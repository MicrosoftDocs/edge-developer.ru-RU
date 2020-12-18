---
description: Вызвано во время выполнения после завершения работы со всеми ресурсами, связанными с выполнением сценария. В настоящее время вызываемая служба должна освободить источник, код ветвей и контекст.
title: JsSerializedScriptUnloadCallback typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235813"
---
# <span data-ttu-id="edd0c-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="edd0c-104">JsSerializedScriptUnloadCallback typedef</span></span>

<span data-ttu-id="edd0c-105">Вызвано во время выполнения после завершения работы со всеми ресурсами, связанными с выполнением сценария.</span><span class="sxs-lookup"><span data-stu-id="edd0c-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="edd0c-106">В настоящее время вызываемая служба должна освободить источник, код для byte и контекст.</span><span class="sxs-lookup"><span data-stu-id="edd0c-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="edd0c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edd0c-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="edd0c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edd0c-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="edd0c-109">Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="edd0c-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="edd0c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="edd0c-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="edd0c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="edd0c-111">Requirements</span></span>  
 <span data-ttu-id="edd0c-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="edd0c-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="edd0c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="edd0c-113">See Also</span></span>  
 [<span data-ttu-id="edd0c-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="edd0c-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
