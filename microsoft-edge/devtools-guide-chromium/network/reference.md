---
description: Полная ссылка на функции панели Microsoft Edge DevTools Network.
title: Ссылка на анализ сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e8e2259e0f95499519c954e2199e191382998649
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398380"
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

# <a name="network-analysis-reference"></a>Ссылка на анализ сети  

Узнайте о новых способах анализа загрузки страницы в этой комплексной ссылке на функции сетевого анализа Microsoft Edge DevTools.  

## <a name="record-network-requests"></a>Запись сетевых запросов  

По умолчанию DevTools записываю все сетевые запросы в средстве **Network,** пока DevTools открыт.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель Network" lightbox="../media/network-network-panel.msft.png":::
   Средство **Network**  
:::image-end:::  

### <a name="stop-recording-network-requests"></a>Остановка записи сетевых запросов  

Чтобы остановить запись запросов, выполните следующие действия.  

1.  В **средстве Network** выберите **Стоп запись сетевого журнала** \( Остановка ![ записи сетевого ][ImageRecordOnIcon] журнала \).  Становится серым, чтобы указать, что DevTools больше не записывает запросы.  
1.  Выберите `Control` + `E` \(Windows, Linux\) `Command` + `E` или \(macOS\) в **** то время как средство Network находится в центре внимания.  

### <a name="clear-requests"></a>Четкие запросы  

Выберите **Clear** \( Clear \) в средстве Network, чтобы очистить все ![ ][ImageClearIcon] запросы из таблицы Запросов. ****  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка Clear" lightbox="../media/network-network-clear-button.msft.png":::
   Кнопка **Clear**  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a>Сохранение запросов в разных нагрузках страниц  

Чтобы сохранить запросы во всех загрузках страниц, в средстве **Network** включите почтовый ящик **Сохранить** журнал.  DevTools сохраняет все запросы, пока не отключите **журнал Preserve.**  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Почтовый ящик Preserve Log" lightbox="../media/network-network-preserve-log.msft.png":::
   Почтовый **ящик Preserve Log**  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a>Захват скриншотов во время загрузки страницы  

Снимите скриншоты для анализа отображаемой информации для пользователей в ожидании загрузки страницы.  

Чтобы включить снимки экрана, выберите **параметры Сети**и в **инструменте Network** включим контрольный ящик **снимков** экрана захвата.  

Обновите страницу, пока средство **Network** находится в фокусе для захвата скриншотов.  

После захвата экрана вы взаимодействуете с ним следующими способами.  

*   Наведите курсор на скриншот, чтобы отобразить точку, в которой был сделан снимок экрана.  На области Обзор отображается **** желтая строка.  
*   Выберите эскиз экрана, чтобы отфильтровать все запросы, которые произошли после захвата экрана.  
*   Дважды щелкните эскиз, чтобы увеличить его.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведите курсор на скриншоте" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Наведите курсор на скриншоте  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a>Изменение поведения загрузки  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a>Эмулировать первого посетителя, отключив кэш браузера  

Чтобы подражать первому пользователю, как он работает с сайтом, включите почтовый ящик **отключения** кэша.  DevTools отключает кэш браузера.  Эта функция более точно эмулирует пользовательский опыт, так как запросы подаются из кэша браузера при повторных посещениях.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Почтовый ящик Отключение кэша" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Почтовый **ящик Отключение кэша**  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a>Отключение кэша браузера из ящика сетевых условий  

Если вы хотите отключить кэш во время работы в других панелях DevTools, используйте ящик Сетевые условия.  

1.  Откройте ящик **сетевых** условий.  
1.  Включите \(или off\) почтовый ящик **отключения** кэша.  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a>Вручную очистить кэш браузера  

Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню \(правой кнопкой мыши\) в любой точке таблицы Запросов и выберите кэш **Clear Browser.**  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор кэша "Ясный браузер"" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Выбор **кэша "Ясный браузер"**  
:::image-end:::  

### <a name="emulate-offline"></a>Эмулировать автономный режим  

Новый класс веб-приложений с именем [Progressive Web Apps (Прогрессивные веб-приложения)][DevtoolsProgressiveWebApps]функционирует в автономном режиме с помощью **сотрудников службы.**  Возможно, вам будет полезно быстро смоделировать устройство, не подключенное к данным при создании такого типа приложения.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Выберите **** меню выпадаемых данных в Интернете, поиск в **пресетах**и выберите **автономный** режим для имитации автономного сетевого подключения.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Меню отключения в автономном режиме" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Меню **отключения** в автономном режиме  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a>Эмулировать медленные сетевые подключения  

Эмулировать медленные скорости подключения 3G, Fast 3G и другие скорости подключения из меню **отсев** в Интернете.  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Меню отключения от регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   Меню **отключения** от регулирования  
:::image-end:::  

Вы можете выбрать из различных пресетов, таких как Slow 3G или Fast 3G.  Чтобы добавить собственные настраиваемые предустанавливные настройки, откройте меню регулирование и выберите **настраиваемый**  >  **добавить**.  

В DevTools рядом с средством **Network** отображается значок предупреждения, чтобы напомнить, что включено регулирование.  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a>Эмулировать медленные сетевые подключения из ящика сетевых условий  

Если вы хотите заторможить сетевое подключение во время работы в других панелях DevTools, используйте ящик сетевых условий.  

1.  Откройте ящик **сетевых** условий.  
1.  Выберите скорость подключения из меню **регулирования.**  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a>Файлы cookie браузера вручную очищают  

Чтобы вручную очистить cookie-файлы браузера в любое время, наведите курсор в любом месте таблицы Запросов, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Clear Browser Cookies**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор cookie-файлов Clear Browser" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Выбор **cookie-файлов Clear Browser**  
:::image-end:::  

### <a name="override-the-user-agent"></a>Переопределять агент пользователя  

Чтобы вручную переопредить агента пользователя, используйте следующие действия.  

1.  Откройте ящик **сетевых** условий.  
1.  Выключите **автоматический почтовый ящик Select.**  
1.  Выберите параметр агента пользователя из меню или введите настраиваемый параметр в текстовом окне.  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a>Запросы фильтрации  

### <a name="filter-requests-by-properties"></a>Фильтрация запросов по свойствам  

Используйте **текстовое** поле Filter для фильтрации запросов по свойствам, таким как домен или размер запроса.  

Если текстовое поле не отображается, возможно, будет скрыта области **Фильтры.**  
Дополнительные сведения можно получить в [области Hide the Filters.](#hide-the-filters-pane)  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле Filter" lightbox="../media/network-network-filters-textbox.msft.png":::
   Текстовое **поле Filter**  
:::image-end:::  

Вы можете использовать несколько свойств одновременно, разделив каждое свойство с пространством.  Например, отображаются все PNGs размером более `mime-type:image/png larger-than:1K` 1 килобайта.  Фильтры с несколькими свойствами эквивалентны `AND` операциям.  `OR` в настоящее время операции не поддерживаются.  

Полный список поддерживаемых свойств.  

| Свойство | Сведения |  
|:--- | :--- |  
| `domain` | Отображаются только ресурсы из указанного домена.  Вы можете использовать символ под диктовки `*` \( \) для использования нескольких доменов.  Например, `*.com` отображает ресурсы из всех доменных имен, заканчивающийся `.com` в .  DevTools заполняют меню автозапуска автокомплектов всеми найденными доменами. |  
| `has-response-header` | Отображает ресурсы, содержащие указанный заглавной ответ HTTP.  DevTools заполняют выпадаемую часть автокомплекта всеми найденными загонами ответа. |  
| `is` | Используйте `is:running` для поиска `WebSocket` ресурсов. |  
| `larger-than` | Отображает ресурсы, которые больше указанного размера, в bytes.  Установка значения `1000` эквивалентна установке значения `1k` . |  
| `method` | Отображает ресурсы, извлеченные за указанный тип метода HTTP.  DevTools заполняют отсев всеми найденными методами HTTP. |  
| `mime-type` | Отображает ресурсы определенного типа MIME.  DevTools заполняют отсев всеми найденными типами MIME. |  
| `mixed-content` | Показать все смешанные ресурсы контента \( \) или только те, которые в настоящее время `mixed-content:all` отображаются `mixed-content:displayed` \( \). |  
| `scheme` | Отображает ресурсы, извлеченные из незащищенных http\( \) или `scheme:http` защищенных HTTPS `scheme:https` \( \). |  
| `set-cookie-domain` | Отображает ресурсы с `Set-Cookie` загонами с `Domain` атрибутом, который соответствует указанному значению.  DevTools заполняют автокомплект всеми найденными доменами cookie. |  
| `set-cookie-name` | Отображает ресурсы с загонами с именем, которое соответствует `Set-Cookie` указанному значению.  DevTools заполняют автокомплект всеми найденными именами файлов cookie. |  
| `set-cookie-value` | Отображает ресурсы с загонами со значением, которое соответствует `Set-Cookie` указанному значению.  DevTools заполняют автокомплект всеми найденными значениями cookie. |  
| `status-code` | Отображает ресурсы, которые соответствуют определенному коду состояния HTTP.  DevTools заполняет меню отсева автокомплетов всеми найденными кодами состояния. |  

### <a name="filter-requests-by-type"></a>Фильтрация запросов по типу  

Чтобы фильтровать запросы по типу запроса, выберите одну из следующих кнопок в **средстве Network.**  

:::row:::
   :::column span="1":::
      **XHR**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **JS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **CSS**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Img**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Media**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Шрифт**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Doc**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **WS**  
   :::column-end:::
   :::column span="2":::
      WebSocket.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Манифест**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Other**  
   :::column-end:::
   :::column span="2":::
      Любой другой тип, не указанный в списке.  
   :::column-end:::
:::row-end:::  

Если кнопки не отображаются, области **Фильтры** могут быть скрыты.  
Дополнительные сведения можно получить в [области Hide the Filters.](#hide-the-filters-pane)  

Чтобы включить несколько фильтров типа одновременно, удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров Type для отображения ресурсов JS, CSS и Document" lightbox="../media/network-network-type-filters.msft.png":::
   Использование фильтров Type для отображения ресурсов JS, CSS и Document  
:::image-end:::  

### <a name="filter-requests-by-time"></a>Фильтрация запросов по времени  

Выберите и перетащите влево или вправо на области **Обзор,** чтобы отображать только запросы, которые были активны в течение этого срока.  Фильтр включен.  Отображается любой запрос, который был активен в течение выделенного времени.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация любых неактивных запросов на 300 мс" lightbox="../media/network-network-overview-filter.msft.png":::
   Фильтрация любых неактивных запросов на 300 мс  
:::image-end:::  

### <a name="hide-data-urls"></a>Скрыть URL-адреса данных  

[URL-адреса данных —][MDNHTTPDataURIs] это небольшие файлы, встроенные в другие документы.  Любой запрос, отображаемый в таблице Запросы, который начинается с `data:` url-адреса данных.  

Чтобы скрыть запросы, выключите почтовый **ящик Скрыть URL-адреса** данных.  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Почтовый ящик Скрыть URL-адреса данных" lightbox="../media/network-network-hide-data-urls.msft.png":::
   Почтовый **ящик Скрыть URL-адреса** данных  
:::image-end:::  

## <a name="sort-requests"></a>Сортировка запросов  

По умолчанию запросы в таблице Запросы сортироваться по времени начала, но вы можете сортировать таблицу с помощью других критериев.  

### <a name="sort-by-column"></a>Сортировка по столбцу  

Выберите заглавную часть любого столбца в запросах для сортировки запросов в этом столбце.  

### <a name="sort-by-activity-phase"></a>Сортировка по этапу действия  

Чтобы изменить сортировку запросов в Водопаде, наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\), наведите курсор на **водопад**и выберите один из следующих вариантов.  

:::row:::
   :::column span="1":::
      **Время начала**  
   :::column-end:::
   :::column span="2":::
      Первый запрос, который был инициирован, находится в верхней части.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время отклика**  
   :::column-end:::
   :::column span="2":::
      Первый запрос, который начал скачивать, находится в верхней части.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время окончания**  
   :::column-end:::
   :::column span="2":::
      Первый завершенный запрос находится в верхней части.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Общая продолжительность**  
   :::column-end:::
   :::column span="2":::
      Запрос с самыми короткими настройками подключения и запросом или ответом находится в верхней части.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Задержка**  
   :::column-end:::
   :::column span="2":::
      Запрос, который выждал самое короткое время для ответа, находится в верхней части.  
   :::column-end:::
:::row-end:::  

В этих описаниях предполагается, что каждый соответствующий параметр занимает место от самого короткого до длинного.  Выберите заглавную колонку **Водопад,** чтобы изменить порядок.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка водопада по общей продолжительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Сортировка водопада по общей продолжительности \(Светлая часть каждого бара — это время ожидания, а более темная — время загрузки bytes\)  
:::image-end:::  

## <a name="analyze-requests"></a>Анализ запросов  

До тех пор, пока DevTools открыты, он регистрит все запросы в **средстве Network.**  
Используйте панель Network для анализа запросов.  

### <a name="display-a-log-of-requests"></a>Отображение журнала запросов  

Используйте таблицу Запросы, чтобы отобразить журнал всех запросов, сделанных во время открытия DevTools.  Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите курсор на запросы.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица Запросов" lightbox="../media/network-network-requests-table.msft.png":::
   Таблица Запросов  
:::image-end:::  

В таблице Запросы по умолчанию отображаются следующие столбцы.  

:::row:::
   :::column span="1":::
      **Имя**  
   :::column-end:::
   :::column span="2":::
      Имя файла ресурса или идентификатор ресурса.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Состояние**  
   :::column-end:::
   :::column span="2":::
      Код состояния HTTP.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Тип**  
   :::column-end:::
   :::column span="2":::
      Тип MIME запрашиваемого ресурса.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Инициатор**  
   :::column-end:::
   :::column span="2":::
      Следующие объекты или процессы инициируют запросы.  
      
      *   **Parser**  Parser HTML для Microsoft Edge.  
      *   **Перенаправление**  Перенаправление HTTP.  
      *   **Сценарий**  Функция JavaScript.  
      *   **Другие**  Некоторые другие процессы или действия, например переход на страницу по ссылке или ввод URL-адреса в панели адресов.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      Совокупный размер заглавных заглавных ответов, а также тело ответа, доставленное сервером.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время**  
   :::column-end:::
   :::column span="2":::
      Общая продолжительность от начала запроса до получения окончательного byte в ответе.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Водопад](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Визуальный сбой действия для каждого запроса.  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a>Добавление или удаление столбцов  

Наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\) и выберите вариант, чтобы скрыть или показать его.  В настоящее время отображаемые параметры имеют контрольные знаки рядом с каждым элементом.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу Запросы" lightbox="../media/network-network-requests-add-column.msft.png":::
   Добавление столбца в таблицу Запросы  
:::image-end:::  

#### <a name="add-custom-columns"></a>Добавление настраиваемой колонки  

Чтобы добавить настраиваемый столбец в таблицу Запросы, наведите курсор на загон таблицы Запросы, откройте контекстное меню \(правой кнопкой мыши\) и выберите заглавные таблицы ответа **** Управление столбцами загонщиков  >  ****.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемой колонки в таблицу Запросы" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Добавление настраиваемой колонки в таблицу Запросы  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a>Отображение отношения времени запросов  

Использование водопада для отображения связей времени запросов.  
Организация водопада по умолчанию использует время начала запросов.  
Таким образом, запросы, которые находятся дальше слева, начались раньше, чем запросы, которые находятся дальше справа.  

Чтобы просмотреть различные способы сортировки водопада, перейдите к [сортировке по этапу действия.](#sort-by-activity-phase)  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец "Водопад" области Запросы" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Столбец "Водопад" области **Запросы**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <a name="display-a-preview-of-a-response-body"></a>Отображение предварительного просмотра тела отклика  

Чтобы отобразить предварительный просмотр тела отклика, используйте следующие действия.  

1.  Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.  
1.  Выберите панель **Preview.**  

Вкладка Preview в основном полезна для отображения изображений.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Панель Предварительного просмотра" lightbox="../media/network-network-resources-preview.msft.png":::
   Панель **Предварительного** просмотра  
:::image-end:::  

### <a name="display-a-response-body"></a>Отображение тела отклика  

Чтобы отобразить тело ответа на запрос, используйте следующие действия.  

1.  Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.  
1.  Выберите панель **ответа.**  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Панель ответов" lightbox="../media/network-network-resources-response.msft.png":::
   Панель **ответов**  
:::image-end:::  

### <a name="display-http-headers"></a>Отображение http-заглавок  

Чтобы отобразить данные http-header о запросе, используйте следующие действия.  

1.  Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.  
1.  Выберите **psanel headers.**  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Панель "Заготки"" lightbox="../media/network-resources-headers.msft.png":::
   Панель **"Заготки"**  
:::image-end:::  

#### <a name="display-http-header-source"></a>Отображение источника заглавной ссылки HTTP  

По умолчанию панель **headers показывает** имена загона в алфавитном порядке.  Чтобы разыграть имена заглавных http в полученном порядке, используйте следующие действия.  

1.  Откройте панель **headers** для запроса, который вас интересует.  Дополнительные сведения см. в загонах [Display HTTP.](#display-http-headers)  
1.  Выберите **источник представления**рядом с разделом Заглавка **запроса** или **заглавного ответа.**  

### <a name="display-query-string-parameters"></a>Отображение параметров строки запроса  

Чтобы отобразить параметры строки запроса URL-адреса в читаемом для человека формате, используйте следующие действия.  

1.  Откройте панель **headers** для запроса, который вас интересует.  Дополнительные сведения см. в загонах [Display HTTP.](#display-http-headers)  
1.  Перейдите к **разделу Параметры строки запроса.**  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел Параметры строки запроса" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Раздел **Параметры строки запроса**  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a>Отображение источника параметров строки запроса  

Чтобы отобразить источник параметров строки запроса, используйте следующие действия.  

1.  Перейдите к разделу Параметры строки запроса.  Дополнительные сведения перейдите к [параметрам строки отображения запроса.](#display-query-string-parameters)  
1.  Выберите **источник представления**.  

#### <a name="display-url-encoded-query-string-parameters"></a>Отображение параметров строки строки запроса с кодом URL-адресов  

Чтобы отобразить параметры строки запроса в читаемом для человека формате, но с сохраненными кодированием, используйте следующие действия.  

1.  Перейдите к разделу Параметры строки запроса.  Дополнительные сведения перейдите к [параметрам строки отображения запроса.](#display-query-string-parameters)  
1.  Выберите **закодированный URL-адрес просмотра.**  

### <a name="display-cookies"></a>Отображение файлов cookie  

Чтобы отобразить файлы cookie, отправленные в http-header запроса, используйте следующие действия.  

1.  Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.  
1.  Выберите панель **cookies.**  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Панель cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   Панель cookies  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a>Отображение разбивки по времени запроса  

Чтобы отобразить разбивку по времени запроса, используйте следующие действия.  

1.  Выберите URL-адрес запроса в столбце **Имя** таблицы Запросов.  
1.  Выберите панель **Timing.**  

Чтобы быстрее получить доступ к данным, перейдите к [предварительному просмотру разбивки по времени.](#preview-a-timing-breakdown)  

Дополнительные сведения о каждом из этапов, которые могут отображаться в панели **Timing,** перейдите к этапам разбивки [синхронизации.](#timing-breakdown-phases-explained)  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Панель синхронизации" lightbox="../media/network-network-resources-timing.msft.png":::
   Панель **синхронизации**  
:::image-end:::  

Дополнительные сведения о каждом из этапов.  

Дополнительные сведения о доступе к дисплею перейдите к [разбивке по времени отображения.](#display-the-timing-breakdown-of-a-request)  

#### <a name="preview-a-timing-breakdown"></a>Предварительный просмотр разбивки по времени  

Чтобы отобразить предварительный просмотр разбивки времени запроса, в столбце **Водопад** таблицы Запросов наведите курсор на запись для запроса.  

Дополнительные сведения о том, как получить доступ к данным без нависания, перейдите к отображения разбивки по времени [запроса](#display-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбивки по времени запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Просмотр разбивки по времени запроса  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a>Объяснены этапы разбивки по времени  

Дополнительные сведения о каждом из этапов, которые могут отображаться в панели **Timing.**  

:::row:::
   :::column span="1":::
      **Очередь**  
   :::column-end:::
   :::column span="2":::
      В очередях браузера запрашиваются запросы, если любое из следующих запросов является верным.  
      
      *   Существуют запросы на более высокий приоритет.  
      *   Шесть подключений TCP открыты для одного и того же происхождения, что является ограничением.  Применяется только к HTTP/1.0 и HTTP/1.1.  
      *   Браузер ненадолго размешает пространство в кэше диска.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Приостановка**  
   :::column-end:::
   :::column span="2":::
      Запрос застопоряется по любой из причин, описанных в **очереди.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **DNS Lookup**  
   :::column-end:::
   :::column span="2":::
      Браузер решает IP-адрес запроса.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Начальное подключение**  
   :::column-end:::
   :::column span="2":::
      Браузер устанавливает подключение, включая рукопожатия TCP, TCP-инслементы и переговоры по безопасному слою socket.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Согласование прокси**  
   :::column-end:::
   :::column span="2":::
      Браузер ведет переговоры по запросу с [прокси-сервером.][WikiProxyServer]  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Отправленный запрос**  
   :::column-end:::
   :::column span="2":::
      Запрос отправляется.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Подготовка serviceWorker**  
   :::column-end:::
   :::column span="2":::
      Браузер начинает рабочий службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Запрос в ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Запрос отправляется работнику службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Ожидание \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      Браузер ожидает первого byte ответа.  TTFB означает "Время для первого byte".  Это время включает одну поездку в конец задержки и время, необходимое серверу для подготовки ответа.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Загрузка контента**  
   :::column-end:::
   :::column span="2":::
      Браузер получает ответ.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Получение push**  
   :::column-end:::
   :::column span="2":::
      Браузер получает данные для этого ответа с помощью http/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Чтение Push**  
   :::column-end:::
   :::column span="2":::
      Браузер читает полученные ранее локальные данные.  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a>Отображение инициаторов и зависимостей  

Чтобы отобразить инициаторов и зависимостей запроса, удерживайте и наведите курсор на запрос `Shift` в таблице Запросы.  Цвета DevTools: инициаторы показаны зеленым цветом, а зависимости — красным.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Отображение инициаторов и зависимостей запроса  
:::image-end:::  

Если таблица Запросов задается в хронологическом порядке, если вы наведите курсор на строку, в строке, предшествуемой этой строке, отображается зеленый запрос.  Зеленый запрос является инициатором зависимости.  Если еще один зеленый запрос отображается на строке до этого, этот более высокий запрос является инициатором инициатора.  И так далее.  

### <a name="display-load-events"></a>Отображение событий загрузки  

DevTools отображает время событий и событий в нескольких `DOMContentLoaded` `load` местах в **средстве Network.**  Событие `DOMContentLoaded` имеет синий цвет, а событие — `load` красный.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и загрузки на панели Network" lightbox="../media/network-network-requests-load-events.msft.png":::
   Расположение и события `DOMContentLoaded` `load` в средстве **Network**  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a>Отображение общего числа запросов  

Общее число запросов перечислены в области **Сводка** в нижней части **средства Network.**  

> [!CAUTION]
> Это число отслеживает только запросы, которые были зарегистрированы с момента открытия DevTools.  Если другие запросы происходили до открытия DevTools, эти запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее число запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Общее число запросов с момента открытия DevTools  
:::image-end:::  

### <a name="display-the-total-download-size"></a>Отображение общего размера загрузки  

Общий размер запросов скачивания указан в области **Сводка** в нижней части **средства Network.**  

> [!CAUTION]
> Это число отслеживает только запросы, которые были зарегистрированы с момента открытия DevTools.  Если другие запросы произошли до открытия DevTools, предыдущие запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий размер запросов загрузки" lightbox="../media/network-network-total-download-size.msft.png":::
   Общий размер запросов загрузки  
:::image-end:::  

Чтобы проверить, насколько большие ресурсы после того, как браузер отпечатает каждый элемент, перейдите, чтобы отобразить ненапечатаный [размер ресурса.](#display-the-uncompressed-size-of-a-resource)  

### <a name="display-the-stack-trace-that-caused-a-request"></a>Отображение трассировки стека, вызываемой запросом  

После запроса ресурса в заявлении JavaScript наведите курсор на столбец Инициатор, чтобы отобразить след стека, ведущий к запросу. ****  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="След стека, ведущий к запросу ресурса" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   След стека, ведущий к запросу ресурса  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a>Отображение неконтпрессивного размера ресурса  

Включив **почтовый ящик Use large request rows,** а затем просмотрите нижнее значение столбца **Size.**  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример uncompressed resources" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Пример некомпрессивных ресурсов \(Сжатый размер файла, отправленного по сети, был , в то время как некомпрессованный размер `jquery-3.3.1.min.js` `29.9 KB` был `84.9 KB` \)  
:::image-end:::  

## <a name="export-requests-data"></a>Экспорт запросов данных  

### <a name="save-all-network-requests-to-a-har-file"></a>Сохранение всех сетевых запросов в файл HAR  

Чтобы сохранить все сетевые запросы в файл HAR, выполните следующие действия.  

1.  Наведите курсор на любой запрос в таблице Запросы и откройте контекстное меню \(правой кнопкой мыши\).  
1.  Выберите **Сохранить как HAR с контентом**.  DevTools сохраняет все запросы, которые произошли с момента открытия DevTools для файла HAR.  Вы не можете фильтровать запросы.  Вы также не можете сохранить один запрос.  

После сохранения файла HAR вы можете импортировать его обратно в DevTools для анализа.  Просто перетащите и сбросите файл HAR в таблицу Запросы.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выберите Сохранить как HAR с контентом" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Выберите **Сохранить как HAR с контентом**  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a>Скопируйте один или несколько запросов в буфер обмена  

В **столбце Имя** таблицы Запросы наведите курсор на запрос, откройте контекстное меню \(правой кнопкой мыши\), наведите курсор на **копию**и выберите один из следующих параметров.  

| Название | Подробные сведения |  
|:--- |:--- |  
| **Адрес ссылки копирования** | Скопируйте URL-адрес запроса в буфер обмена. |  
| **Копирование ответа** | Скопируйте текст ответа на буфер обмена. |  
| **Скопируйте как fetch** | &nbsp; |  
| **Скопируйте как cURL** | Скопируйте запрос в качестве команды cURL. |  
| **Скопируйте все как fetch** | &nbsp; |  
| **Скопируйте все как cURL** | Скопируйте все запросы в виде цепочки команд cURL. |  
| **Скопируйте все как HAR** | Скопируйте все запросы в виде данных HAR. |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор ответа на копирование" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Выбор **ответа на копирование**  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a>Скопируйте форматированный ответ JSON на буфер обмена  

Выберите сетевой запрос и перейдите на области **headers.**  Чтобы скопировать значение JSON ответа, **** перейдите на запрос полезной нагрузки, наведите курсор на содержимое отклика JSON, откройте контекстное меню \(правой кнопкой мыши\) и выберите значение **Copy Value**.  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Скопируйте значение в контекстной меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Скопируйте значение** в контекстной меню  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Код Visual Studio Microsoft с форматированный ответ JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          Вклеить форматированный ответ JSON в Microsoft Visual Studio Code  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a>Копирование значений свойств из сетевых запросов в буфер обмена  

Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните следующие действия.  

1.  Откройте области **заготки.**  
1.  Откройте один из следующих разделов загона.  
    *   Запрос полезной нагрузки \(JSON\)  
    *   Данные форм  
    *   Параметры строки запроса  
    *   Запрашивать заглавные  
    *   Заготчики ответа  
1.  Откройте контекстное меню \(правой кнопкой мыши\) > **значение Copy**.  Теперь вы можете вклеить значение в любой редактор, чтобы просмотреть его.  
    
## <a name="change-the-layout-of-the-network-panel"></a>Изменение макета панели Network  

Вы можете расширить или обвалить **разделы** пользовательского интерфейса сетевых инструментов, чтобы сосредоточиться на важных сведениях.  

### <a name="hide-the-filters-pane"></a>Скрыть области фильтров  

По умолчанию в DevTools покажут **области фильтров.**  
Выберите **фильтр** \( ![ Фильтр ][ImageFilterIcon] \) для его сокрытия.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка "Скрыть фильтры"" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Кнопка "Скрыть фильтры"  
:::image-end:::  

### <a name="use-large-request-rows"></a>Использование больших строк запросов  

Используйте большие строки, если в таблице сетевых запросов нужно больше белого пространства.  Некоторые столбцы также предоставляют дополнительные сведения при использовании больших строк.  Например, нижнее значение столбца **Size** — это ненапечатаный размер запроса.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример больших строк запросов в области Запросы" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Пример больших строк запросов в области **Запросы**  
:::image-end:::  

Чтобы включить большие строки, включим почтовый ящик **Use large request rows.**  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Почтовый ящик Use large request rows" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Почтовый **ящик Use large request rows**  
:::image-end:::  

### <a name="hide-the-overview-pane"></a>Скрыть области Обзор  

По умолчанию в DevTools отображается области **Обзор.**  Чтобы скрыть это, выключите **контрольный ящик "Обзор** шоу".  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Контрольный ящик "Обзор шоу"" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Контрольный **ящик "Обзор** шоу"  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Отламывка прогрессивных веб-приложений | Документы Майкрософт"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
