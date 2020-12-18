---
description: Создает новую функцию JavaScript с именем.
title: JsCreateNamedFunction Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b54add359422a9312a0ded641051fd04585f3d7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235442"
---
# Функция JsCreateNamedFunction

Создает новую функцию JavaScript с именем.
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Параметры  
 `name`  
 Имя этой функции, которая будет использоваться для диагностики и строки.  
  
 `nativeFunction`  
 Метод, вызываемого при вызове функции.  
  
 `callbackState`  
 Пользовательское состояние, которое будет передано обратному вызову.  
  
 `function`  
 Новый объект функции.  
  
## Возвращенное значение  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
