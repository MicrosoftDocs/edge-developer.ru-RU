---
description: Узнайте обо всех способах приостановки кода в Microsoft Edge DevTools.
title: Приостановка кода с помощью точек остановок в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 84077503d6c786244fc2ca4d54c349ae9f6d20d8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398597"
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

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a>Приостановка кода с помощью точек остановок в Microsoft Edge DevTools  

Для приостановки кода JavaScript используйте точки breakpoints.  В этом руководстве рассказывается о каждом типе точки разрыва, доступной в DevTools, а также о том, когда и как настроить каждый тип.  Для практических уроков процесса отладки перейдите к началу отладки JavaScript в [Microsoft Edge DevTools][DevtoolsJavascriptIndex].  

## <a name="overview-of-when-to-use-each-breakpoint-type"></a>Обзор того, когда использовать каждый тип точки разрыва  

Наиболее известным типом точки разрыва является строка кода.  Но точки взлома строки кода могут быть неэффективными для набора, особенно если вы не знаете точно, где искать, или если вы работаете с большой базой кода.  Вы можете сэкономить время при отладки, зная, как и когда использовать другие типы точек разрыва.  

| Тип breakpoint | Используйте это, когда вы хотите сделать паузу...  |  
|:--- |:--- |  
| [Line-of-code](#line-of-code-breakpoints) | На точном регионе кода.  |  
| [Условная строка кода](#conditional-line-of-code-breakpoints) | В точном регионе кода, но только в том случае, если верно другое условие.  |  
| [DOM](#dom-change-breakpoints) | В коде, который изменяет или удаляет определенный узел DOM или детей.  |  
| [XHR](#xhrfetch-breakpoints) | Когда URL-адрес XHR содержит шаблон строки.  |  
| [Слушатель событий](#event-listener-breakpoints) | На коде, который выполняется после события, `click` например, выполняется.  |  
| [Исключение](#exception-breakpoints) | На строке кода, который бросает пойманный или необученный исключение.  |  
| [Функция](#function-breakpoints) | При запуске определенной команды, функции или метода.  |  

## <a name="line-of-code-breakpoints"></a>Точки разлома строки кода  

Используйте точку разрыва кода, когда вы знаете точный регион кода, который необходимо исследовать.  DevTools всегда останавливается перед запуском этой строки кода.  

Чтобы установить точку разрыва кода в DevTools:  

1.  Выберите средство **Sources.**  
1.  Откройте файл, содержащий строку кода, на которой необходимо разорвать.  
1.  Перейдите по строке кода.  
1.  Слева от строки кода находится столбец номеров строки.  Выберите его.  Рядом со столбцом номеров строки отображается красный значок.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Точка взлома строки кода" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Точка взлома строки кода  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a>Точки разлома строк кода в коде  

Запустите `debugger` метод из кода, чтобы остановиться на этой строке.  Это эквивалентно [точке](#line-of-code-breakpoints)разрыва кода, за исключением того, что точка разрыва заданной в коде, а не в пользовательском интерфейсе DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a>Условные точки взлома строки кода  

Используйте условную точку разлома строки кода, если вы знаете точный регион кода, который необходимо исследовать, но вы хотите остановиться только тогда, когда верно другое условие.  

Чтобы установить условную точку разлома строки кода:  

1.  Выберите средство **Sources.**  
1.  Откройте файл, содержащий строку кода, на которой необходимо разорвать.  
1.  Перейдите по строке кода.  
1.  Слева от строки кода находится столбец номеров строки.  Наведите курсор на номер строки и откройте контекстное меню \(правой кнопкой мыши\).  
1.  Выберите **добавить условную точку разрыва**.  Диалоговое окно отображается под строкой кода.  
1.  Введите свое состояние в диалоговом ок.  
1.  Выберите, `Enter` чтобы активировать точку разрыва.  Значок рядом со столбцом номеров строки.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Точка разрыва условной строки кода" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Точка разрыва условной строки кода  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a>Управление точками разрыва кода  

Используйте области **Breakpoints** для отключения или удаления точек разрывов строк кода из одного расположения.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Панель Breakpoints" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Панель **Breakpoints**  
:::image-end:::  

*   Проверьте контрольный ящик рядом с записью, чтобы отключить точку разрыва.  
*   Наведите курсор на запись и откройте контекстное меню \(правой кнопкой мыши\), чтобы удалить точку разрыва.  
*   Наведите курсор в любом месте области **breakpoints** и откройте контекстное меню \(правой кнопкой мыши\), чтобы отключить все точки разрыва, отключить все точки разрыва или удалить все точки разрыва.  Отключение всех точек разрыва эквивалентно отключаемой каждой из них.  Отключение всех точек взлома предписывает DevTools игнорировать все точки разрыва кода, но также поддерживать состояние включенного, чтобы каждый из них был в том же состоянии, что и раньше при повторной активности каждой из них.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Отключенные точки разрыва в области Breakpoints" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Отключенные точки разрыва в области **Breakpoints**  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a>Точки breakpoints изменения DOM  

Используйте точку размыкать doM, если необходимо приостановить использование кода, который изменяет узел DOM или детей.  

Чтобы установить точку breakpoint изменения DOM:  

1.  Выберите **средство Elements.**  
1.  Перейдите к элементу, на котором необходимо установить точку разрыва.  
1.  Наведите курсор на элемент и откройте контекстное меню \(правой кнопкой мыши\).  
1.  Наведите курсор на **break on,** а затем выберите **изменения Subtree,** **изменения**атрибута или **удаление узлов.**  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Контекстное меню для создания точки разрыва изменения DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Контекстное меню для создания точки разрыва изменения DOM  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a>Типы точки breakpoints изменения DOM  

*   **Изменения subtree**.  Вызывается при удалении или добавлении ребенка выбранного узла или изменения содержимого ребенка.  Не срабатывает при изменениях атрибута узла ребенка или о каких-либо изменениях в выбранном в настоящее время узле.  
*   **Изменения атрибутов:** срабатывает при добавлении или удалении атрибута на выбранном в настоящее время узле или при изменении значения атрибута.  
*   **Удаление узлов:** срабатывает при удалении выбранного в настоящее время узла.  
    
## <a name="xhrfetch-breakpoints"></a>XHR/Fetch breakpoints  

Если URL-адрес запроса XHR содержит указанную строку, используйте точку разрыва XHR.  DevTools останавливается на строке кода, где метод выполняется `send()` XHR.  

> [!NOTE]
> Эта функция также работает с [запросами на извлечение API.][MDNFetchApi]  

Один из примеров, когда это полезно, это когда веб-сайт запрашивает неправильный URL-адрес, и вы хотите быстро найти исходный код AJAX или Fetch, который вызывает неправильный запрос.  

Чтобы установить точку разрыва XHR:  

1.  Выберите средство **Sources.**  
1.  **Расширь панель точки разлома XHR.**  
1.  Выберите **точку "Добавить точку разлома".**  
1.  Введите строку, которую необходимо разорвать.  DevTools останавливается, когда эта строка присутствует где-либо в URL-адресе запроса XHR.  
1.  Выберите `Enter` подтверждение.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Создание точки разрыва XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Создание точки разрыва XHR  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a>Breakpoints слушателя событий  

Используйте точки breakpoints слушателя событий, когда необходимо сделать паузу в коде слушателя событий, который запускается после того, как событие будет уволено.  Вы можете выбрать определенные события, такие как события или категории событий, например `click` все события мыши.  

1.  Выберите средство **Sources.**  
1.  Расширение панели **breakpoints слушателя** событий.  В DevTools показан список категорий событий, таких как **Анимация.**  
1.  Проверьте одну из этих категорий, чтобы приостановить любое событие из этой категории или расширить эту категорию и проверить определенное событие.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Создание точки разгона слушателя событий" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Создание точки разгона слушателя событий  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a>Точки разлома исключений  

Используйте точки разлома исключений, если необходимо приостановить на строке кода, бросаемом пойманный или незасвеченный исключение.  

1.  Выберите средство **Sources.**  
1.  Выберите **Пауза для исключений** \. ![ Пауза для ][ImagePauseOnExceptionsIcon] исключений \).  Значок поимеет при включении.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Кнопка "Пауза на исключениях"" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Кнопка **"Пауза на исключениях"**  
    :::image-end:::  
    
1.  **Необязательный**.  Проверьте **почтовый ящик Pause On Caught Exceptions,** если вы также хотите остановиться на пойманных исключениях, а также на незавербовавке.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Пауза на необученном исключении" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Пауза на необученном исключении  
    :::image-end:::  
    
## <a name="function-breakpoints"></a>Точки breakpoints функции  

Запустите метод, где находится команда, функция или метод, который необходимо отлаговать, когда необходимо приостановить при запуске `debug(method)` `method` определенной функции.  Вы можете вставить в код (например, заявление) или запустить метод из `debug()` `console.log()` консоли DevTools.  `debug()` эквивалентно установке [точки разрыва](#line-of-code-breakpoints) кода на первой строке функции.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a>Убедитесь, что целевая функция находится в области  

DevTools бросает, если функция отладки не `ReferenceError` находится в области.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Обеспечение целевой функции в области является сложной, если вы работаете метод `debug()` из консоли DevTools.  Вот одна стратегия:  

1.  Установите [точку разлома строки кода где-нибудь,](#line-of-code-breakpoints) где функция находится в области.
1.  Срабатывает точка разрыва.  
1.  Запустите `debug()` метод в консоли DevTools, пока код остается приостановленным на точке разрыва кода.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Начало работы с отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Извлечение API | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
