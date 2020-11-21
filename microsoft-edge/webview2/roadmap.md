---
description: Узнайте о том, что дальше в WebView2
title: План для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 99e743db0c1fb17ea46405b08e1ed074a3386068
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182362"
---
# <span data-ttu-id="7a068-104">WebView2ная схема Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7a068-104">Microsoft Edge WebView2 roadmap</span></span>  

##### <span data-ttu-id="7a068-105">Последнее обновление: Ноябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7a068-105">Last Updated: November 2020</span></span>  

<span data-ttu-id="7a068-106">Элемент управления WebView2 позволяет разработчикам внедрять веб-технологии в собственные приложения.</span><span class="sxs-lookup"><span data-stu-id="7a068-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="7a068-107">На следующей странице приведена схема перспективной схемы для WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a068-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="7a068-108">WebView2 находится в активном состоянии, а план продолжает развиваться, основываясь на изменениях рынка и отзывах пользователей, поэтому обратите внимание на то, что описанные здесь планы не являются исчерпывающими, и их может изменить.</span><span class="sxs-lookup"><span data-stu-id="7a068-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="7a068-109">Если у вас есть проблемы или вопросы по поводу плана, предоставьте отзыв в [репозитории обратной связи][GithubMicrosoftedgeWebviewfeedbackMain].</span><span class="sxs-lookup"><span data-stu-id="7a068-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="7a068-110">Для будущих обновлений группа разработчиков WebView2 планирует следующие основные усилия.</span><span class="sxs-lookup"><span data-stu-id="7a068-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="7a068-111">Установщик среды выполнения WebView2</span><span class="sxs-lookup"><span data-stu-id="7a068-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="7a068-112">4 квартал 2020</span><span class="sxs-lookup"><span data-stu-id="7a068-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="7a068-113">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="7a068-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="7a068-114">4 квартал 2020</span><span class="sxs-lookup"><span data-stu-id="7a068-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="7a068-115">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="7a068-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="7a068-116">Win32 C/C++ \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="7a068-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="7a068-117">.NET \ (Q4 2020 \)</span><span class="sxs-lookup"><span data-stu-id="7a068-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="7a068-118">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="7a068-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7a068-119">Среда выполнения и установщик WebView2</span><span class="sxs-lookup"><span data-stu-id="7a068-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="7a068-120">[Модель распространения Evergreen][ConceptDistributionEvergreenModel] позволяет целевому объекту или цепочке установить среду выполнения WebView2 на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a068-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="7a068-121">В среде выполнения и установщике Evergreen WebView2 достигнут общий доступ \ (GA \).</span><span class="sxs-lookup"><span data-stu-id="7a068-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="7a068-122">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="7a068-122">Fixed version</span></span>  

<span data-ttu-id="7a068-123">С помощью [фиксированной модели распространения версий][ConceptsDistributionFixedVersionModel] можно упаковать двоичные файлы Microsoft EDGE в собственное приложение.</span><span class="sxs-lookup"><span data-stu-id="7a068-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="7a068-124">Фиксированная версия достигла общей доступности \ (GA \).</span><span class="sxs-lookup"><span data-stu-id="7a068-124">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <span data-ttu-id="7a068-125">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="7a068-125">General availability</span></span>  

### <span data-ttu-id="7a068-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="7a068-126">Win32 C/C++</span></span>  

<span data-ttu-id="7a068-127">Пакет SDK для Win32 C/C++ достиг GA.</span><span class="sxs-lookup"><span data-stu-id="7a068-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <span data-ttu-id="7a068-128">.NET</span><span class="sxs-lookup"><span data-stu-id="7a068-128">.NET</span></span>  

<span data-ttu-id="7a068-129">.NET SDK достиг себя в течение "GA".</span><span class="sxs-lookup"><span data-stu-id="7a068-129">The .NET SDK has reached GA.</span></span> 

### <span data-ttu-id="7a068-130">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="7a068-130">WinUI 3.0</span></span>  

<span data-ttu-id="7a068-131">Вы можете получить доступ к WebView2 в приложениях UWP с помощью [Win UI 3,0][UwpToolkitsWinui3Index], в настоящее время в Alpha.</span><span class="sxs-lookup"><span data-stu-id="7a068-131">You can access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="7a068-132">Дополнительные сведения о том, как своевременно поддерживаться, можно найти в разделе [планы библиотеки пользовательского интерфейса Windows][GithubMicrosoftUiXamlRoadmap].</span><span class="sxs-lookup"><span data-stu-id="7a068-132">For more information about keeping up to date, see [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Модель распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Стандартная модель распространения версий — распространение приложений с помощью WebView2 | Документы Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3,0 Preview 1 (Май 2020) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "План библиотеки пользовательского интерфейса Windows — Microsoft/Microsoft-UI-XAML | GitHub"  
