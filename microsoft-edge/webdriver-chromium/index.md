---
description: Узнайте, как протестировать веб-сайт или приложение в Microsoft Edge или автоматизировать браузер с помощью WebDriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, html, css, javascript, разработчик, webdriver, selenium, тестирование, средства, автоматизация, тест
ms.openlocfilehash: 5e881eec59c966fd4fa6d35118032a3a51e7b9e5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231137"
---
# <span data-ttu-id="7a565-104">Обзор тестовой автоматизации с помощью WebDriver (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7a565-104">Use WebDriver (Chromium) for test automation overview</span></span>  

<span data-ttu-id="7a565-105">WebDriver позволяет создавать автоматические тесты, имитирующие взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7a565-105">WebDriver enables you \(developers\) to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="7a565-106">Тесты и имитации WebDriver отличаются от тестов javaScript по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="7a565-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span>  

*   <span data-ttu-id="7a565-107">Доступ к функциям и сведениям, недоступным для JavaScript, запущенного в браузерах.</span><span class="sxs-lookup"><span data-stu-id="7a565-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="7a565-108">Имитирует события пользователя или события на уровне ОС более точно.</span><span class="sxs-lookup"><span data-stu-id="7a565-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="7a565-109">Управляет несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="7a565-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="7a565-110">Запускает несколько сеансов Microsoft Edge на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7a565-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="7a565-111">В следующем разделе описывается, как начать работу с WebDriver для Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7a565-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="7a565-112">Установка Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7a565-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="7a565-113">Убедитесь, что [вы установили Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="7a565-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="7a565-114">Чтобы убедиться, что у вас установлен Microsoft Edge \(Chromium\), перейдите к и убедитесь, что номер версии `edge://settings/help` 75 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7a565-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="7a565-115">Скачивание драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7a565-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="7a565-116">Чтобы начать автоматизацию тестов, с помощью следующих действий убедитесь, что устанавливаемая версия WebDriver соответствует версии браузера.</span><span class="sxs-lookup"><span data-stu-id="7a565-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="7a565-117">Перейдите `edge://settings/help` к версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a565-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Номер сборки для Microsoft Edge Canary 14 января 2020 г.":::
       <span data-ttu-id="7a565-119">Номер сборки для Microsoft Edge Canary 14 января 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7a565-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="7a565-120">Перейдите на [страницу загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, который соответствует номеру версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a565-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Раздел "Загрузки" страницы "Драйвер Microsoft Edge"":::
       <span data-ttu-id="7a565-122">Раздел "Загрузки" на странице ["Драйвер Microsoft Edge"][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="7a565-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## <span data-ttu-id="7a565-123">Выбор привязки языка WebDriver</span><span class="sxs-lookup"><span data-stu-id="7a565-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="7a565-124">Последний компонент, который необходимо скачать, — это специальный драйвер клиента для перевода кода \(Python, Java, C\#, Ruby, JavaScript\) в команды, которые выполняет драйвер Microsoft Edge в Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7a565-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="7a565-125">[Скачайте языковую привязку WebDriver по вашему выбору.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="7a565-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="7a565-126">Команда Microsoft Edge рекомендует [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она поддерживает Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7a565-126">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7a565-127">Однако вы можете управлять Microsoft Edge \(Chromium\) во всех старых версиях Selenium, включая текущий стабильный выпуск Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="7a565-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="7a565-128">Если вы ранее автоматизировали или тестируете Microsoft Edge \(Chromium\) с использованием и классами, код WebDriver не будет работать в Microsoft Edge версии 80 или более `ChromeDriver` `ChromeOptions` поздней.</span><span class="sxs-lookup"><span data-stu-id="7a565-128">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="7a565-129">Чтобы решить эту проблему, обновите тесты, чтобы использовать `EdgeOptions` класс, и установите [драйвер Microsoft Edge.][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="7a565-129">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="7a565-130">Использование Selenium 3</span><span class="sxs-lookup"><span data-stu-id="7a565-130">Use Selenium 3</span></span>  

<span data-ttu-id="7a565-131">Если вы уже используете [Selenium 3,][|::ref1::|]возможно, у вас уже есть тесты браузера и вы захотите добавить покрытия для Microsoft Edge \(Chromium\) без изменения версии Selenium.</span><span class="sxs-lookup"><span data-stu-id="7a565-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="7a565-132">Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов для Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\), установите пакет [средств Selenium для Microsoft Edge,][GithubMicrosoftEdgeSeleniumTools] чтобы использовать обновленный драйвер.</span><span class="sxs-lookup"><span data-stu-id="7a565-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="7a565-133">Классы, включенные в инструменты, полностью совместимы со встроенными эквивалентами `EdgeDriver` `EdgeDriverService` в Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="7a565-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="7a565-134">Чтобы добавить средства [Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] в проект, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="7a565-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="7a565-135">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="7a565-136">Добавьте [пакеты Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] в проект .NET с помощью [nuGet CLI][NugetCLI] [или Visual Studio.][VisualStudio]</span><span class="sxs-lookup"><span data-stu-id="7a565-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="7a565-137">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="7a565-138">Используйте [конвейер][PythonPip] для установки [пакетов msedge-selenium-tools][PythonSeleniumTools] и [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="7a565-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="7a565-139">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-139">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="7a565-140">Используйте [npm][JavaScript|::ref4::|] для установки [пакетов edge-selenium-tools][JavaScriptSeleniumTools] и [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="7a565-140">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="7a565-141">Использование Microsoft Edge (Chromium) с WebDriver</span><span class="sxs-lookup"><span data-stu-id="7a565-141">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="7a565-142">Можно выполнить следующие примеры с помощью Selenium 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="7a565-142">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="7a565-143">Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]</span><span class="sxs-lookup"><span data-stu-id="7a565-143">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="7a565-144">Базовое использование</span><span class="sxs-lookup"><span data-stu-id="7a565-144">Basic Usage</span></span>  

<span data-ttu-id="7a565-145">Для использования с Microsoft Edge \(EdgeHTML\) создайте экземпляр класса по `EdgeDriver` умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a565-145">To use with Microsoft Edge \(EdgeHTML\), create a default instance of the `EdgeDriver` class.</span></span>  

#### [<span data-ttu-id="7a565-146">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-146">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="7a565-147">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-147">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="7a565-148">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-148">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="7a565-149">Driving Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="7a565-149">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="7a565-150">Чтобы использовать с Microsoft Edge \(Chromium\), создайте новый класс и передайте ему объект со `EdgeDriver` `EdgeOptions` `UseChromium` свойством, задав для него свойство `true` .</span><span class="sxs-lookup"><span data-stu-id="7a565-150">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="7a565-151">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-151">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="7a565-152">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-152">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="7a565-153">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-153">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="7a565-154">Если ваш ИТ-администратор настроил политику [DeveloperToolsAvailability,][DeployedgePoliciesDevelopertoolsavailability] драйвер Microsoft Edge не сможет управлять `2` Microsoft Edge [(Chromium),][MicrosoftEdge] так как драйвер использует [Microsoft Edge DevTools.][DevToolsMain] [][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="7a565-154">If your IT admin has set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="7a565-155">[Убедитесь, что для политики DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] установлено или для автоматизации Microsoft Edge `0` `1` [(Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="7a565-155">Ensure the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="7a565-156">Выбор определенных binaries браузера (только для Chromium)</span><span class="sxs-lookup"><span data-stu-id="7a565-156">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="7a565-157">Вы можете использовать класс `EdgeOptions` с определенными binaries of Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7a565-157">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="7a565-158">Например, можно выполнить тесты с помощью каналов предварительного просмотра [Microsoft Edge,][MicrosoftedgeinsiderDownload] таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="7a565-158">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="7a565-159">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-159">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="7a565-160">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-160">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="7a565-161">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-161">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="7a565-162">Настройка службы драйверов Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7a565-162">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="7a565-163">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-163">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="7a565-164">Когда экземпляр класса создается с помощью класса, он создает и запускает соответствующий класс для `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) или Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="7a565-164">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="7a565-165">Если вы хотите создать , создайте его, настроенный для `EdgeDriverService` Microsoft Edge \(Chromium\) с помощью `CreateChromiumService()` этого метода.</span><span class="sxs-lookup"><span data-stu-id="7a565-165">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="7a565-166">Это может оказаться полезным для дополнительных настроек, таких как включение подробного вывода журнала в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7a565-166">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="7a565-167">При передаче в экземпляр не требуется предоставлять `EdgeOptions` `EdgeDriverService` `EdgeDriver` объект.</span><span class="sxs-lookup"><span data-stu-id="7a565-167">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="7a565-168">В классе используются параметры по умолчанию для `EdgeDriver` Microsoft Edge \(EdgeHTML\) или Microsoft Edge \(Chromium\) в зависимости от предоставляемой службы.</span><span class="sxs-lookup"><span data-stu-id="7a565-168">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="7a565-169">Тем не менее, если вы хотите предоставить и классы, убедитесь, что оба настроены для одной и той же `EdgeDriverService` `EdgeOptions` версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a565-169">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="7a565-170">Например, невозможно использовать класс Microsoft Edge по умолчанию \(EdgeHTML\) и свойства `EdgeDriverService` Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="7a565-170">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="7a565-171">Класс `EdgeDriver` высылает ошибку, чтобы запретить использование различных версий.</span><span class="sxs-lookup"><span data-stu-id="7a565-171">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="7a565-172">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-172">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="7a565-173">При использовании Python `Edge` объект создает объект и управляет `EdgeService` им.</span><span class="sxs-lookup"><span data-stu-id="7a565-173">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="7a565-174">Чтобы настроить , `EdgeService` передав дополнительные аргументы `Edge` объекту, как указано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="7a565-174">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="7a565-175">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-175">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="7a565-176">При использовании JavaScript создайте и настройте a `Service` с `ServiceBuilder` классом.</span><span class="sxs-lookup"><span data-stu-id="7a565-176">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="7a565-177">При желании вы можете передать объект объекту, который запускает `Service` `Driver` \(и останавливает\) службу.</span><span class="sxs-lookup"><span data-stu-id="7a565-177">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="7a565-178">Чтобы настроить метод, перед использованием этого метода запустите дополнительные методы `Service` `ServiceBuilder` в `build()` классе.</span><span class="sxs-lookup"><span data-stu-id="7a565-178">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="7a565-179">Затем `service` передав его в качестве параметра в `Driver.createSession()` методе.</span><span class="sxs-lookup"><span data-stu-id="7a565-179">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="7a565-180">Использование Chromium-Specific параметров</span><span class="sxs-lookup"><span data-stu-id="7a565-180">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="7a565-181">Если вы установите для свойства такое же свойство, вы можете использовать класс для доступа к тем же свойствам и методам, что и при автоматизации других браузеров `UseChromium` `true` `EdgeOptions` Chromium. [][SeleniumWebDriverChromeoptionsClass]</span><span class="sxs-lookup"><span data-stu-id="7a565-181">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="7a565-182">C#</span><span class="sxs-lookup"><span data-stu-id="7a565-182">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="7a565-183">Python</span><span class="sxs-lookup"><span data-stu-id="7a565-183">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="7a565-184">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7a565-184">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  

> [!NOTE]
> <span data-ttu-id="7a565-185">Если для свойства установлено свойство, вы не сможете использовать свойства и методы для `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="7a565-185">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="7a565-186">Дополнительные параметры установки WebDriver</span><span class="sxs-lookup"><span data-stu-id="7a565-186">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="7a565-187">Хомякий</span><span class="sxs-lookup"><span data-stu-id="7a565-187">Chocolatey</span></span>  

<span data-ttu-id="7a565-188">Если вы используете в качестве диспетчера пакетов 10000000000, установите драйвер Microsoft Edge с помощью следующей команды. [][Chocolatey]</span><span class="sxs-lookup"><span data-stu-id="7a565-188">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="7a565-189">Дополнительные сведения см. в теме ["Selenium Chromium Edge Driver onChromy".][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="7a565-189">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="7a565-190">Docker</span><span class="sxs-lookup"><span data-stu-id="7a565-190">Docker</span></span>  

<span data-ttu-id="7a565-191">Если вы используете [Docker,][DockerHub]скачайте предварительно настроенный образ с помощью Microsoft Edge \(Chromium\) и предварительно установленного [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="7a565-191">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="7a565-192">Дополнительные сведения см. [в контейнере Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="7a565-192">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="7a565-193">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7a565-193">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="7a565-194">Команда Microsoft Edge с нетерпением услышит ваши отзывы об использовании WebDriver, Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7a565-194">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="7a565-195">Чтобы дать команде знать, что \*\*\*\* вы думаете, выберите значок отправки отзыва в Microsoft Edge DevTools или отправьте [твит][TwitterTweetEdgeDevTools]@EdgeDevTools.</span><span class="sxs-lookup"><span data-stu-id="7a565-195">To let the team know what you think, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="7a565-197">Значок **отправки отзыва** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7a565-197">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevToolsMain]: ../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"
[Webdriver]: ../webdriver/index.md "WebDriver (EdgeHTML) | Документы Майкрософт"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability — Microsoft Edge — политики | Документы Майкрософт"  

[Chocolatey]: https://chocolatey.org "Хлам | Программное обеспечение"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Хомякий"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Разработчик (Майкрософт)"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Загрузки — WebDriver | Разработчик (Майкрософт)"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Загрузка нового браузера Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Галерея NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium.WebDriver 4.0.0-alpha05 | Галерея NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загрузки | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Класс ChromeOptions — WebDriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Браузер без headless | Википедия"  
