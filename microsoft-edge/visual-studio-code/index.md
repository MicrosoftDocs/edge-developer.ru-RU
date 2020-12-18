---
description: Microsoft Edge (Chromium) и Visual Studio кода
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230693"
---
# <span data-ttu-id="0f01f-104">Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="0f01f-104">Visual Studio Code overview</span></span>  

<span data-ttu-id="0f01f-105">[Visual Studio код —][VisualStudioCodeDocs] это облегченный, но мощный редактор исходных кодов.</span><span class="sxs-lookup"><span data-stu-id="0f01f-105">[Visual Studio Code][VisualStudioCodeDocs] is a lightweight, but powerful source code editor.</span></span>  <span data-ttu-id="0f01f-106">[Visual Studio код][VisualStudioCodeDocs] доступен для Windows, Linux и macOS.</span><span class="sxs-lookup"><span data-stu-id="0f01f-106">[Visual Studio Code][VisualStudioCodeDocs] is available for Windows, Linux, and macOS.</span></span>  <span data-ttu-id="0f01f-107">Он включает встроенную поддержку JavaScript, TypeScript и Node.js, поэтому это отличное средство для веб-разработчиков перед его настройкой.</span><span class="sxs-lookup"><span data-stu-id="0f01f-107">It includes built-in support for JavaScript, TypeScript, and Node.js, so it is a great tool for web developers before you customize it.</span></span>  <span data-ttu-id="0f01f-108">Если вы еще не используете его, скачайте Visual Studio [Code.][VisualstudioCode]</span><span class="sxs-lookup"><span data-stu-id="0f01f-108">If you are not using it yet, download [Visual Studio Code][VisualstudioCode].</span></span>  

## <span data-ttu-id="0f01f-109">Расширения</span><span class="sxs-lookup"><span data-stu-id="0f01f-109">Extensions</span></span>  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

<span data-ttu-id="0f01f-110">Чтобы получить какие-либо расширения, которые выделены ниже, перейдите в Visual Studio `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` Code.</span><span class="sxs-lookup"><span data-stu-id="0f01f-110">To acquire any of the extensions highlighted below, navigate to Extensions \(select `Ctrl`+`Shift`+`X` on Windows/Linux or `Command`+`Shift`+`X` on macOS\) in Visual Studio Code.</span></span>  

<span data-ttu-id="0f01f-111">Найщите в Marketplace определенное расширение и выберите **"Установить".**</span><span class="sxs-lookup"><span data-stu-id="0f01f-111">Search the Marketplace for the specific extension and choose **Install**.</span></span>  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Установка отладщика для Microsoft Edge Visual Studio кода" lightbox="./media/vscode-debugger-install.png":::
   <span data-ttu-id="0f01f-113">Установка **отладщика для Microsoft Edge** Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="0f01f-113">Install the **Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Отладка для расширения microsoft Edge Visual Studio Code" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         <span data-ttu-id="0f01f-115">**Отладка для Microsoft Edge** Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="0f01f-115">**Debugger for Microsoft Edge** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="0f01f-116">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f01f-116">Debugger for Microsoft Edge</span></span>](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         <span data-ttu-id="0f01f-118">**Средства Microsoft Edge для Visual Studio кода** Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="0f01f-118">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="0f01f-119">Microsoft Edge Tools for Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0f01f-119">Microsoft Edge Tools for Visual Studio Code</span></span>](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio code extension" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         <span data-ttu-id="0f01f-121">**webhint** Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="0f01f-121">**webhint** Visual Studio Code extension</span></span>  
      :::image-end:::  
      [<span data-ttu-id="0f01f-122">webhint</span><span class="sxs-lookup"><span data-stu-id="0f01f-122">webhint</span></span>](#webhint)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="0f01f-123">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0f01f-123">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="0f01f-124">С помощью [расширения Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code отладите код javaScript переднего `console.log()` [Visual Studio.][VisualstudioCode]</span><span class="sxs-lookup"><span data-stu-id="0f01f-124">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line-by-line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode].</span></span>  
      
<span data-ttu-id="0f01f-125">С помощью средства отладки можно запустить или присоединить к Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="0f01f-125">Using the Debugger tool, you may launch or attach to both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0f01f-126">Чтобы получить по walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension.][VisualStudioCodeDebuggerEdge]</span><span class="sxs-lookup"><span data-stu-id="0f01f-126">For a walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension][VisualStudioCodeDebuggerEdge].</span></span>  <span data-ttu-id="0f01f-127">Выберите следующее изображение, чтобы увидеть расширение в действии.</span><span class="sxs-lookup"><span data-stu-id="0f01f-127">Choose the following image to see the extension in action.</span></span>  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Отладка для расширения Visual Studio Edge в действии" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="0f01f-129">**Отладка для Microsoft Edge** Visual Studio расширения кода в действии</span><span class="sxs-lookup"><span data-stu-id="0f01f-129">**Debugger for Microsoft Edge** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="0f01f-130">Microsoft Edge Tools for Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0f01f-130">Microsoft Edge Tools for Visual Studio Code</span></span>

<span data-ttu-id="0f01f-131">С помощью [расширения Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code используйте средство **Elements** браузера Microsoft Edge в Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="0f01f-131">With the [Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code extension, use the **Elements** tool of the Microsoft Edge browser within Visual Studio Code.</span></span>  <span data-ttu-id="0f01f-132">Используйте его для следующих действий.</span><span class="sxs-lookup"><span data-stu-id="0f01f-132">Use it for the following actions.</span></span>  

*   <span data-ttu-id="0f01f-133">Присоединить к экземпляру или запустить экземпляр Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0f01f-133">Attach to an instance or launch an instance of Microsoft Edge.</span></span>  
*   <span data-ttu-id="0f01f-134">Отображение HTML-структуры времени работы.</span><span class="sxs-lookup"><span data-stu-id="0f01f-134">Display the runtime HTML structure.</span></span>  
*   <span data-ttu-id="0f01f-135">Обновим макет.</span><span class="sxs-lookup"><span data-stu-id="0f01f-135">Update the layout.</span></span>  
*   <span data-ttu-id="0f01f-136">Устранение проблем со стилем.</span><span class="sxs-lookup"><span data-stu-id="0f01f-136">Fix styling issues.</span></span>  
    
<span data-ttu-id="0f01f-137">Для получения дополнительных сведений перейдите в [microsoft Edge Tools for Visual Studio Code Visual Studio Code extension.][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]</span><span class="sxs-lookup"><span data-stu-id="0f01f-137">For more information, navigate to [Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension][VisualStudioCodeMicrosoftEdgeDevtoolsExtension].</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension in action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   <span data-ttu-id="0f01f-139">**Средства Microsoft Edge для Visual Studio кода** Visual Studio расширения кода в действии</span><span class="sxs-lookup"><span data-stu-id="0f01f-139">**Microsoft Edge Tools for Visual Studio Code** Visual Studio Code extension in action</span></span>  
:::image-end:::  

## <span data-ttu-id="0f01f-140">webhint</span><span class="sxs-lookup"><span data-stu-id="0f01f-140">webhint</span></span>  
      
<span data-ttu-id="0f01f-141">Используйте [webhint][WebhintMain], настраиваемый инструмент linting, чтобы улучшить следующие функциональные возможности сайта.</span><span class="sxs-lookup"><span data-stu-id="0f01f-141">Use [webhint][WebhintMain], a customizable linting tool, to improve the following functionality of your site.</span></span>  

*   <span data-ttu-id="0f01f-142">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="0f01f-142">Accessibility</span></span>
*   <span data-ttu-id="0f01f-143">Производительность</span><span class="sxs-lookup"><span data-stu-id="0f01f-143">Performance</span></span>
*   <span data-ttu-id="0f01f-144">Совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="0f01f-144">Cross-browser compatibility</span></span>
*   <span data-ttu-id="0f01f-145">Совместимость PWA</span><span class="sxs-lookup"><span data-stu-id="0f01f-145">PWA compatibility</span></span>
*   <span data-ttu-id="0f01f-146">Безопасность</span><span class="sxs-lookup"><span data-stu-id="0f01f-146">Security</span></span>

<span data-ttu-id="0f01f-147">Он проверяет код на наличие методик написания кода и распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="0f01f-147">It checks your code for coding practices and common errors.</span></span> <span data-ttu-id="0f01f-148">Проект webhint с открытым исходным кодом, изначально разработанный командой Microsoft Edge, теперь является частью [OpenJS Foundation.][OpenjsFoundation]</span><span class="sxs-lookup"><span data-stu-id="0f01f-148">The webhint open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="0f01f-149">Команда Microsoft Edge продолжает участвовать в веб-проектах вместе с веб-разработчиками в сообществе.</span><span class="sxs-lookup"><span data-stu-id="0f01f-149">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана с расширением webhint Visual Studio Code" lightbox="./media/webhint-extension.png":::
   <span data-ttu-id="0f01f-151">Снимок экрана **с расширением webhint** Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="0f01f-151">Screenshot of **webhint** Visual Studio Code extension</span></span>  
:::image-end:::  
      
<span data-ttu-id="0f01f-152">Выявляйте и устраняйте проблемы на своем веб-сайте, добавляя расширение [webhint для Visual Studio Code.][VisualstudioMarketplaceWebhint]</span><span class="sxs-lookup"><span data-stu-id="0f01f-152">Identify and fix problems in your website by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="0f01f-153">Подсказки проверяют HTML, CSS, JavaScript, TypeScript и другие.</span><span class="sxs-lookup"><span data-stu-id="0f01f-153">Hints examine HTML, CSS, JavaScript, TypeScript, and more.</span></span>  <span data-ttu-id="0f01f-154">Подсказки отображаются как подчеркнутые и суммарные в **области** "Проблемы".</span><span class="sxs-lookup"><span data-stu-id="0f01f-154">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  
      
<span data-ttu-id="0f01f-155">Для получения дополнительных сведений [перейдите к how to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span><span class="sxs-lookup"><span data-stu-id="0f01f-155">For more information, navigate to [How to use webhint in Visual Studio Code][VisualStudioCodeWebhint].</span></span>  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Debugger for Microsoft Edge Visual Studio code extension | Документы Майкрософт"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools для расширения Visual Studio кода | Документы Майкрософт"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio code Extension | Документы Майкрософт"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio кода"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio кода"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
