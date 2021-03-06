---
description: Ссылка На протокол DevTools Версии 0.1 (EdgeHTML) для домена runtime.  Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов.  Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.  Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.
title: Домен runtime - Протокол DevTools Версии 0.1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9aa87c1c289452844ef3442811f84881fc752b4
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397694"
---
# <a name="runtime-domain---devtools-protocol-version-01-edgehtml"></a>Домен runtime - Протокол DevTools Версии 0.1 (EdgeHTML)  

Домен runtime предоставляет время запуска JavaScript с помощью удаленной оценки и зеркальных объектов.  Результаты оценки возвращаются в виде зеркального объекта, который предоставляет тип объекта, представление строки и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.  Исходные объекты сохраняются в памяти, если они не будут либо явно освобождены.  

| Категория | Участники |  
|:--- |:--- |  
| [Методы](#methods) | [включить,](#enable) [отключить,](#disable) [оценить,](#evaluate) [callFunctionOn](#callfunctionon), [getProperties](#getproperties) |  
| [Мероприятия](#events) | [executionContextsCleared](#executioncontextscleared), [exceptionThrown](#exceptionthrown) |  
| [Типы](#types) | [ScriptId](#scriptid), [RemoteObjectId](#remoteobjectid), [UnserializableValue](#unserializablevalue), [RemoteObject](#remoteobject), [PropertyDescriptor](#propertydescriptor), [CallArgument](#callargument), [ExecutionContextId](#executioncontextid), [ExceptionDetails](#exceptiondetails), [Timestamp](#timestamp), [CallFrame](#callframe), [StackTrace](#stacktrace) |  

## <a name="methods"></a>Методы  

### <a name="enable"></a>"Включить"  

Включает отчеты о `executionContextsCleared` событии.  

&nbsp;  

---  

### <a name="disable"></a>"Отключить"   

Отключение отчетов о `executionContextsCleared` событии.  

&nbsp;  

---  

### <a name="evaluate"></a>оценка  

Оценивает выражение на глобальном объекте.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| выражение | `string` | Выражение для оценки. |  
| silent \(необязательный\) | `boolean` | В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.  Переопределяет `setPauseOnException` состояние. |  
| contextId \(необязательный\) | [ExecutionContextId](#executioncontextid) | Указывает, в котором контекст выполнения для выполнения оценки.  Если параметр опущен, оценка будет выполнена в контексте проверенной страницы. |  
| returnByValue \(необязательный\) | `boolean` | Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению. |  
| awaitPromise \(необязательный\) | `boolean` | Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| результат | [RemoteObject](#remoteobject) | Результат оценки. |  

---  

### <a name="callfunctionon"></a>callFunctionOn  

Функция вызовов с заданным объявлением на заданный объект.  Объектная группа результата наследуется от целевого объекта.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| functionDeclaration | `string` | Объявление функции вызова. |  
| objectId \(необязательный\) | [RemoteObjectId](#remoteobjectid) | Идентификатор объекта для вызова функции.  Либо `objectId` `executionContextId` заданы, либо должны быть указаны.  objectId должен быть из функции Runtime.evaluate() |  
| аргументы \(необязательный\) | [CallArgument[]](#callargument) | Аргументы вызова.  Все аргументы вызовов должны принадлежать одному миру JavaScript как целевому объекту. |  
| silent \(необязательный\) | `boolean` | В режиме молчаливого режима исключения, выброшенные во время оценки, не сообщаются и не приостанавливали выполнение.  Переопределяет `setPauseOnException` состояние. |  
| returnByValue \(необязательный\) | `boolean` | Ожидается ли, что результат будет объектом JSON, который должен быть отправлен по значению. |  
| awaitPromise \(необязательный\) | `boolean` | Будет ли `await` разрешено выполнение для результативного значения и возврата после ожидания обещания. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| результат | [RemoteObject](#remoteobject) | Результат вызова. |  

---  

### <a name="getproperties"></a>getProperties  

Возвращает свойства заданного объекта.  Объектная группа результата наследуется от целевого объекта.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| objectId | [RemoteObjectId](#remoteobjectid) | Идентификатор объекта для возврата свойств.  `objectId` должно быть из `Debugger.evaluateOnCallFrame()` функции. |  
| ownProperties \(необязательный\) | `boolean` | Если `true` возвращает свойства, принадлежащие только самому элементу, а не цепочке прототипов. |  
| accessorPropertiesOnly \(необязательный\) | `boolean` | **Экспериментальные**.  Если `true` , возвращает свойства вспомогательного оборудования \(с getter/setter\) только; внутренние свойства также не возвращаются. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| результат | [PropertyDescriptor[]](#propertydescriptor) | Свойства объектов. |  

---  

## <a name="events"></a>Мероприятия  

### <a name="executioncontextscleared"></a>executionContextsCleared  

Выдан, когда все executionContexts были очищены в браузере.  

&nbsp;  

---  

### <a name="exceptionthrown"></a>exceptionThrown  

Выдано, когда исключение было выброшено и ненаблюдаемо.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| timestamp | [Метка времени](#timestamp) | Timestamp исключения. |  
| exceptionDetails | [ExceptionDetails](#exceptiondetails) | &nbsp; |  

---  

## <a name="types"></a>Типы  

### <a name="scriptid-string"></a>Строка ScriptId  

<a name="scriptid"></a>  

Уникальный идентификатор скрипта.  

&nbsp;  

---  

### <a name="remoteobjectid-string"></a>Строка RemoteObjectId  

<a name="remoteobjectid"></a>  

Уникальный идентификатор объекта.  

&nbsp;  

---  

### <a name="unserializablevalue-string"></a>Строка UnserializableValue  

<a name="unserializablevalue"></a>  

Примитивное значение, которое не может быть строкифицировано JSON.  

##### <a name="allowed-values"></a>Допустимые значения  

`Infinity`, `NaN`, `-Infinity`, `-0`  

---  

### <a name="remoteobject-object"></a>Объект RemoteObject  

<a name="remoteobject"></a>  

Объект Mirror, отсылающий к исходному объекту JavaScript.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| Тип | `string` | Тип объекта.  Допустимые значения:  `object` , , , , , `function` `undefined` `string` `number` `boolean` и `symbol` |  
| подтип \(необязательный\) | `string` | Подсказка подтипа объекта.  Только для `object` значений типа.  Допустимые значения:  `null` `error` и `promise` |  
| className \(необязательный\) | `string` | Имя объекта класса \(конструктор\).  Только для `object` значений типа. |  
| значение \(необязательный\) | `any` | Значение удаленного объекта в случае примитивных значений или значений JSON \(если оно было запророшно\). |  
| unserializableValue \(необязательный\) | [UnserializableValue](#unserializablevalue) | Примитивное значение, которое не может быть JSON-stringified, не `value` имеет, но получает это свойство. |  
| описание \(необязательный\) | `string` | Строковая репрезентация объекта. |  
| objectId \(необязательный\) | [RemoteObjectId](#remoteobjectid) | Уникальный идентификатор объекта \(для небытийных значений\). |  
| msDebuggerPropertyId \(необязательный\) | `string` | **Экспериментальные**.  Microsoft. Связанный с этим объектом ID свойства отладки. |  

---  

### <a name="propertydescriptor-object"></a>Объект PropertyDescriptor  

<a name="propertydescriptor"></a>  

Дескриптор свойства объекта.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| name | `string` | Имя свойства или описание символа. |  
| значение \(необязательный\) | [RemoteObject](#remoteobject) | Значение, связанное с свойством. |  
| writable \(необязательный\) | `boolean` | `True` если значение, связанное с свойством, может быть изменено \(только дескрипторы данных\). |  
| получить \(необязательный\) | [RemoteObject](#remoteobject) | Функция, которая служит в качестве геттера для свойства, или если нет геттера `undefined` \(только дескрипторы аксессуара\). |  
| set \(необязательный\) | [RemoteObject](#remoteobject) | Функция, которая служит сеттером для свойства или если нет сеттера `undefined` \(только дескрипторы аксессуара\). |  
| настраиваемый | `boolean` | `True` если тип этого дескриптора свойства может быть изменен и если свойство может быть удалено из соответствующего объекта. |  
| переоменимый | `boolean` | `True` если это свойство появляется во время переопечатки свойств соответствующего объекта. |  
| wasThrown \(необязательный\) | `boolean` | `True` если результат был брошен во время оценки. |  
| isOwn \(необязательный\) | `boolean` | `True` если свойство принадлежит объекту. |  
| msReturnValue \(необязательный\) | `boolean` | **Экспериментальные**.  Майкрософт:  `True` если свойство является возвращаемой величиной. |  
| символ \(необязательный\) | [RemoteObject](#remoteobject) | Объект символа свойства, если свойство имеет `symbol` тип. |  

---  

### <a name="callargument-object"></a>Объект CallArgument  

<a name="callargument"></a>  

Представляет аргумент вызова функции.  Либо удаленный идентификационный объект, неопределимое примитивное значение, либо значение \(для неопределённого\) не `value` должно быть указано.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| значение \(необязательный\) | `any` | Примитивное значение или серийный объект javascript. |  
| unserializableValue \(необязательный\) | [UnserializableValue](#unserializablevalue) | Примитивное значение, которое не может быть jSON-stringified. |  
| objectId \(необязательный\) | [RemoteObjectId](#remoteobjectid) | Удаленная ручка объекта. |  

---  

### <a name="executioncontextid-integer"></a>Integer executionContextId  

<a name="executioncontextid"></a>  

ID контекста выполнения.  

&nbsp;  

---  

### <a name="exceptiondetails-object"></a>Объект ExceptionDetails  

<a name="exceptiondetails"></a>  

Подробные сведения об исключении \(или ошибке\), которое было выброшено во время компиляции или выполнения скрипта.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| exceptionId | `integer` | ID исключения. |  
| текст | `string` | Текст исключения, который следует использовать вместе с объектом исключения при наличии. |  
| lineNumber | `integer` | Номер строки расположения исключения \(0-based\). |  
| columnNumber | `integer` | Номер столбца расположения исключения \(0-based\). |  
| scriptId \(необязательный\) | [ScriptId](#scriptid) | ID сценария расположения исключений. |  
| URL\(необязательный\) | `string` | URL-адрес расположения исключения, который будет использоваться, когда сценарий не был указан. |  
| stackTrace \(необязательный\) | [StackTrace](#stacktrace) | Трассировка стека JavaScript при наличии. |  
| исключение \(необязательный\) | [RemoteObject](#remoteobject) | Объект Исключения, если он доступен. |  
| executionContextId \(необязательный\) | [ExecutionContextId](#executioncontextid) | Идентификатор контекста, в котором произошло исключение. |  

---  

### <a name="timestamp-integer"></a>Integer Timestamp  

<a name="timestamp"></a>  

Количество миллисекунд с эпохи.  

&nbsp;  

---  

### <a name="callframe-object"></a>Объект CallFrame  

<a name="callframe"></a>  

Стек записи для ошибок и утверждений во время работы.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| functionName | `string` | Имя функции JavaScript. |  
| scriptId | [ScriptId](#scriptid) | ID скрипта JavaScript. |  
| url | `string` | Имя сценария JavaScript или URL-адрес. |  
| lineNumber | `integer` | Номер строки скрипта JavaScript \(0-based\). |  
| columnNumber | `integer` | Номер столбца скрипта JavaScript \(0-based\). |  

---  

### <a name="stacktrace-object"></a>Объект StackTrace  

<a name="stacktrace"></a>  

Кадры вызовов для утверждений или сообщений об ошибках.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| описание \(необязательный\) | `string` | Строковая метка этого следа стека.  Для следов async это может быть имя функции, которая инициировала вызов async. |  
| callFrames | [CallFrame[]](#callframe) | Имя функции JavaScript. |  
| родительский \(необязательный\) | [StackTrace](#stacktrace) | Асинхронный след стека JavaScript, предшествующий этому стеку, если доступен. |  

---  
