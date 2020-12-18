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
# Имитация пониженного движения  

Анимация в веб-продуктах может быть проблемой с доступностью.  Операционные системы работают с этой проблемой, включив возможность отключить анимации, чтобы избежать путаницы пользователей и потенциальных проблем со здоровьем, например припадков.  В Интернете можно использовать запрос мультимедиа CSS с пониженным движением [prefers-reduced,][MDNPrefersReducedMotion] чтобы определить, предпочитают ли пользователи не видеть анимации.  В своем продукте вы можете упаковать код анимации в тест, чтобы избежать показа анимаций для затронутых пользователей.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

С помощью [Microsoft Edge DevTools][DevtoolsIndex]вы можете имитировать этот параметр пониженного движения, не изменяя операционную систему.  

1.  Откройте меню **команд.**  
    1.  Выберите `Control` + `Shift` + `P` в Windows, Linux или `Command` + `Shift` + `P` macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Меню **команд**  
        :::image-end:::  
        
1.  Введите `reduced` , чтобы включить и отключить имитацию.  Выберите этот параметр и выберите `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включите или отключите предпочитаемую настройку пониженного движения в меню команд" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Включите или отключите **предпочитаемую настройку пониженного** движения в меню **команд**  
    :::image-end:::  
    
1.  Обновите текущую страницу, чтобы проверить, отключены ли анимации или они видны.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
