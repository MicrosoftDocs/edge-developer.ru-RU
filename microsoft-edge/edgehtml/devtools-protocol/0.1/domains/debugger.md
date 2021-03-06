---
description: Ссылка на протокол DevTools Версии 0.1 (EdgeHTML) для домена Debugger.  Домен Debugger предоставляет возможности отладки JavaScript.  Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.
title: Домен Debugger — протокол DevTools Версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d63408e23fd8912cf617bfefae2b991387b45a38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397680"
---
# <a name="debugger-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="bba2c-105">Домен Debugger — протокол DevTools Версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="bba2c-105">Debugger Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  
  
<span data-ttu-id="bba2c-106">Домен Debugger предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bba2c-106">Debugger domain exposes JavaScript debugging capabilities.</span></span>  <span data-ttu-id="bba2c-107">Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="bba2c-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="bba2c-108">Категория</span><span class="sxs-lookup"><span data-stu-id="bba2c-108">Classification</span></span> | <span data-ttu-id="bba2c-109">Участники</span><span class="sxs-lookup"><span data-stu-id="bba2c-109">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="bba2c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="bba2c-110">Methods</span></span>](#methods) | <span data-ttu-id="bba2c-111">[включить](#enable), отключить [,](#disable) [getPossibleBreakpoints](#getpossiblebreakpoints), [](#resume) [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), setBreakpoint , [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [](#setbreakpoint) [пауза](#pause), резюме , [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [оценкаOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="bba2c-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [<span data-ttu-id="bba2c-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="bba2c-112">Events</span></span>](#events) | <span data-ttu-id="bba2c-113">[scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="bba2c-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [<span data-ttu-id="bba2c-114">Типы</span><span class="sxs-lookup"><span data-stu-id="bba2c-114">Types</span></span>](#types) | <span data-ttu-id="bba2c-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Расположение](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Область](#scope)</span><span class="sxs-lookup"><span data-stu-id="bba2c-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [<span data-ttu-id="bba2c-116">Зависимости</span><span class="sxs-lookup"><span data-stu-id="bba2c-116">Dependencies</span></span>](#dependencies) | [<span data-ttu-id="bba2c-117">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="bba2c-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="bba2c-118">Методы</span><span class="sxs-lookup"><span data-stu-id="bba2c-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="bba2c-119">"Включить"</span><span class="sxs-lookup"><span data-stu-id="bba2c-119">enable</span></span>  

<span data-ttu-id="bba2c-120">Включает отладка для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="bba2c-120">Enables debugger for the given page.</span></span>  <span data-ttu-id="bba2c-121">Клиенты не должны предполагать, что отладка включена до тех пор, пока не будет получен результат для этой команды.</span><span class="sxs-lookup"><span data-stu-id="bba2c-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="bba2c-122">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="bba2c-122">disable</span></span>  

<span data-ttu-id="bba2c-123">Отладка отладки для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="bba2c-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="bba2c-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="bba2c-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="bba2c-125">Возвращает возможные расположения для breakpoint.</span><span class="sxs-lookup"><span data-stu-id="bba2c-125">Returns possible locations for breakpoint.</span></span>  <span data-ttu-id="bba2c-126">ScriptId в расположениях старта и конца диапазона должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="bba2c-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="bba2c-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-127">Parameters</span></span> | <span data-ttu-id="bba2c-128">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-128">Type</span></span> | <span data-ttu-id="bba2c-129">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-130">start</span><span class="sxs-lookup"><span data-stu-id="bba2c-130">start</span></span> | [<span data-ttu-id="bba2c-131">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-131">Location</span></span>](#location) | <span data-ttu-id="bba2c-132">Начало диапазона для поиска возможных точек разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="bba2c-133">завершить</span><span class="sxs-lookup"><span data-stu-id="bba2c-133">end</span></span> | [<span data-ttu-id="bba2c-134">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-134">Location</span></span>](#location) | <span data-ttu-id="bba2c-135">Конец диапазона для поиска возможных точек разрыва в \(excluding\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="bba2c-136">Если не указано, конец скриптов используется как конец диапазона.</span><span class="sxs-lookup"><span data-stu-id="bba2c-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="bba2c-137">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bba2c-137">Returns</span></span> | <span data-ttu-id="bba2c-138">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-138">Type</span></span> | <span data-ttu-id="bba2c-139">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-140">расположения</span><span class="sxs-lookup"><span data-stu-id="bba2c-140">locations</span></span> | [<span data-ttu-id="bba2c-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="bba2c-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="bba2c-142">Список возможных местоположений точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="bba2c-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="bba2c-143">setBreakpointsActive</span></span>  

<span data-ttu-id="bba2c-144">Активирует или отключает все точки взлома на странице.</span><span class="sxs-lookup"><span data-stu-id="bba2c-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="bba2c-145">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-145">Parameters</span></span> | <span data-ttu-id="bba2c-146">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-146">Type</span></span> | <span data-ttu-id="bba2c-147">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-148">active</span><span class="sxs-lookup"><span data-stu-id="bba2c-148">active</span></span> | `boolean` | <span data-ttu-id="bba2c-149">Новое значение для активного состояния точек breakpoints.</span><span class="sxs-lookup"><span data-stu-id="bba2c-149">New value for breakpoints active state.</span></span> |  

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="bba2c-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="bba2c-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="bba2c-151">Задает точку разрыва JavaScript в указанном расположении, указанном URL-адресом или URL-адресом regex.</span><span class="sxs-lookup"><span data-stu-id="bba2c-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="bba2c-152">После того как эта команда будет выдана, все существующие разбиенные сценарии будут иметь точки разрывов, разрешенные и возвращенные в `locations` свойстве.</span><span class="sxs-lookup"><span data-stu-id="bba2c-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="bba2c-153">Дальнейшее соответствие размыву сценариев приведет к последующим `breakpointResolved` событиям, выданным.</span><span class="sxs-lookup"><span data-stu-id="bba2c-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="bba2c-154">Этот логический точкой разрыва будет пережить перезагрузки страниц.</span><span class="sxs-lookup"><span data-stu-id="bba2c-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="bba2c-155">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-155">Parameters</span></span> | <span data-ttu-id="bba2c-156">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-156">Type</span></span> | <span data-ttu-id="bba2c-157">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="bba2c-158">lineNumber</span></span> | `integer` | <span data-ttu-id="bba2c-159">Номер строки для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-159">Line number to set breakpoint at.</span></span> |  
| <span data-ttu-id="bba2c-160">URL\(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-160">url  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-161">URL-адрес ресурсов, на которые необходимо установить точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="bba2c-162">urlRegex \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-162">urlRegex  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-163">Шаблон Regex для URL-адресов ресурсов для набора точек остановок.</span><span class="sxs-lookup"><span data-stu-id="bba2c-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="bba2c-164">Либо `url` необходимо `urlRegex` укаварить.</span><span class="sxs-lookup"><span data-stu-id="bba2c-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="bba2c-165">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-165">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-166">Смещение в строке для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="bba2c-167">условие \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-167">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-168">Выражение для использования в качестве условия breakpoint.</span><span class="sxs-lookup"><span data-stu-id="bba2c-168">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="bba2c-169">Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true.</span><span class="sxs-lookup"><span data-stu-id="bba2c-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="bba2c-170">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bba2c-170">Returns</span></span> | <span data-ttu-id="bba2c-171">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-171">Type</span></span> | <span data-ttu-id="bba2c-172">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-173">breakpointId</span></span> | [<span data-ttu-id="bba2c-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="bba2c-175">ID созданной точки breakpoint для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="bba2c-176">расположения</span><span class="sxs-lookup"><span data-stu-id="bba2c-176">locations</span></span> | [<span data-ttu-id="bba2c-177">Расположение[]</span><span class="sxs-lookup"><span data-stu-id="bba2c-177">Location[]</span></span>](#location) | <span data-ttu-id="bba2c-178">Список местоположений, в которые эта точка взлома была разрешена после добавления.</span><span class="sxs-lookup"><span data-stu-id="bba2c-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="bba2c-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="bba2c-179">setBreakpoint</span></span>  

<span data-ttu-id="bba2c-180">Задает точку разрыва JavaScript в заданное расположение.</span><span class="sxs-lookup"><span data-stu-id="bba2c-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="bba2c-181">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-181">Parameters</span></span> | <span data-ttu-id="bba2c-182">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-182">Type</span></span> | <span data-ttu-id="bba2c-183">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-184">расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-184">location</span></span> | [<span data-ttu-id="bba2c-185">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-185">Location</span></span>](#location) | <span data-ttu-id="bba2c-186">Расположение для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="bba2c-187">условие \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-187">condition  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-188">Выражение для использования в качестве условия breakpoint.</span><span class="sxs-lookup"><span data-stu-id="bba2c-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="bba2c-189">Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true.</span><span class="sxs-lookup"><span data-stu-id="bba2c-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="bba2c-190">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bba2c-190">Returns</span></span> | <span data-ttu-id="bba2c-191">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-191">Type</span></span> | <span data-ttu-id="bba2c-192">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-193">breakpointId</span></span> | [<span data-ttu-id="bba2c-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="bba2c-195">ID созданной точки breakpoint для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="bba2c-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="bba2c-196">actualLocation</span></span> | [<span data-ttu-id="bba2c-197">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-197">Location</span></span>](#location) | <span data-ttu-id="bba2c-198">Расположение этой точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="bba2c-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="bba2c-199">removeBreakpoint</span></span>  

<span data-ttu-id="bba2c-200">Удаляет точку разрыва JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bba2c-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="bba2c-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-201">Parameters</span></span> | <span data-ttu-id="bba2c-202">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-202">Type</span></span> | <span data-ttu-id="bba2c-203">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-204">breakpointId</span></span> | [<span data-ttu-id="bba2c-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="bba2c-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="bba2c-206">stepOver</span></span>  

<span data-ttu-id="bba2c-207">Шаги по заявлению.</span><span class="sxs-lookup"><span data-stu-id="bba2c-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="bba2c-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="bba2c-208">stepInto</span></span>  

<span data-ttu-id="bba2c-209">Шаги в вызов функции.</span><span class="sxs-lookup"><span data-stu-id="bba2c-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="bba2c-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="bba2c-210">stepOut</span></span>  

<span data-ttu-id="bba2c-211">Выход из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="bba2c-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="bba2c-212">pause</span><span class="sxs-lookup"><span data-stu-id="bba2c-212">pause</span></span>  

<span data-ttu-id="bba2c-213">Остановится в следующем заявлении JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bba2c-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="bba2c-214">resume</span><span class="sxs-lookup"><span data-stu-id="bba2c-214">resume</span></span>  

<span data-ttu-id="bba2c-215">Возобновляет выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bba2c-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="bba2c-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="bba2c-216">getScriptSource</span></span>  

<span data-ttu-id="bba2c-217">Возвращает источник для скрипта с заданным ID.</span><span class="sxs-lookup"><span data-stu-id="bba2c-217">Returns source for the script with given ID.</span></span>  

| <span data-ttu-id="bba2c-218">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-218">Parameters</span></span> | <span data-ttu-id="bba2c-219">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-219">Type</span></span> | <span data-ttu-id="bba2c-220">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-221">scriptId</span></span> | [<span data-ttu-id="bba2c-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="bba2c-223">ID скрипта для получения источника.</span><span class="sxs-lookup"><span data-stu-id="bba2c-223">ID of the script to get source for.</span></span> |  
| <span data-ttu-id="bba2c-224">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bba2c-224">Returns</span></span> | <span data-ttu-id="bba2c-225">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-225">Type</span></span> | <span data-ttu-id="bba2c-226">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-226">Details</span></span> |  
|<span data-ttu-id="bba2c-227">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-227">:---</span></span> |<span data-ttu-id="bba2c-228">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-228">:---</span></span> |<span data-ttu-id="bba2c-229">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-229">:---</span></span> |  
| <span data-ttu-id="bba2c-230">scriptSource</span><span class="sxs-lookup"><span data-stu-id="bba2c-230">scriptSource</span></span> | `string` | <span data-ttu-id="bba2c-231">Источник скрипта.</span><span class="sxs-lookup"><span data-stu-id="bba2c-231">Script source.</span></span> |  

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="bba2c-232">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="bba2c-232">setPauseOnExceptions</span></span>  

<span data-ttu-id="bba2c-233">Определяет приостановка состояния исключений.</span><span class="sxs-lookup"><span data-stu-id="bba2c-233">Defines pause on exceptions state.</span></span>  <span data-ttu-id="bba2c-234">Можно запланить остановку на всех исключениях, необученных исключениях или без исключений.</span><span class="sxs-lookup"><span data-stu-id="bba2c-234">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="bba2c-235">Начальная пауза для состояния исключений `none` .</span><span class="sxs-lookup"><span data-stu-id="bba2c-235">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="bba2c-236">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-236">Parameters</span></span> | <span data-ttu-id="bba2c-237">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-237">Type</span></span> | <span data-ttu-id="bba2c-238">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-239">состояние</span><span class="sxs-lookup"><span data-stu-id="bba2c-239">state</span></span> | `string` | <span data-ttu-id="bba2c-240">Пауза в режиме исключений.</span><span class="sxs-lookup"><span data-stu-id="bba2c-240">Pause on exceptions mode.</span></span>  <span data-ttu-id="bba2c-241">Допустимые значения:  `none` `uncaught` и</span><span class="sxs-lookup"><span data-stu-id="bba2c-241">Allowed values:  `none`, `uncaught`, and</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="bba2c-242">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="bba2c-242">evaluateOnCallFrame</span></span>  

<span data-ttu-id="bba2c-243">Оценивает выражение в заданной рамке вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-243">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="bba2c-244">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-244">Parameters</span></span> | <span data-ttu-id="bba2c-245">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-245">Type</span></span> | <span data-ttu-id="bba2c-246">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-246">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-247">callFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-247">callFrameId</span></span> | [<span data-ttu-id="bba2c-248">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-248">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="bba2c-249">Идентификатор кадра вызовов для оценки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-249">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="bba2c-250">выражение</span><span class="sxs-lookup"><span data-stu-id="bba2c-250">expression</span></span> | `string` | <span data-ttu-id="bba2c-251">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-251">Expression to evaluate.</span></span> |  
| <span data-ttu-id="bba2c-252">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bba2c-252">Returns</span></span> | <span data-ttu-id="bba2c-253">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-253">Type</span></span> | <span data-ttu-id="bba2c-254">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-254">Details</span></span> |  
|<span data-ttu-id="bba2c-255">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-255">:---</span></span> |<span data-ttu-id="bba2c-256">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-256">:---</span></span> |<span data-ttu-id="bba2c-257">:---</span><span class="sxs-lookup"><span data-stu-id="bba2c-257">:---</span></span> |  
| <span data-ttu-id="bba2c-258">результат</span><span class="sxs-lookup"><span data-stu-id="bba2c-258">result</span></span> | [<span data-ttu-id="bba2c-259">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="bba2c-259">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="bba2c-260">Объектная оболочка для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-260">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="bba2c-261">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="bba2c-261">setVariableValue</span></span>  

<span data-ttu-id="bba2c-262">Изменяет значение переменной в callframe.</span><span class="sxs-lookup"><span data-stu-id="bba2c-262">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="bba2c-263">Объектные области не поддерживаются и должны мутироваться вручную.</span><span class="sxs-lookup"><span data-stu-id="bba2c-263">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="bba2c-264">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-264">Parameters</span></span> | <span data-ttu-id="bba2c-265">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-265">Type</span></span> | <span data-ttu-id="bba2c-266">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-266">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-267">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="bba2c-267">scopeNumber</span></span> | `integer` | <span data-ttu-id="bba2c-268">0-базирующееся число области, как было перечислены в цепочке области.</span><span class="sxs-lookup"><span data-stu-id="bba2c-268">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="bba2c-269">Разрешены только `local` `closure` типы области и `catch` области.</span><span class="sxs-lookup"><span data-stu-id="bba2c-269">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="bba2c-270">Другими областьми можно управлять вручную.</span><span class="sxs-lookup"><span data-stu-id="bba2c-270">Other scopes could be manipulated manually.</span></span> |  
| <span data-ttu-id="bba2c-271">variableName</span><span class="sxs-lookup"><span data-stu-id="bba2c-271">variableName</span></span> | `string` | <span data-ttu-id="bba2c-272">Переменное имя.</span><span class="sxs-lookup"><span data-stu-id="bba2c-272">Variable name.</span></span> |  
| <span data-ttu-id="bba2c-273">newValue</span><span class="sxs-lookup"><span data-stu-id="bba2c-273">newValue</span></span> | [<span data-ttu-id="bba2c-274">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="bba2c-274">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="bba2c-275">Новое переменная значение.</span><span class="sxs-lookup"><span data-stu-id="bba2c-275">New variable value.</span></span> |  
| <span data-ttu-id="bba2c-276">callFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-276">callFrameId</span></span> | [<span data-ttu-id="bba2c-277">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-277">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="bba2c-278">ID callframe, который содержит переменную.</span><span class="sxs-lookup"><span data-stu-id="bba2c-278">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="bba2c-279">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="bba2c-279">setBlackboxPatterns</span></span>  

<span data-ttu-id="bba2c-280">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-280">**Experimental**.</span></span>  <span data-ttu-id="bba2c-281">Замените предыдущие шаблоны черных ящиков на пройденные.</span><span class="sxs-lookup"><span data-stu-id="bba2c-281">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="bba2c-282">Заставляет отодвигаться, чтобы пропустить шаг/паузу в скриптах с URL-адресом, совпадающий с одним из шаблонов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-282">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="bba2c-283">Отладка будет пытаться оставить черный ящик скрипт, выполняя несколько `step in` раз, наконец, прибегая `step out` к, если неудачно.</span><span class="sxs-lookup"><span data-stu-id="bba2c-283">The debugger will try to leave blackboxed script by performing `step in` several times, finally resorting to `step out` if unsuccessful.</span></span>  

| <span data-ttu-id="bba2c-284">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-284">Parameters</span></span> | <span data-ttu-id="bba2c-285">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-285">Type</span></span> | <span data-ttu-id="bba2c-286">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-286">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-287">шаблоны</span><span class="sxs-lookup"><span data-stu-id="bba2c-287">patterns</span></span> | `string[]` | <span data-ttu-id="bba2c-288">Массив regexps, который будет использоваться для проверки URL-адреса скрипта для состояния blackbox.</span><span class="sxs-lookup"><span data-stu-id="bba2c-288">Array of regexps that will be used to check script url for blackbox state.</span></span> |  

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="bba2c-289">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="bba2c-289">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="bba2c-290">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-290">**Experimental**.</span></span>  <span data-ttu-id="bba2c-291">Microsoft. Задает указанное свойство отладки указанному значению.</span><span class="sxs-lookup"><span data-stu-id="bba2c-291">Microsoft:  Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="bba2c-292">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-292">Parameters</span></span> | <span data-ttu-id="bba2c-293">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-293">Type</span></span> | <span data-ttu-id="bba2c-294">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-294">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-295">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="bba2c-295">debuggerPropertyId</span></span> | `string` | <span data-ttu-id="bba2c-296">Microsoft. ID свойства \(например, msDebuggerPropertyId\) для набора.</span><span class="sxs-lookup"><span data-stu-id="bba2c-296">Microsoft: The property ID \(i.e. msDebuggerPropertyId\) to set.</span></span> |  
| <span data-ttu-id="bba2c-297">newValue</span><span class="sxs-lookup"><span data-stu-id="bba2c-297">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="bba2c-298">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="bba2c-298">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="bba2c-299">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="bba2c-299">scriptParsed</span></span>  

<span data-ttu-id="bba2c-300">Уволено при размыве сценария.</span><span class="sxs-lookup"><span data-stu-id="bba2c-300">Fired when the script is parsed.</span></span>  <span data-ttu-id="bba2c-301">Это событие также будет уволено для всех известных и неиспользванных скриптов при включив отладку.</span><span class="sxs-lookup"><span data-stu-id="bba2c-301">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="bba2c-302">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-302">Parameters</span></span> | <span data-ttu-id="bba2c-303">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-303">Type</span></span> | <span data-ttu-id="bba2c-304">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-304">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-305">scriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-305">scriptId</span></span> | [<span data-ttu-id="bba2c-306">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-306">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="bba2c-307">Идентификатор размыкаемого скрипта.</span><span class="sxs-lookup"><span data-stu-id="bba2c-307">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="bba2c-308">url</span><span class="sxs-lookup"><span data-stu-id="bba2c-308">url</span></span> | `string` | <span data-ttu-id="bba2c-309">URL-адрес или имя разбияемого скрипта \(если таково\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-309">URL or name of the script parsed \(if any\).</span></span> |  
| <span data-ttu-id="bba2c-310">startLine</span><span class="sxs-lookup"><span data-stu-id="bba2c-310">startLine</span></span> | `integer` | <span data-ttu-id="bba2c-311">Строка смещения скрипта в ресурсе с заданным URL-адресом \(для тегов скрипта\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-311">Line offset of the script within the resource with given URL \(for script tags\).</span></span> |  
| <span data-ttu-id="bba2c-312">startColumn</span><span class="sxs-lookup"><span data-stu-id="bba2c-312">startColumn</span></span> | `integer` | <span data-ttu-id="bba2c-313">Столбец смещения скрипта в ресурсе с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="bba2c-313">Column offset of the script within the resource with given URL.</span></span> |  
| <span data-ttu-id="bba2c-314">endLine</span><span class="sxs-lookup"><span data-stu-id="bba2c-314">endLine</span></span> | `integer` | <span data-ttu-id="bba2c-315">Последняя строка сценария.</span><span class="sxs-lookup"><span data-stu-id="bba2c-315">Last line of the script.</span></span> |  
| <span data-ttu-id="bba2c-316">endColumn</span><span class="sxs-lookup"><span data-stu-id="bba2c-316">endColumn</span></span> | `integer` | <span data-ttu-id="bba2c-317">Длина последней строки сценария.</span><span class="sxs-lookup"><span data-stu-id="bba2c-317">Length of the last line of the script.</span></span> |  
| <span data-ttu-id="bba2c-318">executionContextId</span><span class="sxs-lookup"><span data-stu-id="bba2c-318">executionContextId</span></span> | [<span data-ttu-id="bba2c-319">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="bba2c-319">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="bba2c-320">Указывает контекст создания скрипта.</span><span class="sxs-lookup"><span data-stu-id="bba2c-320">Specifies script creation context.</span></span> |  
| <span data-ttu-id="bba2c-321">sourceMapURL \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-321">sourceMapURL  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-322">URL-адрес исходных карт, связанных со сценарием (если таково).</span><span class="sxs-lookup"><span data-stu-id="bba2c-322">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="bba2c-323">длина \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-323">length  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-324">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-324">**Experimental**.</span></span>  <span data-ttu-id="bba2c-325">Длина скрипта.</span><span class="sxs-lookup"><span data-stu-id="bba2c-325">This script length.</span></span> |  
| <span data-ttu-id="bba2c-326">msParentId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-326">msParentId  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-327">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-327">**Experimental**.</span></span>  <span data-ttu-id="bba2c-328">Это родительский документ.</span><span class="sxs-lookup"><span data-stu-id="bba2c-328">This is the parent document ID.</span></span> |  
| <span data-ttu-id="bba2c-329">msMimeType \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-329">msMimeType  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-330">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-330">**Experimental**.</span></span>  <span data-ttu-id="bba2c-331">Это тип mime.</span><span class="sxs-lookup"><span data-stu-id="bba2c-331">This is the mime type.</span></span> |  
| <span data-ttu-id="bba2c-332">msIsDynamicCode \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-332">msIsDynamicCode  \(optional\)</span></span> | `boolean` | <span data-ttu-id="bba2c-333">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-333">**Experimental**.</span></span>  <span data-ttu-id="bba2c-334">Это указывает, является ли это динамический код.</span><span class="sxs-lookup"><span data-stu-id="bba2c-334">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="bba2c-335">msLongDocumentId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-335">msLongDocumentId  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-336">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-336">**Experimental**.</span></span>  <span data-ttu-id="bba2c-337">Это длинный документ.</span><span class="sxs-lookup"><span data-stu-id="bba2c-337">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="bba2c-338">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="bba2c-338">breakpointResolved</span></span>  

<span data-ttu-id="bba2c-339">В случае, если точка разрыва будет разрешена к фактическому сценарию и расположению.</span><span class="sxs-lookup"><span data-stu-id="bba2c-339">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="bba2c-340">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-340">Parameters</span></span> | <span data-ttu-id="bba2c-341">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-341">Type</span></span> | <span data-ttu-id="bba2c-342">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-342">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-343">breakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-343">breakpointId</span></span> | [<span data-ttu-id="bba2c-344">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-344">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="bba2c-345">Уникальный идентификатор Breakpoint.</span><span class="sxs-lookup"><span data-stu-id="bba2c-345">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="bba2c-346">расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-346">location</span></span> | [<span data-ttu-id="bba2c-347">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-347">Location</span></span>](#location) | <span data-ttu-id="bba2c-348">Фактическое расположение точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-348">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="bba2c-349">msLength \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-349">msLength  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-350">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-350">**Experimental**.</span></span>  <span data-ttu-id="bba2c-351">Microsoft. Длина кода \(то есть количество символов\) в расположении точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="bba2c-351">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="bba2c-352">пауза</span><span class="sxs-lookup"><span data-stu-id="bba2c-352">paused</span></span>  

<span data-ttu-id="bba2c-353">Уволено, когда отладки ломаются для точки разлома или исключения.</span><span class="sxs-lookup"><span data-stu-id="bba2c-353">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="bba2c-354">Параметры</span><span class="sxs-lookup"><span data-stu-id="bba2c-354">Parameters</span></span> | <span data-ttu-id="bba2c-355">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-355">Type</span></span> | <span data-ttu-id="bba2c-356">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-356">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-357">callFrames</span><span class="sxs-lookup"><span data-stu-id="bba2c-357">callFrames</span></span> | [<span data-ttu-id="bba2c-358">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="bba2c-358">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="bba2c-359">Вызов стек отладки остановился.</span><span class="sxs-lookup"><span data-stu-id="bba2c-359">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="bba2c-360">причина</span><span class="sxs-lookup"><span data-stu-id="bba2c-360">reason</span></span> | `string` | <span data-ttu-id="bba2c-361">Причина паузы.</span><span class="sxs-lookup"><span data-stu-id="bba2c-361">Pause reason.</span></span>  <span data-ttu-id="bba2c-362">Допустимые значения:  `breakpoint` `step` , `exception` и</span><span class="sxs-lookup"><span data-stu-id="bba2c-362">Allowed values:  `breakpoint`, `step`, `exception`, and</span></span> `other` |  
| <span data-ttu-id="bba2c-363">данные \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-363">data  \(optional\)</span></span> | `object` | <span data-ttu-id="bba2c-364">Объект, содержащий отдельные вспомогательные свойства.</span><span class="sxs-lookup"><span data-stu-id="bba2c-364">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="bba2c-365">hitBreakpoints \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-365">hitBreakpoints  \(optional\)</span></span> | `string[]` | <span data-ttu-id="bba2c-366">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="bba2c-366">Hit breakpoints IDs</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="bba2c-367">возобновлено</span><span class="sxs-lookup"><span data-stu-id="bba2c-367">resumed</span></span>  

<span data-ttu-id="bba2c-368">Уволили, когда отладка возобновляет выполнение.</span><span class="sxs-lookup"><span data-stu-id="bba2c-368">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="bba2c-369">Типы</span><span class="sxs-lookup"><span data-stu-id="bba2c-369">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="bba2c-370">Строка BreakpointId</span><span class="sxs-lookup"><span data-stu-id="bba2c-370">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="bba2c-371">Идентификатор Breakpoint.</span><span class="sxs-lookup"><span data-stu-id="bba2c-371">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="bba2c-372">Строка CallFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-372">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="bba2c-373">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="bba2c-373">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="bba2c-374">Объект Location</span><span class="sxs-lookup"><span data-stu-id="bba2c-374">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="bba2c-375">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="bba2c-375">Location in the source code.</span></span>  

| <span data-ttu-id="bba2c-376">Свойства</span><span class="sxs-lookup"><span data-stu-id="bba2c-376">Properties</span></span> | <span data-ttu-id="bba2c-377">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-377">Type</span></span> | <span data-ttu-id="bba2c-378">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-378">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-379">scriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-379">scriptId</span></span> | [<span data-ttu-id="bba2c-380">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-380">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="bba2c-381">Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="bba2c-381">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="bba2c-382">lineNumber</span><span class="sxs-lookup"><span data-stu-id="bba2c-382">lineNumber</span></span> | `integer` | <span data-ttu-id="bba2c-383">Номер строки в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-383">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="bba2c-384">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-384">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-385">Номер столбца в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-385">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="bba2c-386">msLength</span><span class="sxs-lookup"><span data-stu-id="bba2c-386">msLength</span></span> | `integer` | <span data-ttu-id="bba2c-387">Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-387">Microsoft: Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="bba2c-388">Объект BreakLocation</span><span class="sxs-lookup"><span data-stu-id="bba2c-388">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="bba2c-389">Разорвать расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="bba2c-389">Break location in the source code.</span></span>  

| <span data-ttu-id="bba2c-390">Свойства</span><span class="sxs-lookup"><span data-stu-id="bba2c-390">Properties</span></span> | <span data-ttu-id="bba2c-391">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-391">Type</span></span> | <span data-ttu-id="bba2c-392">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-392">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-393">scriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-393">scriptId</span></span> | [<span data-ttu-id="bba2c-394">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="bba2c-394">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="bba2c-395">Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="bba2c-395">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="bba2c-396">lineNumber</span><span class="sxs-lookup"><span data-stu-id="bba2c-396">lineNumber</span></span> | `integer` | <span data-ttu-id="bba2c-397">Номер строки в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-397">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="bba2c-398">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-398">columnNumber  \(optional\)</span></span> | `integer` | <span data-ttu-id="bba2c-399">Номер столбца в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="bba2c-399">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="bba2c-400">msLength</span><span class="sxs-lookup"><span data-stu-id="bba2c-400">msLength</span></span> | `integer` | <span data-ttu-id="bba2c-401">Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-401">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="bba2c-402">тип \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-402">type  \(optional\)</span></span> | `string` | <span data-ttu-id="bba2c-403">Допустимые значения:  `debuggerStatement` `call` и</span><span class="sxs-lookup"><span data-stu-id="bba2c-403">Allowed values:  `debuggerStatement`, `call`, and</span></span> `return` |  

---  

### <a name="callframe-object"></a><span data-ttu-id="bba2c-404">Объект CallFrame</span><span class="sxs-lookup"><span data-stu-id="bba2c-404">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="bba2c-405">Кадр вызова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bba2c-405">JavaScript call frame.</span></span>  <span data-ttu-id="bba2c-406">Массив кадров вызовов формирует стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-406">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="bba2c-407">Свойства</span><span class="sxs-lookup"><span data-stu-id="bba2c-407">Properties</span></span> | <span data-ttu-id="bba2c-408">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-408">Type</span></span> | <span data-ttu-id="bba2c-409">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-409">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-410">callFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-410">callFrameId</span></span> | [<span data-ttu-id="bba2c-411">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="bba2c-411">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="bba2c-412">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="bba2c-412">Call frame identifier.</span></span>  <span data-ttu-id="bba2c-413">Этот идентификатор действителен только во время паузы отладки.</span><span class="sxs-lookup"><span data-stu-id="bba2c-413">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="bba2c-414">functionName</span><span class="sxs-lookup"><span data-stu-id="bba2c-414">functionName</span></span> | `string` | <span data-ttu-id="bba2c-415">Имя функции JavaScript, вызываемой в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-415">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="bba2c-416">functionLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-416">functionLocation  \(optional\)</span></span> | [<span data-ttu-id="bba2c-417">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-417">Location</span></span>](#location) | <span data-ttu-id="bba2c-418">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="bba2c-418">**Experimental**.</span></span>  <span data-ttu-id="bba2c-419">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="bba2c-419">Location in the source code.</span></span> |  
| <span data-ttu-id="bba2c-420">расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-420">location</span></span> | [<span data-ttu-id="bba2c-421">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-421">Location</span></span>](#location) | <span data-ttu-id="bba2c-422">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="bba2c-422">Location in the source code.</span></span> |  
| <span data-ttu-id="bba2c-423">url</span><span class="sxs-lookup"><span data-stu-id="bba2c-423">url</span></span> | `string` | <span data-ttu-id="bba2c-424">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="bba2c-424">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="bba2c-425">scopeChain</span><span class="sxs-lookup"><span data-stu-id="bba2c-425">scopeChain</span></span> | [<span data-ttu-id="bba2c-426">Область[]</span><span class="sxs-lookup"><span data-stu-id="bba2c-426">Scope[]</span></span>](#scope) | <span data-ttu-id="bba2c-427">Цепочка области для этого кадра вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-427">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="bba2c-428">это</span><span class="sxs-lookup"><span data-stu-id="bba2c-428">this</span></span> | [<span data-ttu-id="bba2c-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="bba2c-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="bba2c-430">объект для этого кадра вызовов.</span><span class="sxs-lookup"><span data-stu-id="bba2c-430">object for this call frame.</span></span> |  
| <span data-ttu-id="bba2c-431">returnValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-431">returnValue  \(optional\)</span></span> | [<span data-ttu-id="bba2c-432">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="bba2c-432">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="bba2c-433">Возвращаемая величина, если функция находится в точке возврата.</span><span class="sxs-lookup"><span data-stu-id="bba2c-433">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="bba2c-434">Объект Scope</span><span class="sxs-lookup"><span data-stu-id="bba2c-434">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="bba2c-435">Описание области.</span><span class="sxs-lookup"><span data-stu-id="bba2c-435">Scope description.</span></span>  

| <span data-ttu-id="bba2c-436">Свойства</span><span class="sxs-lookup"><span data-stu-id="bba2c-436">Properties</span></span> | <span data-ttu-id="bba2c-437">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-437">Type</span></span> | <span data-ttu-id="bba2c-438">Сведения</span><span class="sxs-lookup"><span data-stu-id="bba2c-438">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="bba2c-439">Тип</span><span class="sxs-lookup"><span data-stu-id="bba2c-439">type</span></span> | `string` | <span data-ttu-id="bba2c-440">Тип области.</span><span class="sxs-lookup"><span data-stu-id="bba2c-440">Scope type.</span></span>  <span data-ttu-id="bba2c-441">Допустимые значения: `global` , , , , , , `local` `with` `closure` `catch` `block` `script` и `eval`</span><span class="sxs-lookup"><span data-stu-id="bba2c-441">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, and</span></span> `module` |  
| <span data-ttu-id="bba2c-442">объект</span><span class="sxs-lookup"><span data-stu-id="bba2c-442">object</span></span> | [<span data-ttu-id="bba2c-443">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="bba2c-443">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="bba2c-444">Объект, представляющий область.</span><span class="sxs-lookup"><span data-stu-id="bba2c-444">Object representing the scope.</span></span>  <span data-ttu-id="bba2c-445">Для и областей он представляет фактический объект; для остальных областей это искусственный переходный объект, который в качестве свойств передает переменные `global` `with` области.</span><span class="sxs-lookup"><span data-stu-id="bba2c-445">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="bba2c-446">имя \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-446">name  \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="bba2c-447">startLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-447">startLocation  \(optional\)</span></span> | [<span data-ttu-id="bba2c-448">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-448">Location</span></span>](#location) | <span data-ttu-id="bba2c-449">Расположение в исходный код, где начинается область.</span><span class="sxs-lookup"><span data-stu-id="bba2c-449">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="bba2c-450">endLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="bba2c-450">endLocation  \(optional\)</span></span> | [<span data-ttu-id="bba2c-451">Расположение</span><span class="sxs-lookup"><span data-stu-id="bba2c-451">Location</span></span>](#location) | <span data-ttu-id="bba2c-452">Расположение в исходный код, где область заканчивается.</span><span class="sxs-lookup"><span data-stu-id="bba2c-452">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="bba2c-453">Зависимости</span><span class="sxs-lookup"><span data-stu-id="bba2c-453">Dependencies</span></span>  

[<span data-ttu-id="bba2c-454">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="bba2c-454">Runtime</span></span>](./runtime.md)  
