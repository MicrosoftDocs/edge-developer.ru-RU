---
description: Вызов JsRT с контекстом, переданным в `JsProjectionEnqueueCallback` правильном потоке.
title: JsProjectionCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 211325b536dc84340974b02973f1de9d5749a60a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235631"
---
# JsProjectionCallback Typedef

Вызов JsRT с контекстом, переданным в `JsProjectionEnqueueCallback` правильном потоке.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Параметры  
 `jsContext`  
 Требует вызова `JsSetProjectionEnqueueCallback` для получения вызовов.  
  
## Комментарии  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
