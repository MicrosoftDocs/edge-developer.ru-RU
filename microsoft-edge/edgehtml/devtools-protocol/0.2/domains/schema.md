---
description: Ссылка на протокол DevTools Версии 0.2 (EdgeHTML) для домена Схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — версия протокола DevTools 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6844939f452bc96980d6d67d4652adcc7c078c7a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398149"
---
# <a name="schema-domain---devtools-protocol-version-02-edgehtml"></a><span data-ttu-id="d0179-104">Домен схемы — версия протокола DevTools 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="d0179-104">Schema Domain - DevTools Protocol Version 0.2 (EdgeHTML)</span></span>  

<span data-ttu-id="d0179-105">Предоставляет сведения о схеме протокола.</span><span class="sxs-lookup"><span data-stu-id="d0179-105">Provides information about the protocol schema.</span></span>  

| <span data-ttu-id="d0179-106">Категория</span><span class="sxs-lookup"><span data-stu-id="d0179-106">Classification</span></span> | <span data-ttu-id="d0179-107">Участники</span><span class="sxs-lookup"><span data-stu-id="d0179-107">Members</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="d0179-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d0179-108">Methods</span></span>](#methods) | [<span data-ttu-id="d0179-109">getDomains</span><span class="sxs-lookup"><span data-stu-id="d0179-109">getDomains</span></span>](#getdomains) |  
| [<span data-ttu-id="d0179-110">Типы</span><span class="sxs-lookup"><span data-stu-id="d0179-110">Types</span></span>](#types) | [<span data-ttu-id="d0179-111">Объект Domain</span><span class="sxs-lookup"><span data-stu-id="d0179-111">Domain object</span></span>](#domain) |  

## <a name="methods"></a><span data-ttu-id="d0179-112">Методы</span><span class="sxs-lookup"><span data-stu-id="d0179-112">Methods</span></span>  

### <a name="getdomains"></a><span data-ttu-id="d0179-113">getDomains</span><span class="sxs-lookup"><span data-stu-id="d0179-113">getDomains</span></span>  

<span data-ttu-id="d0179-114">Возвращает поддерживаемые домены.</span><span class="sxs-lookup"><span data-stu-id="d0179-114">Returns supported domains.</span></span>  

| <span data-ttu-id="d0179-115">Возвращает</span><span class="sxs-lookup"><span data-stu-id="d0179-115">Returns</span></span> | <span data-ttu-id="d0179-116">Тип</span><span class="sxs-lookup"><span data-stu-id="d0179-116">Type</span></span> | <span data-ttu-id="d0179-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="d0179-117">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0179-118">домены</span><span class="sxs-lookup"><span data-stu-id="d0179-118">domains</span></span> | [<span data-ttu-id="d0179-119">Домен[]</span><span class="sxs-lookup"><span data-stu-id="d0179-119">Domain[]</span></span>](#domain) | <span data-ttu-id="d0179-120">Список поддерживаемых доменов.</span><span class="sxs-lookup"><span data-stu-id="d0179-120">List of supported domains.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="d0179-121">Типы</span><span class="sxs-lookup"><span data-stu-id="d0179-121">Types</span></span>  

### <a name="domain-object"></a><span data-ttu-id="d0179-122">Объект Domain</span><span class="sxs-lookup"><span data-stu-id="d0179-122">Domain object</span></span>  

<a name="domain"></a>  

<span data-ttu-id="d0179-123">Описание домена протокола.</span><span class="sxs-lookup"><span data-stu-id="d0179-123">Description of the protocol domain.</span></span>  

| <span data-ttu-id="d0179-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0179-124">Properties</span></span> | <span data-ttu-id="d0179-125">Тип</span><span class="sxs-lookup"><span data-stu-id="d0179-125">Type</span></span> | <span data-ttu-id="d0179-126">Сведения</span><span class="sxs-lookup"><span data-stu-id="d0179-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0179-127">name</span><span class="sxs-lookup"><span data-stu-id="d0179-127">name</span></span> | `string` | <span data-ttu-id="d0179-128">Доменное имя.</span><span class="sxs-lookup"><span data-stu-id="d0179-128">Domain name.</span></span> |  
| <span data-ttu-id="d0179-129">version</span><span class="sxs-lookup"><span data-stu-id="d0179-129">version</span></span> | `string` | <span data-ttu-id="d0179-130">Версия домена.</span><span class="sxs-lookup"><span data-stu-id="d0179-130">Domain version.</span></span> |  

---  
