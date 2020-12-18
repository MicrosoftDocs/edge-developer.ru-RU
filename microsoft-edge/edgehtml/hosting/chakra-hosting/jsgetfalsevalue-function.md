---
description: Получает значение в `false` текущем контексте сценария.
title: JsGetFalseValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetFalseValue
helpviewer_keywords:
- JsGetFalseValue function
ms.assetid: 621a584c-4ca8-4ba0-b19a-6cb50cf830b6
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c87ad969fc7547f4d650148005327fb93dce805d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235547"
---
# <span data-ttu-id="8f781-103">Функция JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="8f781-103">JsGetFalseValue Function</span></span>

<span data-ttu-id="8f781-104">Получает значение в `false` текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="8f781-104">Gets the value of `false` in the current script context.</span></span>  
  
## <span data-ttu-id="8f781-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f781-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetFalseValue(  
   _Out_ JsValueRef *falseValue  
);  
```  
  
#### <span data-ttu-id="8f781-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f781-106">Parameters</span></span>  
 `falseValue`  
 <span data-ttu-id="8f781-107">`false`Значение.</span><span class="sxs-lookup"><span data-stu-id="8f781-107">The `false` value.</span></span>  
  
## <span data-ttu-id="8f781-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="8f781-108">Return Value</span></span>  
 <span data-ttu-id="8f781-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="8f781-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8f781-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f781-110">Remarks</span></span>  
 <span data-ttu-id="8f781-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="8f781-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8f781-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8f781-112">Requirements</span></span>  
 <span data-ttu-id="8f781-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="8f781-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8f781-114">См. также</span><span class="sxs-lookup"><span data-stu-id="8f781-114">See Also</span></span>  
 [<span data-ttu-id="8f781-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8f781-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
