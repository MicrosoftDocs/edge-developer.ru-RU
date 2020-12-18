---
description: Использование панели "Производительность" для анализа отзывчивости страницы во время взаимодействия с пользователем
title: DevTools — производительность
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, производительность, профиль, частота кадров, кадр/с, использование ЦП, выполнение JavaScript
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 561cfe62f7db492ce3914b4daba8ccf8c0a62a8a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235247"
---
# <span data-ttu-id="5ca33-104">Производительность</span><span class="sxs-lookup"><span data-stu-id="5ca33-104">Performance</span></span>

<span data-ttu-id="5ca33-105">Панель **производительности** предлагает инструменты для профилирование и анализа отклика пользовательского интерфейса во время взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ca33-105">The **Performance** panel offers tools for profiling and analyzing the responsiveness of your UI during the course of user interaction.</span></span> <span data-ttu-id="5ca33-106">С его помощью вы можете:</span><span class="sxs-lookup"><span data-stu-id="5ca33-106">With it, you can:</span></span>

 - <span data-ttu-id="5ca33-107">[Измерение времени выполнения](#recording-a-profile) различных компонентов страницы</span><span class="sxs-lookup"><span data-stu-id="5ca33-107">[Measure execution times](#recording-a-profile) of the various components of your page</span></span> 
 - <span data-ttu-id="5ca33-108">[Подробнее о том, где](#timeline-ruler) вы проводите больше всего циклов ЦП для запуска страницы и итоговых визуальных эффектов для пользователей</span><span class="sxs-lookup"><span data-stu-id="5ca33-108">[Drill down to where you're spending the most CPU cycles](#timeline-ruler) to run your page and the resulting visual effect for your users</span></span>
 - <span data-ttu-id="5ca33-109">[Пошаговая разбивка процессов,](#timeline-details) потребляющих время выполнения страницы</span><span class="sxs-lookup"><span data-stu-id="5ca33-109">[Get a step-by-step breakdown of the processes](#timeline-details) consuming page execution time</span></span> 
 - <span data-ttu-id="5ca33-110">[Почитайте стеки вызовов JavaScript,](#javascript-call-stacks) чтобы определить дорогостоящие операции, например операции, требующие пересчета макета</span><span class="sxs-lookup"><span data-stu-id="5ca33-110">[Walk your JavaScript call stacks](#javascript-call-stacks) to identify costly operations, such as those requiring layout recalculations</span></span> 

![Панель "Производительность DevTools"](./media/performance.png)

## <span data-ttu-id="5ca33-112">Запись профиля</span><span class="sxs-lookup"><span data-stu-id="5ca33-112">Recording a profile</span></span>

<span data-ttu-id="5ca33-113">Первым этапом анализа производительности страницы является захват профиля при выполнении определенного пользовательского сценария, например этапы повторного анализа ошибки производительности, которые вы пытаетесь исправить, или типичный вариант использования, который вы хотите оптимизировать для улучшения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5ca33-113">The first step to analyzing the performance of your page is to capture a profile as you perform a particular user scenario, such as the repro steps of a performance bug you're trying to fix, or a typical use case you want to optimize for a better user experience.</span></span> 

### <span data-ttu-id="5ca33-114">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="5ca33-114">Toolbar</span></span>

<span data-ttu-id="5ca33-115">Используйте кнопки **остановки**запуска на панели инструментов (или) для запуска и завершения  /  \*\*\*\* `Ctrl+E` трассировки производительности.</span><span class="sxs-lookup"><span data-stu-id="5ca33-115">Use the **Start** / **Stop** buttons on the toolbar (or `Ctrl+E`) to initiate and conclude your performance trace.</span></span> <span data-ttu-id="5ca33-116">На вкладке "Производительность" \*\*\*\* на вкладке "Производительность" будет показан зеленый индикатор, который указывает, что запись идет.</span><span class="sxs-lookup"><span data-stu-id="5ca33-116">A green indicator will apear on the **Performance** tab to indicate a recording is in progress.</span></span> 

![Панель инструментов панели производительности](./media/performance_toolbar.png)

<span data-ttu-id="5ca33-118">После остановки профиля создается отчет о производительности.</span><span class="sxs-lookup"><span data-stu-id="5ca33-118">A performance report will generate upon stopping the profile.</span></span> <span data-ttu-id="5ca33-119">Вы можете сохранить его на диск () и `Ctrl+S` перезагрузить `Ctrl+O` () в DevTools позже.</span><span class="sxs-lookup"><span data-stu-id="5ca33-119">You can choose to save it to disk (`Ctrl+S`) and reload (`Ctrl+O`) in  DevTools at a later time.</span></span>  <span data-ttu-id="5ca33-120">Сеансы диагностики DevTools сохраняются с *расширением .diagsession.*</span><span class="sxs-lookup"><span data-stu-id="5ca33-120">DevTools diagnostic sessions are saved with the *.diagsession* extension.</span></span>

<span data-ttu-id="5ca33-121">Вот что нужно помнить при записи профиля:</span><span class="sxs-lookup"><span data-stu-id="5ca33-121">Here are some things to keep in mind when recording a profile:</span></span>

- <span data-ttu-id="5ca33-122">Выполните меньше всего действий, необходимых для захвата сценария, который вы пытаетесь проанализировать.</span><span class="sxs-lookup"><span data-stu-id="5ca33-122">Perform the fewest actions you need to capture the scenario you're trying to analyze.</span></span> <span data-ttu-id="5ca33-123">Лишние действия со страницей будут создавать дополнительные данные и засорять результаты.</span><span class="sxs-lookup"><span data-stu-id="5ca33-123">Extraneous actions with the page will produce extra data and clutter your results.</span></span>

- <span data-ttu-id="5ca33-124">Профилер автоматически помещает в отчете основные события жизненного цикла приложения, такие как навигация страницы, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)и загрузка [страницы.](https://developer.mozilla.org/docs/Web/Events/load)</span><span class="sxs-lookup"><span data-stu-id="5ca33-124">The profiler will automatically mark major app lifecycle events in the report, such as page navigation, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded), and page [load](https://developer.mozilla.org/docs/Web/Events/load).</span></span> <span data-ttu-id="5ca33-125">Вы можете добавить настраиваемые маркеры, вызывая метод [Performance.mark()](https://developer.mozilla.org/docs/Web/API/Performance/mark) из кода или консоли.</span><span class="sxs-lookup"><span data-stu-id="5ca33-125">You can add custom markers by calling the [Performance.mark()](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the console.</span></span> 

- <span data-ttu-id="5ca33-126">Если время загрузки начальной страницы важно для анализа, обязательно очищайте [](./network.md) кэш браузера (с панели сети), чтобы гарантировать загрузку всех ресурсов страницы из сети.</span><span class="sxs-lookup"><span data-stu-id="5ca33-126">If initial page load times are important to your analysis, make sure to clear your browser cache (from the [Network](./network.md) panel) to ensure all page resources are loading from the network.</span></span>

- <span data-ttu-id="5ca33-127">Иногда бывает полезно записать несколько сеансов и/или пример одного сценария на разных компьютерах, чтобы лучше понять проблему производительности в подмыве.</span><span class="sxs-lookup"><span data-stu-id="5ca33-127">Sometimes it helps to record multiple sessions and/or sample the same scenario across different machines to better understand the performance issue in the wild.</span></span>

## <span data-ttu-id="5ca33-128">Линейка временной шкалы</span><span class="sxs-lookup"><span data-stu-id="5ca33-128">Timeline ruler</span></span>

<span data-ttu-id="5ca33-129">Временная шкала работает в качестве скользящей линейки.</span><span class="sxs-lookup"><span data-stu-id="5ca33-129">The timeline works as a sliding ruler.</span></span> <span data-ttu-id="5ca33-130">Используйте его, чтобы ограничить область отчета определенными временными рамками (или диапазоном событий), которые могут быть интересны.</span><span class="sxs-lookup"><span data-stu-id="5ca33-130">Use it to limit the scope of the report to the particular timeframe (or span of events) of interest.</span></span> <span data-ttu-id="5ca33-131">Перетащите \*\*\*\* элементы управления черным слайдом, чтобы ограничить диапазон времени, который вы [](#timeline-details) хотите изучить и отфильтровать из отчетов временной шкалы и стеков вызовов [JavaScript](#javascript-call-stacks) в нижней области сведений. \*\*</span><span class="sxs-lookup"><span data-stu-id="5ca33-131">Drag the black **slide controls** to limit the time range you wish to investigate and filter out extraneous profiling data from the [Timeline](#timeline-details) and [JavaScript call stacks](#javascript-call-stacks) reports in the lower *Details pane*.</span></span> 

<span data-ttu-id="5ca33-132">На линейке вы увидите два типа маркеров:</span><span class="sxs-lookup"><span data-stu-id="5ca33-132">You will see two types of markers on the ruler:</span></span>

 - <span data-ttu-id="5ca33-133">**Отметки жизненного** цикла приложения на временной шкале (например, навигация по страницам, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)и загрузка [страницы)](https://developer.mozilla.org/docs/Web/Events/load)регистрируются автоматически при записи профиля.</span><span class="sxs-lookup"><span data-stu-id="5ca33-133">**App lifecycle marks** on the timeline (such as page navigation, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded), and page [load](https://developer.mozilla.org/docs/Web/Events/load)) are automatically logged as you record a profile.</span></span>

 - <span data-ttu-id="5ca33-134">**Метки** пользователей — это настраиваемые маркеры, которые можно добавить с помощью вызовов метода [\*\*\*\*](./console.md) [Performance.mark()](https://developer.mozilla.org/docs/Web/API/Performance/mark) из кода или консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="5ca33-134">**User marks** are custom markers you can choose to add  with calls to the [Performance.mark()](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span> <span data-ttu-id="5ca33-135">С помощью *метода* [Performance.measure()](https://developer.mozilla.org/docs/Web/API/Performance/measure) можно сгруппить пометки начала и окончания в одном именовом виде. \*\*</span><span class="sxs-lookup"><span data-stu-id="5ca33-135">You can group *start* and *end* marks together as a single, named measure with the [Performance.measure()](https://developer.mozilla.org/docs/Web/API/Performance/measure) method.</span></span> 

<span data-ttu-id="5ca33-136">Выбрав диапазон времени, вы можете увеличить масштаб на панели инструментов \*\*\*\* или \*\*\*\* сбросить масштаб и очистить выбор, чтобы вернуться в полное представление трассировки производительности (без выбранного диапазона времени). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ca33-136">Once you have selected a time range, you can further **Zoom in** from the toolbar, or **Reset zoom** and **Clear selection** to return to the full view of the performance trace (with no time range selected).</span></span> <span data-ttu-id="5ca33-137">Эти элементы управления также доступны в контекстное меню щелчка правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="5ca33-137">These controls are also available from the right-click context menu.</span></span>

![Временная шкала панели производительности](./media/performance_timeline.png)

### <span data-ttu-id="5ca33-139">Использование ЦП</span><span class="sxs-lookup"><span data-stu-id="5ca33-139">CPU utilization</span></span>

<span data-ttu-id="5ca33-140">График использования ЦП **на** временной шкале % описывает ресурсы обработки, потребляемых различными подсистемами браузера, которые необходимы для запуска страницы, разбиваемой по категориям:</span><span class="sxs-lookup"><span data-stu-id="5ca33-140">The **CPU utilization %** timeline graph describes the processing resources consumed by the various browser subsystems required to run the page, broken out by category:</span></span>

#### <span data-ttu-id="5ca33-141">Загрузка</span><span class="sxs-lookup"><span data-stu-id="5ca33-141">Loading</span></span>
<span data-ttu-id="5ca33-142">Указывает время, затраченное на искомые ресурсы приложения и разчет HTML и CSS.</span><span class="sxs-lookup"><span data-stu-id="5ca33-142">Indicates time spent retrieving app resources and parsing HTML and CSS.</span></span> <span data-ttu-id="5ca33-143">Это могут быть сетевые запросы.</span><span class="sxs-lookup"><span data-stu-id="5ca33-143">This can include network requests.</span></span> <span data-ttu-id="5ca33-144">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-144">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-145">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-145">Event</span></span> | <span data-ttu-id="5ca33-146">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-146">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-147">CssParsing</span><span class="sxs-lookup"><span data-stu-id="5ca33-147">CssParsing</span></span>  | <span data-ttu-id="5ca33-148">Было выявилось новое содержимое CSS, необходимое для различета.</span><span class="sxs-lookup"><span data-stu-id="5ca33-148">New CSS content was encountered that needed to be parsed.</span></span>
<span data-ttu-id="5ca33-149">HtmlParsing</span><span class="sxs-lookup"><span data-stu-id="5ca33-149">HtmlParsing</span></span> | <span data-ttu-id="5ca33-150">Было выявилось новое HTML-содержимое, которое необходимо было разлить в узлы и вставить в DOM.</span><span class="sxs-lookup"><span data-stu-id="5ca33-150">New HTML content was encountered that needed to be parsed into nodes and inserted into the DOM.</span></span>
<span data-ttu-id="5ca33-151">HttpRequest</span><span class="sxs-lookup"><span data-stu-id="5ca33-151">HttpRequest</span></span> | <span data-ttu-id="5ca33-152">В DOM или XMLHttpRequest был создан удаленный ресурс, для создания которой требовался HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="5ca33-152">A remote resource was encountered in the DOM or an XMLHttpRequest was created that required an HTTP request to be made.</span></span>
<span data-ttu-id="5ca33-153">HtmlSpeculativeDownloading</span><span class="sxs-lookup"><span data-stu-id="5ca33-153">HtmlSpeculativeDownloading</span></span> | <span data-ttu-id="5ca33-154">В HTML-содержимом страницы был поиск необходимых ресурсов, чтобы http-запросы для них можно было запланировали как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="5ca33-154">The page's HTML content was being searched for required resources so that the HTTP requests for them could be scheduled as quickly as possible.</span></span>


#### <span data-ttu-id="5ca33-155">Сценарии</span><span class="sxs-lookup"><span data-stu-id="5ca33-155">Scripting</span></span>
<span data-ttu-id="5ca33-156">Указывает время, затраченное на разбиение и выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ca33-156">Indicates time spent parsing and executing JavaScript.</span></span> <span data-ttu-id="5ca33-157">Это относится к событиям DOM, timers, оценке сценариев и вызовам кадров анимации.</span><span class="sxs-lookup"><span data-stu-id="5ca33-157">This includes DOM events, timers, script evaluation, and animation frame callbacks.</span></span> <span data-ttu-id="5ca33-158">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-158">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-159">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-159">Event</span></span> | <span data-ttu-id="5ca33-160">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-160">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-161">DomEvent</span><span class="sxs-lookup"><span data-stu-id="5ca33-161">DomEvent</span></span> | <span data-ttu-id="5ca33-162">Событие сгорело с объектом DOM.</span><span class="sxs-lookup"><span data-stu-id="5ca33-162">An event was fired on a DOM object.</span></span>
<span data-ttu-id="5ca33-163">EvaluatingScript</span><span class="sxs-lookup"><span data-stu-id="5ca33-163">EvaluatingScript</span></span> | <span data-ttu-id="5ca33-164">В DOM был выполнен новый элемент, который необходимо было `<script>` выполнять и выполнять.</span><span class="sxs-lookup"><span data-stu-id="5ca33-164">A new `<script>` element was encountered in the DOM and needed to be parsed and executed.</span></span>
<span data-ttu-id="5ca33-165">EventHandler</span><span class="sxs-lookup"><span data-stu-id="5ca33-165">EventHandler</span></span> | <span data-ttu-id="5ca33-166">Зарегистрированный прослушиватель событий активируется в ответ на событие DOM.</span><span class="sxs-lookup"><span data-stu-id="5ca33-166">A registered event listener was triggered in response to a DOM event being fired.</span></span>
<span data-ttu-id="5ca33-167">Кадр</span><span class="sxs-lookup"><span data-stu-id="5ca33-167">Frame</span></span> | <span data-ttu-id="5ca33-168">Во время подготовки нового кадра активируется зарегистрированный вызов, чтобы он мог вносить визуальные изменения.</span><span class="sxs-lookup"><span data-stu-id="5ca33-168">While a new frame was being prepared a registered callback was triggered so that it could contribute visual changes.</span></span>
<span data-ttu-id="5ca33-169">Измерение</span><span class="sxs-lookup"><span data-stu-id="5ca33-169">Measure</span></span> | <span data-ttu-id="5ca33-170">С помощью этого метода измерялся сценарий для конкретного `performance.measure()` приложения.</span><span class="sxs-lookup"><span data-stu-id="5ca33-170">An app-specific scenario was measured using the `performance.measure()` method.</span></span>
<span data-ttu-id="5ca33-171">MediaQueryListener</span><span class="sxs-lookup"><span data-stu-id="5ca33-171">MediaQueryListener</span></span> | <span data-ttu-id="5ca33-172">Зарегистрированный запрос мультимедиа был признан недействительным, что привело к выполнению связанных прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="5ca33-172">A registered media query was invalidated which resulted in the execution of its associated listener(s).</span></span>
<span data-ttu-id="5ca33-173">Каблобссервер</span><span class="sxs-lookup"><span data-stu-id="5ca33-173">MutationObserver</span></span> | <span data-ttu-id="5ca33-174">Один или несколько наблюдаемых элементов DOM были изменены, что привело к выполнению связанного с Ним вызова.</span><span class="sxs-lookup"><span data-stu-id="5ca33-174">One or more observed DOM elements were modified which resulted in the execution of a MutationObserver's associated callback.</span></span>
<span data-ttu-id="5ca33-175">TimerFired</span><span class="sxs-lookup"><span data-stu-id="5ca33-175">TimerFired</span></span> | <span data-ttu-id="5ca33-176">Время выполнения запланированного времени, которое привело к выполнению связанного с ним вызова.</span><span class="sxs-lookup"><span data-stu-id="5ca33-176">A scheduled timer elapsed which resulted in the execution of its associated callback.</span></span>
<span data-ttu-id="5ca33-177">WindowsRuntimeAsyncCallback</span><span class="sxs-lookup"><span data-stu-id="5ca33-177">WindowsRuntimeAsyncCallback</span></span> | <span data-ttu-id="5ca33-178">Объектом времени runtime Windows была завершена а также астиная операция, которая инициирует `Promise` вызов.</span><span class="sxs-lookup"><span data-stu-id="5ca33-178">An async operation was completed by a Windows Runtime object which triggered a `Promise` callback.</span></span>
<span data-ttu-id="5ca33-179">WindowsRuntimeEvent</span><span class="sxs-lookup"><span data-stu-id="5ca33-179">WindowsRuntimeEvent</span></span> | <span data-ttu-id="5ca33-180">Событие сработало на объекте времени работы Windows, в результате чего активируется зарегистрированный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="5ca33-180">An event was fired on a Windows Runtime object which triggered a registered listener.</span></span>

#### <span data-ttu-id="5ca33-181">GC</span><span class="sxs-lookup"><span data-stu-id="5ca33-181">GC</span></span>
<span data-ttu-id="5ca33-182">Указывает время, затраченное на сбор памяти для объектов, которые больше не используются.</span><span class="sxs-lookup"><span data-stu-id="5ca33-182">Indicates time spent collecting memory for objects that are no longer in use.</span></span> <span data-ttu-id="5ca33-183">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-183">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-184">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-184">Event</span></span> | <span data-ttu-id="5ca33-185">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-185">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-186">Сборка мусора</span><span class="sxs-lookup"><span data-stu-id="5ca33-186">GarbageCollection</span></span> | <span data-ttu-id="5ca33-187">В среде запуска JavaScript был аудит текущего использования памяти приложением, чтобы определить, на какие объекты больше не ссылается и которые могут быть собраны.</span><span class="sxs-lookup"><span data-stu-id="5ca33-187">The JavaScript runtime audited the app's current memory usage in order to determine which objects aren't being referenced anymore and could therefore be collected.</span></span>

#### <span data-ttu-id="5ca33-188">Стиль</span><span class="sxs-lookup"><span data-stu-id="5ca33-188">Styling</span></span>
<span data-ttu-id="5ca33-189">Указывает время, затраченное на вычисление представления элементов и макета.</span><span class="sxs-lookup"><span data-stu-id="5ca33-189">Indicates time spent calculating element presentation and layout.</span></span> <span data-ttu-id="5ca33-190">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-190">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-191">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-191">Event</span></span> | <span data-ttu-id="5ca33-192">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-192">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-193">AlignedBeat</span><span class="sxs-lookup"><span data-stu-id="5ca33-193">AlignedBeat</span></span> | <span data-ttu-id="5ca33-194">Ожидающих визуальных изменений, внесенных в DOM, были обработаны, чтобы можно было обновить отображение приложения.</span><span class="sxs-lookup"><span data-stu-id="5ca33-194">Pending visual changes that were made to the DOM were processed so that the app's display could be updated.</span></span>
<span data-ttu-id="5ca33-195">CssCalculation</span><span class="sxs-lookup"><span data-stu-id="5ca33-195">CssCalculation</span></span> | <span data-ttu-id="5ca33-196">Были внесены изменения в МОДЕЛЬ DOM или добавлен новый контент CSS, что требует пересчета свойств стиля всех затронутых элементов.</span><span class="sxs-lookup"><span data-stu-id="5ca33-196">Changes were made to the DOM or new CSS content was added, requiring the style properties of all affected elements to be recalculated.</span></span>
<span data-ttu-id="5ca33-197">Макет</span><span class="sxs-lookup"><span data-stu-id="5ca33-197">Layout</span></span> | <span data-ttu-id="5ca33-198">В doM были внесены изменения, которые требовали вычисления размера и/или положения всех затронутых элементов.</span><span class="sxs-lookup"><span data-stu-id="5ca33-198">Changes were made to the DOM that required the size and/or position of all affected elements to be computed.</span></span>

#### <span data-ttu-id="5ca33-199">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="5ca33-199">Rendering</span></span>
<span data-ttu-id="5ca33-200">Указывает время, затраченное на рисование экрана.</span><span class="sxs-lookup"><span data-stu-id="5ca33-200">Indicates time spent in painting the screen.</span></span> <span data-ttu-id="5ca33-201">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-201">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-202">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-202">Event</span></span> | <span data-ttu-id="5ca33-203">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-203">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-204">Paint</span><span class="sxs-lookup"><span data-stu-id="5ca33-204">Paint</span></span> | <span data-ttu-id="5ca33-205">В doM были внесены визуальные изменения, которые требовали перерисовки всех затронутых частей страницы.</span><span class="sxs-lookup"><span data-stu-id="5ca33-205">Visual changes were made to the DOM that required all affected portions of the page to be redrawn.</span></span>
<span data-ttu-id="5ca33-206">RenderLayer</span><span class="sxs-lookup"><span data-stu-id="5ca33-206">RenderLayer</span></span> | <span data-ttu-id="5ca33-207">Были внесены визуальные изменения в независимо отрисоваванный фрагмент DOM (называемого слоем), который требовал перерисовки соответствующей части страницы.</span><span class="sxs-lookup"><span data-stu-id="5ca33-207">Visual changes were made to an independently rendered fragment of the DOM (called a layer) which required its respective portion of the page to be redrawn.</span></span>

#### <span data-ttu-id="5ca33-208">Декодирования изображений</span><span class="sxs-lookup"><span data-stu-id="5ca33-208">Image decoding</span></span>
<span data-ttu-id="5ca33-209">Указывает время, затраченное на расшифровку и декодирования изображений.</span><span class="sxs-lookup"><span data-stu-id="5ca33-209">Indicates time spent decompressing and decoding images.</span></span> <span data-ttu-id="5ca33-210">На временной шкале регистрируются следующие связанные [события:](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-210">The following associated events are logged in the [Timeline](#timeline-details):</span></span>

<span data-ttu-id="5ca33-211">Событие</span><span class="sxs-lookup"><span data-stu-id="5ca33-211">Event</span></span> | <span data-ttu-id="5ca33-212">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-212">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-213">ImageDecoded</span><span class="sxs-lookup"><span data-stu-id="5ca33-213">ImageDecoded</span></span> | <span data-ttu-id="5ca33-214">Изображение было включено в DOM, и его необходимо было расшифровки из исходного формата в растровую карту.</span><span class="sxs-lookup"><span data-stu-id="5ca33-214">An image was included into the DOM and needed be to decompressed from its original format into a bitmap.</span></span>

### <span data-ttu-id="5ca33-215">Визуальная пропускная способность</span><span class="sxs-lookup"><span data-stu-id="5ca33-215">Visual throughput</span></span>

<span data-ttu-id="5ca33-216">На графике пропускной способности визуального \*\* представления **(FPS)** показана предполагаемая частота кадров в секунду (FPS) в ходе сценария профилирования, где идеальной скоростью отображения является 60 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="5ca33-216">The **Visual throughput (FPS)** graph shows the estimated *frames per second* (FPS) during the course of the profiling scenario, where 60 FPS is the ideal display rate.</span></span> <span data-ttu-id="5ca33-217">Dips in the frame rate indicate performance bottlenecks and a frame rate of zero means that frames are getting dropped entirely.</span><span class="sxs-lookup"><span data-stu-id="5ca33-217">Dips in the frame rate indicate performance bottlenecks and a frame rate of zero means that frames are getting dropped entirely.</span></span>

## <span data-ttu-id="5ca33-218">Сведения о временной шкале</span><span class="sxs-lookup"><span data-stu-id="5ca33-218">Timeline details</span></span>

<span data-ttu-id="5ca33-219">Используйте нижнюю часть области сведений, чтобы получить полную информацию о том, что произошло на странице.</span><span class="sxs-lookup"><span data-stu-id="5ca33-219">Use the lowermost details pane to get the full breakdown of what happened on the page.</span></span> <span data-ttu-id="5ca33-220">Вкладка **"Сведения** временной шкалы" содержит разбивку событий, произошедших в различных подсистемах браузера.</span><span class="sxs-lookup"><span data-stu-id="5ca33-220">The **Timeline details** tab provides a breakdown of events that occurred within the various browser subsystems.</span></span>

![Области сведений о временной шкале производительности](./media/performance_details_timeline.png)

1. **<span data-ttu-id="5ca33-222">Управление сортировкой списка событий</span><span class="sxs-lookup"><span data-stu-id="5ca33-222">Event list sort control</span></span>**

    <span data-ttu-id="5ca33-223">Используйте управление **сортировкой по** выпадающим спискам, чтобы переключить порядок списка событий между *временем начала* или *длительностью (включительно).* [](#event-list)</span><span class="sxs-lookup"><span data-stu-id="5ca33-223">Use the **Sort by** dropdown control to toggle the [Event list](#event-list) order between *Start time* or *Duration (inclusive*).</span></span> <span data-ttu-id="5ca33-224">Это также изменяет представление сведений выбранной [временной шкалы.](#selected-timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-224">This also changes the view of the [Selected timeline details](#selected-timeline-details).</span></span>

2. **<span data-ttu-id="5ca33-225">Группировка событий по кадру</span><span class="sxs-lookup"><span data-stu-id="5ca33-225">Group events by frame</span></span>**

    <span data-ttu-id="5ca33-226">Используйте \*\*\*\* события верхнего уровня группы по кадрам для группировки событий верхнего уровня *(разметка HTML,* событие DOM и т. д.) в соответствующую единицу работы (или кадр) в периоды времени, в течение которых происходили анимации или визуальные обновления.</span><span class="sxs-lookup"><span data-stu-id="5ca33-226">Use the **Group top level events by frames** toggle to group top-level events (*HTML parsing, Layout, DOM event,* etc.) into their corresponding unit of work (or "frame") during periods of time where animations/visual updates were occurring.</span></span> <span data-ttu-id="5ca33-227">Кадры обрабатываются как другие события, поэтому их можно отсортировать или отфильтровать, а также предоставить сводку по времени инклюзивности при нажатии в списке [событий.](#event-list) \*\*</span><span class="sxs-lookup"><span data-stu-id="5ca33-227">The frames are treated like other events, so they can be sorted/filtered and provide an *Inclusive time* summary when clicked in the [Event list](#event-list).</span></span>

3. **<span data-ttu-id="5ca33-228">Элементы управления фильтром списка событий</span><span class="sxs-lookup"><span data-stu-id="5ca33-228">Event list filter controls</span></span>**

    <span data-ttu-id="5ca33-229">Используйте меню **"События фильтра"** для настройки типов событий, показанных в сведениях временной [шкалы.](#timeline-details)</span><span class="sxs-lookup"><span data-stu-id="5ca33-229">Use the **Filter events** menu to configure the types of events shown in the [timeline details](#timeline-details).</span></span> 

    ![Управление фильтрацией событий производительности](./media/performance_filter_events.png) 

    <span data-ttu-id="5ca33-231">Доступны следующие фильтры:</span><span class="sxs-lookup"><span data-stu-id="5ca33-231">The following filters are available:</span></span>

   - <span data-ttu-id="5ca33-232">**Декодирования изображений**: показать события, произошедшие в фоновом потоке (например, декодирования изображений, GC).</span><span class="sxs-lookup"><span data-stu-id="5ca33-232">**Image decoding**: Show events which occurred on a background thread (e.g. Image decoding, GC).</span></span> 
   - <span data-ttu-id="5ca33-233">**Сетевой трафик**: показывать HTTP-запросы, привязанные к сети.</span><span class="sxs-lookup"><span data-stu-id="5ca33-233">**Network traffic**: Show HTTP requests which were network-bound.</span></span>
   - <span data-ttu-id="5ca33-234">**Действие пользовательского**интерфейса: показывать события, произошедшие в потоке пользовательского интерфейса и/или потоке отрисовки (например, обработчики событий DOM, Layout).</span><span class="sxs-lookup"><span data-stu-id="5ca33-234">**UI activity**: Show events which occurred on the UI thread and/or render thread (e.g. DOM event handlers, Layout).</span></span>
   - <span data-ttu-id="5ca33-235">**Меры пользователя:** показывать настраиваемые события, которые указывают на вызовы метода performance.measure().</span><span class="sxs-lookup"><span data-stu-id="5ca33-235">**User measures**: Show custom events which indicate calls to the performance.measure() method.</span></span>

     <span data-ttu-id="5ca33-236">Можно дополнительно фильтровать события верхнего уровня по их продолжительности включительно.</span><span class="sxs-lookup"><span data-stu-id="5ca33-236">You can further filter top-level events by their inclusive duration.</span></span>

### <span data-ttu-id="5ca33-237">Список событий</span><span class="sxs-lookup"><span data-stu-id="5ca33-237">Event list</span></span>

<span data-ttu-id="5ca33-238">Список *событий предоставляет хронологический* список событий подсистем браузера, произошедших в течение выбранного периода времени. [](#cpu-utilization)</span><span class="sxs-lookup"><span data-stu-id="5ca33-238">The *Event list* gives you a chronological list of [browser subsystem events](#cpu-utilization) that occurred during the selected span of time.</span></span> 

<span data-ttu-id="5ca33-239">Щелкните любую запись, чтобы заполнить диаграмму сведений о выбранном **событии** для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="5ca33-239">Click on any entry to populate the **Selected event details** chart for that item.</span></span> <span data-ttu-id="5ca33-240">Записи с вложенными событиями и функциями будут \*\* отображаться включительно **(время,** затраченное на выполнение функции и любых других вызываемой функции) и монопольное **(время,** затраченное только в теле самой вызывающей функции) на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="5ca33-240">Entries with nested events / functions will show their **inclusive** (time spent executing the function *and* any other functions it called) and **exclusive** (time spent only within the body of the calling function itself) times displayed in the chart.</span></span>

<span data-ttu-id="5ca33-241">Щелкните правой кнопкой мыши любую запись, чтобы открыть контекстное меню, чтобы отфильтровать временную шкалу, чтобы отфильтровать только это событие, и просмотреть исходный код, отвечающий за событие, на панели отладки [**(или**](./debugger.md) панели элементов, если применимо). [\*\*\*\*](./elements.md)</span><span class="sxs-lookup"><span data-stu-id="5ca33-241">Right-click on any entry to open the context menu to filter the timeline to only that event and view the source code responsible for the event in the [**Debugger**](./debugger.md) (or [**Elements**](./elements.md) panel, if applicable).</span></span>

### <span data-ttu-id="5ca33-242">Сведения о выбранной временной шкале</span><span class="sxs-lookup"><span data-stu-id="5ca33-242">Selected timeline details</span></span>

<span data-ttu-id="5ca33-243">Сведения *о выбранной временной шкале* предоставляют подробный график инклюзивного и монопольного времени событий в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="5ca33-243">The *Selected timeline details* provides a detailed bar graph of inclusive/exclusive event times during the selected time span.</span></span> <span data-ttu-id="5ca33-244">При сортировке по *длительности (включительно)* с помощью управления сортировкой списка событий наиболее длительные события визуально выделяются на этой диаграмме. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5ca33-244">When you sort by *Duration (inclusive)* using the **Event list sort control**, the longest running events will visually stand out in this chart.</span></span> 

### <span data-ttu-id="5ca33-245">Сведения о выбранном событии</span><span class="sxs-lookup"><span data-stu-id="5ca33-245">Selected event details</span></span>

<span data-ttu-id="5ca33-246">Этот отчет содержит дополнительные сведения о выбранном событии, включая время *начала,* тип исполняемого потока (например, \*\* Загрузка, *пользовательский* *интерфейс,* отрисовка) и другие контекстные сведения, специфичные для конкретного типа события.</span><span class="sxs-lookup"><span data-stu-id="5ca33-246">This report provides further information about the selected event, including *Start time*, the executing thread type (for example, *Download*, *UI*, *Render*), and other contextual details specific to the specific event type.</span></span> <span data-ttu-id="5ca33-247">Например, типы *прослушиватель событий* предоставляют ссылки отладщика на функцию *callback* и *стек вызовов Scheduling.*</span><span class="sxs-lookup"><span data-stu-id="5ca33-247">For example, *Event listener* types provide debugger links to the *Callback function* and *Scheduling call stack*.</span></span>

## <span data-ttu-id="5ca33-248">Стеки вызовов JavaScript</span><span class="sxs-lookup"><span data-stu-id="5ca33-248">JavaScript call stacks</span></span>

![Временные рамки производительности для стеков вызовов JavaScript](./media/performance_details_javascript.png)

<span data-ttu-id="5ca33-250">Вкладка стека вызовов **JavaScript** предоставляет сведения об использовании ЦП и временные рамки для функций скрипта, которые выполняются в течение выбранного диапазона времени:</span><span class="sxs-lookup"><span data-stu-id="5ca33-250">The **JavaScript call stacks** tab provides CPU usage information and timings for the script functions that ran during the selected time range:</span></span>

 <span data-ttu-id="5ca33-251">Столбец</span><span class="sxs-lookup"><span data-stu-id="5ca33-251">Column</span></span> | <span data-ttu-id="5ca33-252">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca33-252">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5ca33-253">Имя функции</span><span class="sxs-lookup"><span data-stu-id="5ca33-253">Function name</span></span> | <span data-ttu-id="5ca33-254">Имя браузера или пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="5ca33-254">Name of browser or user-defined function.</span></span>
<span data-ttu-id="5ca33-255">Инклюзивный ЦП (%)</span><span class="sxs-lookup"><span data-stu-id="5ca33-255">Inclusive CPU (%)</span></span> | <span data-ttu-id="5ca33-256">Процент выбранных действий ЦП в этой функции и в функциях, которые вызваны этой функцией.</span><span class="sxs-lookup"><span data-stu-id="5ca33-256">Percentage of selected CPU activity in this function and in functions called by this function.</span></span>
<span data-ttu-id="5ca33-257">Монопольный ЦП (%)</span><span class="sxs-lookup"><span data-stu-id="5ca33-257">Exclusive CPU (%)</span></span> | <span data-ttu-id="5ca33-258">Процент выбранных действий ЦП в этой функции, за исключением действий в функциях, называемых этой функцией.</span><span class="sxs-lookup"><span data-stu-id="5ca33-258">Percentage of selected CPU activity in this function, excluding activity in functions called by this function.</span></span>
<span data-ttu-id="5ca33-259">Инклюзивный ЦП (мс)</span><span class="sxs-lookup"><span data-stu-id="5ca33-259">Inclusive CPU (ms)</span></span> | <span data-ttu-id="5ca33-260">Время ЦП, затраченное на выполнение кода в этой функции и в функциях, называемых этой функцией.</span><span class="sxs-lookup"><span data-stu-id="5ca33-260">CPU time spent executing code in this function and in functions called by this function.</span></span>
<span data-ttu-id="5ca33-261">Монопольный ЦП (мс)</span><span class="sxs-lookup"><span data-stu-id="5ca33-261">Exclusive CPU (ms)</span></span> | <span data-ttu-id="5ca33-262">Время, затраченное ЦП на выполнение кода в этой функции, за исключением времени в функциях, которые эта функция вызвала.</span><span class="sxs-lookup"><span data-stu-id="5ca33-262">CPU time spent executing code in this function, excluding time in functions called by this function.</span></span>
<span data-ttu-id="5ca33-263">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="5ca33-263">URL</span></span> | <span data-ttu-id="5ca33-264">URL-адреса, в которых возникла рамка стека.</span><span class="sxs-lookup"><span data-stu-id="5ca33-264">URL(s) where stack frame occurred.</span></span> <span data-ttu-id="5ca33-265">Вызовы функций из браузера (веб-API на основе стандартов) помечены как *[DOM]*.</span><span class="sxs-lookup"><span data-stu-id="5ca33-265">Function calls originating from the browser (standards-based web APIs) are labeled as *[DOM]*.</span></span>

## <span data-ttu-id="5ca33-266">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="5ca33-266">Shortcuts</span></span>

| <span data-ttu-id="5ca33-267">Действие</span><span class="sxs-lookup"><span data-stu-id="5ca33-267">Action</span></span>                         | <span data-ttu-id="5ca33-268">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="5ca33-268">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="5ca33-269">Запуск и остановка сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="5ca33-269">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="5ca33-270">Импорт сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="5ca33-270">Import profiling session</span></span>       | `Ctrl` + `O` |
| <span data-ttu-id="5ca33-271">Экспорт сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="5ca33-271">Export profiling session</span></span>       | `Ctrl` + `S` |

## <span data-ttu-id="5ca33-272">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="5ca33-272">Known Issues</span></span>

### <span data-ttu-id="5ca33-273">Ошибка при запуске сеанса профилирования</span><span class="sxs-lookup"><span data-stu-id="5ca33-273">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="5ca33-274">Если вы видите это \*\*\*\* сообщение об ошибке: ошибка при запуске сеанса профилирования в средстве "Производительность", выполните следующие действия для обходного решения.</span><span class="sxs-lookup"><span data-stu-id="5ca33-274">If you see this error message: **An error occurred while starting the profiling session** in the Performance tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="5ca33-275">Нажмите `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="5ca33-275">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="5ca33-276">В диалоговом окке "Выполнить" **введите services.msc**.</span><span class="sxs-lookup"><span data-stu-id="5ca33-276">In the Run dialog, enter **services.msc**.</span></span>
![known-issues-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="5ca33-278">Найдите стандартную службу сборщика Microsoft **(R) Diagnostics Hub** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="5ca33-278">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![known-issues-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="5ca33-280">Перезапустите стандартную службу сборщика Microsoft **(R) Diagnostics Hub.**</span><span class="sxs-lookup"><span data-stu-id="5ca33-280">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![known-issues-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="5ca33-282">Закроем Инструменты разработчика Microsoft Edge и вкладку. Откройте новую вкладку, перейдите на страницу и нажмите `F12` .</span><span class="sxs-lookup"><span data-stu-id="5ca33-282">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="5ca33-283">Теперь вы сможете начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="5ca33-283">You should now be able to begin profiling.</span></span>
![known-issues-4](./media/known_issues_4-performance.PNG)

<span data-ttu-id="5ca33-285">По-прежнему возникают проблемы?</span><span class="sxs-lookup"><span data-stu-id="5ca33-285">Still running into problems?</span></span> <span data-ttu-id="5ca33-286">Отправьте нам свой отзыв с помощью **значка отправки отзыва!**</span><span class="sxs-lookup"><span data-stu-id="5ca33-286">Please send us your feedback using the **Send feedback** icon!</span></span> 

![known-issues-5](./media/known_issues_5.PNG)

### <span data-ttu-id="5ca33-288">При остановке сеанса профилирования произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ca33-288">An error occurred while stopping the profiling session.</span></span>

<span data-ttu-id="5ca33-289">Если вы видите это \*\*\*\* сообщение об ошибке: при остановке сеанса профилирования в средстве производительности произошла ошибка, выполните следующие действия для обходного решения.</span><span class="sxs-lookup"><span data-stu-id="5ca33-289">If you see this error message: **An error occurred while stopping the profiling session** in the Performance tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="5ca33-290">Нажмите `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="5ca33-290">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="5ca33-291">В диалоговом окке "Выполнить" **введите services.msc**.</span><span class="sxs-lookup"><span data-stu-id="5ca33-291">In the Run dialog, enter **services.msc**.</span></span>
![known-issues-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="5ca33-293">Найдите стандартную службу сборщика Microsoft **(R) Diagnostics Hub** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="5ca33-293">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![known-issues-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="5ca33-295">Перезапустите стандартную службу сборщика Microsoft **(R) Diagnostics Hub.**</span><span class="sxs-lookup"><span data-stu-id="5ca33-295">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![known-issues-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="5ca33-297">Закроем Инструменты разработчика Microsoft Edge и вкладку. Откройте новую вкладку, перейдите на страницу и нажмите `F12` .</span><span class="sxs-lookup"><span data-stu-id="5ca33-297">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="5ca33-298">Теперь вы сможете начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="5ca33-298">You should now be able to begin profiling.</span></span>
![known-issues-4](./media/known_issues_4-performance.PNG)

<span data-ttu-id="5ca33-300">По-прежнему возникают проблемы?</span><span class="sxs-lookup"><span data-stu-id="5ca33-300">Still running into problems?</span></span> <span data-ttu-id="5ca33-301">Отправьте нам свой отзыв с помощью **значка отправки отзыва!**</span><span class="sxs-lookup"><span data-stu-id="5ca33-301">Please send us your feedback using the **Send feedback** icon!</span></span> 

![known-issues-5](./media/known_issues_5.PNG)
