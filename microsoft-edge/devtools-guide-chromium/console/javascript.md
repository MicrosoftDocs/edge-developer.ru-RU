---
description: Сведения о том, как запускать JavaScript на консоли.
title: Начало работы с JavaScript на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d31bcfbdf728e656c9a6fff882f939f8c24cd897
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993123"
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







# <span data-ttu-id="accab-104">Начало работы с JavaScript на консоли</span><span class="sxs-lookup"><span data-stu-id="accab-104">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="accab-105">В этом интерактивном учебнике показано, как запустить JavaScript на **консоли**Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="accab-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="accab-106">Дополнительные сведения о том, как записывать сообщения на **консоль**, можно найти в разделе [Начало работы с сообщениями][DevToolsConsoleLoggingMessages]в журнале.</span><span class="sxs-lookup"><span data-stu-id="accab-106">For more information about how to log messages to the **Console**, see [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="accab-107">Дополнительные сведения о том, как приостановить код JavaScript и пошагово прокручиваться по одной строке, можно найти в разделе [Начало отладки JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="accab-107">For more information about how to pause JavaScript code and step through it one line at a time, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="На консоли" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="accab-109">На **консоли**</span><span class="sxs-lookup"><span data-stu-id="accab-109">The **Console**</span></span>  
:::image-end:::  

## <span data-ttu-id="accab-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="accab-110">Overview</span></span>   

<span data-ttu-id="accab-111">**Консоль** — это [REPL][WikiReadEvalPrintLoop], который означает чтение, оценку, печать и зацикливание.</span><span class="sxs-lookup"><span data-stu-id="accab-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="accab-112">Она считывает JavaScript, который вы вводите в него, оценивает код, выводит результат [выражения][2alityExpressionsVersusStatements]и осуществляет переход к первому шагу.</span><span class="sxs-lookup"><span data-stu-id="accab-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="accab-113">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="accab-113">Set up DevTools</span></span>   

<span data-ttu-id="accab-114">Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все рабочие процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="accab-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="accab-115">После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.</span><span class="sxs-lookup"><span data-stu-id="accab-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="accab-116">`Control` + `Shift` + `J` Чтобы открыть консоль, нажмите клавиши \ (Windows \) или `Command` + `Option` + `J` \ (macOS **Console**\).</span><span class="sxs-lookup"><span data-stu-id="accab-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="accab-117">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **пример на консоли JavaScript** , чтобы открыть его в новом окне.</span><span class="sxs-lookup"><span data-stu-id="accab-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="accab-118">Пример сценария на консоли</span><span class="sxs-lookup"><span data-stu-id="accab-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Страница примера JavaScript на консоли в левой части экрана и DevTools справа" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="accab-120">Страница примера JavaScript на консоли в левой части экрана и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="accab-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="accab-121">Просмотр и изменение JavaScript или DOM страницы</span><span class="sxs-lookup"><span data-stu-id="accab-121">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="accab-122">При сборке или отладке страницы часто бывает полезно запускать инструкции на **консоли** , чтобы изменить внешний вид или выполнение страницы.</span><span class="sxs-lookup"><span data-stu-id="accab-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="accab-123">Обратите внимание на текст на кнопке.</span><span class="sxs-lookup"><span data-stu-id="accab-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="accab-124">Введите текст `document.getElementById('hello').textContent = 'Hello, Console!'` в **консоли** и нажмите клавишу `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="accab-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="accab-125">Обратите внимание на то, как изменится текст внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="accab-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Внешний вид консоли после вычисления выражения" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="accab-127">Внешний вид **консоли** после вычисления выражения</span><span class="sxs-lookup"><span data-stu-id="accab-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="accab-128">Под кодом, который вы проверили `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="accab-128">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="accab-129">Отзывайте 4 шага REPL: чтение, оценка, печать, цикл.</span><span class="sxs-lookup"><span data-stu-id="accab-129">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="accab-130">После оценки кода программа REPL выводит результат выражения.</span><span class="sxs-lookup"><span data-stu-id="accab-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="accab-131">Это `"Hello, Console!"` должно быть результатом вычисления `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="accab-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="accab-132">Запуск произвольного кода JavaScript, не связанного со страницей</span><span class="sxs-lookup"><span data-stu-id="accab-132">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="accab-133">Иногда требуется, чтобы код Песочница в том месте, где вы можете протестировать какой-либо код, или опробуйте новые возможности JavaScript, с которыми вы не знакомы.</span><span class="sxs-lookup"><span data-stu-id="accab-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="accab-134">Консоль — это идеальное место для экспериментов такого рода.</span><span class="sxs-lookup"><span data-stu-id="accab-134">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="accab-135">Введите текст `5 + 15` на консоли и нажмите клавишу `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="accab-135">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="accab-136">Консоль печатает результат выражения под кодом.</span><span class="sxs-lookup"><span data-stu-id="accab-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="accab-137">На приведенном ниже рисунке на **консоли** должны отобразиться результаты после вычисления выражения.</span><span class="sxs-lookup"><span data-stu-id="accab-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="accab-138">На **консоли**введите следующий код.</span><span class="sxs-lookup"><span data-stu-id="accab-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="accab-139">Попробуйте ввести его, а затем построчно, а не скопировав.</span><span class="sxs-lookup"><span data-stu-id="accab-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    <span data-ttu-id="accab-140">Если вы не знакомы с `b=20` синтаксисом, ознакомьтесь со сведениями [Определение значений по умолчанию для аргументов функций][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="accab-140">If you are unfamiliar with the `b=20` syntax, see [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="accab-141">Теперь запустите определенную функцию.</span><span class="sxs-lookup"><span data-stu-id="accab-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль отображается после оценки выражений в фрагменте кода." lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="accab-143">**Консоль** отображается после оценки выражений в фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="accab-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="accab-144">вычисляется `45` , так как при `add` вызове функции без второго аргумента `b` равным ему присваивается значение по умолчанию `20` .</span><span class="sxs-lookup"><span data-stu-id="accab-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="accab-145">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="accab-145">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="accab-146">DevTools позволяет приостановить выполнение сценария в центре выполнения.</span><span class="sxs-lookup"><span data-stu-id="accab-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="accab-147">Во время приостановки вы можете использовать **консоль** для просмотра и изменения `window` `DOM` страницы в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="accab-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="accab-148">Рабочий процесс обеспечивает мощный процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="accab-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="accab-149">Интерактивные учебники можно найти [в статьях Приступая к отладке JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="accab-149">For an interactive tutorial, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="accab-150">Кроме того, **консоль** имеет набор удобных функций, которые облегчают взаимодействие с страницей.</span><span class="sxs-lookup"><span data-stu-id="accab-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="accab-151">Например:</span><span class="sxs-lookup"><span data-stu-id="accab-151">For example:</span></span>  

*   <span data-ttu-id="accab-152">Вместо того `document.querySelector()` чтобы выделять элемент, введите `$()` .</span><span class="sxs-lookup"><span data-stu-id="accab-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="accab-153">Этот синтаксис имеет тот факт, что jQuery, но он не является jQuery.</span><span class="sxs-lookup"><span data-stu-id="accab-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="accab-154">Это просто псевдоним `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="accab-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="accab-155">фактически задает точку останова в первой строке этой функции.</span><span class="sxs-lookup"><span data-stu-id="accab-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="accab-156">Возвращает массив с ключами указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="accab-156">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочник по консоли | Документы Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и операторы в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — обработка расширенных параметров-ECMAScript 6 — новые возможности: Общие сведения о сравнении &"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Пример кода JavaScript на консоли | Цепь"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Read – eval — цикл печати — Википедии"  

> [!NOTE]
> <span data-ttu-id="accab-165">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="accab-165">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="accab-166">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/javascript) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="accab-166">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="accab-168">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="accab-168">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
