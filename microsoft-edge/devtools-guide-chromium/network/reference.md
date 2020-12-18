---
description: Полная справка по функциям панели Сети Microsoft Edge DevTools.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c600197ffa0e415fe42aecc704a523d1b23f8260
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230756"
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

# <span data-ttu-id="c096c-104">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="c096c-104">Network Analysis reference</span></span>  

<span data-ttu-id="c096c-105">Узнайте о новых способах анализа загрузки страницы в этой комплексной ссылке на функции анализа сети Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="c096c-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <span data-ttu-id="c096c-106">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-106">Record network requests</span></span>  

<span data-ttu-id="c096c-107">По умолчанию DevTools записи все \*\*\*\* сетевые запросы в области сети, если DevTools открыт.</span><span class="sxs-lookup"><span data-stu-id="c096c-107">By default, DevTools record all network requests in the **Network** panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель "Сеть"" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="c096c-109">Панель **"Сеть"**</span><span class="sxs-lookup"><span data-stu-id="c096c-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-110">Остановка записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-110">Stop recording network requests</span></span>  

<span data-ttu-id="c096c-111">Чтобы остановить запись запросов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c096c-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="c096c-112">On the **Network** panel, choose **Stop recording network log** \( Stop recording network log ![ ][ImageRecordOnIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c096c-112">On the **Network** panel, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="c096c-113">Серый цвет означает, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="c096c-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="c096c-114">Выберите `Control` + `E` \(Windows, Linux\) или `Command` + `E` \(macOS\) в \*\*\*\* то время как панель сети находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="c096c-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="c096c-115">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-115">Clear requests</span></span>  

<span data-ttu-id="c096c-116">Choose **Clear** \( ![ Clear ][ImageClearIcon] \) on the **Network** panel to clear all requests from the Requests table.</span><span class="sxs-lookup"><span data-stu-id="c096c-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка "Очистить"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="c096c-118">Кнопка **"Очистить"**</span><span class="sxs-lookup"><span data-stu-id="c096c-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-119">Сохранение запросов во время загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="c096c-119">Save requests across page loads</span></span>  

<span data-ttu-id="c096c-120">Чтобы сохранить запросы между загрузками \*\*\*\* страниц, на панели "Сеть" включите для журнала сохранения. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-120">To save requests across page loads, on the **Network** panel, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="c096c-121">DevTools сохраняет все запросы, пока вы не отключите журнал **сохранения.**</span><span class="sxs-lookup"><span data-stu-id="c096c-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="The Preserve Log checkbox" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="c096c-123">The **Preserve Log** checkbox</span><span class="sxs-lookup"><span data-stu-id="c096c-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-124">Снимки экрана во время загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="c096c-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="c096c-125">Снимите снимки экрана, чтобы проанализировать отображаемую информацию для пользователей в ожидании загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="c096c-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="c096c-126">Чтобы включить снимки экрана, выберите **"Параметры** **сети"** \*\*\*\* и на панели "Сеть" включит этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c096c-126">To enable screenshots, choose **Network settings**, and on the **Network** panel, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="c096c-127">Обновите **страницу,** пока панель "Сеть" находится в фокусе для снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="c096c-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="c096c-128">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="c096c-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="c096c-129">Наведите указатель мыши на снимок экрана, чтобы отобразить точку, в которую был сделан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="c096c-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="c096c-130">Желтая линия отображается на области **обзора.**</span><span class="sxs-lookup"><span data-stu-id="c096c-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="c096c-131">Выберите эскиз экрана, чтобы отфильтровать все запросы, которые произошли после снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="c096c-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="c096c-132">Дважды щелкните эскиз, чтобы увеличить его масштаб.</span><span class="sxs-lookup"><span data-stu-id="c096c-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведите курсор на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="c096c-134">Наведите курсор на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="c096c-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="c096c-135">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="c096c-135">Change loading behavior</span></span>  

### <span data-ttu-id="c096c-136">Эмуляция первого посетителя путем отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="c096c-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="c096c-137">Чтобы эмулировать, как пользователь впервые работает с сайтом, включите этот контрольный ящик. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="c096c-138">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="c096c-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="c096c-139">Эта функция более точно эмулирует интерфейс первого пользователя, так как запросы обслуживаются из кэша браузера при повторяемом посещении.</span><span class="sxs-lookup"><span data-stu-id="c096c-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="The Disable Cache checkbox" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="c096c-141">The **Disable Cache** checkbox</span><span class="sxs-lookup"><span data-stu-id="c096c-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="c096c-142">Отключение кэша браузера из окна "Условия сети"</span><span class="sxs-lookup"><span data-stu-id="c096c-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="c096c-143">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте ящик условий сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="c096c-144">Откройте ящик **условий** сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="c096c-145">Включите (или выключите\) почтовый ящик отключения **кэша.**</span><span class="sxs-lookup"><span data-stu-id="c096c-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="c096c-146">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="c096c-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="c096c-147">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню \(щелкните правой кнопкой мыши\) в любом месте таблицы "Запросы" и выберите "Очистить **кэш браузера".**</span><span class="sxs-lookup"><span data-stu-id="c096c-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор "Очистить кэш браузера"" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="c096c-149">Выбор **"Очистить кэш браузера"**</span><span class="sxs-lookup"><span data-stu-id="c096c-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-150">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="c096c-150">Emulate offline</span></span>  

<span data-ttu-id="c096c-151">Новый класс веб-приложений, с именем [Progressive Web Apps,][DevtoolsProgressiveWebApps]работает в автономном режиме с помощью **сотрудников службы.**</span><span class="sxs-lookup"><span data-stu-id="c096c-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="c096c-152">Может оказаться полезным быстро смоделировать устройство без подключения к данным при создании приложения такого типа.</span><span class="sxs-lookup"><span data-stu-id="c096c-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="c096c-153">Выберите меню **"Интернет",** найщите в меню **"Предусмотрить"** и выберите **"Автономный",** чтобы имитировать работу в автономной сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Автономное меню" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="c096c-155">Автономное **меню**</span><span class="sxs-lookup"><span data-stu-id="c096c-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-156">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="c096c-156">Emulate slow network connections</span></span>  

<span data-ttu-id="c096c-157">Эмулировать медленную 3G, быструю 3G и другие скорости подключения из меню **"Интернет".**</span><span class="sxs-lookup"><span data-stu-id="c096c-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="c096c-159">Меню **регулирования**</span><span class="sxs-lookup"><span data-stu-id="c096c-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-160">Вы можете выбрать один из разных предугодий, например Медленную 3G или быструю 3G.</span><span class="sxs-lookup"><span data-stu-id="c096c-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="c096c-161">Чтобы добавить собственные настраиваемые предустанавливные таблицы, откройте меню регулирования и выберите **пункт "Добавить настраиваемую".**  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="c096c-162">DevTools отображает значок предупреждения \*\*\*\* рядом с вкладкой "Сеть", чтобы напомнить, что регулирование включено.</span><span class="sxs-lookup"><span data-stu-id="c096c-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="c096c-163">Эмуляция медленных сетевых подключений из обоймы "Условия сети"</span><span class="sxs-lookup"><span data-stu-id="c096c-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="c096c-164">Если вы хотите улажить сетевое подключение при работе на других панелях DevTools, используйте ящик условий сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="c096c-165">Откройте ящик **условий** сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="c096c-166">Выберите скорость подключения в меню **регулирования.**</span><span class="sxs-lookup"><span data-stu-id="c096c-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="c096c-167">Ручная очистка файлов cookie браузера</span><span class="sxs-lookup"><span data-stu-id="c096c-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="c096c-168">Чтобы вручную очистить файлы cookie браузера в любое время, наведите курсор в любом месте таблицы "Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Очистить файлы **cookie браузера".**</span><span class="sxs-lookup"><span data-stu-id="c096c-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор "Очистить файлы cookie" в браузере" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="c096c-170">Выбор **"Очистить файлы cookie" в браузере**</span><span class="sxs-lookup"><span data-stu-id="c096c-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-171">Переопределения агента пользователя</span><span class="sxs-lookup"><span data-stu-id="c096c-171">Override the user agent</span></span>  

<span data-ttu-id="c096c-172">Чтобы вручную переопрепредить агент пользователя, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-173">Откройте ящик **условий** сети.</span><span class="sxs-lookup"><span data-stu-id="c096c-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="c096c-174">Отключите **автоматический контрольный ящик** "Выбрать".</span><span class="sxs-lookup"><span data-stu-id="c096c-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="c096c-175">Выберите в меню параметр агента пользователя или введите настраиваемый параметр в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="c096c-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="c096c-176">Запросы фильтра</span><span class="sxs-lookup"><span data-stu-id="c096c-176">Filter requests</span></span>  

### <span data-ttu-id="c096c-177">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="c096c-177">Filter requests by properties</span></span>  

<span data-ttu-id="c096c-178">Используйте **текстовое** поле фильтра для фильтрации запросов по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="c096c-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="c096c-179">Если текстовое поле не отображается, возможно, она скрыта. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="c096c-180">Дополнительные сведения можно найти в [области "Скрыть фильтры".](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="c096c-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле фильтра" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="c096c-182">Текстовое **поле фильтра**</span><span class="sxs-lookup"><span data-stu-id="c096c-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-183">Можно использовать несколько свойств одновременно, разделяя каждое свойство пробелом.</span><span class="sxs-lookup"><span data-stu-id="c096c-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="c096c-184">Например, `mime-type:image/png larger-than:1K` отображаются все PNG, размером более 1 килобайта.</span><span class="sxs-lookup"><span data-stu-id="c096c-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="c096c-185">Фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="c096c-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="c096c-186">в настоящее время операции не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c096c-186">operations are currently not supported.</span></span>  

<span data-ttu-id="c096c-187">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="c096c-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="c096c-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="c096c-188">Property</span></span> | <span data-ttu-id="c096c-189">Сведения</span><span class="sxs-lookup"><span data-stu-id="c096c-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="c096c-190">Отображаются только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="c096c-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="c096c-191">Чтобы включить несколько доменов, можно использовать поддиаограмму `*` \( \).</span><span class="sxs-lookup"><span data-stu-id="c096c-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="c096c-192">Например, `*.com` отображаются ресурсы из всех доменных имен, заканчивающийся `.com` на .</span><span class="sxs-lookup"><span data-stu-id="c096c-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="c096c-193">DevTools заполняет меню автозаполнеия всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="c096c-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="c096c-194">Отображает ресурсы, содержащие указанный заголок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="c096c-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="c096c-195">DevTools заполнит в dropdown автозаполнеть все найденные загон ответа.</span><span class="sxs-lookup"><span data-stu-id="c096c-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="c096c-196">Используйте `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c096c-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="c096c-197">Отображает ресурсы, размером больше указанного размера, в ветвях.</span><span class="sxs-lookup"><span data-stu-id="c096c-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="c096c-198">Установка значения `1000` эквивалентна установке значения `1k` .</span><span class="sxs-lookup"><span data-stu-id="c096c-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="c096c-199">Отображает ресурсы, полученные по указанному типу метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="c096c-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="c096c-200">DevTools заполните в этом выпадаке все найденные методы HTTP.</span><span class="sxs-lookup"><span data-stu-id="c096c-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="c096c-201">Отображает ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="c096c-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="c096c-202">DevTools заполните в этом выпадаке все найденные типы MIME.</span><span class="sxs-lookup"><span data-stu-id="c096c-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="c096c-203">Показать все ресурсы смешанного содержимого \( \) или только те, которые отображаются в настоящее время `mixed-content:all` \( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="c096c-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="c096c-204">Отображает ресурсы, извлеченные через незащищенный HTTP \( \) или защищенный `scheme:http` HTTPS \( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="c096c-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="c096c-205">Отображает ресурсы с `Set-Cookie` заголковым `Domain` атрибутом, который соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="c096c-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="c096c-206">DevTools заполняет автозаполнеть всеми найденными доменами cookie.</span><span class="sxs-lookup"><span data-stu-id="c096c-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="c096c-207">Отображает ресурсы с `Set-Cookie` заголковой именем, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="c096c-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="c096c-208">DevTools заполняет автозаполнеть все найденные имена файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="c096c-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="c096c-209">Отображает ресурсы, которые имеют заголок со значением, `Set-Cookie` которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="c096c-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="c096c-210">DevTools заполняет автозаполнеть всеми найденными значениями файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="c096c-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="c096c-211">Отображает ресурсы, которые соответствуют определенному коду состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="c096c-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="c096c-212">DevTools заполняет меню автозаполнеия всеми найденными кодами состояния.</span><span class="sxs-lookup"><span data-stu-id="c096c-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="c096c-213">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="c096c-213">Filter requests by type</span></span>  

<span data-ttu-id="c096c-214">Чтобы отфильтровать запросы по типу запроса, выберите одну из следующих кнопок на панели **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="c096c-214">To filter requests by request type, choose the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-215">XHR</span><span class="sxs-lookup"><span data-stu-id="c096c-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-216">JS</span><span class="sxs-lookup"><span data-stu-id="c096c-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-217">CSS</span><span class="sxs-lookup"><span data-stu-id="c096c-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-218">Img</span><span class="sxs-lookup"><span data-stu-id="c096c-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-219">Media</span><span class="sxs-lookup"><span data-stu-id="c096c-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-220">Шрифт</span><span class="sxs-lookup"><span data-stu-id="c096c-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-221">Doc</span><span class="sxs-lookup"><span data-stu-id="c096c-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-222">WS</span><span class="sxs-lookup"><span data-stu-id="c096c-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="c096c-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-224">Манифест</span><span class="sxs-lookup"><span data-stu-id="c096c-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-225">Other</span><span class="sxs-lookup"><span data-stu-id="c096c-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-226">Любой другой тип не указан.</span><span class="sxs-lookup"><span data-stu-id="c096c-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c096c-227">Если кнопки не отображаются, \*\*\*\* может быть скрыта области фильтров.</span><span class="sxs-lookup"><span data-stu-id="c096c-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="c096c-228">Дополнительные сведения можно найти в [области "Скрыть фильтры".](#hide-the-filters-pane)</span><span class="sxs-lookup"><span data-stu-id="c096c-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="c096c-229">Чтобы включить несколько фильтров типов одновременно, удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите его.</span><span class="sxs-lookup"><span data-stu-id="c096c-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров type для отображения ресурсов JS, CSS и Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="c096c-231">Использование фильтров type для отображения ресурсов JS, CSS и Document</span><span class="sxs-lookup"><span data-stu-id="c096c-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-232">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="c096c-232">Filter requests by time</span></span>  

<span data-ttu-id="c096c-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span><span class="sxs-lookup"><span data-stu-id="c096c-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="c096c-234">Фильтр включен.</span><span class="sxs-lookup"><span data-stu-id="c096c-234">The filter is inclusive.</span></span>  <span data-ttu-id="c096c-235">Отображается любой запрос, который был активен в течение выделенного времени.</span><span class="sxs-lookup"><span data-stu-id="c096c-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация всех неактивных запросов со 300 мс" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="c096c-237">Фильтрация всех неактивных запросов со 300 мс</span><span class="sxs-lookup"><span data-stu-id="c096c-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-238">Скрытие URL-адресов данных</span><span class="sxs-lookup"><span data-stu-id="c096c-238">Hide data URLs</span></span>  

<span data-ttu-id="c096c-239">[URL-адреса данных —][MDNHTTPDataURIs] это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="c096c-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="c096c-240">Любой запрос, который отображается в таблице "Запросы", начинается с `data:` URL-адреса данных.</span><span class="sxs-lookup"><span data-stu-id="c096c-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="c096c-241">Чтобы скрыть запросы, отключите проверку **"Скрыть URL-адреса** данных".</span><span class="sxs-lookup"><span data-stu-id="c096c-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="The Hide Data URLs checkbox" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="c096c-243">The **Hide Data URLs** checkbox</span><span class="sxs-lookup"><span data-stu-id="c096c-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="c096c-244">Запросы на сортировку</span><span class="sxs-lookup"><span data-stu-id="c096c-244">Sort requests</span></span>  

<span data-ttu-id="c096c-245">По умолчанию запросы в таблице "Запросы" сортироваться по времени начала, но можно сортировать таблицу по другим критериям.</span><span class="sxs-lookup"><span data-stu-id="c096c-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="c096c-246">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="c096c-246">Sort by column</span></span>  

<span data-ttu-id="c096c-247">Выберите за колонок любого столбца в запросах, чтобы отсортировать запросы по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="c096c-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="c096c-248">Сортировка по этапу действия</span><span class="sxs-lookup"><span data-stu-id="c096c-248">Sort by activity phase</span></span>  

<span data-ttu-id="c096c-249">Чтобы изменить параметров сортировки запросов в каскадной среде, наведите курсор на загон таблицы \*\*\*\*"Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\), наведите курсор на Каскад и выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="c096c-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-250">Время начала</span><span class="sxs-lookup"><span data-stu-id="c096c-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-251">Первый запрос, который был инициирован, находится вверху.</span><span class="sxs-lookup"><span data-stu-id="c096c-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-252">Время отклика</span><span class="sxs-lookup"><span data-stu-id="c096c-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-253">Первый запрос, который начал скачивать, находится вверху.</span><span class="sxs-lookup"><span data-stu-id="c096c-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-254">Время окончания</span><span class="sxs-lookup"><span data-stu-id="c096c-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-255">Первый завершенный запрос находится вверху.</span><span class="sxs-lookup"><span data-stu-id="c096c-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-256">Общая длительность</span><span class="sxs-lookup"><span data-stu-id="c096c-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-257">Запрос с самыми короткими настройками подключения и запросом или ответом находится вверху.</span><span class="sxs-lookup"><span data-stu-id="c096c-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-258">Задержка</span><span class="sxs-lookup"><span data-stu-id="c096c-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-259">The request that waited the shortest time for a response is at the top.</span><span class="sxs-lookup"><span data-stu-id="c096c-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="c096c-260">В этих описаниях предполагается, что каждый соответствующий параметр ранж находится в ранге от самого короткого к самому длинному.</span><span class="sxs-lookup"><span data-stu-id="c096c-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="c096c-261">Выберите заголок столбца **"Каскад",** чтобы изменить порядок.</span><span class="sxs-lookup"><span data-stu-id="c096c-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскада по общей продолжительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="c096c-263">Сортировка каскада по общей продолжительности \(Светлая часть каждой панели — это время ожидания, а более темная часть — время, затраченное на скачивание bytes\)</span><span class="sxs-lookup"><span data-stu-id="c096c-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="c096c-264">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-264">Analyze requests</span></span>  

<span data-ttu-id="c096c-265">Если devTools открыт, все запросы занося в журнал на панели **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="c096c-265">So long as DevTools are open, it logs all requests in the **Network** panel.</span></span>  
<span data-ttu-id="c096c-266">Используйте панель "Сеть" для анализа запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="c096c-267">Отображение журнала запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-267">Display a log of requests</span></span>  

<span data-ttu-id="c096c-268">Используйте таблицу "Запросы", чтобы отобразить журнал всех запросов, сделанных во время открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="c096c-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="c096c-269">Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите курсор на запросы.</span><span class="sxs-lookup"><span data-stu-id="c096c-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица Requests" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="c096c-271">Таблица Requests</span><span class="sxs-lookup"><span data-stu-id="c096c-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-272">В таблице "Запросы" по умолчанию отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="c096c-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-273">Имя</span><span class="sxs-lookup"><span data-stu-id="c096c-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-274">Имя файла ресурса или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c096c-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-275">Состояние</span><span class="sxs-lookup"><span data-stu-id="c096c-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-276">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="c096c-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-277">Тип</span><span class="sxs-lookup"><span data-stu-id="c096c-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-278">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c096c-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-279">Инициатор</span><span class="sxs-lookup"><span data-stu-id="c096c-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-280">Следующие объекты или процессы инициируют запросы.</span><span class="sxs-lookup"><span data-stu-id="c096c-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="c096c-281">**Parser**  HtmL-разберегатель для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c096c-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="c096c-282">**Перенаправление**  Перенаправление HTTP.</span><span class="sxs-lookup"><span data-stu-id="c096c-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="c096c-283">**Script**  Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c096c-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="c096c-284">**Other**  Другой процесс или действие, например переход на страницу по ссылке или ввод URL-адреса в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="c096c-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-285">Size</span><span class="sxs-lookup"><span data-stu-id="c096c-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-286">Объединенный размер заголовок ответа и тело ответа, доставленные сервером.</span><span class="sxs-lookup"><span data-stu-id="c096c-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-287">Время</span><span class="sxs-lookup"><span data-stu-id="c096c-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-288">Общая продолжительность от начала запроса до получения последнего byte в ответе.</span><span class="sxs-lookup"><span data-stu-id="c096c-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c096c-289">Каскад</span><span class="sxs-lookup"><span data-stu-id="c096c-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-290">Визуальная разбивка действия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="c096c-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="c096c-291">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="c096c-291">Add or remove columns</span></span>  

<span data-ttu-id="c096c-292">Наведите курсор на загон таблицы "Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите параметр, чтобы скрыть или показать его.</span><span class="sxs-lookup"><span data-stu-id="c096c-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="c096c-293">В настоящее время отображаются параметры с контрольными знаками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="c096c-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу "Запросы"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="c096c-295">Добавление столбца в таблицу "Запросы"</span><span class="sxs-lookup"><span data-stu-id="c096c-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="c096c-296">Добавление настраиваемой столбцов</span><span class="sxs-lookup"><span data-stu-id="c096c-296">Add custom columns</span></span>  

<span data-ttu-id="c096c-297">Чтобы добавить настраиваемый столбец в таблицу "Запросы", наведите курсор на загон таблицы \*\*\*\*"Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Заглавные столбцы".  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемного столбца в таблицу "Запросы"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="c096c-299">Добавление настраиваемного столбца в таблицу "Запросы"</span><span class="sxs-lookup"><span data-stu-id="c096c-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-300">Отображение связи синхронизации запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="c096c-301">Используйте каскадный показ для отображения связей синхронизации запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="c096c-302">Организация Каскада по умолчанию использует время начала запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="c096c-303">Таким образом, запросы, которые находятся дальше слева, запущены раньше, чем запросы, которые находятся дальше справа.</span><span class="sxs-lookup"><span data-stu-id="c096c-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="c096c-304">Чтобы просмотреть различные способы сортировки каскада, перейдите к этапу [сортировки по активности.](#sort-by-activity-phase)</span><span class="sxs-lookup"><span data-stu-id="c096c-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Каскад" в области "Запросы"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="c096c-306">Столбец "Каскад" в **области "Запросы"**</span><span class="sxs-lookup"><span data-stu-id="c096c-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
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

### <span data-ttu-id="c096c-307">Отображение предварительного просмотра тела ответа</span><span class="sxs-lookup"><span data-stu-id="c096c-307">Display a preview of a response body</span></span>  

<span data-ttu-id="c096c-308">Чтобы отобразить предварительный просмотр тела ответа, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-309">Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="c096c-310">Выберите вкладку **"Предварительный** просмотр".</span><span class="sxs-lookup"><span data-stu-id="c096c-310">Choose the **Preview** tab.</span></span>  

<span data-ttu-id="c096c-311">Вкладка "Предварительный просмотр" в основном полезна для отображения изображений.</span><span class="sxs-lookup"><span data-stu-id="c096c-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка "Предварительный просмотр"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="c096c-313">Вкладка **"Предварительный** просмотр"</span><span class="sxs-lookup"><span data-stu-id="c096c-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-314">Отображение тела ответа</span><span class="sxs-lookup"><span data-stu-id="c096c-314">Display a response body</span></span>  

<span data-ttu-id="c096c-315">Чтобы отобразить тело ответа на запрос, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-316">Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="c096c-317">Выберите **вкладку "Ответ".**</span><span class="sxs-lookup"><span data-stu-id="c096c-317">Choose the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка "Ответ"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="c096c-319">Вкладка **"Ответ"**</span><span class="sxs-lookup"><span data-stu-id="c096c-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-320">Отображение http-headers</span><span class="sxs-lookup"><span data-stu-id="c096c-320">Display HTTP headers</span></span>  

<span data-ttu-id="c096c-321">Чтобы отобразить данные http-загона о запросе, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-322">Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="c096c-323">Выберите **вкладку "Headers".**</span><span class="sxs-lookup"><span data-stu-id="c096c-323">Choose the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка "Заглавные"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="c096c-325">Вкладка **"Заглавные"**</span><span class="sxs-lookup"><span data-stu-id="c096c-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="c096c-326">Отображение источника http-загона</span><span class="sxs-lookup"><span data-stu-id="c096c-326">Display HTTP header source</span></span>  

<span data-ttu-id="c096c-327">По умолчанию на вкладке "Headers" имена заглавных букв показаны в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="c096c-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="c096c-328">Чтобы dsiplay имена http-загона в порядке получения, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c096c-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-329">Откройте **вкладку "Заглавные"** для интересующих вас запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="c096c-330">Для получения дополнительных сведений перейдите к [отображаемой http-загона.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="c096c-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="c096c-331">Choose **view source**, next to the Request **Header** or **Response Header** section.</span><span class="sxs-lookup"><span data-stu-id="c096c-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="c096c-332">Отображение параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-332">Display query string parameters</span></span>  

<span data-ttu-id="c096c-333">Чтобы отобразить параметры строки запроса URL-адреса в понятном для человека формате, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-334">Откройте **вкладку "Заглавные"** для интересующих вас запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="c096c-335">Для получения дополнительных сведений перейдите к [отображаемой http-загона.](#display-http-headers)</span><span class="sxs-lookup"><span data-stu-id="c096c-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="c096c-336">Перейдите в **раздел "Параметры строки запроса".**</span><span class="sxs-lookup"><span data-stu-id="c096c-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел "Параметры строки запроса"" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="c096c-338">Раздел **"Параметры строки запроса"**</span><span class="sxs-lookup"><span data-stu-id="c096c-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="c096c-339">Отображение источника параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-339">Display query string parameters source</span></span>  

<span data-ttu-id="c096c-340">Чтобы отобразить источник параметра строки запроса, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-341">Перейдите в раздел "Параметры строки запроса".</span><span class="sxs-lookup"><span data-stu-id="c096c-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="c096c-342">Для получения дополнительных сведений перейдите к [параметрам строки запроса.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="c096c-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="c096c-343">Выберите **источник представления.**</span><span class="sxs-lookup"><span data-stu-id="c096c-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="c096c-344">Отображение параметров строки запроса в кодированном URL-адресе</span><span class="sxs-lookup"><span data-stu-id="c096c-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="c096c-345">Чтобы отобразить параметры строки запроса в понятном для человека формате, но с сохраненными кодами, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-346">Перейдите в раздел "Параметры строки запроса".</span><span class="sxs-lookup"><span data-stu-id="c096c-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="c096c-347">Для получения дополнительных сведений перейдите к [параметрам строки запроса.](#display-query-string-parameters)</span><span class="sxs-lookup"><span data-stu-id="c096c-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="c096c-348">Выберите **url-адрес представления в кодированном формате.**</span><span class="sxs-lookup"><span data-stu-id="c096c-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="c096c-349">Отображение файлов cookie</span><span class="sxs-lookup"><span data-stu-id="c096c-349">Display cookies</span></span>  

<span data-ttu-id="c096c-350">Чтобы отобразить файлы cookie, отправленные в http-заголке запроса, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-351">Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="c096c-352">Выберите **вкладку "Файлы cookie".**</span><span class="sxs-lookup"><span data-stu-id="c096c-352">Choose the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка "Файлы cookie"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="c096c-354">Вкладка "Файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="c096c-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-355">Отображение разбивки по времени запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="c096c-356">Чтобы отобразить разбивку по времени запроса, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c096c-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="c096c-357">Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="c096c-358">Выберите вкладку **"Время".**</span><span class="sxs-lookup"><span data-stu-id="c096c-358">Choose the **Timing** tab.</span></span>  

<span data-ttu-id="c096c-359">Чтобы быстрее получить доступ к данным, перейдите к [предварительному просмотру разбивки по времени.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="c096c-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="c096c-360">Дополнительные сведения о каждом из этапов, которые могут отображаться на вкладке "Синхронизация", можно найти в разных этапах разбивки по [времени.](#timing-breakdown-phases-explained) \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка "Время"" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="c096c-362">Вкладка **"Время"**</span><span class="sxs-lookup"><span data-stu-id="c096c-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-363">Дополнительные сведения о каждом из этапов.</span><span class="sxs-lookup"><span data-stu-id="c096c-363">More information about each of the phases.</span></span>  

<span data-ttu-id="c096c-364">Для получения дополнительных сведений о доступе к дисплею перейдите к [разбивке по времени отображения.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="c096c-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="c096c-365">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="c096c-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="c096c-366">Чтобы отобразить предварительный просмотр разбивки по времени запроса, в столбце **"Каскад"** таблицы "Запросы" наведите курсор на запись запроса.</span><span class="sxs-lookup"><span data-stu-id="c096c-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="c096c-367">Дополнительные сведения о том, как получить доступ к данным без наведении курсоров, перейдите к отобралке разбивки по времени [запроса.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="c096c-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбивки по времени запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="c096c-369">Просмотр разбивки по времени запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="c096c-370">Этапы разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="c096c-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="c096c-371">Дополнительные сведения о каждом из этапов, которые могут отображаться на вкладке **"Синхронизация".**</span><span class="sxs-lookup"><span data-stu-id="c096c-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-372">Очередь</span><span class="sxs-lookup"><span data-stu-id="c096c-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-373">Браузер очереди запросов, если любое из следующих true.</span><span class="sxs-lookup"><span data-stu-id="c096c-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="c096c-374">Существуют запросы с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="c096c-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="c096c-375">Для одного источника открыто шесть подключений TCP, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="c096c-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="c096c-376">Применяется только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="c096c-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="c096c-377">Браузер нена короткое время на дисковый кэш.</span><span class="sxs-lookup"><span data-stu-id="c096c-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-378">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="c096c-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-379">Запрос заглох по любой из причин, описанных в **очереди.**</span><span class="sxs-lookup"><span data-stu-id="c096c-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-380">DNS Lookup</span><span class="sxs-lookup"><span data-stu-id="c096c-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-381">Браузер разрешит IP-адрес для запроса.</span><span class="sxs-lookup"><span data-stu-id="c096c-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-382">Начальное подключение</span><span class="sxs-lookup"><span data-stu-id="c096c-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-383">Браузер устанавливает подключение, включая соглашения TCP, повторное создание TCP и согласование уровня безопасного socket.</span><span class="sxs-lookup"><span data-stu-id="c096c-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-384">Согласование прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="c096c-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-385">Браузер согласован с [прокси-сервером.][WikiProxyServer]</span><span class="sxs-lookup"><span data-stu-id="c096c-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-386">Отправленный запрос</span><span class="sxs-lookup"><span data-stu-id="c096c-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-387">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="c096c-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-388">Подготовка ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="c096c-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-389">Браузер запускает рабочий сотрудник службы.</span><span class="sxs-lookup"><span data-stu-id="c096c-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-390">Запрос в ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="c096c-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-391">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="c096c-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-392">Ожидание \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="c096c-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-393">Браузер ожидает первого byte отклика.</span><span class="sxs-lookup"><span data-stu-id="c096c-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="c096c-394">TTFB означает "Время до первого byte".</span><span class="sxs-lookup"><span data-stu-id="c096c-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="c096c-395">Это время включает в себя один круговой путь задержки и время, необходимое серверу для подготовки ответа.</span><span class="sxs-lookup"><span data-stu-id="c096c-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-396">Загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="c096c-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-397">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="c096c-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-398">Получение push-сигнала</span><span class="sxs-lookup"><span data-stu-id="c096c-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-399">Браузер получает данные для этого ответа с помощью http/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="c096c-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="c096c-400">Чтение push-вех</span><span class="sxs-lookup"><span data-stu-id="c096c-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c096c-401">Браузер читает ранее полученные локальные данные.</span><span class="sxs-lookup"><span data-stu-id="c096c-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="c096c-402">Отображение инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="c096c-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="c096c-403">Чтобы отобразить инициаторов и зависимости запроса, удерживайте и наведите курсор на `Shift` запрос в таблице "Запросы".</span><span class="sxs-lookup"><span data-stu-id="c096c-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="c096c-404">Цвета DevTools: инициаторы показаны зеленым цветом, а зависимости — красным цветом.</span><span class="sxs-lookup"><span data-stu-id="c096c-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="c096c-406">Отображение инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-407">Если таблица Requests упорядочена в хронологическом порядке, при наведении курсором на строку в строке перед ней отображается зеленый запрос.</span><span class="sxs-lookup"><span data-stu-id="c096c-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="c096c-408">Зеленый запрос является инициатором зависимостей.</span><span class="sxs-lookup"><span data-stu-id="c096c-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="c096c-409">Если перед этим в строке отображается другой зеленый запрос, этот запрос выше является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="c096c-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="c096c-410">И так далее.</span><span class="sxs-lookup"><span data-stu-id="c096c-410">And so on.</span></span>  

### <span data-ttu-id="c096c-411">Отображение событий загрузки</span><span class="sxs-lookup"><span data-stu-id="c096c-411">Display load events</span></span>  

<span data-ttu-id="c096c-412">DevTools отображает время событий и событий в нескольких `DOMContentLoaded` `load` местах на панели **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="c096c-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** panel.</span></span>  <span data-ttu-id="c096c-413">Событие `DOMContentLoaded` имеет синий цвет, а событие — `load` красный.</span><span class="sxs-lookup"><span data-stu-id="c096c-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположения doMContentLoaded и события загрузки на панели "Сеть"" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="c096c-415">Расположение событий и `DOMContentLoaded` событий `load` на панели **"Сеть"**</span><span class="sxs-lookup"><span data-stu-id="c096c-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-416">Отображение общего количества запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-416">Display the total number of requests</span></span>  

<span data-ttu-id="c096c-417">Общее количество запросов перечислены в \*\*\*\* области сводки в нижней части **панели "Сеть".**</span><span class="sxs-lookup"><span data-stu-id="c096c-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c096c-418">Это число отслеживает только запросы, зарегистрированные с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="c096c-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="c096c-419">Если другие запросы произошли до открытия DevTools, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="c096c-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="c096c-421">Общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="c096c-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-422">Отображение общего размера скачивания</span><span class="sxs-lookup"><span data-stu-id="c096c-422">Display the total download size</span></span>  

<span data-ttu-id="c096c-423">Общий размер скачиваемых запросов указан \*\*\*\* в области "Сводка" в нижней части **панели "Сеть".**</span><span class="sxs-lookup"><span data-stu-id="c096c-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c096c-424">Это число отслеживает только запросы, зарегистрированные с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="c096c-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="c096c-425">Если другие запросы произошли до открытия DevTools, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="c096c-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий размер скачиваемых запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="c096c-427">Общий размер скачиваемых запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-428">Чтобы проверить размер ресурсов после того, как браузер отпечатает каждый элемент, перейдите, чтобы отобразить несжамый [размер ресурса.](#display-the-uncompressed-size-of-a-resource)</span><span class="sxs-lookup"><span data-stu-id="c096c-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="c096c-429">Отображение трассировки стека, вызвавного запрос</span><span class="sxs-lookup"><span data-stu-id="c096c-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="c096c-430">После запроса ресурса в javaScript наведите курсор на столбец "Инициатор", чтобы отобразить трассировку стека перед запросом. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c096c-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека до запроса ресурса" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="c096c-432">Трассировка стека до запроса ресурса</span><span class="sxs-lookup"><span data-stu-id="c096c-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-433">Отображение несжамого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="c096c-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="c096c-434">Включив **контрольный ящик "Использовать** большие строки запросов", а затем просмотрите нижнее значение **столбца Size.**</span><span class="sxs-lookup"><span data-stu-id="c096c-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несмеченных ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="c096c-436">Пример несжатых ресурсов \(Сжатый размер файла, отправленного по сети, был , тогда как несжатый размер `jquery-3.3.1.min.js` `29.9 KB` был `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="c096c-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="c096c-437">Экспорт данных запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-437">Export requests data</span></span>  

### <span data-ttu-id="c096c-438">Сохранение всех сетевых запросов в файл HAR</span><span class="sxs-lookup"><span data-stu-id="c096c-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="c096c-439">Чтобы сохранить все сетевые запросы в файл HAR, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c096c-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="c096c-440">Наведите курсор на любой запрос в таблице "Запросы" и откройте контекстное меню \(щелкните правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="c096c-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c096c-441">Choose **Save as HAR with Content**.</span><span class="sxs-lookup"><span data-stu-id="c096c-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="c096c-442">DevTools сохраняет все запросы, которые произошли с момента открытия DevTools, в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="c096c-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="c096c-443">Фильтровать запросы нельзя.</span><span class="sxs-lookup"><span data-stu-id="c096c-443">You are not able to filter requests.</span></span>  <span data-ttu-id="c096c-444">Вы также не можете сохранить один запрос.</span><span class="sxs-lookup"><span data-stu-id="c096c-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="c096c-445">После сохранения файла HAR вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="c096c-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="c096c-446">Просто перетащите файл HAR в таблицу Requests.</span><span class="sxs-lookup"><span data-stu-id="c096c-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Choose Save as HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="c096c-448">Choose **Save as HAR with Content**</span><span class="sxs-lookup"><span data-stu-id="c096c-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-449">Копирование одного или более запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="c096c-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="c096c-450">В **столбце "Имя"** таблицы "Запросы" наведите курсор на запрос, откройте \*\*\*\* контекстное меню \(щелкните правой кнопкой мыши),наведите курсор на "Копировать" и выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="c096c-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="c096c-451">Название</span><span class="sxs-lookup"><span data-stu-id="c096c-451">Name</span></span> | <span data-ttu-id="c096c-452">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="c096c-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="c096c-453">Копировать адрес ссылки</span><span class="sxs-lookup"><span data-stu-id="c096c-453">Copy Link Address</span></span>** | <span data-ttu-id="c096c-454">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="c096c-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="c096c-455">Копирование ответа</span><span class="sxs-lookup"><span data-stu-id="c096c-455">Copy Response</span></span>** | <span data-ttu-id="c096c-456">Скопируйте текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="c096c-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="c096c-457">Копирование как fetch</span><span class="sxs-lookup"><span data-stu-id="c096c-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="c096c-458">Копировать как cURL</span><span class="sxs-lookup"><span data-stu-id="c096c-458">Copy as cURL</span></span>** | <span data-ttu-id="c096c-459">Скопируйте запрос в виде команды cURL.</span><span class="sxs-lookup"><span data-stu-id="c096c-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="c096c-460">Копировать все как получить</span><span class="sxs-lookup"><span data-stu-id="c096c-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="c096c-461">Копировать все как cURL</span><span class="sxs-lookup"><span data-stu-id="c096c-461">Copy All as cURL</span></span>** | <span data-ttu-id="c096c-462">Скопируйте все запросы в виде цепочки команд cURL.</span><span class="sxs-lookup"><span data-stu-id="c096c-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="c096c-463">Копировать все как HAR</span><span class="sxs-lookup"><span data-stu-id="c096c-463">Copy All as HAR</span></span>** | <span data-ttu-id="c096c-464">Скопируйте все запросы в качестве данных HAR.</span><span class="sxs-lookup"><span data-stu-id="c096c-464">Copy all requests as HAR data.</span></span> |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор ответа "Копировать"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="c096c-466">Выбор **ответа "Копировать"**</span><span class="sxs-lookup"><span data-stu-id="c096c-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-467">Копирование форматированный ответ JSON в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="c096c-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="c096c-468">Выберите сетевой запрос и перейдите в области **"Headers".**</span><span class="sxs-lookup"><span data-stu-id="c096c-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="c096c-469">Чтобы скопировать значение JSON ответа, \*\*\*\* перейдите к запросу полезной нагрузки, наведите курсор на содержимое ответа JSON, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Копировать **значение".**</span><span class="sxs-lookup"><span data-stu-id="c096c-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Копировать значение в контекстное меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="c096c-471">**Копировать значение** в контекстное меню</span><span class="sxs-lookup"><span data-stu-id="c096c-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Visual Studio код с форматированный ответ JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="c096c-473">Pasting formatted response JSON in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c096c-473">Pasting formatted response JSON in Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="c096c-474">Копирование значений свойств из сетевых запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="c096c-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="c096c-475">Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c096c-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="c096c-476">Откройте области **"Headers".**</span><span class="sxs-lookup"><span data-stu-id="c096c-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="c096c-477">Откройте один из следующих разделов.</span><span class="sxs-lookup"><span data-stu-id="c096c-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="c096c-478">Запрос полезной нагрузки \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="c096c-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="c096c-479">Данные формы</span><span class="sxs-lookup"><span data-stu-id="c096c-479">Form Data</span></span>  
    *   <span data-ttu-id="c096c-480">Параметры строки запроса</span><span class="sxs-lookup"><span data-stu-id="c096c-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="c096c-481">Заглавные запросы</span><span class="sxs-lookup"><span data-stu-id="c096c-481">Request Headers</span></span>  
    *   <span data-ttu-id="c096c-482">Заглавные</span><span class="sxs-lookup"><span data-stu-id="c096c-482">Response Headers</span></span>  
1.  <span data-ttu-id="c096c-483">Откройте контекстное меню \(щелкните правой кнопкой мыши\) > **значение копирования.**</span><span class="sxs-lookup"><span data-stu-id="c096c-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="c096c-484">Теперь вы можете в paste the value into any editor to review it.</span><span class="sxs-lookup"><span data-stu-id="c096c-484">You can now paste the value into any editor to review it.</span></span>  
    
## <span data-ttu-id="c096c-485">Изменение макета панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="c096c-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="c096c-486">Вы можете развернуть или свернуть разделы пользовательского **интерфейса** панели "Сеть", чтобы получить важные сведения.</span><span class="sxs-lookup"><span data-stu-id="c096c-486">You may expand or collapse sections of the **Network** panel UI to focus important information.</span></span>  

### <span data-ttu-id="c096c-487">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="c096c-487">Hide the Filters pane</span></span>  

<span data-ttu-id="c096c-488">По умолчанию DevTools показывает области **фильтров.**</span><span class="sxs-lookup"><span data-stu-id="c096c-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="c096c-489">Выберите **filter** \( ![ Filter ][ImageFilterIcon] \), чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="c096c-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "Скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="c096c-491">Кнопка "Скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="c096c-491">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-492">Использование больших строк запросов</span><span class="sxs-lookup"><span data-stu-id="c096c-492">Use large request rows</span></span>  

<span data-ttu-id="c096c-493">Используйте большие строки, если вам нужно большее пространство в таблице сетевых запросов.</span><span class="sxs-lookup"><span data-stu-id="c096c-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="c096c-494">Некоторые столбцы также предоставляют дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="c096c-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="c096c-495">Например, нижним значением столбца **Size** является несмещается размер запроса.</span><span class="sxs-lookup"><span data-stu-id="c096c-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример больших строк запросов в области "Запросы"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="c096c-497">Пример больших строк запросов в \*\*\*\* области "Запросы"</span><span class="sxs-lookup"><span data-stu-id="c096c-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="c096c-498">Чтобы включить большие строки, включите контрольный ящик **"Использовать большие строки запросов".**</span><span class="sxs-lookup"><span data-stu-id="c096c-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="The Use large request rows checkbox" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="c096c-500">The **Use large request rows** checkbox</span><span class="sxs-lookup"><span data-stu-id="c096c-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="c096c-501">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="c096c-501">Hide the Overview pane</span></span>  

<span data-ttu-id="c096c-502">По умолчанию DevTools отображает области **обзора.**</span><span class="sxs-lookup"><span data-stu-id="c096c-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="c096c-503">Чтобы скрыть его, отключите **контрольный ящик "Показать обзор".**</span><span class="sxs-lookup"><span data-stu-id="c096c-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="The Show Overview checkbox" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="c096c-505">The **Show Overview** checkbox</span><span class="sxs-lookup"><span data-stu-id="c096c-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="c096c-506">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c096c-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Debug Progressive Web Apps | Документы Майкрософт"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедия"  

> [!NOTE]
> <span data-ttu-id="c096c-510">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c096c-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c096c-511">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/network/reference) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c096c-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c096c-513">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c096c-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
