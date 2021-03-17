---
description: Откройте консоль, создайте живое выражение и установите выражение document.activeElement.
title: Отслеживание элемента, на котором установлен фокус
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2c2040c690441fb33c802cf454dc7a1e3f33c494
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439172"
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

# <a name="track-which-element-has-focus"></a>Отслеживание элемента, на котором установлен фокус  

Предположим, что вы тестируете доступность навигации по клавиатуре страницы.  При навигации по странице с ключом кольцо фокуса иногда исчезает, так как элемент с `Tab` фокусом скрыт.  

Выполните следующие действия для отслеживания сфокусированного элемента в DevTools.  

1.  Откройте **консоль.**  
1.  Выберите **Создать живое выражение** \. ![ Создайте живое ](../media/create-live-expression-icon.msft.png) выражение \).  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Создание live expression" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       Создание live expression  
    :::image-end:::  
    
1.  Введите `document.activeElement`.  
1.  Чтобы сохранить, выберите вне пользовательского интерфейса **Live Expression.**  
    
Показанное ниже `document.activeElement` значение является результатом выражения.  

Так как это выражение всегда представляет собой сфокусированный элемент, теперь у вас есть способ всегда отслеживать, какой элемент имеет фокус.  

*   Наведите курсор на результат, чтобы выделить фокусный элемент в представлении.  
*   Наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите панель **Reveal in Elements,** чтобы показать элемент дерева DOM на средстве **Elements.**  
*   Наведите курсор на результат, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Store** в качестве глобальной переменной, чтобы создать переменную ссылку на узел, который можно использовать в **консоли.**  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
