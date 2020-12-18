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
# <span data-ttu-id="4c1ea-104">Создание расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4c1ea-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="4c1ea-105">В этом руководстве вы узнаете, как создать расширение для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="4c1ea-106">В этом примере расширения можно управлять [][MicrosoftDocs] определенными CSS для docs.microsoft.com страниц, включая создание файла манифеста, пользовательского интерфейса, фона и сценариев содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com тело изменено на синий":::
   <span data-ttu-id="4c1ea-108">Docs.microsoft.com тело изменено на синий</span><span class="sxs-lookup"><span data-stu-id="4c1ea-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="4c1ea-109">В этом руководстве предполагается, что у вас есть базовое представление о том, что такое расширение браузера и как оно работает.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="4c1ea-110">Подробнее о структурах расширений см. в подстройке ["Структура" расширения.][MDNAnatomyExtension]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="4c1ea-111">Скачайте код для полного [примера на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="4c1ea-112">Создание файла манифеста</span><span class="sxs-lookup"><span data-stu-id="4c1ea-112">Building the manifest file</span></span>  

<span data-ttu-id="4c1ea-113">Для начала создайте каталог для расширения и назовите `color-changer` его.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="4c1ea-114">Внутри `color-changer` папки создайте файл с именем `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="4c1ea-115">Файл необходим для всех расширений и предоставляет важные сведения для расширения, от имени расширения `manifest.json` до разрешений.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="4c1ea-116">В этом руководстве вы можете найти все ключи манифеста, которые необходимо использовать в этом руководстве, но список всех поддерживаемых и рекомендуемых ключей манифеста см. в поддерживаемых [ключах манифеста.][ExtensionsApisupportManifestKeys]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="4c1ea-117">Внутри `manifest.json` добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-117">Inside `manifest.json`, add the following code.</span></span>  

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

### <span data-ttu-id="4c1ea-118">Определения ключей манифеста</span><span class="sxs-lookup"><span data-stu-id="4c1ea-118">Manifest key definitions</span></span>  

| <span data-ttu-id="4c1ea-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-119">Key</span></span> | <span data-ttu-id="4c1ea-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="4c1ea-121">name</span><span class="sxs-lookup"><span data-stu-id="4c1ea-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="4c1ea-122">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="4c1ea-123">author</span><span class="sxs-lookup"><span data-stu-id="4c1ea-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="4c1ea-124">Автор расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="4c1ea-125">version</span><span class="sxs-lookup"><span data-stu-id="4c1ea-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="4c1ea-126">Номер версии расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="4c1ea-127">description</span><span class="sxs-lookup"><span data-stu-id="4c1ea-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="4c1ea-128">Описание расширения, отображаемого в разделе "О" меню расширения в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="4c1ea-129">permissions</span><span class="sxs-lookup"><span data-stu-id="4c1ea-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="4c1ea-130">Массив строк, запрашивающих разрешения для расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="4c1ea-131">Для расширения запрашиваются разрешения на просмотр посещаемых веб-сайтов \("tabs"\) и обновление контента по URL-адресам, совпадающих с " `*://docs.microsoft.com/*` ".</span><span class="sxs-lookup"><span data-stu-id="4c1ea-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="4c1ea-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="4c1ea-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="4c1ea-133">Содержит сведения для значка.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-133">Contains the information for an icon.</span></span> <span data-ttu-id="4c1ea-134">Значок размещен на панели инструментов Microsoft Edge справа от адресной панели.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="4c1ea-135">browser_action ключевых определений</span><span class="sxs-lookup"><span data-stu-id="4c1ea-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="4c1ea-136">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-136">Key</span></span> | <span data-ttu-id="4c1ea-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="4c1ea-138">Значок, используемый на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="4c1ea-139">Текст, который отображается, когда пользователь наведите курсор на значок на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="4c1ea-140">Путь к HTML-файлу для всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="4c1ea-141">После создания файла манифеста вам потребуется пользовательский интерфейс для расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="4c1ea-142">Создание всплывающее окна</span><span class="sxs-lookup"><span data-stu-id="4c1ea-142">Creating the pop-up</span></span>  

<span data-ttu-id="4c1ea-143">Для расширения создайте всплывающее видео для пользовательского интерфейса, как по приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Всплывающий интерфейс расширения":::
   <span data-ttu-id="4c1ea-145">Всплывающий интерфейс расширения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="4c1ea-146">Создайте файл с `popup.html` именем в корне `color-changer` папки.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="4c1ea-147">В paste the following code into `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-147">Paste the following code into `popup.html`.</span></span>  

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

<span data-ttu-id="4c1ea-148">В `popup.html` окну создается заголовок, абзац и три кнопки \(Aliceblue, Reset и Reset\).</span><span class="sxs-lookup"><span data-stu-id="4c1ea-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="4c1ea-149">Теперь создайте папку с именем `css` и внутри создайте файл с именем `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="4c1ea-150">Добавьте стили ниже.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-150">Add the styles below.</span></span>  

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

<span data-ttu-id="4c1ea-151">Эта CSS-команда предоставляет нашему расширению некоторые базовые стили.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="4c1ea-152">Вы можете добавить дополнительные стили для настройки расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="4c1ea-153">Затем необходимо создать файл JavaScript, который взаимодействует с всплывающим файлом.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="4c1ea-154">Создайте `js` папку и файл с именем `popup.js` внутри.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="4c1ea-155">`popup.js`Обновим следующий код.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-155">Update `popup.js` with the following code.</span></span>  

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

<span data-ttu-id="4c1ea-156">In `popup.js` , the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="4c1ea-157">С помощью метода [tabs.insertCSS()][MDNApiTabsInsertcss] вы вставляете указанный CSS на [][MicrosoftDocs] страницу, которая изменяет загон в docs.microsoft.com на другой цвет при нажатии указанной кнопки.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="4c1ea-158">Теперь, когда у вас есть основные функции всплывающих элементов, добавьте значки в расширение.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="4c1ea-159">Добавление значков</span><span class="sxs-lookup"><span data-stu-id="4c1ea-159">Adding icons</span></span>  

<span data-ttu-id="4c1ea-160">Значки используются для представления расширения на панели инструментов браузера, меню расширений и других местах.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="4c1ea-161">Скачайте [значки для расширения на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="4c1ea-162">Дополнительные сведения о значках расширений в Microsoft Edge см. в [руководстве по проектированию.][ExtensionsGuidesDesignIcons]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="4c1ea-163">Скачав значки расширения, сохраните их в `images` папке `color-changer` внутри.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="4c1ea-164">Значок, который отображается на панели инструментов, устанавливается с помощью ключа browser_action, который вы уже добавили в файл манифеста в более `default_icon` ранней части. [][MDNManifestjsonBrowserAction]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="4c1ea-165">Ключ `icons` определяет, какие значки следует использовать в меню параметров расширений.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="4c1ea-166">Ниже вы указываете несколько значков разных размеров с учетом разных разрешений экрана.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="4c1ea-167">Имя значков и высоты значков в `25` `48` пикселях.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="4c1ea-168">Вmanifest.js[ включаем][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] ключ верхнего уровня `icons` для .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="4c1ea-169">Определения ключей манифеста</span><span class="sxs-lookup"><span data-stu-id="4c1ea-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="4c1ea-170">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-170">Key</span></span> | <span data-ttu-id="4c1ea-171">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="4c1ea-172">значки</span><span class="sxs-lookup"><span data-stu-id="4c1ea-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="4c1ea-173">Значки для расширения с парами "ключ-значение" размера изображения и путем изображения относительно `px` корневого каталога расширения.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="4c1ea-174">Используйте значки, `inactive##.png` расположенные в папке изображений, далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="4c1ea-175">Тестирование расширения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-175">Testing the extension</span></span>  

<span data-ttu-id="4c1ea-176">Теперь, когда вы добавили пользовательский интерфейс и создали значки, протестировать расширение.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="4c1ea-177">По шагам по [добавлению расширения][ExtensionsGuidesAddingRemovingExtensionsAdding] в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="4c1ea-178">После этого вернись к этому руководству.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="4c1ea-179">После добавления расширения перейдите на любую [docs.microsoft.com][MicrosoftDocs] страницу.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="4c1ea-180">После нажатия действия браузера вы увидите следующее всплывающее всплывающее ок.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="4c1ea-181">Цвет docs.microsoft.com [также][MicrosoftDocs] должен меняться.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Docs.microsoft.com, измененный на Aliceblue":::
         <span data-ttu-id="4c1ea-183">Docs.microsoft.com, измененный на Aliceblue</span><span class="sxs-lookup"><span data-stu-id="4c1ea-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Docs.microsoft.com заголовка изменена на "lk"":::
         <span data-ttu-id="4c1ea-185">Docs.microsoft.com заголовка изменена на "lk"</span><span class="sxs-lookup"><span data-stu-id="4c1ea-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="4c1ea-186">Если у вас возникнут ошибки или функции, [][ExtensionsGuidesDebuggingExtensions] которые не работают, см. руководство по расширениям отладки или скачайте полный пример на [GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="4c1ea-187">Добавление контента и фоновых сценариев</span><span class="sxs-lookup"><span data-stu-id="4c1ea-187">Adding content and background scripts</span></span>  

<span data-ttu-id="4c1ea-188">Перейдите на один шаг дальше и добавьте логику, чтобы отключить работу расширения на страницах [за][MicrosoftDocs] пределами docs.microsoft.com домена.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="4c1ea-189">Сначала необходимо создать [сценарий контента.][MDNContentScripts]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="4c1ea-190">Далее необходимо создать скрипты контента, которые работают в контексте определенной веб-страницы, имеют доступ к содержимому веб-страницы и могут взаимодействовать с фоновые сценарии.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="4c1ea-191">В каталоге создайте файл с именем и `js` `content.js` добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

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

<span data-ttu-id="4c1ea-192">Этот сценарий получает URL-адрес текущей страницы и проверяет, находится ли текущая страница в docs.microsoft.com `document.location.href` домене. [][MicrosoftDocs]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="4c1ea-193">Если страница находится не в домене [docs.microsoft.com][MicrosoftDocs] \(например, \), пути к неактивным значкам \(серые значки\) отправляются в фоновый сценарий с помощью  [https://www.bing.com/][|::ref1::|] [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span><span class="sxs-lookup"><span data-stu-id="4c1ea-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="4c1ea-194">Необходимо обновитьmanifest.js[ в файле,][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] включив следующий `content_scripts` ключ.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="4c1ea-195">Определения ключей манифеста</span><span class="sxs-lookup"><span data-stu-id="4c1ea-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="4c1ea-196">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-196">Key</span></span> | <span data-ttu-id="4c1ea-197">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="4c1ea-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="4c1ea-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="4c1ea-199">Содержит сведения о том, какие скрипты контента должен загрузить браузер.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="4c1ea-200">content_scripts ключевых определений</span><span class="sxs-lookup"><span data-stu-id="4c1ea-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="4c1ea-201">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-201">Key</span></span> | <span data-ttu-id="4c1ea-202">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="4c1ea-203">\(required\)</span><span class="sxs-lookup"><span data-stu-id="4c1ea-203">\(required\)</span></span> | <span data-ttu-id="4c1ea-204">Шаблон URL-адреса для совпадения перед загрузкой скрипта контента.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="4c1ea-205">Сценарий, который должен быть загружен на url-адреса, совпадающие.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="4c1ea-206">Указывает, куда внедряются файлы JavaScript из `js` ключа.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="4c1ea-207">Затем необходимо создать [фоновый сценарий.][MDNAnatomyExtensionBackgroundScripts]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="4c1ea-208">Фоновые сценарии запускаются в фоновом режиме браузера, запускаются независимо от времени существования веб-страницы или окна браузера и могут взаимодействовать со сценариями содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="4c1ea-209">Внутри папки создайте файл с именем и `js` `background.js` добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

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

<span data-ttu-id="4c1ea-210">Метод [runtime.onMessage][MDNApiRuntimeOnmessage] прослушивает [runtime.sendMessage()][MDNApiRuntimeSendmessage] из скрипта содержимого.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="4c1ea-211">Если домен страницы не является [docs.microsoft.com,][MicrosoftDocs]метод [browserAction.setIcon()][MDNApiBrowseractionSeticon] задает пути значков к неактивным изображениям.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="4c1ea-212">Скрипт также отключает действие браузера \([browserAction.disable][MDApiBrowseractionDisable]\), чтобы пользователи не могли щелкнуть действие браузера за пределами docs.microsoft.com [страницы.][MicrosoftDocs]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="4c1ea-213">Необходимо добавить фоновый сценарий в файлmanifest.js[файла.][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="4c1ea-214">Добавьте следующий `background` ключ в манифест.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="4c1ea-215">Определения ключей манифеста</span><span class="sxs-lookup"><span data-stu-id="4c1ea-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="4c1ea-216">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-216">Key</span></span> | <span data-ttu-id="4c1ea-217">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="4c1ea-218">фон</span><span class="sxs-lookup"><span data-stu-id="4c1ea-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="4c1ea-219">Содержит фоновые сценарии.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="4c1ea-220">определения фонового ключа</span><span class="sxs-lookup"><span data-stu-id="4c1ea-220">background Key definitions</span></span>  

| <span data-ttu-id="4c1ea-221">Раздел</span><span class="sxs-lookup"><span data-stu-id="4c1ea-221">Key</span></span> | <span data-ttu-id="4c1ea-222">Сведения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="4c1ea-223">Путь к файлу JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="4c1ea-224">(обязательно)</span><span class="sxs-lookup"><span data-stu-id="4c1ea-224">(required)</span></span> | <span data-ttu-id="4c1ea-225">Это должно быть установлено `true` или `false` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="4c1ea-226">Если за установлено, фоновый сценарий загружается и сохраняется для `true` всего раздела просмотра.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="4c1ea-227">Если за установлено, фоновый сценарий загружается с задержкой и сохраняется `false` для сеанса просмотра.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="4c1ea-228">Перезагрузите расширение и протестировать его еще раз.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-228">Reload your extension and test again.</span></span>  <span data-ttu-id="4c1ea-229">Чтобы перезагрузить расширение, \*\*\*\* щелкните ... для параметров и многого другого в Microsoft Edge, щелкните "Расширения", \*\*\*\* выберите расширение \(**Изменение**цвета \) и щелкните "Перезагрузить **расширение".**</span><span class="sxs-lookup"><span data-stu-id="4c1ea-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="4c1ea-230">Теперь откройте новую вкладку или обновите существующую вкладку, которая не является [docs.microsoft.com][MicrosoftDocs] страницей.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="4c1ea-231">Вы увидите неактивный значок и не сможете щелкнуть действие браузера.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="4c1ea-232">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="4c1ea-232">Congratulations!</span></span>  <span data-ttu-id="4c1ea-233">Вы создали расширение для Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="4c1ea-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="4c1ea-234">Просмотреть [полный пример на GitHub.][GithubMicrosoftEdgeExtensionsDemosColorChanger]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="4c1ea-235">Продолжайте читать, чтобы узнать больше о расширениях.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="4c1ea-236">Написание более сложного расширения</span><span class="sxs-lookup"><span data-stu-id="4c1ea-236">Writing a more complex extension</span></span>  

<span data-ttu-id="4c1ea-237">Хотите написать более сложное расширение?</span><span class="sxs-lookup"><span data-stu-id="4c1ea-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="4c1ea-238">Посмотрите на расширениеIfy на MDN в статье, [второе расширение.][MDNYourSecondWebextension]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="4c1ea-239">Модель расширения для Microsoft Edge немного отличается от модели расширений для [][MDNYourSecondWebextension] Firefox. Расширение Построительно, созданное во втором расширении, было адаптировано для работы в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="4c1ea-240">Ознакомьтесь с ней на [сайте GitHub.][GithubMicrosoftEdgeExtensionsDemosBeastify]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="4c1ea-241">Во время хождения по статье на MDN, [второе][MDNYourSecondWebextension]расширение, помните о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="4c1ea-242">Интерфейсы API</span><span class="sxs-lookup"><span data-stu-id="4c1ea-242">APIs</span></span>  

<span data-ttu-id="4c1ea-243">Список [поддерживаемых API][ExtensionsAPIsupportApis] расширений в Microsoft Edge см. на странице поддерживаемых API расширений.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="4c1ea-244">Размеры значков</span><span class="sxs-lookup"><span data-stu-id="4c1ea-244">Icon sizes</span></span>  

<span data-ttu-id="4c1ea-245">Предпочитаемый размер значка расширения для Microsoft Edge: `20px` `25px` , , и `30px` `40px` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="4c1ea-246">Другие поддерживаемые размеры: `19px` `35px` , и `38px` .</span><span class="sxs-lookup"><span data-stu-id="4c1ea-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="4c1ea-247">Дополнительные сведения о размерах значков и практических методиках см. в руководстве [по проектированию.][ExtensionsGuidesDesign]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="4c1ea-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4c1ea-248">JavaScript</span></span>  

<span data-ttu-id="4c1ea-249">Модель расширения для Microsoft Edge не поддерживает обещания JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="4c1ea-250">Вместо этого используйте вызовы.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-250">Instead, use callbacks.</span></span>  <span data-ttu-id="4c1ea-251">Дополнительные примеры использования вызовов в расширении можно посмотреть [][GithubMicrosoftEdgeExtensionsDemosQuickPrint] на демонстрационных роликах "Быстрая печать" и "Замена [текста".][GithubMicrosoftEdgeExtensionsDemosTextSwap]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="4c1ea-252">Пойдите по [примеру "Быстрая][GithubMicrosoftEdgeExtensionsDemosQuickPrint] печать" в следующем видео.</span><span class="sxs-lookup"><span data-stu-id="4c1ea-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="4c1ea-253">Manifest.jsв</span><span class="sxs-lookup"><span data-stu-id="4c1ea-253">Manifest.json</span></span>  

*   <span data-ttu-id="4c1ea-254">Ключ `author` необходим в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4c1ea-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="4c1ea-255">Ключ `activeTab` не поддерживается в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4c1ea-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="4c1ea-256">Дополнительные сведения о [расширениях браузера][MDNBrowserExtensions]см. в [веб-документы MDN.][MDNWebDocs]</span><span class="sxs-lookup"><span data-stu-id="4c1ea-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

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
