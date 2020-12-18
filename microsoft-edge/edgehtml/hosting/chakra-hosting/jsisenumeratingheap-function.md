---
description: Возвращает значение, которое указывает, является ли куче текущего контекста является enumerated.
title: JsIsEnumeratingHeap Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsEnumeratingHeap
helpviewer_keywords:
- JsIsEnumeratingHeap function
ms.assetid: 5d14518e-3153-43f2-9a9c-068580cbd54f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5b66fc70ea79d78029f6bc0c900ade1aae38e604
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235677"
---
# <span data-ttu-id="abeb7-103">Функция JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="abeb7-103">JsIsEnumeratingHeap Function</span></span>

<span data-ttu-id="abeb7-104">Возвращает значение, которое указывает, является ли куче текущего контекста является enumerated.</span><span class="sxs-lookup"><span data-stu-id="abeb7-104">Returns a value that indicates whether the heap of the current context is being enumerated.</span></span>  
  
## <span data-ttu-id="abeb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abeb7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsEnumeratingHeap(  
   _Out_ bool *isEnumeratingHeap  
);  
```  
  
#### <span data-ttu-id="abeb7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="abeb7-106">Parameters</span></span>  
 `isEnumeratingHeap`  
 <span data-ttu-id="abeb7-107">Является ли кучи в настоящее время enumerated.</span><span class="sxs-lookup"><span data-stu-id="abeb7-107">Whether the heap is being enumerated.</span></span>  
  
## <span data-ttu-id="abeb7-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="abeb7-108">Return Value</span></span>  
 <span data-ttu-id="abeb7-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="abeb7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="abeb7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abeb7-110">Remarks</span></span>  
 <span data-ttu-id="abeb7-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="abeb7-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="abeb7-112">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="abeb7-112">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="abeb7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="abeb7-113">Requirements</span></span>  
 <span data-ttu-id="abeb7-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="abeb7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="abeb7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="abeb7-115">See Also</span></span>  
 [<span data-ttu-id="abeb7-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="abeb7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
