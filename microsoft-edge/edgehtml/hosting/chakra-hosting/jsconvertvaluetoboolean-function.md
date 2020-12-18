---
description: Преобразует значение в boolean с помощью стандартной семантики JavaScript.
title: JsConvertValueToBoolean Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToBoolean
helpviewer_keywords:
- JsConvertValueToBoolean function
ms.assetid: 7298ec72-a388-4334-b81b-1691ab4cecf0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d2e109690fc8a7a98a1ecb84d6f5abf6a646162b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235321"
---
# <span data-ttu-id="0a911-103">Функция JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="0a911-103">JsConvertValueToBoolean Function</span></span>

<span data-ttu-id="0a911-104">Преобразует значение в boolean с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a911-104">Converts the value to Boolean using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="0a911-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a911-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToBoolean(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="0a911-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a911-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="0a911-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="0a911-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="0a911-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="0a911-108">The converted value.</span></span>  
  
## <span data-ttu-id="0a911-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0a911-109">Return Value</span></span>  
 <span data-ttu-id="0a911-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="0a911-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0a911-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a911-111">Remarks</span></span>  
 <span data-ttu-id="0a911-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="0a911-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0a911-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0a911-113">Requirements</span></span>  
 <span data-ttu-id="0a911-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="0a911-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0a911-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0a911-115">See Also</span></span>  
 [<span data-ttu-id="0a911-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0a911-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
