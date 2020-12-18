---
description: Получает ИД свойства, связанного с именем.
title: JsGetPropertyIdFromName Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235654"
---
# Функция JsGetPropertyIdFromName

Получает ИД свойства, связанного с именем.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### Параметры  
 `name`  
 Имя ИД свойства, которое требуется получить или создать. Имя может состоять только из цифр.  
  
 `propertyId`  
 ИД свойства в этой времени работы для заданного имени.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 ИД свойств являются специфическими для контекста и не могут использоваться в контекстах.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
