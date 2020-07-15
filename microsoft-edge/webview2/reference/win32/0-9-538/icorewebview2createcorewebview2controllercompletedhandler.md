---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: e26d711c24758f82d42067fa28e71bc6ac1177ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877415"
---
# <span data-ttu-id="7898c-104">интерфейс ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7898c-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7898c-105">Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7898c-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="7898c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7898c-106">Summary</span></span>

 <span data-ttu-id="7898c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7898c-107">Members</span></span>                        | <span data-ttu-id="7898c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7898c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7898c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7898c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7898c-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7898c-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7898c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7898c-111">Members</span></span>

#### <span data-ttu-id="7898c-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7898c-112">Invoke</span></span> 

<span data-ttu-id="7898c-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7898c-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7898c-114">общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="7898c-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

