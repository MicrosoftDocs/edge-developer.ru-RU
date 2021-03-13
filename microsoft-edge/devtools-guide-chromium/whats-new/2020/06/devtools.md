---
description: Функции отладки сетки CSS, запросы на редактирование и воспроизведение с сетевой консоли и другие.
title: Новые возможности в DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9031f817a6079f64352c261a70eb9581213bf8c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408320"
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
# <a name="whats-new-in-devtools-microsoft-edge-85"></a>Что нового в DevTools (Microsoft Edge 85)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.  Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.  Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте команде Microsoft [Edge DevTools в Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="css-grid-debugging-features"></a>Функции отладки сетки CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Команда Microsoft Edge DevTools сотрудничает с командой Chrome DevTools и сообществом Chromium, чтобы добавить новые функции отладки сетки CSS в DevTools.  Теперь вы можете отображать номера линий сетки, пробелы в сетке и расширенные строки сетки в качестве наложения на страницу.  Кроме того, в ближайшее время будут усовершенствования средств сетки.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Функции отладки сетки CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Функции отладки сетки CSS
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, [][DevtoolsExperimentalFeaturesTurnOn] перейдите к экспериментальным функциям и выберите почтовый ящик рядом с включить новые функции отладки **CSS Grid.**  
> 
> Чтобы попробовать эксперимент с образцом, перейдите к [примеру планировщика сетки CSS.][CodepenRachelweilYzwBzKM]  

Проблема Chromium [#1047356][CR1047356]  

### <a name="edit-and-replay-requests-with-the-network-console"></a>Редактирование и воспроизведение запросов с помощью сетевой консоли  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Теперь вы можете использовать **редактирование** и воспроизведение запросов в сетевом журнале [с][DevtoolsNetworkIndexLogActivity] помощью **сетевой консоли.**  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Редактирование и воспроизведение запроса в NetworkLog с помощью сетевой консоли" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Редактирование и воспроизведение запроса в [NetworkLog][DevtoolsNetworkIndexLogActivity] с помощью **сетевой консоли**  
:::image-end:::  

Новая панель сетевой консоли открывается в [ящике DevTools][DevtoolsCustomizeIndexDrawer] и автоматически заполняется информацией для запроса HTTP. ****  Чтобы отобразить ответ, возвращаемый с сервера, отредактировать запрос \(если это необходимо\) и выберите **Отправить**.  

Можно также использовать **сетевой консоли** для создания и отправки http-запросов непосредственно из DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Панель сетевой консоли" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Панель **сетевой консоли**  
:::image-end:::  

> [!TIP]
> Чтобы **отобразить** консоль Сети в главной панели \(top\) вместо [ящика DevTools,][DevtoolsCustomizeIndexDrawer]перейдите к перемещая [средствам между панелями.](#move-tools-between-panels)  

> [!NOTE]
> Чтобы включить эксперимент, перейдите к [включаем][DevtoolsExperimentalFeaturesTurnOn] экспериментальные функции и выберите почтовый ящик рядом с **сетевой консолью.**  
> 
> Откройте [сетевой журнал,][DevtoolsNetworkIndexLogActivity]откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.  

Проблема Chromium [#1093687][CR1093687]  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a>Работник службы отвечает На события во вкладке Timing  

Вкладка **Timing** средства **Network** теперь включает события `respondWith` сотрудников службы.  Событие сотрудника службы показывает продолжительность времени, непосредственно перед началом работы обработника событий сотрудника службы до времени, когда обещание обработника `respondWith` `fetch` будет `respondWith` `fetch` урегулировано.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Событие respondWith service worker на вкладке Timing панели Network" lightbox="../../media/2020/06/timing-tab.msft.png":::
   Событие `respondWith` сотрудника службы на **вкладке Timing** средства **Network**  
:::image-end:::  

Расширение **ответов,** полученных для отображения дополнительных сведений `fetch` из ответа, как `CacheStorageCacheName` , и `serviceWorkerResponseSource` `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Расширение ответов, полученных для отображения дополнительных сведений из ответа на выборки" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Расширение **ответов,** полученных для отображения дополнительных сведений из `fetch` ответа  
:::image-end:::  

Проблема Chromium [#1066579][CR1066579]  

### <a name="webhint-feedback-in-the-issues-panel"></a>webhint feedback in the Issues panel  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

[webhint][WebhintMain] — это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени о доступности, совместимости между браузерами, безопасности, производительности, PWAs и других распространенных проблемах веб-разработки веб-сайтов.  Просмотр отзывов веб-сайтов в панели ["Проблемы".][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   webhint feedback in the Issues panel  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, перейдите к [включаем экспериментальные функции][DevtoolsExperimentalFeaturesTurnOn] и выберите почтовый ящик рядом с **веб-хинтом Enable**.  
> 
> Откройте панель ["Проблемы",][DevtoolsIssues] чтобы отобразить отзывы из веб-хинта.  

Проблема Chromium [#1070378][CR1070378]  

### <a name="move-tools-between-panels"></a>Перемещение инструментов между панелями  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Экспериментальная функция":::
   Экспериментальная функция  
:::image-end:::  

Обычно такие средства, как **Elements** и **Network,** могут открываться только в основной панели \(top\) DevTools.  Аналогичным образом такие средства, как **3D View** и **Issues,** могут открываться только в панели ящика \(bottom\) DevTools.  Теперь вы можете настроить макет DevTools, перемещая инструменты между верхней и нижней панелями.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Перемещение инструментов между панелями" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Перемещение инструментов между панелями  
:::image-end:::  

> [!NOTE]
> Чтобы включить эксперимент, [][DevtoolsExperimentalFeaturesTurnOn] перейдите к включаем экспериментальные функции и выберите контрольный ящик рядом, чтобы включить поддержку для перемещения вкладок **между панелями.**  

Проблема Chromium [#897944][CR897944]  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a>Улучшенный инструментарий Инициатора в панели Network  

В Microsoft Edge 83 и 84 в сетевом журнале с горизонтальной панелью [][DevtoolsNetworkIndexLogActivity] прокрутки отображаются инструменты для столбца Инициатор, который показывает причину запроса ресурсов.  Отобразить стек вызовов, который инициировал запрос, удалось только путем горизонтального прокрутки в панели инструментов.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Инструментарий Инициатора в Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Инструментарий Инициатора в Microsoft Edge 84  
:::image-end:::  

Начиная с Microsoft Edge 85, теперь вы можете отображать стек вызовов Инициатора в панели инструментов без прокрутки по горизонтали.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Инструментарий Инициатора в Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Инструментарий Инициатора в Microsoft Edge 85
:::image-end:::  

Проблема Chromium [#1069404][CR1069404]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 85, которые были внесены в проект Chromium с открытым исходным кодом.  

### <a name="style-editing-for-css-in-js-frameworks"></a>Редактирование стилей для структур CSS-in-JS  

В **области Стилей** теперь лучше поддерживать стили редактирования, созданные с API объектов [CSS (CSSOM).][CsswgDraftsCssom]  Многие инфраструктуры и библиотеки CSS-in-JS используют API CSSOM под капотом для создания стилей.  

Теперь вы можете изменять стили, добавленные в JavaScript, используя [таблицы конструкторских стилей.][WicgConstructStylesheet]  Конструкторные таблицы стилей — это новый способ создания и распространения многоиспользоваемых стилей при использовании [теневого DOM.][MdnShadowDom]  

Например, `h1` стили, добавленные `CSSStyleSheet` с API CSSOM\), ранее не редактироваться не были.  Стили теперь можно изменить в панели **Стилей.**  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Изменение фонового свойства стилей h1, добавленных cSSStyleSheet с розового на lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Изменение `background` свойства `h1` стилей, добавленных `CSSStyleSheet` с на `pink` `lightblue` .
:::image-end:::  

Попробуйте использовать эту функцию с помощью примера [CSS-in-JS.][CodepenZoherghadyaliAbdgrpz]

Проблема Chromium [#946975][CR946975]  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a>Маяк 6 в панели Маяк  

Панель **Lighthouse** теперь работает Lighthouse 6.  Полный список всех изменений перейдите к [заметкам о выпуске v6.0.0.][GithubGoogleChromeLighthouse600]  

Маяк 6.0 вводит в отчет три новые метрики: Самая большая контентная краска \(LCP\), Накопительная смена макета \(CLS\) и Общее время блокировки \(TBT\).  

Формула показателей производительности также была перенагружена, чтобы лучше отражать нагрузку пользователя.  

Проблема Chromium [#772558][CR772558]  

#### <a name="first-meaningful-paint-deprecation"></a>Первая амортизации содержательной краски  

Первая значимая краска \(FMP\) отстает в Lighthouse 6.0.  FMP также удален из панели **Performance.**  **Самая большая контентная краска** — это рекомендуемая замена для FMP.  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Проблема Chromium [#1096008][CR1096008]  

### <a name="support-for-new-javascript-features"></a>Поддержка новых функций JavaScript  

DevTools теперь лучше поддерживает некоторые из последних языковых функций JavaScript.  

:::row:::
   :::column span="1":::
      [Необязательный][V8DevOptionalChaining] автозаполнение синтаксиса цепочки  
   :::column-end:::
   :::column span="2":::
      Автоматическое завершение свойства в **консоли** теперь поддерживает необязательный синтаксис цепочки, например, теперь работает в дополнение к  `name?.` и `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Синтаксис выделения для [частных полей][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      Поля частных классов теперь правильно выделены синтаксис и довольно напечатаны в **панели Источники.**  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Синтаксис, выделяющийся для [оператора совмещений Nullish][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      DevTools теперь правильно печатает nullish coalescing operator в **панели Источники.**  
   :::column-end:::
:::row-end:::  

Проблемы Chromium [#1073903,][CR1073903] [#1083214][CR1083214], [#1083797][CR1083797]  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a>Новые предупреждения о ярлыке приложения в области Манифест  

**Ярлыки приложений помогают** пользователям быстро приступить к общим или рекомендуемым задачам в веб-приложении.  

<!--todo: add App shortcuts when section is live  -->  

В **области Манифест** теперь показаны предупреждения для следующих условий.  

* Значки ярлыка приложения меньше 96x96 пикселей  
* Значки ярлыка приложения и значки манифеста не являются квадратными \(так как значки игнорируются\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Предупреждения о ярлыке приложения" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Предупреждения о ярлыке приложения  
:::image-end:::  

Проблема Chromium [#955497][CR955497]  

### <a name="consistent-display-of-the-computed-pane"></a>Последовательное отображение вычислительной области  

Компьютерная **области** в **инструменте Elements** теперь последовательно отображается в качестве области во всех размерах viewport.  Ранее **вычислительная часть** слилась в области **Стилей,** когда ширина представления DevTools была узкой.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Вычислительная области последовательно отображает в качестве отдельной области, даже если DevTools являются узкими" lightbox="../../media/2020/06/computed-pane.msft.png":::
   Компьютерная **области** последовательно отображает в качестве отдельной области, даже если DevTools являются узкими.
:::image-end:::  

Проблема Chromium [#1073899][CR1073899]  

### <a name="bytecode-offsets-for-webassembly-files"></a>Смещение bytecode для файлов WebAssembly  

DevTools теперь использует смещения bytecode для отображения номеров строки разборки Wasm.  
Номера строк делают более понятным, что вы смотрите на двоичные данные, и в большей мере соответствуют расположениям ссылок на время запуска Wasm.  

Проблема Chromium [#1071432][CR1071432]  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a>Line-wise copy and cut in Sources Panel  

При выполнении копирования или вырезания без выбора в редакторе панели [Источников,][DevtoolsSourcesEditCssJavascript]DevTools копирует или режет текущую строку контента.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="С помощью курсора в конце строки 5 скопируйте всю строку из pen.js в DevTools и вклеив Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   С помощью курсора в конце строки 5 скопируйте всю строку из **pen.js** в DevTools и вклеив [Visual Studio Code][VisualStudioCode].
:::image-end:::  

Проблема Chromium [#800028][CR800028]

### <a name="console-settings-updates"></a>Обновления параметров консоли  

#### <a name="ungroup-same-console-messages"></a>Разгруппировка тех же сообщений консоли  

Группа, **похожая** на параметры консоли, теперь применяется к дублирующимся сообщениям.  Раньше он просто применялся к подобным сообщениям.  

Например, ранее DevTools не разгруппировали сообщения, даже несмотря на то, что подобная группа не `hello` была перенастройкой. ****  Теперь сообщения `hello` негруппировываются.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="При неконтраншировке аналогичных групп сообщения привета негруппировываются" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   При **** неконтраншировке аналогичных групп сообщения `hello` негруппировываются
:::image-end:::  

Дайте этой функции попробовать [пример, который отправляет дублирующиеся сообщения на консоль][CodepenZoherghadyaliZyrjgdJ].  

Проблема Chromium [#1082963][CR1082963]  

### <a name="persisting-selected-context-only-settings"></a>Сохраняемая только параметры выбранного контекста  

В **настоящее время сохраняются** только параметры выбранного контекста в параметрах консоли.  Ранее параметры сбрасывались при каждом закрытии и возобновлении работы DevTools.  Это изменение делает поведение параметра совместимым с другими настройками консоли.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Только параметр выбранного контекста" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Только параметр выбранного** контекста  
:::image-end:::  

Проблема Chromium [#1055875][CR1055875]  

### <a name="performance-panel-updates"></a>Обновления панели производительности  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a>Сведения о кэше компиляции JavaScript в **средстве Performance**  

[Сведения о кэше компиляции JavaScript][V8DevCodeCaching] теперь всегда отображаются в панели **сводки** средства **Performance.**  Ранее в DevTools не было ничего, связанного с кэшингом кода, если кэшировать код не удалось.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Сведения о кэше компиляции JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Сведения о кэше компиляции JavaScript  
:::image-end:::  

Проблема Chromium [#912581][CR912581]  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a>Выравнивание времени навигации в панели Performance  

Панель **Performance** используется для показа времени в линейках на основе начала записи.  Теперь время изменилось для записей, в которых пользователь перемещается, где в DevTools теперь указывается время линейки относительно навигации.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Выравнивание времени навигации в средстве Performance" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Выравнивание времени навигации в **средстве Performance**  
:::image-end:::  

Время для событий , First Paint, First Contentful Paint и Biggest Contentful Paint обновляется по отношению к началу навигации, что означает, что время совпадает со сроками, о которых сообщается `DOMContentLoaded` `PerformanceObserver` .  

Проблема Chromium [#974550][CR974550]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Новые значки для точек разрыва, условных точек и точек входа  

Панель **Источников** имеет новые проекты для точек разрыва, условных точек и точек входа.  Точки breakpoints представлены красным кругом, как и [Visual Studio код][VisualStudioCode] [и Visual Studio][VisualStudio].  Значки добавляются для дифференцировать условные точки и точки входа.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Точки останова" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Точки останова  
:::image-end:::  

Проблема Chromium [#1041830][CR1041830]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Изменение CSS и JavaScript — обзор панели источников | Документы Майкрософт"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Сетевое действие журнала — Проверка сетевой активности в Microsoft Edge DevTools | Документы Майкрософт"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Редактирование стилей для CSS-in-JS frameworks | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Отправка дублирующих сообщений в консольные | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Пример планирования сетки CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: обновление до последней версии | Ошибки Chromium"  
[CR800028]: https://crbug.com/800028 "Дублировать ярлык строки в редакторе Средства разработчика, не работая после обновления Chrome | Ошибки Chromium"  
[CR912581]: https://crbug.com/912581 "Показать, какие скрипты были кэшироваться V8 в DevTools/about:tracing | Ошибки Chromium"  
[CR946975]: https://crbug.com/946975 "Боковая панель стилей DevTools не работает со построенными таблицами стилей | Ошибки Chromium"  
[CR955497]: https://crbug.com/955497 "Меню ярлыка значка приложения для pwAs | Ошибки Chromium"  
[CR974550]: https://crbug.com/974550 "Несоответствие показателей между панелью Perf и performanceObserver | Ошибки Chromium"  
[CR1041830]: https://crbug.com/1041830 "Улучшение цветов для точек | Ошибки Chromium"  
[CR1055875]: https://crbug.com/1055875 "Значение параметра выбранной консоли только контекста не сохраняется после закрытия и открытия средств разработки | Ошибки Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Show ServiceWorkers Fetch Timeline per request in Network panel | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Ошибки Chromium"  
[CR1073899]: https://crbug.com/1073899 "Вкладка computed style исчезает в режиме отклика | Ошибки Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: выделение синтаксиса не работает с частными полями | Ошибки Chromium"  
[CR1082963]: https://crbug.com/1082963 "Нельзя отключить аналогичное поведение сообщений группы консоли | Ошибки Chromium"  
[CR1083214]: https://crbug.com/1083214 "acorn не поддерживает необязательный | Ошибки Chromium"  
[CR1083797]: https://crbug.com/1083797 "Красивая печать, нарушенная для ненульского | Ошибки Chromium"  
[CR1096008]: https://crbug.com/1096008 "Удаление FMP-| Ошибки Chromium"  
[CR1047356]: https://crbug.com/1047356 "CSS Grid/Flexbox/Table tooling | Ошибки Chromium"  
[CR1093687]: https://crbug.com/1093687 "Создание средства для создания и воспроизведения синтетических сетевых запросов | Ошибки Chromium"  
[CR1070378]: https://crbug.com/1070378 "Интеграция веб-хинта в devTools | Ошибки Chromium"  
[CR1069404]: https://crbug.com/1069404 "[Средства разработчика] всплывающие окантовки виджетов слишком узкие | Ошибки Chromium"  
[CR897944]: https://crbug.com/897944 "Перетаскиваемые панели | Ошибки Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема — MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Использование теневых doM-| MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Объектная модель CSS (CSSOM) | Проекты редактора рабочей группы W3C CSS"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Поля частных классов — общедоступные и частные | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Кэшинг кода для разработчиков JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Nullish coalescing | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Необязательный | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Объекты таблицы стилей| CG веб-инкубатора"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Веб-сайт, который мы хотим"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/06/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
