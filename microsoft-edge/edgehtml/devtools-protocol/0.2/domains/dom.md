---
description: Справка по домену DOM. Этот домен предоставляет операции чтения и записи DOM. Каждый узел DOM представлен своим зеркальным объектом с объектом `id` . Это можно использовать для получения дополнительных сведений о узле, его разрешения в оболочку объекта JavaScript и т. `id` д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Тыловой узел отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Сбор сведений о узлах, отправленных клиенту, несет ответственность клиент.<p>Обратите `iframe` внимание, что элементы-владельцы возвращают соответствующие элементы документа в качестве своих узлы.</p>
title: Домен DOM — протокол DevTools версии 0.2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d9861a2395f7b24142a41efea9ac599907dec27
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235566"
---
# DOM

Этот домен предоставляет операции чтения и записи DOM. Каждый узел DOM представлен своим зеркальным объектом с объектом `id` . Это `id` можно использовать для получения дополнительных сведений об узле, ее разрешения в оболочку объекта JavaScript и т. д. Важно, чтобы клиент получал события DOM только для тех узлов, которые известны клиенту. Тыловой узел отслеживает узлы, отправленные клиенту, и никогда не отправляет один и тот же узел дважды. Сбор сведений о узлах, отправленных клиенту, несет ответственность клиент.<p>Обратите `iframe` внимание, что элементы-владельцы возвращают соответствующие элементы документа в качестве их узлы.</p>

| | |
|-|-|
| [**Методы**](#methods) | [enable](#enable), [disable](#disable), [getDocument](#getdocument), [highlightNode](#highlightnode), [hideHighlight](#hidehighlight), [requestChildNodes](#requestchildnodes), [getAttributes](#getattributes), [getOuterHTML](#getouterhtml), [pushNodesByBackendIdsToFrontend](#pushnodesbybackendidstofrontend), [querySelector](#queryselector), [querySelectorAll](#queryselectorall), [requestNode , resolveNode](#requestnode), [setInspectedNode](#setinspectednode) [](#resolvenode) |
| [**Мероприятия**](#events) | [setChildNodes](#setchildnodes), [attributeModified](#attributemodified), [attributeRemoved](#attributeremoved), [characterDataModified](#characterdatamodified), [childNodeInserted](#childnodeinserted), [childNodeRemoved](#childnoderemoved), [documentUpdated](#documentupdated) |
| [**Типы**](#types) | [RGBA](#rgba), [HighlightConfig](#highlightconfig), [NodeId](#nodeid), [Node](#node), [BackendNodeId](#backendnodeid), [PseudoType](#pseudotype) |
| [**Зависимости**](#dependencies) | [Время выполнения](runtime.md) |
## Методы

### "Включить"
Включает агент DOM для заданной страницы.

</p>

---

### "Отключить" 
Отключает агент DOM для заданной страницы. Отключение DOM сделает недопустимыми все ранее допустимые nodeId.

</p>

---

### getDocument
Возвращает корневой узел DOM (и, при желании, поддерево) вызываемой. Вызов `getDocument` аннулирует все ранее допустимые nodeIds

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
            <td>depth</td>
            <td><code class="flyout">integer</code></td>
            <td>Максимальная глубина, на которой должны быть извлечены дети, по умолчанию составляет 2. Используйте -1 для всего подtree.</td>
        </tr>
        <tr>
            <td>1</td>
            <td><code class="flyout">boolean</code></td>
            <td>Следует ли обходить iframes при возвращении подtree (по умолчанию — false).</td>
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
            <td>root</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Итоговая точка узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### highlightNode
Узел DOM Higlights с заданным идом или оболочкой объекта. Должны быть указаны nodeId, backendNodeId или objectId.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, который нужно выделить.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Идентификатор выделяемого тылового узла.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript object id of the node to be highlighted.</td>
        </tr>
        <tr>
            <td>higlightConfig</td>
            <td><a href="#highlightconfig"><code class="flyout">HighlightConfig</code></a></td>
            <td>Дескриптор внешнего вида выделения.</td>
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
            <td>root</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Итоговая точка узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### hideHighlight
Скрывает текущее выделение узла DOM.

</p>

---

### requestChildNodes
Запросы на возврат детей узла с заданным идом вызываемой сети в виде `setChildNodes` событий. `setChildNodes` будет запускаться для каждого узла, который ранее не вернул его узлы, начиная с запрашиваемого узла до указанной глубины.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла для получения детей.</td>
        </tr>
        <tr>
            <td>depth</td>
            <td><code class="flyout">integer</code></td>
            <td>Максимальная глубина, на которой должны быть извлечены дети, по умолчанию составляет 1. Используйте -1 для всего подtree.</td>
        </tr>
        <tr>
            <td>1</td>
            <td><code class="flyout">boolean</code></td>
            <td>Следует ли обходить iframes при возвращении подtree (по умолчанию — false).</td>
        </tr>
    </tbody>
</table>
</p>

---

### getAttributes
Возвращает атрибуты для указанного узла.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, для который требуется получить attibutes.</td>
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
            <td>attributes</td>
            <td><code class="flyout">string[]</code></td>
            <td>Массив между именами и значениями атрибутов узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getOuterHTML
Возвращает HTML-разметку узла.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>Идентификатор заднего узла.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript object id of the node wrapper.</td>
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
            <td>outerHTML</td>
            <td><code class="flyout">string</code></td>
            <td>Внешняя разметка HTML.</td>
        </tr>
    </tbody>
</table>
</p>

---

### pushNodesByBackendIdsToFrontend
Ищет и соеди up Node Ids and resolves all parents for the specified Backend Node Ids

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
            <td>backendNodeIds</td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId[]</code></a></td>
            <td>ИД узлов, которые необходимо разрешить</td>
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
            <td>nodeIds</td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>ИД узлов разрешенных узлов</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelector
Выполняется `querySelector` на заданный узел.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла для запроса.</td>
        </tr>
        <tr>
            <td>селектор</td>
            <td><code class="flyout">string</code></td>
            <td>Строка селектора.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Результат селектора запросов.</td>
        </tr>
    </tbody>
</table>
</p>

---

### querySelectorAll
Выполняется `querySelectorAll` на заданный узел.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла для запроса.</td>
        </tr>
        <tr>
            <td>селектор</td>
            <td><code class="flyout">string</code></td>
            <td>Строка селектора.</td>
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
            <td>nodeIds</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Результаты селектора запросов.</td>
        </tr>
    </tbody>
</table>
</p>

---

### requestNode
Запрашивает, чтобы узел с заданным ид удаленного объекта был отправлен вызываемой. Все узлы, которые формируют путь от узла к корню, также отправляются клиенту в виде серии `setChildNodes` уведомлений. возвращает 0, если документ, содержащий запрашиваемого узла, ранее не запрашивался клиентом.

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
            <td>objectId</td>
            <td><a href="runtime.md#remoteobjectid"><code class="flyout">Runtime.RemoteObjectId</code></a></td>
            <td>JavaScript object Id to convert into node.</td>
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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла для данного объекта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### resolveNode
Устраняет объект узла JavaScript для заданного NodeId или BackendNodeId.

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
            <td>nodeId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который требуется разрешить.</td>
        </tr>
        <tr>
            <td>backendNodeId <br/> <i>необязательные</i></td>
            <td><a href="#backendnodeid"><code class="flyout">BackendNodeId</code></a></td>
            <td>ИД узла, который необходимо разрешить.</td>
        </tr>
        <tr>
            <td>objectGroup</td>
            <td><code class="flyout">string</code></td>
            <td>Символьное имя группы, которое можно использовать для освобождения нескольких объектов.</td>
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
            <td>объект</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Оболочка объекта JavaScript для данного узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setInspectedNode
<span><b>Экспериментальная. </b></span>Позволяет консоли ссылаться на предыдущий проверенный узел с заданным идом через $0-$4.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла DOM, доступный с помощью API командной строки в размере 0–4 долларов США.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### setChildNodes
Происходит, когда тыл хочет предоставить клиенту отсутствующие структуры DOM. Это происходит при большинстве вызовов, запрашивающих nodeIds

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
            <td>parentId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Родительский узел для poplate с children.</td>
        </tr>
        <tr>
            <td>nodes</td>
            <td><a href="#nodeid"><code class="flyout">NodeId[]</code></a></td>
            <td>Массив child nodes.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeModified
Сработает, `Element` если изменен атрибут "атрибут".

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который изменился.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя атрибута.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Значение атрибута.</td>
        </tr>
    </tbody>
</table>
</p>

---

### attributeRemoved
Список при `Element` удалении атрибута "атрибут".

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который изменился.</td>
        </tr>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Имя атрибута.</td>
        </tr>
    </tbody>
</table>
</p>

---

### characterDataModified
Событие `DOMCharacterDataModified` Mirrors.

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
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который изменился.</td>
        </tr>
        <tr>
            <td>charcterData</td>
            <td><code class="flyout">string</code></td>
            <td>Новое текстовое значение.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeInserted
Событие `DOMNodeInserted` Mirrors.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который изменился.</td>
        </tr>
        <tr>
            <td>previousNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД предыдущего уровня вставляемого узла.</td>
        </tr>
        <tr>
            <td>node</td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Вставленные данные узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### childNodeRemoved
Событие `DOMNodeRemoved` Mirrors.

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
            <td>parentNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД узла, который изменился.</td>
        </tr>
        <tr>
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>ИД удаляемого узла.</td>
        </tr>
    </tbody>
</table>
</p>

---

### documentUpdated
`Document`Ссвеяно, когда было полностью обновлено. Более не допустимые ид узла.

</p>

---

## Типы

### <a name="rgba"></a> RGBA `object`

Структура с цветом RGBA.

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
            <td>r</td>
            <td><code class="flyout">integer</code></td>
            <td>Красный компонент в диапазоне [0–255].</td>
        </tr>
        <tr>
            <td>g</td>
            <td><code class="flyout">integer</code></td>
            <td>Зеленый компонент в диапазоне [0–255].</td>
        </tr>
        <tr>
            <td>b</td>
            <td><code class="flyout">integer</code></td>
            <td>Синий компонент в диапазоне [0–255].</td>
        </tr>
        <tr>
            <td>а <br/> <i>необязательные</i></td>
            <td><code class="flyout">number</code></td>
            <td>Альфа-компонент в диапазоне [0-1]. Значение по умолчанию — 1.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="highlightconfig"></a> HighlightConfig `object`

Данные конфигурации для выделения элементов страницы.

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
            <td>contentColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки в поле содержимого. Значение по умолчанию прозрачно.</td>
        </tr>
        <tr>
            <td>paddingColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки заполнения. Значение по умолчанию прозрачно.</td>
        </tr>
        <tr>
            <td>borderColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки выделения границы. Значение по умолчанию прозрачно.</td>
        </tr>
        <tr>
            <td>marginColor <br/> <i>необязательные</i></td>
            <td><a href="#rgba"><code class="flyout">RGBA</code></a></td>
            <td>Цвет заливки выделения полей. Значение по умолчанию прозрачно.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="nodeid"></a> NodeId `integer`

Уникальный идентификатор узла DOM

</p>

---

### <a name="node"></a> Node `object`

Зеркальный объект, который представляет фактические узлы DOM.

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
            <td>nodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла, используемый для ссылки на этот узел. На тыловом узле будут происходить события DOM для узлов с узлом NodeId, известным клиенту</td>
        </tr>
        <tr>
            <td>parentId <br/> <i>необязательные</i></td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор узла родительского узла(если он есть).</td>
        </tr>
        <tr>
            <td>backendNodeId</td>
            <td><a href="#nodeid"><code class="flyout">NodeId</code></a></td>
            <td>Идентификатор заднего узла узла. BackendNodeIds ссылается на узлы, которые могут быть известны клиенту, но не выдают события DOM для этого узла.</td>
        </tr>
        <tr>
            <td>nodeType</td>
            <td><code class="flyout">integer</code></td>
            <td>`Node`'s nodeType.</td>
        </tr>
        <tr>
            <td>nodeName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`'s nodeName.</td>
        </tr>
        <tr>
            <td>localName</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`'s localName</td>
        </tr>
        <tr>
            <td>nodeValue</td>
            <td><code class="flyout">string</code></td>
            <td>`Node`'s nodeValue</td>
        </tr>
        <tr>
            <td>childNodeCount <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Количество детей для `Container` узлов.</td>
        </tr>
        <tr>
            <td>дети <br/> <i>необязательные</i></td>
            <td><a href="#node"><code class="flyout">Node[]</code></a></td>
            <td>Узлы этого узла по запросу с их children.</td>
        </tr>
        <tr>
            <td>attributes <br/> <i>необязательные</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>Атрибуты узлов в виде плоского массива `Element` "[name1, value1, name2, value2]</td>
        </tr>
        <tr>
            <td>documentURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес `Document` документа, на который указывают узлы.</td>
        </tr>
        <tr>
            <td>baseURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес `Document` документа, который узлы используют для завершения URL-адреса.</td>
        </tr>
        <tr>
            <td>publicId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` PublicId узла.</td>
        </tr>
        <tr>
            <td>systemId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` SystemId узла.</td>
        </tr>
        <tr>
            <td>internalSubset <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`DocumentType` InternalSubset узла.</td>
        </tr>
        <tr>
            <td>xmlVersion <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Document` XML-версия узла в случае XML-документов.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Имя узла.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>`Attr` Значение узла.</td>
        </tr>
        <tr>
            <td>frameId <br/> <i>необязательные</i></td>
            <td><a href="page.md#frameid"><code class="flyout">Page.FrameId</code></a></td>
            <td>ИД фрейма для элементов владельца кадра.</td>
        </tr>
        <tr>
            <td>contentDocument <br/> <i>необязательные</i></td>
            <td><a href="#node"><code class="flyout">Node</code></a></td>
            <td>Контентный документ для элементов владельца кадра.</td>
        </tr>
        <tr>
            <td>isSVG <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет true, если узел является SVG.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="backendnodeid"></a> BackendNodeId `integer`

Уникальный идентификатор узла DOM, используемый для ссылки на узел, который, возможно, не был передавлен на передний.

</p>

---

### <a name="pseudotype"></a> PseudoType `string`

Псевдоэлементный тип.

##### Допустимые значения
first-line, first-letter, before, after, selection
</p>

---

## Зависимости

[Время выполнения](runtime.md)
