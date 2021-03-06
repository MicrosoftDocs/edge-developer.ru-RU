---
description: Откройте командное меню и запустите команду "Отключить JavaScript".
title: Отключение JavaScript с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2067944fa17c332dd15ffb3ef97afe02d35685ed
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398562"
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

# <a name="disable-javascript-with-microsoft-edge-devtools"></a>Отключение JavaScript с помощью Microsoft Edge DevTools  

Выполните следующие действия, чтобы отобразить внешний вид и поведение веб-страницы при отключении JavaScript.  

1.  [Откройте Microsoft Edge DevTools][DevToolsOpen].  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Меню команд" lightbox="../media/javascript-console-command.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  Начните `javascript` печатать, **выберите отключить JavaScript,** а затем выберите для запуска `Enter` команды.  JavaScript теперь отключен.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Выберите отключение JavaScript в командном меню" lightbox="../media/javascript-console-command-javascript.msft.png":::
       Выберите **отключение JavaScript** в **командном меню**  
    :::image-end:::  
    
    Желтый значок предупреждения рядом с **Источниками** напоминает, что JavaScript отключен.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Значок предупреждения рядом с источниками" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Значок предупреждения рядом с **источниками**  
    :::image-end:::  
    
JavaScript остается отключенным на вкладке до тех пор, пока у вас открыты DevTools.  

Может потребоваться обновить страницу, чтобы просмотреть, зависит ли веб-страница от JavaScript во время загрузки.  

Чтобы повторно включить JavaScript, выполните следующие действия.  

*   Откройте **командное меню** снова и запустите `Enable JavaScript` команду.  
*   Закрой DevTools.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
