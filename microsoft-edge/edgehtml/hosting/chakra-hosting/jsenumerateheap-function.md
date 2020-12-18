---
description: Enumerates the heap of the current context.
title: JsEnumerateHeap Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bb76b28f24b769f71827e59be691188e34e9e1a3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235651"
---
# Функция JsEnumerateHeap

Enumerates the heap of the current context.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### Параметры  
 `enumerator`  
 The heap enumerator.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Во время перезаписи кучи текущий контекст удалить невозможно, а все вызовы для изменения состояния контекста будут неуспешными до тех пор, пока не будет отпущено нумератор кучи.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
