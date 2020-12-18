---
description: Получает текущий предел памяти для времени работы.
title: JsGetRuntimeMemoryLimit Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ed04a0fb921d22eea17eaf86ef7a0152fbf2a1d0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235814"
---
# <span data-ttu-id="b5abf-103">Функция JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="b5abf-103">JsGetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="b5abf-104">Получает текущий предел памяти для времени работы.</span><span class="sxs-lookup"><span data-stu-id="b5abf-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="b5abf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5abf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="b5abf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5abf-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="b5abf-107">Время работы, для которого требуется получить ограничение памяти.</span><span class="sxs-lookup"><span data-stu-id="b5abf-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="b5abf-108">Текущее ограничение памяти в времени работы (в ветвях) или -1, если ограничение не за установлено.</span><span class="sxs-lookup"><span data-stu-id="b5abf-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="b5abf-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b5abf-109">Return Value</span></span>  
 <span data-ttu-id="b5abf-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="b5abf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b5abf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5abf-111">Remarks</span></span>  
 <span data-ttu-id="b5abf-112">Ограничение памяти для времени работы всегда можно получить независимо от того, активна ли она в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="b5abf-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="b5abf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b5abf-113">Requirements</span></span>  
 <span data-ttu-id="b5abf-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="b5abf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b5abf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b5abf-115">See Also</span></span>  
 [<span data-ttu-id="b5abf-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b5abf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
