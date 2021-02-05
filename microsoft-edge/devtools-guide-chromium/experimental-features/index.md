---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: 32eaa3e8d41efefa669142297891e7c62cf4eb5b
ms.sourcegitcommit: d53421b7219ad87fa9d58f601d9c61ee44c2e43a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313467"
---
# Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся на стадии разработки.  Вы можете протестировать и [предоставить отзыв](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.  

Хотя экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.  

## Включить экспериментальные функции  

Чтобы включить экспериментальную функцию \(или off\) в Microsoft Edge, выполните следующие действия.  

1.  [Откройте DevTools.][DevtoolsOpenMain]  
    *   Выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  
1.  Откройте области ["Параметры".][DevToolsCustomizeIndexSettings]  
    *   Выберите `Shift` + `?` .  Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  
1.  В левой части **области** "Параметры" выберите раздел **"Эксперименты".**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница "Эксперименты" в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       Страница **"Эксперименты"** в **параметрах**  
    :::image-end:::  
    
1.  На странице **"Эксперименты"** прокрутите список всех доступных экспериментальных функций и выберите этот элемент рядом с каждой функцией, которую нужно протестировать.  
1.  Закроют и снова откроете Microsoft Edge DevTools.  
    
> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **"Эксперименты"** и скройте контрольный элемент экспериментальной функции, которую нужно отключить.  

## Основные экспериментальные функции  

В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Включить веб-вехин](#enable-webhint) | 85 или более поздней |  
| [Включить сетевую консоль](#enable-network-console) | 85 или более поздней |  
| [Просмотр исходных заказов](#source-order-viewer) | 86 или более поздней |  
| [Включить редактор сочетания клавиш](#enable-keyboard-shortcut-editor) | 87 или более поздней |  
| [Включить составные слои в 3D-представлении](#enable-composited-layers-in-3d-view) | 87 или более поздней |  
| [Включить новое средство редактора шрифтов в области стилей](#enable-new-font-editor-tool-within-the-styles-pane) | 89 или более поздней |  
| [Включить новые функции отладки CSS Flexbox](#enable-new-css-flexbox-debugging-features) | 89 или более поздней |  
| [Включить меню вкладок "+кнопка", чтобы открыть дополнительные инструменты](#enable--button-tab-menus-to-open-more-tools) | 89 или более поздней |  
| [Вкладка "Включить приветствие"](#enable-welcome-tool) | 89 или более поздней |  

### Включить новые функции отладки сетки CSS  

Эта экспериментальная функция предоставляет ряд новых визуализаций для отлаки макетов сетки CSS.  Чтобы просмотреть последние экспериментальные функции, в [этом эксперименте](#turn-on-experimental-features) необходимо включить и перезагрузить DevTools.  Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.  

#### Просмотр наложения сетки при наведении с помощью средства inspect  

Средство **Inspect** позволяет быстро определять и визуализировать макеты сетки CSS на веб-сайте, наведении на них указателя мыши.  Choose the **Inspect** \( ![ Inspect ](../media/inspect-icon.msft.png) \) icon in the top-left corner of DevTools.  Затем наведите курсор на элемент Grid на веб-сайте, который вы отладили.  Контуры отображаются вокруг сетки, а затенение указывает расположение разрывов сетки, если они присутствуют.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Просмотр сеток с помощью средства inspect" lightbox="../media/grid-inspect.msft.png":::
   Просмотр сеток с помощью **средства inspect**  
:::image-end:::  

#### Просмотр наложения сохраняемой сетки  

В Microsoft Edge версии 86 или более поздней версии экспериментальная функция сетки CSS также предлагает возможность включить постоянные наложения Grid.  Постоянные наложения предоставляют ряд преимуществ.  

*   Постоянные наложения остаются видимыми на странице при прокрутке, движении мыши и использовании других функций DevTools.  
*   Одновременно можно включить несколько постоянных наложения, что позволяет просмотреть несколько макетов сетки одновременно.  
*   Постоянные наложения предоставляют множество параметров конфигурации, таких как скрытие или отображение имен в области сетки, разрывы сетки, отслеживание размеров и так далее.  
    
Два способа переналожения сохраняемой сетки.  

*   Выберите **значок** овала Grid рядом с любым элементом Grid, показанным в дереве DOM **средства "Элементы".**  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Значок овала сетки в средстве "Элементы"" lightbox="../media/grid-adorner.msft.png":::
       Значок овала сетки в **средстве "Элементы"**  
    :::image-end:::  
    
*   Откройте новую панель **макета,** расположенную в средстве "Элементы", и выберите этот элемент рядом с каждым элементом Grid, который нужно выделить.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Панель** макета в DevTools  
    :::image-end:::  
    
#### Настройка постоянных наложения  

В Microsoft Edge версии 86 **** или более поздней версии новая панель **** макета расположена в средстве **"Элементы"** вместе со вкладками "Стили" и **"Вычисленные".**  Панель **макета** позволяет параметров конфигурации для постоянных наложения.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Функция отладки сетки CSS" lightbox="../media/experiments-grid.msft.png":::
   Функция отладки сетки CSS  
:::image-end:::  

### Поддержка перемещения вкладок между панелями  

Обычно такие средства, как **** **"Элементы"** и "Сеть", могут открываться только на главной панели, расположенной в верхней части DevTools.  Такие **средства, как трехмерный** просмотр и проблемы, которые обычно открываются только на панели "Drawer", расположенной в нижней части DevTools. **** ****  После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.  Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить** в верхнюю" или "Переместить **в нижнюю часть".**   Этот эксперимент позволяет настроить макет DevTools.  Чтобы отобразить или скрыть **панель "Drawer",** выберите `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить веб-вехин  

[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.  Тип обратной связи, предоставленный [веб-hint.][WebhintMain]  

*   специальные возможности  
*   совместимость между браузерами  
*   безопасность"  
*   производительность  
*   Progressive Web Apps (PWAs)  
*   другие распространенные проблемы веб-разработки  
    
В [эксперименте webhint][WebhintMain] на панели вопросов отображается обратная связь веб-вехи. [][DevtoolsIssues]  Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть **** соответствующую **области** **"Сеть",**"Источники" или "Элементы" в DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="обратная связь веб-панелей на панели "Проблемы"" lightbox="../media/experiments-webhint.msft.png":::
   обратная связь веб-панелей на **панели "Проблемы"**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить сетевую консоль  

**Сетовая** консоль — это рабочий заголовок эксперимента по запросам искусственных сетей по протоколу HTTP.  Вы можете использовать эксперимент **с сетевой** консолью для отправки запросов веб-API.  

После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.  Чтобы использовать **сетевую консоль,** выполните следующие действия.  

1.  Откройте **сетевую** области.  
1.  Найдите сетевой запрос, который вы хотите изменить, и повторно.  
1.  Откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Изменить **и повторить".**  
1.  Когда **откроется сетовая консоль,** отредактируете сведения о сетевом запросе.  
1.  Choose **Send**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Сетовая консоль в консоли" lightbox="../media/network-network-console.msft.png":::
   **Сетовая** консоль в **консоли**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Просмотр исходных заказов  

**"Просмотр порядка источника"** — это эксперимент, который отображает порядок элементов в источнике веб-страницы.  Порядок отображения на экране может отличаться от порядка источника, что приводит к путанице для чтения с экрана и пользователей клавиатуры.  Используйте эксперимент **"Просмотр порядка источника",** чтобы найти различия между порядком отображения на экране и порядком источника.  

После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.  Чтобы использовать **"Просмотр порядка источника",** выполните следующие действия.  

1.  Откройте средство **"Элементы".**  
1.  Откройте панель **"Accessibility"** (Доступность) на панели "Drawer \(bottom\)".  
1.  В разделе **"Просмотр порядка источника"** выберите **"Показать** порядок источника".  
1.  Выделите любой HTML-элемент, чтобы отобразить наложение, которое является порядком в источнике веб-страницы.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Source Order Viewer** in the **Accessibility** pane  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Включить редактор сочетания клавиш

Если включен **эксперимент** "Включить редактор сочетания клавиш", можно настроить сочетания клавиш для любого действия в DevTools.  Чтобы настроить сочетания клавиш для определенного действия, выполните следующие действия.  

1.  [Откройте DevTools.][DevtoolsOpenMain]  
1.  Откройте ["Параметры".][DevToolsCustomizeIndexSettings]  
    *   Выберите `Shift` + `?` .  
1.  Перейдите на **страницу ярлыков.**  
1.  Выберите действие, настраиваемую.  
1.  Choose the **Edit** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \) icon.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выбор действия для настройки на странице "Ярлыки" в параметрах" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Выбор действия для настройки на странице **"Ярлыки"** в [параметрах][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  На клавиатуре выберите клавиши для привязки к действию.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выбор ключей для назначения действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Выбор ключей для назначения действию  
    :::image-end:::  
    
1.  Чтобы сохранить новый ярлык клавиатуры, выберите пометку \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) значок.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Choose the checkmark icon to save your new keyboard shortcut" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Choose the checkmark icon to save your new keyboard shortcut  
    :::image-end:::  
    
1.  Выберите новый ярлык клавиатуры для запуска действия в DevTools.  
    
На странице **"Ярлыки"** значок настраиваемой клавиатуры **\(** ![ CustomKeyboardShortcut \) отображает настроенные сочетания ](../media/custom-keyboard-shortcut-icon.msft.png) клавиш.  Чтобы сбросить все ярлыки, выберите **"Восстановить ярлыки по умолчанию".**  

Чтобы отменить изменения при редактировании сочетания клавиш для действия, выберите значок X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  Чтобы добавить несколько ярлыков для действия, выберите **"Добавить ярлык".**  

> [!NOTE]
> Если ярлык клавиатуры в настоящее время назначен другому действию, вы не можете сохранить его для нового действия.  Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Включить составные слои в 3D-представлении  

Теперь можно визуализировать слои вместе с z-индексами и объектной моделью документа \(DOM\).  Эта функция помогает отлакить без переключения контекстов так часто.  Вы определили, что уменьшение переключения контекста является серьезной проблемой.  Не всегда понятно, как код, который вы пишете, влияет на веб-приложение.  Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.  

После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.  Чтобы использовать **составные слои,** выполните следующие действия.  

1.  В средстве **"3D View" (3D View) выберите его.**  
1.  Откройте области **составных** слоев.  
1.  Отображаются все закрашенные слои приложения.  Попробуйте эту функцию с собственными веб-приложениями.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   Панель **Составные слои**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Включить новое средство редактора шрифтов в области стилей  

Теперь для редактирования шрифтов [можно][DevtoolsInspectStylesEditFonts] использовать новый редактор визуальных шрифтов.  Используйте его для определения шрифтов и характеристик шрифтов.  Редактор **визуальных шрифтов** помогает выполнить следующие действия.  

*   Переключение между единицами для разных свойств шрифта  
*   Переключение между ключевыми словами для различных свойств шрифта  
*   Преобразование единиц  
*   Создание точного кода CSS  
    
После того как вы включите эксперимент, убедитесь, что перезапустите DevTools.  Чтобы использовать новый редактор **визуальных шрифтов,** выполните следующие действия.  

1.  Откройте средство **"Элементы".**  
1.  Откройте области **стилей.**  
1.  Выберите **значок редактора шрифтов.**  
    
Для получения дополнительных сведений о новом редакторе **визуальных**шрифтов перейдите к редактированию стилей и параметров шрифтов CSS в области стилей [в DevTools.][DevtoolsInspectStylesEditFonts]  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена визуальная области редактора шрифтов" lightbox="../media/font-editor-open.msft.png":::
   Выделена **визуальная** области редактора шрифтов  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Включить новые функции отладки CSS Flexbox  

Эта экспериментальная функция предоставляет множество новых визуализаций для отлажки макетов CSS Flexbox.  Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.  

#### Отображение постоянных наложения на макетах Flexbox с помощью средства inspect  

Средство **Inspect** позволяет быстро идентифицировать и визуализировать макеты CSS Flexbox на веб-сайте, наведите на них указатель мыши.  Choose the **Inspect** \( ![ Inspect ](../media/inspect-icon.msft.png) \) icon in the top-left corner of DevTools.  Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера Flex.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства inspect" lightbox="../media/flexbox-hover.msft.png":::
   Отображение контейнеров Flexbox с помощью средства **inspect**  
:::image-end:::  

#### Отображение постоянных наложения на макетах Flexbox  

В Microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения для макетов Flexbox.  Постоянные наложения предоставляют следующие преимущества.  

*   Постоянные наложения остаются видимыми на веб-странице при прокрутке, движении мыши и использовании других функций DevTools.
*   Можно использовать несколько постоянных наложения одновременно, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.  
*   Постоянные наложения предлагают параметры настройки цвета.  
    
Чтобы перебои в постоянных наложениях в макете Flexbox, используйте одно из следующих действий.  

*   Выберите **значок овала Flexbox** рядом с любым контейнером Flexbox, отображаемым в дереве DOM **средства Elements.**  
*   Откройте новую панель **макета,** расположенную в средстве **"Элементы",** и выберите этот элемент рядом с каждым контейнером Flexbox, который нужно выделить.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Гибкие значки и панель макета в DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Гибкие значки **и панель макета** в DevTools  
:::image-end:::  

#### Настройка постоянных наложения  

Чтобы настроить параметры постоянных наложения для сетки CSS или макетов Flexbox, используйте области **макета.**  The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   Панель макета  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Включить меню вкладок "+кнопка", чтобы открыть дополнительные инструменты  

Теперь можно открыть дополнительные средства с помощью нового значка "Дополнительные **средства"** `+` \( \).  После включения меню вкладки **"Включить+** кнопка", чтобы открыть эксперимент с дополнительными инструментами и перезагрузить DevTools, справа от группы вкладок в верхней части DevTools будет отображаться знак "плюс" \( `+` \).  Чтобы отобразить список других средств, которые можно добавить **** на вкладку, выберите новый значок "Дополнительные средства" `+` (\).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Дополнительные средства** в верхней области
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Включить средство приветствия

В этом эксперименте средство **"Что нового"** заменяется новым **средством приветствия.**  Он отображает обновленный дизайн для следующего содержимого.  

*   Ссылки на документы разработчика  
*   последние функции  
*   заметки о выпуске  
*   Возможность связаться с командой Разработчиков Microsoft Edge  
    
Средство **приветствия** открывается автоматически после каждого обновления Microsoft Edge.  Чтобы средство приветствия **** не отображались после каждого обновления, после каждого обновления **** под заголовком средства приветствия сберем его рядом с вкладками **"Открыть".**  

Если вы предпочитаете исходное средство **"Что** нового", перейдите к ["Экспериментам][DevtoolsCustomizeIndexSettings]с настройками" и удалите его рядом с вкладками "Включить  >  **** **приветствие".**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство приветствия" lightbox="../media/experiments-welcome.msft.png":::
   **Средство приветствия**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## Предыдущие экспериментальные функции  

*   [3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  
*   [Поддержка перемещения вкладок между][DevtoolsMoveTabs] панелями теперь доступна и включена по умолчанию в Microsoft Edge версии 85 или более поздней.  
*   [Настройка сочетания клавиш теперь][DevtoolsCustomKeyboardShortcuts] доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.  
*   [Эмуляция: поддержка режима двойного][DevtoolsDeviceModeDualScreenAndFoldables] экрана теперь доступна и включена по умолчанию в Microsoft Edge версии 89 или более поздней.  
*   [Включить новые функции отладки сетки CSS][DevtoolsCssGrid] теперь доступно и включено по умолчанию в Microsoft Edge версии 89 или более поздней.  
    
## Предоставление обратной связи по экспериментальным функциям  

Предоставление отзывов о экспериментах Microsoft Edge DevTools или других экспериментах, связанных с DevTools.  

*   Отправьте свой отзыв с помощью **значка отправки отзыва** в DevTools  
*   Твит на [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   Значок **отправки отзыва** в Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверка сетки CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsMoveTabs]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств в режиме устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области стилей в devTools | Документы Майкрософт"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools keyboard shortcuts | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для двухэкранного обнаружения | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Папка | Сума"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
