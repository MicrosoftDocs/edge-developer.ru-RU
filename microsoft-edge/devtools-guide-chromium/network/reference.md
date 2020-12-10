---
description: Полный справочник по функциям панели DevTools сети Microsoft Edge.
title: Справочник по анализу сети
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4d4dc8ad5102766f3ad3c8322dbf9342a69e9097
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203908"
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

Ознакомьтесь с новыми способами для анализа того, как страница загружается в этой полной версии справочника по функциям сетевого анализа Microsoft Edge DevTools.  

## Запись сетевых запросов  

По умолчанию DevTools запись всех сетевых запросов на панели " **сеть** ", пока открыта DevTools.  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Панель сеть"::: lightbox="../media/network-network-panel.msft.png":::
   Панель " **сеть** "  
:::image-end:::  

### Прекращение записи сетевых запросов  

Чтобы остановить запись запросов, выполните указанные ниже действия.  

1.  На панели **Network (сеть** ) выберите команду **остановить запись журнала сети** \ ( ![ остановить запись сетевого журнала ][ImageRecordOnIcon] \).  Оно превращается в серый, чтобы показать, что DevTools больше не записывает запросы.  
1.  Нажмите кнопку `Control` + `E` \ (Windows, Linux \) или `Command` + `E` \ (macOS \), когда фокус находится на панели **Network (сеть** ).  

### Очистка запросов  

На панели Network (сеть) выберите **clear** \ ( ![ очистить ][ImageClearIcon] \), чтобы удалить все запросы из таблицы запросы. ****  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Кнопка очистить"::: lightbox="../media/network-network-clear-button.msft.png":::
   Кнопка " **очистить** "  
:::image-end:::  

### Сохранение запросов на загрузку страниц  

Чтобы сохранить запросы при загрузке страниц, включите флажок **сохранить журнал** на панели **сеть** .  DevTools сохраняет все запросы, пока не отключайте параметр **сохранить журнал**.  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Флажок сохранить журнал"::: lightbox="../media/network-network-preserve-log.msft.png":::
   Флажок " **сохранить журнал** "  
:::image-end:::  

### Захват снимков экрана при загрузке страницы  

Выведите снимки экрана, чтобы проанализировать, какие дисплеи отображаются для пользователей во время ожидания загрузки страницы.  

Чтобы включить снимки экрана, выберите **Параметры сети**и на панели **сеть** включите флажок **захватить снимки экрана** .  

Обновите страницу, когда фокус находится на панели " **сеть** ", чтобы захватить снимки экрана.  

После захвата снимка экрана вы взаимодействуете с ним следующими способами.  

*   Наведите указатель мыши на снимок экрана, чтобы отобразить точку, в которой был записан снимок экрана.  На панели **обзора** появится желтая линия.  
*   Выберите эскиз экрана, чтобы отфильтровать все запросы, произошедшие после захвата снимка экрана.  
*   Дважды щелкните эскиз, чтобы увеличить его.  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Наведение указателя мыши на снимок экрана" lightbox="../media/network-network-screenshot-hover.msft.png":::
   Наведение указателя мыши на снимок экрана  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## Изменение поведения при загрузке  

### Эмуляция первого времени посетителя с помощью отключения кэша браузера  

Чтобы эмулировать, как пользователь попытается использовать ваш сайт в первый раз, включите флажок **отключить кэш** .  DevTools отключает кэш браузера.  Эта функция более точно эмулирует взаимодействие с пользователем при первом запуске, так как запросы размещаются из кэша браузера на повторных посещениях.  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Флажок отключить кэш"::: lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   Флажок " **отключить кэш** "  
:::image-end:::  

#### Отключение кэша браузера из денежных ящиков условий сети  

Если вы хотите отключить кэш при работе с другими панелями DevTools, используйте денежные ящики условия сети.  

1.  Откройте денежный ящик **условий сети** .  
1.  Включите \ (или выключите) флажок **отключить кэш** .  

<!--todo: add network condition section when available -->  

### Очистка кэша браузера вручную  

Чтобы вручную очистить кэш браузера в любое время, откройте контекстное меню (щелкните правой кнопкой мыши в любом месте таблицы запросов и выберите команду **очистить кэш браузера**).  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Выбор очистки кэша браузера" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   Выбор **очистки кэша браузера**  
:::image-end:::  

### Эмуляция в автономном режиме  

Новый класс веб-приложений, именуемых [прогрессивными веб-приложениями][DevtoolsProgressiveWebApps], не будет работать в автономном режиме с помощью **обслуживания сотрудников**.  Возможно, вам будет удобно быстро смоделировать устройство, которое не имеет подключения к данным, при построении такого типа приложения.  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

Щелкните раскрывающееся меню **онлайн** , выполните поиск в разделе **пресеты**и выберите пункт в **автономном** режиме, чтобы имитировать автономный режим работы сети.  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Раскрывающееся меню автономный режим"::: lightbox="../media/network-network-offline-dropdown.msft.png":::
   Раскрывающееся меню " **автономный режим** "  
:::image-end:::  

### Эмуляция медленных сетевых подключений  

Эмуляция медленной сети 3G, Fast 3G и других скоростей соединения из раскрывающегося меню **Online** .  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Раскрывающееся меню регулирования" lightbox="../media/network-network-throttling-menu.msft.png":::
   Раскрывающееся меню **регулирования**  
:::image-end:::  

Вы можете выбрать один из различных наборов параметров, например "медленный" или "Быстрая 3G".  Чтобы добавить собственные пользовательские стили, откройте меню регулирования и выберите пункт **настраиваемое**  >  **Добавление**.  

DevTools отображает значок предупреждения рядом с вкладкой **сеть** , чтобы напомнить вам, что регулирование разрешено.  

#### Эмуляция медленных сетевых подключений из денежных ящиков условий сети  

Если вы хотите регулировать сетевое соединение при работе с другими панелями DevTools, используйте денежные ящики условий сети.  

1.  Откройте денежный ящик **условий сети** .  
1.  Выберите скорость соединения в меню **регулирования** .  

<!--todo: add network condition section when available -->  

### Очистка файлов cookie браузера вручную  

Чтобы вручную очистить cookie-файлы браузера в любое время, наведите указатель мыши на любое место в таблице запросов, откройте контекстное меню, а затем выберите команду **Удалить cookie-файлы браузера**.  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Выберите команду очистить cookie-браузеры."::: lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   Выберите команду **"очистить" cookie-браузеры** .  
:::image-end:::  

### Переопределение агента пользователя  

Чтобы вручную переопределить агент пользователя, выполните указанные ниже действия.  

1.  Откройте денежный ящик **условий сети** .  
1.  Отключите флажок **выбрать автоматически** .  
1.  Выберите в меню пункт агента пользователя или введите его в текстовом поле.  

<!--todo: add network condition section when available -->  

## Фильтрация запросов  

### Фильтрация запросов по свойствам  

С помощью текстового поля **Фильтр** можно отфильтровать запросы по свойствам, таким как домен или размер запроса.  

Если текстовое поле не отображается, возможно, область **фильтры** скрыта.  
Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Текстовое поле фильтр"::: lightbox="../media/network-network-filters-textbox.msft.png":::
   Текстовое поле " **Фильтр** "  
:::image-end:::  

Вы можете использовать несколько свойств одновременно, разделяя каждое свойство пробелами.  Например, `mime-type:image/png larger-than:1K` отображает все PNGs, размер которых больше 1 Кбайт.  Фильтры с несколькими свойствами эквивалентны `AND` операциям.  `OR` операции в настоящее время не поддерживаются.  

Полный список поддерживаемых свойств.  

| Свойство | Сведения |  
|:--- | :--- |  
| `domain` | Отображать только ресурсы из указанного домена.  Вы можете использовать подстановочный знак "\ `*` ", чтобы включить несколько доменов.  Например, `*.com` отображаются ресурсы из всех доменных имен, которые заканчиваются на `.com` .  DevTools Заполнение раскрывающегося меню "Автозаполнение" всеми найденными доменами. |  
| `has-response-header` | Выводит ресурсы, содержащие указанный заголовок HTTP-ответа.  DevTools заполнить раскрывающийся список автозавершения всеми найденными заголовками ответов. |  
| `is` | Используется `is:running` для поиска `WebSocket` ресурсов. |  
| `larger-than` | Отображаются ресурсы, размер которых превышает указанный в байтах.  Установка значения эквивалентно значению свойства `1000` `1k` . |  
| `method` | Отображает ресурсы, полученные с помощью указанного типа метода HTTP.  DevTools заполнить раскрывающийся список всеми найденными методами HTTP. |  
| `mime-type` | Выводит ресурсы указанного типа MIME.  DevTools заполнить раскрывающийся список всеми найденными типами MIME. |  
| `mixed-content` | Показать все смешанные ресурсы контента \ ( `mixed-content:all` \) или только те из них, которые в данный момент отображаются \ ( `mixed-content:displayed` \). |  
| `scheme` | Отображаются ресурсы, полученные по незащищенным HTTP-( `scheme:http` \) или защищенным HTTPS-( `scheme:https` \). |  
| `set-cookie-domain` | Отображает ресурсы с `Set-Cookie` заголовком с `Domain` атрибутом, соответствующим указанному значению.  DevTools заполнить Автозаполнение всеми найденными доменами cookie-файлов. |  
| `set-cookie-name` | Отображаются ресурсы, у которых есть `Set-Cookie` заголовок с именем, соответствующим указанному значению.  DevTools заполните Автозаполнение всеми найденными именами cookie-файлов. |  
| `set-cookie-value` | Отображает ресурсы с `Set-Cookie` заголовком со значением, которое соответствует указанному значению.  DevTools заполнить Автозаполнение всеми найденными значениями cookie-файлов. |  
| `status-code` | Отображает ресурсы, соответствующие указанному коду состояния HTTP.  DevTools заполняет раскрывающееся меню автозаполнения всеми найденными кодами состояния. |  

### Фильтрация запросов по типу  

Чтобы отфильтровать запросы по типу запроса, выберите один из указанных ниже кнопок на панели **сеть** .  

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
      **IMG**  
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
      **Тов**  
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
      **Является**  
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
      Любые другие типы не указаны в списке.  
   :::column-end:::
:::row-end:::  

Если кнопки не отображаются, область **фильтров** может быть скрыта.  
Чтобы получить дополнительные сведения, перейдите в раздел [скрыть область фильтров](#hide-the-filters-pane).  

Чтобы включить множественные фильтры типов одновременно, удерживайте клавишу `Control` \ (Windows, Linux \) или `Command` \ (macOS \) и выберите.  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Использование фильтров типов для отображения ресурсов JS, CSS и документов" lightbox="../media/network-network-type-filters.msft.png":::
   Использование фильтров типов для отображения ресурсов JS, CSS и документов  
:::image-end:::  

### Фильтрация запросов по времени  

Чтобы отобразить только те запросы, которые были активны в течение этого времени, выберите в области " **Обзор** " и перетащите ее влево или вправо.  Фильтр является инклюзивным.  Отображается любой запрос, который был активен в течение выбранного периода времени.  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Фильтрация запросов, которые были неактивны около 300 MS" lightbox="../media/network-network-overview-filter.msft.png":::
   Фильтрация запросов, которые были неактивны около 300 MS  
:::image-end:::  

### Скрыть URL-адреса данных  

[URL-адреса данных][MDNHTTPDataURIs] — это небольшие файлы, внедренные в другие документы.  Любые запросы, которые отображаются в таблице запросов, которая начинается с `data:` URL-адреса данных.  

Чтобы скрыть запросы, снимите флажок **скрыть URL-адреса данных** .  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Флажок скрыть URL-адреса данных"::: lightbox="../media/network-network-hide-data-urls.msft.png":::
   Флажок " **скрыть URL-адреса данных** "  
:::image-end:::  

## Запросы сортировки  

По умолчанию запросы в таблице запросов сортируются по времени запуска, но вы можете отсортировать таблицу с помощью других условий.  

### Сортировка по столбцам  

Выберите верхний колонтитул любого столбца в запросах для сортировки запросов по этому столбцу.  

### Этап сортировки по действию  

Чтобы изменить способ сортировки запросов, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню, наведите указатель мыши на пункт **Каскад**и выберите один из указанных ниже вариантов.  

:::row:::
   :::column span="1":::
      **Время начала**  
   :::column-end:::
   :::column span="2":::
      Первый инициированный запрос находится наверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время ответа**  
   :::column-end:::
   :::column span="2":::
      Первый запрос, загруженный в верхней части экрана.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время окончания**  
   :::column-end:::
   :::column span="2":::
      Первый завершенный запрос вверху.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Общая длительность**  
   :::column-end:::
   :::column span="2":::
      В верхней части запроса с минимальными параметрами подключения и запроса или ответа.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Задержка**  
   :::column-end:::
   :::column span="2":::
      Запрос, который ожидает наиболее короткий момент ответа, находится наверху.  
   :::column-end:::
:::row-end:::  

В этих описаниях предполагается, что каждый из вариантов имеет приоритет от кратчайшего к наиболее продолжительному.  Выберите верхний колонтитул столбца **каскадом** , чтобы изменить порядок.  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Сортировка каскадом по общей длительности" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   Сортировка каскадной группировки по общей длительности \ (светлая часть каждой линии — это задолгое время, в которое более темная часть загружает байты)  
:::image-end:::  

## Анализ запросов  

Пока DevTools открыты, все запросы на панели " **сеть** " записываются в журнал.  
Проанализируйте запросы с помощью панели "сеть".  

### Вывод журнала запросов  

С помощью таблицы запросы можно просмотреть журнал всех запросов, выполненных, когда DevTools открыты.  Чтобы получить дополнительные сведения о каждом элементе, выберите или наведите указатель мыши на пункт запросы.  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Таблица запросов" lightbox="../media/network-network-requests-table.msft.png":::
   Таблица запросов  
:::image-end:::  

По умолчанию в таблице запросов отображаются следующие столбцы.  

:::row:::
   :::column span="1":::
      **Название**  
   :::column-end:::
   :::column span="2":::
      Имя или идентификатор ресурса.  
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
      **Владельцы**  
   :::column-end:::
   :::column span="2":::
      Следующие объекты или процессы инициируют запросы.  
      
      *   **Средство синтаксического анализа**  Средство синтаксического анализа HTML для Microsoft Edge.  
      *   **Redirect (перенаправление**  )  Переадресация HTTP.  
      *   **Сценарий**  Функция JavaScript.  
      *   **Другие**  Некоторые другие процессы или действия, например переход на страницу с помощью ссылки или ввод URL-адреса в адресную строку.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Size**  
   :::column-end:::
   :::column span="2":::
      Объединенный размер заголовков ответа и текст ответа, доставленный сервером.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Время**  
   :::column-end:::
   :::column span="2":::
      Общая продолжительность от начала запроса до получения последнего байта в ответе.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Каскад](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      Визуальная декомпозиция мероприятия для каждого запроса.  
   :::column-end:::
:::row-end:::  

#### Добавление и удаление столбцов  

Наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите один из вариантов, чтобы скрыть или отобразить его.  Параметры, отображаемые в данный момент, отмечены флажками рядом с каждым элементом.  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Добавление столбца в таблицу запросы"::: lightbox="../media/network-network-requests-add-column.msft.png":::
   Добавление столбца в таблицу "запросы"  
:::image-end:::  

#### Добавление настраиваемых столбцов  

Чтобы добавить настраиваемый столбец в таблицу запросы, наведите указатель мыши на заголовок таблицы запросы, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите **заголовки ответов**для  >  **управления столбцами заголовков**.  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Добавление настраиваемого столбца в таблицу запросы"::: lightbox="../media/network-network-requests-add-custom.msft.png":::
   Добавление настраиваемого столбца в таблицу "запросы"  
:::image-end:::  

### Отображение отношения временных повременных запросов  

Используйте Каскад, чтобы отобразить отношения времени между запросами.  
В структуре, используемой по умолчанию для каскадов, используется время начала запроса.  
Таким образом, запросы, которые раньше приступили к началу, чем те, которые находятся дальше по правому краю.  

Чтобы просмотреть различные способы сортировки каскадов, перейдите на [фазу "Сортировка по действию](#sort-by-activity-phase)".  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Столбец Каскад на панели запросы"::: lightbox="../media/network-network-requests-waterfall.msft.png":::
   Столбец "Каскад" на панели " **запросы** "  
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

### Вывод предварительной версии текста ответа  

Чтобы просмотреть текст ответа, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Выберите вкладку **Предварительный просмотр** .  

Вкладка Предварительный просмотр в основном полезна для отображения изображений.  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Вкладка предварительный просмотр"::: lightbox="../media/network-network-resources-preview.msft.png":::
   Вкладка " **Предварительный просмотр** "  
:::image-end:::  

### Отображение текста ответа  

Чтобы отобразить текст ответа на запрос, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Перейдите на вкладку **ответ** .  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Вкладка ответ"::: lightbox="../media/network-network-resources-response.msft.png":::
   Вкладка " **ответ** "  
:::image-end:::  

### Отображение заголовков HTTP  

Чтобы отобразить данные заголовка HTTP для запроса, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Перейдите на вкладку **заголовки** .  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Вкладка заголовки"::: lightbox="../media/network-resources-headers.msft.png":::
   Вкладка " **заголовки** "  
:::image-end:::  

#### Вывод источника HTTP-заголовков  

По умолчанию на вкладке заголовки отображаются имена заголовков в алфавитном порядке.  Чтобы dsiplay имена HTTP-заголовков в полученном порядке, выполните указанные ниже действия.  

1.  Открытие вкладки " **заголовки** " для запроса, который вас интересует.  Дополнительные сведения можно найти в разделе [Отображение заголовков HTTP](#display-http-headers).  
1.  Нажмите кнопку **Просмотр источника**рядом с разделом **заголовок запроса** или **заголовок ответа** .  

### Отображение параметров строки запроса  

Чтобы отобразить параметры строки запроса URL-адреса в удобочитаемом формате, выполните указанные ниже действия.  

1.  Открытие вкладки " **заголовки** " для запроса, который вас интересует.  Дополнительные сведения можно найти в разделе [Отображение заголовков HTTP](#display-http-headers).  
1.  Перейдите к разделу **Параметры строки запроса** .  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Раздел параметры строки запроса"::: lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   Раздел " **Параметры строки запроса** "  
:::image-end:::  

#### Показать источник параметров строки запроса  

Чтобы отобразить источник параметра строки запроса для запроса, выполните указанные ниже действия.  

1.  Перейдите к разделу Параметры строки запроса.  Дополнительные сведения можно найти в разделе [Отображение параметров строки запроса](#display-query-string-parameters).  
1.  Нажмите кнопку **Просмотр источника**.  

#### Отображение строковых параметров запроса в кодировке URL  

Чтобы отобразить параметры строки запроса в удобочитаемом формате, но с сохранением кодировки, выполните указанные ниже действия.  

1.  Перейдите к разделу Параметры строки запроса.  Дополнительные сведения можно найти в разделе [Отображение параметров строки запроса](#display-query-string-parameters).  
1.  Выберите команду **Просмотреть закодированный URL-адрес**.  

### Отображение файлов cookie  

Чтобы отобразить cookie-файлы, отправленные в заголовке запроса HTTP, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Перейдите на вкладку " **cookie** ".  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Вкладка cookie"::: lightbox="../media/network-network-resources-cookies.msft.png":::
   Вкладка "cookie"  
:::image-end:::  

### Отображение разбиения по времени для запроса  

Чтобы отобразить разбиение по времени для запроса, выполните указанные ниже действия.  

1.  Выберите URL-адрес запроса в столбце " **имя** " таблицы "запросы".  
1.  Выберите вкладку **время** .  

Для более удобного доступа к данным перейдите к разделу [Предварительный просмотр разбивки времени](#preview-a-timing-breakdown).  

Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** , можно найти в разделе [этапы разбивки по времени](#timing-breakdown-phases-explained).  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-network-resources-timing.msft.png":::
   Вкладка **время**  
:::image-end:::  

Дополнительные сведения о каждой из фаз.  

Дополнительные сведения о том, как получить доступ к экрану, можно найти в разделе [Отображение временных интервалов](#display-the-timing-breakdown-of-a-request).  

#### Предварительный просмотр разбивки по времени  

Чтобы отобразить предварительный просмотр разбиения по времени для запроса, наведите указатель мыши на запись запроса в столбце " **Каскад** " таблицы "запросы".  

Дополнительные сведения о том, как получить доступ к данным без наведения указателя мыши, можно найти, чтобы [отобразить разбиение по времени для запроса](#display-the-timing-breakdown-of-a-request).  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> предварительный просмотр разбиения по времени для запроса" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   Предварительный просмотр разбиения по времени для запроса  
:::image-end:::  

#### Описание этапов разделения времени  

Дополнительные сведения о каждой из фаз, которые могут отображаться на вкладке **время** .  

:::row:::
   :::column span="1":::
      **Очередь**  
   :::column-end:::
   :::column span="2":::
      Браузер помещает запросы в очередь, если выполняется одно из следующих условий.  
      
      *   Существуют запросы с более высокими приоритетами.  
      *   Шесть подключений TCP открыты для одного и того же источника, что является ограничением.  Применимо только к HTTP/1.0 и HTTP/1.1.  
      *   Браузер временно выделяет место в кэше на диске.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Блокированы**  
   :::column-end:::
   :::column span="2":::
      Запрос будет остановлен в любой из причин, описанных в разделе **очереди**.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Поиск DNS**  
   :::column-end:::
   :::column span="2":::
      Браузер разрешает IP-адрес запроса.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Начальное соединение**  
   :::column-end:::
   :::column span="2":::
      Браузер устанавливает подключение, в том числе подтверждения TCP, повторы TCP и согласовывающие безопасный уровень сокетов.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Согласование прокси-сервера**  
   :::column-end:::
   :::column span="2":::
      Браузер согласовывает запрос с [прокси-сервером][WikiProxyServer].  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Отправлено запросов**  
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
      Браузер запускает сотрудника службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Запрос на ServiceWorker**  
   :::column-end:::
   :::column span="2":::
      Запрос отправляется сотруднику службы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Ожидание \ (TTFB \)**  
   :::column-end:::
   :::column span="2":::
      Браузер ожидает первый байт ответа.  TTFB означает время для первого байта.  Это время включает один цикл обработки задержки и время, затраченное сервером на подготовку ответа.  
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
      **Получение push-уведомлений**  
   :::column-end:::
   :::column span="2":::
      Браузер получает данные для этого ответа через HTTP/2 серверную извещающую передачу.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Чтение push-уведомлений**  
   :::column-end:::
   :::column span="2":::
      Браузер читает локальные данные, полученные ранее.  
   :::column-end:::
:::row-end:::  

### Отображение инициаторов и зависимостей  

Чтобы отобразить инициаторы и зависимости запроса, удерживайте `Shift` и наведите указатель мыши на запрос в таблице "запросы".  DevTools цвета: инициаторы отображаются зеленым цветом, а зависимости — красным.  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Отображение инициаторов и зависимостей запроса" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   Отображение инициаторов и зависимостей запроса  
:::image-end:::  

Если таблица запросы упорядочивается хронологически, при наведении указателя мыши на строку, предшествующую ей, выводится зеленый запрос.  Зеленый запрос — инициатор зависимости.  Если в строке перед этим отображается еще один зеленый запрос, это более высокий запрос является инициатором инициатора.  И так далее.  

### Вывод событий загрузки  

DevTools отображает время показа `DOMContentLoaded` `load` событий в нескольких местах на панели " **сеть** ".  `DOMContentLoaded`Событие окрашивается синим цветом, а `load` событие — красным.  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Расположение событий DOMContentLoaded и Load на панели сеть" ::: lightbox="../media/network-network-requests-load-events.msft.png":::
   Расположение `DOMContentLoaded` событий "и" `load` на панели " **сеть** "  
:::image-end:::  

### Вывод общего числа запросов  

Общее количество запросов можно найти в области **сводки** в нижней части панели " **сеть** ".  

> [!CAUTION]
> Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.  Если при открытии DevTools возникли другие запросы, эти запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Общее количество запросов с момента открытия DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   Общее количество запросов с момента открытия DevTools  
:::image-end:::  

### Показать общий размер загружаемого файла  

Общий объем загруженных запросов отображается в области **Сводка** в нижней части панели " **сеть** ".  

> [!CAUTION]
> Этот номер отслеживает только те запросы, которые были зарегистрированы с момента открытия DevTools.  Если при открытии DevTools возникли другие запросы, предыдущие запросы не учитываются.  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Общий объем загруженных запросов" lightbox="../media/network-network-total-download-size.msft.png":::
   Общий объем загруженных запросов  
:::image-end:::  

Чтобы убедиться в том, что после того как браузер распаковать все элементы, перейдите к разделу [Отображение несжатого размера ресурса](#display-the-uncompressed-size-of-a-resource).  

### Отобразить трассировку стека, которая привела к запросу  

После того как оператор JavaScript запрашивает ресурс, наведите указатель мыши на столбец **инициатора** , чтобы отобразить трассировку стека, которая выводится в соответствии с запросом.  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Трассировка стека, ведущая к запросу ресурсов" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   Трассировка стека, ведущая к запросу ресурсов  
:::image-end:::  

### Отображение несжатого размера ресурса  

Включите флажок **использовать строки большого запроса** и просмотрите минимальное значение в столбце **Размер** .  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Пример несжатых ресурсов" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   Пример несжатых ресурсов \ (сжатый размер `jquery-3.3.1.min.js` файла, отправленного по сети `29.9 KB` , в то время как несжатый размер `84.9 KB` )  
:::image-end:::  

## Данные запросов на экспорт  

### Сохранение всех сетевых запросов в файле HAR  

Чтобы сохранить все сетевые запросы в файле HAR, выполните указанные ниже действия.  

1.  Наведите указатель мыши на любой запрос в таблице запросов и откройте контекстное меню (щелкните правой кнопкой мыши \).  
1.  Выберите команду **Сохранить как HAR с содержимым**.  DevTools сохраняет все запросы, произошедшие после того, как вы открыли DevTools в файл HAR.  Вы не можете фильтровать запросы.  Вы также не можете сохранить один запрос.  

После того как вы сохраните файл HAR, вы можете импортировать его обратно в DevTools для анализа.  Просто перетащите файл HAR в таблицу запросы.  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Выберите команду Сохранить как HAR с контентом"::: lightbox="../media/network-network-requests-save-har-content.msft.png":::
   Выберите команду " **Сохранить как HAR с контентом** "  
:::image-end:::  

### Копирование одного или нескольких запросов в буфер обмена  

В столбце **имя** таблицы запросы наведите указатель мыши на запрос, откройте контекстное меню (щелкните правой кнопкой мыши, выберите команду **Копировать**) и выберите один из следующих параметров.  

| Название | Подробные сведения |  
|:--- |:--- |  
| **Копировать адрес ссылки** | Скопируйте URL-адрес запроса в буфер обмена. |  
| **Копирование ответа** | Скопировать текст ответа в буфер обмена. |  
| **Копировать как выборку** | &nbsp; |  
| **Копирование в виде изогнутого документа** | Копирование запроса в виде текстовой команды. |  
| **Копировать все как выборку** | &nbsp; |  
| **Копирование в виде изогнутого документа** | Копирование всех запросов в виде последовательности команд с фигурой. |  
| **Копирование всех как HAR** | Скопируйте все запросы как данные HAR. |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Выберите команду Копировать ответ"::: lightbox="../media/network-network-requests-copy-response.msft.png":::
   Выберите команду " **Копировать ответ** "  
:::image-end:::  

### Копирование формата JSON ответа в буфер обмена  

Выберите сетевой запрос и перейдите в область **заголовки** .  Чтобы скопировать значение JSON отклика, перейдите в **полезные данные запроса**, наведите указатель мыши на содержимое ответа JSON, откройте контекстное меню, а затем выберите команду **Копировать значение**.  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Копирование значения в контекстном меню" lightbox="../media/network-header-copy-property-value.msft.png":::
          **Копирование значения** в контекстном меню  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Код Visual Studio с форматом JSON ответа" lightbox="../media/network-header-paste-property-value.msft.png":::
          Вставка форматированного отклика JSON в код Visual Studio  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### Копирование значений свойств из сетевых запросов в буфер обмена  

Чтобы скопировать значения свойств из сетевых запросов в буфер обмена, выполните указанные ниже действия.  

1.  Открытие области " **заголовки** ".  
1.  Откройте один из следующих разделов заголовка.  
    *   Полезные данные для запроса \ (JSON \)  
    *   Данные формы  
    *   Параметры строки запроса  
    *   Заголовки запроса  
    *   Заголовки ответа  
1.  Откройте контекстное меню \ (щелкните правой кнопкой мыши, > **скопировать значение**.  Теперь вы можете вставить значение в любой редактор, чтобы просмотреть его.  
    
## Изменение макета панели "сеть"  

Вы можете развернуть или свернуть разделы пользовательского интерфейса панели " **сеть** ", чтобы сосредоточиться на важных сведениях.  

### Скрытие области фильтров  

По умолчанию DevTools отображает область **фильтров** .  
Щелкните **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы скрыть его.  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Кнопка скрыть фильтры"::: lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   Кнопка "скрыть фильтры"  
:::image-end:::  

### Использование строк большого запроса  

Используйте большие строки, если вы хотите, чтобы в таблице сетевых запросов больше пробелов.  Некоторые столбцы также содержат дополнительные сведения при использовании больших строк.  Например, минимальное значение столбца « **Размер** » — это несжатый размер запроса.  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Пример строк большого запроса в области запросы" ::: lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   Пример строк большого запроса в области " **запросы** "  
:::image-end:::  

Чтобы включить большие строки, включите флажок **использовать строки большого запроса** .  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Флажок использовать строки большого запроса"::: lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   Флажок " **использовать строки большого запроса** "  
:::image-end:::  

### Скрытие области обзора  

По умолчанию DevTools отображает область " **Обзор** ".  Чтобы скрыть его, отключите флажок **Показать обзор** .  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Флажок Показать общие сведения"::: lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   Флажок " **Показать общие сведения** "  
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

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Отладка последовательного веб-приложения | Документы Microsoft"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "URL-адреса данных | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Прокси-сервер — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
