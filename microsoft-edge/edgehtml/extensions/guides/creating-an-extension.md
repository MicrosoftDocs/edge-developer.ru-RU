---
description: Узнайте, как создать расширение Microsoft Edge
title: Создание расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 15cb7a4c187210c885b5d75770bda1c590a8c5d1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235785"
---
# Создание расширения Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

В этом руководстве вы узнаете, как создать расширение для Microsoft Edge.  В этом примере расширения можно управлять [][MicrosoftDocs] определенными CSS для docs.microsoft.com страниц, включая создание файла манифеста, пользовательского интерфейса, фона и сценариев содержимого.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com тело изменено на синий":::
   Docs.microsoft.com тело изменено на синий
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

В этом руководстве предполагается, что у вас есть базовое представление о том, что такое расширение браузера и как оно работает.  Подробнее о структурах расширений см. в подстройке ["Структура" расширения.][MDNAnatomyExtension]  

Скачайте код для полного [примера на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]  

## Создание файла манифеста  

Для начала создайте каталог для расширения и назовите `color-changer` его.  

Внутри `color-changer` папки создайте файл с именем `manifest.json` .  Файл необходим для всех расширений и предоставляет важные сведения для расширения, от имени расширения `manifest.json` до разрешений.  

> [!NOTE] 
> В этом руководстве вы можете найти все ключи манифеста, которые необходимо использовать в этом руководстве, но список всех поддерживаемых и рекомендуемых ключей манифеста см. в поддерживаемых [ключах манифеста.][ExtensionsApisupportManifestKeys]  

Внутри `manifest.json` добавьте следующий код.  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### Определения ключей манифеста  

| Раздел | Сведения |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Имя расширения.  |  
| [author][MDNManifestjsonAuthor] | Автор расширения.  |  
| [version][MDNManifestjsonVersion] | Номер версии расширения.  |  
| [description][MDNManifestjsonDescription] | Описание расширения, отображаемого в разделе "О" меню расширения в Microsoft Edge.  |  
| [permissions][MDNManifestjsonPermissions] | Массив строк, запрашивающих разрешения для расширения.  Для расширения запрашиваются разрешения на просмотр посещаемых веб-сайтов \("tabs"\) и обновление контента по URL-адресам, совпадающих с " `*://docs.microsoft.com/*` ".  |  
| [browser_action][MDNManifestjsonBrowserAction] | Содержит сведения для значка. Значок размещен на панели инструментов Microsoft Edge справа от адресной панели.  |  

#### browser_action ключевых определений  

| Раздел | Сведения |  
|:--- |:--- |  
| `default_icon` | Значок, используемый на панели инструментов.  |  
| `default_title` | Текст, который отображается, когда пользователь наведите курсор на значок на панели инструментов.  |  
| `default_popup` | Путь к HTML-файлу для всплывающее окно.  |  

После создания файла манифеста вам потребуется пользовательский интерфейс для расширения.  

## Создание всплывающее окна  

Для расширения создайте всплывающее видео для пользовательского интерфейса, как по приведенной ниже.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Всплывающий интерфейс расширения":::
   Всплывающий интерфейс расширения
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Создайте файл с `popup.html` именем в корне `color-changer` папки.  В paste the following code into `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

В `popup.html` окну создается заголовок, абзац и три кнопки \(Aliceblue, Reset и Reset\).  

Теперь создайте папку с именем `css` и внутри создайте файл с именем `styles.css` .  Добавьте стили ниже.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Эта CSS-команда предоставляет нашему расширению некоторые базовые стили.  Вы можете добавить дополнительные стили для настройки расширения.  

Затем необходимо создать файл JavaScript, который взаимодействует с всплывающим файлом.  Создайте `js` папку и файл с именем `popup.js` внутри.  `popup.js`Обновим следующий код.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

In `popup.js` , the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.  С помощью метода [tabs.insertCSS()][MDNApiTabsInsertcss] вы вставляете указанный CSS на [][MicrosoftDocs] страницу, которая изменяет загон в docs.microsoft.com на другой цвет при нажатии указанной кнопки.  

Теперь, когда у вас есть основные функции всплывающих элементов, добавьте значки в расширение.  

## Добавление значков  

Значки используются для представления расширения на панели инструментов браузера, меню расширений и других местах.  Скачайте [значки для расширения на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChangerImages] Дополнительные сведения о значках расширений в Microsoft Edge см. в [руководстве по проектированию.][ExtensionsGuidesDesignIcons]  

Скачав значки расширения, сохраните их в `images` папке `color-changer` внутри.  

Значок, который отображается на панели инструментов, устанавливается с помощью ключа browser_action, который вы уже добавили в файл манифеста в более `default_icon` ранней части. [][MDNManifestjsonBrowserAction]  

Ключ `icons` определяет, какие значки следует использовать в меню параметров расширений.  Ниже вы указываете несколько значков разных размеров с учетом разных разрешений экрана.  Имя значков и высоты значков в `25` `48` пикселях.  

Вmanifest.js[ включаем][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] ключ верхнего уровня `icons` для .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Определения ключей манифеста  

| Раздел | Сведения |  
|:--- |:--- |  
| [значки][MDNManifestjsonIcons] | Значки для расширения с парами "ключ-значение" размера изображения и путем изображения относительно `px` корневого каталога расширения. |  

> [!NOTE]
> Используйте значки, `inactive##.png` расположенные в папке изображений, далее в этом руководстве.  

## Тестирование расширения  

Теперь, когда вы добавили пользовательский интерфейс и создали значки, протестировать расширение.  По шагам по [добавлению расширения][ExtensionsGuidesAddingRemovingExtensionsAdding] в Microsoft Edge.  После этого вернись к этому руководству.  

После добавления расширения перейдите на любую [docs.microsoft.com][MicrosoftDocs] страницу.  После нажатия действия браузера вы увидите следующее всплывающее всплывающее ок.  Цвет docs.microsoft.com [также][MicrosoftDocs] должен меняться.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.microsoft.com, измененный на Aliceblue":::
         Docs.microsoft.com, измененный на Aliceblue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.microsoft.com заголовка изменена на lk":::
         Docs.microsoft.com заголовка изменена на "lk" :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Если у вас возникнут ошибки или функции, [][ExtensionsGuidesDebuggingExtensions] которые не работают, см. руководство по расширениям отладки или скачайте полный пример на [GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]  

## Добавление контента и фоновых сценариев  

Перейдите на один шаг дальше и добавьте логику, чтобы отключить работу расширения на страницах [за][MicrosoftDocs] пределами docs.microsoft.com домена.  

Сначала необходимо создать [сценарий контента.][MDNContentScripts]  Далее необходимо создать скрипты контента, которые работают в контексте определенной веб-страницы, имеют доступ к содержимому веб-страницы и могут взаимодействовать с фоновые сценарии.  В каталоге создайте файл с именем и `js` `content.js` добавьте следующий код.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Этот сценарий получает URL-адрес текущей страницы и проверяет, находится ли текущая страница в docs.microsoft.com `document.location.href` домене. [][MicrosoftDocs]  Если страница находится не в домене [docs.microsoft.com][MicrosoftDocs] \(например, \), пути к неактивным значкам \(серые значки\) отправляются в фоновый сценарий с помощью  [https://www.bing.com/][|::ref1::|] [runtime.sendMessage()][MDNApiRuntimeSendmessage].  

Необходимо обновитьmanifest.js[ в файле,][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] включив следующий `content_scripts` ключ.  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Определения ключей манифеста  

| Раздел | Сведения |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Содержит сведения о том, какие скрипты контента должен загрузить браузер. |  

#### content_scripts ключевых определений  

| Раздел | Сведения |  
|:--- |:---- |  
| `matches` \(required\) | Шаблон URL-адреса для совпадения перед загрузкой скрипта контента. |  
| `js` | Сценарий, который должен быть загружен на url-адреса, совпадающие. |  
| `run_at` | Указывает, куда внедряются файлы JavaScript из `js` ключа. |  

Затем необходимо создать [фоновый сценарий.][MDNAnatomyExtensionBackgroundScripts]  Фоновые сценарии запускаются в фоновом режиме браузера, запускаются независимо от времени существования веб-страницы или окна браузера и могут взаимодействовать со сценариями содержимого.  

Внутри папки создайте файл с именем и `js` `background.js` добавьте следующий код.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

Метод [runtime.onMessage][MDNApiRuntimeOnmessage] прослушивает [runtime.sendMessage()][MDNApiRuntimeSendmessage] из скрипта содержимого.  Если домен страницы не является [docs.microsoft.com,][MicrosoftDocs]метод [browserAction.setIcon()][MDNApiBrowseractionSeticon] задает пути значков к неактивным изображениям.  

Скрипт также отключает действие браузера \([browserAction.disable][MDApiBrowseractionDisable]\), чтобы пользователи не могли щелкнуть действие браузера за пределами docs.microsoft.com [страницы.][MicrosoftDocs]  

Необходимо добавить фоновый сценарий в файлmanifest.js[файла.][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]  Добавьте следующий `background` ключ в манифест.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Определения ключей манифеста  

| Раздел | Сведения|  
|:--- |:--- |  
| [фон][MDNManifestjsonBackground] | Содержит фоновые сценарии. |  

#### определения фонового ключа  

| Раздел | Сведения |  
|:--- |:--- |  
| `scripts` | Путь к файлу JavaScript. |  
| `persistent` (обязательно) | Это должно быть установлено `true` или `false` .  Если за установлено, фоновый сценарий загружается и сохраняется для `true` всего раздела просмотра.  Если за установлено, фоновый сценарий загружается с задержкой и сохраняется `false` для сеанса просмотра. |  

Перезагрузите расширение и протестировать его еще раз.  Чтобы перезагрузить расширение, **** щелкните ... для параметров и многого другого в Microsoft Edge, щелкните "Расширения", **** выберите расширение \(**Изменение**цвета \) и щелкните "Перезагрузить **расширение".**  

Теперь откройте новую вкладку или обновите существующую вкладку, которая не является [docs.microsoft.com][MicrosoftDocs] страницей.  Вы увидите неактивный значок и не сможете щелкнуть действие браузера.  

Поздравляем!  Вы создали расширение для Microsoft Edge!  Просмотреть [полный пример на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]  Продолжайте читать, чтобы узнать больше о расширениях.  

## Написание более сложного расширения  

Хотите написать более сложное расширение?  Посмотрите на расширениеIfy на MDN в статье, [второе расширение.][MDNYourSecondWebextension]  Модель расширения для Microsoft Edge немного отличается от модели расширений для [][MDNYourSecondWebextension] Firefox. Расширение Построительно, созданное во втором расширении, было адаптировано для работы в Microsoft Edge.  Ознакомьтесь с ней на [сайте GitHub.][GithubMicrosoftEdgeExtensionsDemosBeastify]  

Во время хождения по статье на MDN, [второе][MDNYourSecondWebextension]расширение, помните о следующих разделах.  

### Интерфейсы API  

Список [поддерживаемых API][ExtensionsAPIsupportApis] расширений в Microsoft Edge см. на странице поддерживаемых API расширений.  

### Размеры значков  

Предпочитаемый размер значка расширения для Microsoft Edge: `20px` `25px` , , и `30px` `40px` .  Другие поддерживаемые размеры: `19px` `35px` , и `38px` .  Дополнительные сведения о размерах значков и практических методиках см. в руководстве [по проектированию.][ExtensionsGuidesDesign]  

### JavaScript  

Модель расширения для Microsoft Edge не поддерживает обещания JavaScript.  Вместо этого используйте вызовы.  Дополнительные примеры использования вызовов в расширении можно посмотреть [][GithubMicrosoftEdgeExtensionsDemosQuickPrint] на демонстрационных роликах "Быстрая печать" и "Замена [текста".][GithubMicrosoftEdgeExtensionsDemosTextSwap]  

Пойдите по [примеру "Быстрая][GithubMicrosoftEdgeExtensionsDemosQuickPrint] печать" в следующем видео.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest.jsв  

*   Ключ `author` необходим в Microsoft Edge  
*   Ключ `activeTab` не поддерживается в Microsoft Edge  

Дополнительные сведения о [расширениях браузера][MDNBrowserExtensions]см. в [веб-документы MDN.][MDNWebDocs]  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Добавление расширения — добавление, перемещение и удаление расширений для Microsoft Edge | Документы Майкрософт"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Отладка расширений | Документы Майкрософт"  
[ExtensionsGuidesDesign]: ./design.md "Рекомендации по проектированию расширений Microsoft Edge | Документы Майкрософт"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Значки — рекомендации по проектированию расширений Microsoft Edge | Документы Майкрософт"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md " Поддерживаемые API | Документы Майкрософт"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Поддерживаемые ключи манифеста | Документы Майкрософт"  

[MicrosoftDocs]: https://docs.microsoft.com "Документы Майкрософт"  

[MDNWebDocs]: https://developer.mozilla.org "Веб-документы MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Расширения браузера | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Структура расширения | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Фоновые сценарии — структура расширения | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction.disable() — API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction.setIcon() — API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "runtime.onMessage — API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "runtime.sendMessage() — API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "tabs — API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "tabs.insertCSS() — API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Сценарии содержимого | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "author — manifest.js| MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "background — manifest.jsв | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action — manifest.js| MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts — manifest.js| MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "description — manifest.js| MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "icons — manifest.js| MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "name — manifest.js| MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "permissions — manifest.js| MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "version — manifest.js| MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Второе расширение | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Theify - MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Изменение цвета — MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Images - Color Changer - MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest.js— изменение цвета — MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Быстрая печать — MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Замена текста — MicrosoftEdge/MicrosoftEdge-Extensions-Demos | GitHub"  
