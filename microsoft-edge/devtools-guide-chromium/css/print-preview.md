---
description: Откройте вкладку "Отрисовка" и выберите "Эмуляция CSS-носителю" > "печать".
title: Принудительное переведите Microsoft Edge DevTools в режим предварительного просмотра печати (тип мультимедиа CSS Print)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a036e710de998f03e876126581956929d8652f1e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230924"
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

# <span data-ttu-id="b8adb-104">Принудительное переведите Microsoft Edge DevTools в режим предварительного просмотра печати (тип мультимедиа CSS Print)</span><span class="sxs-lookup"><span data-stu-id="b8adb-104">Force Microsoft Edge DevTools into Print Preview mode (CSS Print Media Type)</span></span>  

<span data-ttu-id="b8adb-105">Запрос [на печать мультимедиа][MDNUsingMediaQueries] управляет тем, как выглядит страница при печати.</span><span class="sxs-lookup"><span data-stu-id="b8adb-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="b8adb-106">Чтобы принудительно перенадействовать страницу в режим предварительного просмотра:</span><span class="sxs-lookup"><span data-stu-id="b8adb-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="b8adb-107">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="b8adb-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="b8adb-109">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="b8adb-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b8adb-110">`rendering`Введите, **выберите "Показать отрисовку"** и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b8adb-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="b8adb-111">В **эмуляции CSS-носите**выберите **"Печать".**</span><span class="sxs-lookup"><span data-stu-id="b8adb-111">Under **Emulate CSS media**, choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Режим предварительного просмотра" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="b8adb-113">Режим предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="b8adb-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b8adb-114">Здесь вы можете просматривать и изменять CSS, как и любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="b8adb-114">From here, you can view and change your CSS, like any other web page.</span></span>  <span data-ttu-id="b8adb-115">Перейдите [к началу работы с просмотром и изменением CSS.][DevToolsCSSGetStarted]</span><span class="sxs-lookup"><span data-stu-id="b8adb-115">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <span data-ttu-id="b8adb-116">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b8adb-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ./index.md "Начало просмотра и изменения CSS | Документы Майкрософт"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> <span data-ttu-id="b8adb-120">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b8adb-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b8adb-121">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b8adb-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b8adb-123">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b8adb-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
