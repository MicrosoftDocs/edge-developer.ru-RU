---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f3002c6e7941cea1f632e1df4ee42a8f38a468b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655003"
---
# интерфейс ICoreWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Аргументы события для события WebMessageReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Source](#get_source) | Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.
[get_WebMessageAsJson](#get_webmessageasjson) | Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

## Участников

#### get_Source 

Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.

> общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR * Source)

#### get_WebMessageAsJson 

Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.

> общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Используйте этот способ для обмена данными с помощью объектов JavaScript.

Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

> общедоступные значения HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR * webMessageAsString)

Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG. Используйте этот способ для обмена сообщениями через простые строки.

Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```
