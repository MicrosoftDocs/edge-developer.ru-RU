---
description: Справочник по домену DOMDebugger. Отладка DOM позволяет устанавливать точки останова для определенных операций и событий DOM. Выполнение JavaScript остановится для этих операций, как если бы был установлен обычный набор точек останова.
title: Домен DOMDebugger — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235188"
---
# <span data-ttu-id="7001b-105">DOMDebugger</span><span class="sxs-lookup"><span data-stu-id="7001b-105">DOMDebugger</span></span>

<span data-ttu-id="7001b-106">Отладка DOM позволяет устанавливать точки останова для определенных операций и событий DOM.</span><span class="sxs-lookup"><span data-stu-id="7001b-106">DOM debugging allows setting breakpoints on particular DOM operations and events.</span></span> <span data-ttu-id="7001b-107">Выполнение JavaScript остановится для этих операций, как если бы был установлен обычный набор точек останова.</span><span class="sxs-lookup"><span data-stu-id="7001b-107">JavaScript execution will stop on these operations as if there was a regular breakpoint set.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="7001b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7001b-108">Methods</span></span>**](#methods) | <span data-ttu-id="7001b-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span><span class="sxs-lookup"><span data-stu-id="7001b-109">[setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint)</span></span> |
## <span data-ttu-id="7001b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="7001b-110">Methods</span></span>

### <span data-ttu-id="7001b-111">setInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="7001b-111">setInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="7001b-112">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7001b-112">Experimental.</span></span> </b></span><span data-ttu-id="7001b-113">Задает точку останова для конкретного события.</span><span class="sxs-lookup"><span data-stu-id="7001b-113">Sets a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7001b-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="7001b-114">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7001b-115">eventName</span><span class="sxs-lookup"><span data-stu-id="7001b-115">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7001b-116">Имя инструмента для остановки.</span><span class="sxs-lookup"><span data-stu-id="7001b-116">Instrumentation name to stop on.</span></span> <span data-ttu-id="7001b-117">Допустимые значения: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="7001b-117">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="7001b-118">removeInstrumentationBreakpoint</span><span class="sxs-lookup"><span data-stu-id="7001b-118">removeInstrumentationBreakpoint</span></span>
<span><b><span data-ttu-id="7001b-119">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="7001b-119">Experimental.</span></span> </b></span><span data-ttu-id="7001b-120">Удаляет точку останова для определенного события.</span><span class="sxs-lookup"><span data-stu-id="7001b-120">Removes a breakpoint on a particular native event.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="7001b-121">Параметры</span><span class="sxs-lookup"><span data-stu-id="7001b-121">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="7001b-122">eventName</span><span class="sxs-lookup"><span data-stu-id="7001b-122">eventName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="7001b-123">Имя инструмента для остановки.</span><span class="sxs-lookup"><span data-stu-id="7001b-123">Instrumentation name to stop on.</span></span> <span data-ttu-id="7001b-124">Допустимые значения: 'scriptFirstStatement'.</span><span class="sxs-lookup"><span data-stu-id="7001b-124">Valid values: 'scriptFirstStatement'.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
