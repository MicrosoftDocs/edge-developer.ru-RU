---
description: Пользователи ожидают интерактивные и гладкие страницы.  Каждый этап конвейера пикселей представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность выполнения.
title: Анализ производительности выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398002"
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
   limitations under the License.  -->

# <a name="analyze-runtime-performance"></a><span data-ttu-id="8a8aa-106">Анализ производительности выполнения</span><span class="sxs-lookup"><span data-stu-id="8a8aa-106">Analyze runtime performance</span></span>  

<span data-ttu-id="8a8aa-107">Пользователи ожидают интерактивные и гладкие страницы.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="8a8aa-108">Каждый этап конвейера пикселей представляет возможность ввести jank.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="8a8aa-109">Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность выполнения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <a name="summary"></a><span data-ttu-id="8a8aa-110">Сводка</span><span class="sxs-lookup"><span data-stu-id="8a8aa-110">Summary</span></span>  

*   <span data-ttu-id="8a8aa-111">Не пишите JavaScript, который заставляет браузер пересчитывать макет.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="8a8aa-112">Разделяйте функции чтения и записи и выполните сначала чтение.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="8a8aa-113">Не усложняйте работу CSS.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="8a8aa-114">Используйте меньше CSS и сохраняйте простые селекторы CSS.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="8a8aa-115">Избегайте макета как можно больше.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="8a8aa-116">Выберите CSS, который вообще не запускает макет.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="8a8aa-117">Рисование может занять больше времени, чем любая другая отрисовка.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="8a8aa-118">Следите за узкими местами для краски.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-118">Watch out for paint bottlenecks.</span></span>  
    
## <a name="javascript"></a><span data-ttu-id="8a8aa-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="8a8aa-119">JavaScript</span></span>  

<span data-ttu-id="8a8aa-120">Вычисления JavaScript, особенно те, которые вызывают обширные визуальные изменения, могут привести к срыву производительности приложений.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="8a8aa-121">Не позволяйте вовремя или длительному JavaScript вмешиваться в взаимодействие пользователей.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <a name="javascript-tools"></a><span data-ttu-id="8a8aa-122">JavaScript: средства</span><span class="sxs-lookup"><span data-stu-id="8a8aa-122">JavaScript: Tools</span></span>  

<span data-ttu-id="8a8aa-123">Сними запись в **средстве Performance** и найми подозрительно длинные `Evaluate Script` события.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-123">Take a recording in the **Performance** tool and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="8a8aa-124">f. Вы заметь довольно много jank в JavaScript, возможно, потребуется взять анализ на следующий уровень и собрать профиль ЦП JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="8a8aa-125">Профили ЦП показывают, где время работы тратится в функциях страницы.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="8a8aa-126">Узнайте, как создавать профили ЦП в [режиме ускорения запуска JavaScript.][DevtoolsRenderingToolsJavascriptRuntime]</span><span class="sxs-lookup"><span data-stu-id="8a8aa-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <a name="javascript-problems"></a><span data-ttu-id="8a8aa-127">JavaScript: проблемы</span><span class="sxs-lookup"><span data-stu-id="8a8aa-127">JavaScript: Problems</span></span>  

<span data-ttu-id="8a8aa-128">В следующей таблице описаны некоторые распространенные проблемы JavaScript и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-128">The following table describes some common JavaScript problems and potential solutions.</span></span>  

| <span data-ttu-id="8a8aa-129">Проблема</span><span class="sxs-lookup"><span data-stu-id="8a8aa-129">Problem</span></span> | <span data-ttu-id="8a8aa-130">Пример</span><span class="sxs-lookup"><span data-stu-id="8a8aa-130">Example</span></span> | <span data-ttu-id="8a8aa-131">Решение</span><span class="sxs-lookup"><span data-stu-id="8a8aa-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8a8aa-132">Дорогие обработчики ввода, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-133">Сенсорный, параллакс прокрутки.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="8a8aa-134">Позвольте браузеру обрабатывать сенсорные и прокрутки или связывать слушателя как можно позже.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="8a8aa-135">Перейдите [к дорогим обработчикам ввода в][WebPerformanceCalendarRuntimeChecklist]контрольном списке производительности выполнения ПолОм Льюисом .</span><span class="sxs-lookup"><span data-stu-id="8a8aa-135">Navigate to [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="8a8aa-136">Плохо приурочная javaScript влияет на отклик, анимацию, загрузку.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="8a8aa-137">Пользователь прокручивает сразу после загрузки страницы setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="8a8aa-138">Оптимизация времени работы JavaScript: `requestAnimationFrame` использование, распространение манипуляций с DOM по кадрам, использование [веб-рабочих][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="8a8aa-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="8a8aa-139">Долгосрочный JavaScript, влияющий на отклик.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="8a8aa-140">Событие [DOMContentLoaded][MDNUsingWebWorkers] приостановилось, так как оно завалено работой JS.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="8a8aa-141">Перемещение чистой вычислительной работы на [веб-рабочих][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="8a8aa-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="8a8aa-142">Если вам нужен доступ к DOM, используйте `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="8a8aa-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="8a8aa-143">Сценарии garbage-y, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-144">Сбор мусора может происходить в любом месте.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="8a8aa-145">Записывая меньше сценариев с мусором.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="8a8aa-146">Перейдите к разделу Сбор мусора в анимации в контрольном списке производительности во время выполнения [Полом Льюисом.][WebPerformanceCalendarRuntimeChecklist]</span><span class="sxs-lookup"><span data-stu-id="8a8aa-146">Navigate to [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a><span data-ttu-id="8a8aa-147">Стиль</span><span class="sxs-lookup"><span data-stu-id="8a8aa-147">Style</span></span>  

<span data-ttu-id="8a8aa-148">Изменения стиля являются дорогостоящими, особенно если эти изменения затрагивают несколько элементов в DOM.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="8a8aa-149">Каждый раз, когда к элементу применяются стили, браузер высчитывает влияние на все связанные элементы, пересчитывает макет и перекетирует.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a><span data-ttu-id="8a8aa-150">Стиль: средства</span><span class="sxs-lookup"><span data-stu-id="8a8aa-150">Style: Tools</span></span>  

<span data-ttu-id="8a8aa-151">Запись в средстве **Performance.**</span><span class="sxs-lookup"><span data-stu-id="8a8aa-151">Take a recording in the **Performance** tool.</span></span>  <span data-ttu-id="8a8aa-152">Проверьте запись для больших `Recalculate Style` событий \(отображается в фиолетовом\).</span><span class="sxs-lookup"><span data-stu-id="8a8aa-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="8a8aa-153">Выберите `Recalculate Style` событие, чтобы просмотреть дополнительные сведения о нем в области **Details.**</span><span class="sxs-lookup"><span data-stu-id="8a8aa-153">Choose a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="8a8aa-154">Если изменения стиля забирают длительное время, это является хитом производительности.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="8a8aa-155">Если вычисления стилей влияют на большое количество элементов, это еще одна область, где есть возможности для улучшения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="8a8aa-157">Длинный стиль пересчета</span><span class="sxs-lookup"><span data-stu-id="8a8aa-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="8a8aa-158">Чтобы уменьшить влияние `Recalculate Style` событий:</span><span class="sxs-lookup"><span data-stu-id="8a8aa-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="8a8aa-159">Используйте [триггеры CSS,][CssTriggers] чтобы узнать, какие свойства CSS вызывают макет, краску и композит.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="8a8aa-160">Эти свойства оказывают самое сильное влияние на производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="8a8aa-161">Переключиться на свойства, которые имеют меньшее влияние.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-161">Switch to properties that have less impact.</span></span>  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a><span data-ttu-id="8a8aa-162">Стиль: проблемы</span><span class="sxs-lookup"><span data-stu-id="8a8aa-162">Style: Problems</span></span>  

<span data-ttu-id="8a8aa-163">В следующей таблице описаны некоторые распространенные проблемы стиля и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-163">The following table describes some common style problems and potential solutions.</span></span>  

| <span data-ttu-id="8a8aa-164">Проблема</span><span class="sxs-lookup"><span data-stu-id="8a8aa-164">Problem</span></span> | <span data-ttu-id="8a8aa-165">Пример</span><span class="sxs-lookup"><span data-stu-id="8a8aa-165">Example</span></span> | <span data-ttu-id="8a8aa-166">Решение</span><span class="sxs-lookup"><span data-stu-id="8a8aa-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8a8aa-167">Дорогостоящие вычисления стилей, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-168">Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или положение; браузер проверяет все остальные элементы и пересчитывает макет.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="8a8aa-169">Избегайте CSS, который запускает макеты</span><span class="sxs-lookup"><span data-stu-id="8a8aa-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="8a8aa-170">Сложные селекторы, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-171">Вложенные селекторы заставляют браузер знать все обо всех остальных элементах, включая родителей и детей.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="8a8aa-172">Ссылка на элемент в CSS только с классом.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a><span data-ttu-id="8a8aa-173">Макет</span><span class="sxs-lookup"><span data-stu-id="8a8aa-173">Layout</span></span>  

<span data-ttu-id="8a8aa-174">Макет (или переток в Firefox) — это процесс, при котором браузер вычисляет позиции и размеры всех элементов на странице.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="8a8aa-175">Модель макета веб-сайта означает, что один элемент может влиять на другие; например, ширина элемента, как правило, влияет на ширину любых детских элементов и так далее на всем протяжении `<body>` дерева.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="8a8aa-176">Этот процесс может быть достаточно вовлечен для браузера.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="8a8aa-177">Как правило, если вы попросите вернуть геометрическое значение из DOM до завершения кадра, вы найдете "принудительно синхронные макеты", что может быть большим узким местом производительности, если часто повторяться или выполняться для большого дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a><span data-ttu-id="8a8aa-178">Макет: средства</span><span class="sxs-lookup"><span data-stu-id="8a8aa-178">Layout: Tools</span></span>  

<span data-ttu-id="8a8aa-179">В **области Performance** определяется, когда страница вызывает принудительное синхронное расположение.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="8a8aa-180">Эти `Layout` события отмечены красными полосами.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Принудительное синхронное расположение" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="8a8aa-182">Принудительное синхронное расположение</span><span class="sxs-lookup"><span data-stu-id="8a8aa-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="8a8aa-183">"Обмывка макета" — это повторение условий принудительного синхронного макета.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="8a8aa-184">Это происходит, когда JavaScript пишет и читает из DOM несколько раз, что заставляет браузер пересчитать макет снова и снова.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="8a8aa-185">Чтобы определить обмыв макета, найди шаблон нескольких принудительных синхронных предупреждений макета.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="8a8aa-186">Просмотрите предыдущую фигуру.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-186">Review the previous figure.</span></span>  

### <a name="layout-problems"></a><span data-ttu-id="8a8aa-187">Макет: проблемы</span><span class="sxs-lookup"><span data-stu-id="8a8aa-187">Layout: Problems</span></span>  

<span data-ttu-id="8a8aa-188">В следующей таблице описаны некоторые распространенные проблемы макета и возможные решения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-188">The following table describes some common layout problems and potential solutions.</span></span>  

| <span data-ttu-id="8a8aa-189">Проблема</span><span class="sxs-lookup"><span data-stu-id="8a8aa-189">Problem</span></span> | <span data-ttu-id="8a8aa-190">Пример</span><span class="sxs-lookup"><span data-stu-id="8a8aa-190">Example</span></span> | <span data-ttu-id="8a8aa-191">Решение</span><span class="sxs-lookup"><span data-stu-id="8a8aa-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8a8aa-192">Принудительный синхронный макет, влияющий на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-193">Принуждение браузера к выполнению макета ранее в конвейере пикселей, что приводит к повторяемой процедуре отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="8a8aa-194">Пакет вашего стиля сначала читается, а затем записывает все записи.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-194">Batch your style reads first, then do any writes.</span></span>  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="8a8aa-195">Обмыв макета, влияющий на реакцию или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-196">Цикл, который помещает браузер в цикл чтения и чтения, заставляя браузер пересчитывать макет снова и снова.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="8a8aa-197">Автоматически пакетные операции чтения с помощью [библиотеки FastDom.][GitHubWilsonpageFastdom]</span><span class="sxs-lookup"><span data-stu-id="8a8aa-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a><span data-ttu-id="8a8aa-198">Краска и композит</span><span class="sxs-lookup"><span data-stu-id="8a8aa-198">Paint and composite</span></span>  

<span data-ttu-id="8a8aa-199">Paint — это процесс заполнения пикселей.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="8a8aa-200">Зачастую это самая затратная часть процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="8a8aa-201">Если вы заметили, что ваша страница не работает так, как задумано, вполне вероятно, что у вас есть проблемы с краской.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-201">If you noticed that your page is not working as designed in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="8a8aa-202">Композитизация — это то, где расписные части страницы сложены для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="8a8aa-203">По большей части, если придерживаться свойств только для композитора и вообще избегать краски, следует заметить значительное улучшение производительности, но необходимо следить за чрезмерными количествами уровней.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should notice a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a><span data-ttu-id="8a8aa-204">Краска и композитные: средства</span><span class="sxs-lookup"><span data-stu-id="8a8aa-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="8a8aa-205">Хотите узнать, сколько времени занимает рисование и как часто происходит рисование?</span><span class="sxs-lookup"><span data-stu-id="8a8aa-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="8a8aa-206">Проверьте параметр [Включить расширенный инструментарий для краски][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] в панели **Performance,** а затем сдайте запись.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="8a8aa-207">Если большая часть времени отрисовки отработана, возникают проблемы с краской.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a><span data-ttu-id="8a8aa-208">Краска и композитные: проблемы</span><span class="sxs-lookup"><span data-stu-id="8a8aa-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="8a8aa-209">В следующей таблице описаны некоторые распространенные проблемы с краской и композитными решениями.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-209">The following table describes some common paint and composite problems and potential solutions.</span></span>  

| <span data-ttu-id="8a8aa-210">Проблема</span><span class="sxs-lookup"><span data-stu-id="8a8aa-210">Problem</span></span> | <span data-ttu-id="8a8aa-211">Пример</span><span class="sxs-lookup"><span data-stu-id="8a8aa-211">Example</span></span> | <span data-ttu-id="8a8aa-212">Решение</span><span class="sxs-lookup"><span data-stu-id="8a8aa-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8a8aa-213">Краска штормов, влияющих на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-214">Большие области краски или дорогие краски, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="8a8aa-215">Избегайте краски, продвигая элементы, которые перемещаются в собственный слой, используйте преобразования и непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="8a8aa-216">Уровни взрывов, влияющих на анимации.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="8a8aa-217">Перепроизводства слишком многих элементов с `translateZ(0)` большим влиянием на производительность анимации.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="8a8aa-218">Продвигать в слои экономно, и только тогда, когда вы знаете, он предлагает ощутимые улучшения.</span><span class="sxs-lookup"><span data-stu-id="8a8aa-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8a8aa-219">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8a8aa-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение времени работы JavaScript | Документы Майкрософт"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Включаем расширенный инструментарий краски - справочные ссылки на анализ производительности | Документы Майкрософт"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Триггеры CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-| MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности выполнения — веб-календарь производительности"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="8a8aa-226">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a8aa-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8a8aa-227">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="8a8aa-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8a8aa-229">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a8aa-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
