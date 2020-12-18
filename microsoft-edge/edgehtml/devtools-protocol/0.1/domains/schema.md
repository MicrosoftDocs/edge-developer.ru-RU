---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена схемы. Предоставляет сведения о схеме протокола.
title: Домен схемы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7b4ec71b7799ae099c673bd81fa5b15a8ddd5d27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235570"
---
# Домен схемы — протокол DevTools версии 0.1 (EdgeHTML)  

Предоставляет сведения о схеме протокола.

| | |
|-|-|
| [**Методы**](#methods) | [getDomains](#getdomains) |
| [**Типы**](#types) | [Домен](#domain) |
## Методы

### getDomains
Возвращает поддерживаемые домены.

<table>
    <thead>
        <tr>
            <th>Возвращает</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>домены</td>
            <td><a href="#domain"><code class="flyout">Domain[]</code></a></td>
            <td>Список поддерживаемых доменов.</td>
        </tr>
    </tbody>
</table>

---

## Типы

### <a name="domain"></a> Домен `object`

Описание домена протокола.

<table>
    <thead>
        <tr>
            <th>Свойства</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Доменное имя.</td>
        </tr>
        <tr>
            <td>version</td>
            <td><code class="flyout">string</code></td>
            <td>Версия домена.</td>
        </tr>
    </tbody>
</table>

---
