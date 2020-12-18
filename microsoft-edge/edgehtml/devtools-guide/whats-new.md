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
# Средства разработчика в последнем обновлении для Windows 10 (EdgeHTML 18)

Последнее обновление Microsoft Edge DevTools добавляет ряд удобных функций как в пользовательский интерфейс, так [**](#service-workers-panel) и на первый [](#source-file-search-tools) план, включая новые выделенные панели для сотрудников службы и [*хранилища,*](#storage-panel)средства поиска исходных файлов в отладке и новые домены протокола [Edge DevTools](#edge-devtools-protocol-updates) для отладки стилей и макетов и консольных API.

Ниже представлены последние функции Microsoft Edge DevTools, доступные в обновлении Windows 10 за октябрь [2018](/windows/uwp/whats-new/windows-10-build-17763) г.[(EdgeHTML 18).](https://aka.ms/devguide_edgehtml_18) Кроме того, мы исправили ряд ошибок с доступностью, надежностью и производительностью, чтобы улучшить основы!

## Приложение DevTools

Мы обновили приложение Microsoft [Edge DevTools Preview.](./index.md#microsoft-store-app) Последний выпуск включает удаленный доступ отладки к основным [****](./debugger.md)funtionality в отладке, элементах [**(для**](./elements.md) операций только для чтения) и [**панелях**](./console.md) консоли.

## Панель "Рабочие службы"

Теперь существует специальная [****](./service-workers.md) панель "Сотрудники-службы" для проверки, управления и отладки сотрудников службы сайта. Это обеспечивает те же функциональные ** возможности, что и в панели отладки (теперь с менее переполненным пользовательским интерфейсом)..

![Панель "Рабочие службы"](./media/service_worker.png)

## Панель хранения

Мы также переместили все локальные инспекторы хранилища *(local and Sesion Storage, IndexedDB, Cookies, Cache)* ранее в отладке на собственную выделенную панель [**хранения.**](./storage.md) **

![Панель хранения](./media/storage_cache.png)

## Средства поиска исходных файлов

Теперь [**в отладке**](./debugger.md) есть области [поиска исходных](./debugger.md#file-search) файлов. Откройте его с помощью команды *"Найти в* файлах" (), если у вас есть определенная строка кода, который вы пытаетесь найти `Ctrl` + `Shift` + `F` в источнике. Панель инструментов предоставляет различные параметры поиска, включая регулярные выражения. 

![Поиск файлов отладки](./media/debugger_file_search.png)

Вы также можете быстро открыть любой загруженный исходный файл с помощью *команды "Открыть* `Ctrl` + `P` файл" ().

![Открытый файл отладки](./media/debugger_open_file.png)

## Обновления протокола Edge DevTools

Версия [0.2](../devtools-protocol/0.2/index.md) протокола DevTools предоставляет новые домены для отладки стиля и макета (только для чтения) и консольных API, а также основные функции отладки скриптов, введенные в версии [0.1.](../devtools-protocol/0.1/index.md) В пользовательском интерфейсе Edge DevTools это преобразуется в функциональные возможности, доступные в элементах [**(для**](../devtools-guide/elements.md) операций только для [**чтения),**](../devtools-guide/console.md) панелях консоли и [****](../devtools-guide/debugger.md) отладки.
