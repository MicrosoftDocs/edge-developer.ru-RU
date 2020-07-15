---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880124"
---
# интерфейс ICoreWebView2Deferral 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Выполнено](#complete) | Завершает связанное отложенное событие.

## Участников

#### Выполнено 

Завершает связанное отложенное событие.

> общедоступное значение HRESULT [Complete](#complete)()

"Завершить" следует вызывать только один раз для каждого периода отсрочки.

