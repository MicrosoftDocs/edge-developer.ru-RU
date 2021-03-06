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
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a><span data-ttu-id="d2223-104">Поддержка автономного и сетевого подключения в прогрессивных веб-приложениях</span><span class="sxs-lookup"><span data-stu-id="d2223-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="d2223-105">В течение многих лет организации неохотно вкладывали значительные средства в веб-программное обеспечение над отечественным программным обеспечением, так как веб-приложения зависят от стабильных сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="d2223-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="d2223-106">Сегодня веб-платформа предлагает надежные параметры, которые позволяют пользователям продолжать работать, даже если сетевое подключение становится неустойчивым или полностью отключено.</span><span class="sxs-lookup"><span data-stu-id="d2223-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <a name="use-the-caching-to-improve-performance-of-pwas"></a><span data-ttu-id="d2223-107">Использование кэшинга для повышения производительности pwAs</span><span class="sxs-lookup"><span data-stu-id="d2223-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="d2223-108">С введением [рабочих служб][MDNServiceWorker]веб-платформа добавила API для предоставления доступа к управляемым `Cache` кэшным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="d2223-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="d2223-109">Этот API на основе обещаний позволяет разработчикам хранить и извлекать многие веб-ресурсы: HTML, CSS, JavaScript, изображения, JSON и так далее.</span><span class="sxs-lookup"><span data-stu-id="d2223-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="d2223-110">Обычно API кэша используется в контексте сотрудника службы, но он также доступен в основном потоке `window` объекта.</span><span class="sxs-lookup"><span data-stu-id="d2223-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="d2223-111">Одним из распространенных использований API является предварительное кэшировать критически важные ресурсы при установке сотрудника службы, как показано в следующем фрагменте `Cache` кода.</span><span class="sxs-lookup"><span data-stu-id="d2223-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="d2223-112">Этот код, который запускается во время события жизненного цикла сотрудника службы, открывает кэш с именем, а затем, когда он имеет указатель на кэш, добавляет в него четыре ресурса с помощью `install` `static-cache` `addAll()` метода.</span><span class="sxs-lookup"><span data-stu-id="d2223-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="d2223-113">Часто этот подход соеди- `fetch`</span><span class="sxs-lookup"><span data-stu-id="d2223-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="d2223-114">Фрагмент кода выполняется в service Worker всякий раз, когда браузер делает `fetch` запрос на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="d2223-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="d2223-115">В этом случае существует условное заявление, которое выполняется, если запрос для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="d2223-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="d2223-116">Работник службы проверяет, существует ли файл уже в любом кэше \(с помощью `match()` метода\).</span><span class="sxs-lookup"><span data-stu-id="d2223-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="d2223-117">Если запрос существует в кэше, этот кэшный результат возвращается.</span><span class="sxs-lookup"><span data-stu-id="d2223-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="d2223-118">Если нет, для этого ресурса запускается новый ресурс, копия ответа кэшируется на более позднее время, и ответ `fetch` возвращается.</span><span class="sxs-lookup"><span data-stu-id="d2223-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="d2223-119">Если сбой из-за недоступности сети, страница в автономном режиме возвращается `fetch` из кэша.</span><span class="sxs-lookup"><span data-stu-id="d2223-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="d2223-120">Это простое введение показывает, как использовать кэшинг в прогрессивном веб-приложении (PWA).</span><span class="sxs-lookup"><span data-stu-id="d2223-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="d2223-121">Каждый PWA отличается и может использовать различные стратегии кэшинга.</span><span class="sxs-lookup"><span data-stu-id="d2223-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="d2223-122">Ваш код может выглядеть по-другому, и вы можете использовать различные стратегии кэшинга для различных маршрутов в одном приложении.</span><span class="sxs-lookup"><span data-stu-id="d2223-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a><span data-ttu-id="d2223-123">Использование IndexedDB в PWA для хранения структурированных данных</span><span class="sxs-lookup"><span data-stu-id="d2223-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="d2223-124">API для хранения структурированных данных.</span><span class="sxs-lookup"><span data-stu-id="d2223-124">is an API for storing structured data.</span></span> <span data-ttu-id="d2223-125">Как и API, он также асинхронен, что означает, что его можно использовать в основном потоке или с веб-рабочими, такими как `Cache` работники службы.</span><span class="sxs-lookup"><span data-stu-id="d2223-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="d2223-126">Используйте API для хранения значительного количества структурированных данных на клиенте или двоичных данных, таких `IndexedDB` как зашифрованные объекты мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d2223-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="d2223-127">Дополнительные сведения можно получить в [праймере MDN с помощью IndexedDB.][MDNIndexeddbApiUsing]</span><span class="sxs-lookup"><span data-stu-id="d2223-127">For more information, navigate to [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <a name="understand-storage-options-for-pwas"></a><span data-ttu-id="d2223-128">Понимание параметров хранения для PWAs</span><span class="sxs-lookup"><span data-stu-id="d2223-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="d2223-129">Иногда может потребоваться хранить небольшие объемы данных для улучшения автономного доступа пользователей.</span><span class="sxs-lookup"><span data-stu-id="d2223-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="d2223-130">Если это так, вы можете найти простоту системы пары ключ-значение веб-хранилища отвечает вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="d2223-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d2223-131">Веб-хранилище — это синхронный процесс, который не доступен для использования в рабочих потоках, таких как Service Workers.</span><span class="sxs-lookup"><span data-stu-id="d2223-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="d2223-132">Интенсивное использование может создавать проблемы с производительностью для приложения.</span><span class="sxs-lookup"><span data-stu-id="d2223-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="d2223-133">Существует 2 типа веб-хранилища: `localStorage` и `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="d2223-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="d2223-134">Каждый из них поддерживается как отдельный хранилище данных, изолированный для созданного домена.</span><span class="sxs-lookup"><span data-stu-id="d2223-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="d2223-135">сохраняется только в течение сеанса просмотра (например, при открытом браузере, который включает обновление и восстановление).</span><span class="sxs-lookup"><span data-stu-id="d2223-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="d2223-136">сохраняется до тех пор, пока данные не будут удалены кодом, пользователем или браузером (например, если доступно ограниченное хранилище).</span><span class="sxs-lookup"><span data-stu-id="d2223-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="d2223-137">В следующем фрагменте кода показано, как использовать `localStorage` , который похож на `sessionStorage` используемый.</span><span class="sxs-lookup"><span data-stu-id="d2223-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="d2223-138">Этот фрагмент кода захватывает метаданные о текущей странице и хранит ее в объекте JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d2223-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="d2223-139">Затем он сохраняет это значение как JSON при использовании метода и назначает ключ, равный `localStorage` `setItem()` текущему `window.location` URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="d2223-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="d2223-140">Вы можете получить сведения из `localStorage` `getItem()` метода.</span><span class="sxs-lookup"><span data-stu-id="d2223-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="d2223-141">В следующем фрагменте кода показано, как использовать кэширование для перечисляния кэшных страниц и извлечения метаданных для выполнения задачи, например создания списка `localstorage` ссылок.</span><span class="sxs-lookup"><span data-stu-id="d2223-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="d2223-142">Метод передает URL-адрес запроса в метод для получения любых `insertOfflineLink()` `localStorage.getItem()` сохраненных метаданных.</span><span class="sxs-lookup"><span data-stu-id="d2223-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="d2223-143">Полученные данные проверяются, существуют ли они, и если они существуют, можно принять меры к данным, таким как создание и вставка разметки, чтобы отобразить их.</span><span class="sxs-lookup"><span data-stu-id="d2223-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <a name="test-for-network-connections-in-your-pwa"></a><span data-ttu-id="d2223-144">Тестирование сетевых подключений в PWA</span><span class="sxs-lookup"><span data-stu-id="d2223-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="d2223-145">Кроме хранения сведений для автономного использования, полезно знать, когда доступно сетевое подключение, чтобы синхронизировать данные или сообщить пользователям, что состояние сети изменилось.</span><span class="sxs-lookup"><span data-stu-id="d2223-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="d2223-146">Используйте следующие параметры для проверки подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="d2223-146">Use the following options to test for network connectivity.</span></span>

### <a name="navigatoronline"></a><span data-ttu-id="d2223-147">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="d2223-147">navigator.onLine</span></span>  

<span data-ttu-id="d2223-148">Свойство `navigator.onLine` является boolean, который позволяет узнать текущее состояние сети.</span><span class="sxs-lookup"><span data-stu-id="d2223-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="d2223-149">Если это `true` значение, пользователь находится в сети, в противном случае пользователь находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="d2223-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <a name="online-and-offline-events"></a><span data-ttu-id="d2223-150">События в Интернете и автономном режиме</span><span class="sxs-lookup"><span data-stu-id="d2223-150">Online and Offline Events</span></span>  

<span data-ttu-id="d2223-151">Знание того, доступна ли сеть, полезно, но при изменениях подключения к сети может потребоваться принять меры.</span><span class="sxs-lookup"><span data-stu-id="d2223-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="d2223-152">В этой ситуации может потребоваться слушать и принимать меры в ответ на сетевые события.</span><span class="sxs-lookup"><span data-stu-id="d2223-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="d2223-153">События доступны в следующем фрагменте кода и элементах, отображаемом в `window` `document` следующем `document.body` фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="d2223-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a><span data-ttu-id="d2223-154">См. также</span><span class="sxs-lookup"><span data-stu-id="d2223-154">See also</span></span>  

<span data-ttu-id="d2223-155">Чтобы узнать больше об управлении автономными сценариями, перейдите на следующие страницы.</span><span class="sxs-lookup"><span data-stu-id="d2223-155">To learn more about managing offline scenarios, navigate to the following pages.</span></span>  

*   [<span data-ttu-id="d2223-156">Кэш</span><span class="sxs-lookup"><span data-stu-id="d2223-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="d2223-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="d2223-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="d2223-158">Сотрудник службы</span><span class="sxs-lookup"><span data-stu-id="d2223-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="d2223-159">Веб-хранилище</span><span class="sxs-lookup"><span data-stu-id="d2223-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="d2223-160">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="d2223-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="d2223-161">События в Интернете и автономном режиме</span><span class="sxs-lookup"><span data-stu-id="d2223-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="d2223-162">Запрос с намерением: стратегии кэшинга в эпоху PWAs</span><span class="sxs-lookup"><span data-stu-id="d2223-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]
    
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
