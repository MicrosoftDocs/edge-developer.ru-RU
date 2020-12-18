---
description: Извлекает `int` значение числимого значения.
title: JsNumberToInt Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 928be9a7cc5cd3e26e8b8df99af1e08a6c50209c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235643"
---
# Функция JsNumberToInt

Извлекает `int` значение числимого значения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Параметры  
 `value`  
 Число, преобразуемого в `int` значение.  
  
 `intValue`  
 `int`Значение.  
  
## Возвращенное значение  
  
## Комментарии  
 Эта функция извлекает значение числимого значения и преобразуется в `int` значение. Он не будет `JsErrorInvalidArgument` работать, если тип значения не является числом.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
