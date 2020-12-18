---
description: Задает callback выделения памяти для указанной времени работы.
title: JsSetRuntimeMemoryAllocationCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ee2abf36e14c26ac58b90d48a6115fd6502307c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235460"
---
# Функция JsSetRuntimeMemoryAllocationCallback

Задает callback выделения памяти для указанной времени работы.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Параметры  
 `runtime`  
 Время запуска, для которого необходимо зарегистрировать вызов выделения.  
  
 `callbackState`  
 Пользовательское состояние, которое будет передано обратному вызову.  
  
 `allocationCallback`  
 Callback выделения памяти, вызываемой для событий выделения памяти.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Регистрация обратного вызова выделения памяти приведет к тому, что время работы будет вызывать хост каждый раз, когда она получает память от ОС или освобождает ее в нее. Процедура перенаправления вызовов вызвана до того, как диспетчер памяти во время работы выделяет блок памяти. Выделение будет отклонено, если при обратном вызове возвращается false. Диспетчер памяти во время работы также вызывает процедуру вызова после освободить блок памяти, а также после сбоев выделения.  
  
 Этот вызов вызывается в текущем потоке выполнения времени выполнения, поэтому выполнение блокируется до тех пор, пока он не завершится.  
  
 Возвращаемая величина обратного вызова не сохраняется; ранее отклоненные выделения не помешают времени работы вызвать обратное вызов позже для нового выделения памяти.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
