---
description: Задает функцию вызова продолжения promise, вызываемую контекстом, когда задача должна быть поставлена в очередь для дальнейшего выполнения.
title: JsSetPromiseContinuationCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6ef0faf4-1500-4bd9-aeca-c208492af8ea
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da928431f05831c95d5bc116dbd129de9cb5f3b4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235540"
---
# Функция JsSetPromiseContinuationCallback

Задает функцию вызова продолжения promise, вызываемую контекстом, когда задача должна быть поставлена в очередь для дальнейшего выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetPromiseContinuationCallback(  
   _In_ JsPromiseContinuationCallback promiseContinuationCallback,  
   _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `promiseContinuationCallback`  
 Устанавливаемая функция вызова.  
  
 `callbackState`  
 Пользовательское состояние, которое будет передано обратному вызову.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
