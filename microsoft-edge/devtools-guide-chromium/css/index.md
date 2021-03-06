---
description: Узнайте, как использовать Microsoft Edge DevTools для просмотра и изменения CSS страницы.
title: Начало работы с просмотром и редактированием CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399094"
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

# <a name="get-started-with-viewing-and-changing-css"></a>Начало работы с просмотром и редактированием CSS  

Выполните эти интерактивные учебники, чтобы узнать основы просмотра и изменения CSS для страницы с помощью Microsoft Edge DevTools.  

## <a name="open-css-examples"></a>Откройте примеры CSS  

1.  Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **CSS Examples** для открытия в новом окне.  
    
    [Примеры CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Если вы хотите пристыковаться к окну [DevTools][DevToolsCustomizePlacement] справа от вашего viewport \(отображается на следующем рисунке\), выберите Настройка и управление **DevTools** `...` .  В разделе Настройка и управление выпадаемым меню **DevTools** в разделе **Док-станция** выберите **док справа.**  
    
## <a name="view-the-css-for-an-element"></a>Просмотр CSS для элемента  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите `Inspect Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
    1.  В DevTools на **элементе Elements** на панели **дерева DOM** элемент `Inspect Me!` выделяется.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="Элемент проверки выделен в дереве DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           Элемент проверки выделен в **дереве DOM**  
        :::image-end:::  
        
    1.  В `Inspect Me!` элементе найдите значение атрибута `data-message` и скопируйте его.  
1.  На странице в **значении `data-message` : textbox** введите значение.  
1.  Наведите `Inspect Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
    1.  В DevTools на **инструменте Elements** выберите панель **Стилей.**  
    1.  В панели **Styles** элемент `Inspect Me!` выделяется.  
    1.  В `Inspect Me!` элементе найдите `aloha` правило класса.  
        
        > [!NOTE]
        > Это правило отображается, так как оно применяется к `Inspect Me!` элементу.  
        
    1.  В классе `aloha` найдите значение для `padding` стиля и скопируйте его.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Классы CSS применяются к проверенному элементу, выделенному в панели Styles" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Классы CSS применяются к выбранному элементу, например, отображаются `aloha` в панели **Styles**  
        :::image-end:::  
        
1.  На странице в **значении `padding` : textbox** введите значение.  

## <a name="add-a-css-declaration-to-an-element"></a>Добавление объявления CSS в элемент  

Используйте панель **Стилей,** чтобы изменить или добавить в элемент объявления CSS.  

> [!NOTE]
> Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите `Add A Background Color To Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
1.  Выберите `element.style` в верхней части панели **Стилей.**  
1.  Введите `background-color` и выберите `Enter` .  
1.  Введите `honeydew` и выберите `Enter` .  В **dom Tree**отображается вложенное объявление стиля, примененное к элементу.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Добавление объявления CSS в элемент с помощью панели Стилей" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Объявление `background-color:honeydew` применяется к элементу с помощью раздела панели `element.style` **Стилей**  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a>Добавление класса CSS в элемент  

Чтобы отобразить внешний вид элемента при применении класса CSS к элементу или его удалении, перейдите на панель **Стилей.**  

> [!NOTE]
> Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите `Add A Class To Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
1.  Выберите **.cls**.  DevTools открывает текстовое поле, в котором можно добавить классы к выбранному элементу.  
1.  `color_me`Введите **текстовое поле Добавить новый класс** и выберите `Enter` .  В текстовом окне **Добавить новый** класс отображается почтовый ящик, в котором можно отключить класс.  Если к элементу применены какие-либо другие классы, вы также можете ото всех `Add A Class To Me!` перегнастить.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Применить класс color_me к элементу" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Класс применяется к элементу с `color_me` помощью раздела **.cls** панели **Styles**  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a>Добавление псевдостата в класс  

Используйте панель **Стилей** для постоянного применения псевдостата CSS к элементу.  DevTools поддерживает `:active` `:focus` , и `:hover` `:visited` .  

> [!NOTE]
> Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите курсор `Hover Over Me!` на текст.  Меняется цвет фона.  
1.  Наведите `Hover Over Me!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
1.  В панели **Стилей** выберите **:hov**.  
1.  Проверьте **:hover** checkbox.  Цвет фона меняется так же, как и раньше, даже если вы не нависаете над элементом.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Toggle the hover pseudostate on an element" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Toggle the `:hover` pseudostate on an element  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a>Изменение размеров элемента  

Используйте **интерактивную** схему Box Model в панели **Стилей,** чтобы изменить ширину, высоту, обивку, маржу или длину границы элемента.  

> [!NOTE]
> Выполните [просмотр CSS для руководства по элементам](#view-the-css-for-an-element) перед этим.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите `Change My Margin!` курсор на текст, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
1.  На **схеме Box Model** в панели **Стили** наведите курс на **обивку.**  Заполнение элемента выделено в представлении.  

    > [!NOTE]
    > В зависимости от размера окна DevTools может потребоваться прокрутка в нижней части панели **Стилей** для отображения **модели Box.**  

1.  Дважды щелкните левую маржу в **модели Box,** которая в настоящее время имеет значение, которое означает, что элемент не имеет `-` левого поля.  
1.  Введите `100px` и выберите `Enter` .  Модель **box по** умолчанию по умолчанию имеет пиксели, но также принимает другие значения, такие как , или `25%` `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Наведите курсор на обивку элемента" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Наведите курсор на обивку элемента  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Изменение левого поля элемента" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Изменение левого поля элемента  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a>Отладка запросов мультимедиа  

[Запросы мультимедиа][MDNUsingMediaGueries] — это способ заставить веб-продукт реагировать на изменения параметров конфигурации для каждого пользователя.  Наиболее важным случаем использования является предоставление вашему продукту другого макета CSS в зависимости от размеров представления.  Использование отдельных макетов позволяет разметку с одним столбцом для мобильных устройств и макеты с несколькими столбцами при наличии большего имени экрана.  

Если вы хотите отлагировать или протестировать запросы мультимедиа, определенные в CSS, используйте следующие действия.  

1.  Откройте инструменты разработчика и выберите значок панели инструментов **Toggle** в левом верхней части или `Ctrl` + `Shift` + `M` выберите \( `Cmd` + `Shift` + `M` на macOS\).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Откройте панель инструментов устройства" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Откройте панель инструментов устройства  
    :::image-end:::  
    
1.  Открыв панель инструментов устройства, выберите меню в правом верхнем ряду и `...` выберите **View Media Queries**.  Цветные полосы, отображаемые над веб-страницей, представляют различные запросы мультимедиа.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Показать запросы мультимедиа в панели инструментов устройства" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Показать запросы мультимедиа в панели инструментов устройства  
    :::image-end:::  
    
1.  Наведите курсор на границы в барах, чтобы отобразить значения различных запросов мультимедиа.  Выберите каждый из них для повторного выбора веб-страницы, чтобы соответствовать.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Выбор запроса мультимедиа из панели предварительного просмотра" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Выбор запроса мультимедиа из панели предварительного просмотра  
    :::image-end:::  
    
1.  Чтобы отлажать запросы мультимедиа и открыть CSS-файл в редакторе; наведите курсор на любой из сегментов панели, откройте контекстное меню \(правой кнопкой `Sources` мыши\) и выберите `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Раскрытие запросов мультимедиа в редакторе источников" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Раскрытие запросов мультимедиа в редакторе источников  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение размещения Microsoft Edge DevTools (Undock, dock to bottom, dock to left)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование запросов мультимедиа | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
