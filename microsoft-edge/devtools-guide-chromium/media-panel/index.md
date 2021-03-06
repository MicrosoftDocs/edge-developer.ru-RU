---
description: Используйте средство Мультимедиа для просмотра информации и отлаговки медиа-игроков на вкладке браузера.
title: Просмотр и отлаговка сведений о медиа-игроках
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7680faa13f65a2ea6f0a8b085316b5ed67bfdaba
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398408"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="view-and-debug-media-players-information"></a><span data-ttu-id="80a4d-104">Просмотр и отлаговка сведений о медиа-игроках</span><span class="sxs-lookup"><span data-stu-id="80a4d-104">View and debug media players information</span></span>  

<span data-ttu-id="80a4d-105">Используйте средство **Мультимедиа** в Microsoft Edge DevTools для просмотра информации и отладки медиа-игроков на вкладке браузера.</span><span class="sxs-lookup"><span data-stu-id="80a4d-105">Use the **Media** tool in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <a name="open-the-media-tool"></a><span data-ttu-id="80a4d-106">Откройте средство Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-106">Open the Media tool</span></span>  

<span data-ttu-id="80a4d-107">Средство **Мультимедиа** — это основное место в DevTools для проверки медиа-плеер веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="80a4d-107">The **Media** tool is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="80a4d-108">[Откройте DevTools][DevtoolsGuideChromiumOpen].</span><span class="sxs-lookup"><span data-stu-id="80a4d-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="80a4d-109">Чтобы открыть панель **Мультимедиа,** выберите Настройка и **управление средствами DevTools** `...`  >  **Дополнительные**  >  **средства Мультимедиа.**</span><span class="sxs-lookup"><span data-stu-id="80a4d-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="80a4d-111">**Панель мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="80a4d-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <a name="view-media-players-information"></a><span data-ttu-id="80a4d-112">Просмотр сведений о медиа-игроках</span><span class="sxs-lookup"><span data-stu-id="80a4d-112">View media players information</span></span>  

1.  <span data-ttu-id="80a4d-113">Перейдите на веб-страницу с медиа-плеером, например на следующей странице.</span><span class="sxs-lookup"><span data-stu-id="80a4d-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="80a4d-114">Максимальное повышение производительности с помощью средств разработки edge</span><span class="sxs-lookup"><span data-stu-id="80a4d-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="80a4d-115">В меню **Players** отображается медиаплеер.</span><span class="sxs-lookup"><span data-stu-id="80a4d-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="80a4d-116">Выберите игрока.</span><span class="sxs-lookup"><span data-stu-id="80a4d-116">Choose the player.</span></span>  <span data-ttu-id="80a4d-117">Панель **свойств** отображает свойства медиаплеер.</span><span class="sxs-lookup"><span data-stu-id="80a4d-117">The **Properties** panel displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Свойства мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="80a4d-119">Свойства мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="80a4d-120">Чтобы просмотреть все события медиа-плеер, выберите панель **События.**</span><span class="sxs-lookup"><span data-stu-id="80a4d-120">To view all the media player events, choose the **Events** panel.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="События мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="80a4d-122">События мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="80a4d-123">Чтобы просмотреть журналы сообщений мультимедиа-плеер, выберите панель **Сообщений.**</span><span class="sxs-lookup"><span data-stu-id="80a4d-123">To view the media player message logs, choose the **Messages** panel.</span></span>  <span data-ttu-id="80a4d-124">Вы можете фильтровать сообщения по уровню журнала или строке.</span><span class="sxs-lookup"><span data-stu-id="80a4d-124">You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Сообщения мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="80a4d-126">Сообщения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-126">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="80a4d-127">На панели **Timeline** воспроизведение мультимедиа и состояние буфера отображаются в прямом эфире.</span><span class="sxs-lookup"><span data-stu-id="80a4d-127">On the **Timeline** panel, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Временная шкала мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="80a4d-129">Временная шкала мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-129">Media timeline</span></span>  
    :::image-end:::  
    
### <a name="remote-debugging"></a><span data-ttu-id="80a4d-130">Удаленная отладка</span><span class="sxs-lookup"><span data-stu-id="80a4d-130">Remote debugging</span></span>  

<span data-ttu-id="80a4d-131">Просмотр сведений о медиаигредах на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="80a4d-131">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="80a4d-132">Чтобы настроить удаленную отладку, перейдите к началу работы [с устройствами удаленной][DevtoolsGuideChromiumRemoteDebuggingIndex]отладки Android.</span><span class="sxs-lookup"><span data-stu-id="80a4d-132">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="80a4d-133">Просмотр сведений об игроках мультимедиа удаленно.</span><span class="sxs-lookup"><span data-stu-id="80a4d-133">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a><span data-ttu-id="80a4d-134">Скрыть и показать медиа-плеер</span><span class="sxs-lookup"><span data-stu-id="80a4d-134">Hide and show media players</span></span>  

<span data-ttu-id="80a4d-135">Иногда вы запустите несколько медиа-плеер на веб-странице или используете одну вкладку браузера для просмотра различных веб-страниц, каждый из которых имеет медиа-плеер.</span><span class="sxs-lookup"><span data-stu-id="80a4d-135">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="80a4d-136">Вы можете скрыть \(или показать\) каждый медиа-плеер для более простого отладки.</span><span class="sxs-lookup"><span data-stu-id="80a4d-136">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="80a4d-137">Просмотрите несколько различных веб-страниц видео с помощью одной вкладки браузера.</span><span class="sxs-lookup"><span data-stu-id="80a4d-137">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="80a4d-138">Чтобы скрыть медиа-плеер, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="80a4d-138">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="80a4d-139">Чтобы скрыть один медиа-плеер, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **hide player**.</span><span class="sxs-lookup"><span data-stu-id="80a4d-139">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="80a4d-140">Чтобы скрыть все остальные медиа-игроки, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Скрыть все остальные**.</span><span class="sxs-lookup"><span data-stu-id="80a4d-140">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Скрыть медиа-игроки" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="80a4d-142">Скрыть медиа-игроки</span><span class="sxs-lookup"><span data-stu-id="80a4d-142">Hide media players</span></span>  
    :::image-end:::  
    
## <a name="export-media-player-information"></a><span data-ttu-id="80a4d-143">Экспорт сведений о медиа-плеере</span><span class="sxs-lookup"><span data-stu-id="80a4d-143">Export media player information</span></span>  

1.  <span data-ttu-id="80a4d-144">Чтобы скачать сведения о медиа-плеере в качестве файла JSON, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **сохранить сведения об игроке**.</span><span class="sxs-lookup"><span data-stu-id="80a4d-144">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Экспорт сведений о мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="80a4d-146">Экспорт сведений о мультимедиа</span><span class="sxs-lookup"><span data-stu-id="80a4d-146">Export media information</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="80a4d-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="80a4d-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимальное повышение производительности с помощью средств разработки edge | Видео Bing"  

> [!NOTE]
> <span data-ttu-id="80a4d-151">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80a4d-151">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="80a4d-152">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/media-panel/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="80a4d-152">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="80a4d-154">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80a4d-154">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

