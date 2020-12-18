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
# Обзор "Прогрессивное веб-приложение для Windows"  

[Последовательные веб-приложения][MDNApps] \(PWAs\) предоставляют доступ к открытым веб-технологиям для кроссплатформенного межплатформенного использования и предоставляют пользователям собственный пользовательский опыт для своих устройств.  PWAs — это [][AListApartUnderstandingProgressiveEnhancement] веб-сайты, которые постепенно улучшаются для работы как нативные приложения на вспомогательных платформах.  В приложениях PWA объединены лучшие качестве веб- и собственных приложения.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Обнаруживаемый][MDNPwaAdvantagesDiscoverable]
        Из результатов веб-поиска и вспомогательных хранилищ приложений
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Возможность установки][MDNPwaAdvantagesInstallable]
        Закрепление и запуск с домашнего экрана, меню "Пуск", панели задач и других задач
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Повторное вовлечение][MDNPwaAdvantagesReEngageable]
        Отправка push-уведомлений, даже если приложение не активно
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Network Independent][MDNPwaAdvantagesNetworkIndependent]
        Работает в автономном режиме и в условиях низкой сети
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [Постепенный][MDNPwaAdvantagesProgressive]
        Масштабирования (или вниз) с помощью возможностей устройств
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Безопасный][MDNPwaAdvantagesSafe]
        Обеспечивает безопасную конечную точку HTTPS и другие пользовательские меры безопасности
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Хорошая скорость отклика][MDNPwaAdvantagesResponsive]
        Адаптируется к размеру экрана или ориентации пользователя и методу ввода
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Связываемая][MDNPwaAdvantagesLinkable]
        Совместное и запуск из стандартной гиперссылки
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Создайте (или преобразуйте\) существующий веб-сайт в PWA, чтобы улучшить взаимодействие с пользователями.  Усовершенствования включают push-уведомления, интеграцию с приложениями и поддержку автономного режима.  Продолжайте создавать аудиторию на открытом веб-сайте, чтобы пользователи обнаруживали PWA с помощью поиска и обмена ссылками.  Лучше всего то, что ваше приложение обновляется с помощью кода веб-сервера.  

## PWAs в Microsoft Edge (Chromium)  

Когда вы создаете API-API для прогрессивного веб-приложения, нацеленного на веб-стандарты, ваше приложение может быть развернуто на различных платформах и устройствах и использовать преимущества специальных возможностей, доступных для устройств.  PwAs в Microsoft Edge \(Chromium\) добавляет следующие преимущества на ваш веб-сайт.  

*   Ваше приложение основано на веб-платформе на основе стандартов.  
*   Позволяет пользователям устанавливать приложение непосредственно из браузера.  
*   Позволяет пользователям устанавливать приложение без развертывания или регистрации в Магазине.  
    
Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available. Microsoft Edge \(Chromium\) доступен в Windows 7, Windows 10 и macOS.  Включены следующие преимущества.  

*   Приложения могут устанавливаться непосредственно из браузера с помощью значка **"Установить"** на панели навигации.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Установка flyout и значка приложения" lightbox="./media/install_pwa_icon.png":::
       Установка flyout и значка приложения  
    :::image-end:::  
    
*   Приложения также могут устанавливаться, запускаться и управляться из меню **"Приложения**  >  **параметров".**  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Элементы меню приложения в параметрах" lightbox="./media/app_menus.png":::
       Элементы меню приложения в параметрах  
    :::image-end:::  
    
*   Веб-уведомления интегрированы в систему уведомлений Windows  
*   Общее хранилище файлов cookie с профилем браузера, в который было установлено приложение  
*   Доступ к другим функциям браузера с помощью меню "Параметр" и других параметров **,включая** проверку сертификатов, разрешения сайта, защиту от слежения и `...` расширения браузера  
*   Полный доступ к [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] для отладки приложения  
    
> [!IMPORTANT]
> Чтобы адаптировать PWAS специально для Windows 10, которые делают запросы API WinRT с помощью JavaScript, перейдите к [документации, относяшейся к функциям PWA EdgeHTML][PwaEdgehtmlIndex].  Узнайте больше о тестировании PWA в Windows 10 и его распространении в Microsoft Store.  

> [!NOTE]
> Дополнительные сведения о преимуществах PWA, предстоящих функций и коротких демонстрациях можно найти в сеансе [Build 2020 PWA.][BuildVideo] 

## Требования  

Для запуска в качестве PWA ваше веб-приложение, в которое входит сервер, должно включать следующие минимальные требования.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Защищает пользователей, обеспечивая безопасное подключение для связи с сервером или приложением.  Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемой по безопасному подключению \(или из для `localhost` отладки\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Служебные сценарии][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Использует потоки Service Worker для работы в качестве сетевых прокси-серверов между сервером и клиентом приложения.  Рабочие потоки служб обеспечивают поддержку автономного режима, кэширование ресурсов, push-уведомления, синхронизацию фоновых данных и оптимизацию производительности при загрузке страниц.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Манифест веб-приложения][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Предоставляет файл метаданных на основе JSON, в который описываются основные сведения о веб-приложении, чтобы Windows 10 и другие хост-платформы предоставляют пользователям PWA возможность установки, как собственный приложения.  Основные сведения включают значки, язык и точку входа URL-адреса. 
   :::column-end:::
:::row-end:::  

Чтобы быть отличным PWA, ваше приложение также должно соответствовать следующим требованиям.  

:::row:::
   :::column span="1":::
      [Совместимость между браузерами][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Убедитесь, что PWA работает [путем тестирования][MicrosoftDeveloperEdgeToolsRemote] в различных браузерах и средах.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Адаптивный дизайн][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Применяет гибкие макеты и гибкие изображения.  Адаптивный дизайн включает следующие элементы, которые адаптируют пользовательский интерфейс к устройству пользователя.  
      
      *   Сетка [CSS][MDNCssGridLayout]  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   Сетка CSS [и][MDNCssGridLayout] [flexbox][MDNCssFlexibleBoxLayout]  
      *   [запросы мультимедиа][MDNMediaQueries]  
      *   [адаптивные изображения][MDNResponsiveImages]  
      
      Использует [средства эмуляции][DevToolsGuideDeviceModeTestingOtherBrowsers] устройства из браузера для локального тестирования или создания удаленного сеанса отладки в [Windows][DevtoolsRemoteDebuggingWindows] или [Android][DevtoolsRemoteDebuggingIndex] для тестирования непосредственно на целевом устройстве.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Глубокая связь][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Маршрутит каждую страницу сайта по уникальному URL-адресу, чтобы существующие пользователи могли помочь вам привлечь еще более широкую аудиторию с помощью общего доступа к социальным медиа.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Методики проверки и тестирования][Webhint]  
   :::column-end:::
   :::column span="2":::
      Использует средства качества кода, такие как [linter Webhint,][Webhint] для оптимизации эффективности, надежности, безопасности и доступности приложения.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Контрольный список Chromium PWA][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Проверяет PWA на основе контрольного списка PWA google базовых параметров.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Чтобы превратить PWA в приложение [Microsoft Store,][MicrosoftDeveloperStore] перейдите к [Progressive Web Apps (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore].  
  
## См. также  

*   [Вайсинг (PwAs)][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Прогрессивное движение для прогрессивного веб-приложения][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Автономные POS-карты с прогрессивной веб-приложениями][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [Вопросы и&PWA A][AaronGustafsonNotebookPwaQa]  
*   [Подавка в Интернете][JoretegBlogBettingWeb]  
*   [Именовать прогрессивное веб-приложение][Fberriman20170626NamingProgressiveWebApps]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
