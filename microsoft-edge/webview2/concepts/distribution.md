---
description: Варианты распространения при выпуске приложения с помощью Microsoft Edge WebView2
title: Распространение приложений Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 89e53c43c3550d0a7a3707381cc4c76be111db28
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182294"
---
# Распространение приложений с помощью WebView2  

При распространении приложения WebView2 перед запуском приложения убедитесь, что резервная веб-платформа, [WebView2 среды выполнения][Webview2Installer], присутствует.  В этой статье описано, как (разработчику) установить среду выполнения WebView2 и использовать два режима распространения для вашего приложения WebView2:  [Evergreen](#evergreen-distribution-mode) и [fixed Version](#fixed-version-distribution-mode).  

## Режим распространения Evergreen  

> [!NOTE]
> Для большинства разработчиков рекомендуется использовать режим распространения Evergreen.  

Режим распространения Evergreen гарантирует, что ваше приложение использует последние возможности и обновления для системы безопасности.  Она обладает следующими характеристиками.  

*   Базовая веб-платформа \ (WebView2 (среда выполнения)) обновляется автоматически без дополнительных усилий.  
*   Во всех приложениях, использующих режим распространения Evergreen, используется общая копия среды выполнения Evergreen WebView2, что экономит место на диске.  
    
### Общие сведения о среде выполнения WebView2  

Среда выполнения WebView2 является распространяемой средой выполнения и используется в качестве резервной веб-платформы для приложений WebView2.  Концепция сходна с Visual C++ или средой выполнения .NET для приложений/.NET на C++.  Среда выполнения включает измененные двоичные файлы Microsoft Edge \ (Chromium \), которые настроены и протестированы для приложений.  Среда выполнения не отображается в качестве видимого для пользователя браузера при установке.  Например, у пользователя нет ярлыка на рабочем столе браузера или элемента меню "Пуск".  

Во время разработки и тестирования вы можете использовать либо резервную веб-платформу.  

*   Среда выполнения WebView2  
*   Любой канал предварительной оценки (не стабильный) Microsoft Edge \ (Chromium \) в браузере  
    
В рабочих средах перед запуском приложения необходимо убедиться, что среда выполнения присутствует на устройстве пользователя.  Стабильный канал Microsoft Edge недоступен для использования WebView2.  Это решение предотвращает зависимость приложениями от браузера в производстве.

Не следует использовать зависимость от браузера по следующим причинам:  

*   Microsoft Edge \ (Chromium \) не гарантируется на всех устройствах пользователей.  Например, если устройства отключены от центра обновления Windows или не управляются корпорацией Майкрософт напрямую (в крупной части компании и на рынке для образовательных учреждений) не может быть браузера.  Предоставление вам возможности распространения среды выполнения WebView2 не позволяет использовать зависимость в браузере в качестве предварительной версии для приложений.  
*   В браузерах и приложениях используются различные варианты использования, поэтому использование зависимостей в браузере может привести к нежелательным побочным эффектам для приложений.  Например, ИТ-администраторы могут управлять версиями в браузере для обеспечения совместимости внутренних веб-сайтов.  Среда выполнения WebView2 позволяет приложениям оставаться Evergreen, пока обновления браузера активно управляются.  
*   В отличие от браузера, среда выполнения разрабатывается и тестируется для сценариев приложений, а в некоторых случаях может включать исправления ошибок, еще не доступные в браузере.  
    
В будущем планы выполнения Evergreen WebView2, которые планируется использовать в будущих выпусках Windows.  Развертывание среды выполнения с помощью приложения "производство" до тех пор, пока среда выполнения не станет доступной в универсальном виде.  

### Развертывание среды выполнения Evergreen WebView2  

Для всех Evergreen приложений на устройстве требуется только одна установка среды выполнения Evergreen WebView2.  На [странице загрузки среды выполнения WebView2][Webview2Installer]доступно несколько средств.  Следующие инструменты помогут вам развернуть среду выполнения Evergreen.  

*   Загрузчик среды выполнения WebView2 — это крошечный установщик \ (примерно 2 МБ \).  Загрузчик среды выполнения WebView2 загружает и устанавливает среду выполнения Evergreen с серверов Microsoft, которые соответствуют архитектуре устройства пользователя.  
*   Используйте ссылку для программной загрузки загрузчика.  
*   Автономный установщик среды выполнения WebView2 — это полный установщик, который устанавливает среду выполнения Evergreen WebView2 в автономных средах.  
    
В настоящее время загрузчик и автономный установщик поддерживают только установки для компьютера, для которого требуется повышение прав.  Если установщик запускается без повышения прав, пользователю будет предложено поднять разрешения.  

Используйте следующие рабочие процессы, чтобы убедиться, что среда выполнения уже установлена перед запуском приложения.  Вы можете настроить рабочий процесс в зависимости от вашего сценария.  Пример кода можно найти в [репозиторий примеров] [GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### Развертывание только в сети  

Если у вас есть сценарий развертывания, предназначенный только в Интернете, выполните указанные ниже действия.  

1.  Убедитесь, что во время настройки приложения среда выполнения уже установлена.  Чтобы проверить, выполните одно из указанных ниже действий.  
    *   Проверить, существует ли элемент `pv (REG_SZ)` RegKey и что он не является `null` пустым.  Найдите  `pv (REG_SZ)` в следующем расположении.  
        
        В 64 – разрядная версия Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        В 32 – разрядная версия Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Запустите [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] и убедитесь в том, что `versionInfo` это так `NULL` .  
1.  Если среда выполнения не установлена, воспользуйтесь ссылкой, чтобы программно загрузить загрузчик.  
1.  Вызовите загрузчик из процесса с повышенными привилегиями или командной строки `MicrosoftEdgeWebview2Setup.exe /silent /install` для автоматической установки.  
    
Предыдущий рабочий процесс имеет указанные ниже преимущества.  

*   Устанавливайте среду выполнения только в том случае, если это необходимо или если вам не требуется устанавливать пакет для установки.  
*   Загрузчик автоматически обнаружит архитектуру устройства и установит соответствующую среду выполнения.  
*   Установка среды выполнения без вмешательства пользователя.  
    
Вы также можете упаковать загрузчик с приложением, а не загружать его программным путем по запросу.  

#### Развертывание в автономном режиме  

Если вы работаете в автономном режиме, когда развертывание приложения будет работать в автономном режиме, выполните указанные ниже действия.  

1.  Скачайте [автономный установщик][Webview2Installer].  
1.  Включите установщик в установщик приложений или средство обновления.  
1.  Убедитесь, что во время настройки приложения среда выполнения уже установлена.  Чтобы проверить, выполните одно из указанных ниже действий.  
    *   Проверить, существует ли элемент `pv (REG_SZ)` RegKey и что он не является `null` пустым.  Найдите  `pv (REG_SZ)` в следующем расположении.  
        
        В 64 – разрядная версия Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        В 32 – разрядная версия Windows  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Запустите [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] и убедитесь в том, что `versionInfo` это так `NULL` .  
1.  Если среда выполнения не установлена, запустите автономный установщик.  Если вы хотите выполнить автоматическую установку, запустите установщик из процесса с повышенными привилегиями или скопируйте и выполните следующую команду:  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Совместимость в режиме Evergreen  

Интернет постоянно развивается.  Среда выполнения Evergreen WebView2 актуальна для обеспечения последних функций и исправлений для системы безопасности.  Для обеспечения совместимости приложения с Интернетом следует настроить инфраструктуру тестирования.  

Нестабильные каналы Microsoft Edge \ (бета-версия/разработка/Канарские \) предоставляют краткий обзор того, что поступает в среду выполнения WebView2.  Как и в случае разработки веб-сайтов для Microsoft EDGE, вы должны регулярно тестировать приложение WebView2.  Протестируйте приложение WebView2 с одним из нестабильных каналов и обновляйте свое приложение или [сообщайте о проблемах][GithubMicrosoftedgeWebviewfeedback] в случае возникновения проблем. Обычно для разработки и бета-версии рекомендуются каналы.  Чтобы помочь вам выбрать подходящий канал, перейдите к разделу [Обзор каналов Microsoft Edge][DeployEdgeMicrosoftEdgeChannels].  Вы можете скачать [нестабильный канал Microsoft Edge][DownloadNonstableEdge] в тестовой среде, а также использовать `regkey` переменные среды для обозначения канала для вашего приложения, поддерживающего тестирование.  Дополнительные сведения можно найти в [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  Кроме того, вы можете автоматизировать тестирование WebView2 с помощью этого [устройства][HowtoWebdriver] .

## Режим распространения фиксированной версии  

> [!NOTE]
> Режим распространения с фиксированной версией — общедоступный предварительный просмотр.  

Режим распространения с фиксированной версией был ранее назван "My-собственная".  

Для ограниченных сред с строгой совместимостью следует использовать режим распространения с фиксированной версией.  Выберите и упакуйте определенную версию среды выполнения WebView2, используя режим распространения с фиксированной версией.  Вы можете указать время обновления среды выполнения для вашего приложения.  Режим распространения фиксированной версии не получает никаких автоматических обновлений. Спланируйте, как обновить приложение и среду выполнения.  

Чтобы использовать режим фиксированной версии, выполните указанные ниже действия.

1.  [Скачайте][Webview2Installer] пакет фиксированной версии. 
1.  Распакуйте пакет с помощью командной строки `expand {path to the package} -F:* {path to the destination folder}` или таких средств, как WinRAR. Не следует распаковать файл в проводнике, так как это может привести к неправильной структуре папок.  
1.  Включите в проект распакованные двоичные файлы фиксированной версии.  
1.  Укажите путь к двоичным файлам с фиксированной версией при создании среды WebView2.  
    *   Для Win32 C/C++ вы можете создать среду с помощью функции [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] .  Используйте этот `browserExecutableFolder` параметр, чтобы указать путь к папке, содержащей ее `msedgewebview2.exe` .  
    *   В .NET можно задать среду с помощью одного из следующих параметров.  
        
        > [!NOTE]
        > Прежде чем свойство WebView2 будет применено, необходимо указать среду `Source` .  
        
        *   Задайте `CreationProperties` свойство \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) для элемента WebView2.  Используйте `BrowserExecutableFolder` элемент `CoreWebView2CreationProperties` класса \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\), чтобы указать путь к двоичным файлам с фиксированной версией.  
        *   Используйте `EnsureCoreWebView2Async` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\), чтобы указать среду.  Используйте `browserExecutableFolder` параметр в [CoreWebView2Environment. CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] , чтобы указать путь к двоичным файлам с фиксированной версией.  
1.  Упакуйте и отгрузите двоичные файлы фиксированной версии с приложением.  Обновите двоичные файлы соответствующим образом.  
    
### Известные проблемы с исправленной версией  

По сравнению со средой выполнения Evergreen в исправленной версии отсутствует процесс установки, что приводит к тому, что [приложение Microsoft PlayReady][MicrosoftPlayReady] не будет работать без изменений.  Вы можете устранить проблему, выполнив указанные ниже действия.  

1.  Найдите путь, по которому развертывается пакет фиксированной версии на устройстве пользователя, например в следующем расположении.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Выполните указанные ниже команды на устройстве пользователя.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  В настоящее время на устройстве пользователя будет работать PlayReady.  На вкладке **Безопасность** папки **фиксированная версия** она должна включать разрешения `ALL APPLICATION PACKAGES` и `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Разрешение для PlayReady" lightbox="../media/play-ready-permission.png":::
        Разрешение для PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Общие сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[HowtoWebdriver]: ../howto/webdriver.md "Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge | Документы Microsoft"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Документы Microsoft"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Документы Microsoft"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "Класс CreateAsync-Microsoft. Web. WebView2. Core. CoreWebView2Environment | Документы Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Класс EnsureCoreWebView2Async-Microsoft. Web. WebView2. WPF. WebView2 | Документы Microsoft"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Класс EnsureCoreWebView2Async-Microsoft. Web. WebView2. WinForms. WebView2 | Документы Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "Класс CoreWebView2CreationProperties-Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties | Документы Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Класс Microsoft. Web. WebView2. WinForms | Документы Microsoft"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "Класс CreationProperties-Microsoft. Web. WebView2. WPF. WebView2 | Документы Microsoft"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Класс Microsoft. Web. WebView2. WinForms. WebView2 | Документы Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2 | Разработчик Майкрософт"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView отзыв | GitHub"  

[GitHubMicrosoftMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "WebView2 развертывание — MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  
