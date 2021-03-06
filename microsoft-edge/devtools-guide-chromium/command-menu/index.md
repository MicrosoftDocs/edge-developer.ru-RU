---
description: Руководство о том, как открыть командное меню, запустить команды, просмотреть другие действия и другие действия.
title: Запуск команд с помощью меню Команды Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a9e67815f69a44d3bd2a741738b04c7170f6ac15
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398030"
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

# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a>Запуск команд с помощью меню Команды Microsoft Edge DevTools  

Командное меню обеспечивает быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения общих задач, таких как отключение [JavaScript.][JavascriptDisable]  Вы можете быть знакомы с аналогичной функцией в Microsoft Visual Studio Code под названием [Командная][VisualStudioCodeUICommandPalette]палитра , которая была первоначальной вдохновением для командного меню.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Использование командного меню для отключения JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Использование командного меню для отключения JavaScript  
:::image-end:::  

## <a name="open-the-command-menu"></a>Откройте меню команд  

Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\). Или выберите настраивать и **управлять DevTools** `...` \( \) > **run Command**.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Командный запуск" lightbox="../media/command-menu-options-run-command.msft.png":::
   Командный запуск  
:::image-end:::  

## <a name="display-other-available-actions"></a>Отображение других доступных действий  

Если вы используете рабочий процесс, описанный в меню [Open the Command,](#open-the-command-menu)меню команд открывается с помощью символа, предварительно заранее задаваемого в `>` текстовое поле Меню команд.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Символ команды" lightbox="../media/command-menu-run-command.msft.png":::
   Символ команды  
:::image-end:::  

Удалите `>` символ и тип, чтобы `?` отобразить другие действия, доступные в командном меню.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Другие доступные действия" lightbox="../media/command-menu-help.msft.png":::
   Другие доступные действия  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Отключить JavaScript с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Палитра команд — Visual Studio пользовательского интерфейса кода"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
