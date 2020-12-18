---
description: Задает для индексных свойств объекта внешние данные. Внешние данные будут использоваться в качестве заднего хранения для индексных свойств объекта и будут доступны в виде типтного массива.
title: JsSetIndexedPropertiesToExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235288"
---
# <span data-ttu-id="113ff-104">Функция JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="113ff-104">JsSetIndexedPropertiesToExternalData Function</span></span>

<span data-ttu-id="113ff-105">Задает индексные свойства объекта для внешних данных.</span><span class="sxs-lookup"><span data-stu-id="113ff-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="113ff-106">Внешние данные будут использоваться в качестве заднего хранения для индексных свойств объекта и будут доступны в виде типтного массива.</span><span class="sxs-lookup"><span data-stu-id="113ff-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="113ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="113ff-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="113ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="113ff-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="113ff-109">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="113ff-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="113ff-110">Внешние данные, используемые в качестве back store для индексных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="113ff-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="113ff-111">Тип элемента массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="113ff-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="113ff-112">Количество элементов массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="113ff-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="113ff-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="113ff-113">Return Value</span></span>  
 <span data-ttu-id="113ff-114">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="113ff-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="113ff-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="113ff-115">Remarks</span></span>  
 <span data-ttu-id="113ff-116">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="113ff-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="113ff-117">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="113ff-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="113ff-118">Требования</span><span class="sxs-lookup"><span data-stu-id="113ff-118">Requirements</span></span>  
 <span data-ttu-id="113ff-119">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="113ff-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="113ff-120">См. также</span><span class="sxs-lookup"><span data-stu-id="113ff-120">See Also</span></span>  
 [<span data-ttu-id="113ff-121">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="113ff-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
