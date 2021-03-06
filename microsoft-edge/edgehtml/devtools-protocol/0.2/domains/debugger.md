---
description: Ссылка на протокол DevTools Версии 0.2 (EdgeHTML) для домена Debugger. Домен Debugger предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.
title: Домен Debugger — протокол DevTools Версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 00c410812edd4d11e9904a489955e7fd218a7e5d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398177"
---
# <a name="debugger-domain---devtools-protocol-version-02-edgehtml"></a>Домен Debugger — протокол DevTools Версии 0.2 (EdgeHTML)  

Домен Debugger предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки разрывов, проходить выполнение, изучать следы стека и т. д.

| Категория | Участники |  
|:--- |:--- |  
| [**Методы**](#methods) | [включить](#enable), отключить [,](#disable) [getPossibleBreakpoints](#getpossiblebreakpoints), [](#resume) [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), setBreakpoint , [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [](#setbreakpoint) [пауза](#pause), резюме , [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [оценкаOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |  
| [**Мероприятия**](#events) | [scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [paused](#paused), [resumed](#resumed) |  
| [**Типы**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Расположение](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Область](#scope) |  
| [**Зависимости**](#dependencies) | [Время выполнения](./runtime.md) |  

## <a name="methods"></a>Методы  

### <a name="enable"></a>"Включить"  

Включает отладка для данной страницы. Клиенты не должны предполагать, что отладка включена до тех пор, пока не будет получен результат для этой команды.  

&nbsp;  

---  

### <a name="disable"></a>"Отключить"   

Отладка отладки для данной страницы.  

&nbsp;  

---  

### <a name="getpossiblebreakpoints"></a>getPossibleBreakpoints  

Возвращает возможные расположения для breakpoint. ScriptId в расположениях старта и конца диапазона должен быть одинаковым.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| start | [Расположение](#location) | Начало диапазона для поиска возможных точек разрыва. |  
| завершить | [Расположение](#location) | Конец диапазона для поиска возможных точек разрыва в \(excluding\).  Если не указано, конец скриптов используется как конец диапазона. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| расположения | [BreakLocation](#breaklocation) | Список возможных местоположений точки разрыва. |  

---  

### <a name="setbreakpointsactive"></a>setBreakpointsActive  

Активирует или отключает все точки взлома на странице.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| active | `boolean` | Новое значение для активного состояния точек breakpoints. | 

---  

### <a name="setbreakpointbyurl"></a>setBreakpointByUrl  

Задает точку разрыва JavaScript в указанном расположении, указанном URL-адресом или URL-адресом regex.  После того как эта команда будет выдана, все существующие разбиенные сценарии будут иметь точки разрывов, разрешенные и возвращенные в `locations` свойстве.  Дальнейшее соответствие размыву сценариев приведет к последующим `breakpointResolved` событиям, выданным.  Этот логический точкой разрыва будет пережить перезагрузки страниц.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| lineNumber | `integer` | Номер строки для набора точки разрыва. | 
| URL\(необязательный\) | `string` | URL-адрес ресурсов, на которые необходимо установить точку разрыва. |  
| urlRegex \(необязательный\) | `string` | Шаблон Regex для URL-адресов ресурсов для набора точек остановок.  Либо `url` необходимо `urlRegex` укаварить. |  
| columnNumber \(необязательный\) | `integer` | Смещение в строке для набора точки разрыва. |  
| условие \(необязательный\) | `string` | Выражение для использования в качестве условия breakpoint. Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID созданной точки breakpoint для дальнейшей ссылки. |  
| расположения | [Расположение[]](#location) | Список местоположений, в которые эта точка взлома была разрешена после добавления. |  

---  

### <a name="setbreakpoint"></a>setBreakpoint  

Задает точку разрыва JavaScript в заданное расположение.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| расположение | [Расположение](#location) | Расположение для набора точки разрыва. |  
| условие \(необязательный\) | `string` | Выражение для использования в качестве условия breakpoint.  Если указано, отладка остановится только на точке разрыва, если это выражение будет оцениваться до true. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | ID созданной точки breakpoint для дальнейшей ссылки. |  
| actualLocation | [Расположение](#location) | Расположение этой точки разрыва. |  

---  

### <a name="removebreakpoint"></a>removeBreakpoint  

Удаляет точку разрыва JavaScript.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | &nbsp; |  

---  

### <a name="stepover"></a>stepOver  

Шаги по заявлению.  

&nbsp;  

---  

### <a name="stepinto"></a>stepInto  

Шаги в вызов функции.  

&nbsp;  

---  

### <a name="stepout"></a>stepOut  

Выход из вызова функции.  

&nbsp;  

---  

### <a name="pause"></a>pause  

Остановится в следующем заявлении JavaScript.  

&nbsp;  

---  

### <a name="resume"></a>resume  

Возобновляет выполнение JavaScript.  

&nbsp;  

---  

### <a name="getscriptsource"></a>getScriptSource  

Возвращает источник для скрипта с данным id.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | ID скрипта для получения источника. |  

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| scriptSource | `string` | Источник скрипта. | 

---  

### <a name="setpauseonexceptions"></a>setPauseOnExceptions  

Определяет приостановка состояния исключений.  Можно запланить остановку на всех исключениях, необученных исключениях или без исключений.  Начальная пауза для состояния исключений `none` .  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| состояние | `string` | Пауза в режиме исключений.  Допустимые значения:  `none` `uncaught` , `all` |  

---  

### <a name="evaluateoncallframe"></a>evaluateOnCallFrame  

Оценивает выражение в заданной рамке вызовов.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Идентификатор кадра вызовов для оценки. |  
| выражение | `string` | Выражение для оценки. | 

| Возвращает | Тип | Сведения |  
|:--- |:--- |:--- |  
| результат | [Runtime.RemoteObject](./runtime.md#remoteobject) | Объектная оболочка для результата оценки. |  

---  

### <a name="setvariablevalue"></a>setVariableValue  

Изменяет значение переменной в callframe.  Объектные области не поддерживаются и должны мутироваться вручную.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| scopeNumber | `integer` | 0-базирующееся число области, как было перечислены в цепочке области.  Разрешены только `local` `closure` типы области и `catch` области.  Другими областьми можно управлять вручную. | 
| variableName | `string` | Переменное имя. | 
| newValue | [Runtime.CallArgument](./runtime.md#callargument) | Новое переменная значение. |  
| callFrameId | [CallFrameId](#callframeid) | ID callframe, который содержит переменную. |  

---  

### <a name="setblackboxpatterns"></a>setBlackboxPatterns  

**Экспериментальные**.  Замените предыдущие шаблоны черных ящиков на пройденные.  Заставляет отодвигаться, чтобы пропустить шаг/паузу в скриптах с URL-адресом, совпадающий с одним из шаблонов.  Отладка будет пытаться оставить черный ящик скрипт, выполняя "шаг" несколько раз, наконец, прибегая к "выйти" в случае неудачи.  


| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| шаблоны | `string[]` | Массив regexps, который будет использоваться для проверки URL-адреса скрипта для состояния blackbox. | 

---  

### <a name="mssetdebuggerpropertyvalue"></a>msSetDebuggerPropertyValue  

**Экспериментальные**.  Microsoft. Задает указанное свойство отладки указанному значению.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| debuggerPropertyId | string | Microsoft. Свойство id \(i.e. `msDebuggerPropertyId` \) для набора. | 
| newValue | `string` | &nbsp; |  

---  

## <a name="events"></a>Мероприятия  

### <a name="scriptparsed"></a>scriptParsed  

Уволено при размыве сценария. Это событие также будет уволено для всех известных и неиспользванных скриптов при включив отладку.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Идентификатор размыкаемого скрипта. |  
| url | `string` | URL-адрес или имя разбияемого скрипта \(если таково\). | 
| startLine | `integer` | Строка смещения скрипта в ресурсе с заданным URL-адресом \(для тегов скрипта\). | 
| startColumn | `integer` | Столбец смещения скрипта в ресурсе с заданным URL-адресом. | 
| endLine | `integer` | Последняя строка сценария. | 
| endColumn | `integer` | Длина последней строки сценария. | 
| executionContextId | [Runtime.ExecutionContextId](./runtime.md#executioncontextid) | Указывает контекст создания скрипта. |  
| sourceMapURL \(необязательный\) | `string` | URL-адрес исходных карт, связанных со сценарием (если таково). |  
| длина \(необязательный\) | `integer` | **Экспериментальные**.  Длина скрипта. |  
| msParentId \(необязательный\) | `string` | **Экспериментальные**.  Это родительский документ. |  
| msMimeType \(необязательный\) | `string` | **Экспериментальные**.  Это тип mime. |  
| msIsDynamicCode \(необязательный\) | `boolean` | **Экспериментальные**.  Это указывает, является ли это динамический код. |  
| msLongDocumentId \(необязательный\) | `integer` | **Экспериментальные**.  Это длинный документ. |  

---  

### <a name="breakpointresolved"></a>breakpointResolved  

В случае, если точка разрыва будет разрешена к фактическому сценарию и расположению.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| breakpointId | [BreakpointId](#breakpointid) | Уникальный идентификатор Breakpoint. |  
| расположение | [Расположение](#location) | Фактическое расположение точки разрыва. |  
| msLength \(необязательный\) | `integer` | **Экспериментальные**.  Microsoft. Длина кода \(то есть количество символов\) в расположении точки разрыва. |  

---  

### <a name="paused"></a>пауза  

Уволено, когда отладки ломаются для точки разлома или исключения.  

| Параметры | Тип | Сведения |  
|:--- |:--- |:--- |  
| callFrames | [CallFrame[]](#callframe) | Вызов стек отладки остановился. |  
| причина | `string` |  Причина паузы.  Допустимые значения:  `breakpoint` `step` , , , `exception` `other` и `EventListener` |  
| данные \(необязательный\) | `object` | Объект, содержащий отдельные вспомогательные свойства. |  
| hitBreakpoints \(необязательный\) | `string[]` | Hit breakpoints IDs |  
| asyncStackTrace \(необязательный\) | `StackTrace` | Трассировка стека async JavaScript. |  

---  

### <a name="resumed"></a>возобновлено  

Уволили, когда отладка возобновляет выполнение.  

&nbsp;  

---  

## <a name="types"></a>Типы  

### <a name="breakpointid-string"></a>Строка BreakpointId  

<a name="breakpointid"></a>  

Идентификатор Breakpoint.  

&nbsp;  

---  

### <a name="callframeid-string"></a>Строка CallFrameId  

<a name="callframeid"></a>  

Идентификатор кадра вызова.  

&nbsp;  

---  

### <a name="location-object"></a>Объект Location  

<a name="location"></a>  

Расположение в исходный код.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` . |  
| lineNumber | `integer` | Номер строки в скрипте \(0-based\). |  
| columnNumber \(необязательный\) | `integer` | Номер столбца в скрипте \(0-based\). |  
| msLength | `integer` | Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов. |  

---  

### <a name="breaklocation-object"></a>Объект BreakLocation  

<a name="breaklocation"></a>  

Разорвать расположение в исходный код.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| scriptId | [Runtime.ScriptId](./runtime.md#scriptid) | Идентификатор скрипта, как сообщалось в `Debugger.scriptParsed` . |  
| lineNumber | `integer` | Номер строки в скрипте \(0-based\). |  
| columnNumber \(необязательный\) | `integer` | Номер столбца в скрипте \(0-based\). |  
| msLength | `integer` | Microsoft. Длина кода \(то есть количество символов\) в этом кадре вызовов. |  
| тип \(необязательный\) | `string` | Допустимые значения: отладкаStatement, вызов, возврат. |  

---  

### <a name="callframe-object"></a>Объект CallFrame  

<a name="callframe"></a>  

Кадр вызова JavaScript. Массив кадров вызовов формирует стек вызовов.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| callFrameId | [CallFrameId](#callframeid) | Идентификатор кадра вызова.  Этот идентификатор действителен только во время паузы отладки. |  
| functionName | `string` | Имя функции JavaScript, вызываемой в этом кадре вызовов. |  
| functionLocation \(необязательный\) | [Расположение](#location) | **Экспериментальные**.  Расположение в исходный код. |  
| расположение | [Расположение](#location) | Расположение в исходный код. |  
| url | `string` | Имя сценария JavaScript или URL-адрес. |  
| scopeChain | [Область[]](#scope) | Цепочка области для этого кадра вызовов. |  
| это | [Runtime.RemoteObject](./runtime.md#remoteobject) | `this` объект для этого кадра вызовов. |  
| returnValue \(необязательный\) | [Runtime.RemoteObject](./runtime.md#remoteobject) | Возвращаемая величина, если функция находится в точке возврата. |  

---  

### <a name="scope-object"></a>Объект Scope  

<a name="scope"></a>  

Описание области.  

| Свойства | Тип | Сведения |  
|:--- |:--- |:--- |  
| Тип | `string` | Тип области.  Допустимые значения:  `global` , , , , , , `local` `with` `closure` `catch` `block` `script` , `eval` `module` и `return` |  
| объект | [Runtime.RemoteObject](./runtime.md#remoteobject) | Объект, представляющий область.  Для и областей он представляет фактический объект; для остальных областей это искусственный переходный объект, который в качестве свойств передает переменные `global` `with` области. |  
| имя \(необязательный\) | `string` | &nbsp; |  
| startLocation \(необязательный\) | [Расположение](#location) | Расположение в исходный код, где начинается область. |  
| endLocation \(необязательный\) | [Расположение](#location) | Расположение в исходный код, где область заканчивается. |  

---  

## <a name="dependencies"></a>Зависимости  

[Время выполнения](./runtime.md)  
