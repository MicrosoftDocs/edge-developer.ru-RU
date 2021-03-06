---
description: Сопоположите клавиши Visual Studio код, эмулировать Surface Duo и Samsung Galaxy Fold, улучшения наложения сетки CSS и другие.
title: Новые возможности в DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3853f097877fc45b14ceb0674309cb35b58a0aa6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398618"
---
# <a name="whats-new-in-devtools-microsoft-edge-86"></a><span data-ttu-id="c70b0-104">Что нового в DevTools (Microsoft Edge 86)</span><span class="sxs-lookup"><span data-stu-id="c70b0-104">What's New In DevTools (Microsoft Edge 86)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c70b0-105">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c70b0-105">Announcements from the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a><span data-ttu-id="c70b0-106">Совпадение клавиш в DevTools с Visual Studio кодом</span><span class="sxs-lookup"><span data-stu-id="c70b0-106">Match keyboard shortcuts in DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="c70b0-107">В Microsoft Edge 86 клавиши в DevTools могут совпадать с ярлыками в [Microsoft Visual Studio Code.][VisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="c70b0-107">In Microsoft Edge 86, you may match keyboard shortcuts in the DevTools to your shortcuts in [Microsoft Visual Studio Code][VisualStudioCode].</span></span>  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Совпадение клавиш в DevTools для Visual Studio кода" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   <span data-ttu-id="c70b0-109">Совпадение клавиш в DevTools для Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="c70b0-109">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-110">Чтобы активировать эту функцию, перейдите к настройке ярлыков клавиатуры [в Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="c70b0-110">To activate this feature, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  

<span data-ttu-id="c70b0-111">Например, ярлык клавиатуры для прио паузы или продолжения работы скрипта в [Visual Studio коде][VisualStudioCodeShortcutsKeyboardWindows] `F5` .</span><span class="sxs-lookup"><span data-stu-id="c70b0-111">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] is `F5`.</span></span>  <span data-ttu-id="c70b0-112">С предустановленной программой **DevTools (По умолчанию)** этот же ярлык в DevTools есть, но при выборе предустановки кода Visual Studio этот ярлык теперь также `F8` является \*\*\*\* `F5` .</span><span class="sxs-lookup"><span data-stu-id="c70b0-112">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8`, but when you choose the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="c70b0-113">Проблема Chromium [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="c70b0-113">Chromium issue [#174309][CR174309]</span></span>  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a><span data-ttu-id="c70b0-114">Эмулировать Surface Duo и Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="c70b0-114">Emulate Surface Duo and Samsung Galaxy Fold</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="c70b0-116">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="c70b0-116">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-117">Теперь вы можете проверить внешний вид веб-сайта или приложения на двух новых устройствах:  [Surface Duo][MicrosoftSurfaceDevicesDuo] и [Samsung Galaxy Fold][SamsungMobileGalaxyFold] в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c70b0-117">You are now able to test the look and feel of your website or app on two new devices:  [Surface Duo][MicrosoftSurfaceDevicesDuo] and [Samsung Galaxy Fold][SamsungMobileGalaxyFold] in Microsoft Edge.</span></span>  

<span data-ttu-id="c70b0-118">Чтобы улучшить веб-сайт или приложение для двухэкранных и складных устройств, используйте следующие функции при [эмулации устройства.][DevtoolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="c70b0-118">To help enhance your website or app for the dual-screen and foldable devices, use the following features when [emulating the device][DevtoolsDeviceModeIndex].</span></span>  

*   <span data-ttu-id="c70b0-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]— это когда веб-сайт \(или app\) отображается на обоих экранах.</span><span class="sxs-lookup"><span data-stu-id="c70b0-119">[Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], which is when your website \(or app\) appears across both screens.</span></span>
*   <span data-ttu-id="c70b0-120">[Отрисовка шва,][DualScreenIntroductionHowWorkSeam]который является пространством между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="c70b0-120">[Rendering the seam][DualScreenIntroductionHowWorkSeam], which is the space between the two screens.</span></span>
*   <span data-ttu-id="c70b0-121">[Включение экспериментальных API][DevtoolsExperimentalFeaturesEnableExperimentalApis] веб-платформы для доступа к новой функции экранирования экрана [CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].</span><span class="sxs-lookup"><span data-stu-id="c70b0-121">[Enabling experimental Web Platform APIs][DevtoolsExperimentalFeaturesEnableExperimentalApis] to access the new [CSS media screen-spanning feature][DualScreenWebCssMediaSpanning] and [JavaScript getWindowSegments API][DualScreenWebJavascriptGetwindowsegments].</span></span>  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Эмуляция устройств для Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   <span data-ttu-id="c70b0-123">Эмуляция устройств для Surface Duo</span><span class="sxs-lookup"><span data-stu-id="c70b0-123">Device emulation for Surface Duo</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-124">Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, перейдите к экспериментальным функциям и выберите контрольный ящик рядом с **режимом Emulation: Support dual screen mode.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-124">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Emulation: Support dual screen mode**.</span></span>  

<span data-ttu-id="c70b0-125">Дополнительные сведения об этом эксперименте см. в ["Эмуляция: поддержка режима двойного экрана".][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]</span><span class="sxs-lookup"><span data-stu-id="c70b0-125">For more information about this experiment, navigate to [Emulation: Support dual screen mode][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].</span></span>  

<span data-ttu-id="c70b0-126">Проблема Chromium: [#1054281][CR1054281]</span><span class="sxs-lookup"><span data-stu-id="c70b0-126">Chromium issue: [#1054281][CR1054281]</span></span>  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a><span data-ttu-id="c70b0-127">Улучшения наложения сетки CSS и новые функции экспериментальной сетки</span><span class="sxs-lookup"><span data-stu-id="c70b0-127">CSS grid overlay improvements and new experimental grid features</span></span>  

<span data-ttu-id="c70b0-128">Благодарим вас за положительные отзывы об улучшенных наложениях сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="c70b0-128">Thank you for the positive feedback about the improved CSS grid overlays.</span></span>  <span data-ttu-id="c70b0-129">Наложения сетки CSS теперь включены по умолчанию и не требуют включения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="c70b0-129">The CSS grid overlays are now enabled by default and do not require you to turn on an experiment.</span></span>  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Наложение сетки CSS для элемента статьи" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   <span data-ttu-id="c70b0-131">Наложение сетки CSS для `article` элемента</span><span class="sxs-lookup"><span data-stu-id="c70b0-131">CSS grid overlay for `article` element</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c70b0-132">Дополнительные сведения о наложениях сетки перейдите к [функциям отладки сетки CSS.][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]</span><span class="sxs-lookup"><span data-stu-id="c70b0-132">For more information about grid overlays, navigate to [CSS grid debugging features][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="c70b0-133">Команда Microsoft Edge DevTools и команда Chrome DevTools совместно работают над дополнительными функциями.</span><span class="sxs-lookup"><span data-stu-id="c70b0-133">The Microsoft Edge DevTools team and the Chrome DevTools team collaborate on additional features.</span></span>  <span data-ttu-id="c70b0-134">Новые функции включают несколько накладок, которые являются настойчивыми и настраиваемыми из новой области **Макет** на **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-134">The new features include multiple overlays that are persistent and configurable from a new **Layout** pane on the **Elements** tool.</span></span>  

<span data-ttu-id="c70b0-135">Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, включите экспериментальные функции и выберите контрольный ящик рядом с включить новые функции отладки **CSS Grid (параметры**конфигурации, доступные в панели макета в Elements после перезагрузки).</span><span class="sxs-lookup"><span data-stu-id="c70b0-135">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable new CSS Grid debugging features (configuration options available in Layout sidebar pane in Elements after restart)**.</span></span>  

<span data-ttu-id="c70b0-136">Дополнительные сведения об этом эксперименте можно найти в поле Включить новые функции отладки сетки [CSS.][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]</span><span class="sxs-lookup"><span data-stu-id="c70b0-136">For more information about this experiment, navigate to [Enable new CSS grid debugging features][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].</span></span>  

<span data-ttu-id="c70b0-137">Проблема Chromium: [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="c70b0-137">Chromium issue: [#1047356][CR1047356]</span></span>  

### <a name="table-copied-from-the-console-preserves-formatting"></a><span data-ttu-id="c70b0-138">Таблица, скопированная из консоли, сохраняет форматирование</span><span class="sxs-lookup"><span data-stu-id="c70b0-138">Table copied from the Console preserves formatting</span></span>  

<span data-ttu-id="c70b0-139">В Microsoft Edge 85 или более ранний формат копирования `console.table` был потерян.</span><span class="sxs-lookup"><span data-stu-id="c70b0-139">In Microsoft Edge 85 or earlier, the formatting of a copied `console.table` was lost.</span></span>  <span data-ttu-id="c70b0-140">Если вы скопировали [][DevtoolsConsoleApiTable] выход из API консоли таблицы и вклеили его, сохранился только текст таблицы.</span><span class="sxs-lookup"><span data-stu-id="c70b0-140">If you copied the output from the [table][DevtoolsConsoleApiTable] Console API, and pasted it, only the text of the table was kept.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Выход API консоли таблицы в Microsoft Edge 85 или более ранний" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` <span data-ttu-id="c70b0-142">Выход API консоли в Microsoft Edge 85 или более ранний</span><span class="sxs-lookup"><span data-stu-id="c70b0-142">Console API output in Microsoft Edge 85 or earlier</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Выход API консоли таблицы из Microsoft Edge 85 или более ранней вставки в Visual Studio Код" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="c70b0-144">Выход API консоли из Microsoft Edge 85 или более ранней вставки в Visual Studio Код</span><span class="sxs-lookup"><span data-stu-id="c70b0-144">Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c70b0-145">В Microsoft Edge 86 или позже при \*\*\*\* копировании таблицы из консоли форматирование теперь сохраняется.</span><span class="sxs-lookup"><span data-stu-id="c70b0-145">In Microsoft Edge 86 or later, when you copy a table from the **Console**, the formatting is now preserved.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Выход API консоли таблицы в Microsoft Edge 86 или более поздней" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` <span data-ttu-id="c70b0-147">Выход API консоли в Microsoft Edge 86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="c70b0-147">Console API output in Microsoft Edge 86 or later</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Выход API консоли таблицы из Microsoft Edge 86 или более поздней вставки в Visual Studio Код" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` <span data-ttu-id="c70b0-149">Выход API консоли из Microsoft Edge 86 или более поздней Visual Studio код</span><span class="sxs-lookup"><span data-stu-id="c70b0-149">Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c70b0-150">Проблема Chromium: [#1115011][CR1115011]</span><span class="sxs-lookup"><span data-stu-id="c70b0-150">Chromium issue: [#1115011][CR1115011]</span></span>  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a><span data-ttu-id="c70b0-151">Source Order Viewer for easier accessibility testing</span><span class="sxs-lookup"><span data-stu-id="c70b0-151">Source Order Viewer for easier accessibility testing</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="c70b0-153">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="c70b0-153">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-154">Новый помощник по доступности отображает порядок элементов в источнике.</span><span class="sxs-lookup"><span data-stu-id="c70b0-154">The new accessibility helper displays the order of elements in the source.</span></span>  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Активация порядка источника Show" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   <span data-ttu-id="c70b0-156">Активация **порядка источника Show**</span><span class="sxs-lookup"><span data-stu-id="c70b0-156">Activate **Show source order**</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-157">Эта функция упрощает проверку работы чтения с экрана и пользователей клавиатуры на веб-сайте или приложении.</span><span class="sxs-lookup"><span data-stu-id="c70b0-157">This feature makes it easier to test the way screen reader and keyboard users experience your website or app.</span></span>  <span data-ttu-id="c70b0-158">Считыватели экрана и навигация по клавиатуре зависят от контента, размещаемого в определенном порядке в исходный код веб-сайта или приложения, чтобы он совпадал с отрисовывать страницу.</span><span class="sxs-lookup"><span data-stu-id="c70b0-158">Screen readers and keyboard navigation depend on content being placed in a particular order in the source code of your website or app, so that it matches the rendered page.</span></span>  <span data-ttu-id="c70b0-159">Потенциальные различия в порядке между отрисовываемой страницей и исходным кодом отображаются в представлении источника.</span><span class="sxs-lookup"><span data-stu-id="c70b0-159">The Source Order Viewer displays potential differences in order between the rendered page and the source code.</span></span>  

<span data-ttu-id="c70b0-160">Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, перейдите к включив экспериментальные функции и выберите почтовый ящик рядом с **функцией Включить просмотр источника порядка**.</span><span class="sxs-lookup"><span data-stu-id="c70b0-160">To turn on this experimental feature, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Source Order Viewer**.</span></span>  

<span data-ttu-id="c70b0-161">Дополнительные сведения об этом эксперименте перейдите к [включить viewer source order][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span><span class="sxs-lookup"><span data-stu-id="c70b0-161">For more information about this experiment, navigate to [Enable Source Order Viewer][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].</span></span>  

<span data-ttu-id="c70b0-162">Проблема Chromium: [#1094406][CR1094406]</span><span class="sxs-lookup"><span data-stu-id="c70b0-162">Chromium issue: [#1094406][CR1094406]</span></span>  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a><span data-ttu-id="c70b0-163">Выделение всех результатов поиска в инструменте Elements</span><span class="sxs-lookup"><span data-stu-id="c70b0-163">Highlight all search results in Elements tool</span></span>  

<span data-ttu-id="c70b0-164">В Microsoft Edge 84 и 85 первый результат поиска в **инструменте Elements** не был выделен.</span><span class="sxs-lookup"><span data-stu-id="c70b0-164">In Microsoft Edge 84 and 85, the first search result in the **Elements** tool did not highlight.</span></span>  <span data-ttu-id="c70b0-165">Остальные результаты поиска были выделены правильно.</span><span class="sxs-lookup"><span data-stu-id="c70b0-165">The remaining search results were highlighted correctly.</span></span>  

<span data-ttu-id="c70b0-166">Благодарим вас за отправку отзывов и помощь в улучшении Chromium.</span><span class="sxs-lookup"><span data-stu-id="c70b0-166">Thank you for sending your feedback and helping improve Chromium.</span></span>  <span data-ttu-id="c70b0-167">Ваши отзывы обнаружили [#1103316][CR1103316] в проекте Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="c70b0-167">Your feedback uncovered Issue [#1103316][CR1103316] in the open-source Chromium project.</span></span>  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Выделен первый результат поиска на панели Elements в Microsoft Edge 84 или более поздней" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   <span data-ttu-id="c70b0-169">Выделение первого результата поиска в **средстве Elements** в Microsoft Edge 84 или более поздней</span><span class="sxs-lookup"><span data-stu-id="c70b0-169">Highlighted first search result on **Elements** tool in Microsoft Edge 84 or later</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-170">Проблема устранена во всех версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c70b0-170">The issue is now fixed in all versions of Microsoft Edge.</span></span>  

<span data-ttu-id="c70b0-171">Проблема Chromium: [#1103316][CR1103316]</span><span class="sxs-lookup"><span data-stu-id="c70b0-171">Chromium issue: [#1103316][CR1103316]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="c70b0-172">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="c70b0-172">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a><span data-ttu-id="c70b0-173">Новый инструмент Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c70b0-173">New Media tool</span></span>  

<span data-ttu-id="c70b0-174">DevTools теперь отображает сведения о медиаплеерах в [средстве Мультимедиа.][DevtoolsMediaPanelIndex]</span><span class="sxs-lookup"><span data-stu-id="c70b0-174">DevTools now displays media players information in the [Media][DevtoolsMediaPanelIndex] tool.</span></span>  

<span data-ttu-id="c70b0-175">Чтобы открыть новый **инструмент Media,** выполните следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="c70b0-175">To open the new **Media** tool, complete the following step.</span></span>  

1.  <span data-ttu-id="c70b0-176">Выберите **Настройка и управление DevTools** \( `...` \) > **средства**  >  **мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="c70b0-176">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Новый инструмент Мультимедиа" lightbox="../../media/2020/08/media-panel.msft.png":::
       <span data-ttu-id="c70b0-178">Новый **инструмент Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="c70b0-178">New **Media** tool</span></span>  
    :::image-end:::  

<span data-ttu-id="c70b0-179">До создания нового **средства мультимедиа** в DevTools сведения о видеоигрегах и отладке журнала и отладки находились в параметре **Последние игроки.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-179">Before the new **Media** tool in DevTools, the logging and debug information about video players was located under the **Recent Players** setting.</span></span>  <span data-ttu-id="c70b0-180">Чтобы открыть **параметр "Последние игроки",** перейдите к `edge://media-internals` инструменту **Players** и выберите его.</span><span class="sxs-lookup"><span data-stu-id="c70b0-180">To open the **Recent Players** setting, navigate to `edge://media-internals` and choose the **Players** tool.</span></span>  

<span data-ttu-id="c70b0-181">Просмотр контента в прямом эфире и более быстрая проверка потенциальных проблем, включая следующие примеры.</span><span class="sxs-lookup"><span data-stu-id="c70b0-181">View live content and inspect potential issues more quickly, including the following examples.</span></span>  

*   <span data-ttu-id="c70b0-182">Почему кадры отброшены?</span><span class="sxs-lookup"><span data-stu-id="c70b0-182">Why frames are dropped?</span></span>  
*   <span data-ttu-id="c70b0-183">Почему JavaScript взаимодействует с игроком неожиданным образом?</span><span class="sxs-lookup"><span data-stu-id="c70b0-183">Why JavaScript is interacting with the player in an unexpected way?</span></span>  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a><span data-ttu-id="c70b0-184">Захват снимков экрана узла с помощью контекстного меню инструмента Elements</span><span class="sxs-lookup"><span data-stu-id="c70b0-184">Capture node screenshots using the Elements tool context menu</span></span>  

<span data-ttu-id="c70b0-185">Теперь можно запечатлеть скриншоты узлов с помощью контекстного меню в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-185">You may now capture node screenshots using the context menu in the **Elements** tool.</span></span>  

<span data-ttu-id="c70b0-186">Например, чтобы сделать снимок экрана таблицы содержимого, наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите снимок экрана узла **Capture**.</span><span class="sxs-lookup"><span data-stu-id="c70b0-186">For example, to take a screenshot of the table of contents, hover on the element, open the contextual menu \(right-click\), and select **Capture node screenshot**.</span></span>  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Захват скриншотов узлов" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   <span data-ttu-id="c70b0-188">Захват скриншотов узлов</span><span class="sxs-lookup"><span data-stu-id="c70b0-188">Capture node screenshots</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-189">Проблема Chromium: [#1100253][CR1100253]</span><span class="sxs-lookup"><span data-stu-id="c70b0-189">Chromium issue: [#1100253][CR1100253]</span></span>  

### <a name="issues-tool-updates"></a><span data-ttu-id="c70b0-190">Выпуск обновлений инструмента</span><span class="sxs-lookup"><span data-stu-id="c70b0-190">Issues tool updates</span></span>  

<span data-ttu-id="c70b0-191">Панель предупреждений о проблемах в **консоли теперь** заменяется обычным сообщением.</span><span class="sxs-lookup"><span data-stu-id="c70b0-191">The Issues warning bar on the **Console** tool is now replaced with a regular message.</span></span>  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Проблемы в сообщении консоли" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   <span data-ttu-id="c70b0-193">Проблемы в сообщении консоли</span><span class="sxs-lookup"><span data-stu-id="c70b0-193">Issues in console message</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-194">Сторонние проблемы с cookie теперь скрыты по умолчанию в средстве **Issues.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-194">Third-party cookie issues are now hidden by default in the **Issues** tool.</span></span>  <span data-ttu-id="c70b0-195">Включите новый **почтовый** ящик Включить сторонние вопросы cookie для просмотра проблем.</span><span class="sxs-lookup"><span data-stu-id="c70b0-195">Enable the new **Include third-party cookie issues** checkbox to view the issues.</span></span>  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="почтовый ящик сторонних файлов cookie" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   <span data-ttu-id="c70b0-197">почтовый ящик сторонних файлов cookie</span><span class="sxs-lookup"><span data-stu-id="c70b0-197">third-party cookie issues checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-198">Проблемы с хромом: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span><span class="sxs-lookup"><span data-stu-id="c70b0-198">Chromium issues: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]</span></span>  

### <a name="emulate-missing-local-fonts"></a><span data-ttu-id="c70b0-199">Эмулировать отсутствующие локальные шрифты</span><span class="sxs-lookup"><span data-stu-id="c70b0-199">Emulate missing local fonts</span></span>  

<span data-ttu-id="c70b0-200">Откройте средство [визуализации и][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] используйте новую функцию **отключения** локальных шрифтов для эмуляции `local()` отсутствующих источников в `@font-face` правилах.</span><span class="sxs-lookup"><span data-stu-id="c70b0-200">Open the [Rendering tool][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] and use the new **Disable local fonts** feature to emulate missing `local()` sources in `@font-face` rules.</span></span>  

<span data-ttu-id="c70b0-201">Например, когда шрифт установлен на вашем устройстве и правило использует его в качестве шрифта, Microsoft Edge использует локальный файл шрифта `Rubik` `@font-face src` с `local()` устройства.</span><span class="sxs-lookup"><span data-stu-id="c70b0-201">For example, when the `Rubik` font is installed on your device and the `@font-face src` rule uses it as a `local()` font, Microsoft Edge uses the local font file from your device.</span></span>  

<span data-ttu-id="c70b0-202">Когда **отключение локальных шрифтов** включено, DevTools игнорирует шрифты и извлекает каждый `local()` из сети.</span><span class="sxs-lookup"><span data-stu-id="c70b0-202">When **Disable local fonts** is enabled, DevTools ignores the `local()` fonts and fetches each from the network.</span></span>  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Эмулировать отсутствующие локальные шрифты" lightbox="../../media/2020/08/disable-font.msft.png":::
   <span data-ttu-id="c70b0-204">Эмулировать отсутствующие локальные шрифты</span><span class="sxs-lookup"><span data-stu-id="c70b0-204">Emulate missing local fonts</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-205">При использовании двух разных копий одного шрифта во время разработки, например в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="c70b0-205">If you use two different copies of the same font during development, such as the following examples.</span></span>  

*   <span data-ttu-id="c70b0-206">Локальный шрифт для средств разработки.</span><span class="sxs-lookup"><span data-stu-id="c70b0-206">A local font for your design tools.</span></span>  
*   <span data-ttu-id="c70b0-207">Веб-шрифт для кода.</span><span class="sxs-lookup"><span data-stu-id="c70b0-207">A web font for your code.</span></span>  

<span data-ttu-id="c70b0-208">Чтобы \*\*\*\* упростить выполнение следующих задач, используйте отключение локальных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c70b0-208">Use **Disable local fonts** to make it easier for you to complete the following tasks.</span></span>  

*   <span data-ttu-id="c70b0-209">Отлажение и измерение производительности загрузки и оптимизации веб-шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c70b0-209">Debug and measure loading performance and optimization of web fonts.</span></span>  
*   <span data-ttu-id="c70b0-210">Проверка точности правил `@font-face` CSS.</span><span class="sxs-lookup"><span data-stu-id="c70b0-210">Verify accuracy of your CSS `@font-face` rules.</span></span>  
*   <span data-ttu-id="c70b0-211">Узнайте о различиях между локальными версиями, установленными на устройстве, и веб-шрифтом.</span><span class="sxs-lookup"><span data-stu-id="c70b0-211">Discover differences between local versions installed on your device and a web font.</span></span>  

<span data-ttu-id="c70b0-212">Проблема Chromium: [#384968][CR384968]</span><span class="sxs-lookup"><span data-stu-id="c70b0-212">Chromium issue: [#384968][CR384968]</span></span>  

### <a name="emulate-inactive-users"></a><span data-ttu-id="c70b0-213">Эмулировать неактивных пользователей</span><span class="sxs-lookup"><span data-stu-id="c70b0-213">Emulate inactive users</span></span>  

<span data-ttu-id="c70b0-214">API [обнаружения idle][WebDevIdleDetection] позволяет разработчикам обнаруживать неактивных пользователей и реагировать на изменения состояния ожидания.</span><span class="sxs-lookup"><span data-stu-id="c70b0-214">The [Idle Detection API][WebDevIdleDetection] allows developers to detect inactive users and react on idle state changes.</span></span>  <span data-ttu-id="c70b0-215">Теперь вы можете использовать DevTools для подражания неработающим изменениям состояния в средстве **Датчики** как для состояния пользователя, так и для состояния экрана, а не для ожидания изменения фактического состояния простоя.</span><span class="sxs-lookup"><span data-stu-id="c70b0-215">You are now able to use DevTools to emulate idle state changes in the **Sensors** tool for both the user state and the screen state instead of waiting for the actual idle state to change.</span></span>  <span data-ttu-id="c70b0-216">Вы можете открыть средство **Датчики** из [ящика][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="c70b0-216">You may open the **Sensors** tool from the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Эмулировать неактивных пользователей" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   <span data-ttu-id="c70b0-218">Эмулировать неактивных пользователей</span><span class="sxs-lookup"><span data-stu-id="c70b0-218">Emulate inactive users</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-219">Проблема Chromium: [#1090802][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="c70b0-219">Chromium issue: [#1090802][CR1090802]</span></span>  

### <a name="emulate-prefers-reduced-data"></a><span data-ttu-id="c70b0-220">Emulate prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="c70b0-220">Emulate prefers-reduced-data</span></span>  

> [!NOTE]
> <span data-ttu-id="c70b0-221">В Microsoft Edge 86, чтобы включить эту функцию, перейдите и включив флаг функций `edge://flags#enable-experimental-web-platform-features` **экспериментальной веб-платформы.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-221">In Microsoft Edge 86, to enable this feature, navigate to `edge://flags#enable-experimental-web-platform-features` and turn on the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="c70b0-222">Параметр эмуляции отображается только в том случае, если включен флаг.</span><span class="sxs-lookup"><span data-stu-id="c70b0-222">The emulation option is only displayed if the flag is enabled.</span></span>  

<span data-ttu-id="c70b0-223">Запрос [мультимедиа с пониженным][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] объемом данных определяет предпочтения пользователя в контенте для уменьшенных данных.</span><span class="sxs-lookup"><span data-stu-id="c70b0-223">The [prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] media query detects user content preferences for reduced data.</span></span>  <span data-ttu-id="c70b0-224">Если выбрано, пользователь получает альтернативное содержимое страницы, которое использует меньше данных.</span><span class="sxs-lookup"><span data-stu-id="c70b0-224">If selected, the user receives alternate page content that uses less data.</span></span>  

<span data-ttu-id="c70b0-225">Теперь можно использовать DevTools для эмулации `prefers-reduced-data` запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c70b0-225">You may now use DevTools to emulate the `prefers-reduced-data` media query.</span></span>  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emulate prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   <span data-ttu-id="c70b0-227">Emulate prefers-reduced-data</span><span class="sxs-lookup"><span data-stu-id="c70b0-227">Emulate prefers-reduced-data</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-228">Проблема Chromium: [#1096068][CR1096068]</span><span class="sxs-lookup"><span data-stu-id="c70b0-228">Chromium issue: [#1096068][CR1096068]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="c70b0-229">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="c70b0-229">Support for new JavaScript features</span></span>  

<span data-ttu-id="c70b0-230">Теперь DevTools лучше поддерживает следующие языковые функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c70b0-230">DevTools now have better supported the following JavaScript language features.</span></span>  

| <span data-ttu-id="c70b0-231">Языковая функция JavaScript</span><span class="sxs-lookup"><span data-stu-id="c70b0-231">JavaScript language feature</span></span> | <span data-ttu-id="c70b0-232">Сведения</span><span class="sxs-lookup"><span data-stu-id="c70b0-232">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="c70b0-233">Операторы логических назначений</span><span class="sxs-lookup"><span data-stu-id="c70b0-233">Logical assignment operators</span></span>][V8FeaturesLogicalAssignment] | <span data-ttu-id="c70b0-234">DevTools теперь поддерживает логическое назначение с помощью новых и операторов в `&&=` `||=` `??=` **средствах консоли** и **источников.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-234">DevTools now supports logical assignment with the new `&&=`, `||=`, and `??=` operators in the **Console** and **Sources** tools.</span></span>  |  
| <span data-ttu-id="c70b0-235">[Числимые сепараторы][V8FeaturesNumericSeparators] с довольной печатью</span><span class="sxs-lookup"><span data-stu-id="c70b0-235">Pretty-print [numeric separators][V8FeaturesNumericSeparators]</span></span> | <span data-ttu-id="c70b0-236">DevTools теперь правильно печатает числимые сепараторы в **средстве Sources.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-236">DevTools now properly pretty-prints the numeric separators in the **Sources** tool.</span></span>  |  

<span data-ttu-id="c70b0-237">Проблемы с хромом: [1086817][CR1086817], [1080569][CR1080569]</span><span class="sxs-lookup"><span data-stu-id="c70b0-237">Chromium issues: [1086817][CR1086817], [1080569][CR1080569]</span></span>  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a><span data-ttu-id="c70b0-238">Маяк 6.2 в панели Маяк</span><span class="sxs-lookup"><span data-stu-id="c70b0-238">Lighthouse 6.2 in the Lighthouse panel</span></span>  

<span data-ttu-id="c70b0-239">Средство **Lighthouse** теперь работает Lighthouse 6.2.</span><span class="sxs-lookup"><span data-stu-id="c70b0-239">The **Lighthouse** tool is now running Lighthouse 6.2.</span></span>  <span data-ttu-id="c70b0-240">Полный список изменений перейдите к заметкам [о выпуске Lighthouse.][GithubGooglechromeLighthouseV620]</span><span class="sxs-lookup"><span data-stu-id="c70b0-240">For a full list of changes, navigate to the [Lighthouse release notes][GithubGooglechromeLighthouseV620].</span></span>  

<span data-ttu-id="c70b0-241">Проблема Chromium: [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="c70b0-241">Chromium issue: [#772558][CR772558]</span></span>  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a><span data-ttu-id="c70b0-242">Амортизации других истоков в области "Работники службы"</span><span class="sxs-lookup"><span data-stu-id="c70b0-242">Deprecation of other origins listing in the Service Workers pane</span></span>  

<span data-ttu-id="c70b0-243">DevTools теперь предоставляет ссылку из области сотрудников службы \*\*\*\* **\.** Средство приложения > панели сотрудников службы\) для просмотра полного списка сотрудников служб из других истоков. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c70b0-243">DevTools now provides a link from the **Service workers** pane \(**Application** tool > **Service workers** pane\) to view the full list of service workers from other origins.</span></span>  <span data-ttu-id="c70b0-244">Чтобы получить доступ к списку без открытия DevTools, перейдите к `edge://service-worker-internals/?devtools` .</span><span class="sxs-lookup"><span data-stu-id="c70b0-244">To access the list without opening the DevTools, navigate to `edge://service-worker-internals/?devtools`.</span></span>  

<span data-ttu-id="c70b0-245">Ранее в DevTools отображался список, вложенный в > **службы.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c70b0-245">Previously DevTools displayed a list nested under the **Application** tool > **Service workers** pane.</span></span>  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Ссылка на другие истоки" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   <span data-ttu-id="c70b0-247">Ссылка на другие истоки</span><span class="sxs-lookup"><span data-stu-id="c70b0-247">Link to other origins</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-248">Проблема Chromium: [#807440][CR807440]</span><span class="sxs-lookup"><span data-stu-id="c70b0-248">Chromium issue: [#807440][CR807440]</span></span>  

### <a name="show-coverage-summary-for-filtered-items"></a><span data-ttu-id="c70b0-249">Показать сводку покрытия для отфильтрованных элементов</span><span class="sxs-lookup"><span data-stu-id="c70b0-249">Show coverage summary for filtered items</span></span>  

<span data-ttu-id="c70b0-250">DevTools теперь динамически пересчитываю и отображаем сводку сведений об охвате.</span><span class="sxs-lookup"><span data-stu-id="c70b0-250">DevTools now recalculate and display a summary of coverage information dynamically.</span></span>  <span data-ttu-id="c70b0-251">Динамический дисплей запускается при применении фильтров в средстве [Coverage.][DevtoolsCoverageIndex]</span><span class="sxs-lookup"><span data-stu-id="c70b0-251">The dynamic display is triggered when filters are applied in the [Coverage][DevtoolsCoverageIndex] tool.</span></span>  <span data-ttu-id="c70b0-252">Перед тем как средство **Coverage** всегда отображает сводку всех сведений об охвате.</span><span class="sxs-lookup"><span data-stu-id="c70b0-252">Before the **Coverage** tool always displayed a summary of all coverage information.</span></span>  

<span data-ttu-id="c70b0-253">В первом из следующих рисунков сводка сначала отображает, а во второй из следующих фигур отображается сводка после того, как применяется фильтрация `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.</span><span class="sxs-lookup"><span data-stu-id="c70b0-253">In the first of the following figures, the summary initially displays `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` and in the second of the following figures, the summary displays `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` after CSS filtering is applied.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Сводка по охвату" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         <span data-ttu-id="c70b0-255">Сводка по охвату</span><span class="sxs-lookup"><span data-stu-id="c70b0-255">Coverage summary</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Сводка по охвату для отфильтрованных элементов" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         <span data-ttu-id="c70b0-257">Сводка по охвату для отфильтрованных элементов</span><span class="sxs-lookup"><span data-stu-id="c70b0-257">Coverage summary for filtered items</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="c70b0-258">Проблема Chromium: [#1061385][CR1090802]</span><span class="sxs-lookup"><span data-stu-id="c70b0-258">Chromium issue: [#1061385][CR1090802]</span></span>  

### <a name="new-frame-details-view-in-application-panel"></a><span data-ttu-id="c70b0-259">Представление новых сведений о кадре в панели Приложения</span><span class="sxs-lookup"><span data-stu-id="c70b0-259">New frame details view in Application panel</span></span>  

<span data-ttu-id="c70b0-260">В DevTools теперь покажите подробное представление для каждого кадра.</span><span class="sxs-lookup"><span data-stu-id="c70b0-260">DevTools now show a detailed view for each frame.</span></span>  <span data-ttu-id="c70b0-261">Чтобы получить к нему доступ, выберите кадр в меню **Frames** в **инструменте Application.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-261">To access it, choose a frame under the **Frames** menu in the **Application** tool.</span></span>  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Новое подробное представление кадра в панели Приложения" lightbox="../../media/2020/08/frame-details.msft.png":::
   <span data-ttu-id="c70b0-263">Новое подробное представление кадра в **инструменте Application**</span><span class="sxs-lookup"><span data-stu-id="c70b0-263">New detailed view for a frame in **Application** tool</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-264">Проблема Chromium: [#1093247][CR1093247]</span><span class="sxs-lookup"><span data-stu-id="c70b0-264">Chromium issue: [#1093247][CR1093247]</span></span>  

#### <a name="frame-details-for-opened-windows"></a><span data-ttu-id="c70b0-265">Сведения о кадре для открытых окон</span><span class="sxs-lookup"><span data-stu-id="c70b0-265">Frame details for opened windows</span></span>  

<span data-ttu-id="c70b0-266">Открытые окна и всплывающие окна теперь отображаются и под деревом кадров.</span><span class="sxs-lookup"><span data-stu-id="c70b0-266">Open windows and pop-up windows now display under the frame tree as well.</span></span>  <span data-ttu-id="c70b0-267">Подробный обзор открытых окон включает дополнительные сведения о безопасности.</span><span class="sxs-lookup"><span data-stu-id="c70b0-267">The detailed view of the opened windows includes additional security information.</span></span>  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Новое подробное представление кадра для открытых окон" lightbox="../../media/2020/08/window-opener.msft.png":::
   <span data-ttu-id="c70b0-269">Новое подробное представление кадра для открытых окон</span><span class="sxs-lookup"><span data-stu-id="c70b0-269">New frame detailed view for opened windows</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-270">Проблема Chromium: [#1107766][CR1107766]</span><span class="sxs-lookup"><span data-stu-id="c70b0-270">Chromium issue: [#1107766][CR1107766]</span></span>  

#### <a name="security-and-isolation-information"></a><span data-ttu-id="c70b0-271">Сведения о безопасности и изоляции</span><span class="sxs-lookup"><span data-stu-id="c70b0-271">Security and isolation information</span></span>  

<span data-ttu-id="c70b0-272">Безопасный контекст, [cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]и [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] теперь отображаются в деталях кадра.</span><span class="sxs-lookup"><span data-stu-id="c70b0-272">Secure context, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep], and [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] are now displayed in the frame details.</span></span>  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Сведения о безопасности и изоляции" lightbox="../../media/2020/08/coep-coop.msft.png":::
   <span data-ttu-id="c70b0-274">Сведения о безопасности и изоляции</span><span class="sxs-lookup"><span data-stu-id="c70b0-274">Security and isolation information</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-275">В будущем команда Microsoft Edge DevTools и команда Chrome DevTools планируют добавить дополнительные сведения о безопасности в кадр.</span><span class="sxs-lookup"><span data-stu-id="c70b0-275">In the future, the Microsoft Edge DevTools team and the Chrome DevTools team are planning to add more security information to the frame details.</span></span>  

<span data-ttu-id="c70b0-276">Проблема Chromium: [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="c70b0-276">Chromium issue: [#1051466][CR1051466]</span></span>  

### <a name="elements-and-network-panel-updates"></a><span data-ttu-id="c70b0-277">Обновления элементов и сетевых панелей</span><span class="sxs-lookup"><span data-stu-id="c70b0-277">Elements and Network panel updates</span></span>  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a><span data-ttu-id="c70b0-278">Доступное предложение цвета в области Стилей</span><span class="sxs-lookup"><span data-stu-id="c70b0-278">Accessible color suggestion in the Styles pane</span></span>  

<span data-ttu-id="c70b0-279">DevTools теперь предоставляет предложения по цвету для текста с низким контрастом цвета.</span><span class="sxs-lookup"><span data-stu-id="c70b0-279">DevTools now provides color suggestions for low color contrast text.</span></span>  

<span data-ttu-id="c70b0-280">В приведенной ниже `h1` примере имеется текст с низким контрастом.</span><span class="sxs-lookup"><span data-stu-id="c70b0-280">In the example below, `h1` has low contrast text.</span></span>  <span data-ttu-id="c70b0-281">Чтобы исправить это, откройте выборщик цвета `color` свойства в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-281">To fix it, open the color picker of the `color` property in the **Styles** pane.</span></span>  <span data-ttu-id="c70b0-282">После расширения раздела **Коэффициент контраста** в DevTools предлагает предложения по цвету AA и AAA.</span><span class="sxs-lookup"><span data-stu-id="c70b0-282">After you expand the **Contrast ratio** section, DevTools provides AA and AAA color suggestions.</span></span>  <span data-ttu-id="c70b0-283">Выберите предложенный цвет, чтобы применить его.</span><span class="sxs-lookup"><span data-stu-id="c70b0-283">Choose the suggested color to apply the color.</span></span>  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Выбор цвета предлагает предложения по цвету AA и AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   <span data-ttu-id="c70b0-285">Выбор цвета предлагает предложения по цвету AA и AAA</span><span class="sxs-lookup"><span data-stu-id="c70b0-285">Color picker suggests AA and AAA color suggestions</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-286">Проблема Chromium: [#1093227][CR1093227]</span><span class="sxs-lookup"><span data-stu-id="c70b0-286">Chromium issue: [#1093227][CR1093227]</span></span>  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a><span data-ttu-id="c70b0-287">Восстановление области свойств в панели Elements</span><span class="sxs-lookup"><span data-stu-id="c70b0-287">Reinstate Properties pane in the Elements panel</span></span>  

<span data-ttu-id="c70b0-288">Области **свойств** возвращается.</span><span class="sxs-lookup"><span data-stu-id="c70b0-288">The **Properties** pane is back.</span></span>  <span data-ttu-id="c70b0-289">Он был [обесценит в Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span><span class="sxs-lookup"><span data-stu-id="c70b0-289">It was [deprecated in Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].</span></span>  <span data-ttu-id="c70b0-290">Команда Microsoft Edge DevTools и команда Chrome DevTools планируют усовершенствования для проверки свойств элементов.</span><span class="sxs-lookup"><span data-stu-id="c70b0-290">The Microsoft Edge DevTools team and the Chrome DevTools team are planning improvements for inspecting properties of elements.</span></span>  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Панель свойств в панели Elements" lightbox="../../media/2020/08/properties-pane.msft.png":::
   <span data-ttu-id="c70b0-292">**Области свойств** в **средстве Elements**</span><span class="sxs-lookup"><span data-stu-id="c70b0-292">**Properties** pane in the **Elements** tool</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-293">Проблема Chromium:</span><span class="sxs-lookup"><span data-stu-id="c70b0-293">Chromium issue:</span></span>  <!--  [#1105205][CR1105205],  -->  <span data-ttu-id="c70b0-294">[#1116085] [CR1116085]</span><span class="sxs-lookup"><span data-stu-id="c70b0-294">[#1116085][CR1116085]</span></span>  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a><span data-ttu-id="c70b0-295">Автоматические настраиваемые шрифты в области Стилей</span><span class="sxs-lookup"><span data-stu-id="c70b0-295">Autocomplete custom fonts in the Styles pane</span></span>  

<span data-ttu-id="c70b0-296">Импортируемые лица шрифтов теперь добавляются в список автозаполнения CSS при редактировании свойства `font-family` в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-296">Imported font faces are now added to the list of CSS autocompletion when editing the `font-family` property in the **Styles** pane.</span></span>  

<span data-ttu-id="c70b0-297">Например, если на локальной машине установлен настраиваемый шрифт, он отображается в `monospace` списке завершения CSS.</span><span class="sxs-lookup"><span data-stu-id="c70b0-297">For example, if `monospace` is a custom font installed on the local machine, it displays in the CSS completion list.</span></span>  <span data-ttu-id="c70b0-298">В предыдущих версиях Microsoft Edge шрифт не отображался.</span><span class="sxs-lookup"><span data-stu-id="c70b0-298">In previous versions of Microsoft Edge, the font was not displayed.</span></span>

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Автоматические настраиваемые шрифты" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   <span data-ttu-id="c70b0-300">Автоматические настраиваемые шрифты</span><span class="sxs-lookup"><span data-stu-id="c70b0-300">Autocomplete custom fonts</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-301">Проблема Chromium: [#1106221][CR1106221]</span><span class="sxs-lookup"><span data-stu-id="c70b0-301">Chromium issue: [#1106221][CR1106221]</span></span>  

#### <a name="consistently-display-resource-type-in-network-panel"></a><span data-ttu-id="c70b0-302">Последовательно отображает тип ресурса в панели Network</span><span class="sxs-lookup"><span data-stu-id="c70b0-302">Consistently display resource type in Network panel</span></span>  

<span data-ttu-id="c70b0-303">DevTools теперь последовательно отображает тот же тип ресурсов, что и исходный запрос сети, и приложения к значению столбца Type при перенаправлении `/ Redirect` \(КОД состояния HTTP 302\) происходит. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c70b0-303">DevTools now consistently display the same resource type as the original network request and appends `/ Redirect` to the **Type** column value when redirection \(HTTP status code 302\) happens.</span></span>  

<span data-ttu-id="c70b0-304">Ранее DevTools изменил тип на `Other` иногда.</span><span class="sxs-lookup"><span data-stu-id="c70b0-304">Previously DevTools changed the type to `Other` sometimes.</span></span>  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Отображение типа ресурса перенаправления" lightbox="../../media/2020/08/network-redirect.msft.png":::
   <span data-ttu-id="c70b0-306">Отображение типа ресурса перенаправления</span><span class="sxs-lookup"><span data-stu-id="c70b0-306">Display redirect resource type</span></span>  
:::image-end:::  

<span data-ttu-id="c70b0-307">Проблема Chromium: [#997694][CR997694]</span><span class="sxs-lookup"><span data-stu-id="c70b0-307">Chromium issue: [#997694][CR997694]</span></span>  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a><span data-ttu-id="c70b0-308">Clear buttons in the Elements and Network tools</span><span class="sxs-lookup"><span data-stu-id="c70b0-308">Clear buttons in the Elements and Network tools</span></span>  

<span data-ttu-id="c70b0-309">В следующих текстовых полях теперь есть **кнопки Clear.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-309">The following text boxes now have **Clear** buttons.</span></span>  

*   <span data-ttu-id="c70b0-310">Текстовые поля фильтра в **области стилей** и **средстве Network.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-310">The filter text boxes in the **Styles** pane and **Network** tool.</span></span>  
*   <span data-ttu-id="c70b0-311">Текстовое поле поиска DOM в **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="c70b0-311">The DOM search text box in the **Elements** tool.</span></span>  

<span data-ttu-id="c70b0-312">Выберите **кнопку Clear,** чтобы удалить вводимый текст.</span><span class="sxs-lookup"><span data-stu-id="c70b0-312">Choose the **Clear** button to remove any inputted text.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Четкие кнопки в панелях Elements" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         <span data-ttu-id="c70b0-314">Clear buttons in the **Elements** tools</span><span class="sxs-lookup"><span data-stu-id="c70b0-314">Clear buttons in the **Elements** tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Clear buttons in the Network panels" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         <span data-ttu-id="c70b0-316">Clear buttons in the  **Network** tools</span><span class="sxs-lookup"><span data-stu-id="c70b0-316">Clear buttons in the  **Network** tools</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c70b0-317">Проблема Chromium: [#1067184][CR1067184]</span><span class="sxs-lookup"><span data-stu-id="c70b0-317">Chromium issue: [#1067184][CR1067184]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="c70b0-318">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="c70b0-318">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c70b0-319">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c70b0-319">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c70b0-320">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="c70b0-320">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="c70b0-321">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c70b0-321">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок Параметры DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Обесценение области свойств в панели Elements — что нового в DevTools (Microsoft Edge 84) | Документы Майкрософт"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS — Что нового в DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включить экспериментальные API - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включить viewer source Order — экспериментальные функции | Документы Майкрософт"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "таблица — справочные | Документы Майкрософт"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS со вкладками Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering — справочная | Документы Майкрософт"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Просмотр и отламывка информации о медиа-игроках | Документы Майкрософт"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Код "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio клавиши кода для Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"
[CR384968]: https://crbug.com/384968 "Возможность игнорировать локальные () шрифты | Ошибки Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR807440]: https://crbug.com/807440 "Chrome блокируется с большим количеством SWs | Ошибки Chromium"  
[CR997694]: https://crbug.com/997694 "XHR-запросы со статусом 302 не показаны в фильтре \"xhr\" в сетевых панелях | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Запрос на функции: Устройства DevTools должны подражать складным и двухэкранным устройствам | Ошибки Chromium"  
[CR1067184]: https://crbug.com/1067184 "Запрос на функции: кнопка clear filter on Network & Elements -> ввода фильтра | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ панели проблем корабля | Ошибки Chromium"  
[CR1080569]: https://crbug.com/1080569 "acorn не поддерживает операторов логических назначений | Ошибки Chromium"  
[CR1080589]: https://crbug.com/1080589 "Классифицировать проблемы по сторонним и | Ошибки Chromium"  
[CR1086817]: https://crbug.com/1086817 "acorn не поддерживает числимые сепараторы | Ошибки Chromium"  
[CR1090802]: https://crbug.com/1090802 "Имитация изменений состояния ожидания из API обнаружения | Ошибки Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: предложить ближайший доступный цвет | Ошибки Chromium"  
[CR1093247]: https://crbug.com/1093247 "Отображение информации о кадрах в панели приложений | Ошибки Chromium"  
[CR1094406]: https://crbug.com/1094406 "Разработчикам нужен зритель исходных заказов для AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: поддержка эмулировать функцию мультимедиа с пониженным | Ошибки Chromium"  
[CR1096481]: https://crbug.com/1096481 "Вопросы размещения баннеров | Ошибки Chromium"  
[CR1100253]: https://crbug.com/1100253 "Добавление ярлыка узла экрана в меню контекста Element | Ошибки Chromium"  
[CR1103316]: https://crbug.com/1103316 "Поиск элементов не решаетNode (выделение текста и т. д.) при первом поиске | Ошибки Chromium"  
[CR1103854]: https://crbug.com/1103854 "De-obfuscate X-Client-Data values in Developer Tools | Ошибки Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Добавьте импортируемые шрифты в автозаполнение семейства шрифтов в панели https://crbug.com/1106221 Styles | Ошибки Chromium"  
[CR1107766]: "Отображение информации о кадрах, созданных https://crbug.com/1107766 "window.open()" в дереве кадров | Ошибки Chromium"  
[CR1115011]: "При копировании таблицы из консоли структура таблицы не сохраняется https://crbug.com/1115011 | Ошибки Chromium"  
[CR1116085]: "Пожалуйста, верни https://crbug.com/1116085 инспектора свойств DevTools | Ошибки Chromium"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Проекты редактора рабочей группы W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 — GoogleChrome/lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Буферы протокола | Разработчики Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Логическое назначение | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Числимые сепараторы | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Создание изолированного веб-сайта \"cross-origin\" с помощью coOP и COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Обнаружение неактивных пользователей с помощью API обнаружения | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Избегайте не композитных анимаций | web.dev"  

> [!NOTE]
> <span data-ttu-id="c70b0-382">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c70b0-382">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c70b0-383">Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/08/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="c70b0-383">The original page is found [here](https://developers.google.com/web/updates/2020/08/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c70b0-385">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c70b0-385">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
