---
description: Приостанавливать выполнение сценариев и прерывать все запущенные сценарии в реализации.
title: JsDisableRuntimeExecution Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a08e6a7f89c724f8cf1a73afd97d2cb23c0334e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235505"
---
# Функция JsDisableRuntimeExecution

Приостанавливать выполнение сценариев и прерывать все запущенные сценарии в реализации.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Параметры  
 `runtime`  
 Приостановка времени работы.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Вызовы приостановленной времени работы будут неудались до тех пор, `JsEnableRuntimeExecution` пока не будут вызваны.  
  
 Этот API не должен быть вызван в потоке, в который активно время работы. Хотя время выполнения будет приостановлено, выполнение сценария может быть приостановлено не сразу; Запущенный сценарий будет как можно скорее завершен с помощью неуявяемого исключения.  
  
 Приостановка выполнения в уже приостановленной времени выполнения не является действием.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
