---
description: Пользователь реализовал процедуру вызова для событий выделения памяти.
title: JsMemoryAllocationCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235302"
---
# <span data-ttu-id="86ce3-103">JsMemoryAllocationCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="86ce3-103">JsMemoryAllocationCallback Typedef</span></span>

<span data-ttu-id="86ce3-104">Пользователь реализовал процедуру вызова для событий выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="86ce3-104">User implemented callback routine for memory allocation events.</span></span>  
  
## <span data-ttu-id="86ce3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86ce3-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### <span data-ttu-id="86ce3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="86ce3-106">Parameters</span></span>  
 <span data-ttu-id="86ce3-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="86ce3-107">callbackState</span></span>  
 <span data-ttu-id="86ce3-108">Состояние, переданное в JsSetRuntimeMemoryAllocationCallback.</span><span class="sxs-lookup"><span data-stu-id="86ce3-108">The state passed to JsSetRuntimeMemoryAllocationCallback.</span></span>  
  
 <span data-ttu-id="86ce3-109">allocationEvent</span><span class="sxs-lookup"><span data-stu-id="86ce3-109">allocationEvent</span></span>  
 <span data-ttu-id="86ce3-110">Тип события выделения типов.</span><span class="sxs-lookup"><span data-stu-id="86ce3-110">The type of type allocation event.</span></span>  
  
 <span data-ttu-id="86ce3-111">allocationSize</span><span class="sxs-lookup"><span data-stu-id="86ce3-111">allocationSize</span></span>  
 <span data-ttu-id="86ce3-112">Размер выделения.</span><span class="sxs-lookup"><span data-stu-id="86ce3-112">The size of the allocation.</span></span>  
  
## <span data-ttu-id="86ce3-113">Значение свойства или возвращаемая величина</span><span class="sxs-lookup"><span data-stu-id="86ce3-113">Property Value/Return Value</span></span>  
 <span data-ttu-id="86ce3-114">Для события JsMemoryAllocate возврат true позволяет времени работы продолжить выделение.</span><span class="sxs-lookup"><span data-stu-id="86ce3-114">For the JsMemoryAllocate event, returning true allows the runtime to continue with allocation.</span></span> <span data-ttu-id="86ce3-115">Возврат false означает, что запрос на выделение отклонен.</span><span class="sxs-lookup"><span data-stu-id="86ce3-115">Returning false indicates the allocation request is rejected.</span></span> <span data-ttu-id="86ce3-116">Возвращаемая величина игнорируется для других событий выделения.</span><span class="sxs-lookup"><span data-stu-id="86ce3-116">The return value is ignored for other allocation events.</span></span>  
  
## <span data-ttu-id="86ce3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86ce3-117">Remarks</span></span>  
 <span data-ttu-id="86ce3-118">Используйте JsSetRuntimeMemoryAllocationCallback для регистрации этого вызова.</span><span class="sxs-lookup"><span data-stu-id="86ce3-118">Use JsSetRuntimeMemoryAllocationCallback to register this callback.</span></span>  
  
## <span data-ttu-id="86ce3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="86ce3-119">Requirements</span></span>  
 <span data-ttu-id="86ce3-120">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="86ce3-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="86ce3-121">См. также</span><span class="sxs-lookup"><span data-stu-id="86ce3-121">See Also</span></span>  
 [<span data-ttu-id="86ce3-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="86ce3-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
