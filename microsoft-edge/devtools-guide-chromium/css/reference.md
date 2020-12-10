---
description: Найдите новые рабочие процессы для просмотра и изменения CSS в Microsoft Edge DevTools.
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204014"
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

# Справочник по CSS  

Ниже приведен полный справочник по функциям, связанным с просмотром и изменением CSS, в Microsoft Edge DevTools.  

Ознакомьтесь с основными принципами [просмотра и изменения каскадных таблиц стилей][DevToolsCSSGetStarted] .  

## Выбор элемента  

Панель " **элементы** " в DevTools позволяет просматривать или изменять CSS для одного элемента за один раз.  Выбранный элемент выделится в **дереве DOM**.  Стили элемента отображаются на панели " **стили** ".  В разделе [Просмотр CSS для элемента][DevToolsCSSGetStartedTutorial] учебника.  

> [!NOTE]
> На приведенном ниже рисунке `h1` элемент, выделенный в **дереве DOM** , является выбранным элементом.  Справа в области **стили** отображаются стили элемента.  В левой части экрана выделяется элемент в окне просмотра, но только потому, что в данный момент указатель мыши наведен на него в **дереве DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Пример выбранного элемента" lightbox="../media/css-elements-styles-h1.msft.png":::
   Пример выбранного элемента  
:::image-end:::  

Для выбора элемента используйте одно из указанных ниже действий.  

*   В окне просмотра наведите указатель мыши на элемент, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите команду **проверить**.  
*   В DevTools выберите **пункт выбрать** элемент \ ( ![ выбрать элемент ][ImageSelectAnElementIcon] \) или SELECT `Control` + `Shift` + `C` \ (Windows, Linux \) или `Command` + `Shift` + `C` \ (macOS \), а затем выберите элемент в окне просмотра.  
*   В DevTools выберите элемент в **дереве DOM**.  
*   В DevTools выполните запрос, как `document.querySelector('p')` на **консоли**, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **Показать на панели элементы**.  

## Просмотр CSS  

### Просмотр внешней таблицы стилей, в которой определено правило  

В области **стили** щелкните ссылку рядом с правилом CSS, чтобы открыть внешнюю таблицу стилей, которая определяет правило.  

Если таблица стилей minified, перейдите в раздел, чтобы [сделать файл minified доступным для чтения][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> На приведенном ниже рисунке после выбора `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` строки 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , где `.content h1:first-of-type` определено правило CSS.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Просмотр таблицы стилей, в которой определено правило" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Просмотр таблицы стилей, в которой определено правило  
:::image-end:::  

### Просмотр только CSS, которая фактически применяется к элементу  

На вкладке **стили** отображаются все правила, применимые к элементу, включая объявления, которые были переопределены.  Если вы не заинтересованы в переопределенных объявлениях, используйте **вычисляемые** вкладки для просмотра только CSS, которая фактически применяется к элементу.  

1.  [Выберите элемент](#select-an-element).  
1.  Перейдите на вкладку " **вычисляемые** " на панели " **элементы** ".  

> [!NOTE]
> В окне с широкой DevTools **Вычисляемая** вкладка не существует.  Содержимое **вычисляемой** вкладки отображается на вкладке **стили** .  

Унаследованные свойства являются непрозрачными.  Установите флажок **Показать все** , чтобы увидеть все унаследованные значения.  

> [!NOTE]
> На приведенном ниже рисунке показана **Вычисляемая** вкладка, на которой ПОКАЗАНЫ свойства CSS, применяемые к текущему `h1` элементу.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Вычисляемая вкладка" lightbox="../media/css-elements-computed-h1.msft.png":::
   **Вычисляемая** вкладка  
:::image-end:::  

### Просмотр свойств CSS в алфавитном порядке  

Используйте **вычисляемую** вкладку.  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Просмотр унаследованных свойств CSS  

Установите флажок **Показать все** на вкладке **вычисляемый** .  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Просмотр модели Box для элемента  

Чтобы просмотреть [модель Box][MDNBoxModel] элемента, перейдите на вкладку **стили** .  Если окно DevTools узким, схема **модель Box** находится в нижней части вкладки.  

Выберите и измените значение, чтобы изменить значение.  

> [!NOTE]
> На рисунке ниже показана модель Box на вкладке " **стили** " в **поле** "модель" для элемента, выбранного в данный момент `h1` .  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Схема модели Box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Схема **модели Box**  
:::image-end:::  

### Поиск и фильтрация CSS элемента  

С помощью текстового поля **Фильтр** на вкладках **стили** и **вычисляемые** вкладки можно искать определенные свойства или значения CSS.  

Чтобы также искать унаследованные свойства на вкладке **вычисляемые** , установите флажок **Показать все** .  

> [!NOTE]
> На приведенном ниже рисунке для вкладки **стили** отображаются только правила, включающие поисковый запрос `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Фильтрация вкладки "стили"" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Фильтрация вкладки " **стили** "  
:::image-end:::  

> [!NOTE]
> На приведенном ниже рисунке отфильтрованная **вкладка** фильтруется так, чтобы отображались только объявления, включающие поисковый запрос `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Фильтрация вычисляемой вкладки" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Фильтрация **вычисляемой** вкладки  
:::image-end:::  

### Переключение на псевдо-класс  

Выполните указанные ниже действия, чтобы переключить псевдо-класс, например,, `:active` `:focus` `:hover` или `:visited` .  

1.  [Выберите элемент](#select-an-element).  
1.  На панели " **элементы** " перейдите на вкладку " **стили** ".  
1.  Выберите **: Hov**.  
1.  Проверьте псевдо-класс, который вы хотите включить.  

> [!NOTE]
> На рисунке ниже показано, как переключается `:hover` псевдо-класс.  В окне просмотра убедитесь в том, что `background-color: cornflowerblue` объявление применяется к элементу, несмотря на то что элемент фактически не наведен на указатель.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Переключение: псевдо-класс для наведения" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Переключение `:hover` псевдо-класса  
:::image-end:::  

Для интерактивного учебника перейдите к разделу [Добавление PseudoState в класс][DevToolsCSSGetStartedAddPseudoState].  

### Просмотр страницы в режиме печати  

Выполните указанные ниже действия, чтобы просмотреть страницу в режиме печати.  

1.  [Открытие меню команд][DevToolsCommandMenu].  
1.  Начните вводить текст `Rendering` и выберите его `Show Rendering` .  
1.  Для **имитации** раскрывающегося списка выбери мультимедиа в CSS нажмите кнопку **Печать**.  

### Просмотр использованной и неиспользуемой CSS с помощью вкладки "покрытие"  

На вкладке Coverage показано, какая страница CSS используется в действительности.  

1.  Выберите `Control` + `Shift` + `P` \ (Windows, Linux \) или `Command` + `Shift` + `P` \ (macOS \), когда DevTools находится в фокусе, чтобы [Открыть меню команд][DevToolsCommandMenu].  
1.  Начните вводить текст `coverage` и выберите **Показать покрытие**.  Откроется вкладка покрытие.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Открытие вкладки "покрытие" в меню команд" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Открытие вкладки " **покрытие** " в **меню команд**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Вкладка "покрытие"" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             Вкладка " **покрытие** "  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Нажмите кнопку **начать покрытие инструментирования и обновите страницу** \ ( ![ Запуск инструментированного покрытия и обновление страницы ][ImageRefreshIcon] \).  Обновленная страница и вкладка Coverage предоставляют общие сведения о том, сколько стилей CSS и JavaScript используется для каждого файла, загружаемого браузером.  Зеленый представляет используемые CSS.  Красный — неиспользуемый CSS.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Общие сведения о том, сколько каскадных таблиц (и JavaScript \) использует и не используется  
    :::image-end:::  

1.  Выберите CSS-файл, чтобы просмотреть разбиение по строкам для используемого CSS.  
    
    > [!NOTE]
    > На приведенном ниже рисунке строки 145 в 147 и 149 в 151 из `b66bc881.site-ltr.css` не используются, в то время как используются строки 163 — 166.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Разбиение по строкам для используемых и неиспользуемых CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       Разбиение по строкам для используемых и неиспользуемых CSS  
    :::image-end:::  
    
### Принудительная печать в режиме предварительного просмотра  

Просмотрите [DevTools в режиме предварительного просмотра][DevToolsCssPrintPreview].  

## Изменение CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### Добавление объявления CSS в элемент  

Порядок объявлений влияет на стиль элемента с помощью приведенного ниже списка, который поможет вам добавлять объявления различными способами.  

*   [Добавление встроенного объявления](#add-an-inline-declaration).  Эквивалентно добавлению `style` атрибута в HTML элемента.  
*   [Добавление объявления в правило стиля](#add-a-declaration-to-a-style-rule).  

**Какой рабочий процесс следует использовать?** В большинстве сценариев вы, возможно, захотите использовать рабочий процесс объявления на встроенных элементах.  Встроенные объявления имеют более высокие особенности, чем внешние, поэтому встроенный рабочий процесс гарантирует, что изменения вступают в силу в ожидаемом элементе.  Для получения дополнительных сведений об определенном способе перейдите к разделу [типы Selector][MDNSelectorTypes].  

Если при отладке любого стиля элемента требуется специально проверить, что происходит, если объявление определено в разных местах, используйте другой рабочий процесс.  

#### Добавление встроенного объявления  

Чтобы добавить встроенное объявление, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** выберите между скобками раздела **element. Style** .  Курсор фокусируется на том, что позволяет вводить текст.  
1.  Введите имя свойства и нажмите кнопку `Enter` .  
1.  Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .  Убедитесь, что в **дереве DOM** `style` к элементу добавлен атрибут.  

> [!NOTE]
> На приведенном ниже рисунке к `margin-top` `background-color` выбранному элементу применены свойства и.  В **дереве DOM** убедитесь, что объявления отражены в `style` атрибуте для элемента.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Добавление встроенных объявлений" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Добавление встроенных объявлений  
:::image-end:::  

#### Добавление объявления в правило стиля  

Чтобы добавить объявление к существующему правилу стиля, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** выберите один из квадратных скобок правила стиля, к которому вы хотите добавить объявление.  Курсор фокусируется на том, что позволяет вводить текст.  
1.  Введите имя свойства и нажмите кнопку `Enter` .  
1.  Введите допустимое значение для этого свойства и нажмите кнопку `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Добавление объявления в правило стиля" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Добавление `border-bottom-style:groove` объявления в правило стиля  
:::image-end:::  

### Изменение имени или значения объявления  

Выберите и измените имя или значение объявления, чтобы изменить его.  Сочетания клавиш для быстрого увеличения или уменьшения значения (, или единиц) можно найти [в статье изменение значений объявлений](#change-declaration-values-with-keyboard-shortcuts) `0.1` `1` `10` `100` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Изменение значения объявления" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Изменение значения `border-bottom-style` объявления  
:::image-end:::  

### Изменение значений объявлений с помощью сочетаний клавиш  

При редактировании значения объявления вы можете использовать следующие сочетания клавиш, чтобы увеличить значение на определенную величину.  

*   Выберите `Alt` + `Up` \ (Windows, Linux \) или `Option` + `Up` \ (macOS \), чтобы увеличить его `0.1` .  
*   Выберите `Up` , чтобы изменить значение `1` , или, `0.1` Если текущее значение находится в диапазоне от `-1` и до `1` .  
*   Выберите, `Shift` + `Up` чтобы увеличить `10` .  
*   Выберите `Shift` + `Page Up` \ (Windows, Linux \) или `Shift` + `Command` + `Up` \ (macOS \), чтобы увеличить значение `100` .  

Кроме того, выполняется уменьшение.  Просто замените каждый из `Up` упомянутых выше экземпляров `Down` .  

### Добавление класса в элемент  

Чтобы добавить класс в элемент, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element) в **дереве DOM**.  
1.  Выберите **. CLS**.  
1.  Введите имя класса в текстовом поле **Добавить новый класс** .  
1.  Выберите `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Область «классы элементов»" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Область « **классы элементов** »  
:::image-end:::  

### Переключение класса  

Выполните указанные ниже действия, чтобы включить или отключить класс для элемента.  

1.  [Выберите элемент](#select-an-element) в **дереве DOM**.  
1.  Откройте область **классы элементов** .  Дополнительные сведения о том, [как добавить класс в элемент](#add-a-class-to-an-element).  Под текстовым полем **Добавить новый класс** находятся все классы, которые применяются к определенному элементу.  
1.  Установите флажок рядом с классом, который вы хотите включить или отключить.  

### Добавление правила стиля  

Чтобы добавить новое правило стиля, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  Нажмите **новое правило стиля** \ ( ![ новое правило стиля ][ImageNewStyleRuleIcon] ).  DevTools вставляет новое правило под правилом **element. Style** .  

> [!NOTE]
> На приведенном ниже рисунке DevTools добавляет `h1.devsite-page-title` правило стиля после выбора **нового правила стиля**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Добавление нового правила стиля" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Добавление нового правила стиля  
:::image-end:::  

#### Выберите таблицу стилей, к которой нужно добавить правило.  

При [добавлении нового правила стиля](#add-a-style-rule)нажмите и удерживайте **новое правило** стиля \ ( ![ новое правило стиля), ][ImageNewStyleRuleIcon] чтобы выбрать таблицу стилей, к которой нужно добавить правило.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Выбор таблицы стилей" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Выбор таблицы стилей  
:::image-end:::  

#### Добавление правила стиля в определенное место  

Выполните указанные ниже действия, чтобы добавить правило стиля в конкретное расположение на вкладке " **стили** ".  

1.  Наведите указатель мыши на правило стиля, которое находится в том месте, куда вы хотите добавить новое правило стиля.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **Вставить правило стиля ниже** \ ( ![ Вставьте правило стиля ниже значка ][ImageNewStyleRuleIcon] \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Вставить правило стиля ниже" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Вставить правило стиля ниже**  
:::image-end:::  

### Панель инструментов "другие действия"  

На панели инструментов " **другие действия** " можно выполнять указанные ниже действия.  

*   Вставка правила стиля прямо ниже того, на котором вы отправили фокус.  
*   Добавьте в `background-color` `color` `box-shadow` правило стиля, которое `text-shadow` вы хотите включить, или объявление.  

Выполните указанные ниже действия, чтобы открыть панель инструментов **Дополнительные действия** .  

1.  На вкладке **стили** наведите указатель мыши на правило стиля.  **Дополнительные действия** \ ( `...` \) находятся в правом нижнем углу раздела "правило стиля".  
    
    > [!NOTE]
    > На приведенном ниже рисунке наведите указатель мыши на `.header-holder.has-default-focus` правило стиля и **другие действия** будут отображены в правом нижнем углу раздела "правило стиля".  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Показать дополнительные действия" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Показать **Дополнительные действия** \ ( `...` \)  
    :::image-end:::  
    
1.  Наведите указатель мыши на элемент **Дополнительные действия** , `...` чтобы отобразить указанные выше действия.  
    
    > [!NOTE]
    > **Правило стиля вставки, показанное ниже** , выводится при наведении указателя мыши на **другие действия**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Панель инструментов «другие действия»" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Панель инструментов « **другие действия** »  
    :::image-end:::  
    
### Переключить объявление  

Выполните действия folllwoing, чтобы переключить одно объявление на \ (или выключить).  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** наведите указатель мыши на правило, которое определяет объявление.  Рядом с каждым объявлением появится флажок.  
1.  Установите флажок \ (или снимите) флажок рядом с объявлением.  Если вы снимите флажок объявления, DevTools пересекает его, чтобы показать, что он больше не активен.  

> [!NOTE]
> На приведенном ниже рисунке `margin-top` свойство для выбранного в данный момент элемента было отключено.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Переключить объявление" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Переключить объявление  
:::image-end:::  

### Добавление объявления цвета фона  

Выполните указанные ниже действия, чтобы добавить `background-color` объявление к элементу.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `background-color` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **добавить цвет фона** \ ( ![ Добавить значок цвет фона ][ImageAddBackgroundColorIcon] ).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Добавление цвета фона" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Добавление цвета фона**  
:::image-end:::  

### Добавление объявления цвета  

Выполните указанные ниже действия, чтобы добавить `color` объявление к элементу.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `color` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **добавить цвет** \ ( ![ добавить цвет значок ][ImageAddColorIcon] ).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Добавить цвет" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Добавить цвет**  
:::image-end:::  

### Добавление объявления с помощью блочной тени  

Выполните указанные ниже действия, чтобы добавить `box-shadow` объявление к элементу.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `box-shadow` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **"добавить тень"** , а затем — ![ значок "добавить тень" ][ImageAddBoxShadowIcon] .  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Добавление тени для поля" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Добавление тени для поля**  
:::image-end:::  

### Добавление объявления тени для текста  

Выполните указанные ниже действия, чтобы добавить `text-shadow` объявление к элементу.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `text-shadow` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **Добавить тень текста** \ ( ![ Добавить значок тени текста ][ImageAddTextShadowIcon] ).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Добавление тени текста" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Добавление тени текста**  
:::image-end:::  

### Изменение цвета с помощью палитры цветов  

В **средстве выбора цвета** есть графический интерфейс для изменения `color` и `background-color` объявлений.  

Выполните указанные ниже действия, чтобы открыть окно **выбора цвета**.  

1.  [Выберите элемент](#select-an-element).  
1.  На вкладке **стили** найдите и щелкните то `color` `background-color` же объявление, которое вы хотите изменить.  Слева от "," `color` `background-color` или аналогичного значения есть маленький квадрат, который является предварительным просмотром цвета.  
    
    > [!NOTE]
    > На приведенном ниже рисунке небольшой квадрат слева от него `rgba(0, 0, 0, 0.7)` является предварительным просмотром этого цвета.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Цвет предварительного просмотра" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Цвет предварительного просмотра  
    :::image-end:::  
    
1.  Нажмите кнопку Предварительный просмотр, чтобы открыть окно **выбора цвета**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Выбор цвета" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       **Выбор цвета**  
    :::image-end:::  
    
На приведенном ниже рисунке и списке описывает каждого элемента пользовательского интерфейса в **палитре цветов**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Палитра цветов с заметками" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   **Палитра цветов**с заметками  
:::image-end:::  

:::row:::
   :::column span="1":::
      1,1  
   :::column-end:::
   :::column span="1":::
      **Оттенки**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Выбрав**  
   :::column-end:::
   :::column span="2":::
      Дополнительные сведения можно найти с помощью [пипетки, выключив образец цвета на странице](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Трехконтактный  
   :::column-end:::
   :::column span="1":::
      **Копировать в буфер**  
   :::column-end:::
   :::column span="2":::
      Скопируйте **Отображаемое значение** в буфер обмена.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      четырехпроцессорном  
   :::column-end:::
   :::column span="1":::
      **Отображаемое значение**  
   :::column-end:::
   :::column span="2":::
      Представление RGBA, HSLA или шестнадцатеричного представления цвета.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Цветовая палитра**  
   :::column-end:::
   :::column span="2":::
      Выберите один из квадратов, чтобы изменить цвет на этот квадрат.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      152  
   :::column-end:::
   :::column span="1":::
      **Отношения**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5-7  
   :::column-end:::
   :::column span="1":::
      **Opacity (Прозрачность)**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      No8  
   :::column-end:::
   :::column span="1":::
      **Переключатель отображения значений**  
   :::column-end:::
   :::column span="2":::
      Переключение между представлениями "RGBA", "HSLA" и "шестнадцатеричный" текущего цвета.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      @  
   :::column-end:::
   :::column span="1":::
      **Переключатель цветовой палитры**  
   :::column-end:::
   :::column span="2":::
      Переключение между [палитрой «дизайн материала][MaterialDesignColorSystem]», настраиваемой палитрой или палитрой цветов страницы.  DevTools создает цветовую палитру страницы на основе цветов, найденных в стилях.  
   :::column-end:::
:::row-end:::  

#### Выбор цвета на странице с помощью пипетки  

Когда вы откроете окно **выбора цвета**, по умолчанию будет включена **Пипетка** \ ( ![ Пипетка ][ImageEyedropperIcon] \).  Чтобы изменить выбранный цвет на другой цвет на странице, выполните указанные ниже действия.  

1.  Наведите указатель мыши на целевой цвет в окне просмотра.  
1.  Нажмите кнопку подтвердить.  
    
    > [!NOTE]
    > На приведенном ниже рисунке в **средстве выбора цвета** отображается текущее цветное значение `rgba(0,0,0,0.7)` , которое близко к черному.  Определенный цвет должен измениться на черную версию, которая выделена в окне просмотра, после того как вы выберете его.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Использование пипетки" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Использование пипетки  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Начало просмотра и изменения CSS | Документы Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Добавление PseudoState в класс — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Просмотр CSS для элемента — начало работы с просмотром и изменением CSS | Документы Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS) | Документы Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Создание доступного для чтения файла minified — Справка по отладке JavaScript | Документы Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Макет "Цветовая система-материал""  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель Box | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы выбора — "конкретное |" MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  