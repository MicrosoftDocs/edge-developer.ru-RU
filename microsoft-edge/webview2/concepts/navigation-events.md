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
# События навигации  

Обычная последовательность событий навигации: `NavigationStarting` , , , , и затем `SourceChanged` `ContentLoading` `HistoryChanged` `NavigationCompleted` .  Следующие события описывают состояние WebView2 во время каждой навигации.  

| Последовательность | Имя события | Сведения |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 начинает навигацию и приводит к результату сетевого запроса.  Хост может отопросить запрос во время события.  |  
| 2 | `SourceChanged`  |  Источник WebView2 изменяется на новый URL-адрес.  Это событие может быть результатом навигации, которая не вызывает сетевого запроса, такого как навигация по фрагментам.  |  
| 3 | `HistoryChanged`  |  История обновлений WebView2 в результате навигации.  |  
| 4 | `ContentLoading`  |  WebView2 начинает загрузку контента для новой страницы.  |  
| 5 | `NavigationCompleted`  |  WebView2 завершает загрузку контента на новой странице.  |  

Отслеживайте `navigations` каждый новый документ с помощью ИД навигации \( `NavigationId` \).  `NavigationId`Веб-просмотр изменяется каждый раз при успешном переходе к новому документу.

:::image type="complex" source="../media/navigation-graph.png" alt-text="События навигации Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   События навигации Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> На предыдущем рисунке представлены события навигации с тем же `NavigationId` свойством в соответствующей arg события.  

 `Navigations` события с разными экземплярами `NavigationId` событий могут перекрываться.  Например, при запуске навигации необходимо дождаться связанного `NavigationStarting` события.  Если затем вы запустите другую навигацию, вы увидите событие для первого навигации, за которым следует событие для второго навигации, за которым следует событие для первой навигации, а затем все остальные соответствующие события навигации для второй `NavigationStarting` `NavigationStarting` `NavigationCompleted` навигации.  
 
 В случае ошибок может возникнуть событие или нет, в зависимости от того, продолжается ли навигация `ContentLoading` до страницы ошибки.  
 
 В случае перенаправления HTTP в строке имеется несколько событий, где у последующих аргов событий есть набор свойств, но они остаются `NavigationStarting` `IsRedirect` тем `NavigationId` же.  
 
 Тот же документ , например переход к фрагменту, не приводит к событию `navigations` `NavigationStarting` и не добавит . `NavigationId`  

Для отслеживания или отмены в подкадрах в WebView используйте события, которые действуют так же, как аналогичные события, не относя такие же, как `navigations` `FrameNavigationStarting` и другие `FrameNavigationCompleted` события.  

<!-- links -->  
