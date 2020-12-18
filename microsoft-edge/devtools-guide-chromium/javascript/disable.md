---
description: Откройте меню команд и запустите команду "Отключить JavaScript".
title: Отключение JavaScript с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f7aafee4b05f843319a4a744e6cba148d4642667
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230672"
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

# <span data-ttu-id="b789a-104">Отключение JavaScript с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b789a-104">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b789a-105">Выполните следующие действия, чтобы увидеть, как выглядит и работает веб-страница при отключаемом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b789a-105">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="b789a-106">[Откройте Microsoft Edge DevTools.][DevToolsOpen]</span><span class="sxs-lookup"><span data-stu-id="b789a-106">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="b789a-107">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="b789a-107">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Меню команд" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="b789a-109">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="b789a-109">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b789a-110">Начните `javascript` вводить текст, **выберите "Отключить JavaScript",** а затем `Enter` выберите команду.</span><span class="sxs-lookup"><span data-stu-id="b789a-110">Start typing `javascript`, choose **Disable JavaScript**, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="b789a-111">JavaScript теперь отключен.</span><span class="sxs-lookup"><span data-stu-id="b789a-111">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Выберите "Отключить JavaScript" в меню команд" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="b789a-113">Выберите **"Отключить JavaScript"** в меню **команд**</span><span class="sxs-lookup"><span data-stu-id="b789a-113">Choose **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b789a-114">Желтый значок предупреждения рядом с **"Источники"** напоминает, что JavaScript отключен.</span><span class="sxs-lookup"><span data-stu-id="b789a-114">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Значок предупреждения рядом с источниками" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="b789a-116">Значок предупреждения рядом с **источниками**</span><span class="sxs-lookup"><span data-stu-id="b789a-116">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b789a-117">JavaScript остается отключенным на вкладке до тех пор, пока вы открыли DevTools.</span><span class="sxs-lookup"><span data-stu-id="b789a-117">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="b789a-118">Может потребоваться перезагрузить страницу, чтобы узнать, зависит ли страница от JavaScript во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="b789a-118">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="b789a-119">Чтобы повторно включить JavaScript, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b789a-119">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="b789a-120">Снова откройте **меню команд** и запустите `Enable JavaScript` команду.</span><span class="sxs-lookup"><span data-stu-id="b789a-120">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="b789a-121">Закроем DevTools.</span><span class="sxs-lookup"><span data-stu-id="b789a-121">Close DevTools.</span></span>  

## <span data-ttu-id="b789a-122">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b789a-122">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="b789a-124">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b789a-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b789a-125">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b789a-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b789a-127">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b789a-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
