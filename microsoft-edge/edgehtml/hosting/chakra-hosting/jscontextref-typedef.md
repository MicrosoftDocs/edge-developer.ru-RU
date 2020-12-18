---
description: Ссылка на контекст сценария.
title: JsContextRef Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235323"
---
# <span data-ttu-id="91317-103">JsContextRef Typedef</span><span class="sxs-lookup"><span data-stu-id="91317-103">JsContextRef Typedef</span></span>

<span data-ttu-id="91317-104">Ссылка на контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="91317-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="91317-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91317-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="91317-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91317-106">Remarks</span></span>  
 <span data-ttu-id="91317-107">Каждый контекст сценария содержит собственный глобальный объект, который отличается от глобального объекта в других контекстах сценария.</span><span class="sxs-lookup"><span data-stu-id="91317-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="91317-108">Для многих API размещения chakra требуется контекст активного сценария, который можно настроить с помощью `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="91317-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="91317-109">При размещении API-api-akra, для которых требуется установить текущий контекст, обратите внимание, что в документации явно это помечается.</span><span class="sxs-lookup"><span data-stu-id="91317-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="91317-110">Требования</span><span class="sxs-lookup"><span data-stu-id="91317-110">Requirements</span></span>  
 <span data-ttu-id="91317-111">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="91317-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="91317-112">См. также</span><span class="sxs-lookup"><span data-stu-id="91317-112">See Also</span></span>  
 [<span data-ttu-id="91317-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="91317-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
