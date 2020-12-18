---
description: 'Задает функцию вызова, вызываемую во время работы перед сбором мусора. '
title: JsSetRuntimeBeforeCollectCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235290"
---
# Функция JsSetRuntimeBeforeCollectCallback

Задает функцию вызова, вызываемую во время работы перед сбором мусора.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### Параметры  
 `runtime`  
 Время запуска, для которого необходимо зарегистрировать вызов выделения.  
  
 `callbackState`  
 Пользовательское состояние, которое будет передано обратному вызову.  
  
 `beforeCollectCallback`  
 Устанавливаемая функция вызова.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Этот вызов вызывается в текущем потоке выполнения времени выполнения, поэтому выполнение блокируется до тех пор, пока он не завершится.  
  
 Для подготовки к сборке мусора хосты могут использовать этот вызов. Например, освобождая ненужные ссылки на объекты Chakra.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
