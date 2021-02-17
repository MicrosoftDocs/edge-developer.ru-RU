---
description: Заметки о выпуске microsoft Edge WebView2 SDK
title: Заметки о выпуске Для Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/16/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, элемент управления браузером, edge html
ms.openlocfilehash: 58f96dda9c05cfc10790e3523a494e42cf33ec12
ms.sourcegitcommit: 988c9add287abd203acf1d5d51ef7146e6f0b351
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/16/2021
ms.locfileid: "11339922"
---
# Заметки о выпуске webView2 SDK  

Команда WebView2 обновляет [SDK WebView2][NuGetGallery] в течение шести недель.  Просмотрите следующие материалы, чтобы получить последние сведения об объявлениях, добавлениях, изменениях и вносимых в API изменений.  

> [!NOTE]
> Убедитесь, что приложение повторно скомпилировать после обновления пакета NuGet.  Команда рекомендует использовать канал Canary при разработке с использованием пакетов предварительного выпуска, а также невторяемую времени работы при использовании выпущенных пакетов.  Для получения дополнительных сведений перейдите к [versioning][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions].  
 
## 1.0.790-предварительнаяrelease  

Дата выпуска: 10 февраля 2021 г.  

[Пакет NuGet][NuGetGallery1.0.790-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

### Общие  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release package 1.0.781 is deprecated.  Прекращение разработки с пакетом 1.0.781.  

> [!IMPORTANT]
> Предварительный пакет WebView2 0.9.430 является неподготовленным и удаляется из предстоящего выпуска.  Если ваше приложение WebView использует пакет, рекомендуется обновить его до более нового.  

##### Функции  

*   Добавлены [методы TrySuspend и Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] для приостановки и возобновления WebViews.  
*   Добавлен [метод SetVirtualHostNameToFolderMapping,][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] который соповедет имя виртуального хоста с путем каталога.  \([\#37,][GithubMicrosoftedgeWebviewfeedbackIssue37] [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]и [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Добавлено [свойство DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] для настройки цвета и альфа-канала фона.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Добавлено [свойство UserAgent,][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] чтобы получить или установить агент пользователя.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Метод `CreateCookieWithCookie` заменен `CopyCookie` методом.  
*   Добавлена поддержка визуального размещения с помощью интерфейса [ICoreWebView2CompositionController,][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] который создается с помощью нового `CreateCoreWebView2CompositionController` `ICoreWebView2Environment3` метода.  

    
##### Исправления ошибок  

*   Отключена функция покупок в Microsoft Edge в WebView2.  
*   Отключено контекстное меню в представлении PDF, когда `AreDefaultContextMenusEnabled` это `false` так.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Исправлена ошибка, возвращаемая `E_NOINTERFACE` при `ICoreWebView2` `ICoreWebView2Experimental` запросе.  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Исправлена ошибка, разрешив навигацию с неправильно отформатированной ЮРИС, `CoreWebView2NavigationStartingEventArgs.Cancel` если установлено его. `false`  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Исправлена ошибка, заблокированная во всплывающих окнах с подключенными к событиям `window.print()` обработчиками `NewWindowRequested` событий.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Исправлена проблема динамического DPI при перемещении приложений между разными мониторами.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Улучшены экземпляры, переданные `HRESULT` [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke.][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]  
*   Отключена кнопка "Управление автозаполненными".  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Исправлены Visual Studio сбои во `WebView2.Dispose` время работы при их работе в нескольких окнах.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\ и [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Исправлена ошибка для отображения управления WebView2 в Visual Studio панели инструментов.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Снижение высокой нагрузки на ЦП.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Исправлены проблемы с нерекометентным пакетом предварительного выпуска 1.0.781. [\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [и \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
##### Рекламные акции  

*   Следующие экспериментальные API теперь повышены до Stable.  
    *   API визуального размещения.  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend и Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
    
#### .NET  

##### Исправления ошибок  

*   Исправлена ошибка, которая сбой приложений WebView, которые используют WPF SDK.  Сбой произошел, когда окна были закрыты с помощью клавиши F4.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Теперь экран инициализации WebView2 прозрачный, а не серый.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## 1.0.705.50  

Дата выпуска: 25 января 2021 г.  

[Пакет NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime version 86.0.616.0 or newer  

##### Рекламные акции  

*   Следующие экспериментальные API теперь повышены до Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API управления файлами cookie][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Свойство WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## 1.0.721-предварительнаяrelease  

Дата выпуска: 8 декабря 2020 г.  

[Пакет NuGet][NuGetGallery1.0.721-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

#### Общие  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release package 1.0.707 and package 0.9.628 are deprecated.  Прекращение разработки с пакетами 1.0.707 и package0.9.628.  

###### Функции  

*   Добавлены [групповые политики WebView2.][DeployedgeMicrosoftEdgeWebviewPolicies]  Дополнительные сведения о рекомендуемых методиках можно найти в групповых [политиках для WebView2.][Webview2ConceptsEnterpriseGroupPoliciesForWebview2]  
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated the old registry location.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Добавлена поддержка [перетаскивания][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] в WebView2.  
*   Добавлены API для обработки поддержки DPI.  
    *   Добавлено [свойство RasterizationScale,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] чтобы изменить масштаб DPI для содержимого WebView и всплывающих папок пользовательского интерфейса, а также связанное событие [RasterizationScaleChanged.][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]  
    *   Добавлено [свойство ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] для автоматического обновления `RasterizationScale` свойства при необходимости.  
    *   Добавлено свойство [BoundsMode,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] чтобы указать, что границы являются пикселями логики и что WebView можно использовать для отображения пикселей WebView2, а WebView использует его для получения `RasterizationScale` `RasterizationScale` `Bounds` физического размера.  
*   Обновлено `NewWindowRequested` событие для обработки и `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] и [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Следующие экспериментальные API теперь повышены до Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API управления файлами cookie][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Свойство WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
#### .NET  

###### Функции  

*   Включен конструктор WinForms в .NET Core 3.1+ и .NET 5.  
*   Улучшено управление файлами cookie .NET.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Заменено `CoreWebView2Ready` [CoreWebView2InitializationCompleted.][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]  

###### Исправления ошибок

*   Добавлено [событие AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] для поддержки нажатия AcceleratorKey в WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Удалены ненужные файлы из вывода в папки WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Улучшенный API объектов host.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] и [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## 1.0.664.37  

Дата выпуска: 20 ноября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.664.37] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

> [!IMPORTANT]
> **Announcement**: .NET WPF/WinForms WebView2 SDKs are now Generally Available \(GA\).  Начиная с этого выпуска, SDKs выпуска совместимы с другими выпусками.  Дополнительные сведения можно найти в записи блога с [объявлением о ga.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

###### Функции  

*   .NET WPF/WinForms WebView2 теперь доступен в общем доступе \(GA\).  
*   Фиксированный режим распространения \(Bring-your-own\) достиг ga.  
    
#### .NET  

###### Исправления ошибок  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` предотвращает открытие нового окна.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] и [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## 1.0.674-предварительнаяrelease  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

*   Добавлен [метод NavigateWithWebResourceRequest][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] для предоставления данных о публикации или других заголовок запросов во время навигации.  
*   Добавлено [событие DOMContentLoaded,][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] которое запускается при загрузке и разбике исходного HTML-документа.  
*   Добавлено [свойство Environment][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] в WebView2.  Это свойство предоставляет доступ к среде WebView2, в которой был создан экземпляр WebView2.  
*   Добавлены [API управления][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] файлами cookie, позволяющие разработчикам проверить подлинность сеанса WebView2 или получить файлы cookie из WebView для проверки подлинности других средств.  Группа Веб-просмотров планирует внести улучшения в язык или структуру.  Для получения дополнительных сведений перейдите к [обзору API: управление файлами cookie.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Обновлено событие [WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] и добавлены непрерывная [webResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] и [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] в [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent].  
*   [Отключение Application Guard в Microsoft Defender (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] в WebView2.  
*   Добавлен [SystemCursorId для][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] визуального размещения.  
*   Добавлена исправлена ошибка для метода input в визуальном размещении.  
*   Удалены требования к использованию `version.lib` статической библиотеки WebView2.  
    
#### .NET  

*   Обновлен класс [CoreWebView2,][DotnetApiMicrosoftWebWebview2CoreCorewebview2] чтобы показать `CoreWebView2Environment` переменную.  
*   Изменены реализации пользовательских классов EventArgs в пространстве имен на подклассы `Microsoft.Web.WebView2.Core` [System.EventArgs][DotnetApiSystemEventargs] [или System.ComponentModel.CancelEventArgs.][DotnetApiSystemComponentmodelCancelEventargs]  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Добавлена поддержка [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] в WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   Добавлены [API WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Обновлено свойство "Источник [конструктора][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] winForms" по умолчанию или значение null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Обновлены границы WebView2 в WebView2.Init() для поддержки режимов DPI, которые меньше 100 %.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Обновлены [BuildWindowCore и][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] для повышения надежности.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Обновлена база загрузщика .NET для загрузки на бит процесса, а не на архитектуру операционной системы.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Переименовано `EdgeNotFoundExpection` на [WebView2RuntimeNotFoundException.][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]  
    
## 1.0.622.22  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.622.22] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

> [!IMPORTANT]
> **Announcement**: Win32 C/C++ WebView2 is now Generally Available \(GA\).  Начиная с этого выпуска, SDKs выпуска совместимы с версией.  Дополнительные сведения можно найти в записи блога с [объявлением о ga.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [Постоянное застойное время работы WebView2 и установщик][Webview2ConceptsDistributionUnderstandRuntimeInstaller] являются ga.  Bootstrapper, downlink link for the Bootstrapper, and Standalone Installer for the Evergreen WebView2 Runtime are available on [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Пример кода для рабочего процесса установки также доступен в репо [WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   [Режим фиксированной версии][Webview2ConceptsDistributionFixedVersionDistributionMode] доступен для предварительной версии разработчика.  
    
## 0.9.622.11  

Дата выпуска: 10 сентября 2020 г.  

[Пакет NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

*   > [!IMPORTANT]
    > **Announcement**: this SDK is the Release Candidate for WebView2 Win32 C/C++ GA.  Версия ga должна использовать тот же интерфейс API и функции.  
    
*   Отключенные [политики браузера.][DeployedgeMicrosoftEdgePolicies]  
*   Добавлено [свойство AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Обновлено, чтобы включить свойство `ICoreWebView2NewWindowRequestedEventArgs` [WindowFeatures][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] и связанное [с ним ICoreWebView2WindowFeatures.][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Обновлено `System.Windows.Rect`  для использования вместо `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Обновлено событие NewWindowRequested для обработки `window.open()` запроса без параметров.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Указанные параметры AdditionalBrowserArguments][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] не переопределяются переменными среды `ICoreWebView2EnvironmentOptions` или значениями реестра.  Дополнительные сведения можно найти в [createCoreWebView2EnvironmentWithOptions.][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]  
    
## 0.9.579  

Дата выпуска: 20 июля 2020 г.  

[Пакет NuGet][NuGetGallery0.9.579] \| Microsoft Edge версии 86.0.579.0.  

#### Общие  

*   > [!IMPORTANT]
    > **Announcement**: Evergreen WebView2 Runtime and installer is released for preview.  Для получения дополнительных сведений перейдите к [распространению WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Объявление:** следующие версии SDK WebView2 больше не поддерживаются после следующего выпуска SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Версии SDK WebView2 также помечаются как неподготовленные для nuget.org.  WebView2 рекомендует быть в курсе последних версий WebView2.  
    
*   Добавлены улучшения рабочих потоков WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Отключено блокатор всплывающих блоков в WebView.  Для получения дополнительных сведений перейдите к [свойству IsUserInitiated][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] `NewWindowRequested` в событии.  
*   Убедитесь, что событие запуска навигации WebView запускается для `about:blank` .  Теперь события запускаются для всех переходов, но отмены для `NavigationStarting` `about:blank` или iframe `srcdoc` не поддерживаются и игнорируются.  
*   Блокировал некоторые `edge://` схемы URI в WebView.  
*   Добавлено экспериментальное свойство [IsSingleSignOnUsingOSPrimaryAccountEnabled][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Добавлено экспериментальное событие [WebResourceResponseReceived,][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] которое запускается после того, как WebView получит и обрабатывает ответ от запроса WebResource.  В объект отклика включаются заглавныедеры проверки подлинности (если они имеются).  
    
#### .NET  

*   Улучшена обработка фокуса WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Добавлено `ZoomFactor` свойство контроллера WPF Webview2.  
    
## 0.9.538  

[Пакет NuGet][NuGetGallery0.9.538] \| Microsoft Edge версии 85.0.538.0.  

#### Общие  

*   Поддержка WebView2 SDK версии [0.8.149.](#08149)  WebView2 рекомендует быть в курсе последних версий WebView2.  
*   Обновлена групповая политика с учетом времени изменения пути профиля браузера Microsoft Edge \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
#### Win32 C/C++  

*   Добавлен [iCoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures,][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]который срабжает при запуске и связи с `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Нарушение изменений:** чтобы обеспечить соответствие API WebView2 соглашениям об именах API Windows, команда WebView обновила имена следующих приложений.  
    > 
    > *   [AreRemoteObjectsAllowed теперь][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] [— AreHostObjectsAllowed.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]  
    
*   Обновлено [addHostObjectToScript.][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]  Теперь маркеры сериализатора объектов исходного хост-объекта настроены на прокси-объекты.  Затем маркеры сериализации объектов хост-объекта сериализируются обратно в качестве хост-объекта, когда передаются в качестве параметра в обратном вызове JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
#### .NET (предварительная версия 0.9.538)  

*   Выпущены winForms и примеры WPF WebView2API, которые являются полными руководствами по SDK WebView2.  Для получения дополнительных сведений перейдите в [репо примеры][GithubMicrosoftedgeWebview2samplesMain].  
*   Добавлена поддержка экспериментальных API визуального размещения [и][Webview2ConceptsVersioningExperimentalApis]окон.  
*   > [!IMPORTANT]
    > **Breaking Change**: The following deferrals now implement IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested,][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]and [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Добавлены [getAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] и [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] в качестве статических средств [CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## 0.9.515-предварительнаяrelease  

[Пакет NuGet][NuGetGallery0.9.515-prerelease] \| Microsoft Edge версии 84.0.515.0.  

*   > [!IMPORTANT]
    > **Объявление:** WebView2 теперь поддерживает Windows Forms и WPF на .NET Framework 4.6.2 или более **** поздней версии и .NET Core 3.0 или более поздней версии в предварительном пакете.  
    
*   Дополнительные сведения о создании приложений WPF можно найти в руководстве по началу работы [с WPF][Webview2GettingstartedWpf] и справочнике [по WPF WebView2][DotnetApiMicrosoftWebWebview2Wpf] для API, характерных для WPF.  
*   Дополнительные сведения о создании приложений Windows Forms можно найти в руководстве по началу работы с [Windows Forms][Webview2GettingstartedWinforms] и справочнике по формам [Windows][DotnetApiMicrosoftWebWebview2Winforms] WebView2 для API Windows Forms.  
*   Дополнительные сведения об API CoreWebView2 можно найти в [справочнике по .NET.][DotnetApiMicrosoftWebWebview2Core]  
*   > [!CAUTION]
    > **Известные проблемы:** команда WebView знает о некоторых проблемах в предварительной версии, которые будут устранены в будущих выпусках.  
    > 
    > *   **Информирование о DPI:** WebView2 для WPF в настоящее время не знает О DPI.  При инициализации WebView2 на мониторах с высоким DPI существует известная проблема, из-за которой WebView сначала инициализируется как доля окна до тех пор, пока размер окна не будет меняться.  
    > *   **Конструктор WPF**: конструктор WPF в настоящее время не поддерживается.  Добавьте в приложение соответствующий XAML-код, непосредственно изменяя его в текстовом редакторе.  
    
## 0.9.488  

[Пакет NuGet][NuGetGallery0.9.488] \| Microsoft Edge версии 84.0.488.0.  

*   > [!IMPORTANT]
    > **Объявление:** начиная с предстоящей версии 83 Microsoft Edge, Веб-просмотр Evergreen больше не будет ориентирован на канал браузера Stable.  Вместо этого он ориентирован на другой набор binaries под названием ["Всегдаgreen WebView2 Runtime",][Webview2ConceptsDistributionEvergreenDistributionMode]которые можно установить цепочкой с помощью установщика, разрабатываемого командой WebView.  Для получения дополнительных сведений перейдите в [app-Distribution][Webview2ConceptsDistribution].  
    
*   > [!IMPORTANT]
    > **Объявление:** в будущем команда WebView выпускает два пакета: предварительный пакет с экспериментальными API \(для вас, чтобы опробовыть\) и стабильный пакет выпуска со стабильными API \(для вашей уверенности\).  Чтобы узнать о различиях, перейдите к [данным о версиях браузера и WebView2.][Webview2ConceptsVersioning]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Чтобы обеспечить соответствие API WebView2 соглашениям об именованию API Windows, команда WebView обновила имена следующих интерфейсов.  
    > 
    > *   `CORE_WEBVIEW2_*` теперь имеется префикс `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] теперь [— GetAvailableCoreWebView2BrowserVersionString.][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] [теперь][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]get_BrowserVersionString .  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] теперь [является AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] теперь [— RemoveHostObjectFromScript.][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]  
    > *   `chrome.webview.remoteObjects` is now `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: the `AddRemoteObject` JS proxy methods are also renamed.  
    > 
    > *   `getLocal` is now `getLocalProperty` .  
    > *   `setLocal` is now `setLocalProperty` .  
    > *   `getRemote` is now `getHostProperty` .  
    > *   `setRemote` is now `setHostProperty` .  
    > *   `applyRemote` is now `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   Добавлено [событие FrameNavigationCompleted.][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]  Теперь, когда iframe завершает навигацию, происходит событие, которое возвращает успешность навигации и ее ИД.  
*   Добавлен [интерфейс ICoreWebView2EnvironmentOptions,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] который можно использовать для определения версии времени выполнения WebView2, нацеленной на ваше приложение.  
*   Добавлен [параметр IsBuiltInErrorPageEnabled.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  Теперь вы можете включить или отключить встроенную веб-страницу ошибки для сбоя навигации и сбоя процесса отрисовки.  
*   Обновлено внедрение удаленных объектов для поддержки реализаций .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Обновлено [событие NewWindowRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] для обработки запросов из контекстных меню \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Выпущен первый отдельный предварительный пакет WebView2, в котором можно получить доступ к API визуального размещения.  Команда WebView обновила [APISample,][GithubMicrosoftedgeWebview2samplesMain] включив новые экспериментальные API.  
    
    *   Добавлен [интерфейс ICoreWebView2ExperimentalCompositionController][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] для подключения к дереву композиции и предоставления входных данных для WebView.  
    *   Добавлен [iCoreWebView2ExperimentalPointerInfo,][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]который содержит все сведения из `POINTER_INFO` .  Этот объект передается в SendPointerInput для ввода ввода указателя в WebView.  
    *   Добавлен [iCoreWebView2ExperimentalCursorChangedEventHandler,][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]который сообщает приложению, когда следует изменить курсор мыши над WebView.  При нацелии мыши на текстовое поле в WebView курсор изменяется со стрелки на селектор.  Свойство в приложении сообщает приложению, что в настоящее время должен быть курсор мыши `cursor` `CompositionController` для WebView.  
    
## 0.9.430  

[Пакет NuGet][NuGetGallery0.9.430] \| Microsoft Edge версии 82.0.430.0.  

WebView2 SDK является официальной бета-версией Win32 C++, которая включает несколько запросов функций из отзывов.  Команда WebView пытается ограничить количество выпусков с нарушением изменений.  По мере приближения к общей доступности в бета-версию включено несколько существенных существенных изменений.  

*   > [!IMPORTANT]
    > **Breaking Change**: As the final release approaches the WebView team renamed the prefix *IWebView2WebView*   to *ICoreWebView2*   in order to make sure the WebView2 API aligns with the Windows API naming convention.  Кроме того, чтобы использовать SDK WebView2 из структур пользовательского интерфейса, группа WebView разделилась на `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] и [ICoreWebView2Host.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430]  `ICoreWebView2Host` поддерживается размер, отображение и скрытие, фокус и другие функции, связанные с окнами и композицией.  ICoreWebView2 поддерживает все остальные функции WebView2.  Чтобы узнать больше о внедрении изменений, [][GithubMicrosoftedgeWebview2samplesPr17] перейдите к запросу на включение WebView2 в проект [WebView2 APISample.][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Split [DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] into three components:  [SourceChanged,][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged] [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading], and [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Теперь, когда исходный URL-адрес `SourceChanged` изменяет, событие будет запускаться.  При смене состояния истории `HistoryChanged` событие запускается.  Событие запускается перед начальным сценарием при загрузке `ContentLoading` нового документа.  
    
*   Добавлена поддержка архитектуры ARM64.  
*   Добавлена поддержка панели мягкого ввода \(SIP\) для устройств с сенсорным экраном.  
*   Добавлена поддержка Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 и Windows Server 2016.  
*   Добавлено [уведомление NotifyParentWindowPositionChanged][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] для окна состояния, чтобы следовать за окном в оконном режиме.  Кроме того, реализуем изменение в режиме без окон, чтобы функции со специальными возможностями работали.  
*   Добавлен [параметр AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] для глобального управления возможностью доступа к веб-странице любыми удаленными объектами.  По умолчанию он включен, поэтому удаленные объекты, добавленные `AreRemoteObjectsAllowed` [addRemoteObject,][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] доступны на веб-странице.  При `AreRemoteObjectsAllowed` отключлении объекты недоступны с веб-страницы.  Изменения применяются к следующему событию навигации.  
*   Добавлен [параметр IsZoomControlEnabled,][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] чтобы запретить пользователям влиять на масштаб WebView с помощью и `ctrl` + `+` `ctrl` + `-` \(или `ctrl` + колесиком мыши\).  Масштабирование может по-прежнему устанавливаться с [put_ZoomFactor,][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] если параметр отключен.  
*   Изменен ZoomFactor, чтобы применить его только к текущему webView.  Изменение масштаба текущего webView не влияет на другие веб-просмотры, которые вы переходили на тот же сайт источника.  Дополнительные сведения можно найти в [get_ZoomFactor.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Добавлена [настройка SetBoundsAndZoomFactor.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]  Теперь вы можете одновременно установить коэффициент масштабирования и границы WebView.  
*   Добавлено [событие WindowCloseRequested.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]  Дополнительные сведения см. [в add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Добавлена поддержка типа диалоговых окно для событий диалоговых окно JavaScript и `beforeunload` добавлена [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] записи.  
*   Добавлены [getHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] для HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] для HttpResponseHeaders и [get_HasCurrentHeader][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] в HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Breaking Change**: Modified `DevToolsProtocolEventReceived` behavior.  Теперь вы можете создать [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] для определенного события протокола DevTools и подписаться на такое событие или отписаться от него с помощью [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived.][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: `WebMessageReceivedEventArgs` [changed get_WebMessageAsString][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] property to a [TryGetWebMessageAsString][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring] method.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Changed `AcceleratorKeyPressedEventArgs` [Handle][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] method to a [get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] property.  
    
## 0.8.355  

[Пакет NuGet][NuGetGallery0.8.355] \| Microsoft Edge версии 80.0.355.0.  

*   Выпущен пример WebView2API, полное руководство по SDK WebView2.  Дополнительные сведения можно найти в [примере API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Добавлена поддержка IME для всех языков, кроме английского[(#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Обновлена поверхность API события `WebResourceRequested` в ответ на отчеты об ошибках.  Одновременное указание фильтра и события при создании теперь является неподготовленным.  Чтобы создать событие, запрашиваемого [][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] веб-ресурсом, используйте add_WebResourceRequested для добавления события, а [AddWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] — для добавления фильтра.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] удаляет фильтр \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Modified fullscreen behavior.  Неподготовленный [IsFullScreenAllowed.][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]  Теперь, по умолчанию, если элемент в WebView \(например, видео\) имеет полноэкранный режим, он заполняет границы WebView.  Используйте событие [ContainsFullScreenElementChanged][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] и get_ContainsFullScreenElement, чтобы указать, как приложение должно издать webView, если элемент хочет зайти в полноэкранный режим. [][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]  
    
## 0.8.314  

[Пакет NuGet][NuGetGallery0.8.314] \| Microsoft Edge версии 80.0.314.0.  

*   Добавлена поддержка Windows 7, Windows 8 и Windows 8.1.  
*   Добавлена Visual Studio и Visual Studio отлажки кода для WebView2.  Теперь отлаговка скрипта в WebView2 прямо из IDE.  Для получения дополнительных сведений перейдите к how [to debug when developing with WebView2 controls][Webview2HowtoDebug].  
*   Добавлен для запуска сценария в WebView2 для доступа к объекту IDispatch из компонента Win32 приложения и доступа к свойствам объекта `Native Object Injection` IDispatch.  Дополнительные сведения см. в [addRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения см. [в add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Отключение `Context Menus` .  Дополнительные сведения см. [в put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   `DPI Awareness`Обновлено.  Теперь осведомленность о DPI WebView такая же, как и осведомленность о DPI ведущего приложения.  
    
    > [!NOTE]
    > Если запущено другое гибридное приложение с другими уровнями DPI, чем у исходного WebView, новое WebView не будет запущено, если то же `user data folder` самое \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Обновлено таким образом, что WebView2 автоматически отклоняет запросы на разрешение уведомлений, запрашиваемую веб-контентом, которое было в `Notification Change Behavior` Веб-просмотре.  
    
## 0.8.270  

[Пакет NuGet][NuGetGallery0.8.270] \| Microsoft Edge версии 78.0.270.0.  

*   Добавлено событие, которое указывает на изменение `DocumentTitleChanged` названия документа[\( \#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Добавлен `GetWebView2BrowserVersionInfo` API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Добавлено `NewWindowRequested` событие.  
*   Обновлена `CreateWebView2EnvironmentWithDetails` функция для `releaseChannelPreference` удаления.  Дополнительные сведения о функции можно найти в `CreateWebView2EnvironmentWithDetails` [createWebView2EnvironmentWithDetails.][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]  Переопределения переменных реестра и среды по-прежнему поддерживается.  Параметр канала по умолчанию используется без переопределения.  
    Во время поиска канала команда WebView пропускает предыдущую версию канала, несовместимую с SDK WebView2.  
    Команда WebView выбирает более стабильный канал, чтобы обеспечить наиболее согласованное поведение для пользователя.  При проверке с последними сборками Canary необходимо создать сценарий, чтобы настроить переменную среды перед `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` запуском приложения.  
*   Обновлена функция `CreateWebView2EnvironmentWithDetails` с логикой `userDataFolder` выбора, если она не указана.  Дополнительные сведения о функции можно найти в `CreateWebView2EnvironmentWithDetails` [createWebView2EnvironmentWithDetails.][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]  Если ранее вы использовали расположение по умолчанию, при переходе на новый SDK по умолчанию сбрасывается \(задайте новое расположение в каталоге кода хоста\) и состояние также `userDataFolder` `userDataFolder` сбрасывается.  Если у ведущего процесса нет разрешения на записи в указанный каталог, функция `CreateWebView2EnvironmentWithDetails` может не работать.  Вы можете скопировать данные из старого каталога `user data folder` в новый.  
    
## 0.8.230  

[Пакет NuGet][NuGetGallery0.8.230] \| Microsoft Edge версии 77.0.230.0.  

*   Добавлен API для остановки всех переходов и ожидающих извлечений `Stop` ресурсов \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Добавлен `.tlb` файл в пакет NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Добавлены проекты .NET в список установщика в пакете NuGet \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## 0.8.190  

[Пакет NuGet][NuGetGallery0.8.190] \| Microsoft Edge версии 77.0.190.0.  

*   Добавлено для управления тем, могут ли пользователи `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` открывать DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Добавлено для управления отображением панели состояния `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Добавлено `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` для перемещения назад и вперед по истории навигации.  
*   Добавлены типы http-загоров \( \) для просмотра и изменения `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` http-загоров в WebView.  
*   Добавлена 32-битная поддержка WebView на 64-битных компьютерах[\( \#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Добавлен iDL WebView в SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Добавлена библиотека для поддержки `IID\_\*` объектов ID интерфейса[\( \#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Добавлены путь, связывание и автообъеки DLL-файлов с файлом NuGet `TARGET` в SDK.  
*   Включен запрос в `window.open()` сценарии.  
    
## 0.8.149  

[Пакет NuGet][NuGetGallery0.8.149] \| Microsoft Edge версии 76.0.149.0.  

Начальный предварительный выпуск для разработчиков.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Распределение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Постоянное распространение в режиме распространения — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Режим распространения фиксированной версии — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "В этой теме поймут, что используется в средстве webView2 Runtime и установщике — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Групповые политики для WebView2 : управление приложениями WebView2 | Документы Майкрософт"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Understanding browser versions and WebView2 | Документы Майкрософт"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Экспериментальные API- и веб-| Документы Майкрософт"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Соответствие версиям времени работы WebView2 — понимание версий SDK WebView2 | Документы Майкрософт"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях Windows Forms | Документы Майкрософт"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF | Документы Майкрософт"  
[Webview2HowtoDebug]: ./howto/debug.md "Отлагивание при разработке с помощью элементов управления WebView2 | Документы Майкрософт"  

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded интерфейс ICoreWebView2_2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping — интерфейс ICoreWebView2_3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend — интерфейс ICoreWebview2_3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "интерфейс ICoreWebView2CompositionController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor интерфейс ICoreWebView2Controller2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest — интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled интерфейс ICoreWebView2ExperimentalEnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures — интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalPointerInfo | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent интерфейс ICoreWebView2ExperimentalSettings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWindowFeatures | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader — интерфейс ICoreWebView2HttpHeadersCollectionIterator | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders — интерфейс ICoreWebView2HttpRequestHeaders | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader — интерфейс ICoreWebView2HttpResponseHeaders | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures интерфейс ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString — интерфейс ICoreWebView2WebMessageReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke — интерфейс ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "интерфейс ICoreWebView2WindowFeatures | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle — интерфейс IWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "интерфейс IWebView2ContainsFullScreenElementChangedEventHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled интерфейс IWebView2Settings2 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated интерфейс IWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString интерфейс IWebView2WebMessageReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed интерфейс IWebView2WebView4 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс IWebView2WebView4 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged интерфейс IWebView2WebView | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge — политика | Документы Майкрософт"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 — политики | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft.Web.WebView2.Core | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Класс CoreWebView2 (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Класс CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment.CompareBrowserVersions(String, String) Method (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Метод CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Класс CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Класс CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Событие CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2.ScriptDialogOpening Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Класс CoreWebView2InitializationCompletedEventArgs | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft.Web.WebView2.WinForms | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Класс CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Класс Webview2.Source (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft.Web.WebView2.Wpf | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2.BuildWindowCore(HandleRef) Method (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Метод WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Класс CancelEventArgs (System.ComponentModel) | Документы Майкрософт"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Класс EventArgs (System) | Документы Майкрософт"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Сборки со | Документы Майкрософт"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Application Guard в Microsoft Defender (Windows 10) — безопасность Windows | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Репо для MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Пример API WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Перемещение проекта на использование последней версии WebView2 SDK 0.9.430 — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 878"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Объявление об общей доступности Microsoft Edge WebView2 для .NET и фиксированного метода распространения | блоге .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Microsoft Edge"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Коллекции NuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 0.9.515"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 0.9.628"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Коллекции NuGet | Microsoft.Web.WebView2 1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Коллекции NuGet | Microsoft.Web.WebView2 1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Коллекции NuGet | Microsoft.Web.WebView2 1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.674"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Коллекции NuGet | Microsoft.Web.WebView2 1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.721"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.790"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Объявление об общей доступности Microsoft Edge WebView2 | Блог Microsoft Edge"  
