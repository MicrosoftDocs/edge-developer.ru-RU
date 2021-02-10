---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска и устранения ошибок JavaScript.
title: Начало отладки JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325952"
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
# Начало отладки JavaScript в Microsoft Edge DevTools  

В этой статье рассказывается о базовом рабочий процессе для отладки любых проблем JavaScript в DevTools.  

## Шаг 1. Воспроизведение ошибки  

Поиск ряда действий, которые постоянно воспроизводят ошибку, всегда является первым этапом отладки.  

1.  Choose **Open Demo**.  Удерживайте `Control` \(Windows, Linux\) или \(macOS\) и откройте демонстрацию на `Command` новой вкладке браузера.  
    
    [Открытая демонстрация][OpenDebugJSDemo]  
    
1.  Введите `5` в **текстовое поле "Номер 1".**  
1.  Введите `1` в **текстовое поле "Номер 2".**  
1.  Choose **Add Number 1 and Number 2**.  Метка под кнопкой " `5 + 1 = 51` .  Результат должен быть `6` .  Затем исправьте ошибку добавления, которая является ошибкой.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 приводит к 51, но должно быть 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` результаты, `51` но должны быть `6`  
    :::image-end:::  
    
## Шаг 2. Знакомство с пользовательским интерфейсом панели источников  

DevTools предоставляет множество различных средств для различных задач.  К различным задачам относятся изменение CSS, профилирование производительности загрузки страницы и отслеживание сетевых запросов.  Панель **источников** — это место отлаки JavaScript.  

1.  Откройте DevTools, нажав `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).  Этот ярлык открывает панель **консоли.**  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Панель консоли" lightbox="../media/javascript-console-empty.msft.png":::
       **Консольный** инструмент  
    :::image-end:::  
    
1.  Выберите средство **"Источники".**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Панель источников" lightbox="../media/javascript-sources-sections.msft.png":::
       Панель **источников**  
    :::image-end:::  
    
Пользовательский **интерфейс** панели источников имеет три части.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="3 части пользовательского интерфейса панели источников" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   3 части пользовательского интерфейса **панели** источников  
:::image-end:::  

1.  The **File Navigator** pane \(Section 1 in the previous figure\).  Здесь перечислены все файлы, запрашиваемые веб-страницей.  
1.  The **Code Editor** pane \(Section 2 in the previous figure\).  После выбора файла в **области** навигатора файлов здесь отображается его содержимое.  
1.  The **JavaScript Debugging** pane \(Section 3 in the previous figure\).  Различные средства проверки JavaScript для веб-страницы.  Если окно DevTools широкое, эта области отображается справа от области **редактора** кода.  
    
## Шаг 3. Приостановка кода с помощью точки останова  

Распространенным методом отладки этого типа проблемы является вставка нескольких заявлений в код, а затем проверка значений при `console.log()` запуске сценария.  Например:  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

Этот метод может получить задание, но точки `console.log()` **останова** получают его быстрее.  Точка останова позволяет приостановить код в середине времени и проверить все значения в этот момент времени.  Точки останова имеют несколько преимуществ перед `console.log()` методом:  

*   При этом необходимо вручную открыть исходный код, найти соответствующий код, вставить инструкции, а затем обновить веб-страницу, чтобы отобразить сообщения в `console.log()` `console.log()` консоли. ****  С помощью точек останова можно приостановить соответствующий код, даже не зная, как он структурирован.  
*   В своих утверждениях необходимо явно указать каждое значение, `console.log()` которое требуется проверить.  С помощью точек останова DevTools отображает значения всех переменных на данный момент времени.  Иногда переменные, влияющие на код, скрыты и скрыты.  
    
Вкратце, точки останова могут помочь быстрее находить и исправлять ошибки, чем `console.log()` метод.  

Если вернуться назад и подумать о том, как работает приложение, вы можете сделать обоснованные предположения, что неправильная сумма \( \) вычисляется в прослушивателье событий, связанном с кнопкой "Добавить `5 + 1 = 51` `click` номер 1" и **"Номер 2".**  Таким образом, возможно, вы захотите приостановить код во время, когда `click` выполняется прослушиватель.  **Точки останова прослушиватель** событий делают именно это:  

1.  В области **отладки JavaScript** выберите точки останова прослушиватель событий, **чтобы** развернуть раздел.  DevTools открывает список расширяемых категорий событий, таких как анимация **и** **буфер обмена.**  
1.  Рядом с **категорией событий "Мышь"** выберите **"Развернуть".** ![ Значок ][ImageExpandIcon] "Развернуть" \).  DevTools открывает список событий мыши, таких как нажатие **мыши** **и мышью.**  Каждое событие имеет рядом с собой контрольный ящик.  
1.  Рядом с кнопкой мыши нажмите **этот кнопку.**  Теперь DevTools настроен на автоматическое приостановка при запуске `click` прослушиватель событий.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Рядом с кнопкой мыши нажмите кнопку с кнопкой мыши" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Рядом с кнопкой мыши нажмите кнопку с **кнопкой мыши**  
    :::image-end:::  
    
1.  Снова в демонстрации выберите **"Добавить номер 1" и "Номер 2".**  DevTools приостанавлиет демонстрацию и выделяет строку кода на панели **источников.**  DevTools должен приостановиться на строке 16 в `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Если вы приостанавливлиируете другую строку кода, нажмите кнопку **Resume Script Execution** \( Resume Script Execution \) до тех пор, пока не приостановим правильную ![ ][ImageResumeIcon] строку.  
    
    > [!NOTE]
    > Если вы приостановлены на другой строке, у вас есть расширение браузера, которое регистрирует прослушиватель событий на каждой веб-странице, `click` которую вы посещаете.  Вы были приостановлены в `click` прослушивателье расширения.  Если вы используете режим InPrivate для просмотра в закрытом **режиме,** который отключает все расширения, вы можете видеть, что вы каждый раз приостанавливаете нужную строку кода.  

<!--todo: add inprivate section when available -->  

**Точки останова прослушиватель** событий — это лишь один из многих типов точек останова, доступных в DevTools.  Запомните все типы, чтобы помочь вам отлачивать различные сценарии как можно быстрее.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## Шаг 4. Пошаговая пошаговая по  

Одна из распространенных причин ошибок — запуск скрипта в неправильном порядке.  Пошаговая поша  Вы проходите по одной строке за раз, чтобы точно понять, где именно работает ваш код, в другом порядке, чем вы ожидаете.  Попробуйте его сейчас:  

1.  Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).  DevTools выполняет следующий код, не вступая в него.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools пропускает несколько строк кода.  Это происходит потому, что оценивается как false, поэтому блок кода для этого заявления `inputsAreEmpty()` `if` не будет работать.  
    
1.  On the Sources panel of DevTools, choose **Step into next function call** \( Step into next function call \) to step through the **runtime** ![ of the ][ImageIntoIcon] `updateLabel()` function, one line at a time.  
    
Пошаговая проверка по одной строке — это основная идея пошагового кода.  Если вы посмотрите на код в, вы увидите, что ошибка, вероятно, находится `get-started.js` где-то в `updateLabel()` функции.  Вместо того чтобы перешаговое использование каждой строки кода, вы можете использовать другой тип точки останова, чтобы приостановить код ближе к возможному расположению ошибки.  

## Шаг 5. Настройка точки останова кода  

Точки останова кода — это наиболее распространенный тип точки останова.  Когда вы получаете определенную строку кода, который нужно приостановить, используйте точку останова кода.  

1.  Посмотрите на последнюю строку кода `updateLabel()` в:  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  Слева номер этой строки кода отображается как **34**.  Выберите **строку 34**.  DevTools помещает красный значок слева от **34**.  Красный значок указывает, что в этой строке находится точка останова кода.  DevTools всегда приостанавливается перед запуском этой строки кода.  
1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  Сценарий продолжает работать, пока не достигнет строки 33.  В строках 31, 32 и 33 DevTools печатает значения справа от двоеточия в `addend1` `addend2` каждой `sum` строке.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools приостанавливов в точке останова кода в строке 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools приостанавливов в точке останова кода в строке 34  
    :::image-end:::  
    
## Шаг 6. Проверка значений переменных  

Значения `addend1` ,, `addend2` и выглядят `sum` подозрительными.  Значения завернуты в кавычках.  Кавычка означает, что значение является строкой, которая является хорошей догмой, чтобы объяснить причину ошибки.  Соберем дополнительные сведения о ситуации.  DevTools предоставляет множество средств для проверки значений переменных.  

### Метод 1. Область области  

Если приостановить строку кода, **** область области отображает локальные и глобальные переменные, которые определены в настоящее время, а также значение каждой переменной.  Кроме того, отображаются переменные закрытия, если применимо.  Дважды щелкните переменное значение, чтобы изменить его.  Если не приостановить строку кода, область области **будет** пустой.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Область **области**  
:::image-end:::  

### Метод 2. Просмотр выражений  

В **области контрольных выражений** можно отслеживать значения переменных с течением времени.  Как следует из названия, **watch Expressions** не ограничиваются переменными.  Вы можете сохранить любое допустимые выражения JavaScript в watch **Expression.**  Попробуйте его сейчас.  

1.  Выберите в **области** "Часы".  
1.  Choose **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).  
1.  Введите `typeof sum`.  
1.  Выберите `Enter` .  Показывает DevTools `typeof sum: "string"` .  Значение справа от двоеточия является результатом выражения watch.  
    
> [!NOTE]
> В области **"Watch Expression"** (Выражение в нижнем правом) на следующем рисунке отображается выражение "Watch". `typeof sum`  Если окно DevTools имеет **** большой размер, то над точкими останова прослушиватель событий находится справа над этой области. ****  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="The Watch Expression pane" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   The **Watch Expression** pane  
:::image-end:::  

Как есть `sum` подозрение, он оценивается как строка, когда она должна быть числом.  Теперь вы подтверждаете, что причиной ошибки является тип значения.  

### Метод 3: консоль  

Консоль **позволяет** просматривать сообщения, и вы также можете использовать ее для оценки произвольных `console.log()` заявлений JavaScript.  Для отладки можно использовать **** консоль для проверки возможных исправлений ошибок.  Попробуйте его сейчас.  

1.  Если **консольный** ящик закрыт, `Escape` выберите, чтобы открыть его.  В **нижней** панели окна DevTools откроется консольный ящик.  
1.  В консоли **введите** `parseInt(addend1) + parseInt(addend2)` .  The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.  
1.  Выберите `Enter` .  DevTools оценивает заявление и печатает, что является результатом, который вы `6` ожидаете, что демонстрация будет производить.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Консольный ящик после оценки parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       **Консольный** ящик после оценки `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## Шаг 7. Применение исправления  

Если вы нашли исправление ошибки, попробуйте исправить ошибку, отредактировать код и повторно перезахлить демонстрацию.  Вы можете изменить код JavaScript непосредственно в пользовательском интерфейсе DevTools и применить исправление.  Попробуйте его сейчас.  

1.  Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).  
1.  В **редакторе кода**замените строку 32 `var sum = addend1 + addend2` , на `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\) для сохранения изменения.  
1.  Choose **Deactivate breakpoints** \( ![ Deactivate breakpoints ][ImageDeactivateIcon] \).  Он изменяется синим цветом, чтобы указать, что параметр активен.  Хотя **точки останова** отключены, DevTools игнорирует все задаваемые точки останова.  
1.  Попробуйте демонстрацию с разными значениями.  Демонстрация вычисляется правильно.  
    
> [!CAUTION]
> Этот рабочий процесс применяет исправление только к коду, который работает в браузере.  Он не исправит код для всех пользователей, посетив вашу веб-страницу.  Для этого необходимо исправить код, который находится на серверах.  

## Дальнейшие действия  

Поздравляем!  Теперь вы знаете, как сделать все возможное для Microsoft Edge DevTools при отладке JavaScript.  Инструменты и методы, которые вы узнали в этой статье, могут сэкономить много времени.  

В этой статье вы знаете только два способа установить точки останова.  DevTools предлагает множество других способов, включая следующие параметры.  

*   Условные точки останова, которые запускаются только при условии, которое вы предоставляете, является истинным.  
*   Точки останова для перехваченных или неподтверченных исключений.  
*   Точки останова XHR, которые запускаются, когда запрашиваемого URL-адреса соответствует подстроки, которые вы предоставляете.  
    
Для получения дополнительных сведений о том, когда и как использовать каждый тип, перейдите к приостановки [кода с точками останова.][DevtoolsJavscriptBreakpoints]  

Пара элементов управления пошаговым кодом не объясняется в этой статье.  Для получения дополнительных сведений перейдите [к пошаговой строке кода.][DevtoolsJavascriptReferenceStepThroughCode]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с точками останова в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Пошаговое пошаговое название кода: справочные данные по отладки JavaScript | Документы Майкрософт"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Открытие демонстрационных | Временный сбой"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
