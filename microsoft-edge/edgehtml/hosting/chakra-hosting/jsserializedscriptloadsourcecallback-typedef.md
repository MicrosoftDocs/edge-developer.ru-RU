---
description: Вызвано во время работы для загрузки исходный код сериализованного сценария. Вызывающая должна оставить буфер скрипта допустимым, пока не будет отсвеяна. `JsSerializedScriptUnloadCallback`
title: JsSerializedScriptLoadSourceCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235863"
---
# JsSerializedScriptLoadSourceCallback Typedef

Вызвано во время работы для загрузки исходный код сериализованного сценария. Вызывающая должна оставить буфер скрипта допустимым, пока не будет отсвеяна. `JsSerializedScriptUnloadCallback`  
  
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
 Сценарий возвращается.  
  
## Комментарии  
  
> [!WARNING]
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
