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

# <span data-ttu-id="6f579-104">Отладка фоновых служб с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6f579-104">Debug Background Services With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="6f579-105">Раздел **фоновых** служб Microsoft Edge DevTools — это набор средств для API JavaScript, позволяющих веб-сайту отправлять и получать обновления, даже если у пользователя нет открытого веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="6f579-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="6f579-106">Фоновая служба функционально похожа на [фоновый процесс][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="6f579-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="6f579-107">Microsoft Edge DevTools считает каждый из следующих API фоновой службой:</span><span class="sxs-lookup"><span data-stu-id="6f579-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="6f579-108">Фоновое извлечение</span><span class="sxs-lookup"><span data-stu-id="6f579-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="6f579-109">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="6f579-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="6f579-110">Уведомления</span><span class="sxs-lookup"><span data-stu-id="6f579-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="6f579-111">Push Messages</span><span class="sxs-lookup"><span data-stu-id="6f579-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="6f579-112">Microsoft Edge DevTools может занося в журнал события фоновой службы в течение 3 дней, даже если DevTools не открыт.</span><span class="sxs-lookup"><span data-stu-id="6f579-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="6f579-113">Это поможет убедиться, что события отправляются и получаются ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="6f579-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="6f579-114">Вы также можете проверить сведения о каждом событии.</span><span class="sxs-lookup"><span data-stu-id="6f579-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="The Push Messaging pane" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="6f579-116">The **Push Messaging** pane</span><span class="sxs-lookup"><span data-stu-id="6f579-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="6f579-117">Фоновое извлечение</span><span class="sxs-lookup"><span data-stu-id="6f579-117">Background Fetch</span></span>  

<span data-ttu-id="6f579-118">API **фонового получения** \*\*\*\* позволяет сотруднику службы надежно загружать большие ресурсы, такие как фильмы или подкасты, в качестве фоновой службы.</span><span class="sxs-lookup"><span data-stu-id="6f579-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="6f579-119">Запись события Background Fetch в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="6f579-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="6f579-120">[Откройте DevTools.][OpenDevTools]</span><span class="sxs-lookup"><span data-stu-id="6f579-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6f579-121">Откройте средство **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="6f579-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="6f579-122">Откройте **фоновую области получения.**</span><span class="sxs-lookup"><span data-stu-id="6f579-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Фоновая области получения" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="6f579-124">**Фоновая области получения**</span><span class="sxs-lookup"><span data-stu-id="6f579-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-125">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6f579-125">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="6f579-126">После запуска фонового получения событий DevTools записывает события в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f579-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Журнал событий в области "Фоновое извлечение"" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="6f579-128">Журнал событий в области **"Фоновое извлечение"**</span><span class="sxs-lookup"><span data-stu-id="6f579-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-129">Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="6f579-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области "Фоновое извлечение"" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="6f579-131">Просмотр сведений о событии в области **"Фоновое извлечение"**</span><span class="sxs-lookup"><span data-stu-id="6f579-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6f579-132">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="6f579-132">Background Sync</span></span>  

<span data-ttu-id="6f579-133">API **фоновой** синхронизации позволяет \*\*\*\* автономному сотруднику службы отправлять данные на сервер после повторного подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="6f579-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="6f579-134">Запись событий фоновой синхронизации в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="6f579-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="6f579-135">[Откройте DevTools.][OpenDevTools]</span><span class="sxs-lookup"><span data-stu-id="6f579-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6f579-136">Откройте средство **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="6f579-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="6f579-137">Откройте **фоновую области** синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6f579-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Фоновая синхронизация" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="6f579-139">**Фоновая синхронизация**</span><span class="sxs-lookup"><span data-stu-id="6f579-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-140">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6f579-140">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="6f579-141">После запуска некоторых действий фоновой синхронизации DevTools записывает события в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f579-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Журнал событий в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="6f579-143">Журнал событий в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="6f579-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-144">Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="6f579-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="6f579-146">Просмотр сведений о событии в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="6f579-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6f579-147">Уведомления</span><span class="sxs-lookup"><span data-stu-id="6f579-147">Notifications</span></span>  

<span data-ttu-id="6f579-148">После того как сотрудник [][MDNPush] **службы** получит push-сообщение с сервера, он использует [API][MDNNotifications] уведомлений для отображения данных пользователю.</span><span class="sxs-lookup"><span data-stu-id="6f579-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="6f579-149">Для регистрации уведомлений в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="6f579-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="6f579-150">[Откройте DevTools.][OpenDevTools]</span><span class="sxs-lookup"><span data-stu-id="6f579-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6f579-151">Откройте средство **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="6f579-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="6f579-152">Откройте области **уведомлений.**</span><span class="sxs-lookup"><span data-stu-id="6f579-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="The Notifications pane" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="6f579-154">The **Notifications** pane</span><span class="sxs-lookup"><span data-stu-id="6f579-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-155">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6f579-155">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="6f579-156">После запуска некоторых действий notifications DevTools записывает события в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f579-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Журнал событий в области уведомлений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="6f579-158">Журнал событий в **области** уведомлений</span><span class="sxs-lookup"><span data-stu-id="6f579-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-159">Щелкните событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="6f579-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области уведомлений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="6f579-161">Просмотр сведений о событии в области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="6f579-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6f579-162">Push Messages</span><span class="sxs-lookup"><span data-stu-id="6f579-162">Push Messages</span></span>  

<span data-ttu-id="6f579-163">Чтобы отобразить push-уведомление \*\*\*\* для пользователя, сотрудник службы должен сначала использовать [API push-сообщений][MDNPush] для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="6f579-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="6f579-164">Когда рабочий работник службы готов отобразить уведомление, он использует [API уведомлений.][MDNNotifications]</span><span class="sxs-lookup"><span data-stu-id="6f579-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="6f579-165">Запись push-сообщений в журнал в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="6f579-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="6f579-166">[Откройте DevTools.][OpenDevTools]</span><span class="sxs-lookup"><span data-stu-id="6f579-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6f579-167">Откройте средство **"Приложение".**</span><span class="sxs-lookup"><span data-stu-id="6f579-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="6f579-168">Откройте области **push-сообщений.**</span><span class="sxs-lookup"><span data-stu-id="6f579-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Открытие области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="6f579-170">Открытие области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="6f579-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-171">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6f579-171">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="6f579-172">После запуска некоторых действий Push Message DevTools записывает события в таблицу.</span><span class="sxs-lookup"><span data-stu-id="6f579-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Журнал событий в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="6f579-174">Журнал событий в области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="6f579-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6f579-175">Щелкните событие, чтобы просмотреть сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="6f579-175">Click an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="6f579-177">Просмотр сведений о событии в области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="6f579-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="6f579-178">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6f579-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="6f579-183">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f579-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6f579-184">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6f579-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6f579-186">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6f579-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
