---
description: Завершение вызова.
title: JsFinalizeCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235435"
---
# <span data-ttu-id="0d3f5-103">JsFinalizeCallback Typedef</span><span class="sxs-lookup"><span data-stu-id="0d3f5-103">JsFinalizeCallback Typedef</span></span>

<span data-ttu-id="0d3f5-104">Завершение вызова.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="0d3f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d3f5-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="0d3f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d3f5-106">Parameters</span></span>  
 <span data-ttu-id="0d3f5-107">data</span><span class="sxs-lookup"><span data-stu-id="0d3f5-107">data</span></span>  
 <span data-ttu-id="0d3f5-108">Внешние данные, которые были переданы при создании объекта, завершаемом.</span><span class="sxs-lookup"><span data-stu-id="0d3f5-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="0d3f5-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0d3f5-109">Requirements</span></span>  
 <span data-ttu-id="0d3f5-110">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="0d3f5-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0d3f5-111">См. также</span><span class="sxs-lookup"><span data-stu-id="0d3f5-111">See Also</span></span>  
 [<span data-ttu-id="0d3f5-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0d3f5-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
