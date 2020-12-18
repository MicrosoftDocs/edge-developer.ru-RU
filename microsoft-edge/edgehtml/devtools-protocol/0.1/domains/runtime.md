---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена времени работы. Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не отпущены явным образом.
title: Домен времени работы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 942a105199c8740fb7f7496b2a68e3eb0cc46fb4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235202"
---
# <span data-ttu-id="6039f-106">Домен времени работы — протокол DevTools версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="6039f-106">Runtime Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="6039f-107">Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="6039f-107">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="6039f-108">Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="6039f-108">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="6039f-109">Исходные объекты сохраняются в памяти, если они не отпущены явным образом.</span><span class="sxs-lookup"><span data-stu-id="6039f-109">Original objects are maintained in memory unless they are either explicitly released.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="6039f-110">Методы</span><span class="sxs-lookup"><span data-stu-id="6039f-110">Methods</span></span>**](#methods) | <span data-ttu-id="6039f-111">[enable,](#enable) [disable,](#disable) [evaluate,](#evaluate) [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span><span class="sxs-lookup"><span data-stu-id="6039f-111">[enable](#enable), [disable](#disable), [evaluate](#evaluate), [callFunctionOn](#callfunctionon), [getProperties](#getproperties)</span></span> |
| [**<span data-ttu-id="6039f-112">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="6039f-112">Events</span></span>**](#events) | <span data-ttu-id="6039f-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span><span class="sxs-lookup"><span data-stu-id="6039f-113">[executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown)</span></span> |
| [**<span data-ttu-id="6039f-114">Типы</span><span class="sxs-lookup"><span data-stu-id="6039f-114">Types</span></span>**](#types) | <span data-ttu-id="6039f-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span><span class="sxs-lookup"><span data-stu-id="6039f-115">[ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace)</span></span> |
## <span data-ttu-id="6039f-116">Методы</span><span class="sxs-lookup"><span data-stu-id="6039f-116">Methods</span></span>

### <span data-ttu-id="6039f-117">"Включить"</span><span class="sxs-lookup"><span data-stu-id="6039f-117">enable</span></span>
<span data-ttu-id="6039f-118">Включает отчеты о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="6039f-118">Enables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="6039f-119">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="6039f-119">disable</span></span>
<span data-ttu-id="6039f-120">Отключает отчет о <code>executionContextsCleared</code> событии.</span><span class="sxs-lookup"><span data-stu-id="6039f-120">Disables reporting of the <code>executionContextsCleared</code> event.</span></span>


---

### <span data-ttu-id="6039f-121">evaluate</span><span class="sxs-lookup"><span data-stu-id="6039f-121">evaluate</span></span>
<span data-ttu-id="6039f-122">Оценивает выражение для глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-122">Evaluates expression on global object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-123">Параметры</span><span class="sxs-lookup"><span data-stu-id="6039f-123">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-124">выражение</span><span class="sxs-lookup"><span data-stu-id="6039f-124">expression</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-125">Выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="6039f-125">Expression to evaluate.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-126">silent</span><span class="sxs-lookup"><span data-stu-id="6039f-126">silent</span></span> <br/> <i><span data-ttu-id="6039f-127">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-127">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-128">В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="6039f-128">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="6039f-129">Переопределяет <code>setPauseOnException</code> состояние.</span><span class="sxs-lookup"><span data-stu-id="6039f-129">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-130">contextId</span><span class="sxs-lookup"><span data-stu-id="6039f-130">contextId</span></span> <br/> <i><span data-ttu-id="6039f-131">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-131">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="6039f-132">Указывает, в какой контексте выполнения выполнять оценку.</span><span class="sxs-lookup"><span data-stu-id="6039f-132">Specifies in which execution context to perform evaluation.</span></span> <span data-ttu-id="6039f-133">Если этот параметр опущен, оценка будет выполнена в контексте проверенной страницы.</span><span class="sxs-lookup"><span data-stu-id="6039f-133">If the parameter is omitted the evaluation will be performed in the context of the inspected page.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-134">returnByValue</span><span class="sxs-lookup"><span data-stu-id="6039f-134">returnByValue</span></span> <br/> <i><span data-ttu-id="6039f-135">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-135">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-136">Должен ли результат быть объектом JSON, который должен быть отправлен значением.</span><span class="sxs-lookup"><span data-stu-id="6039f-136">Whether the result is expected to be a JSON object that should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-137">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="6039f-137">awaitPromise</span></span> <br/> <i><span data-ttu-id="6039f-138">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-138">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-139">Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="6039f-139">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-140">Возвращает</span><span class="sxs-lookup"><span data-stu-id="6039f-140">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-141">result</span><span class="sxs-lookup"><span data-stu-id="6039f-141">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-142">Результат оценки.</span><span class="sxs-lookup"><span data-stu-id="6039f-142">Evaluation result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6039f-143">callFunctionOn</span><span class="sxs-lookup"><span data-stu-id="6039f-143">callFunctionOn</span></span>
<span data-ttu-id="6039f-144">Вызывает функцию с заданным объявлением для данного объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-144">Calls function with given declaration on the given object.</span></span> <span data-ttu-id="6039f-145">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-145">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-146">Параметры</span><span class="sxs-lookup"><span data-stu-id="6039f-146">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-147">functionDeclaration</span><span class="sxs-lookup"><span data-stu-id="6039f-147">functionDeclaration</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-148">Объявление вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="6039f-148">Declaration of the function to call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-149">objectId</span><span class="sxs-lookup"><span data-stu-id="6039f-149">objectId</span></span> <br/> <i><span data-ttu-id="6039f-150">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-150">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="6039f-151">Идентификатор объекта для вызова функции.</span><span class="sxs-lookup"><span data-stu-id="6039f-151">Identifier of the object to call function on.</span></span> <span data-ttu-id="6039f-152">Должен быть указан objectId или executionContextId.</span><span class="sxs-lookup"><span data-stu-id="6039f-152">Either objectId or executionContextId should be specified.</span></span>  <span data-ttu-id="6039f-153">objectId должен быть из функции Runtime.evaluate().</span><span class="sxs-lookup"><span data-stu-id="6039f-153">objectId must be from the Runtime.evaluate() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-154">arguments</span><span class="sxs-lookup"><span data-stu-id="6039f-154">arguments</span></span> <br/> <i><span data-ttu-id="6039f-155">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-155">optional</span></span></i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td><span data-ttu-id="6039f-156">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="6039f-156">Call arguments.</span></span> <span data-ttu-id="6039f-157">Все аргументы вызова должны принадлежать к одному и тем же мирам JavaScript, что и целевой объект.</span><span class="sxs-lookup"><span data-stu-id="6039f-157">All call arguments must belong to the same JavaScript world as the target object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-158">silent</span><span class="sxs-lookup"><span data-stu-id="6039f-158">silent</span></span> <br/> <i><span data-ttu-id="6039f-159">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-159">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-160">В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.</span><span class="sxs-lookup"><span data-stu-id="6039f-160">In silent mode exceptions thrown during evaluation are not reported and do not pause execution.</span></span> <span data-ttu-id="6039f-161">Переопределяет <code>setPauseOnException</code> состояние.</span><span class="sxs-lookup"><span data-stu-id="6039f-161">Overrides <code>setPauseOnException</code> state.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-162">returnByValue</span><span class="sxs-lookup"><span data-stu-id="6039f-162">returnByValue</span></span> <br/> <i><span data-ttu-id="6039f-163">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-163">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-164">Должен ли результат быть объектом JSON, который должен быть отправлен значением.</span><span class="sxs-lookup"><span data-stu-id="6039f-164">Whether the result is expected to be a JSON object which should be sent by value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-165">awaitPromise</span><span class="sxs-lookup"><span data-stu-id="6039f-165">awaitPromise</span></span> <br/> <i><span data-ttu-id="6039f-166">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-166">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-167">Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</span><span class="sxs-lookup"><span data-stu-id="6039f-167">Whether execution should <code>await</code> for resulting value and return once awaited promise is resolved.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-168">Возвращает</span><span class="sxs-lookup"><span data-stu-id="6039f-168">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-169">result</span><span class="sxs-lookup"><span data-stu-id="6039f-169">result</span></span></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-170">Результат вызова.</span><span class="sxs-lookup"><span data-stu-id="6039f-170">Call result.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <span data-ttu-id="6039f-171">getProperties</span><span class="sxs-lookup"><span data-stu-id="6039f-171">getProperties</span></span>
<span data-ttu-id="6039f-172">Возвращает свойства заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-172">Returns properties of a given object.</span></span> <span data-ttu-id="6039f-173">Группа объектов результата наследуется от целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-173">Object group of the result is inherited from the target object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-174">Параметры</span><span class="sxs-lookup"><span data-stu-id="6039f-174">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-175">objectId</span><span class="sxs-lookup"><span data-stu-id="6039f-175">objectId</span></span></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="6039f-176">Идентификатор объекта, для котором возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="6039f-176">Identifier of the object to return properties for.</span></span>  <span data-ttu-id="6039f-177">objectId должен быть от функции Debugger.evaluateOnCallFrame().</span><span class="sxs-lookup"><span data-stu-id="6039f-177">objectId must be from the Debugger.evaluateOnCallFrame() function.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-178">ownProperties</span><span class="sxs-lookup"><span data-stu-id="6039f-178">ownProperties</span></span> <br/> <i><span data-ttu-id="6039f-179">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-179">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-180">Если имеется true, возвращает свойства, принадлежащие только самому элементу, а не его прототипу цепочки.</span><span class="sxs-lookup"><span data-stu-id="6039f-180">If true, returns properties belonging only to the element itself, not to its prototype chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-181">accessorPropertiesOnly</span><span class="sxs-lookup"><span data-stu-id="6039f-181">accessorPropertiesOnly</span></span> <br/> <i><span data-ttu-id="6039f-182">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-182">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="6039f-183">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="6039f-183">Experimental.</span></span> </b></span><span data-ttu-id="6039f-184">Если установлено true, возвращает только свойства доступа (с getter/setter); внутренние свойства также не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="6039f-184">If true, returns accessor properties (with getter/setter) only; internal properties are not returned either.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-185">Возвращает</span><span class="sxs-lookup"><span data-stu-id="6039f-185">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-186">result</span><span class="sxs-lookup"><span data-stu-id="6039f-186">result</span></span></td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td><span data-ttu-id="6039f-187">Свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-187">Object properties.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="6039f-188">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="6039f-188">Events</span></span>

### <span data-ttu-id="6039f-189">executionContextsCleared</span><span class="sxs-lookup"><span data-stu-id="6039f-189">executionContextsCleared</span></span>
<span data-ttu-id="6039f-190">Выдан, когда все executionContexts были очищены в браузере</span><span class="sxs-lookup"><span data-stu-id="6039f-190">Issued when all executionContexts were cleared in browser</span></span>


---

### <span data-ttu-id="6039f-191">exceptionThrown</span><span class="sxs-lookup"><span data-stu-id="6039f-191">exceptionThrown</span></span>
<span data-ttu-id="6039f-192">Выдается, когда исключение было выброшено и необбрано.</span><span class="sxs-lookup"><span data-stu-id="6039f-192">Issued when exception was thrown and unhandled.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-193">Параметры</span><span class="sxs-lookup"><span data-stu-id="6039f-193">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-194">timestamp</span><span class="sxs-lookup"><span data-stu-id="6039f-194">timestamp</span></span></td>
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td><span data-ttu-id="6039f-195">Timestamp исключения.</span><span class="sxs-lookup"><span data-stu-id="6039f-195">Timestamp of the exception.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-196">exceptionDetails</span><span class="sxs-lookup"><span data-stu-id="6039f-196">exceptionDetails</span></span></td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="6039f-197">Типы</span><span class="sxs-lookup"><span data-stu-id="6039f-197">Types</span></span>

### <a name="scriptid"></a> <span data-ttu-id="6039f-198">ScriptId</span><span class="sxs-lookup"><span data-stu-id="6039f-198">ScriptId</span></span> `string`

<span data-ttu-id="6039f-199">Уникальный идентификатор скрипта.</span><span class="sxs-lookup"><span data-stu-id="6039f-199">Unique script identifier.</span></span>


---

### <a name="remoteobjectid"></a> <span data-ttu-id="6039f-200">RemoteObjectId</span><span class="sxs-lookup"><span data-stu-id="6039f-200">RemoteObjectId</span></span> `string`

<span data-ttu-id="6039f-201">Уникальный идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-201">Unique object identifier.</span></span>


---

### <a name="unserializablevalue"></a> <span data-ttu-id="6039f-202">UnserializableValue</span><span class="sxs-lookup"><span data-stu-id="6039f-202">UnserializableValue</span></span> `string`

<span data-ttu-id="6039f-203">Значение примитива, которое не может быть в строке JSON.</span><span class="sxs-lookup"><span data-stu-id="6039f-203">Primitive value which cannot be JSON-stringified.</span></span>

##### <span data-ttu-id="6039f-204">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="6039f-204">Allowed Values</span></span>
<span data-ttu-id="6039f-205">Бесконечность, неn, -Infinity, -0</span><span class="sxs-lookup"><span data-stu-id="6039f-205">Infinity, NaN, -Infinity, -0</span></span>

---

### <a name="remoteobject"></a> <span data-ttu-id="6039f-206">RemoteObject</span><span class="sxs-lookup"><span data-stu-id="6039f-206">RemoteObject</span></span> `object`

<span data-ttu-id="6039f-207">Зеркальный объект, ссылающийся на исходный объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-207">Mirror object referencing original JavaScript object.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-208">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-208">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-209">Тип</span><span class="sxs-lookup"><span data-stu-id="6039f-209">type</span></span></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="6039f-210">Допустимые значения: object, function, undefined, string, number, boolean, symbol</span><span class="sxs-lookup"><span data-stu-id="6039f-210">Allowed values: object, function, undefined, string, number, boolean, symbol</span></span></i></td>
            <td><span data-ttu-id="6039f-211">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-211">Object type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-212">subtype</span><span class="sxs-lookup"><span data-stu-id="6039f-212">subtype</span></span> <br/> <i><span data-ttu-id="6039f-213">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-213">optional</span></span></i></td>
            <td><code class="flyout">string</code> <br/> <i><span data-ttu-id="6039f-214">Допустимые значения: null, error, promise</span><span class="sxs-lookup"><span data-stu-id="6039f-214">Allowed values: null, error, promise</span></span></i></td>
            <td><span data-ttu-id="6039f-215">Подсказка подтипа объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-215">Object subtype hint.</span></span> <span data-ttu-id="6039f-216">Указывается только <code>object</code> для значений типов.</span><span class="sxs-lookup"><span data-stu-id="6039f-216">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-217">className</span><span class="sxs-lookup"><span data-stu-id="6039f-217">className</span></span> <br/> <i><span data-ttu-id="6039f-218">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-218">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-219">Имя класса объекта (конструктора).</span><span class="sxs-lookup"><span data-stu-id="6039f-219">Object class (constructor) name.</span></span> <span data-ttu-id="6039f-220">Указывается только <code>object</code> для значений типов.</span><span class="sxs-lookup"><span data-stu-id="6039f-220">Specified for <code>object</code> type values only.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-221">value</span><span class="sxs-lookup"><span data-stu-id="6039f-221">value</span></span> <br/> <i><span data-ttu-id="6039f-222">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-222">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="6039f-223">Значение удаленного объекта в случае значений примитивов или значений JSON (если он был запротид).</span><span class="sxs-lookup"><span data-stu-id="6039f-223">Remote object value in case of primitive values or JSON values (if it was requested).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-224">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="6039f-224">unserializableValue</span></span> <br/> <i><span data-ttu-id="6039f-225">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-225">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="6039f-226">Значение примитива, которое не может быть в строке JSON, не имеет</span><span class="sxs-lookup"><span data-stu-id="6039f-226">Primitive value which can not be JSON-stringified does not have</span></span> <code>value</code><span data-ttu-id="6039f-227">, но получает это свойство.</span><span class="sxs-lookup"><span data-stu-id="6039f-227">, but gets this property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-228">description</span><span class="sxs-lookup"><span data-stu-id="6039f-228">description</span></span> <br/> <i><span data-ttu-id="6039f-229">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-229">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-230">Строка представления объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-230">String representation of the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-231">objectId</span><span class="sxs-lookup"><span data-stu-id="6039f-231">objectId</span></span> <br/> <i><span data-ttu-id="6039f-232">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-232">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="6039f-233">Уникальный идентификатор объекта (для не примитивных значений).</span><span class="sxs-lookup"><span data-stu-id="6039f-233">Unique object identifier (for non-primitive values).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-234">msDebuggerPropertyId</span><span class="sxs-lookup"><span data-stu-id="6039f-234">msDebuggerPropertyId</span></span> <br/> <i><span data-ttu-id="6039f-235">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-235">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b><span data-ttu-id="6039f-236">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="6039f-236">Experimental.</span></span> </b></span><span data-ttu-id="6039f-237">Майкрософт: связанный ид свойства отладки для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-237">Microsoft: The associated debugger property id for this object.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> <span data-ttu-id="6039f-238">PropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="6039f-238">PropertyDescriptor</span></span> `object`

<span data-ttu-id="6039f-239">Дескриптор свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-239">Object property descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-240">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-240">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-241">name</span><span class="sxs-lookup"><span data-stu-id="6039f-241">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-242">Имя свойства или описание символа.</span><span class="sxs-lookup"><span data-stu-id="6039f-242">Property name or symbol description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-243">value</span><span class="sxs-lookup"><span data-stu-id="6039f-243">value</span></span> <br/> <i><span data-ttu-id="6039f-244">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-244">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-245">Значение, связанное со свойством.</span><span class="sxs-lookup"><span data-stu-id="6039f-245">The value associated with the property.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-246">writable</span><span class="sxs-lookup"><span data-stu-id="6039f-246">writable</span></span> <br/> <i><span data-ttu-id="6039f-247">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-247">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-248">Имеет значение True, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</span><span class="sxs-lookup"><span data-stu-id="6039f-248">True if the value associated with the property may be changed (data descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-249">получить</span><span class="sxs-lookup"><span data-stu-id="6039f-249">get</span></span> <br/> <i><span data-ttu-id="6039f-250">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-250">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-251">Функция, которая служит в качестве дескриптора для свойства, или если нет <code>undefined</code> getter (только дескрипторы доступа).</span><span class="sxs-lookup"><span data-stu-id="6039f-251">A function which serves as a getter for the property, or <code>undefined</code> if there is no getter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-252">set</span><span class="sxs-lookup"><span data-stu-id="6039f-252">set</span></span> <br/> <i><span data-ttu-id="6039f-253">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-253">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-254">Функция, которая служит в качестве задавщика для свойства или если нет задавщика <code>undefined</code> (только дескрипторы доступа).</span><span class="sxs-lookup"><span data-stu-id="6039f-254">A function which serves as a setter for the property, or <code>undefined</code> if there is no setter (accessor descriptors only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-255">настраиваемая</span><span class="sxs-lookup"><span data-stu-id="6039f-255">configurable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-256">True, если тип этого дескриптора свойства может быть изменен и свойство может быть удалено из соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-256">True if the type of this property descriptor may be changed and if the property may be deleted from the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-257">enumerable</span><span class="sxs-lookup"><span data-stu-id="6039f-257">enumerable</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-258">True, если это свойство появляется во время нумерации свойств соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-258">True if this property shows up during enumeration of the properties on the corresponding object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-259">wasThrown</span><span class="sxs-lookup"><span data-stu-id="6039f-259">wasThrown</span></span> <br/> <i><span data-ttu-id="6039f-260">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-260">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-261">True, если результат был выброшен во время оценки.</span><span class="sxs-lookup"><span data-stu-id="6039f-261">True if the result was thrown during the evaluation.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-262">isOwn</span><span class="sxs-lookup"><span data-stu-id="6039f-262">isOwn</span></span> <br/> <i><span data-ttu-id="6039f-263">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-263">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="6039f-264">Имеет свойство True, если свойство принадлежит объекту.</span><span class="sxs-lookup"><span data-stu-id="6039f-264">True if the property is owned for the object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-265">msReturnValue</span><span class="sxs-lookup"><span data-stu-id="6039f-265">msReturnValue</span></span> <br/> <i><span data-ttu-id="6039f-266">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-266">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b><span data-ttu-id="6039f-267">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="6039f-267">Experimental.</span></span> </b></span><span data-ttu-id="6039f-268">Майкрософт: имеет значение True, если свойство является возвращаемой.</span><span class="sxs-lookup"><span data-stu-id="6039f-268">Microsoft: True if the property is a return value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-269">symbol,</span><span class="sxs-lookup"><span data-stu-id="6039f-269">symbol</span></span> <br/> <i><span data-ttu-id="6039f-270">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-270">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-271">Объект символа свойства, если свойство имеет `symbol` тип.</span><span class="sxs-lookup"><span data-stu-id="6039f-271">Property symbol object, if the property is of the `symbol` type.</span></span> </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> <span data-ttu-id="6039f-272">CallArgument</span><span class="sxs-lookup"><span data-stu-id="6039f-272">CallArgument</span></span> `object`

<span data-ttu-id="6039f-273">Представляет аргумент вызова функции.</span><span class="sxs-lookup"><span data-stu-id="6039f-273">Represents function call argument.</span></span> <span data-ttu-id="6039f-274">Должен быть указан либо ид удаленного <code>objectId</code> объекта, примитив, несериализируемый значение примитива, либо ни один <code>value</code> из них (для неопределенных).</span><span class="sxs-lookup"><span data-stu-id="6039f-274">Either remote object id <code>objectId</code>, primitive <code>value</code>, unserializable primitive value or neither of (for undefined) them should be specified.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-275">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-275">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-276">value</span><span class="sxs-lookup"><span data-stu-id="6039f-276">value</span></span> <br/> <i><span data-ttu-id="6039f-277">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-277">optional</span></span></i></td>
            <td><code class="flyout">any</code></td>
            <td><span data-ttu-id="6039f-278">Значение примитива или сериализуемый объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-278">Primitive value or serializable javascript object.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-279">unserializableValue</span><span class="sxs-lookup"><span data-stu-id="6039f-279">unserializableValue</span></span> <br/> <i><span data-ttu-id="6039f-280">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-280">optional</span></span></i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td><span data-ttu-id="6039f-281">Значение примитива, которое не может быть в строке JSON.</span><span class="sxs-lookup"><span data-stu-id="6039f-281">Primitive value which can not be JSON-stringified.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-282">objectId</span><span class="sxs-lookup"><span data-stu-id="6039f-282">objectId</span></span> <br/> <i><span data-ttu-id="6039f-283">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-283">optional</span></span></i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td><span data-ttu-id="6039f-284">Удаленный handle объекта.</span><span class="sxs-lookup"><span data-stu-id="6039f-284">Remote object handle.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> <span data-ttu-id="6039f-285">ExecutionContextId</span><span class="sxs-lookup"><span data-stu-id="6039f-285">ExecutionContextId</span></span> `integer`

<span data-ttu-id="6039f-286">ИД контекста выполнения.</span><span class="sxs-lookup"><span data-stu-id="6039f-286">Id of an execution context.</span></span>


---

### <a name="exceptiondetails"></a> <span data-ttu-id="6039f-287">ExceptionDetails</span><span class="sxs-lookup"><span data-stu-id="6039f-287">ExceptionDetails</span></span> `object`

<span data-ttu-id="6039f-288">Подробные сведения об исключении (или ошибке), которое было выброшено во время компиляции или выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="6039f-288">Detailed information about exception (or error) that was thrown during script compilation or execution.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-289">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-289">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-290">exceptionId</span><span class="sxs-lookup"><span data-stu-id="6039f-290">exceptionId</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6039f-291">ИД исключения.</span><span class="sxs-lookup"><span data-stu-id="6039f-291">Exception id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-292">текст</span><span class="sxs-lookup"><span data-stu-id="6039f-292">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-293">Текст исключения, который должен использоваться вместе с объектом исключения при наличии.</span><span class="sxs-lookup"><span data-stu-id="6039f-293">Exception text, which should be used together with exception object when available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-294">lineNumber</span><span class="sxs-lookup"><span data-stu-id="6039f-294">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6039f-295">Номер строки расположения исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="6039f-295">Line number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-296">columnNumber</span><span class="sxs-lookup"><span data-stu-id="6039f-296">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6039f-297">Номер столбца расположения исключения (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="6039f-297">Column number of the exception location (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-298">scriptId</span><span class="sxs-lookup"><span data-stu-id="6039f-298">scriptId</span></span> <br/> <i><span data-ttu-id="6039f-299">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-299">optional</span></span></i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="6039f-300">ИД сценария расположения исключения.</span><span class="sxs-lookup"><span data-stu-id="6039f-300">Script ID of the exception location.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-301">url</span><span class="sxs-lookup"><span data-stu-id="6039f-301">url</span></span> <br/> <i><span data-ttu-id="6039f-302">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-302">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-303">URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан.</span><span class="sxs-lookup"><span data-stu-id="6039f-303">URL of the exception location, to be used when the script was not reported.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-304">stackTrace</span><span class="sxs-lookup"><span data-stu-id="6039f-304">stackTrace</span></span> <br/> <i><span data-ttu-id="6039f-305">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-305">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="6039f-306">Трассировка стека JavaScript, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="6039f-306">JavaScript stack trace if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-307">exception</span><span class="sxs-lookup"><span data-stu-id="6039f-307">exception</span></span> <br/> <i><span data-ttu-id="6039f-308">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-308">optional</span></span></i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td><span data-ttu-id="6039f-309">Объект исключения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="6039f-309">Exception object if available.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-310">executionContextId</span><span class="sxs-lookup"><span data-stu-id="6039f-310">executionContextId</span></span> <br/> <i><span data-ttu-id="6039f-311">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-311">optional</span></span></i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td><span data-ttu-id="6039f-312">Идентификатор контекста, в котором произошло исключение.</span><span class="sxs-lookup"><span data-stu-id="6039f-312">Identifier of the context where exception happened.</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> <span data-ttu-id="6039f-313">Метка времени</span><span class="sxs-lookup"><span data-stu-id="6039f-313">Timestamp</span></span> `integer`

<span data-ttu-id="6039f-314">Количество миллисекунд с момента эпохи.</span><span class="sxs-lookup"><span data-stu-id="6039f-314">Number of milliseconds since epoch.</span></span>


---

### <a name="callframe"></a> <span data-ttu-id="6039f-315">CallFrame</span><span class="sxs-lookup"><span data-stu-id="6039f-315">CallFrame</span></span> `object`

<span data-ttu-id="6039f-316">Запись стека для ошибок и утверждений во время работы.</span><span class="sxs-lookup"><span data-stu-id="6039f-316">Stack entry for runtime errors and assertions.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-317">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-317">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-318">functionName</span><span class="sxs-lookup"><span data-stu-id="6039f-318">functionName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-319">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-319">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-320">scriptId</span><span class="sxs-lookup"><span data-stu-id="6039f-320">scriptId</span></span></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td><span data-ttu-id="6039f-321">ИД скрипта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-321">JavaScript script id.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-322">url</span><span class="sxs-lookup"><span data-stu-id="6039f-322">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-323">Имя или URL-адрес сценария JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-323">JavaScript script name or url.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-324">lineNumber</span><span class="sxs-lookup"><span data-stu-id="6039f-324">lineNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6039f-325">Номер строки сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="6039f-325">JavaScript script line number (0-based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-326">columnNumber</span><span class="sxs-lookup"><span data-stu-id="6039f-326">columnNumber</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="6039f-327">Номер столбца сценария JavaScript (на основе 0).</span><span class="sxs-lookup"><span data-stu-id="6039f-327">JavaScript script column number (0-based).</span></span></td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> <span data-ttu-id="6039f-328">StackTrace</span><span class="sxs-lookup"><span data-stu-id="6039f-328">StackTrace</span></span> `object`

<span data-ttu-id="6039f-329">Вызов кадров для утверждений или сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="6039f-329">Call frames for assertions or error messages.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="6039f-330">Свойства</span><span class="sxs-lookup"><span data-stu-id="6039f-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="6039f-331">description</span><span class="sxs-lookup"><span data-stu-id="6039f-331">description</span></span> <br/> <i><span data-ttu-id="6039f-332">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-332">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="6039f-333">Строковая метка трассировки стека.</span><span class="sxs-lookup"><span data-stu-id="6039f-333">String label of this stack trace.</span></span> <span data-ttu-id="6039f-334">Для а async traces это может быть имя функции, которая инициировала ассынский вызов.</span><span class="sxs-lookup"><span data-stu-id="6039f-334">For async traces this may be a name of the function that initiated the async call.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-335">callFrames</span><span class="sxs-lookup"><span data-stu-id="6039f-335">callFrames</span></span></td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td><span data-ttu-id="6039f-336">Имя функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6039f-336">JavaScript function name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="6039f-337">parent</span><span class="sxs-lookup"><span data-stu-id="6039f-337">parent</span></span> <br/> <i><span data-ttu-id="6039f-338">необязательные</span><span class="sxs-lookup"><span data-stu-id="6039f-338">optional</span></span></i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td><span data-ttu-id="6039f-339">Асинхронная трассировка стека JavaScript, предшествующего этому стеку, если доступна.</span><span class="sxs-lookup"><span data-stu-id="6039f-339">Asynchronous JavaScript stack trace that preceded this stack, if available.</span></span></td>
        </tr>
    </tbody>
</table>

---
