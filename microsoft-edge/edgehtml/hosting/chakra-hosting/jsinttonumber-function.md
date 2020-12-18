---
description: Создает значение числа на ряду `int` со значением.
title: JsIntToNumber Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235685"
---
# <span data-ttu-id="56625-103">Функция JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="56625-103">JsIntToNumber Function</span></span>

<span data-ttu-id="56625-104">Создает значение числа на ряду `int` со значением.</span><span class="sxs-lookup"><span data-stu-id="56625-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="56625-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56625-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="56625-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56625-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="56625-107">Значение `int` для преобразования в число.</span><span class="sxs-lookup"><span data-stu-id="56625-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="56625-108">Новое значение номера.</span><span class="sxs-lookup"><span data-stu-id="56625-108">The new number value.</span></span>  
  
## <span data-ttu-id="56625-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="56625-109">Return Value</span></span>  
 <span data-ttu-id="56625-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="56625-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="56625-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56625-111">Remarks</span></span>  
 <span data-ttu-id="56625-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="56625-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="56625-113">Требования</span><span class="sxs-lookup"><span data-stu-id="56625-113">Requirements</span></span>  
 <span data-ttu-id="56625-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="56625-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="56625-115">См. также</span><span class="sxs-lookup"><span data-stu-id="56625-115">See Also</span></span>  
 [<span data-ttu-id="56625-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="56625-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
