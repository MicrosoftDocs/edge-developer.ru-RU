---
description: Создает объект массива с типом JavaScript.
title: JsCreateTypedArray Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62f62296d81dafe6515f69a990e33ff5c00730e1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235656"
---
# Функция JsCreateTypedArray

Создает объект массива с типом JavaScript.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `arrayType`  
 Тип создаемого массива.  
  
 `baseArray`  
 Базовый массив нового массива. Используйте, `JS_INVALID_REFERENCE` если базовый массив не используется.  
  
 `byteOffset`  
 Смещение в ветвях от начала () для `baseArray` `ArrayBuffer` массива результатов, на который требуется ссылаться. Применимо только в `baseArray` том случае, если объект `ArrayBuffer` является объектом. В противном случае должно быть 0.  
  
 `elementLength`  
 Количество элементов в массиве. Применимо только при создании нового типтного массива без `baseArray` ( `baseArray` `JS_INVALID_REFERENCE` есть) или когда `baseArray` является `ArrayBuffer` объектом. В противном случае должно быть 0.  
  
 `result`  
 Новый типный объект массива.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Это `baseArray` может быть другой `ArrayBuffer` типный массив или JavaScript. `Array` Возвращенный типный массив будет использовать массив, если он является или иным образом создает и использует копию массива `baseArray` `ArrayBuffer` исходных источников.  
  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
