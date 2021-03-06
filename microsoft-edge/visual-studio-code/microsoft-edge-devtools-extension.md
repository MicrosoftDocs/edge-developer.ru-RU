---
description: Использование элементов для Microsoft Edge (Chromium) из Visual Studio Кода
title: Элементы для Microsoft Edge (Chromium) из Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398457"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a>Microsoft Edge DevTools для расширения Visual Studio кода  

Использование <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] -->это расширение для доступа в Microsoft Edge DevTools внутри [Microsoft Visual Studio Code][VisualstudioCode].  У вас есть доступ к **средствам Elements** и **Network** в Microsoft Edge DevTools.  Вы можете либо запустить, либо прикрепить к экземпляру Microsoft Edge.  После подключения вы можете отобразить структуру HTML-кодов, изменить макет, устранить проблемы с укладкой и проверить сетевой трафик.  

## <a name="elements-tool"></a>Средство Elements  

По умолчанию расширение запускает экземпляр браузера в уникальном **** окне и предоставляет функциональность Элементов Microsoft Edge DevTools.  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools для Visual Studio кода с полным окном браузера" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   Microsoft Edge DevTools для Visual Studio кода с полным окном браузера  
:::image-end:::  

В параметрах расширения можно включить дополнительные функциональные возможности, такие как **Режим без головы и** **сеть.**  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Включение (или отключение) безголовых режимов и проверка сети в параметрах расширения" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   Включение режима \(или отключения\) безголовых и сетевой проверки в параметрах расширения  
:::image-end:::  

## <a name="headless-mode"></a>Режим без головы  

В безголевом режиме это расширение не запускает полный экземпляр браузера для отлаживания.  Он запускает экземпляр в фоновом режиме.  Возможно, вам придется оставаться в редакторе и взаимодействовать со встроенным браузером.  Дополнительный значок браузера не отображается в панели задач.  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools для Visual Studio кода с безголовым управлением" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   Microsoft Edge DevTools для Visual Studio кода с безголовым браузером  
:::image-end:::  

> [!NOTE]
> На macOS в качестве предпочтительного режима следует включить режим без головы.  Использование безголкового режима должно решить проблему, в которой, если окно не видно, окно браузера сообщает, что это `Not Active` .  

## <a name="network-tool"></a>Средство "Сеть"  

Если вы также хотите проверить сетевой трафик приложения, откройте параметры и включите вкладку **Network.**  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Проверка сети в Microsoft Edge DevTools для Visual Studio code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    Проверка сети в Microsoft Edge DevTools для Visual Studio code  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a>Запуск Microsoft Edge from the extension  

Перейдите к microsoft Edge Tools в **панели действий.**  Рядом с тем, где написано **Microsoft Edge Tools: Targets,** есть знак плюс, который открывает браузер для вашего приложения.  Если вы выбираете параметр **about:blank,** необходимо перейти к веб-приложению в браузере, чтобы оно появлялось в панели **Elements** в Visual Studio Code.  

## <a name="launching-microsoft-edge-from-the-debug-view"></a>Запуск Microsoft Edge из представления отлаговка  

Если вы привыкли использовать представление debug в Visual Studio коде, в него можно получить доступ к Microsoft Edge DevTools.  

1.  В Visual Studio коде перейдите к представлению Debug 
    *   Выберите `Ctrl` + `Shift` + `D` в Windows/Linux \( `Command` + `Shift` + `D` на macOS\).  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  Если в коде Visual Studio нет конфигураций, выполните одно из следующих действий.  
>     *   Выберите `F5` .  
>     *   Выберите **кнопку Play** \(green\) .  
> 1.  В отсеве выберите **Edge** в отсеве.  
> 1.  Должен `launch.json` отображаться файл, содержащий следующую конфигурацию.  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> После загрузки правильной конфигурации выполните следующее действие.  

1.  Чтобы запустить **средство Elements** из Visual Studio Code, выполните одно из следующих действий. 
    *   Выберите `F5` .  
    *   Выберите **кнопку Play** \(green\) .  
         
Теперь вы можете сделать следующие действия.  

*   Доступ к скринкасту браузера.  
*   Проверьте dom и стиль компонентов на странице.  

## <a name="attaching-to-microsoft-edge"></a>Присоединение к Microsoft Edge  

Чтобы открыть браузер и прикрепить экземпляр к Visual Studio коду, выполните следующие действия. 

1.  Чтобы открыть экземпляр Microsoft Edge \(Chromium\), скопируйте и запустите следующую команду.  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  После запуска экземпляра скопируйте и вклейте в файл следующий фрагмент `launch.json` кода.  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  В Visual Studio коде откройте выпадаемое меню **Debugger** и выберите Присоединение к Microsoft Edge и **откройте средства разработчика.**  
1.  Чтобы запустить **средство Elements** из Visual Studio Code, выполните одно из следующих действий. 
    *   Выберите `F5` .  
    *   Выберите **кнопку Play** \(green\) .  
         
Теперь вы можете сделать следующие действия.  

*   Доступ к скринкасту браузера.  
*   Проверьте dom и стиль компонентов на странице.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a>Контакт с командой microsoft Edge DevTools для Visual Studio кода  

Отправьте свои [отзывы, подав жалобу][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] на репозитарий [GitHub][GithubMicrosoftVscodeEdgeDevtools] о расширении.  

Если вы хотите помочь сделать <!--the Microsoft Edge DevTools for Visual Studio Code -->это расширение лучше, ваши вклады приветствуются.  Найдите все необходимое для начала в репозитарии [GitHub][GithubMicrosoftVscodeEdgeDevtools] расширения.  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Код"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio Код"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая проблема — microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода"  
