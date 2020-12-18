---
description: Делает объект неосязаемым.
title: JsPreventExtension Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235632"
---
# <span data-ttu-id="ad4a9-103">Функция JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="ad4a9-103">JsPreventExtension Function</span></span>

<span data-ttu-id="ad4a9-104">Делает объект неосязаемым.</span><span class="sxs-lookup"><span data-stu-id="ad4a9-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="ad4a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad4a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="ad4a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad4a9-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ad4a9-107">Объект, который необходимо сделать неразмещенным.</span><span class="sxs-lookup"><span data-stu-id="ad4a9-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="ad4a9-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ad4a9-108">Return Value</span></span>  
 <span data-ttu-id="ad4a9-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="ad4a9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ad4a9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad4a9-110">Remarks</span></span>  
 <span data-ttu-id="ad4a9-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="ad4a9-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ad4a9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ad4a9-112">Requirements</span></span>  
 <span data-ttu-id="ad4a9-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="ad4a9-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ad4a9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ad4a9-114">See Also</span></span>  
 [<span data-ttu-id="ad4a9-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ad4a9-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
