---
description: Документация по средствам обмена сообщениями
title: Встроенные сообщения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик
ms.openlocfilehash: d9c2370d6a4f9f7cd25001c1c58ce266423af19a
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343068"
---
# Встроенные сообщения  

Расширения взаимодействуют с приложением Win32, установленным на устройстве пользователя, с помощью API передачи сообщений.  Нативный хост приложения отправляет и получает сообщения с расширениями с помощью стандартного ввода и стандартных выходных данных.  Расширения, использующие нативную систему обмена сообщениями, устанавливаются в Microsoft Edge аналогично любому другому расширению.  Однако microsoft Edge не устанавливает и не управляет приложениями нативных приложений.  

Для получения расширения и ведущего приложения у вас есть две модели распространения.  

*   Упакуйте расширение и хост вместе.  Когда пользователь устанавливает пакет, устанавливаются расширение и хост.  
*   Установите расширение с помощью [microsoft Edge Add-ons store,] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]и ваше расширение будет предложено пользователям установить хост.  

Чтобы создать расширение для отправки и получения сообщений с помощью ведущих приложений, следуйте следующим шагам.  

## Шаг 1. Добавление разрешений в манифест расширения  

Добавьте разрешение `nativeMessaging` вmanifest.js** в** файл расширения.  Следующий фрагмент кода является примером **manifest.js.**  

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

## Шаг 2. Создание файла манифеста ведущего приложения для обмена сообщениями  

Native applications must provide a native messaging host manifest file.  Файл манифеста содержит следующие сведения.  

*   Путь к native messaging host runtime.  
*   Метод связи с расширением.  
*   Список разрешенных расширений, с которыми он взаимодействует.  
    
Браузер считыет и проверяет манифест ведущего приложения для обмена сообщениями.  Браузер не устанавливает файл манифеста ведущего приложения для обмена сообщениями и не управляет им.  

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

Файл манифеста ведущего файла должен быть допустимым JSON-файлом, содержащего следующие ключи.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Указывает имя нативного хоста обмена сообщениями.  Клиенты передают эту строку `runtime.connectNative` или `runtime.sendNativeMessage` .  
      
      *   Это значение должно содержать только буквы и цифры нижнего регистра, символы подчеркиваия и точки.  
      *   Это значение не должно начинаться или заканчивается точкой, и точка не должна следовать за другой точкой.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      Описывает приложение.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      Указывает путь к двоичному файлу нативного хоста обмена сообщениями.  
      
      *   На устройствах с Windows можно использовать относительные пути к каталогу, который содержит файл манифеста.  
      *   В macOS и Linux путь должен быть абсолютным.  
      
      Процесс ведущего файла начинается с текущего каталога, в который входит двоичный файл ведущего файла.  Например, \(Windows\), если этот параметр задан, двоичный файл начинает использовать текущий `C:\Application\nm_host.exe` каталог \( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Указывает тип интерфейса, используемого для связи с ведущим приложением системы обмена сообщениями.  Это значение предписывает Microsoft Edge использовать `stdin` и `stdout` взаимодействовать с ведущим сайтом.  
      Единственным допустимым значением `stdio` является .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Указывает список расширений, которые имеют доступ к нативным хосту обмена сообщениями.  Чтобы приложение определяло расширение и связывалось с ним, в файле манифеста ведущего приложения для обмена сообщениями установите следующее значение.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Загрузка нео sideload расширения для проверки нативных сообщений с хост-приложением.  
Для загрузки неогрузки расширения во время разработки и `microsoft_catalog_extension_id` извлечения выполните следующие действия.  

1.  Перейдите к и включите выключатель режима `edge://extensions` разработчика.  
1.  Choose **Load unpacked**, and then select your extension package to sideload.  
1.  Нажмите кнопку **ОК**.  
1.  Перейдите `edge://extensions` на страницу и убедитесь, что расширение указано в списке.  
1.  Скопируйте ключ `microsoft_catalog_extension_id` из \(ID\) из списка расширений на странице.  

Когда вы будете готовы распространять расширение среди пользователей, опубликуйте расширение в магазине надстройки Microsoft Edge.  ИД расширения опубликованного расширения может отличаться от ИД, используемого при загрузке неопубликоваемого расширения.  Если ИД изменился, обновите в файле манифеста ведущего файла с помощью `allowed_origins` ИД опубликованного расширения.  

## Шаг 3. Копирование файла манифеста ведущего приложения для обмена сообщениями в систему  

На заключительном этапе необходимо скопировать собственный файл манифеста хоста обмена сообщениями на компьютер и обеспечить правильную настройку файла манифеста.  Чтобы убедиться, что файл манифеста помещен в ожидаемое расположение, выполните следующие действия.  Расположение зависит от платформы.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

Файл манифеста может быть расположен в любом месте файловой системы.  Установщик приложений должен создать ключ реестра и установить для этого ключа по умолчанию полный путь к файлу манифеста.  Следующие команды являются примерами ключей реестра.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Добавление в каталог ключа реестра с ключом манифеста.  

*   Запустите команду в командной подсказке.  
    
    1.  Запустите следующую команду:  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Создайте `.reg` файл и запустите его.  
    
    1.  Скопируйте следующую команду в `.reg` файл.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Запустите `.reg` файл.  
    
Microsoft Edge запрашивает `HKEY_CURRENT_USER` корневой ключ, за которым следует `HKEY_LOCAL_MACHINE` .  В обоих ключах сначала поиск в 32-битовом реестре, а затем поиск 64-битного реестра для определения нативных ведущих приложений для обмена сообщениями.  В этом ключе реестра указывается расположение манифеста ведущего приложения для обмена сообщениями.  Если Microsoft Edge находит ключ реестра в любом из ранее перечисленных местоположений, он не запрашивает расположения, указанные в этом абзаце.  Если вы запустите вышеуказанный файл как часть пакетного скрипта, убедитесь, что он работает с `.reg` помощью командной подсказки администратора.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Чтобы сохранить файл манифеста, выполните одно из следующих действий.  

*   Системные ведущие приложения для обмена сообщениями, доступные всем пользователям, хранятся в фиксированном расположении.  Например, файл манифеста должен храниться в следующем расположении.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Пользовательские ведущие приложения для обмена сообщениями, доступные только текущему пользователю, находятся в подкадиректоре в `NativeMessagingHosts` каталоге профилей пользователей.  Например, файл манифеста должен храниться в следующем расположении.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    The  `{Channel_Name}` in must be one of the following `Microsoft Edge {Channel_Name}` values.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    При использовании канала Stable `{Channel_Name}` не требуется.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Чтобы сохранить файл манифеста, выполните одно из следующих действий.  

*   Системные ведущие приложения для обмена сообщениями, доступные всем пользователям, хранятся в фиксированном расположении.  Файл манифеста должен храниться в следующем расположении.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Пользовательские ведущие приложения для обмена сообщениями, доступные только текущему пользователю, находятся в подкадиректоре в `NativeMessagingHosts` каталоге профилей пользователей.  Файл манифеста должен храниться в следующем расположении.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Убедитесь, что вы предоставляете разрешения на чтение файла манифеста и запускайте разрешения в хост-оке.  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Надстройки Microsoft Edge"

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Здесь находится исходная [страница.](https://developer.chrome.com/extensions/nativeMessaging)  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
