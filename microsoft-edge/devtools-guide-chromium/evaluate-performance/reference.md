---
description: Ссылка на все способы записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439691"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="performance-analysis-reference"></a>Справочные материалы по анализу производительности  

Эта страница — это всестороннюю ссылку на функции Microsoft Edge DevTools, связанные с анализом производительности.  

Перейдите [к началу][DevtoolsEvaluatePerformanceGettingStarted] работы с анализом производительности выполнения для руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

## <a name="record-performance"></a>Запись производительности  

### <a name="record-runtime-performance"></a>Запись выполнения  

Запись производительности выполнения при анализе производительности страницы во время ее выполнения, а не загрузки.  

1.  Перейдите на страницу, которую необходимо проанализировать.  
1.  Откройте средство **Performance** в DevTools.  
1.  Выберите **запись** \. ![ Значок запись ](../media/record-icon.msft.png) \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Взаимодействие со страницей.  DevTools записываю все действия страниц, которые происходят в результате взаимодействия.  
1.  Выберите **запись** еще раз или **выберите Остановку,** чтобы остановить запись.  
    
### <a name="record-load-performance"></a>Запись производительности нагрузки  

Запись производительности нагрузки при анализе производительности страницы при ее загрузке, а не запуске.  

1.  Перейдите на страницу, которую необходимо проанализировать.  
1.  Откройте панель **Performance** devTools.  
1.  Выберите **страницу Обновления** \. ![ Страница обновления ](../media/refresh-page-icon.msft.png) \).  DevTools записывает показатели производительности при обновлении страницы, а затем автоматически останавливает запись через пару секунд после завершения нагрузки.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Страница обновления" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Страница обновления**  
    :::image-end:::  
    
DevTools автоматически увеличивает масштаб на части записи, где происходило большинство действий.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Запись загрузки страниц" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Запись загрузки страниц  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a>Захват скриншотов во время записи  

Включив **контрольный ящик Screenshots,** чтобы запечатлеть снимок экрана каждого кадра во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Контрольный ящик Screenshots" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   Контрольный **ящик Screenshots**  
:::image-end:::  

Перейдите [к просмотру экрана,](#view-a-screenshot) чтобы узнать, как взаимодействовать со снимками экрана.  

### <a name="force-garbage-collection-while-recording"></a>Принудительное сбор мусора во время записи  

Во время записи страницы выберите **Сбор** мусора \( Сбор значка мусора \) для ![ ](../media/collect-garbage-icon.msft.png) принудительного сбора мусора.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Сбор мусора" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Сбор мусора  
:::image-end:::  

### <a name="show-recording-settings"></a>Показать параметры записи  

Выберите **параметры** Capture \. Параметры захвата \) для выбора дополнительных параметров, связанных с тем, как ![ ](../media/capture-settings-icon.msft.png) DevTools фиксирует записи производительности.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Раздел Параметры захвата" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Раздел **Параметры захвата**  
:::image-end:::  

### <a name="disable-javascript-samples"></a>Отключение образцов JavaScript  

По умолчанию в **основном разделе** записи отображаются подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.  Чтобы отключить эти стеки вызовов:  

1.  Откройте меню **Параметры захвата.**  Перейдите [к показу параметров записи.](#show-recording-settings)  
1.  Включим почтовый ящик **Disable JavaScript Samples.**  
1.  Запись страницы.  
    
На следующих 2 рисунках отображается разница между отключением и включением образцов JavaScript.  Основной **раздел** записи намного короче при отключении выборки, так как он ограничит все стеки вызовов JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Пример записи при отключении образцов JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Пример записи при отключении образцов JS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Пример записи при включении образцов JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Пример записи при включении образцов JS  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a>Throttle сеть во время записи  

Чтобы затормазать сеть во время записи:  

1.  Откройте меню **Параметры захвата.**  Перейдите [к показу параметров записи.](#show-recording-settings)  
1.  Установите **Сеть** на нужный уровень регулирования.  
    
### <a name="throttle-the-cpu-while-recording"></a>Throttle CPU во время записи  

Чтобы затормазать ЦП во время записи:  

1.  Откройте меню **Параметры захвата.**  Перейдите [к показу параметров записи.](#show-recording-settings)  
1.  Установите **ЦП** на нужный уровень регулирования.  
    
Регулирование относительно возможностей компьютера.  Например, параметр **замедления 2x** делает работу ЦП в 2 раза медленнее обычной.  DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств сильно отличается от архитектуры настольных компьютеров и ноутбуков.  

### <a name="turn-on-advanced-paint-instrumentation"></a>Включим расширенный инструментарий краски  

Чтобы просмотреть подробное инструментирование краски:  

1.  Откройте меню **Параметры захвата.**  Перейдите [к показу параметров записи.](#show-recording-settings)  
1.  Проверьте **контрольный ящик Enable advanced paint instrumentation (slow).**  

Чтобы узнать, как взаимодействовать с информацией о краске, перейдите к [слоям Просмотра](#view-layers-information) и [просмотру профилера краски](#view-paint-profiler).  

## <a name="save-a-recording"></a>Сохранение записи  

Чтобы сохранить запись, откройте контекстное меню \(правой кнопкой мыши\) и выберите **сохранить профиль**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Сохранение профиля" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Сохранение профиля**  
:::image-end:::  

## <a name="load-a-recording"></a>Загрузка записи  

Чтобы загрузить запись, откройте контекстное меню \(правой кнопкой мыши\) и выберите **профиль нагрузки**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Профиль нагрузки" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Профиль нагрузки**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a>Очистка предыдущей записи  

После записи выберите **clear recording** \( Clear recording icon \) для очистки этой записи с панели ![ ](../media/clear-recording-icon.msft.png) **Performance.**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Четкая запись" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Четкая запись**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a>Анализ записи производительности  

После [записи производительности выполнения](#record-runtime-performance) или записи производительности нагрузки панель **Performance** предоставляет много данных для анализа производительности того, что только что произошло. [](#record-load-performance)  

### <a name="select-a-portion-of-a-recording"></a>Выберите часть записи  

Перетащите мышь влево или вправо по **обзору,** чтобы выбрать часть записи.  Обзор **—** это раздел, содержащий **диаграммы FPS,** **CPU**и **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Перетаскивать мышь через обзор для масштабирования" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Перетаскивать мышь через **обзор для** масштабирования  
:::image-end:::  

Чтобы выбрать часть с помощью клавиатуры:  

1.  Выберите фон основного **раздела** или любой из следующих разделов, например **Interactions,** **Network**или **GPU.**  Этот рабочий процесс клавиатуры работает только в том случае, если один из этих разделов находится в фокусе.  
1.  Используйте `W` `A` клавиши , , чтобы увеличить, переместить `S` `D` влево, увеличить и переместить вправо, соответственно.  

Чтобы выбрать часть с помощью трекпада, выполните следующие действия.  

1.  Наведите курсор мыши на раздел **Обзор** или раздел **Сведения.**  Раздел **Обзор** — это область, содержащая **диаграммы FPS,** **CPU**и **NET.**  Раздел **Details** — это область, **содержащая основной** раздел, раздел **Взаимодействия** и так далее.  
1.  С помощью двух пальцев проведите пальцем вверх, чтобы увеличить масштаб, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить, и проведите пальцем вправо, чтобы переместить вправо.  

Чтобы прокрутить длинную диаграмму пламени в **разделе Main** или любом из соседей, выберите и удерживайте во время перетаскивание вверх и вниз.  Перетащите влево и вправо, чтобы переместить выбранную часть записи.  

### <a name="search-activities"></a>Действия поиска  

Выберите `Control` + `F` \(Windows, Linux\) `Command` + `F` или \(macOS\) **** для открытия окна поиска в нижней части панели Performance.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Поле поиска" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Поле поиска  
:::image-end:::  

Чтобы ориентироваться в действиях, которые соответствуют запросу:  

*   Используйте **кнопки Previous** \( ![ Previous ](../media/previous-icon.msft.png) \) и **Next** ![ ](../media/next-icon.msft.png) \( Далее \).  
*   Выберите `Shift` + `Enter` для выбора предыдущего или `Enter` для выбора следующего.  

Изменение параметров запроса:  

*   Выберите **деликатный** \. ![ Деловая ](../media/search-case-icon.msft.png) чувствительная \) для того, чтобы сделать запрос чувствительным.  
*   Выберите **Regex** \( Regex \) для использования ![ ](../media/search-regex-icon.msft.png) регулярного выражения в запросе.  

Чтобы скрыть поле поиска, выберите **Отмена**.  

### <a name="view-main-thread-activity"></a>Просмотр основных действий потоков  

Используйте раздел **Main** для просмотра действий, которые произошли в основном потоке страницы.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Основной **** раздел  
:::image-end:::  

Выберите событие, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**  DevTools описывает выбранное событие.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Дополнительные сведения об анонимной функции в панели Сводка" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Дополнительные сведения о `anonymous` функции в панели **Сводка**  
:::image-end:::  

DevTools представляет собой основные потоковые действия с помощью схемы пламени.  X-axis представляет запись с течением времени.  Y-axis представляет собой стек вызовов.  События сверху вызывают события под ней.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Диаграмма пламени" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Диаграмма пламени  
:::image-end:::  

В предыдущем рисунке `click` событие вызвало в `Function Call` `activitytabs.js` строке 53.  Ниже `Function Call` см. отзыв о том, что была запустится анонимная функция.  Запрашиваемая анонимная функция `a` , которая запрашивала `wait` , которая запрашивала `Minor GC` .  

DevTools назначает скрипты случайных цветов.  На предыдущем рисунке запросы функций из одного сценария имеют светло-зеленый цвет.  Запросы из другого скрипта являются цветными бежевыми.  Более темный желтый цвет представляет действие скриптов, а фиолетовое событие — отрисовку.  Эти более темные желтые и фиолетовые события согласуются во всех записях.  

Перейдите [к отключению образцов JavaScript,](#disable-javascript-samples) если вы хотите скрыть подробную схему пламени запросов JavaScript.  Если образцы JS отключены, отображаются только события высокого уровня, такие как и из `Event: choose` `Function Call` `str` предыдущего рисунка.  

### <a name="view-activities-in-a-table"></a>Просмотр действий в таблице  

После записи страницы не нужно полагаться только на основной **раздел** для анализа действий.  DevTools также предоставляет три табулярных представления для анализа действий.  Каждое представление дает различные точки зрения на действия:  

*   Если необходимо просмотреть корневые действия, которые вызывают большую часть работы, используйте панель [Дерева вызовов.](#the-call-tree-panel)  
*   Если необходимо просмотреть действия, на которые было потрачено больше всего времени, используйте [панель Bottom-Up.](#the-bottom-up-panel)  
*   Если необходимо просмотреть действия в порядке, в котором они произошли во время записи, используйте панель [журнала событий.](#the-event-log-panel)  
    
> [!NOTE]
> В следующих трех разделах все ссылаются на одно и то же демо.  Запустите демонстрацию самостоятельно [в демо-версии вкладок Activity.][ActivityTabsDemo]  

#### <a name="root-activities"></a>Корневые действия  

Вот объяснение концепции **** корневых действий, которая упоминается в панели **Дерево** вызовов, панели **Нижней** части и **панели журнала** событий.  

Корневые действия — это те действия, которые вызывают работу браузера.  Например, при выборе веб-страницы браузер выполняет действие в `Event` качестве корневого действия.  Это `Event` может привести к запуску обработера и так далее.  

В диаграмме пламени раздела **Main** корневые действия находятся в верхней части диаграммы.  В **панелях Дерево вызовов** и **журнал событий** корневые действия являются элементами верхнего уровня.  

Перейдите к [панели Дерева вызовов](#the-call-tree-panel) для примера корневых действий.  

#### <a name="the-call-tree-panel"></a>Панель дерева вызовов  

Используйте панель **Дерево вызовов,** чтобы просмотреть, [какие корневые действия](#root-activities) вызывают большую часть работы.  

Панель **Дерева вызовов** отображает действия только во время выбранной части записи.  Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Панель дерева вызовов" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Панель **дерева вызовов**  
:::image-end:::  

На предыдущем рисунке верхний уровень элементов в столбце **Activity,** например корневых действий и `Evaluate Script` `Parse HTML` корневых.  Вложение представляет собой стек вызовов.  Например, на предыдущем рисунке, который `Parse HTML` вызвал `Evaluate Script` и `Compile Script` `(anonymous)` .  

**Self Time** представляет время, непосредственно затраченное в этом действии.  **Общее время** представляет время, затраченное в этом действии или на любое из детей.  

Для **сортировки**таблицы **** в этом столбце выберите "Время самостоятельно", ****"Общее время" или "Действие".  

Используйте **текстовое** поле Filter для фильтрации событий по имени действия.  

По умолчанию **меню группировки** настроено на **No Grouping**.  Используйте меню **группировки** для сортировки таблицы действий на основе различных критериев.  

Выберите **Показать самый тяжелый** стек \. Показать самый тяжелый стек \) чтобы показать другую таблицу ![ ](../media/show-heaviest-stack-icon.msft.png) справа от **таблицы Activity.**  Выберите действие для заполнения самой **тяжелой таблицы стеков.**  Самая **тяжелая таблица стеков** отображает, на которое дети выбранного действия убирали больше всего времени.  

#### <a name="the-bottom-up-panel"></a>Панель Bottom-Up  

Используйте панель **снизу вверх,** чтобы просмотреть, какие действия непосредственно заняли больше всего времени в совокупности.  

Панель **Bottom-Up** отображает действия только во время выбранной части записи.  Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Панель Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Панель **снизу вверх**  
:::image-end:::  

В **диаграмме пламени** основного раздела предыдущего рисунка перейдите к этому практически все время, затраченное на `Parse HTML` запуск.  Верхнее действие в **панели Bottom-Up** предыдущего рисунка `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Перейдите к **панели Bottom-Up,** следующая самая дорогая активность `Layout` .  

Столбец **Self Time** представляет совокупное время, затраченное непосредственно в этом действии, во всех случаях.  

Столбец **Общее** время представляет агрегированное время, затраченное в этом действии или любом из детей.  

#### <a name="the-event-log-panel"></a>Панель журнала событий  

Панель **журнала событий** используется для просмотра действий в порядке, в котором они произошли во время записи.  

Панель **журнала событий** отображает действия только во время выбранной части записи.  Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Панель журнала событий" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Панель **журнала событий**  
:::image-end:::  

Столбец **Время** начала представляет точку, с которой началось это действие, относительно начала записи.  Например, время начала работы выбранного элемента на предыдущем рисунке означает, что действие началось `175.7 ms` с 175,7 мс после начала записи.  

Столбец **Self Time** представляет время, затраченное непосредственно в этом действии.  

Столбцы **Total Time** представляют время, затраченное непосредственно в этом действии или в любом из детей.  

Выберите **время начала,** **время**самостоятельно или **общее** время сортировки таблицы в этом столбце.

Используйте **текстовое поле Filter** для фильтрации действий по имени.  

Используйте меню **Duration,** чтобы отфильтровать все действия, которые заняли менее 1 мс или 15 мс.  По умолчанию **меню "Продолжительность"** заказано **всем,** то есть все действия показаны.  

Отключить **контрольные ящики Loading,** **Scripting,** **Rendering**или **Painting,** чтобы отфильтровать все действия из этих категорий.  

### <a name="view-gpu-activity"></a>Просмотр действий GPU  

Просмотр действий GPU в разделе **GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Раздел GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Раздел **GPU**  
:::image-end:::  

### <a name="view-raster-activity"></a>Просмотр действия raster  

Просмотр действий raster в разделе **Raster.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Раздел Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Раздел **Raster**  
:::image-end:::  

### <a name="view-interactions"></a>Просмотр взаимодействий  

Раздел **Взаимодействия используется** для поиска и анализа взаимодействий пользователей, которые произошли во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Раздел Взаимодействия" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Раздел **Взаимодействия**  
:::image-end:::  

Красная строка в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.  

Выберите взаимодействие, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**  

### <a name="analyze-frames-per-second-fps"></a>Анализ кадров в секунду (FPS)  

DevTools предоставляет множество способов анализа кадров в секунду:  

*   Используйте [диаграмму FPS,](#the-fps-chart) чтобы получить обзор FPS за время записи.  
*   Используйте [раздел Frames,](#the-frames-section) чтобы просмотреть, сколько времени занимает определенный кадр.  
*   Используйте **счетчик FPS для** оценки FPS в режиме реального времени при запуске страницы.  Перейдите [к просмотру кадров в секунду в режиме реального времени с помощью счетчика FPS.](#view-frames-per-second-in-realtime-with-the-fps-meter)  
    
#### <a name="the-fps-chart"></a>Диаграмма FPS  

На **диаграмме FPS** представлен обзор частоты кадров в течение записи.  Как правило, чем выше зеленая планка, тем выше частота кадров.  

Красная планка над **диаграммой FPS** — это предупреждение о том, что частота кадров снизилась настолько низко, что, вероятно, навредила опыту пользователя.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Диаграмма **FPS**  
:::image-end:::  

#### <a name="the-frames-section"></a>Раздел Кадры  

В **разделе Frames** указывается, сколько времени занимает определенный кадр.  

Наведите курсор на кадр, чтобы просмотреть набор инструментов с дополнительными сведениями о нем.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Наведите курсор на кадр" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Наведите курсор на кадр  
:::image-end:::  

Выберите кадр, чтобы просмотреть дополнительные сведения о кадре в панели **Сводка.**  DevTools описывает выбранный кадр синим цветом.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Просмотр кадра в панели Сводка" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Просмотр кадра в панели **Сводка**  
:::image-end:::  

### <a name="view-network-requests"></a>Просмотр сетевых запросов  

**Расширь раздел Network,** чтобы просмотреть водопад сетевых запросов, которые произошли во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Раздел Network" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Раздел **Network**  
:::image-end:::  

Запросы закодироваться следующим образом:  

*   HTML: Синий  
*   CSS: Purple  
*   JS: Желтый  
*   Изображения: Зеленый  
    
Выберите запрос, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**  Например, на предыдущем рисунке панель **Сводка** отображает дополнительные сведения о синем запросе, выбранном в разделе **Сеть.**  

Темно-синий квадрат в верхнем левом конце запроса означает, что это запрос с более высоким приоритетом.  Квадрат светло-синего цвета означает более низкий приоритет.  Например, на предыдущем рисунке синий выбранный запрос имеет более высокий приоритет, а зеленый — более низкий.  

В 1-м из следующих рисунков запрос представлен строкой слева, баром в центре с темной частью и светлой частью, а также строкой `www.bing.com` справа.  Во 2-м из следующих рисунков показано соответствующее представление того же запроса в панели **синхронизации** средства **Network.**  Ниже представлена карта этих двух представлений друг с другом:

*   Левая строка — это все в соответствии с `Connection Start` группой событий, включительно.  Другими словами, это все, прежде чем `Request Sent` , эксклюзивный.  
*   Светлая часть панели и `Request Sent` `Waiting (TTFB)` .  
*   Темная часть панели `Content Download` .  
*   Правая линия — это, по сути, время, затраченное на ожидание основного потока.  Это не представлено в панели **Timing.**  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Представление строки-панели www.bing.com запроса" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Представление строки-панели `www.bing.com` запроса  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Средство Network" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Средство **Network**  
:::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a>Просмотр метрик памяти  

Включив контрольный ящик **Памяти,** чтобы просмотреть показатели памяти из последней записи.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Контрольный ящик памяти" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   Контрольный ящик **памяти**  
:::image-end:::  

В DevTools отображается новая диаграмма **памяти** над **панелью Сводка.**  Существует также новая диаграмма ниже **диаграммы NET,** называемой **HEAP**.  Диаграмма **HEAP** содержит те же сведения, что и строка **JS Heap** в **диаграмме Памяти.**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Метрик памяти" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Метрик памяти  
:::image-end:::  

Цветные строки на карте диаграммы к цветным почтовым ящикам над диаграммой.  
Отключить контрольный ящик, чтобы скрыть эту категорию из диаграммы.  

На диаграмме отображается только область выбранной записи.  Например, на предыдущем рисунке на диаграмме **Памяти** отображается только использование памяти от отметки 400 мс до отметки 1750 мс.  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a>Просмотр продолжительности части записи  

При анализе таких разделов, как **Network** или **Main,** иногда требуется более точная оценка того, сколько времени заняли определенные события.  `Shift`Удерживайте, выберите и удерживайте и перетащите влево или вправо, чтобы выбрать часть записи.  В нижней части выбора DevTools показывает, сколько времени занимает эта часть.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Просмотр продолжительности части записи" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Просмотр продолжительности части записи  
:::image-end:::  

### <a name="view-a-screenshot"></a>Просмотр экрана  

Перейдите [к захвату скриншотов во время записи,](#capture-screenshots-while-recording) чтобы узнать, как включить скриншоты.  

Наведите курсор на **обзор,** чтобы просмотреть снимок экрана, как выглядела страница в этот момент записи.  Обзор **—** это раздел, содержащий **диаграммы CPU,** **FPS**и **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Просмотр экрана" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Просмотр экрана  
:::image-end:::  

Вы также можете просмотреть скриншоты, выбрав кадр в разделе **Frames.**  DevTools отображает небольшую версию экрана в панели **Сводка.**  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Просмотр экрана в панели Сводка" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Просмотр экрана в панели **Сводка**  
:::image-end:::  

Выберите эскиз на панели **Сводка,** чтобы увеличить масштаб экрана.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Масштабирование экрана с панели Сводка" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Масштабирование экрана с панели **Сводка**  
:::image-end:::  

### <a name="view-layers-information"></a>Просмотр сведений о слоях  

Чтобы просмотреть расширенные слои, сведения о кадре:  

1.  [Включи расширенный инструментарий краски.](#turn-on-advanced-paint-instrumentation)  
1.  Выберите кадр в разделе **Frames.**  DevTools отображает сведения о слоях в новой панели **Layers** рядом с панелью **Журнала событий.**  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Области Слоев" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Области **Слоев**  
    :::image-end:::  
    
Наведите курсор на слой, чтобы выделить его на схеме.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Выделение слоя" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Выделение слоя  
:::image-end:::  

Чтобы переместить схему:  

*   Выберите **режим** Pan \( Pan Mode \) для ![ перемещения по осям X и ](../media/pan-mode-icon.msft.png) Y.  
*   Выберите **режим вращать** \( ![ Вращать режим \) для ](../media/rotate-mode-icon.msft.png) поворота вдоль оси Z.  
*   Выберите **сброс преобразования** \. Сброс преобразования \) для ![ ](../media/reset-transform-icon.msft.png) сброса схемы в исходное положение.  
    
### <a name="view-paint-profiler"></a>Просмотр профиля краски  

Чтобы просмотреть расширенные сведения о событии краски:  

1.  [Включаем](#turn-on-advanced-paint-instrumentation).  
1.  Выберите событие **Paint** в **разделе Main.**  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Панель профилера Paint" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Панель **профилера Paint**  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a>Анализ производительности отрисовки с помощью средства визуализации  

Используйте функции панели **rendering** для визуализации производительности визуализации страницы.  

Чтобы открыть **средство отрисовки:**  

1.  [Откройте командное меню.][DevToolsCommandMenu]  
1.  Начните `Rendering` вводить и выберите `Show Rendering` .  DevTools отображает средство **визуализации** в нижней части окна DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Средство отрисовки" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Средство **отрисовки**  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a>Просмотр кадров в секунду в режиме реального времени с помощью счетчика FPS  

Счетчик **FPS —** это наложение, которое отображается в правом верхнем углу представления.  Он предоставляет оценку FPS в режиме реального времени по мере работы страницы.  Чтобы открыть **счетчик FPS:**  

1.  Откройте средство **отрисовки.**  [Анализ производительности визуализации с помощью средства визуализации.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Включи **флажки счетчика FPS.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       Счетчик **FPS**  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a>Просмотр событий рисования в режиме реального времени с помощью мигания краски  

Чтобы получить представление всех событий краски на странице в режиме реального времени, используйте paint Flashing.  Всякий раз, когда часть страницы перерисовывается, DevTools очертает этот раздел зеленым цветом.  

Чтобы включить мигание краски, выполните следующие действия.  

1.  Откройте средство **отрисовки.**  Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Включим **контрольный ящик "Мигать** краской".  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Мигает краской" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Мигает краской**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a>Просмотр наложения слоев с границами слоев  

Используйте **границы слоя,** чтобы просмотреть наложение границ слоев и плиток в верхней части страницы.  

Чтобы включить границы слоя, выполните следующие действия,  

1.  Откройте средство **отрисовки.**  Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Включаем **почтовый ящик Layer Borders.**  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Границы слоя" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Границы слоя**  
    :::image-end:::  
    
Перейдите к комментариям [debug_colors.cc][ChromiumDebugColors] для объяснения цветового кодирования.  

### <a name="find-scroll-performance-issues-in-realtime"></a>Поиск проблем с производительностью прокрутки в режиме реального времени  

Используйте проблемы с производительностью прокрутки для определения элементов страницы, которые имеют слушателей событий, связанных с прокрутки, которые могут повредить производительность страницы.  
DevTools описывает потенциально проблемные элементы в teal.  

Чтобы просмотреть проблемы с производительностью прокрутки, выполните следующие действия. 

1.  Откройте средство **отрисовки.**  Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)  
1.  Включите **почтовый ящик "Проблемы с производительностью прокрутки".**  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Проблемы с прокруткой производительности указывают на то, что объекты с ограниченным представлением неслойного представления могут навредить производительности прокрутки" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Проблемы с прокруткой** производительности указывают на то, что объекты с ограниченным представлением неслойного представления могут навредить производительности прокрутки  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Откройте командное меню — запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Начало работы с анализом производительности выполнения | Документы Майкрософт"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Демонстрация вкладок | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc — поиск кода"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
