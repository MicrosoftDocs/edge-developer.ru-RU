---
title: Использование сотрудников служб для управления сетевыми запросами и push-уведомлениями
description: Сотрудники служб — это веб-работники, которые помогают повысить производительность, реагировать на различные сетевые условия и повысить подключение к вашему веб-приложению.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399136"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a>Использование сотрудников служб для управления сетевыми запросами и push-уведомлениями

Сотрудники службы — это особый тип веб-работника, который может перехватывать, изменять и отвечать на все сетевые запросы с помощью `Fetch` API.  Сотрудники службы могут получать доступ к API и асинхронным хранилищам клиентских `Cache` данных, например, для `IndexedDB` хранения ресурсов.  

## <a name="registering-a-service-worker"></a>Регистрация сотрудника службы  

Как и другие веб-работники, сотрудники службы должны существовать в отдельном файле. Вы ссылались на этот файл при регистрации сотрудника службы, как показано в следующем фрагменте кода.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Современные браузеры предоставляют различные уровни поддержки для сотрудников службы. Поэтому перед запуском любого кода, связанного с работником службы, необходимо проверить наличие `serviceWorker` объекта. В этом фрагменте кода сотрудник службы регистрируется с помощью файла, расположенного `serviceworker.min.js` в корне сайта. Убедитесь, что файл JavaScript, который определяет сотрудника службы, существует в каталоге самого высокого уровня, который необходимо управлять \(который называется областью рабочего службы\).  В предыдущем фрагменте кода файл хранится в корне, и работник службы управляет всеми страницами в домене. Если файл Service Worker хранится в каталоге, областью сотрудника службы будет каталог и все `js` `js` подтеки.  В качестве наилучшей практики поместите файл Service Worker в корне вашего сайта, если не потребуется уменьшить область действия сотрудника службы.  

## <a name="the-service-worker-lifecycle"></a>Жизненный цикл сотрудника службы  

Жизненный цикл сотрудника службы состоит из нескольких этапов, каждый шаг вызывает событие. Вы можете добавить слушателей в эти события, чтобы запустить код для выполнения действия. В следующем списке представлено представление жизненного цикла и связанных с ними событий сотрудников служб. 

1.  Регистрация сотрудника службы.  
1.  Браузер загружает файл JavaScript, устанавливает сотрудника службы и запускает `install` событие. Вы можете использовать событие для предварительного кэша любых важных и долгоживучивых файлов, таких как CSS-файлы, файлы JavaScript, изображения логотипа, автономные страницы и так далее с вашего `install` веб-сайта.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  Активируется сотрудник службы, который запускает `activate` событие.  Используйте это событие для очистки устаревших кэшей.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  Работник службы готов к запуску при обновлении страницы или при переходе пользователя на новую страницу на сайте. Если вы хотите запустить сотрудника службы, не дожидаясь, используйте `self.skipWaiting()` метод во время `install` события.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  В настоящее время работает рабочий службы.     
    
## <a name="using-fetch-in-service-workers"></a>Использование fetch в service Workers  

Главное событие, которое вы используете в service Worker— `fetch` это событие.  Событие выполняется каждый раз, когда браузер пытается получить доступ к содержимому в `fetch` области сотрудника службы. В следующем фрагменте кода показано, как добавить слушателя в событие fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

В обработнике вы можете контролировать, передается ли запрос в сеть, извлекает ли он из `fetch` кэша и так далее.  Подход, который вы принимаете, зависит от типа запрашиваемого ресурса, его частого обновления и другой бизнес-логики, уникальной для вашего приложения.  Вот несколько примеров того, что вы можете сделать:  

*   Если доступно, верните ответ из кэша, в противном случае откат запросив ресурс по сети.  
*   Извлекаем ресурс из сети, кэшируйте копию и возвращая ответ.
*   Разрешить пользователю указать предпочтение для сохранения данных. 
*   Поставляем изображение-местоодатель для определенных запросов изображения.  
*   Создание ответа непосредственно в работнике службы.  
    
## <a name="push-notifications"></a>Push-уведомления  

Сотрудники службы могут нажимать уведомления пользователям. Push-уведомления помогают пользователям повторно взаимодействовать с вашим приложением после некоторого времени. Дополнительные сведения перейдите к погонам Push Notifications и [демонстрации.][AzurewebsitesWebpushdemo]  

## <a name="see-also"></a>См. также  

Чтобы узнать больше о работниках службы, перейдите к следующему списку связанных тем.  

*   [Обеспечение автономной работы PWAs с сотрудниками службы][MDNPwasMakingOfflineServiceWorkers]  
*   [Как сделать PWAs повторно задействованными с помощью Уведомлений и Push][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Веб-push-уведомления |  Демонстрации Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Обеспечение автономной работы PWAs с сотрудниками службы — pwAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Как сделать PWAs повторно задействованными с помощью Уведомлений и Push - PWAs | MDN"  
