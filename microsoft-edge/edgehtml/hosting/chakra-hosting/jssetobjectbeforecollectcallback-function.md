---
description: Задает функцию вызова, вызываемую во время работы перед сборкой мусора объекта.
title: JsSetObjectBeforeCollectCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235289"
---
# <span data-ttu-id="e3645-103">Функция JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="e3645-103">JsSetObjectBeforeCollectCallback Function</span></span>

<span data-ttu-id="e3645-104">Задает функцию вызова, вызываемую во время работы перед сборкой мусора объекта.</span><span class="sxs-lookup"><span data-stu-id="e3645-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="e3645-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3645-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="e3645-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3645-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="e3645-107">Объект, для которого необходимо зарегистрировать вызов.</span><span class="sxs-lookup"><span data-stu-id="e3645-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e3645-108">Предоставленное пользователем состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="e3645-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="e3645-109">Устанавливаемая функция вызова.</span><span class="sxs-lookup"><span data-stu-id="e3645-109">The callback function being set.</span></span> <span data-ttu-id="e3645-110">Используйте null, чтобы очистить зарегистрированный ранее вызов.</span><span class="sxs-lookup"><span data-stu-id="e3645-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="e3645-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e3645-111">Return Value</span></span>  
 <span data-ttu-id="e3645-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="e3645-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e3645-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3645-113">Remarks</span></span>  
 <span data-ttu-id="e3645-114">В текущем потоке выполнения выполнения вызывается метод callback, поэтому выполнение блокируется до тех пор, пока он не завершится.</span><span class="sxs-lookup"><span data-stu-id="e3645-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="e3645-115">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e3645-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="e3645-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e3645-116">Requirements</span></span>  
 <span data-ttu-id="e3645-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e3645-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e3645-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e3645-118">See Also</span></span>  
 [<span data-ttu-id="e3645-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e3645-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
