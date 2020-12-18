---
description: Узнайте, как использовать Microsoft Edge DevTools для просмотра и изменения CSS страницы CSS.
title: Проверка сетки CSS в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1fe6bd1c8efd244315fb9a38777df6ea3e9b1a4d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231099"
---
# Проверка сетки CSS  

В этой статье вы можете определить сетки CSS на веб-сайте и отладить проблемы макета сетки с помощью настраиваемых наложения сетки.  

Примеры, используемые на рисунках в этой статье, взяты с следующих веб-страниц.  

*   [Поле "Вешка"][JecFyiDemoCssGridFruit]  
*   [Поле "Неугомя"][JecFyiDemoCssGridSnack]  

## Перед началом работы  

Сетка CSS — это мощная парадигма макета для Интернета.  Отличное место для начала изучения сетки CSS и многих функций — это руководство по макету сетки [CSS][MdnCssGridLayout] на MDN.  

## Обнаружение сеток CSS  

Если htmL-элемент на странице имеет или применяется к ней, рядом с ней на панели элементов отображается индикатор `display: grid` `display: inline-grid` `grid` событий. [][DevtoolsGuideChromiumOpen]  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Обнаружение сетки" lightbox="../media/grid-discover-grid.msft.png":::
   Обнаружение сетки  
:::image-end:::  

Выберите индикатор событий, чтобы выровнять отображение наложения сетки на странице.  Наложение появляется над элементом и, как сетка, отображает положение линий сетки и дорожек:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Индикатор событий сетки" lightbox="../media/grid-highlight-grid.msft.png":::
   Индикатор событий сетки  
:::image-end:::  

Откройте области **макета.**  Если сетки включены на страницу, в области макета содержится раздел **Grid,** содержащий несколько параметров для просмотра сеток. ****  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Области макета" lightbox="../media/grid-layout-pane.msft.png":::
   **Области** макета  
:::image-end:::  

Раздел **Grid** в области **макета** содержит следующие 2 под раздела.  

*   Параметры отображения наложения  
*   Наложения сетки  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Параметры отображения наложения  

Параметры **отображения наложения** состоят из следующих 2 частей.  

*   Выберите один из следующих параметров из меню в выпадаемом меню.  
    
    | Вариант строки | Сведения |  
    |:--- |:--- |  
    | **Скрытие подписей строк** | Скрыть метки линий для каждого наложения сетки. |  
    | **Показывать номера строк** | Отображение номеров линий для каждого наложения сетки \(выбрано по умолчанию\). |  
    | **Показать имена строк** | Отображение имен линий для каждого наложения сетки при их выводе. |  
    
*  Выберите этот контрольный параметр рядом со следующими вариантами.  
    
    | Параметр | Сведения |  
    |:--- |:--- |  
    | **Показать размеры дорожки**  | Отображение \(или скрытие\) размеров дорожек. |  
    | **Показать имена области** | Отображение \(или скрытие\) имен области при их выводе. |  
    | **Расширение линий сетки** | Отображает \(или скрывает\) расширения размеров сетки вдоль каждой оси.  По умолчанию линии сетки показаны внутри элемента только с установленным или `display: grid` `display: inline-grid` установленным значением CSS. |  
    
В следующих разделах представлены подробные сведения о каждом из параметров отображения **наложения.**  

### Показывать номера строк  

По умолчанию положительные и отрицательные номера строк отображаются на наложение сетки.  

Для получения дополнительных сведений о отрицательных числах в наложение сетки перейдите к расположению на основе [строки с помощью сетки CSS.][MdnLineBasedPlacementCssGrid]  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Отображение номеров строк" lightbox="../media/grid-show-line-numbers.msft.png":::
   Отображение номеров строк  
:::image-end:::  

### Скрытие подписей строк  

Выберите **"Скрыть метки строки",** чтобы скрыть номера строк.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Скрытие подписей строк" lightbox="../media/grid-hide-line-labels.msft.png":::
   Скрытие подписей строк  
:::image-end:::  

### Показать имена строк  

Для получения дополнительных сведений об именах строк в наложение сетки перейдите к макету с [помощью именуемой сетки.][MdnLayoutUsingNamedGridLines]  

Select **Show line names** to view the line names instead of numbers.  В примере 4 строки имеют имена: `left` , , , и `middle1` `middle2` `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Показать имена строк" lightbox="../media/grid-show-line-names.msft.png":::
   **Показать имена строк**  
:::image-end:::  

### Показать размеры дорожки  

В поле **"Показать размеры дорожки"** для просмотра размеров дорожки сетки.  

DevTools отображает `[authored size]` и `[computed size]` в каждой метке строки.  

| Size | Сведения |  
|:--- |:--- |  
| **авторский размер** | Размер, определенный в таблице стилей \(пропущен, если не определен\). |  
| **вычисляемая величина** | Фактический размер на экране. |  

В демонстрации размеры `snack-box` столбцов определяются в `grid-template-columns:1fr 2fr;` CSS.  Поэтому метки строк столбцов отображают как авторские, так и вычисляемые размеры.  

| Размер отслеживания | Авторский размер | Вычисляемая величина |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96.66px** | 1fr | 96,66px |  
| **2fr** &#x2022; **193.32px** | 2fr | 193,32px |  

Метки строк отображают только вычисленные размеры, так как в таблице стилей не определены размеры строк.  

| Размер отслеживания | Авторский размер | Вычисляемая величина |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Показать размеры дорожки" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Показать размеры дорожки**  
:::image-end:::  

### Показать имена области  

Чтобы просмотреть имена области, в убедитесь, что в списке **должны быть имена** области.  В этом примере сетка имеет 3 области: **верхняя,** **нижняя1** и **нижняя 2.**  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Показать имена области" lightbox="../media/grid-show-area-names.msft.png":::
   **Показать имена области**  
:::image-end:::  

### Расширение линий сетки  

В поле **"Расширить линии сетки",** чтобы линии сетки были расширены до края точки просмотра вдоль каждой оси.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Расширение линий сетки" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Расширение линий сетки**  
:::image-end:::  

## Наложения сетки  

Раздел **"Наложения сетки"** содержит список сеток, присутствующих на странице, каждый из которых с помощью контрольного списка, а также различные параметры.  

### Включить представления наложения для нескольких сеток  

Чтобы отобразить сетку наложения для нескольких сеток, выберите его рядом с каждым именем сетки.  В этом примере включены 2 наложения сетки, каждая из которых представлена разными цветами.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Включить представления наложения для нескольких сеток" lightbox="../media/grid-grid-overlays.msft.png":::
   Включить представления наложения для нескольких сеток  
:::image-end:::  

### Настройка цвета наложения сетки  

Чтобы открыть палитру и настроить цвет наложения сетки, выберите поле рядом с именем наложения сетки.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Настройка цвета наложения сетки" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Настройка цвета наложения сетки  
:::image-end:::  

### Выделение сетки  

Чтобы выделить HTML-элемент **** на панели "Элементы" и прокрутить его на веб-странице, выберите элемент **Show** на панели элементов \( Элемент Show в значке панели элементов ![ ][ImageShowElementInElementsPanelIcon] \)  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Выделение сетки" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Выделение сетки  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Сетка CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Сетка CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Макет с использованием именуемой сетки | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Размещение на основе строк с помощью сетки CSS | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/css/grid). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
