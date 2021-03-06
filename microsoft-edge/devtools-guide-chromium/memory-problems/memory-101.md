---
description: В этом разделе описываются общие термины, используемые при анализе памяти, и применимы к различным средствам профилинга памяти для разных языков.
title: Терминология памяти
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1579374be29f0f419ded3bf88f5dea284f0bbb1a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397792"
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
   limitations under the License. -->

# <a name="memory-terminology"></a><span data-ttu-id="4ed73-104">Терминология памяти</span><span class="sxs-lookup"><span data-stu-id="4ed73-104">Memory terminology</span></span>  

<span data-ttu-id="4ed73-105">В этой статье описываются общие термины, используемые в анализе памяти, и применимы к различным средствам профилинга памяти для разных языков.</span><span class="sxs-lookup"><span data-stu-id="4ed73-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="4ed73-106">Термины и понятия, описанные здесь, относятся к панели [Памяти.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="4ed73-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="4ed73-107">Если вы когда-либо работали с Java, .NET или другим профилем памяти, то эта статья может быть обновлением.</span><span class="sxs-lookup"><span data-stu-id="4ed73-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="4ed73-108">Размеры объектов</span><span class="sxs-lookup"><span data-stu-id="4ed73-108">Object sizes</span></span>  

<span data-ttu-id="4ed73-109">Подумайте о памяти как о графике с примитивными типами \(например, числами и строками\) и объектами \(ассоциативными массивами\).</span><span class="sxs-lookup"><span data-stu-id="4ed73-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="4ed73-110">Он может отображаться как график со многими взаимосвязанными точками, такими как следующая фигура.</span><span class="sxs-lookup"><span data-stu-id="4ed73-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Визуальное представление памяти" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="4ed73-112">Визуальное представление памяти</span><span class="sxs-lookup"><span data-stu-id="4ed73-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="4ed73-113">Объект может удерживать память двумя способами:</span><span class="sxs-lookup"><span data-stu-id="4ed73-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="4ed73-114">Непосредственно по объекту.</span><span class="sxs-lookup"><span data-stu-id="4ed73-114">Directly by the object.</span></span>  
*   <span data-ttu-id="4ed73-115">Неявно путем удержания ссылок на другие объекты и, следовательно, предотвращения автоматического утилизации этих объектов сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="4ed73-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="4ed73-116">При работе с панелью [памяти][DevtoolsMemoryProblemsHeapSnapshots] в DevTools \(средство для расследования проблем памяти, найденных в **Memory**\), вы можете найти себе, глядя на несколько различных столбцов информации.</span><span class="sxs-lookup"><span data-stu-id="4ed73-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="4ed73-117">Два, которые выделяются **являются Неглубокий размер** и **сохраненный**размер, но что они представляют?</span><span class="sxs-lookup"><span data-stu-id="4ed73-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Неглубокий и сохраненный размер" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="4ed73-119">Неглубокий и сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="4ed73-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="4ed73-120">Неглубокий размер</span><span class="sxs-lookup"><span data-stu-id="4ed73-120">Shallow size</span></span>  

<span data-ttu-id="4ed73-121">Это размер памяти, удерживаемой объектом.</span><span class="sxs-lookup"><span data-stu-id="4ed73-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="4ed73-122">Типичные объекты JavaScript имеют некоторую память, зарезервированную для их описания и для хранения немедленных значений.</span><span class="sxs-lookup"><span data-stu-id="4ed73-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="4ed73-123">Как правило, только массивы и строки могут иметь значительный неглубокий размер.</span><span class="sxs-lookup"><span data-stu-id="4ed73-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="4ed73-124">Однако строки и внешние массивы часто имеют основное хранилище в памяти отрисовщика, что создает только небольшой объект оболочки на кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ed73-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="4ed73-125">Память renderer — это вся память процесса, в котором отрисовка проинспектировали страницу: родной памяти + JS кучи памяти страницы + JS кучи памяти всех выделенных рабочих, запущенных на странице.</span><span class="sxs-lookup"><span data-stu-id="4ed73-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="4ed73-126">Тем не менее даже небольшой объект может удерживать большое количество памяти косвенно, предотвращая утилизацию других объектов с помощью автоматического процесса сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="4ed73-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="4ed73-127">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="4ed73-127">Retained size</span></span>  

<span data-ttu-id="4ed73-128">Это размер памяти, которая освободилась после удаления объекта вместе с зависимыми объектами, которые были недоступны из корней **коллектора мусора.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="4ed73-129">**Корневой сборщик** мусора \*\*\*\* состоит из дескрипторов, созданных \(локальный или глобальный\) при создании ссылки из родного кода на объект JavaScript за пределами V8.</span><span class="sxs-lookup"><span data-stu-id="4ed73-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="4ed73-130">Все такие ручки можно найти в снимке кучи в области **обработки**корней GC и  >  \*\*\*\* **корней GC**  >  **Global handles.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="4ed73-131">Описание обработок в этой документации без погружения в детали реализации браузера может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="4ed73-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="4ed73-132">И корни коллектора мусора, и ручки не являются чем-то, о чем вам нужно беспокоиться.</span><span class="sxs-lookup"><span data-stu-id="4ed73-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="4ed73-133">Существует множество внутренних корней сборщика мусора, большинство из которых не интересны пользователям.</span><span class="sxs-lookup"><span data-stu-id="4ed73-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="4ed73-134">С точки зрения приложений существуют следующие типы корней.</span><span class="sxs-lookup"><span data-stu-id="4ed73-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="4ed73-135">Объект Window global \(в каждом iframe\).</span><span class="sxs-lookup"><span data-stu-id="4ed73-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="4ed73-136">В снимках кучи имеется поле расстояния, которое является числом ссылок свойств на самом коротком пути сохранения из окна.</span><span class="sxs-lookup"><span data-stu-id="4ed73-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="4ed73-137">Дерево DOM документа, состоящее из всех родных узлов DOM, до которых можно добраться, обходя документ.</span><span class="sxs-lookup"><span data-stu-id="4ed73-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="4ed73-138">Не все узлы могут иметь Обертки JS, но если узел имеет оболочку, он жив, пока документ жив.</span><span class="sxs-lookup"><span data-stu-id="4ed73-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="4ed73-139">Иногда объекты могут сохраняться контекстом отладки в панели **Источники** и консоли \*\*\*\* \(например, после оценки консоли\).</span><span class="sxs-lookup"><span data-stu-id="4ed73-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="4ed73-140">Создайте снимки кучи с помощью очищенной панели **консоли** и без активных точек взлома в отладке в панели **Источники.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="4ed73-141">Сними **панель Консоли,** задействуя и отключая точки разлома в панели Источники, прежде чем принимать снимок кучи `clear()` в панели [памяти.][DevtoolsMemoryProblemsHeapSnapshots] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4ed73-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="4ed73-142">Граф памяти начинается с корневого, который может быть объектом браузера или объектом `window` `Global` Node.js модуля.</span><span class="sxs-lookup"><span data-stu-id="4ed73-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="4ed73-143">Вы не контролируете, как этот корневой объект собирает мусор.</span><span class="sxs-lookup"><span data-stu-id="4ed73-143">You do not control how this root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Вы не можете контролировать, как собираются корневые объекты мусора." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="4ed73-145">Вы не можете контролировать, как собираются корневые объекты мусора.</span><span class="sxs-lookup"><span data-stu-id="4ed73-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="4ed73-146">Все, что невозможно получить из корневого корня, получает собранный мусор.</span><span class="sxs-lookup"><span data-stu-id="4ed73-146">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ed73-147">Столбцы ["Мелкий размер"](#shallow-size) и ["Сохраненный](#retained-size) размер" представляют данные в bytes.</span><span class="sxs-lookup"><span data-stu-id="4ed73-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="4ed73-148">Объекты, удерживающие дерево</span><span class="sxs-lookup"><span data-stu-id="4ed73-148">Objects retaining tree</span></span>  

<span data-ttu-id="4ed73-149">Куча — это сеть взаимосвязанных объектов.</span><span class="sxs-lookup"><span data-stu-id="4ed73-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="4ed73-150">В математическом мире эта структура называется **графом или** графиком памяти.</span><span class="sxs-lookup"><span data-stu-id="4ed73-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="4ed73-151">Граф строится из **узлов, подключенных** с помощью краев, \*\*\*\* оба из которых даются метки.</span><span class="sxs-lookup"><span data-stu-id="4ed73-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="4ed73-152">**Узлы** \(или **объекты**\) помечены с помощью имени функции **конструктора,** которая использовалась для их создания.</span><span class="sxs-lookup"><span data-stu-id="4ed73-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="4ed73-153">**Края помечены** с помощью имен **свойств.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="4ed73-154">Узнайте, [как записывать профиль с помощью профайла кучи.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="4ed73-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="4ed73-155">На следующем рисунке некоторые заметные моментальные записи [][DevtoolsMemoryProblemsHeapSnapshots] в инструменте Памяти включают расстояние: расстояние до корневого коллектора мусора.</span><span class="sxs-lookup"><span data-stu-id="4ed73-155">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="4ed73-156">Если почти все объекты одного типа находятся на одном расстоянии, а некоторые находятся на более большом расстоянии, это то, что стоит и расследовать.</span><span class="sxs-lookup"><span data-stu-id="4ed73-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Расстояние от корневого" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="4ed73-158">Расстояние от корневого</span><span class="sxs-lookup"><span data-stu-id="4ed73-158">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="4ed73-159">Dominators</span><span class="sxs-lookup"><span data-stu-id="4ed73-159">Dominators</span></span>  

<span data-ttu-id="4ed73-160">Объекты Dominator состоят из структуры дерева, так как каждый объект имеет точно один доминатор.</span><span class="sxs-lookup"><span data-stu-id="4ed73-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="4ed73-161">У доминатора объекта может не быть прямых ссылок на объект, в котором он доминирует; то есть дерево доминатора не является охватывающим деревом графа.</span><span class="sxs-lookup"><span data-stu-id="4ed73-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="4ed73-162">На следующем рисунке верно следующее утверждение.</span><span class="sxs-lookup"><span data-stu-id="4ed73-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="4ed73-163">Узел 1 доминирует над узлом 2</span><span class="sxs-lookup"><span data-stu-id="4ed73-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="4ed73-164">Узел 2 доминирует над узлами 3, 4 и 6</span><span class="sxs-lookup"><span data-stu-id="4ed73-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="4ed73-165">Узел 3 доминирует над узлом 5</span><span class="sxs-lookup"><span data-stu-id="4ed73-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="4ed73-166">Узел 5 доминирует над узлом 8</span><span class="sxs-lookup"><span data-stu-id="4ed73-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="4ed73-167">Узел 6 доминирует над узлом 7</span><span class="sxs-lookup"><span data-stu-id="4ed73-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Структура дерева Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="4ed73-169">Структура дерева Dominator</span><span class="sxs-lookup"><span data-stu-id="4ed73-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="4ed73-170">На следующем рисунке узел является доминантом , но также существует в каждом простом пути `#3` `#10` от `#7` коллектора мусора до `#10` .</span><span class="sxs-lookup"><span data-stu-id="4ed73-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="4ed73-171">Таким образом, объект B является доминантом объекта A, если B существует в каждом простом пути от корневого к объекту A.</span><span class="sxs-lookup"><span data-stu-id="4ed73-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Анимированные иллюстрации доминатора" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="4ed73-173">Анимированные иллюстрации доминатора</span><span class="sxs-lookup"><span data-stu-id="4ed73-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="4ed73-174">Особенности V8</span><span class="sxs-lookup"><span data-stu-id="4ed73-174">V8 specifics</span></span>  

<span data-ttu-id="4ed73-175">При профилирование памяти полезно понять, почему снимки кучи выглядят определенным образом.</span><span class="sxs-lookup"><span data-stu-id="4ed73-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="4ed73-176">В этом разделе описываются некоторые темы, связанные с памятью, соответствующие виртуальной машине **V8 JavaScript** \(V8 VM или VM\).</span><span class="sxs-lookup"><span data-stu-id="4ed73-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="4ed73-177">Представление объектов JavaScript</span><span class="sxs-lookup"><span data-stu-id="4ed73-177">JavaScript object representation</span></span>  

<span data-ttu-id="4ed73-178">Существует три примитивных типа:</span><span class="sxs-lookup"><span data-stu-id="4ed73-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="4ed73-179">Номера `3.14159...` \(например\)</span><span class="sxs-lookup"><span data-stu-id="4ed73-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="4ed73-180">Booleans \( `true` или `false` \)</span><span class="sxs-lookup"><span data-stu-id="4ed73-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="4ed73-181">Строки `"Werner Heisenberg"` \(например\)</span><span class="sxs-lookup"><span data-stu-id="4ed73-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="4ed73-182">Примитивы не могут ссылаться на другие значения и всегда являются листами или завершающие узлы.</span><span class="sxs-lookup"><span data-stu-id="4ed73-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="4ed73-183">**Номера** могут храниться так же:</span><span class="sxs-lookup"><span data-stu-id="4ed73-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="4ed73-184">немедленные 31-битные значения, называемые небольшими дополнительными **значениями** \(**SMI**s\), или</span><span class="sxs-lookup"><span data-stu-id="4ed73-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="4ed73-185">кучи объектов, именуемых **кучи номеров**.</span><span class="sxs-lookup"><span data-stu-id="4ed73-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="4ed73-186">Кучи номера используются для хранения значений, не вписывающихся в форму SMI, таких как двойные **значения,** или когда значение должно быть в **поле,** например, параметр свойства на нем.</span><span class="sxs-lookup"><span data-stu-id="4ed73-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="4ed73-187">**Строки** могут храниться в любом из них:</span><span class="sxs-lookup"><span data-stu-id="4ed73-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="4ed73-188">куча **VM**или</span><span class="sxs-lookup"><span data-stu-id="4ed73-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="4ed73-189">внешне в **памяти отрисовщика**.</span><span class="sxs-lookup"><span data-stu-id="4ed73-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="4ed73-190">Объект **оболочки** создается и используется для доступа к внешнему хранилищу, где, например, хранятся источники скриптов и другой контент, полученный из Интернета, а не копируется на кучи VM.</span><span class="sxs-lookup"><span data-stu-id="4ed73-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="4ed73-191">Память для новых объектов JavaScript выделяется из выделенной кучи JavaScript \(или **Кучи VM\).**</span><span class="sxs-lookup"><span data-stu-id="4ed73-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="4ed73-192">Эти объекты управляются сборщиком мусора в V8 и, следовательно, остаются в живых до тех пор, пока существует по крайней мере одна сильная ссылка на них.</span><span class="sxs-lookup"><span data-stu-id="4ed73-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="4ed73-193">Все, что не находится в кучи JavaScript, называется родным **объектом.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="4ed73-194">Местные объекты, в отличие от объектов куча, не управляются сборщиком мусора V8 в течение всего срока службы и могут быть доступны только из JavaScript с помощью объекта оболочки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ed73-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="4ed73-195">**Строка "Минусы"** — это объект, состоящий из пар строк, которые хранятся и затем присоединяются, и является результатом конкатуации.</span><span class="sxs-lookup"><span data-stu-id="4ed73-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="4ed73-196">Присоединение содержимого **строки "против"** происходит только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="4ed73-196">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="4ed73-197">Например, когда необходимо построить подстройку соединяемой строки.</span><span class="sxs-lookup"><span data-stu-id="4ed73-197">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="4ed73-198">Например, если вы одновременно и , вы получите `a` `b` `(a, b)` строку, которая представляет результат concatenation.</span><span class="sxs-lookup"><span data-stu-id="4ed73-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="4ed73-199">Если вы позже согласились с этим результатом, вы получите еще одну строку `d` **минусы**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="4ed73-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="4ed73-200">**Массив** — это объект с числовых клавишами.</span><span class="sxs-lookup"><span data-stu-id="4ed73-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="4ed73-201">**Массивы** широко используются в V8 VM для хранения больших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="4ed73-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="4ed73-202">Наборы пар значений ключей, например словари, имеют подстройки **массивами.**</span><span class="sxs-lookup"><span data-stu-id="4ed73-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="4ed73-203">Типичный объект JavaScript хранится в качестве только одного из двух **типов массивов:**</span><span class="sxs-lookup"><span data-stu-id="4ed73-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="4ed73-204">именуемые свойства и</span><span class="sxs-lookup"><span data-stu-id="4ed73-204">named properties, and</span></span>  
*   <span data-ttu-id="4ed73-205">числимые элементы</span><span class="sxs-lookup"><span data-stu-id="4ed73-205">numeric elements</span></span>  

<span data-ttu-id="4ed73-206">При небольшом количестве свойств свойства хранятся внутри объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ed73-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="4ed73-207">**Map** — это объект, который описывает как вид объекта, так и макет.</span><span class="sxs-lookup"><span data-stu-id="4ed73-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="4ed73-208">Например, карты используются для описания неявных иерархий объектов для [быстрого доступа к свойствам.][V8FastProperties]</span><span class="sxs-lookup"><span data-stu-id="4ed73-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="4ed73-209">Группы объектов</span><span class="sxs-lookup"><span data-stu-id="4ed73-209">Object groups</span></span>  

<span data-ttu-id="4ed73-210">Каждая **группа родных** объектов состоит из объектов, которые содержат взаимные ссылки друг на друга.</span><span class="sxs-lookup"><span data-stu-id="4ed73-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="4ed73-211">Рассмотрим, например, подтрибую DOM, где каждый узел имеет ссылку на родственника и ссылки на следующего ребенка и следующего родственника, образуя, таким образом, связанный график.</span><span class="sxs-lookup"><span data-stu-id="4ed73-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="4ed73-212">Коренные объекты не представлены в кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ed73-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="4ed73-213">Отсутствие представления является причиной нулевого размера родных объектов.</span><span class="sxs-lookup"><span data-stu-id="4ed73-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="4ed73-214">Вместо этого создаются объекты оболочки.</span><span class="sxs-lookup"><span data-stu-id="4ed73-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="4ed73-215">Каждый объект оболочки содержит ссылку на соответствующий родной объект для перенаправления команд на него.</span><span class="sxs-lookup"><span data-stu-id="4ed73-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="4ed73-216">В свою очередь, объектная группа содержит объекты оболочки.</span><span class="sxs-lookup"><span data-stu-id="4ed73-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="4ed73-217">Однако это не создает непостижимый цикл, так как сборщик мусора достаточно умен, чтобы освободить объектные группы, обертки которых больше не ссылались.</span><span class="sxs-lookup"><span data-stu-id="4ed73-217">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="4ed73-218">Но забыв о выпуске одной обертки содержит всю группу и связанные обертки.</span><span class="sxs-lookup"><span data-stu-id="4ed73-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4ed73-219">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4ed73-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Запись снимков кучи | Документы Майкрософт"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Быстрые свойства в V8 | V8"  

> [!NOTE]
> <span data-ttu-id="4ed73-222">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ed73-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4ed73-223">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) и является автором [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="4ed73-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4ed73-225">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4ed73-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
