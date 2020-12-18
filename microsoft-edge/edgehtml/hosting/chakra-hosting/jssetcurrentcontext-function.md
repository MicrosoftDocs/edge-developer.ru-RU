---
description: Задает текущий контекст сценария в потоке.
title: JsSetCurrentContext Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235462"
---
# <span data-ttu-id="47590-103">Функция JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="47590-103">JsSetCurrentContext Function</span></span>

<span data-ttu-id="47590-104">Задает текущий контекст сценария в потоке.</span><span class="sxs-lookup"><span data-stu-id="47590-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="47590-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47590-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="47590-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47590-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="47590-107">Контекст сценария, который необходимо внести в текущий момент.</span><span class="sxs-lookup"><span data-stu-id="47590-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="47590-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="47590-108">Return Value</span></span>  
 <span data-ttu-id="47590-109">Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.</span><span class="sxs-lookup"><span data-stu-id="47590-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="47590-110">Пример.</span><span class="sxs-lookup"><span data-stu-id="47590-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="47590-111">Требования</span><span class="sxs-lookup"><span data-stu-id="47590-111">Requirements</span></span>  
 <span data-ttu-id="47590-112">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="47590-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="47590-113">См. также</span><span class="sxs-lookup"><span data-stu-id="47590-113">See Also</span></span>  
 [<span data-ttu-id="47590-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="47590-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
