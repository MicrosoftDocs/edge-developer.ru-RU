---
description: Запускает отладку в текущем контексте.
title: JsStartDebugging Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235797"
---
# <span data-ttu-id="3f9c7-103">Функция JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="3f9c7-103">JsStartDebugging Function</span></span>

<span data-ttu-id="3f9c7-104">Запускает отладку в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="3f9c7-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="3f9c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f9c7-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="3f9c7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f9c7-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="3f9c7-107">Приложение отладки, которое будет использовать для отладки.</span><span class="sxs-lookup"><span data-stu-id="3f9c7-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="3f9c7-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3f9c7-108">Return Value</span></span>  
 <span data-ttu-id="3f9c7-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="3f9c7-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3f9c7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f9c7-110">Remarks</span></span>  
 <span data-ttu-id="3f9c7-111">Перед использованием этого API хост должен убедиться, что он вызван с помощью этого `CoInitializeEx` `COINIT_MULTITHREADED` `COINIT_APARTMENTTHREADED` API или хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="3f9c7-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="3f9c7-112">Параметр `debugApplication` не поддерживается в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3f9c7-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="3f9c7-113">Дополнительные сведения об использовании этого API в режиме Microsoft Edge см. в подразделе "Нацелив [Microsoft Edge на устаревшие движки".](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md)</span><span class="sxs-lookup"><span data-stu-id="3f9c7-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="3f9c7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3f9c7-114">Requirements</span></span>  
 <span data-ttu-id="3f9c7-115">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="3f9c7-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3f9c7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3f9c7-116">See Also</span></span>  
 [<span data-ttu-id="3f9c7-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3f9c7-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
