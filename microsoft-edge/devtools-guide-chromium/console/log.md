---
description: Узнайте, как занося сообщения в консоль.
title: Начало работы с ведением журнала сообщений в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2f91f1847bf5469e8106edc21553172fc06db9ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231113"
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

# <span data-ttu-id="900f8-104">Начало работы с ведением журнала сообщений в консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-104">Get Started With Logging Messages In The Console</span></span>  

<span data-ttu-id="900f8-105">В этом интерактивном руководстве показано, как занося сообщения в журнал и фильтровать их в консоли [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="900f8-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения в консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="900f8-107">Сообщения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="900f8-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="900f8-108">Это руководство предназначено для завершения по порядку.</span><span class="sxs-lookup"><span data-stu-id="900f8-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="900f8-109">Предполагается, что вы понимаете основы веб-разработки, такие как использование JavaScript для добавления интерактивности на страницу.</span><span class="sxs-lookup"><span data-stu-id="900f8-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="900f8-110">Настройка демонстрации и DevTools</span><span class="sxs-lookup"><span data-stu-id="900f8-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="900f8-111">Это руководство предназначено для того, чтобы вы могли открыть демонстрацию и попробовать все процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="900f8-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="900f8-112">Когда вы будете физически следовать этому пути, скорее всего, позже запомните эти процессы.</span><span class="sxs-lookup"><span data-stu-id="900f8-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="900f8-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span><span class="sxs-lookup"><span data-stu-id="900f8-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="900f8-114">Примеры журнала консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="900f8-115">Сконцентрируем демонстрацию и выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\), чтобы открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="900f8-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="900f8-116">По умолчанию DevTools открывается справа от демонстрации.</span><span class="sxs-lookup"><span data-stu-id="900f8-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools откроется справа от демонстрации" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="900f8-118">DevTools откроется справа от демонстрации</span><span class="sxs-lookup"><span data-stu-id="900f8-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="900f8-119">[Закрепление DevTools в нижней части окна.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="900f8-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools, закрепленный в нижней части демонстрации" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="900f8-121">DevTools, закрепленный в нижней части демонстрации</span><span class="sxs-lookup"><span data-stu-id="900f8-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="900f8-122">[Undock DevTools в отдельное окно.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="900f8-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Браузер в отдельном окне" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="900f8-124">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="900f8-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="900f8-125">[Undock DevTools в отдельное окно.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="900f8-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Отсоединая отсоединая от devTools в отдельном окне" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="900f8-127">Отсоединая отсоединая от devTools в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="900f8-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="900f8-128">Просмотр сообщений, зарегистрированных на JavaScript</span><span class="sxs-lookup"><span data-stu-id="900f8-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="900f8-129">Большинство сообщений, отображаемого \*\*\*\* в консоли, приходят от веб-разработчиков, которые написали JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="900f8-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="900f8-130">Цель этого раздела — познакомить вас с различными типами сообщений, которые вы, скорее всего, будете рассматривать в **консоли,** и объяснить, как вы можете самостоятельно вносить в журнал каждый тип сообщения из собственного кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="900f8-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="900f8-131">В **демонстрации выберите** кнопку "Сведения журнала".</span><span class="sxs-lookup"><span data-stu-id="900f8-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="900f8-132">регистрируется в консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Консоль после выбора данных журнала" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="900f8-134">Консоль **после** выбора данных **журнала**</span><span class="sxs-lookup"><span data-stu-id="900f8-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-135">Рядом с сообщением в консоли выберите `Hello, Console!` **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="900f8-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="900f8-136">Откроется панель источников и выделена строка кода, из-за чего сообщение было зарегистрировано в консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="900f8-137">Сообщение занося в журнал, когда был занося в журнал JavaScript `console.log('Hello, Console!')` страницы.</span><span class="sxs-lookup"><span data-stu-id="900f8-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools открывает панель источников после выбора log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="900f8-139">DevTools открывает панель **источников** после выбора</span><span class="sxs-lookup"><span data-stu-id="900f8-139">DevTools opens the **Sources** panel after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-140">Перейдите к консоли **с** помощью любого из следующих процессов:</span><span class="sxs-lookup"><span data-stu-id="900f8-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="900f8-141">Выберите **вкладку "Консоль".**</span><span class="sxs-lookup"><span data-stu-id="900f8-141">Choose the **Console** tab.</span></span>  
    *   <span data-ttu-id="900f8-142">Выберите `Control` + `[` \(Windows, Linux\) или `Command` + `[` \(macOS\), \*\*\*\* пока панель консоли не будет в фокусе.</span><span class="sxs-lookup"><span data-stu-id="900f8-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** panel is in focus.</span></span>  
    *   <span data-ttu-id="900f8-143">[Откройте меню команд,][DevToolsCommandMenu]введите команду "Показать консольную `Console` **панель",** а затем выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="900f8-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="900f8-144">В **демонстрации выберите кнопку** "Предупреждение журнала".</span><span class="sxs-lookup"><span data-stu-id="900f8-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="900f8-145">регистрируется в **консоли.**</span><span class="sxs-lookup"><span data-stu-id="900f8-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="900f8-146">Сообщения в таком формате являются предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="900f8-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Консоль после выбора предупреждения журнала" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="900f8-148">Консоль **после** выбора предупреждения **журнала**</span><span class="sxs-lookup"><span data-stu-id="900f8-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="900f8-149">Если вы хотите отобразить код, который вызвал определенное внесение сообщения в журнал, выберите сценарий \(например, \), чтобы просмотреть код, который вызвал форматирование `log.js:12` сообщения.</span><span class="sxs-lookup"><span data-stu-id="900f8-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="900f8-150">Choose the **Expand** \( ![ Expand ][ImageExpandIcon] \) icon in front of `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="900f8-150">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="900f8-151">DevTools отображает [трассировку стека][WikiStackTrace] перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="900f8-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Трассировка стека" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="900f8-153">Трассировка стека</span><span class="sxs-lookup"><span data-stu-id="900f8-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="900f8-154">Трассировка стека говорит о том, что выполняется функция с именем, которая, в свою `logWarning` очередь, выполняет функцию с именем `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="900f8-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="900f8-155">Другими словами, первый запрос находится в нижней части трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="900f8-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="900f8-156">Вы можете в любое время занося трассировки стека в `console.trace()` журнал.</span><span class="sxs-lookup"><span data-stu-id="900f8-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="900f8-157">Choose **Log Error**.</span><span class="sxs-lookup"><span data-stu-id="900f8-157">Choose **Log Error**.</span></span>  <span data-ttu-id="900f8-158">Занося в журнал следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="900f8-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщение об ошибке" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="900f8-160">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="900f8-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-161">Choose **Log Table**.</span><span class="sxs-lookup"><span data-stu-id="900f8-161">Choose **Log Table**.</span></span>  <span data-ttu-id="900f8-162">Таблица о неявных исполнителях записируется **в**консоль.</span><span class="sxs-lookup"><span data-stu-id="900f8-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="900f8-163">Столбец `birthday` заполняется только для одной строки.</span><span class="sxs-lookup"><span data-stu-id="900f8-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="900f8-164">Просмотрите код, чтобы определить, почему это так.</span><span class="sxs-lookup"><span data-stu-id="900f8-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Таблица в консоли" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="900f8-166">Таблица **в** консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-167">Выберите **группу журналов.**</span><span class="sxs-lookup"><span data-stu-id="900f8-167">Choose **Log Group**.</span></span>  <span data-ttu-id="900f8-168">Под меткой сгруппировка имен 4 -х- и хламов, где ведется `Adolescent Irradiated Espionage Tortoises` группировка.</span><span class="sxs-lookup"><span data-stu-id="900f8-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Группа сообщений в консоли" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="900f8-170">Группа сообщений в **консоли**</span><span class="sxs-lookup"><span data-stu-id="900f8-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-171">Choose **Log Custom**.</span><span class="sxs-lookup"><span data-stu-id="900f8-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="900f8-172">Сообщение с красной границей и синим фоном регистрируется в консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщение с пользовательским форматированием в консоли" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="900f8-174">Сообщение с пользовательским форматированием **в** консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="900f8-175">Основная идея заключается в том, что при регистрации сообщений в консоли из JavaScript используется один из `console` методов.</span><span class="sxs-lookup"><span data-stu-id="900f8-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="900f8-176">Каждый метод форматирование сообщений по-разному.</span><span class="sxs-lookup"><span data-stu-id="900f8-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="900f8-177">Существует еще больше методов, чем показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="900f8-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="900f8-178">В этом руководстве показано, как изучить остальные методы.</span><span class="sxs-lookup"><span data-stu-id="900f8-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="900f8-179">Просмотр сообщений, зарегистрированных браузером</span><span class="sxs-lookup"><span data-stu-id="900f8-179">View messages logged by the browser</span></span>  

<span data-ttu-id="900f8-180">Браузер также записи сообщений в консоль.</span><span class="sxs-lookup"><span data-stu-id="900f8-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="900f8-181">Обычно это происходит при проблеме со страницей.</span><span class="sxs-lookup"><span data-stu-id="900f8-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="900f8-182">Choose **Cause 404**.</span><span class="sxs-lookup"><span data-stu-id="900f8-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="900f8-183">Браузер записи в журнал кода состояния HTTP сетевой ошибки, так как Код JavaScript страницы пытался получить файл, `404` который не существует.</span><span class="sxs-lookup"><span data-stu-id="900f8-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ошибка 404 в консоли" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="900f8-185">Ошибка `404` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-186">Choose **Cause Error**.</span><span class="sxs-lookup"><span data-stu-id="900f8-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="900f8-187">Браузер занося в журнал ненагрузку, так как JavaScript пытается обновить узел `TypeError` DOM, который не существует.</span><span class="sxs-lookup"><span data-stu-id="900f8-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError в консоли" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="900f8-189">A `TypeError` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="900f8-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-190">Выберите в **качестве входного** параметра "Уровни журнала" и включите параметр **"Подробно",** если он отключен.</span><span class="sxs-lookup"><span data-stu-id="900f8-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="900f8-191">Подробнее о фильтрации вы узнаете в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="900f8-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="900f8-192">Это необходимо сделать, чтобы убедиться, что следующее сообщение, занося в журнал, будет видимым.</span><span class="sxs-lookup"><span data-stu-id="900f8-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="900f8-193">Если выпадание уровней по умолчанию отключено, может потребоваться закрыть **боковую панель** консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="900f8-194">Фильтрация по источнику сообщений ниже для получения дополнительных сведений о **боковой панели** консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Включение уровня подробного журнала" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="900f8-196">Включение уровня подробного журнала</span><span class="sxs-lookup"><span data-stu-id="900f8-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-197">Выберите **"Причина нарушения".**</span><span class="sxs-lookup"><span data-stu-id="900f8-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="900f8-198">Страница в течение нескольких секунд становится неотвечивой, а затем браузер записи сообщения в `[Violation] 'click' handler took 3000ms` консоль.</span><span class="sxs-lookup"><span data-stu-id="900f8-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="900f8-199">Точная длительность может отличаться.</span><span class="sxs-lookup"><span data-stu-id="900f8-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Нарушение в консоли" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="900f8-201">Нарушение в **консоли**</span><span class="sxs-lookup"><span data-stu-id="900f8-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="900f8-202">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="900f8-202">Filter messages</span></span>  

<span data-ttu-id="900f8-203">На некоторых веб-страницы, \*\*\*\* на которые вы просматриваете консоль, переполнили сообщения.</span><span class="sxs-lookup"><span data-stu-id="900f8-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="900f8-204">DevTools предоставляет множество различных способов фильтрации сообщений, не соответствующих задаче.</span><span class="sxs-lookup"><span data-stu-id="900f8-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="900f8-205">Фильтрация по уровню журнала</span><span class="sxs-lookup"><span data-stu-id="900f8-205">Filter by log level</span></span>  

<span data-ttu-id="900f8-206">Каждому `console` методу назначена степень серьезности: `Verbose` , , , или `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="900f8-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="900f8-207">Например, `console.log()` это сообщение уровня, а `Info` сообщение `console.error()` `Error` уровня.</span><span class="sxs-lookup"><span data-stu-id="900f8-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="900f8-208">Выберите в **поле "Уровни журнала"** и отключите **ошибки.**</span><span class="sxs-lookup"><span data-stu-id="900f8-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="900f8-209">Уровень отключается, если рядом с ней больше нет контрольного знака.</span><span class="sxs-lookup"><span data-stu-id="900f8-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="900f8-210">Сообщения `Error` уровня исчезают.</span><span class="sxs-lookup"><span data-stu-id="900f8-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Отключение сообщений уровня ошибки в консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="900f8-212">Отключение сообщений уровня ошибки в **консоли**</span><span class="sxs-lookup"><span data-stu-id="900f8-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-213">Снова выберите **"Уровни** журнала" и снова вйдите в **"Ошибки".**</span><span class="sxs-lookup"><span data-stu-id="900f8-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="900f8-214">Сообщения `Error` уровня снова появляются.</span><span class="sxs-lookup"><span data-stu-id="900f8-214">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="900f8-215">Фильтрация по тексту</span><span class="sxs-lookup"><span data-stu-id="900f8-215">Filter by text</span></span>  

<span data-ttu-id="900f8-216">Если вы хотите просматривать только сообщения с точной строкой, введите эту строку в **текстовое** поле фильтра.</span><span class="sxs-lookup"><span data-stu-id="900f8-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="900f8-217">Введите `Dave` в **текстовое поле фильтра.**</span><span class="sxs-lookup"><span data-stu-id="900f8-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="900f8-218">Все сообщения, которые не включают `Dave` строку, скрыты.</span><span class="sxs-lookup"><span data-stu-id="900f8-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="900f8-219">Вы также можете просмотреть `Adolescent Irradiated Espionage Tortoises` метку.</span><span class="sxs-lookup"><span data-stu-id="900f8-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="900f8-220">Это ошибка.</span><span class="sxs-lookup"><span data-stu-id="900f8-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Фильтрация всех сообщений, не включаемая в список Ю." lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="900f8-222">Фильтрация всех сообщений, которые не включены</span><span class="sxs-lookup"><span data-stu-id="900f8-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-223">Удалите `Dave` из **текстового окна фильтра.**</span><span class="sxs-lookup"><span data-stu-id="900f8-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="900f8-224">Все сообщения снова появляются.</span><span class="sxs-lookup"><span data-stu-id="900f8-224">All the messages reappear.</span></span>  

### <span data-ttu-id="900f8-225">Фильтрация по регулярному выражению</span><span class="sxs-lookup"><span data-stu-id="900f8-225">Filter by regular expression</span></span>  

<span data-ttu-id="900f8-226">Если вы хотите показать все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение.][MDNRegularExpressions]</span><span class="sxs-lookup"><span data-stu-id="900f8-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="900f8-227">Введите `/^[AH]/` в **текстовое поле фильтра.**</span><span class="sxs-lookup"><span data-stu-id="900f8-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="900f8-228">Введите этот шаблон [в RegExr,][|::ref1::|Main] чтобы объяснить, что он делает.</span><span class="sxs-lookup"><span data-stu-id="900f8-228">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Фильтрация сообщений, не совпадающих с шаблоном" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="900f8-230">Фильтрация сообщений, не совпадающих с шаблоном</span><span class="sxs-lookup"><span data-stu-id="900f8-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-231">Удалите `/^[AH]/` из **текстового окна фильтра.**</span><span class="sxs-lookup"><span data-stu-id="900f8-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="900f8-232">Все сообщения снова будут видны.</span><span class="sxs-lookup"><span data-stu-id="900f8-232">All messages are visible again.</span></span>  

### <span data-ttu-id="900f8-233">Фильтрация по источнику сообщений</span><span class="sxs-lookup"><span data-stu-id="900f8-233">Filter by message source</span></span>  

<span data-ttu-id="900f8-234">Если вы хотите просматривать только сообщения, которые поступили с определенного URL-адреса, используйте **боковую панель.**</span><span class="sxs-lookup"><span data-stu-id="900f8-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="900f8-235">Choose **Show Console Sidebar** \( ![ Show Console Sidebar ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="900f8-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Боковая панель" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="900f8-237">Боковая панель</span><span class="sxs-lookup"><span data-stu-id="900f8-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-238">Выберите **значок "Развернуть"** рядом с числом ![ ][ImageExpandIcon] сообщений.</span><span class="sxs-lookup"><span data-stu-id="900f8-238">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="900f8-239">На следующем рисунке число сообщений указано как **13 сообщений.**</span><span class="sxs-lookup"><span data-stu-id="900f8-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="900f8-240">На **боковой панели** показан список URL-адресов, которые привели к записи сообщений в журнал.</span><span class="sxs-lookup"><span data-stu-id="900f8-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="900f8-241">Например, `log.js` вызвано 11 сообщений.</span><span class="sxs-lookup"><span data-stu-id="900f8-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Просмотр источника сообщений на боковой панели" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="900f8-243">Просмотр источника сообщений на боковой панели</span><span class="sxs-lookup"><span data-stu-id="900f8-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="900f8-244">Фильтрация по пользовательским сообщениям</span><span class="sxs-lookup"><span data-stu-id="900f8-244">Filter by user messages</span></span>  

<span data-ttu-id="900f8-245">Ранее при выборе log **Info**сценарий, именуемой для регистрации `console.log('Hello, Console!')` сообщения в консоли.</span><span class="sxs-lookup"><span data-stu-id="900f8-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="900f8-246">Сообщения, зарегистрированные на JavaScript, такие как это, называются **пользовательскими**сообщениями.</span><span class="sxs-lookup"><span data-stu-id="900f8-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="900f8-247">Напротив, при выборе **причины 404**браузер регистрирует сообщение уровня о том, что запрашиваемого ресурса `Error` не удалось найти.</span><span class="sxs-lookup"><span data-stu-id="900f8-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="900f8-248">Такие сообщения считаются сообщениями **браузера.**</span><span class="sxs-lookup"><span data-stu-id="900f8-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="900f8-249">Используйте **боковую панель для** фильтрации сообщений браузера и только для показа сообщений пользователей.</span><span class="sxs-lookup"><span data-stu-id="900f8-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="900f8-250">Выберите **9 пользовательских сообщений.**</span><span class="sxs-lookup"><span data-stu-id="900f8-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="900f8-251">Сообщения браузера скрыты.</span><span class="sxs-lookup"><span data-stu-id="900f8-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Фильтрация сообщений браузера" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="900f8-253">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="900f8-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="900f8-254">Выберите **13 сообщений,** чтобы снова показать все сообщения.</span><span class="sxs-lookup"><span data-stu-id="900f8-254">Choose **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="900f8-255">Использование консоли наряду с любой другой панелью</span><span class="sxs-lookup"><span data-stu-id="900f8-255">Use the Console alongside any other panel</span></span>  

<span data-ttu-id="900f8-256">Что делать, если вы редактируете стили, но вам нужно быстро проверить журнал консоли?</span><span class="sxs-lookup"><span data-stu-id="900f8-256">What if you are editing styles, but you need to quickly check the Console log for something?</span></span>  <span data-ttu-id="900f8-257">Используйте drawer.</span><span class="sxs-lookup"><span data-stu-id="900f8-257">Use the Drawer.</span></span>  

1.  <span data-ttu-id="900f8-258">Выберите **вкладку "Элементы".**</span><span class="sxs-lookup"><span data-stu-id="900f8-258">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="900f8-259">Выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="900f8-259">Select `Escape`.</span></span>  <span data-ttu-id="900f8-260">Откроется вкладка "Консоль" **в drawer.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="900f8-260">The **Console** tab of the **Drawer** opens.</span></span>  <span data-ttu-id="900f8-261">Он содержит все функции панели консоли, которые вы использовали в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="900f8-261">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Вкладка "Консоль" в "Ящике"" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="900f8-263">Вкладка **"Консоль"** в **"Ящике"**</span><span class="sxs-lookup"><span data-stu-id="900f8-263">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   Navigate to [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   Navigate to [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## <span data-ttu-id="900f8-264">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="900f8-264">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md "Справочник по консоли | Документы Майкрософт"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с ведением журнала сообщений | Временный сбой"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедия"  
> [!NOTE]
> <span data-ttu-id="900f8-274">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="900f8-274">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="900f8-275">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/console/log) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="900f8-275">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="900f8-277">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="900f8-277">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
