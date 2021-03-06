---
description: Используйте панель приложений для проверки, изменения и отработки манифестов веб-приложений, сотрудников служб и кэшей сотрудников службы.
title: Отламывка прогрессивных веб-приложений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398541"
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

# <a name="debug-progressive-web-apps"></a><span data-ttu-id="93e24-104">Отламывка прогрессивных веб-приложений</span><span class="sxs-lookup"><span data-stu-id="93e24-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="93e24-105">Используйте панель **приложений** для проверки, изменения и отработки манифестов веб-приложений, сотрудников служб и кэшей сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="93e24-106">В этом руководстве обсуждаются только функции прогрессивного веб-приложения панели **приложений.**</span><span class="sxs-lookup"><span data-stu-id="93e24-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a><span data-ttu-id="93e24-107">Сводка</span><span class="sxs-lookup"><span data-stu-id="93e24-107">Summary</span></span>  

*   <span data-ttu-id="93e24-108">Используйте области **Манифеста** для проверки манифеста веб-приложения и запуска событий Add to Homescreen.</span><span class="sxs-lookup"><span data-stu-id="93e24-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="93e24-109">Используйте области **Service Workers** для целого ряда задач, связанных с рабочим обслуживанием, таких как незарегистрирование или обновление службы, эмуляция событий push-связи, отключение или остановка сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="93e24-110">Просмотр кэша сотрудника службы из **области хранения** кэша.</span><span class="sxs-lookup"><span data-stu-id="93e24-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="93e24-111">Незарегистрировать сотрудника службы и очистить все хранилища и кэши с помощью одной кнопки выберите из области **хранения Clear.**</span><span class="sxs-lookup"><span data-stu-id="93e24-111">Unregister a service worker and clear all storage and caches with a single button choose from the **Clear storage** pane.</span></span>  
    
## <a name="web-app-manifest"></a><span data-ttu-id="93e24-112">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="93e24-112">Web app manifest</span></span>  

<span data-ttu-id="93e24-113">Если вы хотите, чтобы пользователи могли добавлять приложение на мобильные домашние экраны, вам нужен манифест веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="93e24-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="93e24-114">Манифест определяет, как приложение отображается на домашнем экране, куда направлять пользователя при запуске с домашнего экрана и как выглядит приложение при запуске.</span><span class="sxs-lookup"><span data-stu-id="93e24-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="93e24-115">После того, как вы настроите манифест, вы можете проверить его с помощью области **Манифест** **панели** приложений.</span><span class="sxs-lookup"><span data-stu-id="93e24-115">After you have your manifest set up, you may use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Области манифеста" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="93e24-117">Области **манифеста**</span><span class="sxs-lookup"><span data-stu-id="93e24-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="93e24-118">Чтобы взглянуть на источник манифеста, выберите ссылку под меткой **Манифест приложения** \( на `https://airhorner.com/manifest.json` предыдущем рисунке\).</span><span class="sxs-lookup"><span data-stu-id="93e24-118">To look at the manifest source, choose the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="93e24-119">В **разделах Identity** и **Presentation** отображаются поля из источника манифеста в более удобном для пользователя дисплее.</span><span class="sxs-lookup"><span data-stu-id="93e24-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="93e24-120">В **разделе Значки** отображаются все указанные значки.</span><span class="sxs-lookup"><span data-stu-id="93e24-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a><span data-ttu-id="93e24-121">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="93e24-121">Service workers</span></span>  

<span data-ttu-id="93e24-122">Работники служб являются фундаментальной технологией в будущей веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="93e24-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="93e24-123">Это скрипты, которые браузер выполняет в фоновом режиме, отдельно от веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="93e24-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="93e24-124">Скрипты позволяют получать доступ к функциям, которые без необходимости веб-страницы или взаимодействия с пользователем, например push-уведомления, синхронизации фона и автономного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="93e24-124">The scripts allow you to access features that without the need of a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="93e24-125">Панель **сотрудников служб** в панели **Приложений** — это основное место в DevTools для проверки и отладки сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Области рабочих служб" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="93e24-127">Области **рабочих** служб</span><span class="sxs-lookup"><span data-stu-id="93e24-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="93e24-128">Если сотрудник службы установлен на открытую страницу в настоящее время, он указан на этой области.</span><span class="sxs-lookup"><span data-stu-id="93e24-128">If a service worker is installed to the currently open page, then it is listed on this pane.</span></span>  <span data-ttu-id="93e24-129">Например, на предыдущем рисунке установлен сотрудник службы для области `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="93e24-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="93e24-130">Автономный **почтовый** ящик выводит DevTools в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="93e24-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="93e24-131">Это эквивалентно автономному режиму, доступному с помощью средства **Network,** или параметру `Go offline` в [командном меню.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="93e24-131">This is equivalent to the offline mode available from the **Network** tool, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="93e24-132">Обновление **при перезагрузке контрольного** ящика заставляет сотрудника службы обновляться на каждой загрузке страницы.</span><span class="sxs-lookup"><span data-stu-id="93e24-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="93e24-133">Обход **сетевого почтового** ящика обходит сотрудника службы и заставляет браузер перейти в сеть для запрашиваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="93e24-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="93e24-134">Кнопка **Update** выполняет одно время обновление указанного сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="93e24-135">Кнопка **push** эмулирует push-уведомление без полезной нагрузки \(также известной как **щекотка**\).</span><span class="sxs-lookup"><span data-stu-id="93e24-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="93e24-136">Кнопка **Sync** эмулирует событие фоновой синхронизации.</span><span class="sxs-lookup"><span data-stu-id="93e24-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="93e24-137">Кнопка **Unregister** отрегистрирована указанному работнику службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="93e24-138">Ознакомьтесь [с возможностью](#clear-storage) отрегистрации сотрудника службы и очистки хранилища и кэшей с помощью одной кнопки.</span><span class="sxs-lookup"><span data-stu-id="93e24-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button choose.</span></span>  
*   <span data-ttu-id="93e24-139">Строка **Source** сообщает, когда был установлен работающий в настоящее время сотрудник службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="93e24-140">Ссылка — это имя источника файла сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-140">The link is the name of the source file of the service worker.</span></span>  <span data-ttu-id="93e24-141">Выбор по ссылке отправляет вас к источнику сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-141">Choosing on the link sends you to the source of the service worker.</span></span>  
*   <span data-ttu-id="93e24-142">В **строке Status** указывается состояние сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="93e24-143">Номер ID рядом с зеленым индикатором состояния \( на предыдущем рисунке\) для действующего в настоящее время `#36` сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="93e24-144">Рядом со состоянием \*\*\*\* отображается кнопка запуска \(если сотрудник \*\*\*\* службы остановлен\) или кнопка остановки \(если рабочий службы запущен\).</span><span class="sxs-lookup"><span data-stu-id="93e24-144">Next to the status, a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\) is displayed.</span></span>  <span data-ttu-id="93e24-145">Сотрудники службы предназначены для того, чтобы остановиться и начать работу с помощью браузера в любое время.</span><span class="sxs-lookup"><span data-stu-id="93e24-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="93e24-146">Явное прекращение работы сотрудника службы с помощью кнопки **остановки** может имитировать это.</span><span class="sxs-lookup"><span data-stu-id="93e24-146">Explicitly stopping your service worker using the **stop** button may simulate that.</span></span>  <span data-ttu-id="93e24-147">Остановка сотрудника службы — это отличный способ проверить, как ведет себя код, когда сотрудник службы снова запускается обратно.</span><span class="sxs-lookup"><span data-stu-id="93e24-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="93e24-148">Он часто выявляет ошибки из-за ошибок в предположениях о сохраняемом глобальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="93e24-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="93e24-149">В **строке** "Клиенты" указывается происхождение, в которое будет вовсю засвеяна область действия сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="93e24-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="93e24-150">Кнопка **фокуса** в основном полезна при включении всех **контрольных** ящиков.</span><span class="sxs-lookup"><span data-stu-id="93e24-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="93e24-151">Когда этот контрольный ящик включен, все зарегистрированные сотрудники службы перечислены.</span><span class="sxs-lookup"><span data-stu-id="93e24-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="93e24-152">Если вы выбираете кнопку **фокуса** рядом с сотрудником службы, который работает на другой вкладке, Microsoft Edge фокусируется на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="93e24-152">If you choose on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="93e24-153">Если сотрудник службы вызывает какие-либо ошибки, появляется новая метка , называемая **Ошибки.**</span><span class="sxs-lookup"><span data-stu-id="93e24-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a><span data-ttu-id="93e24-154">Кэши сотрудников службы</span><span class="sxs-lookup"><span data-stu-id="93e24-154">Service worker caches</span></span>  

<span data-ttu-id="93e24-155">В **области хранения** кэша содержится список ресурсов, которые кэшировали только для чтения с помощью [API][MDNWebCacheAPI]кэша \(service worker\) .</span><span class="sxs-lookup"><span data-stu-id="93e24-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Пространство хранения кэша" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="93e24-157">Пространство **хранения кэша**</span><span class="sxs-lookup"><span data-stu-id="93e24-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="93e24-158">При первом открываемом кэше и добавлении в него ресурса, DevTools может не обнаружить изменения.</span><span class="sxs-lookup"><span data-stu-id="93e24-158">The first time you open a cache and add a resource to it, DevTools may not detect the change.</span></span>  <span data-ttu-id="93e24-159">Обновите страницу и отобразите кэш.</span><span class="sxs-lookup"><span data-stu-id="93e24-159">Refresh the page and to display the cache.</span></span>  

<span data-ttu-id="93e24-160">Если открыты два или более кэшей, кэши \*\*\*\* отображаются под следующей каплей хранилища кэша.</span><span class="sxs-lookup"><span data-stu-id="93e24-160">If you have two or more caches open, the caches display under the following **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Отсев хранилища кэша" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="93e24-162">**Отсев хранилища кэша**</span><span class="sxs-lookup"><span data-stu-id="93e24-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <a name="quota-usage"></a><span data-ttu-id="93e24-163">Использование квот</span><span class="sxs-lookup"><span data-stu-id="93e24-163">Quota usage</span></span>  

<span data-ttu-id="93e24-164">Некоторые ответы в области **хранения** кэша могут быть помечены как "непрозрачивые".</span><span class="sxs-lookup"><span data-stu-id="93e24-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="93e24-165">Это относится к ответу, извлеченному из другого происхождения, например из **CDN** или удаленного API, когда [CORS][FetchHttpCorsProtocol] не включен.</span><span class="sxs-lookup"><span data-stu-id="93e24-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="93e24-166">Чтобы избежать утечек меж доменных сведений, к размеру непрозрачной реакции, используемой для вычисления ограничений квоты хранения\(например, будет ли выброшено исключение\) добавляется значительное обивка и `QuotaExceeded` `navigator.storage` сообщается API.</span><span class="sxs-lookup"><span data-stu-id="93e24-166">In order to avoid leakage of cross-domain information, significant padding is added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="93e24-167">Сведения об этой обивке варьируются от браузера до браузера, но для Microsoft Edge это означает, что минимальный размер, который любой один кэширования непрозрачной реакции способствует общему использованию хранилища составляет около [7 мегабайт][ChromiumIssues796060#c17]. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="93e24-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="93e24-168">Помните обивку при определении того, сколько непрозрачной реакции необходимо кэширование, так как ограничения квоты на хранение могут быть превышены гораздо раньше, чем ожидались в зависимости от фактического размера непрозрачной информации.</span><span class="sxs-lookup"><span data-stu-id="93e24-168">Remember the padding when determining how many opaque responses you want to cache, since you may easily exceed storage quota limitations much sooner than you otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="93e24-169">Связанные руководства:</span><span class="sxs-lookup"><span data-stu-id="93e24-169">Related Guides:</span></span>  

*   [<span data-ttu-id="93e24-170">Переполнение стека: какие ограничения применяются к непрозрачной реакции?</span><span class="sxs-lookup"><span data-stu-id="93e24-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a><span data-ttu-id="93e24-171">Очистка хранилища</span><span class="sxs-lookup"><span data-stu-id="93e24-171">Clear storage</span></span>  

<span data-ttu-id="93e24-172">Пространство **Clear Storage** — это очень полезная функция при разработке прогрессивных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="93e24-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="93e24-173">Эта области позволяет отрегистрировать сотрудников службы и очистить все кэши и хранилища с помощью одной кнопки выбрать.</span><span class="sxs-lookup"><span data-stu-id="93e24-173">This pane lets you unregister service workers and clear all caches and storage with a single button choose.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="93e24-174">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="93e24-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: значение хранилища кэша повышается при каждом обновлении, когда код Analytics находится в html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш — веб-| MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Переполнение стека: какие ограничения применяются к непрозрачной реакции?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="93e24-179">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="93e24-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="93e24-180">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="93e24-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="93e24-182">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="93e24-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
