---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Узнайте, как перенос расширения Chrome в Microsoft Edge с помощью расширения Microsoft Edge набор средств.
title: Перенос расширений Chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f226d79dbc9efdc43eb68bfb353fa12748198371
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235692"
---
# <span data-ttu-id="7e0c3-104">Перенос расширения из Chrome в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7e0c3-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7e0c3-105">Перенос расширения из Chrome в Microsoft Edge проще с помощью microsoft [Edge Extension набор средств.](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb)</span><span class="sxs-lookup"><span data-stu-id="7e0c3-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="7e0c3-106">Это средство разработчика преобразует распакованное расширение Chrome в распакованное расширение Microsoft Edge, переверив API-интерфейсы и выявив все ошибки в `manifest.json` файле.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="7e0c3-107">Мосты API</span><span class="sxs-lookup"><span data-stu-id="7e0c3-107">API bridges</span></span>
<span data-ttu-id="7e0c3-108">Чтобы обеспечить беспрепятственное перенос API Chrome в поддерживаемые API Microsoft Edge, в папку расширения добавляются два сценария.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="7e0c3-109">Эти сценарии мост API (polyfiling при необходимости), что означает, что вам не придется беспокоиться об изменении какого-либо кода Chrome в фоновых сценариях или сценариях содержимого.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="7e0c3-110">После преобразования они будут включены в файл манифеста расширения с `"-ms-preload"` ключом:</span><span class="sxs-lookup"><span data-stu-id="7e0c3-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="7e0c3-111">Использование расширения Microsoft Edge набор средств</span><span class="sxs-lookup"><span data-stu-id="7e0c3-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="7e0c3-112">Следующие инструкции подробно о том, как преобразовать расширение Chrome для запуска в Microsoft Edge в выпуске Юбилейного обновления Windows 10:</span><span class="sxs-lookup"><span data-stu-id="7e0c3-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="7e0c3-113">Установите microsoft [Edge Extension набор средств](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="7e0c3-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="7e0c3-114">Сделайте копию папки расширения Chrome для безопасного сохраняемого.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="7e0c3-115">Процесс преобразования переопишет код.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="7e0c3-116">Запустите microsoft Edge Extension набор средств и загрузите копию расширения.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![кнопка расширения загрузки](./../media/save-folder.png)
4. <span data-ttu-id="7e0c3-118">Исправлять все ошибки, которые сообщаются в текстовом редакторе средства.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="7e0c3-119">Выберите "Повторно проверить", чтобы проверить ошибки после внося исправлений.</span><span class="sxs-lookup"><span data-stu-id="7e0c3-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![extension-toolkit finding errors](./../media/extension-toolkit.png)
5. <span data-ttu-id="7e0c3-121">Выберите "Сохранить файлы".</span><span class="sxs-lookup"><span data-stu-id="7e0c3-121">Select "Save files".</span></span>

<span data-ttu-id="7e0c3-122">Теперь вы можете выйти из наборов инструментов и загрузить расширение в Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="7e0c3-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="7e0c3-123">Вы можете искать известные проблемы платформы с помощью отслеживания проблем [EdgeHTML.](http://issues.microsoftedge.com)</span><span class="sxs-lookup"><span data-stu-id="7e0c3-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="7e0c3-124">Если вы считаете, что нашли что-то новое, [откройте проблему!](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)</span><span class="sxs-lookup"><span data-stu-id="7e0c3-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>
