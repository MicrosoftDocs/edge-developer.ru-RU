---
description: Добавляет ссылку на объект сборки мусора.
title: JsAddRef Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fd397dbfeacafdf12728ef0ca2a98d97405f6592
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235336"
---
# Функция JsAddRef

Добавляет ссылку на объект сборки мусора.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Параметры  
 `ref`  
 Объект, на который нужно добавить ссылку.  
  
 `count`  
 Новое количество ссылок объекта (может передаваться в null).  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Это необходимо только для работок, которые не будут храниться `JsRef` где-либо в стеке. Вызов гарантирует, что объект, на который ссылается, не будет `JsAddRef` `JsRef` освобожден, пока `JsRelease` не будет вызван.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
