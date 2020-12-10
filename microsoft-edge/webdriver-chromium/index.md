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
# Использование Chromium для автоматизации тестов  

С помощью этого устройства вы можете (разработчикам) создавать автоматические тесты, имитирующие взаимодействие с пользователем.  Проверки и имитации для модулей-накопителей отличаются от модульных тестов JavaScript по следующим причинам.  

*   Доступ к функциям и сведениям, недоступным для JavaScript, которые выполняются в браузерах.  
*   Более точное моделирование событий пользователей и событий на уровне операционной системы.  
*   Управление несколькими окнами, вкладками и веб-страницами в одном тестовом сеансе.  
*   Запуск нескольких сеансов Microsoft EDGE на определенном компьютере.  
    
В следующем разделе описано, как приступить к работе с веб-диском Microsoft Edge \ (Chromium \).  

## Установка Microsoft EDGE (Chromium)  

Убедитесь в том, что вы установили [Microsoft EDGE (Chromium)][MicrosoftEdge].  Чтобы убедиться в том, что у вас установлен Microsoft Edge \ (Chromium \), найдите `edge://settings/help` и проверьте номер версии 75 или более поздней версии.  

## Скачать драйвер Microsoft Edge  

Чтобы приступить к автоматизации тестов, выполните указанные ниже действия, чтобы убедиться, что версия веб – диска, установленная на вашем компьютере, совпадает с вашей версией браузера.  

1.  Перейдите в раздел, чтобы `edge://settings/help` получить версию Microsoft Edge.  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-version.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г." lightbox="../media/webdriver-chromium/edge-version.png":::
       Номер сборки Microsoft Edge Канарские 14 января 2020 г.  
    :::image-end:::  
    
1.  Перейдите на страницу [загрузки драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] и скачайте драйвер, соответствующий номеру версии Microsoft Edge.  
    
    :::image type="complex" source="../media/webdriver-chromium/edge-driver-install.png" alt-text="Раздел загружаемые файлы на странице драйвера Microsoft Edge"::: lightbox="../media/webdriver-chromium/edge-driver-install.png":::
       Раздел "загружаемые файлы" на странице [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]  
    :::image-end:::  
    
    > [!NOTE] 
    > Дополнительные сведения об автоматизации тестирования с помощью Microsoft Edge \ (EdgeHTML \) можно найти в [веб-накопителе Microsoft для Microsoft EDGE (EdgeHTML)][Webdriver].  
    
## Выбор языковой привязки для веб-дисков  

Последний компонент, который необходимо скачать, — это языковый драйвер клиента для перевода кода \ (Python, Java, C \ #, Ruby, JavaScript \) в команды, которые драйвер Microsoft EDGE работает в Microsoft Edge \ (Chromium \).  

[Скачайте выбранную вами языковую привязку веб дисков][SeleniumDownloads].  Команда Microsoft Edge рекомендует [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она поддерживает Microsoft Edge \ (Chromium \).  Тем не менее, вы можете управлять Microsoft Edge \ (Chromium \) во всех более ранних версиях Selenium, включая текущую стабильную версию Selenium 3.  

> [!IMPORTANT]
> Если вы уже выполняли автоматизацию или тестирование Microsoft Edge \ (Chromium \) с использованием `ChromeDriver` и `ChromeOptions` классами, код веб-дисковода не будет работать в Microsoft Edge версии 80 или более поздней.  Чтобы устранить эту проблему, обновите тесты, чтобы использовать этот `EdgeOptions` класс и установить [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Использование Selenium 3  

Если вы уже используете [Selenium 3][|::ref1::|], возможно, у вас есть тестирование браузера и хотите добавить покрытие для Microsoft Edge \ (Chromium \) без изменения версии Selenium.  Чтобы использовать [Selenium 3][|::ref2::|] для написания автоматических тестов как для Microsoft Edge \ (EdgeHTML \), так и для Microsoft Edge \ (Chromium \), установите для него пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , чтобы использовать обновленный драйвер.  `EdgeDriver`Классы и `EdgeDriverService` компоненты, включенные в эти инструменты, полностью совместимы с встроенными эквивалентами в Selenium 4.  

Чтобы добавить в проект [инструменты Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] и [Selenium 3][|::ref3::|] , выполните указанные ниже действия.

#### [C#](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

Добавьте пакеты [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] и [Selenium.][NugetPackagesSeleniumWebdriver31410] Package в проект .NET с помощью [инфраструктуры NuGet][NugetCLI] или [Visual Studio][VisualStudio].  

#### [Языке](#tab/python/)  

<a id="selenium-tools-install"></a>  

Чтобы установить пакеты [msedge-Selenium-Tools][PythonSeleniumTools] и [Selenium][PythonSelenium] , воспользуйтесь [PIP][PythonPip] .  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [JavaScript](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

Используйте [NPM][JavaScript|::ref4::|] для установки пакетов [Edge-Selenium-Tools][JavaScriptSeleniumTools] и [Selenium-Drives][JavaScriptSelenium] .  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## Использование веб-накопителя (Microsoft EDGE (Chromium))

Вы можете использовать следующие примеры с помощью Selenium 3 или 4.  Для использования с Selenium 3 необходимо установить пакет [средств Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .  

### Основное использование  

Для использования с Microsoft Edge \ (EdgeHTML \) создайте экземпляр класса по умолчанию `EdgeDriver` .  

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [Языке](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [JavaScript](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### Управление Microsoft EDGE (Chromium)  

Для использования с Microsoft Edge \ (Chromium \) создайте новый `EdgeDriver` класс и передайте ему `EdgeOptions` объект со `UseChromium` свойством, для которого задано значение `true` .  

#### [C#](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Языке](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
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
> Если у ИТ-администратора задана политика [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] `2` , [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] не сможет установить Microsoft Edge [(Chromium)][MicrosoftEdge] , так как в драйвере используется [Microsoft Edge DevTools][DevToolsMain].  Убедитесь в том, что для политики [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] задано значение " `0` или" `1` автоматизировать [Microsoft EDGE (Chromium)][MicrosoftEdge].  

### Выбор определенных двоичных файлов браузера (только Chromium)  

Вы можете использовать этот `EdgeOptions` класс с определенными двоичными файлами Microsoft Edge \ (Chromium \).  Например, вы можете выполнять тесты с помощью [каналов предварительной версии Microsoft Edge][MicrosoftedgeinsiderDownload] , таких как Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Языке](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [JavaScript](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### Настройка службы драйвера Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

Когда `EdgeDriver` экземпляр класса создается с помощью `EdgeOptions` класса, он создает и запускает соответствующий `EdgeDriverService` класс для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \).  

Если вы хотите создать объект `EdgeDriverService` для Microsoft Edge \ (Chromium \) с помощью метода, создайте его `CreateChromiumService()` .  Вы можете использовать дополнительные настройки, такие как включение подробного вывода журнала в приведенном ниже коде.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
>Вам не нужно предоставлять `EdgeOptions` объект при передаче `EdgeDriverService` `EdgeDriver` экземпляру. `EdgeDriver`Класс использует параметры по умолчанию для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \) в зависимости от предоставленной услуги.  
> Тем не менее, если вы хотите предоставить `EdgeDriverService` оба `EdgeOptions` класса и классы, убедитесь, что они настроены для одной и той же версии Microsoft Edge.  Например, невозможно использовать класс по умолчанию Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` и свойства Chromium в `EdgeOptions` классе.  `EdgeDriver`Класс вызывает ошибку, чтобы предотвратить использование разных версий.  

#### [Языке](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

При использовании Python `Edge` объект создает и управляет `EdgeService` .  Чтобы настроить `EdgeService` , передайте дополнительные аргументы объекту, `Edge` как указано в приведенном ниже коде.  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [JavaScript](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

При использовании JavaScript создайте и настройте `Service` класс с помощью `ServiceBuilder` класса.  При необходимости вы можете передать `Service` объект `Driver` объекту, который будет заключаться в службу (и остановить ее).  
Чтобы настроить `Service` , выполните дополнительные методы в `ServiceBuilder` классе перед использованием `build()` метода.  Затем передается в `service` `Driver.createSession()` методе как параметр.  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### Использование Chromium-Specific параметров  

Если вы задаете `UseChromium` свойство `true` , вы можете использовать `EdgeOptions` Этот класс для доступа к таким же [свойствам и методам Chromium][SeleniumWebDriverChromeoptionsClass] , что и при автоматизации других браузеров Chromium.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Языке](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
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
> Если `UseChromium` свойство имеет значение `true` , вы не можете пользоваться свойствами и методами для Microsoft Edge \ (EdgeHTML \).  

## Дополнительные параметры установки для устройства добавления новых устройств  

### Шоколад  

Если вы используете [шоколад][Chocolatey] в качестве диспетчера пакетов, установите драйвер Microsoft EDGE, выполнив следующую команду:  

```console
choco install selenium-chromium-edge-driver
```  

Дополнительные сведения можно найти [в разделе драйвер Selenium Chromium EDGE на шоколаде][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Если вы используете [закрепление][DockerHub], скачайте предварительно настроенное изображение с помощью Microsoft Edge \ (Chromium \) и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] , которое предустановлено, выполнив следующую команду:  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Дополнительные сведения можно найти [в разделе контейнер в центре Dock][DockerHubMsedgedriver].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

Группа Microsoft Edge – это информация о том, как использовать веб – диски, Selenium и Microsoft Edge.  Чтобы сообщить команде о том, что вы думаете, щелкните значок **Отправить отзыв** в Microsoft Edge DevTools или отправьте твит [@EdgeDevTools][TwitterTweetEdgeDevTools].  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправить отзыв в Microsoft Edge DevTools":::  lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок " **Отправить отзыв** " в Microsoft Edge DevTools  
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
