---
description: Каноническая документация для клавиш Microsoft Edge DevTools.
title: Ярлыки клавиатуры Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c6d51d27ce41ed8192a867cf33555b3880dd3ef9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398352"
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

# <a name="microsoft-edge-devtools-keyboard-shortcuts"></a>Ярлыки клавиатуры Microsoft Edge DevTools  

Эта статья является ссылкой на ярлыки клавиатуры в Microsoft Edge DevTools.

Вы также можете найти ярлыки в инструментах.  Наведите курсор на элемент пользовательского интерфейса DevTools, чтобы отобразить инструмент.  Если элемент имеет ярлык, его включает инструмент.

## <a name="keyboard-shortcuts-for-opening-devtools"></a>Клавиши для открытия DevTools  

Чтобы открыть DevTools, выберите следующие клавиши, в то время как курсор ориентирован на просмотр браузера.

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Откройте любую панель, используемую в последний раз | `F12` или `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Откройте **средство Консоли** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Откройте средство **Elements** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` или `Command`+`Option`+`C` |  

## <a name="global-keyboard-shortcuts"></a>Глобальные ярлыки клавиатуры  

Следующие клавиши доступны в большинстве, если не во всех, панелях DevTools.

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Показать **параметры** | `?` or `F1` | `?` или `Function`+`F1` |  
| Фокус следующей панели | `Control`+`]` | `Command`+`]` |  
| Фокус предыдущей панели | `Control`+`[` | `Command`+`[` |  
| Переключение на любую [позицию стыковки,][DevtoolsCustomizeIndexPlacement] используемую в последний раз.  Если DevTools был в положении по умолчанию на протяжении всего сеанса, этот ярлык отсоединяя DevTools в отдельное окно | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Эмуляция [устройства][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Toggle **Inspect Element Mode** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Откройте [меню команд][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Toggle the [Drawer][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Нормальное обновление | `F5` или `Control`+`R` | `Command`+`R` |  
| Жесткое обновление | `Control`+`F5` или `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Поиск текста в текущей панели.  Не поддерживается в **средствах аудита,** **приложения**и **безопасности** | `Control`+`F` | `Command`+`F` |  
| Открывает **вкладку Поиск** в [ящике,][DevtoolsCustomizeIndexDrawer]которая позволяет искать текст во всех загруженных ресурсах | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Откройте файл в панели **Источники** | `Control`+`O` или `Control`+`P` | `Command`+`O` или `Command`+`P` |  
| Масштабирование | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Уменьшить | `Control`+`-` | `Command`+`-` |  
| Восстановление масштабирования по умолчанию | `Control`+`0` | `Command`+`0` |  
| Выполнить фрагмент | Выберите, `Control` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите с `!` именем скрипта, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите с `!` именем скрипта, а затем выберите `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## <a name="elements-tool-keyboard-shortcuts"></a>Клавиши клавиатуры elements  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Отмена изменений | `Control`+`Z` | `Command`+`Z` |  
| Изменение redo | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Выберите элемент выше или ниже выбранного в настоящее время элемента | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Расширь выбранный в настоящее время узел.  Если узел уже расширен, этот ярлык выбирает элемент ниже него | `Right Arrow` | `Right Arrow` |  
| Свернуть выбранный в настоящее время узел.  Если узел уже свернут, этот ярлык выбирает элемент над ней. | `Left Arrow` | `Left Arrow` |  
| Расширение или обрушение выбранного узла и всех детей | `Control` + `Alt` Удерживайте, затем выберите значок **стрелки** рядом с именем элемента | `Option`Удерживайте, затем выберите значок **стрелки** рядом с именем элемента |  
| Изменение атрибутов **в** режиме редактирования на выбранном в настоящее время элементе | `Enter` | `Enter` |  
| Выберите следующий или предыдущий атрибут после ввода **режима Edit Attributes** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Скрыть выбранный элемент | `H` | `H` |  
| Перенаправить **в режиме HTML** на выбранном в данный момент элементе | `Function`+`F2` | `F2` |  

### <a name="styles-panel-keyboard-shortcuts"></a>Ярлыки клавиш панели стилей  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Перейдите к строке, в которой объявляется значение свойства | `Control`Удержание, а затем выберите значение свойства | `Command`Удержание, а затем выберите значение свойства |  
| Цикл через представления цвета RBGA, HSLA и Hex | `Shift`Удерживайте, а затем выберите поле **"Просмотр** цвета" рядом со значением | `Shift`Удерживайте, а затем выберите поле **"Просмотр** цвета" рядом со значением |  
| Выберите следующее или предыдущее свойство или значение | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` | Выберите имя или значение свойства, а затем выберите `Tab` / `Shift`+`Tab` |  
| Приращение или отсев значения свойства на 0,1 | Выберите значение, а затем выберите `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Выберите значение, а затем `Option` + `Up Arrow` выберите /Option+Down Arrow |  
| Приращение или приумножная приращение значения свойства на 1 | Выберите значение, а затем выберите `Up Arrow` / `Down Arrow` | Выберите значение, а затем выберите `Up Arrow` / `Down Arrow` |  
| Приращение или приумнождение значения свойства на 10 | Выберите значение, а затем выберите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Выберите значение, а затем выберите `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Приращение или приумножная приращение значения свойства на 100 | Выберите значение, а затем выберите `Control`+`Up Arrow` / `Control`+`Down Arrow` | Выберите значение, а затем выберите `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## <a name="sources-tool-keyboard-shortcuts"></a>Ярлыки клавиатуры инструментов источников  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Приостановка запуска скрипта \(если в настоящее время запущен\) или возобновление \(если в настоящее время приостановлено\) | `F8` или `Control`+`\` | `F8` или `Command`+`\` |  
| Шаг за следующим вызовом функции | `F10` или `Control`+`'` | `F10` или `Command`+`'` |  
| Шаг в следующий вызов функции | `F11` или `Control`+`;` | `F11` или `Command`+`;` |  
| Выход из текущей функции | `Shift`+`F11` или `Control`+`Shift`+`;` | `Shift`+`F11` или `Command`+`Shift`+`;` |  
| Продолжайте работу с [определенной строкой кода, приостанавлив][DevtoolsJavascriptBreakpointsLOC] | `Control`Удержание, затем выберите строку кода | `Command`Удержание, затем выберите строку кода |  
| Выберите кадр вызова ниже или выше выбранного в настоящее время кадра | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Сохранение изменений в локальных изменениях | `Control`+`S` | `Command`+`S` |  
| Сохранение всех изменений | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Перейдите к строке | `Control`+`G` | `Control`+`G` |  
| Переход на строку номера открытого в настоящее время файла | Выберите, `Control` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите номер `:` строки, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите номер `:` строки, а затем выберите `Enter` |  
| Переход в столбец открытого в настоящее время файла \(например, строка 5, столбец 9\) | Выберите, `Control` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите, затем номер строки, затем другой, затем номер `:` `:` столбца, а затем выберите `Enter` | Выберите, `Command` + `O` чтобы открыть [командное меню,][DevtoolsCommandMenuIndex]введите, затем номер строки, затем другой, затем номер `:` `:` столбца, а затем выберите `Enter` |  
| Перейдите к объявлению функции, если текущий файл HTML или скрипт.  <br />  Перейдите к набору правил, если текущий файл — это таблица стилей.  | Выберите, затем введите имя набора объявлений и правил или выберите его `Control` + `Shift` + `O` из списка параметров | Выберите, затем введите имя набора объявлений и правил или выберите его `Command` + `Shift` + `O` из списка параметров |  
| Закрыть активную вкладку | `Alt`+`W` | `Option`+`W` |  

### <a name="code-editor-keyboard-shortcuts"></a>Ярлыки клавиатуры редактора кода  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Удаление всех символов в последнем слове, в том числе курсора | `Control`+`Delete` | `Option`+`Delete` |  
| Добавление или удаление [точки взлома строки кода][DevtoolsJavascriptBreakpointsLOC] | Сосредоточь курсор на строке, а затем выберите `Control`+`B` | Сосредоточь курсор на строке, а затем выберите `Command`+`B` |  
| Перейдите к скобке со соответствием | `Control`+`M` | `Control`+`M` |  
| Toggle single-line comment.  Если выбрано несколько строк, DevTools добавляет комментарий к началу каждой строки. | `Control`+`/` | `Command`+`/` |  
| Включите или отключите следующее вхождение любого слова, включаемого курсором.  Каждое событие выделяется одновременно | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## <a name="performance-tool-keyboard-shortcuts"></a>Ярлыки клавиатуры инструмента производительности  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Запуск и остановка записи | `Control`+`E` | `Command`+`E` |  
| Сохранение записи | `Control`+`S` | `Command`+`S` |  
| Запись загрузки | `Control`+`O` | `Command`+`O` |  

## <a name="memory-tool-keyboard-shortcuts"></a>Ярлыки клавиатуры средства памяти  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Запуск и остановка записи | `Control`+`E` | `Command`+`E` |  

## <a name="console-tool-keyboard-shortcuts"></a>Клавиши клавиатуры консоли  

| Действие | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Принять предложение автозаполнеть | `Right Arrow` or `Tab` | `Right Arrow` or `Tab` |  
| Отклонение предложения автозаполнеть | `Escape` | `Escape` |  
| Получить предыдущее заявление | `Up Arrow` | `Up Arrow` |  
| Получить следующее утверждение | `Down Arrow` | `Down Arrow` |  
| Фокус **консоли** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Очистка **консоли** | `Control`+`L` | `Command`+`K` или `Option`+`L` |  
| Принудить к многостройной записи.  Этот ярлык в основном необязательен, так как DevTools должен обнаруживать многолинейные сценарии по умолчанию | `Shift`+`Enter` | `Command`+`Return` |  
| Выполнение | `Enter` | `Return` |  
| Расширь все свойства объекта, зарегистрированного в консоли | `Alt`Удержание, затем **выберите Расширение** \. ![ ][ImageExpandIcon] Развяжите \) | `Alt`Удержание, затем **выберите Расширение** \. ![ ][ImageExpandIcon] Развяжите \) |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Ящик — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Изменение размещения DevTools — настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Breakpoints line-of-code - How to pause your code with breakpoints in Microsoft Edge DevTools | Документы Майкрософт"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/shortcuts) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  