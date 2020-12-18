---
description: Создает объект Javascript `ArrayBuffer` для доступа к внешней памяти.
title: JsCreateExternalArrayBuffer Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235693"
---
# Функция JsCreateExternalArrayBuffer

Создает объект Javascript `ArrayBuffer` для доступа к внешней памяти.
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Параметры  
 `data`  
 Указатель на внешнюю память.  
  
 `byteLength`  
 Количество ветвей во внешней памяти.  
  
 `finalizeCallback`  
 Callback for when the object is finalized. Может иметь null.  
  
 `callbackState`  
 Пользовательское состояние, которое будет передано обратно в finalizeCallback.  
  
 `result`  
 Новый `ArrayBuffer` объект.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
