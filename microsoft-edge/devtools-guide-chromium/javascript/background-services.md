---
description: Отладка фонового получения, фоновой синхронизации, уведомлений и push-уведомлений с помощью Microsoft Edge DevTools.
title: Отладка фоновых служб с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: df832ed2f56faf6412fd42bc080d8af7705d26d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230679"
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

# Отладка фоновых служб с помощью Microsoft Edge DevTools  

Раздел **фоновых** служб Microsoft Edge DevTools — это набор средств для API JavaScript, позволяющих веб-сайту отправлять и получать обновления, даже если у пользователя нет открытого веб-сайта.  
Фоновая служба функционально похожа на [фоновый процесс][WikiBackgroundProcess].  
Microsoft Edge DevTools считает каждый из следующих API фоновой службой:  

*   [Фоновое извлечение](#background-fetch)  
*   [Фоновая синхронизация](#background-sync)  
*   [Уведомления](#notifications)  
*   [Push Messages](#push-messages)  
    
Microsoft Edge DevTools может занося в журнал события фоновой службы в течение 3 дней, даже если DevTools не открыт.  
Это поможет убедиться, что события отправляются и получаются ожидаемым образом.  Вы также можете проверить сведения о каждом событии.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="The Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   The **Push Messaging** pane  
:::image-end:::  

## Фоновое извлечение  

API **фонового получения** **** позволяет сотруднику службы надежно загружать большие ресурсы, такие как фильмы или подкасты, в качестве фоновой службы.  Запись события Background Fetch в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background fetch api section when available -->  

1.  [Откройте DevTools.][OpenDevTools]  
1.  Откройте средство **"Приложение".**  
1.  Откройте **фоновую области получения.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Фоновая области получения" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       **Фоновая области получения**  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ][ImageRecordIcon] \).  
   После запуска фонового получения событий DevTools записывает события в таблицу.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Журнал событий в области Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Журнал событий в области **"Фоновое извлечение"**  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Просмотр сведений о событии в области **"Фоновое извлечение"**  
    :::image-end:::  
    
## Фоновая синхронизация  

API **фоновой** синхронизации позволяет **** автономному сотруднику службы отправлять данные на сервер после повторного подключения к Интернету.  Запись событий фоновой синхронизации в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background sync api section when available -->  

1.  [Откройте DevTools.][OpenDevTools]  
1.  Откройте средство **"Приложение".**  
1.  Откройте **фоновую области** синхронизации.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Фоновая синхронизация" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       **Фоновая синхронизация**  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ][ImageRecordIcon] \).  
   После запуска некоторых действий фоновой синхронизации DevTools записывает события в таблицу.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Журнал событий в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Журнал событий в области **фоновой синхронизации**  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Просмотр сведений о событии в области **фоновой синхронизации**  
    :::image-end:::  
    
## Уведомления  

После того как сотрудник [][MDNPush] **службы** получит push-сообщение с сервера, он использует [API][MDNNotifications] уведомлений для отображения данных пользователю.  Для регистрации уведомлений в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools.][OpenDevTools]  
1.  Откройте средство **"Приложение".**  
1.  Откройте области **уведомлений.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="The Notifications pane" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       The **Notifications** pane  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ][ImageRecordIcon] \).  
   После запуска некоторых действий notifications DevTools записывает события в таблицу.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Журнал событий в области уведомлений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Журнал событий в **области** уведомлений  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области уведомлений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Просмотр сведений о событии в области **уведомлений**  
    :::image-end:::  
    
## Push Messages  

Чтобы отобразить push-уведомление **** для пользователя, сотрудник службы должен сначала использовать [API push-сообщений][MDNPush] для получения данных с сервера.  Когда рабочий работник службы готов отобразить уведомление, он использует [API уведомлений.][MDNNotifications]  Запись push-сообщений в журнал в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools.][OpenDevTools]  
1.  Откройте средство **"Приложение".**  
1.  Откройте области **push-сообщений.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Открытие области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Открытие области **push-сообщений**  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ][ImageRecordIcon] \).  
    После запуска некоторых действий Push Message DevTools записывает события в таблицу.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Журнал событий в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Журнал событий в области **push-сообщений**  
    :::image-end:::  
    
1.  Щелкните событие, чтобы просмотреть сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Просмотр сведений о событии в области **push-сообщений**  
    :::image-end:::  
    
## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Откройте инструменты разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Фоновый процесс — Викимедиа"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
