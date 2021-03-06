---
description: Если вы находите, что введите те же выражения JavaScript в консоль несколько раз, попробуйте Live Expressions вместо этого.
title: Просмотр значений выражений JavaScript в режиме реального времени с помощью Live Expressions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 5bc49b60cc1c1dfb41c793c3fec7681fb6415e4c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398800"
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

# <a name="watch-javascript-expression-values-in-real-time-with-live-expressions"></a>Просмотр значений выражений JavaScript в режиме реального времени с помощью Live Expressions  

Если вы напечатаете одно и то же выражение JavaScript в консоли несколько раз, вам может быть проще создать **выражение Live.**  С **помощью Live Expressions** вы введите выражение один раз, а затем прикрепите его к верхней части консоли.  Значение обновлений выражения почти в режиме реального времени.  

## <a name="create-a-live-expression"></a>Создание live expression  

1.  [Откройте консоль.][DevToolsConsoleReferenceOpenConsole]  
1.  Выберите **Создать живое выражение** \. ![ Создайте живое ][ImageCreateLiveExpressionIcon] выражение \).  Появится текстовое поле **Live Expression.**  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Ввод document.activeElement в текстовом окне Live Expression" lightbox="../media/console-create-live-expression.msft.png":::
       Ввод `document.activeElement` текста **в текстовом окне Live Expression**  
    :::image-end:::  
    
1.  Выберите `Control` + `Enter` \(Windows, Linux\) `Command` + `Enter` или \(macOS\) **** для сохранения выражения или выберите вне текстового ящика Live Expression.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Откройте консоль — справочный | Документы Майкрософт"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
