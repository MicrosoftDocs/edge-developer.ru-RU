---
description: Заметки о выпуске microsoft Edge WebView2 SDK
title: Заметки о выпуске Для Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, элемент управления браузером, edge html
ms.openlocfilehash: 43df4c6155350881059fc6ca7f6fe3a047ba0f12
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327640"
---
# Заметки о выпуске webView2 SDK  

Команда WebView2 обновляет [SDK WebView2][NuGetGallery] в течение шести недель.  Просмотрите следующие материалы, чтобы получить последние сведения об объявлениях, добавлениях, изменениях и вносимых в API изменений.  

> [!NOTE]
> Убедитесь, что приложение повторно скомпилировать после обновления пакета NuGet.  Команда рекомендует использовать канал Canary при разработке с использованием пакетов предварительного выпуска, а также невторяемую времени работы при использовании выпущенных пакетов.  Для получения дополнительных сведений перейдите к [versioning][VersioningDoc].  
 
## 1.0.790-предварительнаяrelease  

Дата выпуска: 10 февраля 2021 г.  

[Пакет NuGet][NuGetGallery1.0.790-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

### Общие  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release package 1.0.781 is deprecated.  Прекратите разработку с помощью этого пакета.  

> [!IMPORTANT]
> Предварительный пакет WebView2 0.9.430 является неподготовленным и удаляется из предстоящего выпуска.  Если ваше приложение WebView использует пакет, рекомендуется обновить его до более нового.  

##### Функции  

*   Добавлены [методы TrySuspend и Resume][ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume] для приостановки и возобновления WebViews.  
*   Добавлен [метод SetVirtualHostNameToFolderMapping,][ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping] который соповедет имя виртуального хоста с путем каталога.  \([\#37,][GithubMicrosoftedgeWebviewfeedbackIssue37] [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]и [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Добавлено [свойство DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor] для настройки цвета и альфа-канала фона.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Добавлено [свойство UserAgent,][ReferenceWin32Icorewebview2experimentalsettings10790PreReleaseGetUserAgent] чтобы получить или установить агент пользователя.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).
*   Метод заменен `CreateCookieWithCookie` `CopyCookie` методом.  
*   Добавлена поддержка визуального размещения с помощью интерфейса [ICoreWebView2CompositionController,][ReferenceWin32Icorewebview2controllerViewWebview210790CompositionController] который создается с помощью нового `CreateCoreWebView2CompositionController` `ICoreWebView2Environment3` метода.  

    
##### Исправления ошибок  

*   Отключена функция покупок в Microsoft Edge в WebView2.  
*   Отключено контекстное меню в представлении PDF, когда `AreDefaultContextMenusEnabled` это `false` так.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Исправлена ошибка, возвращаемая `E_NOINTERFACE` при `ICoreWebView2` `ICoreWebView2Experimental` запросе.  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Исправлена ошибка, разрешив навигацию с неправильно отформатированной ЮРИС, `CoreWebView2NavigationStartingEventArgs.Cancel` когда было установлено его. `false`  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Исправлена ошибка, заблокированная во всплывающих окнах с подключенными к событиям `window.print()` обработчиками `NewWindowRequested` событий.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Исправлена проблема динамического DPI при перемещении приложений между разными мониторами.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Улучшены значения, переданные `HRESULT` [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke.][ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10790]  
*   Отключена кнопка управления автозаполненными возможностями.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\). 
*   Исправлена Visual Studio при сбоях при `WebView2.Dispose` вызове в нескольких окнах.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\ и [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Исправлена ошибка, из-за Visual Studio webView2.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\). 
*   Снижение высокой нагрузки на ЦП.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Исправлены проблемы с нерекометентным пакетом предварительного выпуска 1.0.781. [\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [и \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
##### Рекламные акции  

*   Следующие экспериментальные API теперь повышены до Stable.  
    *   API визуального размещения.  
    *   [SetVirtualHostNameToFolderMapping][ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping]  
    *   [TrySuspend и Resume][ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume]  
    *   [DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor]  
    
#### .NET  

##### Исправления ошибок  

*   Исправлена ошибка, которая сбой приложений WebView, которые используют WPF SDK.  Сбой произошел, когда окна были закрыты с помощью клавиши F4.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Теперь экран инициализации WebView2 прозрачный, а не серый.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## 1.0.705.50  

Дата выпуска: 25 января 2021 г.  

[Пакет NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime version 86.0.616.0 or newer  

##### Рекламные акции  

*   Следующие экспериментальные API теперь повышены до Stable.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API управления файлами cookie][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [Свойство WebView Environment][WebViewEnvironmentproperty]  

## 1.0.721-предварительнаяrelease  

Дата выпуска: 8 декабря 2020 г.  

[Пакет NuGet][NuGetGallery1.0.721-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

#### Общие  

> [!IMPORTANT]
> **Breaking Change**: WebView2 pre-release packages 1.0.707 and 0.9.628 are deprecated.  Прекратите разработку с помощью этих пакетов.  

###### Функции  

*   Добавлены [групповые политики WebView2.][DeployedgeMicrosoftEdgeWebviewPolicies]  Дополнительные сведения о рекомендуемых методиках можно найти в групповых [политиках для WebView2.][Webview2ConceptsEnterpriseGroupPoliciesForWebview2]  
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated the old registry location.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Добавлена поддержка [перетаскивания][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] в WebView2.  
*   Добавлены API для обработки поддержки DPI.  
    *   Добавлено [свойство RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] для изменения масштаба DPI для содержимого WebView и всплывающих папок пользовательского интерфейса, а также связанного события [RasterizationScaleChanged.][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]  
    *   Добавлено [свойство ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges] для автоматического обновления `RasterizationScale` свойства при необходимости.  
    *   Добавлено свойство [BoundsMode,][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode] указывав, что границы являются пикселями логики и позволяют WebView использовать для отображения пикселей WebView2, а WebView использует его для получения `RasterizationScale` `RasterizationScale` `Bounds` физического размера.  
*   Обновлено `NewWindowRequested` событие для обработки и `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] и [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Следующие экспериментальные API теперь повышены до Stable.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API управления файлами cookie][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [Свойство WebView Environment][WebViewEnvironmentproperty]  
        
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
    
## 1.0.674-prerelease  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

*   Добавлен [метод NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] для предоставления данных о публикации или других заголовок запросов во время навигации.  
*   Добавлено [событие DOMContentLoaded,][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] которое запускается при загрузке и разбике исходного HTML-документа.  
*   Добавлено [свойство Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] в WebView2.  Это свойство предоставляет доступ к среде WebView2, в которой был создан экземпляр WebView2.  
*   Добавлены [API управления][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] файлами cookie, позволяющие разработчикам проверить подлинность сеанса WebView2 или получить файлы cookie из WebView для проверки подлинности других средств.  Группа Webview планирует внести улучшения в язык или структуру.  Для получения дополнительных сведений перейдите к [обзору API: управление файлами cookie.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Обновлено событие [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] и добавлены непрерывная [webResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] и [WebResourceResponseReceivedEventArgs::P opulateResponseContent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] в [WebResourceResponseView::GetContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].  
*   [Отключение Application Guard в Microsoft Defender (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] в WebView2.  
*   Добавлен [SystemCursorId для][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] визуального размещения.  
*   Добавлена исправлена ошибка для метода Input в визуальном размещении.  
*   Удалены требования к использованию `version.lib` статической библиотеки WebView2.  
    
#### .NET  

*   Обновлен класс [CoreWebView2,][DotnetApiMicrosoftWebWebview2CoreCorewebview2] чтобы показать `CoreWebView2Environment` переменную.  
*   Изменены реализации пользовательских классов EventArgs в пространстве имен на подклассы `Microsoft.Web.WebView2.Core` [System.EventArgs][DotnetApiSystemEventargs] [или System.ComponentModel.CancelEventArgs.][DotnetApiSystemComponentmodelCancelEventargs]  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Добавлена поддержка [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] в WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   Добавлены [API WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Обновлено свойство "Источник [конструктора][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] WinForms" по умолчанию или значение null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
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
*   [Режим фиксированной версии][Webview2ConceptsDistributionFixedVersionMode] доступен для предварительной версии разработчика.  
    
## 0.9.622.11  

Дата выпуска: 10 сентября 2020 г.  

[Пакет NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

#### Общие  

*   > [!IMPORTANT]
    > **Announcement**: this SDK is the Release Candidate for WebView2 Win32 C/C++ GA.  Версия ga должна использовать одинаковый интерфейс API и функции.  
    
*   Отключенные [политики браузера.][DeployedgeMicrosoftEdgePolicies]  
*   Добавлено [свойство AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Включено `ICoreWebView2NewWindowRequestedEventArgs` свойство [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] и связанное [с ним свойство ICoreWebView2WindowFeatures.][ReferenceWin32Icorewebview2windowfeatures09622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Обновлено `System.Windows.Rect`  для использования вместо `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Обновлено событие NewWindowRequested для обработки `window.open()` запроса без параметров.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Указанные параметры AdditionalBrowserArguments][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] не переопределяются переменными среды `ICoreWebView2EnvironmentOptions` или значениями реестра.  Дополнительные сведения можно найти в [createCoreWebView2EnvironmentWithOptions.][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]  
    
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
*   Отключено блокатор всплывающих блоков в WebView.  Для получения дополнительных сведений перейдите к [свойству IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] `NewWindowRequested` в событии.  
*   Убедитесь, что событие запуска навигации WebView запускается для `about:blank` .  Теперь события запускаются для всей навигации, но отмены для `NavigationStarting` `about:blank` или iframe `srcdoc` не поддерживаются и игнорируются.  
*   Блокировал некоторые `edge://` схемы URI в WebView.  
*   Добавлено экспериментальное свойство [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Добавлено экспериментальное событие [WebResourceResponseReceived,][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] которое запускается после получения и обработки WebView ответа от запроса WebResource.  В объект отклика включаются заглавные и при их настоятели проверки подлинности.  
    
#### .NET  

*   Улучшена обработка фокуса WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Добавлено `ZoomFactor` свойство контроллера WPF Webview2.  
    
## 0.9.538  

[Пакет NuGet][NuGetGallery0.9.538] \| Microsoft Edge версии 85.0.538.0.  

#### Общие  

*   Поддержка WebView2 SDK версии [0.8.149.](#08149)  WebView2 рекомендует быть в курсе последних версий WebView2.  
*   Обновлена групповая политика с учетом времени изменения пути профиля браузера Microsoft Edge \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
#### Win32 C/C++  

*   Добавлен [iCoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures,][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]который срабжает при запуске и связи с `window.open()` [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] and replaced with [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
    
*   > [!IMPORTANT]
    > **Нарушение изменений:** чтобы обеспечить соответствие API WebView2 соглашениям об именовыванию API Windows, команда WebView обновила имена следующих приложений.  
    > 
    > *   [AreRemoteObjectsAllowed теперь][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] [— AreHostObjectsAllowed.][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]  
    
*   Обновлено [addHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538].  Исходные маркеры сериализатора объектов хост-сервера теперь устанавливаются на прокси-объекты.  Затем маркеры сериализации объектов хост-объекта сериализируются обратно в качестве хост-объекта, когда передаются в качестве параметра в обратном вызове JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
#### .NET (предварительная версия 0.9.538)  

*   Выпущены winForms и примеры WPF WebView2API, которые являются полными руководствами по SDK WebView2.  Для получения дополнительных сведений перейдите в [репо примеры][GithubMicrosoftedgeWebview2samplesMain].  
*   Добавлена поддержка экспериментальных API визуального размещения [и][ConceptsVersioningExperimentalApis]окон.  
*   > [!IMPORTANT]
    > **Breaking Change**: The following deferrals now implement IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested], and [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Добавлены [getAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] и [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] в качестве статических средств [CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## 0.9.515-предварительнаяrelease  

[Пакет NuGet][NuGetGallery0.9.515-prerelease] \| Microsoft Edge версии 84.0.515.0.  

*   > [!IMPORTANT]
    > **Announcement**: WebView2 now supports Windows Forms and WPF on .NET Framework 4.6.2 or later and .NET Core 3.0 or later in the **pre-release package**.  
    
*   Дополнительные сведения о создании приложений WPF можно найти в руководстве по началу работы [с WPF][GettingstartedWpf] и справочнике [по WPF WebView2][DotnetApiMicrosoftWebWebview2Wpf] для API, характерных для WPF.  
*   Дополнительные сведения о создании приложений Windows Forms можно найти в руководстве по началу работы с [Windows Forms][GettingstartedWinforms] и справочнике по формам [Windows][DotnetApiMicrosoftWebWebview2Winforms] WebView2 для API Windows Forms.  
*   Дополнительные сведения об API CoreWebView2 можно найти в [справочнике по .NET.][DotnetApiMicrosoftWebWebview2Core]  
*   > [!CAUTION]
    > **Известные проблемы:** команда WebView знает о некоторых проблемах в предварительной версии, которые будут устранены в будущих выпусках.  
    > 
    > *   **Информирование о DPI:** WebView2 для WPF в настоящее время не знает О DPI.  При инициализации WebView2 на мониторах с высоким DPI существует известная проблема, из-за которой WebView сначала инициализируется как доля окна до тех пор, пока размер окна не будет меняться.  
    > *   **Конструктор WPF**: конструктор WPF в настоящее время не поддерживается.  Добавьте в приложение соответствующий XAML-код, непосредственно изменяя его в текстовом редакторе.  
    
## 0.9.488  

[Пакет NuGet][NuGetGallery0.9.488] \| Microsoft Edge версии 84.0.488.0.  

*   > [!IMPORTANT]
    > **Announcement**: Starting with thecoming Microsoft Edge version 83, Evergreen WebView no longer targets the Stable browser channel.  Вместо этого он ориентирован на другой набор binaries, с фирменным названием [Evergreen WebView2 Runtime,][ConceptsDistributionEvergreenMode]которые можно установить цепочкой с помощью установщика, разрабатываемого командой WebView.  Дополнительные сведения можно найти в [app-Distribution.][ConceptsDistribution]  
    
*   > [!IMPORTANT]
    > **Announcement**: Moving forward, the WebView team releases two packages: a pre-release package with experimental API \(for you to try out\) and a stable release package with stable APIs \(for your confidence\).  Чтобы узнать о различиях, перейдите к [данным о версиях браузера и WebView2.][ConceptsVersioning]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Чтобы обеспечить соответствие API WebView2 соглашениям об именованию API Windows, команда WebView обновила имена следующих интерфейсов.  
    > 
    > *   `CORE_WEBVIEW2_*` теперь есть префикс `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] теперь [— GetAvailableCoreWebView2BrowserVersionString.][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] [теперь][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]get_BrowserVersionString.  
    > *   [AddRemoteObject теперь][ReferenceWin32Icorewebview2Addremoteobject09430] [является AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] теперь [является RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
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
    > **Breaking Change**: Deprecated [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] and replaced with [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
    
*   Добавлено [событие FrameNavigationCompleted.][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]  Теперь, когда iframe завершает навигацию, происходит событие, которое возвращает успешность навигации и ее ИД.  
*   Добавлен [интерфейс ICoreWebView2EnvironmentOptions,][ReferenceWin32Icorewebview2environmentoptions09488] который можно использовать для определения версии времени выполнения WebView2, нацеленной на ваше приложение.  
*   Добавлен [параметр IsBuiltInErrorPageEnabled.][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]  Теперь можно включить или отключить встроенную веб-страницу ошибки для сбоя навигации и сбоя процесса отрисовки.  
*   Обновлено внедрение удаленных объектов для поддержки реализаций .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Обновлено [событие NewWindowRequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] для обработки запросов из контекстных меню \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Выпущен первый отдельный предварительный пакет WebView2, в котором можно получить доступ к API визуального размещения.  Команда WebView обновила [APISample,][GithubMicrosoftedgeWebview2samplesMain] включив новые экспериментальные API.  
    
    *   Добавлен [интерфейс ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] для подключения к дереву композиции и предоставления входных данных для WebView.  
    *   Добавлен [iCoreWebView2ExperimentalPointerInfo,][ReferenceWin32Icorewebview2experimentalpointerinfo09488]который содержит все сведения из `POINTER_INFO` .  Этот объект передается в SendPointerInput для ввода ввода указателя в WebView.  
    *   Добавлен [iCoreWebView2ExperimentalCursorChangedEventHandler,][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]который сообщает приложению, когда следует изменить курсор мыши над WebView.  При нацелии мыши на текстовое поле в WebView курсор изменяется со стрелки на селектор.  Свойство в приложении сообщает приложению, каким должен быть курсор мыши в настоящее время `cursor` `CompositionController` для WebView.  
    
## 0.9.430  

[Пакет NuGet][NuGetGallery0.9.430] \| Microsoft Edge версии 82.0.430.0.  

WebView2 SDK является официальной бета-версией Win32 C++, которая включает несколько запросов функций из отзывов.  Команда WebView пытается ограничить количество выпусков, внося в них существенные изменения.  По мере приближения к общей доступности в бета-версию включено несколько существенных существенных изменений.  

*   > [!IMPORTANT]
    > **Breaking Change**: As the final release approaches the WebView team renamed the prefix *IWebView2WebView*   to *ICoreWebView2*   in order to make sure the WebView2 API aligns with the Windows API naming convention.  Кроме того, чтобы использовать SDK WebView2 из структур пользовательского интерфейса, группа WebView разделилась на `ICoreWebView2` [ICoreWebView2][ReferenceWin32Icorewebview209430] и [ICoreWebView2Host.][ReferenceWin32Icorewebview2host09430]  `ICoreWebView2Host` поддерживается размер, отображение и скрытие, фокус и другие функции, связанные с окнами и композицией.  ICoreWebView2 поддерживает все остальные функции WebView2.  Чтобы узнать больше о внедрении изменений, [][GithubMicrosoftedgeWebview2samplesPr17] перейдите к запросу на включение WebView2 в проект [WebView2 APISample.][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Split [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] into three components:  [SourceChanged,][ReferenceWin32Icorewebview2AddSourcechanged09430] [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430], and [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  Теперь, когда исходный URL-адрес `SourceChanged` изменяет, событие будет запускаться.  При смене состояния истории `HistoryChanged` событие запускается.  Событие запускается перед начальным сценарием при загрузке `ContentLoading` нового документа.  
    
*   Добавлена поддержка архитектуры ARM64.  
*   Добавлена поддержка панели мягкого ввода \(SIP\) для устройств с сенсорным экраном.  
*   Добавлена поддержка Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 и Windows Server 2016.  
*   Добавлено [уведомление NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430] для окна состояния, чтобы следовать за окном в оконном режиме.  Кроме того, реализуем изменение в режиме без окон, чтобы функции со специальными возможностями работали.  
*   Добавлен [параметр AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] для глобального управления возможностью доступа к веб-странице любыми удаленными объектами.  По умолчанию он включен, поэтому удаленные объекты, добавленные `AreRemoteObjectsAllowed` [addRemoteObject,][ReferenceWin32Icorewebview2Addremoteobject09430] доступны на веб-странице.  При `AreRemoteObjectsAllowed` отключлении объекты недоступны с веб-страницы.  Изменения применяются к следующему событию навигации.  
*   Добавлен [параметр IsZoomControlEnabled,][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] чтобы запретить пользователям влиять на масштаб WebView с помощью `ctrl` + `+` и `ctrl` + `-` \(или `ctrl` + колесиком мыши\).  Масштабирование может по-прежнему устанавливаться с [put_ZoomFactor,][ReferenceWin32Icorewebview2hostPutZoomfactor09430] если параметр отключен.  
*   Изменен ZoomFactor, чтобы применить его только к текущему webView.  Изменение масштаба текущего webView не влияет на другие веб-просмотры, которые вы переходили на тот же сайт источника.  Дополнительные сведения можно найти в [get_ZoomFactor.][ReferenceWin32Icorewebview2hostGetZoomfactor09430]  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Добавлена [настройка SetBoundsAndZoomFactor.][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]  Теперь вы можете одновременно установить коэффициент масштабирования и границы WebView.  
*   Добавлено [событие WindowCloseRequested.][ReferenceWin32Icorewebview2AddWindowcloserequested09430]  Дополнительные сведения см. в [add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Добавлена поддержка типа диалоговых окно для событий диалоговых окно JavaScript и `beforeunload` добавлена [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] записи.  
*   Добавлены [getHeaders][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] для HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] для HttpResponseHeaders и [get_HasCurrentHeader][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] в HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Breaking Change**: Modified `DevToolsProtocolEventReceived` behavior.  Теперь вы можете создать [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] для определенного события Протокола DevTools и подписаться на такое событие или отписаться от него с помощью [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived.][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]  
    
*   > [!IMPORTANT]
    > **Breaking Change** `WebMessageReceivedEventArgs` [: changed get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] property to a [TryGetWebMessageAsString][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430] method.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Changed `AcceleratorKeyPressedEventArgs` [Handle][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] method to a [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] property.  
    
## 0.8.355  

[Пакет NuGet][NuGetGallery0.8.355] \| Microsoft Edge версии 80.0.355.0.  

*   Выпущен пример WebView2API, полное руководство по SDK WebView2.  Дополнительные сведения можно найти в [примере API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Добавлена поддержка IME для всех языков, кроме английского[(#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Обновлена поверхность API события `WebResourceRequested` в ответ на отчеты об ошибках.  Одновременное указание фильтра и события при создании теперь является неподготовленным.  Чтобы создать запрашиваемого события [][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] веб-ресурса, используйте add_WebResourceRequested добавить событие и [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] для добавления фильтра.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] удаляет фильтр \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change**: Modified fullscreen behavior.  Неподготовленный [IsFullScreenAllowed.][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]  Теперь, по умолчанию, если элемент в WebView \(например, видео\) имеет полноэкранный режим, он заполняет границы WebView.  Используйте событие [ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] и get_ContainsFullScreenElement, чтобы указать, как приложение должно менять его в том случае, если элемент хочет зайти в полноэкранный режим. [][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]  
    
## 0.8.314  

[Пакет NuGet][NuGetGallery0.8.314] \| Microsoft Edge версии 80.0.314.0.  

*   Добавлена поддержка Windows 7, Windows 8 и Windows 8.1.  
*   Добавлена Visual Studio и Visual Studio webView2.  Теперь отлаговка скрипта в WebView2 прямо из IDE.  Для получения дополнительных сведений перейдите к how [to debug when developing with WebView2 controls][HowtoDebug].  
*   Добавлен для запуска сценария в WebView2 для доступа к объекту IDispatch из компонента Win32 приложения и доступа к свойствам объекта `Native Object Injection` IDispatch.  Дополнительные сведения см. в [addRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения см. [в add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Отключение `Context Menus` .  Дополнительные сведения см. [в put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   `DPI Awareness`Обновлено.  Теперь осведомленность о DPI WebView такая же, как и осведомленность о DPI ведущего приложения.  
    
    > [!NOTE]
    > Если запущено другое гибридное приложение с другими уровнями DPI, чем у исходного WebView, новое WebView не будет запущено, если то же `user data folder` самое \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Обновлено таким образом, что WebView2 автоматически отклоняет запросы на разрешение уведомлений, запрашиваемую веб-контентом, которое было в `Notification Change Behavior` Веб-просмотре.  
    
## 0.8.270  

[Пакет NuGet][NuGetGallery0.8.270] \| Microsoft Edge версии 78.0.270.0.  

*   Добавлено событие, которое указывает на изменение `DocumentTitleChanged` названия документа[\( \#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Добавлен `GetWebView2BrowserVersionInfo` API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Добавлено `NewWindowRequested` событие.  
*   Обновлена `CreateWebView2EnvironmentWithDetails` функция для `releaseChannelPreference` удаления.  Дополнительные сведения о функции можно найти в `CreateWebView2EnvironmentWithDetails` [createWebView2EnvironmentWithDetails.][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]  Переопределения переменных реестра и среды по-прежнему поддерживается.  Параметр канала по умолчанию используется без переопределения.  
    Во время поиска канала команда WebView пропускает предыдущую версию канала, несовместимую с SDK WebView2.  
    Команда WebView выбирает более стабильный канал, чтобы обеспечить наиболее согласованное поведение для пользователя.  При проверке с помощью последних сборки Canary необходимо создать сценарий, чтобы настроить переменную среды перед `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` запуском приложения.  
*   Обновлена функция `CreateWebView2EnvironmentWithDetails` с логикой `userDataFolder` выбора, если она не указана.  Дополнительные сведения о функции можно найти в `CreateWebView2EnvironmentWithDetails` [createWebView2EnvironmentWithDetails.][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]  Если ранее вы использовали расположение по умолчанию, при переходе на новый SDK по умолчанию сбрасывается \(устанавливается новое расположение в каталоге кода хост-кода\) и состояние также `userDataFolder` `userDataFolder` сбрасывается.  Если у ведущего процесса нет разрешения на записи в указанный каталог, функция `CreateWebView2EnvironmentWithDetails` может не работать.  Вы можете скопировать данные из старого каталога `user data folder` в новый.  
    
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

[VersioningDoc]: ./concepts/versioning.md#matching-webview2-runtime-versions
[ConceptsDistribution]: ./concepts/distribution.md "Распределение приложений с помощью WebView2 | Документы Майкрософт"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Постоянное распространение в режиме распространения — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Режим распространения фиксированной версии — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "В этой теме поймут, что используется в средстве webView2 Runtime и установщике — распространение приложений с помощью WebView2 | Документы Майкрософт"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Групповые политики для WebView2 : управление приложениями WebView2 | Документы Майкрософт"  
[ConceptsVersioning]: ./concepts/versioning.md "Understanding browser versions and WebView2 | Документы Майкрософт"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Экспериментальные API- и веб-| Документы Майкрософт"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях Windows Forms | Документы Майкрософт"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF | Документы Майкрософт"  
[HowtoDebug]: ./howto/debug.md "Отлагивание при разработке с помощью элементов управления WebView2 | Документы Майкрософт"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle — интерфейс IWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "интерфейс IWebView2ContainsFullScreenElementChangedEventHandler | Документы Майкрософт"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled интерфейс IWebView2Settings2 | Документы Майкрософт"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated интерфейс IWebView2Settings | Документы Майкрософт"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString интерфейс IWebView2WebMessageReceivedEventArgs | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed интерфейс IWebView2WebView4 | Документы Майкрософт"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged интерфейс IWebView2WebView | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс IWebView2WebView4 | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested — интерфейс IWebView2WebView5 | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement интерфейс IWebView2WebView5 | Документы Майкрософт"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails — глобальные | Документы Майкрософт"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled — интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo интерфейс ICoreWebView2Environment | Документы Майкрософт"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2Host | Документы Майкрософт"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo — глобальные | Документы Майкрософт"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor интерфейс ICoreWebView2Host | Документы Майкрософт"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged — интерфейс ICoreWebView2Host | Документы Майкрософт"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor интерфейс ICoreWebView2Host | Документы Майкрософт"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor — интерфейс ICoreWebView2Host | Документы Майкрософт"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader интерфейс ICoreWebView2HttpHeadersCollectionIterator | Документы Майкрософт"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders — интерфейс ICoreWebView2HttpRequestHeaders | Документы Майкрософт"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader — интерфейс ICoreWebView2HttpResponseHeaders | Документы Майкрософт"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed — интерфейс ICoreWebView2Settings | Документы Майкрософт"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled интерфейс ICoreWebView2Settings | Документы Майкрософт"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString — интерфейс ICoreWebView2WebMessageReceivedEventArgs | Документы Майкрософт"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Документы Майкрософт"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Майкрософт"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalPointerInfo | Документы Майкрософт"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed — интерфейс ICoreWebView2Settings | Документы Майкрософт"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Документы Майкрософт"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails — глобальные | Документы Майкрософт"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Документы Майкрософт"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString — глобальные | Документы Майкрософт"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft.Web.WebView2.Core | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft.Web.WebView2.Wpf | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft.Web.WebView2.WinForms | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Класс CoreWebView2 (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Класс CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment.CompareBrowserVersions(String, String) Method (Microsoft.Web.WebView2.Core) | Документы Майкрософт"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Метод CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2.PermissionRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "CoreWebView2.ScriptDialogOpening Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Класс CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Класс CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Класс CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Класс Webview2.Source (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2.BuildWindowCore(HandleRef) Method (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Метод WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Класс CoreWebView2InitializationCompletedEventArgs | Документы Майкрософт"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled интерфейс ICoreWebView2ExperimentalEnvironmentOptions | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures — интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWindowFeatures | Документы Майкрософт"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed интерфейс ICoreWebView2Settings | Документы Майкрософт"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Документы Майкрософт"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures интерфейс ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "интерфейс ICoreWebView2WindowFeatures | Документы Майкрософт"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions — глобальные | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalEnvironment | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Документы Майкрософт"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest — интерфейс ICoreWebView2Experimental | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController3 | Документы Майкрософт"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge — политика | Документы Майкрософт"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 — политика | Документы Майкрософт"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Application Guard в Microsoft Defender (Windows 10) — безопасность Windows | Документы Майкрософт"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Класс CancelEventArgs (System.ComponentModel) | Документы Майкрософт"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Класс EventArgs (System) | Документы Майкрософт"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Сборки со | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 250"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 288"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 611"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repo announcement for MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Перемещение проекта на использование последней версии WebView2 SDK 0.9.430 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Пример API WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Объявление об общей доступности Microsoft Edge WebView2 для .NET и фиксированного метода распространения | блоге .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Microsoft Edge"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Коллекции NuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Коллекции NuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Коллекции NuGet | Microsoft.Web.WebView2 v0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Коллекции NuGet | Microsoft.Web.WebView2 v1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Коллекции NuGet | Microsoft.Web.WebView2 v1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Коллекции NuGet | Microsoft.Web.WebView2 1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.674"  
[NuGetGallery1.0.721-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.721"  
[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Объявление об общей доступности Microsoft Edge WebView2 | Блог Microsoft Edge"  

[WebResourceResponseReceivedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_webresourceresponsereceived&preserve-view=true "add_WebResourceResponseReceived интерфейс ICoreWebView2 | Документы Майкрософт"
[NavigateWithWebResourceRequestAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease#createwebresourcerequest&preserve-view=true "CreateWebResourceRequest — интерфейс ICoreWebView2Environment | Документы Майкрософт"
[CookiemanagementAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Документы Майкрософт"
[DOMContentLoadedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_domcontentloaded&preserve-view=true "add_DOMContentLoaded интерфейс ICoreWebView2_2 | Документы Майкрософт"
[WebViewEnvironmentproperty]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#get_environment&preserve-view=true "ICoreWebView2CookieManager | Документы Майкрософт"

[GithubMicrosoftedgeWebviewfeedbackIssue585]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 585" 
[GithubMicrosoftedgeWebviewfeedbackIssue275]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 275" 
[GithubMicrosoftedgeWebviewfeedbackIssue816]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 816" 
[GithubMicrosoftedgeWebviewfeedbackIssue210]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 210" 
[GithubMicrosoftedgeWebviewfeedbackIssue442]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 442" 
[GithubMicrosoftedgeWebviewfeedbackIssue878]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 878" 
[GithubMicrosoftedgeWebviewfeedbackIssue875]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 875" 
[GithubMicrosoftedgeWebviewfeedbackIssue37]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 37" 
[GithubMicrosoftedgeWebviewfeedbackIssue58]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 58" 
[GithubMicrosoftedgeWebviewfeedbackIssue122]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 122" 
[GithubMicrosoftedgeWebviewfeedbackIssue161]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 161" 
[GithubMicrosoftedgeWebviewfeedbackIssue196]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 196" 
[GithubMicrosoftedgeWebviewfeedbackIssue205]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 205" 
[GithubMicrosoftedgeWebviewfeedbackIssue212]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 212" 
[GithubMicrosoftedgeWebviewfeedbackIssue399]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 399" 
[GithubMicrosoftedgeWebviewfeedbackIssue400]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 409" 
[GithubMicrosoftedgeWebviewfeedbackIssue605]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 691" 
[GithubMicrosoftedgeWebviewfeedbackIssue414]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repo feedback for MicrosoftEdge/WebViewFeedback Issue 414" 
[NuGetGallery1.0.705.50]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Коллекции NuGet | Microsoft.Web.WebView2 v1.0.705.50"
[NuGetGallery1.0.790-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "Коллекции NuGet | Предварительная запись Microsoft.Web.WebView2 1.0.790"  
[ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend — интерфейс ICoreWebview2_3 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2experimentalsettings10790PreReleaseGetUserAgent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent интерфейс ICoreWebView2ExperimentalSettings | Документы Майкрософт"  
[ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping — интерфейс ICoreWebView2_3 | Документы Майкрософт"   
[ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor интерфейс ICoreWebView2Controller2 | Документы Майкрософт"  
[ReferenceWin32Icorewebview2controllerViewWebview210790CompositionController]:  /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "интерфейс ICoreWebView2CompositionController | Документы Майкрософт"  
[ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10790]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke — интерфейс ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Документы Майкрософт"  
