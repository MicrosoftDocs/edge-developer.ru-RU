---
description: Вызывает функцию в качестве конструктора.
title: JsConstructObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8dbb757456412e50efaf3a026d169e6b3612b6b1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235317"
---
# <span data-ttu-id="39151-103">Функция JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="39151-103">JsConstructObject Function</span></span>

<span data-ttu-id="39151-104">Вызывает функцию в качестве конструктора.</span><span class="sxs-lookup"><span data-stu-id="39151-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="39151-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39151-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="39151-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39151-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="39151-107">Функция, вызываемая в качестве конструктора.</span><span class="sxs-lookup"><span data-stu-id="39151-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="39151-108">Аргументы вызова.</span><span class="sxs-lookup"><span data-stu-id="39151-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="39151-109">Количество аргументов, которые передаются в функцию.</span><span class="sxs-lookup"><span data-stu-id="39151-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="39151-110">Значение, возвращаемая вызовом функции.</span><span class="sxs-lookup"><span data-stu-id="39151-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="39151-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="39151-111">Return Value</span></span>  
 <span data-ttu-id="39151-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="39151-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="39151-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39151-113">Remarks</span></span>  
 <span data-ttu-id="39151-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="39151-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="39151-115">Требования</span><span class="sxs-lookup"><span data-stu-id="39151-115">Requirements</span></span>  
 <span data-ttu-id="39151-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="39151-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="39151-117">См. также</span><span class="sxs-lookup"><span data-stu-id="39151-117">See Also</span></span>  
 [<span data-ttu-id="39151-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="39151-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
