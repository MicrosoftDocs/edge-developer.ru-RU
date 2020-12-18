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
# CSS

Этот домен предоставляет операции чтения и записи CSS. Все объекты CSS (таблицы стилей, правила и стили) связаны с последующими операциями с `id` этим объектом. Каждый тип объекта имеет определенную структуру, и они не являются взаимозаменяемыми `id` между объектами разных типов. Объекты CSS можно загружать с помощью вызовов (которые принимают ид `get*ForNode()` узла DOM). Клиент также может отслеживать таблицы стилей с помощью событий, а затем загружать необходимое содержимое таблиц стилей `styleSheetAdded` / `styleSheetRemoved` с помощью `getStyleSheet[Text]()` методов.

| | |
|-|-|
| [**Методы**](#methods) | [enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**Мероприятия**](#events) | [styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Типы**](#types) | [StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader) |
| [**Зависимости**](#dependencies) | [DOM](dom.md) |
## Методы

### "Включить"
Включает агент CSS для заданной страницы. Клиенты не должны предполагать, что агент CSS включен, пока не будет получен результат этой команды.

</p>

---

### "Отключить" 
Отключает агент CSS для заданной страницы.

</p>

---

### getInlineStylesForNode
Возвращает стили, определенные во вписке (явно в атрибуте style и неявно с использованием атрибутов DOM) для узла DOM, определенного по `nodeId` .

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Возвращает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Inline style for the specified DOM node.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Стиль элемента, определяемого атрибутом (например, в результате "width=20 height=100%").</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Возвращает запрашиваемую стили для узла DOM, заденуемого по `nodeId` .

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Возвращает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Inline style for the specified DOM node.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Стиль элемента, определяемого атрибутом (например, в результате "width=20 height=100%").</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>необязательные</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Правила CSS, соответствующие этому узлу, из всех применимых таблиц стилей.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>необязательные</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>Псевдо стиль соответствует этому узлу.</td>
        </tr>
        <tr>
            <td>inherited <br /> <i>необязательные</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Цепочка унаследованных стилей (от непосредственного родительского узла до корневого дерева DOM).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>необязательные</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Список анимаций по ключевым рамкам CSS, которые соответствуют этому узлу.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Запрашивает сведения о шрифтах платформы, которые мы использовали для отрисовки child TextNodes в заданном узле.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Возвращает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>fonts</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Статистика использования для каждого шрифта платформы.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Возвращает вычисленный стиль для узла DOM, заденуемого по `nodeId` .

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Возвращает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>computedStyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Вычисляемая стиль для указанного узла DOM.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### styleSheetAdded
Активна при добавлении активной таблицы стилей документов.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>Добавлены метаинфо таблицы стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetChanged
Собяно при смене таблицы стилей в результате операции клиента.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Активна при удалении активной таблицы стилей документов.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор удаленного таблицы стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Типы

### <a name="stylesheetid"></a> StyleSheetId `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

Коллекция правил CSS для одного псевдо стилей.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>pseudoType</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Псевдоэлементный тип.</td>
        </tr>
        <tr>
            <td>matches</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Соответствует правилам CSS, применимым к псевдо-стилю.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Наследуется коллекция правил CSS от узла-предка.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>необязательные</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Стиль узла-предка (если он есть) в цепочке наследования стилей.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Совпадения правил CSS, совпадающих с узлом предка в цепочке наследования стилей.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Данные совпадения для правила CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>rule</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>Правило CSS в совпадении.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Значение `object`

Данные для простого селектора (они отсортированы запятой в списке селекторов).

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст значения.</td>
        </tr>
        <tr>
            <td>range <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Диапазон значений в основном ресурсе (если он доступен).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> SelectorList `object`

Данные списка селектора.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>селекторы</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Селекторы в списке.</td>
        </tr>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст селектора правил.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

Представление правила CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</td>
        </tr>
        <tr>
            <td>selectorList <br /> <i>необязательные</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Данные селектора правил.</td>
        </tr>
        <tr>
            <td>origin <br /> <i>необязательные</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Происхождение родительской таблицы стилей.</td>
        </tr>
        <tr>
            <td>style</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Объявление связанного стиля.</td>
        </tr>
        <tr>
            <td>мультимедиа <br /> <i>необязательные</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Массив списков мультимедиа (для правил, включающих запросы мультимедиа). Массив инициирует запросы мультимедиа, начиная с внутреннего, с выходом из нее.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Диапазон текста в ресурсе. Все числа основаны на нулях.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Начальная строка диапазона.</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Столбец начала диапазона (включительно).</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>End line of range</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Конечный столбец диапазона (монопольный).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Короткое имя.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Краткое значение.</td>
        </tr>
        <tr>
            <td>important <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет ли свойство аннотацию "!important" `false` (подразумевает, если отсутствует).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Представление стиля CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>Свойства CSS в стиле.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Вычисленные значения для всех ярлыков, найденных в стиле.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Текст объявления стиля (если он доступен).</td>
        </tr>
        <tr>
            <td>range <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Диапазон объявлений стилей в заключаемой таблице стилей (если он доступен).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

Данные объявления свойств CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя свойства.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение свойства.</td>
        </tr>
        <tr>
            <td>important <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет ли свойство аннотацию "!important" `false` (подразумевает, если отсутствует).</td>
        </tr>
        <tr>
            <td>implicit <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Является ли свойство неявным `false` (подразумевает, если отсутствует).</td>
        </tr>
        <tr>
            <td>текст <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Полный текст свойства, указанный в стиле.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Будет ли свойство понято браузером `true` (подразумевает, если оно отсутствует).</td>
        </tr>
        <tr>
            <td>отключено <br /> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Отключено ли свойство пользователем (присутствует только для свойств на основе источника).</td>
        </tr>
        <tr>
            <td>range <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Весь диапазон свойств в объявлении стиля включаемого стиля (если он доступен).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

Дескриптор правила мультимедиа CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>source</td>
            <td><code class="flyout">string</code> <br /> <i>Допустимые значения: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Источник запроса мультимедиа: "mediaRule", если указано правилом @media, "importRule", если указано правилом @import, "linkedSheet", если он указан атрибутом "media" в теге LINK связанного таблицы стилей, "inlineSheet", если он указан атрибутом "media" в теге STYLE таблицы стилей.</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа, содержащего описание запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>range <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Связанный диапазон @media или @import правил в заключаемом таблице стилей (если он доступен).</td>
        </tr>
        <tr>
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей, содержащей этот объект (если он существует).</td>
        </tr>
        <tr>
            <td>mediaList <br /> <i>необязательные</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Массив запросов мультимедиа.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Дескриптор запроса мультимедиа.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>expressions</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Массив выражений запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Удовлетворяет ли условие запроса мультимедиа.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Дескриптор выражения запроса мультимедиа.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Значение выражения запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>unit</td>
            <td><code class="flyout">string</code></td>
            <td>Единицы выражения запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>функция</td>
            <td><code class="flyout">string</code></td>
            <td>Функция выражения запроса мультимедиа.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>необязательные</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Связанный диапазон текста значения в заключаемой таблице стилей (если он доступен).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>необязательные</i></td>
            <td><code class="flyout">number</code></td>
            <td>Вычисляемая длина выражения запроса мультимедиа (если применимо).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Сведения о количестве глифов, которые были отрисовыы с помощью заданного шрифта.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>familyName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя семейства шрифта, сообщаемая платформой.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Указывает, был ли шрифт загружен или разрешен локально.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Количество глифов, которые были отрисовыы с помощью этого шрифта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

Представление правила по ключевым рамкам CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>animationName</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Имя анимации.</td>
        </tr>
        <tr>
            <td>keyframes</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Список ключевых моментов.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

Представление правила по ключевым рамкам CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>необязательные</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей css (отсутствующий для таблицы стилей агента пользователя и заданных пользователем правил таблиц стилей) это правило поступило.</td>
        </tr>
        <tr>
            <td>origin</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Происхождение родительской таблицы стилей.</td>
        </tr>
        <tr>
            <td>keyText</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Связанный текст ключа.</td>
        </tr>
        <tr>
            <td>style</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Объявление связанного стиля.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя вычисленного свойства стиля.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение свойства computed style.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Метаинформация таблиц стилей CSS.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Идентификатор таблицы стилей.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес ресурса Stylesheet.</td>
        </tr>
        <tr>
            <td>отключено</td>
            <td><code class="flyout">boolean</code></td>
            <td>Обозначает, отключена ли таблица стилей.</td>
        </tr>
        <tr>
            <td>isInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Создается ли эта таблица стилей для тега STYLE с помощью разметки. Этот флаг не установлен для тегов DOCUMENT.written STYLE.</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">number</code></td>
            <td>Смещение строк таблицы стилей в ресурсе (на основе нуля).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">number</code></td>
            <td>Смещение столбцов таблицы стилей в ресурсе (на основе нуля).</td>
        </tr>
        <tr>
            <td>length</td>
            <td><code class="flyout">number</code></td>
            <td>Размер содержимого (в символах).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[DOM](dom.md)
