---
description: Использование панели "Сеть" для отслеживания и запросов ресурсов страницы профиля
title: DevTools — сеть
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, сеть, время загрузки, http, https, кэш браузера, HAR
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 261226c7210d978f11290816c81355bb0142dee9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235596"
---
# <span data-ttu-id="b18f4-104">Network</span><span class="sxs-lookup"><span data-stu-id="b18f4-104">Network</span></span>

<span data-ttu-id="b18f4-105">Используйте панель **"Сеть",** чтобы отслеживать, проверять и профилировать запросы и ответы, отправленные по сети.</span><span class="sxs-lookup"><span data-stu-id="b18f4-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="b18f4-106">С его помощью вы можете:</span><span class="sxs-lookup"><span data-stu-id="b18f4-106">With it, you can:</span></span>

 - <span data-ttu-id="b18f4-107">[Просмотр записи всех запросов ресурсов,](#network-summary) сделанных страницей</span><span class="sxs-lookup"><span data-stu-id="b18f4-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="b18f4-108">[Измерение времени загрузки сайта для](#summary-bar) новых и возвращающих пользователей</span><span class="sxs-lookup"><span data-stu-id="b18f4-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="b18f4-109">[Проверьте заглавные и теле сообщения, параметры](#request-details) и файлы cookie, которые обмениваются между вашей страницей и сетью</span><span class="sxs-lookup"><span data-stu-id="b18f4-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="b18f4-110">[Определение сетевых событий, вызывающих узкие места](#timings) во время загрузки сайта</span><span class="sxs-lookup"><span data-stu-id="b18f4-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![Панель Microsoft Edge DevTools Network](./media/network.png)

## <span data-ttu-id="b18f4-112">Сводка по сети</span><span class="sxs-lookup"><span data-stu-id="b18f4-112">Network summary</span></span>

<span data-ttu-id="b18f4-113">Когда вы открываете DevTools, профилирование сети по умолчанию включено.</span><span class="sxs-lookup"><span data-stu-id="b18f4-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="b18f4-114">Весь сетевой трафик с активной вкладки браузера регистрируется в сводном списке сети, даже если вы работаете на панели DevTools, которая отличается от *"Сеть".*</span><span class="sxs-lookup"><span data-stu-id="b18f4-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![Индикатор профилирование сети в процессе выполнения](./media/network_profile_indicator.png)

### <span data-ttu-id="b18f4-116">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="b18f4-116">Toolbar</span></span>

<span data-ttu-id="b18f4-117">Панель инструментов предоставляет элементы управления для профилирование и фильтрации сетевой активности страницы.</span><span class="sxs-lookup"><span data-stu-id="b18f4-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Панель инструментов профилера сети](./media/network_toolbar.png)

1. <span data-ttu-id="b18f4-119">**Запуск и остановка сеанса**профилирование: по умолчанию профилирование сети включено, и сетевой трафик будет регистрироваться в списке [**сетевых профилей.**](#network-request-list)</span><span class="sxs-lookup"><span data-stu-id="b18f4-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="b18f4-120">Вы можете отключить захват сети с помощью кнопки **"Остановить"** `Ctrl+E` ().</span><span class="sxs-lookup"><span data-stu-id="b18f4-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="b18f4-121">**Экспорт в формате HAR:** вы можете сохранить текущий сеанс профилирование сети () в формате `Ctrl+S` JSON [HTTP Archive (HAR).](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html)</span><span class="sxs-lookup"><span data-stu-id="b18f4-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="b18f4-122">**Фильтр типов контента:** фильтрация списка сетевых запросов по определенным запросам содержимого ( документы, таблицы стилей,*изображения, сценарии, мультимедиа, шрифты, XHR, Другие).*</span><span class="sxs-lookup"><span data-stu-id="b18f4-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="b18f4-123">По умолчанию показаны все типы контента.</span><span class="sxs-lookup"><span data-stu-id="b18f4-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="b18f4-124">**Find**: Filter ( `Ctrl+F` ) the network request list by entry names (resource paths) containing a specified search string.</span><span class="sxs-lookup"><span data-stu-id="b18f4-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="b18f4-125">**Всегда обновляются с сервера:** при нажатии этой кнопки ресурсы страниц будут принудительно загружаться из сети, а не из кэша браузера.</span><span class="sxs-lookup"><span data-stu-id="b18f4-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="b18f4-126">Вы можете обновить страницу из сети один раз, нажав кнопку `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="b18f4-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="b18f4-127">**Обход рабочих служб для всех сетевых запросов:** отключите зарегистрированных сотрудников службы в качестве сетевых прокси-прокси.</span><span class="sxs-lookup"><span data-stu-id="b18f4-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="b18f4-128">Очистка кнопок</span><span class="sxs-lookup"><span data-stu-id="b18f4-128">Clear buttons</span></span>

   - <span data-ttu-id="b18f4-129">**Очистка кэша:** удаляет все ресурсы, хранимые в кэше браузера (и эмулирует первый раз загрузку страницы).</span><span class="sxs-lookup"><span data-stu-id="b18f4-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="b18f4-130">**Очистка файлов cookie:** удаляет все файлы cookie для данного домена (и эмулирует первый раз на сайте).</span><span class="sxs-lookup"><span data-stu-id="b18f4-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="b18f4-131">**Очистка записей при навигации:** записанный трафик очищается при навигации по странице.</span><span class="sxs-lookup"><span data-stu-id="b18f4-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="b18f4-132">Этот режим включен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b18f4-132">This is turned on by default.</span></span>
   - <span data-ttu-id="b18f4-133">**Clear session**: Clear session clears all network request entries from the **Network summary** list.</span><span class="sxs-lookup"><span data-stu-id="b18f4-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="b18f4-134">Список сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="b18f4-134">Network request list</span></span>

<span data-ttu-id="b18f4-135">Весь сетевой трафик записи в список (до тех пор, пока не будет очищен при навигации, вручную очищен или DevTools не будет закрыт).</span><span class="sxs-lookup"><span data-stu-id="b18f4-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="b18f4-136">Если щелкнуть любую запись, откроется более [подробное представление запроса.](#request-details)</span><span class="sxs-lookup"><span data-stu-id="b18f4-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Список сетевых запросов](./media/network_request_list.png)

<span data-ttu-id="b18f4-138">Список сетевых запросов включает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b18f4-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="b18f4-139">Столбец</span><span class="sxs-lookup"><span data-stu-id="b18f4-139">Column</span></span> | <span data-ttu-id="b18f4-140">Описание</span><span class="sxs-lookup"><span data-stu-id="b18f4-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="b18f4-141">Name</span><span class="sxs-lookup"><span data-stu-id="b18f4-141">Name</span></span>** | <span data-ttu-id="b18f4-142">Имя и URL-путь запроса</span><span class="sxs-lookup"><span data-stu-id="b18f4-142">Name and URL path of the request</span></span>
**<span data-ttu-id="b18f4-143">Протокол</span><span class="sxs-lookup"><span data-stu-id="b18f4-143">Protocol</span></span>** |  <span data-ttu-id="b18f4-144">Тип протокола для запроса *(например, HTTPS, HTTP/2)*</span><span class="sxs-lookup"><span data-stu-id="b18f4-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="b18f4-145">Метод</span><span class="sxs-lookup"><span data-stu-id="b18f4-145">Method</span></span>** |    <span data-ttu-id="b18f4-146">[Метод HTTP,](https://developer.mozilla.org/docs/Web/HTTP/Methods) используемый для запроса</span><span class="sxs-lookup"><span data-stu-id="b18f4-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="b18f4-147">Результат</span><span class="sxs-lookup"><span data-stu-id="b18f4-147">Result</span></span>** |    <span data-ttu-id="b18f4-148">[Код состояния http-ответа](https://developer.mozilla.org/docs/Web/HTTP/Status)</span><span class="sxs-lookup"><span data-stu-id="b18f4-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="b18f4-149">Тип содержимого</span><span class="sxs-lookup"><span data-stu-id="b18f4-149">Content type</span></span>** |  <span data-ttu-id="b18f4-150">Тип запрашиваемого мультимедиа[(тип MIME)](https://en.wikipedia.org/wiki/Media_type)</span><span class="sxs-lookup"><span data-stu-id="b18f4-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="b18f4-151">Получено</span><span class="sxs-lookup"><span data-stu-id="b18f4-151">Received</span></span>** | <span data-ttu-id="b18f4-152">Размер ответа, доставленного сервером (не вычисляется для кэшных ответов)</span><span class="sxs-lookup"><span data-stu-id="b18f4-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="b18f4-153">Время</span><span class="sxs-lookup"><span data-stu-id="b18f4-153">Time</span></span>** |  <span data-ttu-id="b18f4-154">Время загрузки ответа сервера (не вычисляется для кэшных ответов)</span><span class="sxs-lookup"><span data-stu-id="b18f4-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="b18f4-155">Инициатор</span><span class="sxs-lookup"><span data-stu-id="b18f4-155">Initiator</span></span>** | <span data-ttu-id="b18f4-156">Подсистема, отвечаемая за инициации запроса *(например, Parser, Redirect, Script, Other)*</span><span class="sxs-lookup"><span data-stu-id="b18f4-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="b18f4-157">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="b18f4-157">Timeline</span></span>** | <span data-ttu-id="b18f4-158">Визуальная временная шкала для сетевых событий запроса (таких как *"Ожидание", "Разрешение(DNS"), "Подключение(TCP"), "SSL", "Отправка", "Ожидание" (TTFB), "Загрузка").*</span><span class="sxs-lookup"><span data-stu-id="b18f4-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="b18f4-159">Наведении курсор на диаграмму обеспечивает более детализированное распределение времени [сетевой сети).](#timings)</span><span class="sxs-lookup"><span data-stu-id="b18f4-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="b18f4-160">Сводка</span><span class="sxs-lookup"><span data-stu-id="b18f4-160">Summary bar</span></span>

<span data-ttu-id="b18f4-161">Панель в нижней \*\*\*\* части панели "Сеть" суммирует общее количество ошибок, запросов, передачи данных и времени загрузки HTTP в течение сеанса профилирования сети (то есть, так как были открыты devTools и записывают сетевой трафик).</span><span class="sxs-lookup"><span data-stu-id="b18f4-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Сводка по сети](./media/network_summary_bar.png)

<span data-ttu-id="b18f4-163">**По иному времени** это время между началом сеанса профилированием и моментом последнего скачивания ресурса из сети.</span><span class="sxs-lookup"><span data-stu-id="b18f4-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="b18f4-164">Ресурсы, извлеченные из кэша браузера, не накапливают время на это число.</span><span class="sxs-lookup"><span data-stu-id="b18f4-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="b18f4-165">Время загрузки **DOM** означает время между началом сеанса профилированием и [событием DOMContentLoaded,](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) чтобы указать, что структура документа страницы загружена и различна (хотя не обязательно любые таблицы стилей, изображения или подкадры).</span><span class="sxs-lookup"><span data-stu-id="b18f4-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="b18f4-166">**Время загрузки** страницы означает время между началом сеанса [](https://developer.mozilla.org/docs/Web/Events/load) профилирование и событием загрузки, чтобы указать, что документ страницы (и все его ресурсы) полностью загружен.</span><span class="sxs-lookup"><span data-stu-id="b18f4-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="b18f4-167">Сведения о запросе</span><span class="sxs-lookup"><span data-stu-id="b18f4-167">Request details</span></span>

<span data-ttu-id="b18f4-168">Если щелкнуть любую [\*\*\*\*](#network-summary) запись в сводке [\*\*\*\*](#request-details) по сети, откроется области сведений о запросах с дополнительными сведениями на каждой из следующих вкладок.</span><span class="sxs-lookup"><span data-stu-id="b18f4-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Области сведений о сетевых запросах](./media/network_request_details.png)

### <span data-ttu-id="b18f4-170">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b18f4-170">Headers</span></span>
<span data-ttu-id="b18f4-171">Отображает [http-заготки,](https://developer.mozilla.org/docs/Web/HTTP/Headers) отправленные и полученные с сервера.</span><span class="sxs-lookup"><span data-stu-id="b18f4-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="b18f4-172">Щелкните правой кнопкой мыши любую запись в загонах, чтобы скопировать ее `Ctrl+C` () в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="b18f4-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b18f4-173">Вы также можете выбрать несколько записей, удерживая `Shift` клавишу или выбрав все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b18f4-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="b18f4-174">Body</span><span class="sxs-lookup"><span data-stu-id="b18f4-174">Body</span></span>
<span data-ttu-id="b18f4-175">Отображает данные тела (если они доступны) для полезной нагрузки запроса и ответа.</span><span class="sxs-lookup"><span data-stu-id="b18f4-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="b18f4-176">Содержимое изображения отображается с данными о размерах и измерениях.</span><span class="sxs-lookup"><span data-stu-id="b18f4-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="b18f4-177">Текстовое содержимое отображается в редакторе (только для чтения) \*\*\*\* с возможностью формата минифицированного содержимого с помощью "Очень печать" и/или **переноса в Word** для упростить чтение.</span><span class="sxs-lookup"><span data-stu-id="b18f4-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Вкладка "Тело" области сведений о запросе](./media/network_details_body.png)

### <span data-ttu-id="b18f4-179">Параметры</span><span class="sxs-lookup"><span data-stu-id="b18f4-179">Parameters</span></span>
<span data-ttu-id="b18f4-180">Отображает параметры строки запроса для запросов GET.</span><span class="sxs-lookup"><span data-stu-id="b18f4-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="b18f4-181">Хотя параметры запросов POST отправляются в загонах, запросы GET включают их в URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b18f4-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="b18f4-182">Они разбиты здесь для упростить чтение.</span><span class="sxs-lookup"><span data-stu-id="b18f4-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="b18f4-183">Щелкните правой кнопкой мыши любую строку, чтобы скопировать ее `Ctrl+C` () в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="b18f4-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b18f4-184">Вы также можете выбрать несколько записей, удерживая `Shift` клавишу или выбрав все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b18f4-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="b18f4-185">Файлы cookie</span><span class="sxs-lookup"><span data-stu-id="b18f4-185">Cookies</span></span>
<span data-ttu-id="b18f4-186">Отображает файлы cookie, отправленные или полученные в качестве пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="b18f4-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="b18f4-187">Щелкните правой кнопкой мыши любую строку, чтобы скопировать ее `Ctrl+C` () в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="b18f4-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="b18f4-188">Вы также можете выбрать несколько записей, удерживая клавишу или выбрав `Shift` все ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="b18f4-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="b18f4-189">Вы можете очистить сохраненные файлы cookie для заданного домена с панели [инструментов](#network-summary) (кнопка **"Очистить файлы cookie").**</span><span class="sxs-lookup"><span data-stu-id="b18f4-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="b18f4-190">Сроки</span><span class="sxs-lookup"><span data-stu-id="b18f4-190">Timings</span></span>

<span data-ttu-id="b18f4-191">Вкладка **"Синхронизация"** предоставляет временную шкалу сетевых событий, участвующих в загрузке выбранного ресурса.</span><span class="sxs-lookup"><span data-stu-id="b18f4-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="b18f4-192">Это аналогично сведениям, найденным в столбце "Временная шкала" списка сетевых [запросов,](#network-request-list)но также включают события, ведущие к отправлению запроса по сети, такие как время, затраченное на ожидание (ожидание) в очереди запросов, разрешение DNS и установление подключения TCP. \*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="b18f4-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Вкладка "Синхронизация" области сведений о запросе](./media/network_details_timings.png)

<span data-ttu-id="b18f4-194">Отмечены перенаправления к другим ресурсам, и при нажатии ссылки будет установлен фокус на этом ресурсе в области сведений о [сетевых запросах.](#request details)</span><span class="sxs-lookup"><span data-stu-id="b18f4-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="b18f4-195">На повторное загрузку из кэша не влияет задержка сети, поэтому \*\* диаграмма "Синхронизация сети" не будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="b18f4-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Перенаправленный ресурс, загруженный из кэша](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="b18f4-197">Ниже дано несколько сетевых событий для данного ресурса в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="b18f4-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="b18f4-198">Приостановлено</span><span class="sxs-lookup"><span data-stu-id="b18f4-198">Stalled</span></span>

<span data-ttu-id="b18f4-199">Время, затраченное на ожидание доступного сетевого подключения в очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="b18f4-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="b18f4-200">Для HTTP 1.0/1.1 Microsoft Edge допускает до шести (6) одновременных подключений TCP на имя хоста.</span><span class="sxs-lookup"><span data-stu-id="b18f4-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="b18f4-201">Разрешение (DNS)</span><span class="sxs-lookup"><span data-stu-id="b18f4-201">Resolving (DNS)</span></span>

<span data-ttu-id="b18f4-202">Время, затраченное на поиск IP-адреса для имени хоста ресурса в DNS[(система доменных имен).](https://en.wikipedia.org/wiki/Domain_Name_System)</span><span class="sxs-lookup"><span data-stu-id="b18f4-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="b18f4-203">Подключение (TCP)</span><span class="sxs-lookup"><span data-stu-id="b18f4-203">Connecting (TCP)</span></span>

<span data-ttu-id="b18f4-204">Время, затраченное на установление подключения по протоколу TCP ([Transmission Control Protocol).](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)</span><span class="sxs-lookup"><span data-stu-id="b18f4-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="b18f4-205">SSL</span><span class="sxs-lookup"><span data-stu-id="b18f4-205">SSL</span></span>

<span data-ttu-id="b18f4-206">Время, затраченное на согласование подключения SSL[(слоя secure Sockets Layer)](https://en.wikipedia.org/wiki/Transport_Layer_Security)к прокси-серверу для хоста. [](https://en.wikipedia.org/wiki/Proxy_server)</span><span class="sxs-lookup"><span data-stu-id="b18f4-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="b18f4-207">Отправка</span><span class="sxs-lookup"><span data-stu-id="b18f4-207">Sending</span></span>

<span data-ttu-id="b18f4-208">Время, затраченное на отправку запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="b18f4-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="b18f4-209">Ожидание (TTFB)</span><span class="sxs-lookup"><span data-stu-id="b18f4-209">Waiting (TTFB)</span></span>

<span data-ttu-id="b18f4-210">Время, затраченное на ожидание первого byte ответа от хост-сервера ("время до первого byte", или *TTFB).*</span><span class="sxs-lookup"><span data-stu-id="b18f4-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="b18f4-211">Загрузка</span><span class="sxs-lookup"><span data-stu-id="b18f4-211">Downloading</span></span>

<span data-ttu-id="b18f4-212">Время, затраченное на чтение ответа с сервера.</span><span class="sxs-lookup"><span data-stu-id="b18f4-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="b18f4-213">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="b18f4-213">Shortcuts</span></span>

| <span data-ttu-id="b18f4-214">Действие</span><span class="sxs-lookup"><span data-stu-id="b18f4-214">Action</span></span>                         | <span data-ttu-id="b18f4-215">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="b18f4-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="b18f4-216">Запуск и остановка сеанса профилирование</span><span class="sxs-lookup"><span data-stu-id="b18f4-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="b18f4-217">Экспорт в качестве HAR</span><span class="sxs-lookup"><span data-stu-id="b18f4-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="b18f4-218">Поиск</span><span class="sxs-lookup"><span data-stu-id="b18f4-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="b18f4-219">Копировать</span><span class="sxs-lookup"><span data-stu-id="b18f4-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="b18f4-220">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="b18f4-220">Known Issues</span></span>

### <span data-ttu-id="b18f4-221">Не удалось запустить агент сбора данных сети.</span><span class="sxs-lookup"><span data-stu-id="b18f4-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="b18f4-222">Если вы видите это \*\*\*\* сообщение об ошибке: агенту сетевой коллекции не удалось запуститься в средстве Network, выполните следующие действия для обходного решения.</span><span class="sxs-lookup"><span data-stu-id="b18f4-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b18f4-223">Нажмите `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b18f4-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b18f4-224">В диалоговом окке "Выполнить" **введите services.msc**.</span><span class="sxs-lookup"><span data-stu-id="b18f4-224">In the Run dialog, enter **services.msc**.</span></span>
![known-issues-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b18f4-226">Найдите стандартную службу сборщика Microsoft **(R) Diagnostics Hub** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="b18f4-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![known-issues-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b18f4-228">Перезапустите стандартную службу сборщика Microsoft **(R) Diagnostics Hub.**</span><span class="sxs-lookup"><span data-stu-id="b18f4-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![known-issues-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b18f4-230">Закроем Инструменты разработчика Microsoft Edge и вкладку. Откройте новую вкладку, перейдите на страницу и нажмите `F12` .</span><span class="sxs-lookup"><span data-stu-id="b18f4-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b18f4-231">Теперь рядом с сетью \*\*\*\* должен отсутт уже значок воспроизведения и сетевые запросы для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="b18f4-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![known-issues-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="b18f4-233">По-прежнему возникают проблемы?</span><span class="sxs-lookup"><span data-stu-id="b18f4-233">Still running into problems?</span></span> <span data-ttu-id="b18f4-234">Отправьте нам свой отзыв с помощью **значка отправки отзыва!**</span><span class="sxs-lookup"><span data-stu-id="b18f4-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![known-issues-5](./media/known_issues_5.PNG)

### <span data-ttu-id="b18f4-236">Агенту сетевой коллекции не удалось остановиться.</span><span class="sxs-lookup"><span data-stu-id="b18f4-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="b18f4-237">Если вы видите это \*\*\*\* сообщение об ошибке: агенту сетевой коллекции не удалось остановиться в средстве Network, выполните следующие действия для обходного решения.</span><span class="sxs-lookup"><span data-stu-id="b18f4-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="b18f4-238">Нажмите `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="b18f4-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="b18f4-239">В диалоговом окке "Выполнить" **введите services.msc**.</span><span class="sxs-lookup"><span data-stu-id="b18f4-239">In the Run dialog, enter **services.msc**.</span></span>
![known-issues-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="b18f4-241">Найдите стандартную службу сборщика Microsoft **(R) Diagnostics Hub** и щелкните ее правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="b18f4-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![known-issues-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="b18f4-243">Перезапустите стандартную службу сборщика Microsoft **(R) Diagnostics Hub.**</span><span class="sxs-lookup"><span data-stu-id="b18f4-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![known-issues-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="b18f4-245">Закроем Инструменты разработчика Microsoft Edge и вкладку. Откройте новую вкладку, перейдите на страницу и нажмите `F12` .</span><span class="sxs-lookup"><span data-stu-id="b18f4-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="b18f4-246">Теперь рядом с сетью \*\*\*\* должен отсутт уже значок воспроизведения и сетевые запросы для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="b18f4-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![known-issues-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="b18f4-248">По-прежнему возникают проблемы?</span><span class="sxs-lookup"><span data-stu-id="b18f4-248">Still running into problems?</span></span> <span data-ttu-id="b18f4-249">Отправьте нам свой отзыв с помощью **значка отправки отзыва!**</span><span class="sxs-lookup"><span data-stu-id="b18f4-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![known-issues-5](./media/known_issues_5.PNG)
