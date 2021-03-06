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
# <a name="create-an-extension-tutorial---part-1"></a>Создание учебника по расширению — часть 1  

## <a name="overview"></a>Обзор  

Цель этого руководства состоит в создании расширения Microsoft Edge (Chromium), начиная с пустого каталога.  Вы строите расширение, которое всплывающее изображение ДНЯ НАСА. В этом руководстве узнайте, как создать расширение, завершив следующие действия.  

*   Создание `manifest.json` файла.  
*   Добавление значков.  
*   Открытие всплывающее диалоговое окно по умолчанию.  

## <a name="before-you-begin"></a>Перед началом

Чтобы проверить завершенное расширение, которое вы строите в этом учебнике, скачайте [исходный код.][ArchiveExtensionGettingStartedPart1]  

## <a name="step-1-create-a-manifestjson-file"></a>Шаг 1. Создание manifest.jsфайла

Каждый пакет расширения должен `manifest.json` иметь файл в корне.  Манифест содержит сведения о расширении, версии пакета расширения, имени и описания расширения и так далее.  

В следующем фрагменте кода описаны основные сведения, необходимые в `manifest.json` файле.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a>Шаг 2. Добавление значков  

Начните с создания `icons` каталога в проекте для хранения файлов изображений значков.  Значки используются для фонового изображения кнопки, которую пользователи выбирают для запуска расширения.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок на панели инструментов для открытия расширения":::
   Значок на панели инструментов для открытия расширения  
:::image-end:::  

Для значков рекомендуется использовать: 
*   `PNG` формат для значков, но вы также можете использовать `BMP` `GIF` , или `ICO` `JPEG` форматы.  
*   Изображения размером 128 x 128 px, которые при необходимости будут повторно размера в браузере.  

Каталоги проекта должны быть похожи на следующую структуру.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

Затем добавьте значки в `manifest.json` файл. Обновите файл с помощью иконок, чтобы он совпадал со `manifest.json` следующим фрагментом кода. Файлы, `png` перечисленные в следующем коде, доступны в файле загрузки, упомянутом ранее в этой статье.  

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

## <a name="step-3-open-a-default-pop-up-dialog"></a>Шаг 3. Откройте всплывающее окно по умолчанию  

Создайте файл `HTML` для запуска при запуске расширения пользователем.  Создание HTML-файла `popup.html` с именем в каталоге с именем `popup` .  Когда пользователи выбирают значок для запуска расширения, отображается в качестве `popup/popup.html` модального диалогового модуля.  

Добавьте код из следующего фрагмента кода, чтобы `popup.html` отобразить изображение звезд.  

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

Убедитесь, что файл изображения `images/stars.jpeg` добавляется в папку изображений.  Каталоги проекта должны быть похожи на следующую структуру.   

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

Наконец, убедитесь, что вы зарегистрируете всплывающее всплывающее в соответствии с , как показано в следующем фрагменте `manifest.json` `browser_action` кода.  

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

## <a name="next-steps"></a>Дальнейшие действия
Это все, что необходимо для разработки рабочего расширения.  Теперь продолжайте перегружать и тестировать расширение. Дополнительные сведения перейдите в [Sideload расширение][TestExtensionSideload].  

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
