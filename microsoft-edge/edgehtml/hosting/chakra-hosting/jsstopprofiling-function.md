---
description: Останавливает профилирование в текущем контексте.
title: JsStopProfiling Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235495"
---
# <span data-ttu-id="9c26f-103">Функция JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="9c26f-103">JsStopProfiling Function</span></span>

<span data-ttu-id="9c26f-104">Останавливает профилирование в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="9c26f-104">Stops profiling in the current context.</span></span>  
  
## <span data-ttu-id="9c26f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c26f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### <span data-ttu-id="9c26f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c26f-106">Parameters</span></span>  
 `reason`  
 <span data-ttu-id="9c26f-107">Причина остановки профилирование, передав его в вызов профиля.</span><span class="sxs-lookup"><span data-stu-id="9c26f-107">The reason for stopping profiling to pass to the profiler callback.</span></span>  
  
## <span data-ttu-id="9c26f-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9c26f-108">Return Value</span></span>  
 <span data-ttu-id="9c26f-109">Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="9c26f-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c26f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c26f-110">Remarks</span></span>  
 <span data-ttu-id="9c26f-111">Не возвращает ошибку, если профилирование не запущено.</span><span class="sxs-lookup"><span data-stu-id="9c26f-111">Will not return an error if profiling has not started.</span></span>  
  
 <span data-ttu-id="9c26f-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="9c26f-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9c26f-113">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="9c26f-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="9c26f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9c26f-114">Requirements</span></span>  
 <span data-ttu-id="9c26f-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="9c26f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c26f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9c26f-116">See Also</span></span>  
 [<span data-ttu-id="9c26f-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9c26f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
