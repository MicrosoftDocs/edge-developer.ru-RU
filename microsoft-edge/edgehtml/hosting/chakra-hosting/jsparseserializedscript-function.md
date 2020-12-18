---
description: Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий.
title: JsParseSerializedScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 66ecabb9d96c3f339625f93858444f55d25fd4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235636"
---
# Функция JsParseSerializedScript

Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `script`  
 Сценарий для различета.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.  
  
 `sourceUrl`  
 Расположение, из который поступил сценарий.  
  
 `result`  
 Функция, представляющая код сценария.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Буфер не сохраняется в памяти механизмом сценариев, поэтому код должен поддерживать его в памяти до тех пор, пока он может использоваться для выполнения сценариев.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
