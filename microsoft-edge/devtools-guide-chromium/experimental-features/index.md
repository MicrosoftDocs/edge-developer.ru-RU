---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: fbdeeb08599285a9cfa6edd467282cfbabbadd74
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235481"
---
# Экспериментальные функции  

Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся на стадии разработки.  Вы можете протестировать и [предоставить отзыв](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.  

Хотя экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.  

## Включить экспериментальные функции  

Чтобы включить экспериментальную функцию \(или off\) в Microsoft Edge, выполните следующие действия.  

1.  [Откройте DevTools.][DevtoolsOpenMain]  
    *   Выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).  Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  
1.  Откройте области ["Параметры".][DevToolsCustomizeSettings]  
    *   Выберите `Shift` + `?` .  Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].  
1.  В левой части **области** "Параметры" выберите раздел **"Эксперименты".**  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="../media/experiments-devtools.msft.png":::
       Список экспериментов в параметрах **** DevTools  
    :::image-end:::  
    
1.  На странице **"Эксперименты"** прокрутите список всех доступных экспериментальных функций и выберите этот элемент рядом с каждой функцией, которую нужно протестировать.  
1.  Закроют и снова откроете Microsoft Edge DevTools.  
    
> [!NOTE]
> Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.  Чтобы отключить экспериментальную функцию, откройте страницу **"Эксперименты"** и скройте контрольный элемент экспериментальной функции, которую нужно отключить.  

## Основные экспериментальные функции  

В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.  

| Экспериментальная функция | Версия Microsoft Edge |  
|:--- |:--- |  
| [Эмуляция: поддержка режима двойного экрана](#emulation-support-dual-screen-mode) | 84 или более поздней |  
| [Включить новые функции отладки сетки CSS](#enable-new-css-grid-debugging-features) | 85 или более поздней |  
| [Поддержка перемещения вкладок между панелями](#enable-support-to-move-tabs-between-panels) | 85 или более поздней |  
| [Включить веб-вехин](#enable-webhint) | 85 или более поздней |  
| [Включить сетевую консоль](#enable-network-console) | 85 или более поздней |  
| [Source Order Viewer](#source-order-viewer) | 86 или более поздней |  
| [Включить редактор сочетания клавиш](#enable-keyboard-shortcut-editor) | 87 или более поздней |  
| [Включить составные слои в 3D-представлении](#turn-on-composited-layers-in-3d-view) | 87 или более поздней |  

### Эмуляция: поддержка режима двойного экрана  

Предоставляет дополнительные функции для эмуалации двух новых двух- и папок устройств в Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Папка "Сумяно"][SamsungMobileGalaxyFold]  
    
Эмулируете устройства и перенимаете следующие положения.  

*   Одноэкранное или сложенное положение  
*   Двухэкранное или развернутое положение  
    
[](#enable-experimental-apis) Включить экспериментальные API веб-платформы и использовать функцию расширения экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для улучшения веб-сайта \(или app\) для двухэкранных и папок устройств.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Эмуляция Surface Duo в Microsoft Edge  
:::image-end:::  

#### Включить экспериментальные API  

Чтобы использовать функцию прокрутки экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments,][DualScreenDocsJSAPI]включите флаг `Experimental Web Platform features` в Microsoft Edge.  Выполните следующие действия.  

1.  Перейдите к `edge://flags` .  
1.  In the **Search flags** textbox, `Experimental Web Platform features` enter, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.  
1.  Перезапустите Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Включить флаг экспериментальной веб-платформы" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Включить флаг экспериментальной веб-платформы  
:::image-end:::  

> [!NOTE]
> Если вы используете запросы мультимедиа [CSS][DualScreenDocsCssMedia] или [API нумерации][DualScreenDocsJSAPI] сегментов JavaScript для улучшения веб-сайта **** или приложения [для Surface Duo,][SurfaceDevicesDuo]необходимо также включить флаг экспериментальной веб-платформы в приложении Microsoft Edge для [Android][GooglePlayMicrosoftEdge] на устройстве Surface [Duo.][SurfaceDevicesDuo]  
> 
> Если **** флаг экспериментальной веб-платформы включен в [microsoft Edge][MicrosoftEdge] на настольном компьютере и отключен в приложении Microsoft Edge для [Android,][GooglePlayMicrosoftEdge]поведение вашего веб-сайта или приложения в эмуляторе Surface Duo на настольном компьютере Microsoft Edge не совпадает с приложением [Microsoft Edge для Android][GooglePlayMicrosoftEdge] на Surface [Duo.][SurfaceDevicesDuo]  Убедитесь, что флаги совпадают в Android и на настольном компьютере Microsoft Edge, чтобы успешно использовать эмулятор Surface Duo в настольном [Microsoft Edge.][MicrosoftEdge]  

#### Тестирование на устройствах с двумя экранами и папок  

Когда вы эмулируете [Surface Duo][SurfaceDevicesDuo] в режиме двойного экрана в Microsoft Edge, на вашем веб-сайте или в приложении прорисовка пространства между двумя экранами.  

Эмулированный дисплей соответствует способу отображения вашего веб-сайта (или приложения\) в приложении [Microsoft Edge для Android,][GooglePlayMicrosoftEdge] запущенном на [Surface Duo.][SurfaceDevicesDuo]  Возможно, вам придется обновить свой веб-сайт \(или приложение\), чтобы лучше отображаться на этом пути.  Дополнительные сведения об адаптации веб-сайта \(или приложения\) [][DualScreenIntroductionHowWorkSeam]к скайму см. в подмыве.  

Панель [инструментов устройства содержит][DevtoolsDeviceModeIndexSimulateMobileViewport] дополнительные функции, которые помогут вам протестировать веб-сайт или приложение в различных положениях и ориентациях.  Choose **Rotate** \( ![ Rotate ][ImageRotateIcon] \) to rotate the viewport to landscape orientation. Объединяйте эту функцию с **Span** \( Span \) для перекладки между одноэкранным экраном или сдвойте экран или ![ ][ImageSpanIcon] развернутые положения.  Вместе эти функции позволяют тестировать веб-сайт или приложение во всех четырех возможных положениях и ориентациях.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица положения и ориентации для двухэкранных и папок устройств" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Матрица положения и ориентации для двухэкранных и папок устройств  
:::image-end:::  

Значок **экспериментальной** веб-платформы \( ExperimentalApis \) отображает состояние флага экспериментальной ![ ][ImageExperimentalApisIcon] **веб-платформы.**  Если флаг включен, значок выделяется.  Если флаг отключен, значок не выделяется.  Чтобы включить \(или отключить\) флаг, перейдите к флагу и `edge://flags` переключите его.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Вот дополнительные ресурсы, которые могут помочь вам улучшить веб-сайт \(или приложение\) для двухэкранных устройств.  

*   Дополнительные сведения о веб-разработке на двухэкранных устройствах можно найти в двухэкранных [веб-приложениях.][DualScreenWebIndex]  
*   Установите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]  Он отличается от эмулятора в Microsoft Edge, эмулирует Surface Duo под управлением Android и интегрируется с [Android Studio.][AndroidDeveloperStudio]  Для получения дополнительных сведений перейдите к [get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].  
    
> [!NOTE]
> Ниже приводится список текущих известных проблем.  
> 
> *   При использовании клиента [удаленного][RemoteDesktopClientDocs] рабочего стола Майкрософт для подключения к удаленному КОМПЬЮТЕРу и эмуалации [папки Surface Duo][SurfaceDevicesDuo] или [Windows 2013][SamsungMobileGalaxyFold]указатель может встряхнуться или перебор.  Если у вас проблема, отправьте [отзыв.](#providing-feedback-on-experimental-features)  

### Включить новые функции отладки сетки CSS  

Эта экспериментальная функция предоставляет ряд новых визуализаций для отлаки макетов сетки CSS.  Чтобы просмотреть последние экспериментальные функции, в [этом эксперименте необходимо](#turn-on-experimental-features) включить и перезагрузить DevTools.  Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.  

#### Просмотр наложения сетки при наведении с помощью средства inspect  

Средство **Inspect** позволяет быстро определять и визуализировать макеты сетки CSS на веб-сайте, наведении на них указателя мыши.  Choose the **Inspect** \( ![ Inspect ][ImageInspectIcon] \) icon in the top-left corner of DevTools.  Затем наведите курсор на элемент Grid на веб-сайте, который вы отладили.  Контуры отображаются вокруг сетки, а затенение указывает расположение разрывов сетки, если они присутствуют.  

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

Обычно такие средства, **** как **** элементы и сеть, могут открываться только на главной панели, расположенной в верхней части DevTools.  Такие **средства, как трехмерный** просмотр и проблемы, которые обычно открываются только на панели "Drawer", расположенной в нижней части DevTools. **** ****  После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.  Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить** в верхнюю" или "Переместить **в нижнюю часть".**   Этот эксперимент позволяет настроить макет DevTools.  Чтобы показать или скрыть панель **"Drawer",** выберите `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   Перемещение вкладок между панелями  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить веб-вехин  

[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.  Тип отзыва, предоставляемого [веб-хиной.][WebhintMain]  

*   специальные возможности  
*   совместимость между браузерами  
*   безопасность"  
*   производительность  
*   Progressive Web Apps (PWAs)  
*   другие распространенные проблемы веб-разработки  
    
В [эксперименте webhint][WebhintMain] на панели "Проблемы" отображается обратная связь [веб-хинта.][DevtoolsIssues]  Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем веб-сайте.  Выберите ссылку на ресурс, чтобы открыть **** соответствующую **области** **"Сеть",**"Источники" или "Элементы" в DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="обратная связь веб-панелей на панели "Проблемы"" lightbox="../media/experiments-webhint.msft.png":::
   обратная связь веб-панелей на **панели "Проблемы"**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Включить сетевую консоль  

**Сетовая** консоль — это рабочий заголовок эксперимента по запросам искусственных сетей по протоколу HTTP.  Вы можете использовать эксперимент **с сетевой** консолью для отправки запросов веб-API.  

После включения эксперимента убедитесь, что перезапустите DevTools.  Чтобы использовать **сетевую консоль,** выполните следующие действия.  

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

**"Просмотр порядка источника"** — это эксперимент, который отображает порядок элементов в источнике страницы.  Порядок отображения на экране может отличаться от порядка источника, что приводит к путанице для чтения с экрана и пользователей клавиатуры.  Используйте эксперимент **"Просмотр порядка источника",** чтобы найти различия между порядком отображения на экране и порядком источника.  

После включения эксперимента убедитесь, что перезапустите DevTools.  Чтобы использовать **"Просмотр порядка источника",** выполните следующие действия.  

1.  Откройте области **элементов.**  
1.  Откройте панель **"Accessibility"** (Доступность) на панели "Drawer \(bottom\)".  
1.  В разделе **"Просмотр порядка источника"** выберите **"Показать** порядок источника".  
1.  Выделяем любой htmL-элемент, чтобы отобразить наложение, которое является порядком в источнике страницы.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Source Order Viewer** in the **Accessibility** pane  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Включить редактор сочетания клавиш

После того **как включен** эксперимент "Включить редактор сочетания клавиш", вы можете настраивать сочетания клавиш для любого действия в DevTools.  Чтобы настроить сочетания клавиш для определенного действия, выполните следующие действия.  

1.  [Откройте DevTools.][DevtoolsOpenMain]  
1.  Откройте ["Параметры".][DevToolsCustomizeSettings]
    *   Выберите `Shift` + `?` .  
1.  Перейдите на **страницу ярлыков.**  
1.  Выберите действие, настраиваемую.  
1.  Choose the **Edit** \( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \) icon.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выбор действия для настройки на странице "Ярлыки" в параметрах" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Выбор действия для настройки на странице **"Ярлыки"** в [параметрах][DevToolsCustomizeSettings]
    :::image-end:::  
    
1.  На клавиатуре выберите ключи, которые нужно привязать к действию.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выбор ключей, которые нужно назначить действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Выбор ключей, которые нужно назначить действию
    :::image-end:::  
    
1.  Чтобы сохранить новый ярлык клавиатуры, выберите контрольный знак \(![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]\) значок.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Choose the checkmark icon to save your new keyboard shortcut" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Choose the checkmark icon to save your new keyboard shortcut
    :::image-end:::  
    
1.  Выберите новый ярлык клавиатуры для запуска действия в DevTools.  
    
На странице **"Ярлыки"** значок настраиваемой клавиатуры **\(** ![ CustomKeyboardShortcut \) отображает настроенные сочетания ][ImageCustomKeyboardShortcutIcon] клавиш.  Чтобы сбросить все ярлыки, выберите **"Восстановить ярлыки по умолчанию".**  

При редактировании сочетания клавиш для действия, чтобы отменить изменения, выберите значок X \( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).  Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).  Чтобы добавить несколько ярлыков для действия, выберите **"Добавить ярлык".**

> [!NOTE]
> Если ярлык клавиатуры в настоящее время назначен другому действию, вы не сможете сохранить его для нового действия.  Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.  

<!--Available in Microsoft Edge version 87 and later.  -->

### Включить составные слои в 3D-представлении

Теперь можно визуализировать слои вместе с z-индексами и объектной моделью документа \(DOM\).  Эта функция помогает отлакить без переключения контекстов так часто.  Вы определили, что уменьшение переключения контекста является серьезной проблемой.  Не всегда понятно, как код, который вы пишете, влияет на веб-приложение.  Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.  После включения эксперимента убедитесь, что перезапустите DevTools.  Чтобы использовать **составные слои,** выполните следующие действия.  

1.  В средстве **"3D View"** выберите в этом оке средство.  
1.  Откройте области **составных** слоев.  
1.  Отображаются все закрашенные слои приложения.  Попробуйте эту функцию с собственными веб-приложениями.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   Панель **Составные слои**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## Предыдущие экспериментальные функции  

*   [3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.  
*   [Настройка сочетания клавиш теперь][DevtoolsCustomKeyboardShortcuts] доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.  

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

<!-- image links -->  

[ImageCheckmarkKeyboardShortcutIcon]: ../media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ../media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ../media/delete-keyboard-shortcut-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ../media/edit-keyboard-shortcut-icon.msft.png  
[ImageExperimentalApisIcon]: ../media/experimental-apis-dark-icon.msft.png  
[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ../media/span-dark-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ../media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevToolsCustomizeSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств в режиме устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools сочетания клавиш | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для обнаружения двухэкранного | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Папка | Сума"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
