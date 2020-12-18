---
description: Получает ИД свойства, связанного с символом.
title: JsGetPropertyIdFromSymbol Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 190fe4b9-352e-4b10-9d0e-6c6bbd6363e8
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97f1fb517164d692cdd010f899dc40d2e3596ed
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235688"
---
# <span data-ttu-id="622f0-103">Функция JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="622f0-103">JsGetPropertyIdFromSymbol Function</span></span>

<span data-ttu-id="622f0-104">Получает ИД свойства, связанного с символом.</span><span class="sxs-lookup"><span data-stu-id="622f0-104">Gets the property ID associated with the symbol.</span></span>  
  
## <span data-ttu-id="622f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="622f0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromSymbol(  
   _In_ JsValueRef symbol,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="622f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="622f0-106">Parameters</span></span>  
 `symbol`  
 <span data-ttu-id="622f0-107">Символ, для которого извлекается ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="622f0-107">The symbol whose property ID is being retrieved.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="622f0-108">ИД свойства для заданного символа.</span><span class="sxs-lookup"><span data-stu-id="622f0-108">The property ID for the given symbol.</span></span>  
  
## <span data-ttu-id="622f0-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="622f0-109">Return Value</span></span>  
 <span data-ttu-id="622f0-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="622f0-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="622f0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="622f0-111">Remarks</span></span>  
 <span data-ttu-id="622f0-112">ИД свойств являются специфическими для контекста и не могут использоваться в контекстах.</span><span class="sxs-lookup"><span data-stu-id="622f0-112">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="622f0-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="622f0-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="622f0-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="622f0-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="622f0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="622f0-115">Requirements</span></span>  
 <span data-ttu-id="622f0-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="622f0-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="622f0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="622f0-117">See Also</span></span>  
 [<span data-ttu-id="622f0-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="622f0-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
