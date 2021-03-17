---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска и исправления ошибок JavaScript.
title: Начало работы с отладки JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: bbfb766bcc03e4c4fe0f975f1ecfccbef08084be
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439467"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="04775-104">Начало работы с отладки JavaScript в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="04775-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="04775-105">В этой статье рассказывается об основных процессах отладки любых проблем JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="04775-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="04775-106">Шаг 1. Воспроизведение ошибки</span><span class="sxs-lookup"><span data-stu-id="04775-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="04775-107">Поиск ряда действий, которые последовательно воспроизводят ошибку, всегда является первым шагом к отладки.</span><span class="sxs-lookup"><span data-stu-id="04775-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="04775-108">Выберите **Open Demo**.</span><span class="sxs-lookup"><span data-stu-id="04775-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="04775-109">Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и откройте демонстрацию на новой вкладке браузера.</span><span class="sxs-lookup"><span data-stu-id="04775-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="04775-110">Open Demo</span><span class="sxs-lookup"><span data-stu-id="04775-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="04775-111">`5`Введите **текстовое поле Номер 1.**</span><span class="sxs-lookup"><span data-stu-id="04775-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="04775-112">`1`Введите **текстовое поле Номер 2.**</span><span class="sxs-lookup"><span data-stu-id="04775-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="04775-113">Выберите **Добавить номер 1 и Номер 2.**</span><span class="sxs-lookup"><span data-stu-id="04775-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="04775-114">Метка ниже кнопки говорит `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="04775-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="04775-115">Результат должен быть `6` .</span><span class="sxs-lookup"><span data-stu-id="04775-115">The result should be `6`.</span></span>  <span data-ttu-id="04775-116">Затем исправьте ошибку добавления, которая является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="04775-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 результат в 51, но должен быть 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="04775-118">результаты, `51` но должны быть</span><span class="sxs-lookup"><span data-stu-id="04775-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="04775-119">Шаг 2. Знакомство с пользовательским интерфейсом инструмента Sources</span><span class="sxs-lookup"><span data-stu-id="04775-119">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="04775-120">DevTools предоставляет множество различных инструментов для различных задач.</span><span class="sxs-lookup"><span data-stu-id="04775-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="04775-121">Различные задачи включают изменение CSS, профилирование производительности загрузки страниц и запросы на мониторинг сети.</span><span class="sxs-lookup"><span data-stu-id="04775-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="04775-122">Средство **Sources** — это место, где отламываю JavaScript.</span><span class="sxs-lookup"><span data-stu-id="04775-122">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="04775-123">Чтобы открыть **консольный** инструмент в DevTools, выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="04775-123">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Средство Консоли" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="04775-125">Средство **Консоли**</span><span class="sxs-lookup"><span data-stu-id="04775-125">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="04775-126">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="04775-126">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Средство Источники" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="04775-128">Средство **Источники**</span><span class="sxs-lookup"><span data-stu-id="04775-128">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="04775-129">Пользовательский **интерфейс** средства Sources имеет три части.</span><span class="sxs-lookup"><span data-stu-id="04775-129">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="3 части пользовательского интерфейса инструмента Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="04775-131">3 части пользовательского **интерфейса инструмента Sources**</span><span class="sxs-lookup"><span data-stu-id="04775-131">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="04775-132">Панель **навигатора** файлов \(Раздел 1 на предыдущем рисунке\).</span><span class="sxs-lookup"><span data-stu-id="04775-132">The **File Navigator** panel \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="04775-133">Каждый файл, который запрашивает веб-страницу, указан здесь.</span><span class="sxs-lookup"><span data-stu-id="04775-133">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="04775-134">Панель **редактора** кода \(Раздел 2 на предыдущем рисунке\).</span><span class="sxs-lookup"><span data-stu-id="04775-134">The **Code Editor** panel \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="04775-135">После выбора файла в области **Навигатора** файлов содержимое этого файла отображается здесь.</span><span class="sxs-lookup"><span data-stu-id="04775-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="04775-136">Панель **отладки JavaScript** \(Раздел 3 на предыдущем рисунке\).</span><span class="sxs-lookup"><span data-stu-id="04775-136">The **JavaScript Debugging** panel \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="04775-137">Различные средства для проверки JavaScript для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="04775-137">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="04775-138">Если окно DevTools широкое, эта области отображается справа от области **редактора** кода.</span><span class="sxs-lookup"><span data-stu-id="04775-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="04775-139">Шаг 3. Приостановка кода с помощью точки разрыва</span><span class="sxs-lookup"><span data-stu-id="04775-139">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="04775-140">Распространенный метод отладки этого типа проблемы — вставить несколько заявлений в код, а затем проверить значения по мере `console.log()` работы сценария.</span><span class="sxs-lookup"><span data-stu-id="04775-140">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="04775-141">Пример:</span><span class="sxs-lookup"><span data-stu-id="04775-141">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="04775-142">Метод `console.log()` может получить работу, но **breakpoints** получить его быстрее.</span><span class="sxs-lookup"><span data-stu-id="04775-142">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="04775-143">Точка разрыва позволяет приостановить работу кода в середине времени работы и вовремя изучить все значения.</span><span class="sxs-lookup"><span data-stu-id="04775-143">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="04775-144">Точки breakpoints имеют следующие преимущества по сравнению с `console.log()` методом.</span><span class="sxs-lookup"><span data-stu-id="04775-144">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="04775-145">Для этого необходимо вручную открыть исходный код, найти соответствующий код, вставить инструкции и обновить веб-страницу для отображения сообщений в `console.log()` `console.log()` консоли. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="04775-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="04775-146">При разрывных точках можно остановиться на соответствующем коде, даже не зная, как он структурирован.</span><span class="sxs-lookup"><span data-stu-id="04775-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="04775-147">В своих заявлениях необходимо четко указать каждое `console.log()` значение, которое необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="04775-147">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="04775-148">С помощью точек breakpoints DevTools показывает значения всех переменных в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="04775-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="04775-149">Иногда переменные, влияющие на код, скрыты и запутываются.</span><span class="sxs-lookup"><span data-stu-id="04775-149">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="04775-150">Короче говоря, breakpoints может помочь вам найти и устранить ошибки быстрее, чем `console.log()` метод.</span><span class="sxs-lookup"><span data-stu-id="04775-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="04775-151">Если вы отойти назад и подумать о том, как работает приложение, вы можете сделать образованное предположение, что неправильная сумма \( \) вычисляется в прослушиватель событий, связанный с кнопкой Добавить номер 1 и Номер `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="04775-151">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="04775-152">Таким образом, вероятно, необходимо приостановить код во время `click` прослушивания.</span><span class="sxs-lookup"><span data-stu-id="04775-152">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="04775-153">**Breakpoints listener event** let you do exactly that:</span><span class="sxs-lookup"><span data-stu-id="04775-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="04775-154">В области **отладки JavaScript** выберите точки **breakpoints для** прослушивания событий, чтобы расширить раздел.</span><span class="sxs-lookup"><span data-stu-id="04775-154">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="04775-155">DevTools открывает список расширяемых категорий событий, таких как **Animation** и **Clipboard.**</span><span class="sxs-lookup"><span data-stu-id="04775-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="04775-156">Рядом с **категорией событий Мыши** выберите **Расширение** \( ![ Расширение ](../media/expand-icon.msft.png) значка \).</span><span class="sxs-lookup"><span data-stu-id="04775-156">Next to the **Mouse** event category, choose **Expand** \(![Expand icon](../media/expand-icon.msft.png)\).</span></span>  <span data-ttu-id="04775-157">DevTools показывает список событий мыши, таких как **щелчки** мыши и **мыши.**</span><span class="sxs-lookup"><span data-stu-id="04775-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="04775-158">Рядом с каждым событием имеется почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="04775-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="04775-159">Выберите почтовый ящик рядом, чтобы **щелкнуть**.</span><span class="sxs-lookup"><span data-stu-id="04775-159">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="04775-160">DevTools теперь настроен на автоматическое приостановление при запуске любого `click` прослушиватель события.</span><span class="sxs-lookup"><span data-stu-id="04775-160">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Выберите контрольный ящик рядом с кнопкой мыши" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="04775-162">Выберите контрольный ящик рядом с **кнопкой мыши**</span><span class="sxs-lookup"><span data-stu-id="04775-162">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="04775-163">Возвращаясь к демонстрации, **выберите добавить номер 1 и номер 2** снова.</span><span class="sxs-lookup"><span data-stu-id="04775-163">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="04775-164">DevTools останавливает демонстрацию и выделяет строку кода в **средстве Sources.**</span><span class="sxs-lookup"><span data-stu-id="04775-164">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="04775-165">DevTools следует приостановить на строке 16 в `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="04775-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="04775-166">Если вы приостанавливлить другую строку кода, выберите **выполнение** сценариев возобновления \. Возобновление выполнения скрипта \) до остановки ![ на ](../media/resume-script-run-icon.msft.png) правильной строке.</span><span class="sxs-lookup"><span data-stu-id="04775-166">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="04775-167">Если вы остановились на другой строке, у вас есть расширение браузера, которое регистрирует слушателя событий на каждой `click` веб-странице, которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="04775-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="04775-168">Вы приостанавливована `click` в прослушиватель расширения.</span><span class="sxs-lookup"><span data-stu-id="04775-168">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="04775-169">Если вы используете режим InPrivate для просмотра в закрытом **режиме,** который отключает все расширения, вы можете каждый раз приостанавлить нужную строку кода.</span><span class="sxs-lookup"><span data-stu-id="04775-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="04775-170">**Breakpoints слушателя событий** — это только один из многих типов точек разрыва, доступных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="04775-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="04775-171">Запомните все различные типы, чтобы помочь вам отлачивать различные сценарии как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="04775-171">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="04775-172">Шаг 4. Прошаговка кода</span><span class="sxs-lookup"><span data-stu-id="04775-172">Step 4: Step through the code</span></span>  

<span data-ttu-id="04775-173">Одной из распространенных причин ошибок является то, что сценарий выполняется в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="04775-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="04775-174">Пройдя через код, вы сможете выполнить время работы кода.</span><span class="sxs-lookup"><span data-stu-id="04775-174">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="04775-175">Вы проходите по одной строке, чтобы выяснить, где именно работает код в другом порядке, чем вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="04775-175">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="04775-176">Попробуйте его сейчас:</span><span class="sxs-lookup"><span data-stu-id="04775-176">Try it now:</span></span>  

1.  <span data-ttu-id="04775-177">Выберите **шаг по следующему вызову** функции \. Шаг за следующий вызов ![ ](../media/step-over-icon.msft.png) функции \).</span><span class="sxs-lookup"><span data-stu-id="04775-177">Choose **Step over next function call** \(![Step over next function call](../media/step-over-icon.msft.png)\).</span></span>  <span data-ttu-id="04775-178">DevTools запускает следующий код, не вступая в него.</span><span class="sxs-lookup"><span data-stu-id="04775-178">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="04775-179">DevTools пропускает несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="04775-179">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="04775-180">Это потому, что оценивается как ложное, поэтому блок кода для заявления `inputsAreEmpty()` `if` не работает.</span><span class="sxs-lookup"><span data-stu-id="04775-180">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="04775-181">В **средстве Источники** DevTools \*\*\*\* выберите Шаг в следующий вызов функции \( Шаг в следующий вызов функции \) для того, чтобы выполнить время работы функции по одной ![ ](../media/step-into-icon.msft.png) `updateLabel()` строке за один раз.</span><span class="sxs-lookup"><span data-stu-id="04775-181">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call](../media/step-into-icon.msft.png)\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="04775-182">Просмотр одной строки за один раз — это основная идея пошаговая проверка кода.</span><span class="sxs-lookup"><span data-stu-id="04775-182">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="04775-183">Если просмотреть `get-started.js` код, ошибка, вероятно, находится где-то в `updateLabel()` функции.</span><span class="sxs-lookup"><span data-stu-id="04775-183">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="04775-184">Вместо того, чтобы перешагировать каждую строку кода, вы можете использовать другой тип точки разрыва, чтобы приостановить код ближе к вероятному расположению ошибки.</span><span class="sxs-lookup"><span data-stu-id="04775-184">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="04775-185">Шаг 5. Установите точку разрыва кода</span><span class="sxs-lookup"><span data-stu-id="04775-185">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="04775-186">Разрывные точки line-of-code являются наиболее распространенным типом точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="04775-186">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="04775-187">При подъехав к определенной строке кода, необходимо приостановить, используйте точку разрыва кода.</span><span class="sxs-lookup"><span data-stu-id="04775-187">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="04775-188">Посмотрите на последнюю строку кода в `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="04775-188">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="04775-189">Слева отображается число этой определенной строки кода в **качестве 34**.</span><span class="sxs-lookup"><span data-stu-id="04775-189">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="04775-190">Выберите **строку 34**.</span><span class="sxs-lookup"><span data-stu-id="04775-190">Choose line **34**.</span></span>  <span data-ttu-id="04775-191">DevTools отображает красный значок слева от **34**.</span><span class="sxs-lookup"><span data-stu-id="04775-191">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="04775-192">Красный значок указывает, что в этой строке находится точка разрыва строки кода.</span><span class="sxs-lookup"><span data-stu-id="04775-192">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="04775-193">DevTools всегда останавливается перед запуском этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="04775-193">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="04775-194">Выберите **выполнение скрипта** Resume \. ![ Возобновление выполнения ](../media/resume-script-run-icon.msft.png) скрипта \).</span><span class="sxs-lookup"><span data-stu-id="04775-194">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  <span data-ttu-id="04775-195">Сценарий продолжает работать, пока не достигнет строки 33.</span><span class="sxs-lookup"><span data-stu-id="04775-195">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="04775-196">На строках 31, 32 и 33 DevTools печатает значения , и справа от полу-двоеточия на `addend1` `addend2` каждой `sum` строке.</span><span class="sxs-lookup"><span data-stu-id="04775-196">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools приостанавливовка на точке разрыва кода на строке 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="04775-198">DevTools приостанавливовка на точке разрыва кода на строке 34</span><span class="sxs-lookup"><span data-stu-id="04775-198">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="04775-199">Шаг 6. Проверка переменных значений</span><span class="sxs-lookup"><span data-stu-id="04775-199">Step 6: Check variable values</span></span>  

<span data-ttu-id="04775-200">Значения , `addend1` и `addend2` выглядеть `sum` подозрительно.</span><span class="sxs-lookup"><span data-stu-id="04775-200">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="04775-201">Значения завернуты в кавычках.</span><span class="sxs-lookup"><span data-stu-id="04775-201">The values are wrapped in quotes.</span></span>  <span data-ttu-id="04775-202">Эти цитаты означают, что это значение — строка, которая является хорошей гипотезой для объяснения причины ошибки.</span><span class="sxs-lookup"><span data-stu-id="04775-202">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="04775-203">Дополнительные сведения о ситуации.</span><span class="sxs-lookup"><span data-stu-id="04775-203">Gather more information about the situation.</span></span>  <span data-ttu-id="04775-204">DevTools предоставляет множество инструментов для изучения переменных значений.</span><span class="sxs-lookup"><span data-stu-id="04775-204">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-panel"></a><span data-ttu-id="04775-205">Метод 1. Панель Область</span><span class="sxs-lookup"><span data-stu-id="04775-205">Method 1: The Scope panel</span></span>  

<span data-ttu-id="04775-206">При паузе на строке кода панель **Scope** отображает локальные и глобальные переменные, которые в настоящее время определены, а также значение каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="04775-206">If you pause on a line of code, the **Scope** panel displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="04775-207">В нем также отображаются переменные закрытия, как это применимо.</span><span class="sxs-lookup"><span data-stu-id="04775-207">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="04775-208">Дважды щелкните переменное значение, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="04775-208">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="04775-209">Если не приостанавливать строку кода, панель **Scope** пуста.</span><span class="sxs-lookup"><span data-stu-id="04775-209">If you don't pause on a line of code, the **Scope** panel is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="04775-211">Область **области**</span><span class="sxs-lookup"><span data-stu-id="04775-211">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="04775-212">Метод 2. Просмотр выражений</span><span class="sxs-lookup"><span data-stu-id="04775-212">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="04775-213">Панель **"Выражения часов"** позволяет отслеживать значения переменных со временем.</span><span class="sxs-lookup"><span data-stu-id="04775-213">The **Watch Expressions** panel lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="04775-214">Как следует из названия, **выражения watch не** ограничиваются переменными.</span><span class="sxs-lookup"><span data-stu-id="04775-214">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="04775-215">Вы можете хранить любое допустимые выражения JavaScript в **watch Expression.**</span><span class="sxs-lookup"><span data-stu-id="04775-215">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="04775-216">Попробуйте.</span><span class="sxs-lookup"><span data-stu-id="04775-216">Try it now.</span></span>  

1.  <span data-ttu-id="04775-217">Выберите панель **Watch.**</span><span class="sxs-lookup"><span data-stu-id="04775-217">Choose the **Watch** panel.</span></span>  
1.  <span data-ttu-id="04775-218">Выберите **Add Expression** \( Add Expression ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="04775-218">Choose **Add Expression** \(![Add Expression](../media/add-expression-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="04775-219">Введите `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="04775-219">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="04775-220">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="04775-220">Select `Enter`.</span></span>  <span data-ttu-id="04775-221">DevTools показывает `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="04775-221">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="04775-222">Значение справа от толстой кишки является результатом выражения часов.</span><span class="sxs-lookup"><span data-stu-id="04775-222">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="04775-223">В области **Выражение вахты** \(внизу справа\) на следующем рисунке отображается выражение `typeof sum` watch.</span><span class="sxs-lookup"><span data-stu-id="04775-223">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="04775-224">Если окно DevTools большое, \*\*\*\* то справа над точкой точки **breakpoints** слушателя событий находится области Выражение часов.</span><span class="sxs-lookup"><span data-stu-id="04775-224">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Панель "Выражение часов"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="04775-226">Панель **"Выражение часов"**</span><span class="sxs-lookup"><span data-stu-id="04775-226">The **Watch Expression** panel</span></span>  
:::image-end:::  

<span data-ttu-id="04775-227">Как подозревается, оценивается как `sum` строка, когда она должна быть номером.</span><span class="sxs-lookup"><span data-stu-id="04775-227">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="04775-228">Теперь подтвержден тип значения является причиной ошибки.</span><span class="sxs-lookup"><span data-stu-id="04775-228">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="04775-229">Метод 3. Консоль</span><span class="sxs-lookup"><span data-stu-id="04775-229">Method 3: The Console</span></span>  

<span data-ttu-id="04775-230">Консоль **позволяет** просматривать сообщения, а также использовать ее для оценки произвольных `console.log()` заявлений JavaScript.</span><span class="sxs-lookup"><span data-stu-id="04775-230">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="04775-231">Для отладки можно использовать \*\*\*\* консоль для тестирования возможных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="04775-231">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="04775-232">Попробуйте.</span><span class="sxs-lookup"><span data-stu-id="04775-232">Try it now.</span></span>  

1.  <span data-ttu-id="04775-233">Если средство **консоли** закрыто, выберите `Escape` его открытие.</span><span class="sxs-lookup"><span data-stu-id="04775-233">If the **Console** tool is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="04775-234">**Консольный** инструмент открывается в нижней панели окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="04775-234">The **Console** tool opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="04775-235">В консоли **введите** `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="04775-235">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="04775-236">Заявление, в котором инструмент приостанавлитована, находится на строке кода, где `addend1` `addend2` и находятся в области.</span><span class="sxs-lookup"><span data-stu-id="04775-236">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="04775-237">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="04775-237">Select `Enter`.</span></span>  <span data-ttu-id="04775-238">DevTools оценивает заявление и отпечатки, что является результатом, который вы `6` ожидаете, что демо-версия будет производиться.</span><span class="sxs-lookup"><span data-stu-id="04775-238">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Средство Консоли после оценки parseInt (addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="04775-240">Средство **Консоли** после оценки</span><span class="sxs-lookup"><span data-stu-id="04775-240">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="04775-241">Шаг 7. Применение исправления</span><span class="sxs-lookup"><span data-stu-id="04775-241">Step 7: Apply a fix</span></span>  

<span data-ttu-id="04775-242">Если вы нашли исправление ошибки, попробуйте исправить его, отредактив код и повторив демонстрацию.</span><span class="sxs-lookup"><span data-stu-id="04775-242">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="04775-243">Вы можете изменить код JavaScript непосредственно в пользовательском интерфейсе DevTools и применить исправление.</span><span class="sxs-lookup"><span data-stu-id="04775-243">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="04775-244">Попробуйте.</span><span class="sxs-lookup"><span data-stu-id="04775-244">Try it now.</span></span>  

1.  <span data-ttu-id="04775-245">Выберите **выполнение скрипта** Resume \. ![ Возобновление выполнения ](../media/resume-script-run-icon.msft.png) скрипта \).</span><span class="sxs-lookup"><span data-stu-id="04775-245">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="04775-246">В **редакторе кода**замените строку 32, `var sum = addend1 + addend2` с `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="04775-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="04775-247">Чтобы `Control` + `S` сохранить изменения, выберите \(Windows, Linux\) `Command` + `S` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="04775-247">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="04775-248">Выберите **деактивационные точки** разрывов \. ![ Деактивировать точки ](../media/deactivate-breakpoints-button-icon.msft.png) перерывов \).</span><span class="sxs-lookup"><span data-stu-id="04775-248">Choose **Deactivate breakpoints** \(![Deactivate breakpoints](../media/deactivate-breakpoints-button-icon.msft.png)\).</span></span>  <span data-ttu-id="04775-249">Он изменяется синим цветом, чтобы указать, что параметр активен.</span><span class="sxs-lookup"><span data-stu-id="04775-249">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="04775-250">В **то время как задаваются** точки деактивации, DevTools игнорирует все задаваемые точки.</span><span class="sxs-lookup"><span data-stu-id="04775-250">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="04775-251">Попробуйте демонстрацию с разными значениями.</span><span class="sxs-lookup"><span data-stu-id="04775-251">Try out the demo with different values.</span></span>  <span data-ttu-id="04775-252">Демо теперь вычисляется правильно.</span><span class="sxs-lookup"><span data-stu-id="04775-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="04775-253">Этот рабочий процесс применяет исправление только к коду, который запущен в браузере.</span><span class="sxs-lookup"><span data-stu-id="04775-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="04775-254">Он не исправит код для всех пользователей, которые посещают веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="04775-254">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="04775-255">Для этого необходимо исправить код, который находится на серверах.</span><span class="sxs-lookup"><span data-stu-id="04775-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="04775-256">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="04775-256">Next steps</span></span>  

<span data-ttu-id="04775-257">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="04775-257">Congratulations!</span></span>  <span data-ttu-id="04775-258">Теперь вы знаете, как сделать большую часть Microsoft Edge DevTools при отладке JavaScript.</span><span class="sxs-lookup"><span data-stu-id="04775-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="04775-259">Инструменты и методы, которые вы узнали в этой статье, могут сэкономить бесчисленные часы.</span><span class="sxs-lookup"><span data-stu-id="04775-259">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="04775-260">В этой статье вы можете найти только два способа установить точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="04775-260">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="04775-261">DevTools предлагает множество других способов, включая следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="04775-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="04775-262">Условные точки разрыва, которые срабатывает только при условии, которое вы предоставляете, является верным.</span><span class="sxs-lookup"><span data-stu-id="04775-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="04775-263">Breakpoints on caught or uncaught exceptions.</span><span class="sxs-lookup"><span data-stu-id="04775-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="04775-264">Точки взлома XHR, срабатывающие при совпадении запрашиваемого URL-адреса с подразрядом, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="04775-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="04775-265">Дополнительные сведения о том, когда и как использовать каждый тип, перейдите к паузе кода [с точками breakpoints.][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="04775-265">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="04775-266">Несколько элементов управления шагами кода не объясняются в этой статье.</span><span class="sxs-lookup"><span data-stu-id="04775-266">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="04775-267">Дополнительные сведения, перейдите [на шаг за строку кода][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="04775-267">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="04775-268">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04775-268">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с помощью точек остановок в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Шаг через код — отладка ссылок javaScript | Документы Майкрософт"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Open Demo | Glitch"  

> [!NOTE]
> <span data-ttu-id="04775-272">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04775-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="04775-273">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="04775-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="04775-275">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04775-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
