---
description: Создает новый объект ошибки Синтаксис JavaScriptError.
title: JsCreateSyntaxError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d6534bfa2b59cb2f6ab68c231d7a97c84876d62
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235657"
---
# <span data-ttu-id="82112-103">Функция JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="82112-103">JsCreateSyntaxError Function</span></span>

<span data-ttu-id="82112-104">Создает новый объект ошибки Синтаксис JavaScriptError.</span><span class="sxs-lookup"><span data-stu-id="82112-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="82112-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82112-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="82112-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82112-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="82112-107">Сообщение для объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="82112-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="82112-108">Новый объект ошибки.</span><span class="sxs-lookup"><span data-stu-id="82112-108">The new error object.</span></span>  
  
## <span data-ttu-id="82112-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="82112-109">Return Value</span></span>  
 <span data-ttu-id="82112-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="82112-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="82112-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82112-111">Remarks</span></span>  
 <span data-ttu-id="82112-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="82112-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="82112-113">Требования</span><span class="sxs-lookup"><span data-stu-id="82112-113">Requirements</span></span>  
 <span data-ttu-id="82112-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="82112-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="82112-115">См. также</span><span class="sxs-lookup"><span data-stu-id="82112-115">See Also</span></span>  
 [<span data-ttu-id="82112-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="82112-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
