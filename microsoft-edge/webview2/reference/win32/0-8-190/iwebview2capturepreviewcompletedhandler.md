---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 0cdb6dc17549022bac6ada366f5f54dd5b9b7e12
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654957"
---
# интерфейс IWebView2CapturePreviewCompletedHandler 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.

Результат записывается в поток, указанный в вызове метода CapturePreview.

## Участников

#### Invoke 

Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.

> общедоступный [вызов](#invoke)HRESULT (результат HRESULT)
