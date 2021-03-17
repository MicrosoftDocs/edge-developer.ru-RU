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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a><span data-ttu-id="49a90-104">Отладка фоновых служб с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49a90-104">Debug Background Services with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="49a90-105">Раздел **Справочные** службы Microsoft Edge DevTools — это коллекция средств для API JavaScript, которая позволяет веб-сайту отправлять и получать обновления, даже если пользователь не имеет своего веб-сайта открытым.</span><span class="sxs-lookup"><span data-stu-id="49a90-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="49a90-106">Фоновая служба функционально похожа на [фоновый процесс][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="49a90-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="49a90-107">Microsoft Edge DevTools считает каждый из следующих API фоновой службой:</span><span class="sxs-lookup"><span data-stu-id="49a90-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="49a90-108">Фоновое извлечение</span><span class="sxs-lookup"><span data-stu-id="49a90-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="49a90-109">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="49a90-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="49a90-110">Notifications</span><span class="sxs-lookup"><span data-stu-id="49a90-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="49a90-111">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="49a90-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="49a90-112">Microsoft Edge DevTools может журнал фоновых событий службы в течение 3 дней, даже если DevTools не открыт.</span><span class="sxs-lookup"><span data-stu-id="49a90-112">Microsoft Edge DevTools may log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="49a90-113">Журнал событий фоновой службы может помочь вам убедиться, что события отправляются и получаются как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="49a90-113">The background service events log may help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="49a90-114">Вы также можете проверить сведения о каждом событии.</span><span class="sxs-lookup"><span data-stu-id="49a90-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="49a90-116">Области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="49a90-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <a name="background-fetch"></a><span data-ttu-id="49a90-117">Фоновое извлечение</span><span class="sxs-lookup"><span data-stu-id="49a90-117">Background Fetch</span></span>  

<span data-ttu-id="49a90-118">API **background Fetch** позволяет \*\*\*\* работнику службы надежно загружать большие ресурсы, например фильмы или подкасты, в качестве фоновой службы.</span><span class="sxs-lookup"><span data-stu-id="49a90-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="49a90-119">Чтобы войти событие Background Fetch в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="49a90-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="49a90-120">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="49a90-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="49a90-121">Откройте **средство приложения.**</span><span class="sxs-lookup"><span data-stu-id="49a90-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="49a90-122">Откройте панель **Фоновое извлечение.**</span><span class="sxs-lookup"><span data-stu-id="49a90-122">Open the **Background Fetch** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Панель "Фоновое извлечение"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="49a90-124">Панель **"Фоновое извлечение"**</span><span class="sxs-lookup"><span data-stu-id="49a90-124">The **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-125">Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="49a90-125">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="49a90-126">После запуска некоторых действий "Фоновое извлечение" DevTools записывает события в таблицу.</span><span class="sxs-lookup"><span data-stu-id="49a90-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Журнал событий в панели Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="49a90-128">Журнал событий в панели **Фоновое извлечение**</span><span class="sxs-lookup"><span data-stu-id="49a90-128">A log of events in the **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-129">Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="49a90-129">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области Фоновое извлечение" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="49a90-131">Просмотр сведений о событии в области **Фоновое извлечение**</span><span class="sxs-lookup"><span data-stu-id="49a90-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <a name="background-sync"></a><span data-ttu-id="49a90-132">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="49a90-132">Background Sync</span></span>  

<span data-ttu-id="49a90-133">API **синхронизации** фона позволяет \*\*\*\* работнику автономной службы отправлять данные на сервер после повторного подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="49a90-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="49a90-134">Журнал событий фоновой синхронизации в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="49a90-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="49a90-135">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="49a90-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="49a90-136">Откройте **средство приложения.**</span><span class="sxs-lookup"><span data-stu-id="49a90-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="49a90-137">Откройте области **фоновой синхронизации.**</span><span class="sxs-lookup"><span data-stu-id="49a90-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="49a90-139">Области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="49a90-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-140">Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="49a90-140">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="49a90-141">После запуска некоторых действий фоновой синхронизации DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="49a90-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Журнал событий в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="49a90-143">Журнал событий в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="49a90-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-144">Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="49a90-144">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="49a90-146">Просмотр сведений о событии в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="49a90-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <a name="notifications"></a><span data-ttu-id="49a90-147">Notifications</span><span class="sxs-lookup"><span data-stu-id="49a90-147">Notifications</span></span>  

<span data-ttu-id="49a90-148">После того **как сотрудник службы** получил [push-сообщение][MDNPush] с сервера, сотрудник службы использует [API][MDNNotifications] уведомлений для отображения данных пользователю.</span><span class="sxs-lookup"><span data-stu-id="49a90-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="49a90-149">Чтобы войти уведомления в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="49a90-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="49a90-150">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="49a90-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="49a90-151">Откройте **средство приложения.**</span><span class="sxs-lookup"><span data-stu-id="49a90-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="49a90-152">Откройте \*\*\*\* области Уведомлений.</span><span class="sxs-lookup"><span data-stu-id="49a90-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Области уведомлений" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="49a90-154">Области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="49a90-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-155">Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="49a90-155">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
   <span data-ttu-id="49a90-156">После запуска некоторых действий Notifications DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="49a90-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Журнал событий в области Уведомлений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="49a90-158">Журнал событий в области **Уведомлений**</span><span class="sxs-lookup"><span data-stu-id="49a90-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-159">Выберите событие, чтобы просмотреть его сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="49a90-159">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области Уведомлений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="49a90-161">Просмотр сведений о событии в области **Уведомлений**</span><span class="sxs-lookup"><span data-stu-id="49a90-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <a name="push-messages"></a><span data-ttu-id="49a90-162">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="49a90-162">Push Messages</span></span>  

<span data-ttu-id="49a90-163">Чтобы отобразить push-уведомление \*\*\*\* для пользователя, работник службы должен сначала использовать [API push-сообщения][MDNPush] для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="49a90-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="49a90-164">Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений.][MDNNotifications]</span><span class="sxs-lookup"><span data-stu-id="49a90-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="49a90-165">Журнал Push-сообщений в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="49a90-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="49a90-166">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="49a90-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="49a90-167">Откройте **средство приложения.**</span><span class="sxs-lookup"><span data-stu-id="49a90-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="49a90-168">Откройте панель **push-сообщений.**</span><span class="sxs-lookup"><span data-stu-id="49a90-168">Open the **Push Messaging** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Откройте области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="49a90-170">Откройте области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="49a90-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-171">Выберите **запись** \. ![ Запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="49a90-171">Choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  
    <span data-ttu-id="49a90-172">После запуска некоторых действий Push Message DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="49a90-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Журнал событий в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="49a90-174">Журнал событий в области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="49a90-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49a90-175">Выберите событие, чтобы просмотреть сведения в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="49a90-175">Choose an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="49a90-177">Просмотр сведений о событии в области **push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="49a90-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="49a90-178">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49a90-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="49a90-183">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49a90-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49a90-184">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="49a90-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="49a90-186">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49a90-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
