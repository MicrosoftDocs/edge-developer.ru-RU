---
description: Получает контекст сценария, к котором принадлежит объект.
title: JsGetContextOfObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cea6cdcd-790f-455c-af04-026af8ae2eb7
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9085f9156e4e0ca9e952fe51447185239082f975
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235559"
---
# <span data-ttu-id="ead5b-103">Функция JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="ead5b-103">JsGetContextOfObject Function</span></span>

<span data-ttu-id="ead5b-104">Получает контекст сценария, к котором принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="ead5b-104">Gets the script context that the object belongs to.</span></span>  
  
## <span data-ttu-id="ead5b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ead5b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextOfObject(  
  _In_ JsValueRef object,  
  _Out_ JsContextRef *context  
);  
```  
  
#### <span data-ttu-id="ead5b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ead5b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ead5b-107">Объект для получения контекста.</span><span class="sxs-lookup"><span data-stu-id="ead5b-107">The object to get the context from.</span></span>  
  
 `context`  
 <span data-ttu-id="ead5b-108">Контекст, к котором принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="ead5b-108">The context the object belongs to.</span></span>  
  
## <span data-ttu-id="ead5b-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ead5b-109">Return Value</span></span>  
 <span data-ttu-id="ead5b-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ead5b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ead5b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ead5b-111">Remarks</span></span>  
 <span data-ttu-id="ead5b-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ead5b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ead5b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ead5b-113">Requirements</span></span>  
 <span data-ttu-id="ead5b-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ead5b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ead5b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="ead5b-115">See Also</span></span>  
 [<span data-ttu-id="ead5b-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ead5b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
