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

# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a><span data-ttu-id="00934-104">Запуск команд с помощью меню Команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="00934-104">Run commands with the Microsoft Edge DevTools Command menu</span></span>  

<span data-ttu-id="00934-105">Командное меню обеспечивает быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения общих задач, таких как отключение [JavaScript.][JavascriptDisable]</span><span class="sxs-lookup"><span data-stu-id="00934-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="00934-106">Вы можете быть знакомы с аналогичной функцией в Microsoft Visual Studio Code под названием [Командная][VisualStudioCodeUICommandPalette]палитра , которая была первоначальной вдохновением для командного меню.</span><span class="sxs-lookup"><span data-stu-id="00934-106">You may be familiar with a similar feature in Microsoft Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Использование командного меню для отключения JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="00934-108">Использование командного меню для отключения JavaScript</span><span class="sxs-lookup"><span data-stu-id="00934-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <a name="open-the-command-menu"></a><span data-ttu-id="00934-109">Откройте меню команд</span><span class="sxs-lookup"><span data-stu-id="00934-109">Open the Command Menu</span></span>  

<span data-ttu-id="00934-110">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="00934-110">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="00934-111">Или выберите настраивать и **управлять DevTools** `...` \( \) > **run Command**.</span><span class="sxs-lookup"><span data-stu-id="00934-111">Or choose **Customize And Control DevTools** \(`...`\) > **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Командный запуск" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="00934-113">Командный запуск</span><span class="sxs-lookup"><span data-stu-id="00934-113">Run Command</span></span>  
:::image-end:::  

## <a name="display-other-available-actions"></a><span data-ttu-id="00934-114">Отображение других доступных действий</span><span class="sxs-lookup"><span data-stu-id="00934-114">Display other available actions</span></span>  

<span data-ttu-id="00934-115">Если вы используете рабочий процесс, описанный в меню [Open the Command,](#open-the-command-menu)меню команд открывается с помощью символа, предварительно заранее задаваемого в `>` текстовое поле Меню команд.</span><span class="sxs-lookup"><span data-stu-id="00934-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Символ команды" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="00934-117">Символ команды</span><span class="sxs-lookup"><span data-stu-id="00934-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="00934-118">Удалите `>` символ и тип, чтобы `?` отобразить другие действия, доступные в командном меню.</span><span class="sxs-lookup"><span data-stu-id="00934-118">Delete the `>` character and type `?` to display other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Другие доступные действия" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="00934-120">Другие доступные действия</span><span class="sxs-lookup"><span data-stu-id="00934-120">Other available actions</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="00934-121">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="00934-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Отключить JavaScript с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Палитра команд — Visual Studio пользовательского интерфейса кода"  

> [!NOTE]
> <span data-ttu-id="00934-124">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="00934-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="00934-125">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="00934-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="00934-127">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="00934-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
