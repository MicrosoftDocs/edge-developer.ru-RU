---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эксперимент
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: c76830cb8bbcc597aa026f58e1926cd2f9bc2d62
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439586"
---
# <a name="experimental-features"></a>Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся в разработке.  Вы можете протестировать и [предоставить обратную связь](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.  

В то время как экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Включаем экспериментальные функции  

Чтобы включить экспериментальные функции \(или off\) в Microsoft Edge, выполните следующие действия.  

1.  [Откройте DevTools][DevtoolsOpenIndex].  
    *   Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  
1.  Откройте области [Параметры.][DevToolsCustomizeIndexSettings]  
    *   Выберите `Shift` + `?` .  Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]  
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
| [Enable webhint](#enable-webhint) | 85 или более поздней |  
| [Enable Network Console](#enable-network-console) | 85 или более поздней |  
| [Source Order Viewer](#source-order-viewer) | 86 или более поздней |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | 87 или более поздней |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | 89 или более поздней |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | 89 или более поздней |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | 89 или более поздней |  
| [Enable Welcome tab](#enable-welcome-tab) | 89 или более поздней |  

### Enable webhint  

[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.  Тип обратной связи, предоставляемый [веб-сайтом][WebhintMain].  

*   специальные возможности  
*   совместимость между браузерами  
*   безопасность"  
*   производительность  
*   Прогрессивные веб-приложения (PWAs)  
*   другие распространенные проблемы веб-разработки  
    
Эксперимент [webhint][WebhintMain] отображает обратную связь веб-хинта в панели [Issues.][DevtoolsIssuesIndex]  Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем сайте.  Выберите ссылку на ресурс, чтобы открыть **соответствующую**сеть, **источники**или **элементов** в DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   webhint feedback in the **Issues** panel  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

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

### Source Order Viewer  

**Source Order Viewer** это эксперимент, отображает порядок элементов в источнике веб-страницы.  Порядок отображения на экране может отличаться от порядка источника, что сбивает с толку читателя экрана и пользователей клавиатуры.  Используйте эксперимент, чтобы найти различия между порядком отображения на экране и **Source Order Viewer** порядком источника.  

После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Чтобы **Source Order Viewer** использовать, выполните следующие действия.  

1.  Откройте **средство Elements.**  
1.  Откройте панель **доступности** в панели ящика \(bottom\) .  
1.  В разделе выберите почтовый ящик **Source Order Viewer** Show Source **Order.**  
1.  Выделение любого элемента HTML для отображения наложения, указываемой на источник веб-страницы.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox=".. /media/experiments-source-order-viewer.msft.png"::: в **Source Order Viewer** области **доступности**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

Теперь можно визуализировать Слои вместе с индексами z и объектной моделью документа \(DOM\).  Эта функция позволяет отключить, не переключая контексты так часто.  Вы определили, что уменьшение переключения контекста является основной проблемой.  Не всегда понятно, как код, который вы пишете, влияет на ваше веб-приложение.  Для комплексного визуального отладки теперь 3D View объединяются композитные слои и композитные слои.  

После включите эксперимент, убедитесь, что вы перезапустите DevTools.  Чтобы использовать **композитные слои,** выполните следующие действия.  

1.  В ящике выберите **3D View** средство.  
1.  Откройте области **Композитные слои.**  
1.  Отображаются все расписные слои приложения.  Попробуйте эту функцию с помощью собственных веб-приложений.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   Панель **Составные слои**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

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

### Enable new CSS Flexbox debugging features  

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

### Enable + button tab menus to open more tools  

Теперь можно открыть дополнительные средства с помощью нового значка **More Tools** `+` \( \) .  После включив эксперимент и перезагрузив DevTools, знак плюс \( \) отображает справа от группы вкладок в верхней части **Enable + button tab menus to open more tools** `+` DevTools.  Чтобы отобразить список других средств, которые можно добавить в вкладку, выберите значок **More Tools** `+` \( \) .  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Дополнительные средства** в верхней области
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

Этот эксперимент заменяет средство **What's New** новым средством **Welcome.**  Он отображает обновленный дизайн для следующего контента.  

*   Ссылки на документы разработчика  
*   последние функции  
*   заметки о выпуске  
*   Возможность связаться с командой Microsoft Edge DevTools  
    
Средство **Welcome** автоматически открывается после каждого обновления microsoft Edge.  Чтобы предотвратить отображение средства **Welcome** после каждого обновления, закройте почтовый ящик рядом с вкладками **Open** после каждого обновления под заголовком **Welcome** tool.  

Если вы предпочитаете оригинальный **инструмент What's New,** перейдите к [параметрам][DevtoolsCustomizeIndexSettings]  >  **Эксперименты** и удалите контрольный ящик рядом **Enable Welcome tab** с .  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство welcome" lightbox="../media/experiments-welcome.msft.png":::
   **Средство welcome**  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Предыдущие экспериментальные функции  

*   [3D View][Devtools3dViewIndex] теперь доступна и включена по умолчанию в microsoft Edge версии 83 или более поздней версии.  
*   [Turn on support to move tabs between panels][DevtoolsCustomizeIndex] теперь доступна и включена по умолчанию в Microsoft Edge версии 85 или более поздней версии.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] теперь доступна и включена по умолчанию в microsoft Edge версии 86 или более поздней версии.  
*   [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.  
*   [Turn on new CSS grid debugging features][DevtoolsCssGrid] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.  
*   [Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] теперь доступна и включена по умолчанию в microsoft Edge версии 90 или более поздней версии.  

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

[Devtools3dViewIndex]: ../3d-view/index.md "::::no-loc (3D View)::: | Документы Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверьте сетку CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools ":Изменить клавиши клавиш для любого действия в DevTools | Документы Майкрософт"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Сочетания клавиш в DevTools для Microsoft Visual Studio Code | Документы Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsIssuesIndex]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмулировать устройства с двойным экраном и складными устройствами в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
