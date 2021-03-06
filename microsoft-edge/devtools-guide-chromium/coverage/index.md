---
description: Поиск и анализ неиспользванного кода JavaScript и CSS в Microsoft Edge DevTools.
title: Найдите неиспользванный код JavaScript и CSS с панелью покрытия в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398765"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a>Найдите неиспользванный код JavaScript и CSS с панелью Coverage в Microsoft Edge DevTools  

Панель **coverage** в Microsoft Edge DevTools помогает найти неиспользванный код JavaScript и CSS.  Удаление неиспользованого кода может ускорить загрузку страницы и сохранить мобильные данные пользователей сотовой связи.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Анализ покрытия кода" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Анализ покрытия кода  
:::image-end:::  

> [!WARNING]
> Поиск неиспользованого кода относительно прост.  Но рефакторинг базы кода таким образом, что каждая страница передает только JavaScript и CSS, что она нуждается может быть трудно.  В этом руководстве не сообщается, как рефакторировать базу кода, чтобы избежать неиспользованого кода, так как эти рефакторы сильно зависят от стека технологий.  

## <a name="overview"></a>Обзор  

Доставка неиспользована JavaScript или CSS является распространенной проблемой в веб-разработке.  Например, предположим, что на странице необходимо использовать компонент [кнопки Bootstrap.][BootstrapButtons]  Чтобы использовать компонент кнопки, необходимо добавить ссылку на таблицу стилей Bootstrap в HTML, например:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

В этом таблице стилей не только содержится код компонента кнопки.  Он содержит CSS для **всех** компонентов Bootstrap.  Но вы не используете ни один из других компонентов Bootstrap.  Таким образом, ваша страница скачивает кучу CSS, что она не нужна.  Этот дополнительный CSS является проблемой по следующим причинам.  

*   Дополнительный код замедляет загрузку страницы.  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   Если пользователь получает доступ к странице на мобильном устройстве, дополнительный код использует данные сотовой связи.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a>Откройте панель Coverage  

1.  [Откройте командное меню.][DevToolsCommandMenu]  
1.  Начните `coverage` печатать, выберите команду **Show Coverage,** а затем `Enter` выберите для запуска команды.  Панель **Coverage** открывается в **ящике**.  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Панель Coverage" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       Панель **Coverage**  
    :::image-end:::  
    
## <a name="record-code-coverage"></a>Покрытие кода записи  

1.  Выберите одну из следующих кнопок в панели **Coverage.**  
    *   Если **вы хотите** просмотреть код, необходимый для загрузки страницы, выберите страницу Начните использовать средства и перезагрузить ![ страницу \. ][ImageReloadIcon]  
    *   Если **вы хотите** просмотреть код, используемый после взаимодействия со страницей, выберите охват инструментов ![ ][ImageRecordIcon] \.  
1.  Выберите **stop Instrumenting Coverage and Show Results** \( Stop Instrumenting Coverage and Show Results \) при остановке записи ![ ][ImageStopIcon] кода.  
    
## <a name="analyze-code-coverage"></a>Анализ покрытия кода  

В таблице панели **Coverage** отображаются проанализированые ресурсы и объем кода, используемый в каждом ресурсе.  Выберите строку, чтобы открыть этот ресурс в панели **Источники** и просмотреть строковую разбивку используемого кода и неиспользованого кода.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Отчет о покрытии кода" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Отчет о покрытии кода  
:::image-end:::  

*   **Url-адрес** — это URL-адрес проанализированого ресурса.  
*   В **столбце Тип** говорится, содержит ли ресурс CSS, JavaScript или оба.  
*   Столбец **Total Bytes** — это общий размер ресурса в bytes.  
*   **Неиспользованный** столбец Bytes — это число неиспользованых bytes.  
*   Последний неназванный столбец — это визуализация столбцов **Total Bytes** и **Unused Bytes.**  Красный раздел панели неиспользован bytes.  Зеленый раздел используется bytes.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Кнопки — Bootstrap"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/coverage/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
