---
description: Извлекает внешние данные индексных свойств объекта.
title: JsGetIndexedPropertiesExternalData Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235134"
---
# Функция JsGetIndexedPropertiesExternalData

Извлекает внешние данные индексных свойств объекта.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### Параметры  
 `object`  
 Объект.  
  
 `data`  
 Хранилище внешних данных для индексных свойств объекта.  
  
 `arrayType`  
 Тип элемента массива во внешних данных.  
  
 `elementLength`  
 Количество элементов массива во внешних данных.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
