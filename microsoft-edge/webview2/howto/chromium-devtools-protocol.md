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
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Использование протокола Chromium DevTools в WebView2  

Протокол [Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] предоставляет API для инструментов, проверки, отладки и браузеров на основе профилей на основе хрома.  Протокол Chromium DevTools является основой для Microsoft Edge \(Chromium\) DevTools.  Используйте протокол Chromium DevTools для функций, которые не реализованы на платформе WebView2.  Дополнительные сведения о функциональных возможностях протокола Chromium DevTools перейдите в [протокол Chromium DevTools.][GitHubChromedevtoolsDevtoolsProtocol]  

> [!CAUTION]
> Команда Microsoft Edge WebView2 не поддерживает и не поддерживает протокол Chromium DevTools.  Протокол Chromium DevTools поддерживается проектом Chromium с открытым исходным кодом.  
> 
> Чтобы отправить свои предложения по будущим функциям платформы WebView2, перейдите к [отзыву WebView][GithubMicrosoftedgeWebview2feedback] и отправьте проблему.  

Чтобы использовать API протокола Chromium DevTools в WebView2, используйте одно из следующих действий.  

*   Установите и используйте [пакет Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet \(.NET\).  
*   Запустите один из следующих методов.  
    *   .NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Использование DevToolsProtocolHelper (Предварительная версия)

> [!NOTE]
> Пакет [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet в настоящее время находится в техническом режиме.  Во время предварительного просмотра воздержаться от использования пакета в производственных приложениях.

[Microsoft.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] — это пакет NuGet, созданный командой WebView2, который обеспечивает легкий доступ к функциям протокола Chromium DevTools.  В следующих примерах описывается использование функции геолокации в протоколе Chromium DevTools в вашем контроле WebView2.  Вы можете следовать аналогичному шаблону, чтобы использовать другие функции протокола Chromium DevTools.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Шаг 1. Создание веб-страницы для поиска геолокации  

Чтобы создать `HTML file` геолокацию, выполните следующие действия.  

1.  Откройте Visual Studio \(или IDE по вашему выбору\).  
1.  Создайте новый `.html` файл.  
1.  Скопируйте и вклейте в новый файл следующий фрагмент `.html` кода.  
    
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
    
1.  Сохраните `.html` файл с помощью имени `geolocation.html` файла.  
1.  Откройте Microsoft Edge.  
1.  Откройте файл `geolocation.html`.  
1.  Чтобы отобразить координаты широты и долготы, выберите кнопку **Расположение отображения.**  Чтобы проверить и сравнить геолокацию, скопируйте и вклейте [https://www.bing.com/maps][BingMaps] координаты.  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Отображение координат геолокации пользователя в Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       Отображение координат геолокации пользователя в Microsoft Edge  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a>Шаг 2. Отображение geolocation.html в WebView2  

1.  Чтобы создать приложение WebView2, используйте следующие руководства по началу работы или примеры WebView2.  
    *   [Начало работы с WebView2 в формах Windows][Webview2GettingstartedWinforms]  
    *   [Начало работы с WebView2 в WPF][Webview2GettingstartedWpf]  
    *   [Примеры WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Установите начальную навигацию управления WebView2 `geolocation.html` для .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  `geolocation.html`Убедитесь, что файл отображается в вашем приложении управления WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Отображение файла geolocater.html в вашем приложении управления WebView2" lightbox="./media/initial-geolocate.png":::
       Отображение файла `geolocation.html` в приложении управления WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Шаг 3. Установка пакета DevToolsProtocolHelper NuGet  

Использование NuGet для загрузки `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Чтобы установить пакет, выполните следующие действия.  

1.  Выберите **Project**  >  **Manage NuGet Packages**  >  **Browse**.  
1.  Введите `Microsoft.Web.WebView2.DevToolsProtocolExtension` и выберите **Установку Microsoft.Web.WebView2.DevToolsProtocolExtension.**  >  ****   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Убедитесь, что дисплеи Microsoft.Web.WebView2.DevToolsProtocolExtension отображаются в Visual Studio NuGet диспетчер пакетов" lightbox="./media/cdpnuget.png":::
   Убедитесь, что **дисплеи Microsoft.Web.WebView2.DevToolsProtocolExtension** отображаются в Visual Studio NuGet диспетчер пакетов  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a>Шаг 4. Использование помощника протокола DevTools  

1.  Добавьте пространство `DevToolsProtocolExtension` имен в проект.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  Instantiate объект `DevToolsProtocolHelper` и перейдите к `geolocation.html` .  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  Запустите [метод setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  Дополнительные сведения можно найти в [setGeolocationOverride.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  
    
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
    
1.  Запустите приложение.  
1.  Чтобы отобразить координаты Парижа, Франция, выберите кнопку **Расположение отображения.**  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Отображение файла .html в элементе управления WebView2 с координатами для Парижа" lightbox="./media/finallocation-cdp.png":::
       Отображение файла `.html` в системе управления WebView2 с координатами для Парижа  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Файл ошибки протокола Chromium DevTools  

Команда WebView2 не владеет протоколом Chromium DevTools.  

> [!IMPORTANT]
> Прямая обратная связь и ошибки в репо Chromium Issues.  

Чтобы выполнить ошибку или проблему протокола Chromium DevTools, выполните следующие действия.  

1.  Файл отчета [об ошибке][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].  
1.  Перейдите к [обратной связи WebView][GithubMicrosoftedgeWebview2feedback] и откройте новую проблему.  
    
## <a name="see-also"></a>См. также  

*   [Примеры WebView2][GithubMicrosoftedgeWebview2samples]  
    
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
