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
# <span data-ttu-id="962ca-104">Начало работы с WebView2 в WinUI 3 (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="962ca-104">Getting started with WebView2 in WinUI 3 (Preview)</span></span>  

<span data-ttu-id="962ca-105">В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="962ca-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="962ca-106">Ваше первое приложение WebView2 использует WinUI3.</span><span class="sxs-lookup"><span data-stu-id="962ca-106">Your first WebView2 app uses WinUI3.</span></span>  <span data-ttu-id="962ca-107">Дополнительные сведения об отдельных API можно найти в [справочнике по API.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="962ca-107">For more information on individual APIs, navigate to [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="962ca-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="962ca-108">Prerequisites</span></span>  

<span data-ttu-id="962ca-109">Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.</span><span class="sxs-lookup"><span data-stu-id="962ca-109">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="962ca-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span><span class="sxs-lookup"><span data-stu-id="962ca-110">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="962ca-111">Для получения дополнительных сведений о Windows 10 перейдите к [Обновлению Windows: faq][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="962ca-111">For more information about Windows 10, navigate to [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="962ca-112">Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="962ca-112">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="962ca-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, версия 16.9 Preview.</span><span class="sxs-lookup"><span data-stu-id="962ca-113">[Visual Studio][MicrosoftVisualstudioMain] 2019, version 16.9 Preview.</span></span>  <span data-ttu-id="962ca-114">Дополнительные сведения можно найти в [библиотеке пользовательского интерфейса Windows 3 Preview 3.][WindowsAppsWinui3ConfigureYourDevEnvironment]</span><span class="sxs-lookup"><span data-stu-id="962ca-114">For more information, navigate to [Windows UI Library 3 Preview 3][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
    
    *   <span data-ttu-id="962ca-115">При установке Visual Studio включаем следующие рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="962ca-115">Include the following workloads when you install Visual Studio.</span></span>  
        *   <span data-ttu-id="962ca-116">.NET Desktop Development \(установщик также устанавливает .NET 5\)</span><span class="sxs-lookup"><span data-stu-id="962ca-116">.NET Desktop Development \(the installer also installs .NET 5\)</span></span>  
        *   <span data-ttu-id="962ca-117">Разработка универсальной платформы Windows</span><span class="sxs-lookup"><span data-stu-id="962ca-117">Universal Windows Platform development</span></span>  
    *   <span data-ttu-id="962ca-118">Для создания приложений C++ необходимо также включить следующие рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="962ca-118">To build C++ apps, you must also include the following workloads.</span></span>  
        *   <span data-ttu-id="962ca-119">Разработка классических компьютеров с помощью C++</span><span class="sxs-lookup"><span data-stu-id="962ca-119">Desktop development with C++</span></span>  
        *   <span data-ttu-id="962ca-120">Необязательный компонент средств универсальной платформы Windows (C++ \(v142\) для рабочей нагрузки универсальной платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="962ca-120">The C++ \(v142\) Universal Windows Platform tools optional component for the Universal Windows Platform workload.</span></span>  <span data-ttu-id="962ca-121">Дополнительные сведения можно найти **в разделе** "Сведения об установке" в разделе "Разработка универсальной платформы **Windows"** на правой области.</span><span class="sxs-lookup"><span data-stu-id="962ca-121">For more information,  navigate to **Installation Details** under the **Universal Windows Platform development** section, on the right pane.</span></span>  
        
## <span data-ttu-id="962ca-122">Шаг 0. Visual Studio параметров</span><span class="sxs-lookup"><span data-stu-id="962ca-122">Step 0 - Visual Studio settings</span></span>  

1.  <span data-ttu-id="962ca-123">Убедитесь, что в системе включен источник пакета NuGet [для][NugetHome]nuget.org.  Для получения дополнительных сведений перейдите к [общим конфигурациям NuGet][NugetConsumePackagesConfiguringNugetBehavior] и [сообществу Windows набор средств.][WindowsCommunitytoolkit]</span><span class="sxs-lookup"><span data-stu-id="962ca-123">Ensure your system has a NuGet package source enabled for [nuget.org][NugetHome].  For more information, navigate to [Common NuGet configurations][NugetConsumePackagesConfiguringNugetBehavior] and [Windows Community Toolkit][WindowsCommunitytoolkit].</span></span>  
1.  <span data-ttu-id="962ca-124">Скачайте и установите [пакет VSIX Для WinUI 3 Preview 3.][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates]</span><span class="sxs-lookup"><span data-stu-id="962ca-124">Download and install the [WinUI 3 Preview 3 VSIX package][VisualstudioMarketplaceMicrosoftWinuiWinuiprojecttemplates].</span></span>  <span data-ttu-id="962ca-125">Установщик добавляет шаблоны проектов WinUI 3 и пакет NuGet, содержащий библиотеки WinUI 3, в Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="962ca-125">The installer adds both the WinUI 3 project templates and the NuGet package containing the WinUI 3 libraries to Visual Studio 2019.</span></span>  
    
    <span data-ttu-id="962ca-126">Инструкции по добавлению пакета в Visual Studio найдите и Visual Studio `VSIX` [расширения.][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox]</span><span class="sxs-lookup"><span data-stu-id="962ca-126">For instructions on how to add the `VSIX` package to Visual Studio, navigate to [Finding and Using Visual Studio Extensions][VisualstudioIdeFindingUsingVisualStudioExtensionsInstallWithoutUsing-ManageExtensionsDialogBox].</span></span>
    
1.  <span data-ttu-id="962ca-127">Чтобы получить доступ ко всем функциям Visual Studio разработчика, включите [режим разработчика.][WindowsUwpGetStartedEnableYourDeviceForDevelopment]</span><span class="sxs-lookup"><span data-stu-id="962ca-127">To access all developer-specific Visual Studio features, turn on [Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment].</span></span>  
    
## <span data-ttu-id="962ca-128">Шаг 1. Создание проекта</span><span class="sxs-lookup"><span data-stu-id="962ca-128">Step 1 - Create Project</span></span>  

<span data-ttu-id="962ca-129">Начните с базового проекта настольного компьютера, который содержит одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="962ca-129">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="962ca-130">В Visual Studio выберите **"Создать новый проект".**</span><span class="sxs-lookup"><span data-stu-id="962ca-130">In Visual Studio, choose **Create a new project**.</span></span>  
1.  <span data-ttu-id="962ca-131">В выпадаемом проекте выберите **C#**, **Windows**и **WinUI** соответственно.</span><span class="sxs-lookup"><span data-stu-id="962ca-131">In the project drop-down, choose **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Создание нового проекта WinUI с помощью Visual Studio" lightbox="./media/winui-gettingstarted-selections.png":::
        <span data-ttu-id="962ca-133">Создание нового проекта WinUI с помощью Visual Studio</span><span class="sxs-lookup"><span data-stu-id="962ca-133">Create a new WinUI project using Visual Studio</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="962ca-134">Choose **Blank App, Packaged (WinUI in Desktop)**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="962ca-134">Choose **Blank App, Packaged (WinUI in Desktop)** > **Next**.</span></span>  
1.  <span data-ttu-id="962ca-135">Введите имя проекта.</span><span class="sxs-lookup"><span data-stu-id="962ca-135">Enter a project name.</span></span>
1.  <span data-ttu-id="962ca-136">Выберите нужные параметры.</span><span class="sxs-lookup"><span data-stu-id="962ca-136">Choose options as needed.</span></span>  
1.  <span data-ttu-id="962ca-137">Choose **Create**.</span><span class="sxs-lookup"><span data-stu-id="962ca-137">Choose **Create**.</span></span>  
1.  <span data-ttu-id="962ca-138">В **новом проекте универсальной платформы Windows**выберите следующие значения и выберите "ОК". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="962ca-138">In **New Universal Windows Platform Project**, choose the following values, and then choose **OK**.</span></span>  
    *   <span data-ttu-id="962ca-139">**Целевая версия:**  **Windows 10 версии 1903 (сборка 18362)** или более поздней</span><span class="sxs-lookup"><span data-stu-id="962ca-139">**Target version**:  **Windows 10, version 1903 (build 18362)** or later</span></span>  
    *   <span data-ttu-id="962ca-140">**Минимальная**версия:  **Windows 10 версии 1803 (сборка 17134)**</span><span class="sxs-lookup"><span data-stu-id="962ca-140">**Minimum version**:  **Windows 10, version 1803 (build 17134)**</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно "Проект новой универсальной платформы Windows" с выбранными значениями для целевой версии и минимальной версии." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="962ca-142">Диалоговое окно "Проект новой универсальной платформы Windows" с выбранными значениями для целевой версии и минимальной версии.</span><span class="sxs-lookup"><span data-stu-id="962ca-142">The New Universal Windows Platform Project dialog with chosen values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="962ca-143">В обозревателе решений создаются два проекта.</span><span class="sxs-lookup"><span data-stu-id="962ca-143">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="962ca-144">**Имя проекта (рабочий стол).**</span><span class="sxs-lookup"><span data-stu-id="962ca-144">**Your project name (Desktop)**.</span></span>  <span data-ttu-id="962ca-145">Проект "Рабочий стол" содержит код для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="962ca-145">The Desktop project contains the code for your app.</span></span>  <span data-ttu-id="962ca-146">Файл `App.xaml.cs` определяет `Application` класс, который представляет экземпляр вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="962ca-146">The `App.xaml.cs` file defines an `Application` class that represents your app instance.</span></span>  <span data-ttu-id="962ca-147">Файл определяет класс, который представляет главное окно, `MainWindow.xaml.cs` `MainWindow` отображаемое экземпляром приложения.</span><span class="sxs-lookup"><span data-stu-id="962ca-147">The `MainWindow.xaml.cs` file defines a `MainWindow` class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="962ca-148">Классы являются на основе типов в пространстве имен `Microsoft.UI.Xaml` WinUI.</span><span class="sxs-lookup"><span data-stu-id="962ca-148">The classes derive from types in the `Microsoft.UI.Xaml` namespace of WinUI.</span></span>  
    *   <span data-ttu-id="962ca-149">**Имя проекта (пакет).**</span><span class="sxs-lookup"><span data-stu-id="962ca-149">**Your project name (Package)**.</span></span>  <span data-ttu-id="962ca-150">Проект Package — это проект упаковки приложений для Windows, настроенный для сборки приложения в пакет MSIX для развертывания.</span><span class="sxs-lookup"><span data-stu-id="962ca-150">The Package project is a Windows Application Packaging Project that is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="962ca-151">Проект содержит манифест пакета для вашего приложения и является проектом запуска для вашего решения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="962ca-151">The project contains the package manifest for your app, and is the startup project for your solution by default.</span></span>  <span data-ttu-id="962ca-152">Для получения дополнительных сведений перейдите к настройкам классических приложений для упаковки [MSIX][WindowsMsixDesktopToUwpPackagingDotNet] в Visual Studio и справочнике по схеме манифеста пакета [для Windows 10.][UwpSchemasAppxpackageUapmanifestRoot]</span><span class="sxs-lookup"><span data-stu-id="962ca-152">For more information, navigate to [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>  
1.  <span data-ttu-id="962ca-153">Чтобы отобразить код, откройте файл в обозревателе `MainWindow.xaml` решений.</span><span class="sxs-lookup"><span data-stu-id="962ca-153">In the Solution Explorer, to display the code, open the `MainWindow.xaml` file.</span></span>  <span data-ttu-id="962ca-154">Чтобы запустить проект и отобразить окно с кнопкой, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="962ca-154">To run your project and display a window with a button, select `F5`.</span></span>  
    
## <span data-ttu-id="962ca-155">Шаг 2. Добавление в проект управления WebView2</span><span class="sxs-lookup"><span data-stu-id="962ca-155">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="962ca-156">Добавьте в проект control WebView2.</span><span class="sxs-lookup"><span data-stu-id="962ca-156">Add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="962ca-157">Чтобы добавить `MainWindow.xaml` пространство имен XAML WebView2 в файл, вставьте следующую строку в `<Window/>` тег.</span><span class="sxs-lookup"><span data-stu-id="962ca-157">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="962ca-158">Убедитесь, что код похож на следующий фрагмент `MainWindow.xaml` кода.</span><span class="sxs-lookup"><span data-stu-id="962ca-158">Ensure your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="962ca-159">Чтобы добавить управление WebView2, замените теги на `<StackPanel>` следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="962ca-159">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="962ca-160">Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.</span><span class="sxs-lookup"><span data-stu-id="962ca-160">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
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
    
1.  <span data-ttu-id="962ca-161">В `MainWindow.xaml.cs` файле закомментуем следующую строку.</span><span class="sxs-lookup"><span data-stu-id="962ca-161">In the `MainWindow.xaml.cs` file, comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="962ca-162">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="962ca-162">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="962ca-163">Убедитесь, что отображается ваш контроль [https://www.microsoft.com][|::ref1::|Main] WebView2.</span><span class="sxs-lookup"><span data-stu-id="962ca-163">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="WebView2 отображает microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="962ca-165">WebView2 отображает microsoft.com</span><span class="sxs-lookup"><span data-stu-id="962ca-165">WebView2 control displays microsoft.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="962ca-166">Шаг 3. Добавление элементов управления навигацией</span><span class="sxs-lookup"><span data-stu-id="962ca-166">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="962ca-167">Чтобы разрешить пользователям управлять веб-страницей, отображаемой в вашем веб-браузере WebView2, добавьте адресную планку в приложение.</span><span class="sxs-lookup"><span data-stu-id="962ca-167">To allow users to control the webpage that is displayed in your WebView2 control, add an address bar to your app.</span></span>  

1.  <span data-ttu-id="962ca-168">В `MainWindow.xaml` файле скопируйте и в paste следующий фрагмент кода внутри `<Grid>` элемента, который содержит `WebView2` элемент.</span><span class="sxs-lookup"><span data-stu-id="962ca-168">In the `MainWindow.xaml` file, copy and paste the following code snippet inside the `<Grid>` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="962ca-169">`<Grid>`Убедитесь, что элемент в `MainWindow.xaml` файле похож на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="962ca-169">Ensure your `<Grid>` element in the `MainWindow.xaml` file is similar to the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="962ca-170">Скопируйте в файл следующий фрагмент кода, чтобы перейти к url-адресу, введенного в адресной панели, с помощью управления `MainWindow.xaml.cs` `myButton_Click` WebView2.</span><span class="sxs-lookup"><span data-stu-id="962ca-170">In the `MainWindow.xaml.cs` file, copy the following code snippet into `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
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
    
    <span data-ttu-id="962ca-171">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="962ca-171">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="962ca-172">Введите новый URL-адрес в адресной панели и выберите **"Перейти".**</span><span class="sxs-lookup"><span data-stu-id="962ca-172">Enter a new URL in the address bar, and then choose **Go**.</span></span>  <span data-ttu-id="962ca-173">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="962ca-173">For example, enter `https://www.bing.com`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="962ca-174">Убедитесь, что вы вводите полные URL-адреса в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="962ca-174">Ensure you enter complete URLs in the address bar.</span></span>  `ArgumentException` <span data-ttu-id="962ca-175">исключения высылаются, если URL-адрес не начинается `http://` с или `https://` .</span><span class="sxs-lookup"><span data-stu-id="962ca-175">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="962ca-177">bing.com</span><span class="sxs-lookup"><span data-stu-id="962ca-177">bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="962ca-178">Шаг 4. События навигации</span><span class="sxs-lookup"><span data-stu-id="962ca-178">Step 4 - Navigation events</span></span>  

<span data-ttu-id="962ca-179">Приложения, в которые находятся элементы управления WebView2, прослушивают следующие события, которые вызываются элементами управления WebView2 во время навигации на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="962ca-179">Apps that host WebView2 controls listen for the following events that are raised by WebView2 controls during webpage navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

> [!NOTE]
> <span data-ttu-id="962ca-180">Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.</span><span class="sxs-lookup"><span data-stu-id="962ca-180">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="962ca-181">Дополнительные сведения можно найти в [меню "События навигации".][Webviews2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="962ca-181">For more information, navigate to [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="962ca-182">При ошибках возникают следующие события, которые могут переходить на веб-страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="962ca-182">When errors occur, the following events are raised and may navigate to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
     
<span data-ttu-id="962ca-183">В качестве примера использования событий зарегистрируйте обработок, который отменяет все запросы, не `NavigationStarting` относя такие как HTTPS.</span><span class="sxs-lookup"><span data-stu-id="962ca-183">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  <span data-ttu-id="962ca-184">В , измените конструктор для регистрации и добавьте функцию таким образом, чтобы она соответствует `MainWindow.xaml.cs` `EnsureHttps` `EnsureHttps` следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="962ca-184">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  

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

<span data-ttu-id="962ca-185">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="962ca-185">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="962ca-186">Убедитесь, что навигация заблокирована на сайтах HTTP и разрешена для сайтов HTTPS.</span><span class="sxs-lookup"><span data-stu-id="962ca-186">Ensure navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="962ca-187">Шаг 5. Сценарии</span><span class="sxs-lookup"><span data-stu-id="962ca-187">Step 5 - Scripting</span></span>  

<span data-ttu-id="962ca-188">Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.</span><span class="sxs-lookup"><span data-stu-id="962ca-188">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="962ca-189">Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="962ca-189">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="962ca-190">Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.</span><span class="sxs-lookup"><span data-stu-id="962ca-190">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="962ca-191">Введенный JavaScript работает с определенными сроками.</span><span class="sxs-lookup"><span data-stu-id="962ca-191">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="962ca-192">Запустите его после создания глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="962ca-192">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="962ca-193">Запустите его перед запуском любого другого сценария, включенного в HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="962ca-193">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="962ca-194">В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="962ca-194">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="962ca-195">Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее ExecuteScriptAsync.][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync]</span><span class="sxs-lookup"><span data-stu-id="962ca-195">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][Webviews2ReferenceWpfMicrosoftWebExecutescriptasync].</span></span>  

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

<span data-ttu-id="962ca-196">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="962ca-196">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="962ca-197">Убедитесь, что ваше приложение отображает оповещение при переходе на любые веб-сайты, не относящаться к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="962ca-197">Ensure your app displays an alert when you navigate to any non-HTTPS websites.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="В веб-оке управления WebView2 отображается диалоговое окно оповещения" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="962ca-199">В веб-оке управления WebView2 отображается диалоговое окно оповещения</span><span class="sxs-lookup"><span data-stu-id="962ca-199">WebView2 control displays an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="962ca-200">Поздравляем, вы создали свое первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="962ca-200">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="962ca-201">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="962ca-201">Next steps</span></span>  

<span data-ttu-id="962ca-202">Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="962ca-202">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="962ca-203">См. также</span><span class="sxs-lookup"><span data-stu-id="962ca-203">See also</span></span>  

*   <span data-ttu-id="962ca-204">Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples.][GithubMicrosoftedgeWebview2samplesMain]</span><span class="sxs-lookup"><span data-stu-id="962ca-204">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="962ca-205">Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="962ca-205">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="962ca-206">Объект WinRT CoreWebView2 может быть не доступен в выпуске API WebView2.</span><span class="sxs-lookup"><span data-stu-id="962ca-206">The WinRT CoreWebView2 object may not be available with the release of the WebView2 API.</span></span>  <span data-ttu-id="962ca-207">Чтобы понять, какие API доступны для элементов управления WebView2, перейдите к [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2] для списка доступных API.</span><span class="sxs-lookup"><span data-stu-id="962ca-207">To understand which APIs are available to WebView2 controls, navigate to [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span>  
    
*   <span data-ttu-id="962ca-208">Подробные сведения об API WebView2 можно найти в [спецификации WebView2.][GithubMicrosoftUiXamlSpecsWebview2]</span><span class="sxs-lookup"><span data-stu-id="962ca-208">For detailed information about the WebView2 API, navigate to [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  
    
## <span data-ttu-id="962ca-209">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="962ca-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
