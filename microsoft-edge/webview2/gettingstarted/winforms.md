---
description: Руководство по началу работы с WebView2 для приложений WinForms
title: Начало работы с WebView2 для приложений WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, веб-просмотр, приложения winforms, winforms, edge, CoreWebView2, элемент управления браузером, edge html, начало работы, начало работы, .NET, формы Windows
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306168"
---
# <span data-ttu-id="15416-104">Начало работы с WebView2 в Windows Forms</span><span class="sxs-lookup"><span data-stu-id="15416-104">Getting started with WebView2 in Windows Forms</span></span>

<span data-ttu-id="15416-105">В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="15416-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="15416-106">Дополнительные сведения об отдельных API можно найти в [справочнике по API.][DotnetApiMicrosoftWebWebview2Winforms]</span><span class="sxs-lookup"><span data-stu-id="15416-106">For more information on individual APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2Winforms].</span></span>  

## <span data-ttu-id="15416-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="15416-107">Prerequisites</span></span>  

<span data-ttu-id="15416-108">Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.</span><span class="sxs-lookup"><span data-stu-id="15416-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="15416-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="15416-109">[WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="15416-110">Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="15416-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="15416-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="15416-111">[Visual Studio][MicrosoftVisualstudioMain] 2017 or later.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="15416-112">В настоящее время WebView2 не поддерживает конструкторы .NET 5 и .NET Core.</span><span class="sxs-lookup"><span data-stu-id="15416-112">WebView2 currently does not support the .NET 5 and .NET Core designers.</span></span>

## <span data-ttu-id="15416-113">Шаг 1. Создание одноокнего приложения</span><span class="sxs-lookup"><span data-stu-id="15416-113">Step 1 - Create a single-window app</span></span>

<span data-ttu-id="15416-114">Начните с базового проекта настольного компьютера, который содержит одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="15416-114">Start with a basic desktop project that contains a single main window.</span></span>  

1.  <span data-ttu-id="15416-115">В Visual Studio выберите **приложение Windows Forms .NET Framework**  >  **App Next.**</span><span class="sxs-lookup"><span data-stu-id="15416-115">In Visual Studio, choose **Windows Forms .NET Framework App** > **Next**.</span></span>
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Новый проект" lightbox="./media/winforms-newproject.png":::
       <span data-ttu-id="15416-117">Новый проект</span><span class="sxs-lookup"><span data-stu-id="15416-117">New project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="15416-118">Введите значения для **имени и расположения** **проекта.**</span><span class="sxs-lookup"><span data-stu-id="15416-118">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="15416-119">Выберите **.NET Framework 4.6.2 или более** поздней.</span><span class="sxs-lookup"><span data-stu-id="15416-119">Choose **.NET Framework 4.6.2** or later.</span></span>  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Запуск проекта" lightbox="./media/winforms-startproj.png":::
       <span data-ttu-id="15416-121">Запуск проекта</span><span class="sxs-lookup"><span data-stu-id="15416-121">Start project</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="15416-122">Чтобы создать проект, выберите **"Создать".**</span><span class="sxs-lookup"><span data-stu-id="15416-122">To create your project, choose **Create**.</span></span>
    
## <span data-ttu-id="15416-123">Шаг 2. Установка SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="15416-123">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="15416-124">Добавьте в проект SDK WebView2 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="15416-124">Use NuGet to add the WebView2 SDK to the project.</span></span>  

1.  <span data-ttu-id="15416-125">Наведите курсор на проект, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Управление пакетами **NuGet"...**</span><span class="sxs-lookup"><span data-stu-id="15416-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Управление пакетами NuGet":::
       <span data-ttu-id="15416-127">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="15416-127">Manage NuGet Packages</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="15416-128">В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**</span><span class="sxs-lookup"><span data-stu-id="15416-128">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       <span data-ttu-id="15416-130">NuGet</span><span class="sxs-lookup"><span data-stu-id="15416-130">NuGet</span></span>  
    :::image-end:::
    
    <span data-ttu-id="15416-131">Начните разработку приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="15416-131">Start developing apps using the WebView2 API.</span></span>  <span data-ttu-id="15416-132">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-132">To build and run the project, select `F5`.</span></span>  <span data-ttu-id="15416-133">Запущенный проект отображает пустое окно.</span><span class="sxs-lookup"><span data-stu-id="15416-133">The running project displays an empty window.</span></span>  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Пустое приложение" lightbox="./media/winforms-emptyapp.png":::
       <span data-ttu-id="15416-135">Пустое приложение</span><span class="sxs-lookup"><span data-stu-id="15416-135">Empty app</span></span>  
    :::image-end:::
    
## <span data-ttu-id="15416-136">Шаг 3. Создание одного webView</span><span class="sxs-lookup"><span data-stu-id="15416-136">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="15416-137">Добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="15416-137">Add a WebView to your app.</span></span>  

1.  <span data-ttu-id="15416-138">Откройте **конструктор форм Windows.**</span><span class="sxs-lookup"><span data-stu-id="15416-138">Open the **Windows Forms Designer**.</span></span>  
1.  <span data-ttu-id="15416-139">Поиск **WebView2** на панели **инструментов.**</span><span class="sxs-lookup"><span data-stu-id="15416-139">Search for **WebView2** in the **Toolbox**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="15416-140">Если вы используете Visual Studio 2017, по умолчанию **WebView2** может не отображаться на **панели инструментов.**</span><span class="sxs-lookup"><span data-stu-id="15416-140">If you are using Visual Studio 2017, by default **WebView2** may not display in the **Toolbox**.</span></span>  <span data-ttu-id="15416-141">Чтобы включить поведение, **выберите**"Параметры инструментов" > для параметра "Автоматическое заполнение  >  \*\*\*\*  >  \*\*\*\* **панели инструментов".** `True`</span><span class="sxs-lookup"><span data-stu-id="15416-141">To enable the behavior, choose **Tools** > **Options** > **General** > set the **Automatically Populate Toolbox** setting to `True`.</span></span>  
    
    <span data-ttu-id="15416-142">Перетащите управление **WebView2** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="15416-142">Drag and drop the **WebView2** control into the Windows Forms App.</span></span>
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Панели инструментов, отображающие WebView2":::
       <span data-ttu-id="15416-144">Панели инструментов, отображающие WebView2</span><span class="sxs-lookup"><span data-stu-id="15416-144">Toolbox displaying WebView2</span></span>
    :::image-end:::  

1.  <span data-ttu-id="15416-145">За установите `(Name)` для свойства свойство `webView` .</span><span class="sxs-lookup"><span data-stu-id="15416-145">Set the `(Name)` property to `webView`.</span></span>
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Свойства управления WebView2":::
       <span data-ttu-id="15416-147">Свойства управления WebView2</span><span class="sxs-lookup"><span data-stu-id="15416-147">Properties of the WebView2 control</span></span>
    :::image-end:::

1.  <span data-ttu-id="15416-148">Свойство `Source` задает исходный URI, отображаемой в веб-2-объекте управления.</span><span class="sxs-lookup"><span data-stu-id="15416-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  <span data-ttu-id="15416-149">За установите `Source` для свойства свойство `https://www.microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="15416-149">Set the `Source` property to `https://www.microsoft.com`.</span></span>  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="Свойство Source для управления WebView2":::
       <span data-ttu-id="15416-151">Свойство **Source** для управления WebView2</span><span class="sxs-lookup"><span data-stu-id="15416-151">The **Source** property of the WebView2 control</span></span>
    :::image-end:::  

<span data-ttu-id="15416-152">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-152">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="15416-153">Убедитесь, что отображается ваш контроль [https://www.microsoft.com][|::ref1::|Main] WebView2.</span><span class="sxs-lookup"><span data-stu-id="15416-153">Ensure your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   <span data-ttu-id="15416-155">hello webview</span><span class="sxs-lookup"><span data-stu-id="15416-155">hello webview</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="15416-156">Если вы работаете с монитором с высоким DPI, может потребоваться настроить приложение Windows Forms для [поддержки высокого DPI.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]</span><span class="sxs-lookup"><span data-stu-id="15416-156">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport].</span></span>  

## <span data-ttu-id="15416-157">Шаг 4. Обработка событий window Resize</span><span class="sxs-lookup"><span data-stu-id="15416-157">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="15416-158">Добавьте в формы Windows Forms еще несколько элементов управления с панели элементов, а затем обработать события, соответствующие окну.</span><span class="sxs-lookup"><span data-stu-id="15416-158">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1.  <span data-ttu-id="15416-159">В **конструкторе форм Windows**откройте панели **инструментов**</span><span class="sxs-lookup"><span data-stu-id="15416-159">In the **Windows Forms Designer**, open the **Toolbox**</span></span>
1.  <span data-ttu-id="15416-160">Перетащите **TextBox в** приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="15416-160">Drag and drop a **TextBox** into the Windows Forms App.</span></span>  <span data-ttu-id="15416-161">На **вкладке "Свойства"** назовем **TextBox.** `addressBar`</span><span class="sxs-lookup"><span data-stu-id="15416-161">In the **Properties Tab**, name the **TextBox** `addressBar` .</span></span>
1.  <span data-ttu-id="15416-162">Перетащите **кнопку в** приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="15416-162">Drag and drop a **Button** into the Windows Forms App.</span></span>  <span data-ttu-id="15416-163">Измените текст кнопки на **кнопку** и `Go!` назовем **ее** на `goButton` **вкладке "Свойства".**</span><span class="sxs-lookup"><span data-stu-id="15416-163">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

    <span data-ttu-id="15416-164">Приложение должно выглядеть следующим образом в конструкторе.</span><span class="sxs-lookup"><span data-stu-id="15416-164">The app should look like the following image in the designer.</span></span>
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="designer" lightbox="./media/winforms-designer.png":::
       <span data-ttu-id="15416-166">designer</span><span class="sxs-lookup"><span data-stu-id="15416-166">designer</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="15416-167">В `Form1.cs` файле определите, что элементы управления должны быть на месте при повторном размере окна `Form_Resize` приложения.</span><span class="sxs-lookup"><span data-stu-id="15416-167">In the `Form1.cs` file, define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

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

<span data-ttu-id="15416-168">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-168">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="15416-169">Убедитесь, что приложение отображается примерно так, как по снимку экрана ниже.</span><span class="sxs-lookup"><span data-stu-id="15416-169">Ensure the app displays similar to the following screenshot.</span></span>

:::image type="complex" source="./media/winforms-app.png" alt-text="приложение" lightbox="./media/winforms-app.png":::
   <span data-ttu-id="15416-171">Приложение</span><span class="sxs-lookup"><span data-stu-id="15416-171">App</span></span>  
:::image-end:::

## <span data-ttu-id="15416-172">Шаг 5. Навигация</span><span class="sxs-lookup"><span data-stu-id="15416-172">Step 5 - Navigation</span></span>

<span data-ttu-id="15416-173">Добавьте возможность разрешить пользователям изменять URL-адрес, отображаемый в веб-функции Управления WebView2, добавив адресную стойку в приложение.</span><span class="sxs-lookup"><span data-stu-id="15416-173">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1.  <span data-ttu-id="15416-174">Чтобы добавить пространство имен, вставьте в файл следующий фрагмент кода `Form1.cs` `CoreWebView2` в верхней части файла.</span><span class="sxs-lookup"><span data-stu-id="15416-174">In the `Form1.cs`file, to add the `CoreWebView2` namespace, insert the following code snippet at the top.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  <span data-ttu-id="15416-175">В **конструкторе форм Windows**дважды щелкните кнопку, чтобы `Go!` создать метод в `goButton_Click` `Form1.cs` файле.</span><span class="sxs-lookup"><span data-stu-id="15416-175">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in the `Form1.cs` file.</span></span>  <span data-ttu-id="15416-176">Скопируйте и в paste следующий фрагмент кода внутри функции.</span><span class="sxs-lookup"><span data-stu-id="15416-176">Copy and paste the following snippet inside the function.</span></span>  <span data-ttu-id="15416-177">Теперь функция переходит в WebView по `goButton_Click` URL-адресу, введенного в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="15416-177">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="15416-178">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-178">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="15416-179">Введите новый URL-адрес в адресной панели и выберите **"Перейти".**</span><span class="sxs-lookup"><span data-stu-id="15416-179">Enter a new URL in the address bar, and select **Go**.</span></span>  <span data-ttu-id="15416-180">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="15416-180">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="15416-181">Убедитесь, что с помощью управления WebView2 можно перейти по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="15416-181">Ensure the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="15416-182">Убедитесь, что в адресной панели введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="15416-182">Ensure a complete URL is entered in the address bar.</span></span>  <span data-ttu-id="15416-183">Если URL-адрес не начинается с `ArgumentException` или `http://`</span><span class="sxs-lookup"><span data-stu-id="15416-183">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   <span data-ttu-id="15416-185">bing.com</span><span class="sxs-lookup"><span data-stu-id="15416-185">bing.com</span></span>  
:::image-end:::

## <span data-ttu-id="15416-186">Шаг 6. События навигации</span><span class="sxs-lookup"><span data-stu-id="15416-186">Step 6 - Navigation events</span></span>  

<span data-ttu-id="15416-187">Во время навигации на веб-странице с помощью управления WebView2 вызываются события.</span><span class="sxs-lookup"><span data-stu-id="15416-187">During webpage navigation, the WebView2 control raises events.</span></span>  <span data-ttu-id="15416-188">Приложение, в котором размещены элементы управления WebView2, прослушивает следующие события.</span><span class="sxs-lookup"><span data-stu-id="15416-188">The app that hosts WebView2 controls listens for the following events.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

<span data-ttu-id="15416-189">Дополнительные сведения можно найти в [меню "События навигации".][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="15416-189">For more information, navigate to [Navigation Events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="15416-191">События навигации</span><span class="sxs-lookup"><span data-stu-id="15416-191">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="15416-192">При ошибке возникают следующие события, которые могут зависеть от навигации на веб-страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="15416-192">When an error occurs, the following events are raised and may depend on navigation to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> <span data-ttu-id="15416-193">Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.</span><span class="sxs-lookup"><span data-stu-id="15416-193">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="15416-194">Чтобы продемонстрировать, как использовать эти события, сначала зарегистрируйте обработок, который отменит все запросы, которые не `NavigationStarting` используют ПРОТОКОЛ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="15416-194">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span>  

<span data-ttu-id="15416-195">В файле обновим конструктор в соответствии со следующим фрагментом кода и `Form1.cs` добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="15416-195">In the `Form1.cs` file, update the constructor to match the following code snippet and add the `EnsureHttps` function.</span></span>  

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

<span data-ttu-id="15416-196">В конструкторе EnsureHttps регистрируется как обработчик событий в событии `NavigationStarting` в control WebView2.</span><span class="sxs-lookup"><span data-stu-id="15416-196">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="15416-197">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-197">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="15416-198">Убедитесь, что при переходе к http-сайту Веб-просмотр остается без изменений.</span><span class="sxs-lookup"><span data-stu-id="15416-198">Ensure when navigating to an HTTP site, the WebView remains unchanged.</span></span>  <span data-ttu-id="15416-199">Однако WebView будет переходить на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="15416-199">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="15416-200">Шаг 7. Сценарии</span><span class="sxs-lookup"><span data-stu-id="15416-200">Step 7 - Scripting</span></span>  

<span data-ttu-id="15416-201">Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.</span><span class="sxs-lookup"><span data-stu-id="15416-201">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="15416-202">Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="15416-202">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="15416-203">Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.</span><span class="sxs-lookup"><span data-stu-id="15416-203">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="15416-204">Введенный JavaScript работает с определенными сроками.</span><span class="sxs-lookup"><span data-stu-id="15416-204">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="15416-205">Запустите его после создания глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="15416-205">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="15416-206">Запустите его перед запуском любого другого сценария, включенного в HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="15416-206">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="15416-207">В качестве примера добавьте сценарии, которые отправляют оповещение при переходе пользователя на сайты, не относящаться к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="15416-207">As an example, add scripts that send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="15416-208">Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое, [использующее метод ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]</span><span class="sxs-lookup"><span data-stu-id="15416-208">Modify the `EnsureHttps` function to inject a script into the web content that uses [ExecuteScriptAsync][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync] method.</span></span>  

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

<span data-ttu-id="15416-209">Чтобы построить и запустить проект, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-209">To build and run your project, select `F5`.</span></span>  <span data-ttu-id="15416-210">Убедитесь, что приложение отображает оповещение при переходе на веб-сайт, который не использует ПРОТОКОЛ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="15416-210">Ensure the app displays an alert when you navigate to a website that doesn't use HTTPS.</span></span>  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   <span data-ttu-id="15416-212">https</span><span class="sxs-lookup"><span data-stu-id="15416-212">https</span></span>  
:::image-end:::

## <span data-ttu-id="15416-213">Шаг 8. Взаимодействие между хост-контентом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="15416-213">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="15416-214">Содержимое хоста и веб-сайта может использовать для `postMessage` связи друг с другом следующим образом:</span><span class="sxs-lookup"><span data-stu-id="15416-214">The host and web content may use `postMessage` to communicate with each other as follows:</span></span>  

*   <span data-ttu-id="15416-215">Веб-содержимое в control WebView2 может использовать `window.chrome.webview.postMessage` для публикации сообщения на хост-сервере.</span><span class="sxs-lookup"><span data-stu-id="15416-215">Web content in a WebView2 control may use `window.chrome.webview.postMessage` to post a message to the host.</span></span>  <span data-ttu-id="15416-216">The host handles the message using any registered `WebMessageReceived` on the host.</span><span class="sxs-lookup"><span data-stu-id="15416-216">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
*   <span data-ttu-id="15416-217">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="15416-217">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="15416-218">Эти сообщения перехвачены обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="15416-218">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="15416-219">Механизм связи передает сообщения из веб-содержимого на хост с использованием своих возможностей.</span><span class="sxs-lookup"><span data-stu-id="15416-219">The communication mechanism passes messages from web content to the host using native capabilities.</span></span>  

<span data-ttu-id="15416-220">В проекте при переходе по URL-адресу с помощью управления WebView2 он отображает URL-адрес в адресной панели и оповещает пользователя об URL-адресе, отображаемом в веб-интерфейсе2.</span><span class="sxs-lookup"><span data-stu-id="15416-220">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1.  <span data-ttu-id="15416-221">В файле обновите конструктор и создайте функцию, которая `Form1.cs` `InitializeAsync` будет соответствовать следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="15416-221">In the `Form1.cs` file, update your constructor and create an `InitializeAsync` function to match the following code snippet.</span></span>  <span data-ttu-id="15416-222">Функция `InitializeAsync` ожидает [EnsureCoreWebView2Async,][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="15416-222">The `InitializeAsync` function awaits [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] because the initialization of `CoreWebView2` is asynchronous.</span></span>  

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

1.  <span data-ttu-id="15416-223">После `CoreWebView2` инициализации зарегистрируйте обработок событий, чтобы ответить `WebMessageReceived` на него.</span><span class="sxs-lookup"><span data-stu-id="15416-223">After `CoreWebView2` is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="15416-224">В `Form1.cs` файле `InitializeAsync` обновим и добавьте его, используя следующий `UpdateAddressBar` фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="15416-224">In the `Form1.cs` file, update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

1.  <span data-ttu-id="15416-225">Чтобы webView отправил веб-сообщение и ответил на него, после инициализации хост введет скрипт в `CoreWebView2` веб-содержимое, чтобы:</span><span class="sxs-lookup"><span data-stu-id="15416-225">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1.  <span data-ttu-id="15416-226">Отправьте URL-адрес на хост с помощью `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="15416-226">Send the URL to the host using `postMessage`.</span></span>
    1.  <span data-ttu-id="15416-227">Зарегистрируйте обработок событий, чтобы распечатать сообщение, отправленное с хоста.</span><span class="sxs-lookup"><span data-stu-id="15416-227">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="15416-228">В `Form1.cs` файле `InitializeAsync` обновим, чтобы он совпадал со следующим фрагментом кода.</span><span class="sxs-lookup"><span data-stu-id="15416-228">In the `Form1.cs` file, update `InitializeAsync` to match the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="15416-229">Чтобы выполнить сборку и запустить приложение, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="15416-229">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="15416-230">Теперь в адресной панели отображается URI в control WebView2.</span><span class="sxs-lookup"><span data-stu-id="15416-230">Now, the address bar displays the URI in the WebView2 control.</span></span>  <span data-ttu-id="15416-231">Кроме того, при успешном переходе к новому URL-адресу WebView оповещает пользователя об URL-адресе, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="15416-231">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Окончательное приложение" lightbox="./media/winforms-finalapp.png":::
   <span data-ttu-id="15416-233">Окончательное приложение</span><span class="sxs-lookup"><span data-stu-id="15416-233">Final app</span></span>  
:::image-end:::

<span data-ttu-id="15416-234">Поздравляем, вы создали свое первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="15416-234">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="15416-235">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="15416-235">Next steps</span></span>  

<span data-ttu-id="15416-236">Чтобы продолжить изучение WebView2, перейдите к следующим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="15416-236">To continue learning more about WebView2, navigate to the following resources.</span></span>  

### <span data-ttu-id="15416-237">См. также</span><span class="sxs-lookup"><span data-stu-id="15416-237">See also</span></span>  

*   <span data-ttu-id="15416-238">Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples.][GithubMicrosoftedgeWebview2samplesMain]</span><span class="sxs-lookup"><span data-stu-id="15416-238">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].</span></span>  
*   <span data-ttu-id="15416-239">Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2IndexNextSteps]</span><span class="sxs-lookup"><span data-stu-id="15416-239">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  
*   <span data-ttu-id="15416-240">Подробные сведения об API WebView2 можно найти в справочнике [по API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]</span><span class="sxs-lookup"><span data-stu-id="15416-240">For detailed information about the WebView2 API, navigate to [API reference][DotnetApiMicrosoftWebWebview2WinformsWebview2].</span></span>  

## <span data-ttu-id="15416-241">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="15416-241">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия: введение в Microsoft Edge WebView2 (предварительная | Документы Майкрософт"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Пространство имен Microsoft.Web.WebView2.WinForms | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Класс WebView2 | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Метод WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Документы Майкрософт"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.ExecuteScriptAsync(String) Method | Документы Майкрософт"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Настройка приложения Windows Forms для поддержки высокого DPI — поддержка высокого DPI в Windows Forms | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Разработчик Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Майкрософт"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  