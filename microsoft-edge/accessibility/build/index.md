---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Чтобы создать доступный веб-сайт, пройдитесь по методу "Лучшие практики" и "Доступные приложения для богатого интернета" (ARIA).
title: Сборка | Доступность
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: доступность, доступность для разработчиков, доступные веб-сайты, края, веб-разработки, ARIA, разработчик, UIA, автоматизация пользовательского интерфейса
ms.custom: seodec18
ms.openlocfilehash: 69f0576b39815708d01477972abad1f8bdc9486e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397890"
---
# <a name="building-accessible-websites"></a>Создание доступных веб-сайтов

Веб-сайт заполнен динамическими и сложными веб-сайтами, приложениями и пользовательскими интерфейсами, построенными с использованием комбинации HTML, CSS и JavaScript.  Однако при конструировании и построении без доступности эти сложные веб-сайты трудно использовать людьми, которые используют вспомогательные технологии для просмотра веб-страниц. [](https://webaim.org/articles/motor/assistive) Создание веб-сайтов, доступных для людей с ограниченными возможностями, требует семантических сведений о пользовательском интерфейсе. Это позволяет вспомогательным технологиям, таким как считыватели экрана, передавать необходимую информацию, чтобы помочь людям с рядом возможностей использовать веб-сайт.

Сведения о том, какие новые функции HTML5 доступны при поддержке Microsoft Edge, посетите [HTML5Accessibility.](https://html5accessibility.com)

## <a name="how-accessibility-works"></a>Работа с доступностью

Вспомогательные технологии добавляют возможности, которые обычно не имеют компьютеры. Например, незрячий пользователь может использовать клавиатуру в сочетании с вспомогательными технологиями, такими как считыватель экрана, а не непосредственно с помощью браузера с помощью мыши и экрана. Для приложений на платформах Майкрософт и в Интернете вспомогательные технологии взаимодействуют с Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), объектной моделью, определенной для приложений, например объектной моделью документа (DOM) в Microsoft Edge или их сочетанием.

Для веб-разработчиков определенные элементы HTML соедуются с объектами автоматизации пользовательского интерфейса, поэтому при выборе этих элементов HTML разработчик может использовать свойства доступности и события, встроенные в эти элементы. При разработке веб-сайта обычно требуется только обеспечить правильное написание API (или задан соответствующий элемент), чтобы приложение было доступным. Дополнительные [сведения можно получить в службе автоматизации ARIA](./ARIA-and-UI-Automation.md) и пользовательского интерфейса в Microsoft Edge.  Сведения о доступных приложениях универсальной платформы Windows (UWP) см. в разделе [Доступность](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) в Центре разработчиков Windows.

Многие распространенные проблемы с динамическим контентом можно решить с помощью хорошей практики кодирования, а документация [по WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) содержит множество методов и методов, которые помогут вам создавать более доступные динамические веб-приложения. Однако даже при правильном кодовом коде динамическое содержимое не обязательно доступно. Эту проблему можно решить с помощью доступных приложений с богатым доступом к Интернету [(ARIA).](#aria)  

Дополнительные сведения о доступности веб-сайтов см. в странице [Введение](https://www.w3.org/WAI/intro/accessibility.php) в веб-доступность по инициативе [веб-доступности (WAI).](https://www.w3.org/WAI)

## <a name="aria"></a>ARIA

[Спецификация](https://www.w3.org/TR/wai-aria/) доступных приложений с богатым доступом в Интернет [](https://www.w3.org/WAI/) (ARIA) инициативы W3C по веб-доступности определяется как синтаксис для создания динамического веб-контента и пользовательских интерфейсов доступными для всех пользователей. ARIA расширяет HTML с помощью дополнительных атрибутов (ролей, свойств и состояния), предназначенных для передачи настраиваемой семантики. Эти атрибуты используются браузерами для того, чтобы передать состояние и роль элементов управления API доступности.

### <a name="roles-properties-and-states"></a>Роли, свойства и состояния

Роли ARIA устанавливаются на элементы, использующие атрибут для передачи вспомогательных технологий и API доступности сведений [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) об элементе. Например, ниже задается элемент, который означает, что это элемент `<li>` `role="menuitem"` в меню.

```html
<li role="menuitem">Home</li>
```

Состояния и свойства ARIA — это атрибуты с префиксом арии, которые предоставляют определенную информацию об объекте, чтобы помочь сформировать определение природы ролей. Свойства — это атрибуты, которые имеют важное значение для природы объекта, например [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) и [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Изменение свойства влияет на значение объекта. В приведенной ниже примере свойство задавалось элементу меню, чтобы у него было `aria-haspopup="true"` `<li>` всплывающее всплывающее.

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Состояния не изменяют природу объекта, а представляют сведения, связанные с объектом или взаимодействием пользователя с объектом, например [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) или [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Например, состояние в приведенной ниже примере означает, что контрольный `aria-checked="false"` ящик не проверяется.

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

Перейдите [к модели ролей](https://www.w3.org/TR/wai-aria-1.1/#roles) w3C, чтобы увидеть полный список ролей, свойств и состояния.

Дополнительные сведения об ARIA перейдите к ARIA в разделе [Ресурсы.](#resources)

## <a name="assistive-technology-compatibility-testing"></a>Тестирование совместимости вспомогательных технологий  

Проверка того, что веб-сайт, который вы строите, работает с реальными вспомогательными технологиями, является лучшим способом обеспечения хорошего опыта для пользователей с ограниченными возможностями.  Так как многие вспомогательные технологии используют клавиатуру, тестирование доступности клавиатуры веб-сайта является хорошим местом для начала.  [Тестирование совместимости клавиатуры][W3cPerspectiveVideosKeyboard] подтверждает, что пользователи имеют доступ ко всем интерактивным средствам управления без необходимости использования мыши.  Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] — это расширение браузера для Microsoft Edge и Chrome, которое направляет вас и выявляет несколько распространенных проблем.  

После того как вы уверены, что ваш веб-сайт хорошо работает с клавиатурой, попробуйте его с другими вспомогательными технологиями, такими как считыватели экрана.  Он выявляет проблемы в следующем.

*   HTML, ARIA и CSS.  
*   Уровень поддержки вспомогательных технологий для функции или техники.  
    
Различные браузеры могут отрисовки элементов для API доступности платформы по-другому, чем Microsoft Edge.  При создании интерфейса важно учитывать каждое различие.  

WebAIM проводит опросы [][WebaimProjectsScreenreadersurvey8] с [][WebaimProjectsLowvisionsurvey2] помощью чтения с экрана и пользователей с низким зрением, которые помогут вам определить, какие вспомогательные технологии и браузеры необходимо протестировать.  

### <a name="learning-how-to-test"></a>Обучение проверке  

Вспомогательные технологии — это сложные средства.  Не думайте, что вы можете немедленно приступить к тестированию с помощью вспомогательных технологий, не узнав о том, как это работает.  Обучение проверке с помощью чтения с экрана имеет особенно крутую кривую обучения.  Начинающий пользователь чтения экрана может предположить, что ошибка чтения экрана произошла, когда проблема связана с ненадлежащим использованием чтения экрана.  

Дополнительные сведения о том, как научиться тестировать с помощью вспомогательных технологий, перейдите к [тестированию][WebaimArticlesScreenreaderTesting] с помощью чтения с экрана в WebAIM.  

### <a name="testing-locally"></a>Локальное тестирование  

Большинство устройств включают вспомогательные технологии, встроенные в ОС.  Microsoft Windows включает в себя [считыватель экрана с рассказчиком Windows][MicrosoftSupport22798] и Windows [Magnifier.][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]  Доступны сторонние вспомогательные технологии, такие как [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]и [ZoomText.][FreedomscientificSoftwareZoomtext]  MacOS Apple включает [считыватель экрана VoiceOver.][AppleAccessibilityMacVision]  А iOS, Android и Linux поддерживают различные вспомогательные технологии.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Тестирование в виртуальных машинах и эмуляторах  

В macOS, если вы хотите протестировать с помощью вспомогательных технологий, доступных только для Windows, таких как Windows Narrator или NVDA, создайте виртуальную машину Windows.  Виртуальные машины с Microsoft Edge \(EdgeHTML\) и IE доступны для VirtualBox и VMWare на странице загрузки [виртуальных машин.][MicrosoftDeveloperEdgeVms]  

[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] включает эмулятор, который для тестирования вспомогательных технологий в [пакете доступности Android.][GooglePlayStoreAndroidAccessibilitySuite]  Следуйте инструкциям по установке [виртуального устройства][AndroidDeveloperDevicesManagingAvdsHtml] и запуску [эмулятора,][AndroidDeveloperDevicesEmulatorHtml]а затем установите пакет доступности [Android][GooglePlayStoreAndroidAccessibilitySuite] из магазина GooglePlay.  

> [!NOTE]
> Симулятор iOS в настоящее время не включает VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Облачные средства тестирования  

Если вспомогательные технологии недоступны на оси или не удалось установить ее на виртуальной машине или эмуляторе, средства тестирования вспомогательных технологий на облачной основе — это следующая лучшая вещь.  

*   [Assistiv Labs (коммерческий)][AssistivlabsMain] позволяет вручную тестировать с помощью вспомогательных технологий с помощью любого современного веб-браузера.  Выберите вспомогательные технологии и браузер и соединит вас с виртуальной машиной, эмулятором или реальным устройством, с которым вы можете взаимодействовать.  

## <a name="resources"></a>Ресурсы

### <a name="accessibility-basics"></a>Основы доступности

#### [<a name="the-a11y-project"></a>Проект A11Y](http://a11yproject.com/)

Проект A11Y — это работа, направленная на решение задач по упростить доступ к веб-сайтам. Ознакомьтесь с сайтом [A11Y Project,](https://a11yproject.com/) чтобы узнать об основных принципах доступности, их доступной библиотеке шаблонов и виджетов [и](https://a11yproject.com/patterns)их ресурсах в программном обеспечении, блогах, книгах и средствах. [](http://a11yproject.com/resources.html)

#### [<a name="web-accessibility-initiative-wai"></a>Инициатива по веб-доступности (WAI)](https://w3.org/WAI/)

Инициатива W3C по веб-доступности (WAI) — это усилия по улучшению доступности интернета. Их сайт предоставляет различные [](https://www.w3.org/WAI/gettingstarted/Overview.html)ресурсы для начала работы с веб-доступностью, [проектирование](https://www.w3.org/WAI/users/Overview.html)для включения, учебники и [презентации](https://www.w3.org/WAI/train.html)и другие.

### <a name="accessibility-blogs"></a>Блоги доступности

#### [<a name="the-paciello-group"></a>Группа Paciello](https://www.paciellogroup.com/blog/)

Группа Paciello предоставляет консультационные и технологические решения организациям по всему миру, чтобы обеспечить эффективное и эффективное охват клиентов всеми аудиториями при одновременном обеспечении правительственных и международных стандартов. Их блог охватывает такие темы, как лучшие практики, средства доступности и тенденции доступности веб-доступа.

#### [<a name="simply-accessible"></a>Просто доступно](http://simplyaccessible.com/articles/)

Simply Accessible — это команда специалистов по доступности, предоставляющих обучение, консультации и другие возможности для изменения восприятия доступности в Интернете. В [разделе Статьи](http://simplyaccessible.com/articles/) обсуждаются лучшие практики для веб-доступности, доступной разработки и других.

#### [<a name="ssb-bart-group-ssb"></a>Группа SSB BART (SSB)](http://www.ssbbartgroup.com/blog/)

SSB BART Group — это фирма по цифровой доступности, которая поддерживает своих клиентов в разработке и развертывании доступных продуктов и служб. Их блог адресов темы, как ARIA передовая практика, тенденции доступности, веб-инары и другие.

### <a name="accessible-examples"></a>Доступные примеры

#### [<a name="allyjs---tutorials"></a>ally.js - Учебники](http://allyjs.io/tutorials/)

Библиотека JavaScript, помогая современным веб-приложениям с проблемой доступности, упростив доступность.

#### [<a name="heydonworks---aria-examples"></a>Heydonworks — примеры ARIA](http://heydonworks.com/practical_aria_examples/)

Примеры практической ARIA для повышения доступности приложений

#### [<a name="openajax-examples"></a>Примеры OpenAjax](http://oaa-accessibility.org/)

Веб-сайт Альянса OpenAjax — это отличный ресурс для проверки правил WAI-ARIA и содержит ряд примеров реализации WAI-ARIA.

#### [<a name="patterns"></a>Шаблоны](http://a11yproject.com/patterns.html)

[Проект A11Y](http://a11yproject.com/) предлагает библиотеку доступных виджетов и шаблонов, таких как меню, кнопки, панели инструментов и другие.

### <a name="accessibility-techniques--tools"></a>Методы доступности & средства

#### [<a name="accessibility-creating-accessible-extension-icons-for-microsoft-edge"></a>Доступность: создание доступных значков расширения для Microsoft Edge](../../edgehtml/extensions/guides/accessibility.md)

Получите руководство по созданию значков доступных расширений для Microsoft Edge.

#### [<a name="accessible-name-and-description-computation-and-mappings-11"></a>Доступное имя и описание: вычисления и сопоставления 1.1](https://www.w3.org/TR/accname-1.1/)

В этом документе сопоставления W3C объясняется, как браузеры определяют имена и описания доступных объектов из языков веб-контента и раскрывают их в API доступности.

#### [<a name="accessibility-evaluation-resources"></a>Ресурсы оценки доступности](https://www.w3.org/WAI/eval/Overview.html)

Ресурсы оценки доступности — это многоуровневый ресурс W3C, который описывает различные подходы к оценке доступности веб-сайтов.

#### [<a name="assistive-technology-compatibility-tests"></a>Тесты совместимости вспомогательных технологий](http://www.powermapper.com/tests/)

Результаты тестирования, показывающие, как различные типы контента и стандарты ведут себя в вспомогательных технологиях (AT) как считыватели экрана.

#### [<a name="building-accessible-websites-just-got-a-lot-easier"></a>Создание доступных веб-сайтов стало намного проще](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

В этом блоге веб-разработки и инструментов .NET описывается Visual Studio проверки доступности [веб-сайтов.](https://go.microsoft.com/fwlink/p/?linkid=841539)

#### [<a name="core-accessibility-api-mappings-11"></a>Сопоставление API API основных возможностей 1.1](https://www.w3.org/TR/core-aam-1.1/)

В этом документе сопоставления W3C объясняется, как семантика языков веб-контента подвергается воздействию API доступности.  

#### [<a name="easy-checks--a-first-review-of-web-accessibility"></a>Простые проверки — первый обзор веб-доступности](https://www.w3.org/WAI/eval/preliminary.html)

Серия быстрых проверок WAI, которые помогут вам определить доступность веб-страницы.

#### [<a name="how-to-meet-wcag-20"></a>Как выполнить WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref/)

Быстрая ссылка на рекомендации по доступности веб-контента (WCAG) 2.0 (критерии успешности) и методы.

#### [<a name="html-accessibility-api-mappings-10"></a>Сопоставления API API доступности HTML 1.0](https://www.w3.org/TR/html-aam-1.0/)

В этом документе сопоставления W3C объясняется, как элемент HTML5.1 и атрибуты сопоставления с API доступности платформы.

#### [<a name="quick-tips"></a>Краткие советы](http://a11yproject.com/#Quick-tips)

Список советов по быстрому веб-разработке для доступности [проекта A11Y.](http://a11yproject.com/)

#### [<a name="site-scan"></a>Сканирование сайта](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

Средство сканирования сайтов в Центре разработчиков Microsoft Edge проверяет наличие устарелих библиотек, проблем макета и проблем с доступностью.

#### [<a name="techniques-for-wcag-20"></a>Методы для WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

Методы W3C, которые предоставляют рекомендации для веб-разработчиков по встрече с Рекомендациями по доступности веб-контента [(WCAG) 2.0](https://w3.org/TR/WCAG20/) критериев успешности.

#### [<a name="tips-on-developing-for-web-accessibility"></a>Советы по разработке для веб-доступности](https://w3.org/WAI/gettingstarted/tips/developing.html)

Советы W3C по разработке веб-контента, доступного для людей с ограниченными возможностями.

#### [<a name="wai-aria-authoring-practices-11"></a>WAI-ARIA Authoring Practices 1.1](http://w3c.github.io/aria-practices/)

Документ W3C, который предоставляет читателям представление об использовании WAI-ARIA 1.1 и рекомендует подходы, чтобы сделать виджеты, навигацию и поведение доступными с помощью ролей, состояния и свойств WAI-ARIA.

#### [<a name="wai-guidelines-and-techniques"></a>Рекомендации и методы WAI](https://w3.org/WAI/guid-tech.html)

Серия рекомендаций и стандартов веб-доступности, разработанных WAI.  

#### [<a name="web-accessibility-evaluation-tools-list"></a>Список инструментов оценки доступности веб-сайтов](https://www.w3.org/WAI/ER/tools/index.html)

Список средств оценки доступности веб-сайтов, которые помогут определить, соответствуют ли веб-сайты рекомендациям по доступности.

#### [<a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Перспективы веб-доступности: изучение влияния и преимуществ для всех](https://w3.org/WAI/perspectives/)

Серия коротких сиюмитных видео W3C о влиянии доступности и преимуществах для всех.

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Виртуальные | Microsoft Edge Developer"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Полное руководство по | Поддержка Майкрософт"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Используйте Magnifier, чтобы сделать вещи на экране более легкими для | Поддержка Майкрософт"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Сведения о доступности для веб-| Сведения о доступности"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Создание и управление виртуальными устройствами | Разработчики Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Запустите приложения в эмуляторе Android | Разработчики Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Скачать Android Studio | Разработчики Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Доступность зрения — Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Assistiv Labs"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Freedom Scientific"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freedom Scientific"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Набор доступности Для Android | Магазин GooglePlay"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "О NVDA | Доступ к NV"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Совместимость клавиатуры | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Опрос пользователей с низким зрением \#2 результаты | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Обзор пользователей screen Reader \#8 результаты | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Тестирование с помощью | WebAIM"  
