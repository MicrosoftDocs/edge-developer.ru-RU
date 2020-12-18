---
description: Новые возможности Microsoft Edge DevTools в обновлении Windows 10 за октябрь 2018 г.
title: Новые возможности Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1d3c6fe5bf061186d5c6593a115a8b6794c0dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235587"
---
# <span data-ttu-id="cd997-104">Средства разработчика в последнем обновлении для Windows 10 (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="cd997-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="cd997-105">Последнее обновление Microsoft Edge DevTools добавляет ряд удобных функций как в пользовательский интерфейс, так [\*\*](#service-workers-panel) и на первый [](#source-file-search-tools) план, включая новые выделенные панели для сотрудников службы и [*хранилища,*](#storage-panel)средства поиска исходных файлов в отладке и новые домены протокола [Edge DevTools](#edge-devtools-protocol-updates) для отладки стилей и макетов и консольных API.</span><span class="sxs-lookup"><span data-stu-id="cd997-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="cd997-106">Ниже представлены последние функции Microsoft Edge DevTools, доступные в обновлении Windows 10 за октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г.[(EdgeHTML 18).](https://aka.ms/devguide_edgehtml_18)</span><span class="sxs-lookup"><span data-stu-id="cd997-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="cd997-107">Кроме того, мы исправили ряд ошибок с доступностью, надежностью и производительностью, чтобы улучшить основы!</span><span class="sxs-lookup"><span data-stu-id="cd997-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="cd997-108">Приложение DevTools</span><span class="sxs-lookup"><span data-stu-id="cd997-108">DevTools app</span></span>

<span data-ttu-id="cd997-109">Мы обновили приложение Microsoft [Edge DevTools Preview.](./index.md#microsoft-store-app)</span><span class="sxs-lookup"><span data-stu-id="cd997-109">We've updated the standalone [Microsoft Edge DevTools Preview app](./index.md#microsoft-store-app).</span></span> <span data-ttu-id="cd997-110">Последний выпуск включает удаленный доступ отладки к основным [\*\*\*\*](./debugger.md)funtionality в отладке, элементах [**(для**](./elements.md) операций только для чтения) и [**панелях**](./console.md) консоли.</span><span class="sxs-lookup"><span data-stu-id="cd997-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="cd997-111">Панель "Рабочие службы"</span><span class="sxs-lookup"><span data-stu-id="cd997-111">Service Workers panel</span></span>

<span data-ttu-id="cd997-112">Теперь существует специальная [\*\*\*\*](./service-workers.md) панель "Сотрудники-службы" для проверки, управления и отладки сотрудников службы сайта.</span><span class="sxs-lookup"><span data-stu-id="cd997-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="cd997-113">Это обеспечивает те же функциональные \*\* возможности, что и в панели отладки (теперь с менее переполненным пользовательским интерфейсом)..</span><span class="sxs-lookup"><span data-stu-id="cd997-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Панель "Рабочие службы"](./media/service_worker.png)

## <span data-ttu-id="cd997-115">Панель хранения</span><span class="sxs-lookup"><span data-stu-id="cd997-115">Storage panel</span></span>

<span data-ttu-id="cd997-116">Мы также переместили все локальные инспекторы хранилища *(local and Sesion Storage, IndexedDB, Cookies, Cache)* ранее в отладке на собственную выделенную панель [**хранения.**](./storage.md) \*\*</span><span class="sxs-lookup"><span data-stu-id="cd997-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Панель хранения](./media/storage_cache.png)

## <span data-ttu-id="cd997-118">Средства поиска исходных файлов</span><span class="sxs-lookup"><span data-stu-id="cd997-118">Source file search tools</span></span>

<span data-ttu-id="cd997-119">Теперь [**в отладке**](./debugger.md) есть области [поиска исходных](./debugger.md#file-search) файлов.</span><span class="sxs-lookup"><span data-stu-id="cd997-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="cd997-120">Откройте его с помощью команды *"Найти в* файлах" (), если у вас есть определенная строка кода, который вы пытаетесь найти `Ctrl` + `Shift` + `F` в источнике.</span><span class="sxs-lookup"><span data-stu-id="cd997-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="cd997-121">Панель инструментов предоставляет различные параметры поиска, включая регулярные выражения.</span><span class="sxs-lookup"><span data-stu-id="cd997-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Поиск файлов отладки](./media/debugger_file_search.png)

<span data-ttu-id="cd997-123">Вы также можете быстро открыть любой загруженный исходный файл с помощью *команды "Открыть* `Ctrl` + `P` файл" ().</span><span class="sxs-lookup"><span data-stu-id="cd997-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Открытый файл отладки](./media/debugger_open_file.png)

## <span data-ttu-id="cd997-125">Обновления протокола Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cd997-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="cd997-126">Версия [0.2](../devtools-protocol/0.2/index.md) протокола DevTools предоставляет новые домены для отладки стиля и макета (только для чтения) и консольных API, а также основные функции отладки скриптов, введенные в версии [0.1.](../devtools-protocol/0.1/index.md)</span><span class="sxs-lookup"><span data-stu-id="cd997-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="cd997-127">В пользовательском интерфейсе Edge DevTools это преобразуется в функциональные возможности, доступные в элементах [**(для**](../devtools-guide/elements.md) операций только для [**чтения),**](../devtools-guide/console.md) панелях консоли и [\*\*\*\*](../devtools-guide/debugger.md) отладки.</span><span class="sxs-lookup"><span data-stu-id="cd997-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
