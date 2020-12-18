---
description: Обновление протокола Microsoft Edge DevTools
title: Обновление протокола Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 15b13e2b93d1dbd013a82ea52b643071fa5b6f7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235608"
---
# Обзор протокола DevTools Microsoft Edge (Chromium)  

С переходом платформы Microsoft Edge на Chromium протокол [Microsoft Edge (EdgeHTML) DevTools](../edgehtml/devtools-protocol/index.md) не будет получать дополнительные обновления.  Протокол Microsoft Edge \(Chromium\) DevTools будет соответствовать API протокола Chrome DevTools в будущем.  

Документацию по этим доменам и методам можно найти, обратившись к средству просмотра протокола [Chrome DevTools.](https://chromedevtools.github.io/devtools-protocol/tot/)  

> [!NOTE]
> Любые методы с префиксом в протоколе `ms` [DevTools Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) больше не поддерживаются в протоколе Microsoft Edge \(Chromium\) DevTools.  

## Использование протокола DevTools  

Вот как присоединить настраиваемый клиент инструментов к серверу DevTools в Microsoft Edge \(Chromium\).  

1.  Убедитесь, что все экземпляры Microsoft Edge \(Chromium\) закрыты.  
1.  Запустите Microsoft Edge \(Chromium\) с удаленным портом отладки:. 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  При желании можно запустить отдельный экземпляр Edge с использованием отдельного профиля пользователя.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  Затем используйте конечную точку HTTP, чтобы получить список конечных объектов страниц с возможностью `list` прикрепления.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Наконец, подключите нужный целевой объект и выдав команды/подпишитесь на сообщения о событиях через сервер `webSocketDebuggerUrl` веб-sockets DevTools.  

## Конечные точки HTTP протокола DevTools  

Протокол DevTools Microsoft Edge \(Chromium\) поддерживает следующие конечные точки HTTP.  

## /json/version  

Предоставляет сведения о браузере хост-компьютера и поддерживаемой версии протокола DevTools.  

**Параметры**  

**Нет**  

**Объект Return**  

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```  

## /json/protocol  

Предоставляет всю поверхность API протокола, сериализованную как JSON.  

**Параметры**  

**Нет**  

**Объект Return**  

Объект JSON, который представляет доступную поверхность API для текущей версии протокола.  

## /json/list  

Предоставляет список кандидатов целевых объектов страницы для отладки.  

**Параметры**  

**Нет**  

**Объект Return**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## /json/close  

Закрывает целевой процесс \(например, в Microsoft Edge \(Chromium\), закрывает вкладку страницы\).  

**Параметры**  

Целевой ИД  

**Объект Return**  

```
String(“Target is closing”)
```  

## Удаленные инструменты для Microsoft Edge (бета-версия)  

Теперь вы можете установить удаленные инструменты [для Microsoft Edge (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) из [Microsoft Store.](https://www.microsoft.com/store/apps/windows)  Это приложение позволяет удаленно отладить Microsoft Edge (Chromium), запущенный на устройстве с Windows 10, с компьютера разработчика.  

Чтобы узнать, как настроить устройство с Windows 10 и подключиться к нем с компьютера разработчика, перейдите к началу работы с удаленной отладке [устройств с Windows 10.](../devtools-guide-chromium/remote-debugging/windows.md)  

Удаленные инструменты [для Microsoft Edge (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) используют тот же протокол Microsoft Edge (Chromium) [DevTools, что и DevTools,](../devtools-guide-chromium/index.md) для связи с Microsoft Edge, запущенным на устройстве с Windows 10, которое нужно отладить.  Перед каждым вызовом протокола приложение просто заранее и ид процесса `/msedge/` ( `pid` ).  Он поддерживает следующие конечные точки HTTP.  

### /msedge/json/list  

Предоставляет список кандидатов всех процессов \(включая PWAs и все вкладки во всех экземплярах Microsoft Edge\) на устройстве `msedge.exe` с Windows 10 для отладки. [](../progressive-web-apps-chromium/index.md)  

**Параметры**  

**Нет**  

**Объект Return**  

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, ...  ]
```  

### /msedge/  

Функционально эквивалентно [/msedge/json/list.](#msedgejsonlist)  

### /msedge/[pid]/json/list  

Предоставляет список кандидатов целевых объектов страницы для экземпляра Microsoft Edge, который соответствует предоставленной `[pid]` для отладки.  

**Параметры**  

**Нет**  

**Объект Return**  

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, ...  ]
```  

### /msedge/[pid]/json/version  

Предоставляет сведения об экземпляре Microsoft Edge, который соответствует предоставленной версии и поддерживаемой версии `[pid]` протокола DevTools.  

**Параметры**  

**Нет**  

**Объект Return**  

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```  

### /msedge/[pid]/json/protocol/  

Предоставляет всю поверхность API протокола, сериализованную как JSON для экземпляра Microsoft Edge, который соответствует `[pid]` предоставленному.  

**Параметры**  

**Нет**  

**Объект Return**  

Объект JSON, который представляет доступную поверхность API для версии протокола, используемой экземпляром Microsoft Edge, который соответствует `[pid]` предоставленной версии.  
