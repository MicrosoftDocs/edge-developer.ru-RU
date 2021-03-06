---
description: Используйте панель безопасности, чтобы убедиться, что страница полностью защищена HTTPS.
title: Понимание проблем безопасности с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397778"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a><span data-ttu-id="6964a-104">Понимание проблем безопасности с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6964a-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a><span data-ttu-id="6964a-105">Откройте панель безопасности</span><span class="sxs-lookup"><span data-stu-id="6964a-105">Open the Security panel</span></span>  

<span data-ttu-id="6964a-106">Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.</span><span class="sxs-lookup"><span data-stu-id="6964a-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="6964a-107">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="6964a-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="6964a-108">Выберите **вкладку Безопасность,** чтобы открыть **средство безопасности.**</span><span class="sxs-lookup"><span data-stu-id="6964a-108">Choose the **Security** tab to open the **Security** tool.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Панель безопасности" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="6964a-110">Панель **безопасности**</span><span class="sxs-lookup"><span data-stu-id="6964a-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <a name="common-problems"></a><span data-ttu-id="6964a-111">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="6964a-111">Common problems</span></span>  

### <a name="non-secure-main-origins"></a><span data-ttu-id="6964a-112">Небезопасные основные истоки</span><span class="sxs-lookup"><span data-stu-id="6964a-112">Non-secure main origins</span></span>  

<span data-ttu-id="6964a-113">Если основное происхождение страницы не защищено, в **Обзоре** безопасности говорится, что эта **страница не является безопасной.**</span><span class="sxs-lookup"><span data-stu-id="6964a-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Небезопасная страница" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="6964a-115">Небезопасная страница</span><span class="sxs-lookup"><span data-stu-id="6964a-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="6964a-116">Эта проблема возникает, когда URL-адрес, который вы посетили, был запросят по HTTP.</span><span class="sxs-lookup"><span data-stu-id="6964a-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="6964a-117">Чтобы обеспечить безопасность, необходимо запросить его через HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6964a-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="6964a-118">Например, если вы посмотрите на URL-адрес в панели адресов, он, вероятно, похож на `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="6964a-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="6964a-119">Для обеспечения безопасности URL-адрес должен быть `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="6964a-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="6964a-120">Если вы уже настроили HTTPS на сервере, все, что необходимо сделать для устранения этой проблемы, это настроить сервер, чтобы перенаправить все запросы HTTP на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6964a-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="6964a-121">Если вы не настроили HTTPS на сервере, [let's Encrypt][LetsEncrypt] предоставляет бесплатный и относительно простой способ запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="6964a-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="6964a-122">Или, вы можете рассмотреть возможность размещения вашего сайта на CDN.</span><span class="sxs-lookup"><span data-stu-id="6964a-122">Or, you may consider hosting your site on a CDN.</span></span>  <span data-ttu-id="6964a-123">Большинство основных сайтов cdNs, принимающих https по умолчанию, сейчас.</span><span class="sxs-lookup"><span data-stu-id="6964a-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="6964a-124">Подсказка [Использование HTTPS][WebhintUseHttps] в [веб-хинте][Webhint] может помочь автоматизировать процесс, чтобы убедиться, что все запросы HTTP направляются в HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6964a-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <a name="mixed-content"></a><span data-ttu-id="6964a-125">Смешанный контент</span><span class="sxs-lookup"><span data-stu-id="6964a-125">Mixed content</span></span>  

<span data-ttu-id="6964a-126">**Смешанное** содержимое означает, что основное происхождение страницы является безопасным, но страница запрашивает ресурсы из небезопасных источников.</span><span class="sxs-lookup"><span data-stu-id="6964a-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="6964a-127">Смешанные страницы контента защищены только частично, так как содержимое HTTP доступно для нюхателей и уязвимо для атак из-за человека в центре.</span><span class="sxs-lookup"><span data-stu-id="6964a-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Смешанный контент" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="6964a-129">Смешанный контент</span><span class="sxs-lookup"><span data-stu-id="6964a-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="6964a-130">На предыдущем рисунке выберите запрос **View 1** \*\*\*\* в панели Network, чтобы открыть средство Network и применить фильтр, чтобы журнал Сети отображал только `mixed-content:displayed` небезопасные ресурсы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6964a-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** tool and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Смешанные ресурсы в сетевом журнале" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="6964a-132">Смешанные ресурсы в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="6964a-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <a name="view-details"></a><span data-ttu-id="6964a-133">Просмотреть подробные сведения</span><span class="sxs-lookup"><span data-stu-id="6964a-133">View details</span></span>  

### <a name="view-main-origin-certificate"></a><span data-ttu-id="6964a-134">Просмотр основного сертификата происхождения</span><span class="sxs-lookup"><span data-stu-id="6964a-134">View main origin certificate</span></span>  

<span data-ttu-id="6964a-135">В **обзоре безопасности**выберите **сертификат View,** чтобы быстро проверить сертификат основного происхождения.</span><span class="sxs-lookup"><span data-stu-id="6964a-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Сертификат основного происхождения" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="6964a-137">Сертификат основного происхождения</span><span class="sxs-lookup"><span data-stu-id="6964a-137">A main origin certificate</span></span>  
:::image-end:::  

### <a name="view-origin-details"></a><span data-ttu-id="6964a-138">Просмотр сведений о происхождении</span><span class="sxs-lookup"><span data-stu-id="6964a-138">View origin details</span></span>  

<span data-ttu-id="6964a-139">Выберите одну из записей в левом nav, чтобы просмотреть сведения о происхождении.</span><span class="sxs-lookup"><span data-stu-id="6964a-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="6964a-140">На странице подробные сведения можно просмотреть сведения о подключении и сертификате.</span><span class="sxs-lookup"><span data-stu-id="6964a-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="6964a-141">Сведения о прозрачности сертификата также показано при наличии.</span><span class="sxs-lookup"><span data-stu-id="6964a-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Основные сведения о происхождении" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="6964a-143">Основные сведения о происхождении</span><span class="sxs-lookup"><span data-stu-id="6964a-143">Main origin details</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6964a-144">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6964a-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[LetsEncrypt]: https://letsencrypt.org "Шифруем — бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование https | документация по веб-сайтам"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="6964a-150">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6964a-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6964a-151">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/security/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="6964a-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6964a-153">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6964a-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
