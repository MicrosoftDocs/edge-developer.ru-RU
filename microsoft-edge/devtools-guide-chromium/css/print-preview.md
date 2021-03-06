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

# <a name="force-microsoft-edge-devtools-into-print-preview-mode"></a>Force Microsoft Edge DevTools в режиме предварительного просмотра печати  

Запрос [печатных средств массовой][MDNUsingMediaQueries] информации контролирует внешний вид страницы при печати.  Чтобы принудить страницу к режиму предварительного просмотра печати:  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  `rendering`Введите, **выберите показать визуализацию,** а затем выберите `Enter` .  
1.  Под **эмулировать CSS-носителю**выберите **печать**.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Режим предварительного просмотра печати" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Режим предварительного просмотра печати  
    :::image-end:::  
    
Отсюда можно отобразить и изменить CSS, как и любую другую веб-страницу.  [Перейдите, чтобы начать с просмотра и изменения CSS][DevToolsCSSGetStarted].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ./index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
