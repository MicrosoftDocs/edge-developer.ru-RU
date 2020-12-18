---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена отладки. Домен отладки предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.
title: Домен отлада — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5160e6e69ec76f8c584f1bdb969464d805c7afa7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235578"
---
# <span data-ttu-id="7daab-105">Домен отлада — протокол DevTools версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="7daab-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="7daab-106">Домен отлада предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="7daab-107">Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="7daab-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="7daab-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7daab-108">Methods</span></span>**](#methods) | <span data-ttu-id="7daab-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="7daab-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="7daab-110">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="7daab-110">Events</span></span>**](#events) | <span data-ttu-id="7daab-111">[scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [приостановлено,](#paused) [возобновлено](#resumed)</span><span class="sxs-lookup"><span data-stu-id="7daab-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="7daab-112">Типы</span><span class="sxs-lookup"><span data-stu-id="7daab-112">Types</span></span>**](#types) | <span data-ttu-id="7daab-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="7daab-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="7daab-114">Зависимости</span><span class="sxs-lookup"><span data-stu-id="7daab-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="7daab-115">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="7daab-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="7daab-116">Методы</span><span class="sxs-lookup"><span data-stu-id="7daab-116">Methods</span></span>

### <span data-ttu-id="7daab-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="7daab-117">enable</span></span>
<span data-ttu-id="7daab-118">Включает отладок для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="7daab-118">Enables debugger for the given page.</span></span> <span data-ttu-id="7daab-119">Клиенты не должны предполагать, что отладка включена, пока не будет получен результат для этой команды.</span><span class="sxs-lookup"><span data-stu-id="7daab-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>


---

### <span data-ttu-id="7daab-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="7daab-120">disable</span></span>
<span data-ttu-id="7daab-121">Отключает отладок для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="7daab-121">Disables debugger for given page.</span></span>


---

### <span data-ttu-id="7daab-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="7daab-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="7daab-123">Возвращает возможные расположения для точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="7daab-124">ScriptId в расположениях в начале и конце диапазона должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="7daab-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-126">start</span><span class="sxs-lookup"><span data-stu-id="7daab-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-127">Начало диапазона для поиска возможных местоположений точек останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-128">завершить</span><span class="sxs-lookup"><span data-stu-id="7daab-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-129">Конец диапазона для поиска возможных местоположений точек останова в (за исключением).</span><span class="sxs-lookup"><span data-stu-id="7daab-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="7daab-130">Если он не указан, конец диапазона используется для окончания сценариев.</span><span class="sxs-lookup"><span data-stu-id="7daab-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-131">Возвращает</span><span class="sxs-lookup"><span data-stu-id="7daab-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-132">locations</span><span class="sxs-lookup"><span data-stu-id="7daab-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="7daab-133">Список возможных местоположений точек останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="7daab-134">setBreakpointsActive</span></span>
<span data-ttu-id="7daab-135">Активирует или деактивирует все точки останова на странице.</span><span class="sxs-lookup"><span data-stu-id="7daab-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-137">active</span><span class="sxs-lookup"><span data-stu-id="7daab-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="7daab-138">Новое значение активного состояния точек останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="7daab-139">setBreakpointByUrl</span></span>
<span data-ttu-id="7daab-140">Задает точку останова JavaScript в указанном расположении, указанном с помощью URL-адреса или regex URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7daab-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="7daab-141">После того как эта команда будет выдана, все существующие сценарии будут иметь точки останова, разрешенные и возвращенные в <code>locations</code> свойстве.</span><span class="sxs-lookup"><span data-stu-id="7daab-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="7daab-142">Дальнейшее соответствие сценариев приведет к последующим <code>breakpointResolved</code> событиям.</span><span class="sxs-lookup"><span data-stu-id="7daab-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="7daab-143">Эта логическая точка останова будет выдержать перезагрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="7daab-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-144">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-146">Номер строки для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-147">url</span><span class="sxs-lookup"><span data-stu-id="7daab-147">url</span></span> <br/> <i><span data-ttu-id="7daab-148">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-149">URL-адрес ресурсов для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="7daab-150">urlRegex</span></span> <br/> <i><span data-ttu-id="7daab-151">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-152">Шаблон Regex для URL-адресов ресурсов, в которые необходимо установить точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="7daab-153">Либо <code>url</code> должно <code>urlRegex</code> быть указано, либо должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="7daab-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-154">columnNumber</span></span> <br/> <i><span data-ttu-id="7daab-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-156">Смещение в строке для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-157">condition</span><span class="sxs-lookup"><span data-stu-id="7daab-157">condition</span></span> <br/> <i><span data-ttu-id="7daab-158">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-159">Выражение, используемое в качестве условия точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="7daab-160">Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</span><span class="sxs-lookup"><span data-stu-id="7daab-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-161">Возвращает</span><span class="sxs-lookup"><span data-stu-id="7daab-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="7daab-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="7daab-163">ИД созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="7daab-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-164">locations</span><span class="sxs-lookup"><span data-stu-id="7daab-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="7daab-165">Список местоположений, в которые эта точка останова была разрешена после добавления.</span><span class="sxs-lookup"><span data-stu-id="7daab-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="7daab-166">setBreakpoint</span></span>
<span data-ttu-id="7daab-167">Задает точку останова JavaScript в заданное расположение.</span><span class="sxs-lookup"><span data-stu-id="7daab-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-168">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-169">location</span><span class="sxs-lookup"><span data-stu-id="7daab-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-170">Расположение для определения точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-171">condition</span><span class="sxs-lookup"><span data-stu-id="7daab-171">condition</span></span> <br/> <i><span data-ttu-id="7daab-172">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-173">Выражение, используемое в качестве условия точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="7daab-174">Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</span><span class="sxs-lookup"><span data-stu-id="7daab-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-175">Возвращает</span><span class="sxs-lookup"><span data-stu-id="7daab-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="7daab-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="7daab-177">ИД созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="7daab-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="7daab-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-179">Расположение, в который разрешена точка останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="7daab-180">removeBreakpoint</span></span>
<span data-ttu-id="7daab-181">Удаляет точку останова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-182">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="7daab-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="7daab-184">stepOver</span></span>
<span data-ttu-id="7daab-185">По шагам над заявлением.</span><span class="sxs-lookup"><span data-stu-id="7daab-185">Steps over the statement.</span></span>


---

### <span data-ttu-id="7daab-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="7daab-186">stepInto</span></span>
<span data-ttu-id="7daab-187">Этапы вызова функции.</span><span class="sxs-lookup"><span data-stu-id="7daab-187">Steps into the function call.</span></span>


---

### <span data-ttu-id="7daab-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="7daab-188">stepOut</span></span>
<span data-ttu-id="7daab-189">По шагам из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="7daab-189">Steps out of the function call.</span></span>


---

### <span data-ttu-id="7daab-190">pause</span><span class="sxs-lookup"><span data-stu-id="7daab-190">pause</span></span>
<span data-ttu-id="7daab-191">Останавливает следующий отчет JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-191">Stops on the next JavaScript statement.</span></span>


---

### <span data-ttu-id="7daab-192">resume</span><span class="sxs-lookup"><span data-stu-id="7daab-192">resume</span></span>
<span data-ttu-id="7daab-193">Возобновляет выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-193">Resumes JavaScript execution.</span></span>


---

### <span data-ttu-id="7daab-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="7daab-194">getScriptSource</span></span>
<span data-ttu-id="7daab-195">Возвращает источник для сценария с заданным идом.</span><span class="sxs-lookup"><span data-stu-id="7daab-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="7daab-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="7daab-198">ИД скрипта, для который требуется получить источник.</span><span class="sxs-lookup"><span data-stu-id="7daab-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-199">Возвращает</span><span class="sxs-lookup"><span data-stu-id="7daab-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="7daab-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-201">Источник скрипта.</span><span class="sxs-lookup"><span data-stu-id="7daab-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="7daab-202">setPauseOnExceptions</span></span>
<span data-ttu-id="7daab-203">Определяет паузу в состоянии исключений.</span><span class="sxs-lookup"><span data-stu-id="7daab-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="7daab-204">Можно установить остановку для всех исключений, невысченных исключений или без исключений.</span><span class="sxs-lookup"><span data-stu-id="7daab-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="7daab-205">Начальная пауза в состоянии исключений <code>none</code> — .</span><span class="sxs-lookup"><span data-stu-id="7daab-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-207">state</span><span class="sxs-lookup"><span data-stu-id="7daab-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="7daab-208">Допустимые значения: none, uncaught, all</span><span class="sxs-lookup"><span data-stu-id="7daab-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="7daab-209">Приостановка в режиме исключений.</span><span class="sxs-lookup"><span data-stu-id="7daab-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="7daab-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="7daab-211">Оценивает выражение в заданной рамке вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-212">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="7daab-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="7daab-214">Идентификатор кадра вызова для оценки.</span><span class="sxs-lookup"><span data-stu-id="7daab-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-215">выражение</span><span class="sxs-lookup"><span data-stu-id="7daab-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-216">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="7daab-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-217">Возвращает</span><span class="sxs-lookup"><span data-stu-id="7daab-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-218">result</span><span class="sxs-lookup"><span data-stu-id="7daab-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="7daab-219">Оболочка объекта для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="7daab-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="7daab-220">setVariableValue</span></span>
<span data-ttu-id="7daab-221">Изменяет значение переменной в callframe.</span><span class="sxs-lookup"><span data-stu-id="7daab-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="7daab-222">Области на основе объектов не поддерживаются и должны быть мутированы вручную.</span><span class="sxs-lookup"><span data-stu-id="7daab-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-223">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-225">Число областей на основе 0, указанных в цепочке областей.</span><span class="sxs-lookup"><span data-stu-id="7daab-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="7daab-226">Разрешены только типы областей "local", "closure" и "catch".</span><span class="sxs-lookup"><span data-stu-id="7daab-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="7daab-227">Другие области могут управляться вручную.</span><span class="sxs-lookup"><span data-stu-id="7daab-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-228">variableName</span><span class="sxs-lookup"><span data-stu-id="7daab-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-229">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="7daab-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-230">newValue</span><span class="sxs-lookup"><span data-stu-id="7daab-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="7daab-231">Новое значение переменной.</span><span class="sxs-lookup"><span data-stu-id="7daab-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="7daab-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="7daab-233">ИД callframe, который содержит переменную.</span><span class="sxs-lookup"><span data-stu-id="7daab-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="7daab-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="7daab-235">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-235">Experimental.</span></span> </b></span><span data-ttu-id="7daab-236">Замените предыдущие шаблоны черных ящиков на переданные.</span><span class="sxs-lookup"><span data-stu-id="7daab-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="7daab-237">Заставляет тыловые части пропускать пошаговую или прио паузу в скриптах, url-адресом, совпадающих с одним из шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7daab-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="7daab-238">Отладик попытается выйти из сценария из черной почты, выполив "шаг" несколько раз, и, наконец, при неудачном выполнении прибег к шагу "выйти".</span><span class="sxs-lookup"><span data-stu-id="7daab-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-240">patterns</span><span class="sxs-lookup"><span data-stu-id="7daab-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="7daab-241">Массив regexps, который будет использоваться для проверки URL-адреса скрипта на состояние черного ящика.</span><span class="sxs-lookup"><span data-stu-id="7daab-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="7daab-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="7daab-243">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-243">Experimental.</span></span> </b></span><span data-ttu-id="7daab-244">Корпорация Майкрософт: задает указанное значение для указанного свойства отладки.</span><span class="sxs-lookup"><span data-stu-id="7daab-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="7daab-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-247">Майкрософт: ид свойства (например, msDebuggerPropertyId), который необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="7daab-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-248">newValue</span><span class="sxs-lookup"><span data-stu-id="7daab-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="7daab-249">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="7daab-249">Events</span></span>

### <span data-ttu-id="7daab-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="7daab-250">scriptParsed</span></span>
<span data-ttu-id="7daab-251">Срасть при разчете сценария.</span><span class="sxs-lookup"><span data-stu-id="7daab-251">Fired when the script is parsed.</span></span> <span data-ttu-id="7daab-252">Это событие также иллюбуется для всех известных и несмеченных сценариев при включии отладка.</span><span class="sxs-lookup"><span data-stu-id="7daab-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-253">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="7daab-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="7daab-255">Идентификатор разлияемого скрипта.</span><span class="sxs-lookup"><span data-stu-id="7daab-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-256">url</span><span class="sxs-lookup"><span data-stu-id="7daab-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-257">URL-адрес или имя разбияемого сценария (если таково).</span><span class="sxs-lookup"><span data-stu-id="7daab-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-258">startLine</span><span class="sxs-lookup"><span data-stu-id="7daab-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-259">Смещение строк скрипта в ресурсе с заданным URL-адресом (для тегов скрипта).</span><span class="sxs-lookup"><span data-stu-id="7daab-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="7daab-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-261">Смещение столбцов сценария в ресурсе с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="7daab-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-262">endLine</span><span class="sxs-lookup"><span data-stu-id="7daab-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-263">Последняя строка сценария.</span><span class="sxs-lookup"><span data-stu-id="7daab-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-264">endColumn</span><span class="sxs-lookup"><span data-stu-id="7daab-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-265">Длина последней строки сценария.</span><span class="sxs-lookup"><span data-stu-id="7daab-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="7daab-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="7daab-267">Указывает контекст создания скрипта.</span><span class="sxs-lookup"><span data-stu-id="7daab-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="7daab-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="7daab-269">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-270">URL-адрес карты источника, связанной со сценарием (если таково).</span><span class="sxs-lookup"><span data-stu-id="7daab-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-271">length</span><span class="sxs-lookup"><span data-stu-id="7daab-271">length</span></span> <br/> <i><span data-ttu-id="7daab-272">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="7daab-273">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-273">Experimental.</span></span> </b></span><span data-ttu-id="7daab-274">Длина этого скрипта.</span><span class="sxs-lookup"><span data-stu-id="7daab-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="7daab-275">msParentId</span></span> <br/> <i><span data-ttu-id="7daab-276">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="7daab-277">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-277">Experimental.</span></span> </b></span><span data-ttu-id="7daab-278">Это родительский ИД документа.</span><span class="sxs-lookup"><span data-stu-id="7daab-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="7daab-279">msMimeType</span></span> <br/> <i><span data-ttu-id="7daab-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="7daab-281">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-281">Experimental.</span></span> </b></span><span data-ttu-id="7daab-282">Это тип MIME.</span><span class="sxs-lookup"><span data-stu-id="7daab-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="7daab-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="7daab-284">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="7daab-285">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-285">Experimental.</span></span> </b></span><span data-ttu-id="7daab-286">Это указывает, является ли это динамическим кодом.</span><span class="sxs-lookup"><span data-stu-id="7daab-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="7daab-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="7daab-288">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="7daab-289">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-289">Experimental.</span></span> </b></span><span data-ttu-id="7daab-290">Это длинный ИД документа.</span><span class="sxs-lookup"><span data-stu-id="7daab-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="7daab-291">breakpointResolved</span></span>
<span data-ttu-id="7daab-292">Происходит, когда точка останова разрешена к фактическому сценарию и расположению.</span><span class="sxs-lookup"><span data-stu-id="7daab-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-293">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="7daab-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="7daab-295">Уникальный идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-296">location</span><span class="sxs-lookup"><span data-stu-id="7daab-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-297">Фактическое расположение точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-298">msLength</span><span class="sxs-lookup"><span data-stu-id="7daab-298">msLength</span></span> <br/> <i><span data-ttu-id="7daab-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="7daab-300">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-300">Experimental.</span></span> </b></span><span data-ttu-id="7daab-301">Майкрософт: длина кода (то есть количество символов) в расположении точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-302">пауза</span><span class="sxs-lookup"><span data-stu-id="7daab-302">paused</span></span>
<span data-ttu-id="7daab-303">Происходит, когда отладки разрывают точку останова или исключение.</span><span class="sxs-lookup"><span data-stu-id="7daab-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-304">Параметры</span><span class="sxs-lookup"><span data-stu-id="7daab-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="7daab-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="7daab-306">Вызовите стек, на который остановлен отладок.</span><span class="sxs-lookup"><span data-stu-id="7daab-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-307">reason</span><span class="sxs-lookup"><span data-stu-id="7daab-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="7daab-308">Допустимые значения: точка останова, шаг, исключение, другое</span><span class="sxs-lookup"><span data-stu-id="7daab-308">Allowed values: breakpoint, step, exception, other</span></span></i></td>
            <td><span data-ttu-id="7daab-309">Причина приостановки.</span><span class="sxs-lookup"><span data-stu-id="7daab-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-310">data</span><span class="sxs-lookup"><span data-stu-id="7daab-310">data</span></span> <br/> <i><span data-ttu-id="7daab-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="7daab-312">Объект, содержащий вспомогательные свойства для конкретного разрыва.</span><span class="sxs-lookup"><span data-stu-id="7daab-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="7daab-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="7daab-314">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="7daab-315">ИД точек останова</span><span class="sxs-lookup"><span data-stu-id="7daab-315">Hit breakpoints IDs</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="7daab-316">возобновлено</span><span class="sxs-lookup"><span data-stu-id="7daab-316">resumed</span></span>
<span data-ttu-id="7daab-317">Собяно, когда отладка возобновляет выполнение.</span><span class="sxs-lookup"><span data-stu-id="7daab-317">Fired when the debugger resumes execution.</span></span>


---

## <span data-ttu-id="7daab-318">Типы</span><span class="sxs-lookup"><span data-stu-id="7daab-318">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="7daab-319">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="7daab-319">BreakpointId</span></span> `string`

<span data-ttu-id="7daab-320">Идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="7daab-320">Breakpoint identifier.</span></span>


---

### <a name="callframeid"></a> <span data-ttu-id="7daab-321">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="7daab-321">CallFrameId</span></span> `string`

<span data-ttu-id="7daab-322">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-322">Call frame identifier.</span></span>


---

### <a name="location"></a> <span data-ttu-id="7daab-323">Location</span><span class="sxs-lookup"><span data-stu-id="7daab-323">Location</span></span> `object`

<span data-ttu-id="7daab-324">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="7daab-324">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-325">Свойства</span><span class="sxs-lookup"><span data-stu-id="7daab-325">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-326">scriptId</span><span class="sxs-lookup"><span data-stu-id="7daab-326">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="7daab-327">Идентификатор скрипта, как по данным в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="7daab-327">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-328">lineNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-328">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-329">Номер строки в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="7daab-329">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-330">columnNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-330">columnNumber</span></span> <br/> <i><span data-ttu-id="7daab-331">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-331">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-332">Номер столбца в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="7daab-332">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-333">msLength</span><span class="sxs-lookup"><span data-stu-id="7daab-333">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-334">Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-334">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="breaklocation"></a> <span data-ttu-id="7daab-335">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="7daab-335">BreakLocation</span></span> `object`

<span data-ttu-id="7daab-336">Место приорвать в исходный код.</span><span class="sxs-lookup"><span data-stu-id="7daab-336">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-337">Свойства</span><span class="sxs-lookup"><span data-stu-id="7daab-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-338">scriptId</span><span class="sxs-lookup"><span data-stu-id="7daab-338">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="7daab-339">Идентификатор сценария, как сообщается в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="7daab-339">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-340">lineNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-340">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-341">Номер строки в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="7daab-341">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-342">columnNumber</span><span class="sxs-lookup"><span data-stu-id="7daab-342">columnNumber</span></span> <br/> <i><span data-ttu-id="7daab-343">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-343">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-344">Номер столбца в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="7daab-344">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-345">msLength</span><span class="sxs-lookup"><span data-stu-id="7daab-345">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="7daab-346">Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-346">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-347">Тип</span><span class="sxs-lookup"><span data-stu-id="7daab-347">type</span></span> <br/> <i><span data-ttu-id="7daab-348">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-348">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-349">Допустимые значения: debuggerStatement, call, return.</span><span class="sxs-lookup"><span data-stu-id="7daab-349">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="callframe"></a> <span data-ttu-id="7daab-350">CallFrame</span><span class="sxs-lookup"><span data-stu-id="7daab-350">CallFrame</span></span> `object`

<span data-ttu-id="7daab-351">Фрейм вызова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-351">JavaScript call frame.</span></span> <span data-ttu-id="7daab-352">Массив кадров вызовов формирует стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="7daab-352">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-353">Свойства</span><span class="sxs-lookup"><span data-stu-id="7daab-353">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-354">callFrameId</span><span class="sxs-lookup"><span data-stu-id="7daab-354">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="7daab-355">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-355">Call frame identifier.</span></span> <span data-ttu-id="7daab-356">Этот идентификатор действителен, только когда отладка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="7daab-356">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-357">functionName</span><span class="sxs-lookup"><span data-stu-id="7daab-357">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-358">Имя функции JavaScript, вызываемой в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-358">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-359">functionLocation</span><span class="sxs-lookup"><span data-stu-id="7daab-359">functionLocation</span></span> <br/> <i><span data-ttu-id="7daab-360">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-360">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="7daab-361">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7daab-361">Experimental.</span></span> </b></span><span data-ttu-id="7daab-362">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="7daab-362">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-363">location</span><span class="sxs-lookup"><span data-stu-id="7daab-363">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-364">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="7daab-364">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-365">url</span><span class="sxs-lookup"><span data-stu-id="7daab-365">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7daab-366">Имя или URL-адрес сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7daab-366">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-367">scopeChain</span><span class="sxs-lookup"><span data-stu-id="7daab-367">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="7daab-368">Цепочка областей для этого кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-368">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-369">это</span><span class="sxs-lookup"><span data-stu-id="7daab-369">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="7daab-370">объект для этого кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="7daab-370">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-371">returnValue</span><span class="sxs-lookup"><span data-stu-id="7daab-371">returnValue</span></span> <br/> <i><span data-ttu-id="7daab-372">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-372">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="7daab-373">Возвращаемая величина, если функция находится в точке возврата.</span><span class="sxs-lookup"><span data-stu-id="7daab-373">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="scope"></a> <span data-ttu-id="7daab-374">Область применения</span><span class="sxs-lookup"><span data-stu-id="7daab-374">Scope</span></span> `object`

<span data-ttu-id="7daab-375">Описание области.</span><span class="sxs-lookup"><span data-stu-id="7daab-375">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7daab-376">Свойства</span><span class="sxs-lookup"><span data-stu-id="7daab-376">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7daab-377">Тип</span><span class="sxs-lookup"><span data-stu-id="7daab-377">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="7daab-378">Допустимые значения: global, local, with, closure, catch, block, script, eval, module</span><span class="sxs-lookup"><span data-stu-id="7daab-378">Allowed values: global, local, with, closure, catch, block, script, eval, module</span></span></i></td>
            <td><span data-ttu-id="7daab-379">Тип области.</span><span class="sxs-lookup"><span data-stu-id="7daab-379">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-380">объект</span><span class="sxs-lookup"><span data-stu-id="7daab-380">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="7daab-381">Объект, представляющий область.</span><span class="sxs-lookup"><span data-stu-id="7daab-381">Object representing the scope.</span></span> <span data-ttu-id="7daab-382">Для и областей он представляет фактический объект; для остальных областей он является искусственным временным объектом, который передает переменные области в качестве <code>global</code> <code>with</code> своих свойств.</span><span class="sxs-lookup"><span data-stu-id="7daab-382">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-383">name</span><span class="sxs-lookup"><span data-stu-id="7daab-383">name</span></span> <br/> <i><span data-ttu-id="7daab-384">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-384">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-385">startLocation</span><span class="sxs-lookup"><span data-stu-id="7daab-385">startLocation</span></span> <br/> <i><span data-ttu-id="7daab-386">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-386">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-387">Расположение в исходный код, где начинается область</span><span class="sxs-lookup"><span data-stu-id="7daab-387">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="7daab-388">endLocation</span><span class="sxs-lookup"><span data-stu-id="7daab-388">endLocation</span></span> <br/> <i><span data-ttu-id="7daab-389">необязательные</span><span class="sxs-lookup"><span data-stu-id="7daab-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="7daab-390">Расположение в коде источника, где заканчивается область</span><span class="sxs-lookup"><span data-stu-id="7daab-390">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="7daab-391">Зависимости</span><span class="sxs-lookup"><span data-stu-id="7daab-391">Dependencies</span></span>

[<span data-ttu-id="7daab-392">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="7daab-392">Runtime</span></span>](runtime.md)
