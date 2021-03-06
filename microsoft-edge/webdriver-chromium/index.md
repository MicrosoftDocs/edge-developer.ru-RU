---
description: Узнайте, как протестировать веб-сайт или приложение в Microsoft Edge или автоматизировать браузер с помощью WebDriver
title: Использование WebDriver (Chromium) для автоматизации тестирования
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, web development, html, css, javascript, developer, webdriver, selenium, testing, tools, automation, test
ms.openlocfilehash: 87855fad02243a9d86053e43b5523013644f7e35
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398835"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="cf486-104">Использование WebDriver (Chromium) для автоматизации тестирования</span><span class="sxs-lookup"><span data-stu-id="cf486-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="cf486-105">WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие пользователей.</span><span class="sxs-lookup"><span data-stu-id="cf486-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="cf486-106">Тесты и имитации WebDriver отличаются от тестов подразделений JavaScript следующими способами.</span><span class="sxs-lookup"><span data-stu-id="cf486-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="cf486-107">Доступ к функциям и сведениям, недоступным JavaScript, запущенным в браузерах.</span><span class="sxs-lookup"><span data-stu-id="cf486-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="cf486-108">Более точно имитирует события пользователей или события на уровне ОС.</span><span class="sxs-lookup"><span data-stu-id="cf486-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="cf486-109">Управляет несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="cf486-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="cf486-110">Выполняет несколько сеансов Microsoft Edge на определенной машине.</span><span class="sxs-lookup"><span data-stu-id="cf486-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="cf486-111">В следующем разделе описывается, как начать работу с WebDriver для Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="cf486-112">Установка Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="cf486-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cf486-113">Убедитесь, что [вы установите Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="cf486-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="cf486-114">Чтобы убедиться, что у вас установлен Microsoft Edge \(Chromium\), перейдите к и убедитесь, что номер версии `edge://settings/help` 75 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cf486-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="cf486-115">Скачайте Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="cf486-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="cf486-116">Чтобы начать автоматизацию тестов, воспользуйтесь следующими шагами для обеспечения того, чтобы устанавливаемая версия WebDriver совпадала с версией браузера.</span><span class="sxs-lookup"><span data-stu-id="cf486-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="cf486-117">Чтобы отобразить версию Microsoft Edge, перейдите к `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="cf486-117">To display the version of Microsoft Edge, navigate to `edge://settings/help`.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Номер сборки для Microsoft Edge Canary от 10 февраля 2021 г." lightbox="./media/microsoft-edge-version.msft.png":::
       <span data-ttu-id="cf486-119">Номер сборки для Microsoft Edge Canary от 10 февраля 2021 г.</span><span class="sxs-lookup"><span data-stu-id="cf486-119">The build number for Microsoft Edge Canary on February 10, 2021</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cf486-120">Перейдите [к Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]в разделе **Downloads** и скачайте webDriver, который соответствует номеру версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf486-120">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], under the **Downloads** section, and download the WebDriver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Раздел Downloads на Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="cf486-122">Раздел **Downloads** на [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-122">The **Downloads** section on [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a><span data-ttu-id="cf486-123">Выберите привязку языка WebDriver</span><span class="sxs-lookup"><span data-stu-id="cf486-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="cf486-124">Последний компонент, который необходимо скачать, — это драйвер клиента, который должен переводить код \(Python, Java, C\#, Ruby, JavaScript\) в команды, которые выполняет Microsoft Edge Driver в Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cf486-125">[Скачайте языковую привязку WebDriver по вашему выбору.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="cf486-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="cf486-126">Команда Microsoft Edge рекомендует [selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] или более поздний, так как поддерживает Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cf486-127">Однако вы можете управлять Microsoft Edge \(Chromium\) во всех старых версиях Selenium, включая текущий стабильный выпуск Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="cf486-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cf486-128">Если вы ранее автоматизировали или протестировали Microsoft Edge \(Chromium\) с использованием и классами, код WebDriver не будет работать в `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cf486-128">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="cf486-129">Чтобы решить проблему, обновите тесты для использования класса и `EdgeOptions` скачайте [Microsoft Edge Driver.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-129">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="use-selenium-3"></a><span data-ttu-id="cf486-130">Использование selenium 3</span><span class="sxs-lookup"><span data-stu-id="cf486-130">Use Selenium 3</span></span>  

<span data-ttu-id="cf486-131">Если вы уже используете [Selenium 3,][|::ref1::|]возможно, у вас есть существующие тесты браузера и вы хотите добавить покрытие для Microsoft Edge \(Chromium\) без изменения версии Selenium.</span><span class="sxs-lookup"><span data-stu-id="cf486-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="cf486-132">Чтобы использовать [Selenium 3][|::ref2::|] для записи автоматических тестов для Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\), установите пакет [Selenium Tools для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] для использования обновленного драйвера.</span><span class="sxs-lookup"><span data-stu-id="cf486-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="cf486-133">Классы и классы, включенные в инструменты, полностью совместимы со встроенными эквивалентами `EdgeDriver` `EdgeDriverService` в Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="cf486-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="cf486-134">Используйте следующие действия, чтобы добавить в проект [средства selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3.][|::ref3::|]</span><span class="sxs-lookup"><span data-stu-id="cf486-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<a name="c"></a><span data-ttu-id="cf486-135">C#</span><span class="sxs-lookup"><span data-stu-id="cf486-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="cf486-136">Добавьте [пакеты Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] в проект .NET с помощью [CLI NuGet][NugetCLI] [или Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="cf486-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="cf486-137">Python</span><span class="sxs-lookup"><span data-stu-id="cf486-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="cf486-138">Используйте [пункт][PythonPip] для установки [пакетов msedge-selenium-tools][PythonSeleniumTools] и [selenium.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="cf486-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="cf486-139">Java</span><span class="sxs-lookup"><span data-stu-id="cf486-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="cf486-140">Если в проекте Java используется Maven, скопируйте и вклейте в файл следующую зависимость, чтобы добавить `pom.xml` [msedge-selenium-tools-java.][SonatypeMavenRepositorySearch]</span><span class="sxs-lookup"><span data-stu-id="cf486-140">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="cf486-141">Пакет Java также доступен для скачивания непосредственно на странице [Selenium Tools для Microsoft Edge Releases.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="cf486-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="cf486-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf486-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="cf486-143">Используйте [npm][JavaScript|::ref4::|] для установки [пакетов edge-selenium-tools][JavaScriptSeleniumTools] и [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="cf486-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="cf486-144">Автоматизация Microsoft Edge (Chromium) с помощью WebDriver</span><span class="sxs-lookup"><span data-stu-id="cf486-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="cf486-145">Чтобы автоматизировать браузер с помощью WebDriver, сначала необходимо запустить сеанс WebDriver с помощью предпочтительной языковой привязки WebDriver.</span><span class="sxs-lookup"><span data-stu-id="cf486-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="cf486-146">Сеанс — это один запущенный экземпляр браузера, управляемый с помощью команд WebDriver.</span><span class="sxs-lookup"><span data-stu-id="cf486-146">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="cf486-147">Запустите сеанс WebDriver, чтобы запустить новый экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="cf486-147">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="cf486-148">Экземпляр запущенного браузера остается открытым до закрытия сеанса WebDriver.</span><span class="sxs-lookup"><span data-stu-id="cf486-148">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="cf486-149">В следующем контенте вы можете использовать Selenium для запуска сеанса WebDriver с Помощью Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cf486-150">Примеры можно запускать с помощью selenium 3 или 4.</span><span class="sxs-lookup"><span data-stu-id="cf486-150">You may run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="cf486-151">Чтобы использовать с selenium 3, необходимо установить [пакет Selenium Tools для Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]</span><span class="sxs-lookup"><span data-stu-id="cf486-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="cf486-152">Автоматизация Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="cf486-152">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="cf486-153">Selenium использует `EdgeDriver` класс для управления сеансом Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="cf486-154">Чтобы запустить сеанс и автоматизировать Microsoft Edge \(Chromium\), создайте новый объект и передайте ему объект с `EdgeDriver` `EdgeOptions` `UseChromium` задатким свойству `true` .</span><span class="sxs-lookup"><span data-stu-id="cf486-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="cf486-155">C#</span><span class="sxs-lookup"><span data-stu-id="cf486-155">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="cf486-156">Python</span><span class="sxs-lookup"><span data-stu-id="cf486-156">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="cf486-157">Java</span><span class="sxs-lookup"><span data-stu-id="cf486-157">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="cf486-158">Класс `EdgeDriver` поддерживает только Microsoft Edge \(Chromium\) и не поддерживает Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="cf486-158">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="cf486-159">Для основного использования можно создать без `EdgeDriver` предоставления `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="cf486-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="cf486-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf486-160">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="cf486-161">Если ваш ИТ-администратор задает политику [DeveloperToolsAvailability,][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] Microsoft Edge Driver не может управлять `2` Microsoft Edge \(Chromium\), так как драйвер использует [Microsoft Edge DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="cf486-162">[Убедитесь, что политика developerToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] установлена для или для автоматизации `0` Microsoft Edge `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="cf486-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="cf486-163">Выбор отдельных бинарей браузера (только для хрома)</span><span class="sxs-lookup"><span data-stu-id="cf486-163">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="cf486-164">Сеанс WebDriver можно запустить с помощью определенных разнонамеров Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="cf486-165">Например, можно выполнить тесты с помощью каналов предварительного просмотра [Microsoft Edge,][MicrosoftedgeinsiderDownload] таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="cf486-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="cf486-166">C#</span><span class="sxs-lookup"><span data-stu-id="cf486-166">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="cf486-167">Python</span><span class="sxs-lookup"><span data-stu-id="cf486-167">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="cf486-168">Java</span><span class="sxs-lookup"><span data-stu-id="cf486-168">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="cf486-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf486-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="cf486-170">Настройка службы драйверов Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cf486-170">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="cf486-171">C#</span><span class="sxs-lookup"><span data-stu-id="cf486-171">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cf486-172">При создании экземпляра класса класс создает и запускает соответствующий класс для `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) или Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-172">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="cf486-173">Если вы хотите создать метод, используйте метод для создания метода, настроенного для `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-173">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cf486-174">Метод `CreateChromiumService()` полезен при добавлении настроек.</span><span class="sxs-lookup"><span data-stu-id="cf486-174">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="cf486-175">Например, в следующем коде начинается подробный выход журнала.</span><span class="sxs-lookup"><span data-stu-id="cf486-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="cf486-176">Вам не нужно предоставлять объект при проходе `EdgeOptions` `EdgeDriverService` в `EdgeDriver` экземпляр.</span><span class="sxs-lookup"><span data-stu-id="cf486-176">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="cf486-177">Класс использует параметры по умолчанию для `EdgeDriver` Microsoft Edge \(EdgeHTML\) или Microsoft Edge \(Chromium\) на основе предоставляемой вами службы.</span><span class="sxs-lookup"><span data-stu-id="cf486-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="cf486-178">Однако, если вы хотите предоставить как классы, так и классы, убедитесь, что оба настроены для одной и той же `EdgeDriverService` `EdgeOptions` версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf486-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="cf486-179">Например, по умолчанию можно использовать свойства класса Microsoft Edge \(EdgeHTML\) и `EdgeDriverService` свойства Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="cf486-179">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="cf486-180">Класс `EdgeDriver` бросает ошибку, чтобы предотвратить использование различных версий.</span><span class="sxs-lookup"><span data-stu-id="cf486-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="cf486-181">Python</span><span class="sxs-lookup"><span data-stu-id="cf486-181">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cf486-182">При использовании Python объект создает и `Edge` управляет `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="cf486-182">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="cf486-183">Чтобы настроить объект, передай дополнительные аргументы объекту, `EdgeService` как указано в следующем `Edge` коде.</span><span class="sxs-lookup"><span data-stu-id="cf486-183">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="cf486-184">Java</span><span class="sxs-lookup"><span data-stu-id="cf486-184">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cf486-185">Используйте метод `createDefaultService()` для создания `EdgeDriverService` настраиваемого для Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cf486-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="cf486-186">Используйте свойства системы Java для настройки служб драйверов в Java.</span><span class="sxs-lookup"><span data-stu-id="cf486-186">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="cf486-187">Например, следующий код использует свойство `"webdriver.edge.verboseLogging"` для включаемой многословной выходной записи журнала.</span><span class="sxs-lookup"><span data-stu-id="cf486-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="cf486-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf486-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="cf486-189">При использовании JavaScript создайте и настройте `Service` `ServiceBuilder` класс.</span><span class="sxs-lookup"><span data-stu-id="cf486-189">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="cf486-190">Необязательно, вы можете передать объект объекту, который запускает `Service` `Driver` \(и останавливает\) службу для вас.</span><span class="sxs-lookup"><span data-stu-id="cf486-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="cf486-191">Чтобы настроить `Service` метод, запустите другой метод в `ServiceBuilder` классе перед `build()` использованием метода.</span><span class="sxs-lookup"><span data-stu-id="cf486-191">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="cf486-192">Затем `service` передай параметр в `Driver.createSession()` методе.</span><span class="sxs-lookup"><span data-stu-id="cf486-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="cf486-193">Использование Chromium-Specific параметры</span><span class="sxs-lookup"><span data-stu-id="cf486-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="cf486-194">Если вы установите свойство, вы можете использовать класс для доступа к тем же свойствам и методам, которые используются при автоматизации других браузеров `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="cf486-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="cf486-195">C#</span><span class="sxs-lookup"><span data-stu-id="cf486-195">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="cf486-196">Python</span><span class="sxs-lookup"><span data-stu-id="cf486-196">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="cf486-197">Java</span><span class="sxs-lookup"><span data-stu-id="cf486-197">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="cf486-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="cf486-198">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="cf486-199">Если свойство установлено, вы не можете использовать свойства и методы для `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="cf486-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <a name="other-webdriver-installation-options"></a><span data-ttu-id="cf486-200">Другие параметры установки WebDriver</span><span class="sxs-lookup"><span data-stu-id="cf486-200">Other WebDriver installation options</span></span>  

### <a name="chocolatey"></a><span data-ttu-id="cf486-201">Chocolatey</span><span class="sxs-lookup"><span data-stu-id="cf486-201">Chocolatey</span></span>  

<span data-ttu-id="cf486-202">Если вы используете [Chocolatey][Chocolatey] в качестве диспетчера пакетов, запустите следующую команду, чтобы установить Microsoft Edge Driver.</span><span class="sxs-lookup"><span data-stu-id="cf486-202">If you use [Chocolatey][Chocolatey] as your package manager, run the following command to install the Microsoft Edge Driver.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="cf486-203">Дополнительные сведения перейдите в [Selenium Chromium Edge Driver on Chocolatey.][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-203">For more information, navigate to [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <a name="docker"></a><span data-ttu-id="cf486-204">Docker</span><span class="sxs-lookup"><span data-stu-id="cf486-204">Docker</span></span>  

<span data-ttu-id="cf486-205">Если вы используете [Docker,][DockerHub]запустите следующую команду, чтобы скачать предварительно настроенное изображение с предварительно установленными Microsoft Edge \(Chromium\) и [Microsoft Edge Driver.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-205">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="cf486-206">Дополнительные сведения можно получить в [контейнере msedgedriver в Центре Docker.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="cf486-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="cf486-207">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cf486-207">Next steps</span></span>  

<span data-ttu-id="cf486-208">Чтобы узнать больше о WebDriver и о том, как писать автоматические тесты WebDriver с помощью selenium, перейдите к документации [Selenium][SeleniumDocumentation].</span><span class="sxs-lookup"><span data-stu-id="cf486-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cf486-209">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cf486-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="cf486-210">Команда Microsoft Edge готова услышать ваши отзывы об использовании WebDriver, Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf486-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="cf486-211">Чтобы отправить группе вопросы и комментарии, выберите значок Отправка отзывов в Microsoft Edge DevTools или отправьте @EdgeDevTools [.][TwitterTweetEdgeDevTools] \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cf486-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="cf486-213">Значок **Отправка** отзывов в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cf486-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Возможности и edgeOptions | Документы Майкрософт"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability — Microsoft Edge — политики | Документы Майкрософт"  

[Chocolatey]: https://chocolatey.org "Шоколадный | Chocolatey Software"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Chocolatey"  

[DockerHub]: https://hub.docker.com "Центр Docker"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Центр Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Веб-| Разработчик Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Загрузка нового браузера Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Галерея NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | Галерея NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | Галерея NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "селен | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "Проект автоматизации браузера Selenium | Документация для Selenium"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загрузка | Selenium"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "поиск центрального репозитория maven | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация чирикать"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Веб-| W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Безгол | Википедия"  
