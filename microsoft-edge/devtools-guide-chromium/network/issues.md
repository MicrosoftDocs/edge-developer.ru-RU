---
title: Справочные материалы по неполадкам в сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a9a3234f3516bef16328102858363ffcb06251ec
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985394"
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





# <span data-ttu-id="dc706-103">Руководство по сетевым проблемам</span><span class="sxs-lookup"><span data-stu-id="dc706-103">Network issues guide</span></span>   




<span data-ttu-id="dc706-104">В этом руководстве показано, как определить сетевые проблемы или возможности оптимизации на панели "сеть" Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="dc706-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="dc706-105">Ознакомьтесь со [статьей][NetworkPerformance] "Начало работы", чтобы ознакомиться с основными понятиями панели " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="dc706-105">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="dc706-106">Запросы, поставленные в очередь или остановленные</span><span class="sxs-lookup"><span data-stu-id="dc706-106">Queued or stalled requests</span></span>   

**<span data-ttu-id="dc706-107">Симптомы</span><span class="sxs-lookup"><span data-stu-id="dc706-107">Symptoms</span></span>**  

<span data-ttu-id="dc706-108">Шесть запросов загружаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="dc706-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="dc706-109">После этого серии запросов будут помещены в очередь или остановлены.</span><span class="sxs-lookup"><span data-stu-id="dc706-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="dc706-110">После завершения одного из шести первых запросов запускается один из запросов в очереди.</span><span class="sxs-lookup"><span data-stu-id="dc706-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="dc706-111">На **каскаде** на приведенном ниже рисунке первые шесть запросов `edge-iconx1024.msft.png` актива запускаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="dc706-111">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="dc706-112">Последующие запросы загружаются до тех пор, пока не завершится один из этих шести первоначальных элементов.</span><span class="sxs-lookup"><span data-stu-id="dc706-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Пример списка в очереди или остановленного ряда на панели "сеть"" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="dc706-114">Пример списка в очереди или остановленного ряда на панели " **сеть** "</span><span class="sxs-lookup"><span data-stu-id="dc706-114">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="dc706-115">Причины</span><span class="sxs-lookup"><span data-stu-id="dc706-115">Causes</span></span>**  

<span data-ttu-id="dc706-116">Слишком много запросов выполняется в одном домене.</span><span class="sxs-lookup"><span data-stu-id="dc706-116">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="dc706-117">Для подключений HTTP/1.0 или HTTP/1.1 Microsoft Edge допускает не более шести одновременных подключений TCP на одном узле.</span><span class="sxs-lookup"><span data-stu-id="dc706-117">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="dc706-118">Исправления</span><span class="sxs-lookup"><span data-stu-id="dc706-118">Fixes</span></span>**  

*   <span data-ttu-id="dc706-119">Реализуйте сегментирование доменов, если необходимо использовать HTTP/1.0 или HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="dc706-119">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="dc706-120">Используйте HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="dc706-120">Use HTTP/2.</span></span>  <span data-ttu-id="dc706-121">Не используйте сегментирование доменов с протоколом HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="dc706-121">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="dc706-122">Удалите или отложите ненужные запросы, чтобы загрузить критические запросы.</span><span class="sxs-lookup"><span data-stu-id="dc706-122">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="dc706-123">Медленное время до первого байта (TTFB)</span><span class="sxs-lookup"><span data-stu-id="dc706-123">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="dc706-124">Симптомы</span><span class="sxs-lookup"><span data-stu-id="dc706-124">Symptoms</span></span>**  

<span data-ttu-id="dc706-125">Запрос тратит много времени на ожидание получения первого байта с сервера.</span><span class="sxs-lookup"><span data-stu-id="dc706-125">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="dc706-126">На рисунке ниже показана длинная зеленая полоса в **каскаде** , указывающая на то, что запрос был выполнен в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="dc706-126">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="dc706-127">Это было смоделировано с помощью профиля, ограничивающего скорость сети и добавляя задержку.</span><span class="sxs-lookup"><span data-stu-id="dc706-127">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Пример запроса с медленным временем до получения первого байта" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="dc706-129">Пример запроса с медленным временем до получения первого байта</span><span class="sxs-lookup"><span data-stu-id="dc706-129">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="dc706-130">Причины</span><span class="sxs-lookup"><span data-stu-id="dc706-130">Causes</span></span>**  

*   <span data-ttu-id="dc706-131">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="dc706-131">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="dc706-132">Скорость ответа сервера не отвечает.</span><span class="sxs-lookup"><span data-stu-id="dc706-132">The server is slow to respond.</span></span>  <span data-ttu-id="dc706-133">Разведите сервер на локальный компьютер, чтобы определить, является ли это подключение или медленный сервер.</span><span class="sxs-lookup"><span data-stu-id="dc706-133">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="dc706-134">Если вы по-прежнему получаете очень много времени на первый байт \ (TTFB \) при доступе к локальному серверу, сервер работает медленно.</span><span class="sxs-lookup"><span data-stu-id="dc706-134">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="dc706-135">Исправления</span><span class="sxs-lookup"><span data-stu-id="dc706-135">Fixes</span></span>**  

*   <span data-ttu-id="dc706-136">Если соединение медленное, разрешите размещение содержимого в сети CDN или изменение поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="dc706-136">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="dc706-137">Если сервер работает медленно, рассматривайте запросы к базе данных, реализуйте кэш или изменяйте конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="dc706-137">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="dc706-138">Медленная загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="dc706-138">Slow content download</span></span>   

**<span data-ttu-id="dc706-139">Симптомы</span><span class="sxs-lookup"><span data-stu-id="dc706-139">Symptoms</span></span>**  

<span data-ttu-id="dc706-140">Загрузка запроса занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="dc706-140">A request takes a long time to download.</span></span>  

<span data-ttu-id="dc706-141">На приведенном ниже рисунке показана длинная синяя полоса в **каскаде** рядом с форматом PNG, поэтому загрузка занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="dc706-141">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Пример запроса, загрузка которого занимает много времени" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="dc706-143">Пример запроса, загрузка которого занимает много времени</span><span class="sxs-lookup"><span data-stu-id="dc706-143">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="dc706-144">Причины</span><span class="sxs-lookup"><span data-stu-id="dc706-144">Causes</span></span>**  

*   <span data-ttu-id="dc706-145">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="dc706-145">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="dc706-146">Загружается много контента.</span><span class="sxs-lookup"><span data-stu-id="dc706-146">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="dc706-147">Исправления</span><span class="sxs-lookup"><span data-stu-id="dc706-147">Fixes</span></span>**  

*   <span data-ttu-id="dc706-148">Возможно, вы размещаете содержимое в сети CDN или меняете поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="dc706-148">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="dc706-149">Уменьшите количество байтов, оптимизируя запросы.</span><span class="sxs-lookup"><span data-stu-id="dc706-149">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="dc706-150">Сведения о Contribute</span><span class="sxs-lookup"><span data-stu-id="dc706-150">Contribute knowledge</span></span>  

<span data-ttu-id="dc706-151">Есть ли у вас сетевая проблема, которая должна быть добавлена в это руководство?</span><span class="sxs-lookup"><span data-stu-id="dc706-151">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="dc706-152">Отправить твит на [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="dc706-152">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="dc706-153">Выберите **Отправить отзыв** \ ( ![ Отправить отзыв ][ImageSendFeedbackIcon] \) в DevTools или нажмите клавиши `Alt` + `Shift` + `I` \ (Windows \) или `Option` + `Shift` + `I` \ (macOS \), чтобы предоставить отзыв или запрос функций.</span><span class="sxs-lookup"><span data-stu-id="dc706-153">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="dc706-154">[Открыть вопрос][WebFundamentalsIssue] в репозитории документов.</span><span class="sxs-lookup"><span data-stu-id="dc706-154">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Проверка активности сети в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

> [!NOTE]
> <span data-ttu-id="dc706-157">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc706-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dc706-158">Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/network/issues) и разрабатывается с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Джонатан-искаженного][JonathanGarbee] (эксперта Google Developer, для Web Technology).</span><span class="sxs-lookup"><span data-stu-id="dc706-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dc706-160">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc706-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
