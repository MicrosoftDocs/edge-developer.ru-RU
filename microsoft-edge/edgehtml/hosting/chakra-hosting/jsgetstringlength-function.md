---
description: Получает длину строки.
title: JsGetStringLength Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 10fd6be4bb839ccb9eb64c99931cdb474e3aa7a2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235872"
---
# <span data-ttu-id="204b9-103">Функция JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="204b9-103">JsGetStringLength Function</span></span>

<span data-ttu-id="204b9-104">Получает длину строки.</span><span class="sxs-lookup"><span data-stu-id="204b9-104">Gets the length of a string value.</span></span>  
  
## <span data-ttu-id="204b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="204b9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### <span data-ttu-id="204b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="204b9-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="204b9-107">Строковая длина.</span><span class="sxs-lookup"><span data-stu-id="204b9-107">The string value to get the length of.</span></span>  
  
 `length`  
 <span data-ttu-id="204b9-108">Длина строки.</span><span class="sxs-lookup"><span data-stu-id="204b9-108">The length of the string.</span></span>  
  
## <span data-ttu-id="204b9-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="204b9-109">Return Value</span></span>  
 <span data-ttu-id="204b9-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="204b9-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="204b9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="204b9-111">Remarks</span></span>  
 <span data-ttu-id="204b9-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="204b9-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="204b9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="204b9-113">Requirements</span></span>  
 <span data-ttu-id="204b9-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="204b9-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="204b9-115">См. также</span><span class="sxs-lookup"><span data-stu-id="204b9-115">See Also</span></span>  
 [<span data-ttu-id="204b9-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="204b9-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
