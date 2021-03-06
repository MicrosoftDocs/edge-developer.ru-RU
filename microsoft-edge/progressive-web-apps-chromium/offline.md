---
title: Поддержка автономного и сетевого подключения в прогрессивных веб-приложениях
description: Узнайте, как использовать вспомогательные технологии для создания устойчивых опытом для удовлетворения различных сетевых условий.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 6b6031aac10161c16195c83496f8d8b5b842628e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398079"
---
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a>Поддержка автономного и сетевого подключения в прогрессивных веб-приложениях

В течение многих лет организации неохотно вкладывали значительные средства в веб-программное обеспечение над отечественным программным обеспечением, так как веб-приложения зависят от стабильных сетевых подключений. Сегодня веб-платформа предлагает надежные параметры, которые позволяют пользователям продолжать работать, даже если сетевое подключение становится неустойчивым или полностью отключено.

## <a name="use-the-caching-to-improve-performance-of-pwas"></a>Использование кэшинга для повышения производительности pwAs

С введением [рабочих служб][MDNServiceWorker]веб-платформа добавила API для предоставления доступа к управляемым `Cache` кэшным ресурсам. Этот API на основе обещаний позволяет разработчикам хранить и извлекать многие веб-ресурсы: HTML, CSS, JavaScript, изображения, JSON и так далее. Обычно API кэша используется в контексте сотрудника службы, но он также доступен в основном потоке `window` объекта.

Одним из распространенных использований API является предварительное кэшировать критически важные ресурсы при установке сотрудника службы, как показано в следующем фрагменте `Cache` кода.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Этот код, который запускается во время события жизненного цикла сотрудника службы, открывает кэш с именем, а затем, когда он имеет указатель на кэш, добавляет в него четыре ресурса с помощью `install` `static-cache` `addAll()` метода.  Часто этот подход соеди- `fetch`   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

Фрагмент кода выполняется в service Worker всякий раз, когда браузер делает `fetch` запрос на этот сайт. В этом случае существует условное заявление, которое выполняется, если запрос для HTML-файла. Работник службы проверяет, существует ли файл уже в любом кэше \(с помощью `match()` метода\). Если запрос существует в кэше, этот кэшный результат возвращается. Если нет, для этого ресурса запускается новый ресурс, копия ответа кэшируется на более позднее время, и ответ `fetch` возвращается. Если сбой из-за недоступности сети, страница в автономном режиме возвращается `fetch` из кэша.

Это простое введение показывает, как использовать кэшинг в прогрессивном веб-приложении (PWA). Каждый PWA отличается и может использовать различные стратегии кэшинга. Ваш код может выглядеть по-другому, и вы можете использовать различные стратегии кэшинга для различных маршрутов в одном приложении.

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a>Использование IndexedDB в PWA для хранения структурированных данных

`IndexedDB` API для хранения структурированных данных. Как и API, он также асинхронен, что означает, что его можно использовать в основном потоке или с веб-рабочими, такими как `Cache` работники службы. Используйте API для хранения значительного количества структурированных данных на клиенте или двоичных данных, таких `IndexedDB` как зашифрованные объекты мультимедиа. Дополнительные сведения можно получить в [праймере MDN с помощью IndexedDB.][MDNIndexeddbApiUsing]

## <a name="understand-storage-options-for-pwas"></a>Понимание параметров хранения для PWAs

Иногда может потребоваться хранить небольшие объемы данных для улучшения автономного доступа пользователей. Если это так, вы можете найти простоту системы пары ключ-значение веб-хранилища отвечает вашим потребностям.  

> [!IMPORTANT]
> Веб-хранилище — это синхронный процесс, который не доступен для использования в рабочих потоках, таких как Service Workers. Интенсивное использование может создавать проблемы с производительностью для приложения. 


Существует 2 типа веб-хранилища: `localStorage` и `sessionStorage` . Каждый из них поддерживается как отдельный хранилище данных, изолированный для созданного домена. `sessionStorage` сохраняется только в течение сеанса просмотра (например, при открытом браузере, который включает обновление и восстановление). `localStorage` сохраняется до тех пор, пока данные не будут удалены кодом, пользователем или браузером (например, если доступно ограниченное хранилище). В следующем фрагменте кода показано, как использовать `localStorage` , который похож на `sessionStorage` используемый.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Этот фрагмент кода захватывает метаданные о текущей странице и хранит ее в объекте JavaScript. Затем он сохраняет это значение как JSON при использовании метода и назначает ключ, равный `localStorage` `setItem()` текущему `window.location` URL-адресу. Вы можете получить сведения из `localStorage` `getItem()` метода. 

В следующем фрагменте кода показано, как использовать кэширование для перечисляния кэшных страниц и извлечения метаданных для выполнения задачи, например создания списка `localstorage` ссылок.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

Метод передает URL-адрес запроса в метод для получения любых `insertOfflineLink()` `localStorage.getItem()` сохраненных метаданных. Полученные данные проверяются, существуют ли они, и если они существуют, можно принять меры к данным, таким как создание и вставка разметки, чтобы отобразить их.

## <a name="test-for-network-connections-in-your-pwa"></a>Тестирование сетевых подключений в PWA

Кроме хранения сведений для автономного использования, полезно знать, когда доступно сетевое подключение, чтобы синхронизировать данные или сообщить пользователям, что состояние сети изменилось. Используйте следующие параметры для проверки подключения к сети.

### <a name="navigatoronline"></a>navigator.onLine  

Свойство `navigator.onLine` является boolean, который позволяет узнать текущее состояние сети. Если это `true` значение, пользователь находится в сети, в противном случае пользователь находится в автономном режиме.

### <a name="online-and-offline-events"></a>События в Интернете и автономном режиме  

Знание того, доступна ли сеть, полезно, но при изменениях подключения к сети может потребоваться принять меры. В этой ситуации может потребоваться слушать и принимать меры в ответ на сетевые события. События доступны в следующем фрагменте кода и элементах, отображаемом в `window` `document` следующем `document.body` фрагменте кода.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a>См. также  

Чтобы узнать больше об управлении автономными сценариями, перейдите на следующие страницы.  

*   [Кэш][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Сотрудник службы][MDNServiceWorker]  
*   [Веб-хранилище][MDNWebStorageApi]  
*   [navigator.onLine][MDNNavigatoronline]  
*   [События в Интернете и автономном режиме][MDNNavigatoronlineOfflineEvents]  
*   [Запрос с намерением: стратегии кэшинга в эпоху PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]
    
<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Индексация API | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование IndexDb — API IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "API веб| MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "События в Интернете и автономном режиме — navigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Going Offline by Jeremy Keith | Книга врозь"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Запрос с намерением: Стратегии кэшинга в эпоху PWAs Аароном Густафсоном | Список отдельно"  
