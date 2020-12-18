---
description: Извлекает `int` значение числимого значения.
title: JsNumberToInt Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235643"
---
# <span data-ttu-id="2a647-103">Функция JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="2a647-103">JsNumberToInt Function</span></span>

<span data-ttu-id="2a647-104">Извлекает `int` значение числимого значения.</span><span class="sxs-lookup"><span data-stu-id="2a647-104">Retrieves the `int` value of a number value.</span></span>  
  
## <span data-ttu-id="2a647-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a647-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### <span data-ttu-id="2a647-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a647-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="2a647-107">Число, преобразуемого в `int` значение.</span><span class="sxs-lookup"><span data-stu-id="2a647-107">The number value to convert to an `int` value.</span></span>  
  
 `intValue`  
 <span data-ttu-id="2a647-108">`int`Значение.</span><span class="sxs-lookup"><span data-stu-id="2a647-108">The `int` value.</span></span>  
  
## <span data-ttu-id="2a647-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="2a647-109">Return Value</span></span>  
  
## <span data-ttu-id="2a647-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a647-110">Remarks</span></span>  
 <span data-ttu-id="2a647-111">Эта функция извлекает значение числимого значения и преобразуется в `int` значение.</span><span class="sxs-lookup"><span data-stu-id="2a647-111">This function retrieves the value of a number value and converts to an `int` value.</span></span> <span data-ttu-id="2a647-112">Он не будет `JsErrorInvalidArgument` работать, если тип значения не является числом.</span><span class="sxs-lookup"><span data-stu-id="2a647-112">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="2a647-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="2a647-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2a647-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="2a647-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="2a647-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2a647-115">Requirements</span></span>  
 <span data-ttu-id="2a647-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="2a647-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2a647-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2a647-117">See Also</span></span>  
 [<span data-ttu-id="2a647-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2a647-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
