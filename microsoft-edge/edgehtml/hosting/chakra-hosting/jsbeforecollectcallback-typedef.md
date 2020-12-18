---
description: Callback called before collection.
title: JsBeforeCollectCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235325"
---
# <span data-ttu-id="e4e4c-103">JsBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="e4e4c-103">JsBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="e4e4c-104">Callback called before collection.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="e4e4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4e4c-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="e4e4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4e4c-106">Parameters</span></span>  
 <span data-ttu-id="e4e4c-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="e4e4c-107">callbackState</span></span>  
 <span data-ttu-id="e4e4c-108">Состояние, передамое в JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="e4e4c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4e4c-109">Remarks</span></span>  
 <span data-ttu-id="e4e4c-110">Используйте JsSetBeforeCollectCallback для регистрации этого вызова.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="e4e4c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e4e4c-111">Requirements</span></span>  
 <span data-ttu-id="e4e4c-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e4e4c-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e4e4c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e4e4c-113">See Also</span></span>  
 [<span data-ttu-id="e4e4c-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e4e4c-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
