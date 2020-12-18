---
description: Пользователи ожидают интерактивные и плавные страницы.  Каждая стадия в пиксельном конвейере представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность во время выполнения.
title: Анализ производительности в времени выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d42ac5e7a7456971d48198a1f362eebe7156bbce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230609"
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

# <span data-ttu-id="bc734-106">Анализ производительности в времени выполнения</span><span class="sxs-lookup"><span data-stu-id="bc734-106">Analyze runtime performance</span></span> 

<span data-ttu-id="bc734-107">Пользователи ожидают интерактивные и плавные страницы.</span><span class="sxs-lookup"><span data-stu-id="bc734-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="bc734-108">Каждая стадия в пиксельном конвейере представляет возможность ввести jank.</span><span class="sxs-lookup"><span data-stu-id="bc734-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="bc734-109">Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bc734-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="bc734-110">Сводка</span><span class="sxs-lookup"><span data-stu-id="bc734-110">Summary</span></span>  

*   <span data-ttu-id="bc734-111">Не пишите JavaScript, который заставляет браузер пересчитывать макет.</span><span class="sxs-lookup"><span data-stu-id="bc734-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="bc734-112">Разделяйте функции чтения и записи, а затем выполните чтение.</span><span class="sxs-lookup"><span data-stu-id="bc734-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="bc734-113">Не усложняйте CSS.</span><span class="sxs-lookup"><span data-stu-id="bc734-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="bc734-114">Используйте меньше CSS и сохраняйте простоты селекторов CSS.</span><span class="sxs-lookup"><span data-stu-id="bc734-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="bc734-115">Избегайте максимально возможного макета.</span><span class="sxs-lookup"><span data-stu-id="bc734-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="bc734-116">Выберите CSS,который вообще не активирует макет.</span><span class="sxs-lookup"><span data-stu-id="bc734-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="bc734-117">Рисование может занять больше времени, чем любое другое действие отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bc734-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="bc734-118">Следите за узкими местами для кисок.</span><span class="sxs-lookup"><span data-stu-id="bc734-118">Watch out for paint bottlenecks.</span></span>  
    
## <span data-ttu-id="bc734-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="bc734-119">JavaScript</span></span>  

<span data-ttu-id="bc734-120">Вычисления JavaScript, особенно те, которые вызывают существенные визуальные изменения, могут привести к застою производительности приложения.</span><span class="sxs-lookup"><span data-stu-id="bc734-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="bc734-121">Не мешайте взаимодействию с пользователем с помощью JavaScript во время неудалась или длительной работы.</span><span class="sxs-lookup"><span data-stu-id="bc734-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="bc734-122">JavaScript: средства</span><span class="sxs-lookup"><span data-stu-id="bc734-122">JavaScript: Tools</span></span>  

<span data-ttu-id="bc734-123">Сформуйте запись на панели **"Производительность"** и наймите подозрительные длинные `Evaluate Script` события.</span><span class="sxs-lookup"><span data-stu-id="bc734-123">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="bc734-124">F вы знаете, что в JavaScript достаточно много jank, возможно, вам потребуется оказаться на следующем уровне анализа и собрать профиль ЦП JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc734-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="bc734-125">Профили ЦП показывают, где время работы затрачено на функции страницы.</span><span class="sxs-lookup"><span data-stu-id="bc734-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="bc734-126">Узнайте, как создавать профили ЦП в [среде запуска JavaScript.][DevtoolsRenderingToolsJavascriptRuntime]</span><span class="sxs-lookup"><span data-stu-id="bc734-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="bc734-127">JavaScript: проблемы</span><span class="sxs-lookup"><span data-stu-id="bc734-127">JavaScript: Problems</span></span>  

<span data-ttu-id="bc734-128">В следующей таблице описываются некоторые распространенные проблемы JavaScript и возможные решения:</span><span class="sxs-lookup"><span data-stu-id="bc734-128">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="bc734-129">Проблема</span><span class="sxs-lookup"><span data-stu-id="bc734-129">Problem</span></span> | <span data-ttu-id="bc734-130">Пример.</span><span class="sxs-lookup"><span data-stu-id="bc734-130">Example</span></span> | <span data-ttu-id="bc734-131">Решение</span><span class="sxs-lookup"><span data-stu-id="bc734-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bc734-132">Дорогостоящие обработчики ввода, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="bc734-133">Касание, параллакс прокрутка.</span><span class="sxs-lookup"><span data-stu-id="bc734-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="bc734-134">Разрешите браузеру обрабатывать касание и прокрутку или привязывать прослушиватель как можно позднее.</span><span class="sxs-lookup"><span data-stu-id="bc734-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="bc734-135">См. контрольный список производительности во время выполнения пользователя PaulСвойла (PaulСвойл) с дорогими [обработчиками входных данных.][WebPerformanceCalendarRuntimeChecklist]</span><span class="sxs-lookup"><span data-stu-id="bc734-135">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="bc734-136">JavaScript с плохой временем, влияющий на отклик, анимацию, загрузку.</span><span class="sxs-lookup"><span data-stu-id="bc734-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="bc734-137">Пользователь прокручивает страницу сразу после загрузки, setTimeout / setInterval.</span><span class="sxs-lookup"><span data-stu-id="bc734-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="bc734-138">Оптимизация времени работы JavaScript: `requestAnimationFrame` использование, распространение манипуляций DOM по кадрам, использование [веб-работников.][MDNUsingWebWorkers]</span><span class="sxs-lookup"><span data-stu-id="bc734-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="bc734-139">Долгосрочный JavaScript, влияющий на отклик.</span><span class="sxs-lookup"><span data-stu-id="bc734-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="bc734-140">Событие [DOMContentLoaded][MDNUsingWebWorkers] заглохает, так как оно совмещается с работой JS.</span><span class="sxs-lookup"><span data-stu-id="bc734-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="bc734-141">Перемещайте чисто вычислительные трудоемкие работы [в веб-работники.][MDNUsingWebWorkers]</span><span class="sxs-lookup"><span data-stu-id="bc734-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="bc734-142">Если вам нужен доступ к DOM, используйте `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="bc734-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="bc734-143">Сценарии сборки мусора, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="bc734-144">Сборка мусора может происходить где угодно.</span><span class="sxs-lookup"><span data-stu-id="bc734-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="bc734-145">Напишите меньше скриптов сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="bc734-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="bc734-146">См. контрольный список производительности сборки мусора в анимации в списке производительности [во время выполнения полю ПолОмА ( PaulСвой).][WebPerformanceCalendarRuntimeChecklist]</span><span class="sxs-lookup"><span data-stu-id="bc734-146">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="bc734-147">Стиль</span><span class="sxs-lookup"><span data-stu-id="bc734-147">Style</span></span>  

<span data-ttu-id="bc734-148">Изменение стиля является дорогостоящим, особенно если эти изменения влияют на несколько элементов в DOM.</span><span class="sxs-lookup"><span data-stu-id="bc734-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="bc734-149">Каждый раз, когда вы применяли стили к элементу, браузер вычисляет влияние на все связанные элементы, пересчитывает макет и перерасчеты.</span><span class="sxs-lookup"><span data-stu-id="bc734-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="bc734-150">Стиль: средства</span><span class="sxs-lookup"><span data-stu-id="bc734-150">Style: Tools</span></span>  

<span data-ttu-id="bc734-151">Запись на панели **"Производительность".**</span><span class="sxs-lookup"><span data-stu-id="bc734-151">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="bc734-152">Проверьте запись на большие `Recalculate Style` события \(отображаются в сиреневом цвете\).</span><span class="sxs-lookup"><span data-stu-id="bc734-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="bc734-153">Щелкните `Recalculate Style` событие, чтобы \*\*\*\* просмотреть дополнительные сведения о нем в области сведений.</span><span class="sxs-lookup"><span data-stu-id="bc734-153">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="bc734-154">Если изменение стиля забирает много времени, это будет множать производительность.</span><span class="sxs-lookup"><span data-stu-id="bc734-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="bc734-155">Если вычисления стиля влияют на большое количество элементов, это еще одна область с местом для улучшения.</span><span class="sxs-lookup"><span data-stu-id="bc734-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="bc734-157">Длинный стиль пересчета</span><span class="sxs-lookup"><span data-stu-id="bc734-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="bc734-158">Чтобы уменьшить влияние `Recalculate Style` событий:</span><span class="sxs-lookup"><span data-stu-id="bc734-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="bc734-159">Используйте [триггеры CSS,][CssTriggers] чтобы узнать, какие свойства CSS активирует макет, paint и составные.</span><span class="sxs-lookup"><span data-stu-id="bc734-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="bc734-160">Эти свойства оказывают наихудшее влияние на производительность отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bc734-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="bc734-161">Переключиться на свойства, которые имеют меньшее влияние.</span><span class="sxs-lookup"><span data-stu-id="bc734-161">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="bc734-162">Стиль: проблемы</span><span class="sxs-lookup"><span data-stu-id="bc734-162">Style: Problems</span></span>  

<span data-ttu-id="bc734-163">В следующей таблице описаны некоторые распространенные проблемы со стилем и возможные решения:</span><span class="sxs-lookup"><span data-stu-id="bc734-163">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="bc734-164">Проблема</span><span class="sxs-lookup"><span data-stu-id="bc734-164">Problem</span></span> | <span data-ttu-id="bc734-165">Пример.</span><span class="sxs-lookup"><span data-stu-id="bc734-165">Example</span></span> | <span data-ttu-id="bc734-166">Решение</span><span class="sxs-lookup"><span data-stu-id="bc734-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bc734-167">Затратные вычисления стиля, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="bc734-168">Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или положение; Браузер проверяет все остальные элементы и пересчитает макет.</span><span class="sxs-lookup"><span data-stu-id="bc734-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="bc734-169">Избегайте CSS- инициирует макеты</span><span class="sxs-lookup"><span data-stu-id="bc734-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="bc734-170">Сложные селекторы, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="bc734-171">Вложенные селекторы принудительно должны знать браузер обо всех остальных элементах, включая родителей и детей.</span><span class="sxs-lookup"><span data-stu-id="bc734-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="bc734-172">Ссылаться на элемент в CSS можно только с помощью класса.</span><span class="sxs-lookup"><span data-stu-id="bc734-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="bc734-173">Макет</span><span class="sxs-lookup"><span data-stu-id="bc734-173">Layout</span></span>  

<span data-ttu-id="bc734-174">Макет (или перенабор в Firefox) — это процесс, с помощью которого браузер вычисляет положение и размеры всех элементов на странице.</span><span class="sxs-lookup"><span data-stu-id="bc734-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="bc734-175">Модель макета в Интернете означает, что один элемент может повлиять на других; например, ширина элемента обычно влияет на ширину любых потомков и так далее, в любом случае вверх и `<body>` вниз по дереву.</span><span class="sxs-lookup"><span data-stu-id="bc734-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="bc734-176">Этот процесс может быть довольно сложной для браузера.</span><span class="sxs-lookup"><span data-stu-id="bc734-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="bc734-177">Как правило, если вы запросите геометрическое значение из DOM до завершения фрейма, вы найдете "принудительно синхронные макеты", что может быть большим узким местом производительности, если он повторяется часто или выполняется для большого дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="bc734-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="bc734-178">Макет: средства</span><span class="sxs-lookup"><span data-stu-id="bc734-178">Layout: Tools</span></span>  

<span data-ttu-id="bc734-179">В **области** "Производительность" указывается, когда страница вызывает принудительные синхронные макеты.</span><span class="sxs-lookup"><span data-stu-id="bc734-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="bc734-180">Эти `Layout` события помечаются красными полосами.</span><span class="sxs-lookup"><span data-stu-id="bc734-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Принудительный синхронный макет" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="bc734-182">Принудительный синхронный макет</span><span class="sxs-lookup"><span data-stu-id="bc734-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="bc734-183">"Раскладка макета" — это повторение принудительно синхронных условий макета.</span><span class="sxs-lookup"><span data-stu-id="bc734-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="bc734-184">Это происходит, когда JavaScript несколько раз записывает и считывает из DOM, что заставляет браузер пересчитать макет снова и снова.</span><span class="sxs-lookup"><span data-stu-id="bc734-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="bc734-185">Чтобы определить разметку макета, найди шаблон нескольких принудительных предупреждений о синхронном макете.</span><span class="sxs-lookup"><span data-stu-id="bc734-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="bc734-186">См. предыдущий рисунок.</span><span class="sxs-lookup"><span data-stu-id="bc734-186">See the previous figure.</span></span>  

### <span data-ttu-id="bc734-187">Макет: проблемы</span><span class="sxs-lookup"><span data-stu-id="bc734-187">Layout: Problems</span></span>  

<span data-ttu-id="bc734-188">В следующей таблице описываются некоторые распространенные проблемы с макетом и возможные решения:</span><span class="sxs-lookup"><span data-stu-id="bc734-188">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="bc734-189">Проблема</span><span class="sxs-lookup"><span data-stu-id="bc734-189">Problem</span></span> | <span data-ttu-id="bc734-190">Пример.</span><span class="sxs-lookup"><span data-stu-id="bc734-190">Example</span></span> | <span data-ttu-id="bc734-191">Решение</span><span class="sxs-lookup"><span data-stu-id="bc734-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bc734-192">Принудительный синхронный макет, влияющий на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="bc734-193">Принудительным выполнением макета браузером ранее в пиксельном конвейере, что приводит к повторяемой процедуре отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bc734-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="bc734-194">Сначала пакетное чтение в стиле, а затем любые записи.</span><span class="sxs-lookup"><span data-stu-id="bc734-194">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="bc734-195">Thrashing макета, влияющий на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="bc734-196">Цикл, который помещает браузер в цикл чтения-записи и чтения-записи, заставляет браузер пересчитывать макет снова и снова.</span><span class="sxs-lookup"><span data-stu-id="bc734-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="bc734-197">Автоматически пакетные операции чтения и записи с помощью [библиотеки FastDom.][GitHubWilsonpageFastdom]</span><span class="sxs-lookup"><span data-stu-id="bc734-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="bc734-198">Paint и composite</span><span class="sxs-lookup"><span data-stu-id="bc734-198">Paint and composite</span></span>  

<span data-ttu-id="bc734-199">Paint — это процесс заполнения пикселей.</span><span class="sxs-lookup"><span data-stu-id="bc734-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="bc734-200">Зачастую это наиболее затратная часть процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bc734-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="bc734-201">Если вы заметили, что страница в любом случае неуявная, скорее всего, у вас возникнут проблемы с киской.</span><span class="sxs-lookup"><span data-stu-id="bc734-201">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="bc734-202">Композитные части страницы помещаются вместе для отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="bc734-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="bc734-203">В большинстве случае, если вы не хотите использовать свойства только компонатора и не хотите использовать кисть, производительность должна существенно улучшиться, но следует избегать чрезмерного количества уровней.</span><span class="sxs-lookup"><span data-stu-id="bc734-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="bc734-204">Paint и composite: Tools</span><span class="sxs-lookup"><span data-stu-id="bc734-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="bc734-205">Хотите узнать, сколько времени занимает рисование или как часто происходит рисование?</span><span class="sxs-lookup"><span data-stu-id="bc734-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="bc734-206">Проверьте параметр ["Включить расширенный инструментарий paint"][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] на панели **"Производительность",** а затем с помощью записи.</span><span class="sxs-lookup"><span data-stu-id="bc734-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="bc734-207">Если большая часть времени отрисовки потрачена на рисование, возникают проблемы с рисованием.</span><span class="sxs-lookup"><span data-stu-id="bc734-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="bc734-208">Paint и composite: проблемы</span><span class="sxs-lookup"><span data-stu-id="bc734-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="bc734-209">В следующей таблице описываются некоторые распространенные проблемы с paint и составными решениями, а также возможные решения:</span><span class="sxs-lookup"><span data-stu-id="bc734-209">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="bc734-210">Проблема</span><span class="sxs-lookup"><span data-stu-id="bc734-210">Problem</span></span> | <span data-ttu-id="bc734-211">Пример.</span><span class="sxs-lookup"><span data-stu-id="bc734-211">Example</span></span> | <span data-ttu-id="bc734-212">Решение</span><span class="sxs-lookup"><span data-stu-id="bc734-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bc734-213">Нарисуются ливня, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="bc734-214">Большие области киок или дорогостоящие кинты, влияющие на отклик или анимацию.</span><span class="sxs-lookup"><span data-stu-id="bc734-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="bc734-215">Избегайте использования кисти, рекламы элементов, которые перемещаются на собственный уровень, используйте преобразования и прозрачность.</span><span class="sxs-lookup"><span data-stu-id="bc734-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="bc734-216">Уровни, влияющие на анимации.</span><span class="sxs-lookup"><span data-stu-id="bc734-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="bc734-217">Чрезмерное количество элементов с большим `translateZ(0)` влиянием на производительность анимации.</span><span class="sxs-lookup"><span data-stu-id="bc734-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="bc734-218">Повышение до уровней экономно и только в том случае, если вы знаете, что он предлагает существенные улучшения.</span><span class="sxs-lookup"><span data-stu-id="bc734-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <span data-ttu-id="bc734-219">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bc734-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение времени работы JavaScript | Документы Майкрософт"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Включить расширенный инструментарий paint — справочник по анализу производительности | Документы Майкрософт"

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

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-работников | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности в времени выполнения — календарь производительности веб-сайтов"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="bc734-226">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bc734-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bc734-227">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="bc734-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bc734-229">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bc734-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
