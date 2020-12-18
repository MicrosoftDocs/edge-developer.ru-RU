---
description: Запускает сериализованный сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.
title: JsRunSerializedScriptWithCallback Function | Документы Майкрософт
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235798"
---
# Функция JsRunSerializedScriptWithCallback

Запускает сериализованный сценарий. Предоставляет возможность отложенной загрузки источника скрипта только при необходимости.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
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
 Результат запуска сценария(если он есть). Этот параметр может иметь null.  
  
## Возвращенное значение  
 Код, если операция прошла успешно, в `JsNoError` противном случае код сбоя.  
  
## Комментарии  
  
> [!NOTE]
>  Этот API пока не доступен для приложений Магазина.  
  
 Требуется активный контекст скрипта.  
  
 Время работы будет удерживать буфер, пока не будут собраны все экземпляры функций, созданных из буфера.  Затем он будет вызывать scriptUnloadCallback, чтобы сообщить вызываемой, что ее можно безопасно освободить.  
  
## Требования  
 **Заглавная:** jsrt.h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)
