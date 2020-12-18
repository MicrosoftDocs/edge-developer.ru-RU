---
description: Справка по домену CSS. Этот домен предоставляет операции чтения и записи CSS. Все объекты CSS (таблицы стилей, правила и стили) имеют связанные связи, используемые в последующих операциях `id` с связанным объектом. Каждый тип объекта имеет определенную структуру, и они не являются взаимозаменяемыми `id` между объектами разных типов. Объекты CSS можно загружать с помощью вызовов (которые принимают ид `get*ForNode()` узла DOM). Клиент также может отслеживать таблицы стилей с помощью событий, а затем загружать необходимое содержимое таблиц стилей `styleSheetAdded` / `styleSheetRemoved` с помощью `getStyleSheet[Text]()` методов.
title: Домен CSS — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf5efdef09b7e2d9041cd8536faaff8fb99a7f71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235568"
---
# <span data-ttu-id="362dc-108">CSS</span><span class="sxs-lookup"><span data-stu-id="362dc-108">CSS</span></span>

<span data-ttu-id="362dc-109">Этот домен предоставляет операции чтения и записи CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="362dc-110">Все объекты CSS (таблицы стилей, правила и стили) связаны с последующими операциями с `id` этим объектом.</span><span class="sxs-lookup"><span data-stu-id="362dc-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="362dc-111">Каждый тип объекта имеет определенную структуру, и они не являются взаимозаменяемыми `id` между объектами разных типов.</span><span class="sxs-lookup"><span data-stu-id="362dc-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="362dc-112">Объекты CSS можно загружать с помощью вызовов (которые принимают ид `get*ForNode()` узла DOM).</span><span class="sxs-lookup"><span data-stu-id="362dc-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="362dc-113">Клиент также может отслеживать таблицы стилей с помощью событий, а затем загружать необходимое содержимое таблиц стилей `styleSheetAdded` / `styleSheetRemoved` с помощью `getStyleSheet[Text]()` методов.</span><span class="sxs-lookup"><span data-stu-id="362dc-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="362dc-114">Методы</span><span class="sxs-lookup"><span data-stu-id="362dc-114">Methods</span></span>**](#methods) | <span data-ttu-id="362dc-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="362dc-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="362dc-116">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="362dc-116">Events</span></span>**](#events) | <span data-ttu-id="362dc-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="362dc-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="362dc-118">Типы</span><span class="sxs-lookup"><span data-stu-id="362dc-118">Types</span></span>**](#types) | <span data-ttu-id="362dc-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span><span class="sxs-lookup"><span data-stu-id="362dc-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="362dc-120">Зависимости</span><span class="sxs-lookup"><span data-stu-id="362dc-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="362dc-121">DOM</span><span class="sxs-lookup"><span data-stu-id="362dc-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="362dc-122">Методы</span><span class="sxs-lookup"><span data-stu-id="362dc-122">Methods</span></span>

### <span data-ttu-id="362dc-123">"Включить"</span><span class="sxs-lookup"><span data-stu-id="362dc-123">enable</span></span>
<span data-ttu-id="362dc-124">Включает агент CSS для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="362dc-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="362dc-125">Клиенты не должны предполагать, что агент CSS включен, пока не будет получен результат этой команды.</span><span class="sxs-lookup"><span data-stu-id="362dc-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="362dc-126">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="362dc-126">disable</span></span>
<span data-ttu-id="362dc-127">Отключает агент CSS для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="362dc-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="362dc-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="362dc-128">getInlineStylesForNode</span></span>
<span data-ttu-id="362dc-129">Возвращает стили, определенные во вписке (явно в атрибуте style и неявно с использованием атрибутов DOM) для узла DOM, определенного по `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="362dc-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-130">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-131">nodeId</span><span class="sxs-lookup"><span data-stu-id="362dc-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-132">Возвращает</span><span class="sxs-lookup"><span data-stu-id="362dc-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-133">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="362dc-134">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-135">Inline style for the specified DOM node.</span><span class="sxs-lookup"><span data-stu-id="362dc-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-136">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="362dc-137">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-138">Стиль элемента, определяемого атрибутом (например, в результате "width=20 height=100%").</span><span class="sxs-lookup"><span data-stu-id="362dc-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="362dc-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="362dc-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="362dc-140">Возвращает запрашиваемую стили для узла DOM, заденуемого по `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="362dc-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-141">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-142">nodeId</span><span class="sxs-lookup"><span data-stu-id="362dc-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-143">Возвращает</span><span class="sxs-lookup"><span data-stu-id="362dc-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-144">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="362dc-145">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-146">Inline style for the specified DOM node.</span><span class="sxs-lookup"><span data-stu-id="362dc-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-147">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="362dc-148">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-149">Стиль элемента, определяемого атрибутом (например, в результате "width=20 height=100%").</span><span class="sxs-lookup"><span data-stu-id="362dc-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="362dc-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="362dc-151">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="362dc-152">Правила CSS, соответствующие этому узлу, из всех применимых таблиц стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="362dc-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="362dc-154">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="362dc-155">Псевдо стиль соответствует этому узлу.</span><span class="sxs-lookup"><span data-stu-id="362dc-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-156">inherited</span><span class="sxs-lookup"><span data-stu-id="362dc-156">inherited</span></span> <br /> <i><span data-ttu-id="362dc-157">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="362dc-158">Цепочка унаследованных стилей (от непосредственного родительского узла до корневого дерева DOM).</span><span class="sxs-lookup"><span data-stu-id="362dc-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="362dc-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="362dc-160">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="362dc-161">Список анимаций по ключевым рамкам CSS, которые соответствуют этому узлу.</span><span class="sxs-lookup"><span data-stu-id="362dc-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="362dc-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="362dc-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="362dc-163">Запрашивает сведения о шрифтах платформы, которые мы использовали для отрисовки child TextNodes в заданном узле.</span><span class="sxs-lookup"><span data-stu-id="362dc-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-164">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-165">nodeId</span><span class="sxs-lookup"><span data-stu-id="362dc-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-166">Возвращает</span><span class="sxs-lookup"><span data-stu-id="362dc-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-167">fonts</span><span class="sxs-lookup"><span data-stu-id="362dc-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="362dc-168">Статистика использования для каждого шрифта платформы.</span><span class="sxs-lookup"><span data-stu-id="362dc-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="362dc-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="362dc-169">getComputedStyleForNode</span></span>
<span data-ttu-id="362dc-170">Возвращает вычисленный стиль для узла DOM, заденуемого по `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="362dc-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-171">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-172">nodeId</span><span class="sxs-lookup"><span data-stu-id="362dc-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-173">Возвращает</span><span class="sxs-lookup"><span data-stu-id="362dc-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="362dc-175">Вычисляемая стиль для указанного узла DOM.</span><span class="sxs-lookup"><span data-stu-id="362dc-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="362dc-176">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="362dc-176">Events</span></span>

### <span data-ttu-id="362dc-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="362dc-177">styleSheetAdded</span></span>
<span data-ttu-id="362dc-178">Активна при добавлении активной таблицы стилей документов.</span><span class="sxs-lookup"><span data-stu-id="362dc-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-179">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-180">header</span><span class="sxs-lookup"><span data-stu-id="362dc-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="362dc-181">Добавлены метаинфо таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="362dc-182">styleSheetChanged</span><span class="sxs-lookup"><span data-stu-id="362dc-182">styleSheetChanged</span></span>
<span data-ttu-id="362dc-183">Собяно при смене таблицы стилей в результате операции клиента.</span><span class="sxs-lookup"><span data-stu-id="362dc-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-184">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-185">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="362dc-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="362dc-186">styleSheetRemoved</span></span>
<span data-ttu-id="362dc-187">Активна при удалении активной таблицы стилей документов.</span><span class="sxs-lookup"><span data-stu-id="362dc-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-188">Параметры</span><span class="sxs-lookup"><span data-stu-id="362dc-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-189">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-190">Идентификатор удаленного таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="362dc-191">Типы</span><span class="sxs-lookup"><span data-stu-id="362dc-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="362dc-192">StyleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="362dc-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="362dc-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="362dc-194">Коллекция правил CSS для одного псевдо стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-195">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-196">pseudoType</span><span class="sxs-lookup"><span data-stu-id="362dc-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="362dc-197">Псевдоэлементный тип.</span><span class="sxs-lookup"><span data-stu-id="362dc-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-198">matches</span><span class="sxs-lookup"><span data-stu-id="362dc-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="362dc-199">Соответствует правилам CSS, применимым к псевдо-стилю.</span><span class="sxs-lookup"><span data-stu-id="362dc-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="362dc-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="362dc-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="362dc-201">Наследуется коллекция правил CSS от узла-предка.</span><span class="sxs-lookup"><span data-stu-id="362dc-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-202">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-203">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="362dc-204">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-205">Стиль узла-предка (если он есть) в цепочке наследования стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="362dc-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="362dc-207">Совпадения правил CSS, совпадающих с узлом предка в цепочке наследования стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="362dc-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="362dc-208">RuleMatch</span></span> `object`

<span data-ttu-id="362dc-209">Данные совпадения для правила CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-210">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-211">rule</span><span class="sxs-lookup"><span data-stu-id="362dc-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="362dc-212">Правило CSS в совпадении.</span><span class="sxs-lookup"><span data-stu-id="362dc-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="362dc-213">Значение</span><span class="sxs-lookup"><span data-stu-id="362dc-213">Value</span></span> `object`

<span data-ttu-id="362dc-214">Данные для простого селектора (они отсортированы запятой в списке селекторов).</span><span class="sxs-lookup"><span data-stu-id="362dc-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-215">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-216">текст</span><span class="sxs-lookup"><span data-stu-id="362dc-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-217">Текст значения.</span><span class="sxs-lookup"><span data-stu-id="362dc-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-218">range</span><span class="sxs-lookup"><span data-stu-id="362dc-218">range</span></span> <br /> <i><span data-ttu-id="362dc-219">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="362dc-220">Диапазон значений в основном ресурсе (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="362dc-221">SelectorList</span><span class="sxs-lookup"><span data-stu-id="362dc-221">SelectorList</span></span> `object`

<span data-ttu-id="362dc-222">Данные списка селектора.</span><span class="sxs-lookup"><span data-stu-id="362dc-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-223">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-224">селекторы</span><span class="sxs-lookup"><span data-stu-id="362dc-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="362dc-225">Селекторы в списке.</span><span class="sxs-lookup"><span data-stu-id="362dc-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-226">текст</span><span class="sxs-lookup"><span data-stu-id="362dc-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-227">Текст селектора правил.</span><span class="sxs-lookup"><span data-stu-id="362dc-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="362dc-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="362dc-228">CSSRule</span></span> `object`

<span data-ttu-id="362dc-229">Представление правила CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-230">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-231">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="362dc-232">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-233">Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</span><span class="sxs-lookup"><span data-stu-id="362dc-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-234">selectorList</span><span class="sxs-lookup"><span data-stu-id="362dc-234">selectorList</span></span> <br /> <i><span data-ttu-id="362dc-235">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="362dc-236">Данные селектора правил.</span><span class="sxs-lookup"><span data-stu-id="362dc-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-237">origin</span><span class="sxs-lookup"><span data-stu-id="362dc-237">origin</span></span> <br /> <i><span data-ttu-id="362dc-238">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="362dc-239">Происхождение родительской таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-240">style</span><span class="sxs-lookup"><span data-stu-id="362dc-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-241">Объявление связанного стиля.</span><span class="sxs-lookup"><span data-stu-id="362dc-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-242">мультимедиа</span><span class="sxs-lookup"><span data-stu-id="362dc-242">media</span></span> <br /> <i><span data-ttu-id="362dc-243">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="362dc-244">Массив списков мультимедиа (для правил, включающих запросы мультимедиа).</span><span class="sxs-lookup"><span data-stu-id="362dc-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="362dc-245">Массив инициирует запросы мультимедиа, начиная с внутреннего, с выходом из нее.</span><span class="sxs-lookup"><span data-stu-id="362dc-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="362dc-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="362dc-246">SourceRange</span></span> `object`

<span data-ttu-id="362dc-247">Диапазон текста в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="362dc-247">Text range within a resource.</span></span> <span data-ttu-id="362dc-248">Все числа основаны на нулях.</span><span class="sxs-lookup"><span data-stu-id="362dc-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-249">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-250">startLine</span><span class="sxs-lookup"><span data-stu-id="362dc-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="362dc-251">Начальная строка диапазона.</span><span class="sxs-lookup"><span data-stu-id="362dc-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-252">startColumn</span><span class="sxs-lookup"><span data-stu-id="362dc-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="362dc-253">Столбец начала диапазона (включительно).</span><span class="sxs-lookup"><span data-stu-id="362dc-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-254">endLine</span><span class="sxs-lookup"><span data-stu-id="362dc-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="362dc-255">End line of range</span><span class="sxs-lookup"><span data-stu-id="362dc-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-256">endColumn</span><span class="sxs-lookup"><span data-stu-id="362dc-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="362dc-257">Конечный столбец диапазона (монопольный).</span><span class="sxs-lookup"><span data-stu-id="362dc-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="362dc-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="362dc-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-259">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-260">name</span><span class="sxs-lookup"><span data-stu-id="362dc-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-261">Короткое имя.</span><span class="sxs-lookup"><span data-stu-id="362dc-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-262">value</span><span class="sxs-lookup"><span data-stu-id="362dc-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-263">Краткое значение.</span><span class="sxs-lookup"><span data-stu-id="362dc-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-264">important</span><span class="sxs-lookup"><span data-stu-id="362dc-264">important</span></span> <br /> <i><span data-ttu-id="362dc-265">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-266">Имеет ли свойство аннотацию "!important" `false` (подразумевает, если отсутствует).</span><span class="sxs-lookup"><span data-stu-id="362dc-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="362dc-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="362dc-267">CSSStyle</span></span> `object`

<span data-ttu-id="362dc-268">Представление стиля CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-269">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-270">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="362dc-271">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-272">Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</span><span class="sxs-lookup"><span data-stu-id="362dc-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="362dc-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="362dc-274">Свойства CSS в стиле.</span><span class="sxs-lookup"><span data-stu-id="362dc-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="362dc-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="362dc-276">Вычисленные значения для всех ярлыков, найденных в стиле.</span><span class="sxs-lookup"><span data-stu-id="362dc-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-277">cssText</span><span class="sxs-lookup"><span data-stu-id="362dc-277">cssText</span></span> <br /> <i><span data-ttu-id="362dc-278">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-279">Текст объявления стиля (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-280">range</span><span class="sxs-lookup"><span data-stu-id="362dc-280">range</span></span> <br /> <i><span data-ttu-id="362dc-281">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="362dc-282">Диапазон объявлений стилей в заключаемой таблице стилей (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="362dc-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="362dc-283">CSSProperty</span></span> `object`

<span data-ttu-id="362dc-284">Данные объявления свойств CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-285">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-286">name</span><span class="sxs-lookup"><span data-stu-id="362dc-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-287">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="362dc-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-288">value</span><span class="sxs-lookup"><span data-stu-id="362dc-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-289">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="362dc-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-290">important</span><span class="sxs-lookup"><span data-stu-id="362dc-290">important</span></span> <br /> <i><span data-ttu-id="362dc-291">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-292">Имеет ли свойство аннотацию "!important" `false` (подразумевает, если отсутствует).</span><span class="sxs-lookup"><span data-stu-id="362dc-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-293">implicit</span><span class="sxs-lookup"><span data-stu-id="362dc-293">implicit</span></span> <br /> <i><span data-ttu-id="362dc-294">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-295">Является ли свойство неявным `false` (подразумевает, если отсутствует).</span><span class="sxs-lookup"><span data-stu-id="362dc-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-296">текст</span><span class="sxs-lookup"><span data-stu-id="362dc-296">text</span></span> <br /> <i><span data-ttu-id="362dc-297">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-298">Полный текст свойства, указанный в стиле.</span><span class="sxs-lookup"><span data-stu-id="362dc-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="362dc-299">parsedOk</span></span> <br /> <i><span data-ttu-id="362dc-300">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-301">Будет ли свойство понято браузером `true` (подразумевает, если оно отсутствует).</span><span class="sxs-lookup"><span data-stu-id="362dc-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-302">отключено</span><span class="sxs-lookup"><span data-stu-id="362dc-302">disabled</span></span> <br /> <i><span data-ttu-id="362dc-303">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-304">Отключено ли свойство пользователем (присутствует только для свойств на основе источника).</span><span class="sxs-lookup"><span data-stu-id="362dc-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-305">range</span><span class="sxs-lookup"><span data-stu-id="362dc-305">range</span></span> <br /> <i><span data-ttu-id="362dc-306">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="362dc-307">Весь диапазон свойств в объявлении стиля включаемого стиля (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="362dc-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="362dc-308">CSSMedia</span></span> `object`

<span data-ttu-id="362dc-309">Дескриптор правила мультимедиа CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-310">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-311">текст</span><span class="sxs-lookup"><span data-stu-id="362dc-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-312">Текст запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-313">source</span><span class="sxs-lookup"><span data-stu-id="362dc-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="362dc-314">Допустимые значения: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="362dc-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="362dc-315">Источник запроса мультимедиа: "mediaRule", если указано правилом @media, "importRule", если указано правилом @import, "linkedSheet", если он указан атрибутом "media" в теге LINK связанного таблицы стилей, "inlineSheet", если он указан атрибутом "media" в теге STYLE таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="362dc-316">sourceURL</span></span> <br /> <i><span data-ttu-id="362dc-317">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-318">URL-адрес документа, содержащего описание запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-319">range</span><span class="sxs-lookup"><span data-stu-id="362dc-319">range</span></span> <br /> <i><span data-ttu-id="362dc-320">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="362dc-321">Связанный диапазон @media или @import правил в заключаемом таблице стилей (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-322">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="362dc-323">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-324">Идентификатор таблицы стилей, содержащей этот объект (если он существует).</span><span class="sxs-lookup"><span data-stu-id="362dc-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-325">mediaList</span><span class="sxs-lookup"><span data-stu-id="362dc-325">mediaList</span></span> <br /> <i><span data-ttu-id="362dc-326">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="362dc-327">Массив запросов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="362dc-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="362dc-328">MediaQuery</span></span> `object`

<span data-ttu-id="362dc-329">Дескриптор запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-330">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-331">expressions</span><span class="sxs-lookup"><span data-stu-id="362dc-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="362dc-332">Массив выражений запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-333">active</span><span class="sxs-lookup"><span data-stu-id="362dc-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-334">Удовлетворяет ли условие запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="362dc-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="362dc-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="362dc-336">Дескриптор выражения запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-337">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-338">value</span><span class="sxs-lookup"><span data-stu-id="362dc-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-339">Значение выражения запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-340">unit</span><span class="sxs-lookup"><span data-stu-id="362dc-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-341">Единицы выражения запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-342">функция</span><span class="sxs-lookup"><span data-stu-id="362dc-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-343">Функция выражения запроса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="362dc-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="362dc-344">valueRange</span></span> <br /> <i><span data-ttu-id="362dc-345">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="362dc-346">Связанный диапазон текста значения в заключаемой таблице стилей (если он доступен).</span><span class="sxs-lookup"><span data-stu-id="362dc-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="362dc-347">computedLength</span></span> <br /> <i><span data-ttu-id="362dc-348">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-349">Вычисляемая длина выражения запроса мультимедиа (если применимо).</span><span class="sxs-lookup"><span data-stu-id="362dc-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="362dc-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="362dc-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="362dc-351">Сведения о количестве глифов, которые были отрисовыы с помощью заданного шрифта.</span><span class="sxs-lookup"><span data-stu-id="362dc-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-352">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-353">familyName</span><span class="sxs-lookup"><span data-stu-id="362dc-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-354">Имя семейства шрифта, сообщаемая платформой.</span><span class="sxs-lookup"><span data-stu-id="362dc-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="362dc-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-356">Указывает, был ли шрифт загружен или разрешен локально.</span><span class="sxs-lookup"><span data-stu-id="362dc-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="362dc-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-358">Количество глифов, которые были отрисовыы с помощью этого шрифта.</span><span class="sxs-lookup"><span data-stu-id="362dc-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="362dc-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="362dc-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="362dc-360">Представление правила по ключевым рамкам CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-361">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-362">animationName</span><span class="sxs-lookup"><span data-stu-id="362dc-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="362dc-363">Имя анимации.</span><span class="sxs-lookup"><span data-stu-id="362dc-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-364">keyframes</span><span class="sxs-lookup"><span data-stu-id="362dc-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="362dc-365">Список ключевых моментов.</span><span class="sxs-lookup"><span data-stu-id="362dc-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="362dc-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="362dc-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="362dc-367">Представление правила по ключевым рамкам CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-368">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-369">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="362dc-370">необязательные</span><span class="sxs-lookup"><span data-stu-id="362dc-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-371">Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</span><span class="sxs-lookup"><span data-stu-id="362dc-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-372">origin</span><span class="sxs-lookup"><span data-stu-id="362dc-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="362dc-373">Происхождение родительской таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-374">keyText</span><span class="sxs-lookup"><span data-stu-id="362dc-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="362dc-375">Связанный текст ключа.</span><span class="sxs-lookup"><span data-stu-id="362dc-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-376">style</span><span class="sxs-lookup"><span data-stu-id="362dc-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="362dc-377">Объявление связанного стиля.</span><span class="sxs-lookup"><span data-stu-id="362dc-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="362dc-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="362dc-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-379">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-380">name</span><span class="sxs-lookup"><span data-stu-id="362dc-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-381">Имя вычисленного свойства стиля.</span><span class="sxs-lookup"><span data-stu-id="362dc-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-382">value</span><span class="sxs-lookup"><span data-stu-id="362dc-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-383">Значение свойства computed style.</span><span class="sxs-lookup"><span data-stu-id="362dc-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="362dc-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="362dc-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="362dc-385">Метаинформация таблиц стилей CSS.</span><span class="sxs-lookup"><span data-stu-id="362dc-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="362dc-386">Свойства</span><span class="sxs-lookup"><span data-stu-id="362dc-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="362dc-387">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="362dc-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="362dc-388">Идентификатор таблицы стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="362dc-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="362dc-390">URL-адрес ресурса Stylesheet.</span><span class="sxs-lookup"><span data-stu-id="362dc-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-391">отключено</span><span class="sxs-lookup"><span data-stu-id="362dc-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-392">Обозначает, отключена ли таблица стилей.</span><span class="sxs-lookup"><span data-stu-id="362dc-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-393">isInline</span><span class="sxs-lookup"><span data-stu-id="362dc-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="362dc-394">Создается ли эта таблица стилей для тега STYLE с помощью разметки.</span><span class="sxs-lookup"><span data-stu-id="362dc-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="362dc-395">Этот флаг не установлен для тегов DOCUMENT.written STYLE.</span><span class="sxs-lookup"><span data-stu-id="362dc-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-396">startLine</span><span class="sxs-lookup"><span data-stu-id="362dc-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-397">Смещение строк таблицы стилей в ресурсе (на основе нуля).</span><span class="sxs-lookup"><span data-stu-id="362dc-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-398">startColumn</span><span class="sxs-lookup"><span data-stu-id="362dc-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-399">Смещение столбцов таблицы стилей в ресурсе (на основе нуля).</span><span class="sxs-lookup"><span data-stu-id="362dc-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="362dc-400">length</span><span class="sxs-lookup"><span data-stu-id="362dc-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="362dc-401">Размер содержимого (в символах).</span><span class="sxs-lookup"><span data-stu-id="362dc-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="362dc-402">Зависимости</span><span class="sxs-lookup"><span data-stu-id="362dc-402">Dependencies</span></span>

[<span data-ttu-id="362dc-403">DOM</span><span class="sxs-lookup"><span data-stu-id="362dc-403">DOM</span></span>](dom.md)
