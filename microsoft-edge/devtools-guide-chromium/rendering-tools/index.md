---
description: Пользователи ожидают интерактивные и гладкие страницы.  Каждый этап конвейера пикселей представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность выполнения.
title: Анализ производительности выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 646db5b2e88e33b109e5eb3ae01a296bf3a4fb46
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398002"
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
   limitations under the License.  -->

# <a name="analyze-runtime-performance"></a>Анализ производительности выполнения  

Пользователи ожидают интерактивные и гладкие страницы.  Каждый этап конвейера пикселей представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность выполнения.  

### <a name="summary"></a>Сводка  

*   Не пишите JavaScript, который заставляет браузер пересчитывать макет.  Разделяйте функции чтения и записи и выполните сначала чтение.  
*   Не усложняйте работу CSS.  Используйте меньше CSS и сохраняйте простые селекторы CSS.  
*   Избегайте макета как можно больше.  Выберите CSS, который вообще не запускает макет.  
*   Рисование может занять больше времени, чем любая другая отрисовка.  Следите за узкими местами для краски.  
    
## <a name="javascript"></a>JavaScript  

Вычисления JavaScript, особенно те, которые вызывают обширные визуальные изменения, могут привести к срыву производительности приложений.  Не позволяйте вовремя или длительному JavaScript вмешиваться в взаимодействие пользователей.  

### <a name="javascript-tools"></a>JavaScript: средства  

Сними запись в **средстве Performance** и найми подозрительно длинные `Evaluate Script` события.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

f. Вы заметь довольно много jank в JavaScript, возможно, потребуется взять анализ на следующий уровень и собрать профиль ЦП JavaScript.  Профили ЦП показывают, где время работы тратится в функциях страницы.  Узнайте, как создавать профили ЦП в [режиме ускорения запуска JavaScript.][DevtoolsRenderingToolsJavascriptRuntime]

### <a name="javascript-problems"></a>JavaScript: проблемы  

В следующей таблице описаны некоторые распространенные проблемы JavaScript и возможные решения.  

| Проблема | Пример | Решение |  
|:--- |:--- |:--- |  
| Дорогие обработчики ввода, влияющие на отклик или анимацию.  | Сенсорный, параллакс прокрутки.  | Позвольте браузеру обрабатывать сенсорные и прокрутки или связывать слушателя как можно позже.  Перейдите [к дорогим обработчикам ввода в][WebPerformanceCalendarRuntimeChecklist]контрольном списке производительности выполнения ПолОм Льюисом .  |  
| Плохо приурочная javaScript влияет на отклик, анимацию, загрузку.  | Пользователь прокручивает сразу после загрузки страницы setTimeout/setInterval.  | Оптимизация времени работы JavaScript: `requestAnimationFrame` использование, распространение манипуляций с DOM по кадрам, использование [веб-рабочих][MDNUsingWebWorkers].  |  
| Долгосрочный JavaScript, влияющий на отклик.  | Событие [DOMContentLoaded][MDNUsingWebWorkers] приостановилось, так как оно завалено работой JS.  | Перемещение чистой вычислительной работы на [веб-рабочих][MDNUsingWebWorkers].  Если вам нужен доступ к DOM, используйте `requestAnimationFrame` .  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Сценарии garbage-y, влияющие на отклик или анимацию.  | Сбор мусора может происходить в любом месте.  | Записывая меньше сценариев с мусором.  Перейдите к разделу Сбор мусора в анимации в контрольном списке производительности во время выполнения [Полом Льюисом.][WebPerformanceCalendarRuntimeChecklist]  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a>Стиль  

Изменения стиля являются дорогостоящими, особенно если эти изменения затрагивают несколько элементов в DOM.  Каждый раз, когда к элементу применяются стили, браузер высчитывает влияние на все связанные элементы, пересчитывает макет и перекетирует.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a>Стиль: средства  

Запись в средстве **Performance.**  Проверьте запись для больших `Recalculate Style` событий \(отображается в фиолетовом\).  

<!--todo: add Recording section when available  -->  

Выберите `Recalculate Style` событие, чтобы просмотреть дополнительные сведения о нем в области **Details.**  Если изменения стиля забирают длительное время, это является хитом производительности.  Если вычисления стилей влияют на большое количество элементов, это еще одна область, где есть возможности для улучшения.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Длинный стиль пересчета  
:::image-end:::  

Чтобы уменьшить влияние `Recalculate Style` событий:  

*   Используйте [триггеры CSS,][CssTriggers] чтобы узнать, какие свойства CSS вызывают макет, краску и композит.  Эти свойства оказывают самое сильное влияние на производительность отрисовки.  
*   Переключиться на свойства, которые имеют меньшее влияние.  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a>Стиль: проблемы  

В следующей таблице описаны некоторые распространенные проблемы стиля и возможные решения.  

| Проблема | Пример | Решение |  
|:--- |:--- |:--- |  
| Дорогостоящие вычисления стилей, влияющие на отклик или анимацию.  | Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или положение; браузер проверяет все остальные элементы и пересчитывает макет.  | Избегайте CSS, который запускает макеты |  
| Сложные селекторы, влияющие на отклик или анимацию.  | Вложенные селекторы заставляют браузер знать все обо всех остальных элементах, включая родителей и детей.  | Ссылка на элемент в CSS только с классом.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a>Макет  

Макет (или переток в Firefox) — это процесс, при котором браузер вычисляет позиции и размеры всех элементов на странице.  Модель макета веб-сайта означает, что один элемент может влиять на другие; например, ширина элемента, как правило, влияет на ширину любых детских элементов и так далее на всем протяжении `<body>` дерева.  Этот процесс может быть достаточно вовлечен для браузера.  

Как правило, если вы попросите вернуть геометрическое значение из DOM до завершения кадра, вы найдете "принудительно синхронные макеты", что может быть большим узким местом производительности, если часто повторяться или выполняться для большого дерева DOM.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a>Макет: средства  

В **области Performance** определяется, когда страница вызывает принудительное синхронное расположение.  Эти `Layout` события отмечены красными полосами.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Принудительное синхронное расположение" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Принудительное синхронное расположение  
:::image-end:::  

"Обмывка макета" — это повторение условий принудительного синхронного макета.  Это происходит, когда JavaScript пишет и читает из DOM несколько раз, что заставляет браузер пересчитать макет снова и снова.  Чтобы определить обмыв макета, найди шаблон нескольких принудительных синхронных предупреждений макета.  Просмотрите предыдущую фигуру.  

### <a name="layout-problems"></a>Макет: проблемы  

В следующей таблице описаны некоторые распространенные проблемы макета и возможные решения.  

| Проблема | Пример | Решение |  
|:--- |:--- |:--- |  
| Принудительный синхронный макет, влияющий на отклик или анимацию.  | Принуждение браузера к выполнению макета ранее в конвейере пикселей, что приводит к повторяемой процедуре отрисовки.  | Пакет вашего стиля сначала читается, а затем записывает все записи.  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Обмыв макета, влияющий на реакцию или анимацию.  | Цикл, который помещает браузер в цикл чтения и чтения, заставляя браузер пересчитывать макет снова и снова.  | Автоматически пакетные операции чтения с помощью [библиотеки FastDom.][GitHubWilsonpageFastdom]  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a>Краска и композит  

Paint — это процесс заполнения пикселей.  Зачастую это самая затратная часть процесса отрисовки.  Если вы заметили, что ваша страница не работает так, как задумано, вполне вероятно, что у вас есть проблемы с краской.  

Композитизация — это то, где расписные части страницы сложены для отображения на экране.  По большей части, если придерживаться свойств только для композитора и вообще избегать краски, следует заметить значительное улучшение производительности, но необходимо следить за чрезмерными количествами уровней.  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a>Краска и композитные: средства  

Хотите узнать, сколько времени занимает рисование и как часто происходит рисование?  Проверьте параметр [Включить расширенный инструментарий для краски][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] в панели **Performance,** а затем сдайте запись.  Если большая часть времени отрисовки отработана, возникают проблемы с краской.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a>Краска и композитные: проблемы  

В следующей таблице описаны некоторые распространенные проблемы с краской и композитными решениями.  

| Проблема | Пример | Решение |  
|:--- |:--- |:--- |  
| Краска штормов, влияющих на отклик или анимацию.  | Большие области краски или дорогие краски, влияющие на отклик или анимацию.  | Избегайте краски, продвигая элементы, которые перемещаются в собственный слой, используйте преобразования и непрозрачность.  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Уровни взрывов, влияющих на анимации.  | Перепроизводства слишком многих элементов с `translateZ(0)` большим влиянием на производительность анимации.  | Продвигать в слои экономно, и только тогда, когда вы знаете, он предлагает ощутимые улучшения.  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение времени работы JavaScript | Документы Майкрософт"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Включаем расширенный инструментарий краски - справочные ссылки на анализ производительности | Документы Майкрософт"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Триггеры CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-| MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности выполнения — веб-календарь производительности"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
