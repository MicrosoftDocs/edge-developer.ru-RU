---
description: Все об улучшениях рабочих процессов и том, как использовать каждую из них.
title: Улучшения рабочего процесса службы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, сотрудник службы, Project Web App
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190044"
---
# <span data-ttu-id="a2310-104">Улучшения рабочего процесса службы</span><span class="sxs-lookup"><span data-stu-id="a2310-104">Service Worker improvements</span></span>  

<span data-ttu-id="a2310-105">В этой статье вы узнаете об улучшениях [рабочих процессов обслуживания][MdnServiceWorkerApi] и сетевых запросов, которые продаются через каждую из них.</span><span class="sxs-lookup"><span data-stu-id="a2310-105">This article teaches you about improvements to [service workers][MdnServiceWorkerApi] and the network requests that pass through each one.</span></span>  <span data-ttu-id="a2310-106">**Улучшения рабочего процесса службы** находятся в инструментах " **сеть**", " **приложение**" и " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="a2310-106">The **service worker improvements** are in the **Network**, **Application**, and **Sources** tools.</span></span>  <span data-ttu-id="a2310-107">Усовершенствования включают следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="a2310-107">The improvements include the following tasks.</span></span>  

*   <span data-ttu-id="a2310-108">Отладка на основе временной шкалы рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="a2310-108">Debug based on Service Worker timelines.</span></span>  
    *   <span data-ttu-id="a2310-109">Начало запроса и продолжительность начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="a2310-109">The start of a request and duration of the bootstrap.</span></span>  
    *   <span data-ttu-id="a2310-110">Обновите регистрацию сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="a2310-110">Update to Service worker registration.</span></span>  
    *   <span data-ttu-id="a2310-111">Среда выполнения запроса с помощью обработчика [событий FETCH][MdnFetchEvent] .</span><span class="sxs-lookup"><span data-stu-id="a2310-111">The runtime of a request using the [fetch event][MdnFetchEvent] handler.</span></span>  
    *   <span data-ttu-id="a2310-112">Среда выполнения всех событий FETCH для загрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="a2310-112">The runtime of all fetch events for loading a client.</span></span>  
*   <span data-ttu-id="a2310-113">Ознакомьтесь с подробными сведениями о выборке обработчиков событий, Установка обработчиков событий и активация обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="a2310-113">Explore the runtime details of fetch event handlers, install event handlers, and activate event handlers.</span></span>  
*   <span data-ttu-id="a2310-114">Пошаговый обработчик событий FETCH и out с [данными сценария страницы](#sources).</span><span class="sxs-lookup"><span data-stu-id="a2310-114">Step into and out of fetch event handler with [page script information](#sources).</span></span>  

<span data-ttu-id="a2310-115">Эти возможности охватывают три разных средства разработчика.</span><span class="sxs-lookup"><span data-stu-id="a2310-115">The experiences span three different developer tools.</span></span>  

1.  <span data-ttu-id="a2310-116">Средство " [сеть](#network) ".</span><span class="sxs-lookup"><span data-stu-id="a2310-116">The [Network](#network) tool.</span></span>  <span data-ttu-id="a2310-117">Выберите сетевой запрос, который будет выполняться через сотрудник службы и получить доступ к соответствующей временной шкале сотрудника службы в инструменте **время** .</span><span class="sxs-lookup"><span data-stu-id="a2310-117">Choose a network request that runs through a service worker and access the corresponding timeline of the service worker in the **Timing** tool.</span></span>  
1.  <span data-ttu-id="a2310-118">Инструмент " [приложение](#application) ".</span><span class="sxs-lookup"><span data-stu-id="a2310-118">The [Application](#application) tool.</span></span>  <span data-ttu-id="a2310-119">Для отладки рабочих процессов службы перейдите к инструменту " **работники служб** ".</span><span class="sxs-lookup"><span data-stu-id="a2310-119">To debug the service workers, navigate to the **Service Workers** tool.</span></span>  
1.  <span data-ttu-id="a2310-120">Инструмент « [источники](#sources) ».</span><span class="sxs-lookup"><span data-stu-id="a2310-120">The [Sources](#sources) tool.</span></span>  <span data-ttu-id="a2310-121">Сведения о сценариях страницы Access при пошаговом выборке обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="a2310-121">Access page script information when stepping into fetch event handlers.</span></span>  

## <span data-ttu-id="a2310-122">Network</span><span class="sxs-lookup"><span data-stu-id="a2310-122">Network</span></span>  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Временная шкала рабочего процесса в инструменте "сеть"" lightbox="../media/sw-network-timeline.msft.png":::
   <span data-ttu-id="a2310-124">Представление сети</span><span class="sxs-lookup"><span data-stu-id="a2310-124">Network view</span></span>  
:::image-end:::  

<span data-ttu-id="a2310-125">Чтобы получить доступ к функциям отладки рабочего процесса службы в средстве " **сеть** ", выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="a2310-125">To access the service worker debugging features in the **Network** tool, complete one of the following actions.</span></span>  

*   <span data-ttu-id="a2310-126">Доступ непосредственно в инструменте " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="a2310-126">Access directly in the **Network** tool.</span></span>  
*   <span data-ttu-id="a2310-127">Запущено в инструменте " **приложение** ".</span><span class="sxs-lookup"><span data-stu-id="a2310-127">Started in the **Application** tool.</span></span>  
    
### <span data-ttu-id="a2310-128">Маршрутизация запросов</span><span class="sxs-lookup"><span data-stu-id="a2310-128">Request routing</span></span>  

<span data-ttu-id="a2310-129">Чтобы упростить процесс наглядного представления запросов, временные шкалы теперь отображают запуск рабочего процесса и `respondWith` события выборки.</span><span class="sxs-lookup"><span data-stu-id="a2310-129">To make request routing easier to visualize, timelines now display the service worker start-up and the `respondWith` fetch events.</span></span>  <span data-ttu-id="a2310-130">Для отладки и визуализации сетевого запроса, который передается через сервисный рабочий процесс, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a2310-130">To debug and visualize a network request that passed through a service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="a2310-131">Выберите сетевой запрос, который проходил через сотрудник службы.</span><span class="sxs-lookup"><span data-stu-id="a2310-131">Choose the network request that went through a service worker.</span></span>  
1.  <span data-ttu-id="a2310-132">Откройте инструмент **время** .</span><span class="sxs-lookup"><span data-stu-id="a2310-132">Open the **Timing** tool.</span></span>  
    
### <span data-ttu-id="a2310-133">Получение событий</span><span class="sxs-lookup"><span data-stu-id="a2310-133">Fetch events</span></span>  

<span data-ttu-id="a2310-134">Чтобы узнать больше о `respondWith` событиях выборки, щелкните стрелку раскрывающегося списка слева от `respondWith` .</span><span class="sxs-lookup"><span data-stu-id="a2310-134">To learn more about the `respondWith` fetch events, choose the dropdown arrow to the left of the `respondWith`.</span></span>  <span data-ttu-id="a2310-135">Чтобы получить дополнительные сведения об **исходном запросе** и **ответе**, используйте соответствующие стрелки в раскрывающихся списках.</span><span class="sxs-lookup"><span data-stu-id="a2310-135">To find more details about the **Original Request** and **Response Received**, use the corresponding dropdown arrows.</span></span>  

## <span data-ttu-id="a2310-136">Приложение</span><span class="sxs-lookup"><span data-stu-id="a2310-136">Application</span></span>  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Представление приложения" lightbox="../media/sw-application-timeline.msft.png":::
   <span data-ttu-id="a2310-138">Представление приложения</span><span class="sxs-lookup"><span data-stu-id="a2310-138">Application view</span></span>  
:::image-end:::  

### <span data-ttu-id="a2310-139">Временная шкала обновления рабочего процесса службы</span><span class="sxs-lookup"><span data-stu-id="a2310-139">Service worker update timeline</span></span>  

<span data-ttu-id="a2310-140">Группа Microsoft Edge DevTools добавила временную шкалу в инструмент **приложения** , чтобы отразить жизненный цикл обновления сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="a2310-140">The Microsoft Edge DevTools team added a timeline in the **Application** tool to reflect the update lifecycle of the service worker.</span></span>  <span data-ttu-id="a2310-141">В нем выводятся события установки и активации.</span><span class="sxs-lookup"><span data-stu-id="a2310-141">It displays the installation and activation events.</span></span>  <span data-ttu-id="a2310-142">Каждый из событий имеет соответствующую стрелку раскрывающегося списка, чтобы получить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a2310-142">Each of the events has a corresponding dropdown arrow to give you more details.</span></span>  

### <span data-ttu-id="a2310-143">Запрос событий маршрутизации и получения</span><span class="sxs-lookup"><span data-stu-id="a2310-143">Request routing and fetch events</span></span>  

<span data-ttu-id="a2310-144">Теперь вы можете получить доступ к временной шкале рабочих процессов службы с помощью средства " **сеть** " в консольном ящике.</span><span class="sxs-lookup"><span data-stu-id="a2310-144">You may now access the service worker timelines through the **Network** tool in the console drawer.</span></span>  <span data-ttu-id="a2310-145">Функция повышает производительность, уменьшает дублирование пользовательского интерфейса и создает более обширный процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="a2310-145">The feature benefits performance, minimizes UI duplication, and creates a more comprehensive debugging experience.</span></span>  

1.  <span data-ttu-id="a2310-146">Откройте сервисный процесс, который вы отлаживается.</span><span class="sxs-lookup"><span data-stu-id="a2310-146">Open the service worker you are debugging.</span></span>  
1.  <span data-ttu-id="a2310-147">Нажмите кнопку **Network (сеть** ), чтобы открыть [процесс маршрутизации запросов](#network).</span><span class="sxs-lookup"><span data-stu-id="a2310-147">Choose the **Network** button to open up the [request routing experience](#network).</span></span>  
1.  <span data-ttu-id="a2310-148">Используйте раскрывающиеся раскрывающегося списка **respondWith** для получения сведений о запросе и ответе на события.</span><span class="sxs-lookup"><span data-stu-id="a2310-148">Use the **respondWith** dropdowns for fetch event request and response information.</span></span>  

<span data-ttu-id="a2310-149">Средство **Network (сеть** ) отображает сетевые запросы, которые проходили через сотрудник службы, который вы отлаживается.</span><span class="sxs-lookup"><span data-stu-id="a2310-149">The **Network** tool displays the network requests that went through the service worker you are debugging.</span></span>  <span data-ttu-id="a2310-150">Автоматический фильтр — это способ сузить область исследования.</span><span class="sxs-lookup"><span data-stu-id="a2310-150">The automatic filter is a way to narrow down your exploration.</span></span>

## <span data-ttu-id="a2310-151">"Источники"</span><span class="sxs-lookup"><span data-stu-id="a2310-151">Sources</span></span>  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Представление DOM" lightbox="../media/sw-sources.msft.png":::
   <span data-ttu-id="a2310-153">Представление DOM</span><span class="sxs-lookup"><span data-stu-id="a2310-153">DOM view</span></span>  
:::image-end:::  

<span data-ttu-id="a2310-154">Чтобы найти другие сведения о стеке, установите точку останова в обработчике выборки.</span><span class="sxs-lookup"><span data-stu-id="a2310-154">To find more stack information, set a break point in the fetch handler.</span></span>  <span data-ttu-id="a2310-155">Сведения о том, где находится ресурс, запрашиваются в сценарии страницы.</span><span class="sxs-lookup"><span data-stu-id="a2310-155">The details lead to where the resource is requested in the page script.</span></span>  <span data-ttu-id="a2310-156">Когда отладчик задерживается внутри обработчика выборки, на панели справа отображается Объединенная информация стека.</span><span class="sxs-lookup"><span data-stu-id="a2310-156">When the debugger pauses inside a fetch handler, a combined stack information is displayed in the panel to the right.</span></span>  <span data-ttu-id="a2310-157">После этого вы можете перемещаться по кадрам стопки.</span><span class="sxs-lookup"><span data-stu-id="a2310-157">After that, you may move around in the stack frames.</span></span>  

### <span data-ttu-id="a2310-158">Будущие трудозатраты</span><span class="sxs-lookup"><span data-stu-id="a2310-158">Future work</span></span>  

<span data-ttu-id="a2310-159">Microsoft Edge DevTools Teams для дальнейшей разработки данных кэша и изучения других способов улучшить процесс отладки рабочего процесса для [последовательной разработки веб-приложений][MdnProgressiveWebApps] .</span><span class="sxs-lookup"><span data-stu-id="a2310-159">The Microsoft Edge DevTools team plans to further develop the cache detail and are investigating more ways to improve the service worker debugging experience for [Progressive Web Application][MdnProgressiveWebApps] developers.</span></span>  

## <span data-ttu-id="a2310-160">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a2310-160">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Прогрессивные веб-приложения (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
