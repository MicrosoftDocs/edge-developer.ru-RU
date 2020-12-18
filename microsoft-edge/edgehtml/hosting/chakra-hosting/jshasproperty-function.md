---
description: Определяет, имеет ли объект свойство.
title: JsHasProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasProperty
helpviewer_keywords:
- JsHasProperty function
ms.assetid: 26c94c3d-aae6-4257-8644-df63c7e714fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e45ecfaafb06c49a6a3773eb798ee93a19fd6d6e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235513"
---
# <span data-ttu-id="bbd78-103">Функция JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="bbd78-103">JsHasProperty Function</span></span>

<span data-ttu-id="bbd78-104">Определяет, имеет ли объект свойство.</span><span class="sxs-lookup"><span data-stu-id="bbd78-104">Determines whether an object has a property.</span></span>  
  
## <span data-ttu-id="bbd78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbd78-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ bool *hasProperty  
);  
```  
  
#### <span data-ttu-id="bbd78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbd78-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bbd78-107">Объект, который может содержать свойство.</span><span class="sxs-lookup"><span data-stu-id="bbd78-107">The object that may contain the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="bbd78-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="bbd78-108">The ID of the property.</span></span>  
  
 `hasProperty`  
 <span data-ttu-id="bbd78-109">Имеет ли объект (или прототип) свойство.</span><span class="sxs-lookup"><span data-stu-id="bbd78-109">Whether the object (or a prototype) has the property.</span></span>  
  
## <span data-ttu-id="bbd78-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bbd78-110">Return Value</span></span>  
 <span data-ttu-id="bbd78-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="bbd78-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bbd78-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbd78-112">Remarks</span></span>  
 <span data-ttu-id="bbd78-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="bbd78-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bbd78-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bbd78-114">Requirements</span></span>  
 <span data-ttu-id="bbd78-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="bbd78-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bbd78-116">См. также</span><span class="sxs-lookup"><span data-stu-id="bbd78-116">See Also</span></span>  
 [<span data-ttu-id="bbd78-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bbd78-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
