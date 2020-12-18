---
description: Получает имя, связанное с ИД свойства.
title: JsGetPropertyNameFromId Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235516"
---
# <span data-ttu-id="350cf-103">Функция JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="350cf-103">JsGetPropertyNameFromId Function</span></span>

<span data-ttu-id="350cf-104">Получает имя, связанное с ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="350cf-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="350cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="350cf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="350cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="350cf-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="350cf-107">ИД свойства для получения имени.</span><span class="sxs-lookup"><span data-stu-id="350cf-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="350cf-108">Имя, связанное с ИД свойства.</span><span class="sxs-lookup"><span data-stu-id="350cf-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="350cf-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="350cf-109">Return Value</span></span>  
 <span data-ttu-id="350cf-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="350cf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="350cf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="350cf-111">Remarks</span></span>  
 <span data-ttu-id="350cf-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="350cf-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="350cf-113">Возвращенный буфер действителен, если время работы является актуальным и не может использоваться после его утилизации.</span><span class="sxs-lookup"><span data-stu-id="350cf-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="350cf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="350cf-114">Requirements</span></span>  
 <span data-ttu-id="350cf-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="350cf-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="350cf-116">См. также</span><span class="sxs-lookup"><span data-stu-id="350cf-116">See Also</span></span>  
 [<span data-ttu-id="350cf-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="350cf-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
