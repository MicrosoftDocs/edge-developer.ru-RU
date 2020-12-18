---
description: Удалите значение по указанному индексу объекта.
title: JsDeleteIndexedProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1340b0204d3845d4a9bd3f18a58ec125a82d2bc0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235649"
---
# <span data-ttu-id="1d2d8-103">Функция JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="1d2d8-103">JsDeleteIndexedProperty Function</span></span>

<span data-ttu-id="1d2d8-104">Удалите значение по указанному индексу объекта.</span><span class="sxs-lookup"><span data-stu-id="1d2d8-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="1d2d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d2d8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="1d2d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d2d8-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="1d2d8-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="1d2d8-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="1d2d8-108">Индекс, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="1d2d8-108">The index to delete.</span></span>  
  
## <span data-ttu-id="1d2d8-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="1d2d8-109">Return Value</span></span>  
 <span data-ttu-id="1d2d8-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="1d2d8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1d2d8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d2d8-111">Remarks</span></span>  
 <span data-ttu-id="1d2d8-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="1d2d8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="1d2d8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1d2d8-113">Requirements</span></span>  
 <span data-ttu-id="1d2d8-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="1d2d8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1d2d8-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1d2d8-115">See Also</span></span>  
 [<span data-ttu-id="1d2d8-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1d2d8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
