---
description: Узнайте, как создавать, проектировать и тестировать доступные веб-сайты в Microsoft Edge.
title: Специальные возможности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: accessibility, accessibility for developers, accessible websites, edge, web development, ARIA, developer, UIA, UI Automation
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235278"
---
# <span data-ttu-id="2e45e-104">Обзор специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="2e45e-104">Accessibility overview</span></span>  

> <span data-ttu-id="2e45e-105">"\[T\], влияние ограниченных возможностей значительно изменилось в Интернете, так как Интернет устраняет барьеры на пути к взаимодействию и взаимодействию, с которых сталкиваются многие люди в физическом мире".</span><span class="sxs-lookup"><span data-stu-id="2e45e-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="2e45e-106">(Accessibility | W3C)</span><span class="sxs-lookup"><span data-stu-id="2e45e-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="2e45e-107">В [Всемирной организации здравоохранения][WHODisabilities] ограниченные возможности определяются как "несоответствие во взаимодействии между функциями тела человека и функциями среды, в которой он содержится".</span><span class="sxs-lookup"><span data-stu-id="2e45e-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="2e45e-108">Ограниченные возможности могут варьироваться от сиюмитных ограничений, таких как ограниченная мобильность при удержании детей или яркого света на телефоне, до других физических, аудиторных, визуальных или возрастных нарушений.</span><span class="sxs-lookup"><span data-stu-id="2e45e-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="2e45e-109">Разработка веб-сайтов и других технологий для включения создает у каждого человека простое впечатление.</span><span class="sxs-lookup"><span data-stu-id="2e45e-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="2e45e-110">Инклюзивное проектирование и доступность веб-возможностей расширяют возможности и помогают всем использовать Интернет.</span><span class="sxs-lookup"><span data-stu-id="2e45e-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="2e45e-111">Вот несколько лучших методик, примеров кода и дополнительных ресурсов, которые [][AccessibilityBuild]вы можете [][AccessibilityTest] получить, чтобы узнать больше о проектировании, [][AccessibilityDesign]создании и тестировании доступных веб-сайтов в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2e45e-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="2e45e-112">Доступность в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2e45e-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="2e45e-113">В Microsoft Edge мы представили современный [API автоматизации][WindowsWin32AutoEntryui] пользовательского интерфейса \(API UIA\).</span><span class="sxs-lookup"><span data-stu-id="2e45e-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="2e45e-114">Изменение UIA стало главной инвестицией в доступность браузера и лежит в основе более инклюзивного веб-приложения для пользователей, которые зависят от вспомогательных возможностей в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2e45e-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="2e45e-115">Пользователи также получают преимущества из-за постоянной природы поддвижки Chromium.</span><span class="sxs-lookup"><span data-stu-id="2e45e-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="2e45e-116">Система доступности в Microsoft Edge изначально поддерживает современные веб-стандарты, включая ARIA, HTML5 и CSS3.</span><span class="sxs-lookup"><span data-stu-id="2e45e-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="2e45e-117">На следующей схеме упрощенного конвейера браузера содержимое веб-страниц передается на доступный уровень презентации.</span><span class="sxs-lookup"><span data-stu-id="2e45e-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="Содержимое, преобразованное в модель обдвижки, проецируется в визуальные представления и представления с специальными специальными возможностей, представленные в качестве визуальной или доступной презентации":::
   <span data-ttu-id="2e45e-119">Содержимое, преобразованное в модель обдвижки, проецируется в визуальные представления и представления с доступом, которые представлены как визуальные или доступные презентации</span><span class="sxs-lookup"><span data-stu-id="2e45e-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="2e45e-120">Команда Microsoft Edge постоянно работает с W3C и другими поставщиками браузеров, чтобы убедиться, что новые функции веб-платформы имеют достаточные встроенные возможности доступа.</span><span class="sxs-lookup"><span data-stu-id="2e45e-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="2e45e-121">Сведения о том, какие новые функции HTML5 доступны в Microsoft Edge, можно найти в [htmL5Accessibility.][HTML5Accessibility]</span><span class="sxs-lookup"><span data-stu-id="2e45e-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="2e45e-122">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e45e-122">Resources</span></span>  

#### <span data-ttu-id="2e45e-123">Блог по автоматизации пользовательского интерфейса Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="2e45e-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="2e45e-124">Блог ["Автоматизация пользовательского][ArchiveBlogsWinuiautomation] интерфейса Microsoft Windows" охватывает темы, связанные с API автоматизации Windows.</span><span class="sxs-lookup"><span data-stu-id="2e45e-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="2e45e-125">Web Accessibility Initiative (WAI)</span><span class="sxs-lookup"><span data-stu-id="2e45e-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="2e45e-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span><span class="sxs-lookup"><span data-stu-id="2e45e-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="2e45e-127">Сайт предоставляет множество ресурсов [][W3CWaiGettingstartedOverview]для начала работы со специальными веб-ресурсами, проектирования для [включения,][W3CWaiFundamentals]учебников и [презентаций][W3CWaiTeachAdvocate]и многого другого.</span><span class="sxs-lookup"><span data-stu-id="2e45e-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Создание доступных веб-сайтов | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Разработка доступных веб-сайтов | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Тестирование доступности | Документы Майкрософт"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Автоматизация пользовательского интерфейса | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Блог по автоматизации пользовательского интерфейса Microsoft Windows | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Доступность HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accessibility | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Введение в веб-доступность | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Начало работы: обеспечение доступности веб-сайта | Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Web Accessibility Initiative (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Общие сведения об обучения и адвокате | Web Accessibility Initiative (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Ограниченные возможности | WHO"  

