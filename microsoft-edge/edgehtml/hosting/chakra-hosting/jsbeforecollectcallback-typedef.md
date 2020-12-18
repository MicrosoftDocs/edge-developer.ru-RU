---
description: Callback called before collection.
title: JsBeforeCollectCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 23ed386a6a28d356aa80cf85650a981d4836a6b6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235325"
---
# JsBeforeCollectCallback Typedef

Callback called before collection.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 callbackState  
 Состояние, передамое в JsSetBeforeCollectCallback.  
  
## Комментарии  
 Используйте JsSetBeforeCollectCallback для регистрации этого вызова.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
