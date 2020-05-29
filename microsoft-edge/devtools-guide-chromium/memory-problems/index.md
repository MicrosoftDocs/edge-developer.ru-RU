---
title: Устранение проблем с памятью
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611764"
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





# Устранение проблем с памятью   



Узнайте, как использовать Microsoft EDGE и DevTools для обнаружения проблем с памятью, в том числе утечек памяти, чрезмерного объема памяти и частых сборок мусора.  

### Краткий обзор  

*   Сведения о том, сколько памяти использует ваша страница в диспетчере задач браузера Microsoft Edge.  
*   Визуализировать использование памяти по времени с помощью панели **памяти** .  
*   Определите отсоединенные деревья DOM \ (распространенная причина утечек памяти \) с помощью **моментального снимка кучи**.  
*   Узнайте о том, когда новая память выделяется в куче JavaScript \ (JS-приложение \) с **инструментированием выделения на временной шкале**.  

## Обзор  

В качестве духу модели производительности **салазок** необходимо сосредоточиться на эффективности работы пользователей.  

<!--todo: add RAIL section when available  -->  

Проблемы с памятью важны, так как они часто perceivable пользователями.  Пользователи могут воспринимать проблемы с памятью следующими способами:  

*   **Производительность страницы постепенно восстановится с течением времени**.  Это может быть симптомом утечки памяти.  Утечка памяти возникает, когда ошибка на странице вызывает последовательное использование страницы больше и больше памяти с течением времени.  
*   **Производительность страницы постоянно неисправна**.  Это может быть симптомом чрезмерного объема памяти.  Память забывает в том случае, если на странице используется больше памяти, чем требуется для оптимальной скорости страницы.  
*   **Производительность страницы часто задерживается или приостанавливается**.  Это может быть симптомом частых сборок мусора.  Сборка мусора происходит, когда браузер освобождает память.  Браузер определяет, когда это происходит.  Во время коллекций все выполняемые сценарии приостановлены.  Таким образом, если браузер собирают большое количество мусора, среда выполнения сценариев будет приостанавливаться на очень много времени.  

### Чрезмерное использование памяти: насколько это "слишком много"?  

Определение утечек памяти очень просто.  Если на сайте используется больше и больше памяти, это значит, что у вас есть утечка.  Но закрепление памяти немного сложнее.  Что такое "использование слишком большого объема памяти"?  

Здесь нет жестких номеров, так как различные устройства и браузеры имеют различные возможности.  Одна и та же страница, работающая на высококачественном смартфоне, может аварийно завершить работу на смартфоне.  

Основной способ — использовать модель САЛАЗОК и сосредоточиться на ваших пользователях.  Узнайте, какие устройства будут популярными для ваших пользователей, а затем протестируйте свою страницу на этих устройствах.  Если вы постоянно восстановитсяе, страница может превысить возможности памяти для этих устройств.  

## Наблюдение за использованием памяти в режиме реального времени с помощью диспетчера задач браузера Microsoft Edge  

Используйте диспетчер задач браузера Microsoft EDGE в качестве отправной точки для исследования проблем с памятью.  Диспетчер задач браузера Microsoft Edge — это монитор реального времени, в котором сообщается, сколько памяти использует страница в данный момент.  

1.  Нажмите `Shift` + `Esc` или перейдите в главное меню Microsoft EDGE и выберите пункт **другие инструменты**  >  **Диспетчер задач браузера** , чтобы открыть диспетчер задач браузера Microsoft Edge.  
    
    > ##### Рис. 1  
    > Открытие диспетчера задач браузера Microsoft Edge  
    > ![Открытие диспетчера задач браузера Microsoft Edge][ImageTaskManager]  
    
1.  Щелкните правой кнопкой мыши заголовок таблицы в диспетчере задач браузера Microsoft EDGE и включите **память JavaScript**.  
    
    > ##### Рисунок 2  
    > Включите память JavaScript  
    > ![Включите память JavaScript][ImageJavascriptMemory]  
    
В этих двух столбцах указываются различные способы использования памяти на странице.  

*   Столбец **Memory** представляет встроенную память.  Узлы DOM хранятся в собственной памяти.  Если это значение возрастает, узлы DOM создаются.  
*   Столбец " **память" JavaScript** представляет кучу JS.  Этот столбец состоит из двух значений.  Интересующее вас значение — номер Live (число в круглых скобках).  Номер "в сети" показывает, сколько памяти используется достижимыми объектами на странице.  Если это число будет увеличиваться, создаются либо новые объекты, либо все существующие объекты.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Визуализация утечек памяти с помощью панели "производительность"  

Кроме того, вы можете использовать панель производительности как другую отправную точку расследования.  С помощью панели Performance можно визуализировать использование памяти страницы с течением времени.  

1.  Откройте панель " **производительность** " на DevTools.  
1.  Включите флажок " **память** ".  
1.  [Создание записи][DevtoolsEvaluatePerformanceReferenceRecord].  

> [!TIP]
> Рекомендуется запускать и завершать запись с помощью принудительной сборки мусора.  Нажмите кнопку **собирать** мусорную сборку ![ мусора ][ImageForceGarbageCollectionIcon] при записи для принудительного сбора мусора.  

Чтобы продемонстрировать записи в памяти, Взгляните на приведенный ниже код.  

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

Каждый раз, когда была нажата кнопка, на которую ссылается код, 10000 `div` узлы добавляются в тело документа, а в `x` массив помещается строка из 1 000 000 символов `x` .  Выполнение этого кода приводит к записи на панели **производительности** , например [на рис. 3](#figure-3).  

> ##### Рисунок3  
> Простой рост  
> ![Простой рост][ImageSimpleGrowth]  

Прежде всего, объясните пользовательский интерфейс.  Граф **кучи** в области **обзора** \ (ниже **net**\) представляет кучу JS.  Под областью **обзора** находится панель **счетчиков** .  Здесь вы можете видеть использование памяти, разбитое на "JS-файлы" \ (то же, что и граф **кучи** в области **обзора** \), документы, узлы DOM, прослушиватели и память GPU.  Отключение CheckBox скрывает его на диаграмме.  

Теперь анализ кода по сравнению с [рисунком 3](#figure-3).  Если посмотреть на счетчик Nodes \ (зеленая диаграмма \), вы сможете убедиться, что он правильно соответствует коду.  Количество узлов увеличивается на отдельных этапах.  Возможно, вы предполагаете, что каждый рост количества узлов является вызовом `grow()` .  Диаграмма кучи JS \ (синяя диаграмма \) не так проста.  В соответствии с лучшими рекомендациями, первый DIP — это принудительная сборка мусора (достигается нажатием **collect garbage** ![ кнопки "собрать мусор" для сборки мусора ][ImageForceGarbageCollectionIcon] ).  По мере выполнения записи вы можете видеть, что пики размера кучи JS.  Это является естественным и ожидаемым: код JavaScript создает узлы DOM при каждом нажатии кнопки и выполняет большое количество действий при создании строки из 1 000 000 знаков.  Ключевое описание — тот факт, что куча JS завершается быстрее, чем начало, ("начало" — это точка после принудительной сборки мусора).  В реальном мире, если вы увидели этот шаблон размера кучи JS или размера узла, возможно, он может определять утечку памяти.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Обнаружение утечек памяти отключенного дерева DOM с помощью снимков кучи  

Узел DOM обстается сборщиком мусора только в том случае, если на странице нет ссылок на узел либо из дерева DOM, либо из кода JavaScript.  Узел считается отсоединенным, когда он удаляется из дерева DOM, но некоторые сценарии JavaScript по-прежнему ссылаются на него.  Отсоединенные узлы DOM являются распространенной причиной утечек памяти.  В этом разделе рассказывается о том, как использовать профилировщики кучи в DevTools для определения отделенных узлов.  

Вот простой пример отсоединенных узлов DOM.  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

При нажатии на кнопку, на которую ссылается код, создается `ul` узел с десятью `li` потомками.  На эти узлы ссылается код, но они не существуют в дереве DOM, поэтому каждый из них отсоединен.  

Моментальные снимки кучи — это один из способов идентифицировать отсоединенные узлы.  Как показано в названии, в снимках кучи показано, как распределяются память между объектами JS и сайтами DOM на странице в момент создания снимка.  

Чтобы создать снимок, откройте DevTools и перейдите на панель **память** , установите переключатель в положение " **снимок кучи** ", а затем нажмите кнопку " **сделать снимок** ".  

> ##### Рисунок4  
> Создание снимка кучи  
> ![Создание снимка кучи][ImageTakeHeapSnapshot]  

Для обработки и загрузки снимков может потребоваться некоторое время.  После завершения работы выберите ее в левой панели \ (снимки с именами из **кучи**).  

Введите текст `Detached` в поле " **Фильтр класса** " для поиска отсоединенных деревьев DOM.  

> ##### Рисунок 5  
> Фильтрация для отсоединенных узлов  
> ![Фильтрация для отсоединенных узлов][ImageFilteringForDetachedNodes]  

Разверните CARATS, чтобы разобраться в отсоединенном дереве.  

> ##### Рисунок6  
> Исследование отключенного дерева  
> ![Исследование отключенного дерева][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Щелкните узел, чтобы изучить его еще больше.  В области **объектов** вы можете просмотреть дополнительные сведения о коде, который ссылается на него.  Например, на [рис. 7](#figure-7) вы видите, что `detachedNodes` переменная ссылается на узел.  Чтобы устранить эту проблему, необходимо изучить код, использующий `detachedUNode` переменную, и убедиться, что ссылка на узел удаляется, когда он больше не нужен.

> ##### Рисунок7  
> Исследование узла  
> ![Исследование узла][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Определение утечек памяти кучи JS с инструментированием выделения на временной шкале  

**Инструментирование выделения на временной шкале** — это еще один инструмент, который может помочь вам отслеживать утечки памяти в куче JS.  

На временной шкале с помощью следующего кода показано **Инструментирование выделения ресурсов** .  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

При каждом нажатии кнопки, на которую ссылается код, в массив добавляется строка из 1 000 000 символов `x` .  

Чтобы записать Инструментарий выделения на временную шкалу, откройте DevTools, перейдите на панель **память** , выберите переключатель **Инструментирование на временной шкале** , нажмите кнопку **Пуск** , выполните действие, которое вы считаете причиной возникновения утечек памяти, и нажмите кнопку Остановить запись **профиля кучи** , ![ ][ImageStopRecordingIcon] когда закончите.  

Когда вы записываете элементы, обратите внимание на то, что синие полосы отображаются на инструментальных инструментах выделения на временной шкале, как показано на [рисунке 8](#figure-8).  

> ##### Рисунок8  
> Новые распределения  
> ![Новые распределения][ImageNewAllocations]  

Эти синие отрезки представляют новые выделения памяти.  Новые выделения памяти являются кандидатами на утечку памяти.  Вы можете изменить масштаб на панели, чтобы отфильтровать область **конструктора** , чтобы отображались только те объекты, которые были выделены в течение указанного периода времени.  

> ##### Рисунок9  
> Уменьшенная временная шкала выделения  
> ![Уменьшенная временная шкала выделения][ImageZoomedAllocationTimeline]  

Разверните объект и щелкните значение, чтобы просмотреть дополнительные сведения в области **объектов** .  Например, на [рис. 10](#figure-10), просмотрев сведения о новом выделенном объекте, вы сможете увидеть, что он был выделен для `x` переменной в `Window` области.  

> ##### Рисунок 10 
> Сведения об объекте  
> ![Сведения об объекте][ImageObjectDetail]  

## Изучение выделения памяти по функциям   

Используйте тип профилирования **выборки выделения** для просмотра выделения памяти функцией JavaScript.  

> ##### Рисунок11  
> Выборка распределения записей  
> ![Выборка распределения записей][ImageRecordAllocationSampling]  

1.  Установите переключатель **выборка распределения** .  Если на странице есть рабочий процесс, вы можете выбрать его в качестве целевого объекта профилирования с помощью раскрывающегося меню рядом с кнопкой " **Пуск** ".  
1.  Нажмите кнопку " **Пуск** ".  
1.  Выполните действия, которые нужно изучить на странице.  
1.  После завершения всех действий нажмите кнопку " **остановить** ".  

DevTools показывает разделение выделения памяти по функциям.  Представление по умолчанию является **большим (снизу вверх)**, в котором отображаются функции, которые выделили наибольшую область памяти сверху.  

> ##### Рисунок12  
> Выборка распределения  
>![Выборка распределения][ImageAllocationSampling]  

## Точечные часто используемые сборки мусора  

Если страница часто задерживается, возможно, у вас возникли проблемы с обсбором мусора.  

Вы можете использовать либо Диспетчер задач браузера Microsoft EDGE, либо записи памяти для выявления частых сборок мусора.  В диспетчере задач браузера Microsoft Edge часто растет и падает **память** , а также значения **памяти JavaScript** , которые представляют собой частый процесс сборки мусора.  В записях производительности частые изменения (рост и отпадает) на графы JS или счетчики узлов указывают на частную сборку мусора.  

После того как вы обнаружите проблему, вы можете использовать **инструментарий выделения для записи временной шкалы** , чтобы узнать, где выделяется память, и какая функция вызывает распределение.  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Рисунок 1: Открытие диспетчера задач браузера Microsoft Edge"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Рисунок 2: включение памяти JavaScript"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Рисунок 3: простое расширение"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Рисунок 4: создание снимка кучи"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Рисунок 5: Фильтрация отсоединенных узлов"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Рисунок 6: исследование отсоединенных деревьев"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Рисунок 7: исследование узла"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Рисунок 8: новые выделения"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Рисунок 9: уменьшенная временная шкала выделения"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Рисунок 10: сведения об объекте"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Рисунок 11: выборка для выделения записей"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Рисунок 12: Выбор распределения"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Сведения о производительности записи: Справочник по анализу производительности"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
