---
description: Получает значение в `null` текущем контексте сценария.
title: JsGetNullValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetNullValue
helpviewer_keywords:
- JsGetNullValue function
ms.assetid: 132a1496-8dfe-4d3c-a8f8-389f5b0b50d2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 31e1ba19f9f27e75f0166238d98390e2c4a26c24
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235131"
---
# <span data-ttu-id="eda68-103">Функция JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="eda68-103">JsGetNullValue Function</span></span>

<span data-ttu-id="eda68-104">Получает значение в `null` текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="eda68-104">Gets the value of `null` in the current script context.</span></span>  
  
## <span data-ttu-id="eda68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eda68-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetNullValue(  
   _Out_ JsValueRef *nullValue  
);  
```  
  
#### <span data-ttu-id="eda68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eda68-106">Parameters</span></span>  
 `nullValue`  
 <span data-ttu-id="eda68-107">`null`Значение.</span><span class="sxs-lookup"><span data-stu-id="eda68-107">The `null` value.</span></span>  
  
## <span data-ttu-id="eda68-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="eda68-108">Return Value</span></span>  
 <span data-ttu-id="eda68-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="eda68-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eda68-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eda68-110">Remarks</span></span>  
 <span data-ttu-id="eda68-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="eda68-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eda68-112">Требования</span><span class="sxs-lookup"><span data-stu-id="eda68-112">Requirements</span></span>  
 <span data-ttu-id="eda68-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="eda68-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eda68-114">См. также</span><span class="sxs-lookup"><span data-stu-id="eda68-114">See Also</span></span>  
 [<span data-ttu-id="eda68-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eda68-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
