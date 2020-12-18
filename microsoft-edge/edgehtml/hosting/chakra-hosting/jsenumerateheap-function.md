---
description: Enumerates the heap of the current context.
title: JsEnumerateHeap Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235651"
---
# <span data-ttu-id="218ce-103">Функция JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="218ce-103">JsEnumerateHeap Function</span></span>

<span data-ttu-id="218ce-104">Enumerates the heap of the current context.</span><span class="sxs-lookup"><span data-stu-id="218ce-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="218ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="218ce-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="218ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="218ce-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="218ce-107">The heap enumerator.</span><span class="sxs-lookup"><span data-stu-id="218ce-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="218ce-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="218ce-108">Return Value</span></span>  
 <span data-ttu-id="218ce-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="218ce-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="218ce-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="218ce-110">Remarks</span></span>  
 <span data-ttu-id="218ce-111">Во время перезаписи кучи текущий контекст удалить невозможно, а все вызовы для изменения состояния контекста будут неуспешными до тех пор, пока не будет отпущено нумератор кучи.</span><span class="sxs-lookup"><span data-stu-id="218ce-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="218ce-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="218ce-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="218ce-113">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="218ce-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="218ce-114">Требования</span><span class="sxs-lookup"><span data-stu-id="218ce-114">Requirements</span></span>  
 <span data-ttu-id="218ce-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="218ce-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="218ce-116">См. также</span><span class="sxs-lookup"><span data-stu-id="218ce-116">See Also</span></span>  
 [<span data-ttu-id="218ce-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="218ce-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
