---
description: Преобразует значение в число с помощью стандартной семантики JavaScript.
title: JsConvertValueToNumber Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToNumber
helpviewer_keywords:
- JsConvertValueToNumber function
ms.assetid: c47b8653-0591-4863-b8b5-33187b315816
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8d00950ef3835c6d75f8f55ffe5002b32c6ee160
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235324"
---
# <span data-ttu-id="64ee8-103">Функция JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="64ee8-103">JsConvertValueToNumber Function</span></span>

<span data-ttu-id="64ee8-104">Преобразует значение в число с помощью стандартной семантики JavaScript.</span><span class="sxs-lookup"><span data-stu-id="64ee8-104">Converts the value to number using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="64ee8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64ee8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToNumber(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *numberValue  
);  
```  
  
#### <span data-ttu-id="64ee8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64ee8-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="64ee8-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="64ee8-107">The value to be converted.</span></span>  
  
 `numberValue`  
 <span data-ttu-id="64ee8-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="64ee8-108">The converted value.</span></span>  
  
## <span data-ttu-id="64ee8-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="64ee8-109">Return Value</span></span>  
 <span data-ttu-id="64ee8-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="64ee8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="64ee8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64ee8-111">Remarks</span></span>  
 <span data-ttu-id="64ee8-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="64ee8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="64ee8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="64ee8-113">Requirements</span></span>  
 <span data-ttu-id="64ee8-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="64ee8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="64ee8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="64ee8-115">See Also</span></span>  
 [<span data-ttu-id="64ee8-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="64ee8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
