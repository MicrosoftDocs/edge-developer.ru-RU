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

# Отключение JavaScript с помощью Microsoft Edge DevTools  

Выполните следующие действия, чтобы увидеть, как выглядит и работает веб-страница при отключаемом JavaScript.  

1.  [Откройте Microsoft Edge DevTools.][DevToolsOpen]  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Меню команд" lightbox="../media/javascript-console-command.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  Начните `javascript` вводить текст, **выберите "Отключить JavaScript",** а затем `Enter` выберите команду.  JavaScript теперь отключен.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Выберите Отключить JavaScript в меню команд" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Выберите **"Отключить JavaScript"** в меню **команд**  
    :::image-end:::  
    
    Желтый значок предупреждения рядом с **"Источники"** напоминает, что JavaScript отключен.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Значок предупреждения рядом с источниками" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Значок предупреждения рядом с **источниками**  
    :::image-end:::  
    
JavaScript остается отключенным на вкладке до тех пор, пока вы открыли DevTools.  

Может потребоваться перезагрузить страницу, чтобы узнать, зависит ли страница от JavaScript во время загрузки.  

Чтобы повторно включить JavaScript, выполните следующие действия.  

*   Снова откройте **меню команд** и запустите `Enable JavaScript` команду.  
*   Закроем DevTools.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
