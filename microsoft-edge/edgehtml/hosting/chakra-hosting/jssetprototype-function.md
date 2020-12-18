---
description: Задает прототип объекта.
title: JsSetPrototype Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 88e1e421-4ae5-4e3b-b377-19256cc80e9f
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 860a7b8d85e043c87d554e09de50d0cb642b273a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235286"
---
# <span data-ttu-id="10baf-103">Функция JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="10baf-103">JsSetPrototype Function</span></span>

<span data-ttu-id="10baf-104">Задает прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="10baf-104">Sets the prototype of an object.</span></span>  
  
## <span data-ttu-id="10baf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10baf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPrototype(  
   _In_ JsValueRef object,  
   _In_ JsValueRef prototypeObject  
);  
```  
  
#### <span data-ttu-id="10baf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="10baf-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="10baf-107">Объект, прототип которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="10baf-107">The object whose prototype is to be changed.</span></span>  
  
 `prototypeObject`  
 <span data-ttu-id="10baf-108">Новый прототип объекта.</span><span class="sxs-lookup"><span data-stu-id="10baf-108">The object's new prototype.</span></span>  
  
## <span data-ttu-id="10baf-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="10baf-109">Return Value</span></span>  
 <span data-ttu-id="10baf-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="10baf-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="10baf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10baf-111">Remarks</span></span>  
 <span data-ttu-id="10baf-112">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="10baf-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="10baf-113">Требования</span><span class="sxs-lookup"><span data-stu-id="10baf-113">Requirements</span></span>  
 <span data-ttu-id="10baf-114">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="10baf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="10baf-115">См. также</span><span class="sxs-lookup"><span data-stu-id="10baf-115">See Also</span></span>  
 [<span data-ttu-id="10baf-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="10baf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
