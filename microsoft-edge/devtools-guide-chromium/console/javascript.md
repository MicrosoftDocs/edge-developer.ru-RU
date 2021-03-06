---
description: Узнайте, как запустить JavaScript в консоли.
title: Начало работы с запуском JavaScript в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398821"
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

# <a name="get-started-with-running-javascript-in-the-console"></a>Начало работы с запуском JavaScript в консоли  

В этом интерактивном учебнике показано, как запустить **** JavaScript в консоли Microsoft Edge DevTools.  Дополнительные сведения о том, как вести журнал сообщений в **консоли,** перейдите по ссылке Начало работы [с ведением журнала сообщений][DevToolsConsoleLoggingMessages].  Дополнительные сведения о том, как приостановить работу кода JavaScript и пройти через него по одной строке за раз, перейдите по ссылке Начало работы с отладки [JavaScript.][DevToolsJavascriptIndex]  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   Консоль ****  
:::image-end:::  

## <a name="overview"></a>Обзор  

Консоль **—** это [REPL,][WikiReadEvalPrintLoop]которая обозначает чтение, оценку, печать и цикл.  Он считываю JavaScript, который в него введите, оценивает код, распечатывает результат [выражения,][2alityExpressionsVersusStatements]а затем возвращается к первому шагу.  

## <a name="set-up-devtools"></a>Настройка DevTools  

Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все процессы самостоятельно.  Когда вы физически следуете за ними, вы с большей вероятностью запомните рабочий процесс позже.

1.  Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\) для открытия **консоли.**  
1.  Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **консоль Javascript Example** для открытия в новом окне.  
    
    *   [Пример Javascript консоли][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Страница Консоли JavaScript Пример слева и DevTools справа" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Страница Консоли JavaScript Пример слева и DevTools справа  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a>Просмотр и изменение JavaScript или DOM страницы  

При создании или отладке страницы часто полезно запускать заявления **** в консоли, чтобы изменить внешний вид страницы или ее запуск.  
    
1.  Обратите внимание на текст на кнопке.  
1.  Введите `document.getElementById('hello').textContent = 'Hello, Console!'` консоль **и** выберите `Enter` для оценки выражения.  Обратите внимание, как меняется текст внутри кнопки.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Внешний вид консоли после оценки выражения" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Внешний вид **консоли** после оценки выражения  
    :::image-end:::  
    
    `"Hello, Console!"`, отображается ниже кода, который вы оценивали.  Помните 4 шага REPL: чтение, оценка, печать, цикл.  После оценки кода rePL печатает результат выражения.  Так `"Hello, Console!"` должен быть результат оценки `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a>Запустите произвольный JavaScript, не связанный со страницей  

Иногда просто необходимо использовать игровую площадку кода, на которой можно протестировать код или опробуете новые не знакомые функции JavaScript.  Консоль **является** идеальным местом для подобных экспериментов.  

1.  Введите `5 + 15` консоль и выберите для `Enter` оценки выражения. Консоль распечатает результат выражения под кодом.  На следующем рисунке **консоль** должна отображать результат после оценки выражения.  

1.  Введите следующий код в **консоль**.  Попробуйте ввести его, характер по-характеру, а не копирование вклеить его.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Если вы не знакомы с синтаксис, перейдите к определению значений по умолчанию `b=20` [для аргументов функции][Esma6DefaultParameterValues].  
    
1.  Теперь запустите функцию, которую вы только что определили.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль отображается после оценки выражений в фрагменте кода" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             Консоль **отображается** после оценки выражений в фрагменте кода  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` оценивает, `45` потому что, когда `add` функция вызвана без второго аргумента, `b` по умолчанию `20` .  

## <a name="next-steps"></a>Дальнейшие действия  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools позволяет приостановить сценарий в середине запуска.  В то время как вы **** приостановлены, вы можете использовать консоль для просмотра и изменения страницы в `window` этот момент `DOM` времени.  Рабочий процесс создает мощный рабочий процесс отладки.  Для интерактивного учебника перейдите к [началу работы с отладки JavaScript][DevToolsJavascriptIndex].  

Консоль **также** имеет набор функций удобства, которые упрощают взаимодействие со страницей.  Например:  

*   Вместо ввода `document.querySelector()` для выбора элемента введите `$()` .  Этот синтаксис вдохновлен jQuery, но на самом деле это не jQuery.  Это просто псевдоним для `document.querySelector()` .  
*   `debug(function)` фактически задает точку разрыва на первой строке этой функции.  
*   `keys(object)` возвращает массив, содержащий ключи указанного объекта.  

Дополнительные сведения о удобных функциях перейдите к ссылке [на API консоли Utilities.][DevToolsConsoleUtilities]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журналов сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочные | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочные ссылки на API консоли utilities | Документы Майкрософт"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и утверждения в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — расширенная обработка параметров — ECMAScript 6 — новые функции: обзор & сравнение"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Консоль Javascript Пример | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Цикл чтения-eval-print — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/javascript) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
