---
description: Получает time runtime, к которой принадлежит контекст.
title: JsGetRuntime Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 49739f0cf3675a44b9fc328e3eaa7d49c6282e53
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235517"
---
# <span data-ttu-id="bb109-103">Функция JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="bb109-103">JsGetRuntime Function</span></span>

<span data-ttu-id="bb109-104">Получает time runtime, к которой принадлежит контекст.</span><span class="sxs-lookup"><span data-stu-id="bb109-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="bb109-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb109-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="bb109-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb109-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="bb109-107">Контекст для получения времени работы.</span><span class="sxs-lookup"><span data-stu-id="bb109-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="bb109-108">Время работы, к которой принадлежит контекст.</span><span class="sxs-lookup"><span data-stu-id="bb109-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="bb109-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bb109-109">Return Value</span></span>  
 <span data-ttu-id="bb109-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="bb109-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bb109-111">Требования</span><span class="sxs-lookup"><span data-stu-id="bb109-111">Requirements</span></span>  
 <span data-ttu-id="bb109-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="bb109-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bb109-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bb109-113">See Also</span></span>  
 [<span data-ttu-id="bb109-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bb109-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
