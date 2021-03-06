---
description: Всестороннюю ссылку на все функции и поведение, связанные с интерфейсом консоли в Microsoft Edge DevTools.
title: Ссылка консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399164"
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

# <a name="console-reference"></a>Ссылка консоли  

Эта страница является ссылкой на функции, связанные с консоли Microsoft Edge DevTools.  Предполагается, что вы уже знакомы с использованием консоли для просмотра зарегистрированных сообщений и запуска JavaScript.  Если нет, перейдите к [началу работы с запуском JavaScript в][DevToolsConsoleJavascript] консоли и начать работу с ведением журнала [сообщений в консоли][DevToolsConsoleLog].  

Если вы ищете ссылку API на такие `console.log()` функции, как, перейдите к [консоли API Reference][DevToolsConsoleApi].  Для справки о таких `monitorEvents()` функциях, как, перейдите к [ссылке API консоли utilities][DevToolsConsoleUtilities].  

## <a name="open-the-console"></a>Откройте консоль  

Консоль можно **открыть** как [средство](#open-the-console-tool) в верхней области или как средство [в ящике.](#open-the-console-tool-in-the-drawer)  

### <a name="open-the-console-tool"></a>Откройте средство Консоли  

Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Средство Консоли" lightbox="../media/console-hello-console.msft.png":::
   Средство **Консоли**  
:::image-end:::  

Чтобы открыть **консольный** инструмент из командного [меню,][DevToolsCommandMenu]начните вводить текст и запустите команду "Показать консоль", рядом с ней имеется значок `Console` **** **Панель.**  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда, чтобы показать панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   Команда, чтобы показать **средство Консоли**  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a>Откройте средство Консоли в ящике  

Выберите или выберите Настройка и `Escape` **управление DevTools** `...` \( \) и выберите **ящик консоли Show**.  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Показать ящик консоли" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **Показать ящик консоли**  
:::image-end:::  

Ящик всплывет в нижней части окна DevTools с открытым средством **консоли.**  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Средство консоли в ящике" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   Средство **консоли** в **ящике**  
:::image-end:::  

Чтобы открыть **консольный** инструмент из командного [меню,][DevToolsCommandMenu]начните вводить текст и запустите команду "Показать консоль", рядом с ней имеется значок `Console` **** **Ящика.**  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда, чтобы показать средство **Console** в ящике" lightbox="../media/console-command-menu-show-console.msft.png":::
   Команда, чтобы показать **консольный** инструмент в **ящике**  
:::image-end:::  

### <a name="open-console-settings"></a>Параметры открытой консоли  

Выберите **параметры** консоли \. ![ Значок Параметры ][ImageSettingsButtonIcon] консоли \).  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Параметры консоли" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **Параметры консоли**  
:::image-end:::  

Ссылки ниже объясняют каждый параметр:  

*   [**Скрыть сеть**](#hide-network-messages)  
*   [**Сохранение журнала**](#persist-messages-across-page-loads)  
*   [**Только выбранный контекст**](#filter-out-messages-from-different-contexts)  
*   [**Группа Similar**](#disable-message-grouping)  
*   [**Журнал XmlHttpRequests**](#log-xhr-and-fetch-requests)  
*   [**Оценка с желанием**](#disable-eager-evaluation)  
*   [**Автозаполнеть из истории**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a>Откройте боковую панель консоли  

Выберите **боковую панель** консоли показать \. Показать боковую панель консоли \) для демонстрации боковой панели, которая полезна ![ для ][ImageShowConsoleSidebarIcon] фильтрации.  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Боковая панель консоли" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   **Консоль** Боковая панель  
:::image-end:::  

## <a name="view-messages"></a>Просмотр сообщений  

В этом разделе содержатся функции, которые изменяют то, как сообщения представлены в консоли.  Для практических погон перейдите к [просмотру сообщений.][DevToolsConsoleViewMessages]  

### <a name="disable-message-grouping"></a>Отключение группировки сообщений  

[Откройте параметры консоли и](#open-console-settings) отключим **группу,** аналогичную отключению поведения группы сообщений по умолчанию консоли.  Например, перейдите к запросам [log XHR и Fetch](#log-xhr-and-fetch-requests).  

### <a name="log-xhr-and-fetch-requests"></a>Запросы на журнал XHR и fetch  

[Откройте параметры консоли](#open-console-settings) и вйдите **в журнал XMLHttpRequests** для входа всех и запросов в консоль по мере их `XMLHttpRequest` `Fetch` создания.  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Запросы журнала XMLHttpRequest и Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   Журнал `XMLHttpRequest` и `Fetch` запросы  
:::image-end:::  
В верхнем сообщении на предыдущем рисунке отображается поведение группы консоли по **умолчанию.**  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a>Упорязать сообщения во всех загрузках страниц  

По умолчанию консоль очищается при загрузке новой страницы.  Для сохранения сообщений в разных нагрузках страниц [откройте параметры](#open-console-settings) консоли и вйдите в почтовый ящик **Preserve Log.**  

### <a name="hide-network-messages"></a>Скрыть сетевые сообщения  

По умолчанию браузер регистрит сетевые сообщения в **консоли.**  На следующем рисунке выбранное сообщение представляет код состояния HTTP `429` .  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Сообщение 429 в консоли" lightbox="../media/console-show-network.msft.png":::
   Сообщение `429` в **консоли**  
:::image-end:::  
Чтобы скрыть сетевые сообщения:  

1.  [Параметры открытой консоли](#open-console-settings).  
1.  Включить **почтовый ящик Hide Network.**  
    
## <a name="filter-messages"></a>Фильтрация сообщений  

Существует множество способов фильтрации сообщений в консоли.  

### <a name="filter-out-browser-messages"></a>Фильтрация сообщений браузера  

[Откройте боковую панель консоли](#open-the-console-sidebar) и **выберите сообщения пользователей,** чтобы показать только сообщения, которые поступили из JavaScript страницы.  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Просмотр сообщений пользователей" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   Просмотр сообщений пользователей  
:::image-end:::  

### <a name="filter-by-log-level"></a>Фильтр по уровню журнала  

DevTools назначает каждому `console.*` методу уровень серьезности.  Существует 4 уровня: `Verbose` `Info` , , и `Warning` `Error` .  Например, `console.log()` находится в `Info` группе, в то время `console.error()` как в `Error` группе.  Ссылка [на API консоли][DevToolsConsoleApi] описывает уровень серьезности каждого применимого метода.  Каждое сообщение, которое браузер входит в консоль, также имеет уровень серьезности.  Вы можете скрыть любой уровень сообщений, который вас не интересует.  Например, если вас интересуют только сообщения, можно скрыть `Error` остальные 3 группы.  

Выберите **отсев уровней** журналов, чтобы включить или отключить `Verbose` `Info` `Warning` `Error` сообщения.  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Отсев уровней журналов" lightbox="../media/console-log-level-default-levels.msft.png":::
   **Отсев уровней** журналов  
:::image-end:::  

Вы также можете фильтровать по уровню [журнала,](#open-the-console-sidebar) открыв боковую панель консоли и затем вычеты **ошибок,** **** предупреждений, **info**или **Verbose**.  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Использование боковой панели для просмотра предупреждений" lightbox="../media/console-sidebar-warnings.msft.png":::
   Использование боковой панели для просмотра предупреждений  
:::image-end:::  

### <a name="filter-messages-by-url"></a>Фильтрация сообщений по URL-адресу  

Введите `url:` url-адрес, чтобы просматривать только сообщения, которые пришли из этого URL-адреса.  После введите `url:` DevTools показывает все релевантные URL-адреса.  Домены также работают.  Например, если вы и журналируете сообщения, вы можете сосредоточиться на сообщениях `https://example.com/a.js` `https://example.com/b.js` из этих `url:https://example.com` 2 скриптов.  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Фильтр URL-адреса" lightbox="../media/console-filter-text.msft.png":::
   Фильтр URL-адреса  
:::image-end:::  

`-url:`Введите, чтобы скрыть сообщения из этого URL-адреса.  Это называется фильтром отрицательного URL-адреса.  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Отрицательный URL-фильтр, который скрывает все сообщения, которые соответствуют https://b.wal.co URL-адресу" lightbox="../media/console-negative-filter-text.msft.png":::
   Отрицательный URL-фильтр, который скрывает все сообщения, которые соответствуют `https://b.wal.co` URL-адресу
:::image-end:::  

Вы также можете показывать сообщения из одного URL-адреса, открыв **** боковую панель [консоли,](#open-the-console-sidebar)расширив раздел "Сообщения пользователей", а затем нажав URL-адрес скрипта, содержащий сообщения, на которых необходимо сосредоточиться.  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Просмотр сообщений, которые поступили из wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   Просмотр сообщений, которые пришли из `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a>Фильтрация сообщений из разных контекстов  

Предположим, что на странице есть реклама \(ad\).  В консоль встроено большое количество `<iframe>` сообщений.  Так как это сообщение работает в другом контексте [JavaScript,](#select-javascript-context)одним [](#open-console-settings) из способов скрыть сообщения является открытие параметров консоли и включив выбранный почтовый ящик **Только** контекст.  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a>Фильтрация сообщений, не совпадает с шаблоном регулярных выражений  

Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовом окне **Filter,** чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.  DevTools проверяет, найден ли шаблон в тексте сообщения или скрипте, из-за чего сообщение было в журнале.  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Фильтрация сообщений, не совпадает с выражением regex" lightbox="../media/console-filter-regex.msft.png":::
   Фильтрация сообщений, не совпадает с `/[gm][ta][mi]/` выражением regex  
:::image-end:::  

## <a name="run-javascript"></a>Запуск JavaScript  

В этом разделе содержатся функции, связанные с запуском JavaScript в консоли.  Для практических походить перейдите к [запуску JavaScript][DevToolsConsoleOverviewJavascript].  

### <a name="re-run-expressions-from-history"></a>Повторное запуск выражений из истории  

Выберите ключ для цикла в истории выражений JavaScript, которые были ранее в `Up Arrow` консоли.  Выберите, `Enter` чтобы выполнить это выражение еще раз.  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a>Просмотр значения выражения в режиме реального времени с помощью Live Expressions  

Если вы напечатаете одно и то же выражение JavaScript в консоли несколько раз, вам может быть проще создать **выражение Live.**  С **помощью Live Expressions** вы введите выражение один раз, а затем прикрепите его к верхней части консоли.  Значение обновлений выражения почти в режиме реального времени.  Перейдите [к просмотру значений выражения JavaScript в Real-Time с живыми выражениями][DevToolsConsoleLiveExpressions].  

### <a name="disable-eager-evaluation"></a>Отключение оценки нетерпеливых  

При вписывке выражений JavaScript в консоли **в режиме "Нетерпеливые** оценки" показан предварительный просмотр возвращаемого значения для этого выражения.  [Откройте параметры консоли и](#open-console-settings) отключите контрольный ящик **"Нетерпеливые** оценки", чтобы отключить предварительные просмотры возвращаемой стоимости.  

### <a name="disable-autocomplete-from-history"></a>Отключение автокомплекта из истории  

При введите выражение, в окне всплывающее окно автокомплета консоли показаны выражения, которые вы запустили ранее.  Эти выражения предварительно примыкают к `>` символу.  [Откройте параметры консоли](#open-console-settings) и отключите автоматический автомат из почтового ящика **"История",** чтобы перестать показывать выражения из вашей истории.  

> [!NOTE]
> На следующем рисунке `document.querySelector('a')` и `document.querySelector('img')` находятся выражения, которые были оценены ранее.  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Всплывающее всплывающее всплывающее окантовка автокомплекта отображает выражения из истории" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   Всплывающее всплывающее всплывающее окантовка автокомплекта отображает выражения из истории  
:::image-end:::  

### <a name="select-javascript-context"></a>Выбор контекста JavaScript  

По умолчанию **выпадение контекста JavaScript** устанавливается на [][MDNBrowsingContext] вершину, **** что представляет контекст просмотра основного документа.  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Отсев контекста JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   **Отсев контекста JavaScript**  
:::image-end:::  

Предположим, у вас есть на странице, встроенная в `<iframe>` .  Необходимо запустить JavaScript, чтобы настроить DOM этого ad.  Сначала необходимо выбрать контекст просмотра рекламы из выпадаемого **контекста JavaScript.**  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Выберите другой контекст JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   Выберите другой контекст JavaScript  
:::image-end:::  

## <a name="clear-the-console"></a>Очистка консоли  

Для очистки консоли можно использовать любой из следующих процессов:  

*   Выберите **четкую** консоль \. ![ Четкая ][ImageClearConsoleIcon] консоль \).  
*   Наведите курсор на сообщение, откройте контекстное меню \(righ-click\) и выберите **четкую консоль**.  
*   Введите `clear()` консоль **и** выберите `Enter` .  
*   Запуск `console.clear()` с JavaScript для веб-страницы.  
*   Выберите, `Control` + `L` **пока консоль** находится в фокусе.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Просмотр зарегистрированных сообщений — обзор консоли | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочные | Документы Майкрософт"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Запуск JavaScript — обзор консоли | Документы Майкрософт"  
[DevToolsConsoleJavascript]: ./javascript.md "Начало работы с запуском JavaScript в консоли | Документы Майкрософт"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Просмотр значений выражений JavaScript в режиме реального времени с помощью live Expressions | Документы Майкрософт"  
[DevToolsConsoleLog]: ./log.md "Начало работы с ведением журналов сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочные ссылки на API консоли utilities | Документы Майкрософт"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Просмотр контекста | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
