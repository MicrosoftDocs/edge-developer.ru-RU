---
description: Просмотр узлов, поиск узлов, редактирование узлов, справочных узлов в консоли, перерыв в изменениях узлов и т. д.
title: Начало работы с просмотром и изменением DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439242"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a>Начало работы с просмотром и изменением DOM  

Выполните эти интерактивные учебники, чтобы узнать основы просмотра и изменения DOM страницы с помощью Microsoft Edge DevTools.  

В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.  Перейдите [к приложению: HTML и DOM для](#appendix-html-versus-the-dom) объяснения.  

## <a name="open-dom-examples"></a>Откройте примеры DOM  

1.  Удерживайте `Control` \(Windows, Linux\) `Command` или \(macOS\) и выберите **примеры DOM,** чтобы открыть на новой вкладке.  
    
    [Примеры DOM][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Просмотр узлов DOM  

DoM Tree панели Elements — это место, где вы делаете все действия, связанные с DOM в DevTools.  

### <a name="inspect-a-node"></a>Проверка узла  

Если вас интересует определенный узел DOM, **Проверьте** это быстрый способ открыть DevTools и исследовать этот узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Проверка узла**выберите справа **Микеланджело и** выберите **инспектировать**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Проверка узла" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Проверка узла  
    :::image-end:::  
    
    1.  Откроется **средство Elements** devTools.  `<li>Michelangelo</li>` выделено в **dom Tree**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Выделение узла Микеланджело" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Выделение `Michelangelo` узла  
        :::image-end:::  
        
        1.  Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Значок Inspect" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Значок **Inspect**  
            :::image-end:::  
            
1.  В **статье Inspect a Node**выберите текст **Tokyo.**  Теперь `<li>Tokyo</li>` выделяется дерево DOM.  

Проверка узла также является первым шагом к просмотру и изменению стилей узла.  [Перейдите, чтобы начать с просмотра и изменения CSS][DevToolsCssGetStarted].  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Перемещение дерева DOM с помощью клавиатуры  

Выбрав узел в dom Tree, вы можете перемещаться по дереву DOM с помощью клавиатуры.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Перейдите по дереву DOM с клавиатурой,** выберите Ринго правой ринго **и** выберите **Инспектировать**.  `<li>Ringo</li>` выбрано в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Проверка узла Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Проверка `Ringo` узла  
    :::image-end:::  
    
    1.  Выберите `Up` клавишу стрелки 2 раза.  `<ul>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Проверка узла ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Проверка `ul` узла  
        :::image-end:::  
        
    1.  Выберите `Left` клавишу стрелки.  Список `<ul>` разрушается.  
    1.  Снова выберите `Left` клавишу стрелки.  Выбран родительский `<ul>` узел.  В этом случае это `<div>` с ID `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Выберите клавишу стрелки 2 раза, чтобы повторно выбрать только что свернутый `Down` `<ul>` список.  Это должно выглядеть следующим образом. `<ul>... </ul>`  
    1.  Выберите `Right` клавишу стрелки.  Список расширяется.  

### <a name="scroll-into-view"></a>Прокрутка в представлении  

При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в настоящее время не находится в представлении.  Например, предположим, что вы прокрутки в нижней части страницы, и вас интересует узел в верхней `<h1>` части страницы.  **Прокрутка** в представлении позволяет быстро переместить viewport, чтобы можно было просмотреть узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Scroll into View**выберите **магритт** правой точки и выберите **инспект.**  
1.  Прокрутите в нижней части страницы примеры DOM.  
1.  Узел `<li>Magritte</li>` по-прежнему должен быть выбран в dom Tree.  Если нет, возвращайся к [прокрутке в представлении и](#scroll-into-view) начинай сначала.  
1.  Наведите курсор на узел, откройте контекстное меню \(правой кнопкой `<li>Magritte</li>` мыши\) и выберите **Прокрутку в вид**.  Ваш видпорт прокручивается назад, чтобы просмотреть узел **Magritte.**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если вы не можете просмотреть параметр **Scroll в представлении.**
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Прокрутка в представлении" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Прокрутка в представлении**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Поиск узлов  

Вы можете искать дерево DOM по строке, селектору CSS или селектору XPath.  

1.  Сосредоточь курсор на **средстве Elements.**  
1.  Выберите `Control` + `F` \(Windows, Linux\) `Command` + `F` или \(macOS\).  Строка поиска открывается в нижней части дерева DOM.  
1.  Введите `The Moon is a Harsh Mistress`.  Последнее предложение выделено в дереве DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Выделение запроса в панели поиска" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Выделение запроса в панели поиска  
    :::image-end:::  
    
Как упоминалось выше, в панели поиска также поддерживаются селекторы CSS и XPath.  

## <a name="edit-the-dom"></a>Изменение DOM  

Вы можете изменить DOM на лету и просмотреть, как изменения влияют на страницу.  

### <a name="edit-content"></a>Редактирование контента  

Чтобы изменить содержимое узла, дважды щелкните содержимое в dom Tree.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Редактирование контента**выберите Мишель **правильно и** выберите **инспектировать**.  
    1.  В дереве DOM дважды щелкните `Michelle` .  Другими словами, дважды щелкните текст между `<li>` и `</li>` .  Текст выделен, чтобы указать, что он выбран.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Изменение текста" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Изменение текста  
        :::image-end:::  
        
    1.  `Michelle`Удалите, `Leela` введите, а `Enter` затем выберите, чтобы подтвердить изменение.  Текст в DOM изменяется с **Мишель на** **Лилу**.  

### <a name="edit-attributes"></a>Изменение атрибутов  

Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.  Следуйте инструкциям, чтобы узнать, как добавлять атрибуты в узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Изменить атрибуты**выберите Ховард **** правильно и выберите **инспектировать**.  
1.  Дважды `<li>` щелкните .  Текст выделен, чтобы указать, что узел выбран.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Изменение узла" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Изменение узла  
    :::image-end:::  
    
1.  Выберите `Right` клавишу стрелки, добавьте пробел, введите `style="background-color:gold"` и выберите `Enter` .  Фоновый цвет узла меняется на золото.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Добавление атрибута стиля в узел" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Добавление `style` атрибута в узел  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Изменение типа узла  

Чтобы изменить тип узла, дважды щелкните тип и введите новый тип.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  При **редактировании типа узла**выберите справа **Хэнк** и выберите **инспектировать**.  
    1.  Дважды `<li>` щелкните .  Текст `li` выделен.  
    1.  `li`Удалите, `button` введите, а затем выберите `Enter` .  Узел `<li>` изменяется в `<button>` узел.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Изменение типа узла на кнопку" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Изменение типа узла на `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Reorder DOM nodes  

Перетаскивать узлы для их переуборки.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Reorder DOM Nodes**выберите правый **элвис Пресли** и выберите **Inspect**.  
    
    > [!NOTE]
    > Это последний элемент в списке.  
    
    1.  В дереве DOM `<li>Elvis Presley</li>` перетащите в верхнюю часть списка.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Перетащите узел в верхнюю часть списка" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Перетащите узел в верхнюю часть списка  
        :::image-end:::  
        
### <a name="force-state"></a>Состояние Force  

Вы можете заставить узлы оставаться в состояниях, включая `:active` , , , , и `:hover` `:focus` `:visited` `:focus-within` .  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **состоянии Force**наведите курсор на **"Властелин мух".**  Цвет фона становится оранжевым.  
    1.  Наведите курсор на **"Властелин мух",** откройте контекстное меню \(правой кнопкой мыши\) и выберите **инспектировать**.  
    1.  Наведите `<li class="demo--hover">The Lord of the Flies</li>` курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Состояние силы**  >  **:hover**.  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  Цвет фона остается оранжевым, даже если вы на самом деле не зависаете над узлом.  

### <a name="hide-a-node"></a>Скрыть узел  

Выберите, `H` чтобы скрыть узел.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Скрыть узел**выберите "Звезды моего **назначения"** и выберите **инспектировать**.  
    1.  Выберите `H` ключ.  Узел скрыт.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Как выглядит узел в dom Tree после его сокрытого" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Как выглядит узел в dom Tree после его сокрытого  
        :::image-end:::  
        
    1.  Выберите `H` клавишу снова.  Узел отображается снова.  

### <a name="delete-a-node"></a>Удаление узла  

Выберите `Delete` удаление узла.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Delete a Node**выберите правильный выбор **Основы** и выберите **инспектировать**.  
    1.  Выберите `Delete` ключ.  Узел удаляется.  
    1.  Выберите `Control` + `Z` \(Windows, Linux\) `Command` + `Z` или \(macOS\).  Последнее действие отменить, и узел снова появится.  

## <a name="access-nodes-in-the-console"></a>Доступ к узлам консоли  

DevTools предоставляет несколько ярлыков для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждый из них.  

### <a name="reference-the-currently-selected-node-with-0"></a>Ссылка на выбранный в настоящее время узел с $0  

При проверке узла текст рядом с узлом означает, что этот узел в консоли может ссылаться `== $0` на `$0` переменную.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В статье Ссылка на выбранный в настоящее время **узел с $0**, правой выберите **левую** руку тьмы и выберите **инспектировать**.  
    1.  Выберите ключ `Escape` для открытия ящика консоли.  
    1.  Введите `$0` и выберите `Enter` ключ.  Результат выражения показывает, что `$0` оценивает до `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Результат первого выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            Результат первого выражения `$0` в **** консоли  
        :::image-end:::  
        
    1.  Наведите курсор на результат.  Узел выделен в представлении.  
    1.  Выберите `<li>Dune</li>` в дереве DOM, введите консоль `$0` снова, а затем выберите еще `Enter` раз.  Теперь `$0` оценивается до `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Результат второго выражения $0 в консоли" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Результат второго выражения `$0` в **** консоли  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Хранить как глобальную переменную  

Если требуется много раз возвращаться к узлу, храните его в качестве глобальной переменной.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **Хранилище в качестве глобальной переменной**наведите курсор на **"Большой**сон", откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**.  
    1.  Наведите курсор в dom Tree, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li>The Big Sleep</li>` Store в качестве **глобальной переменной.**  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  
    1.  Введите `temp1` консоль и выберите `Enter` .  Результат выражения показывает, что переменная оценивает узел.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Результат выражения temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           Результат выражения `temp1`  
        :::image-end:::  
        
### <a name="copy-js-path"></a>Путь копирования JS  

Скопируйте путь JavaScript в узел, если необходимо ссылаться на него в автоматическом тесте.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **рамках пути Copy JS**наведите курсор на братья Карамазовы, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Inspect**. ****  
    1.  Наведите курсор в дереве DOM, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li>The Brothers Karamazov</li>` **путь Копирование**  >  **копии JS**.  Выражение, `document.querySelector()` разрешаемая узлу, было скопировано в буфер обмена.  
    1.  Выберите `Control` + `V` \(Windows, Linux\) `Command` + `V` или \(macOS\) для вставки выражения в консоль.  
    1.  Выберите `Enter` для оценки выражения.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Результат выражения Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Результат выражения **Copy JS Path**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Перерыв в изменениях DOM  

DevTools позволяет приостановить JavaScript страницы, когда JavaScript изменяет DOM.  

### <a name="break-on-attribute-modifications"></a>Перерыв в изменении атрибута  

Используйте брейк-точки изменения атрибута, когда необходимо приостановить JavaScript, из-за чего любой атрибут узла будет изменяться.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Break on attribute modifications**выберите правый выбор **Sauerkraut** и выберите **Inspect**.  
    1.  В дереве DOM наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li id="target">Sauerkraut</li>` **Break On**  >  **Attribute Modifications**.  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Перерыв в изменении атрибута" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Перерыв в изменении атрибута**  
        :::image-end:::  
        
    1.  На следующем шаге вам будет поручено выбрать кнопку, приостановив код страницы.  После приостановки страницы вы больше не сможете прокручивать страницу.  Для повторного **прокрутки** страницы необходимо выбрать сценарий резюме ![ ](../media/resume-script-icon.msft.png) \.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Где возобновить работу скрипта" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Где возобновить работу скрипта  
        :::image-end:::  
        
    1.  Выберите **кнопку Set Background** выше.  Это задает `style` атрибут узла `background-color:thistle` .  DevTools останавливает страницу и выделяет код, из-за чего атрибут изменился.  
    1.  Выберите **сценарий** резюме \. ![ Сценарий ](../media/resume-script-icon.msft.png) резюме \), как упоминалось ранее.  
    
### <a name="break-on-node-removal"></a>Перерыв при удалении узлов  

Если необходимо приостановить удаление определенного узла, используйте точки удаления узлов.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В статье Break on Node Removal (Удаление **узлов)** выберите **справа Neuromancer и** выберите **Inspect**.  
    1.  В дереве DOM наведите курсор, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<li id="target">Neuromancer</li>` **Break On**  >  **Node Removal**.  Перейдите [к приложению: отсутствуют параметры,](#appendix-missing-options) если параметр не отображается.  
    1.  Выберите **кнопку Удалить** выше.  DevTools останавливает страницу и выделяет код, из-за чего узел был удален.  
    1.  Выберите **сценарий** резюме \. ![ Сценарий ](../media/resume-script-icon.msft.png) резюме \).  
    
### <a name="break-on-subtree-modifications"></a>Перерыв в изменениях подтрия  

После того, как на узел будет добавлена точка взлома модификации подтримки, DevTools приостанавлит страницу при добавлении или удалении любого из потомков узла.  

1.  [Откройте примеры DOM.](#open-dom-examples)  
1.  В **статье Break on Subtree Modifications (Изменения subtree)** выберите правильное решение **"Пожар на глубине"** и выберите **"Проверка".**  
    1.  В дереве DOM наведите курсор , который является узлом выше, откройте контекстное меню \(правой кнопкой мыши\) и выберите `<ul id="target">` `<li>A Fire Upon the Deep</li>` Break **On**  >  **Subtree Modifications**.  Если параметр не отображается, перейдите в [Приложение: Отсутствующие параметры.](#appendix-missing-options)  
    1.  Выберите **Добавить ребенка**.  Код приостанавливовка, так как `<li>` узел был добавлен в список.  
    1.  Выберите **сценарий** резюме \. ![ Сценарий ](../media/resume-script-icon.msft.png) резюме \).  
    
## <a name="next-steps"></a>Дальнейшие действия  

Это охватывает большинство функций, связанных с DOM в DevTools.  Остальные функции можно обнаружить, зависнув на узлах дерева DOM, открыв контекстное меню \(правой кнопкой мыши\) и поэкспериментируйте с другими вариантами, которые не были охвачены в этом учебнике.  Перейдите к [клавишам клавиатуры][DevToolsShortcutsElements]панели Elements .  

Ознакомьтесь с [домашней страницей Microsoft Edge DevTools,][MicrosoftEdgeDevTools] чтобы узнать все остальное, что вы можете сделать с DevTools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Приложение: HTML по сравнению с DOM  

В следующем разделе быстро объясняется разница между HTML и DOM.  

:::row:::
   :::column span="":::
      При использовании веб-браузера для запроса страницы сервер возвращает HTML, как и следующий фрагмент кода  

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
      Браузер размазирует HTML и создает дерево объектов, таких как следующий список.  
      
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
      Этот код удаляет `h1` узел и добавляет другой узел в `p` DOM.  Полный DOM теперь отображает следующий список.  
      
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

HTML для страницы теперь отличается от DOM.  Другими словами, HTML представляет исходное содержимое страницы, а DOM — текущее содержимое страницы.  Когда JavaScript добавляет, удаляет или редактирует узлы, DOM становится другим, чем HTML.  

Перейдите [к вводу в DOM,][MDNIntroductionToDOM] чтобы узнать больше.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Приложение: отсутствующие параметры  

Многие инструкции в этом руководстве поручают вам наведении на узел в dom Tree, открыть контекстное меню \(правой кнопкой мыши\), а затем выбрать вариант из контекстного меню, которое всплывает.  Если указанный параметр в контекстном меню не отображается, попробуйте отойти от текста узла и открыть контекстное меню \(правой кнопкой мыши\).  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Где выбрать, если все параметры не отображаются" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Где выбрать, если все параметры не отображаются  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge \(Chromium\) | Документы Майкрософт"  
[DevToolsCssGetStarted]: ../css/index.md "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Клавиши клавиатуры elements — клавиши Microsoft Edge DevTools Keyboard Shortcuts | Документы Майкрософт"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Example | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Введение в dom | MDN"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/dom/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
