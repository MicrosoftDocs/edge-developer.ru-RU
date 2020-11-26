---
description: Сведения о том, как протестировать веб-сайт или приложение в Microsoft EDGE, а также автоматизировать браузер с помощью Web Drive.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, HTML, CSS, сценарий JavaScript, разработчик, веб-дисковод, Selenium, тестирование, инструменты, Автоматизация и тестирование
ms.openlocfilehash: 3c197a83dbf16c68102ff6e9a4ee6f33b0573af2
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192259"
---
# <span data-ttu-id="5bd9b-104">Использование Chromium для автоматизации тестов</span><span class="sxs-lookup"><span data-stu-id="5bd9b-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="5bd9b-105">С помощью этого устройства вы можете (разработчикам) создавать автоматические тесты, имитирующие взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-105">WebDriver enables you \(developers\) to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="5bd9b-106">Проверки и имитации для модулей-накопителей отличаются от модульных тестов JavaScript по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span>  

*   <span data-ttu-id="5bd9b-107">Доступ к функциям и сведениям, недоступным для JavaScript, которые выполняются в браузерах.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="5bd9b-108">Более точное моделирование событий пользователей и событий на уровне операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="5bd9b-109">Управление несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="5bd9b-110">Запуск нескольких сеансов Microsoft EDGE на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="5bd9b-111">В следующем разделе описано, как приступить к работе с веб-диском Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="5bd9b-112">Установка Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="5bd9b-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="5bd9b-113">Убедитесь в том, что вы установили [Microsoft EDGE (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="5bd9b-114">Чтобы убедиться в том, что у вас установлен Microsoft Edge \ (Chromium \), найдите `edge://settings/help` и проверьте номер версии 75 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="5bd9b-115">Скачать драйвер Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5bd9b-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="5bd9b-116">Чтобы приступить к автоматизации тестов, выполните указанные ниже действия, чтобы убедиться, что версия веб – диска, установленная на вашем компьютере, совпадает с вашей версией браузера.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="5bd9b-117">Перейдите в раздел, чтобы `edge://settings/help` получить версию Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-version.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г." lightbox="../media/webdriver-chromium/edge-version.png":::
       <span data-ttu-id="5bd9b-119">Номер сборки Microsoft Edge Канарские 14 января 2020 г.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5bd9b-120">Перейдите на страницу [загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, соответствующий номеру версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-driver-install.png" alt-text="Раздел "загружаемые файлы" на странице драйвера Microsoft Edge" lightbox="../media/webdriver-chromium/edge-driver-install.png":::
       <span data-ttu-id="5bd9b-122">Раздел "загружаемые файлы" на странице [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="5bd9b-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>  
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="5bd9b-123">Дополнительные сведения об автоматизации тестирования с помощью Microsoft Edge \ (EdgeHTML \) можно найти в [веб-накопителе Microsoft для Microsoft EDGE (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-123">For more information about test automation using Microsoft Edge \(EdgeHTML\), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  
    
## <span data-ttu-id="5bd9b-124">Выбор языковой привязки для веб-дисков</span><span class="sxs-lookup"><span data-stu-id="5bd9b-124">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="5bd9b-125">Последний компонент, который необходимо скачать, — это языковый драйвер клиента для перевода кода \ (Python, Java, C \ #, Ruby, JavaScript \) в команды, которые драйвер Microsoft EDGE работает в Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-125">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="5bd9b-126">[Скачайте выбранную вами языковую привязку веб дисков][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-126">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="5bd9b-127">Команда Microsoft Edge рекомендует [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она поддерживает Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-127">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="5bd9b-128">Тем не менее, вы можете управлять Microsoft Edge \ (Chromium \) во всех более ранних версиях Selenium, включая текущую стабильную версию Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-128">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="5bd9b-129">Если вы уже выполняли автоматизацию или тестирование Microsoft Edge \ (Chromium \) с использованием `ChromeDriver` и `ChromeOptions` классами, код веб-дисковода не будет работать в Microsoft Edge версии 80 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-129">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="5bd9b-130">Чтобы устранить эту проблему, обновите тесты, чтобы использовать этот `EdgeOptions` класс и установить [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-130">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="5bd9b-131">Использование Selenium 3</span><span class="sxs-lookup"><span data-stu-id="5bd9b-131">Use Selenium 3</span></span>  

<span data-ttu-id="5bd9b-132">Если вы уже используете [Selenium 3][|::ref1::|], возможно, у вас есть тестирование браузера и хотите добавить покрытие для Microsoft Edge \ (Chromium \) без изменения версии Selenium.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-132">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="5bd9b-133">Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов как для Microsoft Edge \ (EdgeHTML \), так и для Microsoft Edge \ (Chromium \), установите для него пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , чтобы использовать обновленный драйвер.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-133">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="5bd9b-134">`EdgeDriver`Классы и `EdgeDriverService` компоненты, включенные в эти инструменты, полностью совместимы с встроенными эквивалентами в Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-134">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="5bd9b-135">Чтобы добавить в проект [инструменты Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-135">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="5bd9b-136">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-136">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="5bd9b-137">Добавьте пакеты [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.][NugetPackagesSeleniumWebdriver31410] Package в проект .NET с помощью [инфраструктуры NuGet][NugetCLI] или [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-137">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="5bd9b-138">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-138">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="5bd9b-139">Чтобы установить пакеты [msedge-Selenium-Tools][PythonSeleniumTools] и [Selenium][PythonSelenium] , воспользуйтесь [PIP][PythonPip] .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-139">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="5bd9b-140">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-140">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="5bd9b-141">Используйте [NPM][JavaScript|::ref4::|] для установки пакетов [Edge-Selenium-Tools][JavaScriptSeleniumTools] и [Selenium-Drives][JavaScriptSelenium] .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-141">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="5bd9b-142">Использование веб-накопителя (Microsoft EDGE (Chromium))</span><span class="sxs-lookup"><span data-stu-id="5bd9b-142">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="5bd9b-143">Вы можете использовать следующие примеры с помощью Selenium 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-143">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="5bd9b-144">Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-144">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="5bd9b-145">Основное использование</span><span class="sxs-lookup"><span data-stu-id="5bd9b-145">Basic Usage</span></span>  

<span data-ttu-id="5bd9b-146">Для использования с Microsoft Edge \ (EdgeHTML \) создайте экземпляр класса по умолчанию `EdgeDriver` .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-146">To use with Microsoft Edge \(EdgeHTML\), create a default instance of the `EdgeDriver` class.</span></span>  

#### [<span data-ttu-id="5bd9b-147">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-147">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="5bd9b-148">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-148">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="5bd9b-149">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-149">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="5bd9b-150">Управление Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="5bd9b-150">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="5bd9b-151">Для использования с Microsoft Edge \ (Chromium \) создайте новый `EdgeDriver` класс и передайте ему `EdgeOptions` объект со `UseChromium` свойством, для которого задано значение `true` .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-151">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="5bd9b-152">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-152">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="5bd9b-153">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-153">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="5bd9b-154">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-154">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="5bd9b-155">Если у ИТ-администратора задана политика [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] `2` , [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] не сможет установить Microsoft Edge [(Chromium)][MicrosoftEdge] , так как в драйвере используется [Microsoft Edge DevTools][DevToolsMain].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-155">If your IT admin has set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="5bd9b-156">Убедитесь в том, что для политики [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] задано значение " `0` или" `1` автоматизировать [Microsoft EDGE (Chromium)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-156">Ensure the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="5bd9b-157">Выбор определенных двоичных файлов браузера (только Chromium)</span><span class="sxs-lookup"><span data-stu-id="5bd9b-157">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="5bd9b-158">Вы можете использовать этот `EdgeOptions` класс с определенными двоичными файлами Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-158">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="5bd9b-159">Например, вы можете выполнять тесты с помощью [каналов предварительной версии Microsoft Edge][MicrosoftedgeinsiderDownload] , таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-159">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="5bd9b-160">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-160">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="5bd9b-161">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-161">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="5bd9b-162">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-162">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="5bd9b-163">Настройка службы драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5bd9b-163">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="5bd9b-164">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-164">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="5bd9b-165">Когда `EdgeDriver` экземпляр класса создается с помощью `EdgeOptions` класса, он создает и запускает соответствующий `EdgeDriverService` класс для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-165">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="5bd9b-166">Если вы хотите создать объект `EdgeDriverService` для Microsoft Edge \ (Chromium \) с помощью метода, создайте его `CreateChromiumService()` .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-166">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="5bd9b-167">Вы можете использовать дополнительные настройки, такие как включение подробного вывода журнала в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-167">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="5bd9b-168">Вам не нужно предоставлять `EdgeOptions` объект при передаче `EdgeDriverService` `EdgeDriver` экземпляру.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-168">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="5bd9b-169">`EdgeDriver`Класс использует параметры по умолчанию для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \) в зависимости от предоставленной услуги.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-169">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="5bd9b-170">Тем не менее, если вы хотите предоставить `EdgeDriverService` оба `EdgeOptions` класса и классы, убедитесь, что они настроены для одной и той же версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-170">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="5bd9b-171">Например, невозможно использовать класс по умолчанию Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` и свойства Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-171">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="5bd9b-172">`EdgeDriver`Класс вызывает ошибку, чтобы предотвратить использование разных версий.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-172">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="5bd9b-173">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-173">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="5bd9b-174">При использовании Python `Edge` объект создает и управляет `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="5bd9b-174">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="5bd9b-175">Чтобы настроить `EdgeService` , передайте дополнительные аргументы объекту, `Edge` как указано в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-175">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="5bd9b-176">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-176">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="5bd9b-177">При использовании JavaScript создайте и настройте `Service` класс с помощью `ServiceBuilder` класса.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-177">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="5bd9b-178">При необходимости вы можете передать `Service` объект `Driver` объекту, который будет заключаться в службу (и остановить ее).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-178">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="5bd9b-179">Чтобы настроить `Service` , выполните дополнительные методы в `ServiceBuilder` классе перед использованием `build()` метода.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-179">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="5bd9b-180">Затем передается в `service` `Driver.createSession()` методе как параметр.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-180">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="5bd9b-181">Использование Chromium-Specific параметров</span><span class="sxs-lookup"><span data-stu-id="5bd9b-181">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="5bd9b-182">Если вы задаете `UseChromium` свойство `true` , вы можете использовать `EdgeOptions` Этот класс для доступа к таким же [свойствам и методам Chromium][SeleniumWebDriverChromeoptionsClass] , что и при автоматизации других браузеров Chromium.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-182">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="5bd9b-183">C#</span><span class="sxs-lookup"><span data-stu-id="5bd9b-183">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="5bd9b-184">Языке</span><span class="sxs-lookup"><span data-stu-id="5bd9b-184">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="5bd9b-185">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5bd9b-185">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> <span data-ttu-id="5bd9b-186">Если `UseChromium` свойство имеет значение `true` , вы не можете пользоваться свойствами и методами для Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="5bd9b-186">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="5bd9b-187">Дополнительные параметры установки для устройства добавления новых устройств</span><span class="sxs-lookup"><span data-stu-id="5bd9b-187">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="5bd9b-188">Шоколад</span><span class="sxs-lookup"><span data-stu-id="5bd9b-188">Chocolatey</span></span>  

<span data-ttu-id="5bd9b-189">Если вы используете [шоколад][Chocolatey] в качестве диспетчера пакетов, установите драйвер Microsoft EDGE, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5bd9b-189">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="5bd9b-190">Дополнительные сведения можно найти [в разделе драйвер Selenium Chromium EDGE на шоколаде][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-190">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="5bd9b-191">Docker</span><span class="sxs-lookup"><span data-stu-id="5bd9b-191">Docker</span></span>  

<span data-ttu-id="5bd9b-192">Если вы используете [закрепление][DockerHub], скачайте предварительно настроенное изображение с помощью Microsoft Edge \ (Chromium \) и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] , которое предустановлено, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5bd9b-192">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="5bd9b-193">Дополнительные сведения можно найти [в разделе контейнер в центре Dock][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-193">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="5bd9b-194">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5bd9b-194">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="5bd9b-195">Группа Microsoft Edge – это информация о том, как использовать веб – диски, Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5bd9b-195">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="5bd9b-196">Чтобы сообщить команде о том, что вы думаете, щелкните значок **Отправить отзыв** в Microsoft Edge DevTools или отправьте твит [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="5bd9b-196">To let the team know what you think, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="5bd9b-198">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5bd9b-198">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"
[Webdriver]: ../webdriver.md "[EdgeHTML) | Документы Microsoft"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Документы Microsoft"  

[Chocolatey]: https://chocolatey.org "Шоколад | Шоколадное программное обеспечение"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Драйвер Selenium Chromium Edge | Шоколад"  

[DockerHub]: https://hub.docker.com "Закрепляемый центр"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Закрепляемый центр"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selenium-стример | NPM"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "[Стример] | Разработчик Майкрософт"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Загружаемые файлы — "[стример" | Разработчик Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Коллекция NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. 3.141.0 | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. 4.0.0-alpha05 | Коллекция NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "точка | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-Tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "Selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загрузки | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Класс ChromeOptions-стример | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "[Стример] | PNG"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
