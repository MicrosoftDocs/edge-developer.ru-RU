---
description: Заметки о выпуске Microsoft Edge WebView2 SDK
title: Заметки о выпуске Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 840d9d5e074e2ea2777942fd19106592151c29ee
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192228"
---
# Заметки о выпуске SDK для WebView2  

Группа WebView2 обновляет [пакет SDK WebView2][NuGetGallery] на частоту в течение шести недель.  Ознакомьтесь со следующими материалами, чтобы получить актуальные сведения о объявлениях, дополнениях, изменениях и критических изменениях API-интерфейсов.  

> [!NOTE]
> Повторно скомпилируйте приложение после обновления пакета NuGet.  

## предварительный выпуск 1.0.707  

Дата выпуска: 23 ноября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.707-prerelease] \ | Минимальная версия Microsoft Edge 86.0.616.0.  

> [!IMPORTANT]
> Этот пакет устарел из-за известных ошибок. 

<!--  
#### General  

###### Features  

*   Added [WebView2 Group Policies][DeployedgeMicrosoftEdgeWebviewPolicies].  For more information on recommended practices, navigate to [group policies for WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Breaking Change**:  Deprecated the old registry location.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
     
*   Added support for [Drag & Drop][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] within WebView2.  
*   Added APIs to handle DPI support.  
    *   Added [RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetRasterizationscale] property to change the DPI scale for WebView content and UI popups, and associated [RasterizationScaleChanged][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseAddRasterizationscalechanged] event.  
    *   Added [ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetShouldDetectMonitorScaleChanges] property to automatically update `RasterizationScale` property if needed.  
    *   Added [BoundsMode property][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetBoundsMode] to specify that the bounds are logic pixels and allow WebView to use the `RasterizationScale` for WebView2 pixel display, and have WebView apply the `RasterizationScale` to the `Bounds` to get the physical size.
*   Updated `NewWindowRequested` event to handle `Ctrl`+`click` and `Shift`+`click`.  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] and [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  

#### .NET  

###### Features  

*   Enabled WinForms designer in .NET Core 3.1+ and .NET 5.  
*   Improved .NET cookie management.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Renamed `CoreWebView2Ready` to [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].

###### Bug fixes

*   Added [AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] event to support AcceleratorKey press in WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Removed unnecessary files from being output to WebView2 folders.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   Improved host object API.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] and [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
-->  

## 1.0.664.37  

Дата выпуска: 20 ноября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.664.37] \ | Минимальная версия среды выполнения WebView2 версии 86.0.616.0.  

#### Общие  

> [!IMPORTANT]
> **Объявление**: платформа .NET WPF/WinForms WebView2 теперь доступна в обычном виде (GA \).  Начиная с этого выпуска, выпущены пакеты SDK, совместимые с переадресацией.  Для получения дополнительных сведений перейдите к записи [блога "объявление в блоге][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]".  

###### Возможности  

*   .NET WPF/WinForms WebView2 теперь является общедоступным: \ (GA \).  
*   Режим фиксированного распределения \ ("само-собственная \") достиг в "GA".  

#### .NET  

###### Исправления ошибок  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` запрещает открытие нового окна \ ([\ #549][GithubMicrosoftedgeWebviewfeedbackIssue549]\) и \ ([\ #560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  


## предварительный выпуск 1.0.674  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.674-prerelease] \ | Минимальная версия среды выполнения WebView2 версии 86.0.616.0.  

#### Общие  

*   Добавлен метод [NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] , который позволяет предоставлять данные POST или дополнительные заголовки запроса во время навигации.
*   Добавлено событие [DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] , которое выполняется при загрузке и анализе исходного HTML-документа.
*   Добавлено свойство [Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] в WebView2.  Это свойство предоставляет среду WebView2, в которой создан экземпляр WebView2.
*   Добавлены API для [управления файлами cookie][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] , позволяющие разработчикам проверять подлинность сеанса WebView2 или извлекать файлы cookie из WebView для проверки подлинности других средств.  Мы планируем внести усовершенствования для определенного языка и платформы.  Дополнительные сведения можно найти в статье [Просмотр API: Управление файлами cookie][GithubMicrosoftedgeWebview2AnnouncementIssue2].
*   Обновлено событие [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] и добавлены неизменяемые [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] и [WebResourceResponseReceivedEventArgs::P opulateresponsecontent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] , чтобы стать [WebResourceResponseView::][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].
*   Выключено [Application Guard в защитнике Microsoft (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] в WebView2.
*   Добавлены [SystemCursorId][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] для визуального размещения.
*   Добавлена ошибка, исправленная для метода ввода в визуальном размещении.
*   Разработчикам больше не нужно включать версию. lib при использовании статической библиотеки WebView2.

#### .NET  

*   Обновленный класс [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] для предоставления переменной CoreWebView2Environment.  
*   Измененные реализации собственных классов EventArgs в `Microsoft.Web.WebView2.Core` пространстве имен должны быть подклассами [System. EventArgs][DotnetApiSystemEventargs] или [System. ComponentModel. CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \ ([\ #250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Добавлена поддержка [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] в WinForms.  \ ([\ #204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   Добавлены API .NET [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .  \ ([\ #219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Обновленному свойству [Source][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] конструктора WinForms значение по умолчанию или сброшено на null.  \ ([\ #177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Обновленные WebView2ные границы в WebView2.Init (), поддерживающие режимы DPI, менее 100%.  \ ([\ #432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Обновленные [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] и [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] более надежны.  \ ([\ #382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   База .NET Loader обновлена для загрузки на бит процесса, а не архитектуры операционной системы.  \ ([\ #431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Переименован `EdgeNotFoundExpection` в [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].
 
## 1.0.622.22  

Дата выпуска: 19 октября 2020 г.  

[Пакет NuGet][NuGetGallery1.0.622.22] \ | Минимальная версия среды выполнения WebView2 версии 86.0.616.0.  

#### Общие  

> [!IMPORTANT]
> **Объявление**: WebView2 Win32 C/C++ теперь является, как обычно, доступным \ (GA \).  Начиная с этого выпуска, выпущены пакеты SDK, совместимые с переадресацией.  Для получения дополнительных сведений перейдите к записи [блога "объявление в блоге][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]".  

*  [Evergreen WebView2 среды выполнения и установщика][Webview2ConceptsDistributionUnderstandRuntimeInstaller] .  Загрузчик, ссылка прием на загрузчик и автономный установщик для среды выполнения Evergreen доступны в [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  Образец кода для рабочего процесса установки также доступен в [репозитории WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*  [Режим фиксированной версии][Webview2ConceptsDistributionFixedVersionMode] доступен для предварительного ознакомления с разработчиком.  

## предварительный выпуск 0.9.628  

Дата выпуска: 10 сентября 2020 г.  

[Пакет NuGet][NuGetGallery0.9.628-prerelease] \ | Минимальная версия Microsoft Edge 86.0.616.0.  

> [!IMPORTANT]
> **Объявление**: Эта предварительная версия продолжает выпустить на основе ветви Microsoft Edge 87.  В будущем выпуск SDK предварительной версии соответствует сборке Microsoft Edge Канарские, а обычный выпуск синхронизируется с Microsoft Edge STABLE.  

#### Общие  

*   > [!IMPORTANT]
    > **Объявление**: API размещения теперь находятся в области предварительного просмотра.  WebView2 использует визуальное размещение для работы параллельно с WinComp/DComp визуальными элементами, а не с дескрипторами HWND.  В экспериментальных интерфейсах.  Дополнительные сведения можно найти в [ICoreWebView2ExperimentalEnvironment][ReferenceWin32Icorewebview2experimentalenvironment09628].  

#### .NET  

*   Двоичные файлы .NET теперь называются [строгими][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   Для включения в конечную версию NuGet `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) и \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Обновлены `WebResourceRequested` для предоставления API [HttpRequestHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders] и [HttpResponseHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders] в .NET.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622.11  

Дата выпуска: 10 сентября 2020 г.  

[Пакет NuGet][NuGetGallery0.9.622.11] \ | Минимальная версия среды выполнения WebView2 версии 86.0.616.0.  

#### Общие  

*   > [!IMPORTANT]
    > **Объявление**: Этот пакет SDK является кандидатом на выпуск для WebView2 Win32 C/C++ GA.  В этой версии должен использоваться тот же интерфейс API и функциональные возможности.  

*   Отключенные [политики браузера][DeployedgeMicrosoftEdgePolicies].  
*   Добавлено свойство [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Обновлены `ICoreWebView2NewWindowRequestedEventArgs` для включения свойства [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] и связанного [ICoreWebView2WindowFeatures][ReferenceWin32Icorewebview2windowfeatures09622].  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Обновлен `System.Windows.Rect`  для использования `System.Drawing.Rectangle` вместо `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Событие NewWindowRequested Обновлено для обработки `window.open()` запроса без параметров.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] Set `ICoreWebView2EnvironmentOptions` не переопределяется с помощью переменных среды или значений реестра.  Дополнительные сведения можно найти в [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  

## 0.9.579  

Дата выпуска: 20 июля 2020 г.  

[Пакет NuGet][NuGetGallery0.9.579] \ | Минимальная версия Microsoft Edge 86.0.579.0.  

#### Общие  

*   > [!IMPORTANT]
    > **Объявление**: Evergreen WebView2 среды выполнения и установщик выпущены для предварительного просмотра.  Дополнительные сведения можно найти в разделе [распространение WebView2] [Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
*   > [!IMPORTANT]
    > **Объявление**: после следующего выпуска SDK больше не будут поддерживаться следующие версии SDK WebView2.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Версии SDK WebView2 также помечены как устаревшие на nuget.org.  WebView2 рекомендует поддерживать последние версии WebView2.  

*   Добавлены усовершенствования WebView рабочего потока.  \ ([\ #318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Заблокированное всплывающее окно в WebView.  Для получения дополнительных сведений перейдите к свойству [IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] в `NewWindowRequested` событии.  
*   Убедитесь, что инициировано событие начала навигации в WebView `about:blank` .  Теперь `NavigationStarting` события будут срабатывать для всех переходов, но отмены для `about:blank` srcdoc и Iframes не поддерживаются и не пропускаются.  
*   Заблокированная `edge:// URI` схема в WebView.  
*   Добавлено экспериментальное свойство [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] в параметрах среды WebView2, чтобы включить условный доступ для WebView.  
*   Добавлено экспериментальное событие [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] , которое срабатывает после того, как WebView получил и обработал ответ для запроса на веб-ресурс.  Заголовки проверки подлинности, если таковые имеются, включаются в объект Response.  

#### .NET  

*   Улучшена обработка фокуса WPF.  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Добавлено `ZoomFactor` свойство на контроллере WEBVIEW2 WPF.  

## 0.9.538  

[Пакет NuGet][NuGetGallery0.9.538] \ | Минимальная версия Microsoft Edge 85.0.538.0.  

#### Общие  

*   Удаление поддержки WebView2 версии SDK для [0.8.149](#08149).  WebView2 рекомендует поддерживать последние версии WebView2.  
*   Обновлена групповая политика для учетной записи при изменении пути к профилю в браузере Microsoft Edge \ ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  

#### Win32 C/C++  

*   Добавлена [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538], которая срабатывает при `window.open()` запуске и связана с [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Коренные изменения**: устаревшие [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] и заменены на [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
*   > [!IMPORTANT]
    > **Коренные изменения**: чтобы обеспечить соответствие API WebView2 с соглашениями об именовании Windows API, Группа WebView обновила имена указанных ниже элементов.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] теперь [AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
*   Обновленные [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538] , чтобы убедиться в том, что маркеры сериализатора для исходного объекта узла установлены на прокси-объекты, и сериализованы как объект узла, передаваемый в качестве параметра обратного вызова JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (Предварительная версия 0.9.538)  

*   Выпущены примеры WebView2API для WinForms и WPF, которые являются исчерпывающими руководствами по WebView2 SDK.  Дополнительные сведения можно найти в [репозитории Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Добавлена поддержка визуального размещения и функций окон для [экспериментальных API][ConceptsVersioningExperimentalApis].  
*   > [!IMPORTANT]
    > **Коренные изменения**: следующие РБП теперь реализуют интерфейс IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]и [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   Добавлены [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] и [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] в качестве [CoreWebView2Environment][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] static.  

## предварительный выпуск 0.9.515  

[Пакет NuGet][NuGetGallery0.9.515-prerelease] \ | Минимальная версия Microsoft Edge 84.0.515.0.  

*   > [!IMPORTANT]
    > **Объявление**: WebView2 теперь поддерживает Windows Forms и WPF на платформе .NET Framework 4.6.2 или более поздней версии, а также .net Core 3,0 или более поздней версии в **предварительной версии пакета**.  
*   Дополнительные сведения о создании приложений для WPF можно найти в [руководстве по началу работы с WPF][GettingstartedWpf] и в [справочнике по WPF][DotnetApiMicrosoftWebWebview2Wpf] для API-интерфейсов, относящихся к WPF.  
*   Для получения дополнительных сведений о создании приложений для Windows Forms перейдите в [руководство по началу работы с Windows Forms][GettingstartedWinforms] и [ссылку на Windows][DotnetApiMicrosoftWebWebview2Winforms] Forms для API Windows Forms WebView2.  
*   Чтобы получить дополнительные сведения о API CoreWebView2, перейдите к [ссылке .NET][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Известные проблемы**: команда WebView отслеживает некоторые проблемы в предварительной версии, которые разрешаются в будущих выпусках.  
    > *   **Осведомленность о dpi**: WEBVIEW2 для WPF — в настоящее время не поддерживается dpi.  При инициализации WebView2 для мониторов с высоким разрешением существует известная ситуация, когда WebView сначала инициализируется как часть окна, пока не будет изменен размер окна.  
    > *   **Конструктор WPF**: конструктор WPF в настоящее время не поддерживается.  Добавьте элемент управления WebView2 в свое приложение, напрямую изменив соответствующий XAML в текстовом редакторе.  

## 0.9.488  

[Пакет NuGet][NuGetGallery0.9.488] \ | Минимальная версия Microsoft Edge 84.0.488.0.  

*   > [!IMPORTANT]
    > **Объявление**: начиная с предстоящей версии Microsoft Edge 83, Evergreen WebView больше не ориентирован на стабильный канал браузера.  Вместо этого он указывает на другой набор двоичных файлов с фирменной [Evergreen WebView2 среды выполнения][ConceptsDistributionEvergreenMode], который можно установить с помощью установщика, который в настоящее время разрабатывается группой WebView.  Дополнительные сведения можно найти в разделе [распространение приложений][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Извещение**. команда WebView выпускает два пакета: пакет предварительной версии с экспериментальными API \ (для пробного использования) и стабильный пакет выпусков с стабильными API \ (для вашего доверия).  Чтобы узнать о различиях, перейдите в раздел [Общие сведения о версиях браузеров и WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Коренные изменения**: чтобы обеспечить соответствие API WebView2 с соглашениями об именовании Windows API, Группа WebView обновила имена указанных ниже интерфейсов.  
    > *   `CORE_WEBVIEW2_*` Теперь префикс `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] теперь [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] теперь [get_BrowserVersionString][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488].  
    > *   [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] теперь [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] теперь [RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` Сейчас `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Коренные изменения**: `AddRemoteObject` методы прокси-сервера также переименовываются.  
    > *   `getLocal` Сейчас `getLocalProperty` .  
    > *   `setLocal` Сейчас `setLocalProperty` .  
    > *   `getRemote` Сейчас `getHostProperty` .  
    > *   `setRemote` Сейчас `setHostProperty` .  
    > *   `applyRemote` Сейчас `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Коренные изменения**: устаревшие [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] и заменены на [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
*   Добавлено событие [FrameNavigationCompleted][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488] .  Теперь, когда IFRAME завершает навигацию, инициируется событие, которое возвращает успешное перемещение и идентификатор навигации.  
*   Добавлен интерфейс [ICoreWebView2EnvironmentOptions][ReferenceWin32Icorewebview2environmentoptions09488] , который можно использовать для определения версии среды выполнения WebView2, целью которой является приложение.  
*   Добавлен параметр [IsBuiltInErrorPageEnabled][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488] .  Теперь вы можете включить или отключить встроенную страницу ошибки для навигации в случае сбоя и обработки ошибок процесса отображения.  
*   Обновленный удаленный объект Injection для поддержки `IDispatch` реализаций .NET ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Обновлено событие [NewWindowRequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] для обработки запросов из контекстных меню \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Выпущен первый отдельный пакет предварительной версии WebView2, в который можно получить доступ к API визуального размещения.  Группа WebView обновила [APISample][GithubMicrosoftedgeWebview2samplesMain] , чтобы добавить новые экспериментальные API.  
    *   Добавлен интерфейс [ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] , который подключается к дереву композиции и предоставляет входные данные для WebView.  
    *   Добавлена [ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488], содержащая все данные из a `POINTER_INFO` .  Этот объект передается в SendPointerInput для вставки входных данных указателя в WebView.  
    *   Добавлена [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488], указывающая на то, что приложение будет изменяться при наведении указателя мыши на WebView.  При наведении указателя мыши на текстовое поле в WebView курсор меняется с стрелки на элемент Selector.  `cursor`Свойство в свойстве `CompositionController` сообщает приложению о том, что в данный момент должен находиться указатель мыши для WebView.  

## 0.9.430  

[Пакет NuGet][NuGetGallery0.9.430] \ | Минимальная версия Microsoft Edge 82.0.430.0.  

WebView2 SDK — это официальная бета-версия C++ для Win32, включающая в себя несколько запросов на функции отзыва.  Группа WebView пытается ограничить количество выпусков с коренными изменениями.  Как и в случае с общим доступом, в бета-версии будут включены некоторые существенные коренные изменения.  

*   > [!IMPORTANT]
    > **Коренные изменения**: в последнем выпуске команда WebView переименовала префикс *IWebView2WebView*   в *ICoreWebView2*   , чтобы убедиться, что API WebView2 соответствует соглашению об именовании Windows API.  Кроме того, чтобы использовать пакет WebView2 SDK из платформ пользовательского интерфейса, Группа WebView, разделенная `ICoreWebView2` на [ICoreWebView2][ReferenceWin32Icorewebview209430] и [ICoreWebView2Host][ReferenceWin32Icorewebview2host09430].  `ICoreWebView2Host` Поддержка изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.  ICoreWebView2 поддерживает все другие функции WebView2.  Чтобы узнать больше о том, как внести изменения, перейдите к запросу [WebView2 в][GithubMicrosoftedgeWebview2samplesPr17] проекте WebView2 [APISample][GithubMicrosoftedgeWebview2samplesMain] .  
*   > [!IMPORTANT]
    > **Коренные изменения**: разделение [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] на три компонента:  [SourceChanged][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]и [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  Теперь, когда URL-адрес источника изменит `SourceChanged` событие, будет запущено.  При изменении состояния журнала `HistoryChanged` возникает событие.  `ContentLoading`Событие срабатывает перед начальным сценарием при загрузке нового документа.  
*   Добавлена поддержка архитектуры ARM64.  
*   Добавлена поддержка панели мягкого ввода \ (SIP \) для устройств с сенсорным экраном.  
*   Добавлена поддержка для Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 и Windows Server 2016.  
*   Добавлен [NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430], который позволяет строке состояния отслеживать окно в оконном режиме.  Кроме того, реализуйте это изменение в режиме без окон, чтобы обеспечить доступность функций специальных возможностей.  
*   Добавлены параметры [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] , определяющие, возможен ли доступ к странице для удаленных объектов.  По умолчанию, `AreRemoteObjectsAllowed` это означает, что удаленные объекты, добавленные с помощью [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] , доступны на странице.  Если `AreRemoteObjectsAllowed` этот элемент отключен, объекты недоступны со страницы.  Изменения применяются к следующему событию навигации.  
*   Добавлена настройка [IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] , не позволяющая пользователям влиять на масштаб WebView с помощью `ctrl` + `+` и `ctrl` + `-` \ (или `ctrl` + колесом мыши).  При отключенном параметре Масштаб по-прежнему можно настроить с помощью [put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] .  
*   Измененные ZoomFactor применяются только к текущему WebView.  Изменение масштаба текущего WebView не влияет на другие веб-представления, к которым вы перешли на тот же самый источник.  Дополнительные сведения можно найти в разделе " [get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430]".  
*   Пользовательский интерфейс HID ZoomView для WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Добавлены [SetBoundsAndZoomFactor][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430].  Теперь вы можете задать коэффициент масштабирования и границы WebViewа одновременно.  
*   Добавлено событие [WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] .  Дополнительные сведения можно найти в разделе [add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Добавлена поддержка `beforeunload` типа диалогового окна для событий диалогового окна JavaScript и добавления элемента перечисления [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] .  
*   В [HttpRequestHeaders, HttpResponseHeaders][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] и [get_HasCurrentHeader][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] свойства добавляются [коголовки][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] в HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Коренные изменения: изменение** `DevToolsProtocolEventReceived` поведения.  Теперь вы можете создать [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] для определенного события протокола DevTools и подписаться на него и отказаться от подписки с помощью [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].
*   > [!IMPORTANT]
    > **Коренные изменения**: `WebMessageReceivedEventArgs` [get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] свойство изменено на метод [TryGetWebMessageAsString][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430] .  
*   > [!IMPORTANT]
    > **Коренные изменения**: измененный `AcceleratorKeyPressedEventArgs` метод [обработки][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] на [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] свойство.  

## 0.8.355

[Пакет NuGet][NuGetGallery0.8.355] \ | Минимальная версия Microsoft Edge 80.0.355.0.

*   Выпущен пример WebView2API, подробное руководство по WebView2 SDK.  Дополнительные сведения можно найти в [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Добавлена поддержка IME для всех языков, кроме английского \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   `WebResourceRequested`В ответ на отчеты об ошибках обновлена поверхность API события.  Одновременное указание фильтра и событие для создания теперь не рекомендуются.  Чтобы создать запрашиваемое веб-ресурсом событие, используйте [add_WebResourceRequested][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] , чтобы добавить событие и [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] , чтобы добавить фильтр.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] удаляет фильтр \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Коренные изменения**: изменено поведение во весь экран.  Устаревший [IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190].  Теперь по умолчанию, если элемент в WebView \ (например, видео \) настроен на полный экран, он заполняет границы WebView.  Используйте событие [ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] и [get_ContainsFullScreenElement][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] , чтобы указать, как приложение должно изменить размер WebView, если элемент хочет войти в полноэкранный режим.  

## 0.8.314  

[Пакет NuGet][NuGetGallery0.8.314] \ | Минимальная версия Microsoft Edge 80.0.314.0.  

*   Добавлена поддержка для Windows 7, Windows 8 и Windows 8,1.  
*   Добавлена поддержка отладки кода Visual Studio и Visual Studio для WebView2.  Теперь Проведите отладку вашего сценария в WebView2 прямо из вашей среды разработки.  Дополнительные сведения можно найти в разделе [Отладка при разработке с помощью элементов управления WebView2][HowtoDebug].  
*   Добавлена `Native Object Injection` возможность для сценария, выполняющегося в WebView2, получить доступ к объекту IDispatch из компонента Win32 приложения и получить доступ к свойствам объекта IDispatch.  Дополнительные сведения можно найти в [AddRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения можно найти в разделе [add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Отключено `Context Menus` .  Дополнительные сведения можно найти в разделе [put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Обновлены `DPI Awareness` .  Теперь сведения о DPI в WebView совпадают с определением DPI для ведущего приложения.  
    
    > [!NOTE]
    > Если другое гибридное приложение запускается с определением разрешения DPI, чем исходное WebView, новый WebView не запускается, если каталог данных пользователя совпадает с параметром \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Обновлен `Notification Change Behavior` таким образом, WebView2 автоматически отвергает запросы разрешений на уведомления, заданные в веб-содержимом, расположенном в WebView.  

## 0.8.270  

[Пакет NuGet][NuGetGallery0.8.270] \ | Минимальная версия Microsoft Edge 78.0.270.0.  

*   Добавлено `DocumentTitleChanged` событие для указания на изменение названия документа \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Добавлен `GetWebView2BrowserVersionInfo` API \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Добавлено `NewWindowRequested` событие.  
*   Обновленная `CreateWebView2EnvironmentWithDetails` функция для удаления `releaseChannelPreference` .  Чтобы получить дополнительные сведения о `CreateWebView2EnvironmentWithDetails` функции, перейдите на [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Переопределение реестра и переменной среды по-прежнему поддерживается.  Параметр канала по умолчанию используется, если он не переопределен.  
    Во время поиска по каналам команда WebView пропускает предыдущую версию канала, которая не совместима с WebView2 SDK.  
    Команда WebView выбирает более стабильный канал для обеспечения наибольшего соответствия поведения для конечного пользователя.  При тестировании с использованием последних сборок Канарские необходимо создать сценарий, чтобы задать `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` переменную среды `1` перед запуском приложения.  
*   Функция, которая была обновлена `CreateWebView2EnvironmentWithDetails` с помощью логики для выбора, `userDataFolder` если не указана.  Чтобы получить дополнительные сведения о `CreateWebView2EnvironmentWithDetails` функции, перейдите на [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Если ранее вы использовали расположение по умолчанию `userDataFolder` при переходе на новый пакет SDK, по умолчанию `userDataFolder` используется сброс \ (новое расположение в каталоге host Code \), а состояние также сбрасывается.  
    Если ведущий процесс не имеет разрешения на запись в указанный каталог, эта `CreateWebView2EnvironmentWithDetails` функция может завершиться ошибкой.  Вы можете скопировать данные из старого каталога данных пользователя в новый каталог.  

## 0.8.230  

[Пакет NuGet][NuGetGallery0.8.230] \ | Минимальная версия Microsoft Edge 77.0.230.0.  

*   Добавлен `Stop` API для остановки всех функций навигации и ожидающих выборок ресурсов \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   `.tlb`Файл добавлен в пакет NuGet \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Добавлены проекты .NET в список установщиков в пакете NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Пакет NuGet][NuGetGallery0.8.190] \ | Минимальная версия Microsoft Edge 77.0.190.0.  

*   Добавлены `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` в элемент управления, если пользователи могут открывать DevTools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Добавляется `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` к элементу управления, если отображается строка состояния \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Добавляется `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` для перемещения вперед и назад по журналу переходов.  
*   Добавлены типы заголовков HTTP \ ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) для просмотра и изменения заголовков HTTP в WebView.  
*   Добавлена поддержка 32-bit WebView на 64-разрядных компьютерах \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Добавил WebView IDL в SDK \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Добавлена библиотека для поддержки `IID\_\*` объектов идентификаторов интерфейсов \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Добавлены путь включения, связывание и автокопирование DLL файлов в `TARGET` файл NuGet в SDK.  
*   Включены запросы `window.open()` в сценарии.  

## 0.8.149  

[Пакет NuGet][NuGetGallery0.8.149] \ | Минимальная версия Microsoft Edge 76.0.149.0.  

Первоначальная версия предварительной версии для разработчиков.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Режим распространения с фиксированной версией — распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Знакомство со средой выполнения WebView2 и распространением приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Групповые политики для WebView2ного управления приложениями WebView2 | Документы Microsoft"  
[ConceptsVersioning]: ./concepts/versioning.md "Общие сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Экспериментальные API — основные сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях для Windows Forms | Документы Microsoft"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF | Документы Microsoft"  
[HowtoDebug]: ./howto/debug.md "Отладка при разработке с помощью элементов управления WebView2 | Документы Microsoft"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle-Interface IWebView2AcceleratorKeyPressedEventArgs | Документы Microsoft"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "интерфейс IWebView2ContainsFullScreenElementChangedEventHandler | Документы Microsoft"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-интерфейс IWebView2Settings2 | Документы Microsoft"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-интерфейс IWebView2Settings | Документы Microsoft"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString-интерфейс IWebView2WebMessageReceivedEventArgs | Документы Microsoft"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed-интерфейс IWebView2WebView4 | Документы Microsoft"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged-интерфейс IWebView2WebView | Документы Microsoft"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject-Interface IWebView2WebView4 | Документы Microsoft"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested-интерфейс IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-Interface IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement-интерфейс IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-Interface IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Документы Microsoft"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled-интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs | Документы Microsoft"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo-интерфейс ICoreWebView2Environment | Документы Microsoft"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Документы Microsoft"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor-интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-Interface ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor-интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor-Interface ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader-интерфейс ICoreWebView2HttpHeadersCollectionIterator | Документы Microsoft"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "Коголовки — интерфейс ICoreWebView2HttpRequestHeaders | Документы Microsoft"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "-Интерфейс ICoreWebView2HttpResponseHeaders | Документы Microsoft"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString-Interface ICoreWebView2WebMessageReceivedEventArgs | Документы Microsoft"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Документы Microsoft"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "интерфейс ICoreWebView2EnvironmentOptions | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Microsoft"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalPointerInfo | Документы Microsoft"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Документы Microsoft"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Документы Microsoft"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Документы Microsoft"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Документы Microsoft"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged-интерфейс ICoreWebView2ExperimentalController | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode-интерфейс ICoreWebView2ExperimentalController | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale-интерфейс ICoreWebView2ExperimentalController | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210707PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.707-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges-интерфейс ICoreWebView2ExperimentalController | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft. Web. WebView2. Core | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft. Web. WebView2. WPF | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft. Web. WebView2. WinForms | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2. WebView2RuntimeNotFound (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Класс CoreWebView2 (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Класс CoreWebView2Environment (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Метод CoreWebView2Environment. CompareBrowserVersions (String, String) | (Microsoft. Web. WebView2. Core) | Документы Microsoft"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Метод CoreWebView2Environment. GetAvailableBrowserVersionString (строка) (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Событие CoreWebView2. NewWindowRequested (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Событие CoreWebView2. PermissionRequested (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Событие CoreWebView2. ScriptDialogOpening (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Событие CoreWebView2. WebResourceRequested (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Класс CoreWebView2HttpRequestHeaders (Microsoft. Web. WebView2. Core) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Класс CoreWebView2HttpResponseHeaders (Microsoft. Web. WebView2. Core) | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Класс CoreWebView2CreationProperties (Microsoft. Web. WebView2. WinForms) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2. Source (Microsoft. Web. WebView2. WinForms) | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Метод WebView2. BuildWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Документы Microsoft"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Метод WebView2. DestroyWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "Microsoft. Web. webview2. WPF. webview2. acceleratorkeypressed | Документы Microsoft"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Класс CoreWebView2InitializationCompletedEventArgs | Документы Microsoft"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-интерфейс ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-интерфейс ICoreWebView2ExperimentalEnvironmentOptions | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures-интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWindowFeatures | Документы Microsoft"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated интерфейса ICoreWebView2NewWindowRequestedEventArgs | Документы Microsoft"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Документы Microsoft"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-интерфейс ICoreWebView2EnvironmentOptions | Документы Microsoft"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments-интерфейс ICoreWebView2EnvironmentOptions | Документы Microsoft"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures-интерфейс ICoreWebView2NewWindowRequestedEventArgs | Документы Microsoft"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "интерфейс ICoreWebView2WindowFeatures | Документы Microsoft"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalEnvironment | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent-Interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Документы Microsoft"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded-интерфейс ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-интерфейс ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager-интерфейс ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment-интерфейс ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest-Interface ICoreWebView2Experimental | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalWebResourceResponseView | Документы Microsoft"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "ICoreWebView2ExperimentalWebResourceResponseView-интерфейс Документы Microsoft"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.707-prerelease&preserve-view=true "интерфейс ICoreWebView2ExperimentalCompositionController3 | Документы Microsoft"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge — политики | Документы Microsoft"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 — политики | Документы Microsoft"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Application Guard в защитнике Microsoft (Windows 10) — безопасность Windows | Документы Microsoft"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Класс CancelEventArgs (System. ComponentModel) | Документы Microsoft"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Класс EventArgs (система) | Документы Microsoft"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Строго именованные сборки | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "MicrosoftEdge/WebViewFeedback, подающий отзыв"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Вопрос в репозитории отзывов о MicrosoftEdge/WebViewFeedback 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "MicrosoftEdge/WebViewFeedback в репозитории обратной связи 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "MicrosoftEdgeный и WebViewFeedbackный репозиторий в виде обратной связи 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 250"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 288"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 611"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Репозиторий объявлений для MicrosoftEdge и WebViewAnnouncement, выпуска 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Перемещение проекта для использования новейшего WebView2 SDK 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Образец API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Объявление о доступности общего доступа для Microsoft Edge WebView2 для .NET и метод фиксированного распределения | блог .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Microsoft Edge"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Коллекция NuGet | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Коллекция NuGet | Microsoft. Web. WebView2 v 1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Коллекция NuGet | Microsoft. Web. WebView2 v 1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Коллекция NuGet | Microsoft. Web. WebView2 v 1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 1.0.674"  
[NuGetGallery1.0.707-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.707-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 1.0.707"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Объявление о общей доступности Microsoft Edge WebView2 | Блог Microsoft Edge"  
