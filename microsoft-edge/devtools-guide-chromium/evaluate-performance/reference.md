---
description: Справочник по всем способам записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d5b6be92c1419ba880a94c62c3f586a740816622
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230763"
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

# Справочные материалы по анализу производительности  

Эта страница является полным справочником по функциям Microsoft Edge DevTools, связанным с анализом производительности.  

Перейдите [к курсу "Начало][DevtoolsEvaluatePerformanceGettingStarted] работы с анализом производительности времени выполнения", чтобы получить руководство по анализу производительности страницы с помощью [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

## Запись производительности  

### Запись производительности в времени выполнения  

Зафиксируйте производительность времени выполнения, если нужно проанализировать производительность страницы в ее работе, а не загрузку.  

1.  Перейдите на страницу, которую нужно проанализировать.  
1.  Выберите **вкладку "Производительность"** в DevTools.  
1.  Choose **Record** \( ![ Record icon ][ImageRecordIcon] \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Record**  
    :::image-end:::  
    
1.  Взаимодействовать со страницей.  DevTools записи все действия страницы, которые происходят в результате ваших взаимодействий.  
1.  Choose **Record** again or choose **Stop** to stop recording.  
    
### Запись производительности загрузки  

Зафиксируйте производительность загрузки, если нужно проанализировать производительность страницы во время ее загрузки, а не запускать ее.  

1.  Перейдите на страницу, которую нужно проанализировать.  
1.  Откройте панель **производительности** DevTools.  
1.  Choose **Refresh page** \( Refresh Page ![ ][ImageRefreshPageIcon] \).  DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись через пару секунд после завершения загрузки.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Страница обновления" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Страница обновления**  
    :::image-end:::  
    
DevTools автоматически масштабируется в части записи, где произошла большая часть действия.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Запись загрузки страницы" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Запись загрузки страницы  
:::image-end:::  

### Снимок экрана во время записи  

Включив этот **снимок экрана,** зафиксировать снимок экрана каждого кадра во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="The Screenshots checkbox" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   The **Screenshots** checkbox  
:::image-end:::  

Перейдите [к снимку экрана,](#view-a-screenshot) чтобы узнать, как взаимодействовать со снимками экрана.  

### Принудительное сбор мусора во время записи  

Пока вы записываете страницу, выберите "Сбор **мусора"** \( Значок ![ "Сбор ][ImageCollectGarbageIcon] мусора"), чтобы принудительно собрать сборку мусора.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Сбор мусора" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Сбор мусора  
:::image-end:::  

### Показать параметры записи  

Choose **Capture settings** \( ![ Capture settings ][ImageCaptureSettingsIcon] \) to expose more settings related to how DevTools captures performance recordings.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Раздел Параметры захвата" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Раздел **"Параметры захвата"**  
:::image-end:::  

### Отключение примеров JavaScript  

По умолчанию в основном **разделе** записи отображаются подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.  Чтобы отключить эти стеки вызовов:  

1.  Откройте меню **параметров захвата.**  Перейдите [к параметрам демонстрации записи.](#show-recording-settings)  
1.  Включите **этот контрольный ящик.**  
1.  Зафиксим страницу.  
    
На следующих двух рисунках показана разница между отключением и включением примеров JavaScript.  Основной **раздел** записи намного короче, если выборка отключена, так как он опустить все стеки вызовов JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Пример записи, когда отключены примеры JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Пример записи, когда отключены примеры JS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Пример записи, когда примеры JS включены" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Пример записи, когда примеры JS включены  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Throttle the network while recording  

Чтобы отлалить сеть во время записи:  

1.  Откройте меню **параметров захвата.**  Перейдите [к параметрам демонстрации записи.](#show-recording-settings)  
1.  Установите **для сети** нужный уровень регулирования.  
    
### Throttle the CPU while recording  

Чтобы отлалить ЦП при записи:  

1.  Откройте меню **параметров захвата.**  Перейдите [к параметрам демонстрации записи.](#show-recording-settings)  
1.  Установите **для ЦП** нужный уровень регулирования.  
    
Регулирование относительно возможностей компьютера.  Например, при **замедлении работы ЦП** в 2 раза медленнее, чем обычно.  DevTools не имитируют ЦП мобильных устройств, так как архитектура мобильных устройств сильно отличается от архитектуры настольных компьютеров и ноутбуков.  

### Включить расширенный инструментарий paint  

Чтобы просмотреть подробный инструментарий paint:  

1.  Откройте меню **параметров захвата.**  Перейдите [к параметрам демонстрации записи.](#show-recording-settings)  
1.  Проверьте , **включить расширенный инструментарий paint (медленно).**  

Чтобы узнать, как взаимодействовать с данными paint, перейдите к слоям просмотра [и](#view-layers-information) профилю [просмотра кисти.](#view-paint-profiler)  

## Сохранение записи  

Чтобы сохранить запись, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить **профиль".**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Сохранение профиля" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Сохранение профиля**  
:::image-end:::  

## Загрузка записи  

Чтобы загрузить запись, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Профиль загрузки".**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Профиль загрузки" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Профиль загрузки**  
:::image-end:::  

## Очистка предыдущей записи  

После записи нажмите кнопку **Clear recording** \( Clear recording icon \), чтобы очистить эту запись с ![ панели ][ImageClearRecordingIcon] **"Производительность".**  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Очистка записи" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Очистка записи**  
:::image-end:::  

## Анализ записи производительности  

После [записи производительности](#record-runtime-performance) или загрузки **** [записи](#record-load-performance)панель производительности предоставляет большое количество данных для анализа производительности только что произошло.  

### Выбор части записи  

Перетащите мышь влево **** или вправо по обзору, чтобы выбрать часть записи.  Обзор **—** это раздел, содержащий **диаграммы FPS,** **ЦП**и **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Перетащите мышь по обзору для масштабирования" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Перетащите мышь по **обзору для** масштабирования  
:::image-end:::  

Чтобы выбрать часть с помощью клавиатуры:  

1.  Выберите фон раздела **Main** или любой из разделов рядом с ними, например "Взаимодействия", **** **"Сеть"** или **"GPU".**  Этот рабочий процесс клавиатуры работает только в том случае, если один из этих разделов находится в фокусе.  
1.  Используйте `W` клавиши , , , чтобы увеличить масштаб, переместить влево, уменьшить масштаб и переместить `A` `S` `D` вправо, соответственно.  

Чтобы выбрать часть с помощью панели отслеживания, выполните следующие действия.  

1.  Наведите указатель мыши на раздел **"Обзор"** или **"Сведения".**  Раздел **"Обзор"** — это область, **содержащая диаграммы FPS,** **ЦП**и **NET.**  Раздел **"Сведения"** — это область, **содержащая основной** раздел, раздел **"Взаимодействия"** и так далее.  
1.  Двумя пальцами проведите пальцем вверх, чтобы уменьшить масштаб, проведите пальцем влево, прокрутка вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы переместить вправо.  

Чтобы прокрутить длинную диаграмму в разделе **Main** или любой из соседей, выберите и удерживайте при перетаскиванием вверх и вниз.  Перетащите влево и вправо, чтобы переместить выбранную часть записи.  

### Действия поиска  

Выберите `Control` + `F` \(Windows, Linux\) или `Command` + `F` \(macOS\), **** чтобы открыть поле поиска в нижней части панели производительности.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Поле поиска" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   Поле поиска  
:::image-end:::  

Для навигации по действиям, которые соответствуют вашему запросу:  

*   Используйте кнопки **Previous** \( ![ Previous ][ImagePreviousIcon] \) и **Next** \( ![ Next ][ImageNextIcon] \).  
*   Выберите `Shift` + `Enter` предыдущий или `Enter` следующий.  

Изменение параметров запроса:  

*   Нажмите **"С чувствительным** к делу" \( ![ "С чувствительным к ][ImageSearchCaseIcon] делу"), чтобы сделать запрос чувствительным к делу.  
*   Нажмите **Regex** \( ![ Regex ][ImageSearchRegexIcon] \), чтобы использовать регулярное выражение в запросе.  

Чтобы скрыть поле поиска, нажмите кнопку **"Отмена".**  

### Просмотр активности основного потока  

Используйте основной **раздел** для просмотра действий, которые произошли в основном потоке страницы.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Основной **** раздел  
:::image-end:::  

Выберите событие, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**  DevTools описывает выбранное событие.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Дополнительные сведения об анонимной функции на вкладке Сводка" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Дополнительные сведения о `anonymous` функции на **вкладке "Сводка"**  
:::image-end:::  

DevTools представляет основные действия потока с помощью диаграммы ..  Ось x представляет запись с течением времени.  Ось Y представляет стек вызовов.  События в верхней части вызывают события под ней.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Диаграмма с замеской диаграммой" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Диаграмма с замеской диаграммой  
:::image-end:::  

На предыдущем рисунке событие `click` вызвало событие `Function Call` в `activitytabs.js` строке 53.  Ниже `Function Call` приведены сообщения о том, что была запускаться анонимная функция.  Запрашиваемая анонимная `a` функция, которая запросила `wait` `Minor GC` запрос.  

DevTools назначает скриптам случайные цвета.  На предыдущем рисунке запросы функций из одного сценария имеют светло-зеленый цвет.  Запросы от другого сценария имеют цвет бежевого цвета.  Темно-желтый представляет действие при написании скриптов, а сиреневый — действие отрисовки.  Эти темные желтые и сиреневые события согласованы во всех записях.  

Если вы хотите скрыть подробную диаграмму запросов [JavaScript,](#disable-javascript-samples) перейдите в окне "Отключить примеры JavaScript".  Если примеры JS отключены, отображаются только события высокого уровня, такие как и на `Event: click` `Function Call` предыдущем `str` рисунке.  

### Просмотр действий в таблице  

После записи страницы вам не нужно полагаться **** только на основной раздел для анализа действий.  DevTools также предоставляет три таблильных представления для анализа действий.  Каждое представление дает разные представления о действиях:  

*   Если вы хотите просмотреть корневые действия, которые вызывают большую часть работы, используйте вкладку ["Дерево вызовов".](#the-call-tree-tab)  
*   Если вы хотите просмотреть действия, на которые было потрачено больше всего времени, используйте вкладку [Bottom-Up.](#the-bottom-up-tab)  
*   Чтобы просмотреть действия в том порядке, в котором они произошли во время записи, используйте вкладку ["Журнал событий".](#the-event-log-tab)  
    
> [!NOTE]
> Следующие три раздела относятся к одной и той же демонстрации.  Запустите демонстрацию самостоятельно на [демонстрационных вкладок активности.][ActivityTabsDemo]  

#### Корневые действия  

Ниже объясняется концепция **** корневых действий, **** упоминаемая в разделах "Дерево вызовов", "Снизу **вверх"** и **"Журнал событий".**  

Корневые действия — это те действия, которые приводят к определенной работе браузера.  Например, при выборе веб-страницы браузер выполняет действие в качестве `Event` корневого действия.  Это `Event` может привести к запуску обработера и так далее.  

На диаграмме "Главный" **корневые** действия находятся в верхней части диаграммы.  На **вкладке "Дерево вызовов"** и **"Журнал событий"** корневые действия являются элементами верхнего уровня.  

Перейдите [на вкладку "Дерево вызовов"](#the-call-tree-tab) для примера корневых действий.  

#### Вкладка "Дерево вызовов"  

Используйте **вкладку "Дерево** вызовов", чтобы просмотреть, какие [корневые действия](#root-activities) вызывают больше всего работы.  

Вкладка **"Дерево** вызовов" отображает действия только во время выбранной части записи.  Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Вкладка Дерево вызовов" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Вкладка **"Дерево вызовов"**  
:::image-end:::  

На предыдущем рисунке верхний уровень элементов в столбце "Действие", например корневые **** `Evaluate Script` `Parse HTML` действия.  Вложенное представляет стек вызовов.  Например, на предыдущем рисунке, `Parse HTML` который вызвал `Evaluate Script` и `Compile Script` `(anonymous)` .  

**Self Time** представляет время, непосредственно затраченное на это действие.  **Общее время** представляет время, затраченное на это действие или любой из его детей.  

Выберите **"Самостоятельное время",** **"Общее время"** или **"Действия",** чтобы отсортировать таблицу по этому столбцу.  

Используйте **текстовое поле фильтра** для фильтрации событий по имени действия.  

По умолчанию для **меню группировки** установлено значение **"Нет группировки".**  Используйте меню **группировки** для сортировки таблицы действий на основе различных критериев.  

Choose **Show Heaviest Stack** \( Show ![ Heaviest Stack ][ImageShowHeaviestStackIcon] \) to reveal another table to the right of the **Activity** table.  Выберите действие для заполнения самой **активной таблицы стека.**  В **таблице "Самый большой** стек" отображается, какие из выбранных действий больше всего запускались.  

#### Вкладка Bottom-Up  

Вкладка **"Снизу вверх"** используется для просмотра действий, которые непосредственно заняли больше всего времени в совокупности.  

На **вкладке "Снизу вверх"** отображаются только действия в выбранной части записи.  Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Вкладка Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Вкладка **"Снизу вверх"**  
:::image-end:::  

На **диаграмме "Главный** раздел" предыдущего рисунка перейдите к этому практически всему времени, затраченному на `Parse HTML` запуск.  Верхнее действие на **вкладке "Вверх"** предыдущего рисунка — `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Перейдите на **вкладку "Снизу вверх".** Далее самое дорогое действие `Layout` .  

Столбец **"Самообнаправление"** представляет собой агрегированное время, затраченное непосредственно на это действие, во всех случаях.  

Столбец **"Общее время"** представляет собой агрегированное время, затраченное на это действие или на какие-либо из его детей.  

#### Вкладка "Журнал событий"  

Вкладка **"Журнал событий"** используется для просмотра действий в том порядке, в котором они произошли во время записи.  

Вкладка **"Журнал** событий" отображает действия только во время выбранной части записи.  Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Вкладка Журнал событий" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Вкладка **"Журнал событий"**  
:::image-end:::  

Столбец **"Время начала"** представляет точку начала этого действия относительно начала записи.  Например, время начала выбранного элемента на предыдущем рисунке означает, что действие началось `175.7 ms` со 175,7 мс после начала записи.  

Столбец **"Самостоятельное** время" представляет время, затраченное непосредственно на это действие.  

Столбцы **"Общее время"** представляют время, затраченное непосредственно на это действие или на какие-либо из детей.  

Выберите **время начала,** **время**самостоятельного выбора или **общее** время сортировки таблицы по этому столбцу.

Используйте **текстовое поле фильтра** для фильтрации действий по имени.  

Используйте меню **"Длительность",** чтобы отфильтровать все действия, которые заняли менее 1 мс или 15 мс.  По умолчанию в **меню "Длительность"** установлено значение **"Все",** то есть показаны все действия.  

Отключает **проверки загрузки,** сценариев, отрисовки или рисования, чтобы отфильтровать все действия из этих категорий. **** **** ****  

### Просмотр действий GPU  

Просмотр действий GPU в разделе **GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Раздел GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Раздел **GPU**  
:::image-end:::  

### Просмотр растровой активности  

Просмотр растерных действий в **разделе Растера.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Раздел Растер" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Раздел **"Растер"**  
:::image-end:::  

### Просмотр взаимодействий  

Раздел **"Взаимодействия"** используется для поиска и анализа взаимодействий с пользователем, которые произошли во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Раздел Взаимодействия" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Раздел **"Взаимодействия"**  
:::image-end:::  

Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание главного потока.  

Выберите взаимодействие, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**  

### Анализ кадров в секунду  

DevTools предоставляет множество способов анализа кадров в секунду:  

*   Используйте [диаграмму FPS,](#the-fps-chart) чтобы получить обзор FPS в течение всей записи.  
*   Используйте [раздел "Кадры",](#the-frames-section) чтобы просмотреть, сколько времени занимает определенный кадр.  
*   Используйте счетчик **FPS для** оценки в режиме реального времени в FPS при запуске страницы.  Перейдите [к просмотру кадров в секунду в режиме реального времени с помощью счетчика кадров](#view-frames-per-second-in-realtime-with-the-fps-meter)в секунду.  
    
#### Диаграмма FPS  

Диаграмма **FPS** предоставляет обзор частоты кадров во время записи.  Как правило, чем выше зеленая гля, тем выше частота кадров.  

Красная черта над **диаграммой FPS** — это предупреждение о том, что частота кадров отброшена настолько низко, что это может нанести вред пользовательскому интерфейсу.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Диаграмма **FPS**  
:::image-end:::  

#### Раздел "Кадры"  

В **разделе "Кадры"** указывается, сколько времени занимает определенный кадр.  

Наведите курсор на кадр, чтобы просмотреть tooltip с дополнительными сведениями о нем.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Наведении курсор на кадр" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Наведении курсор на кадр  
:::image-end:::  

Выберите кадр, чтобы просмотреть дополнительные сведения о кадре на вкладке **"Сводка".**  DevTools описывает выбранный кадр синим цветом.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Просмотр кадра на вкладке Сводка" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Просмотр кадра на вкладке **"Сводка"**  
:::image-end:::  

### Просмотр сетевых запросов  

Раз развернуть **раздел "Сеть",** чтобы просмотреть каскад сетевых запросов, которые произошли во время записи.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Раздел Сеть" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Раздел **"Сеть"**  
:::image-end:::  

Запросы имеют код цвета следующим образом:  

*   HTML: синий  
*   CSS: Сиреневый  
*   JS: желтый  
*   Изображения: зеленый  
    
Выберите запрос, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**  Например, на предыдущем рисунке **** вкладка "Сводка" отображает дополнительные сведения о синем запросе, выбранном в разделе **"Сеть".**  

Темно-синий квадрат в левом верхнем конце запроса означает, что это запрос с более высоким приоритетом.  Светлее-синий квадрат означает более низкий приоритет.  Например, на предыдущем рисунке синий выбранный запрос имеет более высокий приоритет, а зеленый — более низкий.  

На 1-м из следующих рисунков запрос представлен линией слева, строкой в середине с темной частью и светлой частью, а также линией `www.bing.com` справа.  Во 2-й части следующих рисунков показано соответствующее представление того же запроса на вкладке **"Синхронизация"** панели **"Сеть".**  Вот как эти два представления соовествуют друг с другом:

*   Левая строка — это вся группа `Connection Start` событий включительно.  Другими словами, это все до `Request Sent` , монопольный.  
*   Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .  
*   Темная часть панели — `Content Download` .  
*   Правая строка — это, по сути, время, затраченное на ожидание главного потока.  Он не представлен на вкладке **"Синхронизация".**  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Представление строки запроса www.bing.com строки" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Представление запроса на строке `www.bing.com`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Средство Сеть" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         Средство **"Сеть"**  
: ::image-end:::  
   :::column-end:::
:::row-end:::

### Просмотр метрик памяти  

Включив этот **параметр,** вы можете просмотреть показатели памяти из последней записи.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="The Memory checkbox" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   The **Memory** checkbox  
:::image-end:::  

DevTools отображает новую диаграмму **"Память"** над вкладками **"Сводка".**  Под диаграммой **NET** также есть новая диаграмма **HEAP.**  Диаграмма **HEAP** предоставляет те же сведения, что и строка **"Куче JS"** в **диаграмме "Память".**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Показатели памяти" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Показатели памяти  
:::image-end:::  

Цветные линии на диаграмме со картой цветных контрольных точек над диаграммой.  
Отключать этот контрольный ящик, чтобы скрыть эту категорию в диаграмме.  

Диаграмма отображает только область выбранной в данный момент записи.  Например, на предыдущем рисунке **** диаграмма "Память" показывает только использование памяти от 400 мс до отметки 1750 мс.  

### Просмотр длительности части записи  

При анализе таких разделов, как **"Сеть"** или "Главная", **** иногда требуется более точную оценку времени, за который потребовалось определенное событие.  Удерживайте, выбирайте и удерживайте, перетаскивать влево или вправо, чтобы выбрать `Shift` часть записи.  В нижней части выделения DevTools показывает, сколько времени занимает эта часть.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Просмотр длительности части записи" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Просмотр длительности части записи  
:::image-end:::  

### Просмотр снимка экрана  

Перейдите [к снимкам экрана захвата](#capture-screenshots-while-recording) во время записи, чтобы узнать, как включить снимки экрана.  

Наведите курсор на **обзор,** чтобы просмотреть снимок экрана с изображением страницы в этот момент записи.  Обзор **—** это раздел, содержащий **диаграммы ЦП,** **FPS**и **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Просмотр снимка экрана" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Просмотр снимка экрана  
:::image-end:::  

Снимки экрана также можно просмотреть, выбрав кадр в разделе **"Кадры".**  DevTools отображает небольшую версию снимка экрана на вкладке **"Сводка".**  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Просмотр снимка экрана на вкладке Сводка" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Просмотр снимка экрана на **вкладке "Сводка"**  
:::image-end:::  

Выберите эскиз на вкладке **"Сводка",** чтобы увеличить масштаб на снимке экрана.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Масштабирование снимка экрана на вкладке Сводка" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Масштабирование снимка экрана на **вкладке "Сводка"**  
:::image-end:::  

### Просмотр сведений о уровнях  

Чтобы просмотреть сведения о расширенных уровнях кадра:  

1.  [Включив расширенный инструментарий paint.](#turn-on-advanced-paint-instrumentation)  
1.  Выберите кадр в разделе **"Кадры".**  DevTools отображает сведения о слоях на новой вкладке **"Слои"** рядом с вкладкой **"Журнал событий".**  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="The Layers pane" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       The **Layers** pane  
    :::image-end:::  
    
Наведите курсор на слой, чтобы выделить его на схеме.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Выделение слоя" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Выделение слоя  
:::image-end:::  

Чтобы переместить схему:  

*   Choose **Pan Mode** \( Pan Mode ![ ][ImagePanModeIcon] \) to move along the X and Y axes.  
*   Выберите **режим поворота** \( ![ Режим поворота ][ImageRotateModeIcon] \), чтобы вращаться вдоль оси Z.  
*   Choose **Reset Transform** \( Reset Transform ![ ][ImageResetTransformIcon] \) to reset the diagram to the original position.  
    
### Просмотр профиля paint  

Чтобы просмотреть дополнительные сведения о событии paint:  

1.  [Включит](#turn-on-advanced-paint-instrumentation).  
1.  Выберите событие **Paint** в основном **разделе.**  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Вкладка Профиль paint" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Вкладка **"Профиль paint"**  
    :::image-end:::  
    
## Анализ производительности отрисовки с помощью вкладки "Отрисовка"  

Используйте функции вкладки **"Отрисовка"** для визуализации производительности отображения страницы.  

Чтобы открыть **вкладку "Отрисовка":**  

1.  [Откройте меню команд.][DevToolsCommandMenu]  
1.  Начните ввод `Rendering` текста и выберите `Show Rendering` .  DevTools отображает вкладку **"Отрисовка"** в нижней части окна DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Вкладка Отрисовка" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       Вкладка **"Отрисовка"**  
    :::image-end:::  
    
### Просмотр кадров в секунду в режиме реального времени с помощью счетчика кадров в секунду  

Счетчик **FPS —** это наложение, которое отображается в правом верхнем углу окна.  Он предоставляет оценку в режиме реального времени в FPS при запуске страницы.  Чтобы открыть счетчик **FPS:**  

1.  Откройте **вкладку "Отрисовка".**  Na [Анализ производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)  
1.  Включите **флажки счетчика FPS.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       Счетчик **FPS**  
    :::image-end:::  
    
### Просмотр событий рисования в режиме реального времени с помощью paint Flashing  

Используйте Paint Flashing, чтобы получить представление всех событий paint на странице в режиме реального времени.  Каждый раз, когда часть страницы перерисовка, DevTools описывает этот раздел зеленым цветом.  

Чтобы включить Paint Flashing, выполните следующие действия.  

1.  Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки на вкладке "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)  
1.  Включите **контрольный ящик Paint Flashing.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Paint Flashing**  
    :::image-end:::  
    
### Просмотр наложения слоев с границами уровней  

Используйте **границы уровней** для просмотра наложения границ слоя и плиток в верхней части страницы.  

Чтобы включить границы уровня, выполните следующие действия.  

1.  Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)  
1.  Включите **контрольный ящик "Границы** слоя".  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Границы слоя" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Границы слоя**  
    :::image-end:::  
    
Перейдите к комментариям [в debug_colors.cc,][ChromiumDebugColors] чтобы получить объяснение цветового кодирования.  

### Поиск проблем с производительностью прокрутки в режиме реального времени  

Используйте проблемы с производительностью прокрутки, чтобы определить элементы страницы с прослушивателями событий, связанными с прокрутки, которые могут нанести вред производительности страницы.  
DevTools описывает потенциально проблемные элементы в этом документе.  

Чтобы просмотреть проблемы с производительностью прокрутки, выполните следующие действия. 

1.  Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)  
1.  Включите **контрольный список "Проблемы с производительностью прокрутки".**  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Проблемы прокрутки производительности указывают на то, что объекты с неуровневой прокруткой могут повредит производительности прокрутки" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Проблемы прокрутки производительности** указывают на то, что объекты с неуровневой прокруткой могут повредит производительности прокрутки  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Откройте меню команд — запустите команды с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Начало работы с анализом производительности во время выполнения | Документы Майкрософт"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Демонстрация вкладок активности | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc — поиск кода"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
