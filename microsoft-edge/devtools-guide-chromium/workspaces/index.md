---
description: Узнайте, как сохранить изменения, внесенные в DevTools на диск.
title: Редактирование файлов с помощью рабочей области
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 17f9ced15dbacd62c9ffe40e4af889925a8155fb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399248"
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

# <a name="edit-files-with-workspaces"></a>Редактирование файлов с помощью рабочей области  

> [!NOTE]
> Цель этого руководства состоит в предоставлении практической практики по настройке и использованию workspaces, чтобы вы могли использовать workspaces в собственных проектах.  Вы можете сохранить изменения в исходный код на локальном компьютере, внесенные в DevTools после того, как вы включаете workspaces.  

> [!IMPORTANT]
> **Необходимые условия.** Перед началом этого руководства необходимо знать, как выполнять следующие действия.  
> 
> *   [Использование html, CSS и JavaScript для создания веб-страницы][MDNWebGettingStarted]  
> *   [Использование DevTools для внесения основных изменений в CSS][DevToolsCssIndex]  
> *   [Запуск локального веб-сервера HTTP][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a>Обзор  

Рабочее пространство позволяет сохранить изменение, которое вы делаете в Devtools, на локализованную копию того же файла на компьютере.  В этом руководстве на компьютере должны быть следующие параметры.  

*   У вас есть исходный код для сайта на рабочем столе.  
*   Вы работаете на локальном веб-сервере из каталога исходных кодов, чтобы сайт был доступен по `localhost:8080` .  
*   Вы открылись в Microsoft Edge и используете DevTools для изменения `localhost:8080` CSS сайта.  

С включенной рабочей областью изменения CSS, внесенные в DevTools, сохраняются в исходный код на рабочем столе.  

## <a name="limitations"></a>Ограничения  

Если вы используете современную структуру, она, вероятно, преобразует исходный код из формата, который легко поддерживать, в формат, оптимизированный для максимально быстрого запуска.  

Workspaces обычно может с помощью исходных карт составить оптимизированный код обратно в [исходный код.][TreehouseBlogSourceMaps]  Но существует много различий между фреймворками в том, как каждая из них использует исходные карты.  Devtools просто поддерживает все варианты.  

Известно, что рабочей области не работают со следующими рамками.  

*   Создание приложения React  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a>Связанная функция: локальные переопределения  

**Локальные переопределения** — это еще одна функция DevTools, аналогичная рабочей области.  Используйте локальные переопределения, когда вы хотите экспериментировать с изменениями на веб-странице, и вам необходимо отображать изменения на веб-странице нагрузки, но вам не важно сопоставление изменений в исходный код веб-страницы.  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a>Шаг 1. Настройка  

Выполните следующие действия, чтобы получить практический опыт работы с workspaces.  

### <a name="set-up-the-demo"></a>Настройка демонстрации  

1.  [Откройте демо.][GlitchWorkspacesDemo]  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Проект Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Проект Glitch  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Создание `app` каталога на рабочем столе.  Сохранение копий файлов из `workspaces-demo` каталога в `app` каталог.  В остальной части учебника каталог называется `~/Desktop/app` .  
1.  Запустите локальный веб-сервер `~/Desktop/app` в .  Ниже приведен пример кода для `SimpleHTTPServer` запуска, но вы можете использовать любой сервер, который вы предпочитаете.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Откройте вкладку в Microsoft Edge и перейдите к локальной версии сайта.  Вы должны иметь доступ к нему с помощью URL-адреса, как `localhost:8080` или `http://0.0.0.0:8080` .  Точный [номер порта может][WikiPortURLs] быть другим.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Демонстрация" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       Демонстрация  
    :::image-end:::  
    
### <a name="set-up-devtools"></a>Настройка DevTools  

1.  Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\) **** для открытия консоли панели DevTools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Панель Консоли" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       Панель **Консоли**  
    :::image-end:::  
    
1.  Выберите средство **Sources.**  
1.  Выберите панель **Filesystem.**  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Панель Filesystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       Панель **Filesystem**  
    :::image-end:::  
    
1.  Выберите **добавить папку в рабочее пространство.**  
1.  Введите `~/Desktop/app`.  
1.  Выберите **Разрешить** предоставить DevTools разрешение на чтение и записи в каталог.  
    В панели **Filesystem** теперь есть зеленая точка рядом `index.html` с , и `script.js` `styles.css` .  Эти зеленые точки означают, что DevTools установил сопоставление между сетевыми ресурсами страницы и файлами в `~/Desktop/app` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="На панели Filesystem теперь показано сопоставление между локальными и сетевыми файлами" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       На **панели Filesystem** теперь показано сопоставление между локальными и сетевыми файлами  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a>Шаг 2. Сохранение изменения CSS на диск  

1.  Откройте `styles.css` .  
    
    > [!NOTE]
    > Свойство `color` `h1` элементов установлено `fuchsia` для .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Просмотр styles.css в текстовом редакторе" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Просмотр `styles.css` в текстовом редакторе  
    :::image-end:::  
    
1.  Выберите **средство Elements.**  
1.  Измените значение `color` свойства элемента на `<h1>` ваш любимый цвет.  
    Помните, что для отображения правил CSS, примененных к ней в области Стилей, необходимо выбрать `<h1>` элемент **dom Tree.** ****  Зеленая точка рядом с означает, что любое изменение, которое вы `styles.css:1` делаете, соо- `~/Desktop/app/styles.css`  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Зеленый индикатор, связанный с файлом" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       Зеленый индикатор, связанный с файлом  
    :::image-end:::  
    
1.  Откройте `styles.css` в текстовом редакторе снова.  Свойство `color` теперь настроено на ваш любимый цвет.  
1.  Обновите страницу.  Цвет элемента `<h1>` по-прежнему за набором вашего любимого цвета.  Изменение остается через обновление, так как при внося изменения DevTools сохранил изменение на диск.  Затем при обновлении страницы локальный сервер обслуживал измененную копию файла с диска.  
    
## <a name="step-3-save-an-html-change-to-disk"></a>Шаг 3. Сохранение HTML-изменения на диске  

### <a name="change-html-from-the-elements-panel"></a>Изменение HTML-кодов из панели Elements  

Вы можете внести изменения в html из панели элементов, но изменения дерева DOM не сохраняются на диске и влияют только на текущую сессию браузера.  

Дерево DOM не html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-panel"></a>Изменение HTML-кодов с панели Источники  

Если вы хотите сохранить изменение html страницы, сделайте это с помощью **панели Источники.**  

1.  Выберите средство **Sources.**  
1.  Выберите **панель Page.**  
1.  Выберите **(индекс).**  Открывается HTML-код страницы.  
1.  Замените `<h1>Workspaces Demo</h1>` `<h1>I ❤️  Cake</h1>` .  Просмотрите следующую цифру.  
1.  Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения изменений.  
1.  Обновите страницу.  Элемент `<h1>` по-прежнему отображает новый текст.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Изменение HTML-кодов с панели Источники" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Изменение HTML-кодов с **панели Источники**  
    :::image-end:::  
    
1.  Откройте `~/Desktop/app/index.html` .  Элемент `<h1>` содержит новый текст.  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a>Шаг 4. Сохранение изменения JavaScript на диск  

Панель **Источники** также является местом для внесения изменений в JavaScript.  Но иногда вам необходимо получить доступ к другим панелям, например к средству **Elements** или панели **консоли,** при внесении изменений на ваш сайт.  Существует способ открыть панель **Источников** вместе с другими панелями.  

1.  Выберите **средство Elements.**  
1.  Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\).  Откроется **командное** меню.  
1.  `QS`Введите, а затем выберите показать быстрый **источник**.  В нижней части окна DevTools теперь имеется панель **быстрого** источника.  Панель отображает содержимое последнего файла, отредактируемого в `index.html` панели **Источники.**  Панель **Быстрого источника** предоставляет редактор из панели **Источники,** чтобы вы могли редактировать файлы при открытых других панелях.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Откройте панель быстрого источника с помощью командного меню" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Откройте панель **быстрого источника** с помощью **командного меню**  
    :::image-end:::  
    
1.  Чтобы `Control` + `P` открыть диалоговое окно Open File, выберите \(Windows, Linux\) или `Command` + `P` \(macOS\). ****  Просмотрите следующую цифру.  
1.  `script`Введите, а затем выберите **app/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Откройте script.js диалоговое окно Open File" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Откройте `script.js` диалоговое окно **Open File**  
    :::image-end:::  
    
    > [!NOTE]
    > Ссылка `Save Changes To Disk With Workspaces` в демо регулярно стилизуется.  
    
1.  Добавьте следующий код в нижнюю часть **script.js** панели **быстрого** источника.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Выберите `Control` + `S` \(Windows, Linux\) `Command` + `S` или \(macOS\) для сохранения изменений.  
1.  Обновите страницу.  
    
    > [!NOTE]
    > Ссылка на странице теперь является italicized.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Ссылка на странице теперь является итальяно-" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       Ссылка на странице теперь является итальяно-  
    :::image-end:::  
    
## <a name="next-steps"></a>Дальнейшие действия  

Используйте то, что вы узнали в этом руководстве, чтобы настроить workspaces в собственном проекте.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Демо-файлы workspaces | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Содержимое - CSS: каскадные листы стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с веб-| MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Запуск простого локального http-сервера | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в DOM - веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Введение в исходные | Блог Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(компьютерная сеть\) — Википедия"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
