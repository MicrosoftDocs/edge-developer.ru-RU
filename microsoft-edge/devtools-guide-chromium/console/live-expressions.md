---
description: Если вы находите, что введите те же выражения JavaScript в консоль несколько раз, попробуйте Live Expressions вместо этого.
title: Просмотр значений выражений JavaScript в режиме реального времени с помощью Live Expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: af920de1c395489dc09b83f3cc0f24814c4f5cbe
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439228"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a><span data-ttu-id="c3e48-104">Просмотр значений выражений JavaScript в режиме реального времени с помощью Live Expressions</span><span class="sxs-lookup"><span data-stu-id="c3e48-104">Watch JavaScript expression values in real-time with Live Expressions</span></span>  

<span data-ttu-id="c3e48-105">Если вы напечатаете одно и то же выражение JavaScript в консоли несколько раз, вам может быть проще создать **выражение Live.**</span><span class="sxs-lookup"><span data-stu-id="c3e48-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="c3e48-106">С **помощью Live Expressions** вы введите выражение один раз, а затем прикрепите его к верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="c3e48-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="c3e48-107">Значение обновлений выражения почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="c3e48-107">The value of the expression updates in near real-time.</span></span>  

## <a name="create-a-live-expression"></a><span data-ttu-id="c3e48-108">Создание live expression</span><span class="sxs-lookup"><span data-stu-id="c3e48-108">Create a Live Expression</span></span>  

1.  <span data-ttu-id="c3e48-109">[Откройте консоль.][DevToolsConsoleReferenceOpenConsole]</span><span class="sxs-lookup"><span data-stu-id="c3e48-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="c3e48-110">Выберите **Создать живое выражение** \. ![ Создайте живое ](../media/create-live-expression-icon.msft.png) выражение \).</span><span class="sxs-lookup"><span data-stu-id="c3e48-110">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  <span data-ttu-id="c3e48-111">Появится текстовое поле **Live Expression.**</span><span class="sxs-lookup"><span data-stu-id="c3e48-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Ввод document.activeElement в текстовом окне Live Expression" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="c3e48-113">Ввод `document.activeElement` текста **в текстовом окне Live Expression**</span><span class="sxs-lookup"><span data-stu-id="c3e48-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c3e48-114">Выберите `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` или \(macOS\) \*\*\*\* для сохранения выражения или выберите вне текстового ящика Live Expression.</span><span class="sxs-lookup"><span data-stu-id="c3e48-114">Select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\) to save the expression, or choose outside of the **Live Expression** textbox.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c3e48-115">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c3e48-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Откройте консоль — справочный | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="c3e48-117">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3e48-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c3e48-118">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="c3e48-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c3e48-120">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c3e48-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
