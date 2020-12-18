---
description: Вызвано во время работы для загрузки исходный код сериализованного сценария. Вызывающая должна оставить буфер скрипта допустимым, пока не будет отсвеяна. `JsSerializedScriptUnloadCallback`
title: JsSerializedScriptLoadSourceCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235863"
---
# <span data-ttu-id="e4247-104">JsSerializedScriptLoadSourceCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="e4247-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>

<span data-ttu-id="e4247-105">Вызвано во время работы для загрузки исходный код сериализованного сценария.</span><span class="sxs-lookup"><span data-stu-id="e4247-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="e4247-106">Вызывающая должна оставить буфер скрипта допустимым, пока не будет отсвеяна. `JsSerializedScriptUnloadCallback`</span><span class="sxs-lookup"><span data-stu-id="e4247-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="e4247-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4247-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="e4247-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4247-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="e4247-109">Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="e4247-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="e4247-110">Сценарий возвращается.</span><span class="sxs-lookup"><span data-stu-id="e4247-110">The script returned.</span></span>  
  
## <span data-ttu-id="e4247-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4247-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="e4247-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e4247-112">Requirements</span></span>  
 <span data-ttu-id="e4247-113">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="e4247-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e4247-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e4247-114">See Also</span></span>  
 [<span data-ttu-id="e4247-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e4247-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
