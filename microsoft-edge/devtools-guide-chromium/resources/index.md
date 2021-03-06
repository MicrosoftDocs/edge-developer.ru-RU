---
description: Организация ресурсов по кадру, домену, типу или другим критериям.
title: Просмотр ресурсов страниц с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 75063b23f23c25ff4fe2e7f6e044a2de9a7b1ccd
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398226"
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

# <a name="view-page-resources-with-microsoft-edge-devtools"></a><span data-ttu-id="49037-104">Просмотр ресурсов страниц с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49037-104">View page resources with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="49037-105">В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="49037-105">This guide teaches you how to use Microsoft Edge DevTools to view the resources of a web page.</span></span>  <span data-ttu-id="49037-106">Ресурсы — это файлы, необходимые странице для правильного отображения.</span><span class="sxs-lookup"><span data-stu-id="49037-106">Resources are the files that a page needs in order to display correctly.</span></span>  <span data-ttu-id="49037-107">Примеры ресурсов: CSS, JavaScript и HTML-файлы, а также изображения.</span><span class="sxs-lookup"><span data-stu-id="49037-107">Examples of resources include CSS, JavaScript, and HTML files, as well as images.</span></span>  

<span data-ttu-id="49037-108">В этом руководстве предполагается, что [][MDNLearnWebDevelopment] вы знакомы с основами веб-разработки и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="49037-108">This guide assumes that you are familiar with the basics of [web development][MDNLearnWebDevelopment] and [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="open-resources"></a><span data-ttu-id="49037-109">Открытые ресурсы</span><span class="sxs-lookup"><span data-stu-id="49037-109">Open resources</span></span>  

<span data-ttu-id="49037-110">Когда вы знаете имя ресурса, который необходимо проверить, меню **команд** обеспечивает быстрый способ открытия ресурса.</span><span class="sxs-lookup"><span data-stu-id="49037-110">When you know the name of the resource that you want to inspect, the **Command Menu** provides a fast way of opening the resource.</span></span>  

1.  <span data-ttu-id="49037-111">Выберите `Control` + `P` \(Windows, Linux\) `Command` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="49037-111">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\).</span></span>  <span data-ttu-id="49037-112">Открывается диалоговое окно **Open File.**</span><span class="sxs-lookup"><span data-stu-id="49037-112">The **Open File** dialog opens.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-empty.msft.png" alt-text="Диалоговое окно Open File" lightbox="../media/resources-command-menu-empty.msft.png":::
       <span data-ttu-id="49037-114">Диалоговое **окно Open File**</span><span class="sxs-lookup"><span data-stu-id="49037-114">The **Open File** dialog</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49037-115">Выберите файл из выпадаемой папки или начните вводить имя файла и выберите, как только правильный файл будет выделен в поле `Enter` автокомплетов.</span><span class="sxs-lookup"><span data-stu-id="49037-115">Choose the file from the dropdown, or start typing the filename and select `Enter` once the correct file is highlighted in the autocomplete box.</span></span>  
    
    :::image type="complex" source="../media/resources-command-menu-file-search.msft.png" alt-text="Введите имя файла в диалоговом окте "Открытый файл"" lightbox="../media/resources-command-menu-file-search.msft.png":::
       <span data-ttu-id="49037-117">Введите имя файла в **диалоговом окте "Открытый** файл"</span><span class="sxs-lookup"><span data-stu-id="49037-117">Type a filename in the **Open File** dialog</span></span>  
    :::image-end:::  
    
### <a name="open-resources-in-the-network-tool"></a><span data-ttu-id="49037-118">Откройте ресурсы в средстве Network</span><span class="sxs-lookup"><span data-stu-id="49037-118">Open resources in the Network tool</span></span>  

<span data-ttu-id="49037-119">Перейдите [для проверки сведений о ресурсе.][DevtoolsNetworkInspectDetailsResource]</span><span class="sxs-lookup"><span data-stu-id="49037-119">Navigate to [Inspect the details of a resource][DevtoolsNetworkInspectDetailsResource].</span></span>  

:::image type="complex" source="../media/resources-network-response.msft.png" alt-text="Проверка ресурса в средстве Network" lightbox="../media/resources-network-response.msft.png":::
   <span data-ttu-id="49037-121">Проверка ресурса в **средстве Network**</span><span class="sxs-lookup"><span data-stu-id="49037-121">Inspect a resource in the **Network** tool</span></span>  
:::image-end:::  

### <a name="reveal-resources-in-the-network-tool-from-other-panels"></a><span data-ttu-id="49037-122">Выявление ресурсов в средстве Network с других панелей</span><span class="sxs-lookup"><span data-stu-id="49037-122">Reveal resources in the Network tool from other panels</span></span>  

<span data-ttu-id="49037-123">В [разделе Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.</span><span class="sxs-lookup"><span data-stu-id="49037-123">The [Browse resources](#browse-resources) section below shows you how to view resources from various parts of the DevTools UI.</span></span>  <span data-ttu-id="49037-124">Если вы когда-либо хотите \*\*\*\* проверить ресурс в средстве Network, наведите курсор на ресурс, откройте контекстное меню \(правой кнопкой мыши\) и выберите Показать в **панели Сети**.</span><span class="sxs-lookup"><span data-stu-id="49037-124">If you ever want to inspect a resource in the **Network** tool,  hover on the resource, open the contextual menu \(right-click\), and choose **Reveal in Network panel**.</span></span>  

:::image type="complex" source="../media/resources-sources-page-reveal-in-network-panel.msft.png" alt-text="Reveal in Network panel" lightbox="../media/resources-sources-page-reveal-in-network-panel.msft.png":::
   **<span data-ttu-id="49037-126">Reveal in Network panel</span><span class="sxs-lookup"><span data-stu-id="49037-126">Reveal in Network panel</span></span>**  
:::image-end:::  

## <a name="browse-resources"></a><span data-ttu-id="49037-127">Просмотр ресурсов</span><span class="sxs-lookup"><span data-stu-id="49037-127">Browse resources</span></span>  

### <a name="browse-resources-in-the-network-panel"></a><span data-ttu-id="49037-128">Просмотр ресурсов в панели Network</span><span class="sxs-lookup"><span data-stu-id="49037-128">Browse resources in the Network panel</span></span>  

<span data-ttu-id="49037-129">Перейдите к [сетевой активности журнала][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="49037-129">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

:::image type="complex" source="../media/resources-network-resources.msft.png" alt-text="Ресурсы страницы в сетевом журнале" lightbox="../media/resources-network-resources.msft.png":::
   <span data-ttu-id="49037-131">Ресурсы страницы в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="49037-131">Page resources in the **Network** Log</span></span>  
:::image-end:::  

### <a name="browse-by-directory"></a><span data-ttu-id="49037-132">Просмотр каталога</span><span class="sxs-lookup"><span data-stu-id="49037-132">Browse by directory</span></span>  

<span data-ttu-id="49037-133">Просмотр ресурсов страницы, организованной каталогом:</span><span class="sxs-lookup"><span data-stu-id="49037-133">To view the resources of a page organized by directory:</span></span>  

1.  <span data-ttu-id="49037-134">Выберите средство **Источники** для открытия панели **Источники.**</span><span class="sxs-lookup"><span data-stu-id="49037-134">Choose the **Sources** tool to open the **Sources** panel.</span></span>  
1.  <span data-ttu-id="49037-135">Выберите **панель Page,** чтобы показать ресурсы страницы.</span><span class="sxs-lookup"><span data-stu-id="49037-135">Choose the **Page** panel to show the resources of the page.</span></span>  <span data-ttu-id="49037-136">**Откроется** области Страницы.</span><span class="sxs-lookup"><span data-stu-id="49037-136">The **Page** pane opens.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-empty.msft.png" alt-text="Области Страницы" lightbox="../media/resources-sources-page-empty.msft.png":::
       <span data-ttu-id="49037-138">Панель **Page**</span><span class="sxs-lookup"><span data-stu-id="49037-138">The **Page** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="49037-139">Вот разбивка неявных элементов на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="49037-139">Here is a breakdown of the non-obvious items in the previous figure.</span></span>  
    
    | <span data-ttu-id="49037-140">Элемент Page</span><span class="sxs-lookup"><span data-stu-id="49037-140">Page item</span></span> | <span data-ttu-id="49037-141">Описание</span><span class="sxs-lookup"><span data-stu-id="49037-141">Description</span></span> |  
    |:--- |:--- |  
    | `top` | <span data-ttu-id="49037-142">Основной контекст просмотра [документов][MDNInlineFrame].</span><span class="sxs-lookup"><span data-stu-id="49037-142">The main document [browsing context][MDNInlineFrame].</span></span> |  
    | `airhorner.com` | <span data-ttu-id="49037-143">Домен.</span><span class="sxs-lookup"><span data-stu-id="49037-143">The domain.</span></span>  <span data-ttu-id="49037-144">Все ресурсы, вложенные в него, приходят из этого домена.</span><span class="sxs-lookup"><span data-stu-id="49037-144">All resources nested under it come from that domain.</span></span>  <span data-ttu-id="49037-145">Например, полный URL-адрес `comlink.global.j` файла, `https://airhorner.com/scripts/comlink.global.js` вероятно, .</span><span class="sxs-lookup"><span data-stu-id="49037-145">For example, the full URL of the `comlink.global.j` file is probably `https://airhorner.com/scripts/comlink.global.js`.</span></span> |  
    | `scripts` | <span data-ttu-id="49037-146">Каталог.</span><span class="sxs-lookup"><span data-stu-id="49037-146">A directory.</span></span> |  
    | `(index)` | <span data-ttu-id="49037-147">Основной HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="49037-147">The main HTML document.</span></span> |  
    | `sw.js` | <span data-ttu-id="49037-148">Контекст времени работы сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="49037-148">A service worker runtime context.</span></span> |  
    
1.  <span data-ttu-id="49037-149">Выберите ресурс, чтобы просмотреть его в **редакторе**.</span><span class="sxs-lookup"><span data-stu-id="49037-149">Choose a resource to view it in the **Editor**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource.msft.png" alt-text="Просмотр файла в редакторе" lightbox="../media/resources-sources-page-resource.msft.png":::
       <span data-ttu-id="49037-151">Просмотр файла в **редакторе**</span><span class="sxs-lookup"><span data-stu-id="49037-151">View a file in the **Editor**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-filename"></a><span data-ttu-id="49037-152">Просмотр по имени файла</span><span class="sxs-lookup"><span data-stu-id="49037-152">Browse by filename</span></span>  

<span data-ttu-id="49037-153">По умолчанию **ресурсы групп групп** страниц по каталогу.</span><span class="sxs-lookup"><span data-stu-id="49037-153">By default the **Page** panel groups resources by directory.</span></span>  <span data-ttu-id="49037-154">Чтобы отключить эту группу и просмотреть ресурсы для каждого домена в качестве плоского списка:</span><span class="sxs-lookup"><span data-stu-id="49037-154">To disable this grouping and view the resources for each domain as a flat list:</span></span>  

1.  <span data-ttu-id="49037-155">Откройте **панель Page.**</span><span class="sxs-lookup"><span data-stu-id="49037-155">Open the **Page** panel.</span></span>  <span data-ttu-id="49037-156">Перейдите [к просмотру по каталогу](#browse-by-directory).</span><span class="sxs-lookup"><span data-stu-id="49037-156">Navigate to [Browse by directory](#browse-by-directory).</span></span>  
1.  <span data-ttu-id="49037-157">Выберите **дополнительные параметры** `...` и **отключим группу по папке**.</span><span class="sxs-lookup"><span data-stu-id="49037-157">Choose **More Options** `...` and disable **Group By Folder**.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resource-group-by-folder.msft.png" alt-text="Параметр Group By Folder" lightbox="../media/resources-sources-page-resource-group-by-folder.msft.png":::
       <span data-ttu-id="49037-159">Параметр **Group By Folder**</span><span class="sxs-lookup"><span data-stu-id="49037-159">The **Group By Folder** option</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="49037-160">Ресурсы организованы по типу файла.</span><span class="sxs-lookup"><span data-stu-id="49037-160">Resources are organized by file type.</span></span>  <span data-ttu-id="49037-161">В каждом типе файла ресурсы организованы в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="49037-161">Within each file type the resources are organized alphabetically.</span></span>  
    
    :::image type="complex" source="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png" alt-text="Панель Page после отключения группы по папке" lightbox="../media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png":::
       <span data-ttu-id="49037-163">Панель **Page** после отключения **группы по папке**</span><span class="sxs-lookup"><span data-stu-id="49037-163">The **Page** panel after disabling **Group By Folder**</span></span>  
    :::image-end:::  
    
### <a name="browse-by-file-type"></a><span data-ttu-id="49037-164">Просмотр по типу файла</span><span class="sxs-lookup"><span data-stu-id="49037-164">Browse by file type</span></span>  

<span data-ttu-id="49037-165">Сгруппить ресурсы в зависимости от типа файла:</span><span class="sxs-lookup"><span data-stu-id="49037-165">To group resources together based on their file type:</span></span>  

1.  <span data-ttu-id="49037-166">Выберите **вкладку Application.**  Откроется **средство** Приложения.</span><span class="sxs-lookup"><span data-stu-id="49037-166">Choose the **Application** tab.  The **Application** tool opens.</span></span>  <span data-ttu-id="49037-167">По умолчанию **области Манифест** обычно открывается первым.</span><span class="sxs-lookup"><span data-stu-id="49037-167">By default the **Manifest** pane usually opens first.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner.msft.png" alt-text="Средство приложения" lightbox="../media/resources-application-mainfest-airhorner.msft.png":::
       <span data-ttu-id="49037-169">Средство **приложения**</span><span class="sxs-lookup"><span data-stu-id="49037-169">The **Application** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49037-170">Прокрутите вниз **до области Frames.**</span><span class="sxs-lookup"><span data-stu-id="49037-170">Scroll down to the **Frames** pane.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png" alt-text="Рамки" lightbox="../media/resources-application-mainfest-airhorner-frames-expanded.msft.png":::
       <span data-ttu-id="49037-172">**Рамки**</span><span class="sxs-lookup"><span data-stu-id="49037-172">The **Frames** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49037-173">Расширь разделы, в которых вас интересует.</span><span class="sxs-lookup"><span data-stu-id="49037-173">Expand the sections in which you are interested.</span></span>  
1.  <span data-ttu-id="49037-174">Выберите ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="49037-174">Choose a resource to view it.</span></span>  
    
    :::image type="complex" source="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png" alt-text="Просмотр ресурса в панели приложений" lightbox="../media/resources-application-mainfest-airhorner-expanded-resources.msft.png":::
       <span data-ttu-id="49037-176">Просмотр ресурса в панели **приложений**</span><span class="sxs-lookup"><span data-stu-id="49037-176">View a resource in the **Application** panel</span></span>  
    :::image-end:::  
    
#### <a name="browse-files-by-type-in-the-network-panel"></a><span data-ttu-id="49037-177">Просмотр файлов по типу в панели Network</span><span class="sxs-lookup"><span data-stu-id="49037-177">Browse files by type in the Network panel</span></span>  

<span data-ttu-id="49037-178">Перейдите [к фильтру по типу ресурса.][DevtoolsNetworkFilterByResourceType]</span><span class="sxs-lookup"><span data-stu-id="49037-178">Navigate to [Filter by resource type][DevtoolsNetworkFilterByResourceType].</span></span>  

:::image type="complex" source="../media/resources-network-resources-filter-css.msft.png" alt-text="Фильтр CSS в сетевом журнале" lightbox="../media/resources-network-resources-filter-css.msft.png":::
   <span data-ttu-id="49037-180">Фильтр CSS в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="49037-180">Filter for CSS in the **Network** Log</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="49037-181">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49037-181">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsNetworkFilterByResourceType]: ../network/index.md#filter-by-resource-type "Фильтр по типу ресурса — проверьте активность сети в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkInspectDetailsResource]: ../network/index.md#inspect-the-details-of-the-resource "Проверка сведений о ресурсе — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity "Сетевое действие журнала — проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент Inline Frame | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Узнайте, как | MDN"  

> [!NOTE]
> <span data-ttu-id="49037-188">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49037-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49037-189">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/resources/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="49037-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/resources/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49037-191">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49037-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
