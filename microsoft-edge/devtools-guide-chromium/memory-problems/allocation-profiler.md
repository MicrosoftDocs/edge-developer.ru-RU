---
description: Используйте инструментарий выделения на временной шкале, чтобы найти объекты, которые не собираются должным образом и продолжают хранить память.
title: Как использовать инструментарий выделения на временной шкале
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 946c2d8b45f316b491a604c16c37bb2467983222
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230917"
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

# <span data-ttu-id="1ae2b-104">Как использовать инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="1ae2b-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="1ae2b-105">Используйте **инструментарий выделения на временной** шкале, чтобы найти объекты, которые не собираются должным образом и продолжают хранить память.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="1ae2b-106">Как работает инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="1ae2b-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="1ae2b-107">**Инструментарий выделения на** временной шкале \*\*\*\* объединяет подробные моментальные снимки профиля кучи с добавальным обновлением и отслеживанием панели **производительности.**</span><span class="sxs-lookup"><span data-stu-id="1ae2b-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="1ae2b-108">Аналогичным образом, отслеживание выделения кучи для объектов включает запуск записи, выполнение последовательности действий и остановку записи для анализа.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="1ae2b-109">**Инструментарий выделения** на временной шкале периодически делает моментальные снимки кучи на протяжении записи \(так часто, как каждые 50 мс\) и один окончательный снимок в конце записи.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментарий выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="1ae2b-111">Инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="1ae2b-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1ae2b-112">Число после этого — это ИД объекта, который сохраняется в нескольких снимках, сделанных `@` во время сеанса записи.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="1ae2b-113">Постоянный ИД объекта обеспечивает точное сравнение между состояниями кучи.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="1ae2b-114">Объекты перемещаются во время сборки мусора, поэтому отображать адрес объекта не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="1ae2b-115">Включить инструментарий выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="1ae2b-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="1ae2b-116">Выполните следующие действия, чтобы начать использовать **инструментарий выделения на временной шкале.**</span><span class="sxs-lookup"><span data-stu-id="1ae2b-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="1ae2b-117">[Откройте DevTools.][DevtoolsOpenIndex]</span><span class="sxs-lookup"><span data-stu-id="1ae2b-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="1ae2b-118">Откройте панель **"Память"** и выберите **инструментарий выделения на временной шкале.**</span><span class="sxs-lookup"><span data-stu-id="1ae2b-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="1ae2b-119">Start recording.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Запись профиля выделения кучи" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="1ae2b-121">Запись профиля выделения кучи</span><span class="sxs-lookup"><span data-stu-id="1ae2b-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1ae2b-122">Чтение временной шкалы выделения кучи</span><span class="sxs-lookup"><span data-stu-id="1ae2b-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="1ae2b-123">Временная шкала выделения кучи показывает, где создаются объекты, и определяет путь сохранения.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="1ae2b-124">На следующем рисунке полосы в верхней части указывают, когда новые объекты находятся в куче.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="1ae2b-125">Высота каждой панели соответствует размеру недавно выделенных объектов, а цвет полос указывает, находятся ли эти объекты в окончательном снимке кучи.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="1ae2b-126">Синие полосы указывают объекты, которые по-прежнему находятся в конце временной шкалы, серые — объекты, выделенные на временной шкале, но с тех пор собранные мусора.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментарий выделения на моментальный снимок временной шкалы" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="1ae2b-128">**Инструментарий выделения на моментальный снимок временной шкалы**</span><span class="sxs-lookup"><span data-stu-id="1ae2b-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="1ae2b-129">Ползунки на временной шкале выше можно использовать для масштабирования определенного снимка и просмотра объектов, которые были недавно выделены на этом этапе:</span><span class="sxs-lookup"><span data-stu-id="1ae2b-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Масштабирование моментального снимка" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="1ae2b-131">Масштабирование моментального снимка</span><span class="sxs-lookup"><span data-stu-id="1ae2b-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="1ae2b-132">Щелчок определенного объекта в куче показывает дерево сохранения в нижней части снимка кучи.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-132">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="1ae2b-133">При проверке пути сохранения к объекту должно быть достаточно сведений, чтобы понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужные ссылки.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="1ae2b-134">Просмотр выделения памяти по функции</span><span class="sxs-lookup"><span data-stu-id="1ae2b-134">View memory allocation by function</span></span>  

<span data-ttu-id="1ae2b-135">Вы можете просматривать выделение памяти с помощью функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1ae2b-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="1ae2b-136">Для получения дополнительных сведений перейдите к [изучить выделение памяти по функции.][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]</span><span class="sxs-lookup"><span data-stu-id="1ae2b-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <span data-ttu-id="1ae2b-137">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1ae2b-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование выделения памяти по функции — устранение проблем с памятью | Документы Майкрософт"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачивание канала Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="1ae2b-141">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ae2b-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1ae2b-142">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и автором [meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="1ae2b-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1ae2b-144">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ae2b-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
