---
description: Список способов настройки Microsoft Edge DevTools
title: Настройка Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 682ff78b6a5272c1f6462648d64241448838edac
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "11189992"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Настройка Microsoft Edge DevTools  

На этой странице перечислены способы настройки Microsoft Edge DevTools.  

## Параметры  

**Параметры**  >  **Настройки** . доступно множество вариантов настройки DevTools.  

Чтобы открыть параметры, выполните одно из указанных ниже действий.  

*   Выберите `F1` , когда DevTools в фокусе.  
*   Откройте **главное меню** и выберите пункт **Параметры**.  
    
:::image type="complex" source="../media/customize-settings-preferences.msft.png" alt-text="Параметры" lightbox="../media/customize-settings-preferences.msft.png":::
   **Параметры**  
:::image-end:::  

## Зазор  

**Ящик** — это вторая панель, в которой отображаются инструменты выбора.  

Чтобы открыть (или закрыть) **денежный ящик**, выберите `Escape` .  

:::image type="complex" source="../media/customize-drawer-open.msft.png" alt-text="Ящик" lightbox="../media/customize-drawer-open.msft.png":::
   **Ящик**  
:::image-end:::  

По умолчанию некоторые инструменты открываются в главной панели, а другие — в **ящике**.  Нажмите кнопку **Дополнительно** \ ( `...` ), чтобы открыть инструмент в **денежном ящике**.  

:::image type="complex" source="../media/customize-drawer-open-more-tools.msft.png" alt-text="Кнопка для открытия ящика" lightbox="../media/customize-drawer-open-more-tools.msft.png":::
   Кнопка для открытия **ящика**  
:::image-end:::  

Вы можете перемещать инструменты между главной панелью и денежным ящиком.  

*   Чтобы переместить инструмент из почтового ящика на главную панель, наведите на него указатель мыши, откройте контекстное меню, а затем выберите пункт **Перейти к началу**.  
    
    :::image type="complex" source="../media/move-from-drawer.msft.png" alt-text="Перемещение инструмента из ящика на главную панель" lightbox="../media/move-from-drawer.msft.png":::
       Перемещение инструмента из **ящика** на главную панель  
    :::image-end:::  
    
*   Чтобы переместить инструмент из главной панели в денежный, наведите указатель мыши на инструмент, откройте контекстное меню (щелкните правой кнопкой мыши и выберите пункт **переместить в конец**).  
    
    :::image type="complex" source="../media/move-to-drawer.msft.png" alt-text="Инструмент «Перемещение» из главной панели в денежный ящик" lightbox="../media/move-to-drawer.msft.png":::
       Инструмент «Перемещение» из главной панели в **денежный ящик**
    :::image-end:::  
    

## Изменение порядка панелей  

Для изменения порядка выберите и перетащите инструмент.  Ваш заказ на пользовательские инструменты сохраняется в течение сеансов DevTools.  

> [!NOTE]
> По умолчанию средство " **сеть** " обычно является четвертым в левой части экрана.  На приведенном ниже рисунке панель **Network (сеть** ) — это первый из левых.  

:::image type="complex" source="../media/customize-network-first-position.msft.png" alt-text="Настраиваемый порядок Devtools на панели" lightbox="../media/customize-network-first-position.msft.png":::
   Настраиваемый порядок Devtools на панели  
:::image-end:::  

## Изменение положения DevTools  

Ознакомьтесь с [DevTools размещения Microsoft Edge][DevToolsPlacement].  

:::image type="complex" source="../media/customize-dev-tools-dock-side.msft.png" alt-text="Незакрепленные DevTools" lightbox="../media/customize-dev-tools-dock-side.msft.png":::
   Незакрепленные DevTools  
:::image-end:::  

## Темная тема  

См. [: включить темную тему][DarkTheme].  

:::image type="complex" source="../media/customize-settings-appearance-theme.msft.png" alt-text="Темная тема" lightbox="../media/customize-settings-appearance-theme.msft.png":::
   Темная тема  
:::image-end:::  

## Эксперименты  

Чтобы включить эксперименты DevTools, выполните указанные ниже действия.  

1.  Перейдите к `edge://flags/#enable-devtools-experiments` .  
1.  Нажмите кнопку **включить**.  
1.  В нижней части страницы нажмите кнопку " **Перезапустить сейчас**".  

В следующий раз, когда вы открываете DevTools, в разделе " [Параметры](#settings)" отображается новая страница " **эксперименты** ".  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreIcon]: ../media/more-icon.msft.png  

<!-- links -->  

[DevToolsPlacement]: ./placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DarkTheme]: ./dark-theme.md "Включить темную тему в Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/customize/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
