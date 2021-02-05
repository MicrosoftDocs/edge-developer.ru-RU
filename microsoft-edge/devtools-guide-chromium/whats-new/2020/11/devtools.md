---
description: Microsoft Edge в Linux, улучшенные советы webhint в средстве "Проблемы", новые функции отладки служебного сценария и т. д.
title: Что нового в средствах разработчика (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9e4bdfcb3cc32364931894dcb3c857ac6e082809
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313088"
---
# Что нового в средствах разработчика (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Microsoft Edge и Microsoft Edge Driver теперь доступны в Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge Dev теперь поддерживается в дистрибутивах Ubuntu, Debian, Fedora и openSUSE.  Скачайте и установите пакет Microsoft Edge Dev `.deb` или `.rpm` непосредственно с сайта [программы предварительной оценки Microsoft Edge][MicrosoftinsiderDownloadPlatformLinux] или используйте стандартные средства управления пакетами своего дистрибутива Linux.  

Если вы используете среду Linux в решениях непрерывной интеграции и доставки \(CI/CD\), Microsoft Edge Driver также доступен в Linux.  Чтобы начать автоматизацию Microsoft Edge Dev с использованием Microsoft Edge Driver, перейдите на страницу [загрузок Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Справку по автоматизации Microsoft Edge Dev вместе с Microsoft Edge Driver см. в статье [Использование WebDriver (Chromium) для автоматизации тестов][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="Средства разработчика в Microsoft Edge в Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   Средства разработчика в Microsoft Edge в Linux  
:::image-end:::  

## Улучшенные советы webhint и платформы в средстве "Проблемы"  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Средство с открытым кодом [webhint][WebhintMain]предоставляет отзывы в режиме реального времени для веб-сайтов и локальных веб-страниц.  С [Microsoft Edge версии 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel] отзывы webhint доступны в средстве [Проблемы][DevtoolsIssuesIndex].  Проблемы, отображаемые в средстве **Проблемы**, теперь проще просматривать благодаря добавлению следующих категорий.  

*   [Специальные возможности][WebhintUserGuideHintsAccessibility]  
*   [Совместимость][WebhintUserGuideHintsCompatibility]  
*   [Производительность][WebhintUserGuideHintsPerformance]  
*   [Ошибки][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Безопасность][WebhintUserGuideHintsSecurity]  
    
Теперь вы можете отфильтровать сторонние проблемы с помощью новой галочки.  Функция фильтрации помогает скрыть проблемы, связанные с кодом сторонних библиотек или других источников.  

Чтобы помочь с просмотром проблем, выявленных инструментом [webhint][WebhintMain], средство **Проблемы** теперь отображает следующую информацию.  

*   Улучшенные фрагменты кода.  
*   Ссылки на другие связанные панели.  
*   Ссылки на документацию по устранению проблем на вашем веб-сайте.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Средство Проблемы" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Средство **Проблемы**  
:::image-end:::  

## Составные слои теперь находятся в трехмерном представлении  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Теперь вы можете визуализировать содержимое **Слои** вместе со значениями z-index и объектной моделью документов \(DOM\).  Эта функция помогает выполнять отладку без частого переключения между средствами [Трехмерное представление][Devtools3dViewIndex] и **Слои**.  Для обеспечения комплексного визуального интерфейса отладки [трехмерное представление и составные слои теперь объединены][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Панель Составные слои" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Панель **Составные слои**  
:::image-end:::  

## Определения переменных CSS в панели "Стили"  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

В панели **Стили** [переменные CSS][MdnUsingCssCustomProperties] теперь связаны непосредственно с каждым определением.  Выберите переменную, чтобы легко просмотреть или изменить определение переменной CSS.  В этом примере средства разработчика отображают атрибуты CSS для элемента `body`.  Чтобы отобразить определение переменной CSS `--theme-body-background`, выполните следующие действия.  

1.  В области **Стили** выберите `var(--theme-body-background)`.  
1.  В области **Стили** отобразится определение переменной CSS `--theme-body-background`.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Переменная CSS, связанная со стилем" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Переменная CSS, связанная со стилем  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Переменная CSS, связанная с целевым объектом стиля" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Переменная CSS, связанная с целевым объектом стиля  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Улучшения отладки служебного сценария  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Следующие новые функции средств [Сеть](#network-tool), [Приложение](#application-tool) и [Источники](#sources-tool) помогают создавать [PWA][ProgressiveWebAppsChromiumIndex].  Используйте следующие функции, если у вас возникли трудности при отладке служебного сценария.  

Маршрутизация запросов отображает события `startup` и `fetch`, основанные на сетевых запросах, выполняемых в служебных сценариях.  Временные шкалы доступны в средстве **Приложение** или **Сеть**.  Временные шкалы удобно использовать, если у вас возникли проблемы со служебными сценариями и вы хотите проверить наличие ошибок в событиях `startup` или `fetch`.  

### Средство "Приложение"  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Просматривайте все сведения о маршрутизации запросов служебных сценариев с помощью новой ссылки **Сетевые запросы**.  Чтобы отобразить дополнительный контекст при отладке служебного сценария, выполните следующие действия.  

1.  Выберите **Приложение** > **Служебные сценарии**.  
1.  Нажмите **Сетевые запросы**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Открытие средства Сеть из панели Служебные сценарии" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Открытие средства **Сеть** из панели **Служебные сценарии**
    :::image-end:::  
    
1.  Средство **Сеть** открывается в **консоли** и отображает все сетевые запросы, связанные со служебными сценариями.  Сетевые запросы фильтруются с помощью `is:service-worker-intercepted`.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Средство Сеть в консоли" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Средство **Сеть** в **консоли**  
    :::image-end:::
    
1. Чтобы вернуть средство **Сеть** на верхнюю панель, закройте **консоль**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Закрытие консоли для возврата средства Сеть" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Закрытие **консоли** для возврата средства **Сеть**  
    :::image-end:::  
    
### Средство "Сеть"  

Выполняйте отладку сетевых запросов, выполняемых в служебных сценариях.  Вы также можете открывать сетевые запросы в средстве **Приложение**.  Для каждого запроса средства разработчика отображают следующие сведения в панели [Время][DevtoolsNetworkReferenceViewTimingBreakdownRequest].  

*   Начало запроса и длительность начальной загрузки.  
*   Изменения регистрации служебных сценариев.  
*   Время выполнения обработчика события `fetch`.  
*   Время выполнения всех событий `fetch` для загрузки клиента.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Панель Время" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Панель **Время**  
:::image-end:::  

### Средство "Источники"  

В предыдущих версиях Microsoft Edge глубина в стеке вызовов была ограничена кодом JavaScript в вашем служебном сценарии.  Теперь в Microsoft Edge 88 стек вызовов отображает инициатора запросов, выполняемых в служебном сценарии.  

Чтобы найти инициатора запроса, используйте стек вызовов своего кода JavaScript в служебном сценарии.  Стек вызовов на следующих рисунках начинается с кода JavaScript в вашем служебном сценарии и отображает ссылку на исходный запрос веб-страницы как `(index):157`.  На втором рисунке выбрана ссылка и открыт инициатор, выполнивший запрос.  Инициатором на втором рисунке является веб-страница.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Файл service-worker.js и стек вызовов с выделением инициатора запроса" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         Файл `service-worker.js` и стек вызовов с выделением инициатора запроса  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Веб-страница (индекс) является инициатором запроса" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         Веб-страница `(index)` является инициатором запроса  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Копирование значения свойства сетевого запроса  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

В средстве **Сеть** скопируйте значение свойства сетевого запроса с помощью нового параметра **Копировать значение**.  Значение свойства копируется в виде декодированного значения JSON.  В предыдущих версиях Microsoft Edge вам приходилось копировать значение с помощью одного из следующих действий.  

*   Выделение всего текста и его копирование.  
*   Сохранение значения в качестве глобальной переменной (если применимо) и копирование его из вкладки [Консоль][DevtoolsConsoleIndex] средств разработчика.  
    
Сведения о копирования значения свойства в буфер обмена см. в разделе[Копирование форматированного отклика JSON в буфер обмена][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Копирование значения свойства в средствах разработчика" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Копирование значения свойства в средствах разработчика  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Вставка значения свойства в Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Вставка значения свойства в Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Настройка сочетания клавиш с несколькими нажатиями  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[С Microsoft Edge версии 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings] вы можете настраивать сочетания клавиш для любого действия в средствах разработчика.  В Microsoft Edge версии 88 теперь можно создавать сочетания клавиш с несколькими нажатиями.  Чтобы настроить сочетание клавиш для действия в средствах разработчика, перейдите в раздел [Параметры][DevtoolsCustomizeIndexSettings] > **Эксперименты** и установите флажок **Enable keyboard shortcut editor** (Включить редактор сочетания клавиш).  Дополнительные сведения о настройке и изменении сочетаний клавиш см. в разделе о [включении экспериментальной функции редактора сочетания клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Например, красное выделение отображает сочетание клавиш с несколькими нажатиями, настроенное для действия **Начать запись событий**.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Аккордные сочетания клавиш" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Сочетания клавиш с несколькими нажатиями  
:::image-end:::  

## Средства разработчика теперь соответствуют языку браузера  

В Microsoft Edge версии 87, если вы включали параметр **Согласовать язык браузера** в [параметрах средств разработчика][DevtoolsCustomizeIndexSettings], язык средств разработчика не совпадал с языком браузера.  В Microsoft Edge версии 88 средства разработчика соответствуют языку браузера, если вы включите параметр **Согласовать язык браузера**.  Дополнительные сведения о параметре средств разработчика **Согласовать язык браузера** см. в статье [Изменение языковых параметров средств разработчика][DevtoolsCustomizeLocalization].  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Параметр средств разработчика Согласовать язык браузера на японском языке" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   Параметр средств разработчика **Согласовать язык браузера** на японском языке  
:::image-end:::  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Новые средства визуализации угла CSS  

В средствах разработчика улучшена поддержка отладки угла CSS.  Если к элементу HTML на вашей странице применен угол CSS, рядом с углом в средстве **Стили** отображается значок часов.  Чтобы переключить наложение часов, щелкните значок часов.  Чтобы изменить угол, выберите любое место на часах или перетащите стрелку.  Чтобы изменить значение угла, вы также можете использовать мышь и сочетания клавиш.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1126178][CR1126178] и [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

Следующий угол CSS используется в качестве примера.  

```css
background: linear-gradient(100deg, lightblue, pink);
```

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Угол CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Угол CSS  
:::image-end:::  

### Эмуляция размера квоты хранилища в области "Хранилище"  

Теперь вы можете переопределить размер квоты хранилища области **Хранилище**.  Эта функция позволяет эмулировать различные устройства и тестировать поведение веб-сайта или приложения в сценариях низкой доступности диска.  Чтобы эмулировать квоту хранилища, выполните следующие действия.  

1.  Выберите **Приложение** > **Хранилище**.  
1.  Установите флажок **Эмулировать настраиваемую квоту хранилища**.  
1.  Введите допустимое число.  
    
Дополнительные сведения о том, как эмулировать мобильные устройства и другие функции в средствах разработчика, см. в статье [Эмуляция мобильных устройств в средствах разработчика Microsoft Edge][DevtoolsDeviceModeIndex].  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [945786][CR945786] и [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Эмуляция размера квоты хранилища" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Эмуляция размера квоты хранилища  
:::image-end:::  

### Отчет об ошибках CORS в средстве "Сеть"  

Попробуйте эту функцию, перейдя к [демонстрации ошибки CORS][GlitchCorsErrors].  Откройте средство **Сеть**, обновите страницу и наблюдайте за сбоем сетевого запроса CORS.  В столбце состояния отображается **ошибка CORS**.  При наведении курсора на ошибку теперь отображается код ошибки.  В Microsoft Edge версии 87 и более ранних версиях средства разработчика отображали только общее состояние **(сбой)** для ошибок CORS.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Ошибки CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Ошибки CORS  
:::image-end:::  

### Обновления представления сведений о фрейме  

#### Сведения об изоляции между источниками в представлении сведений о фрейме  

Теперь состояние изоляции между источниками отображается в разделе **Безопасность и изоляция**.  В новом разделе **Доступность API** отображается доступность `SharedArrayBuffer`s \(SAB\) и возможность совместного использования буферов с помощью `postMessage()`.  Если в настоящее время SAB и `postMessage()` доступны, но контекст не изолирован между источниками, отображается предупреждение о прекращении поддержки.  Дополнительные сведения об изоляции между источниками и о причине ее необходимости для таких функций, как `SharedArrayBuffers`, см. в разделе [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Информация о взаимодействии источников" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Информация о взаимодействии источников  
:::image-end:::  

#### Сведения о новых рабочих веб-процессах в представлении сведений о фрейме  

Средства разработчика теперь упорядочивают рабочие веб-процессы в соответствующем родительском фрейме.  Например, если фрейм `someName` создает `worker.js`, `worker.js` отображается в разделе `someName` в списке **Кадры**.  Чтобы просмотреть сведения о рабочем веб-процессе, выполните следующие действия.  

1.  Откройте средство **Приложение**.  
1.  Разверните фрейм, содержащий рабочие веб-процессы.  
1.  Разверните дерево **Рабочие процессы**.  
1.  Выберите рабочий процесс.  
    
Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1122507][CR1122507] и [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Сведения о рабочих веб-процессах" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Сведения о рабочих веб-процессах  
:::image-end:::  

#### Отображение сведений об открывающем фрейме для открытых окон  

Средства разработчика теперь упорядочивают открытые [окна][MdnWindowConstructors] в соответствующем родительском [фрейме][MdnWindowFrames].  Например, если фрейм `top` открывает `Window` для `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, `Window`отображается в разделе `top` в списке **Кадры**.  

Чтобы открыть в средстве **Элементы** фрейм, отвечающий за открытие другого окна, выполните следующие действия.  

1.  Откройте дерево **Кадры**.  
1.  Разверните узел **Открытые окна** и выберите `Window` для родительского фрейма, сведения о котором вам нужны.  
1.  Щелкните ссылку **Открывающий фрейм**.  

Отобразятся сведения о том, какой фрейм вызвал открытие другого объекта `Window`.  Чтобы отобразить открывающий элемент с средстве **Элементы**, выполните следующие действия.  

1.  Откройте дерево **Кадры**.  
1.  Выберите открытое окно, чтобы открыть сведения об элементе `Window`.  
1.  Щелкните ссылку **Открывающий фрейм**.  
    
Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Сведения об открытом фрейме" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Сведения об открытом фрейме  
:::image-end:::  

### Копирование трассировки стека для инициатора сети  

Чтобы скопировать трассировку стека в буфер обмена, выполните следующие действия.  

1.  Откройте контекстное меню \(щелкните правой кнопкой мыши\).  
1.  Выберите **Копировать** > **Копировать трассировку стека**.  
    
Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Копирование трассировки стека" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Копирование трассировки стека  
:::image-end:::  

### Просмотр значения переменной Wasm при наведении указателя мыши  

Используйте эту функцию для просмотра значения переменной WebAssembly \(Wasm\) при приостановке кода.  Чтобы отобразить текущее значение переменной, наведите курсор на нее.  Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1058836][CR1058836] и [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Просмотр переменной Wasm при наведении указателя мыши" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Просмотр переменной Wasm при наведении указателя мыши  
:::image-end:::  

### Согласованные единицы измерения для размеров файлов и памяти  

Средства разработчика теперь согласованно используют `kB` для отображения размеров файлов и памяти.  Предыдущие средства смешивали использование `kB` и `KiB`.

*   `kB` или килобайт \(10^3 или 1000 байт\)  
*   `KiB` или кибибайт \(2^10 или 1024 байт\)  
    
Например, средство **Сеть** ранее использовало `kB` в метках, но `KiB` — в вычислениях.  Ваши отзывы показали, что это несоответствие приводило к путанице.  Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1035309][CR1035309].  

## Скачивание Microsoft Edge предварительных каналов  

Если вы используете Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.  Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Трехмерное представление | Документация Майкрософт"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Обзор консоли | Документация Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Изменение языковых параметров средств разработчика | Документация Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включение редактора сочетаний клавиш — экспериментальные функции | Документация Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Включение составных слоев в трехмерном представлении — экспериментальные функции | Документация Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Копирование форматированного отклика JSON в буфер обмена — справочник по анализу сети | Документация Майкрософт"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Просмотр разбивки времени запроса — справочник по анализу сети | Документация Майкрософт"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Использование WebDriver (Chromium) для автоматизации тестирования | Документация Майкрософт"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивное веб-приложение в Windows | Документация Майкрософт"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Настройка сочетания клавиш в параметрах — что нового в средствах разработчика (Microsoft Edge 87) | Документация Майкрософт"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Отзывы webhint в панели "Проблемы" — что нового в средствах разработчика (Microsoft Edge 85) | Документация Майкрософт"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачивание WebDriver | Программа Майкрософт для разработчиков"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "Проблема 174309: средства разработчика: разрешение настройки сочетания клавиш | Ошибки Chromium"  
[CR945786]: https://crbug.com/945786 "Проблема 945786: средства разработчика: разрешение переопределения navigator.storage.estimate() | Ошибки Chromium"  
[CR1029427]: https://crbug.com/1029427 "Проблема 1029427: снижение нагрузки при отправке сообщений протоколом во внешнем интерфейсе | Ошибки Chromium"  
[CR1035309]: https://crbug.com/1035309 "Проблема 1035309: средства разработчика должны согласованно использовать МБ для обозначения мегабайт, а не мебибайт | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Проблема 1051466: поддержка отладки COOP/COEP в средствах разработчика | Ошибки Chromium"  
[CR1058836]: https://crbug.com/1058836 "Проблема 1058836: проблемы пользовательского интерфейса при отладке Wasm | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Проблема 1071432: ☂︝ wasm Basic Developer Experience | Ошибки Chromium"  
[CR1107766]: https://crbug.com/1107766 "Проблема 1107766: отображение сведений о фреймах, созданных командой "window.open()", в дереве фреймов | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1126178]: https://crbug.com/1126178 "Проблема 1126178: ☂ средства разработчика: компоненты CSS <type> | Ошибки Chromium"  
[CR1130556]: https://crbug.com/1130556 "Проблема 1130556: средства разработчика: откаты тестовых образов (эмуляция) | Ошибки Chromium"  
[CR1132084]: https://crbug.com/1132084 "Проблема 1132084: нет простого способа скопировать полезные данные запроса JSON | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1138633]: https://crbug.com/1138633 "Проблема 1138633: средства разработчика: компонент CSS <angle> должен отражать внешний вид своего свойства на фоне часов | Ошибки Chromium"  
[CR1139615]: https://crbug.com/1139615 "Проблема 1139615: инициатор сети должен предоставить возможность копирования трассировки стека | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139945]: https://crbug.com/1139945 "Проблема 1139945: значки для свойств CSS flexbox на панели "Стили" | Ошибки Chromium"  
[CR1141824]: https://crbug.com/1141824 "Проблема 1141824: улучшение отчетов об ошибках CORS в средствах разработчика | Ошибки Chromium"  
[CR1144090]: https://crbug.com/1144090 "Проблема 1144090: добавление графических объектов стиля flex в дерево "Элементы" | Ошибки Chromium"  
[CR1146985]: https://crbug.com/1146985 "Проблема 1146985: очищенный текст по-прежнему виден в текстовом поле раздела "Хранилище" окна "Средства разработчика" | Ошибки Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Ошибки CORS | Сбой"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Общий доступ к ресурсам независимо от источника (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Использование настраиваемых свойств CSS (переменные) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Конструкторы — окно | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Специальные возможности | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Совместимость | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Производительность | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Ошибки | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Безопасность | webhint"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/11/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
