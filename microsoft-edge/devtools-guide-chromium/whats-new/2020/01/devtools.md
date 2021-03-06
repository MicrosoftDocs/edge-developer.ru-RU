---
description: 3D View, Visual Studio интеграция с Microsoft Edge и другие.
title: Новые возможности в DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a60be4d55d7f6152ed7ce7afd24049f0f5909a4b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398247"
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

# <a name="whats-new-in-devtools-microsoft-edge-81"></a>Что нового в DevTools (Microsoft Edge 81)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.  Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.  Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="accessibility-improvements-to-the-devtools"></a>Улучшения доступности для DevTools  

Команда DevTools внесла 170 изменений в Chromium для решения проблем контрастности цвета, клавиатуры и чтения с экрана в DevTools.  Каждый разработчик, строив веб,должен иметь возможность использовать DevTools.  

:::image type="complex" source="../../images/2020/01/a11y-performance-tool.msft.gif" alt-text="Средство Performance в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана" lightbox="../../images/2020/01/a11y-performance-tool.msft.gif":::
   Средство **Performance** в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана  
:::image-end:::  

Хотите узнать, как сделать веб-страницу доступной для всех пользователей?  Скачайте [сведения о доступности][AccessibilityInsights] и [расширения веб-страниц][WebhintBrowserExtension] для Microsoft Edge, чтобы начать работу.  

Если вы используете считыватели экрана или клавиатуру для навигации по DevTools, отправьте нам свои отзывы, направив на нас твиты или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team) [][PostTweetEdgeDevTools]  

Проблема Chromium [#963183][CR963183]  

### <a name="using-the-devtools-in-other-languages"></a>Использование DevTools на других языках  

Многие разработчики используют другие средства разработчика, такие как StackOverflow и Visual Studio Code, на родном языке, а не только на английском языке.  Мы рады сообщить о локализации для DevTools, которые теперь можно использовать на одном из 10 языков, кроме английского:  

:::row:::
   :::column span="":::
      Китайский \(Упрощенный\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Китайский \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Французский —&#231;ais
   :::column-end:::
   :::column span="":::
      Немецкий - deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Итальянский - italiano
   :::column-end:::
   :::column span="":::
      Японский - &#26085;&#26412;&#35486;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Корейский - &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Португальский — portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Русский  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Испанский язык — espa&#241;ol
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

DevTools автоматически совпадают с языком, который используется для Microsoft `edge://settings/languages` Edge.  

Если вы хотите, чтобы Microsoft Edge был на одном языке, а ваши devTools оставались на английском языке, выберите в DevTools, чтобы открыть параметры и отключить язык браузера `F1` **Match.** [][Settings]  

:::image type="complex" source="../../images/2020/01/localized-devtools.msft.png" alt-text="DevTools на немецком языке" lightbox="../../images/2020/01/localized-devtools.msft.png":::
   DevTools на немецком языке  
:::image-end:::  

**Сообщения** консоли не локализованы.  Только строки, используемые в пользовательском интерфейсе DevTools, отображаются на языке, используемом для Microsoft Edge.  

Если вы хотите использовать DevTools на другом языке, чем [доступные,][PostTweetEdgeDevTools] отправьте нам сообщение в Twitter или выберите значок [Отправка отзывов.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>webhint Microsoft Edge extension  

Расширение Microsoft Edge позволяет легко сканировать веб-страницу и получать отзывы о доступности, совместимости браузера, безопасности, производительности и других данных в DevTools.  Дополнительные публикации [https://webhint.io][Webhint] в .  

:::image type="complex" source="../../images/2020/01/webhint-browser-extension.msft.png" alt-text="Средство Подсказки в DevTools при установке расширения веб-браузера" lightbox="../../images/2020/01/webhint-browser-extension.msft.png":::
   Средство **Подсказки** в DevTools при установке расширения веб-браузера  
:::image-end:::  

[Попробуйте расширение веб-браузера в Microsoft Edge][MicrosoftEdgeInsiderAddons].  После установки расширения откройте DevTools и выберите **средство Hints.**  Отсюда запустите настраиваемую проверку сайта.  [Переехав в webhint.io,][WebhintBrowserExtension] чтобы узнать больше.  

### <a name="3d-view"></a>Трехмерное представление  

Использование **3D-представления** для отлаживания веб-приложения путем навигации по объектной модели документа [\(DOM\)][MDNDocumentObjectModel] или контексту укладки [индекса z.][MDNZIndex]  

:::image type="complex" source="../../images/2020/01/3dview.msft.png" alt-text="3D-представление в DevTools" lightbox="../../images/2020/01/3dview.msft.png":::
   3D-представление в DevTools  
:::image-end:::  

Чтобы получить доступ к 3D-представлению, выберите `Ctrl`  +  `Shift`  +  `P` , введите **в 3D-представлении** и выберите **Показать 3D View**.  

Команда Microsoft Edge работает с командой Chromium в пользовательском интерфейсе и добавляет дополнительные функциональные возможности для 3D-представления, поэтому отправьте свои [отзывы.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#987787][CR987787]  

### <a name="visual-studio-code-extensions"></a>Visual Studio расширения кода  

Команда DevTools также выпустила некоторые расширения для [кода Visual Studio,][VisualStudioCode] которые могут использовать силу DevTools непосредственно из текстового редактора! Ознакомьтесь с расширениями ниже:  

#### <a name="elements-for-microsoft-edge"></a>Элементы для Microsoft Edge  

Используйте средство Elements из Visual Studio кода, добавив элементы для [Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio кода.  

:::image type="complex" source="../../images/2020/01/elements-for-edge.msft.png" alt-text="Средство Elements в Visual Studio с помощью расширения Elements for Microsoft Edge" lightbox="../../images/2020/01/elements-for-edge.msft.png":::
   Средство **Elements** в Visual Studio с помощью расширения Elements for Microsoft Edge  
:::image-end:::  

Дополнительные сведения вы можете получить в [службе Elements for Microsoft Edge Visual Studio кода.][VisualStudioCodeElementEdgeExtension]  

#### <a name="debugger-for-microsoft-edge"></a>Отладка для Microsoft Edge  

С [расширением кода Debugger для Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio отладка JavaScript, запущенная в Microsoft Edge непосредственно из Visual Studio Code.  

:::image type="complex" source="../../images/2020/01/vscode-debugger.msft.png" alt-text="Отладка для расширения Microsoft Edge в Visual Studio коде" lightbox="../../images/2020/01/vscode-debugger.msft.png":::
   Отладка для расширения Microsoft Edge в Visual Studio коде  
:::image-end:::  

Дополнительные сведения о том, как отчудировать Microsoft Edge от [Visual Studio Code.][VisualStudioCodeDebuggerEdgeExtension]  

#### <a name="webhint"></a>webhint  

Расширение [веб-Visual Studio][VisualStudioMarketplaceWebhintExtension] кода используется для улучшения `webhint` веб-страницы во время ее написания.  Это расширение запускает и сообщает диагностику в файлах рабочего пространства на основе `webhint` анализа.  

:::image type="complex" source="../../images/2020/01/webhint-vscode-extension.msft.png" alt-text="Веб-Visual Studio кода, анализируя файл tsx в Visual Studio Code" lightbox="../../images/2020/01/webhint-vscode-extension.msft.png":::
   Веб-Visual Studio кода, анализируя `.tsx` файл в Visual Studio Code  
:::image-end:::  

[Узнайте больше о расширении веб-Visual Studio code.][WebhintVisualStudioCodeExtension]  

### <a name="visual-studio-integration"></a>Visual Studio интеграции  

В Visual Studio 2019 версии 16.2 или более поздней версии Visual Studio отладка JavaScript, запущенного в Microsoft Edge.  [Скачайте Visual Studio 2019,][MicrosoftVisualStudioDownloads] чтобы попробовать эту функцию!  

:::image type="complex" source="../../images/2020/01/vs.msft.png" alt-text="Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta" lightbox="../../images/2020/01/vs.msft.png":::
   Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta  
:::image-end:::  

[Узнайте больше о отладке Microsoft Edge][MicrosoftVisualStudio]из Visual Studio.  

### <a name="tracking-prevention-console-messages"></a>Отслеживание сообщений консоли предотвращения  

Отслеживание предотвращения — это уникальная функция в Microsoft Edge, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещали.  Параметр предотвращения отслеживания по умолчанию — это режим Balanced, который блокирует сторонние трекеры и известные вредоносные трекеры для обеспечения баланса конфиденциальности и совместимости с веб-сайтом.  Чтобы получить больше информации о совместимости веб-страницы при блокировке определенных трекеров, **** в консоль добавлялись предупреждающие сообщения, когда трекер заблокирован.  

:::image type="complex" source="../../images/2020/01/tracking-prevention.msft.png" alt-text="Сообщения в консоли при отслеживании предотвращения блокирования доступа к хранилищам для трекера" lightbox="../../images/2020/01/tracking-prevention.msft.png":::
   Сообщения в консоли при **отслеживании** предотвращения блокирования доступа к хранилищам для трекера  
:::image-end:::  

[Дополнительные данные о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 81, которые были внесены в проект Chromium с открытым исходным кодом.  

### <a name="moto-g4-support-in-device-mode"></a>Поддержка Moto G4 в режиме устройства  

После [включения панели инструментов устройства][DeviceToolbar]смоделировать размеры представления Moto G4 из списка **Устройств.**  

:::image type="complex" source="../../images/2020/01/motog4.msft.png" alt-text="Моделирование представления Moto G4" lightbox="../../images/2020/01/motog4.msft.png":::
   Моделирование представления Moto G4  
:::image-end:::  

Выберите [показать кадр устройства,][DeviceFrame] чтобы показать оборудование Moto G4 вокруг представления.  

:::image type="complex" source="../../images/2020/01/motog4frame.msft.png" alt-text="Отображение оборудования Moto G4" lightbox="../../images/2020/01/motog4frame.msft.png":::
   Отображение оборудования Moto G4  
:::image-end:::  

Связанные функции:  

*   Откройте [командное меню][CommandMenu] и запустите команду, чтобы сделать снимок экрана представления, включающее оборудование `Capture screenshot` Moto G4 (после включения **show Device Frame).**  
*   [Перекрой сеть и ЦП,][ThrottleNetworkAndCpu] чтобы более точно имитировать условия просмотра веб-страниц мобильного пользователя.  

Проблема Chromium [#924693][CR924693]  

### <a name="cookie-related-updates"></a>Обновления, связанные с cookie  

#### <a name="blocked-cookies-in-the-cookies-pane"></a>Заблокированные файлы cookie в области cookie  

В области cookies на панели Приложения теперь отображаются заблокированные файлы cookie с желтым фоном.  

:::image type="complex" source="../../images/2020/01/blockedcookies.msft.png" alt-text="Заблокированные файлы cookie в области cookies панели Приложения" lightbox="../../images/2020/01/blockedcookies.msft.png":::
   Заблокированные файлы cookie в области cookies панели Приложения  
:::image-end:::  

Проблема Chromium [#1030258][CR1030258]  <!-- inaccessible  -->  

#### <a name="cookie-priority-in-the-cookie-pane"></a>Приоритет cookie в области Cookie  

Таблицы cookies в **** **средствах сети** и приложений теперь включают **столбец Priority.**  

> [!CAUTION]
> Браузеры на основе хрома, такие как Microsoft Edge, являются единственными браузерами, которые поддерживают приоритет cookie.  

Проблема Chromium [#1026879][CR1026879]  

#### <a name="edit-all-cookie-values"></a>Изменение всех значений cookie  

Все ячейки в таблицах Cookie теперь можно изменить, за исключением ячеек в столбце **Размер,** так как этот столбец представляет размер сети cookie в bytes.  Для объяснения каждого столбца перейдите к [Полям][CookiesFields].  

:::image type="complex" source="../../images/2020/01/editcookie.msft.png" alt-text="Редактирование значения cookie" lightbox="../../images/2020/01/editcookie.msft.png":::
   Редактирование значения cookie  
:::image-end:::  

#### <a name="copy-as-nodejs-fetch-to-include-cookie-data"></a>Скопируйте Node.js, чтобы включить данные cookie  

Чтобы получить выражение, которое включает данные cookie, наведите курсор на сетевой запрос, откройте контекстное меню \(правой кнопкой мыши\) и выберите копию копии в качестве `fetch` ****  >  **Node.js.**  

:::image type="complex" source="../../images/2020/01/fetchcookies.msft.png" alt-text="Скопируйте как Node.js извлечение" lightbox="../../images/2020/01/fetchcookies.msft.png":::
   Скопируйте как Node.js извлечение  
:::image-end:::  

Проблема Chromium [#1029826][CR1029826]  

### <a name="more-accurate-web-app-manifest-icons"></a>Более точные значки манифеста веб-приложения  

Ранее панель Манифеста в панели Приложений отправляла собственные запросы для отображения значков манифеста веб-приложений.  В DevTools теперь показан точно такой же значок манифеста, который использует Microsoft Edge.  

:::image type="complex" source="../../images/2020/01/manifesticons.msft.png" alt-text="Значки в области Манифест" lightbox="../../images/2020/01/manifesticons.msft.png":::
   Значки в области Манифест  
:::image-end:::  

Проблема Chromium [#985402][CR985402]  

### <a name="hover-on-css-content-properties-to-display-unescaped-values"></a>Наведите курсор на свойства контента CSS для отображения неоконченных значений  

Наведите курсор на значение свойства, чтобы `content` отобразить неоконченную версию значения.  

Например, в этой [демонстрации][CSSContentDemo] при проверке псевдоэлемента в области Стилей отображается сбежавая `p::after` строка: ****  

:::image type="complex" source="../../images/2020/01/escapedstring.msft.png" alt-text="Сбежавая строка" lightbox="../../images/2020/01/escapedstring.msft.png":::
   Сбежавая строка  
:::image-end:::  

При наведении на значение отображается `content` неоконченная величина.  

:::image type="complex" source="../../images/2020/01/unescapedstring.msft.png" alt-text="Неоконченные значения" lightbox="../../images/2020/01/unescapedstring.msft.png":::
   Неоконченные значения  
:::image-end:::  

### <a name="more-detailed-source-map-errors-in-the-console"></a>Более подробные ошибки исходных карт в консоли  

Консоль теперь содержит более подробные данные о том, почему не удалось загрузить или размыть исходные карты.  Ранее он просто предоставил ошибку, не объясняя, что пошло не так.  

:::image type="complex" source="../../images/2020/01/sourcemap.msft.png" alt-text="Ошибка загрузки исходных карт в консоли" lightbox="../../images/2020/01/sourcemap.msft.png":::
   Ошибка загрузки исходных карт в консоли  
:::image-end:::  

### <a name="setting-for-disabling-scrolling-past-the-end-of-a-file"></a>Параметр отключения прокрутки в конце файла  

Откройте [параметры,][Settings] а **** затем отключите источники предпочтений, позволяющие прокручивать последний конец файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, которое позволяет прокручиваться хорошо, минуя конец файла в панели  >  ****  >  **** **Источников.**  

:::image type="complex" source="../../images/2020/01/settings.msft.png" alt-text="Отключение Разрешить прокрутку последнего конца файла" lightbox="../../images/2020/01/settings.msft.png":::
   **Отключение Разрешить прокрутку последнего конца файла в** параметрах  
:::image-end:::  

:::image type="complex" source="../../images/2020/01/scrollingsources.msft.png" alt-text="Прокрутка в конце файла теперь отключена в панели Источники" lightbox="../../images/2020/01/scrollingsources.msft.png":::
   Прокрутка в конце файла теперь отключена в панели Источники  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DeviceToolbar]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"
[DeviceFrame]: /microsoft-edge/devtools-guide-chromium/device-mode/index#show-device-frame "Показать кадр устройства — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"
[CommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[ThrottleNetworkAndCpu]: /microsoft-edge/devtools-guide-chromium/device-mode/index#throttle-the-network-and-cpu "Throttle сети и ЦП - Имитация мобильных устройств с режимом устройства в Microsoft Edge DevTools | Документы Майкрософт"
[Settings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"
[MicrosoftVisualStudio]: /microsoft-edge/visual-studio/index "Visual Studio | Документы Майкрософт"  
[CookiesFields]: /microsoft-edge/devtools-guide-chromium/storage/cookies#fields "Поля — просмотр, редактирование и удаление файлов cookie с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладка для расширения Visual Studio Microsoft Edge"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы для расширения кода Microsoft Edge Visual Studio microsoft Edge"  

[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"

[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение предотвращения отслеживания в блоге Microsoft Edge"

[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки инсайдеров Microsoft Edge"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Загрузка Visual Studio 2019 г. для Windows & Mac"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  

[CR924693]: https://crbug.com/924693 "Запрос на функции. Добавьте Moto G4 в список режимов устройств | Chromium Bugs"  
[CR1030258]: https://crbug.com/1030258 "CR 1030258 | Chromium Bugs"  
[CR1026879]: https://crbug.com/1026879 "Вкладка Cookie в консоли разработчиков больше не показывает приоритета | Chromium Bugs"  
[CR1029826]: https://crbug.com/1029826 "сетевой вкладка -> правильно выбрать для запроса -> -> копию, так как извлечение не копирует файлы cookie | Chromium Bugs"  
[CR985402]: https://crbug.com/985402 "Строки ошибки манифеста веб-приложения сбивают с толку | Chromium Bugs"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Chromium Bugs"  
[CR941561]: https://crbug.com/941561 "Локализуемость | Chromium Bugs"  
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"  

[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для неоконченного контента CSS"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  

[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"  
[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о доступности"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документа (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  

[Webhint]: https://aka.ms/webhint "webhint"  

[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузера веб-| документация по веб-сайтам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio расширение кода | документация по веб-сайтам"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/updates/2020/01/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  