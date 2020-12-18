---
description: Утилизирует дневный запуск.
title: JsDisposeRuntime Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235506"
---
# <span data-ttu-id="dd34a-103">Функция JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="dd34a-103">JsDisposeRuntime Function</span></span>

<span data-ttu-id="dd34a-104">Утилизирует дневный запуск.</span><span class="sxs-lookup"><span data-stu-id="dd34a-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="dd34a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd34a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="dd34a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd34a-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="dd34a-107">Время запуска, который необходимо утилизировать.</span><span class="sxs-lookup"><span data-stu-id="dd34a-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="dd34a-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="dd34a-108">Return Value</span></span>  
 <span data-ttu-id="dd34a-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="dd34a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dd34a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd34a-110">Remarks</span></span>  
 <span data-ttu-id="dd34a-111">После этого все ресурсы, которые она владеет, являются недопустимыми и не могут использоваться.</span><span class="sxs-lookup"><span data-stu-id="dd34a-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="dd34a-112">Если время работы активно (то есть установлено в текущем состоянии в определенном потоке), его нельзя удалять.</span><span class="sxs-lookup"><span data-stu-id="dd34a-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="dd34a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dd34a-113">Requirements</span></span>  
 <span data-ttu-id="dd34a-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="dd34a-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd34a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="dd34a-115">See Also</span></span>  
 [<span data-ttu-id="dd34a-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dd34a-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
