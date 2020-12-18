---
description: Отображение и редактирование файлов, создание фрагментов кода, отладка JavaScript и настройка рабочих пространств в панели источников Microsoft Edge DevTools.
title: Обзор панели источников
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: b90f927670146c004a335256ace28203219442eb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235272"
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

# Обзор панели источников  

Используйте панель источников Microsoft **** Edge DevTools для выполнения следующих действий.  

*   [Отображение файлов.](#display-files)  
*   [Редактирование CSS и JavaScript.](#edit-css-and-javascript)  
*   [Создайте и **сохраните фрагменты** Кода JavaScript,](#create-save-and-run-snippets)которые можно запустить на любой веб-странице.  **Фрагменты кода похожи** на закладки.  
*   [Отлаговка JavaScript](#debug-javascript).  
*   [Настройка рабочей области, чтобы](#set-up-a-workspace)изменения, внесенные в DevTools, были сохранены в код в файловой системе.  
    
## Отображение файлов  

Используйте **страницу** для отображения всех ресурсов, загруженных страницей.

:::image type="complex" source="../media/sources-page-pane.msft.png" alt-text="The Page pane" lightbox="../media/sources-page-pane.msft.png":::
   The **Page** pane  
:::image-end:::  

Как **организована** страница:  
*   Верхний уровень, как на `top` предыдущем рисунке, представляет [HTML-кадр.][W3CHtml4Frames]  Найдите `top` на каждой странице, которую вы посещаете.  `top` представляет основной кадр документа.  
*   Второй уровень, как на предыдущем `docs.microsoft.com` рисунке, представляет [собой источник.][HtmlstandardOrigin]  
*   Третий уровень, четвертый уровень и так далее представляют каталоги и ресурсы, загруженные из этого источника.  Например, на предыдущем рисунке полный путь к `devtools-guide-chromium` ресурсу: `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
Выберите файл в **области** страниц, чтобы отобразить содержимое в области **редактора.**  Вы можете отобразить любой тип файла.  Для изображений отображается предварительный просмотр изображения.  

:::image type="complex" source="../media/sources-editor-pane.msft.png" alt-text="Отображение содержимого a4d10f71.index-docs.js в области редактора" lightbox="../media/sources-editor-pane.msft.png":::
   Отображение содержимого в `a4d10f71.index-docs.js` области **редактора**  
:::image-end:::  

## Редактирование CSS и JavaScript  

С помощью **области редактора** можно редактировать CSS и JavaScript.  DevTools обновляет страницу для запуска нового кода.  Например, если изменить CSS-файл, добавив правило стиля ниже:

```css
.metadata.page-metadata {
    color: red;
}
```

Это изменение вступает в силу немедленно.

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Измените CSS в области редактора, чтобы изменить цвет текста субтитра на красный" lightbox="../media/edit-css.msft.png":::
   Измените CSS в **области** редактора, чтобы изменить цвет текста субтитра на красный  
:::image-end:::  

Изменения CSS вступает в силу немедленно, сохранение не требуется.  Чтобы изменения JavaScript вступили в силу, выберите `Control` + `S` \(Windows, Linux\) или `Command` + `S` \(macOS\).  DevTools не выполняет скрипт повторно, поэтому единственными изменениями JavaScript, которые вступает в силу, являются изменения, внесенные в функции.  Например, на следующем рисунке обратите внимание, что это не `console.log('A')` `console.log('B')` так.  Если DevTools повторно запускает весь сценарий после вставки изменения, то текст был бы зарегистрирован в `A` консоли. ****  

:::image type="complex" source="../media/edit-js.msft.png" alt-text="Редактирование JavaScript в области редактора" lightbox="../media/edit-js.msft.png":::
   Редактирование JavaScript в **области редактора**  
:::image-end:::  

DevTools стирает изменения CSS и JavaScript при перезагрузке страницы.  Перейдите [в папку "Настройка рабочей области",](#set-up-a-workspace) чтобы узнать, как сохранить изменения в файловой системе.  

## Создание, сохранение и запуск фрагментов кода  

Фрагменты кода — это сценарии, которые можно запускать на любой странице.  Предположим, что вы многократно вводите следующий код в **консоли,** чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли.**  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Вместо этого вы можете сохранить **** этот код в фрагменте кода и запустить его с помощью нескольких нажатий кнопки в любое время.  DevTools сохраняет **фрагмент** в файловой системе.  

:::image type="complex" source="../media/snippet.msft.png" alt-text="Фрагмент кода, который вставляет библиотеку jQuery на страницу" lightbox="../media/snippet.msft.png":::
   Фрагмент **кода,** который вставляет библиотеку jQuery на страницу  
:::image-end:::  

Чтобы запустить **фрагмент:**

*   Откройте файл с помощью области **фрагментов** кода и выберите **"Выполнить"** \( ![ Кнопка "Выполнить" ][ImageRunIcon] \).  
*   Откройте меню [команд,][DevtoolsGuideChromiumCommandMenuIndex]удалите символ, введите , введите имя фрагмента кода, а `>` `!` затем выберите **** `Enter` .  
    
Чтобы узнать [больше,][DevtoolsGuideChromiumJavascriptSnippets] перейдите к фрагментам кода на любой странице.

## Отлаговка JavaScript  

Вместо того чтобы использовать для того, чтобы выявить, где происходит ошибка JavaScript, рассмотрите возможность использования средств отладки `console.log()` Microsoft Edge DevTools.  Общая идея состоит в том, чтобы установить точку останова, которая является преднамеренным местом остановки в коде, а затем пошаговая пошаговая часть времени работы кода по одной строке за раз.  Пошаговая пошаговая часть кода может отображать и изменять значения всех текущих свойств **** и переменных, запускать JavaScript в консоли и многого другое.

Перейдите [к началу отладки JavaScript,][DevtoolsGuideChromiumJavascriptIndex] чтобы изучить основы отладки в DevTools.

:::image type="complex" source="../media/debugging.msft.png" alt-text="Отлаговка JavaScript" lightbox="../media/debugging.msft.png":::
   Отлаговка JavaScript  
:::image-end:::  

## Настройка рабочей области  

По умолчанию при редактировании файла в средстве **"Источники"** эти изменения теряются при перезагрузке страницы.  **Workspaces** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.  По сути, DevTools можно использовать в качестве редактора кода.

Перейдите [к редактированию файлов с помощью workspaces,][DevtoolsGuideChromiumWorkspacesIndex] чтобы начать работу.

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ../command-menu/index.md "Запуск команд с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Начало отладки JavaScript в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Запуск фрагментов Кода JavaScript на любой странице с Помощью Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Редактирование файлов с помощью workspaces | Документы Майкрософт"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origin | HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Frames | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/sources) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
