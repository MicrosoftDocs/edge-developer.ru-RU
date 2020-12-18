---
description: Извлекает `bool` значение boolean.
title: JsBooleanToBool Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 36bf2dc32b94466d8cdea37886e86a42c4ec01d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235318"
---
# <span data-ttu-id="3f90c-103">Функция JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="3f90c-103">JsBooleanToBool Function</span></span>

<span data-ttu-id="3f90c-104">Извлекает `bool` значение boolean.</span><span class="sxs-lookup"><span data-stu-id="3f90c-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="3f90c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f90c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="3f90c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f90c-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="3f90c-107">Значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="3f90c-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="3f90c-108">Преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="3f90c-108">The converted value.</span></span>  
  
## <span data-ttu-id="3f90c-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3f90c-109">Return Value</span></span>  
 <span data-ttu-id="3f90c-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3f90c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3f90c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f90c-111">Remarks</span></span>  
 <span data-ttu-id="3f90c-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="3f90c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3f90c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3f90c-113">Requirements</span></span>  
 <span data-ttu-id="3f90c-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3f90c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3f90c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3f90c-115">See Also</span></span>  
 [<span data-ttu-id="3f90c-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3f90c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
