---
description: Узнайте, как протестировать веб-сайт или приложение в Microsoft Edge или автоматизировать браузер с помощью WebDriver.
title: Использование WebDriver (Chromium) для тестовой автоматизации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, html, css, javascript, разработчик, webdriver, selenium, тестирование, средства, автоматизация, тест
ms.openlocfilehash: 295985734d93c5912922be22c0af0c0e33e00a54
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306250"
---
# <span data-ttu-id="2bf53-104">Использование WebDriver (Chromium) для тестовой автоматизации</span><span class="sxs-lookup"><span data-stu-id="2bf53-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="2bf53-105">WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2bf53-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="2bf53-106">Тесты и имитации WebDriver отличаются от тестов javaScript, так как WebDriver:</span><span class="sxs-lookup"><span data-stu-id="2bf53-106">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver:</span></span>  

*   <span data-ttu-id="2bf53-107">Доступ к функциям и сведениям, недоступным для JavaScript, запущенного в браузерах.</span><span class="sxs-lookup"><span data-stu-id="2bf53-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="2bf53-108">Имитирует события пользователя или события на уровне ОС более точно.</span><span class="sxs-lookup"><span data-stu-id="2bf53-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="2bf53-109">Управляет несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="2bf53-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="2bf53-110">Запускает несколько сеансов Microsoft Edge на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2bf53-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="2bf53-111">В следующем разделе описывается, как начать работу с WebDriver для Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="2bf53-112">Установка Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="2bf53-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="2bf53-113">Убедитесь, что [вы установили Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="2bf53-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="2bf53-114">Чтобы убедиться, что у вас установлен Microsoft Edge \(Chromium\), перейдите к и убедитесь, что номер версии `edge://settings/help` 75 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="2bf53-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="2bf53-115">Скачивание драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bf53-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="2bf53-116">Чтобы начать автоматизацию тестов, с помощью следующих действий убедитесь, что устанавливаемая версия WebDriver соответствует версии браузера.</span><span class="sxs-lookup"><span data-stu-id="2bf53-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="2bf53-117">Перейдите `edge://settings/help` к версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bf53-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Номер сборки для Microsoft Edge Canary 14 января 2020 г.":::
       <span data-ttu-id="2bf53-119">Номер сборки для Microsoft Edge Canary 14 января 2020 г.</span><span class="sxs-lookup"><span data-stu-id="2bf53-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="2bf53-120">Перейдите на [страницу загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, который соответствует номеру версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bf53-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Раздел "Загрузки" страницы "Драйвер Microsoft Edge"":::
       <span data-ttu-id="2bf53-122">Раздел "Загрузки" страницы ["Драйвер Microsoft Edge"][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="2bf53-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## <span data-ttu-id="2bf53-123">Выбор привязки языка WebDriver</span><span class="sxs-lookup"><span data-stu-id="2bf53-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="2bf53-124">Последний компонент, который необходимо скачать, — это специальный драйвер клиента для перевода кода \(Python, Java, C\#, Ruby, JavaScript\) в команды, которые выполняет драйвер Microsoft Edge в Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="2bf53-125">[Скачайте языковую привязку WebDriver по вашему выбору.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="2bf53-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="2bf53-126">Команда Microsoft Edge рекомендует [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] или более поздней версии, так как она поддерживает Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="2bf53-127">Однако вы можете управлять Microsoft Edge \(Chromium\) во всех старых версиях Selenium, включая текущий стабильный выпуск Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="2bf53-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2bf53-128">Если вы ранее автоматизировали или тестируете Microsoft Edge \(Chromium\) с использованием и классами, код WebDriver не будет работать в Microsoft Edge версии 80 или более `ChromeDriver` `ChromeOptions` поздней.</span><span class="sxs-lookup"><span data-stu-id="2bf53-128">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="2bf53-129">Чтобы решить эту проблему, обновите тесты для использования класса и `EdgeOptions` скачайте [драйвер Microsoft Edge.][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="2bf53-129">To solve this problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="2bf53-130">Использование Selenium 3</span><span class="sxs-lookup"><span data-stu-id="2bf53-130">Use Selenium 3</span></span>  

<span data-ttu-id="2bf53-131">Если вы уже используете [Selenium 3,][|::ref1::|]возможно, у вас уже есть тесты браузера и вы захотите добавить покрытия для Microsoft Edge \(Chromium\) без изменения версии Selenium.</span><span class="sxs-lookup"><span data-stu-id="2bf53-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="2bf53-132">Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов для Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\), установите пакет [средств Selenium для Microsoft Edge,][GithubMicrosoftEdgeSeleniumTools] чтобы использовать обновленный драйвер.</span><span class="sxs-lookup"><span data-stu-id="2bf53-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="2bf53-133">Классы, включенные в инструменты, полностью совместимы со встроенными эквивалентами `EdgeDriver` `EdgeDriverService` в Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="2bf53-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="2bf53-134">Чтобы добавить средства [Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] в проект, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="2bf53-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="2bf53-135">C#</span><span class="sxs-lookup"><span data-stu-id="2bf53-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="2bf53-136">Добавьте [пакеты Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] в проект .NET с помощью [nuGet CLI][NugetCLI] [или Visual Studio.][VisualStudio]</span><span class="sxs-lookup"><span data-stu-id="2bf53-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="2bf53-137">Python</span><span class="sxs-lookup"><span data-stu-id="2bf53-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="2bf53-138">Используйте [конвейер][PythonPip] для установки [пакетов msedge-selenium-tools][PythonSeleniumTools] и [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="2bf53-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="2bf53-139">Java</span><span class="sxs-lookup"><span data-stu-id="2bf53-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="2bf53-140">Если в проекте Java используется Maven, добавьте [msedge-selenium-tools-java,][SonatypeMavenRepositorySearch] выполнив в файле следующую `pom.xml` зависимость:</span><span class="sxs-lookup"><span data-stu-id="2bf53-140">If your Java project uses Maven, add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] by coping the following dependency to your `pom.xml` file:</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="2bf53-141">Пакет Java также доступен для скачивания непосредственно на странице "Средства [Selenium для выпусков Microsoft Edge".][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="2bf53-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="2bf53-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2bf53-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="2bf53-143">Используйте [npm][JavaScript|::ref4::|] для установки [пакетов edge-selenium-tools][JavaScriptSeleniumTools] и [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="2bf53-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="2bf53-144">Автоматизация Microsoft Edge (Chromium) с помощью WebDriver</span><span class="sxs-lookup"><span data-stu-id="2bf53-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="2bf53-145">Чтобы автоматизировать браузер с помощью WebDriver, необходимо сначала запустить сеанс WebDriver с использованием предпочитаемой привязки языка WebDriver.</span><span class="sxs-lookup"><span data-stu-id="2bf53-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="2bf53-146">Сеанс — это один запущенный экземпляр браузера, который можно контролировать с помощью команд WebDriver.</span><span class="sxs-lookup"><span data-stu-id="2bf53-146">A session is a single running instance of a browser that can be controlled using WebDriver commands.</span></span>  <span data-ttu-id="2bf53-147">Запуск сеанса WebDriver запускает новый экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="2bf53-147">Starting a WebDriver session launches a new browser instance.</span></span>  <span data-ttu-id="2bf53-148">Браузер, который открывается, остается открытым до закрытия сеанса WebDriver.</span><span class="sxs-lookup"><span data-stu-id="2bf53-148">The browser that is launched remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="2bf53-149">Ниже приводится последующую информацию об использовании Selenium для запуска сеанса WebDriver с Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="2bf53-150">Эти примеры можно запустить с помощью Selenium 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="2bf53-150">You may run theses examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="2bf53-151">Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]</span><span class="sxs-lookup"><span data-stu-id="2bf53-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="2bf53-152">Автоматизация Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="2bf53-152">Automating Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="2bf53-153">Selenium использует `EdgeDriver` класс для управления сеансом Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span> <span data-ttu-id="2bf53-154">Чтобы запустить сеанс и автоматизировать Microsoft Edge \(Chromium\), создайте новый объект и передайте ему объект со `EdgeDriver` `EdgeOptions` свойством, `UseChromium` задав для него свойство `true` .</span><span class="sxs-lookup"><span data-stu-id="2bf53-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="2bf53-155">C#</span><span class="sxs-lookup"><span data-stu-id="2bf53-155">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="2bf53-156">Python</span><span class="sxs-lookup"><span data-stu-id="2bf53-156">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="2bf53-157">Java</span><span class="sxs-lookup"><span data-stu-id="2bf53-157">Java</span></span>](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="2bf53-158">Класс поддерживает только Microsoft Edge (Chromium) и не поддерживает `EdgeDriver` Microsoft Edge (EdgeHTML).</span><span class="sxs-lookup"><span data-stu-id="2bf53-158">The `EdgeDriver` class supports Microsoft Edge (Chromium) only, and does not support Microsoft Edge (EdgeHTML).</span></span> <span data-ttu-id="2bf53-159">Для базового использования можно создать элемент `EdgeDriver` без предоставления `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="2bf53-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="2bf53-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2bf53-160">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="2bf53-161">Если ваш ИТ-администратор настроил политику [DeveloperToolsAvailability,][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] драйвер Microsoft Edge не сможет управлять Microsoft Edge (Chromium), так как драйвер использует `2` Microsoft Edge [DevTools.][DevtoolsIndex] [][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="2bf53-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive Microsoft Edge (Chromium) because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="2bf53-162">[Убедитесь, что для политики DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] установлено или для автоматизации Microsoft Edge `0` `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="2bf53-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="2bf53-163">Выбор определенных binaries браузера (только для Chromium)</span><span class="sxs-lookup"><span data-stu-id="2bf53-163">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="2bf53-164">Вы можете начать сеанс WebDriver с определенными binaries \(Chromium\) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bf53-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="2bf53-165">Например, можно выполнить тесты с помощью каналов предварительного просмотра [Microsoft Edge,][MicrosoftedgeinsiderDownload] таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="2bf53-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="2bf53-166">C#</span><span class="sxs-lookup"><span data-stu-id="2bf53-166">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="2bf53-167">Python</span><span class="sxs-lookup"><span data-stu-id="2bf53-167">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="2bf53-168">Java</span><span class="sxs-lookup"><span data-stu-id="2bf53-168">Java</span></span>](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="2bf53-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2bf53-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="2bf53-170">Настройка службы драйверов Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bf53-170">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="2bf53-171">C#</span><span class="sxs-lookup"><span data-stu-id="2bf53-171">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="2bf53-172">Когда экземпляр класса создается с помощью класса, он создает и запускает соответствующий класс для `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) или Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-172">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="2bf53-173">Если вы хотите создать , создайте его, настроенный для `EdgeDriverService` Microsoft Edge \(Chromium\) с помощью `CreateChromiumService()` этого метода.</span><span class="sxs-lookup"><span data-stu-id="2bf53-173">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="2bf53-174">Это может оказаться полезным при необходимости добавления настроек.</span><span class="sxs-lookup"><span data-stu-id="2bf53-174">You may find it useful when you need to add customizations.</span></span> <span data-ttu-id="2bf53-175">Например, следующий код запускает подробные выходные данные журнала.</span><span class="sxs-lookup"><span data-stu-id="2bf53-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="2bf53-176">При передаче в экземпляр не требуется предоставлять `EdgeOptions` `EdgeDriverService` `EdgeDriver` объект.</span><span class="sxs-lookup"><span data-stu-id="2bf53-176">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="2bf53-177">Класс использует параметры по умолчанию для `EdgeDriver` Microsoft Edge \(EdgeHTML\) или Microsoft Edge \(Chromium\) на основе предоставляемой службы.</span><span class="sxs-lookup"><span data-stu-id="2bf53-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="2bf53-178">Тем не менее, если вы хотите предоставить и классы, убедитесь, что оба настроены для одной и той же `EdgeDriverService` `EdgeOptions` версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bf53-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="2bf53-179">Например, невозможно использовать класс Microsoft Edge по умолчанию \(EdgeHTML\) и свойства `EdgeDriverService` Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="2bf53-179">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="2bf53-180">Класс `EdgeDriver` высылает ошибку, чтобы запретить использование различных версий.</span><span class="sxs-lookup"><span data-stu-id="2bf53-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="2bf53-181">Python</span><span class="sxs-lookup"><span data-stu-id="2bf53-181">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="2bf53-182">При использовании Python объект создает объект и управляет `Edge` `EdgeService` им.</span><span class="sxs-lookup"><span data-stu-id="2bf53-182">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="2bf53-183">Чтобы настроить , `EdgeService` передав дополнительные аргументы `Edge` объекту, как указано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="2bf53-183">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="2bf53-184">Java</span><span class="sxs-lookup"><span data-stu-id="2bf53-184">Java</span></span>](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="2bf53-185">Используйте этот `createDefaultService()` метод для создания `EdgeDriverService` настроенного для Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="2bf53-186">Службы драйверов на Java настраиваются с помощью свойств системы Java.</span><span class="sxs-lookup"><span data-stu-id="2bf53-186">Driver services in Java are customized using Java system properties.</span></span> <span data-ttu-id="2bf53-187">Например, следующий код использует свойство для подробного вывода `"webdriver.edge.verboseLogging"` журнала.</span><span class="sxs-lookup"><span data-stu-id="2bf53-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to enable verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="2bf53-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2bf53-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="2bf53-189">При использовании JavaScript создайте и настройте a `Service` с `ServiceBuilder` классом.</span><span class="sxs-lookup"><span data-stu-id="2bf53-189">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="2bf53-190">При желании вы можете передать объект объекту, который запускает `Service` `Driver` \(и останавливает\) службу за вас.</span><span class="sxs-lookup"><span data-stu-id="2bf53-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="2bf53-191">Чтобы настроить метод, перед использованием этого метода запустите другой метод `Service` `ServiceBuilder` в `build()` классе.</span><span class="sxs-lookup"><span data-stu-id="2bf53-191">To configure the `Service`, run another method in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="2bf53-192">Затем `service` передав его в качестве параметра в `Driver.createSession()` методе.</span><span class="sxs-lookup"><span data-stu-id="2bf53-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="2bf53-193">Использование Chromium-Specific параметров</span><span class="sxs-lookup"><span data-stu-id="2bf53-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="2bf53-194">Если для свойства установлено такое же свойство, можно использовать класс для доступа к тем же свойствам и методам Chromium, которые используются при автоматизации других браузеров `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="2bf53-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when automating other Chromium browsers.</span></span>  

#### [<span data-ttu-id="2bf53-195">C#</span><span class="sxs-lookup"><span data-stu-id="2bf53-195">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="2bf53-196">Python</span><span class="sxs-lookup"><span data-stu-id="2bf53-196">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="2bf53-197">Java</span><span class="sxs-lookup"><span data-stu-id="2bf53-197">Java</span></span>](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="2bf53-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2bf53-198">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="2bf53-199">Если для свойства установлено свойство, вы не сможете использовать свойства и методы для `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="2bf53-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="2bf53-200">Дополнительные параметры установки WebDriver</span><span class="sxs-lookup"><span data-stu-id="2bf53-200">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="2bf53-201">Хомякий</span><span class="sxs-lookup"><span data-stu-id="2bf53-201">Chocolatey</span></span>  

<span data-ttu-id="2bf53-202">Если в качестве [диспетчера][Chocolatey] пакетов вы используете в качестве диспетчера пакетов, установите драйвер Microsoft Edge с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="2bf53-202">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="2bf53-203">Дополнительные сведения см. в теме ["Selenium Chromium Edge Driver onChromy".][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="2bf53-203">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="2bf53-204">Docker</span><span class="sxs-lookup"><span data-stu-id="2bf53-204">Docker</span></span>  

<span data-ttu-id="2bf53-205">Если вы используете [Docker,][DockerHub]скачайте предварительно настроенный образ с помощью Microsoft Edge \(Chromium\) и предварительно установленного [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="2bf53-205">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="2bf53-206">Для получения дополнительных сведений перейдите к [контейнеру msedgedriver в Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="2bf53-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="2bf53-207">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2bf53-207">Next steps</span></span>

<span data-ttu-id="2bf53-208">Чтобы узнать больше о WebDriver и написании автоматических тестов WebDriver с помощью Selenium, перейдите к документации [Selenium.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="2bf53-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="2bf53-209">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bf53-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="2bf53-210">Команда Microsoft Edge с нетерпением услышит ваши отзывы об использовании WebDriver, Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2bf53-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="2bf53-211">Чтобы отправить команде вопросы и комментарии, выберите значок отправки отзыва в Microsoft Edge DevTools или отправьте твит [@EdgeDevTools.][TwitterTweetEdgeDevTools] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2bf53-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="2bf53-213">Значок **отправки отзыва** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2bf53-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Возможности и edgeOptions | Документы Майкрософт"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability — Microsoft Edge — политики | Документы Майкрософт"  

[Chocolatey]: https://chocolatey.org "Хомяк | Программное обеспечение"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Хомякий"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Разработчик (Майкрософт)"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Загрузки — webDriver | Разработчик (Майкрософт)"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Загрузка нового браузера Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Галерея NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | Галерея NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Проект автоматизации браузера Selenium :: документация для Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загружаемые | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Браузеры без | Википедия"  
