---
Description: Принудительное принудительное переналадка Microsoft Edge DevTools в режим просмотра цветовой схемы.
title: Принудительное принудительное перенаполнитель microsoft Edge DevTools в режим просмотра цветовой схемы (CSS предпочитает цветовую схему)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 29b0121a616a037fa11b61799efeffd201eb1821
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230798"
---
# <span data-ttu-id="83dcf-104">Моделирование темной или светлой цветовой схемы</span><span class="sxs-lookup"><span data-stu-id="83dcf-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="83dcf-105">Операционные системы могут отображать любые приложения в более темных или светлых цветах.</span><span class="sxs-lookup"><span data-stu-id="83dcf-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="83dcf-106">Наличие веб-продукта с светлой темой в операционной системе в темном режиме очень важно и может быть проблемой с доступностью для некоторых пользователей.</span><span class="sxs-lookup"><span data-stu-id="83dcf-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="83dcf-107">В Интернете можно использовать запрос мультимедиа CSS [prefers-color-scheme,][MDNPrefersColorScheme] чтобы определить, предпочитают ли пользователи видеть ваш продукт в схеме темной или светлой цветовой схемы.</span><span class="sxs-lookup"><span data-stu-id="83dcf-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="83dcf-108">Используйте [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] для имитации изменения режима темного на светлый без изменения всей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83dcf-108">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="83dcf-109">Откройте меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="83dcf-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="83dcf-110">Выберите `Control` + `Shift` + `P` в Windows, Linux или `Command` + `Shift` + `P` macOS.</span><span class="sxs-lookup"><span data-stu-id="83dcf-110">Select `Control`+`Shift`+`P`  on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="83dcf-112">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="83dcf-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="83dcf-113">Type `emulate color` , choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="83dcf-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Параметр цветовой схемы из меню команд" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="83dcf-115">Параметр цветовой схемы из **меню команд**</span><span class="sxs-lookup"><span data-stu-id="83dcf-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="83dcf-116">Просто введите или не раскрывают нужное средство, так как существует также способ выбрать тему `dark` `light` для [DevTools.][DevtoolsGuideChromiumCustomizeDarkTheme]</span><span class="sxs-lookup"><span data-stu-id="83dcf-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="83dcf-117">Если вы хотите узнать, что выбрать, убедитесь, что вы выбираете элемент меню визуализации, а не элемент меню **внешнего** вида. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83dcf-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="83dcf-118">После выбора цветовой схемы перезагрузить текущий документ, чтобы увидеть имитированный режим.</span><span class="sxs-lookup"><span data-stu-id="83dcf-118">After you choose a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Режим имитации освещения в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="83dcf-120">Режим имитации освещения в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="83dcf-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="83dcf-121">Просматривайте и изменяйте CSS, как и любую другую веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="83dcf-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="83dcf-122">Дополнительные сведения см. в теме ["Начало работы с просмотром и изменением CSS".][DevtoolsGuideChromiumCssIndex]</span><span class="sxs-lookup"><span data-stu-id="83dcf-122">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
