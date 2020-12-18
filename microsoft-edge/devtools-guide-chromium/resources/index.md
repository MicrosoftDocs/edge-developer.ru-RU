---
description: Упорядодрять ресурсы по кадру, домену, типу или другим критериям.
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 353c36a9d98dac287c3fdaaa3feed2fe3b17cd07
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230777"
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

# <span data-ttu-id="dd753-104">Просмотр ресурсов страниц с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dd753-104">View page resources with Microsoft Edge DevTools</span></span>  

  

<span data-ttu-id="dd753-105">В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="dd753-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="dd753-106">Ресурсы — это файлы, необходимые странице для правильного отображения.</span><span class="sxs-lookup"><span data-stu-id="dd753-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="dd753-107">Примеры ресурсов: CSS, JavaScript и HTML-файлы, а также изображения.</span><span class="sxs-lookup"><span data-stu-id="dd753-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="dd753-108">В этом руководстве предполагается, что [][MDNLearnWebDevelopment] вы знакомы с основами веб-разработки и [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="dd753-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="dd753-109">Открытие ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd753-109">Open resources</span></span>  

<span data-ttu-id="dd753-110">Если вы знаете имя ресурса, который нужно \*\*\*\* проверить, меню команд обеспечивает быстрый способ открытия ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd753-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="dd753-111">Выберите `Control` + `P` \(Windows, Linux\) или `Command` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="dd753-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="dd753-112">Откроется **диалоговое окно** "Открыть файл".</span><span class="sxs-lookup"><span data-stu-id="dd753-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно "Открыть файл"" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="dd753-114">Диалоговое **окно "Открыть** файл"</span><span class="sxs-lookup"><span data-stu-id="dd753-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dd753-115">Выберите файл в выпадаемом окне или начните вводить имя файла и выберите его после выделения нужного файла в поле `Enter` автозаполнеия.</span><span class="sxs-lookup"><span data-stu-id="dd753-115">Select the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Введите имя файла в диалоговом окке "Открыть файл"" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="dd753-117">Введите имя файла в диалоговом окке **"Открыть** файл"</span><span class="sxs-lookup"><span data-stu-id="dd753-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="dd753-118">Открытие ресурсов на панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="dd753-118">Open resources in the Network panel</span></span>  

<span data-ttu-id="dd753-119">Перейдите [к просмотру сведений о ресурсе.][DevtoolsNetworkInspectDetailsResource]</span><span class="sxs-lookup"><span data-stu-id="dd753-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Проверка ресурса на панели "Сеть"" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="dd753-121">Проверка ресурса на панели **"Сеть"**</span><span class="sxs-lookup"><span data-stu-id="dd753-121">Inspect a resource in the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="dd753-122">Ресурсы раскрытия на панели "Сеть" с других панелей</span><span class="sxs-lookup"><span data-stu-id="dd753-122">Reveal resources in the Network panel from other panels</span></span>  

<span data-ttu-id="dd753-123">В [разделе "Обзор](#browse-resources) ресурсов" ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.</span><span class="sxs-lookup"><span data-stu-id="dd753-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="dd753-124">Если вы когда-либо хотите \*\*\*\* проверить ресурс на панели "Сеть", щелкните правой кнопкой мыши ресурс и выберите "Показать" **на панели "Сеть".**</span><span class="sxs-lookup"><span data-stu-id="dd753-124">If you ever want to inspect a resource in the **Network** panel, right-click the resource and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Показать на панели "Сеть"" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="dd753-126">Показать на панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="dd753-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <span data-ttu-id="dd753-127">Просмотр ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd753-127">Browse resources</span></span>  

### <span data-ttu-id="dd753-128">Просмотр ресурсов на панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="dd753-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="dd753-129">Перейдите в [журнал сетевой активности.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="dd753-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ресурсы страницы в сетевом журнале" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="dd753-131">Ресурсы страницы в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="dd753-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <span data-ttu-id="dd753-132">Обзор по каталогу</span><span class="sxs-lookup"><span data-stu-id="dd753-132">Browse by directory</span></span>  

<span data-ttu-id="dd753-133">Чтобы просмотреть ресурсы страницы, организованной по каталогу:</span><span class="sxs-lookup"><span data-stu-id="dd753-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="dd753-134">Щелкните **вкладку "Источники",** чтобы открыть панель **источников.**</span><span class="sxs-lookup"><span data-stu-id="dd753-134">Click the **Sources** tab to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="dd753-135">Щелкните **вкладку** "Страница", чтобы отдемонстрировать ресурсы страницы.</span><span class="sxs-lookup"><span data-stu-id="dd753-135">Click the **Page** tab to show the resources of the page.</span></span>  <span data-ttu-id="dd753-136">**Откроется** страница страницы.</span><span class="sxs-lookup"><span data-stu-id="dd753-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="The Page pane" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="dd753-138">The **Page** pane</span><span class="sxs-lookup"><span data-stu-id="dd753-138">The **Page** pane</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="dd753-139">Вот разбивка неявных элементов на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dd753-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="dd753-140">Элемент страницы</span><span class="sxs-lookup"><span data-stu-id="dd753-140">Page item</span></span> | <span data-ttu-id="dd753-141">Описание</span><span class="sxs-lookup"><span data-stu-id="dd753-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="dd753-142">Контекст просмотра [основного документа.][MDNInlineFrame]</span><span class="sxs-lookup"><span data-stu-id="dd753-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="dd753-143">Домен.</span><span class="sxs-lookup"><span data-stu-id="dd753-143">The domain.</span></span>  <span data-ttu-id="dd753-144">Все вложенные в него ресурсы приходят из этого домена.</span><span class="sxs-lookup"><span data-stu-id="dd753-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="dd753-145">Например, полный URL-адрес `comlink.global.j` файла, вероятно, будет `https://airhorner.com/scripts/comlink.global.js` .</span><span class="sxs-lookup"><span data-stu-id="dd753-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="dd753-146">Каталог.</span><span class="sxs-lookup"><span data-stu-id="dd753-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="dd753-147">Основной HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="dd753-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="dd753-148">Контекст рабочего времени службы.</span><span class="sxs-lookup"><span data-stu-id="dd753-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="dd753-149">Щелкните ресурс, чтобы просмотреть его в **редакторе.**</span><span class="sxs-lookup"><span data-stu-id="dd753-149">Click a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Просмотр файла в редакторе" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="dd753-151">Просмотр файла в **редакторе**</span><span class="sxs-lookup"><span data-stu-id="dd753-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="dd753-152">Обзор по имени файла</span><span class="sxs-lookup"><span data-stu-id="dd753-152">Browse by filename</span></span>  

<span data-ttu-id="dd753-153">По умолчанию в **области** страниц ресурсы группироваться по каталогу.</span><span class="sxs-lookup"><span data-stu-id="dd753-153">By default the **Page** pane groups resources by directory.</span></span>  <span data-ttu-id="dd753-154">Чтобы отключить эту группу и просмотреть ресурсы для каждого домена в качестве плоского списка:</span><span class="sxs-lookup"><span data-stu-id="dd753-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="dd753-155">Откройте **страницу.**</span><span class="sxs-lookup"><span data-stu-id="dd753-155">Open the **Page** pane.</span></span>  <span data-ttu-id="dd753-156">Перейдите в ["Обзор по каталогу".](#browse-by-directory)</span><span class="sxs-lookup"><span data-stu-id="dd753-156">Navigate to [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="dd753-157">Choose **More Options** and `...` disable Group By **Folder**.</span><span class="sxs-lookup"><span data-stu-id="dd753-157">Choose **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Параметр "Группировка по папке"" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="dd753-159">Параметр **"Группировка по папке"**</span><span class="sxs-lookup"><span data-stu-id="dd753-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="dd753-160">Ресурсы организованы по типу файла.</span><span class="sxs-lookup"><span data-stu-id="dd753-160">Resources are organized by file type.</span></span>  <span data-ttu-id="dd753-161">В каждом типе файлов ресурсы организованы в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="dd753-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="The Page pane after disabling Group By Folder" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="dd753-163">The **Page** pane after disabling **Group By Folder**</span><span class="sxs-lookup"><span data-stu-id="dd753-163">The **Page** pane after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="dd753-164">Обзор по типу файла</span><span class="sxs-lookup"><span data-stu-id="dd753-164">Browse by file type</span></span>  

<span data-ttu-id="dd753-165">Группировка ресурсов в зависимости от типа файла:</span><span class="sxs-lookup"><span data-stu-id="dd753-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="dd753-166">Перейдите на **вкладку "Приложение".**  Откроется **панель** "Приложение".</span><span class="sxs-lookup"><span data-stu-id="dd753-166">Click the **Application** tab.  The **Application** panel opens.</span></span>  <span data-ttu-id="dd753-167">По умолчанию **сначала открывается** окно манифеста.</span><span class="sxs-lookup"><span data-stu-id="dd753-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Панель "Приложение"" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="dd753-169">Панель **"Приложение"**</span><span class="sxs-lookup"><span data-stu-id="dd753-169">The **Application** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dd753-170">Прокрутите вниз до области **"Кадры".**</span><span class="sxs-lookup"><span data-stu-id="dd753-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="The Frames pane" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="dd753-172">The **Frames** pane</span><span class="sxs-lookup"><span data-stu-id="dd753-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dd753-173">Разорите разделы, в которых вас интересует.</span><span class="sxs-lookup"><span data-stu-id="dd753-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="dd753-174">Щелкните ресурс, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="dd753-174">Click a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Просмотр ресурса на панели приложения" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="dd753-176">Просмотр ресурса на панели **приложения**</span><span class="sxs-lookup"><span data-stu-id="dd753-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="dd753-177">Просмотр файлов по типу на панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="dd753-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="dd753-178">Перейдите к [фильтру по типу ресурса.][DevtoolsNetworkFilterByResourceType]</span><span class="sxs-lookup"><span data-stu-id="dd753-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Фильтр CSS в сетевом журнале" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="dd753-180">Фильтр CSS в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="dd753-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <span data-ttu-id="dd753-181">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dd753-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтрация по типу ресурса — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Проверка сведений о ресурсе — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Запись сетевой активности — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Изучите веб-разработку | MDN"  

> [!NOTE]
> <span data-ttu-id="dd753-188">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd753-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dd753-189">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/resources/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="dd753-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dd753-191">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd753-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
