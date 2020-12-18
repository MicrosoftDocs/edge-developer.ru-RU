---
description: Сообщает времени работы, что необходимо выполнить любую обработку без простоя.
title: JsIdle Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ecba0aafb6b4dcccb4485c2956cae5ce4045355f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235815"
---
# Функция JsIdle

Сообщает времени работы, что необходимо выполнить любую обработку без простоя.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Параметры  
 `nextIdleTick`  
 Следующий системный такт, когда будет больше работы без простоя. Может иметь null. Возвращает максимальное число тактов, если предстоящих бездействуют.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Если для текущей времени выполнения включена обработка бездействия, вызовы проинформят текущую порядок выполнения о том, что хост бездействует и что она может выполнять задачи очистки `JsIdle` памяти.  
  
 `JsIdle` также может возвращать количество системных тиков, пока не будет больше работы в режиме простоя, чтобы сделать это. Вызов до того, как прошло это число, не `JsIdle` даст никаких трудоемких трудоемкого.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
