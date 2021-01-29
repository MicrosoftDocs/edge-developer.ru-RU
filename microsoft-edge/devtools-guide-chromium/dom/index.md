---
description: Просмотр узлов, поиск узлов, изменение узлов, ссылка на узлы в консоли, разрыв изменений узлов и т. д.
title: Начало работы с просмотром и изменением DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5b12b984aed7e35ce11dd45e8bc33f5d5fd454f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231106"
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

# Начало работы с просмотром и изменением DOM  

Выполните эти интерактивные учебники, чтобы изучить основы просмотра и изменения DOM страницы с помощью Microsoft Edge DevTools.  

В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.  Перейдите [к приложению: HTML и DOM для](#appendix-html-versus-the-dom) пояснения.  

## Открытые примеры DOM  

1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.  
    
    [Примеры DOM][GlitchDomExamples]  
    
## Просмотр узлов DOM  

Дерево DOM панели элементов — это место, в котором вы можете делать все действия, связанные с DOM, в DevTools.  

### Проверка узла  

Если вас интересует определенный узел DOM, **проверьте** это быстрый способ открыть DevTools и изучить этот узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Проверка узла"** правой стороной выберите **"Майклангело" и** выберите **"Проверить".**  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Проверка узла  
    :::image-end:::  
    
    1.  Откроется **панель элементов** DevTools.  `<li>Michelangelo</li>` выделен в дереве **DOM.**  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла Майкланголо" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Выделение `Michelangelo` узла  
        :::image-end:::  
        
        1.  Щелкните **значок "Проверить"** в левом верхнем углу ![ ][ImageInspectIcon] DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок Проверка" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Значок **"Проверка"**  
            :::image-end:::  
            
1.  В **области "Проверка узла"** щелкните **текст в Токио.**  Теперь `<li>Tokyo</li>` он выделен в дереве DOM.  

Проверка узла также является первым шагом к просмотру и изменению стилей узла.  Перейдите [к началу работы с просмотром и изменением CSS.][DevToolsCssGetStarted]  

### Навигация по дереву DOM с помощью клавиатуры  

Выбрав узел в дереве DOM, можно перейти к дереву DOM с помощью клавиатуры.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Navigate the DOM Tree with a Keyboard,** right-choose **Ringo** and choose **Inspect**.  `<li>Ringo</li>` выбран в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Проверка `Ringo` узла  
    :::image-end:::  
    
    1.  Нажмите `Up` клавишу со стрелкой 2 раза.  `<ul>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Проверка `ul` узла  
        :::image-end:::  
        
    1.  Нажмите `Left` клавишу со стрелкой.  Список `<ul>` свернут.  
    1.  Нажмите `Left` клавишу со стрелкой еще раз.  Выбран родительский узел `<ul>` узла.  В этом случае это с `<div>` `navigate-the-dom-tree-with-a-keyboard-1` ИД.  
    1.  Нажмите `Down` клавишу со стрелкой 2 раза, чтобы повторно выбрать свернутый `<ul>` список.  Это должно выглядеть следующим образом. `<ul>... </ul>`  
    1.  Нажмите `Right` клавишу со стрелкой.  Список расширяется.  

### Прокрутка в представление  

При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в настоящее время не находится в окле просмотра.  Например, предположим, что вы прокручивали страницу вниз и вас интересует узел в `<h1>` верхней части страницы.  **Прокрутка в представлении** позволяет быстро изменить расположение окна, чтобы можно было просмотреть узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.  
1.  Прокрутите страницу DOM Examples до конца.  
1.  Узел `<li>Magritte</li>` по-прежнему должен быть выбран в дереве DOM.  Если нет, перейти к [прокрутке в представлении и](#scroll-into-view) начать все сначала.  
1.  Наведите курсор на узел, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите `<li>Magritte</li>` пункт **"Прокрутка в представление".**  В окну просмотра можно просмотреть узел **Magritte.**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если вы не можете просмотреть параметр **"Прокрутка в** представлении".
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка в представление" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Прокрутка в представление**  
    :::image-end:::  

### Поиск узлов  

Вы можете искать в дереве DOM по строке, селектору CSS или селектору XPath.  

1.  На панели элементов выделите **курсор.**  
1.  Выберите `Control` + `F` \(Windows, Linux\) или `Command` + `F` \(macOS\).  В нижней части дерева DOM откроется строка поиска.  
1.  Введите `The Moon is a Harsh Mistress`.  Последнее предложение выделено в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса на панели поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Выделение запроса на панели поиска  
    :::image-end:::  
    
Как упоминалось выше, на панели поиска также поддерживаются селекторы CSS и XPath.  

## Изменение DOM  

Вы можете изменить DOM во время и просмотреть, как изменения влияют на страницу.  

### Редактирование содержимого  

Чтобы изменить содержимое узла, дважды щелкните содержимое дерева DOM.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Изменение содержимого"** выберите **" Michelle" (Изменить** содержимое) и выберите **"Inspect" (Проверить).**  
    1.  В дереве DOM дважды щелкните `Michelle` .  Другими словами, дважды щелкните текст между `<li>` и `</li>` .  Текст выделен, чтобы указать, что он выбран.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Редактирование текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Редактирование текста  
        :::image-end:::  
        
    1.  Delete `Michelle` , type , then select to confirm the `Leela` `Enter` change.  Текст в DOM изменяется с **Michelle** на **Leela**.  

### Изменение атрибутов  

Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.  Следуйте инструкциям, чтобы узнать, как добавить атрибуты в узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Изменить атрибуты"** выберите "Химки" и выберите **"Проверить".** ****  
1.  Дважды `<li>` щелкните .  Текст выделен, чтобы указать, что узел выбран.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Изменение узла  
    :::image-end:::  
    
1.  Нажмите `Right` клавишу со стрелкой, добавьте пробел, введите `style="background-color:gold"` и выберите `Enter` .  Цвет фона узла изменяется на gold.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля в узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Добавление `style` атрибута в узел  
    :::image-end:::  
    
### Изменение типа узла  

Чтобы изменить тип узла, дважды щелкните тип и введите новый тип.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Изменить тип узла"** выберите правой правой выберите **"Инсайт"** и выберите **"Проверить".**  
    1.  Дважды `<li>` щелкните .  Текст `li` выделен.  
    1.  Delete `li` , type , then select `button` `Enter` .  Узел `<li>` изменяется на `<button>` узел.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Измените тип узла на `button`  
        :::image-end:::  
        
### Переусортовка узлов DOM  

Перетащите узлы, чтобы переусортовить их.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Reorder DOM Nodes" (Узлы DOM reorder)** выберите **"Elvis Presley" (Elvis Presley)** и выберите **"Inspect"**(Проверить).  
    
    > [!NOTE]
    > Это последний элемент в списке.  
    
    1.  В дереве DOM перетащите `<li>Elvis Presley</li>` его в верхнюю часть списка.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Перетащите узел в верхнюю часть списка  
        :::image-end:::  
        
### Состояние принудительного применения  

Вы можете заставить узлы оставаться в состояниях, включая `:active` , , , , и `:hover` `:focus` `:visited` `:focus-within` .  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **состоянии Force**наведите курсор на **"Химя".**  Цвет фона становится оранжевым.  
    1.  Right-choose **The The Of the Овне** и choose **Inspect**.  
    1.  Щелкните правой `<li class="demo--hover">The Lord of the Flies</li>` кнопкой мыши и выберите **force State**  >  **:hover**.  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  Цвет фона остается оранжевым, даже если вы на самом деле не наведите курсор на узел.  

### Скрытие узла  

Выберите, `H` чтобы скрыть узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Скрыть узел"** выберите пункт "Звездочки" **и** выберите пункт **"Проверить".**  
    1.  Нажмите `H` клавишу.  Узел скрыт.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Внешний вид узла в дереве DOM после его скрытия" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Внешний вид узла в дереве DOM после его скрытия  
        :::image-end:::  
        
    1.  Снова нажмите `H` клавишу.  Узел снова отображается.  

### Удаление узла  

Выберите, `Delete` чтобы удалить узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.  
    1.  Нажмите `Delete` клавишу.  Узел удаляется.  
    1.  Выберите `Control` + `Z` \(Windows, Linux\) или `Command` + `Z` \(macOS\).  Последнее действие отменено, и узел снова появляется.  

## Доступ к узлам в консоли  

DevTools предоставляет несколько ярлыков для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждый из них.  

### Ссылка на текущий выбранный узел с помощью $0  

При проверке узла текст рядом с узлом означает, что вы можете ссылаться на этот узел в консоли `== $0` с `$0` переменной.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Reference the currently-selected node with $0**, right-choose **The Left Hand ofЯs** and choose **Inspect**.  
    1.  Нажмите `Escape` клавишу, чтобы открыть консольный ящик.  
    1.  Введите `$0` и нажмите `Enter` клавишу.  Результат выражения показывает, что `$0` он оценивается как `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Результат первого выражения `$0` в **** консоли  
        :::image-end:::  
        
    1.  Наведите курсор на результат.  Узел выделен в окле просмотра.  
    1.  Щелкните дерево DOM, введите в консоли еще `<li>Dune</li>` `$0` раз, а затем выберите `Enter` еще раз.  Теперь `$0` оценивается как `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Результат второго выражения `$0` в **** консоли  
        :::image-end:::  
        
### Сохранить как глобальную переменную  

Если требуется много раз сослаться на узел, храните его как глобальную переменную.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Store as global variable**, right-choose The Big **Sleep** and choose **Inspect**.  
    1.  Щелкните правой `<li>The Big Sleep</li>` кнопкой мыши дерево DOM и выберите **"Магазин" в качестве глобальной переменной.**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  
    1.  Введите `temp1` в консоли и выберите `Enter` .  Результат выражения показывает, что переменная оценивается в узле.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Результат выражения `temp1`  
        :::image-end:::  
        
### Копирование пути JS  

Скопируйте путь JavaScript к узлу, если вам нужно со ссылкой на него в автоматическом тесте.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **области "Копировать путь JS"** выберите правой копией **"Иван Иванов"** и выберите **"Проверить".**  
    1.  Щелкните правой кнопкой мыши в дереве DOM и выберите `<li>The Brothers Karamazov</li>` **"Копировать**путь  >  **JS копирования".**  Выражение, `document.querySelector()` разрешаемого в узел, было скопировано в буфер обмена.  
    1.  Выберите `Control` + `V` \(Windows, Linux\) или `Command` + `V` \(macOS\) для вставки выражения в консоль.  
    1.  Выберите, `Enter` чтобы оценить выражение.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения Путь копирования JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Результат выражения **"Путь копирования JS"**  
        :::image-end:::  
        
## Приостановка изменений DOM  

DevTools позволяет приостановить JavaScript страницы, когда JavaScript изменяет DOM.  

### Приорвать изменение атрибута  

Используйте точки останова изменения атрибутов, если необходимо приостановить JavaScript, что приводит к изменению любого атрибута узла.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Break on attribute modifications,** right-choose **Sauerkraut** and choose **Inspect**.  
    1.  В дереве DOM щелкните правой кнопкой мыши и выберите `<li id="target">Sauerkraut</li>` "Приорвать ****  >  **при изменении атрибута".**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Приорвать изменение атрибута" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Приорвать изменение атрибута**  
        :::image-end:::  
        
    1.  На следующем этапе вам будет выдано указание нажать кнопку, которая приостановит код страницы.  После приостановки страницы вы больше не сможете прокручивать страницу.  Необходимо выбрать **сценарий возобновления** \( Resume Script \), чтобы снова сделать страницу ![ ][ImageResumeScriptIcon] прокручиваемой.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Where to resume script running" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Where to resume script running  
        :::image-end:::  
        
    1.  Нажмите **кнопку "Установить фон"** выше.  При этом для `style` атрибута узла устанавливается `background-color:thistle` ".  DevTools приостанавлиет страницу и выделяет код, который вызвал изменение атрибута.  
    1.  Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \), as mentioned earlier.  
    
### Приорвать удаление узла  

Если необходимо приостановить удаление определенного узла, используйте точки останова удаления узлов.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **окне "Приорвать при удалении узла"** выберите "Неуловимый" и выберите **"Проверить".** ****  
    1.  В дереве DOM щелкните правой кнопкой мыши и выберите `<li id="target">Neuromancer</li>` **"Приорвать удаление**  >  **узла".**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  
    1.  Нажмите **кнопку "Удалить"** выше.  DevTools приостанавлиет страницу и выделяет код, который вызвал удаление узла.  
    1.  Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \).  
    
### Приорвать изменения подtree  

После того как вы добавили точку останова изменения подпотека на узел, DevTools приостанавлит страницу при добавлении или удалении любого из потомков узла.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  Under **Break on Subtree Modifications**, right-choose **A Fire On The Deep** and choose **Inspect**.  
    1.  В дереве DOM щелкните правой кнопкой мыши узел выше и выберите "Break `<ul id="target">` `<li>A Fire Upon the Deep</li>` **On**  >  **Subtree Modifications".**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  
    1.  Choose **Add Child**.  Код приостанавливовка, так как `<li>` узел был добавлен в список.  
    1.  Choose **Resume Script** \( Resume Script ![ ][ImageResumeScriptIcon] \).  
    
## Дальнейшие действия  

Это охватывает большинство функций, связанных с DOM, в DevTools.  Остальные узлы можно найти, щелкнув правой кнопкой мыши узлы в дереве DOM и поэкспериментируйте с другими вариантами, которые не были охвачены в этом руководстве.  Перейдите [к сочетаниям клавиш панели элементов.][DevToolsShortcutsElements]  

Ознакомьтесь [с домашней страницей Microsoft Edge DevTools,][MicrosoftEdgeDevTools] чтобы узнать все остальные возможности, которые вы можете сделать с DevTools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## Приложение: HTML и DOM  

В следующем разделе быстро объясняется разница между HTML и DOM.  

:::row:::
   :::column span="":::
      При использовании веб-браузера для запроса страницы сервер возвращает HTML, как в следующем фрагменте кода  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      Браузер проансирует HTML-код и создает дерево объектов, таких как следующий список.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.  

:::row:::
   :::column span="":::
      Сейчас он выглядит так же, как HTML, но предположим, что сценарий, на который ссылается в нижней части HTML, выполняет следующий фрагмент кода.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Этот код удаляет узел `h1` и добавляет другой узел в `p` DOM.  Полная doM теперь отображает следующий список.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

HTML-код страницы теперь отличается от DOM.  Другими словами, HTML представляет исходное содержимое страницы, а DOM — текущее содержимое страницы.  Когда JavaScript добавляет, удаляет или редактирует узлы, DOM становится не так, как HTML.  

Чтобы узнать [больше, перейдите в "Введение][MDNIntroductionToDOM] в DOM".  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## Приложение: отсутствуют параметры  

Многие инструкции в этом руководстве предписывают щелкнуть правой кнопкой мыши узел в дереве DOM, а затем выбрать параметр из всплывающее контекстное меню.  Если указанный параметр в контекстное меню не отображается, попробуйте щелкнуть правой кнопкой мыши текст узла.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Где выбрать, если все параметры не отображаются" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Где выбрать, если все параметры не отображаются  
:::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCssGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-panel-keyboard-shortcuts "Сочетания клавиш панели элементов — Microsoft Edge DevTools Keyboard Shortcuts | Документы Майкрософт"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Example | Временный сбой"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в DOM | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/dom/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
