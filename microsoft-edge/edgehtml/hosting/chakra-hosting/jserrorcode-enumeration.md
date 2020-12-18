---
description: Код ошибки, возвращаемой из API размещения Chakra.
title: JsErrorCode Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b0a4aa7b47070bd5c8c7fe48cdbecf0dbefa9aa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235440"
---
# <span data-ttu-id="0b5a4-103">Перечисление JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="0b5a4-103">JsErrorCode Enumeration</span></span>

<span data-ttu-id="0b5a4-104">Код ошибки, возвращаемой из API размещения Chakra.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="0b5a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b5a4-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="0b5a4-106">Members</span><span class="sxs-lookup"><span data-stu-id="0b5a4-106">Members</span></span>  
  
### <span data-ttu-id="0b5a4-107">Значения</span><span class="sxs-lookup"><span data-stu-id="0b5a4-107">Values</span></span>  
  
|<span data-ttu-id="0b5a4-108">Имя</span><span class="sxs-lookup"><span data-stu-id="0b5a4-108">Name</span></span>|<span data-ttu-id="0b5a4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0b5a4-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="0b5a4-110">Контекст нельзя поместить в состояние отлаки, так как он уже находится в состоянии отлажки.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="0b5a4-111">Контекст не может начать профилирование, так как он уже профилирование.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="0b5a4-112">API размещения, который работает со значениями объектов, был вызван с не объектным значением.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="0b5a4-113">Использовался плохой сериализованный сценарий или сериализованный сценарий с помощью другой версии ядра Chakra.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="0b5a4-114">Runtime does not support reliable script interruption.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="0b5a4-115">Сценарии невозможно сериализовать в контекстах отлаки.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="0b5a4-116">Категория ошибок, которая связана с ошибками, которые происходят в самом движке.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="0b5a4-117">Категория ошибок, которые являются неудамительными и опишите сбой яда.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="0b5a4-118">Категория ошибок, которая связана с ошибками в сценарии.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="0b5a4-119">Категория ошибок, связанная с неправильным использованием самого API.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="0b5a4-120">Произошла неугомявная ошибка в движке.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="0b5a4-121">В настоящее время в контексте сценария ведется enumeration кучи.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="0b5a4-122">Уведомление о бездействии, отданное, когда хост не включает обработку бездействия.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="0b5a4-123">Время работы отключено.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="0b5a4-124">Обдвижок находится в состоянии исключения, и пока исключение не будет очищено, никакие API не могут быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="0b5a4-125">Операция не поддерживается в объекте перед сбором вызова.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="0b5a4-126">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="0b5a4-127">Контекст сценария находится в середине вызова профиля.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="0b5a4-128">В настоящее время проводится вызов службы потоков.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="0b5a4-129">Недопустимый аргумент для API размещения.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="0b5a4-130">Для размещения API требуется, чтобы контекст был текущим, но нет текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="0b5a4-131">API размещения еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="0b5a4-132">В контексте, где не допускается использовать null, аргумент API размещения имеет null.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="0b5a4-133">Объект не может быть развернулся на `IInspectable` указатель.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="0b5a4-134">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="0b5a4-135">В ядрах Chakra не потери памяти.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="0b5a4-136">API размещения, который работает с символьными идами свойств, но был вызван с не символьным идом свойства. Код ошибки возвращается, если функция вызвана с не `JsGetSymbolFromPropertyId` символьным идом свойства.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="0b5a4-137">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="0b5a4-138">API размещения, который работает с идами строковых свойств, но был вызван с не строковой ид свойства. Код ошибки возвращается существующим, если функция вызвана с не `JsGetPropertyNamefromId` строковым идом свойства.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="0b5a4-139">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="0b5a4-140">Используемая по-прежнему время работы не может быть высвоена.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="0b5a4-141">Не удалось скомпилировать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="0b5a4-142">Сценарий был прерван из-за того, что он пытался использовать или `eval` `function` был отключен.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="0b5a4-143">При запуске сценария произошло исключение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="0b5a4-144">Сценарий был завершен из-за запроса на приостановку работы.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="0b5a4-145">Был вызван API размещения с объектом, созданным в другой среде работы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="0b5a4-146">API размещения был вызван в неправильном потоке.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="0b5a4-147">Код ошибки успешной работы.</span><span class="sxs-lookup"><span data-stu-id="0b5a4-147">Success error code.</span></span>|  
  
## <span data-ttu-id="0b5a4-148">Требования</span><span class="sxs-lookup"><span data-stu-id="0b5a4-148">Requirements</span></span>  
 <span data-ttu-id="0b5a4-149">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="0b5a4-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0b5a4-150">См. также</span><span class="sxs-lookup"><span data-stu-id="0b5a4-150">See Also</span></span>  
 [<span data-ttu-id="0b5a4-151">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0b5a4-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
