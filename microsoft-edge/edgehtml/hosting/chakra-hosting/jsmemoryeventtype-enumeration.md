---
description: Тип события распределения событий для вызова вызова.
title: JsMemoryEventType Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235111"
---
# <span data-ttu-id="8682f-103">Перечисление JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="8682f-103">JsMemoryEventType Enumeration</span></span>

<span data-ttu-id="8682f-104">Тип события распределения событий для вызова вызова.</span><span class="sxs-lookup"><span data-stu-id="8682f-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="8682f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8682f-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="8682f-106">Members</span><span class="sxs-lookup"><span data-stu-id="8682f-106">Members</span></span>  
  
### <span data-ttu-id="8682f-107">Значения</span><span class="sxs-lookup"><span data-stu-id="8682f-107">Values</span></span>  
  
|<span data-ttu-id="8682f-108">Имя</span><span class="sxs-lookup"><span data-stu-id="8682f-108">Name</span></span>|<span data-ttu-id="8682f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8682f-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="8682f-110">Указывает запрос на выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="8682f-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="8682f-111">Указывает, что произошел сбой выделения.</span><span class="sxs-lookup"><span data-stu-id="8682f-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="8682f-112">Указывает на событие освободить память.</span><span class="sxs-lookup"><span data-stu-id="8682f-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="8682f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8682f-113">Requirements</span></span>  
 <span data-ttu-id="8682f-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="8682f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8682f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8682f-115">See Also</span></span>  
 [<span data-ttu-id="8682f-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8682f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
