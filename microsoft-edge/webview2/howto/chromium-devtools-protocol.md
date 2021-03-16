---
description: Узнайте, как использовать протокол Chrome DevTools в приложениях WebView2 с помощью пакета Microsoft Edge WebView2 Chromium DevTools Protocol NuGet
title: Использование протокола Chrome DevTools в WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 0f7a2dd4bb3b1621e854cd4c0c5410e64d3c03ff
ms.sourcegitcommit: 0ef5bb3933cde8a466f2931b824f07b4995cfe5e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "11409326"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a><span data-ttu-id="48a6d-104">Использование протокола Chromium DevTools в WebView2</span><span class="sxs-lookup"><span data-stu-id="48a6d-104">Use Chromium DevTools Protocol in WebView2</span></span>  

<span data-ttu-id="48a6d-105">Протокол [Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] предоставляет API для инструментов, проверки, отладки и браузеров на основе профилей на основе хрома.</span><span class="sxs-lookup"><span data-stu-id="48a6d-105">The [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] provides APIs to instrument, inspect, debug, and profile Chromium-based browsers.</span></span>  <span data-ttu-id="48a6d-106">Протокол Chromium DevTools является основой для Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a6d-106">The Chromium DevTools Protocol is the foundation for the Microsoft Edge \(Chromium\) DevTools.</span></span>  <span data-ttu-id="48a6d-107">Используйте протокол Chromium DevTools для функций, которые не реализованы на платформе WebView2.</span><span class="sxs-lookup"><span data-stu-id="48a6d-107">Use the Chromium DevTools Protocol for features that aren't implemented in the WebView2 platform.</span></span>  <span data-ttu-id="48a6d-108">Дополнительные сведения о функциональных возможностях протокола Chromium DevTools перейдите в [протокол Chromium DevTools.][GitHubChromedevtoolsDevtoolsProtocol]</span><span class="sxs-lookup"><span data-stu-id="48a6d-108">For more information about the Chromium DevTools Protocol functionality, navigate to [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span></span>  

> [!CAUTION]
> <span data-ttu-id="48a6d-109">Команда Microsoft Edge WebView2 не поддерживает и не поддерживает протокол Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a6d-109">The Microsoft Edge WebView2 team does not maintain or support the Chromium DevTools Protocol.</span></span>  <span data-ttu-id="48a6d-110">Протокол Chromium DevTools поддерживается проектом Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="48a6d-110">The Chromium DevTools Protocol is maintained by the open source Chromium project.</span></span>  
> 
> <span data-ttu-id="48a6d-111">Чтобы отправить свои предложения по будущим функциям платформы WebView2, перейдите к [отзыву WebView][GithubMicrosoftedgeWebview2feedback] и отправьте проблему.</span><span class="sxs-lookup"><span data-stu-id="48a6d-111">To send your suggestions for future WebView2 platform features, navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and submit an issue.</span></span>  

<span data-ttu-id="48a6d-112">Чтобы использовать API протокола Chromium DevTools в WebView2, используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="48a6d-112">To use the Chromium DevTools Protocol API in WebView2, use either of the following actions.</span></span>  

*   <span data-ttu-id="48a6d-113">Установите и используйте [пакет Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="48a6d-113">Install and use the [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).</span></span>  
*   <span data-ttu-id="48a6d-114">Запустите один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="48a6d-114">Run one of the following methods.</span></span>  
    *   <span data-ttu-id="48a6d-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span><span class="sxs-lookup"><span data-stu-id="48a6d-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span></span>  
    *   <span data-ttu-id="48a6d-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span><span class="sxs-lookup"><span data-stu-id="48a6d-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span></span>  
    
## <a name="use-devtoolsprotocolhelper-preview"></a><span data-ttu-id="48a6d-117">Использование DevToolsProtocolHelper (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="48a6d-117">Use DevToolsProtocolHelper (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="48a6d-118">Пакет [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet в настоящее время находится в техническом режиме.</span><span class="sxs-lookup"><span data-stu-id="48a6d-118">The [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package is currently in technical preview.</span></span>  <span data-ttu-id="48a6d-119">Во время предварительного просмотра воздержаться от использования пакета в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="48a6d-119">While in preview, refrain from using the package in production apps.</span></span>

<span data-ttu-id="48a6d-120">[Microsoft.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] — это пакет NuGet, созданный командой WebView2, который обеспечивает легкий доступ к функциям протокола Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a6d-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] is a NuGet package created by the WebView2 team that provides easy access to Chromium DevTools Protocol features.</span></span>  <span data-ttu-id="48a6d-121">В следующих примерах описывается использование функции геолокации в протоколе Chromium DevTools в вашем контроле WebView2.</span><span class="sxs-lookup"><span data-stu-id="48a6d-121">The following examples describe how to use the geolocation functionality in Chromium DevTools Protocol in your WebView2 control.</span></span>  <span data-ttu-id="48a6d-122">Вы можете следовать аналогичному шаблону, чтобы использовать другие функции протокола Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a6d-122">You may follow a similar pattern to use other Chromium DevTools Protocol features.</span></span>  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a><span data-ttu-id="48a6d-123">Шаг 1. Создание веб-страницы для поиска геолокации</span><span class="sxs-lookup"><span data-stu-id="48a6d-123">Step 1: Create a webpage to find your geolocation</span></span>  

<span data-ttu-id="48a6d-124">Чтобы создать `HTML file` геолокацию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="48a6d-124">To create an `HTML file` to find your geolocation, complete following the actions.</span></span>  

1.  <span data-ttu-id="48a6d-125">Откройте Visual Studio \(или IDE по вашему выбору\).</span><span class="sxs-lookup"><span data-stu-id="48a6d-125">Open Visual Studio Code \(or an IDE of your choice\).</span></span>  
1.  <span data-ttu-id="48a6d-126">Создайте новый `.html` файл.</span><span class="sxs-lookup"><span data-stu-id="48a6d-126">Create a new `.html` file.</span></span>  
1.  <span data-ttu-id="48a6d-127">Скопируйте и вклейте в новый файл следующий фрагмент `.html` кода.</span><span class="sxs-lookup"><span data-stu-id="48a6d-127">Copy and paste the following code snippet in your new `.html` file.</span></span>  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Geolocation Finder</title>
    </head>
    <body>
        <button id="display">Display Location</button>
        <div id="message"></div>
    </body>
    
    <script>
        const btn = document.getElementById('display');
        // Find the user location.
        btn.addEventListener('click', function () {
            navigator.geolocation.getCurrentPosition(onSuccess, onError);
        });
        
        // Update message to display the latitude and longitude coordinates.
        function onSuccess(position) {
            const {latitude, longitude} = position.coords;
            message.textContent = `Your location: (${latitude},${longitude})`;
        }
        
        function onError() {
            message.textContent = `Operation Failed`;
        }
    </script>
    </html>
    ```  
    
1.  <span data-ttu-id="48a6d-128">Сохраните `.html` файл с помощью имени `geolocation.html` файла.</span><span class="sxs-lookup"><span data-stu-id="48a6d-128">Save the `.html` file with the filename `geolocation.html`.</span></span>  
1.  <span data-ttu-id="48a6d-129">Откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="48a6d-129">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="48a6d-130">Откройте файл `geolocation.html`.</span><span class="sxs-lookup"><span data-stu-id="48a6d-130">Open the `geolocation.html` file.</span></span>  
1.  <span data-ttu-id="48a6d-131">Чтобы отобразить координаты широты и долготы, выберите кнопку **Расположение отображения.**</span><span class="sxs-lookup"><span data-stu-id="48a6d-131">To display your latitude and longitude coordinates, choose the **Display Location** button.</span></span>  <span data-ttu-id="48a6d-132">Чтобы проверить и сравнить геолокацию, скопируйте и вклейте [https://www.bing.com/maps][BingMaps] координаты.</span><span class="sxs-lookup"><span data-stu-id="48a6d-132">To verify and compare your geolocation, copy and paste your coordinates in [https://www.bing.com/maps][BingMaps].</span></span>  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Отображение координат геолокации пользователя в Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       <span data-ttu-id="48a6d-134">Отображение координат геолокации пользователя в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="48a6d-134">Display the geolocation coordinates of the user in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a><span data-ttu-id="48a6d-135">Шаг 2. Отображение geolocation.html в WebView2</span><span class="sxs-lookup"><span data-stu-id="48a6d-135">Step 2: Display geolocation.html in a WebView2</span></span>  

1.  <span data-ttu-id="48a6d-136">Чтобы создать приложение WebView2, используйте следующие руководства по началу работы или примеры WebView2.</span><span class="sxs-lookup"><span data-stu-id="48a6d-136">To create a WebView2 app, use either of the following getting started guides or WebView2 samples.</span></span>  
    *   [<span data-ttu-id="48a6d-137">Начало работы с WebView2 в формах Windows</span><span class="sxs-lookup"><span data-stu-id="48a6d-137">Getting Started with WebView2 in Windows Forms</span></span>][Webview2GettingstartedWinforms]  
    *   [<span data-ttu-id="48a6d-138">Начало работы с WebView2 в WPF</span><span class="sxs-lookup"><span data-stu-id="48a6d-138">Getting Started with WebView2 in WPF</span></span>][Webview2GettingstartedWpf]  
    *   [<span data-ttu-id="48a6d-139">Примеры WebView2</span><span class="sxs-lookup"><span data-stu-id="48a6d-139">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
        
1.  <span data-ttu-id="48a6d-140">Установите начальную навигацию управления WebView2 `geolocation.html` для .</span><span class="sxs-lookup"><span data-stu-id="48a6d-140">Set the initial navigation of the WebView2 control to `geolocation.html`.</span></span>  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  <span data-ttu-id="48a6d-141">`geolocation.html`Убедитесь, что файл отображается в вашем приложении управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="48a6d-141">Ensure the `geolocation.html` file displays in your WebView2 control app.</span></span>  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Отображение файла geolocater.html в вашем приложении управления WebView2" lightbox="./media/initial-geolocate.png":::
       <span data-ttu-id="48a6d-143">Отображение файла `geolocation.html` в приложении управления WebView2</span><span class="sxs-lookup"><span data-stu-id="48a6d-143">Display the `geolocation.html` file in your WebView2 control app</span></span>  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a><span data-ttu-id="48a6d-144">Шаг 3. Установка пакета DevToolsProtocolHelper NuGet</span><span class="sxs-lookup"><span data-stu-id="48a6d-144">Step 3: Install the DevToolsProtocolHelper NuGet package</span></span>  

<span data-ttu-id="48a6d-145">Использование NuGet для загрузки `Microsoft.Web.WebView2.DevToolsProtocolExtension` .</span><span class="sxs-lookup"><span data-stu-id="48a6d-145">Use NuGet to download `Microsoft.Web.WebView2.DevToolsProtocolExtension`.</span></span>  <span data-ttu-id="48a6d-146">Чтобы установить пакет, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="48a6d-146">To install the package, complete the following actions.</span></span>  

1.  <span data-ttu-id="48a6d-147">Выберите **Project**  >  **Manage NuGet Packages**  >  **Browse**.</span><span class="sxs-lookup"><span data-stu-id="48a6d-147">Choose **Project** > **Manage NuGet Packages** > **Browse**.</span></span>  
1.  <span data-ttu-id="48a6d-148">Введите `Microsoft.Web.WebView2.DevToolsProtocolExtension` и выберите **Установку Microsoft.Web.WebView2.DevToolsProtocolExtension.**  >  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="48a6d-148">Type `Microsoft.Web.WebView2.DevToolsProtocolExtension` and choose **Microsoft.Web.WebView2.DevToolsProtocolExtension** > **Install**.</span></span>   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Убедитесь, что дисплеи Microsoft.Web.WebView2.DevToolsProtocolExtension отображаются в Visual Studio NuGet диспетчер пакетов" lightbox="./media/cdpnuget.png":::
   <span data-ttu-id="48a6d-150">Убедитесь, что **дисплеи Microsoft.Web.WebView2.DevToolsProtocolExtension** отображаются в Visual Studio NuGet диспетчер пакетов</span><span class="sxs-lookup"><span data-stu-id="48a6d-150">Ensure **Microsoft.Web.WebView2.DevToolsProtocolExtension** displays in the Visual Studio NuGet Package Manager</span></span>  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a><span data-ttu-id="48a6d-151">Шаг 4. Использование помощника протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="48a6d-151">Step 4: Use DevTools Protocol Helper</span></span>  

1.  <span data-ttu-id="48a6d-152">Добавьте пространство `DevToolsProtocolExtension` имен в проект.</span><span class="sxs-lookup"><span data-stu-id="48a6d-152">Add the `DevToolsProtocolExtension` namespace to your project.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  <span data-ttu-id="48a6d-153">Instantiate объект `DevToolsProtocolHelper` и перейдите к `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="48a6d-153">Instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html`.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  <span data-ttu-id="48a6d-154">Запустите [метод setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="48a6d-154">Run the [setGeoLocationOverrideAsync][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] method.</span></span>  <span data-ttu-id="48a6d-155">Дополнительные сведения можно найти в [setGeolocationOverride.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="48a6d-155">For more information, navigate to [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webview.CoreWebView2.GetDevToolsProtocolHelper();
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
        
        // Latitude and longitude for Paris, France.
        double latitude = 48.857024082572565;  
        double longitude = 2.3161581601457386;  
        double accuracy = 1;
        await helper.Emulation.setGeolocationOverrideAsync(latitude, longitude, accuracy);
        
    }
    ```  
    
1.  <span data-ttu-id="48a6d-156">Запустите приложение.</span><span class="sxs-lookup"><span data-stu-id="48a6d-156">Run your app.</span></span>  
1.  <span data-ttu-id="48a6d-157">Чтобы отобразить координаты Парижа, Франция, выберите кнопку **Расположение отображения.**</span><span class="sxs-lookup"><span data-stu-id="48a6d-157">To display the coordinates of Paris, France, choose the **Display Location** button.</span></span>  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Отображение файла .html в элементе управления WebView2 с координатами для Парижа" lightbox="./media/finallocation-cdp.png":::
       <span data-ttu-id="48a6d-159">Отображение файла `.html` в системе управления WebView2 с координатами для Парижа</span><span class="sxs-lookup"><span data-stu-id="48a6d-159">Display the `.html` file in a WebView2 control with the coordinates for Paris</span></span>  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a><span data-ttu-id="48a6d-160">Файл ошибки протокола Chromium DevTools</span><span class="sxs-lookup"><span data-stu-id="48a6d-160">File a Chromium DevTools Protocol bug</span></span>  

<span data-ttu-id="48a6d-161">Команда WebView2 не владеет протоколом Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a6d-161">The WebView2 team doesn't own the Chromium DevTools Protocol.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="48a6d-162">Прямая обратная связь и ошибки в репо Chromium Issues.</span><span class="sxs-lookup"><span data-stu-id="48a6d-162">Direct feedback and bugs to the Chromium Issues repo.</span></span>  

<span data-ttu-id="48a6d-163">Чтобы выполнить ошибку или проблему протокола Chromium DevTools, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="48a6d-163">To file a Chromium DevTools Protocol bug or issue, complete the following actions.</span></span>  

1.  <span data-ttu-id="48a6d-164">Файл отчета [об ошибке][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span><span class="sxs-lookup"><span data-stu-id="48a6d-164">File a [bug report][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span></span>  
1.  <span data-ttu-id="48a6d-165">Перейдите к [обратной связи WebView][GithubMicrosoftedgeWebview2feedback] и откройте новую проблему.</span><span class="sxs-lookup"><span data-stu-id="48a6d-165">Navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and open a new issue.</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="48a6d-166">См. также</span><span class="sxs-lookup"><span data-stu-id="48a6d-166">See also</span></span>  

*   [<span data-ttu-id="48a6d-167">Примеры WebView2</span><span class="sxs-lookup"><span data-stu-id="48a6d-167">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Начало работы с WebView2 в Windows Forms | Документы Майкрософт"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Начало работы с WebView2 в WPF | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Метод CoreWebView2.GetDevToolsProtocolEventReceiver(String) метод | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Метод CoreWebView2.CallDevToolsProtocolMethodAsync (String, String) метод | Документы Майкрософт"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod — интерфейс ICoreWebView2 | Документы Майкрософт"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Майкрософт"  

[BingMaps]: https://www.bing.com/maps "Карты Bing"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Протокол Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride — протокол Chrome DevTools Protocol | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "Веб-отзывы | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Примеры WebView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Отчет об ошибках | Chromium Bugs"  

[NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://int.nugettest.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | Галерея Qa NuGet"  
