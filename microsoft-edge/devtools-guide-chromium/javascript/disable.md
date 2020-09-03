---
description: Открыть меню команд и выполнить команду "отключить JavaScript".
title: Отключение JavaScript с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992801"
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

Выполните описанные ниже действия, чтобы увидеть, как выглядит веб-страница и использует ее при отключении JavaScript.  

1.  [Откройте Microsoft Edge DevTools][DevToolsOpen].  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Меню команд" lightbox="../media/javascript-console-command.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Начните вводить текст, нажмите кнопку `javascript` **отключить JavaScript**, а затем нажмите `Enter` , чтобы выполнить команду.  JavaScript теперь отключен.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Выбор пункта "отключить JavaScript" в меню команд" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Выбор пункта " **отключить JavaScript** " в **меню команд**  
    :::image-end:::  
    
    Значок желтого предупреждения рядом с последующими **источниками** напоминает, что JavaScript отключен.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Значок предупреждения рядом с пунктом «источники»" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Значок предупреждения рядом с пунктом « **источники** »  
    :::image-end:::  
    
JavaScript остается отключенным на вкладке столько, сколько открыто DevTools.  

Возможно, потребуется перезагрузить страницу, чтобы проверить, зависит ли страница от JavaScript во время загрузки.  

Чтобы повторно включить JavaScript, выполните указанные ниже действия.  

*   Снова откройте **меню команд** и выполните `Enable JavaScript` команду.  
*   Закройте DevTools.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
