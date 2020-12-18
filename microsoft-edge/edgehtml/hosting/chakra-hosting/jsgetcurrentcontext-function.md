---
description: Получает текущий контекст сценария в потоке.
title: JsGetCurrentContext Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a43b9a6d4413ef1dc1b66321d6078aef84a0645f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235554"
---
# <span data-ttu-id="19f79-103">Функция JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="19f79-103">JsGetCurrentContext Function</span></span>

<span data-ttu-id="19f79-104">Получает текущий контекст сценария в потоке.</span><span class="sxs-lookup"><span data-stu-id="19f79-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="19f79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19f79-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="19f79-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19f79-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="19f79-107">Текущий контекст сценария в потоке, null, если нет текущего контекста сценария.</span><span class="sxs-lookup"><span data-stu-id="19f79-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="19f79-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="19f79-108">Return Value</span></span>  
 <span data-ttu-id="19f79-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="19f79-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="19f79-110">Требования</span><span class="sxs-lookup"><span data-stu-id="19f79-110">Requirements</span></span>  
 <span data-ttu-id="19f79-111">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="19f79-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="19f79-112">См. также</span><span class="sxs-lookup"><span data-stu-id="19f79-112">See Also</span></span>  
 [<span data-ttu-id="19f79-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="19f79-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
