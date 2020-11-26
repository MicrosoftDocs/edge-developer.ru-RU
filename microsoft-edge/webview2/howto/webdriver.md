---
description: Автоматизация и тестирование элемента управления WebView2 с помощью драйвера Microsoft Edge
title: Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, EDGE, ICoreWebView2, ICoreWebView2Controller, Selenium, драйвер Microsoft Edge
ms.openlocfilehash: 2af1ce222abb1dc7a279afc05e87e7e42a45fe9e
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191619"
---
# <span data-ttu-id="34d8f-104">Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34d8f-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="34d8f-105">Так как WebView2 использует веб-платформу Microsoft Edge \ (Chromium \), WebView2 разработчиков \ (ты \) может воспользоваться стандартными веб-возможностями для отладки и автоматизации.</span><span class="sxs-lookup"><span data-stu-id="34d8f-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="34d8f-106">Selenium — это одно из таких средств.</span><span class="sxs-lookup"><span data-stu-id="34d8f-106">Selenium is one such tool.</span></span>  <span data-ttu-id="34d8f-107">Он реализует API-интерфейс для интерфейса- [дисковода][W3cWebdriver2] W3C.</span><span class="sxs-lookup"><span data-stu-id="34d8f-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="34d8f-108">Вы можете использовать Selenium для создания автоматических тестов для моделирования взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="34d8f-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="34d8f-109">Чтобы начать работу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="34d8f-109">Get started with the following steps.</span></span>  

## <span data-ttu-id="34d8f-110">Шаг 1: Загрузка образца WebView2API</span><span class="sxs-lookup"><span data-stu-id="34d8f-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="34d8f-111">Если у вас нет проекта WebView2, скачайте [пример приложения WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], полный пример НОВЕЙШЕГО пакета SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="34d8f-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="34d8f-112">Убедитесь, что вы удовлетворены [требованиями для примера приложения WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span><span class="sxs-lookup"><span data-stu-id="34d8f-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="34d8f-113">Создав точную копию репозитория, создайте проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="34d8f-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="34d8f-114">Оно должно выглядеть так, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="34d8f-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Пример приложения WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="34d8f-116">Пример приложения WebView2API</span><span class="sxs-lookup"><span data-stu-id="34d8f-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <span data-ttu-id="34d8f-117">Шаг 2: Установка драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34d8f-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="34d8f-118">Следуйте инструкциям, чтобы установить [драйвер Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] , необходимый для автоматизации и тестирования WebView2, который требуется драйверу Selenium для веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="34d8f-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="34d8f-119">Убедитесь, что версия драйвера Microsoft Edge совпадает с версией среды выполнения WebView2, используемой Вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="34d8f-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="34d8f-120">Чтобы WebView2API пример работал, убедитесь в том, что ваша версия среды выполнения WebView2 больше или равна поддерживаемой версии новейшего выпуска SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="34d8f-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="34d8f-121">Чтобы найти последнюю версию SDK для WebView2, перейдите к [WebView2 заметкам о выпуске][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="34d8f-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="34d8f-122">Чтобы узнать, какая у вас версия среды выполнения WebView2 в настоящее время, перейдите на `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="34d8f-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <span data-ttu-id="34d8f-123">Шаг 3: Добавление Selenium в пример WebView2API</span><span class="sxs-lookup"><span data-stu-id="34d8f-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="34d8f-124">На этом этапе необходимо установить среду выполнения WebView2, создать WebView2 проект и установить драйвер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="34d8f-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="34d8f-125">Теперь приступите к работе с Selenium.</span><span class="sxs-lookup"><span data-stu-id="34d8f-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="34d8f-126">Selenium поддерживает C \ #, Java, Python, JavaScript и Ruby.</span><span class="sxs-lookup"><span data-stu-id="34d8f-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="34d8f-127">Однако приведенное ниже руководство написано с использованием C \ #.</span><span class="sxs-lookup"><span data-stu-id="34d8f-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="34d8f-128">Начните с создания нового проекта **C# .NET Framework** в **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="34d8f-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="34d8f-129">Чтобы продолжить, нажмите кнопку **Далее** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="34d8f-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Создание нового проекта" lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="34d8f-131">Создание нового проекта</span><span class="sxs-lookup"><span data-stu-id="34d8f-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34d8f-132">Введите **имя**проекта, сохраните его в нужном **месте**и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="34d8f-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Настройка нового проекта" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="34d8f-134">Настройка нового проекта</span><span class="sxs-lookup"><span data-stu-id="34d8f-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34d8f-135">Создается новый проект.</span><span class="sxs-lookup"><span data-stu-id="34d8f-135">A new project is created.</span></span>  <span data-ttu-id="34d8f-136">В этом руководстве весь код пишется в `Program.cs` файл.</span><span class="sxs-lookup"><span data-stu-id="34d8f-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Новый проект" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="34d8f-138">Новый проект</span><span class="sxs-lookup"><span data-stu-id="34d8f-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34d8f-139">Теперь добавьте **Selenium** в проект.</span><span class="sxs-lookup"><span data-stu-id="34d8f-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="34d8f-140">Установите Selenium с помощью **пакета NuGet для Selenium.**</span><span class="sxs-lookup"><span data-stu-id="34d8f-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="34d8f-141">Чтобы скачать **пакет NuGet для Selenium...** в **Visual Studio**, наведите указатель мыши на элемент **Project**и выберите пункт **Управление пакетом NuGet**.</span><span class="sxs-lookup"><span data-stu-id="34d8f-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="34d8f-142">Появится следующий экран.</span><span class="sxs-lookup"><span data-stu-id="34d8f-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Скачать пакет NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="34d8f-144">Скачать пакет NuGet</span><span class="sxs-lookup"><span data-stu-id="34d8f-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34d8f-145">Введите `Selenium.WebDriver` значение в строке поиска, выберите **Selenium. стример** из результатов и убедитесь в том, что флажок **включить предварительный выпуск установлен**флажком.</span><span class="sxs-lookup"><span data-stu-id="34d8f-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="34d8f-146">В правой части окна убедитесь, что для версии установлено значение **4.0.0-alpha04** или более поздняя **версия** , и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="34d8f-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="34d8f-147">NuGet загружает Selenium на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="34d8f-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="34d8f-148">Чтобы узнать больше о пакете NuGet для Selenium. [Selenium. 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="34d8f-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Управление пакетом NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="34d8f-150">Управление пакетом NuGet</span><span class="sxs-lookup"><span data-stu-id="34d8f-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="34d8f-151">`OpenQA.Selenium.Edge`Для использования добавьте следующую инструкцию: `using OpenQA.Selenium.Edge;` в начале `Program.cs` файла.</span><span class="sxs-lookup"><span data-stu-id="34d8f-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <span data-ttu-id="34d8f-152">Шаг 4: диск WebView2 с драйвером Selenium и Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34d8f-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="34d8f-153">Сначала создайте `EdgeOptions` объект, скопировав следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="34d8f-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="34d8f-154">`EdgeOptions`Объект принимает следующие два параметра.</span><span class="sxs-lookup"><span data-stu-id="34d8f-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="34d8f-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="34d8f-155">Parameter</span></span> | <span data-ttu-id="34d8f-156">Сведения</span><span class="sxs-lookup"><span data-stu-id="34d8f-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="34d8f-157">Параметр `false` , который сообщает Selenium, что вы управляете новым браузером Microsoft EDGE на основе Chromium.</span><span class="sxs-lookup"><span data-stu-id="34d8f-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="34d8f-158">Строка, указывающая Selenium, что вы управляете WebView2.</span><span class="sxs-lookup"><span data-stu-id="34d8f-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="34d8f-159">Затем укажите `edgeOptions.BinaryLocation` путь к файлу исполняющей среды проекта WebView2, создайте строку с именем `msedgedriverDir` , которая содержит путь к файлу, в который вы установили [драйвер Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], и создайте строку с именем `msedgedriverExe` для хранения имени среды выполнения драйвера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="34d8f-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="34d8f-160">По умолчанию используется имя среды выполнения `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="34d8f-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="34d8f-161">Используйте эти две строки для создания `EdgeDriverService` объекта, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="34d8f-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="34d8f-162">Наконец, создайте `EdgeDriver` объект с помощью `EdgeDriverService` и `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="34d8f-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="34d8f-163">Вы можете скопировать и вставить следующий код под ним `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="34d8f-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="34d8f-164">Убедитесь, что вы указали правильные пути к файлам для среды выполнения проекта и исполняющей среды на компьютере с драйвером Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="34d8f-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
    ```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    
    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";
    
    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";
    
    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);
    
    EdgeDriver e = new EdgeDriver(service, edgeOptions);
    ```
    
3.  <span data-ttu-id="34d8f-165">Теперь `EdgeDriver` Настройка WebView2 в проекте.</span><span class="sxs-lookup"><span data-stu-id="34d8f-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="34d8f-166">Например, если вы используете **образец WebView2API**, вы можете перейти `https://microsoft.com` , выполнив `e.Url = @"https://www.microsoft.com";` команду.</span><span class="sxs-lookup"><span data-stu-id="34d8f-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="34d8f-167">Проверьте Selenium диск WebView2, задав точку останова в строке и запуская проект.</span><span class="sxs-lookup"><span data-stu-id="34d8f-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium с WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="34d8f-169">Selenium с WebView2</span><span class="sxs-lookup"><span data-stu-id="34d8f-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="34d8f-170">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="34d8f-170">Congratulations.</span></span>  <span data-ttu-id="34d8f-171">Вы успешно автоматизируи проект WebView2 и управляемый WebView2 с помощью драйвера Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="34d8f-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <span data-ttu-id="34d8f-172">См. также</span><span class="sxs-lookup"><span data-stu-id="34d8f-172">See also</span></span>  

*   <span data-ttu-id="34d8f-173">Подробные сведения о том, как API Selenium диски WebView2 или Microsoft Edge \ (Chromium \), переходить к веб- [диску в Selenium документации][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="34d8f-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="34d8f-174">Дополнительные сведения об элементе управления WebView2 и его использовании при внедрении веб-содержимого в собственное приложение можно найти в [статье Знакомство с Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="34d8f-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="34d8f-175">Дополнительные сведения об автоматизации Microsoft Edge \ (Chromium \) можно найти в статье [Использование веб-накопителя (Chromium) для автоматизации тестов][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="34d8f-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <span data-ttu-id="34d8f-176">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="34d8f-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Использование Chromium для проверки автоматизации тестов Документы Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Скачать драйвер Microsoft Edge — использование веб-накопителя (Chromium) для автоматизации тестов | Документы Microsoft"  
[WebViewIndex]: ../index.md "Введение в Microsoft Edge WebView2-документы Майкрософт"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачать "|" Разработчик Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Образец API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Предварительные требования — пример API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium. 4.0.0-alpha04 | Коллекция NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "[Стример] | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "[Стример] | PNG"  
