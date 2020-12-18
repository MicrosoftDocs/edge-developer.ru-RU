---
description: Узнайте, как занося сообщения в консоль.
title: Начало работы с ведением журнала сообщений в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2f91f1847bf5469e8106edc21553172fc06db9ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231113"
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

# Начало работы с ведением журнала сообщений в консоли  

В этом интерактивном руководстве показано, как занося сообщения в журнал и фильтровать их в консоли [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения в консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Сообщения в **консоли**  
:::image-end:::  

Это руководство предназначено для завершения по порядку.  Предполагается, что вы понимаете основы веб-разработки, такие как использование JavaScript для добавления интерактивности на страницу.  

## Настройка демонстрации и DevTools  

Это руководство предназначено для того, чтобы вы могли открыть демонстрацию и попробовать все процессы самостоятельно.  Когда вы будете физически следовать этому пути, скорее всего, позже запомните эти процессы.  

1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.  
    
    [Примеры журнала консоли][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Сконцентрируем демонстрацию и выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\), чтобы открыть DevTools.  По умолчанию DevTools открывается справа от демонстрации.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools откроется справа от демонстрации" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools откроется справа от демонстрации  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Закрепление DevTools в нижней части окна.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools, закрепленный в нижней части демонстрации" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools, закрепленный в нижней части демонстрации  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Undock DevTools в отдельное окно.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Браузер в отдельном окне" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Браузер в отдельном окне  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Undock DevTools в отдельное окно.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Отсоединая отсоединая от devTools в отдельном окне" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             Отсоединая отсоединая от devTools в отдельном окне  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Просмотр сообщений, зарегистрированных на JavaScript  

Большинство сообщений, отображаемого **** в консоли, приходят от веб-разработчиков, которые написали JavaScript страницы.  Цель этого раздела — познакомить вас с различными типами сообщений, которые вы, скорее всего, будете рассматривать в **консоли,** и объяснить, как вы можете самостоятельно вносить в журнал каждый тип сообщения из собственного кода JavaScript.  

1.  В **демонстрации выберите** кнопку "Сведения журнала".  `Hello, Console!` регистрируется в консоли.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Консоль после выбора данных журнала" lightbox="../media/console-log-info.msft.png":::
       Консоль **после** выбора данных **журнала**  
    :::image-end:::  
    
1.  Рядом с сообщением в консоли выберите `Hello, Console!` **log.js:2**.  Откроется панель источников и выделена строка кода, из-за чего сообщение было зарегистрировано в консоли.  Сообщение занося в журнал, когда был занося в журнал JavaScript `console.log('Hello, Console!')` страницы.
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools открывает панель источников после выбора log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools открывает панель **источников** после выбора `log.js:2`  
    :::image-end:::  
    
1.  Перейдите к консоли **с** помощью любого из следующих процессов:  
    
    *   Выберите **вкладку "Консоль".**  
    *   Выберите `Control` + `[` \(Windows, Linux\) или `Command` + `[` \(macOS\), **** пока панель консоли не будет в фокусе.  
    *   [Откройте меню команд,][DevToolsCommandMenu]введите команду "Показать консольную `Console` **панель",** а затем выберите `Enter` .  
    
1.  В **демонстрации выберите кнопку** "Предупреждение журнала".  `Abandon Hope All Ye Who Enter` регистрируется в **консоли.**  Сообщения в таком формате являются предупреждениями.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Консоль после выбора предупреждения журнала" lightbox="../media/console-log-warning.msft.png":::
       Консоль **после** выбора предупреждения **журнала**  
    :::image-end:::  
    
    > [!TIP]
    > Если вы хотите отобразить код, который вызвал определенное внесение сообщения в журнал, выберите сценарий \(например, \), чтобы просмотреть код, который вызвал форматирование `log.js:12` сообщения.  

1.  Choose the **Expand** \( ![ Expand ][ImageExpandIcon] \) icon in front of `Abandon Hope All Ye Who Enter` .  DevTools отображает [трассировку стека][WikiStackTrace] перед вызовом.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Трассировка стека" lightbox="../media/console-log-warning-expanded.msft.png":::
       Трассировка стека  
    :::image-end:::  
    
    Трассировка стека говорит о том, что выполняется функция с именем, которая, в свою `logWarning` очередь, выполняет функцию с именем `quoteDante` .  Другими словами, первый запрос находится в нижней части трассировки стека.  Вы можете в любое время занося трассировки стека в `console.trace()` журнал.  

1.  Choose **Log Error**.  Занося в журнал следующее сообщение об ошибке: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщение об ошибке" lightbox="../media/console-log-error.msft.png":::
       Сообщение об ошибке  
    :::image-end:::  
    
1.  Choose **Log Table**.  Таблица о неявных исполнителях записируется **в**консоль.  
    
    > [!NOTE]
    > Столбец `birthday` заполняется только для одной строки.  Просмотрите код, чтобы определить, почему это так.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Таблица в консоли" lightbox="../media/console-log-table.msft.png":::
       Таблица **в** консоли  
    :::image-end:::  
    
1.  Выберите **группу журналов.**  Под меткой сгруппировка имен 4 -х- и хламов, где ведется `Adolescent Irradiated Espionage Tortoises` группировка.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Группа сообщений в консоли" lightbox="../media/console-log-group.msft.png":::
       Группа сообщений в **консоли**  
    :::image-end:::  
    
1.  Choose **Log Custom**.  Сообщение с красной границей и синим фоном регистрируется в консоли.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщение с пользовательским форматированием в консоли" lightbox="../media/console-log-custom.msft.png":::
       Сообщение с пользовательским форматированием **в** консоли  
    :::image-end:::  
    
Основная идея заключается в том, что при регистрации сообщений в консоли из JavaScript используется один из `console` методов.  Каждый метод форматирование сообщений по-разному.  

Существует еще больше методов, чем показано в этом разделе.  В этом руководстве показано, как изучить остальные методы.  

## Просмотр сообщений, зарегистрированных браузером  

Браузер также записи сообщений в консоль.  Обычно это происходит при проблеме со страницей.  

1.  Choose **Cause 404**.  Браузер записи в журнал кода состояния HTTP сетевой ошибки, так как Код JavaScript страницы пытался получить файл, `404` который не существует.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ошибка 404 в консоли" lightbox="../media/console-cause-404.msft.png":::
       Ошибка `404` в **** консоли  
    :::image-end:::  
    
1.  Choose **Cause Error**.  Браузер занося в журнал ненагрузку, так как JavaScript пытается обновить узел `TypeError` DOM, который не существует.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError в консоли" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` в **** консоли  
    :::image-end:::  
    
1.  Выберите в **качестве входного** параметра "Уровни журнала" и включите параметр **"Подробно",** если он отключен.  Подробнее о фильтрации вы узнаете в следующем разделе.  Это необходимо сделать, чтобы убедиться, что следующее сообщение, занося в журнал, будет видимым.  
    
    > [!NOTE]
    > Если выпадание уровней по умолчанию отключено, может потребоваться закрыть **боковую панель** консоли.  Фильтрация по источнику сообщений ниже для получения дополнительных сведений о **боковой панели** консоли.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Включение уровня подробного журнала" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Включение уровня подробного журнала  
    :::image-end:::  
    
1.  Выберите **"Причина нарушения".**  Страница в течение нескольких секунд становится неотвечивой, а затем браузер записи сообщения в `[Violation] 'click' handler took 3000ms` консоль.  Точная длительность может отличаться.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Нарушение в консоли" lightbox="../media/console-cause-violation.msft.png":::
       Нарушение в **консоли**  
    :::image-end:::  
    
## Фильтрация сообщений  

На некоторых веб-страницы, **** на которые вы просматриваете консоль, переполнили сообщения.  DevTools предоставляет множество различных способов фильтрации сообщений, не соответствующих задаче.  

### Фильтрация по уровню журнала  

Каждому `console` методу назначена степень серьезности: `Verbose` , , , или `Info` `Warning` `Error` .  Например, `console.log()` это сообщение уровня, а `Info` сообщение `console.error()` `Error` уровня.  

1.  Выберите в **поле "Уровни журнала"** и отключите **ошибки.**  Уровень отключается, если рядом с ней больше нет контрольного знака.  Сообщения `Error` уровня исчезают.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Отключение сообщений уровня ошибки в консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Отключение сообщений уровня ошибки в **консоли**  
    :::image-end:::  
    
1.  Снова выберите **"Уровни** журнала" и снова вйдите в **"Ошибки".**  Сообщения `Error` уровня снова появляются.  

### Фильтрация по тексту  

Если вы хотите просматривать только сообщения с точной строкой, введите эту строку в **текстовое** поле фильтра.  

1.  Введите `Dave` в **текстовое поле фильтра.**  Все сообщения, которые не включают `Dave` строку, скрыты.  Вы также можете просмотреть `Adolescent Irradiated Espionage Tortoises` метку.  Это ошибка.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Фильтрация всех сообщений, не включаемая в список Ю." lightbox="../media/console-all-messages-text-filter.msft.png":::
       Фильтрация всех сообщений, которые не включены `Dave`  
    :::image-end:::  
    
1.  Удалите `Dave` из **текстового окна фильтра.**  Все сообщения снова появляются.  

### Фильтрация по регулярному выражению  

Если вы хотите показать все сообщения, которые содержат шаблон текста, а не определенную строку, используйте [регулярное выражение.][MDNRegularExpressions]  

1.  Введите `/^[AH]/` в **текстовое поле фильтра.**  Введите этот шаблон [в RegExr,][|::ref1::|Main] чтобы объяснить, что он делает.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Фильтрация сообщений, не совпадающих с шаблоном" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Фильтрация сообщений, не совпадающих с шаблоном `/^[AH]/`  
    :::image-end:::  
    
1.  Удалите `/^[AH]/` из **текстового окна фильтра.**  Все сообщения снова будут видны.  

### Фильтрация по источнику сообщений  

Если вы хотите просматривать только сообщения, которые поступили с определенного URL-адреса, используйте **боковую панель.**  

1.  Choose **Show Console Sidebar** \( ![ Show Console Sidebar ][ImageShowConsoleSidebarIcon] \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Боковая панель" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Боковая панель  
    :::image-end:::  
    
1.  Выберите **значок "Развернуть"** рядом с числом ![ ][ImageExpandIcon] сообщений.  На следующем рисунке число сообщений указано как **13 сообщений.**  На **боковой панели** показан список URL-адресов, которые привели к записи сообщений в журнал.  Например, `log.js` вызвано 11 сообщений.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Просмотр источника сообщений на боковой панели" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Просмотр источника сообщений на боковой панели  
    :::image-end:::  
    
### Фильтрация по пользовательским сообщениям  

Ранее при выборе log **Info**сценарий, именуемой для регистрации `console.log('Hello, Console!')` сообщения в консоли.  Сообщения, зарегистрированные на JavaScript, такие как это, называются **пользовательскими**сообщениями.  Напротив, при выборе **причины 404**браузер регистрирует сообщение уровня о том, что запрашиваемого ресурса `Error` не удалось найти.  Такие сообщения считаются сообщениями **браузера.**  Используйте **боковую панель для** фильтрации сообщений браузера и только для показа сообщений пользователей.  

1.  Выберите **9 пользовательских сообщений.**  Сообщения браузера скрыты.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Фильтрация сообщений браузера" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Фильтрация сообщений браузера  
    :::image-end:::  
    
1.  Выберите **13 сообщений,** чтобы снова показать все сообщения.  

## Использование консоли наряду с любой другой панелью  

Что делать, если вы редактируете стили, но вам нужно быстро проверить журнал консоли?  Используйте drawer.  

1.  Выберите **вкладку "Элементы".**  
1.  Выберите `Escape` .  Откроется вкладка "Консоль" **в drawer.** ****  Он содержит все функции панели консоли, которые вы использовали в этом руководстве.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Вкладка "Консоль" в "Ящике"" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Вкладка **"Консоль"** в **"Ящике"**  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   Navigate to [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   Navigate to [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md "Справочник по консоли | Документы Майкрософт"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с ведением журнала сообщений | Временный сбой"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедия"  
> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/console/log) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
