---
description: Создает значение числа из двойного значения.
title: JsDoubleToNumber Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDoubleToNumber
helpviewer_keywords:
- JsDoubleToNumber function
ms.assetid: 43eb2ee1-2789-4302-954e-c4087e1ee786
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3385633f41c2e20c43ca865eaeec763b6ff7f43
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235504"
---
# <span data-ttu-id="3792d-103">Функция JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="3792d-103">JsDoubleToNumber Function</span></span>

<span data-ttu-id="3792d-104">Создает значение числа из `double` значения.</span><span class="sxs-lookup"><span data-stu-id="3792d-104">Creates a number value from a `double` value.</span></span>  
  
## <span data-ttu-id="3792d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3792d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDoubleToNumber(  
   _In_ double doubleValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="3792d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3792d-106">Parameters</span></span>  
 `doubleValue`  
 <span data-ttu-id="3792d-107">Значение `double` для преобразования в число.</span><span class="sxs-lookup"><span data-stu-id="3792d-107">The `double` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="3792d-108">Новое значение номера.</span><span class="sxs-lookup"><span data-stu-id="3792d-108">The new number value.</span></span>  
  
## <span data-ttu-id="3792d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3792d-109">Return Value</span></span>  
 <span data-ttu-id="3792d-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3792d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3792d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3792d-111">Remarks</span></span>  
 <span data-ttu-id="3792d-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="3792d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3792d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3792d-113">Requirements</span></span>  
 <span data-ttu-id="3792d-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3792d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3792d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3792d-115">See Also</span></span>  
 [<span data-ttu-id="3792d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3792d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
