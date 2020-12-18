---
description: Сравните два значения JavaScript для строгой равенства.
title: JsStrictEquals Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 98af1629129986cc21cafe5660d3155e031919dc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235461"
---
# <span data-ttu-id="63014-103">Функция JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="63014-103">JsStrictEquals Function</span></span>

<span data-ttu-id="63014-104">Сравните два значения JavaScript для строгой равенства.</span><span class="sxs-lookup"><span data-stu-id="63014-104">Compare two JavaScript values for strict equality.</span></span>  
  
## <span data-ttu-id="63014-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63014-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="63014-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63014-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="63014-107">Первый объект для сравнения.</span><span class="sxs-lookup"><span data-stu-id="63014-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="63014-108">Второй объект для сравнения.</span><span class="sxs-lookup"><span data-stu-id="63014-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="63014-109">Являются ли значения строго равными.</span><span class="sxs-lookup"><span data-stu-id="63014-109">Whether the values are strictly equal.</span></span>  
  
## <span data-ttu-id="63014-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="63014-110">Return Value</span></span>  
 <span data-ttu-id="63014-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="63014-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="63014-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63014-112">Remarks</span></span>  
 <span data-ttu-id="63014-113">Эта функция эквивалентна оператору `===` в Javascript.</span><span class="sxs-lookup"><span data-stu-id="63014-113">This function is equivalent to the `===` operator in Javascript.</span></span>  
  
 <span data-ttu-id="63014-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="63014-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="63014-115">Требования</span><span class="sxs-lookup"><span data-stu-id="63014-115">Requirements</span></span>  
 <span data-ttu-id="63014-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="63014-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="63014-117">См. также</span><span class="sxs-lookup"><span data-stu-id="63014-117">See Also</span></span>  
 [<span data-ttu-id="63014-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="63014-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
