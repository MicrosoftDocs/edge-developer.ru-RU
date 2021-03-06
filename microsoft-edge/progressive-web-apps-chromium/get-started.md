---
description: В этом руководстве представлен обзор основ и средств PWA для создания прогрессивных веб-приложений (Chromium) в Windows.
title: Начало работы с прогрессивными веб-приложениями (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, Edge, Windows, PWABuilder, веб-манифест, работник службы, push
ms.openlocfilehash: 6ff24b2e9219b2f3755bb2e8f6db137dc7a721ec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398135"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a>Начало работы с прогрессивными веб-приложениями (Chromium)  

Прогрессивные веб-приложения \(PWAs\) — это веб-приложения, которые [постепенно улучшаются.][WikiProgressiveEnhancement]  Прогрессивные усовершенствования включают такие функции, как установка, поддержка в автономном режиме и push-уведомления.  Вы также можете упаковть PWA для магазинов приложений.  Возможные магазины приложений включают магазины Microsoft Store, Google Play, Mac App Store и другие.  Microsoft Store — это коммерческий магазин приложений, встроенный в Windows 10.  

В следующем руководстве представлен обзор основ PWA, создав простое веб-приложение и расширив его как PWA.  Готовый проект работает в современных браузерах.  

> [!TIP]
> Вы можете использовать [PWABuilder][PwaBuilder] для создания новой PWA, улучшения существующего PWA или пакета PWA для магазинов приложений.  

## <a name="prerequisites"></a>Предварительные условия  

*   Используйте [Visual Studio код,][VisualstudioCodeMain] чтобы изменить исходный код PWA.  
*   Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.  
    
## <a name="create-a-basic-web-app"></a>Создание базового веб-приложения  

Чтобы создать пустое веб-приложение, выполните действия в [Node Express App Generator][ExpressjsApplicationGenerator]и назовите ваше `MySamplePwa` приложение.  

В запросе запустите следующие команды.  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

Команды создают пустое веб-приложение и устанавливают любые зависимости.  

Теперь у вас есть простое функциональное веб-приложение.  Чтобы запустить веб-приложение, запустите следующую команду.  

```shell
npm start
```  

Теперь `http://localhost:3000` просмотрите, чтобы просмотреть новое веб-приложение.  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск нового PWA на локальном сайте" lightbox="./media/vs-nodejs-express-index.png":::
   Запуск нового PWA на локальном сайте
:::image-end:::

## <a name="get-started-building-a-pwa"></a>Начало создания PWA  

Теперь, когда у вас есть простое веб-приложение, расширь его как PWA, добавив три требования к PWAs<!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]-->: [HTTPS,](#step-1---use-https) [манифест веб-приложения](#step-2---create-a-web-app-manifest)и [сотрудник службы](#step-3---add-a-service-worker).  

### <a name="step-1---use-https"></a>Шаг 1 — использование HTTPS  

Ключевые части платформы PWA, такие как [Service Workers,][MDNServiceWorkerApi]требуют использования HTTPS.  Когда PWA переходит в прямой эфир, необходимо опубликовать его на URL-адрес HTTPS.  

Для отладки Microsoft Edge также разрешает использовать `http://localhost` API PWA.  

[Опубликуйте свое веб-приложение как живой сайт,][VisualStudioNodejsTutorialPublishAzureAppService]но убедитесь, что сервер настроен для HTTPS.  Например, можно создать свободную учетную запись [Azure.][AzureCreateFreeAccount]  Хост-сайт в [Службе приложений Microsoft Azure,][AzureWebApps] и по умолчанию он обслуживается через HTTPS.  

Следующее руководство, используйте `http://localhost` для создания PWA.  

### <a name="step-2---create-a-web-app-manifest"></a>Шаг 2 . Создание манифеста веб-приложений  

Манифест [веб-приложения][MDNWebAppManifest] — это файл JSON, содержащий метаданные о вашем приложении, такие как имя, описание, значки и другие.  

Добавление манифеста приложения в веб-приложение:  

1.  В Visual Studio коде выберите **папку File**Open и выберите созданный ранее  >  **** `MySamplePwa` каталог.  
1.  Выберите, `Ctrl` + `N` чтобы создать новый файл, и ввести в следующий фрагмент кода.  
    
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
1.  Добавьте изображение значка приложения 512x512 с `icon512.png` именем `/MySamplePwa/public/images` .  Пример изображения можно [использовать для][ImagePwa] тестирования.  
1.  В Visual Studio Код откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a>Шаг 3 . Добавление сотрудника службы  

Сотрудники службы являются ключевой технологией pwAs, позволяющей использовать такие сценарии, как поддержка в автономном режиме, расширенный кэшинг и выполнение фоновых задач, ранее ограниченных для родных приложений.  

Сотрудники служб — это фоновые задачи, перехватыватели сетевых запросов из вашего веб-приложения.  Сотрудники службы пытаются выполнить задачи, даже если ваш PWA не запущен.  Задачи включают следующие действия.  

*   Обслуживание запрашиваемых ресурсов из кэша  
*   Отправка push-уведомлений  
*   Выполнение задач фонового получения  
*   Значки badging  
*   и больше  
    
Сотрудники служб определяются в специальном файле JavaScript.  Дополнительные сведения можно получить в [API Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API.][MDNServiceWorkerApi]  

Чтобы создать сотрудника службы в проекте, используйте рецепт сотрудника сетевой службы **Cache-first** от [PWA Builder.][PwaBuilderServiceWorker]  

1.  Перейдите [pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]выберите сотрудника сетевой службы **Cache-first** и выберите кнопку **Загрузка.**  Загруженный файл содержит следующие файлы:
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  Скопируйте загруженные файлы в `public` папку в проекте веб-приложения.  
1.  В Visual Studio коде откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
Теперь в вашем веб-приложении есть сотрудник службы, использующий стратегию кэш-первого.  Сначала новый сотрудник службы извлекает ресурсы из кэша и из сети только по мере необходимости.  Кэшные ресурсы включают изображения, JavaScript, CSS и HTML.

Чтобы подтвердить, что выполняется рабочий службы, используйте следующие действия.  

1.  Перейдите к веб-приложению с помощью `http://localhost:3000` .  Если ваше веб-приложение не доступно, запустите следующую команду.   
    
    ```shell
    npm start
    ```
    
1.  В Microsoft Edge выберите `F12` для открытия Microsoft Edge DevTools.  Выберите **приложение,** а затем **сотрудников службы,** чтобы просмотреть сотрудников службы.  Если сотрудник службы не отображается, обновите страницу.  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Обзор сотрудника службы Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       Обзор сотрудника службы Microsoft Edge DevTools
    :::image-end:::
    
1.  Просмотр кэша сотрудника службы путем расширения **хранилища кэша** и выбора **pwabuilder-precache.**  Все ресурсы, кэшные работником службы, должны отображаться.  Ресурсы, кэшные работником службы, включают значок приложения, манифест приложения, CSS и файлы JavaScript.  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Кэш сотрудника службы в Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       Кэш сотрудника службы в Microsoft Edge DevTools (F12)
    :::image-end:::
    
1.  Попробуйте PWA как автономное приложение.  В Microsoft Edge DevTools `F12` \( \) выберите **Сеть,** а затем измените состояние **Online** в **автономном режиме.**  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Настройка приложения в автономном режиме в Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       Настройка приложения в автономном режиме в Microsoft Edge DevTools
    :::image-end:::
    
1.  Обновите приложение и отобразите автономный механизм обслуживания ресурсов приложения из кэша.  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск PWA в автономном режиме" lightbox="./media/vs-nodejs-express-index.png":::
       Запуск PWA в автономном режиме
    :::image-end:::
    
## <a name="add-push-notifications-to-your-pwa"></a>Добавление push-уведомлений в PWA  

Вы можете создать PWAs, поддерживаюющие push-уведомления, выполняя следующие задачи.  

1.  Подписка на службу обмена сообщениями с помощью [API Push][MDNPushApi]  
1.  Отображение всплывающее сообщение при получении сообщения из службы с помощью [API уведомлений][MDNNotificationsApi]  
    
Как и у сотрудников службы, API push-уведомлений являются API на основе стандартов.  API push-уведомлений работают в браузерах, поэтому код должен работать везде, где поддерживаются PWAs.  Дополнительные сведения о доставке push-сообщений в различные браузеры на сервере перейдите в [Web-Push.][NPMWebPush]  

Следующие действия были адаптированы из книги "Push Rich Demo in [Service Worker Cookbook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет ряд других полезных рецептов веб-push и рабочих служб.  

### <a name="step-1---generate-vapid-keys"></a>Шаг 1 . Создание ключей VAPID  

Push-уведомления требуют ключей VAPID \(Добровольная идентификация сервера приложений\) для отправки push-сообщений клиенту PWA.  Существует несколько генераторов ключей VAPID, доступных в Интернете \(например, [vapidkeys.com][VapidkeysMain]\).  После генерации необходимо получить объект JSON, содержащий общедоступный и закрытый ключ.  Сохраните ключи для последующих действий в следующем учебнике.  Сведения о VAPID и WebPush перейдите к отправке [выявленных веб-уведомлений веб-приложения VAPID с помощью push-службы Mozilla.][MozillaServicesSendingVapidWebPushNotificationsPush]  

### <a name="step-2---subscribe-to-push-notifications"></a>Шаг 2 . Подписка на push-уведомления  

Сотрудники служб обрабатывают push-события и взаимодействие уведомлений в PWA.  Чтобы подписаться на PWA на push-уведомления сервера, убедитесь, что следующие условия выполнены.  

*   Ваш PWA установлен, активен и зарегистрирован  
*   Код для выполнения задачи подписки находится в основном потоке пользовательского интерфейса PWA  
*   Подключение к сети  
    
Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.  Если нет, пользователь получает запрос от браузера на разрешение.  Если разрешение отказано, запрос на `registration.pushManager.subscribe` бросок `DOMException` , который должен быть обработан.  Дополнительные информации об управлении разрешениями перейдите к [push-уведомлениям в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]  

В `pwabuilder-sw-register.js` файле задайте следующий фрагмент кода.  

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

Дополнительные сведения перейдите в [PushManager][MDNPushManager] и [Web-Push.][NPMWebPushUsage]  

### <a name="step-3---listen-for-push-notifications"></a>Шаг 3 . Прослушивание push-уведомлений  

После создания подписки в PWA добавьте обработчики для реагирования на события push-службы.  Push-событие отправляется с сервера для отображения всплывающих уведомлений.  В всплывающих уведомлениях отображаются данные для полученного сообщения.  Чтобы выполнить следующие задачи, необходимо добавить `click` обработник.  

*   Отклонение уведомления всплывающих уведомлений  
*   Откройте, сосредоточьте или откройте все открытые окна и сосредоточьте их  
*   Откройте и сосредоточьте новое окно для отображения клиентской страницы PWA  
    
В файл `pwabuilder-sw.js` добавьте следующие обработчики.  

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

### <a name="step-4---try-it-out"></a>Шаг 4 . Попробуйте его  

Чтобы протестировать push-уведомления для PWA, выполните следующие действия.  

1.  Перейдите к вашему PWA по `http://localhost:3000` .  Когда сотрудник службы активируется и пытается подписаться на PWA для push-уведомлений, Microsoft Edge подсказывает вам разрешить PWA показывать уведомления.  Выберите **Разрешить**.  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Диалоговое окно разрешений для включения уведомлений" lightbox="./media/notification-permission.png":::
       Диалоговое окно разрешений для включения уведомлений
    :::image-end:::
    
1.  Имитация push-уведомления на стороне сервера.  Чтобы открыть PWA в `http://localhost:3000` браузере, выберите `F12` для открытия DevTools.  Выберите ****  >  **push-сообщение**  >  **сотрудника службы приложений,** чтобы отправить тест-push-уведомление в службу PWA.  
    
    :::row:::
       :::column span="":::
          Push-уведомление должно отображаться рядом с панелью задач.  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push a notification from DevTools" lightbox="./media/devtools-push.png":::
             Push a notification from DevTools  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Если вы не выбираете \(или активируете\) всплывающее уведомление, система автоматически отключает его через несколько секунд и выстроит очередь в центре действий Windows.  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Уведомления в Центре действий Windows" lightbox="./media/windows-action-center.png":::
             Уведомления в Центре действий Windows :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a>Дальнейшие действия  

Следующие действия включают дополнительные задачи, которые помогут вам понять создание pwAs в реальном мире.  

*   Управление подписками push и хранение  
*   [Шифрование][NPMWebPushEncrypt] данных полезной нагрузки  
*   Адаптивный дизайн  
*   Глубокая связь  
*   [Тестирование кросс-браузера][BrowserStackTestEdgeBrowser]  
*   Реализация практик проверки и тестирования, таких как [Webhint][Webhint]  
    
## <a name="see-also"></a>См. также  

*   [Прогрессивные веб-приложения в веб-docs MDN][MDNProgressiveWebApps]  
*   [Прогрессивные веб-приложения на веб-сайте.][WebDevProgressiveWebApps]  
*   [Читатели новостей][HackerNewsProgressiveWebApps] хакеров как прогрессивные веб-приложения — сравнивает различные структуры и шаблоны производительности для реализации примера \(Hacker News reader\) PWA.  
*   [Миф Busting PWAs][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Прогрессивная дорожная карта для прогрессивного веб-приложения][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Автономные POS-карты с прогрессивными веб-приложениями][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Ставки в Интернете][JoretegBlogBettingWeb]  
*   [Наименование прогрессивных веб-приложений][Fberriman20170626NamingProgressiveWebApps]  
*   [Проектирование и создание прогрессивного веб-приложения без рамок (часть 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Проектирование и создание прогрессивного веб-приложения без рамок (часть 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Проектирование и создание прогрессивного веб-приложения без рамок (часть 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание приложения Node.js в Azure с Visual Studio кодом | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивная дорожная карта для прогрессивного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Миф Busting PWAs — новое edge edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Экспресс-генератор приложений | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Наименование прогрессивных веб-приложений"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивных веб-приложений"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Ставки в Интернете"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивные веб-приложения \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API API для сотрудников службы | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование рабочих | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные POS-карты с прогрессивными веб-приложениями"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений webPush с помощью службы push-службы Mozilla | Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "веб-push-| npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — веб-| NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — веб-| NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивные веб-приложения"  

[PwaBuilder]: https://www.pwabuilder.com "Строитель PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Работник службы | Строитель PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | Поваренная книга ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 3)"  

[VapidkeysMain]: https://vapidkeys.com "Безопасный генератор ключей VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивные веб-приложения | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивная | Википедия"  
