---
description: Определяет, является ли объект внешним.
title: JsHasExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasExternalData
helpviewer_keywords:
- JsHasExternalData function
ms.assetid: a077e3ac-4f6f-4d94-8398-f1b5cc4c18e0
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d73333215a33fc409190a0e33fa616b6350fb2a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235164"
---
# <span data-ttu-id="22ff7-103">Функция JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="22ff7-103">JsHasExternalData Function</span></span>

<span data-ttu-id="22ff7-104">Определяет, является ли объект внешним.</span><span class="sxs-lookup"><span data-stu-id="22ff7-104">Determines whether an object is an external object.</span></span>  
  
## <span data-ttu-id="22ff7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22ff7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="22ff7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22ff7-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="22ff7-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="22ff7-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="22ff7-108">Является ли объект внешним.</span><span class="sxs-lookup"><span data-stu-id="22ff7-108">Whether the object is an external object.</span></span>  
  
## <span data-ttu-id="22ff7-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="22ff7-109">Return Value</span></span>  
 <span data-ttu-id="22ff7-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="22ff7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="22ff7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22ff7-111">Remarks</span></span>  
 <span data-ttu-id="22ff7-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="22ff7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="22ff7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="22ff7-113">Requirements</span></span>  
 <span data-ttu-id="22ff7-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="22ff7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="22ff7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="22ff7-115">See Also</span></span>  
 [<span data-ttu-id="22ff7-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="22ff7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
