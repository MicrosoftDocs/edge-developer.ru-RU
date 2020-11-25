---
description: В каноническом руководстве по Microsoft Edge DevTools сочетания клавиш.
title: Сочетания клавиш в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d24728f493b70db2db9cd9bbe2e7e7c1ef943885
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/24/2020
ms.locfileid: "11189965"
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
   limitations under the License. -->

# Сочетания клавиш в Microsoft Edge DevTools  

Эта статья содержит справочник по сочетаниям клавиш в Microsoft Edge DevTools.

Вы также можете находить сочетания клавиш в подсказках. Наведите указатель мыши на элемент пользовательского интерфейса DevTools, чтобы отобразить всплывающую подсказку. Если элемент содержит сочетание клавиш, она будет включена в ее подсказку.

## Сочетания клавиш для открытия DevTools  

Чтобы открыть DevTools, выберите указанные ниже сочетания клавиш, пока курсор не находится в окне просмотра браузера.

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Открытие панели, которая использовалась в прошлый раз | `F12` / `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Открытие панели **консоли** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Открытие панели " **элементы** " | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` / `Command`+`Option`+`C` |  

## Общие сочетания клавиш  

Ниже перечислены сочетания клавиш, доступные в большинстве случаев, если не все, DevTools панели.

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Показать **Параметры** | `?` или `F1` | `?` / `Function`+`F1` |  
| Перемещение фокуса на следующую панель | `Control`+`]` | `Command`+`]` |  
| Фокус предыдущей панели | `Control`+`[` | `Command`+`[` |  
| Вернитесь к [положению закрепления][DevtoolsCustomizeIndexPlacement] , которое вы использовали в прошлый раз.  Если DevTools по умолчанию для всего сеанса, это сочетание закрепляет DevTools в отдельном окне. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Переключение режима [эмуляции устройства][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Переключение **режима проверки элемента** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Открытие [меню команд][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Переключение [денежных ящиков][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Нормальная загрузка | `F5` / `Control`+`R` | `Command`+`R` |  
| Окончательная Загрузка | `Control`+`F5` / `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста на текущей панели.  Не поддерживается в панелях **Аудит**, **приложения**и **Безопасность** | `Control`+`F` | `Command`+`F` |  
| Открытие вкладки **поиска** в [денежном ящике][DevtoolsCustomizeIndexDrawer], позволяющем искать текст во всех загруженных ресурсах | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Открытие файла на панели « **источники** » | `Control`+`O` / `Control`+`P` | `Command`+`O` / `Command`+`P` |  
| Увеличить масштаб | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Control`+`-` | `Command`+`-` |  
| Восстановление масштаба по умолчанию | `Control`+`0` | `Command`+`0` |  
| Выполнить сниппет | Выберите, `Control` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `!` имя сценария, после которого выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `!` имя сценария, после которого выберите `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Сочетания клавиш для панели элементов  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Отменить изменение | `Control`+`Z` | `Command`+`Z` |  
| Вернуть изменение | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Выделение элемента выше или ниже текущего выделенного элемента | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Развертывание выбранного в данный момент узла. Если узел уже развернут, этот ярлык выделяет элемент под ним | `Right Arrow` | `Right Arrow` |  
| Свертывание выбранного в данный момент узла. Если узел уже свернут, этот ярлык выделяет элемент над ним. | `Left Arrow` | `Left Arrow` |  
| Развертывание и свертывание выбранного в данный момент узла и всех дочерних элементов | `Control` + `Alt` , А затем щелкните значок **стрелки** рядом с именем элемента | `Option`, А затем щелкните значок **стрелки** рядом с именем элемента |  
| Переключение режима **изменения атрибутов** для текущего выделенного элемента | `Enter` | `Enter` |  
| Выбор следующего или предыдущего атрибута после ввода режима **изменения атрибутов** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Скрытие текущего выделенного элемента | `H` | `H` |  
| Переключение режима **редактирования в виде HTML** для текущего выделенного элемента | `Function`+`F2` | `F2` |  

### Сочетания клавиш в области стилей  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Перейдите к строке, в которой объявлено значение свойства. | Удержание `Control` и выберите значение свойства | Удержание `Command` и выберите значение свойства |  
| Переключение между RBGA, HSLA и шестнадцатеричным представлением значения цвета | `Shift`, А затем щелкните поле " **Предварительный просмотр цвета** " рядом со значением | `Shift`, А затем щелкните поле " **Предварительный просмотр цвета** " рядом со значением |  
| Выбор следующего или предыдущего свойства или значения | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` |  
| Увеличение или уменьшение значения свойства на 0,1 | Выберите значение, а затем нажмите `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Выберите значение, а затем нажмите кнопку `Option` + `Up Arrow` /Option + Стрелка вниз |  
| Увеличение или уменьшение значения свойства на 1 | Выберите значение, а затем нажмите `Up Arrow` / `Down Arrow` | Выберите значение, а затем нажмите `Up Arrow` / `Down Arrow` |  
| Увеличение или уменьшение значения свойства на 10 | Выберите значение, а затем нажмите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Выберите значение, а затем нажмите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Увеличение или уменьшение значения свойства на 100 | Выберите значение, а затем нажмите `Control`+`Up Arrow` / `Control`+`Down Arrow` | Выберите значение, а затем нажмите `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Сочетания клавиш для панели «источники»  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Приостановить выполнение сценария \ (если она выполняется) или возобновить \ (если в настоящее время приостановлено) | `F8` / `Control`+`\` | `F8` / `Command`+`\` |  
| Вызов функции перехода к следующему | `F10` / `Control`+`'` | `F10` / `Command`+`'` |  
| Перейти к следующему вызову функции | `F11` / `Control`+`;` | `F11` / `Command`+`;` |  
| Выход из текущей функции | `Shift`+`F11` / `Control`+`Shift`+`;` | `Shift`+`F11` / `Command`+`Shift`+`;` |  
| Перейти к [определенной строке кода при приостановке][DevtoolsJavascriptBreakpointsLOC] | Удержание `Control` и выбор строки кода | Удержание `Command` и выбор строки кода |  
| Выберите рамку для звонка ниже или выше текущего кадра | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Сохранение изменений, внесенных в локальные изменения | `Control`+`S` | `Command`+`S` |  
| Сохранение всех изменений | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Переход к строке | `Control`+`G` | `Control`+`G` |  
| Переход к номеру строки текущего открытого файла | Выберите, `Control` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `:` после номера строки и выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `:` после номера строки и выберите `Enter` |  
| Перейти к столбцу открытого файла \ (например, строка 5, столбец 9) | Выберите, `Control` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `:` , затем номер строки, другой номер `:` столбца, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [меню команд][DevtoolsCommandMenuIndex], введите `:` , затем номер строки, другой номер `:` столбца, а затем выберите `Enter` |  
| Если текущим файлом является HTML или сценарий, следует перейти к объявлению функции. <br /> Перейдите к набору правил, если текущий файл является таблицей стилей. | Выберите `Control` + `Shift` + `O` , а затем введите имя для объявления или набора правил или выберите его в списке параметров. | Выберите `Command` + `Shift` + `O` , а затем введите имя для объявления или набора правил или выберите его в списке параметров. |  
| Закрытие активной вкладки | `Alt`+`W` | `Option`+`W` |  

### Сочетания клавиш в редакторе кода  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Удаление всех знаков в последнем слове до курсора | `Control`+`Delete` | `Option`+`Delete` |  
| Добавление или удаление [точки останова в коде строки][DevtoolsJavascriptBreakpointsLOC] | Установите курсор на строке, а затем выберите `Control`+`B` | Установите курсор на строке, а затем выберите `Command`+`B` |  
| Переход в парную скобку | `Control`+`M` | `Control`+`M` |  
| Переключить однострочный комментарий. Если выделено несколько строк, DevTools добавляет примечание в начало каждой строки. | `Control`+`/` | `Command`+`/` |  
| Выберите или снимите следующее вхождение любого слова, на котором находится курсор. Каждое вхождение выделено одновременно | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Сочетания клавиш на панели «производительность»  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Запуск и остановка записи | `Control`+`E` | `Command`+`E` |  
| Сохранение записи | `Control`+`S` | `Command`+`S` |  
| Загрузить запись | `Control`+`O` | `Command`+`O` |  

## Сочетания клавиш на панели памяти  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Запуск и остановка записи | `Control`+`E` | `Command`+`E` |  

## Сочетания клавиш для панели консоли  

| Действие | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Предложение "разрешить автозаполнение" | `Right Arrow` или `Tab` | `Right Arrow` или `Tab` |  
| Отмена предложения автозавершения | `Escape` | `Escape` |  
| Получить предыдущую инструкцию | `Up Arrow` | `Up Arrow` |  
| Получить следующий оператор | `Down Arrow` | `Down Arrow` |  
| Фокус на **консоли** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Очистка **консоли** | `Control`+`L` | `Command`+`K` / `Option`+`L` |  
| Использование многострочного ввода.  Этот ярлык в основном не нужен, так как DevTools должен определять многострочные сценарии по умолчанию. | `Shift`+`Enter` | `Command`+`Return` |  
| Выполнение | `Enter` | `Return` |  
| Развертывание всех вложенных свойств объекта, записанного в консоли | Удерживайте `Alt` , а затем нажмите **expand** \ ( ![ разворачивание ][ImageExpandIcon] ) | Удерживайте `Alt` , а затем нажмите **expand** \ ( ![ разворачивание ][ImageExpandIcon] ) |  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ./media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexDrawer]: ./customize/index.md#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomizeIndexPlacement]: ./customize/index.md#change-devtools-placement "Изменение положения DevTools: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndex]: ./device-mode/index.md "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsJavascriptBreakpointsLOC]: ./javascript/breakpoints.md#line-of-code-breakpoints "Точки останова по строке кода: как приостановить выполнение кода с точки останова в Microsoft Edge DevTools | Документы Microsoft"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/shortcuts) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  