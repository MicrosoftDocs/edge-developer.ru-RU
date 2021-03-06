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
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a><span data-ttu-id="46da3-104">Использование сотрудников служб для управления сетевыми запросами и push-уведомлениями</span><span class="sxs-lookup"><span data-stu-id="46da3-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="46da3-105">Сотрудники службы — это особый тип веб-работника, который может перехватывать, изменять и отвечать на все сетевые запросы с помощью `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="46da3-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="46da3-106">Сотрудники службы могут получать доступ к API и асинхронным хранилищам клиентских `Cache` данных, например, для `IndexedDB` хранения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46da3-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <a name="registering-a-service-worker"></a><span data-ttu-id="46da3-107">Регистрация сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="46da3-107">Registering a Service Worker</span></span>  

<span data-ttu-id="46da3-108">Как и другие веб-работники, сотрудники службы должны существовать в отдельном файле.</span><span class="sxs-lookup"><span data-stu-id="46da3-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="46da3-109">Вы ссылались на этот файл при регистрации сотрудника службы, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="46da3-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="46da3-110">Современные браузеры предоставляют различные уровни поддержки для сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="46da3-111">Поэтому перед запуском любого кода, связанного с работником службы, необходимо проверить наличие `serviceWorker` объекта.</span><span class="sxs-lookup"><span data-stu-id="46da3-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="46da3-112">В этом фрагменте кода сотрудник службы регистрируется с помощью файла, расположенного `serviceworker.min.js` в корне сайта.</span><span class="sxs-lookup"><span data-stu-id="46da3-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="46da3-113">Убедитесь, что файл JavaScript, который определяет сотрудника службы, существует в каталоге самого высокого уровня, который необходимо управлять \(который называется областью рабочего службы\).</span><span class="sxs-lookup"><span data-stu-id="46da3-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="46da3-114">В предыдущем фрагменте кода файл хранится в корне, и работник службы управляет всеми страницами в домене.</span><span class="sxs-lookup"><span data-stu-id="46da3-114">In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="46da3-115">Если файл Service Worker хранится в каталоге, областью сотрудника службы будет каталог и все `js` `js` подтеки.</span><span class="sxs-lookup"><span data-stu-id="46da3-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="46da3-116">В качестве наилучшей практики поместите файл Service Worker в корне вашего сайта, если не потребуется уменьшить область действия сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <a name="the-service-worker-lifecycle"></a><span data-ttu-id="46da3-117">Жизненный цикл сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="46da3-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="46da3-118">Жизненный цикл сотрудника службы состоит из нескольких этапов, каждый шаг вызывает событие.</span><span class="sxs-lookup"><span data-stu-id="46da3-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="46da3-119">Вы можете добавить слушателей в эти события, чтобы запустить код для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="46da3-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="46da3-120">В следующем списке представлено представление жизненного цикла и связанных с ними событий сотрудников служб.</span><span class="sxs-lookup"><span data-stu-id="46da3-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1.  <span data-ttu-id="46da3-121">Регистрация сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="46da3-122">Браузер загружает файл JavaScript, устанавливает сотрудника службы и запускает `install` событие.</span><span class="sxs-lookup"><span data-stu-id="46da3-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="46da3-123">Вы можете использовать событие для предварительного кэша любых важных и долгоживучивых файлов, таких как CSS-файлы, файлы JavaScript, изображения логотипа, автономные страницы и так далее с вашего `install` веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="46da3-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="46da3-124">Активируется сотрудник службы, который запускает `activate` событие.</span><span class="sxs-lookup"><span data-stu-id="46da3-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="46da3-125">Используйте это событие для очистки устаревших кэшей.</span><span class="sxs-lookup"><span data-stu-id="46da3-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="46da3-126">Работник службы готов к запуску при обновлении страницы или при переходе пользователя на новую страницу на сайте.</span><span class="sxs-lookup"><span data-stu-id="46da3-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="46da3-127">Если вы хотите запустить сотрудника службы, не дожидаясь, используйте `self.skipWaiting()` метод во время `install` события.</span><span class="sxs-lookup"><span data-stu-id="46da3-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="46da3-128">В настоящее время работает рабочий службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-128">The Service Worker is now running.</span></span>     
    
## <a name="using-fetch-in-service-workers"></a><span data-ttu-id="46da3-129">Использование fetch в service Workers</span><span class="sxs-lookup"><span data-stu-id="46da3-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="46da3-130">Главное событие, которое вы используете в service Worker— `fetch` это событие.</span><span class="sxs-lookup"><span data-stu-id="46da3-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="46da3-131">Событие выполняется каждый раз, когда браузер пытается получить доступ к содержимому в `fetch` области сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="46da3-132">В следующем фрагменте кода показано, как добавить слушателя в событие fetch.</span><span class="sxs-lookup"><span data-stu-id="46da3-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="46da3-133">В обработнике вы можете контролировать, передается ли запрос в сеть, извлекает ли он из `fetch` кэша и так далее.</span><span class="sxs-lookup"><span data-stu-id="46da3-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="46da3-134">Подход, который вы принимаете, зависит от типа запрашиваемого ресурса, его частого обновления и другой бизнес-логики, уникальной для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="46da3-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="46da3-135">Вот несколько примеров того, что вы можете сделать:</span><span class="sxs-lookup"><span data-stu-id="46da3-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="46da3-136">Если доступно, верните ответ из кэша, в противном случае откат запросив ресурс по сети.</span><span class="sxs-lookup"><span data-stu-id="46da3-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="46da3-137">Извлекаем ресурс из сети, кэшируйте копию и возвращая ответ.</span><span class="sxs-lookup"><span data-stu-id="46da3-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="46da3-138">Разрешить пользователю указать предпочтение для сохранения данных.</span><span class="sxs-lookup"><span data-stu-id="46da3-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="46da3-139">Поставляем изображение-местоодатель для определенных запросов изображения.</span><span class="sxs-lookup"><span data-stu-id="46da3-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="46da3-140">Создание ответа непосредственно в работнике службы.</span><span class="sxs-lookup"><span data-stu-id="46da3-140">Generate a response directly in the Service Worker.</span></span>  
    
## <a name="push-notifications"></a><span data-ttu-id="46da3-141">Push-уведомления</span><span class="sxs-lookup"><span data-stu-id="46da3-141">Push Notifications</span></span>  

<span data-ttu-id="46da3-142">Сотрудники службы могут нажимать уведомления пользователям.</span><span class="sxs-lookup"><span data-stu-id="46da3-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="46da3-143">Push-уведомления помогают пользователям повторно взаимодействовать с вашим приложением после некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="46da3-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="46da3-144">Дополнительные сведения перейдите к погонам Push Notifications и [демонстрации.][AzurewebsitesWebpushdemo]</span><span class="sxs-lookup"><span data-stu-id="46da3-144">For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <a name="see-also"></a><span data-ttu-id="46da3-145">См. также</span><span class="sxs-lookup"><span data-stu-id="46da3-145">See also</span></span>  

<span data-ttu-id="46da3-146">Чтобы узнать больше о работниках службы, перейдите к следующему списку связанных тем.</span><span class="sxs-lookup"><span data-stu-id="46da3-146">To learn more about Service Workers, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="46da3-147">Обеспечение автономной работы PWAs с сотрудниками службы</span><span class="sxs-lookup"><span data-stu-id="46da3-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="46da3-148">Как сделать PWAs повторно задействованными с помощью Уведомлений и Push</span><span class="sxs-lookup"><span data-stu-id="46da3-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Веб-push-уведомления |  Демонстрации Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Обеспечение автономной работы PWAs с сотрудниками службы — pwAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Как сделать PWAs повторно задействованными с помощью Уведомлений и Push - PWAs | MDN"  
