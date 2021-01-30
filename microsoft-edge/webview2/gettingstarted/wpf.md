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
# <span data-ttu-id="6eee3-104">Начало работы с WebView2 в WPF</span><span class="sxs-lookup"><span data-stu-id="6eee3-104">Getting started with WebView2 in WPF</span></span>

<span data-ttu-id="6eee3-105">В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="6eee3-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="6eee3-106">Дополнительные сведения об отдельных API можно найти в [справочнике по API.][DotnetApiMicrosoftWebWebview2Wpf]</span><span class="sxs-lookup"><span data-stu-id="6eee3-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Wpf].</span></span>  

## <span data-ttu-id="6eee3-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="6eee3-107">Prerequisites</span></span>  

<span data-ttu-id="6eee3-108">Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.</span><span class="sxs-lookup"><span data-stu-id="6eee3-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="6eee3-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="6eee3-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
*   <span data-ttu-id="6eee3-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6eee3-110">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
## <span data-ttu-id="6eee3-111">Шаг 1. Создание одноокнего приложения</span><span class="sxs-lookup"><span data-stu-id="6eee3-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="6eee3-112">Начните с базового проекта настольного компьютера, который содержит одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="6eee3-112">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="6eee3-113">В Visual Studio выберите **WPF .NET Core App** \(или **WPF .NET Framework App**\) > **Далее.**</span><span class="sxs-lookup"><span data-stu-id="6eee3-113">In Visual Studio, choose **WPF .NET Core App** \(or **WPF .NET Framework App**\) > **Next**.</span></span>  
    
    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="WPF core":::
             <span data-ttu-id="6eee3-115">WPF core</span><span class="sxs-lookup"><span data-stu-id="6eee3-115">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="WPF Framework":::
             <span data-ttu-id="6eee3-117">WPF Framework</span><span class="sxs-lookup"><span data-stu-id="6eee3-117">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="6eee3-118">Введите значения для **имени и расположения** **проекта.**</span><span class="sxs-lookup"><span data-stu-id="6eee3-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="6eee3-119">Выберите **.NET Framework 4.6.2 или более** поздней \(или **.NET Core 3.0 или** более поздней\).</span><span class="sxs-lookup"><span data-stu-id="6eee3-119">Choose **.NET Framework 4.6.2** or later \(or **.NET Core 3.0** or later\).</span></span>  
    
    :::row:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Создание ядра":::
                 <span data-ttu-id="6eee3-121">Создание ядра</span><span class="sxs-lookup"><span data-stu-id="6eee3-121">Create core</span></span> :::image-end:::
           :::column-end:::
           :::column span="1":::
              :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Create Framework":::
                 <span data-ttu-id="6eee3-123">Create Framework</span><span class="sxs-lookup"><span data-stu-id="6eee3-123">Create Framework</span></span> :::image-end:::
           :::column-end:::
        :::row-end:::
    
1.  <span data-ttu-id="6eee3-124">Чтобы создать проект, выберите **"Создать".**</span><span class="sxs-lookup"><span data-stu-id="6eee3-124">To create your project, choose **Create**.</span></span>  
    
## <span data-ttu-id="6eee3-125">Шаг 2. Установка SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="6eee3-125">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="6eee3-126">Добавьте в проект SDK WebView2 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="6eee3-126">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="6eee3-127">Наведите курсор на проектив, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт "Управление пакетами **NuGet"...**</span><span class="sxs-lookup"><span data-stu-id="6eee3-127">Hover on the projecty, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       <span data-ttu-id="6eee3-129">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="6eee3-129">Manage NuGet packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6eee3-130">В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**</span><span class="sxs-lookup"><span data-stu-id="6eee3-130">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
   
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="6eee3-132">NuGet</span><span class="sxs-lookup"><span data-stu-id="6eee3-132">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="6eee3-133">Вы готовы приступить к разработке приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-133">Ready to start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="6eee3-134">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-134">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="6eee3-135">Запущенный проект отображает пустое окно.</span><span class="sxs-lookup"><span data-stu-id="6eee3-135">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Пустое приложение":::
       <span data-ttu-id="6eee3-137">Пустое приложение</span><span class="sxs-lookup"><span data-stu-id="6eee3-137">Empty app</span></span>
    :::image-end:::  
    
## <span data-ttu-id="6eee3-138">Шаг 3. Создание одного веб-view в MainWindow.xaml</span><span class="sxs-lookup"><span data-stu-id="6eee3-138">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="6eee3-139">Затем добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="6eee3-139">Next add a WebView to your app.</span></span>  

1.  <span data-ttu-id="6eee3-140">Чтобы добавить `MainWindow.xaml` пространство имен XAML WebView2 в файл, вставьте следующую строку в `<Window/>` тег.</span><span class="sxs-lookup"><span data-stu-id="6eee3-140">In the `MainWindow.xaml` file, to add the WebView2 XAML namespace, insert the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  
    
    <span data-ttu-id="6eee3-141">Убедитесь, что код `MainWindow.xaml` в коде выглядит следующим фрагментом кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-141">Ensure the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="6eee3-142">Чтобы добавить управление WebView2, замените теги на `<Grid>` следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-142">To add the WebView2 control, replace the `<Grid>` tags with the following code snippet.</span></span>  <span data-ttu-id="6eee3-143">Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.</span><span class="sxs-lookup"><span data-stu-id="6eee3-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  
    
1.  <span data-ttu-id="6eee3-144">Чтобы выполнить сборку и запустить проект, выберите "Убедитесь, что ваш control `F5`  WebView2 [https://www.microsoft.com][|::ref1::|Main] отображается".</span><span class="sxs-lookup"><span data-stu-id="6eee3-144">To build and run the project, select `F5`  Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="6eee3-146">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6eee3-146">Microsoft.com</span></span>
    :::image-end:::  
    
## <span data-ttu-id="6eee3-147">Шаг 4. Навигация</span><span class="sxs-lookup"><span data-stu-id="6eee3-147">Step 4 - Navigation</span></span>  

<span data-ttu-id="6eee3-148">Добавьте возможность разрешить пользователям изменять URL-адрес, отображаемый в веб-функции Управления WebView2, добавив адресную стойку в приложение.</span><span class="sxs-lookup"><span data-stu-id="6eee3-148">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="6eee3-149">В файле добавьте адресную планку, скопируя и впавив в него следующий фрагмент `MainWindow.xaml` `<DockPanel>` кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-149">In the `MainWindow.xaml` file, add an address bar by copying and pasting the following code snippet inside the `<DockPanel>` that contains the WebView.</span></span>  
    
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
    
    <span data-ttu-id="6eee3-150">`<DockPanel>`Убедитесь, что раздел файла соответствует `MainWindow.xaml` следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-150">Ensure the `<DockPanel>` section of the `MainWindow.xaml` file matches the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="6eee3-151">В Visual Studio файле, чтобы добавить пространство имен, вставьте следующий фрагмент кода `MainWindow.xaml.cs` `CoreWebView2` вверху.</span><span class="sxs-lookup"><span data-stu-id="6eee3-151">In Visual Studio, in the `MainWindow.xaml.cs` file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  <span data-ttu-id="6eee3-152">Скопируйте в файл следующий фрагмент кода, чтобы создать метод, который переходит в WebView по URL-адресу, `MainWindow.xaml.cs` `ButtonGo_Click` введенного в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="6eee3-152">In the `MainWindow.xaml.cs`file, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
    <span data-ttu-id="6eee3-153">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-153">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="6eee3-154">Введите новый URL-адрес в адресной панели и выберите **"Перейти".**</span><span class="sxs-lookup"><span data-stu-id="6eee3-154">Type a new URL in the address bar and choose **Go**.</span></span>  <span data-ttu-id="6eee3-155">Например, введите `https://www.bing.com`.</span><span class="sxs-lookup"><span data-stu-id="6eee3-155">For example, type `https://www.bing.com`.</span></span>  <span data-ttu-id="6eee3-156">Убедитесь, что с помощью управления WebView2 можно перейти по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="6eee3-156">Ensure the WebView2 control navigates to the URL.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6eee3-157">Убедитесь, что в адресной панели введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6eee3-157">Make sure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="6eee3-158">Если URL-адрес не начинается с или . `ArgumentException` `http://` `https://`</span><span class="sxs-lookup"><span data-stu-id="6eee3-158">An `ArgumentException` is thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
       <span data-ttu-id="6eee3-160">bing.com</span><span class="sxs-lookup"><span data-stu-id="6eee3-160">bing.com</span></span>
    :::image-end:::
    
## <span data-ttu-id="6eee3-161">Шаг 5. События навигации</span><span class="sxs-lookup"><span data-stu-id="6eee3-161">Step 5 - Navigation events</span></span>  

<span data-ttu-id="6eee3-162">Во время навигации на веб-странице с помощью управления WebView2 вызываются события.</span><span class="sxs-lookup"><span data-stu-id="6eee3-162">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="6eee3-163">Приложение, в котором размещены элементы управления WebView2, прослушивает следующие события.</span><span class="sxs-lookup"><span data-stu-id="6eee3-163">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="6eee3-164">Дополнительные сведения можно найти в [меню "События навигации".][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="6eee3-164">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="6eee3-166">События навигации</span><span class="sxs-lookup"><span data-stu-id="6eee3-166">Navigation events</span></span>
:::image-end:::  

<span data-ttu-id="6eee3-167">При ошибке возникают следующие события, которые могут зависеть от навигации на веб-страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="6eee3-167">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="6eee3-168">Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.</span><span class="sxs-lookup"><span data-stu-id="6eee3-168">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="6eee3-169">Чтобы продемонстрировать, как использовать события, зарегистрируйте обработок, который отменяет все запросы, не `NavigationStarting` относя такие как HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6eee3-169">To demonstrate how to use the events, register a handler for `NavigationStarting` that cancels any non-HTTPS requests.</span></span>  

<span data-ttu-id="6eee3-170">В файле измените конструктор в соответствии со следующим фрагментом кода и `MainWindow.xaml.cs` добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="6eee3-170">In the `MainWindow.xaml.cs` file, modify the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="6eee3-171">В конструкторе EnsureHttps регистрируется как обработчик событий в событии `NavigationStarting` в control WebView2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-171">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="6eee3-172">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-172">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="6eee3-173">Убедитесь, что при переходе к http-сайту Веб-просмотр остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="6eee3-173">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="6eee3-174">Однако WebView переходит на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6eee3-174">However, the WebView navigates to HTTPS sites.</span></span>  

## <span data-ttu-id="6eee3-175">Шаг 6. Сценарии</span><span class="sxs-lookup"><span data-stu-id="6eee3-175">Step 6 - Scripting</span></span>  

<span data-ttu-id="6eee3-176">Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.</span><span class="sxs-lookup"><span data-stu-id="6eee3-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="6eee3-177">Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="6eee3-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="6eee3-178">Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.</span><span class="sxs-lookup"><span data-stu-id="6eee3-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="6eee3-179">Введенный JavaScript работает с определенными сроками.</span><span class="sxs-lookup"><span data-stu-id="6eee3-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="6eee3-180">Запустите его после создания глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="6eee3-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="6eee3-181">Запустите его перед запуском любого другого сценария, включенного в HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="6eee3-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="6eee3-182">В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6eee3-182">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="6eee3-183">Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее метод ExecuteScriptAsync.](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync)</span><span class="sxs-lookup"><span data-stu-id="6eee3-183">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync](/dotnet/api/microsoft.web.webview2.wpf.webview2.executescriptasync) method.</span></span>  

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

<span data-ttu-id="6eee3-184">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-184">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="6eee3-185">Убедитесь, что приложение отображает оповещение при переходе на веб-сайт, который не использует ПРОТОКОЛ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6eee3-185">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="6eee3-187">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6eee3-187">HTTPS</span></span>
:::image-end:::  

## <span data-ttu-id="6eee3-188">Шаг 7. Взаимодействие между хост-контентом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="6eee3-188">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="6eee3-189">Содержимое хоста и веб-сайта может взаимодействовать друг с другом следующим `postMessage` образом:</span><span class="sxs-lookup"><span data-stu-id="6eee3-189">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

*   <span data-ttu-id="6eee3-190">Веб-содержимое в веб-окте управления WebView2 может отправлять сообщение на хост с помощью `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-190">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="6eee3-191">The host handles the message using any registered `WebMessageReceived` on the host.</span><span class="sxs-lookup"><span data-stu-id="6eee3-191">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="6eee3-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-192">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="6eee3-193">Эти сообщения перехвачены обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-193">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="6eee3-194">Механизм связи передает сообщения из веб-содержимого на хост с использованием своих возможностей.</span><span class="sxs-lookup"><span data-stu-id="6eee3-194">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="6eee3-195">В проекте при переходе по URL-адресу с помощью управления WebView2 он отображает URL-адрес в адресной панели и оповещает пользователя об URL-адресе, отображаемом в веб-интерфейсе2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-195">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="6eee3-196">В файле обновите конструктор и создайте функцию, которая `MainWindow.xaml.cs` `InitializeAsync` будет соответствовать следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-196">In the `MainWindow.xaml.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="6eee3-197">Функция `InitializeAsync` ожидает [EnsureCoreWebView2Async,](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="6eee3-197">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](/dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  
    
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
    
1.  <span data-ttu-id="6eee3-198">После **инициализации CoreWebView2** зарегистрируйте обработец событий для `WebMessageReceived` ответа.</span><span class="sxs-lookup"><span data-stu-id="6eee3-198">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="6eee3-199">В `MainWindow.xaml.cs` , обновить и добавить с помощью следующего `InitializeAsync` `UpdateAddressBar` фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-199">In `MainWindow.xaml.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="6eee3-200">Чтобы webView отправил веб-сообщение после инициализации и реагировал на `CoreWebView2` него, хост:</span><span class="sxs-lookup"><span data-stu-id="6eee3-200">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  
    1.  <span data-ttu-id="6eee3-201">Внедряет сценарий в веб-содержимое, которое регистрирует обработок для печати сообщения с ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="6eee3-201">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    1.  <span data-ttu-id="6eee3-202">Внедряет сценарий в веб-содержимое, которое публикует URL-адрес на хост-сайте.</span><span class="sxs-lookup"><span data-stu-id="6eee3-202">Injects a script to the web content that posts the URL to the host.</span></span>  
        
    <span data-ttu-id="6eee3-203">В `MainWindow.xaml.cs` файле `InitializeAsync` обновим, чтобы он совпадал со следующим фрагментом кода.</span><span class="sxs-lookup"><span data-stu-id="6eee3-203">In the `MainWindow.xaml.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
        
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
        await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
    }
    ```  
    
    <span data-ttu-id="6eee3-204">Чтобы выполнить сборку и запустить приложение, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="6eee3-204">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="6eee3-205">Теперь в адресной панели отображается URI в control WebView2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-205">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="6eee3-206">При успешном переходе к новому URI веб-часть управления WebView2 оповещает пользователя об URI, отображаемом в этом ОКБ WebView2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-206">When you successfully navigate to a new URI, the WebView2 control alerts the user of the URI that's displayed in the WebView2 control.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
       <span data-ttu-id="6eee3-208">addressBar</span><span class="sxs-lookup"><span data-stu-id="6eee3-208">addressBar</span></span>
    :::image-end:::

<span data-ttu-id="6eee3-209">Поздравляем, вы создали свое первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="6eee3-209">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="6eee3-210">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6eee3-210">Next steps</span></span>  

<span data-ttu-id="6eee3-211">Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="6eee3-211">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="6eee3-212">См. также</span><span class="sxs-lookup"><span data-stu-id="6eee3-212">See also</span></span>  

*   <span data-ttu-id="6eee3-213">Полный пример возможностей WebView2 можно найти в репозитарии [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="6eee3-213">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samplesMain] on GitHub.</span></span>  
*   <span data-ttu-id="6eee3-214">Дополнительные сведения об API WebView2 можно найти в справочнике [по API.](/dotnet/api/microsoft.web.webview2.wpf.webview2)</span><span class="sxs-lookup"><span data-stu-id="6eee3-214">For more detailed information about WebView2 API, navigate to [API reference](/dotnet/api/microsoft.web.webview2.wpf.webview2).</span></span>  
*   <span data-ttu-id="6eee3-215">Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.](../index.md#next-steps)</span><span class="sxs-lookup"><span data-stu-id="6eee3-215">For more information about  WebView2, navigate to [WebView2 Resources](../index.md#next-steps).</span></span>  

## <span data-ttu-id="6eee3-216">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="6eee3-216">Getting in touch with the Microsoft Edge WebView team</span></span>  

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