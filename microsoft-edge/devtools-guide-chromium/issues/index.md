---
description: Используйте средство "Проблемы" для поиска и устранения проблем с веб-сайтом.
title: Поиск и устранение проблем с средством Microsoft Edge DevTools Issues
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8bd3e5950572a9d3fdce71ec6cd935f6b6d6a0b7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230665"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Поиск и устранение проблем с средством Microsoft Edge DevTools Issues  

Средство **"Проблемы"** в Microsoft Edge DevTools позволяет уменьшить помехи в уведомлении **консоли.**  Используйте его для поиска решений проблем, обнаруженных браузером, таких как проблемы с файлами cookie и смешанное содержимое.  

> [!NOTE]
> В Microsoft Edge 84 средство **"Проблемы"** поддерживает три типа проблем:  
> *   [Проблемы с файлами cookie][MDNSameSiteCookies]  
> *   [Смешанное содержимое][MDNMixedContent]  
> *   [Проблемы COEP][W3CCOEPSpec]
> 
> Группа разработчиков Microsoft Edge DevTools планирует поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.  

## Открытие средства "Проблемы" в средстве DevTools  

1.  Посетите страницу, например [samesite-sandbox.glitch.me,][GlitchSamesiteSandbox]которая содержит проблемы, которые необходимо исправить.  
1.  [Откройте DevTools.][DevtoolsOpen]  
1.  :::row:::
       :::column span="":::
          Choose the **Go to Issues** button in the yellow warning bar.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Перейдите к кнопке Проблемы в желтой панели предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             Кнопка **"Перейти к вопросам"** в желтой панели предупреждения при обнаружении проблем.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Кроме того, выберите **пункт "Проблемы"** в меню **"Дополнительные средства".**  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Средство Проблемы в меню "Дополнительные средства"" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Средство "Проблемы"** в **меню "Дополнительные средства"**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  При необходимости **выберите кнопку "Перезагрузить** страницу".  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Средство Проблемы в средстве DevTools Drawer с кнопкой Перезагрузить страницу" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Средство "Проблемы"** в средстве "DevTools Drawer" с **кнопкой "Перезагрузить страницу"**  
    :::image-end:::  

    Проблемы, о которые **сообщается** в консоли, довольно сложно понять, например предупреждения cookie на следующем изображении.  В зависимости от сообщений о проблемах может быть не ясно, что необходимо сделать.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Средство Проблемы в средстве DevTools Drawer с тремя вопросами cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Средство "Проблемы"** в средстве DevTools Drawer с тремя вопросами cookie  
    :::image-end:::  
    
## Просмотр элементов в средстве "Проблемы"  

Средство **"Проблемы"** в средстве "DevTools Drawer" представляет предупреждения структурированным, агрегируемым и в действии способом.  

1.  Выберите элемент в средстве **"Проблемы",** чтобы получить инструкции по устранению проблемы и поиску затронутых ресурсов.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Пометить межсемейные файлы cookie как безопасные, открытые в средстве Проблемы" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Пометить межсемейные файлы cookie как безопасные,** открытые в **средстве "Проблемы"**  
    :::image-end:::  
    
    Каждый элемент имеет четыре компонента:  
    
    *   Заголовок, описывающий проблему.  
    *   Описание, предоставляющая контекст и решение.  
    *   Раздел **"ЗАТРОНУТЫЕ** РЕСУРСЫ", который ссылается на ресурсы в соответствующем контексте DevTools, например на панели "Сеть".  
    *   Ссылки на дополнительные рекомендации.  
    
1.  Выберите элементы в **AFFECTED RESOURCES,** чтобы просмотреть сведения.  В следующем примере пометка меж сайта **cookie как** проблема "Безопасная" влияет на один файл cookie и два запроса.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Затронутые ресурсы открываются на вкладке Ящик проблем" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Затронутые ресурсы открываются в средстве **"Проблемы"** в средстве "DevTools Drawer"  
    :::image-end:::  
    
## Просмотр проблем в контексте  

1.  Выберите ссылку на ресурс, чтобы просмотреть элемент в соответствующем контексте в DevTools.  В следующем примере выберите в области `samesite-sandbox.glitch.me` **"Запросы",** чтобы показать файлы cookie, прикрепленные к этому запросу.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Просмотр затронутой области Cookie на панели Сеть DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       Просмотр затронутой области "Cookie" **** на панели "Сеть DevTools"  
    :::image-end:::  

1.  Прокрутите страницу, чтобы просмотреть элемент с проблемой: в следующем примере файл `ck02` cookie.  Наведите курсор на **столбец SameSite,** чтобы увидеть `None` значение, обнаруженного проблемой.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Отсутствует значение в столбце SameSite для файла cookie ck02 на панели DevTools Network" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` значение в **столбце SameSite** для файла cookie на панели `ck02` Сети DevTools ****  
    :::image-end:::  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Тесты файлов cookie SameSite | Временный сбой"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Файлы cookie SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанное содержимое | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика встраивляемого перекрестного источника | Группа сообщества веб-инкуаторов"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/issues/index) и автором [Sam Dutton][SamDutton] \(Developer Advocate\).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
