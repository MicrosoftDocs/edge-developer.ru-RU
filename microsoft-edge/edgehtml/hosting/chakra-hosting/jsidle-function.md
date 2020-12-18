---
description: Сообщает времени работы, что необходимо выполнить любую обработку без простоя.
title: JsIdle Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235815"
---
# <span data-ttu-id="e8c5b-103">Функция JsIdle</span><span class="sxs-lookup"><span data-stu-id="e8c5b-103">JsIdle Function</span></span>

<span data-ttu-id="e8c5b-104">Сообщает времени работы, что необходимо выполнить любую обработку без простоя.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="e8c5b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8c5b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="e8c5b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8c5b-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="e8c5b-107">Следующий системный такт, когда будет больше работы без простоя.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="e8c5b-108">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-108">Can be null.</span></span> <span data-ttu-id="e8c5b-109">Возвращает максимальное число тактов, если предстоящих бездействуют.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="e8c5b-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e8c5b-110">Return Value</span></span>  
 <span data-ttu-id="e8c5b-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e8c5b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c5b-112">Remarks</span></span>  
 <span data-ttu-id="e8c5b-113">Если для текущей времени выполнения включена обработка бездействия, вызовы проинформят текущую порядок выполнения о том, что хост бездействует и что она может выполнять задачи очистки `JsIdle` памяти.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="e8c5b-114">также может возвращать количество системных тиков, пока не будет больше работы в режиме простоя, чтобы сделать это.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="e8c5b-115">Вызов до того, как прошло это число, не `JsIdle` даст никаких трудоемких трудоемкого.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="e8c5b-116">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="e8c5b-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e8c5b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c5b-117">Requirements</span></span>  
 <span data-ttu-id="e8c5b-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e8c5b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e8c5b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e8c5b-119">See Also</span></span>  
 [<span data-ttu-id="e8c5b-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e8c5b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
