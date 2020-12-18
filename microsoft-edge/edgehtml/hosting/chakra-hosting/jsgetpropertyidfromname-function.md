---
description: Получает ИД свойства, связанного с именем.
title: JsGetPropertyIdFromName Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235654"
---
# <span data-ttu-id="2cbfb-103">Функция JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="2cbfb-103">JsGetPropertyIdFromName Function</span></span>

<span data-ttu-id="2cbfb-104">Получает ИД свойства, связанного с именем.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="2cbfb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cbfb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="2cbfb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cbfb-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="2cbfb-107">Имя ИД свойства, которое требуется получить или создать.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="2cbfb-108">Имя может состоять только из цифр.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="2cbfb-109">ИД свойства в этой времени работы для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="2cbfb-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="2cbfb-110">Return Value</span></span>  
 <span data-ttu-id="2cbfb-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2cbfb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cbfb-112">Remarks</span></span>  
 <span data-ttu-id="2cbfb-113">ИД свойств являются специфическими для контекста и не могут использоваться в контекстах.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="2cbfb-114">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="2cbfb-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2cbfb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2cbfb-115">Requirements</span></span>  
 <span data-ttu-id="2cbfb-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="2cbfb-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2cbfb-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2cbfb-117">See Also</span></span>  
 [<span data-ttu-id="2cbfb-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2cbfb-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
