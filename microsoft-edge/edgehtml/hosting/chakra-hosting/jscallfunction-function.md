---
description: Вызывает функцию.
title: JsCallFunction Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCallFunction
helpviewer_keywords:
- JsCallFunction function
ms.assetid: 8a1dca72-d720-4a28-a86e-6809465006fe
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dc26f66cb7deae0857ce34cbd4d83ee26046b3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235319"
---
# <span data-ttu-id="b2a2a-103">Функция JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="b2a2a-103">JsCallFunction Function</span></span>

<span data-ttu-id="b2a2a-104">Вызывает функцию.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-104">Invokes a function.</span></span>  
  
## <span data-ttu-id="b2a2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2a2a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCallFunction(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="b2a2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2a2a-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="b2a2a-107">Вызываемая функция.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-107">The function to invoke.</span></span>  
  
 `arguments`  
 <span data-ttu-id="b2a2a-108">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="b2a2a-109">Количество аргументов, которые передаются в функцию.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="b2a2a-110">Значение, возвращаемая вызовом функции, если таково.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-110">The value returned from the function invocation, if any.</span></span>  
  
## <span data-ttu-id="b2a2a-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b2a2a-111">Return Value</span></span>  
 <span data-ttu-id="b2a2a-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b2a2a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2a2a-113">Remarks</span></span>  
 <span data-ttu-id="b2a2a-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="b2a2a-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b2a2a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b2a2a-115">Requirements</span></span>  
 <span data-ttu-id="b2a2a-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="b2a2a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b2a2a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b2a2a-117">See Also</span></span>  
 [<span data-ttu-id="b2a2a-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b2a2a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
