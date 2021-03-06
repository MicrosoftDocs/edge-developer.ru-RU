---
description: Включить "Пометить сценарии контента в качестве кода библиотеки" > Framework Library Code.
title: Пометить сценарии контента как код библиотеки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ffc27cdd04ce28df888507fb2e1dc460d5bb4f21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398954"
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

# <a name="mark-content-scripts-as-library-code"></a>Пометить сценарии контента как код библиотеки  

При использовании **панели Источников** Microsoft Edge DevTools для прошаговки кода иногда приостанавливается использование кода, который не распознается. [][DevToolsJavascriptStepThroughCode]  Возможно, вы остановились на коде для одного из установленных расширений Microsoft Edge.  Выполните следующие действия, чтобы не приостанавлить код расширения.  

1.  Откройте DevTools, выберите Настройка и **управление DevTools** `...` \( \) > **параметров**.  Вы также можете открыть **Параметры,** выбрав `F1` .  

1.  Выберите панель **кода Библиотеки,** которая открывает раздел **"Параметры** кода библиотеки **Framework".**  
1.  Включи **сценарии контента Mark в качестве почтового ящика кода** библиотеки.  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Включить скрипты контента Mark в качестве почтового ящика кода Библиотеки" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       Включить **скрипты контента Mark в качестве почтового ящика кода** Библиотеки  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Шаг 4. Шаг через код . Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
