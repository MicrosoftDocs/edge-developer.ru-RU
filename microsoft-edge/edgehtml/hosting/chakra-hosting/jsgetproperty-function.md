---
description: Получает свойство объекта.
title: JsGetProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetProperty
helpviewer_keywords:
- JsGetProperty function
ms.assetid: 606bc14f-e849-4f88-a148-6660e923c07b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e5731fa3f889fc1b182f88e37ae90c96d3825402
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235108"
---
# <span data-ttu-id="902bb-103">Функция JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="902bb-103">JsGetProperty Function</span></span>

<span data-ttu-id="902bb-104">Получает свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="902bb-104">Gets an object's property.</span></span>  
  
## <span data-ttu-id="902bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="902bb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="902bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="902bb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="902bb-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="902bb-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="902bb-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="902bb-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="902bb-109">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="902bb-109">The value of the property.</span></span>  
  
## <span data-ttu-id="902bb-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="902bb-110">Return Value</span></span>  
 <span data-ttu-id="902bb-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="902bb-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="902bb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="902bb-112">Remarks</span></span>  
 <span data-ttu-id="902bb-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="902bb-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="902bb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="902bb-114">Requirements</span></span>  
 <span data-ttu-id="902bb-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="902bb-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="902bb-116">См. также</span><span class="sxs-lookup"><span data-stu-id="902bb-116">See Also</span></span>  
 [<span data-ttu-id="902bb-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="902bb-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
