---
description: Просмотр данных кэша из панели приложений Microsoft Edge DevTools.
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0ce4dbbf2456579abe84fca48bca8106384995dd
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439319"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="c8897-104">Просмотр данных кэша с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c8897-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c8897-105">В этом руководстве показано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки [данных кэша.][MDNCache]</span><span class="sxs-lookup"><span data-stu-id="c8897-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="c8897-106">Если вы пытаетесь проверить [данные кэша HTTP,][MDNHTTPCaching] это не нужное руководство.</span><span class="sxs-lookup"><span data-stu-id="c8897-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="c8897-107">Сведения в столбце **Размер** сетевого журнала **.**</span><span class="sxs-lookup"><span data-stu-id="c8897-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="c8897-108">Перейдите к [сетевой активности журнала][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="c8897-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <a name="view-cache-data"></a><span data-ttu-id="c8897-109">Просмотр данных кэша</span><span class="sxs-lookup"><span data-stu-id="c8897-109">View cache data</span></span>  

1.  <span data-ttu-id="c8897-110">Выберите **вкладку Application** для открытия панели **приложения.**</span><span class="sxs-lookup"><span data-stu-id="c8897-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="c8897-111">Обычно **области Манифеста** открываются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c8897-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Области Манифест" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="c8897-113">Области **Манифест**</span><span class="sxs-lookup"><span data-stu-id="c8897-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-114">**Расширь раздел Хранилища кэша,** чтобы просмотреть доступные кэши.</span><span class="sxs-lookup"><span data-stu-id="c8897-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Доступные кэши" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="c8897-116">Доступные кэши</span><span class="sxs-lookup"><span data-stu-id="c8897-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-117">Выберите кэш для просмотра содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8897-117">Choose a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Просмотр содержимого кэша" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="c8897-119">Просмотр содержимого кэша</span><span class="sxs-lookup"><span data-stu-id="c8897-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-120">Выберите ресурс для просмотра заглавных таблиц HTTP в разделе под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c8897-120">Choose a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Просмотр http-заглавных окей ресурса" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="c8897-122">Просмотр http-заглавных окей ресурса</span><span class="sxs-lookup"><span data-stu-id="c8897-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-123">Выберите **Предварительный** просмотр, чтобы просмотреть содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8897-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Просмотр содержимого ресурса" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="c8897-125">Просмотр содержимого ресурса</span><span class="sxs-lookup"><span data-stu-id="c8897-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a><span data-ttu-id="c8897-126">Обновление ресурса</span><span class="sxs-lookup"><span data-stu-id="c8897-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="c8897-127">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c8897-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c8897-128">Выберите ресурс, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="c8897-128">Choose the resource that you want to refresh.</span></span>  <span data-ttu-id="c8897-129">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="c8897-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Выберите ресурс для обновления" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="c8897-131">Выберите ресурс для обновления</span><span class="sxs-lookup"><span data-stu-id="c8897-131">Choose a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-132">Выберите **обновление** \. ![ Обновление ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c8897-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-resources"></a><span data-ttu-id="c8897-133">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8897-133">Filter resources</span></span>  

1.  <span data-ttu-id="c8897-134">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c8897-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c8897-135">Используйте **текстовое поле Filter by Path,** чтобы отфильтровать все ресурсы, которые не соответствуют пути, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="c8897-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Фильтрация ресурсов, не совпадает с указанным путем" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="c8897-137">Фильтрация ресурсов, не совпадает с указанным путем</span><span class="sxs-lookup"><span data-stu-id="c8897-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <a name="delete-a-resource"></a><span data-ttu-id="c8897-138">Удаление ресурса</span><span class="sxs-lookup"><span data-stu-id="c8897-138">Delete a resource</span></span>  

1.  <span data-ttu-id="c8897-139">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="c8897-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="c8897-140">Выберите ресурс, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c8897-140">Choose the resource that you want to delete.</span></span>  <span data-ttu-id="c8897-141">DevTools выделяет его, чтобы указать, что он выбран.</span><span class="sxs-lookup"><span data-stu-id="c8897-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Выбор ресурса для удаления" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="c8897-143">Выбор ресурса для удаления</span><span class="sxs-lookup"><span data-stu-id="c8897-143">Choose a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-144">Выберите **Удалить выбранный** \. ![ Удалить выбранный ](../media/delete-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c8897-144">Choose **Delete Selected** \(![Delete Selected](../media/delete-icon.msft.png)\).</span></span>  
    
## <a name="delete-all-cache-data"></a><span data-ttu-id="c8897-145">Удаление всех данных кэша</span><span class="sxs-lookup"><span data-stu-id="c8897-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="c8897-146">Open **Application**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="c8897-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="c8897-147">Убедитесь, что включен **почтовый ящик хранения** кэша.</span><span class="sxs-lookup"><span data-stu-id="c8897-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Почтовый ящик хранения кэша" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="c8897-149">Почтовый **ящик хранения кэша**</span><span class="sxs-lookup"><span data-stu-id="c8897-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c8897-150">Выберите **четкие данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="c8897-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Кнопка Clear Site Data" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="c8897-152">Кнопка **Clear Site Data**</span><span class="sxs-lookup"><span data-stu-id="c8897-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c8897-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c8897-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Журнал сетевой активности | Документы Майкрософт"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Http кэш | MDN"  

> [!NOTE]
> <span data-ttu-id="c8897-158">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8897-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c8897-159">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/storage/cache) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="c8897-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c8897-161">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c8897-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
