---
description: Создает новую функцию JavaScript с именем.
title: JsCreateNamedFunction Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235442"
---
# <span data-ttu-id="fbcb3-103">Функция JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="fbcb3-103">JsCreateNamedFunction Function</span></span>

<span data-ttu-id="fbcb3-104">Создает новую функцию JavaScript с именем.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-104">Creates a new JavaScript function with name.</span></span>
  
## <span data-ttu-id="fbcb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbcb3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### <span data-ttu-id="fbcb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbcb3-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="fbcb3-107">Имя этой функции, которая будет использоваться для диагностики и строки.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-107">The name of this function that will be used for diagnostics and stringification purposes.</span></span>  
  
 `nativeFunction`  
 <span data-ttu-id="fbcb3-108">Метод, вызываемого при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-108">The method to call when the function is invoked.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="fbcb3-109">Пользовательское состояние, которое будет передано обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-109">User provided state that will be passed back to the callback.</span></span>  
  
 `function`  
 <span data-ttu-id="fbcb3-110">Новый объект функции.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-110">The new function object.</span></span>  
  
## <span data-ttu-id="fbcb3-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="fbcb3-111">Return Value</span></span>  
  
## <span data-ttu-id="fbcb3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fbcb3-112">Remarks</span></span>  
 <span data-ttu-id="fbcb3-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="fbcb3-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fbcb3-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="fbcb3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fbcb3-115">Requirements</span></span>  
 <span data-ttu-id="fbcb3-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="fbcb3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fbcb3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="fbcb3-117">See Also</span></span>  
 [<span data-ttu-id="fbcb3-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fbcb3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
