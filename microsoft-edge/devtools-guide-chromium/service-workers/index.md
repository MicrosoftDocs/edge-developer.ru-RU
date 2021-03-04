---
description: Все об усовершенствованиях сотрудников службы и об использовании каждого из них.
title: Улучшения сотрудников службы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, service worker, PWA
ms.openlocfilehash: 2f32155d1d28d1e65ad29abfe58a414f3e3c6ed7
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387282"
---
# <a name="service-worker-improvements"></a><span data-ttu-id="03f6d-104">Улучшения сотрудников службы</span><span class="sxs-lookup"><span data-stu-id="03f6d-104">Service Worker improvements</span></span>  

<span data-ttu-id="03f6d-105">В этой статье рассказывается об усовершенствованиях [][MdnServiceWorkerApi] средств разработки для работы с сотрудниками службы и сетевых запросах, которые проходят через каждый из них.</span><span class="sxs-lookup"><span data-stu-id="03f6d-105">This article teaches you about improvements to developer tools for working with [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="03f6d-106">Улучшения **сотрудников службы находятся** в **средствах Network,** **Application**и **Sources.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="03f6d-107">Улучшения упрощают выполнение следующих задач.</span><span class="sxs-lookup"><span data-stu-id="03f6d-107">The improvements simplify the following tasks.</span></span>  

*   <span data-ttu-id="03f6d-108">Отлажка на основе временных данных сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="03f6d-109">Начало запроса и длительность начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="03f6d-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="03f6d-110">Обновление регистрации сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="03f6d-111">Время запуска запроса с помощью обработера [событий для получения.][MdnFetchEvent]</span><span class="sxs-lookup"><span data-stu-id="03f6d-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="03f6d-112">Время запуска всех событий получения для загрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="03f6d-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="03f6d-113">Изучите сведения о времени запуска обработчиков событий, установите обработчики событий и активируйте обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="03f6d-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="03f6d-114">Вступай в обработник событий и выйми из него с [помощью сведений о сценарии страниц.](#sources)</span><span class="sxs-lookup"><span data-stu-id="03f6d-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  
    
<span data-ttu-id="03f6d-115">Эти опытом охватывают три различных средства разработчика.</span><span class="sxs-lookup"><span data-stu-id="03f6d-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="03f6d-116">Средство [Network.](#network)</span><span class="sxs-lookup"><span data-stu-id="03f6d-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="03f6d-117">Выберите сетевой запрос, который выполняется через сотрудника службы, и получить доступ к соответствующей временной шкале сотрудника службы в средстве **Синхронизация.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="03f6d-118">Средство [Приложения.](#application)</span><span class="sxs-lookup"><span data-stu-id="03f6d-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="03f6d-119">Чтобы отлукировать сотрудников службы, перейдите к средству **Service Workers.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="03f6d-120">Средство [Источники.](#sources)</span><span class="sxs-lookup"><span data-stu-id="03f6d-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="03f6d-121">Доступ к сведениям о скриптах страниц при входе в обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="03f6d-121">Access page script information when stepping into fetch event handlers.</span></span>  
    
## <a name="network"></a><span data-ttu-id="03f6d-122">Network</span><span class="sxs-lookup"><span data-stu-id="03f6d-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Сроки работы сотрудника службы в средстве Network" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="03f6d-124">Представление сети</span><span class="sxs-lookup"><span data-stu-id="03f6d-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="03f6d-125">Чтобы получить доступ к функциям отладки службы в средстве **Network,** выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="03f6d-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="03f6d-126">Доступ непосредственно в **средстве Network.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="03f6d-127">Запущено в **инструменте Application.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-127">Started in the **Application** tool.</span></span>  
    
### <a name="request-routing"></a><span data-ttu-id="03f6d-128">Маршрутивка запроса</span><span class="sxs-lookup"><span data-stu-id="03f6d-128">Request routing</span></span>  

<span data-ttu-id="03f6d-129">Чтобы упростить визуализацию маршрутизации запросов, в хрониках теперь отображаются запуск рабочего службы и `respondWith` события получения.</span><span class="sxs-lookup"><span data-stu-id="03f6d-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="03f6d-130">Чтобы отлаживать и визуализировать сетевой запрос, который прошел через сотрудника службы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="03f6d-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="03f6d-131">Выберите сетевой запрос, который прошел через сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="03f6d-132">Откройте средство **Синхронизация.**</span><span class="sxs-lookup"><span data-stu-id="03f6d-132">Open the **Timing** tool.</span></span>  
    
### <a name="fetch-events"></a><span data-ttu-id="03f6d-133">Извлечение событий</span><span class="sxs-lookup"><span data-stu-id="03f6d-133">Fetch events</span></span>  

<span data-ttu-id="03f6d-134">Чтобы узнать больше о `respondWith` событиях получения, выберите стрелку падения слева от `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="03f6d-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="03f6d-135">Дополнительные сведения о \*\*\*\* первоначальном запросе и ответе, \*\*\*\* полученных, используйте соответствующие стрелки отсевов.</span><span class="sxs-lookup"><span data-stu-id="03f6d-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <a name="application"></a><span data-ttu-id="03f6d-136">Приложение</span><span class="sxs-lookup"><span data-stu-id="03f6d-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Представление приложения" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="03f6d-138">Представление приложения</span><span class="sxs-lookup"><span data-stu-id="03f6d-138">Application view</span></span>  
:::image-end:::  

### <a name="service-worker-update-timeline"></a><span data-ttu-id="03f6d-139">Сроки обновления сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="03f6d-139">Service worker update timeline</span></span>  

<span data-ttu-id="03f6d-140">Команда Microsoft Edge DevTools добавила \*\*\*\* в средство приложения временную шкалу, чтобы отразить жизненный цикл обновления сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="03f6d-141">Он отображает события установки и активации.</span><span class="sxs-lookup"><span data-stu-id="03f6d-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="03f6d-142">Каждый из событий имеет соответствующую стрелку отсев, чтобы дать вам дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="03f6d-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <a name="request-routing-and-fetch-events"></a><span data-ttu-id="03f6d-143">Запрос на маршрутику и извлечение событий</span><span class="sxs-lookup"><span data-stu-id="03f6d-143">Request routing and fetch events</span></span>  

<span data-ttu-id="03f6d-144">Теперь вы можете получить доступ к временной шкале сотрудника службы с помощью средства **Network** в ящике консоли.</span><span class="sxs-lookup"><span data-stu-id="03f6d-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="03f6d-145">Функция позволяет снизить производительность, свести к минимуму дублирование пользовательского интерфейса и создать более полный интерфейс отладки.</span><span class="sxs-lookup"><span data-stu-id="03f6d-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="03f6d-146">Откройте сотрудника службы, который отладку отладки.</span><span class="sxs-lookup"><span data-stu-id="03f6d-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="03f6d-147">Выберите **кнопку "Сеть",** чтобы открыть [маршрутику запроса.](#network)</span><span class="sxs-lookup"><span data-stu-id="03f6d-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="03f6d-148">Используйте **dropdowns respondWith** для получения сведений о запросе событий и ответах.</span><span class="sxs-lookup"><span data-stu-id="03f6d-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="03f6d-149">Средство **Network** отображает сетевые запросы, которые прошли через отладку сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="03f6d-150">Автоматический фильтр — это способ сузить исследование.</span><span class="sxs-lookup"><span data-stu-id="03f6d-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <a name="sources"></a><span data-ttu-id="03f6d-151">"Источники"</span><span class="sxs-lookup"><span data-stu-id="03f6d-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Представление DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="03f6d-153">Представление DOM</span><span class="sxs-lookup"><span data-stu-id="03f6d-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="03f6d-154">Чтобы найти дополнительные сведения о стеке, установите точку разрыва в обработнике получения.</span><span class="sxs-lookup"><span data-stu-id="03f6d-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="03f6d-155">Сведения приводят к запросу ресурса в сценарии страницы.</span><span class="sxs-lookup"><span data-stu-id="03f6d-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="03f6d-156">Когда отладка останавливается в обработнике для получения, в панели справа отображается комбинированная информация о стеке.</span><span class="sxs-lookup"><span data-stu-id="03f6d-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="03f6d-157">После этого вы можете перемещаться в кадрах стека.</span><span class="sxs-lookup"><span data-stu-id="03f6d-157">After that, you may move around in the stack frames.</span></span>  

### <a name="future-work"></a><span data-ttu-id="03f6d-158">Будущая работа</span><span class="sxs-lookup"><span data-stu-id="03f6d-158">Future work</span></span>  

<span data-ttu-id="03f6d-159">Команда Microsoft Edge DevTools планирует дальнейшее развитие деталей кэша и изучает дополнительные способы [][MdnProgressiveWebApps] улучшения отладки сотрудником службы для разработчиков прогрессивных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="03f6d-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="03f6d-160">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03f6d-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Прогрессивные веб-приложения (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API API для сотрудников службы | MDN"  
