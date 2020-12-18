---
description: 'Атрибуты времени работы. '
title: JsRuntimeAttributes Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235426"
---
# <span data-ttu-id="48f2e-103">Перечисление JsRuntimeAttributes</span><span class="sxs-lookup"><span data-stu-id="48f2e-103">JsRuntimeAttributes Enumeration</span></span>

<span data-ttu-id="48f2e-104">Атрибуты времени работы.</span><span class="sxs-lookup"><span data-stu-id="48f2e-104">Attributes of a runtime.</span></span>  
  
## <span data-ttu-id="48f2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48f2e-105">Syntax</span></span>  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## <span data-ttu-id="48f2e-106">Members</span><span class="sxs-lookup"><span data-stu-id="48f2e-106">Members</span></span>  
  
### <span data-ttu-id="48f2e-107">Значения</span><span class="sxs-lookup"><span data-stu-id="48f2e-107">Values</span></span>  
  
|<span data-ttu-id="48f2e-108">Имя</span><span class="sxs-lookup"><span data-stu-id="48f2e-108">Name</span></span>|<span data-ttu-id="48f2e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="48f2e-109">Description</span></span>|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|<span data-ttu-id="48f2e-110">Время работы должно поддерживать надежное прерывание скриптов.</span><span class="sxs-lookup"><span data-stu-id="48f2e-110">The runtime should support reliable script interruption.</span></span> <span data-ttu-id="48f2e-111">Это увеличивает количество мест, в которых время выполнения будет проверять запрос на прерывание сценария за счет небольшой производительности времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="48f2e-111">This increases the number of places where the runtime will check for a script interrupt request at the cost of a small amount of runtime performance.</span></span>|  
|`JsRuntimeAttributeDisableBackgroundWork`|<span data-ttu-id="48f2e-112">В фоновых потоках не будет работать (например, сборка мусора).</span><span class="sxs-lookup"><span data-stu-id="48f2e-112">The runtime will not do any work (such as garbage collection) on background threads.</span></span>|  
|`JsRuntimeAttributeDisableEval`|<span data-ttu-id="48f2e-113">При `eval` использовании `function` или конструкторе будет выводиться исключение.</span><span class="sxs-lookup"><span data-stu-id="48f2e-113">Using `eval` or `function` constructor will throw an exception.</span></span>|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|<span data-ttu-id="48f2e-114">Во время работы не будет создаваться исходный код.</span><span class="sxs-lookup"><span data-stu-id="48f2e-114">Runtime will not generate native code.</span></span>|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|<span data-ttu-id="48f2e-115">В режиме запуска будут работать все экспериментальные функции.</span><span class="sxs-lookup"><span data-stu-id="48f2e-115">Runtime will enable all experimental features.</span></span>|  
|`JsRuntimeAttributeEnableIdleProcessing`|<span data-ttu-id="48f2e-116">Будет вызываться `JsIdle` хост, поэтому включается простаивающая обработка.</span><span class="sxs-lookup"><span data-stu-id="48f2e-116">Host will call `JsIdle`, so enable idle processing.</span></span> <span data-ttu-id="48f2e-117">В противном случае время работы будет управлять памятью немного более агрессивно.</span><span class="sxs-lookup"><span data-stu-id="48f2e-117">Otherwise, the runtime will manage memory slightly more aggressively.</span></span>|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|<span data-ttu-id="48f2e-118">Вызов также отправляет исключение отладильщику скрипта (при его найме), что дает возможность отладить `JsSetException` исключение.</span><span class="sxs-lookup"><span data-stu-id="48f2e-118">Calling `JsSetException` will also dispatch the exception to the script debugger (if any) giving the debugger a chance to break on the exception.</span></span>|  
|`JsRuntimeAttributeNone`|<span data-ttu-id="48f2e-119">Нет специальных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="48f2e-119">No special attributes.</span></span>|  
  
## <span data-ttu-id="48f2e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="48f2e-120">Requirements</span></span>  
 <span data-ttu-id="48f2e-121">**Заглавная:** jsrt.h</span><span class="sxs-lookup"><span data-stu-id="48f2e-121">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="48f2e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="48f2e-122">See Also</span></span>  
 [<span data-ttu-id="48f2e-123">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="48f2e-123">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
