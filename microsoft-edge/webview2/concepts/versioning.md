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
# <span data-ttu-id="d6a60-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="d6a60-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="d6a60-105">Новые версии пакета WebView2 SDK поставляются в тот же Общий тариф, что и браузер Microsoft Edge \ (Chromium \), примерно каждые шесть недель.</span><span class="sxs-lookup"><span data-stu-id="d6a60-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="d6a60-106">Выпуск и предварительная версия пакета</span><span class="sxs-lookup"><span data-stu-id="d6a60-106">Release and prerelease package</span></span>  

<span data-ttu-id="d6a60-107">Пакет NuGet WebView2 включает в себя пакет для выпуска и предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="d6a60-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="d6a60-108">**Пакет выпусков** совместим с переадресацией и содержит следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="d6a60-108">The **release package** is forward compatible and contains the following components.</span></span>  

*   [<span data-ttu-id="d6a60-109">API C/C++ для Win32</span><span class="sxs-lookup"><span data-stu-id="d6a60-109">Win32 C/C++ APIs</span></span>][ReferenceWin32]
*   <span data-ttu-id="d6a60-110">API .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace].</span><span class="sxs-lookup"><span data-stu-id="d6a60-110">.NET APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span></span>  
    
<span data-ttu-id="d6a60-111">API в SDK полностью поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d6a60-111">APIs in the SDK are fully supported.</span></span>  

<span data-ttu-id="d6a60-112">**Пакет предварительной версии** — это надмножество пакета выпусков с [экспериментальными API](#experimental-apis).</span><span class="sxs-lookup"><span data-stu-id="d6a60-112">The **prerelease package** is a superset of the release package with [Experimental APIs](#experimental-apis).</span></span>  

### <span data-ttu-id="d6a60-113">Стратегия</span><span class="sxs-lookup"><span data-stu-id="d6a60-113">Roadmap</span></span>  

<span data-ttu-id="d6a60-114">Пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.</span><span class="sxs-lookup"><span data-stu-id="d6a60-114">The release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="d6a60-115">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые может измениться в зависимости от вашего отзыва.</span><span class="sxs-lookup"><span data-stu-id="d6a60-115">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span>  

## <span data-ttu-id="d6a60-116">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d6a60-116">Experimental APIs</span></span>  

<span data-ttu-id="d6a60-117">Группа WebView ищет Отзывы о экспериментальных API, которые могут быть включены в будущие выпуски.</span><span class="sxs-lookup"><span data-stu-id="d6a60-117">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="d6a60-118">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="d6a60-118">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="d6a60-119">Чтобы помочь вам оценить экспериментальные API и поделиться отзывом, перейдите в [репозиторий обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="d6a60-119">To help you evaluate the Experimental APIs and share your feedback, navigate to the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="d6a60-120">Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.</span><span class="sxs-lookup"><span data-stu-id="d6a60-120">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="d6a60-121">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="d6a60-121">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="d6a60-122">Экспериментальные API-интерфейсы могут быть недоступны в установленной версии среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="d6a60-122">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="d6a60-123">Соответствие версий среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="d6a60-123">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="d6a60-124">Приложения WebView2 требуют от пользователей установить [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="d6a60-124">WebView2 apps require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span>  <span data-ttu-id="d6a60-125">Среда выполнения WebView2 автоматически обновится до последней доступной версии.</span><span class="sxs-lookup"><span data-stu-id="d6a60-125">The WebView2 Runtime automatically updates to the latest version available.</span></span>  <span data-ttu-id="d6a60-126">В некоторых сценариях пользователи могут отключить автоматическое обновление среды выполнения WebView2, что может привести к проблемам с совместимостью приложений.</span><span class="sxs-lookup"><span data-stu-id="d6a60-126">In some scenarios, users may want to stop automatic WebView2 Runtime updates, which may cause app compatibility issues.</span></span>  

<span data-ttu-id="d6a60-127">Если WebView2 обновления среды выполнения остановлены, убедитесь, что вы понимаете минимальную версию [среды выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , требуемую вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="d6a60-127">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] required by your app.</span></span>  <span data-ttu-id="d6a60-128">Рассматривайте следующие два элемента:</span><span class="sxs-lookup"><span data-stu-id="d6a60-128">Consider the following two items:</span></span>  

1.  <span data-ttu-id="d6a60-129">Минимальная необходимая версия SDK, указанная в [заметках о выпуске][Webview2Releasenotes] WebView2 в разделе **Минимальная версия среды выполнения WebView2**.</span><span class="sxs-lookup"><span data-stu-id="d6a60-129">The minimum required version of the SDK, in found in the WebView2 [Release Notes][Webview2Releasenotes] under **minimum WebView2 Runtime version**.</span></span>  <span data-ttu-id="d6a60-130">Например, для SDK версии [1.0.622.22][Webview2Releasenotes1062222]необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload] с номером сборки `86.0.616.0` или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d6a60-130">For example, for SDK version [1.0.622.22][Webview2Releasenotes1062222], you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of `86.0.616.0` or later.</span></span>  <span data-ttu-id="d6a60-131">Минимальная версия, необходимая для SDK, изменяется только при возникновении критического изменения на веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="d6a60-131">The minimum version required by the SDK only changes when a breaking change occurs in the web platform.</span></span>  
1.  <span data-ttu-id="d6a60-132">Минимальная необходимая версия пакета NuGet, необходимая для поддержки интерфейсов и API-интерфейсов, которые используются в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="d6a60-132">The minimum required version of the NuGet package required to support the interfaces and APIs that you use in your app.</span></span>  <span data-ttu-id="d6a60-133">Новые интерфейсы и API-интерфейсы периодически добавляются в WebView2.</span><span class="sxs-lookup"><span data-stu-id="d6a60-133">New interfaces and APIs are added periodically to WebView2.</span></span>  <span data-ttu-id="d6a60-134">API и интерфейсы, Объединенные в SDK, используют разные версии среды выполнения WebView2, так как API и интерфейс добавляются в пакет SDK в разное время.</span><span class="sxs-lookup"><span data-stu-id="d6a60-134">APIs and interfaces bundled in an SDK require different versions of the WebView2 Runtime, because APIs and interface are added to the SDK at different times.</span></span>  <span data-ttu-id="d6a60-135">Требуемая версия среды выполнения WebView2 соответствует номеру сборки (третье число) версии SDK, в которой впервые появился API.</span><span class="sxs-lookup"><span data-stu-id="d6a60-135">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span>  <span data-ttu-id="d6a60-136">Например, для нового API или интерфейса, добавленного в SDK версии [1.0.622.22][Webview2Releasenotes1062222] требуется версия среды выполнения WEBVIEW2:  `86.0.622.0`  API или интерфейс, добавленный в более поздней версии SDK, требует среды выполнения WebView2 с тем же номером версии, что и у SDK.</span><span class="sxs-lookup"><span data-stu-id="d6a60-136">For example, a new API or interface added in SDK version [1.0.622.22][Webview2Releasenotes1062222] requires the WebView2 Runtime version:  `86.0.622.0`  An API or interface added in a later SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span>  <span data-ttu-id="d6a60-137">Чтобы определить, поддерживает ли версия среды выполнения WebView2 интерфейс или API-интерфейс, перейдите в раздел [Определение требования среды выполнения WebView2](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="d6a60-137">To help you determine if the WebView2 Runtime version supports an interface or API, navigate to [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="d6a60-138">При разработке [приложений Evergreen WebView2][Webview2ConceptsDistributionEvergreenDistributionMode]регулярно проверяйте свое приложение на соответствие последним версиям среды выполнения WebView2 и нестабильным браузерам Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d6a60-138">When developing [Evergreen WebView2 apps][Webview2ConceptsDistributionEvergreenDistributionMode], regularly test your app against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="d6a60-139">Поскольку веб-платформа постоянно развивается, регулярное тестирование является лучшим способом обеспечения надлежащей работы приложения.</span><span class="sxs-lookup"><span data-stu-id="d6a60-139">Because the web platform is constantly evolving, regular testing is the best way to ensure your app performs as intended.</span></span>  

### <span data-ttu-id="d6a60-140">Определение требований среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="d6a60-140">Determine WebView2 Runtime requirement</span></span>  

<span data-ttu-id="d6a60-141">В зависимости от того, какой пакет SDK вы используете, рассматривайте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="d6a60-141">Depending on which SDK you use, consider the following items:</span></span>  

*   <span data-ttu-id="d6a60-142">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="d6a60-142">**Win32 C/C++**.</span></span>  <span data-ttu-id="d6a60-143">При использовании `QueryInterface` для получения нового интерфейса проверьте возвращаемое значение `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="d6a60-143">When using `QueryInterface` to obtain a new interface, verify a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="d6a60-144">Значение может указывать на то, что среда выполнения WebView2 является предыдущей версией и не поддерживает этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d6a60-144">The value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  <span data-ttu-id="d6a60-145">Чтобы получить пример работы, перейдите к [строке 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span><span class="sxs-lookup"><span data-stu-id="d6a60-145">For an example of how it works, navigate to [Line 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span></span>  
*   <span data-ttu-id="d6a60-146">**.NET и WinUI**.</span><span class="sxs-lookup"><span data-stu-id="d6a60-146">**.NET and WinUI**.</span></span>  <span data-ttu-id="d6a60-147">Проверка наличия `No such interface supported` исключения при использовании методов, свойств и событий, добавленных в последние пакеты SDK.</span><span class="sxs-lookup"><span data-stu-id="d6a60-147">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="d6a60-148">Исключение может возникнуть, если среда выполнения WebView2 является предыдущей версией и не поддерживает API.</span><span class="sxs-lookup"><span data-stu-id="d6a60-148">The exception may occur when the WebView2 Runtime is a previous version, and does not support the APIs.</span></span>  
    
<span data-ttu-id="d6a60-149">Если API недоступен, расрешите Удаление связанного компонента или сообщите пользователям о том, что требуется обновление среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="d6a60-149">If an API is unavailable, consider removing the associated feature, or inform your users that an update to the WebView2 Runtime is required.</span></span>  

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
