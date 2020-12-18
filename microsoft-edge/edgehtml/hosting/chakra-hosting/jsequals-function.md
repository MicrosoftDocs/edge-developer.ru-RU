---
description: Сравните два значения JavaScript для равенства.
title: JsEquals Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88f906419e73ed0de6ddde0a872becbd18908997
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235878"
---
# <span data-ttu-id="86958-103">Функция JsEquals</span><span class="sxs-lookup"><span data-stu-id="86958-103">JsEquals Function</span></span>

<span data-ttu-id="86958-104">Сравните два значения JavaScript для равенства.</span><span class="sxs-lookup"><span data-stu-id="86958-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="86958-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86958-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="86958-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86958-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="86958-107">Первый объект для сравнения.</span><span class="sxs-lookup"><span data-stu-id="86958-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="86958-108">Второй объект для сравнения.</span><span class="sxs-lookup"><span data-stu-id="86958-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="86958-109">Будут ли значения равными.</span><span class="sxs-lookup"><span data-stu-id="86958-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="86958-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="86958-110">Return Value</span></span>  
 <span data-ttu-id="86958-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="86958-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="86958-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86958-112">Remarks</span></span>  
 <span data-ttu-id="86958-113">Эта функция эквивалентна оператору `==` в Javascript.</span><span class="sxs-lookup"><span data-stu-id="86958-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="86958-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="86958-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="86958-115">Требования</span><span class="sxs-lookup"><span data-stu-id="86958-115">Requirements</span></span>  
 <span data-ttu-id="86958-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="86958-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="86958-117">См. также</span><span class="sxs-lookup"><span data-stu-id="86958-117">See Also</span></span>  
 [<span data-ttu-id="86958-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="86958-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
