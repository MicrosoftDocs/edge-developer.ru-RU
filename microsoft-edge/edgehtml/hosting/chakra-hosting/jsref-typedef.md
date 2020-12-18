---
description: Ссылка на объект, который принадлежит сборщику мусора Chakra.
title: JsRef Typedef | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235128"
---
# JsRef Typedef

Ссылка на объект, который принадлежит сборщику мусора Chakra.  
  
## Синтаксис  
  
```cpp  
typedef void *JsRef;  
```  
  
## Комментарии  
 Время запуска Chakra автоматически отслеживает ссылки JsRef, если они хранятся в локальных переменных или в параметрах (например, в стеке). Для хранения JsRef в другом месте, кроме стека, необходимо вызывать JsAddRef и JsRelease для управления жизненным сроком жизни объекта, в противном случае сборщик мусора может освободить объект, пока он еще используется.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
