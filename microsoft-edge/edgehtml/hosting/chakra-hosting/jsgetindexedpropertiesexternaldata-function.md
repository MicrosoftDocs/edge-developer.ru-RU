---
description: Извлекает внешние данные индексных свойств объекта.
title: JsGetIndexedPropertiesExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235134"
---
# <span data-ttu-id="e411f-103">Функция JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="e411f-103">JsGetIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="e411f-104">Извлекает внешние данные индексных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="e411f-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="e411f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e411f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="e411f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e411f-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e411f-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="e411f-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="e411f-108">Хранилище внешних данных для индексных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="e411f-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="e411f-109">Тип элемента массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="e411f-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="e411f-110">Количество элементов массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="e411f-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="e411f-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e411f-111">Return Value</span></span>  
 <span data-ttu-id="e411f-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="e411f-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e411f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e411f-113">Remarks</span></span>  
 <span data-ttu-id="e411f-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e411f-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="e411f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e411f-115">Requirements</span></span>  
 <span data-ttu-id="e411f-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e411f-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e411f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e411f-117">See Also</span></span>  
 [<span data-ttu-id="e411f-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e411f-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
