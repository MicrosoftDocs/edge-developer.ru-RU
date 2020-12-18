---
description: Создает объект `DataView` Javascript.
title: JsCreateDataView Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235300"
---
# <span data-ttu-id="ab95b-103">Функция JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="ab95b-103">JsCreateDataView Function</span></span>

<span data-ttu-id="ab95b-104">Создает объект `DataView` Javascript.</span><span class="sxs-lookup"><span data-stu-id="ab95b-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="ab95b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab95b-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ab95b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab95b-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="ab95b-107">Существующий `ArrayBuffer` объект, который будет использовать в качестве хранилища для объекта `DataView` результата.</span><span class="sxs-lookup"><span data-stu-id="ab95b-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="ab95b-108">Смещение в вайтах от начала результата `arrayBuffer` `DataView` для ссылки.</span><span class="sxs-lookup"><span data-stu-id="ab95b-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="ab95b-109">Количество в массиве ArrayBuffer, на которые ссылается DataView результатов.</span><span class="sxs-lookup"><span data-stu-id="ab95b-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="ab95b-110">Новый объект DataView.</span><span class="sxs-lookup"><span data-stu-id="ab95b-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="ab95b-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ab95b-111">Return Value</span></span>  
 <span data-ttu-id="ab95b-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ab95b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ab95b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab95b-113">Remarks</span></span>  
 <span data-ttu-id="ab95b-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ab95b-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ab95b-115">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ab95b-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="ab95b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ab95b-116">Requirements</span></span>  
 <span data-ttu-id="ab95b-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ab95b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ab95b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ab95b-118">See Also</span></span>  
 [<span data-ttu-id="ab95b-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ab95b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
