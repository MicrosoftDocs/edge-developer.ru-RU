---
description: Пользователи ожидают интерактивные и плавные страницы.  Каждая стадия в пиксельном конвейере представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность во время выполнения.
title: Анализ производительности в времени выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d42ac5e7a7456971d48198a1f362eebe7156bbce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230609"
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

# Анализ производительности в времени выполнения 

Пользователи ожидают интерактивные и плавные страницы.  Каждая стадия в пиксельном конвейере представляет возможность ввести jank.  Узнайте о средствах и стратегиях для выявления и устранения распространенных проблем, которые замедляют производительность во время выполнения.  

### Сводка  

*   Не пишите JavaScript, который заставляет браузер пересчитывать макет.  Разделяйте функции чтения и записи, а затем выполните чтение.  
*   Не усложняйте CSS.  Используйте меньше CSS и сохраняйте простоты селекторов CSS.  
*   Избегайте максимально возможного макета.  Выберите CSS,который вообще не активирует макет.  
*   Рисование может занять больше времени, чем любое другое действие отрисовки.  Следите за узкими местами для кисок.  
    
## JavaScript  

Вычисления JavaScript, особенно те, которые вызывают существенные визуальные изменения, могут привести к застою производительности приложения.  Не мешайте взаимодействию с пользователем с помощью JavaScript во время неудалась или длительной работы.  

### JavaScript: средства  

Сформуйте запись на панели **"Производительность"** и наймите подозрительные длинные `Evaluate Script` события.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

F вы знаете, что в JavaScript достаточно много jank, возможно, вам потребуется оказаться на следующем уровне анализа и собрать профиль ЦП JavaScript.  Профили ЦП показывают, где время работы затрачено на функции страницы.  Узнайте, как создавать профили ЦП в [среде запуска JavaScript.][DevtoolsRenderingToolsJavascriptRuntime]

### JavaScript: проблемы  

В следующей таблице описываются некоторые распространенные проблемы JavaScript и возможные решения:  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Дорогостоящие обработчики ввода, влияющие на отклик или анимацию.  | Касание, параллакс прокрутка.  | Разрешите браузеру обрабатывать касание и прокрутку или привязывать прослушиватель как можно позднее.  См. контрольный список производительности во время выполнения пользователя PaulСвойла (PaulСвойл) с дорогими [обработчиками входных данных.][WebPerformanceCalendarRuntimeChecklist]  |  
| JavaScript с плохой временем, влияющий на отклик, анимацию, загрузку.  | Пользователь прокручивает страницу сразу после загрузки, setTimeout / setInterval.  | Оптимизация времени работы JavaScript: `requestAnimationFrame` использование, распространение манипуляций DOM по кадрам, использование [веб-работников.][MDNUsingWebWorkers]  |  
| Долгосрочный JavaScript, влияющий на отклик.  | Событие [DOMContentLoaded][MDNUsingWebWorkers] заглохает, так как оно совмещается с работой JS.  | Перемещайте чисто вычислительные трудоемкие работы [в веб-работники.][MDNUsingWebWorkers]  Если вам нужен доступ к DOM, используйте `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Сценарии сборки мусора, влияющие на отклик или анимацию.  | Сборка мусора может происходить где угодно.  | Напишите меньше скриптов сборки мусора.  См. контрольный список производительности сборки мусора в анимации в списке производительности [во время выполнения полю ПолОмА ( PaulСвой).][WebPerformanceCalendarRuntimeChecklist]  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Стиль  

Изменение стиля является дорогостоящим, особенно если эти изменения влияют на несколько элементов в DOM.  Каждый раз, когда вы применяли стили к элементу, браузер вычисляет влияние на все связанные элементы, пересчитывает макет и перерасчеты.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Стиль: средства  

Запись на панели **"Производительность".**  Проверьте запись на большие `Recalculate Style` события \(отображаются в сиреневом цвете\).  

<!--todo: add Recording section when available  -->  

Щелкните `Recalculate Style` событие, чтобы **** просмотреть дополнительные сведения о нем в области сведений.  Если изменение стиля забирает много времени, это будет множать производительность.  Если вычисления стиля влияют на большое количество элементов, это еще одна область с местом для улучшения.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Длинный стиль пересчета" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Длинный стиль пересчета  
:::image-end:::  

Чтобы уменьшить влияние `Recalculate Style` событий:  

*   Используйте [триггеры CSS,][CssTriggers] чтобы узнать, какие свойства CSS активирует макет, paint и составные.  Эти свойства оказывают наихудшее влияние на производительность отрисовки.  
*   Переключиться на свойства, которые имеют меньшее влияние.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Стиль: проблемы  

В следующей таблице описаны некоторые распространенные проблемы со стилем и возможные решения:  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Затратные вычисления стиля, влияющие на отклик или анимацию.  | Любое свойство CSS, которое изменяет геометрию элемента, например ширину, высоту или положение; Браузер проверяет все остальные элементы и пересчитает макет.  | Избегайте CSS- инициирует макеты |  
| Сложные селекторы, влияющие на отклик или анимацию.  | Вложенные селекторы принудительно должны знать браузер обо всех остальных элементах, включая родителей и детей.  | Ссылаться на элемент в CSS можно только с помощью класса.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Макет  

Макет (или перенабор в Firefox) — это процесс, с помощью которого браузер вычисляет положение и размеры всех элементов на странице.  Модель макета в Интернете означает, что один элемент может повлиять на других; например, ширина элемента обычно влияет на ширину любых потомков и так далее, в любом случае вверх и `<body>` вниз по дереву.  Этот процесс может быть довольно сложной для браузера.  

Как правило, если вы запросите геометрическое значение из DOM до завершения фрейма, вы найдете "принудительно синхронные макеты", что может быть большим узким местом производительности, если он повторяется часто или выполняется для большого дерева DOM.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Макет: средства  

В **области** "Производительность" указывается, когда страница вызывает принудительные синхронные макеты.  Эти `Layout` события помечаются красными полосами.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Принудительный синхронный макет" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Принудительный синхронный макет  
:::image-end:::  

"Раскладка макета" — это повторение принудительно синхронных условий макета.  Это происходит, когда JavaScript несколько раз записывает и считывает из DOM, что заставляет браузер пересчитать макет снова и снова.  Чтобы определить разметку макета, найди шаблон нескольких принудительных предупреждений о синхронном макете.  См. предыдущий рисунок.  

### Макет: проблемы  

В следующей таблице описываются некоторые распространенные проблемы с макетом и возможные решения:  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Принудительный синхронный макет, влияющий на отклик или анимацию.  | Принудительным выполнением макета браузером ранее в пиксельном конвейере, что приводит к повторяемой процедуре отрисовки.  | Сначала пакетное чтение в стиле, а затем любые записи.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Thrashing макета, влияющий на отклик или анимацию.  | Цикл, который помещает браузер в цикл чтения-записи и чтения-записи, заставляет браузер пересчитывать макет снова и снова.  | Автоматически пакетные операции чтения и записи с помощью [библиотеки FastDom.][GitHubWilsonpageFastdom]  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Paint и composite  

Paint — это процесс заполнения пикселей.  Зачастую это наиболее затратная часть процесса отрисовки.  Если вы заметили, что страница в любом случае неуявная, скорее всего, у вас возникнут проблемы с киской.  

Композитные части страницы помещаются вместе для отображения на экране.  В большинстве случае, если вы не хотите использовать свойства только компонатора и не хотите использовать кисть, производительность должна существенно улучшиться, но следует избегать чрезмерного количества уровней.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Paint и composite: Tools  

Хотите узнать, сколько времени занимает рисование или как часто происходит рисование?  Проверьте параметр ["Включить расширенный инструментарий paint"][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] на панели **"Производительность",** а затем с помощью записи.  Если большая часть времени отрисовки потрачена на рисование, возникают проблемы с рисованием.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Paint и composite: проблемы  

В следующей таблице описываются некоторые распространенные проблемы с paint и составными решениями, а также возможные решения:  

| Проблема | Пример. | Решение |  
|:--- |:--- |:--- |  
| Нарисуются ливня, влияющие на отклик или анимацию.  | Большие области киок или дорогостоящие кинты, влияющие на отклик или анимацию.  | Избегайте использования кисти, рекламы элементов, которые перемещаются на собственный уровень, используйте преобразования и прозрачность.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Уровни, влияющие на анимации.  | Чрезмерное количество элементов с большим `translateZ(0)` влиянием на производительность анимации.  | Повышение до уровней экономно и только в том случае, если вы знаете, что он предлагает существенные улучшения.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Ускорение времени работы JavaScript | Документы Майкрософт"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Включить расширенный инструментарий paint — справочник по анализу производительности | Документы Майкрософт"

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

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-работников | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Контрольный список производительности в времени выполнения — календарь производительности веб-сайтов"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) и [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
