---
description: Получает хранилище памяти, используемого ArrayBuffer.
title: JsGetArrayBufferStorage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235429"
---
# <span data-ttu-id="6400c-103">Функция JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="6400c-103">JsGetArrayBufferStorage Function</span></span>

<span data-ttu-id="6400c-104">Получает используемую хранилище `ArrayBuffer` памяти.</span><span class="sxs-lookup"><span data-stu-id="6400c-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="6400c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6400c-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="6400c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6400c-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="6400c-107">Экземпляр ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="6400c-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="6400c-108">Буфер ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="6400c-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="6400c-109">Время жизни возвращаемого буфера такое же, как и время существования `ArrayBuffer` буфера.</span><span class="sxs-lookup"><span data-stu-id="6400c-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="6400c-110">Указатель буфера не считается ссылкой на сборку `ArrayBuffer` мусора.</span><span class="sxs-lookup"><span data-stu-id="6400c-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="6400c-111">Количествобайтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="6400c-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="6400c-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6400c-112">Return Value</span></span>  
 <span data-ttu-id="6400c-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="6400c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6400c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6400c-114">Remarks</span></span>  
 <span data-ttu-id="6400c-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="6400c-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6400c-116">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6400c-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="6400c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6400c-117">Requirements</span></span>  
 <span data-ttu-id="6400c-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="6400c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6400c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6400c-119">See Also</span></span>  
 [<span data-ttu-id="6400c-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6400c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
