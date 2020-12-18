---
description: Инициализирует переданный в качестве `VARIANT` проекции значения JavaScript.
title: JsValueToVariant Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235454"
---
# Функция JsValueToVariant

Инициализирует переданный в качестве `VARIANT` проекции значения JavaScript.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Параметры  
 `object`  
 Значение JavaScript для проекта в качестве `VARIANT` .  
  
 `variant`  
 Указатель на `VARIANT` структуру, которая инициализируются как проекция.  
  
## Возвращенное значение  
  
## Комментарии  
 Проекция `VARIANT` может использоваться клиентами автоматизации COM для вызова проецируемых объектов JavaScript.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
