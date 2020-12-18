---
description: Callback called before collecting an object.
title: JsObjectBeforeCollectCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235641"
---
# <span data-ttu-id="bfb2e-103">JsObjectBeforeCollectCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="bfb2e-103">JsObjectBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="bfb2e-104">Callback called before collecting an object.</span><span class="sxs-lookup"><span data-stu-id="bfb2e-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="bfb2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfb2e-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="bfb2e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfb2e-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="bfb2e-107">Объект, который необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="bfb2e-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="bfb2e-108">Состояние, переданного в `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="bfb2e-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="bfb2e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfb2e-109">Remarks</span></span>  
 <span data-ttu-id="bfb2e-110">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="bfb2e-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="bfb2e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bfb2e-111">Requirements</span></span>  
 <span data-ttu-id="bfb2e-112">jsrt.h</span><span class="sxs-lookup"><span data-stu-id="bfb2e-112">jsrt.h</span></span>  
  
## <span data-ttu-id="bfb2e-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bfb2e-113">See Also</span></span>  
 [<span data-ttu-id="bfb2e-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bfb2e-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
