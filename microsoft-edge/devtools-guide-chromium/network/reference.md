---
description: Полный справочник по функциям панели DevTools сети Microsoft Edge.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4d4dc8ad5102766f3ad3c8322dbf9342a69e9097
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203908"
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

# <span data-ttu-id="19387-104">Справочник по анализу сети</span><span class="sxs-lookup"><span data-stu-id="19387-104">Network Analysis reference</span></span>  

<span data-ttu-id="19387-105">Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="19387-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <span data-ttu-id="19387-106">Запись сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="19387-106">Record network requests</span></span>  

<span data-ttu-id="19387-107">По умолчанию DevTools запись всех сетевых запросов на панели " **сеть** ", пока открыта DevTools.</span><span class="sxs-lookup"><span data-stu-id="19387-107">By default, DevTools record all network requests in the **Network** panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель "сеть"" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="19387-109">Панель " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="19387-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-110">Прекращение записи сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="19387-110">Stop recording network requests</span></span>  

<span data-ttu-id="19387-111">Чтобы остановить запись запросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="19387-112">На панели **Network (сеть** ) выберите команду **остановить запись журнала сети** \ ( ![ остановить запись сетевого журнала ][ImageRecordOnIcon] \).</span><span class="sxs-lookup"><span data-stu-id="19387-112">On the **Network** panel, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="19387-113">Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.</span><span class="sxs-lookup"><span data-stu-id="19387-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="19387-114">Нажмите кнопку `Control` + `E` \ (Windows, Linux \) или `Command` + `E` \ (macOS \), когда фокус находится на панели **Network (сеть** ).</span><span class="sxs-lookup"><span data-stu-id="19387-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="19387-115">Очистка запросов</span><span class="sxs-lookup"><span data-stu-id="19387-115">Clear requests</span></span>  

<span data-ttu-id="19387-116">На панели Network (сеть) выберите **clear** \ ( ![ очистить ][ImageClearIcon] \), чтобы удалить все запросы из таблицы запросы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="19387-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка "очистить"" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="19387-118">Кнопка " **очистить** "</span><span class="sxs-lookup"><span data-stu-id="19387-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-119">Сохранение запросов на загрузку страниц</span><span class="sxs-lookup"><span data-stu-id="19387-119">Save requests across page loads</span></span>  

<span data-ttu-id="19387-120">Чтобы сохранить запросы при загрузке страниц, включите флажок **сохранить журнал** на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="19387-120">To save requests across page loads, on the **Network** panel, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="19387-121">DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.</span><span class="sxs-lookup"><span data-stu-id="19387-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Флажок "сохранить журнал"" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="19387-123">Флажок " **сохранить журнал** "</span><span class="sxs-lookup"><span data-stu-id="19387-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-124">Захват снимков экрана при загрузке страницы</span><span class="sxs-lookup"><span data-stu-id="19387-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="19387-125">Выведите снимки экрана, чтобы проанализировать, какие дисплеи отображаются для пользователей во время ожидания загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="19387-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="19387-126">Чтобы включить снимки экрана, выберите **Параметры сети**и на панели **сеть** включите флажок **захватить снимки экрана** .</span><span class="sxs-lookup"><span data-stu-id="19387-126">To enable screenshots, choose **Network settings**, and on the **Network** panel, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="19387-127">Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="19387-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="19387-128">После захвата снимка экрана вы взаимодействуете с ним следующими способами.</span><span class="sxs-lookup"><span data-stu-id="19387-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="19387-129">Наведите указатель мыши на снимок экрана, чтобы отобразить точку, в которой был записан снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="19387-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="19387-130">На панели **обзора** появится желтая линия.</span><span class="sxs-lookup"><span data-stu-id="19387-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="19387-131">Выберите эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="19387-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="19387-132">Дважды щелкните эскиз, чтобы увеличить его.</span><span class="sxs-lookup"><span data-stu-id="19387-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведение указателя мыши на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="19387-134">Наведение указателя мыши на снимок экрана</span><span class="sxs-lookup"><span data-stu-id="19387-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="19387-135">Изменение поведения при загрузке</span><span class="sxs-lookup"><span data-stu-id="19387-135">Change loading behavior</span></span>  

### <span data-ttu-id="19387-136">Эмуляция первого времени посетителя с помощью отключения кэша браузера</span><span class="sxs-lookup"><span data-stu-id="19387-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="19387-137">Чтобы эмулировать, как пользователь попытается использовать ваш сайт в первый раз, включите флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="19387-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="19387-138">DevTools отключает кэш браузера.</span><span class="sxs-lookup"><span data-stu-id="19387-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="19387-139">Эта функция более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.</span><span class="sxs-lookup"><span data-stu-id="19387-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Флажок "отключить кэш"" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="19387-141">Флажок " **отключить кэш** "</span><span class="sxs-lookup"><span data-stu-id="19387-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="19387-142">Отключение кэша браузера из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="19387-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="19387-143">Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.</span><span class="sxs-lookup"><span data-stu-id="19387-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="19387-144">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="19387-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="19387-145">Включите \ (или выключите) флажок **отключить кэш** .</span><span class="sxs-lookup"><span data-stu-id="19387-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="19387-146">Очистка кэша браузера вручную</span><span class="sxs-lookup"><span data-stu-id="19387-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="19387-147">Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите команду **очистить кэш браузера**).</span><span class="sxs-lookup"><span data-stu-id="19387-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор очистки кэша браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="19387-149">Выбор **очистки кэша браузера**</span><span class="sxs-lookup"><span data-stu-id="19387-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-150">Эмуляция в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="19387-150">Emulate offline</span></span>  

<span data-ttu-id="19387-151">Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.</span><span class="sxs-lookup"><span data-stu-id="19387-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="19387-152">Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.</span><span class="sxs-lookup"><span data-stu-id="19387-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="19387-153">Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе **пресеты**и выберите пункт в **автономном** режиме, чтобы имитировать автономный режим работы сети.</span><span class="sxs-lookup"><span data-stu-id="19387-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Раскрывающееся меню "автономный режим"" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="19387-155">Раскрывающееся меню " **автономный режим** "</span><span class="sxs-lookup"><span data-stu-id="19387-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-156">Эмуляция медленных сетевых подключений</span><span class="sxs-lookup"><span data-stu-id="19387-156">Emulate slow network connections</span></span>  

<span data-ttu-id="19387-157">Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .</span><span class="sxs-lookup"><span data-stu-id="19387-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Раскрывающееся меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="19387-159">Раскрывающееся меню **регулирования**</span><span class="sxs-lookup"><span data-stu-id="19387-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="19387-160">Вы можете выбрать один из различных наборов параметров, например "медленный" или "Быстрая 3G".</span><span class="sxs-lookup"><span data-stu-id="19387-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="19387-161">Чтобы добавить собственные пользовательские стили, откройте меню регулирования и выберите пункт **настраиваемое**  >  **Добавление**.</span><span class="sxs-lookup"><span data-stu-id="19387-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="19387-162">DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.</span><span class="sxs-lookup"><span data-stu-id="19387-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="19387-163">Эмуляция медленных сетевых подключений из денежных ящиков условий сети</span><span class="sxs-lookup"><span data-stu-id="19387-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="19387-164">Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.</span><span class="sxs-lookup"><span data-stu-id="19387-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="19387-165">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="19387-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="19387-166">Выберите скорость соединения в меню **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="19387-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="19387-167">Очистка файлов cookie браузера вручную</span><span class="sxs-lookup"><span data-stu-id="19387-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="19387-168">Чтобы вручную очистить cookie-файлы браузера в любое время, наведите указатель мыши на любое место в таблице запросов, откройте контекстное меню, а затем выберите команду **Удалить cookie-файлы браузера**.</span><span class="sxs-lookup"><span data-stu-id="19387-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выберите команду "очистить" cookie-браузеры." lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="19387-170">Выберите команду **"очистить" cookie-браузеры** .</span><span class="sxs-lookup"><span data-stu-id="19387-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-171">Переопределение агента пользователя</span><span class="sxs-lookup"><span data-stu-id="19387-171">Override the user agent</span></span>  

<span data-ttu-id="19387-172">Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-173">Откройте денежный ящик **условий сети** .</span><span class="sxs-lookup"><span data-stu-id="19387-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="19387-174">Отключите флажок **выбрать автоматически** .</span><span class="sxs-lookup"><span data-stu-id="19387-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="19387-175">Выберите в меню пункт агента пользователя или введите его в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="19387-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="19387-176">Фильтрация запросов</span><span class="sxs-lookup"><span data-stu-id="19387-176">Filter requests</span></span>  

### <span data-ttu-id="19387-177">Фильтрация запросов по свойствам</span><span class="sxs-lookup"><span data-stu-id="19387-177">Filter requests by properties</span></span>  

<span data-ttu-id="19387-178">С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="19387-179">Если текстовое поле не отображается, возможно, область **фильтры** скрыта.</span><span class="sxs-lookup"><span data-stu-id="19387-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="19387-180">Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="19387-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле "фильтр"" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="19387-182">Текстовое поле " **Фильтр** "</span><span class="sxs-lookup"><span data-stu-id="19387-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="19387-183">Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.</span><span class="sxs-lookup"><span data-stu-id="19387-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="19387-184">Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.</span><span class="sxs-lookup"><span data-stu-id="19387-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="19387-185">Фильтры с несколькими свойствами эквивалентны `AND` операциям.</span><span class="sxs-lookup"><span data-stu-id="19387-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="19387-186">операции в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="19387-186">operations are currently not supported.</span></span>  

<span data-ttu-id="19387-187">Полный список поддерживаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="19387-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="19387-188">Свойство</span><span class="sxs-lookup"><span data-stu-id="19387-188">Property</span></span> | <span data-ttu-id="19387-189">Сведения</span><span class="sxs-lookup"><span data-stu-id="19387-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="19387-190">Отображать только ресурсы из указанного домена.</span><span class="sxs-lookup"><span data-stu-id="19387-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="19387-191">Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.</span><span class="sxs-lookup"><span data-stu-id="19387-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="19387-192">Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .</span><span class="sxs-lookup"><span data-stu-id="19387-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="19387-193">DevTools Заполнение раскрывающегося меню "Автозаполнение" всеми найденными доменами.</span><span class="sxs-lookup"><span data-stu-id="19387-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="19387-194">Выводит ресурсы, содержащие указанный заголовок HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19387-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="19387-195">DevTools заполнить раскрывающийся список автозавершения всеми найденными заголовками ответов.</span><span class="sxs-lookup"><span data-stu-id="19387-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="19387-196">Используется `is:running` для поиска `WebSocket` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19387-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="19387-197">Отображаются ресурсы, размер которых превышает указанный в байтах.</span><span class="sxs-lookup"><span data-stu-id="19387-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="19387-198">Установка значения эквивалентно значению свойства `1000` `1k` .</span><span class="sxs-lookup"><span data-stu-id="19387-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="19387-199">Отображает ресурсы, полученные с помощью указанного типа метода HTTP.</span><span class="sxs-lookup"><span data-stu-id="19387-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="19387-200">DevTools заполнить раскрывающийся список всеми найденными методами HTTP.</span><span class="sxs-lookup"><span data-stu-id="19387-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="19387-201">Выводит ресурсы указанного типа MIME.</span><span class="sxs-lookup"><span data-stu-id="19387-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="19387-202">DevTools заполнить раскрывающийся список всеми найденными типами MIME.</span><span class="sxs-lookup"><span data-stu-id="19387-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="19387-203">Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="19387-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="19387-204">Отображаются ресурсы, полученные по незащищенным HTTP-( `scheme:http` \) или защищенным HTTPS-( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="19387-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="19387-205">Отображает ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="19387-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="19387-206">DevTools заполнить Автозаполнение всеми найденными доменами cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="19387-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="19387-207">Отображаются ресурсы, у которых есть `Set-Cookie` заголовок с именем, соответствующим указанному значению.</span><span class="sxs-lookup"><span data-stu-id="19387-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="19387-208">DevTools заполните Автозаполнение всеми найденными именами cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="19387-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="19387-209">Отображает ресурсы с `Set-Cookie` заголовком со значением, которое соответствует указанному значению.</span><span class="sxs-lookup"><span data-stu-id="19387-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="19387-210">DevTools заполнить Автозаполнение всеми найденными значениями cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="19387-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="19387-211">Отображает ресурсы, соответствующие указанному коду состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="19387-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="19387-212">DevTools заполняет раскрывающееся меню автозаполнения всеми найденными кодами состояния.</span><span class="sxs-lookup"><span data-stu-id="19387-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="19387-213">Фильтрация запросов по типу</span><span class="sxs-lookup"><span data-stu-id="19387-213">Filter requests by type</span></span>  

<span data-ttu-id="19387-214">Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок на панели **сеть** .</span><span class="sxs-lookup"><span data-stu-id="19387-214">To filter requests by request type, choose the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-215">XHR</span><span class="sxs-lookup"><span data-stu-id="19387-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-216">JS</span><span class="sxs-lookup"><span data-stu-id="19387-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-217">CSS</span><span class="sxs-lookup"><span data-stu-id="19387-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-218">IMG</span><span class="sxs-lookup"><span data-stu-id="19387-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-219">Media</span><span class="sxs-lookup"><span data-stu-id="19387-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-220">Шрифт</span><span class="sxs-lookup"><span data-stu-id="19387-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-221">Тов</span><span class="sxs-lookup"><span data-stu-id="19387-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-222">WS</span><span class="sxs-lookup"><span data-stu-id="19387-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="19387-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-224">Является</span><span class="sxs-lookup"><span data-stu-id="19387-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-225">Other</span><span class="sxs-lookup"><span data-stu-id="19387-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-226">Любые другие типы не указаны в списке.</span><span class="sxs-lookup"><span data-stu-id="19387-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="19387-227">Если кнопки не отображаются, область **фильтров** может быть скрыта.</span><span class="sxs-lookup"><span data-stu-id="19387-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="19387-228">Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="19387-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="19387-229">Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите.</span><span class="sxs-lookup"><span data-stu-id="19387-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров типов для отображения ресурсов JS, CSS и документов" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="19387-231">Использование фильтров типов для отображения ресурсов JS, CSS и документов</span><span class="sxs-lookup"><span data-stu-id="19387-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-232">Фильтрация запросов по времени</span><span class="sxs-lookup"><span data-stu-id="19387-232">Filter requests by time</span></span>  

<span data-ttu-id="19387-233">Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите в области " **Обзор** " и перетащите ее влево или вправо.</span><span class="sxs-lookup"><span data-stu-id="19387-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="19387-234">Фильтр является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="19387-234">The filter is inclusive.</span></span>  <span data-ttu-id="19387-235">Отображается любой запрос, который был активен в течение выбранного периода времени.</span><span class="sxs-lookup"><span data-stu-id="19387-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация запросов, которые были неактивны около 300 MS" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="19387-237">Фильтрация запросов, которые были неактивны около 300 MS</span><span class="sxs-lookup"><span data-stu-id="19387-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-238">Скрыть URL-адреса данных</span><span class="sxs-lookup"><span data-stu-id="19387-238">Hide data URLs</span></span>  

<span data-ttu-id="19387-239">[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.</span><span class="sxs-lookup"><span data-stu-id="19387-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="19387-240">Любые запросы, которые отображаются в таблице запросов, которая начинается с `data:` URL-адреса данных.</span><span class="sxs-lookup"><span data-stu-id="19387-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="19387-241">Чтобы скрыть запросы, снимите флажок **скрыть URL-адреса данных** .</span><span class="sxs-lookup"><span data-stu-id="19387-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Флажок "скрыть URL-адреса данных"" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="19387-243">Флажок " **скрыть URL-адреса данных** "</span><span class="sxs-lookup"><span data-stu-id="19387-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="19387-244">Запросы сортировки</span><span class="sxs-lookup"><span data-stu-id="19387-244">Sort requests</span></span>  

<span data-ttu-id="19387-245">По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.</span><span class="sxs-lookup"><span data-stu-id="19387-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="19387-246">Сортировка по столбцам</span><span class="sxs-lookup"><span data-stu-id="19387-246">Sort by column</span></span>  

<span data-ttu-id="19387-247">Выберите верхний колонтитул любого столбца в запросах для сортировки запросов по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="19387-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="19387-248">Этап сортировки по действию</span><span class="sxs-lookup"><span data-stu-id="19387-248">Sort by activity phase</span></span>  

<span data-ttu-id="19387-249">Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="19387-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-250">Время начала</span><span class="sxs-lookup"><span data-stu-id="19387-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-251">Первый инициированный запрос находится наверху.</span><span class="sxs-lookup"><span data-stu-id="19387-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-252">Время ответа</span><span class="sxs-lookup"><span data-stu-id="19387-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-253">Первый запрос, загруженный в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="19387-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-254">Время окончания</span><span class="sxs-lookup"><span data-stu-id="19387-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-255">Первый завершенный запрос вверху.</span><span class="sxs-lookup"><span data-stu-id="19387-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-256">Общая длительность</span><span class="sxs-lookup"><span data-stu-id="19387-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-257">В верхней части запроса с минимальными параметрами подключения и запроса или ответа.</span><span class="sxs-lookup"><span data-stu-id="19387-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-258">Задержка</span><span class="sxs-lookup"><span data-stu-id="19387-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-259">Запрос, который ожидает наиболее короткий момент ответа, находится наверху.</span><span class="sxs-lookup"><span data-stu-id="19387-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="19387-260">В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.</span><span class="sxs-lookup"><span data-stu-id="19387-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="19387-261">Выберите верхний колонтитул столбца **каскадом** , чтобы изменить порядок.</span><span class="sxs-lookup"><span data-stu-id="19387-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскадом по общей длительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="19387-263">Сортировка каскадной группировки по общей длительности \ (светлая часть каждой линии — это задолгое время, в которое более темная часть загружает байты)</span><span class="sxs-lookup"><span data-stu-id="19387-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="19387-264">Анализ запросов</span><span class="sxs-lookup"><span data-stu-id="19387-264">Analyze requests</span></span>  

<span data-ttu-id="19387-265">Пока DevTools открыты, все запросы на панели " **сеть** " записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="19387-265">So long as DevTools are open, it logs all requests in the **Network** panel.</span></span>  
<span data-ttu-id="19387-266">Проанализируйте запросы с помощью панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="19387-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="19387-267">Вывод журнала запросов</span><span class="sxs-lookup"><span data-stu-id="19387-267">Display a log of requests</span></span>  

<span data-ttu-id="19387-268">С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыты.</span><span class="sxs-lookup"><span data-stu-id="19387-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="19387-269">Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите указатель мыши на пункт запросы.</span><span class="sxs-lookup"><span data-stu-id="19387-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица запросов" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="19387-271">Таблица запросов</span><span class="sxs-lookup"><span data-stu-id="19387-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="19387-272">По умолчанию в таблице запросов отображаются следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="19387-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-273">Название</span><span class="sxs-lookup"><span data-stu-id="19387-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-274">Имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="19387-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-275">Состояние</span><span class="sxs-lookup"><span data-stu-id="19387-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-276">Код состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="19387-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-277">Тип</span><span class="sxs-lookup"><span data-stu-id="19387-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-278">Тип MIME запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="19387-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-279">Владельцы</span><span class="sxs-lookup"><span data-stu-id="19387-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-280">Следующие объекты или процессы инициируют запросы.</span><span class="sxs-lookup"><span data-stu-id="19387-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="19387-281">**Средство синтаксического анализа**  Средство синтаксического анализа HTML для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="19387-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="19387-282">**Redirect (перенаправление**  )  Переадресация HTTP.</span><span class="sxs-lookup"><span data-stu-id="19387-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="19387-283">**Сценарий**  Функция JavaScript.</span><span class="sxs-lookup"><span data-stu-id="19387-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="19387-284">**Другие**  Некоторые другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="19387-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-285">Size</span><span class="sxs-lookup"><span data-stu-id="19387-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-286">Объединенный размер заголовков ответа и текст ответа, доставленный сервером.</span><span class="sxs-lookup"><span data-stu-id="19387-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-287">Время</span><span class="sxs-lookup"><span data-stu-id="19387-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-288">Общая продолжительность от начала запроса до получения последнего байта в ответе.</span><span class="sxs-lookup"><span data-stu-id="19387-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="19387-289">Каскад</span><span class="sxs-lookup"><span data-stu-id="19387-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-290">Визуальная декомпозиция мероприятия для каждого запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="19387-291">Добавление и удаление столбцов</span><span class="sxs-lookup"><span data-stu-id="19387-291">Add or remove columns</span></span>  

<span data-ttu-id="19387-292">Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.</span><span class="sxs-lookup"><span data-stu-id="19387-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="19387-293">Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.</span><span class="sxs-lookup"><span data-stu-id="19387-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="19387-295">Добавление столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="19387-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="19387-296">Добавление настраиваемых столбцов</span><span class="sxs-lookup"><span data-stu-id="19387-296">Add custom columns</span></span>  

<span data-ttu-id="19387-297">Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**для  >  **управления столбцами заголовков**.</span><span class="sxs-lookup"><span data-stu-id="19387-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемого столбца в таблицу "запросы"" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="19387-299">Добавление настраиваемого столбца в таблицу "запросы"</span><span class="sxs-lookup"><span data-stu-id="19387-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-300">Отображение отношения временных повременных запросов</span><span class="sxs-lookup"><span data-stu-id="19387-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="19387-301">Используйте Каскад, чтобы отобразить отношения времени между запросами.</span><span class="sxs-lookup"><span data-stu-id="19387-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="19387-302">В структуре, используемой по умолчанию для каскадов, используется время начала запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="19387-303">Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.</span><span class="sxs-lookup"><span data-stu-id="19387-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="19387-304">Чтобы просмотреть различные способы сортировки каскадов, перейдите на [фазу "Сортировка по действию](#sort-by-activity-phase)".</span><span class="sxs-lookup"><span data-stu-id="19387-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Каскад" на панели "запросы"" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="19387-306">Столбец "Каскад" на панели " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="19387-306">The Waterfall column of the **Requests** pane</span></span>  
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

### <span data-ttu-id="19387-307">Вывод предварительной версии текста ответа</span><span class="sxs-lookup"><span data-stu-id="19387-307">Display a preview of a response body</span></span>  

<span data-ttu-id="19387-308">Чтобы просмотреть текст ответа, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-309">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="19387-310">Выберите вкладку **Предварительный просмотр** .</span><span class="sxs-lookup"><span data-stu-id="19387-310">Choose the **Preview** tab.</span></span>  

<span data-ttu-id="19387-311">Вкладка Предварительный просмотр в основном полезна для отображения изображений.</span><span class="sxs-lookup"><span data-stu-id="19387-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка "предварительный просмотр"" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="19387-313">Вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="19387-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-314">Отображение текста ответа</span><span class="sxs-lookup"><span data-stu-id="19387-314">Display a response body</span></span>  

<span data-ttu-id="19387-315">Чтобы отобразить текст ответа на запрос, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-316">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="19387-317">Перейдите на вкладку **ответ** .</span><span class="sxs-lookup"><span data-stu-id="19387-317">Choose the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка "ответ"" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="19387-319">Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="19387-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-320">Отображение заголовков HTTP</span><span class="sxs-lookup"><span data-stu-id="19387-320">Display HTTP headers</span></span>  

<span data-ttu-id="19387-321">Чтобы отобразить данные заголовка HTTP для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-322">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="19387-323">Перейдите на вкладку **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="19387-323">Choose the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="19387-325">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="19387-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="19387-326">Вывод источника HTTP-заголовков</span><span class="sxs-lookup"><span data-stu-id="19387-326">Display HTTP header source</span></span>  

<span data-ttu-id="19387-327">По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="19387-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="19387-328">Чтобы dsiplay имена HTTP-заголовков в полученном порядке, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-329">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="19387-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="19387-330">Дополнительные сведения можно найти в разделе [Отображение заголовков HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="19387-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="19387-331">Нажмите кнопку **Просмотр источника**рядом с разделом **заголовок запроса** или **заголовок ответа** .</span><span class="sxs-lookup"><span data-stu-id="19387-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="19387-332">Отображение параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="19387-332">Display query string parameters</span></span>  

<span data-ttu-id="19387-333">Чтобы отобразить параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-334">Открытие вкладки " **заголовки** " для запроса, который вас интересует.</span><span class="sxs-lookup"><span data-stu-id="19387-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="19387-335">Дополнительные сведения можно найти в разделе [Отображение заголовков HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="19387-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="19387-336">Перейдите к разделу **Параметры строки запроса** .</span><span class="sxs-lookup"><span data-stu-id="19387-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел "параметры строки запроса"" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="19387-338">Раздел " **Параметры строки запроса** "</span><span class="sxs-lookup"><span data-stu-id="19387-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="19387-339">Показать источник параметров строки запроса</span><span class="sxs-lookup"><span data-stu-id="19387-339">Display query string parameters source</span></span>  

<span data-ttu-id="19387-340">Чтобы отобразить источник параметра строки запроса для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-341">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="19387-342">Дополнительные сведения можно найти в разделе [Отображение параметров строки запроса](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="19387-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="19387-343">Нажмите кнопку **Просмотр источника**.</span><span class="sxs-lookup"><span data-stu-id="19387-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="19387-344">Отображение строковых параметров запроса в кодировке URL</span><span class="sxs-lookup"><span data-stu-id="19387-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="19387-345">Чтобы отобразить параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-346">Перейдите к разделу Параметры строки запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="19387-347">Дополнительные сведения можно найти в разделе [Отображение параметров строки запроса](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="19387-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="19387-348">Выберите команду **Просмотреть закодированный URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="19387-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="19387-349">Отображение файлов cookie</span><span class="sxs-lookup"><span data-stu-id="19387-349">Display cookies</span></span>  

<span data-ttu-id="19387-350">Чтобы отобразить cookie-файлы, отправленные в заголовке запроса HTTP, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-351">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="19387-352">Перейдите на вкладку " **cookie** ".</span><span class="sxs-lookup"><span data-stu-id="19387-352">Choose the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка "cookie"" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="19387-354">Вкладка "cookie"</span><span class="sxs-lookup"><span data-stu-id="19387-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-355">Отображение разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="19387-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="19387-356">Чтобы отобразить разбиение по времени для запроса, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="19387-357">Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="19387-358">Выберите вкладку **время** .</span><span class="sxs-lookup"><span data-stu-id="19387-358">Choose the **Timing** tab.</span></span>  

<span data-ttu-id="19387-359">Для более удобного доступа к данным перейдите к разделу [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="19387-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="19387-360">Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** , можно найти в разделе [этапы разбивки по времени](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="19387-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="19387-362">Вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="19387-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="19387-363">Дополнительные сведения о каждой из фаз.</span><span class="sxs-lookup"><span data-stu-id="19387-363">More information about each of the phases.</span></span>  

<span data-ttu-id="19387-364">Дополнительные сведения о том, как получить доступ к экрану, можно найти в разделе [Отображение временных интервалов](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="19387-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="19387-365">Предварительный просмотр разбивки по времени</span><span class="sxs-lookup"><span data-stu-id="19387-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="19387-366">Чтобы отобразить предварительный просмотр разбиения по времени для запроса, наведите указатель мыши на запись запроса в столбце " **Каскад** " таблицы "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="19387-367">Дополнительные сведения о том, как получить доступ к данным без наведения указателя мыши, можно найти, чтобы [отобразить разбиение по времени для запроса](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="19387-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбиения по времени для запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="19387-369">Предварительный просмотр разбиения по времени для запроса</span><span class="sxs-lookup"><span data-stu-id="19387-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="19387-370">Описание этапов разделения времени</span><span class="sxs-lookup"><span data-stu-id="19387-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="19387-371">Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** .</span><span class="sxs-lookup"><span data-stu-id="19387-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-372">Очередь</span><span class="sxs-lookup"><span data-stu-id="19387-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-373">Браузер помещает запросы в очередь, если выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="19387-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="19387-374">Существуют запросы с более высокими приоритетами.</span><span class="sxs-lookup"><span data-stu-id="19387-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="19387-375">Шесть подключений TCP открыты для одного и того же источника, что является ограничением.</span><span class="sxs-lookup"><span data-stu-id="19387-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="19387-376">Применимо только к HTTP/1.0 и HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="19387-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="19387-377">Браузер временно выделяет место в кэше на диске.</span><span class="sxs-lookup"><span data-stu-id="19387-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-378">Блокированы</span><span class="sxs-lookup"><span data-stu-id="19387-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-379">Запрос будет остановлен в любой из причин, описанных в разделе **очереди**.</span><span class="sxs-lookup"><span data-stu-id="19387-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-380">Поиск DNS</span><span class="sxs-lookup"><span data-stu-id="19387-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-381">Браузер разрешает IP-адрес запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-382">Начальное соединение</span><span class="sxs-lookup"><span data-stu-id="19387-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-383">Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласовывающие безопасный уровень сокетов.</span><span class="sxs-lookup"><span data-stu-id="19387-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-384">Согласование прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="19387-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-385">Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="19387-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-386">Отправлено запросов</span><span class="sxs-lookup"><span data-stu-id="19387-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-387">Запрос отправляется.</span><span class="sxs-lookup"><span data-stu-id="19387-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-388">Подготовка ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="19387-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-389">Браузер запускает сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="19387-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-390">Запрос на ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="19387-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-391">Запрос отправляется сотруднику службы.</span><span class="sxs-lookup"><span data-stu-id="19387-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-392">Ожидание \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="19387-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-393">Браузер ожидает первый байт ответа.</span><span class="sxs-lookup"><span data-stu-id="19387-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="19387-394">TTFB означает время для первого байта.</span><span class="sxs-lookup"><span data-stu-id="19387-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="19387-395">Это время включает один цикл обработки задержки и время, затраченное сервером на подготовку ответа.</span><span class="sxs-lookup"><span data-stu-id="19387-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-396">Загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="19387-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-397">Браузер получает ответ.</span><span class="sxs-lookup"><span data-stu-id="19387-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-398">Получение push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="19387-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-399">Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.</span><span class="sxs-lookup"><span data-stu-id="19387-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="19387-400">Чтение push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="19387-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="19387-401">Браузер читает локальные данные, полученные ранее.</span><span class="sxs-lookup"><span data-stu-id="19387-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="19387-402">Отображение инициаторов и зависимостей</span><span class="sxs-lookup"><span data-stu-id="19387-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="19387-403">Чтобы отобразить инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице "запросы".</span><span class="sxs-lookup"><span data-stu-id="19387-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="19387-404">DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.</span><span class="sxs-lookup"><span data-stu-id="19387-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="19387-406">Отображение инициаторов и зависимостей запроса</span><span class="sxs-lookup"><span data-stu-id="19387-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="19387-407">Если таблица запросы упорядочивается хронологически, при наведении указателя мыши на строку, предшествующую ей, выводится зеленый запрос.</span><span class="sxs-lookup"><span data-stu-id="19387-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="19387-408">Зеленый запрос — инициатор зависимости.</span><span class="sxs-lookup"><span data-stu-id="19387-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="19387-409">Если в строке перед этим отображается еще один зеленый запрос, это более высокий запрос является инициатором инициатора.</span><span class="sxs-lookup"><span data-stu-id="19387-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="19387-410">И так далее.</span><span class="sxs-lookup"><span data-stu-id="19387-410">And so on.</span></span>  

### <span data-ttu-id="19387-411">Вывод событий загрузки</span><span class="sxs-lookup"><span data-stu-id="19387-411">Display load events</span></span>  

<span data-ttu-id="19387-412">DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="19387-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** panel.</span></span>  <span data-ttu-id="19387-413">`DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.</span><span class="sxs-lookup"><span data-stu-id="19387-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и Load на панели "сеть"" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="19387-415">Расположение `DOMContentLoaded` событий "и" `load` на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="19387-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-416">Вывод общего числа запросов</span><span class="sxs-lookup"><span data-stu-id="19387-416">Display the total number of requests</span></span>  

<span data-ttu-id="19387-417">Общее количество запросов можно найти в области **сводки** в нижней части панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="19387-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="19387-418">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="19387-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="19387-419">Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="19387-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="19387-421">Общее количество запросов с момента открытия DevTools</span><span class="sxs-lookup"><span data-stu-id="19387-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-422">Показать общий размер загружаемого файла</span><span class="sxs-lookup"><span data-stu-id="19387-422">Display the total download size</span></span>  

<span data-ttu-id="19387-423">Общий объем загруженных запросов отображается в области **Сводка** в нижней части панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="19387-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="19387-424">Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="19387-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="19387-425">Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.</span><span class="sxs-lookup"><span data-stu-id="19387-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий объем загруженных запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="19387-427">Общий объем загруженных запросов</span><span class="sxs-lookup"><span data-stu-id="19387-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="19387-428">Чтобы убедиться в том, что после того как браузер распаковать все элементы, перейдите к разделу [Отображение несжатого размера ресурса](#display-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="19387-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="19387-429">Отобразить трассировку стека, которая привела к запросу</span><span class="sxs-lookup"><span data-stu-id="19387-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="19387-430">После того как оператор JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы отобразить трассировку стека, которая выводится в соответствии с запросом.</span><span class="sxs-lookup"><span data-stu-id="19387-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека, ведущая к запросу ресурсов" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="19387-432">Трассировка стека, ведущая к запросу ресурсов</span><span class="sxs-lookup"><span data-stu-id="19387-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-433">Отображение несжатого размера ресурса</span><span class="sxs-lookup"><span data-stu-id="19387-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="19387-434">Включите флажок **использовать строки большого запроса** и просмотрите минимальное значение в столбце **Размер** .</span><span class="sxs-lookup"><span data-stu-id="19387-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несжатых ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="19387-436">Пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )</span><span class="sxs-lookup"><span data-stu-id="19387-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="19387-437">Данные запросов на экспорт</span><span class="sxs-lookup"><span data-stu-id="19387-437">Export requests data</span></span>  

### <span data-ttu-id="19387-438">Сохранение всех сетевых запросов в файле HAR</span><span class="sxs-lookup"><span data-stu-id="19387-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="19387-439">Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="19387-440">Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).</span><span class="sxs-lookup"><span data-stu-id="19387-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="19387-441">Выберите команду **Сохранить как HAR с содержимым**.</span><span class="sxs-lookup"><span data-stu-id="19387-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="19387-442">DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.</span><span class="sxs-lookup"><span data-stu-id="19387-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="19387-443">Вы не можете фильтровать запросы.</span><span class="sxs-lookup"><span data-stu-id="19387-443">You are not able to filter requests.</span></span>  <span data-ttu-id="19387-444">Вы также не можете сохранить один запрос.</span><span class="sxs-lookup"><span data-stu-id="19387-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="19387-445">После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.</span><span class="sxs-lookup"><span data-stu-id="19387-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="19387-446">Просто перетащите файл HAR в таблицу запросы.</span><span class="sxs-lookup"><span data-stu-id="19387-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выберите команду "Сохранить как HAR с контентом"" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="19387-448">Выберите команду " **Сохранить как HAR с контентом** "</span><span class="sxs-lookup"><span data-stu-id="19387-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-449">Копирование одного или нескольких запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="19387-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="19387-450">В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши, выберите команду **Копировать**) и выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="19387-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="19387-451">Название</span><span class="sxs-lookup"><span data-stu-id="19387-451">Name</span></span> | <span data-ttu-id="19387-452">Подробные сведения</span><span class="sxs-lookup"><span data-stu-id="19387-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="19387-453">Копировать адрес ссылки</span><span class="sxs-lookup"><span data-stu-id="19387-453">Copy Link Address</span></span>** | <span data-ttu-id="19387-454">Скопируйте URL-адрес запроса в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="19387-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="19387-455">Копирование ответа</span><span class="sxs-lookup"><span data-stu-id="19387-455">Copy Response</span></span>** | <span data-ttu-id="19387-456">Скопировать текст ответа в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="19387-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="19387-457">Копировать как выборку</span><span class="sxs-lookup"><span data-stu-id="19387-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="19387-458">Копирование в виде изогнутого документа</span><span class="sxs-lookup"><span data-stu-id="19387-458">Copy as cURL</span></span>** | <span data-ttu-id="19387-459">Копирование запроса в виде текстовой команды.</span><span class="sxs-lookup"><span data-stu-id="19387-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="19387-460">Копировать все как выборку</span><span class="sxs-lookup"><span data-stu-id="19387-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="19387-461">Копирование в виде изогнутого документа</span><span class="sxs-lookup"><span data-stu-id="19387-461">Copy All as cURL</span></span>** | <span data-ttu-id="19387-462">Копирование всех запросов в виде последовательности команд с фигурой.</span><span class="sxs-lookup"><span data-stu-id="19387-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="19387-463">Копирование всех как HAR</span><span class="sxs-lookup"><span data-stu-id="19387-463">Copy All as HAR</span></span>** | <span data-ttu-id="19387-464">Скопируйте все запросы как данные HAR.</span><span class="sxs-lookup"><span data-stu-id="19387-464">Copy all requests as HAR data.</span></span> |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выберите команду "Копировать ответ"" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="19387-466">Выберите команду " **Копировать ответ** "</span><span class="sxs-lookup"><span data-stu-id="19387-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-467">Копирование формата JSON ответа в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="19387-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="19387-468">Выберите сетевой запрос и перейдите в область **заголовки** .</span><span class="sxs-lookup"><span data-stu-id="19387-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="19387-469">Чтобы скопировать значение JSON отклика, перейдите в **полезные данные запроса**, наведите указатель мыши на содержимое ответа JSON, откройте контекстное меню, а затем выберите команду **Копировать значение**.</span><span class="sxs-lookup"><span data-stu-id="19387-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Копирование значения в контекстном меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="19387-471">**Копирование значения** в контекстном меню</span><span class="sxs-lookup"><span data-stu-id="19387-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Код Visual Studio с форматом JSON ответа" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="19387-473">Вставка форматированного отклика JSON в код Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19387-473">Pasting formatted response JSON in Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="19387-474">Копирование значений свойств из сетевых запросов в буфер обмена</span><span class="sxs-lookup"><span data-stu-id="19387-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="19387-475">Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="19387-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="19387-476">Открытие области " **заголовки** ".</span><span class="sxs-lookup"><span data-stu-id="19387-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="19387-477">Откройте один из следующих разделов заголовка.</span><span class="sxs-lookup"><span data-stu-id="19387-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="19387-478">Полезные данные для запроса \ (JSON \)</span><span class="sxs-lookup"><span data-stu-id="19387-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="19387-479">Данные формы</span><span class="sxs-lookup"><span data-stu-id="19387-479">Form Data</span></span>  
    *   <span data-ttu-id="19387-480">Параметры строки запроса</span><span class="sxs-lookup"><span data-stu-id="19387-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="19387-481">Заголовки запроса</span><span class="sxs-lookup"><span data-stu-id="19387-481">Request Headers</span></span>  
    *   <span data-ttu-id="19387-482">Заголовки ответа</span><span class="sxs-lookup"><span data-stu-id="19387-482">Response Headers</span></span>  
1.  <span data-ttu-id="19387-483">Откройте контекстное меню \ (щелкните правой кнопкой мыши, > **скопировать значение**.</span><span class="sxs-lookup"><span data-stu-id="19387-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="19387-484">Теперь вы можете вставить значение в любой редактор, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="19387-484">You can now paste the value into any editor to review it.</span></span>  
    
## <span data-ttu-id="19387-485">Изменение макета панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="19387-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="19387-486">Вы можете развернуть или свернуть разделы пользовательского интерфейса панели " **сеть** ", чтобы сосредоточиться на важных сведениях.</span><span class="sxs-lookup"><span data-stu-id="19387-486">You may expand or collapse sections of the **Network** panel UI to focus important information.</span></span>  

### <span data-ttu-id="19387-487">Скрытие области фильтров</span><span class="sxs-lookup"><span data-stu-id="19387-487">Hide the Filters pane</span></span>  

<span data-ttu-id="19387-488">По умолчанию DevTools отображает область **фильтров** .</span><span class="sxs-lookup"><span data-stu-id="19387-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="19387-489">Щелкните **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы скрыть его.</span><span class="sxs-lookup"><span data-stu-id="19387-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="19387-491">Кнопка "скрыть фильтры"</span><span class="sxs-lookup"><span data-stu-id="19387-491">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-492">Использование строк большого запроса</span><span class="sxs-lookup"><span data-stu-id="19387-492">Use large request rows</span></span>  

<span data-ttu-id="19387-493">Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.</span><span class="sxs-lookup"><span data-stu-id="19387-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="19387-494">Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.</span><span class="sxs-lookup"><span data-stu-id="19387-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="19387-495">Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.</span><span class="sxs-lookup"><span data-stu-id="19387-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример строк большого запроса в области "запросы"" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="19387-497">Пример строк большого запроса в области " **запросы** "</span><span class="sxs-lookup"><span data-stu-id="19387-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="19387-498">Чтобы включить большие строки, включите флажок **использовать строки большого запроса** .</span><span class="sxs-lookup"><span data-stu-id="19387-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Флажок "использовать строки большого запроса"" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="19387-500">Флажок " **использовать строки большого запроса** "</span><span class="sxs-lookup"><span data-stu-id="19387-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="19387-501">Скрытие области обзора</span><span class="sxs-lookup"><span data-stu-id="19387-501">Hide the Overview pane</span></span>  

<span data-ttu-id="19387-502">По умолчанию DevTools отображает область " **Обзор** ".</span><span class="sxs-lookup"><span data-stu-id="19387-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="19387-503">Чтобы скрыть его, отключите флажок **Показать обзор** .</span><span class="sxs-lookup"><span data-stu-id="19387-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Флажок "Показать общие сведения"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="19387-505">Флажок " **Показать общие сведения** "</span><span class="sxs-lookup"><span data-stu-id="19387-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="19387-506">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="19387-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Отладка последовательного веб-приложения | Документы Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> <span data-ttu-id="19387-510">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19387-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="19387-511">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="19387-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="19387-513">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19387-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
