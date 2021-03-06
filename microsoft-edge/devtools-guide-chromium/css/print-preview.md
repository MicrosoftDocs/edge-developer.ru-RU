---
description: Откройте средство "Rendering" и выберите эмулировать CSS-носителю > печать.
title: Force Microsoft Edge DevTools в режиме предварительного просмотра печати (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0123b7abf475212304f654c04bc232e3e96f0bda
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399080"
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

# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a><span data-ttu-id="b5134-104">Force Microsoft Edge DevTools в режиме предварительного просмотра печати</span><span class="sxs-lookup"><span data-stu-id="b5134-104">Force Microsoft Edge DevTools into Print Preview mode</span></span>  

<span data-ttu-id="b5134-105">Запрос [печатных средств массовой][MDNUsingMediaQueries] информации контролирует внешний вид страницы при печати.</span><span class="sxs-lookup"><span data-stu-id="b5134-105">The [print media query][MDNUsingMediaQueries] controls how your page looks when printed.</span></span>  <span data-ttu-id="b5134-106">Чтобы принудить страницу к режиму предварительного просмотра печати:</span><span class="sxs-lookup"><span data-stu-id="b5134-106">To force your page into print preview mode:</span></span>  

1.  <span data-ttu-id="b5134-107">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**</span><span class="sxs-lookup"><span data-stu-id="b5134-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="b5134-109">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="b5134-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b5134-110">`rendering`Введите, **выберите показать визуализацию,** а затем выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b5134-110">Type `rendering`, choose **Show Rendering**, and then select `Enter`.</span></span>  
1.  <span data-ttu-id="b5134-111">Под **эмулировать CSS-носителю**выберите **печать**.</span><span class="sxs-lookup"><span data-stu-id="b5134-111">Under **Emulate CSS media**, choose **print**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Режим предварительного просмотра печати" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       <span data-ttu-id="b5134-113">Режим предварительного просмотра печати</span><span class="sxs-lookup"><span data-stu-id="b5134-113">Print preview mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b5134-114">Отсюда можно отобразить и изменить CSS, как и любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="b5134-114">From here, you may display and change your CSS, like any other web page.</span></span>  <span data-ttu-id="b5134-115">[Перейдите, чтобы начать с просмотра и изменения CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="b5134-115">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b5134-116">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b5134-116">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ./index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> <span data-ttu-id="b5134-120">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5134-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b5134-121">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="b5134-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b5134-123">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b5134-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
