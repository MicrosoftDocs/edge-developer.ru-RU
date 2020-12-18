---
description: Протокол Microsoft Edge DevTools версии 0.2 поддерживает следующие конечные точки HTTP.
title: Конечные точки HTTP Microsoft Edge DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a0e100cee6a73d688b9b74a9b38d1dd37722428f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235562"
---
# Конечные точки HTTP Microsoft Edge DevTools версии 0.2 (EdgeHTML)  

> [!NOTE]
> Версия 0.2 протокола Microsoft Edge DevTools работает только в сборках Windows 10 с обновлением за октябрь [2018]() г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)

**Протокол DevTools 0.2** поддерживает следующие конечные точки HTTP. Подробнее [об использовании](../index.md#using-the-protocol) протокола для подключения к процессу [](domains/index.md) контента браузера и документации по доменам для полного API протокола devtools на основе веб-sockets.

## /json/version
Предоставляет сведения о браузере хост-компьютера и поддерживаемой версии протокола DevTools.

**Параметры**

*Нет*

**Объект Return**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## /json/protocol

Предоставляет всю поверхность API протокола, сериализованную как JSON.

**Параметры**

*Нет*

**Объект Return**

Объект JSON, который представляет доступную поверхность API для текущей версии протокола.

## /json/list

Предоставляет список кандидатов целевых объектов страницы для отладки.

**Параметры**

*Нет*

**Объект Return**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Закрывает целевой процесс (например, в Microsoft Edge закрывается вкладка страницы).

**Параметры**

Целевой ИД 

**Объект Return**

```
String("Target is closing")
```
