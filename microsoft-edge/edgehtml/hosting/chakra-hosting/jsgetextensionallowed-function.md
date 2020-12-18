---
description: Возвращает значение, которое указывает, является ли объект extensible или нет.
title: JsGetExtensionAllowed Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7bc9e3265b48a27d0da4bc4646b2b5e3b1765b86
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235549"
---
# <span data-ttu-id="7f1cc-103">Функция JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="7f1cc-103">JsGetExtensionAllowed Function</span></span>

<span data-ttu-id="7f1cc-104">Возвращает значение, которое указывает, является ли объект extensible или нет.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="7f1cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f1cc-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="7f1cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f1cc-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7f1cc-107">Объект для тестирования.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="7f1cc-108">Является ли объект выдохшимся.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="7f1cc-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="7f1cc-109">Return Value</span></span>  
 <span data-ttu-id="7f1cc-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7f1cc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f1cc-111">Remarks</span></span>  
 <span data-ttu-id="7f1cc-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="7f1cc-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7f1cc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7f1cc-113">Requirements</span></span>  
 <span data-ttu-id="7f1cc-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="7f1cc-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7f1cc-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7f1cc-115">See Also</span></span>  
 [<span data-ttu-id="7f1cc-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7f1cc-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
