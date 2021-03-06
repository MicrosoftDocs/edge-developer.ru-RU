---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398681"
---
# <a name="experimental-features"></a><span data-ttu-id="3b48c-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3b48c-104">Experimental features</span></span>  

<span data-ttu-id="3b48c-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="3b48c-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="3b48c-106">Вы можете протестировать и [предоставить обратную связь](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.</span><span class="sxs-lookup"><span data-stu-id="3b48c-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="3b48c-107">В то время как экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="3b48c-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="3b48c-108">Включаем экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3b48c-108">Turn on experimental features</span></span>  

<span data-ttu-id="3b48c-109">Чтобы включить экспериментальные функции \(или off\) в Microsoft Edge, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-110">[Откройте DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="3b48c-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="3b48c-111">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="3b48c-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="3b48c-112">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="3b48c-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="3b48c-113">Откройте области [Параметры.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="3b48c-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="3b48c-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="3b48c-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="3b48c-115">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="3b48c-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="3b48c-116">На левой стороне области **Параметры** выберите раздел **Эксперименты.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница Эксперименты в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="3b48c-118">Страница **Эксперименты** в **параметрах**</span><span class="sxs-lookup"><span data-stu-id="3b48c-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b48c-119">На странице **Эксперименты** прокрутите список всех доступных экспериментальных функций и выберите почтовый ящик рядом с каждой функцией, которую необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="3b48c-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="3b48c-120">Закрыть и открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="3b48c-121">Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="3b48c-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="3b48c-122">Чтобы отключить экспериментальную функцию, откройте страницу **Эксперименты** и закройте контрольный ящик экспериментальной функции, которую необходимо отключить.</span><span class="sxs-lookup"><span data-stu-id="3b48c-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="3b48c-123">Основные экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3b48c-123">Highlighted experimental features</span></span>  

<span data-ttu-id="3b48c-124">В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b48c-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="3b48c-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3b48c-125">Experimental feature</span></span> | <span data-ttu-id="3b48c-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3b48c-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="3b48c-127">Включить веб-хинт</span><span class="sxs-lookup"><span data-stu-id="3b48c-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="3b48c-128">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-128">85 or later</span></span> |  
| [<span data-ttu-id="3b48c-129">Включить консоль сети</span><span class="sxs-lookup"><span data-stu-id="3b48c-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="3b48c-130">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-130">85 or later</span></span> |  
| [<span data-ttu-id="3b48c-131">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="3b48c-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="3b48c-132">86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-132">86 or later</span></span> |  
| [<span data-ttu-id="3b48c-133">Включить редактор ярлыка клавиатуры</span><span class="sxs-lookup"><span data-stu-id="3b48c-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="3b48c-134">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-134">87 or later</span></span> |  
| [<span data-ttu-id="3b48c-135">Включить композитные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="3b48c-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="3b48c-136">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-136">87 or later</span></span> |  
| [<span data-ttu-id="3b48c-137">Включить новый инструмент редактора шрифта в области Стилей</span><span class="sxs-lookup"><span data-stu-id="3b48c-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="3b48c-138">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-138">89 or later</span></span> |  
| [<span data-ttu-id="3b48c-139">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="3b48c-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="3b48c-140">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-140">89 or later</span></span> |  
| [<span data-ttu-id="3b48c-141">Включить меню вкладок + кнопки, чтобы открыть дополнительные средства</span><span class="sxs-lookup"><span data-stu-id="3b48c-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="3b48c-142">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-142">89 or later</span></span> |  
| [<span data-ttu-id="3b48c-143">Включить вкладку Welcome</span><span class="sxs-lookup"><span data-stu-id="3b48c-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="3b48c-144">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="3b48c-144">89 or later</span></span> |  

### <a name="enable-new-css-grid-debugging-features"></a><span data-ttu-id="3b48c-145">Включить новые функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="3b48c-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="3b48c-146">Эта экспериментальная функция предоставляет ряд новых визуализаций, которые помогут отламыть макеты сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="3b48c-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="3b48c-147">Чтобы просмотреть последние экспериментальные функции, в этом [эксперименте необходимо](#turn-on-experimental-features) включить и перезагрузить DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="3b48c-148">Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a><span data-ttu-id="3b48c-149">Просмотр нависайки сетки с помощью средства Inspect</span><span class="sxs-lookup"><span data-stu-id="3b48c-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="3b48c-150">Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Grid на веб-сайте, нависая над ними с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="3b48c-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="3b48c-151">Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="3b48c-152">Затем наведите курсор `Grid` на элемент на отладке веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3b48c-152">Then, hover on a `Grid` element on the webpage you are debugging.</span></span>  <span data-ttu-id="3b48c-153">Контуры отображаются вокруг сетки, а штриховка указывает расположение пробелов сетки, если она присутствует.</span><span class="sxs-lookup"><span data-stu-id="3b48c-153">Outlines are displayed around the grid, and hatching indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Просмотр сетки с помощью средства Inspect" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="3b48c-155">Просмотр сетки с помощью **средства Inspect**</span><span class="sxs-lookup"><span data-stu-id="3b48c-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a><span data-ttu-id="3b48c-156">Просмотр настойчивых накладок сетки</span><span class="sxs-lookup"><span data-stu-id="3b48c-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="3b48c-157">В версии Microsoft Edge 86 или более поздней версии экспериментальная функция сетки CSS также предлагает возможность включить постоянные наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="3b48c-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="3b48c-158">Постоянные наложения предоставляют несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="3b48c-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="3b48c-159">Постоянные наложения остаются видимыми на странице при прокрутке, движении мыши и использовании других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="3b48c-160">Одновременно может быть включено несколько постоянных накладок, что позволяет просмотреть несколько макетов сетки одновременно.</span><span class="sxs-lookup"><span data-stu-id="3b48c-160">Multiple persistent overlays may be turned on at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="3b48c-161">Постоянные наложения предлагают множество вариантов конфигурации, таких как сокрытие или отображение имен в области сетки, пробелы в сетке, размеры трассы и так далее.</span><span class="sxs-lookup"><span data-stu-id="3b48c-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="3b48c-162">Два способа для наложения на настойчивые сетки.</span><span class="sxs-lookup"><span data-stu-id="3b48c-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="3b48c-163">Выберите **значок овал** Grid рядом с любым элементом Grid, показанным в дереве DOM **средства Elements.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Значок Grid oval в инструменте Elements" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="3b48c-165">Значок Grid oval в **инструменте Elements**</span><span class="sxs-lookup"><span data-stu-id="3b48c-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="3b48c-166">Откройте новую панель **Макета,** расположенную в средстве Elements, и выберите контрольный ящик рядом с каждым элементом Grid, который необходимо выделить.</span><span class="sxs-lookup"><span data-stu-id="3b48c-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="3b48c-168">**Панель макета** в DevTools</span><span class="sxs-lookup"><span data-stu-id="3b48c-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a><span data-ttu-id="3b48c-169">Настройка постоянных накладок</span><span class="sxs-lookup"><span data-stu-id="3b48c-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="3b48c-170">В microsoft Edge версии 86 или более поздней версии новая панель \*\*\*\* **Layout** расположена в инструменте **Elements** наряду со стилями и **вычислительными** панелями.</span><span class="sxs-lookup"><span data-stu-id="3b48c-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** panels.</span></span>  <span data-ttu-id="3b48c-171">Панель **Макета** позволяет параметров конфигурации для настойчивых наложения.</span><span class="sxs-lookup"><span data-stu-id="3b48c-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Функция отладки сетки CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="3b48c-173">Функция отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="3b48c-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a><span data-ttu-id="3b48c-174">Включить поддержку для перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="3b48c-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="3b48c-175">Обычно такие средства, как **Elements** и **Network,** могут открываться только в основной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="3b48c-176">Такие **инструменты, как 3D View** и **Issues,** которые обычно открываются только в панели **ящиков,** расположенных в нижней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="3b48c-177">После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="3b48c-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="3b48c-178">Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Переместить** вверх или **Переместить в нижнее**.</span><span class="sxs-lookup"><span data-stu-id="3b48c-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="3b48c-179">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="3b48c-180">Чтобы отобразить или скрыть панель **ящиков,** выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="3b48c-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение инструментов между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="3b48c-182">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="3b48c-182">Moving tools between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a><span data-ttu-id="3b48c-183">Включить веб-хинт</span><span class="sxs-lookup"><span data-stu-id="3b48c-183">Enable webhint</span></span>  

<span data-ttu-id="3b48c-184">[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="3b48c-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="3b48c-185">Тип обратной связи, предоставляемый [веб-сайтом][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="3b48c-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="3b48c-186">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="3b48c-186">accessibility</span></span>  
*   <span data-ttu-id="3b48c-187">совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="3b48c-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="3b48c-188">безопасность"</span><span class="sxs-lookup"><span data-stu-id="3b48c-188">security</span></span>  
*   <span data-ttu-id="3b48c-189">производительность</span><span class="sxs-lookup"><span data-stu-id="3b48c-189">performance</span></span>  
*   <span data-ttu-id="3b48c-190">Прогрессивные веб-приложения (PWAs)</span><span class="sxs-lookup"><span data-stu-id="3b48c-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="3b48c-191">другие распространенные проблемы веб-разработки</span><span class="sxs-lookup"><span data-stu-id="3b48c-191">other common web development issues</span></span>  
    
<span data-ttu-id="3b48c-192">Эксперимент [webhint][WebhintMain] отображает обратную связь веб-хинта в панели [Issues.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="3b48c-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="3b48c-193">Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="3b48c-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="3b48c-194">Выберите ссылку на ресурс, чтобы открыть **соответствующую**сеть, **источники**или **элементов** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="3b48c-196">webhint feedback in the **Issues** panel</span><span class="sxs-lookup"><span data-stu-id="3b48c-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="3b48c-197">Включить консоль сети</span><span class="sxs-lookup"><span data-stu-id="3b48c-197">Enable Network Console</span></span>  

<span data-ttu-id="3b48c-198">**Network Console** — это рабочее название эксперимента по синтетическому запросу сети по HTTP.</span><span class="sxs-lookup"><span data-stu-id="3b48c-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="3b48c-199">Вы можете использовать эксперимент **сетевой консоли** для отправки запросов веб-API.</span><span class="sxs-lookup"><span data-stu-id="3b48c-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="3b48c-200">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3b48c-201">Для использования **сетевой консоли**выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-202">Откройте **области Сети.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="3b48c-203">Найдите сетевой запрос, который необходимо изменить и повторно изменить.</span><span class="sxs-lookup"><span data-stu-id="3b48c-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="3b48c-204">Откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.</span><span class="sxs-lookup"><span data-stu-id="3b48c-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="3b48c-205">При **открываемой сетевой** консоли отредактируете сведения о запросе сети.</span><span class="sxs-lookup"><span data-stu-id="3b48c-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="3b48c-206">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3b48c-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Консоль сети в ящике консоли" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="3b48c-208">**Консоль сети** в **ящике консоли**</span><span class="sxs-lookup"><span data-stu-id="3b48c-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="3b48c-209">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="3b48c-209">Source Order Viewer</span></span>  

<span data-ttu-id="3b48c-210">**Source Order Viewer** — это эксперимент, который отображает порядок элементов в источнике веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3b48c-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="3b48c-211">Порядок отображения на экране может отличаться от порядка источника, что сбивает с толку читателя экрана и пользователей клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3b48c-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="3b48c-212">Чтобы **найти** различия между порядком отображения на экране и порядком источника, используйте эксперимент по просмотру исходных порядков.</span><span class="sxs-lookup"><span data-stu-id="3b48c-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="3b48c-213">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3b48c-214">Чтобы использовать **viewer source order,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-215">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="3b48c-216">Откройте панель **доступности** в панели ящика \(bottom\) .</span><span class="sxs-lookup"><span data-stu-id="3b48c-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="3b48c-217">В разделе **Просмотр источника порядка** выберите почтовый ящик Показать **исходный** порядок.</span><span class="sxs-lookup"><span data-stu-id="3b48c-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="3b48c-218">Выделение любого элемента HTML для отображения наложения, указываемой на источник веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3b48c-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Для просмотра исходных заказов в области доступности" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="3b48c-220">**Для просмотра исходных заказов** в **области доступности**</span><span class="sxs-lookup"><span data-stu-id="3b48c-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a><span data-ttu-id="3b48c-221">Включить редактор ярлыка клавиатуры</span><span class="sxs-lookup"><span data-stu-id="3b48c-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="3b48c-222">С **включенным экспериментом редактора** ярлыков включить клавиши включить, вы можете настроить ярлыки клавиатуры для любого действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="3b48c-223">Чтобы настроить ярлык клавиатуры для определенного действия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-224">[Откройте DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="3b48c-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="3b48c-225">Open [Settings][DevToolsCustomizeIndexSettings].</span><span class="sxs-lookup"><span data-stu-id="3b48c-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="3b48c-226">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="3b48c-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="3b48c-227">Перейдите на **страницу Ярлыки.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="3b48c-228">Выберите действие, необходимое для настройки.</span><span class="sxs-lookup"><span data-stu-id="3b48c-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="3b48c-229">Выберите **значок Edit** \( ![ EditKeyboardShortcut\). ](../media/edit-keyboard-shortcut-icon.msft.png)</span><span class="sxs-lookup"><span data-stu-id="3b48c-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выберите действие для настройки со страницы Ярлыки в Параметры" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="3b48c-231">Выберите действие для настройки со страницы **Ярлыки** в [Параметры][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="3b48c-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b48c-232">На клавиатуре выберите клавиши для привязки к действию.</span><span class="sxs-lookup"><span data-stu-id="3b48c-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выберите клавиши, которые необходимо назначить действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="3b48c-234">Выберите клавиши, которые необходимо назначить действию</span><span class="sxs-lookup"><span data-stu-id="3b48c-234">Choose the keys you want to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b48c-235">Чтобы сохранить новый ярлык клавиатуры, выберите контрольный знак \(</span><span class="sxs-lookup"><span data-stu-id="3b48c-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="3b48c-237">\) значок.</span><span class="sxs-lookup"><span data-stu-id="3b48c-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Выберите значок контрольных знаков, чтобы сохранить новый ярлык клавиатуры" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="3b48c-239">Выберите значок контрольных знаков, чтобы сохранить новый ярлык клавиатуры</span><span class="sxs-lookup"><span data-stu-id="3b48c-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3b48c-240">Выберите новый ярлык клавиатуры, чтобы вызвать действие в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="3b48c-241">На странице **Ярлыки** значок Custom **Keyboard Shortcut** ![ \( CustomKeyboardShortcut \) отображает настроенные ](../media/custom-keyboard-shortcut-icon.msft.png) клавиши клавиш.</span><span class="sxs-lookup"><span data-stu-id="3b48c-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="3b48c-242">Чтобы сбросить все ярлыки, выберите восстановление ярлыков **по умолчанию.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="3b48c-243">Чтобы отменить изменения при редактировании клавиш для действия, выберите значок X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="3b48c-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="3b48c-244">Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut\). ](../media/delete-keyboard-shortcut-icon.msft.png)</span><span class="sxs-lookup"><span data-stu-id="3b48c-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="3b48c-245">Чтобы добавить несколько ярлыков для действия, выберите **Добавить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="3b48c-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="3b48c-246">Если ярлык клавиатуры в настоящее время назначен другому действию, вы не можете сохранить его для нового действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="3b48c-247">Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.</span><span class="sxs-lookup"><span data-stu-id="3b48c-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="3b48c-248">Включить композитные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="3b48c-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="3b48c-249">Теперь можно визуализировать Слои вместе с индексами z и объектной моделью документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="3b48c-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="3b48c-250">Эта функция позволяет отключить, не переключая контексты так часто.</span><span class="sxs-lookup"><span data-stu-id="3b48c-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="3b48c-251">Вы определили, что уменьшение переключения контекста является основной проблемой.</span><span class="sxs-lookup"><span data-stu-id="3b48c-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="3b48c-252">Не всегда понятно, как код, который вы пишете, влияет на ваше веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="3b48c-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="3b48c-253">Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.</span><span class="sxs-lookup"><span data-stu-id="3b48c-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="3b48c-254">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3b48c-255">Чтобы использовать **композитные слои,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-256">В ящике выберите **средство 3D View.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="3b48c-257">Откройте области **Композитные слои.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="3b48c-258">Отображаются все расписные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="3b48c-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="3b48c-259">Попробуйте эту функцию с помощью собственных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="3b48c-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="3b48c-261">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="3b48c-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="3b48c-262">Включить новый инструмент редактора шрифта в области Стилей</span><span class="sxs-lookup"><span data-stu-id="3b48c-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="3b48c-263">Теперь для редактирования шрифтов можно использовать новый визуальный [редактор][DevtoolsInspectStylesEditFonts] шрифтов.</span><span class="sxs-lookup"><span data-stu-id="3b48c-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="3b48c-264">Используйте его для определения шрифтов и характеристик шрифтов.</span><span class="sxs-lookup"><span data-stu-id="3b48c-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="3b48c-265">Визуальный **редактор шрифта** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="3b48c-266">Переключение между единицами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="3b48c-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="3b48c-267">Переключатель между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="3b48c-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="3b48c-268">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="3b48c-268">Convert units</span></span>  
*   <span data-ttu-id="3b48c-269">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="3b48c-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="3b48c-270">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="3b48c-271">Чтобы использовать новый визуальный **редактор шрифтов,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b48c-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="3b48c-272">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="3b48c-273">Откройте области **стилей.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="3b48c-274">Выберите **значок Редактор шрифта.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="3b48c-275">Дополнительные сведения о новом редакторе визуальных шрифтов **перейдите**к редактированию стилей и параметров шрифта CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="3b48c-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена поле редактора визуальных шрифтов" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="3b48c-277">Выделена поле **редактора** визуальных шрифтов</span><span class="sxs-lookup"><span data-stu-id="3b48c-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="3b48c-278">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="3b48c-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="3b48c-279">Эта экспериментальная функция предоставляет множество новых визуализаций, которые помогут отламыть макеты CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="3b48c-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="3b48c-280">Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="3b48c-281">Отображение постоянных наложения на макеты Flexbox с помощью средства Inspect</span><span class="sxs-lookup"><span data-stu-id="3b48c-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="3b48c-282">Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Flexbox на веб-сайте, зависая на них с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="3b48c-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="3b48c-283">Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="3b48c-284">Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера flex.</span><span class="sxs-lookup"><span data-stu-id="3b48c-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="3b48c-286">Отображение контейнеров Flexbox с помощью средства **Inspect**</span><span class="sxs-lookup"><span data-stu-id="3b48c-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="3b48c-287">Отображение настойчивых наложения на макеты Flexbox</span><span class="sxs-lookup"><span data-stu-id="3b48c-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="3b48c-288">В microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения на макеты Flexbox.</span><span class="sxs-lookup"><span data-stu-id="3b48c-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="3b48c-289">Постоянные наложения предоставляют следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="3b48c-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="3b48c-290">Постоянные наложения остаются видимыми на веб-странице во время прокрутки, перемещения мыши и использования других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="3b48c-291">Одновременно можно использовать несколько настойчивых накладок, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.</span><span class="sxs-lookup"><span data-stu-id="3b48c-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="3b48c-292">Постоянные наложения предлагают параметры цветовой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3b48c-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="3b48c-293">Чтобы отладить постоянные наложения на макет Flexbox, используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="3b48c-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="3b48c-294">Выберите **значок овального** ящика Flexbox рядом с любым контейнером Flexbox, отображаемым в дереве DOM средства **Elements.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="3b48c-295">Откройте новую панель **Макета,** расположенную в средстве **Elements,** и выберите контрольный ящик рядом с каждым контейнером Flexbox, который необходимо выделить.</span><span class="sxs-lookup"><span data-stu-id="3b48c-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex icons and Layout panel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="3b48c-297">Flex icons and **Layout** panel in DevTools</span><span class="sxs-lookup"><span data-stu-id="3b48c-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="3b48c-298">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="3b48c-298">Configure persistent overlays</span></span>  

<span data-ttu-id="3b48c-299">Чтобы настроить параметры для настойчивых накладок для сетки CSS или макетов Flexbox, используйте **области макета.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="3b48c-300">Области **макета** расположен в **инструменте Elements** рядом со **стилями** и **вычислительными** стемнами.</span><span class="sxs-lookup"><span data-stu-id="3b48c-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="3b48c-302">Панель макета</span><span class="sxs-lookup"><span data-stu-id="3b48c-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="3b48c-303">Включить меню вкладок + кнопки, чтобы открыть дополнительные средства</span><span class="sxs-lookup"><span data-stu-id="3b48c-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="3b48c-304">Теперь можно открыть дополнительные средства с помощью нового значка **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="3b48c-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="3b48c-305">После включения меню вкладок **Включить +** кнопки, чтобы открыть дополнительные средства эксперимента и перезагрузить DevTools, плюс знак \( \) отображает справа от группы вкладок в верхней части `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="3b48c-306">Чтобы отобразить список других средств, которые можно добавить в вкладку, выберите значок **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="3b48c-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="3b48c-308">**Дополнительные средства** в верхней области</span><span class="sxs-lookup"><span data-stu-id="3b48c-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="3b48c-309">Включить средство Welcome</span><span class="sxs-lookup"><span data-stu-id="3b48c-309">Enable Welcome tool</span></span>

<span data-ttu-id="3b48c-310">Этот эксперимент заменяет средство **What's New** новым средством **Welcome.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="3b48c-311">Он отображает обновленный дизайн для следующего контента.</span><span class="sxs-lookup"><span data-stu-id="3b48c-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="3b48c-312">Ссылки на документы разработчика</span><span class="sxs-lookup"><span data-stu-id="3b48c-312">Links to developer docs</span></span>  
*   <span data-ttu-id="3b48c-313">последние функции</span><span class="sxs-lookup"><span data-stu-id="3b48c-313">the latest features</span></span>  
*   <span data-ttu-id="3b48c-314">заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="3b48c-314">release notes</span></span>  
*   <span data-ttu-id="3b48c-315">Возможность связаться с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b48c-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="3b48c-316">Средство **Welcome** автоматически открывается после каждого обновления microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3b48c-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="3b48c-317">Чтобы предотвратить отображение средства **Welcome** после каждого обновления, закройте почтовый ящик рядом с вкладками **Open** после каждого обновления под заголовком **Welcome** tool.</span><span class="sxs-lookup"><span data-stu-id="3b48c-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="3b48c-318">Если вы предпочитаете оригинальный инструмент **What's New,** перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и удалите почтовый ящик рядом со вкладками  >  \*\*\*\* **Enable Welcome.**</span><span class="sxs-lookup"><span data-stu-id="3b48c-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство welcome" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="3b48c-320">**Средство welcome**</span><span class="sxs-lookup"><span data-stu-id="3b48c-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="3b48c-321">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="3b48c-321">Previous experimental features</span></span>  

*   <span data-ttu-id="3b48c-322">[3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в microsoft Edge версии 83 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="3b48c-323">[Включив поддержку, чтобы][DevtoolsMoveTabs] переместить вкладки между панелями, теперь доступна и включена по умолчанию в microsoft Edge версии 85 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="3b48c-324">[Настройка ярлыков клавиатуры][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="3b48c-325">[Эмуляция. Поддержка режима двойного экрана][DevtoolsDeviceModeDualScreenAndFoldables] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="3b48c-326">[Включив новые функции отладки сетки CSS,][DevtoolsCssGrid] теперь доступны и включены по умолчанию в версии Microsoft Edge 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="3b48c-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="3b48c-327">Предоставление отзывов по экспериментальным функциям</span><span class="sxs-lookup"><span data-stu-id="3b48c-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="3b48c-328">Предоставление отзывов об экспериментах Microsoft Edge DevTools или о чем-либо другом, связанном с DevTools.</span><span class="sxs-lookup"><span data-stu-id="3b48c-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="3b48c-329">Отправка отзывов с помощью **значка Отправка отзывов** в DevTools</span><span class="sxs-lookup"><span data-stu-id="3b48c-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="3b48c-330">Чирикать [в @EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="3b48c-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="3b48c-332">Значок **Отправка отзывов** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3b48c-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверьте сетку CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsMoveTabs]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface Duo | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Используйте эмулятор Surface Duo | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Удаленные клиенты настольных | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy Fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмулировать устройства с двойным экраном и складными устройствами в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
