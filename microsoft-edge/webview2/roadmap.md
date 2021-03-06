---
description: Узнайте, что будет дальше для WebView2
title: Дорожная карта для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398415"
---
# <a name="microsoft-edge-webview2-roadmap"></a><span data-ttu-id="6e3a2-104">Дорожная карта Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="6e3a2-104">Microsoft Edge WebView2 roadmap</span></span>  

> [!NOTE]
> <span data-ttu-id="6e3a2-105">Последнее обновление: ноябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-105">Last Updated:  November 2020</span></span>  

<span data-ttu-id="6e3a2-106">Управление WebView2 позволяет разработчикам встраить веб-технологии в свои собственные приложения.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-106">The WebView2 control allows developers to embed web technologies in their native applications.</span></span>  <span data-ttu-id="6e3a2-107">На следующей странице описывается перспективная дорожная карта для WebView2.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-107">The following page outlines the prospective roadmap for WebView2.</span></span>  

> [!NOTE]
> <span data-ttu-id="6e3a2-108">WebView2 находится в активной разработке, и дорожная карта продолжает развиваться с учетом изменений рынка и отзывов клиентов, поэтому обратите внимание, что описанные здесь планы не являются исчерпывающими и подлежат изменениям.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-108">WebView2 is under active development and the roadmap continues to evolve based on market changes and customer feedback, so please note that the plans outlined here are not exhaustive and are subject to change.</span></span>  

<span data-ttu-id="6e3a2-109">Если у вас есть проблемы или вопросы о дорожной карте, предоподавайте свои отзывы в [репо обратной связи.][GithubMicrosoftedgeWebviewfeedbackMain]</span><span class="sxs-lookup"><span data-stu-id="6e3a2-109">If you have concerns or questions about the Roadmap, provide your feedback in the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain].</span></span>  

<span data-ttu-id="6e3a2-110">Команда WebView2 планирует следующие основные усилия для будущих обновлений.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-110">The WebView2 team is planning the following major efforts for future updates.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="6e3a2-111">Установщик времени работы WebView2</span><span class="sxs-lookup"><span data-stu-id="6e3a2-111">WebView2 Runtime Installer</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6e3a2-112">Q4 2020</span><span class="sxs-lookup"><span data-stu-id="6e3a2-112">Q4 2020</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="6e3a2-113">Фиксированная версия</span><span class="sxs-lookup"><span data-stu-id="6e3a2-113">Fixed Version</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6e3a2-114">Q4 2020</span><span class="sxs-lookup"><span data-stu-id="6e3a2-114">Q4 2020</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="6e3a2-115">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="6e3a2-115">General Availability</span></span>  
   :::column-end:::
   :::column span="2":::
      *   <span data-ttu-id="6e3a2-116">Win32 C/C++ \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="6e3a2-116">Win32 C/C++ \(Q4 2020\)</span></span>  
      *   <span data-ttu-id="6e3a2-117">.NET \(Q4 2020\)</span><span class="sxs-lookup"><span data-stu-id="6e3a2-117">.NET \(Q4 2020\)</span></span>  
      *   [<span data-ttu-id="6e3a2-118">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="6e3a2-118">WinUI 3.0</span></span>][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a><span data-ttu-id="6e3a2-119">Время запуска и установки WebView2</span><span class="sxs-lookup"><span data-stu-id="6e3a2-119">WebView2 Runtime and Installer</span></span>  

<span data-ttu-id="6e3a2-120">[Модель распространения Evergreen][ConceptDistributionEvergreenModel] позволяет нацелить или установить на компьютер пользователя время запуска WebView2.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-120">[Evergreen distribution model][ConceptDistributionEvergreenModel] allows you to target or chain install the WebView2 Runtime onto your user's machine.</span></span>  <span data-ttu-id="6e3a2-121">Время запуска и установки Evergreen WebView2 достигло общего уровня доступности \(GA\).</span><span class="sxs-lookup"><span data-stu-id="6e3a2-121">The Evergreen WebView2 Runtime and installer has reached General Availability \(GA\).</span></span>  

## <a name="fixed-version"></a><span data-ttu-id="6e3a2-122">Исправленная версия</span><span class="sxs-lookup"><span data-stu-id="6e3a2-122">Fixed version</span></span>  

<span data-ttu-id="6e3a2-123">[Модель распространения фиксированной][ConceptsDistributionFixedVersionModel] версии позволяет упаковывать двухфайли Microsoft Edge внутри вашего родного приложения.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-123">[Fixed version distribution model][ConceptsDistributionFixedVersionModel] allows you to package the Microsoft Edge binaries inside your native application.</span></span>  <span data-ttu-id="6e3a2-124">Исправленная версия достигла общей доступности \(GA\).</span><span class="sxs-lookup"><span data-stu-id="6e3a2-124">The Fixed Version has reached General Availability \(GA\).</span></span>  

## <a name="general-availability"></a><span data-ttu-id="6e3a2-125">Общая доступность</span><span class="sxs-lookup"><span data-stu-id="6e3a2-125">General availability</span></span>  

### <a name="win32-cc"></a><span data-ttu-id="6e3a2-126">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="6e3a2-126">Win32 C/C++</span></span>  

<span data-ttu-id="6e3a2-127">SDK Win32 C/C++ достиг ga.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-127">The Win32 C/C++ SDK has reached GA.</span></span>  

### <a name="net"></a><span data-ttu-id="6e3a2-128">.NET</span><span class="sxs-lookup"><span data-stu-id="6e3a2-128">.NET</span></span>  

<span data-ttu-id="6e3a2-129">SDK .NET достиг ga.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-129">The .NET SDK has reached GA.</span></span> 

### <a name="winui-30"></a><span data-ttu-id="6e3a2-130">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="6e3a2-130">WinUI 3.0</span></span>  

<span data-ttu-id="6e3a2-131">Вы можете получить доступ к WebView2 в приложениях UWP с помощью [win UI 3.0,][UwpToolkitsWinui3Index]в настоящее время в альфа-версии.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-131">You can access WebView2 in your UWP applications using [Win UI 3.0][UwpToolkitsWinui3Index], currently in alpha.</span></span>  <span data-ttu-id="6e3a2-132">Дополнительные сведения о том, как быть в курсе, перейдите к дорожной карте [библиотеки пользовательского интерфейса Windows.][GithubMicrosoftUiXamlRoadmap]</span><span class="sxs-lookup"><span data-stu-id="6e3a2-132">For more information about keeping up to date, navigate to [Windows UI Library Roadmap][GithubMicrosoftUiXamlRoadmap].</span></span>  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Модель распространения Evergreen — распространение приложений с помощью webView2 | Документы Майкрософт"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Модель распространения фиксированной версии — распространение приложений с помощью webView2 | Документы Майкрософт"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3.0 Preview 1 (май 2020 г.) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Отзывы веб-просмотров — MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Дорожная карта библиотеки пользовательского интерфейса Windows — microsoft/microsoft-ui-xaml | GitHub"  
