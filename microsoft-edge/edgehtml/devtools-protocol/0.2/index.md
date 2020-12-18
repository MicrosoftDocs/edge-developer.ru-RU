---
description: Заметки о выпуске протокола Microsoft Edge DevTools версии 0.2
title: Заметки о выпуске Протокола Microsoft Edge DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 61d8f5b00dca3505594ca41db6c80c5ba4157092
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235176"
---
# <span data-ttu-id="c6e27-103">Заметки о выпуске протокола DevTools версии 0.2</span><span class="sxs-lookup"><span data-stu-id="c6e27-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="c6e27-104">Версия 0.2 протокола Microsoft Edge DevTools работает только в сборках Windows 10 За октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/getting-started/)</span><span class="sxs-lookup"><span data-stu-id="c6e27-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="c6e27-105">Версия 0.2 протокола Microsoft **Edge DevTools** предоставляет предварительную версию для тестирования инструментирования EdgeHTML и базовой удаленной отладки в новом автономном приложении [Microsoft Edge DevTools Preview.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab)</span><span class="sxs-lookup"><span data-stu-id="c6e27-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="c6e27-106">Таким образом, необходимо использовать Обновление Windows 10 за октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г. или более поздней сборки [Windows Insider Preview.](https://insider.windows.com/getting-started/)</span><span class="sxs-lookup"><span data-stu-id="c6e27-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="c6e27-107">Цели протокола DevTools в три раза:</span><span class="sxs-lookup"><span data-stu-id="c6e27-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="c6e27-108">Предоставление общего API для нашего приложения DevTools для оказания поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6e27-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="c6e27-109">Расширение доступа к функциям DevTools для внешних клиентов инструментов</span><span class="sxs-lookup"><span data-stu-id="c6e27-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="c6e27-110">Включить удаленную отладку на различных устройствах с Windows 10 под управлением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6e27-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="c6e27-111">Версия 0.2 протокола DevTools включает новые домены для отладки стиля и макета (только для чтения) и консольных API, а также основные функции отладки сценариев, добавленные в версии 0.1.</span><span class="sxs-lookup"><span data-stu-id="c6e27-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="c6e27-112">В пользовательском интерфейсе Edge DevTools это преобразуется в [\*\*\*\*](../../devtools-guide/console.md) функциональные возможности, доступные на панелях [**"Элементы",**](../../devtools-guide/elements.md)"Консоль" и [**"Отладка".**](../../devtools-guide/debugger.md)</span><span class="sxs-lookup"><span data-stu-id="c6e27-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
