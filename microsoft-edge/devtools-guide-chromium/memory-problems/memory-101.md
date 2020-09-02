---
title: Терминология памяти
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: cb258135b7b3c931116d84b1e9b7a548a2b58a6d
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986265"
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

# <span data-ttu-id="6657c-103">Терминология памяти</span><span class="sxs-lookup"><span data-stu-id="6657c-103">Memory Terminology</span></span>  

<span data-ttu-id="6657c-104">В этом разделе описаны распространенные термины, используемые при анализе памяти, и применимы различные средства профилирования памяти для разных языков.</span><span class="sxs-lookup"><span data-stu-id="6657c-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="6657c-105">Описанные здесь положения и понятия относятся к [панели память][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="6657c-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="6657c-106">Если вы когда-либо работали с приложением Java, .NET или какой-либо другой профилировщиком памяти, это может быть новым.</span><span class="sxs-lookup"><span data-stu-id="6657c-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="6657c-107">Размеры объектов</span><span class="sxs-lookup"><span data-stu-id="6657c-107">Object sizes</span></span>  

<span data-ttu-id="6657c-108">Рассматривайте память как графы с примитивными типами \ (например, числа и строки \) и Objects \ (ассоциативные массивы \).</span><span class="sxs-lookup"><span data-stu-id="6657c-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="6657c-109">Он может наглядно представлять собой граф с числом взаимосвязанные точек, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="6657c-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Визуальное представление памяти" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="6657c-111">Визуальное представление памяти</span><span class="sxs-lookup"><span data-stu-id="6657c-111">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="6657c-112">Объект может содержать память двумя способами:</span><span class="sxs-lookup"><span data-stu-id="6657c-112">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="6657c-113">Непосредственно объектом.</span><span class="sxs-lookup"><span data-stu-id="6657c-113">Directly by the object.</span></span>  
*   <span data-ttu-id="6657c-114">Неявным образом, сохраняя ссылки на другие объекты и предотвращая автоматическое удаление этих объектов сборщиком мусора (**GC** для коротких \).</span><span class="sxs-lookup"><span data-stu-id="6657c-114">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="6657c-115">При работе с панелью [памяти][DevtoolsMemoryProblemsHeapSnapshots] в DevTools \ (средство для исследования проблем с памятью, обнаруженных в **памяти**\), вы можете просмотреть несколько разных столбцов данных.</span><span class="sxs-lookup"><span data-stu-id="6657c-115">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="6657c-116">Два из них выделены **неполной** и **сохраненной размерностью**, но что они представляют?</span><span class="sxs-lookup"><span data-stu-id="6657c-116">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Неглубокий и сохраненный размер" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="6657c-118">Неглубокий и сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="6657c-118">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="6657c-119">Неглубокий размер</span><span class="sxs-lookup"><span data-stu-id="6657c-119">Shallow size</span></span>  

<span data-ttu-id="6657c-120">Это размер памяти, занимаемой объектом.</span><span class="sxs-lookup"><span data-stu-id="6657c-120">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="6657c-121">Типичные объекты JavaScript зарезервированы для их описания и для хранения непосредственных значений.</span><span class="sxs-lookup"><span data-stu-id="6657c-121">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="6657c-122">Обычно массивы и строки можно использовать для значительного небольшого размера.</span><span class="sxs-lookup"><span data-stu-id="6657c-122">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="6657c-123">Однако строки и внешние массивы часто имеют основное хранилище в памяти обработчика, предоставляя только небольшой объект-оболочку в куче JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6657c-123">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="6657c-124">Память рендеринга — это вся память процесса, на котором выводится проверенная страница: собственная память + JS-память кучи Page + JS для всех выделенных сотрудников, запущенных страницей.</span><span class="sxs-lookup"><span data-stu-id="6657c-124">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="6657c-125">Тем не менее, даже небольшой объект может косвенно хранить большое количество памяти, предотвращая удаление других объектов с помощью автоматического процесса сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="6657c-125">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="6657c-126">Сохраненный размер</span><span class="sxs-lookup"><span data-stu-id="6657c-126">Retained size</span></span>  

<span data-ttu-id="6657c-127">Это размер памяти, которая освобождается после удаления объекта вместе с зависимыми объектами, которые были сделаны недостижимыми из **корней сборщика мусора** \ (корни GC \).</span><span class="sxs-lookup"><span data-stu-id="6657c-127">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="6657c-128">**Корни сборщика мусора** \ (корни GC \) состоят из **дескрипторов** , созданных с помощью локальных и глобальных данных, при создании ссылки из машинного кода на объект JavaScript за пределами V8.</span><span class="sxs-lookup"><span data-stu-id="6657c-128">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="6657c-129">Все подобные дескрипторы могут быть найдены в снимке кучи в разделе **корни GC**  >  , которые**управляют** **GC roots**  >  **глобальными дескрипторами**областей и корней GC.</span><span class="sxs-lookup"><span data-stu-id="6657c-129">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="6657c-130">Описание дескрипторов в этой документации без подробностей о реализации браузера может быть запутанным.</span><span class="sxs-lookup"><span data-stu-id="6657c-130">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="6657c-131">Как корни сборщика мусора, так и дескрипторы — это не то, что вам нужно беспокоиться.</span><span class="sxs-lookup"><span data-stu-id="6657c-131">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="6657c-132">Существует множество внутренних корней GC, большинство из которых не являются интересными для пользователей.</span><span class="sxs-lookup"><span data-stu-id="6657c-132">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="6657c-133">С точки зрения приложений существуют следующие типы корней.</span><span class="sxs-lookup"><span data-stu-id="6657c-133">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="6657c-134">Глобальный объект Window \ (в каждом интернет-кадре).</span><span class="sxs-lookup"><span data-stu-id="6657c-134">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="6657c-135">В снимках кучи есть поле расстояния, представляющее собой число ссылок на свойства в кратчайшем пути хранения из окна.</span><span class="sxs-lookup"><span data-stu-id="6657c-135">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="6657c-136">Дерево документов DOM, состоящее из всех исходных узлов DOM, которые можно получить, обходимым документом.</span><span class="sxs-lookup"><span data-stu-id="6657c-136">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="6657c-137">Не все узлы могут иметь оболочки JS, но если на нем есть обертка, она действует, пока документ активен.</span><span class="sxs-lookup"><span data-stu-id="6657c-137">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="6657c-138">Иногда объекты могут храниться контекстом отладчика на панели **источники** и на **консоли** (например, после вычисления консоли).</span><span class="sxs-lookup"><span data-stu-id="6657c-138">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="6657c-139">Создание моментальных снимков кучи с помощью очищенной **консоли** и без активных точек останова в отладчике на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="6657c-139">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="6657c-140">Очистите панель **консоли** , запустив `clear()` и деактивируйте точки останова на панели « **источники** », прежде чем делать снимок кучи на [панели «память»][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="6657c-140">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="6657c-141">Граф памяти начинается с корневого элемента, который может представлять собой `window` объект браузера или `Global` объект модуля Node.js.</span><span class="sxs-lookup"><span data-stu-id="6657c-141">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="6657c-142">Нельзя управлять тем, как этот корневой объект собирается сборщиком мусора (НОД).</span><span class="sxs-lookup"><span data-stu-id="6657c-142">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Управлять тем, как корневой объект будет собираться сборщиком мусора, невозможно." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="6657c-144">Управлять тем, как корневой объект будет собираться сборщиком мусора, невозможно.</span><span class="sxs-lookup"><span data-stu-id="6657c-144">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="6657c-145">В корне нет доступа к собранию мусора \ (НОД \).</span><span class="sxs-lookup"><span data-stu-id="6657c-145">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="6657c-146">Столбцы " [неглубокий размер](#shallow-size) " и " [сохраненный размер](#retained-size) " представляют данные в байтах.</span><span class="sxs-lookup"><span data-stu-id="6657c-146">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="6657c-147">Дерево сохраненных объектов</span><span class="sxs-lookup"><span data-stu-id="6657c-147">Objects retaining tree</span></span>  

<span data-ttu-id="6657c-148">Куча — это сеть взаимосвязанные объектов.</span><span class="sxs-lookup"><span data-stu-id="6657c-148">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="6657c-149">В математическом мире эта структура называется **графиком** или графиком памяти.</span><span class="sxs-lookup"><span data-stu-id="6657c-149">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="6657c-150">Диаграмма строится на основе **узлов** , которые соединены с помощью **краев**, оба из которых задаются метками.</span><span class="sxs-lookup"><span data-stu-id="6657c-150">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="6657c-151">Для **узлов** \ (или **объектов**\) задана метка с использованием имени функции- **конструктора** , которая использовалась для их построения.</span><span class="sxs-lookup"><span data-stu-id="6657c-151">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="6657c-152">**Края** помечены с использованием имен **свойств**.</span><span class="sxs-lookup"><span data-stu-id="6657c-152">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="6657c-153">Сведения [о том, как записать профиль с помощью профилировщика кучи][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="6657c-153">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="6657c-154">На приведенном ниже рисунке показаны некоторые из глазных элементов, которые можно увидеть в записи снимков кучи на [панели памяти][DevtoolsMemoryProblemsHeapSnapshots] : расстояние от сборщика мусора \ (GC \).</span><span class="sxs-lookup"><span data-stu-id="6657c-154">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="6657c-155">Если почти все объекты одного и того же типа находятся на одном и том же расстоянии, то это может потребоваться для исследования.</span><span class="sxs-lookup"><span data-stu-id="6657c-155">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Расстояние от корня" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="6657c-157">Расстояние от корня</span><span class="sxs-lookup"><span data-stu-id="6657c-157">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="6657c-158">Лидеры</span><span class="sxs-lookup"><span data-stu-id="6657c-158">Dominators</span></span>  

<span data-ttu-id="6657c-159">Лидерские объекты состоят из древовидной структуры, так как у каждого объекта есть только один лидер.</span><span class="sxs-lookup"><span data-stu-id="6657c-159">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="6657c-160">У лидера объекта могут отсутствовать прямые ссылки на объект, который он является лидером; Это значит, что дерево лидера не является деревом графа.</span><span class="sxs-lookup"><span data-stu-id="6657c-160">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="6657c-161">На приведенном ниже рисунке верно следующее утверждение:</span><span class="sxs-lookup"><span data-stu-id="6657c-161">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="6657c-162">Узел 1, являющийся узлом 2</span><span class="sxs-lookup"><span data-stu-id="6657c-162">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="6657c-163">Узел 2 — это узлы 3, 4 и 6</span><span class="sxs-lookup"><span data-stu-id="6657c-163">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="6657c-164">Узел 3 является узлом 5</span><span class="sxs-lookup"><span data-stu-id="6657c-164">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="6657c-165">Узел 5 лидеры в узле 8</span><span class="sxs-lookup"><span data-stu-id="6657c-165">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="6657c-166">Узел 6, являющийся узлом 7</span><span class="sxs-lookup"><span data-stu-id="6657c-166">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Структура дерева (лидера)" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="6657c-168">Структура дерева (лидера)</span><span class="sxs-lookup"><span data-stu-id="6657c-168">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="6657c-169">На приведенном ниже рисунке Node `#3` — это лидер `#10` , но он `#7` также существует в каждом простом пути от сборщика мусора \ (GC \) to `#10` .</span><span class="sxs-lookup"><span data-stu-id="6657c-169">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="6657c-170">Таким образом, объект B является лидером объекта A, если в каждом простом пути от корня к объекту A есть B.</span><span class="sxs-lookup"><span data-stu-id="6657c-170">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Анимированный лидеровый свет" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="6657c-172">Анимированный лидеровый свет</span><span class="sxs-lookup"><span data-stu-id="6657c-172">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="6657c-173">Специальные V8</span><span class="sxs-lookup"><span data-stu-id="6657c-173">V8 specifics</span></span>  

<span data-ttu-id="6657c-174">При профилировании памяти полезно понять, почему снимки кучи выглядят определенным образом.</span><span class="sxs-lookup"><span data-stu-id="6657c-174">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="6657c-175">В этом разделе описаны некоторые связанные с памятью разделы, в частности соответствующие **виртуальной машине V8 JavaScript** \ (V8 VM или VM \).</span><span class="sxs-lookup"><span data-stu-id="6657c-175">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="6657c-176">Представление объекта JavaScript</span><span class="sxs-lookup"><span data-stu-id="6657c-176">JavaScript object representation</span></span>  

<span data-ttu-id="6657c-177">Существуют три простых типа.</span><span class="sxs-lookup"><span data-stu-id="6657c-177">There are three primitive types:</span></span>  

*   <span data-ttu-id="6657c-178">Числа \ (например `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="6657c-178">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="6657c-179">Логические значения \ ( `true` или `false` \)</span><span class="sxs-lookup"><span data-stu-id="6657c-179">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="6657c-180">Строки \ (например `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="6657c-180">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="6657c-181">Примитивы не имеют ссылки на другие значения и всегда Leafs или оконечными узлами.</span><span class="sxs-lookup"><span data-stu-id="6657c-181">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="6657c-182">**Числа** можно хранить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6657c-182">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="6657c-183">немедленные 31-разрядные целые значения, называемые **маленькими целыми числами** (**SMI**s \), или</span><span class="sxs-lookup"><span data-stu-id="6657c-183">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="6657c-184">объекты кучи, которые называются **номерами кучи**.</span><span class="sxs-lookup"><span data-stu-id="6657c-184">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="6657c-185">Номера куч используются для хранения значений, которые не помещаются в форму SMI (например, **Double**), или при необходимости **упаковки**значения, например для установки свойств.</span><span class="sxs-lookup"><span data-stu-id="6657c-185">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="6657c-186">**Строки** можно хранить в одном из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="6657c-186">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="6657c-187">**куча ВМ**или</span><span class="sxs-lookup"><span data-stu-id="6657c-187">the **VM heap**, or</span></span>
*   <span data-ttu-id="6657c-188">внешний в **памяти обработчика**.</span><span class="sxs-lookup"><span data-stu-id="6657c-188">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="6657c-189">**Объект-оболочка** создается и используется для доступа к внешнему хранилищу, в котором, например, сохраняются источники сценариев и другое содержимое, полученное из веб-сайта, а не копируется в кучу ВМ.</span><span class="sxs-lookup"><span data-stu-id="6657c-189">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="6657c-190">Память для новых объектов JavaScript выделяется из выделенной кучи JavaScript \ (или **кучи ВМ**).</span><span class="sxs-lookup"><span data-stu-id="6657c-190">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="6657c-191">Эти объекты управляются сборщиком мусора в V8 и, таким образом, остаются в активном состоянии, так как есть хотя бы одна строгая ссылка на них.</span><span class="sxs-lookup"><span data-stu-id="6657c-191">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="6657c-192">Все, что не входит в кучу JavaScript, называется **неуправляемым объектом**.</span><span class="sxs-lookup"><span data-stu-id="6657c-192">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="6657c-193">Собственные объекты, в отличие от объектов кучи, не управляются сборщиком мусора V8 в течение всего времени существования, и к ним можно получить доступ только из JavaScript с помощью объекта-оболочки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6657c-193">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="6657c-194">**Строка "минус** " — это объект, который содержит пары строк, которые хранятся, а затем объединены и являются результатом сцепления.</span><span class="sxs-lookup"><span data-stu-id="6657c-194">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="6657c-195">Присоединение к **строке** с ненужным содержимым будет выполняться только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6657c-195">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="6657c-196">Примером может быть необходимость создания подстроки присоединенной строки.</span><span class="sxs-lookup"><span data-stu-id="6657c-196">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="6657c-197">Например, если вы выполняете сцепление `a` `b` , вы получаете строку, `(a, b)` представляющую результат сцепления.</span><span class="sxs-lookup"><span data-stu-id="6657c-197">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="6657c-198">Если позднее вы объедините `d` этот результат, вы получите еще одну **строку с недостатком** `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="6657c-198">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="6657c-199">**Массив** — объект с числовыми ключами.</span><span class="sxs-lookup"><span data-stu-id="6657c-199">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="6657c-200">**Массивы** широко используются в виртуальной машине V8 для хранения больших объемов данных.</span><span class="sxs-lookup"><span data-stu-id="6657c-200">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="6657c-201">Наборы пар "ключ-значение", например словарей, заархивированы с помощью **массивов**.</span><span class="sxs-lookup"><span data-stu-id="6657c-201">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="6657c-202">Типичный объект JavaScript хранится только в одном из двух типов **массивов** :</span><span class="sxs-lookup"><span data-stu-id="6657c-202">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="6657c-203">именованные свойства и</span><span class="sxs-lookup"><span data-stu-id="6657c-203">named properties, and</span></span>  
*   <span data-ttu-id="6657c-204">числовые элементы</span><span class="sxs-lookup"><span data-stu-id="6657c-204">numeric elements</span></span>  

<span data-ttu-id="6657c-205">При наличии небольшого количества свойств эти свойства хранятся внутри объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6657c-205">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="6657c-206">**Map** — это объект, который описывает как вид объекта, так и макет.</span><span class="sxs-lookup"><span data-stu-id="6657c-206">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="6657c-207">Например, карты используются для описания неявных иерархий объектов для [быстрого доступа к свойствам][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="6657c-207">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="6657c-208">Группы объектов</span><span class="sxs-lookup"><span data-stu-id="6657c-208">Object groups</span></span>  

<span data-ttu-id="6657c-209">Каждая группа **собственных объектов** состоит из объектов, которые содержат взаимные ссылки друг на друга.</span><span class="sxs-lookup"><span data-stu-id="6657c-209">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="6657c-210">Рассматривайте, например, поддерево DOM, в котором каждый узел имеет ссылку на относительный родительский объект и ссылки на следующий дочерний элемент и следующий одноуровневый элемент, поэтому для них формируется подключенный граф.</span><span class="sxs-lookup"><span data-stu-id="6657c-210">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="6657c-211">Собственные объекты не представлены в куче JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6657c-211">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="6657c-212">Отсутствие представления заключается в том, что у собственных объектов нулевой размер.</span><span class="sxs-lookup"><span data-stu-id="6657c-212">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="6657c-213">Вместо этого создаются объекты-оболочки.</span><span class="sxs-lookup"><span data-stu-id="6657c-213">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="6657c-214">Каждый объект-обертка содержит ссылку на соответствующий собственный объект для перенаправления команд в нее.</span><span class="sxs-lookup"><span data-stu-id="6657c-214">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="6657c-215">В свою очередь, Группа объектов содержит объекты-оболочки.</span><span class="sxs-lookup"><span data-stu-id="6657c-215">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="6657c-216">Однако это не создает несобираемого цикла, так как сборщик мусора (GC \) достаточно интеллектуальный для освобождения групп объектов, оболочки которых больше не упоминаются.</span><span class="sxs-lookup"><span data-stu-id="6657c-216">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="6657c-217">Но при невозможности освобождения одной обертки она содержит всю группу и связанные с ней оболочки.</span><span class="sxs-lookup"><span data-stu-id="6657c-217">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="6657c-218">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6657c-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Запись моментальных снимков кучи | Документы Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Быстрые свойства в V8 | V8"  

> [!NOTE]
> <span data-ttu-id="6657c-221">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6657c-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6657c-222">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) и была написана с помощью [Meggin Kearney][MegginKearney] \ (технический редактор \).</span><span class="sxs-lookup"><span data-stu-id="6657c-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6657c-224">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6657c-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
