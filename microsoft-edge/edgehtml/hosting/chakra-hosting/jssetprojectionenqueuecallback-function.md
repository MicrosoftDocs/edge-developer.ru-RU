---
description: Задает обратное вызов, который будет использоваться для вызова завершения проекции для требуемого потока вызывающих.
title: JsSetProjectionEnqueueCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7dfedfeb1df5a97159a211795a2dd072d239bb35
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235285"
---
# Функция JsSetProjectionEnqueueCallback

Задает обратное вызов, который будет использоваться для вызова завершения проекции для требуемого потока вызывающих.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Параметры  
 `projectionEnqueueContext`  
 Вызов, который будет вызываться при завершении проекции в фоновом потоке.  
  
 `callbackState`  
 Контекст приложения, предоставленный `projectionEnqueueContext` для .  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Вызов должен быть исходя из другого com-или другого потока в той же MTA.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
> [!CAUTION]
>  PInvoke в настоящее время не поддерживается для этого API.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
