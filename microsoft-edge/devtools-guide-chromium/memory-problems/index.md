---
description: Узнайте, как использовать Microsoft Edge и DevTools для поиска проблем с памятью, влияющих на производительность страниц, включая утечки памяти, раздутую память и частые сборы мусора.
title: Устранение проблем с памятью
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: afaea8ca561bd975490d9153cda40877786a0f08
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397834"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="fix-memory-problems"></a><span data-ttu-id="3d33f-104">Устранение проблем с памятью</span><span class="sxs-lookup"><span data-stu-id="3d33f-104">Fix memory problems</span></span>  

<span data-ttu-id="3d33f-105">Узнайте, как использовать Microsoft Edge и DevTools для поиска проблем с памятью, влияющих на производительность страниц, включая утечки памяти, раздутую память и частые сборы мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <a name="summary"></a><span data-ttu-id="3d33f-106">Сводка</span><span class="sxs-lookup"><span data-stu-id="3d33f-106">Summary</span></span>  

*   <span data-ttu-id="3d33f-107">Узнайте, сколько памяти в настоящее время используется на странице с помощью диспетчера задач браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d33f-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="3d33f-108">Визуализация использования памяти с течением времени с помощью **панели памяти.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="3d33f-109">Определите отдельные деревья DOM \(распространенная причина утечки памяти\) с помощью **снимка кучи.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="3d33f-110">Узнайте, когда новая память выделяется в кучи JavaScript \(JS кучи\) с помощью инструментов **распределения на временной шкале.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <a name="overview"></a><span data-ttu-id="3d33f-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="3d33f-111">Overview</span></span>  

<span data-ttu-id="3d33f-112">В духе модели **производительности RAIL** в центре внимания ваших усилий по производительности должны быть ваши пользователи.</span><span class="sxs-lookup"><span data-stu-id="3d33f-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="3d33f-113">Проблемы с памятью важны, так как они часто воспринимаются пользователями.</span><span class="sxs-lookup"><span data-stu-id="3d33f-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="3d33f-114">Пользователи могут воспринимать проблемы с памятью следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d33f-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="3d33f-115">**Производительность страницы со временем ухудшается.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="3d33f-116">Возможно, это симптом утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="3d33f-117">Утечка памяти — это когда ошибка на странице приводит к постепенному использованию с течением времени все большего и большего объемов памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="3d33f-118">**Производительность страницы стабильно плохая.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="3d33f-119">Возможно, это симптом раздува памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="3d33f-120">Раздутие памяти — это когда на странице используется больше памяти, чем необходимо для оптимальной скорости страницы.</span><span class="sxs-lookup"><span data-stu-id="3d33f-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="3d33f-121">**Производительность страницы задерживается**или часто останавливается.</span><span class="sxs-lookup"><span data-stu-id="3d33f-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="3d33f-122">Возможно, это симптом частых сборов мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="3d33f-123">Сбор мусора — это когда браузер возвращает память.</span><span class="sxs-lookup"><span data-stu-id="3d33f-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="3d33f-124">Браузер решает, когда это произойдет.</span><span class="sxs-lookup"><span data-stu-id="3d33f-124">The browser decides when this happens.</span></span>  <span data-ttu-id="3d33f-125">Во время коллекций приостановка работы всех скриптов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="3d33f-126">Так что если браузер собирает много мусора, время запуска скрипта будет приостановлено много.</span><span class="sxs-lookup"><span data-stu-id="3d33f-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <a name="memory-bloat-how-much-is-too-much"></a><span data-ttu-id="3d33f-127">Раздув памяти: сколько "слишком много"?</span><span class="sxs-lookup"><span data-stu-id="3d33f-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="3d33f-128">Утечку памяти легко определить.</span><span class="sxs-lookup"><span data-stu-id="3d33f-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="3d33f-129">Если сайт постепенно использует все больше и больше памяти, то у вас есть утечка.</span><span class="sxs-lookup"><span data-stu-id="3d33f-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="3d33f-130">Но раздуть память немного сложнее прикрепить.</span><span class="sxs-lookup"><span data-stu-id="3d33f-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="3d33f-131">Что квалифицируется как "использование слишком емких воспоминаний"?</span><span class="sxs-lookup"><span data-stu-id="3d33f-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="3d33f-132">Здесь нет жестких номеров, так как различные устройства и браузеры имеют различные возможности.</span><span class="sxs-lookup"><span data-stu-id="3d33f-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="3d33f-133">Та же страница, которая плавно выполняется на смартфоне высокого уровня, может привести к сбою на низком уровне смартфона.</span><span class="sxs-lookup"><span data-stu-id="3d33f-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="3d33f-134">Здесь важно использовать модель RAIL и сосредоточиться на пользователях.</span><span class="sxs-lookup"><span data-stu-id="3d33f-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="3d33f-135">Узнайте, какие устройства популярны у пользователей, а затем проверьте свою страницу на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="3d33f-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="3d33f-136">При последовательном плохом опыте на странице могут быть превышены возможности памяти этих устройств.</span><span class="sxs-lookup"><span data-stu-id="3d33f-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a><span data-ttu-id="3d33f-137">Мониторинг использования памяти в режиме реального времени с помощью диспетчера задач браузера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d33f-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="3d33f-138">Используйте диспетчер задач браузера Microsoft Edge в качестве отправной точки для расследования проблемы памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="3d33f-139">Диспетчер задач браузера Microsoft Edge — это монитор реального времени, который сообщает, сколько памяти используется на странице в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="3d33f-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="3d33f-140">Выберите `Shift` + `Esc` или перейдите в основное \*\*\*\* меню Microsoft Edge и выберите Дополнительные средства Browser Task Manager для открытия диспетчера задач браузера  >  \*\*\*\* Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3d33f-140">Select `Shift`+`Esc` or navigate to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Открытие диспетчера задач браузера Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="3d33f-142">Рис. 1. Открытие диспетчера задач браузера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d33f-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3d33f-143">Наведите курсор на заглавную таблицу диспетчера задач браузера Microsoft Edge, откройте контекстное меню \(правой кнопкой мыши\) и введите **память JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="3d33f-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Включить память JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="3d33f-145">Рис. 2. Включить память JavaScript</span><span class="sxs-lookup"><span data-stu-id="3d33f-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3d33f-146">В этих двух столбцах вы можете рассказать о том, как ваша страница использует память.</span><span class="sxs-lookup"><span data-stu-id="3d33f-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="3d33f-147">Столбец **Memory** представляет родной памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="3d33f-148">Узлы DOM хранятся в родной памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="3d33f-149">Если это значение увеличивается, создаются узлы DOM.</span><span class="sxs-lookup"><span data-stu-id="3d33f-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="3d33f-150">Столбец **Памяти JavaScript** представляет кучу JS.</span><span class="sxs-lookup"><span data-stu-id="3d33f-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="3d33f-151">Этот столбец содержит два значения.</span><span class="sxs-lookup"><span data-stu-id="3d33f-151">This column contains two values.</span></span>  <span data-ttu-id="3d33f-152">Вас интересует живой номер \(число в скобках\).</span><span class="sxs-lookup"><span data-stu-id="3d33f-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="3d33f-153">Живой номер представляет, сколько памяти используют объекты, достигаемые на странице.</span><span class="sxs-lookup"><span data-stu-id="3d33f-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="3d33f-154">Если это число увеличивается, создаются либо новые объекты, либо растут существующие объекты.</span><span class="sxs-lookup"><span data-stu-id="3d33f-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a><span data-ttu-id="3d33f-155">Визуализация утечек памяти с помощью панели Performance</span><span class="sxs-lookup"><span data-stu-id="3d33f-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="3d33f-156">Вы также можете использовать панель Performance в качестве еще одной отправной точки в вашем расследовании.</span><span class="sxs-lookup"><span data-stu-id="3d33f-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="3d33f-157">Панель Performance позволяет со временем визуализировать использование страницы в памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="3d33f-158">Откройте панель **Performance** на DevTools.</span><span class="sxs-lookup"><span data-stu-id="3d33f-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="3d33f-159">Включить **почтовый** ящик памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="3d33f-160">[Запись.][DevtoolsEvaluatePerformanceReferenceRecord]</span><span class="sxs-lookup"><span data-stu-id="3d33f-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="3d33f-161">Это хорошая практика, чтобы начать и закончить запись с принудительного сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="3d33f-162">Для принудительного сбора мусора выберите кнопку **сбора** мусора во время ![ ][ImageForceGarbageCollectionIcon] записи.</span><span class="sxs-lookup"><span data-stu-id="3d33f-162">To force garbage collection, choose the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording.</span></span>  

<span data-ttu-id="3d33f-163">Чтобы продемонстрировать записи памяти, рассмотрим ниже код:</span><span class="sxs-lookup"><span data-stu-id="3d33f-163">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="3d33f-164">Каждый раз, когда выбрана кнопка, на которую ссылается код, к тексту документа примыкают 10 тысяч узлов, а на массив выталкивали строку из одного `div` `x` миллиона `x` символов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-164">Every time that the button referenced in the code is chosen, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="3d33f-165">При запуске предыдущего примера кода создается запись в панели **Performance,** как на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="3d33f-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Простой рост" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="3d33f-167">Рис. 3. Простой рост</span><span class="sxs-lookup"><span data-stu-id="3d33f-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="3d33f-168">Во-первых, объяснение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3d33f-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="3d33f-169">Граф **HEAP** в области **Обзор** \(ниже **NET**\) представляет кучу JS.</span><span class="sxs-lookup"><span data-stu-id="3d33f-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="3d33f-170">Ниже области **Обзор** является области **Счетчик.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="3d33f-171">Использование памяти разбивается по Кучи JS \(так же, как график **HEAP** в области Обзор\), документов, узлов DOM, слушателей и памяти GPU. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3d33f-171">The memory usage is broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="3d33f-172">Выключите почтовый ящик, чтобы скрыть его от графа.</span><span class="sxs-lookup"><span data-stu-id="3d33f-172">Turn off a checkbox to hide it from the graph.</span></span>  

<span data-ttu-id="3d33f-173">Теперь анализ кода по сравнению с предыдущим рисунком.</span><span class="sxs-lookup"><span data-stu-id="3d33f-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="3d33f-174">Если вы просмотрите счетчик узла \(зеленый график\), он будет полностью совпадать с кодом.</span><span class="sxs-lookup"><span data-stu-id="3d33f-174">If you review the node counter \(the green graph\), it matches up cleanly with the code.</span></span>  <span data-ttu-id="3d33f-175">Количество узлов увеличивается в дискретных шагах.</span><span class="sxs-lookup"><span data-stu-id="3d33f-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="3d33f-176">Можно предположить, что каждое увеличение числа узлов является вызовом `grow()` .</span><span class="sxs-lookup"><span data-stu-id="3d33f-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="3d33f-177">График Кучи JS \(синий график\) не так прост.</span><span class="sxs-lookup"><span data-stu-id="3d33f-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="3d33f-178">В соответствии с лучшими практиками, первый провал фактически является \*\*\*\* принудительной коллекцией мусора \(выберите кнопку сбора мусора ![ принудительного ][ImageForceGarbageCollectionIcon] сбора мусора\).</span><span class="sxs-lookup"><span data-stu-id="3d33f-178">In keeping with best practices, the first dip is actually a forced garbage collection \(choose the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="3d33f-179">По мере выполнения записи отображаются пики размера Кучи JS.</span><span class="sxs-lookup"><span data-stu-id="3d33f-179">As the recording progresses, the JS heap size spikes are displayed.</span></span>  <span data-ttu-id="3d33f-180">Это естественно и ожидаемо: код JavaScript создает узлы DOM на каждой кнопке, вы выбираете, и много работы при создании строки из одного миллиона символов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button you choose and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="3d33f-181">Ключевым моментом здесь является тот факт, что куча JS заканчивается выше, чем она началась \(здесь "начало" является точкой после принудительного сбора мусора\).</span><span class="sxs-lookup"><span data-stu-id="3d33f-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="3d33f-182">В реальном мире, если вы увидели этот шаблон увеличения размера или размера узла Кучи JS, это может потенциально определить утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a><span data-ttu-id="3d33f-183">Обнаружение отсоединяемой памяти дерева DOM с помощью снимков кучи</span><span class="sxs-lookup"><span data-stu-id="3d33f-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="3d33f-184">Узел DOM — это только мусор, собираемый, если на странице нет ссылок на узел из дерева DOM или кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3d33f-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="3d33f-185">Сообщается, что узел "отсоединяется" при удалении из дерева DOM, но некоторые JavaScript по-прежнему ссылаются на него.</span><span class="sxs-lookup"><span data-stu-id="3d33f-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="3d33f-186">Отдельные узлы DOM являются распространенной причиной утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="3d33f-187">В этом разделе рассказывается об использовании профилей кучи в DevTools для определения отсоединяемых узлов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="3d33f-188">Вот простой пример отсоединяемых узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="3d33f-188">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="3d33f-189">Выбор кнопки, на которая ссылается в коде, создает `ul` узел с десятью `li` детьми.</span><span class="sxs-lookup"><span data-stu-id="3d33f-189">Choosing the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="3d33f-190">Узлы ссылаются на код, но не существуют в дереве DOM, поэтому каждый из них отсоединяется.</span><span class="sxs-lookup"><span data-stu-id="3d33f-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="3d33f-191">Снимки кучи — это один из способов определения отсоединяемых узлов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="3d33f-192">Как следует из названия, на снимках кучи покажите, как память распределяется между объектами JS и узлами DOM для вашей страницы в момент момент снимка.</span><span class="sxs-lookup"><span data-stu-id="3d33f-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="3d33f-193">Чтобы создать снимок, откройте DevTools \*\*\*\* и перейдите \*\*\*\* к панели памяти, выберите кнопку "Моментальный снимок" > **Снимок.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-193">To create a snapshot, open DevTools and navigate to the **Memory** panel, choose the **Heap snapshot** radio button > **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Снимок кучи" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="3d33f-195">Рис. 4. Снимок кучи</span><span class="sxs-lookup"><span data-stu-id="3d33f-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="3d33f-196">На обработку и загрузку снимка может потребоваться некоторое время.</span><span class="sxs-lookup"><span data-stu-id="3d33f-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="3d33f-197">После его завершения выберите его из левой панели \(с именем **HEAP SNAPSHOTS**\).</span><span class="sxs-lookup"><span data-stu-id="3d33f-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="3d33f-198">`Detached`Введите **текстовый ящик фильтра** класса для поиска отсоединяемого дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="3d33f-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Фильтрация для отсоединяющихся узлов" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="3d33f-200">Рис. 5. Фильтрация для отсоединяющихся узлов</span><span class="sxs-lookup"><span data-stu-id="3d33f-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="3d33f-201">Расширь карат, чтобы исследовать отдельное дерево.</span><span class="sxs-lookup"><span data-stu-id="3d33f-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Исследование отдельного дерева" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="3d33f-203">Рис. 6. Изучение отдельного дерева</span><span class="sxs-lookup"><span data-stu-id="3d33f-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="3d33f-204">Выберите узел для дальнейшего изучения.</span><span class="sxs-lookup"><span data-stu-id="3d33f-204">Choose a node to investigate it further.</span></span>  <span data-ttu-id="3d33f-205">В области **Объекты** можно просмотреть дополнительные сведения о коде, который ссылается на него.</span><span class="sxs-lookup"><span data-stu-id="3d33f-205">In the **Objects** pane, you may review more information about the code that is referencing it.</span></span>  <span data-ttu-id="3d33f-206">Например, на следующем рисунке переменная `detachedNodes` ссылаться на узел.</span><span class="sxs-lookup"><span data-stu-id="3d33f-206">For example, in the following figure, the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="3d33f-207">Чтобы устранить определенную утечку памяти, необходимо изучить код, использующий переменную, и убедиться, что ссылка на узел удаляется, когда она больше `detachedUNode` не требуется.</span><span class="sxs-lookup"><span data-stu-id="3d33f-207">To fix the particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Исследование узла" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="3d33f-209">Рис. 7. Исследование узла</span><span class="sxs-lookup"><span data-stu-id="3d33f-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a><span data-ttu-id="3d33f-210">Определение утечек памяти JS с помощью инструментов распределения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="3d33f-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="3d33f-211">**Инструментирование распределения на временной шкале** — это еще один инструмент, который может помочь вам отслеживать утечки памяти в кучи JS.</span><span class="sxs-lookup"><span data-stu-id="3d33f-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="3d33f-212">Демонстрация **инструментов распределения на временной шкале**  с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="3d33f-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="3d33f-213">При каждом нажатии кнопки, на которую ссылается код, в массив добавляется строка из одного миллиона `x` символов.</span><span class="sxs-lookup"><span data-stu-id="3d33f-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="3d33f-214">Чтобы записать приборы распределения на временной шкале, откройте \*\*\*\* DevTools, перейдите к панели памяти, выберите инструменты распределения на кнопке радиохронологии, \*\*\*\* выберите кнопку Начните, выполните действия, которые, как вы подозреваете, вызывают утечку памяти, а затем выберите кнопку остановки записи профиля Стоп записи профиля стоп-записи. \*\*\*\* \*\*\*\* ![ ][ImageStopRecordingIcon]</span><span class="sxs-lookup"><span data-stu-id="3d33f-214">To record an Allocation instrumentation on timeline, open DevTools, navigate to the **Memory** panel, choose the **Allocation instrumentation on timeline** radio button, choose the **Start** button, perform the action that you suspect is causing the memory leak, and then choose the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="3d33f-215">Во время записи обратите внимание на то, что в приборе Распределения на временной шкале, как на следующем рисунке, покажите, какие-либо синие полосы.</span><span class="sxs-lookup"><span data-stu-id="3d33f-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Новые выделения" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="3d33f-217">Рис. 8. Новые выделения</span><span class="sxs-lookup"><span data-stu-id="3d33f-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="3d33f-218">Эти синие полосы представляют новые выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="3d33f-219">Эти новые выделения памяти являются вашими кандидатами для утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="3d33f-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="3d33f-220">Вы можете увеличить планку, чтобы отфильтровать панели **конструктора,** чтобы показать только объекты, выделенные в указанный период времени.</span><span class="sxs-lookup"><span data-stu-id="3d33f-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Шкала масштабирования выделения" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="3d33f-222">Рис. 9. Шкала масштабирования выделения</span><span class="sxs-lookup"><span data-stu-id="3d33f-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="3d33f-223">Расширьте объект и выберите значение, чтобы просмотреть дополнительные сведения в **области Объект.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="3d33f-224">Например, на следующем рисунке в подробностях вновь выделенного объекта указывается, что он был выделен переменной `x` в `Window` области.</span><span class="sxs-lookup"><span data-stu-id="3d33f-224">For example, in the following figure, in the details of the newly allocated object indicates that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Сведения об объектах" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="3d33f-226">Рис. 10. Сведения об объектах</span><span class="sxs-lookup"><span data-stu-id="3d33f-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a><span data-ttu-id="3d33f-227">Исследование распределения памяти по функции</span><span class="sxs-lookup"><span data-stu-id="3d33f-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="3d33f-228">Используйте тип **профилирования** выборки распределения для просмотра распределения памяти с помощью функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3d33f-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Выборка распределения записей" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="3d33f-230">Рис. 11. Выборка распределения записей</span><span class="sxs-lookup"><span data-stu-id="3d33f-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="3d33f-231">Выберите радио **кнопку Распределение выборки.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-231">Choose the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="3d33f-232">Если на странице есть рабочий, вы можете выбрать его в качестве целевого профилинга с помощью меню отсевов рядом с кнопкой **"Пуск".**</span><span class="sxs-lookup"><span data-stu-id="3d33f-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="3d33f-233">Выберите **кнопку Начните.**</span><span class="sxs-lookup"><span data-stu-id="3d33f-233">Choose the **Start** button.</span></span>  
1.  <span data-ttu-id="3d33f-234">Выполните действия на веб-странице, которую необходимо исследовать.</span><span class="sxs-lookup"><span data-stu-id="3d33f-234">Complete the actions on the webpage which you want to investigate.</span></span>  
1.  <span data-ttu-id="3d33f-235">Выберите **кнопку Stop** после завершения всех действий.</span><span class="sxs-lookup"><span data-stu-id="3d33f-235">Choose the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="3d33f-236">В DevTools показана разбивка распределения памяти по функции.</span><span class="sxs-lookup"><span data-stu-id="3d33f-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="3d33f-237">Представление по умолчанию **— Heavy (Bottom Up),** которое отображает функции, которые выделяли больше всего памяти в верхней части.</span><span class="sxs-lookup"><span data-stu-id="3d33f-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Выборка распределения" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="3d33f-239">Рис. 12. Выборка распределения</span><span class="sxs-lookup"><span data-stu-id="3d33f-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a><span data-ttu-id="3d33f-240">Spot frequent garbage collections</span><span class="sxs-lookup"><span data-stu-id="3d33f-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="3d33f-241">Если страница часто приостанавливована, могут возникнуть проблемы со сбором мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="3d33f-242">Для частого сбора мусора можно использовать либо диспетчер задач браузера Microsoft Edge, либо записи памяти производительности.</span><span class="sxs-lookup"><span data-stu-id="3d33f-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="3d33f-243">В диспетчере задач браузера Microsoft Edge \*\*\*\* часто возрастают и снижаются значения памяти памяти или **JavaScript,** что представляет собой частый сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="3d33f-244">В записях производительности частые изменения \(рост и падение\) в графах Кучи JS или числа узлов указывают на частую коллекцию мусора.</span><span class="sxs-lookup"><span data-stu-id="3d33f-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="3d33f-245">После того как вы определили проблему, \*\*\*\* вы можете использовать инструменты распределения на записи временной шкалы, чтобы узнать, где выделяется память и какие функции вызывают выделение.</span><span class="sxs-lookup"><span data-stu-id="3d33f-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3d33f-246">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3d33f-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Запись производительности — ссылка на анализ производительности"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="3d33f-248">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d33f-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3d33f-249">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="3d33f-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3d33f-251">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3d33f-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
