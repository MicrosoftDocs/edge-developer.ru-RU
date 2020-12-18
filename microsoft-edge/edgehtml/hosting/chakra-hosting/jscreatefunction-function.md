---
description: Создает новую функцию JavaScript.
title: JsCreateFunction Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateFunction
helpviewer_keywords:
- JsCreateFunction function
ms.assetid: b298a96a-5ef7-4203-a8c8-55f9bfc6d2bb
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f7e67e86e6d8055664bfb1b58e6d5653f6d75d1b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235661"
---
# <span data-ttu-id="f77db-103">Функция JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="f77db-103">JsCreateFunction Function</span></span>

<span data-ttu-id="f77db-104">Создает новую функцию JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f77db-104">Creates a new JavaScript function.</span></span>
  
## <span data-ttu-id="f77db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f77db-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateFunction(  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="f77db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f77db-106">Parameters</span></span>  
 `nativeFunction`  
 <span data-ttu-id="f77db-107">Метод, вызываемого при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="f77db-107">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="f77db-108">Предоставленное пользователем состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="f77db-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="f77db-109">Новый объект функции.</span><span class="sxs-lookup"><span data-stu-id="f77db-109">The new function object.</span></span>  
  
## <span data-ttu-id="f77db-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f77db-110">Return Value</span></span>  
 <span data-ttu-id="f77db-111">Результат вызова, если он есть.</span><span class="sxs-lookup"><span data-stu-id="f77db-111">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="f77db-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f77db-112">Remarks</span></span>  
 <span data-ttu-id="f77db-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="f77db-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f77db-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f77db-114">Requirements</span></span>  
 <span data-ttu-id="f77db-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="f77db-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f77db-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f77db-116">See Also</span></span>  
 [<span data-ttu-id="f77db-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f77db-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
