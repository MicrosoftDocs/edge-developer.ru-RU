---
description: Получает хранилище памяти, используемого ArrayBuffer.
title: JsGetArrayBufferStorage Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235429"
---
# Функция JsGetArrayBufferStorage

Получает используемую хранилище `ArrayBuffer` памяти.  
  
## Синтаксис  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Параметры  
 `arrayBuffer`  
 Экземпляр ArrayBuffer.  
  
 `buffer`  
 Буфер ArrayBuffer. Время жизни возвращаемого буфера такое же, как и время существования `ArrayBuffer` буфера. Указатель буфера не считается ссылкой на сборку `ArrayBuffer` мусора.  
  
 `bufferLength`  
 Количествобайтов в буфере.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
