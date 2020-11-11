---
description: Руководство по началу работы с WebView2 для приложений для WinForms
title: Начало работы с WebView2 для приложений WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WinForms, WinForms, EDGE, CoreWebView2, браузер, край HTML, Приступая к работе, Приступая к работе, .NET, Windows Forms
ms.openlocfilehash: c4092c545c24bf09667a5090251b51b96259efc2
ms.sourcegitcommit: a59464aff9e2c0bf57d172afbacdeed2c1a3ea42
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "11162641"
---
# <span data-ttu-id="b57a6-104">Начало работы с WebView2 в Windows Forms (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="b57a6-104">Getting started with WebView2 in Windows Forms (Preview)</span></span>  

<span data-ttu-id="b57a6-105">В этой статье приступите к созданию первого приложения WebView2 и ознакомьтесь с основными возможностями [WebView2 (Предварительная версия)](/microsoft-edge/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="b57a6-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/webview2/index).</span></span>  <span data-ttu-id="b57a6-106">Дополнительные сведения об отдельных API можно найти в [справочнике API](/dotnet/api/microsoft.web.webview2.winforms).</span><span class="sxs-lookup"><span data-stu-id="b57a6-106">For more information on individual APIs, see [API reference](/dotnet/api/microsoft.web.webview2.winforms).</span></span>  

## <span data-ttu-id="b57a6-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b57a6-107">Prerequisites</span></span>  

<span data-ttu-id="b57a6-108">Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:</span><span class="sxs-lookup"><span data-stu-id="b57a6-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="b57a6-109">[Среда выполнения WebView2][Webview2Installer] или любой [нестабильный канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download) , установленный в windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b57a6-109">[WebView2 Runtime][Webview2Installer] or any [non-stable Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="b57a6-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b57a6-110">[Visual Studio](https://visualstudio.microsoft.com) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="b57a6-111">WebView2 в настоящее время не поддерживает базовые конструкторы .NET 5 и .NET.</span><span class="sxs-lookup"><span data-stu-id="b57a6-111">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="b57a6-112">Шаг 1: создание одного оконного приложения</span><span class="sxs-lookup"><span data-stu-id="b57a6-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="b57a6-113">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="b57a6-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="b57a6-114">Откройте **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="b57a6-114">Open **Visual Studio.**</span></span>

1. <span data-ttu-id="b57a6-115">Выберите **приложение Windows Forms .NET Framework** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-115">Choose **Windows Forms .NET Framework App** and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

1. <span data-ttu-id="b57a6-117">Введите значения для **имени проекта** и его **местоположения**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="b57a6-118">Выберите **.NET Framework 4.6.2** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b57a6-118">Select **.NET Framework 4.6.2** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

1. <span data-ttu-id="b57a6-120">Нажмите кнопку **создать** , чтобы создать проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="b57a6-121">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="b57a6-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="b57a6-122">Затем добавьте в проект пакет SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="b57a6-123">Для предварительного просмотра установите пакет SDK WebView2 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="b57a6-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="b57a6-124">Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="b57a6-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       <span data-ttu-id="b57a6-126">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="b57a6-126">Manage NuGet Packages</span></span> :::image-end:::

1. <span data-ttu-id="b57a6-127">Введите `Microsoft.Web.WebView2` строку поиска.</span><span class="sxs-lookup"><span data-stu-id="b57a6-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="b57a6-128">В результатах поиска выберите **Microsoft. Web. WebView2** .</span><span class="sxs-lookup"><span data-stu-id="b57a6-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="b57a6-129">Убедитесь, что установлен флажок **Добавить предварительную**версию, выберите пакет предварительной версии в **версии**и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-129">Ensure you check **Include prerelease**, select a prerelease package in **Version**, and then choose **Install**.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="b57a6-131">Все готово для начала разработки приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="b57a6-132">Выберите `F5` для сборки и запуска проекта.</span><span class="sxs-lookup"><span data-stu-id="b57a6-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="b57a6-133">Запущенный проект отобразит пустое окно.</span><span class="sxs-lookup"><span data-stu-id="b57a6-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="b57a6-135">Шаг 3: создание единого WebView</span><span class="sxs-lookup"><span data-stu-id="b57a6-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="b57a6-136">Далее добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="b57a6-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="b57a6-137">Откройте **конструктор Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-137">Open the **Windows Forms Designer**.</span></span>  
1. <span data-ttu-id="b57a6-138">Найдите **WebView2** на **панели элементов**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="b57a6-139">Перетащите элемент управления **WebView2** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="b57a6-139">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Панель элементов, в которой отображается WebView2":::
       <span data-ttu-id="b57a6-141">Панель элементов, в которой отображается WebView2</span><span class="sxs-lookup"><span data-stu-id="b57a6-141">Toolbox displaying WebView2</span></span> :::image-end:::  

1. <span data-ttu-id="b57a6-142">Измените `Name` свойство на `webView` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-142">Change the `Name` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Свойства элемента управления WebView2":::
       <span data-ttu-id="b57a6-144">Свойства элемента управления WebView2</span><span class="sxs-lookup"><span data-stu-id="b57a6-144">Properties of the WebView2 control</span></span> :::image-end:::

1. <span data-ttu-id="b57a6-145">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-145">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="b57a6-146">Установите для свойства Source значение</span><span class="sxs-lookup"><span data-stu-id="b57a6-146">Set the Source property to</span></span> <https://www.microsoft.com>
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Свойство Source элемента управления WebView2":::
       <span data-ttu-id="b57a6-148">Свойство Source элемента управления WebView2</span><span class="sxs-lookup"><span data-stu-id="b57a6-148">The Source property of the WebView2 control</span></span> :::image-end:::

<span data-ttu-id="b57a6-149">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-149">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b57a6-150">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="b57a6-150">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="b57a6-152">Если вы работаете с монитором с высоким разрешением, может потребоваться [настроить поддержку высокого разрешения для приложения Windows Forms](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="b57a6-152">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="b57a6-153">Шаг 4: обработка событий изменения размера окна</span><span class="sxs-lookup"><span data-stu-id="b57a6-153">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="b57a6-154">Добавьте еще несколько элементов управления в формы Windows Forms с панели элементов, а затем обработайте события изменения размера окна соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="b57a6-154">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="b57a6-155">Открытие **панели элементов** в **конструкторе Windows Forms**</span><span class="sxs-lookup"><span data-stu-id="b57a6-155">In the **Windows Forms Designer** open the **Toolbox**</span></span>
1. <span data-ttu-id="b57a6-156">Перетащите **текстовое поле** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="b57a6-156">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="b57a6-157">Назовите **поле TextBox** `addressBar` на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-157">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
1. <span data-ttu-id="b57a6-158">Перетащите **кнопку** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="b57a6-158">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="b57a6-159">Измените текст **кнопки** `Go!` и назовите **кнопку** на `goButton` **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-159">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="b57a6-160">Приложение должно выглядеть так, как показано в конструкторе:</span><span class="sxs-lookup"><span data-stu-id="b57a6-160">The app should look like the following in the designer:</span></span>
    
    ![Проектировщик](./media/winforms-designer.png)

1. <span data-ttu-id="b57a6-162">В **Form1.CS** определите, `Form_Resize` нужно ли сохранять элементы управления при изменении размера окна приложения.</span><span class="sxs-lookup"><span data-stu-id="b57a6-162">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="b57a6-163">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-163">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b57a6-164">Убедитесь, что приложение отображается примерно так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="b57a6-164">Confirm that the app displays similar to the following screenshot.</span></span>

![приложение](./media/winforms-app.png)

## <span data-ttu-id="b57a6-166">Шаг 5 — Навигация</span><span class="sxs-lookup"><span data-stu-id="b57a6-166">Step 5 - Navigation</span></span>

<span data-ttu-id="b57a6-167">Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-167">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="b57a6-168">В поле `Form1.cs` Добавить `CoreWebView2` пространство имен вставьте следующий фрагмент кода вверху `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-168">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. <span data-ttu-id="b57a6-169">В **конструкторе Windows Forms**дважды щелкните `Go!` кнопку, чтобы создать `goButton_Click` метод `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-169">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="b57a6-170">Скопируйте и вставьте следующий фрагмент в функцию.</span><span class="sxs-lookup"><span data-stu-id="b57a6-170">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="b57a6-171">Теперь `goButton_Click` функция переходит по WebView на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="b57a6-171">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="b57a6-172">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-172">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b57a6-173">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="b57a6-173">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="b57a6-174">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-174">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="b57a6-175">Убедитесь, что элемент управления WebView2 переходит по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="b57a6-175">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="b57a6-176">Убедитесь в том, что в адресной строке введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="b57a6-176">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="b57a6-177">`ArgumentException`Если URL-адрес не начинается с `http://` или</span><span class="sxs-lookup"><span data-stu-id="b57a6-177">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="b57a6-179">Шаг 6 — события навигации</span><span class="sxs-lookup"><span data-stu-id="b57a6-179">Step 6 - Navigation events</span></span>  

<span data-ttu-id="b57a6-180">Приложение, содержащее элементы управления WebView2, прослушивает следующие события, возникающие при переходе на веб-страницы с помощью элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-180">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="b57a6-181">Дополнительные сведения можно найти в разделе [события навигации](../concepts/navigation-events.md).</span><span class="sxs-lookup"><span data-stu-id="b57a6-181">For more information, see [Navigation Events](../concepts/navigation-events.md).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="b57a6-183">События навигации</span><span class="sxs-lookup"><span data-stu-id="b57a6-183">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="b57a6-184">При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="b57a6-184">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="b57a6-185">При перенаправлении HTTP есть несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="b57a6-185">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="b57a6-186">Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, которые не используют HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b57a6-186">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="b57a6-187">`Form1.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="b57a6-187">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="b57a6-188">В конструкторе EnsureHttps регистрируется в качестве обработчика событий для `NavigationStarting` события в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-188">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="b57a6-189">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-189">Select `F5` to build and run your project.</span></span> <span data-ttu-id="b57a6-190">Убедитесь, что при переходе на веб-сайт HTTP WebView не меняется.</span><span class="sxs-lookup"><span data-stu-id="b57a6-190">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="b57a6-191">Однако WebView будет переходить на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b57a6-191">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="b57a6-192">Шаг 7: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="b57a6-192">Step 7 - Scripting</span></span>  

<span data-ttu-id="b57a6-193">Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="b57a6-193">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="b57a6-194">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b57a6-194">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="b57a6-195">Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="b57a6-195">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="b57a6-196">Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b57a6-196">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="b57a6-197">Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="b57a6-197">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

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

<span data-ttu-id="b57a6-198">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="b57a6-198">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="b57a6-199">Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b57a6-199">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="b57a6-201">Шаг 8-связь между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="b57a6-201">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="b57a6-202">Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="b57a6-202">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="b57a6-203">Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-203">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="b57a6-204">Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.</span><span class="sxs-lookup"><span data-stu-id="b57a6-204">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="b57a6-205">Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-205">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="b57a6-206">Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-206">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="b57a6-207">Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.</span><span class="sxs-lookup"><span data-stu-id="b57a6-207">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="b57a6-208">Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="b57a6-208">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="b57a6-209">В **Form1.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="b57a6-209">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="b57a6-210">`InitializeAsync`Функция ожидает [EnsureCoreWebView2Async]() , так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="b57a6-210">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1. <span data-ttu-id="b57a6-211">После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-211">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="b57a6-212">В разделе `Form1.cs` Update `InitializeAsync` и Add `UpdateAddressBar` (добавить с помощью следующего фрагмента кода).</span><span class="sxs-lookup"><span data-stu-id="b57a6-212">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1. <span data-ttu-id="b57a6-213">Чтобы WebView отсылать и отвечать на веб-сообщение, после его `CoreWebView2` инициализации ведущее приложение вставляет сценарий в веб-содержимое в:</span><span class="sxs-lookup"><span data-stu-id="b57a6-213">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="b57a6-214">Отправьте URL-адрес узлу с помощью `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="b57a6-214">Send the URL to the host using `postMessage`.</span></span>
    1. <span data-ttu-id="b57a6-215">Зарегистрируйте обработчик событий, чтобы напечатать сообщение, отправленное с узла.</span><span class="sxs-lookup"><span data-stu-id="b57a6-215">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="b57a6-216">В `Form1.cs` Обновите, `InitializeAsync` как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="b57a6-216">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="b57a6-217">Выберите `F5` , чтобы выполнить сборку и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="b57a6-217">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="b57a6-218">Убедитесь в том, что в адресной строке отображается URL-адрес сайта, отображаемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="b57a6-218">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="b57a6-219">Кроме того, при успешном переходе к новому URL-адресу WebView предупреждает пользователя об URL-адресе, показанном в WebView.</span><span class="sxs-lookup"><span data-stu-id="b57a6-219">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="b57a6-221">Поздравляем! вы создали первое приложение WebView2!</span><span class="sxs-lookup"><span data-stu-id="b57a6-221">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="b57a6-222">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b57a6-222">Next steps</span></span> 

* <span data-ttu-id="b57a6-223">Провлеките [WebView2Samplesный репозиторий](https://github.com/MicrosoftEdge/WebView2Samples) с подробным примером возможностей WebView2's</span><span class="sxs-lookup"><span data-stu-id="b57a6-223">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="b57a6-224">Дополнительные сведения об интерфейсах API для извлечения [справочных](/dotnet/api/microsoft.web.webview2.winforms.webview2) данных</span><span class="sxs-lookup"><span data-stu-id="b57a6-224">Checkout [API reference](/dotnet/api/microsoft.web.webview2.winforms.webview2) for more detailed information about our APIs</span></span>
* <span data-ttu-id="b57a6-225">Извлечение списка [ресурсов WebView2](../index.md#next-steps) для получения дополнительных сведений о WebView2</span><span class="sxs-lookup"><span data-stu-id="b57a6-225">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="b57a6-226">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b57a6-226">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  


<!-- links -->  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2" 