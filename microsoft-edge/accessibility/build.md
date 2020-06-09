---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Чтобы создать общедоступный веб-сайт, пошаговые рекомендации и специальные возможности Интернет-приложений (ARIA) могут быть объединены вместе.
title: Специальные возможности-сборка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Специальные возможности, Специальные возможности для разработчиков, доступные веб-сайты, EDGE, веб-разработка, ARIA, разработчик, модель автоматизации пользовательского интерфейса
ms.custom: seodec18
ms.openlocfilehash: 4412fef6bb78b5a393ccafd5a2cfa79aba223141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570879"
---
# Создание общедоступных веб-сайтов
В Интернете используются динамические и сложные веб-сайты, приложения и пользовательские интерфейсы, созданные с помощью сочетаний HTML, CSS и JavaScript.  Тем не менее, если вы разрабатываете и не заработали специальные возможности, такие сложные веб-сайты будут трудными для людей, использующих [специальные технологии](https://webaim.org/articles/motor/assistive) для просмотра веб-страниц. Для создания веб-сайтов, доступных людям с ограниченными возможностями, требуется семантическая информация о пользовательском интерфейсе. Это позволяет специальным технологиям, например средствам чтения с экрана, передавать необходимые данные, чтобы помочь людям с возможностями, которые могут использовать веб-сайт.

Посетите [HTML5Accessibility](https://html5accessibility.com) , чтобы узнать, какие новые возможности HTML5 accessibly поддерживаются Microsoft Edge.

## Как работает специальные возможности

Специальные возможности – это возможность, чтобы у компьютеров обычно не было. Например, пользователь с ослабленным зрением может использовать клавиатуру в сочетании с технологией специальных возможностей, например средством чтения с экрана, а не непосредственно в браузере с помощью мыши и экрана. Для приложений на платформах Майкрософт и в Интернете специальные возможности взаимодействуют с [автоматизацией пользовательского интерфейса](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)(объектной моделью приложения, например DOM) в Microsoft EDGE или их сочетанием.

Для веб-разработчиков определенные элементы HTML сопоставляются с объектами модели автоматизации пользовательского интерфейса, поэтому при выборе этих элементов HTML разработчик может использовать свойства и события специальных возможностей, встроенные в эти элементы. При разработке веб-сайта обычно необходимо только убедиться, что интерфейс API должен быть правильно написан (или для него указан соответствующий элемент), чтобы приложение было доступно. Для получения дополнительных сведений ознакомьтесь [с возможностями автоматизации пользовательского интерфейса ARIA и UI в Microsoft Edge](./build/ARIA-and-UI-Automation.md) .  Сведения о специальных [возможностях](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) приложений универсальной платформы Windows (UWP) можно найти в разделе Специальные возможности в центре разработки для Windows.

Многие распространенные проблемы с читаемостью, связанные с динамическим содержимым, могут быть направлены на работу с помощью правильного кода, а в документации [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) — большое количество методик и рекомендаций, которые помогут вам создать более доступные динамические веб-приложения. Однако динамический контент не всегда доступен, даже если закодированы должным образом. Этот вопрос можно устранить с помощью [специальных возможностей Интернет-приложений (ARIA)](#aria) .  

Для получения дополнительных сведений о специальных возможностях в Интернете ознакомьтесь со статьей общие сведения о [веб-специальных](https://www.w3.org/WAI/intro/accessibility.php) возможностях [веб-](https://www.w3.org/WAI/) специальных возможностей (помощью ориентиров WAI).

## ВВОДИМ
В соответствии со стандартным [набором](https://www.w3.org/TR/wai-aria/) [веб-приложений, поддерживающим специальные](https://www.w3.org/WAI/) возможности в Интернете, программа W3C's Web Accessibility определяет синтаксис создания динамического веб-контента и специальных пользовательских интерфейсов для всех пользователей. ARIA расширяет HTML с помощью дополнительных атрибутов (ролей, свойств и состояний), предназначенных для передачи настраиваемой семантики. Эти атрибуты используются браузерами для передачи состояния и роли элементов управления API-интерфейсам специальных возможностей.

### Роли, свойства и состояния
Роли ARIA устанавливаются для элементов с помощью [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) атрибута, чтобы предоставить специальные возможности и сведения о специальных возможностях API для элемента. Например, элемент, указанный под элементом "", `<li>` назначается `role="menuitem"` для обозначения элемента в меню.

``` html
<li role="menuitem">Home</li>
```

Состояния ARIA и свойства — это атрибуты префиксов ARIA, которые предоставляют определенные сведения об объекте, которые помогают сформировать определение природы ролей. Свойства — это атрибуты, которые важны для природы объекта, например [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) и [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Изменение свойства влияет на значение объекта. В приведенном ниже примере свойство `aria-haspopup="true"` задано для `<li>` элемента меню, чтобы показать, что у него есть всплывающее окно.

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Состояния не изменяют природу объекта, но представляют данные, связанные с объектом или взаимодействие с пользователем с объектом, например [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) или [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Например, в приведенном `aria-checked="false"` ниже примере состояния флажок не установлен.

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

Чтобы просмотреть полный список ролей, свойств и состояний, перейдите в [модель РОЛЕЙ](https://www.w3.org/TR/wai-aria-1.1/#roles) консорциума W3C.

Дополнительные сведения об ARIA можно найти в разделе [ресурсы](#resources) ARIA.

## Ресурсы

### Основные сведения о специальных возможностях
#### [Проект A11Y](http://a11yproject.com/)
Проект A11Y — это управляемые сообществом усилия для упрощения веб-специальных возможностей. Ознакомьтесь со статьей сайт [проекта A11Y](https://a11yproject.com/) , чтобы узнать об основных принципах доступности, шаблонах специальных возможностей и [библиотеке](https://a11yproject.com/patterns)мини-приложений, а также их [ресурсах](http://a11yproject.com/resources.html) по специальным возможностям, блогам, книгам и инструментам.

#### [Концепция специальных возможностей в Интернете (помощью ОРИЕНТИРОВ WAI)](https://w3.org/WAI/)
Инициатива W3C's Web Accessibility (помощью ОРИЕНТИРОВ WAI) — это усилия, которые помогут вам улучшить доступность веб-сайта. На своем веб-сайте представлены различные ресурсы для [начала работы со специальными возможностями в Интернете](https://www.w3.org/WAI/gettingstarted/Overview.html), [Разработка для включения](https://www.w3.org/WAI/users/Overview.html), [учебников и презентаций](https://www.w3.org/WAI/train.html), а также других возможностей.

### Блоги о специальных возможностях
#### [Группа "Paciello Group"](https://www.paciellogroup.com/blog/)
Группа Paciello Group предоставляет технологические решения для организаций по всему миру, обеспечивая тем самым эффективное и эффективное достижение клиентами всех аудиторий, в то время как правительственные учреждения и международные стандарты. В своем блоге рассматриваются такие темы, как рекомендации по обеспечению специальных возможностей, Специальные возможности и тенденции специальных возможностей.

#### [Простой доступ](http://simplyaccessible.com/articles/)
Простой доступ — это группа специалистов по специальным возможностям, обеспечивающих обучение по специальным возможностям, консультации и многое другое для изменения восприятия специальных возможностей в Интернете. В разделе " [статьи](http://simplyaccessible.com/articles/) " рассматриваются рекомендации по обеспечению доступности веб-страниц, дизайну специальных возможностей и т. д.

#### [Группа SSB BART (SSB)](http://www.ssbbartgroup.com/blog/)
SSB BART Group — это цифровая фирма, поддерживающая клиентов в разработке и развертывании специальных продуктов и служб. Их адреса блога, такие как советы и рекомендации по использованию ARIA, тенденции в специальных возможностях, веб – семинары и многое другое.

### Примеры специальных возможностей
#### [Ally. js — учебники](http://allyjs.io/tutorials/)
Библиотека JavaScript, позволяющая создавать специальные возможности в современных веб-приложениях благодаря упрощению специальных возможностей.

#### [Примеры Heydonworks-ARIA](http://heydonworks.com/practical_aria_examples/)
Примеры использования ARIA для расширения специальных возможностей приложения

#### [Примеры OpenAjax](http://oaa-accessibility.org/)
Веб-сайт OpenAjax Alliance является отличным ресурсом для проверки правил для помощью ОРИЕНТИРОВ WAI-ARIA и содержит несколько примеров реализаций помощью ОРИЕНТИРОВ WAI-ARIA.

#### [Структуру](http://a11yproject.com/patterns.html)
[Проект A11Y](http://a11yproject.com/) содержит библиотеку графических элементов со специальными возможностями и шаблонов, таких как меню, кнопки, всплывающие подсказки и многое другое.

### Технологии специальных возможностей & инструменты
#### [Специальные возможности: создание специальных значков расширений для Microsoft Edge](../extensions/guides/accessibility.md)
Ознакомьтесь с рекомендациями по созданию значков расширенного доступа к Microsoft Edge.

#### [Специальные и описательные имена: вычисление и сопоставление 1,1](https://www.w3.org/TR/accname-1.1/)
В этом документе сопоставления W3C объясняется, как браузеры определяют имена и описания объектов с поддержкой специальных возможностей в интерфейсах веб-содержимого и предоставляют их в API для доступа к данным.

#### [Ресурсы для оценки специальных возможностей](https://www.w3.org/WAI/eval/Overview.html)
Ресурсы для оценки специальных возможностей — это многостраничный ресурс консорциумом W3C, который структурирован различными подходами для оценки веб-сайтов на предмет специальных возможностей.

#### [Тесты на совместимость с технологией специальных возможностей](http://www.powermapper.com/tests/)
Результаты тестов, показывающие поведение различных типов контента и стандартов в специальных возописаниях, например в средствах чтения с экрана.

#### [Создание общедоступных веб-сайтов стало намного проще](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
В этой записи в блоге по веб-разработке и средствам .NET описывается [средство проверки читаемости](https://go.microsoft.com/fwlink/p/?linkid=841539)в расширении Visual Studio.

#### [Базовые сопоставления API специальных возможностей 1,1](https://www.w3.org/TR/core-aam-1.1/)
В этом документе сопоставления W3C объясняется, как семантика языков веб-содержимого предоставляется интерфейсам API для специальных возможностей.  

#### [Простые проверки — первый просмотр специальных возможностей в Интернете](https://www.w3.org/WAI/eval/preliminary.html)
Набор быстрых проверок с помощью помощью ОРИЕНТИРОВ Wai, которые помогут вам Asses специальные возможности веб-страниц.

#### [Как соблюсти вопросы, посвященные рекомендациям WCAG 2,0](https://www.w3.org/WAI/WCAG20/quickref/)
Краткий справочник по требованиям к рекомендациям по специальным возможностям для веб-содержимого (WCAG) 2,0 (условия успеха) и методы.

#### [Сопоставления API для специальных возможностей HTML 1,0](https://www.w3.org/TR/html-aam-1.0/)
В этом документе сопоставления W3C объясняется соответствие элементов и атрибутов HTML 5.1 и API для специальных возможностей платформы.


#### [Краткие советы](http://a11yproject.com/#Quick-tips)
Список быстрых советов по веб-разработке для специальных возможностей [в проекте A11Y](http://a11yproject.com/).

#### [Сканирование сайта](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
Средство сканирования сайта в центре разработки Microsoft Edge проверяет наличие неактуальных библиотек, проблем с разметкой и проблем с читаемостью.

#### [Методики WCAG 2,0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
Методики консорциума W3C, предоставляющие рекомендации для веб-разработчиков по [требованиям по обеспечению доступности](https://w3.org/TR/WCAG20/) веб-содержимого для собраний (WCAG), 2,0 критерии успеха.

#### [Советы по разработке веб-специальных возможностей](https://w3.org/WAI/gettingstarted/tips/developing.html)
Рекомендации консорциума W3C по разработке веб-содержимого, доступного для людей с ограниченными возможностями.

#### [Рекомендации по созданию помощью ОРИЕНТИРОВ WAI-ARIA 1,1](http://w3c.github.io/aria-practices/)
Документ консорциума W3C, который предоставляет читателям понимание того, как использовать помощью ОРИЕНТИРОВ WAI-ARIA 1,1 и рекомендует подходы к внедрению графических элементов, навигации и вариантов поведения с использованием ролей, состояний и свойств помощью ОРИЕНТИРОВ WAI-ARIA.

#### [Рекомендации и методики помощью ОРИЕНТИРОВ WAI](https://w3.org/WAI/guid-tech.html)
Серия руководств и стандартов по обеспечению специальных возможностей в Интернете, разработанных помощью ОРИЕНТИРОВ Wai.  

#### [Список средств оценки специальных возможностей в Интернете](https://www.w3.org/WAI/ER/tools/index.html)
Список средств оценки специальных возможностей в Интернете, которые помогут определить, соответствуют ли веб-сайты требованиям по обеспечению доступности.

#### [Перспективы для веб-специальных возможностей: изучение воздействия и преимуществ для всех](https://w3.org/WAI/perspectives/)
Набор коротких видеороликов согласно РЕКОМЕНДАЦИЯм, посвященным возможностям специальных возможностей и преимуществам для всех.