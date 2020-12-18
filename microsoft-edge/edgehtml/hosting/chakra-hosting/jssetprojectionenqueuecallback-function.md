---
description: Задает обратное вызов, который будет использоваться для вызова завершения проекции для требуемого потока вызывающих.
title: JsSetProjectionEnqueueCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235285"
---
# <span data-ttu-id="9c549-103">Функция JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="9c549-103">JsSetProjectionEnqueueCallback Function</span></span>

<span data-ttu-id="9c549-104">Задает обратное вызов, который будет использоваться для вызова завершения проекции для требуемого потока вызывающих.</span><span class="sxs-lookup"><span data-stu-id="9c549-104">Sets the callback to be used in order to invoke a projection completion back to the callers required thread.</span></span>  
  
## <span data-ttu-id="9c549-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c549-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### <span data-ttu-id="9c549-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c549-106">Parameters</span></span>  
 `projectionEnqueueContext`  
 <span data-ttu-id="9c549-107">Вызов, который будет вызываться при завершении проекции в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="9c549-107">The callback that will be invoked any time a projection completion occurs on a background thread.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="9c549-108">Контекст приложения, предоставленный `projectionEnqueueContext` для .</span><span class="sxs-lookup"><span data-stu-id="9c549-108">The application context provided to `projectionEnqueueContext`.</span></span>  
  
## <span data-ttu-id="9c549-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9c549-109">Return Value</span></span>  
 <span data-ttu-id="9c549-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="9c549-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9c549-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c549-111">Remarks</span></span>  
 <span data-ttu-id="9c549-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="9c549-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9c549-113">Вызов должен быть исходя из другого com-или другого потока в той же MTA.</span><span class="sxs-lookup"><span data-stu-id="9c549-113">The call should be coming from a different COM apartment or from a different thread in the same MTA.</span></span>  
  
 <span data-ttu-id="9c549-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="9c549-114">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="9c549-115">PInvoke в настоящее время не поддерживается для этого API.</span><span class="sxs-lookup"><span data-stu-id="9c549-115">PInvoke is not currently supported for this API.</span></span>  
  
## <span data-ttu-id="9c549-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9c549-116">Requirements</span></span>  
 <span data-ttu-id="9c549-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="9c549-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9c549-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9c549-118">See Also</span></span>  
 [<span data-ttu-id="9c549-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9c549-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
