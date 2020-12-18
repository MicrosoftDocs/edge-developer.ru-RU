---
description: Справка по домену наложения. Домен наложения предоставляет визуальные эффекты и взаимодействие при выборе узла
title: Домен наложения — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235186"
---
# <span data-ttu-id="4c0a0-104">Наложение</span><span class="sxs-lookup"><span data-stu-id="4c0a0-104">Overlay</span></span>

<span data-ttu-id="4c0a0-105">Домен наложения предоставляет визуальные эффекты и взаимодействие при выборе узла</span><span class="sxs-lookup"><span data-stu-id="4c0a0-105">Overlay domain exposes visual adornments and node selection interaction</span></span>

| | |
|-|-|
| [**<span data-ttu-id="4c0a0-106">Методы</span><span class="sxs-lookup"><span data-stu-id="4c0a0-106">Methods</span></span>**](#methods) | <span data-ttu-id="4c0a0-107">[enable,](#enable) [disable,](#disable) [setInspectMode](#setinspectmode)</span><span class="sxs-lookup"><span data-stu-id="4c0a0-107">[enable](#enable), [disable](#disable), [setInspectMode](#setinspectmode)</span></span> |
| [**<span data-ttu-id="4c0a0-108">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="4c0a0-108">Events</span></span>**](#events) | <span data-ttu-id="4c0a0-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span><span class="sxs-lookup"><span data-stu-id="4c0a0-109">[inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested)</span></span> |
| [**<span data-ttu-id="4c0a0-110">Зависимости</span><span class="sxs-lookup"><span data-stu-id="4c0a0-110">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="4c0a0-111">DOM</span><span class="sxs-lookup"><span data-stu-id="4c0a0-111">DOM</span></span>](dom.md) |
## <span data-ttu-id="4c0a0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="4c0a0-112">Methods</span></span>

### <span data-ttu-id="4c0a0-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="4c0a0-113">enable</span></span>
<span data-ttu-id="4c0a0-114">Включает отчеты о <code>nodeHighlightRequested</code> <code>inspectElementRequested</code> событиях и событиях</span><span class="sxs-lookup"><span data-stu-id="4c0a0-114">Enables reporting of <code>nodeHighlightRequested</code> and <code>inspectElementRequested</code> events</span></span>

</p>

---

### <span data-ttu-id="4c0a0-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="4c0a0-115">disable</span></span>
<span data-ttu-id="4c0a0-116">Отключает отчеты о событиях домена наложения</span><span class="sxs-lookup"><span data-stu-id="4c0a0-116">Disables reporting of Overlay domain events</span></span>

</p>

---

### <span data-ttu-id="4c0a0-117">setInspectMode</span><span class="sxs-lookup"><span data-stu-id="4c0a0-117">setInspectMode</span></span>
<span data-ttu-id="4c0a0-118">Задает режим выбора элементов для клиента</span><span class="sxs-lookup"><span data-stu-id="4c0a0-118">Sets the element selection mode for the client</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4c0a0-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c0a0-119">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4c0a0-120">mode</span><span class="sxs-lookup"><span data-stu-id="4c0a0-120">mode</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="4c0a0-121">Режим проверки.</span><span class="sxs-lookup"><span data-stu-id="4c0a0-121">The inspection mode.</span></span>  <span data-ttu-id="4c0a0-122">Допустимые значения: searchForNode и none.</span><span class="sxs-lookup"><span data-stu-id="4c0a0-122">Valid values are 'searchForNode' and 'none'.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="4c0a0-123">highlightConfig</span><span class="sxs-lookup"><span data-stu-id="4c0a0-123">highlightConfig</span></span> <br/> <i><span data-ttu-id="4c0a0-124">необязательные</span><span class="sxs-lookup"><span data-stu-id="4c0a0-124">optional</span></span></i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td><span data-ttu-id="4c0a0-125">Конфигурация выделения, используемая при проверке</span><span class="sxs-lookup"><span data-stu-id="4c0a0-125">The highlight configuration to use while inspecting</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="4c0a0-126">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="4c0a0-126">Events</span></span>

### <span data-ttu-id="4c0a0-127">inspectNodeRequested</span><span class="sxs-lookup"><span data-stu-id="4c0a0-127">inspectNodeRequested</span></span>
<span data-ttu-id="4c0a0-128">Сообщает клиенту, что пользователь запросит проверку определенного узла</span><span class="sxs-lookup"><span data-stu-id="4c0a0-128">Notifies the client that the user has asked to inspect a particular node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4c0a0-129">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c0a0-129">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4c0a0-130">backendNodeId</span><span class="sxs-lookup"><span data-stu-id="4c0a0-130">backendNodeId</span></span></td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td><span data-ttu-id="4c0a0-131">ИД запрашиваемого узла на тыловом узле</span><span class="sxs-lookup"><span data-stu-id="4c0a0-131">The backend node ID of node requested</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="4c0a0-132">nodeHighlightRequested</span><span class="sxs-lookup"><span data-stu-id="4c0a0-132">nodeHighlightRequested</span></span>
<span data-ttu-id="4c0a0-133">Указывает, что пользователь наведении курсор на узел и может проверить узел</span><span class="sxs-lookup"><span data-stu-id="4c0a0-133">Indicates that the user has hovered over the node and may inspect the node</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="4c0a0-134">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c0a0-134">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="4c0a0-135">nodeId</span><span class="sxs-lookup"><span data-stu-id="4c0a0-135">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td><span data-ttu-id="4c0a0-136">ИД узла, который рассматривается</span><span class="sxs-lookup"><span data-stu-id="4c0a0-136">The node ID of the node being considered</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="4c0a0-137">Зависимости</span><span class="sxs-lookup"><span data-stu-id="4c0a0-137">Dependencies</span></span>

[<span data-ttu-id="4c0a0-138">DOM</span><span class="sxs-lookup"><span data-stu-id="4c0a0-138">DOM</span></span>](dom.md)
