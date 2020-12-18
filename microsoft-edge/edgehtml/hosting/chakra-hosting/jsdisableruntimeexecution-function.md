---
description: Приостанавливать выполнение сценариев и прерывать все запущенные сценарии в реализации.
title: JsDisableRuntimeExecution Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235505"
---
# <span data-ttu-id="4af0b-103">Функция JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="4af0b-103">JsDisableRuntimeExecution Function</span></span>

<span data-ttu-id="4af0b-104">Приостанавливать выполнение сценариев и прерывать все запущенные сценарии в реализации.</span><span class="sxs-lookup"><span data-stu-id="4af0b-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="4af0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4af0b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="4af0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4af0b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="4af0b-107">Приостановка времени работы.</span><span class="sxs-lookup"><span data-stu-id="4af0b-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="4af0b-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4af0b-108">Return Value</span></span>  
 <span data-ttu-id="4af0b-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="4af0b-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4af0b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4af0b-110">Remarks</span></span>  
 <span data-ttu-id="4af0b-111">Вызовы приостановленной времени работы будут неудались до тех пор, `JsEnableRuntimeExecution` пока не будут вызваны.</span><span class="sxs-lookup"><span data-stu-id="4af0b-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="4af0b-112">Этот API не должен быть вызван в потоке, в который активно время работы.</span><span class="sxs-lookup"><span data-stu-id="4af0b-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="4af0b-113">Хотя время выполнения будет приостановлено, выполнение сценария может быть приостановлено не сразу; Запущенный сценарий будет как можно скорее завершен с помощью неуявяемого исключения.</span><span class="sxs-lookup"><span data-stu-id="4af0b-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="4af0b-114">Приостановка выполнения в уже приостановленной времени выполнения не является действием.</span><span class="sxs-lookup"><span data-stu-id="4af0b-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="4af0b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4af0b-115">Requirements</span></span>  
 <span data-ttu-id="4af0b-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="4af0b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4af0b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4af0b-117">See Also</span></span>  
 [<span data-ttu-id="4af0b-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4af0b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
