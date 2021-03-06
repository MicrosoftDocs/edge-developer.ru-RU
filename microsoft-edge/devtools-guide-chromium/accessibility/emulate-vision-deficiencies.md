---
description: Эмулировать недостатки зрения в Microsoft Edge DevTools.
title: Эмулировать недостатки зрения в Microsoft Edge DevTools (цветовая слепота)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: eec3c95bac93e600acf1887c8d31cea2173c6aee
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397876"
---
# <a name="emulate-vision-deficiencies"></a>Имитация дефектов зрения

Чтобы лучше удовлетворять потребности пользователей [][ColorblindawarenessMain] с дефицитом цветового зрения \(цветовая слепота\), [Microsoft Edge DevTools][DevtoolsIndex] позволяет имитировать определенные недостатки цветового зрения.  Средство **эмулировать недостатки зрения** имитирует следующие категории.  

| Дефицит цветового зрения | Сведения |  
|:--- |:--- |  
| Размытое зрение | Пользователю трудно сосредоточиться на тонкостях. |  
| Протанопия | Пользователь не может воспринимать красный свет. |  
| Deuteranopia | Пользователь не может воспринимать зеленый свет. |  
| Тританопия | Пользователь не может воспринимать синий свет. |  
| Ахроматопсия | Пользователь не может воспринимать любой цвет, который уменьшает весь цвет до серого. |  

## <a name="navigate-to-the-rendering-tools"></a>Перейдите к средствам визуализации  

Для имитации дефицита зрения, применяемой для вашего веб-продукта, откройте [средства визуализации.][DevtoolsRenderingToolsIndex]  

1.  Чтобы открыть средства визуализации, выберите `...` элемент меню на панели инструментов  
1.  Выбор **дополнительных средств**  
1.  Выберите **отрисовку**  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств визуализации" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Открытие **средств визуализации**  
    :::image-end:::  

Меню **rendering** отображается в ящике.  

1.  Прокрутите вниз `Emulate vision deficiencies` к элементу меню и выберите выпадаемое меню, чтобы отобразить параметры.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню Эмулировать недостатки зрения в ящике визуализации" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Меню **недостатков эмулировать** зрение в **ящике rendering**  
    :::image-end:::  
    
1.  Выберите параметр.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню "Эмуляция недостатков зрения"" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Параметры **меню "Подражать недостаткам** зрения"  
    :::image-end:::  
    
1.  В главных окнах отображается моделирование выбранного параметра, примененного к текущей странице.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Отображение с помощью моделирования **Blurred Vision**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Отображение с помощью **моделирования размытого зрения**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Отображение с помощью моделирования **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Отображение с помощью **моделирования Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a>Используйте командное меню  

Вы также можете использовать **командное меню для** доступа к различным имитациям.  

1.  Выберите `Control` + `Shift` + `P` \(Windows/Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  Введите `emulate` , выберите то, что вы хотите имитировать и выбрать `Enter` .  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры моделирования, доступные в командном меню" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Различные параметры моделирования, доступные в **командном меню**  
    :::image-end:::  
    
> [!IMPORTANT]
> Средства **эмулирования** недостатков зрения имитируют приближения того, как человек с каждым недостатком может видеть ваш продукт.  Каждый человек отличается, поэтому недостатки зрения различаются по серьезности от человека к человеку.  Чтобы лучше удовлетворять потребности пользователей, избегайте любых цветовых сочетаний, которые могут быть проблемой.  Средства **эмулировать недостатки зрения** не являются полной оценкой доступности вашего продукта.  Вместо этого средства **эмулировать** недостатки зрения должны дать вам хороший первый шаг, чтобы избежать проблем.  

<!-- links -->  

[DevToolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Анализ производительности выполнения | Документы Майкрософт"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация цветовой слепой осведомленности"  

[AmfcbMain]: https://www.amfcb.org "Американский фонд цветных слепых (AFCB)"  
