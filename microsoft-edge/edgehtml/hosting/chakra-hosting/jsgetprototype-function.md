---
description: Возвращает прототип объекта.
title: JsGetPrototype Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPrototype
helpviewer_keywords:
- JsGetPrototype function
ms.assetid: 05d743fc-103e-4a92-86f2-a063f39a2a6f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d64e8b090753e5d0627f0d40ee8745eeadd65227
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235801"
---
# <span data-ttu-id="30f12-103">Функция JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="30f12-103">JsGetPrototype Function</span></span>

<span data-ttu-id="30f12-104">Возвращает прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="30f12-104">Returns the prototype of an object.</span></span>  
  
## <span data-ttu-id="30f12-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30f12-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPrototype(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *prototypeObject  
);  
```  
  
#### <span data-ttu-id="30f12-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30f12-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="30f12-107">Объект, прототип которого должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="30f12-107">The object whose prototype is to be returned.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="30f12-108">Прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="30f12-108">The object's prototype.</span></span>  
  
## <span data-ttu-id="30f12-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="30f12-109">Return Value</span></span>  
 <span data-ttu-id="30f12-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="30f12-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="30f12-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30f12-111">Remarks</span></span>  
 <span data-ttu-id="30f12-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="30f12-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="30f12-113">Требования</span><span class="sxs-lookup"><span data-stu-id="30f12-113">Requirements</span></span>  
 <span data-ttu-id="30f12-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="30f12-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="30f12-115">См. также</span><span class="sxs-lookup"><span data-stu-id="30f12-115">See Also</span></span>  
 [<span data-ttu-id="30f12-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="30f12-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
