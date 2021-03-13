---
description: Подражать недостаткам цветового зрения, док-станции налево в командном меню и другие.
title: Новые возможности в DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f97155b12a679f630ce80c007e7f0ca693e19876
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408355"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a>Что нового в DevTools (Microsoft Edge 83)  

В соответствии с обновленным расписанием хрома мы корректируем расписание предстоящих выпусков Microsoft Edge и отменяем выпуск Microsoft Edge 82. Дополнительные сведения можно [получить в][WindowsBlogStableRelease] нашем блоге.  

Вот новые функции, доступные в DevTools в Microsoft Edge 83.  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Объявления из команды Microsoft Edge DevTools  

В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.  Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.  Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a>Удаленное отлагивание Microsoft Edge на устройствах с Windows 10  

Приложение [Remote Tools для Microsoft Edge \(Beta\)][RemoteTools] теперь доступно в Microsoft [Store.][MicrosoftStore]  С помощью этого приложения, которое расширяет портал устройств [Windows,][WindowsUwpDebugTestPerfDevicePortal]вы можете подключиться от экземпляра Microsoft Edge, запущенного на компьютере разработки, к удаленному устройству Windows 10, отобразить список целей \(все вкладки в Microsoft Edge и [PWAs][ProgressiveWebAppsChromiumIndex] открыты на устройстве Windows 10\), а также использовать DevTools на машине разработки против целевой задачи, запущенной на удаленном устройстве Windows 10.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools for Microsoft Edge (Beta), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Приложение [Remote Tools for Microsoft Edge (Beta),][RemoteTools] доступное в Microsoft [Store][MicrosoftStore]  
:::image-end:::  

[Ознакомьтесь с нашим руководством по настройке устройства Windows 10][DevtoolsRemoteDebuggingWindows]и компьютера разработки для удаленной отладки.  Дайте нам знать о вашем опыте удаленной отладки, отправив в [twitter][PostTweetEdgeDevTools] или отправив значок [обратной связи!](#getting-in-touch-with-microsoft-edge-devtools-team)  

### <a name="new-ways-to-access-settings"></a>Новые способы доступа к Настройкам  

Есть тонны параметров для DevTools, которые вы можете настроить, чтобы сделать DevTools выглядеть, чувствовать и работать так, как вам нужно. В Microsoft Edge 83 доступ к [настройкам][DevtoolsCustomizeIndexSettings] в DevTools теперь намного проще.  Откройте параметры со значком передач рядом с оповещениями консоли и основным меню.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Значок передач открывает параметры в DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   Значок передач открывает **параметры** в DevTools  
:::image-end:::  

Вы также можете открыть [параметры][DevtoolsCustomizeIndexSettings] из **основного** меню в **дополнительных средствах.**

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Главное меню > дополнительные средства > параметры" lightbox="../../media/2020/03/settings2.msft.png":::
   **Главное меню**  >  **Дополнительные средства**  >  **Параметры**  
:::image-end:::  

Проблема Chromium [#1050855][CR1050855]

### <a name="new-and-improved-infobars"></a>Новые и улучшенные информационные панели

Информационные панели уведомлений \(infobars\) в DevTools теперь имеют улучшенный внешний вид и более функциональные возможности. В Microsoft Edge 83 информационные панели легче читать и предоставлять кнопки, чтобы можно было сразу принять соответствующие действия.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infobar для красивой печати добытого файла в Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Infobar для красивой печати добытого файла в Microsoft Edge Version 83  
:::image-end:::  

Проблема Chromium [#1056348][CR1056348]

### <a name="navigate-the-color-picker-with-your-keyboard"></a>Перейдите по выбору цвета с помощью клавиатуры  

Выбор [цвета —][DevtoolsCssReferenceColorPicker] это GUI в панели [Elements][DevtoolsCssIndex] для изменений и `color` `background-color` объявлений.  В предыдущих версиях Microsoft Edge вы не могли перемещаться по разделу **Оттенки** выбора [цвета][DevtoolsCssReferenceColorPicker] с помощью клавиатуры.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Теперь вы можете использовать клавиатуру для перемещения селектора в разделе Оттенки выбора цвета" lightbox="../../media/2020/03/color-picker.msft.png":::
   Теперь вы можете использовать клавиатуру для перемещения селектора в разделе **Оттенки** выбора [цвета][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **Оттенки** выбора цвета.  

Проблема Chromium [#963183][CR963183]  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a>Вкладка Свойства теперь заполняется после обновления страницы  

В Microsoft Edge 81 и ранее вкладка **Properties** в панели [Elements][DevtoolsCssIndex] была нарушена путем обновления страницы.  При обновлении страницы вкладка **Properties** не заполняла свойства выбранного в настоящее время элемента.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="В Microsoft Edge 81 и ранее вкладка Properties была пустой после обновления страницы" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   В Microsoft Edge 81 и ранее вкладка **Properties** была пустой после обновления страницы  
:::image-end:::  

В Microsoft Edge 83 теперь можно отобразить свойства выбранного в настоящее время элемента после обновления страницы на **вкладке Свойства.**  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="В Microsoft Edge 83 вкладка Properties отображает свойства выбранного в настоящее время элемента после обновления страницы" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   В Microsoft Edge 83 вкладка **Properties** отображает свойства выбранного в настоящее время элемента после обновления страницы  
:::image-end:::  

Проблема Chromium [#1050999][CR1050999]  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a>Используйте клавиши стрелки для прокрутки в средстве Изменения  

Средство **Изменения отслеживает** все изменения, внесенные в CSS или JavaScript в DevTools.  Вы можете использовать средство **Изменения,** чтобы быстро отображать все изменения и возвращать их в редактор/IDE.  

Чтобы открыть средство **Изменения,** выберите `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [командное меню][DevToolsCommandMenuIndex] и введите `changes` .  выберите и запустите команду **Show Changes,** чтобы открыть средство **Изменения** в ящике DevTools.  

При внесении изменения в минированную папку средство **Changes** позволяет прокручивать по горизонтали, чтобы отобразить весь заминированный код.  Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш стрелки на клавиатуре.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="В Microsoft Edge 83 можно прокручивать по горизонтали клавиши со стрелками, чтобы отобразить код в средстве Изменения" lightbox="../../media/2020/03/changes.msft.png":::
   В Microsoft Edge 83 можно прокручивать по горизонтали клавиши со стрелками, чтобы отобразить изменения, внесенные в ваш заминированный код в средстве **Изменения**  
:::image-end:::  

Если вы используете считыватели экрана или клавиатуру для навигации по DevTools, отправьте нам свои отзывы, направив на нас твиты или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team) [][PostTweetEdgeDevTools]  

Проблема Chromium [#963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Объявления из проекта Chromium  

В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 83, которые были внесены в проект Chromium с открытым исходным кодом.  

### <a name="emulate-vision-deficiencies"></a>Эмуляция дефектов зрения  

Откройте [вкладку Rendering][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] и используйте новую функцию **эмулировать** недостатки зрения, чтобы получить представление о том, как люди с различными типами недостатков зрения испытывают на своем сайте.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Эмулирование размытого зрения" lightbox="../../media/2020/03/vision.msft.png":::
   Эмулирование размытого зрения  
:::image-end:::  

DevTools может эмулировать размытое зрение и следующие типы [недостатков цветового зрения.][ColorBlindnessTypes]  

| Дефицит цветового зрения | Сведения |  
|:--- |:--- |  
| Протанопия | Невозможность воспринимать красный свет. |  
| Deuteranopia | Невозможность воспринимать зеленый свет. |  
| Тританопия | Невозможность воспринимать синий свет. |  
| Ахроматопсия | Невозможность воспринимать любой цвет, за исключением оттенков серого \(крайне редко\). |  

Существуют менее экстремальные версии этих недостатков цветового зрения, и на самом деле они являются более распространенными.  
Например, протаномали — это пониженная чувствительность к красному свету (в отличие от протанопии, которая является полной невозможностью воспринимать красный свет). Тем не менее, эти недостатки зрения **omaly** не так четко определены: каждый человек с таким недостатком зрения отличается и может видеть вещи по-разному \(возможность воспринимать больше / меньше соответствующих цветов \).  

При разработке более экстремальных моделей в DevTools ваши веб-приложения гарантированно будут доступны для людей с протаномалией, deuteranomaly, tritanomaly и achromatomaly.  

Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#1003700][CR1003700]  

### <a name="emulate-locales"></a>Эмулировать локальные  

Эмулировать локальные параметры, задав расположение в **расположении**  >  **датчиков.** [Откройте **командное меню и** ][DevToolsCommandMenuIndex] `Sensors` введите, чтобы получить доступ к **вкладке Датчики.**  После выполнения этих действий DevTools изменяет текущий локальный код по умолчанию, влияя на следующий код.  

*   `Intl.*` API, например: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Другие API JavaScript с локальными данными, например: `String.prototype.localeCompare` `*.prototype.toLocaleString` `123_456..toLocaleString()`  
*   API DOM, такие как `navigator.language` и `navigator.languages`  
*   [Заглавная головка запроса http accept-Language][MDNAcceptLanguage] HTTP  

> [!NOTE]
> Обновления и не видны сразу, но только после `navigator.language` `navigator.languages` следующей навигации или обновления страницы.  Изменения в `Accept-Language` загона HTTP отражаются только для последующих запросов.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Эмулирование локального" lightbox="../../media/2020/03/locale.msft.png":::
   Эмулирование локального  
:::image-end:::  

Чтобы попробовать демонстрацию, перейдите к [примеру кода,][MathiasByensLocaleDemo]зависимого от locale.

Проблема Chromium [#1051822][CR1051822]

### <a name="cross-origin-embedder-policy-coep-debugging"></a>Отладка политики встраивляемого в поперечнике (COEP)  

Панель Network теперь предоставляет сведения [о][COEP] отладки политики встраивляющихся между собой.  

В **столбце Status** теперь приводится краткое объяснение, почему был заблокирован запрос, а также ссылка для просмотра заглавных окей этого запроса для дальнейшей отладки:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Заблокированные запросы в столбце **Status**" lightbox="../../media/2020/03/status.msft.png":::
   Заблокированные запросы в **столбце Состояние**  
:::image-end:::  

В **разделе Заглавные ответы** вкладки **"Заготки"** содержится дополнительные рекомендации по устранению проблем:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Дополнительные рекомендации в разделе Заглавные ответы" lightbox="../../media/2020/03/guidance.msft.png":::
   Дополнительные рекомендации в **разделе Заглавные ответы**  
:::image-end:::  

Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#1051466][CR1051466]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Новые значки для точек разрыва, условных точек и точек входа  

Панель Источников имеет новые значки для точек разрыва, условных точек и точек входа:  

*   Breakpoints \(![Breakpoint](../../media/2020/03/breakpoint.msft.png)\) представлены красными кругами.  
*   Условные точки разрывов \.![Условная точка разрыва](../../media/2020/03/conditional.msft.png)\) представлены полу-красными полубелыми кругами.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) представлены красными кругами с значками консоли.  

Мотивация для новых значков была в том, чтобы сделать пользовательский интерфейс более совместимым с другими средствами отладки GUI \(которые обычно красные точки разлома цвета\) и упростить различие между 3 функциями с первого взгляда.  

Проблема Chromium [#1041830][CR1041830]  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a>Просмотр сетевых запросов, за набором определенного пути cookie  

Используйте новое `cookie-path` ключевое слово фильтра в средстве **Network,** чтобы сосредоточиться на сетевых запросах, которые устанавливают определенный [путь cookie.][MDNCookiePath]  

Проверьте [запросы фильтра по свойствам,][DevtoolsNetworkReferenceFilterRequestsProperties] чтобы узнать больше ключевых слов, как `cookie-path` .

### <a name="dock-to-left-from-the-command-menu"></a>Стыковка слева от меню команды  

Откройте [командное меню][DevToolsCommandMenuIndex] и запустите команду для перемещения `Dock to left` DevTools слева от вашего представления.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, пристыкованный слева от viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   DevTools, пристыкованный слева от viewport  
:::image-end:::  

> [!NOTE]
> Функция **Dock слева** была доступна с Microsoft Edge 75, но ранее она была доступна только из [основного меню.][DevtoolsCustomizePlacementsChangeMainMenu]  Новая функция в Microsoft Edge 83 в том, что теперь вы можете получить доступ к этой функции из командного меню.  

Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#1011679][CR1011679]  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a>Панель аудитов теперь является панелью Маяк  

Команда DevTools часто получает отзывы от веб-разработчиков о том, что хотя можно было запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они пытались его найти, они не могли найти панель "Маяк", поэтому панель **Аудиты** теперь панель **Маяк.**  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Панель Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Панель Lighthouse  
:::image-end:::  

> [!NOTE]
> Панель **Lighthouse** предоставляет ссылки на контент, который содержится на сторонних веб-сайтах.  Корпорация Майкрософт не несет ответственности и не контролирует содержимое этих сайтов и любые данные, которые они могут собирать.  

### <a name="delete-all-local-overrides-in-a-folder"></a>Удаление всех локальных переопределей в папке  

После настройки **** локальных переопределей можно навести курсор на каталог, открыть контекстное меню \(правой кнопкой мыши\) и выбрать новый параметр **Удалить** все переопределения, чтобы удалить все локальные переопределения в этой папке.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Удаление всех переопределе-" lightbox="../../media/2020/03/overrides.msft.png":::
   Удаление всех переопределе-  
:::image-end:::  

Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#1016501][CR1016501]  

### <a name="updated-long-tasks-ui"></a>Обновленный пользовательский интерфейс длинных задач  

Long **Task —** это код JavaScript, который монополизирует основной поток в течение длительного времени, из-за чего веб-страница замерзает.  

Некоторое время [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] вы могли визуализировать длинные задачи в панели Performance, но в Microsoft Edge 83 пользовательский интерфейс визуализации длинных задач в панели Performance был обновлен.  Длинная часть задачи теперь окрашена полосатым красным фоном.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Новый пользовательский интерфейс long Task" lightbox="../../media/2020/03/long-task.msft.png":::
   Новый пользовательский интерфейс long Task  
:::image-end:::  

Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)  

Проблема Chromium [#1054447][CR1054447]  

### <a name="maskable-icon-support-in-the-manifest-pane"></a>Поддержка значка маскировки в области Манифест  

Android Oreo представил адаптивные значки, которые отображают значки приложений в различных формах на разных моделях устройств.  **Маскируемые** значки — это новый формат значков, который поддерживает адаптивные значки, которые позволяют обеспечить хорошее внешний вид значка [PWA][ProgressiveWebAppsChromiumIndex] на устройствах, поддерживаюх стандартные значки с масками.  

Вкажите в новом **Show** только минимальную безопасную область для почтового ящика с масками значков в области **Манифест,** чтобы проверить, хорошо ли выглядит ваша маскабельная иконка на устройствах Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Показать только минимальную безопасную область для проверки маскируемых значков" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Показать **только минимальную безопасную область для проверки маскируемых значков**  
:::image-end:::  

> [!NOTE]
> Эта функция запущена в Microsoft Edge 81.  Обновления, охватываемых здесь в Microsoft Edge 83, не были охвачены в [What's New In DevTools (Microsoft Edge 81).][WhatsNew81]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Скачивание Microsoft Edge предварительных каналов  

Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Новые возможности в DevTools (Microsoft Edge 81) | Документы Майкрософт"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Измените цвета с помощью | Документы Майкрософт"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение размещения из основного меню | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основных действий потоков | Документы Майкрософт"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering | Документы Майкрософт"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладки устройств Windows 10 | Документы Майкрософт"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Breakpoints line-of-code - How To Pause Your Code with Breakpoints in Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам — ссылки на | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка Microsoft Edge DevTools | Документы Майкрософт"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Обзор портала устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные средства для Microsoft Edge (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Обновление выпусков стабильных каналов для Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема - MicrosoftDocs/edge-developer - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Веб-сайт, который мы хотим"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Типы цветовой слепоты"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящих от локального доступа"  

[CR963183]: https://crbug.com/963183 "Выпуск 963183: DevTools не соответствуют требованиям WCAG"  
[CR1003700]: https://crbug.com/1003700 "Выпуск 1003700. Добавление поддержки DevTools для моделирования дефицита цветового зрения"  
[CR1011679]: https://crbug.com/1011679 "Выпуск 1011679: ввести пункт "Стыковка налево" с помощью командного меню"  
[CR1016501]: https://crbug.com/1016501 "Выпуск 1016501: запрос на функции: кнопка для удаления всех локальных переопределей"  
[CR1050999]: https://crbug.com/1050999 "Выпуск 1050999: Вкладка свойств"  
[CR1051466]: https://crbug.com/1051466 "Выпуск 1051466: поддержка отладки COOP/COEP в DevTools"  
[CR1054447]: https://crbug.com/1054447 "Выпуск 1054447: Обновление показателей производительности в Хронике DevTools"  
[CR1051822]: https://crbug.com/1051822 "Выпуск 1051822: DevTools: добавление пользовательского интерфейса для эмуляции локального интерфейса"
[CR1041830]: https://crbug.com/1041830 "Выпуск 1041830: улучшение цветов для точек разрыва"
[CR1050855]: https://crbug.com/1050855 "Выпуск 1050855: трудно найти представление параметров"
[CR1056348]: https://crbug.com/1056348 "Выпуск 1056348: обновление компонентов Infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "CoOP и COEP — политика кросс-origin Opener"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "CoOP и COEP — политика встраивляемого перекрестного происхождения"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Маяк | GitHub"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/updates/2020/03/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
