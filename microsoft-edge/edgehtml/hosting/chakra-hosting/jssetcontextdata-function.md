---
description: Задает внутренние данные JsrtContext.
title: JsSetContextData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cac404b9e79bafb5a8eafb47e893dbdf38a02405
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235623"
---
# <span data-ttu-id="05e74-103">Функция JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="05e74-103">JsSetContextData Function</span></span>

<span data-ttu-id="05e74-104">Задает внутренние данные JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="05e74-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="05e74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05e74-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="05e74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05e74-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="05e74-107">Контекст, в котором необходимо настроить данные.</span><span class="sxs-lookup"><span data-stu-id="05e74-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="05e74-108">Указатель на данные, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="05e74-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="05e74-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="05e74-109">Return Value</span></span>  
 <span data-ttu-id="05e74-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="05e74-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="05e74-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05e74-111">Remarks</span></span>  
 <span data-ttu-id="05e74-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="05e74-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="05e74-113">Требования</span><span class="sxs-lookup"><span data-stu-id="05e74-113">Requirements</span></span>  
 <span data-ttu-id="05e74-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="05e74-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="05e74-115">См. также</span><span class="sxs-lookup"><span data-stu-id="05e74-115">See Also</span></span>  
 [<span data-ttu-id="05e74-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="05e74-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
