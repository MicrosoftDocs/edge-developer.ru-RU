---
description: 'Включает выполнение скрипта в время выполнения. '
title: JsEnableRuntimeExecution Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235502"
---
# <span data-ttu-id="36969-103">Функция JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="36969-103">JsEnableRuntimeExecution Function</span></span>

<span data-ttu-id="36969-104">Включает выполнение скрипта в время выполнения.</span><span class="sxs-lookup"><span data-stu-id="36969-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="36969-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36969-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="36969-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36969-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="36969-107">Время запуска, который необходимо включить.</span><span class="sxs-lookup"><span data-stu-id="36969-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="36969-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="36969-108">Return Value</span></span>  
 <span data-ttu-id="36969-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="36969-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="36969-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36969-110">Remarks</span></span>  
 <span data-ttu-id="36969-111">Включение выполнения сценария в время выполнения, где уже включено выполнение скрипта, не является работой.</span><span class="sxs-lookup"><span data-stu-id="36969-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="36969-112">Требования</span><span class="sxs-lookup"><span data-stu-id="36969-112">Requirements</span></span>  
 <span data-ttu-id="36969-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="36969-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="36969-114">См. также</span><span class="sxs-lookup"><span data-stu-id="36969-114">See Also</span></span>  
 [<span data-ttu-id="36969-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="36969-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
