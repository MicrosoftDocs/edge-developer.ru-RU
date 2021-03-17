---
description: Узнайте, как использовать Microsoft Edge DevTools для просмотра и изменения CSS страницы CSS.
title: Проверка CSS Grid в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 034fbdf82ddba39fc0818bc6f3add8824c6bb3ac
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439263"
---
# <a name="inspect-css-grid"></a><span data-ttu-id="72c95-104">Проверка сетки CSS</span><span class="sxs-lookup"><span data-stu-id="72c95-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="72c95-105">В этой статье вы можете определить сетки CSS на веб-сайте и отладить проблемы макета сетки с помощью настраиваемых накладок сетки.</span><span class="sxs-lookup"><span data-stu-id="72c95-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="72c95-106">Примеры, используемые в рисунках в этой статье, взяты из следующих веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="72c95-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="72c95-107">Поле "Фрукты"</span><span class="sxs-lookup"><span data-stu-id="72c95-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="72c95-108">Снэк-ок</span><span class="sxs-lookup"><span data-stu-id="72c95-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a><span data-ttu-id="72c95-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="72c95-109">Before you begin</span></span>  

<span data-ttu-id="72c95-110">CSS Grid — это мощная парадигма макета для Интернета.</span><span class="sxs-lookup"><span data-stu-id="72c95-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="72c95-111">Отличное место для начала изучения CSS Grid и многих функций — руководство по макету [сетки CSS][MdnCssGridLayout] на MDN.</span><span class="sxs-lookup"><span data-stu-id="72c95-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <a name="discover-css-grids"></a><span data-ttu-id="72c95-112">Откройте для себя сетки CSS</span><span class="sxs-lookup"><span data-stu-id="72c95-112">Discover CSS grids</span></span>  

<span data-ttu-id="72c95-113">Если элемент HTML на вашей странице имеет или применяется к ней, рядом с ней в панели Elements отображается `display: grid` `display: inline-grid` `grid` значок. [][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="72c95-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Откройте сетку" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="72c95-115">Откройте сетку</span><span class="sxs-lookup"><span data-stu-id="72c95-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="72c95-116">Выберите значок, чтобы отобразить накладку сетки на странице.</span><span class="sxs-lookup"><span data-stu-id="72c95-116">Choose the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="72c95-117">Наложение появляется над элементом, выложенным как сетка, чтобы отобразить положение линий и треков сетки:</span><span class="sxs-lookup"><span data-stu-id="72c95-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Значок сетки toggle" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="72c95-119">Значок сетки toggle</span><span class="sxs-lookup"><span data-stu-id="72c95-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="72c95-120">Откройте области **макета.**</span><span class="sxs-lookup"><span data-stu-id="72c95-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="72c95-121">Когда сетки включены на странице, в области **Макета** содержится раздел **Grid,** содержащий несколько вариантов просмотра сетки.</span><span class="sxs-lookup"><span data-stu-id="72c95-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Области макета" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="72c95-123">**Области** макета</span><span class="sxs-lookup"><span data-stu-id="72c95-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="72c95-124">Раздел **Grid** в области **Макет** содержит следующие 2 под раздела.</span><span class="sxs-lookup"><span data-stu-id="72c95-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="72c95-125">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="72c95-125">Overlay display settings</span></span>  
*   <span data-ttu-id="72c95-126">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a><span data-ttu-id="72c95-127">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="72c95-127">Overlay display settings</span></span>  

<span data-ttu-id="72c95-128">Параметры **отображения overlay состоят** из следующих 2 частей.</span><span class="sxs-lookup"><span data-stu-id="72c95-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="72c95-129">Выберите один из следующих вариантов из меню отсев.</span><span class="sxs-lookup"><span data-stu-id="72c95-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="72c95-130">Параметр Line</span><span class="sxs-lookup"><span data-stu-id="72c95-130">Line option</span></span> | <span data-ttu-id="72c95-131">Сведения</span><span class="sxs-lookup"><span data-stu-id="72c95-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="72c95-132">Скрыть метки строки</span><span class="sxs-lookup"><span data-stu-id="72c95-132">Hide line labels</span></span>** | <span data-ttu-id="72c95-133">Скрыть метки линий для каждой сетки наложения.</span><span class="sxs-lookup"><span data-stu-id="72c95-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="72c95-134">Показать номера строк</span><span class="sxs-lookup"><span data-stu-id="72c95-134">Show line numbers</span></span>** | <span data-ttu-id="72c95-135">Отображение номеров линий для каждой сетки наложения \(выбрано по умолчанию\).</span><span class="sxs-lookup"><span data-stu-id="72c95-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="72c95-136">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="72c95-136">Show line names</span></span>** | <span data-ttu-id="72c95-137">Отображение имен линий для каждой сетки при условии их наложения.</span><span class="sxs-lookup"><span data-stu-id="72c95-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="72c95-138">Выберите контрольный ящик далее следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="72c95-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="72c95-139">Параметр</span><span class="sxs-lookup"><span data-stu-id="72c95-139">Option</span></span> | <span data-ttu-id="72c95-140">Сведения</span><span class="sxs-lookup"><span data-stu-id="72c95-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="72c95-141">Показать размеры трека</span><span class="sxs-lookup"><span data-stu-id="72c95-141">Show track sizes</span></span>**  | <span data-ttu-id="72c95-142">Отображение \(или скрыть\) размеров треков.</span><span class="sxs-lookup"><span data-stu-id="72c95-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="72c95-143">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="72c95-143">Show area names</span></span>** | <span data-ttu-id="72c95-144">Отображение \(или скрыть\) имен области, когда предоставляются имена.</span><span class="sxs-lookup"><span data-stu-id="72c95-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="72c95-145">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-145">Extend grid lines</span></span>** | <span data-ttu-id="72c95-146">Отображает \(или скрывает\) расширения размеров сетки вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="72c95-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="72c95-147">По умолчанию строки сетки показаны только внутри элемента с набором `display: grid` `display: inline-grid` CSS или на нем.</span><span class="sxs-lookup"><span data-stu-id="72c95-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="72c95-148">В следующих разделах представлены сведения для каждого из **параметров отображения overlay.**</span><span class="sxs-lookup"><span data-stu-id="72c95-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <a name="show-line-numbers"></a><span data-ttu-id="72c95-149">Показать номера строк</span><span class="sxs-lookup"><span data-stu-id="72c95-149">Show line numbers</span></span>  

<span data-ttu-id="72c95-150">По умолчанию на накладке сетки отображаются номера положительных и отрицательных строк.</span><span class="sxs-lookup"><span data-stu-id="72c95-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="72c95-151">Дополнительные сведения о отрицательных номерах в сетке наложения перейдите к размещению на основе [строки с CSS Grid][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="72c95-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Отображение номеров строк" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="72c95-153">Отображение номеров строк</span><span class="sxs-lookup"><span data-stu-id="72c95-153">Display line numbers</span></span>  
:::image-end:::  

### <a name="hide-line-labels"></a><span data-ttu-id="72c95-154">Скрыть метки строки</span><span class="sxs-lookup"><span data-stu-id="72c95-154">Hide line labels</span></span>  

<span data-ttu-id="72c95-155">Выберите **метки hide line,** чтобы скрыть номера строк.</span><span class="sxs-lookup"><span data-stu-id="72c95-155">Choose **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Скрыть метки строки" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="72c95-157">Скрыть метки строки</span><span class="sxs-lookup"><span data-stu-id="72c95-157">Hide line labels</span></span>  
:::image-end:::  

### <a name="show-line-names"></a><span data-ttu-id="72c95-158">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="72c95-158">Show line names</span></span>  

<span data-ttu-id="72c95-159">Дополнительные сведения о именах строк в накладке сетки перейдите в [Макет с помощью именных линий сетки.][MdnLayoutUsingNamedGridLines]</span><span class="sxs-lookup"><span data-stu-id="72c95-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="72c95-160">Выберите **имена строк Show,** чтобы просмотреть имена строк, а не числа.</span><span class="sxs-lookup"><span data-stu-id="72c95-160">Choose **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="72c95-161">В примере 4 строки имеют имена: `left` `middle1` , и `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="72c95-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Показать имена строк" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="72c95-163">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="72c95-163">Show line names</span></span>**  
:::image-end:::  

### <a name="show-track-sizes"></a><span data-ttu-id="72c95-164">Показать размеры трека</span><span class="sxs-lookup"><span data-stu-id="72c95-164">Show track sizes</span></span>  

<span data-ttu-id="72c95-165">Включить **контрольный ящик Размеров** трассы Show для просмотра размеров трассы сетки.</span><span class="sxs-lookup"><span data-stu-id="72c95-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="72c95-166">DevTools отображает `[authored size]` и `[computed size]` на каждой метке строки.</span><span class="sxs-lookup"><span data-stu-id="72c95-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="72c95-167">Size</span><span class="sxs-lookup"><span data-stu-id="72c95-167">Size</span></span> | <span data-ttu-id="72c95-168">Сведения</span><span class="sxs-lookup"><span data-stu-id="72c95-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="72c95-169">авторский размер</span><span class="sxs-lookup"><span data-stu-id="72c95-169">authored size</span></span>** | <span data-ttu-id="72c95-170">Размер, определенный в таблице стилей \(опущен, если не определен\).</span><span class="sxs-lookup"><span data-stu-id="72c95-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="72c95-171">вычислительный размер</span><span class="sxs-lookup"><span data-stu-id="72c95-171">computed size</span></span>** | <span data-ttu-id="72c95-172">Фактический размер на экране.</span><span class="sxs-lookup"><span data-stu-id="72c95-172">The actual size on screen.</span></span> |  

<span data-ttu-id="72c95-173">В демонстрации размеры `snack-box` столбцов определяются в `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="72c95-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="72c95-174">Поэтому метки строк столбцов отображают как авторские, так и вычислительные размеры.</span><span class="sxs-lookup"><span data-stu-id="72c95-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="72c95-175">Размер дорожки</span><span class="sxs-lookup"><span data-stu-id="72c95-175">Track size</span></span> | <span data-ttu-id="72c95-176">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="72c95-176">Authored size</span></span> | <span data-ttu-id="72c95-177">Вычислительный размер</span><span class="sxs-lookup"><span data-stu-id="72c95-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="72c95-178">**1fr** &#x2022; **96.66px**</span><span class="sxs-lookup"><span data-stu-id="72c95-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="72c95-179">1fr</span><span class="sxs-lookup"><span data-stu-id="72c95-179">1fr</span></span> | <span data-ttu-id="72c95-180">96.66px</span><span class="sxs-lookup"><span data-stu-id="72c95-180">96.66px</span></span> |  
| <span data-ttu-id="72c95-181">**2fr** &#x2022; **193.32px**</span><span class="sxs-lookup"><span data-stu-id="72c95-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="72c95-182">2fr</span><span class="sxs-lookup"><span data-stu-id="72c95-182">2fr</span></span> | <span data-ttu-id="72c95-183">193.32px</span><span class="sxs-lookup"><span data-stu-id="72c95-183">193.32px</span></span> |  

<span data-ttu-id="72c95-184">Метки строк отображают только вычисляемые размеры, так как в таблице стилей нет размеров строк.</span><span class="sxs-lookup"><span data-stu-id="72c95-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="72c95-185">Размер дорожки</span><span class="sxs-lookup"><span data-stu-id="72c95-185">Track size</span></span> | <span data-ttu-id="72c95-186">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="72c95-186">Authored size</span></span> | <span data-ttu-id="72c95-187">Вычислительный размер</span><span class="sxs-lookup"><span data-stu-id="72c95-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="72c95-188">80px</span><span class="sxs-lookup"><span data-stu-id="72c95-188">80px</span></span>** | &nbsp;| <span data-ttu-id="72c95-189">80px</span><span class="sxs-lookup"><span data-stu-id="72c95-189">80px</span></span> |  
| **<span data-ttu-id="72c95-190">80px</span><span class="sxs-lookup"><span data-stu-id="72c95-190">80px</span></span>** | &nbsp;| <span data-ttu-id="72c95-191">80px</span><span class="sxs-lookup"><span data-stu-id="72c95-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Показать размеры трека" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="72c95-193">Показать размеры трека</span><span class="sxs-lookup"><span data-stu-id="72c95-193">Show track sizes</span></span>**  
:::image-end:::  

### <a name="show-area-names"></a><span data-ttu-id="72c95-194">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="72c95-194">Show area names</span></span>  

<span data-ttu-id="72c95-195">Чтобы просмотреть имена области, вкажите почтовый ящик **Имена области** Показать.</span><span class="sxs-lookup"><span data-stu-id="72c95-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="72c95-196">В примере в сетке 3 области: **верхняя,** **нижняя и** **нижняя 2.**</span><span class="sxs-lookup"><span data-stu-id="72c95-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Показать имена области" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="72c95-198">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="72c95-198">Show area names</span></span>**  
:::image-end:::  

### <a name="extend-grid-lines"></a><span data-ttu-id="72c95-199">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-199">Extend grid lines</span></span>  

<span data-ttu-id="72c95-200">**Вдайте контрольный** ящик Extend grid lines для расширения линий сетки до края представления на каждой оси.</span><span class="sxs-lookup"><span data-stu-id="72c95-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Расширение линий сетки" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="72c95-202">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-202">Extend grid lines</span></span>**  
:::image-end:::  

## <a name="grid-overlays"></a><span data-ttu-id="72c95-203">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-203">Grid overlays</span></span>  

<span data-ttu-id="72c95-204">Раздел **Grid overlays** содержит список сетки, которые присутствуют на странице, каждая из которых имеет почтовый ящик, а также различные параметры.</span><span class="sxs-lookup"><span data-stu-id="72c95-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <a name="enable-overlay-views-of-multiple-grids"></a><span data-ttu-id="72c95-205">Включить представления наложения нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="72c95-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="72c95-206">Чтобы отобразить сетку наложения для нескольких сеток, выберите контрольный ящик рядом с каждым именем сетки.</span><span class="sxs-lookup"><span data-stu-id="72c95-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="72c95-207">В примере включено 2 сетки, каждая из которых представлена разными цветами.</span><span class="sxs-lookup"><span data-stu-id="72c95-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Включить представления наложения нескольких сеток" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="72c95-209">Включить представления наложения нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="72c95-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a><span data-ttu-id="72c95-210">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="72c95-211">Чтобы открыть выбор цвета и настроить цвет наложения сетки, выберите поле рядом с именем наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="72c95-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Настройка цвета наложения сетки" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="72c95-213">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <a name="highlight-the-grid"></a><span data-ttu-id="72c95-214">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-214">Highlight the grid</span></span>  

<span data-ttu-id="72c95-215">Чтобы выделить элемент HTML в средстве **Elements** и прокрутите его на веб-странице, выберите элемент Show в панели **Elements** \( Элемент Show в значке панели ![ Elements ](../media/show-element-in-element-panel-icon.msft.png) \) .</span><span class="sxs-lookup"><span data-stu-id="72c95-215">To highlight the HTML element in the **Elements** tool and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon](../media/show-element-in-element-panel-icon.msft.png)\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Выделение сетки" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="72c95-217">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="72c95-217">Highlight the grid</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="72c95-218">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="72c95-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Сетка CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Сетка CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Макет с использованием именных линий сетки | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Размещение на основе строки с CSS Grid | MDN"  

> [!NOTE]
> <span data-ttu-id="72c95-225">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="72c95-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="72c95-226">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/css/grid). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="72c95-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="72c95-228">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="72c95-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
