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
# Заметки о выпуске протокола DevTools версии 0.2

> [!NOTE]
> Версия 0.2 протокола Microsoft Edge DevTools работает только в сборках Windows 10 За октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г. и более поздних версий [Windows Insider Preview.](https://insider.windows.com/getting-started/)

Версия 0.2 протокола Microsoft **Edge DevTools** предоставляет предварительную версию для тестирования инструментирования EdgeHTML и базовой удаленной отладки в новом автономном приложении [Microsoft Edge DevTools Preview.](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Таким образом, необходимо использовать Обновление Windows 10 за октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г. или более поздней сборки [Windows Insider Preview.](https://insider.windows.com/getting-started/)

Цели протокола DevTools в три раза:

 - Предоставление общего API для нашего приложения DevTools для оказания поддержки Microsoft Edge
 - Расширение доступа к функциям DevTools для внешних клиентов инструментов
 - Включить удаленную отладку на различных устройствах с Windows 10 под управлением Microsoft Edge 

Версия 0.2 протокола DevTools включает новые домены для отладки стиля и макета (только для чтения) и консольных API, а также основные функции отладки сценариев, добавленные в версии 0.1. В пользовательском интерфейсе Edge DevTools это преобразуется в [****](../../devtools-guide/console.md) функциональные возможности, доступные на панелях [**"Элементы",**](../../devtools-guide/elements.md)"Консоль" и [**"Отладка".**](../../devtools-guide/debugger.md)
