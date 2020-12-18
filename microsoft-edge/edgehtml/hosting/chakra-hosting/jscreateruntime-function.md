---
description: Создает новую time runtime.
title: JsCreateRuntime Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235523"
---
# Функция JsCreateRuntime

Создает новую time runtime.
  
## Синтаксис  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Параметры  
 `attributes`  
 Атрибуты создаемой времени работы.  
  
 `version`  
 Версия создаемой времени работы.  
  
 `threadService`  
 Служба потоков для времени работы. Может иметь null.  
  
 `runtime`  
 Созданная время работы.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Параметр `version` не поддерживается в режиме Microsoft Edge. Дополнительные сведения об использовании этого API в режиме Microsoft Edge см. в подразделе "Нацелив [Microsoft Edge на устаревшие движки".](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md)  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
