---
description: Создает новый объект ошибки JavaScript ReferenceError.
title: JsCreateReferenceError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fc8f10c443d6ca019c1460c84344bf04513e44b9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235524"
---
# <span data-ttu-id="37de5-103">Функция JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="37de5-103">JsCreateReferenceError Function</span></span>

<span data-ttu-id="37de5-104">Создает новый объект ошибки JavaScript ReferenceError.</span><span class="sxs-lookup"><span data-stu-id="37de5-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="37de5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37de5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="37de5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37de5-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="37de5-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="37de5-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="37de5-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="37de5-108">The new error object.</span></span>  
  
## <span data-ttu-id="37de5-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="37de5-109">Return Value</span></span>  
 <span data-ttu-id="37de5-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="37de5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="37de5-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37de5-111">Remarks</span></span>  
 <span data-ttu-id="37de5-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="37de5-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="37de5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="37de5-113">Requirements</span></span>  
 <span data-ttu-id="37de5-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="37de5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="37de5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="37de5-115">See Also</span></span>  
 [<span data-ttu-id="37de5-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="37de5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
