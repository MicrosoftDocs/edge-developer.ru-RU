---
description: Код ошибки, возвращаемой из API размещения Chakra.
title: JsErrorCode Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b0a4aa7b47070bd5c8c7fe48cdbecf0dbefa9aa5
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235440"
---
# Перечисление JsErrorCode

Код ошибки, возвращаемой из API размещения Chakra.  
  
## Синтаксис  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## Members  
  
### Значения  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|Контекст нельзя поместить в состояние отлаки, так как он уже находится в состоянии отлажки.|  
|`JsErrorAlreadyProfilingContext`|Контекст не может начать профилирование, так как он уже профилирование.|  
|`JsErrorArgumentNotObject`|API размещения, который работает со значениями объектов, был вызван с не объектным значением.|  
|`JsErrorBadSerializedScript`|Использовался плохой сериализованный сценарий или сериализованный сценарий с помощью другой версии ядра Chakra.|  
|`JsErrorCannotDisableExecution`|Runtime does not support reliable script interruption.|  
|`JsErrorCannotSerializeDebugScript`|Сценарии невозможно сериализовать в контекстах отлаки.|  
|`JsErrorCategoryEngine`|Категория ошибок, которая связана с ошибками, которые происходят в самом движке.|  
|`JsErrorCategoryFatal`|Категория ошибок, которые являются неудамительными и опишите сбой яда.|  
|`JsErrorCategoryScript`|Категория ошибок, которая связана с ошибками в сценарии.|  
|`JsErrorCategoryUsage`|Категория ошибок, связанная с неправильным использованием самого API.|  
|`JsErrorFatal`|Произошла неугомявная ошибка в движке.|  
|`JsErrorHeapEnumInProgress`|В настоящее время в контексте сценария ведется enumeration кучи.|  
|`JsErrorIdleNotEnabled`|Уведомление о бездействии, отданное, когда хост не включает обработку бездействия.|  
|`JsErrorInDisabledState`|Время работы отключено.|  
|`JsErrorInExceptionState`|Обдвижок находится в состоянии исключения, и пока исключение не будет очищено, никакие API не могут быть вызваны.|  
|`JsErrorInObjectBeforeCollectCallback`|Операция не поддерживается в объекте перед сбором вызова.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsErrorInProfileCallback`|Контекст сценария находится в середине вызова профиля.|  
|`JsErrorInThreadServiceCallback`|В настоящее время проводится вызов службы потоков.|  
|`JsErrorInvalidArgument`|Недопустимый аргумент для API размещения.|  
|`JsErrorNoCurrentContext`|Для размещения API требуется, чтобы контекст был текущим, но нет текущего контекста.|  
|`JsErrorNotImplemented`|API размещения еще не реализован.|  
|`JsErrorNullArgument`|В контексте, где не допускается использовать null, аргумент API размещения имеет null.|  
|`JsErrorObjectNotInspectable`|Объект не может быть развернулся на `IInspectable` указатель.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsErrorOutOfMemory`|В ядрах Chakra не потери памяти.|  
|`JsErrorPropertyNotSymbol`|API размещения, который работает с символьными идами свойств, но был вызван с не символьным идом свойства. Код ошибки возвращается, если функция вызвана с не `JsGetSymbolFromPropertyId` символьным идом свойства.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsErrorPropertyNotString`|API размещения, который работает с идами строковых свойств, но был вызван с не строковой ид свойства. Код ошибки возвращается существующим, если функция вызвана с не `JsGetPropertyNamefromId` строковым идом свойства.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsErrorRuntimeInUse`|Используемая по-прежнему время работы не может быть высвоена.|  
|`JsErrorScriptCompile`|Не удалось скомпилировать JavaScript.|  
|`JsErrorScriptEvalDisabled`|Сценарий был прерван из-за того, что он пытался использовать или `eval` `function` был отключен.|  
|`JsErrorScriptException`|При запуске сценария произошло исключение JavaScript.|  
|`JsErrorScriptTerminated`|Сценарий был завершен из-за запроса на приостановку работы.|  
|`JsErrorWrongRuntime`|Был вызван API размещения с объектом, созданным в другой среде работы JavaScript.|  
|`JsErrorWrongThread`|API размещения был вызван в неправильном потоке.|  
|`JsNoError`|Код ошибки успешной работы.|  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
