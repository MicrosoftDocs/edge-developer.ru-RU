---
description: Пользователь реализовал процедуру вызова для событий выделения памяти.
title: JsMemoryAllocationCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 22b5cc0fe5a2c8b49f71c91d28f95ba29af37849
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235302"
---
# JsMemoryAllocationCallback Typedef

Пользователь реализовал процедуру вызова для событий выделения памяти.  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Параметры  
 callbackState  
 Состояние, переданное в JsSetRuntimeMemoryAllocationCallback.  
  
 allocationEvent  
 Тип события выделения типов.  
  
 allocationSize  
 Размер выделения.  
  
## Значение свойства или возвращаемая величина  
 Для события JsMemoryAllocate возврат true позволяет времени работы продолжить выделение. Возврат false означает, что запрос на выделение отклонен. Возвращаемая величина игнорируется для других событий выделения.  
  
## Комментарии  
 Используйте JsSetRuntimeMemoryAllocationCallback для регистрации этого вызова.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
