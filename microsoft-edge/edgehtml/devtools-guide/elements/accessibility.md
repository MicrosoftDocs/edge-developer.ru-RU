---
description: Использование средств accessibility для просмотра проверки и тестирования доступности страницы
title: Accessibility — DevTools (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, элементы, доступность
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5fd5f072f602cb8fa344df8124ee174f2a20aa5d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235379"
---
# <span data-ttu-id="4f823-104">Accessibility — DevTools (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4f823-104">Accessibility - DevTools (EdgeHTML)</span></span>  

<span data-ttu-id="4f823-105">Просмотр доступных свойств, присвоенных выбранному элементу.</span><span class="sxs-lookup"><span data-stu-id="4f823-105">View the accessible properties assigned to the selected element.</span></span> <span data-ttu-id="4f823-106">Наведите на любое из имен свойств описание того, как оно используется вспомогательными технологиями.</span><span class="sxs-lookup"><span data-stu-id="4f823-106">Hover over any of the property names for a description of how it's used by assistive technologies.</span></span> <span data-ttu-id="4f823-107">Можно также щелкнуть правой кнопкой мыши любое свойство, чтобы скопировать его значение в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="4f823-107">You can also right-click any property to copy its value to the clipboard.</span></span>

![Области доступности](../media/elements_accessibility.png)

<span data-ttu-id="4f823-109">Полезно открыть дерево доступности для перемещения по странице, как это было бы для чтения с экрана, а затем с помощью области "Accessibility" проверить сведения о свойствах, которые могут быть интересны. [](#accessibility-tree) \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f823-109">It's useful to open the [Accessibility tree](#accessibility-tree) to navigate around your page as a screen reader would, and then use the **Accessibility** pane to inspect details about accessibility properties of interest.</span></span>

## <span data-ttu-id="4f823-110">Дерево доступности</span><span class="sxs-lookup"><span data-stu-id="4f823-110">Accessibility tree</span></span>  

<span data-ttu-id="4f823-111">На \*\*\*\* древостройке "Доступность" показана структура страницы, которая будет отображаться для вспомогательных возможностей, таких как экранное устройство с экранным [диктором Windows.](https://support.microsoft.com/help/22798/windows-10-narrator-get-started)</span><span class="sxs-lookup"><span data-stu-id="4f823-111">The **Accessibility tree** pane shows the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screen reader.</span></span>

<span data-ttu-id="4f823-112">При щелчке по узлу в древовом представлении он также выбирается в [**дереве HTML**](../elements.md#html-tree-view)и наоборот.</span><span class="sxs-lookup"><span data-stu-id="4f823-112">Clicking on a node in the tree view will also select it in the [**HTML tree**](../elements.md#html-tree-view), and vice versa.</span></span> <span data-ttu-id="4f823-113">Выбор доступного элемента из *htmL-представлений* или дерева доступности также позволит получить дополнительные сведения о свойствах доступности в области инструментов \*\* "Accessibility". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f823-113">Selecting an accessible element from either the *HTML* or *Accessibility* tree views will also populate further accessibility property details in the **Accessibility** tool pane.</span></span> 

![Представление дерева доступности](../media/elements_accessibility_tree.png)

<!--  Here are further resources on [Accessibility with Microsoft Edge](../../accessibility.md).  -->  
