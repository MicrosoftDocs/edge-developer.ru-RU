---
description: Полная ссылка на функции панели Microsoft Edge DevTools Network.
title: Ссылка на анализ сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 94a7031763da1e540b4dab802358e5f200e0db4a
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439705"
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

# <a name="network-analysis-reference"></a><span data-ttu-id="8d920-104">Ссылка на анализ сети</span><span class="sxs-lookup"><span data-stu-id="8d920-104">Network Analysis reference</span></span>  

<span data-ttu-id="8d920-105">Узнайте о новых способах анализа загрузки страницы в этой комплексной ссылке на функции сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d920-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <a name="record-network-requests"></a><span data-ttu-id="8d920-106">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-106">Record network requests</span></span>  

<span data-ttu-id="8d920-107">По умолчанию DevTools записываю все сетевые запросы в средстве **Network,** пока DevTools открыт.</span><span class="sxs-lookup"><span data-stu-id="8d920-107">By default, DevTools record all network requests in the **Network** tool, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель Network" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="8d920-109">Средство **Network**</span><span class="sxs-lookup"><span data-stu-id="8d920-109">The **Network** tool</span></span>  
:::image-end:::  

### <a name="stop-recording-network-requests"></a><span data-ttu-id="8d920-110">Остановка записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-110">Stop recording network requests</span></span>  

<span data-ttu-id="8d920-111">Чтобы остановить запись запросов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d920-112">В **средстве Network** выберите **Стоп запись сетевого журнала** \( Остановка ![ записи сетевого ](../media/record-on-icon.msft.png) журнала \).</span><span class="sxs-lookup"><span data-stu-id="8d920-112">On the **Network** tool, choose **Stop recording network log** \(![Stop recording network log](../media/record-on-icon.msft.png)\).</span></span>  <span data-ttu-id="8d920-113">Становится серым, чтобы указать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="8d920-114">Выберите `Control` + `E` \(Windows, Linux\) `Command` + `E` или \(macOS\) в \*\*\*\* то время как средство Network находится в центре внимания.</span><span class="sxs-lookup"><span data-stu-id="8d920-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** tool is in focus.</span></span>  

### <a name="clear-requests"></a><span data-ttu-id="8d920-115">Четкие запросы</span><span class="sxs-lookup"><span data-stu-id="8d920-115">Clear requests</span></span>  

<span data-ttu-id="8d920-116">Выберите **Clear** \( Clear \) в средстве Network, чтобы очистить все ![ ](../media/clear-requests-icon.msft.png) запросы из таблицы Запросов. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d920-116">Choose **Clear** \(![Clear](../media/clear-requests-icon.msft.png)\) on the **Network** tool to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка Clear" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="8d920-118">Кнопка **Clear**</span><span class="sxs-lookup"><span data-stu-id="8d920-118">The **Clear** button</span></span>  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a><span data-ttu-id="8d920-119">Сохранение запросов в разных нагрузках страниц</span><span class="sxs-lookup"><span data-stu-id="8d920-119">Save requests across page loads</span></span>  

<span data-ttu-id="8d920-120">Чтобы сохранить запросы во всех загрузках страниц, в средстве **Network** включите почтовый ящик **Сохранить** журнал.</span><span class="sxs-lookup"><span data-stu-id="8d920-120">To save requests across page loads, on the **Network** tool, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="8d920-121">DevTools сохраняет все запросы, пока не отключите **журнал Preserve.**</span><span class="sxs-lookup"><span data-stu-id="8d920-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Почтовый ящик Preserve Log" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="8d920-123">Почтовый **ящик Preserve Log**</span><span class="sxs-lookup"><span data-stu-id="8d920-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a><span data-ttu-id="8d920-124">Захват скриншотов во время загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="8d920-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="8d920-125">Снимите скриншоты для анализа отображаемой информации для пользователей в ожидании загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="8d920-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="8d920-126">Чтобы включить снимки экрана, выберите **параметры Сети**и в **инструменте Network** включим контрольный ящик **снимков** экрана захвата.</span><span class="sxs-lookup"><span data-stu-id="8d920-126">To enable screenshots, choose **Network settings**, and on the **Network** tool, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="8d920-127">Обновите страницу, пока средство **Network** находится в фокусе для захвата скриншотов.</span><span class="sxs-lookup"><span data-stu-id="8d920-127">Refresh the page while the **Network** tool is in focus to capture screenshots.</span></span>  

<span data-ttu-id="8d920-128">После захвата экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="8d920-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="8d920-129">Наведите курсор на скриншот, чтобы отобразить точку, в которой был сделан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="8d920-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="8d920-130">На области Обзор отображается \*\*\*\* желтая строка.</span><span class="sxs-lookup"><span data-stu-id="8d920-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="8d920-131">Выберите эскиз экрана, чтобы отфильтровать все запросы, которые произошли после захвата экрана.</span><span class="sxs-lookup"><span data-stu-id="8d920-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="8d920-132">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="8d920-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведите курсор на скриншоте" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="8d920-134">Наведите курсор на скриншоте</span><span class="sxs-lookup"><span data-stu-id="8d920-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a><span data-ttu-id="8d920-135">Изменение поведения загрузки</span><span class="sxs-lookup"><span data-stu-id="8d920-135">Change loading behavior</span></span>  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a><span data-ttu-id="8d920-136">Эмулировать первого посетителя, отключив кэш браузера</span><span class="sxs-lookup"><span data-stu-id="8d920-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="8d920-137">Чтобы подражать первому пользователю, как он работает с сайтом, включите почтовый ящик **отключения** кэша.</span><span class="sxs-lookup"><span data-stu-id="8d920-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="8d920-138">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="8d920-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="8d920-139">Эта функция более точно эмулирует пользовательский опыт, так как запросы подаются из кэша браузера при повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="8d920-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Почтовый ящик Отключение кэша" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="8d920-141">Почтовый **ящик Отключение кэша**</span><span class="sxs-lookup"><span data-stu-id="8d920-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a><span data-ttu-id="8d920-142">Отключение кэша браузера из ящика сетевых условий</span><span class="sxs-lookup"><span data-stu-id="8d920-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="8d920-143">Если вы хотите отключить кэш во время работы в других панелях DevTools, используйте ящик Сетевые условия.</span><span class="sxs-lookup"><span data-stu-id="8d920-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="8d920-144">Откройте ящик **сетевых** условий.</span><span class="sxs-lookup"><span data-stu-id="8d920-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8d920-145">Включите \(или off\) почтовый ящик **отключения** кэша.</span><span class="sxs-lookup"><span data-stu-id="8d920-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a><span data-ttu-id="8d920-146">Вручную очистить кэш браузера</span><span class="sxs-lookup"><span data-stu-id="8d920-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="8d920-147">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню \(правой кнопкой мыши\) в любой точке таблицы Запросов и выберите кэш **Clear Browser.**</span><span class="sxs-lookup"><span data-stu-id="8d920-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор кэша "Ясный браузер"" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="8d920-149">Выбор **кэша "Ясный браузер"**</span><span class="sxs-lookup"><span data-stu-id="8d920-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <a name="emulate-offline"></a><span data-ttu-id="8d920-150">Эмулировать автономный режим</span><span class="sxs-lookup"><span data-stu-id="8d920-150">Emulate offline</span></span>  

<span data-ttu-id="8d920-151">Новый класс веб-приложений с именем [Progressive Web Apps (Прогрессивные веб-приложения)][DevtoolsProgressiveWebApps]функционирует в автономном режиме с помощью **сотрудников службы.**</span><span class="sxs-lookup"><span data-stu-id="8d920-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="8d920-152">Возможно, вам будет полезно быстро смоделировать устройство, не подключенное к данным при создании такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="8d920-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="8d920-153">Выберите \*\*\*\* меню выпадаемых данных в Интернете, поиск в **пресетах**и выберите **автономный** режим для имитации автономного сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="8d920-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Меню отключения в автономном режиме" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="8d920-155">Меню **отключения** в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="8d920-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a><span data-ttu-id="8d920-156">Эмулировать медленные сетевые подключения</span><span class="sxs-lookup"><span data-stu-id="8d920-156">Emulate slow network connections</span></span>  

<span data-ttu-id="8d920-157">Эмулировать медленные скорости подключения 3G, Fast 3G и другие скорости подключения из меню **отсев** в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8d920-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Меню отключения от регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="8d920-159">Меню **отключения** от регулирования</span><span class="sxs-lookup"><span data-stu-id="8d920-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-160">Вы можете выбрать из различных пресетов, таких как Slow 3G или Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="8d920-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="8d920-161">Чтобы добавить собственные настраиваемые предустанавливные настройки, откройте меню регулирование и выберите **настраиваемый**  >  **добавить**.</span><span class="sxs-lookup"><span data-stu-id="8d920-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="8d920-162">В DevTools рядом с средством **Network** отображается значок предупреждения, чтобы напомнить, что включено регулирование.</span><span class="sxs-lookup"><span data-stu-id="8d920-162">DevTools displays a warning icon next to the **Network** tool to remind you that throttling is enabled.</span></span>  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a><span data-ttu-id="8d920-163">Эмулировать медленные сетевые подключения из ящика сетевых условий</span><span class="sxs-lookup"><span data-stu-id="8d920-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="8d920-164">Если вы хотите заторможить сетевое подключение во время работы в других панелях DevTools, используйте ящик сетевых условий.</span><span class="sxs-lookup"><span data-stu-id="8d920-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="8d920-165">Откройте ящик **сетевых** условий.</span><span class="sxs-lookup"><span data-stu-id="8d920-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8d920-166">Выберите скорость подключения из меню **регулирования.**</span><span class="sxs-lookup"><span data-stu-id="8d920-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a><span data-ttu-id="8d920-167">Файлы cookie браузера вручную очищают</span><span class="sxs-lookup"><span data-stu-id="8d920-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="8d920-168">Чтобы вручную очистить cookie-файлы браузера в любое время, наведите курсор в любом месте таблицы Запросов, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Clear Browser Cookies**.</span><span class="sxs-lookup"><span data-stu-id="8d920-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор cookie-файлов Clear Browser" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="8d920-170">Выбор **cookie-файлов Clear Browser**</span><span class="sxs-lookup"><span data-stu-id="8d920-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <a name="override-the-user-agent"></a><span data-ttu-id="8d920-171">Переопределять агент пользователя</span><span class="sxs-lookup"><span data-stu-id="8d920-171">Override the user agent</span></span>  

<span data-ttu-id="8d920-172">Чтобы вручную переопредить агента пользователя, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-173">Откройте ящик **сетевых** условий.</span><span class="sxs-lookup"><span data-stu-id="8d920-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="8d920-174">Выключите **автоматический почтовый ящик Select.**</span><span class="sxs-lookup"><span data-stu-id="8d920-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="8d920-175">Выберите параметр агента пользователя из меню или введите настраиваемый параметр в текстовом окне.</span><span class="sxs-lookup"><span data-stu-id="8d920-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a><span data-ttu-id="8d920-176">Запросы фильтрации</span><span class="sxs-lookup"><span data-stu-id="8d920-176">Filter requests</span></span>  

### <a name="filter-requests-by-properties"></a><span data-ttu-id="8d920-177">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="8d920-177">Filter requests by properties</span></span>  

<span data-ttu-id="8d920-178">Используйте **текстовое** поле Filter для фильтрации запросов по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="8d920-179">Если текстовое поле не отображается, возможно, будет скрыта области **Фильтры.**</span><span class="sxs-lookup"><span data-stu-id="8d920-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="8d920-180">Дополнительные сведения можно получить в [области Hide the Filters.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="8d920-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле Filter" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="8d920-182">Текстовое **поле Filter**</span><span class="sxs-lookup"><span data-stu-id="8d920-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-183">Вы можете использовать несколько свойств одновременно, разделив каждое свойство с пространством.</span><span class="sxs-lookup"><span data-stu-id="8d920-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="8d920-184">Например, отображаются все PNGs размером более `mime-type:image/png larger-than:1K` 1 килобайта.</span><span class="sxs-lookup"><span data-stu-id="8d920-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="8d920-185">Фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="8d920-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="8d920-186">в настоящее время операции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8d920-186">operations are currently not supported.</span></span>  

<span data-ttu-id="8d920-187">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="8d920-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="8d920-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d920-188">Property</span></span> | <span data-ttu-id="8d920-189">Сведения</span><span class="sxs-lookup"><span data-stu-id="8d920-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="8d920-190">Отображаются только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="8d920-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="8d920-191">Вы можете использовать символ под диктовки `*` \( \) для использования нескольких доменов.</span><span class="sxs-lookup"><span data-stu-id="8d920-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="8d920-192">Например, `*.com` отображает ресурсы из всех доменных имен, заканчивающийся `.com` в .</span><span class="sxs-lookup"><span data-stu-id="8d920-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="8d920-193">DevTools заполняют меню автозапуска автокомплектов всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="8d920-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="8d920-194">Отображает ресурсы, содержащие указанный заглавной ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="8d920-195">DevTools заполняют выпадаемую часть автокомплекта всеми найденными загонами ответа.</span><span class="sxs-lookup"><span data-stu-id="8d920-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="8d920-196">Используйте `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d920-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="8d920-197">Отображает ресурсы, которые больше указанного размера, в bytes.</span><span class="sxs-lookup"><span data-stu-id="8d920-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="8d920-198">Установка значения `1000` эквивалентна установке значения `1k` .</span><span class="sxs-lookup"><span data-stu-id="8d920-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="8d920-199">Отображает ресурсы, извлеченные за указанный тип метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="8d920-200">DevTools заполняют отсев всеми найденными методами HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="8d920-201">Отображает ресурсы определенного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="8d920-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="8d920-202">DevTools заполняют отсев всеми найденными типами MIME.</span><span class="sxs-lookup"><span data-stu-id="8d920-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="8d920-203">Показать все смешанные ресурсы контента \( \) или только те, которые в настоящее время `mixed-content:all` отображаются `mixed-content:displayed` \( \).</span><span class="sxs-lookup"><span data-stu-id="8d920-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="8d920-204">Отображает ресурсы, извлеченные из незащищенных http\( \) или `scheme:http` защищенных HTTPS `scheme:https` \( \).</span><span class="sxs-lookup"><span data-stu-id="8d920-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="8d920-205">Отображает ресурсы с `Set-Cookie` загонами с `Domain` атрибутом, который соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="8d920-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="8d920-206">DevTools заполняют автокомплект всеми найденными доменами cookie.</span><span class="sxs-lookup"><span data-stu-id="8d920-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="8d920-207">Отображает ресурсы с загонами с именем, которое соответствует `Set-Cookie` указанному значению.</span><span class="sxs-lookup"><span data-stu-id="8d920-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="8d920-208">DevTools заполняют автокомплект всеми найденными именами файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="8d920-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="8d920-209">Отображает ресурсы с загонами со значением, которое соответствует `Set-Cookie` указанному значению.</span><span class="sxs-lookup"><span data-stu-id="8d920-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="8d920-210">DevTools заполняют автокомплект всеми найденными значениями cookie.</span><span class="sxs-lookup"><span data-stu-id="8d920-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="8d920-211">Отображает ресурсы, которые соответствуют определенному коду состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="8d920-212">DevTools заполняет меню отсева автокомплетов всеми найденными кодами состояния.</span><span class="sxs-lookup"><span data-stu-id="8d920-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <a name="filter-requests-by-type"></a><span data-ttu-id="8d920-213">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="8d920-213">Filter requests by type</span></span>  

<span data-ttu-id="8d920-214">Чтобы фильтровать запросы по типу запроса, выберите одну из следующих кнопок в **средстве Network.**</span><span class="sxs-lookup"><span data-stu-id="8d920-214">To filter requests by request type, choose the one of the following buttons on the **Network** tool.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-215">XHR</span><span class="sxs-lookup"><span data-stu-id="8d920-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-216">JS</span><span class="sxs-lookup"><span data-stu-id="8d920-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-217">CSS</span><span class="sxs-lookup"><span data-stu-id="8d920-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-218">Img</span><span class="sxs-lookup"><span data-stu-id="8d920-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-219">Носители</span><span class="sxs-lookup"><span data-stu-id="8d920-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-220">Шрифт</span><span class="sxs-lookup"><span data-stu-id="8d920-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-221">Doc</span><span class="sxs-lookup"><span data-stu-id="8d920-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-222">WS</span><span class="sxs-lookup"><span data-stu-id="8d920-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8d920-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-224">Манифест</span><span class="sxs-lookup"><span data-stu-id="8d920-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-225">Other</span><span class="sxs-lookup"><span data-stu-id="8d920-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-226">Любой другой тип, не указанный в списке.</span><span class="sxs-lookup"><span data-stu-id="8d920-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8d920-227">Если кнопки не отображаются, области **Фильтры** могут быть скрыты.</span><span class="sxs-lookup"><span data-stu-id="8d920-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="8d920-228">Дополнительные сведения можно получить в [области Hide the Filters.](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="8d920-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="8d920-229">Чтобы включить несколько фильтров типа одновременно, удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите.</span><span class="sxs-lookup"><span data-stu-id="8d920-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров Type для отображения ресурсов JS, CSS и Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="8d920-231">Использование фильтров Type для отображения ресурсов JS, CSS и Document</span><span class="sxs-lookup"><span data-stu-id="8d920-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <a name="filter-requests-by-time"></a><span data-ttu-id="8d920-232">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="8d920-232">Filter requests by time</span></span>  

<span data-ttu-id="8d920-233">Выберите и перетащите влево или вправо на области **Обзор,** чтобы отображать только запросы, которые были активны в течение этого срока.</span><span class="sxs-lookup"><span data-stu-id="8d920-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="8d920-234">Фильтр включен.</span><span class="sxs-lookup"><span data-stu-id="8d920-234">The filter is inclusive.</span></span>  <span data-ttu-id="8d920-235">Отображается любой запрос, который был активен в течение выделенного времени.</span><span class="sxs-lookup"><span data-stu-id="8d920-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация любых неактивных запросов на 300 мс" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="8d920-237">Фильтрация любых неактивных запросов на 300 мс</span><span class="sxs-lookup"><span data-stu-id="8d920-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <a name="hide-data-urls"></a><span data-ttu-id="8d920-238">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="8d920-238">Hide data URLs</span></span>  

<span data-ttu-id="8d920-239">[URL-адреса данных —][MDNHTTPDataURIs] это небольшие файлы, встроенные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="8d920-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="8d920-240">Любой запрос, отображаемый в таблице Запросы, который начинается с `data:` url-адреса данных.</span><span class="sxs-lookup"><span data-stu-id="8d920-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="8d920-241">Чтобы скрыть запросы, выключите почтовый **ящик Скрыть URL-адреса** данных.</span><span class="sxs-lookup"><span data-stu-id="8d920-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Почтовый ящик Скрыть URL-адреса данных" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="8d920-243">Почтовый **ящик Скрыть URL-адреса** данных</span><span class="sxs-lookup"><span data-stu-id="8d920-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <a name="sort-requests"></a><span data-ttu-id="8d920-244">Сортировка запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-244">Sort requests</span></span>  

<span data-ttu-id="8d920-245">По умолчанию запросы в таблице Запросы сортироваться по времени начала, но вы можете сортировать таблицу с помощью других критериев.</span><span class="sxs-lookup"><span data-stu-id="8d920-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <a name="sort-by-column"></a><span data-ttu-id="8d920-246">Сортировка по столбцу</span><span class="sxs-lookup"><span data-stu-id="8d920-246">Sort by column</span></span>  

<span data-ttu-id="8d920-247">Выберите заглавную часть любого столбца в запросах для сортировки запросов в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="8d920-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <a name="sort-by-activity-phase"></a><span data-ttu-id="8d920-248">Сортировка по этапу действия</span><span class="sxs-lookup"><span data-stu-id="8d920-248">Sort by activity phase</span></span>  

<span data-ttu-id="8d920-249">Чтобы изменить сортировку запросов в Водопаде, наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\), наведите курсор на **водопад**и выберите один из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="8d920-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-250">Время начала</span><span class="sxs-lookup"><span data-stu-id="8d920-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-251">Первый запрос, который был инициирован, находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="8d920-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-252">Время отклика</span><span class="sxs-lookup"><span data-stu-id="8d920-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-253">Первый запрос, который начал скачивать, находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="8d920-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-254">Время окончания</span><span class="sxs-lookup"><span data-stu-id="8d920-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-255">Первый завершенный запрос находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="8d920-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-256">Общая продолжительность</span><span class="sxs-lookup"><span data-stu-id="8d920-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-257">Запрос с самыми короткими настройками подключения и запросом или ответом находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="8d920-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-258">Задержка</span><span class="sxs-lookup"><span data-stu-id="8d920-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-259">Запрос, который выждал самое короткое время для ответа, находится в верхней части.</span><span class="sxs-lookup"><span data-stu-id="8d920-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8d920-260">В этих описаниях предполагается, что каждый соответствующий параметр занимает место от самого короткого до длинного.</span><span class="sxs-lookup"><span data-stu-id="8d920-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="8d920-261">Выберите заглавную колонку **Водопад,** чтобы изменить порядок.</span><span class="sxs-lookup"><span data-stu-id="8d920-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка водопада по общей продолжительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="8d920-263">Сортировка водопада по общей продолжительности \(Светлая часть каждого бара — это время ожидания, а более темная — время загрузки bytes\)</span><span class="sxs-lookup"><span data-stu-id="8d920-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <a name="analyze-requests"></a><span data-ttu-id="8d920-264">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-264">Analyze requests</span></span>  

<span data-ttu-id="8d920-265">До тех пор, пока DevTools открыты, он регистрит все запросы в **средстве Network.**</span><span class="sxs-lookup"><span data-stu-id="8d920-265">So long as DevTools are open, it logs all requests in the **Network** tool.</span></span>  
<span data-ttu-id="8d920-266">Используйте панель Network для анализа запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-266">Use the Network panel to analyze requests.</span></span>  

### <a name="display-a-log-of-requests"></a><span data-ttu-id="8d920-267">Отображение журнала запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-267">Display a log of requests</span></span>  

<span data-ttu-id="8d920-268">Используйте таблицу Запросы, чтобы отобразить журнал всех запросов, сделанных во время открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d920-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="8d920-269">Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите курсор на запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица Запросов" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="8d920-271">Таблица Запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-272">В таблице Запросы по умолчанию отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="8d920-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-273">Имя</span><span class="sxs-lookup"><span data-stu-id="8d920-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-274">Имя файла ресурса или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d920-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-275">Состояние</span><span class="sxs-lookup"><span data-stu-id="8d920-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-276">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-277">Тип</span><span class="sxs-lookup"><span data-stu-id="8d920-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-278">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d920-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-279">Инициатор</span><span class="sxs-lookup"><span data-stu-id="8d920-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-280">Следующие объекты или процессы инициируют запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="8d920-281">**Parser**  Parser HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8d920-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="8d920-282">**Перенаправление**  Перенаправление HTTP.</span><span class="sxs-lookup"><span data-stu-id="8d920-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="8d920-283">**Сценарий**  Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8d920-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="8d920-284">**Другие**  Некоторые другие процессы или действия, например переход на страницу по ссылке или ввод URL-адреса в панели адресов.</span><span class="sxs-lookup"><span data-stu-id="8d920-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-285">Size</span><span class="sxs-lookup"><span data-stu-id="8d920-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-286">Совокупный размер заглавных заглавных ответов, а также тело ответа, доставленное сервером.</span><span class="sxs-lookup"><span data-stu-id="8d920-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-287">Время</span><span class="sxs-lookup"><span data-stu-id="8d920-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-288">Общая продолжительность от начала запроса до получения окончательного byte в ответе.</span><span class="sxs-lookup"><span data-stu-id="8d920-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="8d920-289">Водопад</span><span class="sxs-lookup"><span data-stu-id="8d920-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-290">Визуальный сбой действия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a><span data-ttu-id="8d920-291">Добавление или удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="8d920-291">Add or remove columns</span></span>  

<span data-ttu-id="8d920-292">Наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\) и выберите вариант, чтобы скрыть или показать его.</span><span class="sxs-lookup"><span data-stu-id="8d920-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="8d920-293">В настоящее время отображаемые параметры имеют контрольные знаки рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="8d920-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу Запросы" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="8d920-295">Добавление столбца в таблицу Запросы</span><span class="sxs-lookup"><span data-stu-id="8d920-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <a name="add-custom-columns"></a><span data-ttu-id="8d920-296">Добавление настраиваемой колонки</span><span class="sxs-lookup"><span data-stu-id="8d920-296">Add custom columns</span></span>  

<span data-ttu-id="8d920-297">Чтобы добавить настраиваемый столбец в таблицу Запросы, наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\) и выберите заглавные таблицы ответа \*\*\*\* Управление столбцами загонщиков  >  \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="8d920-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемой колонки в таблицу Запросы" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="8d920-299">Добавление настраиваемой колонки в таблицу Запросы</span><span class="sxs-lookup"><span data-stu-id="8d920-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a><span data-ttu-id="8d920-300">Отображение отношения времени запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="8d920-301">Использование водопада для отображения связей времени запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="8d920-302">Организация водопада по умолчанию использует время начала запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="8d920-303">Таким образом, запросы, которые находятся дальше слева, начались раньше, чем запросы, которые находятся дальше справа.</span><span class="sxs-lookup"><span data-stu-id="8d920-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="8d920-304">Чтобы просмотреть различные способы сортировки водопада, перейдите к [сортировке по этапу действия.](#sort-by-activity-phase)</span><span class="sxs-lookup"><span data-stu-id="8d920-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Водопад" области Запросы" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="8d920-306">Столбец "Водопад" области **Запросы**</span><span class="sxs-lookup"><span data-stu-id="8d920-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a><span data-ttu-id="8d920-307">Отображение предварительного просмотра тела отклика</span><span class="sxs-lookup"><span data-stu-id="8d920-307">Display a preview of a response body</span></span>  

<span data-ttu-id="8d920-308">Чтобы отобразить предварительный просмотр тела отклика, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-309">Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8d920-310">Выберите панель **Preview.**</span><span class="sxs-lookup"><span data-stu-id="8d920-310">Choose the **Preview** panel.</span></span>  

<span data-ttu-id="8d920-311">Вкладка Preview в основном полезна для отображения изображений.</span><span class="sxs-lookup"><span data-stu-id="8d920-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Панель Предварительного просмотра" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="8d920-313">Панель **Предварительного** просмотра</span><span class="sxs-lookup"><span data-stu-id="8d920-313">The **Preview** panel</span></span>  
:::image-end:::  

### <a name="display-a-response-body"></a><span data-ttu-id="8d920-314">Отображение тела отклика</span><span class="sxs-lookup"><span data-stu-id="8d920-314">Display a response body</span></span>  

<span data-ttu-id="8d920-315">Чтобы отобразить тело ответа на запрос, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-316">Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8d920-317">Выберите панель **ответа.**</span><span class="sxs-lookup"><span data-stu-id="8d920-317">Choose the **Response** panel.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Панель ответов" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="8d920-319">Панель **ответов**</span><span class="sxs-lookup"><span data-stu-id="8d920-319">The **Response** panel</span></span>  
:::image-end:::  

### <a name="display-http-headers"></a><span data-ttu-id="8d920-320">Отображение http-заглавок</span><span class="sxs-lookup"><span data-stu-id="8d920-320">Display HTTP headers</span></span>  

<span data-ttu-id="8d920-321">Чтобы отобразить данные http-header о запросе, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-322">Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8d920-323">Выберите **psanel headers.**</span><span class="sxs-lookup"><span data-stu-id="8d920-323">Choose the **Headers** psanel.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Панель "Заготки"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="8d920-325">Панель **"Заготки"**</span><span class="sxs-lookup"><span data-stu-id="8d920-325">The **Headers** panel</span></span>  
:::image-end:::  

#### <a name="display-http-header-source"></a><span data-ttu-id="8d920-326">Отображение источника заглавной ссылки HTTP</span><span class="sxs-lookup"><span data-stu-id="8d920-326">Display HTTP header source</span></span>  

<span data-ttu-id="8d920-327">По умолчанию панель **headers показывает** имена загона в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="8d920-327">By default, the **Headers** panel shows header names alphabetically.</span></span>  <span data-ttu-id="8d920-328">Чтобы разыграть имена заглавных http в полученном порядке, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-329">Откройте панель **headers** для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="8d920-329">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="8d920-330">Дополнительные сведения см. в загонах [Display HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="8d920-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="8d920-331">Выберите **источник представления**рядом с разделом Заглавка **запроса** или **заглавного ответа.**</span><span class="sxs-lookup"><span data-stu-id="8d920-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <a name="display-query-string-parameters"></a><span data-ttu-id="8d920-332">Отображение параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-332">Display query string parameters</span></span>  

<span data-ttu-id="8d920-333">Чтобы отобразить параметры строки запроса URL-адреса в читаемом для человека формате, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-334">Откройте панель **headers** для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="8d920-334">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="8d920-335">Дополнительные сведения см. в загонах [Display HTTP.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="8d920-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="8d920-336">Перейдите к **разделу Параметры строки запроса.**</span><span class="sxs-lookup"><span data-stu-id="8d920-336">Navigate to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел Параметры строки запроса" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="8d920-338">Раздел **Параметры строки запроса**</span><span class="sxs-lookup"><span data-stu-id="8d920-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a><span data-ttu-id="8d920-339">Отображение источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-339">Display query string parameters source</span></span>  

<span data-ttu-id="8d920-340">Чтобы отобразить источник параметров строки запроса, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-341">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-341">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="8d920-342">Дополнительные сведения перейдите к [параметрам строки отображения запроса.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="8d920-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="8d920-343">Выберите **источник представления**.</span><span class="sxs-lookup"><span data-stu-id="8d920-343">Choose **view source**.</span></span>  

#### <a name="display-url-encoded-query-string-parameters"></a><span data-ttu-id="8d920-344">Отображение параметров строки строки запроса с кодом URL-адресов</span><span class="sxs-lookup"><span data-stu-id="8d920-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="8d920-345">Чтобы отобразить параметры строки запроса в читаемом для человека формате, но с сохраненными кодированием, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-346">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-346">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="8d920-347">Дополнительные сведения перейдите к [параметрам строки отображения запроса.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="8d920-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="8d920-348">Выберите **закодированный URL-адрес просмотра.**</span><span class="sxs-lookup"><span data-stu-id="8d920-348">Choose **view URL encoded**.</span></span>  

### <a name="display-cookies"></a><span data-ttu-id="8d920-349">Отображение файлов cookie</span><span class="sxs-lookup"><span data-stu-id="8d920-349">Display cookies</span></span>  

<span data-ttu-id="8d920-350">Чтобы отобразить файлы cookie, отправленные в http-header запроса, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-351">Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8d920-352">Выберите панель **cookies.**</span><span class="sxs-lookup"><span data-stu-id="8d920-352">Choose the **Cookies** panel.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Панель cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="8d920-354">Панель cookies</span><span class="sxs-lookup"><span data-stu-id="8d920-354">The Cookies panel</span></span>  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a><span data-ttu-id="8d920-355">Отображение разбивки по времени запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="8d920-356">Чтобы отобразить разбивку по времени запроса, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="8d920-357">Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.</span><span class="sxs-lookup"><span data-stu-id="8d920-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="8d920-358">Выберите панель **Timing.**</span><span class="sxs-lookup"><span data-stu-id="8d920-358">Choose the **Timing** panel.</span></span>  

<span data-ttu-id="8d920-359">Чтобы быстрее получить доступ к данным, перейдите к [предварительному просмотру разбивки по времени.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="8d920-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="8d920-360">Дополнительные сведения о каждом из этапов, которые могут отображаться в панели **Timing,** перейдите к этапам разбивки [синхронизации.](#timing-breakdown-phases-explained)</span><span class="sxs-lookup"><span data-stu-id="8d920-360">For more information about each of the phases that may be displayed in the **Timing** panel, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Панель синхронизации" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="8d920-362">Панель **синхронизации**</span><span class="sxs-lookup"><span data-stu-id="8d920-362">The **Timing** panel</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-363">Дополнительные сведения о каждом из этапов.</span><span class="sxs-lookup"><span data-stu-id="8d920-363">More information about each of the phases.</span></span>  

<span data-ttu-id="8d920-364">Дополнительные сведения о доступе к дисплею перейдите к [разбивке по времени отображения.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="8d920-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <a name="preview-a-timing-breakdown"></a><span data-ttu-id="8d920-365">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="8d920-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="8d920-366">Чтобы отобразить предварительный просмотр разбивки времени запроса, в столбце **Водопад** таблицы Запросов наведите курсор на запись для запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="8d920-367">Дополнительные сведения о том, как получить доступ к данным без нависания, перейдите к отображения разбивки по времени [запроса](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="8d920-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбивки по времени запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="8d920-369">Просмотр разбивки по времени запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a><span data-ttu-id="8d920-370">Объяснены этапы разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="8d920-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="8d920-371">Дополнительные сведения о каждом из этапов, которые могут отображаться в панели **Timing.**</span><span class="sxs-lookup"><span data-stu-id="8d920-371">More information about each of the phases that may display in the **Timing** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-372">Очередь</span><span class="sxs-lookup"><span data-stu-id="8d920-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-373">В очередях браузера запрашиваются запросы, если любое из следующих запросов является верным.</span><span class="sxs-lookup"><span data-stu-id="8d920-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="8d920-374">Существуют запросы на более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="8d920-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="8d920-375">Шесть подключений TCP открыты для одного и того же происхождения, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="8d920-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="8d920-376">Применяется только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="8d920-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="8d920-377">Браузер ненадолго размешает пространство в кэше диска.</span><span class="sxs-lookup"><span data-stu-id="8d920-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-378">Приостановка</span><span class="sxs-lookup"><span data-stu-id="8d920-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-379">Запрос застопоряется по любой из причин, описанных в **очереди.**</span><span class="sxs-lookup"><span data-stu-id="8d920-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-380">DNS Lookup</span><span class="sxs-lookup"><span data-stu-id="8d920-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-381">Браузер решает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-382">Начальное подключение</span><span class="sxs-lookup"><span data-stu-id="8d920-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-383">Браузер устанавливает подключение, включая рукопожатия TCP, TCP-инслементы и переговоры по безопасному слою socket.</span><span class="sxs-lookup"><span data-stu-id="8d920-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-384">Согласование прокси</span><span class="sxs-lookup"><span data-stu-id="8d920-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-385">Браузер ведет переговоры по запросу с [прокси-сервером.][WikiProxyServer]</span><span class="sxs-lookup"><span data-stu-id="8d920-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-386">Отправленный запрос</span><span class="sxs-lookup"><span data-stu-id="8d920-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-387">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="8d920-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-388">Подготовка serviceWorker</span><span class="sxs-lookup"><span data-stu-id="8d920-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-389">Браузер начинает рабочий службы.</span><span class="sxs-lookup"><span data-stu-id="8d920-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-390">Запрос в ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="8d920-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-391">Запрос отправляется работнику службы.</span><span class="sxs-lookup"><span data-stu-id="8d920-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-392">Ожидание \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="8d920-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-393">Браузер ожидает первого byte ответа.</span><span class="sxs-lookup"><span data-stu-id="8d920-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="8d920-394">TTFB означает "Время для первого byte".</span><span class="sxs-lookup"><span data-stu-id="8d920-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="8d920-395">Это время включает одну поездку в конец задержки и время, необходимое серверу для подготовки ответа.</span><span class="sxs-lookup"><span data-stu-id="8d920-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-396">Загрузка контента</span><span class="sxs-lookup"><span data-stu-id="8d920-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-397">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="8d920-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-398">Получение push</span><span class="sxs-lookup"><span data-stu-id="8d920-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-399">Браузер получает данные для этого ответа с помощью http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="8d920-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="8d920-400">Чтение Push</span><span class="sxs-lookup"><span data-stu-id="8d920-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="8d920-401">Браузер читает полученные ранее локальные данные.</span><span class="sxs-lookup"><span data-stu-id="8d920-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a><span data-ttu-id="8d920-402">Отображение инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="8d920-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="8d920-403">Чтобы отобразить инициаторов и зависимостей запроса, удерживайте и наведите курсор на запрос `Shift` в таблице Запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="8d920-404">Цвета DevTools: инициаторы показаны зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="8d920-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="8d920-406">Отображение инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-407">Если таблица Запросов задается в хронологическом порядке, если вы наведите курсор на строку, в строке, предшествуемой этой строке, отображается зеленый запрос.</span><span class="sxs-lookup"><span data-stu-id="8d920-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="8d920-408">Зеленый запрос является инициатором зависимости.</span><span class="sxs-lookup"><span data-stu-id="8d920-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="8d920-409">Если еще один зеленый запрос отображается на строке до этого, этот более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="8d920-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="8d920-410">И так далее.</span><span class="sxs-lookup"><span data-stu-id="8d920-410">And so on.</span></span>  

### <a name="display-load-events"></a><span data-ttu-id="8d920-411">Отображение событий загрузки</span><span class="sxs-lookup"><span data-stu-id="8d920-411">Display load events</span></span>  

<span data-ttu-id="8d920-412">DevTools отображает время событий и событий в нескольких `DOMContentLoaded` `load` местах в **средстве Network.**</span><span class="sxs-lookup"><span data-stu-id="8d920-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** tool.</span></span>  <span data-ttu-id="8d920-413">Событие `DOMContentLoaded` имеет синий цвет, а событие — `load` красный.</span><span class="sxs-lookup"><span data-stu-id="8d920-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и загрузки на панели Network" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="8d920-415">Расположение и события `DOMContentLoaded` `load` в средстве **Network**</span><span class="sxs-lookup"><span data-stu-id="8d920-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** tool</span></span>  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a><span data-ttu-id="8d920-416">Отображение общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-416">Display the total number of requests</span></span>  

<span data-ttu-id="8d920-417">Общее число запросов перечислены в области **Сводка** в нижней части **средства Network.**</span><span class="sxs-lookup"><span data-stu-id="8d920-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="8d920-418">Это число отслеживает только запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d920-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="8d920-419">Если другие запросы происходили до открытия DevTools, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="8d920-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее число запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="8d920-421">Общее число запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="8d920-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <a name="display-the-total-download-size"></a><span data-ttu-id="8d920-422">Отображение общего размера загрузки</span><span class="sxs-lookup"><span data-stu-id="8d920-422">Display the total download size</span></span>  

<span data-ttu-id="8d920-423">Общий размер запросов скачивания указан в области **Сводка** в нижней части **средства Network.**</span><span class="sxs-lookup"><span data-stu-id="8d920-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="8d920-424">Это число отслеживает только запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="8d920-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="8d920-425">Если другие запросы произошли до открытия DevTools, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="8d920-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий размер запросов загрузки" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="8d920-427">Общий размер запросов загрузки</span><span class="sxs-lookup"><span data-stu-id="8d920-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-428">Чтобы проверить, насколько большие ресурсы после того, как браузер отпечатает каждый элемент, перейдите, чтобы отобразить ненапечатаный [размер ресурса.](#display-the-uncompressed-size-of-a-resource)</span><span class="sxs-lookup"><span data-stu-id="8d920-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <a name="display-the-stack-trace-that-caused-a-request"></a><span data-ttu-id="8d920-429">Отображение трассировки стека, вызываемой запросом</span><span class="sxs-lookup"><span data-stu-id="8d920-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="8d920-430">После запроса ресурса в заявлении JavaScript наведите курсор на столбец Инициатор, чтобы отобразить след стека, ведущий к запросу. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="8d920-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="След стека, ведущий к запросу ресурса" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="8d920-432">След стека, ведущий к запросу ресурса</span><span class="sxs-lookup"><span data-stu-id="8d920-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a><span data-ttu-id="8d920-433">Отображение неконтпрессивного размера ресурса</span><span class="sxs-lookup"><span data-stu-id="8d920-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="8d920-434">Включив **почтовый ящик Use large request rows,** а затем просмотрите нижнее значение столбца **Size.**</span><span class="sxs-lookup"><span data-stu-id="8d920-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример uncompressed resources" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="8d920-436">Пример некомпрессивных ресурсов \(Сжатый размер файла, отправленного по сети, был , в то время как некомпрессованный размер `jquery-3.3.1.min.js` `29.9 KB` был `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="8d920-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <a name="export-requests-data"></a><span data-ttu-id="8d920-437">Экспорт запросов данных</span><span class="sxs-lookup"><span data-stu-id="8d920-437">Export requests data</span></span>  

### <a name="save-all-network-requests-to-a-har-file"></a><span data-ttu-id="8d920-438">Сохранение всех сетевых запросов в файл HAR</span><span class="sxs-lookup"><span data-stu-id="8d920-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="8d920-439">Чтобы сохранить все сетевые запросы в файл HAR, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="8d920-440">Наведите курсор на любой запрос в таблице Запросы и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="8d920-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="8d920-441">Выберите **Сохранить как HAR с контентом**.</span><span class="sxs-lookup"><span data-stu-id="8d920-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="8d920-442">DevTools сохраняет все запросы, которые произошли с момента открытия DevTools для файла HAR.</span><span class="sxs-lookup"><span data-stu-id="8d920-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="8d920-443">Вы не можете фильтровать запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-443">You are not able to filter requests.</span></span>  <span data-ttu-id="8d920-444">Вы также не можете сохранить один запрос.</span><span class="sxs-lookup"><span data-stu-id="8d920-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="8d920-445">После сохранения файла HAR вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="8d920-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="8d920-446">Просто перетащите и сбросите файл HAR в таблицу Запросы.</span><span class="sxs-lookup"><span data-stu-id="8d920-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выберите Сохранить как HAR с контентом" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="8d920-448">Выберите **Сохранить как HAR с контентом**</span><span class="sxs-lookup"><span data-stu-id="8d920-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a><span data-ttu-id="8d920-449">Скопируйте один или несколько запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="8d920-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="8d920-450">В **столбце Имя** таблицы Запросы наведите курсор на запрос, откройте контекстное меню \(правой кнопкой мыши\), наведите курсор на **копию**и выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="8d920-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="8d920-451">Название</span><span class="sxs-lookup"><span data-stu-id="8d920-451">Name</span></span> | <span data-ttu-id="8d920-452">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="8d920-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="8d920-453">Адрес ссылки копирования</span><span class="sxs-lookup"><span data-stu-id="8d920-453">Copy Link Address</span></span>** | <span data-ttu-id="8d920-454">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="8d920-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="8d920-455">Копирование ответа</span><span class="sxs-lookup"><span data-stu-id="8d920-455">Copy Response</span></span>** | <span data-ttu-id="8d920-456">Скопируйте текст ответа на буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="8d920-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="8d920-457">Скопируйте как fetch</span><span class="sxs-lookup"><span data-stu-id="8d920-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="8d920-458">Скопируйте как cURL</span><span class="sxs-lookup"><span data-stu-id="8d920-458">Copy as cURL</span></span>** | <span data-ttu-id="8d920-459">Скопируйте запрос в качестве команды cURL.</span><span class="sxs-lookup"><span data-stu-id="8d920-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="8d920-460">Скопируйте все как fetch</span><span class="sxs-lookup"><span data-stu-id="8d920-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="8d920-461">Скопируйте все как cURL</span><span class="sxs-lookup"><span data-stu-id="8d920-461">Copy All as cURL</span></span>** | <span data-ttu-id="8d920-462">Скопируйте все запросы в виде цепочки команд cURL.</span><span class="sxs-lookup"><span data-stu-id="8d920-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="8d920-463">Скопируйте все как HAR</span><span class="sxs-lookup"><span data-stu-id="8d920-463">Copy All as HAR</span></span>** | <span data-ttu-id="8d920-464">Скопируйте все запросы в виде данных HAR.</span><span class="sxs-lookup"><span data-stu-id="8d920-464">Copy all requests as HAR data.</span></span> |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор ответа на копирование" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="8d920-466">Выбор **ответа на копирование**</span><span class="sxs-lookup"><span data-stu-id="8d920-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a><span data-ttu-id="8d920-467">Скопируйте форматированный ответ JSON на буфер обмена</span><span class="sxs-lookup"><span data-stu-id="8d920-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="8d920-468">Выберите сетевой запрос и перейдите на области **headers.**</span><span class="sxs-lookup"><span data-stu-id="8d920-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="8d920-469">Чтобы скопировать значение JSON ответа, \*\*\*\* перейдите на запрос полезной нагрузки, наведите курсор на содержимое отклика JSON, откройте контекстное меню \(правой кнопкой мыши\) и выберите значение **Copy Value**.</span><span class="sxs-lookup"><span data-stu-id="8d920-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Скопируйте значение в контекстной меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="8d920-471">**Скопируйте значение** в контекстной меню</span><span class="sxs-lookup"><span data-stu-id="8d920-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Код Visual Studio Microsoft с форматированный ответ JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="8d920-473">Вклеить форматированный ответ JSON в Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="8d920-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a><span data-ttu-id="8d920-474">Копирование значений свойств из сетевых запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="8d920-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="8d920-475">Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8d920-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="8d920-476">Откройте области **заготки.**</span><span class="sxs-lookup"><span data-stu-id="8d920-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="8d920-477">Откройте один из следующих разделов загона.</span><span class="sxs-lookup"><span data-stu-id="8d920-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="8d920-478">Запрос полезной нагрузки \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="8d920-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="8d920-479">Данные форм</span><span class="sxs-lookup"><span data-stu-id="8d920-479">Form Data</span></span>  
    *   <span data-ttu-id="8d920-480">Параметры строки запроса</span><span class="sxs-lookup"><span data-stu-id="8d920-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="8d920-481">Запрашивать заглавные</span><span class="sxs-lookup"><span data-stu-id="8d920-481">Request Headers</span></span>  
    *   <span data-ttu-id="8d920-482">Заготчики ответа</span><span class="sxs-lookup"><span data-stu-id="8d920-482">Response Headers</span></span>  
1.  <span data-ttu-id="8d920-483">Откройте контекстное меню \(правой кнопкой мыши\) > **значение Copy**.</span><span class="sxs-lookup"><span data-stu-id="8d920-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="8d920-484">Теперь вы можете вклеить значение в любой редактор, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="8d920-484">You may now paste the value into any editor to review it.</span></span>  
    
## <a name="change-the-layout-of-the-network-panel"></a><span data-ttu-id="8d920-485">Изменение макета панели Network</span><span class="sxs-lookup"><span data-stu-id="8d920-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="8d920-486">Вы можете расширить или обвалить **разделы** пользовательского интерфейса сетевых инструментов, чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="8d920-486">You may expand or collapse sections of the **Network** tool UI to focus important information.</span></span>  

### <a name="hide-the-filters-pane"></a><span data-ttu-id="8d920-487">Скрыть области фильтров</span><span class="sxs-lookup"><span data-stu-id="8d920-487">Hide the Filters pane</span></span>  

<span data-ttu-id="8d920-488">По умолчанию в DevTools покажут **области фильтров.**</span><span class="sxs-lookup"><span data-stu-id="8d920-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="8d920-489">Выберите **фильтр** \( ![ Фильтр ](../media/filter-icon.msft.png) \) для его сокрытия.</span><span class="sxs-lookup"><span data-stu-id="8d920-489">Choose **Filter** \(![Filter](../media/filter-icon.msft.png)\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "Скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="8d920-491">Кнопка "Скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="8d920-491">The Hide Filters button</span></span>  
:::image-end:::  

### <a name="use-large-request-rows"></a><span data-ttu-id="8d920-492">Использование больших строк запросов</span><span class="sxs-lookup"><span data-stu-id="8d920-492">Use large request rows</span></span>  

<span data-ttu-id="8d920-493">Используйте большие строки, если в таблице сетевых запросов нужно больше белого пространства.</span><span class="sxs-lookup"><span data-stu-id="8d920-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="8d920-494">Некоторые столбцы также предоставляют дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="8d920-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="8d920-495">Например, нижнее значение столбца **Size** — это ненапечатаный размер запроса.</span><span class="sxs-lookup"><span data-stu-id="8d920-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример больших строк запросов в области Запросы" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="8d920-497">Пример больших строк запросов в области **Запросы**</span><span class="sxs-lookup"><span data-stu-id="8d920-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="8d920-498">Чтобы включить большие строки, включим почтовый ящик **Use large request rows.**</span><span class="sxs-lookup"><span data-stu-id="8d920-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Почтовый ящик Use large request rows" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="8d920-500">Почтовый **ящик Use large request rows**</span><span class="sxs-lookup"><span data-stu-id="8d920-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <a name="hide-the-overview-pane"></a><span data-ttu-id="8d920-501">Скрыть области Обзор</span><span class="sxs-lookup"><span data-stu-id="8d920-501">Hide the Overview pane</span></span>  

<span data-ttu-id="8d920-502">По умолчанию в DevTools отображается области **Обзор.**</span><span class="sxs-lookup"><span data-stu-id="8d920-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="8d920-503">Чтобы скрыть это, выключите **контрольный ящик "Обзор** шоу".</span><span class="sxs-lookup"><span data-stu-id="8d920-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Контрольный ящик "Обзор шоу"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="8d920-505">Контрольный **ящик "Обзор** шоу"</span><span class="sxs-lookup"><span data-stu-id="8d920-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8d920-506">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8d920-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Отламывка прогрессивных веб-приложений | Документы Майкрософт"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедия"  

> [!NOTE]
> <span data-ttu-id="8d920-510">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d920-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8d920-511">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="8d920-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8d920-513">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d920-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
