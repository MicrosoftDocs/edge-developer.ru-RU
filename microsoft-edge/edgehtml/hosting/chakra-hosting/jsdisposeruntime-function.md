---
description: Утилизирует дневный запуск.
title: JsDisposeRuntime Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8cff4578415cdf1aaa01b7203ce734cef9115301
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235506"
---
# Функция JsDisposeRuntime

Утилизирует дневный запуск.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Параметры  
 `runtime`  
 Время запуска, который необходимо утилизировать.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 После этого все ресурсы, которые она владеет, являются недопустимыми и не могут использоваться. Если время работы активно (то есть установлено в текущем состоянии в определенном потоке), его нельзя удалять.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
