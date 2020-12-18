---
description: Получает значение в `true` текущем контексте сценария.
title: JsGetTrueValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetTrueValue
helpviewer_keywords:
- JsGetTrueValue function
ms.assetid: c2a56d48-344b-492b-90b8-f570710f8310
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58798e1e8aab57d626be0c8c878f9be39d0af942
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235867"
---
# <span data-ttu-id="3a580-103">Функция JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="3a580-103">JsGetTrueValue Function</span></span>

<span data-ttu-id="3a580-104">Получает значение в `true` текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="3a580-104">Gets the value of `true` in the current script context.</span></span>  
  
## <span data-ttu-id="3a580-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a580-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTrueValue(  
   _Out_ JsValueRef *trueValue  
);  
```  
  
#### <span data-ttu-id="3a580-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a580-106">Parameters</span></span>  
 `trueValue`  
 <span data-ttu-id="3a580-107">`true`Значение.</span><span class="sxs-lookup"><span data-stu-id="3a580-107">The `true` value.</span></span>  
  
## <span data-ttu-id="3a580-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3a580-108">Return Value</span></span>  
 <span data-ttu-id="3a580-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3a580-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3a580-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a580-110">Remarks</span></span>  
 <span data-ttu-id="3a580-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="3a580-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3a580-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3a580-112">Requirements</span></span>  
 <span data-ttu-id="3a580-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3a580-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3a580-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3a580-114">See Also</span></span>  
 [<span data-ttu-id="3a580-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3a580-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
