---
description: Узнайте, как запустить JavaScript в консоли.
title: Начало работы с запуском JavaScript в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ecd1a2fffb311990b6e743e99d038f1f2a519ee4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231092"
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

# <span data-ttu-id="5c975-104">Начало работы с запуском JavaScript в консоли</span><span class="sxs-lookup"><span data-stu-id="5c975-104">Get Started With Running JavaScript In The Console</span></span>  

<span data-ttu-id="5c975-105">В этом интерактивном руководстве показано, как запустить \*\*\*\* JavaScript в консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5c975-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="5c975-106">Дополнительные сведения о регистрации сообщений в консоли **можно**найти в окне "Начало работы [с сообщениями журналов".][DevToolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="5c975-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="5c975-107">Дополнительные сведения о приостановки кода JavaScript и пошаговом его пошаговом переходе к началу работы с [отладки JavaScript.][DevToolsJavascriptIndex]</span><span class="sxs-lookup"><span data-stu-id="5c975-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="5c975-109">Консоль \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5c975-109">The **Console**</span></span>  
:::image-end:::  

## <span data-ttu-id="5c975-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="5c975-110">Overview</span></span>  

<span data-ttu-id="5c975-111">Консоль **—** это [REPL,][WikiReadEvalPrintLoop]который обозначает чтение, оценку, печать и цикл.</span><span class="sxs-lookup"><span data-stu-id="5c975-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="5c975-112">Он считывает в него код JavaScript, оценивает код, выпечатает результат [выражения,][2alityExpressionsVersusStatements]а затем возвращается к первому шагу.</span><span class="sxs-lookup"><span data-stu-id="5c975-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="5c975-113">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="5c975-113">Set up DevTools</span></span>  

<span data-ttu-id="5c975-114">Это руководство предназначено для вас, чтобы открыть демонстрацию и попробовать все процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="5c975-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="5c975-115">Когда вы будете физически следовать этому пути, скорее всего, позже запомните эти процессы.</span><span class="sxs-lookup"><span data-stu-id="5c975-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="5c975-116">Выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\) для открытия **консоли.**</span><span class="sxs-lookup"><span data-stu-id="5c975-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="5c975-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span><span class="sxs-lookup"><span data-stu-id="5c975-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="5c975-118">Пример кода Javascript консоли</span><span class="sxs-lookup"><span data-stu-id="5c975-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Страница "Пример кода javaScript консоли" слева и DevTools справа" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="5c975-120">Страница "Пример кода javaScript консоли" слева и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="5c975-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5c975-121">Просмотр и изменение JavaScript или DOM страницы</span><span class="sxs-lookup"><span data-stu-id="5c975-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="5c975-122">При создании или отладке страницы часто полезно запускать в \*\*\*\* консоли утверждения, чтобы изменить внешний вид или запуск страницы.</span><span class="sxs-lookup"><span data-stu-id="5c975-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="5c975-123">Обратите внимание на текст на кнопке.</span><span class="sxs-lookup"><span data-stu-id="5c975-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="5c975-124">Введите `document.getElementById('hello').textContent = 'Hello, Console!'` в **консоли** и выберите `Enter` для оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="5c975-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="5c975-125">Обратите внимание, как изменяется текст внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="5c975-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Внешний вид консоли после оценки выражения" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="5c975-127">Внешний вид **консоли** после оценки выражения</span><span class="sxs-lookup"><span data-stu-id="5c975-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="5c975-128">Под кодом, который вы вычисляли, вы видите `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="5c975-128">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="5c975-129">Напомню 4 шага REPL: чтение, оценка, печать, цикл.</span><span class="sxs-lookup"><span data-stu-id="5c975-129">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="5c975-130">После оценки кода rePL печатает результат выражения.</span><span class="sxs-lookup"><span data-stu-id="5c975-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="5c975-131">Это `"Hello, Console!"` должен быть результат оценки. `document.getElementById('hello').textContent = 'Hello, Console!'`</span><span class="sxs-lookup"><span data-stu-id="5c975-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="5c975-132">Запуск произвольного Кода JavaScript, не связанного со страницей</span><span class="sxs-lookup"><span data-stu-id="5c975-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="5c975-133">Иногда вам просто нужна функциональная возможность кода, в которой можно протестировать код или попробовать новые функции JavaScript, которые вам незнакомы.</span><span class="sxs-lookup"><span data-stu-id="5c975-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="5c975-134">Консоль **идеально** подходит для экспериментов такого рода.</span><span class="sxs-lookup"><span data-stu-id="5c975-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="5c975-135">Введите `5 + 15` в консоли и выберите для `Enter` оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="5c975-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="5c975-136">Консоль выпечатает результат выражения под кодом.</span><span class="sxs-lookup"><span data-stu-id="5c975-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="5c975-137">На следующем рисунке **после** оценки выражения в консоли должен отображаться результат.</span><span class="sxs-lookup"><span data-stu-id="5c975-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="5c975-138">Введите следующий код в **консоль.**</span><span class="sxs-lookup"><span data-stu-id="5c975-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="5c975-139">Попробуйте ввести его по символам, а не копировать.</span><span class="sxs-lookup"><span data-stu-id="5c975-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="5c975-140">Если вы не знакомы с синтаксисом, перейдите к определению значений по умолчанию `b=20` [для аргументов функции.][Esma6DefaultParameterValues]</span><span class="sxs-lookup"><span data-stu-id="5c975-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="5c975-141">Теперь запустите функцию, которую вы только что определили.</span><span class="sxs-lookup"><span data-stu-id="5c975-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль отображается после оценки выражений в фрагменте кода" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="5c975-143">Консоль **отображается** после оценки выражений в фрагменте кода</span><span class="sxs-lookup"><span data-stu-id="5c975-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="5c975-144">`45`оценивается, так как когда функция вызвана без второго `add` аргумента, значение по умолчанию — `b` `20` .</span><span class="sxs-lookup"><span data-stu-id="5c975-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="5c975-145">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5c975-145">Next steps</span></span>  

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="5c975-146">DevTools позволяет приостановить сценарий в середине работы.</span><span class="sxs-lookup"><span data-stu-id="5c975-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="5c975-147">Пока вы приостановлены, вы \*\*\*\* можете использовать консоль для просмотра и изменения страницы или страницы в `window` этот момент `DOM` времени.</span><span class="sxs-lookup"><span data-stu-id="5c975-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="5c975-148">Рабочий процесс создает мощный рабочий процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="5c975-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="5c975-149">Интерактивное руководство по началу работы [с отладой JavaScript.][DevToolsJavascriptIndex]</span><span class="sxs-lookup"><span data-stu-id="5c975-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="5c975-150">Консоль **также** имеет набор удобных функций, упрощающих взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="5c975-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="5c975-151">Например:</span><span class="sxs-lookup"><span data-stu-id="5c975-151">For example:</span></span>  

*   <span data-ttu-id="5c975-152">Вместо ввода `document.querySelector()` текста для выбора элемента введите `$()` .</span><span class="sxs-lookup"><span data-stu-id="5c975-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="5c975-153">Этот синтаксис навеян jQuery, но на самом деле он не является jQuery.</span><span class="sxs-lookup"><span data-stu-id="5c975-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="5c975-154">Это просто псевдоним для `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="5c975-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="5c975-155">эффективно задает точку останова в первой строке этой функции.</span><span class="sxs-lookup"><span data-stu-id="5c975-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="5c975-156">возвращает массив, содержащий ключи указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5c975-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="5c975-157">Дополнительные сведения об удобных функциях можно найти в справочнике [по API консоли.][DevToolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="5c975-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="5c975-158">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c975-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журнала сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочник по консоли | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API консольных utilities | Документы Майкрософт"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и выражения в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — расширенная обработка параметров — ECMAScript 6 — новые функции: обзор & сравнения"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Пример кода Javascript консоли | Временный сбой"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Цикл read-eval-print — Википдия"  

> [!NOTE]
> <span data-ttu-id="5c975-167">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c975-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5c975-168">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/console/javascript) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5c975-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5c975-170">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5c975-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
