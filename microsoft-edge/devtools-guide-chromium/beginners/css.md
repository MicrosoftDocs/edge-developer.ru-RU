---
description: Начало работы с CSS
title: 'DevTools для начинающих: начало работы с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools
ms.openlocfilehash: 6a7135e144123917535e7c43e6a3cd608ec0c8a7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439439"
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

# <a name="devtools-for-beginners-get-started-with-css"></a>DevTools для начинающих: начало работы с CSS  

В этом руководстве вы узнаете, как использовать CSS для стиля веб-страницы.  Вы также узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.  

Следующая статья — это второй учебник из серии учебников, который учит вас основам веб-разработки и Microsoft Edge DevTools.  Вы получаете практический опыт, фактически построив собственный веб-сайт.  Вам не нужно завершить первый учебник, прежде чем следовать второму.  [Настройка кода показывает,](#set-up-your-code) как настроиться.  

> [!NOTE]
> Этот учебник предназначен для абсолютных новичков **** и посвящен основам веб-разработки и основам использования DevTools для экспериментов с CSS.  Если вы хотите учебник, который фокусируется только на DevTools, перейдите к началу просмотра и [изменения CSS][DevtoolsCssIndex].  

В начале учебника ваш сайт должен выглядеть следующим образом.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Как выглядит ваш сайт в настоящее время" lightbox="../media/beginners-css-intro1.msft.png":::
   Как выглядит ваш сайт в настоящее время  
:::image-end:::  

После завершения руководства сайт должен выглядеть следующим образом.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Как должен выглядеть ваш сайт в конце учебника" lightbox="../media/beginners-css-intro2.msft.png":::
   Как должен выглядеть ваш сайт в конце учебника  
:::image-end:::  

## <a name="goals"></a>Цели  

Следуйте этому учебнику, чтобы лучше понять следующие понятия и задачи.  

*   Использование CSS для стиля веб-страницы.  
*   Использование Microsoft Edge DevTools для экспериментов с CSS.  
*   Разница между CSS и CSS frameworks.  

Вы строите реальный веб-сайт.  

## <a name="prerequisites"></a>Предварительные условия  

Перед попыткой этого руководства выполните следующие необходимые условия.  

*   Полное начало работы с HTML и [DOM][DevtoolsBeginnersHtml] или убедитесь, что у вас есть понимание HTML и DOM аналогично тому, что преподается в этом учебнике.  
*   Скачайте [веб-браузер Microsoft Edge.][MicrosoftEdgeInsider]  В следующем руководстве используется набор средств веб-разработки, называемых Microsoft Edge DevTools, встроенных в Microsoft Edge.  

## <a name="set-up-your-code"></a>Настройка кода  

Чтобы создать свой сайт, сначала необходимо выполнить следующие действия, чтобы настроить код.  

> [!NOTE]
> Если вы уже завершили первый учебник в этой серии, переехав в следующий раздел.  Продолжить использование кода из последнего учебника, [начало работы с HTML и DOM][DevtoolsBeginnersHtml].  

1.  Откройте [исходный код.][GlitchCookedAmphibianIndex]  Вкладка в фокусе браузера ссылается на вкладку **редактирования.**  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Вкладка редактирования" lightbox="../media/beginners-css-setup1.msft.png":::
       Вкладка **редактирования**  
    :::image-end:::  
    
1.  Выберите **вареную амфибию.**  Всплывающее меню.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Меню Параметры проекта" lightbox="../media/beginners-css-setup2.msft.png":::
       Меню Параметры проекта  
    :::image-end:::  

1.  Выберите **Проект Remix**.  Сбой создает копию проекта, которую можно изменить.  
    
    > [!NOTE]
    > Сбой создает случайное имя для нового проекта.  
    
1.  Выберите **Показать** и **выбрать в новом окне**.  Откроется еще одна вкладка с живым представлением сайта.  Вкладка в фокусе браузера ссылается на вкладку **live.**  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Вкладка live" lightbox="../media/beginners-css-setup3.msft.png":::
       Вкладка **live**  
    :::image-end:::  

## <a name="understand-css"></a>Понимание CSS  

**CSS** — это компьютерный язык, который определяет макет и стиль веб-страниц.  Следующая фигура — абзац с границей.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Текст стилизовылся с помощью CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Текст стилизовылся с помощью CSS  
:::image-end:::  

Следующий фрагмент кода — код HTML и CSS, используемый для создания абзаца на предыдущем рисунке.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` вероятно, выглядит новым для вас.  Остальные должны выглядеть знакомыми.  Если нет, выполните начало работы с HTML и [DOM,][DevtoolsBeginnersHtml] прежде чем пытаться выполнить следующие разделы.  

## <a name="add-inline-styles"></a>Добавление встройных стилей  

Выполните следующие действия, чтобы использовать стили **для** применения стилей к одному элементу.  

1.  Вернуться на вкладку редактирования и открыть `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Откройте `index.html` на вкладке редактирования  
    :::image-end:::  
    
1.  Добавьте `style="background-color: aliceblue;"` к вашему `<nav>` .  В блоке кода ниже четвертая строка кода — это строка, которая должна измениться.  Остальное только там, поэтому вы можете убедиться, что вы ставите новый код в нужном месте.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Чтобы отобразить изменения, перейдите на **вкладку live.**  Фон раздела `<nav>` теперь синий.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="Фоновый цвет ссылок дома и контактов теперь синий" lightbox="../media/beginners-css-inline2.msft.png":::
       Фоновый цвет ссылок **дома** и **контактов** теперь синий  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a>Повторное использование стилей на одной странице с внутренними таблицами стилей  

В предыдущем фрагменте кода вложенный стиль применял стиль к одному `<p>` тегу.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Что делать, если вы хотите, чтобы все элементы на вашей веб-странице были одинаково `<p>` стили.  Код необходимо скопировать и вклеить в каждый `<p>` тег на вашем сайте.  Это много времени и усилий.  И, если вам нужно сделать изменение, вам придется изменить каждый тег снова.  Выполните следующие действия, чтобы использовать **таблицу внутренних** стилей для записи CSS один раз, чтобы она применяла к нескольким элементам.  

1.  На вкладке в прямом эфире **выберите Контакт,** чтобы перейти на контактную страницу.  Обратите внимание на шрифт **Дома и** **Контакта.**  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Страница Контакт" lightbox="../media/beginners-css-internal1.msft.png":::
       Страница Контакт  
    :::image-end:::  
    
1.  На **вкладке редактор откройте** `contact.html` .  
1.  Добавьте следующий код в `contact.html` .  Помните, что строки, начиная с и `<style>` `</style>` заканчивая, это то, что нужно добавить.  Другой код только там, чтобы вы знали, куда поместить новый код.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Возвращайся к **вкладке live.**  
1.  Выберите **Контакт,** чтобы вернуться на контактную страницу.  Изменен шрифт **Дома и** **Контакта.**  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="Изменен шрифт ссылок дома и контактов" lightbox="../media/beginners-css-internal2.msft.png":::
       Изменен шрифт ссылок **дома** и **контактов**  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a>Понимание внутренних таблиц стилей  

Внутренние таблицы стилей применяют стили с помощью **селекторов.**  Селекторы — это шаблоны, которые могут применяться к одному или более элементам HTML.  Предыдущий фрагмент кода добавил следующий стиль.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` является селектором, который переводится как "любой `<li>` элемент, содержащий `<a>` элемент".  Браузер меняет шрифт ссылок **"Дома"** и **"Контакт",** так как каждая из групп тегов соответствует шаблону.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` является **объявлением**.  Объявление состоит из следующих двух частей.  

:::row:::
   :::column span="1":::
      **свойство**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      Свойство описывает общий способ изменения стиля элемента.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      В значении описывается, как именно должен меняться стиль элемента.  
   :::column-end:::
:::row-end:::  

Например, `font-family: 'Courier New', Courier, serif` дает браузеру следующую инструкцию: "Установите шрифт элементов, которые соответствуют `li a` шаблону `'Courier New'` .  Если этот шрифт не доступен, используйте `Courier` .  Если это не доступно, используйте `serif` ."  

### <a name="add-multiple-selectors-to-a-ruleset"></a>Добавление нескольких селекторов в правило  

Блок кода CSS, как и следующий фрагмент кода, называется **правилом.**  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Выполните следующие действия, чтобы использовать запятые для добавления нескольких селекторов в список правил.  

1.  На **вкладке редактор откройте** `contact.html` .  
1.  После `li a` введите `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    Предыдущий фрагмент кода сообщает браузеру о стиле элементов так же, как он стили `<h1>` элементов, которые соответствуют шаблону `li a` .  
    
1.  Перейдите на **вкладку в прямом эфире.**  
1.  Выберите **контактную** ссылку, чтобы вернуться на контактную страницу.  Теперь **свяжитесь со мной!** имеет тот же шрифт, что и ссылки на навигацию.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Текст Свяжитесь со мной!  теперь имеет тот же шрифт, что и ссылки Home и Contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       Текст **Свяжитесь со мной!** теперь имеет тот же шрифт, что и **ссылки Home** и **Contact**  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a>Эксперимент с DevTools  

По мере того как вы продолжите свое путешествие, чтобы стать экспертом в веб-разработке, вы можете обнаружить, что CSS является сложной.  Вы можете написать некоторые CSS и ожидать его отображения в одну сторону, но браузер делает что-то совершенно другое.  Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно отображает влияние изменений на страницу.  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a>Добавление объявления к существующему правилу в DevTools  

Выполните следующие действия, чтобы итерировать стиль существующего элемента, добавьте объявление в существующий список правил.  

1.  Наведите курсор на **ссылку Главная,** откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Проверка домашней ссылки" lightbox="../media/beginners-css-add1.msft.png":::
       Проверка домашней ссылки  
    :::image-end:::  
    
    DevTools открывается рядом со своей страницей.  Код, который представляет ссылку Главная, выделен синим `<a href="/">Home</a>` цветом в дереве DOM.  Фрагмент кода и предварительный просмотр должны быть знакомы в [get Started с HTML и DOM.][DevtoolsBeginnersHtml]  
    
    :::row:::
       :::column span="":::
          На следующем рисунке объявление, к которое вы ранее добавили, отображается на вкладке `font-family: 'Courier New', Courier, serif` `contact.html` **Стили** ниже дерева DOM.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="Вкладка Стили находится ниже дерева DOM" lightbox="../media/beginners-css-add2.msft.png":::
             Вкладка **Стили** находится ниже дерева DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Если окно DevTools широкое, вкладка Styles находится справа от дерева DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Вкладка Styles находится справа от дерева DOM" lightbox="../media/beginners-css-add3.msft.png":::
             Вкладка **Styles** находится справа от дерева DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Выберите пустую строку `font-family: 'Courier New', Courier, Serif` ниже, чтобы добавить новое объявление.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Добавление нового объявления" lightbox="../media/beginners-css-add4.msft.png":::
       Добавление нового объявления  
    :::image-end:::  
    
1.  Введите `color` и выберите `Enter` .  Пользовательский интерфейс автокомплекта предлагает варианты при введите.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Цвет типа" lightbox="../media/beginners-css-add5.msft.png":::
       Тип `color`  
    :::image-end:::  
    
1.  Введите `magenta` и выберите `Enter` .  Весь текст на странице контакта теперь пурпурный.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Тип magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Тип `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a>Изменение объявления в DevTools  

Выполните следующие действия по редактированию существующих деклараций в DevTools.  

1.  Выберите квадрат magenta рядом `magenta` с .  Всплывет подбиратель цветов.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Выбор цвета" lightbox="../media/beginners-css-edit1.msft.png":::
       Выбор цвета  
    :::image-end:::  
    
1.  Используйте выборщик цвета, чтобы изменить текст шрифта на цвет, который вам нравится.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Измените цвет шрифта на фиолетовый с помощью цвета Picker" lightbox="../media/beginners-css-edit2.msft.png":::
       Измените цвет шрифта на фиолетовый с помощью цвета Picker  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a>Добавление нового правила в DevTools  

Выполните следующие действия, чтобы добавить новые правила в DevTools.  

1.  Выберите **новое правило** стиля \( Новое правило стиля ![ ](../media/new-style-rule-icon.msft.png) \), которое находится рядом с **.cls**.  Пустой регламент отображается в `a` качестве селектора.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Добавление нового правила" lightbox="../media/beginners-css-rule1.msft.png":::
       Добавление нового правила  
    :::image-end:::  
    
1.  Замените `a` `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Замените a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Замените `a` на `a:hover`  
    :::image-end:::  
    
    `:hover` является **псевдоклассом.**  Используйте псевдо-классы для элементов стиля, которые могут вводить особые состояния.  Например, стиль вступает в силу только при наведении над `a:hover` `<a>` элементом.  
    
1.  Выберите между скобками, чтобы добавить новое объявление.  
1.  Введите `background-color` имя объявления и выберите `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Тип фонового цвета" lightbox="../media/beginners-css-rule3.msft.png":::
       Тип `background-color`  
    :::image-end:::  
    
1.  Введите `green` значение объявления и выберите `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Введите зеленый цвет" lightbox="../media/beginners-css-rule4.msft.png":::
       Тип `green`  
    :::image-end:::  
    
1.  Наведите курсор мыши по **ссылке Главная.**  Фон ссылки становится зеленым.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Наведите курсор на ссылку Главная, чтобы показать ее зеленый фон" lightbox="../media/beginners-css-rule5.msft.png":::
       Наведите курсор на ссылку Главная, чтобы показать ее зеленый фон  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a>Повторное использование стилей на страницах с внешними таблицами стилей  

На предыдущем этапе в таблицу внутренних стилей добавлен следующий фрагмент `contact.html` кода.  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

Что делать, если вы хотите стиль `index.html` таким же образом?  Что делать, если у вас есть большое количество страниц, на которые вы хотите применить стили?  Необходимо скопировать и вклеить таблицу внутренних стилей на каждую веб-страницу на вашем сайте.  Выполните следующие действия, чтобы добавить таблицу **внешних** стилей, чтобы позволить вам написать CSS один раз и применить его к нескольким страницам.  

1.  Сначала обновите вкладку в прямом эфире, чтобы удалить изменения, внесенные в DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" После обновления страницы изменения, внесенные в DevTools, исчезли" lightbox="../media/beginners-css-external1.msft.png":::
        После обновления страницы изменения, внесенные в DevTools, исчезли  
    :::image-end:::  
    
1.  Возвращайся на **вкладку редактора и** открывай `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Удаление всего `<style>` между и , в том числе и `</style>` `<style>` `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="Тег стиля удален" lightbox="../media/beginners-css-external3.msft.png":::
       Тег стиля удален  
    :::image-end:::  
    
1.  Откройте `index.html` и `style="background-color: aliceblue;"` удалите из `<nav>` тега.  Теперь вы удалили все CSS, которые вы ранее добавили на свой сайт.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Стиль inline был удален из элемента nav" lightbox="../media/beginners-css-external4.msft.png":::
       Стиль inline был удален из элемента nav  
    :::image-end:::  
    
1.  Выберите **новый файл**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Новый диалоговое окно файла" lightbox="../media/beginners-css-external5.msft.png":::
       Новый диалоговое окно файла  
    :::image-end:::  
    
1.  Замените `cool-file.js` и выберите Add `style.css` **File**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Тип style.css" lightbox="../media/beginners-css-external6.msft.png":::
       Тип `style.css`  
    :::image-end:::  
    
1.  Добавьте в файл следующий фрагмент `style.css` кода.  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Добавление кода в style.css" lightbox="../media/beginners-css-external7.msft.png":::
       Добавление кода в `style.css`  
    :::image-end:::  
    
    Убедитесь, что вы создали таблицу внешних стилей. Ваш HTML не знает, что он существует.  
    
1.  Откройте `index.html` .  
1.  Добавьте `<link rel="stylesheet" href="style.css">` в HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Ссылка на style.css" lightbox="../media/beginners-css-external8.msft.png":::
       Ссылка на `style.css`  
    :::image-end:::  
    
1.  Откройте файл `contact.html` и добавьте ссылку.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Ссылка на style.css в contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Ссылка на `style.css` в `contact.html`  
    :::image-end:::  
    
1.  Перейдите на **вкладку в прямом эфире.**  На домашней странице теперь есть тот же шрифт из последнего раздела и синий раздел навигации.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Главная страница" lightbox="../media/beginners-css-external10.msft.png":::
       Главная страница  
    :::image-end:::  
    
1.  Выберите **контактную** ссылку, чтобы перейти на контактную страницу.  Контактная страница имеет тот же формат, что и домашняя страница.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Страница контактов" lightbox="../media/beginners-css-external11.msft.png":::
       Страница контактов  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a>Использование CSS-фреймворка  

**CSS frameworks —** это коллекции стилей, построенных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.  Вместо того, чтобы самостоятельно определять стили, рамки предоставляют вам коллекцию стилей, которые можно использовать на элементах страницы.  

1.  Скопируйте следующий код:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Откройте вкладку редактирования и вклеите код в `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Ссылка на рамки в contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Ссылка на фреймворк в `contact.html`  
    :::image-end:::  
    
1.  Откройте файл `index.html` и добавьте код.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Ссылка на рамки в index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Ссылка на фреймворк в `index.html`  
    :::image-end:::  
    
1.  Возвращайся на вкладку в прямом эфире, чтобы просмотреть изменения.  Несмотря на то, что фоновый цвет элемента и шрифта и элементов одинаковы, шрифт других элементов `<nav>` `<li>` `<a>` изменился.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Некоторые шрифты на домашней странице изменились из-за рамок" lightbox="../media/beginners-css-framework3.msft.png":::
       Некоторые шрифты на домашней странице изменились из-за рамок  
    :::image-end:::  
    
### <a name="use-a-class"></a>Использование класса  

В последнем разделе вы добавили Bootstrap на свои веб-страницы, которые изменили шрифты некоторых элементов на вашем сайте.  CSS-фреймворки помогают вносить существенные изменения на страницу с очень небольшим кодом.  Выполните следующие действия по изменению загона.  

1.  Скопируйте следующий фрагмент кода.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Добавьте предыдущий фрагмент кода в тег `<header>` `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Добавление классов в index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Добавление классов в `index.html`  
    :::image-end:::  
    
1.  Добавьте код в тег `<header>` `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Добавление классов в contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Добавление классов в `contact.html`  
    :::image-end:::  
    
1.  Просмотр изменений на вкладке в прямом эфире.  Вокруг загона есть большая серая коробка.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="В загоне теперь есть большой серый поле вокруг него" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       В загоне теперь есть большой серый поле вокруг него  
    :::image-end:::  
    
### <a name="understand-classes"></a>Понимание классов  

Классы могут назначать коллекции стилей произвольным элементам.  Используйте следующий фрагмент кода, чтобы применить несколько стилей к элементу после того, как `<header>` задаете `class` атрибут `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Одним из преимуществ класса является то, что он позволяет применять стили к любым элементам, которые вы хотите.  Например, предположим, что необходимо установить фоновый цвет некоторых элементов на фиолетовый, но `<p>` не все `<p>` элементы.  Чтобы определить стиль в классе, используйте следующий фрагмент кода.  

```css
.custom-background {
  background-color: purple;
}
```  

Далее применим класс только `<p>` к элементам, которые необходимо в стиле.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a>Выравнивание элементов  

Выполните следующие действия, чтобы выполнить загрузку и предоставить классы для выравнивания элементов.  

1.  Возвращайся на вкладку редактора и открывай `index.html` .  
1.  Добавьте `class="container-fluid"` в `<body>` тег.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Добавление класса контейнерной жидкости" lightbox="../media/beginners-css-align1.msft.png":::
       Добавление `container-fluid` класса  
    :::image-end:::  
    
1.  Wrap your `<nav>` and `<main>` elements in `<div class="row">` .  Чтобы правильно закрыть новый тег, убедитесь, что нужно поставить `</div>` `</main>` после.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Добавление строки" lightbox="../media/beginners-css-align2.msft.png":::
       Добавление строки  
    :::image-end:::  
    
1.  Добавьте `class="col-3"` в тег и в `<nav>` `class="col-9"` `<main>` тег.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Добавление классов col-3 и col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Добавление `col-3` классов `col-9` и классов  
    :::image-end:::  
    
1.  Просмотр изменений на вкладке в прямом эфире.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Содержимое nav теперь находится слева от основного контента" lightbox="../media/beginners-css-align4.msft.png":::
       Содержимое nav теперь находится слева от основного контента  
    :::image-end:::  
    
## <a name="next-steps"></a>Дальнейшие действия  

Поздравляем, вы закончили.  

*   Лучший способ улучшить веб-разработку — создать больше сайтов.  Не беспокойтесь о взломе вещей.  Просто повеселиться и узнать как можно больше по пути.  
*   Чтобы узнать больше о стиле веб-страниц, перейдите к [вводу в CSS][MDNCssFirstSteps].  
*   Чтобы узнать больше о том, как использовать DevTools для экспериментов с CSS страницы, перейдите к началу просмотра и изменения [CSS][DevtoolsCssIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools для начинающих: начало работы с HTML и doM | Документы Майкрософт"  
[DevtoolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html — приготовленные амфибии | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и является автором [Кэтрин][KatherineJackson] Джексон \(Технический стажер писатель, Chrome DevTools\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
