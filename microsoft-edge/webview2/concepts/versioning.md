---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 132ccab0f9f378eedd8c83a7404c350161556f2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182397"
---
# <span data-ttu-id="a191b-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="a191b-104">Understand WebView2 SDK versions</span></span>

<span data-ttu-id="a191b-105">Новые версии пакета WebView2 SDK поставляются в тот же Общий тариф, что и браузер Microsoft Edge \ (Chromium \), примерно каждые шесть недель.</span><span class="sxs-lookup"><span data-stu-id="a191b-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="a191b-106">Выпуск и предварительная версия пакета</span><span class="sxs-lookup"><span data-stu-id="a191b-106">Release and prerelease package</span></span>  

<span data-ttu-id="a191b-107">Пакет NuGet WebView2 включает в себя пакет для выпуска и предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a191b-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="a191b-108">Пакет выпусков совместим с переадресацией и содержит [API-интерфейсы C/C++ для Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="a191b-108">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="a191b-109">API в этом SDK полностью поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a191b-109">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="a191b-110">Пакет предварительной версии — это надмножество пакета выпуска с дополнительными компонентами, перечисленными ниже.</span><span class="sxs-lookup"><span data-stu-id="a191b-110">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="a191b-111">API-интерфейсы .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]и [ядро][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="a191b-111">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="a191b-112">Экспериментальные API-интерфейсы: Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="a191b-112">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="a191b-113">Стратегия</span><span class="sxs-lookup"><span data-stu-id="a191b-113">Roadmap</span></span>  

<span data-ttu-id="a191b-114">Пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++.</span><span class="sxs-lookup"><span data-stu-id="a191b-114">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="a191b-115">В будущем пакет выпуска будет содержать все стабильные, поддерживаемые API .NET, когда они станут общедоступными.</span><span class="sxs-lookup"><span data-stu-id="a191b-115">In the future, the release package will contain all stable, supported .NET APIs when they're made generally available.</span></span>  <span data-ttu-id="a191b-116">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые может измениться в зависимости от вашего отзыва.</span><span class="sxs-lookup"><span data-stu-id="a191b-116">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span> 

## <span data-ttu-id="a191b-117">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="a191b-117">Experimental APIs</span></span>  

<span data-ttu-id="a191b-118">Группа WebView ищет Отзывы о экспериментальных API, которые могут быть включены в будущие выпуски.</span><span class="sxs-lookup"><span data-stu-id="a191b-118">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="a191b-119">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="a191b-119">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="a191b-120">Вы можете оценить экспериментальные API-интерфейсы и поделиться обратной связью с помощью [репозитория обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="a191b-120">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="a191b-121">Экспериментальные API-интерфейсы могут быть введены, изменены и удалены из SDK в SDK.</span><span class="sxs-lookup"><span data-stu-id="a191b-121">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="a191b-122">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="a191b-122">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="a191b-123">Экспериментальные API-интерфейсы могут быть недоступны в установленной версии среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="a191b-123">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="a191b-124">Соответствие версий среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="a191b-124">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="a191b-125">Приложения WebView2 требуют от пользователей установить [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="a191b-125">WebView2 applications require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span> <span data-ttu-id="a191b-126">Среда выполнения WebView2 автоматически обновится до последней доступной версии.</span><span class="sxs-lookup"><span data-stu-id="a191b-126">The WebView2 Runtime updates automatically to the latest version that's available.</span></span> <span data-ttu-id="a191b-127">В некоторых сценариях пользователям может потребоваться остановить автоматическое обновление среды выполнения WebView2, что может привести к проблемам с совместимостью приложений.</span><span class="sxs-lookup"><span data-stu-id="a191b-127">In some scenarios, users may need to stop automatic WebView2 Runtime updates, which can cause application compatibility issues.</span></span>

<span data-ttu-id="a191b-128">Если WebView2 обновления среды выполнения остановлены, убедитесь в том, что вы понимаете минимальную версию [среды выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , которая необходима для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="a191b-128">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] that's required by your application.</span></span> <span data-ttu-id="a191b-129">Рассматривайте следующие два элемента:</span><span class="sxs-lookup"><span data-stu-id="a191b-129">Consider the following two items:</span></span>  

1. <span data-ttu-id="a191b-130">Минимальная требуемая версия SDK, которую можно найти в [заметках о выпуске][Releasenotes] WebView2 в разделе " **Минимальная версия среды выполнения WebView2**.</span><span class="sxs-lookup"><span data-stu-id="a191b-130">The minimum required version of the SDK, which can be found in the WebView2 [Release Notes][Releasenotes] under **minimum WebView2 Runtime version**.</span></span> <span data-ttu-id="a191b-131">Например, для SDK версии [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222)необходимо установить либо [среду выполнения WebView2][MicrosoftDeveloperEdgeWebview2] , либо [нестабильный канал Microsoft Edge][MicrosoftedgeinsiderDownload] с номером сборки **86.0.616.0** или более поздней.</span><span class="sxs-lookup"><span data-stu-id="a191b-131">For example, for SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of **86.0.616.0** or later.</span></span> <span data-ttu-id="a191b-132">Минимальный номер версии, необходимый для SDK, будет изменен только в случае критических изменений на веб-платформе.</span><span class="sxs-lookup"><span data-stu-id="a191b-132">The minimum version required by the SDK will only change when there's a breaking change in the web platform.</span></span>

2. <span data-ttu-id="a191b-133">Минимальная требуемая версия пакета NuGet, необходимая для поддержки интерфейсов и API, используемых в вашем приложении.</span><span class="sxs-lookup"><span data-stu-id="a191b-133">The minimum required version of the NuGet package that's required to support the interfaces and APIs used in your app.</span></span> <span data-ttu-id="a191b-134">Новые интерфейсы и API-интерфейсы периодически добавляются в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a191b-134">New interfaces and APIs are added periodically to WebView2.</span></span> <span data-ttu-id="a191b-135">API и интерфейсы, Объединенные в SDK, потребуют разных версий среды выполнения WebView2, так как они были добавлены в пакет SDK в разное время.</span><span class="sxs-lookup"><span data-stu-id="a191b-135">APIs and interfaces bundled in an SDK will require different versions of the WebView2 Runtime because they were added to the SDK at different times.</span></span>  <span data-ttu-id="a191b-136">Требуемая версия среды выполнения WebView2 соответствует номеру сборки (третье число) версии SDK, в которой впервые появился API.</span><span class="sxs-lookup"><span data-stu-id="a191b-136">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span> <span data-ttu-id="a191b-137">Например, для нового API или интерфейса, добавленного в SDK версии [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) , потребуется версия среды выполнения WebView2:86,0. **622**. 0.</span><span class="sxs-lookup"><span data-stu-id="a191b-137">For example, a new API or interface added in SDK version [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) will need the WebView2 Runtime version: 86.0.**622**.0.</span></span> <span data-ttu-id="a191b-138">Для API или интерфейса, добавленного в последующем выпуске SDK, требуется среда выполнения WebView2, имеющая тот же номер версии, что и SDK.</span><span class="sxs-lookup"><span data-stu-id="a191b-138">An API or interface added in a subsequent SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span> <span data-ttu-id="a191b-139">Вы можете определить, поддерживает ли версия среды выполнения WebView2 интерфейс или API с [помощью программных средств](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="a191b-139">You can determine if the WebView2 Runtime version supports an interface or API [programmatically](#determine-webview2-runtime-requirement).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a191b-140">При разработке [приложений Evergreen WebView2](distribution.md#evergreen-distribution-mode)регулярно проверяйте приложение на соответствие последним версиям среды выполнения WebView2 и нестабильным браузерам Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a191b-140">When developing [Evergreen WebView2 applications](distribution.md#evergreen-distribution-mode), regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="a191b-141">Поскольку веб-платформа постоянно развивается, регулярное тестирование является лучшим способом обеспечения надлежащей работы приложения.</span><span class="sxs-lookup"><span data-stu-id="a191b-141">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

### <span data-ttu-id="a191b-142">Определение требований среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="a191b-142">Determine WebView2 Runtime requirement</span></span>

<span data-ttu-id="a191b-143">В зависимости от того, какой пакет SDK вы используете, рассматривайте следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="a191b-143">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="a191b-144">**Win32 C/C++**.</span><span class="sxs-lookup"><span data-stu-id="a191b-144">**Win32 C/C++**.</span></span>  <span data-ttu-id="a191b-145">При использовании `QueryInterface` для получения нового интерфейса проверьте возвращаемое значение `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="a191b-145">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="a191b-146">Это значение может указывать на то, что среда выполнения WebView2 является предыдущей версией и не поддерживает этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a191b-146">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span> <span data-ttu-id="a191b-147">Перейдите к примеру WebView2API, чтобы получить [Пример](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) такого способа работы.</span><span class="sxs-lookup"><span data-stu-id="a191b-147">Navigate to the WebView2API Sample for an [example](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) of how this works.</span></span>
*   <span data-ttu-id="a191b-148">**.NET и WinUI**.</span><span class="sxs-lookup"><span data-stu-id="a191b-148">**.NET and WinUI**.</span></span>  <span data-ttu-id="a191b-149">Проверка наличия `No such interface supported` исключения при использовании методов, свойств и событий, добавленных в последние пакеты SDK.</span><span class="sxs-lookup"><span data-stu-id="a191b-149">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="a191b-150">Это исключение может возникнуть, если среда выполнения WebView2 является предыдущей версией и не поддерживает эти API.</span><span class="sxs-lookup"><span data-stu-id="a191b-150">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="a191b-151">Если API недоступен, расрешите Удаление связанного компонента или сообщите пользователям о том, что им нужно обновить свою версию среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="a191b-151">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  



 

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Пространство имен Microsoft. Web. WebView2. Core | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft. Web. WebView2. WPF | Документы Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft. Web. WebView2. WinForms | Документы Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Разработчик Майкрософт"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  
