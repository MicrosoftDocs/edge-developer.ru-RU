---
description: Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.
title: JsInspectableToObject Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235686"
---
# Функция JsInspectableToObject

Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Параметры  
 `inspectable`  
 A `IInspectable` для проецируемых проектов.  
  
 `value`  
 Значение JavaScript, которое является проекцией `IInspectable` .  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Проецируемые значения могут использоваться сценарием для вызова объекта WinRT. Ведущие точки отвечают за принудительное применение правил потоков COM.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
