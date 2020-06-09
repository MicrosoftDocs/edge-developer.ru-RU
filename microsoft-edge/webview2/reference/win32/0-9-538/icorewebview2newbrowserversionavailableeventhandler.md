---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c8444741480ba3b07d2755dcac0ec11f7194a783
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699288"
---
# <span data-ttu-id="b2c4e-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="b2c4e-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="b2c4e-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="b2c4e-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="b2c4e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b2c4e-106">Summary</span></span>

 <span data-ttu-id="b2c4e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b2c4e-107">Members</span></span>                        | <span data-ttu-id="b2c4e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b2c4e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2c4e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b2c4e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b2c4e-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b2c4e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b2c4e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="b2c4e-111">Members</span></span>

#### <span data-ttu-id="b2c4e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b2c4e-112">Invoke</span></span> 

<span data-ttu-id="b2c4e-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b2c4e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b2c4e-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b2c4e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

