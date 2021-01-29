---
description: Полная справка по функциям панели Сети Microsoft Edge DevTools.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c600197ffa0e415fe42aecc704a523d1b23f8260
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230756"
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

# Справочник по анализу сети  

Узнайте о новых способах анализа загрузки страницы в этой комплексной ссылке на функции анализа сети Microsoft Edge DevTools.  

## Запись сетевых запросов  

По умолчанию DevTools записи все **** сетевые запросы в области сети, если DevTools открыт.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель Сеть" lightbox="../media/network-network-panel.msft.png":::
   Панель **"Сеть"**  
:::image-end:::  

### Остановка записи сетевых запросов  

Чтобы остановить запись запросов, выполните следующие действия.  

1.  On the **Network** panel, choose **Stop recording network log** \( Stop recording network log ![ ][ImageRecordOnIcon] \).  Серый цвет означает, что DevTools больше не записывает запросы.  
1.  Выберите `Control` + `E` \(Windows, Linux\) или `Command` + `E` \(macOS\) в **** то время как панель сети находится в фокусе.  

### Очистка запросов  

Choose **Clear** \( ![ Clear ][ImageClearIcon] \) on the **Network** panel to clear all requests from the Requests table.  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка Очистить" lightbox="../media/network-network-clear-button.msft.png":::
   Кнопка **"Очистить"**  
:::image-end:::  

### Сохранение запросов во время загрузки страницы  

Чтобы сохранить запросы между загрузками **** страниц, на панели "Сеть" включите для журнала сохранения. ****  DevTools сохраняет все запросы, пока вы не отключите журнал **сохранения.**  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="The Preserve Log checkbox" lightbox="../media/network-network-preserve-log.msft.png":::
   The **Preserve Log** checkbox  
:::image-end:::  

### Снимки экрана во время загрузки страницы  

Снимите снимки экрана, чтобы проанализировать отображаемую информацию для пользователей в ожидании загрузки страницы.  

Чтобы включить снимки экрана, выберите **"Параметры** **сети"** **** и на панели "Сеть" включит этот параметр.  

Обновите **страницу,** пока панель "Сеть" находится в фокусе для снимка экрана.  

После захвата снимка экрана вы взаимодействуете с ним следующими способами.  

*   Наведите указатель мыши на снимок экрана, чтобы отобразить точку, в которую был сделан снимок экрана.  Желтая линия отображается на области **обзора.**  
*   Выберите эскиз экрана, чтобы отфильтровать все запросы, которые произошли после снимка экрана.  
*   Дважды щелкните эскиз, чтобы увеличить его масштаб.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведите курсор на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Наведите курсор на снимок экрана  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## Изменение поведения при загрузке  

### Эмуляция первого посетителя путем отключения кэша браузера  

Чтобы эмулировать, как пользователь впервые работает с сайтом, включите этот контрольный ящик. ****  DevTools отключает кэш браузера.  Эта функция более точно эмулирует интерфейс первого пользователя, так как запросы обслуживаются из кэша браузера при повторяемом посещении.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="The Disable Cache checkbox" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   The **Disable Cache** checkbox  
:::image-end:::  

#### Отключение кэша браузера из окна "Условия сети"  

Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте ящик условий сети.  

1.  Откройте ящик **условий** сети.  
1.  Включите (или выключите\) почтовый ящик отключения **кэша.**  

<!--todo: add network condition section when available -->  

### Очистка кэша браузера вручную  

Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню \(щелкните правой кнопкой мыши\) в любом месте таблицы "Запросы" и выберите "Очистить **кэш браузера".**  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор Очистить кэш браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Выбор **"Очистить кэш браузера"**  
:::image-end:::  

### Эмуляция в автономном режиме  

Новый класс веб-приложений, с именем [Progressive Web Apps,][DevtoolsProgressiveWebApps]работает в автономном режиме с помощью **сотрудников службы.**  Может оказаться полезным быстро смоделировать устройство без подключения к данным при создании приложения такого типа.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Выберите меню **"Интернет",** найщите в меню **"Предусмотрить"** и выберите **"Автономный",** чтобы имитировать работу в автономной сети.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Автономное меню" lightbox="../media/network-network-offline-dropdown.msft.png":::
   Автономное **меню**  
:::image-end:::  

### Эмуляция медленных сетевых подключений  

Эмулировать медленную 3G, быструю 3G и другие скорости подключения из меню **"Интернет".**  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   Меню **регулирования**  
:::image-end:::  

Вы можете выбрать один из разных предугодий, например Медленную 3G или быструю 3G.  Чтобы добавить собственные настраиваемые предустанавливные таблицы, откройте меню регулирования и выберите **пункт "Добавить настраиваемую".**  >  ****  

DevTools отображает значок предупреждения **** рядом с вкладкой "Сеть", чтобы напомнить, что регулирование включено.  

#### Эмуляция медленных сетевых подключений из обоймы "Условия сети"  

Если вы хотите улажить сетевое подключение при работе на других панелях DevTools, используйте ящик условий сети.  

1.  Откройте ящик **условий** сети.  
1.  Выберите скорость подключения в меню **регулирования.**  

<!--todo: add network condition section when available -->  

### Ручная очистка файлов cookie браузера  

Чтобы вручную очистить файлы cookie браузера в любое время, наведите курсор в любом месте таблицы "Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Очистить файлы **cookie браузера".**  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выбор Очистить файлы cookie в браузере" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Выбор **"Очистить файлы cookie" в браузере**  
:::image-end:::  

### Переопределения агента пользователя  

Чтобы вручную переопрепредить агент пользователя, с помощью следующих действий.  

1.  Откройте ящик **условий** сети.  
1.  Отключите **автоматический контрольный ящик** "Выбрать".  
1.  Выберите в меню параметр агента пользователя или введите настраиваемый параметр в текстовом поле.  

<!--todo: add network condition section when available -->  

## Запросы фильтра  

### Фильтрация запросов по свойствам  

Используйте **текстовое** поле фильтра для фильтрации запросов по свойствам, таким как домен или размер запроса.  

Если текстовое поле не отображается, возможно, она скрыта. ****  
Дополнительные сведения можно найти в [области "Скрыть фильтры".](#hide-the-filters-pane)  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле фильтра" lightbox="../media/network-network-filters-textbox.msft.png":::
   Текстовое **поле фильтра**  
:::image-end:::  

Можно использовать несколько свойств одновременно, разделяя каждое свойство пробелом.  Например, `mime-type:image/png larger-than:1K` отображаются все PNG, размером более 1 килобайта.  Фильтры с несколькими свойствами эквивалентны `AND` операциям.  `OR` в настоящее время операции не поддерживаются.  

Полный список поддерживаемых свойств.  

| Свойство | Сведения |  
|:--- | :--- |  
| `domain` | Отображаются только ресурсы из указанного домена.  Чтобы включить несколько доменов, можно использовать поддиаограмму `*` \( \).  Например, `*.com` отображаются ресурсы из всех доменных имен, заканчивающийся `.com` на .  DevTools заполняет меню автозаполнеия всеми найденными доменами. |  
| `has-response-header` | Отображает ресурсы, содержащие указанный заголок HTTP-ответа.  DevTools заполнит в dropdown автозаполнеть все найденные загон ответа. |  
| `is` | Используйте `is:running` для поиска `WebSocket` ресурсов. |  
| `larger-than` | Отображает ресурсы, размером больше указанного размера, в ветвях.  Установка значения `1000` эквивалентна установке значения `1k` . |  
| `method` | Отображает ресурсы, полученные по указанному типу метода HTTP.  DevTools заполните в этом выпадаке все найденные методы HTTP. |  
| `mime-type` | Отображает ресурсы указанного типа MIME.  DevTools заполните в этом выпадаке все найденные типы MIME. |  
| `mixed-content` | Показать все ресурсы смешанного содержимого \( \) или только те, которые отображаются в настоящее время `mixed-content:all` \( `mixed-content:displayed` \). |  
| `scheme` | Отображает ресурсы, извлеченные через незащищенный HTTP \( \) или защищенный `scheme:http` HTTPS \( `scheme:https` \). |  
| `set-cookie-domain` | Отображает ресурсы с `Set-Cookie` заголковым `Domain` атрибутом, который соответствует указанному значению.  DevTools заполняет автозаполнеть всеми найденными доменами cookie. |  
| `set-cookie-name` | Отображает ресурсы с `Set-Cookie` заголковой именем, которое соответствует указанному значению.  DevTools заполняет автозаполнеть все найденные имена файлов cookie. |  
| `set-cookie-value` | Отображает ресурсы, которые имеют заголок со значением, `Set-Cookie` которое соответствует указанному значению.  DevTools заполняет автозаполнеть всеми найденными значениями файлов cookie. |  
| `status-code` | Отображает ресурсы, которые соответствуют определенному коду состояния HTTP.  DevTools заполняет меню автозаполнеия всеми найденными кодами состояния. |  

### Фильтрация запросов по типу  

Чтобы отфильтровать запросы по типу запроса, выберите одну из следующих кнопок на панели **"Сеть".**  

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
      Любой другой тип не указан.  
   :::column-end:::
:::row-end:::  

Если кнопки не отображаются, **** может быть скрыта области фильтров.  
Дополнительные сведения можно найти в [области "Скрыть фильтры".](#hide-the-filters-pane)  

Чтобы включить несколько фильтров типов одновременно, удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите его.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров type для отображения ресурсов JS, CSS и Document" lightbox="../media/network-network-type-filters.msft.png":::
   Использование фильтров type для отображения ресурсов JS, CSS и Document  
:::image-end:::  

### Фильтрация запросов по времени  

Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.  Фильтр включен.  Отображается любой запрос, который был активен в течение выделенного времени.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация всех неактивных запросов со 300 мс" lightbox="../media/network-network-overview-filter.msft.png":::
   Фильтрация всех неактивных запросов со 300 мс  
:::image-end:::  

### Скрытие URL-адресов данных  

[URL-адреса данных —][MDNHTTPDataURIs] это небольшие файлы, внедренные в другие документы.  Любой запрос, который отображается в таблице "Запросы", начинается с `data:` URL-адреса данных.  

Чтобы скрыть запросы, отключите проверку **"Скрыть URL-адреса** данных".  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="The Hide Data URLs checkbox" lightbox="../media/network-network-hide-data-urls.msft.png":::
   The **Hide Data URLs** checkbox  
:::image-end:::  

## Запросы на сортировку  

По умолчанию запросы в таблице "Запросы" сортироваться по времени начала, но можно сортировать таблицу по другим критериям.  

### Сортировка по столбцам  

Выберите за колонок любого столбца в запросах, чтобы отсортировать запросы по этому столбцу.  

### Сортировка по этапу действия  

Чтобы изменить параметров сортировки запросов в каскадной среде, наведите курсор на загон таблицы ****"Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\), наведите курсор на Каскад и выберите один из следующих параметров.  

:::row:::
   :::column span="1":::
      **Время начала**  
   :::column-end:::
   :::column span="2":::
      Первый запрос, который был инициирован, находится вверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время отклика**  
   :::column-end:::
   :::column span="2":::
      Первый запрос, который начал скачивать, находится вверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время окончания**  
   :::column-end:::
   :::column span="2":::
      Первый завершенный запрос находится вверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Общая длительность**  
   :::column-end:::
   :::column span="2":::
      Запрос с самыми короткими настройками подключения и запросом или ответом находится вверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Задержка**  
   :::column-end:::
   :::column span="2":::
      The request that waited the shortest time for a response is at the top.  
   :::column-end:::
:::row-end:::  

В этих описаниях предполагается, что каждый соответствующий параметр ранж находится в ранге от самого короткого к самому длинному.  Выберите заголок столбца **"Каскад",** чтобы изменить порядок.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскада по общей продолжительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Сортировка каскада по общей продолжительности \(Светлая часть каждой панели — это время ожидания, а более темная часть — время, затраченное на скачивание bytes\)  
:::image-end:::  

## Анализ запросов  

Если devTools открыт, все запросы занося в журнал на панели **"Сеть".**  
Используйте панель "Сеть" для анализа запросов.  

### Отображение журнала запросов  

Используйте таблицу "Запросы", чтобы отобразить журнал всех запросов, сделанных во время открытия DevTools.  Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите курсор на запросы.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица Requests" lightbox="../media/network-network-requests-table.msft.png":::
   Таблица Requests  
:::image-end:::  

В таблице "Запросы" по умолчанию отображаются следующие столбцы.  

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
      
      *   **Parser**  HtmL-разберегатель для Microsoft Edge.  
      *   **Перенаправление**  Перенаправление HTTP.  
      *   **Script**  Функция JavaScript.  
      *   **Other**  Другой процесс или действие, например переход на страницу по ссылке или ввод URL-адреса в адресной панели.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      Объединенный размер заголовок ответа и тело ответа, доставленные сервером.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время**  
   :::column-end:::
   :::column span="2":::
      Общая продолжительность от начала запроса до получения последнего byte в ответе.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Каскад](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Визуальная разбивка действия для каждого запроса.  
   :::column-end:::
:::row-end:::  

#### Добавление и удаление столбцов  

Наведите курсор на загон таблицы "Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите параметр, чтобы скрыть или показать его.  В настоящее время отображаются параметры с контрольными знаками рядом с каждым элементом.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу Запросы" lightbox="../media/network-network-requests-add-column.msft.png":::
   Добавление столбца в таблицу "Запросы"  
:::image-end:::  

#### Добавление настраиваемой столбцов  

Чтобы добавить настраиваемый столбец в таблицу "Запросы", наведите курсор на загон таблицы ****"Запросы", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Заглавные столбцы".  >  ****  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемного столбца в таблицу Запросы" lightbox="../media/network-network-requests-add-custom.msft.png":::
   Добавление настраиваемного столбца в таблицу "Запросы"  
:::image-end:::  

### Отображение связи синхронизации запросов  

Используйте каскадный показ для отображения связей синхронизации запросов.  
Организация Каскада по умолчанию использует время начала запросов.  
Таким образом, запросы, которые находятся дальше слева, запущены раньше, чем запросы, которые находятся дальше справа.  

Чтобы просмотреть различные способы сортировки каскада, перейдите к этапу [сортировки по активности.](#sort-by-activity-phase)  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец Каскад в области Запросы" lightbox="../media/network-network-requests-waterfall.msft.png":::
   Столбец "Каскад" в **области "Запросы"**  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
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

### Отображение предварительного просмотра тела ответа  

Чтобы отобразить предварительный просмотр тела ответа, с помощью следующих действий.  

1.  Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".  
1.  Выберите вкладку **"Предварительный** просмотр".  

Вкладка "Предварительный просмотр" в основном полезна для отображения изображений.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка Предварительный просмотр" lightbox="../media/network-network-resources-preview.msft.png":::
   Вкладка **"Предварительный** просмотр"  
:::image-end:::  

### Отображение тела ответа  

Чтобы отобразить тело ответа на запрос, с помощью следующих действий.  

1.  Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".  
1.  Выберите **вкладку "Ответ".**  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка Ответ" lightbox="../media/network-network-resources-response.msft.png":::
   Вкладка **"Ответ"**  
:::image-end:::  

### Отображение http-headers  

Чтобы отобразить данные http-загона о запросе, с помощью следующих действий.  

1.  Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".  
1.  Выберите **вкладку "Headers".**  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка Заглавные" lightbox="../media/network-resources-headers.msft.png":::
   Вкладка **"Заглавные"**  
:::image-end:::  

#### Отображение источника http-загона  

По умолчанию на вкладке "Headers" имена заглавных букв показаны в алфавитном порядке.  Чтобы dsiplay имена http-загона в порядке получения, используйте следующие действия.  

1.  Откройте **вкладку "Заглавные"** для интересующих вас запросов.  Для получения дополнительных сведений перейдите к [отображаемой http-загона.](#display-http-headers)  
1.  Choose **view source**, next to the Request **Header** or **Response Header** section.  

### Отображение параметров строки запроса  

Чтобы отобразить параметры строки запроса URL-адреса в понятном для человека формате, с помощью следующих действий.  

1.  Откройте **вкладку "Заглавные"** для интересующих вас запросов.  Для получения дополнительных сведений перейдите к [отображаемой http-загона.](#display-http-headers)  
1.  Перейдите в **раздел "Параметры строки запроса".**  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел Параметры строки запроса" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Раздел **"Параметры строки запроса"**  
:::image-end:::  

#### Отображение источника параметров строки запроса  

Чтобы отобразить источник параметра строки запроса, с помощью следующих действий.  

1.  Перейдите в раздел "Параметры строки запроса".  Для получения дополнительных сведений перейдите к [параметрам строки запроса.](#display-query-string-parameters)  
1.  Выберите **источник представления.**  

#### Отображение параметров строки запроса в кодированном URL-адресе  

Чтобы отобразить параметры строки запроса в понятном для человека формате, но с сохраненными кодами, с помощью следующих действий.  

1.  Перейдите в раздел "Параметры строки запроса".  Для получения дополнительных сведений перейдите к [параметрам строки запроса.](#display-query-string-parameters)  
1.  Выберите **url-адрес представления в кодированном формате.**  

### Отображение файлов cookie  

Чтобы отобразить файлы cookie, отправленные в http-заголке запроса, с помощью следующих действий.  

1.  Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".  
1.  Выберите **вкладку "Файлы cookie".**  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка Файлы cookie" lightbox="../media/network-network-resources-cookies.msft.png":::
   Вкладка "Файлы cookie"  
:::image-end:::  

### Отображение разбивки по времени запроса  

Чтобы отобразить разбивку по времени запроса, с помощью следующих действий.  

1.  Выберите URL-адрес запроса в столбце **"Имя"** таблицы "Запросы".  
1.  Выберите вкладку **"Время".**  

Чтобы быстрее получить доступ к данным, перейдите к [предварительному просмотру разбивки по времени.](#preview-a-timing-breakdown)  

Дополнительные сведения о каждом из этапов, которые могут отображаться на вкладке "Синхронизация", можно найти в разных этапах разбивки по [времени.](#timing-breakdown-phases-explained) ****  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка Время" lightbox="../media/network-network-resources-timing.msft.png":::
   Вкладка **"Время"**  
:::image-end:::  

Дополнительные сведения о каждом из этапов.  

Для получения дополнительных сведений о доступе к дисплею перейдите к [разбивке по времени отображения.](#display-the-timing-breakdown-of-a-request)  

#### Предварительный просмотр разбивки по времени  

Чтобы отобразить предварительный просмотр разбивки по времени запроса, в столбце **"Каскад"** таблицы "Запросы" наведите курсор на запись запроса.  

Дополнительные сведения о том, как получить доступ к данным без наведении курсоров, перейдите к отобралке разбивки по времени [запроса.](#display-the-timing-breakdown-of-a-request)  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбивки по времени запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Просмотр разбивки по времени запроса  
:::image-end:::  

#### Этапы разбивки по времени  

Дополнительные сведения о каждом из этапов, которые могут отображаться на вкладке **"Синхронизация".**  

:::row:::
   :::column span="1":::
      **Очередь**  
   :::column-end:::
   :::column span="2":::
      Браузер очереди запросов, если любое из следующих true.  
      
      *   Существуют запросы с более высоким приоритетом.  
      *   Для одного источника открыто шесть подключений TCP, что является ограничением.  Применяется только к HTTP/1.0 и HTTP/1.1.  
      *   Браузер нена короткое время на дисковый кэш.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Приостановлено**  
   :::column-end:::
   :::column span="2":::
      Запрос заглох по любой из причин, описанных в **очереди.**  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **DNS Lookup**  
   :::column-end:::
   :::column span="2":::
      Браузер разрешит IP-адрес для запроса.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Начальное подключение**  
   :::column-end:::
   :::column span="2":::
      Браузер устанавливает подключение, включая соглашения TCP, повторное создание TCP и согласование уровня безопасного socket.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Согласование прокси-сервера**  
   :::column-end:::
   :::column span="2":::
      Браузер согласован с [прокси-сервером.][WikiProxyServer]  
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
      **Подготовка ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Браузер запускает рабочий сотрудник службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Запрос в ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Запрос отправляется сотруднику службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Ожидание \(TTFB\)**  
   :::column-end:::
   :::column span="2":::
      Браузер ожидает первого byte отклика.  TTFB означает "Время до первого byte".  Это время включает в себя один круговой путь задержки и время, необходимое серверу для подготовки ответа.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Загрузка содержимого**  
   :::column-end:::
   :::column span="2":::
      Браузер получает ответ.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Получение push-сигнала**  
   :::column-end:::
   :::column span="2":::
      Браузер получает данные для этого ответа с помощью http/2 Server Push.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Чтение push-вех**  
   :::column-end:::
   :::column span="2":::
      Браузер читает ранее полученные локальные данные.  
   :::column-end:::
:::row-end:::  

### Отображение инициаторов и зависимостей  

Чтобы отобразить инициаторов и зависимости запроса, удерживайте и наведите курсор на `Shift` запрос в таблице "Запросы".  Цвета DevTools: инициаторы показаны зеленым цветом, а зависимости — красным цветом.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Отображение инициаторов и зависимостей запроса  
:::image-end:::  

Если таблица Requests упорядочена в хронологическом порядке, при наведении курсором на строку в строке перед ней отображается зеленый запрос.  Зеленый запрос является инициатором зависимостей.  Если перед этим в строке отображается другой зеленый запрос, этот запрос выше является инициатором инициатора.  И так далее.  

### Отображение событий загрузки  

DevTools отображает время событий и событий в нескольких `DOMContentLoaded` `load` местах на панели **"Сеть".**  Событие `DOMContentLoaded` имеет синий цвет, а событие — `load` красный.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположения doMContentLoaded и события загрузки на панели Сеть" lightbox="../media/network-network-requests-load-events.msft.png":::
   Расположение событий и `DOMContentLoaded` событий `load` на панели **"Сеть"**  
:::image-end:::  

### Отображение общего количества запросов  

Общее количество запросов перечислены в **** области сводки в нижней части **панели "Сеть".**  

> [!CAUTION]
> Это число отслеживает только запросы, зарегистрированные с момента открытия DevTools.  Если другие запросы произошли до открытия DevTools, эти запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Общее количество запросов с момента открытия DevTools  
:::image-end:::  

### Отображение общего размера скачивания  

Общий размер скачиваемых запросов указан **** в области "Сводка" в нижней части **панели "Сеть".**  

> [!CAUTION]
> Это число отслеживает только запросы, зарегистрированные с момента открытия DevTools.  Если другие запросы произошли до открытия DevTools, предыдущие запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий размер скачиваемых запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   Общий размер скачиваемых запросов  
:::image-end:::  

Чтобы проверить размер ресурсов после того, как браузер отпечатает каждый элемент, перейдите, чтобы отобразить несжамый [размер ресурса.](#display-the-uncompressed-size-of-a-resource)  

### Отображение трассировки стека, вызвавного запрос  

После запроса ресурса в javaScript наведите курсор на столбец "Инициатор", чтобы отобразить трассировку стека перед запросом. ****  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека до запроса ресурса" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Трассировка стека до запроса ресурса  
:::image-end:::  

### Отображение несжамого размера ресурса  

Включив **контрольный ящик "Использовать** большие строки запросов", а затем просмотрите нижнее значение **столбца Size.**  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несмеченных ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Пример несжатых ресурсов \(Сжатый размер файла, отправленного по сети, был , тогда как несжатый размер `jquery-3.3.1.min.js` `29.9 KB` был `84.9 KB` \)  
:::image-end:::  

## Экспорт данных запросов  

### Сохранение всех сетевых запросов в файл HAR  

Чтобы сохранить все сетевые запросы в файл HAR, выполните следующие действия.  

1.  Наведите курсор на любой запрос в таблице "Запросы" и откройте контекстное меню \(щелкните правой кнопкой мыши\).  
1.  Choose **Save as HAR with Content**.  DevTools сохраняет все запросы, которые произошли с момента открытия DevTools, в файл HAR.  Фильтровать запросы нельзя.  Вы также не можете сохранить один запрос.  

После сохранения файла HAR вы можете импортировать его обратно в DevTools для анализа.  Просто перетащите файл HAR в таблицу Requests.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Choose Save as HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Choose **Save as HAR with Content**  
:::image-end:::  

### Копирование одного или более запросов в буфер обмена  

В **столбце "Имя"** таблицы "Запросы" наведите курсор на запрос, откройте **** контекстное меню \(щелкните правой кнопкой мыши),наведите курсор на "Копировать" и выберите один из следующих параметров.  

| Название | Подробные сведения |  
|:--- |:--- |  
| **Копировать адрес ссылки** | Скопируйте URL-адрес запроса в буфер обмена. |  
| **Копирование ответа** | Скопируйте текст ответа в буфер обмена. |  
| **Копирование как fetch** | &nbsp; |  
| **Копировать как cURL** | Скопируйте запрос в виде команды cURL. |  
| **Копировать все как получить** | &nbsp; |  
| **Копировать все как cURL** | Скопируйте все запросы в виде цепочки команд cURL. |  
| **Копировать все как HAR** | Скопируйте все запросы в качестве данных HAR. |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выбор ответа Копировать" lightbox="../media/network-network-requests-copy-response.msft.png":::
   Выбор **ответа "Копировать"**  
:::image-end:::  

### Копирование форматированный ответ JSON в буфер обмена  

Выберите сетевой запрос и перейдите в области **"Headers".**  Чтобы скопировать значение JSON ответа, **** перейдите к запросу полезной нагрузки, наведите курсор на содержимое ответа JSON, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Копировать **значение".**  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Копировать значение в контекстное меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Копировать значение** в контекстное меню  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Visual Studio код с форматированный ответ JSON" lightbox="../media/network-header-paste-property-value.msft.png":::
          Pasting formatted response JSON in Visual Studio Code  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### Копирование значений свойств из сетевых запросов в буфер обмена  

Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните следующие действия.  

1.  Откройте области **"Headers".**  
1.  Откройте один из следующих разделов.  
    *   Запрос полезной нагрузки \(JSON\)  
    *   Данные формы  
    *   Параметры строки запроса  
    *   Заглавные запросы  
    *   Заглавные  
1.  Откройте контекстное меню \(щелкните правой кнопкой мыши\) > **значение копирования.**  Теперь вы можете в paste the value into any editor to review it.  
    
## Изменение макета панели "Сеть"  

Вы можете развернуть или свернуть разделы пользовательского **интерфейса** панели "Сеть", чтобы получить важные сведения.  

### Скрытие области фильтров  

По умолчанию DevTools показывает области **фильтров.**  
Выберите **filter** \( ![ Filter ][ImageFilterIcon] \), чтобы скрыть его.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка Скрыть фильтры" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Кнопка "Скрыть фильтры"  
:::image-end:::  

### Использование больших строк запросов  

Используйте большие строки, если вам нужно большее пространство в таблице сетевых запросов.  Некоторые столбцы также предоставляют дополнительные сведения при использовании больших строк.  Например, нижним значением столбца **Size** является несмещается размер запроса.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример больших строк запросов в области Запросы" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Пример больших строк запросов в **** области "Запросы"  
:::image-end:::  

Чтобы включить большие строки, включите контрольный ящик **"Использовать большие строки запросов".**  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="The Use large request rows checkbox" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   The **Use large request rows** checkbox  
:::image-end:::  

### Скрытие области обзора  

По умолчанию DevTools отображает области **обзора.**  Чтобы скрыть его, отключите **контрольный ящик "Показать обзор".**  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="The Show Overview checkbox" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   The **Show Overview** checkbox  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Debug Progressive Web Apps | Документы Майкрософт"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/network/reference) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
