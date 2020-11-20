---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода VS
title: Отладка Microsoft EDGE (Chromium) из кода VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: d9f33a17db7083a6a7cbb013dbf9886755f92c5e
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182303"
---
# Отладчик для расширения кода Microsoft Edge VS  

С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS выполните отладку клиентского кода JavaScript по строкам и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode]!  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладчик для расширения кода EDGE на работе":::
   Отладчик для расширения кода EDGE на работе  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## Запуск Microsoft Edge  

Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \) на **панели действий**.  Если у вас нет каких бы то ни было конфигураций в коде VS, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .  Выберите **ребро** в раскрывающемся списке.  Вы увидите `launch.json` файл со следующей конфигурацией.  

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

Если вы нажмете клавишу `F5` Windows или macOS или выбираете зеленую кнопку **воспроизведения** , код VS запускает Microsoft Edge \ (EdgeHTML \), и вы сможете выполнять отладку любого веб-проекта, который вы используете на порту `8080` прямо из кода VS!  

### Microsoft Edge (на основе Chromium)  

Если вы хотите запустить Microsoft Edge \ (Chromium \), следующую версию Microsoft EDGE, вместо Microsoft Edge \ (EdgeHTML \), просто добавьте `version` атрибут к существующей конфигурации с помощью версии Microsoft Edge \ (Chromium \), которую вы хотите запустить \ ( `stable` ,, `dev` `beta` или `canary` \). В приведенной ниже конфигурации ниже показано, как запустить Канарские версию Microsoft Edge \ (Chromium \).  

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

Прикрепление кода к Microsoft Edge \ (Chromium \).  На своем терминале выполните следующую команду:  

```console
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

Если сейчас выполнить эту настройку, код VS прикрепляется к Microsoft Edge \ (Chromium \) и начнет отладку.  

## Связь с элементами для группы расширения кода Microsoft Edge VS    

Отправьте отзыв, выполнив в [репозитории][GithubMicrosoftVscodeEdgeDebug2] сообщение о том, что у вас [есть вопрос][GithubMicrosoftVscodeEdgeDebug2NewIssue] в расширении.  Укажите файл журнала адаптера отладки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .  Перетащите этот файл в комментарий вопроса, чтобы отправить его в GitHub.  

Чтобы лучше сделать элементы для расширения кода Microsoft EDGE более качественными, вы можете воспользоваться вашими публикациями!  Найдите все, что вам нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDebug2] на расширение.  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "отладчик для расширения кода Edge VS в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая ошибка — Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
