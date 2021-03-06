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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="36360-104">Пометить сценарии контента как код библиотеки</span><span class="sxs-lookup"><span data-stu-id="36360-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="36360-105">При использовании **панели Источников** Microsoft Edge DevTools для прошаговки кода иногда приостанавливается использование кода, который не распознается. [][DevToolsJavascriptStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="36360-105">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="36360-106">Возможно, вы остановились на коде для одного из установленных расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="36360-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="36360-107">Выполните следующие действия, чтобы не приостанавлить код расширения.</span><span class="sxs-lookup"><span data-stu-id="36360-107">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="36360-108">Откройте DevTools, выберите Настройка и **управление DevTools** `...` \( \) > **параметров**.</span><span class="sxs-lookup"><span data-stu-id="36360-108">Open DevTools, choose **Customize and control DevTools** \(`...`\) > **Settings**.</span></span>  <span data-ttu-id="36360-109">Вы также можете открыть **Параметры,** выбрав `F1` .</span><span class="sxs-lookup"><span data-stu-id="36360-109">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="36360-110">Выберите панель **кода Библиотеки,** которая открывает раздел **"Параметры** кода библиотеки **Framework".**</span><span class="sxs-lookup"><span data-stu-id="36360-110">Choose the **Library code** panel which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="36360-111">Включи **сценарии контента Mark в качестве почтового ящика кода** библиотеки.</span><span class="sxs-lookup"><span data-stu-id="36360-111">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Включить скрипты контента Mark в качестве почтового ящика кода Библиотеки" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="36360-113">Включить **скрипты контента Mark в качестве почтового ящика кода** Библиотеки</span><span class="sxs-lookup"><span data-stu-id="36360-113">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="36360-114">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="36360-114">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Шаг 4. Шаг через код . Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> <span data-ttu-id="36360-116">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="36360-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="36360-117">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="36360-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="36360-119">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="36360-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
