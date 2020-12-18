---
description: Извлекает значение по указанному индексу объекта.
title: JsGetIndexedProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bd0246464d00884ca71fd8d3564ce775415f6267
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235132"
---
# <span data-ttu-id="3c9e3-103">Функция JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="3c9e3-103">JsGetIndexedProperty Function</span></span>

<span data-ttu-id="3c9e3-104">Извлекает значение по указанному индексу объекта.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="3c9e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c9e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="3c9e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c9e3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3c9e3-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="3c9e3-108">Индекс, который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="3c9e3-109">Полученные значения.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="3c9e3-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3c9e3-110">Return Value</span></span>  
 <span data-ttu-id="3c9e3-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3c9e3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c9e3-112">Remarks</span></span>  
 <span data-ttu-id="3c9e3-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="3c9e3-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3c9e3-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3c9e3-114">Requirements</span></span>  
 <span data-ttu-id="3c9e3-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3c9e3-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3c9e3-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3c9e3-116">See Also</span></span>  
 [<span data-ttu-id="3c9e3-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3c9e3-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
