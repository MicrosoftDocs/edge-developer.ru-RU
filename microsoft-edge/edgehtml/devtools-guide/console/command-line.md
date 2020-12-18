---
description: Использование командной строки консоли для взаимодействия с запущенной страницей
title: DevTools — консоль — командная строка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, командная строка консоли
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d7ea2bef9fa0014e4d61745636a06d508565df91
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235380"
---
# <span data-ttu-id="e2fa5-104">Командная строка консоли</span><span class="sxs-lookup"><span data-stu-id="e2fa5-104">Console command line</span></span>

<span data-ttu-id="e2fa5-105">Используйте командную строку консоли для просмотра [*и изменения*](/visualstudio/ide/javascript-intellisense) значений на странице и выполнения кода отлаки во время выполнения, при этом используйте преимущества Visual Studio IntelliSense автоматического выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="e2fa5-106">Просто введите любой допустимый JavaScript в командной строке и нажмите `Enter` для выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="e2fa5-107">Для многостроального ввода используйте `Shift+Enter` для добавления разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="e2fa5-108">Используйте клавиши со стрелками для навигации по предыдущим командам консоли, которые вы ввели во время текущего `Up` `Down` сеанса DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="e2fa5-109">Помимо стандартного JavaScript и [консольного API](./console-api.md)консоль также поддерживает следующие команды:</span><span class="sxs-lookup"><span data-stu-id="e2fa5-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="e2fa5-110">Выбор объектов DOM</span><span class="sxs-lookup"><span data-stu-id="e2fa5-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="e2fa5-111">Проверка свойств объекта</span><span class="sxs-lookup"><span data-stu-id="e2fa5-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="e2fa5-112">Поиск всех прослушивателей событий для заданного объекта</span><span class="sxs-lookup"><span data-stu-id="e2fa5-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="e2fa5-113">Сценарий, введенный в командной строке, выполняется в глобальной области выбранного в данный момент окна, если страница не приостановлена в точке останова. [](/scripting/javascript/advanced/variable-scope-javascript)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="e2fa5-114">Команды консоли, которые введены во время приостановки страницы, будут выполняться в локальной области текущей функции в стеке вызовов. [](/scripting/javascript/advanced/variable-scope-javascript)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="e2fa5-115">Над областью \*\*\*\* вывода консоли имеется контекст целевого выполнения.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="e2fa5-116">Выбором по умолчанию является документ верхнего уровня, **_top.**</span><span class="sxs-lookup"><span data-stu-id="e2fa5-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="e2fa5-117">Любые iframes в документе или запущенных расширениях также отображаются в качестве параметров, что позволяет поочередно запускать команды в этих области.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="e2fa5-118">Селекторы DOM</span><span class="sxs-lookup"><span data-stu-id="e2fa5-118">DOM selectors</span></span>
<span data-ttu-id="e2fa5-119">Эти селекторы консоли предоставляют простые ярлыки для быстрого доступа к объектам в DOM:</span><span class="sxs-lookup"><span data-stu-id="e2fa5-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="e2fa5-120">$(*Строка селектора CSS)*</span><span class="sxs-lookup"><span data-stu-id="e2fa5-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="e2fa5-121">Возвращает первый элемент в документе, соответствующий указанной строке [селектора CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (или разделенной запятой группой селекторов).</span><span class="sxs-lookup"><span data-stu-id="e2fa5-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="e2fa5-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="e2fa5-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="e2fa5-123">Пример. Откройте консоль и введите, чтобы вернуть объект div на `$('#main')` `id='main'` этой странице.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Пример использования селектора $](../media/console_cmd_$.png)

### <span data-ttu-id="e2fa5-125">$$(*строка селектора CSS)*</span><span class="sxs-lookup"><span data-stu-id="e2fa5-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="e2fa5-126">Возвращает массив элементов в документе, соответствующий указанной строке [селектора CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (или разделенной запятой группой селекторов).</span><span class="sxs-lookup"><span data-stu-id="e2fa5-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="e2fa5-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="e2fa5-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="e2fa5-128">Пример. Откройте консоль и введите, чтобы вернуть все объекты div на `$$('.container')` `class='container'` этой странице.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Пример использования селектора $$](../media/console_cmd_$$.png)

### <span data-ttu-id="e2fa5-130">0, 1, 2 ,...</span><span class="sxs-lookup"><span data-stu-id="e2fa5-130">$0, $1, $2,...</span></span>
<span data-ttu-id="e2fa5-131">Возвращает последние элементы, выбранные [\*\*\*\*](../elements.md) на панели элементов, где представляет текущий выбранный элемент, был выбранным элементом до этого и так `$0` `$1` далее.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="e2fa5-132">Пример. Откройте DevTools \*\*\*\* на вкладке "Элементы", нажмите, чтобы активировать элемент Select, и щелкните мышью некоторые области на `CTRL + B` этой странице. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e2fa5-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="e2fa5-133">Теперь откройте консоль и `$0` введите, чтобы вернуть элемент, который вы только что нажали.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Пример использования селектора "$0"](../media/console_cmd_$0.png)

### <span data-ttu-id="e2fa5-135">$x( выражение*XPath)*</span><span class="sxs-lookup"><span data-stu-id="e2fa5-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="e2fa5-136">Возвращает массив элементов, совпав с указанным выражением [XPath.](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="e2fa5-137">Пример. Откройте консоль и введите, чтобы вернуть все элементы на этой странице, содержащие `$x('//script[@defer]')` `<script>` `defer` атрибут.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Пример использования селектора "$x"](../media/console_cmd_$x.png)

## <span data-ttu-id="e2fa5-139">Проверка объектов</span><span class="sxs-lookup"><span data-stu-id="e2fa5-139">Object inspection</span></span>

<span data-ttu-id="e2fa5-140">Эти команды предоставляют быстрые способы проверки свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="e2fa5-141">Указанный объект должен быть определен либо в глобальном пространстве имен, либо в текущей области отладки.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="e2fa5-142">dir(*object*)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-142">dir(*object*)</span></span>
<span data-ttu-id="e2fa5-143">Возвращает список свойств древового представления для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="e2fa5-144">Пример. Откройте консоль и введите, чтобы увидеть свойства объекта `dir(document)` документа, представляющего эту страницу.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Пример использования метода dir](../media/console_cmd_dir.png)

### <span data-ttu-id="e2fa5-146">keys(*object*)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-146">keys(*object*)</span></span>
<span data-ttu-id="e2fa5-147">Возвращает массив имен свойств, прикрепленных к указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="e2fa5-148">Пример. Откройте консоль и введите, чтобы вернуть все свойства, `keys(window)` определенные в объекте глобального окна.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Пример использования метода "keys"](../media/console_cmd_keys.png)

### <span data-ttu-id="e2fa5-150">*values(object*)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-150">values(*object*)</span></span>
<span data-ttu-id="e2fa5-151">Возвращает массив значений свойств, прикрепленных к указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="e2fa5-152">Пример. Откройте консоль и введите, чтобы вернуть значения всех свойств `values(window)` (ключей), определенных в объекте глобального окна.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Пример использования метода values](../media/console_cmd_values.png)

## <span data-ttu-id="e2fa5-154">Прослушиватели событий</span><span class="sxs-lookup"><span data-stu-id="e2fa5-154">Event listeners</span></span>

<span data-ttu-id="e2fa5-155">Эта команда позволяет проверить прослушиватели событий, зарегистрированные в заданном объекте.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="e2fa5-156">Указанный объект должен быть определен либо в глобальном пространстве имен, либо в текущей области отладки.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="e2fa5-157">getEventListeners(*object*)</span><span class="sxs-lookup"><span data-stu-id="e2fa5-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="e2fa5-158">Возвращает объект, содержащий ключ для каждого зарегистрированного типа события в заданный объект.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="e2fa5-159">Значение каждого ключа — это массив прослушивателей событий и связанных с ними данных.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="e2fa5-160">Пример. Откройте консоль и введите, чтобы увидеть все прослушиватели событий, зарегистрированные в `getEventListeners(document)` объекте документа этой страницы.</span><span class="sxs-lookup"><span data-stu-id="e2fa5-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Пример использования метода getEventListeners](../media/console_cmd_getEventListeners.png)
