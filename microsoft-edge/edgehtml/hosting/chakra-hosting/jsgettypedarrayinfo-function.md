---
description: Получает часто используемые свойства типтного массива.
title: JsGetTypedArrayInfo Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235669"
---
# <span data-ttu-id="fa320-103">Функция JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="fa320-103">JsGetTypedArrayInfo Function</span></span>

<span data-ttu-id="fa320-104">Получает часто используемые свойства типтного массива.</span><span class="sxs-lookup"><span data-stu-id="fa320-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="fa320-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa320-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="fa320-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa320-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="fa320-107">Типный экземпляр массива.</span><span class="sxs-lookup"><span data-stu-id="fa320-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="fa320-108">Тип массива.</span><span class="sxs-lookup"><span data-stu-id="fa320-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="fa320-109">Backstore `ArrayBuffer` массива.</span><span class="sxs-lookup"><span data-stu-id="fa320-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="fa320-110">Смещение в bytes от начала arrayBuffer, на который ссылается массив.</span><span class="sxs-lookup"><span data-stu-id="fa320-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="fa320-111">Количество данных в массиве.</span><span class="sxs-lookup"><span data-stu-id="fa320-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="fa320-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="fa320-112">Return Value</span></span>  
 <span data-ttu-id="fa320-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="fa320-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fa320-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa320-114">Remarks</span></span>  
 <span data-ttu-id="fa320-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="fa320-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fa320-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fa320-116">Requirements</span></span>  
 <span data-ttu-id="fa320-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="fa320-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fa320-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fa320-118">See Also</span></span>  
 [<span data-ttu-id="fa320-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fa320-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
