---
description: Новые средства отладки CSS Grid, средство Webauthn, инструменты для перемещения и панель компьютерной панели.
title: Новые возможности в DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 621df58042b390897646a359a208ea62d1a6e06c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398569"
---
# <a name="whats-new-in-devtools-microsoft-edge-87"></a><span data-ttu-id="5904e-104">Что нового в DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="5904e-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a><span data-ttu-id="5904e-105">Улучшение локализации DevTools</span><span class="sxs-lookup"><span data-stu-id="5904e-105">Improving DevTools localization</span></span>  

<span data-ttu-id="5904e-106">Чтобы удовлетворить ваши потребности в переводе, команда Microsoft Edge DevTools нацелена на улучшение качества перевода.</span><span class="sxs-lookup"><span data-stu-id="5904e-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="5904e-107">Начиная с microsoft Edge версии 87, несколько строк и терминов заблокированы и не изменяются даже при отображке остальных версий DevTools на других языках.</span><span class="sxs-lookup"><span data-stu-id="5904e-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="5904e-108">Список затронутых строк и терминов включает следующие.</span><span class="sxs-lookup"><span data-stu-id="5904e-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="5904e-109">Строки в **средстве Маяк.**</span><span class="sxs-lookup"><span data-stu-id="5904e-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="5904e-110">Термин `service worker` .</span><span class="sxs-lookup"><span data-stu-id="5904e-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="5904e-111">Некоторые **фильтры сетевых** средств, такие `URL` как , и `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="5904e-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="5904e-112">API [консоли $0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="5904e-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="5904e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] теперь доступен [](/microsoft-edge/devtools-guide-chromium/console/index.md) в консоли для пользователей локализованных версий DevTools.</span><span class="sxs-lookup"><span data-stu-id="5904e-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="5904e-114">Спасибо глобальному сообществу разработчиков за помощь в улучшении локализации Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5904e-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="5904e-115">Продолжайте отправлять [отзывы о качестве локализации,](#getting-in-touch-with-microsoft-edge-devtools-team) чтобы улучшить поддержку DevTools во всех локальных местах.</span><span class="sxs-lookup"><span data-stu-id="5904e-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="5904e-116">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="5904e-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Сетевой инструмент с не локализованными фильтрами" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="5904e-118">**Сетевое** панно с не локализованными фильтрами</span><span class="sxs-lookup"><span data-stu-id="5904e-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a><span data-ttu-id="5904e-119">Перемещение инструментов между верхними и нижними панелями</span><span class="sxs-lookup"><span data-stu-id="5904e-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="5904e-120">DevTools теперь поддерживает перемещение инструментов между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="5904e-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="5904e-121">Настройте devTools и повысите производительность, одновременно просматривая любое сочетание двух инструментов.</span><span class="sxs-lookup"><span data-stu-id="5904e-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="5904e-122">Например, просмотр **элементов** и средств **Sources** одновременно \(путем перемещения средства **Источники** в нижнее\).</span><span class="sxs-lookup"><span data-stu-id="5904e-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="5904e-123">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1075732.][CR1075732]</span><span class="sxs-lookup"><span data-stu-id="5904e-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5904e-124">Чтобы переместить любой верхний инструмент в нижнее, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Перемещение в нижнее**.</span><span class="sxs-lookup"><span data-stu-id="5904e-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Перемещение в нижнее" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="5904e-126">Перемещение в нижнее</span><span class="sxs-lookup"><span data-stu-id="5904e-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5904e-127">Чтобы переместить любой нижний инструмент в верхнюю часть, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Перемещение вверх.**</span><span class="sxs-lookup"><span data-stu-id="5904e-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Перемещение на вершину" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="5904e-129">Перемещение на вершину</span><span class="sxs-lookup"><span data-stu-id="5904e-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a><span data-ttu-id="5904e-130">Сохранение и экспорт с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="5904e-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="5904e-132">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="5904e-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="5904e-133">Средство **сетевой** консоли теперь имеет улучшенную совместимость с схемами [Postman v2.1][PostmanSchemaJsonCollectionv210Index] и [OpenAPI v2.][SwaggerSpecificationV2]</span><span class="sxs-lookup"><span data-stu-id="5904e-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="5904e-134">Чтобы включить эксперимент, перейдите к [включаем экспериментальные функции][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и выберите почтовый ящик рядом с **сетевой консолью.**</span><span class="sxs-lookup"><span data-stu-id="5904e-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="5904e-135">Дополнительные сведения о **сетевой консоли**перейдите к [функции Включить экспериментальную][DevtoolsExperimentalFeaturesEnableNetworkConsole]функцию сетевой консоли .</span><span class="sxs-lookup"><span data-stu-id="5904e-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="5904e-136">В этом эксперименте теперь поддерживаются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5904e-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="5904e-137">Сохранение и экспорт коллекций и сред.</span><span class="sxs-lookup"><span data-stu-id="5904e-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="5904e-138">Изменить и экспортировать наборы переменных среды в **средстве сетевой консоли.**</span><span class="sxs-lookup"><span data-stu-id="5904e-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="5904e-139">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="5904e-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Введите имя для новой среды" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="5904e-141">Введите имя для новой среды</span><span class="sxs-lookup"><span data-stu-id="5904e-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Выберите формат для новой среды" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="5904e-143">Выберите формат для новой среды</span><span class="sxs-lookup"><span data-stu-id="5904e-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a><span data-ttu-id="5904e-144">Улучшено средство CSS Grid</span><span class="sxs-lookup"><span data-stu-id="5904e-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="5904e-146">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="5904e-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="5904e-147">Теперь Microsoft Edge DevTools поддерживает следующие функции для проверки, просмотра и отладки сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="5904e-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="5904e-148">Отображение упрощенной сетки с помощью средства **Inspect** или получения более подробных сведений с постоянными наложениями.</span><span class="sxs-lookup"><span data-stu-id="5904e-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="5904e-149">Чтобы включить постоянные наложения сетки, выберите значок сетки рядом с элементом контейнера сетки в средстве **Elements** или выберите сетку в **средстве Layout.**</span><span class="sxs-lookup"><span data-stu-id="5904e-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="5904e-150">Вы можете включить постоянные наложения для нескольких сетей.</span><span class="sxs-lookup"><span data-stu-id="5904e-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="5904e-151">Новый инструмент **Layout** позволяет легко настраивать наложения сетки и настраивать внешний вид и содержимое для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="5904e-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="5904e-152">Функции включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5904e-152">The features are turned on by default.</span></span>  <span data-ttu-id="5904e-153">Дополнительные сведения об этих функциях перейдите к [сеткам CSS.][DevtoolsCssGrid]</span><span class="sxs-lookup"><span data-stu-id="5904e-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="5904e-154">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="5904e-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="5904e-155">Кроме того, команда Microsoft Edge DevTools сотрудничает с командой Chrome DevTools и сообществом Chromium, чтобы добавить в DevTools новые функции инструментов flexbox.</span><span class="sxs-lookup"><span data-stu-id="5904e-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="5904e-156">Для обновления инструментов flexbox в проекте с открытым исходным кодом Chromium перейдите к выпуску [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="5904e-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Средство макета с сетками" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="5904e-158">**Средство макета** с сетками</span><span class="sxs-lookup"><span data-stu-id="5904e-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="5904e-159">Настройка ярлыков клавиатуры в параметрах</span><span class="sxs-lookup"><span data-stu-id="5904e-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="5904e-161">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="5904e-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="5904e-162">Теперь вы можете настроить ярлык клавиатуры для любого действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="5904e-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="5904e-163">Так как Microsoft Edge версии 84, вы можете выбрать между Visual Studio **код** и **DevTools (по умолчанию)** предуговосток для [клавиши ярлыки][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="5904e-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="5904e-164">Начиная с microsoft Edge версии 87, вы можете включить эксперимент редактора клавиши **Включить,** чтобы дополнительно настроить ярлыки [клавиатуры.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]</span><span class="sxs-lookup"><span data-stu-id="5904e-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="5904e-165">Чтобы включить эксперимент, перейдите к [включаем экспериментальные][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функции и выберите почтовый ящик рядом с **редактором клавиши Включить**ярлык .</span><span class="sxs-lookup"><span data-stu-id="5904e-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="5904e-166">Дополнительные сведения о настройке и изменении сочетаний клавиш см. в разделе о [включении экспериментальной функции редактора сочетания клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="5904e-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="5904e-167">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="5904e-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Настраиваемый ярлык для прио паузы в скрипте" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="5904e-169">Настраиваемый ярлык для прио паузы в скрипте</span><span class="sxs-lookup"><span data-stu-id="5904e-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a><span data-ttu-id="5904e-170">Введение microsoft Edge Tools для расширения Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="5904e-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="5904e-171">Элементы **для Visual Studio и** сети для **Visual Studio** теперь объединены в новые средства разработки Microsoft Edge для [расширения][VisualStudioCodeMarketplaceMsEdgedevtools] Visual Studio кода.</span><span class="sxs-lookup"><span data-stu-id="5904e-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="5904e-172">Используйте Microsoft Edge DevTools для следующих действий, не покидая Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="5904e-172">Use the Microsoft Edge DevTools for the following activities without leaving Microsoft Visual Studio Code.</span></span>  

*   <span data-ttu-id="5904e-173">Отламка DOM</span><span class="sxs-lookup"><span data-stu-id="5904e-173">Debug the DOM</span></span>  
*   <span data-ttu-id="5904e-174">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="5904e-174">Edit CSS</span></span>  
*   <span data-ttu-id="5904e-175">Проверка сетевого трафика</span><span class="sxs-lookup"><span data-stu-id="5904e-175">Inspect network traffic</span></span>  

<span data-ttu-id="5904e-176">С помощью расширения запустите Microsoft Edge, подключите существующий экземпляр браузера или используйте безголовые браузеры непосредственно из редактора.</span><span class="sxs-lookup"><span data-stu-id="5904e-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="5904e-177">Чтобы начать вносить свой вклад и подавать свои отзывы об этом расширении, перейдите в [Microsoft Edge Developer Tools для][GithubMicrosoftVscodeEdgeDevtools] Visual Studio кода на GitHub.</span><span class="sxs-lookup"><span data-stu-id="5904e-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Использование экрана расширения в режиме полного браузера" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="5904e-179">Использование экрана расширения в режиме полного браузера</span><span class="sxs-lookup"><span data-stu-id="5904e-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Использование расширения в безголовом скриншоте режима" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="5904e-181">Использование расширения в безголовом скриншоте режима</span><span class="sxs-lookup"><span data-stu-id="5904e-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="5904e-182">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="5904e-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a><span data-ttu-id="5904e-183">Новый инструмент WebAuthn</span><span class="sxs-lookup"><span data-stu-id="5904e-183">New WebAuthn tool</span></span>  

<span data-ttu-id="5904e-184">В более ранних версиях Microsoft Edge не было поддержки отладки webAuthn.</span><span class="sxs-lookup"><span data-stu-id="5904e-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="5904e-185">Чтобы протестировать свое веб-приложение с API веб-проверки подлинности, необходимы [физические аутентификации.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="5904e-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="5904e-186">С помощью нового **средства WebAuthn** вы можете делать следующие действия без использования каких-либо физических аутентификаций.</span><span class="sxs-lookup"><span data-stu-id="5904e-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="5904e-187">Эмулировать аутентификацию</span><span class="sxs-lookup"><span data-stu-id="5904e-187">Emulate authenticators</span></span>
*   <span data-ttu-id="5904e-188">Настройка атрибутов аутентификаций</span><span class="sxs-lookup"><span data-stu-id="5904e-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="5904e-189">Проверка состояния аутентификаций</span><span class="sxs-lookup"><span data-stu-id="5904e-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="5904e-190">Дополнительные сведения о функции **WebAuthn** перейдите к эмулировать аутентификацию и отладку [WebAuthn в Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="5904e-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="5904e-191">Вы можете эмулировать аутентификацию и отладить API веб-проверки [подлинности][GithubW3cWebauthn] с помощью нового средства [WebAuthn.][DevtoolsWebauthnIndex]</span><span class="sxs-lookup"><span data-stu-id="5904e-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="5904e-192">Чтобы открыть **средство WebAuthn,** выберите значок Настройка и управление **значком DevTools** \( \) > Дополнительные средства `...` \*\*\*\*  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="5904e-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="5904e-193">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="5904e-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Откройте средство WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="5904e-195">Откройте **средство WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="5904e-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="5904e-197">**Средство WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="5904e-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="5904e-198">Обновления инструмента Elements</span><span class="sxs-lookup"><span data-stu-id="5904e-198">Elements tool updates</span></span>  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a><span data-ttu-id="5904e-199">Просмотр области компьютерной боковой панели в области Стилей</span><span class="sxs-lookup"><span data-stu-id="5904e-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="5904e-200">Переналадка **вычислительной области** в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="5904e-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="5904e-201">Вычислительная **области** в области **Стилей** разрушается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5904e-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="5904e-202">Чтобы его перенажать, выберите кнопку.</span><span class="sxs-lookup"><span data-stu-id="5904e-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="5904e-203">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="5904e-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Откройте панель computed sidebar" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="5904e-205">Откройте панель **computed sidebar**</span><span class="sxs-lookup"><span data-stu-id="5904e-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Вычислительная панель боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="5904e-207">**Вычислительная панель боковой** панели</span><span class="sxs-lookup"><span data-stu-id="5904e-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a><span data-ttu-id="5904e-208">Группировка свойств CSS в панели Computed</span><span class="sxs-lookup"><span data-stu-id="5904e-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="5904e-209">Чтобы просмотреть примененный CSS с меньшим прокрутки, сгруппировать свойства CSS по категориям в **области Computed.**</span><span class="sxs-lookup"><span data-stu-id="5904e-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="5904e-210">Вы также можете выборочно сосредоточиться на наборе связанных свойств во время проверки CSS.</span><span class="sxs-lookup"><span data-stu-id="5904e-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="5904e-211">Из средства **Elements** выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="5904e-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="5904e-212">Чтобы сгруппировать \(или разгруппировать\) свойства CSS, перегнастить **групповой почтовый** ящик.</span><span class="sxs-lookup"><span data-stu-id="5904e-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="5904e-213">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к [#1096230,][CR1096230] [#1084673][CR1084673]и [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="5904e-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Группировка свойств CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="5904e-215">Группировка свойств CSS</span><span class="sxs-lookup"><span data-stu-id="5904e-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a><span data-ttu-id="5904e-216">Маяк 6.4 в средстве Маяк</span><span class="sxs-lookup"><span data-stu-id="5904e-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="5904e-217">Инструмент **Lighthouse** теперь работает Lighthouse 6.4.</span><span class="sxs-lookup"><span data-stu-id="5904e-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="5904e-218">Полный список изменений перейдите к заметкам [о выпуске Lighthouse.][GithubGoogleChromeLighthouseReleasesV641]</span><span class="sxs-lookup"><span data-stu-id="5904e-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="5904e-219">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="5904e-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <a name="performancemark-events-in-the-timings-section"></a><span data-ttu-id="5904e-220">события performance.mark() в разделе Timings</span><span class="sxs-lookup"><span data-stu-id="5904e-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="5904e-221">Раздел **Timings записи** в средстве [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] теперь отмечает `performance.mark()` события.</span><span class="sxs-lookup"><span data-stu-id="5904e-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="5904e-222">Чтобы попробовать эту функцию и оценить производительность кода JavaScript, добавьте `performance.mark()` события в код.</span><span class="sxs-lookup"><span data-stu-id="5904e-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="5904e-223">Например, следующий фрагмент кода добавляет маркеры до и после цикла, который итерирует от 0 до 1000 с помощью приращений `for` 7.</span><span class="sxs-lookup"><span data-stu-id="5904e-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="5904e-224">Затем откройте средство [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] и перейдите в раздел **Timings для** записи кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5904e-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="5904e-225">Добавленные `performance.mark()` события теперь отображаются в записи.</span><span class="sxs-lookup"><span data-stu-id="5904e-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="События Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="5904e-227">события</span><span class="sxs-lookup"><span data-stu-id="5904e-227">events</span></span>  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a><span data-ttu-id="5904e-228">Новые фильтры типа ресурсов и URL-адресов в средстве Network</span><span class="sxs-lookup"><span data-stu-id="5904e-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="5904e-229">Используйте новые `resource-type` и `url` ключевые слова в средстве **Network** для фильтрации сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="5904e-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="5904e-230">Например, используйте `resource-type:image` для фокусии на сетевых запросах, которые являются изображениями.</span><span class="sxs-lookup"><span data-stu-id="5904e-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="фильтр типа ресурса" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="5904e-232">фильтр типа ресурса</span><span class="sxs-lookup"><span data-stu-id="5904e-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="5904e-233">Чтобы узнать больше специальных ключевых слов, таких как `resource-type` `url` и , перейдите к [фильтрации запросов по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="5904e-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="5904e-234">Чтобы просмотреть обновления этой функции в проекте с открытым исходным [][CR1121141] кодом Chromium в режиме реального времени, перейдите к #1121141 [и #1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="5904e-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <a name="frame-details-view-updates"></a><span data-ttu-id="5904e-235">Обновления представления сведений о фрейме</span><span class="sxs-lookup"><span data-stu-id="5904e-235">Frame details view updates</span></span>  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a><span data-ttu-id="5904e-236">Отображение отчетов COEP и COOP в конечной точке</span><span class="sxs-lookup"><span data-stu-id="5904e-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="5904e-237">Просмотр конечной точки политики встраивщика cross-origin \(COEP\) и политики открытия кросс-происхождения \(COOP\) в разделе Изоляция & `reporting to` безопасности. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5904e-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="5904e-238">API [отчетов][MdnReportingApi] определяет новый http-заголовок, который позволяет указать конечные точки сервера для браузера для отправки предупреждений и `Report-To` ошибок.</span><span class="sxs-lookup"><span data-stu-id="5904e-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="5904e-239">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="5904e-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Отчеты до конечной точки" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="5904e-241">`reporting to`Конечная точка</span><span class="sxs-lookup"><span data-stu-id="5904e-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a><span data-ttu-id="5904e-242">Отображение режима отчетов только для COEP и COOP</span><span class="sxs-lookup"><span data-stu-id="5904e-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="5904e-243">В DevTools теперь `report-only` отображаются метки coEP и COOP, задаваемые в `report-only` режиме.</span><span class="sxs-lookup"><span data-stu-id="5904e-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="5904e-244">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="5904e-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Метка режима только для отчетов" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="5904e-246">Метка `report-only` режима</span><span class="sxs-lookup"><span data-stu-id="5904e-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a><span data-ttu-id="5904e-247">Просмотр и устранение проблем контрастности цветов в инструменте CSS Overview</span><span class="sxs-lookup"><span data-stu-id="5904e-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="5904e-249">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="5904e-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="5904e-250">Средство **CSS Overview** теперь отображает список элементов на странице с вопросами контрастности цвета.</span><span class="sxs-lookup"><span data-stu-id="5904e-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="5904e-251">На следующей демо-странице приводится пример проблемы контраста цвета.</span><span class="sxs-lookup"><span data-stu-id="5904e-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="5904e-252">Демонстрация доступных цветов CSS Обзор</span><span class="sxs-lookup"><span data-stu-id="5904e-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="5904e-253">Чтобы включить этот эксперимент, в **статье**  >  **Settings Experiments**выберите почтовый ящик **CSS Overview.**</span><span class="sxs-lookup"><span data-stu-id="5904e-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="5904e-254">Чтобы просмотреть список элементов с проблемой контрастности цвета, **выберите** **Текст**.</span><span class="sxs-lookup"><span data-stu-id="5904e-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="5904e-255">Чтобы открыть элемент в **средстве Elements,** выберите элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="5904e-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="5904e-256">Чтобы помочь устранить проблемы контрастности, Microsoft Edge DevTools автоматически [предоставляет цветовые предложения.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="5904e-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="5904e-257">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="5904e-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Проблемы с контрастом цвета" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="5904e-259">Проблемы с контрастом цвета</span><span class="sxs-lookup"><span data-stu-id="5904e-259">Low color contrast issues</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="5904e-260">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="5904e-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="5904e-261">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5904e-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="5904e-262">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="5904e-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="5904e-263">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5904e-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Обесценение области свойств в средстве Elements — что нового в DevTools (Microsoft Edge 84) | Документы Майкрософт"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS — Что нового в DevTools (Microsoft Edge 85) | Документы Майкрософт"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Доступное предложение цвета в области Стилей — что нового в DevTools (Microsoft Edge 86) | Документы Майкрософт"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript — справочные ссылки на API консоли | Документы Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справочные ссылки | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включить экспериментальные API - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор ярлыка клавиатуры — экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Включить сетевые консоли — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включить viewer source Order — экспериментальные функции | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "таблица — справочные | Документы Майкрософт"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS со вкладками Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Проверка CSS Grid | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering — справочная | Документы Майкрософт"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отламывка информации о медиа-игроках | Документы Майкрософт"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Запросы фильтрации по свойствам — эталонный | Документы Майкрософт"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Эмулировать аутентификацию и отладку WebAuthn в Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Код"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR1034663]: https://crbug.com/1034663 "Создание переднего входа для API тестирования WebAuthn | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка computed style исчезает в режиме отклика | Ошибки Chromium"  
[CR1075732]: https://crbug.com/1075732 "Персонализация DevTools — вкладки Movable | Ошибки Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: улучшаем способ, который мы представляем пользовательским свойствам CSS (aka). Переменные CSS) и их значения | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и воспроизведения синтетических сетевых запросов | Ошибки Chromium"  
[CR1096230]: https://crbug.com/1096230 "Свойства группы CSS по категориям в области вычислительных стилей | Ошибки Chromium"  
[CR1104188]: https://crbug.com/1104188 "Поиск сетевых средств не находит результатов при поиске полного URL-адреса | Ошибки Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: улучшение вкладки Computed Styles | Ошибки Chromium"  
[CR1120316]: https://crbug.com/1120316 "Выделение плохого контраста в CSS Обзор > цвета | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Разрешить фильтрацию по типу ресурса в сетевом журнале | Ошибки Chromium"  
[CR1121312]: https://crbug.com/1121312 "Параметры должны быть удалены из меню More Tools | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Flexbox tooling | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Локализация V2 | Ошибки Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Отчет об API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 — GoogleChrome/lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-| GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Привет! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Формат коллекции почтальонов v2.1.0 | Почтальон"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Спецификация OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="5904e-316">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5904e-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5904e-317">Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/10/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="5904e-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5904e-319">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5904e-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
