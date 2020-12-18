---
description: Эмулировать недостатки зрения в Microsoft Edge DevTools.
title: Эмуляция недостатков зрения в Microsoft Edge DevTools (дальтонизм)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230826"
---
# Имитация дефектов зрения

Для лучшего удовлетворения потребностей пользователей с недостатком цветового зрения [\(color][ColorblindawarenessMain] blindness\), Microsoft Edge [DevTools][DevtoolsIndex] позволяет моделировать определенные недостатки цветового зрения.  Средство **эмуляции недостатков зрения** имитирует следующие категории.  

| Недостаток цветового зрения | Сведения |  
|:--- |:--- |  
| Размытое зрение | Пользователю трудно сосредоточиться на подробных сведениях. |   
| Протанопия | Пользователь не может воспринимать красный свет. |  
| Deuteranopia | Пользователь не может воспринимать зеленый свет. |  
| Тританопия | Пользователь не может воспринимать синий свет. |  
| Achromatopsia | Пользователь не может воспринимать какой-либо цвет, который уменьшает весь цвет до оттенка серого. |  

## Переход к средствам отрисовки  

Чтобы смоделировать недостаток зрения, применяемый к веб-продукту, откройте [инструменты отрисовки.][DevtoolsRenderingToolsIndex]  

1.  Чтобы открыть инструменты отрисовки, выберите пункт `...` меню на панели инструментов  
1.  Выбрать `More tools`  
1.  Выбрать `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Открытие средств отрисовки" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       Открытие средств **отрисовки**  
    :::image-end:::  

В **этом ящике** появится меню "Отрисовка".  

1.  Прокрутите вниз до `Emulate vision deficiencies` пункта меню и выберите его, чтобы отобразить параметры.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Меню эмуляции недостатков зрения в отрисовке" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       Меню **"Эмуляция недостатков зрения"** в **отрисовке**  
    :::image-end:::  
    
1.  Выберите параметр.  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Параметры меню эмуляции недостатков зрения" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       Параметры **меню "Эмуляция недостатков зрения"**  
    :::image-end:::  
    
1.  В главных окнах отображается имитация выбранного параметра, примененного к текущей странице.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Отображение с помощью имитации **Размытое зрение**" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             Отображение с помощью **имитации размытого** зрения  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Отображение с помощью имитации **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             Отображение с помощью **имитации Achromatopsia** :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Использование меню команд  

Вы также можете использовать меню **команд для** доступа к различным имитациям.  

1.  Выберите `Control` + `Shift` + `P` \(Windows\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Меню команд" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  Введите `emulate` , выберите то, что нужно смоделировать, и `Enter` выберите.  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Различные параметры имитации, доступные в меню команд" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       Различные параметры имитации, доступные в меню **команд**  
    :::image-end:::  
    
> [!IMPORTANT]
> Средства **эмуляции недостатков зрения** имитируют приближение того, как человек с каждым недостатком может видеть ваш продукт.  Каждый человек разный, поэтому недостатки зрения различаются по степени серьезности от человека к человеку.  Чтобы лучше удовлетворить потребности пользователей, избегайте любых сочетаний цветов, которые могут быть проблемой.  Средства **эмуляции недостатков зрения** не являются полной оценкой доступности вашего продукта.  Вместо этого средства **эмуляции** недостатков зрения должны дать вам хороший первый шаг, чтобы избежать проблем.  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Анализ производительности в времени выполнения | Документы Майкрософт"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "Организация по информированию о незрячих цветах"  

[AmfcbMain]: https://www.amfcb.org "American Foundation для дальтоник (AFCB)"  

