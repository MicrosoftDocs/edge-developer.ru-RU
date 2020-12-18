---
description: Останавливает профилирование в текущем контексте.
title: JsStopProfiling Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 02c42afda7e61d71b90a9a1a71aa71cc53584ff8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235495"
---
# Функция JsStopProfiling

Останавливает профилирование в текущем контексте.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Параметры  
 `reason`  
 Причина остановки профилирование, передав его в вызов профиля.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.  
  
## Комментарии  
 Не возвращает ошибку, если профилирование не запущено.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
