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
# <a name="dark-or-light-color-scheme-simulation"></a>Моделирование темной или светлой цветовой схемы  

Операционные системы могут отображать любое приложение в более темных или более светлых цветах.  Наличие веб-продукта с легкой темой в операционной системе темного режима является натертым и может быть проблемой доступности для некоторых пользователей.  В Интернете можно использовать [][MDNPrefersColorScheme] запрос CSS Media Query с предпочитаемой цветовой схемой, чтобы определить, предпочитают ли пользователи отображать ваш продукт в более темной или светлой цветовой схеме.  Используйте [Microsoft Edge DevTools][DevtoolsIndex] для имитации изменения из темно-светлого режима без изменения всей операционной системы.  

1.  Откройте **командное меню.**  
    1.  Выберите `Control` + `Shift` + `P` \(Windows/Linux\) `Command` + `Shift` + `P` или \(macOS\).  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           Меню **команд**  
        :::image-end:::  
        
1.  Введите , выберите эмулировать `emulate color` **CSS предпочитает-цветовой схемы:** темные или эмулировать **CSS предпочитает-цветовой схемы:** свет, а затем выберите `Enter` .  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Параметр цветовой схемы из Меню команды" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       Параметр цветовой схемы **из Меню** команды  
    :::image-end:::  
    
    > [!IMPORTANT]
    > Просто `dark` введите или не раскроет нужный инструмент, так как существует также способ выбрать тему `light` [для DevTools][DevtoolsCustomizeDarkTheme].  Если вам интересно, что выбрать, убедитесь, **** что вы выбираете элемент меню отрисовки, а не **элемент меню** внешнего вида.  

1.  После выбора цветовой схемы обновите текущий документ, чтобы отобразить смоделированный режим.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Режим имитации освещения в Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Режим имитации освещения в Microsoft Edge DevTools  
    :::image-end:::  
    
    Просмотр и изменение CSS, как и любой другой веб-страницы.  Дополнительные сведения, перейдите к [началу работы с просмотром и изменением CSS][DevtoolsCssIndex].  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
