---
description: Задает текущий предел памяти для времени работы.
title: JsSetRuntimeMemoryLimit Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1c31d8bbbec4be22fc1af09e546ad4c95f8ec2bd
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235112"
---
# Функция JsSetRuntimeMemoryLimit

Задает текущий предел памяти для времени работы.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Параметры  
 `runtime`  
 Время работы, ограничение памяти которого необходимо установить.  
  
 `memoryLimit`  
 Новое ограничение памяти во время работы (в ветвях) или -1 (без ограничения памяти).  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Ограничение памяти приведет к сбойу любой операции, которая превышает ограничение, из-за ошибки "из памяти". Установка для времени работы ограничения памяти на -1 означает, что в среде работы нет предела памяти. Новые потери памяти по умолчанию не ограничиваются. Если новое ограничение памяти превышает текущий объем использования, вызов будет успешным, а любые будущие выделения в этой время будут невыполнена до тех пор, пока объем памяти в времени работы не опускается ниже предельного.  
  
 Ограничение памяти для времени работы всегда можно установить независимо от того, активна ли она в другом потоке.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
