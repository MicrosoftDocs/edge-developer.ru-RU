---
description: Создает новый объект, который хранит некоторые внешние данные.
title: JsCreateExternalObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateExternalObject
helpviewer_keywords:
- JsCreateExternalObject function
ms.assetid: 6bcef506-93fb-429b-b06a-a971ff0b71f3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d402c3d379a16186daaba601c7f830c53a9a953
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235816"
---
# <span data-ttu-id="fb4ce-103">Функция JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="fb4ce-103">JsCreateExternalObject Function</span></span>

<span data-ttu-id="fb4ce-104">Создает новый объект, который хранит некоторые внешние данные.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-104">Creates a new object that stores some external data.</span></span>
  
## <span data-ttu-id="fb4ce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb4ce-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalObject(  
   _In_opt_ void *data,  
   _In_opt_ JsFinalizeCallback finalizeCallback,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="fb4ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb4ce-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="fb4ce-107">Внешние данные, которые будет представлять объект.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-107">External data that the object will represent.</span></span> <span data-ttu-id="fb4ce-108">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-108">May be null.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="fb4ce-109">Callback for when the object is finalized.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="fb4ce-110">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-110">May be null.</span></span>  
  
 `object`  
 <span data-ttu-id="fb4ce-111">Новый объект.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-111">The new object.</span></span>  
  
## <span data-ttu-id="fb4ce-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="fb4ce-112">Return Value</span></span>  
 <span data-ttu-id="fb4ce-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fb4ce-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb4ce-114">Remarks</span></span>  
 <span data-ttu-id="fb4ce-115">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="fb4ce-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fb4ce-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fb4ce-116">Requirements</span></span>  
 <span data-ttu-id="fb4ce-117">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="fb4ce-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fb4ce-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fb4ce-118">See Also</span></span>  
 [<span data-ttu-id="fb4ce-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fb4ce-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
