---
description: Сериализует сценарий с разбиение на буфер, чем можно использовать повторно.
title: JsSerializeScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235812"
---
# Функция JsSerializeScript

Сериализует сценарий с разбиение на буфер, чем можно использовать повторно.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Параметры  
 `script`  
 Сценарий сериализации.  
  
 `buffer`  
 Буфер, в который необходимо поместить сериализованный сценарий. Может иметь null.  
  
 `bufferSize`  
 При вводе размер буфера вбайтах; При выходе размер буфера (в битах), необходимый для удержания сериализованного сценария.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.  
  
## Комментарии  
 `JsSerializeScript` Разблокирует сценарий, а затем сохраняет его форму в независимом от времени работы формате. Сериализованный сценарий затем можно десериализировать в любой время работы без необходимости повторного различета сценария.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
