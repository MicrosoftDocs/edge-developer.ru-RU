---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191612"
---
# Общие сведения о версиях SDK для WebView2  

Новые версии пакета WebView2 SDK поставляются в тот же Общий тариф, что и браузер Microsoft Edge \ (Chromium \), примерно каждые шесть недель.  

## Выпуск и предварительная версия пакета  

Пакет NuGet WebView2 включает в себя пакет для выпуска и предварительной версии.  

**Пакет выпусков** совместим с переадресацией и содержит следующие компоненты:  

*   [API C/C++ для Win32][ReferenceWin32]
*   API .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace].  
    
API в SDK полностью поддерживаются.  

**Пакет предварительной версии** — это надмножество пакета выпусков с [экспериментальными API](#experimental-apis).  

### Стратегия  

Пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые может измениться в зависимости от вашего отзыва.  

## Экспериментальные API-интерфейсы  

Группа WebView ищет Отзывы о экспериментальных API, которые могут быть включены в будущие выпуски.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Чтобы помочь вам оценить экспериментальные API и поделиться отзывом, перейдите в [репозиторий обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.  Старайтесь не использовать экспериментальные API в производственных приложениях.  

> [!NOTE]
> Экспериментальные API-интерфейсы могут быть недоступны в установленной версии среды выполнения WebView2.  

## Соответствие версий среды выполнения WebView2  
Приложения WebView2 требуют от пользователей установить [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2].  Среда выполнения WebView2 автоматически обновится до последней доступной версии.  В некоторых сценариях пользователи могут отключить автоматическое обновление среды выполнения WebView2, что может привести к проблемам с совместимостью приложений.  

Если WebView2 обновления среды выполнения остановлены, убедитесь, что вы понимаете минимальную версию [среды выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , требуемую вашим приложением.  Рассматривайте следующие два элемента:  

1.  Минимальная необходимая версия SDK, указанная в [заметках о выпуске][Webview2Releasenotes] WebView2 в разделе **Минимальная версия среды выполнения WebView2**.  Например, для SDK версии [1.0.622.22][Webview2Releasenotes1062222]необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload] с номером сборки `86.0.616.0` или более поздней.  Минимальная версия, необходимая для SDK, изменяется только при возникновении критического изменения на веб-платформе.  
1.  Минимальная необходимая версия пакета NuGet, необходимая для поддержки интерфейсов и API-интерфейсов, которые используются в вашем приложении.  Новые интерфейсы и API-интерфейсы периодически добавляются в WebView2.  API и интерфейсы, Объединенные в SDK, используют разные версии среды выполнения WebView2, так как API и интерфейс добавляются в пакет SDK в разное время.  Требуемая версия среды выполнения WebView2 соответствует номеру сборки (третье число) версии SDK, в которой впервые появился API.  Например, для нового API или интерфейса, добавленного в SDK версии [1.0.622.22][Webview2Releasenotes1062222] требуется версия среды выполнения WEBVIEW2:  `86.0.622.0`  API или интерфейс, добавленный в более поздней версии SDK, требует среды выполнения WebView2 с тем же номером версии, что и у SDK.  Чтобы определить, поддерживает ли версия среды выполнения WebView2 интерфейс или API-интерфейс, перейдите в раздел [Определение требования среды выполнения WebView2](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> При разработке [приложений Evergreen WebView2][Webview2ConceptsDistributionEvergreenDistributionMode]регулярно проверяйте свое приложение на соответствие последним версиям среды выполнения WebView2 и нестабильным браузерам Microsoft Edge.  Поскольку веб-платформа постоянно развивается, регулярное тестирование является лучшим способом обеспечения надлежащей работы приложения.  

### Определение требований среды выполнения WebView2  

В зависимости от того, какой пакет SDK вы используете, рассматривайте следующие элементы:  

*   **Win32 C/C++**.  При использовании `QueryInterface` для получения нового интерфейса проверьте возвращаемое значение `E_NOINTERFACE` .  Значение может указывать на то, что среда выполнения WebView2 является предыдущей версией и не поддерживает этот интерфейс.  Чтобы получить пример работы, перейдите к [строке 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.NET и WinUI**.  Проверка наличия `No such interface supported` исключения при использовании методов, свойств и событий, добавленных в последние пакеты SDK.  Исключение может возникнуть, если среда выполнения WebView2 является предыдущей версией и не поддерживает API.  
    
Если API недоступен, расрешите Удаление связанного компонента или сообщите пользователям о том, что требуется обновление среды выполнения WebView2.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Режим распространения Evergreen-распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22 — заметки о выпуске для WebView2 SDK | Документы Microsoft"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft. Web. WebView2. Core | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft. Web. WebView2. WPF | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft. Web. WebView2. WinForms | Документы Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Майкрософт"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Строка 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  
