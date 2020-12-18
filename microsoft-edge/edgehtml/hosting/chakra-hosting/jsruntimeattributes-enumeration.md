---
description: 'Атрибуты времени работы. '
title: JsRuntimeAttributes Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bbc5341c3214d9796278d334507e284989ff45dd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235426"
---
# Перечисление JsRuntimeAttributes

Атрибуты времени работы.  
  
## Синтаксис  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## Members  
  
### Значения  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|Время работы должно поддерживать надежное прерывание скриптов. Это увеличивает количество мест, в которых время выполнения будет проверять запрос на прерывание сценария за счет небольшой производительности времени выполнения.|  
|`JsRuntimeAttributeDisableBackgroundWork`|В фоновых потоках не будет работать (например, сборка мусора).|  
|`JsRuntimeAttributeDisableEval`|При `eval` использовании `function` или конструкторе будет выводиться исключение.|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|Во время работы не будет создаваться исходный код.|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|В режиме запуска будут работать все экспериментальные функции.|  
|`JsRuntimeAttributeEnableIdleProcessing`|Будет вызываться `JsIdle` хост, поэтому включается простаивающая обработка. В противном случае время работы будет управлять памятью немного более агрессивно.|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|Вызов также отправляет исключение отладильщику скрипта (при его найме), что дает возможность отладить `JsSetException` исключение.|  
|`JsRuntimeAttributeNone`|Нет специальных атрибутов.|  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
