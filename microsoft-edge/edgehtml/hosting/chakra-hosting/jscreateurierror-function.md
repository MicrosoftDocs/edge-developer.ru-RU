---
description: Создает новый объект ошибки JavaScript URIError.
title: JsCreateURIError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235441"
---
# <span data-ttu-id="bf89f-103">Функция JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="bf89f-103">JsCreateURIError Function</span></span>

<span data-ttu-id="bf89f-104">Создает новый объект ошибки JavaScript URIError.</span><span class="sxs-lookup"><span data-stu-id="bf89f-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="bf89f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf89f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="bf89f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf89f-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="bf89f-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="bf89f-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="bf89f-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="bf89f-108">The new error object.</span></span>  
  
## <span data-ttu-id="bf89f-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bf89f-109">Return Value</span></span>  
 <span data-ttu-id="bf89f-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="bf89f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bf89f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf89f-111">Remarks</span></span>  
 <span data-ttu-id="bf89f-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="bf89f-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bf89f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bf89f-113">Requirements</span></span>  
 <span data-ttu-id="bf89f-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="bf89f-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf89f-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bf89f-115">See Also</span></span>  
 [<span data-ttu-id="bf89f-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf89f-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
