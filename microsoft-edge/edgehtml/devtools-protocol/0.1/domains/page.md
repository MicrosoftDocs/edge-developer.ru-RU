---
description: Ссылка на протокол DevTools Версии 0.1 (EdgeHTML) для домена Страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — Протокол DevTools Версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b04b0685a6b465d40e999a2a48d370573a3058d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399150"
---
# <a name="page-domain---devtools-protocol-version-01-edgehtml"></a><span data-ttu-id="f45cc-104">Домен страницы — Протокол DevTools Версии 0.1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f45cc-104">Page Domain - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

<span data-ttu-id="f45cc-105">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="f45cc-105">Actions and events related to the inspected page belong to the page domain.</span></span>  

| <span data-ttu-id="f45cc-106">Категория</span><span class="sxs-lookup"><span data-stu-id="f45cc-106">Classification</span></span> | <span data-ttu-id="f45cc-107">Участники</span><span class="sxs-lookup"><span data-stu-id="f45cc-107">Members</span></span> |  
|:--- |:--- |  
| [**<span data-ttu-id="f45cc-108">Методы</span><span class="sxs-lookup"><span data-stu-id="f45cc-108">Methods</span></span>**](#methods) | <span data-ttu-id="f45cc-109">[включить,](#enable) [отключить,](#disable) [перейти](#navigate)</span><span class="sxs-lookup"><span data-stu-id="f45cc-109">[enable](#enable), [disable](#disable), [navigate](#navigate)</span></span> |  
| [**<span data-ttu-id="f45cc-110">Типы</span><span class="sxs-lookup"><span data-stu-id="f45cc-110">Types</span></span>**](#types) | [<span data-ttu-id="f45cc-111">FrameId</span><span class="sxs-lookup"><span data-stu-id="f45cc-111">FrameId</span></span>](#frameid) |  

## <a name="methods"></a><span data-ttu-id="f45cc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f45cc-112">Methods</span></span>  

### <a name="enable"></a><span data-ttu-id="f45cc-113">"Включить"</span><span class="sxs-lookup"><span data-stu-id="f45cc-113">enable</span></span>  

<span data-ttu-id="f45cc-114">Включает уведомления домена страницы.</span><span class="sxs-lookup"><span data-stu-id="f45cc-114">Enables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="disable"></a><span data-ttu-id="f45cc-115">"Отключить" </span><span class="sxs-lookup"><span data-stu-id="f45cc-115">disable</span></span>  

<span data-ttu-id="f45cc-116">Отключение уведомлений домена страницы.</span><span class="sxs-lookup"><span data-stu-id="f45cc-116">Disables page domain notifications.</span></span>  

&nbsp;  

---  

### <a name="navigate"></a><span data-ttu-id="f45cc-117">переход</span><span class="sxs-lookup"><span data-stu-id="f45cc-117">navigate</span></span>  

<span data-ttu-id="f45cc-118">Перемещает текущую страницу на данный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f45cc-118">Navigates current page to the given URL.</span></span>  

| <span data-ttu-id="f45cc-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="f45cc-119">Parameters</span></span> | <span data-ttu-id="f45cc-120">Тип</span><span class="sxs-lookup"><span data-stu-id="f45cc-120">Type</span></span> | <span data-ttu-id="f45cc-121">Сведения</span><span class="sxs-lookup"><span data-stu-id="f45cc-121">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="f45cc-122">url</span><span class="sxs-lookup"><span data-stu-id="f45cc-122">url</span></span> | `string` | <span data-ttu-id="f45cc-123">URL-адрес для навигации по странице.</span><span class="sxs-lookup"><span data-stu-id="f45cc-123">URL to navigate the page to.</span></span> |  

| <span data-ttu-id="f45cc-124">Возвращает</span><span class="sxs-lookup"><span data-stu-id="f45cc-124">Returns</span></span> | <span data-ttu-id="f45cc-125">Тип</span><span class="sxs-lookup"><span data-stu-id="f45cc-125">Type</span></span> | <span data-ttu-id="f45cc-126">Сведения</span><span class="sxs-lookup"><span data-stu-id="f45cc-126">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="f45cc-127">frameId</span><span class="sxs-lookup"><span data-stu-id="f45cc-127">frameId</span></span> | [<span data-ttu-id="f45cc-128">FrameId</span><span class="sxs-lookup"><span data-stu-id="f45cc-128">FrameId</span></span>](#frameid) | <span data-ttu-id="f45cc-129">**Экспериментальные**.</span><span class="sxs-lookup"><span data-stu-id="f45cc-129">**Experimental**.</span></span>  <span data-ttu-id="f45cc-130">Frame ID, который будет перемещаться.</span><span class="sxs-lookup"><span data-stu-id="f45cc-130">Frame ID that will be navigated.</span></span> |  

---  

## <a name="types"></a><span data-ttu-id="f45cc-131">Типы</span><span class="sxs-lookup"><span data-stu-id="f45cc-131">Types</span></span>  

### <a name="frameid-string"></a><span data-ttu-id="f45cc-132">Строка FrameId</span><span class="sxs-lookup"><span data-stu-id="f45cc-132">FrameId string</span></span>  

<a name="frameid"></a>  

<span data-ttu-id="f45cc-133">Уникальный идентификатор кадра.</span><span class="sxs-lookup"><span data-stu-id="f45cc-133">Unique frame identifier.</span></span>  

&nbsp;  

---  
