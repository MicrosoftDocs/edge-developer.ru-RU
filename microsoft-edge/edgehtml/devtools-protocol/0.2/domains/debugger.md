---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена отлада. Домен отлада предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.
title: Домен отлада — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24571b3a32acf085dd9ccbd641b1e5b06b3b9504
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235190"
---
# <span data-ttu-id="97277-105">Домен отлада — протокол DevTools версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="97277-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="97277-106">Домен отладки предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="97277-107">Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="97277-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="97277-108">Методы</span><span class="sxs-lookup"><span data-stu-id="97277-108">Methods</span></span>**](#methods) | <span data-ttu-id="97277-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="97277-109">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |
| [**<span data-ttu-id="97277-110">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="97277-110">Events</span></span>**](#events) | <span data-ttu-id="97277-111">[scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [приостановлено,](#paused) [возобновлено](#resumed)</span><span class="sxs-lookup"><span data-stu-id="97277-111">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |
| [**<span data-ttu-id="97277-112">Типы</span><span class="sxs-lookup"><span data-stu-id="97277-112">Types</span></span>**](#types) | <span data-ttu-id="97277-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span><span class="sxs-lookup"><span data-stu-id="97277-113">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |
| [**<span data-ttu-id="97277-114">Зависимости</span><span class="sxs-lookup"><span data-stu-id="97277-114">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="97277-115">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="97277-115">Runtime</span></span>](runtime.md) |
## <span data-ttu-id="97277-116">Методы</span><span class="sxs-lookup"><span data-stu-id="97277-116">Methods</span></span>

### <span data-ttu-id="97277-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="97277-117">enable</span></span>
<span data-ttu-id="97277-118">Включает отладок для заданной страницы.</span><span class="sxs-lookup"><span data-stu-id="97277-118">Enables debugger for the given page.</span></span> <span data-ttu-id="97277-119">Клиенты не должны предполагать, что отладка включена, пока не будет получен результат для этой команды.</span><span class="sxs-lookup"><span data-stu-id="97277-119">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>

</p>

---

### <span data-ttu-id="97277-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="97277-120">disable</span></span>
<span data-ttu-id="97277-121">Отключает отладок для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="97277-121">Disables debugger for given page.</span></span>

</p>

---

### <span data-ttu-id="97277-122">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="97277-122">getPossibleBreakpoints</span></span>
<span data-ttu-id="97277-123">Возвращает возможные расположения для точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-123">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="97277-124">ScriptId в расположениях в начале и конце диапазона должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="97277-124">scriptId in start and end range locations should be the same.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-125">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-126">start</span><span class="sxs-lookup"><span data-stu-id="97277-126">start</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-127">Начало диапазона для поиска возможных местоположений точек останова.</span><span class="sxs-lookup"><span data-stu-id="97277-127">Start of range to search possible breakpoint locations in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-128">завершить</span><span class="sxs-lookup"><span data-stu-id="97277-128">end</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-129">Конец диапазона для поиска возможных местоположений точек останова в (за исключением).</span><span class="sxs-lookup"><span data-stu-id="97277-129">End of range to search possible breakpoint locations in (excluding).</span></span> <span data-ttu-id="97277-130">Если он не указан, конец диапазона используется для окончания сценариев.</span><span class="sxs-lookup"><span data-stu-id="97277-130">When not specified, end of scripts is used as end of range.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-131">Возвращает</span><span class="sxs-lookup"><span data-stu-id="97277-131">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-132">locations</span><span class="sxs-lookup"><span data-stu-id="97277-132">locations</span></span></td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td><span data-ttu-id="97277-133">Список возможных местоположений точек останова.</span><span class="sxs-lookup"><span data-stu-id="97277-133">List of the possible breakpoint locations.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-134">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="97277-134">setBreakpointsActive</span></span>
<span data-ttu-id="97277-135">Активирует или деактивирует все точки останова на странице.</span><span class="sxs-lookup"><span data-stu-id="97277-135">Activates / deactivates all breakpoints on the page.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-136">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-137">active</span><span class="sxs-lookup"><span data-stu-id="97277-137">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="97277-138">Новое значение активного состояния точек останова.</span><span class="sxs-lookup"><span data-stu-id="97277-138">New value for breakpoints active state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-139">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="97277-139">setBreakpointByUrl</span></span>
<span data-ttu-id="97277-140">Задает точку останова JavaScript в указанном расположении, указанном с помощью URL-адреса или regex URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="97277-140">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span> <span data-ttu-id="97277-141">После того как эта команда будет выдана, все существующие сценарии будут иметь точки останова, разрешенные и возвращенные в <code>locations</code> свойстве.</span><span class="sxs-lookup"><span data-stu-id="97277-141">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in <code>locations</code> property.</span></span> <span data-ttu-id="97277-142">Дальнейшее соответствие сценариев приведет к последующим <code>breakpointResolved</code> событиям.</span><span class="sxs-lookup"><span data-stu-id="97277-142">Further matching script parsing will result in subsequent <code>breakpointResolved</code> events issued.</span></span> <span data-ttu-id="97277-143">Эта логическая точка останова будет выдержать перезагрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="97277-143">This logical breakpoint will survive page reloads.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-144">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-144">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-145">lineNumber</span><span class="sxs-lookup"><span data-stu-id="97277-145">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-146">Номер строки для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-146">Line number to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-147">url</span><span class="sxs-lookup"><span data-stu-id="97277-147">url</span></span> <br/> <i><span data-ttu-id="97277-148">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-148">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-149">URL-адрес ресурсов для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-149">URL of the resources to set breakpoint on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-150">urlRegex</span><span class="sxs-lookup"><span data-stu-id="97277-150">urlRegex</span></span> <br/> <i><span data-ttu-id="97277-151">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-151">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-152">Шаблон повторного использования URL-адресов ресурсов, в которые необходимо установить точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-152">Regex pattern for the URLs of the resources to set breakpoints on.</span></span> <span data-ttu-id="97277-153">Либо <code>url</code> должно <code>urlRegex</code> быть указано, либо должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="97277-153">Either <code>url</code> or <code>urlRegex</code> must be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-154">columnNumber</span><span class="sxs-lookup"><span data-stu-id="97277-154">columnNumber</span></span> <br/> <i><span data-ttu-id="97277-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-155">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-156">Смещение в строке для назначения точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-156">Offset in the line to set breakpoint at.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-157">condition</span><span class="sxs-lookup"><span data-stu-id="97277-157">condition</span></span> <br/> <i><span data-ttu-id="97277-158">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-158">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-159">Выражение, используемое в качестве условия точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-159">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="97277-160">Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</span><span class="sxs-lookup"><span data-stu-id="97277-160">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-161">Возвращает</span><span class="sxs-lookup"><span data-stu-id="97277-161">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-162">breakpointId</span><span class="sxs-lookup"><span data-stu-id="97277-162">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="97277-163">ИД созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="97277-163">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-164">locations</span><span class="sxs-lookup"><span data-stu-id="97277-164">locations</span></span></td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td><span data-ttu-id="97277-165">Список местоположений, в которые эта точка останова была разрешена после добавления.</span><span class="sxs-lookup"><span data-stu-id="97277-165">List of the locations this breakpoint resolved into upon addition.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-166">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="97277-166">setBreakpoint</span></span>
<span data-ttu-id="97277-167">Задает точку останова JavaScript в заданное расположение.</span><span class="sxs-lookup"><span data-stu-id="97277-167">Sets JavaScript breakpoint at a given location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-168">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-168">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-169">location</span><span class="sxs-lookup"><span data-stu-id="97277-169">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-170">Расположение для определения точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-170">Location to set breakpoint in.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-171">condition</span><span class="sxs-lookup"><span data-stu-id="97277-171">condition</span></span> <br/> <i><span data-ttu-id="97277-172">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-172">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-173">Выражение, используемое в качестве условия точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-173">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="97277-174">Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</span><span class="sxs-lookup"><span data-stu-id="97277-174">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-175">Возвращает</span><span class="sxs-lookup"><span data-stu-id="97277-175">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-176">breakpointId</span><span class="sxs-lookup"><span data-stu-id="97277-176">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="97277-177">ИД созданной точки останова для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="97277-177">Id of the created breakpoint for further reference.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-178">actualLocation</span><span class="sxs-lookup"><span data-stu-id="97277-178">actualLocation</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-179">Расположение, в который разрешена точка останова.</span><span class="sxs-lookup"><span data-stu-id="97277-179">Location this breakpoint resolved into.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-180">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="97277-180">removeBreakpoint</span></span>
<span data-ttu-id="97277-181">Удаляет точку останова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-181">Removes JavaScript breakpoint.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-182">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-182">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-183">breakpointId</span><span class="sxs-lookup"><span data-stu-id="97277-183">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-184">stepOver</span><span class="sxs-lookup"><span data-stu-id="97277-184">stepOver</span></span>
<span data-ttu-id="97277-185">По шагам над заявлением.</span><span class="sxs-lookup"><span data-stu-id="97277-185">Steps over the statement.</span></span>

</p>

---

### <span data-ttu-id="97277-186">stepInto</span><span class="sxs-lookup"><span data-stu-id="97277-186">stepInto</span></span>
<span data-ttu-id="97277-187">Этапы вызова функции.</span><span class="sxs-lookup"><span data-stu-id="97277-187">Steps into the function call.</span></span>

</p>

---

### <span data-ttu-id="97277-188">stepOut</span><span class="sxs-lookup"><span data-stu-id="97277-188">stepOut</span></span>
<span data-ttu-id="97277-189">По шагам из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="97277-189">Steps out of the function call.</span></span>

</p>

---

### <span data-ttu-id="97277-190">pause</span><span class="sxs-lookup"><span data-stu-id="97277-190">pause</span></span>
<span data-ttu-id="97277-191">Останавливает следующий отчет JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-191">Stops on the next JavaScript statement.</span></span>

</p>

---

### <span data-ttu-id="97277-192">resume</span><span class="sxs-lookup"><span data-stu-id="97277-192">resume</span></span>
<span data-ttu-id="97277-193">Возобновляет выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-193">Resumes JavaScript execution.</span></span>

</p>

---

### <span data-ttu-id="97277-194">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="97277-194">getScriptSource</span></span>
<span data-ttu-id="97277-195">Возвращает источник для сценария с заданным идом.</span><span class="sxs-lookup"><span data-stu-id="97277-195">Returns source for the script with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-196">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-196">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-197">scriptId</span><span class="sxs-lookup"><span data-stu-id="97277-197">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="97277-198">ИД сценария, для который требуется получить источник.</span><span class="sxs-lookup"><span data-stu-id="97277-198">Id of the script to get source for.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-199">Возвращает</span><span class="sxs-lookup"><span data-stu-id="97277-199">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-200">scriptSource</span><span class="sxs-lookup"><span data-stu-id="97277-200">scriptSource</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-201">Источник скрипта.</span><span class="sxs-lookup"><span data-stu-id="97277-201">Script source.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-202">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="97277-202">setPauseOnExceptions</span></span>
<span data-ttu-id="97277-203">Определяет паузу в состоянии исключений.</span><span class="sxs-lookup"><span data-stu-id="97277-203">Defines pause on exceptions state.</span></span> <span data-ttu-id="97277-204">Можно установить остановку для всех исключений, невысченных исключений или без исключений.</span><span class="sxs-lookup"><span data-stu-id="97277-204">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span> <span data-ttu-id="97277-205">Начальная пауза в состоянии исключений <code>none</code> — .</span><span class="sxs-lookup"><span data-stu-id="97277-205">Initial pause on exceptions state is <code>none</code>.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-206">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-206">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-207">state</span><span class="sxs-lookup"><span data-stu-id="97277-207">state</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="97277-208">Допустимые значения: none, uncaught, all</span><span class="sxs-lookup"><span data-stu-id="97277-208">Allowed values: none, uncaught, all</span></span></i></td>
            <td><span data-ttu-id="97277-209">Приостановка в режиме исключений.</span><span class="sxs-lookup"><span data-stu-id="97277-209">Pause on exceptions mode.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-210">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="97277-210">evaluateOnCallFrame</span></span>
<span data-ttu-id="97277-211">Оценивает выражение в заданной рамке вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-211">Evaluates expression on a given call frame.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-212">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-212">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-213">callFrameId</span><span class="sxs-lookup"><span data-stu-id="97277-213">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="97277-214">Идентификатор кадра вызова для оценки.</span><span class="sxs-lookup"><span data-stu-id="97277-214">Call frame identifier to evaluate on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-215">выражение</span><span class="sxs-lookup"><span data-stu-id="97277-215">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-216">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="97277-216">Expression to evaluate.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-217">Возвращает</span><span class="sxs-lookup"><span data-stu-id="97277-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-218">result</span><span class="sxs-lookup"><span data-stu-id="97277-218">result</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="97277-219">Оболочка объекта для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="97277-219">Object wrapper for the evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-220">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="97277-220">setVariableValue</span></span>
<span data-ttu-id="97277-221">Изменяет значение переменной в callframe.</span><span class="sxs-lookup"><span data-stu-id="97277-221">Changes value of variable in a callframe.</span></span> <span data-ttu-id="97277-222">Области на основе объектов не поддерживаются и должны быть мутированы вручную.</span><span class="sxs-lookup"><span data-stu-id="97277-222">Object-based scopes are not supported and must be mutated manually.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-223">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-223">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-224">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="97277-224">scopeNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-225">Число областей на основе 0, указанных в цепочке областей.</span><span class="sxs-lookup"><span data-stu-id="97277-225">0-based number of scope as was listed in scope chain.</span></span> <span data-ttu-id="97277-226">Разрешены только типы областей "local", "closure" и "catch".</span><span class="sxs-lookup"><span data-stu-id="97277-226">Only 'local', 'closure' and 'catch' scope types are allowed.</span></span> <span data-ttu-id="97277-227">Другие области могут управляться вручную.</span><span class="sxs-lookup"><span data-stu-id="97277-227">Other scopes could be manipulated manually.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-228">variableName</span><span class="sxs-lookup"><span data-stu-id="97277-228">variableName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-229">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="97277-229">Variable name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-230">newValue</span><span class="sxs-lookup"><span data-stu-id="97277-230">newValue</span></span></td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td><span data-ttu-id="97277-231">Новое значение переменной.</span><span class="sxs-lookup"><span data-stu-id="97277-231">New variable value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-232">callFrameId</span><span class="sxs-lookup"><span data-stu-id="97277-232">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="97277-233">ИД callframe, который содержит переменную.</span><span class="sxs-lookup"><span data-stu-id="97277-233">Id of callframe that holds variable.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-234">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="97277-234">setBlackboxPatterns</span></span>
<span><b><span data-ttu-id="97277-235">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-235">Experimental.</span></span> </b></span><span data-ttu-id="97277-236">Замените предыдущие шаблоны черных ящиков на переданные.</span><span class="sxs-lookup"><span data-stu-id="97277-236">Replace previous blackbox patterns with passed ones.</span></span> <span data-ttu-id="97277-237">Заставляет тыловые части пропускать пошаговую или приоходную пошаговую отрисовку в сценариях с URL-адресом, совпадающий с одним из шаблонов.</span><span class="sxs-lookup"><span data-stu-id="97277-237">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span> <span data-ttu-id="97277-238">Отладик попытается выйти из сценария из черной почты, выполив "шаг" несколько раз, и, наконец, при неудачном выполнении прибег к шагу "выйти".</span><span class="sxs-lookup"><span data-stu-id="97277-238">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-240">patterns</span><span class="sxs-lookup"><span data-stu-id="97277-240">patterns</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="97277-241">Массив regexps, который будет использоваться для проверки URL-адреса скрипта на состояние черного ящика.</span><span class="sxs-lookup"><span data-stu-id="97277-241">Array of regexps that will be used to check script url for blackbox state.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-242">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="97277-242">msSetDebuggerPropertyValue</span></span>
<span><b><span data-ttu-id="97277-243">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-243">Experimental.</span></span> </b></span><span data-ttu-id="97277-244">Корпорация Майкрософт: задает указанное значение для указанного свойства отладки.</span><span class="sxs-lookup"><span data-stu-id="97277-244">Microsoft: Sets the specified debugger property to the specified value.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-245">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-246">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="97277-246">debuggerPropertyId</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-247">Майкрософт: ид свойства (например, msDebuggerPropertyId), который необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="97277-247">Microsoft: The property id (i.e. msDebuggerPropertyId) to set.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-248">newValue</span><span class="sxs-lookup"><span data-stu-id="97277-248">newValue</span></span></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="97277-249">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="97277-249">Events</span></span>

### <span data-ttu-id="97277-250">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="97277-250">scriptParsed</span></span>
<span data-ttu-id="97277-251">Срасть при разчете сценария.</span><span class="sxs-lookup"><span data-stu-id="97277-251">Fired when the script is parsed.</span></span> <span data-ttu-id="97277-252">Это событие также иллюбуется для всех известных и несмеченных сценариев при включии отладки.</span><span class="sxs-lookup"><span data-stu-id="97277-252">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-253">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-253">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-254">scriptId</span><span class="sxs-lookup"><span data-stu-id="97277-254">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="97277-255">Идентификатор разлияемого скрипта.</span><span class="sxs-lookup"><span data-stu-id="97277-255">Identifier of the script parsed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-256">url</span><span class="sxs-lookup"><span data-stu-id="97277-256">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-257">URL-адрес или имя разбияемого сценария (если таково).</span><span class="sxs-lookup"><span data-stu-id="97277-257">URL or name of the script parsed (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-258">startLine</span><span class="sxs-lookup"><span data-stu-id="97277-258">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-259">Смещение строк скрипта в ресурсе с заданным URL-адресом (для тегов скрипта).</span><span class="sxs-lookup"><span data-stu-id="97277-259">Line offset of the script within the resource with given URL (for script tags).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-260">startColumn</span><span class="sxs-lookup"><span data-stu-id="97277-260">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-261">Смещение столбцов сценария в ресурсе с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="97277-261">Column offset of the script within the resource with given URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-262">endLine</span><span class="sxs-lookup"><span data-stu-id="97277-262">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-263">Последняя строка сценария.</span><span class="sxs-lookup"><span data-stu-id="97277-263">Last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-264">endColumn</span><span class="sxs-lookup"><span data-stu-id="97277-264">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-265">Длина последней строки сценария.</span><span class="sxs-lookup"><span data-stu-id="97277-265">Length of the last line of the script.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="97277-266">executionContextId</span></span></td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td><span data-ttu-id="97277-267">Указывает контекст создания скрипта.</span><span class="sxs-lookup"><span data-stu-id="97277-267">Specifies script creation context.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-268">sourceMapURL</span><span class="sxs-lookup"><span data-stu-id="97277-268">sourceMapURL</span></span> <br/> <i><span data-ttu-id="97277-269">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-269">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-270">URL-адрес карты источника, связанной со сценарием (если таково).</span><span class="sxs-lookup"><span data-stu-id="97277-270">URL of source map associated with script (if any).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-271">length</span><span class="sxs-lookup"><span data-stu-id="97277-271">length</span></span> <br/> <i><span data-ttu-id="97277-272">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-272">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="97277-273">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-273">Experimental.</span></span> </b></span><span data-ttu-id="97277-274">Длина этого скрипта.</span><span class="sxs-lookup"><span data-stu-id="97277-274">This script length.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-275">msParentId</span><span class="sxs-lookup"><span data-stu-id="97277-275">msParentId</span></span> <br/> <i><span data-ttu-id="97277-276">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-276">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="97277-277">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-277">Experimental.</span></span> </b></span><span data-ttu-id="97277-278">Это родительский ИД документа.</span><span class="sxs-lookup"><span data-stu-id="97277-278">This is the parent document ID.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-279">msMimeType</span><span class="sxs-lookup"><span data-stu-id="97277-279">msMimeType</span></span> <br/> <i><span data-ttu-id="97277-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-280">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="97277-281">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-281">Experimental.</span></span> </b></span><span data-ttu-id="97277-282">Это тип MIME.</span><span class="sxs-lookup"><span data-stu-id="97277-282">This is the mime type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-283">msIsDynamicCode</span><span class="sxs-lookup"><span data-stu-id="97277-283">msIsDynamicCode</span></span> <br/> <i><span data-ttu-id="97277-284">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-284">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="97277-285">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-285">Experimental.</span></span> </b></span><span data-ttu-id="97277-286">Это указывает, является ли это динамическим кодом.</span><span class="sxs-lookup"><span data-stu-id="97277-286">This indicates whether it is dynamic code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-287">msLongDocumentId</span><span class="sxs-lookup"><span data-stu-id="97277-287">msLongDocumentId</span></span> <br/> <i><span data-ttu-id="97277-288">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-288">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="97277-289">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-289">Experimental.</span></span> </b></span><span data-ttu-id="97277-290">Это длинный ИД документа.</span><span class="sxs-lookup"><span data-stu-id="97277-290">This is the long document ID.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-291">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="97277-291">breakpointResolved</span></span>
<span data-ttu-id="97277-292">Происходит, когда точка останова разрешена к фактическому сценарию и расположению.</span><span class="sxs-lookup"><span data-stu-id="97277-292">Fired when breakpoint is resolved to an actual script and location.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-293">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-293">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-294">breakpointId</span><span class="sxs-lookup"><span data-stu-id="97277-294">breakpointId</span></span></td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td><span data-ttu-id="97277-295">Уникальный идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-295">Breakpoint unique identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-296">location</span><span class="sxs-lookup"><span data-stu-id="97277-296">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-297">Фактическое расположение точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-297">Actual breakpoint location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-298">msLength</span><span class="sxs-lookup"><span data-stu-id="97277-298">msLength</span></span> <br/> <i><span data-ttu-id="97277-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-299">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b><span data-ttu-id="97277-300">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-300">Experimental.</span></span> </b></span><span data-ttu-id="97277-301">Майкрософт: длина кода (то есть количество символов) в расположении точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-301">Microsoft: Length of code (i.e. number of characters) at the breakpoint location.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-302">пауза</span><span class="sxs-lookup"><span data-stu-id="97277-302">paused</span></span>
<span data-ttu-id="97277-303">Происходит, когда отладки разрывают точку останова или исключение.</span><span class="sxs-lookup"><span data-stu-id="97277-303">Fired when the debuggers breaks for a breakpoint or exception.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-304">Параметры</span><span class="sxs-lookup"><span data-stu-id="97277-304">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-305">callFrames</span><span class="sxs-lookup"><span data-stu-id="97277-305">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="97277-306">Вызовите стек, на который остановлен отладок.</span><span class="sxs-lookup"><span data-stu-id="97277-306">Call stack the debugger stopped on.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-307">reason</span><span class="sxs-lookup"><span data-stu-id="97277-307">reason</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="97277-308">Допустимые значения: точка останова, шаг, исключение, другое, EventListener</span><span class="sxs-lookup"><span data-stu-id="97277-308">Allowed values: breakpoint, step, exception, other, EventListener</span></span></i></td>
            <td><span data-ttu-id="97277-309">Причина приостановки.</span><span class="sxs-lookup"><span data-stu-id="97277-309">Pause reason.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-310">data</span><span class="sxs-lookup"><span data-stu-id="97277-310">data</span></span> <br/> <i><span data-ttu-id="97277-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-311">optional</span></span></i></td>
            <td><code class="flyout">object</code></td>
            <td><span data-ttu-id="97277-312">Объект, содержащий вспомогательные свойства для конкретного разрыва.</span><span class="sxs-lookup"><span data-stu-id="97277-312">Object containing break-specific auxiliary properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-313">hitBreakpoints</span><span class="sxs-lookup"><span data-stu-id="97277-313">hitBreakpoints</span></span> <br/> <i><span data-ttu-id="97277-314">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-314">optional</span></span></i></td>
            <td><code class="flyout">string[]</code></td>
            <td><span data-ttu-id="97277-315">ИД точек останова</span><span class="sxs-lookup"><span data-stu-id="97277-315">Hit breakpoints IDs</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-316">asyncStackTrace</span><span class="sxs-lookup"><span data-stu-id="97277-316">asyncStackTrace</span></span> <br/> <i><span data-ttu-id="97277-317">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-317">optional</span></span></i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td><span data-ttu-id="97277-318">Трассировка а async стека JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-318">JavaScript async stack trace.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="97277-319">возобновлено</span><span class="sxs-lookup"><span data-stu-id="97277-319">resumed</span></span>
<span data-ttu-id="97277-320">Собяно, когда отладка возобновляет выполнение.</span><span class="sxs-lookup"><span data-stu-id="97277-320">Fired when the debugger resumes execution.</span></span>

</p>

---

## <span data-ttu-id="97277-321">Типы</span><span class="sxs-lookup"><span data-stu-id="97277-321">Types</span></span>

### <a name="breakpointid"></a> <span data-ttu-id="97277-322">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="97277-322">BreakpointId</span></span> `string`

<span data-ttu-id="97277-323">Идентификатор точки останова.</span><span class="sxs-lookup"><span data-stu-id="97277-323">Breakpoint identifier.</span></span>

</p>

---

### <a name="callframeid"></a> <span data-ttu-id="97277-324">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="97277-324">CallFrameId</span></span> `string`

<span data-ttu-id="97277-325">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-325">Call frame identifier.</span></span>

</p>

---

### <a name="location"></a> <span data-ttu-id="97277-326">Location</span><span class="sxs-lookup"><span data-stu-id="97277-326">Location</span></span> `object`

<span data-ttu-id="97277-327">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="97277-327">Location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-328">Свойства</span><span class="sxs-lookup"><span data-stu-id="97277-328">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-329">scriptId</span><span class="sxs-lookup"><span data-stu-id="97277-329">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="97277-330">Идентификатор скрипта, как по данным в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="97277-330">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-331">lineNumber</span><span class="sxs-lookup"><span data-stu-id="97277-331">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-332">Номер строки в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="97277-332">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-333">columnNumber</span><span class="sxs-lookup"><span data-stu-id="97277-333">columnNumber</span></span> <br/> <i><span data-ttu-id="97277-334">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-334">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-335">Номер столбца в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="97277-335">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-336">msLength</span><span class="sxs-lookup"><span data-stu-id="97277-336">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-337">Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-337">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> <span data-ttu-id="97277-338">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="97277-338">BreakLocation</span></span> `object`

<span data-ttu-id="97277-339">Место приорвать в исходный код.</span><span class="sxs-lookup"><span data-stu-id="97277-339">Break location in the source code.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-340">Свойства</span><span class="sxs-lookup"><span data-stu-id="97277-340">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-341">scriptId</span><span class="sxs-lookup"><span data-stu-id="97277-341">scriptId</span></span></td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td><span data-ttu-id="97277-342">Идентификатор сценария, как сообщается в <code>Debugger.scriptParsed</code> .</span><span class="sxs-lookup"><span data-stu-id="97277-342">Script identifier as reported in the <code>Debugger.scriptParsed</code>.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-343">lineNumber</span><span class="sxs-lookup"><span data-stu-id="97277-343">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-344">Номер строки в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="97277-344">Line number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-345">columnNumber</span><span class="sxs-lookup"><span data-stu-id="97277-345">columnNumber</span></span> <br/> <i><span data-ttu-id="97277-346">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-346">optional</span></span></i></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-347">Номер столбца в сценарии (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="97277-347">Column number in the script (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-348">msLength</span><span class="sxs-lookup"><span data-stu-id="97277-348">msLength</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="97277-349">Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-349">Microsoft: Length of code (i.e. number of characters) at this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-350">Тип</span><span class="sxs-lookup"><span data-stu-id="97277-350">type</span></span> <br/> <i><span data-ttu-id="97277-351">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-351">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-352">Допустимые значения: debuggerStatement, call, return.</span><span class="sxs-lookup"><span data-stu-id="97277-352">Allowed values: debuggerStatement, call, return.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> <span data-ttu-id="97277-353">CallFrame</span><span class="sxs-lookup"><span data-stu-id="97277-353">CallFrame</span></span> `object`

<span data-ttu-id="97277-354">Фрейм вызова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-354">JavaScript call frame.</span></span> <span data-ttu-id="97277-355">Массив кадров вызовов формирует стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="97277-355">Array of call frames form the call stack.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-356">Свойства</span><span class="sxs-lookup"><span data-stu-id="97277-356">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-357">callFrameId</span><span class="sxs-lookup"><span data-stu-id="97277-357">callFrameId</span></span></td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td><span data-ttu-id="97277-358">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-358">Call frame identifier.</span></span> <span data-ttu-id="97277-359">Этот идентификатор действителен, только когда отладка приостановлена.</span><span class="sxs-lookup"><span data-stu-id="97277-359">This identifier is only valid while the debugger is paused.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-360">functionName</span><span class="sxs-lookup"><span data-stu-id="97277-360">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-361">Имя функции JavaScript, вызываемой в этом фрейме вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-361">Name of the JavaScript function called on this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-362">functionLocation</span><span class="sxs-lookup"><span data-stu-id="97277-362">functionLocation</span></span> <br/> <i><span data-ttu-id="97277-363">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-363">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b><span data-ttu-id="97277-364">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="97277-364">Experimental.</span></span> </b></span><span data-ttu-id="97277-365">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="97277-365">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-366">location</span><span class="sxs-lookup"><span data-stu-id="97277-366">location</span></span></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-367">Расположение в коде источника.</span><span class="sxs-lookup"><span data-stu-id="97277-367">Location in the source code.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-368">url</span><span class="sxs-lookup"><span data-stu-id="97277-368">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="97277-369">Имя или URL-адрес сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97277-369">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-370">scopeChain</span><span class="sxs-lookup"><span data-stu-id="97277-370">scopeChain</span></span></td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td><span data-ttu-id="97277-371">Цепочка областей для этого кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-371">Scope chain for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-372">это</span><span class="sxs-lookup"><span data-stu-id="97277-372">this</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> <span data-ttu-id="97277-373">объект для этого кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="97277-373">object for this call frame.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-374">returnValue</span><span class="sxs-lookup"><span data-stu-id="97277-374">returnValue</span></span> <br/> <i><span data-ttu-id="97277-375">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-375">optional</span></span></i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="97277-376">Возвращаемая величина, если функция находится в точке возврата.</span><span class="sxs-lookup"><span data-stu-id="97277-376">The value being returned, if the function is at return point.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> <span data-ttu-id="97277-377">Область применения</span><span class="sxs-lookup"><span data-stu-id="97277-377">Scope</span></span> `object`

<span data-ttu-id="97277-378">Описание области.</span><span class="sxs-lookup"><span data-stu-id="97277-378">Scope description.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="97277-379">Свойства</span><span class="sxs-lookup"><span data-stu-id="97277-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="97277-380">Тип</span><span class="sxs-lookup"><span data-stu-id="97277-380">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="97277-381">Допустимые значения: global, local, with, closure, catch, block, script, eval, module, return</span><span class="sxs-lookup"><span data-stu-id="97277-381">Allowed values: global, local, with, closure, catch, block, script, eval, module, return</span></span></i></td>
            <td><span data-ttu-id="97277-382">Тип области.</span><span class="sxs-lookup"><span data-stu-id="97277-382">Scope type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-383">объект</span><span class="sxs-lookup"><span data-stu-id="97277-383">object</span></span></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><span data-ttu-id="97277-384">Объект, представляющий область.</span><span class="sxs-lookup"><span data-stu-id="97277-384">Object representing the scope.</span></span> <span data-ttu-id="97277-385">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span><span class="sxs-lookup"><span data-stu-id="97277-385">For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-386">name</span><span class="sxs-lookup"><span data-stu-id="97277-386">name</span></span> <br/> <i><span data-ttu-id="97277-387">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-387">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-388">startLocation</span><span class="sxs-lookup"><span data-stu-id="97277-388">startLocation</span></span> <br/> <i><span data-ttu-id="97277-389">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-389">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-390">Расположение в исходный код, где начинается область</span><span class="sxs-lookup"><span data-stu-id="97277-390">Location in the source code where scope starts</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="97277-391">endLocation</span><span class="sxs-lookup"><span data-stu-id="97277-391">endLocation</span></span> <br/> <i><span data-ttu-id="97277-392">необязательные</span><span class="sxs-lookup"><span data-stu-id="97277-392">optional</span></span></i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span data-ttu-id="97277-393">Расположение в коде источника, где заканчивается область</span><span class="sxs-lookup"><span data-stu-id="97277-393">Location in the source code where scope ends</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="97277-394">Зависимости</span><span class="sxs-lookup"><span data-stu-id="97277-394">Dependencies</span></span>

[<span data-ttu-id="97277-395">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="97277-395">Runtime</span></span>](runtime.md)
