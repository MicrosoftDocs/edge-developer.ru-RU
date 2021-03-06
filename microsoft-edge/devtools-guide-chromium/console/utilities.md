---
description: Ссылка на удобные команды, доступные в консоли Microsoft Edge DevTools.
title: Ссылка на API консоли utilities
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398828"
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

# <a name="console-utilities-api-reference"></a><span data-ttu-id="80a11-104">Ссылка на API консоли utilities</span><span class="sxs-lookup"><span data-stu-id="80a11-104">Console Utilities API reference</span></span>  

<span data-ttu-id="80a11-105">API консоли Utilities содержит набор команд удобства для выполнения общих задач: выбора и проверки элементов DOM, отображения данных в читаемом формате, остановки и запуска профиля и мониторинга событий DOM.</span><span class="sxs-lookup"><span data-stu-id="80a11-105">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="80a11-106">Следующие команды работают только в консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="80a11-106">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="80a11-107">Команды не работают при запуске из скриптов.</span><span class="sxs-lookup"><span data-stu-id="80a11-107">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="80a11-108">Для `console.log()` остальных `console.error()` методов и методов перейдите к `console.*` [ссылке консоли API.][DevToolsConsoleApi]</span><span class="sxs-lookup"><span data-stu-id="80a11-108">For the `console.log()` and `console.error()` methods the rest of the `console.*` methods, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  

## <a name="recently-evaluated-expression"></a><span data-ttu-id="80a11-109">Недавно оцененное выражение</span><span class="sxs-lookup"><span data-stu-id="80a11-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="80a11-110">Возвращает значение последнего оцениваемого выражения.</span><span class="sxs-lookup"><span data-stu-id="80a11-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="80a11-111">На следующем рисунке оценивается простое выражение `2 + 2` \( \).</span><span class="sxs-lookup"><span data-stu-id="80a11-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="80a11-112">Затем `$_` свойство оценивается, которое содержит одно и то же значение.</span><span class="sxs-lookup"><span data-stu-id="80a11-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ — это наиболее недавно оцененное выражение" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="80a11-114">Рис. 1:  `$_` это наиболее недавно оцененное выражение</span><span class="sxs-lookup"><span data-stu-id="80a11-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-115">На следующем рисунке оцениваемая экспрессия изначально содержит массив имен.</span><span class="sxs-lookup"><span data-stu-id="80a11-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="80a11-116">Оценивая длину массива, значение, сохраненное в изменениях, чтобы стать `$_.length` `$_` последним оцениваемого выражения, `4` .</span><span class="sxs-lookup"><span data-stu-id="80a11-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="Изменения $_ при оценке новых команд" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="80a11-118">Рис. 2.  `$_` Изменения при оценке новых команд</span><span class="sxs-lookup"><span data-stu-id="80a11-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a><span data-ttu-id="80a11-119">Недавно выбранный элемент или объект JavaScript</span><span class="sxs-lookup"><span data-stu-id="80a11-119">Recently Chosen Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="80a11-120">Возвращает последний элемент или объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="80a11-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="80a11-121">возвращает второй недавно выбранный и так далее.</span><span class="sxs-lookup"><span data-stu-id="80a11-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="80a11-122">Команды и команды работают в качестве исторической ссылки на последние пять элементов DOM, инспектировался в инструменте Elements или в последних пяти объектах `$0` `$1` `$2` `$3` `$4` JavaScript, \*\*\*\* \*\*\*\* выбранных в средстве Памяти.</span><span class="sxs-lookup"><span data-stu-id="80a11-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** tool or the last five JavaScript heap objects selected in the **Memory** tool.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

<span data-ttu-id="80a11-123">На следующем рисунке элемент `img` выбирается в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="80a11-123">In the following figure, an `img` element is selected in the **Elements** tool.</span></span>  <span data-ttu-id="80a11-124">В **ящике консоли** была оценена и `$0` отображается один и тот же элемент.</span><span class="sxs-lookup"><span data-stu-id="80a11-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="80a11-126">Рис. 3.</span><span class="sxs-lookup"><span data-stu-id="80a11-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="80a11-127">На следующем рисунке на изображении показан другой элемент, выбранный на одной странице.</span><span class="sxs-lookup"><span data-stu-id="80a11-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="80a11-128">Теперь `$0` относится к недавно выбранному элементу, а возвращает выбранный `$1` ранее элемент.</span><span class="sxs-lookup"><span data-stu-id="80a11-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="80a11-130">Рис. 4.</span><span class="sxs-lookup"><span data-stu-id="80a11-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <a name="query-selector"></a><span data-ttu-id="80a11-131">Селектор запросов</span><span class="sxs-lookup"><span data-stu-id="80a11-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="80a11-132">Возвращает ссылку на первый элемент DOM с указанным селектором CSS.</span><span class="sxs-lookup"><span data-stu-id="80a11-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="80a11-133">Этот метод является псевдонимом метода [document.querySelector().][MDNDocumentQuerySelector]</span><span class="sxs-lookup"><span data-stu-id="80a11-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="80a11-134">На следующем рисунке возвращается ссылка на первый элемент `<img>` документа.</span><span class="sxs-lookup"><span data-stu-id="80a11-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="80a11-136">Рис. 5.</span><span class="sxs-lookup"><span data-stu-id="80a11-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="80a11-137">Наведите курсор на возвращаемом результате, откройте контекстное \*\*\*\* меню \(правой кнопкой мыши\) \*\*\*\* и выберите Показать в панели элементов, чтобы найти его в DOM или прокрутите, чтобы просмотреть его на странице.</span><span class="sxs-lookup"><span data-stu-id="80a11-137">Hover on the returned result, open the contextual menu \(right-click\), and choose **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="80a11-138">На следующем рисунке возвращается ссылка на выбранный в настоящее время элемент и отображается свойство SRC.</span><span class="sxs-lookup"><span data-stu-id="80a11-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="The $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="80a11-140">Рис. 6.</span><span class="sxs-lookup"><span data-stu-id="80a11-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="80a11-141">Этот метод также поддерживает второй параметр startNode, который указывает элемент или узел для поиска элементов.</span><span class="sxs-lookup"><span data-stu-id="80a11-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="80a11-142">Значение параметра по умолчанию `document` .</span><span class="sxs-lookup"><span data-stu-id="80a11-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="80a11-143">На следующем рисунке первый элемент найден после того, как возвращается правильно `img` `title--image` `src` отображаемый элемент.</span><span class="sxs-lookup"><span data-stu-id="80a11-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')))src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="80a11-145">Рис. 7.</span><span class="sxs-lookup"><span data-stu-id="80a11-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="80a11-146">Если вы используете библиотеку, например jQuery, которая использует, функциональность перезаписана и соответствует реализации `$` `$` из этой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="80a11-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <a name="query-selector-all"></a><span data-ttu-id="80a11-147">Селектор запросов Все</span><span class="sxs-lookup"><span data-stu-id="80a11-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="80a11-148">Возвращает массив элементов, которые соответствуют указанному селектору CSS.</span><span class="sxs-lookup"><span data-stu-id="80a11-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="80a11-149">Этот метод эквивалентен запуску [метода document.querySelectorAll().][MDNDocumentQuerySelectorAll]</span><span class="sxs-lookup"><span data-stu-id="80a11-149">This method is equivalent to running the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="80a11-150">В следующем примере кода и рисунке используйте для создания массива всех элементов текущего документа и отображения значения `$$()` `<img>` свойства для каждого `src` элемента.</span><span class="sxs-lookup"><span data-stu-id="80a11-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Использование $$() для выбора всех изображений в документе и отображения источников" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="80a11-152">Рис. 8. Использование `$$()` для выбора всех изображений в документе и отображения источников</span><span class="sxs-lookup"><span data-stu-id="80a11-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-153">Этот метод также поддерживает второй параметр startNode, который указывает элемент или узел для поиска элементов.</span><span class="sxs-lookup"><span data-stu-id="80a11-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="80a11-154">Значение параметра по умолчанию `document` .</span><span class="sxs-lookup"><span data-stu-id="80a11-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="80a11-155">В следующем примере кода и рисунке измененная версия предыдущего примера кода и рисунка использует для создания массива всех элементов, которые отображаются в текущем документе после выбранного `$$()` `<img>` узла.</span><span class="sxs-lookup"><span data-stu-id="80a11-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Использование $$() для выбора всех изображений, которые отображаются после указанного элемента <div> документа, и отображения источников" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="80a11-157">Рис. 9. Использование для выбора всех изображений, которые отображаются после указанного элемента в документе, и `$$()` `<div>` отображения источников</span><span class="sxs-lookup"><span data-stu-id="80a11-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="80a11-158">Выберите `Shift` + `Enter` в консоли, чтобы запустить новую строку без запуска сценария.</span><span class="sxs-lookup"><span data-stu-id="80a11-158">Select `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <a name="xpath"></a><span data-ttu-id="80a11-159">XPath</span><span class="sxs-lookup"><span data-stu-id="80a11-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="80a11-160">Возвращает массив элементов DOM, которые соответствуют указанному выражению XPath.</span><span class="sxs-lookup"><span data-stu-id="80a11-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="80a11-161">В следующем примере кода и рисунке возвращаются все элементы на `<p>` странице.</span><span class="sxs-lookup"><span data-stu-id="80a11-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Использование селектора XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="80a11-163">Рис. 10. Использование селектора XPath</span><span class="sxs-lookup"><span data-stu-id="80a11-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-164">В следующем примере кода и рисунке возвращаются все элементы, содержащие `<p>` `<a>` элементы.</span><span class="sxs-lookup"><span data-stu-id="80a11-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Использование более сложного селектора XPath" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="80a11-166">Рис. 11. Использование более сложного селектора XPath</span><span class="sxs-lookup"><span data-stu-id="80a11-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-167">Как и другие команды селектора, имеет необязательный второй параметр, который указывает элемент или узел, из которого можно искать `$x(path)` `startNode` элементы.</span><span class="sxs-lookup"><span data-stu-id="80a11-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Использование селектора XPath с помощью startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="80a11-169">Рис. 12. Использование селектора XPath с</span><span class="sxs-lookup"><span data-stu-id="80a11-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <a name="clear"></a><span data-ttu-id="80a11-170">clear</span><span class="sxs-lookup"><span data-stu-id="80a11-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="80a11-171">Очищает консоль истории.</span><span class="sxs-lookup"><span data-stu-id="80a11-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <a name="copy"></a><span data-ttu-id="80a11-172">copy</span><span class="sxs-lookup"><span data-stu-id="80a11-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="80a11-173">Метод `copy(object)` копирует строковую репрезентативность указанного объекта в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="80a11-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <a name="debug"></a><span data-ttu-id="80a11-174">отладка</span><span class="sxs-lookup"><span data-stu-id="80a11-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="80a11-175">Проблема [Chromium #1050237][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.</span><span class="sxs-lookup"><span data-stu-id="80a11-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="80a11-176">Если вы столкнулись с проблемой, [попробуйте использовать точки перерывов.][DevtoolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="80a11-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="80a11-177">При запросе указанного метода отладка вызывается и ломается внутри метода на средстве **Sources,** позволяя вам ступить через код и отладить его.</span><span class="sxs-lookup"><span data-stu-id="80a11-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** tool allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Взлом метода с помощью отлаговки()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="80a11-179">Рис. 13. Взлом метода с помощью</span><span class="sxs-lookup"><span data-stu-id="80a11-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="80a11-180">Используйте `undebug(method)` для остановки взлома метода или использования пользовательского интерфейса для отключения всех точек взлома.</span><span class="sxs-lookup"><span data-stu-id="80a11-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="80a11-181">Дополнительные сведения о точках остановок перейдите к [паузе кода с breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="80a11-181">For more information on breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="dir"></a><span data-ttu-id="80a11-182">dir</span><span class="sxs-lookup"><span data-stu-id="80a11-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="80a11-183">Отображает список всех свойств указанного объекта в стиле объекта.</span><span class="sxs-lookup"><span data-stu-id="80a11-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="80a11-184">Этот метод является псевдонимом [метода console.dir().][MDNConsoleDir]</span><span class="sxs-lookup"><span data-stu-id="80a11-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="80a11-185">Оцените `document.head` в консоли отображение HTML между `<head>` `</head>` тегами и тегами.</span><span class="sxs-lookup"><span data-stu-id="80a11-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="80a11-186">В следующем примере кода и рисунке после использования в консоли отображается список в стиле `console.dir()` объекта.</span><span class="sxs-lookup"><span data-stu-id="80a11-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Ведение журнала document.head с помощью метода dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="80a11-188">Рис. 14. Ведение журнала `document.head` с помощью `dir()` метода</span><span class="sxs-lookup"><span data-stu-id="80a11-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-189">Дополнительные сведения перейдите к [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API консоли.</span><span class="sxs-lookup"><span data-stu-id="80a11-189">For more information, navigate to [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <a name="dirxml"></a><span data-ttu-id="80a11-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="80a11-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="80a11-191">Печать XML-представления указанного объекта, отображаемого в **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="80a11-191">Prints an XML representation of the specified object, as displayed in the **Elements** tool.</span></span>  <span data-ttu-id="80a11-192">Этот метод эквивалентен [методу console.dirxml().][MDNConsoleDirxml]</span><span class="sxs-lookup"><span data-stu-id="80a11-192">This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <a name="inspect"></a><span data-ttu-id="80a11-193">проверка</span><span class="sxs-lookup"><span data-stu-id="80a11-193">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="80a11-194">Открывает и выбирает указанный элемент или объект в соответствующей панели: либо средство \*\*\*\* **Elements** для элементов DOM, либо средство памяти для объектов кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="80a11-194">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** tool for DOM elements or the **Memory** tool for JavaScript heap objects.</span></span>  

<span data-ttu-id="80a11-195">В следующем примере кода и рисунке `document.body` откроется средство **Elements.**</span><span class="sxs-lookup"><span data-stu-id="80a11-195">In the following code sample and figure, the `document.body` opens in the **Elements** tool.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Проверка элемента с помощью проверки()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="80a11-197">Рис. 15. Проверка элемента с помощью</span><span class="sxs-lookup"><span data-stu-id="80a11-197">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="80a11-198">При передаче метода для проверки метод открывает документ в **инструменте Источники** для проверки.</span><span class="sxs-lookup"><span data-stu-id="80a11-198">When passing a method to inspect, the method opens the document in the **Sources** tool for you to inspect.</span></span>  

## <a name="geteventlisteners"></a><span data-ttu-id="80a11-199">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="80a11-199">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="80a11-200">Возвращает слушателей событий, зарегистрированных на указанном объекте.</span><span class="sxs-lookup"><span data-stu-id="80a11-200">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="80a11-201">Возвращаемая величина — это объект, содержащий массив для каждого зарегистрированного типа событий \(например `click` или `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="80a11-201">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="80a11-202">Участники каждого массива — это объекты, описывая прослушиватель, зарегистрированный для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="80a11-202">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="80a11-203">В следующем примере кода перечислены все слушатели событий, зарегистрированные на объекте документа.</span><span class="sxs-lookup"><span data-stu-id="80a11-203">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Выход с помощью getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="80a11-205">Рис. 16. Результат использования</span><span class="sxs-lookup"><span data-stu-id="80a11-205">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="80a11-206">Если на указанном объекте зарегистрировано несколько слушателей, массив содержит член для каждого слушателя.</span><span class="sxs-lookup"><span data-stu-id="80a11-206">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="80a11-207">На следующем рисунке в элементе документа для события зарегистрированы два слушателя `click` событий.</span><span class="sxs-lookup"><span data-stu-id="80a11-207">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Несколько слушателей" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="80a11-209">Рис. 17. Несколько слушателей</span><span class="sxs-lookup"><span data-stu-id="80a11-209">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-210">Вы можете дополнительно расширить каждый из следующих объектов, чтобы изучить свойства.</span><span class="sxs-lookup"><span data-stu-id="80a11-210">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Расширенное представление объекта-слушателя" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="80a11-212">Рис. 18. Расширенное представление объекта-слушателя</span><span class="sxs-lookup"><span data-stu-id="80a11-212">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <a name="keys"></a><span data-ttu-id="80a11-213">клавиши</span><span class="sxs-lookup"><span data-stu-id="80a11-213">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="80a11-214">Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="80a11-214">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="80a11-215">Чтобы получить связанные значения тех же свойств, используйте `values()` .</span><span class="sxs-lookup"><span data-stu-id="80a11-215">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="80a11-216">Например, предположим, что ваше приложение определило следующий объект.</span><span class="sxs-lookup"><span data-stu-id="80a11-216">For example, suppose your application defined the following object.</span></span>  

```console
var player1 =   
```  

<span data-ttu-id="80a11-217">В следующих примерах кода и рисунке предполагается, что результат был определен в глобальном пространстве имен \(для простоты\) до ввода и `player1` `keys(player1)` в `values(player1)` консоли.</span><span class="sxs-lookup"><span data-stu-id="80a11-217">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Команды клавиши() и значения()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="80a11-219">Рис. 19. Команды `keys()` `values()` и команды</span><span class="sxs-lookup"><span data-stu-id="80a11-219">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <a name="monitor"></a><span data-ttu-id="80a11-220">монитор</span><span class="sxs-lookup"><span data-stu-id="80a11-220">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="80a11-221">В журнале сообщения на консоль, которое указывает имя метода, а также аргументы, которые передаются методу при его призыве.</span><span class="sxs-lookup"><span data-stu-id="80a11-221">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Метод monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="80a11-223">Рис. 20. `monitor()` Метод</span><span class="sxs-lookup"><span data-stu-id="80a11-223">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-224">Использование `unmonitor(method)` для прекращения мониторинга.</span><span class="sxs-lookup"><span data-stu-id="80a11-224">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <a name="monitorevents"></a><span data-ttu-id="80a11-225">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="80a11-225">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="80a11-226">Когда одно из указанных событий происходит на указанном объекте, объект события регистрируется на консоли.</span><span class="sxs-lookup"><span data-stu-id="80a11-226">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="80a11-227">Можно указать одно событие для мониторинга, массив событий или один из типов общих событий, которые соединяются с предопределяемой коллекцией событий.</span><span class="sxs-lookup"><span data-stu-id="80a11-227">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="80a11-228">Просмотрите следующий пример кода и рисунок.</span><span class="sxs-lookup"><span data-stu-id="80a11-228">Review the following code sample and figure.</span></span>  

<span data-ttu-id="80a11-229">Далее отслеживаются все события, происходящие в окне.</span><span class="sxs-lookup"><span data-stu-id="80a11-229">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Мониторинг событий в окне" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="80a11-231">Рис. 21. Мониторинг событий в окне</span><span class="sxs-lookup"><span data-stu-id="80a11-231">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="80a11-232">Далее определяется массив для мониторинга событий и событий `resize` `scroll` на объекте окна.</span><span class="sxs-lookup"><span data-stu-id="80a11-232">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="80a11-233">Вы также можете указать один из доступных типов событий, строки, которые соединяются с предопределенными наборами событий.</span><span class="sxs-lookup"><span data-stu-id="80a11-233">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="80a11-234">В следующей таблице отображаются доступные типы событий и связанные сопоставления событий.</span><span class="sxs-lookup"><span data-stu-id="80a11-234">The following table displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="80a11-235">Тип события</span><span class="sxs-lookup"><span data-stu-id="80a11-235">Event type</span></span> | <span data-ttu-id="80a11-236">Соответствующие события, относясь к карте</span><span class="sxs-lookup"><span data-stu-id="80a11-236">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="80a11-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span><span class="sxs-lookup"><span data-stu-id="80a11-237">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="80a11-238">"keydown", "keypress", "keyup", "textInput"</span><span class="sxs-lookup"><span data-stu-id="80a11-238">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="80a11-239">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="80a11-239">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="80a11-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span><span class="sxs-lookup"><span data-stu-id="80a11-240">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="80a11-241">В следующем примере кода тип события, соответствующий событиям в текстовом поле ввода, в настоящее время выбирается `key` `key` в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="80a11-241">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** tool.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="80a11-242">На следующем рисунке отображается пример вывода после ввода символа в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="80a11-242">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Мониторинг ключевых событий" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="80a11-244">Рис. 22. Мониторинг ключевых событий</span><span class="sxs-lookup"><span data-stu-id="80a11-244">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <a name="profile"></a><span data-ttu-id="80a11-245">профиль</span><span class="sxs-lookup"><span data-stu-id="80a11-245">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="80a11-246">Запускает сеанс профилирование ЦП JavaScript с необязательным именем.</span><span class="sxs-lookup"><span data-stu-id="80a11-246">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="80a11-247">Метод [profileEnd()](#profileend) завершает профиль и отображает результаты в средстве **памяти.**</span><span class="sxs-lookup"><span data-stu-id="80a11-247">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** tool.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="80a11-248">Запустите `profile()` метод, чтобы начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="80a11-248">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="80a11-249">Запустите [метод profileEnd()](#profileend) для остановки профилирование и отображения результатов в **средстве памяти.**</span><span class="sxs-lookup"><span data-stu-id="80a11-249">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** tool.</span></span>  

<span data-ttu-id="80a11-250">Профили также могут быть вложены.</span><span class="sxs-lookup"><span data-stu-id="80a11-250">Profiles may also be nested.</span></span>  <span data-ttu-id="80a11-251">В следующих примерах кода и рисунке результат один и тот же независимо от порядка.</span><span class="sxs-lookup"><span data-stu-id="80a11-251">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="80a11-252">Одновременно могут работать несколько профилей ЦП, и не требуется закрывать каждый из них в порядке создания.</span><span class="sxs-lookup"><span data-stu-id="80a11-252">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="profileend"></a><span data-ttu-id="80a11-253">profileEnd</span><span class="sxs-lookup"><span data-stu-id="80a11-253">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="80a11-254">Завершает сеанс профилирование ЦП JavaScript и отображает результаты в **средстве памяти.**</span><span class="sxs-lookup"><span data-stu-id="80a11-254">Completes a JavaScript CPU profiling session and displays the results in the **Memory** tool.</span></span>  <span data-ttu-id="80a11-255">Вы должны запускать [метод profile()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="80a11-255">You must be running the [profile()](#profile) method.</span></span>  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="80a11-256">Запустите [метод profile()](#profile) для начала профилирование.</span><span class="sxs-lookup"><span data-stu-id="80a11-256">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="80a11-257">Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты в **средстве Памяти.**</span><span class="sxs-lookup"><span data-stu-id="80a11-257">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** tool.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="80a11-258">Профили также могут быть вложены.</span><span class="sxs-lookup"><span data-stu-id="80a11-258">Profiles may also be nested.</span></span>  <span data-ttu-id="80a11-259">В следующем примере кода и рисунке результат один и тот же независимо от порядка.</span><span class="sxs-lookup"><span data-stu-id="80a11-259">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="80a11-260">Результат отображается в качестве снимка куча в **средстве памяти.**</span><span class="sxs-lookup"><span data-stu-id="80a11-260">The result appears as a Heap Snapshot in the **Memory** tool.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Сгруппные профили" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="80a11-262">Рис. 23. Сгруппные профили</span><span class="sxs-lookup"><span data-stu-id="80a11-262">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="80a11-263">Одновременно могут работать несколько профилей ЦП, и не требуется закрывать каждый из них в порядке создания.</span><span class="sxs-lookup"><span data-stu-id="80a11-263">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <a name="queryobjects"></a><span data-ttu-id="80a11-264">queryObjects</span><span class="sxs-lookup"><span data-stu-id="80a11-264">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="80a11-265">Возвращаем массив объектов, созданных с указанным конструктором.</span><span class="sxs-lookup"><span data-stu-id="80a11-265">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="80a11-266">Областью является выбранный в настоящее время `queryObjects()` контекст времени запуска на консоли.</span><span class="sxs-lookup"><span data-stu-id="80a11-266">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="80a11-267">Возвращает все `Promises` .</span><span class="sxs-lookup"><span data-stu-id="80a11-267">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="80a11-268">Возвращает все элементы HTML.</span><span class="sxs-lookup"><span data-stu-id="80a11-268">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="80a11-269">Возвращает все объекты, которые были мгновенно с помощью `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="80a11-269">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="80a11-270">таблица</span><span class="sxs-lookup"><span data-stu-id="80a11-270">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="80a11-271">Журналы данных объектов с форматированием таблиц на основе объекта данных с необязательными заголовками столбцов.</span><span class="sxs-lookup"><span data-stu-id="80a11-271">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="80a11-272">В следующем примере кода и рисунке отображается список имен с помощью таблицы на консоли.</span><span class="sxs-lookup"><span data-stu-id="80a11-272">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Результат метода таблицы()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="80a11-274">Рис. 24. Результат `table()` метода</span><span class="sxs-lookup"><span data-stu-id="80a11-274">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <a name="undebug"></a><span data-ttu-id="80a11-275">undebug</span><span class="sxs-lookup"><span data-stu-id="80a11-275">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="80a11-276">Останавливает отладку указанного метода, чтобы при вызове метода отладка больше не вызывалась.</span><span class="sxs-lookup"><span data-stu-id="80a11-276">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <a name="unmonitor"></a><span data-ttu-id="80a11-277">unmonitor</span><span class="sxs-lookup"><span data-stu-id="80a11-277">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="80a11-278">Останавливает мониторинг указанного метода.</span><span class="sxs-lookup"><span data-stu-id="80a11-278">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="80a11-279">Этот метод используется в согласованном с [методом monitor()](#monitor) методе.</span><span class="sxs-lookup"><span data-stu-id="80a11-279">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a><span data-ttu-id="80a11-280">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="80a11-280">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="80a11-281">Останавливает мониторинг событий для указанного объекта и событий.</span><span class="sxs-lookup"><span data-stu-id="80a11-281">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="80a11-282">Например, ниже останавливается весь мониторинг событий на объекте окна.</span><span class="sxs-lookup"><span data-stu-id="80a11-282">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="80a11-283">Кроме того, можно выборочно прекратить мониторинг определенных событий на объекте.</span><span class="sxs-lookup"><span data-stu-id="80a11-283">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="80a11-284">Например, в следующем коде начинается мониторинг всех событий на выбранном в настоящее время элементе, а затем прекращается мониторинг событий \(возможно, для уменьшения шума в выходной `mouse` `mousemove` консоли\).</span><span class="sxs-lookup"><span data-stu-id="80a11-284">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a><span data-ttu-id="80a11-285">значения</span><span class="sxs-lookup"><span data-stu-id="80a11-285">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="80a11-286">Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="80a11-286">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="80a11-287">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="80a11-287">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Ссылка на API консоли"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — ссылка на API консоли"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Приостановка кода с помощью точек breakpoints в Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Ускорение времени запуска JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Выпуск 1050237: отлаговка (функция) не работает | Monorail"  

> [!NOTE]
> <span data-ttu-id="80a11-297">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80a11-297">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="80a11-298">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/utilities) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="80a11-298">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="80a11-300">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80a11-300">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
