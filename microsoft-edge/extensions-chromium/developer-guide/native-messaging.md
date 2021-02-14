---
description: Документация по средствам обмена сообщениями
title: Встроенные сообщения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: 2d629762d4c7c75832905cfbf8c2d5311191092d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327703"
---
# <span data-ttu-id="85ae5-104">Встроенные сообщения</span><span class="sxs-lookup"><span data-stu-id="85ae5-104">Native messaging</span></span>  

<span data-ttu-id="85ae5-105">Расширения взаимодействуют с приложением Win32, установленным на устройстве пользователя, с помощью API передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="85ae5-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="85ae5-106">Нативный хост приложения отправляет и получает сообщения с расширениями с помощью стандартного ввода и стандартных выходных данных.</span><span class="sxs-lookup"><span data-stu-id="85ae5-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="85ae5-107">Расширения, использующие средства обмена сообщениями, устанавливаются в Microsoft Edge аналогично любому другому расширению.</span><span class="sxs-lookup"><span data-stu-id="85ae5-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="85ae5-108">Тем не менее, microsoft Edge не устанавливает и не управляет приложениями из нативных приложений.</span><span class="sxs-lookup"><span data-stu-id="85ae5-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="85ae5-109">Чтобы получить расширение и машинный хост приложения, у вас есть две модели распространения.</span><span class="sxs-lookup"><span data-stu-id="85ae5-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="85ae5-110">Упакуйте расширение и хост вместе.</span><span class="sxs-lookup"><span data-stu-id="85ae5-110">Package your extension and the host together.</span></span>  <span data-ttu-id="85ae5-111">Когда пользователь устанавливает пакет, устанавливаются расширение и хост.</span><span class="sxs-lookup"><span data-stu-id="85ae5-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="85ae5-112">Установите расширение с помощью [microsoft Edge Add-ons store,] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]и ваше расширение будет предложено пользователям установить хост.</span><span class="sxs-lookup"><span data-stu-id="85ae5-112">Install your extension using the [Microsoft Edge Add-ons store] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="85ae5-113">Чтобы создать расширение для отправки и получения сообщений с помощью ведущих приложений, следуйте следующим шагам.</span><span class="sxs-lookup"><span data-stu-id="85ae5-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="85ae5-114">Шаг 1. Добавление разрешений в манифест расширения</span><span class="sxs-lookup"><span data-stu-id="85ae5-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="85ae5-115">Добавьте разрешение `nativeMessaging` вmanifest.js\*\* в\*\* файл расширения.</span><span class="sxs-lookup"><span data-stu-id="85ae5-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="85ae5-116">Следующий фрагмент кода является примером **manifest.js.**</span><span class="sxs-lookup"><span data-stu-id="85ae5-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```  

## <span data-ttu-id="85ae5-117">Шаг 2. Создание файла манифеста ведущего приложения для обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="85ae5-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="85ae5-118">Native applications must provide a native messaging host manifest file.</span><span class="sxs-lookup"><span data-stu-id="85ae5-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="85ae5-119">Файл манифеста содержит следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="85ae5-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="85ae5-120">Путь к native messaging host runtime.</span><span class="sxs-lookup"><span data-stu-id="85ae5-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="85ae5-121">Метод связи с расширением.</span><span class="sxs-lookup"><span data-stu-id="85ae5-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="85ae5-122">Список разрешенных расширений, с которыми он взаимодействует.</span><span class="sxs-lookup"><span data-stu-id="85ae5-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="85ae5-123">Браузер считыет и проверяет манифест ведущего приложения системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="85ae5-124">Браузер не устанавливает файл манифеста ведущего приложения системы обмена сообщениями и не управляет им.</span><span class="sxs-lookup"><span data-stu-id="85ae5-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

```json
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
```  

<span data-ttu-id="85ae5-125">Файл манифеста ведущего файла должен быть допустимым JSON-файлом, содержащего следующие ключи.</span><span class="sxs-lookup"><span data-stu-id="85ae5-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85ae5-126">Указывает имя нативного хоста обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-126">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="85ae5-127">Клиенты передают эту строку `runtime.connectNative` или `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="85ae5-127">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="85ae5-128">Это значение должно содержать только буквы и цифры нижнего регистра, подчеркиваия и точки.</span><span class="sxs-lookup"><span data-stu-id="85ae5-128">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="85ae5-129">Это значение не должно начинаться или заканчивается точкой, и точка не должна следовать за другой точкой.</span><span class="sxs-lookup"><span data-stu-id="85ae5-129">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85ae5-130">Описывает приложение.</span><span class="sxs-lookup"><span data-stu-id="85ae5-130">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85ae5-131">Указывает путь к двоичному файлу нативного хоста обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-131">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="85ae5-132">На устройствах с Windows можно использовать относительные пути к каталогу, который содержит файл манифеста.</span><span class="sxs-lookup"><span data-stu-id="85ae5-132">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="85ae5-133">В macOS и Linux путь должен быть абсолютным.</span><span class="sxs-lookup"><span data-stu-id="85ae5-133">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="85ae5-134">Процесс ведущего файла начинается с текущего каталога, в который входит двоичный файл ведущего файла.</span><span class="sxs-lookup"><span data-stu-id="85ae5-134">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="85ae5-135">Например, \(Windows\), если этот параметр задан, двоичный файл начинает использовать текущий `C:\Application\nm_host.exe` каталог \( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="85ae5-135">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85ae5-136">Указывает тип интерфейса, используемого для связи с ведущим приложением системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-136">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="85ae5-137">Это значение предписывает Microsoft Edge использовать `stdin` и `stdout` взаимодействовать с ведущим.</span><span class="sxs-lookup"><span data-stu-id="85ae5-137">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="85ae5-138">Единственным допустимым значением `stdio` является .</span><span class="sxs-lookup"><span data-stu-id="85ae5-138">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85ae5-139">Указывает список расширений, которые имеют доступ к нативным хосту обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-139">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="85ae5-140">Чтобы приложение определяло расширение и связывалось с ним, в файле манифеста ведущего приложения для обмена сообщениями установите следующее значение.</span><span class="sxs-lookup"><span data-stu-id="85ae5-140">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="85ae5-141">Загрузка нео sideload расширения для проверки нативных сообщений с хост-приложением.</span><span class="sxs-lookup"><span data-stu-id="85ae5-141">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="85ae5-142">Для загрузки неогрузки расширения во время разработки и `microsoft_catalog_extension_id` извлечения выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85ae5-142">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="85ae5-143">Перейдите к и включите выключатель режима `edge://extensions` разработчика.</span><span class="sxs-lookup"><span data-stu-id="85ae5-143">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="85ae5-144">Choose **Load unpacked**, and then select your extension package to sideload.</span><span class="sxs-lookup"><span data-stu-id="85ae5-144">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="85ae5-145">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="85ae5-145">Choose **OK**.</span></span>  
1.  <span data-ttu-id="85ae5-146">Перейдите `edge://extensions` на страницу и убедитесь, что расширение указано в списке.</span><span class="sxs-lookup"><span data-stu-id="85ae5-146">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="85ae5-147">Скопируйте ключ `microsoft_catalog_extension_id` из \(ID\) из списка расширений на странице.</span><span class="sxs-lookup"><span data-stu-id="85ae5-147">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  

<span data-ttu-id="85ae5-148">Когда вы будете готовы распространять расширение среди пользователей, опубликуйте расширение в магазине надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85ae5-148">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="85ae5-149">ИД расширения опубликованного расширения может отличаться от ИД, используемого при загрузке неопубликоваемого расширения.</span><span class="sxs-lookup"><span data-stu-id="85ae5-149">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="85ae5-150">Если ИД изменился, обновите в файле манифеста ведущего файла с помощью `allowed_origins` ИД опубликованного расширения.</span><span class="sxs-lookup"><span data-stu-id="85ae5-150">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="85ae5-151">Шаг 3. Копирование файла манифеста ведущего приложения для обмена сообщениями в систему</span><span class="sxs-lookup"><span data-stu-id="85ae5-151">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="85ae5-152">На заключительном этапе необходимо скопировать собственный файл манифеста хоста обмена сообщениями на компьютер и обеспечить правильную настройку файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="85ae5-152">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="85ae5-153">Чтобы убедиться, что файл манифеста помещен в ожидаемое расположение, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85ae5-153">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="85ae5-154">Расположение зависит от платформы.</span><span class="sxs-lookup"><span data-stu-id="85ae5-154">The location varies by platform.</span></span>  

### [<span data-ttu-id="85ae5-155">Windows</span><span class="sxs-lookup"><span data-stu-id="85ae5-155">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="85ae5-156">Файл манифеста может быть расположен в любом месте файловой системы.</span><span class="sxs-lookup"><span data-stu-id="85ae5-156">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="85ae5-157">Установщик приложений должен создать ключ реестра и установить для этого ключа по умолчанию полный путь к файлу манифеста.</span><span class="sxs-lookup"><span data-stu-id="85ae5-157">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="85ae5-158">Следующие команды являются примерами ключей реестра.</span><span class="sxs-lookup"><span data-stu-id="85ae5-158">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="85ae5-159">Добавление в каталог ключа реестра с ключом манифеста.</span><span class="sxs-lookup"><span data-stu-id="85ae5-159">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="85ae5-160">Запустите команду в командной подсказке.</span><span class="sxs-lookup"><span data-stu-id="85ae5-160">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="85ae5-161">Запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="85ae5-161">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="85ae5-162">Создайте `.reg` файл и запустите его.</span><span class="sxs-lookup"><span data-stu-id="85ae5-162">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="85ae5-163">Скопируйте следующую команду в `.reg` файл.</span><span class="sxs-lookup"><span data-stu-id="85ae5-163">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="85ae5-164">Запустите `.reg` файл.</span><span class="sxs-lookup"><span data-stu-id="85ae5-164">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="85ae5-165">Microsoft Edge запрашивает `HKEY_CURRENT_USER` корневой ключ, за которым следует `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="85ae5-165">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="85ae5-166">В обоих ключах сначала поиск в 32-битовом реестре, а затем поиск 64-битного реестра для определения нативных ведущих приложений для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-166">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="85ae5-167">В этом ключе реестра указывается расположение манифеста ведущего приложения для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="85ae5-167">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="85ae5-168">Если Microsoft Edge находит ключ реестра в любом из ранее перечисленных местоположений, он не запрашивает расположения, указанные в этом абзаце.</span><span class="sxs-lookup"><span data-stu-id="85ae5-168">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in this paragraph.</span></span>  <span data-ttu-id="85ae5-169">При запуске вышеуказанного файла в составе пакетного сценария убедитесь, что он был запускаться с `.reg` помощью командной команды администратора.</span><span class="sxs-lookup"><span data-stu-id="85ae5-169">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="85ae5-170">macOS</span><span class="sxs-lookup"><span data-stu-id="85ae5-170">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="85ae5-171">Чтобы сохранить файл манифеста, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="85ae5-171">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="85ae5-172">Системные ведущие приложения для обмена сообщениями, доступные всем пользователям, хранятся в фиксированном расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-172">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="85ae5-173">Например, файл манифеста должен храниться в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-173">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="85ae5-174">Пользовательские ведущие приложения для обмена сообщениями, доступные только текущему пользователю, находятся в подкадиректоре в `NativeMessagingHosts` каталоге профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="85ae5-174">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="85ae5-175">Например, файл манифеста должен храниться в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-175">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="85ae5-176">The  `{Channel_Name}` in must be one of the following `Microsoft Edge {Channel_Name}` values.</span><span class="sxs-lookup"><span data-stu-id="85ae5-176">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="85ae5-177">Canary</span><span class="sxs-lookup"><span data-stu-id="85ae5-177">Canary</span></span>  
    *   <span data-ttu-id="85ae5-178">Dev</span><span class="sxs-lookup"><span data-stu-id="85ae5-178">Dev</span></span>  
    *   <span data-ttu-id="85ae5-179">Beta</span><span class="sxs-lookup"><span data-stu-id="85ae5-179">Beta</span></span>  

    <span data-ttu-id="85ae5-180">При использовании канала Stable `{Channel_Name}` не требуется.</span><span class="sxs-lookup"><span data-stu-id="85ae5-180">When using the Stable channel, `{Channel_Name}` isn't required.</span></span>  

### [<span data-ttu-id="85ae5-181">Linux</span><span class="sxs-lookup"><span data-stu-id="85ae5-181">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="85ae5-182">Чтобы сохранить файл манифеста, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="85ae5-182">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="85ae5-183">Системные ведущие приложения для обмена сообщениями, доступные всем пользователям, хранятся в фиксированном расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-183">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="85ae5-184">Файл манифеста должен храниться в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-184">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="85ae5-185">Пользовательские ведущие приложения для обмена сообщениями, доступные только текущему пользователю, находятся в подкадиректоре в `NativeMessagingHosts` каталоге профилей пользователей.</span><span class="sxs-lookup"><span data-stu-id="85ae5-185">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="85ae5-186">Файл манифеста должен храниться в следующем расположении.</span><span class="sxs-lookup"><span data-stu-id="85ae5-186">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="85ae5-187">Убедитесь, что вы предоставляете разрешения на чтение файла манифеста и запускайте разрешения в хост-оке.</span><span class="sxs-lookup"><span data-stu-id="85ae5-187">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Надстройки Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="85ae5-189">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="85ae5-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="85ae5-190">Здесь находится исходная [страница.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="85ae5-190">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="85ae5-192">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="85ae5-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
