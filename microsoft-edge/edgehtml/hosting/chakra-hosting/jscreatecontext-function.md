---
description: Создает контекст сценария для запуска сценариев.
title: JsCreateContext Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235304"
---
# <span data-ttu-id="6f021-103">Функция JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="6f021-103">JsCreateContext Function</span></span>

<span data-ttu-id="6f021-104">Создает контекст сценария для запуска сценариев.</span><span class="sxs-lookup"><span data-stu-id="6f021-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="6f021-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f021-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="6f021-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f021-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="6f021-107">Время запуска, в котором создается контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="6f021-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="6f021-108">Приложение отладки, которое будет использовать для отладки.</span><span class="sxs-lookup"><span data-stu-id="6f021-108">The debug application to use for debugging.</span></span> <span data-ttu-id="6f021-109">Этот параметр может иметь null, в этом случае отладка для контекста не включена.</span><span class="sxs-lookup"><span data-stu-id="6f021-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="6f021-110">Контекст созданного сценария.</span><span class="sxs-lookup"><span data-stu-id="6f021-110">The created script context.</span></span>  
  
## <span data-ttu-id="6f021-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6f021-111">Return Value</span></span>  
 <span data-ttu-id="6f021-112">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="6f021-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6f021-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f021-113">Remarks</span></span>  
 <span data-ttu-id="6f021-114">Каждый контекст сценария имеет собственный глобальный объект, изолированный от всех остальных контекстов сценария.</span><span class="sxs-lookup"><span data-stu-id="6f021-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="6f021-115">Параметр `debugApplication` не поддерживается в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6f021-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="6f021-116">Дополнительные сведения об использовании этого API в режиме Microsoft Edge см. в подразделе "Нацелив [Microsoft Edge на устаревшие движки".](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md)</span><span class="sxs-lookup"><span data-stu-id="6f021-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="6f021-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6f021-117">Requirements</span></span>  
 <span data-ttu-id="6f021-118">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="6f021-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6f021-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6f021-119">See Also</span></span>  
 [<span data-ttu-id="6f021-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6f021-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
