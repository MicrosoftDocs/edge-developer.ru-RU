---
description: Откройте для себя новые процессы отладки в этой всеобъемлющей ссылке на функции отладки Microsoft Edge DevTools.
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2944e054a08a901d2e1752fa7c4e48ae110f5787
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439460"
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

# <a name="javascript-debugging-reference"></a><span data-ttu-id="d259b-104">Справочник по отладке JavaScript</span><span class="sxs-lookup"><span data-stu-id="d259b-104">JavaScript debugging reference</span></span>  

<span data-ttu-id="d259b-105">Откройте для себя новые процессы отладки со следующей всеобъемлющей ссылкой на функции отладки Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d259b-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="d259b-106">Чтобы узнать основы отладки, перейдите по ссылке Начало работы с отладки [JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span><span class="sxs-lookup"><span data-stu-id="d259b-106">To learn the basics of debugging, navigate to [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span></span>  

## <a name="pause-code-with-breakpoints"></a><span data-ttu-id="d259b-107">Приостановка кода с точками остановок</span><span class="sxs-lookup"><span data-stu-id="d259b-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="d259b-108">Установите точку разрыва, чтобы вы могли приостановить работу кода в середине времени работы.</span><span class="sxs-lookup"><span data-stu-id="d259b-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="d259b-109">Чтобы узнать, как установить точки остановок, перейдите к приостановки [кода с точками breakpoints.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="d259b-109">To learn how to set breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="step-through-code"></a><span data-ttu-id="d259b-110">Шаг через код</span><span class="sxs-lookup"><span data-stu-id="d259b-110">Step through code</span></span>  

<span data-ttu-id="d259b-111">После приостановки кода перешадите его по одной строке, исследуя поток управления и значения свойств по пути.</span><span class="sxs-lookup"><span data-stu-id="d259b-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="d259b-112">Шаг за строку кода</span><span class="sxs-lookup"><span data-stu-id="d259b-112">Step over line of code</span></span>  

<span data-ttu-id="d259b-113">При остановке на строке кода, содержащей функцию, которая не относится к проблеме отладки, выберите кнопку **Step over** \( Step over \) для запуска функции, не вступая в нее. ![ ](../media/step-over-icon.msft.png)</span><span class="sxs-lookup"><span data-stu-id="d259b-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, choose the **Step over** \(![Step over](../media/step-over-icon.msft.png)\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Выберите шаг более" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="d259b-115">Выберите **шаг более**</span><span class="sxs-lookup"><span data-stu-id="d259b-115">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="d259b-116">Например, предположим, что вы отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-116">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="d259b-117">Вы приостановили. `A`</span><span class="sxs-lookup"><span data-stu-id="d259b-117">You are paused on `A`.</span></span>  <span data-ttu-id="d259b-118">После выбора **Step over,** DevTools выполняет весь код в функции, которую вы переступили, которая `B` является и `C` .</span><span class="sxs-lookup"><span data-stu-id="d259b-118">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="d259b-119">Затем DevTools приостанавливается. `D`</span><span class="sxs-lookup"><span data-stu-id="d259b-119">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="d259b-120">Шаг в строку кода</span><span class="sxs-lookup"><span data-stu-id="d259b-120">Step into line of code</span></span>  

<span data-ttu-id="d259b-121">При остановке на строке кода, содержащей вызов функции, связанный с проблемой отладки, выберите кнопку **Шаг** в \( Шаг в \) для дальнейшего изучения этой ![ ](../media/step-into-icon.msft.png) функции.</span><span class="sxs-lookup"><span data-stu-id="d259b-121">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into](../media/step-into-icon.msft.png)\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Выберите шаг в" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="d259b-123">Выберите **шаг в**</span><span class="sxs-lookup"><span data-stu-id="d259b-123">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="d259b-124">Например, предположим, что вы отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-124">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="d259b-125">Вы приостановили. `A`</span><span class="sxs-lookup"><span data-stu-id="d259b-125">You are paused on `A`.</span></span>  <span data-ttu-id="d259b-126">После выбора **Шаг в,** DevTools запускает эту строку кода, а затем останавливается `B` на .</span><span class="sxs-lookup"><span data-stu-id="d259b-126">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="d259b-127">Выход из строки кода</span><span class="sxs-lookup"><span data-stu-id="d259b-127">Step out of line of code</span></span>  

<span data-ttu-id="d259b-128">При остановке внутри функции, не связанной с проблемой отладки, выберите кнопку **Step out** \( Step out \) для запуска остальной части кода ![ ](../media/step-out-icon.msft.png) функции.</span><span class="sxs-lookup"><span data-stu-id="d259b-128">When paused inside of a function that is not related to the problem you are debugging, choose the **Step out** \(![Step out](../media/step-out-icon.msft.png)\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Выберите шаг" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="d259b-130">Выберите **шаг**</span><span class="sxs-lookup"><span data-stu-id="d259b-130">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="d259b-131">Например, предположим, что вы отладка следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-131">For example, suppose you are debugging the following code snippet.</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="d259b-132">Вы приостановили. `A`</span><span class="sxs-lookup"><span data-stu-id="d259b-132">You are paused on `A`.</span></span>  <span data-ttu-id="d259b-133">После выбора **Шаг,** DevTools запускает остальную часть кода в , который находится только в этом примере, а `getName()` затем останавливается на `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="d259b-133">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="d259b-134">Запустите весь код до определенной строки</span><span class="sxs-lookup"><span data-stu-id="d259b-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="d259b-135">При отладки длинной функции может быть много кода, не связанного с проблемой отладки.</span><span class="sxs-lookup"><span data-stu-id="d259b-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="d259b-136">Вы можете выбрать шаг через все строки, но это утомительно.</span><span class="sxs-lookup"><span data-stu-id="d259b-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="d259b-137">Вы можете установить точку разлома строки кода на интересуемой строке, а затем выбрать кнопку **Выполнение** скриптов резюме \. Выполнение скриптов возобновления \) но существует более быстрый ![ ](../media/resume-script-run-icon.msft.png) способ.</span><span class="sxs-lookup"><span data-stu-id="d259b-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) button, but there is a faster way.</span></span>  

<span data-ttu-id="d259b-138">Наведите курсор на строку кода, в которой вас интересует, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Продолжить здесь**.</span><span class="sxs-lookup"><span data-stu-id="d259b-138">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="d259b-139">DevTools выполняет весь код до этой точки, а затем останавливается на этой строке.</span><span class="sxs-lookup"><span data-stu-id="d259b-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Выберите Продолжить здесь" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="d259b-141">Выберите **Продолжить здесь**</span><span class="sxs-lookup"><span data-stu-id="d259b-141">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="d259b-142">Перезапуск верхней функции стека вызовов</span><span class="sxs-lookup"><span data-stu-id="d259b-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="d259b-143">Чтобы остановиться на первой строке верхней функции в стеке вызовов, \*\*\*\* приостановив работу на строке кода, наведите курсор в любом месте области стек вызовов, откройте контекстное меню \(правой кнопкой мыши\) и выберите перезапуск кадров **.**</span><span class="sxs-lookup"><span data-stu-id="d259b-143">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart Frame**.</span></span>  <span data-ttu-id="d259b-144">Верхней функцией является последняя функция, которая была запустить.</span><span class="sxs-lookup"><span data-stu-id="d259b-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="d259b-145">Следующий фрагмент кода является примером для пошаговое решение.</span><span class="sxs-lookup"><span data-stu-id="d259b-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="d259b-146">Вы приостановили. `A`</span><span class="sxs-lookup"><span data-stu-id="d259b-146">You are paused on `A`.</span></span>  <span data-ttu-id="d259b-147">После выбора **перезапуска кадра,** вы должны быть приостановлены, никогда не задав точку разлома или `B` выбрав выполнение **скрипта Резюме**.</span><span class="sxs-lookup"><span data-stu-id="d259b-147">After choosing **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Выбор кадра перезагрузки" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="d259b-149">Выбор **кадра перезагрузки**</span><span class="sxs-lookup"><span data-stu-id="d259b-149">Choose **Restart Frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="d259b-150">Время возобновления запуска сценария</span><span class="sxs-lookup"><span data-stu-id="d259b-150">Resume script runtime</span></span>  

<span data-ttu-id="d259b-151">Чтобы продолжить время выполнения после паузы скрипта, выберите кнопку **"Выполнение** скрипта ![ резюме"\. ](../media/resume-script-run-icon.msft.png)</span><span class="sxs-lookup"><span data-stu-id="d259b-151">To continue the runtime after a pause of your script, choose the **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) button.</span></span>  <span data-ttu-id="d259b-152">DevTools запускает сценарий до следующей точки перерыва, если таковые есть.</span><span class="sxs-lookup"><span data-stu-id="d259b-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Выбор выполнения скрипта Resume" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="d259b-154">Выбор **выполнения скрипта Resume**</span><span class="sxs-lookup"><span data-stu-id="d259b-154">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="d259b-155">Время запуска сценария force</span><span class="sxs-lookup"><span data-stu-id="d259b-155">Force script runtime</span></span>  

<span data-ttu-id="d259b-156">Чтобы игнорировать все точки разлома и заставить скрипт возобновить работу, выберите и удерживайте кнопку Выполнение скрипта резюме **\(** Выполнение скрипта резюме \) и выберите кнопку Выполнение сценария Force \( Принудительное выполнение скрипта ![ ](../media/resume-script-run-icon.msft.png) \*\*\*\* ![ ](../media/force-script-run-icon.msft.png) \) .</span><span class="sxs-lookup"><span data-stu-id="d259b-156">To ignore all breakpoints and force your script to resume running, choose and hold the **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) button and then choose the **Force script execution** \(![Force script execution](../media/force-script-run-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Выбор выполнения сценария Force" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="d259b-158">Выбор **выполнения сценария Force**</span><span class="sxs-lookup"><span data-stu-id="d259b-158">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="d259b-159">Изменение контекста потока</span><span class="sxs-lookup"><span data-stu-id="d259b-159">Change thread context</span></span>  

<span data-ttu-id="d259b-160">При работе с веб-работниками или сотрудниками служб выберите контекст, указанный в области **Threads,** чтобы перейти к этому контексту.</span><span class="sxs-lookup"><span data-stu-id="d259b-160">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="d259b-161">Значок синей стрелки представляет, какой контекст выбран в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d259b-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Области threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="d259b-163">Области **threads**</span><span class="sxs-lookup"><span data-stu-id="d259b-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="d259b-164">Например, предположим, что в основном скрипте и скрипте сотрудника службы вы приостановили паузу на точке разрыва.</span><span class="sxs-lookup"><span data-stu-id="d259b-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="d259b-165">Необходимо просмотреть локальные и глобальные свойства для контекста сотрудника службы, но панель **Источников** показывает основной контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="d259b-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="d259b-166">Выбрав в записи сотрудника службы в области **Threads,** вы сможете перейти на этот контекст.</span><span class="sxs-lookup"><span data-stu-id="d259b-166">By choosing on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <a name="view-and-edit-local-closure-and-global-properties"></a><span data-ttu-id="d259b-167">Просмотр и редактирование локальных, закрытий и глобальных свойств</span><span class="sxs-lookup"><span data-stu-id="d259b-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="d259b-168">Останавливаясь на строке кода, используйте область **Область** для просмотра и редактирования значений свойств и переменных в локальных, закрытии и глобальных сферах.</span><span class="sxs-lookup"><span data-stu-id="d259b-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="d259b-169">Дважды щелкните значение свойства, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="d259b-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="d259b-170">Свойства, которые не могут быть засеяны, серые.</span><span class="sxs-lookup"><span data-stu-id="d259b-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="d259b-172">Область **области**</span><span class="sxs-lookup"><span data-stu-id="d259b-172">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="view-the-current-call-stack"></a><span data-ttu-id="d259b-173">Просмотр текущего стека вызовов</span><span class="sxs-lookup"><span data-stu-id="d259b-173">View the current call stack</span></span>  

<span data-ttu-id="d259b-174">Остановив на строке кода, используйте области **стек** вызовов, чтобы просмотреть стек вызовов, который получил вас к этой точке.</span><span class="sxs-lookup"><span data-stu-id="d259b-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="d259b-175">Выберите запись, чтобы перейти к строке кода, в которой была вызвана эта функция.</span><span class="sxs-lookup"><span data-stu-id="d259b-175">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="d259b-176">Значок синей стрелки представляет функцию, которую в настоящее время выделяет DevTools.</span><span class="sxs-lookup"><span data-stu-id="d259b-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Области стек вызовов" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="d259b-178">Области **стек** вызовов</span><span class="sxs-lookup"><span data-stu-id="d259b-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d259b-179">Если на строке кода не приостанавливали паузу, области **стек** вызовов пусты.</span><span class="sxs-lookup"><span data-stu-id="d259b-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="d259b-180">Трассировка копирования стека</span><span class="sxs-lookup"><span data-stu-id="d259b-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="d259b-181">чтобы скопировать текущий стек вызовов в \*\*\*\* буфер обмена, наведите курсор в любом месте области Стек вызовов, откройте контекстное меню \(правой кнопкой мыши\) и выберите трассировку **стека скопировки**.</span><span class="sxs-lookup"><span data-stu-id="d259b-181">to copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Выбор трассировки стека копирования" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="d259b-183">Выбор **трассировки стека копирования**</span><span class="sxs-lookup"><span data-stu-id="d259b-183">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="d259b-184">В качестве примера вывода приводится следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="d259b-185">Игнорировать сценарий или шаблон сценариев</span><span class="sxs-lookup"><span data-stu-id="d259b-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="d259b-186">Пометить сценарий как код библиотеки, если вы хотите игнорировать этот сценарий при отладки.</span><span class="sxs-lookup"><span data-stu-id="d259b-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="d259b-187">При обозначении кода Библиотеки сценарий заслоняется в области **стеков** вызовов, и вы никогда не вступите в функции скрипта при проступке кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="d259b-188">Следующий фрагмент кода является примером для пошаговое решение.</span><span class="sxs-lookup"><span data-stu-id="d259b-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="d259b-189">— это сторонная библиотека, которую вы доверяете.</span><span class="sxs-lookup"><span data-stu-id="d259b-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="d259b-190">Если вы уверены, что проблема отладки не связана с сторонней библиотекой, имеет смысл пометить сценарий как код **библиотеки.**</span><span class="sxs-lookup"><span data-stu-id="d259b-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="d259b-191">Пометить сценарий как код библиотеки из области редактора</span><span class="sxs-lookup"><span data-stu-id="d259b-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="d259b-192">Выполните следующие действия, чтобы пометить сценарий **как код библиотеки** из области **редактора.**</span><span class="sxs-lookup"><span data-stu-id="d259b-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="d259b-193">Откройте файл.</span><span class="sxs-lookup"><span data-stu-id="d259b-193">Open the file.</span></span>  
1.  <span data-ttu-id="d259b-194">Наведите курсор в любом месте и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="d259b-194">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="d259b-195">Выберите **Mark в качестве кода библиотеки.**</span><span class="sxs-lookup"><span data-stu-id="d259b-195">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из области редактора" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="d259b-197">Пометить сценарий **как код библиотеки** из области **редактора**</span><span class="sxs-lookup"><span data-stu-id="d259b-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="d259b-198">Пометить сценарий как код библиотеки из области стек вызовов</span><span class="sxs-lookup"><span data-stu-id="d259b-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="d259b-199">Выполните следующие действия, чтобы пометить сценарий как **код библиотеки** из области **стек** вызовов.</span><span class="sxs-lookup"><span data-stu-id="d259b-199">Complete the following actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="d259b-200">Наведите курсор на функцию из скрипта и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="d259b-200">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="d259b-201">Выберите **Mark в качестве кода библиотеки.**</span><span class="sxs-lookup"><span data-stu-id="d259b-201">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из области стек вызовов" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="d259b-203">Пометить сценарий **как код библиотеки** из области **стек** вызовов</span><span class="sxs-lookup"><span data-stu-id="d259b-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="d259b-204">Пометить сценарий как код библиотеки из параметров</span><span class="sxs-lookup"><span data-stu-id="d259b-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="d259b-205">Выполните следующие действия, чтобы отметить один сценарий или шаблон сценариев из **параметров.**</span><span class="sxs-lookup"><span data-stu-id="d259b-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="d259b-206">Open [Settings][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="d259b-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="d259b-207">Перейдите к **параметру кода Библиотеки.**</span><span class="sxs-lookup"><span data-stu-id="d259b-207">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="d259b-208">Выберите **шаблон Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d259b-208">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="d259b-209">Введите имя сценария или шаблон regex имен скриптов, чтобы пометить код **библиотеки.**</span><span class="sxs-lookup"><span data-stu-id="d259b-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="d259b-210">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="d259b-210">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из параметров" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="d259b-212">Пометить сценарий **как код библиотеки** из **параметров**</span><span class="sxs-lookup"><span data-stu-id="d259b-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="d259b-213">Запуск фрагментов кода отлаговки с любой страницы</span><span class="sxs-lookup"><span data-stu-id="d259b-213">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="d259b-214">Если вы снова и снова работает один и тот же код отлаговки в консоли, рассмотрите фрагменты.</span><span class="sxs-lookup"><span data-stu-id="d259b-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="d259b-215">Фрагменты — это сценарии времени запуска, которые вы пишете, сохраняете и запускаете в DevTools.</span><span class="sxs-lookup"><span data-stu-id="d259b-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="d259b-216">Чтобы узнать больше, перейдите к [запуску фрагментов кода с любой страницы][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="d259b-216">To learn more, navigate to [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets].</span></span>  

## <a name="watch-the-values-of-custom-javascript-expressions"></a><span data-ttu-id="d259b-217">Просмотр значений пользовательских выражений JavaScript</span><span class="sxs-lookup"><span data-stu-id="d259b-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="d259b-218">Используйте области **Watch** для просмотра значений пользовательских выражений.</span><span class="sxs-lookup"><span data-stu-id="d259b-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="d259b-219">Вы можете просмотреть любое допустимые выражения JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d259b-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Области Часы" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="d259b-221">Области **Часы**</span><span class="sxs-lookup"><span data-stu-id="d259b-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="d259b-222">Выберите **кнопку Add Expression** \( ![ Add Expression ](../media/add-expression-icon.msft.png) \) для создания нового выражения часов.</span><span class="sxs-lookup"><span data-stu-id="d259b-222">Choose the **Add Expression** \(![Add Expression](../media/add-expression-icon.msft.png)\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="d259b-223">Выберите **кнопку Обновление** ![ \( Обновление \) для обновления ](../media/refresh-icon.msft.png) значений всех существующих выражений.</span><span class="sxs-lookup"><span data-stu-id="d259b-223">Choose the **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="d259b-224">Значения автоматически обновляются при прошагове кода.</span><span class="sxs-lookup"><span data-stu-id="d259b-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="d259b-225">Наведите курсор на выражение и выберите кнопку **Delete Expression** ![ \( Delete Expression ](../media/delete-expression-icon.msft.png) \) для ее удаления.</span><span class="sxs-lookup"><span data-stu-id="d259b-225">Hover on an expression and choose the **Delete Expression** \(![Delete Expression](../media/delete-expression-icon.msft.png)\) button to delete it.</span></span>  

## <a name="make-a-minified-file-readable"></a><span data-ttu-id="d259b-226">Сделать минированную папку читаемой</span><span class="sxs-lookup"><span data-stu-id="d259b-226">Make a minified file readable</span></span>  

<span data-ttu-id="d259b-227">Выберите **кнопку Format** \( Format \) для того, чтобы сделать этот файл ![ ](../media/format-icon.msft.png) понятным для человека.</span><span class="sxs-lookup"><span data-stu-id="d259b-227">Choose the **Format** \(![Format](../media/format-icon.msft.png)\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Кнопка "Формат"" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="d259b-229">Кнопка **"Формат"**</span><span class="sxs-lookup"><span data-stu-id="d259b-229">The **Format** button</span></span>  
:::image-end:::  

## <a name="edit-a-script"></a><span data-ttu-id="d259b-230">Изменение сценария</span><span class="sxs-lookup"><span data-stu-id="d259b-230">Edit a script</span></span>  

<span data-ttu-id="d259b-231">При исправлении ошибки часто необходимо проверить некоторые изменения в коде JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d259b-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="d259b-232">Вам не нужно вносить изменения во внешнем редакторе или IDE, а затем обновлять страницу.</span><span class="sxs-lookup"><span data-stu-id="d259b-232">You do not need to make the changes in an external editor or IDE and then refresh the page.</span></span>  <span data-ttu-id="d259b-233">Вы можете изменить сценарий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="d259b-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="d259b-234">Выполните следующие действия для редактирования сценария.</span><span class="sxs-lookup"><span data-stu-id="d259b-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="d259b-235">Откройте файл в области **редактора** панели **Источники.**</span><span class="sxs-lookup"><span data-stu-id="d259b-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="d259b-236">Внести изменения в **области редактора.**</span><span class="sxs-lookup"><span data-stu-id="d259b-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="d259b-237">Выберите `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения.</span><span class="sxs-lookup"><span data-stu-id="d259b-237">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="d259b-238">DevTools заплатит весь JS-файл в javaScript-движок Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d259b-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Области редактора" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="d259b-240">Области **редактора**</span><span class="sxs-lookup"><span data-stu-id="d259b-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="disable-javascript"></a><span data-ttu-id="d259b-241">Отключение JavaScript</span><span class="sxs-lookup"><span data-stu-id="d259b-241">Disable JavaScript</span></span>  

<span data-ttu-id="d259b-242">Перейдите [к отключению JavaScript с помощью Microsoft Edge DevTools.][DevToolsJavascriptDisable]</span><span class="sxs-lookup"><span data-stu-id="d259b-242">Navigate to [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d259b-243">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d259b-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Приостановка кода с помощью точек остановок в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptDisable]: ./disable.md "Отключить JavaScript с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptGetStarted]: ./index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptSnippets]: ./snippets.md "Запустите фрагменты JavaScript на любой странице с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="d259b-249">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d259b-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d259b-250">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="d259b-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d259b-252">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d259b-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
