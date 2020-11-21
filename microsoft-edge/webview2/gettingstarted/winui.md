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
# <span data-ttu-id="92f01-104">Начало работы с WebView2 в WinUI 3 (ознакомительная версия)</span><span class="sxs-lookup"><span data-stu-id="92f01-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="92f01-105">В этой статье объясняется, как создать свое первое приложение WebView2 и ознакомиться с основными возможностями [знакомства с Microsoft Edge WebView2 (Предварительная версия)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="92f01-105">In this article, learn how to create your first WebView2 app and about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="92f01-106">Первое приложение WebView2 использует WinUI3.</span><span class="sxs-lookup"><span data-stu-id="92f01-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="92f01-107">Дополнительные сведения об отдельных API можно найти в [справочнике по API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="92f01-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="92f01-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="92f01-108">Prerequisites</span></span>  

<span data-ttu-id="92f01-109">Перед переходом к следующей статье убедитесь, что вы установили приведенный ниже список предварительных условий.</span><span class="sxs-lookup"><span data-stu-id="92f01-109">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

1.  <span data-ttu-id="92f01-110">Windows 10 версии 1803 \ (сборка 17134 \) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="92f01-110">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="92f01-111">Дополнительные сведения можно найти в [центре обновления Windows: вопросы и ответы][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="92f01-111">For more information, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
1.  <span data-ttu-id="92f01-112">[Microsoft EDGE (Chromium) Канарские Channel][MicrosoftedgeinsiderDownload] в Windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92f01-112">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
1.  <span data-ttu-id="92f01-113">Visual Studio 2019, версия 16,9 Preview.</span><span class="sxs-lookup"><span data-stu-id="92f01-113">Visual Studio 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="92f01-114">Дополнительные сведения можно найти в [библиотеке Windows UI 3 Preview][WindowsAppsWinui3ConfigureYourDevEnvironment].</span><span class="sxs-lookup"><span data-stu-id="92f01-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    <span data-ttu-id="92f01-115">При установке Visual Studio включите указанные ниже рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="92f01-115">Include the following workloads when you install Visual Studio.</span></span>  
    
    *   <span data-ttu-id="92f01-116">Разработка приложений для настольных систем .NET (установщик также устанавливает .NET 5 \)</span><span class="sxs-lookup"><span data-stu-id="92f01-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
    *   <span data-ttu-id="92f01-117">Разработка универсальной платформы Windows</span><span class="sxs-lookup"><span data-stu-id="92f01-117">Universal Windows Platform development</span></span>  
        
    <span data-ttu-id="92f01-118">Для сборки приложений C++ необходимо также включить следующие рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="92f01-118">To build C++ apps, you must also include the following workloads.</span></span>  
    
    *   <span data-ttu-id="92f01-119">Разработка для настольных систем с использованием C++</span><span class="sxs-lookup"><span data-stu-id="92f01-119">Desktop development with C++</span></span>  
    *   <span data-ttu-id="92f01-120">Необязательный компонент универсальной платформы Windows для C++ (v142) для рабочей нагрузки универсальной платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="92f01-120">The C++ (v142) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="92f01-121">Для получения дополнительных сведений перейдите к разделу сведения об установке в разделе универсальная разработка платформы Windows в области справа.</span><span class="sxs-lookup"><span data-stu-id="92f01-121">For more information,  navigate to Installation Details under the Universal Windows Platform development section, on the right pane.</span></span>  
        
1.  <span data-ttu-id="92f01-122">Убедитесь, что для вашей системы установлен источник пакета NuGet для [NuGet.org][NugetHome].  Дополнительные сведения можно найти в разделе [Общие конфигурации NuGet][NugetConsumePackagesConfiguringNugetBehavior] и [набор средств сообщества Windows][WindowsCommunitytoolkit].</span><span class="sxs-lookup"><span data-stu-id="92f01-122">Make sure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="92f01-123">Скачайте и установите [пакет VSIX для WinUI 3 Preview 3][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span><span class="sxs-lookup"><span data-stu-id="92f01-123">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="92f01-124">Установщик добавит оба шаблона проекта WinUI 3 и пакет NuGet, содержащий библиотеки WinUI 3, в Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="92f01-124">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="92f01-125">Инструкции по добавлению пакета VSIX в Visual Studio можно найти в разделе [Поиск и использование расширений Visual Studio][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span><span class="sxs-lookup"><span data-stu-id="92f01-125">For instructions on how to add the VSIX package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="92f01-126">Включите [режим разработчика][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , чтобы убедиться, что у вас есть доступ ко всем функциональным возможностям Visual Studio, определенным разработчиком.</span><span class="sxs-lookup"><span data-stu-id="92f01-126">Enable [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all developer-specific Visual Studio features.</span></span>  
    
## <span data-ttu-id="92f01-127">Шаг 1: Создание проекта</span><span class="sxs-lookup"><span data-stu-id="92f01-127">Step 1 - Create Project</span></span>  

<span data-ttu-id="92f01-128">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="92f01-128">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="92f01-129">В Visual Studio выберите **создать новый проект**.</span><span class="sxs-lookup"><span data-stu-id="92f01-129">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="92f01-130">В раскрывающемся списке Проект выберите **C#**, **Windows**и **WinUI** соответственно.</span><span class="sxs-lookup"><span data-stu-id="92f01-130">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Создание нового проекта WinUI с помощью Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="92f01-132">Создание нового проекта WinUI с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92f01-132">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="92f01-133">Выберите **пустое приложение, упакованное (WinUI на рабочем столе)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="92f01-133">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="92f01-134">Введите имя проекта, выберите нужные параметры и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="92f01-134">Enter a project name, choose other options as needed, and then choose **Create**.</span></span>  
1.  <span data-ttu-id="92f01-135">В **новом проекте универсальной платформы Windows**выберите указанные ниже значения, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="92f01-135">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="92f01-136">**Целевая версия**:  **Windows 10, версия 1903 (сборка 18362)** или более поздняя</span><span class="sxs-lookup"><span data-stu-id="92f01-136">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="92f01-137">**Минимальная версия**:  **Windows 10, версия 1803 (сборка 17134)**</span><span class="sxs-lookup"><span data-stu-id="92f01-137">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно «Новый проект универсальной платформы Windows» с выбранными значениями для целевой версии и минимальной версии." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="92f01-139">Диалоговое окно «Новый проект универсальной платформы Windows» с выбранными значениями для целевой версии и минимальной версии.</span><span class="sxs-lookup"><span data-stu-id="92f01-139">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="92f01-140">В обозревателе решений создаются два проекта.</span><span class="sxs-lookup"><span data-stu-id="92f01-140">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="92f01-141">**Название проекта (классическое приложение)**.</span><span class="sxs-lookup"><span data-stu-id="92f01-141">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="92f01-142">Этот проект включает код для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="92f01-142">This project contains the code for your app.</span></span>  <span data-ttu-id="92f01-143">**App.XAML.CS** определяет `Application` класс, представляющий экземпляр приложения.</span><span class="sxs-lookup"><span data-stu-id="92f01-143">**App.xaml.cs** defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="92f01-144">**MainWindow.XAML.CS** определяет `MainWindow` класс, представляющий главное окно, которое отображается в экземпляре приложения.</span><span class="sxs-lookup"><span data-stu-id="92f01-144">**MainWindow.xaml.cs** defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="92f01-145">Эти классы являются производными от типов в `Microsoft.UI.Xaml` пространстве имен WinUI.</span><span class="sxs-lookup"><span data-stu-id="92f01-145">These classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="92f01-146">**Имя проекта (пакет)**.</span><span class="sxs-lookup"><span data-stu-id="92f01-146">**Your project name (Package)**.</span></span>  <span data-ttu-id="92f01-147">Этот проект — это проект упаковки приложений для Windows, который настроен для сборки приложения в пакет MSIX для развертывания.</span><span class="sxs-lookup"><span data-stu-id="92f01-147">This project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="92f01-148">Проект содержит манифест пакета для вашего приложения, и по умолчанию он является запускаемым проектом для вашего решения.</span><span class="sxs-lookup"><span data-stu-id="92f01-148">The project contains the package manifest for your app, and it is the startup project for your solution by default.</span></span>  <span data-ttu-id="92f01-149">Дополнительные сведения можно найти в [разделе Настройка классического приложения для MSIX упаковки в Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] и [Справочник по схеме манифеста пакета для Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="92f01-149">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="92f01-150">В обозревателе решений откройте файл, чтобы отобразить код `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="92f01-150">In the Solution Explorer, to display the code, open `MainWindow.xaml` file.</span></span>  <span data-ttu-id="92f01-151">Выберите `F5` , чтобы запустить проект и отобразить окно с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="92f01-151">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="92f01-152">Шаг 2: Добавление элемента управления WebView2 в проект</span><span class="sxs-lookup"><span data-stu-id="92f01-152">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="92f01-153">Затем добавьте элемент управления WebView2 в проект.</span><span class="sxs-lookup"><span data-stu-id="92f01-153">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="92f01-154">Open (открыть) `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="92f01-154">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="92f01-155">Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .</span><span class="sxs-lookup"><span data-stu-id="92f01-155">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="92f01-156">Убедитесь, что ваш код `MainWindow.xaml` похож на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="92f01-156">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="92f01-157">Чтобы добавить элемент управления WebView2, замените `<StackPanel>` теги на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="92f01-157">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="92f01-158">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="92f01-158">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="92f01-159">Откройте `MainWindow.xaml.cs` следующую строку и закомментируйте ее.</span><span class="sxs-lookup"><span data-stu-id="92f01-159">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="92f01-160">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="92f01-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="92f01-161">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="92f01-161">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Элемент управления WebView2, на котором отображается сайт microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="92f01-163">Элемент управления WebView2, на котором отображается сайт microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="92f01-163">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="92f01-164">Шаг 3: Добавление элементов управления навигацией</span><span class="sxs-lookup"><span data-stu-id="92f01-164">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="92f01-165">Разрешите пользователям управлять веб-страницей, которая отображается в элементе управления WebView2, добавив адресную строку в приложение.</span><span class="sxs-lookup"><span data-stu-id="92f01-165">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span>  

1.  <span data-ttu-id="92f01-166">`MainWindow.xaml`Скопируйте и вставьте следующий фрагмент кода в `Grid` элемент, содержащий `WebView2` элемент.</span><span class="sxs-lookup"><span data-stu-id="92f01-166">In `MainWindow.xaml`, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="92f01-167">Убедитесь, что `Grid` элемент `MainWindow.xaml` похож на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="92f01-167">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="92f01-168">`MainWindow.xaml.cs`Скопируйте приведенный ниже фрагмент кода `myButton_Click` , который будет перемещаться по элементу управления WebView2 на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="92f01-168">In `MainWindow.xaml.cs`, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="92f01-169">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="92f01-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="92f01-170">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="92f01-170">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="92f01-171">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="92f01-171">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="92f01-172">Убедитесь в том, что в адресной строке используются полные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="92f01-172">Ensure you use complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="92f01-173">Если URL-адрес не начинается с or, возникают `http://` исключения `https://` .</span><span class="sxs-lookup"><span data-stu-id="92f01-173">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="92f01-175">Bing.com</span><span class="sxs-lookup"><span data-stu-id="92f01-175">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="92f01-176">Шаг 4 — события навигации</span><span class="sxs-lookup"><span data-stu-id="92f01-176">Step 4 - Navigation events</span></span>  

<span data-ttu-id="92f01-177">Приложения, на которых размещаются элементы управления WebView2, прослушивают следующие события, возникающие в элементах управления WebView2 на этапе навигации веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="92f01-177">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="92f01-178">Переадресация HTTP вызывает несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="92f01-178">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="92f01-179">Дополнительные сведения можно найти в разделе [события навигации][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="92f01-179">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="92f01-180">При возникновении ошибок возникают следующие события, которые могут перейти на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="92f01-180">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="92f01-181">В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` этого отменяет все запросы, не ИСПОЛЬЗУЮЩИЕ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92f01-181">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any request that does not use HTTPS.</span></span>  <span data-ttu-id="92f01-182">`MainWindow.xaml.cs`Измените конструктор, чтобы `EnsureHttps` он регистрировал, и добавьте `EnsureHttps` функцию так, чтобы она соответствовала следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="92f01-182">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="92f01-183">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="92f01-183">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="92f01-184">Убедитесь, что Навигация заблокирована на сайтах HTTP и разрешена для HTTPS-сайтов.</span><span class="sxs-lookup"><span data-stu-id="92f01-184">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="92f01-185">Шаг 5: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="92f01-185">Step 5 - Scripting</span></span>  

<span data-ttu-id="92f01-186">Ведущее приложение может внедрять код JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="92f01-186">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="92f01-187">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.</span><span class="sxs-lookup"><span data-stu-id="92f01-187">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="92f01-188">Вставленный JavaScript выполняется с определенным временем.</span><span class="sxs-lookup"><span data-stu-id="92f01-188">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="92f01-189">Запустите ее после создания глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="92f01-189">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="92f01-190">Запустите ее перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="92f01-190">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="92f01-191">В качестве примера добавьте сценарии, отправляющие предупреждение, когда пользователь переходит на сайты, не поддерживающие HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92f01-191">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="92f01-192">Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, использующее [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="92f01-192">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="92f01-193">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="92f01-193">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="92f01-194">Убедитесь, что ваше приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92f01-194">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Элемент управления WebView2, в котором отображается диалоговое окно оповещения" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="92f01-196">Элемент управления WebView2, в котором отображается диалоговое окно оповещения</span><span class="sxs-lookup"><span data-stu-id="92f01-196">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="92f01-197">Поздравляем! вы создали первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="92f01-197">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="92f01-198">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="92f01-198">Next Steps</span></span>  

<span data-ttu-id="92f01-199">Наша группа в настоящее время использует дополнительные API WebView2.</span><span class="sxs-lookup"><span data-stu-id="92f01-199">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="92f01-200">Чтобы получить дополнительные сведения о текущем состоянии API WebView2, перейдите к [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="92f01-200">For more information on the current state of WebView2 APIs, navigate to the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="92f01-201">Объект CoreWebView2 WinRT может быть недоступен на момент отгрузки API WebView2.</span><span class="sxs-lookup"><span data-stu-id="92f01-201">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span>  <span data-ttu-id="92f01-202">Чтобы узнать, какие API доступны для элементов управления WebView2, перейдите в [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] , чтобы просмотреть список доступных API.</span><span class="sxs-lookup"><span data-stu-id="92f01-202">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  

<span data-ttu-id="92f01-203">Для получения дополнительных сведений о возможностях WebView2 перейдите к [WebView2 концепциям и How-To руководствам][Webview2IndexNextSteps] и [репозиторию примеров WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="92f01-203">For more information about WebView2 capabilities, navigate to [WebView2 Concepts and How-To guides][Webview2IndexNextSteps] and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="92f01-204">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="92f01-204">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
