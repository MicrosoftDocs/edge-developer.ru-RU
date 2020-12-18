---
description: Создает объект `ArrayBuffer` JavaScript.
title: JsCreateArrayBuffer Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235301"
---
# <span data-ttu-id="5bc1f-103">Функция JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="5bc1f-103">JsCreateArrayBuffer Function</span></span>

<span data-ttu-id="5bc1f-104">Создает объект `ArrayBuffer` JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="5bc1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5bc1f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="5bc1f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5bc1f-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="5bc1f-107">Количествобайтов в ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="5bc1f-108">Новый объект ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="5bc1f-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="5bc1f-109">Return Value</span></span>  
 <span data-ttu-id="5bc1f-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5bc1f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bc1f-111">Remarks</span></span>  
 <span data-ttu-id="5bc1f-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5bc1f-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="5bc1f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5bc1f-114">Requirements</span></span>  
 <span data-ttu-id="5bc1f-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="5bc1f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5bc1f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5bc1f-116">See Also</span></span>  
 [<span data-ttu-id="5bc1f-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
