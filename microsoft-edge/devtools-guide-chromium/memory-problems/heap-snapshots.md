---
description: Узнайте, как записывать снимки с помощью профиля кучи Microsoft Edge DevTools и находить утечки памяти.
title: Запись снимков кучи
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ce7a6f972bed386f96312808428bd74f1241668f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397806"
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
   limitations under the License.  -->

# <a name="how-to-record-heap-snapshots"></a>Запись снимков кучи  

Узнайте, как записывать снимки с помощью профиля кучи Microsoft Edge DevTools и находить утечки памяти.  

Профиль microsoft Edge DevTools показывает распределение памяти по объектам JavaScript и связанным узлам DOM вашей страницы.  С его помощью можно сделать снимки javaScript \(JS heap\) , проанализировать графики памяти, сравнить снимки и найти утечки памяти.  Перейдите к [дереву объектов.][DevtoolsMemoryProblems101ObjectsRetainingTree]  

## <a name="take-a-snapshot"></a>Снимок  

На панели **Памяти** выберите **Снимок,** а затем выберите **Начните**.  Вы также можете `Ctrl` + `E` выбрать \(Windows, Linux\) `Cmd` + `E` или \(macOS\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Выберите тип профилирование" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Выберите тип профилирование  
:::image-end:::  

**Снимки** первоначально хранятся в памяти процесса визуализации.  Снимки передаются в DevTools по запросу при выборе значка снимка для просмотра.  

После загрузки снимка в DevTools и его разбрасыва, появляется номер ниже заголовка снимка и отображается общий размер достигаемых объектов [JavaScript.][DevtoolsMemoryProblems101ObjectSizes]  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Общий размер досяжимых объектов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Общий размер досяжимых объектов  
:::image-end:::  

> [!NOTE]
> В снимки включены только досяжимые объекты.  Кроме того, снимок всегда начинается со сбора мусора.  

## <a name="clear-snapshots"></a>Снимок очистки  

Выберите **значок Clear all profiles** для удаления снимков \(как из DevTools, так и из любой памяти, связанной с процессом рендера\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Удаление снимков" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Удаление снимков  
:::image-end:::  

Закрытие окна DevTools не удаляет профили из памяти, связанной с процессом отрисовки.  При повторном восстановлении DevTools все ранее сделанные снимки вновь появляются в списке снимков.  

> [!NOTE]
> Попробуйте этот пример [рассеянных объектов][GlitchDevtoolsMemoryExample03] и профиль его с помощью профайла кучи.  Отображается несколько распределений элементов \(object\).  

## <a name="view-snapshots"></a>Просмотр снимков  

Просмотр снимков с разных точек зрения для различных задач.  

**Сводное представление** показывает объекты, сгруппив их под именем конструктора.  Используйте его для выслеки объектов \(и использования памяти\) на основе типа, сгруппив по имени конструктора.  Это особенно полезно для **отслеживания утечек DOM**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Представление сравнения**.  Отображает разницу между двумя снимками.  Используйте его для сравнения двух снимков памяти \(или более\) до и после операции.  Проверка дельты в освобожденной памяти и отсчете ссылок позволяет подтвердить наличие и причину утечки памяти.  

**Представление сдерживания**.  Позволяет исследовать содержимое кучи.  **Представление сдерживания** обеспечивает лучшее представление структуры объектов, помогая анализировать объекты, на которые ссылается глобальное пространство имен \(window\) для поиска того, что содержит объекты вокруг.  Используйте его для анализа замыкания и погружения в объекты на низком уровне.  

Чтобы переключаться между представлениями, используйте селектор в верхней части представления.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Селектор переключатель представлений" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Селектор переключатель представлений  
:::image-end:::  

> [!NOTE]
> Не все свойства хранятся на кучи JavaScript.  Свойства, реализованные с помощью геттеров, использующих исходный код, не захватываются.  Кроме того, неконструкционные значения, такие как числа, не захватываются.  

### <a name="summary-view"></a>Представление сводки  

Сначала снимок открывается в представлении Сводка, отображая итоговые объекты, которые могут быть расширены, чтобы показать экземпляры:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Представление сводки" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Представление сводки**  
:::image-end:::  

Записи верхнего уровня — это "общие" строки.  

| Записи верхнего уровня | Описание |  
|:--- |:--- |  
| **Конструктор** | Представляет все объекты, созданные с помощью этого конструктора.  |  
| **Расстояние** | отображает расстояние до корневого с помощью самого короткого простого пути узлов.  |  
| **Неглубокий размер** | Отображает сумму мелких размеров всех объектов, созданных определенной функцией конструктора.  Небольшой размер — это размер памяти, удерживаемой объектом \(как правило, массивы и строки имеют более крупные неглубокие размеры\).  Перейдите [к размерам объекта.][DevtoolsMemoryProblems101ObjectSizes]  |  
| **Сохраненный размер** | Отображает максимальный сохраненный размер одного и того же набора объектов.  Размер памяти, который вы можете освободить после удаления объекта \((а иждивенцы больше не достигаются\) называется сохраненным размером.  Перейдите [к размерам объекта.][DevtoolsMemoryProblems101ObjectSizes]  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

После расширения общей строки в верхнем представлении отображаются все экземпляры.  В каждом экземпляре в соответствующих столбцах отображаются неглубокие и сохраненные размеры.  Номер после `@` символа — уникальный ID объекта, позволяющий сравнивать снимки кучи на основе объекта.  

Помните, что желтые объекты имеют ссылки на JavaScript, а красные — это отдельные узлы, которые ссылаются на один с желтым фоном.  

**Что соответствуют различным записям конструктора \(group\) в профиле Куча?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Группы конструкторов" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Группы конструкторов**  
:::image-end:::  

| Запись Конструктор \(group\) | Описание |  
|:--- |:--- |  
| **\(глобальное свойство\)** | Промежуточные объекты между глобальным объектом \(like \) и `window` объектом, на который он ссылается.  Если объект создается с помощью конструктора и удерживается глобальным объектом, путь сохранения может быть `Person` представлен как `[global] > \(global property\) > Person` .  Это контрастирует с нормой, когда объекты напрямую ссылались друг на друга.  Промежуточные объекты существуют по причинам производительности.  Глобальные объекты регулярно меняются, а оптимизация доступа к свойствам хорошо действует для объектов, не влияемых на глобальные объекты.  |  
| **\(roots\)** | Корневые записи в представлении сохраняемой елки — это объекты, которые имеют ссылки на выбранный объект.  Записи также могут быть ссылками, созданными двигателем для определенных целей.  У двигателя есть кэши, которые являются эталонными объектами, но все эти ссылки являются слабыми и не препятствуют сбору объекта, учитывая отсутствие действительно сильных ссылок.  |  
| **\(closure\)** | Количество ссылок на группу объектов с помощью закрытия функций.  |  
| **\(массив, строка, номер, regexp\)** | Список типов объектов со свойствами, которые ссылались на массив, строку, номер или регулярное выражение.  |  
| **\(компилировать код\)** | Все, что связано с скомпиловым кодом.  Скрипт похож на функцию, но соответствует `<script>` телу.  SharedFunctionInfos \(SFI\) — это объекты, стоящие между функциями и компилировать код.  Функции обычно имеют контекст, а SFIs - нет.  |  
| **HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment**и так далее.  | Ссылки на элементы или объекты документов определенного типа, на которые ссылается код.  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a>Представление сравнения  

Найдите объекты с утечкой, сравнивая несколько снимков друг с другом.  Чтобы убедиться, что определенная операция приложения не создает утечек \(например, обычно пара прямых и обратных операций, таких как открытие документа, а затем его закрытие, не должно оставлять мусора\), вы можете следовать ниже сценарию:  

1.  Снимок кучи перед выполнением операции.  
1.  Выполните операцию \(взаимодействовать со страницей в некотором смысле, что вы считаете причиной утечки\).  
1.  Выполните обратную операцию \(выполните противоположное взаимодействие и повторите ее несколько раз\).  
1.  Снимок второй кучи и измените представление этого снимка на **Сравнение,** сравнивая его со **снимком 1**.  
    
В **представлении Сравнение** отображается разница между двумя снимками.  При расширении общей записи показаны экземпляры добавленных и удаленных объектов.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Представление сравнения" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Представление сравнения**  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a>Представление сдерживания  

Представление **Containment** — это, по сути, "вид с высоты птичьего полета" структуры объектов приложения.  Это позволяет заглянуть внутрь замыкания функций, наблюдать внутренние объекты виртуальной машины \(VM\), которые вместе составляют объекты JavaScript, и понимать, сколько памяти ваше приложение использует на очень низком уровне.  

| Точки входа представления сдерживания | Описание |  
|:--- |:--- |  
| **Объекты DOMWindow** | Глобальные объекты для кода JavaScript.  |  
| **Корни GC** | Фактические корневишки GC, используемые мусором VM.  Корни GC состоят из встроенных карт объектов, таблиц символов, стеков потоков VM, кэшей компиляции, областей обработки и глобальных ручейков.  |  
| **Объекты native** | Объекты браузера "толкнули" внутри виртуальной машины JavaScript \(JavaScript VM\), чтобы разрешить автоматизацию, например, узлы DOM, правила CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Представление сдерживания" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Представление сдерживания**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Подсказка о закрытии.  Назови функции, чтобы можно было легко различать закрытия на снимке.  Например, в этом примере не используются именуемые функции.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> В фрагменте следующего кода используются именные функции.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Попробуйте в этом [примере, почему `eval` зло,][GlitchDevtoolsMemoryExample07] чтобы проанализировать влияние замыкания на память.  Вы также можете быть заинтересованы в следующем его с этим примером, который принимает вас через запись [кучи выделения][GlitchDevtoolsMemoryExample08].  
> 

## <a name="look-up-color-coding"></a>Искать цветовое кодирование  

Свойства и значения свойств объектов имеют различные типы и соответственно цветные.  Каждое свойство имеет один из четырех типов.  

| Тип свойства | Описание |  
|:--- |:--- |  
| **a: свойство** | Обычное свойство с именем, к нему можно получить доступ через оператора \(dot\) или с помощью `.` `[` `]` нотации \(кронштейны\) например `["foo bar"]` .  |  
| **0: элемент** | Обычное свойство с числительным индексом, доступ к нему осуществляется с помощью `[` `]` нотации \(кронштейны\).  |  
| **a: context var** |  Переменная в контексте функции, доступная по имени переменной изнутри закрытия функции.  |  
| **a: системная опора** | Свойство, добавленное VM JavaScript, не доступное из кода JavaScript.  |  

Объекты, назначенные `System` как не имеют соответствующего типа JavaScript.  Каждый из них является частью реализации объектной системы VM Javascript.  V8 выделяет большинство внутренних объектов в той же куче, что и объекты JS пользователя.  Это всего лишь внутренние органы V8.  

## <a name="find-a-specific-object"></a>Поиск определенного объекта  

Чтобы найти объект в собранной куче, можно поискать с помощью и `Ctrl` + `F` предоставить ID объекта.  

## <a name="uncover-dom-leaks"></a>Раскрытие утечек DOM  

Профайлатор кучи имеет возможность отражать бидырекционные зависимости между родными объектами браузера \(узлы DOM, правила CSS\) и объектами JavaScript.
Это помогает обнаружить невидимые утечки, происходящие из-за забытых отсоединяющихся подтрибов DOM, плавающих вокруг.  

Утечки DOM могут быть больше, чем вы думаете.  Рассмотрим следующий пример.  Когда #tree GC?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

Поддерживает ссылку на соответствующий родитель `#leaf` \(parentNode\) и recursively до , поэтому только когда leafRef является nullified является целое дерево под кандидатом `#tree` `#tree` для GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subtrees DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Subtrees DOM  
:::image-end:::  

> [!NOTE]
> Примеры. Попробуйте пример утечки [узла DOM,][GlitchDevtoolsMemoryExample06] чтобы понять, где он может протекать и как его обнаружить.  Вы также можете посмотреть на этот пример [утечки DOM больше, чем ожидалось][GlitchDevtoolsMemoryExample09].  

Дополнительные новости об утечках doM и основах анализа памяти при поиске и отладке утечек памяти с помощью [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] от Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Размеры объектов — терминология памяти | Документы Майкрософт"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Объекты сохранения дерева — терминология памяти | Документы Майкрософт"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html — Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html — Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "память | Слайды"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) и является автором [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
