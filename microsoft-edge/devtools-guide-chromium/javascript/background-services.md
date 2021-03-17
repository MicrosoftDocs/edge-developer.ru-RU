---
description: Как отладить фоновое извлечение, фоновую синхронизацию, уведомления и push-сообщения с помощью Microsoft Edge DevTools.
title: Отладка фоновых служб с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 15023098c547d31bf46bd387f849b365c13b38f6
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439530"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a>Отладка фоновых служб с помощью Microsoft Edge DevTools  

Раздел **Справочные** службы Microsoft Edge DevTools — это коллекция средств для API JavaScript, которая позволяет веб-сайту отправлять и получать обновления, даже если пользователь не имеет своего веб-сайта открытым.  
Фоновая служба функционально похожа на [фоновый процесс][WikiBackgroundProcess].  
Microsoft Edge DevTools считает каждый из следующих API фоновой службой:  

*   [Фоновое извлечение](#background-fetch)  
*   [Фоновая синхронизация](#background-sync)  
*   [Notifications](#notifications)  
*   [Push-сообщения](#push-messages)  
    
Microsoft Edge DevTools может журнал фоновых событий службы в течение 3 дней, даже если DevTools не открыт.  
Журнал событий фоновой службы может помочь вам убедиться, что события отправляются и получаются как ожидалось.  Вы также можете проверить сведения о каждом событии.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Области **push-сообщений**  
:::image-end:::  

## <a name="background-fetch"></a>Фоновое извлечение  

API **background Fetch** позволяет **** работнику службы надежно загружать большие ресурсы, например фильмы или подкасты, в качестве фоновой службы.  Чтобы войти событие Background Fetch в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background fetch api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте **средство приложения.**  
1.  Откройте панель **Фоновое извлечение.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Панель "Фоновое извлечение"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Панель **"Фоновое извлечение"**  
    :::image-end:::  
    
1.  Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).  
   После запуска некоторых действий "Фоновое извлечение" DevTools записывает события в таблицу.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Журнал событий в панели Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Журнал событий в панели **Фоновое извлечение**  
    :::image-end:::  
    
1.  Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Просмотр сведений о событии в области **Фоновое извлечение**  
    :::image-end:::  
    
## <a name="background-sync"></a>Фоновая синхронизация  

API **синхронизации** фона позволяет **** работнику автономной службы отправлять данные на сервер после повторного подключения к Интернету.  Журнал событий фоновой синхронизации в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background sync api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте **средство приложения.**  
1.  Откройте области **фоновой синхронизации.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Области **фоновой синхронизации**  
    :::image-end:::  
    
1.  Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).  
   После запуска некоторых действий фоновой синхронизации DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Журнал событий в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Журнал событий в области **фоновой синхронизации**  
    :::image-end:::  
    
1.  Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Просмотр сведений о событии в области **фоновой синхронизации**  
    :::image-end:::  
    
## <a name="notifications"></a>Notifications  

После того **как сотрудник службы** получил [push-сообщение][MDNPush] с сервера, сотрудник службы использует [API][MDNNotifications] уведомлений для отображения данных пользователю.  Чтобы войти уведомления в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте **средство приложения.**  
1.  Откройте **** области Уведомлений.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Области уведомлений" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Области **уведомлений**  
    :::image-end:::  
    
1.  Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).  
   После запуска некоторых действий Notifications DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Журнал событий в области Уведомлений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Журнал событий в области **Уведомлений**  
    :::image-end:::  
    
1.  Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области Уведомлений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Просмотр сведений о событии в области **Уведомлений**  
    :::image-end:::  
    
## <a name="push-messages"></a>Push-сообщения  

Чтобы отобразить push-уведомление **** для пользователя, работник службы должен сначала использовать [API push-сообщения][MDNPush] для получения данных с сервера.  Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений.][MDNNotifications]  Журнал Push-сообщений в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте **средство приложения.**  
1.  Откройте панель **push-сообщений.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Откройте области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Откройте области **push-сообщений**  
    :::image-end:::  
    
1.  Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).  
    После запуска некоторых действий Push Message DevTools регистрирует события в таблице.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Журнал событий в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Журнал событий в области **push-сообщений**  
    :::image-end:::  
    
1.  Выберите событие, чтобы просмотреть сведения в пространстве под таблицей.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Просмотр сведений о событии в области **push-сообщений**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Откройте средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "Фоновый процесс — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
