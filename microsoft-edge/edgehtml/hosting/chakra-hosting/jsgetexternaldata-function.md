---
description: Извлекает данные из внешнего объекта.
title: JsGetExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d046b5c515b1a688cd527fdc0eb9cd173eb47570
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235548"
---
# <span data-ttu-id="6ebee-103">Функция JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="6ebee-103">JsGetExternalData Function</span></span>

<span data-ttu-id="6ebee-104">Извлекает данные из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="6ebee-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="6ebee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ebee-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="6ebee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ebee-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6ebee-107">Внешний объект.</span><span class="sxs-lookup"><span data-stu-id="6ebee-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="6ebee-108">Внешние данные, хранимые в объекте.</span><span class="sxs-lookup"><span data-stu-id="6ebee-108">The external data stored in the object.</span></span> <span data-ttu-id="6ebee-109">Может иметь null, если в объекте не хранятся внешние данные.</span><span class="sxs-lookup"><span data-stu-id="6ebee-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="6ebee-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6ebee-110">Return Value</span></span>  
 <span data-ttu-id="6ebee-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="6ebee-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6ebee-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ebee-112">Remarks</span></span>  
 <span data-ttu-id="6ebee-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="6ebee-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6ebee-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6ebee-114">Requirements</span></span>  
 <span data-ttu-id="6ebee-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="6ebee-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6ebee-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6ebee-116">See Also</span></span>  
 [<span data-ttu-id="6ebee-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6ebee-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
