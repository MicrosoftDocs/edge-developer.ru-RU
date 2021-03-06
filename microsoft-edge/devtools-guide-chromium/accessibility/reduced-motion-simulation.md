---
description: Имитация уменьшенного движения с помощью средств разработчика.
title: Имитация уменьшенного движения с помощью средств разработчика (CSS предпочитает уменьшенное движение)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397869"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="53473-104">Имитация уменьшенного движения</span><span class="sxs-lookup"><span data-stu-id="53473-104">Reduced motion simulation</span></span>  

<span data-ttu-id="53473-105">Анимация в веб-продуктах может быть проблемой доступности.</span><span class="sxs-lookup"><span data-stu-id="53473-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="53473-106">Операционные системы работают с этой проблемой, включив возможность отключить анимацию, чтобы избежать путаницы пользователей и потенциальных проблем со здоровьем, таких как запуск изъятий.</span><span class="sxs-lookup"><span data-stu-id="53473-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="53473-107">В Интернете можно использовать [][MDNPrefersReducedMotion] запрос CSS Media Query с пониженным движением, чтобы определить, предпочитают ли пользователи не запускать и не отображать анимацию.</span><span class="sxs-lookup"><span data-stu-id="53473-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not run or display any animations.</span></span>  <span data-ttu-id="53473-108">В продукте можно завернуть код анимации в тест, чтобы не показывать анимации для пострадавших пользователей.</span><span class="sxs-lookup"><span data-stu-id="53473-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="53473-109">С помощью [Microsoft Edge DevTools][DevtoolsIndex]можно смоделировать этот параметр уменьшенного движения, не меняя операционную систему.</span><span class="sxs-lookup"><span data-stu-id="53473-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="53473-110">Откройте **командное меню.**</span><span class="sxs-lookup"><span data-stu-id="53473-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="53473-111">Выберите `Control` + `Shift` + `P` в Windows/Linux или `Command` + `Shift` + `P` на macOS.</span><span class="sxs-lookup"><span data-stu-id="53473-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="53473-113">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="53473-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="53473-114">`reduced`Введите, чтобы включить и отключить моделирование.</span><span class="sxs-lookup"><span data-stu-id="53473-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="53473-115">Выберите параметр и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="53473-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включите или отключите параметры с пониженным движением из командного меню" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="53473-117">Включите или отключите параметры с **пониженным движением** из **командного меню**</span><span class="sxs-lookup"><span data-stu-id="53473-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="53473-118">Обновите текущую страницу, чтобы проверить, отключены ли анимации или видны.</span><span class="sxs-lookup"><span data-stu-id="53473-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "предпочитает уменьшенное движение | MDN"  
