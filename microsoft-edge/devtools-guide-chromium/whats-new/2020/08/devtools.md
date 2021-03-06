---
description: Сопоположите клавиши Visual Studio код, эмулировать Surface Duo и Samsung Galaxy Fold, улучшения наложения сетки CSS и другие.
title: Новые возможности в DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3853f097877fc45b14ceb0674309cb35b58a0aa6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398618"
---
# <a name="whats-new-in-devtools-microsoft-edge-86"></a>Что нового в DevTools (Microsoft Edge 86)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a>Совпадение клавиш в DevTools с Visual Studio кодом  

В Microsoft Edge 86 клавиши в DevTools могут совпадать с ярлыками в [Microsoft Visual Studio Code.][VisualStudioCode]  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Совпадение клавиш в DevTools для Visual Studio кода" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Совпадение клавиш в DevTools для Visual Studio кода  
:::image-end:::  

Чтобы активировать эту функцию, перейдите к настройке ярлыков клавиатуры [в Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Например, ярлык клавиатуры для прио паузы или продолжения работы скрипта в [Visual Studio коде][VisualStudioCodeShortcutsKeyboardWindows] `F5` .  С предустановленной программой **DevTools (По умолчанию)** этот же ярлык в DevTools есть, но при выборе предустановки кода Visual Studio этот ярлык теперь также `F8` является **** `F5` .  

Проблема Chromium [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Эмулировать Surface Duo и Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете проверить внешний вид веб-сайта или приложения на двух новых устройствах:  [Surface Duo][MicrosoftSurfaceDevicesDuo] и [Samsung Galaxy Fold][SamsungMobileGalaxyFold] в Microsoft Edge.  

Чтобы улучшить веб-сайт или приложение для двухэкранных и складных устройств, используйте следующие функции при [эмулации устройства.][DevtoolsDeviceModeIndex]  

*   [Spanning][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]— это когда веб-сайт \(или app\) отображается на обоих экранах.
*   [Отрисовка шва,][DualScreenIntroductionHowWorkSeam]который является пространством между двумя экранами.
*   [Включение экспериментальных API][DevtoolsExperimentalFeaturesEnableExperimentalApis] веб-платформы для доступа к новой функции экранирования экрана [CSS][DualScreenWebCssMediaSpanning] и [API JavaScript getWindowSegments][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Эмуляция устройств для Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Эмуляция устройств для Surface Duo  
:::image-end:::  

Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, перейдите к экспериментальным функциям и выберите контрольный ящик рядом с **режимом Emulation: Support dual screen mode.**  

Дополнительные сведения об этом эксперименте см. в ["Эмуляция: поддержка режима двойного экрана".][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]  

Проблема Chromium: [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Улучшения наложения сетки CSS и новые функции экспериментальной сетки  

Благодарим вас за положительные отзывы об улучшенных наложениях сетки CSS.  Наложения сетки CSS теперь включены по умолчанию и не требуют включения эксперимента.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Наложение сетки CSS для элемента статьи" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Наложение сетки CSS для `article` элемента  
:::image-end:::  

> [!NOTE]
> Дополнительные сведения о наложениях сетки перейдите к [функциям отладки сетки CSS.][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]  

Команда Microsoft Edge DevTools и команда Chrome DevTools совместно работают над дополнительными функциями.  Новые функции включают несколько накладок, которые являются настойчивыми и настраиваемыми из новой области **Макет** на **инструменте Elements.**  

Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, включите экспериментальные функции и выберите контрольный ящик рядом с включить новые функции отладки **CSS Grid (параметры**конфигурации, доступные в панели макета в Elements после перезагрузки).  

Дополнительные сведения об этом эксперименте можно найти в поле Включить новые функции отладки сетки [CSS.][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]  

Проблема Chromium: [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>Таблица, скопированная из консоли, сохраняет форматирование  

В Microsoft Edge 85 или более ранний формат копирования `console.table` был потерян.  Если вы скопировали [][DevtoolsConsoleApiTable] выход из API консоли таблицы и вклеили его, сохранился только текст таблицы.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Выход API консоли таблицы в Microsoft Edge 85 или более ранний" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Выход API консоли в Microsoft Edge 85 или более ранний  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Выход API консоли таблицы из Microsoft Edge 85 или более ранней вставки в Visual Studio Код" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Выход API консоли из Microsoft Edge 85 или более ранней вставки в Visual Studio Код  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

В Microsoft Edge 86 или позже при **** копировании таблицы из консоли форматирование теперь сохраняется.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Выход API консоли таблицы в Microsoft Edge 86 или более поздней" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Выход API консоли в Microsoft Edge 86 или более поздней  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Выход API консоли таблицы из Microsoft Edge 86 или более поздней вставки в Visual Studio Код" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Выход API консоли из Microsoft Edge 86 или более поздней Visual Studio код  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Проблема Chromium: [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Source Order Viewer for easier accessibility testing  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Новый помощник по доступности отображает порядок элементов в источнике.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Активация порядка источника Show" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Активация **порядка источника Show**  
:::image-end:::  

Эта функция упрощает проверку работы чтения с экрана и пользователей клавиатуры на веб-сайте или приложении.  Считыватели экрана и навигация по клавиатуре зависят от контента, размещаемого в определенном порядке в исходный код веб-сайта или приложения, чтобы он совпадал с отрисовывать страницу.  Потенциальные различия в порядке между отрисовываемой страницей и исходным кодом отображаются в представлении источника.  

Чтобы включить эту экспериментальную [][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функцию, перейдите к включив экспериментальные функции и выберите почтовый ящик рядом с **функцией Включить просмотр источника порядка**.  

Дополнительные сведения об этом эксперименте перейдите к [включить viewer source order][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Проблема Chromium: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a>Выделение всех результатов поиска в инструменте Elements  

В Microsoft Edge 84 и 85 первый результат поиска в **инструменте Elements** не был выделен.  Остальные результаты поиска были выделены правильно.  

Благодарим вас за отправку отзывов и помощь в улучшении Chromium.  Ваши отзывы обнаружили [#1103316][CR1103316] в проекте Chromium с открытым исходным кодом.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Выделен первый результат поиска на панели Elements в Microsoft Edge 84 или более поздней" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Выделение первого результата поиска в **средстве Elements** в Microsoft Edge 84 или более поздней  
:::image-end:::  

Проблема устранена во всех версиях Microsoft Edge.  

Проблема Chromium: [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Новый инструмент Мультимедиа  

DevTools теперь отображает сведения о медиаплеерах в [средстве Мультимедиа.][DevtoolsMediaPanelIndex]  

Чтобы открыть новый **инструмент Media,** выполните следующий шаг.  

1.  Выберите **Настройка и управление DevTools** \( `...` \) > **средства**  >  **мультимедиа**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Новый инструмент Мультимедиа" lightbox="../../media/2020/08/media-panel.msft.png":::
       Новый **инструмент Мультимедиа**  
    :::image-end:::  

До создания нового **средства мультимедиа** в DevTools сведения о видеоигрегах и отладке журнала и отладки находились в параметре **Последние игроки.**  Чтобы открыть **параметр "Последние игроки",** перейдите к `edge://media-internals` инструменту **Players** и выберите его.  

Просмотр контента в прямом эфире и более быстрая проверка потенциальных проблем, включая следующие примеры.  

*   Почему кадры отброшены?  
*   Почему JavaScript взаимодействует с игроком неожиданным образом?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Захват снимков экрана узла с помощью контекстного меню инструмента Elements  

Теперь можно запечатлеть скриншоты узлов с помощью контекстного меню в **инструменте Elements.**  

Например, чтобы сделать снимок экрана таблицы содержимого, наведите курсор на элемент, откройте контекстное меню \(правой кнопкой мыши\) и выберите снимок экрана узла **Capture**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Захват скриншотов узлов" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Захват скриншотов узлов  
:::image-end:::  

Проблема Chromium: [#1100253][CR1100253]  

### <a name="issues-tool-updates"></a>Выпуск обновлений инструмента  

Панель предупреждений о проблемах в **консоли теперь** заменяется обычным сообщением.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Проблемы в сообщении консоли" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Проблемы в сообщении консоли  
:::image-end:::  

Сторонние проблемы с cookie теперь скрыты по умолчанию в средстве **Issues.**  Включите новый **почтовый** ящик Включить сторонние вопросы cookie для просмотра проблем.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="почтовый ящик сторонних файлов cookie" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   почтовый ящик сторонних файлов cookie  
:::image-end:::  

Проблемы с хромом: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### <a name="emulate-missing-local-fonts"></a>Эмулировать отсутствующие локальные шрифты  

Откройте средство [визуализации и][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] используйте новую функцию **отключения** локальных шрифтов для эмуляции `local()` отсутствующих источников в `@font-face` правилах.  

Например, когда шрифт установлен на вашем устройстве и правило использует его в качестве шрифта, Microsoft Edge использует локальный файл шрифта `Rubik` `@font-face src` с `local()` устройства.  

Когда **отключение локальных шрифтов** включено, DevTools игнорирует шрифты и извлекает каждый `local()` из сети.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Эмулировать отсутствующие локальные шрифты" lightbox="../../media/2020/08/disable-font.msft.png":::
   Эмулировать отсутствующие локальные шрифты  
:::image-end:::  

При использовании двух разных копий одного шрифта во время разработки, например в следующих примерах.  

*   Локальный шрифт для средств разработки.  
*   Веб-шрифт для кода.  

Чтобы **** упростить выполнение следующих задач, используйте отключение локальных шрифтов.  

*   Отлажение и измерение производительности загрузки и оптимизации веб-шрифтов.  
*   Проверка точности правил `@font-face` CSS.  
*   Узнайте о различиях между локальными версиями, установленными на устройстве, и веб-шрифтом.  

Проблема Chromium: [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Эмулировать неактивных пользователей  

API [обнаружения idle][WebDevIdleDetection] позволяет разработчикам обнаруживать неактивных пользователей и реагировать на изменения состояния ожидания.  Теперь вы можете использовать DevTools для подражания неработающим изменениям состояния в средстве **Датчики** как для состояния пользователя, так и для состояния экрана, а не для ожидания изменения фактического состояния простоя.  Вы можете открыть средство **Датчики** из [ящика][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Эмулировать неактивных пользователей" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Эмулировать неактивных пользователей  
:::image-end:::  

Проблема Chromium: [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Emulate prefers-reduced-data  

> [!NOTE]
> В Microsoft Edge 86, чтобы включить эту функцию, перейдите и включив флаг функций `edge://flags#enable-experimental-web-platform-features` **экспериментальной веб-платформы.**  Параметр эмуляции отображается только в том случае, если включен флаг.  

Запрос [мультимедиа с пониженным][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] объемом данных определяет предпочтения пользователя в контенте для уменьшенных данных.  Если выбрано, пользователь получает альтернативное содержимое страницы, которое использует меньше данных.  

Теперь можно использовать DevTools для эмулации `prefers-reduced-data` запроса мультимедиа.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emulate prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emulate prefers-reduced-data  
:::image-end:::  

Проблема Chromium: [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Поддержка новых функций JavaScript  

Теперь DevTools лучше поддерживает следующие языковые функции JavaScript.  

| Языковая функция JavaScript | Сведения |  
|:--- |:--- |  
| [Операторы логических назначений][V8FeaturesLogicalAssignment] | DevTools теперь поддерживает логическое назначение с помощью новых и операторов в `&&=` `||=` `??=` **средствах консоли** и **источников.**  |  
| [Числимые сепараторы][V8FeaturesNumericSeparators] с довольной печатью | DevTools теперь правильно печатает числимые сепараторы в **средстве Sources.**  |  

Проблемы с хромом: [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a>Маяк 6.2 в панели Маяк  

Средство **Lighthouse** теперь работает Lighthouse 6.2.  Полный список изменений перейдите к заметкам [о выпуске Lighthouse.][GithubGooglechromeLighthouseV620]  

Проблема Chromium: [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a>Амортизации других истоков в области "Работники службы"  

DevTools теперь предоставляет ссылку из области сотрудников службы **** **\.** Средство приложения > панели сотрудников службы\) для просмотра полного списка сотрудников служб из других истоков. ****  Чтобы получить доступ к списку без открытия DevTools, перейдите к `edge://service-worker-internals/?devtools` .  

Ранее в DevTools отображался список, вложенный в > **службы.** ****  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Ссылка на другие истоки" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Ссылка на другие истоки  
:::image-end:::  

Проблема Chromium: [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Показать сводку покрытия для отфильтрованных элементов  

DevTools теперь динамически пересчитываю и отображаем сводку сведений об охвате.  Динамический дисплей запускается при применении фильтров в средстве [Coverage.][DevtoolsCoverageIndex]  Перед тем как средство **Coverage** всегда отображает сводку всех сведений об охвате.  

В первом из следующих рисунков сводка сначала отображает, а во второй из следующих фигур отображается сводка после того, как применяется фильтрация `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Сводка по охвату" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Сводка по охвату  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Сводка по охвату для отфильтрованных элементов" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Сводка по охвату для отфильтрованных элементов  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Проблема Chromium: [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Представление новых сведений о кадре в панели Приложения  

В DevTools теперь покажите подробное представление для каждого кадра.  Чтобы получить к нему доступ, выберите кадр в меню **Frames** в **инструменте Application.**  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Новое подробное представление кадра в панели Приложения" lightbox="../../media/2020/08/frame-details.msft.png":::
   Новое подробное представление кадра в **инструменте Application**  
:::image-end:::  

Проблема Chromium: [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Сведения о кадре для открытых окон  

Открытые окна и всплывающие окна теперь отображаются и под деревом кадров.  Подробный обзор открытых окон включает дополнительные сведения о безопасности.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Новое подробное представление кадра для открытых окон" lightbox="../../media/2020/08/window-opener.msft.png":::
   Новое подробное представление кадра для открытых окон  
:::image-end:::  

Проблема Chromium: [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Сведения о безопасности и изоляции  

Безопасный контекст, [cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]и [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] теперь отображаются в деталях кадра.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Сведения о безопасности и изоляции" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Сведения о безопасности и изоляции  
:::image-end:::  

В будущем команда Microsoft Edge DevTools и команда Chrome DevTools планируют добавить дополнительные сведения о безопасности в кадр.  

Проблема Chromium: [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Обновления элементов и сетевых панелей  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Доступное предложение цвета в области Стилей  

DevTools теперь предоставляет предложения по цвету для текста с низким контрастом цвета.  

В приведенной ниже `h1` примере имеется текст с низким контрастом.  Чтобы исправить это, откройте выборщик цвета `color` свойства в области **Стилей.**  После расширения раздела **Коэффициент контраста** в DevTools предлагает предложения по цвету AA и AAA.  Выберите предложенный цвет, чтобы применить его.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Выбор цвета предлагает предложения по цвету AA и AAA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   Выбор цвета предлагает предложения по цвету AA и AAA  
:::image-end:::  

Проблема Chromium: [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Восстановление области свойств в панели Elements  

Области **свойств** возвращается.  Он был [обесценит в Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  Команда Microsoft Edge DevTools и команда Chrome DevTools планируют усовершенствования для проверки свойств элементов.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Панель свойств в панели Elements" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Области свойств** в **средстве Elements**  
:::image-end:::  

Проблема Chromium:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a>Автоматические настраиваемые шрифты в области Стилей  

Импортируемые лица шрифтов теперь добавляются в список автозаполнения CSS при редактировании свойства `font-family` в области **Стилей.**  

Например, если на локальной машине установлен настраиваемый шрифт, он отображается в `monospace` списке завершения CSS.  В предыдущих версиях Microsoft Edge шрифт не отображался.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Автоматические настраиваемые шрифты" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Автоматические настраиваемые шрифты  
:::image-end:::  

Проблема Chromium: [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Последовательно отображает тип ресурса в панели Network  

DevTools теперь последовательно отображает тот же тип ресурсов, что и исходный запрос сети, и приложения к значению столбца Type при перенаправлении `/ Redirect` \(КОД состояния HTTP 302\) происходит. ****  

Ранее DevTools изменил тип на `Other` иногда.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Отображение типа ресурса перенаправления" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Отображение типа ресурса перенаправления  
:::image-end:::  

Проблема Chromium: [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Clear buttons in the Elements and Network tools  

В следующих текстовых полях теперь есть **кнопки Clear.**  

*   Текстовые поля фильтра в **области стилей** и **средстве Network.**  
*   Текстовое поле поиска DOM в **средстве Elements.**  

Выберите **кнопку Clear,** чтобы удалить вводимый текст.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Четкие кнопки в панелях Elements" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Clear buttons in the **Elements** tools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Clear buttons in the Network panels" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Clear buttons in the  **Network** tools  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Проблема Chromium: [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Значок Параметры DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Обесценение области свойств в панели Elements — что нового в DevTools (Microsoft Edge 84) | Документы Майкрософт"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS — Что нового в DevTools (Microsoft Edge 85) | Документы Майкрософт"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включить экспериментальные API - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включить viewer source Order — экспериментальные функции | Документы Майкрософт"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "таблица — справочные | Документы Майкрософт"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS со вкладками Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering — справочная | Документы Майкрософт"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Просмотр и отламывка информации о медиа-игроках | Документы Майкрософт"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Работа с швом — введение в устройства с двойным экраном | Документы Майкрософт"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Функция экранирования экрана CSS для обнаружения двухэкранных | Документы Майкрософт"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для устройств с двойным экраном | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Код "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio клавиши кода для Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"
[CR384968]: https://crbug.com/384968 "Возможность игнорировать локальные () шрифты | Ошибки Chromium"  
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR807440]: https://crbug.com/807440 "Chrome блокируется с большим количеством SWs | Ошибки Chromium"  
[CR997694]: https://crbug.com/997694 "XHR-запросы со статусом 302 не показаны в фильтре \"xhr\" в сетевых панелях | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1054281]: https://crbug.com/1054281 "Запрос на функции: Устройства DevTools должны подражать складным и двухэкранным устройствам | Ошибки Chromium"  
[CR1067184]: https://crbug.com/1067184 "Запрос на функции: кнопка clear filter on Network & Elements -> ввода фильтра | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "☂ панели проблем корабля | Ошибки Chromium"  
[CR1080569]: https://crbug.com/1080569 "acorn не поддерживает операторов логических назначений | Ошибки Chromium"  
[CR1080589]: https://crbug.com/1080589 "Классифицировать проблемы по сторонним и | Ошибки Chromium"  
[CR1086817]: https://crbug.com/1086817 "acorn не поддерживает числимые сепараторы | Ошибки Chromium"  
[CR1090802]: https://crbug.com/1090802 "Имитация изменений состояния ожидания из API обнаружения | Ошибки Chromium"  
[CR1093227]: https://crbug.com/1093227 "DevTools: предложить ближайший доступный цвет | Ошибки Chromium"  
[CR1093247]: https://crbug.com/1093247 "Отображение информации о кадрах в панели приложений | Ошибки Chromium"  
[CR1094406]: https://crbug.com/1094406 "Разработчикам нужен зритель исходных заказов для AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: поддержка эмулировать функцию мультимедиа с пониженным | Ошибки Chromium"  
[CR1096481]: https://crbug.com/1096481 "Вопросы размещения баннеров | Ошибки Chromium"  
[CR1100253]: https://crbug.com/1100253 "Добавление ярлыка узла экрана в меню контекста Element | Ошибки Chromium"  
[CR1103316]: https://crbug.com/1103316 "Поиск элементов не решаетNode (выделение текста и т. д.) при первом поиске | Ошибки Chromium"  
[CR1103854]: https://crbug.com/1103854 "De-obfuscate X-Client-Data values in Developer Tools | Ошибки Chromium"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Добавьте импортируемые шрифты в автозаполнение семейства шрифтов в панели https://crbug.com/1106221 Styles | Ошибки Chromium"  
[CR1107766]: "Отображение информации о кадрах, созданных https://crbug.com/1107766 "window.open()" в дереве кадров | Ошибки Chromium"  
[CR1115011]: "При копировании таблицы из консоли структура таблицы не сохраняется https://crbug.com/1115011 | Ошибки Chromium"  
[CR1116085]: "Пожалуйста, верни https://crbug.com/1116085 инспектора свойств DevTools | Ошибки Chromium"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data - Media Queries Level 5 | Проекты редактора рабочей группы W3C CSS"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0 — GoogleChrome/lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Буферы протокола | Разработчики Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung US"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Логическое назначение | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Числимые сепараторы | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Создание изолированного веб-сайта \"cross-origin\" с помощью coOP и COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Обнаружение неактивных пользователей с помощью API обнаружения | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Избегайте не композитных анимаций | web.dev"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/08/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
