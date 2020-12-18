---
description: Вызвано во время выполнения после завершения работы со всеми ресурсами, связанными с выполнением сценария. В настоящее время вызываемая служба должна освободить источник, код ветвей и контекст.
title: JsSerializedScriptUnloadCallback typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235813"
---
# JsSerializedScriptUnloadCallback typedef

Вызвано во время выполнения после завершения работы со всеми ресурсами, связанными с выполнением сценария. В настоящее время вызываемая служба должна освободить источник, код для byte и контекст.  
  
## Синтаксис  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Параметры  
 `sourceContext`  
 Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .  
  
## Комментарии  
  
> [!WARNING]
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
