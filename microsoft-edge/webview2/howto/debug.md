---
description: Узнайте, как отлалать элементы управления WebView2.
title: Начало отладки приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузером, edge html
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230700"
---
# Начало отладки приложений WebView2  

Цель средства управления Microsoft Edge WebView2 — объединить лучшие функции и средства разработки веб-приложений и приложений.  При разработке приложения WebView2 необходимо отлалать приложение.  В этой статье описаны различные средства для отлажений веб-кода и нативного кода в приложении WebView2.  

## [Microsoft Edge DevTools](#tab/devtools)  

Используйте инструменты разработчика [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-содержимого, отображаемого в элементе управления WebView2, так же, как вы можете отладить другую веб-страницу, отображаемую в Microsoft Edge.  Чтобы открыть DevTools, установите фокус на веб-части управления и используйте одно из следующих действий.  

*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите `Inspect` .  
    
Дополнительные сведения см. в [обзоре DevTools.][DevtoolsGuideChromiumMain]  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   Отладка DevTools  
:::image-end:::  

## [VisualStudio](#tab/visualstudio)  

Visual Studio предоставляет различные средства отладки для веб-кода и нативного кода в приложениях WebView2.  В разделе Visual Studio основное внимание уделяется отладию элементов управления WebView, однако другие методы отладки в Visual Studio доступны как обычно.  Используйте следующий процесс для отлажений веб-кода и нативного кода только в приложениях Win32 или надстройки Office.  

> [!IMPORTANT]
> При отладки приложения в Visual Studio с присоединенным отладителям выбор может вызвать собственный отладок, а не `F12` "Инструменты разработчика".  Выберите `Ctrl` + `Shift` + `I` или используйте контекстное меню \(щелкните правой кнопкой мыши\), чтобы избежать этой ситуации.  

Перед началом убедитесь, что выполнены следующие требования.  

*   Для отлаки сценариев приложение должно быть запущено из Visual Studio.  
*   Отладка невозможно прикрепить к запущенной процедуре WebView2.  
*   Установите Visual Studio 2019 версии 16.4 Preview 2 или более поздней.  
    
Установите и настройте средства отладщика скриптов в Visual Studio.  

1.  Выполните следующие действия, чтобы установить компонент **диагностики JavaScript** в разработке для **настольных компьютеров с помощью C++.**  
    
    1.  В панели проводника Windows введите `Visual Studio Installer` .  
    1.  Выберите **Visual Studio установщика,** чтобы открыть его.  
    1.  В установщике Visual Studio в установленной версии выберите **кнопку** "Еще" и выберите **"Изменить".**  
    1.  В Visual Studio области **"Рабочие нагрузки"** выберите параметр "Разработка компьютеров **на C++".**  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Изменение рабочих нагрузок" lightbox="./media/workloads.png":::
            Visual Studio "Изменение рабочих нагрузок"
        :::image-end:::  
        
    1.  Выберите **отдельные компоненты.**  
    1.  В поле поиска введите `JavaScript diagnostics` .  
    1.  Выберите параметр **диагностики JavaScript.**  
    1.  Choose **Modify**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Вкладка Изменение отдельных компонентов" lightbox="./media/indivcomp.png":::
           Visual Studio Вкладка "Изменение отдельных компонентов"  
        :::image-end:::  
        
1.  Включить отладку сценариев для приложений WebView2.  
    1.  В проекте WebView2 откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Свойства".**  
    1.  В области **"Свойства конфигурации"** выберите **"Отладка".**  
    1.  В области **"Тип отладка"** выберите **JavaScript (WebView2).**  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio конфигурации отладки" lightbox="./media/enbjs.png":::
           Visual Studio **конфигурации отладки**  
        :::image-end:::  
        
Выполните следующие действия для отлаки приложения WebView2.  

1.  Чтобы установить точку останова в коде, наведите курсор слева от номера строки и выберите точку останова.  Адаптер отлаживки JS/TS не выполняет сопоставление исходных путей.  Необходимо открыть тот же путь, который связан с WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio точку останова" lightbox="./media/breakpoint.png"::: 
       Visual Studio точку останова  
    :::image-end:::  
    
1.  Чтобы запустить отладку, выберите размер бита платформы, а затем выберите зеленую кнопку воспроизведения рядом с локальным **отладильщиком Windows.**  Приложение запускается, и отладка подключается к первому созданному процессу WebView2.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio локального отладка Windows" lightbox="./media/run.png"::: 
       Visual Studio **локальный отладник Windows**  
    :::image-end:::  
    
1.  В консоли **отладки**найдите выходные данные от отладки.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio консоли отлаки" lightbox="./media/console.png"::: 
       Visual Studio консоли **отлаки**  
    :::image-end:::  
    
## [Visual Studio Code](#tab/visualstudiocode)  

Используйте Microsoft Visual Studio Code для отлаки сценариев, которые запускают элементы управления WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

В Visual Studio Code выполните следующие действия для отлаки кода. 

1.  Проект должен иметь `launch.json` файл.  Если в проекте нет файла, скопируйте следующий фрагмент кода и `launch.json` создайте `launch.json` новый файл.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  Чтобы установить точку останова в коде, наведите курсор на строку и выберите `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Точка останова за установлена в Visual Studio коде" lightbox="./media/breakpointvs.png":::
       Точка останова устанавливается в Visual Studio коде  
    :::image-end:::
    
    > [!NOTE]
    > Так Visual Studio Code не выполняет сопоставление источника, убедитесь, что вы установили точки останова в том же файле, который использует WebView2.  Если пути не совпадают, код Visual Studio не приостанавливовка запущенного кода в точке останова.  
    
1.  Запустите код.  
    1.  На **вкладке "Выполнить"** выберите конфигурацию запуска в меню в выпадаемом меню.  
    1.  Чтобы начать отладку приложения, выберите "Начать отладку", который является зеленым треугольником рядом с drop down конфигурации запуска.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio вкладки Запуск кода" lightbox="./media/runvs.png":::
           Visual Studio вкладки "Запуск кода"  
        :::image-end:::  
        
1.  Откройте **консоль отлаки,** чтобы просмотреть выходные данные и ошибки отлаки.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio консоли отлаки кода" lightbox="./media/resultsvs.png":::
       Visual Studio консоли отлаки кода  
    :::image-end:::  
    
**Дополнительные параметры:**  

*   Отладка целевого веб-приложения. 
    
    В некоторых приложениях WebView2 можно использовать более одного управления WebView2. Чтобы выбрать отладку для управления WebView2 в этой ситуации, можно использовать целевую отладку webview2 
    
    Откройте `launch.json` и выполните следующие действия, чтобы использовать целевую отладку Веб-просмотр.  
    
    1.  Подтвердим, `useWebview` что для параметра установлено заданный параметр `true` .  
    1.  Добавьте `urlFilter` параметр.  Когда управление WebView2 переходит по URL-адресу, значение параметра используется для сравнения строк, которые `urlFilter` отображаются в URL-адресе.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    При отладки приложения может потребоваться пошаговое начало процесса отрисовки. Если веб-страницы отрисовываются на сайтах и у вас нет доступа к исходным кодам, можно использовать этот параметр, так как веб-страницы игнорируют невыявимые `?=value`  параметры.   
    
    > [!IMPORTANT]
    > После того как в URL-адресе будет найдено первое совпадение, отладка останавливается.  Невозможно одновременно отлалать два средства управления WebView2, так как порт CDP совместно используется всеми элементами управления WebView2 и использует один номер порта.  
    
*   Отлагивание запущенных процессов  
    
    Возможно, вам потребуется присоединить отладчий отладок к запущенным процессам WebView2. Для этого в `launch.json` окнах обновим `request` параметр до `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Чтобы разрешить отладку управления WebView2, необходимо открыть порт CDP.  Перед запуском отладка код должен быть создан таким образом, чтобы только один из них был открыт с помощью порта chrome Developer Protocol (CDP).  
    
*   Параметры отлаки  
    
    Добавьте параметр `trace` в launch.js, чтобы включить трассировку отлаки.  
    
    1.  Добавьте `trace` параметр.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Сохраните выходные данные отлаки в файле журнала." lightbox="./media/tracelog.png":::
                 Сохранение выходных данных отлаки в файле журнала  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Подробный вывод" lightbox="./media/verbose.png":::
                 Visual Studio отлаки кода с включенной подробной трассировой  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Отлаговка надстроек Office.
    
    Если вы отладка надстроек Office, откройте исходный код надстройки в отдельном экземпляре Visual Studio Code.  Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладник к надстройки Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Устранение неполадок отладки  
    
    При использовании отладка могут возникнуть следующие сценарии.  
    
    *   Отладка не останавливается в точке останова, и вы вывод отладки.  Чтобы устранить проблему, подтвердим, что файл с точкой останова тот же, что используется в веб-view2.  Отладка не выполняет сопоставление исходных путей.  
    *   Вы не можете присоединяться к запущенным процессам, и вы получаете ошибку времени.  Чтобы устранить эту проблему, подтвердим, что для управления WebView2 открыт порт CDP.  Убедитесь, что значение в  `additionalBrowserArguments`  реестре правильное или параметры правильные.  Дополнительные сведения см. в дополнительных [данныхBrowserArguments для dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [additionalBrowserArguments для Win32.][Webview2ReferenceWin32Webview2IdlParameters]  
    
* * *  

## См. также  

*   Руководства по началу работы с WebView2 см. в руководстве [по началу работы с WebView2.][Webview2MainGettingStarted]  
*   Полный пример возможностей WebView2 см. в репозитарии [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.
*   Дополнительные сведения об API WebView2 см. в справочнике [по API.][Webview2ApiReference]
*   Дополнительные сведения о WebView2 см. в [поддоме "Ресурсы WebView2".][Webview2MainNextSteps]
    
## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment — Globals | Документы Майкрософт"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности - Отладатель JavaScript для Visual Studio Code — microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Приложения Microsoft Edge (Chromium) WebView — код Visual Studio отладка для Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
