---
description: Начало работы с HTML и DOM
title: 'DevTools для начинающих: начало работы с HTML и DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools
ms.openlocfilehash: 6ca27b720a17928545712666e43495c4da2fb880
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397932"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools для начинающих: начало работы с HTML и DOM  

Это первый из серии учебников, которые обучат вас основам веб-разработки.  Узнайте о наборе средств веб-разработчика с именем Microsoft Edge DevTools, которые могут повысить производительность.  

В этом руководстве вы узнаете о HTML и DOM.  HTML — одна из основных технологий веб-разработки.  Это язык, который управляет структурой и контентом веб-страниц.  DoM также связан со структурой и контентом веб-страниц, подробнее об этом вы узнаете позже.  

## <a name="goals"></a>Цели  

Вы собираетесь изучить веб-разработку, фактически построив собственный веб-сайт.  К завершению всех учебников в серии **DevTools для** начинающих ваш готовый сайт может выглядеть следующим образом.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Готовый сайт" lightbox="../media/beginners-html-finished.msft.png":::
   Готовый сайт  
:::image-end:::  

К концу этого учебника вы должны понять следующие темы.  

*   Как HTML и DOM создают контент, отображаемый на веб-сайтах.  
*   Как Microsoft Edge DevTools может помочь вам поэкспериментировать с изменениями HTML и DOM.  
*   Разница между HTML и DOM.  

У вас также есть реальный веб-сайт.  Вы можете использовать сайт для хозяйского резюме или блога.  

## <a name="prerequisites"></a>Предварительные условия  

Перед попыткой этого руководства выполните следующие необходимые условия:  

*   Если вы не знакомы с HTML, [прочитайте начало работы с HTML.][MDNGettingStartedHtml]  
*   Скачайте [веб-браузер Microsoft Edge.][MicrosoftEdgeInsider]  В этом руководстве используется набор средств веб-разработки, называемых Microsoft Edge DevTools, встроенных в Microsoft Edge.  

## <a name="set-up-your-code"></a>Настройка кода  

Вы собираетесь создать свой сайт в редакторе кода в Интернете под названием Glitch.  

1.  Откройте [исходный код.][GlitchAlluringShockIndex]  Эта вкладка называется вкладка **редактора** во всем этом учебнике.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Вкладка редактора" lightbox="../media/beginners-html-setup1.msft.png":::
       Вкладка редактора  
    :::image-end:::  
    
1.  Выберите **завихрение-шок**.  Меню Параметры проекта открывается в левом верхнем углу.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Меню Параметры проекта" lightbox="../media/beginners-html-setup2.msft.png":::
       Меню Параметры проекта  
    :::image-end:::  
    
1.  Выберите **Проект Remix**.  Сбой создает копию проекта, которую можно изменить и случайным образом создать новое имя для проекта.  Контент такой же, как и раньше.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Ремиксируемый проект" lightbox="../media/beginners-html-setup3.msft.png":::
       Ремиксируемый проект  
    :::image-end:::  
    
1.  Если вы планируете завершить следующий учебник в **** этой серии, выберите вход и войдя в глюк с помощью учетной записи GitHub или Facebook.  Если вы решите не войти в свою учетную запись, вы потеряете возможность изменить проект после закрытия вкладки редактирования.  
1.  Выберите **Показать** и **выбрать в новом окне**.  Откроется новая вкладка, показывающая живую страницу.  Эта вкладка называется вкладка **live во** всем этом учебнике.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Вкладка live" lightbox="../media/beginners-html-setup4.msft.png":::
       Вкладка live  
    :::image-end:::  
    
## <a name="add-content"></a>Добавление контента  

Ваш сайт довольно пуст.  Следуйте ниже шагам, чтобы добавить в него содержимое.  

1.  На **вкладке редактора** `<!-- You're "About Me" will go here.  -->` замените `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Новый код выделен на вкладке редактора" lightbox="../media/beginners-html-add1.msft.png":::
             Новый код выделен на вкладке редактора  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Просмотр изменений на **вкладке в прямом эфире.**  Текст `About Me` отображается на странице.  Текст больше, чем окружающий текст, так как элемент `<h1>` представляет заголовки раздела.  Ваш веб-браузер автоматически стили заголовки в больших размерах шрифта.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Новая рубрика видна на вкладке live" lightbox="../media/beginners-html-add2.msft.png":::
       Новая рубрика видна на вкладке live  
    :::image-end:::  
    
1.  Назад в **вкладке редактор**, `<p>I am learning HTML.  Recent accomplishments:</p>` вставьте на строку ниже, где вы только что `<h1>About Me</h1>` положили .  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
              <body>
                  <p> Your site!</p>
                  <main>
                      <h1>About Me</h1>
                      <p>I am learning web development.  Recent accomplishments:</p>
                  </main>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Обновленный код выделен на вкладке редактора" lightbox="../media/beginners-html-add3.msft.png":::
             Обновленный код выделен на вкладке редактора  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Просмотр изменений в **вкладке в прямом эфире.**  
1.  Возвращаясь на **вкладку редактора,** добавьте список достижений:  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <p>I am learning web development.  Recent accomplishments:</p>
                  <ul>
                      <li>Learned how to set up my code in Glitch.</li>
                      <li>Added content to my HTML.</li>
                      <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                      <li>TODO: Learn the difference between HTML and the DOM.</li>
                  </ul>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Обновленный код также выделен на вкладке редактора" lightbox="../media/beginners-html-add4.msft.png":::
             Обновленный код также выделен на вкладке редактора  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Снова возвращайтесь на вкладку **в прямом эфире,** чтобы убедиться, что новое содержимое отображается правильно.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="Новый список отображается на вкладке live" lightbox="../media/beginners-html-add5.msft.png":::
       Новый список отображается на вкладке live  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Экспериментируйте с изменениями контента в Microsoft Edge DevTools  

Если вы разрабатывали большую страницу с большим количеством HTML, то несколько утомительным было бы несколько утомительным ходить между вкладкой редактора и вкладкой live сотни раз, чтобы отобразить изменения, особенно если вы не уверены, что именно нужно поместить на странице.  Microsoft Edge DevTools помогает вам экспериментировать с изменениями контента, не покидая **вкладку в прямом эфире.**  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Узнайте разницу между HTML и DOM  

Прежде чем приступить к редактированию контента из Microsoft Edge DevTools, необходимо понять разницу между HTML и DOM.  Лучший способ узнать это на примере:  

1.  Перейдите на **вкладку в прямом эфире.**  В нижней части страницы отображается `A new element!?!` текст.  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="В нижней части страницы текст Новый элемент!?! отображается" lightbox="../media/beginners-html-dom1.msft.png":::
       В нижней части страницы отображается `A new element!?!` текст  
    :::image-end:::  
    
1.  Вернуться на вкладку **редактора** и попытаться найти текст `index.html` в .  Текст не существует.  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Тайный текст Новый элемент!?! нигде не найти в index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       Текст тайны `A new element!?!` нигде не найти в `index.html`  
    :::image-end:::  
    
1.  Возвращайся к **вкладке в прямом эфире,** наведите курсор, откройте контекстное меню \(правой кнопкой `A new element!?!` мыши\) и выберите **Inspect**.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Проверка текста" lightbox="../media/beginners-html-dom3.msft.png":::
       Проверка текста  
    :::image-end:::  
    
    DevTools открывается рядом со своей страницей.  `<div>A new element!?!</div>` выделено синим цветом.  Хотя эта структура в DevTools выглядит как HTML, на самом деле это **дерево DOM.**  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools открыт рядом со страницей" lightbox="../media/beginners-html-dom4.msft.png":::
       DevTools открыт рядом со страницей  
    :::image-end:::  
    
При загрузке страницы браузер принимает HTML для создания *исходного* контента страницы.  DoM представляет *текущее* содержимое страницы, которое со временем может изменяться.  Загадочное `<div>A new element!?!</div>` содержимое добавляется на страницу из-за тега `<script src="new.js"></script>` в нижней части HTML.  Этот тег вызывает запуск кода JavaScript.  Дополнительные материалы о JavaScript можно узнать в более позднем руководстве, но пока думайте о нем как о языке программирования, который может изменить содержимое вашей страницы.  В этом конкретном случае код JavaScript `<div>A new element!?!</div>` добавляется на страницу.  Поэтому этот таинственный текст отображается на вашей странице в прямом эфире, но не в HTML.  

### <a name="edit-the-dom"></a>Изменение DOM  

Если вы хотите быстро поэкспериментировать с изменениями контента, не покидая вкладку в прямом эфире, попробуйте DevTools.  

1.  В DevTools наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `Your site!` **Изменить в качестве HTML.**  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Редактирование узла в формате HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Редактирование узла в формате HTML  
    :::image-end:::  
    
1.  Замените `<p>Your site!</p>` код ниже.  
    
    :::row:::
       :::column span="":::
          ```html
          ...
              ...
                  ...
                  <header>
                      <p><b>Welcome to my site!</b></p>
                      <button>Download my resume</button>
                  </header>
                  ...
              ...
          ...
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Обновление узла в формате HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Обновление узла в формате HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Выберите `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` или \(macOS\) для сохранения изменений или выберите вне окна.  Изменения автоматически показываются в режиме прямого просмотра страницы.  Текст `Your site!` был заменен новым контентом.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Новое содержимое сразу же появляется на странице" lightbox="../media/beginners-html-edit3.msft.png":::
       Новое содержимое сразу же появляется на странице  
    :::image-end:::  
    
Этот рабочий процесс хорош только для экспериментов с изменениями контента.  Если вы обновите страницу или закройте вкладку, ваши изменения будут потеряны навсегда.  Если вы используете этот рабочий процесс и хотите сохранить изменения, необходимо вручную скопировать эти изменения в HTML.  В следующих нескольких разделах покажут еще несколько способов изменения контента из дерева DOM.  

## <a name="reorder-nodes"></a>Узлы реордера  

Вы также можете изменить порядок узлов DOM.  Например, на веб-странице меню навигации находится в нижней части.  Чтобы переместить его в верхнюю часть:  

1.  Найдите `<nav>` узел в **dom Tree** of DevTools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Узел nav выделен синим цветом в DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       Узел nav выделен синим цветом в DevTools  
    :::image-end:::  
    
1.  Перетащите узел в верхнюю часть, чтобы узел был первым `<nav>` ребенком `<body>` узла.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Перетаскивание узла nav в верхнюю часть" lightbox="../media/beginners-html-reorder2.msft.png":::
             Перетаскивание узла nav в верхнюю часть  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Узел `<nav>` отображается в верхней части страницы.  
          
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Узел nav находится в верхней части страницы" lightbox="../media/beginners-html-reorder3.msft.png":::
             Узел nav находится в верхней части страницы  
          :::image-end:::  
       :::column-end:::
   :::row-end:::  
    
### <a name="delete-a-node"></a>Удаление узла  

Кроме того, можно удалить узлы из дерева DOM.  

1.  В **дереве DOM выберите** `<div>A new element!?!</div>` .  DevTools выделяет синий узел.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Выберите удаленный узел" lightbox="../media/beginners-html-delete1.msft.png":::
       Выберите удаленный узел  
    :::image-end:::  
    
1.  Выберите `Delete` клавишу на клавиатуре.  Узел `<div>A new element!?!</div>` удаляется из дерева DOM.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Узел удален" lightbox="../media/beginners-html-delete2.msft.png":::
       Узел удален  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Копирование изменений  

Вы почти закончили.  Вы сделали несколько изменений на своей странице в DevTools, но они еще не сохранены в исходный код.  

1.  Обновление **вкладки в прямом эфире.**  Изменения, внесенные в dom Tree, исчезают.  В частности, текст возвращается в верхнюю часть страницы, а текст `Your site!` `A new element!?!` возвращается в нижнюю часть.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Внесенные изменения исчезли" lightbox="../media/beginners-html-copy1.msft.png":::
       Внесенные изменения исчезли  
    :::image-end:::  
    
1.  Скопируйте код ниже.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
    
1.  Возвращайся на **вкладку редактора** и замените содержимое файла `index.html` кодом, который вы только что скопировали.  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Как должен выглядеть index.html-файл" lightbox="../media/beginners-html-copy2.msft.png":::
       Внешний вид `index.html` файла  
    :::image-end:::  
    
## <a name="next-steps"></a>Дальнейшие действия  

*   Выполните следующий учебник в этой серии , Начало работы с [CSS][DevToolsBeginnersCss], чтобы узнать, как стиль вашей страницы и экспериментировать с изменениями стиля в Microsoft Edge DevTools.  
*   Ознакомьтесь [с введением в DOM,][MDNIntroductionDom] чтобы узнать больше о DOM.  
*   Ознакомьтесь с курсом ["Введение в веб-разработку",][CourseraIntroductionToWebDevelopment] чтобы получить дополнительные практические веб-разработки.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools для начинающих: начало работы с CSS | Документы Майкрософт"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Введение в веб-разработку | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html — | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML-| MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в dom | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и является автором [Кэтрин][KatherineJackson] Джексон \(Технический стажер писатель, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
