---
description: Вызов продолжения обещания.
title: JsPromiseContinuationCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235864"
---
# <span data-ttu-id="f4356-103">JsPromiseContinuationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="f4356-103">JsPromiseContinuationCallback Typedef</span></span>

<span data-ttu-id="f4356-104">Вызов продолжения обещания.</span><span class="sxs-lookup"><span data-stu-id="f4356-104">A promise continuation callback.</span></span>  
  
## <span data-ttu-id="f4356-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4356-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="f4356-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4356-106">Parameters</span></span>  
 `task`  
  `callbackState`  
  
## <span data-ttu-id="f4356-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4356-107">Remarks</span></span>  
 <span data-ttu-id="f4356-108">В хост-вызове можно указать вызов продолжения `JsSetPromiseContinuationCallback` promise.</span><span class="sxs-lookup"><span data-stu-id="f4356-108">The host can specify a promise continuation callback in `JsSetPromiseContinuationCallback`.</span></span> <span data-ttu-id="f4356-109">Если сценарий создает задачу, которая будет выполняться позже, то с задачей будет вызван вызов вызова продолжения promise, и задача должна быть поставлена в очередь FIFO, которая будет выполняться после выполнения текущего сценария.</span><span class="sxs-lookup"><span data-stu-id="f4356-109">If a script creates a task to be run later, then the promise continuation callback will be called with the task and the task should be put in a FIFO queue, to be run when the current script is done executing.</span></span>  
  
 <span data-ttu-id="f4356-110">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="f4356-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="f4356-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f4356-111">Requirements</span></span>  
 <span data-ttu-id="f4356-112">jsrt.h</span><span class="sxs-lookup"><span data-stu-id="f4356-112">jsrt.h</span></span>  
  
## <span data-ttu-id="f4356-113">См. также</span><span class="sxs-lookup"><span data-stu-id="f4356-113">See Also</span></span>  
 [<span data-ttu-id="f4356-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f4356-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
