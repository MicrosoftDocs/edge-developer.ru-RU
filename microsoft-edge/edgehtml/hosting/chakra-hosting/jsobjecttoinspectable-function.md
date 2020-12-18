---
description: Отвергет объект JavaScript на `IInspectable` указатель.
title: JsObjectToInspectable Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235633"
---
# Функция JsObjectToInspectable

Отвергет объект JavaScript на `IInspectable` указатель.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### Параметры  
 `value`  
 Значение JavaScript, которое должно быть проецируемым на `IInspectable` .  
  
 `inspectable`  
 Значение `IInspectable` объекта.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Ведущие точки отвечают за принудительное применение правил потоков COM.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
