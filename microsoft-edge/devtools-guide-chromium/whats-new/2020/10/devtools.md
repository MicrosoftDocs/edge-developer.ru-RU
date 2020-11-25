---
description: Новые инструменты для отладки в КАСКАДных таблицах, средства Webauthn, средства для перемещаемых и вычисляемых панелей.
title: Новые возможности DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190007"
---
# <span data-ttu-id="38e25-104">Новые возможности DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="38e25-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="38e25-105">Улучшение локализации DevTools</span><span class="sxs-lookup"><span data-stu-id="38e25-105">Improving DevTools localization</span></span>  

<span data-ttu-id="38e25-106">В соответствии с потребностями перевода группа Microsoft Edge DevTools фокусируется на улучшении качества перевода.</span><span class="sxs-lookup"><span data-stu-id="38e25-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="38e25-107">Начиная с Microsoft Edge версии 87, некоторые строки и условия заблокированы и не изменяются даже в том случае, если остальные DevTools отображаются на других языках.</span><span class="sxs-lookup"><span data-stu-id="38e25-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="38e25-108">Ниже перечислены затронутые строки и термины.</span><span class="sxs-lookup"><span data-stu-id="38e25-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="38e25-109">Строки в инструменте **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="38e25-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="38e25-110">Термин `service worker` .</span><span class="sxs-lookup"><span data-stu-id="38e25-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="38e25-111">Некоторые фильтры **сетевых** средств, такие как `URL` ,, `XHR` `JS` и `CSS` .</span><span class="sxs-lookup"><span data-stu-id="38e25-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="38e25-112">API-интерфейс служебных программ для консоли [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .</span><span class="sxs-lookup"><span data-stu-id="38e25-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="38e25-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] теперь доступен на [консоли](/microsoft-edge/devtools-guide-chromium/console/index.md) для пользователей локализованных версий DevTools.</span><span class="sxs-lookup"><span data-stu-id="38e25-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="38e25-114">Благодарим вас за участие в глобальном сообществе разработчиков, которые помогут вам улучшить локализацию Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="38e25-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="38e25-115">Продолжите [отправку обратной связи по качеству локализации](#getting-in-touch-with-microsoft-edge-devtools-team) для улучшения поддержки DevTools на всех языках.</span><span class="sxs-lookup"><span data-stu-id="38e25-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="38e25-116">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="38e25-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Сетевое средство с нелокализованными фильтрами" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="38e25-118">Область **сети** с нелокализованными фильтрами</span><span class="sxs-lookup"><span data-stu-id="38e25-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="38e25-119">Перемещение инструментов между верхней и нижней панелями</span><span class="sxs-lookup"><span data-stu-id="38e25-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="38e25-120">DevTools теперь поддерживает перемещение инструментов между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="38e25-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="38e25-121">Настройка DevTools и повышение продуктивности благодаря одновременному просмотру любой комбинации двух инструментов.</span><span class="sxs-lookup"><span data-stu-id="38e25-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="38e25-122">Например, вы можете одновременно просматривать **элементы** и инструменты **исходного** кода (путем перемещения инструмента **источники** вниз).</span><span class="sxs-lookup"><span data-stu-id="38e25-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="38e25-123">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="38e25-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="38e25-124">Чтобы переместить верхний инструмент в нижнюю часть экрана, наведите на него указатель мыши, откройте контекстное меню, а затем выберите пункт **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="38e25-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Переместить вниз" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="38e25-126">Переместить вниз</span><span class="sxs-lookup"><span data-stu-id="38e25-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="38e25-127">Чтобы переместить нижние инструменты в верхнюю часть экрана, наведите указатель мыши на вкладку, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Перейти к началу**.</span><span class="sxs-lookup"><span data-stu-id="38e25-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Перейти к началу страницы" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="38e25-129">Перейти к началу страницы</span><span class="sxs-lookup"><span data-stu-id="38e25-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="38e25-130">Сохранение и экспорт с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="38e25-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="38e25-132">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="38e25-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="38e25-133">Средство **Network Console** теперь повысило совместимость с схемами [posts v 2.1][PostmanSchemaJsonCollectionv210Index] и [OpenAPI v2][SwaggerSpecificationV2] .</span><span class="sxs-lookup"><span data-stu-id="38e25-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="38e25-134">Чтобы включить функцию эксперимента, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить сетевую консоль**.</span><span class="sxs-lookup"><span data-stu-id="38e25-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="38e25-135">Дополнительные сведения о **сетевой консоли**можно найти в разделе [Включение экспериментальной сетевой консоли][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="38e25-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="38e25-136">Этот эксперимент теперь поддерживает описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="38e25-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="38e25-137">Сохранение и экспорт коллекций и сред.</span><span class="sxs-lookup"><span data-stu-id="38e25-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="38e25-138">Изменяйте и экспортируйте наборы переменных среды в инструменте **Network Console** .</span><span class="sxs-lookup"><span data-stu-id="38e25-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="38e25-139">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="38e25-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Введите имя новой среды" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="38e25-141">Введите имя новой среды</span><span class="sxs-lookup"><span data-stu-id="38e25-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Выберите формат для новой среды" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="38e25-143">Выберите формат для новой среды</span><span class="sxs-lookup"><span data-stu-id="38e25-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="38e25-144">Улучшенные инструменты сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38e25-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="38e25-146">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="38e25-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="38e25-147">Microsoft Edge DevTools теперь поддерживает следующие функции для проверки, просмотра и отладки сетки каскадных стилей.</span><span class="sxs-lookup"><span data-stu-id="38e25-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="38e25-148">Отображение упрощенного раскрытия сетки с помощью средства **проверки** или получение более подробных сведений с постоянными наложениями.</span><span class="sxs-lookup"><span data-stu-id="38e25-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="38e25-149">Чтобы включить постоянную наложение сетки, щелкните значок сетки рядом с элементом контейнера сетки в инструменте **элементы** или выберите сетку в инструменте **Макет** .</span><span class="sxs-lookup"><span data-stu-id="38e25-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="38e25-150">Вы можете включить постоянную наложение для нескольких сеток.</span><span class="sxs-lookup"><span data-stu-id="38e25-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="38e25-151">С помощью нового инструмента " **Макет** " можно легко переключать наложения сетки и настраивать внешний вид и содержимое каждого из них.</span><span class="sxs-lookup"><span data-stu-id="38e25-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="38e25-152">Эти функции включены по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38e25-152">The features are turned on by default.</span></span>  <span data-ttu-id="38e25-153">Дополнительные сведения о функциях можно найти в [таблице каскадных таблиц стилей][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="38e25-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="38e25-154">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="38e25-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="38e25-155">Кроме того, группа Microsoft Edge DevTools работает совместно с коллегами по DevTools и Chromiumом для добавления новых функций управления подложкой в DevTools.</span><span class="sxs-lookup"><span data-stu-id="38e25-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="38e25-156">Чтобы получить обновления для средств управления подпадающими ящиками в проекте Open-Source Chromium, перейдите к вопросу [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="38e25-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Инструмент "макет" с сетками" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="38e25-158">Инструмент " **Макет** " с сетками</span><span class="sxs-lookup"><span data-stu-id="38e25-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="38e25-159">Настройка сочетаний клавиш в параметрах</span><span class="sxs-lookup"><span data-stu-id="38e25-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="38e25-161">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="38e25-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="38e25-162">Теперь вы можете настроить сочетание клавиш для любого действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="38e25-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="38e25-163">Поскольку Microsoft Edge версии 84, вы можете выбирать из **кода Visual Studio** и **DevTools (по умолчанию)** стандартные наборы сочетаний [клавиш][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="38e25-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="38e25-164">Начиная с Microsoft Edge версии 87, вы можете включить **Редактор сочетаний клавиш включения** экспериментов для дальнейшей [настройки сочетаний клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="38e25-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="38e25-165">Чтобы включить функцию эксперимента, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить редактор сочетаний клавиш**.</span><span class="sxs-lookup"><span data-stu-id="38e25-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="38e25-166">Дополнительные сведения о настройке и редактировании сочетаний клавиш можно найти в статье [включить режим экспериментального редактора сочетаних][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]клавиш.</span><span class="sxs-lookup"><span data-stu-id="38e25-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="38e25-167">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="38e25-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Настраиваемое сочетание клавиш для приостановки сценария" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="38e25-169">Настраиваемое сочетание клавиш для приостановки сценария</span><span class="sxs-lookup"><span data-stu-id="38e25-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="38e25-170">Знакомство с расширением кода Microsoft Edge Tools для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="38e25-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="38e25-171">**Элементы для расширений кода Visual Studio** и **Network для Visual Studio** теперь объединяются в новое расширение [кода средств разработчика Microsoft Edge для Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .</span><span class="sxs-lookup"><span data-stu-id="38e25-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="38e25-172">Используйте Microsoft Edge DevTools для следующих действий, не выходя из кода Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38e25-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="38e25-173">Отладка модели DOM</span><span class="sxs-lookup"><span data-stu-id="38e25-173">Debug the DOM</span></span>  
*   <span data-ttu-id="38e25-174">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="38e25-174">Edit CSS</span></span>  
*   <span data-ttu-id="38e25-175">Проверка сетевого трафика</span><span class="sxs-lookup"><span data-stu-id="38e25-175">Inspect network traffic</span></span>  

<span data-ttu-id="38e25-176">С помощью расширения запустите Microsoft EDGE, подключитесь к существующему экземпляру браузера или используйте браузер без монитора прямо из редактора.</span><span class="sxs-lookup"><span data-stu-id="38e25-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="38e25-177">Чтобы приступить к откликам и разрешению проблем с отзывом об этом расширении, перейдите к разделу [Инструменты разработчика Microsoft Edge для Visual Studio][GithubMicrosoftVscodeEdgeDevtools] в GitHub.</span><span class="sxs-lookup"><span data-stu-id="38e25-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Снимок экрана: использование расширения в полноэкранном режиме браузера" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="38e25-179">Снимок экрана: использование расширения в полноэкранном режиме браузера</span><span class="sxs-lookup"><span data-stu-id="38e25-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Снимок экрана: использование расширения в режиме без монитора" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="38e25-181">Снимок экрана: использование расширения в режиме без монитора</span><span class="sxs-lookup"><span data-stu-id="38e25-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="38e25-182">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="38e25-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="38e25-183">Новое средство WebAuthn</span><span class="sxs-lookup"><span data-stu-id="38e25-183">New WebAuthn tool</span></span>  

<span data-ttu-id="38e25-184">В более ранних версиях Microsoft EDGE не поддерживалась Отладка с родным WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="38e25-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="38e25-185">Необходимы физические средства проверки подлинности для проверки веб-приложения с помощью [API проверки подлинности веб-сайта][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="38e25-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="38e25-186">С помощью нового средства **WebAuthn** вы можете выполнять следующие действия без использования каких – либо физических средств проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="38e25-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="38e25-187">Эмуляция средств проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="38e25-187">Emulate authenticators</span></span>
*   <span data-ttu-id="38e25-188">Настройка атрибутов средств проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="38e25-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="38e25-189">Проверка состояний средств проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="38e25-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="38e25-190">Дополнительные сведения о функции **WebAuthn** можно найти в [разделе Эмуляция проверки подлинности и отладка Webauthn в Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="38e25-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="38e25-191">Вы можете эмулировать средства проверки подлинности и отлаживать [API проверки подлинности веб-сайта][GithubW3cWebauthn] с помощью нового инструмента [WebAuthn][DevtoolsWebauthnIndex] .</span><span class="sxs-lookup"><span data-stu-id="38e25-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="38e25-192">Чтобы открыть средство **WebAuthn** , щелкните значок **Настройка и управление DevTools** \ ( `...` \) > **более средствам**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="38e25-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="38e25-193">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="38e25-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Открытие средства WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="38e25-195">Открытие средства **WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="38e25-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="38e25-197">Средство **WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="38e25-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="38e25-198">Обновление инструмента "элементы"</span><span class="sxs-lookup"><span data-stu-id="38e25-198">Elements tool updates</span></span>  

#### <span data-ttu-id="38e25-199">Просмотр области "вычисляемая боковая панель" в области "стили"</span><span class="sxs-lookup"><span data-stu-id="38e25-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="38e25-200">Переключить **вычисляемую** область на панели **стили** .</span><span class="sxs-lookup"><span data-stu-id="38e25-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="38e25-201">**Вычисляемая** область в области **стили** свернута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38e25-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="38e25-202">Чтобы переключить его, нажмите кнопку.</span><span class="sxs-lookup"><span data-stu-id="38e25-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="38e25-203">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="38e25-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Открытие области "вычисляемая боковая панель"" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="38e25-205">Открытие области " **Вычисляемая боковая** панель"</span><span class="sxs-lookup"><span data-stu-id="38e25-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Вычисляемая область боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="38e25-207">**Вычисляемая область боковой** панели</span><span class="sxs-lookup"><span data-stu-id="38e25-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="38e25-208">Группировка свойств CSS в вычисляемой панели</span><span class="sxs-lookup"><span data-stu-id="38e25-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="38e25-209">Чтобы просмотреть примененную CSS с меньшим прокруткой, сгруппируйте свойства CSS по категориям в **вычисляемой** области.</span><span class="sxs-lookup"><span data-stu-id="38e25-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="38e25-210">Вы также можете выбрать набор связанных свойств при проверке CSS.</span><span class="sxs-lookup"><span data-stu-id="38e25-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="38e25-211">В инструменте **элементы** выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="38e25-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="38e25-212">Чтобы выполнить группировку \ (или разгрупповую) свойства CSS, установите или снимите флажок **Группа** .</span><span class="sxs-lookup"><span data-stu-id="38e25-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="38e25-213">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к разделу проблемы [#1096230][CR1096230], [#1084673][CR1084673]и [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="38e25-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Группировка свойств CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="38e25-215">Группировка свойств CSS</span><span class="sxs-lookup"><span data-stu-id="38e25-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="38e25-216">Lighthouse 6,4 в инструменте Lighthouse</span><span class="sxs-lookup"><span data-stu-id="38e25-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="38e25-217">Средство **Lighthouse** теперь запущено Lighthouse 6,4.</span><span class="sxs-lookup"><span data-stu-id="38e25-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="38e25-218">Чтобы просмотреть полный список изменений, перейдите к [заметкам о выпуске Lighthouse][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="38e25-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="38e25-219">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="38e25-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="38e25-220">события Performance. Mark () в разделе "время показа слайдов"</span><span class="sxs-lookup"><span data-stu-id="38e25-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="38e25-221">**Раздел "временные интервалы** " записи в инструменте " [производительность][DevtoolsGuideChromiumEvaluatePerformanceReference] " теперь отмечает `performance.mark()` события.</span><span class="sxs-lookup"><span data-stu-id="38e25-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="38e25-222">Чтобы попробовать эту функцию и оценить производительность кода JavaScript, добавьте `performance.mark()` события в код.</span><span class="sxs-lookup"><span data-stu-id="38e25-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="38e25-223">Например, в приведенном ниже фрагменте кода добавляются маркеры до и после `for` цикла, который выполняет итерацию от 0 до 1000 с шагом 7.</span><span class="sxs-lookup"><span data-stu-id="38e25-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="38e25-224">Затем откройте средство " [производительность][DevtoolsGuideChromiumEvaluatePerformanceReference] " и перейдите к **разделу временные показатели** для записи кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="38e25-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="38e25-225">`performance.mark()`Добавленные события будут отображены в записи.</span><span class="sxs-lookup"><span data-stu-id="38e25-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Событие Performance. Mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="38e25-227">событиях</span><span class="sxs-lookup"><span data-stu-id="38e25-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="38e25-228">Новые фильтры типа ресурсов и URL-адреса в инструменте "сеть"</span><span class="sxs-lookup"><span data-stu-id="38e25-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="38e25-229">Используйте новые `resource-type` `url` Ключевые слова в инструменте " **сеть** " для фильтрации сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="38e25-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="38e25-230">Например, вы можете `resource-type:image` сосредоточиться на сетевых запросах, которые являются изображениями.</span><span class="sxs-lookup"><span data-stu-id="38e25-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Фильтр по типу ресурсов" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="38e25-232">Фильтр по типу ресурсов</span><span class="sxs-lookup"><span data-stu-id="38e25-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="38e25-233">Чтобы найти другие специальные ключевые слова, такие как `resource-type` и `url` , перейдите в [раздел запросы фильтра по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="38e25-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="38e25-234">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к разделу проблемы [#1121141][CR1121141] и [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="38e25-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="38e25-235">Обновления представления "сведения о кадрах"</span><span class="sxs-lookup"><span data-stu-id="38e25-235">Frame details view updates</span></span>  

#### <span data-ttu-id="38e25-236">Отображение отчетов COEP и COOP в конечную точку</span><span class="sxs-lookup"><span data-stu-id="38e25-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="38e25-237">`reporting to`В разделе " **изоляция &** " перейдите на вкладку "политика встроенного внедрения" \ (COEP \) и межисточниковая политика OPENER \ (Coop \).</span><span class="sxs-lookup"><span data-stu-id="38e25-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="38e25-238">[API отчетов][MdnReportingApi] определяет `Report-To` новый заголовок HTTP, который позволяет указать конечные точки сервера для браузера, чтобы отправлять предупреждения и ошибки.</span><span class="sxs-lookup"><span data-stu-id="38e25-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="38e25-239">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="38e25-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Отправка сообщения конечной точке" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="38e25-241">`reporting to`Конечная точка</span><span class="sxs-lookup"><span data-stu-id="38e25-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="38e25-242">Отображение COEP и COOP режима "только отчет"</span><span class="sxs-lookup"><span data-stu-id="38e25-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="38e25-243">DevTools теперь отобразите `report-only` метку для COEP и Coop, которые установлены в `report-only` режим.</span><span class="sxs-lookup"><span data-stu-id="38e25-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="38e25-244">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="38e25-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Метка режима «только отчет»" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="38e25-246">`report-only`Метка "режим"</span><span class="sxs-lookup"><span data-stu-id="38e25-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="38e25-247">Просмотр и устранение проблем с контрастностью цвета в инструменте "Общие сведения о CSS"</span><span class="sxs-lookup"><span data-stu-id="38e25-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="38e25-249">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="38e25-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="38e25-250">В инструменте " **Обзор CSS** " теперь отображается список элементов на странице с проблемами цветовой контрастности.</span><span class="sxs-lookup"><span data-stu-id="38e25-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="38e25-251">На приведенной ниже демонстрационной странице показан пример ошибки цветовой контрастности.</span><span class="sxs-lookup"><span data-stu-id="38e25-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="38e25-252">Обзор CSS: демонстрация доступных цветов</span><span class="sxs-lookup"><span data-stu-id="38e25-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="38e25-253">Чтобы включить этот эксперимент, в **Settings**разделе  >  **эксперименты**с параметрами установите флажок **CSS Overview (обзор** ).</span><span class="sxs-lookup"><span data-stu-id="38e25-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="38e25-254">Чтобы просмотреть список элементов с проблемой цветовой контрастности, в **вопросах контрастности**выберите **текст**.</span><span class="sxs-lookup"><span data-stu-id="38e25-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="38e25-255">Чтобы открыть элемент в инструменте **элементы** , выберите элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="38e25-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="38e25-256">Для устранения проблем с контрастностью Microsoft Edge DevTools [автоматически предлагают варианты цветов][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span><span class="sxs-lookup"><span data-stu-id="38e25-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="38e25-257">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="38e25-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Проблемы с низким контрастом цвета" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="38e25-259">Проблемы с низким контрастом цвета</span><span class="sxs-lookup"><span data-stu-id="38e25-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="38e25-260">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38e25-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="38e25-261">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="38e25-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="38e25-262">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="38e25-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="38e25-263">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="38e25-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Устаревшая область свойств в инструменте "элементы" — новые возможности DevTools (Microsoft Edge 84) | Документы Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS: новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Специальные возможности цвета в области "стили" — новые возможности DevTools (Microsoft Edge 86) | Документы Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript: Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справка по анализу производительности | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включите экспериментальные API — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор сочетаний клавиш — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Включить сетевую консоль — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включение средства просмотра заказов на исходный номер — экспериментальные функции | Документы Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складная и устройствах с двумя экранами — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Справочник по API для консоли "Таблица" | Документы Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Проверка сетки CSS | Документы Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" — Справка по анализу производительности | Документы Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отладка сведений о проигрывателях мультимедиа | Документы Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Инструменты Microsoft Edge для Visual Studio, код | Код Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR1034663]: https://crbug.com/1034663 "Создание передней части API тестирования WebAuthn | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS/гибкая таблица/подсказка для таблиц | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "вычисляемый стиль" исчезает в режиме отклика | Ошибки Chromium"  
[CR1075732]: https://crbug.com/1075732 "Персонализация DevTools — незакрепленные вкладки | Ошибки Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Улучшите способ представления настраиваемых свойств CSS ((то есть). Переменные CSS) и их значения | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Инструмент "создать" для создания и воспроизведения запросов виртуальных сетей | Ошибки Chromium"  
[CR1096230]: https://crbug.com/1096230 "Группировка свойств CSS по категориям в области «Вычисляемые стили» | Ошибки Chromium"  
[CR1104188]: https://crbug.com/1104188 "При поиске полного URL-адреса в средстве поиска в сети не удается найти результаты. Ошибки Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: улучшение вкладки "вычисляемые стили" | Ошибки Chromium"  
[CR1120316]: https://crbug.com/1120316 "Выделение неправильной контрастности в разделе Общие сведения о CSS > цвета | Ошибки Chromium"  
[CR1121141]: https://crbug.com/1121141 "Разрешать фильтрацию по типу ресурсов в сетевом журнале | Ошибки Chromium"  
[CR1121312]: https://crbug.com/1121312 "Параметры должны быть удалены из меню "другие инструменты" | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Инструмент "Подсказка" | Ошибки Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools: локализация v2 | Ошибки Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API отчетов | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-проверка подлинности | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Здравствуйте! | Цепь"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Опубликовать формат коллекции v 2.1.0 | Опубликовать"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Спецификация OpenAPI | Машин"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="38e25-316">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38e25-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="38e25-317">Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/10/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="38e25-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="38e25-319">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38e25-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  