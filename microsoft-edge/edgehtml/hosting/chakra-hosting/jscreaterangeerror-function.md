---
description: Создает новый объект ошибки RangeError javaScript.
title: JsCreateRangeError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 72cf882d5f9517f0f05d9e3367283f5f531dbdb3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235468"
---
# <span data-ttu-id="eba8d-103">Функция JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="eba8d-103">JsCreateRangeError Function</span></span>

<span data-ttu-id="eba8d-104">Создает новый объект ошибки RangeError javaScript.</span><span class="sxs-lookup"><span data-stu-id="eba8d-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="eba8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eba8d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="eba8d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eba8d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="eba8d-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="eba8d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="eba8d-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="eba8d-108">The new error object.</span></span>  
  
## <span data-ttu-id="eba8d-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="eba8d-109">Return Value</span></span>  
 <span data-ttu-id="eba8d-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="eba8d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="eba8d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eba8d-111">Remarks</span></span>  
 <span data-ttu-id="eba8d-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="eba8d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="eba8d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="eba8d-113">Requirements</span></span>  
 <span data-ttu-id="eba8d-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="eba8d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="eba8d-115">См. также</span><span class="sxs-lookup"><span data-stu-id="eba8d-115">See Also</span></span>  
 [<span data-ttu-id="eba8d-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="eba8d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
