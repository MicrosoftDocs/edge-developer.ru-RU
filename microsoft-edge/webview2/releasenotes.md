---
description: Заметки о выпуске для SDK Microsoft Edge WebView2
title: Заметки о выпуске для Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: c3a541560394f2e144f1ffbbd621c800c415602d
ms.sourcegitcommit: 140e09e508fa97f2d124f264d7d2ff77d12d1ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "11399839"
---
# <a name="release-notes-for-webview2-sdk"></a>Заметки о выпуске для SDK WebView2  

Команда WebView2 обновляет [SDK WebView2][NuGetGallery] в течение шести недель.  Просмотрите следующий контент, чтобы получить последние сведения о объявлениях, дополнениях, изменениях и изменениях API.  

> [!NOTE]
> Убедитесь, что вы повторно компилировать приложение после обновления пакета NuGet.  Команда WebView рекомендует использовать канал Canary при разработке с помощью пакетов предварительной подготовки, а также вечнозеленое время работы при использовании выпущенных пакетов.  Дополнительные сведения перейдите к [версии][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions].  
 
<!--## 1.0.816-prerelease  

Release Date: March 8, 2021  

[NuGet package][NuGetGallery1.0.816-prerelease] \| Microsoft Edge version 86.0.616.0 or newer  

### General  

#### Features  

*   Extended `ProcessFailed` event that it will now be raised for non-renderer child processes and frame renderers.  
*   Added experimental [AreBrowserAcceleratorKeysEnabled][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210811GetArebrowseracceleratorkeysenabled] setting.  You may choose to keeps the browser from responding to accelerator keys related to navigation, printing, saving, and other browser-specific functions.  
*   Added iframe support for `AddScriptToExecuteOnDocumentCreated`.  
    
#### Promotion

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] API is now promoted to public.  
*   Rasterization Scale APIs ([RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] property,  [RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] event, [BoundsMode property][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode], and [ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] property) are now promoted to public.  
    
#### Bug fixes  

*   Expanded supported C++ and .NET project types such as MFC and ATL.  \([\#506][GithubMicrosoftedgeWebviewfeedbackIssue506], [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669], and [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Fixed a bug that WebView2 Runtime leaks Inbound firewall entry.  
*   Fixed setting Response during WebResourceRequested event.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Fixed a bug that navigating to `edge://` causes browser process to exit.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Fixed a bug that limited WebView2 bounds to size of screen in Visual Hosting mode. 
    -->  

## <a name="1077444"></a>1.0.774.44  

Дата выпуска: 8 марта 2021 г.  

[Пакет NuGet][NuGetGallery1.0.774.44] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

### <a name="general"></a>Общие  

#### <a name="features"></a>Возможности  

*   Отключены различные службы браузера Microsoft Edge в WebView2.  
*   Visual Hosting API are now generally available.  

#### <a name="promotions"></a>Рекламные акции  

*   Следующие экспериментальные API теперь продвигаются в Stable.  
    *   [Поддержка связанных API DPI][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   API визуального размещения  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend и Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Исправление ошибок  

*   Исправлена ошибка, которая ограничивала пределы WebView2 размером экрана в режиме visual Hosting.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Дата выпуска: 10 февраля 2021 г.  

[Пакет NuGet][NuGetGallery1.0.790-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

### <a name="general"></a>Общие  

> [!IMPORTANT]
> **Breaking Change:** пакет предварительного выпуска WebView2 1.0.781 обесценив.  Прекратите разработку с пакетом 1.0.781.  

> [!IMPORTANT]
> Пакет предварительного выпуска WebView2 0.9.430 отстает и удаляется со следующего выпуска.  Если приложение WebView использует пакет, команда WebView рекомендует использовать его в более новом пакете.  

#### <a name="features"></a>Возможности  

*   Добавлен [метод TrySuspend и Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] для приостановки и возобновления webViews.  
*   Добавлен [метод SetVirtualHostNameToFolderMapping,][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] который совмещая имя виртуального хоста с маршрутом каталога.  \.[\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]и [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Добавлено [свойство DefaultBackgroundColor,][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] чтобы установить цвет и альфа-канал фона.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Добавлено [свойство UserAgent][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] для получения или набора агента пользователя.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Заменил `CreateCookieWithCookie` метод `CopyCookie` методом.  
*   Добавлена поддержка визуального хостинга с помощью [интерфейса ICoreWebView2CompositionController,][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] который создается с помощью `CreateCoreWebView2CompositionController` нового метода `ICoreWebView2Environment3` .  
    
#### <a name="bug-fixes"></a>Исправление ошибок  

*   Отключена функция Microsoft Edge Shopping в WebView2.  
*   Отключено контекстное меню в pdf-представлении, когда `AreDefaultContextMenusEnabled` `false` это .  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Исправлена ошибка, возвращаемая `E_NOINTERFACE` при `ICoreWebView2` запросе `ICoreWebView2Experimental` на .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Исправлена ошибка, разрешив навигацию с неоформленными URL-адресами при `CoreWebView2NavigationStartingEventArgs.Cancel` наборе `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Исправлена ошибка, заблокированная в всплывающих окнах с обработчиками `window.print()` событий, присоединенными к `NewWindowRequested` событиям.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Исправлена проблема динамического DPI при перемещении приложений между различными мониторами.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Улучшены `HRESULT` экземпляры, переданные [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke].  
*   Отключена кнопка управления автозаполненными заправлями.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Исправленные Visual Studio при запуске `WebView2.Dispose` при хозяйской работе в нескольких окнах.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\ и [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Исправленная ошибка для отображения управления WebView2 в Visual Studio панели инструментов.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Снижение проблем с использованием ЦП.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Исправлены проблемы с заданным пакетом 1.0.781-prerelease. [\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [и \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Рекламные акции  

*   Следующие экспериментальные API теперь продвигаются в Stable.  
    *   API визуального размещения  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Исправление ошибок  

*   Исправлена ошибка, которая разбила приложения WebView, которые используют SDK WPF.  Сбой произошел при закрытии окон с помощью клавиши F4.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   Экран инициализации WebView2 теперь прозрачный, а не серый.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Дата выпуска: 25 января 2021 г.  

[Пакет NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime версии 86.0.616.0 или более новой  

### <a name="general"></a>Общие  

#### <a name="promotions"></a>Рекламные акции  

*   Следующие экспериментальные API теперь продвигаются в Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API управления cookie][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Свойство WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## <a name="10721-prerelease"></a>1.0.721-prerelease  

Дата выпуска: 8 декабря 2020 г.  

[Пакет NuGet][NuGetGallery1.0.721-prerelease] \| Microsoft Edge версии 86.0.616.0 или более новой  

### <a name="general"></a>Общие  

> [!IMPORTANT]
> **Breaking Change:** пакет webView2 для предварительного выпуска 1.0.707 и пакет 0.9.628 не являются готовыми.  Прекратите разработку пакетом 1.0.707 и пакетом 0.9.628.  

#### <a name="features"></a>Возможности  

*   Добавлены [групповые политики WebView2.][DeployedgeMicrosoftEdgeWebviewPolicies]  Дополнительные сведения о рекомендуемых практиках перейдите к групповым [политикам для WebView2.][Webview2ConceptsEnterpriseGroupPoliciesForWebview2]  
*   > [!IMPORTANT]
    > **Breaking Change:** Deprecated the old registry location.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Добавлена поддержка [перетаскивания и сброса][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] в WebView2.  
*   Добавлены API для обработки поддержки DPI.  
    *   Добавлено [свойство RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] для изменения шкалы DPI для контента WebView и всплывающих интерфейсов пользовательского интерфейса и связанного события [RasterizationScaleChanged.][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]  
    *   Добавлено [свойство ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] для автоматического обновления `RasterizationScale` свойства при необходимости.  
    *   Добавлено свойство [BoundsMode,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] чтобы указать, что границы — это пиксели логики и разрешить WebView использовать для пиксельного отображения WebView2, а WebView — с помощью этого объекта, чтобы получить `RasterizationScale` `RasterizationScale` `Bounds` физический размер.  
*   Обновленное `NewWindowRequested` событие для `Ctrl` + `click` обработки и `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] и [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Следующие экспериментальные API теперь продвигаются в Stable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API управления cookie][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Свойство WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Возможности  

*   Включен конструктор WinForms в .NET Core 3.1+ и .NET 5.  
*   Улучшено управление файлами cookie .NET.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Заменено `CoreWebView2Ready` [на CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

#### <a name="bug-fixes"></a>Исправление ошибок

*   Добавлено [событие AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] для поддержки выбора AcceleratorKey в WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Удаление ненужных файлов из вывода в папки WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Улучшенный API объектов-хостов.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] и [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Дата выпуска: 20 ноября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.664.37] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

### <a name="general"></a>Общие  

> [!IMPORTANT]
> **Объявление**. .NET WPF/WinForms WebView2 SDKs теперь, как правило, доступны \(GA\).  Начиная с этого выпуска, SDKs выпуска являются совместимыми с форвардными версиями.  Дополнительные сведения, перейдите к [сообщению блога объявления GA][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod].  

#### <a name="features"></a>Возможности  

*   .NET WPF/WinForms WebView2 теперь обычно доступен \(GA\).  
*   Режим фиксированной рассылки \(Bring-your-own\) достиг ga.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Исправление ошибок  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` предотвращает открытие нового окна.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] и [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

### <a name="general"></a>Общие  

*   Добавлен [метод NavigateWithWebResourceRequest][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] для предоставления почтовых данных или других заголовок запросов во время навигации.  
*   Добавлено [событие DOMContentLoaded,][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] которое запускается при загрузке и размыве исходного HTML-документа.  
*   Добавлено [свойство Environment][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] в WebView2.  Это свойство предоставляет среду WebView2, в которой был создан экземпляр WebView2.  
*   Добавлены [API][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] управления файлами cookie, позволяющие разработчикам проверить подлинность сеанса WebView2 или получить файлы cookie из WebView для проверки подлинности других средств.  Группа Веб-просмотров планирует улучшить языковые или рамочные улучшения.  Дополнительные сведения перейдите в [API Review: Cookie Management.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Обновлено [событие WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] и добавлено непрестанное [webResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] и [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] к [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent].  
*   Отключено [приложение Microsoft Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] в WebView2.  
*   Добавлен [SystemCursorId для][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] визуального размещения.  
*   Добавлена ошибка, исправленная для метода ввода в Visual Hosting.  
*   Удаление включает требования к `version.lib` использованию статической библиотеки WebView2.  
    
### <a name="net"></a>.NET  

*   Обновленный [класс CoreWebView2 для][DotnetApiMicrosoftWebWebview2CoreCorewebview2] разоблачения `CoreWebView2Environment` переменной.  
*   Изменены реализации пользовательских классов EventArgs в пространстве имен на подклассы `Microsoft.Web.WebView2.Core` [System.EventArgs][DotnetApiSystemEventargs] или [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Добавлена поддержка [свойств CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] в WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   Добавлены [API WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Обновленное свойство конструктора WinForms [по умолчанию][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] или сброс с null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Обновленные границы WebView2 в WebView2.Init() для поддержки режимов DPI, которые менее 100%.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Обновленные [BuildWindowCore и][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [DestroyWindowCore для][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] повышения надежности.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Обновленная база погрузчиков .NET для загрузки бита процесса вместо архитектуры операционной системы.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Переименован в `EdgeNotFoundExpection` [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.622.22] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

### <a name="general"></a>Общие  

> [!IMPORTANT]
> **Объявление:** Win32 C/C++ WebView2 теперь обычно доступен \(GA\).  Начиная с этого выпуска, SDKs выпуска являются совместимыми с форвардами.  Дополнительные сведения перейдите к [сообщению в блоге объявления GA][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*   [Evergreen WebView2 Runtime и установщик][Webview2ConceptsDistributionUnderstandRuntimeInstaller] являются GA.  Загрузчик, ссылки на ссылку для Bootstrapper и автономный установщик для запуска Evergreen WebView2 доступны в [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Пример кода для рабочего процесса установки также доступен в [репо WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   [Режим фиксированной версии][Webview2ConceptsDistributionFixedVersionDistributionMode] доступен для предварительного просмотра разработчика.  
    
## <a name="0962211"></a>0.9.622.11  

Дата выпуска: 10 сентября 2020 г.  

[Пакет NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime версии 86.0.616.0 или более новой.  

### <a name="general"></a>Общие  

*   > [!IMPORTANT]
    > **Объявление.** Этот SDK является кандидатом на выпуск webView2 Win32 C/C++ GA.  Версия GA должна использовать тот же интерфейс API и функциональные возможности.  
    
*   Отключенные [политики браузера.][DeployedgeMicrosoftEdgePolicies]  
*   Добавлено [свойство AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   `ICoreWebView2NewWindowRequestedEventArgs`Обновлено, чтобы включить свойство [WindowFeatures][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] и связанные [ICoreWebView2WindowFeatures][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622].  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Обновлено `System.Windows.Rect`  для использования вместо `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Обновленное событие NewWindowRequested для обработки `window.open()` запроса без параметров.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Параметры AdditionalBrowserArguments, указанные с помощью параметра AdditionalBrowserArguments,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] не переопределяются с переменными среды `ICoreWebView2EnvironmentOptions` или значениями реестра.  Дополнительные сведения можно получить в [createCoreWebView2EnvironmentWithOptions.][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]  
    
## <a name="09579"></a>0.9.579  

Дата выпуска: 20 июля 2020 г.  

[Пакет NuGet][NuGetGallery0.9.579] \| Microsoft Edge версии 86.0.579.0.  

### <a name="general"></a>Общие  

*   > [!IMPORTANT]
    > **Объявление.** Для предварительного просмотра выпущены время запуска и установки Evergreen WebView2.  Дополнительные сведения перейдите к [рассылке WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Объявление.** Следующие версии SDK WebView2 больше не поддерживаются после следующего выпуска SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Версии SDK WebView2 также отмечены в nuget.org.  WebView2 рекомендует оставаться в курсе последней версии WebView2.  
    
*   Добавлены улучшения рабочих потоков WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Отключен блокатор всплывающих в WebView.  Дополнительные сведения перейдите к [свойству IsUserInitiated][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] в `NewWindowRequested` событии.  
*   Гарантируется запуск события навигации WebView для `about:blank` .  Теперь события запускаются для всех навигаций, но отмены для или iframe не поддерживаются и `NavigationStarting` `about:blank` `srcdoc` игнорируются.  
*   Заблокированы некоторые `edge://` схемы URI в WebView.  
*   Добавлено экспериментальное свойство [IsSingleSignOnUsingOSPrimaryAccountEnabled][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Добавлено экспериментальное событие [WebResourceResponseReceived,][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] которое запускается после того, как WebView получает и обрабатывает ответ от запроса WebResource.  Заглавы проверки подлинности, если таково, включены в объект ответа.  
    
### <a name="net"></a>.NET  

*   Улучшенная обработка фокуса WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Добавлено `ZoomFactor` свойство контроллера WPF Webview2.  
    
## <a name="09538"></a>0.9.538  

[Пакет NuGet][NuGetGallery0.9.538] \| Microsoft Edge версии 85.0.538.0.  

### <a name="general"></a>Общие  

*   Удаление поддержки для WebView2 SDK Версии [0.8.149](#08149).  WebView2 рекомендует оставаться в курсе последней версии WebView2.  
*   Обновленная политика группы для учета изменения пути профиля браузера Microsoft Edge \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   Добавлено [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures], который срабжает при запуске и связан с `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Breaking Change:** Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Breaking Change.** Для обеспечения соответствие API WebView2 конвенциям именования API Windows, команда WebView обновила имена следующих.  
    > 
    > *   [AreRemoteObjectsAllowed теперь][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] [AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   Обновленный [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript].  В настоящее время исходные маркеры сериализатора объектов хост настроены на прокси-объекты.  Затем маркеры сериализации объектов хост-объектов сериализируются обратно в качестве объекта-хоста, когда передаются в качестве параметра в обратном вызове JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
### <a name="net-09538-pre-release"></a>.NET (0.9.538 предварительного выпуска)  

*   Выпущены образцы WinForms и WPF WebView2API, которые являются исчерпывающими руководствами SDK WebView2.  Дополнительные сведения можно получить в [примере Репо][GithubMicrosoftedgeWebview2samplesMain].  
*   Добавлена поддержка визуального размещения и оконных функций [экспериментальных API.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Breaking Change:** Следующие отсрочки теперь реализуют IDisposable:  [ScriptDialogOpening,][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening] [NewWindowRequested,][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested] [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]и [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Добавлены [getAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] и [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] в качестве статики [CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[Пакет NuGet][NuGetGallery0.9.515-prerelease] \| Microsoft Edge версии 84.0.515.0.  

*   > [!IMPORTANT]
    > **Объявление.** WebView2 теперь поддерживает Windows Forms и WPF платформа .NET Framework 4.6.2 или более поздней версии и .NET Core 3.0 или более поздней версии пакета **.**  
    
*   Дополнительные сведения о создании приложений WPF перейдите в руководство [WPF по][Webview2GettingstartedWpf] началу работы и ссылку [WPF WebView2][DotnetApiMicrosoftWebWebview2Wpf] для API, характерных для WPF.  
*   Дополнительные сведения о создании приложений Для форм Windows перейдите в руководство по началу работы с формами [Windows][Webview2GettingstartedWinforms] и ссылку На веб-формы [Windows][DotnetApiMicrosoftWebWebview2Winforms] Для Форм Windows конкретные API.  
*   Дополнительные сведения об API CoreWebView2 перейдите в [ссылку .NET.][DotnetApiMicrosoftWebWebview2Core]  
*   > [!CAUTION]
    > **Известные проблемы.** Команда WebView знает о некоторых проблемах в предварительном выпуске, которые будут решены в будущих выпусках.  
    > 
    > *   **Осведомленность о DPI:** WebView2 для WPF в настоящее время не знает DPI.  При инициализации WebView2 на высоких мониторах DPI существует известная проблема, при которой WebView сначала инициализируется как часть окна до повторного размера окна.  
    > *   **Конструктор WPF.** Дизайнер WPF в настоящее время не поддерживается.  Добавьте в приложение управление WebView2, непосредственно изменяя соответствующий XAML в текстовом редакторе.  
    
## <a name="09488"></a>0.9.488  

[Пакет NuGet][NuGetGallery0.9.488] \| Microsoft Edge версии 84.0.488.0.  

*   > [!IMPORTANT]
    > **Объявление.** Начиная с предстоящей версии Microsoft Edge 83, Evergreen WebView больше не нацелен на канал стабильного браузера.  Вместо этого он нацелен на другой набор разнонастроек, фирменное время запуска [Evergreen WebView2,][Webview2ConceptsDistributionEvergreenDistributionMode]которые можно установить с помощью установщика, который в настоящее время разрабатывает команда WebView.  Дополнительные сведения перейдите в [App-Distribution.][Webview2ConceptsDistribution]  
    
*   > [!IMPORTANT]
    > **Объявление.** Двигаясь вперед, команда WebView выпускает два пакета: пакет предварительного выпуска с экспериментальными API \(для вас, чтобы попробовать\) и стабильный пакет выпуска со стабильными API \(для вашего доверия\).  Чтобы узнать о различиях, перейдите к пониманию версий [браузера и WebView2][Webview2ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Breaking Change.** Для обеспечения соответствие API WebView2 конвенциям именования API Windows, команда WebView обновила имена следующих интерфейсов.  
    > 
    > *   `CORE_WEBVIEW2_*` префикс теперь `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] теперь [getAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] теперь [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] теперь [является AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] теперь [RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` теперь `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Breaking Change:** `AddRemoteObject` прокси-методы JS также переименованы.  
    > 
    > *   `getLocal` теперь `getLocalProperty` .  
    > *   `setLocal` теперь `setLocalProperty` .  
    > *   `getRemote` теперь `getHostProperty` .  
    > *   `setRemote` теперь `setHostProperty` .  
    > *   `applyRemote` теперь `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Deprecated [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] and replaced with [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   Добавлено [событие FrameNavigationCompleted.][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]  Теперь, когда iframe завершает навигацию, событие запускается и возвращает успех навигации и навигационного ID.  
*   Добавлен [интерфейс ICoreWebView2EnvironmentOptions,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] который может использоваться для определения версии времени выполнения WebView2, на которое нацелено ваше приложение.  
*   Добавлен [параметр IsBuiltInErrorPageEnabled.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  Теперь вы можете включить или отключить встроенную веб-страницу ошибки для сбоя навигации и сбоя процесса визуализации.  
*   Обновленная удаленная инъекция объектов для поддержки реализации .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Обновленное [событие NewWindowRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] для обработки запросов из контекстных меню \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Выпущен первый отдельный пакет предварительного выпуска WebView2, в котором вы можете получить доступ к API визуального размещения.  Команда WebView обновила [APISample,][GithubMicrosoftedgeWebview2samplesMain] чтобы включить новые экспериментальные API.  
    *   Добавлен [интерфейс ICoreWebView2ExperimentalCompositionController,][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] чтобы подключиться к дереве композиции и предоставить вход для WebView.  
    *   Добавлен [iCoreWebView2ExperimentalPointerInfo,][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]который содержит всю информацию из `POINTER_INFO` .  Этот объект передается в SendPointerInput для ввода ввода указателя в WebView.  
    *   Добавлено [приложение ICoreWebView2ExperimentalCursorChangedEventHandler,][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]которое сообщает приложению, когда следует изменить курсор мыши над WebView.  Когда мышь находится над текстовым полем в WebView, курсор изменяется со стрелки на селектор.  Свойство в приложении сообщает, каким должен быть курсор мыши в настоящее время `cursor` `CompositionController` для WebView.  
        
## <a name="09430"></a>0.9.430  

[Пакет NuGet][NuGetGallery0.9.430] \| Microsoft Edge версии 82.0.430.0.  

SDK WebView2 — это официальная бета-версия Win32 C++ с несколькими запросами на функции из отзывов.  Команда WebView пытается ограничить количество выпусков с помощью нарушающих изменений.  По мере приближения общих подходов к доступности в бета-версии включалось несколько существенных изменений.  

*   > [!IMPORTANT]
    > **Breaking Change.** По мере приближения окончательного выпуска команда WebView переименовала префикс, чтобы убедиться, что API WebView2 соответствует конвенции именования `IWebView2WebView` `ICoreWebView2` API Windows.  Кроме того, чтобы использовать SDK WebView2 из пользовательского интерфейса, команда WebView разделилась на `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] и [ICoreWebView2Host.][Webview2ReferenceWin32Icorewebview2hostViewWebview209430]  `ICoreWebView2Host` поддерживает размер, отображение и сокрытие, фокусиро- и другие функции, связанные с окном и композицией.  ICoreWebView2 поддерживает все остальные функции WebView2.  Чтобы узнать больше об учете изменений, перейдите к запросу на вытягивать [WebView2][GithubMicrosoftedgeWebview2samplesPr17] в проекте [APISample][GithubMicrosoftedgeWebview2samplesMain] WebView2.  
    
*   > [!IMPORTANT]
    > **Breaking Change:** [Split DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] на три компонента: [SourceChanged,][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged] [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]и [HistoryChanged.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]  Теперь, когда исходный URL-адрес `SourceChanged` изменяется, событие будет запускаться.  При смене состояния истории `HistoryChanged` событие запускается.  Событие `ContentLoading` запускается перед начальным сценарием при загрузке нового документа.  
    
*   Добавлена поддержка архитектуры ARM64.  
*   Добавлена поддержка soft Input Panel \(SIP\) для устройств с сенсорным экраном.  
*   Добавлена поддержка Windows Server 2008 R2 Windows Server 2012, Windows Server 2012 R2 и Windows Server 2016.  
*   Добавлена [notifyParentWindowPositionChanged для][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] панели состояния, которая следует за окном в окне.  Кроме того, реализуем изменение в режиме без окон, чтобы функции доступности работали.  
*   Добавлен [параметр AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] для глобального управления доступом к веб-странице любыми удаленными объектами.  По умолчанию включено, поэтому удаленные объекты, добавленные `AreRemoteObjectsAllowed` [AddRemoteObject,][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] доступны на веб-странице.  При `AreRemoteObjectsAllowed` выключении объекты недоступны на веб-странице.  Изменения применяются в следующем событии навигации.  
*   Добавлен [параметр IsZoomControlEnabled,][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] чтобы пользователи не влияли на масштаб веб-изображения с помощью `ctrl` + `+` и `ctrl` + `-` \(или `ctrl` + колесо мыши\).  Масштабирование может по-прежнему put_ZoomFactor [при][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] выключении параметра.  
*   Изменен ZoomFactor, чтобы применяться только к текущему WebView.  Изменение масштабирования текущего WebView не влияет на другие веб-просмотры, которые вы переходили на один и тот же сайт происхождения.  Дополнительные сведения, перейдите [к get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Hid ZoomView UI для WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Добавлен [SetBoundsAndZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor].  Теперь можно одновременно установить фактор масштабирования и границы WebView.  
*   Добавлено [событие WindowCloseRequested.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]  Дополнительные сведения см. в [add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Добавлена поддержка типа диалогов для диалоговых событий JavaScript и `beforeunload` [добавлена CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] записи.  
*   Добавлены [GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] в HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] в HttpResponseHeaders и [get_HasCurrentHeader][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] в httpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Breaking Change.** `DevToolsProtocolEventReceived` Измененное поведение.  Теперь можно создать [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] для определенного события Протокола DevTools и подписаться/отписаться от такого события с помощью [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived].  
    
*   > [!IMPORTANT]
    > **Breaking Change**: `WebMessageReceivedEventArgs` [изменено get_WebMessageAsString][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] на [метод TryGetWebMessageAsString.][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]  
    
*   > [!IMPORTANT]
    > **Breaking Change.** Изменен метод `AcceleratorKeyPressedEventArgs` [Handle][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] на [свойство get_Handled.][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]  
    
## <a name="08355"></a>0.8.355  

[Пакет NuGet][NuGetGallery0.8.355] \| Microsoft Edge версии 80.0.355.0.  

*   Выпущенный образец WebView2API, полное руководство по SDK WebView2.  Дополнительные сведения перейдите к [примеру API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Добавлена поддержка IME для всех языков, кроме английского \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Обновлена поверхность API события `WebResourceRequested` в ответ на сообщения об ошибках.  Одновременное указание фильтра и события при создании теперь отстает.  Чтобы создать событие, запрашиваемого [][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] веб-ресурсом, используйте add_WebResourceRequested для добавления события и [AddWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] для добавления фильтра.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] удаляет фильтр \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change:** Изменение полноэкранного поведения.  Deprecated [IsFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Теперь, по умолчанию, если элемент в WebView \(например, видео\) установлен на полный экран, он заполняет границы WebView.  Используйте [событие ContainsFullScreenElementChanged][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] и get_ContainsFullScreenElement, чтобы указать, как приложение должно повторно использовать WebView, если элемент хочет ввести полноэкранный режим. [][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]  
    
## <a name="08314"></a>0.8.314  

[Пакет NuGet][NuGetGallery0.8.314] \| Microsoft Edge версии 80.0.314.0.  

*   Добавлена поддержка Windows 7, Windows 8 и Windows 8.1.  
*   Добавлена Visual Studio и Visual Studio поддержка отлажки кода для WebView2.  Теперь отлаговка скрипта в WebView2 прямо из вашего IDE.  Дополнительные сведения можно найти в элементе [How to debug when developing with WebView2 controls.][Webview2HowtoDebug]  
*   Добавлен для запуска скрипта в WebView2 для доступа к объекту IDispatch из компонента Win32 приложения и доступа к свойствам `Native Object Injection` объекта IDispatch.  Дополнительные сведения см. в [странице AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения см. в [add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Отключено `Context Menus` .  Дополнительные сведения см. в [put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Обновлено `DPI Awareness` .  Теперь уровень осведомленности об уровне DPI в WebView такой же, как и уровень осведомленности о DPI в хост-приложении.  
    
    > [!NOTE]
    > Если другое гибридное приложение запущено с другим пониманием DPI, чем исходное WebView, новое WebView не запущено, если то же `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Обновляется `Notification Change Behavior` таким образом, что WebView2 автоматически отклоняет запросы на разрешение уведомлений, запрашиваемые веб-контентом, который был организован в WebView.  
    
## <a name="08270"></a>0.8.270  

[Пакет NuGet][NuGetGallery0.8.270] \| Microsoft Edge версии 78.0.270.0.  

*   Добавлено `DocumentTitleChanged` событие, указать изменение заголовка документа[\. \#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Добавлен `GetWebView2BrowserVersionInfo` API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Добавлено `NewWindowRequested` событие.  
*   Обновленная `CreateWebView2EnvironmentWithDetails` функция для удаления `releaseChannelPreference` .  Дополнительные сведения о `CreateWebView2EnvironmentWithDetails` функции перейдите в [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Переопределения реестра и переменной среды по-прежнему поддерживаются.  Предпочтение канала по умолчанию используется, если не переопределять.  
    Во время поиска канала команда WebView пропускает предыдущую версию канала, не совместимую с SDK WebView2.  
    Команда WebView выбирает более стабильный канал, чтобы обеспечить наиболее последовательное поведение для конечному пользователю.  При проверке последних сборки Canary необходимо создать сценарий, чтобы настроить переменную среды перед `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` запуском приложения.  
*   Обновлена `CreateWebView2EnvironmentWithDetails` функция с помощью логики `userDataFolder` выбора, если она не указана.  Дополнительные сведения о `CreateWebView2EnvironmentWithDetails` функции перейдите в [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Если вы ранее использовали расположение по умолчанию, при переходе на новый SDK по умолчанию сбрасывается \(задайте новое расположение в каталоге кода хост\) и ваше состояние также `userDataFolder` `userDataFolder` сбрасывается.  Если у хост-процесса нет разрешения на записи в указанный каталог, функция `CreateWebView2EnvironmentWithDetails` может привести к сбойу.  Можно скопировать данные из старого в `user data folder` новый каталог.  
    
## <a name="08230"></a>0.8.230  

[Пакет NuGet][NuGetGallery0.8.230] \| Microsoft Edge версии 77.0.230.0.  

*   Добавлен API для остановки всех извлечений навигации и ожидающих ресурсов `Stop` [\. \#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Добавлен `.tlb` файл в пакет NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Добавлены проекты .NET в список установщика в пакете NuGet \.[\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## <a name="08190"></a>0.8.190  

[Пакет NuGet][NuGetGallery0.8.190] \| Microsoft Edge версии 77.0.190.0.  

*   Добавлено `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` управление, если пользователи могут открывать DevTools[\. \#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Добавлено управление, если отображается планка `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` состояния \.[\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Добавлено `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` для перемещения назад и вперед в истории навигации.  
*   Добавлены типы http header \( \) для просмотра и `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` изменения http-заглавок в WebView.  
*   Добавлена 32-битная поддержка WebView на 64-битных машинах[\( \#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Добавлен IDL WebView в SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Добавлено lib для `IID\_\*` поддержки ID-объектов интерфейса \.[\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Добавлены путь, привязка и автокопизание DLL-файлов в файл NuGet `TARGET` в SDK.  
*   Включен запрос в `window.open()` скрипте.  
    
## <a name="08149"></a>0.8.149  

[Пакет NuGet][NuGetGallery0.8.149] \| Microsoft Edge версии 76.0.149.0.  

Начальный выпуск предварительного просмотра разработчика.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью webView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью webView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Режим распространения фиксированной версии — распространение приложений с помощью webView2 | Документы Майкрософт"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Понимание времени работы и установки WebView2 — распространение приложений с помощью webView2 | Документы Майкрософт"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Групповые политики для WebView2 — управление приложениями WebView2 | Документы Майкрософт"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Понимание версий браузера и webView2 | Документы Майкрософт"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Экспериментальные API — понимание версий браузера и webView2 | Документы Майкрософт"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Соответствие версиям времени работы WebView2 — понимание версий SDK webView2 | Документы Майкрософт"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях Форм Windows | Документы Майкрософт"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF | Документы Майкрософт"  
[Webview2HowtoDebug]: ./howto/debug.md "Отламывка при разработке с помощью элементов управления WebView2 | Документы Майкрософт"  

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210811GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.816&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed — интерфейс ICoreWebView2ExperimentalSettings | Документы Майкрософт" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded — интерфейс ICoreWebView2_2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping — интерфейс ICoreWebView2_3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend — интерфейс ICoreWebview2_3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled — интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "интерфейс ICoreWebView2CompositionController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor — интерфейс ICoreWebView2Controller2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived — интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived — интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest — интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount — интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments — интерфейс ICoreWebView2EnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo — интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString — интерфейс ICoreWebView2Environment | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController3 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges — интерфейс ICoreWebView2ExperimentalController | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled — интерфейс ICoreWebView2ExperimentalEnvironmentOptions | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures — интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalPointerInfo | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent — интерфейс ICoreWebView2ExperimentalSettings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest — интерфейс ICoreWebView2Experimental | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent — интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWindowFeatures | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor — интерфейс ICoreWebView2Host | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader — интерфейс ICoreWebView2HttpHeadersCollectionIterator | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders — интерфейс ICoreWebView2HttpRequestHeaders | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader — интерфейс ICoreWebView2HttpResponseHeaders | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures — интерфейс ICoreWebView2NewWindowRequestedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed — интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled — интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed — интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled — интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed — интерфейс ICoreWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript — интерфейс ICoreWebView2 | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString — интерфейс ICoreWebView2WebMessageReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Вызов — интерфейс ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "интерфейс ICoreWebView2WindowFeatures | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle — интерфейс IWebView2AcceleratorKeyPressedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "интерфейс IWebView2ContainsFullScreenElementChangedEventHandler | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled — интерфейс IWebView2Settings2 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated — интерфейс IWebView2Settings | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString — интерфейс IWebView2WebMessageReceivedEventArgs | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed — интерфейс IWebView2WebView4 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject — интерфейс IWebView2WebView4 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter — интерфейс IWebView2WebView5 | Документы Майкрософт" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged — интерфейс IWebView2WebView | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails - Globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo — globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails - Globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString — globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Документы Майкрософт" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge — политики | Документы Майкрософт"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 — политики | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Microsoft.Web.WebView2.Core Namespace | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Класс CoreWebView2 (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Класс CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Метод CoreWebView2Environment.CompareBrowserVersions (String, String) (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Метод CoreWebView2Environment.GetAvailableBrowserVersionString (String) (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Класс CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Класс CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "CoreWebView2.NewWindowRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "CoreWebView2.PermissionRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Событие CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "CoreWebView2.WebResourceRequested Event (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "CoreWebView2InitializationCompletedEventArgs class | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft.Web.WebView2.WinForms | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Класс CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Класс Webview2.Source (Microsoft.Web.WebView2.Winforms) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft.Web.WebView2.Wpf | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Метод WebView2.BuildWindowCore (HandleRef) (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Метод WebView2.DestroyWindowCore (HandleRef) (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "CancelEventArgs Class (System.ComponentModel) | Документы Майкрософт"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "EventArgs Class (System) | Документы Майкрософт"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Сборки с сильными | Документы Майкрософт"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Охрана приложений Microsoft Defender (Windows 10) — служба безопасности Windows | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Репо объявления для MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Образец API WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Примеры WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Перемещение проекта с использованием последней версии WebView2 SDK 0.9.430 — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Репо обратной связи для MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Репо отзывов для MicrosoftEdge/WebViewFeedback Issue 878"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Объявление общей доступности для Microsoft Edge WebView2 для .NET и фиксированного метода | .NET Blog"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Edge Developer"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Галерея NuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Галерея NuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Галерея NuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Галерея NuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v0.9.515 prerelease"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Галерея NuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Галерея NuGet | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Галерея NuGet | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v0.9.628 prerelease"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Галерея NuGet | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Галерея NuGet | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Галерея NuGet | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v1.0.674 prerelease"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Галерея NuGet | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v1.0.721 prerelease"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "Галерея NuGet | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v1.0.790 prerelease"  
[NuGetGallery1.0.816-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.816-prerelease "Галерея NuGet | Microsoft.Web.WebView2 v1.0.816 prerelease"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Объявление об общей доступности Microsoft Edge WebView2 | Microsoft Edge Blog"  
