---
description: Получает хранилище памяти, используемого типтным массивом.
title: JsGetTypedArrayStorage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235166"
---
# Функция JsGetTypedArrayStorage

Получает хранилище памяти, используемого типтным массивом.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Параметры  
 `typedArray`  
 Типный экземпляр массива.  
  
 `buffer`  
 Буфер массива. Время жизни возвращаемого буфера такое же, как и время жизни массива. Указатель буфера не считается ссылкой на массив для сборки мусора.  
  
 `bufferLength`  
 Количествобайтов в буфере.  
  
 `arrayType`  
 Тип массива.  
  
 `elementSize`  
 Размер элемента массива.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
