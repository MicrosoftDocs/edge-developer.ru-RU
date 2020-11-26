---
description: Ссылка на возможности веб-дисководов и параметров, специфичных для Microsoft EDGE, которые поддерживаются EdgeDriver (Chromium).
title: Возможности и EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, HTML, CSS, сценарий JavaScript, разработчик, веб-дисковод, Selenium, тестирование, инструменты, Автоматизация и тестирование
ms.openlocfilehash: 1f6dca1b7ce3eb4fab3aaaab6450eee7cbf3eae5
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192257"
---
# Возможности и EdgeOptions  

Возможности: параметры, которые можно использовать для настройки и настройки `EdgeDriver` сеанса.  Чтобы начать `EdgeDriver` сеанс, перейдите в раздел Управление [Microsoft Edge][DrivingEdgeWebDriverIndex].  В этой статье описаны все поддерживаемые возможности [Microsoft Edge][DownloadEdgeWebDriverIndex] и дополнительные сведения о том, как передавать возможности в `EdgeDriver` сеанс.  

Языковые привязки для работы с дисками обеспечивают способы передачи возможностей `EdgeDriver` .  Точный механизм зависит от [выбранной вами языковой привязки][ChooseLanguageBindingWebDriverIndex].  В [Selenium][SeleniumMain]возможности обеспечиваются через `EdgeOptions` класс.  

## Использование класса EdgeOptions  

Создайте экземпляр `EdgeOptions` , который имеет удобные методы для настройки возможностей Microsoft Edge.  После того как вы настроили `EdgeOptions` объект, передайте ему `EdgeOptions` `EdgeDriver` конструктор.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Для возможностей, которые еще не имеют удобного метода, используйте `AddAdditionalCapability` метод.  Вам необходимо знать имя возможности и тип принимаемого ею значения.  Чтобы просмотреть полный список, перейдите на [объект EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Распознаваемые возможности  

Чтобы обеспечить поддержку стандартных возможностей `EdgeDriver` , перейдите к [документации Selenium][SharedCapabilitiesSeleniumDocumentation] и [стандарту консорциума W3C][CapabilitiesW3cWebdriver].  В этой статье перечислены только возможности, связанные с Microsoft Edge.  

## Объект EdgeOptions  

Большинство возможностей, специфичных для Microsoft EDGE, предоставляются через `EdgeOptions` объект.  В некоторых языках возможности реализуются `EdgeOptions` классом.  В других языках возможности хранятся в `ms:edgeOptions` словаре в `DesiredCapabilities` .  

| Возможность | Тип | Значение по умолчанию | Сведения |  
|:--- |:--- |:--- |:--- |  
| аргументы | список строк |  | Список аргументов командной строки, которые следует использовать при запуске Microsoft Edge.  Аргументы со связанными значениями должны быть разделены `=` знаком (например, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \).  |  
| код | string |  | Путь к двоичному файлу Microsoft Edge для использования \ (для macOS путь должен быть фактическим двоичным файлом, а не только приложением.  Например, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \).  |  
| MIME | список строк |  | Список расширений для установки при запуске.  Каждый элемент списка должен быть упакованным расширением (\) Base-64 Encoded `.crx` .  |  
| localState | dictionary |  | Словарь, в котором каждый элемент состоит из имени предпочтения и его значения.  Параметры применяются к локальному файлу состояния в папке User Data.  |  
| Prefs | dictionary |  | Словарь, в котором каждый элемент состоит из имени предпочтения и его значения.  Настройки применяются только к используемым профилям пользователей.  Например, перейдите к `Preferences` файлу в каталоге User Data (Microsoft EDGE).  |  
| Отсоединение | логическое значение | false | Если ложь, Microsoft Edge завершает работу по завершении `EdgeDriver` сеанса, вне зависимости от того, завершился ли сеанс.  При значении true Microsoft Edge завершает работу только в том случае, если сеанс завершен (или закрыт).  **Примечание**. Если установлено значение true, а сеанс не завершает работу, не `EdgeDriver` очищается временной каталог данных пользователя, используемый экземпляром Microsoft Edge.  |  
| debuggerAddress | string |  | Адрес сервера отладчика, к которому нужно подключиться, в форме <hostname/IP:> порта, например  `127.0.0.1:38947` .  |
| excludeSwitches | список строк |  | Список параметров командной строки Microsoft EDGE, которые позволяют исключить EdgeDriver по умолчанию при запуске Microsoft Edge.  Не следует использовать префиксы переключателей `--` .  |  
| minidumpPath | string |  | Каталог для хранения минидампа Microsoft Edge.  \ (Поддерживается только в Linux. \) |  
| mobileEmulation | dictionary |  | Словарь со значением `deviceName` или значениями для `deviceMetrics` and `userAgent` .  |  
| perfLoggingPrefs | dictionary |  | Необязательный словарь, задающий параметры ведения журнала производительности.  Дополнительные сведения можно найти в разделе [объект perfLoggingPrefs](#perfloggingprefs-object).  |  
| windowTypes | список строк |  | Список типов окон, отображаемых в списке оконных дескрипторов.  Чтобы получить доступ к элементам WebView Android, включите `webview` их в список.  |  
| wdpAddress | string |  | Адрес сервера портала устройств Windows, к которому вы подключаетесь, в форме `hostname/ip:port` , например  `127.0.0.1:50080` .  Дополнительные сведения можно найти в разделе [Удаленная отладка — устройства с Windows 10][DevtoolsRemoteDebuggingWindows].  |  
| wdpUsername | string |  | Необязательное имя пользователя, используемое при подключении к серверу портала устройств Windows.  Обязательно, если на сервере включена проверка подлинности.  |  
| wdpPassword | string |  | Необязательный пароль, который необходимо использовать при подключении к серверу портала устройств Windows.  Обязательно, если на сервере включена проверка подлинности.  |  
| windowsApp | string |  | ИДЕНТИФИКАТОР пользовательской модели приложения для запускаемого пакета приложения Microsoft EDGE, например `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Используйте `windowsApp` вместо `binary` подключения к устройству или эмулятору Windows 10X с помощью портала устройств Windows.  |  

## Объект perfLoggingPrefs  

`perfLoggingPrefs`Словарь имеет следующий формат \ (все клавиши являются необязательными \).  

| Ключ | Тип | Значение по умолчанию | Сведения |  
|:--- |:--- |:--- |:--- |  
| enableNetwork | логический | true | Для сбора данных о событиях \ (или не собирать) из сетевого домена.  |  
| enablePage | логический | true | Для сбора событий "\ (или не собирать") из домена страницы.  |  
| traceCategories | string | \ (пусто \) | Строка, разделенная запятыми, для категорий трассировки Microsoft EDGE, для которых нужно собрать события трассировки.  Неуказанная или пустая строка отключает трассировку.  |  
| bufferUsageReportingInterval | положительное целое число | 1000 | Указанное количество миллисекунд между событиями использования буфера трассировки DevTools.  Например, если 1000, а затем раз в секунду, DevTools сообщает, насколько заполнен буфер трассировки.  Если в отчете указано использование буфера 100%, выдается предупреждение.  |  

## Возвращенные возможности  

В следующем списке перечислены все возможности Microsoft EDGE, которые `EdgeDriver` возвращаются при создании нового сеанса.  

| Возможность | Тип | Сведения |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | Версия EdgeDriver. |  
| msedge.userDataDir | string | Путь к каталогу данных пользователя, используемому экземпляром Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Начало работы с удаленной отладкой на устройствах с Windows 10 | Документы Microsoft"  
[DrivingEdgeWebDriverIndex]: ./index.md#driving-microsoft-edge-chromium "Управление Microsoft EDGE (Chromium) | Документы Microsoft"    
[DownloadEdgeWebDriverIndex]: ./index.md#install-microsoft-edge-chromium "Установка Microsoft EDGE (Chromium) | Документы Microsoft"  
[ChooseLanguageBindingWebDriverIndex]: ./index.md#choose-a-webdriver-language-binding "Выбор языковой привязки для веб-дисков | Документы Microsoft"

[SeleniumMain]: https://www.selenium.dev "Автоматизация браузера SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Общие возможности | Selenium документация"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver/#capabilities "Возможности: спецификация для устройства PNG"   
