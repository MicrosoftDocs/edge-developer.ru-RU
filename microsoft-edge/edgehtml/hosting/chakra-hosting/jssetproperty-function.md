---
description: Помещает свойство объекта.
title: JsSetProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 29c3e04fc240bd63fc755c6727752d053b94484d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235514"
---
# <span data-ttu-id="84d01-103">Функция JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="84d01-103">JsSetProperty Function</span></span>

<span data-ttu-id="84d01-104">Помещает свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="84d01-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="84d01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84d01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="84d01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84d01-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="84d01-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="84d01-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="84d01-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="84d01-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="84d01-109">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="84d01-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="84d01-110">Набор свойств должен следовать строгим правилам режима.</span><span class="sxs-lookup"><span data-stu-id="84d01-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="84d01-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="84d01-111">Return Value</span></span>  
 <span data-ttu-id="84d01-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="84d01-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="84d01-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84d01-113">Remarks</span></span>  
 <span data-ttu-id="84d01-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="84d01-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="84d01-115">Требования</span><span class="sxs-lookup"><span data-stu-id="84d01-115">Requirements</span></span>  
 <span data-ttu-id="84d01-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="84d01-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="84d01-117">См. также</span><span class="sxs-lookup"><span data-stu-id="84d01-117">See Also</span></span>  
 [<span data-ttu-id="84d01-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="84d01-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
