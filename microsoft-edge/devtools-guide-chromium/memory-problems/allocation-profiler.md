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

# <a name="how-to-use-allocation-instrumentation-on-timeline"></a>Использование инструментов распределения в Timeline  

Используйте **приборы Распределения на временной шкале,** чтобы найти объекты, которые не собираются должным образом, и сохраните память.  

## <a name="how-allocation-instrumentation-on-timeline-works"></a>Работа приборов распределения на временной шкале  

**Инструментирование распределения на временной шкале** **** объединяет подробные сведения об снимках профиля кучи с дополнительным обновлением и отслеживанием панели **Performance.**  Точно так же отслеживание выделения кучи для объектов включает запуск записи, выполнение последовательности действий и остановку записи для анализа.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**Инструментирование распределения** на временной шкале периодически делает снимки кучи на протяжении записи \(так часто, как каждые 50 мс\) и один последний снимок в конце записи.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментарий распределения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Инструментарий распределения на временной шкале**  
:::image-end:::  

> [!NOTE]
> Номер после объекта — это объектный ID, который сохраняется на нескольких снимках, сделанных `@` во время сеанса записи.  Стойкий ID объекта позволяет точно сравнивать состояния кучи.  Объекты перемещаются во время сборов мусора, поэтому отображение адреса объекта не имеет смысла.  

## <a name="enable-allocation-instrumentation-on-timeline"></a>Включить инструментарий распределения на временной шкале  

Выполните следующие действия, чтобы приступить к использованию **инструментов распределения на временной шкале.**  

1.  [Откройте DevTools][DevtoolsOpenIndex].  
1.  Откройте панель **памяти,** выберите приборы Распределения на **кнопке радиохронологии.**  
1.  Start recording.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Профайл распределения записи кучи" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Профайл распределения записи кучи  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a>Чтение временной шкалы выделения кучи  

В временной шкале распределения кучи показано, где создаются объекты, и определяет путь сохранения.  На следующем рисунке в верхней части полосы указывают, когда в куче находятся новые объекты.  

Высота каждой панели соответствует размеру недавно выделенных объектов, а цвет баров указывает, живут ли эти объекты в окончательном снимке кучи.  Синие полосы указывают объекты, которые по-прежнему живут в конце временной шкалы, серые — объекты, выделенные во время временной шкалы, но с тех пор собранные.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментирование распределения на моментальный снимок временной шкалы" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Инструментирование распределения на моментальный снимок временной шкалы**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

Вы можете использовать ползунки в временной шкале выше, чтобы увеличить этот снимок и просмотреть объекты, которые были недавно выделены в этот момент:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Масштабирование снимка" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Масштабирование снимка  
:::image-end:::  

Выбор на определенном объекте в куче показывает дерево сохранения в нижней части снимка кучи.  Изучение пути сохранения объекта должно дать вам достаточно информации, чтобы понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужные ссылки.  

## <a name="view-memory-allocation-by-function"></a>Просмотр распределения памяти по функции  

Вы можете просматривать распределение памяти с помощью функции JavaScript.  Дополнительные сведения перейдите к расследованию [распределения памяти по функции][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование распределения памяти по функции — исправление проблем с памятью | Документы Майкрософт"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачайте канал Microsoft Edge"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и является автором [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
