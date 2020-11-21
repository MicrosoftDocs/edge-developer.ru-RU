---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода Visual Studio
title: Отладка Microsoft EDGE (Chromium) из кода Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182507"
---
# Отладчик для расширения кода Microsoft Edge Visual Studio  

С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio выполните отладку клиентского кода JavaScript по строкам и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладчик для расширения кода пограничного сервера Visual Studio на работе" lightbox="./media/debugger-for-edge.gif":::
   Отладчик для расширения кода пограничного сервера Visual Studio на работе  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## Запуск Microsoft Edge  

Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \) на **панели действий**.  Если у вас нет каких бы то ни было конфигураций в коде Visual Studio, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .  Выберите **ребро** в раскрывающемся списке.  Вы увидите `launch.json` файл со следующей конфигурацией.  

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

При нажатии `F5` на Windows или macOS или нажатии зеленой кнопки **воспроизведения** код Visual Studio запускает Microsoft Edge \ (EdgeHTML \), и вы можете выполнять отладку любого веб-проекта, который вы используете для порта, `8080` прямо из кода Visual Studio!  

### Microsoft Edge (на основе Chromium)  

Если вы хотите запустить Microsoft Edge \ (Chromium \), новый Microsoft EDGE вместо Microsoft Edge \ (EdgeHTML \), просто добавьте `version` атрибут в существующую конфигурацию с помощью версии Microsoft Edge \ (Chromium \), которую вы хотите запустить \ ( `dev` , `beta` или `canary` \).  В приведенной ниже конфигурации ниже показано, как запустить Канарские версию Microsoft Edge \ (Chromium \).  

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

## Присоединение к Microsoft Edge  

Прикрепите код Visual Studio к Microsoft Edge \ (Chromium \).  На своем терминале выполните следующую команду:  

```shell
start msedge --remote-debugging-port=9222
```  

Добавьте в файл указанную ниже конфигурацию `launch.json` .   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

Если теперь выполнить эту настройку, код Visual Studio прикрепляется к Microsoft Edge \ (Chromium \) и запускает отладку.  

## Связь с элементами для группы расширения кода Microsoft Edge Visual Studio    

Отправьте отзыв, выполнив в [репозитории][GithubMicrosoftVscodeEdgeDebug2] сообщение о том, что у вас [есть вопрос][GithubMicrosoftVscodeEdgeDebug2NewIssue] в расширении.  Укажите файл журнала адаптера отладки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .  Перетащите этот файл в комментарий вопроса, чтобы отправить его в GitHub.  

Чтобы лучше сделать элементы для расширения кода Microsoft Edge Visual Studio более привлекательными, ваши публикации будут рады!  Найдите все, что вам нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDebug2] на расширение.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "отладчик для расширения кода Visual Studio EDGE в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая ошибка — Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
