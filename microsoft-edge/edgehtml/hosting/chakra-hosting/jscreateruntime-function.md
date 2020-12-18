---
description: Создает новую time runtime.
title: JsCreateRuntime Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235523"
---
# <span data-ttu-id="e937c-103">Функция JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="e937c-103">JsCreateRuntime Function</span></span>

<span data-ttu-id="e937c-104">Создает новую time runtime.</span><span class="sxs-lookup"><span data-stu-id="e937c-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="e937c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e937c-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="e937c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e937c-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="e937c-107">Атрибуты создаемой времени работы.</span><span class="sxs-lookup"><span data-stu-id="e937c-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="e937c-108">Версия создаемой времени работы.</span><span class="sxs-lookup"><span data-stu-id="e937c-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="e937c-109">Служба потоков для времени работы.</span><span class="sxs-lookup"><span data-stu-id="e937c-109">The thread service for the runtime.</span></span> <span data-ttu-id="e937c-110">Может иметь null.</span><span class="sxs-lookup"><span data-stu-id="e937c-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="e937c-111">Созданная время работы.</span><span class="sxs-lookup"><span data-stu-id="e937c-111">The runtime created.</span></span>  
  
## <span data-ttu-id="e937c-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e937c-112">Return Value</span></span>  
 <span data-ttu-id="e937c-113">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="e937c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e937c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e937c-114">Remarks</span></span>  
 <span data-ttu-id="e937c-115">Параметр `version` не поддерживается в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e937c-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="e937c-116">Дополнительные сведения об использовании этого API в режиме Microsoft Edge см. в подразделе "Нацелив [Microsoft Edge на устаревшие движки".](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md)</span><span class="sxs-lookup"><span data-stu-id="e937c-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="e937c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e937c-117">Requirements</span></span>  
 <span data-ttu-id="e937c-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e937c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e937c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e937c-119">See Also</span></span>  
 [<span data-ttu-id="e937c-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e937c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
