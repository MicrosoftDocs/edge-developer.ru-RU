---
description: Используйте приборы Распределения на временной шкале, чтобы найти объекты, которые не собираются должным образом, и сохраните память.
title: Использование инструментов распределения в Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 374b7f0ad80b8975319b2b0ec5cecf42ce4bde82
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397820"
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

# <a name="how-to-use-allocation-instrumentation-on-timeline"></a><span data-ttu-id="62fa9-104">Использование инструментов распределения в Timeline</span><span class="sxs-lookup"><span data-stu-id="62fa9-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="62fa9-105">Используйте **приборы Распределения на временной шкале,** чтобы найти объекты, которые не собираются должным образом, и сохраните память.</span><span class="sxs-lookup"><span data-stu-id="62fa9-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <a name="how-allocation-instrumentation-on-timeline-works"></a><span data-ttu-id="62fa9-106">Работа приборов распределения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="62fa9-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="62fa9-107">**Инструментирование распределения на временной шкале** \*\*\*\* объединяет подробные сведения об снимках профиля кучи с дополнительным обновлением и отслеживанием панели **Performance.**</span><span class="sxs-lookup"><span data-stu-id="62fa9-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="62fa9-108">Точно так же отслеживание выделения кучи для объектов включает запуск записи, выполнение последовательности действий и остановку записи для анализа.</span><span class="sxs-lookup"><span data-stu-id="62fa9-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="62fa9-109">**Инструментирование распределения** на временной шкале периодически делает снимки кучи на протяжении записи \(так часто, как каждые 50 мс\) и один последний снимок в конце записи.</span><span class="sxs-lookup"><span data-stu-id="62fa9-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментарий распределения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="62fa9-111">Инструментарий распределения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="62fa9-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="62fa9-112">Номер после объекта — это объектный ID, который сохраняется на нескольких снимках, сделанных `@` во время сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="62fa9-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="62fa9-113">Стойкий ID объекта позволяет точно сравнивать состояния кучи.</span><span class="sxs-lookup"><span data-stu-id="62fa9-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="62fa9-114">Объекты перемещаются во время сборов мусора, поэтому отображение адреса объекта не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="62fa9-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <a name="enable-allocation-instrumentation-on-timeline"></a><span data-ttu-id="62fa9-115">Включить инструментарий распределения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="62fa9-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="62fa9-116">Выполните следующие действия, чтобы приступить к использованию **инструментов распределения на временной шкале.**</span><span class="sxs-lookup"><span data-stu-id="62fa9-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="62fa9-117">[Откройте DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="62fa9-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="62fa9-118">Откройте панель **памяти,** выберите приборы Распределения на **кнопке радиохронологии.**</span><span class="sxs-lookup"><span data-stu-id="62fa9-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="62fa9-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="62fa9-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Профайл распределения записи кучи" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="62fa9-121">Профайл распределения записи кучи</span><span class="sxs-lookup"><span data-stu-id="62fa9-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a><span data-ttu-id="62fa9-122">Чтение временной шкалы выделения кучи</span><span class="sxs-lookup"><span data-stu-id="62fa9-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="62fa9-123">В временной шкале распределения кучи показано, где создаются объекты, и определяет путь сохранения.</span><span class="sxs-lookup"><span data-stu-id="62fa9-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="62fa9-124">На следующем рисунке в верхней части полосы указывают, когда в куче находятся новые объекты.</span><span class="sxs-lookup"><span data-stu-id="62fa9-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="62fa9-125">Высота каждой панели соответствует размеру недавно выделенных объектов, а цвет баров указывает, живут ли эти объекты в окончательном снимке кучи.</span><span class="sxs-lookup"><span data-stu-id="62fa9-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="62fa9-126">Синие полосы указывают объекты, которые по-прежнему живут в конце временной шкалы, серые — объекты, выделенные во время временной шкалы, но с тех пор собранные.</span><span class="sxs-lookup"><span data-stu-id="62fa9-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментирование распределения на моментальный снимок временной шкалы" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="62fa9-128">**Инструментирование распределения на моментальный снимок временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="62fa9-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

<span data-ttu-id="62fa9-129">Вы можете использовать ползунки в временной шкале выше, чтобы увеличить этот снимок и просмотреть объекты, которые были недавно выделены в этот момент:</span><span class="sxs-lookup"><span data-stu-id="62fa9-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Масштабирование снимка" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="62fa9-131">Масштабирование снимка</span><span class="sxs-lookup"><span data-stu-id="62fa9-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="62fa9-132">Выбор на определенном объекте в куче показывает дерево сохранения в нижней части снимка кучи.</span><span class="sxs-lookup"><span data-stu-id="62fa9-132">Choosing on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="62fa9-133">Изучение пути сохранения объекта должно дать вам достаточно информации, чтобы понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужные ссылки.</span><span class="sxs-lookup"><span data-stu-id="62fa9-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <a name="view-memory-allocation-by-function"></a><span data-ttu-id="62fa9-134">Просмотр распределения памяти по функции</span><span class="sxs-lookup"><span data-stu-id="62fa9-134">View memory allocation by function</span></span>  

<span data-ttu-id="62fa9-135">Вы можете просматривать распределение памяти с помощью функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="62fa9-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="62fa9-136">Дополнительные сведения перейдите к расследованию [распределения памяти по функции][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="62fa9-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="62fa9-137">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="62fa9-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование распределения памяти по функции — исправление проблем с памятью | Документы Майкрософт"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачайте канал Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="62fa9-141">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="62fa9-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="62fa9-142">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и является автором [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="62fa9-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="62fa9-144">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="62fa9-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
