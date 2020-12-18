---
description: Проект пространства имен WinRT.
title: JsProjectWinRTNamespace Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235869"
---
# <span data-ttu-id="6c79a-103">Функция JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="6c79a-103">JsProjectWinRTNamespace Function</span></span>

<span data-ttu-id="6c79a-104">Проект пространства имен WinRT.</span><span class="sxs-lookup"><span data-stu-id="6c79a-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="6c79a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c79a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="6c79a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c79a-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="6c79a-107">Пространство имен WinRT для проецируемых проектов.</span><span class="sxs-lookup"><span data-stu-id="6c79a-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="6c79a-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6c79a-108">Return Value</span></span>  
 <span data-ttu-id="6c79a-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="6c79a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6c79a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c79a-110">Remarks</span></span>  
 <span data-ttu-id="6c79a-111">Требуется активный контекст скрипта.</span><span class="sxs-lookup"><span data-stu-id="6c79a-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6c79a-112">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="6c79a-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6c79a-113">WinRT был именем платформы до универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="6c79a-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="6c79a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6c79a-114">Requirements</span></span>  
 <span data-ttu-id="6c79a-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="6c79a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6c79a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6c79a-116">See Also</span></span>  
 [<span data-ttu-id="6c79a-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6c79a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
