---
description: Задает для индексных свойств объекта внешние данные. Внешние данные будут использоваться в качестве заднего хранения для индексных свойств объекта и будут доступны в виде типтного массива.
title: JsSetIndexedPropertiesToExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235288"
---
# Функция JsSetIndexedPropertiesToExternalData

Задает индексные свойства объекта для внешних данных. Внешние данные будут использоваться в качестве заднего хранения для индексных свойств объекта и будут доступны в виде типтного массива.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Параметры  
 `object`  
 Объект для работы.  
  
 `data`  
 Внешние данные, используемые в качестве back store для индексных свойств объекта.  
  
 `arrayType`  
 Тип элемента массива во внешних данных.  
  
 `elementLength`  
 Количество элементов массива во внешних данных.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
