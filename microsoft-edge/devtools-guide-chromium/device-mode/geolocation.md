---
description: Откройте средство Датчики и выберите координаты из списка Geolocation.
title: Переопределение геолокации с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8f6ad09b2f8db110f6743aae32e16cc9b1185400
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399003"
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a><span data-ttu-id="90294-104">Переопределение геолокации с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="90294-104">Override geolocation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="90294-105">Многие веб-сайты пользуются расположением пользователей, чтобы обеспечить пользователям более релевантный опыт.</span><span class="sxs-lookup"><span data-stu-id="90294-105">Many websites take advantage of user location in order to provide a more relevant experience for the users.</span></span>  <span data-ttu-id="90294-106">Например, веб-сайт погоды может показывать локальный прогноз в области пользователя, после того как пользователь предоставил веб-сайту разрешение на доступ к текущему расположению пользователя.</span><span class="sxs-lookup"><span data-stu-id="90294-106">For example, a weather website may show the local forecast in a user's area, after the user has granted the website permission to access the current user location.</span></span>  

<!--todo: add link to user location section when available -->  

<span data-ttu-id="90294-107">Если вы строите пользовательский интерфейс, который изменяется в зависимости от того, где находится пользователь, вероятно, необходимо убедиться, что сайт ведет себя правильно в разных местах по всему миру.</span><span class="sxs-lookup"><span data-stu-id="90294-107">If you are building a UI that changes depending on where the user is located, you probably want to make sure that the site behaves correctly in different places around the world.</span></span>  <span data-ttu-id="90294-108">Чтобы переопредить геолокацию в Microsoft Edge DevTools, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="90294-108">To override your geolocation in Microsoft Edge DevTools, complete the following actions.</span></span>  

1.  <span data-ttu-id="90294-109">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**</span><span class="sxs-lookup"><span data-stu-id="90294-109">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="90294-111">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="90294-111">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="90294-112">`sensors`Введите, **выберите датчики show**и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="90294-112">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="90294-113">Средство **Sensors** открывается в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="90294-113">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="90294-114">Из списка **Geolocation** выберите один из заранее заранее выбранных городов, например, или выберите настраиваемое расположение, чтобы ввести настраиваемые координаты долготы и широты, или выберите расположение, недоступное для отображения того, как ведет себя ваш сайт, когда расположение пользователя `Tokyo` \*\*\*\* недоступно. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="90294-114">From the **Geolocation** list select one of the preset cities, like `Tokyo`, or choose **Custom location** to enter custom longitude and latitude coordinates, or choose **Location unavailable** to display how your site behaves when the user's location is not available.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Выберите Токио из списка Geolocation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       <span data-ttu-id="90294-116">Выберите `Tokyo` из **списка Geolocation**</span><span class="sxs-lookup"><span data-stu-id="90294-116">Choose `Tokyo` from the **Geolocation** list</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="90294-117">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="90294-117">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> <span data-ttu-id="90294-118">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90294-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="90294-119">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="90294-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="90294-121">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="90294-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
