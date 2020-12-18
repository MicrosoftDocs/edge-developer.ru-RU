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
# Моделирование темной или светлой цветовой схемы  

Операционные системы могут отображать любые приложения в более темных или светлых цветах.  Наличие веб-продукта с светлой темой в операционной системе в темном режиме очень важно и может быть проблемой с доступностью для некоторых пользователей.  В Интернете можно использовать запрос мультимедиа CSS [prefers-color-scheme,][MDNPrefersColorScheme] чтобы определить, предпочитают ли пользователи видеть ваш продукт в схеме темной или светлой цветовой схемы.  Используйте [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] для имитации изменения режима темного на светлый без изменения всей операционной системы.  

1.  Откройте меню **команд.**  
    1.  Выберите `Control` + `Shift` + `P` в Windows, Linux или `Command` + `Shift` + `P` macOS.  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Меню **команд**  
        :::image-end:::  
        
1.  Type `emulate color` , choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Параметр цветовой схемы из меню команд" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Параметр цветовой схемы из **меню команд**  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Просто введите или не раскрывают нужное средство, так как существует также способ выбрать тему `dark` `light` для [DevTools.][DevtoolsGuideChromiumCustomizeDarkTheme]  Если вы хотите узнать, что выбрать, убедитесь, что вы выбираете элемент меню визуализации, а не элемент меню **внешнего** вида. ****  

1.  После выбора цветовой схемы перезагрузить текущий документ, чтобы увидеть имитированный режим.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Режим имитации освещения в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Режим имитации освещения в Microsoft Edge DevTools  
    :::image-end:::  
    
    Просматривайте и изменяйте CSS, как и любую другую веб-страницу.  Дополнительные сведения см. в теме ["Начало работы с просмотром и изменением CSS".][DevtoolsGuideChromiumCssIndex]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
