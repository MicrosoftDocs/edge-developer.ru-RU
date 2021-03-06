---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398681"
---
# <a name="experimental-features"></a>Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся в разработке.  Вы можете протестировать и [предоставить обратную связь](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.  

В то время как экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Включаем экспериментальные функции  

Чтобы включить экспериментальные функции \(или off\) в Microsoft Edge, выполните следующие действия.  

1.  [Откройте DevTools][DevtoolsOpenMain].  
    *   Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevToolsShortcuts]  
1.  Откройте области [Параметры.][DevToolsCustomizeIndexSettings]  
    *   Выберите `Shift` + `?` .  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevToolsShortcuts]  
1.  На левой стороне области **Параметры** выберите раздел **Эксперименты.**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница Эксперименты в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       Страница **Эксперименты** в **параметрах**  
    :::image-end:::  
    
1.  На странице **Эксперименты** прокрутите список всех доступных экспериментальных функций и выберите почтовый ящик рядом с каждой функцией, которую необходимо протестировать.  
1.  Закрыть и открыть Microsoft Edge DevTools.  
    
> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **Эксперименты** и закройте контрольный ящик экспериментальной функции, которую необходимо отключить.  

## <a name="highlighted-experimental-features"></a>Основные экспериментальные функции  

В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Включить веб-хинт](#enable-webhint) | 85 или более поздней |  
| [Включить консоль сети](#enable-network-console) | 85 или более поздней |  
| [Source Order Viewer](#source-order-viewer) | 86 или более поздней |  
| [Включить редактор ярлыка клавиатуры](#enable-keyboard-shortcut-editor) | 87 или более поздней |  
| [Включить композитные слои в 3D-представлении](#enable-composited-layers-in-3d-view) | 87 или более поздней |  
| [Включить новый инструмент редактора шрифта в области Стилей](#enable-new-font-editor-tool-within-the-styles-pane) | 89 или более поздней |  
| [Включить новые функции отладки CSS Flexbox](#enable-new-css-flexbox-debugging-features) | 89 или более поздней |  
| [Включить меню вкладок + кнопки, чтобы открыть дополнительные средства](#enable--button-tab-menus-to-open-more-tools) | 89 или более поздней |  
| [Включить вкладку Welcome](#enable-welcome-tool) | 89 или более поздней |  

### <a name="enable-new-css-grid-debugging-features"></a>Включить новые функции отладки сетки CSS  

Эта экспериментальная функция предоставляет ряд новых визуализаций, которые помогут отламыть макеты сетки CSS.  Чтобы просмотреть последние экспериментальные функции, в этом [эксперименте необходимо](#turn-on-experimental-features) включить и перезагрузить DevTools.  Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a>Просмотр нависайки сетки с помощью средства Inspect  

Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Grid на веб-сайте, нависая над ними с помощью мыши.  Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.  Затем наведите курсор `Grid` на элемент на отладке веб-страницы.  Контуры отображаются вокруг сетки, а штриховка указывает расположение пробелов сетки, если она присутствует.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Просмотр сетки с помощью средства Inspect" lightbox="../media/grid-inspect.msft.png":::
   Просмотр сетки с помощью **средства Inspect**  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a>Просмотр настойчивых накладок сетки  

В версии Microsoft Edge 86 или более поздней версии экспериментальная функция сетки CSS также предлагает возможность включить постоянные наложения сетки.  Постоянные наложения предоставляют несколько преимуществ.  

*   Постоянные наложения остаются видимыми на странице при прокрутке, движении мыши и использовании других функций DevTools.  
*   Одновременно может быть включено несколько постоянных накладок, что позволяет просмотреть несколько макетов сетки одновременно.  
*   Постоянные наложения предлагают множество вариантов конфигурации, таких как сокрытие или отображение имен в области сетки, пробелы в сетке, размеры трассы и так далее.  
    
Два способа для наложения на настойчивые сетки.  

*   Выберите **значок овал** Grid рядом с любым элементом Grid, показанным в дереве DOM **средства Elements.**  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Значок Grid oval в инструменте Elements" lightbox="../media/grid-adorner.msft.png":::
       Значок Grid oval в **инструменте Elements**  
    :::image-end:::  
    
*   Откройте новую панель **Макета,** расположенную в средстве Elements, и выберите контрольный ящик рядом с каждым элементом Grid, который необходимо выделить.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Панель макета** в DevTools  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a>Настройка постоянных накладок  

В microsoft Edge версии 86 или более поздней версии новая панель **** **Layout** расположена в инструменте **Elements** наряду со стилями и **вычислительными** панелями.  Панель **Макета** позволяет параметров конфигурации для настойчивых наложения.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Функция отладки сетки CSS" lightbox="../media/experiments-grid.msft.png":::
   Функция отладки сетки CSS  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a>Включить поддержку для перемещения вкладок между панелями  

Обычно такие средства, как **Elements** и **Network,** могут открываться только в основной панели, расположенной в верхней части DevTools.  Такие **инструменты, как 3D View** и **Issues,** которые обычно открываются только в панели **ящиков,** расположенных в нижней части DevTools.  После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.  Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Переместить** вверх или **Переместить в нижнее**.   Этот эксперимент позволяет настроить макет DevTools.  Чтобы отобразить или скрыть панель **ящиков,** выберите `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение инструментов между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   Перемещение инструментов между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a>Включить веб-хинт  

[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.  Тип обратной связи, предоставляемый [веб-сайтом][WebhintMain].  

*   специальные возможности  
*   совместимость между браузерами  
*   безопасность"  
*   производительность  
*   Прогрессивные веб-приложения (PWAs)  
*   другие распространенные проблемы веб-разработки  
    
Эксперимент [webhint][WebhintMain] отображает обратную связь веб-хинта в панели [Issues.][DevtoolsIssues]  Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем сайте.  Выберите ссылку на ресурс, чтобы открыть **соответствующую**сеть, **источники**или **элементов** в DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   webhint feedback in the **Issues** panel  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a>Включить консоль сети  

**Network Console** — это рабочее название эксперимента по синтетическому запросу сети по HTTP.  Вы можете использовать эксперимент **сетевой консоли** для отправки запросов веб-API.  

После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Для использования **сетевой консоли**выполните следующие действия.  

1.  Откройте **области Сети.**  
1.  Найдите сетевой запрос, который необходимо изменить и повторно изменить.  
1.  Откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.  
1.  При **открываемой сетевой** консоли отредактируете сведения о запросе сети.  
1.  Выберите **Отправить**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Консоль сети в ящике консоли" lightbox="../media/network-network-console.msft.png":::
   **Консоль сети** в **ящике консоли**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a>Source Order Viewer  

**Source Order Viewer** — это эксперимент, который отображает порядок элементов в источнике веб-страницы.  Порядок отображения на экране может отличаться от порядка источника, что сбивает с толку читателя экрана и пользователей клавиатуры.  Чтобы **найти** различия между порядком отображения на экране и порядком источника, используйте эксперимент по просмотру исходных порядков.  

После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Чтобы использовать **viewer source order,** выполните следующие действия.  

1.  Откройте **средство Elements.**  
1.  Откройте панель **доступности** в панели ящика \(bottom\) .  
1.  В разделе **Просмотр источника порядка** выберите почтовый ящик Показать **исходный** порядок.  
1.  Выделение любого элемента HTML для отображения наложения, указываемой на источник веб-страницы.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Для просмотра исходных заказов в области доступности" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Для просмотра исходных заказов** в **области доступности**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a>Включить редактор ярлыка клавиатуры

С **включенным экспериментом редактора** ярлыков включить клавиши включить, вы можете настроить ярлыки клавиатуры для любого действия в DevTools.  Чтобы настроить ярлык клавиатуры для определенного действия, выполните следующие действия.  

1.  [Откройте DevTools][DevtoolsOpenMain].  
1.  Open [Settings][DevToolsCustomizeIndexSettings].  
    *   Выберите `Shift` + `?` .  
1.  Перейдите на **страницу Ярлыки.**  
1.  Выберите действие, необходимое для настройки.  
1.  Выберите **значок Edit** \( ![ EditKeyboardShortcut\). ](../media/edit-keyboard-shortcut-icon.msft.png)  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выберите действие для настройки со страницы Ярлыки в Параметры" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Выберите действие для настройки со страницы **Ярлыки** в [Параметры][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  На клавиатуре выберите клавиши для привязки к действию.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выберите клавиши, которые необходимо назначить действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Выберите клавиши, которые необходимо назначить действию  
    :::image-end:::  
    
1.  Чтобы сохранить новый ярлык клавиатуры, выберите контрольный знак \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) значок.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Выберите значок контрольных знаков, чтобы сохранить новый ярлык клавиатуры" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Выберите значок контрольных знаков, чтобы сохранить новый ярлык клавиатуры  
    :::image-end:::  
    
1.  Выберите новый ярлык клавиатуры, чтобы вызвать действие в DevTools.  
    
На странице **Ярлыки** значок Custom **Keyboard Shortcut** ![ \( CustomKeyboardShortcut \) отображает настроенные ](../media/custom-keyboard-shortcut-icon.msft.png) клавиши клавиш.  Чтобы сбросить все ярлыки, выберите восстановление ярлыков **по умолчанию.**  

Чтобы отменить изменения при редактировании клавиш для действия, выберите значок X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut\). ](../media/delete-keyboard-shortcut-icon.msft.png)  Чтобы добавить несколько ярлыков для действия, выберите **Добавить ярлык**.  

> [!NOTE]
> Если ярлык клавиатуры в настоящее время назначен другому действию, вы не можете сохранить его для нового действия.  Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a>Включить композитные слои в 3D-представлении  

Теперь можно визуализировать Слои вместе с индексами z и объектной моделью документа \(DOM\).  Эта функция позволяет отключить, не переключая контексты так часто.  Вы определили, что уменьшение переключения контекста является основной проблемой.  Не всегда понятно, как код, который вы пишете, влияет на ваше веб-приложение.  Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.  

После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Чтобы использовать **композитные слои,** выполните следующие действия.  

1.  В ящике выберите **средство 3D View.**  
1.  Откройте области **Композитные слои.**  
1.  Отображаются все расписные слои приложения.  Попробуйте эту функцию с помощью собственных веб-приложений.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   Панель **Составные слои**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a>Включить новый инструмент редактора шрифта в области Стилей  

Теперь для редактирования шрифтов можно использовать новый визуальный [редактор][DevtoolsInspectStylesEditFonts] шрифтов.  Используйте его для определения шрифтов и характеристик шрифтов.  Визуальный **редактор шрифта** помогает выполнить следующие действия.  

*   Переключение между единицами для различных свойств шрифта  
*   Переключатель между ключевыми словами для различных свойств шрифта  
*   Преобразование единиц  
*   Создание точного кода CSS  
    
После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Чтобы использовать новый визуальный **редактор шрифтов,** выполните следующие действия.  

1.  Откройте **средство Elements.**  
1.  Откройте области **стилей.**  
1.  Выберите **значок Редактор шрифта.**  
    
Дополнительные сведения о новом редакторе визуальных шрифтов **перейдите**к редактированию стилей и параметров шрифта CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена поле редактора визуальных шрифтов" lightbox="../media/font-editor-open.msft.png":::
   Выделена поле **редактора** визуальных шрифтов  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a>Включить новые функции отладки CSS Flexbox  

Эта экспериментальная функция предоставляет множество новых визуализаций, которые помогут отламыть макеты CSS Flexbox.  Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Отображение постоянных наложения на макеты Flexbox с помощью средства Inspect  

Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Flexbox на веб-сайте, зависая на них с помощью мыши.  Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.  Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера flex.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства Inspect" lightbox="../media/flexbox-hover.msft.png":::
   Отображение контейнеров Flexbox с помощью средства **Inspect**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Отображение настойчивых наложения на макеты Flexbox  

В microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения на макеты Flexbox.  Постоянные наложения предоставляют следующие преимущества.  

*   Постоянные наложения остаются видимыми на веб-странице во время прокрутки, перемещения мыши и использования других функций DevTools.
*   Одновременно можно использовать несколько настойчивых накладок, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.  
*   Постоянные наложения предлагают параметры цветовой конфигурации.  
    
Чтобы отладить постоянные наложения на макет Flexbox, используйте одно из следующих действий.  

*   Выберите **значок овального** ящика Flexbox рядом с любым контейнером Flexbox, отображаемым в дереве DOM средства **Elements.**  
*   Откройте новую панель **Макета,** расположенную в средстве **Elements,** и выберите контрольный ящик рядом с каждым контейнером Flexbox, который необходимо выделить.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex icons and Layout panel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Flex icons and **Layout** panel in DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Настройка постоянных наложения  

Чтобы настроить параметры для настойчивых накладок для сетки CSS или макетов Flexbox, используйте **области макета.**  Области **макета** расположен в **инструменте Elements** рядом со **стилями** и **вычислительными** стемнами.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   Панель макета  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a>Включить меню вкладок + кнопки, чтобы открыть дополнительные средства  

Теперь можно открыть дополнительные средства с помощью нового значка **More Tools** `+` \( \) .  После включения меню вкладок **Включить +** кнопки, чтобы открыть дополнительные средства эксперимента и перезагрузить DevTools, плюс знак \( \) отображает справа от группы вкладок в верхней части `+` DevTools.  Чтобы отобразить список других средств, которые можно добавить в вкладку, выберите значок **More Tools** `+` \( \) .  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Дополнительные средства** в верхней области
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a>Включить средство Welcome

Этот эксперимент заменяет средство **What's New** новым средством **Welcome.**  Он отображает обновленный дизайн для следующего контента.  

*   Ссылки на документы разработчика  
*   последние функции  
*   заметки о выпуске  
*   Возможность связаться с командой Microsoft Edge DevTools  
    
Средство **Welcome** автоматически открывается после каждого обновления microsoft Edge.  Чтобы предотвратить отображение средства **Welcome** после каждого обновления, закройте почтовый ящик рядом с вкладками **Open** после каждого обновления под заголовком **Welcome** tool.  

Если вы предпочитаете оригинальный инструмент **What's New,** перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и удалите почтовый ящик рядом со вкладками  >  **** **Enable Welcome.**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство welcome" lightbox="../media/experiments-welcome.msft.png":::
   **Средство welcome**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Предыдущие экспериментальные функции  

*   [3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в microsoft Edge версии 83 или более поздней версии.  
*   [Включив поддержку, чтобы][DevtoolsMoveTabs] переместить вкладки между панелями, теперь доступна и включена по умолчанию в microsoft Edge версии 85 или более поздней версии.  
*   [Настройка ярлыков клавиатуры][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в microsoft Edge версии 86 или более поздней версии.  
*   [Эмуляция. Поддержка режима двойного экрана][DevtoolsDeviceModeDualScreenAndFoldables] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.  
*   [Включив новые функции отладки сетки CSS,][DevtoolsCssGrid] теперь доступны и включены по умолчанию в версии Microsoft Edge 89 или более поздней версии.  
    
## <a name="providing-feedback-on-experimental-features"></a>Предоставление отзывов по экспериментальным функциям  

Предоставление отзывов об экспериментах Microsoft Edge DevTools или о чем-либо другом, связанном с DevTools.  

*   Отправка отзывов с помощью **значка Отправка отзывов** в DevTools  
*   Чирикать [в @EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   Значок **Отправка отзывов** в Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверьте сетку CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsMoveTabs]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface Duo | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Используйте эмулятор Surface Duo | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Удаленные клиенты настольных | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy Fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмулировать устройства с двойным экраном и складными устройствами в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
