---
description: Поддержка отладки для CSS Flexbox, отображение на веб-странице над головой производительности, выпуск обновлений инструментов и другие
title: Новые возможности в DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408561"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-90"></a>Что нового в DevTools (Microsoft Edge 90)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a>Групповые инструменты вместе в режиме Фокус  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

Focus Mode — это экспериментальный интерфейс, который позволяет сгруппировать различные инструменты вместе на основе собственных сценариев отладки.  Новая **планка действий,** отображаемая слева, включает предопределяющие группы инструментов, такие как **Layout** и **Debugging.**  Чтобы настроить каждую группу инструментов, закройте инструменты значком **Close** \( \) или добавьте новые средства с значком `X` More **tools** `+` \( \) .  

Чтобы включить эксперимент, перейдите к включаем экспериментальные функции и выберите контрольные ящики рядом с режимом Фокус и **Инструменты DevTools** и **включить +** меню вкладок кнопки, чтобы открыть дополнительные средства . [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  Дополнительные сведения об этой функции или комментарии с вопросами и идеями перейдите к [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Отображение панели действий" lightbox="../../media/2021/02/focus-mode.msft.png":::
   Отображение **панели действий**  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a>Узнайте о DevTools с помощью информационных инструментов  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

Функция Tooltips DevTools поможет вам узнать обо всех различных средствах и стеколах.  Выберите значок Справка \( \) в нижней части панели действий, чтобы перегнастить инструменты `?` в DevTools. ****  Когда используются инструменты, наведите курсор на каждый из описанных областей DevTools, чтобы узнать больше о том, как использовать средство.  Чтобы включить эксперимент, перейдите к включаем экспериментальные функции и выберите контрольные ящики рядом с режимом Фокус и **Инструменты DevTools** и **включить +** меню вкладок кнопки, чтобы открыть дополнительные средства . [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  Дополнительные сведения об этой функции или комментарии с вопросами и идеями перейдите к [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Выберите значок Справка (?) в панели действий для отображения наборов инструментов" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   Выберите значок Справка `?` \( \) в панели **действий для** отображения наборов инструментов  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Настройка ярлыков клавиатуры в параметрах  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

Теперь можно настроить ярлык клавиатуры для любых действий в DevTools.  Чтобы изменить ярлык клавиатуры, выполните следующие действия.  

1.  Откройте DevTools и выберите **ярлыки**  >  **Параметры.**  
1.  Выберите действие, необходимое для настройки.  
1.  Выбор редактирования \.![Изменение значка ярлыка клавиатуры](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)\) значок.  
1.  Выберите клавиши, которые необходимо привязать к действию.  
1.  Выбор контрольного знака \.![Значок ярлыка клавиатуры checkmark](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)\) значок.  
    
Дополнительные сведения о настройке и редактировании ярлыков перейдите к настройкам клавиш в [Microsoft Edge DevTools.][DevtoolsCustomizeShortcuts]  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [174309][CR174309].  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Настройка ярлыков клавиатуры в параметрах DevTools на ярлыках с помощью ярлыка в режиме редактирования" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   Настройка ярлыков клавиатуры в [параметрах DevTools][DevtoolsCustomizeIndexSettings] на ярлыках с помощью ярлыка в режиме редактирования  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a>Microsoft Edge DevTools для Visual Studio обновления расширения кода 1.1.4  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

В [microsoft Edge Developer Tools для Visual Studio][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.4 для Microsoft Visual Studio Code теперь отображается февикон рядом с каждым экземпляром DevTools.  Консольные сообщения от Microsoft Edge теперь отображаются в **консоли DevTools** в статье **Output** of Microsoft Visual Studio Code.  Microsoft Visual Studio обновления кода автоматически.  Чтобы вручную обновить версию 1.1.4, перейдите к [обновлению расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  Вы можете файл проблемы и внести свой вклад в расширение [на vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub репо.  

:::row:::
   :::column span="":::
      На следующем рисунке отображаются сообщения с веб-страницы примера, зарегистрированной **в** консоли в Microsoft Edge.  
   :::column-end:::
   :::column span="":::
      На следующем рисунке отображаются те же сообщения с веб-страницы примера, зарегистрированной в **консоли DevTools** в **статье Output** of Microsoft Visual Studio Code.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Отображение сообщения в консоли в Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         Отображение сообщения в консоли в Microsoft Edge DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Отображение того же сообщения в консоли DevTools в статье Output of Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         Отображение того же сообщения в консоли DevTools в статье Output of Microsoft Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a>Улучшенное редактирование flexbox CSS с помощью визуального редактора flexbox и нескольких накладок  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

DevTools теперь имеет выделенные средства отладки flexbox CSS.  Если стиль CSS применяется к элементу HTML, значок отображается рядом с этим элементом в `display: flex` `display: inline-flex` `flex` **средстве Elements.**  Чтобы отобразить на веб-странице наложение flex \(или скрыть\) выберите `flex` значок.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1166710][CR1166710] и [1175699][CR1175699].  

:::row:::
   :::column span="":::
      Чтобы открыть **редактор Flexbox,** перейдите на области **Стилей** и выберите новый значок рядом с `display: flex` `display: inline-flex` стилем или стилем.  Редактор **Flexbox** предоставляет быстрый способ редактирования свойств flexbox.  
   :::column-end:::
   :::column span="":::
      Кроме того, раздел **Flexbox** в области **Макет** отображает все элементы flexbox на веб-странице.  Можно перенакладку каждого элемента.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Средства отладки flexbox CSS" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         Средства отладки flexbox CSS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Раздел Flexbox в области Макет" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         **Раздел Flexbox** в области **Макет**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a>Улучшения навигации по клавиатуре для сетевых запросов  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

Ранее вы не могли расширить или свернуть цепочку запросов с помощью **** клавиш стрелки на клавиатуре в области Инициатор, в отличие от DOM в **инструменте Elements.**  При выборе сетевого запроса в средстве **Network** в области Инициатор отображает цепочку запросов, которые инициировали выбранный в настоящее время запрос. ****  

В microsoft Edge версии 90 можно расширить или свернуть цепочку запросов с помощью клавиш стрелки на клавиатуре в области **Инициатор.**  Фокусный запрос сети в цепочке также теперь выделен.  Чтобы узнать больше о инициаторах в средстве **Network,** перейдите к [инициаторам отображения и зависимостей.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1158276][CR1158276] и [1160637][CR1160637].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Выберите запрос Сети и выберите области инициатора" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         Выберите запрос Сети и выберите области **инициатора**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Расширение или свернуть цепочку инициатора запроса и следовать выделенной строке" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         Расширение или свернуть цепочку инициатора запроса и следовать выделенной строке  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a>Фильтрация в консоли более согласована  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

При фильтрации с [боковой панелью][DevtoolsConsoleReferenceOpenConsoleSidebar]консоли [][DevtoolsConsoleReferenceFilterByLogLevel] фильтры в отсеве уровней журналов недоступны.  Ранее **отсев уровней** журналов выделялся при наведении на **** него, даже если был выбран фильтр из боковой панели консоли.  В Microsoft Edge версии 90 отсев уровней журналов больше не выделяется при наведении на нем при выборе фильтра из боковой панели консоли. **** ****  Чтобы узнать больше о фильтрации в **консоли,** перейдите к [фильтрации сообщений][DevtoolsConsoleReferenceFilterMessages].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Ранее, если вы откроете боковую панель консоли и наведите курсор на уровнях по умолчанию, она была выделена" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         Ранее, если вы откроете **боковую** панель консоли и наведите курсор на уровнях **по** умолчанию, она была выделена  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Начиная с Microsoft Edge 90, если выбрать боковую панель консоли и наведении на уровнях по умолчанию, она не выделяется" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         Начиная с Microsoft Edge 90, если выбрать боковую панель **консоли** и наведении на уровнях по **умолчанию,** она не выделяется  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a>Консоль теперь избегает символов двойной кавычка  

Ранее консоль не **выводит** допустимые двойные кавычка `"` \( \) символов в строках JavaScript.  Начиная с microsoft Edge версии **** 90, консоль выводит строки JavaScript с использованием избежавных двойных кавычков `"` \( \) символов.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1178530][CR1178530].  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Консоль выводит строки JavaScript с помощью сбежавных символов двойной &#0022;" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   Консоль **выводит** строки JavaScript с помощью сбежавных символов двойной `"` цитаты \( \)  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a>Эмулировать функцию CSS цветовой гаммы мультимедиа  

Запрос [мультимедиа с цветовой][ChromestatusFeature5354410980933632] гаммой эмулирует примерный диапазон цветов, поддерживаемых браузером, и тестируемого устройства.  Выпадательная информация под **эмулировать цветовую гамму CSS-мультимедиа** содержит цветовые пространства, которые могут эмулировать DevTools.  Например, чтобы вызвать запрос `color-gamut: p3` мультимедиа, выберите **цветовую гамму: p3** из отсеки.  

Чтобы подражать функции CSS цветовой гаммы мультимедиа, выполните следующие действия.  

1.  Откройте [командное меню.][DevtoolsCommandMenuIndex]  
1.  Введите `Rendering`.  
1.  Запустите **команду отрисовки отображения.**  
1.  Перейдите **к эмулировать цветовую гамму CSS-мультимедиа** и выберите вариант.  

Чтобы узнать больше об этой `color-gamut` функции, перейдите к [качеству отображения цвета: функция "цветовая гамма".][CsswgDraftsMediaqueries4ColorGamut]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1073887][CR1073887].  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Эмулировать функцию CSS цветовой гаммы мультимедиа" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   Эмулировать функцию CSS цветовой гаммы мультимедиа  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a>Улучшенная прогрессивная программа веб-приложений  

#### <a name="pwa-installability-warning-in-the-console"></a>Предупреждение об установке PWA в консоли  

Консоль **теперь** отображает более подробное предупреждение об установке прогрессивных веб-приложений [(PWA)][ProgressiveWebAppsIndex] со ссылкой на улучшение обнаружения поддержки прогрессивного веб-приложения в [автономном режиме.][ChromeDeveloperBlogImprovedPwaOfflineDetection]  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Предупреждение об установке PWA в консоли" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   Предупреждение об установке PWA в **консоли**  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a>Предупреждение о длине описания PWA в области Манифест

Теперь **в области Манифест** отображается предупреждение, если описание манифеста превышает 324 символа.  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Предупреждение об усечении описания PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   Предупреждение об усечении описания PWA  
:::image-end:::  

Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [965802,][CR965802] [1146450][CR1146450]и [1169689][CR1169689].  

### <a name="new-remote-address-space-column-in-the-network-tool"></a>Новый столбец удаленного пространства адресов в средстве Network  

<!-- does not work in canary 90.0.813.0 -->  
В новом **столбце Удаленное пространство** адресов отображается сетевое пространство IP-адресов каждого сетевого ресурса.  Чтобы отобразить новый столбец Удаленное пространство адресов, выполните следующие действия.  

1.  Перейдите к **средству Network.**  
1.  В таблице Запросы наведите курсор на строку загона и откройте контекстное меню \(правой кнопкой мыши\).  Чтобы узнать, как добавлять или удалять столбцы из таблицы Запросы, перейдите по добавлению [или удалению столбцов.][DevtoolsNetworkReferenceAddRemoveColumns]  
1.  Выберите **удаленное пространство адресов.**  
    
В таблице Запросы теперь отображается новый столбец с заготвом с именем **Удаленное пространство адресов.**  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1128885][CR1128885].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="В контекстной меню выберите удаленное пространство адресов" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         В контекстной меню выберите удаленное пространство **адресов**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="В таблице Запросы теперь отображается столбец Удаленное пространство адресов" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         В таблице Запросы теперь отображается столбец **Удаленное пространство адресов** :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a>Отображение разрешенных и отложенных функций в представлении подробностей Frame  

Представление сведений о кадре теперь отображает список разрешенных и запрещенных функций браузера, контролируемых [политикой разрешений.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]  Политика разрешений — это API веб-платформы, который позволяет \(или blocks\) веб-страницу использовать функции браузера в отдельном кадре или в iframes, которые он встраивал.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1158827][CR1158827].  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Разрешенные и отостановимые функции на основе политики разрешений" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   Разрешенные и отостановимые функции на основе политики разрешений  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a>Новый столбец SameParty в области cookies  

В **области Cookies** в **инструменте Application** теперь отображается атрибут для каждого файла `SameParty` cookie.  Атрибут — это новый атрибут boolean, который указывает, включено ли cookie в запросы на истоки тех же `SameParty` [первопартийных наборов.][GithubPrivacycgFirstPartySets]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1161427][CR1161427].  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Столбец SameParty в области Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   **Столбец SameParty** в **области Cookies**  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a>Свойство fn.displayName в средстве Консоли теперь отстает от  

Ранее свойство позволяло управлять отладкой имен для функций, отображаемой в `fn.displayName` `error.stack` и в следах стека DevTools.  Начиная с microsoft Edge версии 90, свойство теперь отстает `fn.displayName` и заменяется `fn.name` свойством.  Для определения `Object.defineProperty` свойства используйте стандартный `fn.name` метод.  Чтобы узнать больше, `fn.name` перейдите к [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1177685][CR1177685].  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Пример свойства fn.name для управления отлагиванием имен для функций" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   Пример свойства `fn.name` для управления отлагиванием имен для функций  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a>Полное представление дерева доступности в средстве Elements  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Этот эксперимент предоставляет полное представление дерева **доступности** в **средстве Elements.**  В [области доступности][DevtoolsAccessibilityReferenceTheAccessibilityPane] обеспечивается частичное представление дерева доступности, которое отображает прямую цепочку предка от корневого узла до проверенного узла.  
После включения этого эксперимента и перезагрузки DevTools выберите одну из следующих кнопок, чтобы переключить дисплей в инструменте Elements для всех элементов на веб-странице.  

*   Чтобы отобразить полное представление дерева доступности, выберите представление **Переключатель дерева доступности.**  
*   Чтобы отобразить представление дерева DOM, выберите представление **Переключатель на дерево DOM.**  
    
Чтобы включить эксперимент, перейдите к включив экспериментальные функции и выберите почтовый ящик рядом с включить полное представление дерева доступности в **области Elements.** [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [887173][CR887173].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Отображение представления дерева DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         Отображение **представления DOM**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Отображение полного представления дерева доступности" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         Отображение представления **Дерева полнодоступности**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Области доступности — справочные | Документы Майкрософт"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтр по уровню журнала — консольная справочная | Документы Майкрософт"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Фильтрация сообщений — справочные | Документы Майкрософт"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Откройте боковую панель консоли — справочные | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Включить меню вкладки + кнопки, чтобы открыть дополнительные средства - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Добавление или удаление столбцов — ссылки на | Документы Майкрософт"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Отображение инициаторов и зависимостей — справочные | Документы Майкрософт"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в обзоре Windows | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — расширение marketplace | Visual Studio Код"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Улучшение обнаружения прогрессивных веб-приложений в автономном режиме | Разработчики Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "запрос мультимедиа с цветовой гаммой | Состояние платформы Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR174309]: https://crbug.com/174309 "Проблема 174309: средства разработчика: разрешение настройки сочетания клавиш | Ошибки Chromium"  
[CR887173]: https://crbug.com/887173 "Выпуск 887173: DevTools: Проверка дерева полной доступности | Ошибки Chromium"  
[CR965802]: https://crbug.com/965802 "Выпуск 965802. Реализация более точного обнаружения автономных возможностей сотрудника службы | Ошибки Chromium"  
[CR1073887]: https://crbug.com/1073887 "Выпуск 1073887: DevTools: @media (цветовая гамма: ...) эмуляция | Ошибки Chromium"  
[CR1128885]: https://crbug.com/1128885 "Выпуск 1128885: поддержка DevTools для corS-RFC1918 | Ошибки Chromium"  
[CR1146450]: https://crbug.com/1146450 "Выпуск 1146450: [Android] Реализация нижнего листа | Ошибки Chromium"  
[CR1158276]: https://crbug.com/1158276 "Выпуск 1158276: невозможно расширить и задать контракт области "Цепочка инициаторов запроса" с помощью клавиш стрелки в разделе "Сеть" в DevTools | Ошибки Chromium"  
[CR1158827]: https://crbug.com/1158827 "Выпуск 1158827: [Политика разрешений] Реализация поддержки devtool политики разрешений | Ошибки Chromium"  
[CR1160637]: https://crbug.com/1160637 "Выпуск 1160637. Фокус на "цепочке инициаторов запроса" рассматривается неполным в разделе "Сеть" окна "Средства разработчика" | Chromium Bugs"  
[CR1161427]: https://crbug.com/1161427 "Выпуск 1161427: &#9730; отладка атрибута cookie SameParty в DevTools | Ошибки Chromium"  
[CR1166710]: https://crbug.com/1166710 "Выпуск 1166710: включить эксперимент по инструментарию flexbox по умолчанию | Ошибки Chromium"  
[CR1169689]: https://crbug.com/1169689 "Выпуск 1169689: нижний лист установки PWA не должен иметь категорий | Ошибки Chromium"  
[CR1175699]: https://crbug.com/1175699 "Выпуск 1175699: редактор Flexbox | Ошибки Chromium"  
[CR1177685]: https://crbug.com/1177685 "Выпуск 1177685: Удаление нестандартной поддержки fn.displayName | Ошибки Chromium"  
[CR1178530]: https://crbug.com/1178530 "Выпуск 1178530: консоль не избегает двойных квотов при печати строк | Ошибки Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Качество отображения цвета: функция "цветовая гамма" | Черновики редактора рабочей группы CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: пользовательский интерфейс режима фокуса — MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Первопартийные наборы | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Объяснятель политики разрешений | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/02/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
