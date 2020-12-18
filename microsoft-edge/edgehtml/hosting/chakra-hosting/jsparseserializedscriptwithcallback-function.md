---
description: Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.
title: JsParseSerializedScriptWithCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235630"
---
# Функция JsParseSerializedScriptWithCallback

Проансирует сериализованный сценарий и возвращает функцию, представляющую сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### Параметры  
 `scriptLoadCallback`  
 Callback called when the source code of the script needs to be loaded.  
  
 `scriptUnloadCallback`  
 Callback called when the serialized script and source code are no longer needed.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Файл cookie, определяющий сценарий, который может использоваться контекстами сценариев с отладимой отладки.     Этот контекст передается в scriptLoadCallback и scriptUnloadCallback.  
  
 `sourceUrl`  
 Расположение, из который поступил сценарий.  
  
 `result`  
 Функция, представляющая код сценария.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в противном `JsNoError` случае код сбоя.  
  
## Комментарии  
  
> [!NOTE]
>  Этот API пока не доступен для приложений Магазина.  
  
 Требуется активный контекст скрипта.  
  
 Время работы будет удерживать буфер, пока не будут собраны все экземпляры функций, созданных из буфера.  Затем он будет вызывать scriptUnloadCallback, чтобы сообщить вызываемой, что ее можно безопасно освободить.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
