---
description: Новые инструменты для отладки в КАСКАДных таблицах, средства Webauthn, средства для перемещаемых и вычисляемых панелей.
title: Новые возможности DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190007"
---
# Новые возможности DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Улучшение локализации DevTools  

В соответствии с потребностями перевода группа Microsoft Edge DevTools фокусируется на улучшении качества перевода.  Начиная с Microsoft Edge версии 87, некоторые строки и условия заблокированы и не изменяются даже в том случае, если остальные DevTools отображаются на других языках.  Ниже перечислены затронутые строки и термины.  

*   Строки в инструменте **Lighthouse** .  
*   Термин `service worker` .  
*   Некоторые фильтры **сетевых** средств, такие как `URL` ,, `XHR` `JS` и `CSS` .  
*   API-интерфейс служебных программ для консоли [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] теперь доступен на [консоли](/microsoft-edge/devtools-guide-chromium/console/index.md) для пользователей локализованных версий DevTools.   Благодарим вас за участие в глобальном сообществе разработчиков, которые помогут вам улучшить локализацию Microsoft Edge DevTools.  Продолжите [отправку обратной связи по качеству локализации](#getting-in-touch-with-microsoft-edge-devtools-team) для улучшения поддержки DevTools на всех языках.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Сетевое средство с нелокализованными фильтрами" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   Область **сети** с нелокализованными фильтрами  
:::image-end:::  

## Перемещение инструментов между верхней и нижней панелями  

DevTools теперь поддерживает перемещение инструментов между верхней и нижней панелями.  Настройка DevTools и повышение продуктивности благодаря одновременному просмотру любой комбинации двух инструментов.  Например, вы можете одновременно просматривать **элементы** и инструменты **исходного** кода (путем перемещения инструмента **источники** вниз).  Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Чтобы переместить верхний инструмент в нижнюю часть экрана, наведите на него указатель мыши, откройте контекстное меню, а затем выберите пункт **Переместить вниз**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Переместить вниз" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Переместить вниз  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Чтобы переместить нижние инструменты в верхнюю часть экрана, наведите указатель мыши на вкладку, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Перейти к началу**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Перейти к началу страницы" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Перейти к началу страницы  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Сохранение и экспорт с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Средство **Network Console** теперь повысило совместимость с схемами [posts v 2.1][PostmanSchemaJsonCollectionv210Index] и [OpenAPI v2][SwaggerSpecificationV2] .  Чтобы включить функцию эксперимента, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить сетевую консоль**.  Дополнительные сведения о **сетевой консоли**можно найти в разделе [Включение экспериментальной сетевой консоли][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Этот эксперимент теперь поддерживает описанные ниже действия.  

*   Сохранение и экспорт коллекций и сред.  
*   Изменяйте и экспортируйте наборы переменных среды в инструменте **Network Console** .  
    
Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Введите имя новой среды" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Введите имя новой среды  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Выберите формат для новой среды" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Выберите формат для новой среды  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Улучшенные инструменты сетки CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Microsoft Edge DevTools теперь поддерживает следующие функции для проверки, просмотра и отладки сетки каскадных стилей.  

*   Отображение упрощенного раскрытия сетки с помощью средства **проверки** или получение более подробных сведений с постоянными наложениями.  
*   Чтобы включить постоянную наложение сетки, щелкните значок сетки рядом с элементом контейнера сетки в инструменте **элементы** или выберите сетку в инструменте **Макет** .  
*   Вы можете включить постоянную наложение для нескольких сеток.  
*   С помощью нового инструмента " **Макет** " можно легко переключать наложения сетки и настраивать внешний вид и содержимое каждого из них.  
    
Эти функции включены по умолчанию.  Дополнительные сведения о функциях можно найти в [таблице каскадных таблиц стилей][DevtoolsCssGrid].  Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1047356][CR1047356].  Кроме того, группа Microsoft Edge DevTools работает совместно с коллегами по DevTools и Chromiumом для добавления новых функций управления подложкой в DevTools.  Чтобы получить обновления для средств управления подпадающими ящиками в проекте Open-Source Chromium, перейдите к вопросу [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Инструмент "макет" с сетками" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   Инструмент " **Макет** " с сетками  
:::image-end:::  

## Настройка сочетаний клавиш в параметрах  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете настроить сочетание клавиш для любого действия в DevTools.  Поскольку Microsoft Edge версии 84, вы можете выбирать из **кода Visual Studio** и **DevTools (по умолчанию)** стандартные наборы сочетаний [клавиш][DevtoolsCustomizeShortcuts].  Начиная с Microsoft Edge версии 87, вы можете включить **Редактор сочетаний клавиш включения** экспериментов для дальнейшей [настройки сочетаний клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Чтобы включить функцию эксперимента, перейдите к разделу [Включение экспериментальных функций][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] и установите флажок **включить редактор сочетаний клавиш**.  Дополнительные сведения о настройке и редактировании сочетаний клавиш можно найти в статье [включить режим экспериментального редактора сочетаних][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]клавиш.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Настраиваемое сочетание клавиш для приостановки сценария" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Настраиваемое сочетание клавиш для приостановки сценария  
:::image-end:::  

## Знакомство с расширением кода Microsoft Edge Tools для Visual Studio  

**Элементы для расширений кода Visual Studio** и **Network для Visual Studio** теперь объединяются в новое расширение [кода средств разработчика Microsoft Edge для Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .  Используйте Microsoft Edge DevTools для следующих действий, не выходя из кода Visual Studio.  

*   Отладка модели DOM  
*   Изменение CSS  
*   Проверка сетевого трафика  

С помощью расширения запустите Microsoft EDGE, подключитесь к существующему экземпляру браузера или используйте браузер без монитора прямо из редактора.  Чтобы приступить к откликам и разрешению проблем с отзывом об этом расширении, перейдите к разделу [Инструменты разработчика Microsoft Edge для Visual Studio][GithubMicrosoftVscodeEdgeDevtools] в GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Снимок экрана: использование расширения в полноэкранном режиме браузера" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Снимок экрана: использование расширения в полноэкранном режиме браузера  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Снимок экрана: использование расширения в режиме без монитора" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Снимок экрана: использование расширения в режиме без монитора  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Новое средство WebAuthn  

В более ранних версиях Microsoft EDGE не поддерживалась Отладка с родным WebAuthn.  Необходимы физические средства проверки подлинности для проверки веб-приложения с помощью [API проверки подлинности веб-сайта][GithubW3cWebauthn].  С помощью нового средства **WebAuthn** вы можете выполнять следующие действия без использования каких – либо физических средств проверки подлинности.

*   Эмуляция средств проверки подлинности
*   Настройка атрибутов средств проверки подлинности
*   Проверка состояний средств проверки подлинности
    
Дополнительные сведения о функции **WebAuthn** можно найти в [разделе Эмуляция проверки подлинности и отладка Webauthn в Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Вы можете эмулировать средства проверки подлинности и отлаживать [API проверки подлинности веб-сайта][GithubW3cWebauthn] с помощью нового инструмента [WebAuthn][DevtoolsWebauthnIndex] .  Чтобы открыть средство **WebAuthn** , щелкните значок **Настройка и управление DevTools** \ ( `...` \) > **более средствам**  >  **webauthn**.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Открытие средства WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Открытие средства **WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Средство WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         Средство **WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Обновление инструмента "элементы"  

#### Просмотр области "вычисляемая боковая панель" в области "стили"  

Переключить **вычисляемую** область на панели **стили** .  **Вычисляемая** область в области **стили** свернута по умолчанию.  Чтобы переключить его, нажмите кнопку.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Открытие области "вычисляемая боковая панель"" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Открытие области " **Вычисляемая боковая** панель"  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Вычисляемая область боковой панели" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Вычисляемая область боковой** панели  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Группировка свойств CSS в вычисляемой панели  

Чтобы просмотреть примененную CSS с меньшим прокруткой, сгруппируйте свойства CSS по категориям в **вычисляемой** области.  Вы также можете выбрать набор связанных свойств при проверке CSS.  В инструменте **элементы** выберите элемент.  Чтобы выполнить группировку \ (или разгрупповую) свойства CSS, установите или снимите флажок **Группа** .  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к разделу проблемы [#1096230][CR1096230], [#1084673][CR1084673]и [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Группировка свойств CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Группировка свойств CSS  
:::image-end:::  

### Lighthouse 6,4 в инструменте Lighthouse  

Средство **Lighthouse** теперь запущено Lighthouse 6,4.  Чтобы просмотреть полный список изменений, перейдите к [заметкам о выпуске Lighthouse][GithubGoogleChromeLighthouseReleasesV641].  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#772558][CR772558].  

### события Performance. Mark () в разделе "время показа слайдов"  

**Раздел "временные интервалы** " записи в инструменте " [производительность][DevtoolsGuideChromiumEvaluatePerformanceReference] " теперь отмечает `performance.mark()` события.  Чтобы попробовать эту функцию и оценить производительность кода JavaScript, добавьте `performance.mark()` события в код.  Например, в приведенном ниже фрагменте кода добавляются маркеры до и после `for` цикла, который выполняет итерацию от 0 до 1000 с шагом 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Затем откройте средство " [производительность][DevtoolsGuideChromiumEvaluatePerformanceReference] " и перейдите к **разделу временные показатели** для записи кода JavaScript.  `performance.mark()`Добавленные события будут отображены в записи.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Событие Performance. Mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` событиях  
:::image-end:::  

### Новые фильтры типа ресурсов и URL-адреса в инструменте "сеть"  

Используйте новые `resource-type` `url` Ключевые слова в инструменте " **сеть** " для фильтрации сетевых запросов.  Например, вы можете `resource-type:image` сосредоточиться на сетевых запросах, которые являются изображениями.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Фильтр по типу ресурсов" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   Фильтр по типу ресурсов  
:::image-end:::  

Чтобы найти другие специальные ключевые слова, такие как `resource-type` и `url` , перейдите в [раздел запросы фильтра по свойствам][DevtoolsNetworkReferenceFilterRequestsProperties].  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к разделу проблемы [#1121141][CR1121141] и [#1104188][CR1104188].  

### Обновления представления "сведения о кадрах"  

#### Отображение отчетов COEP и COOP в конечную точку  

`reporting to`В разделе " **изоляция &** " перейдите на вкладку "политика встроенного внедрения" \ (COEP \) и межисточниковая политика OPENER \ (Coop \).  [API отчетов][MdnReportingApi] определяет `Report-To` новый заголовок HTTP, который позволяет указать конечные точки сервера для браузера, чтобы отправлять предупреждения и ошибки.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Отправка сообщения конечной точке" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   `reporting to`Конечная точка  
:::image-end:::  

#### Отображение COEP и COOP режима "только отчет"  

DevTools теперь отобразите `report-only` метку для COEP и Coop, которые установлены в `report-only` режим.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Метка режима «только отчет»" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   `report-only`Метка "режим"  
:::image-end:::  

### Просмотр и устранение проблем с контрастностью цвета в инструменте "Общие сведения о CSS"  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

В инструменте " **Обзор CSS** " теперь отображается список элементов на странице с проблемами цветовой контрастности.  На приведенной ниже демонстрационной странице показан пример ошибки цветовой контрастности.  

[Обзор CSS: демонстрация доступных цветов][GlitchCssOverviewAccessibleColorsDemo]  

Чтобы включить этот эксперимент, в **Settings**разделе  >  **эксперименты**с параметрами установите флажок **CSS Overview (обзор** ).  Чтобы просмотреть список элементов с проблемой цветовой контрастности, в **вопросах контрастности**выберите **текст**.  Чтобы открыть элемент в инструменте **элементы** , выберите элемент в списке.  Для устранения проблем с контрастностью Microsoft Edge DevTools [автоматически предлагают варианты цветов][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Проблемы с низким контрастом цвета" lightbox="../../media/2020/10/css-overview.msft.png":::
   Проблемы с низким контрастом цвета  
:::image-end:::  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Устаревшая область свойств в инструменте "элементы" — новые возможности DevTools (Microsoft Edge 84) | Документы Microsoft"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Функции отладки сетки CSS: новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Специальные возможности цвета в области "стили" — новые возможности DevTools (Microsoft Edge 86) | Документы Microsoft"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript: Справочник по API служебных программ для консоли | Документы Microsoft"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Справка по анализу производительности | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Включите экспериментальные API — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор сочетаний клавиш — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Эмуляция: поддержка двух режимов экрана — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Включить сетевую консоль — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Включение средства просмотра заказов на исходный номер — экспериментальные функции | Документы Microsoft"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Тестирование на складная и устройствах с двумя экранами — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включите экспериментальные функции — экспериментальные функции | Документы Microsoft"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "Справочник по API для консоли "Таблица" | Документы Microsoft"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Проверка сетки CSS | Документы Microsoft"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг" — Справка по анализу производительности | Документы Microsoft"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Просмотр и отладка сведений о проигрывателях мультимедиа | Документы Microsoft"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Эмуляция средств проверки подлинности и отладки WebAuthn в Microsoft Edge DevTools | Документы Microsoft"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительной версии Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Инструменты Microsoft Edge для Visual Studio, код | Код Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: разрешение на настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии Lighthouse | Ошибки Chromium"  
[CR1034663]: https://crbug.com/1034663 "Создание передней части API тестирования WebAuthn | Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "Сетка CSS/гибкая таблица/подсказка для таблиц | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка "вычисляемый стиль" исчезает в режиме отклика | Ошибки Chromium"  
[CR1075732]: https://crbug.com/1075732 "Персонализация DevTools — незакрепленные вкладки | Ошибки Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: Улучшите способ представления настраиваемых свойств CSS ((то есть). Переменные CSS) и их значения | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Инструмент "создать" для создания и воспроизведения запросов виртуальных сетей | Ошибки Chromium"  
[CR1096230]: https://crbug.com/1096230 "Группировка свойств CSS по категориям в области «Вычисляемые стили» | Ошибки Chromium"  
[CR1104188]: https://crbug.com/1104188 "При поиске полного URL-адреса в средстве поиска в сети не удается найти результаты. Ошибки Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: улучшение вкладки "вычисляемые стили" | Ошибки Chromium"  
[CR1120316]: https://crbug.com/1120316 "Выделение неправильной контрастности в разделе Общие сведения о CSS > цвета | Ошибки Chromium"  
[CR1121141]: https://crbug.com/1121141 "Разрешать фильтрацию по типу ресурсов в сетевом журнале | Ошибки Chromium"  
[CR1121312]: https://crbug.com/1121312 "Параметры должны быть удалены из меню "другие инструменты" | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Инструмент "Подсказка" | Ошибки Chromium"  
[CR1136655]: https://crbug.com/1136655 "Devtools: локализация v2 | Ошибки Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API отчетов | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Веб-проверка подлинности | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Здравствуйте! | Цепь"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Опубликовать формат коллекции v 2.1.0 | Опубликовать"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Спецификация OpenAPI | Машин"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/10/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  