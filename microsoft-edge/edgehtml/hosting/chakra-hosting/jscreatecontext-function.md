---
description: Создает контекст сценария для запуска сценариев.
title: JsCreateContext Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235304"
---
# Функция JsCreateContext

Создает контекст сценария для запуска сценариев.  
  
## Синтаксис  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### Параметры  
 `runtime`  
 Время запуска, в котором создается контекст сценария.  
  
 `debugApplication`  
 Приложение отладки, которое будет использовать для отладки. Этот параметр может иметь null, в этом случае отладка для контекста не включена.  
  
 `newContext`  
 Контекст созданного сценария.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Каждый контекст сценария имеет собственный глобальный объект, изолированный от всех остальных контекстов сценария.  
  
 Параметр `debugApplication` не поддерживается в режиме Microsoft Edge. Дополнительные сведения об использовании этого API в режиме Microsoft Edge см. в подразделе "Нацелив [Microsoft Edge на устаревшие движки".](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md)  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
