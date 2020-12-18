---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена времени работы. Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не отпущены явным образом.
title: Домен времени работы — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f18cca951b298e8b4d870a7d722f30c9d28ad346
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235565"
---
# <span data-ttu-id="743a3-106">Домен времени работы — протокол DevTools версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="743a3-106">Runtime Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="743a3-107">Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="743a3-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="743a3-108">Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="743a3-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="743a3-109">Исходные объекты сохраняются в памяти, если они не отпущены явным образом.</span><span class="sxs-lookup"><span data-stu-id="743a3-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="743a3-110">Методы</span><span class="sxs-lookup"><span data-stu-id="743a3-110">Methods</span></span>**](#methods) | <span data-ttu-id="743a3-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span><span class="sxs-lookup"><span data-stu-id="743a3-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [awaitPromise](#awaitpromise), [getProperties](#getproperties), [globalLexicalScopeNames](#globallexicalscopenames), [releaseObject](#releaseobject), [releaseObjectGroup](#releaseobjectgroup), [discardConsoleEntries](#discardconsoleentries)</span></span> |
| [**<span data-ttu-id="743a3-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="743a3-112">Events</span></span>**](#events) | <span data-ttu-id="743a3-113">[executionContextCreated,](#executioncontextcreated) [executionContextDestroyed,](#executioncontextdestroyed) [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span><span class="sxs-lookup"><span data-stu-id="743a3-113">[executionContextCreated](#executioncontextcreated), [executionContextDestroyed](#executioncontextdestroyed), [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown), [consoleAPICalled](#consoleapicalled)</span></span> |
| [**<span data-ttu-id="743a3-114">Типы</span><span class="sxs-lookup"><span data-stu-id="743a3-114">Types</span></span>**](#types) | <span data-ttu-id="743a3-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="743a3-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExecutionContextDescription](#executioncontextdescription), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="743a3-116">Методы</span><span class="sxs-lookup"><span data-stu-id="743a3-116">Methods</span></span>

### <span data-ttu-id="743a3-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="743a3-117">enable</span></span>
<span data-ttu-id="743a3-118">Включает отчеты о <code>executionContextCreated</code> <code>executionContextDestroyed</code> событиях и <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="743a3-118">Enables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span> <span data-ttu-id="743a3-119">Когда отчет включен, событие <code>executionContextCreated</code> немедленно отправляется для каждого существующего контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-119">When the reporting gets enabled the <code>executionContextCreated</code> event will be sent immediately for each existing execution context.</span></span>

</p>

---

### <span data-ttu-id="743a3-120">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="743a3-120">disable</span></span>
<span data-ttu-id="743a3-121">Отключает отчеты о <code>executionContextCreated</code> <code>executionContextDestroyed</code> событиях и <code>executionContextsCleared</code> событиях.</span><span class="sxs-lookup"><span data-stu-id="743a3-121">Disables reporting of the <code>executionContextCreated</code>, <code>executionContextDestroyed</code> and <code>executionContextsCleared</code> events.</span></span>

</p>

---

### <span data-ttu-id="743a3-122">evaluate</span><span class="sxs-lookup"><span data-stu-id="743a3-122">evaluate</span></span>
<span data-ttu-id="743a3-123">Оценивает выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-123">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-124">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-125">выражение</span><span class="sxs-lookup"><span data-stu-id="743a3-125">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-126">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="743a3-126">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-127">includeCommandLineAPI</span><span class="sxs-lookup"><span data-stu-id="743a3-127">includeCommandLineAPI</span></span> <br/> <i><span data-ttu-id="743a3-128">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-128">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-129">Определяет, должен ли API командной строки быть доступным во время оценки.</span><span class="sxs-lookup"><span data-stu-id="743a3-129">Determines whether Command Line API should be available during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-130">objectGroup</span><span class="sxs-lookup"><span data-stu-id="743a3-130">objectGroup</span></span> <br/> <i><span data-ttu-id="743a3-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-131">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-132">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="743a3-132">Symbolic group name that can be used to release multiple objects.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-133">silent</span><span class="sxs-lookup"><span data-stu-id="743a3-133">silent</span></span> <br/> <i><span data-ttu-id="743a3-134">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-134">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-135">В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="743a3-135">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="743a3-136">Переопределяет <code>setPauseOnException</code> состояние.</span><span class="sxs-lookup"><span data-stu-id="743a3-136">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-137">contextId</span><span class="sxs-lookup"><span data-stu-id="743a3-137">contextId</span></span> <br/> <i><span data-ttu-id="743a3-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-138">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-139">Указывает, в какой контексте выполнения выполнять оценку.</span><span class="sxs-lookup"><span data-stu-id="743a3-139">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="743a3-140">Если этот параметр опущен, оценка будет выполнена в контексте проверенной страницы.</span><span class="sxs-lookup"><span data-stu-id="743a3-140">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-141">returnByValue</span><span class="sxs-lookup"><span data-stu-id="743a3-141">returnByValue</span></span> <br/> <i><span data-ttu-id="743a3-142">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-142">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-143">Должен ли результат быть объектом JSON, который должен быть отправлен значением.</span><span class="sxs-lookup"><span data-stu-id="743a3-143">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-144">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="743a3-144">awaitPromise</span></span> <br/> <i><span data-ttu-id="743a3-145">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-145">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-146">Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="743a3-146">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-147">Возвращает</span><span class="sxs-lookup"><span data-stu-id="743a3-147">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-148">result</span><span class="sxs-lookup"><span data-stu-id="743a3-148">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-149">Результат оценки.</span><span class="sxs-lookup"><span data-stu-id="743a3-149">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-150">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="743a3-150">callFunctionOn</span></span>
<span data-ttu-id="743a3-151">Вызывает функцию с заданным объявлением для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-151">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="743a3-152">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-152">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-153">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-153">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-154">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="743a3-154">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-155">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="743a3-155">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-156">objectId</span><span class="sxs-lookup"><span data-stu-id="743a3-156">objectId</span></span> <br/> <i><span data-ttu-id="743a3-157">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-157">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-158">Идентификатор объекта для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="743a3-158">Identifier of the object to call function on.</span></span> <span data-ttu-id="743a3-159">Должен быть указан objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="743a3-159">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="743a3-160">objectId должен быть из функции Runtime.evaluate().</span><span class="sxs-lookup"><span data-stu-id="743a3-160">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-161">arguments</span><span class="sxs-lookup"><span data-stu-id="743a3-161">arguments</span></span> <br/> <i><span data-ttu-id="743a3-162">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-162">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="743a3-163">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="743a3-163">Call arguments.</span></span> <span data-ttu-id="743a3-164">Все аргументы вызова должны принадлежать к одному и тем же мирам JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="743a3-164">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-165">silent</span><span class="sxs-lookup"><span data-stu-id="743a3-165">silent</span></span> <br/> <i><span data-ttu-id="743a3-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-167">В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="743a3-167">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="743a3-168">Переопределяет <code>setPauseOnException</code> состояние.</span><span class="sxs-lookup"><span data-stu-id="743a3-168">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-169">returnByValue</span><span class="sxs-lookup"><span data-stu-id="743a3-169">returnByValue</span></span> <br/> <i><span data-ttu-id="743a3-170">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-170">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-171">Должен ли результат быть объектом JSON, который должен быть отправлен значением.</span><span class="sxs-lookup"><span data-stu-id="743a3-171">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-172">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="743a3-172">awaitPromise</span></span> <br/> <i><span data-ttu-id="743a3-173">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-173">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-174">Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="743a3-174">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-175">executionContextId</span><span class="sxs-lookup"><span data-stu-id="743a3-175">executionContextId</span></span> <br/> <i><span data-ttu-id="743a3-176">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-176">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-177">Указывает контекст выполнения, в котором будет использоваться глобальный объект для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="743a3-177">Specifies execution context which global object will be used to call function on.</span></span> <span data-ttu-id="743a3-178">Должен быть указан объект executionContextId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="743a3-178">Either executionContextId or objectId should be specified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-179">objectGroup</span><span class="sxs-lookup"><span data-stu-id="743a3-179">objectGroup</span></span> <br/> <i><span data-ttu-id="743a3-180">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-180">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-181">Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</span><span class="sxs-lookup"><span data-stu-id="743a3-181">Symbolic group name that can be used to release multiple objects.</span></span> <span data-ttu-id="743a3-182">Если objectGroup не указан, а objectId указан, objectGroup наследуется от объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-182">If objectGroup is not specified and objectId is, objectGroup will be inherited from object.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-183">Возвращает</span><span class="sxs-lookup"><span data-stu-id="743a3-183">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-184">result</span><span class="sxs-lookup"><span data-stu-id="743a3-184">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-185">Результат вызова.</span><span class="sxs-lookup"><span data-stu-id="743a3-185">Call result.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-186">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="743a3-186">awaitPromise</span></span>
<span data-ttu-id="743a3-187">Добавьте обработок, чтобы обещать с заданным ид объекта promise.</span><span class="sxs-lookup"><span data-stu-id="743a3-187">Add handler to promise with given promise object id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-188">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-189">promiseObjectId</span><span class="sxs-lookup"><span data-stu-id="743a3-189">promiseObjectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-190">Идентификатор обещания.</span><span class="sxs-lookup"><span data-stu-id="743a3-190">Identifier of the promise.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-191">returnByValue</span><span class="sxs-lookup"><span data-stu-id="743a3-191">returnByValue</span></span> <br/> <i><span data-ttu-id="743a3-192">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-192">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-193">Должен ли результат быть объектом JSON, который должен быть отправлен значением.</span><span class="sxs-lookup"><span data-stu-id="743a3-193">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-194">Возвращает</span><span class="sxs-lookup"><span data-stu-id="743a3-194">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-195">result</span><span class="sxs-lookup"><span data-stu-id="743a3-195">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-196">Результат обещания.</span><span class="sxs-lookup"><span data-stu-id="743a3-196">Promise result.</span></span>  <span data-ttu-id="743a3-197">Будет содержать отклоненные значения, если обещание было отклонено.</span><span class="sxs-lookup"><span data-stu-id="743a3-197">Will contain rejected value if promise was rejected.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-198">getProperties</span><span class="sxs-lookup"><span data-stu-id="743a3-198">getProperties</span></span>
<span data-ttu-id="743a3-199">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-199">Returns properties of a given object.</span></span> <span data-ttu-id="743a3-200">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-200">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-201">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-202">objectId</span><span class="sxs-lookup"><span data-stu-id="743a3-202">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-203">Идентификатор объекта, для котором возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="743a3-203">Identifier of the object to return properties for.</span></span> <span data-ttu-id="743a3-204">objectId должен быть от функции Debugger.evaluateOnCallFrame().</span><span class="sxs-lookup"><span data-stu-id="743a3-204">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-205">ownProperties</span><span class="sxs-lookup"><span data-stu-id="743a3-205">ownProperties</span></span> <br/> <i><span data-ttu-id="743a3-206">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-206">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-207">Если имеется true, возвращает свойства, принадлежащие только самому элементу, а не его прототипу цепочки.</span><span class="sxs-lookup"><span data-stu-id="743a3-207">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-208">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="743a3-208">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="743a3-209">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-209">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="743a3-210">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="743a3-210">Experimental.</span></span> </b></span><span data-ttu-id="743a3-211">Если установлено true, возвращает только свойства доступа (с getter/setter); внутренние свойства также не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="743a3-211">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-212">Возвращает</span><span class="sxs-lookup"><span data-stu-id="743a3-212">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-213">result</span><span class="sxs-lookup"><span data-stu-id="743a3-213">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="743a3-214">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-214">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-215">globalLexicalScopeNames</span><span class="sxs-lookup"><span data-stu-id="743a3-215">globalLexicalScopeNames</span></span>
<span data-ttu-id="743a3-216">Возвращает все переменные let, const и class из глобальной области консоли.</span><span class="sxs-lookup"><span data-stu-id="743a3-216">Returns all let, const, and class variables from the console global scope.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-217">Возвращает</span><span class="sxs-lookup"><span data-stu-id="743a3-217">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-218">names</span><span class="sxs-lookup"><span data-stu-id="743a3-218">names</span></span></td>
            <td><code class="flyout">string[]</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-219">releaseObject</span><span class="sxs-lookup"><span data-stu-id="743a3-219">releaseObject</span></span>
<span data-ttu-id="743a3-220">Освобождает удаленный объект с заданным идом.</span><span class="sxs-lookup"><span data-stu-id="743a3-220">Releases remote object with given id.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-221">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-221">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-222">objectId</span><span class="sxs-lookup"><span data-stu-id="743a3-222">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-223">Идентификатор объекта, который необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="743a3-223">Identifier of the object to release.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-224">releaseObjectGroup</span><span class="sxs-lookup"><span data-stu-id="743a3-224">releaseObjectGroup</span></span>
<span data-ttu-id="743a3-225">Освобождает все удаленные объекты, принадлежащие данной группе.</span><span class="sxs-lookup"><span data-stu-id="743a3-225">Releases all remote objects that belong to a given group.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-226">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-226">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-227">objectGroup</span><span class="sxs-lookup"><span data-stu-id="743a3-227">objectGroup</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-228">Символьное имя группы объектов.</span><span class="sxs-lookup"><span data-stu-id="743a3-228">Symbolic object group name.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-229">discardConsoleEntries</span><span class="sxs-lookup"><span data-stu-id="743a3-229">discardConsoleEntries</span></span>
<span data-ttu-id="743a3-230">Удаляет собранные исключения и вызовы консольного API.</span><span class="sxs-lookup"><span data-stu-id="743a3-230">Discards collected exceptions and console API calls.</span></span>

</p>

---

## <span data-ttu-id="743a3-231">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="743a3-231">Events</span></span>

### <span data-ttu-id="743a3-232">executionContextCreated</span><span class="sxs-lookup"><span data-stu-id="743a3-232">executionContextCreated</span></span>
<span data-ttu-id="743a3-233">Выдается при новом контексте выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-233">Issued when new execution context is created.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-234">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-234">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-235">context</span><span class="sxs-lookup"><span data-stu-id="743a3-235">context</span></span></td>
            <td><a href="#executioncontextdescription"><code class="flyout">ExecutionContextDescription</code></a></td>
            <td><span data-ttu-id="743a3-236">Только что созданный контекст выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-236">A newly created execution context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-237">executionContextDestroyed</span><span class="sxs-lookup"><span data-stu-id="743a3-237">executionContextDestroyed</span></span>
<span data-ttu-id="743a3-238">Выдается при уничтожении контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-238">Issued when execution context is destroyed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-239">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-240">executionContextId</span><span class="sxs-lookup"><span data-stu-id="743a3-240">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-241">ИД контекста уничтожения</span><span class="sxs-lookup"><span data-stu-id="743a3-241">Id of the destroyed context</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-242">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="743a3-242">executionContextsCleared</span></span>
<span data-ttu-id="743a3-243">Выдан, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="743a3-243">Issued when all executionContexts were cleared in browser</span></span>

</p>

---

### <span data-ttu-id="743a3-244">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="743a3-244">exceptionThrown</span></span>
<span data-ttu-id="743a3-245">Выдается, когда исключение было выброшено и необбрано.</span><span class="sxs-lookup"><span data-stu-id="743a3-245">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-246">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-246">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-247">timestamp</span><span class="sxs-lookup"><span data-stu-id="743a3-247">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="743a3-248">Timestamp исключения.</span><span class="sxs-lookup"><span data-stu-id="743a3-248">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-249">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="743a3-249">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="743a3-250">consoleAPICalled</span><span class="sxs-lookup"><span data-stu-id="743a3-250">consoleAPICalled</span></span>


<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-251">Параметры</span><span class="sxs-lookup"><span data-stu-id="743a3-251">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-252">Тип</span><span class="sxs-lookup"><span data-stu-id="743a3-252">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="743a3-253">Допустимые значения: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span><span class="sxs-lookup"><span data-stu-id="743a3-253">Allowed values: log, info, warning, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, timeStamp, startGroup, startGroupCollapsed, endGroup</span></span></i></td>
            <td><span data-ttu-id="743a3-254">Тип вызова.</span><span class="sxs-lookup"><span data-stu-id="743a3-254">Type of the call.</span></span> <span data-ttu-id="743a3-255">К ним относятся журнал, сведения, предупреждение, ошибка, отлаженная, assert, таблица, трассировка, dir, dirxml, clear, select, count, countReset, timeEnd, исключение, timeStamp, группа, groupCollapsed, groupEnd.</span><span class="sxs-lookup"><span data-stu-id="743a3-255">This includes log, info, warn, error, debug, assert, table, trace, dir, dirxml, clear, select, count, countReset, timeEnd, exception, timeStamp, group, groupCollapsed, groupEnd.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-256">args</span><span class="sxs-lookup"><span data-stu-id="743a3-256">args</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject[]</code></a></td>
            <td><span data-ttu-id="743a3-257">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="743a3-257">Call arguments.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-258">executionContextId</span><span class="sxs-lookup"><span data-stu-id="743a3-258">executionContextId</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-259">Идентификатор контекста, в котором был выполнен вызов консоли</span><span class="sxs-lookup"><span data-stu-id="743a3-259">Identifier of the context where console call was made</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-260">timestamp</span><span class="sxs-lookup"><span data-stu-id="743a3-260">timestamp</span></span> <br/> <i><span data-ttu-id="743a3-261">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-261">optional</span></span></i></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="743a3-262">Временная пометь вызова.</span><span class="sxs-lookup"><span data-stu-id="743a3-262">Call timestamp.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-263">stackTrace</span><span class="sxs-lookup"><span data-stu-id="743a3-263">stackTrace</span></span> <br/> <i><span data-ttu-id="743a3-264">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-264">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="743a3-265">Трассировка стека, если она доступна</span><span class="sxs-lookup"><span data-stu-id="743a3-265">Stack trace captured if available</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="743a3-266">Типы</span><span class="sxs-lookup"><span data-stu-id="743a3-266">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="743a3-267">ScriptId</span><span class="sxs-lookup"><span data-stu-id="743a3-267">ScriptId</span></span> `string`

<span data-ttu-id="743a3-268">Уникальный идентификатор скрипта.</span><span class="sxs-lookup"><span data-stu-id="743a3-268">Unique script identifier.</span></span>

</p>

---

### <a name="remoteobjectid"></a> <span data-ttu-id="743a3-269">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="743a3-269">RemoteObjectId</span></span> `string`

<span data-ttu-id="743a3-270">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-270">Unique object identifier.</span></span>

</p>

---

### <a name="unserializablevalue"></a> <span data-ttu-id="743a3-271">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="743a3-271">UnserializableValue</span></span> `string`

<span data-ttu-id="743a3-272">Значение примитива, которое не может быть в строке JSON.</span><span class="sxs-lookup"><span data-stu-id="743a3-272">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="743a3-273">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="743a3-273">Allowed Values</span></span>
<span data-ttu-id="743a3-274">Бесконечность, неn, -Infinity, -0</span><span class="sxs-lookup"><span data-stu-id="743a3-274">Infinity, NaN, -Infinity, -0</span></span>
</p>

---

### <a name="remoteobject"></a> <span data-ttu-id="743a3-275">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="743a3-275">RemoteObject</span></span> `object`

<span data-ttu-id="743a3-276">Зеркальный объект, ссылающийся на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743a3-276">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-277">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-277">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-278">Тип</span><span class="sxs-lookup"><span data-stu-id="743a3-278">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="743a3-279">Допустимые значения: object, function, undefined, string, number, boolean, symbol</span><span class="sxs-lookup"><span data-stu-id="743a3-279">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="743a3-280">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-280">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-281">subtype</span><span class="sxs-lookup"><span data-stu-id="743a3-281">subtype</span></span> <br/> <i><span data-ttu-id="743a3-282">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-282">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="743a3-283">Допустимые значения: null, error, promise, node</span><span class="sxs-lookup"><span data-stu-id="743a3-283">Allowed values: null, error, promise, node</span></span></i></td>
            <td><span data-ttu-id="743a3-284">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-284">Object subtype hint.</span></span> <span data-ttu-id="743a3-285">Указывается только <code>object</code> для значений типов.</span><span class="sxs-lookup"><span data-stu-id="743a3-285">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-286">className</span><span class="sxs-lookup"><span data-stu-id="743a3-286">className</span></span> <br/> <i><span data-ttu-id="743a3-287">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-287">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-288">Имя класса объекта (конструктора).</span><span class="sxs-lookup"><span data-stu-id="743a3-288">Object class (constructor) name.</span></span> <span data-ttu-id="743a3-289">Указывается только <code>object</code> для значений типов.</span><span class="sxs-lookup"><span data-stu-id="743a3-289">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-290">value</span><span class="sxs-lookup"><span data-stu-id="743a3-290">value</span></span> <br/> <i><span data-ttu-id="743a3-291">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-291">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="743a3-292">Значение удаленного объекта в случае значений примитивов или значений JSON (если он был запротид).</span><span class="sxs-lookup"><span data-stu-id="743a3-292">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-293">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="743a3-293">unserializableValue</span></span> <br/> <i><span data-ttu-id="743a3-294">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-294">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="743a3-295">Значение примитива, которое не может быть в строке JSON, не имеет</span><span class="sxs-lookup"><span data-stu-id="743a3-295">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="743a3-296">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="743a3-296">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-297">description</span><span class="sxs-lookup"><span data-stu-id="743a3-297">description</span></span> <br/> <i><span data-ttu-id="743a3-298">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-298">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-299">Строка представления объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-299">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-300">objectId</span><span class="sxs-lookup"><span data-stu-id="743a3-300">objectId</span></span> <br/> <i><span data-ttu-id="743a3-301">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-301">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-302">Уникальный идентификатор объекта (для не примитивных значений).</span><span class="sxs-lookup"><span data-stu-id="743a3-302">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-303">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="743a3-303">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="743a3-304">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-304">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="743a3-305">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="743a3-305">Experimental.</span></span> </b></span><span data-ttu-id="743a3-306">Майкрософт: связанный ид свойства отладки для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-306">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="743a3-307">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="743a3-307">PropertyDescriptor</span></span> `object`

<span data-ttu-id="743a3-308">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-308">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-309">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-309">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-310">name</span><span class="sxs-lookup"><span data-stu-id="743a3-310">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-311">Имя свойства или описание символа.</span><span class="sxs-lookup"><span data-stu-id="743a3-311">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-312">value</span><span class="sxs-lookup"><span data-stu-id="743a3-312">value</span></span> <br/> <i><span data-ttu-id="743a3-313">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-313">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-314">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="743a3-314">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-315">writable</span><span class="sxs-lookup"><span data-stu-id="743a3-315">writable</span></span> <br/> <i><span data-ttu-id="743a3-316">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-316">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-317">Имеет значение True, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="743a3-317">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-318">получить</span><span class="sxs-lookup"><span data-stu-id="743a3-318">get</span></span> <br/> <i><span data-ttu-id="743a3-319">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-319">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-320">Функция, которая служит в качестве дескриптора для свойства, или если нет <code>undefined</code> getter (только дескрипторы доступа).</span><span class="sxs-lookup"><span data-stu-id="743a3-320">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-321">set</span><span class="sxs-lookup"><span data-stu-id="743a3-321">set</span></span> <br/> <i><span data-ttu-id="743a3-322">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-322">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-323">Функция, которая служит в качестве задавщика для свойства или если нет задавщика <code>undefined</code> (только дескрипторы доступа).</span><span class="sxs-lookup"><span data-stu-id="743a3-323">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-324">настраиваемая</span><span class="sxs-lookup"><span data-stu-id="743a3-324">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-325">True, если тип этого дескриптора свойства может быть изменен и свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-325">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-326">enumerable</span><span class="sxs-lookup"><span data-stu-id="743a3-326">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-327">True, если это свойство появляется во время нумерации свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-327">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-328">wasThrown</span><span class="sxs-lookup"><span data-stu-id="743a3-328">wasThrown</span></span> <br/> <i><span data-ttu-id="743a3-329">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-329">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-330">True, если результат был выброшен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="743a3-330">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-331">isOwn</span><span class="sxs-lookup"><span data-stu-id="743a3-331">isOwn</span></span> <br/> <i><span data-ttu-id="743a3-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-332">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="743a3-333">Имеет свойство True, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="743a3-333">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-334">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="743a3-334">msReturnValue</span></span> <br/> <i><span data-ttu-id="743a3-335">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-335">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="743a3-336">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="743a3-336">Experimental.</span></span> </b></span><span data-ttu-id="743a3-337">Майкрософт: имеет значение True, если свойство является возвращаемой.</span><span class="sxs-lookup"><span data-stu-id="743a3-337">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-338">symbol,</span><span class="sxs-lookup"><span data-stu-id="743a3-338">symbol</span></span> <br/> <i><span data-ttu-id="743a3-339">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-339">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-340">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="743a3-340">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callargument"></a> <span data-ttu-id="743a3-341">CallArgument</span><span class="sxs-lookup"><span data-stu-id="743a3-341">CallArgument</span></span> `object`

<span data-ttu-id="743a3-342">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="743a3-342">Represents function call argument.</span></span> <span data-ttu-id="743a3-343">Должен быть указан либо ид удаленного <code>objectId</code> объекта, примитив, несериализируемый значение примитива, либо ни один <code>value</code> из них (для неопределенных).</span><span class="sxs-lookup"><span data-stu-id="743a3-343">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-344">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-344">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-345">value</span><span class="sxs-lookup"><span data-stu-id="743a3-345">value</span></span> <br/> <i><span data-ttu-id="743a3-346">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-346">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="743a3-347">Значение примитива или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743a3-347">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-348">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="743a3-348">unserializableValue</span></span> <br/> <i><span data-ttu-id="743a3-349">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-349">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="743a3-350">Значение примитива, которое не может быть в строке JSON.</span><span class="sxs-lookup"><span data-stu-id="743a3-350">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-351">objectId</span><span class="sxs-lookup"><span data-stu-id="743a3-351">objectId</span></span> <br/> <i><span data-ttu-id="743a3-352">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-352">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="743a3-353">Удаленный handle объекта.</span><span class="sxs-lookup"><span data-stu-id="743a3-353">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="executioncontextid"></a> <span data-ttu-id="743a3-354">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="743a3-354">ExecutionContextId</span></span> `integer`

<span data-ttu-id="743a3-355">ИД контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-355">Id of an execution context.</span></span>

</p>

---

### <a name="executioncontextdescription"></a> <span data-ttu-id="743a3-356">ExecutionContextDescription</span><span class="sxs-lookup"><span data-stu-id="743a3-356">ExecutionContextDescription</span></span> `object`

<span data-ttu-id="743a3-357">Описание изолированного мира.</span><span class="sxs-lookup"><span data-stu-id="743a3-357">Description of an isolated world.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-358">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-358">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-359">id</span><span class="sxs-lookup"><span data-stu-id="743a3-359">id</span></span></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-360">Уникальный ид контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-360">Unique id of the execution context.</span></span> <span data-ttu-id="743a3-361">Его можно использовать для указания того, в какой оценке сценария контекста выполнения следует выполнить.</span><span class="sxs-lookup"><span data-stu-id="743a3-361">It can be used to specify in which execution context script evaluation should be performed.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-362">origin</span><span class="sxs-lookup"><span data-stu-id="743a3-362">origin</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-363">Источник контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="743a3-363">Execution context origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-364">name</span><span class="sxs-lookup"><span data-stu-id="743a3-364">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-365">Понятное имя, описывающие заданный контекст.</span><span class="sxs-lookup"><span data-stu-id="743a3-365">Human readable name describing given context.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="exceptiondetails"></a> <span data-ttu-id="743a3-366">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="743a3-366">ExceptionDetails</span></span> `object`

<span data-ttu-id="743a3-367">Подробные сведения об исключении (или ошибке), которое было выброшено во время компиляции или выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="743a3-367">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-368">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-369">exceptionId</span><span class="sxs-lookup"><span data-stu-id="743a3-369">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="743a3-370">ИД исключения.</span><span class="sxs-lookup"><span data-stu-id="743a3-370">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-371">текст</span><span class="sxs-lookup"><span data-stu-id="743a3-371">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-372">Текст исключения, который должен использоваться вместе с объектом исключения при наличии.</span><span class="sxs-lookup"><span data-stu-id="743a3-372">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-373">lineNumber</span><span class="sxs-lookup"><span data-stu-id="743a3-373">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="743a3-374">Номер строки расположения исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="743a3-374">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-375">columnNumber</span><span class="sxs-lookup"><span data-stu-id="743a3-375">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="743a3-376">Номер столбца расположения исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="743a3-376">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-377">scriptId</span><span class="sxs-lookup"><span data-stu-id="743a3-377">scriptId</span></span> <br/> <i><span data-ttu-id="743a3-378">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-378">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="743a3-379">ИД сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="743a3-379">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-380">url</span><span class="sxs-lookup"><span data-stu-id="743a3-380">url</span></span> <br/> <i><span data-ttu-id="743a3-381">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-381">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-382">URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан.</span><span class="sxs-lookup"><span data-stu-id="743a3-382">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-383">stackTrace</span><span class="sxs-lookup"><span data-stu-id="743a3-383">stackTrace</span></span> <br/> <i><span data-ttu-id="743a3-384">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-384">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="743a3-385">Трассировка стека JavaScript, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="743a3-385">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-386">exception</span><span class="sxs-lookup"><span data-stu-id="743a3-386">exception</span></span> <br/> <i><span data-ttu-id="743a3-387">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-387">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="743a3-388">Объект исключения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="743a3-388">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-389">executionContextId</span><span class="sxs-lookup"><span data-stu-id="743a3-389">executionContextId</span></span> <br/> <i><span data-ttu-id="743a3-390">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-390">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="743a3-391">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="743a3-391">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="timestamp"></a> <span data-ttu-id="743a3-392">Метка времени</span><span class="sxs-lookup"><span data-stu-id="743a3-392">Timestamp</span></span> `integer`

<span data-ttu-id="743a3-393">Количество миллисекунд с момента эпохи.</span><span class="sxs-lookup"><span data-stu-id="743a3-393">Number of milliseconds since epoch.</span></span>

</p>

---

### <a name="callframe"></a> <span data-ttu-id="743a3-394">CallFrame</span><span class="sxs-lookup"><span data-stu-id="743a3-394">CallFrame</span></span> `object`

<span data-ttu-id="743a3-395">Запись стека для ошибок и утверждений во время работы.</span><span class="sxs-lookup"><span data-stu-id="743a3-395">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-396">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-396">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-397">functionName</span><span class="sxs-lookup"><span data-stu-id="743a3-397">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-398">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743a3-398">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-399">scriptId</span><span class="sxs-lookup"><span data-stu-id="743a3-399">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="743a3-400">ИД скрипта JavaScript. Если отладка не включена, ScriptId будет пустым.</span><span class="sxs-lookup"><span data-stu-id="743a3-400">JavaScript script id. ScriptId will be empty if debugger is not enabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-401">url</span><span class="sxs-lookup"><span data-stu-id="743a3-401">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-402">Имя или URL-адрес сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743a3-402">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-403">lineNumber</span><span class="sxs-lookup"><span data-stu-id="743a3-403">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="743a3-404">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="743a3-404">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-405">columnNumber</span><span class="sxs-lookup"><span data-stu-id="743a3-405">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="743a3-406">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="743a3-406">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="stacktrace"></a> <span data-ttu-id="743a3-407">StackTrace</span><span class="sxs-lookup"><span data-stu-id="743a3-407">StackTrace</span></span> `object`

<span data-ttu-id="743a3-408">Вызов кадров для утверждений или сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="743a3-408">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="743a3-409">Свойства</span><span class="sxs-lookup"><span data-stu-id="743a3-409">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="743a3-410">description</span><span class="sxs-lookup"><span data-stu-id="743a3-410">description</span></span> <br/> <i><span data-ttu-id="743a3-411">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-411">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="743a3-412">Строковая метка трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="743a3-412">String label of this stack trace.</span></span> <span data-ttu-id="743a3-413">Для а async traces это может быть имя функции, которая инициировала ассынский вызов.</span><span class="sxs-lookup"><span data-stu-id="743a3-413">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-414">callFrames</span><span class="sxs-lookup"><span data-stu-id="743a3-414">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="743a3-415">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="743a3-415">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="743a3-416">parent</span><span class="sxs-lookup"><span data-stu-id="743a3-416">parent</span></span> <br/> <i><span data-ttu-id="743a3-417">необязательные</span><span class="sxs-lookup"><span data-stu-id="743a3-417">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="743a3-418">Асинхронная трассировка стека JavaScript, предшествующего этому стеку, если доступна.</span><span class="sxs-lookup"><span data-stu-id="743a3-418">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
