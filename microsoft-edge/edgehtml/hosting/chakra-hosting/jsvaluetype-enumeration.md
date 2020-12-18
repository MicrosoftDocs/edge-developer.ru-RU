---
description: Тип JavaScript JsValueRef.
title: JsValueType Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235452"
---
# <span data-ttu-id="7a84c-103">Перечисление JsValueType</span><span class="sxs-lookup"><span data-stu-id="7a84c-103">JsValueType Enumeration</span></span>

<span data-ttu-id="7a84c-104">Тип JavaScript JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="7a84c-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="7a84c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a84c-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="7a84c-106">Members</span><span class="sxs-lookup"><span data-stu-id="7a84c-106">Members</span></span>  
  
### <span data-ttu-id="7a84c-107">Значения</span><span class="sxs-lookup"><span data-stu-id="7a84c-107">Values</span></span>  
  
|<span data-ttu-id="7a84c-108">Имя</span><span class="sxs-lookup"><span data-stu-id="7a84c-108">Name</span></span>|<span data-ttu-id="7a84c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7a84c-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="7a84c-110">Значением является `undefined` значение.</span><span class="sxs-lookup"><span data-stu-id="7a84c-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="7a84c-111">Значением является `null` значение.</span><span class="sxs-lookup"><span data-stu-id="7a84c-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="7a84c-112">Это значение является числом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="7a84c-113">Значением является строка JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="7a84c-114">Значением является значение JavaScript Boolean.</span><span class="sxs-lookup"><span data-stu-id="7a84c-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="7a84c-115">Значением является значение объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="7a84c-116">Значением является значение объекта функции JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="7a84c-117">Значением является значение объекта ошибки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="7a84c-118">Значением является значение объекта массива JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="7a84c-119">Значением является значение символа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="7a84c-120">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a84c-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="7a84c-121">Значением является значение объекта `ArrayBuffer` JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="7a84c-122">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a84c-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="7a84c-123">Это значение является значением объекта массива JavaScript, введите его.</span><span class="sxs-lookup"><span data-stu-id="7a84c-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="7a84c-124">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a84c-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="7a84c-125">Значением является значение объекта `DataView` JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a84c-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="7a84c-126">Это значение поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a84c-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="7a84c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7a84c-127">Requirements</span></span>  
 <span data-ttu-id="7a84c-128">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="7a84c-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7a84c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7a84c-129">See Also</span></span>  
 [<span data-ttu-id="7a84c-130">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7a84c-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
