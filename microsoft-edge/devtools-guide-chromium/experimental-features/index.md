---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: 32eaa3e8d41efefa669142297891e7c62cf4eb5b
ms.sourcegitcommit: d53421b7219ad87fa9d58f601d9c61ee44c2e43a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313467"
---
# <span data-ttu-id="69c18-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="69c18-104">Experimental features</span></span>  

<span data-ttu-id="69c18-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="69c18-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="69c18-106">Вы можете протестировать и [предоставить отзыв](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.</span><span class="sxs-lookup"><span data-stu-id="69c18-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="69c18-107">Хотя экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="69c18-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="69c18-108">Включить экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="69c18-108">Turn on experimental features</span></span>  

<span data-ttu-id="69c18-109">Чтобы включить экспериментальную функцию \(или off\) в Microsoft Edge, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-110">[Откройте DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="69c18-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="69c18-111">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="69c18-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="69c18-112">Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="69c18-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="69c18-113">Откройте области ["Параметры".][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="69c18-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="69c18-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="69c18-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="69c18-115">Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="69c18-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="69c18-116">В левой части **области** "Параметры" выберите раздел **"Эксперименты".**</span><span class="sxs-lookup"><span data-stu-id="69c18-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница "Эксперименты" в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="69c18-118">Страница **"Эксперименты"** в **параметрах**</span><span class="sxs-lookup"><span data-stu-id="69c18-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c18-119">На странице **"Эксперименты"** прокрутите список всех доступных экспериментальных функций и выберите этот элемент рядом с каждой функцией, которую нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="69c18-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="69c18-120">Закроют и снова откроете Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="69c18-121">Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="69c18-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="69c18-122">Чтобы отключить экспериментальную функцию, откройте страницу **"Эксперименты"** и скройте контрольный элемент экспериментальной функции, которую нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="69c18-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="69c18-123">Основные экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="69c18-123">Highlighted experimental features</span></span>  

<span data-ttu-id="69c18-124">В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69c18-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="69c18-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="69c18-125">Experimental feature</span></span> | <span data-ttu-id="69c18-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69c18-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="69c18-127">Включить веб-вехин</span><span class="sxs-lookup"><span data-stu-id="69c18-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="69c18-128">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-128">85 or later</span></span> |  
| [<span data-ttu-id="69c18-129">Включить сетевую консоль</span><span class="sxs-lookup"><span data-stu-id="69c18-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="69c18-130">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-130">85 or later</span></span> |  
| [<span data-ttu-id="69c18-131">Просмотр исходных заказов</span><span class="sxs-lookup"><span data-stu-id="69c18-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="69c18-132">86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-132">86 or later</span></span> |  
| [<span data-ttu-id="69c18-133">Включить редактор сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="69c18-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="69c18-134">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-134">87 or later</span></span> |  
| [<span data-ttu-id="69c18-135">Включить составные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="69c18-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="69c18-136">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-136">87 or later</span></span> |  
| [<span data-ttu-id="69c18-137">Включить новое средство редактора шрифтов в области стилей</span><span class="sxs-lookup"><span data-stu-id="69c18-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="69c18-138">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-138">89 or later</span></span> |  
| [<span data-ttu-id="69c18-139">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="69c18-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="69c18-140">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-140">89 or later</span></span> |  
| [<span data-ttu-id="69c18-141">Включить меню вкладок "+кнопка", чтобы открыть дополнительные инструменты</span><span class="sxs-lookup"><span data-stu-id="69c18-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="69c18-142">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-142">89 or later</span></span> |  
| [<span data-ttu-id="69c18-143">Вкладка "Включить приветствие"</span><span class="sxs-lookup"><span data-stu-id="69c18-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="69c18-144">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="69c18-144">89 or later</span></span> |  

### <span data-ttu-id="69c18-145">Включить новые функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="69c18-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="69c18-146">Эта экспериментальная функция предоставляет ряд новых визуализаций для отлаки макетов сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="69c18-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="69c18-147">Чтобы просмотреть последние экспериментальные функции, в [этом эксперименте](#turn-on-experimental-features) необходимо включить и перезагрузить DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="69c18-148">Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="69c18-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="69c18-149">Просмотр наложения сетки при наведении с помощью средства inspect</span><span class="sxs-lookup"><span data-stu-id="69c18-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="69c18-150">Средство **Inspect** позволяет быстро определять и визуализировать макеты сетки CSS на веб-сайте, наведении на них указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="69c18-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="69c18-151">Choose the **Inspect** \( ![ Inspect ](../media/inspect-icon.msft.png) \) icon in the top-left corner of DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="69c18-152">Затем наведите курсор на элемент Grid на веб-сайте, который вы отладили.</span><span class="sxs-lookup"><span data-stu-id="69c18-152">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="69c18-153">Контуры отображаются вокруг сетки, а затенение указывает расположение разрывов сетки, если они присутствуют.</span><span class="sxs-lookup"><span data-stu-id="69c18-153">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Просмотр сеток с помощью средства inspect" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="69c18-155">Просмотр сеток с помощью **средства inspect**</span><span class="sxs-lookup"><span data-stu-id="69c18-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="69c18-156">Просмотр наложения сохраняемой сетки</span><span class="sxs-lookup"><span data-stu-id="69c18-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="69c18-157">В Microsoft Edge версии 86 или более поздней версии экспериментальная функция сетки CSS также предлагает возможность включить постоянные наложения Grid.</span><span class="sxs-lookup"><span data-stu-id="69c18-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="69c18-158">Постоянные наложения предоставляют ряд преимуществ.</span><span class="sxs-lookup"><span data-stu-id="69c18-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="69c18-159">Постоянные наложения остаются видимыми на странице при прокрутке, движении мыши и использовании других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="69c18-160">Одновременно можно включить несколько постоянных наложения, что позволяет просмотреть несколько макетов сетки одновременно.</span><span class="sxs-lookup"><span data-stu-id="69c18-160">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="69c18-161">Постоянные наложения предоставляют множество параметров конфигурации, таких как скрытие или отображение имен в области сетки, разрывы сетки, отслеживание размеров и так далее.</span><span class="sxs-lookup"><span data-stu-id="69c18-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="69c18-162">Два способа переналожения сохраняемой сетки.</span><span class="sxs-lookup"><span data-stu-id="69c18-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="69c18-163">Выберите **значок** овала Grid рядом с любым элементом Grid, показанным в дереве DOM **средства "Элементы".**</span><span class="sxs-lookup"><span data-stu-id="69c18-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Значок овала сетки в средстве "Элементы"" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="69c18-165">Значок овала сетки в **средстве "Элементы"**</span><span class="sxs-lookup"><span data-stu-id="69c18-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="69c18-166">Откройте новую панель **макета,** расположенную в средстве "Элементы", и выберите этот элемент рядом с каждым элементом Grid, который нужно выделить.</span><span class="sxs-lookup"><span data-stu-id="69c18-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="69c18-168">**Панель** макета в DevTools</span><span class="sxs-lookup"><span data-stu-id="69c18-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="69c18-169">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="69c18-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="69c18-170">В Microsoft Edge версии 86 \*\*\*\* или более поздней версии новая панель \*\*\*\* макета расположена в средстве **"Элементы"** вместе со вкладками "Стили" и **"Вычисленные".**</span><span class="sxs-lookup"><span data-stu-id="69c18-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="69c18-171">Панель **макета** позволяет параметров конфигурации для постоянных наложения.</span><span class="sxs-lookup"><span data-stu-id="69c18-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Функция отладки сетки CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="69c18-173">Функция отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="69c18-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="69c18-174">Поддержка перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="69c18-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="69c18-175">Обычно такие средства, как \*\*\*\* **"Элементы"** и "Сеть", могут открываться только на главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="69c18-176">Такие **средства, как трехмерный** просмотр и проблемы, которые обычно открываются только на панели "Drawer", расположенной в нижней части DevTools. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="69c18-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="69c18-177">После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="69c18-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="69c18-178">Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить** в верхнюю" или "Переместить **в нижнюю часть".**</span><span class="sxs-lookup"><span data-stu-id="69c18-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="69c18-179">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="69c18-180">Чтобы отобразить или скрыть **панель "Drawer",** выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="69c18-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="69c18-182">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="69c18-182">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="69c18-183">Включить веб-вехин</span><span class="sxs-lookup"><span data-stu-id="69c18-183">Enable webhint</span></span>  

<span data-ttu-id="69c18-184">[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="69c18-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="69c18-185">Тип обратной связи, предоставленный [веб-hint.][WebhintMain]</span><span class="sxs-lookup"><span data-stu-id="69c18-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="69c18-186">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="69c18-186">accessibility</span></span>  
*   <span data-ttu-id="69c18-187">совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="69c18-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="69c18-188">безопасность"</span><span class="sxs-lookup"><span data-stu-id="69c18-188">security</span></span>  
*   <span data-ttu-id="69c18-189">производительность</span><span class="sxs-lookup"><span data-stu-id="69c18-189">performance</span></span>  
*   <span data-ttu-id="69c18-190">Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="69c18-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="69c18-191">другие распространенные проблемы веб-разработки</span><span class="sxs-lookup"><span data-stu-id="69c18-191">other common web development issues</span></span>  
    
<span data-ttu-id="69c18-192">В [эксперименте webhint][WebhintMain] на панели вопросов отображается обратная связь веб-вехи. [][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="69c18-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="69c18-193">Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="69c18-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="69c18-194">Выберите ссылку на ресурс, чтобы открыть \*\*\*\* соответствующую **области** **"Сеть",**"Источники" или "Элементы" в DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="обратная связь веб-панелей на панели "Проблемы"" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="69c18-196">обратная связь веб-панелей на **панели "Проблемы"**</span><span class="sxs-lookup"><span data-stu-id="69c18-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="69c18-197">Включить сетевую консоль</span><span class="sxs-lookup"><span data-stu-id="69c18-197">Enable Network Console</span></span>  

<span data-ttu-id="69c18-198">**Сетовая** консоль — это рабочий заголовок эксперимента по запросам искусственных сетей по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="69c18-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="69c18-199">Вы можете использовать эксперимент **с сетевой** консолью для отправки запросов веб-API.</span><span class="sxs-lookup"><span data-stu-id="69c18-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="69c18-200">После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="69c18-201">Чтобы использовать **сетевую консоль,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-202">Откройте **сетевую** области.</span><span class="sxs-lookup"><span data-stu-id="69c18-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="69c18-203">Найдите сетевой запрос, который вы хотите изменить, и повторно.</span><span class="sxs-lookup"><span data-stu-id="69c18-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="69c18-204">Откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Изменить **и повторить".**</span><span class="sxs-lookup"><span data-stu-id="69c18-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="69c18-205">Когда **откроется сетовая консоль,** отредактируете сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="69c18-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="69c18-206">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="69c18-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Сетовая консоль в консоли" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="69c18-208">**Сетовая** консоль в **консоли**</span><span class="sxs-lookup"><span data-stu-id="69c18-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="69c18-209">Просмотр исходных заказов</span><span class="sxs-lookup"><span data-stu-id="69c18-209">Source Order Viewer</span></span>  

<span data-ttu-id="69c18-210">**"Просмотр порядка источника"** — это эксперимент, который отображает порядок элементов в источнике веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="69c18-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="69c18-211">Порядок отображения на экране может отличаться от порядка источника, что приводит к путанице для чтения с экрана и пользователей клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="69c18-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="69c18-212">Используйте эксперимент **"Просмотр порядка источника",** чтобы найти различия между порядком отображения на экране и порядком источника.</span><span class="sxs-lookup"><span data-stu-id="69c18-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="69c18-213">После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="69c18-214">Чтобы использовать **"Просмотр порядка источника",** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-215">Откройте средство **"Элементы".**</span><span class="sxs-lookup"><span data-stu-id="69c18-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="69c18-216">Откройте панель **"Accessibility"** (Доступность) на панели "Drawer \(bottom\)".</span><span class="sxs-lookup"><span data-stu-id="69c18-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="69c18-217">В разделе **"Просмотр порядка источника"** выберите **"Показать** порядок источника".</span><span class="sxs-lookup"><span data-stu-id="69c18-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="69c18-218">Выделите любой HTML-элемент, чтобы отобразить наложение, которое является порядком в источнике веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="69c18-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="69c18-220">**Source Order Viewer** in the **Accessibility** pane</span><span class="sxs-lookup"><span data-stu-id="69c18-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="69c18-221">Включить редактор сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="69c18-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="69c18-222">Если включен **эксперимент** "Включить редактор сочетания клавиш", можно настроить сочетания клавиш для любого действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="69c18-223">Чтобы настроить сочетания клавиш для определенного действия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-224">[Откройте DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="69c18-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="69c18-225">Откройте ["Параметры".][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="69c18-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="69c18-226">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="69c18-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="69c18-227">Перейдите на **страницу ярлыков.**</span><span class="sxs-lookup"><span data-stu-id="69c18-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="69c18-228">Выберите действие, настраиваемую.</span><span class="sxs-lookup"><span data-stu-id="69c18-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="69c18-229">Choose the **Edit** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \) icon.</span><span class="sxs-lookup"><span data-stu-id="69c18-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выбор действия для настройки на странице "Ярлыки" в параметрах" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="69c18-231">Выбор действия для настройки на странице **"Ярлыки"** в [параметрах][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="69c18-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c18-232">На клавиатуре выберите клавиши для привязки к действию.</span><span class="sxs-lookup"><span data-stu-id="69c18-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выбор ключей для назначения действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="69c18-234">Выбор ключей для назначения действию</span><span class="sxs-lookup"><span data-stu-id="69c18-234">Select the keys to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c18-235">Чтобы сохранить новый ярлык клавиатуры, выберите пометку \(</span><span class="sxs-lookup"><span data-stu-id="69c18-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="69c18-237">\) значок.</span><span class="sxs-lookup"><span data-stu-id="69c18-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Choose the checkmark icon to save your new keyboard shortcut" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="69c18-239">Choose the checkmark icon to save your new keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="69c18-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69c18-240">Выберите новый ярлык клавиатуры для запуска действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="69c18-241">На странице **"Ярлыки"** значок настраиваемой клавиатуры **\(** ![ CustomKeyboardShortcut \) отображает настроенные сочетания ](../media/custom-keyboard-shortcut-icon.msft.png) клавиш.</span><span class="sxs-lookup"><span data-stu-id="69c18-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="69c18-242">Чтобы сбросить все ярлыки, выберите **"Восстановить ярлыки по умолчанию".**</span><span class="sxs-lookup"><span data-stu-id="69c18-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="69c18-243">Чтобы отменить изменения при редактировании сочетания клавиш для действия, выберите значок X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="69c18-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="69c18-244">Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="69c18-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="69c18-245">Чтобы добавить несколько ярлыков для действия, выберите **"Добавить ярлык".**</span><span class="sxs-lookup"><span data-stu-id="69c18-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="69c18-246">Если ярлык клавиатуры в настоящее время назначен другому действию, вы не можете сохранить его для нового действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="69c18-247">Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.</span><span class="sxs-lookup"><span data-stu-id="69c18-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="69c18-248">Включить составные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="69c18-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="69c18-249">Теперь можно визуализировать слои вместе с z-индексами и объектной моделью документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="69c18-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="69c18-250">Эта функция помогает отлакить без переключения контекстов так часто.</span><span class="sxs-lookup"><span data-stu-id="69c18-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="69c18-251">Вы определили, что уменьшение переключения контекста является серьезной проблемой.</span><span class="sxs-lookup"><span data-stu-id="69c18-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="69c18-252">Не всегда понятно, как код, который вы пишете, влияет на веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="69c18-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="69c18-253">Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.</span><span class="sxs-lookup"><span data-stu-id="69c18-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="69c18-254">После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="69c18-255">Чтобы использовать **составные слои,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-256">В средстве **"3D View" (3D View) выберите его.**</span><span class="sxs-lookup"><span data-stu-id="69c18-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="69c18-257">Откройте области **составных** слоев.</span><span class="sxs-lookup"><span data-stu-id="69c18-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="69c18-258">Отображаются все закрашенные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="69c18-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="69c18-259">Попробуйте эту функцию с собственными веб-приложениями.</span><span class="sxs-lookup"><span data-stu-id="69c18-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="69c18-261">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="69c18-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="69c18-262">Включить новое средство редактора шрифтов в области стилей</span><span class="sxs-lookup"><span data-stu-id="69c18-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="69c18-263">Теперь для редактирования шрифтов [можно][DevtoolsInspectStylesEditFonts] использовать новый редактор визуальных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="69c18-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="69c18-264">Используйте его для определения шрифтов и характеристик шрифтов.</span><span class="sxs-lookup"><span data-stu-id="69c18-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="69c18-265">Редактор **визуальных шрифтов** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="69c18-266">Переключение между единицами для разных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="69c18-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="69c18-267">Переключение между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="69c18-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="69c18-268">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="69c18-268">Convert units</span></span>  
*   <span data-ttu-id="69c18-269">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="69c18-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="69c18-270">После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="69c18-271">Чтобы использовать новый редактор **визуальных шрифтов,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69c18-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="69c18-272">Откройте средство **"Элементы".**</span><span class="sxs-lookup"><span data-stu-id="69c18-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="69c18-273">Откройте области **стилей.**</span><span class="sxs-lookup"><span data-stu-id="69c18-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="69c18-274">Выберите **значок редактора шрифтов.**</span><span class="sxs-lookup"><span data-stu-id="69c18-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="69c18-275">Для получения дополнительных сведений о новом редакторе **визуальных**шрифтов перейдите к редактированию стилей и параметров шрифтов CSS в области стилей [в DevTools.][DevtoolsInspectStylesEditFonts]</span><span class="sxs-lookup"><span data-stu-id="69c18-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена визуальная области редактора шрифтов" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="69c18-277">Выделена **визуальная** области редактора шрифтов</span><span class="sxs-lookup"><span data-stu-id="69c18-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="69c18-278">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="69c18-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="69c18-279">Эта экспериментальная функция предоставляет множество новых визуализаций для отлажки макетов CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="69c18-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="69c18-280">Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <span data-ttu-id="69c18-281">Отображение постоянных наложения на макетах Flexbox с помощью средства inspect</span><span class="sxs-lookup"><span data-stu-id="69c18-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="69c18-282">Средство **Inspect** позволяет быстро идентифицировать и визуализировать макеты CSS Flexbox на веб-сайте, наведите на них указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="69c18-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="69c18-283">Choose the **Inspect** \( ![ Inspect ](../media/inspect-icon.msft.png) \) icon in the top-left corner of DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="69c18-284">Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера Flex.</span><span class="sxs-lookup"><span data-stu-id="69c18-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="69c18-286">Отображение контейнеров Flexbox с помощью средства **inspect**</span><span class="sxs-lookup"><span data-stu-id="69c18-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="69c18-287">Отображение постоянных наложения на макетах Flexbox</span><span class="sxs-lookup"><span data-stu-id="69c18-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="69c18-288">В Microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения для макетов Flexbox.</span><span class="sxs-lookup"><span data-stu-id="69c18-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="69c18-289">Постоянные наложения предоставляют следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="69c18-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="69c18-290">Постоянные наложения остаются видимыми на веб-странице при прокрутке, движении мыши и использовании других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="69c18-291">Можно использовать несколько постоянных наложения одновременно, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.</span><span class="sxs-lookup"><span data-stu-id="69c18-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="69c18-292">Постоянные наложения предлагают параметры настройки цвета.</span><span class="sxs-lookup"><span data-stu-id="69c18-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="69c18-293">Чтобы перебои в постоянных наложениях в макете Flexbox, используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="69c18-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="69c18-294">Выберите **значок овала Flexbox** рядом с любым контейнером Flexbox, отображаемым в дереве DOM **средства Elements.**</span><span class="sxs-lookup"><span data-stu-id="69c18-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="69c18-295">Откройте новую панель **макета,** расположенную в средстве **"Элементы",** и выберите этот элемент рядом с каждым контейнером Flexbox, который нужно выделить.</span><span class="sxs-lookup"><span data-stu-id="69c18-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Гибкие значки и панель макета в DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="69c18-297">Гибкие значки **и панель макета** в DevTools</span><span class="sxs-lookup"><span data-stu-id="69c18-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <span data-ttu-id="69c18-298">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="69c18-298">Configure persistent overlays</span></span>  

<span data-ttu-id="69c18-299">Чтобы настроить параметры постоянных наложения для сетки CSS или макетов Flexbox, используйте области **макета.**</span><span class="sxs-lookup"><span data-stu-id="69c18-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="69c18-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span><span class="sxs-lookup"><span data-stu-id="69c18-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="69c18-302">Панель макета</span><span class="sxs-lookup"><span data-stu-id="69c18-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="69c18-303">Включить меню вкладок "+кнопка", чтобы открыть дополнительные инструменты</span><span class="sxs-lookup"><span data-stu-id="69c18-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="69c18-304">Теперь можно открыть дополнительные средства с помощью нового значка "Дополнительные **средства"** `+` \( \).</span><span class="sxs-lookup"><span data-stu-id="69c18-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="69c18-305">После включения меню вкладки **"Включить+** кнопка", чтобы открыть эксперимент с дополнительными инструментами и перезагрузить DevTools, справа от группы вкладок в верхней части DevTools будет отображаться знак "плюс" \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="69c18-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="69c18-306">Чтобы отобразить список других средств, которые можно добавить \*\*\*\* на вкладку, выберите новый значок "Дополнительные средства" `+` (\).</span><span class="sxs-lookup"><span data-stu-id="69c18-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="69c18-308">**Дополнительные средства** в верхней области</span><span class="sxs-lookup"><span data-stu-id="69c18-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="69c18-309">Включить средство приветствия</span><span class="sxs-lookup"><span data-stu-id="69c18-309">Enable Welcome tool</span></span>

<span data-ttu-id="69c18-310">В этом эксперименте средство **"Что нового"** заменяется новым **средством приветствия.**</span><span class="sxs-lookup"><span data-stu-id="69c18-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="69c18-311">Он отображает обновленный дизайн для следующего содержимого.</span><span class="sxs-lookup"><span data-stu-id="69c18-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="69c18-312">Ссылки на документы разработчика</span><span class="sxs-lookup"><span data-stu-id="69c18-312">Links to developer docs</span></span>  
*   <span data-ttu-id="69c18-313">последние функции</span><span class="sxs-lookup"><span data-stu-id="69c18-313">the latest features</span></span>  
*   <span data-ttu-id="69c18-314">заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="69c18-314">release notes</span></span>  
*   <span data-ttu-id="69c18-315">Возможность связаться с командой Разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69c18-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="69c18-316">Средство **приветствия** открывается автоматически после каждого обновления Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69c18-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="69c18-317">Чтобы средство приветствия \*\*\*\* не отображались после каждого обновления, после каждого обновления \*\*\*\* под заголовком средства приветствия сберем его рядом с вкладками **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="69c18-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="69c18-318">Если вы предпочитаете исходное средство **"Что** нового", перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и удалите его рядом с вкладками "Включить  >  \*\*\*\* **приветствие".**</span><span class="sxs-lookup"><span data-stu-id="69c18-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство приветствия" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="69c18-320">**Средство приветствия**</span><span class="sxs-lookup"><span data-stu-id="69c18-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <span data-ttu-id="69c18-321">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="69c18-321">Previous experimental features</span></span>  

*   <span data-ttu-id="69c18-322">[3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="69c18-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="69c18-323">[Поддержка перемещения вкладок между][DevtoolsMoveTabs] панелями теперь доступна и включена по умолчанию в Microsoft Edge версии 85 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="69c18-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="69c18-324">[Настройка сочетания клавиш теперь][DevtoolsCustomKeyboardShortcuts] доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="69c18-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="69c18-325">[Эмуляция: поддержка режима двойного][DevtoolsDeviceModeDualScreenAndFoldables] экрана теперь доступна и включена по умолчанию в Microsoft Edge версии 89 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="69c18-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="69c18-326">[Включить новые функции отладки сетки CSS][DevtoolsCssGrid] теперь доступно и включено по умолчанию в Microsoft Edge версии 89 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="69c18-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <span data-ttu-id="69c18-327">Предоставление обратной связи по экспериментальным функциям</span><span class="sxs-lookup"><span data-stu-id="69c18-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="69c18-328">Предоставление отзывов о экспериментах Microsoft Edge DevTools или других экспериментах, связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="69c18-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="69c18-329">Отправьте свой отзыв с помощью **значка отправки отзыва** в DevTools</span><span class="sxs-lookup"><span data-stu-id="69c18-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="69c18-330">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="69c18-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="69c18-332">Значок **отправки отзыва** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="69c18-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверка сетки CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsMoveTabs]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств в режиме устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области стилей в devTools | Документы Майкрософт"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools keyboard shortcuts | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для двухэкранного обнаружения | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Папка | Сума"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
