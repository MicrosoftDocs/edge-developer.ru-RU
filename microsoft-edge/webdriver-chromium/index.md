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
# Использование WebDriver (Chromium) для тестовой автоматизации  

WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие с пользователем.  Тесты и имитации WebDriver отличаются от тестов javaScript, так как WebDriver:  

*   Доступ к функциям и сведениям, недоступным для JavaScript, запущенного в браузерах.  
*   Имитирует события пользователя или события на уровне ОС более точно.  
*   Управляет несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.  
*   Запускает несколько сеансов Microsoft Edge на определенном компьютере.  
    
В следующем разделе описывается, как начать работу с WebDriver для Microsoft Edge \(Chromium\).  

## Установка Microsoft Edge (Chromium)  

Убедитесь, что [вы установили Microsoft Edge (Chromium).][MicrosoftEdge]  Чтобы убедиться, что у вас установлен Microsoft Edge \(Chromium\), перейдите к и убедитесь, что номер версии `edge://settings/help` 75 или более поздней версии.  

## Скачивание драйвера Microsoft Edge  

Чтобы начать автоматизацию тестов, с помощью следующих действий убедитесь, что устанавливаемая версия WebDriver соответствует версии браузера.  

1.  Перейдите `edge://settings/help` к версии Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="Номер сборки для Microsoft Edge Canary 14 января 2020 г.":::
       Номер сборки для Microsoft Edge Canary 14 января 2020 г.
    :::image-end:::  
    
1.  Перейдите на [страницу загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, который соответствует номеру версии Microsoft Edge.  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="Раздел Загрузки страницы Драйвер Microsoft Edge":::
       Раздел "Загрузки" страницы ["Драйвер Microsoft Edge"][MicrosoftDeveloperEdgeToolsWebdriver]
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## Выбор привязки языка WebDriver  

Последний компонент, который необходимо скачать, — это специальный драйвер клиента для перевода кода \(Python, Java, C\#, Ruby, JavaScript\) в команды, которые выполняет драйвер Microsoft Edge в Microsoft Edge \(Chromium\).  

[Скачайте языковую привязку WebDriver по вашему выбору.][SeleniumDownloads]  Команда Microsoft Edge рекомендует [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] или более поздней версии, так как она поддерживает Microsoft Edge \(Chromium\).  Однако вы можете управлять Microsoft Edge \(Chromium\) во всех старых версиях Selenium, включая текущий стабильный выпуск Selenium 3.  

> [!IMPORTANT]
> Если вы ранее автоматизировали или тестируете Microsoft Edge \(Chromium\) с использованием и классами, код WebDriver не будет работать в Microsoft Edge версии 80 или более `ChromeDriver` `ChromeOptions` поздней.  Чтобы решить эту проблему, обновите тесты для использования класса и `EdgeOptions` скачайте [драйвер Microsoft Edge.][MicrosoftDeveloperEdgeToolsWebdriver]  

### Использование Selenium 3  

Если вы уже используете [Selenium 3,][|::ref1::|]возможно, у вас уже есть тесты браузера и вы захотите добавить покрытия для Microsoft Edge \(Chromium\) без изменения версии Selenium.  Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов для Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\), установите пакет [средств Selenium для Microsoft Edge,][GithubMicrosoftEdgeSeleniumTools] чтобы использовать обновленный драйвер.  Классы, включенные в инструменты, полностью совместимы со встроенными эквивалентами `EdgeDriver` `EdgeDriverService` в Selenium 4.  

Чтобы добавить средства [Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] в проект, с помощью следующих действий.  

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Добавьте [пакеты Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] в проект .NET с помощью [nuGet CLI][NugetCLI] [или Visual Studio.][VisualStudio]  

#### [Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Используйте [конвейер][PythonPip] для установки [пакетов msedge-selenium-tools][PythonSeleniumTools] и [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Если в проекте Java используется Maven, добавьте [msedge-selenium-tools-java,][SonatypeMavenRepositorySearch] выполнив в файле следующую `pom.xml` зависимость:  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Пакет Java также доступен для скачивания непосредственно на странице "Средства [Selenium для выпусков Microsoft Edge".][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Используйте [npm][JavaScript|::ref4::|] для установки [пакетов edge-selenium-tools][JavaScriptSeleniumTools] и [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Автоматизация Microsoft Edge (Chromium) с помощью WebDriver  

Чтобы автоматизировать браузер с помощью WebDriver, необходимо сначала запустить сеанс WebDriver с использованием предпочитаемой привязки языка WebDriver.  Сеанс — это один запущенный экземпляр браузера, который можно контролировать с помощью команд WebDriver.  Запуск сеанса WebDriver запускает новый экземпляр браузера.  Браузер, который открывается, остается открытым до закрытия сеанса WebDriver.  

Ниже приводится последующую информацию об использовании Selenium для запуска сеанса WebDriver с Microsoft Edge \(Chromium\).  Эти примеры можно запустить с помощью Selenium 3 или 4.  Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]  

### Автоматизация Microsoft Edge (Chromium)  

Selenium использует `EdgeDriver` класс для управления сеансом Microsoft Edge \(Chromium\). Чтобы запустить сеанс и автоматизировать Microsoft Edge \(Chromium\), создайте новый объект и передайте ему объект со `EdgeDriver` `EdgeOptions` свойством, `UseChromium` задав для него свойство `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

Класс поддерживает только Microsoft Edge (Chromium) и не поддерживает `EdgeDriver` Microsoft Edge (EdgeHTML). Для базового использования можно создать элемент `EdgeDriver` без предоставления `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [JavaScript](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Если ваш ИТ-администратор настроил политику [DeveloperToolsAvailability,][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] драйвер Microsoft Edge не сможет управлять Microsoft Edge (Chromium), так как драйвер использует `2` Microsoft Edge [DevTools.][DevtoolsIndex] [][MicrosoftDeveloperEdgeToolsWebdriver]  [Убедитесь, что для политики DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] установлено или для автоматизации Microsoft Edge `0` `1` (Chromium).  

### Выбор определенных binaries браузера (только для Chromium)  

Вы можете начать сеанс WebDriver с определенными binaries \(Chromium\) Microsoft Edge.  Например, можно выполнить тесты с помощью каналов предварительного просмотра [Microsoft Edge,][MicrosoftedgeinsiderDownload] таких как Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Python](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [Java](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Настройка службы драйверов Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Когда экземпляр класса создается с помощью класса, он создает и запускает соответствующий класс для `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) или Microsoft Edge \(Chromium\).  

Если вы хотите создать , создайте его, настроенный для `EdgeDriverService` Microsoft Edge \(Chromium\) с помощью `CreateChromiumService()` этого метода.  Это может оказаться полезным при необходимости добавления настроек. Например, следующий код запускает подробные выходные данные журнала.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>При передаче в экземпляр не требуется предоставлять `EdgeOptions` `EdgeDriverService` `EdgeDriver` объект.  Класс использует параметры по умолчанию для `EdgeDriver` Microsoft Edge \(EdgeHTML\) или Microsoft Edge \(Chromium\) на основе предоставляемой службы.  
> Тем не менее, если вы хотите предоставить и классы, убедитесь, что оба настроены для одной и той же `EdgeDriverService` `EdgeOptions` версии Microsoft Edge.  Например, невозможно использовать класс Microsoft Edge по умолчанию \(EdgeHTML\) и свойства `EdgeDriverService` Chromium в `EdgeOptions` классе.  Класс `EdgeDriver` высылает ошибку, чтобы запретить использование различных версий.  

#### [Python](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

При использовании Python объект создает объект и управляет `Edge` `EdgeService` им.  Чтобы настроить , `EdgeService` передав дополнительные аргументы `Edge` объекту, как указано в следующем коде.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [Java](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Используйте этот `createDefaultService()` метод для создания `EdgeDriverService` настроенного для Microsoft Edge \(Chromium\). Службы драйверов на Java настраиваются с помощью свойств системы Java. Например, следующий код использует свойство для подробного вывода `"webdriver.edge.verboseLogging"` журнала.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

При использовании JavaScript создайте и настройте a `Service` с `ServiceBuilder` классом.  При желании вы можете передать объект объекту, который запускает `Service` `Driver` \(и останавливает\) службу за вас.  
Чтобы настроить метод, перед использованием этого метода запустите другой метод `Service` `ServiceBuilder` в `build()` классе.  Затем `service` передав его в качестве параметра в `Driver.createSession()` методе.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Использование Chromium-Specific параметров  

Если для свойства установлено такое же свойство, можно использовать класс для доступа к тем же свойствам и методам Chromium, которые используются при автоматизации других браузеров `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Python](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [Java](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [JavaScript](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Если для свойства установлено свойство, вы не сможете использовать свойства и методы для `UseChromium` `true` Microsoft Edge \(EdgeHTML\).  

## Дополнительные параметры установки WebDriver  

### Хомякий  

Если в качестве [диспетчера][Chocolatey] пакетов вы используете в качестве диспетчера пакетов, установите драйвер Microsoft Edge с помощью следующей команды.  

```console
choco install selenium-chromium-edge-driver
```  

Дополнительные сведения см. в теме ["Selenium Chromium Edge Driver onChromy".][ChocolateyPackagesSeleniumChromiumEdgeDriver]  

### Docker  

Если вы используете [Docker,][DockerHub]скачайте предварительно настроенный образ с помощью Microsoft Edge \(Chromium\) и предварительно установленного [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] с помощью следующей команды.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Для получения дополнительных сведений перейдите к [контейнеру msedgedriver в Docker Hub.][DockerHubMsedgedriver]  

## Дальнейшие действия

Чтобы узнать больше о WebDriver и написании автоматических тестов WebDriver с помощью Selenium, перейдите к документации [Selenium.][SeleniumDocumentation]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

Команда Microsoft Edge с нетерпением услышит ваши отзывы об использовании WebDriver, Selenium и Microsoft Edge.  Чтобы отправить команде вопросы и комментарии, выберите значок отправки отзыва в Microsoft Edge DevTools или отправьте твит [@EdgeDevTools.][TwitterTweetEdgeDevTools] ****  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок **отправки отзыва** в Microsoft Edge DevTools  
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
