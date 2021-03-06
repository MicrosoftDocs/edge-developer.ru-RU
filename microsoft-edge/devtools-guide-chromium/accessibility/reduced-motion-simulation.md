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
# <a name="reduced-motion-simulation"></a>Имитация уменьшенного движения  

Анимация в веб-продуктах может быть проблемой доступности.  Операционные системы работают с этой проблемой, включив возможность отключить анимацию, чтобы избежать путаницы пользователей и потенциальных проблем со здоровьем, таких как запуск изъятий.  В Интернете можно использовать [][MDNPrefersReducedMotion] запрос CSS Media Query с пониженным движением, чтобы определить, предпочитают ли пользователи не запускать и не отображать анимацию.  В продукте можно завернуть код анимации в тест, чтобы не показывать анимации для пострадавших пользователей.  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

С помощью [Microsoft Edge DevTools][DevtoolsIndex]можно смоделировать этот параметр уменьшенного движения, не меняя операционную систему.  

1.  Откройте **командное меню.**  
    1.  Выберите `Control` + `Shift` + `P` в Windows/Linux или `Command` + `Shift` + `P` на macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Меню **команд**  
        :::image-end:::  
        
1.  `reduced`Введите, чтобы включить и отключить моделирование.  Выберите параметр и выберите `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Включите или отключите параметры с пониженным движением из командного меню" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       Включите или отключите параметры с **пониженным движением** из **командного меню**  
    :::image-end:::  
    
1.  Обновите текущую страницу, чтобы проверить, отключены ли анимации или видны.  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "предпочитает уменьшенное движение | MDN"  
