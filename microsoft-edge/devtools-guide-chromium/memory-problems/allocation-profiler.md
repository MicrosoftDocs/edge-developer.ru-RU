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

# Как использовать инструментарий выделения на временной шкале  

Используйте **инструментарий выделения на временной** шкале, чтобы найти объекты, которые не собираются должным образом и продолжают хранить память.  

## Как работает инструментарий выделения на временной шкале  

**Инструментарий выделения на** временной шкале **** объединяет подробные моментальные снимки профиля кучи с добавальным обновлением и отслеживанием панели **производительности.**  Аналогичным образом, отслеживание выделения кучи для объектов включает запуск записи, выполнение последовательности действий и остановку записи для анализа.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**Инструментарий выделения** на временной шкале периодически делает моментальные снимки кучи на протяжении записи \(так часто, как каждые 50 мс\) и один окончательный снимок в конце записи.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Инструментарий выделения на временной шкале" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Инструментарий выделения на временной шкале**  
:::image-end:::  

> [!NOTE]
> Число после этого — это ИД объекта, который сохраняется в нескольких снимках, сделанных `@` во время сеанса записи.  Постоянный ИД объекта обеспечивает точное сравнение между состояниями кучи.  Объекты перемещаются во время сборки мусора, поэтому отображать адрес объекта не имеет смысла.  

## Включить инструментарий выделения на временной шкале  

Выполните следующие действия, чтобы начать использовать **инструментарий выделения на временной шкале.**  

1.  [Откройте DevTools.][DevtoolsOpenIndex]  
1.  Откройте панель **"Память"** и выберите **инструментарий выделения на временной шкале.**  
1.  Start recording.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Запись профиля выделения кучи" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Запись профиля выделения кучи  
    :::image-end:::  
    
## Чтение временной шкалы выделения кучи  

Временная шкала выделения кучи показывает, где создаются объекты, и определяет путь сохранения.  На следующем рисунке полосы в верхней части указывают, когда новые объекты находятся в куче.  

Высота каждой панели соответствует размеру недавно выделенных объектов, а цвет полос указывает, находятся ли эти объекты в окончательном снимке кучи.  Синие полосы указывают объекты, которые по-прежнему находятся в конце временной шкалы, серые — объекты, выделенные на временной шкале, но с тех пор собранные мусора.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Инструментарий выделения на моментальный снимок временной шкалы" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Инструментарий выделения на моментальный снимок временной шкалы**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Ползунки на временной шкале выше можно использовать для масштабирования определенного снимка и просмотра объектов, которые были недавно выделены на этом этапе:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Масштабирование моментального снимка" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Масштабирование моментального снимка  
:::image-end:::  

Щелчок определенного объекта в куче показывает дерево сохранения в нижней части снимка кучи.  При проверке пути сохранения к объекту должно быть достаточно сведений, чтобы понять, почему объект не был собран, и необходимо внести необходимые изменения в код, чтобы удалить ненужные ссылки.  

## Просмотр выделения памяти по функции  

Вы можете просматривать выделение памяти с помощью функции JavaScript.  Для получения дополнительных сведений перейдите к [изучить выделение памяти по функции.][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Исследование выделения памяти по функции — устранение проблем с памятью | Документы Майкрософт"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Скачивание канала Microsoft Edge"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) и автором [meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
