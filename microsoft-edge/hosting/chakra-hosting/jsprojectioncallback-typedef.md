---
description: Обратный вызов JsRT, который должен вызываться с контекстом, передаваемым `JsProjectionEnqueueCallback` в нужном потоке.
title: JsProjectionCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571345"
---
# JsProjectionCallback typedef
Обратный вызов JsRT, который должен вызываться с контекстом, передаваемым `JsProjectionEnqueueCallback` в нужном потоке.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### Параметры  
 `jsContext`  
 Требуется вызов `JsSetProjectionEnqueueCallback` для приема обратных вызовов.  
  
## Комментарии  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)