---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235577"
---
# <span data-ttu-id="8fa58-104">Домен страницы — протокол DevTools версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8fa58-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="8fa58-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="8fa58-105">Actions and events related to the inspected page belong to the page domain.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="8fa58-106">Методы</span><span class="sxs-lookup"><span data-stu-id="8fa58-106">Methods</span></span>**](#methods) | <span data-ttu-id="8fa58-107">[включить,](#enable) [отключить,](#disable) [перейти](#navigate)</span><span class="sxs-lookup"><span data-stu-id="8fa58-107">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |
| [**<span data-ttu-id="8fa58-108">Типы</span><span class="sxs-lookup"><span data-stu-id="8fa58-108">Types</span></span>**](#types) | [<span data-ttu-id="8fa58-109">FrameId</span><span class="sxs-lookup"><span data-stu-id="8fa58-109">FrameId</span></span>](#frameid) |
## <span data-ttu-id="8fa58-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8fa58-110">Methods</span></span>

### <span data-ttu-id="8fa58-111">"Включить"</span><span class="sxs-lookup"><span data-stu-id="8fa58-111">enable</span></span>
<span data-ttu-id="8fa58-112">Включает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="8fa58-112">Enables page domain notifications.</span></span>


---

### <span data-ttu-id="8fa58-113">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="8fa58-113">disable</span></span>
<span data-ttu-id="8fa58-114">Отключает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="8fa58-114">Disables page domain notifications.</span></span>


---

### <span data-ttu-id="8fa58-115">переход</span><span class="sxs-lookup"><span data-stu-id="8fa58-115">navigate</span></span>
<span data-ttu-id="8fa58-116">Переходит на текущую страницу по заданным URL-адресам.</span><span class="sxs-lookup"><span data-stu-id="8fa58-116">Navigates current page to the given URL.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8fa58-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fa58-117">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8fa58-118">url</span><span class="sxs-lookup"><span data-stu-id="8fa58-118">url</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="8fa58-119">URL-адрес для навигации по странице.</span><span class="sxs-lookup"><span data-stu-id="8fa58-119">URL to navigate the page to.</span></span></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="8fa58-120">Возвращает</span><span class="sxs-lookup"><span data-stu-id="8fa58-120">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="8fa58-121">frameId</span><span class="sxs-lookup"><span data-stu-id="8fa58-121">frameId</span></span></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b><span data-ttu-id="8fa58-122">Экспериментальная.</span><span class="sxs-lookup"><span data-stu-id="8fa58-122">Experimental.</span></span> </b></span><span data-ttu-id="8fa58-123">ИД кадра, который будет перемещаться.</span><span class="sxs-lookup"><span data-stu-id="8fa58-123">Frame id that will be navigated.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="8fa58-124">Типы</span><span class="sxs-lookup"><span data-stu-id="8fa58-124">Types</span></span>

### <a name="frameid"></a> <span data-ttu-id="8fa58-125">FrameId</span><span class="sxs-lookup"><span data-stu-id="8fa58-125">FrameId</span></span> `string`

<span data-ttu-id="8fa58-126">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="8fa58-126">Unique frame identifier.</span></span>


---
