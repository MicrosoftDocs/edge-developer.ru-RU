---
description: Улучшения доступности, использование DevTools на других языках и другие.
title: Новые возможности в DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7758b7f8ed55bb766abc56d6dd29ec124617e7ff
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408313"
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
# <a name="whats-new-in-devtools-microsoft-edge-80"></a>Новые возможности в DevTools (Microsoft Edge 80)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.  Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.  Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="accessibility-improvements-to-the-devtools"></a>Улучшения доступности для DevTools  

Команда DevTools внесла 170 изменений в Chromium для решения проблем контрастности цвета, клавиатуры и чтения с экрана в DevTools.  Каждый разработчик, строив веб,должен иметь возможность использовать DevTools.  

:::image type="complex" source="../../images/2019/12/a11y-performance-tool.msft.gif" alt-text="Средство Performance в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана" lightbox="../../images/2019/12/a11y-performance-tool.msft.gif":::
   Средство **Performance** в DevTools с навигацией по клавиатуре и улучшениями чтения с экрана  
:::image-end:::  

Хотите узнать, как сделать веб-страницу доступной для всех пользователей?  Скачайте [сведения о доступности][AccessibilityInsights] и [расширения веб-страниц][WebhintBrowserExtension] для Microsoft Edge, чтобы начать работу.  

Если вы используете считыватели экрана или клавиатуру для [][PostTweetEdgeDevTools] навигации по DevTools, отправьте свои отзывы, направив на нас твиты или отправив значок [Отправка](#getting-in-touch-with-microsoft-edge-devtools-team) отзывов!  

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
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

Перейдите к `edge://flags` флажку **Включить локализованные средства разработчика** и установите **его на включено.**  Кроме того, **установите флаг экспериментов для** средств разработки с **включенной**.  Перезапустите Microsoft Edge и откройте DevTools.  <!-- Select `F1` in the DevTools or navigate to Settings > Experiments and check the **Match browser language** checkbox.  -->  Язык DevTools совпадает с языком, который используется для Microsoft `edge://settings/languages` Edge.  

:::image type="complex" source="../../images/2019/12/localized-devtools.msft.png" alt-text="DevTools на немецком языке" lightbox="../../images/2019/12/localized-devtools.msft.png":::
   DevTools на немецком языке  
:::image-end:::  

Если вы хотите использовать DevTools на другом языке, чем [доступные,][PostTweetEdgeDevTools] отправьте нам сообщение в Twitter или выберите значок [Отправка отзывов.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#941561][CR941561]  

### <a name="webhint-microsoft-edge-extension"></a>webhint Microsoft Edge extension  

Расширение Microsoft Edge позволяет легко сканировать веб-страницу и получать отзывы о доступности, совместимости браузера, безопасности, производительности и других данных в DevTools.  Дополнительные публикации [https://webhint.io][Webhint] в .  

:::image type="complex" source="../../images/2019/12/webhint-browser-extension.msft.png" alt-text="Средство Подсказки в DevTools при установке расширения веб-браузера" lightbox="../../images/2019/12/webhint-browser-extension.msft.png":::
   Средство **Подсказки** в DevTools при установке расширения веб-браузера  
:::image-end:::  

[Попробуйте расширение веб-браузера в Microsoft Edge][MicrosoftEdgeInsiderAddons].  После установки расширения откройте DevTools и выберите **средство Hints.**  Отсюда запустите настраиваемую проверку сайта.  [Переехав в webhint.io,][WebhintBrowserExtension] чтобы узнать больше.

### <a name="3d-view"></a>Трехмерное представление  

Использование **3D-представления** для отлаживания веб-приложения путем навигации по объектной модели документа [\(DOM\)][MDNDocumentObjectModel] или контексту укладки [индекса z.][MDNZIndex]  

:::image type="complex" source="../../images/2019/12/3dview.msft.png" alt-text="3D-представление в DevTools" lightbox="../../images/2019/12/3dview.msft.png":::
   **3D-представление** в DevTools  
:::image-end:::  

Чтобы получить доступ к 3D-представлению, перейдите по флажку Эксперименты для разработчиков и убедитесь, что флаг экспериментов для разработчиков `edge://flags` задает **включено.** ****  Перезапустите Microsoft Edge и откройте DevTools.  Выберите `F1` в разделе DevTools или откройте раздел **Параметры**Эксперименты и включим контрольный ящик  >  **** Enable **3D View.**  Теперь выберите `Ctrl`  +  `Shift`  +  `P` , введите **в 3D-представлении** и **выберите Показать 3D-представление**.  

Мы работаем над пользовательским интерфейсом и добавляем дополнительные функциональные возможности в 3D View, поэтому отправьте нам свои [отзывы.](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#987787][CR987787]

### <a name="visual-studio-code-extensions"></a>Visual Studio расширения кода  

Команда DevTools также выпустила некоторые расширения для кода [Visual Studio,][VisualStudioCode] которые могут использовать силу DevTools непосредственно из текстового редактора. Ознакомьтесь со следующими расширениями.  

#### <a name="elements-for-microsoft-edge"></a>Элементы для Microsoft Edge  

Используйте средство Elements из Visual Studio кода, добавив элементы для [Microsoft Edge (Chromium)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] Visual Studio кода.  

:::image type="complex" source="../../images/2019/12/elements-for-edge.msft.png" alt-text="Средство Elements в Visual Studio с помощью расширения Elements for Microsoft Edge" lightbox="../../images/2019/12/elements-for-edge.msft.png":::
   Средство **Elements** в Visual Studio с помощью расширения Elements for Microsoft Edge  
:::image-end:::  

Дополнительные сведения вы можете получить в [службе Elements for Microsoft Edge Visual Studio кода.][VisualStudioCodeElementEdgeExtension]  

#### <a name="debugger-for-microsoft-edge"></a>Отладка для Microsoft Edge  

С [расширением кода Debugger для Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] Visual Studio отладка JavaScript, запущенная в Microsoft Edge непосредственно из Visual Studio Code.  

:::image type="complex" source="../../images/2019/12/vscode-debugger.msft.png" alt-text="Отладка для расширения Microsoft Edge в Visual Studio коде" lightbox="../../images/2019/12/vscode-debugger.msft.png":::
   Отладка для расширения Microsoft Edge в Visual Studio коде  
:::image-end:::  

Дополнительные сведения о том, как отчудировать Microsoft Edge от [Visual Studio Code.][VisualStudioCodeDebuggerEdgeExtension]  

#### <a name="webhint"></a>webhint  

Расширение [веб-Visual Studio][VisualStudioMarketplaceWebhintExtension] кода используется для улучшения веб-страницы во время `webhint` ее записи! Это расширение запускает и сообщает диагностику в файлах рабочего пространства на основе `webhint` анализа.  

:::image type="complex" source="../../images/2019/12/webhint-vscode-extension.msft.png" alt-text="Веб-Visual Studio кода, анализируя файл tsx в Visual Studio Code" lightbox="../../images/2019/12/webhint-vscode-extension.msft.png":::
   Веб-Visual Studio кода, анализируя `.tsx` файл в Visual Studio Code  
:::image-end:::  

[Узнайте больше о расширении веб-Visual Studio code.][WebhintVisualStudioCodeExtension]  

### <a name="visual-studio-integration"></a>Visual Studio интеграции  

В Visual Studio 2019 версии 16.2 или более поздней версии Visual Studio отладка JavaScript, запущенного в Microsoft Edge.  [Скачайте Visual Studio 2019,][MicrosoftVisualStudioDownloads] чтобы попробовать эту функцию.  

:::image type="complex" source="../../images/2019/12/vs.msft.png" alt-text="Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta" lightbox="../../images/2019/12/vs.msft.png":::
   Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Beta  
:::image-end:::  

[Ознакомьтесь с нашим сообщением][MicrosoftVisualStudioBlogDebugJavascript]в блоге, чтобы узнать, как отламыть Microsoft Edge из Visual Studio .  

### <a name="tracking-prevention-console-messages"></a>Отслеживание сообщений консоли предотвращения  

Отслеживание предотвращения — это уникальная функция в Microsoft Edge, которая блокирует отслеживание веб-сайта перед его посещением.  Параметр предотвращения отслеживания по умолчанию — это режим Balanced, который блокирует сторонние трекеры и известные вредоносные трекеры для обеспечения баланса конфиденциальности и совместимости с веб-сайтом.  Чтобы получить больше информации о совместимости веб-страницы при блокировке определенных трекеров, группа **** Microsoft Edge добавила предупреждающие сообщения в консоли при блокировке трекера.  

:::image type="complex" source="../../images/2019/12/tracking-prevention.msft.png" alt-text="Сообщения в консоли при отслеживании предотвращения блокирования доступа к хранилищам для трекера" lightbox="../../images/2019/12/tracking-prevention.msft.png":::
   Сообщения в консоли при **отслеживании** предотвращения блокирования доступа к хранилищам для трекера  
:::image-end:::  

[Дополнительные данные о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 80, которые были внесены в проект Chromium с открытым исходным кодом.  

### <a name="support-for-let-and-class-redeclarations-in-the-console"></a>Поддержка переделокации допустимого и классового класса в консоли  

Консоль **теперь** поддерживает переделки `let` и `class` утверждения.  Неумелость к переописыванию была обычным раздражением для веб-разработчиков, которые используют консоль для экспериментов с новым кодом JavaScript.  

> [!WARNING]
> Переоценка или утверждение в скрипте за пределами консоли или в одной консоли ввода `let` `class` по-прежнему вызывает `SyntaxError` .  

Например, ранее при повторном объявлении локальной переменной с `let` консолью была допущена ошибка:  

:::image type="complex" source="../../images/2019/12/letbefore.msft.png" alt-text="Консоль в Microsoft Edge 79, показывающая, что переделокация не удается" lightbox="../../images/2019/12/letbefore.msft.png":::
   Консоль **в** Microsoft Edge 79, показывающая, что повторное объявление не удается  
:::image-end:::  

Теперь консоль позволяет переоцирять:  

:::image type="complex" source="../../images/2019/12/letafter.msft.png" alt-text="Консоль в Microsoft Edge 80 с указанием успешности переделокации" lightbox="../../images/2019/12/letafter.msft.png":::
   Консоль **в** Microsoft Edge 80 с указанием успешности повторного декларирования  
:::image-end:::  

Проблема Chromium [#1004193][CR1004193]  

### <a name="improved-webassembly-debugging"></a>Улучшенная отладка webAssembly  

DevTools начала поддерживать стандарт отладки [DWARF,][DwarfHome]что означает повышенную поддержку для перешагровки кода, установки точек разрыва и устранения следов стека на исходных языках в DevTools.  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
:::image type="complex" source="../../images/2019/12/wasm.msft.png" alt-text="The new DWARF-powered WebAssembly debugging" lightbox="../../images/2019/12/wasm.msft.png":::
   The new DWARF-powered WebAssembly debugging  
:::image-end:::  
-->  

### <a name="network-panel-updates"></a>Обновления сетевых панелей  

#### <a name="request-initiator-chains-in-the-initiator-panel"></a>Запрос Цепочек инициаторов в панели Инициатор  

Теперь вы можете просматривать инициаторов и зависимостей сетевого запроса как вложенный список.  Это может помочь вам понять, почему был запротесрен ресурс или какая деятельность сети вызвана определенным ресурсом \(например, скрипт\).  

:::image type="complex" source="../../images/2019/12/initiators.msft.png" alt-text="Цепочка инициаторов запроса в панели Инициатор" lightbox="../../images/2019/12/initiators.msft.png":::
   Цепочка инициаторов запроса в **панели Инициатор**  
:::image-end:::  

После [ведения журнала сетевой активности][DevToolsNetworkIndex]в панели Network выберите **** ресурс, а затем перейдите на панель Инициатора, чтобы просмотреть цепочку инициатора **запроса:**  

*   **Проинспектировали ресурс** является смелым.  На скриншоте выше `ai.2.min.js` — проверенный ресурс.  
*   Ресурсы, которые находятся выше проверенного ресурса, являются **инициаторами.**  На скриншоте `https://www.microsoftedgeinsider.com` выше, является инициатором `ai.2.min.js` .  Другими словами, `https://www.microsoftedgeinsider.com` вызвал запрос сети для `ai.2.min.js` .  
*   Ресурсы ниже проверенного ресурса — **это зависимости.**  На скриншоте `https://dc.services.visualstudio.com/v2/track` выше— зависимость `ai.2.min.js` от .  Другими словами, `ai.2.min.js` вызвал запрос сети для `https://dc.services.visualstudio.com/v2/track` .  

> [!NOTE]
> Сведения о инициаторе и зависимостей также могут быть доступны путем удержания и нависания над `Shift` сетевыми ресурсами.  Перейдите к [просмотру инициаторов и зависимостей.][DevToolsNetworkReferenceViewInitiatorsDependencies]  

Проблема Chromium [#842488][CR842488]  

#### <a name="highlight-the-selected-network-request-in-the-overview"></a>Выделение выбранного сетевого запроса в Обзоре  

После выбора сетевого ресурса для его проверки панель Network теперь помещает синюю границу вокруг этого ресурса в **Обзоре.**  Это поможет вам определить, происходит ли запрос сети раньше или позже, чем ожидалось.  

:::image type="complex" source="../../images/2019/12/overview.msft.png" alt-text="Области Обзор выделения проверенного ресурса" lightbox="../../images/2019/12/overview.msft.png":::
   Области **Обзор** выделения проверенного ресурса  
:::image-end:::  

Проблема Chromium [#988253][CR988253]  

#### <a name="url-and-path-columns-in-the-network-panel"></a>СТОЛБЦЫ URL-адресов и путей в панели Network  

Используйте новые **столбцы Path** и **URL-адрес** в средстве **Network** для отображения абсолютного пути или полного URL-адреса каждого сетевого ресурса.  

:::image type="complex" source="../../images/2019/12/columns.msft.png" alt-text="Новые столбцы Path и URL-адресов в панели Network" lightbox="../../images/2019/12/columns.msft.png":::
   Новые столбцы Path и URL-адрес в **средстве Network**  
:::image-end:::  

Чтобы отобразить новые столбцы, наведите курсор на загон таблицы **Водопад,** откройте контекстное меню \(righ-click\) и выберите **Путь** или **URL-адрес.**  

Проблема Chromium [#993366][CR993366]  

#### <a name="updated-user-agent-strings"></a>Обновленные User-Agent строки  

DevTools поддерживает настройку настраиваемой строки User-Agent через панель **сетевых условий.**  Строка User-Agent влияет на `User-Agent` заглавную строку HTTP, присоединенную к сетевым ресурсам, а также значение `navigator.userAgent` .  

Предопределяющие User-Agent строки были обновлены, чтобы отражать современные версии браузера.  

:::image type="complex" source="../../images/2019/12/useragent.msft.png" alt-text="Меню Агента пользователя в панели сетевых условий" lightbox="../../images/2019/12/useragent.msft.png":::
   Меню Агента пользователя в панели **сетевых условий**  
:::image-end:::  

Чтобы получить **доступ к сетевым** [условиям, откройте командное меню][DevToolsCommandMenuIndex] и запустите `Show Network Conditions` команду.  

> [!NOTE]
> Вы также можете [User-Agent строки в режиме устройства.][DevToolsDeviceModeIndex]  

Проблема Chromium [#1029031][CR1029031]  

### <a name="audits-panel-updates"></a>Аудит обновлений панелей  

#### <a name="new-configuration-ui"></a>Новый пользовательский интерфейс конфигурации  

Пользовательский интерфейс конфигурации имеет новый, отзывчивый дизайн, а параметры настройки регулирования были упрощены.  Дополнительные сведения об изменениях пользовательского интерфейса регулирования см. в окне Регулирование панели [аудитов.][GitHubGoogleChromeDevToolsAuditsPanelThrottling]  

:::image type="complex" source="../../images/2019/12/start.msft.png" alt-text="Новый пользовательский интерфейс конфигурации" lightbox="../../images/2019/12/start.msft.png":::
   Новый пользовательский интерфейс конфигурации  
:::image-end:::  

### <a name="coverage-tool-updates"></a>Обновления средства покрытия  

#### <a name="per-function-or-per-block-coverage-modes"></a>Режимы покрытия на одну функцию или на блок  

Средство [Coverage][DevToolsCoverageIndex] имеет новое меню выпадения, которое позволяет указать, следует ли собирать данные о покрытии кода на одну функцию **или** **на блок.**  **Покрытие каждого блока** является более подробным, но и гораздо более дорогостоящим в сборе.  DevTools использует **по умолчанию покрытие** функций по умолчанию.  

> [!CAUTION]
> Вы можете заметить большие различия в охвате кода в HTML-файлах в зависимости от того, используете ли вы одну функцию **или** **режим блокировки.**  При использовании **режима функции** встроенные скрипты в HTML-файлах рассматриваются как функции.  Если сценарий работает вообще, то DevTools отмечает весь скрипт как используемый код.  Только если сценарий вообще не работает, DevTools пометит сценарий как неиспользимый код.  

:::image type="complex" source="../../images/2019/12/modes.msft.png" alt-text="Меню отсев в режиме покрытия" lightbox="../../images/2019/12/modes.msft.png":::
   Меню отсев в режиме покрытия  
:::image-end:::  

#### <a name="coverage-must-now-be-initiated-by-a-page-refresh"></a>Теперь охват должен быть инициирован обновлением страницы  

Переналадка покрытия кода без обновления страницы была удалена из-за недостоверности данных об охвате.  Например, функция может быть неиспользована, если время запуска было давно, и сборщик мусора V8 убрал ее.  

Проблема Chromium [#1004203][CR1004203]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

<!--[../../images/2019/12/wasm.msft.png]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Найдите неиспользванный код JavaScript и CSS с помощью средства Coverage в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index#simulate-a-mobile-viewport "Имитация мобильного представления — имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsNetworkIndex]: /microsoft-edge/devtools-guide-chromium/network/index "Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#view-initiators-and-dependencies "Просмотр инициаторов и зависимостей — справочник по сетевому анализу | Документы Майкрософт"  
[DevGuideEdgeHtmlWhatsNew]: /microsoft-edge/dev-guide/whats-new "Новые возможности в edgeHTML | Документы Майкрософт"  
[VisualStudioCodeDebuggerEdgeExtension]: /microsoft-edge/visual-studio-code/debugger-for-edge "Отладка для расширения Visual Studio Microsoft Edge | Документы Майкрософт"  
[VisualStudioCodeElementEdgeExtension]: /microsoft-edge/visual-studio-code/elements-for-edge "Элементы для расширения Visual Studio Microsoft Edge | Документы Майкрософт"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[CR842488]: https://crbug.com/842488 "Добавьте поле Инициатор в вкладку Headers | Chromium Bugs"  
[CR988253]: https://crbug.com/988253 "Ошибка DevTools — отсутствие связи между сетевым запросом и графиком | Chromium Bugs"  
[CR993366]: https://crbug.com/993366 "Пожалуйста, покажите часть пути URL-адреса в списке запросов сетевых панелей | Chromium Bugs"  
[CR1004193]: https://crbug.com/1004193 "Режим REPL для V8 | Chromium Bugs"  
[CR1004203]: https://crbug.com/1004203 "Сделайте покрытие кода потрясающим | Chromium Bugs"  
[CR1029031]: https://crbug.com/1029031 "Строки UA устарели | Chromium Bugs" 
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Chromium Bugs"
[CR941561]: https://crbug.com/941561 "Локализуемость | Chromium Bugs"
[CR987787]: https://crbug.com/987787 "Dom 3D View | Chromium Bugs"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о доступности"  

[DwarfHome]: https://dwarfstd.org "Карлик Главная"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Регулирование аудита DevTools — GoogleChrome/lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки инсайдеров Microsoft Edge"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отламыв JavaScript в Microsoft Edge из Visual Studio | Visual Studio блог"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \& Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документа (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio Код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) - Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузера веб-| документация по веб-сайтам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Webhint Visual Studio расширение кода | документация по веб-сайтам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение предотвращения отслеживания в блоге Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/updates/2019/12/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
