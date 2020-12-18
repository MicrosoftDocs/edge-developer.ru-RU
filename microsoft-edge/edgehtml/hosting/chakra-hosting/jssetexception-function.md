---
description: Задает состояние исключения для времени работы текущего контекста.
title: JsSetException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235501"
---
# <span data-ttu-id="dbc17-103">Функция JsSetException</span><span class="sxs-lookup"><span data-stu-id="dbc17-103">JsSetException Function</span></span>

<span data-ttu-id="dbc17-104">Задает состояние исключения для времени работы текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="dbc17-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="dbc17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc17-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="dbc17-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbc17-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="dbc17-107">Исключение JavaScript, устанавливаемого для времени работы текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="dbc17-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="dbc17-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="dbc17-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="dbc17-109">если подстройка была перенастройка в состояние исключения, код сбоя в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dbc17-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dbc17-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbc17-110">Remarks</span></span>  
 <span data-ttu-id="dbc17-111">Если время работы текущего контекста уже находится в состоянии исключения, этот API `JsErrorInExceptionState` возвращается.</span><span class="sxs-lookup"><span data-stu-id="dbc17-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="dbc17-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="dbc17-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dbc17-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dbc17-113">Requirements</span></span>  
 <span data-ttu-id="dbc17-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="dbc17-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dbc17-115">См. также</span><span class="sxs-lookup"><span data-stu-id="dbc17-115">See Also</span></span>  
 [<span data-ttu-id="dbc17-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dbc17-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
