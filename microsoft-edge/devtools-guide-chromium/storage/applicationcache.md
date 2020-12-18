---
description: Просмотр данных кэша приложений с панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша приложений с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3d73047a8332e4d6cae5f7411f968a7dfe4c3738
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230784"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="1ab17-104">Просмотр данных кэша приложений с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1ab17-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="1ab17-105">API кэша приложений удаляется [с веб-платформы.][HTMLStandardOfflineWebApplications]</span><span class="sxs-lookup"><span data-stu-id="1ab17-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="1ab17-106">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки ресурсов [кэша][MDNWebAPIsWindowApplicationCache] приложений.</span><span class="sxs-lookup"><span data-stu-id="1ab17-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="1ab17-107">Просмотр данных кэша приложений</span><span class="sxs-lookup"><span data-stu-id="1ab17-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="1ab17-108">Выберите **вкладку "Источники",** чтобы открыть панель **источников.**</span><span class="sxs-lookup"><span data-stu-id="1ab17-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="1ab17-109">Обычно **по** умолчанию открывается окно манифеста.</span><span class="sxs-lookup"><span data-stu-id="1ab17-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="1ab17-111">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="1ab17-111">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="1ab17-112">Раз expand **the Application Cache** section and choose a cache to view the resources.</span><span class="sxs-lookup"><span data-stu-id="1ab17-112">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="The Application Cache pane" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="1ab17-114">The **Application Cache** pane</span><span class="sxs-lookup"><span data-stu-id="1ab17-114">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="1ab17-115">Каждая строка таблицы представляет кэшный ресурс.</span><span class="sxs-lookup"><span data-stu-id="1ab17-115">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="1ab17-116">Столбец **"Тип"** представляет [категорию ресурса.][MDNHTMLResourcesInAnApplicationCache]</span><span class="sxs-lookup"><span data-stu-id="1ab17-116">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="1ab17-117">Категория</span><span class="sxs-lookup"><span data-stu-id="1ab17-117">Category</span></span> | <span data-ttu-id="1ab17-118">Сведения</span><span class="sxs-lookup"><span data-stu-id="1ab17-118">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="1ab17-119">Этот ресурс был явно указан в манифесте.</span><span class="sxs-lookup"><span data-stu-id="1ab17-119">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="1ab17-120">URL-адрес является откатом для другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ab17-120">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="1ab17-121">URL-адрес другого ресурса не указан в DevTools.</span><span class="sxs-lookup"><span data-stu-id="1ab17-121">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="1ab17-122">Атрибут ресурса указывает, что кэш `manifest` является родительским для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1ab17-122">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="1ab17-123">Манифест указывает, что ресурс должен быть источником из сети.</span><span class="sxs-lookup"><span data-stu-id="1ab17-123">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="1ab17-124">В нижней части таблицы находятся значки состояния, указывающие сетевое подключение и состояние **кэша приложений.**</span><span class="sxs-lookup"><span data-stu-id="1ab17-124">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="1ab17-125">Кэш **приложений может** иметь следующие состояния.</span><span class="sxs-lookup"><span data-stu-id="1ab17-125">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="1ab17-126">Состояние</span><span class="sxs-lookup"><span data-stu-id="1ab17-126">State</span></span> | <span data-ttu-id="1ab17-127">Сведения</span><span class="sxs-lookup"><span data-stu-id="1ab17-127">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="1ab17-128">Манифест извлекется и проверяется на наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="1ab17-128">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="1ab17-129">Ресурсы добавляются в кэш.</span><span class="sxs-lookup"><span data-stu-id="1ab17-129">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="1ab17-130">В кэше нет новых изменений.</span><span class="sxs-lookup"><span data-stu-id="1ab17-130">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="1ab17-131">Кэш удаляется.</span><span class="sxs-lookup"><span data-stu-id="1ab17-131">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="1ab17-132">Доступна новая версия кэша.</span><span class="sxs-lookup"><span data-stu-id="1ab17-132">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Автономные веб-приложения — HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ресурсы в кэше приложений | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache — веб-API | MDN"  

> [!NOTE]
> <span data-ttu-id="1ab17-137">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ab17-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1ab17-138">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="1ab17-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1ab17-140">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1ab17-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
