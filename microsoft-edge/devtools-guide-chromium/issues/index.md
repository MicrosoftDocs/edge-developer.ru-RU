---
description: Используйте средство Issues для поиска и устранения проблем с веб-сайтом.
title: Поиск и устранение проблем с помощью средства Microsoft Edge DevTools Issues
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e16bd926ea5bae35ad82f54ac5d1ae2028e3c59d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398978"
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

# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a>Поиск и устранение проблем с помощью средства Microsoft Edge DevTools Issues  

Средство **Issues** в Microsoft Edge DevTools снижает усталость уведомлений и помехи **консоли.**  Используйте его для поиска решений проблем, обнаруженных браузером, таких как проблемы с файлами cookie и смешанный контент.  

> [!NOTE]
> В Microsoft Edge 84 средство **Issues** поддерживает три типа проблем:  
> *   [Проблемы с cookie][MDNSameSiteCookies]  
> *   [Смешанный контент][MDNMixedContent]  
> *   [Проблемы COEP][W3CCOEPSpec]
> 
> Группа Microsoft Edge DevTools планирует поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a>Откройте средство Issues в ящике DevTools  

1.  Перейдите на веб-страницу, [например samesite-sandbox.glitch.me,][GlitchSamesiteSandbox]которая содержит проблемы, которые необходимо устранить.  
1.  [Откройте DevTools][DevtoolsOpen].  
1.  :::row:::
       :::column span="":::
          Выберите **кнопку Перейти к вопросам** в желтой панели предупреждения.  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Перейдите к кнопке "Проблемы" в желтой панели предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             Кнопка **"Перейти к вопросам"** в желтой панели предупреждения при обнаружении проблем.  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Кроме того, выберите **Вопросы из** меню **More tools.**  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Средство issues в меню More tools" lightbox="../media//issues-more-tools-menu.msft.png":::
             **Средство issues** в **меню More tools**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  При необходимости **выберите кнопку** Перезагрузить страницу.  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Проблема средства в ящике DevTools с кнопкой перезагрузки страницы" lightbox="../media/issues-tab-before-refresh.msft.png":::
       **Проблема средства** в ящике DevTools с **кнопкой перезагрузки страницы**  
    :::image-end:::  

    Проблемы, которые сообщаются в **консоли,** довольно трудно понять, например предупреждения о cookie на следующем изображении.  На основании сообщений о проблемах может быть не ясно, что нужно сделать.  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Проблема средства в ящике DevTools с тремя вопросами cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       **Проблема средства** в ящике DevTools с тремя вопросами cookie  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a>Просмотр элементов в средстве Issues  

Средство **Issues** в ящике DevTools представляет предупреждения структурированным, агрегируемым и действий.  

1.  Выберите элемент в средстве **Issues,** чтобы получить рекомендации по устранению проблемы и поиску затронутых ресурсов.  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Пометить межуголевое cookie как проблему Secure, открытую в средстве Issues" lightbox="../media/issues-tab-issue-open.msft.png":::
       **Пометить межуголевое cookie как проблему Secure,** открытую в **средстве Issues**  
    :::image-end:::  
    
    Каждый элемент имеет четыре компонента:  
    
    *   Заголовок, описывающий проблему.  
    *   Описание, предоставляющая контекст и решение.  
    *   Раздел **AFFECTED RESOURCES,** который связывается с ресурсами в соответствующем контексте DevTools, например с панелью Network.  
    *   Ссылки на дополнительные рекомендации.  
    
1.  Выберите элементы **в AFFECTED RESOURCES для** просмотра сведений.  В следующем примере **маркеры Mark в качестве** проблемы Secure затрагивают один файл cookie и два запроса.  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Затронутые ресурсы, открытые в средстве Issues" lightbox="../media/issues-tab-affected-resources.msft.png":::
       Затронутые ресурсы, открытые в **средстве Issues** в ящике DevTools  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a>Просмотр проблем в контексте  

1.  Выберите ссылку ресурса для просмотра элемента в соответствующем контексте в DevTools.  В следующем примере выберите `samesite-sandbox.glitch.me` в **статье Запросы,** чтобы показать файлы cookie, присоединенные к этому запросу.  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Просмотр затронутых файлов cookie в средстве Сети DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       Просмотр затронутых файлов cookie в **** средстве Сети DevTools  
    :::image-end:::  

1.  Прокрутите, чтобы просмотреть элемент с проблемой: в следующем примере — `ck02` файл cookie.  Наведите курсор **на столбец SameSite,** чтобы просмотреть `None` обнаруженную проблему.  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Нет значения в столбце SameSite для cookie ck02 в средстве Сети DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` значение в столбце **SameSite** для `ck02` cookie в **** средстве Сети DevTools  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Тесты cookie SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Файлы cookie SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанный контент | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика встраивляемого | Группа сообщества веб-инкубаторов"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/issues/index) и является автором [Sam Dutton][SamDutton] \(Developer Advocate\).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
