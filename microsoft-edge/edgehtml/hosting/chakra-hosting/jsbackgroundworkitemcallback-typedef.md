---
description: Вызов фонового элемента работы.
title: JsBackgroundWorkItemCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d69306b334c2e0c9b27b96a5a417739ffdcd7dd7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235334"
---
# JsBackgroundWorkItemCallback Typedef

Вызов фонового элемента работы.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Параметры  
 callbackData  
 Аргумент данных, переданный в службу потоков.  
  
## Комментарии  
 Он передается в потоковую службу хоста (если она предоставляется), чтобы разрешить хосту вызывать вызов элемента работы в фоновом потоке по своему выбору.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
