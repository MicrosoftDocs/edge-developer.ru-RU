---
description: Справка по домену наложения. Домен наложения предоставляет визуальные эффекты и взаимодействие при выборе узла
title: Домен наложения — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: dcf5feff9983aa2e9e61ac0569938988812165f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235186"
---
# Наложение

Домен наложения предоставляет визуальные эффекты и взаимодействие при выборе узла

| | |
|-|-|
| [**Методы**](#methods) | [enable,](#enable) [disable,](#disable) [setInspectMode](#setinspectmode) |
| [**Мероприятия**](#events) | [inspectNodeRequested](#inspectnoderequested), [nodeHighlightRequested](#nodehighlightrequested) |
| [**Зависимости**](#dependencies) | [DOM](dom.md) |
## Методы

### "Включить"
Включает отчеты о <code>nodeHighlightRequested</code> <code>inspectElementRequested</code> событиях и событиях

</p>

---

### "Отключить" 
Отключает отчеты о событиях домена наложения

</p>

---

### setInspectMode
Задает режим выбора элементов для клиента

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
            <td>mode</td>
            <td><code class="flyout">string</code></td>
            <td>Режим проверки.  Допустимые значения: searchForNode и none.</td>
        </tr>
        <tr>
            <td>highlightConfig <br/> <i>необязательные</i></td>
            <td><a href="dom.md#highlightconfig"><code class="flyout">DOM.HighlightConfig</code></a></td>
            <td>Конфигурация выделения, используемая при проверке</td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### inspectNodeRequested
Сообщает клиенту, что пользователь запросит проверку определенного узла

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
            <td>backendNodeId</td>
            <td><a href="dom.md#backendnodeid"><code class="flyout">DOM.BackendNodeId</code></a></td>
            <td>ИД запрашиваемого узла на тыловом узле</td>
        </tr>
    </tbody>
</table>
</p>

---

### nodeHighlightRequested
Указывает, что пользователь наведении курсор на узел и может проверить узел

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
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td>ИД узла, который рассматривается</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[DOM](dom.md)
