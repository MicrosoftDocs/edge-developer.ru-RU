---
description: Откройте для себя новые процессы просмотра и изменения CSS в Microsoft Edge DevTools.
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 84aacbb3961f6b8f6e9a0bda8823fecbbb26ec25
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439305"
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

# <a name="css-reference"></a>Справочник по CSS  

Откройте для себя новые процессы в следующей комплексной ссылке на функции Microsoft Edge DevTools, связанные с просмотром и изменением CSS.  

Чтобы узнать основы, перейдите к [началу работы с просмотром и изменением CSS][DevToolsCSSGetStarted].  

## <a name="choose-an-element"></a>Выбор элемента  

Средство **Elements** devTools позволяет просматривать или изменять CSS одного элемента одновременно.  Выбранный элемент выделен в **дереве DOM.**  Стили элемента показаны в области **Стилей.**  Для руководства перейдите к [просмотру CSS для элемента][DevToolsCSSGetStartedTutorial].  

> [!NOTE]
> На следующем рисунке выбран элемент, который выделен в `h1` **дереве DOM.**  Справа стили элемента показаны в области **Стилей.**  Слева элемент выделяется в представлении, но только потому, что мышь в настоящее время нависает над ней в **dom Tree**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Пример выбранного элемента" lightbox="../media/css-elements-styles-h1.msft.png":::
   Пример выбранного элемента  
:::image-end:::  

Для выбора элемента используйте одно из следующих действий.  

*   В представлении наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
*   В DevTools выберите элемент **\(** Выберите элемент \) или выберите ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) или `Command` + `Shift` + `C` \(macOS\), а затем выберите элемент в представлении.  
*   В DevTools выберите элемент **dom Tree**.  
*   В DevTools запустите запрос, как в консоли, наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите панель `document.querySelector('p')` **Reveal in Elements** ****.  

## <a name="view-css"></a>Просмотр CSS  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a>Просмотр таблицы внешних стилей, где определено правило  

В области **Стилей** выберите ссылку рядом с правилом CSS, чтобы открыть таблицу внешних стилей, определяемую правилом.  

Если таблица стилей минирована, перейдите, [чтобы сделать минированную папку читаемой.][DevToolsJavascriptReferenceFormat]  

> [!NOTE]
> На следующем рисунке после выбора вы перенастроили строку 2 из, где определено правило `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` `.content h1:first-of-type` CSS.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Просмотр таблицы стилей, в которой определено правило" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Просмотр таблицы стилей, в которой определено правило  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a>Просмотр только CSS, который фактически применяется к элементу  

На **панели Стилей** показаны все правила, применимые к элементу, включая переопределяемые объявления.  Если вы не заинтересованы в переопределяемом объявлении, используйте **панель Computed** для просмотра только CSS, который на самом деле применяется к элементу.  

1.  [Выберите элемент](#choose-an-element).  
1.  Перейдите к **панели Computed** в **инструменте Elements.**  

> [!NOTE]
> В широком окне DevTools панель **Computed** не существует.  Содержимое панели **Computed отображается** на панели **Styles.**  

Унаследованные свойства непрозрачны.  Чтобы отобразить все унаследованные значения, выберите контрольный ящик **Show All.**  

> [!NOTE]
> На следующем рисунке на панели **Computed** показаны свойства CSS, применяемые к выбранному в настоящее время `h1` элементу.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Панель Computed" lightbox="../media/css-elements-computed-h1.msft.png":::
   Панель **Computed**  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a>Просмотр свойств CSS в алфавитном порядке  

Используйте **панель Computed.**  Перейдите [к просмотру только CSS, который фактически применяется к элементу.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-inherited-css-properties"></a>Просмотр унаследованных свойств CSS  

Проверьте **контрольный ящик Show All** в **панели Computed.**  Перейдите [к просмотру только CSS, который фактически применяется к элементу.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-the-box-model-for-an-element"></a>Просмотр модели окна для элемента  

Чтобы [просмотреть модель элемента полей,][MDNBoxModel] перейдите на панель **Стилей.**  Если окно DevTools узкое, диаграмма **Box Model** находится в нижней части панели.  

Выберите и измените значение для изменения значения.  

> [!NOTE]
> На следующем рисунке диаграмма **Box Model** на панели **Стилей** показывает модель окна для выбранного `h1` элемента.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Схема модели box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Схема **модели box**  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a>Поиск и фильтрация CSS элемента  

Для поиска **определенных** свойств **** или значений CSS используйте текстовое поле Filter на панелях **Стилей** и Вычислительные панели.  

Чтобы также найти унаследованные свойства в **панели Computed,** проверьте контрольный ящик **Show All.**  

> [!NOTE]
> На следующем рисунке панель **Стилей** фильтруется, чтобы показывать только правила, которые включают запрос `color` поиска.  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Фильтр панели Стилей" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Фильтр панели **Стилей**  
:::image-end:::  

> [!NOTE]
> На следующем рисунке панель **Computed** фильтруется, чтобы показывать только объявления, которые включают запрос `100%` поиска.  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Фильтр вычислительной панели" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Фильтр **вычислительной панели**  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a>Toggle a pseudo-class  

Выполните следующие действия, чтобы переохитрить псевдокласс, например `:active` `:focus` , или `:hover` `:visited` .  

1.  [Выберите элемент](#choose-an-element).  
1.  В **инструменте Elements** перейдите на панель **Стилей.**  
1.  Выберите **:hov**.  
1.  Проверьте псевдокласс, который необходимо включить.  

> [!NOTE]
> На следующем рисунке переохитрить `:hover` псевдокласс.  В viewport убедитесь, что объявление применяется к элементу, даже если элемент фактически не `background-color: cornflowerblue` зависает.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Toggle the :hover pseudo-class" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Toggle the `:hover` pseudo-class  
:::image-end:::  

Для интерактивного руководства перейдите к [добавлению псевдостата в класс.][DevToolsCSSGetStartedAddPseudoState]  

### <a name="view-a-page-in-print-mode"></a>Просмотр страницы в режиме печати  

Выполните следующие действия, чтобы просмотреть страницу в режиме печати.  

1.  [Откройте командное меню.][DevToolsCommandMenu]  
1.  Начните `Rendering` вводить и выберите `Show Rendering` .  
1.  Для **выпадаемой CSS Media** эмулировать выберите **печать**.  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a>Просмотр используемой и неиспользоваемой CSS с помощью средства Coverage  

Средство **Coverage** показывает, что на самом деле использует CSS страницы.  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) [][DevToolsCommandMenu]в то время как DevTools находится в центре внимания, чтобы открыть командное меню .  
1.  Начните `coverage` вводить текст и **выберите показать охват**.  Появляется **средство Coverage.**  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Открытие средства Coverage из командного меню" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Откройте средство **Coverage** из **командного меню**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Средство Coverage" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             Средство **Coverage**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Выберите **охват Начните инструментарий и обновите** страницу \. Начните использовать инструменты ![ и обновите ](../media/refresh-icon.msft.png) страницу \).  Страница обновляется, а средство **coverage** предоставляет обзор того, сколько CSS \(и JavaScript\) используется из каждого файла, загруженного браузером.  Зеленый представляет используемый CSS.  Красный цвет представляет неиспользована CSS.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Обзор того, сколько CSS (и JavaScript) используется и не используется" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Обзор того, сколько CSS \(и JavaScript\) используется и не используется  
    :::image-end:::  

1.  Чтобы отобразить по очереди разбивку того, что используется CSS, выберите CSS-файл.  
    
    > [!NOTE]
    > На следующем рисунке не используются строки от 145 до 147 и 149 до 151, в то время как используются строки `b66bc881.site-ltr.css` от 163 до 166.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Разбивка по очереди используемого и неиспользованого CSS" lightbox="../media/css-sources-css-coverage.msft.png":::
       Разбивка по очереди используемого и неиспользованого CSS  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a>Режим предварительного просмотра принудительной печати  

Перейдите [к Force DevTools в режиме предварительного просмотра печати.][DevToolsCssPrintPreview]  

## <a name="change-css"></a>Изменение CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a>Добавление объявления CSS в элемент  

Порядок объявлений влияет на стиль элемента, используйте следующий список, чтобы помочь вам добавлять объявления по-разному.  

*   [Добавление встройного объявления.](#add-an-inline-declaration)  Эквивалентно `style` добавлению атрибута в HTML элемента.  
*   [Добавьте объявление в правило стиля](#add-a-declaration-to-a-style-rule).  

**Какой рабочий процесс следует использовать?** В большинстве сценариев, вероятно, необходимо использовать рабочий процесс inline declaration.  Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.  Дополнительные сведения о специфике перейдите к [типам Selector.][MDNSelectorTypes]  

Если вы отладили все стили элемента и вам необходимо специально проверить, что происходит при определении объявления в разных местах, используйте другой рабочий процесс.  

#### <a name="add-an-inline-declaration"></a>Добавление встройного объявления  

Выполните следующие действия, чтобы добавить встройное объявление.  

1.  [Выберите элемент](#choose-an-element).  
1.  В области **Стилей** выберите между скобками раздела **element.style.**  Курсор фокусируется, позволяя вводить текст.  
1.  Введите имя свойства и выберите `Enter` .  
1.  Введите допустимые значения для этого свойства и выберите `Enter` .  В **дереве DOM убедитесь,** что атрибут `style` был добавлен в элемент.  

> [!NOTE]
> На следующем рисунке свойства и свойства были применены к `margin-top` `background-color` выбранному элементу.  В **дереве DOM убедитесь,** что объявления отражаются в `style` атрибуте элемента.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Добавление встройных деклараций" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Добавление встройных деклараций  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a>Добавление объявления в правило стиля  

Выполните следующие действия, чтобы добавить объявление в существующее правило стиля.  

1.  [Выберите элемент](#choose-an-element).  
1.  В области **Стилей** выберите между скобками правила стиля, к которому необходимо добавить объявление.  Курсор фокусируется, позволяя вводить текст.  
1.  Введите имя свойства и выберите `Enter` .  
1.  Введите допустимые значения для этого свойства и выберите `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Добавление объявления в правило стиля" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Добавление `border-bottom-style:groove` объявления в правило стиля  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a>Изменение имени или значения объявления  

Выберите и измените имя или значение объявления, чтобы изменить его.  Для ярлыков для быстрого приращения или приумноживления значения на `0.1` , `1` , или `10` `100` единицы, перейдите к [изменению](#change-declaration-values-with-keyboard-shortcuts)значений объявления с помощью клавиши ярлыки .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Изменение значения объявления" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Изменение значения `border-bottom-style` объявления  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a>Изменение значений объявления с помощью ярлыков клавиатуры  

При редактировании значения объявления можно использовать следующие клавиши, чтобы приумнозить значение на определенную сумму.  

*   Выберите `Alt` + `Up` \(Windows, Linux\) `Option` + `Up` или \(macOS\) для приращения путем `0.1` .  
*   Выберите изменение значения путем или путем, если `Up` `1` `0.1` текущее значение находится между `-1` и `1` .  
*   Выберите `Shift` + `Up` для приращения `10` путем .  
*   Выберите `Shift` + `Page Up` \(Windows, Linux\) `Shift` + `Command` + `Up` или \(macOS\) `100` для приумнождения значения путем .  

Приумножная работа также работает.  Просто замените каждый экземпляр `Up` упомянутых выше `Down` .  

### <a name="add-a-class-to-an-element"></a>Добавление класса в элемент  

Выполните следующие действия, чтобы добавить класс в элемент.  

1.  [Выберите элемент dom](#choose-an-element) **Tree**.  
1.  Выберите **.cls**.  
1.  Введите имя класса в текстовом окне **Добавить новый** класс.  
1.  Выберите `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Области классов элементов" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Области **классов** элементов  
:::image-end:::  

### <a name="toggle-a-class"></a>Toggle a class  

Выполните следующие действия, чтобы включить или отключить класс элемента.  

1.  [Выберите элемент dom](#choose-an-element) **Tree**.  
1.  Откройте области **классов** элементов.  Перейдите [к добавлению класса к элементу.](#add-a-class-to-an-element)  В **текстовом окне Добавить** новый класс приведены все классы, применяемые к конкретному элементу.  
1.  Переключите контрольный ящик рядом с классом, который необходимо включить или отключить.  

### <a name="add-a-style-rule"></a>Добавление правила стиля  

Выполните следующие действия, чтобы добавить новое правило стиля.  

1.  [Выберите элемент](#choose-an-element).  
1.  Выберите **новое правило стиля** \. Новое правило стиля ![ ](../media/new-style-rule-icon.msft.png) \).  DevTools вставляет новое правило под **правилом element.style.**  

> [!NOTE]
> На следующем рисунке DevTools добавляет правило стиля после `h1.devsite-page-title` выбора **правила New Style.**  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Добавление нового правила стиля" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Добавление нового правила стиля  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a>Выберите таблицу стилей, чтобы добавить правило  

При [добавлении](#add-a-style-rule)нового правила стиля выберите и удерживайте правило **New Style** \( New Style Rule \) для выбора таблицы стилей для добавления ![ правила ](../media/new-style-rule-icon.msft.png) стиля.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Выберите таблицу стилей" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Выберите таблицу стилей  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a>Добавление правила стиля в определенное расположение  

Выполните следующие действия, чтобы добавить правило стиля в определенное расположение в панели **Стилей.**  

1.  Наведите курс на правило стиля, которое находится непосредственно над тем, где необходимо добавить новое правило стиля.  
1.  [ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).  
1.  Выберите **Правило стиля вставки ниже** \. ![ Вставить правило стиля ниже значок ](../media/new-style-rule-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Вставьте правило стиля ниже" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Вставьте правило стиля ниже**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a>Раскрой панель инструментов More Actions  

Панель **инструментов More Actions** позволяет выполнять следующие действия.  

*   Вставьте правило стиля непосредственно под тем, на который вы ориентированы.  
*   Добавьте `background-color` , `color` или объявление к `box-shadow` `text-shadow` правилу стиля, на который вы ориентированы.  

Выполните следующие действия, чтобы выявить панель **инструментов More Actions.**  

1.  В панели **Стилей** введите правило стиля.  **Дополнительные** действия `...` \( \) раскрыты в нижнем правом разделе правила стиля.  
    
    > [!NOTE]
    > На следующей фигуре наведите курс на правило стиля, и в нижнем правом разделе правила стиля будет обнаружено больше `.header-holder.has-default-focus` действий. ****  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Раскрыть дополнительные действия" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       **Раскрой дополнительные** действия `...` \( \)  
    :::image-end:::  
    
1.  Наведите **курсор на дополнительные** действия `...` \( \) для раскрытия указанных выше действий.  
    
    > [!NOTE]
    > Действие **Insert Style Под действием вставляется** после нависания над **дополнительными действиями.**  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Панель инструментов More Actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Панель **инструментов More Actions**  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a>Toggle a declaration  

Выполните действия folllwoing, чтобы переключение одной декларации на \(или off\).  

1.  [Выберите элемент](#choose-an-element).  
1.  В области **Стилей** наведите курсор на правило, определя которое определяет объявление.  Рядом с каждым объявлением отображается почтовый ящик.  
1.  Проверьте \(или разгрузку\) почтовый ящик рядом с объявлением.  При отладке объявления DevTools пересекает его, чтобы указать, что она больше не активна.  

> [!NOTE]
> На следующем рисунке свойство для выбранного в настоящее время элемента `margin-top` отключено.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Toggle a declaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Toggle a declaration  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a>Добавление объявления фонового цвета  

Выполните следующие действия, чтобы `background-color` добавить в элемент объявление.  

1.  Наведите курс на правило стиля, в которое нужно добавить `background-color` объявление.  
1.  [ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).  
1.  Выберите **Добавить фоновый** цвет \. ![ Добавьте значок фонового ](../media/add-background-color-icon.msft.png) цвета \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Добавление фонового цвета" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Добавление фонового цвета**  
:::image-end:::  

### <a name="add-a-color-declaration"></a>Добавление объявления цвета  

Выполните следующие действия, чтобы `color` добавить в элемент объявление.  

1.  Наведите курс на правило стиля, в которое нужно добавить `color` объявление.  
1.  [ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).  
1.  Выберите **Добавить цвет** \. Добавить ![ значок цвета ](../media/add-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Добавление цвета" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Добавление цвета**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a>Добавление объявления box-shadow  

Выполните следующие действия, чтобы `box-shadow` добавить в элемент объявление.  

1.  Наведите курс на правило стиля, в которое нужно добавить `box-shadow` объявление.  
1.  [ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).  
1.  Выберите **Добавить поле Shadow** \. Добавьте ![ значок Тень окна ](../media/add-box-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Добавление тени box" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Добавление тени box**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a>Добавление объявления text-shadow  

Выполните следующие действия, чтобы `text-shadow` добавить в элемент объявление.  

1.  Наведите курс на правило стиля, в которое нужно добавить `text-shadow` объявление.  
1.  [ **Раскрой панель инструментов More Actions** ](#reveal-the-more-actions-toolbar).  
1.  Выберите **Добавить текстовую тень** \. Добавьте ![ значок Text Shadow ](../media/add-text-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Добавление тени текста" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Добавление тени текста**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a>Изменение цветов с помощью выборки цвета  

Выбор **цвета предоставляет** GUI для изменений и `color` `background-color` объявлений.  

Выполните следующие действия, чтобы открыть **выбор цвета.**  

1.  [Выберите элемент](#choose-an-element).  
1.  В панели **Стилей** найдите `color` или `background-color` аналогичное объявление, которое необходимо изменить.  Слева от значения , или аналогичного значения, имеется небольшой квадрат, который является `color` `background-color` предварительным просмотром цвета.  
    
    > [!NOTE]
    > На следующем рисунке небольшой квадрат слева `rgba(0, 0, 0, 0.7)` — это предварительный просмотр этого цвета.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Цвет предварительного просмотра" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Цвет предварительного просмотра  
    :::image-end:::  
    
1.  Выберите предварительный просмотр, чтобы **открыть выбор цвета**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Выбор цвета" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       Выбор **цвета**  
    :::image-end:::  
    
Следующая фигура и список descries каждого из элементов пользовательского интерфейса **в color Picker**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Выбор цвета, аннотированный" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   Выбор **цвета,** аннотированный  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
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
      **Eyedropper**  
   :::column-end:::
   :::column span="2":::
      Дополнительные сведения можно получить в примере цвета со [страницы с помощью eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3  
   :::column-end:::
   :::column span="1":::
      **Копировать в буфер**  
   :::column-end:::
   :::column span="2":::
      Скопируйте **значение Display в** буфер обмена.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4  
   :::column-end:::
   :::column span="1":::
      **Отображение значения**  
   :::column-end:::
   :::column span="2":::
      Представление цвета RGBA, HSLA или Hex.  
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
      6  
   :::column-end:::
   :::column span="1":::
      **Hue**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      7  
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
      8  
   :::column-end:::
   :::column span="1":::
      **Переключатель отображения значений**  
   :::column-end:::
   :::column span="2":::
      Перетасковка между представлениями RGBA, HSLA и Hex текущего цвета.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **Коммутатор цветовой палитры**  
   :::column-end:::
   :::column span="2":::
      Перегиб между палитрой [material Design,][MaterialDesignColorSystem]настраиваемой палитрой или палитрой цветов страниц.  DevTools создает цветовую палитру страниц на основе цветов, которые он находит в таблицах стилей.  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a>Пример цвета со страницы с помощью Eyedropper  

Когда вы открываете **Выбор цвета,** **Eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) находится на по умолчанию.  Выполните следующие действия, чтобы изменить выбранный цвет на другой цвет на странице.  

1.  Наведите курсор на целевой цвет в представлении.  
1.  Выберите подтверждение.  
    
    > [!NOTE]
    > На следующем рисунке в **списке цветов** указывается текущее значение цвета `rgba(0,0,0,0.7)` , близкое к черному.  Определенный цвет должен измениться на версию черного цвета, которая в данный момент выделяется в представлении после его выборки.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Использование eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Использование eyedropper  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCSSGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Добавление псевдостата в класс . Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Просмотр CSS для элемента . Начало работы с просмотром и изменением CSS | Документы Майкрософт"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Force Microsoft Edge DevTools into Print Preview Mode (CSS Print Media Type) | Документы Майкрософт"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Сделайте минированную папку читаемой — отладка ссылки javaScript | Документы Майкрософт"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Цветовая система — material Design"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель окна | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы селекторов — | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/css/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  