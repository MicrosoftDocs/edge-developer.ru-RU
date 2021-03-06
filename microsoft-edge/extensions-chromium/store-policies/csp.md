---
description: Политика безопасности контента для расширений edge (Chromium).
title: Политика безопасности контента (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, центр партнеров, разработчик
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397519"
---
# <a name="content-security-policy-csp"></a>Политика безопасности контента \(CSP\)  

Для смягчения большого класса потенциальных проблем с межсайтовой скриптизаписи система расширения Microsoft Edge включила общую концепцию политики безопасности контента [\(CSP\)][W3CContentSecurityPolicy].  Это вводит некоторые довольно строгие политики, которые делают Расширения более безопасными по умолчанию, и предоставляет вам возможность создавать и применять правила, регулирующие типы контента, которые могут быть загружены и запускаются вашими расширениями и приложениями.  

В общем, CSP работает как механизм блокировки и допуска ресурсов, загруженных или запускающихся вашими расширениями.  Определение разумной политики для расширения позволяет тщательно рассмотреть ресурсы, необходимые вашему расширению, и попросить браузер убедиться, что это единственные ресурсы, к которые ваше расширение имеет доступ.  Политики обеспечивают безопасность над разрешениями хост-разрешений на расширение; это дополнительный уровень защиты, а не замена.  

В Интернете такая политика определяется с помощью http-загона или `meta` элемента.  В системе расширения Microsoft Edge не существует соответствующего механизма.  Вместо этого политика расширения определяется с помощью файла `manifest.json` для расширения следующим образом:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Дополнительные сведения о синтаксисе CSP можно найти в спецификации политики безопасности контента [и][W3CContentSecurityPolicy] статье "Введение в политику безопасности [контента"][HTML5RocksIntroductionContentSecurityPolicy] на HTML5Rocks.  

## <a name="default-policy-restrictions"></a>Ограничения политики по умолчанию  

Пакеты, которые не определяют политику безопасности контента по `manifest_version` умолчанию, не имеют.  Пакеты, которые выбирают `manifest_version` 2, имеют следующую политику безопасности контента по умолчанию.  

```javascript
script-src 'self'; object-src 'self'
```  

Политика добавляет безопасность, ограничив расширения и приложения тремя способами:  

**Отключены Eval и связанные функции**  

Код, похожий на следующий, не работает:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Такая оценка строк JavaScript является распространенным вектором атак XSS.  Вместо этого следует написать код так:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**Inline JavaScript не запускаются**  

Inline JavaScript не запускаются.  Это ограничение запрещает как рядные блоки, так и обработчики событий, например `<script>` `<button onclick="...">` .

Первое ограничение уничтожает огромный класс атак сценариев на меж сайте, что делает невозможным случайное запуск скрипта, предоставляемого вредоносным сторонним участником.  Это, однако, требует, чтобы вы написали код с чистым разделением между контентом и поведением \(что вы, конечно, должны сделать в любом случае, не так ли?\).  Пример может сделать это понятнее.  Вы можете попытаться написать всплывающее всплывающее действие браузера в качестве одного, `pop-up.html` содержащего:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

Чтобы сделать эту работу так, как вы ожидаете, необходимо изменить три вещи:  

*   Определение `clickHandler` должно быть перемещено во внешний файл JavaScript \( `popup.js` может быть хорошей целью).  
*   Определения обработчива событий в рамках должны быть переписаны с точки зрения и `addEventListener` извлечены в `popup.js` .  
    Если вы в настоящее время начинаете программу с помощью подобного кода, подумайте о ее замене, подключившись к событию документа или событию окна в зависимости от ваших `<body onload="main();">` `DOMContentLoaded` `load` требований.  Используйте первое, так как оно обычно запускается быстрее.  

*   Вызов необходимо переписать, чтобы не преобразовать строку `setTimeout` в `"awesome(); totallyAwesome()"` JavaScript для запуска.  
    Эти изменения могут выглядеть следующим образом:  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**Загружаются только локальные скрипты и объектные ресурсы**  

Ресурсы скрипта и объектов могут быть загружены только из пакета расширения, а не из сети в целом.  Это гарантирует, что ваше расширение выполняет только код, который был специально утвержден, что предотвращает злонамеренное перенаправление запроса на ресурс активного сетевого злоумышленника.  

Вместо написания кода, который зависит от загрузки jQuery \(или любой другой библиотеки\) из внешнего CDN, рассмотрите возможность включить конкретную версию jQuery в пакет расширения.  То есть вместо:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

Скачайте файл, включите его в пакет и напишите:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## <a name="relaxing-the-default-policy"></a>Расслабление политики по умолчанию  

**Inline Script**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.  Этот хеш должен быть префиксом использованного алгоритма хеша \(sha256, sha384 или sha512\).  Например, перейдите к [использованию hash для \<script\> элементов][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].  

**Удаленный скрипт**  

Если требуется внешний JavaScript или объектные ресурсы, вы можете в ограниченной степени ослабить политику, разрешив список безопасных источников, из которых следует принимать сценарии.  Убедитесь, что ресурсы, загруженные с повышенными разрешениями расширения, являются именно ресурсами, которые вы ожидаете, и не заменяются активным сетевым злоумышленником.  Так [как][WikiManMiddleAttacks] атаки между посредниками являются тривиальными и неуядаемыми для HTTP, эти истоки не принимаются.  

В настоящее время разработчики могут разрешить истоки со следующими схемами: `blob` `filesystem` , , и `https` `extension` .  Хост-часть происхождения должна быть явно указана для схем `https` `extension` и схем.  Универсальные подгруппы, такие как https:, и не допускаются; поддомен подкарды, `https://*` `https://*.com` такие как `https://*.example.com` разрешены.  Домены в [списке Public Suffix][PublicSuffixList] также рассматриваются как общие домены верхнего уровня.  Чтобы загрузить ресурс из этих доменов, необходимо явно перечислить поддомен.  Например, `https://*.cloudfront.net` не является допустимым, но `https://XXXX.cloudfront.net` и может быть `https://*.XXXX.cloudfront.net` `allowlisted` .  

Для удобства разработки ресурсы, загруженные через HTTP с серверов на локальной машине, могут быть `allowlisted` .  Вы можете разрешить список скриптов и источников объектов в любом порту или `http://127.0.0.1` `http://localhost` .  

> [!NOTE]
> Ограничение для ресурсов, загруженных через HTTP, применяется только к тем ресурсам, которые запускаются напрямую.  Вы по-прежнему свободны, например, для подключения к любому источнику, который вам нравится; политика по умолчанию не ограничивает или любые другие директивы CSP в `XMLHTTPRequest` `connect-src` любом случае.  

Раскованное определение политики, которое позволяет загружать ресурсы скрипта из `example.com` более чем HTTPS, может выглядеть так:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> И `script-src` `object-src` то, и другое определяется политикой.  Microsoft Edge не принимает политику, которая не ограничивает каждое из этих значений \(по крайней мере\) `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**Оценка JavaScript**  

Политика в отношении и связанных с ней функций, таких как , и могут быть `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` смягчены, добавив `unsafe-eval` в политику:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Однако следует избегать расслабляющей политики.  Функции — это пресловутые векторы атак XSS.  

## <a name="tightening-the-default-policy"></a>Ужесточение политики по умолчанию  

Конечно, вы можете ужесточить эту политику в той мере, в какой это позволяет расширение, чтобы повысить безопасность за счет удобства.  Например, чтобы указать, что расширение может загружать ресурсы любого типа \(изображения и так далее\) из связанного пакета расширения, например, может потребоваться `default-src 'self'` политика.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a>Сценарии контента  

Обсуждаемая политика применяется к фоновых страницах и страницам событий расширения.  Более сложной является то, как сценарии контента применяются к сценариям контента расширения.  

Сценарии контента, как правило, не подлежат CSP расширения.  Так как сценарии контента не являются HTML-кодами, основное влияние этого заключается в том, что они могут использовать, даже если CSP расширения не указывает, хотя это не `eval` `unsafe-eval` рекомендуется.  Кроме того, CSP страницы не применяется к сценариям контента.  Более сложными являются теги, которые скрипты контента создают и помещают в `<script>` DOM страницы, на которую они запущены.  Эти ссылки ссылаются на doM вводят скрипты в будущем.  

DoM вводил скрипты, которые запускаются сразу после впрыскивания на страницу, запускается, как вы можете ожидать.  Представьте сценарий контента со следующим кодом в качестве простого примера:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Этот сценарий контента `alert` вызывает немедленное `document.write()` .  Обратите внимание, что это выполняется независимо от политики, которую может указать страница.
Тем не менее, поведение становится более сложным как внутри, что doM вводили сценарий и для любого скрипта, который не сразу запустить после инъекции.  Представьте, что ваше расширение запущено на странице, которая предоставляет связанный CSP, который указывает `script-src 'self'` .  Теперь представьте, что сценарий контента запускает следующий код:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Если пользователь выбирает эту кнопку, `onclick` скрипт не запустится.  Это происходит из-за того, что сценарий не запускался немедленно, а код не интерпретируется до тех пор, пока событие не произойдет, не считается частью сценария контента, поэтому CSP страницы `click` \(не расширения\) ограничивает поведение.  И так как этот CSP не указывает, обработник событий в линии `unsafe-inline` заблокирован.  
Правильный способ реализации желаемого поведения в этом случае может быть добавление обработивляющее в качестве функции из сценария контента `onclick` следующим образом:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Другая аналогичная проблема возникает, если сценарий контента запускается следующим образом:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

В этом случае сценарий запускается и отображается оповещение.  Однако возьмем этот случай:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

При запуске начального сценария вызов `eval` блокируется.  То есть, хотя начальное время запуска сценария разрешено, поведение в скрипте регулируется CSP страницы.  
Таким образом, в зависимости от того, как вы пишете скрипты doM, введенные в расширение, изменения в CSP страницы могут повлиять на поведение вашего расширения.  Так как сценарии контента не влияют на CSP страницы, это отличный повод, чтобы поместить как можно больше поведения вашего расширения в сценарий контента, а не doM вводили скрипты.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Введение в политику безопасности контента | HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "ПРОСМОТР СПИСКА ОБЩЕДОСТУПНЫХ СУФФИКСОВ"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Использование hash для элементов <\> — уровень политики безопасности контента 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Политика безопасности контента 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Атака "Человек в центре" | Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
