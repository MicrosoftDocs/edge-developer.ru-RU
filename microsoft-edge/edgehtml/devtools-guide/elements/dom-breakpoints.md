---
description: Использование точек останова DOM для визуальной отлажений макета на странице
title: DevTools — элементы — точки останова DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, элементы, точки останова dom, dom
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb60fa0497c98c152ca2c5adf28e9dee5d7c9f98
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235402"
---
# <span data-ttu-id="b2fdb-104">Точки останова DOM</span><span class="sxs-lookup"><span data-stu-id="b2fdb-104">DOM breakpoints</span></span>

<span data-ttu-id="b2fdb-105">Управляйте точками останова изменения doM на этой области, включая их отключение, удаление и переназначение.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-105">Manage your DOM mutation breakpoints from this pane, including disabling, deleting and rebinding them.</span></span>

<span data-ttu-id="b2fdb-106">Вы можете использовать точки останова модификации DOM, чтобы вламывать отладить каждый раз, когда изменяется выбранный узел элемента.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-106">You can use DOM mutation breakpoints to break into the debugger whenever a selected element node changes.</span></span> <span data-ttu-id="b2fdb-107">Это полезно для отслеживания кода, который вызывает визуальные сбои в пользовательском интерфейсе без необходимости устанавливать отдельные точки останова для каждого API DOM 450+ в *EdgeHTML,* которые могут вызывать такие изменения.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-107">This is helpful for tracking down the code responsible for causing visual glitches with your UI without having to set individual breakpoints on each of the 450+ DOM APIs in *EdgeHTML* that can trigger such changes.</span></span> 

<span data-ttu-id="b2fdb-108">Чтобы установить точку останова DOM, щелкните \*\*\*\* правой кнопкой мыши любой элемент в *HTML-представлении HTML* панели элементов, чтобы открыть контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-108">To set a DOM breakpoint, right-click on any element in the **Elements** panel *HTML tree view* to open the context menu.</span></span>

![Контекстное меню "Точки останова DOM"](../media/elements_dom_breakpoints_contextmenu.png)

<span data-ttu-id="b2fdb-110">Можно установить любую из следующих точек останова:</span><span class="sxs-lookup"><span data-stu-id="b2fdb-110">You can set any of the following breakpoints:</span></span>

 - <span data-ttu-id="b2fdb-111">**Break on Node removed**: Break into the debugger when the selected element is removed from the document (DOM tree).</span><span class="sxs-lookup"><span data-stu-id="b2fdb-111">**Break on Node removed**: Break into the debugger when the selected element is removed from the document (DOM tree).</span></span>

 - <span data-ttu-id="b2fdb-112">**Break on Subtree modified**: Break into the debugger when any of the descendants of the selected element are changed (added, removed, or their subtrees are modified).</span><span class="sxs-lookup"><span data-stu-id="b2fdb-112">**Break on Subtree modified**: Break into the debugger when any of the descendants of the selected element are changed (added, removed, or their subtrees are modified).</span></span> <span data-ttu-id="b2fdb-113">Это не будет нарушать при изменениях атрибутов (см. следующий вариант).</span><span class="sxs-lookup"><span data-stu-id="b2fdb-113">This will not break when attributes are modified (see the next option for that).</span></span>

 - <span data-ttu-id="b2fdb-114">**Break on Attribute modified**: Break into the debugger when an attribute of the selected element is added, removed or changed in value.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-114">**Break on Attribute modified**: Break into the debugger when an attribute of the selected element is added, removed or changed in value.</span></span>

<span data-ttu-id="b2fdb-115">Затем в области "точки останова **DOM"** отображится выбранный элемент (путем создания селектора, описывающий его расположение в DOM) и типы установленных точек останова (узел*удален, подtree изменен,* изменен атрибут).</span><span class="sxs-lookup"><span data-stu-id="b2fdb-115">The **DOM breakpoints** pane will then list the selected element (by generating a selector describing its location in the DOM) and the types of breakpoints you have set (*Node removed, Subtree modified, Attribute modified*).</span></span> <span data-ttu-id="b2fdb-116">Здесь вы также можете переназначать, \*\* отключать или удалять точки останова по отдельности (из контекстного меню rt-click) или одновременно (с помощью кнопок). \*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="b2fdb-116">From here, you can also *rebind*, *disable*, or *delete* your breakpoints, individually (from the rt-click context menu) or all at once (using the buttons).</span></span>

![DoM breakpoints pane](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="b2fdb-118">Сохраняемость точки останова</span><span class="sxs-lookup"><span data-stu-id="b2fdb-118">Breakpoint persistence</span></span>

<span data-ttu-id="b2fdb-119">Точки останова хранятся (и устанавливаются на уровне URL-адреса страницы, в пределах каждой из них) как часть параметров DevTools.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-119">Breakpoints are stored (and scoped to the URL of the page they're set within) as part of your DevTools settings.</span></span> <span data-ttu-id="b2fdb-120">Когда страница будет перезагружена или инструменты будут закрыты и повторно открыты, DevTools попытается перенагрузить точки останова для связанных с ними элементов.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-120">When the page is reloaded or the tools are closed and reopened, DevTools will attempt to rebind your breakpoints to their associated elements.</span></span>

<span data-ttu-id="b2fdb-121">Точки останова, которые не могут быть автоматически переназначаемы, обозначены значком предупреждения в круге точки останова.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-121">Breakpoints that couldn't be automatically rebinded are indicated with a warning icon on the breakpoint circle.</span></span> <span data-ttu-id="b2fdb-122">Для этого можно дождаться переназначаемого элемента вручную (с помощью кнопки «Rebind **breakpoint»** или параметра контекстного меню), когда соответствующий элемент \*\*\*\* появится в DOM (а значок точки останова больше не отображает индикатор предупреждения) или полностью удалит точку останова.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-122">For these, you can wait to rebind the element manually (using the **Rebind breakpoint** button and/or context menu option) once a corresponding element appears in the DOM (and the breakpoint icon no longer shows the warning indicator), or **Delete** the breakpoint altogether.</span></span>

![Индикатор точки останова без точки останова](../media/elements_dom_breakpoint_unbound.png)

<span data-ttu-id="b2fdb-124">Помимо этой области точек останова *DOM,* вы также можете управлять точками останова [DOM](../debugger.md#dom-breakpoints) в **отладке.**</span><span class="sxs-lookup"><span data-stu-id="b2fdb-124">In addition to this *DOM breakpoints* pane, you can also manage your [DOM breakpoints](../debugger.md#dom-breakpoints) from within the **Debugger**.</span></span>

## <span data-ttu-id="b2fdb-125">Текущие ограничения</span><span class="sxs-lookup"><span data-stu-id="b2fdb-125">Current limitations</span></span>

<span data-ttu-id="b2fdb-126">Помните о следующих ограничениях отладки точек останова DOM в Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="b2fdb-126">Please be aware of the following limitations of DOM breakpoint debugging in Edge DevTools:</span></span>

- <span data-ttu-id="b2fdb-127">Edge DevTools в настоящее время не поддерживает повторное переназначение точек останова внутри [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span><span class="sxs-lookup"><span data-stu-id="b2fdb-127">Edge DevTools don't currently support rebinding breakpoints inside of [`<iframe>`s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span></span> <span data-ttu-id="b2fdb-128">Если установить точку останова в iframe и закрыть Edge DevTools или обновить страницу, точка останова будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-128">If you set a breakpoint in an iframe and close Edge DevTools or refresh the page, the breakpoint will be lost.</span></span>

- <span data-ttu-id="b2fdb-129">Если ваш сценарий сталкивается с синхронно выполненной точкой останова перед выполнением DOM, вы не сможете установить точку останова DOM, пока отладка [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) приостановлена.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-129">If your script encounters a synchronously-executed breakpoint before the DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) is completed, you won't be able to set a DOM breakpoint while the debugger is paused.</span></span> <span data-ttu-id="b2fdb-130">Как правило, эту ситуацию можно исправить, установив [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) атрибуты [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) или скрипт.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-130">You can typically remedy this situation by setting the [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) or [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) script attributes.</span></span>

- <span data-ttu-id="b2fdb-131">Для синхронных сценариев при вызывается автоматическое переназначение точек [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) останова.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-131">For synchronous scripts, we trigger automatic rebinding of breakpoints when the [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) event is called.</span></span> <span data-ttu-id="b2fdb-132">В этом случае мы можем пропустить точки останова привязки, которые будут запускаться при первоначальном создании DOM на основе скриптов.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-132">In this case, we may miss binding breakpoints that would trigger during initial script-driven build-up of the DOM.</span></span> <span data-ttu-id="b2fdb-133">Для асинхронных сценариев мы запускаем попытку переназначаем перед выполнением первого сценария, поэтому точки останова могут быть переназначены и активизированы по мере желаний.</span><span class="sxs-lookup"><span data-stu-id="b2fdb-133">For asynchronous scripts, we trigger a rebind attempt before the first script executes, so your breakpoints may rebind and trigger as desired.</span></span>
