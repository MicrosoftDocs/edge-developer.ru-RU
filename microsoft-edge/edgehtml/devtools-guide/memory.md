---
description: Использование панели памяти для
title: DevTools — память
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, память, куч, GC, сборка мусора, сохраненный размер, объехатели
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5ad284f8072cc296743299ec9c4fb2037f8fd883
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235228"
---
# <span data-ttu-id="64247-104">Память</span><span class="sxs-lookup"><span data-stu-id="64247-104">Memory</span></span>

<span data-ttu-id="64247-105">Используйте панель **"Память",** чтобы оценить использование системных ресурсов и сравнить моментальные снимки кучи в разных состояниях выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="64247-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="64247-106">С его помощью вы можете:</span><span class="sxs-lookup"><span data-stu-id="64247-106">With it, you can:</span></span>

- <span data-ttu-id="64247-107">[График использования памяти страницы](#memory-usage-timeline) в режиме реального времени и снимки кучи</span><span class="sxs-lookup"><span data-stu-id="64247-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="64247-108">[Определение потенциальных проблем с](#snapshot-summary) памятью в коде, таких как сохраненные объекты, не подключенные к DOM</span><span class="sxs-lookup"><span data-stu-id="64247-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="64247-109">[Просмотр данных об использовании памяти](#snapshot-details) по типу объекта, подсчету экземпляров, размеру и ссылкам, чтобы изолировать проблемы</span><span class="sxs-lookup"><span data-stu-id="64247-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="64247-110">[Применение фильтров данных моментальных](#filters) снимков для уменьшения шума неанимаемых сведений</span><span class="sxs-lookup"><span data-stu-id="64247-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="64247-111">[Определение стоимости памяти определенного](#object-references) объекта и ссылок, которые его содержат</span><span class="sxs-lookup"><span data-stu-id="64247-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="64247-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span><span class="sxs-lookup"><span data-stu-id="64247-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![Панель памяти Microsoft Edge DevTools](./media/memory.png)


## <span data-ttu-id="64247-114">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="64247-114">Toolbar</span></span>

1. <span data-ttu-id="64247-115">**Запуск/остановка сеанса профилирование (CTRL+E):** включение профиля позволяет отслеживать использование памяти и делать моментальные снимки кучи.</span><span class="sxs-lookup"><span data-stu-id="64247-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="64247-116">**Импорт сеанса профилирование (CTRL+O):** загрузка сохраненного сеанса диагностики памяти DevTools.</span><span class="sxs-lookup"><span data-stu-id="64247-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="64247-117">**Экспортировать сеанс профилирование (CTRL+S):** сохраните текущий сеанс диагностики на диск.</span><span class="sxs-lookup"><span data-stu-id="64247-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="64247-118">**Снимок кучи (CTRL+SHIFT+T):** запись текущих выделений памяти на заданный момент времени.</span><span class="sxs-lookup"><span data-stu-id="64247-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="64247-119">Временная шкала использования памяти</span><span class="sxs-lookup"><span data-stu-id="64247-119">Memory usage timeline</span></span>

<span data-ttu-id="64247-120">Проблемы с памятью могут стать главной причиной проблем с производительностью, из-за чего страница со временем становится все более неотвеченной и запаздыванием.</span><span class="sxs-lookup"><span data-stu-id="64247-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="64247-121">Первым шагом при анализе использования памяти страницы [](#toolbar) является запуск сеанса профилирование, чтобы сделать моментальные снимки кучи до или после него при повторном анализе действий, вызывающих большой объем памяти или предположительное утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="64247-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="64247-122">При запуске профиля памяти вы увидите график памяти процесса, который позволяет со временем наблюдать за общим частным рабочим набором (объемом памяти, потребляемой страницей).</span><span class="sxs-lookup"><span data-stu-id="64247-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="64247-123">На графике памяти показано прямое представление памяти процесса вкладки, которая включает личные данные, тивную память и куч JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64247-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Временная шкала использования памяти](./media/memory_timeline.png)

 <span data-ttu-id="64247-125">На графике показана тенденция развития памяти для страницы, которая позволяет оценить [](#toolbar) целесообразность создания снимка кучи для дальнейшего сравнения, например периоды непредвиденное хранение памяти.</span><span class="sxs-lookup"><span data-stu-id="64247-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="64247-126">Performance.mark()</span><span class="sxs-lookup"><span data-stu-id="64247-126">Performance.mark()</span></span>

<span data-ttu-id="64247-127">Вы можете \*\*\*\* добавить на временную шкалу настраиваемые пометки пользователя, чтобы определить ключевые события во время сеанса анализа, вызывая метод из кода или консоли [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) DevTools. [\*\*\*\*](./console.md)</span><span class="sxs-lookup"><span data-stu-id="64247-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="64247-128">Console.takeheapSnapshot()</span><span class="sxs-lookup"><span data-stu-id="64247-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="64247-129">Иногда необходимо делать моментальные снимки в конкретные моменты времени, например непосредственно перед большим перемехаком DOM.</span><span class="sxs-lookup"><span data-stu-id="64247-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="64247-130">В таких случаях снимки можно сделать программным [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) путем.</span><span class="sxs-lookup"><span data-stu-id="64247-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="64247-131">Сводка по моментальных снимкам</span><span class="sxs-lookup"><span data-stu-id="64247-131">Snapshot summary</span></span>

<span data-ttu-id="64247-132">[При снимке](#toolbar) создается итоговая плитка, которая указывает размер кучи JavaScript на момент создания снимка, а также количество выделенных объектов и снимок экрана страницы.</span><span class="sxs-lookup"><span data-stu-id="64247-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="64247-133">Вы можете продолжать делать моментальные снимки в любое время при запуске пользовательского сценария, требующего анализа.</span><span class="sxs-lookup"><span data-stu-id="64247-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="64247-134">Моментальные снимки создают дополнительные плитки, каждый из которых показывает разницу в памяти JavaScript от предыдущего снимка.</span><span class="sxs-lookup"><span data-stu-id="64247-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Моментальный снимок кучи](./media/memory_snapshot.png)

<span data-ttu-id="64247-136">Если щелкнуть значения на плитке сводки, переключимся на области с подробными [сведениями о моментальных снимках.](#snapshot-details)</span><span class="sxs-lookup"><span data-stu-id="64247-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="64247-137">Потенциальные [проблемы с памятью обозначены](#snapshot-details) синим информационным значком ("i").</span><span class="sxs-lookup"><span data-stu-id="64247-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="64247-138">Сведения о моментальных снимках</span><span class="sxs-lookup"><span data-stu-id="64247-138">Snapshot details</span></span>

<span data-ttu-id="64247-139">Данные в области *моментальных* снимков показывают объекты, созданные страницей, а также память, выделенную платформами JavaScript, которые вы можете использовать.</span><span class="sxs-lookup"><span data-stu-id="64247-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Таблица сведений о моментальных снимках](./media/memory_details.png)

<span data-ttu-id="64247-141">Эти три вкладки представляют различные представления данных:</span><span class="sxs-lookup"><span data-stu-id="64247-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="64247-142">Типы</span><span class="sxs-lookup"><span data-stu-id="64247-142">Types</span></span>

<span data-ttu-id="64247-143">Показывает количество экземпляров и общий размер объектов в куче, сгруппных по типу объекта.</span><span class="sxs-lookup"><span data-stu-id="64247-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="64247-144">По умолчанию они сортироваться по подсчету экземпляров.</span><span class="sxs-lookup"><span data-stu-id="64247-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="64247-145">При выборе объекта в \*\* верхней области [](#object-references) типов таблица "Ссылки на объекты" в нижней области будет перечислять все объекты, которые указывают на этот объект.</span><span class="sxs-lookup"><span data-stu-id="64247-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="64247-146">Корневая</span><span class="sxs-lookup"><span data-stu-id="64247-146">Roots</span></span>

<span data-ttu-id="64247-147">Показывает иерархическое представление ссылок на детей, чтобы описать, как объекты коренится в глобальном объекте, предотвращая их сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="64247-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="64247-148">По умолчанию эти узлы сортироваться по столбце сохраненного размера с наибольшим значением в верхней части.</span><span class="sxs-lookup"><span data-stu-id="64247-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="64247-149">Предикторы</span><span class="sxs-lookup"><span data-stu-id="64247-149">Dominators</span></span>

<span data-ttu-id="64247-150">Отображает список объектов в куче, которые имеют исключительные ссылки на другие объекты.</span><span class="sxs-lookup"><span data-stu-id="64247-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="64247-151">Обилители сортировать по сохраненным размерам, чтобы указать объекты, потребляющие больше всего памяти, которые потенциально проще освободить.</span><span class="sxs-lookup"><span data-stu-id="64247-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="64247-152">Вот как интерпретировать столбцы в представлениях *"Типы",* "Корневая *корня" и "Объехатели":*</span><span class="sxs-lookup"><span data-stu-id="64247-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="64247-153">Столбец</span><span class="sxs-lookup"><span data-stu-id="64247-153">Column</span></span> | <span data-ttu-id="64247-154">Описание</span><span class="sxs-lookup"><span data-stu-id="64247-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="64247-155">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="64247-155">Identifier(s)</span></span> | <span data-ttu-id="64247-156">Имя, которое лучше всего идентифицирует объект.</span><span class="sxs-lookup"><span data-stu-id="64247-156">Name that best identifies the object.</span></span> <span data-ttu-id="64247-157">Например, для элементов HTML сведения моментального снимка показывают значение атрибута ID, если он используется.</span><span class="sxs-lookup"><span data-stu-id="64247-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="64247-158">Тип</span><span class="sxs-lookup"><span data-stu-id="64247-158">Type</span></span> | <span data-ttu-id="64247-159">Тип объекта (например, *HTMLDivElement).*</span><span class="sxs-lookup"><span data-stu-id="64247-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="64247-160">Size</span><span class="sxs-lookup"><span data-stu-id="64247-160">Size</span></span> | <span data-ttu-id="64247-161">Размер объекта, не включая размер объектов, на которые ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="64247-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="64247-162">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="64247-162">Retained size</span></span> | <span data-ttu-id="64247-163">Размер объекта плюс размер всех объектов-детей, у которых нет других родительских объектов.</span><span class="sxs-lookup"><span data-stu-id="64247-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="64247-164">Для практических целей это объем памяти, который сохраняется объектом, поэтому при удалении объекта необходимо освободить указанный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="64247-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="64247-165">Количество</span><span class="sxs-lookup"><span data-stu-id="64247-165">Count</span></span> | <span data-ttu-id="64247-166">Количество экземпляров объектов.</span><span class="sxs-lookup"><span data-stu-id="64247-166">Number of object instances.</span></span> <span data-ttu-id="64247-167">Это значение отображается только в представлении "Типы".</span><span class="sxs-lookup"><span data-stu-id="64247-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="64247-168">При выборе объекта в верхней области *"Объекторы"* в таблице ссылок на объекты в нижней области будут перечисляться все объекты, которые указывают на этот объект. [](#object-references)</span><span class="sxs-lookup"><span data-stu-id="64247-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="64247-169">Фильтры</span><span class="sxs-lookup"><span data-stu-id="64247-169">Filters</span></span>

<span data-ttu-id="64247-170">Вы можете дополнительно настроить данные в таблице с помощью следующих данных:</span><span class="sxs-lookup"><span data-stu-id="64247-170">You can further adjust data in the table with the following:</span></span>

![Фильтрация для встроенных объектов и их ИД](./media/memory_filter.png)

1. <span data-ttu-id="64247-172">**Фильтр идентификаторов:** фильтрация данных путем поиска определенного идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="64247-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="64247-173">**Группировать по**объектору: в представлении объектов верхнего уровня показываются только объекты с исключительными ссылками на другие объекты (это представление по умолчанию на вкладке \*\* *"Обзорчики").*</span><span class="sxs-lookup"><span data-stu-id="64247-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="64247-174">**Встроенные фильтры и ID:** по умолчанию встроенные объекты [JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) включены в список.</span><span class="sxs-lookup"><span data-stu-id="64247-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="64247-175">Перечисление ИД объектов может быть полезно, если существует несколько анонимных объектов, которые необходимо различать.</span><span class="sxs-lookup"><span data-stu-id="64247-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="64247-176">Представления *"Типы",* "Корневая корня" и "Обилители" имеют собственный фильтр, поэтому фильтр не сохраняется при переключении на другое представление. \*\*</span><span class="sxs-lookup"><span data-stu-id="64247-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="64247-177">Ссылки на объекты</span><span class="sxs-lookup"><span data-stu-id="64247-177">Object references</span></span>

<span data-ttu-id="64247-178">В [**представлениях "Типы**](#types) и [**обилители"**](#dominators) нижняя области содержит список ссылок на объекты, в котором отображаются общие ссылки. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="64247-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="64247-179">При выборе объекта в верхней области в этом списке отображаются все объекты, которые указывают на этот объект, другими словами, объекты, которые по-настоящему живы для выбранного объекта.</span><span class="sxs-lookup"><span data-stu-id="64247-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="64247-180">Циклальные ссылки показаны со звездочкой (\*) и информационной tooltip и не могут быть расширены.</span><span class="sxs-lookup"><span data-stu-id="64247-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="64247-181">В противном случае они не помешали бы вам ходить вверх по эталонным деревам и определять объекты, которые сохраняют память.</span><span class="sxs-lookup"><span data-stu-id="64247-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="64247-182">Чтобы быстро определить эквивалентные [\*\*](#filters) объекты, отметьте параметр фильтра идентификаторов объектов отображения, чтобы отобразить идентификаторы объектов рядом с именами объектов в столбце *идентификаторов.*</span><span class="sxs-lookup"><span data-stu-id="64247-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="64247-183">Объекты с одинаковым ИД являются общими ссылками.</span><span class="sxs-lookup"><span data-stu-id="64247-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="64247-184">Сравнение моментальных снимков</span><span class="sxs-lookup"><span data-stu-id="64247-184">Snapshot comparison</span></span>

<span data-ttu-id="64247-185">Если щелкнуть [вкладку](#snapshot-details) сравнения моментальных снимков или ссылку сравнения на плитке сводки моментальных снимков, между двумя снимками будет отметен разрыв данных. [](#snapshot-summary)</span><span class="sxs-lookup"><span data-stu-id="64247-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="64247-186">В области сравнения представления *"Объекторы",* [\*\*](#snapshot-details) "Типы" и "Корневая" предоставляют те же моментальные снимки, что и для отдельных моментальных снимков, с такими дополнительными значениями: \*\*</span><span class="sxs-lookup"><span data-stu-id="64247-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="64247-187">Столбец</span><span class="sxs-lookup"><span data-stu-id="64247-187">Column</span></span> | <span data-ttu-id="64247-188">Описание</span><span class="sxs-lookup"><span data-stu-id="64247-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="64247-189">DIFF размера.</span><span class="sxs-lookup"><span data-stu-id="64247-189">Size diff.</span></span> | <span data-ttu-id="64247-190">Разница между размером объекта в текущем снимке и его размером в предыдущем снимке, не включая размер объектов, на которые ссылается ссылка.</span><span class="sxs-lookup"><span data-stu-id="64247-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="64247-191">DIFF сохраненного размера.</span><span class="sxs-lookup"><span data-stu-id="64247-191">Retained size diff.</span></span> | <span data-ttu-id="64247-192">Разница между сохраненным размером объекта в текущем снимке и его сохраненным размером в предыдущем снимке.</span><span class="sxs-lookup"><span data-stu-id="64247-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="64247-193">Сохраненный размер включает размер объекта плюс размер всех его родительских объектов, у которых нет других родительских объектов.</span><span class="sxs-lookup"><span data-stu-id="64247-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="64247-194">В практических целях сохраненный размер — это объем памяти, который сохраняется объектом, поэтому при удалении объекта необходимо освободить указанный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="64247-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="64247-195">Для фильтрации \*\*\*\* разнонаправленной информации между моментальными снимками можно использовать выпадаемую область:</span><span class="sxs-lookup"><span data-stu-id="64247-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Фильтр области для сравнения моментальных снимков](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="64247-197">Объекты, остались в моментальных снимках # : показывает разницу между объектами, добавленными в куче и удаляемой из кучи из базового снимка в <number></strong> предыдущий моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="64247-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="64247-198">Например, если сводка моментальных снимков показывает <em> +205 / -195 в числе объектов, этот фильтр отображает десять объектов, которые были добавлены, но </em> не удалены.</span><span class="sxs-lookup"><span data-stu-id="64247-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="64247-199">Объекты, добавленные между моментальный снимок # и # : показывает все объекты, добавленные к <number> <number></strong> куче из предыдущего снимка.</span><span class="sxs-lookup"><span data-stu-id="64247-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="64247-200">Все объекты в моментальный снимок # : показывает все объекты в куче (другими словами, неотрисованное <number></strong> <em> </em> представление).</span><span class="sxs-lookup"><span data-stu-id="64247-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="64247-201">По умолчанию фильтр *"Показать не* совпадающие ссылки" применяется к представлению сравнения, чтобы указать ссылки на объекты, не совпадающие с текущим фильтром области.</span><span class="sxs-lookup"><span data-stu-id="64247-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="64247-202">Вы можете отключить его из меню в выпаданом меню:</span><span class="sxs-lookup"><span data-stu-id="64247-202">You can turn it off from the dropdown menu:</span></span>

![Фильтр не совпадающих ссылок для сравнения моментальных снимков](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="64247-204">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="64247-204">Shortcuts</span></span>

 <span data-ttu-id="64247-205">Действие</span><span class="sxs-lookup"><span data-stu-id="64247-205">Action</span></span> | <span data-ttu-id="64247-206">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="64247-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="64247-207">Запуск и остановка сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="64247-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="64247-208">Импорт сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="64247-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="64247-209">Экспорт сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="64247-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="64247-210">Снимок кучи</span><span class="sxs-lookup"><span data-stu-id="64247-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="64247-211">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="64247-211">Known Issues</span></span>

### <span data-ttu-id="64247-212">Ошибка при запуске сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="64247-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="64247-213">Если вы видите это \*\*\*\* сообщение об ошибке: при запуске сеанса профилирования в средстве "Память" произошла ошибка, выполните следующие действия для обходного решения.</span><span class="sxs-lookup"><span data-stu-id="64247-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="64247-214">Нажмите `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="64247-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="64247-215">В диалоговом окке "Выполнить" **введите services.msc**.</span><span class="sxs-lookup"><span data-stu-id="64247-215">In the Run dialog, enter **services.msc**.</span></span>
![known-issues-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="64247-217">Найдите стандартную службу сборщика Microsoft **(R) Diagnostics Hub** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="64247-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![known-issues-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="64247-219">Перезапустите стандартную службу сборщика Microsoft **(R) Diagnostics Hub.**</span><span class="sxs-lookup"><span data-stu-id="64247-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![known-issues-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="64247-221">Закроем Инструменты разработчика Microsoft Edge и вкладку. Откройте новую вкладку, перейдите на страницу и нажмите `F12` .</span><span class="sxs-lookup"><span data-stu-id="64247-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="64247-222">Теперь вы сможете начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="64247-222">You should now be able to begin profiling.</span></span> 
![known-issues-4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="64247-224">По-прежнему возникают проблемы?</span><span class="sxs-lookup"><span data-stu-id="64247-224">Still running into problems?</span></span> <span data-ttu-id="64247-225">Отправьте нам свой отзыв с помощью **значка отправки отзыва!**</span><span class="sxs-lookup"><span data-stu-id="64247-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![known-issues-5](./media/known_issues_5.PNG)
