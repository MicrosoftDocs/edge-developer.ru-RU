---
description: Руководство по началу работы с WebView2 для приложений WPF
title: Начало работы с WebView2 для приложений WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, wpf apps, wpf, edge, CoreWebView2, элемент управления браузером, html edge, начало работы, начало работы, .NET
ms.openlocfilehash: de67b8a2da8cda0339b5e8d0b96cf4c3df260ec6
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306147"
---
# Начало работы с WebView2 в WPF

В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Дополнительные сведения об отдельных API можно найти в [справочнике по API.][DotnetApiMicrosoftWebWebview2Wpf]  

## Предварительные условия  

Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.  

*   [WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).  
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 или более поздней.  
    
## Шаг 1. Создание одноокнего приложения  

Начните с базового проекта настольного компьютера, который содержит одно главное окно.  

1.  В Visual Studio выберите **WPF .NET Core App** \(или **WPF .NET Framework App**\) > **Далее.**  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF core":::
             WPF core :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             WPF Framework :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  Введите значения для **имени и расположения** **проекта.**  Выберите **.NET Framework 4.6.2 или более** поздней \(или **.NET Core 3.0 или** более поздней\).  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Создание ядра":::
                 Создание ядра :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Create Framework":::
                 Create Framework :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  Чтобы создать проект, выберите **"Создать".**  
    
## Шаг 2. Установка SDK WebView2  

Добавьте в проект SDK WebView2 с помощью NuGet.  

1.  Наведите курсор на проектив, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт "Управление пакетами **NuGet"...**  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       Управление пакетами NuGet
    :::image-end:::
    
1.  В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Вы готовы приступить к разработке приложений с помощью API WebView2.  Чтобы построить и запустить проект, выберите `F5` .  Запущенный проект отображает пустое окно.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Пустое приложение":::
       Пустое приложение
    :::image-end:::  
    
## Шаг 3. Создание одного веб-view в MainWindow.xaml  

Затем добавьте WebView в приложение.  

1.  Чтобы добавить `MainWindow.xaml` пространство имен XAML WebView2 в файл, вставьте следующую строку в `<Window/>` тег.  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    Убедитесь, что код `MainWindow.xaml` в коде выглядит следующим фрагментом кода.  
    
    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
    >
        <Grid>
        
        </Grid>
    </Window>
    ```  
    
1.  Чтобы добавить управление WebView2, замените теги на `<Grid>` следующий фрагмент кода.  Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  Чтобы выполнить сборку и запустить проект, выберите "Убедитесь, что ваш control `F5`  WebView2 [https://www.microsoft.com][|::ref1::|Main] отображается".  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       Microsoft.com
    :::image-end:::  
    
## Шаг 4. Навигация  

Добавьте возможность разрешить пользователям изменять URL-адрес, отображаемый в веб-функции Управления WebView2, добавив адресную стойку в приложение.

1.  В файле добавьте адресную планку, скопируя и впавив в него следующий фрагмент `MainWindow.xaml` `<DockPanel>` кода.  
    
    ```xml
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo"
                DockPanel.Dock="Right"
                Click="ButtonGo_Click"
                Content="Go"
        />
        <TextBox Name="addressBar"/>
    </DockPanel>
    ```  
    
    `<DockPanel>`Убедитесь, что раздел файла соответствует `MainWindow.xaml` следующему фрагменту кода.  
    
    ```xml
    <DockPanel>
        <DockPanel DockPanel.Dock="Top">
            <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
            <TextBox Name = "addressBar"/>
        </DockPanel>
        <wv2:WebView2 Name = "webView"
                      Source = "https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  В Visual Studio файле, чтобы добавить пространство имен, вставьте следующий фрагмент кода `MainWindow.xaml.cs` `CoreWebView2` вверху.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  Скопируйте в файл следующий фрагмент кода, чтобы создать метод, который переходит в WebView по URL-адресу, `MainWindow.xaml.cs` `ButtonGo_Click` введенного в адресной панели.  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    Чтобы построить и запустить проект, выберите `F5` .  Введите новый URL-адрес в адресной панели и выберите **"Перейти".**  Например, введите `https://www.bing.com`.  Убедитесь, что с помощью управления WebView2 можно перейти по URL-адресу.  
    
    > [!NOTE]
    > Убедитесь, что в адресной панели введен полный URL-адрес.  Если URL-адрес не начинается с или . `ArgumentException` `http://` `https://`  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       bing.com
    :::image-end:::
    
## Шаг 5. События навигации  

Во время навигации на веб-странице с помощью управления WebView2 вызываются события.  Приложение, в котором размещены элементы управления WebView2, прослушивает следующие события.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Дополнительные сведения можно найти в [меню "События навигации".][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   События навигации
:::image-end:::  

При ошибке возникают следующие события, которые могут зависеть от навигации на веб-страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.  

Чтобы продемонстрировать, как использовать события, зарегистрируйте обработок, который отменяет все запросы, не `NavigationStarting` относя такие как HTTPS.  

В файле измените конструктор в соответствии со следующим фрагментом кода и `MainWindow.xaml.cs` добавьте `EnsureHttps` функцию.  

```csharp
public MainWindow()
{
    InitializeComponent();
    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

В конструкторе EnsureHttps регистрируется как обработчик событий в событии `NavigationStarting` в control WebView2.  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что при переходе к http-сайту Веб-просмотр остается без изменений.  Однако WebView переходит на сайты HTTPS.  

## Шаг 6. Сценарии  

Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.  Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.  Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.  Введенный JavaScript работает с определенными сроками.  

*   Запустите его после создания глобального объекта.  
*   Запустите его перед запуском любого другого сценария, включенного в HTML-документ.  

В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.  Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее метод ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что приложение отображает оповещение при переходе на веб-сайт, который не использует ПРОТОКОЛ HTTPS.  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   HTTPS
:::image-end:::  

## Шаг 7. Взаимодействие между хост-контентом и веб-контентом  

Содержимое хоста и веб-сайта может взаимодействовать друг с другом следующим `postMessage` образом:  

*   Веб-содержимое в веб-окте управления WebView2 может отправлять сообщение на хост с помощью `window.chrome.webview.postMessage` .  The host handles the message using any registered `WebMessageReceived` on the host.  
*   Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .  Эти сообщения перехвачены обработчиками, добавленными в `window.chrome.webview.addEventListener` .  

Механизм связи передает сообщения из веб-содержимого на хост с использованием своих возможностей.  

В проекте при переходе по URL-адресу с помощью управления WebView2 он отображает URL-адрес в адресной панели и оповещает пользователя об URL-адресе, отображаемом в веб-интерфейсе2.  

1.  В файле обновите конструктор и создайте функцию, которая `MainWindow.xaml.cs` `InitializeAsync` будет соответствовать следующему фрагменту кода.  Функция `InitializeAsync` ожидает [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) так как инициализация `CoreWebView2` является асинхронной.  
    
    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }
    
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  После **инициализации CoreWebView2** зарегистрируйте обработец событий для `WebMessageReceived` ответа.  В `MainWindow.xaml.cs` , обновить и добавить с помощью следующего `InitializeAsync` `UpdateAddressBar` фрагмента кода.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }
    
    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Чтобы webView отправил веб-сообщение после инициализации и реагировал на `CoreWebView2` него, хост:  
    1.  Внедряет сценарий в веб-содержимое, которое регистрирует обработок для печати сообщения с ведущего приложения.  
    1.  Внедряет сценарий в веб-содержимое, которое публикует URL-адрес на хост-сайте.  
        
    В `MainWindow.xaml.cs` файле `InitializeAsync` обновим, чтобы он совпадал со следующим фрагментом кода.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    Чтобы выполнить сборку и запустить приложение, выберите `F5` .  Теперь в адресной панели отображается URI в control WebView2.  При успешном переходе к новому URI веб-часть управления WebView2 оповещает пользователя об URI, отображаемом в этом ОКБ WebView2.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       addressBar
    :::image-end:::

Поздравляем, вы создали свое первое приложение WebView2.  

## Дальнейшие действия  

Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.  

### См. также  

*   Полный пример возможностей WebView2 можно найти в репозитарии [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] на GitHub.  
*   Дополнительные сведения об API WebView2 можно найти в справочнике [по API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)  
*   Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.](../index.md#next-steps)  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
 
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Пространство имен Microsoft.Web.WebView2.Wpf | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Класс WebView2 | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Метод WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Разработчик Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftMain]: https://www.microsoft.com "Майкрософт"  

[MicrosoftVisualStudioMain]: https://visualstudio.microsoft.com "Microsoft Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2" 