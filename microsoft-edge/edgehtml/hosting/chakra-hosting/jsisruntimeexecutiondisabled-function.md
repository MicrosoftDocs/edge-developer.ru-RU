---
description: Возвращает значение, которое указывает, отключено ли выполнение сценария во время выполнения.
title: JsIsRuntimeExecutionDisabled Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235126"
---
# <span data-ttu-id="de637-103">Функция JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="de637-103">JsIsRuntimeExecutionDisabled Function</span></span>

<span data-ttu-id="de637-104">Возвращает значение, которое указывает, отключено ли выполнение сценария во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="de637-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="de637-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de637-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="de637-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de637-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="de637-107">Указывает времени выполнения, чтобы проверить, отключено ли выполнение.</span><span class="sxs-lookup"><span data-stu-id="de637-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="de637-108">если выполнение отключено, `false` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="de637-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="de637-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="de637-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="de637-110">если операция прошла успешно, код сбоя в противном случае.</span><span class="sxs-lookup"><span data-stu-id="de637-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="de637-111">Требования</span><span class="sxs-lookup"><span data-stu-id="de637-111">Requirements</span></span>  
 <span data-ttu-id="de637-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="de637-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="de637-113">См. также</span><span class="sxs-lookup"><span data-stu-id="de637-113">See Also</span></span>  
 [<span data-ttu-id="de637-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="de637-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
