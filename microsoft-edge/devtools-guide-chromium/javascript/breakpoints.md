---
description: Узнайте обо всех способах приостановки кода в Microsoft Edge DevTools.
title: Приостановка кода с помощью точек остановок в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 84077503d6c786244fc2ca4d54c349ae9f6d20d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398597"
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

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a><span data-ttu-id="7e04d-104">Приостановка кода с помощью точек остановок в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7e04d-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7e04d-105">Для приостановки кода JavaScript используйте точки breakpoints.</span><span class="sxs-lookup"><span data-stu-id="7e04d-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="7e04d-106">В этом руководстве рассказывается о каждом типе точки разрыва, доступной в DevTools, а также о том, когда и как настроить каждый тип.</span><span class="sxs-lookup"><span data-stu-id="7e04d-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="7e04d-107">Для практических уроков процесса отладки перейдите к началу отладки JavaScript в [Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="7e04d-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <a name="overview-of-when-to-use-each-breakpoint-type"></a><span data-ttu-id="7e04d-108">Обзор того, когда использовать каждый тип точки разрыва</span><span class="sxs-lookup"><span data-stu-id="7e04d-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="7e04d-109">Наиболее известным типом точки разрыва является строка кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="7e04d-110">Но точки взлома строки кода могут быть неэффективными для набора, особенно если вы не знаете точно, где искать, или если вы работаете с большой базой кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="7e04d-111">Вы можете сэкономить время при отладки, зная, как и когда использовать другие типы точек разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="7e04d-112">Тип breakpoint</span><span class="sxs-lookup"><span data-stu-id="7e04d-112">Breakpoint Type</span></span> | <span data-ttu-id="7e04d-113">Используйте это, когда вы хотите сделать паузу...</span><span class="sxs-lookup"><span data-stu-id="7e04d-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="7e04d-114">Line-of-code</span><span class="sxs-lookup"><span data-stu-id="7e04d-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="7e04d-115">На точном регионе кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="7e04d-116">Условная строка кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="7e04d-117">В точном регионе кода, но только в том случае, если верно другое условие.</span><span class="sxs-lookup"><span data-stu-id="7e04d-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="7e04d-118">DOM</span><span class="sxs-lookup"><span data-stu-id="7e04d-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="7e04d-119">В коде, который изменяет или удаляет определенный узел DOM или детей.</span><span class="sxs-lookup"><span data-stu-id="7e04d-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="7e04d-120">XHR</span><span class="sxs-lookup"><span data-stu-id="7e04d-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="7e04d-121">Когда URL-адрес XHR содержит шаблон строки.</span><span class="sxs-lookup"><span data-stu-id="7e04d-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="7e04d-122">Слушатель событий</span><span class="sxs-lookup"><span data-stu-id="7e04d-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="7e04d-123">На коде, который выполняется после события, `click` например, выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e04d-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="7e04d-124">Исключение</span><span class="sxs-lookup"><span data-stu-id="7e04d-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="7e04d-125">На строке кода, который бросает пойманный или необученный исключение.</span><span class="sxs-lookup"><span data-stu-id="7e04d-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="7e04d-126">Функция</span><span class="sxs-lookup"><span data-stu-id="7e04d-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="7e04d-127">При запуске определенной команды, функции или метода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <a name="line-of-code-breakpoints"></a><span data-ttu-id="7e04d-128">Точки разлома строки кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="7e04d-129">Используйте точку разрыва кода, когда вы знаете точный регион кода, который необходимо исследовать.</span><span class="sxs-lookup"><span data-stu-id="7e04d-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="7e04d-130">DevTools всегда останавливается перед запуском этой строки кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="7e04d-131">Чтобы установить точку разрыва кода в DevTools:</span><span class="sxs-lookup"><span data-stu-id="7e04d-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="7e04d-132">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-132">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="7e04d-133">Откройте файл, содержащий строку кода, на которой необходимо разорвать.</span><span class="sxs-lookup"><span data-stu-id="7e04d-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="7e04d-134">Перейдите по строке кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="7e04d-135">Слева от строки кода находится столбец номеров строки.</span><span class="sxs-lookup"><span data-stu-id="7e04d-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="7e04d-136">Выберите его.</span><span class="sxs-lookup"><span data-stu-id="7e04d-136">Choose it.</span></span>  <span data-ttu-id="7e04d-137">Рядом со столбцом номеров строки отображается красный значок.</span><span class="sxs-lookup"><span data-stu-id="7e04d-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Точка взлома строки кода" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="7e04d-139">Точка взлома строки кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a><span data-ttu-id="7e04d-140">Точки разлома строк кода в коде</span><span class="sxs-lookup"><span data-stu-id="7e04d-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="7e04d-141">Запустите `debugger` метод из кода, чтобы остановиться на этой строке.</span><span class="sxs-lookup"><span data-stu-id="7e04d-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="7e04d-142">Это эквивалентно [точке](#line-of-code-breakpoints)разрыва кода, за исключением того, что точка разрыва заданной в коде, а не в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e04d-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a><span data-ttu-id="7e04d-143">Условные точки взлома строки кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="7e04d-144">Используйте условную точку разлома строки кода, если вы знаете точный регион кода, который необходимо исследовать, но вы хотите остановиться только тогда, когда верно другое условие.</span><span class="sxs-lookup"><span data-stu-id="7e04d-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="7e04d-145">Чтобы установить условную точку разлома строки кода:</span><span class="sxs-lookup"><span data-stu-id="7e04d-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="7e04d-146">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-146">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="7e04d-147">Откройте файл, содержащий строку кода, на которой необходимо разорвать.</span><span class="sxs-lookup"><span data-stu-id="7e04d-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="7e04d-148">Перейдите по строке кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="7e04d-149">Слева от строки кода находится столбец номеров строки.</span><span class="sxs-lookup"><span data-stu-id="7e04d-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="7e04d-150">Наведите курсор на номер строки и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="7e04d-150">Hover on the line number and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="7e04d-151">Выберите **добавить условную точку разрыва**.</span><span class="sxs-lookup"><span data-stu-id="7e04d-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="7e04d-152">Диалоговое окно отображается под строкой кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="7e04d-153">Введите свое состояние в диалоговом ок.</span><span class="sxs-lookup"><span data-stu-id="7e04d-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="7e04d-154">Выберите, `Enter` чтобы активировать точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="7e04d-155">Значок рядом со столбцом номеров строки.</span><span class="sxs-lookup"><span data-stu-id="7e04d-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Точка разрыва условной строки кода" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="7e04d-157">Точка разрыва условной строки кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a><span data-ttu-id="7e04d-158">Управление точками разрыва кода</span><span class="sxs-lookup"><span data-stu-id="7e04d-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="7e04d-159">Используйте области **Breakpoints** для отключения или удаления точек разрывов строк кода из одного расположения.</span><span class="sxs-lookup"><span data-stu-id="7e04d-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Панель Breakpoints" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="7e04d-161">Панель **Breakpoints**</span><span class="sxs-lookup"><span data-stu-id="7e04d-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="7e04d-162">Проверьте контрольный ящик рядом с записью, чтобы отключить точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="7e04d-163">Наведите курсор на запись и откройте контекстное меню \(правой кнопкой мыши\), чтобы удалить точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-163">Hover on an entry and open the contextual menu \(right-click\) to remove that breakpoint.</span></span>  
*   <span data-ttu-id="7e04d-164">Наведите курсор в любом месте области **breakpoints** и откройте контекстное меню \(правой кнопкой мыши\), чтобы отключить все точки разрыва, отключить все точки разрыва или удалить все точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-164">Hover anywhere in the **Breakpoints** pane and open the contextual menu \(right-click\) to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="7e04d-165">Отключение всех точек разрыва эквивалентно отключаемой каждой из них.</span><span class="sxs-lookup"><span data-stu-id="7e04d-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="7e04d-166">Отключение всех точек взлома предписывает DevTools игнорировать все точки разрыва кода, но также поддерживать состояние включенного, чтобы каждый из них был в том же состоянии, что и раньше при повторной активности каждой из них.</span><span class="sxs-lookup"><span data-stu-id="7e04d-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Отключенные точки разрыва в области Breakpoints" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="7e04d-168">Отключенные точки разрыва в области **Breakpoints**</span><span class="sxs-lookup"><span data-stu-id="7e04d-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a><span data-ttu-id="7e04d-169">Точки breakpoints изменения DOM</span><span class="sxs-lookup"><span data-stu-id="7e04d-169">DOM change breakpoints</span></span>  

<span data-ttu-id="7e04d-170">Используйте точку размыкать doM, если необходимо приостановить использование кода, который изменяет узел DOM или детей.</span><span class="sxs-lookup"><span data-stu-id="7e04d-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="7e04d-171">Чтобы установить точку breakpoint изменения DOM:</span><span class="sxs-lookup"><span data-stu-id="7e04d-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="7e04d-172">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-172">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="7e04d-173">Перейдите к элементу, на котором необходимо установить точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="7e04d-174">Наведите курсор на элемент и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="7e04d-174">Hover on the element and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="7e04d-175">Наведите курсор на **break on,** а затем выберите **изменения Subtree,** **изменения**атрибута или **удаление узлов.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Контекстное меню для создания точки разрыва изменения DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="7e04d-177">Контекстное меню для создания точки разрыва изменения DOM</span><span class="sxs-lookup"><span data-stu-id="7e04d-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a><span data-ttu-id="7e04d-178">Типы точки breakpoints изменения DOM</span><span class="sxs-lookup"><span data-stu-id="7e04d-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="7e04d-179">**Изменения subtree**.</span><span class="sxs-lookup"><span data-stu-id="7e04d-179">**Subtree modifications**.</span></span>  <span data-ttu-id="7e04d-180">Вызывается при удалении или добавлении ребенка выбранного узла или изменения содержимого ребенка.</span><span class="sxs-lookup"><span data-stu-id="7e04d-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="7e04d-181">Не срабатывает при изменениях атрибута узла ребенка или о каких-либо изменениях в выбранном в настоящее время узле.</span><span class="sxs-lookup"><span data-stu-id="7e04d-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="7e04d-182">**Изменения атрибутов:** срабатывает при добавлении или удалении атрибута на выбранном в настоящее время узле или при изменении значения атрибута.</span><span class="sxs-lookup"><span data-stu-id="7e04d-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="7e04d-183">**Удаление узлов:** срабатывает при удалении выбранного в настоящее время узла.</span><span class="sxs-lookup"><span data-stu-id="7e04d-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <a name="xhrfetch-breakpoints"></a><span data-ttu-id="7e04d-184">XHR/Fetch breakpoints</span><span class="sxs-lookup"><span data-stu-id="7e04d-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="7e04d-185">Если URL-адрес запроса XHR содержит указанную строку, используйте точку разрыва XHR.</span><span class="sxs-lookup"><span data-stu-id="7e04d-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="7e04d-186">DevTools останавливается на строке кода, где метод выполняется `send()` XHR.</span><span class="sxs-lookup"><span data-stu-id="7e04d-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="7e04d-187">Эта функция также работает с [запросами на извлечение API.][MDNFetchApi]</span><span class="sxs-lookup"><span data-stu-id="7e04d-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="7e04d-188">Один из примеров, когда это полезно, это когда веб-сайт запрашивает неправильный URL-адрес, и вы хотите быстро найти исходный код AJAX или Fetch, который вызывает неправильный запрос.</span><span class="sxs-lookup"><span data-stu-id="7e04d-188">One example of when this is helpful is when your webpage is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="7e04d-189">Чтобы установить точку разрыва XHR:</span><span class="sxs-lookup"><span data-stu-id="7e04d-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="7e04d-190">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-190">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="7e04d-191">**Расширь панель точки разлома XHR.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-191">Expand the **XHR Breakpoints** panel.</span></span>  
1.  <span data-ttu-id="7e04d-192">Выберите **точку "Добавить точку разлома".**</span><span class="sxs-lookup"><span data-stu-id="7e04d-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="7e04d-193">Введите строку, которую необходимо разорвать.</span><span class="sxs-lookup"><span data-stu-id="7e04d-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="7e04d-194">DevTools останавливается, когда эта строка присутствует где-либо в URL-адресе запроса XHR.</span><span class="sxs-lookup"><span data-stu-id="7e04d-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="7e04d-195">Выберите `Enter` подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7e04d-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Создание точки разрыва XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="7e04d-197">Создание точки разрыва XHR</span><span class="sxs-lookup"><span data-stu-id="7e04d-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a><span data-ttu-id="7e04d-198">Breakpoints слушателя событий</span><span class="sxs-lookup"><span data-stu-id="7e04d-198">Event listener breakpoints</span></span>  

<span data-ttu-id="7e04d-199">Используйте точки breakpoints слушателя событий, когда необходимо сделать паузу в коде слушателя событий, который запускается после того, как событие будет уволено.</span><span class="sxs-lookup"><span data-stu-id="7e04d-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="7e04d-200">Вы можете выбрать определенные события, такие как события или категории событий, например `click` все события мыши.</span><span class="sxs-lookup"><span data-stu-id="7e04d-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="7e04d-201">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-201">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="7e04d-202">Расширение панели **breakpoints слушателя** событий.</span><span class="sxs-lookup"><span data-stu-id="7e04d-202">Expand the **Event Listener Breakpoints** panel.</span></span>  <span data-ttu-id="7e04d-203">В DevTools показан список категорий событий, таких как **Анимация.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="7e04d-204">Проверьте одну из этих категорий, чтобы приостановить любое событие из этой категории или расширить эту категорию и проверить определенное событие.</span><span class="sxs-lookup"><span data-stu-id="7e04d-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Создание точки разгона слушателя событий" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="7e04d-206">Создание точки разгона слушателя событий</span><span class="sxs-lookup"><span data-stu-id="7e04d-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a><span data-ttu-id="7e04d-207">Точки разлома исключений</span><span class="sxs-lookup"><span data-stu-id="7e04d-207">Exception breakpoints</span></span>  

<span data-ttu-id="7e04d-208">Используйте точки разлома исключений, если необходимо приостановить на строке кода, бросаемом пойманный или незасвеченный исключение.</span><span class="sxs-lookup"><span data-stu-id="7e04d-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="7e04d-209">Выберите средство **Sources.**</span><span class="sxs-lookup"><span data-stu-id="7e04d-209">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="7e04d-210">Выберите **Пауза для исключений** \. ![ Пауза для ][ImagePauseOnExceptionsIcon] исключений \).</span><span class="sxs-lookup"><span data-stu-id="7e04d-210">Choose **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="7e04d-211">Значок поимеет при включении.</span><span class="sxs-lookup"><span data-stu-id="7e04d-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Кнопка "Пауза на исключениях"" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="7e04d-213">Кнопка **"Пауза на исключениях"**</span><span class="sxs-lookup"><span data-stu-id="7e04d-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7e04d-214">**Необязательный**.</span><span class="sxs-lookup"><span data-stu-id="7e04d-214">**Optional**.</span></span>  <span data-ttu-id="7e04d-215">Проверьте **почтовый ящик Pause On Caught Exceptions,** если вы также хотите остановиться на пойманных исключениях, а также на незавербовавке.</span><span class="sxs-lookup"><span data-stu-id="7e04d-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Пауза на необученном исключении" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="7e04d-217">Пауза на необученном исключении</span><span class="sxs-lookup"><span data-stu-id="7e04d-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <a name="function-breakpoints"></a><span data-ttu-id="7e04d-218">Точки breakpoints функции</span><span class="sxs-lookup"><span data-stu-id="7e04d-218">Function breakpoints</span></span>  

<span data-ttu-id="7e04d-219">Запустите метод, где находится команда, функция или метод, который необходимо отлаговать, когда необходимо приостановить при запуске `debug(method)` `method` определенной функции.</span><span class="sxs-lookup"><span data-stu-id="7e04d-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="7e04d-220">Вы можете вставить в код (например, заявление) или запустить метод из `debug()` `console.log()` консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e04d-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="7e04d-221">эквивалентно установке [точки разрыва](#line-of-code-breakpoints) кода на первой строке функции.</span><span class="sxs-lookup"><span data-stu-id="7e04d-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a><span data-ttu-id="7e04d-222">Убедитесь, что целевая функция находится в области</span><span class="sxs-lookup"><span data-stu-id="7e04d-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="7e04d-223">DevTools бросает, если функция отладки не `ReferenceError` находится в области.</span><span class="sxs-lookup"><span data-stu-id="7e04d-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="7e04d-224">Обеспечение целевой функции в области является сложной, если вы работаете метод `debug()` из консоли DevTools.</span><span class="sxs-lookup"><span data-stu-id="7e04d-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="7e04d-225">Вот одна стратегия:</span><span class="sxs-lookup"><span data-stu-id="7e04d-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="7e04d-226">Установите [точку разлома строки кода где-нибудь,](#line-of-code-breakpoints) где функция находится в области.</span><span class="sxs-lookup"><span data-stu-id="7e04d-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="7e04d-227">Срабатывает точка разрыва.</span><span class="sxs-lookup"><span data-stu-id="7e04d-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="7e04d-228">Запустите `debug()` метод в консоли DevTools, пока код остается приостановленным на точке разрыва кода.</span><span class="sxs-lookup"><span data-stu-id="7e04d-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7e04d-229">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7e04d-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Извлечение API | MDN"  

> [!NOTE]
> <span data-ttu-id="7e04d-232">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e04d-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7e04d-233">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="7e04d-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7e04d-235">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7e04d-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
