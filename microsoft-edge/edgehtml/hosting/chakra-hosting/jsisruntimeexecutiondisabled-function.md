---
description: Возвращает значение, которое указывает, отключено ли выполнение сценария во время выполнения.
title: JsIsRuntimeExecutionDisabled Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235126"
---
# Функция JsIsRuntimeExecutionDisabled

Возвращает значение, которое указывает, отключено ли выполнение сценария во время выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Параметры  
 `runtime`  
 Указывает времени выполнения, чтобы проверить, отключено ли выполнение.  
  
 `isDisabled`  
 `true` если выполнение отключено, `false` в противном случае.  
  
## Возвращенное значение  
 `JsNoError` если операция прошла успешно, код сбоя в противном случае.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
