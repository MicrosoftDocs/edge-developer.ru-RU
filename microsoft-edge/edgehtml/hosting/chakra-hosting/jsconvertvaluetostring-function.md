---
description: Преобразует значение в строку с помощью стандартной семантики JavaScript.
title: JsConvertValueToString Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 499f9555f6385b8458524fb4e14b92339c0aa478
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235306"
---
# <span data-ttu-id="a129a-103">Функция JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="a129a-103">JsConvertValueToString Function</span></span>

<span data-ttu-id="a129a-104">Преобразует значение в строку с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a129a-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="a129a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a129a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="a129a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a129a-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="a129a-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a129a-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="a129a-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="a129a-108">The converted value.</span></span>  
  
## <span data-ttu-id="a129a-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a129a-109">Return Value</span></span>  
 <span data-ttu-id="a129a-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="a129a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a129a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a129a-111">Remarks</span></span>  
 <span data-ttu-id="a129a-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="a129a-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a129a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a129a-113">Requirements</span></span>  
 <span data-ttu-id="a129a-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="a129a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a129a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a129a-115">See Also</span></span>  
 [<span data-ttu-id="a129a-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a129a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
