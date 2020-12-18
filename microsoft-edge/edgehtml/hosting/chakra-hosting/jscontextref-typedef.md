---
description: Ссылка на контекст сценария.
title: JsContextRef Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c8a8fcbd67afb150d682cfc19321f0f13acfe3a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235323"
---
# JsContextRef Typedef

Ссылка на контекст сценария.  
  
## Синтаксис  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Комментарии  
 Каждый контекст сценария содержит собственный глобальный объект, который отличается от глобального объекта в других контекстах сценария.  
  
 Для многих API размещения chakra требуется контекст активного сценария, который можно настроить с помощью `JsSetCurrentContext` . При размещении API-api-akra, для которых требуется установить текущий контекст, обратите внимание, что в документации явно это помечается.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
