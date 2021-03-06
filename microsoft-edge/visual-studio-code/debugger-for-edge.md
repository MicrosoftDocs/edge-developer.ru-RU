---
description: Отладка Microsoft Edge (Chromium) и Microsoft Edge (EdgeHTML) из Visual Studio Code
title: Отладка Microsoft Edge (Chromium) из Visual Studio кода
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, debugger
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399297"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a>Отладка для microsoft Edge Visual Studio расширения кода  

С [расширением кода Debugger][VisualstudioMarketplaceDebuggerMicrosoftEdge] для Microsoft Edge Visual Studio отладите переднюю строку кода JavaScript по очереди и см. отчеты непосредственно из `console.log()` [Visual Studio Code!][VisualstudioCode]  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладка для расширения Visual Studio edge на работе" lightbox="./media/debugger-for-edge.gif":::
   Отладка для расширения Visual Studio edge на работе  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a>Запуск Microsoft Edge  

Перейдите к представлению отладки \( в `Ctrl` + `Shift` + `D` Windows или `Command` + `Shift` + `D` macOS\) в **панели действий.**  Если в коде Visual Studio нет конфигураций, выберите в Windows или macOS или выберите `F5` зеленую **кнопку Play.**  Выберите **Edge** в отсеве.  Вы должны увидеть `launch.json` файл со следующей конфигурацией.  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

Если вы выберите на Windows или macOS или снова выберите зеленую кнопку Play, Visual Studio Code запускает `F5` Microsoft Edge \(EdgeHTML\) и вы можете отладить любой веб-проект, запущенный в порту непосредственно из Visual Studio **** `8080` Code!  

### <a name="microsoft-edge-chromium"></a>Microsoft Edge (на основе Chromium)  

Если вы хотите запустить Microsoft Edge \(Chromium\), новый Microsoft Edge, а не Microsoft Edge \(EdgeHTML\), просто добавьте атрибут к существующей конфигурации с версией `version` Microsoft Edge \(Chromium\) вы хотите запустить \( `dev` , или `beta` `canary` \).  Следующая конфигурация ниже запускает канареевую версию Microsoft Edge \(Chromium\).  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## <a name="attaching-to-microsoft-edge"></a>Присоединение к Microsoft Edge  

Прикрепить Visual Studio к Microsoft Edge \(Chromium\).  Из терминала запустите следующую команду.  

```shell
start msedge --remote-debugging-port=9222
```  

Добавьте конфигурацию ниже в `launch.json` файл.   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Если вы запустите эту конфигурацию, Visual Studio код прикрепится к Microsoft Edge \(Chromium\) и запустите отладку.  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a>Контакт с командой расширения кода Elements for Microsoft Edge Visual Studio кода    

Отправьте свои [отзывы, подав жалобу][GithubMicrosoftVscodeEdgeDebug2NewIssue] в репозитарий [GitHub][GithubMicrosoftVscodeEdgeDebug2] о расширении.  Включите файл журнала адаптера отключки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .  Перетащите этот файл в комментарий проблемы, чтобы загрузить его в GitHub.  

Чтобы помочь сделать расширение кода Elements для Microsoft Edge более Visual Studio, ваши вклады приветствуются!  Найдите все необходимое для начала в репозитарии [GitHub][GithubMicrosoftVscodeEdgeDebug2] расширения.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger for Edge Visual Studio в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Код"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio Код"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая проблема — microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  
