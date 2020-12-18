---
description: Получает тип свойства.
title: JsGetPropertyIdType Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2b6e85ad-c630-4a07-a759-3b344d06faaa
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 93ee11bf74014361c89aa93bbb58361b426f573f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235687"
---
# <span data-ttu-id="deb4a-103">Функция JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="deb4a-103">JsGetPropertyIdType Function</span></span>

<span data-ttu-id="deb4a-104">Получает тип свойства.</span><span class="sxs-lookup"><span data-stu-id="deb4a-104">Gets the type of property.</span></span>  
  
## <span data-ttu-id="deb4a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deb4a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdType(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsPropertyIdType* propertyIdType  
);  
```  
  
#### <span data-ttu-id="deb4a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="deb4a-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="deb4a-107">ИД свойства для получения типа.</span><span class="sxs-lookup"><span data-stu-id="deb4a-107">The property ID to get the type of.</span></span>  
  
 `propertyIdType`  
 <span data-ttu-id="deb4a-108">`JsPropertyIdType`Заданный ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="deb4a-108">The `JsPropertyIdType` of the given property ID.</span></span>  
  
## <span data-ttu-id="deb4a-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="deb4a-109">Return Value</span></span>  
 <span data-ttu-id="deb4a-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="deb4a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="deb4a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="deb4a-111">Remarks</span></span>  
 <span data-ttu-id="deb4a-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="deb4a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="deb4a-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="deb4a-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="deb4a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="deb4a-114">Requirements</span></span>  
 <span data-ttu-id="deb4a-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="deb4a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="deb4a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="deb4a-116">See Also</span></span>  
 [<span data-ttu-id="deb4a-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="deb4a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
