---
description: Перемещение Microsoft Edge DevTools в нижней или левой части представления или в отдельное окно.
title: Изменение размещения Microsoft Edge DevTools (Undock, Dock to Bottom, Dock to Left)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e3160999a1072afffdc5c5d44f8fc60fab65d264
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399044"
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

# <a name="change-microsoft-edge-devtools-placement-undock-dock-to-bottom-dock-to-left"></a><span data-ttu-id="32333-104">Изменение размещения Microsoft Edge DevTools (Undock, Dock to Bottom, Dock to Left)</span><span class="sxs-lookup"><span data-stu-id="32333-104">Change Microsoft Edge DevTools placement (Undock, Dock To Bottom, Dock To Left)</span></span>  

<span data-ttu-id="32333-105">По умолчанию DevTools пришвартовано справа от вашего viewport.</span><span class="sxs-lookup"><span data-stu-id="32333-105">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="32333-106">Вы также можете пристыковаться к нижнему, док-станции слева или отстыковать DevTools к отдельному окну.</span><span class="sxs-lookup"><span data-stu-id="32333-106">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-right-docked.msft.png" alt-text="Выбор док-станции влево" lightbox="../media/customize-elements-styles-right-docked.msft.png":::
         <span data-ttu-id="32333-108">Выбрать</span><span class="sxs-lookup"><span data-stu-id="32333-108">Choose</span></span> `Dock To Left`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-bottom-docked.msft.png" alt-text="Выбор док-станции донизу" lightbox="../media/customize-elements-styles-bottom-docked.msft.png":::
         <span data-ttu-id="32333-110">Выбрать</span><span class="sxs-lookup"><span data-stu-id="32333-110">Choose</span></span> `Dock To Bottom`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png" alt-text="Браузер в отдельном окне" lightbox="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png":::
         <span data-ttu-id="32333-112">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="32333-112">Browser in separate window</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png" alt-text="Незаблокировали DevTools в отдельном окне" lightbox="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png":::
         <span data-ttu-id="32333-114">Незаблокировали DevTools в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="32333-114">Undocked DevTools in separate window</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="change-placement-from-the-main-menu"></a><span data-ttu-id="32333-115">Изменение размещения из основного меню</span><span class="sxs-lookup"><span data-stu-id="32333-115">Change placement from the main menu</span></span>  

1.  <span data-ttu-id="32333-116">Выберите настройка и управление **DevTools** \( \) и выберите Undock в отдельное окно `...` \( \*\*\*\* ![ Undock \), dock to Bottom \( Dock to ][ImageUndockIcon] **Bottom** ![ \), ][ImageBottomIcon] \*\*\*\* ![ или ][ImageLeftIcon] стыковка налево \( Стыковка слева \).</span><span class="sxs-lookup"><span data-stu-id="32333-116">Choose **Customize And Control DevTools** \(`...`\) and choose **Undock Into Separate Window** \(![Undock][ImageUndockIcon]\), **Dock To Bottom** \(![Dock To Bottom][ImageBottomIcon]\), or **Dock To Left** \(![Dock To Left][ImageLeftIcon]\).</span></span>  
    
    :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight.msft.png" alt-text="Выберите Undock в отдельное окно" lightbox="../media/customize-elements-styles-options-dock-side-highlight.msft.png":::
       <span data-ttu-id="32333-118">Выберите **Undock в отдельное окно**</span><span class="sxs-lookup"><span data-stu-id="32333-118">Choose **Undock Into Separate Window**</span></span>  
    :::image-end:::  
    
## <a name="change-placement-from-the-command-menu"></a><span data-ttu-id="32333-119">Изменение размещения из меню команды</span><span class="sxs-lookup"><span data-stu-id="32333-119">Change placement from the Command Menu</span></span>  

1.  <span data-ttu-id="32333-120">[Откройте командное меню.][DevtoolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="32333-120">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="32333-121">Запустите одну из следующих команд: `Dock To Bottom` , `Undock Into Separate Window` .</span><span class="sxs-lookup"><span data-stu-id="32333-121">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="32333-122">В настоящее время нет команды для стыковки слева, но вы можете получить доступ к ней из [основного меню](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="32333-122">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    :::image type="complex" source="../media/customize-elements-styles-command-menu-undo.msft.png" alt-text="Команда отсоединого" lightbox="../media/customize-elements-styles-command-menu-undo.msft.png":::
       <span data-ttu-id="32333-124">Команда отсоединого</span><span class="sxs-lookup"><span data-stu-id="32333-124">The undock command</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="32333-125">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="32333-125">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageUndockIcon]: ../media/undock-icon.msft.png  
[ImageBottomIcon]: ../media/bottom-icon.msft.png  
[ImageLeftIcon]: ../media/left-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="32333-127">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32333-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="32333-128">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/customize/placement) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="32333-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="32333-130">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32333-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
