---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска и устранения ошибок JavaScript.
title: Начало отладки JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325952"
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
# <span data-ttu-id="4d378-104">Начало отладки JavaScript в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4d378-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="4d378-105">В этой статье рассказывается о базовом рабочий процессе для отладки любых проблем JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d378-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="4d378-106">Шаг 1. Воспроизведение ошибки</span><span class="sxs-lookup"><span data-stu-id="4d378-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="4d378-107">Поиск ряда действий, которые постоянно воспроизводят ошибку, всегда является первым этапом отладки.</span><span class="sxs-lookup"><span data-stu-id="4d378-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="4d378-108">Choose **Open Demo**.</span><span class="sxs-lookup"><span data-stu-id="4d378-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="4d378-109">Удерживайте `Control` \(Windows, Linux\) или \(macOS\) и откройте демонстрацию на `Command` новой вкладке браузера.</span><span class="sxs-lookup"><span data-stu-id="4d378-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="4d378-110">Открытая демонстрация</span><span class="sxs-lookup"><span data-stu-id="4d378-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="4d378-111">Введите `5` в **текстовое поле "Номер 1".**</span><span class="sxs-lookup"><span data-stu-id="4d378-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="4d378-112">Введите `1` в **текстовое поле "Номер 2".**</span><span class="sxs-lookup"><span data-stu-id="4d378-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="4d378-113">Choose **Add Number 1 and Number 2**.</span><span class="sxs-lookup"><span data-stu-id="4d378-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="4d378-114">Метка под кнопкой " `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="4d378-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="4d378-115">Результат должен быть `6` .</span><span class="sxs-lookup"><span data-stu-id="4d378-115">The result should be `6`.</span></span>  <span data-ttu-id="4d378-116">Затем исправьте ошибку добавления, которая является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4d378-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 приводит к 51, но должно быть 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="4d378-118">результаты, `51` но должны быть</span><span class="sxs-lookup"><span data-stu-id="4d378-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="4d378-119">Шаг 2. Знакомство с пользовательским интерфейсом панели источников</span><span class="sxs-lookup"><span data-stu-id="4d378-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="4d378-120">DevTools предоставляет множество различных средств для различных задач.</span><span class="sxs-lookup"><span data-stu-id="4d378-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="4d378-121">К различным задачам относятся изменение CSS, профилирование производительности загрузки страницы и отслеживание сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="4d378-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="4d378-122">Панель **источников** — это место отлаки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4d378-122">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="4d378-123">Откройте DevTools, нажав `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4d378-123">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="4d378-124">Этот ярлык открывает панель **консоли.**</span><span class="sxs-lookup"><span data-stu-id="4d378-124">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Панель консоли" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="4d378-126">**Консольный** инструмент</span><span class="sxs-lookup"><span data-stu-id="4d378-126">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4d378-127">Выберите средство **"Источники".**</span><span class="sxs-lookup"><span data-stu-id="4d378-127">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Панель источников" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="4d378-129">Панель **источников**</span><span class="sxs-lookup"><span data-stu-id="4d378-129">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4d378-130">Пользовательский **интерфейс** панели источников имеет три части.</span><span class="sxs-lookup"><span data-stu-id="4d378-130">The **Sources** panel UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="3 части пользовательского интерфейса панели источников" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="4d378-132">3 части пользовательского интерфейса **панели** источников</span><span class="sxs-lookup"><span data-stu-id="4d378-132">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="4d378-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span><span class="sxs-lookup"><span data-stu-id="4d378-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="4d378-134">Здесь перечислены все файлы, запрашиваемые веб-страницей.</span><span class="sxs-lookup"><span data-stu-id="4d378-134">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="4d378-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span><span class="sxs-lookup"><span data-stu-id="4d378-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="4d378-136">После выбора файла в **области** навигатора файлов здесь отображается его содержимое.</span><span class="sxs-lookup"><span data-stu-id="4d378-136">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="4d378-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span><span class="sxs-lookup"><span data-stu-id="4d378-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="4d378-138">Различные средства проверки JavaScript для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="4d378-138">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="4d378-139">Если окно DevTools широкое, эта области отображается справа от области **редактора** кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-139">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="4d378-140">Шаг 3. Приостановка кода с помощью точки останова</span><span class="sxs-lookup"><span data-stu-id="4d378-140">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="4d378-141">Распространенным методом отладки этого типа проблемы является вставка нескольких заявлений в код, а затем проверка значений при `console.log()` запуске сценария.</span><span class="sxs-lookup"><span data-stu-id="4d378-141">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="4d378-142">Например:</span><span class="sxs-lookup"><span data-stu-id="4d378-142">For example:</span></span>  

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

<span data-ttu-id="4d378-143">Этот метод может получить задание, но точки `console.log()` **останова** получают его быстрее.</span><span class="sxs-lookup"><span data-stu-id="4d378-143">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="4d378-144">Точка останова позволяет приостановить код в середине времени и проверить все значения в этот момент времени.</span><span class="sxs-lookup"><span data-stu-id="4d378-144">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="4d378-145">Точки останова имеют несколько преимуществ перед `console.log()` методом:</span><span class="sxs-lookup"><span data-stu-id="4d378-145">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="4d378-146">При этом необходимо вручную открыть исходный код, найти соответствующий код, вставить инструкции, а затем обновить веб-страницу, чтобы отобразить сообщения в `console.log()` `console.log()` консоли. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4d378-146">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="4d378-147">С помощью точек останова можно приостановить соответствующий код, даже не зная, как он структурирован.</span><span class="sxs-lookup"><span data-stu-id="4d378-147">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="4d378-148">В своих утверждениях необходимо явно указать каждое значение, `console.log()` которое требуется проверить.</span><span class="sxs-lookup"><span data-stu-id="4d378-148">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="4d378-149">С помощью точек останова DevTools отображает значения всех переменных на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4d378-149">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="4d378-150">Иногда переменные, влияющие на код, скрыты и скрыты.</span><span class="sxs-lookup"><span data-stu-id="4d378-150">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="4d378-151">Вкратце, точки останова могут помочь быстрее находить и исправлять ошибки, чем `console.log()` метод.</span><span class="sxs-lookup"><span data-stu-id="4d378-151">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="4d378-152">Если вернуться назад и подумать о том, как работает приложение, вы можете сделать обоснованные предположения, что неправильная сумма \( \) вычисляется в прослушивателье событий, связанном с кнопкой "Добавить `5 + 1 = 51` `click` номер 1" и **"Номер 2".**</span><span class="sxs-lookup"><span data-stu-id="4d378-152">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="4d378-153">Таким образом, возможно, вы захотите приостановить код во время, когда `click` выполняется прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="4d378-153">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="4d378-154">**Точки останова прослушиватель** событий делают именно это:</span><span class="sxs-lookup"><span data-stu-id="4d378-154">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="4d378-155">В области **отладки JavaScript** выберите точки останова прослушиватель событий, **чтобы** развернуть раздел.</span><span class="sxs-lookup"><span data-stu-id="4d378-155">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="4d378-156">DevTools открывает список расширяемых категорий событий, таких как анимация **и** **буфер обмена.**</span><span class="sxs-lookup"><span data-stu-id="4d378-156">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="4d378-157">Рядом с **категорией событий "Мышь"** выберите **"Развернуть".** ![ Значок ][ImageExpandIcon] "Развернуть" \).</span><span class="sxs-lookup"><span data-stu-id="4d378-157">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="4d378-158">DevTools открывает список событий мыши, таких как нажатие **мыши** **и мышью.**</span><span class="sxs-lookup"><span data-stu-id="4d378-158">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="4d378-159">Каждое событие имеет рядом с собой контрольный ящик.</span><span class="sxs-lookup"><span data-stu-id="4d378-159">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="4d378-160">Рядом с кнопкой мыши нажмите **этот кнопку.**</span><span class="sxs-lookup"><span data-stu-id="4d378-160">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="4d378-161">Теперь DevTools настроен на автоматическое приостановка при запуске `click` прослушиватель событий.</span><span class="sxs-lookup"><span data-stu-id="4d378-161">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Рядом с кнопкой мыши нажмите кнопку с кнопкой мыши" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="4d378-163">Рядом с кнопкой мыши нажмите кнопку с **кнопкой мыши**</span><span class="sxs-lookup"><span data-stu-id="4d378-163">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4d378-164">Снова в демонстрации выберите **"Добавить номер 1" и "Номер 2".**</span><span class="sxs-lookup"><span data-stu-id="4d378-164">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="4d378-165">DevTools приостанавлиет демонстрацию и выделяет строку кода на панели **источников.**</span><span class="sxs-lookup"><span data-stu-id="4d378-165">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="4d378-166">DevTools должен приостановиться на строке 16 в `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="4d378-166">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="4d378-167">Если вы приостанавливлиируете другую строку кода, нажмите кнопку **Resume Script Execution** \( Resume Script Execution \) до тех пор, пока не приостановим правильную ![ ][ImageResumeIcon] строку.</span><span class="sxs-lookup"><span data-stu-id="4d378-167">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4d378-168">Если вы приостановлены на другой строке, у вас есть расширение браузера, которое регистрирует прослушиватель событий на каждой веб-странице, `click` которую вы посещаете.</span><span class="sxs-lookup"><span data-stu-id="4d378-168">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="4d378-169">Вы были приостановлены в `click` прослушивателье расширения.</span><span class="sxs-lookup"><span data-stu-id="4d378-169">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="4d378-170">Если вы используете режим InPrivate для просмотра в закрытом **режиме,** который отключает все расширения, вы можете видеть, что вы каждый раз приостанавливаете нужную строку кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-170">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="4d378-171">**Точки останова прослушиватель** событий — это лишь один из многих типов точек останова, доступных в DevTools.</span><span class="sxs-lookup"><span data-stu-id="4d378-171">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="4d378-172">Запомните все типы, чтобы помочь вам отлачивать различные сценарии как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="4d378-172">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="4d378-173">Шаг 4. Пошаговая пошаговая по</span><span class="sxs-lookup"><span data-stu-id="4d378-173">Step 4: Step through the code</span></span>  

<span data-ttu-id="4d378-174">Одна из распространенных причин ошибок — запуск скрипта в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="4d378-174">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="4d378-175">Пошаговая поша</span><span class="sxs-lookup"><span data-stu-id="4d378-175">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="4d378-176">Вы проходите по одной строке за раз, чтобы точно понять, где именно работает ваш код, в другом порядке, чем вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="4d378-176">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="4d378-177">Попробуйте его сейчас:</span><span class="sxs-lookup"><span data-stu-id="4d378-177">Try it now:</span></span>  

1.  <span data-ttu-id="4d378-178">Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4d378-178">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="4d378-179">DevTools выполняет следующий код, не вступая в него.</span><span class="sxs-lookup"><span data-stu-id="4d378-179">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="4d378-180">DevTools пропускает несколько строк кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-180">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="4d378-181">Это происходит потому, что оценивается как false, поэтому блок кода для этого заявления `inputsAreEmpty()` `if` не будет работать.</span><span class="sxs-lookup"><span data-stu-id="4d378-181">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="4d378-182">On the Sources panel of DevTools, choose **Step into next function call** \( Step into next function call \) to step through the **runtime** ![ of the ][ImageIntoIcon] `updateLabel()` function, one line at a time.</span><span class="sxs-lookup"><span data-stu-id="4d378-182">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="4d378-183">Пошаговая проверка по одной строке — это основная идея пошагового кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-183">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="4d378-184">Если вы посмотрите на код в, вы увидите, что ошибка, вероятно, находится `get-started.js` где-то в `updateLabel()` функции.</span><span class="sxs-lookup"><span data-stu-id="4d378-184">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="4d378-185">Вместо того чтобы перешаговое использование каждой строки кода, вы можете использовать другой тип точки останова, чтобы приостановить код ближе к возможному расположению ошибки.</span><span class="sxs-lookup"><span data-stu-id="4d378-185">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="4d378-186">Шаг 5. Настройка точки останова кода</span><span class="sxs-lookup"><span data-stu-id="4d378-186">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="4d378-187">Точки останова кода — это наиболее распространенный тип точки останова.</span><span class="sxs-lookup"><span data-stu-id="4d378-187">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="4d378-188">Когда вы получаете определенную строку кода, который нужно приостановить, используйте точку останова кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-188">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="4d378-189">Посмотрите на последнюю строку кода `updateLabel()` в:</span><span class="sxs-lookup"><span data-stu-id="4d378-189">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="4d378-190">Слева номер этой строки кода отображается как **34**.</span><span class="sxs-lookup"><span data-stu-id="4d378-190">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="4d378-191">Выберите **строку 34**.</span><span class="sxs-lookup"><span data-stu-id="4d378-191">Choose line **34**.</span></span>  <span data-ttu-id="4d378-192">DevTools помещает красный значок слева от **34**.</span><span class="sxs-lookup"><span data-stu-id="4d378-192">DevTools puts a red icon to the left of **34**.</span></span>  <span data-ttu-id="4d378-193">Красный значок указывает, что в этой строке находится точка останова кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-193">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="4d378-194">DevTools всегда приостанавливается перед запуском этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="4d378-194">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="4d378-195">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4d378-195">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="4d378-196">Сценарий продолжает работать, пока не достигнет строки 33.</span><span class="sxs-lookup"><span data-stu-id="4d378-196">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="4d378-197">В строках 31, 32 и 33 DevTools печатает значения справа от двоеточия в `addend1` `addend2` каждой `sum` строке.</span><span class="sxs-lookup"><span data-stu-id="4d378-197">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools приостанавливов в точке останова кода в строке 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="4d378-199">DevTools приостанавливов в точке останова кода в строке 34</span><span class="sxs-lookup"><span data-stu-id="4d378-199">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="4d378-200">Шаг 6. Проверка значений переменных</span><span class="sxs-lookup"><span data-stu-id="4d378-200">Step 6: Check variable values</span></span>  

<span data-ttu-id="4d378-201">Значения `addend1` ,, `addend2` и выглядят `sum` подозрительными.</span><span class="sxs-lookup"><span data-stu-id="4d378-201">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="4d378-202">Значения завернуты в кавычках.</span><span class="sxs-lookup"><span data-stu-id="4d378-202">The values are wrapped in quotes.</span></span>  <span data-ttu-id="4d378-203">Кавычка означает, что значение является строкой, которая является хорошей догмой, чтобы объяснить причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="4d378-203">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="4d378-204">Соберем дополнительные сведения о ситуации.</span><span class="sxs-lookup"><span data-stu-id="4d378-204">Gather more information about the situation.</span></span>  <span data-ttu-id="4d378-205">DevTools предоставляет множество средств для проверки значений переменных.</span><span class="sxs-lookup"><span data-stu-id="4d378-205">DevTools provides many tools for examining variable values.</span></span>  

### <span data-ttu-id="4d378-206">Метод 1. Область области</span><span class="sxs-lookup"><span data-stu-id="4d378-206">Method 1: The Scope pane</span></span>  

<span data-ttu-id="4d378-207">Если приостановить строку кода, \*\*\*\* область области отображает локальные и глобальные переменные, которые определены в настоящее время, а также значение каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="4d378-207">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="4d378-208">Кроме того, отображаются переменные закрытия, если применимо.</span><span class="sxs-lookup"><span data-stu-id="4d378-208">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="4d378-209">Дважды щелкните переменное значение, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="4d378-209">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="4d378-210">Если не приостановить строку кода, область области **будет** пустой.</span><span class="sxs-lookup"><span data-stu-id="4d378-210">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="4d378-212">Область **области**</span><span class="sxs-lookup"><span data-stu-id="4d378-212">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="4d378-213">Метод 2. Просмотр выражений</span><span class="sxs-lookup"><span data-stu-id="4d378-213">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="4d378-214">В **области контрольных выражений** можно отслеживать значения переменных с течением времени.</span><span class="sxs-lookup"><span data-stu-id="4d378-214">The **Watch Expressions** pane lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="4d378-215">Как следует из названия, **watch Expressions** не ограничиваются переменными.</span><span class="sxs-lookup"><span data-stu-id="4d378-215">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="4d378-216">Вы можете сохранить любое допустимые выражения JavaScript в watch **Expression.**</span><span class="sxs-lookup"><span data-stu-id="4d378-216">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="4d378-217">Попробуйте его сейчас.</span><span class="sxs-lookup"><span data-stu-id="4d378-217">Try it now.</span></span>  

1.  <span data-ttu-id="4d378-218">Выберите в **области** "Часы".</span><span class="sxs-lookup"><span data-stu-id="4d378-218">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="4d378-219">Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4d378-219">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="4d378-220">Введите `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="4d378-220">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="4d378-221">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4d378-221">Select `Enter`.</span></span>  <span data-ttu-id="4d378-222">Показывает DevTools `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="4d378-222">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="4d378-223">Значение справа от двоеточия является результатом выражения watch.</span><span class="sxs-lookup"><span data-stu-id="4d378-223">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="4d378-224">В области **"Watch Expression"** (Выражение в нижнем правом) на следующем рисунке отображается выражение "Watch". `typeof sum`</span><span class="sxs-lookup"><span data-stu-id="4d378-224">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="4d378-225">Если окно DevTools имеет \*\*\*\* большой размер, то над точкими останова прослушиватель событий находится справа над этой области. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4d378-225">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="The Watch Expression pane" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="4d378-227">The **Watch Expression** pane</span><span class="sxs-lookup"><span data-stu-id="4d378-227">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="4d378-228">Как есть `sum` подозрение, он оценивается как строка, когда она должна быть числом.</span><span class="sxs-lookup"><span data-stu-id="4d378-228">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="4d378-229">Теперь вы подтверждаете, что причиной ошибки является тип значения.</span><span class="sxs-lookup"><span data-stu-id="4d378-229">You now confirmed value type is the cause of the bug.</span></span>  

### <span data-ttu-id="4d378-230">Метод 3: консоль</span><span class="sxs-lookup"><span data-stu-id="4d378-230">Method 3: The Console</span></span>  

<span data-ttu-id="4d378-231">Консоль **позволяет** просматривать сообщения, и вы также можете использовать ее для оценки произвольных `console.log()` заявлений JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4d378-231">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="4d378-232">Для отладки можно использовать \*\*\*\* консоль для проверки возможных исправлений ошибок.</span><span class="sxs-lookup"><span data-stu-id="4d378-232">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="4d378-233">Попробуйте его сейчас.</span><span class="sxs-lookup"><span data-stu-id="4d378-233">Try it now.</span></span>  

1.  <span data-ttu-id="4d378-234">Если **консольный** ящик закрыт, `Escape` выберите, чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="4d378-234">If the **Console** drawer is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="4d378-235">В **нижней** панели окна DevTools откроется консольный ящик.</span><span class="sxs-lookup"><span data-stu-id="4d378-235">The **Console** drawer opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="4d378-236">В консоли **введите** `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="4d378-236">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="4d378-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span><span class="sxs-lookup"><span data-stu-id="4d378-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="4d378-238">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4d378-238">Select `Enter`.</span></span>  <span data-ttu-id="4d378-239">DevTools оценивает заявление и печатает, что является результатом, который вы `6` ожидаете, что демонстрация будет производить.</span><span class="sxs-lookup"><span data-stu-id="4d378-239">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Консольный ящик после оценки parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="4d378-241">**Консольный** ящик после оценки</span><span class="sxs-lookup"><span data-stu-id="4d378-241">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="4d378-242">Шаг 7. Применение исправления</span><span class="sxs-lookup"><span data-stu-id="4d378-242">Step 7: Apply a fix</span></span>  

<span data-ttu-id="4d378-243">Если вы нашли исправление ошибки, попробуйте исправить ошибку, отредактировать код и повторно перезахлить демонстрацию.</span><span class="sxs-lookup"><span data-stu-id="4d378-243">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="4d378-244">Вы можете изменить код JavaScript непосредственно в пользовательском интерфейсе DevTools и применить исправление.</span><span class="sxs-lookup"><span data-stu-id="4d378-244">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="4d378-245">Попробуйте его сейчас.</span><span class="sxs-lookup"><span data-stu-id="4d378-245">Try it now.</span></span>  

1.  <span data-ttu-id="4d378-246">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4d378-246">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="4d378-247">В **редакторе кода**замените строку 32 `var sum = addend1 + addend2` , на `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="4d378-247">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="4d378-248">Выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\) для сохранения изменения.</span><span class="sxs-lookup"><span data-stu-id="4d378-248">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="4d378-249">Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4d378-249">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="4d378-250">Он изменяется синим цветом, чтобы указать, что параметр активен.</span><span class="sxs-lookup"><span data-stu-id="4d378-250">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="4d378-251">Хотя **точки останова** отключены, DevTools игнорирует все задаваемые точки останова.</span><span class="sxs-lookup"><span data-stu-id="4d378-251">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="4d378-252">Попробуйте демонстрацию с разными значениями.</span><span class="sxs-lookup"><span data-stu-id="4d378-252">Try out the demo with different values.</span></span>  <span data-ttu-id="4d378-253">Демонстрация вычисляется правильно.</span><span class="sxs-lookup"><span data-stu-id="4d378-253">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="4d378-254">Этот рабочий процесс применяет исправление только к коду, который работает в браузере.</span><span class="sxs-lookup"><span data-stu-id="4d378-254">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="4d378-255">Он не исправит код для всех пользователей, посетив вашу веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="4d378-255">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="4d378-256">Для этого необходимо исправить код, который находится на серверах.</span><span class="sxs-lookup"><span data-stu-id="4d378-256">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="4d378-257">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="4d378-257">Next steps</span></span>  

<span data-ttu-id="4d378-258">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="4d378-258">Congratulations!</span></span>  <span data-ttu-id="4d378-259">Теперь вы знаете, как сделать все возможное для Microsoft Edge DevTools при отладке JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4d378-259">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="4d378-260">Инструменты и методы, которые вы узнали в этой статье, могут сэкономить много времени.</span><span class="sxs-lookup"><span data-stu-id="4d378-260">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="4d378-261">В этой статье вы знаете только два способа установить точки останова.</span><span class="sxs-lookup"><span data-stu-id="4d378-261">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="4d378-262">DevTools предлагает множество других способов, включая следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="4d378-262">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="4d378-263">Условные точки останова, которые запускаются только при условии, которое вы предоставляете, является истинным.</span><span class="sxs-lookup"><span data-stu-id="4d378-263">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="4d378-264">Точки останова для перехваченных или неподтверченных исключений.</span><span class="sxs-lookup"><span data-stu-id="4d378-264">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="4d378-265">Точки останова XHR, которые запускаются, когда запрашиваемого URL-адреса соответствует подстроки, которые вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="4d378-265">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="4d378-266">Для получения дополнительных сведений о том, когда и как использовать каждый тип, перейдите к приостановки [кода с точками останова.][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="4d378-266">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="4d378-267">Пара элементов управления пошаговым кодом не объясняется в этой статье.</span><span class="sxs-lookup"><span data-stu-id="4d378-267">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="4d378-268">Для получения дополнительных сведений перейдите [к пошаговой строке кода.][DevtoolsJavascriptReferenceStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="4d378-268">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="4d378-269">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4d378-269">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с точками останова в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Пошаговое пошаговое название кода: справочные данные по отладки JavaScript | Документы Майкрософт"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Открытие демонстрационных | Временный сбой"  

> [!NOTE]
> <span data-ttu-id="4d378-273">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4d378-273">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4d378-274">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4d378-274">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4d378-276">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4d378-276">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
