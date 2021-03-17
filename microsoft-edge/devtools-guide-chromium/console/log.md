---
description: Узнайте, как войти сообщения в консоль.
title: Начало работы с ведением журналов сообщений в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: fb428154b00959db1627096819c565dd5dc11346
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439291"
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

# <a name="get-started-with-logging-messages-in-the-console"></a>Начало работы с ведением журналов сообщений в консоли  

В этом интерактивном учебнике показано, как журнал и фильтрация сообщений в [консоли Microsoft Edge DevTools.][MicrosoftEdgeDevTools]  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Сообщения в консоли" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   Сообщения в **консоли**  
:::image-end:::  

Этот учебник предназначен для завершения в порядке.  Предполагается, что вы понимаете основы веб-разработки, например использование JavaScript для добавления интерактивности на страницу.  

## <a name="set-up-the-demo-and-devtools"></a>Настройка демонстрации и DevTools  

Этот учебник разработан таким образом, чтобы вы могли открыть демонстрацию и попробовать все процессы самостоятельно.  Когда вы физически следуете за ними, вы с большей вероятностью запомните рабочий процесс позже.  

1.  Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) **** и выберите примеры журнала консоли для открытия на новой вкладке.  
    
    [Примеры журнала консоли][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  Уделяем внимание демонстрации, а затем выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\) для открытия DevTools.  По умолчанию DevTools открывается справа от демонстрации.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools открывается справа от демонстрации" lightbox="../media/console-example-devtools-right-console.msft.png":::
             DevTools открывается справа от демонстрации  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Dock DevTools в нижней части окна.][DevToolsCustomizePlacement]  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools, пристыкованные к нижней части демонстрации" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             DevTools, пристыкованные к нижней части демонстрации  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > [Undock DevTools в отдельное окно][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Браузер в отдельном окне" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             Браузер в отдельном окне  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > [Undock DevTools в отдельное окно][DevToolsCustomizePlacement].  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools, отсоединая в отдельном окне" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             DevTools, отсоединая в отдельном окне  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a>Просмотр сообщений, в журнале из JavaScript  

Большинство сообщений, отображаемого **** в консоли, приходят от веб-разработчиков, которые написали JavaScript страницы.  Цель этого раздела состоит в том, чтобы познакомить вас с различными типами сообщений, которые можно просмотреть в **консоли,** и объяснить, как можно самостоятельно войти в каждый тип сообщения из собственного JavaScript.  

1.  Выберите **кнопку Log Info** в демонстрации.  `Hello, Console!` получает войти в консоль.
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Консоль после выбора информации журнала" lightbox="../media/console-log-info.msft.png":::
       Консоль **после** выбора информации **журнала**  
    :::image-end:::  
    
1.  Рядом с `Hello, Console!` сообщением в консоли выберите **log.js:2**.  Панель Источников открывает и выделяет строку кода, из-за чего сообщение было занесно в консоль.  Сообщение было в журнале, когда javaScript страницы побежал `console.log('Hello, Console!')` .
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools открывает средство Sources после выбора log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       DevTools открывает средство **Sources** после выбора `log.js:2`  
    :::image-end:::  
    
1.  Возвращайтесь к консоли **с** помощью любого из следующих процессов:  
    
    *   Выберите **средство Консоли.**  
    *   Выберите `Control` + `[` \(Windows, Linux\) `Command` + `[` или \(macOS\) до **** тех пор, пока средство консоли не будет в фокусе.  
    *   [Откройте командное меню,][DevToolsCommandMenu] `Console` введите, выберите команду Панель консоли **Show,** а затем выберите `Enter` .  
    
1.  Выберите **кнопку Предупреждение журнала** в демонстрации.  `Abandon Hope All Ye Who Enter` получает войти в **консоль**.  Сообщения, отформатированные таким образом, являются предупреждениями.  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Консоль после выбора предупреждения журнала" lightbox="../media/console-log-warning.msft.png":::
       Консоль **после** выбора **предупреждения журнала**  
    :::image-end:::  
    
    > [!TIP]
    > Если вы хотите отобразить код, который вызвал определенный вход сообщения, выберите в скрипте \(например\) для просмотра кода, из-за чего сообщение было `log.js:12` отформатировано.  

1.  Выберите **значок Expand** \( ![ Expand ](../media/expand-icon.msft.png) \) перед `Abandon Hope All Ye Who Enter` .  В DevTools показан [след стека,][WikiStackTrace] ведущий к вызову.  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Трассировка стека" lightbox="../media/console-log-warning-expanded.msft.png":::
       Трассировка стека  
    :::image-end:::  
    
    Трассировка стека говорит, что выполняется функция с именем, которая, в свою очередь, `logWarning` выполняет функцию с именем `quoteDante` .  Другими словами, первый запрос находится в нижней части трассировки стека.  Вы можете войти следы стека в любое время при запуске `console.trace()` .  

1.  Выберите **ошибку журнала**.  В журнал попадает следующее сообщение об ошибке: `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Сообщение об ошибке" lightbox="../media/console-log-error.msft.png":::
       Сообщение об ошибке  
    :::image-end:::  
    
1.  Выберите **таблицу журнала**.  Таблица о известных артистах попадает в **консоль.**  
    
    > [!NOTE]
    > Столбец `birthday` заполняется только для одной строки.  Просмотрите код, чтобы определить, почему это так.
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Таблица в консоли" lightbox="../media/console-log-table.msft.png":::
       Таблица в **консоли**  
    :::image-end:::  
    
1.  Выберите **группу журнала**.  Имена 4 известных, борющихся с преступностью черепах группуются под `Adolescent Irradiated Espionage Tortoises` меткой.  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Группа сообщений в консоли" lightbox="../media/console-log-group.msft.png":::
       Группа сообщений в **консоли**  
    :::image-end:::  
    
1.  Выберите **настраиваемый журнал**.  Сообщение с красной границей и синим фоном попадает в консоль.  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Сообщение с настраиваемой формата в консоли" lightbox="../media/console-log-custom.msft.png":::
       Сообщение с настраиваемой формата в **консоли**  
    :::image-end:::  
    
Основная идея заключается в том, что при входе сообщений в консоль из JavaScript используется один из `console` методов.  Каждый метод форматов сообщений по-разному.  

Существует еще больше методов, чем было продемонстрировано в этом разделе.  В этом руководстве показано, как изучить остальные методы.  

## <a name="view-messages-logged-by-the-browser"></a>Просмотр сообщений, зарегистрированных в браузере  

Браузер также регистрит сообщения в консоли.  Обычно это происходит при проблеме со страницей.  

1.  Выберите **причина 404**.  Браузер регистрит код сетевой ошибки состояния HTTP, так как JavaScript страницы пытался получить файл, `404` который не существует.  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Ошибка 404 в консоли" lightbox="../media/console-cause-404.msft.png":::
       Ошибка `404` в **консоли**  
    :::image-end:::  
    
1.  Выбор **причины ошибки**.  Браузер регистрит необученный, так как JavaScript пытается обновить узел `TypeError` DOM, который не существует.  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError в консоли" lightbox="../media/console-cause-error.msft.png":::
       A `TypeError` в **консоли**  
    :::image-end:::  
    
1.  Выберите **выпадаемые** уровни журналов и включите параметр **Verbose,** если он отключен.  Дополнительные статьи о фильтрации в следующем разделе.  Это необходимо сделать, чтобы убедиться, что следующее сообщение, которое вы в журнале, будет видимым.  
    
    > [!NOTE]
    > Если отключена отключка уровней по умолчанию, может потребоваться закрыть боковую панель **консоли.**  Фильтр по источнику сообщений ниже, чтобы получить дополнительные сведения о **боковой** панели консоли.
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Включение уровня журнала Verbose" lightbox="../media/console-cause-error-log-levels.msft.png":::
       Включение уровня журнала Verbose  
    :::image-end:::  
    
1.  Выберите **причину нарушения**.  Страница на несколько секунд становится безответной, а затем браузер записывет сообщение `[Violation] 'click' handler took 3000ms` на консоль.  Точная продолжительность может отличаться.  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Нарушение в консоли" lightbox="../media/console-cause-violation.msft.png":::
       Нарушение в **консоли**  
    :::image-end:::  
    
## <a name="filter-messages"></a>Фильтрация сообщений  

На некоторых веб-сайтах вы просматриваете **консоль,** которая заполоняется сообщениями.  DevTools предоставляет множество различных способов фильтрации сообщений, не соответствующих поставленной задаче.  

### <a name="filter-by-log-level"></a>Фильтр по уровню журнала  

Каждому `console` методу назначен уровень серьезности: `Verbose` , , , или `Info` `Warning` `Error` .  Например, это сообщение уровня, в то время как это `console.log()` `Info` сообщение `console.error()` `Error` уровня.  

1.  Выберите **выпадаемые** уровни журналов и отключите **ошибки.**  Уровень отключен, когда рядом с ней больше нет контрольного знака.  Сообщения `Error` уровня исчезают.  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Отключение сообщений уровня ошибок в консоли" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       Отключение сообщений уровня ошибок в **консоли**  
    :::image-end:::  
    
1.  Снова выберите **выпадаемые** уровни журналов и повторно включить **ошибки.**  Снова `Error` появляются сообщения уровня.  

### <a name="filter-by-text"></a>Фильтр по тексту  

Если нужно просматривать только сообщения, включаю точные строки, введите эту строку в текстовое поле **Filter.**  

1.  `Dave`Введите **текстовое поле Filter.**  Все сообщения, которые не включают `Dave` строку, скрыты.  Вы также можете просмотреть `Adolescent Irradiated Espionage Tortoises` метку.  Это ошибка.  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Отфильтровать любое сообщение, не включаее Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       Фильтрация любых сообщений, не включа `Dave`  
    :::image-end:::  
    
1.  Удаление `Dave` из **текстового окна Filter.**  Все сообщения появляются снова.  

### <a name="filter-by-regular-expression"></a>Фильтр по регулярному выражению  

Если вы хотите показать все сообщения, которые включают шаблон текста, а не определенную строку, используйте [регулярное выражение][MDNRegularExpressions].  

1.  `/^[AH]/`Введите **текстовое поле Filter.**  Введите шаблон в [RegExr][|::ref1::|Main] для объяснения того, что он делает.  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Фильтрация любых сообщений, не совпадающих с шаблоном" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       Фильтрация любых сообщений, не совпадающих с шаблоном `/^[AH]/`  
    :::image-end:::  
    
1.  Удаление `/^[AH]/` из **текстового окна Filter.**  Все сообщения снова видны.  

### <a name="filter-by-message-source"></a>Фильтр по источнику сообщений  

Если вы хотите просматривать только сообщения, которые поступили из определенного URL-адреса, используйте **боковую панель**.  

1.  Выберите **боковую панель** консоли show \. ![ Показать боковую панель ](../media/show-console-sidebar-icon.msft.png) консоли \).  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Боковая панель" lightbox="../media/console-sidebar-all-messages.msft.png":::
       Боковая панель  
    :::image-end:::  
    
1.  Выберите **значок Expand** ![ \( Expand ](../media/expand-icon.msft.png) \) рядом с числом сообщений.  На следующем рисунке количество сообщений указывается как **13 сообщений.**  На **боковой панели** показан список URL-адресов, из-за чего сообщения были внесены в журнал.  Например, `log.js` вызвало 11 сообщений.  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Просмотр источника сообщений в боковой панели" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       Просмотр источника сообщений в боковой панели  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a>Фильтрация сообщений пользователей  

Ранее, при выборе **журнала Info**, скрипт с именем для входа сообщения в `console.log('Hello, Console!')` консоль.  Сообщения, в журнале из JavaScript, как это **называются сообщения пользователей**.  Напротив, при выборе **Cause 404**браузер регистрирует сообщение уровня, указывав, что запрашиваемого `Error` ресурса не обнаружено.  Такие сообщения считаются сообщениями **браузера.**  Используйте **боковую панель,** чтобы отфильтровать сообщения браузера и показывать только сообщения пользователей.  

1.  Выберите **9 сообщений пользователей**.  Сообщения браузера скрыты.  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Фильтрация сообщений браузера" lightbox="../media/console-sidebar-user-messages.msft.png":::
       Фильтрация сообщений браузера  
    :::image-end:::  
    
1.  Выберите **13 сообщений,** чтобы показать все сообщения снова.  

## <a name="use-the-console-alongside-any-other-tools"></a>Используйте консоль вместе с любыми другими средствами  

Если вы редактируете стили, но вам необходимо быстро проверить журнал консоли для чего-то, используйте ящик.  

1.  Выберите **средство Elements.**  
1.  Выберите `Escape` .  Откроется **консольный** инструмент **в ящике.**  Он содержит все функции панели Консоли, которые вы использовали во всем этом руководстве.  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Средство консоли в ящике" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         Средство **консоли** в **ящике**  
    :::image-end:::  
    
## <a name="see-also"></a>См. также  

*   Чтобы изучить дополнительные функции и процессы, связанные с интерфейсом **консоли,** перейдите на [консоль ссылку][DevToolsConsoleApi].  
*   Чтобы узнать больше обо всех методах, демонстрируемых в View `console` [messages logged from JavaScript,](#view-messages-logged-from-javascript) и ознакомьтесь с другими методами, не охваченными в этой статье, перейдите к ссылке `console` На [API консоли][DevToolsConsoleReference].  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочные | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md "Справочные | Документы Майкрософт"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Начало работы с ведением журнала сообщений | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Регулярные выражения | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Трассировка стека — Википедия"  
> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/log) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
