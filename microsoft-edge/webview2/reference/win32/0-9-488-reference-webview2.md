---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d7e38f25a3e58d21744c8631319f553f2b0962fb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654972"
---
# <span data-ttu-id="8041d-104">Справочные материалы (WebView2)</span><span class="sxs-lookup"><span data-stu-id="8041d-104">Reference (WebView2)</span></span>  

<span data-ttu-id="8041d-105">Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) в качестве обработчика визуализации.</span><span class="sxs-lookup"><span data-stu-id="8041d-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="8041d-106">Дополнительные сведения можно найти в [статье Обзор Microsoft Edge WebView2](../../index.md)) и [Приступая к работе с WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="8041d-106">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="8041d-107">[ICoreWebView2](0-9-488/ICoreWebView2.md) — это удобное место для изучения данных API.</span><span class="sxs-lookup"><span data-stu-id="8041d-107">[ICoreWebView2](0-9-488/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="8041d-108">Глобальные</span><span class="sxs-lookup"><span data-stu-id="8041d-108">Globals</span></span>  

*   [<span data-ttu-id="8041d-109">Глобальные</span><span class="sxs-lookup"><span data-stu-id="8041d-109">Globals</span></span>](0-9-430/webview2-idl.md)  

## <span data-ttu-id="8041d-110">Приклад</span><span class="sxs-lookup"><span data-stu-id="8041d-110">Interfaces</span></span>  
*   [<span data-ttu-id="8041d-111">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8041d-111">ICoreWebView2</span></span>](0-9-488/icorewebview2.md)
*   [<span data-ttu-id="8041d-112">ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="8041d-112">ICoreWebView2Controller</span></span>](0-9-488/icorewebview2controller.md)
*   [<span data-ttu-id="8041d-113">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="8041d-113">ICoreWebView2Deferral</span></span>](0-9-488/icorewebview2deferral.md)
*   [<span data-ttu-id="8041d-114">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="8041d-114">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="8041d-115">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="8041d-115">ICoreWebView2Environment</span></span>](0-9-488/icorewebview2environment.md)
*   [<span data-ttu-id="8041d-116">ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="8041d-116">ICoreWebView2EnvironmentOptions</span></span>](0-9-488/icorewebview2environmentoptions.md)
*   [<span data-ttu-id="8041d-117">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="8041d-117">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-488/icorewebview2httpheaderscollectioniterator.md)
*   [<span data-ttu-id="8041d-118">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="8041d-118">ICoreWebView2HttpRequestHeaders</span></span>](0-9-488/icorewebview2httprequestheaders.md)
*   [<span data-ttu-id="8041d-119">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8041d-119">ICoreWebView2HttpResponseHeaders</span></span>](0-9-488/icorewebview2httpresponseheaders.md)
*   [<span data-ttu-id="8041d-120">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="8041d-120">ICoreWebView2Settings</span></span>](0-9-488/icorewebview2settings.md)
*   [<span data-ttu-id="8041d-121">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="8041d-121">ICoreWebView2WebResourceRequest</span></span>](0-9-488/icorewebview2webresourcerequest.md)
*   [<span data-ttu-id="8041d-122">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="8041d-122">ICoreWebView2WebResourceResponse</span></span>](0-9-488/icorewebview2webresourceresponse.md)

### <span data-ttu-id="8041d-123">Аргументы события</span><span class="sxs-lookup"><span data-stu-id="8041d-123">Event arguments</span></span>

*   [<span data-ttu-id="8041d-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-488/icorewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="8041d-125">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-125">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-488/icorewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="8041d-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="8041d-127">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-127">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-488/icorewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="8041d-128">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-128">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-488/icorewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="8041d-129">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-129">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-488/icorewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="8041d-130">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-130">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-488/icorewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="8041d-131">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-131">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-488/icorewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="8041d-132">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-132">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-488/icorewebview2processfailedeventargs.md)
*   [<span data-ttu-id="8041d-133">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-133">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-488/icorewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="8041d-134">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-134">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-488/icorewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="8041d-135">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-135">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-488/icorewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="8041d-136">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8041d-136">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-488/icorewebview2webresourcerequestedeventargs.md)

### <span data-ttu-id="8041d-137">Делегаты</span><span class="sxs-lookup"><span data-stu-id="8041d-137">Delegates</span></span>

*   [<span data-ttu-id="8041d-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-488/icorewebview2acceleratorkeypressedeventhandler.md)
*   [<span data-ttu-id="8041d-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-488/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [<span data-ttu-id="8041d-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-488/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [<span data-ttu-id="8041d-141">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-141">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-488/icorewebview2capturepreviewcompletedhandler.md)
*   [<span data-ttu-id="8041d-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-488/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [<span data-ttu-id="8041d-143">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-143">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-488/icorewebview2contentloadingeventhandler.md)
*   [<span data-ttu-id="8041d-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span>](0-9-488/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [<span data-ttu-id="8041d-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-488/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [<span data-ttu-id="8041d-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [<span data-ttu-id="8041d-147">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-147">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-488/icorewebview2documenttitlechangedeventhandler.md)
*   [<span data-ttu-id="8041d-148">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-148">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-488/icorewebview2executescriptcompletedhandler.md)
*   [<span data-ttu-id="8041d-149">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-149">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-488/icorewebview2focuschangedeventhandler.md)
*   [<span data-ttu-id="8041d-150">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-150">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-488/icorewebview2historychangedeventhandler.md)
*   [<span data-ttu-id="8041d-151">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-151">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-488/icorewebview2movefocusrequestedeventhandler.md)
*   [<span data-ttu-id="8041d-152">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-152">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-488/icorewebview2navigationcompletedeventhandler.md)
*   [<span data-ttu-id="8041d-153">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-153">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-488/icorewebview2navigationstartingeventhandler.md)
*   [<span data-ttu-id="8041d-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-488/icorewebview2newbrowserversionavailableeventhandler.md)
*   [<span data-ttu-id="8041d-155">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-155">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-488/icorewebview2newwindowrequestedeventhandler.md)
*   [<span data-ttu-id="8041d-156">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-156">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-488/icorewebview2permissionrequestedeventhandler.md)
*   [<span data-ttu-id="8041d-157">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-157">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-488/icorewebview2processfailedeventhandler.md)
*   [<span data-ttu-id="8041d-158">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-158">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-488/icorewebview2scriptdialogopeningeventhandler.md)
*   [<span data-ttu-id="8041d-159">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-159">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-488/icorewebview2sourcechangedeventhandler.md)
*   [<span data-ttu-id="8041d-160">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-160">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-488/icorewebview2webmessagereceivedeventhandler.md)
*   [<span data-ttu-id="8041d-161">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-161">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-488/icorewebview2webresourcerequestedeventhandler.md)
*   [<span data-ttu-id="8041d-162">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-162">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-488/icorewebview2windowcloserequestedeventhandler.md)
*   [<span data-ttu-id="8041d-163">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-163">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-488/icorewebview2zoomfactorchangedeventhandler.md)

### <span data-ttu-id="8041d-164">Проб</span><span class="sxs-lookup"><span data-stu-id="8041d-164">Experimental</span></span>

*   [<span data-ttu-id="8041d-165">ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="8041d-165">ICoreWebView2ExperimentalCompositionController</span></span>](0-9-488/icorewebview2experimentalcompositioncontroller.md)
*   [<span data-ttu-id="8041d-166">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-166">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span>](0-9-488/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [<span data-ttu-id="8041d-167">ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8041d-167">ICoreWebView2ExperimentalCursorChangedEventHandler</span></span>](0-9-488/icorewebview2experimentalcursorchangedeventhandler.md)
*   [<span data-ttu-id="8041d-168">ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="8041d-168">ICoreWebView2ExperimentalEnvironment</span></span>](0-9-488/icorewebview2experimentalenvironment.md)
*   [<span data-ttu-id="8041d-169">ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="8041d-169">ICoreWebView2ExperimentalPointerInfo</span></span>](0-9-488/icorewebview2experimentalpointerinfo.md)
