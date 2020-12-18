---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/16/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 53038a02844fafc9550a6ac26303620a1a0183f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235182"
---
# <span data-ttu-id="fce4d-104">Домен схемы — протокол DevTools версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="fce4d-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="fce4d-105">Предоставляет сведения о схеме протокола.</span><span class="sxs-lookup"><span data-stu-id="fce4d-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="fce4d-106">Методы</span><span class="sxs-lookup"><span data-stu-id="fce4d-106">Methods</span></span>**](#methods) | [<span data-ttu-id="fce4d-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="fce4d-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="fce4d-108">Типы</span><span class="sxs-lookup"><span data-stu-id="fce4d-108">Types</span></span>**](#types) | [<span data-ttu-id="fce4d-109">Домен</span><span class="sxs-lookup"><span data-stu-id="fce4d-109">Domain</span></span>](#domain) |
## <span data-ttu-id="fce4d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="fce4d-110">Methods</span></span>

### <span data-ttu-id="fce4d-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="fce4d-111">getDomains</span></span>
<span data-ttu-id="fce4d-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="fce4d-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fce4d-113">Возвращает</span><span class="sxs-lookup"><span data-stu-id="fce4d-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fce4d-114">домены</span><span class="sxs-lookup"><span data-stu-id="fce4d-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="fce4d-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="fce4d-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="fce4d-116">Типы</span><span class="sxs-lookup"><span data-stu-id="fce4d-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="fce4d-117">Домен</span><span class="sxs-lookup"><span data-stu-id="fce4d-117">Domain</span></span> `object`

<span data-ttu-id="fce4d-118">Описание домена протокола.</span><span class="sxs-lookup"><span data-stu-id="fce4d-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="fce4d-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="fce4d-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="fce4d-120">name</span><span class="sxs-lookup"><span data-stu-id="fce4d-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fce4d-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="fce4d-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="fce4d-122">version</span><span class="sxs-lookup"><span data-stu-id="fce4d-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="fce4d-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="fce4d-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---
