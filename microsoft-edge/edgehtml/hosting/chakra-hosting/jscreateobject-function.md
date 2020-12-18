---
description: Создает новый объект.
title: JsCreateObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5effe7ade1679392fcad7f2bb5cea880712ef7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235443"
---
# <span data-ttu-id="96c93-103">Функция JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="96c93-103">JsCreateObject Function</span></span>

<span data-ttu-id="96c93-104">Создает новый объект.</span><span class="sxs-lookup"><span data-stu-id="96c93-104">Creates a new object.</span></span>
  
## <span data-ttu-id="96c93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96c93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="96c93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96c93-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="96c93-107">Новый объект.</span><span class="sxs-lookup"><span data-stu-id="96c93-107">The new object.</span></span>  
  
## <span data-ttu-id="96c93-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="96c93-108">Return Value</span></span>  
 <span data-ttu-id="96c93-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="96c93-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="96c93-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96c93-110">Remarks</span></span>  
 <span data-ttu-id="96c93-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="96c93-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="96c93-112">Требования</span><span class="sxs-lookup"><span data-stu-id="96c93-112">Requirements</span></span>  
 <span data-ttu-id="96c93-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="96c93-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="96c93-114">См. также</span><span class="sxs-lookup"><span data-stu-id="96c93-114">See Also</span></span>  
 [<span data-ttu-id="96c93-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="96c93-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
