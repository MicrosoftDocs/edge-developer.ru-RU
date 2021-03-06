---
description: В режиме событий timeline отображаются все события, срабатывав при записи.  Используйте ссылку на события временной шкалы, чтобы узнать больше о каждом типе событий временной шкалы.
title: Справка о событиях Timeline
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2a166c9eebc980682fa872e5ee8d213f2058b384
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398667"
---
<!-- Copyright Meggin Kearney and Flavio Copes

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="timeline-event-reference"></a>Справка о событиях Timeline  

В режиме событий timeline отображаются все события, срабатывав при записи.  Используйте ссылку на события временной шкалы, чтобы узнать больше о каждом типе событий временной шкалы.  

## <a name="common-timeline-event-properties"></a>Общие свойства событий временной шкалы  

Некоторые сведения присутствуют в событиях всех типов, а некоторые применяются только к определенным типам событий.  В этом разделе перечислены свойства, общие для различных типов событий.  Свойства, определенные определенным типам событий, перечислены в ссылках для последующих типов событий.  

| Свойство | Когда показано |  
|:--- |:--- |  
| Совокупное время | Для событий с **вложенными событиями**время, заданной каждой категорией событий. |  
| Стек вызовов | Для событий с **детскими событиями**время, заданной каждой категорией событий. |  
| Время ЦП | Сколько времени занял ЦП записанного события. |  
| Сведения | Другие сведения о событии. |  
| Duration \(at time-stamp\) | Сколько времени потребовалось на завершение события со всеми его детьми; timestamp — это время, в которое произошло событие, относительно времени начала записи. |  
| Время самообнаправления | Сколько времени заняло событие без детей. |  
| Размер используемой кучи | Количество памяти, используемой приложением при записи события, и дельта \(+/-\) изменяют размер используемой кучи с момента последней выборки. |  

<!--todo: add nested and child events (timelinetool) section when available -->  

## <a name="loading-events"></a>События загрузки  

В этом разделе перечислены события, которые относятся к категории Loading и их свойствам.  

| Событие | Описание |  
|:--- |:--- |  
| Parse HTML |  Microsoft Edge запустила алгоритм htmL-размыкания. |  
| Finish Loading |  Запрос сети выполнен. |  
| Получение данных |  Получены данные для запроса.  Существует одно или несколько событий получения данных. |  
| Получение ответа |  Начальный http-ответ от запроса. |  
| Отправка запроса |  Отправлен запрос сети. |  

### <a name="loading-event-properties"></a>Свойства событий загрузки  

| Свойство | Описание |  
|:--- |:--- |  
| Ресурс | URL-адрес запрашиваемого ресурса. |  
| Preview | Предварительный просмотр запрашиваемого ресурса \(только изображения\). |  
| Метод запроса | МЕТОД HTTP, используемый для запроса \( `GET` или `POST` , например\). |  
| Код состояния | Код ответа HTTP. |  
| Тип MIME | Тип MIME запрашиваемого ресурса. |  
| Закодированная длина данных | Длина запрашиваемого ресурса в bytes. |  

## <a name="scripting-events"></a>События сценариев  

В этом разделе перечислены события, которые относятся к категории Scripting и их свойствам.  

| Событие | Описание |  
|:--- |:--- |  
| Кадр анимации | Уволена запланированная анимационная рамка и вызван обработник вызова. |  
| Отмена кадра анимации |  Запланированный кадр анимации был отменен. |  
| Событие GC |  Произошел сбор мусора. |  
| DOMContentLoaded |  Событие [DOMContentLoaded][MDNWindowDOMContentLoadedEvent] было уволено браузером.  Это событие происходит при загрузке и размыве всего контента DOM страницы. |  
| Оценка скрипта | Был оценен сценарий. |  
| Событие | Событие JavaScript \(например, `mousedown` или `key` \). |  
| Вызов функции | Вызов функции JavaScript верхнего уровня был выполнен \(появляется только при входе браузера в javaScript engine\). |  
| Установка timer | Был создан timer с [setInterval()][MDNWindowOrWorkerGlobalScopeSetInterval] или [setTimeout()][MDNWindowOrWorkerGlobalScopeSetTimeout]. |  
| Кадр запроса анимации | Вызов `requestAnimationFrame()` запланил новый кадр. |  
| Удаление timer | Ранее созданный timer был очищен. |  
| Время |  Скрипт под [названием console.time()][ConsoleApiTime]. |  
| Время окончания | Скрипт под [названием console.timeEnd()][ConsoleApiTimeEnd]. |  
| Отсев времени | Отсвеченный ото всех часов, запланированный с `setInterval()` помощью или `setTimeout()` . |  
| Изменение состояния готовности XHR | Изменено готовое состояние XMLHTTPRequest. |  
| XHR Load | Готовая `XMLHTTPRequest` загрузка. |  

### <a name="scripting-event-properties"></a>Свойства событий сценариев  

| Свойство | Описание |  
|:--- |:--- |  
| Timer ID | ИД отмерить. |  
| Превышено время ожидания | Время, указанное в отоимке. |  
| Повторы | Boolean, который указывает, повторяется ли отсвечив. |  
| Вызов функции | Вызываемая функция. |  

## <a name="rendering-events"></a>События визуализации  

В этом разделе перечислены события, которые относятся к категории Rendering и их свойствам.  

| Событие | Описание |  
|:--- |:--- |  
| Недействительный макет | Макет страницы был признан недействительным из-за изменения DOM. |  
| Макет | Макет страницы завершен. |  
| Стиль пересчета | Microsoft Edge пересчитал стили элементов. |  
| Scroll | Содержимое вложенного представления было прокрутки. |  

### <a name="rendering-event-properties"></a>Свойства отрисовки событий  

| Свойство | Описание |  
|:--- |:--- |  
| Недействительный макет | Для записей layout трассировка кода, из-за чего макет был признан недействительным. |  
| Узлы, которые нуждаются в макете | Для записей Layout количество узлов, отмеченных как нуждающийся макет до начала ретрансляции.  Как правило, это те узлы, которые были признаны недействительными кодом разработчика, а также путь вверх к корнею ретрансляции. |  
| Размер дерева макета | Для записей макета общее число узлов под корнем ретрансляторов \(узел, который Microsoft Edge запускает ретранслятор\). |  
| Область макета | Возможные значения \ (граница повторного макета является `Partial` частью DOM\) или `Whole document` . |  
| Элементы, затронутые | Для пересчета записей стилей количество элементов, затронутых перерасчетом стиля. |  
| Стили недействительны | Для пересчета записей стилей предоставляется след стека кода, из-за чего стиль был признан недействительным. |  

## <a name="painting-events"></a>События рисования  

В этом разделе перечислены события, которые относятся к категории Painting и их свойствам.  

| Событие | Описание |  
|:--- |:--- |  
| Композитные слои | Композитные слои изображений для движка отрисовки Microsoft Edge. |  
| Расшифровка изображения | Расшифровка ресурса изображений. |  
| Image Resize | Изображение было реамизировано из его родных размеров. |  
| Paint | Композитные слои были окрашены в область дисплея.  При наведении на запись Paint выделяется область обновленного отображения. |  

### <a name="painting-event-properties"></a>Свойства событий рисования  

| Свойство | Описание |  
|:--- |:--- |  
| Расположение | Для событий Paint x и y координаты прямоугольника краски. |  
| Размеры | Для событий Paint высота и ширина расписной области. |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[ConsoleApiTime]: /microsoft-edge/devtools-guide-chromium/console/api#time "time - Ссылка на API консоли"  
[ConsoleApiTimeEnd]: /microsoft-edge/devtools-guide-chromium/console/api#timeend "timeEnd — ссылка на API консоли"  
<!--[EvaluatePerformanceTimelineTool]: timeline-tool "How to Use the Timeline Tool"  -->

[MDNWindowDOMContentLoadedEvent]: https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded "Окно: событие DOMContentLoaded | MDN"  
[MDNWindowOrWorkerGlobalScopeSetInterval]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setInterval "WindowOrWorkerGlobalScope.setInterval() | MDN"  
[MDNWindowOrWorkerGlobalScopeSetTimeout]: https://developer.mozilla.org/docs/Web/API/WindowTimers/setTimeout "WindowOrWorkerGlobalScope.setTimeout() | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/performance-reference) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и [Flavio Copes][FlavioCopes] \(Full Stack Developer\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[FlavioCopes]: https://developers.google.com/web/resources/contributors/flaviocopes  
