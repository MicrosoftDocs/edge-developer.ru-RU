---
description: Узнайте, как записывать снимки с помощью профиля кучи Microsoft Edge DevTools и находить утечки памяти.
title: Запись снимков кучи
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ce7a6f972bed386f96312808428bd74f1241668f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397806"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="how-to-record-heap-snapshots"></a><span data-ttu-id="ba93c-104">Запись снимков кучи</span><span class="sxs-lookup"><span data-stu-id="ba93c-104">How to record heap snapshots</span></span>  

<span data-ttu-id="ba93c-105">Узнайте, как записывать снимки с помощью профиля кучи Microsoft Edge DevTools и находить утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="ba93c-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="ba93c-106">Профиль microsoft Edge DevTools показывает распределение памяти по объектам JavaScript и связанным узлам DOM вашей страницы.</span><span class="sxs-lookup"><span data-stu-id="ba93c-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="ba93c-107">С его помощью можно сделать снимки javaScript \(JS heap\) , проанализировать графики памяти, сравнить снимки и найти утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="ba93c-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="ba93c-108">Перейдите к [дереву объектов.][DevtoolsMemoryProblems101ObjectsRetainingTree]</span><span class="sxs-lookup"><span data-stu-id="ba93c-108">Navigate to [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <a name="take-a-snapshot"></a><span data-ttu-id="ba93c-109">Снимок</span><span class="sxs-lookup"><span data-stu-id="ba93c-109">Take a snapshot</span></span>  

<span data-ttu-id="ba93c-110">На панели **Памяти** выберите **Снимок,** а затем выберите **Начните**.</span><span class="sxs-lookup"><span data-stu-id="ba93c-110">On the **Memory** panel, choose **Take snapshot**, then choose **Start**.</span></span>  <span data-ttu-id="ba93c-111">Вы также можете `Ctrl` + `E` выбрать \(Windows, Linux\) `Cmd` + `E` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-111">You may also select `Ctrl`+`E` \(Windows, Linux\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Выберите тип профилирование" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="ba93c-113">Выберите тип профилирование</span><span class="sxs-lookup"><span data-stu-id="ba93c-113">Choose profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="ba93c-114">**Снимки** первоначально хранятся в памяти процесса визуализации.</span><span class="sxs-lookup"><span data-stu-id="ba93c-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="ba93c-115">Снимки передаются в DevTools по запросу при выборе значка снимка для просмотра.</span><span class="sxs-lookup"><span data-stu-id="ba93c-115">Snapshots are transferred to the DevTools on demand, when you choose on the snapshot icon to view it.</span></span>  

<span data-ttu-id="ba93c-116">После загрузки снимка в DevTools и его разбрасыва, появляется номер ниже заголовка снимка и отображается общий размер достигаемых объектов [JavaScript.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="ba93c-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Общий размер досяжимых объектов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="ba93c-118">Общий размер досяжимых объектов</span><span class="sxs-lookup"><span data-stu-id="ba93c-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba93c-119">В снимки включены только досяжимые объекты.</span><span class="sxs-lookup"><span data-stu-id="ba93c-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="ba93c-120">Кроме того, снимок всегда начинается со сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="ba93c-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <a name="clear-snapshots"></a><span data-ttu-id="ba93c-121">Снимок очистки</span><span class="sxs-lookup"><span data-stu-id="ba93c-121">Clear snapshots</span></span>  

<span data-ttu-id="ba93c-122">Выберите **значок Clear all profiles** для удаления снимков \(как из DevTools, так и из любой памяти, связанной с процессом рендера\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-122">Choose **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Удаление снимков" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="ba93c-124">Удаление снимков</span><span class="sxs-lookup"><span data-stu-id="ba93c-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="ba93c-125">Закрытие окна DevTools не удаляет профили из памяти, связанной с процессом отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ba93c-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="ba93c-126">При повторном восстановлении DevTools все ранее сделанные снимки вновь появляются в списке снимков.</span><span class="sxs-lookup"><span data-stu-id="ba93c-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="ba93c-127">Попробуйте этот пример [рассеянных объектов][GlitchDevtoolsMemoryExample03] и профиль его с помощью профайла кучи.</span><span class="sxs-lookup"><span data-stu-id="ba93c-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="ba93c-128">Отображается несколько распределений элементов \(object\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-128">A number of \(object\) item allocations are displayed.</span></span>  

## <a name="view-snapshots"></a><span data-ttu-id="ba93c-129">Просмотр снимков</span><span class="sxs-lookup"><span data-stu-id="ba93c-129">View snapshots</span></span>  

<span data-ttu-id="ba93c-130">Просмотр снимков с разных точек зрения для различных задач.</span><span class="sxs-lookup"><span data-stu-id="ba93c-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="ba93c-131">**Сводное представление** показывает объекты, сгруппив их под именем конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba93c-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="ba93c-132">Используйте его для выслеки объектов \(и использования памяти\) на основе типа, сгруппив по имени конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba93c-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="ba93c-133">Это особенно полезно для **отслеживания утечек DOM**.</span><span class="sxs-lookup"><span data-stu-id="ba93c-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="ba93c-134">**Представление сравнения**.</span><span class="sxs-lookup"><span data-stu-id="ba93c-134">**Comparison view**.</span></span>  <span data-ttu-id="ba93c-135">Отображает разницу между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="ba93c-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="ba93c-136">Используйте его для сравнения двух снимков памяти \(или более\) до и после операции.</span><span class="sxs-lookup"><span data-stu-id="ba93c-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="ba93c-137">Проверка дельты в освобожденной памяти и отсчете ссылок позволяет подтвердить наличие и причину утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="ba93c-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="ba93c-138">**Представление сдерживания**.</span><span class="sxs-lookup"><span data-stu-id="ba93c-138">**Containment view**.</span></span>  <span data-ttu-id="ba93c-139">Позволяет исследовать содержимое кучи.</span><span class="sxs-lookup"><span data-stu-id="ba93c-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="ba93c-140">**Представление сдерживания** обеспечивает лучшее представление структуры объектов, помогая анализировать объекты, на которые ссылается глобальное пространство имен \(window\) для поиска того, что содержит объекты вокруг.</span><span class="sxs-lookup"><span data-stu-id="ba93c-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="ba93c-141">Используйте его для анализа замыкания и погружения в объекты на низком уровне.</span><span class="sxs-lookup"><span data-stu-id="ba93c-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="ba93c-142">Чтобы переключаться между представлениями, используйте селектор в верхней части представления.</span><span class="sxs-lookup"><span data-stu-id="ba93c-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Селектор переключатель представлений" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="ba93c-144">Селектор переключатель представлений</span><span class="sxs-lookup"><span data-stu-id="ba93c-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba93c-145">Не все свойства хранятся на кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="ba93c-146">Свойства, реализованные с помощью геттеров, использующих исходный код, не захватываются.</span><span class="sxs-lookup"><span data-stu-id="ba93c-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="ba93c-147">Кроме того, неконструкционные значения, такие как числа, не захватываются.</span><span class="sxs-lookup"><span data-stu-id="ba93c-147">Also, non-string values such as numbers are not captured.</span></span>  

### <a name="summary-view"></a><span data-ttu-id="ba93c-148">Представление сводки</span><span class="sxs-lookup"><span data-stu-id="ba93c-148">Summary view</span></span>  

<span data-ttu-id="ba93c-149">Сначала снимок открывается в представлении Сводка, отображая итоговые объекты, которые могут быть расширены, чтобы показать экземпляры:</span><span class="sxs-lookup"><span data-stu-id="ba93c-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Представление сводки" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="ba93c-151">**Представление сводки**</span><span class="sxs-lookup"><span data-stu-id="ba93c-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="ba93c-152">Записи верхнего уровня — это "общие" строки.</span><span class="sxs-lookup"><span data-stu-id="ba93c-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="ba93c-153">Записи верхнего уровня</span><span class="sxs-lookup"><span data-stu-id="ba93c-153">Top-level entries</span></span> | <span data-ttu-id="ba93c-154">Описание</span><span class="sxs-lookup"><span data-stu-id="ba93c-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="ba93c-155">Конструктор</span><span class="sxs-lookup"><span data-stu-id="ba93c-155">Constructor</span></span>** | <span data-ttu-id="ba93c-156">Представляет все объекты, созданные с помощью этого конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba93c-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="ba93c-157">Расстояние</span><span class="sxs-lookup"><span data-stu-id="ba93c-157">Distance</span></span>** | <span data-ttu-id="ba93c-158">отображает расстояние до корневого с помощью самого короткого простого пути узлов.</span><span class="sxs-lookup"><span data-stu-id="ba93c-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="ba93c-159">Неглубокий размер</span><span class="sxs-lookup"><span data-stu-id="ba93c-159">Shallow size</span></span>** | <span data-ttu-id="ba93c-160">Отображает сумму мелких размеров всех объектов, созданных определенной функцией конструктора.</span><span class="sxs-lookup"><span data-stu-id="ba93c-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="ba93c-161">Небольшой размер — это размер памяти, удерживаемой объектом \(как правило, массивы и строки имеют более крупные неглубокие размеры\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="ba93c-162">Перейдите [к размерам объекта.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="ba93c-162">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="ba93c-163">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="ba93c-163">Retained size</span></span>** | <span data-ttu-id="ba93c-164">Отображает максимальный сохраненный размер одного и того же набора объектов.</span><span class="sxs-lookup"><span data-stu-id="ba93c-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="ba93c-165">Размер памяти, который вы можете освободить после удаления объекта \((а иждивенцы больше не достигаются\) называется сохраненным размером.</span><span class="sxs-lookup"><span data-stu-id="ba93c-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="ba93c-166">Перейдите [к размерам объекта.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="ba93c-166">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="ba93c-167">После расширения общей строки в верхнем представлении отображаются все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="ba93c-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="ba93c-168">В каждом экземпляре в соответствующих столбцах отображаются неглубокие и сохраненные размеры.</span><span class="sxs-lookup"><span data-stu-id="ba93c-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="ba93c-169">Номер после `@` символа — уникальный ID объекта, позволяющий сравнивать снимки кучи на основе объекта.</span><span class="sxs-lookup"><span data-stu-id="ba93c-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="ba93c-170">Помните, что желтые объекты имеют ссылки на JavaScript, а красные — это отдельные узлы, которые ссылаются на один с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="ba93c-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="ba93c-171">Что соответствуют различным записям конструктора \(group\) в профиле Куча?</span><span class="sxs-lookup"><span data-stu-id="ba93c-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Группы конструкторов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="ba93c-173">**Группы конструкторов**</span><span class="sxs-lookup"><span data-stu-id="ba93c-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="ba93c-174">Запись Конструктор \(group\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="ba93c-175">Описание</span><span class="sxs-lookup"><span data-stu-id="ba93c-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="ba93c-176">\(глобальное свойство\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-176">\(global property\)</span></span>** | <span data-ttu-id="ba93c-177">Промежуточные объекты между глобальным объектом \(like \) и `window` объектом, на который он ссылается.</span><span class="sxs-lookup"><span data-stu-id="ba93c-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="ba93c-178">Если объект создается с помощью конструктора и удерживается глобальным объектом, путь сохранения может быть `Person` представлен как `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="ba93c-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path may be represented as `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="ba93c-179">Это контрастирует с нормой, когда объекты напрямую ссылались друг на друга.</span><span class="sxs-lookup"><span data-stu-id="ba93c-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="ba93c-180">Промежуточные объекты существуют по причинам производительности.</span><span class="sxs-lookup"><span data-stu-id="ba93c-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="ba93c-181">Глобальные объекты регулярно меняются, а оптимизация доступа к свойствам хорошо действует для объектов, не влияемых на глобальные объекты.</span><span class="sxs-lookup"><span data-stu-id="ba93c-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="ba93c-182">\(roots\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-182">\(roots\)</span></span>** | <span data-ttu-id="ba93c-183">Корневые записи в представлении сохраняемой елки — это объекты, которые имеют ссылки на выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="ba93c-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="ba93c-184">Записи также могут быть ссылками, созданными двигателем для определенных целей.</span><span class="sxs-lookup"><span data-stu-id="ba93c-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="ba93c-185">У двигателя есть кэши, которые являются эталонными объектами, но все эти ссылки являются слабыми и не препятствуют сбору объекта, учитывая отсутствие действительно сильных ссылок.</span><span class="sxs-lookup"><span data-stu-id="ba93c-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="ba93c-186">\(closure\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-186">\(closure\)</span></span>** | <span data-ttu-id="ba93c-187">Количество ссылок на группу объектов с помощью закрытия функций.</span><span class="sxs-lookup"><span data-stu-id="ba93c-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="ba93c-188">\(массив, строка, номер, regexp\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="ba93c-189">Список типов объектов со свойствами, которые ссылались на массив, строку, номер или регулярное выражение.</span><span class="sxs-lookup"><span data-stu-id="ba93c-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="ba93c-190">\(компилировать код\)</span><span class="sxs-lookup"><span data-stu-id="ba93c-190">\(compiled code\)</span></span>** | <span data-ttu-id="ba93c-191">Все, что связано с скомпиловым кодом.</span><span class="sxs-lookup"><span data-stu-id="ba93c-191">Everything related to compiled code.</span></span>  <span data-ttu-id="ba93c-192">Скрипт похож на функцию, но соответствует `<script>` телу.</span><span class="sxs-lookup"><span data-stu-id="ba93c-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="ba93c-193">SharedFunctionInfos \(SFI\) — это объекты, стоящие между функциями и компилировать код.</span><span class="sxs-lookup"><span data-stu-id="ba93c-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="ba93c-194">Функции обычно имеют контекст, а SFIs - нет.</span><span class="sxs-lookup"><span data-stu-id="ba93c-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="ba93c-195">**HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment**и так далее.</span><span class="sxs-lookup"><span data-stu-id="ba93c-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="ba93c-196">Ссылки на элементы или объекты документов определенного типа, на которые ссылается код.</span><span class="sxs-lookup"><span data-stu-id="ba93c-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a><span data-ttu-id="ba93c-197">Представление сравнения</span><span class="sxs-lookup"><span data-stu-id="ba93c-197">Comparison view</span></span>  

<span data-ttu-id="ba93c-198">Найдите объекты с утечкой, сравнивая несколько снимков друг с другом.</span><span class="sxs-lookup"><span data-stu-id="ba93c-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="ba93c-199">Чтобы убедиться, что определенная операция приложения не создает утечек \(например, обычно пара прямых и обратных операций, таких как открытие документа, а затем его закрытие, не должно оставлять мусора\), вы можете следовать ниже сценарию:</span><span class="sxs-lookup"><span data-stu-id="ba93c-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="ba93c-200">Снимок кучи перед выполнением операции.</span><span class="sxs-lookup"><span data-stu-id="ba93c-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="ba93c-201">Выполните операцию \(взаимодействовать со страницей в некотором смысле, что вы считаете причиной утечки\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="ba93c-202">Выполните обратную операцию \(выполните противоположное взаимодействие и повторите ее несколько раз\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="ba93c-203">Снимок второй кучи и измените представление этого снимка на **Сравнение,** сравнивая его со **снимком 1**.</span><span class="sxs-lookup"><span data-stu-id="ba93c-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="ba93c-204">В **представлении Сравнение** отображается разница между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="ba93c-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="ba93c-205">При расширении общей записи показаны экземпляры добавленных и удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="ba93c-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Представление сравнения" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="ba93c-207">**Представление сравнения**</span><span class="sxs-lookup"><span data-stu-id="ba93c-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a><span data-ttu-id="ba93c-208">Представление сдерживания</span><span class="sxs-lookup"><span data-stu-id="ba93c-208">Containment view</span></span>  

<span data-ttu-id="ba93c-209">Представление **Containment** — это, по сути, "вид с высоты птичьего полета" структуры объектов приложения.</span><span class="sxs-lookup"><span data-stu-id="ba93c-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="ba93c-210">Это позволяет заглянуть внутрь замыкания функций, наблюдать внутренние объекты виртуальной машины \(VM\), которые вместе составляют объекты JavaScript, и понимать, сколько памяти ваше приложение использует на очень низком уровне.</span><span class="sxs-lookup"><span data-stu-id="ba93c-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="ba93c-211">Точки входа представления сдерживания</span><span class="sxs-lookup"><span data-stu-id="ba93c-211">Containment view entry points</span></span> | <span data-ttu-id="ba93c-212">Описание</span><span class="sxs-lookup"><span data-stu-id="ba93c-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="ba93c-213">Объекты DOMWindow</span><span class="sxs-lookup"><span data-stu-id="ba93c-213">DOMWindow objects</span></span>** | <span data-ttu-id="ba93c-214">Глобальные объекты для кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="ba93c-215">Корни GC</span><span class="sxs-lookup"><span data-stu-id="ba93c-215">GC roots</span></span>** | <span data-ttu-id="ba93c-216">Фактические корневишки GC, используемые мусором VM.</span><span class="sxs-lookup"><span data-stu-id="ba93c-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="ba93c-217">Корни GC состоят из встроенных карт объектов, таблиц символов, стеков потоков VM, кэшей компиляции, областей обработки и глобальных ручейков.</span><span class="sxs-lookup"><span data-stu-id="ba93c-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="ba93c-218">Объекты native</span><span class="sxs-lookup"><span data-stu-id="ba93c-218">Native objects</span></span>** | <span data-ttu-id="ba93c-219">Объекты браузера "толкнули" внутри виртуальной машины JavaScript \(JavaScript VM\), чтобы разрешить автоматизацию, например, узлы DOM, правила CSS.</span><span class="sxs-lookup"><span data-stu-id="ba93c-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Представление сдерживания" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="ba93c-221">**Представление сдерживания**</span><span class="sxs-lookup"><span data-stu-id="ba93c-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="ba93c-222">Подсказка о закрытии.</span><span class="sxs-lookup"><span data-stu-id="ba93c-222">A tip about closures.</span></span>  <span data-ttu-id="ba93c-223">Назови функции, чтобы можно было легко различать закрытия на снимке.</span><span class="sxs-lookup"><span data-stu-id="ba93c-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="ba93c-224">Например, в этом примере не используются именуемые функции.</span><span class="sxs-lookup"><span data-stu-id="ba93c-224">For example, this example does not use named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <span data-ttu-id="ba93c-225">В фрагменте следующего кода используются именные функции.</span><span class="sxs-lookup"><span data-stu-id="ba93c-225">The followingcode snippet uses named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="ba93c-226">Попробуйте в этом [примере, почему `eval` зло,][GlitchDevtoolsMemoryExample07] чтобы проанализировать влияние замыкания на память.</span><span class="sxs-lookup"><span data-stu-id="ba93c-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="ba93c-227">Вы также можете быть заинтересованы в следующем его с этим примером, который принимает вас через запись [кучи выделения][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="ba93c-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <a name="look-up-color-coding"></a><span data-ttu-id="ba93c-228">Искать цветовое кодирование</span><span class="sxs-lookup"><span data-stu-id="ba93c-228">Look up color coding</span></span>  

<span data-ttu-id="ba93c-229">Свойства и значения свойств объектов имеют различные типы и соответственно цветные.</span><span class="sxs-lookup"><span data-stu-id="ba93c-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="ba93c-230">Каждое свойство имеет один из четырех типов.</span><span class="sxs-lookup"><span data-stu-id="ba93c-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="ba93c-231">Тип свойства</span><span class="sxs-lookup"><span data-stu-id="ba93c-231">Property Type</span></span> | <span data-ttu-id="ba93c-232">Описание</span><span class="sxs-lookup"><span data-stu-id="ba93c-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="ba93c-233">a: свойство</span><span class="sxs-lookup"><span data-stu-id="ba93c-233">a: property</span></span>** | <span data-ttu-id="ba93c-234">Обычное свойство с именем, к нему можно получить доступ через оператора \(dot\) или с помощью `.` `[` `]` нотации \(кронштейны\) например `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="ba93c-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="ba93c-235">0: элемент</span><span class="sxs-lookup"><span data-stu-id="ba93c-235">0: element</span></span>** | <span data-ttu-id="ba93c-236">Обычное свойство с числительным индексом, доступ к нему осуществляется с помощью `[` `]` нотации \(кронштейны\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="ba93c-237">a: context var</span><span class="sxs-lookup"><span data-stu-id="ba93c-237">a: context var</span></span>** |  <span data-ttu-id="ba93c-238">Переменная в контексте функции, доступная по имени переменной изнутри закрытия функции.</span><span class="sxs-lookup"><span data-stu-id="ba93c-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="ba93c-239">a: системная опора</span><span class="sxs-lookup"><span data-stu-id="ba93c-239">a: system prop</span></span>** | <span data-ttu-id="ba93c-240">Свойство, добавленное VM JavaScript, не доступное из кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="ba93c-241">Объекты, назначенные `System` как не имеют соответствующего типа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="ba93c-242">Каждый из них является частью реализации объектной системы VM Javascript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="ba93c-243">V8 выделяет большинство внутренних объектов в той же куче, что и объекты JS пользователя.</span><span class="sxs-lookup"><span data-stu-id="ba93c-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="ba93c-244">Это всего лишь внутренние органы V8.</span><span class="sxs-lookup"><span data-stu-id="ba93c-244">So these are just V8 internals.</span></span>  

## <a name="find-a-specific-object"></a><span data-ttu-id="ba93c-245">Поиск определенного объекта</span><span class="sxs-lookup"><span data-stu-id="ba93c-245">Find a specific object</span></span>  

<span data-ttu-id="ba93c-246">Чтобы найти объект в собранной куче, можно поискать с помощью и `Ctrl` + `F` предоставить ID объекта.</span><span class="sxs-lookup"><span data-stu-id="ba93c-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <a name="uncover-dom-leaks"></a><span data-ttu-id="ba93c-247">Раскрытие утечек DOM</span><span class="sxs-lookup"><span data-stu-id="ba93c-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="ba93c-248">Профайлатор кучи имеет возможность отражать бидырекционные зависимости между родными объектами браузера \(узлы DOM, правила CSS\) и объектами JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ba93c-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="ba93c-249">Это помогает обнаружить невидимые утечки, происходящие из-за забытых отсоединяющихся подтрибов DOM, плавающих вокруг.</span><span class="sxs-lookup"><span data-stu-id="ba93c-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="ba93c-250">Утечки DOM могут быть больше, чем вы думаете.</span><span class="sxs-lookup"><span data-stu-id="ba93c-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="ba93c-251">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="ba93c-251">Consider the following sample.</span></span>  <span data-ttu-id="ba93c-252">Когда #tree GC?</span><span class="sxs-lookup"><span data-stu-id="ba93c-252">When is the #tree GC?</span></span>  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

<span data-ttu-id="ba93c-253">Поддерживает ссылку на соответствующий родитель `#leaf` \(parentNode\) и recursively до , поэтому только когда leafRef является nullified является целое дерево под кандидатом `#tree` `#tree` для GC.</span><span class="sxs-lookup"><span data-stu-id="ba93c-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subtrees DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="ba93c-255">Subtrees DOM</span><span class="sxs-lookup"><span data-stu-id="ba93c-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ba93c-256">Примеры. Попробуйте пример утечки [узла DOM,][GlitchDevtoolsMemoryExample06] чтобы понять, где он может протекать и как его обнаружить.</span><span class="sxs-lookup"><span data-stu-id="ba93c-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="ba93c-257">Вы также можете посмотреть на этот пример [утечки DOM больше, чем ожидалось][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="ba93c-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="ba93c-258">Дополнительные новости об утечках doM и основах анализа памяти при поиске и отладке утечек памяти с помощью [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] от Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="ba93c-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ba93c-259">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba93c-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Размеры объектов — терминология памяти | Документы Майкрософт"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Объекты сохранения дерева — терминология памяти | Документы Майкрософт"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html — Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "память | Слайды"  

> [!NOTE]
> <span data-ttu-id="ba93c-269">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba93c-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ba93c-270">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) и является автором [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="ba93c-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ba93c-272">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ba93c-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
