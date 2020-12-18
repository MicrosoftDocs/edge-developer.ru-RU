---
description: Получает символ, связанный с ИД свойства.
title: JsGetSymbolFromPropertyId Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472253aea228ca0374c42d99710a7a7ab528184c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235871"
---
# <span data-ttu-id="84894-103">Функция JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="84894-103">JsGetSymbolFromPropertyId Function</span></span>

<span data-ttu-id="84894-104">Получает символ, связанный с ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="84894-104">Gets the symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="84894-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84894-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### <span data-ttu-id="84894-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84894-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="84894-107">ИД свойства, для получения символа.</span><span class="sxs-lookup"><span data-stu-id="84894-107">The property ID to get the symbol of.</span></span>  
  
 `symbol`  
 <span data-ttu-id="84894-108">Символ, связанный с ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="84894-108">The symbol associated with the property ID.</span></span>  
  
## <span data-ttu-id="84894-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="84894-109">Return Value</span></span>  
 <span data-ttu-id="84894-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="84894-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="84894-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84894-111">Remarks</span></span>  
 <span data-ttu-id="84894-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="84894-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="84894-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84894-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="84894-114">Требования</span><span class="sxs-lookup"><span data-stu-id="84894-114">Requirements</span></span>  
 <span data-ttu-id="84894-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="84894-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="84894-116">См. также</span><span class="sxs-lookup"><span data-stu-id="84894-116">See Also</span></span>  
 [<span data-ttu-id="84894-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="84894-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
