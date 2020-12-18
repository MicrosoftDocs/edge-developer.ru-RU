---
description: Проверяет, имеет ли объект значение в указанном индексе.
title: JsHasIndexedProperty Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9eb1794c465b4b116978a2150285e2fed3ae1d9b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235515"
---
# <span data-ttu-id="f727f-103">Функция JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="f727f-103">JsHasIndexedProperty Function</span></span>

<span data-ttu-id="f727f-104">Проверяет, имеет ли объект значение в указанном индексе.</span><span class="sxs-lookup"><span data-stu-id="f727f-104">Tests whether an object has a value at the specified index.</span></span>  
  
## <span data-ttu-id="f727f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f727f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="f727f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f727f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="f727f-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="f727f-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="f727f-108">Тестовый индекс.</span><span class="sxs-lookup"><span data-stu-id="f727f-108">The index to test.</span></span>  
  
 `result`  
 <span data-ttu-id="f727f-109">Указывает, имеет ли объект значение в указанном индексе.</span><span class="sxs-lookup"><span data-stu-id="f727f-109">Whether the object has an value at the specified index.</span></span>  
  
## <span data-ttu-id="f727f-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f727f-110">Return Value</span></span>  
 <span data-ttu-id="f727f-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="f727f-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f727f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f727f-112">Remarks</span></span>  
 <span data-ttu-id="f727f-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="f727f-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f727f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f727f-114">Requirements</span></span>  
 <span data-ttu-id="f727f-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="f727f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f727f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f727f-116">See Also</span></span>  
 [<span data-ttu-id="f727f-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f727f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
