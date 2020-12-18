---
description: Создает boolean значение из `bool` значения.
title: JsBoolToBoolean Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3d6ec9f85d53e0d78c6bbe1c7d3282971831717b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235322"
---
# <span data-ttu-id="21a63-103">Функция JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="21a63-103">JsBoolToBoolean Function</span></span>

<span data-ttu-id="21a63-104">Создает boolean значение из `bool` значения.</span><span class="sxs-lookup"><span data-stu-id="21a63-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="21a63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21a63-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="21a63-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="21a63-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="21a63-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="21a63-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="21a63-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="21a63-108">The converted value.</span></span>  
  
## <span data-ttu-id="21a63-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="21a63-109">Return Value</span></span>  
 <span data-ttu-id="21a63-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="21a63-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="21a63-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="21a63-111">Remarks</span></span>  
 <span data-ttu-id="21a63-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="21a63-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="21a63-113">Требования</span><span class="sxs-lookup"><span data-stu-id="21a63-113">Requirements</span></span>  
 <span data-ttu-id="21a63-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="21a63-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="21a63-115">См. также</span><span class="sxs-lookup"><span data-stu-id="21a63-115">See Also</span></span>  
 [<span data-ttu-id="21a63-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="21a63-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
