---
description: Используйте DevTools в режиме высокой контрастности Windows, уравнося клавишами клавиш в DevTools, чтобы Visual Studio код и другие.
title: Новые возможности в DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3264292721d5e4385b0e6d256d042c76182c21c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408327"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Новые возможности в DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.  Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.  Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Использование DevTools в режиме высокой контрастности Windows

Теперь Microsoft Edge DevTools отображаются в режиме высокой контрастности, когда Windows находится в режиме высокой контрастности.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools в режиме высокой контрастности  
:::image-end:::  

[Следуйте инструкциям, чтобы включить режим высокой контрастности в Windows][MicrosoftSupportWindows10HighContrastMode].  Чтобы открыть DevTools в Microsoft Edge, выберите `F12` или `Ctrl` + `Shift` + `I` .  DevTools отображаются в режиме высокой контрастности.  

> [!NOTE]
> Microsoft Edge DevTools в настоящее время поддерживает режим высокой контрастности на Windows, но не на macOS.  

Проблема Chromium [#1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Совпадение клавиш в DevTools для Visual Studio кода  

Из [отзывов](#getting-in-touch-with-microsoft-edge-devtools-team) и отслеживания общедоступных проблем [Chromium][CRIssuesList]команда Microsoft Edge DevTools узнала, что вы хотите настроить ярлыки клавиатуры в DevTools.  В Microsoft Edge 84 теперь можно соотносят клавиши в DevTools с [кодом Visual Studio,][VisualStudioCode]который является лишь одной из функций, над которыми команда работает для настройки ярлыков.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Совпадение клавиш в DevTools для Visual Studio кода" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools в режиме высокой контрастности  
:::image-end:::  

Чтобы попробовать эксперимент, откройте Параметры DevTools, выбрав или выбрав значок Параметры DevTools в правом верхнем углу `?` ![ ][ImageSettingsIcon] DevTools.  Перейдите в раздел **Эксперименты** и проверьте вкладку Включить настраиваемые параметры ярлыков **клавиатуры (требуется перезагрузка).**  Теперь перезагрузить DevTools, открыть параметры снова и перейти к **разделу Ярлыки.**  

Выберите **DevTools (По умолчанию)** в ярлыках **Match** из предустановленного отсева и **выберите код Visual Studio.**  Ярлыки клавиатуры в DevTools теперь соответствуют ярлыкам для эквивалентных действий в Visual Studio Code.  

Например, ярлык клавиатуры для прио паузы или продолжения работы скрипта в [Visual Studio коде][VisualStudioCodeShortcuts] `F5` .  С предустановленной программой **DevTools (По умолчанию)** этот же ярлык в DevTools есть, но с заранее задаваемой программой Visual Studio, этот ярлык теперь `F8` также **** `F5` .  

В настоящее время эта функция доступна в Microsoft Edge 84 в качестве эксперимента, поэтому поделитесь своими [отзывами](#getting-in-touch-with-microsoft-edge-devtools-team) с командой!  

Проблема Chromium [#174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Эмуляторы Surface Duo удаленного отладки  

Теперь вы можете удаленно отладить веб-контент, работающий в эмуляторе [Surface Duo,][DualScreensAndroidEmulator] используя полную мощность [Microsoft Edge DevTools][DevToolsChromiumGuide].  

С помощью [эмулятора Surface Duo][DualScreensAndroidEmulator]вы сможете проверить, как отрисовка веб-контента на новом классе складных и двухэкранных устройств.  Эмулятор запускает операционную систему Android и предоставляет [приложение Microsoft Edge Android.][AndroidEdge]  Загрузите веб-содержимое в [приложение Microsoft Edge и][AndroidEdge] отладите его с помощью Microsoft Edge [DevTools.][DevToolsChromiumGuide]  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Приложение Microsoft Edge, запущенное в эмуляторе Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   Приложение Microsoft Edge в эмуляторе Surface Duo  
:::image-end:::  

На странице в настольном экземпляре Microsoft Edge показан `edge://inspect` **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs,][PwaIndex] которые работают на эмуляторе [Surface Duo.][DualScreensAndroidEmulator] [][DesktopEdge]  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, которое работает на эмуляторе" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   На странице отображается список открытых вкладок в `edge://inspect` приложении Microsoft Edge, которое работает на эмуляторе
:::image-end:::  

Выберите **для** проверки вкладку или PWA, которую необходимо отладить, чтобы открыть [Microsoft Edge DevTools.][DevToolsChromiumGuide]  [Следуйте пошаговому][DevToolsRemoteDebugDuoEmulator]руководству по удаленной отладки веб-контента в эмуляторе Surface Duo.  

### <a name="resize-the-devtools-drawer-more-easily"></a>Более простое решение по окантовке ящика DevTools  

В Microsoft Edge 83 или ранее можно было только повторно использовать [ящик DevTools,][DevToolsDrawer] зависая в панели инструментов ящика.  Ящик вел себя по-другому, чем другие элементы управления, меняя их для стекол в DevTools, где вы наведите курсор на границе области, чтобы повторно ее использовать.  Выберите следующее изображение, чтобы отобразить, как работал ящик в версии 83 или более ранней версии Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Размер ящика DevTools в Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Размер ящика DevTools в Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Начиная с Microsoft Edge 84, теперь вы можете повторно использовать ящик, зависая над границей ящика.  Это изменение выравнивает поведение, меняющее размер ящика DevTools, с способом изменения размеров других стекол в DevTools.  Выберите следующее изображение для отображения размеров в действии в Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Размер ящика DevTools в Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Размер ящика DevTools в Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Проблема Chromium [#1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Экранизация навигационных кнопок отображения фокуса  

При удаленном отладке android-устройства, устройства [Windows 10][DevToolsRemoteDebugWindows]или эмулятора [Surface Duo][DevToolsRemoteDebugDuoEmulator]можно отладить скринкастинг с помощью значка Toggle Screencast в левом верхнем углу [][DevToolsRemoteDebugAndroid] ![ ][ImageScreencastingIcon] DevTools.  Благодаря включенной экранной трансляции вы можете перемещать вкладку в Microsoft Edge на удаленном устройстве из окна DevTools.  В Microsoft Edge 84 эти кнопки навигации теперь также доступны для клавиатуры.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Выберите Shift+Tab из экранируемой панели URL-адресов с фокусом на кнопке Обновление" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Выберите `Shift` + `Tab` из экранируемой панели URL-адресов фокус на кнопке **Обновление**
:::image-end:::  

Проблема Chromium [#1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Теперь доступна панель сведений о панели сети  

В Microsoft Edge 84 поле [Details][DevToolsNetworkDetails] в средстве **Network** теперь фокусируется при его открываемом ресурсе в [сетевом журнале.][DevToolsNetworkLog]  Это изменение позволяет читателям экрана читать и взаимодействовать с содержимым области **Details.**  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Панель Details в панели Network фокусируется при открываемом" lightbox="../../media/2020/05/network-details.msft.png":::
   Области **подробностей** в **средстве Network** фокусируется при открываемом
:::image-end:::  

Проблема Chromium [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 84, которые были внесены в проект Chromium с открытым исходным кодом.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Устранение проблем с сайтом с помощью нового средства "Проблемы" в ящике DevTools

Новый инструмент **Issues** в ящике DevTools был создан, чтобы уменьшить усталость уведомлений и захламление **консоли.**  В **настоящее** время консоль является центральным местом для разработчиков веб-сайтов, библиотек, рамок и Microsoft Edge для журналов сообщений, предупреждений и ошибок.  Средство **Issues** собирает предупреждения из браузера структурированным, агрегируемым и действий способом ссылок на затронутые ресурсы в Microsoft Edge DevTools и предоставляет рекомендации по устранению проблем.  Со временем все больше и больше предупреждений **** в Microsoft Edge в инструменте Проблемы, а не консоли **,** которые должны помочь уменьшить беспорядок в **консоли**.  

Чтобы начать работу, перейдите к поиску и устранению проблем с помощью средства [Microsoft Edge DevTools Issues.][DevtoolsIssuesIndex]  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Средство Проблемы в ящике DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   Средство **Проблемы** в ящике DevTools  
:::image-end:::  

Проблема Chromium [#1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Просмотр сведений о доступности в инструменте Inspect Mode  

В **инструменте Inspect Mode** теперь указывается, имеет [][WebhintHintsAxeNameRoleValue] ли элемент доступное имя и роль и является ли он [фокусируемым на клавиатуре.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Средство Inspect Mode с сведениями о доступности" lightbox="../../media/2020/05/a11y.msft.png":::
  Средство **Inspect Mode** с сведениями о доступности  
:::image-end:::  

Проблема Chromium [#1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Обновления панели производительности  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Просмотр сведений о времени блокировки в подножке  

После записи производительности нагрузки панель **Performance** теперь отображает сведения об общем времени блокировки \(TBT\) в подножке.  TBT — это показатель производительности нагрузки, который позволяет количественно определить, сколько времени занимает страница, чтобы стать полезной.  В нем по существу измеряется, как долго страница может быть использовать \(так как содержимое отображается на экране\); но на самом деле не может быть удобным, так как JavaScript блокирует основной поток и поэтому страница не реагирует на ввод пользователя.  TBT является основным показателем для приближения первой задержки ввода.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Чтобы получить сведения о времени блокировки, не используйте **значок** обновления страницы обновления страницы для записи производительности ![ ][ImageRefreshPageIcon] загрузки страницы.  

Вместо этого выберите **значок Запись** записи, вручную перезагрузите страницу, подождите загрузку страницы ![ и ][ImageRecordIcon] прекратите запись.  

Если отображается, Microsoft Edge DevTools не получают необходимые сведения из внутренних данных `Total Blocking Time: Unavailable` профилирование в Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Общая информация о времени блокировки в подножке записи панели Performance" lightbox="../../media/2020/05/tbt.msft.png":::
   Общая информация о времени блокировки в подножке записи панели **Performance**  
:::image-end:::  

Проблема Chromium [#1054381][CR1054381]  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>События переноса макета в новом разделе Experience  

Новый раздел **Experience** панели **Performance** помогает обнаруживать сдвиги макета.  Накопительная смена макета \(CLS\) — это метрика, которая помогает количественно оценить нежелательную визуальную нестабильность.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Выберите событие **Перенос макета,** чтобы отобразить сведения о переносе макета в области **Сводка.**  Наведите курсор на **перемещении** и **перемещении** в поля, чтобы визуализировать место, где произошла смена макета.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Сведения о переносе макета" lightbox="../../media/2020/05/cls.msft.png":::
   Сведения о переносе макета  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Более точная терминология обещаний в консоли  

При входе в журнал консоли неправильно `Promise` при условии **** `PromiseStatus` значения, установленного `resolved` для .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Пример консоли с использованием старой разрешенной терминологии" lightbox="../../media/2020/05/resolved.msft.png":::
   Пример консоли **с использованием** старой `resolved` терминологии  
:::image-end:::  

Консоль **теперь** использует термин `fulfilled` , который соответствует `Promise` спецификации.  Дополнительные сведения о `Promise` спецификации перейдите в [Штаты и судьбы на GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Пример консоли с использованием новой терминологии" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Пример консоли **с** использованием новой `fulfilled` терминологии  
:::image-end:::  

Выпуск V8 [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Обновления области стилей  

#### <a name="support-for-the-revert-keyword"></a>Поддержка ключевого слова revert  

Пользовательский интерфейс автокомплекта области **Стилей** обнаруживает ключевое слово [][MDNRevert] CSS, которое возвращает каскадное значение свойства к предыдущему значению, примененному к стилю элемента.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Настройка значения свойства для повторного" lightbox="../../media/2020/05/revert.msft.png":::
  Настройка значения свойства для повторного  
:::image-end:::  

Проблема Chromium [#1075437][CR1075437]  

#### <a name="image-previews"></a>Предварительные просмотры изображений  

Наведите курсор на значение в области Стилей, чтобы отобразить предварительный просмотр изображения `background-image` в панели инструментов. ****  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Наведении на фоновое значение изображения" lightbox="../../media/2020/05/image-preview.msft.png":::
  Наведении над `background-image` значением  
:::image-end:::  

Проблема Chromium [#1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>В color Picker теперь используется функциональная нотация с раздельным пространством  

[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] указывает, что цветовые функции, например, должны поддерживать аргументы, разделенные `rgb()` пространством.  Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.  

Когда вы выбираете [][DevtoolsCssReferenceColorPicker] цвета с помощью выбора цвета или чередуется между представлениями цветов в области **Стилей,** удерживая и выбирая значение, отображается синтаксис аргументов, разделенных `Shift` `background-color` пробелами.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Использование аргументов, разделенных пространством, в области Стилей" lightbox="../../media/2020/05/color.msft.png":::
  Использование аргументов, разделенных пространством, в области **Стилей**  
:::image-end:::  

Кроме того, необходимо отобразить синтаксис в **области Computed** и **инструментарий Режима** проверки.  

Microsoft Edge DevTools использует новый синтаксис, так как предстоящие функции CSS, такие как [color()][CSSWGDraftsColor4Property] не поддерживают синтаксис аргументов, разделенных запятой.  

Синтаксис аргументов, разделенных пробелами, некоторое время поддерживался в большинстве браузеров.  Дополнительные сведения можно найти в [раздел "Можно ли использовать: функциональные нотации, разделенные пробелами"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Проблема Chromium [#1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Обесценение области свойств в панели Elements  

Области **свойств** в **инструменте Elements** отстает.  Вместо `console.dir($0)` этого **запустите в консоли.**  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Неуловимая панорама свойств" lightbox="../../media/2020/05/properties.msft.png":::
   Неуловимая **панорама свойств**  
:::image-end:::  

#### <a name="references"></a>Ссылки  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Поддержка ярлыков приложений в области Манифест  

Ярлыки приложений помогают пользователям быстро приступить к общим или рекомендуемым задачам в веб-приложении.  Меню ярлыков приложения отображается только [][PwaIndex] для прогрессивных веб-приложений, установленных на рабочем столе или мобильном устройстве пользователя.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Ярлыки приложения в области Манифест" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Ярлыки приложения в **области Манифест**  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Контакт с командой Microsoft Edge Devtools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Используйте эмулятор Surface Duo | Документы Майкрософт"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — справочные | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript — справочные ссылки на API консоли | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Измените цвета с помощью выборки цвета — CSS Reference | Документы Майкрософт"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка | Документы Майкрософт"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладками Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленной отладки android-устройств | Документы Майкрософт"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с эмуляторами Surface Duo удаленного отладки | Документы Майкрософт"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладки устройств Windows 10 | Документы Майкрософт"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверка сведений о | Документы Майкрософт"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Журнал сетевой активности | Документы Майкрософт"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android app"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Разделенные пространством функциональные цветовые нотации — MDN | Могу ли я использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: легко просматривать изображения и фоновые изображения в области стилей | Ошибки Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: показать основные сведения a11y в элементе popover | Ошибки Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского интерфейса DevTools для режима высокой контрастности | Ошибки Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель проблем корабля | Ошибки Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: выбор цвета должен производить современный синтаксис цвета CSS | Ошибки Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавьте поддержку ключевого слова/значения CSS для | Ошибки Chromium"  
[CR1076112]: https://crbug.com/1076112 "Персонализация Devtools — resizer ящика"  
[CR1081486]: https://crbug.com/1081486 "Фокус клавиатуры не виден для кнопок навигации в режиме screencast | Ошибки Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть "выполнен", а не "разрешен" | Ошибки V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения из цветов 3 — CSS Color Module Level 4 | Проекты редактора рабочей группы W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Цвет переднего плана: "цвет" - CSS Color Module Level 4 | Проекты редактора рабочей группы W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Представление нового microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Состояния и судьбы — domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "повторное | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость браузера | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Код"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio клавиши кода для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: клавиатура | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Значение роли имени | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включить или отключить режим высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/updates/2020/05/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
