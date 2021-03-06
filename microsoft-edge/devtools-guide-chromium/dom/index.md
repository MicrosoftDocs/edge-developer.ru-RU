---
description: Просмотр узлов, поиск узлов, редактирование узлов, справочных узлов в консоли, перерыв в изменениях узлов и т. д.
title: Начало работы с просмотром и изменением DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: bb2b733cfa3597c47f0a20de00e9c8b506e7c41c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398331"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="4a5d5-104">Начало работы с просмотром и изменением DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="4a5d5-105">Выполните эти интерактивные учебники, чтобы узнать основы просмотра и изменения DOM страницы с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="4a5d5-106">В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="4a5d5-107">Перейдите [к приложению: HTML и DOM для](#appendix-html-versus-the-dom) объяснения.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="4a5d5-108">Откройте примеры DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="4a5d5-109">Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **примеры DOM,** чтобы открыть на новой вкладке.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="4a5d5-110">Примеры DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="4a5d5-111">Просмотр узлов DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-111">View DOM nodes</span></span>  

<span data-ttu-id="4a5d5-112">DoM Tree панели Elements — это место, где вы делаете все действия, связанные с DOM в DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="4a5d5-113">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-113">Inspect a node</span></span>  

<span data-ttu-id="4a5d5-114">Если вас интересует определенный узел DOM, **Проверьте** это быстрый способ открыть DevTools и исследовать этот узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="4a5d5-115">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-116">В **статье Проверка узла**выберите справа **Микеланджело и** выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="4a5d5-118">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="4a5d5-119">Откроется **средство Elements** devTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="4a5d5-120">выделено в **dom Tree**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла Микеланджело" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="4a5d5-122">Выделение `Michelangelo` узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="4a5d5-123">Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ][ImageInspectIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-123">Choose the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок Inspect" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="4a5d5-125">Значок **Inspect**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="4a5d5-126">В **статье Inspect a Node**выберите текст **Tokyo.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="4a5d5-127">Теперь `<li>Tokyo</li>` выделяется дерево DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="4a5d5-128">Проверка узла также является первым шагом к просмотру и изменению стилей узла.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="4a5d5-129">[Перейдите, чтобы начать с просмотра и изменения CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="4a5d5-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="4a5d5-130">Перемещение дерева DOM с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="4a5d5-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="4a5d5-131">Выбрав узел в dom Tree, вы можете перемещаться по дереву DOM с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="4a5d5-132">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-133">В **статье Перейдите по дереву DOM с клавиатурой,** выберите Ринго правой ринго **и** выберите **Инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="4a5d5-134">выбрано в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="4a5d5-136">Проверка `Ringo` узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="4a5d5-137">Выберите `Up` клавишу стрелки 2 раза.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="4a5d5-138">.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="4a5d5-140">Проверка `ul` узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-141">Выберите `Left` клавишу стрелки.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="4a5d5-142">Список `<ul>` разрушается.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="4a5d5-143">Снова выберите `Left` клавишу стрелки.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="4a5d5-144">Выбран родительский `<ul>` узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="4a5d5-145">В этом случае это `<div>` с ID `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="4a5d5-146">Выберите клавишу стрелки 2 раза, чтобы повторно выбрать только что свернутый `Down` `<ul>` список.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="4a5d5-147">Это должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="4a5d5-148">Выберите `Right` клавишу стрелки.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="4a5d5-149">Список расширяется.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="4a5d5-150">Прокрутка в представлении</span><span class="sxs-lookup"><span data-stu-id="4a5d5-150">Scroll into view</span></span>  

<span data-ttu-id="4a5d5-151">При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в настоящее время не находится в представлении.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="4a5d5-152">Например, предположим, что вы прокрутки в нижней части страницы, и вас интересует узел в верхней `<h1>` части страницы.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="4a5d5-153">**Прокрутка** в представлении позволяет быстро переместить viewport, чтобы можно было просмотреть узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="4a5d5-154">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-155">В **статье Scroll into View**выберите **магритт** правой точки и выберите **инспект.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="4a5d5-156">Прокрутите в нижней части страницы примеры DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="4a5d5-157">Узел `<li>Magritte</li>` по-прежнему должен быть выбран в dom Tree.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="4a5d5-158">Если нет, возвращайся к [прокрутке в представлении и](#scroll-into-view) начинай сначала.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="4a5d5-159">Наведите курсор на узел, откройте контекстное меню \(правой кнопкой `<li>Magritte</li>` мыши\) и выберите **Прокрутку в вид**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="4a5d5-160">Ваш видпорт прокручивается назад, чтобы просмотреть узел **Magritte.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="4a5d5-161">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если вы не можете просмотреть параметр **Scroll в представлении.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка в представлении" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="4a5d5-163">Прокрутка в представлении</span><span class="sxs-lookup"><span data-stu-id="4a5d5-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="4a5d5-164">Поиск узлов</span><span class="sxs-lookup"><span data-stu-id="4a5d5-164">Search for nodes</span></span>  

<span data-ttu-id="4a5d5-165">Вы можете искать дерево DOM по строке, селектору CSS или селектору XPath.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="4a5d5-166">Сосредоточь курсор на **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="4a5d5-167">Выберите `Control` + `F` \(Windows, Linux\) `Command` + `F` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="4a5d5-168">Строка поиска открывается в нижней части дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="4a5d5-169">Введите `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="4a5d5-170">Последнее предложение выделено в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса в панели поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="4a5d5-172">Выделение запроса в панели поиска</span><span class="sxs-lookup"><span data-stu-id="4a5d5-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4a5d5-173">Как упоминалось выше, в панели поиска также поддерживаются селекторы CSS и XPath.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="4a5d5-174">Изменение DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-174">Edit the DOM</span></span>  

<span data-ttu-id="4a5d5-175">Вы можете изменить DOM на лету и просмотреть, как изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="4a5d5-176">Редактирование контента</span><span class="sxs-lookup"><span data-stu-id="4a5d5-176">Edit content</span></span>  

<span data-ttu-id="4a5d5-177">Чтобы изменить содержимое узла, дважды щелкните содержимое в dom Tree.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="4a5d5-178">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-179">В **статье Редактирование контента**выберите Мишель **правильно и** выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-180">В дереве DOM дважды щелкните `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="4a5d5-181">Другими словами, дважды щелкните текст между `<li>` и `</li>` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="4a5d5-182">Текст выделен, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Изменение текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="4a5d5-184">Изменение текста</span><span class="sxs-lookup"><span data-stu-id="4a5d5-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-185">`Michelle`Удалите, `Leela` введите, а `Enter` затем выберите, чтобы подтвердить изменение.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="4a5d5-186">Текст в DOM изменяется с **Мишель на** **Лилу**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="4a5d5-187">Изменение атрибутов</span><span class="sxs-lookup"><span data-stu-id="4a5d5-187">Edit attributes</span></span>  

<span data-ttu-id="4a5d5-188">Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="4a5d5-189">Следуйте инструкциям, чтобы узнать, как добавлять атрибуты в узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="4a5d5-190">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-191">В **статье Изменить атрибуты**выберите Ховард \*\*\*\* правильно и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="4a5d5-192">Дважды `<li>` щелкните .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-192">Double-click `<li>`.</span></span>  <span data-ttu-id="4a5d5-193">Текст выделен, чтобы указать, что узел выбран.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="4a5d5-195">Изменение узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4a5d5-196">Выберите `Right` клавишу стрелки, добавьте пробел, введите `style="background-color:gold"` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="4a5d5-197">Фоновый цвет узла меняется на золото.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля в узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="4a5d5-199">Добавление `style` атрибута в узел</span><span class="sxs-lookup"><span data-stu-id="4a5d5-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="4a5d5-200">Изменение типа узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-200">Edit node type</span></span>  

<span data-ttu-id="4a5d5-201">Чтобы изменить тип узла, дважды щелкните тип и введите новый тип.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="4a5d5-202">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-203">При **редактировании типа узла**выберите справа **Хэнк** и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-204">Дважды `<li>` щелкните .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-204">Double-click `<li>`.</span></span>  <span data-ttu-id="4a5d5-205">Текст `li` выделен.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="4a5d5-206">`li`Удалите, `button` введите, а затем выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="4a5d5-207">Узел `<li>` изменяется в `<button>` узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="4a5d5-209">Изменение типа узла на</span><span class="sxs-lookup"><span data-stu-id="4a5d5-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="4a5d5-210">Reorder DOM nodes</span><span class="sxs-lookup"><span data-stu-id="4a5d5-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="4a5d5-211">Перетаскивать узлы для их переуборки.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="4a5d5-212">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-213">В **статье Reorder DOM Nodes**выберите правый **элвис Пресли** и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4a5d5-214">Это последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="4a5d5-215">В дереве DOM `<li>Elvis Presley</li>` перетащите в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="4a5d5-217">Перетащите узел в верхнюю часть списка</span><span class="sxs-lookup"><span data-stu-id="4a5d5-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="4a5d5-218">Состояние Force</span><span class="sxs-lookup"><span data-stu-id="4a5d5-218">Force state</span></span>  

<span data-ttu-id="4a5d5-219">Вы можете заставить узлы оставаться в состояниях, включая `:active` , , , , и `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="4a5d5-220">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-221">В **состоянии Force**наведите курсор на **"Властелин мух".**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="4a5d5-222">Цвет фона становится оранжевым.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="4a5d5-223">Наведите курсор на **"Властелин мух",** откройте контекстное меню \(правой кнопкой мыши\) и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-224">Наведите `<li class="demo--hover">The Lord of the Flies</li>` курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Состояние силы**  >  **:hover**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="4a5d5-225">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="4a5d5-226">Цвет фона остается оранжевым, даже если вы на самом деле не зависаете над узлом.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="4a5d5-227">Скрыть узел</span><span class="sxs-lookup"><span data-stu-id="4a5d5-227">Hide a node</span></span>  

<span data-ttu-id="4a5d5-228">Выберите, `H` чтобы скрыть узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="4a5d5-229">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-230">В **статье Скрыть узел**выберите "Звезды моего **назначения"** и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-231">Выберите `H` ключ.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-231">Select the `H` key.</span></span>  <span data-ttu-id="4a5d5-232">Узел скрыт.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Как выглядит узел в dom Tree после его сокрытого" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="4a5d5-234">Как выглядит узел в dom Tree после его сокрытого</span><span class="sxs-lookup"><span data-stu-id="4a5d5-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-235">Выберите `H` клавишу снова.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-235">Select the `H` key again.</span></span>  <span data-ttu-id="4a5d5-236">Узел отображается снова.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="4a5d5-237">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="4a5d5-237">Delete a node</span></span>  

<span data-ttu-id="4a5d5-238">Выберите `Delete` удаление узла.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="4a5d5-239">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-240">В **статье Delete a Node**выберите правильный выбор **Основы** и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-241">Выберите `Delete` ключ.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-241">Select the `Delete` key.</span></span>  <span data-ttu-id="4a5d5-242">Узел удаляется.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="4a5d5-243">Выберите `Control` + `Z` \(Windows, Linux\) `Command` + `Z` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="4a5d5-244">Последнее действие отменить, и узел снова появится.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="4a5d5-245">Доступ к узлам консоли</span><span class="sxs-lookup"><span data-stu-id="4a5d5-245">Access nodes in the Console</span></span>  

<span data-ttu-id="4a5d5-246">DevTools предоставляет несколько ярлыков для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждый из них.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="4a5d5-247">Ссылка на выбранный в настоящее время узел с $0</span><span class="sxs-lookup"><span data-stu-id="4a5d5-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="4a5d5-248">При проверке узла текст рядом с узлом означает, что этот узел в консоли может ссылаться `== $0` на `$0` переменную.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="4a5d5-249">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-250">В статье Ссылка на выбранный в настоящее время **узел с $0**, правой выберите **левую** руку тьмы и выберите **инспектировать**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-251">Выберите ключ `Escape` для открытия ящика консоли.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="4a5d5-252">Введите `$0` и выберите `Enter` ключ.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="4a5d5-253">Результат выражения показывает, что `$0` оценивает до `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="4a5d5-255">Результат первого выражения `$0` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="4a5d5-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-256">Наведите курсор на результат.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-256">Hover on the result.</span></span>  <span data-ttu-id="4a5d5-257">Узел выделен в представлении.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="4a5d5-258">Выберите `<li>Dune</li>` в дереве DOM, введите консоль `$0` снова, а затем выберите еще `Enter` раз.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="4a5d5-259">Теперь `$0` оценивается до `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="4a5d5-261">Результат второго выражения `$0` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="4a5d5-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="4a5d5-262">Хранить как глобальную переменную</span><span class="sxs-lookup"><span data-stu-id="4a5d5-262">Store as global variable</span></span>  

<span data-ttu-id="4a5d5-263">Если требуется много раз возвращаться к узлу, храните его в качестве глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="4a5d5-264">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-265">В **Хранилище в качестве глобальной переменной**наведите курсор на **"Большой**сон", откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-266">Наведите курсор в dom Tree, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li>The Big Sleep</li>` Store в качестве **глобальной переменной.**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="4a5d5-267">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="4a5d5-268">Введите `temp1` консоль и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="4a5d5-269">Результат выражения показывает, что переменная оценивает узел.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="4a5d5-271">Результат выражения `temp1`</span><span class="sxs-lookup"><span data-stu-id="4a5d5-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="4a5d5-272">Путь копирования JS</span><span class="sxs-lookup"><span data-stu-id="4a5d5-272">Copy JS path</span></span>  

<span data-ttu-id="4a5d5-273">Скопируйте путь JavaScript в узел, если необходимо ссылаться на него в автоматическом тесте.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="4a5d5-274">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-275">В **рамках пути Copy JS**наведите курсор на братья Карамазовы, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4a5d5-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-276">Наведите курсор в дереве DOM, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li>The Brothers Karamazov</li>` **путь Копирование**  >  **копии JS**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="4a5d5-277">Выражение, `document.querySelector()` разрешаемая узлу, было скопировано в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="4a5d5-278">Выберите `Control` + `V` \(Windows, Linux\) `Command` + `V` или \(macOS\) для вставки выражения в консоль.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="4a5d5-279">Выберите `Enter` для оценки выражения.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="4a5d5-281">Результат выражения **Copy JS Path**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="4a5d5-282">Перерыв в изменениях DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-282">Break on DOM changes</span></span>  

<span data-ttu-id="4a5d5-283">DevTools позволяет приостановить JavaScript страницы, когда JavaScript изменяет DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="4a5d5-284">Перерыв в изменении атрибута</span><span class="sxs-lookup"><span data-stu-id="4a5d5-284">Break on attribute modifications</span></span>  

<span data-ttu-id="4a5d5-285">Используйте брейк-точки изменения атрибута, когда необходимо приостановить JavaScript, из-за чего любой атрибут узла будет изменяться.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="4a5d5-286">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-287">В **статье Break on attribute modifications**выберите правый выбор **Sauerkraut** и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-288">В дереве DOM наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li id="target">Sauerkraut</li>` **Break On**  >  **Attribute Modifications**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="4a5d5-289">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Перерыв в изменении атрибута" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="4a5d5-291">Перерыв в изменении атрибута</span><span class="sxs-lookup"><span data-stu-id="4a5d5-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-292">На следующем шаге вам будет поручено выбрать кнопку, приостановив код страницы.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="4a5d5-293">После приостановки страницы вы больше не сможете прокручивать страницу.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="4a5d5-294">Для повторного **прокрутки** страницы необходимо выбрать сценарий резюме ![ ][ImageResumeScriptIcon] \.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-294">You must choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Где возобновить работу скрипта" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="4a5d5-296">Где возобновить работу скрипта</span><span class="sxs-lookup"><span data-stu-id="4a5d5-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="4a5d5-297">Выберите **кнопку Set Background** выше.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="4a5d5-298">Это задает `style` атрибут узла `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="4a5d5-299">DevTools останавливает страницу и выделяет код, из-за чего атрибут изменился.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="4a5d5-300">Выберите **сценарий** резюме \. ![ Сценарий ][ImageResumeScriptIcon] резюме \), как упоминалось ранее.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-300">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="4a5d5-301">Перерыв при удалении узлов</span><span class="sxs-lookup"><span data-stu-id="4a5d5-301">Break on node removal</span></span>  

<span data-ttu-id="4a5d5-302">Если необходимо приостановить удаление определенного узла, используйте точки удаления узлов.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="4a5d5-303">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-304">В статье Break on Node Removal (Удаление **узлов)** выберите **справа Neuromancer и** выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-305">В дереве DOM наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li id="target">Neuromancer</li>` **Break On**  >  **Node Removal**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="4a5d5-306">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="4a5d5-307">Выберите **кнопку Удалить** выше.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="4a5d5-308">DevTools останавливает страницу и выделяет код, из-за чего узел был удален.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="4a5d5-309">Выберите **сценарий** резюме \. ![ Сценарий ][ImageResumeScriptIcon] резюме \).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-309">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="4a5d5-310">Перерыв в изменениях подтрия</span><span class="sxs-lookup"><span data-stu-id="4a5d5-310">Break on subtree modifications</span></span>  

<span data-ttu-id="4a5d5-311">После того, как на узел будет добавлена точка взлома модификации подтримки, DevTools приостанавлит страницу при добавлении или удалении любого из потомков узла.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="4a5d5-312">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="4a5d5-313">В **статье Break on Subtree Modifications (Изменения subtree)** выберите правильное решение **"Пожар на глубине"** и выберите **"Проверка".**</span><span class="sxs-lookup"><span data-stu-id="4a5d5-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="4a5d5-314">В дереве DOM наведите курсор , который является узлом выше, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<ul id="target">` `<li>A Fire Upon the Deep</li>` Break **On**  >  **Subtree Modifications**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="4a5d5-315">Если параметр не отображается, перейдите в [Приложение: Отсутствующие параметры.](#appendix-missing-options)</span><span class="sxs-lookup"><span data-stu-id="4a5d5-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="4a5d5-316">Выберите **Добавить ребенка**.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-316">Choose **Add Child**.</span></span>  <span data-ttu-id="4a5d5-317">Код приостанавливовка, так как `<li>` узел был добавлен в список.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="4a5d5-318">Выберите **сценарий** резюме \. ![ Сценарий ][ImageResumeScriptIcon] резюме \).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-318">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="4a5d5-319">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="4a5d5-319">Next steps</span></span>  

<span data-ttu-id="4a5d5-320">Это охватывает большинство функций, связанных с DOM в DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="4a5d5-321">Остальные функции можно обнаружить, зависнув на узлах дерева DOM, открыв контекстное меню \(правой кнопкой мыши\) и поэкспериментируйте с другими вариантами, которые не были охвачены в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="4a5d5-322">Перейдите к [клавишам клавиатуры][DevToolsShortcutsElements]панели Elements .</span><span class="sxs-lookup"><span data-stu-id="4a5d5-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="4a5d5-323">Ознакомьтесь с [домашней страницей Microsoft Edge DevTools,][MicrosoftEdgeDevTools] чтобы узнать все остальное, что вы можете сделать с DevTools.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="4a5d5-324">Приложение: HTML по сравнению с DOM</span><span class="sxs-lookup"><span data-stu-id="4a5d5-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="4a5d5-325">В следующем разделе быстро объясняется разница между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4a5d5-326">При использовании веб-браузера для запроса страницы сервер возвращает HTML, как и следующий фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="4a5d5-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4a5d5-327">Браузер размазирует HTML и создает дерево объектов, таких как следующий список.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4a5d5-328">Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="4a5d5-329">Сейчас он выглядит так же, как HTML, но предположим, что сценарий, на который ссылается в нижней части HTML, выполняет следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="4a5d5-330">Этот код удаляет `h1` узел и добавляет другой узел в `p` DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="4a5d5-331">Полный DOM теперь отображает следующий список.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-331">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="4a5d5-332">HTML для страницы теперь отличается от DOM.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="4a5d5-333">Другими словами, HTML представляет исходное содержимое страницы, а DOM — текущее содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="4a5d5-334">Когда JavaScript добавляет, удаляет или редактирует узлы, DOM становится другим, чем HTML.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="4a5d5-335">Перейдите [к вводу в DOM,][MDNIntroductionToDOM] чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="4a5d5-336">Приложение: отсутствующие параметры</span><span class="sxs-lookup"><span data-stu-id="4a5d5-336">Appendix: Missing options</span></span>  

<span data-ttu-id="4a5d5-337">Многие инструкции в этом руководстве поручают вам наведении на узел в dom Tree, открыть контекстное меню \(правой кнопкой мыши\), а затем выбрать вариант из контекстного меню, которое всплывает.</span><span class="sxs-lookup"><span data-stu-id="4a5d5-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="4a5d5-338">Если указанный параметр в контекстном меню не отображается, попробуйте отойти от текста узла и открыть контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Где выбрать, если все параметры не отображаются" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="4a5d5-340">Где выбрать, если все параметры не отображаются</span><span class="sxs-lookup"><span data-stu-id="4a5d5-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4a5d5-341">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4a5d5-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCssGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Клавиши клавиатуры elements — клавиши Microsoft Edge DevTools Keyboard Shortcuts | Документы Майкрософт"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Example | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в dom | MDN"  

> [!NOTE]
> <span data-ttu-id="4a5d5-347">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4a5d5-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4a5d5-348">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/dom/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="4a5d5-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4a5d5-350">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4a5d5-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
