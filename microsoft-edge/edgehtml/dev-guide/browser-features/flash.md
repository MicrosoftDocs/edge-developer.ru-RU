---
description: Обеспечивает простое пользовательское интерфейс на сайтах, требующих Adobe Flash.
title: Flash — руководство для разработчиков
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, вспышка
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a81fb0808897e1763a55c3e97bc604d276a7b9f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235675"
---
# Flash  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Adobe Flash был неотъемлемой частью Интернета в течение нескольких десятков лет, предоставляя в браузерах богатый контент и анимации еще до внедрения HTML5.  В современных браузерах веб-стандарты, которые использует Корпорация Майкрософт, Adobe, Google, Apple, Mozilla и многие другие, теперь позволяют сайтам превысить эти возможности без Flash, а также повысить производительность и безопасность.  В сотрудничестве с другими поставщиками браузеров и компанией Adobe мы настоятельно рекомендуем разработчикам перейти на стандарты HTML5, включая зашифрованные расширения [мультимедиа,](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions)расширения источников [мультимедиа,](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions) [Canvas,](https://developer.microsoft.com/microsoft-edge/platform/status/canvas) [веб-звук](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi)и связь в режиме реального времени. [](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)  

С выпуском Windows 10 Microsoft Edge за октябрь 2018 г. мы [](https://theblog.adobe.com/adobe-flash-update) продолжаем работу по отзыву flash, о чем мы сообщили в рамках объявления о завершении поддержки Adobe после 2021 г. [](https://blogs.windows.com/msedgedev/2017/07/25)  В выпуске за октябрь 2018 г. пользователям потребуется явно разрешить запуск Flash на сайте на время существования вкладки.  Постоянный параметр "Всегда разрешать" больше не будет доступен, и пользователь не сможет управлять разрешением flash сайта, охватывающим сеансы вкладок.  

Переходя к стандартам HTML5, вы можете сделать несколько простых способов, чтобы ваши пользователи по-прежнему могли посетить ваш веб-сайт с помощью Microsoft Edge в Windows 10 Creators Update.  

Если на странице используется Flash, но пользователь не включил его, Microsoft Edge обычно будет показывать значок фрагмента задачи в адресной панели, как показано в [этом блоге.](https://blogs.windows.com/msedgedev/2016/12/14)  Если вы динамически добавляете элемент управления Flash после загрузки страницы, этот значок фрагмента задачи может не отображаться.  В этом случае лучше проверить наличие Flash и предоставить ссылку, как описано ниже.  

Чтобы убедиться, что все пользователи имеют хороший опыт, продолжайте тестировать наличие Flash с помощью стандартных механизмов.  Если Microsoft Edge сообщает о том, что Flash не доступен, предопортите пользователю ссылку для скачивания [Flash](http://get.adobe.com/flashplayer) и образ скачивания [Flash.](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer)  Когда пользователь щелкает ссылку, Microsoft Edge \(а также другие браузеры\) будет представлять необходимые запросы, чтобы включить Flash Player для сайта.  Ссылка должна отображаться на основном домене, где необходимо включить Flash.  Он не будет работать, если перенаправлять пользователей на страницы в других доменах.  [Вот демонстрация рекомендуемого](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun) опыта и соответствующего [примера кода.](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun)  
