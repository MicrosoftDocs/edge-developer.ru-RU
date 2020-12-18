---
description: Вызов приложения, вызываемого JsRT при заполнении API проекции в потоке, отличаемом от исходного.
title: JsProjectionEnqueueCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 47527d5e32076e40a82ab5452c2e0f624e8a2818
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235866"
---
# JsProjectionEnqueueCallback Typedef

Вызов приложения, вызываемого JsRT при заполнении API проекции в потоке, отличаемом от исходного.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `jsCallback`  
 Callback to be invoked on the original thread.  
  
 `jsContext`  
 Контекст приложений.  
  
 `callbackState`  
 Контекст JsRT, который необходимо `jsCallback` передать.  
  
## Комментарии  
 Для получения вызовов требуется вызов JsSetProjectionEnqueueCallback.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
