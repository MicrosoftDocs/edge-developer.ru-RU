---
description: Учебник по наиболее популярным сетевым функциям в Microsoft Edge DevTools.
title: Проверка сетевой активности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1874c6222798755aa5ad7002e22b0cef00c8fd41
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230980"
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

# Проверка сетевой активности в Microsoft Edge DevTools  

Это практический учебник по некоторым наиболее часто используемым функциям DevTools, связанным с проверкой сетевой активности страницы.  

Если [вы хотите][DevtoolsNetworkReference] просмотреть функции, см. справку по сети.  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Когда использовать панель "Сеть"  

Как правило, используйте панель "Сеть", чтобы убедиться, что ресурсы загружаются или загружаются ожидаемым образом.  Наиболее распространенные случаи использования для панели "Сеть":  

*   Убедитесь, что ресурсы фактически загружаются или загружаются.  
*   Проверка свойств отдельного ресурса, таких как http-загодеры, содержимое, размер и т. д.  
    
Если вы ищете способы повышения производительности загрузки страницы, **не** начинайте с средства **"Сеть".**  Существует множество типов проблем с производительностью нагрузки, не связанных с сетевой активностью.  Начните с панели "Аудит", так как она дает вам рекомендации по улучшению страницы.  Перейдите к [оптимизации скорости веб-сайта.][DevtoolsSpeedGetStarted]  

## Открытие панели "Сеть"  

Чтобы получить все возможности из этого руководства, откройте демонстрацию и попробуйте функции на странице демонстрации.  

1.  Откройте [демонстрационную версию "Начало работы".][GlitchNetworkGetStarted]  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Демонстрация  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  [Откройте DevTools,][DevToolsOpen] нажав `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).  Откроется **средство** консоли.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Консоль" lightbox="../media/network-glitch-console.msft.png":::
       Консоль ****  
    :::image-end:::  
    
    Вы можете [пристыковать DevTools к нижней части окна.][DevToolsCustomizePlacement]  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools, закрепленный в нижней части окна" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools, закрепленный в нижней части окна  
    :::image-end:::  
    
1.  Выберите **вкладку "Сеть".**  Откроется **панель** "Сеть".  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Консольное средство в DevTools, закрепленное в нижней части окна" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Консольное** средство в DevTools, закрепленное в нижней части окна  
    :::image-end:::  
    
Сейчас панель "Сеть" пуста.  DevTools записывает сетевое действие только после его открытия, и с момента открытия DevTools никаких сетевых действий не было.  

## Запись сетевой активности в журнал  

Чтобы просмотреть сетевое действие, которое вызывает страница:  

1.  Перезагрузите страницу.  Панель "Сеть" записи всех сетевых действий в журнал **сети.**  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Сетевой журнал" lightbox="../media/network-glitch-network.msft.png":::
       Сетевой **журнал**  
    :::image-end:::  
    
    Каждая строка **сетевого журнала** представляет ресурс.  По умолчанию ресурсы перечислены в хронологическом порядке.  Верхний ресурс обычно является основным HTML-документом.  Нижний ресурс — это ресурс, который был запросрош последним.  
    
    Каждый столбец представляет сведения о ресурсе.  На предыдущем рисунке отображаются столбцы по умолчанию.  

    *   **Состояние**.  Код состояния HTTP для ответа.  
    *   **Тип**.  Тип ресурса.  
    *   **Инициатор .**  Причина запроса ресурса.  При выборе ссылки в столбце "Инициатор" вы будете перенабором кода, который вызвал запрос.  
    *   **Time**.  Продолжительность запроса.  
    *   **Каскад .**  Графическое представление различных этапов запроса.  Наведите курсор на каскадный каскад, чтобы увидеть разбивку.  
    
    > [!NOTE]
    > График над журналом сети называется обзором.  Вы не будете использовать график "Обзор" в этом руководстве, поэтому можете скрыть его.  См. ["Скрытие области обзора".][DevtoolsReferenceHideOverview]
    
1.  После открытия DevTools он записи сетевой активности в сетевой журнал.  
    Чтобы продемонстрировать это, сначала посмотрите **** в нижнюю часть сетевого журнала и заметьте последнее действие.  
1.  Теперь выберите кнопку **"Получить данные"** в демонстрации.  
1.  Еще раз посмотрите на нижнюю **часть сетевого журнала.**  Вы увидите новый ресурс под названием `getstarted.json` .  При **нажатии кнопки "Получить данные"** страница запросила этот файл.  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Новый ресурс в сетевом журнале" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Новый ресурс в **сетевом журнале**  
    :::image-end:::  
    
## Показать дополнительные сведения  

Столбцы сетевого журнала настраиваются.  Вы можете скрыть столбцы, которые не используете.  
Также существует много скрытых по умолчанию столбцов, которые могут оказаться полезными.  

1.  Наведите курсор на загон таблицы "Журнал сети", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Домен".**  Теперь отображается домен каждого ресурса.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Включить столбец Домен" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Включить столбец "Домен"  
    :::image-end:::  
    
    > [!TIP]
    > Чтобы увидеть полный URL-адрес ресурса, наведите курсор на ячейку в столбце **"Имя".**  
    
## Имитация более медленного сетевого подключения  

Сетевое подключение компьютера, используемого для создания сайтов, скорее всего, быстрее, чем сетевые подключения мобильных устройств пользователей.  Регулирование страницы позволяет лучше понять, сколько времени занимает страница для загрузки на мобильное устройство.  

1.  Выберите в **этом выпадаемом окне** значение **Online** по умолчанию.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Включить регулирование" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Включить регулирование  
    :::image-end:::  
    
1.  Choose **Slow 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Выбор медленной 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Выбор медленной 3G  
    :::image-end:::  
    
1.  Reload \( **Reload** ![ \( Reload ][ImageRefreshIcon] \) и выберите **пустой кэш и твердую перезагрузку.**  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Пустой кэш и неостановленная перезагрузка" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Пустой кэш и неостановленная перезагрузка**  
    :::image-end:::  
    
    При повторном посещении браузер обычно [][MDNHTTPCache]обслуживает некоторые файлы из кэша, что ускоряет загрузку страницы.  **Пустой кэш и твердая перезагрузка** заставляет браузер переходить по сети для всех ресурсов.  Это полезно, если вы хотите увидеть, как посетитель в первый раз видит загрузку страницы.  
    
    > [!NOTE]
    > Рабочий **процесс пустого кэша** и жесткой перезагрузки доступен, только если открыт DevTools.  
    
## Снимки экрана  

Screenshots let you see how a page looked over time while it was loading.  

1.  Choose \( ![ Network settings ][ImageSettingsIcon] \) and turn on the **Capture screenshots** checkbox.
1.  Обновите страницу еще раз с помощью рабочего процесса "Пустой кэш" и **"Неокрепленная** перезагрузка".  Если вам [нужно](#simulate-a-slower-network-connection) напоминание о том, как это сделать, перейдите к "Имитация медленных подключений".  
    На области "Снимки экрана" представлены эскизы того, как страница выглядела в различных точках во время загрузки.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Снимки экрана загрузки страницы" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Снимки экрана загрузки страницы  
    :::image-end:::  
    
1.  Выберите первый эскиз.  DevTools показывает, какие сетевые действия происходили в этот момент времени.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Сетевое действие, которое происходило на первом снимке экрана" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Сетевое действие, которое происходило на первом снимке экрана  
    :::image-end:::  
    
1.  Снова выберите \( Параметры сети \) и отключите снимок экрана для закрытия области ![ ][ImageSettingsIcon] снимков экрана. ****
1.  Обновите страницу еще раз.  
    
## Проверка сведений о ресурсе  

Выберите ресурс, чтобы получить дополнительные сведения о нем.  Попробуйте сделать это сейчас:  

1.  Выберите `getstarted.html` .  Отображается **вкладка** "Заглавные".  Эта вкладка используется для проверки http-headers.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Вкладка Заглавные" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Вкладка **"Заглавные"**  
    :::image-end:::  
    
1.  Выберите вкладку **"Предварительный** просмотр".  Показана базовая отрисовка HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Вкладка Предварительный просмотр" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Вкладка **"Предварительный** просмотр"  
    :::image-end:::  
    
    Вкладка полезна, когда API возвращает код ошибки в HTML.  Может оказаться, что проще читать отрисовки HTML, чем исходный код HTML, или при проверке изображений.  

1.  Выберите **вкладку "Ответ".**  Показан исходный код HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Вкладка Ответ" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Вкладка **"Ответ"**  
    :::image-end:::  
    
    > [!TIP]
    > При минифицировании файла выберите кнопку **Format** \( Format \) в нижней части вкладки "Ответ", чтобы повторно отформатирование содержимого файла для ![ ][ImageFormatIcon] **** учитаемости.  
    
1.  Выберите вкладку **"Время".**  Отображается разбивка сетевой активности ресурса.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Вкладка Время" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Вкладка **"Время"**  
    :::image-end:::  
    
1.  Choose **Close** \( ![ Close ][ImageCloseIcon] \) to view the Network Log again.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Кнопка Закрыть" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Кнопка **"Закрыть"**  
    :::image-end:::  
    
## Поиск в сетевых загонах и ответах  

Используйте поиск **в области** поиска, если необходимо искать определенные строки или регулярные выражения в http-загонах и ответах всех ресурсов.  

Например, предположим, что вы хотите убедиться, что ресурсы используют разумные **политики кэша.**  

<!--TODO: add cache policies section when available  -->

1.  Choose **Search** \( ![ Search ][ImageSearchIcon] \).  Слева от сетевого журнала откроется окно поиска.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="The Search pane" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       The **Search** pane  
    :::image-end:::  
    
1.  Введите `Cache-Control` и выберите `Enter` .  В области поиска перечислены все экземпляры, которые она находит в `Cache-Control` загонах ресурсов или содержимом.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Результаты поиска для Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Результаты поиска по запросу  `Cache-Control`  
    :::image-end:::  
    
1.  Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.  Если вы ищете сведения о ресурсе, выберите результат, чтобы перейти непосредственно к ресурсу.  Например, если запрос был найден в заголке, откроется вкладка "Headers".   Если запрос найден в содержимом, откроется вкладка **"Ответ".**  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Результат поиска, выделенный на вкладке Headers" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Результат поиска, выделенный на **вкладке "Headers"**  
    :::image-end:::  
    
1.  Закроем области поиска и вкладку "Headers".  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Кнопки закрытия" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Кнопки **закрытия**  
    :::image-end:::  
    
## Фильтрация ресурсов  

DevTools предоставляет множество процессов для фильтрации ресурсов, не имеющих отношения к задаче.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Панель инструментов Фильтры" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Панель **инструментов "Фильтры"**  
:::image-end:::  

Панель **инструментов фильтров** должна быть включена по умолчанию.  Если нет:  

1.  Выберите **фильтр** \( ![ Фильтр ][ImageFilterIcon] \), чтобы отдемонстрировать его.  
    
### Фильтрация по строке, регулярному выражению или свойству  

**Текстовое** поле фильтра поддерживает различные типы фильтрации.  

1.  Введите `png` в **текстовое поле фильтра.**  Будут показаны только файлы, содержащие `png` текст.  В этом случае единственными файлами, которые соответствуют фильтру, являются изображения PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Фильтр строк" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Фильтр строк  
    :::image-end:::  
    
1.  Введите `/.*\.[cj]s+$/`.  DevTools отфильтровывает любой ресурс с именом файла, который не заканчивается на 1 или более `j` `c` `s` символов.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Фильтр регулярных выражений" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Фильтр регулярных выражений  
    :::image-end:::  
    
1.  Введите `-main.css`.  Фильтры DevTools `main.css` .  Если какой-либо другой файл соответствует шаблону, он также будет отфильтрован.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Отрицательный фильтр" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Отрицательный фильтр  
    :::image-end:::  
    
1.  Введите `domain:cdn.glitch.com` в **текстовое поле** "Фильтр".  DevTools отфильтровывает любой ресурс с URL-адресом, который не соответствует этому домену.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Фильтр свойств" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Фильтр свойств  
    :::image-end:::  
    
    Полный [список фильтруемых][DevtoolsReferenceProperty] свойств см. в запросах фильтра по свойствам.  
    
1.  Очищает **текстовое** поле фильтра для любого текста.  
    
### Фильтрация по типу ресурса  

Чтобы сосредоточиться на определенном типе файлов, таких как таблицы стилей:  

1.  Выберите **CSS.**  Все остальные типы файлов отфильтровыются.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Показывать только CSS-файлы" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Показывать только CSS-файлы  
    :::image-end:::  
    
1.  Чтобы также увидеть сценарии, удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите **JS.**  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Показывать только CSS- и JS-файлы" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Показывать только CSS- и JS-файлы  
    :::image-end:::  
    
1.  Выберите **"Все",** чтобы удалить фильтры и снова увидеть все ресурсы.  
    
См. [запросы фильтра][DevtoolsNetworkReferenceFilter] для других процессов фильтрации.  

## Блокировка запросов  

Как выглядит и работает страница, когда некоторые ресурсы страницы недоступны?  Полностью ли он дает сбой или по-прежнему работает?  Блокируют запросы, чтобы узнать:  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Меню команд" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  `block`Введите, **выберите "Показать блокирование запросов"** и "Выбрать". `Enter`  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Показать блокирование запросов" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Показать блокирование запросов**  
    :::image-end:::  
    
1.  Choose **Add Pattern** \( Add Pattern ![ ][ImageAddIcon] \).  
1.  Введите `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Блокировка main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Блокировка `main.css`  
    :::image-end:::  
    
1.  Choose **Add**.  
1.  Перезагрузите страницу.  Как и ожидалось, оформление страницы немного перепутано, так как основная таблица стилей заблокирована.  
    
    > [!NOTE]
    > Строка `main.css` в сетевом журнале.  Красный текст означает, что ресурс заблокирован.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css заблокирован" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` заблокировано  
    :::image-end:::  
    
1.  Отбрасыйте этот **блокирующий запрос.**  

## Заключение  

Поздравляем, вы завершили учебное руководство.  Теперь вы знаете, как использовать панель **"Сеть"** в Microsoft Edge DevTools!

Перейдите в [справочник по сети,][DevtoolsNetworkReference] чтобы найти дополнительные функции DevTools, связанные с проверкой сетевой активности.  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkReference]: ./reference.md "Справочник по анализу сети | Документы Майкрософт"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы фильтра — справочник по анализу сети | Документы Майкрософт"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрытие области обзора — справочник по анализу сети | Документы Майкрософт"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам — справочник по анализу сети | Документы Майкрософт"
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Проверка демонстрации сетевой активности | Временный сбой"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэшинг HTTP | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/network/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
