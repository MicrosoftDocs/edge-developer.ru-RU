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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a>Переопределение геолокации с помощью Microsoft Edge DevTools  

Многие веб-сайты пользуются расположением пользователей, чтобы обеспечить пользователям более релевантный опыт.  Например, веб-сайт погоды может показывать локальный прогноз в области пользователя, после того как пользователь предоставил веб-сайту разрешение на доступ к текущему расположению пользователя.  

<!--todo: add link to user location section when available -->  

Если вы строите пользовательский интерфейс, который изменяется в зависимости от того, где находится пользователь, вероятно, необходимо убедиться, что сайт ведет себя правильно в разных местах по всему миру.  Чтобы переопредить геолокацию в Microsoft Edge DevTools, выполните следующие действия.  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  `sensors`Введите, **выберите датчики show**и выберите `Enter` .  Средство **Sensors** открывается в нижней части окна DevTools.  
1.  Из списка **Geolocation** выберите один из заранее заранее выбранных городов, например, или выберите настраиваемое расположение, чтобы ввести настраиваемые координаты долготы и широты, или выберите расположение, недоступное для отображения того, как ведет себя ваш сайт, когда расположение пользователя `Tokyo` **** недоступно. ****  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Выберите Токио из списка Geolocation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Выберите `Tokyo` из **списка Geolocation**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
