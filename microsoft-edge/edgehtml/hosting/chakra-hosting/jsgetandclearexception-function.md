---
description: Возвращает исключение, из-за чего время работы текущего контекста было в состоянии исключения, и сбрасывает состояние исключения для этой времени.
title: JsGetAndClearException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235428"
---
# <span data-ttu-id="61158-103">Функция JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="61158-103">JsGetAndClearException Function</span></span>

<span data-ttu-id="61158-104">Возвращает исключение, из-за чего время работы текущего контекста было в состоянии исключения, и сбрасывает состояние исключения для этой времени.</span><span class="sxs-lookup"><span data-stu-id="61158-104">Returns the exception that caused the runtime of the current context to be in the exception state and resets the exception state for that runtime.</span></span>  
  
## <span data-ttu-id="61158-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61158-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### <span data-ttu-id="61158-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61158-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="61158-107">Исключение для времени работы текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="61158-107">The exception for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="61158-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="61158-108">Return Value</span></span>  
 <span data-ttu-id="61158-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="61158-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="61158-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61158-110">Remarks</span></span>  
 <span data-ttu-id="61158-111">Если время работы текущего контекста находится не в состоянии исключения, этот API `JsErrorInvalidArgument` возвращается.</span><span class="sxs-lookup"><span data-stu-id="61158-111">If the runtime of the current context is not in an exception state, this API will return `JsErrorInvalidArgument`.</span></span> <span data-ttu-id="61158-112">Если время работы отключено, будет возвращено исключение, указывающее на то, что сценарий был завершен, но исключение не будет очищено (исключение будет очищено при повторном включаемом использовании). `JsEnableRuntimeExecution`</span><span class="sxs-lookup"><span data-stu-id="61158-112">If the runtime is disabled, this will return an exception indicating that the script was terminated, but it will not clear the exception (the exception will be cleared if the runtime is re-enabled using `JsEnableRuntimeExecution`).</span></span>  
  
 <span data-ttu-id="61158-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="61158-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="61158-114">Требования</span><span class="sxs-lookup"><span data-stu-id="61158-114">Requirements</span></span>  
 <span data-ttu-id="61158-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="61158-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="61158-116">См. также</span><span class="sxs-lookup"><span data-stu-id="61158-116">See Also</span></span>  
 [<span data-ttu-id="61158-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="61158-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
