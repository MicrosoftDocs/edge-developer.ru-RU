---
description: Получает хранилище памяти, используемого типтным массивом.
title: JsGetTypedArrayStorage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235166"
---
# <span data-ttu-id="a476c-103">Функция JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="a476c-103">JsGetTypedArrayStorage Function</span></span>

<span data-ttu-id="a476c-104">Получает хранилище памяти, используемого типтным массивом.</span><span class="sxs-lookup"><span data-stu-id="a476c-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="a476c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a476c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="a476c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a476c-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="a476c-107">Типный экземпляр массива.</span><span class="sxs-lookup"><span data-stu-id="a476c-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="a476c-108">Буфер массива.</span><span class="sxs-lookup"><span data-stu-id="a476c-108">The array's buffer.</span></span> <span data-ttu-id="a476c-109">Время жизни возвращаемого буфера такое же, как и время жизни массива.</span><span class="sxs-lookup"><span data-stu-id="a476c-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="a476c-110">Указатель буфера не считается ссылкой на массив для сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="a476c-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="a476c-111">Количествобайтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="a476c-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="a476c-112">Тип массива.</span><span class="sxs-lookup"><span data-stu-id="a476c-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="a476c-113">Размер элемента массива.</span><span class="sxs-lookup"><span data-stu-id="a476c-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="a476c-114">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a476c-114">Return Value</span></span>  
 <span data-ttu-id="a476c-115">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="a476c-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a476c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a476c-116">Remarks</span></span>  
 <span data-ttu-id="a476c-117">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="a476c-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a476c-118">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a476c-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="a476c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a476c-119">Requirements</span></span>  
 <span data-ttu-id="a476c-120">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="a476c-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a476c-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a476c-121">See Also</span></span>  
 [<span data-ttu-id="a476c-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a476c-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
