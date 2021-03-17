---
description: Откройте для себя новые процессы просмотра и изменения CSS в Microsoft Edge DevTools.
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 84aacbb3961f6b8f6e9a0bda8823fecbbb26ec25
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439305"
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

# <a name="css-reference"></a><span data-ttu-id="1cb40-104">Справочник по CSS</span><span class="sxs-lookup"><span data-stu-id="1cb40-104">CSS reference</span></span>  

<span data-ttu-id="1cb40-105">Откройте для себя новые процессы в следующей комплексной ссылке на функции Microsoft Edge DevTools, связанные с просмотром и изменением CSS.</span><span class="sxs-lookup"><span data-stu-id="1cb40-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="1cb40-106">Чтобы узнать основы, перейдите к [началу работы с просмотром и изменением CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="1cb40-106">To learn the basics, navigate to [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="choose-an-element"></a><span data-ttu-id="1cb40-107">Выбор элемента</span><span class="sxs-lookup"><span data-stu-id="1cb40-107">Choose an element</span></span>  

<span data-ttu-id="1cb40-108">Средство **Elements** devTools позволяет просматривать или изменять CSS одного элемента одновременно.</span><span class="sxs-lookup"><span data-stu-id="1cb40-108">The **Elements** tool of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="1cb40-109">Выбранный элемент выделен в **дереве DOM.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="1cb40-110">Стили элемента показаны в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="1cb40-111">Для руководства перейдите к [просмотру CSS для элемента][DevToolsCSSGetStartedTutorial].</span><span class="sxs-lookup"><span data-stu-id="1cb40-111">For a tutorial, navigate to [View the CSS for an element][DevToolsCSSGetStartedTutorial].</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-112">На следующем рисунке выбран элемент, который выделен в `h1` **дереве DOM.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="1cb40-113">Справа стили элемента показаны в области **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="1cb40-114">Слева элемент выделяется в представлении, но только потому, что мышь в настоящее время нависает над ней в **dom Tree**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Пример выбранного элемента" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="1cb40-116">Пример выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="1cb40-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="1cb40-117">Для выбора элемента используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="1cb40-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="1cb40-118">В представлении наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="1cb40-119">В DevTools выберите элемент **\(** Выберите элемент \) или выберите ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) или `Command` + `Shift` + `C` \(macOS\), а затем выберите элемент в представлении.</span><span class="sxs-lookup"><span data-stu-id="1cb40-119">In DevTools, choose **Select an element** \(![Select an element](../media/select-an-element-icon.msft.png)\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="1cb40-120">В DevTools выберите элемент **dom Tree**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="1cb40-121">В DevTools запустите запрос, как в консоли, наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите панель `document.querySelector('p')` **Reveal in Elements** \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="1cb40-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <a name="view-css"></a><span data-ttu-id="1cb40-122">Просмотр CSS</span><span class="sxs-lookup"><span data-stu-id="1cb40-122">View CSS</span></span>  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a><span data-ttu-id="1cb40-123">Просмотр таблицы внешних стилей, где определено правило</span><span class="sxs-lookup"><span data-stu-id="1cb40-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="1cb40-124">В области **Стилей** выберите ссылку рядом с правилом CSS, чтобы открыть таблицу внешних стилей, определяемую правилом.</span><span class="sxs-lookup"><span data-stu-id="1cb40-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="1cb40-125">Если таблица стилей минирована, перейдите, [чтобы сделать минированную папку читаемой.][DevToolsJavascriptReferenceFormat]</span><span class="sxs-lookup"><span data-stu-id="1cb40-125">If the stylesheet is minified, navigate to [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-126">На следующем рисунке после выбора вы перенастроили строку 2 из, где определено правило `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` `.content h1:first-of-type` CSS.</span><span class="sxs-lookup"><span data-stu-id="1cb40-126">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Просмотр таблицы стилей, в которой определено правило" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="1cb40-128">Просмотр таблицы стилей, в которой определено правило</span><span class="sxs-lookup"><span data-stu-id="1cb40-128">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a><span data-ttu-id="1cb40-129">Просмотр только CSS, который фактически применяется к элементу</span><span class="sxs-lookup"><span data-stu-id="1cb40-129">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="1cb40-130">На **панели Стилей** показаны все правила, применимые к элементу, включая переопределяемые объявления.</span><span class="sxs-lookup"><span data-stu-id="1cb40-130">The **Styles** panel shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="1cb40-131">Если вы не заинтересованы в переопределяемом объявлении, используйте **панель Computed** для просмотра только CSS, который на самом деле применяется к элементу.</span><span class="sxs-lookup"><span data-stu-id="1cb40-131">When you are not interested in overridden declarations, use the **Computed** panel to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="1cb40-132">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-132">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-133">Перейдите к **панели Computed** в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-133">Navigate to the **Computed** panel in the **Elements** tool.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-134">В широком окне DevTools панель **Computed** не существует.</span><span class="sxs-lookup"><span data-stu-id="1cb40-134">On a wide DevTools window, the **Computed** panel does not exist.</span></span>  <span data-ttu-id="1cb40-135">Содержимое панели **Computed отображается** на панели **Styles.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-135">The contents of the **Computed** panel are shown on the **Styles** panel.</span></span>  

<span data-ttu-id="1cb40-136">Унаследованные свойства непрозрачны.</span><span class="sxs-lookup"><span data-stu-id="1cb40-136">Inherited properties are opaque.</span></span>  <span data-ttu-id="1cb40-137">Чтобы отобразить все унаследованные значения, выберите контрольный ящик **Show All.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-137">To display all inherited values, select the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-138">На следующем рисунке на панели **Computed** показаны свойства CSS, применяемые к выбранному в настоящее время `h1` элементу.</span><span class="sxs-lookup"><span data-stu-id="1cb40-138">In the following figure, the **Computed** panel shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Панель Computed" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="1cb40-140">Панель **Computed**</span><span class="sxs-lookup"><span data-stu-id="1cb40-140">The **Computed** panel</span></span>  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a><span data-ttu-id="1cb40-141">Просмотр свойств CSS в алфавитном порядке</span><span class="sxs-lookup"><span data-stu-id="1cb40-141">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="1cb40-142">Используйте **панель Computed.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-142">Use the **Computed** panel.</span></span>  <span data-ttu-id="1cb40-143">Перейдите [к просмотру только CSS, который фактически применяется к элементу.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="1cb40-143">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-inherited-css-properties"></a><span data-ttu-id="1cb40-144">Просмотр унаследованных свойств CSS</span><span class="sxs-lookup"><span data-stu-id="1cb40-144">View inherited CSS properties</span></span>  

<span data-ttu-id="1cb40-145">Проверьте **контрольный ящик Show All** в **панели Computed.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-145">Check the **Show All** checkbox in the **Computed** panel.</span></span>  <span data-ttu-id="1cb40-146">Перейдите [к просмотру только CSS, который фактически применяется к элементу.](#view-only-the-css-that-is-actually-applied-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="1cb40-146">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-the-box-model-for-an-element"></a><span data-ttu-id="1cb40-147">Просмотр модели окна для элемента</span><span class="sxs-lookup"><span data-stu-id="1cb40-147">View the box model for an element</span></span>  

<span data-ttu-id="1cb40-148">Чтобы [просмотреть модель элемента полей,][MDNBoxModel] перейдите на панель **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-148">To view [the box model][MDNBoxModel] of an element, navigate to the **Styles** panel.</span></span>  <span data-ttu-id="1cb40-149">Если окно DevTools узкое, диаграмма **Box Model** находится в нижней части панели.</span><span class="sxs-lookup"><span data-stu-id="1cb40-149">If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the panel.</span></span>  

<span data-ttu-id="1cb40-150">Выберите и измените значение для изменения значения.</span><span class="sxs-lookup"><span data-stu-id="1cb40-150">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-151">На следующем рисунке диаграмма **Box Model** на панели **Стилей** показывает модель окна для выбранного `h1` элемента.</span><span class="sxs-lookup"><span data-stu-id="1cb40-151">In the following figure, the **Box Model** diagram in the **Styles** panel shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Схема модели box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="1cb40-153">Схема **модели box**</span><span class="sxs-lookup"><span data-stu-id="1cb40-153">The **Box Model** diagram</span></span>  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a><span data-ttu-id="1cb40-154">Поиск и фильтрация CSS элемента</span><span class="sxs-lookup"><span data-stu-id="1cb40-154">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="1cb40-155">Для поиска **определенных** свойств \*\*\*\* или значений CSS используйте текстовое поле Filter на панелях **Стилей** и Вычислительные панели.</span><span class="sxs-lookup"><span data-stu-id="1cb40-155">Use the **Filter** text box on the **Styles** and **Computed** panels to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="1cb40-156">Чтобы также найти унаследованные свойства в **панели Computed,** проверьте контрольный ящик **Show All.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-156">To also search inherited properties in the **Computed** panel, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-157">На следующем рисунке панель **Стилей** фильтруется, чтобы показывать только правила, которые включают запрос `color` поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb40-157">In the following figure, the **Styles** panel is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Фильтр панели Стилей" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="1cb40-159">Фильтр панели **Стилей**</span><span class="sxs-lookup"><span data-stu-id="1cb40-159">Filter the **Styles** panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1cb40-160">На следующем рисунке панель **Computed** фильтруется, чтобы показывать только объявления, которые включают запрос `100%` поиска.</span><span class="sxs-lookup"><span data-stu-id="1cb40-160">In the following figure, the **Computed** panel is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Фильтр вычислительной панели" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="1cb40-162">Фильтр **вычислительной панели**</span><span class="sxs-lookup"><span data-stu-id="1cb40-162">Filter the **Computed** panel</span></span>  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a><span data-ttu-id="1cb40-163">Toggle a pseudo-class</span><span class="sxs-lookup"><span data-stu-id="1cb40-163">Toggle a pseudo-class</span></span>  

<span data-ttu-id="1cb40-164">Выполните следующие действия, чтобы переохитрить псевдокласс, например `:active` `:focus` , или `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-164">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="1cb40-165">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-165">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-166">В **инструменте Elements** перейдите на панель **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-166">On the **Elements** tool, navigate to the **Styles** panel.</span></span>  
1.  <span data-ttu-id="1cb40-167">Выберите **:hov**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-167">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="1cb40-168">Проверьте псевдокласс, который необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="1cb40-168">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-169">На следующем рисунке переохитрить `:hover` псевдокласс.</span><span class="sxs-lookup"><span data-stu-id="1cb40-169">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="1cb40-170">В viewport убедитесь, что объявление применяется к элементу, даже если элемент фактически не `background-color: cornflowerblue` зависает.</span><span class="sxs-lookup"><span data-stu-id="1cb40-170">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Toggle the :hover pseudo-class" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="1cb40-172">Toggle the `:hover` pseudo-class</span><span class="sxs-lookup"><span data-stu-id="1cb40-172">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="1cb40-173">Для интерактивного руководства перейдите к [добавлению псевдостата в класс.][DevToolsCSSGetStartedAddPseudoState]</span><span class="sxs-lookup"><span data-stu-id="1cb40-173">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <a name="view-a-page-in-print-mode"></a><span data-ttu-id="1cb40-174">Просмотр страницы в режиме печати</span><span class="sxs-lookup"><span data-stu-id="1cb40-174">View a page in print mode</span></span>  

<span data-ttu-id="1cb40-175">Выполните следующие действия, чтобы просмотреть страницу в режиме печати.</span><span class="sxs-lookup"><span data-stu-id="1cb40-175">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="1cb40-176">[Откройте командное меню.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="1cb40-176">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="1cb40-177">Начните `Rendering` вводить и выберите `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-177">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="1cb40-178">Для **выпадаемой CSS Media** эмулировать выберите **печать**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-178">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a><span data-ttu-id="1cb40-179">Просмотр используемой и неиспользоваемой CSS с помощью средства Coverage</span><span class="sxs-lookup"><span data-stu-id="1cb40-179">View used and unused CSS with the Coverage tool</span></span>  

<span data-ttu-id="1cb40-180">Средство **Coverage** показывает, что на самом деле использует CSS страницы.</span><span class="sxs-lookup"><span data-stu-id="1cb40-180">The **Coverage** tool shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="1cb40-181">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) [][DevToolsCommandMenu]в то время как DevTools находится в центре внимания, чтобы открыть командное меню .</span><span class="sxs-lookup"><span data-stu-id="1cb40-181">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="1cb40-182">Начните `coverage` вводить текст и **выберите показать охват**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-182">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="1cb40-183">Появляется **средство Coverage.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-183">The **Coverage** tool appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Открытие средства Coverage из командного меню" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="1cb40-185">Откройте средство **Coverage** из **командного меню**</span><span class="sxs-lookup"><span data-stu-id="1cb40-185">Open the **Coverage** tool from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Средство Coverage" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="1cb40-187">Средство **Coverage**</span><span class="sxs-lookup"><span data-stu-id="1cb40-187">The **Coverage** tool</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="1cb40-188">Выберите **охват Начните инструментарий и обновите** страницу \. Начните использовать инструменты ![ и обновите ](../media/refresh-icon.msft.png) страницу \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-188">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page](../media/refresh-icon.msft.png)\).</span></span>  <span data-ttu-id="1cb40-189">Страница обновляется, а средство **coverage** предоставляет обзор того, сколько CSS \(и JavaScript\) используется из каждого файла, загруженного браузером.</span><span class="sxs-lookup"><span data-stu-id="1cb40-189">The page refreshes and the **Coverage** tool provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="1cb40-190">Зеленый представляет используемый CSS.</span><span class="sxs-lookup"><span data-stu-id="1cb40-190">Green represents used CSS.</span></span>  <span data-ttu-id="1cb40-191">Красный цвет представляет неиспользована CSS.</span><span class="sxs-lookup"><span data-stu-id="1cb40-191">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Обзор того, сколько CSS (и JavaScript) используется и не используется" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="1cb40-193">Обзор того, сколько CSS \(и JavaScript\) используется и не используется</span><span class="sxs-lookup"><span data-stu-id="1cb40-193">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="1cb40-194">Чтобы отобразить по очереди разбивку того, что используется CSS, выберите CSS-файл.</span><span class="sxs-lookup"><span data-stu-id="1cb40-194">To display a line-by-line breakdown of what CSS is used, choose a CSS file.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1cb40-195">На следующем рисунке не используются строки от 145 до 147 и 149 до 151, в то время как используются строки `b66bc881.site-ltr.css` от 163 до 166.</span><span class="sxs-lookup"><span data-stu-id="1cb40-195">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Разбивка по очереди используемого и неиспользованого CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="1cb40-197">Разбивка по очереди используемого и неиспользованого CSS</span><span class="sxs-lookup"><span data-stu-id="1cb40-197">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a><span data-ttu-id="1cb40-198">Режим предварительного просмотра принудительной печати</span><span class="sxs-lookup"><span data-stu-id="1cb40-198">Force print preview mode</span></span>  

<span data-ttu-id="1cb40-199">Перейдите [к Force DevTools в режиме предварительного просмотра печати.][DevToolsCssPrintPreview]</span><span class="sxs-lookup"><span data-stu-id="1cb40-199">Navigate to [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <a name="change-css"></a><span data-ttu-id="1cb40-200">Изменение CSS</span><span class="sxs-lookup"><span data-stu-id="1cb40-200">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="1cb40-201">Добавление объявления CSS в элемент</span><span class="sxs-lookup"><span data-stu-id="1cb40-201">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="1cb40-202">Порядок объявлений влияет на стиль элемента, используйте следующий список, чтобы помочь вам добавлять объявления по-разному.</span><span class="sxs-lookup"><span data-stu-id="1cb40-202">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="1cb40-203">[Добавление встройного объявления.](#add-an-inline-declaration)</span><span class="sxs-lookup"><span data-stu-id="1cb40-203">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="1cb40-204">Эквивалентно `style` добавлению атрибута в HTML элемента.</span><span class="sxs-lookup"><span data-stu-id="1cb40-204">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="1cb40-205">[Добавьте объявление в правило стиля](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="1cb40-205">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="1cb40-206">Какой рабочий процесс следует использовать?</span><span class="sxs-lookup"><span data-stu-id="1cb40-206">What workflow should you use?</span></span>** <span data-ttu-id="1cb40-207">В большинстве сценариев, вероятно, необходимо использовать рабочий процесс inline declaration.</span><span class="sxs-lookup"><span data-stu-id="1cb40-207">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="1cb40-208">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span><span class="sxs-lookup"><span data-stu-id="1cb40-208">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="1cb40-209">Дополнительные сведения о специфике перейдите к [типам Selector.][MDNSelectorTypes]</span><span class="sxs-lookup"><span data-stu-id="1cb40-209">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="1cb40-210">Если вы отладили все стили элемента и вам необходимо специально проверить, что происходит при определении объявления в разных местах, используйте другой рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="1cb40-210">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <a name="add-an-inline-declaration"></a><span data-ttu-id="1cb40-211">Добавление встройного объявления</span><span class="sxs-lookup"><span data-stu-id="1cb40-211">Add an inline declaration</span></span>  

<span data-ttu-id="1cb40-212">Выполните следующие действия, чтобы добавить встройное объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-212">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="1cb40-213">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-213">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-214">В области **Стилей** выберите между скобками раздела **element.style.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-214">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="1cb40-215">Курсор фокусируется, позволяя вводить текст.</span><span class="sxs-lookup"><span data-stu-id="1cb40-215">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="1cb40-216">Введите имя свойства и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-216">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="1cb40-217">Введите допустимые значения для этого свойства и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-217">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="1cb40-218">В **дереве DOM убедитесь,** что атрибут `style` был добавлен в элемент.</span><span class="sxs-lookup"><span data-stu-id="1cb40-218">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-219">На следующем рисунке свойства и свойства были применены к `margin-top` `background-color` выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="1cb40-219">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="1cb40-220">В **дереве DOM убедитесь,** что объявления отражаются в `style` атрибуте элемента.</span><span class="sxs-lookup"><span data-stu-id="1cb40-220">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Добавление встройных деклараций" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="1cb40-222">Добавление встройных деклараций</span><span class="sxs-lookup"><span data-stu-id="1cb40-222">Add inline declarations</span></span>  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a><span data-ttu-id="1cb40-223">Добавление объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="1cb40-223">Add a declaration to a style rule</span></span>  

<span data-ttu-id="1cb40-224">Выполните следующие действия, чтобы добавить объявление в существующее правило стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-224">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="1cb40-225">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-225">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-226">В области **Стилей** выберите между скобками правила стиля, к которому необходимо добавить объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-226">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="1cb40-227">Курсор фокусируется, позволяя вводить текст.</span><span class="sxs-lookup"><span data-stu-id="1cb40-227">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="1cb40-228">Введите имя свойства и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-228">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="1cb40-229">Введите допустимые значения для этого свойства и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-229">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Добавление объявления в правило стиля" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="1cb40-231">Добавление `border-bottom-style:groove` объявления в правило стиля</span><span class="sxs-lookup"><span data-stu-id="1cb40-231">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a><span data-ttu-id="1cb40-232">Изменение имени или значения объявления</span><span class="sxs-lookup"><span data-stu-id="1cb40-232">Change a declaration name or value</span></span>  

<span data-ttu-id="1cb40-233">Выберите и измените имя или значение объявления, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="1cb40-233">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="1cb40-234">Для ярлыков для быстрого приращения или приумноживления значения на `0.1` , `1` , или `10` `100` единицы, перейдите к [изменению](#change-declaration-values-with-keyboard-shortcuts)значений объявления с помощью клавиши ярлыки .</span><span class="sxs-lookup"><span data-stu-id="1cb40-234">For shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units, navigate to [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts).</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Изменение значения объявления" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="1cb40-236">Изменение значения `border-bottom-style` объявления</span><span class="sxs-lookup"><span data-stu-id="1cb40-236">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a><span data-ttu-id="1cb40-237">Изменение значений объявления с помощью ярлыков клавиатуры</span><span class="sxs-lookup"><span data-stu-id="1cb40-237">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="1cb40-238">При редактировании значения объявления можно использовать следующие клавиши, чтобы приумнозить значение на определенную сумму.</span><span class="sxs-lookup"><span data-stu-id="1cb40-238">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="1cb40-239">Выберите `Alt` + `Up` \(Windows, Linux\) `Option` + `Up` или \(macOS\) для приращения путем `0.1` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-239">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="1cb40-240">Выберите изменение значения путем или путем, если `Up` `1` `0.1` текущее значение находится между `-1` и `1` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-240">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="1cb40-241">Выберите `Shift` + `Up` для приращения `10` путем .</span><span class="sxs-lookup"><span data-stu-id="1cb40-241">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="1cb40-242">Выберите `Shift` + `Page Up` \(Windows, Linux\) `Shift` + `Command` + `Up` или \(macOS\) `100` для приумнождения значения путем .</span><span class="sxs-lookup"><span data-stu-id="1cb40-242">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="1cb40-243">Приумножная работа также работает.</span><span class="sxs-lookup"><span data-stu-id="1cb40-243">Decrementing also works.</span></span>  <span data-ttu-id="1cb40-244">Просто замените каждый экземпляр `Up` упомянутых выше `Down` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-244">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <a name="add-a-class-to-an-element"></a><span data-ttu-id="1cb40-245">Добавление класса в элемент</span><span class="sxs-lookup"><span data-stu-id="1cb40-245">Add a class to an element</span></span>  

<span data-ttu-id="1cb40-246">Выполните следующие действия, чтобы добавить класс в элемент.</span><span class="sxs-lookup"><span data-stu-id="1cb40-246">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="1cb40-247">[Выберите элемент dom](#choose-an-element) **Tree**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-247">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="1cb40-248">Выберите **.cls**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-248">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="1cb40-249">Введите имя класса в текстовом окне **Добавить новый** класс.</span><span class="sxs-lookup"><span data-stu-id="1cb40-249">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="1cb40-250">Выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1cb40-250">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Области классов элементов" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="1cb40-252">Области **классов** элементов</span><span class="sxs-lookup"><span data-stu-id="1cb40-252">The **Element Classes** pane</span></span>  
:::image-end:::  

### <a name="toggle-a-class"></a><span data-ttu-id="1cb40-253">Toggle a class</span><span class="sxs-lookup"><span data-stu-id="1cb40-253">Toggle a class</span></span>  

<span data-ttu-id="1cb40-254">Выполните следующие действия, чтобы включить или отключить класс элемента.</span><span class="sxs-lookup"><span data-stu-id="1cb40-254">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="1cb40-255">[Выберите элемент dom](#choose-an-element) **Tree**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-255">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="1cb40-256">Откройте области **классов** элементов.</span><span class="sxs-lookup"><span data-stu-id="1cb40-256">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="1cb40-257">Перейдите [к добавлению класса к элементу.](#add-a-class-to-an-element)</span><span class="sxs-lookup"><span data-stu-id="1cb40-257">Navigate to [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="1cb40-258">В **текстовом окне Добавить** новый класс приведены все классы, применяемые к конкретному элементу.</span><span class="sxs-lookup"><span data-stu-id="1cb40-258">Below the **Add New Class** text box are all of the classes applied to the specific element.</span></span>  
1.  <span data-ttu-id="1cb40-259">Переключите контрольный ящик рядом с классом, который необходимо включить или отключить.</span><span class="sxs-lookup"><span data-stu-id="1cb40-259">Toggle the checkbox next to the class that you want to turn on or off.</span></span>  

### <a name="add-a-style-rule"></a><span data-ttu-id="1cb40-260">Добавление правила стиля</span><span class="sxs-lookup"><span data-stu-id="1cb40-260">Add a style rule</span></span>  

<span data-ttu-id="1cb40-261">Выполните следующие действия, чтобы добавить новое правило стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-261">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="1cb40-262">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-262">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-263">Выберите **новое правило стиля** \. Новое правило стиля ![ ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-263">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\).</span></span>  <span data-ttu-id="1cb40-264">DevTools вставляет новое правило под **правилом element.style.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-264">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-265">На следующем рисунке DevTools добавляет правило стиля после `h1.devsite-page-title` выбора **правила New Style.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-265">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Добавление нового правила стиля" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="1cb40-267">Добавление нового правила стиля</span><span class="sxs-lookup"><span data-stu-id="1cb40-267">Add a new style rule</span></span>  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a><span data-ttu-id="1cb40-268">Выберите таблицу стилей, чтобы добавить правило</span><span class="sxs-lookup"><span data-stu-id="1cb40-268">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="1cb40-269">При [добавлении](#add-a-style-rule)нового правила стиля выберите и удерживайте правило **New Style** \( New Style Rule \) для выбора таблицы стилей для добавления ![ правила ](../media/new-style-rule-icon.msft.png) стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-269">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Выберите таблицу стилей" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="1cb40-271">Выберите таблицу стилей</span><span class="sxs-lookup"><span data-stu-id="1cb40-271">Choose a stylesheet</span></span>  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a><span data-ttu-id="1cb40-272">Добавление правила стиля в определенное расположение</span><span class="sxs-lookup"><span data-stu-id="1cb40-272">Add a style rule to a specific location</span></span>  

<span data-ttu-id="1cb40-273">Выполните следующие действия, чтобы добавить правило стиля в определенное расположение в панели **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-273">Complete the following actions to add a style rule to a specific location in the **Styles** panel.</span></span>  

1.  <span data-ttu-id="1cb40-274">Наведите курс на правило стиля, которое находится непосредственно над тем, где необходимо добавить новое правило стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-274">Hover on the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="1cb40-275">[ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="1cb40-275">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="1cb40-276">Выберите **Правило стиля вставки ниже** \. ![ Вставить правило стиля ниже значок ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-276">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon](../media/new-style-rule-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Вставьте правило стиля ниже" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="1cb40-278">Вставьте правило стиля ниже</span><span class="sxs-lookup"><span data-stu-id="1cb40-278">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a><span data-ttu-id="1cb40-279">Раскрой панель инструментов More Actions</span><span class="sxs-lookup"><span data-stu-id="1cb40-279">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="1cb40-280">Панель **инструментов More Actions** позволяет выполнять следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1cb40-280">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="1cb40-281">Вставьте правило стиля непосредственно под тем, на который вы ориентированы.</span><span class="sxs-lookup"><span data-stu-id="1cb40-281">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="1cb40-282">Добавьте `background-color` , `color` или объявление к `box-shadow` `text-shadow` правилу стиля, на который вы ориентированы.</span><span class="sxs-lookup"><span data-stu-id="1cb40-282">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="1cb40-283">Выполните следующие действия, чтобы выявить панель **инструментов More Actions.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-283">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="1cb40-284">В панели **Стилей** введите правило стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-284">In the **Styles** panel, hover on a style rule.</span></span>  <span data-ttu-id="1cb40-285">**Дополнительные** действия `...` \( \) раскрыты в нижнем правом разделе правила стиля.</span><span class="sxs-lookup"><span data-stu-id="1cb40-285">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1cb40-286">На следующей фигуре наведите курс на правило стиля, и в нижнем правом разделе правила стиля будет обнаружено больше `.header-holder.has-default-focus` действий. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1cb40-286">In the following figure, hover on the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Раскрыть дополнительные действия" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="1cb40-288">**Раскрой дополнительные** действия `...` \( \)</span><span class="sxs-lookup"><span data-stu-id="1cb40-288">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cb40-289">Наведите **курсор на дополнительные** действия `...` \( \) для раскрытия указанных выше действий.</span><span class="sxs-lookup"><span data-stu-id="1cb40-289">Hover on **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1cb40-290">Действие **Insert Style Под действием вставляется** после нависания над **дополнительными действиями.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-290">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Панель инструментов More Actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="1cb40-292">Панель **инструментов More Actions**</span><span class="sxs-lookup"><span data-stu-id="1cb40-292">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a><span data-ttu-id="1cb40-293">Toggle a declaration</span><span class="sxs-lookup"><span data-stu-id="1cb40-293">Toggle a declaration</span></span>  

<span data-ttu-id="1cb40-294">Выполните действия folllwoing, чтобы переключение одной декларации на \(или off\).</span><span class="sxs-lookup"><span data-stu-id="1cb40-294">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="1cb40-295">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-295">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-296">В области **Стилей** наведите курсор на правило, определя которое определяет объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-296">In the **Styles** pane, hover on the rule that defines the declaration.</span></span>  <span data-ttu-id="1cb40-297">Рядом с каждым объявлением отображается почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="1cb40-297">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="1cb40-298">Проверьте \(или разгрузку\) почтовый ящик рядом с объявлением.</span><span class="sxs-lookup"><span data-stu-id="1cb40-298">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="1cb40-299">При отладке объявления DevTools пересекает его, чтобы указать, что она больше не активна.</span><span class="sxs-lookup"><span data-stu-id="1cb40-299">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="1cb40-300">На следующем рисунке свойство для выбранного в настоящее время элемента `margin-top` отключено.</span><span class="sxs-lookup"><span data-stu-id="1cb40-300">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Toggle a declaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="1cb40-302">Toggle a declaration</span><span class="sxs-lookup"><span data-stu-id="1cb40-302">Toggle a declaration</span></span>  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a><span data-ttu-id="1cb40-303">Добавление объявления фонового цвета</span><span class="sxs-lookup"><span data-stu-id="1cb40-303">Add a background-color declaration</span></span>  

<span data-ttu-id="1cb40-304">Выполните следующие действия, чтобы `background-color` добавить в элемент объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-304">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="1cb40-305">Наведите курс на правило стиля, в которое нужно добавить `background-color` объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-305">Hover on the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="1cb40-306">[ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="1cb40-306">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="1cb40-307">Выберите **Добавить фоновый** цвет \. ![ Добавьте значок фонового ](../media/add-background-color-icon.msft.png) цвета \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-307">Choose **Add Background Color** \(![Add Background Color icon](../media/add-background-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Добавление фонового цвета" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="1cb40-309">Добавление фонового цвета</span><span class="sxs-lookup"><span data-stu-id="1cb40-309">Add Background Color</span></span>**  
:::image-end:::  

### <a name="add-a-color-declaration"></a><span data-ttu-id="1cb40-310">Добавление объявления цвета</span><span class="sxs-lookup"><span data-stu-id="1cb40-310">Add a color declaration</span></span>  

<span data-ttu-id="1cb40-311">Выполните следующие действия, чтобы `color` добавить в элемент объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-311">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="1cb40-312">Наведите курс на правило стиля, в которое нужно добавить `color` объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-312">Hover on the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="1cb40-313">[ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="1cb40-313">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="1cb40-314">Выберите **Добавить цвет** \. Добавить ![ значок цвета ](../media/add-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-314">Choose **Add Color** \(![Add Color icon](../media/add-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Добавление цвета" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="1cb40-316">Добавление цвета</span><span class="sxs-lookup"><span data-stu-id="1cb40-316">Add Color</span></span>**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a><span data-ttu-id="1cb40-317">Добавление объявления box-shadow</span><span class="sxs-lookup"><span data-stu-id="1cb40-317">Add a box-shadow declaration</span></span>  

<span data-ttu-id="1cb40-318">Выполните следующие действия, чтобы `box-shadow` добавить в элемент объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-318">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="1cb40-319">Наведите курс на правило стиля, в которое нужно добавить `box-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-319">Hover on the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="1cb40-320">[ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="1cb40-320">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="1cb40-321">Выберите **Добавить поле Shadow** \. Добавьте ![ значок Тень окна ](../media/add-box-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-321">Choose **Add Box Shadow** \(![Add Box Shadow icon](../media/add-box-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Добавление тени box" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="1cb40-323">Добавление тени box</span><span class="sxs-lookup"><span data-stu-id="1cb40-323">Add Box Shadow</span></span>**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a><span data-ttu-id="1cb40-324">Добавление объявления text-shadow</span><span class="sxs-lookup"><span data-stu-id="1cb40-324">Add a text-shadow declaration</span></span>  

<span data-ttu-id="1cb40-325">Выполните следующие действия, чтобы `text-shadow` добавить в элемент объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-325">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="1cb40-326">Наведите курс на правило стиля, в которое нужно добавить `text-shadow` объявление.</span><span class="sxs-lookup"><span data-stu-id="1cb40-326">Hover on the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="1cb40-327">[ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="1cb40-327">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="1cb40-328">Выберите **Добавить текстовую тень** \. Добавьте ![ значок Text Shadow ](../media/add-text-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="1cb40-328">Choose **Add Text Shadow** \(![Add Text Shadow icon](../media/add-text-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Добавление тени текста" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="1cb40-330">Добавление тени текста</span><span class="sxs-lookup"><span data-stu-id="1cb40-330">Add Text Shadow</span></span>**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a><span data-ttu-id="1cb40-331">Изменение цветов с помощью выборки цвета</span><span class="sxs-lookup"><span data-stu-id="1cb40-331">Change colors with the Color Picker</span></span>  

<span data-ttu-id="1cb40-332">Выбор **цвета предоставляет** GUI для изменений и `color` `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="1cb40-332">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="1cb40-333">Выполните следующие действия, чтобы открыть **выбор цвета.**</span><span class="sxs-lookup"><span data-stu-id="1cb40-333">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="1cb40-334">[Выберите элемент](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="1cb40-334">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="1cb40-335">В панели **Стилей** найдите `color` или `background-color` аналогичное объявление, которое необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="1cb40-335">In the **Styles** panel, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="1cb40-336">Слева от значения , или аналогичного значения, имеется небольшой квадрат, который является `color` `background-color` предварительным просмотром цвета.</span><span class="sxs-lookup"><span data-stu-id="1cb40-336">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1cb40-337">На следующем рисунке небольшой квадрат слева `rgba(0, 0, 0, 0.7)` — это предварительный просмотр этого цвета.</span><span class="sxs-lookup"><span data-stu-id="1cb40-337">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Цвет предварительного просмотра" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="1cb40-339">Цвет предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="1cb40-339">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1cb40-340">Выберите предварительный просмотр, чтобы **открыть выбор цвета**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-340">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Выбор цвета" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="1cb40-342">Выбор **цвета**</span><span class="sxs-lookup"><span data-stu-id="1cb40-342">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="1cb40-343">Следующая фигура и список descries каждого из элементов пользовательского интерфейса **в color Picker**.</span><span class="sxs-lookup"><span data-stu-id="1cb40-343">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Выбор цвета, аннотированный" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="1cb40-345">Выбор **цвета,** аннотированный</span><span class="sxs-lookup"><span data-stu-id="1cb40-345">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-346">1</span><span class="sxs-lookup"><span data-stu-id="1cb40-346">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-347">Оттенки</span><span class="sxs-lookup"><span data-stu-id="1cb40-347">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-348">2</span><span class="sxs-lookup"><span data-stu-id="1cb40-348">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-349">Eyedropper</span><span class="sxs-lookup"><span data-stu-id="1cb40-349">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-350">Дополнительные сведения можно получить в примере цвета со [страницы с помощью eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="1cb40-350">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-351">3</span><span class="sxs-lookup"><span data-stu-id="1cb40-351">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-352">Копировать в буфер</span><span class="sxs-lookup"><span data-stu-id="1cb40-352">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-353">Скопируйте **значение Display в** буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="1cb40-353">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-354">4</span><span class="sxs-lookup"><span data-stu-id="1cb40-354">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-355">Отображение значения</span><span class="sxs-lookup"><span data-stu-id="1cb40-355">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-356">Представление цвета RGBA, HSLA или Hex.</span><span class="sxs-lookup"><span data-stu-id="1cb40-356">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-357">5</span><span class="sxs-lookup"><span data-stu-id="1cb40-357">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-358">Цветовая палитра</span><span class="sxs-lookup"><span data-stu-id="1cb40-358">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-359">Выберите один из квадратов, чтобы изменить цвет на этот квадрат.</span><span class="sxs-lookup"><span data-stu-id="1cb40-359">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-360">6</span><span class="sxs-lookup"><span data-stu-id="1cb40-360">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-361">Hue</span><span class="sxs-lookup"><span data-stu-id="1cb40-361">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-362">7</span><span class="sxs-lookup"><span data-stu-id="1cb40-362">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-363">Opacity (Прозрачность)</span><span class="sxs-lookup"><span data-stu-id="1cb40-363">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-364">8</span><span class="sxs-lookup"><span data-stu-id="1cb40-364">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-365">Переключатель отображения значений</span><span class="sxs-lookup"><span data-stu-id="1cb40-365">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-366">Перетасковка между представлениями RGBA, HSLA и Hex текущего цвета.</span><span class="sxs-lookup"><span data-stu-id="1cb40-366">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="1cb40-367">9</span><span class="sxs-lookup"><span data-stu-id="1cb40-367">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="1cb40-368">Коммутатор цветовой палитры</span><span class="sxs-lookup"><span data-stu-id="1cb40-368">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1cb40-369">Перегиб между палитрой [material Design,][MaterialDesignColorSystem]настраиваемой палитрой или палитрой цветов страниц.</span><span class="sxs-lookup"><span data-stu-id="1cb40-369">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="1cb40-370">DevTools создает цветовую палитру страниц на основе цветов, которые он находит в таблицах стилей.</span><span class="sxs-lookup"><span data-stu-id="1cb40-370">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a><span data-ttu-id="1cb40-371">Пример цвета со страницы с помощью Eyedropper</span><span class="sxs-lookup"><span data-stu-id="1cb40-371">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="1cb40-372">Когда вы открываете **Выбор цвета,** **Eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) находится на по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1cb40-372">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper](../media/eyedropper-icon.msft.png)\) is on by default.</span></span>  <span data-ttu-id="1cb40-373">Выполните следующие действия, чтобы изменить выбранный цвет на другой цвет на странице.</span><span class="sxs-lookup"><span data-stu-id="1cb40-373">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="1cb40-374">Наведите курсор на целевой цвет в представлении.</span><span class="sxs-lookup"><span data-stu-id="1cb40-374">Hover on the target color in the viewport.</span></span>  
1.  <span data-ttu-id="1cb40-375">Выберите подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1cb40-375">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1cb40-376">На следующем рисунке в **списке цветов** указывается текущее значение цвета `rgba(0,0,0,0.7)` , близкое к черному.</span><span class="sxs-lookup"><span data-stu-id="1cb40-376">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="1cb40-377">Определенный цвет должен измениться на версию черного цвета, которая в данный момент выделяется в представлении после его выборки.</span><span class="sxs-lookup"><span data-stu-id="1cb40-377">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Использование eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="1cb40-379">Использование eyedropper</span><span class="sxs-lookup"><span data-stu-id="1cb40-379">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1cb40-380">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1cb40-380">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Добавление псевдостата в класс . Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Просмотр CSS для элемента . Начало работы с просмотром и изменением CSS | Документы Майкрософт"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Force Microsoft Edge DevTools into Print Preview Mode (CSS Print Media Type) | Документы Майкрософт"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Сделайте минированную папку читаемой — отладка ссылки javaScript | Документы Майкрософт"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Цветовая система — material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель окна | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы селекторов — | MDN"  

> [!NOTE]
> <span data-ttu-id="1cb40-390">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1cb40-390">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1cb40-391">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="1cb40-391">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1cb40-393">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1cb40-393">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  