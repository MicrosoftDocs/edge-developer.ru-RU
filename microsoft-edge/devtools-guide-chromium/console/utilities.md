---
description: Ссылка на удобные команды, доступные в консоли Microsoft Edge DevTools.
title: Ссылка на API консоли utilities
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398828"
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

# <a name="console-utilities-api-reference"></a>Ссылка на API консоли utilities  

API консоли Utilities содержит набор команд удобства для выполнения общих задач: выбора и проверки элементов DOM, отображения данных в читаемом формате, остановки и запуска профиля и мониторинга событий DOM.  

> [!WARNING]
> Следующие команды работают только в консоли Microsoft Edge DevTools.  Команды не работают при запуске из скриптов.  

Для `console.log()` остальных `console.error()` методов и методов перейдите к `console.*` [ссылке консоли API.][DevToolsConsoleApi]  

## <a name="recently-evaluated-expression"></a>Недавно оцененное выражение  

```console
$_
```  

Возвращает значение последнего оцениваемого выражения.  

На следующем рисунке оценивается простое выражение `2 + 2` \( \).  Затем `$_` свойство оценивается, которое содержит одно и то же значение.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ — это наиболее недавно оцененное выражение" lightbox="../media/console-arithmatic.msft.png":::
   Рис. 1:  `$_` это наиболее недавно оцененное выражение  
:::image-end:::  

На следующем рисунке оцениваемая экспрессия изначально содержит массив имен.  Оценивая длину массива, значение, сохраненное в изменениях, чтобы стать `$_.length` `$_` последним оцениваемого выражения, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="Изменения $_ при оценке новых команд" lightbox="../media/console-array-length.msft.png":::
   Рис. 2.  `$_` Изменения при оценке новых команд  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a>Недавно выбранный элемент или объект JavaScript  

```console
$0
```  

Возвращает последний элемент или объект JavaScript.  `$1` возвращает второй недавно выбранный и так далее.  Команды и команды работают в качестве исторической ссылки на последние пять элементов DOM, инспектировался в инструменте Elements или в последних пяти объектах `$0` `$1` `$2` `$3` `$4` JavaScript, **** **** выбранных в средстве Памяти.  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

На следующем рисунке элемент `img` выбирается в **инструменте Elements.**  В **ящике консоли** была оценена и `$0` отображается один и тот же элемент.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Рис. 3. `$0`  
:::image-end:::  

На следующем рисунке на изображении показан другой элемент, выбранный на одной странице.  Теперь `$0` относится к недавно выбранному элементу, а возвращает выбранный `$1` ранее элемент.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Рис. 4. `$1`  
:::image-end:::  

## <a name="query-selector"></a>Селектор запросов  

```console
$(selector, [startNode])
```  

Возвращает ссылку на первый элемент DOM с указанным селектором CSS.  Этот метод является псевдонимом метода [document.querySelector().][MDNDocumentQuerySelector]  

На следующем рисунке возвращается ссылка на первый элемент `<img>` документа.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Рис. 5. `$('img')`  
:::image-end:::  

Наведите курсор на возвращаемом результате, откройте контекстное **** меню \(правой кнопкой мыши\) **** и выберите Показать в панели элементов, чтобы найти его в DOM или прокрутите, чтобы просмотреть его на странице.  

На следующем рисунке возвращается ссылка на выбранный в настоящее время элемент и отображается свойство SRC.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="The $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Рис. 6. `$('img').src`  
:::image-end:::  

Этот метод также поддерживает второй параметр startNode, который указывает элемент или узел для поиска элементов.  Значение параметра по умолчанию `document` .  

На следующем рисунке первый элемент найден после того, как возвращается правильно `img` `title--image` `src` отображаемый элемент.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="The $('img', document.querySelector('title--image')))src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Рис. 7. `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Если вы используете библиотеку, например jQuery, которая использует, функциональность перезаписана и соответствует реализации `$` `$` из этой библиотеки.  

## <a name="query-selector-all"></a>Селектор запросов Все  

```console
$$(selector, [startNode])
```  

Возвращает массив элементов, которые соответствуют указанному селектору CSS.  Этот метод эквивалентен запуску [метода document.querySelectorAll().][MDNDocumentQuerySelectorAll]  

В следующем примере кода и рисунке используйте для создания массива всех элементов текущего документа и отображения значения `$$()` `<img>` свойства для каждого `src` элемента.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Использование $$() для выбора всех изображений в документе и отображения источников" lightbox="../media/console-element-selector-image-all.msft.png":::
   Рис. 8. Использование `$$()` для выбора всех изображений в документе и отображения источников  
:::image-end:::  

Этот метод также поддерживает второй параметр startNode, который указывает элемент или узел для поиска элементов.  Значение параметра по умолчанию `document` .  

В следующем примере кода и рисунке измененная версия предыдущего примера кода и рисунка использует для создания массива всех элементов, которые отображаются в текущем документе после выбранного `$$()` `<img>` узла.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Использование $$() для выбора всех изображений, которые отображаются после указанного элемента <div> документа, и отображения источников" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Рис. 9. Использование для выбора всех изображений, которые отображаются после указанного элемента в документе, и `$$()` `<div>` отображения источников  
:::image-end:::  

> [!NOTE]
> Выберите `Shift` + `Enter` в консоли, чтобы запустить новую строку без запуска сценария.  

## <a name="xpath"></a>XPath  

```console
$x(path, [startNode])
```  

Возвращает массив элементов DOM, которые соответствуют указанному выражению XPath.  

В следующем примере кода и рисунке возвращаются все элементы на `<p>` странице.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Использование селектора XPath" lightbox="../media/console-array-xpath.msft.png":::
   Рис. 10. Использование селектора XPath  
:::image-end:::  

В следующем примере кода и рисунке возвращаются все элементы, содержащие `<p>` `<a>` элементы.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Использование более сложного селектора XPath" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Рис. 11. Использование более сложного селектора XPath  
:::image-end:::  

Как и другие команды селектора, имеет необязательный второй параметр, который указывает элемент или узел, из которого можно искать `$x(path)` `startNode` элементы.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Использование селектора XPath с помощью startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Рис. 12. Использование селектора XPath с `startNode`  
:::image-end:::  

## <a name="clear"></a>clear  

```console
clear()
```  

Очищает консоль истории.  

```console
clear()
```  

## <a name="copy"></a>copy  

```console
copy(object)
```  

Метод `copy(object)` копирует строковую репрезентативность указанного объекта в буфер обмена.  

```console
copy($0)
```  

## <a name="debug"></a>отладка  

```console
debug(method)
```  

>[!NOTE]
> Проблема [Chromium #1050237][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.  Если вы столкнулись с проблемой, [попробуйте использовать точки перерывов.][DevtoolsJavascriptBreakpoints]  

При запросе указанного метода отладка вызывается и ломается внутри метода на средстве **Sources,** позволяя вам ступить через код и отладить его.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Взлом метода с помощью отлаговки()" lightbox="../media/console-debug-text.msft.png":::
   Рис. 13. Взлом метода с помощью `debug()`  
:::image-end:::  

Используйте `undebug(method)` для остановки взлома метода или использования пользовательского интерфейса для отключения всех точек взлома.  

Дополнительные сведения о точках остановок перейдите к [паузе кода с breakpoints][DevToolsJavascriptBreakpoints].  

## <a name="dir"></a>dir  

```console
dir(object)
```  

Отображает список всех свойств указанного объекта в стиле объекта.  Этот метод является псевдонимом [метода console.dir().][MDNConsoleDir]  

Оцените `document.head` в консоли отображение HTML между `<head>` `</head>` тегами и тегами.  В следующем примере кода и рисунке после использования в консоли отображается список в стиле `console.dir()` объекта.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Ведение журнала document.head с помощью метода dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Рис. 14. Ведение журнала `document.head` с помощью `dir()` метода  
:::image-end:::  

Дополнительные сведения перейдите к [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API консоли.  

## <a name="dirxml"></a>dirxml  

```console
dirxml(object)
```  

Печать XML-представления указанного объекта, отображаемого в **средстве Elements.**  Этот метод эквивалентен [методу console.dirxml().][MDNConsoleDirxml]  

## <a name="inspect"></a>проверка  

```console
inspect(object/method)
```  

Открывает и выбирает указанный элемент или объект в соответствующей панели: либо средство **** **Elements** для элементов DOM, либо средство памяти для объектов кучи JavaScript.  

В следующем примере кода и рисунке `document.body` откроется средство **Elements.**  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Проверка элемента с помощью проверки()" lightbox="../media/console-inspect-document-body.msft.png":::
   Рис. 15. Проверка элемента с помощью `inspect()`  
:::image-end:::  

При передаче метода для проверки метод открывает документ в **инструменте Источники** для проверки.  

## <a name="geteventlisteners"></a>getEventListeners  

```console
getEventListeners(object)
```  

Возвращает слушателей событий, зарегистрированных на указанном объекте.  Возвращаемая величина — это объект, содержащий массив для каждого зарегистрированного типа событий \(например `click` или `keydown` \).  Участники каждого массива — это объекты, описывая прослушиватель, зарегистрированный для каждого типа.  В следующем примере кода перечислены все слушатели событий, зарегистрированные на объекте документа.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Выход с помощью getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Рис. 16. Результат использования `getEventListeners(document)`  
:::image-end:::  

Если на указанном объекте зарегистрировано несколько слушателей, массив содержит член для каждого слушателя.  На следующем рисунке в элементе документа для события зарегистрированы два слушателя `click` событий.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Несколько слушателей" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Рис. 17. Несколько слушателей  
:::image-end:::  

Вы можете дополнительно расширить каждый из следующих объектов, чтобы изучить свойства.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Расширенное представление объекта-слушателя" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Рис. 18. Расширенное представление объекта-слушателя  
:::image-end:::  

## <a name="keys"></a>клавиши  

```console
keys(object)
```  

Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.  Чтобы получить связанные значения тех же свойств, используйте `values()` .  

Например, предположим, что ваше приложение определило следующий объект.  

```console
var player1 =   
```  

В следующих примерах кода и рисунке предполагается, что результат был определен в глобальном пространстве имен \(для простоты\) до ввода и `player1` `keys(player1)` в `values(player1)` консоли.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Команды клавиши() и значения()" lightbox="../media/console-keys-values.msft.png":::
   Рис. 19. Команды `keys()` `values()` и команды  
:::image-end:::  

## <a name="monitor"></a>монитор  

```console
monitor(method)
```  

В журнале сообщения на консоль, которое указывает имя метода, а также аргументы, которые передаются методу при его призыве.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Метод monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Рис. 20. `monitor()` Метод  
:::image-end:::  

Использование `unmonitor(method)` для прекращения мониторинга.  

## <a name="monitorevents"></a>monitorEvents  

```console
monitorEvents(object[, events])
```  

Когда одно из указанных событий происходит на указанном объекте, объект события регистрируется на консоли.  Можно указать одно событие для мониторинга, массив событий или один из типов общих событий, которые соединяются с предопределяемой коллекцией событий.  Просмотрите следующий пример кода и рисунок.  

Далее отслеживаются все события, происходящие в окне.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Мониторинг событий в окне" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Рис. 21. Мониторинг событий в окне  
:::image-end:::  

Далее определяется массив для мониторинга событий и событий `resize` `scroll` на объекте окна.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Вы также можете указать один из доступных типов событий, строки, которые соединяются с предопределенными наборами событий.  В следующей таблице отображаются доступные типы событий и связанные сопоставления событий.  

| Тип события | Соответствующие события, относясь к карте |  
|:--- |:--- |  
| `mouse` | "click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel" |  
| `key` | "keydown", "keypress", "keyup", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom" |  

В следующем примере кода тип события, соответствующий событиям в текстовом поле ввода, в настоящее время выбирается `key` `key` в **инструменте Elements.**  

```console
monitorEvents($0, "key");
```  

На следующем рисунке отображается пример вывода после ввода символа в текстовом поле.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Мониторинг ключевых событий" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Рис. 22. Мониторинг ключевых событий  
:::image-end:::  

## <a name="profile"></a>профиль  

```console
profile([name])
```  

Запускает сеанс профилирование ЦП JavaScript с необязательным именем.  Метод [profileEnd()](#profileend) завершает профиль и отображает результаты в средстве **памяти.**  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите `profile()` метод, чтобы начать профилирование.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Запустите [метод profileEnd()](#profileend) для остановки профилирование и отображения результатов в **средстве памяти.**  

Профили также могут быть вложены.  В следующих примерах кода и рисунке результат один и тот же независимо от порядка.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Одновременно могут работать несколько профилей ЦП, и не требуется закрывать каждый из них в порядке создания.  

## <a name="profileend"></a>profileEnd  

```console
profileEnd([name])
```  

Завершает сеанс профилирование ЦП JavaScript и отображает результаты в **средстве памяти.**  Вы должны запускать [метод profile()](#profile) .  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите [метод profile()](#profile) для начала профилирование.  
1.  Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты в **средстве Памяти.**  
    
    ```console
    profileEnd("My profile")
    ```  

Профили также могут быть вложены.  В следующем примере кода и рисунке результат один и тот же независимо от порядка.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Результат отображается в качестве снимка куча в **средстве памяти.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Сгруппные профили" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Рис. 23. Сгруппные профили  
:::image-end:::  

> [!NOTE]
> Одновременно могут работать несколько профилей ЦП, и не требуется закрывать каждый из них в порядке создания.  

## <a name="queryobjects"></a>queryObjects  

```console
queryObjects(Constructor)
```  

Возвращаем массив объектов, созданных с указанным конструктором.  Областью является выбранный в настоящее время `queryObjects()` контекст времени запуска на консоли.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Возвращает все `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Возвращает все элементы HTML.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Возвращает все объекты, которые были мгновенно с помощью `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>таблица  

```console
table(data[, columns])
```  

Журналы данных объектов с форматированием таблиц на основе объекта данных с необязательными заголовками столбцов.  В следующем примере кода и рисунке отображается список имен с помощью таблицы на консоли.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Результат метода таблицы()" lightbox="../media/console-table-display.msft.png":::
   Рис. 24. Результат `table()` метода  
:::image-end:::  

## <a name="undebug"></a>undebug  

```console
undebug(method)
```  

Останавливает отладку указанного метода, чтобы при вызове метода отладка больше не вызывалась.  

```console
undebug(getData);
```  

## <a name="unmonitor"></a>unmonitor  

```console
unmonitor(method)
```  

Останавливает мониторинг указанного метода.  Этот метод используется в согласованном с [методом monitor()](#monitor) методе.  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a>unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Останавливает мониторинг событий для указанного объекта и событий.  Например, ниже останавливается весь мониторинг событий на объекте окна.  

```console
unmonitorEvents(window);
```  

Кроме того, можно выборочно прекратить мониторинг определенных событий на объекте.  Например, в следующем коде начинается мониторинг всех событий на выбранном в настоящее время элементе, а затем прекращается мониторинг событий \(возможно, для уменьшения шума в выходной `mouse` `mousemove` консоли\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a>значения  

```console
values(object)
```  

Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Ссылка на API консоли"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — ссылка на API консоли"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Приостановка кода с помощью точек breakpoints в Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Ускорение времени запуска JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Выпуск 1050237: отлаговка (функция) не работает | Monorail"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/utilities) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
