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
# <span data-ttu-id="78375-103">Конечные точки HTTP Microsoft Edge DevTools версии 0.2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="78375-103">Microsoft Edge DevTools Protocol Version 0.2 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="78375-104">Версия 0.2 протокола Microsoft Edge DevTools работает только в сборках Windows 10 с обновлением за октябрь [2018]() г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)</span><span class="sxs-lookup"><span data-stu-id="78375-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update]() and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="78375-105">**Протокол DevTools 0.2** поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="78375-105">**DevTools Protocol 0.2** supports the following HTTP endpoints.</span></span> <span data-ttu-id="78375-106">Подробнее [об использовании](../index.md#using-the-protocol) протокола для подключения к процессу [](domains/index.md) контента браузера и документации по доменам для полного API протокола devtools на основе веб-sockets.</span><span class="sxs-lookup"><span data-stu-id="78375-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="78375-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="78375-107">/json/version</span></span>
<span data-ttu-id="78375-108">Предоставляет сведения о браузере хост-компьютера и поддерживаемой версии протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="78375-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="78375-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="78375-109">Parameters</span></span>**

*<span data-ttu-id="78375-110">Нет</span><span class="sxs-lookup"><span data-stu-id="78375-110">None</span></span>*

**<span data-ttu-id="78375-111">Объект Return</span><span class="sxs-lookup"><span data-stu-id="78375-111">Return object</span></span>**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## <span data-ttu-id="78375-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="78375-112">/json/protocol</span></span>

<span data-ttu-id="78375-113">Предоставляет всю поверхность API протокола, сериализованную как JSON.</span><span class="sxs-lookup"><span data-stu-id="78375-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="78375-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="78375-114">Parameters</span></span>**

*<span data-ttu-id="78375-115">Нет</span><span class="sxs-lookup"><span data-stu-id="78375-115">None</span></span>*

**<span data-ttu-id="78375-116">Объект Return</span><span class="sxs-lookup"><span data-stu-id="78375-116">Return object</span></span>**

<span data-ttu-id="78375-117">Объект JSON, который представляет доступную поверхность API для текущей версии протокола.</span><span class="sxs-lookup"><span data-stu-id="78375-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="78375-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="78375-118">/json/list</span></span>

<span data-ttu-id="78375-119">Предоставляет список кандидатов целевых объектов страницы для отладки.</span><span class="sxs-lookup"><span data-stu-id="78375-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="78375-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="78375-120">Parameters</span></span>**

*<span data-ttu-id="78375-121">Нет</span><span class="sxs-lookup"><span data-stu-id="78375-121">None</span></span>*

**<span data-ttu-id="78375-122">Объект Return</span><span class="sxs-lookup"><span data-stu-id="78375-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="78375-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="78375-123">/json/close</span></span>

<span data-ttu-id="78375-124">Закрывает целевой процесс (например, в Microsoft Edge закрывается вкладка страницы).</span><span class="sxs-lookup"><span data-stu-id="78375-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="78375-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="78375-125">Parameters</span></span>**

<span data-ttu-id="78375-126">Целевой ИД</span><span class="sxs-lookup"><span data-stu-id="78375-126">Target ID</span></span> 

**<span data-ttu-id="78375-127">Объект Return</span><span class="sxs-lookup"><span data-stu-id="78375-127">Return object</span></span>**

```
String("Target is closing")
```
