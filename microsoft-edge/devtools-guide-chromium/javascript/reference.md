---
description: Откройте для себя новые процессы отладки в этой всеобъемлющей ссылке на функции отладки Microsoft Edge DevTools.
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398478"
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

# <a name="javascript-debugging-reference"></a>Справочник по отладке JavaScript  

Откройте для себя новые процессы отладки со следующей всеобъемлющей ссылкой на функции отладки Microsoft Edge DevTools.  

Чтобы узнать основы отладки, перейдите по ссылке Начало работы с отладки [JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted].  

## <a name="pause-code-with-breakpoints"></a>Приостановка кода с точками остановок  

Установите точку разрыва, чтобы вы могли приостановить работу кода в середине времени работы.  

Чтобы узнать, как установить точки остановок, перейдите к приостановки [кода с точками breakpoints.][DevToolsJavascriptBreakpoints]  

## <a name="step-through-code"></a>Шаг через код  

После приостановки кода перешадите его по одной строке, исследуя поток управления и значения свойств по пути.  

### <a name="step-over-line-of-code"></a>Шаг за строку кода  

При остановке на строке кода, содержащей функцию, которая не относится к проблеме отладки, выберите кнопку **Step over** \( Step over \) для запуска функции, не вступая в нее. ![ ][ImageStepOverIcon]  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Выберите шаг более" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   Выберите **шаг более**  
:::image-end:::  

Например, предположим, что вы отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Вы приостановили. `A`  После выбора **Step over,** DevTools выполняет весь код в функции, которую вы переступили, которая `B` является и `C` .  Затем DevTools приостанавливается. `D`  

### <a name="step-into-line-of-code"></a>Шаг в строку кода  

При остановке на строке кода, содержащей вызов функции, связанный с проблемой отладки, выберите кнопку **Шаг** в \( Шаг в \) для дальнейшего изучения этой ![ ][ImageStepIntoIcon] функции.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Выберите шаг в" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   Выберите **шаг в**  
:::image-end:::  

Например, предположим, что вы отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Вы приостановили. `A`  После выбора **Шаг в,** DevTools запускает эту строку кода, а затем останавливается `B` на .  

### <a name="step-out-of-line-of-code"></a>Выход из строки кода  

При остановке внутри функции, не связанной с проблемой отладки, выберите кнопку **Step out** \( Step out \) для запуска остальной части кода ![ ][ImageStepOutIcon] функции.  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Выберите шаг" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   Выберите **шаг**  
:::image-end:::  

Например, предположим, что вы отладка следующего фрагмента кода.  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Вы приостановили. `A`  После выбора **Шаг,** DevTools запускает остальную часть кода в , который находится только в этом примере, а `getName()` затем останавливается на `B` `C` .  

### <a name="run-all-code-up-to-a-specific-line"></a>Запустите весь код до определенной строки  

При отладки длинной функции может быть много кода, не связанного с проблемой отладки.  

Вы можете выбрать шаг через все строки, но это утомительно.  Вы можете установить точку разлома строки кода на интересуемой строке, а затем выбрать кнопку **Выполнение** скриптов резюме \. Выполнение скриптов возобновления \) но существует более быстрый ![ ][ImageResumeScriptExecutionIcon] способ.  

Наведите курсор на строку кода, в которой вас интересует, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Продолжить здесь**.  DevTools выполняет весь код до этой точки, а затем останавливается на этой строке.  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Выберите Продолжить здесь" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   Выберите **Продолжить здесь**  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a>Перезапуск верхней функции стека вызовов  

Чтобы остановиться на первой строке верхней функции в стеке вызовов, **** приостановив работу на строке кода, наведите курсор в любом месте области стек вызовов, откройте контекстное меню \(правой кнопкой мыши\) и выберите перезапуск кадров **.**  Верхней функцией является последняя функция, которая была запустить.  

Следующий фрагмент кода является примером для пошаговое решение.  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Вы приостановили. `A`  После выбора **перезапуска кадра,** вы должны быть приостановлены, никогда не задав точку разлома или `B` выбрав выполнение **скрипта Резюме**.  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Выбор кадра перезагрузки" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   Выбор **кадра перезагрузки**  
:::image-end:::  

### <a name="resume-script-runtime"></a>Время возобновления запуска сценария  

Чтобы продолжить время выполнения после паузы скрипта, выберите кнопку **"Выполнение** скрипта ![ резюме"\. ][ImageResumeScriptExecutionIcon]  DevTools запускает сценарий до следующей точки перерыва, если таковые есть.  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Выбор выполнения скрипта Resume" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   Выбор **выполнения скрипта Resume**  
:::image-end:::  

#### <a name="force-script-runtime"></a>Время запуска сценария force  

Чтобы игнорировать все точки разлома и заставить скрипт возобновить работу, выберите и удерживайте кнопку Выполнение скрипта резюме **\(** Выполнение скрипта резюме \) и выберите кнопку Выполнение сценария Force \( Принудительное выполнение скрипта ![ ][ImageResumeScriptExecutionIcon] **** ![ ][ImageForceScriptExecutionIcon] \) .  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Выбор выполнения сценария Force" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   Выбор **выполнения сценария Force**  
:::image-end:::  

### <a name="change-thread-context"></a>Изменение контекста потока  

При работе с веб-работниками или сотрудниками служб выберите контекст, указанный в области **Threads,** чтобы перейти к этому контексту.  Значок синей стрелки представляет, какой контекст выбран в данный момент.  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Области threads" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   Области **threads**  
:::image-end:::  

Например, предположим, что в основном скрипте и скрипте сотрудника службы вы приостановили паузу на точке разрыва.  Необходимо просмотреть локальные и глобальные свойства для контекста сотрудника службы, но панель **Источников** показывает основной контекст сценария.  Выбрав в записи сотрудника службы в области **Threads,** вы сможете перейти на этот контекст.  

## <a name="view-and-edit-local-closure-and-global-properties"></a>Просмотр и редактирование локальных, закрытий и глобальных свойств  

Останавливаясь на строке кода, используйте область **Область** для просмотра и редактирования значений свойств и переменных в локальных, закрытии и глобальных сферах.  

*   Дважды щелкните значение свойства, чтобы изменить его.  
*   Свойства, которые не могут быть засеяны, серые.  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Область области" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   Область **области**  
:::image-end:::  

## <a name="view-the-current-call-stack"></a>Просмотр текущего стека вызовов  

Остановив на строке кода, используйте области **стек** вызовов, чтобы просмотреть стек вызовов, который получил вас к этой точке.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Выберите запись, чтобы перейти к строке кода, в которой была вызвана эта функция.  Значок синей стрелки представляет функцию, которую в настоящее время выделяет DevTools.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Области стек вызовов" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   Области **стек** вызовов  
:::image-end:::  

> [!NOTE]
> Если на строке кода не приостанавливали паузу, области **стек** вызовов пусты.  

### <a name="copy-stack-trace"></a>Трассировка копирования стека  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

чтобы скопировать текущий стек вызовов в **** буфер обмена, наведите курсор в любом месте области Стек вызовов, откройте контекстное меню \(правой кнопкой мыши\) и выберите трассировку **стека скопировки**.  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Выбор трассировки стека копирования" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   Выбор **трассировки стека копирования**  
:::image-end:::  

В качестве примера вывода приводится следующий фрагмент кода.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a>Игнорировать сценарий или шаблон сценариев  

Пометить сценарий как код библиотеки, если вы хотите игнорировать этот сценарий при отладки.  При обозначении кода Библиотеки сценарий заслоняется в области **стеков** вызовов, и вы никогда не вступите в функции скрипта при проступке кода.  

Следующий фрагмент кода является примером для пошаговое решение.  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` — это сторонная библиотека, которую вы доверяете.  Если вы уверены, что проблема отладки не связана с сторонней библиотекой, имеет смысл пометить сценарий как код **библиотеки.**  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a>Пометить сценарий как код библиотеки из области редактора  

Выполните следующие действия, чтобы пометить сценарий **как код библиотеки** из области **редактора.**  

1.  Откройте файл.  
1.  Наведите курсор в любом месте и откройте контекстное меню \(правой кнопкой мыши\).  
1.  Выберите **Mark в качестве кода библиотеки.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из области редактора" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       Пометить сценарий **как код библиотеки** из области **редактора**  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a>Пометить сценарий как код библиотеки из области стек вызовов  

Выполните следующие действия, чтобы пометить сценарий как **код библиотеки** из области **стек** вызовов.  

1.  Наведите курсор на функцию из скрипта и откройте контекстное меню \(правой кнопкой мыши\).  
1.  Выберите **Mark в качестве кода библиотеки.**  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из области стек вызовов" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       Пометить сценарий **как код библиотеки** из области **стек** вызовов  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a>Пометить сценарий как код библиотеки из параметров  

Выполните следующие действия, чтобы отметить один сценарий или шаблон сценариев из **параметров.**  

1.  Open [Settings][DevToolsCustomize].  
1.  Перейдите к **параметру кода Библиотеки.**  
1.  Выберите **шаблон Добавить**.  
1.  Введите имя сценария или шаблон regex имен скриптов, чтобы пометить код **библиотеки.**  
1.  Выберите **Добавить**.  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Пометить сценарий как код библиотеки из параметров" lightbox="../media/javascript-framework-library-code.msft.png":::
       Пометить сценарий **как код библиотеки** из **параметров**  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a>Запуск фрагментов кода отлаговки с любой страницы  

Если вы снова и снова работает один и тот же код отлаговки в консоли, рассмотрите фрагменты.  Фрагменты — это сценарии времени запуска, которые вы пишете, сохраняете и запускаете в DevTools.  

Чтобы узнать больше, перейдите к [запуску фрагментов кода с любой страницы][DevToolsJavascriptSnippets].  

## <a name="watch-the-values-of-custom-javascript-expressions"></a>Просмотр значений пользовательских выражений JavaScript  

Используйте области **Watch** для просмотра значений пользовательских выражений.  Вы можете просмотреть любое допустимые выражения JavaScript.  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Области Часы" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   Области **Часы**  
:::image-end:::  

*   Выберите **кнопку Add Expression** \( ![ Add Expression ][ImageAddExpressionIcon] \) для создания нового выражения часов.  
*   Выберите **кнопку Обновление** ![ \( Обновление \) для обновления ][ImageRefreshIcon] значений всех существующих выражений.  Значения автоматически обновляются при прошагове кода.  
*   Наведите курсор на выражение и выберите кнопку **Delete Expression** ![ \( Delete Expression ][ImageDeleteExpressionIcon] \) для ее удаления.  

## <a name="make-a-minified-file-readable"></a>Сделать минированную папку читаемой  

Выберите **кнопку Format** \( Format \) для того, чтобы сделать этот файл ![ ][ImageFormatIcon] понятным для человека.  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="Кнопка "Формат"" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   Кнопка **"Формат"**  
:::image-end:::  

## <a name="edit-a-script"></a>Изменение сценария  

При исправлении ошибки часто необходимо проверить некоторые изменения в коде JavaScript.  Вам не нужно вносить изменения во внешнем редакторе или IDE, а затем обновлять страницу.  Вы можете изменить сценарий в DevTools.  

Выполните следующие действия для редактирования сценария.  

1.  Откройте файл в области **редактора** панели **Источники.**  
1.  Внести изменения в **области редактора.**  
1.  Выберите `Ctrl` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения.  DevTools заплатит весь JS-файл в javaScript-движок Microsoft Edge.  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Области редактора" lightbox="../media/javascript-sources-html-minified.msft.png":::
       Области **редактора**  
    :::image-end:::  
     
## <a name="disable-javascript"></a>Отключение JavaScript  

Перейдите [к отключению JavaScript с помощью Microsoft Edge DevTools.][DevToolsJavascriptDisable]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Приостановка кода с помощью точек остановок в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptDisable]: ./disable.md "Отключить JavaScript с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptGetStarted]: ./index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsJavascriptSnippets]: ./snippets.md "Запустите фрагменты JavaScript на любой странице с помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
