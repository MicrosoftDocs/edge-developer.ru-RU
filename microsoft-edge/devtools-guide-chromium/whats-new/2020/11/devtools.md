---
description: Microsoft Edge для Linux, улучшенные советы по веб – подсказкам в инструменте "проблемы", новые функции отладки рабочих процессов и многое другое.
title: Новые возможности DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205245"
---
# Новые возможности DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Драйвер Microsoft EDGE и Microsoft EDGE, теперь доступные в Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Теперь приложение Microsoft Edge dev поддерживается для Debian, Fedora и openSUSE.  Скачайте и установите Microsoft Edge dev `.deb` или `.rpm` пакет прямо из [сайта предварительной оценки Microsoft Edge][MicrosoftinsiderDownloadPlatformLinux] или воспользуйтесь стандартными средствами управления пакетами для дистрибутива Linux.  

Если вы используете среду Linux в решениях непрерывной интеграции и поставки \ (CI/CD \), драйвер Microsoft EDGE также доступен в ОС Linux.  Чтобы приступить к автоматизации разработки Microsoft Edge с помощью драйвера Microsoft EDGE, перейдите на [страницу загрузки драйверов Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Чтобы получить помощь по автоматизации разработки Microsoft Edge вместе с драйвером Microsoft EDGE, перейдите в раздел [Использование веб-накопителя (Chromium) для автоматизации тестов][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools в Microsoft Edge для Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools в Microsoft Edge для Linux  
:::image-end:::  

## Улучшенная подсказка и советы по платформе в инструменте "проблемы"  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Средство веб- [подсказки][WebhintMain]с открытым кодом обеспечивает отзыв в реальном времени для веб-сайтов и локальных веб-страниц.  Начиная с [Microsoft Edge версии 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], изучите Отзывы по веб – подсказкам в инструменте " [вопросы][DevtoolsIssuesIndex] ".  Проблемы, возникающие в инструменте " **проблемы** ", теперь проще проанализировать с добавлением следующих категорий.  

*   [Специальные возможности][WebhintUserGuideHintsAccessibility]  
*   [Совместимость][WebhintUserGuideHintsCompatibility]  
*   [Производительность][WebhintUserGuideHintsPerformance]  
*   [Ошибок][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Безопасность][WebhintUserGuideHintsSecurity]  
    
Теперь вы можете отфильтровать сторонние проблемы с помощью нового флажка.  Функция фильтрации помогает скрыть проблемы, связанные с кодом из сторонних библиотек или из других источников.  

Для ознакомления с вопросами, обнаруженными с помощью этой [подсказки][WebhintMain], в инструменте " **проблемы** " отображаются следующие сведения.  

*   Улучшенные фрагменты кода.  
*   Ссылки на другие подходящие панели.  
*   Ссылки на документы, которые помогут вам устранить проблемы на веб-сайте.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Инструмент "проблемы"" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Инструмент " **проблемы** "  
:::image-end:::  

## Составные слои теперь отображаются в трехмерном представлении  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

Теперь вы можете визуализировать содержимое **слоев** вместе со значениями z-индекса и объектной модели документов \ (DOM \).  Эта функция позволяет выполнять отладку, не переключаясь между инструментами [3D View][Devtools3dViewIndex] и **слоев** как можно чаще.  Для всесторонней визуальной отладки [теперь можно объединять трехмерное представление и составные слои][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Область «составные слои»" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Область « **Составные слои** »  
:::image-end:::  

## Определение переменных CSS на панели «Стили»  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

В области **стили** [CSS переменные][MdnUsingCssCustomProperties] теперь прямо связываются с каждым определением.  Выберите переменную, чтобы легко просмотреть или изменить определение переменной CSS.  В примере DevTools отображает атрибуты CSS для `body` элемента.  Чтобы отобразить определение переменной `--theme-body-background` CSS, выполните указанные ниже действия.  

1.  В области **стили** выберите `var(--theme-body-background)` .  
1.  В области " **стили** " теперь отображается определение `--theme-body-background` переменной CSS.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Переменная CSS, связанная с этим стилем" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Переменная CSS, связанная с этим стилем  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Переменная CSS, связанная с целевым объектом стиля" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Переменная CSS, связанная с целевым объектом стиля  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Улучшения в отладке рабочих процессов служб  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Ниже перечислены новые возможности средств " [сеть](#network-tool)", " [приложение](#application-tool)" и " [источники](#sources-tool) ", которые помогут вам создать [PWA][ProgressiveWebAppsChromiumIndex].  Если у вас возникли проблемы при отладке вашего сотрудника службы, используйте следующие функции.  

В маршруте запроса отображаются `startup` события и данные, `fetch` основанные на запросах в сети, которые выполняются сотрудниками службы.  Доступ к временной шкале осуществляется с помощью средства " **приложение** " или " **сеть** ".  Временные шкалы помогают вам при возникновении проблем с сотрудниками служб, которые хотят проверить, не возникло ли что-то с `startup` `fetch` событием.  

### Инструмент "приложение"  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Просмотреть все сведения о маршруте запроса на обслуживание с помощью новой ссылки " **сетевые запросы** ".  Чтобы отобразить дополнительный контекст при отладке рабочего процесса службы, выполните указанные ниже действия.  

1.  Перейдите к ****  >  **сотрудникам службы**приложений.  
1.  Выберите **сетевые запросы**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Инструмент "открыть сеть" из области "работники службы"" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Инструмент "открыть **сеть** " из области " **работники службы** "
    :::image-end:::  
    
1.  В **ящике** откроется средство " **сеть** ", в котором выводятся все сетевые запросы, связанные с сотрудниками служб.  Сетевые запросы фильтруются с использованием `is:service-worker-intercepted` .  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Инструмент "сеть" в ящике" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Инструмент " **сеть** " в **ящике**  
    :::image-end:::
    
1. Чтобы вернуть инструмент **Network (сеть** ) на верхнюю панель, закройте **денежный ящик**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Закройте денежный ящик, чтобы вернуть сетевое средство" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Закройте **денежный ящик** , чтобы вернуть **Сетевое** средство  
    :::image-end:::  
    
### Инструмент "сеть"  

Сетевые запросы на отладку, которые выполняются сотрудниками службы;  Кроме того, вы можете открывать сетевые запросы из средства **приложения** .  Для каждого запроса DevTools отобразить следующие сведения в области [временных интервалов][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .  

*   Начало запроса и продолжительность начальной загрузки.  
*   Изменения регистрации рабочих процессов служб.  
*   Среда выполнения `fetch` обработчика событий.  
*   Среда выполнения всех событий, возникающих `fetch` при загрузке клиента.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Область временных интервалов" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Область **временных интервалов**  
:::image-end:::  

### Инструмент «источники»  

В предыдущих версиях Microsoft Edge уровень глубины в стеке вызовов ограничен кодом JavaScript в сервисном рабочем процессе.  В Microsoft Edge 88 в стеке вызовов теперь отображаются инициаторы запросов, которые выполняются в рамках вашего сотрудника службы.  

Чтобы найти инициатора запроса, используйте стек вызовов вашего кода JavaScript в сервисном рабочем процессе.  Стек вызовов на приведенных ниже рисунках начинается с кода JavaScript в рабочем процессе и отображает ссылку на первоначальное приглашение на веб-страницу `(index):157` .  На втором рисунке показано, как выбрать ссылку и открыть инициатор, который сделал запрос.  Инициатор на втором рисунке — это веб-страница.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Создатель запроса, который выделит service-worker.js файл и стек вызовов" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         `service-worker.js`Инициатор запроса, выделяя файл и стек вызовов  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Веб-страница указателя является инициатором запроса" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         `(index)`Веб-страница является инициатором запроса  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Копирование значения свойства сетевого запроса  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

В средстве **Network (сеть** ) скопируйте значение свойства сетевого запроса с помощью нового параметра **Копировать значение** .  Значение свойства копируется как декодированное значение JSON.  В предыдущих версиях Microsoft Edge пришло время скопировать значение с помощью одного из указанных ниже действий.  

*   Выделит весь текст и скопируйте его.  
*   Сохраните значение как глобальную переменную, если это применимо, и скопируйте ее из [консоли][DevtoolsConsoleIndex]DevTools.  
    
Чтобы скопировать значение свойства в буфер обмена, перейдите в [буфер обмена, чтобы скопировать отформатированный JSON ответа][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Копирование значения свойства в DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Копирование значения свойства в DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Вставка значения свойства в код Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Вставка значения свойства в код Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Настройка сочетаний клавиш с несколькими нажатиями клавиш  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Поскольку Microsoft Edge версии 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], вы можете настроить сочетания клавиш для любых действий в DevTools.  В Microsoft Edge версии 88 вы можете создать несколько сочетаний клавиш.  Чтобы задать сочетание клавиш для действия в DevTools, перейдите в раздел [][DevtoolsCustomizeIndexSettings]  >  **эксперименты** с параметрами и установите флажок **включить редактор сочетаний клавиш**.  Дополнительные сведения о настройке и редактировании сочетаний клавиш можно найти в статье [включить режим экспериментального редактора сочетаних][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]клавиш.  

Например, красная подсветка отображает сочетание клавиш для нескольких нажатий, настроенное для действия " **начать запись событий** ".  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к [вопросу #174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Сочетания клавиш для аккордов" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Сочетания клавиш для нескольких клавиш  
:::image-end:::  

## Объявления из проекта Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Новые инструменты визуализации для угла CSS  

DevTools теперь имеет улучшенную поддержку отладки для углов CSS.  Если к элементу HTML на странице применен угол CSS, рядом с углом в инструменте " **стили** " отображается значок "Часы".  Чтобы включить или выключить наложение часов, щелкните значок часы.  Чтобы изменить угол, выберите любое место в часах или перетащите поле стрелки.  Для изменения значения угла вы также можете использовать клавиши мыши и сочетания клавиш.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1126178][CR1126178] и [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

Для этого примера используется следующий угол CSS.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Угол CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Угол CSS  
:::image-end:::  

### Имитация размера квоты хранилища в области "хранилище"  

Теперь вы можете переопределить размер квоты хранилища в области **хранения** .  Эта функция позволяет моделировать различные устройства и тестировать работу вашего веб-сайта или приложения в сценариях недостаточной доступности диска.  Чтобы смоделировать квоту хранилища, выполните указанные ниже действия.  

1.  Перейдите в **** раздел  >  **хранилище**приложений.  
1.  Включите флажок **Эмуляция настраиваемой квоты хранилища** .  
1.  Введите допустимое число.  
    
Дополнительные сведения о том, как эмулировать мобильные устройства и другие функции в DevTools, можно найти в [разделе Эмуляция мобильных устройств в Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [945786][CR945786] и [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Имитация размера квоты хранилища" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Имитация размера квоты хранилища  
:::image-end:::  

### Ошибки при составлении отчета CORS в инструменте "сеть"  

Ознакомьтесь с этой функцией, перейдя в [демонстрацию ошибки CORS][GlitchCorsErrors].  Откройте средство **Network (сеть** ), обновите страницу и просмотрите ошибочный запрос CORS Network.  В столбце status отображается **Ошибка CORS**.  При наведении указателя мыши на ошибку появляется подсказка с кодом ошибки.  В Microsoft Edge версии 87 и более ранних версий DevTools только что выводит общее состояние ошибки CORS **(сбой)** .  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Ошибки CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Ошибки CORS  
:::image-end:::  

### Обновления представления "сведения о кадрах"  

#### Сведения о межисточниковой изоляции в представлении сведений о кадре  

Изолированное состояние "перекрестный источник" теперь отображается в разделе **изоляция & безопасности** .  В разделе новый **доступ к API** отображаются сведения о доступности `SharedArrayBuffer` s \ (SAB \) и о том, можно ли совместно использовать буферы `postMessage()` .  Предупреждение об устаревании отображается, если свойство SAB и в `postMessage()` настоящее время доступно, но контекст не является зависимым от других источников.  Чтобы получить дополнительные сведения о межисточниковой изоляции и о том, что необходимо для таких функций `SharedArrayBuffers` , перейдите на сайт [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Чтобы просмотреть обновления в режиме реального времени в проекте Open-Source Chromium, перейдите к вопросу [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Сведения о разных источниках" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Сведения о разных источниках  
:::image-end:::  

#### Новые сведения о веб-сотрудниках в представлении "сведения о кадре"  

Теперь DevTools организует веб-рабочие процессы в соответствующем родительском фрейме.  Например, если `someName` рамка создана `worker.js` , в `worker.js` `someName` списке **кадры** появится надпись.  Чтобы просмотреть сведения о веб-сотруднике, выполните указанные ниже действия.  

1.  Откройте средство " **приложение** ".  
1.  Разверните рамку, содержащую веб-сотрудников.  
1.  Разверните дерево " **сотрудники** ".  
1.  Выберите работника.  
    
Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1122507][CR1122507] и [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Сведения о веб-работниках" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Сведения о веб-работниках  
:::image-end:::  

#### Отображение сведений о кадре opener для открытых окон  

DevTools теперь упорядочивает открытые [окна][MdnWindowConstructors] под соответствующим родительским [кадром][MdnWindowFrames].  Например, если при `top` открытии кадра в поле `Window` "Кому" появится надпись `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` `Window` `top` в списке **рамок** .  

Чтобы отобразить кадр, ответственный за открытие другого окна в инструменте " **элементы** ", выполните указанные ниже действия.  

1.  Откройте дерево **рамок** .  
1.  Разверните **открытые окна** и выберите `Window` родительский фрейм, который вы хотите узнать.  
1.  Щелкните ссылку **рамка opener** .  

Отображаются сведения о том, какой кадр вызвал открытие другого `Window` .  Чтобы открыть opener в инструменте **элементы** , выполните указанные ниже действия.  

1.  Откройте дерево **рамок** .  
1.  Выберите открытое окно, чтобы открыть `Window` подробные сведения.  
1.  Щелкните ссылку **рамка opener** .  
    
Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Сведения об открытых кадрах" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Сведения об открытых кадрах  
:::image-end:::  

### Копирование StackTrace для инициатора сети  

Чтобы скопировать StackTrace в буфер обмена, выполните указанные ниже действия.  

1.  Откройте контекстное меню, щелкнув правой кнопкой мыши.  
1.  Нажмите кнопку **Копировать**/скопировать  >  **StackTrace**.  
    
Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Копирование StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Копирование StackTrace  
:::image-end:::  

### Предварительный просмотр значения переменной Wasm на onmouseover  

Используйте эту функцию для проверки значения переменной Assembly \ (Wasm \) при приостановке кода.  Для отображения текущего значения переменной наведите указатель мыши на переменную.  Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1058836][CR1058836] и [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Предварительный просмотр переменной Wasm на onmouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Предварительный просмотр переменной Wasm на onmouseover  
:::image-end:::  

### Единые единицы измерения для размеров файлов и памяти  

DevTools теперь постоянно используется `kB` для отображения размеров файлов и памяти.  Ранее DevTools смешанный `kB` и `KiB` .

*   `kB` или КБ \ (10 ^ 3 или 1000 байт \)  
*   `KiB` или kibibyte \ (2 ^ 10 или 1024 байт \)  
    
Например, **Сетевое** средство, ранее использованное `kB` в этикетках, которое использовалось для `KiB` вычислений.  Ваше мнение показало, что эта несогласованность привела к путанице.  Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1035309][CR1035309].  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете операционную систему Windows, Linux или macOS, в качестве браузера разработки по умолчанию рекомендуется использовать [каналы предварительного просмотра Microsoft Edge] [MicrosoftEdgePreviewChannels].  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

## Знакомство с Microsoft Edge DevTools Team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Трехмерный вид | Документы Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Обзор консоли | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор сочетаний клавиш — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Включение составных слоев в режиме трехмерной графики — экспериментальные функции | Документы Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Копирование отформатированного ответа JSON в буфер обмена — Справка по анализу сети | Документы Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Просмотр разбиения по времени для запроса на анализ сети | Документы Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Использование Chromium для проверки автоматизации тестов Документы Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Настройка сочетаний клавиш в окне "Параметры" — новые возможности DevTools (Microsoft Edge 87) | Документы Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "отзыв о веб-подсказках на панели "вопросы" — новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачать "|" Разработчик Майкрософт"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Скачайте каналы предварительной оценки Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "Ошибка 174309: DevTools: разрешить настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"  
[CR945786]: https://crbug.com/945786 "Ошибка 945786: DevTools: разрешить переопределение навигатора. Storage. Оценка () | Ошибки Chromium"  
[CR1029427]: https://crbug.com/1029427 "Ошибка 1029427: сократите нагрузку на передачу сообщений протокола в интерфейсе | Ошибки Chromium"  
[CR1035309]: https://crbug.com/1035309 "Дата_выпуска 1035309: DevTools должен постоянно использовать для обозначения мегабайта (МБ), а не mebibyte | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1058836]: https://crbug.com/1058836 "Проблема 1058836: проблемы с UX при отладке Wasm | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Вопрос 1071432: ☂️ Wasm Basic Developer | Ошибки Chromium"  
[CR1107766]: https://crbug.com/1107766 "Ошибка 1107766: отображает сведения о кадрах, созданных с помощью "Window. Open ()" в дереве кадров | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Ошибка 1122507: сведения о сотруднике Surface в представлении дерева кадров | Ошибки Chromium"  
[CR1126178]: https://crbug.com/1126178 "Ошибка 1126178: ☂ DevTools: CSS <Type> Components | Ошибки Chromium"  
[CR1130556]: https://crbug.com/1130556 "Ошибка 1130556: DevTools: Проверка резервных изображений (эмуляция) | Ошибки Chromium"  
[CR1132084]: https://crbug.com/1132084 "Ошибка 1132084: простой способ скопировать полезные данные запроса JSON | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ошибка 1136394: средство управления подсказкой | Ошибки Chromium"  
[CR1138633]: https://crbug.com/1138633 "Ошибка 1138633: DevTools: CSS <Angle> компонент должен отражать его внешний вид свойства в фоновом режиме "Часы" | Ошибки Chromium"  
[CR1139615]: https://crbug.com/1139615 "Ошибка 1139615: инициатору сети следует предоставить возможность копировать трассировку стека | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Ошибка 1139899: создание отчета о доступности с ИНТЕРФЕЙСом в режиме "сведения о кадре" | Ошибки Chromium"  
[CR1139945]: https://crbug.com/1139945 "Вопрос 1139945: значки свойств CSS для подэлементного бокса на панели «Стили» | Ошибки Chromium"  
[CR1141824]: https://crbug.com/1141824 "Ошибка 1141824: ускорение работы с отчетами об ошибках CORS в DevTools | Ошибки Chromium"  
[CR1144090]: https://crbug.com/1144090 "Ошибка 1144090: Добавление графических элементов стиля Flex в дерево Elements | Ошибки Chromium"  
[CR1146985]: https://crbug.com/1146985 "Проблема 1146985: очищенный текст по-прежнему отображается в текстовом поле в разделе "хранилище" окна "средства разработки" | Ошибки Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Ошибки CORS | Цепь"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Общий доступ к ресурсам через источник (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Использование настраиваемых свойств CSS (переменных) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Конструкторы — окно | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "Подсказка"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Специальные возможности | Подсказка"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Совместимость | Подсказка"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Производительность | Подсказка"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Ловушки | Подсказка"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Подсказка"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Безопасность | Подсказка"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/11/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
