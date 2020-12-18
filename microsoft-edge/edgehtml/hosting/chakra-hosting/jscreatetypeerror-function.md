---
description: Создает новый объект ошибки JavaScript TypeError.
title: JsCreateTypeError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627dfdc6f01f0708366720a957b3784fc7bb59a4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235653"
---
# <span data-ttu-id="9b3dc-103">Функция JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="9b3dc-103">JsCreateTypeError Function</span></span>

<span data-ttu-id="9b3dc-104">Создает новый объект ошибки JavaScript TypeError.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="9b3dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b3dc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="9b3dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b3dc-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="9b3dc-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="9b3dc-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-108">The new error object.</span></span>  
  
## <span data-ttu-id="9b3dc-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9b3dc-109">Return Value</span></span>  
 <span data-ttu-id="9b3dc-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9b3dc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b3dc-111">Remarks</span></span>  
 <span data-ttu-id="9b3dc-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="9b3dc-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9b3dc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9b3dc-113">Requirements</span></span>  
 <span data-ttu-id="9b3dc-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="9b3dc-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9b3dc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="9b3dc-115">See Also</span></span>  
 [<span data-ttu-id="9b3dc-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9b3dc-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
