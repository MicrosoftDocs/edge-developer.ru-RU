---
description: Создает новый объект ошибки JavaScript URIError.
title: JsCreateURIError Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235441"
---
# Функция JsCreateURIError

Создает новый объект ошибки JavaScript URIError.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### Параметры  
 `message`  
 Сообщение для объекта ошибки.  
  
 `error`  
 Новый объект ошибки.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
