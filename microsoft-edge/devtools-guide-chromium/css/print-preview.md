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

# Принудительное переведите Microsoft Edge DevTools в режим предварительного просмотра печати (тип мультимедиа CSS Print)  

Запрос [на печать мультимедиа][MDNUsingMediaQueries] управляет тем, как выглядит страница при печати.  Чтобы принудительно перенадействовать страницу в режим предварительного просмотра:  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  `rendering`Введите, **выберите "Показать отрисовку"** и выберите `Enter` .  
1.  В **эмуляции CSS-носите**выберите **"Печать".**  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Режим предварительного просмотра" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Режим предварительного просмотра  
    :::image-end:::  
    
Здесь вы можете просматривать и изменять CSS, как и любую другую веб-страницу.  Перейдите [к началу работы с просмотром и изменением CSS.][DevToolsCSSGetStarted]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ./index.md "Начало просмотра и изменения CSS | Документы Майкрософт"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
