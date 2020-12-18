---
description: Функция вызова.
title: JsNativeFunction Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235125"
---
# JsNativeFunction Typedef

Функция вызова.  
  
## Синтаксис  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Параметры  
 вызываемая  
 Объект, `Function` который представляет вызываемую функцию.  
  
 isConstructCall  
 Указывает, является ли этот вызов регулярным или новым.  
  
 arguments  
 Аргументы вызова.  
  
 argumentCount  
 Количество аргументов.  
  
## Значение свойства или возвращаемая величина  
 Результат вызова, если он есть.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
