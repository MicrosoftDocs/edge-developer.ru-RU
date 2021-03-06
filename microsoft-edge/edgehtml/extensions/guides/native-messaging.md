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
# <a name="native-messaging-in-microsoft-edge"></a><span data-ttu-id="88f03-104">Родной обмен сообщениями в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="88f03-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a><span data-ttu-id="88f03-105">Обзор архитектуры родной системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="88f03-105">Native messaging architecture overview</span></span>  

<span data-ttu-id="88f03-106">С обновлением создателей Windows 10 расширения Microsoft Edge могут использовать родной обмен сообщениями для связи с приложением универсальной платформы Windows \(UWP\).</span><span class="sxs-lookup"><span data-stu-id="88f03-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform \(UWP\) app.</span></span>  <span data-ttu-id="88f03-107">На высоком уровне расширения Microsoft Edge используют те же API для родных сообщений, что и расширения Chrome и Firefox.</span><span class="sxs-lookup"><span data-stu-id="88f03-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span>  <span data-ttu-id="88f03-108">Однако необходимо реализовать родной хост обмена сообщениями с помощью универсальной платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="88f03-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>  

> [!NOTE]
> <span data-ttu-id="88f03-109">Метод, описанный ниже \(подключение к приложению UWP с помощью AppService\) — это единственный поддерживаемый механизм, позволяющий поддерживать связь между расширениями Microsoft Edge и родными компонентами.</span><span class="sxs-lookup"><span data-stu-id="88f03-109">The method outlined below \(connecting to a UWP app via AppService\) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span>  <span data-ttu-id="88f03-110">Дополнительные [сведения](#adding-a-desktop-bridge-component) о том, как включить связь с устаревшими компонентами Win32, см. в разделе Добавление компонента моста рабочего стола в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="88f03-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span>  

<span data-ttu-id="88f03-111">Архитектура обмена сообщениями в Microsoft Edge использует существующий API в качестве инфраструктуры меж процесса [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\).</span><span class="sxs-lookup"><span data-stu-id="88f03-111">The native messaging architecture in Microsoft Edge leverages the existing [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API as the underlying inter-process communication \(IPC\) infrastructure.</span></span>  <span data-ttu-id="88f03-112">Приложения UWP используют `AppService` API для взаимодействия друг с другом.</span><span class="sxs-lookup"><span data-stu-id="88f03-112">UWP apps use the `AppService` API to communicate with one another.</span></span>  <span data-ttu-id="88f03-113">Благодаря этому расширения Microsoft Edge теперь могут взаимодействовать с приложениями UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-113">Because of this, Microsoft Edge extensions are now able to communicate with UWP apps.</span></span>  

![родной архитектуры обмена сообщениями](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a><span data-ttu-id="88f03-115">Когда и когда не использовать родной обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="88f03-115">When and when not to use native messaging</span></span>  

<span data-ttu-id="88f03-116">Родной обмен сообщениями добавляет новый уровень в расширение.</span><span class="sxs-lookup"><span data-stu-id="88f03-116">Native messaging adds a whole new layer to your extension.</span></span>  <span data-ttu-id="88f03-117">Реализуя приложение-компаньон UWP для расширения, вам станут доступны следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="88f03-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>  

*   <span data-ttu-id="88f03-118">Синхронизация данных \(например учетных данных\) с приложением-компаньоном UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-118">Synchronize data \(for example credentials\) with a companion UWP app.</span></span>  
*   <span data-ttu-id="88f03-119">Реализация более прочных алгоритмов шифрования и расшифровки, недоступных в веб-API.</span><span class="sxs-lookup"><span data-stu-id="88f03-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>  
*   <span data-ttu-id="88f03-120">Доступ к ресурсам, недоступным с помощью веб-интерфейсов API, например оборудования или USB-устройств.</span><span class="sxs-lookup"><span data-stu-id="88f03-120">Access resources that are not accessible through web APIs, for example hardware or USB devices</span></span>  

<span data-ttu-id="88f03-121">Существует несколько случаев, когда не следует использовать родной обмен сообщениями из-за ограничений безопасности или политики:</span><span class="sxs-lookup"><span data-stu-id="88f03-121">There are a few instances where native messaging should not be used due to security or policy restrictions:</span></span>  

*   <span data-ttu-id="88f03-122">Изменение параметров пользователя в Microsoft Edge или Windows, например изменение браузера по умолчанию или поставщика поиска.</span><span class="sxs-lookup"><span data-stu-id="88f03-122">Modifying user settings in either Microsoft Edge or Windows, for example changing the default browser or search provider.</span></span>  
*   <span data-ttu-id="88f03-123">Действия, нарушающие политики Microsoft Store для приложений и расширений.</span><span class="sxs-lookup"><span data-stu-id="88f03-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>  
*   <span data-ttu-id="88f03-124">Передача данных в удаленную конечную точку с помощью родного хоста сообщений.</span><span class="sxs-lookup"><span data-stu-id="88f03-124">Transferring data to remote endpoint via native message host.</span></span>  
*   <span data-ttu-id="88f03-125">Разрешение другим приложениям скачивать контент, который изменяет поведение расширения.</span><span class="sxs-lookup"><span data-stu-id="88f03-125">Allowing other apps to download content that changes extension behavior.</span></span>  

## <a name="demos"></a><span data-ttu-id="88f03-126">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="88f03-126">Demos</span></span>  

<span data-ttu-id="88f03-127">Чтобы узнать, как выглядит родной удлинитель обмена сообщениями Microsoft Edge с приложением UWP и мостом для настольных компьютеров, ознакомьтесь с примерами [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) [и DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) в GitHub.</span><span class="sxs-lookup"><span data-stu-id="88f03-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>  

### <a name="how-it-works"></a><span data-ttu-id="88f03-128">Принцип работы</span><span class="sxs-lookup"><span data-stu-id="88f03-128">How it works</span></span>  

<span data-ttu-id="88f03-129">Компонент расширения Microsoft Edge в примере использует сценарий контента, чтобы определить, когда пользователь введет информацию, которая должна быть зашифрована.</span><span class="sxs-lookup"><span data-stu-id="88f03-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span>  <span data-ttu-id="88f03-130">Расширение передает это компоненту Моста настольных компьютеров с помощью родных сообщений.</span><span class="sxs-lookup"><span data-stu-id="88f03-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span>  <span data-ttu-id="88f03-131">Когда пользователь будет готов к отправке данных, расширение возвращает зашифрованное значение обратно на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="88f03-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>  

> [!NOTE]
> <span data-ttu-id="88f03-132">Этот пример будет работать только на веб-странице, которая использует настраиваемые события для связи со сценарием контента расширения.</span><span class="sxs-lookup"><span data-stu-id="88f03-132">This sample will only work on a webpage that uses custom events to communicate with the content script of the extension.</span></span>  <span data-ttu-id="88f03-133">Пример папки включает [файл .html для](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) проверки расширения.</span><span class="sxs-lookup"><span data-stu-id="88f03-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>  

<span data-ttu-id="88f03-134">В этом примере приложение UWP используется для перенаправки ответов с моста настольных компьютеров в Microsoft Edge, который затем отправляется в расширение Microsoft Edge с помощью вызова.</span><span class="sxs-lookup"><span data-stu-id="88f03-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span>  <span data-ttu-id="88f03-135">Хотя в этом примере имеется родной хост обмена сообщениями в основном приложении, он также может работать в качестве фоновой задачи.</span><span class="sxs-lookup"><span data-stu-id="88f03-135">While this example has the native messaging host run in the main app, it is also able to run as a background task.</span></span>  <span data-ttu-id="88f03-136">Переключение между ними требует редактирования фонового сценария расширения и изменения строки в `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` `"NativeMessagingHostOutOfProcess"` пределах .</span><span class="sxs-lookup"><span data-stu-id="88f03-136">Switching between the two requires editing the background script of the extension, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>  

## <a name="chrome-vs-microsoft-edge-implementation"></a><span data-ttu-id="88f03-137">Реализация Chrome vs Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="88f03-137">Chrome vs Microsoft Edge implementation</span></span>  

<span data-ttu-id="88f03-138">В то время как Chrome использует API передачи сообщений для своих расширений для связи с приложениями, Microsoft Edge использует API, который теперь позволяет расширениям Microsoft Edge и приложениям [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) UWP общаться.</span><span class="sxs-lookup"><span data-stu-id="88f03-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>  

<span data-ttu-id="88f03-139">В этом разделе подробно повеяна разница между тем, как Chrome и Microsoft Edge обрабатывают реализацию личных сообщений.</span><span class="sxs-lookup"><span data-stu-id="88f03-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>  

### <a name="registration-and-host-manifest"></a><span data-ttu-id="88f03-140">Манифест регистрации и хост</span><span class="sxs-lookup"><span data-stu-id="88f03-140">Registration and host manifest</span></span>  

<span data-ttu-id="88f03-141">Для того чтобы ваше приложение было признано вашим расширением в качестве родного хоста обмена сообщениями, его необходимо зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="88f03-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>  

<span data-ttu-id="88f03-142">Для [регистрации хост-личных](https://developer.chrome.com/extensions/nativeMessaging) сообщений Chrome приложение должно установить файл манифеста в любой точке файловой системы Windows, определяющий конфигурацию родного хоста обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="88f03-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>  

<span data-ttu-id="88f03-143">Ниже приводится пример параметров файла config:</span><span class="sxs-lookup"><span data-stu-id="88f03-143">The following JSON is an example of settings for the config file:</span></span>  

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

<span data-ttu-id="88f03-144">Чтобы установить этот файл, приложению потребуется:</span><span class="sxs-lookup"><span data-stu-id="88f03-144">To install this file, the app would need to:</span></span>  

1.  <span data-ttu-id="88f03-145">Зарегистрируйте файл манифеста в заранее определенном расположении в реестре, определяемом конфигурацией хостов:</span><span class="sxs-lookup"><span data-stu-id="88f03-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        <span data-ttu-id="88f03-146">or</span><span class="sxs-lookup"><span data-stu-id="88f03-146">or</span></span>  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  <span data-ttu-id="88f03-147">Установите значение этого ключа по умолчанию для полного пути к файлу манифеста, например</span><span class="sxs-lookup"><span data-stu-id="88f03-147">Set the default value of that key to the full path to the manifest file, for example</span></span> `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

<span data-ttu-id="88f03-148">Для Microsoft Edge, чтобы зарегистрировать \(родной хост обмена сообщениями\), необходимо включить приложение-компаньон UWP в тот же пакет, что и расширение, и указать расширение AppService в файле [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) `Package.appxmanifest` проекта.</span><span class="sxs-lookup"><span data-stu-id="88f03-148">For Microsoft Edge, in order to register an [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(native messaging host\) you must include the UWP companion app in the same package as your extension and specify the [AppService extension](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in the `Package.appxmanifest` file of your project.</span></span>  <span data-ttu-id="88f03-149">Атрибуты `EntryPoint` `Name` и атрибуты могут быть настроены вами:</span><span class="sxs-lookup"><span data-stu-id="88f03-149">The `EntryPoint` and `Name` attributes may be configured by you:</span></span>  

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

<span data-ttu-id="88f03-150">Также необходимо установить, какие расширения разрешены для подключения к службе.</span><span class="sxs-lookup"><span data-stu-id="88f03-150">You also need to set which extensions are allowed to connect to the service.</span></span>  <span data-ttu-id="88f03-151">Так как Microsoft Edge не имеет эквивалентного свойства манифеста в AppxManifest, это необходимо будет определять и применять во время запуска с помощью `"allowed_origins"` приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-151">Because Microsoft Edge does not have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span>  <span data-ttu-id="88f03-152">Так как Microsoft Edge устанавливает подключение от имени расширения, приложение ищет имя семейства пакетов вызываемого, чтобы определить, подключено ли расширение microsoft Edge для управления или проверки подлинности вызываемого.</span><span class="sxs-lookup"><span data-stu-id="88f03-152">Since Microsoft Edge establishes the connection on behalf of the extension, the app looks up the Package Family Name of the caller to determine if extension is being connected by Microsoft Edge to control or authenticate the caller.</span></span>  <span data-ttu-id="88f03-153">Например:</span><span class="sxs-lookup"><span data-stu-id="88f03-153">For example</span></span>   

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

### <a name="message-sending"></a><span data-ttu-id="88f03-154">Отправка сообщений</span><span class="sxs-lookup"><span data-stu-id="88f03-154">Message sending</span></span>  

<span data-ttu-id="88f03-155">Чтобы приложение и расширение общались друг с другом, сообщения должны отправляться в них и от них.</span><span class="sxs-lookup"><span data-stu-id="88f03-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>  

<span data-ttu-id="88f03-156">Расширения Chrome инициируют сообщение с помощью API для доставки сообщения родному [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) хосту с помощью нестационарочного канала.</span><span class="sxs-lookup"><span data-stu-id="88f03-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span>  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="88f03-157">Первый параметр — это имя родного хоста, которое Chrome ищет в реестре манифеста.</span><span class="sxs-lookup"><span data-stu-id="88f03-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span>  <span data-ttu-id="88f03-158">Манифест указывает .exe, который Chrome запустит в песочнице, и сообщение отправляется с помощью std i/o.</span><span class="sxs-lookup"><span data-stu-id="88f03-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span>  
<span data-ttu-id="88f03-159">Расширения также устанавливают постоянный канал с помощью API, который принимает имя родного хоста `runtime.connectNative` как единственный параметр.</span><span class="sxs-lookup"><span data-stu-id="88f03-159">Extensions also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span>  

<span data-ttu-id="88f03-160">Microsoft Edge использует ту же конструкцию, что и API для обмена сообщениями в Chrome, чтобы разрешить расширениям Microsoft Edge указывать, к какой службе приложений можно подключиться.</span><span class="sxs-lookup"><span data-stu-id="88f03-160">Microsoft Edge uses the same construct as the native messaging API in Chrome to allow Microsoft Edge extensions to specify which app service to connect to.</span></span>  <span data-ttu-id="88f03-161">Первый параметр указывает `runtime.sendNativeMessage` имя службы приложения.</span><span class="sxs-lookup"><span data-stu-id="88f03-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span>  <span data-ttu-id="88f03-162">В разделе [Манифест регистрации и](#registration-and-host-manifest) хост-манифеста это `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="88f03-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span>  <span data-ttu-id="88f03-163">Платформа расширения Microsoft Edge ограничивает родной хост обмена сообщениями приложением UWP, упакованным в том же AppX, что и расширение.</span><span class="sxs-lookup"><span data-stu-id="88f03-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span>  <span data-ttu-id="88f03-164">Это снижает все риски безопасности, связанные с вредоносными атаками, которые пытаются подключить Microsoft Edge к другому семейство пакетов путем фальсификации записей манифеста.</span><span class="sxs-lookup"><span data-stu-id="88f03-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span>  

<span data-ttu-id="88f03-165">Это означает, что Microsoft Edge будет использовать то же имя семейства пакетов, что и расширение, в дополнение к имени, указанному в API, для уникальной идентификации поставщика `AppService` службы приложений.</span><span class="sxs-lookup"><span data-stu-id="88f03-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="88f03-166">Это не будет легко преобразовано в [microsoft Edge Extension набор средств](./porting-chrome-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="88f03-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span>  <span data-ttu-id="88f03-167">Все расширения, указанные в разрешении, будут помечены как требующие `"nativeMessaging"` ручного преобразования для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="88f03-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>  

### <a name="communication-protocol"></a><span data-ttu-id="88f03-168">Протокол связи</span><span class="sxs-lookup"><span data-stu-id="88f03-168">Communication protocol</span></span>  

<span data-ttu-id="88f03-169">Протокол связи для обмена сообщениями определяет форматирование сообщений перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="88f03-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>  

<span data-ttu-id="88f03-170">Chrome запускает каждый родной хост обмена сообщениями в отдельном процессе и взаимодействует с ним с помощью стандартных входных данных и стандартных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="88f03-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span>  <span data-ttu-id="88f03-171">Один и тот же формат используется для отправки сообщений в обоих направлениях: каждое сообщение сериализируются с помощью JSON, UTF-8 закодированы и ему предшествует длина 32-битного сообщения в порядке родного byte.</span><span class="sxs-lookup"><span data-stu-id="88f03-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>  

<span data-ttu-id="88f03-172">Для Microsoft Edge фоновое задание/основное приложение, которое реализует службу приложений, будет запущено платформой.</span><span class="sxs-lookup"><span data-stu-id="88f03-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span>  <span data-ttu-id="88f03-173">При запуске вызывается метод `Run` фоновой задачи:</span><span class="sxs-lookup"><span data-stu-id="88f03-173">On startup, the `Run` method of the background task is invoked:</span></span>  

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

<span data-ttu-id="88f03-174">Когда расширение отправляет сообщение в приложение UWP, событие [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) будет поднято.</span><span class="sxs-lookup"><span data-stu-id="88f03-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) event will be raised.</span></span>  <span data-ttu-id="88f03-175">Затем это отформатифицированное сообщение JSON будет строкифицировано в первую пару объекта [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) KeyValue.</span><span class="sxs-lookup"><span data-stu-id="88f03-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object.</span></span>  <span data-ttu-id="88f03-176">:</span><span class="sxs-lookup"><span data-stu-id="88f03-176">:</span></span>  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="88f03-177">Когда приложение UWP отправляет ответ на расширение, объект будет [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) `ValueSet` добавлен.</span><span class="sxs-lookup"><span data-stu-id="88f03-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) will be added to the `ValueSet` object.</span></span>  <span data-ttu-id="88f03-178">Свойство будет игнорироваться Microsoft Edge, но свойство будет содержать `Key` `Value` допустимую строку JSON.</span><span class="sxs-lookup"><span data-stu-id="88f03-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>  

### <a name="callback"></a><span data-ttu-id="88f03-179">Callback</span><span class="sxs-lookup"><span data-stu-id="88f03-179">Callback</span></span>  

<span data-ttu-id="88f03-180">Для ответных вызовов Chrome использует функцию вызова для обработки любых асинхронных ответов от [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="88f03-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>  

<span data-ttu-id="88f03-181">Microsoft Edge использует метод объекта, чтобы позволить приложению [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) отправить объект обратно в [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) расширение.</span><span class="sxs-lookup"><span data-stu-id="88f03-181">Microsoft Edge uses the [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) method  of the [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) object to let the app send a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object back to the extension.</span></span>  

### <a name="message-size-limit"></a><span data-ttu-id="88f03-182">Ограничение размера сообщения</span><span class="sxs-lookup"><span data-stu-id="88f03-182">Message size limit</span></span>  

<span data-ttu-id="88f03-183">Сообщения, которые отправляются между расширением и приложением, имеют различные ограничения размера сообщений для Chrome и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>  

<span data-ttu-id="88f03-184">Chrome имеет следующие ограничения по размеру сообщений:</span><span class="sxs-lookup"><span data-stu-id="88f03-184">Chrome has the following message size limitations:</span></span>  

*   <span data-ttu-id="88f03-185">Ограничение единого сообщения из родного хоста обмена сообщениями: 1 МБ</span><span class="sxs-lookup"><span data-stu-id="88f03-185">Single message limit from native messaging host:  1 MB</span></span>  
*   <span data-ttu-id="88f03-186">Ограничение единого сообщения, отправленное в родной хост обмена сообщениями: 4 ГБ</span><span class="sxs-lookup"><span data-stu-id="88f03-186">Single message limit sent to native messaging host:  4 GB</span></span>  

<span data-ttu-id="88f03-187">Для Microsoft Edge, несмотря на отсутствие ограничений по размеру сообщений \(зависит от памяти\), Microsoft Edge защищает себя от неправильного поведения местных приложений, вводя следующие ограничения размера `AppService` сообщения:</span><span class="sxs-lookup"><span data-stu-id="88f03-187">For Microsoft Edge, while `AppService` has no limit on message size \(dependent on memory\), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>  

*   <span data-ttu-id="88f03-188">Ограничение одного сообщения из приложения UWP в расширение: 1 МБ</span><span class="sxs-lookup"><span data-stu-id="88f03-188">Single message limit from UWP app to extension: 1 MB</span></span>  
*   <span data-ttu-id="88f03-189">Ограничение одного сообщения от расширения до приложения UWP: 100 МБ</span><span class="sxs-lookup"><span data-stu-id="88f03-189">Single message limit from extension to UWP app: 100 MB</span></span>  

### <a name="native-messaging-connections"></a><span data-ttu-id="88f03-190">Родные подключения к обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="88f03-190">Native messaging connections</span></span>  

<span data-ttu-id="88f03-191">Существует два типа подключений для родных сообщений; сохраняемая и неустанная.</span><span class="sxs-lookup"><span data-stu-id="88f03-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>  
<span data-ttu-id="88f03-192">**Постоянное** подключение — это подключение, которое будет запущено до тех пор, пока порт не будет уничтожен.</span><span class="sxs-lookup"><span data-stu-id="88f03-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span>  <span data-ttu-id="88f03-193">**Нестандартное** подключение — это подключение, которое открывается для одного сообщения одновременно и закрывается после доставки.</span><span class="sxs-lookup"><span data-stu-id="88f03-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>  

#### <a name="persistent"></a><span data-ttu-id="88f03-194">Постоянные правила</span><span class="sxs-lookup"><span data-stu-id="88f03-194">Persistent</span></span>  

<span data-ttu-id="88f03-195">Для Chrome постоянное подключение создается с помощью порта обмена [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) сообщениями.</span><span class="sxs-lookup"><span data-stu-id="88f03-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="88f03-196">После создания порта Chrome запускает процесс родного хоста обмена сообщениями, который будет запущен до тех пор, пока порт не будет уничтожен.</span><span class="sxs-lookup"><span data-stu-id="88f03-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>  

<span data-ttu-id="88f03-197">Для Microsoft Edge после создания порта обмена сообщениями microsoft Edge запускает его и продолжает работать до тех пор, пока порт `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) не будет уничтожен.</span><span class="sxs-lookup"><span data-stu-id="88f03-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) and keeps it running until the port is destroyed.</span></span>  <span data-ttu-id="88f03-198">В следующем фрагменте показано, как установлено постоянное подключение из приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span>  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a><span data-ttu-id="88f03-199">Нестандартные</span><span class="sxs-lookup"><span data-stu-id="88f03-199">Non-persistent</span></span>  

<span data-ttu-id="88f03-200">Когда сообщение отправляется с помощью Chrome, не создавая порт обмена сообщениями, Chrome запускает новый процесс родного хоста обмена [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) сообщениями для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="88f03-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span>  <span data-ttu-id="88f03-201">Первое сообщение, генерируемого процессом хост, обрабатывается как ответ на исходный запрос, а все остальные сообщения после его игнорирования.</span><span class="sxs-lookup"><span data-stu-id="88f03-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>  

<span data-ttu-id="88f03-202">Microsoft Edge останавливает и завершает подключение после каждого ответа на каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="88f03-202">Microsoft Edge stops and ends the connection after every response to each message has been received.</span></span>  <span data-ttu-id="88f03-203">В следующем фрагменте показана нестандартная связь, которая устанавливается с этим, которая затем будет прекращена в приложении UWP после того, как запрос был получен и сохранен в `AppServiceConnection` качестве [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="88f03-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true).</span></span>  

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

### <a name="permission"></a><span data-ttu-id="88f03-204">Разрешение</span><span class="sxs-lookup"><span data-stu-id="88f03-204">Permission</span></span>  

<span data-ttu-id="88f03-205">Чтобы включить использование родных сообщений с расширением, для Chrome и Microsoft Edge необходимо объявить `"nativeMessaging"` разрешение в `manifest.json` файле.</span><span class="sxs-lookup"><span data-stu-id="88f03-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you must declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>  

## <a name="app-services"></a><span data-ttu-id="88f03-206">Услуги для приложений</span><span class="sxs-lookup"><span data-stu-id="88f03-206">App services</span></span>  

<span data-ttu-id="88f03-207">В этом разделе подробно сообщается о влиянии служб приложений на производительность и память родных сообщений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>  

### <a name="performance"></a><span data-ttu-id="88f03-208">Производительность</span><span class="sxs-lookup"><span data-stu-id="88f03-208">Performance</span></span>  

<span data-ttu-id="88f03-209">Службы приложений "спонсируется" приложением переднего плана, которое вызывает их, которое для родных целей обмена сообщениями — Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span>  <span data-ttu-id="88f03-210">Это означает, что службы приложений могут работать до тех пор, пока работает Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-210">This means that app services can run as long as Microsoft Edge is running.</span></span>  

<span data-ttu-id="88f03-211">Что касается задержки, службы приложений используют именные трубы, которые после начального подключения позволяют двум приложениям напрямую общаться.</span><span class="sxs-lookup"><span data-stu-id="88f03-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span>  <span data-ttu-id="88f03-212">Этот метод связи создает низкую задержку.</span><span class="sxs-lookup"><span data-stu-id="88f03-212">This method of communication produces low latency.</span></span>  <span data-ttu-id="88f03-213">Устройства с медленными процессорами будут испытывать некоторые начальные задержки после запуска процесса, в котором размещена служба приложений \(~80ms для запуска фоновой задачи на некоторых устройствах\).</span><span class="sxs-lookup"><span data-stu-id="88f03-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service \(~80ms to startup the background task on some devices\).</span></span>  <span data-ttu-id="88f03-214">После запуска производительность на медленных устройствах ЦП должна быть хорошей.</span><span class="sxs-lookup"><span data-stu-id="88f03-214">After start-up, performance on slow CPU devices should be good.</span></span>  

### <a name="memory"></a><span data-ttu-id="88f03-215">Память</span><span class="sxs-lookup"><span data-stu-id="88f03-215">Memory</span></span>  

<span data-ttu-id="88f03-216">Память, выделенная службе приложений, вымыта из квоты, выделенной Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span>  <span data-ttu-id="88f03-217">Это означает, что если Microsoft Edge запускает слишком много служб приложений, существует вероятность того, что у них может не быть памяти.</span><span class="sxs-lookup"><span data-stu-id="88f03-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span>  <span data-ttu-id="88f03-218">Обычные ограничения фоновой памяти задач применяются в службах приложений.</span><span class="sxs-lookup"><span data-stu-id="88f03-218">The usual background task memory caps are enforced on app services.</span></span>  <span data-ttu-id="88f03-219">Например, на устройстве с 512 МБ фоновая задача службы приложений может быть не более 16 МБ.</span><span class="sxs-lookup"><span data-stu-id="88f03-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span>  <span data-ttu-id="88f03-220">Это число по мере масштабирования устройств.</span><span class="sxs-lookup"><span data-stu-id="88f03-220">This number goes up as the devices scale up.</span></span>  

## <a name="creating-an-extension-with-native-messaging"></a><span data-ttu-id="88f03-221">Создание расширения с помощью родных сообщений</span><span class="sxs-lookup"><span data-stu-id="88f03-221">Creating an extension with native messaging</span></span>  

<span data-ttu-id="88f03-222">Чтобы протестировать родной обмен сообщениями, вашему расширению необходимо имя семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="88f03-222">In order to test native messaging, your extension needs a Package Family Name.</span></span>  <span data-ttu-id="88f03-223">Microsoft Edge использует это для определения удостоверения родного носителя сообщения, что означает, что расширение должно быть упаковано.</span><span class="sxs-lookup"><span data-stu-id="88f03-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span>  

<span data-ttu-id="88f03-224">Чтобы создать расширение с помощью родных сообщений в Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="88f03-224">To create your extension with native messaging in Visual Studio:</span></span>  

1.  <span data-ttu-id="88f03-225">Создание проекта UWP в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="88f03-225">Create a UWP project in Visual Studio.</span></span>  
1.  <span data-ttu-id="88f03-226">[Добавьте `AppService` в приложение UWP](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="88f03-226">[Add `AppService` to your UWP app](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>  
    *   <span data-ttu-id="88f03-227">Вы можете дополнительно настроить для [ `AppService` хозяйского хозяйского](/windows/uwp/launch-resume/convert-app-service-in-process) приложения, а не в качестве фоновой задачи на данном этапе.</span><span class="sxs-lookup"><span data-stu-id="88f03-227">You can optionally [configure `AppService` to be hosted in the main app](/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>  
1.  <span data-ttu-id="88f03-228">Сборка и тестирование проекта UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-228">Build and test your UWP project.</span></span>  
    *   <span data-ttu-id="88f03-229">Можно дополнительно добавить компонент [Моста настольных компьютеров.](#adding-a-desktop-bridge-component)</span><span class="sxs-lookup"><span data-stu-id="88f03-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>  
1.  <span data-ttu-id="88f03-230">Создайте расширение Microsoft Edge, которое использует родной обмен сообщениями для связи с приложением-компаньоном UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span>  <span data-ttu-id="88f03-231">Файлы расширения можно добавить в папку с именем `Extension` в проекте UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span>  <span data-ttu-id="88f03-232">Все файлы под этой папкой, в том числе подмостки, должны иметь свои свойства настроены таким `Build Action=Content` образом, что и `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="88f03-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  <span data-ttu-id="88f03-233">`manifest.json`Убедитесь, что также настроены с этими свойствами.</span><span class="sxs-lookup"><span data-stu-id="88f03-233">Make sure `manifest.json` is also configured with these properties.</span></span>  
1.  <span data-ttu-id="88f03-234">Измените файл в проекте, чтобы включить метаданные расширения и преобразовать его в `package.manifest.xml` безголовые приложения, `AppListEntry="none"` добавив:</span><span class="sxs-lookup"><span data-stu-id="88f03-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>  
    
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
    
1.  <span data-ttu-id="88f03-235">Используйте `AppService` имя, настроенное для UWP, в API для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="88f03-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>  
1.  <span data-ttu-id="88f03-236">Сборка [и развертывание](#deploying) проекта UWP \(с необязательным компонентом Моста настольных компьютеров\).</span><span class="sxs-lookup"><span data-stu-id="88f03-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span></span>  
1.  <span data-ttu-id="88f03-237">[Пакет](#packaging) вашего родного расширения обмена сообщениями после его готовности к отправке в Магазин</span><span class="sxs-lookup"><span data-stu-id="88f03-237">[Package](#packaging) your native messaging extension once it is ready for Store submission</span></span>  
    
> [!NOTE]
> <span data-ttu-id="88f03-238">Ссылка на [раздел Demos](#demos) для примера полного расширения родных сообщений.</span><span class="sxs-lookup"><span data-stu-id="88f03-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>  

## <a name="adding-a-desktop-bridge-component"></a><span data-ttu-id="88f03-239">Добавление компонента моста рабочего стола</span><span class="sxs-lookup"><span data-stu-id="88f03-239">Adding a Desktop Bridge component</span></span>  

<span data-ttu-id="88f03-240">Если вы хотите добавить компонент Моста настольных компьютеров в пакет, необходимо создать и построить проект Win32 в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="88f03-240">If you want to add a Desktop Bridge component to your package, you must create and build your Win32 project in Visual Studio.</span></span>  <span data-ttu-id="88f03-241">Сведения о преобразовании приложения win32 в UWP см. в сведениях о переносе приложений в [Windows 10 с помощью моста настольных компьютеров.](/windows/uwp/porting/desktop-to-uwp-root)</span><span class="sxs-lookup"><span data-stu-id="88f03-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span>  <span data-ttu-id="88f03-242">После Visual Studio в пакет можно добавить исполняемый win32, делая следующие действия:</span><span class="sxs-lookup"><span data-stu-id="88f03-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>  

1.  <span data-ttu-id="88f03-243">Добавьте проект Win32 в то же решение, что и проект UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-243">Add the Win32 project to the same solution as the UWP project.</span></span>  
1.  <span data-ttu-id="88f03-244">Установите проект Win32 в качестве зависимого проекта для проекта UWP:</span><span class="sxs-lookup"><span data-stu-id="88f03-244">Set the Win32 project as a dependent project for the UWP project:</span></span>  
    
    ![настройка зависимостей проекта](../media/project-dependencies.png)  
    
1.  <span data-ttu-id="88f03-246">Создание `Win32` папки в проекте UWP.</span><span class="sxs-lookup"><span data-stu-id="88f03-246">Create a `Win32` folder within the UWP project.</span></span>  <span data-ttu-id="88f03-247">Скопируйте необходимые для проекта `Win32` раздвители в эту папку.</span><span class="sxs-lookup"><span data-stu-id="88f03-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span>  <span data-ttu-id="88f03-248">Настройка свойств всех бинарей, таких, что `Build Action=Content` и `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="88f03-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  
    
    ![папка с файлами приложений win32 и UWP в ней](../media/desktop-bridge.png)  
    
1.  <span data-ttu-id="88f03-250">Измените файл проекта UWP, чтобы скопировать все необходимые файлы для проекта в эту папку `Win32` с помощью команды событий PostBuild.</span><span class="sxs-lookup"><span data-stu-id="88f03-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span>  <span data-ttu-id="88f03-251">Это гарантирует, что обновленные биналоги копируется в папку каждый раз при восстановлении решения.</span><span class="sxs-lookup"><span data-stu-id="88f03-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  <span data-ttu-id="88f03-252">`package.manifest.xml`Измените, `<desktop:Extension>` добавив элемент в `<Extensions>` элемент:</span><span class="sxs-lookup"><span data-stu-id="88f03-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a><span data-ttu-id="88f03-253">Развертывание</span><span class="sxs-lookup"><span data-stu-id="88f03-253">Deploying</span></span>  

<span data-ttu-id="88f03-254">После настройки проекта UWP \(и необязательно Win32 project\) как описано выше, вы будете готовы развернуть решение с помощью Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="88f03-254">Once you have configured your UWP project \(and optionally Win32 project\) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>  

![создание проекта inprocess](../media/native-message-uwp-debug.png)  

<span data-ttu-id="88f03-256">После правильного развертывания решения необходимо увидеть расширение в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>  

![расширение, показывающаяся в Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a><span data-ttu-id="88f03-258">Создание пакетов</span><span class="sxs-lookup"><span data-stu-id="88f03-258">Packaging</span></span>  

> [!NOTE]
> <span data-ttu-id="88f03-259">Отправка расширения Microsoft Edge в Microsoft Store в настоящее время является ограниченной возможностью.</span><span class="sxs-lookup"><span data-stu-id="88f03-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="88f03-260">[Отправьте запрос](https://developer.microsoft.com/microsoft-edge/extensions/requests/) на участие в Microsoft Store и рассматривайте его для будущих обновлений.</span><span class="sxs-lookup"><span data-stu-id="88f03-260">[Send a request](https://developer.microsoft.com/microsoft-edge/extensions/requests/) to be a part of the Microsoft Store, and be considered for future updates.</span></span>  

<span data-ttu-id="88f03-261">Вы можете создать пакет Store для отправки в Центр разработчиков Windows с помощью встроенных Visual Studio функций:</span><span class="sxs-lookup"><span data-stu-id="88f03-261">You may generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>  

![Создание пакета Store](../media/create-store-package.png)  

## <a name="debugging"></a><span data-ttu-id="88f03-263">Отладка</span><span class="sxs-lookup"><span data-stu-id="88f03-263">Debugging</span></span>  

<span data-ttu-id="88f03-264">Инструкции по отладки различаются в зависимости от того, какой компонент необходимо протестировать:</span><span class="sxs-lookup"><span data-stu-id="88f03-264">The instructions for debugging vary depending on which component you want to test out:</span></span>  

### <a name="debugging-the-extension"></a><span data-ttu-id="88f03-265">Отладка расширения</span><span class="sxs-lookup"><span data-stu-id="88f03-265">Debugging the extension</span></span>  

<span data-ttu-id="88f03-266">После развертывания решения расширение будет установлено в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88f03-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span>  <span data-ttu-id="88f03-267">Сведения о [](./debugging-extensions.md) том, как отладить расширение, ознакомьтесь с руководством по отладки.</span><span class="sxs-lookup"><span data-stu-id="88f03-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>  

### <a name="debugging-the-uwp-app"></a><span data-ttu-id="88f03-268">Отладка приложения UWP</span><span class="sxs-lookup"><span data-stu-id="88f03-268">Debugging the UWP app</span></span>  

<span data-ttu-id="88f03-269">Приложение UWP запустится, когда расширение попытается подключиться к ней с [помощью](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)API обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="88f03-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="88f03-270">Отламываю приложение UWP только после начала процесса.</span><span class="sxs-lookup"><span data-stu-id="88f03-270">You must debug the UWP app only once the process starts.</span></span>  <span data-ttu-id="88f03-271">Это может быть настроено с помощью страницы Свойства проекта:</span><span class="sxs-lookup"><span data-stu-id="88f03-271">This may be configured using the Property page of the project:</span></span>  

1.  <span data-ttu-id="88f03-272">В Visual Studio наведите курсор на проект приложения UWP и откройте контекстное меню \(правой кнопкой мыши\)</span><span class="sxs-lookup"><span data-stu-id="88f03-272">In Visual Studio, hover on your UWP app project and open the contextual menu \(right-click\)</span></span>  
1.  <span data-ttu-id="88f03-273">Выбор **свойств**</span><span class="sxs-lookup"><span data-stu-id="88f03-273">Select **Properties**</span></span>  
1.  <span data-ttu-id="88f03-274">Check **Do not launch, but debug my code when it starts**</span><span class="sxs-lookup"><span data-stu-id="88f03-274">Check **Do not launch, but debug my code when it starts**</span></span>  
    
    ![выбор не запускать поле](../media/native-message-do-not-launch.png)  
    
<span data-ttu-id="88f03-276">В Visual Studio теперь можно установить точки разлома в коде, где нужно отладить, а затем запустить отладка, нажав F5.</span><span class="sxs-lookup"><span data-stu-id="88f03-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span>  <span data-ttu-id="88f03-277">После взаимодействия с расширением для подключения к приложению UWP Visual Studio автоматически подключается к процессу.</span><span class="sxs-lookup"><span data-stu-id="88f03-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>  

### <a name="debugging-the-desktop-bridge"></a><span data-ttu-id="88f03-278">Отладка моста настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="88f03-278">Debugging the Desktop Bridge</span></span>  

<span data-ttu-id="88f03-279">Несмотря на то, что существуют различные методы отладки настольного моста [](/windows/msix/desktop/desktop-to-uwp-debug) \(преобразованное приложение Win32\), единственным применимым для этого сценария является вариант PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="88f03-279">Even though there are various [methods for debugging a Desktop Bridge](/windows/msix/desktop/desktop-to-uwp-debug) \(converted Win32 app\), the only one applicable for this scenarios is the PLMDebug option.</span></span>  <span data-ttu-id="88f03-280">Вы также можете добавить код отладки в функцию запуска, чтобы выполнить ожидание в течение определенного времени, что позволяет Visual Studio к процессу.</span><span class="sxs-lookup"><span data-stu-id="88f03-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>  
