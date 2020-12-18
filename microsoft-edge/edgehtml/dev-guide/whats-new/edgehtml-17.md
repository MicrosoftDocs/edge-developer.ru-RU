---
title: Новые функции и API в EdgeHTML 17
description: В этом руководстве представлен обзор функций и стандартов разработчика, включенных в EdgeHTML 17.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, css, javascript, разработчик
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 75429528fd814963a8c78e27f85564223fb2d3c8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235273"
---
# Новые возможности EdgeHTML 17  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Вот список новых и обновленных функций веб-платформы [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30) в составе обновления Windows 10 за апрель [2018](https://blogs.windows.com/windowsexperience/2018/04/27) г. \(04/2018, сборка 17134\).  Изменения в конкретных сборках [Windows Insider](https://insider.windows.com) Preview см. в записях microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) и [What's New in EdgeHTML.](../whats-new.md)  

Ниже приводится permalink для следующего списка изменений: [https://aka.ms/devguide_edgehtml_17](./edgehtml-17.md) .  

## Новые и обновленные функции  

### Роли, состояния и события ARIA 1.1  

EdgeHTML 17 добавляет поддержку различных ролей, состояния и свойств из спецификации [WAI-ARIA 1.1,](https://w3.org/TR/wai-aria-1.1)включая веб-канал, [](https://www.w3.org/TR/wai-aria-1.1#feed) [форму,](https://www.w3.org/TR/wai-aria-1.1#form) [aria-haspopup,](https://w3.org/TR/wai-aria-1.1#aria-haspopup) [aria-placeholder](https://w3.org/TR/wai-aria-1.1#aria-placeholder)и многие другие; найти полный [список обновлений ARIA в списке изменений.](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299)  В этом обновлении EdgeHTML 17 теперь поддерживает все роли и атрибуты, определенные в WAI-ARIA 1.1.  <!--  Check out the [Accessibility](../../accessibility.md) docs for more information about accessibility in Microsoft Edge.  -->  

### Маскировка CSS  

EdgeHTML 17 включает экспериментальную поддержку [маскировки CSS.](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking)  Частичная реализация представляет свойства маски CSS [и](https://developer.mozilla.org/docs/Web/CSS/mask-image) [размера маски.](https://developer.mozilla.org/docs/Web/CSS/mask-size)  Проверьте флаг "Включить маскировку CSS" в about:flags для экспериментов!  

### Преобразования CSS для элементов SVG  

EdgeHTML 17 теперь поддерживает преобразования CSS для элементов SVG и атрибутов презентации.  Это позволяет визуально управлять элементами SVG, включая поворот, масштабирование, перемещение, переключение или перевод.  

### Расширения  

Microsoft Edge теперь поддерживает [API](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) уведомлений, который отображает уведомления из расширений.  Разработчики расширений теперь могут создавать различные типы уведомлений \(базовые, списки, изображения и так далее\), которые поддерживают полное взаимодействие с пользователем.  Уведомления также автоматически регистрируются в центре уведомлений.  Посетите пример [уведомлений о](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) том, как использовать этот API в расширении.  

EdgeHTML 17 теперь также поддерживает метод как часть стандартного `Tabs.reload()` класса API вкладок.  Кроме того, в обновлении Windows 10 за апрель 2018 г. пользователи могут разрешить запуск расширений во время просмотра inPrivate.  

Дополнительные сведения об обновлениях расширений в этом выпуске можно найти в записи блога "Новые возможности для расширений" в обновлении Windows 10 за апрель [2018 г.](https://blogs.windows.com/msedgedev/2018/05/24)  

### DevTools  

Этот выпуск DevTools включает два способа: как традиционные средства в браузере \( \) для Microsoft Edge и предварительный просмотр в качестве автономного приложения `F12` [для Windows 10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) из Microsoft Store!  

:::image type="complex" source="../../devtools-protocol/media/microsoft-edge-devtools.png" alt-text="Приложение Microsoft Edge DevTools" lightbox="../../devtools-protocol/media/microsoft-edge-devtools.png":::
   Приложение Microsoft Edge DevTools  
:::image-end:::  

Эти средства также были обновлены с помощью ряда основных функций, включая базовую поддержку удаленной отладки [\(через](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) наш новый протокол [DevTools](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)\), функции отладки [PWA,](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging)управление кэшом [IndexedDB,](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection)вертикальную док-станцию и т. д. [](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) Мы также продолжали общие усилия по [рефакторингу,](./edgehtml-16.md) запущенные в последнем выпуске в рамках текущих инвестиций в производительность и надежность.  

Дополнительные сведения см. на сайте DevTools в последнем обновлении [Windows 10 (EdgeHTML 17).](../../devtools-guide/whats-new/edgehtml-17.md)  

### JavaScript  

С помощью EdgeHTML 17 обработчик JavaScript для Chakra вносит улучшения в производительность в ряде ключевых областей:  

:::row:::
   :::column span="1":::
      **Более емкий объем памяти**  
   :::column-end:::
   :::column span="2":::
      *   \(Re-\)defer parsing for [arrow functions](https://github.com/Microsoft/ChakraCore/pull/4105) and methods on [object literals](https://github.com/Microsoft/ChakraCore/pull/4136)  
      *   [Рефакторинг RegExp bytecode](https://github.com/Microsoft/ChakraCore/pull/3915)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Более быстрые встроенные javaScript**
   :::column-end:::
   :::column span="2":::
      *   [Общий доступ к типам для Object.create](https://github.com/Microsoft/ChakraCore/pull/3901)  
      *   [Многоморфный inline кэш для Object.assign](https://github.com/Microsoft/ChakraCore/pull/3792)  
      *   [Оптимизация JSON.parse/stringify](https://github.com/Microsoft/ChakraCore/pull/4077)  
      *   [Переописывание итераторов массива в JavaScript и более быстрое для... of](https://github.com/Microsoft/ChakraCore/pull/4095)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Веб-сборка**
   :::column-end:::
   :::column span="2":::
      *   [Поддержка влиять](https://github.com/Microsoft/ChakraCore/pull/3681)  
   :::column-end:::
:::row-end:::  

Подробнее об этом: улучшенная производительность JavaScript и [WebAssembly в EdgeHTML 17.](https://blogs.windows.com/msedgedev/2018/06/19)  

### Элемент мультимедиа

EdgeHTML 17 включает обновления [HTMLMediaElement,](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) в том числе:  

*   Новый атрибут `preload` в [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) элементе указывает, какие данные должны быть предварительно загружены.
*   Добавление метода и [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) свойства позволяет разработчикам выбрать устройство для вывода [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) звука.  
    
    > [!NOTE]
    > В RTC эта информация пока недоступна.  
    
### API захвата мультимедиа  

Microsoft Edge теперь поддерживает запись экрана в RTC с помощью [API захвата мультимедиа.](https://w3c.github.io/mediacapture-screen-share)  Эта функция позволяет веб-страницам захватывать выходные данные отображаемого устройства пользователя, которое обычно используется для трансляции рабочего стола для виртуальных собраний или презентаций без подключаемых модульов.  

### Прогрессивные веб-приложения  

Начиная с EdgeHTML 17, рабочие службы и push-уведомления включены по умолчанию [](https://blogs.windows.com/msedgedev/2017/12/19)\(подробнее об этих функций см. в записи блога".  Это завершает набор технологий \(включая сеть Fetch и API Push и кэша\), который лежит в технической основе для прогрессивного web Apps \(PWAs\) в Windows 10.  

PWAs — это просто [](https://en.wikipedia.org/wiki/Progressive_enhancement) веб-приложения, которые постепенно улучшаются с помощью нативных функций, подобных приложениям, на вспомогательных платформах и браузерных движках, таких как установка и запуск домашнего экрана, поддержка в автономном режиме и push-уведомления.  В Windows 10 с обдвижком Microsoft Edge \(EdgeHTML\) pwAs пользуются дополнительным преимуществом работы независимо от окна браузера в качестве приложений универсальной [платформы Windows.](/windows/uwp/get-started/whats-a-uwp)  

Помимо PWAS, службы и API кэша позволяют разработчикам перехватывать сетевые запросы и отвечать из кэша.  Веб-сайт даже не должен быть полноценным веб-приложением, чтобы воспользоваться преимуществами кэша рабочих служб для точной загрузки и надежности страницы, а также для обеспечения автономной работы в периоды без подключения к Интернету или неудовлетворительного качества.  

Дополнительные сведения о рабочих службах и сведения о PWAS в [Windows](../../progressive-web-apps/index.md) 10 можно найти в наших последовательных веб-приложениях для Windows.  

### Веб-безопасность  

EdgeHTML 17 представляет поддержку целостности подресурса \(SRI\).  [Целостность подресурса](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) — это функция безопасности, которая позволяет браузерам проверять, доставляются ли извлеченные ресурсы (например, изображения, сценарии, шрифты и так далее) без непредвиденных манипуляций.  

Добавьте атрибут, содержащий криптографическое представление ресурса, который вы ожидаете загрузить на веб-странице, к элементу или элементу, как по примеру `integrity` `<script>` `<link>` ниже.  Затем Microsoft Edge сравнивает запрашиваемую ресурс с параметром hash, определенным в `integrity` атрибуте.  Если они не совпадают, Microsoft Edge не будет выполнять ресурс и возвращает в сеть ошибку.  

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```  

Кроме того, в EdgeHTML 17 новый заголок запроса [Upgrade-Insecure-Requests](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) позволяет браузерам запрашивать безопасный просмотр.  Этот загоер сообщает серверу, что браузер поддерживает обновление незащищенных запросов, и пользователь должен быть перенаправлен на безопасную версию сайта, если он доступен.  

### Переменные шрифты
В EdgeHTML 17 доступна полная поддержка переменных шрифтов (включая параметры вариантов шрифтов [CSS](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) и [шрифт-оптическое](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)изменение размеров).)  Переменные шрифты позволяют разработчикам добиться внешнего вида разных шрифтов с помощью одного шрифта, настраивая различные оси, уменьшая потребность в нескольких файлах шрифтов и снижая производительность.  

Присоединяйтесь [к нам, чтобы узнать,](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts)какие переменные шрифты предоставляют веб-разработчики и дизайнеры, а также как использовать их на своем сайте.  Кроме того, в записи блога вы можете узнать больше о переменных шрифтах, привнося в [Microsoft Edge экспресс-шрифты с переменными шрифтами.](https://blogs.windows.com/msedgedev/2018/03/13)  

<iframe height='456' scrolling='no' title='Примеры билетов переменной "Переменные"' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. примеры <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> билета переменной пера </a> msEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> </a> @MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>  

## Новые API в EdgeHTML 17  

Ниже полный список новых API в EdgeHTML 17.  Они перечислены в формате `[interface name].[api name]` .  

> [!NOTE] 
> Несмотря на то что в модели DOM есть следующие API, все еще возможно, что некоторые из них находятся в разработке.  Официальное слово о поддержке функций можно найти в статусе платформы [Microsoft Edge.](https://developer.microsoft.com/microsoft-edge/platform/status)  

<iframe height='580' scrolling='no' title='Новые API в EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>См. API-код для новых перьев в <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> EdgeHTML 17 от </a> MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> </a> CodePen.</iframe>  

> [!TIP]
> Мы сотрудничаем с другими браузерами и веб-сообществом, внедряя веб-документы [MDN](https://developer.mozilla.org) в качестве точного места для полезной, непредвзятой документации, не зависит от браузера, для текущих и новых веб-технологий на основе стандартов. [](https://blogs.windows.com/msedgedev/2017/10/18)  Подробные сведения о поддержке API EdgeHTML можно найти непосредственно на каждой странице библиотеки [веб-ссылок MDN.](https://developer.mozilla.org/docs/Web)  Последние функции, [](https://developer.microsoft.com/microsoft-edge/status) поддерживаемые в Microsoft Edge, можно получить в статусе платформы Microsoft Edge.  

## Предыдущие выпуски EdgeHTML  

[EdgeHTML 13 / Сборка Windows 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)  

[EdgeHTML 14 / Сборка Windows 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)  

[EdgeHTML 15 / Сборка Windows 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)  

[EdgeHTML 16 / Сборка Windows 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)  
