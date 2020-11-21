---
description: Руководство по началу работы с WebView2 для WinUI приложений
title: Приступая к работе с WebView2 для WinUI приложений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, winui, winui, EDGE, CoreWebView2, Browser Control, EDGE HTML, Приступая к работе, Приступая к работе, .NET
ms.openlocfilehash: a1ccffe332f71ee9d53ff267e8cca6bdbda81703
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182723"
---
# Начало работы с WebView2 в WinUI 3 (ознакомительная версия)  

В этой статье объясняется, как создать свое первое приложение WebView2 и ознакомиться с основными возможностями [знакомства с Microsoft Edge WebView2 (Предварительная версия)][Webview2Index].  Первое приложение WebView2 использует WinUI3.  Дополнительные сведения об отдельных API можно найти в [справочнике по API][GithubMicrosoftUiXamlSpecsWebview2].  

## Предварительные условия  

Перед переходом к следующей статье убедитесь, что вы установили приведенный ниже список предварительных условий.  

1.  Windows 10 версии 1803 \ (сборка 17134 \) или более поздней версии.  Дополнительные сведения можно найти в [центре обновления Windows: вопросы и ответы][MicrosoftSupport12373].  
1.  [Microsoft EDGE (Chromium) Канарские Channel][MicrosoftedgeinsiderDownload] в Windows 10, Windows 8,1 или Windows 7.  
1.  Visual Studio 2019, версия 16,9 Preview.  Дополнительные сведения можно найти в [библиотеке Windows UI 3 Preview][WindowsAppsWinui3ConfigureYourDevEnvironment].  
    
    При установке Visual Studio включите указанные ниже рабочие нагрузки.  
    
    *   Разработка приложений для настольных систем .NET (установщик также устанавливает .NET 5 \)  
    *   Разработка универсальной платформы Windows  
        
    Для сборки приложений C++ необходимо также включить следующие рабочие нагрузки.  
    
    *   Разработка для настольных систем с использованием C++  
    *   Необязательный компонент универсальной платформы Windows для C++ (v142) для рабочей нагрузки универсальной платформы Windows.  Для получения дополнительных сведений перейдите к разделу сведения об установке в разделе универсальная разработка платформы Windows в области справа.  
        
1.  Убедитесь, что для вашей системы установлен источник пакета NuGet для [NuGet.org][NugetHome].  Дополнительные сведения можно найти в разделе [Общие конфигурации NuGet][NugetConsumePackagesConfiguringNugetBehavior] и [набор средств сообщества Windows][WindowsCommunitytoolkit].  
1.  Скачайте и установите [пакет VSIX для WinUI 3 Preview 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].  Установщик добавит оба шаблона проекта WinUI 3 и пакет NuGet, содержащий библиотеки WinUI 3, в Visual Studio 2019.  
    
    Инструкции по добавлению пакета VSIX в Visual Studio можно найти в разделе [Поиск и использование расширений Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].
    
1.  Включите [режим разработчика][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , чтобы убедиться, что у вас есть доступ ко всем функциональным возможностям Visual Studio, определенным разработчиком.  
    
## Шаг 1: Создание проекта  

Начните с базового классического проекта, содержащего одно главное окно.  

1.  В Visual Studio выберите **создать новый проект**.  
1.  В раскрывающемся списке Проект выберите **C#**, **Windows**и **WinUI** соответственно.  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Создание нового проекта WinUI с помощью Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        Создание нового проекта WinUI с помощью Visual Studio
    :::image-end:::  
    
1.  Выберите **пустое приложение, упакованное (WinUI на рабочем столе)**, а затем нажмите кнопку **Далее**.  
1.  Введите имя проекта, выберите нужные параметры и нажмите кнопку **создать**.  
1.  В **новом проекте универсальной платформы Windows**выберите указанные ниже значения, а затем нажмите кнопку **ОК**.  
    *   **Целевая версия**:  **Windows 10, версия 1903 (сборка 18362)** или более поздняя  
    *   **Минимальная версия**:  **Windows 10, версия 1803 (сборка 17134)**  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно «Новый проект универсальной платформы Windows» с выбранными значениями для целевой версии и минимальной версии." lightbox="./media/winui-gettingstarted-projecttype.png":::
       Диалоговое окно «Новый проект универсальной платформы Windows» с выбранными значениями для целевой версии и минимальной версии.
    :::image-end:::  
    
1.  В обозревателе решений создаются два проекта.  
    *   **Название проекта (классическое приложение)**.  Этот проект включает код для вашего приложения.  **App.XAML.CS** определяет `Application` класс, представляющий экземпляр приложения.  **MainWindow.XAML.CS** определяет `MainWindow` класс, представляющий главное окно, которое отображается в экземпляре приложения.  Эти классы являются производными от типов в `Microsoft.UI.Xaml` пространстве имен WinUI.  
    
    *   **Имя проекта (пакет)**.  Этот проект — это проект упаковки приложений для Windows, который настроен для сборки приложения в пакет MSIX для развертывания.  Проект содержит манифест пакета для вашего приложения, и по умолчанию он является запускаемым проектом для вашего решения.  Дополнительные сведения можно найти в [разделе Настройка классического приложения для MSIX упаковки в Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] и [Справочник по схеме манифеста пакета для Windows 10][UwpSchemasAppxpackageUapmanifestRoot].
    
1.  В обозревателе решений откройте файл, чтобы отобразить код `MainWindow.xaml` .  Выберите `F5` , чтобы запустить проект и отобразить окно с кнопкой.  
    
## Шаг 2: Добавление элемента управления WebView2 в проект  

Затем добавьте элемент управления WebView2 в проект.  

1.  Open (открыть) `MainWindow.xaml` .  Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    Убедитесь, что ваш код `MainWindow.xaml` похож на следующий фрагмент кода.  
    
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
    
1.  Чтобы добавить элемент управления WebView2, замените `<StackPanel>` теги на следующий фрагмент кода.  `Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.  
    
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
    
1.  Откройте `MainWindow.xaml.cs` следующую строку и закомментируйте ее.
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com][|::ref1::|Main] .  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Элемент управления WebView2, на котором отображается сайт microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       Элемент управления WebView2, на котором отображается сайт microsoft.com.  
    :::image-end:::  
    
## Шаг 3: Добавление элементов управления навигацией  

Разрешите пользователям управлять веб-страницей, которая отображается в элементе управления WebView2, добавив адресную строку в приложение.  

1.  `MainWindow.xaml`Скопируйте и вставьте следующий фрагмент кода в `Grid` элемент, содержащий `WebView2` элемент.  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    Убедитесь, что `Grid` элемент `MainWindow.xaml` похож на следующий фрагмент кода.  
    
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
    
1.  `MainWindow.xaml.cs`Скопируйте приведенный ниже фрагмент кода `myButton_Click` , который будет перемещаться по элементу управления WebView2 на URL-адрес, введенный в адресной строке.  
    
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
    
    Выберите `F5` , чтобы выполнить сборку и запустить проект.  Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.  Например, введите `https://www.bing.com` .  
    
    > [!NOTE]
    > Убедитесь в том, что в адресной строке используются полные URL-адреса.  `ArgumentException` Если URL-адрес не начинается с or, возникают `http://` исключения `https://` .  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       Bing.com  
    :::image-end:::  
    
## Шаг 4 — события навигации  

Приложения, на которых размещаются элементы управления WebView2, прослушивают следующие события, возникающие в элементах управления WebView2 на этапе навигации веб-страницы.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> Переадресация HTTP вызывает несколько `NavigationStarting` событий.  

Дополнительные сведения можно найти в разделе [события навигации][Webviews2ConceptsNavigationEvents].  

При возникновении ошибок возникают следующие события, которые могут перейти на страницу ошибки.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` этого отменяет все запросы, не ИСПОЛЬЗУЮЩИЕ HTTPS.  `MainWindow.xaml.cs`Измените конструктор, чтобы `EnsureHttps` он регистрировал, и добавьте `EnsureHttps` функцию так, чтобы она соответствовала следующему фрагменту кода.  

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

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что Навигация заблокирована на сайтах HTTP и разрешена для HTTPS-сайтов.  

## Шаг 5: создание сценариев  

Ведущее приложение может внедрять код JavaScript в элементы управления WebView2 во время выполнения.  Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.  Вставленный JavaScript выполняется с определенным временем.  

*   Запустите ее после создания глобального объекта.  
*   Запустите ее перед выполнением любого другого сценария, включенного в документ HTML.  

В качестве примера добавьте сценарии, отправляющие предупреждение, когда пользователь переходит на сайты, не поддерживающие HTTPS.  Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, использующее [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].  

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

Выберите `F5` , чтобы выполнить сборку и запустить проект.  Убедитесь, что ваше приложение отображает оповещение при переходе на сайт, который не использует HTTPS.  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Элемент управления WebView2, в котором отображается диалоговое окно оповещения" lightbox="./media/winui-gettingstarted-script.png":::
   Элемент управления WebView2, в котором отображается диалоговое окно оповещения
:::image-end:::  

Поздравляем! вы создали первое приложение WebView2.  

## Дальнейшие действия  

Наша группа в настоящее время использует дополнительные API WebView2.  Чтобы получить дополнительные сведения о текущем состоянии API WebView2, перейдите к [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2].  

> [!NOTE]
> Объект CoreWebView2 WinRT может быть недоступен на момент отгрузки API WebView2.  Чтобы узнать, какие API доступны для элементов управления WebView2, перейдите в [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] , чтобы просмотреть список доступных API.  

Для получения дополнительных сведений о возможностях WebView2 перейдите к [WebView2 концепциям и How-To руководствам][Webview2IndexNextSteps] и [репозиторию примеров WebView2][GithubMicrosoftedgeWebview2samplesMain].  

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2Index]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Microsoft"  
[Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]: /dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync "WebView2.ExecuteScriptAsync (String) method (Microsoft. Web. WebView2. WPF) | Документы Microsoft"  

[NugetConsumePackagesConfiguringNugetBehavior]: /nuget/consume-packages/configuring-nuget-behavior "Общие конфигурации NuGet | Документы Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Справочник по схеме манифеста пакета для Windows 10 | Документы Microsoft"  

[VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]: /visualstudio/ide/finding-and-using-visual-studio-extensions#install-without-using-the-manage-extensions-dialog-box "Установка без использования диалогового окна "Управление расширениями" — Управление расширениями для Visual Studio | Документы Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Настройка среды разработки — библиотеки пользовательского интерфейса Windows 3,0 Preview (Май 2020) | Документы Microsoft"  
[WindowsCommunitytoolkit]: /windows/communitytoolkit "Документация по набору средств для сообщества Windows | Документы Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Настройка классического приложения для MSIX упаковки в Visual Studio | Документы Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Активация устройства для разработки | Документы Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 Spec-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "SMTP"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Обновление Windows: вопросы и ответы"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[NugetHome]: https://nuget.org "Главная | Коллекция NuGet"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Скачать dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe " dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Шаблоны проектов WinUI 3 | Visual Studio Marketplace"  
