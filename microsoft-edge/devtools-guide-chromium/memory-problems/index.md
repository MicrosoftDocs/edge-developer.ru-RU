---
description: Узнайте, как использовать Microsoft Edge и DevTools для поиска проблем с памятью, влияющих на производительность страниц, включая утечки памяти, раздутую память и частые сборы мусора.
title: Устранение проблем с памятью
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: afaea8ca561bd975490d9153cda40877786a0f08
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397834"
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

# <a name="fix-memory-problems"></a>Устранение проблем с памятью  

Узнайте, как использовать Microsoft Edge и DevTools для поиска проблем с памятью, влияющих на производительность страниц, включая утечки памяти, раздутую память и частые сборы мусора.  

### <a name="summary"></a>Сводка  

*   Узнайте, сколько памяти в настоящее время используется на странице с помощью диспетчера задач браузера Microsoft Edge.  
*   Визуализация использования памяти с течением времени с помощью **панели памяти.**  
*   Определите отдельные деревья DOM \(распространенная причина утечки памяти\) с помощью **снимка кучи.**  
*   Узнайте, когда новая память выделяется в кучи JavaScript \(JS кучи\) с помощью инструментов **распределения на временной шкале.**  

## <a name="overview"></a>Обзор  

В духе модели **производительности RAIL** в центре внимания ваших усилий по производительности должны быть ваши пользователи.  

<!--todo: add RAIL section when available  -->  

Проблемы с памятью важны, так как они часто воспринимаются пользователями.  Пользователи могут воспринимать проблемы с памятью следующим образом:  

*   **Производительность страницы со временем ухудшается.**  Возможно, это симптом утечки памяти.  Утечка памяти — это когда ошибка на странице приводит к постепенному использованию с течением времени все большего и большего объемов памяти.  
*   **Производительность страницы стабильно плохая.**  Возможно, это симптом раздува памяти.  Раздутие памяти — это когда на странице используется больше памяти, чем необходимо для оптимальной скорости страницы.  
*   **Производительность страницы задерживается**или часто останавливается.  Возможно, это симптом частых сборов мусора.  Сбор мусора — это когда браузер возвращает память.  Браузер решает, когда это произойдет.  Во время коллекций приостановка работы всех скриптов.  Так что если браузер собирает много мусора, время запуска скрипта будет приостановлено много.  

### <a name="memory-bloat-how-much-is-too-much"></a>Раздув памяти: сколько "слишком много"?  

Утечку памяти легко определить.  Если сайт постепенно использует все больше и больше памяти, то у вас есть утечка.  Но раздуть память немного сложнее прикрепить.  Что квалифицируется как "использование слишком емких воспоминаний"?  

Здесь нет жестких номеров, так как различные устройства и браузеры имеют различные возможности.  Та же страница, которая плавно выполняется на смартфоне высокого уровня, может привести к сбою на низком уровне смартфона.  

Здесь важно использовать модель RAIL и сосредоточиться на пользователях.  Узнайте, какие устройства популярны у пользователей, а затем проверьте свою страницу на этих устройствах.  При последовательном плохом опыте на странице могут быть превышены возможности памяти этих устройств.  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a>Мониторинг использования памяти в режиме реального времени с помощью диспетчера задач браузера Microsoft Edge  

Используйте диспетчер задач браузера Microsoft Edge в качестве отправной точки для расследования проблемы памяти.  Диспетчер задач браузера Microsoft Edge — это монитор реального времени, который сообщает, сколько памяти используется на странице в настоящее время.  

1.  Выберите `Shift` + `Esc` или перейдите в основное **** меню Microsoft Edge и выберите Дополнительные средства Browser Task Manager для открытия диспетчера задач браузера  >  **** Microsoft Edge.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Открытие диспетчера задач браузера Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Рис. 1. Открытие диспетчера задач браузера Microsoft Edge  
    :::image-end:::  
    
1.  Наведите курсор на заглавную таблицу диспетчера задач браузера Microsoft Edge, откройте контекстное меню \(правой кнопкой мыши\) и введите **память JavaScript**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Включить память JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Рис. 2. Включить память JavaScript  
    :::image-end:::  
    
В этих двух столбцах вы можете рассказать о том, как ваша страница использует память.  

*   Столбец **Memory** представляет родной памяти.  Узлы DOM хранятся в родной памяти.  Если это значение увеличивается, создаются узлы DOM.  
*   Столбец **Памяти JavaScript** представляет кучу JS.  Этот столбец содержит два значения.  Вас интересует живой номер \(число в скобках\).  Живой номер представляет, сколько памяти используют объекты, достигаемые на странице.  Если это число увеличивается, создаются либо новые объекты, либо растут существующие объекты.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a>Визуализация утечек памяти с помощью панели Performance  

Вы также можете использовать панель Performance в качестве еще одной отправной точки в вашем расследовании.  Панель Performance позволяет со временем визуализировать использование страницы в памяти.  

1.  Откройте панель **Performance** на DevTools.  
1.  Включить **почтовый** ящик памяти.  
1.  [Запись.][DevtoolsEvaluatePerformanceReferenceRecord]  

> [!TIP]
> Это хорошая практика, чтобы начать и закончить запись с принудительного сбора мусора.  Для принудительного сбора мусора выберите кнопку **сбора** мусора во время ![ ][ImageForceGarbageCollectionIcon] записи.  

Чтобы продемонстрировать записи памяти, рассмотрим ниже код:  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Каждый раз, когда выбрана кнопка, на которую ссылается код, к тексту документа примыкают 10 тысяч узлов, а на массив выталкивали строку из одного `div` `x` миллиона `x` символов.  При запуске предыдущего примера кода создается запись в панели **Performance,** как на следующем рисунке.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Простой рост" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Рис. 3. Простой рост  
:::image-end:::  

Во-первых, объяснение пользовательского интерфейса.  Граф **HEAP** в области **Обзор** \(ниже **NET**\) представляет кучу JS.  Ниже области **Обзор** является области **Счетчик.**  Использование памяти разбивается по Кучи JS \(так же, как график **HEAP** в области Обзор\), документов, узлов DOM, слушателей и памяти GPU. ****  Выключите почтовый ящик, чтобы скрыть его от графа.  

Теперь анализ кода по сравнению с предыдущим рисунком.  Если вы просмотрите счетчик узла \(зеленый график\), он будет полностью совпадать с кодом.  Количество узлов увеличивается в дискретных шагах.  Можно предположить, что каждое увеличение числа узлов является вызовом `grow()` .  График Кучи JS \(синий график\) не так прост.  В соответствии с лучшими практиками, первый провал фактически является **** принудительной коллекцией мусора \(выберите кнопку сбора мусора ![ принудительного ][ImageForceGarbageCollectionIcon] сбора мусора\).  По мере выполнения записи отображаются пики размера Кучи JS.  Это естественно и ожидаемо: код JavaScript создает узлы DOM на каждой кнопке, вы выбираете, и много работы при создании строки из одного миллиона символов.  Ключевым моментом здесь является тот факт, что куча JS заканчивается выше, чем она началась \(здесь "начало" является точкой после принудительного сбора мусора\).  В реальном мире, если вы увидели этот шаблон увеличения размера или размера узла Кучи JS, это может потенциально определить утечку памяти.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a>Обнаружение отсоединяемой памяти дерева DOM с помощью снимков кучи  

Узел DOM — это только мусор, собираемый, если на странице нет ссылок на узел из дерева DOM или кода JavaScript.  Сообщается, что узел "отсоединяется" при удалении из дерева DOM, но некоторые JavaScript по-прежнему ссылаются на него.  Отдельные узлы DOM являются распространенной причиной утечек памяти.  В этом разделе рассказывается об использовании профилей кучи в DevTools для определения отсоединяемых узлов.  

Вот простой пример отсоединяемых узлов DOM.  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

Выбор кнопки, на которая ссылается в коде, создает `ul` узел с десятью `li` детьми.  Узлы ссылаются на код, но не существуют в дереве DOM, поэтому каждый из них отсоединяется.  

Снимки кучи — это один из способов определения отсоединяемых узлов.  Как следует из названия, на снимках кучи покажите, как память распределяется между объектами JS и узлами DOM для вашей страницы в момент момент снимка.  

Чтобы создать снимок, откройте DevTools **** и перейдите **** к панели памяти, выберите кнопку "Моментальный снимок" > **Снимок.**  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Снимок кучи" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Рис. 4. Снимок кучи  
:::image-end:::  

На обработку и загрузку снимка может потребоваться некоторое время.  После его завершения выберите его из левой панели \(с именем **HEAP SNAPSHOTS**\).  

`Detached`Введите **текстовый ящик фильтра** класса для поиска отсоединяемого дерева DOM.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Фильтрация для отсоединяющихся узлов" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Рис. 5. Фильтрация для отсоединяющихся узлов  
:::image-end:::  

Расширь карат, чтобы исследовать отдельное дерево.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Исследование отдельного дерева" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Рис. 6. Изучение отдельного дерева  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Выберите узел для дальнейшего изучения.  В области **Объекты** можно просмотреть дополнительные сведения о коде, который ссылается на него.  Например, на следующем рисунке переменная `detachedNodes` ссылаться на узел.  Чтобы устранить определенную утечку памяти, необходимо изучить код, использующий переменную, и убедиться, что ссылка на узел удаляется, когда она больше `detachedUNode` не требуется.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Исследование узла" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Рис. 7. Исследование узла  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a>Определение утечек памяти JS с помощью инструментов распределения на временной шкале  

**Инструментирование распределения на временной шкале** — это еще один инструмент, который может помочь вам отслеживать утечки памяти в кучи JS.  

Демонстрация **инструментов распределения на временной шкале**  с помощью следующего кода.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

При каждом нажатии кнопки, на которую ссылается код, в массив добавляется строка из одного миллиона `x` символов.  

Чтобы записать приборы распределения на временной шкале, откройте **** DevTools, перейдите к панели памяти, выберите инструменты распределения на кнопке радиохронологии, **** выберите кнопку Начните, выполните действия, которые, как вы подозреваете, вызывают утечку памяти, а затем выберите кнопку остановки записи профиля Стоп записи профиля стоп-записи. **** **** ![ ][ImageStopRecordingIcon]  

Во время записи обратите внимание на то, что в приборе Распределения на временной шкале, как на следующем рисунке, покажите, какие-либо синие полосы.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Новые выделения" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Рис. 8. Новые выделения  
:::image-end:::  

Эти синие полосы представляют новые выделения памяти.  Эти новые выделения памяти являются вашими кандидатами для утечки памяти.  Вы можете увеличить планку, чтобы отфильтровать панели **конструктора,** чтобы показать только объекты, выделенные в указанный период времени.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Шкала масштабирования выделения" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Рис. 9. Шкала масштабирования выделения  
:::image-end:::  

Расширьте объект и выберите значение, чтобы просмотреть дополнительные сведения в **области Объект.**  Например, на следующем рисунке в подробностях вновь выделенного объекта указывается, что он был выделен переменной `x` в `Window` области.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Сведения об объектах" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Рис. 10. Сведения об объектах  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a>Исследование распределения памяти по функции  

Используйте тип **профилирования** выборки распределения для просмотра распределения памяти с помощью функции JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Выборка распределения записей" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Рис. 11. Выборка распределения записей  
:::image-end:::  

1.  Выберите радио **кнопку Распределение выборки.**  Если на странице есть рабочий, вы можете выбрать его в качестве целевого профилинга с помощью меню отсевов рядом с кнопкой **"Пуск".**  
1.  Выберите **кнопку Начните.**  
1.  Выполните действия на веб-странице, которую необходимо исследовать.  
1.  Выберите **кнопку Stop** после завершения всех действий.  

В DevTools показана разбивка распределения памяти по функции.  Представление по умолчанию **— Heavy (Bottom Up),** которое отображает функции, которые выделяли больше всего памяти в верхней части.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Выборка распределения" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Рис. 12. Выборка распределения  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a>Spot frequent garbage collections  

Если страница часто приостанавливована, могут возникнуть проблемы со сбором мусора.  

Для частого сбора мусора можно использовать либо диспетчер задач браузера Microsoft Edge, либо записи памяти производительности.  В диспетчере задач браузера Microsoft Edge **** часто возрастают и снижаются значения памяти памяти или **JavaScript,** что представляет собой частый сбор мусора.  В записях производительности частые изменения \(рост и падение\) в графах Кучи JS или числа узлов указывают на частую коллекцию мусора.  

После того как вы определили проблему, **** вы можете использовать инструменты распределения на записи временной шкалы, чтобы узнать, где выделяется память и какие функции вызывают выделение.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Запись производительности — ссылка на анализ производительности"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
