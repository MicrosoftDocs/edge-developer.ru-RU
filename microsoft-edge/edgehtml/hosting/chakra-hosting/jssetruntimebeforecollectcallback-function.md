---
description: 'Задает функцию вызова, вызываемую во время работы перед сбором мусора. '
title: JsSetRuntimeBeforeCollectCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235290"
---
# <span data-ttu-id="d5065-103">Функция JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="d5065-103">JsSetRuntimeBeforeCollectCallback Function</span></span>

<span data-ttu-id="d5065-104">Задает функцию вызова, вызываемую во время работы перед сбором мусора.</span><span class="sxs-lookup"><span data-stu-id="d5065-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="d5065-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5065-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="d5065-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5065-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="d5065-107">Время запуска, для которого необходимо зарегистрировать вызов выделения.</span><span class="sxs-lookup"><span data-stu-id="d5065-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="d5065-108">Пользовательское состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="d5065-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="d5065-109">Устанавливаемая функция вызова.</span><span class="sxs-lookup"><span data-stu-id="d5065-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="d5065-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d5065-110">Return Value</span></span>  
 <span data-ttu-id="d5065-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="d5065-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d5065-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5065-112">Remarks</span></span>  
 <span data-ttu-id="d5065-113">Этот вызов вызывается в текущем потоке выполнения времени выполнения, поэтому выполнение блокируется до тех пор, пока он не завершится.</span><span class="sxs-lookup"><span data-stu-id="d5065-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="d5065-114">Для подготовки к сборке мусора хосты могут использовать этот вызов.</span><span class="sxs-lookup"><span data-stu-id="d5065-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="d5065-115">Например, освобождая ненужные ссылки на объекты Chakra.</span><span class="sxs-lookup"><span data-stu-id="d5065-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="d5065-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d5065-116">Requirements</span></span>  
 <span data-ttu-id="d5065-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="d5065-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d5065-118">См. также</span><span class="sxs-lookup"><span data-stu-id="d5065-118">See Also</span></span>  
 [<span data-ttu-id="d5065-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d5065-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
