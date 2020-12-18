---
description: Создает новый объект ошибки JavaScript.
title: JsCreateError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd2fd0172902cc6dc8a4dd169eef5947d0b25256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235303"
---
# <span data-ttu-id="d8e89-103">Функция JsCreateError</span><span class="sxs-lookup"><span data-stu-id="d8e89-103">JsCreateError Function</span></span>

<span data-ttu-id="d8e89-104">Создает новый объект ошибки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d8e89-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="d8e89-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8e89-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d8e89-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8e89-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d8e89-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8e89-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d8e89-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8e89-108">The new error object.</span></span>  
  
## <span data-ttu-id="d8e89-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d8e89-109">Return Value</span></span>  
 <span data-ttu-id="d8e89-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="d8e89-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d8e89-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8e89-111">Remarks</span></span>  
 <span data-ttu-id="d8e89-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="d8e89-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d8e89-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d8e89-113">Requirements</span></span>  
 <span data-ttu-id="d8e89-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="d8e89-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d8e89-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d8e89-115">See Also</span></span>  
 [<span data-ttu-id="d8e89-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d8e89-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
