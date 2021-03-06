---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска способов ускорения загрузки веб-сайтов.
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7de97ab27528e89e2373e0a0d1002e8c86e37613
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398114"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a>Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools  

## <a name="goal-of-tutorial"></a>Цель учебника  

В этом руководстве рассказывается о том, как использовать Microsoft Edge DevTools для поиска способов ускорения загрузки веб-сайтов.  

## <a name="prerequisites"></a>Предварительные условия  

*   Вы должны иметь базовый опыт веб-разработки, аналогичный тому, что преподается в этом классе ["Введение в веб-разработку".][CourseraIntroductionWebDevelopmentClass]  
*   Вам не нужно ничего знать о производительности нагрузки.  Об этом вы узнаете в этом руководстве.  

## <a name="introduction"></a>Введение  

Это Тони.  Тони очень известен в кошачьем обществе.  Он создал веб-сайт, чтобы его поклонники могли узнать о его любимых продуктах.  Его поклонники любят сайт, но Тони продолжает слышать жалобы, что сайт загружается медленно.  Тони попросил вас помочь ему ускорить сайт.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony the cat" lightbox="../media/speed-tony.msft.png":::
   Tony the cat  
:::image-end:::  

## <a name="step-1-audit-the-site"></a>Шаг 1. Аудит сайта  

Всякий раз, когда вы затеяли повышение производительности загрузки сайта, **всегда начните с аудита.**  
Аудит имеет 2 важных функции:  

*   Он создает **базовый уровень** для измерения последующих изменений.  
*   Это дает вам **полезные советы** о том, какие изменения оказывают наибольшее влияние.  
    
### <a name="set-up"></a>Настройка  

Сначала необходимо настроить сайт, чтобы можно было внести изменения в него позже.  

1.  [Откройте исходный код сайта](https://glitch.com/edit/#!/tony).  Эта вкладка называется вкладка **редактора**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Вкладка редактора" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       Вкладка **редактора**  
    :::image-end:::  
    
1.  Выберите **Тони**.  Появляется меню.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Меню, которое появляется после выбора Тони" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Меню, которое появляется после выбора **Тони**  
    :::image-end:::  
    
1.  Выберите **Проект Remix**.  Имя проекта изменяется с **тони** на какое-то случайным образом созданным именем.  Теперь у вас есть собственная редактируемая копия кода.  Позже вы можете внести изменения в этот код.  
1.  Выберите **Показать** и **выбрать в новом окне**.  Демонстрация открывается на новой вкладке.  Эта вкладка называется вкладка **демо.**  Загрузка сайта может занять некоторое время.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Вкладка демонстрации" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Вкладка демонстрации  
    :::image-end:::  
    
1.  Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).  Microsoft Edge DevTools открывается рядом с демонстрацией.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools и демо" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools и демо  
    :::image-end:::  
    
Для остальных скриншотов в этом руководстве DevTools отображается в отдельном окне.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\) `Undock` **** для открытия командного меню, ввода и выбора Undock в отдельное окно.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Неохватанные DevTools" lightbox="../media/speed-console.msft.png":::
   Неохватанные DevTools  
:::image-end:::  

### <a name="establish-a-baseline"></a>Создание базового плана  

Базовая запись о том, как сайт выполнялся, прежде чем вы сделали какие-либо улучшения производительности.  

1.  Выберите средство **аудита.**  Она может быть скрыта за кнопкой **More Panels** ![ \( More Panels ][ImageMorePanelsIcon] \) .  На этой панели есть маяк, так как проект, который имеет полномочия панели аудитов, называется **Маяк.**  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Средство аудита" lightbox="../media/speed-audits-performance.msft.png":::
       Средство **аудита**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Параметры конфигурации аудита совпадают с настройками предыдущего рисунка.  Вот объяснение различных вариантов:  
    
    *   **Устройство**.  Set to **Mobile** изменяет строку агента пользователя и имитирует мобильный видпорт.  Установите для **настольного** компьютера в значительной степени просто отключит **мобильные** изменения.  
    *   **Аудиты**.  Отключите категорию, чтобы группа **аудитов** не проводила эти аудиты, и исключите эти аудиты из отчета.  Оставьте остальные категории включенными, если вы хотите отобразить типы предоставляемых рекомендаций.  Отключите категории, чтобы немного ускорить процесс аудита.  
    *   **Регулирование.**  **Задаваемых для имитации медленного 4G, 4x замедление** ЦП имитирует типичные условия просмотра на мобильном устройстве.  Она называется "смоделированная", так как панель аудита фактически не работает в процессе аудита.  Вместо этого он просто экстраполирует время загрузки страницы в условиях мобильной связи.  Параметр **Applied...,** с другой стороны, фактически обрабатывает ЦП и сеть с помощью более длительного процесса аудита.  
    *   **Clear Storage**.  Включив почтовый ящик, чтобы очистить все хранилища, связанные со страницей перед каждым аудитом.  Оставьте этот параметр, если вы хотите проверять, как посетители впервые испытывают ваш сайт.  Отключите этот параметр, если вы хотите повторить посещение.  
    
1.  Выберите **выполнить аудиты.**  Через 10-30 секунд панель **Аудита** отображает отчет о производительности сайта.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Отчет для панели аудитов производительности сайта" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Отчет для панели аудитов производительности сайта  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a>Обработка ошибок отчета  

Если вы когда-либо получили ошибку в отчете панели аудитов, попробуйте запускать вкладку демонстрации из окна **InPrivate** без открытия других вкладок.  Это гарантирует, что вы работаете Microsoft Edge из чистого состояния.  Расширение Microsoft Edge, в частности, часто вмешивается в процесс аудита.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a>Понимание отчета  

Номер в верхней части отчета — это общая оценка производительности сайта.  Позже при внесении изменений в код число отображаемого кода должно вырасти.  Более высокий балл означает лучшую производительность.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Общая оценка производительности" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Общая оценка производительности  
:::image-end:::  

В **разделе Metrics** приводится количественная оценка производительности сайта.  Каждый показатель дает представление о различных аспектах производительности.  Например, first **Contentful Paint** сообщает вам, когда содержимое сначала покрашено на экран, что является важной вехой в восприятии пользователем нагрузки страницы, в то время как **Time To Interactive** указывает точку, на которой страница отображается достаточно готова для обработки взаимодействий пользователей.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Раздел Метрик" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Раздел **Метрик**  
:::image-end:::  

Выберите выделенную кнопку торгле в следующем рисунке, чтобы отобразить описание для каждой метрики, и узнайте больше, **чтобы** прочитать документацию об этом.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Выберите выделенную кнопку toggle для расширения элементов Metrics" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Выберите выделенную кнопку toggle для расширения элементов Metrics  
:::image-end:::  

Ниже Метрики — это коллекция скриншотов, которые показывают, как выглядела страница при загрузке.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Скриншоты того, как выглядела страница при загрузке" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Скриншоты того, как выглядела страница при загрузке  
:::image-end:::  

В **разделе "Возможности"** приводится конкретный совет по повышению производительности нагрузки на этой конкретной странице.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Раздел Возможности" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Раздел **Возможности**  
:::image-end:::  

Выберите возможность узнать больше об этом.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Исключить возможность блокировки ресурсов отрисовки" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Исключить возможность блокировки ресурсов отрисовки**  
:::image-end:::  

Узнайте **больше,** чтобы отобразить документацию о том, почему важна возможность, и рекомендации по ее устранению.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Документация по возможности устранения ресурсов, блокирующих отрисовки" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Документация по возможности **устранения ресурсов, блокирующих отрисовки**  
:::image-end:::  

В **разделе Диагностика** содержится больше сведений о факторах, влияющих на время загрузки страницы.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Раздел Диагностика" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Раздел **Диагностика**  
:::image-end:::  

В **разделе Пройденные аудиты** показано, что сайт делает правильно.  Выберите для расширения раздела.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Раздел Пройденные аудиты" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Раздел **Пройденные аудиты**  
:::image-end:::  

## <a name="step-2-experiment"></a>Шаг 2. Эксперимент  

В разделе Возможности отчета о аудите вы можете получить советы по повышению производительности страницы.  В этом разделе реализуются рекомендуемые изменения в кодовую базу, аудит сайта после каждого изменения, чтобы оценить, как это влияет на скорость сайта.  

### <a name="enable-text-compression"></a>Включить сжатие текста  

В отчете говорится, что одной из главных возможностей повышения производительности страницы является предотвращение огромных сетевых полезной нагрузки.  Включение сжатия текста — это возможность повысить производительность страницы.  

Сжатие текста — это уменьшение или сжатие размера текстового файла перед отправкой его по сети.  Аналогично тому, как можно архивировать каталог перед отправкой, чтобы уменьшить размер.  

Перед тем как включить сжатие, ознакомьтесь с несколькими способами вручную проверить, сжаты ли текстовые ресурсы.  

1.  Выберите средство **Network.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Панель Network" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Средство **Network**  
    :::image-end:::  
    
1.  Выберите **значок параметра Network.**  
1.  Выберите **почтовый ящик Use Large Request Rows.**  Высота строк в таблице сетевых запросов увеличивается.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Большие строки в таблице сетевых запросов" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Большие строки в таблице сетевых запросов  
    :::image-end:::  
    
1.  Если **столбец Размер** в таблице сетевых запросов не отображается, выберите заглавную таблицу > **Размер**.  

Каждая **ячейка Size** отображает два значения.  Верхнее значение — размер загруженного ресурса.  
Нижнее значение — это размер ненапечатаемого ресурса.  Если эти два значения одинаковы, ресурс не сжимается, когда он отправляется по сети.  Например, на предыдущем рисунке верхние и нижние значения `bundle.js` для них `1.2 MB` и `1.2 MB` .  

Проверьте сжатие, проверив http-заготки ресурса:  

1.  Выберите `bundle.js` .  
1.  Выберите панель **загона.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Панель "Заготки"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Панель **"Заготки"**  
    :::image-end:::  
    
1.  Поиск раздела **Заглавные ответы** для `content-encoding` загона.  Заголовки `content-encoding` не отображаются, что означает, `bundle.js` что не было сжато.  При сжатии ресурса этот заглавный загот обычно задатки `gzip` , `deflate` или `br` .  Для объяснения значений перейдите к [Директивам.][MDNContentEncodingDirectives]  

Достаточно объяснений.  Время внести некоторые изменения.  Включить сжатие текста, добавив несколько строк кода:  

1.  На вкладке редактор выберите **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Изменение server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Edit `server.js`  
    :::image-end:::  
    
1.  Добавьте следующий код в **server.js. **  Убедитесь, что поставить `app.use(compression())` перед `app.use(express.static('build'))` .  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > Обычно, вы должны установить пакет `compression` с помощью что-то `npm i -S compression` вроде, но это уже было сделано для вас.  
    
1.  Подождите, пока глюк развернет новую сборку сайта.  Фантазия анимации рядом с **Инструменты** означает, что сайт перестроен и передиплоен.  Изменение готово, когда анимация рядом с **Инструменты** уходит.  Выберите **Показать** и **снова выбрать в новом окне.**  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие:  

1.  Возвращайся на вкладку демонстрации и обнови страницу.  Столбец **Размер** теперь должен показывать 2 различных значения для текстовых ресурсов, таких как `bundle.js` .  На рисунке ниже верхнее значение для — размер файла, отправленного по сети, а нижним значением является `256 KB` `bundle.js` ненапечатаный размер `1.2 MB` файла.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="В столбце Размер теперь показаны 2 различных значения для текстовых ресурсов" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       В **столбце Размер** теперь показаны 2 различных значения для текстовых ресурсов  
    :::image-end:::  
    
1.  Раздел **Заглавные ответы** теперь `bundle.js` должен включать `content-encoding: gzip` заглавную.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="В разделе Заглавные ответы теперь содержится заготчик коди-кодинга контента" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       В **разделе Заглавные ответы** теперь содержится заготчик коди-кодинга контента  
    :::image-end:::  
    
Проверь страницу еще раз, чтобы оценить, какое влияние оказывает сжатие текста на производительность нагрузки страницы:  

1.  Выберите средство **аудита.**  
1.  Выберите **Выполнение аудита** \. ![ Выполните аудит ][ImagePerformIcon] \).  
1.  Оставьте параметры так же, как и раньше.  
1.  Выберите **аудит Run**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Отчет аудита после включения сжатия текста" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Отчет аудита после включения сжатия текста  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  Общий показатель производительности должен был увеличиться, а это значит, что сайт становится быстрее.  

#### <a name="text-compression-in-the-real-world"></a>Сжатие текста в реальном мире  

Большинство серверов действительно имеют простые исправления, такие как это для включения сжатия!  Просто сделайте поиск о том, как настроить любой сервер, который используется для сжатия текста.  

### <a name="resize-images"></a>Resize images  

В отчете указывается, что одной из главных возможностей повышения производительности страницы является предотвращение огромных сетевых полезной нагрузки.  Размер изображений позволяет уменьшить размер полезной нагрузки сети.  Если пользователь просматривает изображения на экране мобильного устройства шириной 500 пикселей, отправка изображения шириной 1500 пикселей не имеет смысла.  В идеале вы отправляете не более 500 пикселей изображения.  

1.  В отчете выберите **Избегать огромных сетевых** полезной нагрузки для отображения изображений, которые следует повторно использовать.  Похоже, что 2 из jpg-файлов более 2000 КБ, что больше, чем необходимо.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  Возвращаясь на вкладку редактора, откройте `src/model.js` .  
1.  Замените `const dir = 'big'` `const dir = 'small'` .  Этот каталог содержит копии тех же изображений, которые были повторно размера.  
1.  Снова проверь страницу, чтобы показать, как изменение влияет на производительность нагрузки.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Отчет аудита после повторного размеров изображений" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Отчет аудита после повторного размеров изображений  
    :::image-end:::  
    
Отображаемая перемена имеет незначительное влияние на общую оценку производительности.  Однако одна вещь, которая не показывает четко, это то, сколько сетевых данных вы экономите пользователей.  Общий размер старых фотографий составил около 5,3 мегабайт, в то время как сейчас он составляет всего 0,18 мегабайта.  

#### <a name="resizing-images-in-the-real-world"></a>Размер изображений в реальном мире  

Для небольшого приложения сделать разовую размер, как это может быть достаточно хорошо.  Но для большого приложения это, очевидно, не масштабируемо.  Вот некоторые стратегии управления изображениями в крупных приложениях:  

*   Resize images during your build process.  
*   Создайте несколько размеров каждого изображения в процессе сборки и используйте `srcset` в коде.  При запуске браузер принимает решение о том, какой размер лучше всего для устройства.  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Используйте CDN изображения, который позволяет динамически реамизировать изображение при его запросе.  
*   По крайней мере, оптимизируйте каждое изображение.  Это может создать огромную экономию.  
  Оптимизация — это при запуске изображения через специальную программу, которая уменьшает размер файла изображений.  Дополнительные советы, перейдите к [существенной оптимизации изображения][EssentialImageOptimization].  
    
### <a name="eliminate-render-blocking-resources"></a>Устранение ресурсов, блокирующих рендеринг  

В последнем отчете говорится, что устранение ресурсов, блокирующих рендеринг, теперь является самой большой возможностью.  

Ресурс, блокирующий отрисовку, — это внешний файл JavaScript или CSS, который браузер должен скачать, разбрасировать и запустить до отображения страницы.  Цель состоит в том, чтобы выполнить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.  

Первой задачей является поиск кода, который не требуется запускать на странице нагрузки.  

1.  Выберите **исключить ресурсы, блокирующие отрисовки,** чтобы отобразить заблокированные ресурсы:  
    `lodash.js` и `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Дополнительные сведения о возможности устранения ресурсов, блокирующих отрисовки" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Дополнительные сведения о возможности **устранения ресурсов, блокирующих отрисовки**  
    :::image-end:::  
    
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) `Coverage` **** для открытия командного меню, начала ввода, а затем выберите Показать покрытие .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Откройте меню команд из панели Аудиты" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Откройте меню команд из панели **Аудиты**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Средство Coverage" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       Средство **Coverage**  
    :::image-end:::  
    
1.  Выберите **обновление** \. ![ Обновление ][ImageRefreshIcon] \).  Средство **Coverage** предоставляет обзор того, сколько кода в , и запускается во время `bundle.js` `jquery.js` `lodash.js` загрузки страницы.  На следующем рисунке не используется соответственно около 76% и 30% файлов jQuery и Lodash.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Отчет По охвату" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       Отчет По охвату  
    :::image-end:::  
    
1.  Выберите **строкуjquery.js.**  DevTools открывает файл в панели Источники.  Строка кода побежала, если рядом с ней имеется синяя строка.  Красная планка означает, что она не была запускаться и определенно не требуется для загрузки страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Просмотр файла jQuery в панели Источники" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Просмотр файла jQuery в панели **Источники**  
    :::image-end:::  
    
1.  Прокрутите код jQuery немного.  Некоторые строки, которые получают "запустить" на самом деле просто комментарии.  Запуск этого кода через мини-файл, который полосы комментариев является еще одним способом уменьшить размер этого файла.  

Короче говоря, при работе с собственным кодом средство **Coverage** помогает анализировать код, строку за строкой и только отгрузку кода, необходимого для загрузки страницы.  

Нужны ли файлы и файлы `jquery.js` `lodash.js` для загрузки страницы?  Средство **блокировки** запроса отображает, что происходит, когда ресурсы недоступны.  

1.  Выберите средство **Network.**  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для повторного открытия командного меню.  
1.  Начните `blocking` вводить текст, а затем **выберите блокировку запроса на показ.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Средство блокировки запроса" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       Средство **блокировки запроса**  
    :::image-end:::  
    
1.  Выберите **Добавить шаблон** \. Добавьте шаблон ![ ][ImageAddPatternIcon] \), введите , а затем `/libs/*` `Enter` выберите, чтобы подтвердить.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Добавление шаблона для блокировки любого запроса в каталог libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Добавление шаблона для блокировки любого запроса `libs` в каталог  
    :::image-end:::  
    
1.  Обновите страницу.  Запросы jQuery и Lodash являются красными, что означает, что запросы были заблокированы.   Страница по-прежнему загружается и является интерактивной, поэтому похоже, что эти ресурсы вообще не нужны!  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Панель Network показывает, что запросы были заблокированы" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       Средство **Network** показывает, что запросы заблокированы  
    :::image-end:::  
    
1.  Выберите **Удалить все шаблоны** \. Удалите все ![ шаблоны ][ImageRemoveIcon] \) для удаления `/libs/*` шаблона блокировки.  
    
Как правило, средство блокировки **запроса** полезно для моделирования поведения страницы, если какой-либо ресурс не доступен.  

Теперь удалите ссылки на эти файлы из кода и снова проверите страницу:  

1.  Возвращаясь на вкладку редактора, откройте `template.html` .  
1.  Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.  
1.  Дождись повторной сборки и повторного развертывания сайта.  
1.  Снова аудит страницы из средства **аудита.**  Ваш общий результат должен был улучшиться снова.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Отчет аудита после удаления ресурсов, блокирующих рендеринг" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Отчет **аудита** после удаления ресурсов, блокирующих рендеринг  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a>Оптимизация пути критической визуализации в реальном мире  

Путь **критической визуализации** относится к коду, необходимому для загрузки страницы.  В общем, ускорять загрузку страницы, только отгрузка критического кода во время загрузки страницы, а затем ленивая загрузка всего остального.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Маловероятно, что вы сможете найти сценарии, которые можно удалить прямо, но вы можете найти много скриптов, которые вам не нужно запрашивать во время загрузки страницы, а вместо этого может быть запротезировали асинхронно.  <!--Navigate to [Using async or defer][async].  -->  
*   Если вы используете фреймворк, проверьте, есть ли в нем режим производства.  Этот режим может использовать [][WebpackTreeShaking] такую функцию, как встряхивания дерева, чтобы исключить ненужный код, блокирующий критически важную отрисовку.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a>Меньше работы основного потока  

В последнем отчете показано некоторое незначительное потенциальное сэкономление в разделе Возможности, но если вы посмотрите вниз в разделе Диагностика, то, похоже, что самое большое узким местом является слишком большая активность основного потока.  

Основной поток — это то, что браузер делает большую часть работы, необходимой для отображения страницы, например для размыва и запуска HTML, CSS и JavaScript.  

Цель состоит в том, чтобы использовать панель Performance для анализа работы основного потока во время загрузки страницы, а также поиска способов отложить или удалить ненужные работы.  

1.  Выберите **средство Performance.**  
1.  Выберите **Параметры захвата** \. ![ Параметры захвата ][ImageCaptureIcon] \).  
1.  Установите **сеть** для **замедления 3G** и **ЦП** до **замедления 6x**.  Мобильные устройства обычно имеют больше ограничений оборудования, чем ноутбуки или настольные компьютеры, поэтому эти параметры позволяет испытывать нагрузку на страницу, как если бы вы использовали менее мощное устройство.  
1.  Выберите **обновление** \. ![ Обновление ][ImageRefreshIcon] \).  DevTools обновляет страницу, а затем создает визуализацию всей работы, выполняемой для загрузки страницы.  Эта визуализация называется **трассировка**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Трассировка средства Performance для загрузки страницы" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       **Трассировка** средства Performance для загрузки страницы  
    :::image-end:::  
    
Трассировка показывает активность в хронологическом порядке, слева направо.  Диаграммы FPS, CPU и NET в верхней части дают обзор кадров в секунду, активности ЦП и сетевой активности.  Блок желтого цвета, выделенный на рисунке после следующего, ЦП был полностью занят действиями скриптов.  Это подсказка о том, что вы можете ускорить загрузку страниц, делая меньше работы с JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Раздел Обзор трассировки" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   Раздел Обзор трассировки  
:::image-end:::  

Изучите след, чтобы найти способы сделать меньше работы JavaScript:  

1.  Чтобы расширить его, выберите раздел **Timings.**  Основываясь на том, что может быть куча мер [Timings][MDNUserTimingApi] от React, кажется, что приложение Тони использует режим разработки React.  Переход на производственный режим React может привести к некоторому простому выигрышу производительности.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Раздел Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Раздел **Timings**  
    :::image-end:::  
    
1.  Снова **выберите Тайминги,** чтобы свернуть этот раздел.  
1.  Просмотрите **раздел Main.**  В этом разделе показан хронологический журнал основной активности потока слева направо.  Y-axis (сверху вниз) показывает, почему произошли события.  Например, в figyre после следующего события, событие вызвало функцию для запуска, что вызвало запуск, что вызвало `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` запуск, и так далее.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Основной раздел" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Основной **** раздел  
    :::image-end:::  
    
1.  Прокрутите вниз в нижней части **основного** раздела.  При использовании фреймворка большая часть верхней активности вызвана рамками, которые обычно находятся вне вашего контроля.  Действие, вызываемая вашим приложением, обычно находится в нижней части.  В этом приложении кажется, что функция с именем вызывает большое количество запросов `App` для `mineBitcoin` функции.  Похоже, Тони может использовать устройства своих поклонников для майнинга криптовалюты...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Наведите курсор на действие mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Наведите курсор `mineBitcoin` на действие  
    :::image-end:::  
    
    > [!NOTE]
    > Несмотря на то, что запросы, которые делает ваша структура, обычно не под вашим контролем, иногда вы можете структурировать приложение таким образом, что это приводит к неэффективному запуску фреймворка.  Реструктуризация приложения для эффективного использования фреймворка — это способ сделать меньше основной работы потока.  Однако для этого требуется глубокое понимание того, как работает ваша структура, и какие изменения вы вносяте в собственный код для более эффективного использования фреймворка.  
    
1.  **Расширь раздел Bottom-Up.**  Эта вкладка разбивает, какие действия заняли больше всего времени.  Если в разделе Bottom-Up ничего не отображается, выберите метку для **раздела Main.**  В **разделе Bottom-Up** показаны только сведения о любых действиях или группах действий, выбранных в настоящее время.  Например, если вы выбрали одно из действий, в разделе Bottom-Up будут показываться только сведения `mineBitcoin` об этом одном действии. ****  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Вкладка Bottom-Up" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Вкладка **Bottom-Up**  
    :::image-end:::  
    
Столбец **Self Time** показывает, сколько времени было затрачено непосредственно в каждом действии.  Например, на следующую цифру было потрачено около 63% основного времени потока на `mineBitcoin` функцию.  

Время для проверки того, может ли использование режима производства и снижение активности JavaScript ускорить загрузку страницы.  Начните с режима производства:  

1.  На вкладке редактор откройте `webpack.config.js` .  
1.  Изменение `"mode":"development"` в `"mode":"production"` .  
1.  Подождите развертывание новой сборки.  
1.  Снова аудит страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Отчет аудита после настройки вебпака для использования режима производства" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Отчет аудита после настройки вебпака для использования режима производства  
    :::image-end:::  
    
Уменьшите активность JavaScript, удалив запрос `mineBitcoin` на:  

1.  На вкладке редактор откройте `src/App.jsx` .  
1.  Комментарий `this.mineBitcoin(1500)` запроса в `constructor` .  
1.  Подождите развертывание новой сборки.  
1.  Снова аудит страницы.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Отчет аудита после удаления ненужной работы JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Отчет аудита после удаления ненужной работы JavaScript  
    :::image-end:::  
    
Похоже, что последнее изменение вызвало массовый скачок производительности!  

> [!NOTE]
> В этом разделе представлено краткое введение в панель Performance.  Дополнительные данные о том, как анализировать производительность страниц, перейдите к ссылке [на анализ производительности.][DevtoolsEvaluatePerformanceReference]  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a>Работа с меньшим количеством основных потоков в реальном мире  

В общем, средство **Performance** — это наиболее распространенный способ понять, какие действия ваш сайт делает при загрузке, и найти способы удаления ненужных действий.  

Если вы предпочитаете более похожий `console.log()` подход, [API][MDNUserTimingApi] времени пользователя позволяет произвольно отмечать определенные этапы жизненного цикла приложения, чтобы отслеживать, сколько времени занимает каждый из этих этапов.  

## <a name="summary"></a>Сводка  

*   Всякий раз, когда вы затеяли оптимизацию производительности загрузки сайта, всегда начните с аудита.  Аудит устанавливает базовый уровень и дает советы по улучшению.  
*   Внося по одному изменение за раз и проверяя веб-страницу после каждого изменения, чтобы отобразить, как это изолированное изменение влияет на производительность.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Справочные ссылки | Документы Майкрософт"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Введение в класс веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Необходимая оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы — кодиро-кодиро-| MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Встряхивания | webpack"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
