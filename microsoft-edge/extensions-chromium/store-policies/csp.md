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
# <a name="content-security-policy-csp"></a><span data-ttu-id="19519-104">Политика безопасности контента \(CSP\)</span><span class="sxs-lookup"><span data-stu-id="19519-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="19519-105">Для смягчения большого класса потенциальных проблем с межсайтовой скриптизаписи система расширения Microsoft Edge включила общую концепцию политики безопасности контента [\(CSP\)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="19519-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="19519-106">Это вводит некоторые довольно строгие политики, которые делают Расширения более безопасными по умолчанию, и предоставляет вам возможность создавать и применять правила, регулирующие типы контента, которые могут быть загружены и запускаются вашими расширениями и приложениями.</span><span class="sxs-lookup"><span data-stu-id="19519-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="19519-107">В общем, CSP работает как механизм блокировки и допуска ресурсов, загруженных или запускающихся вашими расширениями.</span><span class="sxs-lookup"><span data-stu-id="19519-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="19519-108">Определение разумной политики для расширения позволяет тщательно рассмотреть ресурсы, необходимые вашему расширению, и попросить браузер убедиться, что это единственные ресурсы, к которые ваше расширение имеет доступ.</span><span class="sxs-lookup"><span data-stu-id="19519-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="19519-109">Политики обеспечивают безопасность над разрешениями хост-разрешений на расширение; это дополнительный уровень защиты, а не замена.</span><span class="sxs-lookup"><span data-stu-id="19519-109">The policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="19519-110">В Интернете такая политика определяется с помощью http-загона или `meta` элемента.</span><span class="sxs-lookup"><span data-stu-id="19519-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="19519-111">В системе расширения Microsoft Edge не существует соответствующего механизма.</span><span class="sxs-lookup"><span data-stu-id="19519-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="19519-112">Вместо этого политика расширения определяется с помощью файла `manifest.json` для расширения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19519-112">Instead, an Extension policy is defined using the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="19519-113">Дополнительные сведения о синтаксисе CSP можно найти в спецификации политики безопасности контента [и][W3CContentSecurityPolicy] статье "Введение в политику безопасности [контента"][HTML5RocksIntroductionContentSecurityPolicy] на HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="19519-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <a name="default-policy-restrictions"></a><span data-ttu-id="19519-114">Ограничения политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19519-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="19519-115">Пакеты, которые не определяют политику безопасности контента по `manifest_version` умолчанию, не имеют.</span><span class="sxs-lookup"><span data-stu-id="19519-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="19519-116">Пакеты, которые выбирают `manifest_version` 2, имеют следующую политику безопасности контента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19519-116">Packages that choose `manifest_version` 2, have a the follwoing default content security policy.</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="19519-117">Политика добавляет безопасность, ограничив расширения и приложения тремя способами:</span><span class="sxs-lookup"><span data-stu-id="19519-117">The policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="19519-118">Отключены Eval и связанные функции</span><span class="sxs-lookup"><span data-stu-id="19519-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="19519-119">Код, похожий на следующий, не работает:</span><span class="sxs-lookup"><span data-stu-id="19519-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="19519-120">Такая оценка строк JavaScript является распространенным вектором атак XSS.</span><span class="sxs-lookup"><span data-stu-id="19519-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="19519-121">Вместо этого следует написать код так:</span><span class="sxs-lookup"><span data-stu-id="19519-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="19519-122">Inline JavaScript не запускаются</span><span class="sxs-lookup"><span data-stu-id="19519-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="19519-123">Inline JavaScript не запускаются.</span><span class="sxs-lookup"><span data-stu-id="19519-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="19519-124">Это ограничение запрещает как рядные блоки, так и обработчики событий, например `<script>` `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="19519-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="19519-125">Первое ограничение уничтожает огромный класс атак сценариев на меж сайте, что делает невозможным случайное запуск скрипта, предоставляемого вредоносным сторонним участником.</span><span class="sxs-lookup"><span data-stu-id="19519-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="19519-126">Это, однако, требует, чтобы вы написали код с чистым разделением между контентом и поведением \(что вы, конечно, должны сделать в любом случае, не так ли?\).</span><span class="sxs-lookup"><span data-stu-id="19519-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="19519-127">Пример может сделать это понятнее.</span><span class="sxs-lookup"><span data-stu-id="19519-127">An example may make this clearer.</span></span>  <span data-ttu-id="19519-128">Вы можете попытаться написать всплывающее всплывающее действие браузера в качестве одного, `pop-up.html` содержащего:</span><span class="sxs-lookup"><span data-stu-id="19519-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="19519-129">Чтобы сделать эту работу так, как вы ожидаете, необходимо изменить три вещи:</span><span class="sxs-lookup"><span data-stu-id="19519-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="19519-130">Определение `clickHandler` должно быть перемещено во внешний файл JavaScript \( `popup.js` может быть хорошей целью).</span><span class="sxs-lookup"><span data-stu-id="19519-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="19519-131">Определения обработчива событий в рамках должны быть переписаны с точки зрения и `addEventListener` извлечены в `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="19519-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="19519-132">Если вы в настоящее время начинаете программу с помощью подобного кода, подумайте о ее замене, подключившись к событию документа или событию окна в зависимости от ваших `<body onload="main();">` `DOMContentLoaded` `load` требований.</span><span class="sxs-lookup"><span data-stu-id="19519-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="19519-133">Используйте первое, так как оно обычно запускается быстрее.</span><span class="sxs-lookup"><span data-stu-id="19519-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="19519-134">Вызов необходимо переписать, чтобы не преобразовать строку `setTimeout` в `"awesome(); totallyAwesome()"` JavaScript для запуска.</span><span class="sxs-lookup"><span data-stu-id="19519-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="19519-135">Эти изменения могут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19519-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="19519-136">Загружаются только локальные скрипты и объектные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19519-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="19519-137">Ресурсы скрипта и объектов могут быть загружены только из пакета расширения, а не из сети в целом.</span><span class="sxs-lookup"><span data-stu-id="19519-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="19519-138">Это гарантирует, что ваше расширение выполняет только код, который был специально утвержден, что предотвращает злонамеренное перенаправление запроса на ресурс активного сетевого злоумышленника.</span><span class="sxs-lookup"><span data-stu-id="19519-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="19519-139">Вместо написания кода, который зависит от загрузки jQuery \(или любой другой библиотеки\) из внешнего CDN, рассмотрите возможность включить конкретную версию jQuery в пакет расширения.</span><span class="sxs-lookup"><span data-stu-id="19519-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="19519-140">То есть вместо:</span><span class="sxs-lookup"><span data-stu-id="19519-140">That is, instead of:</span></span>  

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

<span data-ttu-id="19519-141">Скачайте файл, включите его в пакет и напишите:</span><span class="sxs-lookup"><span data-stu-id="19519-141">Download the file, include it in your package, and write:</span></span>  

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

## <a name="relaxing-the-default-policy"></a><span data-ttu-id="19519-142">Расслабление политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19519-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="19519-143">Inline Script</span><span class="sxs-lookup"><span data-stu-id="19519-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="19519-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span><span class="sxs-lookup"><span data-stu-id="19519-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="19519-145">Этот хеш должен быть префиксом использованного алгоритма хеша \(sha256, sha384 или sha512\).</span><span class="sxs-lookup"><span data-stu-id="19519-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="19519-146">Например, перейдите к [использованию hash для \<script\> элементов][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span><span class="sxs-lookup"><span data-stu-id="19519-146">For an example, navigate to [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span></span>  

**<span data-ttu-id="19519-147">Удаленный скрипт</span><span class="sxs-lookup"><span data-stu-id="19519-147">Remote Script</span></span>**  

<span data-ttu-id="19519-148">Если требуется внешний JavaScript или объектные ресурсы, вы можете в ограниченной степени ослабить политику, разрешив список безопасных источников, из которых следует принимать сценарии.</span><span class="sxs-lookup"><span data-stu-id="19519-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="19519-149">Убедитесь, что ресурсы, загруженные с повышенными разрешениями расширения, являются именно ресурсами, которые вы ожидаете, и не заменяются активным сетевым злоумышленником.</span><span class="sxs-lookup"><span data-stu-id="19519-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="19519-150">Так [как][WikiManMiddleAttacks] атаки между посредниками являются тривиальными и неуядаемыми для HTTP, эти истоки не принимаются.</span><span class="sxs-lookup"><span data-stu-id="19519-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="19519-151">В настоящее время разработчики могут разрешить истоки со следующими схемами: `blob` `filesystem` , , и `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="19519-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="19519-152">Хост-часть происхождения должна быть явно указана для схем `https` `extension` и схем.</span><span class="sxs-lookup"><span data-stu-id="19519-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="19519-153">Универсальные подгруппы, такие как https:, и не допускаются; поддомен подкарды, `https://*` `https://*.com` такие как `https://*.example.com` разрешены.</span><span class="sxs-lookup"><span data-stu-id="19519-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="19519-154">Домены в [списке Public Suffix][PublicSuffixList] также рассматриваются как общие домены верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="19519-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="19519-155">Чтобы загрузить ресурс из этих доменов, необходимо явно перечислить поддомен.</span><span class="sxs-lookup"><span data-stu-id="19519-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="19519-156">Например, `https://*.cloudfront.net` не является допустимым, но `https://XXXX.cloudfront.net` и может быть `https://*.XXXX.cloudfront.net` `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="19519-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be `allowlisted`.</span></span>  

<span data-ttu-id="19519-157">Для удобства разработки ресурсы, загруженные через HTTP с серверов на локальной машине, могут быть `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="19519-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be `allowlisted`.</span></span>  <span data-ttu-id="19519-158">Вы можете разрешить список скриптов и источников объектов в любом порту или `http://127.0.0.1` `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="19519-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="19519-159">Ограничение для ресурсов, загруженных через HTTP, применяется только к тем ресурсам, которые запускаются напрямую.</span><span class="sxs-lookup"><span data-stu-id="19519-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="19519-160">Вы по-прежнему свободны, например, для подключения к любому источнику, который вам нравится; политика по умолчанию не ограничивает или любые другие директивы CSP в `XMLHTTPRequest` `connect-src` любом случае.</span><span class="sxs-lookup"><span data-stu-id="19519-160">You are still free, for example, to make `XMLHTTPRequest` connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="19519-161">Раскованное определение политики, которое позволяет загружать ресурсы скрипта из `example.com` более чем HTTPS, может выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="19519-161">A relaxed policy definition which allows script resources to be loaded from `example.com` over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="19519-162">И `script-src` `object-src` то, и другое определяется политикой.</span><span class="sxs-lookup"><span data-stu-id="19519-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="19519-163">Microsoft Edge не принимает политику, которая не ограничивает каждое из этих значений \(по крайней мере\) `self` '.</span><span class="sxs-lookup"><span data-stu-id="19519-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="19519-164">Оценка JavaScript</span><span class="sxs-lookup"><span data-stu-id="19519-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="19519-165">Политика в отношении и связанных с ней функций, таких как , и могут быть `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` смягчены, добавив `unsafe-eval` в политику:</span><span class="sxs-lookup"><span data-stu-id="19519-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="19519-166">Однако следует избегать расслабляющей политики.</span><span class="sxs-lookup"><span data-stu-id="19519-166">However, you should avoid relaxing policies.</span></span>  <span data-ttu-id="19519-167">Функции — это пресловутые векторы атак XSS.</span><span class="sxs-lookup"><span data-stu-id="19519-167">The functions are notorious XSS attack vectors.</span></span>  

## <a name="tightening-the-default-policy"></a><span data-ttu-id="19519-168">Ужесточение политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="19519-168">Tightening the default policy</span></span>  

<span data-ttu-id="19519-169">Конечно, вы можете ужесточить эту политику в той мере, в какой это позволяет расширение, чтобы повысить безопасность за счет удобства.</span><span class="sxs-lookup"><span data-stu-id="19519-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="19519-170">Например, чтобы указать, что расширение может загружать ресурсы любого типа \(изображения и так далее\) из связанного пакета расширения, например, может потребоваться `default-src 'self'` политика.</span><span class="sxs-lookup"><span data-stu-id="19519-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a><span data-ttu-id="19519-171">Сценарии контента</span><span class="sxs-lookup"><span data-stu-id="19519-171">Content Scripts</span></span>  

<span data-ttu-id="19519-172">Обсуждаемая политика применяется к фоновых страницах и страницам событий расширения.</span><span class="sxs-lookup"><span data-stu-id="19519-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="19519-173">Более сложной является то, как сценарии контента применяются к сценариям контента расширения.</span><span class="sxs-lookup"><span data-stu-id="19519-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="19519-174">Сценарии контента, как правило, не подлежат CSP расширения.</span><span class="sxs-lookup"><span data-stu-id="19519-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="19519-175">Так как сценарии контента не являются HTML-кодами, основное влияние этого заключается в том, что они могут использовать, даже если CSP расширения не указывает, хотя это не `eval` `unsafe-eval` рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="19519-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="19519-176">Кроме того, CSP страницы не применяется к сценариям контента.</span><span class="sxs-lookup"><span data-stu-id="19519-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="19519-177">Более сложными являются теги, которые скрипты контента создают и помещают в `<script>` DOM страницы, на которую они запущены.</span><span class="sxs-lookup"><span data-stu-id="19519-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="19519-178">Эти ссылки ссылаются на doM вводят скрипты в будущем.</span><span class="sxs-lookup"><span data-stu-id="19519-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="19519-179">DoM вводил скрипты, которые запускаются сразу после впрыскивания на страницу, запускается, как вы можете ожидать.</span><span class="sxs-lookup"><span data-stu-id="19519-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="19519-180">Представьте сценарий контента со следующим кодом в качестве простого примера:</span><span class="sxs-lookup"><span data-stu-id="19519-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="19519-181">Этот сценарий контента `alert` вызывает немедленное `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="19519-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="19519-182">Обратите внимание, что это выполняется независимо от политики, которую может указать страница.</span><span class="sxs-lookup"><span data-stu-id="19519-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="19519-183">Тем не менее, поведение становится более сложным как внутри, что doM вводили сценарий и для любого скрипта, который не сразу запустить после инъекции.</span><span class="sxs-lookup"><span data-stu-id="19519-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="19519-184">Представьте, что ваше расширение запущено на странице, которая предоставляет связанный CSP, который указывает `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="19519-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="19519-185">Теперь представьте, что сценарий контента запускает следующий код:</span><span class="sxs-lookup"><span data-stu-id="19519-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="19519-186">Если пользователь выбирает эту кнопку, `onclick` скрипт не запустится.</span><span class="sxs-lookup"><span data-stu-id="19519-186">If a user chooses that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="19519-187">Это происходит из-за того, что сценарий не запускался немедленно, а код не интерпретируется до тех пор, пока событие не произойдет, не считается частью сценария контента, поэтому CSP страницы `click` \(не расширения\) ограничивает поведение.</span><span class="sxs-lookup"><span data-stu-id="19519-187">This is because the script did not immediately run and code is not interpreted until the `click` event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="19519-188">И так как этот CSP не указывает, обработник событий в линии `unsafe-inline` заблокирован.</span><span class="sxs-lookup"><span data-stu-id="19519-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="19519-189">Правильный способ реализации желаемого поведения в этом случае может быть добавление обработивляющее в качестве функции из сценария контента `onclick` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19519-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="19519-190">Другая аналогичная проблема возникает, если сценарий контента запускается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19519-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="19519-191">В этом случае сценарий запускается и отображается оповещение.</span><span class="sxs-lookup"><span data-stu-id="19519-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="19519-192">Однако возьмем этот случай:</span><span class="sxs-lookup"><span data-stu-id="19519-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="19519-193">При запуске начального сценария вызов `eval` блокируется.</span><span class="sxs-lookup"><span data-stu-id="19519-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="19519-194">То есть, хотя начальное время запуска сценария разрешено, поведение в скрипте регулируется CSP страницы.</span><span class="sxs-lookup"><span data-stu-id="19519-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="19519-195">Таким образом, в зависимости от того, как вы пишете скрипты doM, введенные в расширение, изменения в CSP страницы могут повлиять на поведение вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="19519-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="19519-196">Так как сценарии контента не влияют на CSP страницы, это отличный повод, чтобы поместить как можно больше поведения вашего расширения в сценарий контента, а не doM вводили скрипты.</span><span class="sxs-lookup"><span data-stu-id="19519-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Введение в политику безопасности контента | HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "ПРОСМОТР СПИСКА ОБЩЕДОСТУПНЫХ СУФФИКСОВ"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Использование hash для элементов <\> — уровень политики безопасности контента 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Политика безопасности контента 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Атака "Человек в центре" | Википедия"  

> [!NOTE]
> <span data-ttu-id="19519-202">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19519-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="19519-203">Оригинальная страница находится [здесь](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="19519-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="19519-205">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19519-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
