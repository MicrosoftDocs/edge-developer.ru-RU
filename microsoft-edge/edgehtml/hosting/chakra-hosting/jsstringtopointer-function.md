---
description: Извлекает указатель строки строки.
title: JsStringToPointer Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 77b8e16be41d8b5541129b50fa200b947f566342
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235458"
---
# Функция JsStringToPointer

Извлекает указатель строки строки.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Параметры  
 `value`  
 Строка, преобразуемая в указатель строки.  
  
 `stringValue`  
 Указатель строки.  
  
 `stringLength`  
 Длина строки.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Эта функция извлекает строку указателя строки. Он не будет `JsErrorInvalidArgument` работать, если тип значения не является строкой. Время жизни возвращаемой строки будет таким же, как и время жизни значения, из него поступило, однако указатель строки не считается ссылкой на значение (и поэтому не позволит его собрать).  
  
 Требуется активный контекст скрипта.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
