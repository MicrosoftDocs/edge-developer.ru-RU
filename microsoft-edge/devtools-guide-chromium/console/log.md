---
description: Узнайте, как войти сообщения в консоль.
title: Начало работы с ведением журналов сообщений в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e2ea1a8327dd2a591e067b69198c4509b2abcb2d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399171"
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

# <a name="get-started-with-logging-messages-in-the-console"></a><span data-ttu-id="52204-104">Начало работы с ведением журналов сообщений в консоли</span><span class="sxs-lookup"><span data-stu-id="52204-104">Get started with logging messages in the Console</span></span>  

<span data-ttu-id="52204-105">В этом интерактивном учебнике показано, как журнал и фильтрация сообщений в [консоли Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="52204-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения в консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="52204-107">Сообщения в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="52204-108">Этот учебник предназначен для завершения в порядке.</span><span class="sxs-lookup"><span data-stu-id="52204-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="52204-109">Предполагается, что вы понимаете основы веб-разработки, например использование JavaScript для добавления интерактивности на страницу.</span><span class="sxs-lookup"><span data-stu-id="52204-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <a name="set-up-the-demo-and-devtools"></a><span data-ttu-id="52204-110">Настройка демонстрации и DevTools</span><span class="sxs-lookup"><span data-stu-id="52204-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="52204-111">Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="52204-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="52204-112">Когда вы физически следуете за ними, вы с большей вероятностью запомните рабочий процесс позже.</span><span class="sxs-lookup"><span data-stu-id="52204-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="52204-113">Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) \*\*\*\* и выберите примеры журнала консоли для открытия на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="52204-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="52204-114">Примеры журнала консоли</span><span class="sxs-lookup"><span data-stu-id="52204-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="52204-115">Уделяем внимание демонстрации, а затем выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\) для открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="52204-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="52204-116">По умолчанию DevTools открывается справа от демонстрации.</span><span class="sxs-lookup"><span data-stu-id="52204-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools открывается справа от демонстрации" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="52204-118">DevTools открывается справа от демонстрации</span><span class="sxs-lookup"><span data-stu-id="52204-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="52204-119">[Dock DevTools в нижней части окна.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="52204-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools, пристыкованные к нижней части демонстрации" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="52204-121">DevTools, пристыкованные к нижней части демонстрации</span><span class="sxs-lookup"><span data-stu-id="52204-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="52204-122">[Undock DevTools в отдельное окно][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="52204-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Браузер в отдельном окне" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="52204-124">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="52204-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="52204-125">[Undock DevTools в отдельное окно][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="52204-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools, отсоединая в отдельном окне" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="52204-127">DevTools, отсоединая в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="52204-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a><span data-ttu-id="52204-128">Просмотр сообщений, в журнале из JavaScript</span><span class="sxs-lookup"><span data-stu-id="52204-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="52204-129">Большинство сообщений, отображаемого \*\*\*\* в консоли, приходят от веб-разработчиков, которые написали JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="52204-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="52204-130">Цель этого раздела состоит в том, чтобы познакомить вас с различными типами сообщений, которые можно просмотреть в **консоли,** и объяснить, как можно самостоятельно войти в каждый тип сообщения из собственного JavaScript.</span><span class="sxs-lookup"><span data-stu-id="52204-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="52204-131">Выберите **кнопку Log Info** в демонстрации.</span><span class="sxs-lookup"><span data-stu-id="52204-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="52204-132">получает войти в консоль.</span><span class="sxs-lookup"><span data-stu-id="52204-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Консоль после выбора информации журнала" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="52204-134">Консоль **после** выбора информации **журнала**</span><span class="sxs-lookup"><span data-stu-id="52204-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-135">Рядом с `Hello, Console!` сообщением в консоли выберите **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="52204-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="52204-136">Панель Источников открывает и выделяет строку кода, из-за чего сообщение было занесно в консоль.</span><span class="sxs-lookup"><span data-stu-id="52204-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="52204-137">Сообщение было в журнале, когда javaScript страницы побежал `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="52204-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools открывает средство Sources после выбора log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="52204-139">DevTools открывает средство **Sources** после выбора</span><span class="sxs-lookup"><span data-stu-id="52204-139">DevTools opens the **Sources** tool after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-140">Возвращайтесь к консоли **с** помощью любого из следующих процессов:</span><span class="sxs-lookup"><span data-stu-id="52204-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="52204-141">Выберите **средство Консоли.**</span><span class="sxs-lookup"><span data-stu-id="52204-141">Choose the **Console** tool.</span></span>  
    *   <span data-ttu-id="52204-142">Выберите `Control` + `[` \(Windows, Linux\) `Command` + `[` или \(macOS\) до \*\*\*\* тех пор, пока средство консоли не будет в фокусе.</span><span class="sxs-lookup"><span data-stu-id="52204-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** tool is in focus.</span></span>  
    *   <span data-ttu-id="52204-143">[Откройте командное меню,][DevToolsCommandMenu] `Console` введите, выберите команду Панель консоли **Show,** а затем выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="52204-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="52204-144">Выберите **кнопку Предупреждение журнала** в демонстрации.</span><span class="sxs-lookup"><span data-stu-id="52204-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="52204-145">получает войти в **консоль**.</span><span class="sxs-lookup"><span data-stu-id="52204-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="52204-146">Сообщения, отформатированные таким образом, являются предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="52204-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Консоль после выбора предупреждения журнала" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="52204-148">Консоль **после** выбора **предупреждения журнала**</span><span class="sxs-lookup"><span data-stu-id="52204-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="52204-149">Если вы хотите отобразить код, который вызвал определенный вход сообщения, выберите в скрипте \(например\) для просмотра кода, из-за чего сообщение было `log.js:12` отформатировано.</span><span class="sxs-lookup"><span data-stu-id="52204-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="52204-150">Выберите **значок Expand** \( ![ Expand ][ImageExpandIcon] \) перед `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="52204-150">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="52204-151">В DevTools показан [след стека,][WikiStackTrace] ведущий к вызову.</span><span class="sxs-lookup"><span data-stu-id="52204-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Трассировка стека" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="52204-153">Трассировка стека</span><span class="sxs-lookup"><span data-stu-id="52204-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="52204-154">Трассировка стека говорит, что выполняется функция с именем, которая, в свою очередь, `logWarning` выполняет функцию с именем `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="52204-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="52204-155">Другими словами, первый запрос находится в нижней части трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="52204-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="52204-156">Вы можете войти следы стека в любое время при запуске `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="52204-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="52204-157">Выберите **ошибку журнала**.</span><span class="sxs-lookup"><span data-stu-id="52204-157">Choose **Log Error**.</span></span>  <span data-ttu-id="52204-158">В журнал попадает следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="52204-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщение об ошибке" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="52204-160">Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="52204-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-161">Выберите **таблицу журнала**.</span><span class="sxs-lookup"><span data-stu-id="52204-161">Choose **Log Table**.</span></span>  <span data-ttu-id="52204-162">Таблица о известных артистах попадает в **консоль.**</span><span class="sxs-lookup"><span data-stu-id="52204-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="52204-163">Столбец `birthday` заполняется только для одной строки.</span><span class="sxs-lookup"><span data-stu-id="52204-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="52204-164">Просмотрите код, чтобы определить, почему это так.</span><span class="sxs-lookup"><span data-stu-id="52204-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Таблица в консоли" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="52204-166">Таблица в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-167">Выберите **группу журнала**.</span><span class="sxs-lookup"><span data-stu-id="52204-167">Choose **Log Group**.</span></span>  <span data-ttu-id="52204-168">Имена 4 известных, борющихся с преступностью черепах группуются под `Adolescent Irradiated Espionage Tortoises` меткой.</span><span class="sxs-lookup"><span data-stu-id="52204-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Группа сообщений в консоли" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="52204-170">Группа сообщений в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-171">Выберите **настраиваемый журнал**.</span><span class="sxs-lookup"><span data-stu-id="52204-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="52204-172">Сообщение с красной границей и синим фоном попадает в консоль.</span><span class="sxs-lookup"><span data-stu-id="52204-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщение с настраиваемой формата в консоли" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="52204-174">Сообщение с настраиваемой формата в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="52204-175">Основная идея заключается в том, что при входе сообщений в консоль из JavaScript используется один из `console` методов.</span><span class="sxs-lookup"><span data-stu-id="52204-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="52204-176">Каждый метод форматов сообщений по-разному.</span><span class="sxs-lookup"><span data-stu-id="52204-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="52204-177">Существует еще больше методов, чем было продемонстрировано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="52204-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="52204-178">В этом руководстве показано, как изучить остальные методы.</span><span class="sxs-lookup"><span data-stu-id="52204-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <a name="view-messages-logged-by-the-browser"></a><span data-ttu-id="52204-179">Просмотр сообщений, зарегистрированных в браузере</span><span class="sxs-lookup"><span data-stu-id="52204-179">View messages logged by the browser</span></span>  

<span data-ttu-id="52204-180">Браузер также регистрит сообщения в консоли.</span><span class="sxs-lookup"><span data-stu-id="52204-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="52204-181">Обычно это происходит при проблеме со страницей.</span><span class="sxs-lookup"><span data-stu-id="52204-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="52204-182">Выберите **причина 404**.</span><span class="sxs-lookup"><span data-stu-id="52204-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="52204-183">Браузер регистрит код сетевой ошибки состояния HTTP, так как JavaScript страницы пытался получить файл, `404` который не существует.</span><span class="sxs-lookup"><span data-stu-id="52204-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ошибка 404 в консоли" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="52204-185">Ошибка `404` в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-186">Выбор **причины ошибки**.</span><span class="sxs-lookup"><span data-stu-id="52204-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="52204-187">Браузер регистрит необученный, так как JavaScript пытается обновить узел `TypeError` DOM, который не существует.</span><span class="sxs-lookup"><span data-stu-id="52204-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError в консоли" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="52204-189">A `TypeError` в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-190">Выберите **выпадаемые** уровни журналов и включите параметр **Verbose,** если он отключен.</span><span class="sxs-lookup"><span data-stu-id="52204-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="52204-191">Дополнительные статьи о фильтрации в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="52204-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="52204-192">Это необходимо сделать, чтобы убедиться, что следующее сообщение, которое вы в журнале, будет видимым.</span><span class="sxs-lookup"><span data-stu-id="52204-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="52204-193">Если отключена отключка уровней по умолчанию, может потребоваться закрыть боковую панель **консоли.**</span><span class="sxs-lookup"><span data-stu-id="52204-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="52204-194">Фильтр по источнику сообщений ниже, чтобы получить дополнительные сведения о **боковой** панели консоли.</span><span class="sxs-lookup"><span data-stu-id="52204-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Включение уровня журнала Verbose" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="52204-196">Включение уровня журнала Verbose</span><span class="sxs-lookup"><span data-stu-id="52204-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-197">Выберите **причину нарушения**.</span><span class="sxs-lookup"><span data-stu-id="52204-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="52204-198">Страница на несколько секунд становится безответной, а затем браузер записывет сообщение `[Violation] 'click' handler took 3000ms` на консоль.</span><span class="sxs-lookup"><span data-stu-id="52204-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="52204-199">Точная продолжительность может отличаться.</span><span class="sxs-lookup"><span data-stu-id="52204-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Нарушение в консоли" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="52204-201">Нарушение в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <a name="filter-messages"></a><span data-ttu-id="52204-202">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="52204-202">Filter messages</span></span>  

<span data-ttu-id="52204-203">На некоторых веб-сайтах вы просматриваете **консоль,** которая заполоняется сообщениями.</span><span class="sxs-lookup"><span data-stu-id="52204-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="52204-204">DevTools предоставляет множество различных способов фильтрации сообщений, не соответствующих поставленной задаче.</span><span class="sxs-lookup"><span data-stu-id="52204-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <a name="filter-by-log-level"></a><span data-ttu-id="52204-205">Фильтр по уровню журнала</span><span class="sxs-lookup"><span data-stu-id="52204-205">Filter by log level</span></span>  

<span data-ttu-id="52204-206">Каждому `console` методу назначен уровень серьезности: `Verbose` , , , или `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="52204-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="52204-207">Например, это сообщение уровня, в то время как это `console.log()` `Info` сообщение `console.error()` `Error` уровня.</span><span class="sxs-lookup"><span data-stu-id="52204-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="52204-208">Выберите **выпадаемые** уровни журналов и отключите **ошибки.**</span><span class="sxs-lookup"><span data-stu-id="52204-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="52204-209">Уровень отключен, когда рядом с ней больше нет контрольного знака.</span><span class="sxs-lookup"><span data-stu-id="52204-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="52204-210">Сообщения `Error` уровня исчезают.</span><span class="sxs-lookup"><span data-stu-id="52204-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Отключение сообщений уровня ошибок в консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="52204-212">Отключение сообщений уровня ошибок в **консоли**</span><span class="sxs-lookup"><span data-stu-id="52204-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-213">Снова выберите **выпадаемые** уровни журналов и повторно включить **ошибки.**</span><span class="sxs-lookup"><span data-stu-id="52204-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="52204-214">Снова `Error` появляются сообщения уровня.</span><span class="sxs-lookup"><span data-stu-id="52204-214">The `Error`-level messages reappear.</span></span>  

### <a name="filter-by-text"></a><span data-ttu-id="52204-215">Фильтр по тексту</span><span class="sxs-lookup"><span data-stu-id="52204-215">Filter by text</span></span>  

<span data-ttu-id="52204-216">Если нужно просматривать только сообщения, включаю точные строки, введите эту строку в текстовое поле **Filter.**</span><span class="sxs-lookup"><span data-stu-id="52204-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="52204-217">`Dave`Введите **текстовое поле Filter.**</span><span class="sxs-lookup"><span data-stu-id="52204-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="52204-218">Все сообщения, которые не включают `Dave` строку, скрыты.</span><span class="sxs-lookup"><span data-stu-id="52204-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="52204-219">Вы также можете просмотреть `Adolescent Irradiated Espionage Tortoises` метку.</span><span class="sxs-lookup"><span data-stu-id="52204-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="52204-220">Это ошибка.</span><span class="sxs-lookup"><span data-stu-id="52204-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Отфильтровать любое сообщение, не включаее Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="52204-222">Фильтрация любых сообщений, не включа</span><span class="sxs-lookup"><span data-stu-id="52204-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-223">Удаление `Dave` из **текстового окна Filter.**</span><span class="sxs-lookup"><span data-stu-id="52204-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="52204-224">Все сообщения появляются снова.</span><span class="sxs-lookup"><span data-stu-id="52204-224">All the messages reappear.</span></span>  

### <a name="filter-by-regular-expression"></a><span data-ttu-id="52204-225">Фильтр по регулярному выражению</span><span class="sxs-lookup"><span data-stu-id="52204-225">Filter by regular expression</span></span>  

<span data-ttu-id="52204-226">Если вы хотите показать все сообщения, которые включают шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="52204-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="52204-227">`/^[AH]/`Введите **текстовое поле Filter.**</span><span class="sxs-lookup"><span data-stu-id="52204-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="52204-228">Введите шаблон в [RegExr][|::ref1::|Main] для объяснения того, что он делает.</span><span class="sxs-lookup"><span data-stu-id="52204-228">Type the pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Фильтрация любых сообщений, не совпадающих с шаблоном" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="52204-230">Фильтрация любых сообщений, не совпадающих с шаблоном</span><span class="sxs-lookup"><span data-stu-id="52204-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-231">Удаление `/^[AH]/` из **текстового окна Filter.**</span><span class="sxs-lookup"><span data-stu-id="52204-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="52204-232">Все сообщения снова видны.</span><span class="sxs-lookup"><span data-stu-id="52204-232">All messages are visible again.</span></span>  

### <a name="filter-by-message-source"></a><span data-ttu-id="52204-233">Фильтр по источнику сообщений</span><span class="sxs-lookup"><span data-stu-id="52204-233">Filter by message source</span></span>  

<span data-ttu-id="52204-234">Если вы хотите просматривать только сообщения, которые поступили из определенного URL-адреса, используйте **боковую панель**.</span><span class="sxs-lookup"><span data-stu-id="52204-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="52204-235">Выберите **боковую панель** консоли show \. ![ Показать боковую панель ][ImageShowConsoleSidebarIcon] консоли \).</span><span class="sxs-lookup"><span data-stu-id="52204-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Боковая панель" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="52204-237">Боковая панель</span><span class="sxs-lookup"><span data-stu-id="52204-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-238">Выберите **значок Expand** ![ \( Expand ][ImageExpandIcon] \) рядом с числом сообщений.</span><span class="sxs-lookup"><span data-stu-id="52204-238">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="52204-239">На следующем рисунке количество сообщений указывается как **13 сообщений.**</span><span class="sxs-lookup"><span data-stu-id="52204-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="52204-240">На **боковой панели** показан список URL-адресов, из-за чего сообщения были внесены в журнал.</span><span class="sxs-lookup"><span data-stu-id="52204-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="52204-241">Например, `log.js` вызвало 11 сообщений.</span><span class="sxs-lookup"><span data-stu-id="52204-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Просмотр источника сообщений в боковой панели" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="52204-243">Просмотр источника сообщений в боковой панели</span><span class="sxs-lookup"><span data-stu-id="52204-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a><span data-ttu-id="52204-244">Фильтрация сообщений пользователей</span><span class="sxs-lookup"><span data-stu-id="52204-244">Filter by user messages</span></span>  

<span data-ttu-id="52204-245">Ранее, при выборе **журнала Info**, скрипт с именем для входа сообщения в `console.log('Hello, Console!')` консоль.</span><span class="sxs-lookup"><span data-stu-id="52204-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="52204-246">Сообщения, в журнале из JavaScript, как это **называются сообщения пользователей**.</span><span class="sxs-lookup"><span data-stu-id="52204-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="52204-247">Напротив, при выборе **Cause 404**браузер регистрирует сообщение уровня, указывав, что запрашиваемого `Error` ресурса не обнаружено.</span><span class="sxs-lookup"><span data-stu-id="52204-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource is not found.</span></span>  <span data-ttu-id="52204-248">Такие сообщения считаются сообщениями **браузера.**</span><span class="sxs-lookup"><span data-stu-id="52204-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="52204-249">Используйте **боковую панель,** чтобы отфильтровать сообщения браузера и показывать только сообщения пользователей.</span><span class="sxs-lookup"><span data-stu-id="52204-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="52204-250">Выберите **9 сообщений пользователей**.</span><span class="sxs-lookup"><span data-stu-id="52204-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="52204-251">Сообщения браузера скрыты.</span><span class="sxs-lookup"><span data-stu-id="52204-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Фильтрация сообщений браузера" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="52204-253">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="52204-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="52204-254">Выберите **13 сообщений,** чтобы показать все сообщения снова.</span><span class="sxs-lookup"><span data-stu-id="52204-254">Choose **13 Messages** to show all messages again.</span></span>  

## <a name="use-the-console-alongside-any-other-tools"></a><span data-ttu-id="52204-255">Используйте консоль вместе с любыми другими средствами</span><span class="sxs-lookup"><span data-stu-id="52204-255">Use the Console alongside any other tools</span></span>  

<span data-ttu-id="52204-256">Если вы редактируете стили, но вам необходимо быстро проверить журнал консоли для чего-то, используйте ящик.</span><span class="sxs-lookup"><span data-stu-id="52204-256">If you are editing styles, but you need to quickly check the Console log for something, Use the Drawer.</span></span>  

1.  <span data-ttu-id="52204-257">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="52204-257">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="52204-258">Выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="52204-258">Select `Escape`.</span></span>  <span data-ttu-id="52204-259">Откроется **консольный** инструмент **в ящике.**</span><span class="sxs-lookup"><span data-stu-id="52204-259">The **Console** tool in the **Drawer** opens.</span></span>  <span data-ttu-id="52204-260">Он содержит все функции панели Консоли, которые вы использовали во всем этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="52204-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Средство консоли в ящике" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="52204-262">Средство **консоли** в **ящике**</span><span class="sxs-lookup"><span data-stu-id="52204-262">The **Console** tool in the **Drawer**</span></span>  
    :::image-end:::  
    
## <a name="see-also"></a><span data-ttu-id="52204-263">См. также</span><span class="sxs-lookup"><span data-stu-id="52204-263">See also</span></span>  

*   <span data-ttu-id="52204-264">Чтобы изучить дополнительные функции и процессы, связанные с интерфейсом **консоли,** перейдите на [консоль ссылку][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="52204-264">To explore more features and workflows related to the **Console** UI,navigate to [Console Reference][DevToolsConsoleApi].</span></span>  
*   <span data-ttu-id="52204-265">Чтобы узнать больше обо всех методах, демонстрируемых в View `console` [messages logged from JavaScript,](#view-messages-logged-from-javascript) и ознакомьтесь с другими методами, не охваченными в этой статье, перейдите к ссылке `console` На [API консоли][DevToolsConsoleReference].</span><span class="sxs-lookup"><span data-stu-id="52204-265">To learn more about all of the `console` methods demonstrated in [View messages logged from JavaScript](#view-messages-logged-from-javascript) and explore the other `console` methods not covered in this article, navigate to [Console API Reference][DevToolsConsoleReference].</span></span>  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="52204-266">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="52204-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочные | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md "Справочные | Документы Майкрософт"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с ведением журнала сообщений | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедия"  
> [!NOTE]
> <span data-ttu-id="52204-276">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52204-276">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="52204-277">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/log) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="52204-277">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="52204-279">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52204-279">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
