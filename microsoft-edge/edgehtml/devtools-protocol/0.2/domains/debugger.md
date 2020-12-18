---
description: Справочник по протоколу DevTools версии 0.2 (EdgeHTML) для домена отлада. Домен отлада предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.
title: Домен отлада — протокол DevTools версии 0.2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24571b3a32acf085dd9ccbd641b1e5b06b3b9504
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235190"
---
# Домен отлада — протокол DevTools версии 0.2 (EdgeHTML)  

Домен отладки предоставляет возможности отладки JavaScript. Он позволяет устанавливать и удалять точки останова, пошаговую настройку выполнения, изучать трассировки стека и т. д.

| | |
|-|-|
| [**Методы**](#methods) | [enable](#enable), [disable](#disable), [getPossibleBreakpoints](#getpossiblebreakpoints), [setBreakpointsActive](#setbreakpointsactive), [setBreakpointByUrl](#setbreakpointbyurl), [setBreakpoint](#setbreakpoint), [removeBreakpoint](#removebreakpoint), [stepOver](#stepover), [stepInto](#stepinto), [stepOut](#stepout), [pause](#pause), [resume](#resume), [getScriptSource](#getscriptsource), [setPauseOnExceptions](#setpauseonexceptions), [evaluateOnCallFrame](#evaluateoncallframe), [setVariableValue](#setvariablevalue), [setBlackboxPatterns](#setblackboxpatterns), [msSetDebuggerPropertyValue](#mssetdebuggerpropertyvalue) |
| [**Мероприятия**](#events) | [scriptParsed,](#scriptparsed) [breakpointResolved,](#breakpointresolved) [приостановлено,](#paused) [возобновлено](#resumed) |
| [**Типы**](#types) | [BreakpointId](#breakpointid), [CallFrameId](#callframeid), [Location](#location), [BreakLocation](#breaklocation), [CallFrame](#callframe), [Scope](#scope) |
| [**Зависимости**](#dependencies) | [Время выполнения](runtime.md) |
## Методы

### "Включить"
Включает отладок для заданной страницы. Клиенты не должны предполагать, что отладка включена, пока не будет получен результат для этой команды.

</p>

---

### "Отключить" 
Отключает отладок для данной страницы.

</p>

---

### getPossibleBreakpoints
Возвращает возможные расположения для точки останова. ScriptId в расположениях в начале и конце диапазона должен быть одинаковым.

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
            <td>start</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Начало диапазона для поиска возможных местоположений точек останова.</td>
        </tr>
        <tr>
            <td>завершить</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Конец диапазона для поиска возможных местоположений точек останова в (за исключением). Если он не указан, конец диапазона используется для окончания сценариев.</td>
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
            <td>locations</td>
            <td><a href="#breaklocation"><code class="flyout">BreakLocation</code></a></td>
            <td>Список возможных местоположений точек останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointsActive
Активирует или деактивирует все точки останова на странице.

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
            <td>active</td>
            <td><code class="flyout">boolean</code></td>
            <td>Новое значение активного состояния точек останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpointByUrl
Задает точку останова JavaScript в указанном расположении, указанном с помощью URL-адреса или regex URL-адреса. После того как эта команда будет выдана, все существующие сценарии будут иметь точки останова, разрешенные и возвращенные в <code>locations</code> свойстве. Дальнейшее соответствие сценариев приведет к последующим <code>breakpointResolved</code> событиям. Эта логическая точка останова будет выдержать перезагрузку страницы.

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
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки для назначения точки останова.</td>
        </tr>
        <tr>
            <td>url <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес ресурсов для назначения точки останова.</td>
        </tr>
        <tr>
            <td>urlRegex <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Шаблон повторного использования URL-адресов ресурсов, в которые необходимо установить точки останова. Либо <code>url</code> должно <code>urlRegex</code> быть указано, либо должно быть указано.</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение в строке для назначения точки останова.</td>
        </tr>
        <tr>
            <td>condition <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Выражение, используемое в качестве условия точки останова. Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ИД созданной точки останова для дальнейшей ссылки.</td>
        </tr>
        <tr>
            <td>locations</td>
            <td><a href="#location"><code class="flyout">Location[]</code></a></td>
            <td>Список местоположений, в которые эта точка останова была разрешена после добавления.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBreakpoint
Задает точку останова JavaScript в заданное расположение.

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
            <td>location</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение для определения точки останова.</td>
        </tr>
        <tr>
            <td>condition <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Выражение, используемое в качестве условия точки останова. Если этот способ указан, отладка останавливается только в точке останова, если это выражение оценивается как истинное.</td>
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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>ИД созданной точки останова для дальнейшей ссылки.</td>
        </tr>
        <tr>
            <td>actualLocation</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение, в который разрешена точка останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### removeBreakpoint
Удаляет точку останова JavaScript.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### stepOver
По шагам над заявлением.

</p>

---

### stepInto
Этапы вызова функции.

</p>

---

### stepOut
По шагам из вызова функции.

</p>

---

### pause
Останавливает следующий отчет JavaScript.

</p>

---

### resume
Возобновляет выполнение JavaScript.

</p>

---

### getScriptSource
Возвращает источник для сценария с заданным идом.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>ИД сценария, для который требуется получить источник.</td>
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
            <td>scriptSource</td>
            <td><code class="flyout">string</code></td>
            <td>Источник скрипта.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setPauseOnExceptions
Определяет паузу в состоянии исключений. Можно установить остановку для всех исключений, невысченных исключений или без исключений. Начальная пауза в состоянии исключений <code>none</code> — .

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
            <td>state</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: none, uncaught, all</i></td>
            <td>Приостановка в режиме исключений.</td>
        </tr>
    </tbody>
</table>
</p>

---

### evaluateOnCallFrame
Оценивает выражение в заданной рамке вызова.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Идентификатор кадра вызова для оценки.</td>
        </tr>
        <tr>
            <td>выражение</td>
            <td><code class="flyout">string</code></td>
            <td>Выражение для оценки.</td>
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
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Оболочка объекта для результата оценки.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setVariableValue
Изменяет значение переменной в callframe. Области на основе объектов не поддерживаются и должны быть мутированы вручную.

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
            <td>scopeNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Число областей на основе 0, указанных в цепочке областей. Разрешены только типы областей "local", "closure" и "catch". Другие области могут управляться вручную.</td>
        </tr>
        <tr>
            <td>variableName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя переменной.</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><a href="runtime.md#callargument"><code class="flyout">Runtime.CallArgument</code></a></td>
            <td>Новое значение переменной.</td>
        </tr>
        <tr>
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>ИД callframe, который содержит переменную.</td>
        </tr>
    </tbody>
</table>
</p>

---

### setBlackboxPatterns
<span><b>Экспериментальная. </b></span>Замените предыдущие шаблоны черных ящиков на переданные. Заставляет тыловые части пропускать пошаговую или приоходную пошаговую отрисовку в сценариях с URL-адресом, совпадающий с одним из шаблонов. Отладик попытается выйти из сценария из черной почты, выполив "шаг" несколько раз, и, наконец, при неудачном выполнении прибег к шагу "выйти".

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
            <td>patterns</td>
            <td><code class="flyout">string[]</code></td>
            <td>Массив regexps, который будет использоваться для проверки URL-адреса скрипта на состояние черного ящика.</td>
        </tr>
    </tbody>
</table>
</p>

---

### msSetDebuggerPropertyValue
<span><b>Экспериментальная. </b></span>Корпорация Майкрософт: задает указанное значение для указанного свойства отладки.

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
            <td>debuggerPropertyId</td>
            <td><code class="flyout">string</code></td>
            <td>Майкрософт: ид свойства (например, msDebuggerPropertyId), который необходимо установить.</td>
        </tr>
        <tr>
            <td>newValue</td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

## Мероприятия

### scriptParsed
Срасть при разчете сценария. Это событие также иллюбуется для всех известных и несмеченных сценариев при включии отладки.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор разлияемого скрипта.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес или имя разбияемого сценария (если таково).</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение строк скрипта в ресурсе с заданным URL-адресом (для тегов скрипта).</td>
        </tr>
        <tr>
            <td>startColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Смещение столбцов сценария в ресурсе с заданным URL-адресом.</td>
        </tr>
        <tr>
            <td>endLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Последняя строка сценария.</td>
        </tr>
        <tr>
            <td>endColumn</td>
            <td><code class="flyout">integer</code></td>
            <td>Длина последней строки сценария.</td>
        </tr>
        <tr>
            <td>executionContextId</td>
            <td><a href="runtime.md#executioncontextid"><code class="flyout">Runtime.ExecutionContextId</code></a></td>
            <td>Указывает контекст создания скрипта.</td>
        </tr>
        <tr>
            <td>sourceMapURL <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>URL-адрес карты источника, связанной со сценарием (если таково).</td>
        </tr>
        <tr>
            <td>length <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Экспериментальная. </b></span>Длина этого скрипта.</td>
        </tr>
        <tr>
            <td>msParentId <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Экспериментальная. </b></span>Это родительский ИД документа.</td>
        </tr>
        <tr>
            <td>msMimeType <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td><span><b>Экспериментальная. </b></span>Это тип MIME.</td>
        </tr>
        <tr>
            <td>msIsDynamicCode <br/> <i>необязательные</i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span><b>Экспериментальная. </b></span>Это указывает, является ли это динамическим кодом.</td>
        </tr>
        <tr>
            <td>msLongDocumentId <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Экспериментальная. </b></span>Это длинный ИД документа.</td>
        </tr>
    </tbody>
</table>
</p>

---

### breakpointResolved
Происходит, когда точка останова разрешена к фактическому сценарию и расположению.

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
            <td>breakpointId</td>
            <td><a href="#breakpointid"><code class="flyout">BreakpointId</code></a></td>
            <td>Уникальный идентификатор точки останова.</td>
        </tr>
        <tr>
            <td>location</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Фактическое расположение точки останова.</td>
        </tr>
        <tr>
            <td>msLength <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td><span><b>Экспериментальная. </b></span>Майкрософт: длина кода (то есть количество символов) в расположении точки останова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### пауза
Происходит, когда отладки разрывают точку останова или исключение.

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
            <td>callFrames</td>
            <td><a href="#callframe"><code class="flyout">CallFrame[]</code></a></td>
            <td>Вызовите стек, на который остановлен отладок.</td>
        </tr>
        <tr>
            <td>reason</td>
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: точка останова, шаг, исключение, другое, EventListener</i></td>
            <td>Причина приостановки.</td>
        </tr>
        <tr>
            <td>data <br/> <i>необязательные</i></td>
            <td><code class="flyout">object</code></td>
            <td>Объект, содержащий вспомогательные свойства для конкретного разрыва.</td>
        </tr>
        <tr>
            <td>hitBreakpoints <br/> <i>необязательные</i></td>
            <td><code class="flyout">string[]</code></td>
            <td>ИД точек останова</td>
        </tr>
        <tr>
            <td>asyncStackTrace <br/> <i>необязательные</i></td>
            <td><!--  <a href="#stacktrace">  --><code class="flyout">StackTrace</code><!--  </a>  --></td>
            <td>Трассировка а async стека JavaScript.</td>
        </tr>
    </tbody>
</table>
</p>

---

### возобновлено
Собяно, когда отладка возобновляет выполнение.

</p>

---

## Типы

### <a name="breakpointid"></a> BreakpointId `string`

Идентификатор точки останова.

</p>

---

### <a name="callframeid"></a> CallFrameId `string`

Идентификатор кадра вызова.

</p>

---

### <a name="location"></a> Location `object`

Расположение в коде источника.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор скрипта, как по данным в <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки в сценарии (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца в сценарии (на основе 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="breaklocation"></a> BreakLocation `object`

Место приорвать в исходный код.

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
            <td>scriptId</td>
            <td><a href="runtime.md#scriptid"><code class="flyout">Runtime.ScriptId</code></a></td>
            <td>Идентификатор сценария, как сообщается в <code>Debugger.scriptParsed</code> .</td>
        </tr>
        <tr>
            <td>lineNumber</td>
            <td><code class="flyout">integer</code></td>
            <td>Номер строки в сценарии (на основе 0).</td>
        </tr>
        <tr>
            <td>columnNumber <br/> <i>необязательные</i></td>
            <td><code class="flyout">integer</code></td>
            <td>Номер столбца в сценарии (на основе 0).</td>
        </tr>
        <tr>
            <td>msLength</td>
            <td><code class="flyout">integer</code></td>
            <td>Майкрософт: длина кода (то есть количество символов) в этом фрейме вызова.</td>
        </tr>
        <tr>
            <td>Тип <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td>Допустимые значения: debuggerStatement, call, return.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="callframe"></a> CallFrame `object`

Фрейм вызова JavaScript. Массив кадров вызовов формирует стек вызовов.

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
            <td>callFrameId</td>
            <td><a href="#callframeid"><code class="flyout">CallFrameId</code></a></td>
            <td>Идентификатор кадра вызова. Этот идентификатор действителен, только когда отладка приостановлена.</td>
        </tr>
        <tr>
            <td>functionName</td>
            <td><code class="flyout">string</code></td>
            <td>Имя функции JavaScript, вызываемой в этом фрейме вызова.</td>
        </tr>
        <tr>
            <td>functionLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td><span><b>Экспериментальная. </b></span>Расположение в коде источника.</td>
        </tr>
        <tr>
            <td>location</td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение в коде источника.</td>
        </tr>
        <tr>
            <td>url</td>
            <td><code class="flyout">string</code></td>
            <td>Имя или URL-адрес сценария JavaScript.</td>
        </tr>
        <tr>
            <td>scopeChain</td>
            <td><a href="#scope"><code class="flyout">Scope[]</code></a></td>
            <td>Цепочка областей для этого кадра вызова.</td>
        </tr>
        <tr>
            <td>это</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td><code>this</code> объект для этого кадра вызова.</td>
        </tr>
        <tr>
            <td>returnValue <br/> <i>необязательные</i></td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Возвращаемая величина, если функция находится в точке возврата.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="scope"></a> Область применения `object`

Описание области.

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
            <td><code class="flyout">string</code> <br/> <i>Допустимые значения: global, local, with, closure, catch, block, script, eval, module, return</i></td>
            <td>Тип области.</td>
        </tr>
        <tr>
            <td>объект</td>
            <td><a href="runtime.md#remoteobject"><code class="flyout">Runtime.RemoteObject</code></a></td>
            <td>Объект, представляющий область. For <code>global</code> and <code>with</code> scopes it represents the actual object; for the rest of the scopes, it is artificial transient object enumerating scope variables as its properties.</td>
        </tr>
        <tr>
            <td>name <br/> <i>необязательные</i></td>
            <td><code class="flyout">string</code></td>
            <td></td>
        </tr>
        <tr>
            <td>startLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение в исходный код, где начинается область</td>
        </tr>
        <tr>
            <td>endLocation <br/> <i>необязательные</i></td>
            <td><a href="#location"><code class="flyout">Location</code></a></td>
            <td>Расположение в коде источника, где заканчивается область</td>
        </tr>
    </tbody>
</table>
</p>

---

## Зависимости

[Время выполнения](runtime.md)
