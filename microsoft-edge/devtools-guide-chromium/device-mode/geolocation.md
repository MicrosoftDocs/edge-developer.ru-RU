---
title: Переопределение географического положения с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1bd6da8d0e4c170fa94fed995a26e77b119992f1
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981833"
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





# <span data-ttu-id="eb9cf-103">Переопределение географического положения с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="eb9cf-103">Override geolocation with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="eb9cf-104">Многие веб-сайты имеют преимущество для предоставления пользователям более подходящих возможностей.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-104">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="eb9cf-105">Например, на веб-сайте Weather может отображаться локальный прогноз в области пользователя, после того как пользователь выдает разрешение веб-сайту на доступ к текущему расположению пользователя.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-105">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="eb9cf-106">Если вы создаете пользовательский интерфейс, который изменяется в зависимости от того, где находится пользователь, возможно, вы захотите убедиться в том, что сайт правильно работает в разных местах по всему миру.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-106">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="eb9cf-107">Чтобы переопределить географическое положение в Microsoft Edge DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-107">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="eb9cf-108">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="eb9cf-108">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="eb9cf-110">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="eb9cf-110">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="eb9cf-111">Введите текст `sensors` , установите флажок **Показать датчики**и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="eb9cf-111">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="eb9cf-112">Вкладка **датчики** откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-112">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="eb9cf-113">В списке **географическое положение** выберите один из готовых городов `Tokyo` или выберите **другое расположение** , чтобы указать пользовательские координаты долготы и широты, или выберите пункт **расположение недоступно** , чтобы увидеть, как работает сайт, когда его расположение недоступно.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-113">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or select **Custom location** to enter custom longitude and latitude coordinates, or select **Location unavailable** to see how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Выберите Токио в списке "географическое положение"" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="eb9cf-115">Выберите в `Tokyo` списке " **географическое положение** "</span><span class="sxs-lookup"><span data-stu-id="eb9cf-115">Select `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
<!--  
## Feedback   

  
-->  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="eb9cf-116">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb9cf-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eb9cf-117">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="eb9cf-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="eb9cf-119">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb9cf-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
