---
description: Начинает профилирование в текущем контексте.
title: JsStartProfiling Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartProfiling
helpviewer_keywords:
- JsStartProfiling function
ms.assetid: 638da395-42dd-4fc5-b581-819e647e887d
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 332ff04a987e6e7ae5030983af96dd48249e58e2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235494"
---
# <span data-ttu-id="278f2-103">Функция JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="278f2-103">JsStartProfiling Function</span></span>

<span data-ttu-id="278f2-104">Начинает профилирование в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="278f2-104">Starts profiling in the current context.</span></span>  
  
## <span data-ttu-id="278f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="278f2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStartProfiling(  
   _In_ IActiveScriptProfilerCallback *callback,  
   _In_ PROFILER_EVENT_MASK eventMask,  
   _In_ unsigned long context  
);  
```  
  
#### <span data-ttu-id="278f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="278f2-106">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="278f2-107">Вызов профилии, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="278f2-107">The profiling callback to use.</span></span>  
  
 `eventMask`  
 <span data-ttu-id="278f2-108">События профилирование для перена вызываемого вызова.</span><span class="sxs-lookup"><span data-stu-id="278f2-108">The profiling events to callback with.</span></span>  
  
 `context`  
 <span data-ttu-id="278f2-109">Контекст, который необходимо передать в вызов профилии.</span><span class="sxs-lookup"><span data-stu-id="278f2-109">A context to pass to the profiling callback.</span></span>  
  
## <span data-ttu-id="278f2-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="278f2-110">Return Value</span></span>  
 <span data-ttu-id="278f2-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="278f2-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="278f2-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="278f2-112">Remarks</span></span>  
 <span data-ttu-id="278f2-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="278f2-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="278f2-114">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="278f2-114">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="278f2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="278f2-115">Requirements</span></span>  
 <span data-ttu-id="278f2-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="278f2-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="278f2-117">См. также</span><span class="sxs-lookup"><span data-stu-id="278f2-117">See Also</span></span>  
 [<span data-ttu-id="278f2-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="278f2-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
