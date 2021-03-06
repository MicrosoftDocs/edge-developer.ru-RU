---
description: Узнайте, как использовать Microsoft Edge DevTools для просмотра и изменения CSS страницы.
title: Начало работы с просмотром и редактированием CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399094"
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

# <a name="get-started-with-viewing-and-changing-css"></a><span data-ttu-id="a5a91-104">Начало работы с просмотром и редактированием CSS</span><span class="sxs-lookup"><span data-stu-id="a5a91-104">Get started with viewing and changing CSS</span></span>  

<span data-ttu-id="a5a91-105">Выполните эти интерактивные учебники, чтобы узнать основы просмотра и изменения CSS для страницы с помощью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="a5a91-105">Complete these interactive tutorials to learn the basics of viewing and changing the CSS for a page using Microsoft Edge DevTools.</span></span>  

## <a name="open-css-examples"></a><span data-ttu-id="a5a91-106">Откройте примеры CSS</span><span class="sxs-lookup"><span data-stu-id="a5a91-106">Open CSS Examples</span></span>  

1.  <span data-ttu-id="a5a91-107">Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **CSS Examples** для открытия в новом окне.</span><span class="sxs-lookup"><span data-stu-id="a5a91-107">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.</span></span>  
    
    [<span data-ttu-id="a5a91-108">Примеры CSS</span><span class="sxs-lookup"><span data-stu-id="a5a91-108">CSS Examples</span></span>][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > <span data-ttu-id="a5a91-109">Если вы хотите пристыковаться к окну [DevTools][DevToolsCustomizePlacement] справа от вашего viewport \(отображается на следующем рисунке\), выберите Настройка и управление **DevTools** `...` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-109">If you want to [dock your DevTools window][DevToolsCustomizePlacement] to the right of your viewport \(displayed in the following figure\), choose **Customize and control DevTools** `...`.</span></span>  <span data-ttu-id="a5a91-110">В разделе Настройка и управление выпадаемым меню **DevTools** в разделе **Док-станция** выберите **док справа.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-110">On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose **Dock to right**.</span></span>  
    
## <a name="view-the-css-for-an-element"></a><span data-ttu-id="a5a91-111">Просмотр CSS для элемента</span><span class="sxs-lookup"><span data-stu-id="a5a91-111">View the CSS for an element</span></span>  

1.  <span data-ttu-id="a5a91-112">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a5a91-112">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a5a91-113">Наведите `Inspect Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-113">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="a5a91-114">В DevTools на **элементе Elements** на панели **дерева DOM** элемент `Inspect Me!` выделяется.</span><span class="sxs-lookup"><span data-stu-id="a5a91-114">In DevTools, on the **Elements** tool, in the **DOM Tree** panel, the `Inspect Me!` element is highlighted.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Элемент проверки выделен в дереве DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           <span data-ttu-id="a5a91-116">Элемент проверки выделен в **дереве DOM**</span><span class="sxs-lookup"><span data-stu-id="a5a91-116">The inspected element is highlighted in the **DOM Tree**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="a5a91-117">В `Inspect Me!` элементе найдите значение атрибута `data-message` и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="a5a91-117">In the `Inspect Me!` element, find the value of the `data-message` attribute and copy it.</span></span>  
1.  <span data-ttu-id="a5a91-118">На странице в **значении `data-message` : textbox** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a5a91-118">On the page, in the **Value of `data-message`:** textbox, enter the value.</span></span>  
1.  <span data-ttu-id="a5a91-119">Наведите `Inspect Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-119">Hover on the `Inspect Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="a5a91-120">В DevTools на **инструменте Elements** выберите панель **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-120">In DevTools, on the **Elements** tool, select the **Styles** panel.</span></span>  
    1.  <span data-ttu-id="a5a91-121">В панели **Styles** элемент `Inspect Me!` выделяется.</span><span class="sxs-lookup"><span data-stu-id="a5a91-121">In the **Styles** panel, the `Inspect Me!` element is highlighted.</span></span>  
    1.  <span data-ttu-id="a5a91-122">В `Inspect Me!` элементе найдите `aloha` правило класса.</span><span class="sxs-lookup"><span data-stu-id="a5a91-122">In the `Inspect Me!` element, find the `aloha` class rule.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="a5a91-123">Это правило отображается, так как оно применяется к `Inspect Me!` элементу.</span><span class="sxs-lookup"><span data-stu-id="a5a91-123">This rule is displayed, because it is being applied to the `Inspect Me!` element.</span></span>  
        
    1.  <span data-ttu-id="a5a91-124">В классе `aloha` найдите значение для `padding` стиля и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="a5a91-124">In the `aloha` class, find the value for the `padding` style and copy it.</span></span>  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Классы CSS применяются к проверенному элементу, выделенному в панели Styles" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           <span data-ttu-id="a5a91-126">Классы CSS применяются к выбранному элементу, например, отображаются `aloha` в панели **Styles**</span><span class="sxs-lookup"><span data-stu-id="a5a91-126">CSS classes is applied to the selected element, such as `aloha`, are displayed in the **Styles** panel</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="a5a91-127">На странице в **значении `padding` : textbox** введите значение.</span><span class="sxs-lookup"><span data-stu-id="a5a91-127">On the page, in the **Value of `padding`:** textbox, enter the value.</span></span>  

## <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="a5a91-128">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="a5a91-128">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="a5a91-129">Используйте панель **Стилей,** чтобы изменить или добавить в элемент объявления CSS.</span><span class="sxs-lookup"><span data-stu-id="a5a91-129">Use the **Styles** panel when you want to change or add CSS declarations to an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5a91-130">Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.</span><span class="sxs-lookup"><span data-stu-id="a5a91-130">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a5a91-131">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a5a91-131">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a5a91-132">Наведите `Add A Background Color To Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-132">Hover on the `Add A Background Color To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a5a91-133">Выберите `element.style` в верхней части панели **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-133">Choose `element.style` near the top of the **Styles** panel.</span></span>  
1.  <span data-ttu-id="a5a91-134">Введите `background-color` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-134">Type `background-color` and select `Enter`.</span></span>  
1.  <span data-ttu-id="a5a91-135">Введите `honeydew` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-135">Type `honeydew` and select `Enter`.</span></span>  <span data-ttu-id="a5a91-136">В **dom Tree**отображается вложенное объявление стиля, примененное к элементу.</span><span class="sxs-lookup"><span data-stu-id="a5a91-136">In the **DOM Tree**, an inline style declaration applied to the element is displayed.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Добавление объявления CSS в элемент с помощью панели Стилей" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       <span data-ttu-id="a5a91-138">Объявление `background-color:honeydew` применяется к элементу с помощью раздела панели `element.style` **Стилей**</span><span class="sxs-lookup"><span data-stu-id="a5a91-138">The `background-color:honeydew` declaration is applied to the element using the `element.style` section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a><span data-ttu-id="a5a91-139">Добавление класса CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="a5a91-139">Add a CSS class to an element</span></span>  

<span data-ttu-id="a5a91-140">Чтобы отобразить внешний вид элемента при применении класса CSS к элементу или его удалении, перейдите на панель **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-140">To display how an element looks when a CSS class is applied to or removed from an element, navigate to the **Styles** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5a91-141">Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.</span><span class="sxs-lookup"><span data-stu-id="a5a91-141">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a5a91-142">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a5a91-142">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a5a91-143">Наведите `Add A Class To Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-143">Hover on the `Add A Class To Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a5a91-144">Выберите **.cls**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-144">Choose **.cls**.</span></span>  <span data-ttu-id="a5a91-145">DevTools открывает текстовое поле, в котором можно добавить классы к выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="a5a91-145">DevTools reveals a text box where you may add classes to the selected element.</span></span>  
1.  <span data-ttu-id="a5a91-146">`color_me`Введите **текстовое поле Добавить новый класс** и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-146">Type `color_me` in the **Add new class** text box and then select `Enter`.</span></span>  <span data-ttu-id="a5a91-147">В текстовом окне **Добавить новый** класс отображается почтовый ящик, в котором можно отключить класс.</span><span class="sxs-lookup"><span data-stu-id="a5a91-147">A checkbox appears below the **Add new class** text box, where you may toggle the class on and off.</span></span>  <span data-ttu-id="a5a91-148">Если к элементу применены какие-либо другие классы, вы также можете ото всех `Add A Class To Me!` перегнастить.</span><span class="sxs-lookup"><span data-stu-id="a5a91-148">If the `Add A Class To Me!` element has any other classes applied to it, you are also able to toggle each from here.</span></span>  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Применить класс color_me к элементу" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       <span data-ttu-id="a5a91-150">Класс применяется к элементу с `color_me` помощью раздела **.cls** панели **Styles**</span><span class="sxs-lookup"><span data-stu-id="a5a91-150">The `color_me` class is applied to the element using the **.cls** section of the **Styles** panel</span></span>  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a><span data-ttu-id="a5a91-151">Добавление псевдостата в класс</span><span class="sxs-lookup"><span data-stu-id="a5a91-151">Add a pseudostate to a class</span></span>  

<span data-ttu-id="a5a91-152">Используйте панель **Стилей** для постоянного применения псевдостата CSS к элементу.</span><span class="sxs-lookup"><span data-stu-id="a5a91-152">Use the **Styles** panel to permanently apply a CSS pseudostate to an element.</span></span>  <span data-ttu-id="a5a91-153">DevTools поддерживает `:active` `:focus` , и `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-153">DevTools supports `:active`, `:focus`, `:hover`, and `:visited`.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5a91-154">Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.</span><span class="sxs-lookup"><span data-stu-id="a5a91-154">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a5a91-155">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a5a91-155">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a5a91-156">Наведите курсор `Hover Over Me!` на текст.</span><span class="sxs-lookup"><span data-stu-id="a5a91-156">Hover on the `Hover Over Me!` text.</span></span>  <span data-ttu-id="a5a91-157">Меняется цвет фона.</span><span class="sxs-lookup"><span data-stu-id="a5a91-157">The background color changes.</span></span>  
1.  <span data-ttu-id="a5a91-158">Наведите `Hover Over Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-158">Hover on the `Hover Over Me!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a5a91-159">В панели **Стилей** выберите **:hov**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-159">In the **Styles** panel, choose **:hov**.</span></span>  
1.  <span data-ttu-id="a5a91-160">Проверьте **:hover** checkbox.</span><span class="sxs-lookup"><span data-stu-id="a5a91-160">Check the **:hover** checkbox.</span></span>  <span data-ttu-id="a5a91-161">Цвет фона меняется так же, как и раньше, даже если вы не нависаете над элементом.</span><span class="sxs-lookup"><span data-stu-id="a5a91-161">The background color changes like before, even though you are not actually hovering over the element.</span></span>  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Toggle the hover pseudostate on an element" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       <span data-ttu-id="a5a91-163">Toggle the `:hover` pseudostate on an element</span><span class="sxs-lookup"><span data-stu-id="a5a91-163">Toggle the `:hover` pseudostate on an element</span></span>  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a><span data-ttu-id="a5a91-164">Изменение размеров элемента</span><span class="sxs-lookup"><span data-stu-id="a5a91-164">Change the dimensions of an element</span></span>  

<span data-ttu-id="a5a91-165">Используйте **интерактивную** схему Box Model в панели **Стилей,** чтобы изменить ширину, высоту, обивку, маржу или длину границы элемента.</span><span class="sxs-lookup"><span data-stu-id="a5a91-165">Use the **Box Model** interactive diagram in the **Styles** panel to change the width, height, padding, margin, or border length of an element.</span></span>  

> [!NOTE]
> <span data-ttu-id="a5a91-166">Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.</span><span class="sxs-lookup"><span data-stu-id="a5a91-166">Complete the [View the CSS for an element](#view-the-css-for-an-element) tutorial before doing this one.</span></span>  

1.  <span data-ttu-id="a5a91-167">[Откройте примеры CSS](#open-css-examples).</span><span class="sxs-lookup"><span data-stu-id="a5a91-167">[Open CSS Examples](#open-css-examples).</span></span>  
1.  <span data-ttu-id="a5a91-168">Наведите `Change My Margin!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-168">Hover on the `Change My Margin!` text, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="a5a91-169">На **схеме Box Model** в панели **Стили** наведите курс на **обивку.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-169">In the **Box Model** diagram in the **Styles** panel, hover on **padding**.</span></span>  <span data-ttu-id="a5a91-170">Заполнение элемента выделено в представлении.</span><span class="sxs-lookup"><span data-stu-id="a5a91-170">The padding of an element is highlighted in the viewport.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="a5a91-171">В зависимости от размера окна DevTools может потребоваться прокрутка в нижней части панели **Стилей** для отображения **модели Box.**</span><span class="sxs-lookup"><span data-stu-id="a5a91-171">Depending on the size of your DevTools window, you may need to scroll to the bottom of the **Styles** panel to display the **Box Model**.</span></span>  

1.  <span data-ttu-id="a5a91-172">Дважды щелкните левую маржу в **модели Box,** которая в настоящее время имеет значение, которое означает, что элемент не имеет `-` левого поля.</span><span class="sxs-lookup"><span data-stu-id="a5a91-172">Double-click the left margin in the **Box Model**, which currently has a value of `-` meaning that the element does not have a left-margin.</span></span>  
1.  <span data-ttu-id="a5a91-173">Введите `100px` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-173">Type `100px` and select `Enter`.</span></span>  <span data-ttu-id="a5a91-174">Модель **box по** умолчанию по умолчанию имеет пиксели, но также принимает другие значения, такие как , или `25%` `10vw` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-174">The **Box Model** defaults to pixels, but it also accepts other values, such as `25%`, or `10vw`.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Наведите курсор на обивку элемента" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             <span data-ttu-id="a5a91-176">Наведите курсор на обивку элемента</span><span class="sxs-lookup"><span data-stu-id="a5a91-176">Hover on the padding of the element</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Изменение левого поля элемента" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             <span data-ttu-id="a5a91-178">Изменение левого поля элемента</span><span class="sxs-lookup"><span data-stu-id="a5a91-178">Change the left-margin of the element</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a><span data-ttu-id="a5a91-179">Отладка запросов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="a5a91-179">Debugging Media Queries</span></span>  

<span data-ttu-id="a5a91-180">[Запросы мультимедиа][MDNUsingMediaGueries] — это способ заставить веб-продукт реагировать на изменения параметров конфигурации для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5a91-180">[Media Queries][MDNUsingMediaGueries] are a way to make your web product react to changes in the configuration settings for each user.</span></span>  <span data-ttu-id="a5a91-181">Наиболее важным случаем использования является предоставление вашему продукту другого макета CSS в зависимости от размеров представления.</span><span class="sxs-lookup"><span data-stu-id="a5a91-181">The most significant use case is to provide your product a different CSS layout depending on the dimensions of the viewport.</span></span>  <span data-ttu-id="a5a91-182">Использование отдельных макетов позволяет разметку с одним столбцом для мобильных устройств и макеты с несколькими столбцами при наличии большего имени экрана.</span><span class="sxs-lookup"><span data-stu-id="a5a91-182">Using separate layouts allows for a one-column layout for mobile devices and multi-column layouts when there is more screen estate available.</span></span>  

<span data-ttu-id="a5a91-183">Если вы хотите отлагировать или протестировать запросы мультимедиа, определенные в CSS, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a5a91-183">If you want to debug or test the Media Queries you defined in your CSS, use the following steps.</span></span>  

1.  <span data-ttu-id="a5a91-184">Откройте инструменты разработчика и выберите значок панели инструментов **Toggle** в левом верхней части или `Ctrl` + `Shift` + `M` выберите \( `Cmd` + `Shift` + `M` на macOS\).</span><span class="sxs-lookup"><span data-stu-id="a5a91-184">Open the developer tools and select the **Toggle device toolbar** icon second on the top-left, or select `Ctrl`+`Shift`+`M` \(`Cmd`+`Shift`+`M` on macOS\).</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Откройте панель инструментов устройства" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       <span data-ttu-id="a5a91-186">Откройте панель инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="a5a91-186">Open the device toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5a91-187">Открыв панель инструментов устройства, выберите меню в правом верхнем ряду и `...` выберите **View Media Queries**.</span><span class="sxs-lookup"><span data-stu-id="a5a91-187">With the device toolbar open, select the `...` menu on the top-right and choose **View Media Queries**.</span></span>  <span data-ttu-id="a5a91-188">Цветные полосы, отображаемые над веб-страницей, представляют различные запросы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a5a91-188">The colored bars displayed above the webpage represent the different media queries.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Показать запросы мультимедиа в панели инструментов устройства" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       <span data-ttu-id="a5a91-190">Показать запросы мультимедиа в панели инструментов устройства</span><span class="sxs-lookup"><span data-stu-id="a5a91-190">Show Media Queries in Device Toolbar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5a91-191">Наведите курсор на границы в барах, чтобы отобразить значения различных запросов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a5a91-191">Hover on the boundaries in the bars to display the values of the different media queries.</span></span>  <span data-ttu-id="a5a91-192">Выберите каждый из них для повторного выбора веб-страницы, чтобы соответствовать.</span><span class="sxs-lookup"><span data-stu-id="a5a91-192">Choose each to resize the web page to match.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Выбор запроса мультимедиа из панели предварительного просмотра" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       <span data-ttu-id="a5a91-194">Выбор запроса мультимедиа из панели предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="a5a91-194">Choose Media Query from preview bar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a5a91-195">Чтобы отлажать запросы мультимедиа и открыть CSS-файл в редакторе; наведите курсор на любой из сегментов панели, откройте контекстное меню \(правой кнопкой `Sources` мыши\) и выберите `reveal in source code` .</span><span class="sxs-lookup"><span data-stu-id="a5a91-195">To debug media queries and open the CSS file in the `Sources` editor; hover on any of the bar segments, open the contextual menu \(right-click\), and select `reveal in source code`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Раскрытие запросов мультимедиа в редакторе источников" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       <span data-ttu-id="a5a91-197">Раскрытие запросов мультимедиа в редакторе источников</span><span class="sxs-lookup"><span data-stu-id="a5a91-197">Reveal Media Queries in Sources Editor</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a5a91-198">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5a91-198">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение размещения Microsoft Edge DevTools (Undock, dock to bottom, dock to left)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> <span data-ttu-id="a5a91-202">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5a91-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a5a91-203">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="a5a91-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a5a91-205">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a5a91-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
