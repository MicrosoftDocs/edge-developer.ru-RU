---
description: В этом руководстве представлен обзор основ и средств PWA для создания прогрессивного веб-приложения (Chromium) в Windows.
title: Начало работы с progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: progressive web apps, PWA, Edge, Windows, PWABuilder, web manifest, service worker, push
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231225"
---
# Начало работы с progressive Web Apps (Chromium)  

Прогрессивное веб-приложения \(PWAs\) — это веб-приложения, [которые постепенно улучшаются.][WikiProgressiveEnhancement]  К последовательным усовершенствованиям относятся такие функции, как установка, поддержка в автономном режиме и push-уведомления.  Вы также можете упаковать PWA для магазинов приложений.  Возможные магазины приложений включают Microsoft Store, Google Play, Магазин приложений Mac и другие.  Microsoft Store — это коммерческий магазин приложений, встроенный в Windows 10.  

В следующем руководстве приводится обзор основ PWA путем создания простого веб-приложения и расширения его в качестве PWA.  Готовый проект работает в современных браузерах.  

> [!TIP]
> Вы можете использовать [PWABuilder][PwaBuilder] для создания нового PWA, улучшения существующей PWA или упаковки PWA для магазинов приложений.  

## Предварительные условия  

*   Используйте [Visual Studio code для][VisualstudioCodeMain] редактирования кода PWA.  
*   Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.  
    
## Создание базового веб-приложения  

Чтобы создать пустое веб-приложение, следуйте шагам в [node Express App Generator][ExpressjsApplicationGenerator]и придайте приложению `MySamplePwa` имя.  

В командной подсказке запустите следующие команды.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Команды создают пустое веб-приложение и устанавливают зависимости.  

Теперь у вас есть простое функциональное веб-приложение.  Чтобы запустить веб-приложение, запустите следующую команду.  

```shell
npm start
```  

Теперь `http://localhost:3000` перейдите, чтобы просмотреть новое веб-приложение.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
   Запуск нового PWA на localhost
:::image-end:::

## Начало создания PWA  

Теперь, когда у вас есть простое веб-приложение, расширьте его как PWA, добавив три требования для PWAS<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [HTTPS,](#step-1---use-https)манифест [веб-приложения](#step-2---create-a-web-app-manifest)и [рабочий работник службы.](#step-3---add-a-service-worker)  

### Шаг 1. Использование ПРОТОКОЛА HTTPS  

Ключевые части платформы PWA, такие как [сотрудники][MDNServiceWorkerApi]служб, требуют использования ПРОТОКОЛА HTTPS.  Когда веб-сайт PWA будет работать, его необходимо опубликовать на URL-адресе HTTPS.  

В целях отладки Microsoft Edge также разрешает использовать `http://localhost` API PWA.  

[Опубликуйте веб-приложение в качестве][VisualStudioNodejsTutorialPublishAzureAppService]веб-сайта, но убедитесь, что сервер настроен для HTTPS.  Например, вы можете создать бесплатную учетную [запись Azure.][AzureCreateFreeAccount]  Разойдите сайт в [службу приложений Microsoft Azure,][AzureWebApps] и он по умолчанию обслуживается по протоколу HTTPS.  

В следующем руководстве используется `http://localhost` для создания PWA.  

### Шаг 2. Создание манифеста веб-приложения  

Манифест [Веб-приложения][MDNWebAppManifest] — это JSON-файл, содержащий метаданные о вашем приложении, такие как имя, описание, значки и другие.  

Добавление манифеста приложения в веб-приложение:  

1.  В Visual Studio code выберите **папку "Открыть**файл" и выберите созданный  >  **** `MySamplePwa` ранее каталог.  
1.  Выберите, `Ctrl` + `N` чтобы создать новый файл, и в paste в следующем фрагменте кода.  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  Сохраните файл как `/MySamplePwa/public/manifest.json` .  
1.  Добавьте изображение значка приложения 512x512 с именем `icon512.png` `/MySamplePwa/public/images` .  Пример изображения можно [использовать в][ImagePwa] целях тестирования.  
1.  В Visual Studio Code откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### Шаг 3. Добавление сотрудника службы  

Сотрудники службы — это ключевая технология, обеспечивающая такие сценарии, как поддержка в автономном режиме, расширенный кэш и выполнение фоновых задач, которые ранее были ограничены основными приложениями.  

Сотрудники службы — это фоновые задачи, которые перехватывают сетевые запросы из веб-приложения.  Сотрудники служб пытаются выполнить задачи, даже если PWA не запущен.  К задачам относятся следующие действия.  

*   Обслуживание запрашиваемых ресурсов из кэша  
*   Отправка push-уведомлений  
*   Выполнение фоновых задач получения  
*   Плохое значки  
*   и другие  
    
Сотрудники служб определяются в специальном файле JavaScript.  Для получения дополнительных сведений перейдите к использованию API ["Сотрудники службы"][MDNUsingServiceWorkers] [и "Рабочие службы".][MDNServiceWorkerApi]  

Чтобы создать в проекте рабочий **** работник службы, используйте рабочий рецепт сетевой службы из кэша из [построщика PWA.][PwaBuilderServiceWorker]  

1.  Перейдите [pwabuilder.com/serviceworker,][PwaBuilderServiceWorker] **выберите** рабочий процесс сетевой службы с первым кэшом и кнопку **"Скачать".**  Загруженный файл содержит следующие файлы:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Скопируйте загруженные файлы в `public` папку проекта веб-приложения.  
1.  В Visual Studio Code откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Теперь в вашем веб-приложении есть сотрудник службы, использующий стратегию с первого кэша.  Новый рабочий процесс службы сначала получает ресурсы из кэша и только из сети при необходимости.  К кэшным ресурсам относятся изображения, JavaScript, CSS и HTML.

Чтобы подтвердить, что ваш рабочий работник работает, с помощью следующих действий.  

1.  Перейдите к веб-приложению с помощью `http://localhost:3000` .  Если веб-приложение не доступно, запустите следующую команду.   
    
    ```shell
    npm start
    ```
    
1.  В Microsoft Edge `F12` выберите, чтобы открыть Microsoft Edge DevTools.  Выберите **"Приложение",** затем **"Сотрудники служб",** чтобы просмотреть сотрудников службы.  Если рабочий работник службы не отображается, обновите страницу.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Обзор рабочих сотрудников службы Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       Обзор рабочих сотрудников службы Microsoft Edge DevTools
    :::image-end:::
    
1.  Просмотреть кэш рабочих **** служб, расширив хранилище кэша и выбрав **pwabuilder-precache.**  Должны отображаться все ресурсы, кэшные рабочим работником службы.  Ресурсы, кэшментные сотрудником службы, включают значок приложения, манифест приложения, CSS-файлы и файлы JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Кэш рабочих служб в Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Кэш рабочих служб в Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Попробуйте PWA в качестве автономного приложения.  В Microsoft Edge DevTools \( \) выберите "Сеть", а затем измените состояние `F12` **"Online"** на **"Автономный".** ****  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Настройка автономного режима приложения в Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Настройка автономного режима приложения в Microsoft Edge DevTools
    :::image-end:::
    
1.  Обновите приложение, и оно должно отобразить автономный механизм обслуживания ресурсов приложения из кэша.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск PWA в автономном режиме" lightbox="./media/vs-nodejs-express-index.png":::
       Запуск PWA в автономном режиме
    :::image-end:::
    
## Добавление push-уведомлений в PWA  

Вы можете создать PWAS, которые поддерживают push-уведомления, выполв следующие задачи.  

1.  Подписка на службу обмена сообщениями с помощью [API Push][MDNPushApi]  
1.  Отображение всплывающее сообщение при получении сообщения от службы с помощью [API уведомлений][MDNNotificationsApi]  
    
Как и в службах, API push-уведомлений являются основанными на стандартах API.  API push-уведомлений работают в браузерах, поэтому ваш код должен работать везде, где поддерживаются PWAs.  Дополнительные сведения о доставке push-сообщений в различные браузеры на сервере можно найти в [Web-Push.][NPMWebPush]  

Следующие действия были адаптированы из книги "Push Rich Demo in [Service WorkerBook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет ряд других полезных рецептов для рабочих рабочих служб и веб-push-служб.  

### Шаг 1. Создание ключей VAPID  

Для push-уведомлений требуются ключи VAPID \(Voluntary Application Server Identification\) для отправки push-сообщений клиенту PWA.  В Сети доступно несколько генераторов ключей VAPID (например, [vapidkeys.com][VapidkeysMain]\).  После генерации вы должны получить объект JSON, содержащий открытый и закрытый ключ.  Сохраните ключи для последующих действий в следующем руководстве.  For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].  

### Шаг 2. Подписка на push-уведомления  

Сотрудники служб обрабатывают события push-уведомлений и взаимодействия всплывающих уведомлений в PWA.  Чтобы подписать PWA на push-уведомления сервера, убедитесь, что выполнены следующие условия.  

*   Веб-приложение PWA установлено, активно и зарегистрировано  
*   Код для выполнения задачи подписки находится в основном потоке пользовательского интерфейса PWA  
*   У вас есть сетевое подключение  
    
Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.  В этом случае браузер запросит разрешение у пользователя.  Если разрешение отказано, запрос на отклонение запроса `registration.pushManager.subscribe` , который должен быть `DOMException` обработан.  Для получения дополнительных информации об управлении разрешениями перейдите к [push-уведомлениям в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]  

В `pwabuilder-sw-register.js` файле примените следующий фрагмент кода.  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
                });
            });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Дополнительные сведения можно найти в [PushManager][MDNPushManager] и [Web-Push.][NPMWebPushUsage]  

### Шаг 3. Прослушивание push-уведомлений  

После создания подписки в PWA добавьте обработчики в рабочий процесс службы для реагирования на события push-рассылки.  Событие Push отправляется с сервера для отображения всплывающих уведомлений.  Всплывающие уведомления отображают данные о полученном сообщении.  Для выполнения следующих задач необходимо добавить обработок щелчка.  

*   Отклонение всплывающее уведомление  
*   Открывать, фокусировать или открывать и фокусировать любые открытые окна  
*   Открытие и фокус в новом окне для отображения клиентской страницы PWA  
    
Добавьте `pwabuilder-sw.js` в файл следующие обработчики.  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Шаг 4. Попробуйте  

Чтобы протестировать push-уведомления для PWA, выполните следующие действия.  

1.  Перейдите к PWA `http://localhost:3000` по  Когда ваш сотрудник службы активируется и пытается подписать PWA на push-уведомления, Microsoft Edge вы запросит разрешение PWA показывать уведомления.  Выберите **"Разрешить".**  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Диалоговое окно разрешений для включения уведомлений" lightbox="./media/notification-permission.png":::
       Диалоговое окно разрешений для включения уведомлений
    :::image-end:::
    
1.  Имитация push-уведомлений на стороне сервера.  Открыв PWA в браузере, выберите открытие `http://localhost:3000` `F12` DevTools.  Выберите **push-уведомления**для сотрудников службы приложений, чтобы  >  ****  >  **** отправить тестовую push-уведомления в PWA.  
    
    :::row:::
       :::column span="":::
          Push-уведомление должно отображаться рядом с панелью задач.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push-уведомление от DevTools" lightbox="./media/devtools-push.png":::
             Push-уведомление от DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Если не выбрать всплывающее уведомление (или активировать\), система автоматически отключит его через несколько секунд и включит его в очередь в центре уведомлений Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Уведомления в Центре уведомлений Windows" lightbox="./media/windows-action-center.png":::
             Уведомления в Центре уведомлений Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## Дальнейшие действия  

Следующие действия включают дополнительные задачи, которые помогут вам понять создание реальных pwAs.  

*   Управление push-подписками и их хранение  
*   [Шифрование][NPMWebPushEncrypt] данных полезной нагрузки  
*   Адаптивный дизайн  
*   Глубокое связывание  
*   [Тестирование в разных браузерах][BrowserStackTestEdgeBrowser]  
*   Реализация методик проверки и тестирования, таких как [webhint][Webhint]  
    
## См. также  

*   [Прогрессивное веб-приложение в веб-документы MDN][MDNProgressiveWebApps]  
*   [Прогрессивное веб-приложение на веб-сайте web.dev][WebDevProgressiveWebApps]  
*   [Читатели новостей Хакера как прогрессивное веб-приложение][HackerNewsProgressiveWebApps] — сравнивают различные структуры и шаблоны производительности для реализации примера \(Читателя новостей хакера\) PWA.  
*   [Захиминг (PwAs)][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Прогрессивное движение для прогрессивного веб-приложения][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Автономные POS-карты с прогрессивной веб-приложениями][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [Вопросы и&PWA][AaronGustafsonNotebookPwaQa]  
*   [Подавка в Интернете][JoretegBlogBettingWeb]  
*   [Именовка прогрессивного веб-приложения][Fberriman20170626NamingProgressiveWebApps]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание Node.js в Azure с помощью Visual Studio кода | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "Вопросы и&PWA"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивное движение для прогрессивного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Захиминг PWAs — новый выпуск Edge Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Генератор экспресс-приложений | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Именовка прогрессивного веб-приложения"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивного веб-приложения"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Подавка в Интернете"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивное веб-приложение \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование сотрудников служб | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные POS-карты с прогрессивной веб-приложениями"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений WebPush с помощью службы push-уведомлений Mozilla | Службы Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивное веб-приложение"  

[PwaBuilder]: https://www.pwabuilder.com "Построитель PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Построитель PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorkerBook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)"  

[VapidkeysMain]: https://vapidkeys.com "Безопасный генератор ключей VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивное веб-приложение | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивное улучшение | Википедия"  
