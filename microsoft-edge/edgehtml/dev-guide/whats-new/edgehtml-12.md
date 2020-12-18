---
description: На этой странице представлен обзор новых функций EdgeHTML 12.
title: Новые функции и API в EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a96d75ff7decf2c6efdfee3be94736707fea5a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235471"
---
# Новые возможности EdgeHTML 12  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge представляет EdgeHTML, новый "живой" обдвижок, разработанный с возможностью обеспечения связи в своей основе, чтобы гарантировать, что вы всегда получаете последнюю и наибольшую веб-платформу Windows.  Microsoft Edge представляет собой чистую отладку от прошлых, не из устаревшего кода, необходимого для поддержки элементов управления ActiveX, объектов-помощников браузера \(BHOs\) и других устаревших методик веб-разработки.  Кроме того, Microsoft Edge поддерживает встроенные PDF-файлы.  С IE11 устаревшие режимы документов были устаревшими, а в Microsoft Edge инфраструктура браузера для их поддержки не существует.  Дополнительные сведения [можно узнать в IEBlog.](/archive/blogs/ie/living-on-the-edge-our-next-step-in-interoperability)  

Вот изменения, внесенные с помощью EdgeHTML 12 в первоначальном выпуске [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) \(07/2015, сборка 10240\).  Общие сведения об изменениях браузера Microsoft [](https://blogs.windows.com/msedgedev/2015/02/26) Edge см. в отложенном от прошлом: о рождения нового обдвижка веб-отрисовки Майкрософт и о разрыве с прошлых, часть 2. Досвидая [ActiveX, VBScript, attachEvent...](https://blogs.windows.com/msedgedev/2015/05/06).  

Ниже приводится permalink для следующего списка изменений:  [https://aka.ms/devguide_edgehtml_12](./edgehtml-12.md) .  

## Новые возможности  

### Политика безопасности контента 1.0  

Теперь в Microsoft Edge реализована политика безопасности контента \(CSP\) 1.0.  Стандарт безопасности CSP позволяет веб-разработчикам контролировать ресурсы \(сценарий, CSS, подключаемый модуль, изображения и т. д.), которые определенная страница может получать или выполнять с целью предотвращения межсайтовых сценариев \(XSS\), clickjacking и других атак с целью встраивания кода, целью которых является выполнение вредоносного содержимого в контексте доверенной веб-страницы.  Дополнительные [сведения о](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) CSP в Microsoft Edge можно узнать в политике безопасности контента.  

### Эффекты фильтра  

Microsoft Edge предоставляет простой способ добавления визуальных эффектов в элементы.  С помощью свойства можно добавлять размытия, настраивать яркость, добавлять тени, изменять прозрачность и другие `filter` элементы.  С помощью исключительно CSS можно применить несколько эффектов фильтра к одному элементу и анимировать фильтры.  Дополнительные сведения см. в [эффектах фильтра.](https://developer.mozilla.org/docs/Web/CSS/filter)  

### JavaScript  

Поддержка JavaScript немного зависит от окончательной версии Internet Explorer \(IE11\) и Microsoft Edge.  К новым функциям в Edge относятся:  

:::row:::
   :::column span="1":::
      **Выписки**  
   :::column-end:::
   :::column span="2":::
      [class](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) \(experimental\), [for... of](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Объекты**  
   :::column-end:::
   :::column span="2":::
      [Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [Proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [Symbol](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [WeakSet](/scripting/javascript/reference/weakset-object-javascript)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Функции**  
   :::column-end:::
   :::column span="2":::
      [acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint) [,т](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [isNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [raw](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Методы**  
   :::column-end:::
   :::column span="2":::
      [includes](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) \(Array\), [repeat](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) \(String\), [values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) \(Array\)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Другие возможности**  
   :::column-end:::
   :::column span="2":::
      [Functions](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) \(experimental\), [Generators](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators),  [Iterators](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [Regular Expression `y` flag](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) \(experimental\), [Template strings](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), [Unicode code point escape characters](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)  
   :::column-end:::
:::row-end:::  

Сравнение поддержки JavaScript в internet Explorer, Microsoft Edge и приложениях Microsoft Store см. в [сведениях о версии JavaScript.](./javascript-version-information.md)  

### Захват мультимедиа и потоки  

В Microsoft Edge появилась поддержка API захвата мультимедиа и потоков на основе спецификации [W3C Media Capture and Streams.](https://w3c.github.io/mediacapture-main/getusermedia.html)  Эти API JavaScript позволяют веб-страницам получать доступ к устройствам захвата мультимедиа, таким как веб-камеры или микрофоны, с разрешения пользователя.  С помощью API захвата мультимедиа и потоков можно создавать такие сценарии, как захват фотографии с помощью веб-камеры или захват голосового сообщения с микрофона.  Узнайте больше о записи мультимедиа в Microsoft Edge в блоге [разработчика Microsoft Edge.](https://blogs.windows.com/msedgedev/2015/05/13)  

### Новый элемент и атрибуты HTML  

*   `meter` element  
*   `picture` element  
*   `template` element  
*   `image` element: `srcset` and `sizes` attributes \(Microsoft Edge Developer [blog post](https://blogs.windows.com/msedgedev/2015/06/08)\)  
*   `selectionDirection` attribute  
*   `input type=time` и `input type=datetime-local`  

### API RTC объекта  

Объект Real-Time Communications \(ORTC\) позволяет передавать мультимедиа \(аудио и/или видео\) в режиме реального времени непосредственно между веб-браузерами, мобильными устройствами и серверами через API JavaScript.  Дополнительные сведения об ORTC в Microsoft Edge можно узнать в разделе руководства разработчика по [объекту RTC API.](https://ortc.org)  

### Представление чтения  

Microsoft Edge предоставляет представление чтения для более упрощенного и похожего на книгу чтения веб-страниц без отвлекания от несвязанных или другого дополнительного содержимого на странице.  В адресной панели или с помощью кнопки "Чтение" можно включать или отключать представление чтения (значок книги) в адресной панели или с помощью `Ctrl` + `Shift` + `R` .  Дополнительные [сведения можно получить в](../browser-features/reading-view.md) представлении чтения.  

### Обнаружение службы поиска  

Интеграция с богатым поиском встроена в адресную планку Microsoft Edge, включая предложения поиска, результаты из Интернета, историю браузеров и избранное.  Microsoft Edge следует спецификации [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) для обнаружения и использования поставщиков веб-поиска.  Если вы поставщик [поиска,](../browser-features/search-provider-discovery.md) узнайте больше о том, как убедиться, что Microsoft Edge поддерживает вашу службу.  

### Поддержка API WebKit  

Для улучшения совместимости Microsoft Edge поддерживает различные API `-webkit-` с префиксами.  Полный список поддерживаемых `-webkit-` API можно использовать в каталоге [API.](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit)  

### Веб-аудио  

Microsoft Edge представляет поддержку спецификации [веб-аудио API W3C.](https://webaudio.github.io/web-audio-api)  Веб-звук — это высокоуровневый API JavaScript для обработки и синтеза звука в веб-приложениях для предоставления богатых звуковых и музыкальных функций.  Хотя элемент HTML5 обеспечивает базовое воспроизведение потокового звука, API Web Audio предоставляет ряд API, которые позволяют играть несколько звуков с жесткой синхронизацией и применять эффекты усиления, исчезания, переходы и базовые эффекты для смешанного `audio` звука.  Узнайте больше о [web Audio](.. /multimedia/web-audio.md в руководстве разработчика и в блоге [разработчика Microsoft Edge.](https://blogs.windows.com/msedgedev/2015/05/19)  

### Веб-драйвер  

[API-интерфейс W3C WebDriver](https://w3.org/TR/webdriver) — это неотвеязающий от языка интерфейс и протокол провода, позволяющий программам или сценариям управлять поведением веб-браузера.  WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие с пользователем.  Это отличается от unit tests JavaScript, так как WebDriver имеет доступ к функциям и сведениям, которые JavaScript, запущенный в браузере, не имеет, и он может более точно имитировать события пользователя или события на уровне ОС.  WebDriver также может управлять тестированием в нескольких окнах, вкладок и веб-страницы в одном тестовом сеансе.  Дополнительные сведения о том, как начать работу с WebDriver для Microsoft Edge, можно найти в [WebDriver.](../../webdriver/index.md)  

## Новые API в EdgeHTML 12  

Ниже полный список новых API в EdgeHTML 12.  Они перечислены в формате `[interface name].[api name]` .  

 > [!NOTE] 
 > Многие из этих API были доступны в IE11.  Данные ниже для EdgeHTML 12 предлагаются в качестве базового плана для сравнения начальной версии EdgeHTML с более поздними версиями.  

<iframe height='580' scrolling='no' title='Новые API в EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. API для новых перьев в <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> EdgeHTML 12 в </a> Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation ) на </a> <a href='https://codepen.io'> </a> CodePen.</iframe>  
