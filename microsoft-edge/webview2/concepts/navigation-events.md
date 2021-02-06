---
description: Навигация
title: Навигация
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузера, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314799"
---
# <span data-ttu-id="5222a-104">События навигации</span><span class="sxs-lookup"><span data-stu-id="5222a-104">Navigation events</span></span>  

<span data-ttu-id="5222a-105">Обычная последовательность событий навигации: `NavigationStarting` , , , , и затем `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="5222a-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="5222a-106">Следующие события описывают состояние WebView2 во время каждой навигации.</span><span class="sxs-lookup"><span data-stu-id="5222a-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="5222a-107">Последовательность</span><span class="sxs-lookup"><span data-stu-id="5222a-107">Sequence</span></span> | <span data-ttu-id="5222a-108">Имя события</span><span class="sxs-lookup"><span data-stu-id="5222a-108">Event name</span></span> | <span data-ttu-id="5222a-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="5222a-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5222a-110">1</span><span class="sxs-lookup"><span data-stu-id="5222a-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="5222a-111">WebView2 начинает навигацию и приводит к результату сетевого запроса.</span><span class="sxs-lookup"><span data-stu-id="5222a-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="5222a-112">Хост может отопросить запрос во время события.</span><span class="sxs-lookup"><span data-stu-id="5222a-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="5222a-113">2</span><span class="sxs-lookup"><span data-stu-id="5222a-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="5222a-114">Источник WebView2 изменяется на новый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5222a-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="5222a-115">Это событие может быть результатом навигации, которая не вызывает сетевого запроса, такого как навигация по фрагментам.</span><span class="sxs-lookup"><span data-stu-id="5222a-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="5222a-116">3</span><span class="sxs-lookup"><span data-stu-id="5222a-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="5222a-117">История обновлений WebView2 в результате навигации.</span><span class="sxs-lookup"><span data-stu-id="5222a-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="5222a-118">4</span><span class="sxs-lookup"><span data-stu-id="5222a-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="5222a-119">WebView2 начинает загрузку контента для новой страницы.</span><span class="sxs-lookup"><span data-stu-id="5222a-119">WebView2 starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="5222a-120">5</span><span class="sxs-lookup"><span data-stu-id="5222a-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="5222a-121">WebView2 завершает загрузку контента на новой странице.</span><span class="sxs-lookup"><span data-stu-id="5222a-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="5222a-122">Отслеживайте `navigations` каждый новый документ с помощью ИД навигации \( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="5222a-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="5222a-123">`NavigationId`Веб-просмотр изменяется каждый раз при успешном переходе к новому документу.</span><span class="sxs-lookup"><span data-stu-id="5222a-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="События навигации Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="5222a-125">События навигации Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="5222a-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="5222a-126">На предыдущем рисунке представлены события навигации с тем же `NavigationId` свойством в соответствующей arg события.</span><span class="sxs-lookup"><span data-stu-id="5222a-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="5222a-127">события с разными экземплярами `NavigationId` событий могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="5222a-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="5222a-128">Например, при запуске навигации необходимо дождаться связанного `NavigationStarting` события.</span><span class="sxs-lookup"><span data-stu-id="5222a-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="5222a-129">Если затем вы запустите другую навигацию, вы увидите событие для первого навигации, за которым следует событие для второго навигации, за которым следует событие для первой навигации, а затем все остальные соответствующие события навигации для второй `NavigationStarting` `NavigationStarting` `NavigationCompleted` навигации.</span><span class="sxs-lookup"><span data-stu-id="5222a-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="5222a-130">В случае ошибок может возникнуть событие или нет, в зависимости от того, продолжается ли навигация `ContentLoading` до страницы ошибки.</span><span class="sxs-lookup"><span data-stu-id="5222a-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="5222a-131">В случае перенаправления HTTP в строке имеется несколько событий, где у последующих аргов событий есть набор свойств, но они остаются `NavigationStarting` `IsRedirect` тем `NavigationId` же.</span><span class="sxs-lookup"><span data-stu-id="5222a-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="5222a-132">Тот же документ , например переход к фрагменту, не приводит к событию `navigations` `NavigationStarting` и не добавит . `NavigationId`</span><span class="sxs-lookup"><span data-stu-id="5222a-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="5222a-133">Для отслеживания или отмены в подкадрах в WebView используйте события, которые действуют так же, как аналогичные события, не относя такие же, как `navigations` `FrameNavigationStarting` и другие `FrameNavigationCompleted` события.</span><span class="sxs-lookup"><span data-stu-id="5222a-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
