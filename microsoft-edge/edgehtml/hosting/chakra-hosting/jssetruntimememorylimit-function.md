---
description: Задает текущий предел памяти для времени работы.
title: JsSetRuntimeMemoryLimit Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235112"
---
# <span data-ttu-id="1634b-103">Функция JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="1634b-103">JsSetRuntimeMemoryLimit Function</span></span>

<span data-ttu-id="1634b-104">Задает текущий предел памяти для времени работы.</span><span class="sxs-lookup"><span data-stu-id="1634b-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="1634b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1634b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="1634b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1634b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="1634b-107">Время работы, ограничение памяти которого необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="1634b-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="1634b-108">Новое ограничение памяти во время работы (в ветвях) или -1 (без ограничения памяти).</span><span class="sxs-lookup"><span data-stu-id="1634b-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="1634b-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="1634b-109">Return Value</span></span>  
 <span data-ttu-id="1634b-110">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="1634b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1634b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1634b-111">Remarks</span></span>  
 <span data-ttu-id="1634b-112">Ограничение памяти приведет к сбойу любой операции, которая превышает ограничение, из-за ошибки "из памяти".</span><span class="sxs-lookup"><span data-stu-id="1634b-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="1634b-113">Установка для времени работы ограничения памяти на -1 означает, что в среде работы нет предела памяти.</span><span class="sxs-lookup"><span data-stu-id="1634b-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="1634b-114">Новые потери памяти по умолчанию не ограничиваются.</span><span class="sxs-lookup"><span data-stu-id="1634b-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="1634b-115">Если новое ограничение памяти превышает текущий объем использования, вызов будет успешным, а любые будущие выделения в этой время будут невыполнена до тех пор, пока объем памяти в времени работы не опускается ниже предельного.</span><span class="sxs-lookup"><span data-stu-id="1634b-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="1634b-116">Ограничение памяти для времени работы всегда можно установить независимо от того, активна ли она в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="1634b-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="1634b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1634b-117">Requirements</span></span>  
 <span data-ttu-id="1634b-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="1634b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1634b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="1634b-119">See Also</span></span>  
 [<span data-ttu-id="1634b-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1634b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
