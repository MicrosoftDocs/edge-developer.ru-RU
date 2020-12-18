---
description: Контекст, переданный в обратном вызове приложения JsProjectionEnqueueCallback из JsRT, а затем передан обратно в JsRT в предоставленном обратном вызове приложением в правильном `JsProjectionCallback` потоке.
title: JsProjectionCallbackContext Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235627"
---
# JsProjectionCallbackContext Typedef

Контекст, переданный в обратном вызове приложения JsProjectionEnqueueCallback из JsRT, а затем передан обратно в JsRT в предоставленном обратном вызове приложением в правильном `JsProjectionCallback` потоке.  
  
## Синтаксис  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Комментарии  
 Требует вызова `JsSetProjectionEnqueueCallback` для получения вызовов.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
