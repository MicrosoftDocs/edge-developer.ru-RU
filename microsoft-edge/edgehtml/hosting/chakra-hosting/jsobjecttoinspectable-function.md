---
description: Отвергет объект JavaScript на `IInspectable` указатель.
title: JsObjectToInspectable Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235633"
---
# <span data-ttu-id="468e4-103">Функция JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="468e4-103">JsObjectToInspectable Function</span></span>

<span data-ttu-id="468e4-104">Отвергет объект JavaScript на `IInspectable` указатель.</span><span class="sxs-lookup"><span data-stu-id="468e4-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="468e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="468e4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="468e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="468e4-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="468e4-107">Значение JavaScript, которое должно быть проецируемым на `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="468e4-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="468e4-108">Значение `IInspectable` объекта.</span><span class="sxs-lookup"><span data-stu-id="468e4-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="468e4-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="468e4-109">Return Value</span></span>  
 <span data-ttu-id="468e4-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="468e4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="468e4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="468e4-111">Remarks</span></span>  
 <span data-ttu-id="468e4-112">Ведущие точки отвечают за принудительное применение правил потоков COM.</span><span class="sxs-lookup"><span data-stu-id="468e4-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="468e4-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="468e4-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="468e4-114">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="468e4-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="468e4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="468e4-115">Requirements</span></span>  
 <span data-ttu-id="468e4-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="468e4-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="468e4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="468e4-117">See Also</span></span>  
 [<span data-ttu-id="468e4-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="468e4-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
