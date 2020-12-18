---
description: Возвращает исключение, из-за чего время работы текущего контекста было в состоянии исключения, и сбрасывает состояние исключения для этой времени.
title: JsGetAndClearException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cb296ea351d0466a856d5ac020550ebacc254ac9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235428"
---
# Функция JsGetAndClearException

Возвращает исключение, из-за чего время работы текущего контекста было в состоянии исключения, и сбрасывает состояние исключения для этой времени.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Параметры  
 `exception`  
 Исключение для времени работы текущего контекста.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Если время работы текущего контекста находится не в состоянии исключения, этот API `JsErrorInvalidArgument` возвращается. Если время работы отключено, будет возвращено исключение, указывающее на то, что сценарий был завершен, но исключение не будет очищено (исключение будет очищено при повторном включаемом использовании). `JsEnableRuntimeExecution`  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
