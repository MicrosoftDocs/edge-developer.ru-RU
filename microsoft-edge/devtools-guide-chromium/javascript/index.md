---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска и исправления ошибок JavaScript.
title: Начало работы с отладки JavaScript в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398443"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a>Начало работы с отладки JavaScript в Microsoft Edge DevTools  

В этой статье рассказывается об основных процессах отладки любых проблем JavaScript в DevTools.  

## <a name="step-1-reproduce-the-bug"></a>Шаг 1. Воспроизведение ошибки  

Поиск ряда действий, которые последовательно воспроизводят ошибку, всегда является первым шагом к отладки.  

1.  Выберите **Open Demo**.  Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и откройте демонстрацию на новой вкладке браузера.  
    
    [Open Demo][OpenDebugJSDemo]  
    
1.  `5`Введите **текстовое поле Номер 1.**  
1.  `1`Введите **текстовое поле Номер 2.**  
1.  Выберите **Добавить номер 1 и Номер 2.**  Метка ниже кнопки говорит `5 + 1 = 51` .  Результат должен быть `6` .  Затем исправьте ошибку добавления, которая является ошибкой.  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 результат в 51, но должен быть 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` результаты, `51` но должны быть `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a>Шаг 2. Знакомство с пользовательским интерфейсом инструмента Sources  

DevTools предоставляет множество различных инструментов для различных задач.  Различные задачи включают изменение CSS, профилирование производительности загрузки страниц и запросы на мониторинг сети.  Средство **Sources** — это место, где отламываю JavaScript.  

1.  Чтобы открыть **консольный** инструмент в DevTools, выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Средство Консоли" lightbox="../media/javascript-console-empty.msft.png":::
       Средство **Консоли**  
    :::image-end:::  
    
1.  Выберите средство **Sources.**  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Средство Источники" lightbox="../media/javascript-sources-sections.msft.png":::
       Средство **Источники**  
    :::image-end:::  
    
Пользовательский **интерфейс** средства Sources имеет три части.  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="3 части пользовательского интерфейса инструмента Sources" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   3 части пользовательского **интерфейса инструмента Sources**  
:::image-end:::  

1.  Панель **навигатора** файлов \(Раздел 1 на предыдущем рисунке\).  Каждый файл, который запрашивает веб-страницу, указан здесь.  
1.  Панель **редактора** кода \(Раздел 2 на предыдущем рисунке\).  После выбора файла в области **Навигатора** файлов содержимое этого файла отображается здесь.  
1.  Панель **отладки JavaScript** \(Раздел 3 на предыдущем рисунке\).  Различные средства для проверки JavaScript для веб-страницы.  Если окно DevTools широкое, эта области отображается справа от области **редактора** кода.  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a>Шаг 3. Приостановка кода с помощью точки разрыва  

Распространенный метод отладки этого типа проблемы — вставить несколько заявлений в код, а затем проверить значения по мере `console.log()` работы сценария.  Например:  

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

Метод `console.log()` может получить работу, но **breakpoints** получить его быстрее.  Точка разрыва позволяет приостановить работу кода в середине времени работы и вовремя изучить все значения.  Точки breakpoints имеют следующие преимущества по сравнению с `console.log()` методом.  

*   Для этого необходимо вручную открыть исходный код, найти соответствующий код, вставить инструкции и обновить веб-страницу для отображения сообщений в `console.log()` `console.log()` консоли. ****  При разрывных точках можно остановиться на соответствующем коде, даже не зная, как он структурирован.  
*   В своих заявлениях необходимо четко указать каждое `console.log()` значение, которое необходимо проверить.  С помощью точек breakpoints DevTools показывает значения всех переменных в данный момент времени.  Иногда переменные, влияющие на код, скрыты и запутываются.  
    
Короче говоря, breakpoints может помочь вам найти и устранить ошибки быстрее, чем `console.log()` метод.  

Если вы отойти назад и подумать о том, как работает приложение, вы можете сделать образованное предположение, что неправильная сумма \( \) вычисляется в прослушиватель событий, связанный с кнопкой Добавить номер 1 и Номер `5 + 1 = 51` `click` **2.**  Таким образом, вероятно, необходимо приостановить код во время `click` прослушивания.  **Breakpoints listener event** let you do exactly that:  

1.  В области **отладки JavaScript** выберите точки **breakpoints для** прослушивания событий, чтобы расширить раздел.  DevTools открывает список расширяемых категорий событий, таких как **Animation** и **Clipboard.**  
1.  Рядом с **категорией событий Мыши** выберите **Расширение** \( ![ Расширение ][ImageExpandIcon] значка \).  DevTools показывает список событий мыши, таких как **щелчки** мыши и **мыши.**  Рядом с каждым событием имеется почтовый ящик.  
1.  Выберите почтовый ящик рядом, чтобы **щелкнуть**.  DevTools теперь настроен на автоматическое приостановление при запуске любого `click` прослушиватель события.  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Выберите контрольный ящик рядом с кнопкой мыши" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       Выберите контрольный ящик рядом с **кнопкой мыши**  
    :::image-end:::  
    
1.  Возвращаясь к демонстрации, **выберите добавить номер 1 и номер 2** снова.  DevTools останавливает демонстрацию и выделяет строку кода в **средстве Sources.**  DevTools следует приостановить на строке 16 в `get-started.js` .  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    Если вы приостанавливлить другую строку кода, выберите **выполнение** сценариев возобновления \. Возобновление выполнения скрипта \) до остановки ![ на ][ImageResumeIcon] правильной строке.  
    
    > [!NOTE]
    > Если вы остановились на другой строке, у вас есть расширение браузера, которое регистрирует слушателя событий на каждой `click` веб-странице, которую вы посещаете.  Вы приостанавливована `click` в прослушиватель расширения.  Если вы используете режим InPrivate для просмотра в закрытом **режиме,** который отключает все расширения, вы можете каждый раз приостанавлить нужную строку кода.  

<!--todo: add inprivate section when available -->  

**Breakpoints слушателя событий** — это только один из многих типов точек разрыва, доступных в DevTools.  Запомните все различные типы, чтобы помочь вам отлачивать различные сценарии как можно быстрее.  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a>Шаг 4. Прошаговка кода  

Одной из распространенных причин ошибок является то, что сценарий выполняется в неправильном порядке.  Пройдя через код, вы сможете выполнить время работы кода.  Вы проходите по одной строке, чтобы выяснить, где именно работает код в другом порядке, чем вы ожидаете.  Попробуйте его сейчас:  

1.  Выберите **шаг по следующему вызову** функции \. Шаг за следующий вызов ![ ][ImageOverIcon] функции \).  DevTools запускает следующий код, не вступая в него.  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > DevTools пропускает несколько строк кода.  Это потому, что оценивается как ложное, поэтому блок кода для заявления `inputsAreEmpty()` `if` не работает.  
    
1.  В **средстве Источники** DevTools **** выберите Шаг в следующий вызов функции \( Шаг в следующий вызов функции \) для того, чтобы выполнить время работы функции по одной ![ ][ImageIntoIcon] `updateLabel()` строке за один раз.  
    
Просмотр одной строки за один раз — это основная идея пошаговая проверка кода.  Если просмотреть `get-started.js` код, ошибка, вероятно, находится где-то в `updateLabel()` функции.  Вместо того, чтобы перешагировать каждую строку кода, вы можете использовать другой тип точки разрыва, чтобы приостановить код ближе к вероятному расположению ошибки.  

## <a name="step-5-set-a-line-of-code-breakpoint"></a>Шаг 5. Установите точку разрыва кода  

Разрывные точки line-of-code являются наиболее распространенным типом точки разрыва.  При подъехав к определенной строке кода, необходимо приостановить, используйте точку разрыва кода.  

1.  Посмотрите на последнюю строку кода в `updateLabel()` :  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  Слева отображается число этой определенной строки кода в **качестве 34**.  Выберите **строку 34**.  DevTools отображает красный значок слева от **34**.  Красный значок указывает, что в этой строке находится точка разрыва строки кода.  DevTools всегда останавливается перед запуском этой строки кода.  
1.  Выберите **выполнение скрипта** Resume \. ![ Возобновление выполнения ][ImageResumeIcon] скрипта \).  Сценарий продолжает работать, пока не достигнет строки 33.  На строках 31, 32 и 33 DevTools печатает значения , и справа от полу-двоеточия на `addend1` `addend2` каждой `sum` строке.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools приостанавливовка на точке разрыва кода на строке 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       DevTools приостанавливовка на точке разрыва кода на строке 34  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a>Шаг 6. Проверка переменных значений  

Значения , `addend1` и `addend2` выглядеть `sum` подозрительно.  Значения завернуты в кавычках.  Эти цитаты означают, что это значение — строка, которая является хорошей гипотезой для объяснения причины ошибки.  Дополнительные сведения о ситуации.  DevTools предоставляет множество инструментов для изучения переменных значений.  

### <a name="method-1-the-scope-panel"></a>Метод 1. Панель Область  

При паузе на строке кода панель **Scope** отображает локальные и глобальные переменные, которые в настоящее время определены, а также значение каждой переменной.  В нем также отображаются переменные закрытия, как это применимо.  Дважды щелкните переменное значение, чтобы изменить его.  Если не приостанавливать строку кода, панель **Scope** пуста.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   Область **области**  
:::image-end:::  

### <a name="method-2-watch-expressions"></a>Метод 2. Просмотр выражений  

Панель **"Выражения часов"** позволяет отслеживать значения переменных со временем.  Как следует из названия, **выражения watch не** ограничиваются переменными.  Вы можете хранить любое допустимые выражения JavaScript в **watch Expression.**  Попробуйте.  

1.  Выберите панель **Watch.**  
1.  Выберите **Add Expression** \( Add Expression ![ ][ImageAddIcon] \).  
1.  Введите `typeof sum`.  
1.  Выберите `Enter` .  DevTools показывает `typeof sum: "string"` .  Значение справа от толстой кишки является результатом выражения часов.  
    
> [!NOTE]
> В области **Выражение вахты** \(внизу справа\) на следующем рисунке отображается выражение `typeof sum` watch.  Если окно DevTools большое, **** то справа над точкой точки **breakpoints** слушателя событий находится области Выражение часов.  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Панель "Выражение часов"" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   Панель **"Выражение часов"**  
:::image-end:::  

Как подозревается, оценивается как `sum` строка, когда она должна быть номером.  Теперь подтвержден тип значения является причиной ошибки.  

### <a name="method-3-the-console"></a>Метод 3. Консоль  

Консоль **позволяет** просматривать сообщения, а также использовать ее для оценки произвольных `console.log()` заявлений JavaScript.  Для отладки можно использовать **** консоль для тестирования возможных исправлений ошибок.  Попробуйте.  

1.  Если средство **консоли** закрыто, выберите `Escape` его открытие.  **Консольный** инструмент открывается в нижней панели окна DevTools.  
1.  В консоли **введите** `parseInt(addend1) + parseInt(addend2)` .  Заявление, в котором инструмент приостанавлитована, находится на строке кода, где `addend1` `addend2` и находятся в области.  
1.  Выберите `Enter` .  DevTools оценивает заявление и отпечатки, что является результатом, который вы `6` ожидаете, что демо-версия будет производиться.  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="Средство Консоли после оценки parseInt (addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       Средство **Консоли** после оценки `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a>Шаг 7. Применение исправления  

Если вы нашли исправление ошибки, попробуйте исправить его, отредактив код и повторив демонстрацию.  Вы можете изменить код JavaScript непосредственно в пользовательском интерфейсе DevTools и применить исправление.  Попробуйте.  

1.  Выберите **выполнение скрипта** Resume \. ![ Возобновление выполнения ][ImageResumeIcon] скрипта \).  
1.  В **редакторе кода**замените строку 32, `var sum = addend1 + addend2` с `var sum = parseInt(addend1) + parseInt(addend2)` .  
1.  Чтобы `Control` + `S` сохранить изменения, выберите \(Windows, Linux\) `Command` + `S` или \(macOS\).  
1.  Выберите **деактивационные точки** разрывов \. ![ Деактивировать точки ][ImageDeactivateIcon] перерывов \).  Он изменяется синим цветом, чтобы указать, что параметр активен.  В **то время как задаваются** точки деактивации, DevTools игнорирует все задаваемые точки.  
1.  Попробуйте демонстрацию с разными значениями.  Демо теперь вычисляется правильно.  
    
> [!CAUTION]
> Этот рабочий процесс применяет исправление только к коду, который запущен в браузере.  Он не исправит код для всех пользователей, которые посещают веб-страницу.  Для этого необходимо исправить код, который находится на серверах.  

## <a name="next-steps"></a>Дальнейшие действия  

Поздравляем!  Теперь вы знаете, как сделать большую часть Microsoft Edge DevTools при отладке JavaScript.  Инструменты и методы, которые вы узнали в этой статье, могут сэкономить бесчисленные часы.  

В этой статье вы можете найти только два способа установить точки разрыва.  DevTools предлагает множество других способов, включая следующие параметры.  

*   Условные точки разрыва, которые срабатывает только при условии, которое вы предоставляете, является верным.  
*   Breakpoints on caught or uncaught exceptions.  
*   Точки взлома XHR, срабатывающие при совпадении запрашиваемого URL-адреса с подразрядом, который вы предоставляете.  
    
Дополнительные сведения о том, когда и как использовать каждый тип, перейдите к паузе кода [с точками breakpoints.][DevtoolsJavscriptBreakpoints]  

Несколько элементов управления шагами кода не объясняются в этой статье.  Дополнительные сведения, перейдите [на шаг за строку кода][DevtoolsJavascriptReferenceStepThroughCode].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Приостановка кода с помощью точек остановок в Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Шаг через код — отладка ссылок javaScript | Документы Майкрософт"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Open Demo | Glitch"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
