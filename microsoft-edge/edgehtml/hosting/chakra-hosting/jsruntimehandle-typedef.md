---
description: Handle to a Chakra runtime.
title: JsRuntimeHandle Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235287"
---
# JsRuntimeHandle Typedef

Handle to a Chakra runtime.  
  
## Синтаксис  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Комментарии  
 У каждой реализации Chakra есть собственный независимый механизм выполнения, компилятор JIT и куч, собираемая мусора. Поэтому каждая из них полностью изолирована от других.  
  
 Times can be used on any thread, but only one thread can call into a runtime at any time.  
  
> [!WARNING]
>  JsRuntimeHandle, в отличие от других ссылок на объекты в API размещения Chakra, не является сборщиком мусора, так как содержит сам по себе собранный мусора. Время работы будет существовать до тех пор, пока не будет вызвана JsDisposeRuntime.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
