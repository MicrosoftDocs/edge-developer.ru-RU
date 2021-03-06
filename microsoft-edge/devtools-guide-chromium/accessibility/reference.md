---
description: Полная ссылка на функции доступности в Microsoft Edge DevTools.
title: Справка о доступности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e3fed1c4e53c69b7a6837f71c270c0bf2f65b7e2
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398338"
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

# <a name="accessibility-reference"></a><span data-ttu-id="395dc-104">Справка о доступности</span><span class="sxs-lookup"><span data-stu-id="395dc-104">Accessibility reference</span></span>  

<span data-ttu-id="395dc-105">Эта страница — это всеобъемлющая ссылка на функции доступности в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="395dc-105">This page is a comprehensive reference of accessibility features in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="395dc-106">Он предназначен для веб-разработчиков, которые:</span><span class="sxs-lookup"><span data-stu-id="395dc-106">It is intended for web developers who:</span></span>  

*   <span data-ttu-id="395dc-107">У вас есть базовое представление о DevTools, например о том, как его открыть.</span><span class="sxs-lookup"><span data-stu-id="395dc-107">Have a basic understanding of DevTools, such as how to open it.</span></span>  
*   <span data-ttu-id="395dc-108">Знакомы с [принципами доступности и лучшими практиками.][MDNAccessibility]</span><span class="sxs-lookup"><span data-stu-id="395dc-108">Are familiar with [accessibility principles and best practices][MDNAccessibility].</span></span>  
    
<span data-ttu-id="395dc-109">Эта ссылка поможет вам найти все средства, доступные в DevTools, которые помогут вам изучить доступность страницы.</span><span class="sxs-lookup"><span data-stu-id="395dc-109">The purpose of this reference is to help you discover all of the tools available in DevTools that help you examine the accessibility of a page.</span></span>  

<span data-ttu-id="395dc-110">Если вы ищете помощь в навигации по DevTools с помощью вспомогательных технологий, таких как считыватель экрана, перейдите к навигации [Microsoft Edge DevTools с помощью вспомогательных технологий][DevtoolsAccessibilityNavigation].</span><span class="sxs-lookup"><span data-stu-id="395dc-110">If you are looking for help on navigating DevTools with an assistive technology like a screen reader, navigate to [Navigating Microsoft Edge DevTools With Assistive Technology][DevtoolsAccessibilityNavigation].</span></span>  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a><span data-ttu-id="395dc-111">Обзор возможностей доступности в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="395dc-111">Overview of accessibility features in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="395dc-112">В этом разделе объясняется, как DevTools вписывается в общий набор средств доступности.</span><span class="sxs-lookup"><span data-stu-id="395dc-112">This section explains how DevTools fits into your overall accessibility toolkit.</span></span>  

<span data-ttu-id="395dc-113">При определении доступности страницы необходимо иметь в виду 2 общих вопроса:</span><span class="sxs-lookup"><span data-stu-id="395dc-113">When determining whether a page is accessible, you need to have 2 general questions in mind:</span></span>  

1.  <span data-ttu-id="395dc-114">Можете ли вы перемещаться по странице с помощью клавиатуры или [чтения с экрана?][MDNScreenReader]</span><span class="sxs-lookup"><span data-stu-id="395dc-114">Are you able to navigate the page with a keyboard or [screen reader][MDNScreenReader]?</span></span>  
1.  <span data-ttu-id="395dc-115">Правильно ли помечены элементы страницы для чтения с экрана?</span><span class="sxs-lookup"><span data-stu-id="395dc-115">Are the elements of the page properly marked up for screen readers?</span></span>  
    
<span data-ttu-id="395dc-116">В общем, DevTools должен помочь вам устранить ошибки, связанные с вопросом #2, так как эти ошибки легко обнаружить в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="395dc-116">In general, DevTools should help you fix errors related to question #2, because these errors are easy to detect in an automated fashion.</span></span>  <span data-ttu-id="395dc-117">Вопрос #1 так же важен, но, к сожалению, DevTools не поможет вам там.</span><span class="sxs-lookup"><span data-stu-id="395dc-117">Question #1 is just as important, but unfortunately DevTools does not help you there.</span></span>  <span data-ttu-id="395dc-118">Единственный способ найти ошибки, связанные с вопросом #1, это попробовать использовать страницу с клавиатурой или экраном чтения самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="395dc-118">The only way to find errors related to question #1 is to try using a page with a keyboard or screen reader yourself.</span></span>  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a><span data-ttu-id="395dc-119">Аудит доступности страницы</span><span class="sxs-lookup"><span data-stu-id="395dc-119">Audit the accessibility of a page</span></span>  

> [!NOTE]
> <span data-ttu-id="395dc-120">Средство **аудита** предоставляет ссылки на контент, который содержится на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="395dc-120">The **Audits** tool provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="395dc-121">Корпорация Майкрософт не несет ответственности и не контролирует содержимое этих сайтов и любые данные, которые могут быть собраны.</span><span class="sxs-lookup"><span data-stu-id="395dc-121">Microsoft is not responsible for and has no control over the content of these sites and any data that may be collected.</span></span>  

<span data-ttu-id="395dc-122">В общем случае используйте панель аудитов, чтобы определить, если:</span><span class="sxs-lookup"><span data-stu-id="395dc-122">In general, use the Audits panel to determine if:</span></span>  

*   <span data-ttu-id="395dc-123">Страница правильно помечена для чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="395dc-123">A page is properly marked up for screen readers.</span></span>  
*   <span data-ttu-id="395dc-124">Текстовые элементы на странице имеют достаточные коэффициенты контрастности.</span><span class="sxs-lookup"><span data-stu-id="395dc-124">The text elements on a page have sufficient contrast ratios.</span></span>  <span data-ttu-id="395dc-125">Перейдите [к просмотру соотношения контрастности текстового элемента в элементе Color Picker.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)</span><span class="sxs-lookup"><span data-stu-id="395dc-125">Navigate to [View the contrast ratio of a text element in the Color Picker](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker).</span></span>  

<span data-ttu-id="395dc-126">Аудит страницы:</span><span class="sxs-lookup"><span data-stu-id="395dc-126">To audit a page:</span></span>  

1.  <span data-ttu-id="395dc-127">Перейдите к URL-адресу, который необходимо аудитировать.</span><span class="sxs-lookup"><span data-stu-id="395dc-127">Navigate to the URL that you want to audit.</span></span>  
1.  <span data-ttu-id="395dc-128">В DevTools выберите средство **аудита.**</span><span class="sxs-lookup"><span data-stu-id="395dc-128">In DevTools, choose the **Audits** tool.</span></span>  <span data-ttu-id="395dc-129">В DevTools показаны различные параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="395dc-129">DevTools shows you various configuration options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-pane.msft.png":::
       <span data-ttu-id="395dc-131">Настройка аудита</span><span class="sxs-lookup"><span data-stu-id="395dc-131">Configure audits</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="395dc-132">Скриншоты в этом разделе были сделаны с помощью версии 79 Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="395dc-132">The screenshots in this section were taken with version 79 of Microsoft Edge.</span></span>  <span data-ttu-id="395dc-133">Вы можете проверить, в какой версии вы `edge://version` работаете.</span><span class="sxs-lookup"><span data-stu-id="395dc-133">You may check what version you are running at `edge://version`.</span></span>  <span data-ttu-id="395dc-134">Пользовательский **интерфейс** средства аудита выглядит иначе в более ранних версиях Microsoft Edge, но общий рабочий процесс одинаковый.</span><span class="sxs-lookup"><span data-stu-id="395dc-134">The **Audits** tool UI looks different in earlier versions of Microsoft Edge, but the general workflow is the same.</span></span>  
    
1.  <span data-ttu-id="395dc-135">Для **устройства**выберите **Mobile,** если вы хотите смоделировать мобильное устройство.</span><span class="sxs-lookup"><span data-stu-id="395dc-135">For **Device**, choose **Mobile** if you want to simulate a mobile device.</span></span>  <span data-ttu-id="395dc-136">Этот параметр изменяет строку агента пользователя и изменяет параметр viewport.</span><span class="sxs-lookup"><span data-stu-id="395dc-136">This option changes your user agent string and resizes the viewport.</span></span>  <span data-ttu-id="395dc-137">Если мобильная версия страницы отображает не так, как в настольной версии, этот параметр может существенно действовать на результаты аудита.</span><span class="sxs-lookup"><span data-stu-id="395dc-137">If the mobile version of the page displays differently than the desktop version, this option may have a significant effect on the results of your audit.</span></span>  
1.  <span data-ttu-id="395dc-138">В разделе **Аудиты** убедитесь, что **включена доступность.**</span><span class="sxs-lookup"><span data-stu-id="395dc-138">In the **Audits** section, make sure that **Accessibility** is enabled.</span></span>  <span data-ttu-id="395dc-139">Отключите другие категории, если вы хотите исключить их из отчета.</span><span class="sxs-lookup"><span data-stu-id="395dc-139">Disable the other categories if you want to exclude them from your report.</span></span>  <span data-ttu-id="395dc-140">Оставьте их включенными, если вы хотите найти другие способы улучшения качества страницы.</span><span class="sxs-lookup"><span data-stu-id="395dc-140">Leave them enabled if you want to discover other ways to improve the quality of your page.</span></span>  
1.  <span data-ttu-id="395dc-141">Раздел **регулирование позволяет** управлять сетью и ЦП, что полезно при анализе производительности нагрузки.</span><span class="sxs-lookup"><span data-stu-id="395dc-141">The **Throttling** section lets you throttle the network and CPU, which is useful when analyzing load performance.</span></span>  <span data-ttu-id="395dc-142">Этот параметр должен быть неактуален для оценки доступности, поэтому вы можете использовать все, что хотите.</span><span class="sxs-lookup"><span data-stu-id="395dc-142">This option should be irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="395dc-143">Почтовый **ящик Clear Storage** позволяет очистить все хранилища перед загрузкой страницы или сохранить хранилище между нагрузками на страницу.</span><span class="sxs-lookup"><span data-stu-id="395dc-143">The **Clear Storage** checkbox lets you clear all storage before loading the page, or preserve storage between page loads.</span></span>  <span data-ttu-id="395dc-144">Этот параметр также, вероятно, не имеет значения для оценки доступности, поэтому вы можете использовать все, что вы предпочитаете.</span><span class="sxs-lookup"><span data-stu-id="395dc-144">This option is also probably irrelevant to your accessibility score, so you may use whatever you prefer.</span></span>  
1.  <span data-ttu-id="395dc-145">Выберите **выполнить аудиты.**</span><span class="sxs-lookup"><span data-stu-id="395dc-145">Choose **Run Audits**.</span></span> <span data-ttu-id="395dc-146">Через 10-30 секунд DevTools предоставляет отчет.</span><span class="sxs-lookup"><span data-stu-id="395dc-146">After 10 to 30 seconds, DevTools provides a report.</span></span>  <span data-ttu-id="395dc-147">В отчете вы можете получить различные советы по улучшению доступности страницы.</span><span class="sxs-lookup"><span data-stu-id="395dc-147">Your report gives you various tips on how to improve the accessibility of the page.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Отчет" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       <span data-ttu-id="395dc-149">Отчет</span><span class="sxs-lookup"><span data-stu-id="395dc-149">A report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="395dc-150">Чтобы узнать больше об этом, выберите аудит.</span><span class="sxs-lookup"><span data-stu-id="395dc-150">Choose an audit to learn more about it.</span></span>  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Дополнительные сведения о аудите" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       <span data-ttu-id="395dc-152">Дополнительные сведения о аудите</span><span class="sxs-lookup"><span data-stu-id="395dc-152">More information about an audit</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="395dc-153">Чтобы **просмотреть** документацию этого аудита, выберите Дополнительные дополнительные.</span><span class="sxs-lookup"><span data-stu-id="395dc-153">Choose **Learn More** to view the documentation of that audit.</span></span>  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Просмотр документации аудита" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       <span data-ttu-id="395dc-155">Просмотр документации аудита</span><span class="sxs-lookup"><span data-stu-id="395dc-155">View the documentation of an audit</span></span>  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a><span data-ttu-id="395dc-156">См. также: расширение aXe</span><span class="sxs-lookup"><span data-stu-id="395dc-156">See also: aXe extension</span></span>  

<span data-ttu-id="395dc-157">Вы можете использовать расширение [aXe,][ChromeWebStoreAxe] а не средство **аудита.**</span><span class="sxs-lookup"><span data-stu-id="395dc-157">You may prefer to use the [aXe extension][ChromeWebStoreAxe] rather than the **Audits** tool.</span></span>  
<span data-ttu-id="395dc-158">Расширение aXe обычно предоставляет ту же информацию, так как это является движком, который приводит в движок панели Аудиты.</span><span class="sxs-lookup"><span data-stu-id="395dc-158">The aXe extension generally provides the same information, since it is the underlying engine that powers the Audits panel.</span></span>  <span data-ttu-id="395dc-159">Расширение aXe имеет другой пользовательский интерфейс и описывает аудиты немного по-другому.</span><span class="sxs-lookup"><span data-stu-id="395dc-159">The aXe extension has a different UI and describes audits slightly differently.</span></span>  
<span data-ttu-id="395dc-160">Одно из преимуществ расширения aXe над средством **Аудита** заключается в том, что оно позволяет проверять и выделять узлы с ошибками.</span><span class="sxs-lookup"><span data-stu-id="395dc-160">One advantage that the aXe extension has over the **Audits** tool is that it enables you to inspect and highlight failing nodes.</span></span>  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Расширение aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   <span data-ttu-id="395dc-162">Расширение aXe</span><span class="sxs-lookup"><span data-stu-id="395dc-162">The aXe extension</span></span>  
:::image-end:::  

## <a name="the-accessibility-panel"></a><span data-ttu-id="395dc-163">Панель доступности</span><span class="sxs-lookup"><span data-stu-id="395dc-163">The Accessibility panel</span></span>  

<span data-ttu-id="395dc-164">Панель **доступности** — это панель, на которой вы видите дерево доступности, атрибуты ARIA и вычислительные свойства узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="395dc-164">The **Accessibility** panel is where you view the accessibility tree, ARIA attributes, and computed accessibility properties of DOM nodes.</span></span>  

<span data-ttu-id="395dc-165">Чтобы открыть панель **доступности:**</span><span class="sxs-lookup"><span data-stu-id="395dc-165">To open the **Accessibility** panel:</span></span>  

1.  <span data-ttu-id="395dc-166">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="395dc-166">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="395dc-167">В дереве **DOM выберите**элемент, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="395dc-167">In the **DOM Tree**, select the element which you want to inspect.</span></span>  
1.  <span data-ttu-id="395dc-168">Выберите панель **доступности.**</span><span class="sxs-lookup"><span data-stu-id="395dc-168">Choose the **Accessibility** panel.</span></span>  <span data-ttu-id="395dc-169">Эта панель может быть скрыта за кнопкой **More Tabs** \( ![ More Tabs ][ImageMoreTabsIcon] \)</span><span class="sxs-lookup"><span data-stu-id="395dc-169">This panel may be hidden behind the **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) button.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Проверьте элемент h1 домашней страницы DevTools в панели доступности" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   <span data-ttu-id="395dc-171">Проверьте `h1` элемент домашней страницы DevTools в панели **доступности**</span><span class="sxs-lookup"><span data-stu-id="395dc-171">Inspect the `h1` element of the DevTools homepage in the **Accessibility** panel</span></span>  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a><span data-ttu-id="395dc-172">Просмотр положения элемента в дереве доступности</span><span class="sxs-lookup"><span data-stu-id="395dc-172">View the position of an element in the accessibility tree</span></span>  

<span data-ttu-id="395dc-173">Дерево [доступности][MDNAccessibilityTree] — это подмножество дерева DOM.</span><span class="sxs-lookup"><span data-stu-id="395dc-173">The [accessibility tree][MDNAccessibilityTree] is a subset of the DOM tree.</span></span>  <span data-ttu-id="395dc-174">Он содержит только элементы из дерева DOM, которые являются актуальными и полезными для отображения содержимого страницы в считыватель экрана.</span><span class="sxs-lookup"><span data-stu-id="395dc-174">It only contains elements from the DOM tree that are relevant and useful for displaying the contents of a page in a screen reader.</span></span>  

<span data-ttu-id="395dc-175">Проверьте положение элемента в дереве доступности из панели [accessibility.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="395dc-175">Inspect the position of an element in the accessibility tree from the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Раздел Дерево доступности" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   <span data-ttu-id="395dc-177">Раздел **Дерево доступности**</span><span class="sxs-lookup"><span data-stu-id="395dc-177">The **Accessibility Tree** section</span></span>  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a><span data-ttu-id="395dc-178">Просмотр атрибутов ARIA элемента</span><span class="sxs-lookup"><span data-stu-id="395dc-178">View the ARIA attributes of an element</span></span>  

<span data-ttu-id="395dc-179">Атрибуты ARIA гарантируют, что читатели экрана будут иметь всю необходимую информацию для правильного представления содержимого страницы.</span><span class="sxs-lookup"><span data-stu-id="395dc-179">ARIA attributes ensure that screen readers have all of the information that they need in order to properly represent the contents of a page.</span></span>  

<span data-ttu-id="395dc-180">Просмотр атрибутов ARIA элемента в панели [доступности.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="395dc-180">View the ARIA attributes of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Раздел Атрибуты ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   <span data-ttu-id="395dc-182">Раздел **Атрибуты ARIA**</span><span class="sxs-lookup"><span data-stu-id="395dc-182">The **ARIA Attributes** section</span></span>  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a><span data-ttu-id="395dc-183">Просмотр свойств вычислительной доступности элемента</span><span class="sxs-lookup"><span data-stu-id="395dc-183">View the computed accessibility properties of an element</span></span>  

> [!NOTE]
> <span data-ttu-id="395dc-184">Если вы ищете вычислительные свойства CSS, перейдите на [панель Computed.][DevtoolsCssReferenceViewActuallyAppliedElements]</span><span class="sxs-lookup"><span data-stu-id="395dc-184">If you are looking for computed CSS properties, navigate to [Computed][DevtoolsCssReferenceViewActuallyAppliedElements] panel.</span></span>  

<span data-ttu-id="395dc-185">Некоторые свойства доступности динамически вычисляются браузером.</span><span class="sxs-lookup"><span data-stu-id="395dc-185">Some accessibility properties are dynamically calculated by the browser.</span></span>  <span data-ttu-id="395dc-186">Эти свойства отображаются в разделе **Computed Properties** панели **доступности.**</span><span class="sxs-lookup"><span data-stu-id="395dc-186">These properties are displayed in the **Computed Properties** section of the **Accessibility** panel.</span></span>  

<span data-ttu-id="395dc-187">Просмотр свойств вычислительной доступности элемента в панели [доступности.](#the-accessibility-panel)</span><span class="sxs-lookup"><span data-stu-id="395dc-187">View the computed accessibility properties of an element in the [Accessibility](#the-accessibility-panel) panel.</span></span>  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Раздел Computed Properties панели доступности" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   <span data-ttu-id="395dc-189">Раздел **Computed Properties** панели **доступности**</span><span class="sxs-lookup"><span data-stu-id="395dc-189">The **Computed Properties** section of the **Accessibility** panel</span></span>  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a><span data-ttu-id="395dc-190">Просмотр соотношения контрастности текстового элемента в элементе Color Picker</span><span class="sxs-lookup"><span data-stu-id="395dc-190">View the contrast ratio of a text element in the Color Picker</span></span>  

<span data-ttu-id="395dc-191">Некоторые люди с низким зрением не видят области как очень яркие или очень темные.</span><span class="sxs-lookup"><span data-stu-id="395dc-191">Some people with low vision do not see areas as very bright or very dark.</span></span>  <span data-ttu-id="395dc-192">Все имеет тенденцию отображаться примерно с одинаковой яркостью, что затрудняет разграничение контуров и краев.</span><span class="sxs-lookup"><span data-stu-id="395dc-192">Everything tends to appear at about the same brightness, which makes it hard to distinguish outlines and edges.</span></span>  

<span data-ttu-id="395dc-193">Коэффициент контрастности измеряет разницу в яркости между переднем плане и фоном текста.</span><span class="sxs-lookup"><span data-stu-id="395dc-193">Contrast ratio measures the difference in brightness between the foreground and background of text.</span></span>  <span data-ttu-id="395dc-194">Если в тексте низкий контраст, то пользователи с низким зрением могут буквально оказаться на вашем сайте в виде пустого экрана.</span><span class="sxs-lookup"><span data-stu-id="395dc-194">If your text has a low contrast ratio, then these low vision users may literally experience your site as a blank screen.</span></span>  

<span data-ttu-id="395dc-195">Выбор цвета поможет вам убедиться, что текст соответствует рекомендуемым уровням коэффициента контрастности:</span><span class="sxs-lookup"><span data-stu-id="395dc-195">The Color Picker helps you verify that your text meets recommended contrast ratio levels:</span></span>  

1.  <span data-ttu-id="395dc-196">Выберите **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="395dc-196">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="395dc-197">В **дереве DOM выберите**текстовый элемент, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="395dc-197">In the **DOM Tree**, select the text element that you want to inspect.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Проверка абзаца в дереве DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       <span data-ttu-id="395dc-199">Проверка абзаца **в дереве DOM**</span><span class="sxs-lookup"><span data-stu-id="395dc-199">Inspect a paragraph in the **DOM Tree**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="395dc-200">В панели **Стилей** выберите цветной квадрат рядом со `color` значением элемента.</span><span class="sxs-lookup"><span data-stu-id="395dc-200">In the **Styles** panel, choose the color square next to the `color` value of the element.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Свойство цвета элемента" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       <span data-ttu-id="395dc-202">Свойство `color` элемента</span><span class="sxs-lookup"><span data-stu-id="395dc-202">The `color` property of the element</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="395dc-203">Проверьте раздел **Коэффициент контрастности** в цветопоимке.</span><span class="sxs-lookup"><span data-stu-id="395dc-203">Check the **Contrast Ratio** section of the Color Picker.</span></span>  <span data-ttu-id="395dc-204">Одна из контрольных знаков означает, что элемент соответствует [минимальной рекомендации.][W3CContrastMinimum]</span><span class="sxs-lookup"><span data-stu-id="395dc-204">One checkmark means that the element meets the [minimum recommendation][W3CContrastMinimum].</span></span>  <span data-ttu-id="395dc-205">Два контрольных знака означает, что он соответствует [расширенной рекомендации][W3CContrastEnhanced].</span><span class="sxs-lookup"><span data-stu-id="395dc-205">Two checkmarks means that it meets the [enhanced recommendation][W3CContrastEnhanced].</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="В разделе Коэффициент контрастности в средстве выборки цвета показаны 2 контрольных знака и значение 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       <span data-ttu-id="395dc-207">В **разделе Коэффициент** контрастности в средстве цветопоимыватель показаны 2 контрольных знака и значение</span><span class="sxs-lookup"><span data-stu-id="395dc-207">The **Contrast Ratio** section of the Color Picker shows 2 checkmarks and a value of</span></span> `13.97`  
    :::image-end:::  
    
1.  <span data-ttu-id="395dc-208">Дополнительные сведения можно получить в разделе **Коэффициент контрастности.**</span><span class="sxs-lookup"><span data-stu-id="395dc-208">For more information, choose the **Contrast Ratio** section.</span></span>  <span data-ttu-id="395dc-209">Строка отображается в визуальном выборщике в верхней части выборки цвета.</span><span class="sxs-lookup"><span data-stu-id="395dc-209">A line appears in the visual picker at the top of the Color Picker.</span></span>  <span data-ttu-id="395dc-210">Если текущий цвет соответствует рекомендациям, то все, что на той же стороне линии, также соответствует рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="395dc-210">If the current color meets recommendations, then anything on the same side of the line also meets recommendations.</span></span>  <span data-ttu-id="395dc-211">Если текущий цвет не соответствует рекомендациям, то все, что имеет одну и ту же сторону, также не соответствует рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="395dc-211">If the current color does not meet recommendations, then anything on the same side also does not meet recommendations.</span></span>  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Линия коэффициента контрастности в визуальном выборке" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       <span data-ttu-id="395dc-213">Линия **коэффициента контрастности** в визуальном выборке</span><span class="sxs-lookup"><span data-stu-id="395dc-213">The **Contrast Ratio** Line in the visual picker</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="395dc-214">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="395dc-214">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Перейдите по Microsoft Edge DevTools с помощью вспомогательных технологий | Документы Майкрософт"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Просмотр только CSS, который на самом деле применяется к элементу — CSS Reference | Документы Майкрософт"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe — тестирование веб-доступности — Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Дерево доступности (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Доступность | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Считыватель | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contrast (Enhanced) Level AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Контрастный (минимальный) уровень AA | W3C"  

> [!NOTE]
> <span data-ttu-id="395dc-223">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="395dc-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="395dc-224">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="395dc-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="395dc-226">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="395dc-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
