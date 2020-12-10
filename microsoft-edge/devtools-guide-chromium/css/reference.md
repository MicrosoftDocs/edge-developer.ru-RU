---
description: Найдите новые рабочие процессы для просмотра и изменения CSS в Microsoft Edge DevTools.
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204014"
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

# <span data-ttu-id="273b1-104">Справочник по CSS</span><span class="sxs-lookup"><span data-stu-id="273b1-104">CSS reference</span></span>  

<span data-ttu-id="273b1-105">Ниже приведен полный справочник по функциям, связанным с просмотром и изменением CSS, в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="273b1-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="273b1-106">Ознакомьтесь с основными принципами [просмотра и изменения каскадных таблиц стилей][DevToolsCSSGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="273b1-106">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="273b1-107">Выбор элемента</span><span class="sxs-lookup"><span data-stu-id="273b1-107">Select an element</span></span>  

<span data-ttu-id="273b1-108">Панель " **элементы** " в DevTools позволяет просматривать или изменять CSS для одного элемента за один раз.</span><span class="sxs-lookup"><span data-stu-id="273b1-108">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="273b1-109">Выбранный элемент выделится в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="273b1-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="273b1-110">Стили элемента отображаются на панели " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="273b1-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="273b1-111">В разделе [Просмотр CSS для элемента][DevToolsCSSGetStartedTutorial] учебника.</span><span class="sxs-lookup"><span data-stu-id="273b1-111">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-112">На приведенном ниже рисунке `h1` элемент, выделенный в **дереве DOM** , является выбранным элементом.</span><span class="sxs-lookup"><span data-stu-id="273b1-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="273b1-113">Справа в области **стили** отображаются стили элемента.</span><span class="sxs-lookup"><span data-stu-id="273b1-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="273b1-114">В левой части экрана выделяется элемент в окне просмотра, но только потому, что в данный момент указатель мыши наведен на него в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="273b1-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Пример выбранного элемента" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="273b1-116">Пример выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="273b1-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="273b1-117">Для выбора элемента используйте одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="273b1-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="273b1-118">В окне просмотра наведите указатель мыши на элемент, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **проверить**.</span><span class="sxs-lookup"><span data-stu-id="273b1-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="273b1-119">В DevTools выберите **пункт выбрать** элемент \ ( ![ выбрать элемент ][ImageSelectAnElementIcon] \) или SELECT `Control` + `Shift` + `C` \ (Windows, Linux \) или `Command` + `Shift` + `C` \ (macOS \), а затем выберите элемент в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="273b1-119">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="273b1-120">В DevTools выберите элемент в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="273b1-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="273b1-121">В DevTools выполните запрос, как `document.querySelector('p')` на **консоли**, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **Показать на панели элементы**.</span><span class="sxs-lookup"><span data-stu-id="273b1-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="273b1-122">Просмотр CSS</span><span class="sxs-lookup"><span data-stu-id="273b1-122">View CSS</span></span>  

### <span data-ttu-id="273b1-123">Просмотр внешней таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="273b1-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="273b1-124">В области **стили** щелкните ссылку рядом с правилом CSS, чтобы открыть внешнюю таблицу стилей, которая определяет правило.</span><span class="sxs-lookup"><span data-stu-id="273b1-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="273b1-125">Если таблица стилей minified, перейдите в раздел, чтобы [сделать файл minified доступным для чтения][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="273b1-125">If the stylesheet is minified, navigate to [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-126">На приведенном ниже рисунке после выбора `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` строки 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , где `.content h1:first-of-type` определено правило CSS.</span><span class="sxs-lookup"><span data-stu-id="273b1-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Просмотр таблицы стилей, в которой определено правило" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="273b1-128">Просмотр таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="273b1-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-129">Просмотр только CSS, которая фактически применяется к элементу</span><span class="sxs-lookup"><span data-stu-id="273b1-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="273b1-130">На вкладке **стили** отображаются все правила, применимые к элементу, включая объявления, которые были переопределены.</span><span class="sxs-lookup"><span data-stu-id="273b1-130">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="273b1-131">Если вы не заинтересованы в переопределенных объявлениях, используйте **вычисляемые** вкладки для просмотра только CSS, которая фактически применяется к элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-131">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="273b1-132">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-132">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-133">Перейдите на вкладку " **вычисляемые** " на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="273b1-133">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-134">В окне с широкой DevTools **Вычисляемая** вкладка не существует.</span><span class="sxs-lookup"><span data-stu-id="273b1-134">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="273b1-135">Содержимое **вычисляемой** вкладки отображается на вкладке **стили** .</span><span class="sxs-lookup"><span data-stu-id="273b1-135">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="273b1-136">Унаследованные свойства являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="273b1-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="273b1-137">Установите флажок **Показать все** , чтобы увидеть все унаследованные значения.</span><span class="sxs-lookup"><span data-stu-id="273b1-137">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-138">На приведенном ниже рисунке показана **Вычисляемая** вкладка, на которой ПОКАЗАНЫ свойства CSS, применяемые к текущему `h1` элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-138">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Вычисляемая вкладка" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="273b1-140">**Вычисляемая** вкладка</span><span class="sxs-lookup"><span data-stu-id="273b1-140">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-141">Просмотр свойств CSS в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="273b1-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="273b1-142">Используйте **вычисляемую** вкладку.  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-142">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="273b1-143">Просмотр унаследованных свойств CSS</span><span class="sxs-lookup"><span data-stu-id="273b1-143">View inherited CSS properties</span></span>  

<span data-ttu-id="273b1-144">Установите флажок **Показать все** на вкладке **вычисляемый** .  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-144">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="273b1-145">Просмотр модели Box для элемента</span><span class="sxs-lookup"><span data-stu-id="273b1-145">View the box model for an element</span></span>  

<span data-ttu-id="273b1-146">Чтобы просмотреть [модель Box][MDNBoxModel] элемента, перейдите на вкладку **стили** .  Если окно DevTools узким, схема **модель Box** находится в нижней части вкладки.</span><span class="sxs-lookup"><span data-stu-id="273b1-146">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="273b1-147">Выберите и измените значение, чтобы изменить значение.</span><span class="sxs-lookup"><span data-stu-id="273b1-147">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-148">На рисунке ниже показана модель Box на вкладке " **стили** " в **поле** "модель" для элемента, выбранного в данный момент `h1` .</span><span class="sxs-lookup"><span data-stu-id="273b1-148">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Схема модели Box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="273b1-150">Схема **модели Box**</span><span class="sxs-lookup"><span data-stu-id="273b1-150">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-151">Поиск и фильтрация CSS элемента</span><span class="sxs-lookup"><span data-stu-id="273b1-151">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="273b1-152">С помощью текстового поля **Фильтр** на вкладках **стили** и **вычисляемые** вкладки можно искать определенные свойства или значения CSS.</span><span class="sxs-lookup"><span data-stu-id="273b1-152">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="273b1-153">Чтобы также искать унаследованные свойства на вкладке **вычисляемые** , установите флажок **Показать все** .</span><span class="sxs-lookup"><span data-stu-id="273b1-153">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-154">На приведенном ниже рисунке для вкладки **стили** отображаются только правила, включающие поисковый запрос `color` .</span><span class="sxs-lookup"><span data-stu-id="273b1-154">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Фильтрация вкладки "стили"" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="273b1-156">Фильтрация вкладки " **стили** "</span><span class="sxs-lookup"><span data-stu-id="273b1-156">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="273b1-157">На приведенном ниже рисунке отфильтрованная **вкладка** фильтруется так, чтобы отображались только объявления, включающие поисковый запрос `100%` .</span><span class="sxs-lookup"><span data-stu-id="273b1-157">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Фильтрация вычисляемой вкладки" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="273b1-159">Фильтрация **вычисляемой** вкладки</span><span class="sxs-lookup"><span data-stu-id="273b1-159">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-160">Переключение на псевдо-класс</span><span class="sxs-lookup"><span data-stu-id="273b1-160">Toggle a pseudo-class</span></span>  

<span data-ttu-id="273b1-161">Выполните указанные ниже действия, чтобы переключить псевдо-класс, например,, `:active` `:focus` `:hover` или `:visited` .</span><span class="sxs-lookup"><span data-stu-id="273b1-161">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="273b1-162">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-162">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-163">На панели " **элементы** " перейдите на вкладку " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="273b1-163">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="273b1-164">Выберите **: Hov**.</span><span class="sxs-lookup"><span data-stu-id="273b1-164">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="273b1-165">Проверьте псевдо-класс, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="273b1-165">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-166">На рисунке ниже показано, как переключается `:hover` псевдо-класс.</span><span class="sxs-lookup"><span data-stu-id="273b1-166">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="273b1-167">В окне просмотра убедитесь в том, что `background-color: cornflowerblue` объявление применяется к элементу, несмотря на то что элемент фактически не наведен на указатель.</span><span class="sxs-lookup"><span data-stu-id="273b1-167">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Переключение: псевдо-класс для наведения" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="273b1-169">Переключение `:hover` псевдо-класса</span><span class="sxs-lookup"><span data-stu-id="273b1-169">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="273b1-170">Для интерактивного учебника перейдите к разделу [Добавление PseudoState в класс][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="273b1-170">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="273b1-171">Просмотр страницы в режиме печати</span><span class="sxs-lookup"><span data-stu-id="273b1-171">View a page in print mode</span></span>  

<span data-ttu-id="273b1-172">Выполните указанные ниже действия, чтобы просмотреть страницу в режиме печати.</span><span class="sxs-lookup"><span data-stu-id="273b1-172">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="273b1-173">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="273b1-173">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="273b1-174">Начните вводить текст `Rendering` и выберите его `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="273b1-174">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="273b1-175">Для **имитации** раскрывающегося списка выбери мультимедиа в CSS нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="273b1-175">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <span data-ttu-id="273b1-176">Просмотр использованной и неиспользуемой CSS с помощью вкладки "покрытие"</span><span class="sxs-lookup"><span data-stu-id="273b1-176">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="273b1-177">На вкладке Coverage показано, какая страница CSS используется в действительности.</span><span class="sxs-lookup"><span data-stu-id="273b1-177">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="273b1-178">Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), когда DevTools находится в фокусе, чтобы [Открыть меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="273b1-178">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="273b1-179">Начните вводить текст `coverage` и выберите **Показать покрытие**.</span><span class="sxs-lookup"><span data-stu-id="273b1-179">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="273b1-180">Откроется вкладка покрытие.</span><span class="sxs-lookup"><span data-stu-id="273b1-180">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Открытие вкладки "покрытие" в меню команд" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="273b1-182">Открытие вкладки " **покрытие** " в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="273b1-182">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Вкладка "покрытие"" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="273b1-184">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="273b1-184">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="273b1-185">Нажмите кнопку **начать покрытие инструментирования и обновите страницу** \ ( ![ Запуск инструментированного покрытия и обновление страницы ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="273b1-185">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="273b1-186">Обновленная страница и вкладка Coverage предоставляют общие сведения о том, сколько стилей CSS и JavaScript используется для каждого файла, загружаемого браузером.</span><span class="sxs-lookup"><span data-stu-id="273b1-186">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="273b1-187">Зеленый представляет используемые CSS.</span><span class="sxs-lookup"><span data-stu-id="273b1-187">Green represents used CSS.</span></span>  <span data-ttu-id="273b1-188">Красный — неиспользуемый CSS.</span><span class="sxs-lookup"><span data-stu-id="273b1-188">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="273b1-190">Общие сведения о том, сколько каскадных таблиц (и JavaScript \) использует и не используется</span><span class="sxs-lookup"><span data-stu-id="273b1-190">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="273b1-191">Выберите CSS-файл, чтобы просмотреть разбиение по строкам для используемого CSS.</span><span class="sxs-lookup"><span data-stu-id="273b1-191">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="273b1-192">На приведенном ниже рисунке строки 145 в 147 и 149 в 151 из `b66bc881.site-ltr.css` не используются, в то время как используются строки 163 — 166.</span><span class="sxs-lookup"><span data-stu-id="273b1-192">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Разбиение по строкам для используемых и неиспользуемых CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="273b1-194">Разбиение по строкам для используемых и неиспользуемых CSS</span><span class="sxs-lookup"><span data-stu-id="273b1-194">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="273b1-195">Принудительная печать в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="273b1-195">Force print preview mode</span></span>  

<span data-ttu-id="273b1-196">Просмотрите [DevTools в режиме предварительного просмотра][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="273b1-196">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="273b1-197">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="273b1-197">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="273b1-198">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="273b1-198">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="273b1-199">Порядок объявлений влияет на стиль элемента с помощью приведенного ниже списка, который поможет вам добавлять объявления различными способами.</span><span class="sxs-lookup"><span data-stu-id="273b1-199">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="273b1-200">[Добавление встроенного объявления](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="273b1-200">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="273b1-201">Эквивалентно добавлению `style` атрибута в HTML элемента.</span><span class="sxs-lookup"><span data-stu-id="273b1-201">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="273b1-202">[Добавление объявления в правило стиля](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="273b1-202">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="273b1-203">Какой рабочий процесс следует использовать?</span><span class="sxs-lookup"><span data-stu-id="273b1-203">What workflow should you use?</span></span>** <span data-ttu-id="273b1-204">В большинстве сценариев вы, возможно, захотите использовать рабочий процесс объявления на встроенных элементах.</span><span class="sxs-lookup"><span data-stu-id="273b1-204">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="273b1-205">Встроенные объявления имеют более высокие особенности, чем внешние, поэтому встроенный рабочий процесс гарантирует, что изменения вступают в силу в ожидаемом элементе.</span><span class="sxs-lookup"><span data-stu-id="273b1-205">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="273b1-206">Для получения дополнительных сведений об определенном способе перейдите к разделу [типы Selector][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="273b1-206">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="273b1-207">Если при отладке любого стиля элемента требуется специально проверить, что происходит, если объявление определено в разных местах, используйте другой рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="273b1-207">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="273b1-208">Добавление встроенного объявления</span><span class="sxs-lookup"><span data-stu-id="273b1-208">Add an inline declaration</span></span>  

<span data-ttu-id="273b1-209">Чтобы добавить встроенное объявление, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-209">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="273b1-210">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-210">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-211">В области **стили** выберите между скобками раздела **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="273b1-211">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="273b1-212">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="273b1-212">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="273b1-213">Введите имя свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="273b1-213">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="273b1-214">Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="273b1-214">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="273b1-215">Убедитесь, что в **дереве DOM** `style` к элементу добавлен атрибут.</span><span class="sxs-lookup"><span data-stu-id="273b1-215">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-216">На приведенном ниже рисунке к `margin-top` `background-color` выбранному элементу применены свойства и.</span><span class="sxs-lookup"><span data-stu-id="273b1-216">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="273b1-217">В **дереве DOM** убедитесь, что объявления отражены в `style` атрибуте для элемента.</span><span class="sxs-lookup"><span data-stu-id="273b1-217">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Добавление встроенных объявлений" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="273b1-219">Добавление встроенных объявлений</span><span class="sxs-lookup"><span data-stu-id="273b1-219">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="273b1-220">Добавление объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="273b1-220">Add a declaration to a style rule</span></span>  

<span data-ttu-id="273b1-221">Чтобы добавить объявление к существующему правилу стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-221">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="273b1-222">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-222">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-223">В области **стили** выберите один из квадратных скобок правила стиля, к которому вы хотите добавить объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-223">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="273b1-224">Курсор фокусируется на том, что позволяет вводить текст.</span><span class="sxs-lookup"><span data-stu-id="273b1-224">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="273b1-225">Введите имя свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="273b1-225">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="273b1-226">Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="273b1-226">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Добавление объявления в правило стиля" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="273b1-228">Добавление `border-bottom-style:groove` объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="273b1-228">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-229">Изменение имени или значения объявления</span><span class="sxs-lookup"><span data-stu-id="273b1-229">Change a declaration name or value</span></span>  

<span data-ttu-id="273b1-230">Выберите и измените имя или значение объявления, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="273b1-230">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="273b1-231">Сочетания клавиш для быстрого увеличения или уменьшения значения (, или единиц) можно найти [в статье изменение значений объявлений](#change-declaration-values-with-keyboard-shortcuts) `0.1` `1` `10` `100` .</span><span class="sxs-lookup"><span data-stu-id="273b1-231">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Изменение значения объявления" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="273b1-233">Изменение значения `border-bottom-style` объявления</span><span class="sxs-lookup"><span data-stu-id="273b1-233">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-234">Изменение значений объявлений с помощью сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="273b1-234">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="273b1-235">При редактировании значения объявления вы можете использовать следующие сочетания клавиш, чтобы увеличить значение на определенную величину.</span><span class="sxs-lookup"><span data-stu-id="273b1-235">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="273b1-236">Выберите `Alt` + `Up` \ (Windows, Linux \) или `Option` + `Up` \ (macOS \), чтобы увеличить его `0.1` .</span><span class="sxs-lookup"><span data-stu-id="273b1-236">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="273b1-237">Выберите `Up` , чтобы изменить значение `1` , или, `0.1` Если текущее значение находится в диапазоне от `-1` и до `1` .</span><span class="sxs-lookup"><span data-stu-id="273b1-237">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="273b1-238">Выберите, `Shift` + `Up` чтобы увеличить `10` .</span><span class="sxs-lookup"><span data-stu-id="273b1-238">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="273b1-239">Выберите `Shift` + `Page Up` \ (Windows, Linux \) или `Shift` + `Command` + `Up` \ (macOS \), чтобы увеличить значение `100` .</span><span class="sxs-lookup"><span data-stu-id="273b1-239">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="273b1-240">Кроме того, выполняется уменьшение.</span><span class="sxs-lookup"><span data-stu-id="273b1-240">Decrementing also works.</span></span>  <span data-ttu-id="273b1-241">Просто замените каждый из `Up` упомянутых выше экземпляров `Down` .</span><span class="sxs-lookup"><span data-stu-id="273b1-241">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="273b1-242">Добавление класса в элемент</span><span class="sxs-lookup"><span data-stu-id="273b1-242">Add a class to an element</span></span>  

<span data-ttu-id="273b1-243">Чтобы добавить класс в элемент, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-243">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="273b1-244">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="273b1-244">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="273b1-245">Выберите **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="273b1-245">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="273b1-246">Введите имя класса в текстовом поле **Добавить новый класс** .</span><span class="sxs-lookup"><span data-stu-id="273b1-246">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="273b1-247">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="273b1-247">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Область «классы элементов»" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="273b1-249">Область « **классы элементов** »</span><span class="sxs-lookup"><span data-stu-id="273b1-249">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-250">Переключение класса</span><span class="sxs-lookup"><span data-stu-id="273b1-250">Toggle a class</span></span>  

<span data-ttu-id="273b1-251">Выполните указанные ниже действия, чтобы включить или отключить класс для элемента.</span><span class="sxs-lookup"><span data-stu-id="273b1-251">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="273b1-252">[Выберите элемент](#select-an-element) в **дереве DOM**.</span><span class="sxs-lookup"><span data-stu-id="273b1-252">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="273b1-253">Откройте область **классы элементов** .</span><span class="sxs-lookup"><span data-stu-id="273b1-253">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="273b1-254">Дополнительные сведения о том, [как добавить класс в элемент](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-254">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="273b1-255">Под текстовым полем **Добавить новый класс** находятся все классы, которые применяются к определенному элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-255">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="273b1-256">Установите флажок рядом с классом, который вы хотите включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="273b1-256">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="273b1-257">Добавление правила стиля</span><span class="sxs-lookup"><span data-stu-id="273b1-257">Add a style rule</span></span>  

<span data-ttu-id="273b1-258">Чтобы добавить новое правило стиля, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-258">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="273b1-259">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-259">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-260">Нажмите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="273b1-260">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="273b1-261">DevTools вставляет новое правило под правилом **element. Style** .</span><span class="sxs-lookup"><span data-stu-id="273b1-261">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-262">На приведенном ниже рисунке DevTools добавляет `h1.devsite-page-title` правило стиля после выбора **нового правила стиля**.</span><span class="sxs-lookup"><span data-stu-id="273b1-262">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Добавление нового правила стиля" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="273b1-264">Добавление нового правила стиля</span><span class="sxs-lookup"><span data-stu-id="273b1-264">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="273b1-265">Выберите таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="273b1-265">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="273b1-266">При [добавлении нового правила стиля](#add-a-style-rule)нажмите и удерживайте **новое правило** стиля \ ( ![ новое правило стиля), ][ImageNewStyleRuleIcon] чтобы выбрать таблицу стилей, к которой нужно добавить правило.</span><span class="sxs-lookup"><span data-stu-id="273b1-266">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Выбор таблицы стилей" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="273b1-268">Выбор таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="273b1-268">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="273b1-269">Добавление правила стиля в определенное место</span><span class="sxs-lookup"><span data-stu-id="273b1-269">Add a style rule to a specific location</span></span>  

<span data-ttu-id="273b1-270">Выполните указанные ниже действия, чтобы добавить правило стиля в конкретное расположение на вкладке " **стили** ".</span><span class="sxs-lookup"><span data-stu-id="273b1-270">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="273b1-271">Наведите указатель мыши на правило стиля, которое находится в том месте, куда вы хотите добавить новое правило стиля.</span><span class="sxs-lookup"><span data-stu-id="273b1-271">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="273b1-272">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="273b1-272">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="273b1-273">Нажмите кнопку **Вставить правило стиля ниже** \ ( ![ Вставьте правило стиля ниже значка ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="273b1-273">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Вставить правило стиля ниже" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="273b1-275">Вставить правило стиля ниже</span><span class="sxs-lookup"><span data-stu-id="273b1-275">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="273b1-276">Панель инструментов "другие действия"</span><span class="sxs-lookup"><span data-stu-id="273b1-276">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="273b1-277">На панели инструментов " **другие действия** " можно выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-277">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="273b1-278">Вставка правила стиля прямо ниже того, на котором вы отправили фокус.</span><span class="sxs-lookup"><span data-stu-id="273b1-278">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="273b1-279">Добавьте в `background-color` `color` `box-shadow` правило стиля, которое `text-shadow` вы хотите включить, или объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-279">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="273b1-280">Выполните указанные ниже действия, чтобы открыть панель инструментов **Дополнительные действия** .</span><span class="sxs-lookup"><span data-stu-id="273b1-280">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="273b1-281">На вкладке **стили** наведите указатель мыши на правило стиля.</span><span class="sxs-lookup"><span data-stu-id="273b1-281">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="273b1-282">**Дополнительные действия** \ ( `...` \) находятся в правом нижнем углу раздела "правило стиля".</span><span class="sxs-lookup"><span data-stu-id="273b1-282">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="273b1-283">На приведенном ниже рисунке наведите указатель мыши на `.header-holder.has-default-focus` правило стиля и **другие действия** будут отображены в правом нижнем углу раздела "правило стиля".</span><span class="sxs-lookup"><span data-stu-id="273b1-283">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Показать дополнительные действия" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="273b1-285">Показать **Дополнительные действия** \ ( `...` \)</span><span class="sxs-lookup"><span data-stu-id="273b1-285">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="273b1-286">Наведите указатель мыши на элемент **Дополнительные действия** , `...` чтобы отобразить указанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-286">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="273b1-287">**Правило стиля вставки, показанное ниже** , выводится при наведении указателя мыши на **другие действия**.</span><span class="sxs-lookup"><span data-stu-id="273b1-287">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Панель инструментов «другие действия»" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="273b1-289">Панель инструментов « **другие действия** »</span><span class="sxs-lookup"><span data-stu-id="273b1-289">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="273b1-290">Переключить объявление</span><span class="sxs-lookup"><span data-stu-id="273b1-290">Toggle a declaration</span></span>  

<span data-ttu-id="273b1-291">Выполните действия folllwoing, чтобы переключить одно объявление на \ (или выключить).</span><span class="sxs-lookup"><span data-stu-id="273b1-291">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="273b1-292">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-292">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-293">В области **стили** наведите указатель мыши на правило, которое определяет объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-293">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="273b1-294">Рядом с каждым объявлением появится флажок.</span><span class="sxs-lookup"><span data-stu-id="273b1-294">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="273b1-295">Установите флажок \ (или снимите) флажок рядом с объявлением.</span><span class="sxs-lookup"><span data-stu-id="273b1-295">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="273b1-296">Если вы снимите флажок объявления, DevTools пересекает его, чтобы показать, что он больше не активен.</span><span class="sxs-lookup"><span data-stu-id="273b1-296">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="273b1-297">На приведенном ниже рисунке `margin-top` свойство для выбранного в данный момент элемента было отключено.</span><span class="sxs-lookup"><span data-stu-id="273b1-297">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Переключить объявление" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="273b1-299">Переключить объявление</span><span class="sxs-lookup"><span data-stu-id="273b1-299">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="273b1-300">Добавление объявления цвета фона</span><span class="sxs-lookup"><span data-stu-id="273b1-300">Add a background-color declaration</span></span>  

<span data-ttu-id="273b1-301">Выполните указанные ниже действия, чтобы добавить `background-color` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-301">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="273b1-302">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `background-color` объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-302">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="273b1-303">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="273b1-303">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="273b1-304">Нажмите кнопку **добавить цвет фона** \ ( ![ Добавить значок цвет фона ][ImageAddBackgroundColorIcon] ).</span><span class="sxs-lookup"><span data-stu-id="273b1-304">Choose **Add Background Color** \(![Add Background Color icon][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Добавление цвета фона" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="273b1-306">Добавление цвета фона</span><span class="sxs-lookup"><span data-stu-id="273b1-306">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="273b1-307">Добавление объявления цвета</span><span class="sxs-lookup"><span data-stu-id="273b1-307">Add a color declaration</span></span>  

<span data-ttu-id="273b1-308">Выполните указанные ниже действия, чтобы добавить `color` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-308">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="273b1-309">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `color` объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-309">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="273b1-310">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="273b1-310">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="273b1-311">Нажмите кнопку **добавить цвет** \ ( ![ добавить цвет значок ][ImageAddColorIcon] ).</span><span class="sxs-lookup"><span data-stu-id="273b1-311">Choose **Add Color** \(![Add Color icon][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Добавить цвет" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="273b1-313">Добавить цвет</span><span class="sxs-lookup"><span data-stu-id="273b1-313">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="273b1-314">Добавление объявления с помощью блочной тени</span><span class="sxs-lookup"><span data-stu-id="273b1-314">Add a box-shadow declaration</span></span>  

<span data-ttu-id="273b1-315">Выполните указанные ниже действия, чтобы добавить `box-shadow` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-315">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="273b1-316">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `box-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-316">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="273b1-317">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="273b1-317">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="273b1-318">Нажмите кнопку **"добавить тень"** , а затем — ![ значок "добавить тень" ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="273b1-318">Choose **Add Box Shadow** \(![Add Box Shadow icon][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Добавление тени для поля" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="273b1-320">Добавление тени для поля</span><span class="sxs-lookup"><span data-stu-id="273b1-320">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="273b1-321">Добавление объявления тени для текста</span><span class="sxs-lookup"><span data-stu-id="273b1-321">Add a text-shadow declaration</span></span>  

<span data-ttu-id="273b1-322">Выполните указанные ниже действия, чтобы добавить `text-shadow` объявление к элементу.</span><span class="sxs-lookup"><span data-stu-id="273b1-322">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="273b1-323">Наведите указатель мыши на правило стиля, в которое вы хотите добавить `text-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="273b1-323">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="273b1-324">[Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="273b1-324">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="273b1-325">Нажмите кнопку **Добавить тень текста** \ ( ![ Добавить значок тени текста ][ImageAddTextShadowIcon] ).</span><span class="sxs-lookup"><span data-stu-id="273b1-325">Choose **Add Text Shadow** \(![Add Text Shadow icon][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Добавление тени текста" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="273b1-327">Добавление тени текста</span><span class="sxs-lookup"><span data-stu-id="273b1-327">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="273b1-328">Изменение цвета с помощью палитры цветов</span><span class="sxs-lookup"><span data-stu-id="273b1-328">Change colors with the Color Picker</span></span>  

<span data-ttu-id="273b1-329">В **средстве выбора цвета** есть графический интерфейс для изменения `color` и `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="273b1-329">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="273b1-330">Выполните указанные ниже действия, чтобы открыть окно **выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="273b1-330">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="273b1-331">[Выберите элемент](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="273b1-331">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="273b1-332">На вкладке **стили** найдите и щелкните то `color` `background-color` же объявление, которое вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="273b1-332">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="273b1-333">Слева от "," `color` `background-color` или аналогичного значения есть маленький квадрат, который является предварительным просмотром цвета.</span><span class="sxs-lookup"><span data-stu-id="273b1-333">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="273b1-334">На приведенном ниже рисунке небольшой квадрат слева от него `rgba(0, 0, 0, 0.7)` является предварительным просмотром этого цвета.</span><span class="sxs-lookup"><span data-stu-id="273b1-334">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Цвет предварительного просмотра" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="273b1-336">Цвет предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="273b1-336">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="273b1-337">Нажмите кнопку Предварительный просмотр, чтобы открыть окно **выбора цвета**.</span><span class="sxs-lookup"><span data-stu-id="273b1-337">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Выбор цвета" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="273b1-339">**Выбор цвета**</span><span class="sxs-lookup"><span data-stu-id="273b1-339">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="273b1-340">На приведенном ниже рисунке и списке описывает каждого элемента пользовательского интерфейса в **палитре цветов**.</span><span class="sxs-lookup"><span data-stu-id="273b1-340">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Палитра цветов с заметками" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="273b1-342">**Палитра цветов**с заметками</span><span class="sxs-lookup"><span data-stu-id="273b1-342">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-343">1,1</span><span class="sxs-lookup"><span data-stu-id="273b1-343">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-344">Оттенки</span><span class="sxs-lookup"><span data-stu-id="273b1-344">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-345">2</span><span class="sxs-lookup"><span data-stu-id="273b1-345">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-346">Выбрав</span><span class="sxs-lookup"><span data-stu-id="273b1-346">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-347">Дополнительные сведения можно найти с помощью [пипетки, выключив образец цвета на странице](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="273b1-347">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-348">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="273b1-348">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-349">Копировать в буфер</span><span class="sxs-lookup"><span data-stu-id="273b1-349">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-350">Скопируйте **Отображаемое значение** в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="273b1-350">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-351">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="273b1-351">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-352">Отображаемое значение</span><span class="sxs-lookup"><span data-stu-id="273b1-352">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-353">Представление RGBA, HSLA или шестнадцатеричного представления цвета.</span><span class="sxs-lookup"><span data-stu-id="273b1-353">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-354">5</span><span class="sxs-lookup"><span data-stu-id="273b1-354">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-355">Цветовая палитра</span><span class="sxs-lookup"><span data-stu-id="273b1-355">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-356">Выберите один из квадратов, чтобы изменить цвет на этот квадрат.</span><span class="sxs-lookup"><span data-stu-id="273b1-356">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-357">152</span><span class="sxs-lookup"><span data-stu-id="273b1-357">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-358">Отношения</span><span class="sxs-lookup"><span data-stu-id="273b1-358">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-359">5-7</span><span class="sxs-lookup"><span data-stu-id="273b1-359">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-360">Opacity (Прозрачность)</span><span class="sxs-lookup"><span data-stu-id="273b1-360">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-361">No8</span><span class="sxs-lookup"><span data-stu-id="273b1-361">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-362">Переключатель отображения значений</span><span class="sxs-lookup"><span data-stu-id="273b1-362">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-363">Переключение между представлениями "RGBA", "HSLA" и "шестнадцатеричный" текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="273b1-363">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="273b1-364">@</span><span class="sxs-lookup"><span data-stu-id="273b1-364">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="273b1-365">Переключатель цветовой палитры</span><span class="sxs-lookup"><span data-stu-id="273b1-365">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="273b1-366">Переключение между [палитрой «дизайн материала][MaterialDesignColorSystem]», настраиваемой палитрой или палитрой цветов страницы.</span><span class="sxs-lookup"><span data-stu-id="273b1-366">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="273b1-367">DevTools создает цветовую палитру страницы на основе цветов, найденных в стилях.</span><span class="sxs-lookup"><span data-stu-id="273b1-367">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="273b1-368">Выбор цвета на странице с помощью пипетки</span><span class="sxs-lookup"><span data-stu-id="273b1-368">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="273b1-369">Когда вы откроете окно **выбора цвета**, по умолчанию будет включена **Пипетка** \ ( ![ Пипетка ][ImageEyedropperIcon] \).</span><span class="sxs-lookup"><span data-stu-id="273b1-369">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="273b1-370">Чтобы изменить выбранный цвет на другой цвет на странице, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="273b1-370">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="273b1-371">Наведите указатель мыши на целевой цвет в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="273b1-371">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="273b1-372">Нажмите кнопку подтвердить.</span><span class="sxs-lookup"><span data-stu-id="273b1-372">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="273b1-373">На приведенном ниже рисунке в **средстве выбора цвета** отображается текущее цветное значение `rgba(0,0,0,0.7)` , которое близко к черному.</span><span class="sxs-lookup"><span data-stu-id="273b1-373">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="273b1-374">Определенный цвет должен измениться на черную версию, которая выделена в окне просмотра, после того как вы выберете его.</span><span class="sxs-lookup"><span data-stu-id="273b1-374">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Использование пипетки" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="273b1-376">Использование пипетки</span><span class="sxs-lookup"><span data-stu-id="273b1-376">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <span data-ttu-id="273b1-377">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="273b1-377">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Добавление PseudoState в класс — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Просмотр CSS для элемента — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS) | Документы Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Создание доступного для чтения файла minified — Справка по отладке JavaScript | Документы Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Макет "Цветовая система-материал""  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель Box | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы выбора — "конкретное |" MDN"  

> [!NOTE]
> <span data-ttu-id="273b1-387">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="273b1-387">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="273b1-388">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="273b1-388">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="273b1-390">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="273b1-390">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  