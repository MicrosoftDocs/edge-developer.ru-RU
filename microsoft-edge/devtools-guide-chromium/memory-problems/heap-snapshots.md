---
title: Запись моментальных снимков кучи
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: e6f64b219bc2b28d01780c28cc605d56a07cb491
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611680"
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





# <span data-ttu-id="f8ff2-103">Запись моментальных снимков кучи</span><span class="sxs-lookup"><span data-stu-id="f8ff2-103">How to Record Heap Snapshots</span></span>   



<span data-ttu-id="f8ff2-104">Узнайте, как записывать моментальные снимки кучи с помощью профилировщика Microsoft Edge DevTools и поиска утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="f8ff2-105">Профилировщик кучи Microsoft Edge DevTools показывает распределение памяти по объектам JavaScript и связанным узлам DOM на странице.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="f8ff2-106">Используйте его для создания моментальных снимков JavaScript \ (JS-файлов, кучи и т. д.), анализа графов памяти, сравнения снимков и поиска утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="f8ff2-107">Смотрите также [объекты][DevtoolsMemoryProblems101ObjectsRetainingTree], которые хранятся в дереве.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="f8ff2-108">Создание снимка</span><span class="sxs-lookup"><span data-stu-id="f8ff2-108">Take a snapshot</span></span>  

<span data-ttu-id="f8ff2-109">На панели **память** выберите команду **сделать снимок**, а затем нажмите кнопку **начать**.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="f8ff2-110">Вы также можете нажать клавиши `Ctrl` + `E` \ (Windows \) или `Cmd` + `E` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

> ##### <span data-ttu-id="f8ff2-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="f8ff2-111">Figure 1</span></span>  
> <span data-ttu-id="f8ff2-112">Выбор типа профилирования</span><span class="sxs-lookup"><span data-stu-id="f8ff2-112">Select profiling type</span></span>  
> ![Выбор типа профилирования][ImageProfilingType]  

<span data-ttu-id="f8ff2-114">**Моментальные снимки** первоначально хранятся в памяти процесса обработчика.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="f8ff2-115">При необходимости снимки переносятся в DevTools по запросу, если щелкнуть значок снимка, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="f8ff2-116">После того как вы загрузили моментальный снимок в DevTools и проанализируете его, появится число под заголовком снимка, в котором будет показан [Общий размер достижимых объектов JavaScript][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

> ##### <span data-ttu-id="f8ff2-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="f8ff2-117">Figure 2</span></span>  
> <span data-ttu-id="f8ff2-118">Общий размер достижимых объектов</span><span class="sxs-lookup"><span data-stu-id="f8ff2-118">Total size of reachable objects</span></span>  
> ![Общий размер достижимых объектов][ImageTotalSize]  

> [!NOTE]
> <span data-ttu-id="f8ff2-120">В снимки включаются только достижимые объекты.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-120">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="f8ff2-121">Кроме того, создание моментального снимка всегда начинается со сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-121">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="f8ff2-122">Очистка снимков</span><span class="sxs-lookup"><span data-stu-id="f8ff2-122">Clear snapshots</span></span>  

<span data-ttu-id="f8ff2-123">Нажмите кнопку **Очистить все профили** , чтобы удалить снимки \ (как из DevTools, так и из памяти, связанной с процессом рендеринга \).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-123">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

> ##### <span data-ttu-id="f8ff2-124">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="f8ff2-124">Figure 3</span></span>  
> <span data-ttu-id="f8ff2-125">Удаление снимков</span><span class="sxs-lookup"><span data-stu-id="f8ff2-125">Remove snapshots</span></span>  
> ![Удаление снимков][ImageRemoveSnapshots]  

<span data-ttu-id="f8ff2-127">Закрытие окна DevTools не приводит к удалению профилей из памяти, связанной с процессом рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-127">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="f8ff2-128">При повторном открытии DevTools все ранее созданные моментальные снимки снова появляются в списке снимков.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-128">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="f8ff2-129">Попробуйте этот пример [геоточечных объектов][GlitchDevtoolsMemoryExample03] и пропрофилировать его с помощью профилировщика кучи.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-129">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="f8ff2-130">Вы увидите число выделений элементов \ (объект \).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-130">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="f8ff2-131">Просмотр снимков</span><span class="sxs-lookup"><span data-stu-id="f8ff2-131">View snapshots</span></span>  

<span data-ttu-id="f8ff2-132">Просмотр снимков с разных точек зрения для разных задач.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-132">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="f8ff2-133">В **представлении "Сводка** " отображаются объекты, сгруппированные по имени конструктора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-133">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="f8ff2-134">Используйте его для поиска объектов \ (и использование памяти \) в зависимости от типа, сгруппированного по имени конструктора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-134">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="f8ff2-135">Это особенно полезно для **отслеживания УТЕЧЕК DOM**.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-135">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="f8ff2-136">**Представление сравнения**.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-136">**Comparison view**.</span></span>  <span data-ttu-id="f8ff2-137">Показывает разницу между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-137">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="f8ff2-138">Используйте его для сравнения двух (или более) моментальных снимков памяти от до и после выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-138">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="f8ff2-139">Проверка дельты в освобожденной памяти и счетчике ссылок позволяет вам подтвердить присутствие и причину утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-139">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="f8ff2-140">**Представление "вложение**".</span><span class="sxs-lookup"><span data-stu-id="f8ff2-140">**Containment view**.</span></span>  <span data-ttu-id="f8ff2-141">Позволяет исследовать содержимое кучи.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-141">Allows exploration of heap contents.</span></span>  <span data-ttu-id="f8ff2-142">**Представление "вложение** " обеспечивает более эффективное представление структуры объектов, помогая анализировать объекты, на которые ссылается глобальное пространство имен \ (окно \), чтобы узнать, что такое хранение объектов.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-142">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="f8ff2-143">Используйте его для анализа замыканий и пошагового углубления объектов на низком уровне.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-143">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="f8ff2-144">Для переключения между представлениями Используйте селектор в верхней части представления.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-144">To switch between views, use the selector at the top of the view.</span></span>  

> ##### <span data-ttu-id="f8ff2-145">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="f8ff2-145">Figure 4</span></span>  
> <span data-ttu-id="f8ff2-146">Переключатель выбора представлений</span><span class="sxs-lookup"><span data-stu-id="f8ff2-146">Switch views selector</span></span>  
> ![Переключатель выбора представлений][ImageSwitchViews]  

> [!NOTE]
> <span data-ttu-id="f8ff2-148">Не все свойства хранятся в куче JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-148">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="f8ff2-149">Свойства, реализованные с помощью методов доступа, которые выполняют машинный код, не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-149">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="f8ff2-150">Кроме того, не записываются значения, не являющиеся строками, например числа.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-150">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="f8ff2-151">Представление сводки</span><span class="sxs-lookup"><span data-stu-id="f8ff2-151">Summary view</span></span>  

<span data-ttu-id="f8ff2-152">Изначально в представлении сводки открывается моментальный снимок, в котором отображаются итоговые объекты, которые могут быть развернуты для отображения экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-152">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

> ##### <span data-ttu-id="f8ff2-153">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="f8ff2-153">Figure 5</span></span>  
> <span data-ttu-id="f8ff2-154">Представление сводки</span><span class="sxs-lookup"><span data-stu-id="f8ff2-154">Summary view</span></span>  
> ![Представление сводки][ImageSummaryView]  

<span data-ttu-id="f8ff2-156">Элементы верхнего уровня — строки "Итого".</span><span class="sxs-lookup"><span data-stu-id="f8ff2-156">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="f8ff2-157">Элементы верхнего уровня</span><span class="sxs-lookup"><span data-stu-id="f8ff2-157">Top-level entries</span></span> | <span data-ttu-id="f8ff2-158">Описание</span><span class="sxs-lookup"><span data-stu-id="f8ff2-158">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="f8ff2-159">Конструктор</span><span class="sxs-lookup"><span data-stu-id="f8ff2-159">Constructor</span></span>** | <span data-ttu-id="f8ff2-160">Представляет все объекты, созданные с помощью этого конструктора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-160">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="f8ff2-161">Расстояние</span><span class="sxs-lookup"><span data-stu-id="f8ff2-161">Distance</span></span>** | <span data-ttu-id="f8ff2-162">показывает расстояние до корня с минимальным простым путем к узлам.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-162">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="f8ff2-163">Неглубокий размер</span><span class="sxs-lookup"><span data-stu-id="f8ff2-163">Shallow size</span></span>** | <span data-ttu-id="f8ff2-164">Отображает сумму мелких размеров всех объектов, созданных с помощью определенной функции конструктора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-164">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="f8ff2-165">Неглубокий размер — это размер памяти, занимаемой объектом, (обычно массивы и строки имеют более мелких размеров).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-165">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="f8ff2-166">Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="f8ff2-167">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="f8ff2-167">Retained size</span></span>** | <span data-ttu-id="f8ff2-168">Отображение максимального размера в одном наборе объектов.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-168">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="f8ff2-169">Объем памяти, который вы можете освобождать после удаления объекта \ (а зависимые элементы становятся недостижимыми \), называется сохраненным размером.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-169">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="f8ff2-170">Смотрите также [размеры объектов][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-170">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="f8ff2-171">После того как вы разворачиваете итоговую строку в верхнем представлении, отобразятся все экземпляры.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-171">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="f8ff2-172">Для каждого экземпляра в соответствующих столбцах отображаются неполные и удержанные размеры.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-172">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="f8ff2-173">Число после `@` символа является уникальным идентификатором объекта, что позволяет сравнивать моментальные снимки кучи на отдельных объектах.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-173">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="f8ff2-174">Обратите внимание, что желтые объекты содержат ссылки на JavaScript, а красные объекты — это отсоединенные узлы, на которые ссылается один из них с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-174">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="f8ff2-175">Что в профилировщике кучи соотносятся различные элементы конструктора \ (Group \)?</span><span class="sxs-lookup"><span data-stu-id="f8ff2-175">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

> ##### <span data-ttu-id="f8ff2-176">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="f8ff2-176">Figure 6</span></span>  
> <span data-ttu-id="f8ff2-177">Группы конструкторов</span><span class="sxs-lookup"><span data-stu-id="f8ff2-177">Constructor groups</span></span>  
> ![Группы конструкторов][ImageConstructorGroups]  

| <span data-ttu-id="f8ff2-179">Элемент Конструктор \ (группировка)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-179">Constructor \(group\) entry</span></span> | <span data-ttu-id="f8ff2-180">Описание</span><span class="sxs-lookup"><span data-stu-id="f8ff2-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="f8ff2-181">\ (глобальное свойство)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-181">\(global property\)</span></span>** | <span data-ttu-id="f8ff2-182">Промежуточные объекты между глобальным объектом (например, `window` \) и объектом, на который ссылается этот объект.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-182">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="f8ff2-183">Если объект создается с помощью конструктора `Person` и удерживается глобальным объектом, путь сохранения будет выглядеть так, как нужно `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="f8ff2-183">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="f8ff2-184">Это отличается от нормы, где объекты непосредственно ссылаются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-184">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="f8ff2-185">Промежуточные объекты существуют для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-185">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="f8ff2-186">Глобальные объекты регулярно изменяются, а оптимизации доступа к свойствам являются хорошим заданием для неглобальных объектов, неприменимо для глобальных.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-186">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="f8ff2-187">\ (корни \)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-187">\(roots\)</span></span>** | <span data-ttu-id="f8ff2-188">Корневые элементы в представлении в виде дерева сохраняются как сущности, которые содержат ссылки на выбранный объект.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-188">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="f8ff2-189">Записи могут также содержать ссылки, созданные ядром для целей, специфических для ядра.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-189">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="f8ff2-190">Ядро содержит кэш, в котором есть ссылки на объекты, но все такие ссылки являются слабыми и не запрещают сбору объекта с учетом того, что нет действительно строгой ссылки.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-190">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="f8ff2-191">\ (замыкание)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-191">\(closure\)</span></span>** | <span data-ttu-id="f8ff2-192">Количество ссылок на группу объектов с помощью замыкания функций.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-192">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="f8ff2-193">\ (массив, строка, число, regexp)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-193">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="f8ff2-194">Список типов объектов со свойствами, которые ссылаются на массив, строку, число или регулярное выражение.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-194">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="f8ff2-195">\ (скомпилированный код)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-195">\(compiled code\)</span></span>** | <span data-ttu-id="f8ff2-196">Все, что связано с компилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-196">Everything related to compiled code.</span></span>  <span data-ttu-id="f8ff2-197">Сценарий похож на функцию, но соответствует `<script>` телу.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-197">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="f8ff2-198">SharedFunctionInfos \ (SFI \) — объекты, зафиксированные между функциями и скомпилированным кодом.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-198">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="f8ff2-199">У функций обычно есть контекст, а не SFIs.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-199">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="f8ff2-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**и т. д.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="f8ff2-201">Ссылки на элементы или объекты документа определенного типа, на которые ссылается ваш код.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-201">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="f8ff2-202">Представление "Сравнение"</span><span class="sxs-lookup"><span data-stu-id="f8ff2-202">Comparison view</span></span>  

<span data-ttu-id="f8ff2-203">Находить потерянные объекты, сравнивая несколько моментальных снимков друг с другом.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-203">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="f8ff2-204">Чтобы убедиться в том, что определенная операция приложения не создает утечки \ (например, при открытии документа, а затем его закрытии), не следует оставлять все сборки мусора, вы можете воспользоваться приведенным ниже сценарием.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-204">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="f8ff2-205">Сделайте снимок кучи, прежде чем выполнять операцию.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-205">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="f8ff2-206">Выполнение операции \ (взаимодействие с страницей в некоторых условиях, когда вы считаете, что она вызывает утечку).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-206">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="f8ff2-207">Выполните обратную операцию, чтобы (выполнить обратное взаимодействие и повторить ее несколько раз).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-207">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="f8ff2-208">Сделайте второй снимок кучи и измените его представление на **Сравнение**, сравнив его с **снимком 1**.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-208">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  

<span data-ttu-id="f8ff2-209">В представлении **Сравнение** отображается разница между двумя снимками.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-209">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="f8ff2-210">При развертывании элемента общего типа отображаются добавленные и удаленные экземпляры объекта.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-210">When expanding a total entry, added and deleted object instances are shown.</span></span>  

> ##### <span data-ttu-id="f8ff2-211">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="f8ff2-211">Figure 7</span></span>  
> <span data-ttu-id="f8ff2-212">Представление "Сравнение"</span><span class="sxs-lookup"><span data-stu-id="f8ff2-212">Comparison view</span></span>  
> ![Представление "Сравнение"][ImageComparisonView]  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="f8ff2-214">Представление "вложение"</span><span class="sxs-lookup"><span data-stu-id="f8ff2-214">Containment view</span></span>  

<span data-ttu-id="f8ff2-215">Представление " **вложение** " — это по сути представление "глаз с высоты птичьего полета" для структуры объектов приложения.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-215">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="f8ff2-216">Это позволяет просматривать замыкания функций внутри функции, чтобы отслеживать внутренние объекты виртуальной машины \ (VM \), которые вместе составляют объекты JavaScript, и понять, какая память используется приложением на очень низком уровне.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-216">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="f8ff2-217">Точки входа в Просмотр вложений</span><span class="sxs-lookup"><span data-stu-id="f8ff2-217">Containment view entry points</span></span> | <span data-ttu-id="f8ff2-218">Описание</span><span class="sxs-lookup"><span data-stu-id="f8ff2-218">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="f8ff2-219">Объекты DOMWindow</span><span class="sxs-lookup"><span data-stu-id="f8ff2-219">DOMWindow objects</span></span>** | <span data-ttu-id="f8ff2-220">Глобальные объекты для кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-220">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="f8ff2-221">Корни GC</span><span class="sxs-lookup"><span data-stu-id="f8ff2-221">GC roots</span></span>** | <span data-ttu-id="f8ff2-222">Фактические корни GC, используемые сборкой мусора ВМ.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-222">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="f8ff2-223">Корни GC состоят из встроенных карт объектов, таблиц символов, стеков потоков виртуальной машины, кэшей компиляций, областей обработки и глобальных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-223">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="f8ff2-224">Собственные объекты</span><span class="sxs-lookup"><span data-stu-id="f8ff2-224">Native objects</span></span>** | <span data-ttu-id="f8ff2-225">Объекты браузера "отправили" на виртуальной машине JavaScript \ (JavaScript VM \), чтобы разрешить автоматизацию, например узлы DOM, правила CSS.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-225">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

> ##### <span data-ttu-id="f8ff2-226">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="f8ff2-226">Figure 8</span></span>  
> <span data-ttu-id="f8ff2-227">Представление "вложение"</span><span class="sxs-lookup"><span data-stu-id="f8ff2-227">Containment view</span></span>  
> ![Представление "вложение"][ImageContainmentView]  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="f8ff2-229">Всплывающая подсказка о замыканиях.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-229">A tip about closures.</span></span>  <span data-ttu-id="f8ff2-230">Назовите функции таким образом, чтобы можно было легко отличать между собой замыкания в снимке.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-230">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="f8ff2-231">Например, в этом примере не используются именованные функции.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-231">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="f8ff2-232">В этом примере используются именованные функции.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-232">This example uses named functions:</span></span>  
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
> > ##### old Figure 9  
> > Name functions to distinguish between closures  
> > ![Name functions to distinguish between closures][ImageDomLeaks]  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="f8ff2-233">Попробуйте этот пример, чтобы [можно `eval` было][GlitchDevtoolsMemoryExample07] проанализировать влияние замыканий на память.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-233">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="f8ff2-234">Кроме того, вам может потребоваться подписаться на этот пример, в котором осуществляется запись [ресурсов кучи][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-234">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="f8ff2-235">Поиск цветового кодирования</span><span class="sxs-lookup"><span data-stu-id="f8ff2-235">Look up color coding</span></span>  

<span data-ttu-id="f8ff2-236">Свойства и значения свойств объектов имеют различные типы и окрашены соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-236">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="f8ff2-237">Каждое свойство имеет один из четырех типов.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-237">Each property has one of four types.</span></span>  

| <span data-ttu-id="f8ff2-238">Тип свойства</span><span class="sxs-lookup"><span data-stu-id="f8ff2-238">Property Type</span></span> | <span data-ttu-id="f8ff2-239">Описание</span><span class="sxs-lookup"><span data-stu-id="f8ff2-239">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="f8ff2-240">a: свойство</span><span class="sxs-lookup"><span data-stu-id="f8ff2-240">a: property</span></span>** | <span data-ttu-id="f8ff2-241">Обычное свойство с именем, доступ к которому осуществляется с помощью `.` оператора \ (точка) или через `[` `]` \ (квадратные скобки \), например `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="f8ff2-241">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="f8ff2-242">0: элемент</span><span class="sxs-lookup"><span data-stu-id="f8ff2-242">0: element</span></span>** | <span data-ttu-id="f8ff2-243">Регулярное свойство с числовым индексом, доступ к которому осуществляется через `[` `]` представление \ (скобки).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-243">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="f8ff2-244">a: VAR (контекст)</span><span class="sxs-lookup"><span data-stu-id="f8ff2-244">a: context var</span></span>** |  <span data-ttu-id="f8ff2-245">Переменная в контексте функции, доступная по имени переменной из замыкания функции.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-245">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="f8ff2-246">a: System Prop</span><span class="sxs-lookup"><span data-stu-id="f8ff2-246">a: system prop</span></span>** | <span data-ttu-id="f8ff2-247">Свойство, добавленное виртуальной машиной JavaScript, недоступно из кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-247">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="f8ff2-248">Объекты, помеченные как не `System` имеющие соответствующего типа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-248">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="f8ff2-249">Каждый из них является частью реализации объектной системы виртуальной машины JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-249">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="f8ff2-250">V8 выделяет большинство внутренних объектов в той же куче, где находятся объекты JS пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-250">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="f8ff2-251">Итак, это только внутренние V8.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-251">So these are just V8 internals.</span></span>  

## <span data-ttu-id="f8ff2-252">Поиск конкретного объекта</span><span class="sxs-lookup"><span data-stu-id="f8ff2-252">Find a specific object</span></span>  

<span data-ttu-id="f8ff2-253">Чтобы найти объект в собранной куче, вы можете найти его с помощью `Ctrl` + `F` и присвоить ему идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-253">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="f8ff2-254">Обнаружение утечек DOM</span><span class="sxs-lookup"><span data-stu-id="f8ff2-254">Uncover DOM leaks</span></span>  

<span data-ttu-id="f8ff2-255">Профилировщик кучи может отображать двунаправленные зависимости между собственными объектами браузера \ (узлы DOM, правила CSS \) и объекты JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-255">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="f8ff2-256">Это помогает выявить невидимые утечки, происходящие из-за плавающего отсоединенного поддерева DOM.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-256">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="f8ff2-257">Утечки DOM могут быть больше, чем вы думаете.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-257">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="f8ff2-258">Вот пример.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-258">Consider the following sample.</span></span>  <span data-ttu-id="f8ff2-259">Когда #tree GC?</span><span class="sxs-lookup"><span data-stu-id="f8ff2-259">When is the #tree GC?</span></span>  

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

<span data-ttu-id="f8ff2-260">Функция `#leaf` хранит ссылку на подходящую родительскую структуру \ (ParentNode \) и рекурсивно `#tree` дополнить, так что только в том случае, если leafRef является nullified — это всего лишь дерево с `#tree` кандидатом на сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-260">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

> ##### <span data-ttu-id="f8ff2-261">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="f8ff2-261">Figure 9</span></span>  
> <span data-ttu-id="f8ff2-262">Поддерево DOM</span><span class="sxs-lookup"><span data-stu-id="f8ff2-262">DOM subtrees</span></span>  
> <span data-ttu-id="f8ff2-263">! [Поддеревья DOM] [ImageTreeGc]</span><span class="sxs-lookup"><span data-stu-id="f8ff2-263">![DOM subtrees][ImageTreeGc]</span></span>  

> [!NOTE]
> <span data-ttu-id="f8ff2-264">Примеры: попробуйте этот пример [утечки узла DOM][GlitchDevtoolsMemoryExample06] , чтобы понять, где она может быть потеряна и как ее найти.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-264">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="f8ff2-265">Кроме того, вы можете просмотреть этот пример [утечек DOM больше, чем ожидалось][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-265">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="f8ff2-266">Для получения дополнительных сведений о утечках DOM и анализе памяти ознакомьтесь с разделом извлечение [и отладка утечек памяти с помощью Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] , Gonzalo Ruiz De Villa.</span><span class="sxs-lookup"><span data-stu-id="f8ff2-266">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageProfilingType]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png "Рисунок 1: Выбор типа профилирования"  
[ImageTotalSize]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png "Рисунок 2: общий размер достижимых объектов"  
[ImageRemoveSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png "Рисунок 3: удаление моментальных снимков"  
[ImageSwitchViews]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png "Рисунок 4: переключение режима выбора представлений"  
[ImageSummaryView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png "Рисунок 5: представление "Сводка""  
[ImageConstructorGroups]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png "Рисунок 6: группы конструкторов"  
[ImageComparisonView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png "Рисунок 7: сравнительный режим"  
[ImageContainmentView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png "Рисунок 8: режим вложения"  
<!--[ImageDomLeaks]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-domleaks.msft.png "old Figure 9: Name functions to distinguish between closures"  -->  
[ImageTreeGc]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Memory-Problems-Tree-GC.MSFT.png "Рисунок 9: поддерево DOM"  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#object-sizes "Размеры объектов — терминология с памятью"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#objects-retaining-tree "Объекты, которые сохраняют терминологию в структуре памяти"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "Example-03. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "Example-06. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "Example-07. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "Example-08. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "Example-09. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "Example-10. HTML — Microsoft EDGE (Chromium) DevTools | Цепь"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "память | Закончен"  

> [!NOTE]
> <span data-ttu-id="f8ff2-285">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f8ff2-286">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="f8ff2-286">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f8ff2-288">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f8ff2-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
