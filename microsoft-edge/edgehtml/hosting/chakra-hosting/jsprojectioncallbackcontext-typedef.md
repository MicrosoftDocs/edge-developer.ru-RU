---
description: Контекст, переданный в обратном вызове приложения JsProjectionEnqueueCallback из JsRT, а затем передан обратно в JsRT в предоставленном обратном вызове приложением в правильном `JsProjectionCallback` потоке.
title: JsProjectionCallbackContext Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235627"
---
# <span data-ttu-id="91025-103">JsProjectionCallbackContext Typedef</span><span class="sxs-lookup"><span data-stu-id="91025-103">JsProjectionCallbackContext Typedef</span></span>

<span data-ttu-id="91025-104">Контекст, переданный в обратном вызове приложения JsProjectionEnqueueCallback из JsRT, а затем передан обратно в JsRT в предоставленном обратном вызове приложением в правильном `JsProjectionCallback` потоке.</span><span class="sxs-lookup"><span data-stu-id="91025-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="91025-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91025-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="91025-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91025-106">Remarks</span></span>  
 <span data-ttu-id="91025-107">Требует вызова `JsSetProjectionEnqueueCallback` для получения вызовов.</span><span class="sxs-lookup"><span data-stu-id="91025-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="91025-108">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="91025-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="91025-109">Требования</span><span class="sxs-lookup"><span data-stu-id="91025-109">Requirements</span></span>  
 <span data-ttu-id="91025-110">jsrt.h</span><span class="sxs-lookup"><span data-stu-id="91025-110">jsrt.h</span></span>  
  
## <span data-ttu-id="91025-111">См. также</span><span class="sxs-lookup"><span data-stu-id="91025-111">See Also</span></span>  
 [<span data-ttu-id="91025-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="91025-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
