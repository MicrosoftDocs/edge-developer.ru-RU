---
description: Основные виды использования консоли Microsoft Edge DevTools — ведение журналов сообщений и запуск JavaScript.
title: Обзор консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399122"
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

# <a name="console-overview"></a>Обзор консоли  

  

На этой странице рассказывается, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.  Консоль **имеет** 2 основных использования: просмотр [зарегистрированных](#viewing-logged-messages) сообщений и [запуск JavaScript.](#running-javascript)  

## <a name="viewing-logged-messages"></a>Просмотр зарегистрированных сообщений  

Веб-разработчики часто в журнале сообщений на консоли, чтобы убедиться, что их JavaScript работает как ожидалось.  Чтобы войти в журнал сообщения, вставьте выражение, как `console.log('Hello, Console!')` в javaScript.  Когда браузер запускает JavaScript и обрабатывает подобное выражение, браузер регистрирует сообщение в **консоли.**  

:::row:::
   :::column span="":::
      HTML и JavaScript для страницы.  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      На следующем рисунке консоль **отображает** результаты загрузки страницы и ожидания 3 секунды.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Панель Консоли" lightbox="../media/console-console-demo.msft.png":::
         Средство **Консоли**  
      :::image-end:::  
      
      Попробуйте определить, какие строки кода привели браузер к журналу сообщений.  
   :::column-end:::
:::row-end:::  

Веб-разработчики журнал сообщений по следующим 2 общим причинам.  

*   Убедитесь, что код работает в правильном порядке.  
*   Проверка значений переменных в определенный момент времени.  

Чтобы получить практический опыт ведения журнала, перейдите к [началу работы с ведением журналов сообщений.][DevtoolsConsoleLoggingMessages]  Чтобы просмотреть полный список `console` методов, перейдите к ссылке [API консоли][DevToolsConsoleAPI].  Основное различие между методами заключается в том, как отображаются данные, которые регистрируются.  

## <a name="running-javascript"></a>Запуск JavaScript  

Консоль **также** является [rePL][WikiREPLoop].  Вы можете запустить JavaScript в **консоли, чтобы** взаимодействовать со проверяемой страницей.   

:::row:::
   :::column span="":::
      На следующем рисунке консоль **отображается** рядом с домашней страницей DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Средство Консоли рядом с домашней страницей DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         Средство **Консоли** рядом с домашней страницей DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      На следующем рисунке показана та же **** страница после использования консоли для изменения верхнего заголовка страницы.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Использование консоли для изменения верхнего заголовка страницы" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Использование консоли **для** изменения верхнего заголовка страницы  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Изменение страницы из **** консоли возможно, так как консоль **имеет** полный доступ к [окну][MDNWindow] страницы.  В DevTools есть несколько функций удобства, которые упрощают проверку страницы.  Например, предположим, что javaScript содержит функцию под названием `hideModal` .  Запуск `debug(hideModal)` приостанавливовка кода в первой строке следующего `hideModal` запуска.  Дополнительные сведения о полном списке полезных функций перейдите к ссылке [API консоли Utilities.][DevtoolsConsoleUtilitiesDebug]  

При запуске JavaScript не нужно взаимодействовать со страницей.  Вы можете использовать **консоль для** опробовки нового кода, не связанного со страницей.  Например, предположим, что вы только что узнали о встроенной карте Массива JavaScript [и][MDNMap] хотите поэкспериментировать с ним.  
Консоль **—** это хорошее место для опробовки функции.  

Дополнительные практические опыт работы с запуском JavaScript в консоли **,** перейдите к [началу работы с запуском JavaScript][DevtoolsConsoleRunningJavascript].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Справочные | Документы Майкрософт"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Начало работы с ведением журнала сообщений в консоли | Документы Майкрософт"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Начало работы с запуском JavaScript в консоли | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "отлажка — справочные ссылки на API консоли | Документы Майкрософт"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Окно | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Цикл чтения-eval-print — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
