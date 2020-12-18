---
description: Вызов продолжения обещания.
title: JsPromiseContinuationCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da121d186cd9d0ab1a9770be08c9a92b52cf3366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235864"
---
# JsPromiseContinuationCallback Typedef

Вызов продолжения обещания.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `task`  
  `callbackState`  
  
## Комментарии  
 В хост-вызове можно указать вызов продолжения `JsSetPromiseContinuationCallback` promise. Если сценарий создает задачу, которая будет выполняться позже, то с задачей будет вызван вызов вызова продолжения promise, и задача должна быть поставлена в очередь FIFO, которая будет выполняться после выполнения текущего сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
