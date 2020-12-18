---
description: Извлекает `double` значение числимого значения.
title: JsNumberToDouble Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e4ae744f091045116a639aff619c475c7c7025f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235645"
---
# <span data-ttu-id="88bb9-103">Функция JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="88bb9-103">JsNumberToDouble Function</span></span>

<span data-ttu-id="88bb9-104">Извлекает `double` значение числимого значения.</span><span class="sxs-lookup"><span data-stu-id="88bb9-104">Retrieves the `double` value of a number value.</span></span>  
  
## <span data-ttu-id="88bb9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88bb9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### <span data-ttu-id="88bb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88bb9-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="88bb9-107">Число, преобразуемого в `double` значение.</span><span class="sxs-lookup"><span data-stu-id="88bb9-107">The number value to convert to a `double` value.</span></span>  
  
 `doubleValue`  
 <span data-ttu-id="88bb9-108">`double`Значение.</span><span class="sxs-lookup"><span data-stu-id="88bb9-108">The `double` value.</span></span>  
  
## <span data-ttu-id="88bb9-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="88bb9-109">Return Value</span></span>  
 <span data-ttu-id="88bb9-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="88bb9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="88bb9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88bb9-111">Remarks</span></span>  
 <span data-ttu-id="88bb9-112">Эта функция извлекает значение числа.</span><span class="sxs-lookup"><span data-stu-id="88bb9-112">This function retrieves the value of a number value.</span></span> <span data-ttu-id="88bb9-113">Он не будет `JsErrorInvalidArgument` работать, если тип значения не является числом.</span><span class="sxs-lookup"><span data-stu-id="88bb9-113">It will fail with `JsErrorInvalidArgument` if the type of the value is not number.</span></span>  
  
 <span data-ttu-id="88bb9-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="88bb9-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="88bb9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="88bb9-115">Requirements</span></span>  
 <span data-ttu-id="88bb9-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="88bb9-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="88bb9-117">См. также</span><span class="sxs-lookup"><span data-stu-id="88bb9-117">See Also</span></span>  
 [<span data-ttu-id="88bb9-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="88bb9-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
