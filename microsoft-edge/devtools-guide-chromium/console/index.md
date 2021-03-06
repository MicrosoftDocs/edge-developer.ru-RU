---
description: Основные виды использования консоли Microsoft Edge DevTools — ведение журналов сообщений и запуск JavaScript.
title: Обзор консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399122"
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

# <a name="console-overview"></a><span data-ttu-id="5835e-104">Обзор консоли</span><span class="sxs-lookup"><span data-stu-id="5835e-104">Console overview</span></span>  

  

<span data-ttu-id="5835e-105">На этой странице рассказывается, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="5835e-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="5835e-106">Консоль **имеет** 2 основных использования: просмотр [зарегистрированных](#viewing-logged-messages) сообщений и [запуск JavaScript.](#running-javascript)</span><span class="sxs-lookup"><span data-stu-id="5835e-106">The **Console** has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <a name="viewing-logged-messages"></a><span data-ttu-id="5835e-107">Просмотр зарегистрированных сообщений</span><span class="sxs-lookup"><span data-stu-id="5835e-107">Viewing logged messages</span></span>  

<span data-ttu-id="5835e-108">Веб-разработчики часто в журнале сообщений на консоли, чтобы убедиться, что их JavaScript работает как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="5835e-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="5835e-109">Чтобы войти в журнал сообщения, вставьте выражение, как `console.log('Hello, Console!')` в javaScript.</span><span class="sxs-lookup"><span data-stu-id="5835e-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="5835e-110">Когда браузер запускает JavaScript и обрабатывает подобное выражение, браузер регистрирует сообщение в **консоли.**</span><span class="sxs-lookup"><span data-stu-id="5835e-110">When the browser runs your JavaScript and processes an expression like it, the browser logs the message to the **Console**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="5835e-111">HTML и JavaScript для страницы.</span><span class="sxs-lookup"><span data-stu-id="5835e-111">The HTML and JavaScript for the page.</span></span>  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5835e-112">На следующем рисунке консоль **отображает** результаты загрузки страницы и ожидания 3 секунды.</span><span class="sxs-lookup"><span data-stu-id="5835e-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Панель Консоли" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="5835e-114">Средство **Консоли**</span><span class="sxs-lookup"><span data-stu-id="5835e-114">The **Console** tool</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="5835e-115">Попробуйте определить, какие строки кода привели браузер к журналу сообщений.</span><span class="sxs-lookup"><span data-stu-id="5835e-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5835e-116">Веб-разработчики журнал сообщений по следующим 2 общим причинам.</span><span class="sxs-lookup"><span data-stu-id="5835e-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="5835e-117">Убедитесь, что код работает в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="5835e-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="5835e-118">Проверка значений переменных в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="5835e-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="5835e-119">Чтобы получить практический опыт ведения журнала, перейдите к [началу работы с ведением журналов сообщений.][DevtoolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="5835e-119">To get hands-on experience with logging, navigate to [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="5835e-120">Чтобы просмотреть полный список `console` методов, перейдите к ссылке [API консоли][DevToolsConsoleAPI].</span><span class="sxs-lookup"><span data-stu-id="5835e-120">To browse the full list of `console` methods, navigate to the [Console API Reference][DevToolsConsoleAPI].</span></span>  <span data-ttu-id="5835e-121">Основное различие между методами заключается в том, как отображаются данные, которые регистрируются.</span><span class="sxs-lookup"><span data-stu-id="5835e-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <a name="running-javascript"></a><span data-ttu-id="5835e-122">Запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="5835e-122">Running JavaScript</span></span>  

<span data-ttu-id="5835e-123">Консоль **также** является [rePL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="5835e-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="5835e-124">Вы можете запустить JavaScript в **консоли, чтобы** взаимодействовать со проверяемой страницей.</span><span class="sxs-lookup"><span data-stu-id="5835e-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="5835e-125">На следующем рисунке консоль **отображается** рядом с домашней страницей DevTools.</span><span class="sxs-lookup"><span data-stu-id="5835e-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Средство Консоли рядом с домашней страницей DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="5835e-127">Средство **Консоли** рядом с домашней страницей DevTools</span><span class="sxs-lookup"><span data-stu-id="5835e-127">The **Console** tool next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5835e-128">На следующем рисунке показана та же \*\*\*\* страница после использования консоли для изменения верхнего заголовка страницы.</span><span class="sxs-lookup"><span data-stu-id="5835e-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Использование консоли для изменения верхнего заголовка страницы" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="5835e-130">Использование консоли **для** изменения верхнего заголовка страницы</span><span class="sxs-lookup"><span data-stu-id="5835e-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="5835e-131">Изменение страницы из \*\*\*\* консоли возможно, так как консоль **имеет** полный доступ к [окну][MDNWindow] страницы.</span><span class="sxs-lookup"><span data-stu-id="5835e-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="5835e-132">В DevTools есть несколько функций удобства, которые упрощают проверку страницы.</span><span class="sxs-lookup"><span data-stu-id="5835e-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="5835e-133">Например, предположим, что javaScript содержит функцию под названием `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="5835e-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="5835e-134">Запуск `debug(hideModal)` приостанавливовка кода в первой строке следующего `hideModal` запуска.</span><span class="sxs-lookup"><span data-stu-id="5835e-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="5835e-135">Дополнительные сведения о полном списке полезных функций перейдите к ссылке [API консоли Utilities.][DevtoolsConsoleUtilitiesDebug]</span><span class="sxs-lookup"><span data-stu-id="5835e-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="5835e-136">При запуске JavaScript не нужно взаимодействовать со страницей.</span><span class="sxs-lookup"><span data-stu-id="5835e-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="5835e-137">Вы можете использовать **консоль для** опробовки нового кода, не связанного со страницей.</span><span class="sxs-lookup"><span data-stu-id="5835e-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="5835e-138">Например, предположим, что вы только что узнали о встроенной карте Массива JavaScript [и][MDNMap] хотите поэкспериментировать с ним.</span><span class="sxs-lookup"><span data-stu-id="5835e-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="5835e-139">Консоль **—** это хорошее место для опробовки функции.</span><span class="sxs-lookup"><span data-stu-id="5835e-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="5835e-140">Дополнительные практические опыт работы с запуском JavaScript в консоли **,** перейдите к [началу работы с запуском JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="5835e-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5835e-141">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5835e-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Справочные | Документы Майкрософт"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журнала сообщений в консоли | Документы Майкрософт"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Начало работы с запуском JavaScript в консоли | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "отлажка — справочные ссылки на API консоли | Документы Майкрософт"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Окно | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Цикл чтения-eval-print — Википедия"  

> [!NOTE]
> <span data-ttu-id="5835e-149">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5835e-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5835e-150">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="5835e-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5835e-152">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5835e-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
