---
description: Создайте расширение, которое всплывет на снимке дня в НАСА
title: Создание учебника по расширению — часть 1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, web development, html, css, javascript, developer, extensions
ms.openlocfilehash: dfbe7893ce576c223d2b1d39ec21b6c5f46d8356
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397512"
---
# <a name="create-an-extension-tutorial---part-1"></a><span data-ttu-id="dd281-104">Создание учебника по расширению — часть 1</span><span class="sxs-lookup"><span data-stu-id="dd281-104">Create an extension tutorial - Part 1</span></span>  

## <a name="overview"></a><span data-ttu-id="dd281-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="dd281-105">Overview</span></span>  

<span data-ttu-id="dd281-106">Цель этого руководства состоит в создании расширения Microsoft Edge (Chromium), начиная с пустого каталога.</span><span class="sxs-lookup"><span data-stu-id="dd281-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span>  <span data-ttu-id="dd281-107">Вы строите расширение, которое всплывающее изображение ДНЯ НАСА.</span><span class="sxs-lookup"><span data-stu-id="dd281-107">You are building an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="dd281-108">В этом руководстве узнайте, как создать расширение, завершив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dd281-108">In this tutorial, learn how to create an extension by completing the following actions.</span></span>  

*   <span data-ttu-id="dd281-109">Создание `manifest.json` файла.</span><span class="sxs-lookup"><span data-stu-id="dd281-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="dd281-110">Добавление значков.</span><span class="sxs-lookup"><span data-stu-id="dd281-110">Adding icons.</span></span>  
*   <span data-ttu-id="dd281-111">Открытие всплывающее диалоговое окно по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dd281-111">Opening a default pop-up dialog.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="dd281-112">Перед началом</span><span class="sxs-lookup"><span data-stu-id="dd281-112">Before you Begin</span></span>

<span data-ttu-id="dd281-113">Чтобы проверить завершенное расширение, которое вы строите в этом учебнике, скачайте [исходный код.][ArchiveExtensionGettingStartedPart1]</span><span class="sxs-lookup"><span data-stu-id="dd281-113">To test out the completed extension that you are building in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <a name="step-1-create-a-manifestjson-file"></a><span data-ttu-id="dd281-114">Шаг 1. Создание manifest.jsфайла</span><span class="sxs-lookup"><span data-stu-id="dd281-114">Step 1: Create a manifest.json file</span></span>

<span data-ttu-id="dd281-115">Каждый пакет расширения должен `manifest.json` иметь файл в корне.</span><span class="sxs-lookup"><span data-stu-id="dd281-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="dd281-116">Манифест содержит сведения о расширении, версии пакета расширения, имени и описания расширения и так далее.</span><span class="sxs-lookup"><span data-stu-id="dd281-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="dd281-117">В следующем фрагменте кода описаны основные сведения, необходимые в `manifest.json` файле.</span><span class="sxs-lookup"><span data-stu-id="dd281-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a><span data-ttu-id="dd281-118">Шаг 2. Добавление значков</span><span class="sxs-lookup"><span data-stu-id="dd281-118">Step 2: Add icons</span></span>  

<span data-ttu-id="dd281-119">Начните с создания `icons` каталога в проекте для хранения файлов изображений значков.</span><span class="sxs-lookup"><span data-stu-id="dd281-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="dd281-120">Значки используются для фонового изображения кнопки, которую пользователи выбирают для запуска расширения.</span><span class="sxs-lookup"><span data-stu-id="dd281-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок на панели инструментов для открытия расширения":::
   <span data-ttu-id="dd281-122">Значок на панели инструментов для открытия расширения</span><span class="sxs-lookup"><span data-stu-id="dd281-122">Icon on the toolbar to open your extension</span></span>  
:::image-end:::  

<span data-ttu-id="dd281-123">Для значков рекомендуется использовать:</span><span class="sxs-lookup"><span data-stu-id="dd281-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="dd281-124">формат для значков, но вы также можете использовать `BMP` `GIF` , или `ICO` `JPEG` форматы.</span><span class="sxs-lookup"><span data-stu-id="dd281-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="dd281-125">Изображения размером 128 x 128 px, которые при необходимости будут повторно размера в браузере.</span><span class="sxs-lookup"><span data-stu-id="dd281-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="dd281-126">Каталоги проекта должны быть похожи на следующую структуру.</span><span class="sxs-lookup"><span data-stu-id="dd281-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="dd281-127">Затем добавьте значки в `manifest.json` файл.</span><span class="sxs-lookup"><span data-stu-id="dd281-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="dd281-128">Обновите файл с помощью иконок, чтобы он совпадал со `manifest.json` следующим фрагментом кода.</span><span class="sxs-lookup"><span data-stu-id="dd281-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="dd281-129">Файлы, `png` перечисленные в следующем коде, доступны в файле загрузки, упомянутом ранее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="dd281-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a><span data-ttu-id="dd281-130">Шаг 3. Откройте всплывающее окно по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dd281-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="dd281-131">Создайте файл `HTML` для запуска при запуске расширения пользователем.</span><span class="sxs-lookup"><span data-stu-id="dd281-131">Now, create a `HTML` file to run when the user launches your extension.</span></span>  <span data-ttu-id="dd281-132">Создание HTML-файла `popup.html` с именем в каталоге с именем `popup` .</span><span class="sxs-lookup"><span data-stu-id="dd281-132">Create the HTML file named `popup.html` in a directory named `popup`.</span></span>  <span data-ttu-id="dd281-133">Когда пользователи выбирают значок для запуска расширения, отображается в качестве `popup/popup.html` модального диалогового модуля.</span><span class="sxs-lookup"><span data-stu-id="dd281-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="dd281-134">Добавьте код из следующего фрагмента кода, чтобы `popup.html` отобразить изображение звезд.</span><span class="sxs-lookup"><span data-stu-id="dd281-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

<span data-ttu-id="dd281-135">Убедитесь, что файл изображения `images/stars.jpeg` добавляется в папку изображений.</span><span class="sxs-lookup"><span data-stu-id="dd281-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="dd281-136">Каталоги проекта должны быть похожи на следующую структуру.</span><span class="sxs-lookup"><span data-stu-id="dd281-136">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

<span data-ttu-id="dd281-137">Наконец, убедитесь, что вы зарегистрируете всплывающее всплывающее в соответствии с , как показано в следующем фрагменте `manifest.json` `browser_action` кода.</span><span class="sxs-lookup"><span data-stu-id="dd281-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## <a name="next-steps"></a><span data-ttu-id="dd281-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="dd281-138">Next steps</span></span>
<span data-ttu-id="dd281-139">Это все, что необходимо для разработки рабочего расширения.</span><span class="sxs-lookup"><span data-stu-id="dd281-139">That is everything you need to develop a working extension.</span></span>  <span data-ttu-id="dd281-140">Теперь продолжайте перегружать и тестировать расширение.</span><span class="sxs-lookup"><span data-stu-id="dd281-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="dd281-141">Дополнительные сведения перейдите в [Sideload расширение][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="dd281-141">For more information, navigate to [Sideload an extension][TestExtensionSideload].</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Завершенный источник пакета расширения | Документы Майкрософт"

[TestExtensionSideload]: ./extension-sideloading.md "Проверьте расширение (sideloading) | Документы Майкрософт"
