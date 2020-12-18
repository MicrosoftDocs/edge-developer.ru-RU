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
# Просмотр и отлагивание сведений об игроках мультимедиа  

Используйте панель **мультимедиа** в Microsoft Edge DevTools для просмотра информации и отладки мультимедиа-плееров на вкладке браузера.  

## Открытие панели "Мультимедиа"  

Панель **мультимедиа** — это основное место в DevTools для проверки мультимедиа-плеер веб-страницы.

1.  [Откройте DevTools.][DevtoolsGuideChromiumOpen]  
1.  Чтобы открыть панель **"Мультимедиа",** выберите "Настройка и **управление средствами DevTools** `...`  >  **More".**  >  ****  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Панель мультимедиа" lightbox="../media/media-panel-empty.msft.png":::
       **Панель мультимедиа**  
    :::image-end:::  
    
## Просмотр сведений об игроках мультимедиа  

1.  Перейдите на веб-страницу с мультимедиа-плеером, например на следующей веб-странице.  
    
    [Максимальное повышение производительности с помощью средств разработчика edge][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  В меню **"Игроки"** отображается медиаплеер.  
1.  Выберите игрока.  На **вкладке "Свойства"** отображаются свойства мультимедиа-плеер.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Свойства мультимедиа" lightbox="../media/media-panel-view.msft.png":::
       Свойства мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть все события мультимедиа-игрока, выберите вкладку **"События".**  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="События мультимедиа" lightbox="../media/media-panel-events.msft.png":::
       События мультимедиа  
    :::image-end:::  
    
1.  Чтобы просмотреть журналы сообщений для мультимедиа-игрока, выберите вкладку **"Сообщения".**  Вы можете фильтровать сообщения по уровню журнала или строке.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Сообщения мультимедиа" lightbox="../media/media-panel-messages.msft.png":::
       Сообщения мультимедиа  
    :::image-end:::  
    
1.  На **вкладке "Временная** шкала" отображается состояние воспроизведения мультимедиа и буфера.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Временная шкала мультимедиа" lightbox="../media/media-panel-timeline.msft.png":::
       Временная шкала мультимедиа  
    :::image-end:::  
    
### Удаленная отладка  

Просмотр сведений об игроках мультимедиа на устройстве с Android с компьютера с Windows или macOS.  

1.  Чтобы настроить удаленную отладку, перейдите к ссылке "Начало работы с [удаленной отладой устройств с Android".][DevtoolsGuideChromiumRemoteDebuggingIndex]  
1.  Удаленное просмотр сведений об игроках мультимедиа.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Скрытие и показ мультимедиа-плееров  

Иногда на веб-странице можно запустить несколько мультимедиа-плееров или использовать одну вкладку браузера для просмотра разных веб-страниц, каждый из которых имеет мультимедиа-плеер.

Вы можете скрыть \(или показать\) каждый мультимедиа-плеер для упростить отладку.  

1.  Перейдите на несколько разных веб-страниц видео с помощью одной вкладки браузера.  
1.  Чтобы скрыть мультимедиа-плеер, выполните одно из следующих действий.  
    *   Чтобы скрыть один мультимедиа-плеер, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Скрыть игрока".**  
    *   Чтобы скрыть всех других игроков мультимедиа, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Скрыть все остальные".**  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Скрытие мультимедиа-плееров" lightbox="../media/media-panel-hide-show.msft.png":::
       Скрытие мультимедиа-плееров  
    :::image-end:::  
    
## Экспорт сведений о мультимедиа-плеере  

1.  Чтобы скачать сведения о мультимедиа-игроке в качестве JSON-файла, наведите курсор на мультимедиа-плеер, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить **данные игрока".**  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Экспорт сведений о мультимедиа" lightbox="../media/media-panel-save.msft.png":::
       Экспорт сведений о мультимедиа  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge (Chromium) DevTools | Документы Майкрософт"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Начало работы с удаленной отладой устройств с Android | Документы Майкрософт"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Максимальное увеличение производительности с помощью средств разработчика edge | Видео Bing"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/media-panel/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

