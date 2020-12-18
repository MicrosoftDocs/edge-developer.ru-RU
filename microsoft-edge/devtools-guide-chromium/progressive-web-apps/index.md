---
description: Используйте панель приложений для проверки, изменения и отлаки манифестов веб-приложения, сотрудников служб и рабочих кэшей служб.
title: Debug Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 79edf4b04c85db33e89d18ec1832138a61f4f884
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235152"
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

# <span data-ttu-id="76cc1-104">Debug Progressive Web Apps</span><span class="sxs-lookup"><span data-stu-id="76cc1-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="76cc1-105">Используйте панель **приложений** для проверки, изменения и отлажки манифестов веб-приложений, сотрудников служб и рабочих кэшей служб.</span><span class="sxs-lookup"><span data-stu-id="76cc1-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="76cc1-106">В этом руководстве обсуждаются только функции прогрессивного веб-приложения на панели **приложений.**</span><span class="sxs-lookup"><span data-stu-id="76cc1-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="76cc1-107">Сводка</span><span class="sxs-lookup"><span data-stu-id="76cc1-107">Summary</span></span>  

*   <span data-ttu-id="76cc1-108">С помощью **области манифеста** проверьте манифест веб-приложения и активируете события Add to Homescreen.</span><span class="sxs-lookup"><span data-stu-id="76cc1-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="76cc1-109">С помощью области **"Сотрудники** службы" можно выполнять целый ряд задач, связанных с работой службы, таких как прекращение регистрации или обновление службы, эмуляция событий push-данных, отключение или остановка работы службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="76cc1-110">Просмотр рабочего кэша службы из области **хранения** кэша.</span><span class="sxs-lookup"><span data-stu-id="76cc1-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="76cc1-111">Отрегистрировать сотрудников службы и очистить все хранилища и \*\*\*\* кэши одним нажатием кнопки в области очистки хранилища.</span><span class="sxs-lookup"><span data-stu-id="76cc1-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="76cc1-112">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="76cc1-112">Web app manifest</span></span>  

<span data-ttu-id="76cc1-113">Если вы хотите, чтобы пользователи могли добавлять приложение на свои домашние экраны для мобильных устройств, вам потребуется манифест веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="76cc1-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="76cc1-114">Манифест определяет, как приложение отображается на домашнем экране, куда направить пользователя при запуске с домашнего экрана и как оно выглядит при запуске.</span><span class="sxs-lookup"><span data-stu-id="76cc1-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="76cc1-115">После того как манифест настроен, вы \*\*\*\* можете проверить \*\*\*\* его с помощью области манифеста панели приложений.</span><span class="sxs-lookup"><span data-stu-id="76cc1-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="The Manifest Pane" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="76cc1-117">The **Manifest** Pane</span><span class="sxs-lookup"><span data-stu-id="76cc1-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="76cc1-118">Чтобы посмотреть на источник манифеста, щелкните ссылку **под** меткой манифеста приложения \( на `https://airhorner.com/manifest.json` предыдущем рисунке\).</span><span class="sxs-lookup"><span data-stu-id="76cc1-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="76cc1-119">В **разделах** "Удостоверение" и **"Презентация"** просто отображаются поля из источника манифеста на более удобном для пользователя дисплее.</span><span class="sxs-lookup"><span data-stu-id="76cc1-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="76cc1-120">В **разделе "Значки"** отображаются все указанные вами значки.</span><span class="sxs-lookup"><span data-stu-id="76cc1-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="76cc1-121">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="76cc1-121">Service workers</span></span>  

<span data-ttu-id="76cc1-122">Сотрудники служб являются фундаментальной технологией в будущей веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="76cc1-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="76cc1-123">Это сценарии, которые браузер выполняет в фоновом режиме, отдельно от веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="76cc1-124">Эти сценарии позволяют получить доступ к функциям, которые не требуют веб-страницы или взаимодействия с пользователем, например push-уведомления, фоновую синхронизацию и автономные функции.</span><span class="sxs-lookup"><span data-stu-id="76cc1-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="76cc1-125">Панель **"Рабочие службы"** на панели приложений — это основное место в DevTools для проверки и отладки сотрудников служб. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="76cc1-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="The Service Workers pane" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="76cc1-127">The **Service Workers** pane</span><span class="sxs-lookup"><span data-stu-id="76cc1-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="76cc1-128">Если рабочий работник службы установлен на открытую в данный момент страницу, он будет указан на этой области.</span><span class="sxs-lookup"><span data-stu-id="76cc1-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="76cc1-129">Например, на предыдущем рисунке установлен рабочий работник службы для `https://weather-pwa-sample.firebaseapp.com` области .</span><span class="sxs-lookup"><span data-stu-id="76cc1-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="76cc1-130">Автономный **контрольный** ящик помещает DevTools в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="76cc1-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="76cc1-131">Это эквивалентно автономному режиму, доступного на панели **"Сеть"** или параметру `Go offline` в меню [команд.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="76cc1-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="76cc1-132">При **перезагрузке при** обновлении необходимо, чтобы рабочий работник службы обновлял каждую загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="76cc1-133">Обход **для сетевого checkbox** обходит рабочий процесс службы и заставляет браузер перейти в сеть для запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="76cc1-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="76cc1-134">**Кнопка** "Обновить" выполняет одно разовую обновление указанного рабочего сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="76cc1-135">**Кнопка** push-уведомлений эмулирует push-уведомление без полезной нагрузки (также известной как **"tickle**\").</span><span class="sxs-lookup"><span data-stu-id="76cc1-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="76cc1-136">Кнопка **"Синхронизация"** эмулирует событие фоновой синхронизации.</span><span class="sxs-lookup"><span data-stu-id="76cc1-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="76cc1-137">Кнопка **"Отрегистрить"** отрегистрет указанного сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="76cc1-138">Ознакомьтесь [с очисткой хранилища,](#clear-storage) чтобы отоимнуть регистрацию сотрудника службы и очистить хранилище и кэш одним нажатием кнопки.</span><span class="sxs-lookup"><span data-stu-id="76cc1-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="76cc1-139">**Строка** источника сообщает, когда был установлен работающий в данный момент рабочий день службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="76cc1-140">Ссылка — это имя файла источника рабочего службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="76cc1-141">Щелкнув ссылку, вы отправите вас к источнику рабочего службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="76cc1-142">**Строка** состояния сообщает о состоянии рабочего сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="76cc1-143">Номер ИД рядом с зеленым индикатором состояния \( на предыдущем рисунке\) — для активного рабочего `#36` рабочего.</span><span class="sxs-lookup"><span data-stu-id="76cc1-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="76cc1-144">Рядом с состоянием вы \*\*\*\* увидите кнопку запуска \(если рабочий работник \*\*\*\* службы остановлен\) или кнопку остановки \(если рабочий работник службы запущен\).</span><span class="sxs-lookup"><span data-stu-id="76cc1-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="76cc1-145">Рабочие службы должны быть остановлены и запущены браузером в любое время.</span><span class="sxs-lookup"><span data-stu-id="76cc1-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="76cc1-146">Явное остановка рабочего сотрудника службы с помощью кнопки **остановки** может имитировать это.</span><span class="sxs-lookup"><span data-stu-id="76cc1-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="76cc1-147">Остановка работы службы — это отличный способ проверить поведение кода при повторном вработке.</span><span class="sxs-lookup"><span data-stu-id="76cc1-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="76cc1-148">Он часто выявляет ошибки из-за ошибок, предполагающих постоянное глобальное состояние.</span><span class="sxs-lookup"><span data-stu-id="76cc1-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="76cc1-149">В **строке** "Клиенты" указывается источник, к который имеет область действия для рабочего сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="76cc1-150">**Кнопка** фокуса в основном полезна при включаемом всех **контрольных** окнах.</span><span class="sxs-lookup"><span data-stu-id="76cc1-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="76cc1-151">Если этот контрольный список включен, в списке будут перечислены все зарегистрированные сотрудники службы.</span><span class="sxs-lookup"><span data-stu-id="76cc1-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="76cc1-152">Если нажать кнопку **фокуса** рядом с сотрудником службы, работающим на другой вкладке, Microsoft Edge будет фокусироваться на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="76cc1-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="76cc1-153">Если сотрудник службы вызывает ошибки, появляется новая метка **"Ошибки".**</span><span class="sxs-lookup"><span data-stu-id="76cc1-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="76cc1-154">Кэши рабочих служб</span><span class="sxs-lookup"><span data-stu-id="76cc1-154">Service worker caches</span></span>  

<span data-ttu-id="76cc1-155">В **области хранилища** кэша содержится список ресурсов, которые были кэшироваться только для чтения с помощью [API][MDNWebCacheAPI]кэша \(service worker\) .</span><span class="sxs-lookup"><span data-stu-id="76cc1-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="The Cache Storage Pane" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="76cc1-157">The **Cache Storage** Pane</span><span class="sxs-lookup"><span data-stu-id="76cc1-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="76cc1-158">При первом откройте кэш и добавьте в него ресурс, DevTools может не обнаружить изменение.</span><span class="sxs-lookup"><span data-stu-id="76cc1-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="76cc1-159">Перезагрузите страницу, и вы увидите кэш.</span><span class="sxs-lookup"><span data-stu-id="76cc1-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="76cc1-160">Если у вас два или более кэша, они \*\*\*\* будут указаны ниже в выпаданом списке "Хранилище кэша".</span><span class="sxs-lookup"><span data-stu-id="76cc1-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="The Cache Storage dropdown" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="76cc1-162">The **Cache Storage** dropdown</span><span class="sxs-lookup"><span data-stu-id="76cc1-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="76cc1-163">Использование квоты</span><span class="sxs-lookup"><span data-stu-id="76cc1-163">Quota usage</span></span>  

<span data-ttu-id="76cc1-164">Некоторые ответы в области **хранения** кэша могут быть помечены как непрозрачивые.</span><span class="sxs-lookup"><span data-stu-id="76cc1-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="76cc1-165">Это означает ответ, полученный из другого источника, например из **CDN** или удаленного API, если [CORS][FetchHttpCorsProtocol] не включен.</span><span class="sxs-lookup"><span data-stu-id="76cc1-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="76cc1-166">Чтобы избежать утечки информации между доменами, к размеру непрозрачной реакции, используемой для вычисления ограничений квот хранилища (например, о том, было ли исключение выброшено)и сообщается API, значительно добавлено `QuotaExceeded` `navigator.storage` заполнение.</span><span class="sxs-lookup"><span data-stu-id="76cc1-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="76cc1-167">Сведения об этом заполнении отличаются в зависимости от браузера, но для Microsoft Edge это означает, что минимальный размер любого кэширования непрозрачной реакции на общий объем использования хранилища составляет примерно \*\*\*\* [7 Мбайт.][ChromiumIssues796060#c17]</span><span class="sxs-lookup"><span data-stu-id="76cc1-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="76cc1-168">Это следует помнить при определении необходимого объема непрозрачной реакции, так как вы можете легко превысить ограничения квоты хранилища намного раньше, чем ожидалось в противном случае, в зависимости от фактического размера непрозрачной информации.</span><span class="sxs-lookup"><span data-stu-id="76cc1-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="76cc1-169">Связанные руководства:</span><span class="sxs-lookup"><span data-stu-id="76cc1-169">Related Guides:</span></span>  

*   [<span data-ttu-id="76cc1-170">Stack Overflow: какие ограничения применяются к непрозрачной реакции?</span><span class="sxs-lookup"><span data-stu-id="76cc1-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="76cc1-171">Очистка хранилища</span><span class="sxs-lookup"><span data-stu-id="76cc1-171">Clear storage</span></span>  

<span data-ttu-id="76cc1-172">Очистка **области** хранения — очень полезная функция при разработке последовательных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="76cc1-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="76cc1-173">С помощью этой области можно оторегистрировать службы и очистить все кэши и хранилище одним нажатием кнопки.</span><span class="sxs-lookup"><span data-stu-id="76cc1-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <span data-ttu-id="76cc1-174">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76cc1-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Проблема Chromium 796060: значение хранилища кэша растет при каждом обновлении, когда код аналитики находится в HTML-коде"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш веб-API | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Stack Overflow: какие ограничения применяются к непрозрачной реакции?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="76cc1-179">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76cc1-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="76cc1-180">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="76cc1-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="76cc1-182">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76cc1-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
