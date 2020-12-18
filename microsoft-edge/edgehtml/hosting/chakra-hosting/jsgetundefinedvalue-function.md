---
description: Получает значение в `undefined` текущем контексте сценария.
title: JsGetUndefinedValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetUndefinedValue
helpviewer_keywords:
- JsGetUndefinedValue function
ms.assetid: e118eaf6-452c-42f2-86b8-e63c7d987cba
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34bfaec4548ee2b77d6d98749c3049bb8f679134
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235165"
---
# <span data-ttu-id="730d1-103">Функция JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="730d1-103">JsGetUndefinedValue Function</span></span>

<span data-ttu-id="730d1-104">Получает значение в `undefined` текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="730d1-104">Gets the value of `undefined` in the current script context.</span></span>  
  
## <span data-ttu-id="730d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="730d1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetUndefinedValue(  
   _Out_ JsValueRef *undefinedValue  
);  
```  
  
#### <span data-ttu-id="730d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="730d1-106">Parameters</span></span>  
 `undefinedValue`  
 <span data-ttu-id="730d1-107">`undefined`Значение.</span><span class="sxs-lookup"><span data-stu-id="730d1-107">The `undefined` value.</span></span>  
  
## <span data-ttu-id="730d1-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="730d1-108">Return Value</span></span>  
 <span data-ttu-id="730d1-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="730d1-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="730d1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="730d1-110">Remarks</span></span>  
 <span data-ttu-id="730d1-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="730d1-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="730d1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="730d1-112">Requirements</span></span>  
 <span data-ttu-id="730d1-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="730d1-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="730d1-114">См. также</span><span class="sxs-lookup"><span data-stu-id="730d1-114">See Also</span></span>  
 [<span data-ttu-id="730d1-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="730d1-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
