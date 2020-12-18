---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235570"
---
# <span data-ttu-id="bc23a-104">Домен схемы — протокол DevTools версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="bc23a-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="bc23a-105">Предоставляет сведения о схеме протокола.</span><span class="sxs-lookup"><span data-stu-id="bc23a-105">Provides information about the protocol schema.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="bc23a-106">Методы</span><span class="sxs-lookup"><span data-stu-id="bc23a-106">Methods</span></span>**](#methods) | [<span data-ttu-id="bc23a-107">getDomains</span><span class="sxs-lookup"><span data-stu-id="bc23a-107">getDomains</span></span>](#getdomains) |
| [**<span data-ttu-id="bc23a-108">Типы</span><span class="sxs-lookup"><span data-stu-id="bc23a-108">Types</span></span>**](#types) | [<span data-ttu-id="bc23a-109">Домен</span><span class="sxs-lookup"><span data-stu-id="bc23a-109">Domain</span></span>](#domain) |
## <span data-ttu-id="bc23a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="bc23a-110">Methods</span></span>

### <span data-ttu-id="bc23a-111">getDomains</span><span class="sxs-lookup"><span data-stu-id="bc23a-111">getDomains</span></span>
<span data-ttu-id="bc23a-112">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="bc23a-112">Returns supported domains.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bc23a-113">Возвращает</span><span class="sxs-lookup"><span data-stu-id="bc23a-113">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bc23a-114">домены</span><span class="sxs-lookup"><span data-stu-id="bc23a-114">domains</span></span></td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td><span data-ttu-id="bc23a-115">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="bc23a-115">List of supported domains.</span></span></td>
        </tr>
    </tbody>
</table>

---

## <span data-ttu-id="bc23a-116">Типы</span><span class="sxs-lookup"><span data-stu-id="bc23a-116">Types</span></span>

### <a name="domain"></a> <span data-ttu-id="bc23a-117">Домен</span><span class="sxs-lookup"><span data-stu-id="bc23a-117">Domain</span></span> `object`

<span data-ttu-id="bc23a-118">Описание домена протокола.</span><span class="sxs-lookup"><span data-stu-id="bc23a-118">Description of the protocol domain.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="bc23a-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc23a-119">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="bc23a-120">name</span><span class="sxs-lookup"><span data-stu-id="bc23a-120">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bc23a-121">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="bc23a-121">Domain name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="bc23a-122">version</span><span class="sxs-lookup"><span data-stu-id="bc23a-122">version</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="bc23a-123">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="bc23a-123">Domain version.</span></span></td>
        </tr>
    </tbody>
</table>

---
