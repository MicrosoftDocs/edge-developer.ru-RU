---
description: Определяет, находится ли время работы текущего контекста в состоянии исключения.
title: JsHasException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235169"
---
# <span data-ttu-id="456eb-103">Функция JsHasException</span><span class="sxs-lookup"><span data-stu-id="456eb-103">JsHasException Function</span></span>

<span data-ttu-id="456eb-104">Определяет, находится ли время работы текущего контекста в состоянии исключения.</span><span class="sxs-lookup"><span data-stu-id="456eb-104">Determines whether the runtime of the current context is in an exception state.</span></span>  
  
## <span data-ttu-id="456eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="456eb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### <span data-ttu-id="456eb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="456eb-106">Parameters</span></span>  
 `hasException`  
 <span data-ttu-id="456eb-107">Находится ли время запуска текущего контекста в состоянии исключения.</span><span class="sxs-lookup"><span data-stu-id="456eb-107">Whether the runtime of the current context is in the exception state.</span></span>  
  
## <span data-ttu-id="456eb-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="456eb-108">Return Value</span></span>  
 <span data-ttu-id="456eb-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="456eb-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="456eb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="456eb-110">Remarks</span></span>  
 <span data-ttu-id="456eb-111">Если вызов в окн. ок. приводит к исключению (в результате запуска сценария или из-за ошибки преобразования), то она переводит ее в "состояние исключения".</span><span class="sxs-lookup"><span data-stu-id="456eb-111">If a call into the runtime results in an exception (either as the result of running a script or due to something like a conversion failure), the runtime is placed into an "exception state."</span></span> <span data-ttu-id="456eb-112">Все вызовы в любом контексте, созданном в среде запуска (за исключением API-api исключений), будут неудались до тех пор, пока исключение не будет `JsErrorInExceptionState` очищено.</span><span class="sxs-lookup"><span data-stu-id="456eb-112">All calls into any context created by the runtime (except for the exception APIs) will fail with `JsErrorInExceptionState` until the exception is cleared.</span></span>  
  
 <span data-ttu-id="456eb-113">Если время работы текущего контекста находится в состоянии исключения при возвращении обратного вызова в обдвижку, обдвижок автоматически перезаписал исключение.</span><span class="sxs-lookup"><span data-stu-id="456eb-113">If the runtime of the current context is in the exception state when a callback returns into the engine, the engine will automatically rethrow the exception.</span></span>  
  
 <span data-ttu-id="456eb-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="456eb-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="456eb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="456eb-115">Requirements</span></span>  
 <span data-ttu-id="456eb-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="456eb-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="456eb-117">См. также</span><span class="sxs-lookup"><span data-stu-id="456eb-117">See Also</span></span>  
 [<span data-ttu-id="456eb-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="456eb-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
