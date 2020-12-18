---
description: Используйте панель элементов для проверки HTML, CSS, DOM и доступности страницы.
title: DevTools — элементы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, элементы, html, css, точки останова dom, события, доступность
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235237"
---
# <span data-ttu-id="f5565-104">Элементы</span><span class="sxs-lookup"><span data-stu-id="f5565-104">Elements</span></span>

<span data-ttu-id="f5565-105">Панель **элементов** позволяет:</span><span class="sxs-lookup"><span data-stu-id="f5565-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="f5565-106">[Определение и редактирование элементов в дереве HTML](#html-tree-view) текущей страницы</span><span class="sxs-lookup"><span data-stu-id="f5565-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="f5565-107">[Проверка и изменение CSS](./elements/styles.md) на странице, включая псевдо-состояния и псевдоэлементы</span><span class="sxs-lookup"><span data-stu-id="f5565-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="f5565-108">[Понимание каскада стилей](./elements/computed.md) и макета CSS, происходящих на странице</span><span class="sxs-lookup"><span data-stu-id="f5565-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="f5565-109">[Отслеживание мошеннических обработчиков событий](./elements/events.md) для их отлаки</span><span class="sxs-lookup"><span data-stu-id="f5565-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="f5565-110">Установите точки останова отладки для [неожиданных визуальных изменений,](./elements/dom-breakpoints.md) чтобы перейти в код, вызывающий их</span><span class="sxs-lookup"><span data-stu-id="f5565-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="f5565-111">[Получите подробные сведения о шрифтах,](./elements/fonts.md) используемых на странице, и о том, откуда они загружаются</span><span class="sxs-lookup"><span data-stu-id="f5565-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="f5565-112">[Просмотр страницы с точки](./elements/accessibility.md) зрения чтения с экрана для проверки и проверки доступности</span><span class="sxs-lookup"><span data-stu-id="f5565-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="f5565-113">[Просмотр хода изменений CSS,](./elements/changes.md) которые вы внося при отлачивии пользовательского интерфейса страницы</span><span class="sxs-lookup"><span data-stu-id="f5565-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="f5565-114">Представление дерева HTML</span><span class="sxs-lookup"><span data-stu-id="f5565-114">HTML tree view</span></span>

![Панель элементов Microsoft Edge DevTools](./media/elements.png)

1. <span data-ttu-id="f5565-116">Используйте элемент **Select** () для поиска элемента в представлении дерева `Ctrl+B` **HTML,** щелкнув его на странице.</span><span class="sxs-lookup"><span data-stu-id="f5565-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="f5565-117">Используйте средство **выделения элементов** () для поиска элемента на странице путем наведении на него курсор в `Ctrl+Shift+L` **представлении дерева HTML.**</span><span class="sxs-lookup"><span data-stu-id="f5565-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="f5565-118">Откройте средство **"Выбор цвета"** (), чтобы увидеть список цветов, `Ctrl+K` которые используются на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="f5565-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="f5565-119">Щелчок цвета в списке предоставит дополнительные сведения (hue, Saturation, Lightness, Alpha).</span><span class="sxs-lookup"><span data-stu-id="f5565-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="f5565-120">Элемент *управления "Выбор* цвета" также открывается при нажатии \*\*\*\* цветного квадрата рядом со значением цвета в области стилей, что позволяет изменить цвет элемента страницы и сразу же увидеть результаты.</span><span class="sxs-lookup"><span data-stu-id="f5565-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="f5565-121">Кнопка **"Дерево** доступности" () откроет дерево доступности, в котором показана структура страницы, как это может показаться специальным технологиям, таким как экранный диктор `Ctrl+Shift+A` [Windows.](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) [](./elements/accessibility.md)</span><span class="sxs-lookup"><span data-stu-id="f5565-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="f5565-122">Вы также можете **найти** () элемент в представлении дерева HTML, выполнив поиск его имени `Ctrl+F` тега, атрибутов или текстового содержимого.</span><span class="sxs-lookup"><span data-stu-id="f5565-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="f5565-123">Элементы редактирования</span><span class="sxs-lookup"><span data-stu-id="f5565-123">Editing elements</span></span>

<span data-ttu-id="f5565-124">Вы можете изменить элемент, щелкнув его правой кнопкой мыши в представлении дерева HTML и выбрав "Изменить как **HTML"** в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f5565-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="f5565-125">Контекстное меню также предоставляет параметры для удаления, вырезания, копирования, вики- и настройки псевдо-классов CSS (*:active,* *:focus,* *:hover*, *:visited)* и добавления атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f5565-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="f5565-126">Другой способ изменить атрибут и(или) его значение — дважды щелкнуть его в представлении дерева HTML.</span><span class="sxs-lookup"><span data-stu-id="f5565-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Контекстное меню представления дерева HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="f5565-128">Редактирование дерева HTML не влияет на базовую разметку источника.</span><span class="sxs-lookup"><span data-stu-id="f5565-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="f5565-129">Обновление страницы позволит отостановить изменения и отрисовки только макета, определяемой источником страницы.</span><span class="sxs-lookup"><span data-stu-id="f5565-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="f5565-130">Вы можете **скопировать** измененный HTML-код в буфер обмена, щелкнув правой кнопкой мыши нужный элемент (или глобальный элемент, если требуется вся страница), чтобы открыть `html` контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="f5565-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="f5565-131">(**Также** доступны **параметры вырезания** и в paste.</span><span class="sxs-lookup"><span data-stu-id="f5565-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="f5565-132">В области [стилей](./elements/styles.md) можно также добавлять, удалять и редактировать псевдо-состояния CSS и псевдоэлементы.</span><span class="sxs-lookup"><span data-stu-id="f5565-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="f5565-133">Области инструментов</span><span class="sxs-lookup"><span data-stu-id="f5565-133">Tool Panes</span></span>

<span data-ttu-id="f5565-134">Выбрав интересующие вас элементы страницы, вы можете использовать области инструментов для дальнейшего просмотра его различных стилей и свойств доступности, просмотра прослушивателей событий и назначения точек останова изменения doM.</span><span class="sxs-lookup"><span data-stu-id="f5565-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Области инструментов на панели элементов](./media/elements_toolpanes.png)

1. <span data-ttu-id="f5565-136">[**Стили**](./elements/styles.md): в настоящее время примененные стили, уорганизованные в таблицу стилей</span><span class="sxs-lookup"><span data-stu-id="f5565-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="f5565-137">[**Computed**](./elements/computed.md): в настоящее время примененные стили, у организованы по атрибутам CSS</span><span class="sxs-lookup"><span data-stu-id="f5565-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="f5565-138">[**События:**](./elements/events.md)прослушиватели событий, зарегистрированные в текущем элементе и предках</span><span class="sxs-lookup"><span data-stu-id="f5565-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="f5565-139">[**Точки останова DOM:**](./elements/dom-breakpoints.md)точки останова при снобизме doM</span><span class="sxs-lookup"><span data-stu-id="f5565-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="f5565-140">[**Fonts**](./elements/fonts.md): currently applied fonts for a selected element</span><span class="sxs-lookup"><span data-stu-id="f5565-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="f5565-141">[**Accessibility**](./elements/accessibility.md): Accessibility properties</span><span class="sxs-lookup"><span data-stu-id="f5565-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="f5565-142">[**Изменения:**](./elements/changes.md)изменения CSS, внесенные во время сеанса диагностики</span><span class="sxs-lookup"><span data-stu-id="f5565-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="f5565-143">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="f5565-143">Shortcuts</span></span>

| <span data-ttu-id="f5565-144">Действие</span><span class="sxs-lookup"><span data-stu-id="f5565-144">Action</span></span>               | <span data-ttu-id="f5565-145">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="f5565-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="f5565-146">Панель элементов</span><span class="sxs-lookup"><span data-stu-id="f5565-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="f5565-147">Выделение элементов</span><span class="sxs-lookup"><span data-stu-id="f5565-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="f5565-148">Элемент Select</span><span class="sxs-lookup"><span data-stu-id="f5565-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="f5565-149">Палитра</span><span class="sxs-lookup"><span data-stu-id="f5565-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="f5565-150">Дерево доступности</span><span class="sxs-lookup"><span data-stu-id="f5565-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
