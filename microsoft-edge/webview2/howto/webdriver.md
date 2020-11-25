---
description: Автоматизация и тестирование элемента управления WebView2 с помощью драйвера Microsoft Edge
title: Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, EDGE, ICoreWebView2, ICoreWebView2Controller, Selenium, драйвер Microsoft Edge
ms.openlocfilehash: 6f7f84fa88a57e54d7b5143a489d1138c7426d88
ms.sourcegitcommit: 652c345b46aae8b7e3723eb55a01b71a4ef76bf0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191452"
---
# Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge  

Так как WebView2 использует веб-платформу Microsoft Edge \ (Chromium \), WebView2 разработчиков \ (ты \) может воспользоваться стандартными веб-возможностями для отладки и автоматизации.  Selenium — это одно из таких средств.  Он реализует API-интерфейс для интерфейса- [дисковода][W3cWebdriver2] W3C.  Вы можете использовать Selenium для создания автоматических тестов для моделирования взаимодействия с пользователем.  

Чтобы начать работу, выполните указанные ниже действия.  

## Шаг 1: Загрузка образца WebView2API  

Если у вас нет проекта WebView2, скачайте [пример приложения WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], полный пример НОВЕЙШЕГО пакета SDK для WebView2.  Убедитесь, что вы удовлетворены [требованиями для примера приложения WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]. 

Создав точную копию репозитория, создайте проект в Visual Studio.  Оно должно выглядеть так, как показано на рисунке ниже.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Пример приложения WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Пример приложения WebView2API  
:::image-end:::  

## Шаг 2: Установка драйвера Microsoft Edge  

Следуйте инструкциям, чтобы установить [драйвер Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] , необходимый для автоматизации и тестирования WebView2, который требуется драйверу Selenium для веб-браузера.  

Убедитесь, что версия драйвера Microsoft Edge совпадает с версией среды выполнения WebView2, используемой Вашим приложением.  Чтобы WebView2API пример работал, убедитесь в том, что ваша версия среды выполнения WebView2 больше или равна поддерживаемой версии новейшего выпуска SDK для WebView2.  Чтобы найти последнюю версию SDK для WebView2, перейдите к [WebView2 заметкам о выпуске][Webview2Releasenotes].  Чтобы узнать, какая у вас версия среды выполнения WebView2 в настоящее время, перейдите на `edge://settings/help` .  

## Шаг 3: Добавление Selenium в пример WebView2API  

На этом этапе необходимо установить среду выполнения WebView2, создать WebView2 проект и установить драйвер Microsoft Edge.  Теперь приступите к работе с Selenium.  

> [!NOTE]
> Selenium поддерживает C \ #, Java, Python, JavaScript и Ruby.  Однако приведенное ниже руководство написано с использованием C \ #.  

1.  Начните с создания нового проекта **C# .NET Framework** в **Visual Studio**.  Чтобы продолжить, нажмите кнопку **Далее** в правом нижнем углу.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Создание нового проекта" lightbox="../media/webdriver/new-project.png":::
       Создание нового проекта  
    :::image-end:::  
    
1.  Введите **имя**проекта, сохраните его в нужном **месте**и нажмите кнопку **создать**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Настройка нового проекта" lightbox="../media/webdriver/app-create.png":::
       Настройка нового проекта  
    :::image-end:::  
    
1.  Создается новый проект.  В этом руководстве весь код пишется в `Program.cs` файл.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Новый проект" lightbox="../media/webdriver/start-app.png":::
       Новый проект  
    :::image-end:::  
    
1.  Теперь добавьте **Selenium** в проект.  Установите Selenium с помощью **пакета NuGet для Selenium.**  
    
    Чтобы скачать **пакет NuGet для Selenium...** в **Visual Studio**, наведите указатель мыши на элемент **Project**и выберите пункт **Управление пакетом NuGet**.  Появится следующий экран.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Скачать пакет NuGet" lightbox="../media/webdriver/download-nuget.png":::
       Скачать пакет NuGet  
    :::image-end:::  
    
1.  Введите **Selenium.** Selenium на панели поиска, выберите **. стример** из результатов, а затем установите флажок **включить предварительную версию**. В правой части окна убедитесь, что для версии установлено значение **4.0.0-alpha04** или более поздняя **версия** , и нажмите кнопку **установить**.  NuGet загружает Selenium на ваш компьютер.  
    
    Чтобы узнать больше о пакете NuGet для Selenium. [Selenium. 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Управление пакетом NuGet" lightbox="../media/webdriver/nuget.png":::
       Управление пакетом NuGet  
    :::image-end:::  
    
1.  `OpenQA.Selenium.Edge`Для использования добавьте следующую инструкцию: `using OpenQA.Selenium.Edge;` в начале `Program.cs` файла.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## Шаг 4: диск WebView2 с драйвером Selenium и Microsoft Edge  

1.  Сначала создайте `EdgeOptions` объект, скопировав следующий фрагмент кода.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    `EdgeOptions`Объект принимает следующие два параметра.  
    
    | Параметр | Сведения |    
    |:--- |:--- |  
    | `is_legacy` | Параметр `false` , который сообщает Selenium, что вы управляете новым браузером Microsoft EDGE на основе Chromium. |  
    | `"webview2"` | Строка, указывающая Selenium, что вы управляете WebView2. |  
    
1.  Затем укажите `edgeOptions.BinaryLocation` путь к файлу исполняющей среды проекта WebView2, создайте строку с именем `msedgedriverDir` , которая содержит путь к файлу, в который вы установили [драйвер Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], и создайте строку с именем `msedgedriverExe` для хранения имени среды выполнения драйвера Microsoft Edge.  По умолчанию используется имя среды выполнения `msedgedriver.exe` . Используйте эти две строки для создания `EdgeDriverService` объекта, как показано ниже.  Наконец, создайте `EdgeDriver` объект с помощью `EdgeDriverService` и `EdgeOptions` .  
    
    Вы можете скопировать и вставить следующий код под ним `edgeOptions` .  Убедитесь, что вы указали правильные пути к файлам для среды выполнения проекта и исполняющей среды на компьютере с драйвером Microsoft Edge.  
    
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
    
3.  Теперь `EdgeDriver` Настройка WebView2 в проекте.  Например, если вы используете **образец WebView2API**, вы можете перейти `https://microsoft.com` , выполнив `e.Url = @"https://www.microsoft.com";` команду.  Проверьте Selenium диск WebView2, задав точку останова в строке и запуская проект.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium с WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenium с WebView2  
    :::image-end:::

Поздравляем!  Вы успешно автоматизируи проект WebView2 и управляемый WebView2 с помощью драйвера Selenium и Microsoft Edge.  

## См. также  

*   Подробные сведения о том, как API Selenium диски WebView2 или Microsoft Edge \ (Chromium \), переходить к веб- [диску в Selenium документации][SeleniumWebdriver]   
*   Дополнительные сведения об элементе управления WebView2 и его использовании при внедрении веб-содержимого в собственное приложение можно найти в [статье Знакомство с Microsoft Edge WebView2][WebViewIndex].  
*   Дополнительные сведения об автоматизации Microsoft Edge \ (Chromium \) можно найти в статье [Использование веб-накопителя (Chromium) для автоматизации тестов][WebdriverChromium]   
    
## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium.md "Использование Chromium для проверки автоматизации тестов Документы Microsoft"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium.md#download-microsoft-edge-driver "Скачать драйвер Microsoft Edge — использование веб-накопителя (Chromium) для автоматизации тестов | Документы Microsoft"  
[WebViewIndex]: ../index.md "Введение в Microsoft Edge WebView2-документы Майкрософт"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачать "|" Разработчик Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Образец API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Предварительные требования — пример API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium. 4.0.0-alpha04 | Коллекция NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "[Стример] | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "[Стример] | PNG"  
