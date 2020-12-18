---
description: Узнайте, как использовать Microsoft Edge DevTools для просмотра и изменения CSS страницы CSS.
title: Проверка сетки CSS в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1fe6bd1c8efd244315fb9a38777df6ea3e9b1a4d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231099"
---
# <span data-ttu-id="a9c29-104">Проверка сетки CSS</span><span class="sxs-lookup"><span data-stu-id="a9c29-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="a9c29-105">В этой статье вы можете определить сетки CSS на веб-сайте и отладить проблемы макета сетки с помощью настраиваемых наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="a9c29-106">Примеры, используемые на рисунках в этой статье, взяты с следующих веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="a9c29-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="a9c29-107">Поле "Вешка"</span><span class="sxs-lookup"><span data-stu-id="a9c29-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="a9c29-108">Поле "Неугомя"</span><span class="sxs-lookup"><span data-stu-id="a9c29-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <span data-ttu-id="a9c29-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="a9c29-109">Before you begin</span></span>  

<span data-ttu-id="a9c29-110">Сетка CSS — это мощная парадигма макета для Интернета.</span><span class="sxs-lookup"><span data-stu-id="a9c29-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="a9c29-111">Отличное место для начала изучения сетки CSS и многих функций — это руководство по макету сетки [CSS][MdnCssGridLayout] на MDN.</span><span class="sxs-lookup"><span data-stu-id="a9c29-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <span data-ttu-id="a9c29-112">Обнаружение сеток CSS</span><span class="sxs-lookup"><span data-stu-id="a9c29-112">Discover CSS grids</span></span>  

<span data-ttu-id="a9c29-113">Если htmL-элемент на странице имеет или применяется к ней, рядом с ней на панели элементов отображается индикатор `display: grid` `display: inline-grid` `grid` событий. [][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="a9c29-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Обнаружение сетки" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="a9c29-115">Обнаружение сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="a9c29-116">Выберите индикатор событий, чтобы выровнять отображение наложения сетки на странице.</span><span class="sxs-lookup"><span data-stu-id="a9c29-116">Select the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="a9c29-117">Наложение появляется над элементом и, как сетка, отображает положение линий сетки и дорожек:</span><span class="sxs-lookup"><span data-stu-id="a9c29-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Индикатор событий сетки" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="a9c29-119">Индикатор событий сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="a9c29-120">Откройте области **макета.**</span><span class="sxs-lookup"><span data-stu-id="a9c29-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="a9c29-121">Если сетки включены на страницу, в области макета содержится раздел **Grid,** содержащий несколько параметров для просмотра сеток. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a9c29-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Области макета" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="a9c29-123">**Области** макета</span><span class="sxs-lookup"><span data-stu-id="a9c29-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="a9c29-124">Раздел **Grid** в области **макета** содержит следующие 2 под раздела.</span><span class="sxs-lookup"><span data-stu-id="a9c29-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="a9c29-125">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="a9c29-125">Overlay display settings</span></span>  
*   <span data-ttu-id="a9c29-126">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <span data-ttu-id="a9c29-127">Параметры отображения наложения</span><span class="sxs-lookup"><span data-stu-id="a9c29-127">Overlay display settings</span></span>  

<span data-ttu-id="a9c29-128">Параметры **отображения наложения** состоят из следующих 2 частей.</span><span class="sxs-lookup"><span data-stu-id="a9c29-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="a9c29-129">Выберите один из следующих параметров из меню в выпадаемом меню.</span><span class="sxs-lookup"><span data-stu-id="a9c29-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="a9c29-130">Вариант строки</span><span class="sxs-lookup"><span data-stu-id="a9c29-130">Line option</span></span> | <span data-ttu-id="a9c29-131">Сведения</span><span class="sxs-lookup"><span data-stu-id="a9c29-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="a9c29-132">Скрытие подписей строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-132">Hide line labels</span></span>** | <span data-ttu-id="a9c29-133">Скрыть метки линий для каждого наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="a9c29-134">Показывать номера строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-134">Show line numbers</span></span>** | <span data-ttu-id="a9c29-135">Отображение номеров линий для каждого наложения сетки \(выбрано по умолчанию\).</span><span class="sxs-lookup"><span data-stu-id="a9c29-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="a9c29-136">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-136">Show line names</span></span>** | <span data-ttu-id="a9c29-137">Отображение имен линий для каждого наложения сетки при их выводе.</span><span class="sxs-lookup"><span data-stu-id="a9c29-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="a9c29-138">Выберите этот контрольный параметр рядом со следующими вариантами.</span><span class="sxs-lookup"><span data-stu-id="a9c29-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="a9c29-139">Параметр</span><span class="sxs-lookup"><span data-stu-id="a9c29-139">Option</span></span> | <span data-ttu-id="a9c29-140">Сведения</span><span class="sxs-lookup"><span data-stu-id="a9c29-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="a9c29-141">Показать размеры дорожки</span><span class="sxs-lookup"><span data-stu-id="a9c29-141">Show track sizes</span></span>**  | <span data-ttu-id="a9c29-142">Отображение \(или скрытие\) размеров дорожек.</span><span class="sxs-lookup"><span data-stu-id="a9c29-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="a9c29-143">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="a9c29-143">Show area names</span></span>** | <span data-ttu-id="a9c29-144">Отображение \(или скрытие\) имен области при их выводе.</span><span class="sxs-lookup"><span data-stu-id="a9c29-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="a9c29-145">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-145">Extend grid lines</span></span>** | <span data-ttu-id="a9c29-146">Отображает \(или скрывает\) расширения размеров сетки вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="a9c29-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="a9c29-147">По умолчанию линии сетки показаны внутри элемента только с установленным или `display: grid` `display: inline-grid` установленным значением CSS.</span><span class="sxs-lookup"><span data-stu-id="a9c29-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="a9c29-148">В следующих разделах представлены подробные сведения о каждом из параметров отображения **наложения.**</span><span class="sxs-lookup"><span data-stu-id="a9c29-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <span data-ttu-id="a9c29-149">Показывать номера строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-149">Show line numbers</span></span>  

<span data-ttu-id="a9c29-150">По умолчанию положительные и отрицательные номера строк отображаются на наложение сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="a9c29-151">Для получения дополнительных сведений о отрицательных числах в наложение сетки перейдите к расположению на основе [строки с помощью сетки CSS.][MdnLineBasedPlacementCssGrid]</span><span class="sxs-lookup"><span data-stu-id="a9c29-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Отображение номеров строк" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="a9c29-153">Отображение номеров строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-153">Display line numbers</span></span>  
:::image-end:::  

### <span data-ttu-id="a9c29-154">Скрытие подписей строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-154">Hide line labels</span></span>  

<span data-ttu-id="a9c29-155">Выберите **"Скрыть метки строки",** чтобы скрыть номера строк.</span><span class="sxs-lookup"><span data-stu-id="a9c29-155">Select **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Скрытие подписей строк" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="a9c29-157">Скрытие подписей строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-157">Hide line labels</span></span>  
:::image-end:::  

### <span data-ttu-id="a9c29-158">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-158">Show line names</span></span>  

<span data-ttu-id="a9c29-159">Для получения дополнительных сведений об именах строк в наложение сетки перейдите к макету с [помощью именуемой сетки.][MdnLayoutUsingNamedGridLines]</span><span class="sxs-lookup"><span data-stu-id="a9c29-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="a9c29-160">Select **Show line names** to view the line names instead of numbers.</span><span class="sxs-lookup"><span data-stu-id="a9c29-160">Select **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="a9c29-161">В примере 4 строки имеют имена: `left` , , , и `middle1` `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="a9c29-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Показать имена строк" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="a9c29-163">Показать имена строк</span><span class="sxs-lookup"><span data-stu-id="a9c29-163">Show line names</span></span>**  
:::image-end:::  

### <span data-ttu-id="a9c29-164">Показать размеры дорожки</span><span class="sxs-lookup"><span data-stu-id="a9c29-164">Show track sizes</span></span>  

<span data-ttu-id="a9c29-165">В поле **"Показать размеры дорожки"** для просмотра размеров дорожки сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="a9c29-166">DevTools отображает `[authored size]` и `[computed size]` в каждой метке строки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="a9c29-167">Size</span><span class="sxs-lookup"><span data-stu-id="a9c29-167">Size</span></span> | <span data-ttu-id="a9c29-168">Сведения</span><span class="sxs-lookup"><span data-stu-id="a9c29-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="a9c29-169">авторский размер</span><span class="sxs-lookup"><span data-stu-id="a9c29-169">authored size</span></span>** | <span data-ttu-id="a9c29-170">Размер, определенный в таблице стилей \(пропущен, если не определен\).</span><span class="sxs-lookup"><span data-stu-id="a9c29-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="a9c29-171">вычисляемая величина</span><span class="sxs-lookup"><span data-stu-id="a9c29-171">computed size</span></span>** | <span data-ttu-id="a9c29-172">Фактический размер на экране.</span><span class="sxs-lookup"><span data-stu-id="a9c29-172">The actual size on screen.</span></span> |  

<span data-ttu-id="a9c29-173">В демонстрации размеры `snack-box` столбцов определяются в `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="a9c29-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="a9c29-174">Поэтому метки строк столбцов отображают как авторские, так и вычисляемые размеры.</span><span class="sxs-lookup"><span data-stu-id="a9c29-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="a9c29-175">Размер отслеживания</span><span class="sxs-lookup"><span data-stu-id="a9c29-175">Track size</span></span> | <span data-ttu-id="a9c29-176">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="a9c29-176">Authored size</span></span> | <span data-ttu-id="a9c29-177">Вычисляемая величина</span><span class="sxs-lookup"><span data-stu-id="a9c29-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="a9c29-178">**1fr** &#x2022; **96.66px**</span><span class="sxs-lookup"><span data-stu-id="a9c29-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="a9c29-179">1fr</span><span class="sxs-lookup"><span data-stu-id="a9c29-179">1fr</span></span> | <span data-ttu-id="a9c29-180">96,66px</span><span class="sxs-lookup"><span data-stu-id="a9c29-180">96.66px</span></span> |  
| <span data-ttu-id="a9c29-181">**2fr** &#x2022; **193.32px**</span><span class="sxs-lookup"><span data-stu-id="a9c29-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="a9c29-182">2fr</span><span class="sxs-lookup"><span data-stu-id="a9c29-182">2fr</span></span> | <span data-ttu-id="a9c29-183">193,32px</span><span class="sxs-lookup"><span data-stu-id="a9c29-183">193.32px</span></span> |  

<span data-ttu-id="a9c29-184">Метки строк отображают только вычисленные размеры, так как в таблице стилей не определены размеры строк.</span><span class="sxs-lookup"><span data-stu-id="a9c29-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="a9c29-185">Размер отслеживания</span><span class="sxs-lookup"><span data-stu-id="a9c29-185">Track size</span></span> | <span data-ttu-id="a9c29-186">Авторский размер</span><span class="sxs-lookup"><span data-stu-id="a9c29-186">Authored size</span></span> | <span data-ttu-id="a9c29-187">Вычисляемая величина</span><span class="sxs-lookup"><span data-stu-id="a9c29-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="a9c29-188">80px</span><span class="sxs-lookup"><span data-stu-id="a9c29-188">80px</span></span>** | &nbsp;| <span data-ttu-id="a9c29-189">80px</span><span class="sxs-lookup"><span data-stu-id="a9c29-189">80px</span></span> |  
| **<span data-ttu-id="a9c29-190">80px</span><span class="sxs-lookup"><span data-stu-id="a9c29-190">80px</span></span>** | &nbsp;| <span data-ttu-id="a9c29-191">80px</span><span class="sxs-lookup"><span data-stu-id="a9c29-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Показать размеры дорожки" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="a9c29-193">Показать размеры дорожки</span><span class="sxs-lookup"><span data-stu-id="a9c29-193">Show track sizes</span></span>**  
:::image-end:::  

### <span data-ttu-id="a9c29-194">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="a9c29-194">Show area names</span></span>  

<span data-ttu-id="a9c29-195">Чтобы просмотреть имена области, в убедитесь, что в списке **должны быть имена** области.</span><span class="sxs-lookup"><span data-stu-id="a9c29-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="a9c29-196">В этом примере сетка имеет 3 области: **верхняя,** **нижняя1** и **нижняя 2.**</span><span class="sxs-lookup"><span data-stu-id="a9c29-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Показать имена области" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="a9c29-198">Показать имена области</span><span class="sxs-lookup"><span data-stu-id="a9c29-198">Show area names</span></span>**  
:::image-end:::  

### <span data-ttu-id="a9c29-199">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-199">Extend grid lines</span></span>  

<span data-ttu-id="a9c29-200">В поле **"Расширить линии сетки",** чтобы линии сетки были расширены до края точки просмотра вдоль каждой оси.</span><span class="sxs-lookup"><span data-stu-id="a9c29-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Расширение линий сетки" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="a9c29-202">Расширение линий сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-202">Extend grid lines</span></span>**  
:::image-end:::  

## <span data-ttu-id="a9c29-203">Наложения сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-203">Grid overlays</span></span>  

<span data-ttu-id="a9c29-204">Раздел **"Наложения сетки"** содержит список сеток, присутствующих на странице, каждый из которых с помощью контрольного списка, а также различные параметры.</span><span class="sxs-lookup"><span data-stu-id="a9c29-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <span data-ttu-id="a9c29-205">Включить представления наложения для нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="a9c29-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="a9c29-206">Чтобы отобразить сетку наложения для нескольких сеток, выберите его рядом с каждым именем сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="a9c29-207">В этом примере включены 2 наложения сетки, каждая из которых представлена разными цветами.</span><span class="sxs-lookup"><span data-stu-id="a9c29-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Включить представления наложения для нескольких сеток" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="a9c29-209">Включить представления наложения для нескольких сеток</span><span class="sxs-lookup"><span data-stu-id="a9c29-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <span data-ttu-id="a9c29-210">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="a9c29-211">Чтобы открыть палитру и настроить цвет наложения сетки, выберите поле рядом с именем наложения сетки.</span><span class="sxs-lookup"><span data-stu-id="a9c29-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Настройка цвета наложения сетки" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="a9c29-213">Настройка цвета наложения сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <span data-ttu-id="a9c29-214">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-214">Highlight the grid</span></span>  

<span data-ttu-id="a9c29-215">Чтобы выделить HTML-элемент \*\*\*\* на панели "Элементы" и прокрутить его на веб-странице, выберите элемент **Show** на панели элементов \( Элемент Show в значке панели элементов ![ ][ImageShowElementInElementsPanelIcon] \)</span><span class="sxs-lookup"><span data-stu-id="a9c29-215">To highlight the HTML element in the **Elements** panel and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Выделение сетки" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="a9c29-217">Выделение сетки</span><span class="sxs-lookup"><span data-stu-id="a9c29-217">Highlight the grid</span></span>  
:::image-end:::  

## <span data-ttu-id="a9c29-218">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a9c29-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Сетка CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Сетка CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Макет с использованием именуемой сетки | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Размещение на основе строк с помощью сетки CSS | MDN"  

> [!NOTE]
> <span data-ttu-id="a9c29-225">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9c29-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a9c29-226">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/css/grid). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="a9c29-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a9c29-228">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9c29-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
