---
description: Новые средства отладки CSS Grid, средство Webauthn, инструменты для перемещения и панель компьютерной панели.
title: Новые возможности в DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 53aa8f20ba400c7ff95432b1e752f1f008dac919
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408334"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a>Что нового в DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a>Улучшение локализации DevTools  

Чтобы удовлетворить ваши потребности в переводе, команда Microsoft Edge DevTools нацелена на улучшение качества перевода.  Начиная с microsoft Edge версии 87, несколько строк и терминов заблокированы и не изменяются даже при отображке остальных версий DevTools на других языках.  Список затронутых строк и терминов включает следующие.  

*   Строки в **средстве Маяк.**  
*   Термин `service worker` .  
*   Некоторые **фильтры сетевых** средств, такие `URL` как , и `XHR` `JS` `CSS` .  
*   API [консоли $0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] теперь доступен [](/microsoft-edge/devtools-guide-chromium/console/index.md) в консоли для пользователей локализованных версий DevTools.   Спасибо глобальному сообществу разработчиков за помощь в улучшении локализации Microsoft Edge DevTools.  Продолжайте отправлять [отзывы о качестве локализации,](#getting-in-touch-with-microsoft-edge-devtools-team) чтобы улучшить поддержку DevTools во всех локальных местах.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Сетевой инструмент с не локализованными фильтрами" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Сетевое** панно с не локализованными фильтрами  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Перемещение инструментов между верхними и нижними панелями  

DevTools теперь поддерживает перемещение инструментов между верхней и нижней панелями.  Настройте devTools и повысите производительность, одновременно просматривая любое сочетание двух инструментов.  Например, просмотр **элементов** и средств **Sources** одновременно \(путем перемещения средства **Источники** в нижнее\).  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1075732.][CR1075732]  

:::row:::
   :::column span="":::
      Чтобы переместить любой верхний инструмент в нижнее, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Перемещение в нижнее**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Перемещение в нижнее" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Перемещение в нижнее  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Чтобы переместить любой нижний инструмент в верхнюю часть, наведите курсор на вкладку, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Перемещение вверх.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Перемещение на вершину" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Перемещение на вершину  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a>Сохранение и экспорт с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Средство **сетевой** консоли теперь имеет улучшенную совместимость с схемами [Postman v2.1][PostmanSchemaJsonCollectionv210Index] и [OpenAPI v2.][SwaggerSpecificationV2]  Чтобы включить эксперимент, перейдите к [включаем экспериментальные функции][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и выберите почтовый ящик рядом с **сетевой консолью.**  Дополнительные сведения о **сетевой консоли**перейдите к [функции Включить экспериментальную][DevtoolsExperimentalFeaturesEnableNetworkConsole]функцию сетевой консоли .  В этом эксперименте теперь поддерживаются следующие действия.  

*   Сохранение и экспорт коллекций и сред.  
*   Изменить и экспортировать наборы переменных среды в **средстве сетевой консоли.**  
    
Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Введите имя для новой среды" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Введите имя для новой среды  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Выберите формат для новой среды" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Выберите формат для новой среды  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a>Улучшено средство CSS Grid  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь Microsoft Edge DevTools поддерживает следующие функции для проверки, просмотра и отладки сетки CSS.  

*   Отображение упрощенной сетки с помощью средства **Inspect** или получения более подробных сведений с постоянными наложениями.  
*   Чтобы включить постоянные наложения сетки, выберите значок сетки рядом с элементом контейнера сетки в средстве **Elements** или выберите сетку в **средстве Layout.**  
*   Вы можете включить постоянные наложения для нескольких сетей.  
*   Новый инструмент **Layout** позволяет легко настраивать наложения сетки и настраивать внешний вид и содержимое для каждого из них.  
    
Функции включены по умолчанию.  Дополнительные сведения об этих функциях перейдите к [сеткам CSS.][DevtoolsCssGrid]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1047356][CR1047356].  Кроме того, команда Microsoft Edge DevTools сотрудничает с командой Chrome DevTools и сообществом Chromium, чтобы добавить в DevTools новые функции инструментов flexbox.  Для обновления инструментов flexbox в проекте с открытым исходным кодом Chromium перейдите к выпуску [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Средство макета с сетками" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Средство макета** с сетками  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Настройка ярлыков клавиатуры в параметрах  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете настроить ярлык клавиатуры для любого действия в DevTools.  Так как Microsoft Edge версии 84, вы можете выбрать между Visual Studio **код** и **DevTools (по умолчанию)** предуговосток для [клавиши ярлыки][DevtoolsCustomizeShortcuts].  Начиная с microsoft Edge версии 87, вы можете включить эксперимент редактора клавиши **Включить,** чтобы дополнительно настроить ярлыки [клавиатуры.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Чтобы включить эксперимент, перейдите к [включаем экспериментальные][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] функции и выберите почтовый ящик рядом с **редактором клавиши Включить**ярлык .  Дополнительные сведения о настройке и изменении сочетаний клавиш см. в разделе о [включении экспериментальной функции редактора сочетания клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Настраиваемый ярлык для прио паузы в скрипте" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Настраиваемый ярлык для прио паузы в скрипте  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Введение microsoft Edge Tools для расширения Visual Studio кода  

Элементы **для Visual Studio и** сети для **Visual Studio** теперь объединены в новые средства разработки Microsoft Edge для [расширения][VisualStudioCodeMarketplaceMsEdgedevtools] Visual Studio кода.  Используйте Microsoft Edge DevTools для следующих действий, не покидая Microsoft Visual Studio Code.  

*   Отламка DOM  
*   Изменение CSS  
*   Проверка сетевого трафика  

С помощью расширения запустите Microsoft Edge, подключите существующий экземпляр браузера или используйте безголовые браузеры непосредственно из редактора.  Чтобы начать вносить свой вклад и подавать свои отзывы об этом расширении, перейдите в [Microsoft Edge Developer Tools для][GithubMicrosoftVscodeEdgeDevtools] Visual Studio кода на GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Использование экрана расширения в режиме полного браузера" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Использование экрана расширения в режиме полного браузера  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Использование расширения в безголовом скриншоте режима" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Использование расширения в безголовом скриншоте режима  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a>Новый инструмент WebAuthn  

В более ранних версиях Microsoft Edge не было поддержки отладки webAuthn.  Чтобы протестировать свое веб-приложение с API веб-проверки подлинности, необходимы [физические аутентификации.][GithubW3cWebauthn]  С помощью нового **средства WebAuthn** вы можете делать следующие действия без использования каких-либо физических аутентификаций.

*   Эмулировать аутентификацию
*   Настройка атрибутов аутентификаций
*   Проверка состояния аутентификаций
    
Дополнительные сведения о функции **WebAuthn** перейдите к эмулировать аутентификацию и отладку [WebAuthn в Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Вы можете эмулировать аутентификацию и отладить API веб-проверки [подлинности][GithubW3cWebauthn] с помощью нового средства [WebAuthn.][DevtoolsWebauthnIndex]  Чтобы открыть **средство WebAuthn,** выберите значок Настройка и управление **значком DevTools** \( \) > Дополнительные средства `...` ****  >  **WebAuthn**.  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Откройте средство WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Откройте **средство WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **Средство WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a>Обновления инструмента Elements  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Просмотр области компьютерной боковой панели в области Стилей  

Переналадка **вычислительной области** в области **Стилей.**  Вычислительная **области** в области **Стилей** разрушается по умолчанию.  Чтобы его перенажать, выберите кнопку.  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Откройте панель computed sidebar" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Откройте панель **computed sidebar**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Вычислительная панель боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Вычислительная панель боковой** панели  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a>Группировка свойств CSS в панели Computed  

Чтобы просмотреть примененный CSS с меньшим прокрутки, сгруппировать свойства CSS по категориям в **области Computed.**  Вы также можете выборочно сосредоточиться на наборе связанных свойств во время проверки CSS.  Из средства **Elements** выберите элемент.  Чтобы сгруппировать \(или разгруппировать\) свойства CSS, перегнастить **групповой почтовый** ящик.  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к [#1096230,][CR1096230] [#1084673][CR1084673]и [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Группировка свойств CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Группировка свойств CSS  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a>Маяк 6.4 в средстве Маяк  

Инструмент **Lighthouse** теперь работает Lighthouse 6.4.  Полный список изменений перейдите к заметкам [о выпуске Lighthouse.][GithubGoogleChromeLighthouseReleasesV641]  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>события performance.mark() в разделе Timings  

Раздел **Timings записи** в средстве [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] теперь отмечает `performance.mark()` события.  Чтобы попробовать эту функцию и оценить производительность кода JavaScript, добавьте `performance.mark()` события в код.  Например, следующий фрагмент кода добавляет маркеры до и после цикла, который итерирует от 0 до 1000 с помощью приращений `for` 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Затем откройте средство [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] и перейдите в раздел **Timings для** записи кода JavaScript.  Добавленные `performance.mark()` события теперь отображаются в записи.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="События Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` события  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Новые фильтры типа ресурсов и URL-адресов в средстве Network  

Используйте новые `resource-type` и `url` ключевые слова в средстве **Network** для фильтрации сетевых запросов.  Например, используйте `resource-type:image` для фокусии на сетевых запросах, которые являются изображениями.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="фильтр типа ресурса" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   фильтр типа ресурса  
:::image-end:::  

Чтобы узнать больше специальных ключевых слов, таких как `resource-type` `url` и , перейдите к [фильтрации запросов по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties].  Чтобы просмотреть обновления этой функции в проекте с открытым исходным [][CR1121141] кодом Chromium в режиме реального времени, перейдите к #1121141 [и #1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Обновления представления сведений о фрейме  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Отображение отчетов COEP и COOP в конечной точке  

Просмотр конечной точки политики встраивщика cross-origin \(COEP\) и политики открытия кросс-происхождения \(COOP\) в разделе Изоляция & `reporting to` безопасности. ****  API [отчетов][MdnReportingApi] определяет новый http-заголовок, который позволяет указать конечные точки сервера для браузера для отправки предупреждений и `Report-To` ошибок.  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Отчеты до конечной точки" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   `reporting to`Конечная точка  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Отображение режима отчетов только для COEP и COOP  

В DevTools теперь `report-only` отображаются метки coEP и COOP, задаваемые в `report-only` режиме.  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Метка режима только для отчетов" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Метка `report-only` режима  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Просмотр и устранение проблем контрастности цветов в инструменте CSS Overview  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Средство **CSS Overview** теперь отображает список элементов на странице с вопросами контрастности цвета.  На следующей демо-странице приводится пример проблемы контраста цвета.  

[Демонстрация доступных цветов CSS Обзор][GlitchCssOverviewAccessibleColorsDemo]  

Чтобы включить этот эксперимент, в **статье**  >  **Settings Experiments**выберите почтовый ящик **CSS Overview.**  Чтобы просмотреть список элементов с проблемой контрастности цвета, **выберите** **Текст**.  Чтобы открыть элемент в **средстве Elements,** выберите элемент в списке.  Чтобы помочь устранить проблемы контрастности, Microsoft Edge DevTools автоматически [предоставляет цветовые предложения.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Проблемы с контрастом цвета" lightbox="../../media/2020/10/css-overview.msft.png":::
   Проблемы с контрастом цвета  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Обесценение области свойств в средстве Elements — что нового в DevTools (Microsoft Edge 84) | Документы Майкрософт"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS — Что нового в DevTools (Microsoft Edge 85) | Документы Майкрософт"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Доступное предложение цвета в области Стилей — что нового в DevTools (Microsoft Edge 86) | Документы Майкрософт"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript — справочные ссылки на API консоли | Документы Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справочные ссылки | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включить экспериментальные API - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор ярлыка клавиатуры — экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка режима двойного экрана — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Включить сетевые консоли — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включить viewer source Order — экспериментальные функции | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складных и двухэкранных устройствах — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "таблица — справочные | Документы Майкрософт"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS со вкладками Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Проверка CSS Grid | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering — справочная | Документы Майкрософт"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отламывка информации о медиа-игроках | Документы Майкрософт"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Запросы фильтрации по свойствам — эталонный | Документы Майкрософт"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Эмулировать аутентификацию и отладку WebAuthn в Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Код"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR1034663]: https://crbug.com/1034663 "Создание переднего входа для API тестирования WebAuthn | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка computed style исчезает в режиме отклика | Ошибки Chromium"  
[CR1075732]: https://crbug.com/1075732 "Персонализация DevTools — вкладки Movable | Ошибки Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: улучшаем способ, который мы представляем пользовательским свойствам CSS (aka). Переменные CSS) и их значения | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и воспроизведения синтетических сетевых запросов | Ошибки Chromium"  
[CR1096230]: https://crbug.com/1096230 "Свойства группы CSS по категориям в области вычислительных стилей | Ошибки Chromium"  
[CR1104188]: https://crbug.com/1104188 "Поиск сетевых средств не находит результатов при поиске полного URL-адреса | Ошибки Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: улучшение вкладки Computed Styles | Ошибки Chromium"  
[CR1120316]: https://crbug.com/1120316 "Выделение плохого контраста в CSS Обзор > цвета | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Разрешить фильтрацию по типу ресурса в сетевом журнале | Ошибки Chromium"  
[CR1121312]: https://crbug.com/1121312 "Параметры должны быть удалены из меню More Tools | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Flexbox tooling | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Локализация V2 | Ошибки Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Отчет об API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 — GoogleChrome/lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-| GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Привет! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Формат коллекции почтальонов v2.1.0 | Почтальон"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Спецификация OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/10/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
