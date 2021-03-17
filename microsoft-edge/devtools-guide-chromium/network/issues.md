---
description: Узнайте, как обнаруживать сетевые проблемы в сетевой панели Microsoft Edge DevTools.
title: Справочные материалы по неполадкам в сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9b92ca7b759fab80d7d829b31f605ccb8062a816
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439621"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="network-issues-guide"></a><span data-ttu-id="742bc-104">Справочные материалы по неполадкам в сети</span><span class="sxs-lookup"><span data-stu-id="742bc-104">Network issues guide</span></span>  

<span data-ttu-id="742bc-105">В этом руководстве показано, как выявлять сетевые проблемы или возможности оптимизации в сетевой панели Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="742bc-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="742bc-106">Чтобы узнать основы сетевого средства, перейдите к [сайту Get Started][NetworkPerformance]. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="742bc-106">To learn the basics of the **Network** tool, navigate to [Get Started][NetworkPerformance].</span></span>  

## <a name="queued-or-stalled-requests"></a><span data-ttu-id="742bc-107">Очередные или отостановимые запросы</span><span class="sxs-lookup"><span data-stu-id="742bc-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="742bc-108">Симптомы</span><span class="sxs-lookup"><span data-stu-id="742bc-108">Symptoms</span></span>**  

<span data-ttu-id="742bc-109">Одновременно загружаются шесть запросов.</span><span class="sxs-lookup"><span data-stu-id="742bc-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="742bc-110">После этого ряд запросов выстроились в очередь или застопорились.</span><span class="sxs-lookup"><span data-stu-id="742bc-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="742bc-111">После завершения одного из первых шести запросов начинается один из запросов в очереди.</span><span class="sxs-lookup"><span data-stu-id="742bc-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="742bc-112">В **водопаде** на следующем рисунке одновременно начинаются первые шесть запросов `edge-iconx1024.msft.png` на актив.</span><span class="sxs-lookup"><span data-stu-id="742bc-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="742bc-113">Последующие запросы отостановятся до завершения одного из шести исходных запросов.</span><span class="sxs-lookup"><span data-stu-id="742bc-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Пример очереди или срыва ряда в панели Network" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="742bc-115">Пример очереди или срыва ряда в **средстве Network**</span><span class="sxs-lookup"><span data-stu-id="742bc-115">An example of a queued or stalled series in the **Network** tool</span></span>  
:::image-end:::  

**<span data-ttu-id="742bc-116">Причины</span><span class="sxs-lookup"><span data-stu-id="742bc-116">Causes</span></span>**  

<span data-ttu-id="742bc-117">Слишком много запросов делается в одном домене.</span><span class="sxs-lookup"><span data-stu-id="742bc-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="742bc-118">В подключениях HTTP/1.0 или HTTP/1.1 Microsoft Edge разрешает не более шести одновременных подключений TCP на один хост.</span><span class="sxs-lookup"><span data-stu-id="742bc-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="742bc-119">Исправление</span><span class="sxs-lookup"><span data-stu-id="742bc-119">Fixes</span></span>**  

*   <span data-ttu-id="742bc-120">Реализуем осколок домена, если необходимо использовать HTTP/1.0 или HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="742bc-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="742bc-121">Используйте HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="742bc-121">Use HTTP/2.</span></span>  <span data-ttu-id="742bc-122">Не используйте осколок домена с помощью HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="742bc-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="742bc-123">Удалите или отойте ненужные запросы, чтобы критические запросы загружались ранее.</span><span class="sxs-lookup"><span data-stu-id="742bc-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <a name="slow-time-to-first-byte-ttfb"></a><span data-ttu-id="742bc-124">Медленное время для первого byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="742bc-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="742bc-125">Симптомы</span><span class="sxs-lookup"><span data-stu-id="742bc-125">Symptoms</span></span>**  

<span data-ttu-id="742bc-126">Запрос тратит много времени на ожидание получения первого byte с сервера.</span><span class="sxs-lookup"><span data-stu-id="742bc-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="742bc-127">На следующем рисунке длинная зеленая \*\*\*\* планка водопада указывает на то, что запрос долго ждали.</span><span class="sxs-lookup"><span data-stu-id="742bc-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="742bc-128">Это было смоделированно с помощью профиля, чтобы ограничить скорость сети и добавить задержку.</span><span class="sxs-lookup"><span data-stu-id="742bc-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Пример запроса с медленным временем до первого byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="742bc-130">Пример запроса с медленным временем до первого byte</span><span class="sxs-lookup"><span data-stu-id="742bc-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="742bc-131">Причины</span><span class="sxs-lookup"><span data-stu-id="742bc-131">Causes</span></span>**  

*   <span data-ttu-id="742bc-132">Подключение между клиентом и сервером медленно.</span><span class="sxs-lookup"><span data-stu-id="742bc-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="742bc-133">Сервер медленно реагирует.</span><span class="sxs-lookup"><span data-stu-id="742bc-133">The server is slow to respond.</span></span>  <span data-ttu-id="742bc-134">Локализуй сервер, чтобы определить, медленно ли это подключение или сервер.</span><span class="sxs-lookup"><span data-stu-id="742bc-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="742bc-135">Если при доступе к локальному серверу вы все еще получаете медленное время для первого byte \(TTFB\), сервер медленно.</span><span class="sxs-lookup"><span data-stu-id="742bc-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="742bc-136">Исправление</span><span class="sxs-lookup"><span data-stu-id="742bc-136">Fixes</span></span>**  

*   <span data-ttu-id="742bc-137">Если подключение медленное, рассмотрите возможность размещения контента на CDN или изменения поставщиков хостинга.</span><span class="sxs-lookup"><span data-stu-id="742bc-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="742bc-138">Если сервер медленный, следует оптимизировать запросы баз данных, реализовать кэш или изменить конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="742bc-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <a name="slow-content-download"></a><span data-ttu-id="742bc-139">Медленная загрузка контента</span><span class="sxs-lookup"><span data-stu-id="742bc-139">Slow content download</span></span>  

**<span data-ttu-id="742bc-140">Симптомы</span><span class="sxs-lookup"><span data-stu-id="742bc-140">Symptoms</span></span>**  

<span data-ttu-id="742bc-141">Загрузка запроса занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="742bc-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="742bc-142">На следующем рисунке длинная синяя планка в **водопаде** рядом с png означает, что загрузка заняла много времени.</span><span class="sxs-lookup"><span data-stu-id="742bc-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Пример запроса, который занимает много времени для скачивания" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="742bc-144">Пример запроса, который занимает много времени для скачивания</span><span class="sxs-lookup"><span data-stu-id="742bc-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="742bc-145">Причины</span><span class="sxs-lookup"><span data-stu-id="742bc-145">Causes</span></span>**  

*   <span data-ttu-id="742bc-146">Подключение между клиентом и сервером медленно.</span><span class="sxs-lookup"><span data-stu-id="742bc-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="742bc-147">Загружается большое количество контента.</span><span class="sxs-lookup"><span data-stu-id="742bc-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="742bc-148">Исправление</span><span class="sxs-lookup"><span data-stu-id="742bc-148">Fixes</span></span>**  

*   <span data-ttu-id="742bc-149">Рассмотрите возможность размещения контента на CDN или изменения поставщиков хостинга.</span><span class="sxs-lookup"><span data-stu-id="742bc-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="742bc-150">Отправьте меньшее количество bytes путем оптимизации запросов.</span><span class="sxs-lookup"><span data-stu-id="742bc-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="742bc-151">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="742bc-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая проблема — MicrosoftDocs/edge-developer"  

> [!NOTE]
> <span data-ttu-id="742bc-154">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="742bc-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="742bc-155">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/issues) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\) и [Джонатан Гарби][JonathanGarbee] \(Эксперт разработчика Google для веб-технологий\).</span><span class="sxs-lookup"><span data-stu-id="742bc-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="742bc-157">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="742bc-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
