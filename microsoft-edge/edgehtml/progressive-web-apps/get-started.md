---
description: В этом руководстве представлен обзор основ и средств PWA для создания последовательных веб-приложений в Windows.
title: Начало работы с последовательными веб-приложениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: progressive web apps, PWA, Edge, Windows, PWABuilder, web manifest, service worker, push
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235124"
---
# Начало работы с последовательными веб-приложениями  

Последовательные веб-приложения \(PWAs\) — [][WikiProgressiveEnhancement] это просто веб-приложения, которые постепенно улучшаются с помощью машинных функций, похожих на приложения, на вспомогательных платформах и браузерных системах, таких как установка с домашнего экрана, поддержка в автономном режиме и push-уведомления.  В Windows 10 с обдвижком Microsoft Edge \(EdgeHTML\) pwAs пользуются дополнительным преимуществом работы независимо от окна браузера в качестве приложений универсальной [платформы Windows.][WindowsUwpGetStartedWhat]  

В этом руководстве приводится обзор основ PWA путем создания простого веб-приложения в качестве PWA с помощью Microsoft Visual Studio и некоторых программах `localhost` построитель PWA.  Готовый продукт работает аналогично в любом браузере, который поддерживает PWAs.  

> [!TIP]
> Чтобы быстро преобразовать существующий сайт в PWA и упаковить его для Windows 10 и других платформ приложений, просмотрите [построитель PWA.][PwaBuilder]  

## Предварительные условия  

Вы можете создавать PWAS с помощью любой IDE веб-разработки.  Ниже приводится только обязательное условие для этого руководства, которое поможет вам в поддержке инструментов PWA в экосистеме разработчиков Windows.  

*   Скачайте файл \(free\) [Visual Studio Community 2017.][VisualStudioDownloads]  Вы также можете использовать выпуски Professional, Enterprise или [Preview.][VisualStudioPreview]  В установщике Visual Studio выберите следующие рабочие нагрузки.  
    
    *   **Разработка универсальной платформы Windows**  
    *   **Node.js разработки**  

## Настройка базового веб-приложения  

Для простоты используйте шаблон приложения Visual Studio [Node.js Express][VisualStudioNodeJsTutorial] для создания веб-приложения, которое обслуживает `localhost` `index.html` страницу.  Представьте себе это в качестве заметика для привлекательных полноразмерных веб-приложений, которые вы разрабатываете как PWA.  

1.  Запустите Visual Studio и запустите новый проект.  
    *   **Файл**  >  **Новый**  >  **Project...**  
    *   `Ctrl`+`Shift`+`N`  
1.  В **javaScript**выберите **basic Node.js Express 4 Application**.  За выберите имя и расположение и выберите **"ОК".**  
    
    ![Выбор шаблона Node.js express 4 в Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  После загрузки нового проекта выберите **build** \( `Ctrl` + `Shift` + `B` \) и **Start Debugging** \( `F5` \).  Убедитесь, `index.html` что файл загружается при `http://localhost:1337` просмотре.  
    
    ![Запуск нового сайта на localhost][ImageVsNodejsExpressIndex]  

## Как превратить приложение в PWA  

Теперь настало время примедить основные требования [PWA][PwaEdgehtmlIndexRequirements] для вашего веб-приложения: манифест *веб-приложения,* *HTTPS* и *службы.*  

### Манифест веб-приложения  

Манифест [веб-приложения][MDNWebAppManifest] — это файл метаданных JSON, описывающий ваше приложение, включая имя, автора, URL-адрес страницы записи и один или несколько значков.  Так как она основана на стандартной схеме, необходимо предоставить только один манифест [веб-приложения][W3cWebAppManifest]для PWA, устанавливаемого на любой платформе, ОС и комбинации устройств, поддерживаюшей PWAs.  В экосистеме Windows манифест веб-приложения сообщает веб-индекселю Bing, что ваш PWA является кандидатом на автоматическое включение в [Microsoft Store,][PwaEdgehtmlMicrosoftStore]где он может достигать почти 700 миллионов активных ежемесячных пользователей в качестве приложения для Windows 10.  

Если это был существующий веб-сайт, можно создать манифест веб-приложения с помощью [построитель PWA.][PwaBuilder]  Так как это еще неопубликованный проект, скопируйте пример манифеста.  

1.  В обозревателе Visual Studio *щелкните*правой кнопкой мыши обную папку и выберите "Добавить новый ** ****  >  **файл...",** указав имя `manifest.json` элемента.  
1.  `manifest.json`Скопируйте в файл следующий код.  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    В реальном PWA следующим шагом является настройка имени *,* *start_url*, *short_name*, *описание*и *значки* \(значки описаны на следующем шаге\).  
    
    Дополнительные данные о различных значениях членов и связанных с ними целях см. в справочнике по [манифесту Web App.][MDNWebAppManifest]  
    
1.  Затем заполните пустой массив фактическими путями изображений с помощью генератора изображений `icons` приложения построитель PWA.  
    
    1.  С помощью веб-браузера скачайте этот пример изображения [PWA 512x512.][ImagePwa]  
    1.  Перейдите в генератор изображений приложения построитель [PWA][PwaBuilderAppImageGenerator]и выберите изображение, которое вы только что сохранили в качестве входного изображения, а затем `pwa.png` нажать кнопку **"Скачать".** ****  
    1.  **Откройте** и **извлеките** ZIP-файл.  
    1.  В обозревателе Visual Studio щелкните правой кнопкой мыши папку и откройте папку `public` **в проводнике.**  Создайте **папку с именем** `images` ..  
    1.  Скопируйте все папки платформы \( , , , и т. д.\) из извлеченного ZIP-файла в папку и закройте `android` `chrome` окно `windows10` `images` проводника.  Добавьте папки в проект Visual Studio \(в обозревателе решений щелкните правой кнопкой мыши папку и выберите "Добавить существующую папку..." для каждой `images` ****  >  **** папки\).  
    1.  Откройте \(с Visual Studio или любым редактором\) файл из извлеченного ZIP-файла и скопируйте массив в файл `icons.json` `"icons": [...]` `manifest.json` проекта.  

1.  Теперь необходимо связать манифест веб-приложения с приложением.  Откройте файл \(в папке\) для редактирования и добавьте эту строку сразу после ссылки `layout.pug` `views` на таблицу стилей.  \(Это просто ярлык шаблона ["Уайл"][PugAttributes] узла `<link rel='manifest' href='/manifest.json'>` для \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Теперь ваше веб-приложение обслуживает манифест и значки приложений, готовых к домашнему экрану!  Попробуйте запускать приложение \( `F5` \) и загружать манифест.  

![Загрузка манифеста веб-приложения с localhost][ImageVsNodejsExpressManifest]  

И один из ваших значков.  

![Загрузка логотипа приложения Square71x71Logo с localhost][ImageVsNodejsExpressIcon]  

Если вы публикуете приложение в режиме реального времени \(с фактическим \), поисковая система Bing определяет его в качестве кандидата для автоматической упаковки и отправки в Microsoft Store как устанавливаемое приложение `start_url` для Windows [][PwaEdgehtmlMicrosoftStore] 10.  Убедитесь, что manifest.jsфайл содержит сигналы качества для [последовательных веб-приложений,][WindowsBlogsPwaEdge] для которых Bing проверяется, включая следующие элементы.   

*   `name`  
*   `description`  
*   По крайней мере один значок квадрата размером 512 пкс или больше (чтобы обеспечить источник изображения достаточного разрешения для автоматического создания экрана-заставки вашего приложения, описание в магазине, изображение плитки и т. п.).  

Кроме того, используйте [ПРОТОКОЛ HTTPS,](#https) [сотрудников служб](#service-workers)и соблюдайте политики [Microsoft Store.][LegalWindowsAgrementsMicrosoftStorePolicies]  

### HTTPS  

[][MDNServiceWorkerApi] Сотрудники служб и другие ключевые технологии PWA, которые работают с сотрудниками [][MDNSyncManager] служб \(например, [][MDNCache]API кэша, [][MDNPushApi]push-файлов и фоновой синхронизации\), работают только через безопасные подключения, то есть [HTTPS][WikiHttps] для рабочих сайтов или в целях `localhost` отладки.  

Если вы [публикуете это][VisualStudioNodejsTutorialPublishAzureAppService] веб-приложение как веб-сайт \(например, путем настройки бесплатной учетной записи [Azure][AzureCreateFreeAccount]\), необходимо убедиться, что сервер настроен для HTTPS.  Если для узла сайта используется [служба приложений Microsoft Azure,][AzureWebApps] она по умолчанию обслуживается по протоколу HTTPS.  

В этом руководстве по-прежнему используется в качестве замещего для `http://localhost` обслуживаемого веб-сайта. `https://`  

### Служебные сценарии  

Service Workers is the key technology behind PWAs. Сотрудники служб выступают в качестве прокси-сервера между PWA и сетью, чтобы ваш веб-сайт функционировал как установленное нативное приложение, которое обслуживает автономные сценарии, реагирует на push-уведомления сервера и выполняет фоновые задачи.  Кроме того, сотрудники служб открывают новые стратегии производительности.  Вам не требуется реализовать полное веб-приложение для использования кэша рабочих служб для точной настройки производительности загрузки страницы для веб-сайта.  

Сотрудники службы — это фоновые потоки на основе событий, которые запускаются из файлов JavaScript, обслуживаемого вместе с обычными сценариями, которые используют ваше веб-приложение.  Поскольку рабочие процессы не работают в основном потоке пользовательского интерфейса, [][MDNWorkerPrototypePostMessage] у сотрудников [][MDNDedicatedWorkerGlobalScopePostMessage] служб нет доступа к DOM, хотя поток пользовательского интерфейса и рабочий поток могут взаимодействовать с помощью обработчиков событий и обработчиков `postMessage()` `onmessage` событий.  

Вы связываете сотрудника службы с приложением, регистрируете его в источнике URL-адреса сайта \(или указанном пути в нем\).  После регистрации рабочий файл службы загружается, устанавливается и активируется на компьютере пользователя.  Для получения дополнительной информации в веб-документы [][MDNUsingServiceWorkers] MDN есть полное руководство по использованию рабочих работников и подробная справка [по API рабочих][MDNServiceWorkerApi] служб.  

В этом руководстве используйте рабочий сценарий службы автономной страницы в [ПОСТРОИТЕЛЕ PWA.][PwaBuilderServiceWorker]  Начните с настройки скрипта с дополнительными функциональными возможностями в соответствии с требованиями к производительности, пропускной способности сети и так далее.  Просмотрите [руководство по работе с рабочими службами,][ServiceWorkerCookbook]  предоставленное Mozilla, чтобы просмотреть ряд полезных идей о кэшинге рабочих служб.  

1.  Откройте и выберите рабочий сотрудник службы автономной страницы [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] \(default\) и нажмите кнопку "Загрузить **рабочий файл службы".** ****  
1.  Откройте папку скачивания и скопируйте два следующих файла  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Сохраните файлы в `public` папку проекта Visual Studio веб-приложения.  \(Из Visual Studio откройте проводник в проекте и перейдите `Ctrl` + `O` в `public` папку\).  
    
    В обозревателе решений откройте `public/pwabuilder-sw.js` файл и измените значение на `offlineFallbackPage` `offline.html` .  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    Стоит инициировать код в обоих этих файлах, чтобы узнать, как зарегистрировать сотрудника службы, который кэширует назначенную страницу \( \) и обслуживает ее, когда происходит сбой сетевого `offline.html` получения.  Затем создайте простую страницу в качестве замещего для `offline.html` автономной функциональности приложения.  
    
1.  В обозревателе решений откройте файл и добавьте `views/layout.pug` следующую строку под тегами ссылок.  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    Сайт загружает и запускает скрипт регистрации рабочих служб.  
    
1.  В обозревателе решений щелкните папку правой кнопкой мыши и `public` выберите **"Добавить**  >  **новый файл"...**  `offline.html`Назовем его и добавьте содержимое и некоторые части `<title>` тела, например следующий код.  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    На этом этапе ваша `public` папка должна иметь три новых файла.  
    
    ![Файлы, добавленные в обную папку решения][ImageVsNodejsExpressPublic]  
    
1.  В обозревателе решений откройте файл и добавьте следующий код перед последней `routes\index.js` командой \( `module.exports = router;` \).  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Это предписывает приложению обслуживать файл \(когда сотрудник службы извлекает его для `offline.html` автономного кэша\).  
    
1.  Протестировать PWA!  Создайте \( `Ctrl` + `Shift` + `B` \) и запустите `F5` \( ваше веб-приложение, чтобы запустить Microsoft Edge и открыть `localhost` страницу.  Затем выполните следующие действия.  
    
    1.  Откройте консоль Edge DevTools **** \( \) и `Ctrl` + `Shift` + `J` убедитесь, что сотрудник службы зарегистрирован.  
    1.  На панели **отладки** разйдите к окне управления **"Service Workers" (Рабочие** службы) и щелкните свой источник.  В **обзоре рабочих служб**убедитесь, что ваш рабочий работник активирован и запущен.  
        
        ![Обзор рабочего сотрудника службы Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  Раз развернуть **кэш-контроль** и `offline.html` убедиться, что страница кэшироваться.  
        
        ![Кэш рабочего кэша службы Edge DevTools][ImageDevtoolsSwCache]  
        
1.  Время попробовать PWA в качестве автономного приложения!  В Visual Studio остановите **отладку** \( \) вашего веб-приложения, а затем откройте `Shift` + `F5` Microsoft Edge \(или обновить\) на адрес localhost вашего веб-сайта.  Теперь она должна загрузить страницу \(благодаря рабочим службам и автономному `offline.html` кэше\)!  
    
    ![offline.html из http://localhost:1337 загруженного в Microsoft Edge][ImageOfflineHtml]  

## Добавление push-уведомлений  

Сделайте PWA более похожим на приложение, добавив поддержку push-уведомлений на стороне клиента с помощью [Push API][MDNPushApi] для подписки на службу обмена сообщениями и [API][MDNNotificationsApi] уведомлений для отображения всплывающее сообщение при получении сообщения.  Как и для сотрудников служб, это основанные на стандартах API, работающие в разных браузерах, поэтому вам нужно написать код только один раз, чтобы он работал везде, где поддерживаются PWAs.  На стороне сервера используйте библиотеку с открытым кодом [Web-Push][NPMWebPush] для обработки различий, которые связаны с доставкой push-сообщений в различные браузеры.  

Ниже приводится адаптация из книги "Push Rich Demo in [Service WorkerBook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет смысл инициировать ряд других полезных рабочих рецептов web Push и служб.  

### Шаг 1. Установка библиотеки веб-push NPM  

В Visual Studio обозревателе решений щелкните правой кнопкой мыши проект и откройте **Node.js интерактивное окно...**  Введите в него следующий код.  

```javascript
.npm install web-push
```  

При этом будет [устанавливаться библиотека Web-Push.][NPMWebPush]  Затем откройте файл и добавьте следующую строку в верхнюю часть файла после `index.js` других требований.  

```javascript
var webpush = require('web-push');
```  

### Шаг 2. Создание ключей VAPID для сервера  

Затем необходимо создать ключи VAPID \(Voluntary Application Server Identification\) для сервера для отправки push-сообщений клиенту PWA.  Это необходимо сделать только один раз (то есть серверу требуется только одна пара ключей VAPID\).  В интерактивном Node.js введите следующий код.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

Выходные данные должны привести к объекту JSON, содержащего открытый и закрытый ключ, который копируется в логику сервера.  

В `index.js` файле перед последней строкой \( `module.exports = router` \) добавьте следующий код.  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

`publicKey`Скопируйте `privateKey` только что созданные значения и их значения.  Вы также можете настроить адрес \(хотя это не обязательно для запуска `mailto` этого примера\).  

В [блоге разработчика Mozilla Services][MozillaServicesSendingVapidWebPushNotificationsPush] есть хорошее объяснение о VAPID и WebPush, если вас интересуют подробные сведения о том, как это работает.  

### Шаг 3. Обработка запросов серверов, связанных с push-запросами  

Теперь настроим маршруты для обработки запросов, связанных с push-запросами от клиента PWA, включая обслуживание открытого ключа VAPID и регистрацию клиента для получения push-запросов.  

В реальном сценарии push-уведомление, скорее всего, происходит из события в логике сервера.  Чтобы упростить эту процедуру, необходимо добавить кнопку push-уведомлений на нашу домашную странице PWA для создания push-уведомлений с сервера и конечную точку **** `/sendNotification` \(маршрут сервера\) для обработки этих запросов.  

В файле следует добавить следующие маршруты сразу после кода инициализации VAPID, добавленного в `index.js` [шаг 2][#step-2---generate-vapid-keys-for-your-server].  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

После на месте кода на стороне сервера можно получать push-уведомления в клиенте PWA.  

### Шаг 4. Подписка на push-уведомления  

В качестве прокси-служб сети PWA сотрудники службы обрабатывают события push-уведомлений и взаимодействия всплывающих уведомлений.  Однако, как и при первой настройке \(или регистрации\) рабочего сервера службы, подписка PWA на сервер push-уведомлений происходит в основном потоке пользовательского интерфейса PWA и требует сетевого подключения.  Для подписки на push-уведомления требуется активная регистрация рабочих служб, поэтому необходимо сначала убедиться, что рабочий процесс службы установлен и активен, прежде чем пытаться подписать его на push-уведомления.  

Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.  В этом случае браузер запросит разрешение у пользователя.  Если в разрешении отказано, запрос на `registration.pushManager.subscribe` отклонение `DOMException` запроса будет отклонен, поэтому его необходимо обработать.  Подробнее об управлении разрешениями см. в [push-уведомлениях в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]  

В `pwabuilder-sw-register.js` файле в коде ниже.  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
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

Дополнительные сведения о работе API и различных связанных параметрах можно узнать в документации MDN по интерфейсу [PushManager][MDNPushManager] и документации NPM в библиотеке [Web-Push.][NPMWebPushUsage]  

### Шаг 5. Настройка обработчиков событий push-уведомлений и push-уведомлений  

После того как настроена наша push-подписка, оставшаяся часть работы будет происходить в сотруднике службы.  Сначала необходимо настроить обработок для событий push-уведомлений, отправленных сервером, и ответить всплывающим уведомлением \(если разрешение было предоставлено\) с отображением полезной нагрузки push-данных.  Далее добавляется обработок щелчка для всплывающее уведомление, чтобы отклонять уведомление и сортировать список открытых в настоящее время окон для открытия, фокуса или открытия и фокуса на нужной клиентской странице PWA.  

В `pwabuilder-sw.js` файле привяжем следующие обработчики.  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
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

### Шаг 6. Попробуйте  

Время для тестирования push-уведомлений в PWA!  

1.  Запустите \( `F5` \) PWA в браузере.  Так как вы изменили рабочий код службы \( \), необходимо открыть `pwabuilder-sw.js` devTools Debugger \( \) на панели "Обзор рабочего сотрудника службы" и отозарегистрировать рабочий сотрудник службы и перезагрузить страницу, чтобы повторно зарегистрировать ее (или щелкнуть `F12` **** **** `F5` "Обновить\"). ****  В производственном сценарии браузер регулярно проверяет наличие обновлений рабочих служб и устанавливает их в фоновом режиме.  Вы должны принудительно использовать его для немедленного результата.  
    
    По мере активации и попытки подписки PWA на push-уведомления сотрудник службы должен увидеть диалоговое окно разрешений в нижней части страницы.  
    
    ![Диалоговое окно разрешений для включения уведомлений][ImageNotificationPermission]  
    
    Выберите **"Да",** чтобы включить всплывающие уведомления для PWA.  
    
1.  В области "Общие сведения о рабочих службах" попробуйте нажать кнопку **"Push".**  Должно появиться всплывающее уведомление с жестко задаваемой кодой "Test push message from DevTools"\).  
    
    ![Push-уведомление от DevTools][ImageDevtoolsPush]  
    
1.  Затем попробуйте нажать кнопку **"Отправить уведомление"** на домашней странице PWA.  На этот раз появляется всплывающее уведомление с полезной нагрузкой с сервера.  
    
    ![Push-уведомление с сервера PWA][ImagePwaPush]  
    
    Если вы не нажмете \(или активируете\) всплывающее уведомление, оно будет отклонено через несколько секунд и в очереди в центре уведомлений Windows.  
    
    ![Уведомления в Центре уведомлений Windows][ImageWindowsActionCenter]  
    
    У вас есть основы push-уведомлений PWA.  В реальном приложении дальнейшие действия реализуются таким образом, чтобы управлять push-подписками и хранить их, а также правильно шифровать данные полезной нагрузки, отправляемые по сети. [][NPMWebPushEncrypt]  
    
## Дальнейшая работа  

В этом руководстве демонстрируется базовая структура прогрессивного веб-приложения и средств разработки Microsoft PWA, включая Visual Studio, построитель PWA и Edge DevTools.  

Конечно, существует намного больше возможностей для создания отличной [веб-части][BrowserStackTestEdgeBrowser] [PWA,][PwaEdgehtmlIndexRequirements] которая выходит за рамки того, что вы здесь читаете, включая адаптивный дизайн, глубокие связи, тестирование в нескольких браузерах и другие лучшие методики [\(не][Webhint] говоря уже о возможностях вашего приложения!\), но надеемся, что в этом руководстве вы хорошо знаете основы PWA и некоторые идеи по началу работы.  Если у вас есть дополнительные вопросы о разработке PWA с помощью Windows или Visual Studio, оставьте комментарий!  

Просмотрите другие руководства PWA, чтобы узнать, как повысить вовлеченность клиентов и обеспечить более простое, интегрированное с ОС взаимодействие с приложением.  

*   [Подекание Windows.][PwaEdgehtmlWindowsFeatures] Используя простое обнаружение функций, вы можете постепенно улучшить PWA для пользователей Windows 10 с помощью собственный API-интерфейсов windows runtime \(WinRT\), например для настройки уведомлений плитки меню "Пуск" **и** списков переходов на панели задач Windows, а также \(по разрешению\) работы с пользовательскими ресурсами, такими как фотографии, музыка и календарь.  
*   [PWAs в Microsoft Store.][PwaEdgehtmlMicrosoftStore]  Узнайте больше о преимуществах распространения магазина приложений и о том, как отправить PWA.  

## См. также  

*   [Прогрессивное веб-приложения в веб-документы MDN][MDNProgressiveWebApps] — отличное руководство по прогрессивному веб-приложениям.  
*   [Прогрессивное веб-приложения на веб-сайте web.dev][WebDevProgressiveWebApps] — отличное руководство по прогрессивному веб-приложениям.  
*   [Прогрессивное веб-приложение —][ProgressiveWebApps] демонстрация реальных примеров PWAs.  
*   [Читатели новостей Хакера как прогрессивное веб-приложение][HackerNewsProgressiveWebApps] — сравнивают различные структуры и шаблоны производительности для реализации примера \(Читателя новостей хакера\) PWA.  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Документы Майкрософт"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Progressive Web Apps \(EdgeHTML\)in the Microsoft Store | Документы Майкрософт"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Адаптировать PWA \(EdgeHTML\) для Windows | Документы Майкрософт"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Политики Microsoft Store | Документы Майкрософт"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Учебник. Создание приложения Node.js Express в Visual Studio | Документы Майкрософт"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Публикация в службе приложений Azure : создание приложения Node.js и приложения Express в Visual Studio | Документы Майкрософт"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Что такое приложение универсальной платформы Windows \(UWP\)?  | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Постепенное обновление веб-приложений в Microsoft Edge и Windows 10 | Блоги Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Загрузки | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Free Developer Software & Services | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio Preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивного веб-приложения"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope.postMessage\(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивное веб-приложение \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование сотрудников служб | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker.prototype.postMessage\(\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений WebPush с помощью службы push-уведомлений Mozilla | Службы Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивное веб-приложение"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Атрибуты | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Построитель PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Генератор изображений приложений"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Построитель PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorkerBook"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorkerBook"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Манифест веб-приложения | W3C"  

[Webhint]: https://sonarwhal.com "webhint, механизм подсказок для веб-методов" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-работников" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивное веб-приложение | web.dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Википедия"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивное улучшение | Википедия"  
