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
# API веб-уведомлений  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

API веб-уведомлений позволяет веб-сайтам отправлять пользователям уведомления вне контекста веб-страницы в браузере Microsoft Edge.  Примером этой функции в действии может быть приложение для обмена сообщениями, например Skype.  Когда пользователь получит новое сообщение, на его рабочем столе появится уведомление с уведомлением о сообщении.  Веб-уведомления полностью интегрированы с платформой уведомлений и центром уведомлений в Windows 10.  

## Создание уведомления  

CodePen ниже создает фик-уведомление Skype, делая объект [](https://msdn.microsoft.com/library/mt710814) [Notification](https://msdn.microsoft.com/library/mt710818) с заголовком, [](https://msdn.microsoft.com/library/mt710826)значком и [настройками параметров](https://msdn.microsoft.com/library/mt710811) тела:  

<iframe height='295' scrolling='no' title='Веб-уведомления' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. уведомления <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> веб-пера </a> от Microsoft Edge Docs ( @MicrosoftEdgeDocumentation <a href='https://codepen.io/MicrosoftEdgeDocumentation'> ) на </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

Настоятельно рекомендуется, чтобы значок **был** указан для каждого уведомления.  Это не только улучшает уведомление с точки зрения пользовательского интерфейса, но и помогает оповещать пользователей о том, откуда отправляется уведомление.  

Просмотрите видео ниже, чтобы узнать, как создать веб-уведомление, и увидеть его поведение в Windows 10!  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Свойства уведомлений  

Уведомления можно настроить со следующими свойствами:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      Текст уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      Направление текста уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      URL-адрес уведомления, используемый для значка.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [lang](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      Язык уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [permission](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      Текущее разрешение на отображение уведомления, предоставленное пользователем для текущего источника.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      Тег уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      Заголовок уведомления.  
   :::column-end:::
:::row-end:::  

### События уведомлений  

С объектом [Notification](https://developer.mozilla.org/docs/Web/API/Notification) используются следующие события:  

:::row:::
   :::column span="1":::
      [onclick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Происходит, когда пользователь щелкает уведомление.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onclose](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Происходит, когда пользователь закрывает уведомление или автоматически заносит в нее время.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onerror](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Возникает при ошибке при обработке уведомления.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [onshow](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Сгореет при отобращении уведомления.  
   :::column-end:::
:::row-end:::  

### Методы уведомлений  

С объектом [Notification](https://developer.mozilla.org/docs/Web/API/Notification) используются следующие методы:  

:::row:::
   :::column span="1":::
      [close](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Закрывает отображаемую уведомление.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Запрашивает у пользователя разрешение на отображение уведомлений по текущему источнику.  
   :::column-end:::
:::row-end:::  

## Разрешения уведомлений  

Microsoft Edge позволяет пользователям управлять разрешениями уведомлений для каждого конкретного домена веб-сайта.  Пользователь может выбрать "Да" **** или **** "Нет" при запросе домена на показ уведомлений.  Метод [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) используется для передачи сигнала о состоянии разрешений как `granted` либо , , , или `denied` `default` .  Значение указывает, что пользователь не принял решение, что `default` эквивалентно `denied` .  

## Справочник по API  

[Веб-уведомления](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Спецификация  

[Веб-уведомления](https://notifications.spec.whatwg.org)  
