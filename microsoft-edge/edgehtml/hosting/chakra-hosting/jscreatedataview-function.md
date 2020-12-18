---
description: Создает объект `DataView` Javascript.
title: JsCreateDataView Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1d6d170d53f3bfaf885713b6f3abca0b066f8c1d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235300"
---
# Функция JsCreateDataView

Создает объект `DataView` Javascript.  
  
## Синтаксис  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `arrayBuffer`  
 Существующий `ArrayBuffer` объект, который будет использовать в качестве хранилища для объекта `DataView` результата.  
  
 `byteOffset`  
 Смещение в вайтах от начала результата `arrayBuffer` `DataView` для ссылки.  
  
 `byteLength`  
 Количество в массиве ArrayBuffer, на которые ссылается DataView результатов.  
  
 `result`  
 Новый объект DataView.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
 Требуется активный контекст скрипта.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
