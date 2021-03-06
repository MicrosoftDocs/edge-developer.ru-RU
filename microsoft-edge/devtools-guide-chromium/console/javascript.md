---
description: Узнайте, как запустить JavaScript в консоли.
title: Начало работы с запуском JavaScript в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398821"
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

# <a name="get-started-with-running-javascript-in-the-console"></a><span data-ttu-id="6f647-104">Начало работы с запуском JavaScript в консоли</span><span class="sxs-lookup"><span data-stu-id="6f647-104">Get started with running JavaScript in the Console</span></span>  

<span data-ttu-id="6f647-105">В этом интерактивном учебнике показано, как запустить \*\*\*\* JavaScript в консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6f647-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="6f647-106">Дополнительные сведения о том, как вести журнал сообщений в **консоли,** перейдите по ссылке Начало работы [с ведением журнала сообщений][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="6f647-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="6f647-107">Дополнительные сведения о том, как приостановить работу кода JavaScript и пройти через него по одной строке за раз, перейдите по ссылке Начало работы с отладки [JavaScript.][DevToolsJavascriptIndex]</span><span class="sxs-lookup"><span data-stu-id="6f647-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="6f647-109">Консоль \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f647-109">The **Console**</span></span>  
:::image-end:::  

## <a name="overview"></a><span data-ttu-id="6f647-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="6f647-110">Overview</span></span>  

<span data-ttu-id="6f647-111">Консоль **—** это [REPL,][WikiReadEvalPrintLoop]которая обозначает чтение, оценку, печать и цикл.</span><span class="sxs-lookup"><span data-stu-id="6f647-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="6f647-112">Он считываю JavaScript, который в него введите, оценивает код, распечатывает результат [выражения,][2alityExpressionsVersusStatements]а затем возвращается к первому шагу.</span><span class="sxs-lookup"><span data-stu-id="6f647-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <a name="set-up-devtools"></a><span data-ttu-id="6f647-113">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="6f647-113">Set up DevTools</span></span>  

<span data-ttu-id="6f647-114">Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="6f647-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="6f647-115">Когда вы физически следуете за ними, вы с большей вероятностью запомните рабочий процесс позже.</span><span class="sxs-lookup"><span data-stu-id="6f647-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="6f647-116">Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\) для открытия **консоли.**</span><span class="sxs-lookup"><span data-stu-id="6f647-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="6f647-117">Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **консоль Javascript Example** для открытия в новом окне.</span><span class="sxs-lookup"><span data-stu-id="6f647-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="6f647-118">Пример Javascript консоли</span><span class="sxs-lookup"><span data-stu-id="6f647-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Страница Консоли JavaScript Пример слева и DevTools справа" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="6f647-120">Страница Консоли JavaScript Пример слева и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="6f647-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a><span data-ttu-id="6f647-121">Просмотр и изменение JavaScript или DOM страницы</span><span class="sxs-lookup"><span data-stu-id="6f647-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="6f647-122">При создании или отладке страницы часто полезно запускать заявления \*\*\*\* в консоли, чтобы изменить внешний вид страницы или ее запуск.</span><span class="sxs-lookup"><span data-stu-id="6f647-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="6f647-123">Обратите внимание на текст на кнопке.</span><span class="sxs-lookup"><span data-stu-id="6f647-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="6f647-124">Введите `document.getElementById('hello').textContent = 'Hello, Console!'` консоль **и** выберите `Enter` для оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="6f647-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="6f647-125">Обратите внимание, как меняется текст внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="6f647-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Внешний вид консоли после оценки выражения" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="6f647-127">Внешний вид **консоли** после оценки выражения</span><span class="sxs-lookup"><span data-stu-id="6f647-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    `"Hello, Console!"`<span data-ttu-id="6f647-128">, отображается ниже кода, который вы оценивали.</span><span class="sxs-lookup"><span data-stu-id="6f647-128">, is displayed below the code that you evaluated.</span></span>  <span data-ttu-id="6f647-129">Помните 4 шага REPL: чтение, оценка, печать, цикл.</span><span class="sxs-lookup"><span data-stu-id="6f647-129">Remember the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="6f647-130">После оценки кода rePL печатает результат выражения.</span><span class="sxs-lookup"><span data-stu-id="6f647-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="6f647-131">Так `"Hello, Console!"` должен быть результат оценки `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="6f647-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a><span data-ttu-id="6f647-132">Запустите произвольный JavaScript, не связанный со страницей</span><span class="sxs-lookup"><span data-stu-id="6f647-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="6f647-133">Иногда просто необходимо использовать игровую площадку кода, на которой можно протестировать код или опробуете новые не знакомые функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6f647-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="6f647-134">Консоль **является** идеальным местом для подобных экспериментов.</span><span class="sxs-lookup"><span data-stu-id="6f647-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="6f647-135">Введите `5 + 15` консоль и выберите для `Enter` оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="6f647-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="6f647-136">Консоль распечатает результат выражения под кодом.</span><span class="sxs-lookup"><span data-stu-id="6f647-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="6f647-137">На следующем рисунке **консоль** должна отображать результат после оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="6f647-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="6f647-138">Введите следующий код в **консоль**.</span><span class="sxs-lookup"><span data-stu-id="6f647-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="6f647-139">Попробуйте ввести его, характер по-характеру, а не копирование вклеить его.</span><span class="sxs-lookup"><span data-stu-id="6f647-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="6f647-140">Если вы не знакомы с синтаксис, перейдите к определению значений по умолчанию `b=20` [для аргументов функции][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="6f647-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="6f647-141">Теперь запустите функцию, которую вы только что определили.</span><span class="sxs-lookup"><span data-stu-id="6f647-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль отображается после оценки выражений в фрагменте кода" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="6f647-143">Консоль **отображается** после оценки выражений в фрагменте кода</span><span class="sxs-lookup"><span data-stu-id="6f647-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="6f647-144">оценивает, `45` потому что, когда `add` функция вызвана без второго аргумента, `b` по умолчанию `20` .</span><span class="sxs-lookup"><span data-stu-id="6f647-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="6f647-145">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6f647-145">Next steps</span></span>  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="6f647-146">DevTools позволяет приостановить сценарий в середине запуска.</span><span class="sxs-lookup"><span data-stu-id="6f647-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="6f647-147">В то время как вы \*\*\*\* приостановлены, вы можете использовать консоль для просмотра и изменения страницы в `window` этот момент `DOM` времени.</span><span class="sxs-lookup"><span data-stu-id="6f647-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="6f647-148">Рабочий процесс создает мощный рабочий процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="6f647-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="6f647-149">Для интерактивного учебника перейдите к [началу работы с отладки JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="6f647-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="6f647-150">Консоль **также** имеет набор функций удобства, которые упрощают взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="6f647-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="6f647-151">Например:</span><span class="sxs-lookup"><span data-stu-id="6f647-151">For example:</span></span>  

*   <span data-ttu-id="6f647-152">Вместо ввода `document.querySelector()` для выбора элемента введите `$()` .</span><span class="sxs-lookup"><span data-stu-id="6f647-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="6f647-153">Этот синтаксис вдохновлен jQuery, но на самом деле это не jQuery.</span><span class="sxs-lookup"><span data-stu-id="6f647-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="6f647-154">Это просто псевдоним для `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="6f647-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="6f647-155">фактически задает точку разрыва на первой строке этой функции.</span><span class="sxs-lookup"><span data-stu-id="6f647-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="6f647-156">возвращает массив, содержащий ключи указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f647-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="6f647-157">Дополнительные сведения о удобных функциях перейдите к ссылке [на API консоли Utilities.][DevToolsConsoleUtilities]</span><span class="sxs-lookup"><span data-stu-id="6f647-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6f647-158">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6f647-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журналов сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочные | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочные ссылки на API консоли utilities | Документы Майкрософт"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и утверждения в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — расширенная обработка параметров — ECMAScript 6 — новые функции: обзор & сравнение"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Консоль Javascript Пример | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Цикл чтения-eval-print — Википедия"  

> [!NOTE]
> <span data-ttu-id="6f647-167">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f647-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6f647-168">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/javascript) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="6f647-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6f647-170">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f647-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
