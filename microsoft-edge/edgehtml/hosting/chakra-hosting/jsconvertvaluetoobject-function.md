---
description: Преобразует значение в объект с помощью стандартной семантики JavaScript.
title: JsConvertValueToObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6f3676b512585b0750c994bcfcdf9d2e6e4e1cc3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235307"
---
# <span data-ttu-id="f8029-103">Функция JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="f8029-103">JsConvertValueToObject Function</span></span>

<span data-ttu-id="f8029-104">Преобразует значение в объект с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f8029-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="f8029-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8029-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="f8029-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8029-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="f8029-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="f8029-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="f8029-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="f8029-108">The converted value.</span></span>  
  
## <span data-ttu-id="f8029-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f8029-109">Return Value</span></span>  
 <span data-ttu-id="f8029-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="f8029-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f8029-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8029-111">Remarks</span></span>  
 <span data-ttu-id="f8029-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="f8029-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f8029-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f8029-113">Requirements</span></span>  
 <span data-ttu-id="f8029-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="f8029-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f8029-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f8029-115">See Also</span></span>  
 [<span data-ttu-id="f8029-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f8029-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
