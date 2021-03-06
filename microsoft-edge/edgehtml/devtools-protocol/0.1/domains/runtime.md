---
description: Ссылка На протокол DevTools Версии 0.1 (EdgeHTML) для домена runtime.  Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов.  Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.  Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.
title: Домен runtime - Протокол DevTools Версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397694"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="4af80-106">Домен runtime - Протокол DevTools Версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4af80-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="4af80-107">Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="4af80-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span>  <span data-ttu-id="4af80-108">Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="4af80-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span>  <span data-ttu-id="4af80-109">Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="4af80-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="4af80-110">Категория</span><span class="sxs-lookup"><span data-stu-id="4af80-110">Classification</span></span> | <span data-ttu-id="4af80-111">Участники</span><span class="sxs-lookup"><span data-stu-id="4af80-111">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="4af80-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4af80-112">Methods</span></span>](#methods) | <span data-ttu-id="4af80-113">[включить,](#enable) [отключить,](#disable) [оценить,](#evaluate) [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="4af80-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |  
| [<span data-ttu-id="4af80-114">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="4af80-114">Events</span></span>](#events) | <span data-ttu-id="4af80-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="4af80-115">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |  
| [<span data-ttu-id="4af80-116">Типы</span><span class="sxs-lookup"><span data-stu-id="4af80-116">Types</span></span>](#types) | <span data-ttu-id="4af80-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="4af80-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="4af80-118">Методы</span><span class="sxs-lookup"><span data-stu-id="4af80-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="4af80-119">"Включить"</span><span class="sxs-lookup"><span data-stu-id="4af80-119">enable</span></span>  

<span data-ttu-id="4af80-120">Включает отчеты о `executionContextsCleared` событии.</span><span class="sxs-lookup"><span data-stu-id="4af80-120">Enables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="4af80-121">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="4af80-121">disable</span></span>  

<span data-ttu-id="4af80-122">Отключение отчетов о `executionContextsCleared` событии.</span><span class="sxs-lookup"><span data-stu-id="4af80-122">Disables reporting of the `executionContextsCleared` event.</span></span>  

&nbsp;  

---  

### <a name="evaluate"></a><span data-ttu-id="4af80-123">оценка</span><span class="sxs-lookup"><span data-stu-id="4af80-123">evaluate</span></span>  

<span data-ttu-id="4af80-124">Оценивает выражение на глобальном объекте.</span><span class="sxs-lookup"><span data-stu-id="4af80-124">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="4af80-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af80-125">Parameters</span></span> | <span data-ttu-id="4af80-126">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-126">Type</span></span> | <span data-ttu-id="4af80-127">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-127">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-128">выражение</span><span class="sxs-lookup"><span data-stu-id="4af80-128">expression</span></span> | `string` | <span data-ttu-id="4af80-129">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="4af80-129">Expression to evaluate.</span></span> |  
| <span data-ttu-id="4af80-130">silent \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-130">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-131">В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="4af80-131">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="4af80-132">Переопределяет `setPauseOnException` состояние.</span><span class="sxs-lookup"><span data-stu-id="4af80-132">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="4af80-133">contextId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-133">contextId \(optional\)</span></span> | [<span data-ttu-id="4af80-134">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4af80-134">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4af80-135">Указывает, в котором контекст выполнения для выполнения оценки.</span><span class="sxs-lookup"><span data-stu-id="4af80-135">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="4af80-136">Если параметр опущен, оценка будет выполнена в контексте проверенной страницы.</span><span class="sxs-lookup"><span data-stu-id="4af80-136">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="4af80-137">returnByValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-137">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-138">Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению.</span><span class="sxs-lookup"><span data-stu-id="4af80-138">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="4af80-139">awaitPromise \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-139">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-140">Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="4af80-140">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="4af80-141">Возвращает</span><span class="sxs-lookup"><span data-stu-id="4af80-141">Returns</span></span> | <span data-ttu-id="4af80-142">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-142">Type</span></span> | <span data-ttu-id="4af80-143">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-143">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-144">результат</span><span class="sxs-lookup"><span data-stu-id="4af80-144">result</span></span> | [<span data-ttu-id="4af80-145">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-145">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-146">Результат оценки.</span><span class="sxs-lookup"><span data-stu-id="4af80-146">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="4af80-147">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="4af80-147">callFunctionOn</span></span>  

<span data-ttu-id="4af80-148">Функция вызовов с заданным объявлением на заданный объект.</span><span class="sxs-lookup"><span data-stu-id="4af80-148">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="4af80-149">Объектная группа результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-149">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="4af80-150">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af80-150">Parameters</span></span> | <span data-ttu-id="4af80-151">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-151">Type</span></span> | <span data-ttu-id="4af80-152">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-152">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-153">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="4af80-153">functionDeclaration</span></span> | `string` | <span data-ttu-id="4af80-154">Объявление функции вызова.</span><span class="sxs-lookup"><span data-stu-id="4af80-154">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="4af80-155">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-155">objectId \(optional\)</span></span> | [<span data-ttu-id="4af80-156">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4af80-156">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4af80-157">Идентификатор объекта для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="4af80-157">Identifier of the object to call function on.</span></span>  <span data-ttu-id="4af80-158">Либо `objectId` `executionContextId` заданы, либо должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="4af80-158">Either `objectId` or `executionContextId` should be specified.</span></span>  <span data-ttu-id="4af80-159">objectId должен быть из функции Runtime.evaluate()</span><span class="sxs-lookup"><span data-stu-id="4af80-159">objectId must be from the Runtime.evaluate() function.</span></span> |  
| <span data-ttu-id="4af80-160">аргументы \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-160">arguments \(optional\)</span></span> | [<span data-ttu-id="4af80-161">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="4af80-161">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="4af80-162">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="4af80-162">Call arguments.</span></span>  <span data-ttu-id="4af80-163">Все аргументы вызовов должны принадлежать одному миру JavaScript как целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="4af80-163">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="4af80-164">silent \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-164">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-165">В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="4af80-165">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="4af80-166">Переопределяет `setPauseOnException` состояние.</span><span class="sxs-lookup"><span data-stu-id="4af80-166">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="4af80-167">returnByValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-167">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-168">Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению.</span><span class="sxs-lookup"><span data-stu-id="4af80-168">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="4af80-169">awaitPromise \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-169">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-170">Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="4af80-170">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="4af80-171">Возвращает</span><span class="sxs-lookup"><span data-stu-id="4af80-171">Returns</span></span> | <span data-ttu-id="4af80-172">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-172">Type</span></span> | <span data-ttu-id="4af80-173">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-173">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-174">результат</span><span class="sxs-lookup"><span data-stu-id="4af80-174">result</span></span> | [<span data-ttu-id="4af80-175">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-175">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-176">Результат вызова.</span><span class="sxs-lookup"><span data-stu-id="4af80-176">Call result.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="4af80-177">getProperties</span><span class="sxs-lookup"><span data-stu-id="4af80-177">getProperties</span></span>  

<span data-ttu-id="4af80-178">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-178">Returns properties of a given object.</span></span>  <span data-ttu-id="4af80-179">Объектная группа результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-179">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="4af80-180">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af80-180">Parameters</span></span> | <span data-ttu-id="4af80-181">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-181">Type</span></span> | <span data-ttu-id="4af80-182">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-182">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-183">objectId</span><span class="sxs-lookup"><span data-stu-id="4af80-183">objectId</span></span> | [<span data-ttu-id="4af80-184">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4af80-184">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4af80-185">Идентификатор объекта для возврата свойств.</span><span class="sxs-lookup"><span data-stu-id="4af80-185">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="4af80-186">должно быть из `Debugger.evaluateOnCallFrame()` функции.</span><span class="sxs-lookup"><span data-stu-id="4af80-186">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="4af80-187">ownProperties \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-187">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-188">Если `true` возвращает свойства, принадлежащие только самому элементу, а не цепочке прототипов.</span><span class="sxs-lookup"><span data-stu-id="4af80-188">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="4af80-189">accessorPropertiesOnly \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-189">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-190">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="4af80-190">**Experimental**.</span></span>  <span data-ttu-id="4af80-191">Если `true` , возвращает свойства вспомогательного оборудования \(с getter/setter\) только; внутренние свойства также не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="4af80-191">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="4af80-192">Возвращает</span><span class="sxs-lookup"><span data-stu-id="4af80-192">Returns</span></span> | <span data-ttu-id="4af80-193">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-193">Type</span></span> | <span data-ttu-id="4af80-194">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-195">результат</span><span class="sxs-lookup"><span data-stu-id="4af80-195">result</span></span> | [<span data-ttu-id="4af80-196">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="4af80-196">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="4af80-197">Свойства объектов.</span><span class="sxs-lookup"><span data-stu-id="4af80-197">Object properties.</span></span> |  

---  

## <a name="events"></a><span data-ttu-id="4af80-198">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="4af80-198">Events</span></span>  

### <a name="executioncontextscleared"></a><span data-ttu-id="4af80-199">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="4af80-199">executionContextsCleared</span></span>  

<span data-ttu-id="4af80-200">Выдан, когда все executionContexts были очищены в браузере.</span><span class="sxs-lookup"><span data-stu-id="4af80-200">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="4af80-201">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="4af80-201">exceptionThrown</span></span>  

<span data-ttu-id="4af80-202">Выдано, когда исключение было выброшено и ненаблюдаемо.</span><span class="sxs-lookup"><span data-stu-id="4af80-202">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="4af80-203">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af80-203">Parameters</span></span> | <span data-ttu-id="4af80-204">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-204">Type</span></span> | <span data-ttu-id="4af80-205">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-205">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-206">timestamp</span><span class="sxs-lookup"><span data-stu-id="4af80-206">timestamp</span></span> | [<span data-ttu-id="4af80-207">Метка времени</span><span class="sxs-lookup"><span data-stu-id="4af80-207">Timestamp</span></span>](#timestamp) | <span data-ttu-id="4af80-208">Timestamp исключения.</span><span class="sxs-lookup"><span data-stu-id="4af80-208">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="4af80-209">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="4af80-209">exceptionDetails</span></span> | [<span data-ttu-id="4af80-210">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="4af80-210">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a><span data-ttu-id="4af80-211">Типы</span><span class="sxs-lookup"><span data-stu-id="4af80-211">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="4af80-212">Строка ScriptId</span><span class="sxs-lookup"><span data-stu-id="4af80-212">ScriptId string</span></span>  

<a name="scriptid"></a>  

<span data-ttu-id="4af80-213">Уникальный идентификатор скрипта.</span><span class="sxs-lookup"><span data-stu-id="4af80-213">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="4af80-214">Строка RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4af80-214">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>  

<span data-ttu-id="4af80-215">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-215">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="4af80-216">Строка UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4af80-216">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="4af80-217">Примитивное значение, которое не может быть строкифицировано JSON.</span><span class="sxs-lookup"><span data-stu-id="4af80-217">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="4af80-218">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="4af80-218">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="4af80-219">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="4af80-219">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="4af80-220">Объект RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-220">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="4af80-221">Объект Mirror, отсылающий к исходному объекту JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4af80-221">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="4af80-222">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-222">Properties</span></span> | <span data-ttu-id="4af80-223">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-223">Type</span></span> | <span data-ttu-id="4af80-224">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-224">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-225">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-225">type</span></span> | `string` | <span data-ttu-id="4af80-226">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-226">Object type.</span></span>  <span data-ttu-id="4af80-227">Допустимые значения:  `object` , , , , , `function` `undefined` `string` `number` `boolean` и</span><span class="sxs-lookup"><span data-stu-id="4af80-227">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="4af80-228">подтип \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-228">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-229">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-229">Object subtype hint.</span></span>  <span data-ttu-id="4af80-230">Только для `object` значений типа.</span><span class="sxs-lookup"><span data-stu-id="4af80-230">Specified for `object` type values only.</span></span>  <span data-ttu-id="4af80-231">Допустимые значения:  `null` `error` и</span><span class="sxs-lookup"><span data-stu-id="4af80-231">Allowed values:  `null`, `error`, and</span></span> `promise` |  
| <span data-ttu-id="4af80-232">className \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-232">className \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-233">Имя объекта класса \(конструктор\).</span><span class="sxs-lookup"><span data-stu-id="4af80-233">Object class \(constructor\) name.</span></span>  <span data-ttu-id="4af80-234">Только для `object` значений типа.</span><span class="sxs-lookup"><span data-stu-id="4af80-234">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="4af80-235">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-235">value \(optional\)</span></span> | `any` | <span data-ttu-id="4af80-236">Значение удаленного объекта в случае примитивных значений или значений JSON \(если оно было запророшно\).</span><span class="sxs-lookup"><span data-stu-id="4af80-236">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="4af80-237">unserializableValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-237">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="4af80-238">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4af80-238">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="4af80-239">Примитивное значение, которое не может быть JSON-stringified, не `value` имеет, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="4af80-239">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="4af80-240">описание \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-240">description \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-241">Строковая репрезентация объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-241">String representation of the object.</span></span> |  
| <span data-ttu-id="4af80-242">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-242">objectId \(optional\)</span></span> | [<span data-ttu-id="4af80-243">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4af80-243">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4af80-244">Уникальный идентификатор объекта \(для небытийных значений\).</span><span class="sxs-lookup"><span data-stu-id="4af80-244">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="4af80-245">msDebuggerPropertyId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-245">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-246">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="4af80-246">**Experimental**.</span></span>  <span data-ttu-id="4af80-247">Microsoft. Связанный с этим объектом ID свойства отладки.</span><span class="sxs-lookup"><span data-stu-id="4af80-247">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="4af80-248">Объект PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="4af80-248">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="4af80-249">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-249">Object property descriptor.</span></span>  

| <span data-ttu-id="4af80-250">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-250">Properties</span></span> | <span data-ttu-id="4af80-251">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-251">Type</span></span> | <span data-ttu-id="4af80-252">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-252">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-253">name</span><span class="sxs-lookup"><span data-stu-id="4af80-253">name</span></span> | `string` | <span data-ttu-id="4af80-254">Имя свойства или описание символа.</span><span class="sxs-lookup"><span data-stu-id="4af80-254">Property name or symbol description.</span></span> |  
| <span data-ttu-id="4af80-255">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-255">value \(optional\)</span></span> | [<span data-ttu-id="4af80-256">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-256">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-257">Значение, связанное с свойством.</span><span class="sxs-lookup"><span data-stu-id="4af80-257">The value associated with the property.</span></span> |  
| <span data-ttu-id="4af80-258">writable \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-258">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4af80-259">если значение, связанное с свойством, может быть изменено \(только дескрипторы данных\).</span><span class="sxs-lookup"><span data-stu-id="4af80-259">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="4af80-260">получить \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-260">get \(optional\)</span></span> | [<span data-ttu-id="4af80-261">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-261">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-262">Функция, которая служит в качестве геттера для свойства, или если нет геттера `undefined` \(только дескрипторы аксессуара\).</span><span class="sxs-lookup"><span data-stu-id="4af80-262">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="4af80-263">set \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-263">set \(optional\)</span></span> | [<span data-ttu-id="4af80-264">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-264">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-265">Функция, которая служит сеттером для свойства или если нет сеттера `undefined` \(только дескрипторы аксессуара\).</span><span class="sxs-lookup"><span data-stu-id="4af80-265">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="4af80-266">настраиваемый</span><span class="sxs-lookup"><span data-stu-id="4af80-266">configurable</span></span> | `boolean` | `True` <span data-ttu-id="4af80-267">если тип этого дескриптора свойства может быть изменен и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-267">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="4af80-268">переоменимый</span><span class="sxs-lookup"><span data-stu-id="4af80-268">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="4af80-269">если это свойство появляется во время переопечатки свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-269">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="4af80-270">wasThrown \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-270">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4af80-271">если результат был брошен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="4af80-271">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="4af80-272">isOwn \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-272">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="4af80-273">если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="4af80-273">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="4af80-274">msReturnValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-274">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="4af80-275">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="4af80-275">**Experimental**.</span></span>  <span data-ttu-id="4af80-276">Майкрософт:  `True` если свойство является возвращаемой величиной.</span><span class="sxs-lookup"><span data-stu-id="4af80-276">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="4af80-277">символ \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-277">symbol \(optional\)</span></span> | [<span data-ttu-id="4af80-278">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-278">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-279">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="4af80-279">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="4af80-280">Объект CallArgument</span><span class="sxs-lookup"><span data-stu-id="4af80-280">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="4af80-281">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="4af80-281">Represents function call argument.</span></span>  <span data-ttu-id="4af80-282">Либо удаленный идентификационный объект, неопределимое примитивное значение, либо значение \(для неопределённого\) не `value` должно быть указано.</span><span class="sxs-lookup"><span data-stu-id="4af80-282">Either remote object ID `value`, unserializable primitive value or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="4af80-283">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-283">Properties</span></span> | <span data-ttu-id="4af80-284">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-284">Type</span></span> | <span data-ttu-id="4af80-285">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-285">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-286">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-286">value \(optional\)</span></span> | `any` | <span data-ttu-id="4af80-287">Примитивное значение или серийный объект javascript.</span><span class="sxs-lookup"><span data-stu-id="4af80-287">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="4af80-288">unserializableValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-288">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="4af80-289">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="4af80-289">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="4af80-290">Примитивное значение, которое не может быть jSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="4af80-290">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="4af80-291">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-291">objectId \(optional\)</span></span> | [<span data-ttu-id="4af80-292">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="4af80-292">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="4af80-293">Удаленная ручка объекта.</span><span class="sxs-lookup"><span data-stu-id="4af80-293">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="4af80-294">Integer executionContextId</span><span class="sxs-lookup"><span data-stu-id="4af80-294">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="4af80-295">ID контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="4af80-295">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="4af80-296">Объект ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="4af80-296">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="4af80-297">Подробные сведения об исключении \(или ошибке\), которое было выброшено во время компиляции или выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="4af80-297">Detailed information about exception \(or error\) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="4af80-298">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-298">Properties</span></span> | <span data-ttu-id="4af80-299">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-299">Type</span></span> | <span data-ttu-id="4af80-300">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-300">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-301">exceptionId</span><span class="sxs-lookup"><span data-stu-id="4af80-301">exceptionId</span></span> | `integer` | <span data-ttu-id="4af80-302">ID исключения.</span><span class="sxs-lookup"><span data-stu-id="4af80-302">Exception ID.</span></span> |  
| <span data-ttu-id="4af80-303">текст</span><span class="sxs-lookup"><span data-stu-id="4af80-303">text</span></span> | `string` | <span data-ttu-id="4af80-304">Текст исключения, который следует использовать вместе с объектом исключения при наличии.</span><span class="sxs-lookup"><span data-stu-id="4af80-304">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="4af80-305">lineNumber</span><span class="sxs-lookup"><span data-stu-id="4af80-305">lineNumber</span></span> | `integer` | <span data-ttu-id="4af80-306">Номер строки расположения исключения \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="4af80-306">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="4af80-307">columnNumber</span><span class="sxs-lookup"><span data-stu-id="4af80-307">columnNumber</span></span> | `integer` | <span data-ttu-id="4af80-308">Номер столбца расположения исключения \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="4af80-308">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="4af80-309">scriptId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-309">scriptId \(optional\)</span></span> | [<span data-ttu-id="4af80-310">ScriptId</span><span class="sxs-lookup"><span data-stu-id="4af80-310">ScriptId</span></span>](#scriptid) | <span data-ttu-id="4af80-311">ID сценария расположения исключений.</span><span class="sxs-lookup"><span data-stu-id="4af80-311">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="4af80-312">URL\(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-312">url \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-313">URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан.</span><span class="sxs-lookup"><span data-stu-id="4af80-313">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="4af80-314">stackTrace \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-314">stackTrace \(optional\)</span></span> | [<span data-ttu-id="4af80-315">StackTrace</span><span class="sxs-lookup"><span data-stu-id="4af80-315">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="4af80-316">Трассировка стека JavaScript при наличии.</span><span class="sxs-lookup"><span data-stu-id="4af80-316">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="4af80-317">исключение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-317">exception \(optional\)</span></span> | [<span data-ttu-id="4af80-318">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="4af80-318">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="4af80-319">Объект Исключения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="4af80-319">Exception object if available.</span></span> |  
| <span data-ttu-id="4af80-320">executionContextId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-320">executionContextId \(optional\)</span></span> | [<span data-ttu-id="4af80-321">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="4af80-321">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="4af80-322">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="4af80-322">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="4af80-323">Integer Timestamp</span><span class="sxs-lookup"><span data-stu-id="4af80-323">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="4af80-324">Количество миллисекунд с эпохи.</span><span class="sxs-lookup"><span data-stu-id="4af80-324">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="4af80-325">Объект CallFrame</span><span class="sxs-lookup"><span data-stu-id="4af80-325">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="4af80-326">Стек записи для ошибок и утверждений во время работы.</span><span class="sxs-lookup"><span data-stu-id="4af80-326">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="4af80-327">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-327">Properties</span></span> | <span data-ttu-id="4af80-328">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-328">Type</span></span> | <span data-ttu-id="4af80-329">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-329">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-330">functionName</span><span class="sxs-lookup"><span data-stu-id="4af80-330">functionName</span></span> | `string` | <span data-ttu-id="4af80-331">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4af80-331">JavaScript function name.</span></span> |  
| <span data-ttu-id="4af80-332">scriptId</span><span class="sxs-lookup"><span data-stu-id="4af80-332">scriptId</span></span> | [<span data-ttu-id="4af80-333">ScriptId</span><span class="sxs-lookup"><span data-stu-id="4af80-333">ScriptId</span></span>](#scriptid) | <span data-ttu-id="4af80-334">ID скрипта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4af80-334">JavaScript script ID.</span></span> |  
| <span data-ttu-id="4af80-335">url</span><span class="sxs-lookup"><span data-stu-id="4af80-335">url</span></span> | `string` | <span data-ttu-id="4af80-336">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="4af80-336">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="4af80-337">lineNumber</span><span class="sxs-lookup"><span data-stu-id="4af80-337">lineNumber</span></span> | `integer` | <span data-ttu-id="4af80-338">Номер строки скрипта JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="4af80-338">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="4af80-339">columnNumber</span><span class="sxs-lookup"><span data-stu-id="4af80-339">columnNumber</span></span> | `integer` | <span data-ttu-id="4af80-340">Номер столбца скрипта JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="4af80-340">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="4af80-341">Объект StackTrace</span><span class="sxs-lookup"><span data-stu-id="4af80-341">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="4af80-342">Кадры вызовов для утверждений или сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="4af80-342">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="4af80-343">Свойства</span><span class="sxs-lookup"><span data-stu-id="4af80-343">Properties</span></span> | <span data-ttu-id="4af80-344">Тип</span><span class="sxs-lookup"><span data-stu-id="4af80-344">Type</span></span> | <span data-ttu-id="4af80-345">Сведения</span><span class="sxs-lookup"><span data-stu-id="4af80-345">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="4af80-346">описание \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-346">description \(optional\)</span></span> | `string` | <span data-ttu-id="4af80-347">Строковая метка этого следа стека.</span><span class="sxs-lookup"><span data-stu-id="4af80-347">String label of this stack trace.</span></span>  <span data-ttu-id="4af80-348">Для следов async это может быть имя функции, которая инициировала вызов async.</span><span class="sxs-lookup"><span data-stu-id="4af80-348">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="4af80-349">callFrames</span><span class="sxs-lookup"><span data-stu-id="4af80-349">callFrames</span></span> | [<span data-ttu-id="4af80-350">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="4af80-350">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="4af80-351">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4af80-351">JavaScript function name.</span></span> |  
| <span data-ttu-id="4af80-352">родительский \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="4af80-352">parent \(optional\)</span></span> | [<span data-ttu-id="4af80-353">StackTrace</span><span class="sxs-lookup"><span data-stu-id="4af80-353">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="4af80-354">Асинхронный след стека JavaScript, предшествующий этому стеку, если доступен.</span><span class="sxs-lookup"><span data-stu-id="4af80-354">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
