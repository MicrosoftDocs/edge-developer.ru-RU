---
description: Определение дорогостоящих функций с помощью панели памяти Microsoft Edge DevTools.
title: Ускорение среды выполнения JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2151777c6a9f94408f48552839531c3534d3de36
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439740"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->

# <a name="speed-up-javascript-runtime"></a>Ускорение среды выполнения JavaScript  

Определение дорогостоящих функций с **помощью средства памяти.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Примеры профилей" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Примеры профилей  
:::image-end:::  

### <a name="summary"></a>Сводка  

*   Записывая точно, какие функции были вызваны и сколько памяти требуется для каждой из них, с помощью выделения выборки в **средстве памяти.**  
*   Визуализация профилей в качестве диаграммы пламени.  
    
## <a name="record-a-sampling-profile"></a>Запись профиля выборки  

Если вы заметили jank в JavaScript, соберите профиль выборки.  В профилях выборки покажите, где время работы тратится на функции на странице.  

1.  Перейдите к **средству памяти** DevTools.  
1.  Выберите радио **кнопку Распределение выборки.**  
1.  Выберите **Начните**.  
1.  В зависимости от того, что вы пытаетесь проанализировать, вы можете обновить страницу, взаимодействовать со страницей или просто запустить страницу.  
1.  Выберите **кнопку Stop** по завершению.  
    
> [!NOTE]
> Можно также использовать [API консоли utilities][DevtoolsConsoleUtilities] для записи профилей командной строки и групп.  

## <a name="view-sampling-profile"></a>Просмотр профиля выборки  

Когда вы закончите запись, DevTools **** автоматически заполняет панель памяти в **профили SAMPLING** с данными из записи.  

Представление по умолчанию **— Heavy \(Bottom Up\)**.  Это представление позволяет просмотреть, какие функции оказали наибольшее влияние на производительность и просмотреть путь запроса для каждой функции.  

### <a name="change-sort-order"></a>Изменение порядка сортировки  

Чтобы изменить порядок сортировки, выберите меню dropdown рядом с выбранной функцией **фокуса** \( функция фокуса \) и выберите один из ![ ](../media/focus-icon.msft.png) следующих вариантов.

**Диаграмма**.  Отображает хронологическую диаграмму записи.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Диаграмма пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Диаграмма пламени  
:::image-end:::  

**Heavy \(Bottom Up\)**.  Списки функций по влиянию на производительность и позволяет изучить пути вызова к функциям.  Это представление по умолчанию.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Тяжелая диаграмма" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Тяжелая диаграмма  
:::image-end:::  

**Tree \(Top Down\)**.  Отображает общую картину структуры вызовов, начиная с верхней части стека вызовов.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Диаграмма дерева" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Диаграмма дерева  
:::image-end:::  

### <a name="exclude-functions"></a>Исключение функций  

Чтобы исключить функцию из профиля выборки, выберите ее, а затем выберите исключенную выбранную функцию **\(** исключить выбранную ![ ](../media/exclude-icon.msft.png) функцию \) кнопку.  Функция запроса \(parent\) исключенной функции \(child\) заряжается выделенной памятью, назначенной исключенной функции \(child\).  

Выберите **кнопку восстановление** всех функций \( восстановление всех функций \) для восстановления всех исключенных функций ![ обратно в ](../media/restore-icon.msft.png) запись.  

## <a name="view-sampling-profile-as-chart"></a>Просмотр профиля выборки в качестве диаграммы  

Представление Диаграммы обеспечивает визуальное представление профиля выборки со временем.  

После [записи профиля выборки](#record-a-sampling-profile)просмотреть запись в качестве диаграммы [пламени,](#change-sort-order) изменив порядок сортировки на **диаграмму**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Представление диаграммы пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Представление диаграммы пламени  
:::image-end:::  

Диаграмма пламени разделена на две части.  

| индекс | Часть | Описание |  
| --- |:--- |:--- |  
| 1 | Обзор | Вид с глаз птиц на всю запись.  Высота баров соответствует глубине стека вызовов.  Чем выше планка, тем глубже стек вызовов.  |  
| 2 | Стеки вызовов | Это углубленное представление функций, которые были вызваны во время записи.  Горизонтальная ось — это время, а вертикальная ось — это стек вызовов.  Стеки организованы сверху вниз.  Таким образом, функция в верхней части называется одна ниже нее, и так далее.  |  

Функции окрашены случайным образом.  Нет корреляции с цветами, используемыми в других панелях.  Однако функции всегда покрашены одинаково между вызовами, чтобы вы могли наблюдать шаблоны в каждом времени работы.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Аннотированная диаграмма пламени" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Аннотированная диаграмма пламени  
:::image-end:::  

Высокий стек вызовов не обязательно является значительным, это просто означает, что было вызвано множество функций.  Но широкая планка означает, что для выполнения функции потребовалось много времени.  Это кандидаты на оптимизацию.  

### <a name="zoom-in-on-specific-parts-of-recording"></a>Увеличение масштабирования определенных частей записи  

Выберите, удерживайте и перетащите мышь влево и вправо по обзору, чтобы увеличить масштаб определенных частей стека вызовов.  После масштабирования стек вызовов автоматически отображает часть выбранной записи.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Масштабирование диаграммы" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Масштабирование диаграммы  
:::image-end:::  

### <a name="view-function-details"></a>Просмотр сведений о функциях  

Выберите функцию для просмотра определения в **средстве Источники.**  

Наведите курсор на функцию, чтобы отобразить данные о времени и имени.  Ниже предоставляются следующие сведения.  

| Подробные | Описание |  
|:--- |:--- |  
| **Name** | Имя функции.  |  
| **Размер self** | Размер текущего призыва функции, включая только утверждения в функции.  |  
| **Общий размер** | Размер текущего призыва этой функции и всех функций, которые она называла.  |  
| **URL-адрес** | Расположение определения функции в виде имени файла, в котором определена функция, и является номером `base.js:261` `base.js` `261` строки определения.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Просмотр сведений о функциях на диаграмме" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Просмотр сведений о функциях на диаграмме  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Справочные | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile — справочные ссылки на API для консоли | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd — справочные | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
