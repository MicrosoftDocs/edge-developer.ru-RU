---
description: Учебник по наиболее популярным сетевым функциям в Microsoft Edge DevTools.
title: Проверка сетевой активности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a4a552fa9a45267a6ffa4a4e83e7ebc4e1817162
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439698"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a>Проверка сетевой активности в Microsoft Edge DevTools  

Это практический учебник некоторых наиболее часто используемых функций DevTools, связанных с проверкой сетевой активности страницы.  

Если вы хотите просмотреть функции, перейдите к [ссылке сети][DevtoolsNetworkReference].  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a>Когда использовать панель Network  

В общем случае используйте панель Network, когда необходимо убедиться, что ресурсы загружаются или загружаются как ожидалось.  Наиболее распространенными случаями использования панели Network являются:  

*   Убедитесь, что ресурсы фактически загружаются или загружаются вообще.  
*   Проверка свойств отдельного ресурса, таких как http-headers, контент, размер и т. д.  
    
Если вы ищете способы повышения производительности загрузки страниц, **не начинайте** с средства **Network.**  Существует множество типов проблем производительности нагрузки, не связанных с сетевой активностью.  Начните с панели Аудиты, так как она дает вам целенаправленные предложения по улучшению страницы.  Перейдите к [оптимизации скорости веб-сайта][DevtoolsSpeedGetStarted].  

## <a name="open-the-network-panel"></a>Откройте панель Network  

Чтобы получить больше всего от этого руководства, откройте демонстрацию и попробуйте функции на демо-странице.  

1.  Откройте [демонстрацию "Начало работы".][GlitchNetworkGetStarted]  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       Демонстрация  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  Чтобы [открыть DevTools,][DevToolsOpen] `Control` + `Shift` + `J` выберите \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).  Откроется **консольный** инструмент.  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Консоль" lightbox="../media/network-glitch-console.msft.png":::
       Консоль ****  
    :::image-end:::  
    
    Вы можете [пристыковать DevTools к нижней части окна.][DevToolsCustomizePlacement]  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools, пристыкованные к нижней части окна" lightbox="../media/network-glitch-console-bottom.msft.png":::
       DevTools, пристыкованные к нижней части окна  
    :::image-end:::  
    
1.  Откройте **средство Network.**  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Консольный инструмент в DevTools, пристыкованный к нижней части окна" lightbox="../media/network-glitch-network-bottom.msft.png":::
       **Консольный** инструмент в DevTools, пристыкованный к нижней части окна  
    :::image-end:::  
    
Сейчас средство **Network** пусто.  DevTools регистрит сетевое действие только после его открытия, и с момента открытия DevTools сетевой активности не было.  

## <a name="log-network-activity"></a>Сетевое действие журнала  

Чтобы просмотреть сетевое действие, которое вызывает страница:  

1.  Обновление веб-страницы.  Панель Network регистрит все сетевые действия в **журнале Сети.**  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Журнал сети" lightbox="../media/network-glitch-network.msft.png":::
       Журнал **сети**  
    :::image-end:::  
    
    Каждая строка **сетевого журнала** представляет ресурс.  По умолчанию ресурсы перечислены в хронологическом порядке.  Верхний ресурс обычно является основным HTML-документом.  Нижний ресурс — это все, что запрашивалось в последний раз.  
    
    Каждый столбец представляет сведения о ресурсе.  На предыдущем рисунке отображаются столбцы по умолчанию.  

    *   **Состояние**.  Код состояния HTTP для ответа.  
    *   **Тип**.  Тип ресурса.  
    *   **Инициатор**.  Причина запроса ресурса.  CHoosing a link in the Initiator column takes you to the source code that caused the request.  
    *   **Время**.  Продолжительность запроса.  
    *   **Водопад**.  Графическое представление различных этапов запроса.  Чтобы отобразить поломку, наведите курсор на водопад.  
    
    > [!NOTE]
    > График над журналом сети называется Обзором.  В этом руководстве не используется граф Обзор, поэтому его можно скрыть.  [Перейдите, чтобы скрыть области Обзор][DevtoolsReferenceHideOverview].
    
1.  После открытия DevTools записывалось сетевое действие в сетевом журнале.  
    Чтобы продемонстрировать это, сначала посмотрите **** в нижней части сетевого журнала и сделайте умственную заметку о последнем действии.  
1.  Теперь выберите кнопку **Get Data** в демонстрации.  
1.  Посмотрите в нижней части **сетевого журнала** еще раз.  Отображается новый ресурс `getstarted.json` с именем.  Чтобы вызвать запрос файла на веб-страницу, выберите кнопку **Get Data.**  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Новый ресурс в журнале network" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       Новый ресурс в **журнале network**  
    :::image-end:::  
    
## <a name="show-more-information"></a>Дополнительные сведения  

Столбцы сетевого журнала настраиваются.  Вы можете скрыть столбцы, которые вы не используете.  
Существует также множество столбцов, скрытых по умолчанию, которые могут оказаться полезными.  

1.  Наведите курсор на загон для таблицы сетевого журнала, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Домен**.  Домен каждого ресурса теперь показан.  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Включить столбец Домен" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       Включить столбец Домен  
    :::image-end:::  
    
    > [!TIP]
    > Чтобы просмотреть полный URL-адрес ресурса, наведите курсор на ячейку в столбце **Имя.**  
    
## <a name="simulate-a-slower-network-connection"></a>Имитация более медленного подключения к сети  

Сетевое подключение компьютера, используемого для создания сайтов, вероятно, быстрее сетевых подключений мобильных устройств пользователей.  С помощью регулирования страницы вы получите более лучшее представление о том, сколько времени занимает страница для загрузки на мобильном устройстве.  

1.  Выберите **отсев** регулирования, который по умолчанию устанавливается в **Online.**  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Включить регулирование" lightbox="../media/network-glitch-network-throttling.msft.png":::
       Включить регулирование  
    :::image-end:::  
    
1.  Выберите **медленную 3G**.  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Выбор медленного 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       Выбор медленного 3G  
    :::image-end:::  
    
1.  **Перезагрузить** в длительном прессе \( Перезагружать \) и затем выбрать ![ пустой ](../media/refresh-icon.msft.png) **кэш и твердую перезагрузку.**  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Пустой кэш и твердая перезагрузка" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **Пустой кэш и твердая перезагрузка**  
    :::image-end:::  
    
    При повторных посещениях браузер обычно обслуживает некоторые файлы из [кэша,][MDNHTTPCache]что ускоряет загрузку страницы.  **Пустой кэш и твердая перезагрузка** вынуждают браузер идти по сети для всех ресурсов.  Используйте его, чтобы отобразить, как первый посетитель испытывает нагрузку на страницу.  
    
    > [!NOTE]
    > Рабочий **процесс пустого кэша** и жесткой перезагрузки доступен только при открытом доступе DevTools.  
    
## <a name="capture-screenshots"></a>Захват скриншотов  

На скриншотах отображается внешний вид веб-страницы во время загрузки.  

1.  Выберите \. ![ Параметры ](../media/settings-icon.msft.png) сети \) и включив почтовый ящик **скриншотов** захвата.
1.  Снова обновите страницу с помощью рабочего **процесса Пустой кэш и** тяжелая перезагрузка.  Перейдите [к имитации более медленного подключения,](#simulate-a-slower-network-connection) если вам нужно напоминание о том, как это сделать.  
    На панели Screenshots представлены эскизы того, как страница выглядела в различных точках во время процесса загрузки.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Скриншоты загрузки страницы" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       Скриншоты загрузки страницы  
    :::image-end:::  
    
1.  Выберите первый эскиз.  DevTools показывает, какие сетевые действия происходили в этот момент времени.  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Сетевое действие, которое происходило во время первого скриншота" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       Сетевое действие, которое происходило во время первого скриншота  
    :::image-end:::  
    
1.  Выберите \. Параметры сети \) снова и отключите контрольный ящик скриншотов захвата, чтобы закрыть области ![ ](../media/settings-icon.msft.png) скриншотов. ****
1.  Снова обновите страницу.  
    
## <a name="inspect-the-details-of-the-resource"></a>Проверка сведений о ресурсе  

Выберите ресурс, чтобы узнать о нем дополнительные сведения.  Попробуйте его сейчас:  

1.  Выберите `getstarted.html` .  Показана панель **headers.**  Используйте эту панель для проверки http-заглавных заглав.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Панель "Заготки"" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       Панель **"Заготки"**  
    :::image-end:::  
    
1.  Выберите панель **Preview.**  Показана базовая визуализация HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Панель Предварительного просмотра" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       Панель **Предварительного** просмотра  
    :::image-end:::  
    
    Панель полезна, когда API возвращает код ошибки в HTML.  При проверке изображений может быть проще считыть отрисовка HTML, чем исходный код HTML.  

1.  Выберите панель **ответа.**  Показан исходный код HTML.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Панель ответов" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       Панель **ответов**  
    :::image-end:::  
    
    > [!TIP]
    > При минировании файла выберите кнопку **Format** \( Format \) в нижней части панели ответа для повторного формата содержимого файла для ![ ](../media/format-icon.msft.png) **** читаемости.  
    
1.  Выберите панель **Timing.**  Отображается разбивка сетевой активности для ресурса.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Панель синхронизации" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       Панель **синхронизации**  
    :::image-end:::  
    
1.  Выберите **Закрыть** \( Закрыть \) чтобы ![ снова ](../media/close-icon.msft.png) просмотреть журнал сети.  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Кнопка Закрыть" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       Кнопка **Закрыть**  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a>Заглавные главы и ответы в сети поиска  

Используйте области **Поиска,** когда необходимо искать http-заготки и ответы всех ресурсов для определенной строки или регулярного выражения.  

Например, предположим, что необходимо убедиться, что ваши ресурсы используют разумные **политики кэша.**  

<!--TODO: add cache policies section when available  -->

1.  Выберите **поиск** \. ![ Поиск ](../media/search-icon.msft.png) \).  Поле Поиска открывается слева от журнала Network.  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Области поиска" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       Области **поиска**  
    :::image-end:::  
    
1.  Введите `Cache-Control` и выберите `Enter` .  В области поиска перечислены все экземпляры, которые он находит в загонах ресурсов `Cache-Control` или контенте.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Результаты поиска Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       Результаты поиска по запросу  `Cache-Control`  
    :::image-end:::  
    
1.  Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.  Если вы ищете сведения о ресурсе, выберите результат, чтобы перейти непосредственно к ним.  Например, если запрос был найден в загонах, откроется панель **headers.**   Если запрос найден в содержимом, **откроется панель** ответа.  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Результат поиска, высветимый в панели Headers" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       Результат поиска, высветимый в панели **Headers**  
    :::image-end:::  
    
1.  Закрой панель поиска и панель **загона.**  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Кнопки Закрыть" lightbox="../media/network-glitch-network-search-close.msft.png":::
       Кнопки **Закрыть**  
    :::image-end:::  
    
## <a name="filter-resources"></a>Фильтрация ресурсов  

DevTools предоставляет множество процессов для фильтрации ресурсов, не имеющих отношения к поставленной задаче.  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Панель инструментов Filters" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   Панель **инструментов Filters**  
:::image-end:::  

Панель **инструментов Filters** должна быть включена по умолчанию.  Если нет:  

1.  Выберите **фильтр** \( ![ Фильтр ](../media/filter-icon.msft.png) \) для его демонстрации.  
    
### <a name="filter-by-string-regular-expression-or-property"></a>Фильтр по строке, регулярному выражению или свойству  

Текстовое поле **Filter** поддерживает множество различных типов фильтрации.  

1.  `png`Введите **текстовое поле Filter.**  Показаны только файлы, содержащие `png` текст.  В этом случае единственными файлами, которые соответствуют фильтру, являются изображения PNG.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Фильтр строки" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       Фильтр строки  
    :::image-end:::  
    
1.  Введите `/.*\.[cj]s+$/`.  DevTools отфильтровывает любой ресурс с иным файловым иным имям, которое не заканчивается с 1 или `j` `c` более `s` символов.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Фильтр регулярных выражений" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       Фильтр регулярных выражений  
    :::image-end:::  
    
1.  Введите `-main.css`.  DevTools отфильтровываю. `main.css`  Если какой-либо файл соответствует шаблону, синица также отфильтровыется.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Отрицательный фильтр" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       Отрицательный фильтр  
    :::image-end:::  
    
1.  `domain:cdn.glitch.com`Введите **текстовое поле Filter.**  DevTools отфильтровывает любой ресурс с URL-адресом, который не соответствует этому домену.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Фильтр свойств" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       Фильтр свойств  
    :::image-end:::  
    
    Полный список фильтруемых свойств перейдите к [запросам фильтрации по свойствам.][DevtoolsReferenceProperty]  
    
1.  Очистить **текстовое** поле Filter любого текста.  
    
### <a name="filter-by-resource-type"></a>Фильтр по типу ресурса  

Чтобы сосредоточиться на определенном типе файла, например таблицах стилей:  

1.  Выберите **CSS**.  Все другие типы файлов отфильтровыются.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Показать только файлы CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       Показать только файлы CSS  
    :::image-end:::  
    
1.  Чтобы также отображать скрипты, выберите и удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите **JS**.  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Показать только файлы CSS и JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       Показать только файлы CSS и JS  
    :::image-end:::  
    
1.  Чтобы удалить фильтры и снова отобразить все ресурсы, выберите **All**.  
    
Для других процессов фильтрации перейдите к [запросам фильтрации.][DevtoolsNetworkReferenceFilter]  

## <a name="block-requests"></a>Блокировка запросов  

Как выглядит и ведет себя страница, если некоторые ресурсы страницы недоступны?  Он полностью сбой или он все еще несколько функциональный?  Блокировка запросов, чтобы узнать:  

1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Меню команд" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       Меню **команд**  
    :::image-end:::  
    
1.  `block`Введите, **выберите показать блокировку запроса**и выберите `Enter` .  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Показать блокировку запросов" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **Показать блокировку запросов**  
    :::image-end:::  
    
1.  Выберите **Добавить шаблон** \. Добавьте шаблон ![ ](../media/add-icon.msft.png) \).  
1.  Введите `main.css`.  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Блокировка main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       Блокировка `main.css`  
    :::image-end:::  
    
1.  Выберите **Добавить**.  
1.  Обновите страницу.  Как и ожидалось, укладка страницы немного перепуталась, так как основной лист стилей был заблокирован.  
    
    > [!NOTE]
    > Строка `main.css` в сетевом журнале.  Красный текст означает, что ресурс заблокирован.
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css заблокирован" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` заблокирована  
    :::image-end:::  
    
1.  Deselect the **Enable request blocking** checkbox.  

## <a name="conclusion"></a>Заключение  

Поздравляем, вы завершили учебник.  Теперь вы знаете, как использовать средство **Network** в Microsoft Edge DevTools!

Перейдите к [ссылке на сеть,][DevtoolsNetworkReference] чтобы узнать больше функций DevTools, связанных с проверкой сетевой активности.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkReference]: ./reference.md "Справочные ссылки на | Документы Майкрософт"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы на фильтрацию — ссылки на | Документы Майкрософт"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрыть области Обзор — ссылки на анализ сети | Документы Майкрософт"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам — ссылки на | Документы Майкрософт"
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Проверка демонстрации сетевой активности | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Http кэш | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
