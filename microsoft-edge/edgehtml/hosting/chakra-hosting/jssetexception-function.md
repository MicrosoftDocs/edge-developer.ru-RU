---
description: Задает состояние исключения для времени работы текущего контекста.
title: JsSetException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2c2e3840d2a831db23a525c5d8854b9b2fcfb8c9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235501"
---
# Функция JsSetException

Задает состояние исключения для времени работы текущего контекста.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Параметры  
 `exception`  
 Исключение JavaScript, устанавливаемого для времени работы текущего контекста.  
  
## Возвращенное значение  
 `JsNoError` если подстройка была перенастройка в состояние исключения, код сбоя в противном случае.  
  
## Комментарии  
 Если время работы текущего контекста уже находится в состоянии исключения, этот API `JsErrorInExceptionState` возвращается.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
