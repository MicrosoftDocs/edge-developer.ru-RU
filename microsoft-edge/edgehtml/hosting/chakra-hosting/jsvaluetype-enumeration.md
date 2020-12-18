---
description: Тип JavaScript JsValueRef.
title: JsValueType Enumeration | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235452"
---
# Перечисление JsValueType

Тип JavaScript JsValueRef.  
  
## Синтаксис  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## Members  
  
### Значения  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsUndefined`|Значением является `undefined` значение.|  
|`JsNull`|Значением является `null` значение.|  
|`JsNumber`|Это значение является числом JavaScript.|  
|`JsString`|Значением является строка JavaScript.|  
|`JsBoolean`|Значением является значение JavaScript Boolean.|  
|`JsObject`|Значением является значение объекта JavaScript.|  
|`JsFunction`|Значением является значение объекта функции JavaScript.|  
|`JsError`|Значением является значение объекта ошибки JavaScript.|  
|`JsArray`|Значением является значение объекта массива JavaScript.|  
|`JsSymbol`|Значением является значение символа JavaScript.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsArrayBuffer`|Значением является значение объекта `ArrayBuffer` JavaScript.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsTypedArray`|Это значение является значением объекта массива JavaScript, введите его.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
|`JsDataView`|Значением является значение объекта `DataView` JavaScript.<br /><br /> Это значение поддерживается только в режиме Microsoft Edge.|  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
