---
description: Создает объект массива с типом JavaScript.
title: JsCreateTypedArray Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62f62296d81dafe6515f69a990e33ff5c00730e1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235656"
---
# <span data-ttu-id="72ec4-103">Функция JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="72ec4-103">JsCreateTypedArray Function</span></span>

<span data-ttu-id="72ec4-104">Создает объект массива с типом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="72ec4-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="72ec4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72ec4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="72ec4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72ec4-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="72ec4-107">Тип создаемого массива.</span><span class="sxs-lookup"><span data-stu-id="72ec4-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="72ec4-108">Базовый массив нового массива.</span><span class="sxs-lookup"><span data-stu-id="72ec4-108">The base array of the new array.</span></span> <span data-ttu-id="72ec4-109">Используйте, `JS_INVALID_REFERENCE` если базовый массив не используется.</span><span class="sxs-lookup"><span data-stu-id="72ec4-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="72ec4-110">Смещение в ветвях от начала () для `baseArray` `ArrayBuffer` массива результатов, на который требуется ссылаться.</span><span class="sxs-lookup"><span data-stu-id="72ec4-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="72ec4-111">Применимо только в `baseArray` том случае, если объект `ArrayBuffer` является объектом.</span><span class="sxs-lookup"><span data-stu-id="72ec4-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="72ec4-112">В противном случае должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="72ec4-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="72ec4-113">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="72ec4-113">The number of elements in the array.</span></span> <span data-ttu-id="72ec4-114">Применимо только при создании нового типтного массива без `baseArray` ( `baseArray` `JS_INVALID_REFERENCE` есть) или когда `baseArray` является `ArrayBuffer` объектом.</span><span class="sxs-lookup"><span data-stu-id="72ec4-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="72ec4-115">В противном случае должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="72ec4-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="72ec4-116">Новый типный объект массива.</span><span class="sxs-lookup"><span data-stu-id="72ec4-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="72ec4-117">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="72ec4-117">Return Value</span></span>  
 <span data-ttu-id="72ec4-118">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="72ec4-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72ec4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72ec4-119">Remarks</span></span>  
 <span data-ttu-id="72ec4-120">Это `baseArray` может быть другой `ArrayBuffer` типный массив или JavaScript. `Array`</span><span class="sxs-lookup"><span data-stu-id="72ec4-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="72ec4-121">Возвращенный типный массив будет использовать массив, если он является или иным образом создает и использует копию массива `baseArray` `ArrayBuffer` исходных источников.</span><span class="sxs-lookup"><span data-stu-id="72ec4-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="72ec4-122">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="72ec4-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="72ec4-123">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="72ec4-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="72ec4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="72ec4-124">Requirements</span></span>  
 <span data-ttu-id="72ec4-125">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="72ec4-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72ec4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="72ec4-126">See Also</span></span>  
 [<span data-ttu-id="72ec4-127">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72ec4-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
