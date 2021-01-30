---
description: Справочник по возможностям WebDriver и вариантам Microsoft Edge, поддерживаемых EdgeDriver (Chromium).
title: Возможности и EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, html, css, javascript, разработчик, webdriver, selenium, тестирование, средства, автоматизация, тест
ms.openlocfilehash: c2842740dfc6d902d1727634e00565f8e556969d
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306236"
---
# Возможности и EdgeOptions  

Возможности — это параметры, которые можно использовать для настройки и настройки `EdgeDriver` сеанса.  Чтобы узнать о запуске нового `EdgeDriver` сеанса, перейдите к [функции автоматизации Microsoft Edge.][WebdriverIndexDrivingMicrosoftEdgeChromium]  В этой статье описываются все поддерживаемые возможности [Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] и сведения о передаче возможностей в `EdgeDriver` сеансы.  

Возможности передаются в сеанс WebDriver в качестве карты JSON.  Привязки языка WebDriver обычно предоставляют безопасные для типа методы удобства, поэтому вам не нужно настраивать карту JSON самостоятельно.  Различные привязки языков WebDriver используют различные механизмы для настройки возможностей.  Перейдите к документации по [предпочитаемой привязке][WebdriverIndexChooseWebdriverLanguageBinding] языка, чтобы узнать больше о настройке возможностей.  [Selenium][SeleniumMain] настраивает возможности с помощью `EdgeOptions` класса.  

## Использование класса EdgeOptions  

Создайте экземпляр , который предоставляет удобные методы для создания специальных `EdgeOptions` возможностей Microsoft Edge.  После настройки объекта `EdgeOptions` передав `EdgeOptions` его в `EdgeDriver` конструктор.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Чтобы использовать возможности, не связанные с удобным методом, используйте `AddAdditionalCapability` этот метод.  Необходимо передать полное имя возможности и значение с правильным типом.  Чтобы просмотреть полный список принятых возможностей и типов значений, перейдите к [объекту EdgeOptions.](#edgeoptions-object)  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Распознаваемая возможность  

Чтобы получить стандартные возможности, перейдите к документации `EdgeDriver` [Selenium][SharedCapabilitiesSeleniumDocumentation] и [стандарту W3C WebDriver.][CapabilitiesW3cWebdriver]  В этой статье перечислены только возможности, специфичные для Microsoft Edge.  

## Объект EdgeOptions  

Большинство специальных возможностей Microsoft Edge 2013 2013 2013 2013 2013 и 2013 201 `EdgeOptions`  В некоторых языках возможности реализуются `EdgeOptions` классом.  На других языках эти возможности хранятся в словаре в `ms:edgeOptions` `DesiredCapabilities` .  

| Возможность | Тип | Значение по умолчанию | Сведения |  
|:--- |:--- |:--- |:--- |  
| args | список строк |  | Список аргументов командной строки, которые необходимо использовать при запуске Microsoft Edge.  Аргументы со связанным значением должны разделяться знаком `=` \(например, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binary | string |  | Путь к двоичному файлу Microsoft Edge для использования \(в macOS путь должен быть фактическим двоичным файлом, а не только приложением.  например, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Адрес сервера отладки, к которому необходимо подключиться, например, в `hostname/ip:port` виде `127.0.0.1:38947` . |
| detach | логический | `false` | Если Microsoft Edge завершит работу, когда служба WebDriver завершит работу, даже если локальный конец `false` WebDriver не закрыл сеанс.  Если microsoft Edge закрывает сеанс, локальный конец `true` WebDriver закрывает сеанс.  Если локальный конец WebDriver не закрывает сеанс, не очищает временную папку данных пользователя, используемую `true` `EdgeDriver` экземпляром Microsoft Edge. |  
| excludeSwitches | список строк |  | Список коммутаторов командной строки Microsoft Edge, которые необходимо исключить, что EdgeDriver по умолчанию передается при запуске Microsoft Edge.  Избегайте `--` префикса для коммутаторов. |  
| extensions | список строк |  | Список расширений, которые необходимо установить при запуске.  Каждый элемент в списке должен быть упакованным расширением с кодировки Base 64 `.crx` (\( \). |  
| localState | dictionary |  | Словарь с каждой записью, состоящей из имени предпочтения и значения.  Настройки применяются к файлу локального состояния в папке данных пользователя. |  
| minidumpPath | string |  | Каталог для хранения мини-надушек Microsoft Edge.  \(Поддерживается только в Linux.\) |  
| mobileEmulation | dictionary |  | Словарь со значением или `deviceName` значениями `deviceMetrics` для и `userAgent` . |  
| perfLoggingPrefs | dictionary |  | Необязательный словарь, который определяет параметры ведения журнала производительности.  для получения дополнительных сведений перейдите к [объекту perfLoggingPrefs.](#perfloggingprefs-object) |  
| prefs | dictionary |  | Словарь с каждой записью, состоящей из имени предпочтения и значения.  Параметры применяются только к используемой учетной записи пользователя.  Например, перейдите к файлу в папке пользовательских `Preferences` данных Microsoft Edge. |  
| wdpAddress | string |  | Адрес сервера портала устройств Windows, к которому вы подключаетсяе, например, в `hostname/ip:port` виде  `127.0.0.1:50080` .  Для получения дополнительных сведений перейдите к [удаленной отладки — устройства с Windows 10.][DevtoolsRemoteDebuggingWindows] |  
| wdpPassword | string |  | Необязательный пароль для подключения к серверу портала устройств Windows.  Обязательно, если на сервере включена проверка подлинности. |  
| wdpUsername | string |  | Необязательное имя пользователя, используемое при подключении к серверу портала устройств Windows.  Обязательно, если на сервере включена проверка подлинности. |  
| windowsApp | string |  | Пример: ИД модели пользователя приложения для запуска пакета приложения Microsoft `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` Edge.  Используйте вместо подключения к устройству или эмулятору `windowsApp` `binary` Windows 10X с помощью портала устройств Windows. |  
| windowTypes | список строк |  | Список типов окон, отображаемого в списке окне.  Для доступа к элементам веб-приложения Android `webview` включаем в список. |  

## Объект perfLoggingPrefs  

Словарь `perfLoggingPrefs` имеет следующий формат \(все ключи являются необязательными\).  

| Ключ | Тип | Значение по умолчанию | Сведения |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | положительное integer | 1000 | Запрашивается количество миллисекунд между событиями использования буфера трассировки DevTools.  Например, если 1000, то один раз в секунду DevTools сообщает, насколько заполнен буфер трассировки.  Если отчет указывает, что использование буфера составляет 100 %, выдано предупреждение. |  
| enableNetwork | логический | true | Сбор событий \(или не сбор\) из сетевого домена. |  
| enablePage | логический | true | Сбор событий \(или не сбор\) из домена Page. |  
| traceCategories | string | \(empty\) | Строка категорий трассировки Microsoft Edge, разделенных запятой, для которых следует собирать события трассировки.  Неустановленная или пустая строка отключает трассировку. |  

## Возвращенные возможности  

В следующем списке представлены все возможности Microsoft Edge, которые возвращаются при `EdgeDriver` создании нового сеанса.  

| Возможность | Тип | Сведения |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | Версия EdgeDriver. |  
| msedge.userDataDir | string | Путь к папке данных пользователя, используемой экземпляром Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Начало работы с удаленной отладки устройств с Windows 10 | Документы Майкрософт"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Выбор привязки языка WebDriver — WebDriver (Chromium) | Документы Майкрософт"
[WebdriverIndexDrivingMicrosoftEdgeChromium]: ./index.md#automating-microsoft-edge-chromium "Автоматизация Microsoft Edge (Chromium) — webDriver (Chromium) | Документы Майкрософт"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Установка Microsoft Edge (Chromium) — webDriver (Chromium) | Документы Майкрософт"  

[SeleniumMain]: https://www.selenium.dev "Автоматизация браузера SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Общие возможности | Документация по Selenium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Возможности : спецификации WebDriver | W3C"   
