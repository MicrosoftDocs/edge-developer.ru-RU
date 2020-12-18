---
description: Получает тип JavaScript JsValueRef.
title: JsGetValueType Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b2e9937ca13bf2a680a4a33c07020d06c53efdf3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235170"
---
# <span data-ttu-id="59f90-103">Функция JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="59f90-103">JsGetValueType Function</span></span>

<span data-ttu-id="59f90-104">Получает тип JavaScript JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="59f90-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="59f90-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59f90-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="59f90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59f90-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="59f90-107">Значение, тип которого должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="59f90-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="59f90-108">Тип значения.</span><span class="sxs-lookup"><span data-stu-id="59f90-108">The type of the value.</span></span>  
  
## <span data-ttu-id="59f90-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="59f90-109">Return Value</span></span>  
 <span data-ttu-id="59f90-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="59f90-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="59f90-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59f90-111">Remarks</span></span>  
 <span data-ttu-id="59f90-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="59f90-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="59f90-113">Требования</span><span class="sxs-lookup"><span data-stu-id="59f90-113">Requirements</span></span>  
 <span data-ttu-id="59f90-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="59f90-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="59f90-115">См. также</span><span class="sxs-lookup"><span data-stu-id="59f90-115">See Also</span></span>  
 [<span data-ttu-id="59f90-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="59f90-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
