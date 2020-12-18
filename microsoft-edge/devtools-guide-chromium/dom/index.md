---
description: Просмотр узлов, поиск узлов, изменение узлов, ссылка на узлы в консоли, разрыв изменений узлов и т. д.
title: Начало работы с просмотром и изменением DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5b12b984aed7e35ce11dd45e8bc33f5d5fd454f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231106"
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

# <span data-ttu-id="9529b-104">Начало работы с просмотром и изменением DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="9529b-105">Выполните эти интерактивные учебники, чтобы изучить основы просмотра и изменения DOM страницы с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="9529b-106">В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.</span><span class="sxs-lookup"><span data-stu-id="9529b-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="9529b-107">Перейдите [к приложению: HTML и DOM для](#appendix-html-versus-the-dom) пояснения.</span><span class="sxs-lookup"><span data-stu-id="9529b-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="9529b-108">Открытые примеры DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="9529b-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span><span class="sxs-lookup"><span data-stu-id="9529b-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="9529b-110">Примеры DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="9529b-111">Просмотр узлов DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-111">View DOM nodes</span></span>  

<span data-ttu-id="9529b-112">Дерево DOM панели элементов — это место, в котором вы можете делать все действия, связанные с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="9529b-113">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="9529b-113">Inspect a node</span></span>  

<span data-ttu-id="9529b-114">Если вас интересует определенный узел DOM, **проверьте** это быстрый способ открыть DevTools и изучить этот узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="9529b-115">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-116">В **области "Проверка узла"** правой стороной выберите **"Майклангело" и** выберите **"Проверить".**</span><span class="sxs-lookup"><span data-stu-id="9529b-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="9529b-118">Проверка узла</span><span class="sxs-lookup"><span data-stu-id="9529b-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="9529b-119">Откроется **панель элементов** DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="9529b-120">выделен в дереве **DOM.**</span><span class="sxs-lookup"><span data-stu-id="9529b-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла "Майкланголо"" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="9529b-122">Выделение `Michelangelo` узла</span><span class="sxs-lookup"><span data-stu-id="9529b-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="9529b-123">Щелкните **значок "Проверить"** в левом верхнем углу ![ ][ImageInspectIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-123">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок "Проверка"" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="9529b-125">Значок **"Проверка"**</span><span class="sxs-lookup"><span data-stu-id="9529b-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="9529b-126">В **области "Проверка узла"** щелкните **текст в Токио.**</span><span class="sxs-lookup"><span data-stu-id="9529b-126">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="9529b-127">Теперь `<li>Tokyo</li>` он выделен в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="9529b-128">Проверка узла также является первым шагом к просмотру и изменению стилей узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="9529b-129">Перейдите [к началу работы с просмотром и изменением CSS.][DevToolsCssGetStarted]</span><span class="sxs-lookup"><span data-stu-id="9529b-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="9529b-130">Навигация по дереву DOM с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="9529b-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="9529b-131">Выбрав узел в дереве DOM, можно перейти к дереву DOM с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="9529b-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="9529b-132">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-133">Under **Navigate the DOM Tree with a Keyboard,** right-choose **Ringo** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="9529b-134">выбран в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="9529b-136">Проверка `Ringo` узла</span><span class="sxs-lookup"><span data-stu-id="9529b-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="9529b-137">Нажмите `Up` клавишу со стрелкой 2 раза.</span><span class="sxs-lookup"><span data-stu-id="9529b-137">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="9529b-138">.</span><span class="sxs-lookup"><span data-stu-id="9529b-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="9529b-140">Проверка `ul` узла</span><span class="sxs-lookup"><span data-stu-id="9529b-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-141">Нажмите `Left` клавишу со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="9529b-141">Press the `Left` arrow key.</span></span>  <span data-ttu-id="9529b-142">Список `<ul>` свернут.</span><span class="sxs-lookup"><span data-stu-id="9529b-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="9529b-143">Нажмите `Left` клавишу со стрелкой еще раз.</span><span class="sxs-lookup"><span data-stu-id="9529b-143">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="9529b-144">Выбран родительский узел `<ul>` узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="9529b-145">В этом случае это с `<div>` `navigate-the-dom-tree-with-a-keyboard-1` ИД.</span><span class="sxs-lookup"><span data-stu-id="9529b-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="9529b-146">Нажмите `Down` клавишу со стрелкой 2 раза, чтобы повторно выбрать свернутый `<ul>` список.</span><span class="sxs-lookup"><span data-stu-id="9529b-146">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="9529b-147">Это должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9529b-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="9529b-148">Нажмите `Right` клавишу со стрелкой.</span><span class="sxs-lookup"><span data-stu-id="9529b-148">Press the `Right` arrow key.</span></span>  <span data-ttu-id="9529b-149">Список расширяется.</span><span class="sxs-lookup"><span data-stu-id="9529b-149">The list expands.</span></span>  

### <span data-ttu-id="9529b-150">Прокрутка в представление</span><span class="sxs-lookup"><span data-stu-id="9529b-150">Scroll into view</span></span>  

<span data-ttu-id="9529b-151">При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в настоящее время не находится в окле просмотра.</span><span class="sxs-lookup"><span data-stu-id="9529b-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="9529b-152">Например, предположим, что вы прокручивали страницу вниз и вас интересует узел в `<h1>` верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="9529b-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="9529b-153">**Прокрутка в представлении** позволяет быстро изменить расположение окна, чтобы можно было просмотреть узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="9529b-154">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="9529b-156">Прокрутите страницу DOM Examples до конца.</span><span class="sxs-lookup"><span data-stu-id="9529b-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="9529b-157">Узел `<li>Magritte</li>` по-прежнему должен быть выбран в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="9529b-158">Если нет, перейти к [прокрутке в представлении и](#scroll-into-view) начать все сначала.</span><span class="sxs-lookup"><span data-stu-id="9529b-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="9529b-159">Наведите курсор на узел, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите `<li>Magritte</li>` пункт **"Прокрутка в представление".**</span><span class="sxs-lookup"><span data-stu-id="9529b-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="9529b-160">В окну просмотра можно просмотреть узел **Magritte.**</span><span class="sxs-lookup"><span data-stu-id="9529b-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="9529b-161">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если вы не можете просмотреть параметр **"Прокрутка в** представлении".</span><span class="sxs-lookup"><span data-stu-id="9529b-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка в представление" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="9529b-163">Прокрутка в представление</span><span class="sxs-lookup"><span data-stu-id="9529b-163">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="9529b-164">Поиск узлов</span><span class="sxs-lookup"><span data-stu-id="9529b-164">Search for nodes</span></span>  

<span data-ttu-id="9529b-165">Вы можете искать в дереве DOM по строке, селектору CSS или селектору XPath.</span><span class="sxs-lookup"><span data-stu-id="9529b-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="9529b-166">На панели элементов выделите **курсор.**</span><span class="sxs-lookup"><span data-stu-id="9529b-166">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="9529b-167">Выберите `Control` + `F` \(Windows, Linux\) или `Command` + `F` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9529b-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="9529b-168">В нижней части дерева DOM откроется строка поиска.</span><span class="sxs-lookup"><span data-stu-id="9529b-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="9529b-169">Введите `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="9529b-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="9529b-170">Последнее предложение выделено в дереве DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса на панели поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="9529b-172">Выделение запроса на панели поиска</span><span class="sxs-lookup"><span data-stu-id="9529b-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9529b-173">Как упоминалось выше, на панели поиска также поддерживаются селекторы CSS и XPath.</span><span class="sxs-lookup"><span data-stu-id="9529b-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="9529b-174">Изменение DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-174">Edit the DOM</span></span>  

<span data-ttu-id="9529b-175">Вы можете изменить DOM во время и просмотреть, как изменения влияют на страницу.</span><span class="sxs-lookup"><span data-stu-id="9529b-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <span data-ttu-id="9529b-176">Редактирование содержимого</span><span class="sxs-lookup"><span data-stu-id="9529b-176">Edit content</span></span>  

<span data-ttu-id="9529b-177">Чтобы изменить содержимое узла, дважды щелкните содержимое дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="9529b-178">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-179">В **области "Изменение содержимого"** выберите **" Michelle" (Изменить** содержимое) и выберите **"Inspect" (Проверить).**</span><span class="sxs-lookup"><span data-stu-id="9529b-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-180">В дереве DOM дважды щелкните `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="9529b-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="9529b-181">Другими словами, дважды щелкните текст между `<li>` и `</li>` .</span><span class="sxs-lookup"><span data-stu-id="9529b-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="9529b-182">Текст выделен, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="9529b-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Редактирование текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="9529b-184">Редактирование текста</span><span class="sxs-lookup"><span data-stu-id="9529b-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-185">Delete `Michelle` , type , then select to confirm the `Leela` `Enter` change.</span><span class="sxs-lookup"><span data-stu-id="9529b-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="9529b-186">Текст в DOM изменяется с **Michelle** на **Leela**.</span><span class="sxs-lookup"><span data-stu-id="9529b-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="9529b-187">Изменение атрибутов</span><span class="sxs-lookup"><span data-stu-id="9529b-187">Edit attributes</span></span>  

<span data-ttu-id="9529b-188">Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="9529b-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="9529b-189">Следуйте инструкциям, чтобы узнать, как добавить атрибуты в узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="9529b-190">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-191">В **области "Изменить атрибуты"** выберите "Химки" и выберите **"Проверить".** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9529b-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="9529b-192">Дважды `<li>` щелкните .</span><span class="sxs-lookup"><span data-stu-id="9529b-192">Double-click `<li>`.</span></span>  <span data-ttu-id="9529b-193">Текст выделен, чтобы указать, что узел выбран.</span><span class="sxs-lookup"><span data-stu-id="9529b-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="9529b-195">Изменение узла</span><span class="sxs-lookup"><span data-stu-id="9529b-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9529b-196">Нажмите `Right` клавишу со стрелкой, добавьте пробел, введите `style="background-color:gold"` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9529b-196">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="9529b-197">Цвет фона узла изменяется на gold.</span><span class="sxs-lookup"><span data-stu-id="9529b-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля в узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="9529b-199">Добавление `style` атрибута в узел</span><span class="sxs-lookup"><span data-stu-id="9529b-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9529b-200">Изменение типа узла</span><span class="sxs-lookup"><span data-stu-id="9529b-200">Edit node type</span></span>  

<span data-ttu-id="9529b-201">Чтобы изменить тип узла, дважды щелкните тип и введите новый тип.</span><span class="sxs-lookup"><span data-stu-id="9529b-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="9529b-202">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-203">В **области "Изменить тип узла"** выберите правой правой выберите **"Инсайт"** и выберите **"Проверить".**</span><span class="sxs-lookup"><span data-stu-id="9529b-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-204">Дважды `<li>` щелкните .</span><span class="sxs-lookup"><span data-stu-id="9529b-204">Double-click `<li>`.</span></span>  <span data-ttu-id="9529b-205">Текст `li` выделен.</span><span class="sxs-lookup"><span data-stu-id="9529b-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="9529b-206">Delete `li` , type , then select `button` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9529b-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="9529b-207">Узел `<li>` изменяется на `<button>` узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="9529b-209">Измените тип узла на</span><span class="sxs-lookup"><span data-stu-id="9529b-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="9529b-210">Переусортовка узлов DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="9529b-211">Перетащите узлы, чтобы переусортовить их.</span><span class="sxs-lookup"><span data-stu-id="9529b-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="9529b-212">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-213">В **области "Reorder DOM Nodes" (Узлы DOM reorder)** выберите **"Elvis Presley" (Elvis Presley)** и выберите **"Inspect"**(Проверить).</span><span class="sxs-lookup"><span data-stu-id="9529b-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9529b-214">Это последний элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="9529b-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="9529b-215">В дереве DOM перетащите `<li>Elvis Presley</li>` его в верхнюю часть списка.</span><span class="sxs-lookup"><span data-stu-id="9529b-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="9529b-217">Перетащите узел в верхнюю часть списка</span><span class="sxs-lookup"><span data-stu-id="9529b-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="9529b-218">Состояние принудительного применения</span><span class="sxs-lookup"><span data-stu-id="9529b-218">Force state</span></span>  

<span data-ttu-id="9529b-219">Вы можете заставить узлы оставаться в состояниях, включая `:active` , , , , и `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="9529b-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="9529b-220">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-221">В **состоянии Force**наведите курсор на **"Химя".**</span><span class="sxs-lookup"><span data-stu-id="9529b-221">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="9529b-222">Цвет фона становится оранжевым.</span><span class="sxs-lookup"><span data-stu-id="9529b-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="9529b-223">Right-choose **The The Of the Овне** и choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-223">Right-choose **The Lord of the Flies** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-224">Щелкните правой `<li class="demo--hover">The Lord of the Flies</li>` кнопкой мыши и выберите **force State**  >  **:hover**.</span><span class="sxs-lookup"><span data-stu-id="9529b-224">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="9529b-225">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="9529b-226">Цвет фона остается оранжевым, даже если вы на самом деле не наведите курсор на узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="9529b-227">Скрытие узла</span><span class="sxs-lookup"><span data-stu-id="9529b-227">Hide a node</span></span>  

<span data-ttu-id="9529b-228">Выберите, `H` чтобы скрыть узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="9529b-229">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-230">В **области "Скрыть узел"** выберите пункт "Звездочки" **и** выберите пункт **"Проверить".**</span><span class="sxs-lookup"><span data-stu-id="9529b-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-231">Нажмите `H` клавишу.</span><span class="sxs-lookup"><span data-stu-id="9529b-231">Press the `H` key.</span></span>  <span data-ttu-id="9529b-232">Узел скрыт.</span><span class="sxs-lookup"><span data-stu-id="9529b-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Внешний вид узла в дереве DOM после его скрытия" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="9529b-234">Внешний вид узла в дереве DOM после его скрытия</span><span class="sxs-lookup"><span data-stu-id="9529b-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-235">Снова нажмите `H` клавишу.</span><span class="sxs-lookup"><span data-stu-id="9529b-235">Press the `H` key again.</span></span>  <span data-ttu-id="9529b-236">Узел снова отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-236">The node is shown again.</span></span>  

### <span data-ttu-id="9529b-237">Удаление узла</span><span class="sxs-lookup"><span data-stu-id="9529b-237">Delete a node</span></span>  

<span data-ttu-id="9529b-238">Выберите, `Delete` чтобы удалить узел.</span><span class="sxs-lookup"><span data-stu-id="9529b-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="9529b-239">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-241">Нажмите `Delete` клавишу.</span><span class="sxs-lookup"><span data-stu-id="9529b-241">Press the `Delete` key.</span></span>  <span data-ttu-id="9529b-242">Узел удаляется.</span><span class="sxs-lookup"><span data-stu-id="9529b-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="9529b-243">Выберите `Control` + `Z` \(Windows, Linux\) или `Command` + `Z` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9529b-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="9529b-244">Последнее действие отменено, и узел снова появляется.</span><span class="sxs-lookup"><span data-stu-id="9529b-244">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="9529b-245">Доступ к узлам в консоли</span><span class="sxs-lookup"><span data-stu-id="9529b-245">Access nodes in the Console</span></span>  

<span data-ttu-id="9529b-246">DevTools предоставляет несколько ярлыков для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждый из них.</span><span class="sxs-lookup"><span data-stu-id="9529b-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="9529b-247">Ссылка на текущий выбранный узел с помощью $0</span><span class="sxs-lookup"><span data-stu-id="9529b-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="9529b-248">При проверке узла текст рядом с узлом означает, что вы можете ссылаться на этот узел в консоли `== $0` с `$0` переменной.</span><span class="sxs-lookup"><span data-stu-id="9529b-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="9529b-249">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand ofЯs** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-251">Нажмите `Escape` клавишу, чтобы открыть консольный ящик.</span><span class="sxs-lookup"><span data-stu-id="9529b-251">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="9529b-252">Введите `$0` и нажмите `Enter` клавишу.</span><span class="sxs-lookup"><span data-stu-id="9529b-252">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="9529b-253">Результат выражения показывает, что `$0` он оценивается как `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="9529b-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="9529b-255">Результат первого выражения `$0` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="9529b-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-256">Наведите курсор на результат.</span><span class="sxs-lookup"><span data-stu-id="9529b-256">Hover over the result.</span></span>  <span data-ttu-id="9529b-257">Узел выделен в окле просмотра.</span><span class="sxs-lookup"><span data-stu-id="9529b-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="9529b-258">Щелкните дерево DOM, введите в консоли еще `<li>Dune</li>` `$0` раз, а затем выберите `Enter` еще раз.</span><span class="sxs-lookup"><span data-stu-id="9529b-258">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="9529b-259">Теперь `$0` оценивается как `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="9529b-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="9529b-261">Результат второго выражения `$0` в \*\*\*\* консоли</span><span class="sxs-lookup"><span data-stu-id="9529b-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="9529b-262">Сохранить как глобальную переменную</span><span class="sxs-lookup"><span data-stu-id="9529b-262">Store as global variable</span></span>  

<span data-ttu-id="9529b-263">Если требуется много раз сослаться на узел, храните его как глобальную переменную.</span><span class="sxs-lookup"><span data-stu-id="9529b-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="9529b-264">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-265">Under **Store as global variable**, right-choose The Big **Sleep** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-265">Under **Store as global variable**, right-choose **The Big Sleep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-266">Щелкните правой `<li>The Big Sleep</li>` кнопкой мыши дерево DOM и выберите **"Магазин" в качестве глобальной переменной.**</span><span class="sxs-lookup"><span data-stu-id="9529b-266">Right-click `<li>The Big Sleep</li>` in the DOM Tree and choose **Store as global variable**.</span></span>  <span data-ttu-id="9529b-267">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="9529b-268">Введите `temp1` в консоли и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="9529b-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="9529b-269">Результат выражения показывает, что переменная оценивается в узле.</span><span class="sxs-lookup"><span data-stu-id="9529b-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="9529b-271">Результат выражения `temp1`</span><span class="sxs-lookup"><span data-stu-id="9529b-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="9529b-272">Копирование пути JS</span><span class="sxs-lookup"><span data-stu-id="9529b-272">Copy JS path</span></span>  

<span data-ttu-id="9529b-273">Скопируйте путь JavaScript к узлу, если вам нужно со ссылкой на него в автоматическом тесте.</span><span class="sxs-lookup"><span data-stu-id="9529b-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="9529b-274">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-275">В **области "Копировать путь JS"** выберите правой копией **"Иван Иванов"** и выберите **"Проверить".**</span><span class="sxs-lookup"><span data-stu-id="9529b-275">Under **Copy JS path**, right-choose **The Brothers Karamazov** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-276">Щелкните правой кнопкой мыши в дереве DOM и выберите `<li>The Brothers Karamazov</li>` **"Копировать**путь  >  **JS копирования".**</span><span class="sxs-lookup"><span data-stu-id="9529b-276">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="9529b-277">Выражение, `document.querySelector()` разрешаемого в узел, было скопировано в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="9529b-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="9529b-278">Выберите `Control` + `V` \(Windows, Linux\) или `Command` + `V` \(macOS\) для вставки выражения в консоль.</span><span class="sxs-lookup"><span data-stu-id="9529b-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="9529b-279">Выберите, `Enter` чтобы оценить выражение.</span><span class="sxs-lookup"><span data-stu-id="9529b-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения "Путь копирования JS"" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="9529b-281">Результат выражения **"Путь копирования JS"**</span><span class="sxs-lookup"><span data-stu-id="9529b-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="9529b-282">Приостановка изменений DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-282">Break on DOM changes</span></span>  

<span data-ttu-id="9529b-283">DevTools позволяет приостановить JavaScript страницы, когда JavaScript изменяет DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="9529b-284">Приорвать изменение атрибута</span><span class="sxs-lookup"><span data-stu-id="9529b-284">Break on attribute modifications</span></span>  

<span data-ttu-id="9529b-285">Используйте точки останова изменения атрибутов, если необходимо приостановить JavaScript, что приводит к изменению любого атрибута узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="9529b-286">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-287">Under **Break on attribute modifications,** right-choose **Sauerkraut** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-288">В дереве DOM щелкните правой кнопкой мыши и выберите `<li id="target">Sauerkraut</li>` "Приорвать \*\*\*\*  >  **при изменении атрибута".**</span><span class="sxs-lookup"><span data-stu-id="9529b-288">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="9529b-289">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Приорвать изменение атрибута" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="9529b-291">Приорвать изменение атрибута</span><span class="sxs-lookup"><span data-stu-id="9529b-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-292">На следующем этапе вам будет выдано указание нажать кнопку, которая приостановит код страницы.</span><span class="sxs-lookup"><span data-stu-id="9529b-292">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="9529b-293">После приостановки страницы вы больше не сможете прокручивать страницу.</span><span class="sxs-lookup"><span data-stu-id="9529b-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="9529b-294">Необходимо выбрать **сценарий возобновления** \( Resume Script \), чтобы снова сделать страницу ![ ][ImageResumeScriptIcon] прокручиваемой.</span><span class="sxs-lookup"><span data-stu-id="9529b-294">You must choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Where to resume script running" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="9529b-296">Where to resume script running</span><span class="sxs-lookup"><span data-stu-id="9529b-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="9529b-297">Нажмите **кнопку "Установить фон"** выше.</span><span class="sxs-lookup"><span data-stu-id="9529b-297">Click the **Set Background** button above.</span></span>  <span data-ttu-id="9529b-298">При этом для `style` атрибута узла устанавливается `background-color:thistle` ".</span><span class="sxs-lookup"><span data-stu-id="9529b-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="9529b-299">DevTools приостанавлиет страницу и выделяет код, который вызвал изменение атрибута.</span><span class="sxs-lookup"><span data-stu-id="9529b-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="9529b-300">Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \), as mentioned earlier.</span><span class="sxs-lookup"><span data-stu-id="9529b-300">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="9529b-301">Приорвать удаление узла</span><span class="sxs-lookup"><span data-stu-id="9529b-301">Break on node removal</span></span>  

<span data-ttu-id="9529b-302">Если необходимо приостановить удаление определенного узла, используйте точки останова удаления узлов.</span><span class="sxs-lookup"><span data-stu-id="9529b-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="9529b-303">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-304">В **окне "Приорвать при удалении узла"** выберите "Неуловимый" и выберите **"Проверить".** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9529b-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-305">В дереве DOM щелкните правой кнопкой мыши и выберите `<li id="target">Neuromancer</li>` **"Приорвать удаление**  >  **узла".**</span><span class="sxs-lookup"><span data-stu-id="9529b-305">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="9529b-306">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="9529b-307">Нажмите **кнопку "Удалить"** выше.</span><span class="sxs-lookup"><span data-stu-id="9529b-307">Click the **Delete** button above.</span></span>  <span data-ttu-id="9529b-308">DevTools приостанавлиет страницу и выделяет код, который вызвал удаление узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="9529b-309">Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9529b-309">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="9529b-310">Приорвать изменения подtree</span><span class="sxs-lookup"><span data-stu-id="9529b-310">Break on subtree modifications</span></span>  

<span data-ttu-id="9529b-311">После того как вы добавили точку останова изменения подпотека на узел, DevTools приостанавлит страницу при добавлении или удалении любого из потомков узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="9529b-312">[Откройте примеры DOM.](#open-dom-examples)</span><span class="sxs-lookup"><span data-stu-id="9529b-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="9529b-313">Under **Break on Subtree Modifications**, right-choose **A Fire On The Deep** and choose **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="9529b-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="9529b-314">В дереве DOM щелкните правой кнопкой мыши узел выше и выберите "Break `<ul id="target">` `<li>A Fire Upon the Deep</li>` **On**  >  **Subtree Modifications".**</span><span class="sxs-lookup"><span data-stu-id="9529b-314">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="9529b-315">Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.</span><span class="sxs-lookup"><span data-stu-id="9529b-315">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="9529b-316">Choose **Add Child**.</span><span class="sxs-lookup"><span data-stu-id="9529b-316">Choose **Add Child**.</span></span>  <span data-ttu-id="9529b-317">Код приостанавливовка, так как `<li>` узел был добавлен в список.</span><span class="sxs-lookup"><span data-stu-id="9529b-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="9529b-318">Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9529b-318">Choose **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="9529b-319">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9529b-319">Next steps</span></span>  

<span data-ttu-id="9529b-320">Это охватывает большинство функций, связанных с DOM, в DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="9529b-321">Остальные узлы можно найти, щелкнув правой кнопкой мыши узлы в дереве DOM и поэкспериментируйте с другими вариантами, которые не были охвачены в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="9529b-321">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="9529b-322">Перейдите [к сочетаниям клавиш панели элементов.][DevToolsShortcutsElements]</span><span class="sxs-lookup"><span data-stu-id="9529b-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="9529b-323">Ознакомьтесь [с домашней страницей Microsoft Edge DevTools,][MicrosoftEdgeDevTools] чтобы узнать все остальные возможности, которые вы можете сделать с DevTools.</span><span class="sxs-lookup"><span data-stu-id="9529b-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <span data-ttu-id="9529b-324">Приложение: HTML и DOM</span><span class="sxs-lookup"><span data-stu-id="9529b-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="9529b-325">В следующем разделе быстро объясняется разница между HTML и DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9529b-326">При использовании веб-браузера для запроса страницы сервер возвращает HTML, как в следующем фрагменте кода</span><span class="sxs-lookup"><span data-stu-id="9529b-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="9529b-327">Браузер проансирует HTML-код и создает дерево объектов, таких как следующий список.</span><span class="sxs-lookup"><span data-stu-id="9529b-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="9529b-328">Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9529b-329">Сейчас он выглядит так же, как HTML, но предположим, что сценарий, на который ссылается в нижней части HTML, выполняет следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="9529b-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9529b-330">Этот код удаляет узел `h1` и добавляет другой узел в `p` DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="9529b-331">Полная doM теперь отображает следующий список.</span><span class="sxs-lookup"><span data-stu-id="9529b-331">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="9529b-332">HTML-код страницы теперь отличается от DOM.</span><span class="sxs-lookup"><span data-stu-id="9529b-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="9529b-333">Другими словами, HTML представляет исходное содержимое страницы, а DOM — текущее содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="9529b-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="9529b-334">Когда JavaScript добавляет, удаляет или редактирует узлы, DOM становится не так, как HTML.</span><span class="sxs-lookup"><span data-stu-id="9529b-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="9529b-335">Чтобы узнать [больше, перейдите в "Введение][MDNIntroductionToDOM] в DOM".</span><span class="sxs-lookup"><span data-stu-id="9529b-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <span data-ttu-id="9529b-336">Приложение: отсутствуют параметры</span><span class="sxs-lookup"><span data-stu-id="9529b-336">Appendix: Missing options</span></span>  

<span data-ttu-id="9529b-337">Многие инструкции в этом руководстве предписывают щелкнуть правой кнопкой мыши узел в дереве DOM, а затем выбрать параметр из всплывающее контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="9529b-337">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="9529b-338">Если указанный параметр в контекстное меню не отображается, попробуйте щелкнуть правой кнопкой мыши текст узла.</span><span class="sxs-lookup"><span data-stu-id="9529b-338">If the specified option in the context menu is not displayed, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Где выбрать, если все параметры не отображаются" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="9529b-340">Где выбрать, если все параметры не отображаются</span><span class="sxs-lookup"><span data-stu-id="9529b-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <span data-ttu-id="9529b-341">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9529b-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCssGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-panel-keyboard-shortcuts "Сочетания клавиш панели элементов — Microsoft Edge DevTools Keyboard Shortcuts | Документы Майкрософт"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Example | Временный сбой"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="9529b-347">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9529b-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9529b-348">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/dom/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9529b-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9529b-350">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9529b-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
