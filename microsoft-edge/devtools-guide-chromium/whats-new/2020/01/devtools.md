---
description: 3D View, Visual Studio интеграция с Microsoft Edge и другие.
title: Новые возможности в DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a60be4d55d7f6152ed7ce7afd24049f0f5909a4b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398247"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="whats-new-in-devtools-microsoft-edge-81"></a><span data-ttu-id="c7ba8-104">Что нового в DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="c7ba8-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c7ba8-105">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c7ba8-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c7ba8-106">В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="c7ba8-107">Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="c7ba8-108">Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="c7ba8-109">Улучшения доступности для DevTools</span><span class="sxs-lookup"><span data-stu-id="c7ba8-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="c7ba8-110">Команда DevTools внесла 170 изменений в Chromium для решения проблем контрастности цвета, клавиатуры и чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="c7ba8-111">Каждый разработчик, строив веб,должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Средство Performance в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="c7ba8-113">Средство **Performance** в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="c7ba8-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-114">Хотите узнать, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="c7ba8-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="c7ba8-115">Скачайте [сведения о доступности][AccessibilityInsights] и [расширения веб-страниц][WebhintBrowserExtension] для Microsoft Edge, чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="c7ba8-116">Если вы используете считыватели экрана или клавиатуру для навигации по DevTools, отправьте нам свои отзывы, направив на нас твиты или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team) [][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="c7ba8-117">Проблема Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="c7ba8-118">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="c7ba8-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="c7ba8-119">Многие разработчики используют другие средства разработчика, такие как StackOverflow и Visual Studio Code, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="c7ba8-120">Мы рады сообщить о локализации для DevTools, которые теперь можно использовать на одном из 10 языков, кроме английского:</span><span class="sxs-lookup"><span data-stu-id="c7ba8-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="c7ba8-121">Китайский \(Упрощенный\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="c7ba8-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c7ba8-122">Китайский \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="c7ba8-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c7ba8-123">Французский —&#231;ais</span><span class="sxs-lookup"><span data-stu-id="c7ba8-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c7ba8-124">Немецкий - deutsch</span><span class="sxs-lookup"><span data-stu-id="c7ba8-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c7ba8-125">Итальянский - italiano</span><span class="sxs-lookup"><span data-stu-id="c7ba8-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c7ba8-126">Японский - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="c7ba8-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c7ba8-127">Корейский - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="c7ba8-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c7ba8-128">Португальский — portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="c7ba8-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c7ba8-129">Русский  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="c7ba8-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c7ba8-130">Испанский язык — espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="c7ba8-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="c7ba8-131">DevTools автоматически совпадают с языком, который используется для Microsoft `edge://settings/languages` Edge.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="c7ba8-132">Если вы хотите, чтобы Microsoft Edge был на одном языке, а ваши devTools оставались на английском языке, выберите в DevTools, чтобы открыть параметры и отключить язык браузера `F1` **Match.** [][Settings]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, select `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools на немецком языке" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   <span data-ttu-id="c7ba8-134">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="c7ba8-134">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-135">**Сообщения** консоли не локализованы.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-135">**Console** messages are not localized.</span></span>  <span data-ttu-id="c7ba8-136">Только строки, используемые в пользовательском интерфейсе DevTools, отображаются на языке, используемом для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-136">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="c7ba8-137">Если вы хотите использовать DevTools на другом языке, чем [доступные,][PostTweetEdgeDevTools] отправьте нам сообщение в Twitter или выберите значок [Отправка отзывов.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="c7ba8-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="c7ba8-138">Проблема Chromium [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="c7ba8-139">webhint Microsoft Edge extension</span><span class="sxs-lookup"><span data-stu-id="c7ba8-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="c7ba8-140">Расширение Microsoft Edge позволяет легко сканировать веб-страницу и получать отзывы о доступности, совместимости браузера, безопасности, производительности и других данных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="c7ba8-141">Дополнительные публикации [https://webhint.io][Webhint] в .</span><span class="sxs-lookup"><span data-stu-id="c7ba8-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Средство Подсказки в DevTools при установке расширения веб-браузера" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   <span data-ttu-id="c7ba8-143">Средство **Подсказки** в DevTools при установке расширения веб-браузера</span><span class="sxs-lookup"><span data-stu-id="c7ba8-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-144">[Попробуйте расширение веб-браузера в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="c7ba8-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="c7ba8-145">После установки расширения откройте DevTools и выберите **средство Hints.**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="c7ba8-146">Отсюда запустите настраиваемую проверку сайта.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="c7ba8-147">[Переехав в webhint.io,][WebhintBrowserExtension] чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <a name="3d-view"></a><span data-ttu-id="c7ba8-148">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="c7ba8-148">3D View</span></span>  

<span data-ttu-id="c7ba8-149">Использование **3D-представления** для отлаживания веб-приложения путем навигации по объектной модели документа [\(DOM\)][MDNDocumentObjectModel] или контексту укладки [индекса z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="3D-представление в DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   <span data-ttu-id="c7ba8-151">3D-представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="c7ba8-151">The 3D View in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-152">Чтобы получить доступ к 3D-представлению, выберите `Ctrl`  +  `Shift`  +  `P` , введите **в 3D-представлении** и выберите **Показать 3D View**.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-152">To access the 3D View, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="c7ba8-153">Команда Microsoft Edge работает с командой Chromium в пользовательском интерфейсе и добавляет дополнительные функциональные возможности для 3D-представления, поэтому отправьте свои [отзывы.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="c7ba8-153">The Microsoft Edge team is working with the Chromium team on the UI and adding more functionality to the 3D View, so please send your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="c7ba8-154">Проблема Chromium [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-154">Chromium issue [#987787][CR987787]</span></span>  

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="c7ba8-155">Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="c7ba8-155">Visual Studio Code extensions</span></span>  

<span data-ttu-id="c7ba8-156">Команда DevTools также выпустила некоторые расширения для [кода Visual Studio,][VisualStudioCode] которые могут использовать силу DevTools непосредственно из текстового редактора!</span><span class="sxs-lookup"><span data-stu-id="c7ba8-156">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="c7ba8-157">Ознакомьтесь с расширениями ниже:</span><span class="sxs-lookup"><span data-stu-id="c7ba8-157">Check out the extensions below:</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="c7ba8-158">Элементы для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c7ba8-158">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="c7ba8-159">Используйте средство Elements из Visual Studio кода, добавив элементы для [Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio кода.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-159">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Средство Elements в Visual Studio с помощью расширения Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   <span data-ttu-id="c7ba8-161">Средство **Elements** в Visual Studio с помощью расширения Elements for Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c7ba8-161">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-162">Дополнительные сведения вы можете получить в [службе Elements for Microsoft Edge Visual Studio кода.][VisualStudioCodeElementEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-162">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="c7ba8-163">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c7ba8-163">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="c7ba8-164">С [расширением кода Debugger для Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio отладка JavaScript, запущенная в Microsoft Edge непосредственно из Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-164">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Отладка для расширения Microsoft Edge в Visual Studio коде" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   <span data-ttu-id="c7ba8-166">Отладка для расширения Microsoft Edge в Visual Studio коде</span><span class="sxs-lookup"><span data-stu-id="c7ba8-166">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-167">Дополнительные сведения о том, как отчудировать Microsoft Edge от [Visual Studio Code.][VisualStudioCodeDebuggerEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-167">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="c7ba8-168">webhint</span><span class="sxs-lookup"><span data-stu-id="c7ba8-168">webhint</span></span>  

<span data-ttu-id="c7ba8-169">Расширение [веб-Visual Studio][VisualStudioMarketplaceWebhintExtension] кода используется для улучшения `webhint` веб-страницы во время ее написания.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-169">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you are writing it.</span></span>  <span data-ttu-id="c7ba8-170">Это расширение запускает и сообщает диагностику в файлах рабочего пространства на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-170">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Веб-Visual Studio кода, анализируя файл tsx в Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="c7ba8-172">Веб-Visual Studio кода, анализируя `.tsx` файл в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c7ba8-172">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-173">[Узнайте больше о расширении веб-Visual Studio code.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-173">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="c7ba8-174">Visual Studio интеграции</span><span class="sxs-lookup"><span data-stu-id="c7ba8-174">Visual Studio integration</span></span>  

<span data-ttu-id="c7ba8-175">В Visual Studio 2019 версии 16.2 или более поздней версии Visual Studio отладка JavaScript, запущенного в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-175">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="c7ba8-176">[Скачайте Visual Studio 2019,][MicrosoftVisualStudioDownloads] чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="c7ba8-176">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta" lightbox="../../images/2020/01/vs.msft.png":::
   <span data-ttu-id="c7ba8-178">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta</span><span class="sxs-lookup"><span data-stu-id="c7ba8-178">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-179">[Узнайте больше о отладке Microsoft Edge][MicrosoftVisualStudio]из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-179">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="c7ba8-180">Отслеживание сообщений консоли предотвращения</span><span class="sxs-lookup"><span data-stu-id="c7ba8-180">Tracking prevention Console messages</span></span>  

<span data-ttu-id="c7ba8-181">Отслеживание предотвращения — это уникальная функция в Microsoft Edge, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещали.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-181">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you have not visited before.</span></span>  <span data-ttu-id="c7ba8-182">Параметр предотвращения отслеживания по умолчанию — это режим Balanced, который блокирует сторонние трекеры и известные вредоносные трекеры для обеспечения баланса конфиденциальности и совместимости с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-182">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="c7ba8-183">Чтобы получить больше информации о совместимости веб-страницы при блокировке определенных трекеров, \*\*\*\* в консоль добавлялись предупреждающие сообщения, когда трекер заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-183">To give you more insight into the compatibility of your web page when certain trackers are blocked, warning messages were added in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Сообщения в консоли при отслеживании предотвращения блокирования доступа к хранилищам для трекера" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   <span data-ttu-id="c7ba8-185">Сообщения в консоли при **отслеживании** предотвращения блокирования доступа к хранилищам для трекера</span><span class="sxs-lookup"><span data-stu-id="c7ba8-185">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-186">[Дополнительные данные о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-186">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="c7ba8-187">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="c7ba8-187">Announcements from the Chromium project</span></span>  

<span data-ttu-id="c7ba8-188">В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 81, которые были внесены в проект Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-188">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <a name="moto-g4-support-in-device-mode"></a><span data-ttu-id="c7ba8-189">Поддержка Moto G4 в режиме устройства</span><span class="sxs-lookup"><span data-stu-id="c7ba8-189">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="c7ba8-190">После [включения панели инструментов устройства][DeviceToolbar]смоделировать размеры представления Moto G4 из списка **Устройств.**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-190">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Моделирование представления Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   <span data-ttu-id="c7ba8-192">Моделирование представления Moto G4</span><span class="sxs-lookup"><span data-stu-id="c7ba8-192">Simulating a Moto G4 viewport</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-193">Выберите [показать кадр устройства,][DeviceFrame] чтобы показать оборудование Moto G4 вокруг представления.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-193">Choose [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Отображение оборудования Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   <span data-ttu-id="c7ba8-195">Отображение оборудования Moto G4</span><span class="sxs-lookup"><span data-stu-id="c7ba8-195">Showing the Moto G4 hardware</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-196">Связанные функции:</span><span class="sxs-lookup"><span data-stu-id="c7ba8-196">Related features:</span></span>  

*   <span data-ttu-id="c7ba8-197">Откройте [командное меню][CommandMenu] и запустите команду, чтобы сделать снимок экрана представления, включающее оборудование `Capture screenshot` Moto G4 (после включения **show Device Frame).**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-197">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="c7ba8-198">[Перекрой сеть и ЦП,][ThrottleNetworkAndCpu] чтобы более точно имитировать условия просмотра веб-страниц мобильного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-198">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="c7ba8-199">Проблема Chromium [#924693][CR924693]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-199">Chromium issue [#924693][CR924693]</span></span>  

### <a name="cookie-related-updates"></a><span data-ttu-id="c7ba8-200">Обновления, связанные с cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-200">Cookie-related updates</span></span>  

#### <a name="blocked-cookies-in-the-cookies-pane"></a><span data-ttu-id="c7ba8-201">Заблокированные файлы cookie в области cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-201">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="c7ba8-202">В области cookies на панели Приложения теперь отображаются заблокированные файлы cookie с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-202">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Заблокированные файлы cookie в области cookies панели Приложения" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   <span data-ttu-id="c7ba8-204">Заблокированные файлы cookie в области cookies панели Приложения</span><span class="sxs-lookup"><span data-stu-id="c7ba8-204">Blocked cookies in the Cookies pane of the Application panel</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-205">Проблема Chromium [#1030258][CR1030258]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-205">Chromium issue [#1030258][CR1030258]</span></span>  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a><span data-ttu-id="c7ba8-206">Приоритет cookie в области Cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-206">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="c7ba8-207">Таблицы cookies в \*\*\*\* **средствах сети** и приложений теперь включают **столбец Priority.**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-207">The Cookies tables in the **Network** and **Application** tools now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c7ba8-208">Браузеры на основе хрома, такие как Microsoft Edge, являются единственными браузерами, которые поддерживают приоритет cookie.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-208">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="c7ba8-209">Проблема Chromium [#1026879][CR1026879]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-209">Chromium issue [#1026879][CR1026879]</span></span>  

#### <a name="edit-all-cookie-values"></a><span data-ttu-id="c7ba8-210">Изменение всех значений cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-210">Edit all cookie values</span></span>  

<span data-ttu-id="c7ba8-211">Все ячейки в таблицах Cookie теперь можно изменить, за исключением ячеек в столбце **Размер,** так как этот столбец представляет размер сети cookie в bytes.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-211">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="c7ba8-212">Для объяснения каждого столбца перейдите к [Полям][CookiesFields].</span><span class="sxs-lookup"><span data-stu-id="c7ba8-212">For an explanation of each column, navigate to [Fields][CookiesFields].</span></span>  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Редактирование значения cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   <span data-ttu-id="c7ba8-214">Редактирование значения cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-214">Editing a cookie value</span></span>  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a><span data-ttu-id="c7ba8-215">Скопируйте Node.js, чтобы включить данные cookie</span><span class="sxs-lookup"><span data-stu-id="c7ba8-215">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="c7ba8-216">Чтобы получить выражение, которое включает данные cookie, наведите курсор на сетевой запрос, откройте контекстное меню \(правой кнопкой мыши\) и выберите копию копии в качестве `fetch` \*\*\*\*  >  **Node.js.**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-216">To get a `fetch` expression that includes cookie data, hover on a network request, open the contextual menu \(right-click\), and choose **Copy** > **Copy as Node.js fetch**.</span></span>  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Скопируйте как Node.js извлечение" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   <span data-ttu-id="c7ba8-218">Скопируйте как Node.js извлечение</span><span class="sxs-lookup"><span data-stu-id="c7ba8-218">Copy as Node.js fetch</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-219">Проблема Chromium [#1029826][CR1029826]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-219">Chromium issue [#1029826][CR1029826]</span></span>  

### <a name="more-accurate-web-app-manifest-icons"></a><span data-ttu-id="c7ba8-220">Более точные значки манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c7ba8-220">More accurate web app manifest icons</span></span>  

<span data-ttu-id="c7ba8-221">Ранее панель Манифеста в панели Приложений отправляла собственные запросы для отображения значков манифеста веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-221">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="c7ba8-222">В DevTools теперь показан точно такой же значок манифеста, который использует Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-222">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Значки в области Манифест" lightbox="../../images/2020/01/manifesticons.msft.png":::
   <span data-ttu-id="c7ba8-224">Значки в области Манифест</span><span class="sxs-lookup"><span data-stu-id="c7ba8-224">Icons in the Manifest pane</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-225">Проблема Chromium [#985402][CR985402]</span><span class="sxs-lookup"><span data-stu-id="c7ba8-225">Chromium issue [#985402][CR985402]</span></span>  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a><span data-ttu-id="c7ba8-226">Наведите курсор на свойства контента CSS для отображения неоконченных значений</span><span class="sxs-lookup"><span data-stu-id="c7ba8-226">Hover on CSS content properties to display unescaped values</span></span>  

<span data-ttu-id="c7ba8-227">Наведите курсор на значение свойства, чтобы `content` отобразить неоконченную версию значения.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-227">Hover on the value of a `content` property to display the unescaped version of the value.</span></span>  

<span data-ttu-id="c7ba8-228">Например, в этой [демонстрации][CSSContentDemo] при проверке псевдоэлемента в области Стилей отображается сбежавая `p::after` строка: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c7ba8-228">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element an escaped string is displayed in the **Styles** pane:</span></span>  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Сбежавая строка" lightbox="../../images/2020/01/escapedstring.msft.png":::
   <span data-ttu-id="c7ba8-230">Сбежавая строка</span><span class="sxs-lookup"><span data-stu-id="c7ba8-230">The escaped string</span></span>  
:::image-end:::  

<span data-ttu-id="c7ba8-231">При наведении на значение отображается `content` неоконченная величина.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-231">When you hover on the `content` value, the unescaped value is displayed.</span></span>  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Неоконченные значения" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   <span data-ttu-id="c7ba8-233">Неоконченные значения</span><span class="sxs-lookup"><span data-stu-id="c7ba8-233">The unescaped value</span></span>  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a><span data-ttu-id="c7ba8-234">Более подробные ошибки исходных карт в консоли</span><span class="sxs-lookup"><span data-stu-id="c7ba8-234">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="c7ba8-235">Консоль теперь содержит более подробные данные о том, почему не удалось загрузить или размыть исходные карты.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-235">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="c7ba8-236">Ранее он просто предоставил ошибку, не объясняя, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-236">Previously it just provided an error without explaining what went wrong.</span></span>  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Ошибка загрузки исходных карт в консоли" lightbox="../../images/2020/01/sourcemap.msft.png":::
   <span data-ttu-id="c7ba8-238">Ошибка загрузки исходных карт в консоли</span><span class="sxs-lookup"><span data-stu-id="c7ba8-238">A source map loading error in the Console</span></span>  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a><span data-ttu-id="c7ba8-239">Параметр отключения прокрутки в конце файла</span><span class="sxs-lookup"><span data-stu-id="c7ba8-239">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="c7ba8-240">Откройте [параметры,][Settings] а \*\*\*\* затем отключите источники предпочтений, позволяющие прокручивать последний конец файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, которое позволяет прокручиваться хорошо, минуя конец файла в панели  >  \*\*\*\*  >  \*\*\*\* **Источников.**</span><span class="sxs-lookup"><span data-stu-id="c7ba8-240">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Отключение Разрешить прокрутку последнего конца файла" lightbox="../../images/2020/01/settings.msft.png":::
   <span data-ttu-id="c7ba8-242">**Отключение Разрешить прокрутку последнего конца файла в** параметрах</span><span class="sxs-lookup"><span data-stu-id="c7ba8-242">Disabling **Allow scrolling past end of file** in Settings</span></span>  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Прокрутка в конце файла теперь отключена в панели Источники" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   <span data-ttu-id="c7ba8-244">Прокрутка в конце файла теперь отключена в панели Источники</span><span class="sxs-lookup"><span data-stu-id="c7ba8-244">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="c7ba8-245">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="c7ba8-245">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c7ba8-246">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-246">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c7ba8-247">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="c7ba8-247">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="c7ba8-248">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c7ba8-248">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Показать кадр устройства — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Throttle сети и ЦП - Имитация мобильных устройств с режимом устройства в Microsoft Edge DevTools | Документы Майкрософт"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Документы Майкрософт"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Поля — просмотр, редактирование и удаление файлов cookie с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладка для расширения Visual Studio Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы для расширения кода Microsoft Edge Visual Studio microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение предотвращения отслеживания в блоге Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки инсайдеров Microsoft Edge"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Загрузка Visual Studio 2019 г. для Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  

[CR924693]: https://crbug.com/924693 "Запрос на функции. Добавьте Moto G4 в список режимов устройств | Chromium Bugs"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Bugs"  
[CR1026879]: https://crbug.com/1026879 "Вкладка Cookie в консоли разработчиков больше не показывает приоритета | Chromium Bugs"  
[CR1029826]: https://crbug.com/1029826 "сетевой вкладка -> правильно выбрать для запроса -> -> копию, так как извлечение не копирует файлы cookie | Chromium Bugs"  
[CR985402]: https://crbug.com/985402 "Строки ошибки манифеста веб-приложения сбивают с толку | Chromium Bugs"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Chromium Bugs"  
[CR941561]: https://crbug.com/941561 "Локализуемость | Chromium Bugs"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для неоконченного контента CSS"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о доступности"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документа (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузера веб-| документация по веб-сайтам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio расширение кода | документация по веб-сайтам"  

> [!NOTE]
> <span data-ttu-id="c7ba8-285">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7ba8-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c7ba8-286">Оригинальная страница [](https://developers.google.com/web/updates/2020/01/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="c7ba8-286">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c7ba8-288">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7ba8-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  