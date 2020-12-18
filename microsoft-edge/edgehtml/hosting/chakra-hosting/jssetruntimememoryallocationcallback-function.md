---
description: Задает callback выделения памяти для указанной времени работы.
title: JsSetRuntimeMemoryAllocationCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ee2abf36e14c26ac58b90d48a6115fd6502307c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235460"
---
# <span data-ttu-id="325e0-103">Функция JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="325e0-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>

<span data-ttu-id="325e0-104">Задает callback выделения памяти для указанной времени работы.</span><span class="sxs-lookup"><span data-stu-id="325e0-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="325e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="325e0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="325e0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="325e0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="325e0-107">Время запуска, для которого необходимо зарегистрировать вызов выделения.</span><span class="sxs-lookup"><span data-stu-id="325e0-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="325e0-108">Пользовательское состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="325e0-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="325e0-109">Callback выделения памяти, вызываемой для событий выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="325e0-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="325e0-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="325e0-110">Return Value</span></span>  
 <span data-ttu-id="325e0-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="325e0-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="325e0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="325e0-112">Remarks</span></span>  
 <span data-ttu-id="325e0-113">Регистрация обратного вызова выделения памяти приведет к тому, что время работы будет вызывать хост каждый раз, когда она получает память от ОС или освобождает ее в нее.</span><span class="sxs-lookup"><span data-stu-id="325e0-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="325e0-114">Процедура перенаправления вызовов вызвана до того, как диспетчер памяти во время работы выделяет блок памяти.</span><span class="sxs-lookup"><span data-stu-id="325e0-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="325e0-115">Выделение будет отклонено, если при обратном вызове возвращается false.</span><span class="sxs-lookup"><span data-stu-id="325e0-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="325e0-116">Диспетчер памяти во время работы также вызывает процедуру вызова после освободить блок памяти, а также после сбоев выделения.</span><span class="sxs-lookup"><span data-stu-id="325e0-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="325e0-117">Этот вызов вызывается в текущем потоке выполнения времени выполнения, поэтому выполнение блокируется до тех пор, пока он не завершится.</span><span class="sxs-lookup"><span data-stu-id="325e0-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="325e0-118">Возвращаемая величина обратного вызова не сохраняется; ранее отклоненные выделения не помешают времени работы вызвать обратное вызов позже для нового выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="325e0-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="325e0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="325e0-119">Requirements</span></span>  
 <span data-ttu-id="325e0-120">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="325e0-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="325e0-121">См. также</span><span class="sxs-lookup"><span data-stu-id="325e0-121">See Also</span></span>  
 [<span data-ttu-id="325e0-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="325e0-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
