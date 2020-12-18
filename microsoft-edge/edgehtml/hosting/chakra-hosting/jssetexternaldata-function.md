---
description: Задает внешние данные для внешнего объекта.
title: JsSetExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235618"
---
# <span data-ttu-id="73a49-103">Функция JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="73a49-103">JsSetExternalData Function</span></span>

<span data-ttu-id="73a49-104">Задает внешние данные для внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="73a49-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="73a49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73a49-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="73a49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="73a49-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="73a49-107">Внешний объект.</span><span class="sxs-lookup"><span data-stu-id="73a49-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="73a49-108">Внешние данные, хранимые в объекте.</span><span class="sxs-lookup"><span data-stu-id="73a49-108">The external data stored in the object.</span></span> <span data-ttu-id="73a49-109">Может иметь null, если в объекте не хранятся внешние данные.</span><span class="sxs-lookup"><span data-stu-id="73a49-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="73a49-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="73a49-110">Return Value</span></span>  
 <span data-ttu-id="73a49-111">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="73a49-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="73a49-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73a49-112">Remarks</span></span>  
 <span data-ttu-id="73a49-113">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="73a49-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="73a49-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73a49-114">Requirements</span></span>  
 <span data-ttu-id="73a49-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="73a49-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="73a49-116">См. также</span><span class="sxs-lookup"><span data-stu-id="73a49-116">See Also</span></span>  
 [<span data-ttu-id="73a49-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="73a49-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
