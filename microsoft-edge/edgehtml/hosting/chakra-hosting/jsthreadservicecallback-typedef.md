---
description: Вызов службы потоков.
title: JsThreadServiceCallback Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5f1fe416e158e9524bdd1caab847977a5dd21b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235456"
---
# JsThreadServiceCallback Typedef

Вызов службы потоков.  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Параметры  
 callback  
 Callback for the background work item.  
  
 callbackData  
 Аргумент данных, который необходимо передать в callback.  
  
## Комментарии  
 При вызове JsCreateRuntime хост может указать фоновую службу потоков. Если этот элемент указан, элементы фоновой работы будут переданы на хост с помощью этого вызова. Ожидается, что хост начнет немедленно выполнять фоновый рабочий элемент и возвращать true или возвращать false, а время выполнения обрабатывает рабочий элемент в потоке.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
