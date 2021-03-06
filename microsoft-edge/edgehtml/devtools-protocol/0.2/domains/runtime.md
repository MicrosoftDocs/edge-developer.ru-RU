---
description: Ссылка на протокол DevTools Версии 0.2 (EdgeHTML) для домена runtime. Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.
title: Домен runtime — версия протокола DevTools 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: afc79a17c5002f60806872a9add57f518ff6cb45
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398142"
---
# <a name="runtime-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="0456d-106">Домен runtime — версия протокола DevTools 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="0456d-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="0456d-107">Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="0456d-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="0456d-108">Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="0456d-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="0456d-109">Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="0456d-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>  

| <span data-ttu-id="0456d-110">Категория</span><span class="sxs-lookup"><span data-stu-id="0456d-110">Classification</span></span> | <span data-ttu-id="0456d-111">Участники</span><span class="sxs-lookup"><span data-stu-id="0456d-111">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="0456d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="0456d-112">Methods</span></span>**](#methods) | <span data-ttu-id="0456d-113">[включить](#enable) [](#disable), отключить [,](#evaluate)оценить , [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="0456d-113">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |  
| [**<span data-ttu-id="0456d-114">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="0456d-114">Events</span></span>**](#events) | <span data-ttu-id="0456d-115">[executionContextCreated,](#executioncontextcreated) [executionContextDestroyed,](#executioncontextdestroyed) [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="0456d-115">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |  
| [**<span data-ttu-id="0456d-116">Типы</span><span class="sxs-lookup"><span data-stu-id="0456d-116">Types</span></span>**](#types) | <span data-ttu-id="0456d-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="0456d-117">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |  

## <a name="methods"></a><span data-ttu-id="0456d-118">Методы</span><span class="sxs-lookup"><span data-stu-id="0456d-118">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="0456d-119">"Включить"</span><span class="sxs-lookup"><span data-stu-id="0456d-119">enable</span></span>  

<span data-ttu-id="0456d-120">Включает отчеты `executionContextCreated` о `executionContextDestroyed` событиях и `executionContextsCleared` событиях.</span><span class="sxs-lookup"><span data-stu-id="0456d-120">Enables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  <span data-ttu-id="0456d-121">После включения отчетов `executionContextCreated` событие будет немедленно отправлено для каждого существующего контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-121">When the reporting gets enabled the `executionContextCreated` event will be sent immediately for each existing execution context.</span></span>  

---  

### <a name="disable"></a><span data-ttu-id="0456d-122">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="0456d-122">disable</span></span>  

<span data-ttu-id="0456d-123">Отключает отчеты `executionContextCreated` о `executionContextDestroyed` событиях и `executionContextsCleared` событиях.</span><span class="sxs-lookup"><span data-stu-id="0456d-123">Disables reporting of the `executionContextCreated`, `executionContextDestroyed`, and `executionContextsCleared` events.</span></span>  

---  

### <a name="evaluate"></a><span data-ttu-id="0456d-124">оценка</span><span class="sxs-lookup"><span data-stu-id="0456d-124">evaluate</span></span>  

<span data-ttu-id="0456d-125">Оценивает выражение на глобальном объекте.</span><span class="sxs-lookup"><span data-stu-id="0456d-125">Evaluates expression on global object.</span></span>  

| <span data-ttu-id="0456d-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-126">Parameters</span></span> | <span data-ttu-id="0456d-127">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-127">Type</span></span> | <span data-ttu-id="0456d-128">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-128">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-129">выражение</span><span class="sxs-lookup"><span data-stu-id="0456d-129">expression</span></span> | `string` | <span data-ttu-id="0456d-130">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="0456d-130">Expression to evaluate.</span></span> |  
| <span data-ttu-id="0456d-131">includeCommandLineAPI \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-131">includeCommandLineAPI \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-132">Определяет, должен ли API командной строки быть доступным во время оценки.</span><span class="sxs-lookup"><span data-stu-id="0456d-132">Determines whether Command Line API should be available during the evaluation.</span></span> |  
| <span data-ttu-id="0456d-133">objectGroup \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-133">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-134">Символическое имя группы, которое можно использовать для выпуска нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="0456d-134">Symbolic group name that can be used to release multiple objects.</span></span> |  
| <span data-ttu-id="0456d-135">silent \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-135">silent \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-136">В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="0456d-136">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span>  <span data-ttu-id="0456d-137">Переопределяет `setPauseOnException` состояние.</span><span class="sxs-lookup"><span data-stu-id="0456d-137">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="0456d-138">contextId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-138">contextId \(optional\)</span></span> | [<span data-ttu-id="0456d-139">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-139">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-140">Указывает, в котором контекст выполнения для выполнения оценки.</span><span class="sxs-lookup"><span data-stu-id="0456d-140">Specifies in which execution context to perform evaluation.</span></span>  <span data-ttu-id="0456d-141">Если параметр опущен, оценка будет выполнена в контексте проверенной страницы.</span><span class="sxs-lookup"><span data-stu-id="0456d-141">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span> |  
| <span data-ttu-id="0456d-142">returnByValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-142">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-143">Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению.</span><span class="sxs-lookup"><span data-stu-id="0456d-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  
| <span data-ttu-id="0456d-144">awaitPromise \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-144">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-145">Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="0456d-145">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  

| <span data-ttu-id="0456d-146">Возвращает</span><span class="sxs-lookup"><span data-stu-id="0456d-146">Returns</span></span> | <span data-ttu-id="0456d-147">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-147">Type</span></span> | <span data-ttu-id="0456d-148">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-148">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-149">результат</span><span class="sxs-lookup"><span data-stu-id="0456d-149">result</span></span> | [<span data-ttu-id="0456d-150">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-150">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-151">Результат оценки.</span><span class="sxs-lookup"><span data-stu-id="0456d-151">Evaluation result.</span></span> |  

---  

### <a name="callfunctionon"></a><span data-ttu-id="0456d-152">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="0456d-152">callFunctionOn</span></span>  

<span data-ttu-id="0456d-153">Функция вызовов с заданным объявлением на заданный объект.</span><span class="sxs-lookup"><span data-stu-id="0456d-153">Calls function with given declaration on the given object.</span></span>  <span data-ttu-id="0456d-154">Объектная группа результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-154">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="0456d-155">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-155">Parameters</span></span> | <span data-ttu-id="0456d-156">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-156">Type</span></span> | <span data-ttu-id="0456d-157">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-157">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-158">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="0456d-158">functionDeclaration</span></span> | `string` | <span data-ttu-id="0456d-159">Объявление функции вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-159">Declaration of the function to call.</span></span> |  
| <span data-ttu-id="0456d-160">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-160">objectId \(optional\)</span></span> | [<span data-ttu-id="0456d-161">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-161">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0456d-162">Идентификатор объекта для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="0456d-162">Identifier of the object to call function on.</span></span>  <span data-ttu-id="0456d-163">Либо `objectId` `executionContextId` заданы, либо должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="0456d-163">Either `objectId` or `executionContextId` should be specified.</span></span>  `objectId` <span data-ttu-id="0456d-164">должно быть из `Runtime.evaluate()` функции.</span><span class="sxs-lookup"><span data-stu-id="0456d-164">must be from the `Runtime.evaluate()` function.</span></span> |  
| <span data-ttu-id="0456d-165">аргументы \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-165">arguments \(optional\)</span></span> | [<span data-ttu-id="0456d-166">CallArgument[]</span><span class="sxs-lookup"><span data-stu-id="0456d-166">CallArgument[]</span></span>](#callargument) | <span data-ttu-id="0456d-167">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-167">Call arguments.</span></span>  <span data-ttu-id="0456d-168">Все аргументы вызовов должны принадлежать одному миру JavaScript как целевому объекту.</span><span class="sxs-lookup"><span data-stu-id="0456d-168">All call arguments must belong to the same JavaScript world as the target object.</span></span> |  
| <span data-ttu-id="0456d-169">boolean \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-169">boolean \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-170">В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="0456d-170">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="0456d-171">Переопределяет `setPauseOnException` состояние.</span><span class="sxs-lookup"><span data-stu-id="0456d-171">Overrides `setPauseOnException` state.</span></span> |  
| <span data-ttu-id="0456d-172">returnByValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-172">returnByValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-173">Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению.</span><span class="sxs-lookup"><span data-stu-id="0456d-173">Whether the result is expected to be a JSON object which should be sent by value.</span></span> |  
| <span data-ttu-id="0456d-174">awaitPromise \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-174">awaitPromise \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-175">Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="0456d-175">Whether execution should `await` for resulting value and return once awaited promise is resolved.</span></span> |  
| <span data-ttu-id="0456d-176">executionContextId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-176">executionContextId \(optional\)</span></span> | [<span data-ttu-id="0456d-177">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-177">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-178">Указывает контекст выполнения, на котором будет использоваться глобальный объект для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="0456d-178">Specifies execution context which global object will be used to call function on.</span></span>  <span data-ttu-id="0456d-179">Либо</span><span class="sxs-lookup"><span data-stu-id="0456d-179">Either</span></span>
`executionContextId` <span data-ttu-id="0456d-180">или `objectId` должны быть указаны</span><span class="sxs-lookup"><span data-stu-id="0456d-180">or `objectId` should be specified</span></span> |  
| <span data-ttu-id="0456d-181">objectGroup \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-181">objectGroup \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-182">Символическое имя группы, которое можно использовать для выпуска нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="0456d-182">Symbolic group name that can be used to release multiple objects.</span></span>  <span data-ttu-id="0456d-183">Если `objectGroup` не указано и `objectId` является, будет `objectGroup` унаследовано от объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-183">If `objectGroup` is not specified and `objectId` is, `objectGroup` will be inherited from object.</span></span> |  

| <span data-ttu-id="0456d-184">Возвращает</span><span class="sxs-lookup"><span data-stu-id="0456d-184">Returns</span></span> | <span data-ttu-id="0456d-185">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-185">Type</span></span> | <span data-ttu-id="0456d-186">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-186">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-187">результат</span><span class="sxs-lookup"><span data-stu-id="0456d-187">result</span></span> | [<span data-ttu-id="0456d-188">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-188">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-189">Результат вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-189">Call result.</span></span> |  

---  

### <a name="awaitpromise"></a><span data-ttu-id="0456d-190">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="0456d-190">awaitPromise</span></span>  

<span data-ttu-id="0456d-191">Добавьте обработник, чтобы обещать с данным id объекта обещания.</span><span class="sxs-lookup"><span data-stu-id="0456d-191">Add handler to promise with given promise object id.</span></span>  

| <span data-ttu-id="0456d-192">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-192">Parameters</span></span> | <span data-ttu-id="0456d-193">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-193">Type</span></span> | <span data-ttu-id="0456d-194">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-194">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-195">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-195">promiseObjectId</span></span> | [<span data-ttu-id="0456d-196">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-196">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0456d-197">Идентификатор обещания.</span><span class="sxs-lookup"><span data-stu-id="0456d-197">Identifier of the promise.</span></span> |  
| <span data-ttu-id="0456d-198">returnByValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-198">returnByValue \(optional\)</span></span> | <span data-ttu-id="0456d-199">логический</span><span class="sxs-lookup"><span data-stu-id="0456d-199">boolean</span></span> | <span data-ttu-id="0456d-200">Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению.</span><span class="sxs-lookup"><span data-stu-id="0456d-200">Whether the result is expected to be a JSON object that should be sent by value.</span></span> |  

| <span data-ttu-id="0456d-201">Возвращает</span><span class="sxs-lookup"><span data-stu-id="0456d-201">Returns</span></span> | <span data-ttu-id="0456d-202">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-202">Type</span></span> | <span data-ttu-id="0456d-203">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-203">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-204">результат</span><span class="sxs-lookup"><span data-stu-id="0456d-204">result</span></span> | [<span data-ttu-id="0456d-205">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-205">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-206">Результат promise.</span><span class="sxs-lookup"><span data-stu-id="0456d-206">Promise result.</span></span>  <span data-ttu-id="0456d-207">Будет содержать отклоненные значения, если обещание было отклонено.</span><span class="sxs-lookup"><span data-stu-id="0456d-207">Will contain rejected value if promise was rejected.</span></span> |  

---  

### <a name="getproperties"></a><span data-ttu-id="0456d-208">getProperties</span><span class="sxs-lookup"><span data-stu-id="0456d-208">getProperties</span></span>  

<span data-ttu-id="0456d-209">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-209">Returns properties of a given object.</span></span> <span data-ttu-id="0456d-210">Объектная группа результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-210">Object group of the result is inherited from the target object.</span></span>  

| <span data-ttu-id="0456d-211">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-211">Parameters</span></span> | <span data-ttu-id="0456d-212">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-212">Type</span></span> | <span data-ttu-id="0456d-213">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-213">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-214">objectId</span><span class="sxs-lookup"><span data-stu-id="0456d-214">objectId</span></span> | [<span data-ttu-id="0456d-215">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-215">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0456d-216">Идентификатор объекта для возврата свойств.</span><span class="sxs-lookup"><span data-stu-id="0456d-216">Identifier of the object to return properties for.</span></span>  `objectId` <span data-ttu-id="0456d-217">должно быть из `Debugger.evaluateOnCallFrame()` функции.</span><span class="sxs-lookup"><span data-stu-id="0456d-217">must be from the `Debugger.evaluateOnCallFrame()` function.</span></span> |  
| <span data-ttu-id="0456d-218">ownProperties \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-218">ownProperties \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-219">Если `true` возвращает свойства, принадлежащие только самому элементу, а не цепочке прототипов.</span><span class="sxs-lookup"><span data-stu-id="0456d-219">If `true`, returns properties belonging only to the element itself, not to its prototype chain.</span></span> |  
| <span data-ttu-id="0456d-220">accessorPropertiesOnly \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-220">accessorPropertiesOnly \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-221">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="0456d-221">**Experimental**.</span></span>  <span data-ttu-id="0456d-222">Если `true` , возвращает свойства вспомогательного оборудования \(с getter/setter\) только; внутренние свойства также не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="0456d-222">If `true`, returns accessor properties \(with getter/setter\) only; internal properties are not returned either.</span></span> |  

| <span data-ttu-id="0456d-223">Возвращает</span><span class="sxs-lookup"><span data-stu-id="0456d-223">Returns</span></span> | <span data-ttu-id="0456d-224">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-224">Type</span></span> | <span data-ttu-id="0456d-225">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-225">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-226">результат</span><span class="sxs-lookup"><span data-stu-id="0456d-226">result</span></span> | [<span data-ttu-id="0456d-227">PropertyDescriptor[]</span><span class="sxs-lookup"><span data-stu-id="0456d-227">PropertyDescriptor[]</span></span>](#propertydescriptor) | <span data-ttu-id="0456d-228">Свойства объектов.</span><span class="sxs-lookup"><span data-stu-id="0456d-228">Object properties.</span></span> |  

---  

### <a name="globallexicalscopenames"></a><span data-ttu-id="0456d-229">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="0456d-229">globalLexicalScopeNames</span></span>  

<span data-ttu-id="0456d-230">Возвращает все переменные let, const и class из глобальной области консоли.</span><span class="sxs-lookup"><span data-stu-id="0456d-230">Returns all let, const, and class variables from the console global scope.</span></span>  

| <span data-ttu-id="0456d-231">Возвращает</span><span class="sxs-lookup"><span data-stu-id="0456d-231">Returns</span></span> | <span data-ttu-id="0456d-232">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-232">Type</span></span> | <span data-ttu-id="0456d-233">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-233">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-234">имена</span><span class="sxs-lookup"><span data-stu-id="0456d-234">names</span></span> | `string[]` | &nbsp; |  

---  

### <a name="releaseobject"></a><span data-ttu-id="0456d-235">releaseObject</span><span class="sxs-lookup"><span data-stu-id="0456d-235">releaseObject</span></span>  

<span data-ttu-id="0456d-236">Выпускает удаленный объект с заданным ID.</span><span class="sxs-lookup"><span data-stu-id="0456d-236">Releases remote object with given ID.</span></span>  

| <span data-ttu-id="0456d-237">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-237">Parameters</span></span> | <span data-ttu-id="0456d-238">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-238">Type</span></span> | <span data-ttu-id="0456d-239">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-239">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-240">objectId</span><span class="sxs-lookup"><span data-stu-id="0456d-240">objectId</span></span> | [<span data-ttu-id="0456d-241">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-241">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0456d-242">Идентификатор объекта для выпуска.</span><span class="sxs-lookup"><span data-stu-id="0456d-242">Identifier of the object to release.</span></span> |  

---  

### <a name="releaseobjectgroup"></a><span data-ttu-id="0456d-243">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="0456d-243">releaseObjectGroup</span></span>  

<span data-ttu-id="0456d-244">Освобождает все удаленные объекты, принадлежащие к данной группе.</span><span class="sxs-lookup"><span data-stu-id="0456d-244">Releases all remote objects that belong to a given group.</span></span>  

| <span data-ttu-id="0456d-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-245">Parameters</span></span> | <span data-ttu-id="0456d-246">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-246">Type</span></span> | <span data-ttu-id="0456d-247">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-247">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-248">objectGroup</span><span class="sxs-lookup"><span data-stu-id="0456d-248">objectGroup</span></span> | `string` | <span data-ttu-id="0456d-249">Символическое имя группы объектов.</span><span class="sxs-lookup"><span data-stu-id="0456d-249">Symbolic object group name.</span></span> |  

---  

### <a name="discardconsoleentries"></a><span data-ttu-id="0456d-250">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="0456d-250">discardConsoleEntries</span></span>  

<span data-ttu-id="0456d-251">Удаляет собранные исключения и вызовы API консоли.</span><span class="sxs-lookup"><span data-stu-id="0456d-251">Discards collected exceptions and console API calls.</span></span>  

---  

## <a name="events"></a><span data-ttu-id="0456d-252">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="0456d-252">Events</span></span>  

### <a name="executioncontextcreated"></a><span data-ttu-id="0456d-253">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="0456d-253">executionContextCreated</span></span>  

<span data-ttu-id="0456d-254">Выдан при новом контексте выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-254">Issued when new execution context is created.</span></span>  

| <span data-ttu-id="0456d-255">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-255">Parameters</span></span> | <span data-ttu-id="0456d-256">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-256">Type</span></span> | <span data-ttu-id="0456d-257">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-257">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-258">контекст</span><span class="sxs-lookup"><span data-stu-id="0456d-258">context</span></span> | [<span data-ttu-id="0456d-259">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="0456d-259">ExecutionContextDescription</span></span>](#executioncontextdescription) | <span data-ttu-id="0456d-260">Вновь созданный контекст выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-260">A newly created execution context.</span></span> |  

---  

### <a name="executioncontextdestroyed"></a><span data-ttu-id="0456d-261">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="0456d-261">executionContextDestroyed</span></span>  

<span data-ttu-id="0456d-262">Выдана при уничтожении контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-262">Issued when execution context is destroyed.</span></span>  

| <span data-ttu-id="0456d-263">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-263">Parameters</span></span> | <span data-ttu-id="0456d-264">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-264">Type</span></span> | <span data-ttu-id="0456d-265">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-265">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-266">executionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-266">executionContextId</span></span> | [<span data-ttu-id="0456d-267">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-267">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-268">ID разрушенного контекста.</span><span class="sxs-lookup"><span data-stu-id="0456d-268">ID of the destroyed context.</span></span> |  

---  

### <a name="executioncontextscleared"></a><span data-ttu-id="0456d-269">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="0456d-269">executionContextsCleared</span></span>  

<span data-ttu-id="0456d-270">Выдан, когда все executionContexts были очищены в браузере.</span><span class="sxs-lookup"><span data-stu-id="0456d-270">Issued when all executionContexts were cleared in browser.</span></span>  

&nbsp;  

---  

### <a name="exceptionthrown"></a><span data-ttu-id="0456d-271">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="0456d-271">exceptionThrown</span></span>  

<span data-ttu-id="0456d-272">Выдано, когда исключение было выброшено и ненаблюдаемо.</span><span class="sxs-lookup"><span data-stu-id="0456d-272">Issued when exception was thrown and unhandled.</span></span>  

| <span data-ttu-id="0456d-273">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-273">Parameters</span></span> | <span data-ttu-id="0456d-274">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-274">Type</span></span> | <span data-ttu-id="0456d-275">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-275">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-276">timestamp</span><span class="sxs-lookup"><span data-stu-id="0456d-276">timestamp</span></span> | [<span data-ttu-id="0456d-277">Метка времени</span><span class="sxs-lookup"><span data-stu-id="0456d-277">Timestamp</span></span>](#timestamp) | <span data-ttu-id="0456d-278">Timestamp исключения.</span><span class="sxs-lookup"><span data-stu-id="0456d-278">Timestamp of the exception.</span></span> |  
| <span data-ttu-id="0456d-279">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0456d-279">exceptionDetails</span></span> | [<span data-ttu-id="0456d-280">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0456d-280">ExceptionDetails</span></span>](#exceptiondetails) | &nbsp; |  

---  

### <a name="consoleapicalled"></a><span data-ttu-id="0456d-281">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="0456d-281">consoleAPICalled</span></span>  

| <span data-ttu-id="0456d-282">Параметры</span><span class="sxs-lookup"><span data-stu-id="0456d-282">Parameters</span></span> | <span data-ttu-id="0456d-283">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-283">Type</span></span> | <span data-ttu-id="0456d-284">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-284">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-285">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-285">type</span></span> | `string` | <span data-ttu-id="0456d-286">Тип вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-286">Type of the call.</span></span>  <span data-ttu-id="0456d-287">Допустимые значения: `log` , , , , , `info` `warning` `error` `debug` `assert` `table` `trace` `dir` `dirxml` `clear` `select` `count` `countReset` `timeEnd` `timeStamp` `startGroup` и `startGroupCollapsed`</span><span class="sxs-lookup"><span data-stu-id="0456d-287">Allowed values:  `log`, `info`, `warning`, `error`, `debug`, `assert`, `table`, `trace`, `dir`, `dirxml`, `clear`, `select`, `count`, `countReset`, `timeEnd`, `timeStamp`, `startGroup`, `startGroupCollapsed`, and</span></span> `endGroup` |  
| <span data-ttu-id="0456d-288">args</span><span class="sxs-lookup"><span data-stu-id="0456d-288">args</span></span> | <span data-ttu-id="0456d-289">[RemoteObject[]] (#remoteobject</span><span class="sxs-lookup"><span data-stu-id="0456d-289">[RemoteObject[]](#remoteobject</span></span> | <span data-ttu-id="0456d-290">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-290">Call arguments.</span></span> |  
| <span data-ttu-id="0456d-291">executionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-291">executionContextId</span></span> | [<span data-ttu-id="0456d-292">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-292">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-293">Идентификатор контекста, в котором был выполнен вызов консоли.</span><span class="sxs-lookup"><span data-stu-id="0456d-293">Identifier of the context where console call was made.</span></span> |  
| <span data-ttu-id="0456d-294">timestamp \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-294">timestamp \(optional\)</span></span> | [<span data-ttu-id="0456d-295">Метка времени</span><span class="sxs-lookup"><span data-stu-id="0456d-295">Timestamp</span></span>](#timestamp) | <span data-ttu-id="0456d-296">Время вызова.</span><span class="sxs-lookup"><span data-stu-id="0456d-296">Call timestamp.</span></span> |  
| <span data-ttu-id="0456d-297">stackTrace \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-297">stackTrace \(optional\)</span></span> | [<span data-ttu-id="0456d-298">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0456d-298">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0456d-299">Стек трассировки, захваченный при наличии.</span><span class="sxs-lookup"><span data-stu-id="0456d-299">Stack trace captured if available.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="0456d-300">Типы</span><span class="sxs-lookup"><span data-stu-id="0456d-300">Types</span></span>  

### <a name="scriptid-string"></a><span data-ttu-id="0456d-301">Строка ScriptId</span><span class="sxs-lookup"><span data-stu-id="0456d-301">ScriptId string</span></span>  

<a name="scriptid"></a>

<span data-ttu-id="0456d-302">Уникальный идентификатор скрипта.</span><span class="sxs-lookup"><span data-stu-id="0456d-302">Unique script identifier.</span></span>  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a><span data-ttu-id="0456d-303">Строка RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-303">RemoteObjectId string</span></span>  

<a name="remoteobjectid"></a>

<span data-ttu-id="0456d-304">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-304">Unique object identifier.</span></span>  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a><span data-ttu-id="0456d-305">Строка UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0456d-305">UnserializableValue string</span></span>  

<a name="unserializablevalue"></a>  

<span data-ttu-id="0456d-306">Примитивное значение, которое не может быть строкифицировано JSON.</span><span class="sxs-lookup"><span data-stu-id="0456d-306">Primitive value which cannot be JSON-stringified.</span></span>  

##### <a name="allowed-values"></a><span data-ttu-id="0456d-307">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="0456d-307">Allowed Values</span></span>  

`Infinity`<span data-ttu-id="0456d-308">, `NaN`, `-Infinity`,</span><span class="sxs-lookup"><span data-stu-id="0456d-308">, `NaN`, `-Infinity`,</span></span> `-0`  

---  

### <a name="remoteobject-object"></a><span data-ttu-id="0456d-309">Объект RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-309">RemoteObject object</span></span>  

<a name="remoteobject"></a>  

<span data-ttu-id="0456d-310">Объект Mirror, отсылающий к исходному объекту JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0456d-310">Mirror object referencing original JavaScript object.</span></span>  

| <span data-ttu-id="0456d-311">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-311">Properties</span></span> | <span data-ttu-id="0456d-312">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-312">Type</span></span> | <span data-ttu-id="0456d-313">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-313">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-314">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-314">type</span></span> | `string` | <span data-ttu-id="0456d-315">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-315">Object type.</span></span>  <span data-ttu-id="0456d-316">Допустимые значения:  `object` , , , , , `function` `undefined` `string` `number` `boolean` и</span><span class="sxs-lookup"><span data-stu-id="0456d-316">Allowed values:  `object`, `function`, `undefined`, `string`, `number`, `boolean`, and</span></span> `symbol` |  
| <span data-ttu-id="0456d-317">подтип \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-317">subtype \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-318">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-318">Object subtype hint.</span></span>  <span data-ttu-id="0456d-319">Только для `object` значений типа.</span><span class="sxs-lookup"><span data-stu-id="0456d-319">Specified for `object` type values only.</span></span>  <span data-ttu-id="0456d-320">Допустимые значения:  `null` `error` , `promise` и</span><span class="sxs-lookup"><span data-stu-id="0456d-320">Allowed values:  `null`, `error`, `promise`, and</span></span> `node` |  
| <span data-ttu-id="0456d-321">className \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-321">className \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-322">Имя объекта класса \(конструктор\).</span><span class="sxs-lookup"><span data-stu-id="0456d-322">Object class \(constructor\) name.</span></span>  <span data-ttu-id="0456d-323">Только для `object` значений типа.</span><span class="sxs-lookup"><span data-stu-id="0456d-323">Specified for `object` type values only.</span></span> |  
| <span data-ttu-id="0456d-324">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-324">value \(optional\)</span></span> | `any` | <span data-ttu-id="0456d-325">Значение удаленного объекта в случае примитивных значений или значений JSON \(если оно было запророшно\).</span><span class="sxs-lookup"><span data-stu-id="0456d-325">Remote object value in case of primitive values or JSON values \(if it was requested\).</span></span> |  
| <span data-ttu-id="0456d-326">unserializableValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-326">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="0456d-327">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0456d-327">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="0456d-328">Примитивное значение, которое не может быть JSON-stringified, не `value` имеет, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="0456d-328">Primitive value which can not be JSON-stringified does not have `value`, but gets this property.</span></span> |  
| <span data-ttu-id="0456d-329">описание \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-329">description \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-330">Строковая репрезентация объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-330">String representation of the object.</span></span> |  
| <span data-ttu-id="0456d-331">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-331">objectId \(optional\)</span></span> | [<span data-ttu-id="0456d-332">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="0456d-332">RemoteObjectId</span></span>](#remoteobjectid) | <span data-ttu-id="0456d-333">Уникальный идентификатор объекта \(для небытийных значений\).</span><span class="sxs-lookup"><span data-stu-id="0456d-333">Unique object identifier \(for non-primitive values\).</span></span> |  
| <span data-ttu-id="0456d-334">msDebuggerPropertyId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-334">msDebuggerPropertyId \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-335">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="0456d-335">**Experimental**.</span></span>  <span data-ttu-id="0456d-336">Microsoft. Связанный с этим объектом ID свойства отладки.</span><span class="sxs-lookup"><span data-stu-id="0456d-336">Microsoft:  The associated debugger property ID for this object.</span></span> |  

---  

### <a name="propertydescriptor-object"></a><span data-ttu-id="0456d-337">Объект PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="0456d-337">PropertyDescriptor object</span></span>  

<a name="propertydescriptor"></a>  

<span data-ttu-id="0456d-338">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-338">Object property descriptor.</span></span>  

| <span data-ttu-id="0456d-339">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-339">Properties</span></span> | <span data-ttu-id="0456d-340">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-340">Type</span></span> | <span data-ttu-id="0456d-341">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-341">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-342">name</span><span class="sxs-lookup"><span data-stu-id="0456d-342">name</span></span> | `string` | <span data-ttu-id="0456d-343">Имя свойства или описание символа.</span><span class="sxs-lookup"><span data-stu-id="0456d-343">Property name or symbol description.</span></span> |  
| <span data-ttu-id="0456d-344">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-344">value \(optional\)</span></span> | [<span data-ttu-id="0456d-345">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-345">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-346">Значение, связанное с свойством.</span><span class="sxs-lookup"><span data-stu-id="0456d-346">The value associated with the property.</span></span> |  
| <span data-ttu-id="0456d-347">writable \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-347">writable \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0456d-348">если значение, связанное с свойством, может быть изменено \(только дескрипторы данных\).</span><span class="sxs-lookup"><span data-stu-id="0456d-348">if the value associated with the property may be changed \(data descriptors only\).</span></span> |  
| <span data-ttu-id="0456d-349">получить \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-349">get \(optional\)</span></span> | [<span data-ttu-id="0456d-350">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-350">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-351">Функция, которая служит в качестве геттера для свойства, или если нет геттера `undefined` \(только дескрипторы аксессуара\).</span><span class="sxs-lookup"><span data-stu-id="0456d-351">A function which serves as a getter for the property, or `undefined` if there is no getter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="0456d-352">set \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-352">set \(optional\)</span></span> | [<span data-ttu-id="0456d-353">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-353">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-354">Функция, которая служит сеттером для свойства или если нет сеттера `undefined` \(только дескрипторы аксессуара\).</span><span class="sxs-lookup"><span data-stu-id="0456d-354">A function which serves as a setter for the property, or `undefined` if there is no setter \(accessor descriptors only\).</span></span> |  
| <span data-ttu-id="0456d-355">настраиваемый</span><span class="sxs-lookup"><span data-stu-id="0456d-355">configurable</span></span> | `boolean` | `True` <span data-ttu-id="0456d-356">если тип этого дескриптора свойства может быть изменен и если свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-356">if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span> |  
| <span data-ttu-id="0456d-357">переоменимый</span><span class="sxs-lookup"><span data-stu-id="0456d-357">enumerable</span></span> | `boolean` | `True` <span data-ttu-id="0456d-358">если это свойство появляется во время переопечатки свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-358">if this property shows up during enumeration of the properties on the corresponding object.</span></span> |  
| <span data-ttu-id="0456d-359">wasThrown \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-359">wasThrown \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0456d-360">если результат был брошен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="0456d-360">if the result was thrown during the evaluation.</span></span> |  
| <span data-ttu-id="0456d-361">isOwn \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-361">isOwn \(optional\)</span></span> | `boolean` | `True` <span data-ttu-id="0456d-362">если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="0456d-362">if the property is owned for the object.</span></span> |  
| <span data-ttu-id="0456d-363">msReturnValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-363">msReturnValue \(optional\)</span></span> | `boolean` | <span data-ttu-id="0456d-364">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="0456d-364">**Experimental**.</span></span>  <span data-ttu-id="0456d-365">Майкрософт:  `True` если свойство является возвращаемой величиной.</span><span class="sxs-lookup"><span data-stu-id="0456d-365">Microsoft:  `True` if the property is a return value.</span></span> |  
| <span data-ttu-id="0456d-366">символ \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-366">symbol \(optional\)</span></span> | [<span data-ttu-id="0456d-367">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-367">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-368">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="0456d-368">Property symbol object, if the property is of the `symbol` type.</span></span> |  

---  

### <a name="callargument-object"></a><span data-ttu-id="0456d-369">Объект CallArgument</span><span class="sxs-lookup"><span data-stu-id="0456d-369">CallArgument object</span></span>  

<a name="callargument"></a>  

<span data-ttu-id="0456d-370">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="0456d-370">Represents function call argument.</span></span>  <span data-ttu-id="0456d-371">Либо удаленный ID объекта, примитивный, несериализируемый примитивный значение, либо `objectId` `value` ни \(для неопределимых\) они не должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="0456d-371">Either remote object ID `objectId`, primitive `value`, unserializable primitive value, or neither of \(for undefined\) them should be specified.</span></span>  

| <span data-ttu-id="0456d-372">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-372">Properties</span></span> | <span data-ttu-id="0456d-373">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-373">Type</span></span> | <span data-ttu-id="0456d-374">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-374">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-375">значение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-375">value \(optional\)</span></span> | `any` | <span data-ttu-id="0456d-376">Примитивное значение или серийный объект javascript.</span><span class="sxs-lookup"><span data-stu-id="0456d-376">Primitive value or serializable javascript object.</span></span> |  
| <span data-ttu-id="0456d-377">unserializableValue \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-377">unserializableValue \(optional\)</span></span> | [<span data-ttu-id="0456d-378">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="0456d-378">UnserializableValue</span></span>](#unserializablevalue) | <span data-ttu-id="0456d-379">Примитивное значение, которое не может быть jSON-stringified.</span><span class="sxs-lookup"><span data-stu-id="0456d-379">Primitive value which can not be JSON-stringified.</span></span> |  
| <span data-ttu-id="0456d-380">objectId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-380">objectId \(optional\)</span></span> | <span data-ttu-id="0456d-381">[RemoteObjectId](#remoteobjectid)]</span><span class="sxs-lookup"><span data-stu-id="0456d-381">[RemoteObjectId](#remoteobjectid)]</span></span> | <span data-ttu-id="0456d-382">Удаленная ручка объекта.</span><span class="sxs-lookup"><span data-stu-id="0456d-382">Remote object handle.</span></span> |  

---  

### <a name="executioncontextid-integer"></a><span data-ttu-id="0456d-383">Integer executionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-383">ExecutionContextId integer</span></span>  

<a name="executioncontextid"></a>  

<span data-ttu-id="0456d-384">ID контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-384">ID of an execution context.</span></span>  

&nbsp;  

---  

### <a name="executioncontextdescription-object"></a><span data-ttu-id="0456d-385">Объект ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="0456d-385">ExecutionContextDescription object</span></span>  

<a name="executioncontextdescription"></a>  

<span data-ttu-id="0456d-386">Описание изолированного мира.</span><span class="sxs-lookup"><span data-stu-id="0456d-386">Description of an isolated world.</span></span>  

| <span data-ttu-id="0456d-387">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-387">Properties</span></span> | <span data-ttu-id="0456d-388">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-388">Type</span></span> | <span data-ttu-id="0456d-389">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-389">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-390">id</span><span class="sxs-lookup"><span data-stu-id="0456d-390">id</span></span> | [<span data-ttu-id="0456d-391">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-391">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-392">Уникальный ID контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-392">Unique ID of the execution context.</span></span>  <span data-ttu-id="0456d-393">Его можно использовать для указания контекста выполнения</span><span class="sxs-lookup"><span data-stu-id="0456d-393">It can be used to specify in which execution context</span></span>
<span data-ttu-id="0456d-394">Необходимо выполнить оценку скрипта.</span><span class="sxs-lookup"><span data-stu-id="0456d-394">script evaluation should be performed.</span></span> |  
| <span data-ttu-id="0456d-395">происхождение</span><span class="sxs-lookup"><span data-stu-id="0456d-395">origin</span></span> | `string` | <span data-ttu-id="0456d-396">Происхождение контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="0456d-396">Execution context origin.</span></span> |  
| <span data-ttu-id="0456d-397">name</span><span class="sxs-lookup"><span data-stu-id="0456d-397">name</span></span> | `string` | <span data-ttu-id="0456d-398">Имя, которое можно прочитать, описывая данный контекст.</span><span class="sxs-lookup"><span data-stu-id="0456d-398">Human readable name describing given context.</span></span> |  

---  

### <a name="exceptiondetails-object"></a><span data-ttu-id="0456d-399">Объект ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="0456d-399">ExceptionDetails object</span></span>  

<a name="exceptiondetails"></a>  

<span data-ttu-id="0456d-400">Подробные сведения об исключении (или ошибке), которое было выброшено во время компиляции или выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="0456d-400">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>  

| <span data-ttu-id="0456d-401">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-401">Properties</span></span> | <span data-ttu-id="0456d-402">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-402">Type</span></span> | <span data-ttu-id="0456d-403">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-403">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-404">exceptionId</span><span class="sxs-lookup"><span data-stu-id="0456d-404">exceptionId</span></span> | `integer` | <span data-ttu-id="0456d-405">ID исключения.</span><span class="sxs-lookup"><span data-stu-id="0456d-405">Exception ID.</span></span> |  
| <span data-ttu-id="0456d-406">текст</span><span class="sxs-lookup"><span data-stu-id="0456d-406">text</span></span> | `string` | <span data-ttu-id="0456d-407">Текст исключения, который следует использовать вместе с объектом исключения при наличии.</span><span class="sxs-lookup"><span data-stu-id="0456d-407">Exception text, which should be used together with exception object when available.</span></span> |  
| <span data-ttu-id="0456d-408">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0456d-408">lineNumber</span></span> | `integer` | <span data-ttu-id="0456d-409">Номер строки расположения исключения \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0456d-409">Line number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="0456d-410">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0456d-410">columnNumber</span></span> | `integer` | <span data-ttu-id="0456d-411">Номер столбца расположения исключения \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0456d-411">Column number of the exception location \(0-based\).</span></span> |  
| <span data-ttu-id="0456d-412">scriptId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-412">scriptId \(optional\)</span></span> | [<span data-ttu-id="0456d-413">ScriptId</span><span class="sxs-lookup"><span data-stu-id="0456d-413">ScriptId</span></span>](#scriptid) | <span data-ttu-id="0456d-414">ID сценария расположения исключений.</span><span class="sxs-lookup"><span data-stu-id="0456d-414">Script ID of the exception location.</span></span> |  
| <span data-ttu-id="0456d-415">URL\(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-415">url \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-416">URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан.</span><span class="sxs-lookup"><span data-stu-id="0456d-416">URL of the exception location, to be used when the script was not reported.</span></span> |  
| <span data-ttu-id="0456d-417">stackTrace \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-417">stackTrace \(optional\)</span></span> | [<span data-ttu-id="0456d-418">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0456d-418">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0456d-419">Трассировка стека JavaScript при наличии.</span><span class="sxs-lookup"><span data-stu-id="0456d-419">JavaScript stack trace if available.</span></span> |  
| <span data-ttu-id="0456d-420">исключение \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-420">exception \(optional\)</span></span> | [<span data-ttu-id="0456d-421">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="0456d-421">RemoteObject</span></span>](#remoteobject) | <span data-ttu-id="0456d-422">Объект Исключения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="0456d-422">Exception object if available.</span></span> |  
| <span data-ttu-id="0456d-423">executionContextId \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-423">executionContextId \(optional\)</span></span> | [<span data-ttu-id="0456d-424">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="0456d-424">ExecutionContextId</span></span>](#executioncontextid) | <span data-ttu-id="0456d-425">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="0456d-425">Identifier of the context where exception happened.</span></span> |  

---  

### <a name="timestamp-integer"></a><span data-ttu-id="0456d-426">Integer Timestamp</span><span class="sxs-lookup"><span data-stu-id="0456d-426">Timestamp integer</span></span>  

<a name="timestamp"></a>  

<span data-ttu-id="0456d-427">Количество миллисекунд с эпохи.</span><span class="sxs-lookup"><span data-stu-id="0456d-427">Number of milliseconds since epoch.</span></span>  

&nbsp;  

---  

### <a name="callframe-object"></a><span data-ttu-id="0456d-428">Объект CallFrame</span><span class="sxs-lookup"><span data-stu-id="0456d-428">CallFrame object</span></span>  

<a name="callframe"></a>  

<span data-ttu-id="0456d-429">Стек записи для ошибок и утверждений во время работы.</span><span class="sxs-lookup"><span data-stu-id="0456d-429">Stack entry for runtime errors and assertions.</span></span>  

| <span data-ttu-id="0456d-430">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-430">Properties</span></span> | <span data-ttu-id="0456d-431">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-431">Type</span></span> | <span data-ttu-id="0456d-432">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-432">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-433">functionName</span><span class="sxs-lookup"><span data-stu-id="0456d-433">functionName</span></span> | `string` | <span data-ttu-id="0456d-434">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0456d-434">JavaScript function name.</span></span> |  
| <span data-ttu-id="0456d-435">scriptId</span><span class="sxs-lookup"><span data-stu-id="0456d-435">scriptId</span></span> | [<span data-ttu-id="0456d-436">ScriptId</span><span class="sxs-lookup"><span data-stu-id="0456d-436">ScriptId</span></span>](#scriptid) | <span data-ttu-id="0456d-437">ID скрипта JavaScript. ScriptId будет пустым, если отладка не включена.</span><span class="sxs-lookup"><span data-stu-id="0456d-437">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span> |  
| <span data-ttu-id="0456d-438">url</span><span class="sxs-lookup"><span data-stu-id="0456d-438">url</span></span> | `string` | <span data-ttu-id="0456d-439">Имя сценария JavaScript или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="0456d-439">JavaScript script name or url.</span></span> |  
| <span data-ttu-id="0456d-440">lineNumber</span><span class="sxs-lookup"><span data-stu-id="0456d-440">lineNumber</span></span> | `integer` | <span data-ttu-id="0456d-441">Номер строки скрипта JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0456d-441">JavaScript script line number \(0-based\).</span></span> |  
| <span data-ttu-id="0456d-442">columnNumber</span><span class="sxs-lookup"><span data-stu-id="0456d-442">columnNumber</span></span> | <span data-ttu-id="0456d-443">integer</span><span class="sxs-lookup"><span data-stu-id="0456d-443">integer</span></span> | <span data-ttu-id="0456d-444">Номер столбца скрипта JavaScript \(0-based\).</span><span class="sxs-lookup"><span data-stu-id="0456d-444">JavaScript script column number \(0-based\).</span></span> |  

---  

### <a name="stacktrace-object"></a><span data-ttu-id="0456d-445">Объект StackTrace</span><span class="sxs-lookup"><span data-stu-id="0456d-445">StackTrace object</span></span>  

<a name="stacktrace"></a>  

<span data-ttu-id="0456d-446">Кадры вызовов для утверждений или сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0456d-446">Call frames for assertions or error messages.</span></span>  

| <span data-ttu-id="0456d-447">Свойства</span><span class="sxs-lookup"><span data-stu-id="0456d-447">Properties</span></span> | <span data-ttu-id="0456d-448">Тип</span><span class="sxs-lookup"><span data-stu-id="0456d-448">Type</span></span> | <span data-ttu-id="0456d-449">Сведения</span><span class="sxs-lookup"><span data-stu-id="0456d-449">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="0456d-450">описание \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-450">description \(optional\)</span></span> | `string` | <span data-ttu-id="0456d-451">Строковая метка этого следа стека.</span><span class="sxs-lookup"><span data-stu-id="0456d-451">String label of this stack trace.</span></span>  <span data-ttu-id="0456d-452">Для следов async это может быть имя функции, которая инициировала вызов async.</span><span class="sxs-lookup"><span data-stu-id="0456d-452">For async traces this may be a name of the function that initiated the async call.</span></span> |  
| <span data-ttu-id="0456d-453">callFrames</span><span class="sxs-lookup"><span data-stu-id="0456d-453">callFrames</span></span> | [<span data-ttu-id="0456d-454">CallFrame[]</span><span class="sxs-lookup"><span data-stu-id="0456d-454">CallFrame[]</span></span>](#callframe) | <span data-ttu-id="0456d-455">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0456d-455">JavaScript function name.</span></span> |  
| <span data-ttu-id="0456d-456">родительский \(необязательный\)</span><span class="sxs-lookup"><span data-stu-id="0456d-456">parent \(optional\)</span></span> | [<span data-ttu-id="0456d-457">StackTrace</span><span class="sxs-lookup"><span data-stu-id="0456d-457">StackTrace</span></span>](#stacktrace) | <span data-ttu-id="0456d-458">Асинхронный след стека JavaScript, предшествующий этому стеку, если доступен.</span><span class="sxs-lookup"><span data-stu-id="0456d-458">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span> |  

---  
