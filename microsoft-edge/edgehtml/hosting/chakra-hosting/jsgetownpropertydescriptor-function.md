---
description: Получает дескриптор свойства для собственного свойства объекта.
title: JsGetOwnPropertyDescriptor Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyDescriptor
helpviewer_keywords:
- JsGetOwnPropertyDescriptor function
ms.assetid: 44c417ce-ab63-44eb-a0ab-19838e3ab34f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 05c7a58fa12d7ca8013c512f40031963ebc8ac18
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235499"
---
# <span data-ttu-id="321fd-103">Функция JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="321fd-103">JsGetOwnPropertyDescriptor Function</span></span>

<span data-ttu-id="321fd-104">Получает дескриптор свойства для собственного свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="321fd-104">Gets a property descriptor for an object's own property.</span></span>  
  
## <span data-ttu-id="321fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="321fd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyDescriptor(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *propertyDescriptor  
);  
```  
  
#### <span data-ttu-id="321fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="321fd-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="321fd-107">Объект, который имеет свойство.</span><span class="sxs-lookup"><span data-stu-id="321fd-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="321fd-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="321fd-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="321fd-109">Дескриптор свойства.</span><span class="sxs-lookup"><span data-stu-id="321fd-109">The property descriptor.</span></span>  
  
## <span data-ttu-id="321fd-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="321fd-110">Return Value</span></span>  
 <span data-ttu-id="321fd-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="321fd-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="321fd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="321fd-112">Remarks</span></span>  
 <span data-ttu-id="321fd-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="321fd-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="321fd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="321fd-114">Requirements</span></span>  
 <span data-ttu-id="321fd-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="321fd-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="321fd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="321fd-116">See Also</span></span>  
 [<span data-ttu-id="321fd-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="321fd-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
