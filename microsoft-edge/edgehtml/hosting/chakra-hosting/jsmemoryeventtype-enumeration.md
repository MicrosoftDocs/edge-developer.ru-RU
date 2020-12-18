---
description: Тип события распределения событий для вызова вызова.
title: JsMemoryEventType Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a28010f908285098cf652b497b6d6c272bc763fc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235111"
---
# Перечисление JsMemoryEventType

Тип события распределения событий для вызова вызова.  
  
## Синтаксис  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Members  
  
### Значения  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsMemoryAllocate`|Указывает запрос на выделение памяти.|  
|`JsMemoryFailure`|Указывает, что произошел сбой выделения.|  
|`JsMemoryFree`|Указывает на событие освободить память.|  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
