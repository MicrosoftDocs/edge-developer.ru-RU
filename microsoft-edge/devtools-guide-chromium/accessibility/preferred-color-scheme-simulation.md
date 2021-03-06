---
description: Привяжь Microsoft Edge DevTools в режим предварительного просмотра цветовой схемы.
title: Force Microsoft Edge DevTools в режиме предварительного просмотра цветовой схемы (CSS предпочитает цветовую схему)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 84f482605acd6edab6829e00d5fa31f927ebc032
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398303"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="2b61a-104">Моделирование темной или светлой цветовой схемы</span><span class="sxs-lookup"><span data-stu-id="2b61a-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="2b61a-105">Операционные системы могут отображать любое приложение в более темных или более светлых цветах.</span><span class="sxs-lookup"><span data-stu-id="2b61a-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="2b61a-106">Наличие веб-продукта с легкой темой в операционной системе темного режима является натертым и может быть проблемой доступности для некоторых пользователей.</span><span class="sxs-lookup"><span data-stu-id="2b61a-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="2b61a-107">В Интернете можно использовать [][MDNPrefersColorScheme] запрос CSS Media Query с предпочитаемой цветовой схемой, чтобы определить, предпочитают ли пользователи отображать ваш продукт в более темной или светлой цветовой схеме.</span><span class="sxs-lookup"><span data-stu-id="2b61a-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to display your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="2b61a-108">Используйте [Microsoft Edge DevTools][DevtoolsIndex] для имитации изменения из темно-светлого режима без изменения всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2b61a-108">Use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="2b61a-109">Откройте **командное меню.**</span><span class="sxs-lookup"><span data-stu-id="2b61a-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="2b61a-110">Выберите `Control` + `Shift` + `P` \(Windows/Linux\) `Command` + `Shift` + `P` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2b61a-110">Select `Control`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="2b61a-112">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="2b61a-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="2b61a-113">Введите , выберите эмулировать `emulate color` **CSS предпочитает-цветовой схемы:** темные или эмулировать **CSS предпочитает-цветовой схемы:** свет, а затем выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="2b61a-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Параметр цветовой схемы из Меню команды" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="2b61a-115">Параметр цветовой схемы **из Меню** команды</span><span class="sxs-lookup"><span data-stu-id="2b61a-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="2b61a-116">Просто `dark` введите или не раскроет нужный инструмент, так как существует также способ выбрать тему `light` [для DevTools][DevtoolsCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="2b61a-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="2b61a-117">Если вам интересно, что выбрать, убедитесь, \*\*\*\* что вы выбираете элемент меню отрисовки, а не **элемент меню** внешнего вида.</span><span class="sxs-lookup"><span data-stu-id="2b61a-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="2b61a-118">После выбора цветовой схемы обновите текущий документ, чтобы отобразить смоделированный режим.</span><span class="sxs-lookup"><span data-stu-id="2b61a-118">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Режим имитации освещения в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="2b61a-120">Режим имитации освещения в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2b61a-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="2b61a-121">Просмотр и изменение CSS, как и любой другой веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="2b61a-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="2b61a-122">Дополнительные сведения, перейдите к [началу работы с просмотром и изменением CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="2b61a-122">For more information, navigate to [Get Started With Viewing And Changing CSS][DevtoolsCssIndex].</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
