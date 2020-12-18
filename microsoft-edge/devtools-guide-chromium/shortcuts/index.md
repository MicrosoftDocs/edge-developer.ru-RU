---
description: Каноническая документация по Microsoft Edge DevTools сочетания клавиш.
title: Сочетания клавиш Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 417e2235e4ea63d0258c158035ea201cd5657099
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235148"
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

# Сочетания клавиш Microsoft Edge DevTools  

Эта статья является ссылкой на сочетания клавиш в Microsoft Edge DevTools.

Также можно найти ярлыки во ветвях инструментов.  Наведите курсор на элемент пользовательского интерфейса DevTools, чтобы отобразить ее.  Если элемент имеет ярлык, то в него включается его.

## Сочетания клавиш для открытия DevTools  

Чтобы открыть DevTools, выберите следующие сочетания клавиш, пока курсор будет ориентирован на окна просмотра браузера.

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Откройте любую панель, которая использовалась в последний раз | `F12` или `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Открытие панели **консоли** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Открытие панели **элементов** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` или `Command`+`Option`+`C` |  

## Глобальные сочетания клавиш  

Следующие сочетания клавиш доступны в большинстве (если не во всех) панелях DevTools.

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Показать **параметры** | `?` или `F1` | `?` или `Function`+`F1` |  
| Фокус на следующей панели | `Control`+`]` | `Command`+`]` |  
| Фокус на предыдущей панели | `Control`+`[` | `Command`+`[` |  
| Переключиться на любую [позицию док-станции,][DevtoolsCustomizeIndexPlacement] которая использовалась в последний раз.  Если DevTools был в позиции по умолчанию для всего сеанса, то этот ярлык отсоединяя DevTools в отдельное окно | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Toggle [Device emulation][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Откройте меню [команд][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Перегонать [ящик][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Обычная перезагрузка | `F5` или `Control`+`R` | `Command`+`R` |  
| Твердая перезагрузка | `Control`+`F5` или `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста на текущей панели.  Не поддерживается в **панелях аудита,** **приложений** **и** безопасности | `Control`+`F` | `Command`+`F` |  
| Открывает **вкладку "Поиск"** в [средстве "Drawer",][DevtoolsCustomizeIndexDrawer]которая позволяет искать текст во всех загруженных ресурсах | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Открытие файла на панели **источников** | `Control`+`O` или `Control`+`P` | `Command`+`O` или `Command`+`P` |  
| Масштабирование | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Control`+`-` | `Command`+`-` |  
| Восстановление уровня масштабирования по умолчанию | `Control`+`0` | `Command`+`0` |  
| Запуск фрагмента кода | Выберите, `Control` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, введите после имени `!` скрипта, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, `!` введите после имени скрипта, а затем выберите `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Сочетания клавиш панели элементов  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Отмена изменения | `Control`+`Z` | `Command`+`Z` |  
| Изменение для повторного изменения | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Выберите элемент выше или под текущим выбранным элементом | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Раз expand the currently selected node.  Если узел уже расширен, этот ярлык выбирает элемент под ней | `Right Arrow` | `Right Arrow` |  
| Свернуть текущий выбранный узел.  Если узел уже свернут, этот ярлык выбирает элемент над ней | `Left Arrow` | `Left Arrow` |  
| Развернуть или свернуть текущий выбранный узел и все его потомки | Удерживайте, а затем выберите значок со стрелкой `Control` + `Alt` рядом с именем элемента **** | Удерживайте, а затем выберите значок со стрелкой `Option` рядом с именем элемента **** |  
| Toggle **Edit Attributes** mode on the currently selected element | `Enter` | `Enter` |  
| Выберите следующий или предыдущий атрибут после ввода **режима "Изменить атрибуты"** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Скрытие выбранного элемента | `H` | `H` |  
| Toggle **Edit as HTML** mode on the currently selected element | `Function`+`F2` | `F2` |  

### Сочетания клавиш области стилей  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Перейдите к строке, в которой объявляется значение свойства | `Control`Удержание и выбор значения свойства | `Command`Удержание и выбор значения свойства |  
| Циклическое представление значения цвета с помощью RBGA, HSLA и Hex | `Shift`Удержание, а затем выберите **поле просмотра** цвета рядом со значением | `Shift`Удержание, а затем **выберите поле просмотра** цвета рядом со значением |  
| Выберите следующее или предыдущее свойство или значение | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` |  
| Приращение и приращение значения свойства на 0,1 | Выберите значение, а затем выберите `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Выберите значение, а затем `Option` + `Up Arrow` выберите / Option+СТРЕЛКА ВНИЗ |  
| Приращение и приращение значения свойства на 1 | Выберите значение, а затем выберите `Up Arrow` / `Down Arrow` | Выберите значение, а затем выберите `Up Arrow` / `Down Arrow` |  
| Приращение и приращение значения свойства на 10 | Выберите значение, а затем выберите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Выберите значение, а затем выберите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Приращение и приращение значения свойства на 100 | Выберите значение, а затем выберите `Control`+`Up Arrow` / `Control`+`Down Arrow` | Выберите значение, а затем выберите `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Сочетания клавиш панели источников  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Приостановка работы сценария \(если в данный момент запущен\) или возобновление \(если в настоящее время приостановлено\) | `F8` или `Control`+`\` | `F8` или `Command`+`\` |  
| Шаг за следующим вызовом функции | `F10` или `Control`+`'` | `F10` или `Command`+`'` |  
| Шаг в следующий вызов функции | `F11` или `Control`+`;` | `F11` или `Command`+`;` |  
| Выход из текущей функции | `Shift`+`F11` или `Control`+`Shift`+`;` | `Shift`+`F11` или `Command`+`Shift`+`;` |  
| Продолжите работу [с определенной строкой кода, пока она приостановлена][DevtoolsJavascriptBreakpointsLOC] | `Control`Удержание, а затем выберите строку кода | `Command`Удержание, а затем выберите строку кода |  
| Выберите кадр вызова ниже или над текущим выбранным кадром | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Сохранение изменений в локальных изменениях | `Control`+`S` | `Command`+`S` |  
| Сохранение всех изменений | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Перейти к строке | `Control`+`G` | `Control`+`G` |  
| Перейти к номеру строки открытого в данный момент файла | Выберите, `Control` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, `:` введите номер строки, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, `:` введите номер строки, а затем выберите `Enter` |  
| Перейти к столбце открытого в данный момент файла \(например, строка 5, столбец 9\) | Выберите, `Control` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, введите , затем номер строки, затем другой, затем номер `:` `:` столбца, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы [][DevtoolsCommandMenuIndex]открыть меню команд, введите, затем номер строки, затем другой, затем номер `:` `:` столбца, а затем выберите `Enter` |  
| Перейдите к объявлению функции, если текущим файлом является HTML или сценарий.  <br />  Перейдите к набору правил, если текущий файл является таблицой стилей.  | Выберите, затем введите имя объявления или набора правил или выберите его `Control` + `Shift` + `O` в списке параметров | Выберите, затем введите имя объявления или набора правил или выберите `Command` + `Shift` + `O` его в списке параметров |  
| Закроем активную вкладку | `Alt`+`W` | `Option`+`W` |  

### Сочетания клавиш редактора кода  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Удаление всех символов в последнем слове до курсора | `Control`+`Delete` | `Option`+`Delete` |  
| Добавление или удаление [точки останова кода][DevtoolsJavascriptBreakpointsLOC] | Настроите курсор на строку, а затем выберите `Control`+`B` | Настроите курсор на строку, а затем выберите `Command`+`B` |  
| Go to matching bracket | `Control`+`M` | `Control`+`M` |  
| Перенимаем одностроный комментарий.  Если выбрано несколько строк, DevTools добавляет комментарий в начало каждой строки | `Control`+`/` | `Command`+`/` |  
| Выберите или отбирать следующее слово, в которое вмеется курсор.  Каждое событие выделяется одновременно | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Сочетания клавиш для панели производительности  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Начало/остановка записи | `Control`+`E` | `Command`+`E` |  
| Сохранение записи | `Control`+`S` | `Command`+`S` |  
| Загрузка записи | `Control`+`O` | `Command`+`O` |  

## Сочетания клавиш для панели памяти  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Начало/остановка записи | `Control`+`E` | `Command`+`E` |  

## Сочетания клавиш панели консоли  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Принятие предложения автозаполнеия | `Right Arrow` или `Tab` | `Right Arrow` или `Tab` |  
| Отклонение предложения автозаполнеия | `Escape` | `Escape` |  
| Получить предыдущее утверждение | `Up Arrow` | `Up Arrow` |  
| Get next statement | `Down Arrow` | `Down Arrow` |  
| Фокус **на** консоли | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Очистка **консоли** | `Control`+`L` | `Command`+`K` или `Option`+`L` |  
| Принудительное ввод многострок.  Этот ярлык в основном не является нужным, так как DevTools должен обнаруживать многостроки по умолчанию | `Shift`+`Enter` | `Command`+`Return` |  
| Выполнение | `Enter` | `Return` |  
| Разорвем все под свойства объекта, зарегистрированного в консоли | Hold `Alt` , then choose **Expand** \( ![ Expand ][ImageExpandIcon] \) | Hold `Alt` , then choose **Expand** \( ![ Expand ][ImageExpandIcon] \) |  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Изменение размещения DevTools — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Точки останова кода: приостановка кода с помощью точек останова в Microsoft Edge DevTools | Документы Майкрософт"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/shortcuts) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  