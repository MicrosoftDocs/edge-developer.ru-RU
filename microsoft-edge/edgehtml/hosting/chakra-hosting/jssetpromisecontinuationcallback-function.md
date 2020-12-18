---
description: Задает функцию вызова продолжения promise, вызываемую контекстом, когда задача должна быть поставлена в очередь для дальнейшего выполнения.
title: JsSetPromiseContinuationCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235540"
---
# <span data-ttu-id="2b0f6-103">Функция JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="2b0f6-103">JsSetPromiseContinuationCallback Function</span></span>

<span data-ttu-id="2b0f6-104">Задает функцию вызова продолжения promise, вызываемую контекстом, когда задача должна быть поставлена в очередь для дальнейшего выполнения.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-104">Sets a promise continuation callback function that is called by the context when a task needs to be queued for future execution.</span></span>  
  
## <span data-ttu-id="2b0f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b0f6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="2b0f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b0f6-106">Parameters</span></span>  
 `promiseContinuationCallback`  
 <span data-ttu-id="2b0f6-107">Устанавливаемая функция вызова.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-107">The callback function being set.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="2b0f6-108">Пользовательское состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-108">User provided state that will be passed back to the callback.</span></span>  
  
## <span data-ttu-id="2b0f6-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="2b0f6-109">Return Value</span></span>  
 <span data-ttu-id="2b0f6-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2b0f6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b0f6-111">Remarks</span></span>  
 <span data-ttu-id="2b0f6-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2b0f6-113">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="2b0f6-113">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="2b0f6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="2b0f6-114">Requirements</span></span>  
 <span data-ttu-id="2b0f6-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="2b0f6-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2b0f6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="2b0f6-116">See Also</span></span>  
 [<span data-ttu-id="2b0f6-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2b0f6-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
