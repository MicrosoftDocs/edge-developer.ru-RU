---
description: Узнайте, как запустить JavaScript в консоли.
title: Начало работы с запуском JavaScript в консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: ecd1a2fffb311990b6e743e99d038f1f2a519ee4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231092"
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

# Начало работы с запуском JavaScript в консоли  

В этом интерактивном руководстве показано, как запустить **** JavaScript в консоли Microsoft Edge DevTools.  Дополнительные сведения о регистрации сообщений в консоли **можно**найти в окне "Начало работы [с сообщениями журналов".][DevToolsConsoleLoggingMessages]  Дополнительные сведения о приостановки кода JavaScript и пошаговом его пошаговом переходе к началу работы с [отладки JavaScript.][DevToolsJavascriptIndex]  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="Консоль" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   Консоль ****  
:::image-end:::  

## Обзор  

Консоль **—** это [REPL,][WikiReadEvalPrintLoop]который обозначает чтение, оценку, печать и цикл.  Он считывает в него код JavaScript, оценивает код, выпечатает результат [выражения,][2alityExpressionsVersusStatements]а затем возвращается к первому шагу.  

## Настройка DevTools  

Это руководство предназначено для вас, чтобы открыть демонстрацию и попробовать все процессы самостоятельно.  Когда вы будете физически следовать этому пути, скорее всего, позже запомните эти процессы.

1.  Выберите `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\) для открытия **консоли.**  
1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.  
    
    *   [Пример кода Javascript консоли][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Страница Пример кода javaScript консоли слева и DevTools справа" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Страница "Пример кода javaScript консоли" слева и DevTools справа  
    :::image-end:::  
    
## Просмотр и изменение JavaScript или DOM страницы  

При создании или отладке страницы часто полезно запускать в **** консоли утверждения, чтобы изменить внешний вид или запуск страницы.  
    
1.  Обратите внимание на текст на кнопке.  
1.  Введите `document.getElementById('hello').textContent = 'Hello, Console!'` в **консоли** и выберите `Enter` для оценки выражения.  Обратите внимание, как изменяется текст внутри кнопки.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Внешний вид консоли после оценки выражения" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Внешний вид **консоли** после оценки выражения  
    :::image-end:::  
    
    Под кодом, который вы вычисляли, вы видите `"Hello, Console!"` .  Напомню 4 шага REPL: чтение, оценка, печать, цикл.  После оценки кода rePL печатает результат выражения.  Это `"Hello, Console!"` должен быть результат оценки. `document.getElementById('hello').textContent = 'Hello, Console!'`  
    
## Запуск произвольного Кода JavaScript, не связанного со страницей  

Иногда вам просто нужна функциональная возможность кода, в которой можно протестировать код или попробовать новые функции JavaScript, которые вам незнакомы.  Консоль **идеально** подходит для экспериментов такого рода.  

1.  Введите `5 + 15` в консоли и выберите для `Enter` оценки выражения. Консоль выпечатает результат выражения под кодом.  На следующем рисунке **после** оценки выражения в консоли должен отображаться результат.  

1.  Введите следующий код в **консоль.**  Попробуйте ввести его по символам, а не копировать.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Если вы не знакомы с синтаксисом, перейдите к определению значений по умолчанию `b=20` [для аргументов функции.][Esma6DefaultParameterValues]  
    
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
    
    `add(25)` `45`оценивается, так как когда функция вызвана без второго `add` аргумента, значение по умолчанию — `b` `20` .  

## Дальнейшие действия  

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools позволяет приостановить сценарий в середине работы.  Пока вы приостановлены, вы **** можете использовать консоль для просмотра и изменения страницы или страницы в `window` этот момент `DOM` времени.  Рабочий процесс создает мощный рабочий процесс отладки.  Интерактивное руководство по началу работы [с отладой JavaScript.][DevToolsJavascriptIndex]  

Консоль **также** имеет набор удобных функций, упрощающих взаимодействие со страницей.  Например:  

*   Вместо ввода `document.querySelector()` текста для выбора элемента введите `$()` .  Этот синтаксис навеян jQuery, но на самом деле он не является jQuery.  Это просто псевдоним для `document.querySelector()` .  
*   `debug(function)` эффективно задает точку останова в первой строке этой функции.  
*   `keys(object)` возвращает массив, содержащий ключи указанного объекта.  

Дополнительные сведения об удобных функциях можно найти в справочнике [по API консоли.][DevToolsConsoleUtilities]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журнала сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Справочник по консоли | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API консольных utilities | Документы Майкрософт"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и выражения в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — расширенная обработка параметров — ECMAScript 6 — новые функции: обзор & сравнения"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Пример кода Javascript консоли | Временный сбой"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Цикл read-eval-print — Википдия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/console/javascript) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
