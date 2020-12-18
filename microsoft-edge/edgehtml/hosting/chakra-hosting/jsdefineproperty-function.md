---
description: Определяет собственное свойство нового объекта из дескриптора свойства.
title: JsDefineProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a35dd6214190fa558c50cbb743b0f2b92b5e00b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235652"
---
# <span data-ttu-id="ffef6-103">Функция JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="ffef6-103">JsDefineProperty Function</span></span>

<span data-ttu-id="ffef6-104">Определяет собственное свойство нового объекта из дескриптора свойства.</span><span class="sxs-lookup"><span data-stu-id="ffef6-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="ffef6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffef6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="ffef6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffef6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ffef6-107">Объект, который имеет свойство.</span><span class="sxs-lookup"><span data-stu-id="ffef6-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="ffef6-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="ffef6-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="ffef6-109">Дескриптор свойства.</span><span class="sxs-lookup"><span data-stu-id="ffef6-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="ffef6-110">Определяется ли свойство.</span><span class="sxs-lookup"><span data-stu-id="ffef6-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="ffef6-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ffef6-111">Return Value</span></span>  
 <span data-ttu-id="ffef6-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ffef6-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ffef6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffef6-113">Remarks</span></span>  
 <span data-ttu-id="ffef6-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ffef6-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ffef6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ffef6-115">Requirements</span></span>  
 <span data-ttu-id="ffef6-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ffef6-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ffef6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ffef6-117">See Also</span></span>  
 [<span data-ttu-id="ffef6-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ffef6-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
