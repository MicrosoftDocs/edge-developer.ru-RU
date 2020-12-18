---
description: Получает текущее использование памяти для времени работы.
title: JsGetRuntimeMemoryUsage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a9c8d59e8cf73ad178f539f2f9f0ed191ceb47fd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235875"
---
# <span data-ttu-id="c35b7-103">Функция JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="c35b7-103">JsGetRuntimeMemoryUsage Function</span></span>

<span data-ttu-id="c35b7-104">Получает текущее использование памяти для времени работы.</span><span class="sxs-lookup"><span data-stu-id="c35b7-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="c35b7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c35b7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="c35b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c35b7-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="c35b7-107">Время работы, использование памяти которого требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c35b7-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="c35b7-108">Текущее использование памяти в времени работы в ветвях.</span><span class="sxs-lookup"><span data-stu-id="c35b7-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="c35b7-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="c35b7-109">Return Value</span></span>  
 <span data-ttu-id="c35b7-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="c35b7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c35b7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c35b7-111">Remarks</span></span>  
 <span data-ttu-id="c35b7-112">Использование памяти всегда может быть извлечено независимо от того, активна ли она в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="c35b7-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="c35b7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c35b7-113">Requirements</span></span>  
 <span data-ttu-id="c35b7-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="c35b7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c35b7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c35b7-115">See Also</span></span>  
 [<span data-ttu-id="c35b7-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c35b7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
