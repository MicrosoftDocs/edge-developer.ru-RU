---
description: Ссылка на протокол DevTools Версии 0.1 (EdgeHTML) для домена Схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — Версия протокола DevTools 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e89f4269b4984ee49e83a23fcab9679485c49040
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398863"
---
# <a name="schema-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="6738f-104">Домен схемы — Версия протокола DevTools 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="6738f-104">Schema Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="6738f-105">Предоставляет сведения о схеме протокола.</span><span class="sxs-lookup"><span data-stu-id="6738f-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="6738f-106">Категория</span><span class="sxs-lookup"><span data-stu-id="6738f-106">Classification</span></span> | <span data-ttu-id="6738f-107">Участники</span><span class="sxs-lookup"><span data-stu-id="6738f-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="6738f-108">Методы</span><span class="sxs-lookup"><span data-stu-id="6738f-108">Methods</span></span>](#methods) | [<span data-ttu-id="6738f-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="6738f-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="6738f-110">Типы</span><span class="sxs-lookup"><span data-stu-id="6738f-110">Types</span></span>](#types) | [<span data-ttu-id="6738f-111">Домен</span><span class="sxs-lookup"><span data-stu-id="6738f-111">Domain</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="6738f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6738f-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="6738f-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="6738f-113">getDomains</span></span>  

<span data-ttu-id="6738f-114">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="6738f-114">Returns supported domains.</span></span>  

| <span data-ttu-id="6738f-115">Возвращает</span><span class="sxs-lookup"><span data-stu-id="6738f-115">Returns</span></span> | <span data-ttu-id="6738f-116">Тип</span><span class="sxs-lookup"><span data-stu-id="6738f-116">Type</span></span> | <span data-ttu-id="6738f-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="6738f-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="6738f-118">домены</span><span class="sxs-lookup"><span data-stu-id="6738f-118">domains</span></span> | [<span data-ttu-id="6738f-119">Домен[]</span><span class="sxs-lookup"><span data-stu-id="6738f-119">Domain[]</span></span>](#domain) | <span data-ttu-id="6738f-120">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="6738f-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="6738f-121">Типы</span><span class="sxs-lookup"><span data-stu-id="6738f-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="6738f-122">Объект Domain</span><span class="sxs-lookup"><span data-stu-id="6738f-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="6738f-123">Описание домена протокола.</span><span class="sxs-lookup"><span data-stu-id="6738f-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="6738f-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="6738f-124">Properties</span></span> | <span data-ttu-id="6738f-125">Тип</span><span class="sxs-lookup"><span data-stu-id="6738f-125">Type</span></span> | <span data-ttu-id="6738f-126">Сведения</span><span class="sxs-lookup"><span data-stu-id="6738f-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="6738f-127">name</span><span class="sxs-lookup"><span data-stu-id="6738f-127">name</span></span> | `string` | <span data-ttu-id="6738f-128">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="6738f-128">Domain name.</span></span> |  
| <span data-ttu-id="6738f-129">version</span><span class="sxs-lookup"><span data-stu-id="6738f-129">version</span></span> | `string` | <span data-ttu-id="6738f-130">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="6738f-130">Domain version.</span></span> |  

---  
