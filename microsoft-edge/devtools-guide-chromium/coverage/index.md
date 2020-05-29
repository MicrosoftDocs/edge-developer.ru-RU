---
title: Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601721"
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





# Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools   



Вкладка "покрытие" в Microsoft Edge DevTools помогает найти неиспользуемый код JavaScript и CSS.  Удаление неиспользуемого кода может ускорить загрузку страницы и сохранить мобильные данные мобильных пользователей.  

> ##### Рис. 1  
> Анализ объема протестированного кода  
> ![Анализ объема протестированного кода][ImageExample]  

> [!WARNING]
> Найти неиспользуемый код довольно просто.  Но рефакторинг базы кода таким образом, чтобы каждая страница расгрузка только JavaScript и CSS может быть сложной.  Это руководство не содержит сведения о том, как оптимизировать базу кода, чтобы избежать неиспользуемого кода, поскольку эти данные фактов сильно зависят от вашего стека технологий.  

## Обзор   

При отправке неиспользуемого сценария JavaScript или CSS часто возникают проблемы с веб-разработкой.  Например, предположим, что вы хотите использовать [компонент кнопки начальной загрузки][BootstrapButtons] на странице.  Чтобы использовать компонент Button, необходимо добавить ссылку на таблицу параметров начальной загрузки в HTML-коде, как показано ниже.  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Эта таблица стилей не только содержит код для компонента Button.  Она включает CSS для **всех** компонентов начальной загрузки.  Но вы не используете никакие другие компоненты начальной загрузки.  Таким образом, страница загружается с ненужным набором CSS.  Эта дополнительная таблица CSS является проблемой по следующим причинам.  

*   Дополнительный код замедляет загрузку страницы.  <!--See [Render-Blocking CSS][render].  -->  
*   Если пользователь получает доступ к странице на мобильном устройстве, в дополнительном коде используются данные сотовой связи.  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## Открытие вкладки "покрытие"   

1.  [Открытие меню команд][DevToolsCommandMenu].  
1.  Начните вводить текст `coverage` , выберите команду **Показать покрытие** , а затем нажмите `Enter` , чтобы выполнить команду.  В **денежном ящике**откроется вкладка **покрытие** .  

    > ##### Рисунок 2  
    > Вкладка " **покрытие** "  
    > ![Вкладка "покрытие"][ImageCoverage]  

## Запись покрытия кода   

1.  На вкладке **покрытие** нажмите одну из указанных ниже кнопок.  
    *   Нажмите кнопку **Запуск инструментирования и перезагрузка страницы** , ![ ][ImageReloadIcon] чтобы просмотреть код, необходимый для загрузки страницы.  
    *   **Instrument Coverage** ![ ][ImageRecordIcon] Если вы хотите узнать, какой код используется после взаимодействия со страницей, щелкните покрытие инструментированного покрытия.  
1.  Нажмите кнопку **остановить покрытие и выводит результаты** ![ остановить инструментирование и показать результаты, ][ImageStopIcon] когда необходимо остановить запись покрытия кода.  

## Анализ объема протестированного кода   

В таблице на вкладке **покрытие** показано, какие ресурсы были проанализированы, и сколько кода используется в каждом ресурсе. Щелкните строку, чтобы открыть ресурс на панели « **источники** » и просмотреть разбиение по строкам используемого кода и неиспользуемый код.  

> ##### Рисунок3  
> Отчет о покрытии кода  
> ![Отчет о покрытии кода][ImageExample]  

*   Столбец **URL** — это URL-адрес анализируемого ресурса.  
*   Столбец **Type (тип** ) показывает, содержит ли ресурс CSS, JavaScript или и то, и другое.  
*   Столбец **Total Bytes** — это общий размер ресурса в байтах.  
*   Столбец **неиспользованных байтов** — это количество байтов, которые не использовались.  
*   Последний безымянный столбец — это визуализация общего числа столбцов в **байтах** и **неиспользуемых байтах** .  Красная область на панели содержит неиспользуемые байты.  Зеленый раздел используется в байтах.  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Рисунок 1: анализ объема протестированного кода"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Рисунок 2: вкладка "покрытие""  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Рисунок 3: отчет о покрытии кода"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Кнопки для загрузки"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/coverage/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
