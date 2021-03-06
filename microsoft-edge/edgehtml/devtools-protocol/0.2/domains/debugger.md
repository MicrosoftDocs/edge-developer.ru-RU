---
description: Ссылка на протокол DevTools Версии 0.2 (EdgeHTML) для домена Debugger. Домен Debugger предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.
title: Домен Debugger — протокол DevTools Версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398177"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="e1ef3-105">Домен Debugger — протокол DevTools Версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-105">Debugger Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="e1ef3-106">Домен Debugger предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-106">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="e1ef3-107">Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-107">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>

| <span data-ttu-id="e1ef3-108">Категория</span><span class="sxs-lookup"><span data-stu-id="e1ef3-108">Classification</span></span> | <span data-ttu-id="e1ef3-109">Участники</span><span class="sxs-lookup"><span data-stu-id="e1ef3-109">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="e1ef3-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e1ef3-110">Methods</span></span>**](#methods) | <span data-ttu-id="e1ef3-111">[включить](#enable), отключить [,](#disable) [getPossibleBreakpoints](#getpossiblebreakpoints), [](#resume) [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), setBreakpoint , [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [](#setbreakpoint) [пауза](#pause), резюме , [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [оценкаOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-111">[enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue)</span></span> |  
| [**<span data-ttu-id="e1ef3-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="e1ef3-112">Events</span></span>**](#events) | <span data-ttu-id="e1ef3-113">[scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [paused](#paused), [resumed](#resumed)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-113">[scriptParsed](#scriptparsed), [breakpointResolved](#breakpointresolved), [paused](#paused), [resumed](#resumed)</span></span> |  
| [**<span data-ttu-id="e1ef3-114">Типы</span><span class="sxs-lookup"><span data-stu-id="e1ef3-114">Types</span></span>**](#types) | <span data-ttu-id="e1ef3-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Расположение](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Область](#scope)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-115">[BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope)</span></span> |  
| [**<span data-ttu-id="e1ef3-116">Зависимости</span><span class="sxs-lookup"><span data-stu-id="e1ef3-116">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="e1ef3-117">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-117">Runtime</span></span>](./runtime.md) |  

## <a name="methods"></a><span data-ttu-id="e1ef3-118">Методы</span><span class="sxs-lookup"><span data-stu-id="e1ef3-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="e1ef3-119">"Включить"</span><span class="sxs-lookup"><span data-stu-id="e1ef3-119">enable</span></span>  

<span data-ttu-id="e1ef3-120">Включает отладка для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-120">Enables debugger for the given page.</span></span> <span data-ttu-id="e1ef3-121">Клиенты не должны предполагать, что отладка включена до тех пор, пока не будет получен результат для этой команды.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-121">Clients should not assume that the debugging has been enabled until the result for this command is received.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="e1ef3-122">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="e1ef3-122">disable</span></span>  

<span data-ttu-id="e1ef3-123">Отладка отладки для данной страницы.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-123">Disables debugger for given page.</span></span>  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a><span data-ttu-id="e1ef3-124">getPossibleBreakpoints</span><span class="sxs-lookup"><span data-stu-id="e1ef3-124">getPossibleBreakpoints</span></span>  

<span data-ttu-id="e1ef3-125">Возвращает возможные расположения для breakpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-125">Returns possible locations for breakpoint.</span></span> <span data-ttu-id="e1ef3-126">ScriptId в расположениях старта и конца диапазона должен быть одинаковым.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-126">scriptId in start and end range locations should be the same.</span></span>  

| <span data-ttu-id="e1ef3-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-127">Parameters</span></span> | <span data-ttu-id="e1ef3-128">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-128">Type</span></span> | <span data-ttu-id="e1ef3-129">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-129">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-130">start</span><span class="sxs-lookup"><span data-stu-id="e1ef3-130">start</span></span> | [<span data-ttu-id="e1ef3-131">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-131">Location</span></span>](#location) | <span data-ttu-id="e1ef3-132">Начало диапазона для поиска возможных точек разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-132">Start of range to search possible breakpoint locations in.</span></span> |  
| <span data-ttu-id="e1ef3-133">завершить</span><span class="sxs-lookup"><span data-stu-id="e1ef3-133">end</span></span> | [<span data-ttu-id="e1ef3-134">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-134">Location</span></span>](#location) | <span data-ttu-id="e1ef3-135">Конец диапазона для поиска возможных точек разрыва в \(excluding\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-135">End of range to search possible breakpoint locations in \(excluding\).</span></span>  <span data-ttu-id="e1ef3-136">Если не указано, конец скриптов используется как конец диапазона.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-136">When not specified, end of scripts is used as end of range.</span></span> |  

| <span data-ttu-id="e1ef3-137">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e1ef3-137">Returns</span></span> | <span data-ttu-id="e1ef3-138">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-138">Type</span></span> | <span data-ttu-id="e1ef3-139">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-139">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-140">расположения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-140">locations</span></span> | [<span data-ttu-id="e1ef3-141">BreakLocation</span><span class="sxs-lookup"><span data-stu-id="e1ef3-141">BreakLocation</span></span>](#breaklocation) | <span data-ttu-id="e1ef3-142">Список возможных местоположений точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-142">List of the possible breakpoint locations.</span></span> |  

---  

### <a name="setbreakpointsactive"></a><span data-ttu-id="e1ef3-143">setBreakpointsActive</span><span class="sxs-lookup"><span data-stu-id="e1ef3-143">setBreakpointsActive</span></span>  

<span data-ttu-id="e1ef3-144">Активирует или отключает все точки взлома на странице.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-144">Activates / deactivates all breakpoints on the page.</span></span>  

| <span data-ttu-id="e1ef3-145">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-145">Parameters</span></span> | <span data-ttu-id="e1ef3-146">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-146">Type</span></span> | <span data-ttu-id="e1ef3-147">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-147">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-148">active</span><span class="sxs-lookup"><span data-stu-id="e1ef3-148">active</span></span> | `boolean` | <span data-ttu-id="e1ef3-149">Новое значение для активного состояния точек breakpoints.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-149">New value for breakpoints active state.</span></span> | 

---  

### <a name="setbreakpointbyurl"></a><span data-ttu-id="e1ef3-150">setBreakpointByUrl</span><span class="sxs-lookup"><span data-stu-id="e1ef3-150">setBreakpointByUrl</span></span>  

<span data-ttu-id="e1ef3-151">Задает точку разрыва JavaScript в указанном расположении, указанном URL-адресом или URL-адресом regex.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-151">Sets JavaScript breakpoint at given location specified either by URL or URL regex.</span></span>  <span data-ttu-id="e1ef3-152">После того как эта команда будет выдана, все существующие разбиенные сценарии будут иметь точки разрывов, разрешенные и возвращенные в `locations` свойстве.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-152">Once this command is issued, all existing parsed scripts will have breakpoints resolved and returned in `locations` property.</span></span>  <span data-ttu-id="e1ef3-153">Дальнейшее соответствие размыву сценариев приведет к последующим `breakpointResolved` событиям, выданным.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-153">Further matching script parsing will result in subsequent `breakpointResolved` events issued.</span></span>  <span data-ttu-id="e1ef3-154">Этот логический точкой разрыва будет пережить перезагрузки страниц.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-154">This logical breakpoint will survive page reloads.</span></span>  

| <span data-ttu-id="e1ef3-155">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-155">Parameters</span></span> | <span data-ttu-id="e1ef3-156">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-156">Type</span></span> | <span data-ttu-id="e1ef3-157">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-158">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e1ef3-158">lineNumber</span></span> | `integer` | <span data-ttu-id="e1ef3-159">Номер строки для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-159">Line number to set breakpoint at.</span></span> | 
| <span data-ttu-id="e1ef3-160">URL\(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-160">url \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-161">URL-адрес ресурсов, на которые необходимо установить точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-161">URL of the resources to set breakpoint on.</span></span> |  
| <span data-ttu-id="e1ef3-162">urlRegex \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-162">urlRegex \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-163">Шаблон Regex для URL-адресов ресурсов для набора точек остановок.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-163">Regex pattern for the URLs of the resources to set breakpoints on.</span></span>  <span data-ttu-id="e1ef3-164">Либо `url` необходимо `urlRegex` укаварить.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-164">Either `url` or `urlRegex` must be specified.</span></span> |  
| <span data-ttu-id="e1ef3-165">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-165">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-166">Смещение в строке для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-166">Offset in the line to set breakpoint at.</span></span> |  
| <span data-ttu-id="e1ef3-167">условие \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-167">condition \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-168">Выражение для использования в качестве условия breakpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-168">Expression to use as a breakpoint condition.</span></span> <span data-ttu-id="e1ef3-169">Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-169">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="e1ef3-170">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e1ef3-170">Returns</span></span> | <span data-ttu-id="e1ef3-171">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-171">Type</span></span> | <span data-ttu-id="e1ef3-172">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-172">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-173">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-173">breakpointId</span></span> | [<span data-ttu-id="e1ef3-174">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-174">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e1ef3-175">ID созданной точки breakpoint для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-175">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="e1ef3-176">расположения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-176">locations</span></span> | [<span data-ttu-id="e1ef3-177">Расположение[]</span><span class="sxs-lookup"><span data-stu-id="e1ef3-177">Location[]</span></span>](#location) | <span data-ttu-id="e1ef3-178">Список местоположений, в которые эта точка взлома была разрешена после добавления.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-178">List of the locations this breakpoint resolved into upon addition.</span></span> |  

---  

### <a name="setbreakpoint"></a><span data-ttu-id="e1ef3-179">setBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e1ef3-179">setBreakpoint</span></span>  

<span data-ttu-id="e1ef3-180">Задает точку разрыва JavaScript в заданное расположение.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-180">Sets JavaScript breakpoint at a given location.</span></span>  

| <span data-ttu-id="e1ef3-181">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-181">Parameters</span></span> | <span data-ttu-id="e1ef3-182">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-182">Type</span></span> | <span data-ttu-id="e1ef3-183">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-183">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-184">расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-184">location</span></span> | [<span data-ttu-id="e1ef3-185">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-185">Location</span></span>](#location) | <span data-ttu-id="e1ef3-186">Расположение для набора точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-186">Location to set breakpoint in.</span></span> |  
| <span data-ttu-id="e1ef3-187">условие \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-187">condition \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-188">Выражение для использования в качестве условия breakpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-188">Expression to use as a breakpoint condition.</span></span>  <span data-ttu-id="e1ef3-189">Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-189">When specified, debugger will only stop on the breakpoint if this expression evaluates to true.</span></span> |  

| <span data-ttu-id="e1ef3-190">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e1ef3-190">Returns</span></span> | <span data-ttu-id="e1ef3-191">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-191">Type</span></span> | <span data-ttu-id="e1ef3-192">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-192">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-193">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-193">breakpointId</span></span> | [<span data-ttu-id="e1ef3-194">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-194">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e1ef3-195">ID созданной точки breakpoint для дальнейшей ссылки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-195">ID of the created breakpoint for further reference.</span></span> |  
| <span data-ttu-id="e1ef3-196">actualLocation</span><span class="sxs-lookup"><span data-stu-id="e1ef3-196">actualLocation</span></span> | [<span data-ttu-id="e1ef3-197">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-197">Location</span></span>](#location) | <span data-ttu-id="e1ef3-198">Расположение этой точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-198">Location this breakpoint resolved into.</span></span> |  

---  

### <a name="removebreakpoint"></a><span data-ttu-id="e1ef3-199">removeBreakpoint</span><span class="sxs-lookup"><span data-stu-id="e1ef3-199">removeBreakpoint</span></span>  

<span data-ttu-id="e1ef3-200">Удаляет точку разрыва JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-200">Removes JavaScript breakpoint.</span></span>  

| <span data-ttu-id="e1ef3-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-201">Parameters</span></span> | <span data-ttu-id="e1ef3-202">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-202">Type</span></span> | <span data-ttu-id="e1ef3-203">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-204">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-204">breakpointId</span></span> | [<span data-ttu-id="e1ef3-205">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-205">BreakpointId</span></span>](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a><span data-ttu-id="e1ef3-206">stepOver</span><span class="sxs-lookup"><span data-stu-id="e1ef3-206">stepOver</span></span>  

<span data-ttu-id="e1ef3-207">Шаги по заявлению.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-207">Steps over the statement.</span></span>  

&nbsp;  

---  

### <a name="stepinto"></a><span data-ttu-id="e1ef3-208">stepInto</span><span class="sxs-lookup"><span data-stu-id="e1ef3-208">stepInto</span></span>  

<span data-ttu-id="e1ef3-209">Шаги в вызов функции.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-209">Steps into the function call.</span></span>  

&nbsp;  

---  

### <a name="stepout"></a><span data-ttu-id="e1ef3-210">stepOut</span><span class="sxs-lookup"><span data-stu-id="e1ef3-210">stepOut</span></span>  

<span data-ttu-id="e1ef3-211">Выход из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-211">Steps out of the function call.</span></span>  

&nbsp;  

---  

### <a name="pause"></a><span data-ttu-id="e1ef3-212">pause</span><span class="sxs-lookup"><span data-stu-id="e1ef3-212">pause</span></span>  

<span data-ttu-id="e1ef3-213">Остановится в следующем заявлении JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-213">Stops on the next JavaScript statement.</span></span>  

&nbsp;  

---  

### <a name="resume"></a><span data-ttu-id="e1ef3-214">resume</span><span class="sxs-lookup"><span data-stu-id="e1ef3-214">resume</span></span>  

<span data-ttu-id="e1ef3-215">Возобновляет выполнение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-215">Resumes JavaScript execution.</span></span>  

&nbsp;  

---  

### <a name="getscriptsource"></a><span data-ttu-id="e1ef3-216">getScriptSource</span><span class="sxs-lookup"><span data-stu-id="e1ef3-216">getScriptSource</span></span>  

<span data-ttu-id="e1ef3-217">Возвращает источник для скрипта с данным id.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-217">Returns source for the script with given id.</span></span>  

| <span data-ttu-id="e1ef3-218">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-218">Parameters</span></span> | <span data-ttu-id="e1ef3-219">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-219">Type</span></span> | <span data-ttu-id="e1ef3-220">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-220">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-221">scriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-221">scriptId</span></span> | [<span data-ttu-id="e1ef3-222">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-222">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e1ef3-223">ID скрипта для получения источника.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-223">ID of the script to get source for.</span></span> |  

| <span data-ttu-id="e1ef3-224">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e1ef3-224">Returns</span></span> | <span data-ttu-id="e1ef3-225">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-225">Type</span></span> | <span data-ttu-id="e1ef3-226">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-226">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-227">scriptSource</span><span class="sxs-lookup"><span data-stu-id="e1ef3-227">scriptSource</span></span> | `string` | <span data-ttu-id="e1ef3-228">Источник скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-228">Script source.</span></span> | 

---  

### <a name="setpauseonexceptions"></a><span data-ttu-id="e1ef3-229">setPauseOnExceptions</span><span class="sxs-lookup"><span data-stu-id="e1ef3-229">setPauseOnExceptions</span></span>  

<span data-ttu-id="e1ef3-230">Определяет приостановка состояния исключений.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-230">Defines pause on exceptions state.</span></span>  <span data-ttu-id="e1ef3-231">Можно запланить остановку на всех исключениях, необученных исключениях или без исключений.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-231">Can be set to stop on all exceptions, uncaught exceptions or no exceptions.</span></span>  <span data-ttu-id="e1ef3-232">Начальная пауза для состояния исключений `none` .</span><span class="sxs-lookup"><span data-stu-id="e1ef3-232">Initial pause on exceptions state is `none`.</span></span>  

| <span data-ttu-id="e1ef3-233">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-233">Parameters</span></span> | <span data-ttu-id="e1ef3-234">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-234">Type</span></span> | <span data-ttu-id="e1ef3-235">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-235">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-236">состояние</span><span class="sxs-lookup"><span data-stu-id="e1ef3-236">state</span></span> | `string` | <span data-ttu-id="e1ef3-237">Пауза в режиме исключений.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-237">Pause on exceptions mode.</span></span>  <span data-ttu-id="e1ef3-238">Допустимые значения:  `none` `uncaught` ,</span><span class="sxs-lookup"><span data-stu-id="e1ef3-238">Allowed values:  `none`, `uncaught`,</span></span> `all` |  

---  

### <a name="evaluateoncallframe"></a><span data-ttu-id="e1ef3-239">evaluateOnCallFrame</span><span class="sxs-lookup"><span data-stu-id="e1ef3-239">evaluateOnCallFrame</span></span>  

<span data-ttu-id="e1ef3-240">Оценивает выражение в заданной рамке вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-240">Evaluates expression on a given call frame.</span></span>  

| <span data-ttu-id="e1ef3-241">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-241">Parameters</span></span> | <span data-ttu-id="e1ef3-242">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-242">Type</span></span> | <span data-ttu-id="e1ef3-243">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-243">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-244">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-244">callFrameId</span></span> | [<span data-ttu-id="e1ef3-245">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-245">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e1ef3-246">Идентификатор кадра вызовов для оценки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-246">Call frame identifier to evaluate on.</span></span> |  
| <span data-ttu-id="e1ef3-247">выражение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-247">expression</span></span> | `string` | <span data-ttu-id="e1ef3-248">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-248">Expression to evaluate.</span></span> | 

| <span data-ttu-id="e1ef3-249">Возвращает</span><span class="sxs-lookup"><span data-stu-id="e1ef3-249">Returns</span></span> | <span data-ttu-id="e1ef3-250">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-250">Type</span></span> | <span data-ttu-id="e1ef3-251">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-251">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-252">результат</span><span class="sxs-lookup"><span data-stu-id="e1ef3-252">result</span></span> | [<span data-ttu-id="e1ef3-253">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e1ef3-253">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e1ef3-254">Объектная оболочка для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-254">Object wrapper for the evaluation result.</span></span> |  

---  

### <a name="setvariablevalue"></a><span data-ttu-id="e1ef3-255">setVariableValue</span><span class="sxs-lookup"><span data-stu-id="e1ef3-255">setVariableValue</span></span>  

<span data-ttu-id="e1ef3-256">Изменяет значение переменной в callframe.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-256">Changes value of variable in a callframe.</span></span>  <span data-ttu-id="e1ef3-257">Объектные области не поддерживаются и должны мутироваться вручную.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-257">Object-based scopes are not supported and must be mutated manually.</span></span>  

| <span data-ttu-id="e1ef3-258">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-258">Parameters</span></span> | <span data-ttu-id="e1ef3-259">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-259">Type</span></span> | <span data-ttu-id="e1ef3-260">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-260">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-261">scopeNumber</span><span class="sxs-lookup"><span data-stu-id="e1ef3-261">scopeNumber</span></span> | `integer` | <span data-ttu-id="e1ef3-262">0-базирующееся число области, как было перечислены в цепочке области.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-262">0-based number of scope as was listed in scope chain.</span></span>  <span data-ttu-id="e1ef3-263">Разрешены только `local` `closure` типы области и `catch` области.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-263">Only `local`, `closure`, and `catch` scope types are allowed.</span></span>  <span data-ttu-id="e1ef3-264">Другими областьми можно управлять вручную.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-264">Other scopes could be manipulated manually.</span></span> | 
| <span data-ttu-id="e1ef3-265">variableName</span><span class="sxs-lookup"><span data-stu-id="e1ef3-265">variableName</span></span> | `string` | <span data-ttu-id="e1ef3-266">Переменное имя.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-266">Variable name.</span></span> | 
| <span data-ttu-id="e1ef3-267">newValue</span><span class="sxs-lookup"><span data-stu-id="e1ef3-267">newValue</span></span> | [<span data-ttu-id="e1ef3-268">Runtime.CallArgument</span><span class="sxs-lookup"><span data-stu-id="e1ef3-268">Runtime.CallArgument</span></span>](./runtime.md#callargument) | <span data-ttu-id="e1ef3-269">Новое переменная значение.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-269">New variable value.</span></span> |  
| <span data-ttu-id="e1ef3-270">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-270">callFrameId</span></span> | [<span data-ttu-id="e1ef3-271">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-271">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e1ef3-272">ID callframe, который содержит переменную.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-272">ID of callframe that holds variable.</span></span> |  

---  

### <a name="setblackboxpatterns"></a><span data-ttu-id="e1ef3-273">setBlackboxPatterns</span><span class="sxs-lookup"><span data-stu-id="e1ef3-273">setBlackboxPatterns</span></span>  

<span data-ttu-id="e1ef3-274">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-274">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-275">Замените предыдущие шаблоны черных ящиков на пройденные.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-275">Replace previous blackbox patterns with passed ones.</span></span>  <span data-ttu-id="e1ef3-276">Заставляет отодвигаться, чтобы пропустить шаг/паузу в скриптах с URL-адресом, совпадающий с одним из шаблонов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-276">Forces backend to skip stepping/pausing in scripts with url matching one of the patterns.</span></span>  <span data-ttu-id="e1ef3-277">Отладка будет пытаться оставить черный ящик скрипт, выполняя "шаг" несколько раз, наконец, прибегая к "выйти" в случае неудачи.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-277">The debugger will try to leave blackboxed script by performing 'step in' several times, finally resorting to 'step out' if unsuccessful.</span></span>  


| <span data-ttu-id="e1ef3-278">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-278">Parameters</span></span> | <span data-ttu-id="e1ef3-279">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-279">Type</span></span> | <span data-ttu-id="e1ef3-280">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-280">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-281">шаблоны</span><span class="sxs-lookup"><span data-stu-id="e1ef3-281">patterns</span></span> | `string[]` | <span data-ttu-id="e1ef3-282">Массив regexps, который будет использоваться для проверки URL-адреса скрипта для состояния blackbox.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-282">Array of regexps that will be used to check script url for blackbox state.</span></span> | 

---  

### <a name="mssetdebuggerpropertyvalue"></a><span data-ttu-id="e1ef3-283">msSetDebuggerPropertyValue</span><span class="sxs-lookup"><span data-stu-id="e1ef3-283">msSetDebuggerPropertyValue</span></span>  

<span data-ttu-id="e1ef3-284">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-284">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-285">Microsoft. Задает указанное свойство отладки указанному значению.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-285">Microsoft: Sets the specified debugger property to the specified value.</span></span>  

| <span data-ttu-id="e1ef3-286">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-286">Parameters</span></span> | <span data-ttu-id="e1ef3-287">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-287">Type</span></span> | <span data-ttu-id="e1ef3-288">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-288">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-289">debuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-289">debuggerPropertyId</span></span> | <span data-ttu-id="e1ef3-290">string</span><span class="sxs-lookup"><span data-stu-id="e1ef3-290">string</span></span> | <span data-ttu-id="e1ef3-291">Microsoft. Свойство id \(i.e. `msDebuggerPropertyId` \) для набора.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-291">Microsoft:  The property id \(i.e. `msDebuggerPropertyId`\) to set.</span></span> | 
| <span data-ttu-id="e1ef3-292">newValue</span><span class="sxs-lookup"><span data-stu-id="e1ef3-292">newValue</span></span> | `string` | &nbsp; |  

---  

## <a name="events"></a><span data-ttu-id="e1ef3-293">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="e1ef3-293">Events</span></span>  

### <a name="scriptparsed"></a><span data-ttu-id="e1ef3-294">scriptParsed</span><span class="sxs-lookup"><span data-stu-id="e1ef3-294">scriptParsed</span></span>  

<span data-ttu-id="e1ef3-295">Уволено при размыве сценария.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-295">Fired when the script is parsed.</span></span> <span data-ttu-id="e1ef3-296">Это событие также будет уволено для всех известных и неиспользванных скриптов при включив отладку.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-296">This event is also fired for all known and uncollected scripts upon enabling debugger.</span></span>  

| <span data-ttu-id="e1ef3-297">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-297">Parameters</span></span> | <span data-ttu-id="e1ef3-298">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-298">Type</span></span> | <span data-ttu-id="e1ef3-299">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-299">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-300">scriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-300">scriptId</span></span> | [<span data-ttu-id="e1ef3-301">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-301">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e1ef3-302">Идентификатор размыкаемого скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-302">Identifier of the script parsed.</span></span> |  
| <span data-ttu-id="e1ef3-303">url</span><span class="sxs-lookup"><span data-stu-id="e1ef3-303">url</span></span> | `string` | <span data-ttu-id="e1ef3-304">URL-адрес или имя разбияемого скрипта \(если таково\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-304">URL or name of the script parsed \(if any\).</span></span> | 
| <span data-ttu-id="e1ef3-305">startLine</span><span class="sxs-lookup"><span data-stu-id="e1ef3-305">startLine</span></span> | `integer` | <span data-ttu-id="e1ef3-306">Строка смещения скрипта в ресурсе с заданным URL-адресом \(для тегов скрипта\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-306">Line offset of the script within the resource with given URL \(for script tags\).</span></span> | 
| <span data-ttu-id="e1ef3-307">startColumn</span><span class="sxs-lookup"><span data-stu-id="e1ef3-307">startColumn</span></span> | `integer` | <span data-ttu-id="e1ef3-308">Столбец смещения скрипта в ресурсе с заданным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-308">Column offset of the script within the resource with given URL.</span></span> | 
| <span data-ttu-id="e1ef3-309">endLine</span><span class="sxs-lookup"><span data-stu-id="e1ef3-309">endLine</span></span> | `integer` | <span data-ttu-id="e1ef3-310">Последняя строка сценария.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-310">Last line of the script.</span></span> | 
| <span data-ttu-id="e1ef3-311">endColumn</span><span class="sxs-lookup"><span data-stu-id="e1ef3-311">endColumn</span></span> | `integer` | <span data-ttu-id="e1ef3-312">Длина последней строки сценария.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-312">Length of the last line of the script.</span></span> | 
| <span data-ttu-id="e1ef3-313">executionContextId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-313">executionContextId</span></span> | [<span data-ttu-id="e1ef3-314">Runtime.ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-314">Runtime.ExecutionContextId</span></span>](./runtime.md#executioncontextid) | <span data-ttu-id="e1ef3-315">Указывает контекст создания скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-315">Specifies script creation context.</span></span> |  
| <span data-ttu-id="e1ef3-316">sourceMapURL \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-316">sourceMapURL \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-317">URL-адрес исходных карт, связанных со сценарием (если таково).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-317">URL of source map associated with script (if any).</span></span> |  
| <span data-ttu-id="e1ef3-318">длина \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-318">length \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-319">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-319">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-320">Длина скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-320">This script length.</span></span> |  
| <span data-ttu-id="e1ef3-321">msParentId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-321">msParentId \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-322">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-322">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-323">Это родительский документ.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-323">This is the parent document ID.</span></span> |  
| <span data-ttu-id="e1ef3-324">msMimeType \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-324">msMimeType \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-325">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-325">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-326">Это тип mime.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-326">This is the mime type.</span></span> |  
| <span data-ttu-id="e1ef3-327">msIsDynamicCode \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-327">msIsDynamicCode \(optional\)</span></span> | `boolean` | <span data-ttu-id="e1ef3-328">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-328">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-329">Это указывает, является ли это динамический код.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-329">This indicates whether it is dynamic code.</span></span> |  
| <span data-ttu-id="e1ef3-330">msLongDocumentId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-330">msLongDocumentId \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-331">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-331">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-332">Это длинный документ.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-332">This is the long document ID.</span></span> |  

---  

### <a name="breakpointresolved"></a><span data-ttu-id="e1ef3-333">breakpointResolved</span><span class="sxs-lookup"><span data-stu-id="e1ef3-333">breakpointResolved</span></span>  

<span data-ttu-id="e1ef3-334">В случае, если точка разрыва будет разрешена к фактическому сценарию и расположению.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-334">Fired when breakpoint is resolved to an actual script and location.</span></span>  

| <span data-ttu-id="e1ef3-335">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-335">Parameters</span></span> | <span data-ttu-id="e1ef3-336">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-336">Type</span></span> | <span data-ttu-id="e1ef3-337">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-337">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-338">breakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-338">breakpointId</span></span> | [<span data-ttu-id="e1ef3-339">BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-339">BreakpointId</span></span>](#breakpointid) | <span data-ttu-id="e1ef3-340">Уникальный идентификатор Breakpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-340">Breakpoint unique identifier.</span></span> |  
| <span data-ttu-id="e1ef3-341">расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-341">location</span></span> | [<span data-ttu-id="e1ef3-342">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-342">Location</span></span>](#location) | <span data-ttu-id="e1ef3-343">Фактическое расположение точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-343">Actual breakpoint location.</span></span> |  
| <span data-ttu-id="e1ef3-344">msLength \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-344">msLength \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-345">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-345">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-346">Microsoft. Длина кода \(то есть количество символов\) в расположении точки разрыва.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-346">Microsoft:  Length of code \(i.e. number of characters\) at the breakpoint location.</span></span> |  

---  

### <a name="paused"></a><span data-ttu-id="e1ef3-347">пауза</span><span class="sxs-lookup"><span data-stu-id="e1ef3-347">paused</span></span>  

<span data-ttu-id="e1ef3-348">Уволено, когда отладки ломаются для точки разлома или исключения.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-348">Fired when the debuggers breaks for a breakpoint or exception.</span></span>  

| <span data-ttu-id="e1ef3-349">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1ef3-349">Parameters</span></span> | <span data-ttu-id="e1ef3-350">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-350">Type</span></span> | <span data-ttu-id="e1ef3-351">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-351">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-352">callFrames</span><span class="sxs-lookup"><span data-stu-id="e1ef3-352">callFrames</span></span> | [<span data-ttu-id="e1ef3-353">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="e1ef3-353">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="e1ef3-354">Вызов стек отладки остановился.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-354">Call stack the debugger stopped on.</span></span> |  
| <span data-ttu-id="e1ef3-355">причина</span><span class="sxs-lookup"><span data-stu-id="e1ef3-355">reason</span></span> | `string` |  <span data-ttu-id="e1ef3-356">Причина паузы.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-356">Pause reason.</span></span>  <span data-ttu-id="e1ef3-357">Допустимые значения:  `breakpoint` `step` , , , `exception` `other` и</span><span class="sxs-lookup"><span data-stu-id="e1ef3-357">Allowed values:  `breakpoint`, `step`, `exception`, `other`, and</span></span> `EventListener` |  
| <span data-ttu-id="e1ef3-358">данные \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-358">data \(optional\)</span></span> | `object` | <span data-ttu-id="e1ef3-359">Объект, содержащий отдельные вспомогательные свойства.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-359">Object containing break-specific auxiliary properties.</span></span> |  
| <span data-ttu-id="e1ef3-360">hitBreakpoints \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-360">hitBreakpoints \(optional\)</span></span> | `string[]` | <span data-ttu-id="e1ef3-361">Hit breakpoints IDs</span><span class="sxs-lookup"><span data-stu-id="e1ef3-361">Hit breakpoints IDs</span></span> |  
| <span data-ttu-id="e1ef3-362">asyncStackTrace \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-362">asyncStackTrace \(optional\)</span></span> | `StackTrace` | <span data-ttu-id="e1ef3-363">Трассировка стека async JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-363">JavaScript async stack trace.</span></span> |  

---  

### <a name="resumed"></a><span data-ttu-id="e1ef3-364">возобновлено</span><span class="sxs-lookup"><span data-stu-id="e1ef3-364">resumed</span></span>  

<span data-ttu-id="e1ef3-365">Уволили, когда отладка возобновляет выполнение.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-365">Fired when the debugger resumes execution.</span></span>  

&nbsp;  

---  

## <a name="types"></a><span data-ttu-id="e1ef3-366">Типы</span><span class="sxs-lookup"><span data-stu-id="e1ef3-366">Types</span></span>  

### <a name="breakpointid-string"></a><span data-ttu-id="e1ef3-367">Строка BreakpointId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-367">BreakpointId string</span></span>  

<a name="breakpointid"></a>  

<span data-ttu-id="e1ef3-368">Идентификатор Breakpoint.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-368">Breakpoint identifier.</span></span>  

&nbsp;  

---  

### <a name="callframeid-string"></a><span data-ttu-id="e1ef3-369">Строка CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-369">CallFrameId string</span></span>  

<a name="callframeid"></a>  

<span data-ttu-id="e1ef3-370">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-370">Call frame identifier.</span></span>  

&nbsp;  

---  

### <a name="location-object"></a><span data-ttu-id="e1ef3-371">Объект Location</span><span class="sxs-lookup"><span data-stu-id="e1ef3-371">Location object</span></span>  

<a name="location"></a>  

<span data-ttu-id="e1ef3-372">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-372">Location in the source code.</span></span>  

| <span data-ttu-id="e1ef3-373">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1ef3-373">Properties</span></span> | <span data-ttu-id="e1ef3-374">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-374">Type</span></span> | <span data-ttu-id="e1ef3-375">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-375">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-376">scriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-376">scriptId</span></span> | [<span data-ttu-id="e1ef3-377">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-377">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e1ef3-378">Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="e1ef3-378">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="e1ef3-379">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e1ef3-379">lineNumber</span></span> | `integer` | <span data-ttu-id="e1ef3-380">Номер строки в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-380">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e1ef3-381">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-381">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-382">Номер столбца в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-382">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e1ef3-383">msLength</span><span class="sxs-lookup"><span data-stu-id="e1ef3-383">msLength</span></span> | `integer` | <span data-ttu-id="e1ef3-384">Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-384">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  

---  

### <a name="breaklocation-object"></a><span data-ttu-id="e1ef3-385">Объект BreakLocation</span><span class="sxs-lookup"><span data-stu-id="e1ef3-385">BreakLocation object</span></span>  

<a name="breaklocation"></a>  

<span data-ttu-id="e1ef3-386">Разорвать расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-386">Break location in the source code.</span></span>  

| <span data-ttu-id="e1ef3-387">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1ef3-387">Properties</span></span> | <span data-ttu-id="e1ef3-388">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-388">Type</span></span> | <span data-ttu-id="e1ef3-389">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-390">scriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-390">scriptId</span></span> | [<span data-ttu-id="e1ef3-391">Runtime.ScriptId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-391">Runtime.ScriptId</span></span>](./runtime.md#scriptid) | <span data-ttu-id="e1ef3-392">Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` .</span><span class="sxs-lookup"><span data-stu-id="e1ef3-392">Script identifier as reported in the `Debugger.scriptParsed`.</span></span> |  
| <span data-ttu-id="e1ef3-393">lineNumber</span><span class="sxs-lookup"><span data-stu-id="e1ef3-393">lineNumber</span></span> | `integer` | <span data-ttu-id="e1ef3-394">Номер строки в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-394">Line number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e1ef3-395">columnNumber \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-395">columnNumber \(optional\)</span></span> | `integer` | <span data-ttu-id="e1ef3-396">Номер столбца в скрипте \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="e1ef3-396">Column number in the script \(0-based\).</span></span> |  
| <span data-ttu-id="e1ef3-397">msLength</span><span class="sxs-lookup"><span data-stu-id="e1ef3-397">msLength</span></span> | `integer` | <span data-ttu-id="e1ef3-398">Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-398">Microsoft:  Length of code \(i.e. number of characters\) at this call frame.</span></span> |  
| <span data-ttu-id="e1ef3-399">тип \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-399">type \(optional\)</span></span> | `string` | <span data-ttu-id="e1ef3-400">Допустимые значения: отладкаStatement, вызов, возврат.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-400">Allowed values: debuggerStatement, call, return.</span></span> |  

---  

### <a name="callframe-object"></a><span data-ttu-id="e1ef3-401">Объект CallFrame</span><span class="sxs-lookup"><span data-stu-id="e1ef3-401">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="e1ef3-402">Кадр вызова JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-402">JavaScript call frame.</span></span> <span data-ttu-id="e1ef3-403">Массив кадров вызовов формирует стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-403">Array of call frames form the call stack.</span></span>  

| <span data-ttu-id="e1ef3-404">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1ef3-404">Properties</span></span> | <span data-ttu-id="e1ef3-405">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-405">Type</span></span> | <span data-ttu-id="e1ef3-406">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-406">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-407">callFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-407">callFrameId</span></span> | [<span data-ttu-id="e1ef3-408">CallFrameId</span><span class="sxs-lookup"><span data-stu-id="e1ef3-408">CallFrameId</span></span>](#callframeid) | <span data-ttu-id="e1ef3-409">Идентификатор кадра вызова.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-409">Call frame identifier.</span></span>  <span data-ttu-id="e1ef3-410">Этот идентификатор действителен только во время паузы отладки.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-410">This identifier is only valid while the debugger is paused.</span></span> |  
| <span data-ttu-id="e1ef3-411">functionName</span><span class="sxs-lookup"><span data-stu-id="e1ef3-411">functionName</span></span> | `string` | <span data-ttu-id="e1ef3-412">Имя функции JavaScript, вызываемой в этом кадре вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-412">Name of the JavaScript function called on this call frame.</span></span> |  
| <span data-ttu-id="e1ef3-413">functionLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-413">functionLocation \(optional\)</span></span> | [<span data-ttu-id="e1ef3-414">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-414">Location</span></span>](#location) | <span data-ttu-id="e1ef3-415">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-415">**Experimental**.</span></span>  <span data-ttu-id="e1ef3-416">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-416">Location in the source code.</span></span> |  
| <span data-ttu-id="e1ef3-417">расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-417">location</span></span> | [<span data-ttu-id="e1ef3-418">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-418">Location</span></span>](#location) | <span data-ttu-id="e1ef3-419">Расположение в исходный код.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-419">Location in the source code.</span></span> |  
| <span data-ttu-id="e1ef3-420">url</span><span class="sxs-lookup"><span data-stu-id="e1ef3-420">url</span></span> | `string` | <span data-ttu-id="e1ef3-421">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-421">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="e1ef3-422">scopeChain</span><span class="sxs-lookup"><span data-stu-id="e1ef3-422">scopeChain</span></span> | [<span data-ttu-id="e1ef3-423">Область[]</span><span class="sxs-lookup"><span data-stu-id="e1ef3-423">Scope[]</span></span>](#scope) | <span data-ttu-id="e1ef3-424">Цепочка области для этого кадра вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-424">Scope chain for this call frame.</span></span> |  
| <span data-ttu-id="e1ef3-425">это</span><span class="sxs-lookup"><span data-stu-id="e1ef3-425">this</span></span> | [<span data-ttu-id="e1ef3-426">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e1ef3-426">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | `this` <span data-ttu-id="e1ef3-427">объект для этого кадра вызовов.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-427">object for this call frame.</span></span> |  
| <span data-ttu-id="e1ef3-428">returnValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-428">returnValue \(optional\)</span></span> | [<span data-ttu-id="e1ef3-429">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e1ef3-429">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e1ef3-430">Возвращаемая величина, если функция находится в точке возврата.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-430">The value being returned, if the function is at return point.</span></span> |  

---  

### <a name="scope-object"></a><span data-ttu-id="e1ef3-431">Объект Scope</span><span class="sxs-lookup"><span data-stu-id="e1ef3-431">Scope object</span></span>  

<a name="scope"></a>  

<span data-ttu-id="e1ef3-432">Описание области.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-432">Scope description.</span></span>  

| <span data-ttu-id="e1ef3-433">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1ef3-433">Properties</span></span> | <span data-ttu-id="e1ef3-434">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-434">Type</span></span> | <span data-ttu-id="e1ef3-435">Сведения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-435">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e1ef3-436">Тип</span><span class="sxs-lookup"><span data-stu-id="e1ef3-436">type</span></span> | `string` | <span data-ttu-id="e1ef3-437">Тип области.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-437">Scope type.</span></span>  <span data-ttu-id="e1ef3-438">Допустимые значения:  `global` , , , , , , `local` `with` `closure` `catch` `block` `script` , `eval` `module` и</span><span class="sxs-lookup"><span data-stu-id="e1ef3-438">Allowed values:  `global`, `local`, `with`, `closure`, `catch`, `block`, `script`, `eval`, `module`, and</span></span> `return` |  
| <span data-ttu-id="e1ef3-439">объект</span><span class="sxs-lookup"><span data-stu-id="e1ef3-439">object</span></span> | [<span data-ttu-id="e1ef3-440">Runtime.RemoteObject</span><span class="sxs-lookup"><span data-stu-id="e1ef3-440">Runtime.RemoteObject</span></span>](./runtime.md#remoteobject) | <span data-ttu-id="e1ef3-441">Объект, представляющий область.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-441">Object representing the scope.</span></span>  <span data-ttu-id="e1ef3-442">Для и областей он представляет фактический объект; для остальных областей это искусственный переходный объект, который в качестве свойств передает переменные `global` `with` области.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-442">For `global` and `with` scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</span></span> |  
| <span data-ttu-id="e1ef3-443">имя \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-443">name \(optional\)</span></span> | `string` | &nbsp; |  
| <span data-ttu-id="e1ef3-444">startLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-444">startLocation \(optional\)</span></span> | [<span data-ttu-id="e1ef3-445">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-445">Location</span></span>](#location) | <span data-ttu-id="e1ef3-446">Расположение в исходный код, где начинается область.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-446">Location in the source code where scope starts.</span></span> |  
| <span data-ttu-id="e1ef3-447">endLocation \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="e1ef3-447">endLocation \(optional\)</span></span> | [<span data-ttu-id="e1ef3-448">Расположение</span><span class="sxs-lookup"><span data-stu-id="e1ef3-448">Location</span></span>](#location) | <span data-ttu-id="e1ef3-449">Расположение в исходный код, где область заканчивается.</span><span class="sxs-lookup"><span data-stu-id="e1ef3-449">Location in the source code where scope ends.</span></span> |  

---  

## <a name="dependencies"></a><span data-ttu-id="e1ef3-450">Зависимости</span><span class="sxs-lookup"><span data-stu-id="e1ef3-450">Dependencies</span></span>  

[<span data-ttu-id="e1ef3-451">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="e1ef3-451">Runtime</span></span>](./runtime.md)  
