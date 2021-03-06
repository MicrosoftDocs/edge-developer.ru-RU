---
description: Определение дорогостоящих функций с помощью панели памяти Microsoft Edge DevTools.
title: Ускорение среды выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 682001ae8d265b342e5d6e0725f9f8ac4e298cf8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397603"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# <a name="speed-up-javascript-runtime"></a><span data-ttu-id="a3ec1-104">Ускорение среды выполнения JavaScript</span><span class="sxs-lookup"><span data-stu-id="a3ec1-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="a3ec1-105">Определение дорогостоящих функций с **помощью панели памяти.**</span><span class="sxs-lookup"><span data-stu-id="a3ec1-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Примеры профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="a3ec1-107">Примеры профилей</span><span class="sxs-lookup"><span data-stu-id="a3ec1-107">Sample Profiles</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="a3ec1-108">Сводка</span><span class="sxs-lookup"><span data-stu-id="a3ec1-108">Summary</span></span>  

*   <span data-ttu-id="a3ec1-109">Зафиксировать точно, какие функции были вызваны и сколько памяти требуется для каждой из них с помощью выборки выделения в **панели памяти.**</span><span class="sxs-lookup"><span data-stu-id="a3ec1-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="a3ec1-110">Визуализация профилей в качестве диаграммы пламени.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-110">Visualize your profiles as a flame chart.</span></span>  
    
## <a name="record-a-sampling-profile"></a><span data-ttu-id="a3ec1-111">Запись профиля выборки</span><span class="sxs-lookup"><span data-stu-id="a3ec1-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="a3ec1-112">Если вы заметили jank в JavaScript, соберите профиль выборки.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="a3ec1-113">В профилях выборки покажите, где время работы тратится на функции на странице.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="a3ec1-114">Перейдите к **панели памяти** DevTools.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-114">Navigate to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="a3ec1-115">Выберите радио **кнопку Распределение выборки.**</span><span class="sxs-lookup"><span data-stu-id="a3ec1-115">Choose the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="a3ec1-116">Выберите **Начните**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="a3ec1-117">В зависимости от того, что вы пытаетесь проанализировать, вы можете обновить страницу, взаимодействовать со страницей или просто запустить страницу.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-117">Depending on what you are trying to analyze, you may either refresh the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="a3ec1-118">Выберите **кнопку Stop** по завершению.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-118">Choose the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a3ec1-119">Можно также использовать [API консоли utilities][DevtoolsConsoleUtilities] для записи профилей командной строки и групп.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <a name="view-sampling-profile"></a><span data-ttu-id="a3ec1-120">Просмотр профиля выборки</span><span class="sxs-lookup"><span data-stu-id="a3ec1-120">View Sampling Profile</span></span>  

<span data-ttu-id="a3ec1-121">Когда вы закончите запись, DevTools \*\*\*\* автоматически заполняет панель памяти в **профили SAMPLING** с данными из записи.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="a3ec1-122">Представление по умолчанию **— Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a3ec1-123">Это представление позволяет просмотреть, какие функции оказали наибольшее влияние на производительность и просмотреть путь запроса для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-123">This view allows you to review which functions had the most impact on performance and examine the requesting path for each function.</span></span>  

### <a name="change-sort-order"></a><span data-ttu-id="a3ec1-124">Изменение порядка сортировки</span><span class="sxs-lookup"><span data-stu-id="a3ec1-124">Change sort order</span></span>  

<span data-ttu-id="a3ec1-125">Чтобы изменить порядок сортировки, выберите меню dropdown рядом с выбранной функцией **фокуса** \( функция фокуса \) и выберите один из ![ ][ImageFocusIcon] следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="a3ec1-126">**Диаграмма**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-126">**Chart**.</span></span>  <span data-ttu-id="a3ec1-127">Отображает хронологическую диаграмму записи.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Диаграмма пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="a3ec1-129">Диаграмма пламени</span><span class="sxs-lookup"><span data-stu-id="a3ec1-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a3ec1-130">**Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a3ec1-131">Списки функций по влиянию на производительность и позволяет изучить пути вызова к функциям.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="a3ec1-132">Это представление по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Тяжелая диаграмма" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="a3ec1-134">Тяжелая диаграмма</span><span class="sxs-lookup"><span data-stu-id="a3ec1-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="a3ec1-135">**Tree \(Top Down\)**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="a3ec1-136">Отображает общую картину структуры вызовов, начиная с верхней части стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Диаграмма дерева" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="a3ec1-138">Диаграмма дерева</span><span class="sxs-lookup"><span data-stu-id="a3ec1-138">Tree chart</span></span>  
:::image-end:::  

### <a name="exclude-functions"></a><span data-ttu-id="a3ec1-139">Исключение функций</span><span class="sxs-lookup"><span data-stu-id="a3ec1-139">Exclude functions</span></span>  

<span data-ttu-id="a3ec1-140">Чтобы исключить функцию из профиля выборки, выберите ее, а затем выберите исключенную выбранную функцию **\(** исключить выбранную ![ ][ImageExcludeIcon] функцию \) кнопку.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="a3ec1-141">Функция запроса \(parent\) исключенной функции \(child\) заряжается выделенной памятью, назначенной исключенной функции \(child\).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="a3ec1-142">Выберите **кнопку восстановление** всех функций \( восстановление всех функций \) для восстановления всех исключенных функций ![ обратно в ][ImageRestoreIcon] запись.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-142">Choose the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <a name="view-sampling-profile-as-chart"></a><span data-ttu-id="a3ec1-143">Просмотр профиля выборки в качестве диаграммы</span><span class="sxs-lookup"><span data-stu-id="a3ec1-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="a3ec1-144">Представление Диаграммы обеспечивает визуальное представление профиля выборки со временем.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="a3ec1-145">После [записи профиля выборки](#record-a-sampling-profile)просмотреть запись в качестве диаграммы [пламени,](#change-sort-order) изменив порядок сортировки на **диаграмму**.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Представление диаграммы пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="a3ec1-147">Представление диаграммы пламени</span><span class="sxs-lookup"><span data-stu-id="a3ec1-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="a3ec1-148">Диаграмма пламени разделена на две части.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="a3ec1-149">индекс</span><span class="sxs-lookup"><span data-stu-id="a3ec1-149">index</span></span> | <span data-ttu-id="a3ec1-150">Часть</span><span class="sxs-lookup"><span data-stu-id="a3ec1-150">Part</span></span> | <span data-ttu-id="a3ec1-151">Описание</span><span class="sxs-lookup"><span data-stu-id="a3ec1-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="a3ec1-152">1</span><span class="sxs-lookup"><span data-stu-id="a3ec1-152">1</span></span> | <span data-ttu-id="a3ec1-153">Обзор</span><span class="sxs-lookup"><span data-stu-id="a3ec1-153">Overview</span></span> | <span data-ttu-id="a3ec1-154">Вид с глаз птиц на всю запись.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="a3ec1-155">Высота баров соответствует глубине стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="a3ec1-156">Чем выше планка, тем глубже стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="a3ec1-157">2</span><span class="sxs-lookup"><span data-stu-id="a3ec1-157">2</span></span> | <span data-ttu-id="a3ec1-158">Стеки вызовов</span><span class="sxs-lookup"><span data-stu-id="a3ec1-158">Call Stacks</span></span> | <span data-ttu-id="a3ec1-159">Это углубленное представление функций, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="a3ec1-160">Горизонтальная ось — это время, а вертикальная ось — это стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="a3ec1-161">Стеки организованы сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="a3ec1-162">Таким образом, функция в верхней части называется одна ниже нее, и так далее.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="a3ec1-163">Функции окрашены случайным образом.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-163">Functions are colored randomly.</span></span>  <span data-ttu-id="a3ec1-164">Нет корреляции с цветами, используемыми в других панелях.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="a3ec1-165">Однако функции всегда покрашены одинаково между вызовами, чтобы вы могли наблюдать шаблоны в каждом времени работы.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-165">However, functions are always colored the same across invocations so that you may observe patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Аннотированная диаграмма пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="a3ec1-167">Аннотированная диаграмма пламени</span><span class="sxs-lookup"><span data-stu-id="a3ec1-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a3ec1-168">Высокий стек вызовов не обязательно является значительным, это просто означает, что было вызвано множество функций.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="a3ec1-169">Но широкая планка означает, что для выполнения функции потребовалось много времени.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="a3ec1-170">Это кандидаты на оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-170">These are candidates for optimization.</span></span>  

### <a name="zoom-in-on-specific-parts-of-recording"></a><span data-ttu-id="a3ec1-171">Увеличение масштабирования определенных частей записи</span><span class="sxs-lookup"><span data-stu-id="a3ec1-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="a3ec1-172">Выберите, удерживайте и перетащите мышь влево и вправо по обзору, чтобы увеличить масштаб определенных частей стека вызовов.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-172">Choose, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="a3ec1-173">После масштабирования стек вызовов автоматически отображает часть выбранной записи.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Масштабирование диаграммы" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="a3ec1-175">Масштабирование диаграммы</span><span class="sxs-lookup"><span data-stu-id="a3ec1-175">Chart zoomed</span></span>  
:::image-end:::  

### <a name="view-function-details"></a><span data-ttu-id="a3ec1-176">Просмотр сведений о функциях</span><span class="sxs-lookup"><span data-stu-id="a3ec1-176">View function details</span></span>  

<span data-ttu-id="a3ec1-177">Выберите функцию для просмотра определения в панели **Источники.**</span><span class="sxs-lookup"><span data-stu-id="a3ec1-177">Choose a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="a3ec1-178">Наведите курсор на функцию, чтобы отобразить данные о времени и имени.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-178">Hover on a function to display the name and timing data.</span></span>  <span data-ttu-id="a3ec1-179">Ниже предоставляются следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-179">The following information is provided.</span></span>  

| <span data-ttu-id="a3ec1-180">Подробные</span><span class="sxs-lookup"><span data-stu-id="a3ec1-180">Detail</span></span> | <span data-ttu-id="a3ec1-181">Описание</span><span class="sxs-lookup"><span data-stu-id="a3ec1-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="a3ec1-182">Name</span><span class="sxs-lookup"><span data-stu-id="a3ec1-182">Name</span></span>** | <span data-ttu-id="a3ec1-183">Имя функции.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="a3ec1-184">Размер self</span><span class="sxs-lookup"><span data-stu-id="a3ec1-184">Self size</span></span>** | <span data-ttu-id="a3ec1-185">Размер текущего призыва функции, включая только утверждения в функции.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="a3ec1-186">Общий размер</span><span class="sxs-lookup"><span data-stu-id="a3ec1-186">Total size</span></span>** | <span data-ttu-id="a3ec1-187">Размер текущего призыва этой функции и всех функций, которые она называла.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="a3ec1-188">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="a3ec1-188">URL</span></span>** | <span data-ttu-id="a3ec1-189">Расположение определения функции в виде имени файла, в котором определена функция, и является номером `base.js:261` `base.js` `261` строки определения.</span><span class="sxs-lookup"><span data-stu-id="a3ec1-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Просмотр сведений о функциях на диаграмме" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="a3ec1-191">Просмотр сведений о функциях на диаграмме</span><span class="sxs-lookup"><span data-stu-id="a3ec1-191">View functions details in chart</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a3ec1-192">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a3ec1-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Справочные | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile — справочные ссылки на API для консоли | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd — справочные | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="a3ec1-196">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a3ec1-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a3ec1-197">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="a3ec1-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a3ec1-199">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a3ec1-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
