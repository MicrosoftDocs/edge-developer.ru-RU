---
description: Имитация пониженного движения с помощью средств разработчика.
title: Имитация пониженного движения с помощью средств разработчика (CSS предпочитает пониженное движение)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230791"
---
# <span data-ttu-id="64943-104">Имитация пониженного движения</span><span class="sxs-lookup"><span data-stu-id="64943-104">Reduced Motion Simulation</span></span>  

<span data-ttu-id="64943-105">Анимация в веб-продуктах может быть проблемой с доступностью.</span><span class="sxs-lookup"><span data-stu-id="64943-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="64943-106">Операционные системы работают с этой проблемой, включив возможность отключить анимации, чтобы избежать путаницы пользователей и потенциальных проблем со здоровьем, например припадков.</span><span class="sxs-lookup"><span data-stu-id="64943-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="64943-107">В Интернете можно использовать запрос мультимедиа CSS с пониженным движением [prefers-reduced,][MDNPrefersReducedMotion] чтобы определить, предпочитают ли пользователи не видеть анимации.</span><span class="sxs-lookup"><span data-stu-id="64943-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="64943-108">В своем продукте вы можете упаковать код анимации в тест, чтобы избежать показа анимаций для затронутых пользователей.</span><span class="sxs-lookup"><span data-stu-id="64943-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="64943-109">С помощью [Microsoft Edge DevTools][DevtoolsIndex]вы можете имитировать этот параметр пониженного движения, не изменяя операционную систему.</span><span class="sxs-lookup"><span data-stu-id="64943-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="64943-110">Откройте меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="64943-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="64943-111">Выберите `Control` + `Shift` + `P` в Windows, Linux или `Command` + `Shift` + `P` macOS.</span><span class="sxs-lookup"><span data-stu-id="64943-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="64943-113">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="64943-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="64943-114">Введите `reduced` , чтобы включить и отключить имитацию.</span><span class="sxs-lookup"><span data-stu-id="64943-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="64943-115">Выберите этот параметр и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="64943-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включите или отключите предпочитаемую настройку пониженного движения в меню команд" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="64943-117">Включите или отключите **предпочитаемую настройку пониженного** движения в меню **команд**</span><span class="sxs-lookup"><span data-stu-id="64943-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="64943-118">Обновите текущую страницу, чтобы проверить, отключены ли анимации или они видны.</span><span class="sxs-lookup"><span data-stu-id="64943-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
