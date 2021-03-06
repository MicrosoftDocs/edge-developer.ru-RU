---
description: Функции отладки сетки CSS, запросы на редактирование и воспроизведение с сетевой консоли и другие.
title: Новые возможности в DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3085153b87f09c1b5aba8fbe43c42cef0851fa9c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397757"
---
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="3493d-104">Что нового в DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="3493d-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3493d-105">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3493d-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="3493d-106">В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="3493d-107">Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.</span><span class="sxs-lookup"><span data-stu-id="3493d-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="3493d-108">Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте команде Microsoft [Edge DevTools в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="3493d-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="3493d-109">Функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="3493d-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3493d-111">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3493d-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-112">Команда Microsoft Edge DevTools сотрудничает с командой Chrome DevTools и сообществом Chromium, чтобы добавить новые функции отладки сетки CSS в DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="3493d-113">Теперь вы можете отображать номера линий сетки, пробелы в сетке и расширенные строки сетки в качестве наложения на страницу.</span><span class="sxs-lookup"><span data-stu-id="3493d-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="3493d-114">Кроме того, в ближайшее время будут усовершенствования средств сетки.</span><span class="sxs-lookup"><span data-stu-id="3493d-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Функции отладки сетки CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="3493d-116">Функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="3493d-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3493d-117">Чтобы включить эксперимент, [][DevtoolsExperimentalFeaturesTurnOn] перейдите к экспериментальным функциям и выберите почтовый ящик рядом с включить новые функции отладки **CSS Grid.**</span><span class="sxs-lookup"><span data-stu-id="3493d-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="3493d-118">Чтобы попробовать эксперимент с образцом, перейдите к [примеру планировщика сетки CSS.][CodepenRachelweilYzwBzKM]</span><span class="sxs-lookup"><span data-stu-id="3493d-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="3493d-119">Проблема Chromium [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="3493d-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="3493d-120">Редактирование и воспроизведение запросов с помощью сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="3493d-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3493d-122">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3493d-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-123">Теперь вы можете использовать **редактирование** и воспроизведение запросов в сетевом журнале [с][DevtoolsNetworkIndexLogActivity] помощью **сетевой консоли.**</span><span class="sxs-lookup"><span data-stu-id="3493d-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Редактирование и воспроизведение запроса в NetworkLog с помощью сетевой консоли" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="3493d-125">Редактирование и воспроизведение запроса в [NetworkLog][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**</span><span class="sxs-lookup"><span data-stu-id="3493d-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-126">Новая панель сетевой консоли открывается в [ящике DevTools][DevtoolsCustomizeIndexDrawer] и автоматически заполняется информацией для запроса HTTP. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3493d-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="3493d-127">Чтобы отобразить ответ, возвращаемый с сервера, отредактировать запрос \(если это необходимо\) и выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3493d-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="3493d-128">Можно также использовать **сетевой консоли** для создания и отправки http-запросов непосредственно из DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Панель сетевой консоли" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="3493d-130">Панель **сетевой консоли**</span><span class="sxs-lookup"><span data-stu-id="3493d-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="3493d-131">Чтобы **отобразить** консоль Сети в главной панели \(top\) вместо [ящика DevTools,][DevtoolsCustomizeIndexDrawer]перейдите к перемещая [средствам между панелями.](#move-tools-between-panels)</span><span class="sxs-lookup"><span data-stu-id="3493d-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="3493d-132">Чтобы включить эксперимент, перейдите к [включаем][DevtoolsExperimentalFeaturesTurnOn] экспериментальные функции и выберите почтовый ящик рядом с **сетевой консолью.**</span><span class="sxs-lookup"><span data-stu-id="3493d-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="3493d-133">Откройте [сетевой журнал,][DevtoolsNetworkIndexLogActivity]откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.</span><span class="sxs-lookup"><span data-stu-id="3493d-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="3493d-134">Проблема Chromium [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="3493d-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="3493d-135">Работник службы отвечает На события во вкладке Timing</span><span class="sxs-lookup"><span data-stu-id="3493d-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="3493d-136">Вкладка **Timing** средства **Network** теперь включает события `respondWith` сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="3493d-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="3493d-137">Событие сотрудника службы показывает продолжительность времени, непосредственно перед началом работы обработника событий сотрудника службы до времени, когда обещание обработника `respondWith` `fetch` будет `respondWith` `fetch` урегулировано.</span><span class="sxs-lookup"><span data-stu-id="3493d-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Событие respondWith service worker на вкладке Timing панели Network" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="3493d-139">Событие `respondWith` сотрудника службы на **вкладке Timing** средства **Network**</span><span class="sxs-lookup"><span data-stu-id="3493d-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-140">Расширение **ответов,** полученных для отображения дополнительных сведений `fetch` из ответа, как `CacheStorageCacheName` , и `serviceWorkerResponseSource` `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="3493d-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Расширение ответов, полученных для отображения дополнительных сведений из ответа на выборки" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="3493d-142">Расширение **ответов,** полученных для отображения дополнительных сведений из `fetch` ответа</span><span class="sxs-lookup"><span data-stu-id="3493d-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-143">Проблема Chromium [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="3493d-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="3493d-144">webhint feedback in the Issues panel</span><span class="sxs-lookup"><span data-stu-id="3493d-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3493d-146">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3493d-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-147">[webhint][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени о доступности, совместимости между браузерами, безопасности, производительности, PWAs и других распространенных проблемах веб-разработки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="3493d-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="3493d-148">Просмотр отзывов веб-сайтов в панели ["Проблемы".][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="3493d-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="3493d-150">webhint feedback in the Issues panel</span><span class="sxs-lookup"><span data-stu-id="3493d-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3493d-151">Чтобы включить эксперимент, перейдите к [включаем экспериментальные функции][DevtoolsExperimentalFeaturesTurnOn] и выберите почтовый ящик рядом с **веб-хинтом Enable**.</span><span class="sxs-lookup"><span data-stu-id="3493d-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="3493d-152">Откройте панель ["Проблемы",][DevtoolsIssues] чтобы отобразить отзывы из веб-хинта.</span><span class="sxs-lookup"><span data-stu-id="3493d-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="3493d-153">Проблема Chromium [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="3493d-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="3493d-154">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="3493d-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   <span data-ttu-id="3493d-156">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="3493d-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-157">Обычно такие средства, как **Elements** и **Network,** могут открываться только в основной панели \(top\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="3493d-158">Аналогичным образом такие средства, как **3D View** и **Issues,** могут открываться только в панели ящика \(bottom\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="3493d-159">Теперь вы можете настроить макет DevTools, перемещая инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="3493d-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Перемещение инструментов между панелями" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="3493d-161">Перемещение инструментов между панелями</span><span class="sxs-lookup"><span data-stu-id="3493d-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3493d-162">Чтобы включить эксперимент, [][DevtoolsExperimentalFeaturesTurnOn] перейдите к включаем экспериментальные функции и выберите контрольный ящик рядом, чтобы включить поддержку для перемещения вкладок **между панелями.**</span><span class="sxs-lookup"><span data-stu-id="3493d-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="3493d-163">Проблема Chromium [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="3493d-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="3493d-164">Улучшенный инструментарий Инициатора в панели Network</span><span class="sxs-lookup"><span data-stu-id="3493d-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="3493d-165">В Microsoft Edge 83 и 84 в сетевом журнале с горизонтальной панелью [][DevtoolsNetworkIndexLogActivity] прокрутки отображаются инструменты для столбца Инициатор, который показывает причину запроса ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3493d-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="3493d-166">Отобразить стек вызовов, который инициировал запрос, удалось только путем горизонтального прокрутки в панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3493d-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Инструментарий Инициатора в Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="3493d-168">Инструментарий Инициатора в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="3493d-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-169">Начиная с Microsoft Edge 85, теперь вы можете отображать стек вызовов Инициатора в панели инструментов без прокрутки по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="3493d-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Инструментарий Инициатора в Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="3493d-171">Инструментарий Инициатора в Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="3493d-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="3493d-172">Проблема Chromium [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="3493d-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="3493d-173">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="3493d-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="3493d-174">В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 85, которые были внесены в проект Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="3493d-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="3493d-175">Редактирование стилей для структур CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="3493d-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="3493d-176">В **области Стилей** теперь лучше поддерживать стили редактирования, созданные с API объектов [CSS (CSSOM).][CsswgDraftsCssom]</span><span class="sxs-lookup"><span data-stu-id="3493d-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="3493d-177">Многие инфраструктуры и библиотеки CSS-in-JS используют API CSSOM под капотом для создания стилей.</span><span class="sxs-lookup"><span data-stu-id="3493d-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="3493d-178">Теперь вы можете изменять стили, добавленные в JavaScript, используя [таблицы конструкторских стилей.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="3493d-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="3493d-179">Конструкторные таблицы стилей — это новый способ создания и распространения многоиспользоваемых стилей при использовании [теневого DOM.][MdnShadowDom]</span><span class="sxs-lookup"><span data-stu-id="3493d-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="3493d-180">Например, `h1` стили, добавленные `CSSStyleSheet` с API CSSOM\), ранее не редактироваться не были.</span><span class="sxs-lookup"><span data-stu-id="3493d-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="3493d-181">Стили теперь можно изменить в панели **Стилей.**</span><span class="sxs-lookup"><span data-stu-id="3493d-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Изменение фонового свойства стилей h1, добавленных cSSStyleSheet с розового на lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="3493d-183">Изменение `background` свойства `h1` стилей, добавленных `CSSStyleSheet` с на `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="3493d-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="3493d-184">Попробуйте использовать эту функцию с помощью примера [CSS-in-JS.][CodepenZoherghadyaliAbdgrpz]</span><span class="sxs-lookup"><span data-stu-id="3493d-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="3493d-185">Проблема Chromium [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="3493d-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="3493d-186">Маяк 6 в панели Маяк</span><span class="sxs-lookup"><span data-stu-id="3493d-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="3493d-187">Панель **Lighthouse** теперь работает Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="3493d-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="3493d-188">Полный список всех изменений перейдите к [заметкам о выпуске v6.0.0.][GithubGoogleChromeLighthouse600]</span><span class="sxs-lookup"><span data-stu-id="3493d-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="3493d-189">Маяк 6.0 вводит в отчет три новые метрики: Самая большая контентная краска \(LCP\), Накопительная смена макета \(CLS\) и Общее время блокировки \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="3493d-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="3493d-190">Формула показателей производительности также была перенагружена, чтобы лучше отражать нагрузку пользователя.</span><span class="sxs-lookup"><span data-stu-id="3493d-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="3493d-191">Проблема Chromium [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="3493d-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="3493d-192">Первая амортизации содержательной краски</span><span class="sxs-lookup"><span data-stu-id="3493d-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="3493d-193">Первая значимая краска \(FMP\) отстает в Lighthouse 6.0.</span><span class="sxs-lookup"><span data-stu-id="3493d-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="3493d-194">FMP также удален из панели **Performance.**</span><span class="sxs-lookup"><span data-stu-id="3493d-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="3493d-195">**Самая большая контентная краска** — это рекомендуемая замена для FMP.</span><span class="sxs-lookup"><span data-stu-id="3493d-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="3493d-196">Проблема Chromium [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="3493d-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="3493d-197">Поддержка новых функций JavaScript</span><span class="sxs-lookup"><span data-stu-id="3493d-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="3493d-198">DevTools теперь лучше поддерживает некоторые из последних языковых функций JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3493d-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="3493d-199">[Необязательный][V8DevOptionalChaining] автозаполнение синтаксиса цепочки</span><span class="sxs-lookup"><span data-stu-id="3493d-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3493d-200">Автоматическое завершение свойства в **консоли** теперь поддерживает необязательный синтаксис цепочки, например, теперь работает в дополнение к  `name?.` и `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="3493d-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="3493d-201">Синтаксис выделения для [частных полей][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="3493d-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3493d-202">Поля частных классов теперь правильно выделены синтаксис и довольно напечатаны в **панели Источники.**</span><span class="sxs-lookup"><span data-stu-id="3493d-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="3493d-203">Синтаксис, выделяющийся для [оператора совмещений Nullish][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="3493d-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="3493d-204">DevTools теперь правильно печатает nullish coalescing operator в **панели Источники.**</span><span class="sxs-lookup"><span data-stu-id="3493d-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3493d-205">Проблемы Chromium [#1073903,][CR1073903] [#1083214][CR1083214], [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="3493d-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="3493d-206">Новые предупреждения о ярлыке приложения в области Манифест</span><span class="sxs-lookup"><span data-stu-id="3493d-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="3493d-207">**Ярлыки приложений помогают** пользователям быстро приступить к общим или рекомендуемым задачам в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="3493d-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="3493d-208">В **области Манифест** теперь показаны предупреждения для следующих условий.</span><span class="sxs-lookup"><span data-stu-id="3493d-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="3493d-209">Значки ярлыка приложения меньше 96x96 пикселей</span><span class="sxs-lookup"><span data-stu-id="3493d-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="3493d-210">Значки ярлыка приложения и значки манифеста не являются квадратными \(так как значки игнорируются\)</span><span class="sxs-lookup"><span data-stu-id="3493d-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Предупреждения о ярлыке приложения" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="3493d-212">Предупреждения о ярлыке приложения</span><span class="sxs-lookup"><span data-stu-id="3493d-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-213">Проблема Chromium [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="3493d-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="3493d-214">Последовательное отображение вычислительной области</span><span class="sxs-lookup"><span data-stu-id="3493d-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="3493d-215">Компьютерная **области** в **инструменте Elements** теперь последовательно отображается в качестве области во всех размерах viewport.</span><span class="sxs-lookup"><span data-stu-id="3493d-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="3493d-216">Ранее **вычислительная часть** слилась в области **Стилей,** когда ширина представления DevTools была узкой.</span><span class="sxs-lookup"><span data-stu-id="3493d-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Вычислительная области последовательно отображает в качестве отдельной области, даже если DevTools являются узкими" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="3493d-218">Компьютерная **области** последовательно отображает в качестве отдельной области, даже если DevTools являются узкими.</span><span class="sxs-lookup"><span data-stu-id="3493d-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="3493d-219">Проблема Chromium [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="3493d-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="3493d-220">Смещение bytecode для файлов WebAssembly</span><span class="sxs-lookup"><span data-stu-id="3493d-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="3493d-221">DevTools теперь использует смещения bytecode для отображения номеров строки разборки Wasm.</span><span class="sxs-lookup"><span data-stu-id="3493d-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="3493d-222">Номера строк делают более понятным, что вы смотрите на двоичные данные, и в большей мере соответствуют расположениям ссылок на время запуска Wasm.</span><span class="sxs-lookup"><span data-stu-id="3493d-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="3493d-223">Проблема Chromium [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="3493d-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="3493d-224">Line-wise copy and cut in Sources Panel</span><span class="sxs-lookup"><span data-stu-id="3493d-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="3493d-225">При выполнении копирования или вырезания без выбора в редакторе панели [Источников,][DevtoolsSourcesEditCssJavascript]DevTools копирует или режет текущую строку контента.</span><span class="sxs-lookup"><span data-stu-id="3493d-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="С помощью курсора в конце строки 5 скопируйте всю строку из pen.js в DevTools и вклеив Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="3493d-227">С помощью курсора в конце строки 5 скопируйте всю строку из **pen.js** в DevTools и вклеив [Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="3493d-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="3493d-228">Проблема Chromium [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="3493d-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="3493d-229">Обновления параметров консоли</span><span class="sxs-lookup"><span data-stu-id="3493d-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="3493d-230">Разгруппировка тех же сообщений консоли</span><span class="sxs-lookup"><span data-stu-id="3493d-230">Ungroup same console messages</span></span>  

<span data-ttu-id="3493d-231">Группа, **похожая** на параметры консоли, теперь применяется к дублирующимся сообщениям.</span><span class="sxs-lookup"><span data-stu-id="3493d-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="3493d-232">Раньше он просто применялся к подобным сообщениям.</span><span class="sxs-lookup"><span data-stu-id="3493d-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="3493d-233">Например, ранее DevTools не разгруппировали сообщения, даже несмотря на то, что подобная группа не `hello` была перенастройкой. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3493d-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="3493d-234">Теперь сообщения `hello` негруппировываются.</span><span class="sxs-lookup"><span data-stu-id="3493d-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="При неконтраншировке аналогичных групп сообщения привета негруппировываются" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="3493d-236">При \*\*\*\* неконтраншировке аналогичных групп сообщения `hello` негруппировываются</span><span class="sxs-lookup"><span data-stu-id="3493d-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="3493d-237">Дайте этой функции попробовать [пример, который отправляет дублирующиеся сообщения на консоль][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="3493d-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="3493d-238">Проблема Chromium [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="3493d-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="3493d-239">Сохраняемая только параметры выбранного контекста</span><span class="sxs-lookup"><span data-stu-id="3493d-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="3493d-240">В **настоящее время сохраняются** только параметры выбранного контекста в параметрах консоли.</span><span class="sxs-lookup"><span data-stu-id="3493d-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="3493d-241">Ранее параметры сбрасывались при каждом закрытии и возобновлении работы DevTools.</span><span class="sxs-lookup"><span data-stu-id="3493d-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="3493d-242">Это изменение делает поведение параметра совместимым с другими настройками консоли.</span><span class="sxs-lookup"><span data-stu-id="3493d-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Только параметр выбранного контекста" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="3493d-244">**Только параметр выбранного** контекста</span><span class="sxs-lookup"><span data-stu-id="3493d-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-245">Проблема Chromium [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="3493d-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="3493d-246">Обновления панели производительности</span><span class="sxs-lookup"><span data-stu-id="3493d-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="3493d-247">Сведения о кэше компиляции JavaScript в **средстве Performance**</span><span class="sxs-lookup"><span data-stu-id="3493d-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="3493d-248">[Сведения о кэше компиляции JavaScript][V8DevCodeCaching] теперь всегда отображаются в панели **сводки** средства **Performance.**</span><span class="sxs-lookup"><span data-stu-id="3493d-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="3493d-249">Ранее в DevTools не было ничего, связанного с кэшингом кода, если кэшировать код не удалось.</span><span class="sxs-lookup"><span data-stu-id="3493d-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Сведения о кэше компиляции JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="3493d-251">Сведения о кэше компиляции JavaScript</span><span class="sxs-lookup"><span data-stu-id="3493d-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-252">Проблема Chromium [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="3493d-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="3493d-253">Выравнивание времени навигации в панели Performance</span><span class="sxs-lookup"><span data-stu-id="3493d-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="3493d-254">Панель **Performance** используется для показа времени в линейках на основе начала записи.</span><span class="sxs-lookup"><span data-stu-id="3493d-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="3493d-255">Теперь время изменилось для записей, в которых пользователь перемещается, где в DevTools теперь указывается время линейки относительно навигации.</span><span class="sxs-lookup"><span data-stu-id="3493d-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Выравнивание времени навигации в средстве Performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="3493d-257">Выравнивание времени навигации в **средстве Performance**</span><span class="sxs-lookup"><span data-stu-id="3493d-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-258">Время для событий , First Paint, First Contentful Paint и Biggest Contentful Paint обновляется по отношению к началу навигации, что означает, что время совпадает со сроками, о которых сообщается `DOMContentLoaded` `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="3493d-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="3493d-259">Проблема Chromium [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="3493d-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="3493d-260">Новые значки для точек разрыва, условных точек и точек входа</span><span class="sxs-lookup"><span data-stu-id="3493d-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="3493d-261">Панель **Источников** имеет новые проекты для точек разрыва, условных точек и точек входа.</span><span class="sxs-lookup"><span data-stu-id="3493d-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="3493d-262">Точки breakpoints представлены красным кругом, как и [Visual Studio код][VisualStudioCode] [и Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="3493d-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="3493d-263">Значки добавляются для дифференцировать условные точки и точки входа.</span><span class="sxs-lookup"><span data-stu-id="3493d-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Точки останова" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="3493d-265">Точки останова</span><span class="sxs-lookup"><span data-stu-id="3493d-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="3493d-266">Проблема Chromium [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="3493d-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="3493d-267">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="3493d-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="3493d-268">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3493d-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="3493d-269">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="3493d-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="3493d-270">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3493d-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Изменение CSS и JavaScript — обзор панели источников | Документы Майкрософт"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Сетевое действие журнала — Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для CSS-in-JS frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправка дублирующих сообщений в консольные | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планирования сетки CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR800028]: https://crbug.com/800028 "Дублировать ярлык строки в редакторе Средства разработчика, не работая после обновления Chrome | Ошибки Chromium"  
[CR912581]: https://crbug.com/912581 "Показать, какие скрипты были кэшироваться V8 в DevTools/about:tracing | Ошибки Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель стилей DevTools не работает со построенными таблицами стилей | Ошибки Chromium"  
[CR955497]: https://crbug.com/955497 "Меню ярлыка значка приложения для pwAs | Ошибки Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие показателей между панелью Perf и performanceObserver | Ошибки Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшение цветов для точек | Ошибки Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение параметра выбранной консоли только контекста не сохраняется после закрытия и открытия средств разработки | Ошибки Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Show ServiceWorkers Fetch Timeline per request in Network panel | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка computed style исчезает в режиме отклика | Ошибки Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксиса не работает с частными полями | Ошибки Chromium"  
[CR1082963]: https://crbug.com/1082963 "Нельзя отключить аналогичное поведение сообщений группы консоли | Ошибки Chromium"  
[CR1083214]: https://crbug.com/1083214 "acorn не поддерживает необязательный | Ошибки Chromium"  
[CR1083797]: https://crbug.com/1083797 "Красивая печать, нарушенная для ненульского | Ошибки Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удаление FMP-| Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и воспроизведения синтетических сетевых запросов | Ошибки Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интеграция веб-хинта в devTools | Ошибки Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработчика] всплывающие окантовки виджетов слишком узкие | Ошибки Chromium"  
[CR897944]: https://crbug.com/897944 "Перетаскиваемые панели | Ошибки Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема — MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование теневых doM-| MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектная модель CSS (CSSOM) | Проекты редактора рабочей группы W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Поля частных классов — общедоступные и частные | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэшинг кода для разработчиков JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Nullish coalescing | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Необязательный | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты таблицы стилей| CG веб-инкубатора"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Веб-сайт, который мы хотим"  

> [!NOTE]
> <span data-ttu-id="3493d-319">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3493d-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3493d-320">Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/06/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="3493d-320">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3493d-322">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3493d-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
