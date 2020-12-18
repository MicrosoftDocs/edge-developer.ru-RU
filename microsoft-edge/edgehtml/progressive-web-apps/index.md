---
description: Прогрессивное веб-приложение работает в Windows 10.  Вот все, что вам нужно знать как веб-разработчик.
title: Прогрессивные веб-приложения (EdgeHTML) на Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: последовательные веб-приложения, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 87996f6be7c1963c01a476b307a31e689e3880d4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235496"
---
# Прогрессивные веб-приложения (EdgeHTML) на Windows  

С [помощью progressive Web Apps][MDNApps] (или просто PWAs\) вам не нужно решать между использованием открытых веб-технологий для кроссплатформенного взаимодействия и предоставлением пользователям собственных приложений, настроенных для их устройства.  Это происходит потому, что PWAs [][AListApartUnderstandingProgressiveEnhancement] — это только веб-сайты, которые постепенно улучшаются для работы как нативные приложения на вспомогательных платформах.  В приложениях PWA объединены лучшие качестве веб- и собственных приложения.  

:::row:::
    :::column:::
        ![Значок обнаружения][ImageISearch]
        ### [Обнаруживаемый][MDNPwaAdvantagesDiscoverable]
        Из результатов веб-поиска и вспомогательных хранилищ приложений
    :::column-end:::
    :::column:::
        ![Устанавливаемый значок][ImageIPackage]
        ### [Возможность установки][MDNPwaAdvantagesInstallable]
        Закрепление и запуск с домашнего экрана  
    :::column-end:::
    :::column:::
        ![Значок повторного вовлечения][ImageIPushNotification]
        ### [Повторное вовлечение][MDNPwaAdvantagesReEngageable]
        Отправка push-уведомлений, даже если приложение не активно  
    :::column-end:::
    :::column:::
        ![Сетевой независимый значок][ImageIOffline]
        ### [Network Independent][MDNPwaAdvantagesNetworkIndependent]
        Работает в автономном режиме и в условиях низкой сети  
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Значок "Прогрессивное"][ImageIProgressive]
        ### [Постепенный][MDNPwaAdvantagesProgressive]
        Масштабы возможностей \(вверх или вниз)с возможностями устройств  
    :::column-end:::
    :::column:::
        ![Значок "Безопасный"][ImageISecurity]
        ### [Безопасный][MDNPwaAdvantagesSafe]
        Обеспечивает безопасную конечную точку HTTPS и другие пользовательские меры безопасности  
    :::column-end:::
    :::column:::
        ![Значок отклика][ImageIResponsive]
        ### [Хорошая скорость отклика][MDNPwaAdvantagesResponsive]
        Адаптируется к размеру экрана, ориентации и методу ввода пользователя  
    :::column-end:::
    :::column:::
        ![Значок со ссылками][ImageILink]
        ### [Связываемая][MDNPwaAdvantagesLinkable]
        Совместное и запуск из стандартной гиперссылки  
    :::column-end:::
:::row-end:::

Построив или преобразовав существующий сайт в PWA, вы сможете лучше привлекать существующую аудиторию с помощью push-уведомлений и автономной поддержки.  В то же время вы можете продолжить построение аудитории на открытом веб-сайте, так как пользователи обнаруживают PWA с помощью поиска и обмена ссылками.  

## PWAs в Windows 10 (EdgeHTML)  

> [!NOTE]
> С переходом на Microsoft Edge (Chromium) с EdgeHTML, используемые PWAs, используются не одинаковые веб-платформы.  Edge (Chromium) PWAs устанавливаются и запускаются в браузере.  Edge (EdgeHTML) PWAs работают как приложения универсальной платформы Windows (UWP) и используют более старую веб-платформу EdgeHTML.  Если вам требуется доступ к API Windows 10 для PWA, эта документация EdgeHTML для вас.  Если ваша цель — кроссплатформовая поддержка без доступа к API для Windows, переходить к документации [по Microsoft Edge (Chromium) PWA.][PwaChromiumIndex]  

Когда вы создаете прогрессивное веб-приложение, чтобы воспользоваться преимуществами Windows 10, вы можете распространять PWA через [Microsoft Store,][MicrosoftDeveloperStore]вся база установки Windows 10, вмеяемая 600 и более миллионов активных ежемесячных пользователей, является потенциальной аудиторией приложения!  Приложения, разработанные таким образом, запускались как приложения универсальной [платформы Windows][WindowsUWPGetStartedGuide] и имеют такой же доступ к API WinRT.  Обратите внимание, что веб-платформа, отрисовка кода является EdgeHTML при использовании API WinRT, поэтому обязательно используйте обнаружение функций перед вызовом любых API Для Windows, чтобы убедиться, что PWA может по-прежнему работать на платформах, где Доступны PWA Microsoft Edge \(Chromium\) PWAs.  

[Вот как][PwaEdgehtmlGetStarted] начать преобразовывать веб-приложение в PWA \(EdgeHTML\), тестировать его в Windows 10 и распространять в Microsoft Store.  

## Требования  

Для запуска в качестве веб-приложения PWA как минимум требуется:  

*   [HTTPS][WikiHttps].  Защитите пользователей, предоставив безопасное подключение для связи между сервером и приложением.  Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемой по безопасному подключению \(или из для `localhost` отладки\).  
  
*   [Сотрудники службы.][MDNServiceWorkerApi]  Используйте рабочие потоки службы для работы в качестве сетевых прокси-серверов между сервером и клиентом приложения, чтобы обеспечить поддержку автономного режима, кэширование ресурсов, push-уведомления, синхронизацию фоновых данных и оптимизацию загрузки страницы.  

*   [Манифест веб-приложения.][MDNWebAppManifest]  Предодайте файл метаданных на основе JSON, описывающий основные сведения о вашем веб-приложении (например, значки, язык и точка входа URL-адреса\), чтобы Windows 10 и другие хост-платформы могли предоставлять пользователям PWA возможность установки, как собственный приложения.  Связывание сайта с манифестом веб-приложения дает ему право на автоматическое включение в [Microsoft Store][PwaEdgehtmlMicrosoftStoreImportingBing] через службу индексации Bing.  

Чтобы ваше приложение было отличным PWA, ему также требуется:  

*   [Совместимость между браузерами.][MDNCrossBrowserTesting]  Убедитесь, что PWA работает [путем тестирования][MicrosoftDeveloperEdgeToolsRemote] в различных браузерах и средах.  В Windows 10 обязательно протестировать приложение как в браузере Microsoft Edge, так и в полной версии PWA: в качестве установленного, standalone приложения для Windows 10 \(на основе движка EdgeHTML\).  
  
*   [Адаптивный дизайн.][WikiResponsiveWebDesign]  Применяйте гибкие макеты и гибкие изображения с [][MDNMediaQueries]сеткой [CSS][MDNCssGridLayout] и/или [flexbox,][MDNCssFlexibleBoxLayout]запросами мультимедиа и [адаптивными изображениями[MDNResponsiveImages),] чтобы адаптировать пользовательский интерфейс к устройству пользователя.  Используйте средства [эмуляции][DevToolsGuideEmulation] устройств из браузера для [][DevToolsProtocolClientsEdgeDevToolsPreview] локального тестирования или настроить удаленный сеанс отладки для тестирования непосредственно на целевом устройстве.  В Windows 10 PWAs \(EdgeHTML\) также [][WindowsUWPDesignDevicesIndex] можно адаптировать для форм-факторов помимо настольных компьютеров, телефонов и планшетов, включая устройства [Xbox и TV,][WindowsUWPDesignDevicesDesigningTv] [Surface Hub][MicrosoftDeveloperWindowsSurfaceHub]и Windows [Mixed Reality.][MicrosoftDeveloperWindowsMixedReality]  
  
*   [Глубокая связь.][WikiDeepLinking]  Перена основе каждой страницы сайта на уникальный URL-адрес, чтобы существующие пользователи могли помочь вам привлечь еще более широкую аудиторию с помощью общего доступа к социальным медиа.  

*   [Практические практики.][Webhint]  Используйте средства качества кода, такие как [webhint][Webhint] linter, для оптимизации эффективности, надежности, безопасности и доступности приложения.  

Чтобы отправить прогрессивное веб-приложение в [Microsoft Store,][MicrosoftDeveloperStore]необходимо:  

*   Учетная [запись разработчика Майкрософт][WindowsUWPPublishDeveloperAccount]  
*   Завершены [действия по публикации приложения для Windows][WindowsUWPPublishIndex]  

В ближайшие месяцы существующие pwAs [][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] в Интернете, которые соответствуют определенным критериям, будут автоматически индексироваться поисковой программой Bing в Microsoft Store (где разработчики могут напрямую управлять ими для своей аудитории Windows 10\).  

Дополнительные сведения см. в [pwAs (EdgeHTML) в Microsoft Store.][PwaEdgehtmlMicrosoftStore]  

## Текущая доступность  

Поддержка браузерных движков для вызовов "Прогрессивного веб-приложения" для ряда компонентов архитектуры, наиболее важной из них является сетическая инфраструктура, которая является частью [API fetch.][MDNFetchApi]  Поддержка PWA в движке EdgeHTML была завершена в выпуске Windows 10 1809.  Дополнительные улучшения веб-стандартов с момента этого времени не будут включены в обработок EdgeHTML, поэтому обязательно запустите тесты совместимости и используйте обнаружение функций для корректного отката, если требуется неподключить функцию PWA на платформе EdgeHTML.  

Для предстоящего выпуска Microsoft Edge \(Chromium\) в 2020 г. платформа браузера будет полностью поддерживать эти функции, которые работают на всех устройствах, на которых поддерживается браузер Chromium.  

Для EdgeHTML и Windows текущее состояние технологий PWA на основе стандартов:  

| Технология | Описание | Доступность | Примечания по использованию |  
|:--- |:--- |:--- |:--- |  
| [Манифест веб-приложения][MDNWebAppManifest] | Предоставляет метаданные приложения операционной системы на хост-сайте для включения установки и продвижения магазина приложений.  Требуется для PWAs в Microsoft Store.  | [В разработке][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | На данный момент вы можете использовать [построитель PWA][|::ref1::|] для создания манифеста JSON, совместимого с W3C, и упаковки приложения для различных платформ ОС.  В Windows PWA Builder преобразует манифест JSON в формат `.appxmanifest` \(XML\), необходимый для приложений для Windows 10.  |  
| [Fetch API][MDNFetchApi] | Предоставляет асинхронную сеть \(запросы, ответы\) для ресурсов страницы |[EdgeHTML 14+][DevGuideWhatsNewEdgeHtml14] / Сборка 14393 и более новые | [Синтаксис API][MDNServiceWorkerApi] для рабочих служб основан на сетевых API на основе fetch.  Вы также можете использовать [API fetch][MDNFetchApi] в целом в качестве современной альтернативы. `XMLHttpRequest`  |  
| [API рабочих служб][MDNServiceWorkerApi] | Предоставляет модель веб-приложения с автономным режимом или сетевой прокси-сервер, где сценарии на основе событий запускают независимо от веб-страниц  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] / сборка 17133+ | Экспериментальная поддержка \(за `Enable Service Workers` флагом\) поставляется в EdgeHTML 16.  On by default in EdgeHTML 17+ builds.  |  
| [API кэша][MDNCache] | Предоставляет механизм хранения для пар сетевых запросов и ответов | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] / сборка 17133+ | См. [примечание об API для рабочих служб][MDNServiceWorkerApi] выше.  |  
| [Push API][MDNPushApi] | Позволяет сотруднику службы подписываться на push-уведомления |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] / сборка 17133+| См. [примечание об API для рабочих служб][MDNServiceWorkerApi] выше.  Приложения для Windows 10 \(включая PWAs\) требуют, чтобы служба push-уведомлений [Windows \(WNS\)][WindowsUWPControlsPatternTilesNotificationsWns] доставляла push-уведомления, которая поддерживает [API][MDNPushApi]push-уведомлений W3C.  |  
| [API уведомлений][MDNNotificationsApi] | Позволяет сотруднику службы отображать системное уведомление пользователю при push-уведомлении | [EdgeHTML 14+][DevGuideWhatsNewEdgeHtml14] / Сборка 14393 и более новые | Веб-уведомления в EdgeHTML полностью интегрированы с [][MicrosoftSupportWindowsNotificationSettings]центром уведомлений Windows 10, где пользователи могут управлять уведомлениями приложений и устанавливать часы ["Тихий".][MicrosoftSupportWindowsFocusAssist]  |  
| [API фоновой синхронизации][MDNSyncManager] | Предоставляет API для уведомления сотрудника службы о том, что пользователь снова в сети, и для планирования периодических событий для синхронизации локальных данных с сервером | [В разработке][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | На данный момент вы можете использовать собственный [API BackgroundTask WinRT][WindowsUWPLaunchResumeBackgroundTasks] для реализации фоновых задач для PWA при запуске в качестве приложения для Windows 10.  |  

Вот текущее состояние поддержки PWAs в Microsoft Store в Windows 10:  

| Метод отправки в Магазин | Состояние | Сведения |  
|:--- |:--- |:--- |  
| Manual \(developer initiated\) | Доступно | Ознакомьтесь [с pwAs (EdgeHTML) в Microsoft Store,][PwaEdgehtmlMicrosoftStore] чтобы начать работу.  |  
| Automatic \(auto-indexed with Bing\) | Ожидается в ближайшее время | В [настоящее время мы пилотно][WindowsBlogsWelcomingPWAsEdgeWindows] работаем над процессом встраиваемого процесса PWA с ограниченным подмножеством партнеров приложений.  В ближайшие месяцы Корпорация Майкрософт приветствует PWAs на основном веб-сайте в Microsoft Store.  Ознакомьтесь с автоматическим импортом PWA с [помощью Bing,][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] чтобы узнать больше о требованиях Microsoft Store для автоматически созданных объявлений PWA.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview — клиенты протокола DevTools | Документы Майкрософт"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Эмуляция | Документы Майкрософт"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Новые возможности EdgeHTML 17 | Документы Майкрософт"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Новые возможности EdgeHTML 14 | Документы Майкрософт"  
[PwaChromiumIndex]: ../../progressive-web-apps-chromium/index.md "Progressive Web Apps (Chromium) в Windows | Документы Майкрософт"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps/get-started.md "Начало работы с progressive Web Apps (EdgeHTML) | Документы Майкрософт"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Прогрессивное веб-приложение в Microsoft Store | Документы Майкрософт"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Критерии автоматической отправки — прогрессивное веб-приложение в Microsoft Store | Документы Майкрософт"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: ./microsoft-store.md#automatic-pwa-importing-with-bing "Автоматический импорт PWA с помощью Bing — прогрессивное веб-приложение (EdgeHTML) в Microsoft Store | Документы Майкрософт"  


[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Обзор push-службы Notification Services Windows \(WNS\)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Проектирование для Xbox и телевизора"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Вопросы пользовательского интерфейса для устройств UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Поддержка приложения с помощью фоновых задач"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Публикация приложений и игр для Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Открытие учетной записи разработчика"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Постепенное обновление веб-приложений в Microsoft Edge и Windows 10 — блоги о Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API фоновой синхронизации — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Манифест веб-приложения — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Мгновенное тестирование"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Смешанная реальность для разработчиков"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Включить или отключить фокус в Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Изменение параметров уведомлений в Windows 10"  

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
[Адаптивные изображения MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "| MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википдия"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS — Википедия"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Адаптивный веб-дизайн — Википедия"  
