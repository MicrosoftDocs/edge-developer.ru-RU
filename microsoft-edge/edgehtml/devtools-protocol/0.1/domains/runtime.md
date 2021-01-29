---
description: Справочник по протоколу DevTools версии 0.1 (EdgeHTML) для домена времени работы. Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не отпущены явным образом.
title: Домен времени работы — протокол DevTools версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 942a105199c8740fb7f7496b2a68e3eb0cc46fb4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235202"
---
# Домен времени работы — протокол DevTools версии 0.1 (EdgeHTML)  

Домен времени работы предоставляет time JavaScript с помощью удаленной оценки и зеркальных объектов. Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, которые можно использовать для дальнейшей ссылки на объект. Исходные объекты сохраняются в памяти, если они не отпущены явным образом.

| | |
|-|-|
| [**Методы**](#methods) | [enable,](#enable) [disable,](#disable) [evaluate,](#evaluate) [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |
| [**Мероприятия**](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |
| [**Типы**](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |
## Методы

### "Включить"
Включает отчеты о <code>executionContextsCleared</code> событии.


---

### "Отключить" 
Отключает отчет о <code>executionContextsCleared</code> событии.


---

### evaluate
Оценивает выражение для глобального объекта.

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
            <td>выражение</td>
            <td><code class="flyout">string</code></td>
            <td>Выражение для оценки.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение. Переопределяет <code>setPauseOnException</code> состояние.</td>
        </tr>
        <tr>
            <td>contextId <br/> <i>необязательные</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Указывает, в какой контексте выполнения выполнять оценку. Если этот параметр опущен, оценка будет выполнена в контексте проверенной страницы.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Должен ли результат быть объектом JSON, который должен быть отправлен значением.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</td>
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
            <td>result</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Результат оценки.</td>
        </tr>
    </tbody>
</table>

---

### callFunctionOn
Вызывает функцию с заданным объявлением для данного объекта. Группа объектов результата наследуется от целевого объекта.

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
            <td>functionDeclaration</td>
            <td><code class="flyout">string</code></td>
            <td>Объявление вызываемой функции.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор объекта для вызова функции. Должен быть указан objectId или executionContextId.  objectId должен быть из функции Runtime.evaluate().</td>
        </tr>
        <tr>
            <td>arguments <br/> <i>необязательные</i></td>
            <td><a href="#callargument"><code class="flyout">CallArgument[]</code></a></td>
            <td>Аргументы вызова. Все аргументы вызова должны принадлежать к одному и тем же мирам JavaScript, что и целевой объект.</td>
        </tr>
        <tr>
            <td>silent <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>В тихом режиме исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение. Переопределяет <code>setPauseOnException</code> состояние.</td>
        </tr>
        <tr>
            <td>returnByValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Должен ли результат быть объектом JSON, который должен быть отправлен значением.</td>
        </tr>
        <tr>
            <td>awaitPromise <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Будет ли <code>await</code> разрешено выполнение для возвращаемой величины и возврата после ожидания обещания.</td>
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
            <td>result</td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Результат вызова.</td>
        </tr>
    </tbody>
</table>

---

### getProperties
Возвращает свойства заданного объекта. Группа объектов результата наследуется от целевого объекта.

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
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Идентификатор объекта, для котором возвращаются свойства.  objectId должен быть от функции Debugger.evaluateOnCallFrame().</td>
        </tr>
        <tr>
            <td>ownProperties <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Если имеется true, возвращает свойства, принадлежащие только самому элементу, а не его прототипу цепочки.</td>
        </tr>
        <tr>
            <td>accessorPropertiesOnly <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Экспериментальная. </b></span>Если установлено true, возвращает только свойства доступа (с getter/setter); внутренние свойства также не возвращаются.</td>
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
            <td>result</td>
            <td><a href="#propertydescriptor"><code class="flyout">PropertyDescriptor[]</code></a></td>
            <td>Свойства объекта.</td>
        </tr>
    </tbody>
</table>

---

## Мероприятия

### executionContextsCleared
Выдан, когда все executionContexts были очищены в браузере


---

### exceptionThrown
Выдается, когда исключение было выброшено и необбрано.

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
            <td><a href="#timestamp"><code class="flyout">Timestamp</code></a></td>
            <td>Timestamp исключения.</td>
        </tr>
        <tr>
            <td>exceptionDetails</td>
            <td><a href="#exceptiondetails"><code class="flyout">ExceptionDetails</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>

---

## Типы

### <a name="scriptid"></a> ScriptId `string`

Уникальный идентификатор скрипта.


---

### <a name="remoteobjectid"></a> RemoteObjectId `string`

Уникальный идентификатор объекта.


---

### <a name="unserializablevalue"></a> UnserializableValue `string`

Значение примитива, которое не может быть в строке JSON.

##### Допустимые значения
Бесконечность, неn, -Infinity, -0

---

### <a name="remoteobject"></a> RemoteObject `object`

Зеркальный объект, ссылающийся на исходный объект JavaScript.

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
            <td>Тип</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: object, function, undefined, string, number, boolean, symbol</i></td>
            <td>Тип объекта.</td>
        </tr>
        <tr>
            <td>subtype <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: null, error, promise</i></td>
            <td>Подсказка подтипа объекта. Указывается только <code>object</code> для значений типов.</td>
        </tr>
        <tr>
            <td>className <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Имя класса объекта (конструктора). Указывается только <code>object</code> для значений типов.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">any</code></td>
            <td>Значение удаленного объекта в случае значений примитивов или значений JSON (если он был запротид).</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>необязательные</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Значение примитива, которое не может быть в строке JSON, не имеет <code>value</code>, но получает это свойство.</td>
        </tr>
        <tr>
            <td>description <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Строка представления объекта.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Уникальный идентификатор объекта (для не примитивных значений).</td>
        </tr>
        <tr>
            <td>msDebuggerPropertyId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Экспериментальная. </b></span>Майкрософт: связанный ид свойства отладки для этого объекта.</td>
        </tr>
    </tbody>
</table>

---

### <a name="propertydescriptor"></a> PropertyDescriptor `object`

Дескриптор свойства объекта.

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
            <td>Имя свойства или описание символа.</td>
        </tr>
        <tr>
            <td>value <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Значение, связанное со свойством.</td>
        </tr>
        <tr>
            <td>writable <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет значение True, если значение, связанное со свойством, может быть изменено (только дескрипторы данных).</td>
        </tr>
        <tr>
            <td>получить <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Функция, которая служит в качестве дескриптора для свойства, или если нет <code>undefined</code> getter (только дескрипторы доступа).</td>
        </tr>
        <tr>
            <td>set <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Функция, которая служит в качестве задавщика для свойства или если нет задавщика <code>undefined</code> (только дескрипторы доступа).</td>
        </tr>
        <tr>
            <td>настраиваемая</td>
            <td><code class="flyout">boolean</code></td>
            <td>True, если тип этого дескриптора свойства может быть изменен и свойство может быть удалено из соответствующего объекта.</td>
        </tr>
        <tr>
            <td>enumerable</td>
            <td><code class="flyout">boolean</code></td>
            <td>True, если это свойство появляется во время нумерации свойств соответствующего объекта.</td>
        </tr>
        <tr>
            <td>wasThrown <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>True, если результат был выброшен во время оценки.</td>
        </tr>
        <tr>
            <td>isOwn <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Имеет свойство True, если свойство принадлежит объекту.</td>
        </tr>
        <tr>
            <td>msReturnValue <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Экспериментальная. </b></span>Майкрософт: имеет значение True, если свойство является возвращаемой.</td>
        </tr>
        <tr>
            <td>symbol, <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Объект символа свойства, если свойство имеет `symbol` тип. </td>
        </tr>
    </tbody>
</table>

---

### <a name="callargument"></a> CallArgument `object`

Представляет аргумент вызова функции. Должен быть указан либо ид удаленного <code>objectId</code> объекта, примитив, несериализируемый значение примитива, либо ни один <code>value</code> из них (для неопределенных).

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
            <td>value <br/> <i>необязательные</i></td>
            <td><code class="flyout">any</code></td>
            <td>Значение примитива или сериализуемый объект JavaScript.</td>
        </tr>
        <tr>
            <td>unserializableValue <br/> <i>необязательные</i></td>
            <td><a href="#unserializablevalue"><code class="flyout">UnserializableValue</code></a></td>
            <td>Значение примитива, которое не может быть в строке JSON.</td>
        </tr>
        <tr>
            <td>objectId <br/> <i>необязательные</i></td>
            <td><a href="#remoteobjectid"><code class="flyout">RemoteObjectId</code></a></td>
            <td>Удаленный handle объекта.</td>
        </tr>
    </tbody>
</table>

---

### <a name="executioncontextid"></a> ExecutionContextId `integer`

ИД контекста выполнения.


---

### <a name="exceptiondetails"></a> ExceptionDetails `object`

Подробные сведения об исключении (или ошибке), которое было выброшено во время компиляции или выполнения сценария.

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
            <td>exceptionId</td>
            <td><code class="flyout">integer</code></td>
            <td>ИД исключения.</td>
        </tr>
        <tr>
            <td>текст</td>
            <td><code class="flyout">string</code></td>
            <td>Текст исключения, который должен использоваться вместе с объектом исключения при наличии.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки расположения исключения (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца расположения исключения (на основе 0).</td>
        </tr>
        <tr>
            <td>scriptId <br/> <i>необязательные</i></td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ИД сценария расположения исключения.</td>
        </tr>
        <tr>
            <td>url <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан.</td>
        </tr>
        <tr>
            <td>stackTrace <br/> <i>необязательные</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Трассировка стека JavaScript, если она доступна.</td>
        </tr>
        <tr>
            <td>exception <br/> <i>необязательные</i></td>
            <td><a href="#remoteobject"><code class="flyout">RemoteObject</code></a></td>
            <td>Объект исключения, если он доступен.</td>
        </tr>
        <tr>
            <td>executionContextId <br/> <i>необязательные</i></td>
            <td><a href="#executioncontextid"><code class="flyout">ExecutionContextId</code></a></td>
            <td>Идентификатор контекста, в котором произошло исключение.</td>
        </tr>
    </tbody>
</table>

---

### <a name="timestamp"></a> Метка времени `integer`

Количество миллисекунд с момента эпохи.


---

### <a name="callframe"></a> CallFrame `object`

Запись стека для ошибок и утверждений во время работы.

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
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя функции JavaScript.</td>
        </tr>
        <tr>
            <td>scriptId</td>
            <td><a href="#scriptid"><code class="flyout">ScriptId</code></a></td>
            <td>ИД скрипта JavaScript.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Имя или URL-адрес сценария JavaScript.</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки сценария JavaScript (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца сценария JavaScript (на основе 0).</td>
        </tr>
    </tbody>
</table>

---

### <a name="stacktrace"></a> StackTrace `object`

Вызов кадров для утверждений или сообщений об ошибках.

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
            <td>description <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Строковая метка трассировки стека. Для а async traces это может быть имя функции, которая инициировала ассынский вызов.</td>
        </tr>
        <tr>
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Имя функции JavaScript.</td>
        </tr>
        <tr>
            <td>parent <br/> <i>необязательные</i></td>
            <td><a href="#stacktrace"><code class="flyout">StackTrace</code></a></td>
            <td>Асинхронная трассировка стека JavaScript, предшествующего этому стеку, если доступна.</td>
        </tr>
    </tbody>
</table>

---