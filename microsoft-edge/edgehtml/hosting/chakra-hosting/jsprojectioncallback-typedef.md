---
description: Вызов JsRT с контекстом, переданным в `JsProjectionEnqueueCallback` правильном потоке.
title: JsProjectionCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235631"
---
# <span data-ttu-id="83ab9-103">JsProjectionCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="83ab9-103">JsProjectionCallback Typedef</span></span>

<span data-ttu-id="83ab9-104">Вызов JsRT с контекстом, переданным в `JsProjectionEnqueueCallback` правильном потоке.</span><span class="sxs-lookup"><span data-stu-id="83ab9-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="83ab9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83ab9-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="83ab9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83ab9-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="83ab9-107">Требует вызова `JsSetProjectionEnqueueCallback` для получения вызовов.</span><span class="sxs-lookup"><span data-stu-id="83ab9-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="83ab9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83ab9-108">Remarks</span></span>  
 <span data-ttu-id="83ab9-109">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="83ab9-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="83ab9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="83ab9-110">Requirements</span></span>  
 <span data-ttu-id="83ab9-111">jsrt.h</span><span class="sxs-lookup"><span data-stu-id="83ab9-111">jsrt.h</span></span>  
  
## <span data-ttu-id="83ab9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="83ab9-112">See Also</span></span>  
 [<span data-ttu-id="83ab9-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="83ab9-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
