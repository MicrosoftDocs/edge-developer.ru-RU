---
description: Улучшения доступности, использование DevTools на других языках и другие.
title: Новые возможности в DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 80f870d22c81479bff9b9413717ccc7c323d9a05
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397561"
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

# <a name="whats-new-in-devtools-microsoft-edge-80"></a><span data-ttu-id="2f9c6-104">Новые возможности в DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="2f9c6-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2f9c6-105">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f9c6-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="2f9c6-106">В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="2f9c6-107">Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="2f9c6-108">Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="accessibility-improvements-to-the-devtools"></a><span data-ttu-id="2f9c6-109">Улучшения доступности для DevTools</span><span class="sxs-lookup"><span data-stu-id="2f9c6-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="2f9c6-110">Команда DevTools внесла 170 изменений в Chromium для решения проблем контрастности цвета, клавиатуры и чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="2f9c6-111">Каждый разработчик, строив веб,должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-111">Every developer building the web should be able to use the DevTools.</span></span>  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Средство Performance в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   <span data-ttu-id="2f9c6-113">Средство **Performance** в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="2f9c6-113">The **Performance** tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-114">Хотите узнать, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="2f9c6-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="2f9c6-115">Скачайте [сведения о доступности][AccessibilityInsights] и [расширения веб-страниц][WebhintBrowserExtension] для Microsoft Edge, чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="2f9c6-116">Если вы используете считыватели экрана или клавиатуру для [][PostTweetEdgeDevTools] навигации по DevTools, отправьте свои отзывы, направив на нас твиты или отправив значок [Отправка](#getting-in-touch-with-microsoft-edge-devtools-team) отзывов!</span><span class="sxs-lookup"><span data-stu-id="2f9c6-116">If you use screen readers or the keyboard to navigate around the DevTools, send your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="2f9c6-117">Проблема Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-117">Chromium issue [#963183][CR963183]</span></span>  

### <a name="using-the-devtools-in-other-languages"></a><span data-ttu-id="2f9c6-118">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="2f9c6-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="2f9c6-119">Многие разработчики используют другие средства разработчика, такие как StackOverflow и Visual Studio Code, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-119">Many developers use other developer tools, like StackOverflow and Visual Studio Code, in their native language, not just in English.</span></span>  <span data-ttu-id="2f9c6-120">Мы рады сообщить о локализации для DevTools, которые теперь можно использовать на одном из 10 языков, кроме английского:</span><span class="sxs-lookup"><span data-stu-id="2f9c6-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="2f9c6-121">Китайский \(Упрощенный\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2f9c6-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f9c6-122">Китайский \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="2f9c6-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f9c6-123">Французский —&#231;ais</span><span class="sxs-lookup"><span data-stu-id="2f9c6-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f9c6-124">Немецкий - deutsch</span><span class="sxs-lookup"><span data-stu-id="2f9c6-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f9c6-125">Итальянский - italiano</span><span class="sxs-lookup"><span data-stu-id="2f9c6-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f9c6-126">Японский - &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="2f9c6-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f9c6-127">Корейский - &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="2f9c6-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f9c6-128">Португальский — portugu&#234;s</span><span class="sxs-lookup"><span data-stu-id="2f9c6-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="2f9c6-129">Русский  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="2f9c6-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="2f9c6-130">Испанский язык — espa&#241;ol</span><span class="sxs-lookup"><span data-stu-id="2f9c6-130">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="2f9c6-131">Перейдите к `edge://flags` флажку **Включить локализованные средства разработчика** и установите **его на включено.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="2f9c6-132">Кроме того, **установите флаг экспериментов для** средств разработки с **включенной**.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="2f9c6-133">Перезапустите Microsoft Edge и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="2f9c6-134">Язык DevTools совпадает с языком, который используется для Microsoft `edge://settings/languages` Edge.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools на немецком языке" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   <span data-ttu-id="2f9c6-136">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="2f9c6-136">The DevTools in German</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-137">Если вы хотите использовать DevTools на другом языке, чем [доступные,][PostTweetEdgeDevTools] отправьте нам сообщение в Twitter или выберите значок [Отправка отзывов.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2f9c6-137">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or choose the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="2f9c6-138">Проблема Chromium [#941561][CR941561]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-138">Chromium issue [#941561][CR941561]</span></span>  

### <a name="webhint-microsoft-edge-extension"></a><span data-ttu-id="2f9c6-139">webhint Microsoft Edge extension</span><span class="sxs-lookup"><span data-stu-id="2f9c6-139">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="2f9c6-140">Расширение Microsoft Edge позволяет легко сканировать веб-страницу и получать отзывы о доступности, совместимости браузера, безопасности, производительности и других данных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-140">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="2f9c6-141">Дополнительные публикации [https://webhint.io][Webhint] в .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-141">Read more at [https://webhint.io][Webhint].</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Средство Подсказки в DevTools при установке расширения веб-браузера" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   <span data-ttu-id="2f9c6-143">Средство **Подсказки** в DevTools при установке расширения веб-браузера</span><span class="sxs-lookup"><span data-stu-id="2f9c6-143">The **Hints** tool in the DevTools when the webhint browser extension is installed</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-144">[Попробуйте расширение веб-браузера в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="2f9c6-144">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="2f9c6-145">После установки расширения откройте DevTools и выберите **средство Hints.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-145">Once you install the extension, open the DevTools and choose the **Hints** tool.</span></span>  <span data-ttu-id="2f9c6-146">Отсюда запустите настраиваемую проверку сайта.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-146">From here, run a customizable site scan.</span></span>  <span data-ttu-id="2f9c6-147">[Переехав в webhint.io,][WebhintBrowserExtension] чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-147">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <a name="3d-view"></a><span data-ttu-id="2f9c6-148">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="2f9c6-148">3D View</span></span>  

<span data-ttu-id="2f9c6-149">Использование **3D-представления** для отлаживания веб-приложения путем навигации по объектной модели документа [\(DOM\)][MDNDocumentObjectModel] или контексту укладки [индекса z.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-149">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="3D-представление в DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   <span data-ttu-id="2f9c6-151">**3D-представление** в DevTools</span><span class="sxs-lookup"><span data-stu-id="2f9c6-151">The **3D View** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-152">Чтобы получить доступ к 3D-представлению, перейдите по флажку Эксперименты для разработчиков и убедитесь, что флаг экспериментов для разработчиков `edge://flags` задает **включено.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2f9c6-152">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="2f9c6-153">Перезапустите Microsoft Edge и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-153">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="2f9c6-154">Выберите `F1` в разделе DevTools или откройте раздел **Параметры**Эксперименты и включим контрольный ящик  >  \*\*\*\* Enable **3D View.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-154">Select `F1` in the DevTools or open the **Settings** > **Experiments** section, and turn on the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="2f9c6-155">Теперь выберите `Ctrl`  +  `Shift`  +  `P` , введите **в 3D-представлении** и **выберите Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-155">Now, select `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="2f9c6-156">Мы работаем над пользовательским интерфейсом и добавляем дополнительные функциональные возможности в 3D View, поэтому отправьте нам свои [отзывы.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2f9c6-156">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="2f9c6-157">Проблема Chromium [#987787][CR987787]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-157">Chromium issue [#987787][CR987787]</span></span>

### <a name="visual-studio-code-extensions"></a><span data-ttu-id="2f9c6-158">Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="2f9c6-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="2f9c6-159">Команда DevTools также выпустила некоторые расширения для кода [Visual Studio,][VisualStudioCode] которые могут использовать силу DevTools непосредственно из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-159">The DevTools team has also released some extensions for [Visual Studio Code][VisualStudioCode] that let you use the power of the DevTools directly from your text editor.</span></span> <span data-ttu-id="2f9c6-160">Ознакомьтесь со следующими расширениями.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-160">Check out the following extensions.</span></span>  

#### <a name="elements-for-microsoft-edge"></a><span data-ttu-id="2f9c6-161">Элементы для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f9c6-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="2f9c6-162">Используйте средство Elements из Visual Studio кода, добавив элементы для [Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio кода.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-162">Use the Elements tool from within Visual Studio Code by adding the [Elements for Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio Code extension.</span></span>  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Средство Elements в Visual Studio с помощью расширения Elements for Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   <span data-ttu-id="2f9c6-164">Средство **Elements** в Visual Studio с помощью расширения Elements for Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f9c6-164">The **Elements** tool in Visual Studio Code using the Elements for Microsoft Edge extension</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-165">Дополнительные сведения вы можете получить в [службе Elements for Microsoft Edge Visual Studio кода.][VisualStudioCodeElementEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-165">For more information, check out [Elements for Microsoft Edge Visual Studio Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <a name="debugger-for-microsoft-edge"></a><span data-ttu-id="2f9c6-166">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f9c6-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="2f9c6-167">С [расширением кода Debugger для Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio отладка JavaScript, запущенная в Microsoft Edge непосредственно из Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio Code extension, debug JavaScript running in Microsoft Edge directly from Visual Studio Code.</span></span>  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Отладка для расширения Microsoft Edge в Visual Studio коде" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   <span data-ttu-id="2f9c6-169">Отладка для расширения Microsoft Edge в Visual Studio коде</span><span class="sxs-lookup"><span data-stu-id="2f9c6-169">The Debugger for Microsoft Edge Extension in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-170">Дополнительные сведения о том, как отчудировать Microsoft Edge от [Visual Studio Code.][VisualStudioCodeDebuggerEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-170">For more information, check out [how to debug Microsoft Edge from Visual Studio Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <a name="webhint"></a><span data-ttu-id="2f9c6-171">webhint</span><span class="sxs-lookup"><span data-stu-id="2f9c6-171">webhint</span></span>  

<span data-ttu-id="2f9c6-172">Расширение [веб-Visual Studio][VisualStudioMarketplaceWebhintExtension] кода используется для улучшения веб-страницы во время `webhint` ее записи!</span><span class="sxs-lookup"><span data-stu-id="2f9c6-172">The [webhint][VisualStudioMarketplaceWebhintExtension] Visual Studio Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="2f9c6-173">Это расширение запускает и сообщает диагностику в файлах рабочего пространства на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Веб-Visual Studio кода, анализируя файл tsx в Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   <span data-ttu-id="2f9c6-175">Веб-Visual Studio кода, анализируя `.tsx` файл в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2f9c6-175">The webhint Visual Studio Code extension analyzing a `.tsx` file in Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-176">[Узнайте больше о расширении веб-Visual Studio code.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-176">[Learn more about the Visual Studio Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <a name="visual-studio-integration"></a><span data-ttu-id="2f9c6-177">Visual Studio интеграции</span><span class="sxs-lookup"><span data-stu-id="2f9c6-177">Visual Studio integration</span></span>  

<span data-ttu-id="2f9c6-178">В Visual Studio 2019 версии 16.2 или более поздней версии Visual Studio отладка JavaScript, запущенного в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-178">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="2f9c6-179">[Скачайте Visual Studio 2019,][MicrosoftVisualStudioDownloads] чтобы попробовать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-179">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out.</span></span>  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta" lightbox="../../images/2019/12/vs.msft.png":::
   <span data-ttu-id="2f9c6-181">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta</span><span class="sxs-lookup"><span data-stu-id="2f9c6-181">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-182">[Ознакомьтесь с нашим сообщением][MicrosoftVisualStudioBlogDebugJavascript]в блоге, чтобы узнать, как отламыть Microsoft Edge из Visual Studio .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-182">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <a name="tracking-prevention-console-messages"></a><span data-ttu-id="2f9c6-183">Отслеживание сообщений консоли предотвращения</span><span class="sxs-lookup"><span data-stu-id="2f9c6-183">Tracking prevention Console messages</span></span>  

<span data-ttu-id="2f9c6-184">Отслеживание предотвращения — это уникальная функция в Microsoft Edge, которая блокирует отслеживание веб-сайта перед его посещением.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-184">Tracking prevention is a unique feature in Microsoft Edge that blocks you from being tracked by a website before you visited it.</span></span>  <span data-ttu-id="2f9c6-185">Параметр предотвращения отслеживания по умолчанию — это режим Balanced, который блокирует сторонние трекеры и известные вредоносные трекеры для обеспечения баланса конфиденциальности и совместимости с веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-185">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="2f9c6-186">Чтобы получить больше информации о совместимости веб-страницы при блокировке определенных трекеров, группа \*\*\*\* Microsoft Edge добавила предупреждающие сообщения в консоли при блокировке трекера.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-186">To give you more insight into the compatibility of your web page when certain trackers are blocked, The Microsoft Edge team added warning messages in the **Console** when a tracker is blocked.</span></span>  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Сообщения в консоли при отслеживании предотвращения блокирования доступа к хранилищам для трекера" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   <span data-ttu-id="2f9c6-188">Сообщения в консоли при **отслеживании** предотвращения блокирования доступа к хранилищам для трекера</span><span class="sxs-lookup"><span data-stu-id="2f9c6-188">Messages in the **Console** when tracking prevention blocks access to storage for a tracker</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-189">[Дополнительные данные о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-189">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="2f9c6-190">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="2f9c6-190">Announcements from the Chromium project</span></span>  

<span data-ttu-id="2f9c6-191">В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 80, которые были внесены в проект Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-191">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a><span data-ttu-id="2f9c6-192">Поддержка переделокации допустимого и классового класса в консоли</span><span class="sxs-lookup"><span data-stu-id="2f9c6-192">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="2f9c6-193">Консоль **теперь** поддерживает переделки `let` и `class` утверждения.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-193">The **Console** now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="2f9c6-194">Неумелость к переописыванию была обычным раздражением для веб-разработчиков, которые используют консоль для экспериментов с новым кодом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-194">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="2f9c6-195">Переоценка или утверждение в скрипте за пределами консоли или в одной консоли ввода `let` `class` по-прежнему вызывает `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-195">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="2f9c6-196">Например, ранее при повторном объявлении локальной переменной с `let` консолью была допущена ошибка:</span><span class="sxs-lookup"><span data-stu-id="2f9c6-196">For example, previously, when re-declaring a local variable with `let`, the Console threw an error:</span></span>  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Консоль в Microsoft Edge 79, показывающая, что переделокация не удается" lightbox="../../images/2019/12/letbefore.msft.png":::
   <span data-ttu-id="2f9c6-198">Консоль **в** Microsoft Edge 79, показывающая, что повторное объявление не удается</span><span class="sxs-lookup"><span data-stu-id="2f9c6-198">The **Console** in Microsoft Edge 79 showing that the let re-declaration fails</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-199">Теперь консоль позволяет переоцирять:</span><span class="sxs-lookup"><span data-stu-id="2f9c6-199">Now, the Console allows the redeclaration:</span></span>  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Консоль в Microsoft Edge 80 с указанием успешности переделокации" lightbox="../../images/2019/12/letafter.msft.png":::
   <span data-ttu-id="2f9c6-201">Консоль **в** Microsoft Edge 80 с указанием успешности повторного декларирования</span><span class="sxs-lookup"><span data-stu-id="2f9c6-201">The **Console** in Microsoft Edge 80 showing that the let re-declaration succeeds</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-202">Проблема Chromium [#1004193][CR1004193]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-202">Chromium issue [#1004193][CR1004193]</span></span>  

### <a name="improved-webassembly-debugging"></a><span data-ttu-id="2f9c6-203">Улучшенная отладка webAssembly</span><span class="sxs-lookup"><span data-stu-id="2f9c6-203">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="2f9c6-204">DevTools начала поддерживать стандарт отладки [DWARF,][DwarfHome]что означает повышенную поддержку для перешагровки кода, установки точек разрыва и устранения следов стека на исходных языках в DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-204">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a><span data-ttu-id="2f9c6-205">Обновления сетевых панелей</span><span class="sxs-lookup"><span data-stu-id="2f9c6-205">Network panel updates</span></span>  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a><span data-ttu-id="2f9c6-206">Запрос Цепочек инициаторов в панели Инициатор</span><span class="sxs-lookup"><span data-stu-id="2f9c6-206">Request Initiator Chains in the Initiator panel</span></span>  

<span data-ttu-id="2f9c6-207">Теперь вы можете просматривать инициаторов и зависимостей сетевого запроса как вложенный список.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-207">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="2f9c6-208">Это может помочь вам понять, почему был запротесрен ресурс или какая деятельность сети вызвана определенным ресурсом \(например, скрипт\).</span><span class="sxs-lookup"><span data-stu-id="2f9c6-208">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Цепочка инициаторов запроса в панели Инициатор" lightbox="../../images/2019/12/initiators.msft.png":::
   <span data-ttu-id="2f9c6-210">Цепочка инициаторов запроса в **панели Инициатор**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-210">A Request Initiator Chain in the **Initiator** panel</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-211">После [ведения журнала сетевой активности][DevToolsNetworkIndex]в панели Network выберите \*\*\*\* ресурс, а затем перейдите на панель Инициатора, чтобы просмотреть цепочку инициатора **запроса:**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-211">After [logging network activity in the Network panel][DevToolsNetworkIndex], choose a resource and then navigate to the **Initiator** panel to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="2f9c6-212">**Проинспектировали ресурс** является смелым.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-212">The **inspected resource** is bold.</span></span>  <span data-ttu-id="2f9c6-213">На скриншоте выше `ai.2.min.js` — проверенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-213">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="2f9c6-214">Ресурсы, которые находятся выше проверенного ресурса, являются **инициаторами.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-214">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="2f9c6-215">На скриншоте `https://www.microsoftedgeinsider.com` выше, является инициатором `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-215">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="2f9c6-216">Другими словами, `https://www.microsoftedgeinsider.com` вызвал запрос сети для `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-216">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="2f9c6-217">Ресурсы ниже проверенного ресурса — **это зависимости.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-217">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="2f9c6-218">На скриншоте `https://dc.services.visualstudio.com/v2/track` выше— зависимость `ai.2.min.js` от .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-218">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="2f9c6-219">Другими словами, `ai.2.min.js` вызвал запрос сети для `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-219">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="2f9c6-220">Сведения о инициаторе и зависимостей также могут быть доступны путем удержания и нависания над `Shift` сетевыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-220">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="2f9c6-221">Перейдите к [просмотру инициаторов и зависимостей.][DevToolsNetworkReferenceViewInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-221">Navigate to [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="2f9c6-222">Проблема Chromium [#842488][CR842488]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-222">Chromium issue [#842488][CR842488]</span></span>  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a><span data-ttu-id="2f9c6-223">Выделение выбранного сетевого запроса в Обзоре</span><span class="sxs-lookup"><span data-stu-id="2f9c6-223">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="2f9c6-224">После выбора сетевого ресурса для его проверки панель Network теперь помещает синюю границу вокруг этого ресурса в **Обзоре.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-224">After you choose a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="2f9c6-225">Это поможет вам определить, происходит ли запрос сети раньше или позже, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-225">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Области Обзор выделения проверенного ресурса" lightbox="../../images/2019/12/overview.msft.png":::
   <span data-ttu-id="2f9c6-227">Области **Обзор** выделения проверенного ресурса</span><span class="sxs-lookup"><span data-stu-id="2f9c6-227">The **Overview** pane highlighting the inspected resource</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-228">Проблема Chromium [#988253][CR988253]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-228">Chromium issue [#988253][CR988253]</span></span>  

#### <a name="url-and-path-columns-in-the-network-panel"></a><span data-ttu-id="2f9c6-229">СТОЛБЦЫ URL-адресов и путей в панели Network</span><span class="sxs-lookup"><span data-stu-id="2f9c6-229">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="2f9c6-230">Используйте новые **столбцы Path** и **URL-адрес** в средстве **Network** для отображения абсолютного пути или полного URL-адреса каждого сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-230">Use the new **Path** and **URL** columns in the **Network** tool to display the absolute path or full URL of each network resource.</span></span>  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Новые столбцы Path и URL-адресов в панели Network" lightbox="../../images/2019/12/columns.msft.png":::
   <span data-ttu-id="2f9c6-232">Новые столбцы Path и URL-адрес в **средстве Network**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-232">The new Path and URL columns in the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-233">Чтобы отобразить новые столбцы, наведите курсор на загон таблицы **Водопад,** откройте контекстное меню \(righ-click\) и выберите **Путь** или **URL-адрес.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-233">To display the new columns, hover on the **Waterfall** table header, open the contextual menu \(righ-click\), and choose **Path** or **URL**.</span></span>  

<span data-ttu-id="2f9c6-234">Проблема Chromium [#993366][CR993366]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-234">Chromium issue [#993366][CR993366]</span></span>  

#### <a name="updated-user-agent-strings"></a><span data-ttu-id="2f9c6-235">Обновленные User-Agent строки</span><span class="sxs-lookup"><span data-stu-id="2f9c6-235">Updated User-Agent strings</span></span>  

<span data-ttu-id="2f9c6-236">DevTools поддерживает настройку настраиваемой строки User-Agent через панель **сетевых условий.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-236">DevTools supports setting a custom User-Agent string through the **Network Conditions** panel.</span></span>  <span data-ttu-id="2f9c6-237">Строка User-Agent влияет на `User-Agent` заглавную строку HTTP, присоединенную к сетевым ресурсам, а также значение `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="2f9c6-237">The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="2f9c6-238">Предопределяющие User-Agent строки были обновлены, чтобы отражать современные версии браузера.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-238">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Меню Агента пользователя в панели сетевых условий" lightbox="../../images/2019/12/useragent.msft.png":::
   <span data-ttu-id="2f9c6-240">Меню Агента пользователя в панели **сетевых условий**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-240">The User Agent menu in the **Network Conditions** panel</span></span>  
:::image-end:::  

<span data-ttu-id="2f9c6-241">Чтобы получить **доступ к сетевым** [условиям, откройте командное меню][DevToolsCommandMenuIndex] и запустите `Show Network Conditions` команду.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-241">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="2f9c6-242">Вы также можете [User-Agent строки в режиме устройства.][DevToolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-242">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="2f9c6-243">Проблема Chromium [#1029031][CR1029031]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-243">Chromium issue [#1029031][CR1029031]</span></span>  

### <a name="audits-panel-updates"></a><span data-ttu-id="2f9c6-244">Аудит обновлений панелей</span><span class="sxs-lookup"><span data-stu-id="2f9c6-244">Audits panel updates</span></span>  

#### <a name="new-configuration-ui"></a><span data-ttu-id="2f9c6-245">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="2f9c6-245">New configuration UI</span></span>  

<span data-ttu-id="2f9c6-246">Пользовательский интерфейс конфигурации имеет новый, отзывчивый дизайн, а параметры настройки регулирования были упрощены.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-246">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="2f9c6-247">Дополнительные сведения об изменениях пользовательского интерфейса регулирования см. в окне Регулирование панели [аудитов.][GitHubGoogleChromeDevToolsAuditsPanelThrottling]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-247">For more information on the throttling UI changes, navigate to [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling].</span></span>  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Новый пользовательский интерфейс конфигурации" lightbox="../../images/2019/12/start.msft.png":::
   <span data-ttu-id="2f9c6-249">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="2f9c6-249">The new configuration UI</span></span>  
:::image-end:::  

### <a name="coverage-tool-updates"></a><span data-ttu-id="2f9c6-250">Обновления средства покрытия</span><span class="sxs-lookup"><span data-stu-id="2f9c6-250">Coverage tool updates</span></span>  

#### <a name="per-function-or-per-block-coverage-modes"></a><span data-ttu-id="2f9c6-251">Режимы покрытия на одну функцию или на блок</span><span class="sxs-lookup"><span data-stu-id="2f9c6-251">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="2f9c6-252">Средство [Coverage][DevToolsCoverageIndex] имеет новое меню выпадения, которое позволяет указать, следует ли собирать данные о покрытии кода на одну функцию **или** **на блок.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-252">The [Coverage][DevToolsCoverageIndex] tool has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="2f9c6-253">**Покрытие каждого блока** является более подробным, но и гораздо более дорогостоящим в сборе.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-253">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="2f9c6-254">DevTools использует **по умолчанию покрытие** функций по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-254">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2f9c6-255">Вы можете заметить большие различия в охвате кода в HTML-файлах в зависимости от того, используете ли вы одну функцию **или** **режим блокировки.**</span><span class="sxs-lookup"><span data-stu-id="2f9c6-255">You may notice large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="2f9c6-256">При использовании **режима функции** встроенные скрипты в HTML-файлах рассматриваются как функции.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-256">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="2f9c6-257">Если сценарий работает вообще, то DevTools отмечает весь скрипт как используемый код.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-257">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="2f9c6-258">Только если сценарий вообще не работает, DevTools пометит сценарий как неиспользимый код.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-258">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Меню отсев в режиме покрытия" lightbox="../../images/2019/12/modes.msft.png":::
   <span data-ttu-id="2f9c6-260">Меню отсев в режиме покрытия</span><span class="sxs-lookup"><span data-stu-id="2f9c6-260">The coverage mode dropdown menu</span></span>  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a><span data-ttu-id="2f9c6-261">Теперь охват должен быть инициирован обновлением страницы</span><span class="sxs-lookup"><span data-stu-id="2f9c6-261">Coverage must now be initiated by a page refresh</span></span>  

<span data-ttu-id="2f9c6-262">Переналадка покрытия кода без обновления страницы была удалена из-за недостоверности данных об охвате.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-262">Toggling code coverage without a page refresh has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="2f9c6-263">Например, функция может быть неиспользована, если время запуска было давно, и сборщик мусора V8 убрал ее.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-263">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="2f9c6-264">Проблема Chromium [#1004203][CR1004203]</span><span class="sxs-lookup"><span data-stu-id="2f9c6-264">Chromium issue [#1004203][CR1004203]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="2f9c6-265">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="2f9c6-265">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="2f9c6-266">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-266">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="2f9c6-267">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="2f9c6-267">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="2f9c6-268">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f9c6-268">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS с помощью средства Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Просмотр инициаторов и зависимостей — справочник по сетевому анализу | Документы Майкрософт"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Новые возможности в edgeHTML | Документы Майкрософт"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладка для расширения Visual Studio Microsoft Edge | Документы Майкрософт"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы для расширения Visual Studio Microsoft Edge | Документы Майкрософт"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Добавьте поле Инициатор в вкладку Headers | Chromium Bugs"  
[CR988253]: https://crbug.com/988253 "Ошибка DevTools — отсутствие связи между сетевым запросом и графиком | Chromium Bugs"  
[CR993366]: https://crbug.com/993366 "Пожалуйста, покажите часть пути URL-адреса в списке запросов сетевых панелей | Chromium Bugs"  
[CR1004193]: https://crbug.com/1004193 "Режим REPL для V8 | Chromium Bugs"  
[CR1004203]: https://crbug.com/1004203 "Сделайте покрытие кода потрясающим | Chromium Bugs"  
[CR1029031]: https://crbug.com/1029031 "Строки UA устарели | Chromium Bugs" 
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Chromium Bugs"
[CR941561]: https://crbug.com/941561 "Локализуемость | Chromium Bugs"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о доступности"  

[DwarfHome]: https://dwarfstd.org "Карлик Главная"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Регулирование аудита DevTools — GoogleChrome/lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки инсайдеров Microsoft Edge"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отламыв JavaScript в Microsoft Edge из Visual Studio | Visual Studio блог"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документа (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузера веб-| документация по веб-сайтам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio расширение кода | документация по веб-сайтам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение предотвращения отслеживания в блоге Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"

> [!NOTE]
> <span data-ttu-id="2f9c6-308">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f9c6-308">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2f9c6-309">Оригинальная страница [](https://developers.google.com/web/updates/2019/12/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="2f9c6-309">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2f9c6-311">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2f9c6-311">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
