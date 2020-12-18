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
# Заметки о выпуске протокола DevTools версии 0.1

> [!NOTE]
> Протокол Microsoft Edge DevTools работает только в сборках Windows 10 с обновлением за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)

Версия 0.1 протокола Microsoft **Edge DevTools** предоставляет предварительную предварительную версию для тестирования инструментирования EdgeHTML и базовой удаленной отладки в новом автономном приложении [Microsoft Edge DevTools Preview.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Таким образом, необходимо использовать Windows 10 с обновлением за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) г. или более поздней сборкой [Windows Insider Preview.](https://insider.windows.com/en-us/getting-started/)

Цели протокола DevTools в три раза:

 - Предоставление общего API для нашего приложения DevTools для оказания поддержки Microsoft Edge
 - Расширение доступа к функциям DevTools для внешних клиентов инструментов
 - Включить удаленную отладку на различных устройствах с Windows 10 под управлением Microsoft Edge 

Этот предварительный выпуск предоставляет основные функции отладки, такие как установка точек останова, пошаговое изучение кода и изучение трассировок стека. В пользовательском интерфейсе Edge DevTools это преобразуется [****](../../devtools-guide/debugger.md) в функциональные возможности, доступные на панели отладки, за вычетом проверки кэша (для веб-хранилища, рабочих служб, API кэша и IndexedDB). 

Дополнительные функции отладки будут добавлены в предстоящих выпусках, а инструментарий будет использовать другие панели [DevTools.](../index.md)
