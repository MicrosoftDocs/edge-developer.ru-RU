---
description: Узнайте, как использовать родной обмен сообщениями для связи расширения с приложением UWP-компаньона.
title: Родной | Расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, native, messaging, uwp
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9a306055b8f86b92aa5c3e7cd6de44f2386307d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399360"
---
# <a name="native-messaging-in-microsoft-edge"></a>Родной обмен сообщениями в Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a>Обзор архитектуры родной системы обмена сообщениями  

С обновлением создателей Windows 10 расширения Microsoft Edge могут использовать родной обмен сообщениями для связи с приложением универсальной платформы Windows \(UWP\).  На высоком уровне расширения Microsoft Edge используют те же API для родных сообщений, что и расширения Chrome и Firefox.  Однако необходимо реализовать родной хост обмена сообщениями с помощью универсальной платформы Windows.  

> [!NOTE]
> Метод, описанный ниже \(подключение к приложению UWP с помощью AppService\) — это единственный поддерживаемый механизм, позволяющий поддерживать связь между расширениями Microsoft Edge и родными компонентами.  Дополнительные [сведения](#adding-a-desktop-bridge-component) о том, как включить связь с устаревшими компонентами Win32, см. в разделе Добавление компонента моста рабочего стола в этом руководстве.  

Архитектура обмена сообщениями в Microsoft Edge использует существующий API в качестве инфраструктуры меж процесса [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\).  Приложения UWP используют `AppService` API для взаимодействия друг с другом.  Благодаря этому расширения Microsoft Edge теперь могут взаимодействовать с приложениями UWP.  

![родной архитектуры обмена сообщениями](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a>Когда и когда не использовать родной обмен сообщениями  

Родной обмен сообщениями добавляет новый уровень в расширение.  Реализуя приложение-компаньон UWP для расширения, вам станут доступны следующие возможности:  

*   Синхронизация данных \(например учетных данных\) с приложением-компаньоном UWP.  
*   Реализация более прочных алгоритмов шифрования и расшифровки, недоступных в веб-API.  
*   Доступ к ресурсам, недоступным с помощью веб-интерфейсов API, например оборудования или USB-устройств.  

Существует несколько случаев, когда не следует использовать родной обмен сообщениями из-за ограничений безопасности или политики:  

*   Изменение параметров пользователя в Microsoft Edge или Windows, например изменение браузера по умолчанию или поставщика поиска.  
*   Действия, нарушающие политики Microsoft Store для приложений и расширений.  
*   Передача данных в удаленную конечную точку с помощью родного хоста сообщений.  
*   Разрешение другим приложениям скачивать контент, который изменяет поведение расширения.  

## <a name="demos"></a>Демонстрационные примеры  

Чтобы узнать, как выглядит родной удлинитель обмена сообщениями Microsoft Edge с приложением UWP и мостом для настольных компьютеров, ознакомьтесь с примерами [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) [и DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) в GitHub.  

### <a name="how-it-works"></a>Принцип работы  

Компонент расширения Microsoft Edge в примере использует сценарий контента, чтобы определить, когда пользователь введет информацию, которая должна быть зашифрована.  Расширение передает это компоненту Моста настольных компьютеров с помощью родных сообщений.  Когда пользователь будет готов к отправке данных, расширение возвращает зашифрованное значение обратно на веб-сайт.  

> [!NOTE]
> Этот пример будет работать только на веб-странице, которая использует настраиваемые события для связи со сценарием контента расширения.  Пример папки включает [файл .html для](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) проверки расширения.  

В этом примере приложение UWP используется для перенаправки ответов с моста настольных компьютеров в Microsoft Edge, который затем отправляется в расширение Microsoft Edge с помощью вызова.  Хотя в этом примере имеется родной хост обмена сообщениями в основном приложении, он также может работать в качестве фоновой задачи.  Переключение между ними требует редактирования фонового сценария расширения и изменения строки в `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` пределах .  

## <a name="chrome-vs-microsoft-edge-implementation"></a>Реализация Chrome vs Microsoft Edge  

В то время как Chrome использует API передачи сообщений для своих расширений для связи с приложениями, Microsoft Edge использует API, который теперь позволяет расширениям Microsoft Edge и приложениям [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) UWP общаться.  

В этом разделе подробно повеяна разница между тем, как Chrome и Microsoft Edge обрабатывают реализацию личных сообщений.  

### <a name="registration-and-host-manifest"></a>Манифест регистрации и хост  

Для того чтобы ваше приложение было признано вашим расширением в качестве родного хоста обмена сообщениями, его необходимо зарегистрировать.  

Для [регистрации хост-личных](https://developer.chrome.com/extensions/nativeMessaging) сообщений Chrome приложение должно установить файл манифеста в любой точке файловой системы Windows, определяющий конфигурацию родного хоста обмена сообщениями.  

Ниже приводится пример параметров файла config:  

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

Чтобы установить этот файл, приложению потребуется:  

1.  Зарегистрируйте файл манифеста в заранее определенном расположении в реестре, определяемом конфигурацией хостов:  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        or  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  Установите значение этого ключа по умолчанию для полного пути к файлу манифеста, например `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

Для Microsoft Edge, чтобы зарегистрировать \(родной хост обмена сообщениями\), необходимо включить приложение-компаньон UWP в тот же пакет, что и расширение, и указать расширение AppService в файле [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) `Package.appxmanifest` проекта.  Атрибуты `EntryPoint` `Name` и атрибуты могут быть настроены вами:  

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...   
    </Application>
</Applications>
```  

Также необходимо установить, какие расширения разрешены для подключения к службе.  Так как Microsoft Edge не имеет эквивалентного свойства манифеста в AppxManifest, это необходимо будет определять и применять во время запуска с помощью `"allowed_origins"` приложения UWP.  Так как Microsoft Edge устанавливает подключение от имени расширения, приложение ищет имя семейства пакетов вызываемого, чтобы определить, подключено ли расширение microsoft Edge для управления или проверки подлинности вызываемого.  Например:   

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```  

### <a name="message-sending"></a>Отправка сообщений  

Чтобы приложение и расширение общались друг с другом, сообщения должны отправляться в них и от них.  

Расширения Chrome инициируют сообщение с помощью API для доставки сообщения родному [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) хосту с помощью нестационарочного канала.  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

Первый параметр — это имя родного хоста, которое Chrome ищет в реестре манифеста.  Манифест указывает .exe, который Chrome запустит в песочнице, и сообщение отправляется с помощью std i/o.  
Расширения также устанавливают постоянный канал с помощью API, который принимает имя родного хоста `runtime.connectNative` как единственный параметр.  

Microsoft Edge использует ту же конструкцию, что и API для обмена сообщениями в Chrome, чтобы разрешить расширениям Microsoft Edge указывать, к какой службе приложений можно подключиться.  Первый параметр указывает `runtime.sendNativeMessage` имя службы приложения.  В разделе [Манифест регистрации и](#registration-and-host-manifest) хост-манифеста это `"com.microsoft.inventory"` .  Платформа расширения Microsoft Edge ограничивает родной хост обмена сообщениями приложением UWP, упакованным в том же AppX, что и расширение.  Это снижает все риски безопасности, связанные с вредоносными атаками, которые пытаются подключить Microsoft Edge к другому семейство пакетов путем фальсификации записей манифеста.  

Это означает, что Microsoft Edge будет использовать то же имя семейства пакетов, что и расширение, в дополнение к имени, указанному в API, для уникальной идентификации поставщика `AppService` службы приложений.  

> [!NOTE]
> Это не будет легко преобразовано в [microsoft Edge Extension набор средств](./porting-chrome-extensions.md).  Все расширения, указанные в разрешении, будут помечены как требующие `"nativeMessaging"` ручного преобразования для этого компонента.  

### <a name="communication-protocol"></a>Протокол связи  

Протокол связи для обмена сообщениями определяет форматирование сообщений перед отправкой.  

Chrome запускает каждый родной хост обмена сообщениями в отдельном процессе и взаимодействует с ним с помощью стандартных входных данных и стандартных выходных данных.  Один и тот же формат используется для отправки сообщений в обоих направлениях: каждое сообщение сериализируются с помощью JSON, UTF-8 закодированы и ему предшествует длина 32-битного сообщения в порядке родного byte.  

Для Microsoft Edge фоновое задание/основное приложение, которое реализует службу приложений, будет запущено платформой.  При запуске вызывается метод `Run` фоновой задачи:  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service is not stopped and ended.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

Когда расширение отправляет сообщение в приложение UWP, событие [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) будет поднято.  Затем это отформатифицированное сообщение JSON будет строкифицировано в первую пару объекта [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) KeyValue.  :  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

Когда приложение UWP отправляет ответ на расширение, объект будет [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) `ValueSet` добавлен.  Свойство будет игнорироваться Microsoft Edge, но свойство будет содержать `Key` `Value` допустимую строку JSON.  

### <a name="callback"></a>Callback  

Для ответных вызовов Chrome использует функцию вызова для обработки любых асинхронных ответов от [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) отправки сообщения.  

Microsoft Edge использует метод объекта, чтобы позволить приложению [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) отправить объект обратно в [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) расширение.  

### <a name="message-size-limit"></a>Ограничение размера сообщения  

Сообщения, которые отправляются между расширением и приложением, имеют различные ограничения размера сообщений для Chrome и Microsoft Edge.  

Chrome имеет следующие ограничения по размеру сообщений:  

*   Ограничение единого сообщения из родного хоста обмена сообщениями: 1 МБ  
*   Ограничение единого сообщения, отправленное в родной хост обмена сообщениями: 4 ГБ  

Для Microsoft Edge, несмотря на отсутствие ограничений по размеру сообщений \(зависит от памяти\), Microsoft Edge защищает себя от неправильного поведения местных приложений, вводя следующие ограничения размера `AppService` сообщения:  

*   Ограничение одного сообщения из приложения UWP в расширение: 1 МБ  
*   Ограничение одного сообщения от расширения до приложения UWP: 100 МБ  

### <a name="native-messaging-connections"></a>Родные подключения к обмена сообщениями  

Существует два типа подключений для родных сообщений; сохраняемая и неустанная.  
**Постоянное** подключение — это подключение, которое будет запущено до тех пор, пока порт не будет уничтожен.  **Нестандартное** подключение — это подключение, которое открывается для одного сообщения одновременно и закрывается после доставки.  

#### <a name="persistent"></a>Постоянные правила  

Для Chrome постоянное подключение создается с помощью порта обмена [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) сообщениями.  После создания порта Chrome запускает процесс родного хоста обмена сообщениями, который будет запущен до тех пор, пока порт не будет уничтожен.  

Для Microsoft Edge после создания порта обмена сообщениями microsoft Edge запускает его и продолжает работать до тех пор, пока порт `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) не будет уничтожен.  В следующем фрагменте показано, как установлено постоянное подключение из приложения UWP.  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a>Нестандартные  

Когда сообщение отправляется с помощью Chrome, не создавая порт обмена сообщениями, Chrome запускает новый процесс родного хоста обмена [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) сообщениями для каждого сообщения.  Первое сообщение, генерируемого процессом хост, обрабатывается как ответ на исходный запрос, а все остальные сообщения после его игнорирования.  

Microsoft Edge останавливает и завершает подключение после каждого ответа на каждое сообщение.  В следующем фрагменте показана нестандартная связь, которая устанавливается с этим, которая затем будет прекращена в приложении UWP после того, как запрос был получен и сохранен в `AppServiceConnection` качестве [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .  

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```  

### <a name="permission"></a>Разрешение  

Чтобы включить использование родных сообщений с расширением, для Chrome и Microsoft Edge необходимо объявить `"nativeMessaging"` разрешение в `manifest.json` файле.  

## <a name="app-services"></a>Услуги для приложений  

В этом разделе подробно сообщается о влиянии служб приложений на производительность и память родных сообщений Microsoft Edge.  

### <a name="performance"></a>Производительность  

Службы приложений "спонсируется" приложением переднего плана, которое вызывает их, которое для родных целей обмена сообщениями — Microsoft Edge.  Это означает, что службы приложений могут работать до тех пор, пока работает Microsoft Edge.  

Что касается задержки, службы приложений используют именные трубы, которые после начального подключения позволяют двум приложениям напрямую общаться.  Этот метод связи создает низкую задержку.  Устройства с медленными процессорами будут испытывать некоторые начальные задержки после запуска процесса, в котором размещена служба приложений \(~80ms для запуска фоновой задачи на некоторых устройствах\).  После запуска производительность на медленных устройствах ЦП должна быть хорошей.  

### <a name="memory"></a>Память  

Память, выделенная службе приложений, вымыта из квоты, выделенной Microsoft Edge.  Это означает, что если Microsoft Edge запускает слишком много служб приложений, существует вероятность того, что у них может не быть памяти.  Обычные ограничения фоновой памяти задач применяются в службах приложений.  Например, на устройстве с 512 МБ фоновая задача службы приложений может быть не более 16 МБ.  Это число по мере масштабирования устройств.  

## <a name="creating-an-extension-with-native-messaging"></a>Создание расширения с помощью родных сообщений  

Чтобы протестировать родной обмен сообщениями, вашему расширению необходимо имя семейства пакетов.  Microsoft Edge использует это для определения удостоверения родного носителя сообщения, что означает, что расширение должно быть упаковано.  

Чтобы создать расширение с помощью родных сообщений в Visual Studio:  

1.  Создание проекта UWP в Visual Studio.  
1.  [Добавьте `AppService` в приложение UWP](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).  
    *   Вы можете дополнительно настроить для [ `AppService` хозяйского хозяйского](/windows/uwp/launch-resume/convert-app-service-in-process) приложения, а не в качестве фоновой задачи на данном этапе.  
1.  Сборка и тестирование проекта UWP.  
    *   Можно дополнительно добавить компонент [Моста настольных компьютеров.](#adding-a-desktop-bridge-component)  
1.  Создайте расширение Microsoft Edge, которое использует родной обмен сообщениями для связи с приложением-компаньоном UWP.  Файлы расширения можно добавить в папку с именем `Extension` в проекте UWP.  Все файлы под этой папкой, в том числе подмостки, должны иметь свои свойства настроены таким `Build Action=Content` образом, что и `Copy to Output Directory=Copy Always` .  `manifest.json`Убедитесь, что также настроены с этими свойствами.  
1.  Измените файл в проекте, чтобы включить метаданные расширения и преобразовать его в `package.manifest.xml` безголовые приложения, `AppListEntry="none"` добавив:  
    
    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">
    
    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>
       
       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```  
    
1.  Используйте `AppService` имя, настроенное для UWP, в API для обмена сообщениями.  
1.  Сборка [и развертывание](#deploying) проекта UWP \(с необязательным компонентом Моста настольных компьютеров\).  
1.  [Пакет](#packaging) вашего родного расширения обмена сообщениями после его готовности к отправке в Магазин  
    
> [!NOTE]
> Ссылка на [раздел Demos](#demos) для примера полного расширения родных сообщений.  

## <a name="adding-a-desktop-bridge-component"></a>Добавление компонента моста рабочего стола  

Если вы хотите добавить компонент Моста настольных компьютеров в пакет, необходимо создать и построить проект Win32 в Visual Studio.  Сведения о преобразовании приложения win32 в UWP см. в сведениях о переносе приложений в [Windows 10 с помощью моста настольных компьютеров.](/windows/uwp/porting/desktop-to-uwp-root)  После Visual Studio в пакет можно добавить исполняемый win32, делая следующие действия:  

1.  Добавьте проект Win32 в то же решение, что и проект UWP.  
1.  Установите проект Win32 в качестве зависимого проекта для проекта UWP:  
    
    ![настройка зависимостей проекта](../media/project-dependencies.png)  
    
1.  Создание `Win32` папки в проекте UWP.  Скопируйте необходимые для проекта `Win32` раздвители в эту папку.  Настройка свойств всех бинарей, таких, что `Build Action=Content` и `Copy to Output Directory=Copy Always` .  
    
    ![папка с файлами приложений win32 и UWP в ней](../media/desktop-bridge.png)  
    
1.  Измените файл проекта UWP, чтобы скопировать все необходимые файлы для проекта в эту папку `Win32` с помощью команды событий PostBuild.  Это гарантирует, что обновленные биналоги копируется в папку каждый раз при восстановлении решения.  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  `package.manifest.xml`Измените, `<desktop:Extension>` добавив элемент в `<Extensions>` элемент:  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a>Развертывание  

После настройки проекта UWP \(и необязательно Win32 project\) как описано выше, вы будете готовы развернуть решение с помощью Visual Studio.  

![создание проекта inprocess](../media/native-message-uwp-debug.png)  

После правильного развертывания решения необходимо увидеть расширение в Microsoft Edge.  

![расширение, показывающаяся в Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a>Создание пакетов  

> [!NOTE]
> Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.  [Отправьте запрос](https://developer.microsoft.com/microsoft-edge/extensions/requests/) на участие в Microsoft Store и рассматривайте его для будущих обновлений.  

Вы можете создать пакет Store для отправки в Центр разработчиков Windows с помощью встроенных Visual Studio функций:  

![Создание пакета Store](../media/create-store-package.png)  

## <a name="debugging"></a>Отладка  

Инструкции по отладки различаются в зависимости от того, какой компонент необходимо протестировать:  

### <a name="debugging-the-extension"></a>Отладка расширения  

После развертывания решения расширение будет установлено в Microsoft Edge.  Сведения о [](./debugging-extensions.md) том, как отладить расширение, ознакомьтесь с руководством по отладки.  

### <a name="debugging-the-uwp-app"></a>Отладка приложения UWP  

Приложение UWP запустится, когда расширение попытается подключиться к ней с [помощью](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)API обмена сообщениями.  Отламываю приложение UWP только после начала процесса.  Это может быть настроено с помощью страницы Свойства проекта:  

1.  В Visual Studio наведите курсор на проект приложения UWP и откройте контекстное меню \(правой кнопкой мыши\)  
1.  Выбор **свойств**  
1.  Check **Do not launch, but debug my code when it starts**  
    
    ![выбор не запускать поле](../media/native-message-do-not-launch.png)  
    
В Visual Studio теперь можно установить точки разлома в коде, где нужно отладить, а затем запустить отладка, нажав F5.  После взаимодействия с расширением для подключения к приложению UWP Visual Studio автоматически подключается к процессу.  

### <a name="debugging-the-desktop-bridge"></a>Отладка моста настольных компьютеров  

Несмотря на то, что существуют различные методы отладки настольного моста [](/windows/msix/desktop/desktop-to-uwp-debug) \(преобразованное приложение Win32\), единственным применимым для этого сценария является вариант PLMDebug.  Вы также можете добавить код отладки в функцию запуска, чтобы выполнить ожидание в течение определенного времени, что позволяет Visual Studio к процессу.  
