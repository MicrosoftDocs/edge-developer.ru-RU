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
# <a name="use-webdriver-chromium-for-test-automation"></a>Использование WebDriver (Chromium) для автоматизации тестирования  

WebDriver позволяет разработчикам создавать автоматические тесты, имитирующие взаимодействие пользователей.  Тесты и имитации WebDriver отличаются от тестов подразделений JavaScript следующими способами.  

*   Доступ к функциям и сведениям, недоступным JavaScript, запущенным в браузерах.  
*   Более точно имитирует события пользователей или события на уровне ОС.  
*   Управляет несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.  
*   Выполняет несколько сеансов Microsoft Edge на определенной машине.  
    
В следующем разделе описывается, как начать работу с WebDriver для Microsoft Edge \(Chromium\).  

## <a name="install-microsoft-edge-chromium"></a>Установка Microsoft Edge (Chromium)  

Убедитесь, что [вы установите Microsoft Edge (Chromium).][MicrosoftEdge]  Чтобы убедиться, что у вас установлен Microsoft Edge \(Chromium\), перейдите к и убедитесь, что номер версии `edge://settings/help` 75 или более поздней версии.  

## <a name="download-microsoft-edge-driver"></a>Скачайте Microsoft Edge Driver  

Чтобы начать автоматизацию тестов, воспользуйтесь следующими шагами для обеспечения того, чтобы устанавливаемая версия WebDriver совпадала с версией браузера.  

1.  Чтобы отобразить версию Microsoft Edge, перейдите к `edge://settings/help` .  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="Номер сборки для Microsoft Edge Canary от 10 февраля 2021 г." lightbox="./media/microsoft-edge-version.msft.png":::
       Номер сборки для Microsoft Edge Canary от 10 февраля 2021 г.  
    :::image-end:::  
    
1.  Перейдите [к Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]в разделе **Downloads** и скачайте webDriver, который соответствует номеру версии Microsoft Edge.  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="Раздел Downloads на Microsoft Edge Driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       Раздел **Downloads** на [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a>Выберите привязку языка WebDriver  

Последний компонент, который необходимо скачать, — это драйвер клиента, который должен переводить код \(Python, Java, C\#, Ruby, JavaScript\) в команды, которые выполняет Microsoft Edge Driver в Microsoft Edge \(Chromium\).  

[Скачайте языковую привязку WebDriver по вашему выбору.][SeleniumDownloads]  Команда Microsoft Edge рекомендует [selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] или более поздний, так как поддерживает Microsoft Edge \(Chromium\).  Однако вы можете управлять Microsoft Edge \(Chromium\) во всех старых версиях Selenium, включая текущий стабильный выпуск Selenium 3.  

> [!IMPORTANT]
> Если вы ранее автоматизировали или протестировали Microsoft Edge \(Chromium\) с использованием и классами, код WebDriver не будет работать в `ChromeDriver` `ChromeOptions` Microsoft Edge Version 80 или более поздней версии.  Чтобы решить проблему, обновите тесты для использования класса и `EdgeOptions` скачайте [Microsoft Edge Driver.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  

### <a name="use-selenium-3"></a>Использование selenium 3  

Если вы уже используете [Selenium 3,][|::ref1::|]возможно, у вас есть существующие тесты браузера и вы хотите добавить покрытие для Microsoft Edge \(Chromium\) без изменения версии Selenium.  Чтобы использовать [Selenium 3][|::ref2::|] для записи автоматических тестов для Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\), установите пакет [Selenium Tools для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] для использования обновленного драйвера.  Классы и классы, включенные в инструменты, полностью совместимы со встроенными эквивалентами `EdgeDriver` `EdgeDriverService` в Selenium 4.  

Используйте следующие действия, чтобы добавить в проект [средства selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3.][|::ref3::|]  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Добавьте [пакеты Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] в проект .NET с помощью [CLI NuGet][NugetCLI] [или Visual Studio][VisualStudio].  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="selenium-tools-install"></a>  

Используйте [пункт][PythonPip] для установки [пакетов msedge-selenium-tools][PythonSeleniumTools] и [selenium.][PythonSelenium]  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="selenium-tools-install"></a>  

Если в проекте Java используется Maven, скопируйте и вклейте в файл следующую зависимость, чтобы добавить `pom.xml` [msedge-selenium-tools-java.][SonatypeMavenRepositorySearch]  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

Пакет Java также доступен для скачивания непосредственно на странице [Selenium Tools для Microsoft Edge Releases.][GithubMicrosoftEdgeSeleniumToolsReleases]  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Используйте [npm][JavaScript|::ref4::|] для установки [пакетов edge-selenium-tools][JavaScriptSeleniumTools] и [selenium-webdriver.][JavaScriptSelenium]  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a>Автоматизация Microsoft Edge (Chromium) с помощью WebDriver  

Чтобы автоматизировать браузер с помощью WebDriver, сначала необходимо запустить сеанс WebDriver с помощью предпочтительной языковой привязки WebDriver.  Сеанс — это один запущенный экземпляр браузера, управляемый с помощью команд WebDriver.  Запустите сеанс WebDriver, чтобы запустить новый экземпляр браузера.  Экземпляр запущенного браузера остается открытым до закрытия сеанса WebDriver.  

В следующем контенте вы можете использовать Selenium для запуска сеанса WebDriver с Помощью Microsoft Edge \(Chromium\).  Примеры можно запускать с помощью selenium 3 или 4.  Чтобы использовать с selenium 3, необходимо установить [пакет Selenium Tools для Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]  

### <a name="automate-microsoft-edge-chromium"></a>Автоматизация Microsoft Edge (Chromium)  

Selenium использует `EdgeDriver` класс для управления сеансом Microsoft Edge \(Chromium\).  Чтобы запустить сеанс и автоматизировать Microsoft Edge \(Chromium\), создайте новый объект и передайте ему объект с `EdgeDriver` `EdgeOptions` `UseChromium` задатким свойству `true` .  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

Класс `EdgeDriver` поддерживает только Microsoft Edge \(Chromium\) и не поддерживает Microsoft Edge \(EdgeHTML\).  Для основного использования можно создать без `EdgeDriver` предоставления `EdgeOptions` .  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> Если ваш ИТ-администратор задает политику [DeveloperToolsAvailability,][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] Microsoft Edge Driver не может управлять `2` Microsoft Edge \(Chromium\), так как драйвер использует [Microsoft Edge DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  [Убедитесь, что политика developerToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] установлена для или для автоматизации `0` Microsoft Edge `1` (Chromium).  

### <a name="choose-specific-browser-binaries-chromium-only"></a>Выбор отдельных бинарей браузера (только для хрома)  

Сеанс WebDriver можно запустить с помощью определенных разнонамеров Microsoft Edge \(Chromium\).  Например, можно выполнить тесты с помощью каналов предварительного просмотра [Microsoft Edge,][MicrosoftedgeinsiderDownload] таких как Microsoft Edge Beta.  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a>Настройка службы драйверов Microsoft Edge  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

При создании экземпляра класса класс создает и запускает соответствующий класс для `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) или Microsoft Edge \(Chromium\).  

Если вы хотите создать метод, используйте метод для создания метода, настроенного для `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).  Метод `CreateChromiumService()` полезен при добавлении настроек.  Например, в следующем коде начинается подробный выход журнала.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Вам не нужно предоставлять объект при проходе `EdgeOptions` `EdgeDriverService` в `EdgeDriver` экземпляр.  Класс использует параметры по умолчанию для `EdgeDriver` Microsoft Edge \(EdgeHTML\) или Microsoft Edge \(Chromium\) на основе предоставляемой вами службы.  
> Однако, если вы хотите предоставить как классы, так и классы, убедитесь, что оба настроены для одной и той же `EdgeDriverService` `EdgeOptions` версии Microsoft Edge.  Например, по умолчанию можно использовать свойства класса Microsoft Edge \(EdgeHTML\) и `EdgeDriverService` свойства Chromium в `EdgeOptions` классе.  Класс `EdgeDriver` бросает ошибку, чтобы предотвратить использование различных версий.  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

При использовании Python объект создает и `Edge` управляет `EdgeService` .  Чтобы настроить объект, передай дополнительные аргументы объекту, `EdgeService` как указано в следующем `Edge` коде.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

Используйте метод `createDefaultService()` для создания `EdgeDriverService` настраиваемого для Microsoft Edge \(Chromium\).  Используйте свойства системы Java для настройки служб драйверов в Java.  Например, следующий код использует свойство `"webdriver.edge.verboseLogging"` для включаемой многословной выходной записи журнала.  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

При использовании JavaScript создайте и настройте `Service` `ServiceBuilder` класс.  Необязательно, вы можете передать объект объекту, который запускает `Service` `Driver` \(и останавливает\) службу для вас.  
Чтобы настроить `Service` метод, запустите другой метод в `ServiceBuilder` классе перед `build()` использованием метода.  Затем `service` передай параметр в `Driver.createSession()` методе.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a>Использование Chromium-Specific параметры  

Если вы установите свойство, вы можете использовать класс для доступа к тем же свойствам и методам, которые используются при автоматизации других браузеров `UseChromium` `true` `EdgeOptions` Chromium. [][WebdriverCapabilitiesEdgeOptions]  

#### [<a name="c"></a>C#](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a>Python](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a>Java](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a>JavaScript](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> Если свойство установлено, вы не можете использовать свойства и методы для `UseChromium` `true` Microsoft Edge \(EdgeHTML\).  

## <a name="other-webdriver-installation-options"></a>Другие параметры установки WebDriver  

### <a name="chocolatey"></a>Chocolatey  

Если вы используете [Chocolatey][Chocolatey] в качестве диспетчера пакетов, запустите следующую команду, чтобы установить Microsoft Edge Driver.  

```console
choco install selenium-chromium-edge-driver
```  

Дополнительные сведения перейдите в [Selenium Chromium Edge Driver on Chocolatey.][ChocolateyPackagesSeleniumChromiumEdgeDriver]  

### <a name="docker"></a>Docker  

Если вы используете [Docker,][DockerHub]запустите следующую команду, чтобы скачать предварительно настроенное изображение с предварительно установленными Microsoft Edge \(Chromium\) и [Microsoft Edge Driver.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Дополнительные сведения можно получить в [контейнере msedgedriver в Центре Docker.][DockerHubMsedgedriver]  

## <a name="next-steps"></a>Дальнейшие действия  

Чтобы узнать больше о WebDriver и о том, как писать автоматические тесты WebDriver с помощью selenium, перейдите к документации [Selenium][SeleniumDocumentation].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

Команда Microsoft Edge готова услышать ваши отзывы об использовании WebDriver, Selenium и Microsoft Edge.  Чтобы отправить группе вопросы и комментарии, выберите значок Отправка отзывов в Microsoft Edge DevTools или отправьте @EdgeDevTools [.][TwitterTweetEdgeDevTools] ****  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок **Отправка** отзывов в Microsoft Edge DevTools  
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
