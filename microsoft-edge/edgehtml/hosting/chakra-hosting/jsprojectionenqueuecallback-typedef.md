---
description: Вызов приложения, вызываемого JsRT при заполнении API проекции в потоке, отличаемом от исходного.
title: JsProjectionEnqueueCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235866"
---
# <span data-ttu-id="c9c92-103">JsProjectionEnqueueCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="c9c92-103">JsProjectionEnqueueCallback Typedef</span></span>

<span data-ttu-id="c9c92-104">Вызов приложения, вызываемого JsRT при заполнении API проекции в потоке, отличаемом от исходного.</span><span class="sxs-lookup"><span data-stu-id="c9c92-104">The application callback which is called by JsRT when a projection API is completed on a different thread than the original.</span></span>  
  
## <span data-ttu-id="c9c92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9c92-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="c9c92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9c92-106">Parameters</span></span>  
 `jsCallback`  
 <span data-ttu-id="c9c92-107">Callback to be invoked on the original thread.</span><span class="sxs-lookup"><span data-stu-id="c9c92-107">The callback to be invoked on the original thread.</span></span>  
  
 `jsContext`  
 <span data-ttu-id="c9c92-108">Контекст приложений.</span><span class="sxs-lookup"><span data-stu-id="c9c92-108">The applications context.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="c9c92-109">Контекст JsRT, который необходимо `jsCallback` передать.</span><span class="sxs-lookup"><span data-stu-id="c9c92-109">The JsRT context that must be passed into `jsCallback`.</span></span>  
  
## <span data-ttu-id="c9c92-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9c92-110">Remarks</span></span>  
 <span data-ttu-id="c9c92-111">Для получения вызовов требуется вызов JsSetProjectionEnqueueCallback.</span><span class="sxs-lookup"><span data-stu-id="c9c92-111">Requires calling JsSetProjectionEnqueueCallback to receive callbacks.</span></span>  
  
 <span data-ttu-id="c9c92-112">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="c9c92-112">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="c9c92-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c9c92-113">Requirements</span></span>  
 <span data-ttu-id="c9c92-114">jsrt.h</span><span class="sxs-lookup"><span data-stu-id="c9c92-114">jsrt.h</span></span>  
  
## <span data-ttu-id="c9c92-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c9c92-115">See Also</span></span>  
 [<span data-ttu-id="c9c92-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c9c92-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
