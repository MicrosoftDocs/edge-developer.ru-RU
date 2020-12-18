---
description: Заметки о выпуске протокола Microsoft Edge DevTools версии 0.1
title: Заметки о выпуске протокола DevTools версии 0.1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60e92cb3afa9b10b15c8ebdd520c0061fbb3b366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235571"
---
# <span data-ttu-id="86846-103">Заметки о выпуске протокола DevTools версии 0.1</span><span class="sxs-lookup"><span data-stu-id="86846-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="86846-104">Протокол Microsoft Edge DevTools работает только в сборках Windows 10 с обновлением за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)</span><span class="sxs-lookup"><span data-stu-id="86846-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="86846-105">Версия 0.1 протокола Microsoft **Edge DevTools** предоставляет предварительную предварительную версию для тестирования инструментирования EdgeHTML и базовой удаленной отладки в новом автономном приложении [Microsoft Edge DevTools Preview.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab)</span><span class="sxs-lookup"><span data-stu-id="86846-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="86846-106">Таким образом, необходимо использовать Windows 10 с обновлением за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. или более поздней сборкой [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)</span><span class="sxs-lookup"><span data-stu-id="86846-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="86846-107">Цели протокола DevTools в три раза:</span><span class="sxs-lookup"><span data-stu-id="86846-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="86846-108">Предоставление общего API для нашего приложения DevTools для оказания поддержки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="86846-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="86846-109">Расширение доступа к функциям DevTools для внешних клиентов инструментов</span><span class="sxs-lookup"><span data-stu-id="86846-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="86846-110">Включить удаленную отладку на различных устройствах с Windows 10 под управлением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="86846-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="86846-111">Этот предварительный выпуск предоставляет основные функции отладки, такие как установка точек останова, пошаговое изучение кода и изучение трассировок стека.</span><span class="sxs-lookup"><span data-stu-id="86846-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="86846-112">В пользовательском интерфейсе Edge DevTools это преобразуется [\*\*\*\*](../../devtools-guide/debugger.md) в функциональные возможности, доступные на панели отладки, за вычетом проверки кэша (для веб-хранилища, рабочих служб, API кэша и IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="86846-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="86846-113">Дополнительные функции отладки будут добавлены в предстоящих выпусках, а инструментарий будет использовать другие панели [DevTools.](../index.md)</span><span class="sxs-lookup"><span data-stu-id="86846-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../index.md) panels.</span></span>
