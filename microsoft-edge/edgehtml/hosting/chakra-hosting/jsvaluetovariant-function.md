---
description: Инициализирует переданный в качестве `VARIANT` проекции значения JavaScript.
title: JsValueToVariant Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235454"
---
# <span data-ttu-id="19f93-103">Функция JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="19f93-103">JsValueToVariant Function</span></span>

<span data-ttu-id="19f93-104">Инициализирует переданный в качестве `VARIANT` проекции значения JavaScript.</span><span class="sxs-lookup"><span data-stu-id="19f93-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="19f93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19f93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="19f93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="19f93-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="19f93-107">Значение JavaScript для проекта в качестве `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="19f93-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="19f93-108">Указатель на `VARIANT` структуру, которая инициализируются как проекция.</span><span class="sxs-lookup"><span data-stu-id="19f93-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="19f93-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="19f93-109">Return Value</span></span>  
  
## <span data-ttu-id="19f93-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19f93-110">Remarks</span></span>  
 <span data-ttu-id="19f93-111">Проекция `VARIANT` может использоваться клиентами автоматизации COM для вызова проецируемых объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="19f93-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="19f93-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="19f93-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="19f93-113">Требования</span><span class="sxs-lookup"><span data-stu-id="19f93-113">Requirements</span></span>  
 <span data-ttu-id="19f93-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="19f93-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="19f93-115">См. также</span><span class="sxs-lookup"><span data-stu-id="19f93-115">See Also</span></span>  
 [<span data-ttu-id="19f93-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="19f93-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
