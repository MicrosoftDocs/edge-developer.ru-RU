---
description: Создает символ JavaScript.
title: JsCreateSymbol Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a2f77f477aeebac150635d93cbd0cd043357256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235519"
---
# <span data-ttu-id="af21d-103">Функция JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="af21d-103">JsCreateSymbol Function</span></span>

<span data-ttu-id="af21d-104">Создает символ JavaScript.</span><span class="sxs-lookup"><span data-stu-id="af21d-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="af21d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af21d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="af21d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af21d-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="af21d-107">Описание строки символа.</span><span class="sxs-lookup"><span data-stu-id="af21d-107">The string description of the symbol.</span></span> <span data-ttu-id="af21d-108">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="af21d-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="af21d-109">Новый символ.</span><span class="sxs-lookup"><span data-stu-id="af21d-109">The new symbol.</span></span>  
  
## <span data-ttu-id="af21d-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="af21d-110">Return Value</span></span>  
 <span data-ttu-id="af21d-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="af21d-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="af21d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af21d-112">Remarks</span></span>  
 <span data-ttu-id="af21d-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="af21d-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="af21d-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="af21d-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="af21d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="af21d-115">Requirements</span></span>  
 <span data-ttu-id="af21d-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="af21d-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="af21d-117">См. также</span><span class="sxs-lookup"><span data-stu-id="af21d-117">See Also</span></span>  
 [<span data-ttu-id="af21d-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="af21d-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
