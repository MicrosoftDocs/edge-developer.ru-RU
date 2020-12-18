---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55575e54b9125d7ff544c23c81da4b15d3b56fb1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235577"
---
# Домен страницы — протокол DevTools версии 0.1 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.

| | |
|-|-|
| [**Методы**](#methods) | [включить,](#enable) [отключить,](#disable) [перейти](#navigate) |
| [**Типы**](#types) | [FrameId](#frameid) |
## Методы

### "Включить"
Включает уведомления домена страницы.


---

### "Отключить" 
Отключает уведомления домена страницы.


---

### переход
Переходит на текущую страницу по заданным URL-адресам.

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
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес для навигации по странице.</td>
        </tr>
    </tbody>
</table>
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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td><span><b>Экспериментальная. </b></span>ИД кадра, который будет перемещаться.</td>
        </tr>
    </tbody>
</table>

---

## Типы

### <a name="frameid"></a> FrameId `string`

Уникальный идентификатор кадра.


---
