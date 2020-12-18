---
description: Получает хранилище памяти, используемого DataView.
title: JsGetDataViewStorage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235550"
---
# <span data-ttu-id="010e4-103">Функция JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="010e4-103">JsGetDataViewStorage Function</span></span>

<span data-ttu-id="010e4-104">Получает используемую хранилище `DataView` памяти.</span><span class="sxs-lookup"><span data-stu-id="010e4-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="010e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="010e4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="010e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="010e4-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="010e4-107">Экземпляр DataView.</span><span class="sxs-lookup"><span data-stu-id="010e4-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="010e4-108">Буфер DataView.</span><span class="sxs-lookup"><span data-stu-id="010e4-108">The DataView's buffer.</span></span> <span data-ttu-id="010e4-109">Время жизни возвращаемого буфера такое же, как и время существования `DataView` буфера.</span><span class="sxs-lookup"><span data-stu-id="010e4-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="010e4-110">Указатель буфера не считается ссылкой на сборку `DataView` мусора.</span><span class="sxs-lookup"><span data-stu-id="010e4-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="010e4-111">Количествобайтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="010e4-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="010e4-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="010e4-112">Return Value</span></span>  
 <span data-ttu-id="010e4-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="010e4-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="010e4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="010e4-114">Remarks</span></span>  
 <span data-ttu-id="010e4-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="010e4-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="010e4-116">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="010e4-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="010e4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="010e4-117">Requirements</span></span>  
 <span data-ttu-id="010e4-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="010e4-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="010e4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="010e4-119">See Also</span></span>  
 [<span data-ttu-id="010e4-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="010e4-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
