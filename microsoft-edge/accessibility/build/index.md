---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Пойдите по всем методикам и приложениям ARIA, чтобы создать доступный веб-сайт.
title: Сборка | Доступность
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accessibility, accessibility for developers, accessible websites, edge, web development, ARIA, developer, UIA, UI Automation
ms.custom: seodec18
ms.openlocfilehash: 40ab1acd0b5356ad4696cde0762f656708a67890
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235279"
---
# <span data-ttu-id="d244d-104">Создание доступных веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="d244d-104">Building Accessible Websites</span></span>

<span data-ttu-id="d244d-105">Веб-сайт заполняется динамическими и сложными веб-сайтами, приложениями и пользовательскими интерфейсами, построенными на основе HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d244d-105">The web is filled with dynamic and complex websites, applications, and user interfaces built using a combination of HTML, CSS, and JavaScript.</span></span>  <span data-ttu-id="d244d-106">Однако при конструировании и построении без использования специальности эти сложные [](https://webaim.org/articles/motor/assistive) веб-сайты сложно использовать людям, которые используют вспомогательные технологии для просмотра веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="d244d-106">However, when designed and built without accessibility in mind, these complex websites are difficult to use by people who rely on [assistive technologies](https://webaim.org/articles/motor/assistive) to browse the web.</span></span> <span data-ttu-id="d244d-107">Для создания веб-сайтов, доступных людям с ограниченными возможностями, требуется семантическая информация об пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d244d-107">Building websites that are accessible to people with disabilities requires semantic information about the user interface.</span></span> <span data-ttu-id="d244d-108">Это позволяет вспомогательным технологиям, таким как средства чтения с экрана, передавать необходимую информацию, чтобы помочь пользователям с разнообразными возможностями использовать веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="d244d-108">This allows for assistive technologies, like screen readers, to convey the necessary information to help people with a range of abilities use the website.</span></span>

<span data-ttu-id="d244d-109">Сведения о том, какие новые функции HTML5 доступны в Microsoft Edge, можно получить на сайте [HTML5Accessibility.](https://html5accessibility.com)</span><span class="sxs-lookup"><span data-stu-id="d244d-109">Visit [HTML5Accessibility](https://html5accessibility.com) for information on which new HTML5 features are accessibly supported by Microsoft Edge.</span></span>

## <span data-ttu-id="d244d-110">Как работает accessibility</span><span class="sxs-lookup"><span data-stu-id="d244d-110">How Accessibility Works</span></span>

<span data-ttu-id="d244d-111">Вспомогательные технологии добавляют возможности, которые обычно не имеются на компьютерах.</span><span class="sxs-lookup"><span data-stu-id="d244d-111">Assistive technologies add capabilities that computers don't usually have.</span></span> <span data-ttu-id="d244d-112">Например, пользователь с нарушениями зрения может использовать клавиатуру в сочетании с такими вспомогательными технологиями, как устройство чтения с экрана, а не непосредственно с помощью браузера с мышью и экраном.</span><span class="sxs-lookup"><span data-stu-id="d244d-112">For example, a visually impaired user might use their keyboard in combination with assistive technology such as a screen reader, rather than directly using the browser with the mouse and screen.</span></span> <span data-ttu-id="d244d-113">Для приложений на платформах Майкрософт и в Интернете специальные возможности взаимодействуют с [автоматизацией](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)пользовательского интерфейса Майкрософт , объектной моделью для конкретного приложения, такой как модель doM в Microsoft Edge, или их сочетанием.</span><span class="sxs-lookup"><span data-stu-id="d244d-113">For applications on Microsoft platforms and on the web, the assistive technology interacts with Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), an application-specific object model such as the Document Object Model (DOM) in Microsoft Edge, or a combination of these.</span></span>

<span data-ttu-id="d244d-114">Для веб-разработчиков определенные элементы HTML соедуются с объектами автоматизации пользовательского интерфейса, поэтому при выборе этих элементов HTML разработчик может использовать свойства и события, встроенные в эти элементы.</span><span class="sxs-lookup"><span data-stu-id="d244d-114">For web developers, certain HTML elements are mapped to UI Automation objects, so in selecting those HTML elements, the developer can use the accessibility properties and events built in to those elements.</span></span> <span data-ttu-id="d244d-115">При разработке веб-сайта обычно требуется только обеспечить правильную написание API (или указан соответствующий элемент), чтобы приложение было доступно.</span><span class="sxs-lookup"><span data-stu-id="d244d-115">While developing your website, you usually only need to be concerned with ensuring that the API is correctly written to (or that the appropriate element is specified), in order for the application to be accessible.</span></span> <span data-ttu-id="d244d-116">Дополнительные сведения можно узнать в ARIA и автоматизации пользовательского [интерфейса в Microsoft Edge.](./ARIA-and-UI-Automation.md)</span><span class="sxs-lookup"><span data-stu-id="d244d-116">Check out [ARIA and UI Automation in Microsoft Edge](./ARIA-and-UI-Automation.md) for more information.</span></span>  <span data-ttu-id="d244d-117">Сведения о доступных приложениях универсальной платформы Windows [](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) (UWP) см. в разделе "Доступность" в Центре разработчиков для Windows.</span><span class="sxs-lookup"><span data-stu-id="d244d-117">For information on accessible Universal Windows Platform (UWP) apps, see the [Accessibility](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) topic in the Windows Dev Center.</span></span>

<span data-ttu-id="d244d-118">Многие распространенные проблемы с доступом к динамическому контенту можно решить с помощью хорошего метода кодирования, а документация [по WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) содержит множество методов и практических методик, которые помогут вам создать более доступные динамические веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d244d-118">Many common accessibility issues with dynamic content can be addressed by good coding practice, and the [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) documentation includes many techniques and best practices to help you create more accessible dynamic web applications.</span></span> <span data-ttu-id="d244d-119">Однако даже при правильном коде динамический контент не обязательно доступен.</span><span class="sxs-lookup"><span data-stu-id="d244d-119">Even when coded properly, however, dynamic content is not necessarily accessible.</span></span> <span data-ttu-id="d244d-120">[Доступные приложения ARIA помогают](#aria) решить эту проблему.</span><span class="sxs-lookup"><span data-stu-id="d244d-120">[Accessible Rich Internet Applications (ARIA)](#aria) helps overcome this issue.</span></span>  

<span data-ttu-id="d244d-121">Дополнительные сведения о веб-доступности [](https://www.w3.org/WAI/intro/accessibility.php) см. в подзаголовок "Введение в веб-доступность" в рамках инициативы по веб-специальным [данным](https://www.w3.org/WAI/) (WAI).</span><span class="sxs-lookup"><span data-stu-id="d244d-121">For more information on web accessibility, check out the [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative](https://www.w3.org/WAI/) (WAI).</span></span>

## <span data-ttu-id="d244d-122">ARIA</span><span class="sxs-lookup"><span data-stu-id="d244d-122">ARIA</span></span>

<span data-ttu-id="d244d-123">Спецификация ARIA (Accessible [Rich Internet Applications,](https://www.w3.org/TR/wai-aria/) ARIA) в рамках инициативы по веб-специальным данным W3C определяется как синтаксис для создания динамического веб-контента и пользовательских интерфейсов, доступных всем пользователям. [](https://www.w3.org/WAI/)</span><span class="sxs-lookup"><span data-stu-id="d244d-123">The [Accessible Rich Internet Applications](https://www.w3.org/TR/wai-aria/) (ARIA) specification by the W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) defines as a syntax for making dynamic web content and custom user interfaces accessible to all people.</span></span> <span data-ttu-id="d244d-124">ARIA расширяет HTML, используя дополнительные атрибуты (роли, свойства и состояния), предназначенные для передачи пользовательской семантики.</span><span class="sxs-lookup"><span data-stu-id="d244d-124">ARIA extends HTML by using additional attributes (roles, properties, and states) that are designed to convey custom semantics.</span></span> <span data-ttu-id="d244d-125">Эти атрибуты используются браузерами для передать состояние и роль элементов управления в API доступности.</span><span class="sxs-lookup"><span data-stu-id="d244d-125">These attributes are used by browsers to pass along the controls' state and role to the accessibility API.</span></span>

### <span data-ttu-id="d244d-126">Роли, свойства и состояния</span><span class="sxs-lookup"><span data-stu-id="d244d-126">Roles, Properties, and States</span></span>

<span data-ttu-id="d244d-127">Роли ARIA устанавливаются для элементов с использованием атрибута, чтобы предоставить вспомогательные технологии и API-API для доступа к [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) элементу.</span><span class="sxs-lookup"><span data-stu-id="d244d-127">ARIA roles are set on elements using the [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribute to give assistive technologies and accessibility APIs information about the element.</span></span> <span data-ttu-id="d244d-128">Например, приведенное ниже элемент назначено для знака его `<li>` `role="menuitem"` элемента в меню.</span><span class="sxs-lookup"><span data-stu-id="d244d-128">For example, the below `<li>` element is assigned `role="menuitem"` to signify it's an item in a menu.</span></span>

```html
<li role="menuitem">Home</li>
```

<span data-ttu-id="d244d-129">Состояния и свойства ARIA — это атрибуты с префиксом aria, которые предоставляют определенную информацию об объекте для формирования определения природы ролей.</span><span class="sxs-lookup"><span data-stu-id="d244d-129">ARIA states and properties are aria-prefixed attributes that provide specific information about an object to help form the definition of the nature of roles.</span></span> <span data-ttu-id="d244d-130">Свойства — это атрибуты, необходимые для природы объекта, например [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) и [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="d244d-130">Properties are attributes that are essential to the nature of an object, like [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) and [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx).</span></span> <span data-ttu-id="d244d-131">Изменение свойства влияет на значение объекта.</span><span class="sxs-lookup"><span data-stu-id="d244d-131">Changing a property affects the meaning of the object.</span></span> <span data-ttu-id="d244d-132">В примере ниже свойство устанавливается в элементе меню, чтобы у него было `aria-haspopup="true"` `<li>` всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="d244d-132">In the example below, the property `aria-haspopup="true"` is set on a `<li>` menu item to signify it has a popup.</span></span>

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

<span data-ttu-id="d244d-133">Состояния не изменяют природу объекта, но представляют сведения, связанные с объектом или взаимодействием пользователя с объектом, например [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) или [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="d244d-133">States do not change the nature of the object, but represent information associated with the object or user interaction with the object, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) or [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx).</span></span> <span data-ttu-id="d244d-134">Например, состояние в примере ниже означает, что этот контрольный ящик `aria-checked="false"` не проверяется.</span><span class="sxs-lookup"><span data-stu-id="d244d-134">For example, the state `aria-checked="false"` in the example below represents that the checkbox is not checked.</span></span>

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

<span data-ttu-id="d244d-135">Перейдите [в модель ролей](https://www.w3.org/TR/wai-aria-1.1/#roles) W3C, чтобы увидеть полный список ролей, свойств и состояния.</span><span class="sxs-lookup"><span data-stu-id="d244d-135">Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.</span></span>

<span data-ttu-id="d244d-136">Дополнительные сведения об ARIA см. [](#resources) в разделе "Ресурсы" по ARIA.</span><span class="sxs-lookup"><span data-stu-id="d244d-136">For more information on ARIA, see the ARIA in the [Resources](#resources) section.</span></span>

## <span data-ttu-id="d244d-137">Тестирование совместимости с вспомогательными технологиями</span><span class="sxs-lookup"><span data-stu-id="d244d-137">Assistive Technology Compatibility Testing</span></span>  

<span data-ttu-id="d244d-138">Проверка того, что веб-сайт, который вы строите, работает с реальными вспомогательными технологиями, — это лучший способ обеспечить хорошее впечатление для пользователей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="d244d-138">Verifying that the website you are building works with real assistive technologies is the best way to ensure a good experience for your users with disabilities.</span></span>  <span data-ttu-id="d244d-139">Так как многие вспомогательные технологии используют клавиатуру, тестирование возможностей клавиатуры на вашем веб-сайте является хорошим местом для начала.</span><span class="sxs-lookup"><span data-stu-id="d244d-139">Since many assistive technologies make use of the keyboard, testing the keyboard accessibility of your website is a good place to start.</span></span>  <span data-ttu-id="d244d-140">[Тестирование совместимости клавиатуры][W3cPerspectiveVideosKeyboard] проверяет, есть ли у пользователей доступ ко всем интерактивным средствам управления без использования мыши.</span><span class="sxs-lookup"><span data-stu-id="d244d-140">[Keyboard compatibility testing][W3cPerspectiveVideosKeyboard] validates that users have access to all interactive controls without requiring a mouse.</span></span>  <span data-ttu-id="d244d-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] — это расширение браузера для Microsoft Edge и Chrome, которое поможет вам и покажет несколько распространенных проблем.</span><span class="sxs-lookup"><span data-stu-id="d244d-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] is a browser extension for Microsoft Edge and Chrome that guides you and reveals several common issues.</span></span>  

<span data-ttu-id="d244d-142">После того как вы уверены, что ваш веб-сайт хорошо работает с клавиатурой, попробуйте его с другими вспомогательными технологиями, такими как устройства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="d244d-142">Once you are confident that your website works well with a keyboard, try it with other assistive technologies, such as screen readers.</span></span>  <span data-ttu-id="d244d-143">Он выявляет проблемы в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d244d-143">It uncover issues in the following.</span></span>

*   <span data-ttu-id="d244d-144">HTML, ARIA и CSS.</span><span class="sxs-lookup"><span data-stu-id="d244d-144">Your HTML, ARIA, and CSS.</span></span>  
*   <span data-ttu-id="d244d-145">Уровень поддержки вспомогательных технологий для функций или методов.</span><span class="sxs-lookup"><span data-stu-id="d244d-145">The level of support of an assistive technology for a feature or technique.</span></span>  
    
<span data-ttu-id="d244d-146">Различные браузеры могут сопооставить элементы с API доступности платформы иначе, чем Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d244d-146">Different browsers may map elements to platform accessibility APIs differently than Microsoft Edge.</span></span>  <span data-ttu-id="d244d-147">При создании интерфейса важно учитывать все различия.</span><span class="sxs-lookup"><span data-stu-id="d244d-147">While building your interface, it is important to consider each difference.</span></span>  

<span data-ttu-id="d244d-148">WebAIM проводит опросы [][WebaimProjectsScreenreadersurvey8] с [][WebaimProjectsLowvisionsurvey2] помощью устройства чтения с экрана и пользователей с низким зрением, которые помогут вам определить, какие вспомогательные технологии и браузеры вы хотите протестировать.</span><span class="sxs-lookup"><span data-stu-id="d244d-148">WebAIM conducts surveys with [screen reader][WebaimProjectsScreenreadersurvey8] and [low vision][WebaimProjectsLowvisionsurvey2] users that help you decide which assistive technologies and browsers you want to test.</span></span>  

### <span data-ttu-id="d244d-149">Обучение проверке</span><span class="sxs-lookup"><span data-stu-id="d244d-149">Learning How to Test</span></span>  

<span data-ttu-id="d244d-150">Вспомогательные технологии — это сложные инструменты.</span><span class="sxs-lookup"><span data-stu-id="d244d-150">Assistive technologies are sophisticated tools.</span></span>  <span data-ttu-id="d244d-151">Не предполагайте, что вы можете сразу же начать тестирование с помощью вспомогательных технологий, не изучив их работу.</span><span class="sxs-lookup"><span data-stu-id="d244d-151">Do not assume that you are able to immediately start testing with an assistive technology without first learning about how it works.</span></span>  <span data-ttu-id="d244d-152">При обучении тесту с помощью чтения с экрана особенно важно научиться.</span><span class="sxs-lookup"><span data-stu-id="d244d-152">Learning to test with a screen reader has an especially steep learning curve.</span></span>  <span data-ttu-id="d244d-153">Пользователь, читаюющий экран, может предположить, что произошла ошибка чтения с экрана, когда проблема связана с ненадлежащим использованием этого устройства.</span><span class="sxs-lookup"><span data-stu-id="d244d-153">A novice screen reader user may assume that a screen reader bug has occurred while the issue is related to misuse of the screen reader.</span></span>  

<span data-ttu-id="d244d-154">Дополнительные сведения об обучении тестированию с помощью вспомогательных технологий можно найти на странице ["Тестирование][WebaimArticlesScreenreaderTesting] с помощью чтения с экрана" на веб-сайте WebAIM.</span><span class="sxs-lookup"><span data-stu-id="d244d-154">For more information about learning to test with assistive technologies, navigate to [Testing with Screen Readers][WebaimArticlesScreenreaderTesting] on WebAIM.</span></span>  

### <span data-ttu-id="d244d-155">Локальное тестирование</span><span class="sxs-lookup"><span data-stu-id="d244d-155">Testing Locally</span></span>  

<span data-ttu-id="d244d-156">Большинство устройств включают в себя вспомогательные средства, встроенные в ОС.</span><span class="sxs-lookup"><span data-stu-id="d244d-156">Most devices include assistive technology that is built-in to the OS.</span></span>  <span data-ttu-id="d244d-157">Microsoft Windows включает в себя экранный [диктор Windows][MicrosoftSupport22798] и [экранную лупу Windows.][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]</span><span class="sxs-lookup"><span data-stu-id="d244d-157">Microsoft Windows includes the [Windows Narrator][MicrosoftSupport22798] screen reader and [Windows Magnifier][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span></span>  <span data-ttu-id="d244d-158">Сторонние вспомогательные технологии, такие как [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]и [ZoomText,][FreedomscientificSoftwareZoomtext] доступны для скачивания.</span><span class="sxs-lookup"><span data-stu-id="d244d-158">3rd party assistive technologies like [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws], and [ZoomText][FreedomscientificSoftwareZoomtext] are available to download.</span></span>  <span data-ttu-id="d244d-159">Apple macOS включает в себя устройство чтения с экрана [VoiceOver.][AppleAccessibilityMacVision]</span><span class="sxs-lookup"><span data-stu-id="d244d-159">Apple macOS includes the [VoiceOver][AppleAccessibilityMacVision] screen reader.</span></span>  <span data-ttu-id="d244d-160">IOS, Android и Linux поддерживают различные вспомогательные технологии.</span><span class="sxs-lookup"><span data-stu-id="d244d-160">And iOS, Android, and Linux all support a variety of assistive technologies.</span></span>  

### <span data-ttu-id="d244d-161">Тестирование на виртуальных машинах и эмуляторах</span><span class="sxs-lookup"><span data-stu-id="d244d-161">Testing in Virtual Machines and Emulators</span></span>  

<span data-ttu-id="d244d-162">Если в macOS вы хотите протестировать возможности, доступные только для Windows, например, с помощью диктора Windows или NVDA, создайте виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="d244d-162">Under macOS, if you want to test with an assistive technology only available for Windows, like Windows Narrator or NVDA, create a Windows virtual machine.</span></span>  <span data-ttu-id="d244d-163">Виртуальные машины с Microsoft Edge \(EdgeHTML\) и IE доступны для VirtualBox и VMWare на странице загрузки [виртуальных машин.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="d244d-163">Virtual machines with Microsoft Edge \(EdgeHTML\) and IE are available for VirtualBox and VMWare on the [Virtual Machines download page][MicrosoftDeveloperEdgeVms].</span></span>  

<span data-ttu-id="d244d-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] включает эмулятор, который поможет вам протестировать вспомогательные технологии в [наборе accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite]для Android.</span><span class="sxs-lookup"><span data-stu-id="d244d-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] includes an emulator that for you to test assistive technologies in the [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite].</span></span>  <span data-ttu-id="d244d-165">Следуйте инструкциям по [установке виртуального][AndroidDeveloperDevicesManagingAvdsHtml] устройства и запуску эмулятора, [][AndroidDeveloperDevicesEmulatorHtml]а затем установите пакет [accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] для Android из магазина GooglePlay.</span><span class="sxs-lookup"><span data-stu-id="d244d-165">Follow the instructions to [set up a virtual device][AndroidDeveloperDevicesManagingAvdsHtml] and [start the emulator][AndroidDeveloperDevicesEmulatorHtml], then install [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] from the GooglePlay store.</span></span>  

> [!NOTE]
> <span data-ttu-id="d244d-166">Имитатор iOS в настоящее время не включает VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="d244d-166">The iOS Simulator does not currently include VoiceOver.</span></span>  

### <span data-ttu-id="d244d-167">Облачные средства тестирования</span><span class="sxs-lookup"><span data-stu-id="d244d-167">Cloud-based Testing Tools</span></span>  

<span data-ttu-id="d244d-168">Если в вашей ОС отсутствует доступная технология или ее невозможно установить на виртуальной машине или эмуляторе, лучше всего использовать облачные средства тестирования.</span><span class="sxs-lookup"><span data-stu-id="d244d-168">If an assistive technology is not available on your OS or you not possible to install one on a virtual machine or emulator, cloud-based assistive technology testing tools are the next best thing.</span></span>  

*   <span data-ttu-id="d244d-169">[Лаборатории assistiv (коммерческие)][AssistivlabsMain] позволяют вручную тестировать вспомогательные технологии с помощью любого современного веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="d244d-169">[Assistiv Labs (commercial)][AssistivlabsMain] enables you to manually test with assistive technologies through any modern web browser.</span></span>  <span data-ttu-id="d244d-170">Выберите технологию и браузер, который связывает вас с виртуальной машиной, эмулятором или реальным устройством, с которым вы можете взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="d244d-170">Choose an assistive technology and browser and it connects you with a virtual machine, emulator, or real device with which you may interact.</span></span>  

## <span data-ttu-id="d244d-171">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="d244d-171">Resources</span></span>

### <span data-ttu-id="d244d-172">Основы доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-172">Accessibility Basics</span></span>

#### [<span data-ttu-id="d244d-173">Проект A11Y</span><span class="sxs-lookup"><span data-stu-id="d244d-173">The A11Y Project</span></span>](http://a11yproject.com/)

<span data-ttu-id="d244d-174">Проект A11Y — это проект, который управляется сообществом, чтобы упростить работу с веб-приложениями.</span><span class="sxs-lookup"><span data-stu-id="d244d-174">The A11Y Project is a community-driven effort to make web accessibility easier.</span></span> <span data-ttu-id="d244d-175">Ознакомьтесь с сайтом [A11Y Project,](https://a11yproject.com/) чтобы узнать об основных принципах доступности, их шаблонах и библиотеках мини-приложения, а также их ресурсах по специальным программам, блогам, книгам и инструментам. [](https://a11yproject.com/patterns) [](http://a11yproject.com/resources.html)</span><span class="sxs-lookup"><span data-stu-id="d244d-175">Check out [The A11Y Project](https://a11yproject.com/) site to learn about basic accessibility principles, their accessible pattern and widget [library](https://a11yproject.com/patterns), and their [resources](http://a11yproject.com/resources.html) on accessibility software, blogs, books, and tools.</span></span>

#### [<span data-ttu-id="d244d-176">Web Accessibility Initiative (WAI)</span><span class="sxs-lookup"><span data-stu-id="d244d-176">Web Accessibility Initiative (WAI)</span></span>](https://w3.org/WAI/)

<span data-ttu-id="d244d-177">W3C Web Accessibility Initiative (WAI) — это попытка улучшить доступность интернета.</span><span class="sxs-lookup"><span data-stu-id="d244d-177">The W3C Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web.</span></span> <span data-ttu-id="d244d-178">Их сайт предоставляет множество [](https://www.w3.org/WAI/gettingstarted/Overview.html)ресурсов для начала работы со специальными веб-ресурсами, проектирования для [включения,](https://www.w3.org/WAI/users/Overview.html)учебников и [презентаций](https://www.w3.org/WAI/train.html)и многого другого.</span><span class="sxs-lookup"><span data-stu-id="d244d-178">Their site provides a variety of resources for [Getting Started with Web Accessibility](https://www.w3.org/WAI/gettingstarted/Overview.html), [Designing for Inclusion](https://www.w3.org/WAI/users/Overview.html), [tutorials and presentations](https://www.w3.org/WAI/train.html), and more.</span></span>

### <span data-ttu-id="d244d-179">Блоги о доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-179">Accessibility Blogs</span></span>

#### [<span data-ttu-id="d244d-180">Группа Paciello</span><span class="sxs-lookup"><span data-stu-id="d244d-180">The Paciello Group</span></span>](https://www.paciellogroup.com/blog/)

<span data-ttu-id="d244d-181">Группа Paciello предоставляет консультационные и технологические решения для организаций по всему миру, чтобы их клиенты эффективно и эффективно охватить все аудитории, одновременно обеспечивая при этом правительственные и международные стандарты.</span><span class="sxs-lookup"><span data-stu-id="d244d-181">The Paciello Group provides consulting and technology solutions to organizations around the world to ensure their clients reach all audiences effectively and efficiently, while meeting governmental and international standards.</span></span> <span data-ttu-id="d244d-182">Их блог охватывает такие темы, как лучшие методики работы с веб-специальными данными, средства для работы с специальными данными и тенденции.</span><span class="sxs-lookup"><span data-stu-id="d244d-182">Their blog covers topics like web accessibility best practices, accessibility tools, and accessibility trends.</span></span>

#### [<span data-ttu-id="d244d-183">Простое доступное</span><span class="sxs-lookup"><span data-stu-id="d244d-183">Simply Accessible</span></span>](http://simplyaccessible.com/articles/)

<span data-ttu-id="d244d-184">Простое специальные возможности — это команда специалистов по специальным специальным услугам, которая проводит обучение по специальным специальным данным, консультации и другие возможности, чтобы изменить представление о доступности в Интернете.</span><span class="sxs-lookup"><span data-stu-id="d244d-184">Simply Accessible is a team of accessibility specialists providing accessibility training, consulting and more to change the perception of accessibility on the web.</span></span> <span data-ttu-id="d244d-185">В [разделе "Статьи"](http://simplyaccessible.com/articles/) обсуждаются лучшие методики работы со специальными веб-приложениями, специальным дизайном и многого другго.</span><span class="sxs-lookup"><span data-stu-id="d244d-185">Their [Articles](http://simplyaccessible.com/articles/) section discusses best practices for web accessibility, accessible design, and more.</span></span>

#### [<span data-ttu-id="d244d-186">Группа SSB СУИБ (SSB)</span><span class="sxs-lookup"><span data-stu-id="d244d-186">SSB BART Group (SSB)</span></span>](http://www.ssbbartgroup.com/blog/)

<span data-ttu-id="d244d-187">SSB CLIENTS Group — это цифровая компания, поддерживаюющая своих клиентов в разработке и развертывании доступных продуктов и служб.</span><span class="sxs-lookup"><span data-stu-id="d244d-187">SSB BART Group is a digital accessibility firm supporting their clients in developing and deploying accessible products and services.</span></span> <span data-ttu-id="d244d-188">В блогах этих разработчиков имеются такие темы, как практические методики ARIA, тенденции доступности, вебинары и другие.</span><span class="sxs-lookup"><span data-stu-id="d244d-188">Their blog addresses topics like ARIA best practices, accessibility trends, webinars, and more.</span></span>

### <span data-ttu-id="d244d-189">Доступные примеры</span><span class="sxs-lookup"><span data-stu-id="d244d-189">Accessible Examples</span></span>

#### [<span data-ttu-id="d244d-190">ally.js - Учебники</span><span class="sxs-lookup"><span data-stu-id="d244d-190">ally.js - Tutorials</span></span>](http://allyjs.io/tutorials/)

<span data-ttu-id="d244d-191">Библиотека JavaScript, помогая современным веб-приложениям с учетом проблем с доступностью, упростив доступность.</span><span class="sxs-lookup"><span data-stu-id="d244d-191">JavaScript library to help modern web applications with accessibility concerns by making accessibility simpler.</span></span>

#### [<span data-ttu-id="d244d-192">Heydonworks — примеры ARIA</span><span class="sxs-lookup"><span data-stu-id="d244d-192">Heydonworks - ARIA Examples</span></span>](http://heydonworks.com/practical_aria_examples/)

<span data-ttu-id="d244d-193">Практические примеры ARIA для улучшения доступности приложения</span><span class="sxs-lookup"><span data-stu-id="d244d-193">Practical ARIA examples to enhance your application accessibility</span></span>

#### [<span data-ttu-id="d244d-194">Примеры openAjax</span><span class="sxs-lookup"><span data-stu-id="d244d-194">OpenAjax Examples</span></span>](http://oaa-accessibility.org/)

<span data-ttu-id="d244d-195">Веб-сайт OpenAjax Alliance — это отличный ресурс для проверки правил для WAI-ARIA и предоставляет ряд примеров реализации WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="d244d-195">The OpenAjax Alliance website is an excellent resource for verifying the rules for WAI-ARIA and provides a number of examples of WAI-ARIA implementations.</span></span>

#### [<span data-ttu-id="d244d-196">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="d244d-196">Patterns</span></span>](http://a11yproject.com/patterns.html)

<span data-ttu-id="d244d-197">[Проект A11Y](http://a11yproject.com/) предлагает библиотеку доступных виджетов и шаблонов, таких как меню, кнопки, инструменты и другие.</span><span class="sxs-lookup"><span data-stu-id="d244d-197">[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.</span></span>

### <span data-ttu-id="d244d-198">Accessibility Techniques & Tools</span><span class="sxs-lookup"><span data-stu-id="d244d-198">Accessibility Techniques & Tools</span></span>

#### [<span data-ttu-id="d244d-199">Доступность: создание доступных значков расширений для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d244d-199">Accessibility: Creating accessible extension icons for Microsoft Edge</span></span>](../../edgehtml/extensions/guides/accessibility.md)

<span data-ttu-id="d244d-200">Получите руководство по созданию значков доступных расширений для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d244d-200">Get guidance on creating accessible extensions icons for Microsoft Edge.</span></span>

#### [<span data-ttu-id="d244d-201">Доступное имя и описание: вычисления и сопоставления 1.1</span><span class="sxs-lookup"><span data-stu-id="d244d-201">Accessible Name and Description: Computation and Mappings 1.1</span></span>](https://www.w3.org/TR/accname-1.1/)

<span data-ttu-id="d244d-202">В этом документе о сопоставлении W3C объясняется, как браузеры определяют имена и описания доступных объектов из языков веб-контента и выставляют их в API для работы с специальными данными.</span><span class="sxs-lookup"><span data-stu-id="d244d-202">This W3C mapping document explains how browsers determine name and descriptions of accessible objects from web content languages and expose them in accessibility APIs.</span></span>

#### [<span data-ttu-id="d244d-203">Ресурсы для оценки доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-203">Accessibility Evaluation Resources</span></span>](https://www.w3.org/WAI/eval/Overview.html)

<span data-ttu-id="d244d-204">Ресурсы оценки доступности — это многоуровневый ресурс W3C, который описывает различные подходы к оценке доступности веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="d244d-204">Accessibility Evaluation Resources is a multi-page resource by the W3C that outlines different approaches for evaluating websites for accessibility.</span></span>

#### [<span data-ttu-id="d244d-205">Тесты совместимости с вспомогательными технологиями</span><span class="sxs-lookup"><span data-stu-id="d244d-205">Assistive technology compatibility tests</span></span>](http://www.powermapper.com/tests/)

<span data-ttu-id="d244d-206">Результаты тестирования, показывающие, как различные типы контента и стандарты ведут себя в вспомогательных технологиях (AT), таких как считыватели с экрана.</span><span class="sxs-lookup"><span data-stu-id="d244d-206">Test results showing how different content types and standards behave in assistive technologies (AT) like screen readers.</span></span>

#### [<span data-ttu-id="d244d-207">Создание доступных веб-сайтов стало намного проще</span><span class="sxs-lookup"><span data-stu-id="d244d-207">Building accessible websites just got a lot easier</span></span>](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

<span data-ttu-id="d244d-208">В этой записи блога о веб-разработке и инструментах .NET описывается проверка Visual Studio [веб-доступности](https://go.microsoft.com/fwlink/p/?linkid=841539)расширения.</span><span class="sxs-lookup"><span data-stu-id="d244d-208">This .NET Web Development and Tools blog post describes the Visual Studio extension [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).</span></span>

#### [<span data-ttu-id="d244d-209">Сопоставления API основных возможностей 1.1</span><span class="sxs-lookup"><span data-stu-id="d244d-209">Core Accessibility API Mappings 1.1</span></span>](https://www.w3.org/TR/core-aam-1.1/)

<span data-ttu-id="d244d-210">В этом документе о сопоставлении W3C объясняется, как семантика языков веб-контента доступна для API-аналитики доступности.</span><span class="sxs-lookup"><span data-stu-id="d244d-210">This W3C mapping document explains how the semantics of web content languages are exposed to accessibility APIs.</span></span>  

#### [<span data-ttu-id="d244d-211">Простые проверки — первый обзор веб-доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-211">Easy Checks – A First Review of Web Accessibility</span></span>](https://www.w3.org/WAI/eval/preliminary.html)

<span data-ttu-id="d244d-212">Серия быстрых проверок WAI, которые помогают определить доступность веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="d244d-212">A series of quick checks by the WAI that help you asses the accessibility of a web page.</span></span>

#### [<span data-ttu-id="d244d-213">Как выполнить WCAG 2.0</span><span class="sxs-lookup"><span data-stu-id="d244d-213">How to Meet WCAG 2.0</span></span>](https://www.w3.org/WAI/WCAG20/quickref/)

<span data-ttu-id="d244d-214">Краткий справочник по требованиям WCAG 2.0 (критерии успешности) и методам.</span><span class="sxs-lookup"><span data-stu-id="d244d-214">A quick reference to Web Content Accessibility Guidelines (WCAG) 2.0 requirements (success criteria) and techniques.</span></span>

#### [<span data-ttu-id="d244d-215">HtmL Accessibility API Mappings 1.0</span><span class="sxs-lookup"><span data-stu-id="d244d-215">HTML Accessibility API Mappings 1.0</span></span>](https://www.w3.org/TR/html-aam-1.0/)

<span data-ttu-id="d244d-216">В этом документе сопоставлений W3C объясняется, как элементы и атрибуты HTML5.1 сопоняются с API-кодами доступности платформы.</span><span class="sxs-lookup"><span data-stu-id="d244d-216">This W3C mappings document explains how HTML5.1 element and attributes map to platform accessibility APIs.</span></span>

#### [<span data-ttu-id="d244d-217">Быстрые советы</span><span class="sxs-lookup"><span data-stu-id="d244d-217">Quick Tips</span></span>](http://a11yproject.com/#Quick-tips)

<span data-ttu-id="d244d-218">Список советов по быстрой веб-разработке для доступности [проекта A11Y.](http://a11yproject.com/)</span><span class="sxs-lookup"><span data-stu-id="d244d-218">A list of quick web development tips for accessibility by [The A11Y Project](http://a11yproject.com/).</span></span>

#### [<span data-ttu-id="d244d-219">Сканирование сайта</span><span class="sxs-lookup"><span data-stu-id="d244d-219">Site Scan</span></span>](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

<span data-ttu-id="d244d-220">Средство сканирования сайтов в Центре разработчиков Microsoft Edge проверяет наличие библиотек, проблем макета и проблем с специальными возможностями.</span><span class="sxs-lookup"><span data-stu-id="d244d-220">The Site Scan tool on Microsoft Edge Dev Center checks for out-of-date libraries, layout issues, and accessibility issues.</span></span>

#### [<span data-ttu-id="d244d-221">Методы для WCAG 2.0</span><span class="sxs-lookup"><span data-stu-id="d244d-221">Techniques for WCAG 2.0</span></span>](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

<span data-ttu-id="d244d-222">Методы из W3C, которые предоставляют рекомендации для веб-разработчиков по критерию успешности соответствия рекомендациям по специальным требованиям веб-контента [(WCAG) 2.0.](https://w3.org/TR/WCAG20/)</span><span class="sxs-lookup"><span data-stu-id="d244d-222">Techniques from the W3C that provide guidance for web developers on meeting [Web Content Accessibility Guidelines (WCAG) 2.0](https://w3.org/TR/WCAG20/) success criteria.</span></span>

#### [<span data-ttu-id="d244d-223">Советы по разработке для веб-доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-223">Tips on Developing for Web Accessibility</span></span>](https://w3.org/WAI/gettingstarted/tips/developing.html)

<span data-ttu-id="d244d-224">Советы из W3C по разработке веб-контента, доступного для людей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="d244d-224">Tips from the W3C on developing web content that is more accessible to people with disabilities.</span></span>

#### [<span data-ttu-id="d244d-225">WAI-ARIA Authoring Practices 1.1</span><span class="sxs-lookup"><span data-stu-id="d244d-225">WAI-ARIA Authoring Practices 1.1</span></span>](http://w3c.github.io/aria-practices/)

<span data-ttu-id="d244d-226">Документ W3C, который предоставляет читателям представление о том, как использовать WAI-ARIA 1.1, и рекомендует подходы к обеспечению доступности виджетов, навигации и поведения с помощью ролей, состояния и свойств WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="d244d-226">A document by the W3C that provides readers with an understanding of how to use WAI-ARIA 1.1 and recommends approaches to make widgets, navigation, and behaviors accessible using WAI-ARIA roles, states, and properties.</span></span>

#### [<span data-ttu-id="d244d-227">Рекомендации и методики WAI</span><span class="sxs-lookup"><span data-stu-id="d244d-227">WAI Guidelines and Techniques</span></span>](https://w3.org/WAI/guid-tech.html)

<span data-ttu-id="d244d-228">Ряд рекомендаций и стандартов для работы с веб-специальными данными, разработанных WAI.</span><span class="sxs-lookup"><span data-stu-id="d244d-228">A series of web accessibility guidelines and standards developed by the WAI.</span></span>  

#### [<span data-ttu-id="d244d-229">Список средств оценки веб-доступности</span><span class="sxs-lookup"><span data-stu-id="d244d-229">Web Accessibility Evaluation Tools List</span></span>](https://www.w3.org/WAI/ER/tools/index.html)

<span data-ttu-id="d244d-230">Список средств оценки доступности веб-сайтов, которые помогут определить, соответствуют ли веб-сайты рекомендациям по специальным требованиям.</span><span class="sxs-lookup"><span data-stu-id="d244d-230">A list of web accessibility evaluation tools to help determine if websites meet accessibility guidelines.</span></span>

#### [<span data-ttu-id="d244d-231">Перспективы по специальным возможности в Интернете: изучение влияния и преимуществ для всех пользователей</span><span class="sxs-lookup"><span data-stu-id="d244d-231">Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone</span></span>](https://w3.org/WAI/perspectives/)

<span data-ttu-id="d244d-232">Серия коротких сиюмитных видеороликов W3C о влиянии на доступность и преимуществах для всех.</span><span class="sxs-lookup"><span data-stu-id="d244d-232">A series of short situational videos by the W3C about the impact of accessibility and the benefits for everyone.</span></span>

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Виртуальные машины | Разработчик Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Полное руководство по диктору | Поддержка Майкрософт"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Использование экранной лубки для упростит процесс на экране | Поддержка Майкрософт"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Accessibility Insights for Web | Accessibility Insights"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Создание виртуальных устройств и управление ими | Разработчики Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Запуск приложений на эмуляторе Android | Разработчики Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Скачать Android Studio | Разработчики Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Доступ к зрению — Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Лаборатории assistiv"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Freedom Scientific"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freedom Scientific"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android Accessibility Suite | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "О NVDA | NV Access"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Совместимость с клавиатурой | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Опрос пользователей с низким зрением \#2 результаты | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Опрос пользователей программы чтения с экрана \#8 результаты | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Тестирование с помощью чтения с экрана | WebAIM"  
