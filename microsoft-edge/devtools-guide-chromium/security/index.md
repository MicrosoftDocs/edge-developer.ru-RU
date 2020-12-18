---
description: С помощью панели безопасности убедитесь, что страница полностью защищена протоколом HTTPS.
title: Проблемы безопасности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5bef22eae8deacc81e31cf6d1c7791e016541346
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230616"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="10d40-104">Проблемы безопасности в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="10d40-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="10d40-105">Открытие панели безопасности</span><span class="sxs-lookup"><span data-stu-id="10d40-105">Open the Security panel</span></span>  

<span data-ttu-id="10d40-106">Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.</span><span class="sxs-lookup"><span data-stu-id="10d40-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="10d40-107">[Откройте DevTools.][DevToolsOpen]</span><span class="sxs-lookup"><span data-stu-id="10d40-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="10d40-108">Откройте панель **безопасности** на вкладке **"Безопасность".**</span><span class="sxs-lookup"><span data-stu-id="10d40-108">Choose the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Панель безопасности" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="10d40-110">Панель **безопасности**</span><span class="sxs-lookup"><span data-stu-id="10d40-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="10d40-111">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="10d40-111">Common problems</span></span>  

### <span data-ttu-id="10d40-112">Небезопасные основные источника</span><span class="sxs-lookup"><span data-stu-id="10d40-112">Non-secure main origins</span></span>  

<span data-ttu-id="10d40-113">Если основной источник страницы не является безопасным, в **обзоре** безопасности говорится, что эта страница **не является безопасной.**</span><span class="sxs-lookup"><span data-stu-id="10d40-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Небезопасная страница" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="10d40-115">Небезопасная страница</span><span class="sxs-lookup"><span data-stu-id="10d40-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="10d40-116">Эта проблема возникает при запросе URL-адреса по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="10d40-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="10d40-117">Для обеспечения безопасности необходимо запросить его по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="10d40-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="10d40-118">Например, если вы посмотрите на URL-адрес в адресной панели, он, вероятно, будет выглядеть примерно `http://example.com` так.</span><span class="sxs-lookup"><span data-stu-id="10d40-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="10d40-119">Для обеспечения безопасности URL-адрес должен быть `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="10d40-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="10d40-120">Если вы уже настроили HTTPS на сервере, все, что нужно сделать, чтобы устранить эту проблему, — настроить сервер на перенаправление всех HTTP-запросов на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="10d40-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="10d40-121">Если вы еще не настроили ПРОТОКОЛ HTTPS на сервере, [let's Encrypt][LetsEncrypt] предоставляет бесплатный и относительно простой способ запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="10d40-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="10d40-122">Или вы можете рассмотреть возможность размещения сайта в сети CDN.</span><span class="sxs-lookup"><span data-stu-id="10d40-122">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="10d40-123">Большинство основных узлов CDNs по умолчанию теперь находится на https.</span><span class="sxs-lookup"><span data-stu-id="10d40-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="10d40-124">Подсказка ["Использовать HTTPS"][WebhintUseHttps] в [веб-канале][Webhint] может помочь автоматизировать процесс перенаправки всех HTTP-запросов на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="10d40-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="10d40-125">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="10d40-125">Mixed content</span></span>  

<span data-ttu-id="10d40-126">**Смешанное** содержимое означает, что основной источник страницы является безопасным, но страница запрашивает ресурсы из небезопасных источников.</span><span class="sxs-lookup"><span data-stu-id="10d40-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="10d40-127">Страницы смешанного содержимого защищены только частично, так как содержимое HTTP доступно для анализаторов и уязвимо для атак "человек в середине".</span><span class="sxs-lookup"><span data-stu-id="10d40-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Смешанное содержимое" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="10d40-129">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="10d40-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="10d40-130">На предыдущем рисунке выберите запрос "Просмотр **1"** на панели "Сеть", чтобы открыть панель "Сеть" и применить фильтр, чтобы сетевой журнал отображал только незабезопасные \*\*\*\* `mixed-content:displayed` ресурсы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="10d40-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Смешанные ресурсы в сетевом журнале" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="10d40-132">Смешанные ресурсы в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="10d40-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="10d40-133">Просмотреть подробные сведения</span><span class="sxs-lookup"><span data-stu-id="10d40-133">View details</span></span>  

### <span data-ttu-id="10d40-134">Просмотр сертификата основного источника</span><span class="sxs-lookup"><span data-stu-id="10d40-134">View main origin certificate</span></span>  

<span data-ttu-id="10d40-135">В **обзоре безопасности**выберите **"Просмотреть сертификат",** чтобы быстро проверить сертификат для основного источника.</span><span class="sxs-lookup"><span data-stu-id="10d40-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Сертификат основного источника" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="10d40-137">Сертификат основного источника</span><span class="sxs-lookup"><span data-stu-id="10d40-137">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="10d40-138">Просмотр сведений об источнике</span><span class="sxs-lookup"><span data-stu-id="10d40-138">View origin details</span></span>  

<span data-ttu-id="10d40-139">Выберите одну из записей в левой области nav, чтобы просмотреть сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="10d40-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="10d40-140">На странице сведений можно просмотреть сведения о подсети и сертификате.</span><span class="sxs-lookup"><span data-stu-id="10d40-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="10d40-141">Сведения о прозрачности сертификата также показано, когда они доступны.</span><span class="sxs-lookup"><span data-stu-id="10d40-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Основные сведения об источнике" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="10d40-143">Основные сведения об источнике</span><span class="sxs-lookup"><span data-stu-id="10d40-143">Main origin details</span></span>  
:::image-end:::  

## <span data-ttu-id="10d40-144">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="10d40-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[LetsEncrypt]: https://letsencrypt.org "Шифруем — бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование HTTPS | документация по webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="10d40-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="10d40-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="10d40-151">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/security/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="10d40-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="10d40-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="10d40-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
