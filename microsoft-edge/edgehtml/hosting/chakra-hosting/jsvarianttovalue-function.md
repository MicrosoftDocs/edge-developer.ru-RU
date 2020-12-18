---
description: Создает значение JavaScript, которое является проекцией `VARIANT` переданного.
title: JsVariantToValue Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235451"
---
# Функция JsVariantToValue

Создает значение JavaScript, которое является проекцией `VARIANT` переданного.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### Параметры  
 `variant`  
 A `VARIANT` для проецируемых проектов.  
  
 `value`  
 Значение JavaScript, которое является проекцией `VARIANT` .  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Проецируемые значения могут использоваться сценарием для вызова объекта автоматизации COM из скрипта. Ведущие точки отвечают за принудительное применение правил потоков COM.  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
