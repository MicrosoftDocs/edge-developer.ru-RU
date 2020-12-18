---
description: Получает глобальный объект в текущем контексте сценария.
title: JsGetGlobalObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cda960710180c135b99abd359d0cc76776ff0225
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235546"
---
# <span data-ttu-id="145f2-103">Функция JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="145f2-103">JsGetGlobalObject Function</span></span>

<span data-ttu-id="145f2-104">Получает глобальный объект в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="145f2-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="145f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="145f2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="145f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="145f2-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="145f2-107">Глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="145f2-107">The global object.</span></span>  
  
## <span data-ttu-id="145f2-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="145f2-108">Return Value</span></span>  
 <span data-ttu-id="145f2-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="145f2-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="145f2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="145f2-110">Remarks</span></span>  
 <span data-ttu-id="145f2-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="145f2-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="145f2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="145f2-112">Requirements</span></span>  
 <span data-ttu-id="145f2-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="145f2-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="145f2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="145f2-114">See Also</span></span>  
 [<span data-ttu-id="145f2-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="145f2-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
