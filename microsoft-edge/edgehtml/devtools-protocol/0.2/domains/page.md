---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена страницы. Действия и события, связанные с проверенной страницей, относятся к домену страницы.
title: Домен страницы — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2f1849a2e2aa2f53cef9dff5d03ac991d368a6f3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235187"
---
# Домен страницы — протокол DevTools версии 0.2 (EdgeHTML)  

Действия и события, связанные с проверенной страницей, относятся к домену страницы.

| | |
|-|-|
| [**Методы**](#methods) | [включить,](#enable) [отключить,](#disable) [перейти,](#navigate) [getFrameTree](#getframetree) |
| [**Мероприятия**](#events) | [frameAttached](#frameattached), [frameDetached](#framedetached), [frameNavigated](#framenavigated), [loadEventFired](#loadeventfired), [domContentEventFired](#domcontenteventfired) |
| [**Типы**](#types) | [FrameId](#frameid), [Frame](#frame), [FrameTree](#frametree) |
## Методы

### "Включить"
Включает уведомления домена страницы.

</p>

---

### "Отключить" 
Отключает уведомления домена страницы.

</p>

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
        <tr>
            <td>frameId <br/> <i>необязательные</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ИД кадра для навигации. Если не указано, будет перемещаться по верхней странице.</td>
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
            <td>ИД кадра, который будет перемещаться.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getFrameTree
Возвращает представленную структуру дерева кадров.

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
            <td>frameTree</td>
            <td><a href="#frametree"><code class="flyout">FrameTree</code></a></td>
            <td>Представляет структуру дерева кадров.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### frameAttached
Собяно, когда фрейм присоединен к родительскому кадру.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ИД прикрепленного кадра.</td>
        </tr>
        <tr>
            <td>parentFrameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Идентификатор родительского кадра.</td>
        </tr>
        <tr>
            <td>stack <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#stacktrace"><code class="flyout">Runtime.StackTrace</code></a></td>
            <td>Трассировка стека JavaScript, когда кадр был прикреплен, устанавливается, только если фрейм инициировался сценарием.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameDetached
Происходит, когда фрейм отсоединяется от родительского кадра.

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
            <td>frameId</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>ИД отсоединяемого кадра.</td>
        </tr>
    </tbody>
</table>
</p>

---

### frameNavigated
Сгорел после завершения навигации по кадру.

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
            <td>frame</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Объект Frame.</td>
        </tr>
    </tbody>
</table>
</p>

---

### loadEventFired
Соответствует событию window.onload.

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
            <td>timestamp</td>
            <td><code class="flyout">number</code></td>
            <td>Количество миллисекунд с момента эпохи.</td>
        </tr>
    </tbody>
</table>
</p>

---

### domContentEventFired
Соответствует событию document.onDOMContentLoaded.

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
            <td>timestamp</td>
            <td><code class="flyout">number</code></td>
            <td>Количество миллисекунд с момента эпохи.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Типы

### <a name="frameid"></a> FrameId `string`

Уникальный идентификатор кадра.

</p>

---

### <a name="frame"></a> Кадр `object`

Сведения о фрейме на странице.

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
            <td>id</td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Уникальный идентификатор кадра.</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>необязательные</i></td>
            <td><a href="#frameid"><code class="flyout">FrameId</code></a></td>
            <td>Уникальный идентификатор родительского кадра.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Имя кадра, указанное в теге.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес документа фрейма.</td>
        </tr>
        <tr>
            <td>securityOrigin</td>
            <td><code class="flyout">string</code></td>
            <td>Источник безопасности документа frame.</td>
        </tr>
        <tr>
            <td>mimeType</td>
            <td><code class="flyout">string</code></td>
            <td>Тип mimeType кадра документа, определяемого браузером.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="frametree"></a> FrameTree `object`

Сведения об иерархии frame.

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
            <td>frame</td>
            <td><a href="#frame"><code class="flyout">Frame</code></a></td>
            <td>Сведения о фрейме для этого элемента дерева.</td>
        </tr>
        <tr>
            <td>childFrames <br/> <i>необязательные</i></td>
            <td><a href="#frametree"><code class="flyout">FrameTree[]</code></a></td>
            <td>Child frames.</td>
        </tr>
    </tbody>
</table>
</p>

---
