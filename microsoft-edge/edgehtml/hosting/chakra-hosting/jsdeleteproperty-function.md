---
description: Удаляет свойство объекта.
title: JsDeleteProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235135"
---
# <span data-ttu-id="377b4-103">Функция JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="377b4-103">JsDeleteProperty Function</span></span>

<span data-ttu-id="377b4-104">Удаляет свойство объекта.</span><span class="sxs-lookup"><span data-stu-id="377b4-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="377b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="377b4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="377b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="377b4-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="377b4-107">Объект, содержащий свойство.</span><span class="sxs-lookup"><span data-stu-id="377b4-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="377b4-108">ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="377b4-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="377b4-109">Набор свойств должен следовать строгим правилам режима.</span><span class="sxs-lookup"><span data-stu-id="377b4-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="377b4-110">Было ли удалено свойство.</span><span class="sxs-lookup"><span data-stu-id="377b4-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="377b4-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="377b4-111">Return Value</span></span>  
 <span data-ttu-id="377b4-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="377b4-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="377b4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="377b4-113">Remarks</span></span>  
 <span data-ttu-id="377b4-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="377b4-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="377b4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="377b4-115">Requirements</span></span>  
 <span data-ttu-id="377b4-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="377b4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="377b4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="377b4-117">See Also</span></span>  
 [<span data-ttu-id="377b4-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="377b4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
