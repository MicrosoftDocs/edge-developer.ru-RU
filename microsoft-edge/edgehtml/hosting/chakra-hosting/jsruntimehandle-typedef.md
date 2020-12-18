---
description: Handle to a Chakra runtime.
title: JsRuntimeHandle Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235287"
---
# <span data-ttu-id="e8c55-103">JsRuntimeHandle Typedef</span><span class="sxs-lookup"><span data-stu-id="e8c55-103">JsRuntimeHandle Typedef</span></span>

<span data-ttu-id="e8c55-104">Handle to a Chakra runtime.</span><span class="sxs-lookup"><span data-stu-id="e8c55-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="e8c55-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8c55-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="e8c55-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8c55-106">Remarks</span></span>  
 <span data-ttu-id="e8c55-107">У каждой реализации Chakra есть собственный независимый механизм выполнения, компилятор JIT и куч, собираемая мусора.</span><span class="sxs-lookup"><span data-stu-id="e8c55-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="e8c55-108">Поэтому каждая из них полностью изолирована от других.</span><span class="sxs-lookup"><span data-stu-id="e8c55-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="e8c55-109">Times can be used on any thread, but only one thread can call into a runtime at any time.</span><span class="sxs-lookup"><span data-stu-id="e8c55-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="e8c55-110">JsRuntimeHandle, в отличие от других ссылок на объекты в API размещения Chakra, не является сборщиком мусора, так как содержит сам по себе собранный мусора.</span><span class="sxs-lookup"><span data-stu-id="e8c55-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="e8c55-111">Время работы будет существовать до тех пор, пока не будет вызвана JsDisposeRuntime.</span><span class="sxs-lookup"><span data-stu-id="e8c55-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="e8c55-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c55-112">Requirements</span></span>  
 <span data-ttu-id="e8c55-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e8c55-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e8c55-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e8c55-114">See Also</span></span>  
 [<span data-ttu-id="e8c55-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e8c55-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
