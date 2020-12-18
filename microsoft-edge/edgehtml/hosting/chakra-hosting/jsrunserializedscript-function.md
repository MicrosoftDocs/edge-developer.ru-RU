---
description: Запускает сериализованный сценарий.
title: JsRunSerializedScript Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46f293d76bf0944c1cdedae917735c505798f4ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235799"
---
# Функция JsRunSerializedScript

Запускает сериализованный сценарий.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `script`  
 Исходный код сериализованного сценария.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.  
  
 `sourceUrl`  
 Расположение, из который поступил сценарий.  
  
 `result`  
 Результат запуска сценария(если он есть). Этот параметр может иметь null.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Буфер не сохраняется в памяти механизмом сценариев, поэтому код должен поддерживать его в памяти до тех пор, пока он может использоваться для выполнения сценариев.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
