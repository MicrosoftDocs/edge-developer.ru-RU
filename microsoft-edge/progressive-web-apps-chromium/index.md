---
description: Прогрессивное веб-приложение (Chromium) работает в Windows 10.  Вот все, что вам нужно знать как веб-разработчик.
title: Прогрессивное веб-приложение в Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: последовательные веб-приложения, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a13f39dc3b3e0d47ad07b0e447556dc14093e71b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231218"
---
# <span data-ttu-id="fe58f-105">Обзор "Прогрессивное веб-приложение для Windows"</span><span class="sxs-lookup"><span data-stu-id="fe58f-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="fe58f-106">[Последовательные веб-приложения][MDNApps] \(PWAs\) предоставляют доступ к открытым веб-технологиям для кроссплатформенного межплатформенного использования и предоставляют пользователям собственный пользовательский опыт для своих устройств.</span><span class="sxs-lookup"><span data-stu-id="fe58f-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="fe58f-107">PWAs — это [][AListApartUnderstandingProgressiveEnhancement] веб-сайты, которые постепенно улучшаются для работы как нативные приложения на вспомогательных платформах.</span><span class="sxs-lookup"><span data-stu-id="fe58f-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="fe58f-108">В приложениях PWA объединены лучшие качестве веб- и собственных приложения.</span><span class="sxs-lookup"><span data-stu-id="fe58f-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="fe58f-109">Обнаруживаемый</span><span class="sxs-lookup"><span data-stu-id="fe58f-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="fe58f-110">Из результатов веб-поиска и вспомогательных хранилищ приложений</span><span class="sxs-lookup"><span data-stu-id="fe58f-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="fe58f-111">Возможность установки</span><span class="sxs-lookup"><span data-stu-id="fe58f-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="fe58f-112">Закрепление и запуск с домашнего экрана, меню "Пуск", панели задач и других задач</span><span class="sxs-lookup"><span data-stu-id="fe58f-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="fe58f-113">Повторное вовлечение</span><span class="sxs-lookup"><span data-stu-id="fe58f-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="fe58f-114">Отправка push-уведомлений, даже если приложение не активно</span><span class="sxs-lookup"><span data-stu-id="fe58f-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="fe58f-115">Network Independent</span><span class="sxs-lookup"><span data-stu-id="fe58f-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="fe58f-116">Работает в автономном режиме и в условиях низкой сети</span><span class="sxs-lookup"><span data-stu-id="fe58f-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="fe58f-117">Постепенный</span><span class="sxs-lookup"><span data-stu-id="fe58f-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="fe58f-118">Масштабирования (или вниз) с помощью возможностей устройств</span><span class="sxs-lookup"><span data-stu-id="fe58f-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="fe58f-119">Безопасный</span><span class="sxs-lookup"><span data-stu-id="fe58f-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="fe58f-120">Обеспечивает безопасную конечную точку HTTPS и другие пользовательские меры безопасности</span><span class="sxs-lookup"><span data-stu-id="fe58f-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="fe58f-121">Хорошая скорость отклика</span><span class="sxs-lookup"><span data-stu-id="fe58f-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="fe58f-122">Адаптируется к размеру экрана или ориентации пользователя и методу ввода</span><span class="sxs-lookup"><span data-stu-id="fe58f-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="fe58f-123">Связываемая</span><span class="sxs-lookup"><span data-stu-id="fe58f-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="fe58f-124">Совместное и запуск из стандартной гиперссылки</span><span class="sxs-lookup"><span data-stu-id="fe58f-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="fe58f-125">Создайте (или преобразуйте\) существующий веб-сайт в PWA, чтобы улучшить взаимодействие с пользователями.</span><span class="sxs-lookup"><span data-stu-id="fe58f-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="fe58f-126">Усовершенствования включают push-уведомления, интеграцию с приложениями и поддержку автономного режима.</span><span class="sxs-lookup"><span data-stu-id="fe58f-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="fe58f-127">Продолжайте создавать аудиторию на открытом веб-сайте, чтобы пользователи обнаруживали PWA с помощью поиска и обмена ссылками.</span><span class="sxs-lookup"><span data-stu-id="fe58f-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="fe58f-128">Лучше всего то, что ваше приложение обновляется с помощью кода веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="fe58f-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="fe58f-129">PWAs в Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="fe58f-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="fe58f-130">Когда вы создаете API-API для прогрессивного веб-приложения, нацеленного на веб-стандарты, ваше приложение может быть развернуто на различных платформах и устройствах и использовать преимущества специальных возможностей, доступных для устройств.</span><span class="sxs-lookup"><span data-stu-id="fe58f-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="fe58f-131">PwAs в Microsoft Edge \(Chromium\) добавляет следующие преимущества на ваш веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="fe58f-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="fe58f-132">Ваше приложение основано на веб-платформе на основе стандартов.</span><span class="sxs-lookup"><span data-stu-id="fe58f-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="fe58f-133">Позволяет пользователям устанавливать приложение непосредственно из браузера.</span><span class="sxs-lookup"><span data-stu-id="fe58f-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="fe58f-134">Позволяет пользователям устанавливать приложение без развертывания или регистрации в Магазине.</span><span class="sxs-lookup"><span data-stu-id="fe58f-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="fe58f-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span><span class="sxs-lookup"><span data-stu-id="fe58f-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="fe58f-136">Microsoft Edge \(Chromium\) доступен в Windows 7, Windows 10 и macOS.</span><span class="sxs-lookup"><span data-stu-id="fe58f-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="fe58f-137">Включены следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="fe58f-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="fe58f-138">Приложения могут устанавливаться непосредственно из браузера с помощью значка **"Установить"** на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="fe58f-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Установка flyout и значка приложения" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="fe58f-140">Установка flyout и значка приложения</span><span class="sxs-lookup"><span data-stu-id="fe58f-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="fe58f-141">Приложения также могут устанавливаться, запускаться и управляться из меню **"Приложения**  >  **параметров".**</span><span class="sxs-lookup"><span data-stu-id="fe58f-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Элементы меню приложения в параметрах" lightbox="./media/app_menus.png":::
       <span data-ttu-id="fe58f-143">Элементы меню приложения в параметрах</span><span class="sxs-lookup"><span data-stu-id="fe58f-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="fe58f-144">Веб-уведомления интегрированы в систему уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="fe58f-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="fe58f-145">Общее хранилище файлов cookie с профилем браузера, в который было установлено приложение</span><span class="sxs-lookup"><span data-stu-id="fe58f-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="fe58f-146">Доступ к другим функциям браузера с помощью меню "Параметр" и других параметров **,включая** проверку сертификатов, разрешения сайта, защиту от слежения и `...` расширения браузера</span><span class="sxs-lookup"><span data-stu-id="fe58f-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="fe58f-147">Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения</span><span class="sxs-lookup"><span data-stu-id="fe58f-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="fe58f-148">Чтобы адаптировать PWAS специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, перейдите к [документации, относяшейся к функциям PWA EdgeHTML][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="fe58f-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="fe58f-149">Узнайте больше о тестировании PWA в Windows 10 и его распространении в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="fe58f-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="fe58f-150">Дополнительные сведения о преимуществах PWA, предстоящих функций и коротких демонстрациях можно найти в сеансе [Build 2020 PWA.][BuildVideo]</span><span class="sxs-lookup"><span data-stu-id="fe58f-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="fe58f-151">Требования</span><span class="sxs-lookup"><span data-stu-id="fe58f-151">Requirements</span></span>  

<span data-ttu-id="fe58f-152">Для запуска в качестве PWA ваше веб-приложение, в которое входит сервер, должно включать следующие минимальные требования.</span><span class="sxs-lookup"><span data-stu-id="fe58f-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="fe58f-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-154">Защищает пользователей, обеспечивая безопасное подключение для связи с сервером или приложением.</span><span class="sxs-lookup"><span data-stu-id="fe58f-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="fe58f-155">Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемой по безопасному подключению \(или из для `localhost` отладки\).</span><span class="sxs-lookup"><span data-stu-id="fe58f-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-156">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="fe58f-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-157">Использует потоки Service Worker для работы в качестве сетевых прокси-серверов между сервером и клиентом приложения.</span><span class="sxs-lookup"><span data-stu-id="fe58f-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="fe58f-158">Рабочие потоки служб обеспечивают поддержку автономного режима, кэширование ресурсов, push-уведомления, синхронизацию фоновых данных и оптимизацию производительности при загрузке страниц.</span><span class="sxs-lookup"><span data-stu-id="fe58f-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-159">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="fe58f-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-160">Предоставляет файл метаданных на основе JSON, в который описываются основные сведения о веб-приложении, чтобы Windows 10 и другие хост-платформы предоставляют пользователям PWA возможность установки, как собственный приложения.</span><span class="sxs-lookup"><span data-stu-id="fe58f-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="fe58f-161">Основные сведения включают значки, язык и точку входа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="fe58f-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="fe58f-162">Чтобы быть отличным PWA, ваше приложение также должно соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="fe58f-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-163">Совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="fe58f-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-164">Убедитесь, что PWA работает [путем тестирования][MicrosoftDeveloperEdgeToolsRemote] в различных браузерах и средах.</span><span class="sxs-lookup"><span data-stu-id="fe58f-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-165">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="fe58f-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-166">Применяет гибкие макеты и гибкие изображения.</span><span class="sxs-lookup"><span data-stu-id="fe58f-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="fe58f-167">Адаптивный дизайн включает следующие элементы, которые адаптируют пользовательский интерфейс к устройству пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe58f-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="fe58f-168">Сетка [CSS][MDNCssGridLayout]</span><span class="sxs-lookup"><span data-stu-id="fe58f-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="fe58f-169">flexbox</span><span class="sxs-lookup"><span data-stu-id="fe58f-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="fe58f-170">Сетка CSS [и][MDNCssGridLayout] [flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="fe58f-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="fe58f-171">запросы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fe58f-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="fe58f-172">адаптивные изображения</span><span class="sxs-lookup"><span data-stu-id="fe58f-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="fe58f-173">Использует [средства эмуляции][DevToolsGuideDeviceModeTestingOtherBrowsers] устройства из браузера для локального тестирования или создания удаленного сеанса отладки в [Windows][DevtoolsRemoteDebuggingWindows] или [Android][DevtoolsRemoteDebuggingIndex] для тестирования непосредственно на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="fe58f-173">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-174">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="fe58f-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-175">Маршрутит каждую страницу сайта по уникальному URL-адресу, чтобы существующие пользователи могли помочь вам привлечь еще более широкую аудиторию с помощью общего доступа к социальным медиа.</span><span class="sxs-lookup"><span data-stu-id="fe58f-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-176">Методики проверки и тестирования</span><span class="sxs-lookup"><span data-stu-id="fe58f-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-177">Использует средства качества кода, такие как [linter Webhint,][Webhint] для оптимизации эффективности, надежности, безопасности и доступности приложения.</span><span class="sxs-lookup"><span data-stu-id="fe58f-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="fe58f-178">Контрольный список Chromium PWA</span><span class="sxs-lookup"><span data-stu-id="fe58f-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="fe58f-179">Проверяет PWA на основе контрольного списка PWA google базовых параметров.</span><span class="sxs-lookup"><span data-stu-id="fe58f-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="fe58f-180">Чтобы превратить PWA в приложение [Microsoft Store,][MicrosoftDeveloperStore] перейдите к [Progressive Web Apps (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="fe58f-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="fe58f-181">См. также</span><span class="sxs-lookup"><span data-stu-id="fe58f-181">See also</span></span>  

*   [<span data-ttu-id="fe58f-182">Вайсинг (PwAs)</span><span class="sxs-lookup"><span data-stu-id="fe58f-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="fe58f-183">Прогрессивное движение для прогрессивного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="fe58f-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="fe58f-184">Автономные POS-карты с прогрессивной веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="fe58f-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="fe58f-185">Вопросы и&PWA A</span><span class="sxs-lookup"><span data-stu-id="fe58f-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="fe58f-186">Подавка в Интернете</span><span class="sxs-lookup"><span data-stu-id="fe58f-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="fe58f-187">Именовать прогрессивное веб-приложение</span><span class="sxs-lookup"><span data-stu-id="fe58f-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="fe58f-188">Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)</span><span class="sxs-lookup"><span data-stu-id="fe58f-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="fe58f-189">Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)</span><span class="sxs-lookup"><span data-stu-id="fe58f-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="fe58f-190">Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)</span><span class="sxs-lookup"><span data-stu-id="fe58f-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Начало работы с удаленной отладой устройств с Android | Документы Майкрософт"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Начало работы с удаленной отладки устройств с Windows 10 | Документы Майкрософт"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Эмуляция и тестирование других браузеров | Документы Майкрософт"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Debug Progressive Web Apps | Документы Майкрософт"  
<!--[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "What's new in EdgeHTML 17 | Microsoft Docs"  -->  
<!--[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "What's New in EdgeHTML 14 | Microsoft Docs"  -->  
[PwaEdgehtmlIndex]: .. /edgehtml/progressive-web-apps/index.md "Progressive Web Apps (EdgeHTML) on Windows | Microsoft Docs"  
[PwaEdgehtmlMicrosoftStore]: .. /edgehtml/progressive-web-apps/microsoft-store.md "Progressive Web Apps in the Microsoft Store | Microsoft Docs"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Обзор push-службы Notification Services Windows (WNS) | Документы Майкрософт"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Проектирование для Xbox и телевизора | Документы Майкрософт"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Вопросы пользовательского интерфейса для устройств UWP | Документы Майкрософт"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Что такое приложение универсальной платформы Windows (UWP)? | Документы Майкрософт"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Поддержка приложения с помощью фоновых задач | Документы Майкрософт"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Публикация приложений и игр для Windows | Документы Майкрософт"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Открытие учетной записи разработчика | Документы Майкрософт"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Постепенное обновление веб-приложений в Microsoft Edge и Windows 10 — блоги о Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API фоновой синхронизации — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Манифест веб-приложения — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Мгновенное тестирование"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Смешанная реальность для разработчиков"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Загрузка нового браузера Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Включить или отключить фокус в Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Изменение параметров уведомлений в Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "Вопросы и&PWA A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Understanding Progressive Enhancement - A List Apart"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "apps | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Тестирование в разных браузерах | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Гибкий макет полей CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API fetch | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Запросы мультимедиа | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Обнаруживаемые преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installable — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Независимо от сети — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Прогрессивное — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Повторное вовлечение — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Адаптивный — преимущества прогрессивного веб-приложения"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Безопасный — преимущества прогрессивного веб-приложения"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Адаптивные изображения | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Видео по PWA"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивное движение для прогрессивного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Захиминг PWAs — новый выпуск Edge Edition"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Именовать прогрессивное веб-приложение"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Подавка в Интернете"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные POS-карты с прогрессивной веб-приложениями"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Что делает хорошее прогрессивное веб-приложение? | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википдия"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS — Википедия"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Адаптивный веб-дизайн — Википедия"  
