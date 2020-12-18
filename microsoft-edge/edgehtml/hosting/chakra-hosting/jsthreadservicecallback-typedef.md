---
description: Вызов службы потоков.
title: JsThreadServiceCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235456"
---
# <span data-ttu-id="0ec22-103">JsThreadServiceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="0ec22-103">JsThreadServiceCallback Typedef</span></span>

<span data-ttu-id="0ec22-104">Вызов службы потоков.</span><span class="sxs-lookup"><span data-stu-id="0ec22-104">A thread service callback.</span></span>  
  
## <span data-ttu-id="0ec22-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ec22-105">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### <span data-ttu-id="0ec22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ec22-106">Parameters</span></span>  
 <span data-ttu-id="0ec22-107">callback</span><span class="sxs-lookup"><span data-stu-id="0ec22-107">callback</span></span>  
 <span data-ttu-id="0ec22-108">Callback for the background work item.</span><span class="sxs-lookup"><span data-stu-id="0ec22-108">The callback for the background work item.</span></span>  
  
 <span data-ttu-id="0ec22-109">callbackData</span><span class="sxs-lookup"><span data-stu-id="0ec22-109">callbackData</span></span>  
 <span data-ttu-id="0ec22-110">Аргумент данных, который необходимо передать в callback.</span><span class="sxs-lookup"><span data-stu-id="0ec22-110">The data argument to be passed to the callback.</span></span>  
  
## <span data-ttu-id="0ec22-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ec22-111">Remarks</span></span>  
 <span data-ttu-id="0ec22-112">При вызове JsCreateRuntime хост может указать фоновую службу потоков.</span><span class="sxs-lookup"><span data-stu-id="0ec22-112">The host can specify a background thread service when calling JsCreateRuntime.</span></span> <span data-ttu-id="0ec22-113">Если этот элемент указан, элементы фоновой работы будут переданы на хост с помощью этого вызова.</span><span class="sxs-lookup"><span data-stu-id="0ec22-113">If specified, then background work items will be passed to the host using this callback.</span></span> <span data-ttu-id="0ec22-114">Ожидается, что хост начнет немедленно выполнять фоновый рабочий элемент и возвращать true или возвращать false, а время выполнения обрабатывает рабочий элемент в потоке.</span><span class="sxs-lookup"><span data-stu-id="0ec22-114">The host is expected to either begin executing the background work item immediately and return true or return false and the runtime will handle the work item in-thread.</span></span>  
  
## <span data-ttu-id="0ec22-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0ec22-115">Requirements</span></span>  
 <span data-ttu-id="0ec22-116">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="0ec22-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0ec22-117">См. также</span><span class="sxs-lookup"><span data-stu-id="0ec22-117">See Also</span></span>  
 [<span data-ttu-id="0ec22-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0ec22-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
