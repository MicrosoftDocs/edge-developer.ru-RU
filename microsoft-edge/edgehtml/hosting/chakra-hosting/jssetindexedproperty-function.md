---
description: Установите значение в указанном индексе объекта.
title: JsSetIndexedProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1fa961750fa5db262e1512d8d26572280d5e726c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235283"
---
# <span data-ttu-id="a9d0e-103">Функция JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="a9d0e-103">JsSetIndexedProperty Function</span></span>

<span data-ttu-id="a9d0e-104">Установите значение в указанном индексе объекта.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="a9d0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9d0e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="a9d0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9d0e-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="a9d0e-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="a9d0e-108">Индекс, который необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="a9d0e-109">Значение, за который необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-109">The value to set.</span></span>  
  
## <span data-ttu-id="a9d0e-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a9d0e-110">Return Value</span></span>  
 <span data-ttu-id="a9d0e-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a9d0e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9d0e-112">Remarks</span></span>  
 <span data-ttu-id="a9d0e-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="a9d0e-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a9d0e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a9d0e-114">Requirements</span></span>  
 <span data-ttu-id="a9d0e-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="a9d0e-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a9d0e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a9d0e-116">See Also</span></span>  
 [<span data-ttu-id="a9d0e-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a9d0e-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
