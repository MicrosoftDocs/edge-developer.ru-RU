---
description: Просмотр данных кэша с панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 770001beb9b7eebd4dae76355a1f3e41a8021ecb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230805"
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

# <span data-ttu-id="30c2a-104">Просмотр данных кэша с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="30c2a-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="30c2a-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки [данных кэша.][MDNCache]</span><span class="sxs-lookup"><span data-stu-id="30c2a-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="30c2a-106">Если вы пытаетесь проверить [данные кэша HTTP,][MDNHTTPCaching] это руководство вам не нужно.</span><span class="sxs-lookup"><span data-stu-id="30c2a-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="30c2a-107">Найдите сведения в столбце **"Размер"** **сетевого журнала.**</span><span class="sxs-lookup"><span data-stu-id="30c2a-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="30c2a-108">Перейдите в [журнал сетевой активности.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="30c2a-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="30c2a-109">Просмотр данных кэша</span><span class="sxs-lookup"><span data-stu-id="30c2a-109">View cache data</span></span>  

1.  <span data-ttu-id="30c2a-110">Выберите **вкладку "Приложение",** чтобы открыть **панель** приложений.</span><span class="sxs-lookup"><span data-stu-id="30c2a-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="30c2a-111">Обычно **по** умолчанию открывается окно манифеста.</span><span class="sxs-lookup"><span data-stu-id="30c2a-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="The Manifest pane" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="30c2a-113">The **Manifest** pane</span><span class="sxs-lookup"><span data-stu-id="30c2a-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-114">Раз развернуть раздел **"Хранилище кэша",** чтобы просмотреть доступные кэши.</span><span class="sxs-lookup"><span data-stu-id="30c2a-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Доступные кэши" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="30c2a-116">Доступные кэши</span><span class="sxs-lookup"><span data-stu-id="30c2a-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-117">Выберите кэш для просмотра содержимого.</span><span class="sxs-lookup"><span data-stu-id="30c2a-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Просмотр содержимого кэша" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="30c2a-119">Просмотр содержимого кэша</span><span class="sxs-lookup"><span data-stu-id="30c2a-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-120">Выберите ресурс, чтобы просмотреть http-заготки в разделе под таблицей.</span><span class="sxs-lookup"><span data-stu-id="30c2a-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Просмотр HTTP-загодеров ресурса" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="30c2a-122">Просмотр HTTP-загодеров ресурса</span><span class="sxs-lookup"><span data-stu-id="30c2a-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-123">Выберите **"Предварительный** просмотр", чтобы просмотреть содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="30c2a-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Просмотр содержимого ресурса" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="30c2a-125">Просмотр содержимого ресурса</span><span class="sxs-lookup"><span data-stu-id="30c2a-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="30c2a-126">Обновление ресурса</span><span class="sxs-lookup"><span data-stu-id="30c2a-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="30c2a-127">[Просмотр данных для кэша.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="30c2a-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="30c2a-128">Выберите ресурс, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="30c2a-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="30c2a-129">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="30c2a-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Выбор ресурса для обновления" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="30c2a-131">Выбор ресурса для обновления</span><span class="sxs-lookup"><span data-stu-id="30c2a-131">Select a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-132">Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="30c2a-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="30c2a-133">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="30c2a-133">Filter resources</span></span>  

1.  <span data-ttu-id="30c2a-134">[Просмотр данных для кэша.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="30c2a-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="30c2a-135">Используйте **текстовое поле "Фильтр** по пути", чтобы отфильтровать все ресурсы, которые не соответствуют предоставляемой вами пути.</span><span class="sxs-lookup"><span data-stu-id="30c2a-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Фильтрация ресурсов, которые не соответствуют указанному пути" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="30c2a-137">Фильтрация ресурсов, которые не соответствуют указанному пути</span><span class="sxs-lookup"><span data-stu-id="30c2a-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="30c2a-138">Удаление ресурса</span><span class="sxs-lookup"><span data-stu-id="30c2a-138">Delete a resource</span></span>  

1.  <span data-ttu-id="30c2a-139">[Просмотр данных для кэша.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="30c2a-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="30c2a-140">Выберите ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="30c2a-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="30c2a-141">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="30c2a-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Выбор ресурса для удаления" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="30c2a-143">Выбор ресурса для удаления</span><span class="sxs-lookup"><span data-stu-id="30c2a-143">Select a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-144">Choose **Delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="30c2a-144">Choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="30c2a-145">Удаление всех данных кэша</span><span class="sxs-lookup"><span data-stu-id="30c2a-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="30c2a-146">Откройте **приложение**  >  **"Очистить хранилище".**</span><span class="sxs-lookup"><span data-stu-id="30c2a-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="30c2a-147">Убедитесь, что включен **контрольный** ящик хранилища кэша.</span><span class="sxs-lookup"><span data-stu-id="30c2a-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="The Cache Storage checkbox" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="30c2a-149">The **Cache Storage checkbox**</span><span class="sxs-lookup"><span data-stu-id="30c2a-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="30c2a-150">Выберите **"Очистить данные сайта".**</span><span class="sxs-lookup"><span data-stu-id="30c2a-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Кнопка очистки данных сайта" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="30c2a-152">Кнопка **очистки данных** сайта</span><span class="sxs-lookup"><span data-stu-id="30c2a-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="30c2a-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="30c2a-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Запись сетевой активности | Документы Майкрософт"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэшинг HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="30c2a-158">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="30c2a-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="30c2a-159">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cache) находится здесь и автором является [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="30c2a-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="30c2a-161">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="30c2a-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
