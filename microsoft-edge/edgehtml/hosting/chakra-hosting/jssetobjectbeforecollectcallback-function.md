---
description: Задает функцию вызова, вызываемую во время работы перед сборкой мусора объекта.
title: JsSetObjectBeforeCollectCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4689184dccaf6bc9f98eeacda5f5a4b91a927d40
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235289"
---
# Функция JsSetObjectBeforeCollectCallback

Задает функцию вызова, вызываемую во время работы перед сборкой мусора объекта.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Параметры  
 `ref`  
 Объект, для которого необходимо зарегистрировать вызов.  
  
 `callbackState`  
 Предоставленное пользователем состояние, которое будет передано обратному вызову.  
  
 `objectBeforeCollectCallback`  
 Устанавливаемая функция вызова. Используйте null, чтобы очистить зарегистрированный ранее вызов.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 В текущем потоке выполнения выполнения вызывается метод callback, поэтому выполнение блокируется до тех пор, пока он не завершится.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
