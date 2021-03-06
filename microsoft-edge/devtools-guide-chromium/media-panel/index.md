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

# <a name="view-and-debug-media-players-information"></a>Просмотр и отлаговка сведений о медиа-игроках  

Используйте средство **Мультимедиа** в Microsoft Edge DevTools для просмотра информации и отладки медиа-игроков на вкладке браузера.  

## <a name="open-the-media-tool"></a>Откройте средство Мультимедиа  

Средство **Мультимедиа** — это основное место в DevTools для проверки медиа-плеер веб-страницы.

1.  [Откройте DevTools][DevtoolsGuideChromiumOpen].  
1.  Чтобы открыть панель **Мультимедиа,** выберите Настройка и **управление средствами DevTools** `...`  >  **Дополнительные**  >  **средства Мультимедиа.**  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       **Панель мультимедиа**  
    :::image-end:::  
    
## <a name="view-media-players-information"></a>Просмотр сведений о медиа-игроках  

1.  Перейдите на веб-страницу с медиа-плеером, например на следующей странице.  
    
    [Максимальное повышение производительности с помощью средств разработки edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  В меню **Players** отображается медиаплеер.  
1.  Выберите игрока.  Панель **свойств** отображает свойства медиаплеер.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Свойства мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       Свойства мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть все события медиа-плеер, выберите панель **События.**  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="События мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       События мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть журналы сообщений мультимедиа-плеер, выберите панель **Сообщений.**  Вы можете фильтровать сообщения по уровню журнала или строке.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Сообщения мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       Сообщения мультимедиа  
    :::image-end:::  
    
1.  На панели **Timeline** воспроизведение мультимедиа и состояние буфера отображаются в прямом эфире.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Временная шкала мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       Временная шкала мультимедиа  
    :::image-end:::  
    
### <a name="remote-debugging"></a>Удаленная отладка  

Просмотр сведений о медиаигредах на устройстве Android с компьютера Windows или macOS.  

1.  Чтобы настроить удаленную отладку, перейдите к началу работы [с устройствами удаленной][DevtoolsGuideChromiumRemoteDebuggingIndex]отладки Android.  
1.  Просмотр сведений об игроках мультимедиа удаленно.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a>Скрыть и показать медиа-плеер  

Иногда вы запустите несколько медиа-плеер на веб-странице или используете одну вкладку браузера для просмотра различных веб-страниц, каждый из которых имеет медиа-плеер.

Вы можете скрыть \(или показать\) каждый медиа-плеер для более простого отладки.  

1.  Просмотрите несколько различных веб-страниц видео с помощью одной вкладки браузера.  
1.  Чтобы скрыть медиа-плеер, выполните одно из следующих действий.  
    *   Чтобы скрыть один медиа-плеер, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **hide player**.  
    *   Чтобы скрыть все остальные медиа-игроки, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Скрыть все остальные**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Скрыть медиа-игроки" lightbox="../media/media-panel-hide-show.msft.png":::
       Скрыть медиа-игроки  
    :::image-end:::  
    
## <a name="export-media-player-information"></a>Экспорт сведений о медиа-плеере  

1.  Чтобы скачать сведения о медиа-плеере в качестве файла JSON, наведите курсор на медиа-плеер, откройте контекстное меню \(правой кнопкой мыши\) и выберите **сохранить сведения об игроке**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Экспорт сведений о мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       Экспорт сведений о мультимедиа  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимальное повышение производительности с помощью средств разработки edge | Видео Bing"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/media-panel/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

