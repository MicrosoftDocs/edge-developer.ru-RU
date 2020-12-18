---
description: Вызов фонового элемента работы.
title: JsBackgroundWorkItemCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235334"
---
# <span data-ttu-id="c8279-103">JsBackgroundWorkItemCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="c8279-103">JsBackgroundWorkItemCallback Typedef</span></span>

<span data-ttu-id="c8279-104">Вызов фонового элемента работы.</span><span class="sxs-lookup"><span data-stu-id="c8279-104">A background work item callback.</span></span>  
  
## <span data-ttu-id="c8279-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8279-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="c8279-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8279-106">Parameters</span></span>  
 <span data-ttu-id="c8279-107">callbackData</span><span class="sxs-lookup"><span data-stu-id="c8279-107">callbackData</span></span>  
 <span data-ttu-id="c8279-108">Аргумент данных, переданный в службу потоков.</span><span class="sxs-lookup"><span data-stu-id="c8279-108">Data argument passed to the thread service.</span></span>  
  
## <span data-ttu-id="c8279-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8279-109">Remarks</span></span>  
 <span data-ttu-id="c8279-110">Он передается в потоковую службу хоста (если она предоставляется), чтобы разрешить хосту вызывать вызов элемента работы в фоновом потоке по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="c8279-110">This is passed to the host's thread service (if provided) to allow the host to invoke the work item callback on the background thread of its choice.</span></span>  
  
## <span data-ttu-id="c8279-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c8279-111">Requirements</span></span>  
 <span data-ttu-id="c8279-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="c8279-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c8279-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c8279-113">See Also</span></span>  
 [<span data-ttu-id="c8279-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c8279-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
