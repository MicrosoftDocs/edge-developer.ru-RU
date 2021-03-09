---
description: Узнайте, как отлаговка элементов управления WebView2.
title: Начало отладки приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: 140e09e508fa97f2d124f264d7d2ff77d12d1ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "11399846"
---
# <a name="get-started-debugging-webview2-apps"></a>Начало отладки приложений WebView2  

Цель управления Microsoft Edge WebView2 состоит в том, чтобы объединить лучшие функции и средства разработки веб-и родных приложений.  При разработке приложения WebView2 необходимо отчудить приложение.  В этой статье описаны различные средства, которые можно использовать для отлажений веб-кода и родного кода в приложении WebView2.  

## [<a name="microsoft-edge-devtools"></a>Microsoft Edge DevTools](#tab/devtools)  

Используйте средства разработчика [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-контента, отображаемого в средствах управления WebView2, так же, как вы можете отладить другую веб-страницу, отображаемую в Microsoft Edge.  Чтобы открыть DevTools, установите фокус на управление WebView и используйте одно из следующих действий.  

*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню \(правой кнопкой мыши\) и выберите `Inspect` .  
    
Дополнительные сведения перейдите к [обзору DevTools.][DevtoolsGuideChromiumMain]  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   Отладка DevTools  
:::image-end:::  

## [<a name="visual-studio"></a>VisualStudio](#tab/visualstudio)  

Visual Studio предоставляет различные средства отладки для веб-и родного кода в приложениях WebView2.  В разделе Visual Studio основное внимание уделяется отладки элементов управления WebView, однако другие методы отладки в Visual Studio доступны в обычном режиме.  Используйте следующий процесс для отлажений веб-и родного кода в приложениях Win32 или надстройки Office.  

> [!IMPORTANT]
> Если отладить приложение в Visual Studio с подключенным отладильщиком, выбор может вызвать отладку, а не `F12` средства разработчика.  Выберите `Ctrl` + `Shift` + `I` или используйте контекстное меню \(правой кнопкой мыши\), чтобы избежать ситуации.  

Перед началом работы убедитесь, что следующие требования будут выполнены.  

*   Чтобы отламыть скрипты, приложение должно быть запущено из Visual Studio.  
*   Нельзя прикрепить отладка к запущенной процедуре WebView2.  
*   Установка Visual Studio версии 16.4 Preview 2 или более поздней версии 2.  
    
Установка и настройка средств отладки сценариев в Visual Studio.  

1.  Выполните следующие действия по установке компонента **диагностики JavaScript** в разработке настольных компьютеров **с помощью C++**.  
    
    1.  В панели Обозреватель Windows введите `Visual Studio Installer` .  
    1.  Выберите **Visual Studio установщик,** чтобы открыть его.  
    1.  В Visual Studio установщике в установленной версии выберите кнопку **More,** а затем **измените**.  
    1.  В Visual Studio **в статье Workloads**выберите параметр **Desktop Development в параметре C++.**  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Экран изменения рабочих нагрузок" lightbox="./media/workloads.png":::
            Visual Studio Экран изменения рабочих нагрузок
        :::image-end:::  
        
    1.  Выберите **отдельные компоненты.**  
    1.  В поле поиска введите `JavaScript diagnostics` .  
    1.  Выберите параметр **диагностики JavaScript.**  
    1.  Выберите **Изменение**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Изменение вкладки отдельных компонентов" lightbox="./media/indivcomp.png":::
           Visual Studio Изменение вкладки отдельных компонентов  
        :::image-end:::  
        
1.  Включить отладку скриптов для приложений WebView2.  
    1.  В проекте WebView2 откройте контекстное меню \(правой кнопкой мыши\) и выберите **Свойства**.  
    1.  В статье **Configuration Properties**выберите **отладку.**  
    1.  В соответствии **с типом Debugger**выберите **JavaScript (WebView2).**  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio отладки свойства конфигурации" lightbox="./media/enbjs.png":::
           Visual Studio **отладки свойства** конфигурации  
        :::image-end:::  
        
Выполните следующие действия для отлаговки приложения WebView2.  

1.  Чтобы установить точку разрыва в исходный код, наведите курсор слева от номера строки и выберите точку разрыва.  Адаптер отлажений JS/TS не выполняет сопоставление исходных путей.  Необходимо открыть тот же путь, который связан с веб-сайтом WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio точку разрыва" lightbox="./media/breakpoint.png"::: 
       Visual Studio точку разрыва  
    :::image-end:::  
    
1.  Чтобы запустить отладку, выберите размер бита платформы, а затем выберите зеленую кнопку воспроизведения рядом с **локальным Отладильщиком Windows.**  Приложение запускается, а отладка подключается к первому созданному процессу WebView2.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio отладка Windows" lightbox="./media/run.png"::: 
       Visual Studio **отладка Windows**  
    :::image-end:::  
    
1.  В консоли **отладки**найдите выход из отладки.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio отлаговка консоли" lightbox="./media/console.png"::: 
       Visual Studio **отлаговка консоли**  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a>Visual Studio Code](#tab/visualstudiocode)  

Используйте Код Visual Studio Майкрософт для отлаговки скриптов, запускаемой в средствах управления WebView2.  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

В Visual Studio коде выполните следующие действия по отламыву кода. 

1.  В проекте должен быть `launch.json` файл.  Если в проекте нет файла, скопируйте следующий фрагмент кода `launch.json` и создайте `launch.json` новый файл.  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > Visual Studio для сопоставления исходных путей кода теперь требуется URL-адрес, поэтому ваше приложение получает параметр командной строки при его старте.  При необходимости можно смело игнорировать `url` параметр.  
    
1.  Чтобы установить точку разрыва в исходный код, наведите курсор на строку и выберите `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Точка breakpoint установлена в Visual Studio коде" lightbox="./media/breakpointvs.png":::
       Точка breakpoint установлена в Visual Studio коде  
    :::image-end:::
    
1.  Запустите код.  
    1.  На **вкладке Run** выберите конфигурацию запуска из меню отсев.  
    1.  Чтобы начать отладку приложения, выберите Пуск отладки, который является зеленым треугольником рядом с падением конфигурации запуска.  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio вкладка "Запуск кода"" lightbox="./media/runvs.png":::
           Visual Studio вкладка "Запуск кода"  
        :::image-end:::  
        
1.  Откройте **консоль отлаговка,** чтобы просмотреть выход отлагирования и ошибки.  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio консоли отлаговка кода" lightbox="./media/resultsvs.png":::
       Visual Studio консоли отлаговка кода  
    :::image-end:::  
    
**Расширенные параметры:**  

*   Целевое отладка веб-просмотров. 
    
    В некоторых приложениях WebView2 можно использовать несколько устройств управления WebView2. Чтобы выбрать управление WebView2 для отладки в этой ситуации, можно использовать целевое отладку webview2 
    
    Откройте `launch.json` и выполните следующие действия, чтобы использовать целевое отладка веб-просмотров.  
    
    1.  Подтверди, `useWebview` что задан параметр `true` .  
    1.  Добавьте `urlFilter` параметр.  При переходе управления WebView2 на URL-адрес значение параметра используется для сравнения строк, которые `urlFilter` отображаются в URL-адресе.  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    При отладе приложения может потребоваться пройти код с самого начала процесса отрисовки. Если вы отрисовываю веб-страницы на сайтах и у вас нет доступа к исходным кодам, вы можете использовать этот параметр, так как веб-страницы игнорируют неузнаваемые `?=value`  параметры.   
    
    > [!IMPORTANT]
    > После первого совпадения в URL-адресе отладка прекращается.  Нельзя одновременно отламыть два управления WebView2, так как порт CDP используется всеми средствами управления WebView2 и использует один номер порта.  
    
*   Отлачив процессы запуска  
    
    Возможно, потребуется прикрепить отладка к запущенным процессам WebView2. Чтобы сделать это, в `launch.json` , обновить `request` параметр `attach` .
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    Чтобы разрешить отладку управления WebView2, необходимо открыть порт CDP.  Код должен быть создан для того, чтобы перед запуском отладки только один контроль WebView2 открыл порт Протокола разработчика Chrome (CDP).  
    
*   Параметры отслеживания отлаговок  
    
    Добавьте параметр `trace` в launch.js, чтобы включить трассировку отлаговок.  
    
    1.  Добавьте `trace` параметр.  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Сохранение вывода отлаговки в файл журнала." lightbox="./media/tracelog.png":::
                 Сохранение вывода отлаговки в файл журнала  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Многословный вывод" lightbox="./media/verbose.png":::
                 Visual Studio отламывка кода с включенной многословной трассировой  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   Отламывка надстроек Office.  
    
    Если вы отладка надстроек Office, откройте исходный код надстройки в отдельном экземпляре Visual Studio Code.  Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладка к надстройки Office.
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   Устранение неполадок отладки  
    
    При использовании отладки можно столкнуться со следующими сценариями.  
    
    *   Отладка не останавливается на точке разрыва, и у вас есть отладка вывода.  Чтобы решить проблему, подтвердим, что файл с точкой разрыва — это тот же файл, который используется с помощью управления WebView2.  Отладка не выполняет сопоставление исходных путей.  
    *   Вы не можете прикрепиться к запущенным процессам, и вы получите ошибку времени.  Чтобы решить проблему, подтвердим, что управление WebView2 открыло порт CDP.   `additionalBrowserArguments` Убедитесь, что значение в реестре правильное или правильные параметры.  Дополнительные сведения перейдите в [дополнительныеBrowserArguments для dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [дополнительныеBrowserArguments для Win32][Webview2ReferenceWin32Webview2IdlParameters].  
    
* * *  

## <a name="see-also"></a>См. также  

*   Чтобы начать работу с webView2, перейдите к руководствам по началу [webView2.][Webview2MainGettingStarted]  
*   Для полного примера возможностей WebView2 перейдите к [репо WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.
*   Дополнительные сведения об API WebView2 перейдите по ссылке [API.][Webview2ApiReference]
*   Дополнительные сведения о WebView2 перейдите в [webView2 Resources.][Webview2MainNextSteps]
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Контакт с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Документы Майкрософт"  
[Webview2ApiReference]: ../webview2-api-reference.md "Ссылка на API API Microsoft Edge WebView2 | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Примеры WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
