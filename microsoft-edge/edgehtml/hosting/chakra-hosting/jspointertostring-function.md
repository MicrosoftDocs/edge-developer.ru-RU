---
description: Создает строку из указателя строки.
title: JsPointerToString Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c00a060098f0b021afca27b300f3e0578e992cb9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235634"
---
# <span data-ttu-id="8e4a4-103">Функция JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="8e4a4-103">JsPointerToString Function</span></span>

<span data-ttu-id="8e4a4-104">Создает строку из указателя строки.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="8e4a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e4a4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="8e4a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e4a4-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="8e4a4-107">Указатель строки, который необходимо преобразовать в строку.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="8e4a4-108">Длина строки для преобразования.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="8e4a4-109">Новое строковая строка.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-109">The new string value.</span></span>  
  
## <span data-ttu-id="8e4a4-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="8e4a4-110">Return Value</span></span>  
 <span data-ttu-id="8e4a4-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8e4a4-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e4a4-112">Remarks</span></span>  
 <span data-ttu-id="8e4a4-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="8e4a4-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8e4a4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8e4a4-114">Requirements</span></span>  
 <span data-ttu-id="8e4a4-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="8e4a4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8e4a4-116">См. также</span><span class="sxs-lookup"><span data-stu-id="8e4a4-116">See Also</span></span>  
 [<span data-ttu-id="8e4a4-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8e4a4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
