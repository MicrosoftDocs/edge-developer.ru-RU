---
description: Новые средства отладки сетки CSS, средство webauthn, перемещаемые средства и вычисленная панель боковой панели.
title: Новые возможности DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/26/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 88e6678880172a7a494bcf73c74874aeb70c24b9
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325961"
---
# Новые возможности DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Улучшение локализации DevTools  

Для удовлетворения ваших потребностей в переводе команда Разработчиков Microsoft Edge нацелена на улучшение качества перевода.  Начиная с Microsoft Edge версии 87, несколько строк и терминов заблокированы и не изменяются, даже если остальные языки DevTools отображаются на других языках.  Список затронутых строк и терминов включает следующие строки и термины.  

*   Строки в **средстве Lighthouse.**  
*   Термин `service worker` .  
*   Некоторые **фильтры сетевого** инструмента, такие как `URL` , , , и `XHR` `JS` `CSS` .  
*   API консольных жков [$0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] теперь доступно в консоли для [пользователей](/microsoft-edge/devtools-guide-chromium/console/index.md) локализованных версий DevTools.   Благодарим глобальное сообщество разработчиков за помощь в локализации Microsoft Edge DevTools.  Продолжайте отправлять [отзывы о качестве локализации,](#getting-in-touch-with-microsoft-edge-devtools-team) чтобы улучшить поддержку DevTools во всех региональных стандартах.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1136655.][CR1136655]  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Сетевое средство с не локализованными фильтрами" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Сетовая** области с не локализованными фильтрами  
:::image-end:::  

## Перемещение инструментов между верхней и нижней панелями  

DevTools теперь поддерживает перемещение инструментов между верхней и нижней панелями.  Настройте DevTools и улучшите производительность, одновременно просматривая любое сочетание двух средств.  Например, просмотр **** элементов и инструментов **Sources** одновременно \(путем перемещения инструмента **Sources** в нижнюю часть\).  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к [#1075732.][CR1075732]  

:::row:::
   :::column span="":::
      Чтобы переместить любое верхнее средство в нижнюю часть, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить в нижнюю часть"**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Перейти к нижнему" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Перейти к нижнему  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Чтобы переместить любое средство снизу вверх, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить вверх"**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Перейти к началу" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Перейти к началу  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Сохранение и экспорт с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь **средство сетевой** консоли улучшено совместимость со схемами [Postman 2.1][PostmanSchemaJsonCollectionv210Index] и [OpenAPI v2.][SwaggerSpecificationV2]  Чтобы включить эксперимент, перейдите к функции ["Включить][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] экспериментальную" и выберите "Включить сетевую консоль" рядом с **ней.**  Для получения дополнительных сведений о **сетевой консоли**перейдите к экспериментальной функции "Включить экспериментальную сетевую [консоль".][DevtoolsExperimentalFeaturesEnableNetworkConsole]  Этот эксперимент теперь поддерживает следующие действия.  

*   Сохранение и экспорт коллекций и сред.  
*   Изменение и экспорт наборов переменных среды в **средстве сетевой консоли.**  
    
Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1093687.][CR1093687]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Введите имя новой среды" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Введите имя новой среды  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Выбор формата для новой среды" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Выбор формата для новой среды  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Улучшенные инструменты сетки CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь Microsoft Edge DevTools поддерживает следующие функции для проверки, просмотра и отладки сетки CSS.  

*   Отображение упрощенного наложения сетки с помощью средства **inspect** или получения более подробных сведений с постоянными наложениями.  
*   Чтобы включить наложения сохраняемой сетки, выберите значок сетки рядом с элементом контейнера сетки в средстве **"Элементы"** или выберите сетку в средстве **макета.**  
*   Можно включить постоянные наложения для нескольких сеток.  
*   Новое средство **layout** позволяет легко перегрешить наложения сетки и настроить внешний вид и содержимое для каждого из них.  
    
Функции по умолчанию отключены.  Дополнительные сведения о функции можно найти в [сетках CSS.][DevtoolsCssGrid]  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к [#1047356.][CR1047356]  Кроме того, группа разработчиков Microsoft Edge devTools совместно с командой Chrome DevTools и сообществом Chromium добавляет новые гибкие инструменты в DevTools.  Для обновления инструментов flexbox в проекте с открытым исходным кодом Chromium перейдите к [#1136394.][CR1136394]  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Средство макета с сетками" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Средство макета** с сетками  
:::image-end:::  

## Настройка сочетания клавиш в параметрах  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете настроить ярлык клавиатуры для любого действия в DevTools.  Начиная с Microsoft Edge версии 84, вы можете выбрать между Visual Studio **Code** и **DevTools (по умолчанию)** для сочетания [клавиш.][DevtoolsCustomizeShortcuts]  Начиная с Microsoft Edge версии 87, **** вы можете включить эксперимент "Включить редактор сочетания клавиш" для дальнейшей настройки сочетания [клавиш.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Чтобы включить эксперимент, перейдите к функции ["Включить][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] экспериментальную" и выберите "Включить редактор сочетания **клавиш".**  Дополнительные сведения о настройке и изменении сочетаний клавиш см. в разделе о [включении экспериментальной функции редактора сочетания клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#174309.][CR174309]  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Настраиваемый ярлык для прио паузы в сценарии" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Настраиваемый ярлык для прио паузы в сценарии  
:::image-end:::  

## Знакомство с расширением Microsoft Edge tools for Visual Studio Code  

Элементы **для Visual Studio Code** and **Network for Visual Studio Code** теперь объединены в новое расширение Microsoft Edge Developer Tools для Visual Studio [Code.][VisualStudioCodeMarketplaceMsEdgedevtools]  Используйте Microsoft Edge DevTools для следующих действий, не Visual Studio Code.  

*   Отлаговка DOM  
*   Редактирование CSS  
*   Проверка сетевого трафика  

С помощью расширения запустите Microsoft Edge, подключите существующий экземпляр браузера или используйте браузер без headless непосредственно из редактора.  Чтобы начать вносить в отзывы о расширении свои отзывы и вносить в них документы, перейдите к репозиту "Инструменты разработчика Microsoft [Edge для Visual Studio][GithubMicrosoftVscodeEdgeDevtools] кода" на GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Снимок экрана с использованием расширения в полно браузерном режиме" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Снимок экрана с использованием расширения в полно браузерном режиме  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Снимок экрана с использованием расширения в безголовом режиме" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Снимок экрана с использованием расширения в безголовом режиме  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Новое средство WebAuthn  

В более ранних версиях Microsoft Edge не существовало поддержки отладки WebAuthn.  Для тестирования веб-приложения с помощью API веб-проверки подлинности необходимы [физические аутентификация.][GithubW3cWebauthn]  С помощью нового **средства WebAuthn** можно делать следующие действия без использования физических средств проверки подлинности.

*   Эмуляция аутентификаций
*   Настройка атрибутов аутентификаций
*   Проверка состояния аутентификаций
    
Дополнительные сведения о функции **WebAuthn** см. в эмуляторе аутентификаций и отладке [WebAuthn в Microsoft Edge DevTools.][DevtoolsWebauthnIndex]  

Вы можете эмулировать средства проверки подлинности и отлагонять [API][GithubW3cWebauthn] веб-проверки подлинности с помощью нового средства [WebAuthn.][DevtoolsWebauthnIndex]  Чтобы открыть средство **WebAuthn,** выберите значок "Настройка и управление **DevTools** \( \) > Другие средства `...` ****  >  **WebAuthn**.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1034663.][CR1034663]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Открытие средства WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Открытие средства **WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **Средство WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Обновления средства "Элементы"  

#### Просмотр вычисляемой боковой панели в области стилей  

Перегоняем **вычисляемую области** в **области** стилей.  **Вычисляемая области** в **области** стилей по умолчанию свернута.  Чтобы его пережать, выберите кнопку.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1073899.][CR1073899]  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Открытие вычисленной боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Открытие **вычисленной боковой панели**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Вычисляемая панель боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Вычисляемая панель боковой** панели  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Группировка свойств CSS в вычисляемой панели  

Чтобы просмотреть примененную CSS с меньшей прокрутки, сгруппировать свойства CSS по категориям в **вычисляемой** области.  Вы также можете выборочно сосредоточиться на наборе связанных свойств при проверке CSS.  В **средстве "Элементы"** выберите элемент.  Чтобы сгруппировать (или разгруппировать\) свойства CSS, перебейте **этот контрольный** ящик группы.  Чтобы просмотреть обновления в режиме реального времени для этой функции [][CR1096230]в проекте с открытым исходным кодом Chromium, перейдите к #1096230, [#1084673][CR1084673]и [#1106251.][CR1106251]  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Группировка свойств CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Группировка свойств CSS  
:::image-end:::  

### Lighthouse 6.4 в средстве Lighthouse  

Средство **Lighthouse** теперь работает под управлением Lighthouse 6.4.  Полный список изменений можно найти в заметках о [выпуске Lighthouse.][GithubGoogleChromeLighthouseReleasesV641]  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#772558.][CR772558]  

### События performance.mark() в разделе "Синхронизация"  

Раздел **"Синхронизация" записи** в средстве ["Производительность"][DevtoolsGuideChromiumEvaluatePerformanceReference] теперь пометит `performance.mark()` события.  Чтобы попробовать эту функцию и оценить производительность кода JavaScript, добавьте `performance.mark()` события в код.  Например, следующий фрагмент кода добавляет маркеры до и после цикла, который итерирует от 0 до 1000 с помощью добавок `for` 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Затем откройте средство ["Производительность"][DevtoolsGuideChromiumEvaluatePerformanceReference] и перейдите к разделу **"Синхронизация",** чтобы записать код JavaScript.  Добавленные `performance.mark()` события теперь отображаются в записи.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="События Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` events  
:::image-end:::  

### Новые фильтры типа ресурса и URL-адресов в средстве "Сеть"  

Используйте новые и `resource-type` `url` ключевые слова в средстве **"Сеть"** для фильтрации сетевых запросов.  Например, используйте, `resource-type:image` чтобы сосредоточиться на сетевых запросах, которые являются изображениями.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="фильтр типа ресурса" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   фильтр типа ресурса  
:::image-end:::  

Чтобы найти более специальные ключевые слова, такие как `resource-type` и `url` , перейдите к [фильтрации запросов по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties].  Чтобы просмотреть обновления этой функции в режиме реального времени в [][CR1121141] проекте с открытым исходным кодом Chromium, перейдите к #1121141 и [#1104188.][CR1104188]  

### Обновления представления сведений о фрейме  

#### Отображение отчетов COEP и COOP в конечной точке  

Просмотреть конечную точку политики меж источника embedder \(COEP\) и политику межпрогонного открытия \(COOP\) в разделе "Изоляция & `reporting to` безопасности". ****  API [отчетов][MdnReportingApi] определяет новый http-заголовок, который позволяет указать конечные точки сервера для браузера для отправки предупреждений и `Report-To` ошибок.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1051466.][CR1051466]  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Отчеты в конечную точку" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   `reporting to`Конечная точка  
:::image-end:::  

#### Отображение режима только отчетов COEP и COOP  

Теперь DevTools отображает `report-only` метку для COEP и COOP, которые настроены в `report-only` режиме.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1051466.][CR1051466]  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Метка режима "Только отчет"" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   Метка `report-only` режима  
:::image-end:::  

### Просмотр и устранение проблем цветовой контрастности в средстве "Обзор CSS"  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь в средстве "Обзор **CSS"** отображается список элементов на странице с проблемой цветовой контрастности.  На следующей демонстрации имеется пример проблемы с цветовой контрастностью.  

[Демонстрация доступных цветов CSS][GlitchCssOverviewAccessibleColorsDemo]  

Чтобы включить этот эксперимент, в **области "Эксперименты**  >  **параметров"** выберите параметр **"Обзор CSS".**  Чтобы просмотреть список элементов с проблемой **** цветовой контрастности, в области "Проблемы с контрастом" выберите **"Текст".**  Чтобы открыть элемент в средстве **Elements,** выберите элемент в списке.  Чтобы устранить проблемы контрастности, Microsoft Edge DevTools автоматически [предоставляет варианты цвета.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к [#1120316.][CR1120316]  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Проблемы низкой цветовой контрастности" lightbox="../../media/2020/10/css-overview.msft.png":::
   Проблемы низкой цветовой контрастности  
:::image-end:::  

## Скачивание Microsoft Edge предварительных каналов  

Если вы используете Windows или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Deprecation of the Properties pane in the Elements tool - What's new in DevTools (Microsoft Edge 84) | Документы Майкрософт"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS — новые возможности DevTools (Microsoft Edge 85) | Документы Майкрософт"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Предложение доступных цветов в области стилей — новые возможности в DevTools (Microsoft Edge 86) | Документы Майкрософт"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript — справочник по API консольных utilities | Документы Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справочник по анализу производительности | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Эмуляция: поддержка режима двойного экрана — экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включить экспериментальные API - экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор сочетания клавиш — экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка режима двойного экрана — экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Enable Network Console - Experimental features | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на устройствах с двумя и двумя экранами — экспериментальные | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включить экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "table — справочник по API консоли | Документы Майкрософт"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS на вкладке "Охват" в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Проверка сетки CSS | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "Отрисовка " Справочник по анализу производительности" | Документы Майкрософт"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отлагивание сведений об игроках мультимедиа | Документы Майкрософт"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Фильтрация запросов по свойствам : справочник по анализу сети | Документы Майкрософт"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Эмуляция аутентификаций и отладка WebAuthn в Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Средства Microsoft Edge для Visual Studio кода | Visual Studio кода"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: позволяет настраивать сочетания клавиш и привязки клавиш | Ошибки Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии lighthouse | Ошибки Chromium"  
[CR1034663]: https://crbug.com/1034663 "Создание серверного приложения для API тестирования WebAuthn | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Таблица CSS/ Flexbox/Таблица | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP и COEP в DevTools | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "Вычисляемая стиль" исчезает в адаптивном режиме | Ошибки Chromium"  
[CR1075732]: https://crbug.com/1075732 "Персонализация DevTools — вкладки Movable | Ошибки Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: улучшение способа, который мы представляем настраиваемые свойства CSS ((aka). Переменные CSS) и их значения | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создайте средство для создания и воспроизведения искусственных сетевых запросов | Ошибки Chromium"  
[CR1096230]: https://crbug.com/1096230 "Группировать свойства CSS по категориям в области вычисляемой | Ошибки Chromium"  
[CR1104188]: https://crbug.com/1104188 "Поиск с помощью сетевого средства не находит результатов при поиске полного URL-адреса | Ошибки Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: улучшение вкладки "Вычисляемая стили| Ошибки Chromium"  
[CR1120316]: https://crbug.com/1120316 "Выделение плохой контрастности в обзоре CSS > цветов | Ошибки Chromium"  
[CR1121141]: https://crbug.com/1121141 "Разрешить фильтрацию по типу ресурса в сетевых журналах | Ошибки Chromium"  
[CR1121312]: https://crbug.com/1121312 "Параметры следует удалить из меню "Дополнительные инструменты" | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Набор инструментов Flexbox | Ошибки Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools: локализация 2 | Ошибки Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Отчеты API | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1 — GoogleChrome/lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-проверка подлинности | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hello! | Временный сбой"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Формат коллекции Postman 2.1.0 | Postman"  

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
