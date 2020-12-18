---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Узнайте, как можно использовать API веб-уведомлений, чтобы веб-сайты могли отправлять уведомления пользователям за пределы контекста браузера Microsoft Edge.
title: API веб-уведомлений — руководство разработчика
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2be201a790c6fca1526c8b6eb13e4203e8e53206
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235598"
---
# <span data-ttu-id="7d96c-104">API веб-уведомлений</span><span class="sxs-lookup"><span data-stu-id="7d96c-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="7d96c-105">API веб-уведомлений позволяет веб-сайтам отправлять пользователям уведомления вне контекста веб-страницы в браузере Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d96c-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="7d96c-106">Примером этой функции в действии может быть приложение для обмена сообщениями, например Skype.</span><span class="sxs-lookup"><span data-stu-id="7d96c-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="7d96c-107">Когда пользователь получит новое сообщение, на его рабочем столе появится уведомление с уведомлением о сообщении.</span><span class="sxs-lookup"><span data-stu-id="7d96c-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="7d96c-108">Веб-уведомления полностью интегрированы с платформой уведомлений и центром уведомлений в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7d96c-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="7d96c-109">Создание уведомления</span><span class="sxs-lookup"><span data-stu-id="7d96c-109">Creating a notification</span></span>  

<span data-ttu-id="7d96c-110">CodePen ниже создает фик-уведомление Skype, делая объект [](https://msdn.microsoft.com/library/mt710814) [Notification](https://msdn.microsoft.com/library/mt710818) с заголовком, [](https://msdn.microsoft.com/library/mt710826)значком и [настройками параметров](https://msdn.microsoft.com/library/mt710811) тела:</span><span class="sxs-lookup"><span data-stu-id="7d96c-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="7d96c-111">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="7d96c-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="7d96c-112">См. уведомления <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> веб-пера </a> от Microsoft Edge Docs ( @MicrosoftEdgeDocumentation <a href='https://codepen.io/MicrosoftEdgeDocumentation'> ) на </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="7d96c-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="7d96c-113">Настоятельно рекомендуется, чтобы значок **был** указан для каждого уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="7d96c-114">Это не только улучшает уведомление с точки зрения пользовательского интерфейса, но и помогает оповещать пользователей о том, откуда отправляется уведомление.</span><span class="sxs-lookup"><span data-stu-id="7d96c-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="7d96c-115">Просмотрите видео ниже, чтобы узнать, как создать веб-уведомление, и увидеть его поведение в Windows 10!</span><span class="sxs-lookup"><span data-stu-id="7d96c-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="7d96c-116">Свойства уведомлений</span><span class="sxs-lookup"><span data-stu-id="7d96c-116">Notification properties</span></span>  

<span data-ttu-id="7d96c-117">Уведомления можно настроить со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="7d96c-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-118">body</span><span class="sxs-lookup"><span data-stu-id="7d96c-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-119">Текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-120">dir</span><span class="sxs-lookup"><span data-stu-id="7d96c-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-121">Направление текста уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-122">icon</span><span class="sxs-lookup"><span data-stu-id="7d96c-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-123">URL-адрес уведомления, используемый для значка.</span><span class="sxs-lookup"><span data-stu-id="7d96c-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-124">lang</span><span class="sxs-lookup"><span data-stu-id="7d96c-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-125">Язык уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-126">permission</span><span class="sxs-lookup"><span data-stu-id="7d96c-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-127">Текущее разрешение на отображение уведомления, предоставленное пользователем для текущего источника.</span><span class="sxs-lookup"><span data-stu-id="7d96c-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-128">tag</span><span class="sxs-lookup"><span data-stu-id="7d96c-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-129">Тег уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-130">title</span><span class="sxs-lookup"><span data-stu-id="7d96c-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-131">Заголовок уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="7d96c-132">События уведомлений</span><span class="sxs-lookup"><span data-stu-id="7d96c-132">Notification events</span></span>  

<span data-ttu-id="7d96c-133">С объектом [Notification](https://developer.mozilla.org/docs/Web/API/Notification) используются следующие события:</span><span class="sxs-lookup"><span data-stu-id="7d96c-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-134">onclick</span><span class="sxs-lookup"><span data-stu-id="7d96c-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-135">Происходит, когда пользователь щелкает уведомление.</span><span class="sxs-lookup"><span data-stu-id="7d96c-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-136">onclose</span><span class="sxs-lookup"><span data-stu-id="7d96c-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-137">Происходит, когда пользователь закрывает уведомление или автоматически заносит в нее время.</span><span class="sxs-lookup"><span data-stu-id="7d96c-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-138">onerror</span><span class="sxs-lookup"><span data-stu-id="7d96c-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-139">Возникает при ошибке при обработке уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-140">onshow</span><span class="sxs-lookup"><span data-stu-id="7d96c-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-141">Сгореет при отобращении уведомления.</span><span class="sxs-lookup"><span data-stu-id="7d96c-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="7d96c-142">Методы уведомлений</span><span class="sxs-lookup"><span data-stu-id="7d96c-142">Notification methods</span></span>  

<span data-ttu-id="7d96c-143">С объектом [Notification](https://developer.mozilla.org/docs/Web/API/Notification) используются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="7d96c-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-144">close</span><span class="sxs-lookup"><span data-stu-id="7d96c-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-145">Закрывает отображаемую уведомление.</span><span class="sxs-lookup"><span data-stu-id="7d96c-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="7d96c-146">requestPermission</span><span class="sxs-lookup"><span data-stu-id="7d96c-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7d96c-147">Запрашивает у пользователя разрешение на отображение уведомлений по текущему источнику.</span><span class="sxs-lookup"><span data-stu-id="7d96c-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="7d96c-148">Разрешения уведомлений</span><span class="sxs-lookup"><span data-stu-id="7d96c-148">Notification permissions</span></span>  

<span data-ttu-id="7d96c-149">Microsoft Edge позволяет пользователям управлять разрешениями уведомлений для каждого конкретного домена веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="7d96c-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="7d96c-150">Пользователь может выбрать "Да" \*\*\*\* или \*\*\*\* "Нет" при запросе домена на показ уведомлений.</span><span class="sxs-lookup"><span data-stu-id="7d96c-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="7d96c-151">Метод [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) используется для передачи сигнала о состоянии разрешений как `granted` либо , , , или `denied` `default` .</span><span class="sxs-lookup"><span data-stu-id="7d96c-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="7d96c-152">Значение указывает, что пользователь не принял решение, что `default` эквивалентно `denied` .</span><span class="sxs-lookup"><span data-stu-id="7d96c-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="7d96c-153">Справочник по API</span><span class="sxs-lookup"><span data-stu-id="7d96c-153">API reference</span></span>  

[<span data-ttu-id="7d96c-154">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="7d96c-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="7d96c-155">Спецификация</span><span class="sxs-lookup"><span data-stu-id="7d96c-155">Specification</span></span>  

[<span data-ttu-id="7d96c-156">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="7d96c-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  
