---
description: Полная ссылка на функции доступности в Microsoft Edge DevTools.
title: Справка о доступности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e3fed1c4e53c69b7a6837f71c270c0bf2f65b7e2
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398338"
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

# <a name="accessibility-reference"></a>Справка о доступности  

Эта страница — это всеобъемлющая ссылка на функции доступности в Microsoft Edge DevTools.  Он предназначен для веб-разработчиков, которые:  

*   У вас есть базовое представление о DevTools, например о том, как его открыть.  
*   Знакомы с [принципами доступности и лучшими практиками.][MDNAccessibility]  
    
Эта ссылка поможет вам найти все средства, доступные в DevTools, которые помогут вам изучить доступность страницы.  

Если вы ищете помощь в навигации по DevTools с помощью вспомогательных технологий, таких как считыватель экрана, перейдите к навигации [Microsoft Edge DevTools с помощью вспомогательных технологий][DevtoolsAccessibilityNavigation].  

## <a name="overview-of-accessibility-features-in-microsoft-edge-devtools"></a>Обзор возможностей доступности в Microsoft Edge DevTools  

В этом разделе объясняется, как DevTools вписывается в общий набор средств доступности.  

При определении доступности страницы необходимо иметь в виду 2 общих вопроса:  

1.  Можете ли вы перемещаться по странице с помощью клавиатуры или [чтения с экрана?][MDNScreenReader]  
1.  Правильно ли помечены элементы страницы для чтения с экрана?  
    
В общем, DevTools должен помочь вам устранить ошибки, связанные с вопросом #2, так как эти ошибки легко обнаружить в автоматическом режиме.  Вопрос #1 так же важен, но, к сожалению, DevTools не поможет вам там.  Единственный способ найти ошибки, связанные с вопросом #1, это попробовать использовать страницу с клавиатурой или экраном чтения самостоятельно.  <!--To learn more, navigate to [How To Do An Accessibility Review][AccessibilityReview].  -->  

<!--[AccessibilityReview]: /web/fundamentals/accessibility/how-to-review  -->  

## <a name="audit-the-accessibility-of-a-page"></a>Аудит доступности страницы  

> [!NOTE]
> Средство **аудита** предоставляет ссылки на контент, который содержится на сторонних веб-сайтах.  Корпорация Майкрософт не несет ответственности и не контролирует содержимое этих сайтов и любые данные, которые могут быть собраны.  

В общем случае используйте панель аудитов, чтобы определить, если:  

*   Страница правильно помечена для чтения с экрана.  
*   Текстовые элементы на странице имеют достаточные коэффициенты контрастности.  Перейдите [к просмотру соотношения контрастности текстового элемента в элементе Color Picker.](#view-the-contrast-ratio-of-a-text-element-in-the-color-picker)  

Аудит страницы:  

1.  Перейдите к URL-адресу, который необходимо аудитировать.  
1.  В DevTools выберите средство **аудита.**  В DevTools показаны различные параметры конфигурации.  
    
    :::image type="complex" source="../media/accessibility-audits-pane.msft.png" alt-text="Настройка аудита" lightbox="../media/accessibility-audits-pane.msft.png":::
       Настройка аудита  
    :::image-end:::  
    
    > [!NOTE]
    > Скриншоты в этом разделе были сделаны с помощью версии 79 Microsoft Edge.  Вы можете проверить, в какой версии вы `edge://version` работаете.  Пользовательский **интерфейс** средства аудита выглядит иначе в более ранних версиях Microsoft Edge, но общий рабочий процесс одинаковый.  
    
1.  Для **устройства**выберите **Mobile,** если вы хотите смоделировать мобильное устройство.  Этот параметр изменяет строку агента пользователя и изменяет параметр viewport.  Если мобильная версия страницы отображает не так, как в настольной версии, этот параметр может существенно действовать на результаты аудита.  
1.  В разделе **Аудиты** убедитесь, что **включена доступность.**  Отключите другие категории, если вы хотите исключить их из отчета.  Оставьте их включенными, если вы хотите найти другие способы улучшения качества страницы.  
1.  Раздел **регулирование позволяет** управлять сетью и ЦП, что полезно при анализе производительности нагрузки.  Этот параметр должен быть неактуален для оценки доступности, поэтому вы можете использовать все, что хотите.  
1.  Почтовый **ящик Clear Storage** позволяет очистить все хранилища перед загрузкой страницы или сохранить хранилище между нагрузками на страницу.  Этот параметр также, вероятно, не имеет значения для оценки доступности, поэтому вы можете использовать все, что вы предпочитаете.  
1.  Выберите **выполнить аудиты.** Через 10-30 секунд DevTools предоставляет отчет.  В отчете вы можете получить различные советы по улучшению доступности страницы.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result.msft.png" alt-text="Отчет" lightbox="../media/accessibility-audits-run-audits-result.msft.png":::
       Отчет  
    :::image-end:::  
    
1.  Чтобы узнать больше об этом, выберите аудит.  
    
    :::image type="complex" source="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png" alt-text="Дополнительные сведения о аудите" lightbox="../media/accessibility-audits-run-audits-result-issues-expanded.msft.png":::
       Дополнительные сведения о аудите  
    :::image-end:::  
    
1.  Чтобы **просмотреть** документацию этого аудита, выберите Дополнительные дополнительные.  
    
    :::image type="complex" source="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png" alt-text="Просмотр документации аудита" lightbox="../media/accessibility-web-dev-accessibility-audits-learn-more.msft.png":::
       Просмотр документации аудита  
    :::image-end:::  
    
### <a name="see-also-axe-extension"></a>См. также: расширение aXe  

Вы можете использовать расширение [aXe,][ChromeWebStoreAxe] а не средство **аудита.**  
Расширение aXe обычно предоставляет ту же информацию, так как это является движком, который приводит в движок панели Аудиты.  Расширение aXe имеет другой пользовательский интерфейс и описывает аудиты немного по-другому.  
Одно из преимуществ расширения aXe над средством **Аудита** заключается в том, что оно позволяет проверять и выделять узлы с ошибками.  

:::image type="complex" source="../media/accessibility-devtools-extension-axe-panel.msft.png" alt-text="Расширение aXe" lightbox="../media/accessibility-devtools-extension-axe-panel.msft.png":::
   Расширение aXe  
:::image-end:::  

## <a name="the-accessibility-panel"></a>Панель доступности  

Панель **доступности** — это панель, на которой вы видите дерево доступности, атрибуты ARIA и вычислительные свойства узлов DOM.  

Чтобы открыть панель **доступности:**  

1.  Выберите **средство Elements.**  
1.  В дереве **DOM выберите**элемент, который необходимо проверить.  
1.  Выберите панель **доступности.**  Эта панель может быть скрыта за кнопкой **More Tabs** \( ![ More Tabs ][ImageMoreTabsIcon] \)  

:::image type="complex" source="../media/accessibility-elements-accessibility.msft.png" alt-text="Проверьте элемент h1 домашней страницы DevTools в панели доступности" lightbox="../media/accessibility-elements-accessibility.msft.png":::
   Проверьте `h1` элемент домашней страницы DevTools в панели **доступности**  
:::image-end:::  

### <a name="view-the-position-of-an-element-in-the-accessibility-tree"></a>Просмотр положения элемента в дереве доступности  

Дерево [доступности][MDNAccessibilityTree] — это подмножество дерева DOM.  Он содержит только элементы из дерева DOM, которые являются актуальными и полезными для отображения содержимого страницы в считыватель экрана.  

Проверьте положение элемента в дереве доступности из панели [accessibility.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-tree.msft.png" alt-text="Раздел Дерево доступности" lightbox="../media/accessibility-elements-accessibility-tree.msft.png":::
   Раздел **Дерево доступности**  
:::image-end:::  

### <a name="view-the-aria-attributes-of-an-element"></a>Просмотр атрибутов ARIA элемента  

Атрибуты ARIA гарантируют, что читатели экрана будут иметь всю необходимую информацию для правильного представления содержимого страницы.  

Просмотр атрибутов ARIA элемента в панели [доступности.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-aria-attributes.msft.png" alt-text="Раздел Атрибуты ARIA" lightbox="../media/accessibility-elements-accessibility-aria-attributes.msft.png":::
   Раздел **Атрибуты ARIA**  
:::image-end:::  

### <a name="view-the-computed-accessibility-properties-of-an-element"></a>Просмотр свойств вычислительной доступности элемента  

> [!NOTE]
> Если вы ищете вычислительные свойства CSS, перейдите на [панель Computed.][DevtoolsCssReferenceViewActuallyAppliedElements]  

Некоторые свойства доступности динамически вычисляются браузером.  Эти свойства отображаются в разделе **Computed Properties** панели **доступности.**  

Просмотр свойств вычислительной доступности элемента в панели [доступности.](#the-accessibility-panel)  

:::image type="complex" source="../media/accessibility-elements-accessibility-computed-properties.msft.png" alt-text="Раздел Computed Properties панели доступности" lightbox="../media/accessibility-elements-accessibility-computed-properties.msft.png":::
   Раздел **Computed Properties** панели **доступности**  
:::image-end:::  

## <a name="view-the-contrast-ratio-of-a-text-element-in-the-color-picker"></a>Просмотр соотношения контрастности текстового элемента в элементе Color Picker  

Некоторые люди с низким зрением не видят области как очень яркие или очень темные.  Все имеет тенденцию отображаться примерно с одинаковой яркостью, что затрудняет разграничение контуров и краев.  

Коэффициент контрастности измеряет разницу в яркости между переднем плане и фоном текста.  Если в тексте низкий контраст, то пользователи с низким зрением могут буквально оказаться на вашем сайте в виде пустого экрана.  

Выбор цвета поможет вам убедиться, что текст соответствует рекомендуемым уровням коэффициента контрастности:  

1.  Выберите **средство Elements.**  
1.  В **дереве DOM выберите**текстовый элемент, который необходимо проверить.  
    
    :::image type="complex" source="../media/accessibility-elements-paragraph-highlight.msft.png" alt-text="Проверка абзаца в дереве DOM" lightbox="../media/accessibility-elements-paragraph-highlight.msft.png":::
       Проверка абзаца **в дереве DOM**  
    :::image-end:::  
    
1.  В панели **Стилей** выберите цветной квадрат рядом со `color` значением элемента.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png" alt-text="Свойство цвета элемента" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color.msft.png":::
       Свойство `color` элемента  
    :::image-end:::  
    
1.  Проверьте раздел **Коэффициент контрастности** в цветопоимке.  Одна из контрольных знаков означает, что элемент соответствует [минимальной рекомендации.][W3CContrastMinimum]  Два контрольных знака означает, что он соответствует [расширенной рекомендации][W3CContrastEnhanced].  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png" alt-text="В разделе Коэффициент контрастности в средстве выборки цвета показаны 2 контрольных знака и значение 13,97" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker.msft.png":::
       В **разделе Коэффициент** контрастности в средстве цветопоимыватель показаны 2 контрольных знака и значение `13.97`  
    :::image-end:::  
    
1.  Дополнительные сведения можно получить в разделе **Коэффициент контрастности.**  Строка отображается в визуальном выборщике в верхней части выборки цвета.  Если текущий цвет соответствует рекомендациям, то все, что на той же стороне линии, также соответствует рекомендациям.  Если текущий цвет не соответствует рекомендациям, то все, что имеет одну и ту же сторону, также не соответствует рекомендациям.  
    
    :::image type="complex" source="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png" alt-text="Линия коэффициента контрастности в визуальном выборке" lightbox="../media/accessibility-elements-styles-paragraph-highlight-color-picker-contrast-ratio-details.msft.png":::
       Линия **коэффициента контрастности** в визуальном выборке  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  

<!-- links -->  

[DevtoolsAccessibilityNavigation]: ./navigation.md "Перейдите по Microsoft Edge DevTools с помощью вспомогательных технологий | Документы Майкрософт"  
[DevtoolsCssReferenceViewActuallyAppliedElements]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "Просмотр только CSS, который на самом деле применяется к элементу — CSS Reference | Документы Майкрософт"  

[ChromeWebStoreAxe]: https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US "axe — тестирование веб-доступности — Chrome Web Store"  

[MDNAccessibilityTree]: https://developer.mozilla.org/docs/Glossary/AOM "Дерево доступности (AOM) | MDN"  
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Доступность | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Считыватель | MDN"  

[W3CContrastEnhanced]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-enhanced "Contrast (Enhanced) Level AAA | W3C"  
[W3CContrastMinimum]: https://www.w3.org/WAI/WCAG21/quickref/#contrast-minimum "Контрастный (минимальный) уровень AA | W3C"  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/accessibility/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
