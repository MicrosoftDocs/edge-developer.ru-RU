---
description: Справочник по домену DOMDebugger. Отладка DOM позволяет устанавливать точки останова для определенных операций и событий DOM. Выполнение JavaScript остановится для этих операций, как если бы был установлен обычный набор точек останова.
title: Домен DOMDebugger — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d97a9a8f2d0e49166f5f081e8bb0c0d5d3cdd93f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235188"
---
# DOMDebugger

Отладка DOM позволяет устанавливать точки останова для определенных операций и событий DOM. Выполнение JavaScript остановится для этих операций, как если бы был установлен обычный набор точек останова.

| | |
|-|-|
| [**Методы**](#methods) | [setInstrumentationBreakpoint](#setinstrumentationbreakpoint), [removeInstrumentationBreakpoint](#removeinstrumentationbreakpoint) |
## Методы

### setInstrumentationBreakpoint
<span><b>Экспериментальная. </b></span>Задает точку останова для конкретного события.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>eventName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя инструмента для остановки. Допустимые значения: 'scriptFirstStatement'.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeInstrumentationBreakpoint
<span><b>Экспериментальная. </b></span>Удаляет точку останова для определенного события.

<table>
    <thead>
        <tr>
            <th>Параметры</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>eventName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя инструмента для остановки. Допустимые значения: 'scriptFirstStatement'.</td>
        </tr>
    </tbody>
</table>
</p>

---
