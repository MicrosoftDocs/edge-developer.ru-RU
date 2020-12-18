---
description: Определяет, находится ли время работы текущего контекста в состоянии исключения.
title: JsHasException Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4f4abbd6c69a6b2b6414dae2f1de3a2acf21cc32
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235169"
---
# Функция JsHasException

Определяет, находится ли время работы текущего контекста в состоянии исключения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Параметры  
 `hasException`  
 Находится ли время запуска текущего контекста в состоянии исключения.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Если вызов в окн. ок. приводит к исключению (в результате запуска сценария или из-за ошибки преобразования), то она переводит ее в "состояние исключения". Все вызовы в любом контексте, созданном в среде запуска (за исключением API-api исключений), будут неудались до тех пор, пока исключение не будет `JsErrorInExceptionState` очищено.  
  
 Если время работы текущего контекста находится в состоянии исключения при возвращении обратного вызова в обдвижку, обдвижок автоматически перезаписал исключение.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
