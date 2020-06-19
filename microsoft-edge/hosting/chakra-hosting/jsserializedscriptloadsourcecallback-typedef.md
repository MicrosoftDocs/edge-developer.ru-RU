---
description: Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752201"
---
# JsSerializedScriptLoadSourceCallback Typedef
Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Параметры  
 `sourceContext`  
 Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 Возвращаемый сценарий.  
  
## Комментарии  
  
> [!WARNING]
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)