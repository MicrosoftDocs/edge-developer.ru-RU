---
description: Откройте консоль, создайте живое выражение и установите выражение document.activeElement.
title: Отслеживание элемента с фокусом
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3f3e59c4ee6f10b8e162f30efbff337ca2beec8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398317"
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

# <a name="track-which-element-has-focus"></a><span data-ttu-id="8ebaa-104">Отслеживание элемента с фокусом</span><span class="sxs-lookup"><span data-stu-id="8ebaa-104">Track which element has focus</span></span>  

<span data-ttu-id="8ebaa-105">Предположим, что вы тестируете доступность навигации по клавиатуре страницы.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="8ebaa-106">При навигации по странице с ключом кольцо фокуса иногда исчезает, так как элемент с `Tab` фокусом скрыт.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="8ebaa-107">Выполните следующие действия для отслеживания сфокусированного элемента в DevTools.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="8ebaa-108">Откройте **консоль.**</span><span class="sxs-lookup"><span data-stu-id="8ebaa-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="8ebaa-109">Выберите **Создать живое выражение** \. ![ Создайте живое ][ImageCreateIcon] выражение \).</span><span class="sxs-lookup"><span data-stu-id="8ebaa-109">Choose **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Создание live expression" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="8ebaa-111">Создание live expression</span><span class="sxs-lookup"><span data-stu-id="8ebaa-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="8ebaa-112">Введите `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="8ebaa-113">Чтобы сохранить, выберите вне пользовательского интерфейса **Live Expression.**</span><span class="sxs-lookup"><span data-stu-id="8ebaa-113">Choose outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="8ebaa-114">Показанное ниже `document.activeElement` значение является результатом выражения.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="8ebaa-115">Так как это выражение всегда представляет собой сфокусированный элемент, теперь у вас есть способ всегда отслеживать, какой элемент имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="8ebaa-116">Наведите курсор на результат, чтобы выделить фокусный элемент в представлении.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="8ebaa-117">Наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите панель **Reveal in Elements,** чтобы показать элемент дерева DOM на средстве **Elements.**</span><span class="sxs-lookup"><span data-stu-id="8ebaa-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="8ebaa-118">Наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Store** в качестве глобальной переменной, чтобы создать переменную ссылку на узел, который можно использовать в **консоли.**</span><span class="sxs-lookup"><span data-stu-id="8ebaa-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8ebaa-119">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ebaa-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="8ebaa-120">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8ebaa-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8ebaa-121">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="8ebaa-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8ebaa-123">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8ebaa-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
