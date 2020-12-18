---
description: Используйте панель мультимедиа для просмотра сведений и отлаки мультимедиа-плеер на вкладке браузера.
title: Просмотр и отлагивание сведений об игроках мультимедиа
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e6259cf573b76df7e281527ad30360b8f473a165
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230952"
---
# <span data-ttu-id="1b5a7-104">Просмотр и отлагивание сведений об игроках мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-104">View and debug media players information</span></span>  

<span data-ttu-id="1b5a7-105">Используйте панель **мультимедиа** в Microsoft Edge DevTools для просмотра информации и отладки мультимедиа-плееров на вкладке браузера.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-105">Use the **Media** panel in Microsoft Edge DevTools to view information and debug the media players per browser tab.</span></span>  

## <span data-ttu-id="1b5a7-106">Открытие панели "Мультимедиа"</span><span class="sxs-lookup"><span data-stu-id="1b5a7-106">Open the Media panel</span></span>  

<span data-ttu-id="1b5a7-107">Панель **мультимедиа** — это основное место в DevTools для проверки мультимедиа-плеер веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-107">The **Media** panel is the main place in DevTools for inspecting the media player of a webpage.</span></span>

1.  <span data-ttu-id="1b5a7-108">[Откройте DevTools.][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="1b5a7-108">[Open DevTools][DevtoolsGuideChromiumOpen].</span></span>  
1.  <span data-ttu-id="1b5a7-109">Чтобы открыть панель **"Мультимедиа",** выберите "Настройка и **управление средствами DevTools** `...`  >  **More".**  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1b5a7-109">To open the **Media** panel, choose **Customize and control DevTools** `...` > **More tools** > **Media**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       <span data-ttu-id="1b5a7-111">**Панель мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1b5a7-111">**Media** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1b5a7-112">Просмотр сведений об игроках мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-112">View media players information</span></span>  

1.  <span data-ttu-id="1b5a7-113">Перейдите на веб-страницу с мультимедиа-плеером, например на следующей веб-странице.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-113">Navigate to a webpage with a media player, such as the following webpage.</span></span>  
    
    [<span data-ttu-id="1b5a7-114">Максимальное повышение производительности с помощью средств разработчика edge</span><span class="sxs-lookup"><span data-stu-id="1b5a7-114">Maximizing productivity with the Edge Developer Tools</span></span>][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  <span data-ttu-id="1b5a7-115">В меню **"Игроки"** отображается медиаплеер.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-115">Under the **Players** menu, a media player is displayed.</span></span>  
1.  <span data-ttu-id="1b5a7-116">Выберите игрока.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-116">Select the player.</span></span>  <span data-ttu-id="1b5a7-117">На **вкладке "Свойства"** отображаются свойства мультимедиа-плеер.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-117">The **Properties** tab displays the properties of the media player.</span></span>  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Свойства мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       <span data-ttu-id="1b5a7-119">Свойства мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-119">Media properties</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1b5a7-120">Чтобы просмотреть все события мультимедиа-игрока, выберите вкладку **"События".**</span><span class="sxs-lookup"><span data-stu-id="1b5a7-120">To view all the media player events, choose the **Events** tab.</span></span>  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="События мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       <span data-ttu-id="1b5a7-122">События мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-122">Media events</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1b5a7-123">Чтобы просмотреть журналы сообщений для мультимедиа-игрока, выберите вкладку **"Сообщения".**  Вы можете фильтровать сообщения по уровню журнала или строке.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-123">To view the media player message logs, choose the **Messages** tab.  You may filter the messages by log level or string.</span></span>  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Сообщения мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       <span data-ttu-id="1b5a7-125">Сообщения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-125">Media messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1b5a7-126">На **вкладке "Временная** шкала" отображается состояние воспроизведения мультимедиа и буфера.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-126">On the **Timeline** tab, the media playback and buffer status is displayed live.</span></span>  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Временная шкала мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       <span data-ttu-id="1b5a7-128">Временная шкала мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-128">Media timeline</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="1b5a7-129">Удаленная отладка</span><span class="sxs-lookup"><span data-stu-id="1b5a7-129">Remote debugging</span></span>  

<span data-ttu-id="1b5a7-130">Просмотр сведений об игроках мультимедиа на устройстве с Android с компьютера с Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-130">View the media players information on an Android device from your Windows or macOS computer.</span></span>  

1.  <span data-ttu-id="1b5a7-131">Чтобы настроить удаленную отладку, перейдите к ссылке "Начало работы с [удаленной отладой устройств с Android".][DevtoolsGuideChromiumRemoteDebuggingIndex]</span><span class="sxs-lookup"><span data-stu-id="1b5a7-131">To set up remote debugging, navigate to [Get started with remote debugging Android devices][DevtoolsGuideChromiumRemoteDebuggingIndex].</span></span>  
1.  <span data-ttu-id="1b5a7-132">Удаленное просмотр сведений об игроках мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-132">View the media players information remotely.</span></span>  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <span data-ttu-id="1b5a7-133">Скрытие и показ мультимедиа-плееров</span><span class="sxs-lookup"><span data-stu-id="1b5a7-133">Hide and show media players</span></span>  

<span data-ttu-id="1b5a7-134">Иногда на веб-странице можно запустить несколько мультимедиа-плееров или использовать одну вкладку браузера для просмотра разных веб-страниц, каждый из которых имеет мультимедиа-плеер.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-134">Sometimes you run more than one media player on a webpage, or use the same browser tab to browse different webpages, each with media players.</span></span>

<span data-ttu-id="1b5a7-135">Вы можете скрыть \(или показать\) каждый мультимедиа-плеер для упростить отладку.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-135">You may choose to hide \(or show\) each media player for an easier debugging experience.</span></span>  

1.  <span data-ttu-id="1b5a7-136">Перейдите на несколько разных веб-страниц видео с помощью одной вкладки браузера.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-136">Browse to several different video webpages using the same browser tab.</span></span>  
1.  <span data-ttu-id="1b5a7-137">Чтобы скрыть мультимедиа-плеер, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="1b5a7-137">To hide media players, complete one of the following actions.</span></span>  
    *   <span data-ttu-id="1b5a7-138">Чтобы скрыть один мультимедиа-плеер, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Скрыть игрока".**</span><span class="sxs-lookup"><span data-stu-id="1b5a7-138">To hide one media player, hover on a media player, open the contextual menu \(right-click\), and choose **Hide player**.</span></span>  
    *   <span data-ttu-id="1b5a7-139">Чтобы скрыть всех других игроков мультимедиа, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Скрыть все остальные".**</span><span class="sxs-lookup"><span data-stu-id="1b5a7-139">To hide all of the other media players, hover on a media player, open the contextual menu \(right-click\), and choose **Hide all others**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Скрытие мультимедиа-плееров" lightbox="../media/media-panel-hide-show.msft.png":::
       <span data-ttu-id="1b5a7-141">Скрытие мультимедиа-плееров</span><span class="sxs-lookup"><span data-stu-id="1b5a7-141">Hide media players</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1b5a7-142">Экспорт сведений о мультимедиа-плеере</span><span class="sxs-lookup"><span data-stu-id="1b5a7-142">Export media player information</span></span>  

1.  <span data-ttu-id="1b5a7-143">Чтобы скачать сведения о мультимедиа-игроке в качестве JSON-файла, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить **данные игрока".**</span><span class="sxs-lookup"><span data-stu-id="1b5a7-143">To download the media player info as a JSON file, hover on a media player, open the contextual menu \(right-click\), and choose **Save player info**.</span></span>  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Экспорт сведений о мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       <span data-ttu-id="1b5a7-145">Экспорт сведений о мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1b5a7-145">Export media information</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1b5a7-146">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b5a7-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленной отладой устройств с Android | Документы Майкрософт"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимальное увеличение производительности с помощью средств разработчика edge | Видео Bing"  

> [!NOTE]
> <span data-ttu-id="1b5a7-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1b5a7-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1b5a7-151">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/media-panel/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="1b5a7-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1b5a7-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1b5a7-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

