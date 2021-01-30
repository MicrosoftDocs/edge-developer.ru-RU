---
description: Руководство по началу работы с WebView2 для приложений WinUI
title: Начало работы с WebView2 для приложений WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, веб-просмотр, приложения winui, winui, edge, CoreWebView2, элемент управления браузером, html edge, начало работы, начало работы, .NET
ms.openlocfilehash: 5188a735eaf635c3b3bc0eead6f4ee4f3a83f1c4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306154"
---
# Начало работы с WebView2 в WinUI 3 (предварительная версия)  

В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]  Ваше первое приложение WebView2 использует WinUI3.  Дополнительные сведения об отдельных API можно найти в [справочнике по API.][GithubMicrosoftUiXamlSpecsWebview2]  

## Предварительные условия  

Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.  

*   [WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.  Для получения дополнительных сведений о Windows 10 перейдите к [Обновлению Windows: faq][MicrosoftSupport12373].  
    
    > [!NOTE]
    > Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2019, версия 16.9 Preview.  Дополнительные сведения можно найти в [библиотеке пользовательского интерфейса Windows 3 Preview 3.][WindowsAppsWinui3ConfigureYourDevEnvironment]  
    
    *   При установке Visual Studio включаем следующие рабочие нагрузки.  
        *   .NET Desktop Development \(установщик также устанавливает .NET 5\)  
        *   Разработка универсальной платформы Windows  
    *   Для создания приложений C++ необходимо также включить следующие рабочие нагрузки.  
        *   Разработка классических компьютеров с помощью C++  
        *   Необязательный компонент средств универсальной платформы Windows (C++ \(v142\) для рабочей нагрузки универсальной платформы Windows.  Дополнительные сведения можно найти **в разделе** "Сведения об установке" в разделе "Разработка универсальной платформы **Windows"** на правой области.  
        
## Шаг 0. Visual Studio параметров  

1.  Убедитесь, что в системе включен источник пакета NuGet [для][NugetHome]nuget.org.  Для получения дополнительных сведений перейдите к [общим конфигурациям NuGet][NugetConsumePackagesConfiguringNugetBehavior] и [сообществу Windows набор средств.][WindowsCommunitytoolkit]  
1.  Скачайте и установите [пакет VSIX Для WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]  Установщик добавляет шаблоны проектов WinUI 3 и пакет NuGet, содержащий библиотеки WinUI 3, в Visual Studio 2019.  
    
    Инструкции по добавлению пакета в Visual Studio найдите и Visual Studio `VSIX` [расширения.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]
    
1.  Чтобы получить доступ ко всем функциям Visual Studio разработчика, включите [режим разработчика.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]  
    
## Шаг 1. Создание проекта  

Начните с базового проекта настольного компьютера, который содержит одно главное окно.  

1.  В Visual Studio выберите **"Создать новый проект".**  
1.  В выпадаемом проекте выберите **C#**, **Windows**и **WinUI** соответственно.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Создание нового проекта WinUI с помощью Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Создание нового проекта WinUI с помощью Visual Studio
    :::image-end:::  
    
1.  Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.  
1.  Введите имя проекта.
1.  Выберите нужные параметры.  
1.  Choose **Create**.  
1.  В **новом проекте универсальной платформы Windows**выберите следующие значения и выберите "ОК". ****  
    *   **Целевая версия:**  **Windows 10 версии 1903 (сборка 18362)** или более поздней  
    *   **Минимальная**версия:  **Windows 10 версии 1803 (сборка 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно "Проект новой универсальной платформы Windows" с выбранными значениями для целевой версии и минимальной версии." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Диалоговое окно "Проект новой универсальной платформы Windows" с выбранными значениями для целевой версии и минимальной версии.
    :::image-end:::  
    
1.  В обозревателе решений создаются два проекта.  
    *   **Имя проекта (рабочий стол).**  Проект "Рабочий стол" содержит код для вашего приложения.  Файл `App.xaml.cs` определяет `Application` класс, который представляет экземпляр вашего приложения.  Файл определяет класс, который представляет главное окно, `MainWindow.xaml.cs` `MainWindow` отображаемое экземпляром приложения.  Классы являются на основе типов в пространстве имен `Microsoft.UI.Xaml` WinUI.  
    *   **Имя проекта (пакет).**  Проект Package — это проект упаковки приложений для Windows, настроенный для сборки приложения в пакет MSIX для развертывания.  Проект содержит манифест пакета для вашего приложения и является проектом запуска для вашего решения по умолчанию.  Для получения дополнительных сведений перейдите к настройкам классических приложений для упаковки [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] в Visual Studio и справочнике по схеме манифеста пакета [для Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]  
1.  Чтобы отобразить код, откройте файл в обозревателе `MainWindow.xaml` решений.  Чтобы запустить проект и отобразить окно с кнопкой, выберите `F5` .  
    
## Шаг 2. Добавление в проект управления WebView2  

Добавьте в проект control WebView2.  

1.  Чтобы добавить `MainWindow.xaml` пространство имен XAML WebView2 в файл, вставьте следующую строку в `<Window/>` тег.  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Убедитесь, что код похож на следующий фрагмент `MainWindow.xaml` кода.  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  Чтобы добавить управление WebView2, замените теги на `<StackPanel>` следующий фрагмент кода.  Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  В `MainWindow.xaml.cs` файле закомментуем следующую строку.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что отображается ваш контроль [https://www.microsoft.com][|::ref1::|Main] WebView2.  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="WebView2 отображает microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       WebView2 отображает microsoft.com  
    :::image-end:::  
    
## Шаг 3. Добавление элементов управления навигацией  

Чтобы разрешить пользователям управлять веб-страницей, отображаемой в вашем веб-браузере WebView2, добавьте адресную планку в приложение.  

1.  В `MainWindow.xaml` файле скопируйте и в paste следующий фрагмент кода внутри `<Grid>` элемента, который содержит `WebView2` элемент.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    `<Grid>`Убедитесь, что элемент в `MainWindow.xaml` файле похож на следующий фрагмент кода.  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  Скопируйте в файл следующий фрагмент кода, чтобы перейти к url-адресу, введенного в адресной панели, с помощью управления `MainWindow.xaml.cs` `myButton_Click` WebView2.  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    Чтобы построить и запустить проект, выберите `F5` .  Введите новый URL-адрес в адресной панели и выберите **"Перейти".**  Например, введите `https://www.bing.com` .  
    
    > [!NOTE]
    > Убедитесь, что вы вводите полные URL-адреса в адресной панели.  `ArgumentException` исключения высылаются, если URL-адрес не начинается `http://` с или `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       bing.com  
    :::image-end:::  
    
## Шаг 4. События навигации  

Приложения, в которые находятся элементы управления WebView2, прослушивают следующие события, которые вызываются элементами управления WebView2 во время навигации на веб-странице.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.  

Дополнительные сведения можно найти в [меню "События навигации".][Webviews2ConceptsNavigationEvents]  

При ошибках возникают следующие события, которые могут переходить на веб-страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
В качестве примера использования событий зарегистрируйте обработок, который отменяет все запросы, не `NavigationStarting` относя такие как HTTPS.  В , измените конструктор для регистрации и добавьте функцию таким образом, чтобы она соответствует `MainWindow.xaml.cs` `EnsureHttps` `EnsureHttps` следующему фрагменту кода.  

```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что навигация заблокирована на сайтах HTTP и разрешена для сайтов HTTPS.  

## Шаг 5. Сценарии  

Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.  Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.  Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.  Введенный JavaScript работает с определенными сроками.  

*   Запустите его после создания глобального объекта.  
*   Запустите его перед запуском любого другого сценария, включенного в HTML-документ.  

В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.  Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее ExecuteScriptAsync.][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

Чтобы построить и запустить проект, выберите `F5` .  Убедитесь, что ваше приложение отображает оповещение при переходе на любые веб-сайты, не относящаться к HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="В веб-оке управления WebView2 отображается диалоговое окно оповещения" lightbox="./media/winui-gettingstarted-script.png":::
   В веб-оке управления WebView2 отображается диалоговое окно оповещения
:::image-end:::  

Поздравляем, вы создали свое первое приложение WebView2.  

## Дальнейшие действия  

Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.  

### См. также  

*   Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2IndexNextSteps]  
    
    > [!NOTE]
    > Объект WinRT CoreWebView2 может быть не доступен в выпуске API WebView2.  Чтобы понять, какие API доступны для элементов управления WebView2, перейдите к [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2] для списка доступных API.  
    
*   Подробные сведения об API WebView2 можно найти в [спецификации WebView2.][GithubMicrosoftUiXamlSpecsWebview2]  
    
## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: ../index.md "Введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия: введение в Microsoft Edge WebView2 (предварительная | Документы Майкрософт"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method (Microsoft.Web.WebView2.Wpf) | Документы Майкрософт"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Общие конфигурации NuGet | Документы Майкрософт"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Справочник по схеме манифеста пакета для Windows 10 | Документы Майкрософт"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Установка без использования диалогового окна "Управление расширениями" — управление расширениями для Visual Studio | Документы Майкрософт"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Настройка среды разработчика — Windows UI Library 3.0 Preview 1 (май 2020 г.) | Документы Майкрософт"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Документация по набор средств сообщества Windows | Документы Майкрософт"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Настройка классических приложений для упаковки MSIX в Visual Studio | Документы Майкрософт"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Включить устройство для разработки | Документы Майкрософт"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Спецификация WebView2 — microsoft/microsoft-ui-xaml-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "Майкрософт"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Обновление Windows: faq"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[NugetHome]: https://nuget.org "Домашняя | Галерея NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Загрузите dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Шаблоны проектов WinUI 3 | Visual Studio Marketplace"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2" 
