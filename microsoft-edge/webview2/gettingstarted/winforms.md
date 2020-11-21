---
description: Руководство по началу работы с WebView2 для приложений для WinForms
title: Начало работы с WebView2 для приложений WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WinForms, WinForms, EDGE, CoreWebView2, браузер, край HTML, Приступая к работе, Приступая к работе, .NET, Windows Forms
ms.openlocfilehash: f4768c38f293d1931e625136ea7068a61176541e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182390"
---
# <span data-ttu-id="ca704-104">Начало работы с WebView2 в Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca704-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="ca704-105">В этой статье приступите к созданию первого приложения WebView2 и Узнайте о основных возможностях [WebView2](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="ca704-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="ca704-106">Дополнительные сведения об отдельных API можно найти в [справочнике API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="ca704-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="ca704-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="ca704-107">Prerequisites</span></span>  

<span data-ttu-id="ca704-108">Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:</span><span class="sxs-lookup"><span data-stu-id="ca704-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="ca704-109">[Среда выполнения WebView2][Webview2Installer] или любой [нестабильный канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download) , установленный в windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca704-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="ca704-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ca704-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="ca704-111">WebView2 в настоящее время не поддерживает базовые конструкторы .NET 5 и .NET.</span><span class="sxs-lookup"><span data-stu-id="ca704-111">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="ca704-112">Шаг 1: создание одного оконного приложения</span><span class="sxs-lookup"><span data-stu-id="ca704-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="ca704-113">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="ca704-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="ca704-114">Откройте **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="ca704-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="ca704-115">Выберите **приложение Windows Forms .NET Framework** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ca704-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

1. <span data-ttu-id="ca704-117">Введите значения для **имени проекта** и его **местоположения**.</span><span class="sxs-lookup"><span data-stu-id="ca704-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="ca704-118">Выберите **.NET Framework 4.6.2** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ca704-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="ca704-120">Нажмите кнопку **создать** , чтобы создать проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="ca704-121">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="ca704-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="ca704-122">Затем добавьте пакет SDK WebView2 в проект с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="ca704-122">Next add the WebView2 SDK to the project using NuGet.</span></span>

1. <span data-ttu-id="ca704-123">Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="ca704-123">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       <span data-ttu-id="ca704-125">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="ca704-125">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="ca704-126">Введите `Microsoft.Web.WebView2` строку поиска.</span><span class="sxs-lookup"><span data-stu-id="ca704-126">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="ca704-127">В результатах поиска выберите **Microsoft. Web. WebView2** .</span><span class="sxs-lookup"><span data-stu-id="ca704-127">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="ca704-129">Все готово для начала разработки приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca704-129">You're all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="ca704-130">Выберите `F5` для сборки и запуска проекта.</span><span class="sxs-lookup"><span data-stu-id="ca704-130">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="ca704-131">Запущенный проект отобразит пустое окно.</span><span class="sxs-lookup"><span data-stu-id="ca704-131">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="ca704-133">Шаг 3: создание единого WebView</span><span class="sxs-lookup"><span data-stu-id="ca704-133">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="ca704-134">Далее добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="ca704-134">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="ca704-135">Откройте **конструктор Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="ca704-135">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="ca704-136">Найдите **WebView2** на **панели элементов**.</span><span class="sxs-lookup"><span data-stu-id="ca704-136">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="ca704-137">Перетащите элемент управления **WebView2** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ca704-137">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Панель элементов, в которой отображается WebView2":::
       <span data-ttu-id="ca704-139">Панель элементов, в которой отображается WebView2</span><span class="sxs-lookup"><span data-stu-id="ca704-139">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="ca704-140">Измените `Name` свойство на `webView` .</span><span class="sxs-lookup"><span data-stu-id="ca704-140">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Свойства элемента управления WebView2":::
       <span data-ttu-id="ca704-142">Свойства элемента управления WebView2</span><span class="sxs-lookup"><span data-stu-id="ca704-142">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="ca704-143">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca704-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="ca704-144">Установите для свойства Source значение</span><span class="sxs-lookup"><span data-stu-id="ca704-144">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Свойство Source элемента управления WebView2":::
       <span data-ttu-id="ca704-146">Свойство Source элемента управления WebView2</span><span class="sxs-lookup"><span data-stu-id="ca704-146">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="ca704-147">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-147">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ca704-148">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ca704-148">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="ca704-150">Если вы работаете с монитором с высоким разрешением, может потребоваться [настроить поддержку высокого разрешения для приложения Windows Forms](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="ca704-150">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="ca704-151">Шаг 4: обработка событий изменения размера окна</span><span class="sxs-lookup"><span data-stu-id="ca704-151">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="ca704-152">Добавьте еще несколько элементов управления в формы Windows Forms с панели элементов, а затем обработайте события изменения размера окна соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ca704-152">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="ca704-153">В **конструкторе Windows Forms**откройте **область элементов** .</span><span class="sxs-lookup"><span data-stu-id="ca704-153">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1. <span data-ttu-id="ca704-154">Перетащите **текстовое поле** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ca704-154">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="ca704-155">Назовите **поле TextBox** `addressBar` на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="ca704-155">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="ca704-156">Перетащите **кнопку** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="ca704-156">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="ca704-157">Измените текст **кнопки** `Go!` и назовите **кнопку** на `goButton` **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="ca704-157">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="ca704-158">Приложение должно выглядеть так, как показано на следующем рисунке в конструкторе.</span><span class="sxs-lookup"><span data-stu-id="ca704-158">The app should look like the following image in the designer.</span></span>
    
    ![Проектировщик](./media/winforms-designer.png)

1. <span data-ttu-id="ca704-160">В **Form1.CS** определите, `Form_Resize` нужно ли сохранять элементы управления при изменении размера окна приложения.</span><span class="sxs-lookup"><span data-stu-id="ca704-160">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="ca704-161">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-161">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ca704-162">Убедитесь, что приложение отображается примерно так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="ca704-162">Confirm that the app displays similar to the following screenshot.</span></span>

![приложение](./media/winforms-app.png)

## <span data-ttu-id="ca704-164">Шаг 5 — Навигация</span><span class="sxs-lookup"><span data-stu-id="ca704-164">Step 5 - Navigation</span></span>

<span data-ttu-id="ca704-165">Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca704-165">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="ca704-166">В поле `Form1.cs` Добавить `CoreWebView2` пространство имен вставьте следующий фрагмент кода вверху `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="ca704-166">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="ca704-167">В **конструкторе Windows Forms**дважды щелкните `Go!` кнопку, чтобы создать `goButton_Click` метод `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="ca704-167">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="ca704-168">Скопируйте и вставьте следующий фрагмент в функцию.</span><span class="sxs-lookup"><span data-stu-id="ca704-168">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="ca704-169">Теперь `goButton_Click` функция переходит по WebView на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="ca704-169">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="ca704-170">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-170">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ca704-171">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="ca704-171">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="ca704-172">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="ca704-172">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="ca704-173">Убедитесь, что элемент управления WebView2 переходит по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="ca704-173">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="ca704-174">Убедитесь в том, что в адресной строке введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ca704-174">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="ca704-175">`ArgumentException`Если URL-адрес не начинается с `http://` или</span><span class="sxs-lookup"><span data-stu-id="ca704-175">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="ca704-177">Шаг 6 — события навигации</span><span class="sxs-lookup"><span data-stu-id="ca704-177">Step 6 - Navigation events</span></span>  

<span data-ttu-id="ca704-178">Во время навигации по веб-странице элемент управления WebView2 создает события.</span><span class="sxs-lookup"><span data-stu-id="ca704-178">During webpage navigation, the WebView2 control raises events.</span></span> <span data-ttu-id="ca704-179">Приложение, содержащее элементы управления WebView2, прослушивает следующие события.</span><span class="sxs-lookup"><span data-stu-id="ca704-179">The application that hosts WebView2 controls listens for the following events.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="ca704-180">Дополнительные сведения можно найти в разделе [события навигации](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="ca704-180">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="ca704-182">События навигации</span><span class="sxs-lookup"><span data-stu-id="ca704-182">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="ca704-183">При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="ca704-183">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="ca704-184">При перенаправлении HTTP есть несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="ca704-184">When there's an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="ca704-185">Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, не ИСПОЛЬЗУЮЩИЕ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ca704-185">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="ca704-186">`Form1.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="ca704-186">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

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

<span data-ttu-id="ca704-187">В конструкторе EnsureHttps регистрируется в качестве обработчика событий для `NavigationStarting` события в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca704-187">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="ca704-188">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-188">Select `F5` to build and run your project.</span></span> <span data-ttu-id="ca704-189">Убедитесь, что при переходе на веб-сайт HTTP WebView не меняется.</span><span class="sxs-lookup"><span data-stu-id="ca704-189">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="ca704-190">Однако WebView будет переходить на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ca704-190">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="ca704-191">Шаг 7: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="ca704-191">Step 7 - Scripting</span></span>  

<span data-ttu-id="ca704-192">Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca704-192">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="ca704-193">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален сценарий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca704-193">The injected JavaScript applies to all new top-level documents and any child frames, until the JavaScript is removed.</span></span>  <span data-ttu-id="ca704-194">Вставленный JavaScript запускается после создания глобального объекта и перед всеми сценариями, включенными в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="ca704-194">The injected JavaScript is run after creation of the global object, and before any scripts included in the HTML document.</span></span>  

<span data-ttu-id="ca704-195">Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ca704-195">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="ca704-196">Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="ca704-196">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="ca704-197">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="ca704-197">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="ca704-198">Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ca704-198">Confirm that the application displays an alert when you navigate to a site that doesn't use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="ca704-200">Шаг 8-связь между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="ca704-200">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="ca704-201">Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="ca704-201">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="ca704-202">Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ca704-202">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="ca704-203">Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.</span><span class="sxs-lookup"><span data-stu-id="ca704-203">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="ca704-204">Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="ca704-204">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="ca704-205">Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="ca704-205">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="ca704-206">Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.</span><span class="sxs-lookup"><span data-stu-id="ca704-206">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="ca704-207">Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="ca704-207">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="ca704-208">В **Form1.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="ca704-208">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="ca704-209">`InitializeAsync`Функция ожидает [EnsureCoreWebView2Async]() , так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="ca704-209">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

1. <span data-ttu-id="ca704-210">После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="ca704-210">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="ca704-211">В `Form1.cs` , обновить `InitializeAsync` и добавить `UpdateAddressBar` с помощью следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="ca704-211">In `Form1.cs`, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="ca704-212">Чтобы WebView отсылать и отвечать на веб-сообщение, после его `CoreWebView2` инициализации ведущее приложение вставляет сценарий в веб-содержимое в:</span><span class="sxs-lookup"><span data-stu-id="ca704-212">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="ca704-213">Отправьте URL-адрес узлу с помощью `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="ca704-213">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="ca704-214">Зарегистрируйте обработчик событий, чтобы напечатать сообщение, отправленное с узла.</span><span class="sxs-lookup"><span data-stu-id="ca704-214">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="ca704-215">В `Form1.cs` Обновите, `InitializeAsync` как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="ca704-215">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="ca704-216">Выберите `F5` , чтобы выполнить сборку и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="ca704-216">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="ca704-217">Убедитесь в том, что в адресной строке отображается URL-адрес сайта, отображаемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="ca704-217">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="ca704-218">Кроме того, при успешном переходе к новому URL-адресу WebView предупреждает пользователя об URL-адресе, показанном в WebView.</span><span class="sxs-lookup"><span data-stu-id="ca704-218">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="ca704-220">Поздравляем! вы создали первое приложение WebView2!</span><span class="sxs-lookup"><span data-stu-id="ca704-220">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="ca704-221">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="ca704-221">Next steps</span></span> 

<span data-ttu-id="ca704-222">Чтобы больше узнать о WebView2, перейдите к следующим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="ca704-222">To continue learning more about WebView2, navigate to the following resources.</span></span>

* <span data-ttu-id="ca704-223">В [репозитории WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) содержится подробный пример возможностей WebView2's.</span><span class="sxs-lookup"><span data-stu-id="ca704-223">The [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) has a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="ca704-224">[Справочник по API](/dotnet/api/microsoft.web.webview2.winforms.webview2) для получения более подробной информации о наших API.</span><span class="sxs-lookup"><span data-stu-id="ca704-224">The [API reference](/dotnet/api/microsoft.web.webview2.winforms.webview2) for more detailed information about our APIs.</span></span>
* <span data-ttu-id="ca704-225">[WebView2 ресурсы](../index.md#next-steps).</span><span class="sxs-lookup"><span data-stu-id="ca704-225">[WebView2 Resources](../index.md#next-steps).</span></span>


## <span data-ttu-id="ca704-226">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="ca704-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2" 
