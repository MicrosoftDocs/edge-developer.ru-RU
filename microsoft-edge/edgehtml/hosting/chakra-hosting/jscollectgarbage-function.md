---
description: Выполняет полную сборку мусора.
title: JsCollectGarbage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c551ddf119ec0aa349fcd756f6001d92dbbb0faa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235320"
---
# <span data-ttu-id="625f0-103">Функция JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="625f0-103">JsCollectGarbage Function</span></span>

<span data-ttu-id="625f0-104">Выполняет полную сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="625f0-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="625f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="625f0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="625f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="625f0-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="625f0-107">Время выполнения, в котором будет выполняться сборка мусора.</span><span class="sxs-lookup"><span data-stu-id="625f0-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="625f0-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="625f0-108">Return Value</span></span>  
 <span data-ttu-id="625f0-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="625f0-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="625f0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="625f0-110">Requirements</span></span>  
 <span data-ttu-id="625f0-111">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="625f0-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="625f0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="625f0-112">See Also</span></span>  
 [<span data-ttu-id="625f0-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="625f0-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
