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
# <a name="building-accessible-websites"></a><span data-ttu-id="93fd0-104">Создание доступных веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="93fd0-104">Building Accessible Websites</span></span>

<span data-ttu-id="93fd0-105">Веб-сайт заполнен динамическими и сложными веб-сайтами, приложениями и пользовательскими интерфейсами, построенными с использованием комбинации HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="93fd0-105">The web is filled with dynamic and complex websites, applications, and user interfaces built using a combination of HTML, CSS, and JavaScript.</span></span>  <span data-ttu-id="93fd0-106">Однако при конструировании и построении без доступности эти сложные веб-сайты трудно использовать людьми, которые используют вспомогательные технологии для просмотра веб-страниц. [](https://webaim.org/articles/motor/assistive)</span><span class="sxs-lookup"><span data-stu-id="93fd0-106">However, when designed and built without accessibility in mind, these complex websites are difficult to use by people who rely on [assistive technologies](https://webaim.org/articles/motor/assistive) to browse the web.</span></span> <span data-ttu-id="93fd0-107">Создание веб-сайтов, доступных для людей с ограниченными возможностями, требует семантических сведений о пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93fd0-107">Building websites that are accessible to people with disabilities requires semantic information about the user interface.</span></span> <span data-ttu-id="93fd0-108">Это позволяет вспомогательным технологиям, таким как считыватели экрана, передавать необходимую информацию, чтобы помочь людям с рядом возможностей использовать веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="93fd0-108">This allows for assistive technologies, like screen readers, to convey the necessary information to help people with a range of abilities use the website.</span></span>

<span data-ttu-id="93fd0-109">Сведения о том, какие новые функции HTML5 доступны при поддержке Microsoft Edge, посетите [HTML5Accessibility.](https://html5accessibility.com)</span><span class="sxs-lookup"><span data-stu-id="93fd0-109">Visit [HTML5Accessibility](https://html5accessibility.com) for information on which new HTML5 features are accessibly supported by Microsoft Edge.</span></span>

## <a name="how-accessibility-works"></a><span data-ttu-id="93fd0-110">Работа с доступностью</span><span class="sxs-lookup"><span data-stu-id="93fd0-110">How Accessibility Works</span></span>

<span data-ttu-id="93fd0-111">Вспомогательные технологии добавляют возможности, которые обычно не имеют компьютеры.</span><span class="sxs-lookup"><span data-stu-id="93fd0-111">Assistive technologies add capabilities that computers don't usually have.</span></span> <span data-ttu-id="93fd0-112">Например, незрячий пользователь может использовать клавиатуру в сочетании с вспомогательными технологиями, такими как считыватель экрана, а не непосредственно с помощью браузера с помощью мыши и экрана.</span><span class="sxs-lookup"><span data-stu-id="93fd0-112">For example, a visually impaired user might use their keyboard in combination with assistive technology such as a screen reader, rather than directly using the browser with the mouse and screen.</span></span> <span data-ttu-id="93fd0-113">Для приложений на платформах Майкрософт и в Интернете вспомогательные технологии взаимодействуют с Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), объектной моделью, определенной для приложений, например объектной моделью документа (DOM) в Microsoft Edge или их сочетанием.</span><span class="sxs-lookup"><span data-stu-id="93fd0-113">For applications on Microsoft platforms and on the web, the assistive technology interacts with Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), an application-specific object model such as the Document Object Model (DOM) in Microsoft Edge, or a combination of these.</span></span>

<span data-ttu-id="93fd0-114">Для веб-разработчиков определенные элементы HTML соедуются с объектами автоматизации пользовательского интерфейса, поэтому при выборе этих элементов HTML разработчик может использовать свойства доступности и события, встроенные в эти элементы.</span><span class="sxs-lookup"><span data-stu-id="93fd0-114">For web developers, certain HTML elements are mapped to UI Automation objects, so in selecting those HTML elements, the developer can use the accessibility properties and events built in to those elements.</span></span> <span data-ttu-id="93fd0-115">При разработке веб-сайта обычно требуется только обеспечить правильное написание API (или задан соответствующий элемент), чтобы приложение было доступным.</span><span class="sxs-lookup"><span data-stu-id="93fd0-115">While developing your website, you usually only need to be concerned with ensuring that the API is correctly written to (or that the appropriate element is specified), in order for the application to be accessible.</span></span> <span data-ttu-id="93fd0-116">Дополнительные [сведения можно получить в службе автоматизации ARIA](./ARIA-and-UI-Automation.md) и пользовательского интерфейса в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="93fd0-116">Check out [ARIA and UI Automation in Microsoft Edge](./ARIA-and-UI-Automation.md) for more information.</span></span>  <span data-ttu-id="93fd0-117">Сведения о доступных приложениях универсальной платформы Windows (UWP) см. в разделе [Доступность](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) в Центре разработчиков Windows.</span><span class="sxs-lookup"><span data-stu-id="93fd0-117">For information on accessible Universal Windows Platform (UWP) apps, navigate to the [Accessibility](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) topic in the Windows Dev Center.</span></span>

<span data-ttu-id="93fd0-118">Многие распространенные проблемы с динамическим контентом можно решить с помощью хорошей практики кодирования, а документация [по WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) содержит множество методов и методов, которые помогут вам создавать более доступные динамические веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="93fd0-118">Many common accessibility issues with dynamic content can be addressed by good coding practice, and the [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) documentation includes many techniques and best practices to help you create more accessible dynamic web applications.</span></span> <span data-ttu-id="93fd0-119">Однако даже при правильном кодовом коде динамическое содержимое не обязательно доступно.</span><span class="sxs-lookup"><span data-stu-id="93fd0-119">Even when coded properly, however, dynamic content is not necessarily accessible.</span></span> <span data-ttu-id="93fd0-120">Эту проблему можно решить с помощью доступных приложений с богатым доступом к Интернету [(ARIA).](#aria)</span><span class="sxs-lookup"><span data-stu-id="93fd0-120">[Accessible Rich Internet Applications (ARIA)](#aria) helps overcome this issue.</span></span>  

<span data-ttu-id="93fd0-121">Дополнительные сведения о доступности веб-сайтов см. в странице [Введение](https://www.w3.org/WAI/intro/accessibility.php) в веб-доступность по инициативе [веб-доступности (WAI).](https://www.w3.org/WAI)</span><span class="sxs-lookup"><span data-stu-id="93fd0-121">For more information on web accessibility, check out the [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative (WAI)](https://www.w3.org/WAI).</span></span>

## <a name="aria"></a><span data-ttu-id="93fd0-122">ARIA</span><span class="sxs-lookup"><span data-stu-id="93fd0-122">ARIA</span></span>

<span data-ttu-id="93fd0-123">[Спецификация](https://www.w3.org/TR/wai-aria/) доступных приложений с богатым доступом в Интернет [](https://www.w3.org/WAI/) (ARIA) инициативы W3C по веб-доступности определяется как синтаксис для создания динамического веб-контента и пользовательских интерфейсов доступными для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="93fd0-123">The [Accessible Rich Internet Applications](https://www.w3.org/TR/wai-aria/) (ARIA) specification by the W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) defines as a syntax for making dynamic web content and custom user interfaces accessible to all people.</span></span> <span data-ttu-id="93fd0-124">ARIA расширяет HTML с помощью дополнительных атрибутов (ролей, свойств и состояния), предназначенных для передачи настраиваемой семантики.</span><span class="sxs-lookup"><span data-stu-id="93fd0-124">ARIA extends HTML by using additional attributes (roles, properties, and states) that are designed to convey custom semantics.</span></span> <span data-ttu-id="93fd0-125">Эти атрибуты используются браузерами для того, чтобы передать состояние и роль элементов управления API доступности.</span><span class="sxs-lookup"><span data-stu-id="93fd0-125">These attributes are used by browsers to pass along the controls' state and role to the accessibility API.</span></span>

### <a name="roles-properties-and-states"></a><span data-ttu-id="93fd0-126">Роли, свойства и состояния</span><span class="sxs-lookup"><span data-stu-id="93fd0-126">Roles, Properties, and States</span></span>

<span data-ttu-id="93fd0-127">Роли ARIA устанавливаются на элементы, использующие атрибут для передачи вспомогательных технологий и API доступности сведений [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) об элементе.</span><span class="sxs-lookup"><span data-stu-id="93fd0-127">ARIA roles are set on elements using the [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribute to give assistive technologies and accessibility APIs information about the element.</span></span> <span data-ttu-id="93fd0-128">Например, ниже задается элемент, который означает, что это элемент `<li>` `role="menuitem"` в меню.</span><span class="sxs-lookup"><span data-stu-id="93fd0-128">For example, the below `<li>` element is assigned `role="menuitem"` to signify it's an item in a menu.</span></span>

```html
<li role="menuitem">Home</li>
```

<span data-ttu-id="93fd0-129">Состояния и свойства ARIA — это атрибуты с префиксом арии, которые предоставляют определенную информацию об объекте, чтобы помочь сформировать определение природы ролей.</span><span class="sxs-lookup"><span data-stu-id="93fd0-129">ARIA states and properties are aria-prefixed attributes that provide specific information about an object to help form the definition of the nature of roles.</span></span> <span data-ttu-id="93fd0-130">Свойства — это атрибуты, которые имеют важное значение для природы объекта, например [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) и [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="93fd0-130">Properties are attributes that are essential to the nature of an object, like [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) and [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx).</span></span> <span data-ttu-id="93fd0-131">Изменение свойства влияет на значение объекта.</span><span class="sxs-lookup"><span data-stu-id="93fd0-131">Changing a property affects the meaning of the object.</span></span> <span data-ttu-id="93fd0-132">В приведенной ниже примере свойство задавалось элементу меню, чтобы у него было `aria-haspopup="true"` `<li>` всплывающее всплывающее.</span><span class="sxs-lookup"><span data-stu-id="93fd0-132">In the example below, the property `aria-haspopup="true"` is set on a `<li>` menu item to signify it has a popup.</span></span>

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

<span data-ttu-id="93fd0-133">Состояния не изменяют природу объекта, а представляют сведения, связанные с объектом или взаимодействием пользователя с объектом, например [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) или [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="93fd0-133">States do not change the nature of the object, but represent information associated with the object or user interaction with the object, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) or [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx).</span></span> <span data-ttu-id="93fd0-134">Например, состояние в приведенной ниже примере означает, что контрольный `aria-checked="false"` ящик не проверяется.</span><span class="sxs-lookup"><span data-stu-id="93fd0-134">For example, the state `aria-checked="false"` in the example below represents that the checkbox is not checked.</span></span>

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

<span data-ttu-id="93fd0-135">Перейдите [к модели ролей](https://www.w3.org/TR/wai-aria-1.1/#roles) w3C, чтобы увидеть полный список ролей, свойств и состояния.</span><span class="sxs-lookup"><span data-stu-id="93fd0-135">Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.</span></span>

<span data-ttu-id="93fd0-136">Дополнительные сведения об ARIA перейдите к ARIA в разделе [Ресурсы.](#resources)</span><span class="sxs-lookup"><span data-stu-id="93fd0-136">For more information on ARIA, navigate to ARIA in the [Resources](#resources) section.</span></span>

## <a name="assistive-technology-compatibility-testing"></a><span data-ttu-id="93fd0-137">Тестирование совместимости вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="93fd0-137">Assistive Technology Compatibility Testing</span></span>  

<span data-ttu-id="93fd0-138">Проверка того, что веб-сайт, который вы строите, работает с реальными вспомогательными технологиями, является лучшим способом обеспечения хорошего опыта для пользователей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="93fd0-138">Verifying that the website you are building works with real assistive technologies is the best way to ensure a good experience for your users with disabilities.</span></span>  <span data-ttu-id="93fd0-139">Так как многие вспомогательные технологии используют клавиатуру, тестирование доступности клавиатуры веб-сайта является хорошим местом для начала.</span><span class="sxs-lookup"><span data-stu-id="93fd0-139">Since many assistive technologies make use of the keyboard, testing the keyboard accessibility of your website is a good place to start.</span></span>  <span data-ttu-id="93fd0-140">[Тестирование совместимости клавиатуры][W3cPerspectiveVideosKeyboard] подтверждает, что пользователи имеют доступ ко всем интерактивным средствам управления без необходимости использования мыши.</span><span class="sxs-lookup"><span data-stu-id="93fd0-140">[Keyboard compatibility testing][W3cPerspectiveVideosKeyboard] validates that users have access to all interactive controls without requiring a mouse.</span></span>  <span data-ttu-id="93fd0-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] — это расширение браузера для Microsoft Edge и Chrome, которое направляет вас и выявляет несколько распространенных проблем.</span><span class="sxs-lookup"><span data-stu-id="93fd0-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] is a browser extension for Microsoft Edge and Chrome that guides you and reveals several common issues.</span></span>  

<span data-ttu-id="93fd0-142">После того как вы уверены, что ваш веб-сайт хорошо работает с клавиатурой, попробуйте его с другими вспомогательными технологиями, такими как считыватели экрана.</span><span class="sxs-lookup"><span data-stu-id="93fd0-142">Once you are confident that your website works well with a keyboard, try it with other assistive technologies, such as screen readers.</span></span>  <span data-ttu-id="93fd0-143">Он выявляет проблемы в следующем.</span><span class="sxs-lookup"><span data-stu-id="93fd0-143">It uncover issues in the following.</span></span>

*   <span data-ttu-id="93fd0-144">HTML, ARIA и CSS.</span><span class="sxs-lookup"><span data-stu-id="93fd0-144">Your HTML, ARIA, and CSS.</span></span>  
*   <span data-ttu-id="93fd0-145">Уровень поддержки вспомогательных технологий для функции или техники.</span><span class="sxs-lookup"><span data-stu-id="93fd0-145">The level of support of an assistive technology for a feature or technique.</span></span>  
    
<span data-ttu-id="93fd0-146">Различные браузеры могут отрисовки элементов для API доступности платформы по-другому, чем Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="93fd0-146">Different browsers may map elements to platform accessibility APIs differently than Microsoft Edge.</span></span>  <span data-ttu-id="93fd0-147">При создании интерфейса важно учитывать каждое различие.</span><span class="sxs-lookup"><span data-stu-id="93fd0-147">While building your interface, it is important to consider each difference.</span></span>  

<span data-ttu-id="93fd0-148">WebAIM проводит опросы [][WebaimProjectsScreenreadersurvey8] с [][WebaimProjectsLowvisionsurvey2] помощью чтения с экрана и пользователей с низким зрением, которые помогут вам определить, какие вспомогательные технологии и браузеры необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="93fd0-148">WebAIM conducts surveys with [screen reader][WebaimProjectsScreenreadersurvey8] and [low vision][WebaimProjectsLowvisionsurvey2] users that help you decide which assistive technologies and browsers you want to test.</span></span>  

### <a name="learning-how-to-test"></a><span data-ttu-id="93fd0-149">Обучение проверке</span><span class="sxs-lookup"><span data-stu-id="93fd0-149">Learning How to Test</span></span>  

<span data-ttu-id="93fd0-150">Вспомогательные технологии — это сложные средства.</span><span class="sxs-lookup"><span data-stu-id="93fd0-150">Assistive technologies are sophisticated tools.</span></span>  <span data-ttu-id="93fd0-151">Не думайте, что вы можете немедленно приступить к тестированию с помощью вспомогательных технологий, не узнав о том, как это работает.</span><span class="sxs-lookup"><span data-stu-id="93fd0-151">Do not assume that you are able to immediately start testing with an assistive technology without first learning about how it works.</span></span>  <span data-ttu-id="93fd0-152">Обучение проверке с помощью чтения с экрана имеет особенно крутую кривую обучения.</span><span class="sxs-lookup"><span data-stu-id="93fd0-152">Learning to test with a screen reader has an especially steep learning curve.</span></span>  <span data-ttu-id="93fd0-153">Начинающий пользователь чтения экрана может предположить, что ошибка чтения экрана произошла, когда проблема связана с ненадлежащим использованием чтения экрана.</span><span class="sxs-lookup"><span data-stu-id="93fd0-153">A novice screen reader user may assume that a screen reader bug has occurred while the issue is related to misuse of the screen reader.</span></span>  

<span data-ttu-id="93fd0-154">Дополнительные сведения о том, как научиться тестировать с помощью вспомогательных технологий, перейдите к [тестированию][WebaimArticlesScreenreaderTesting] с помощью чтения с экрана в WebAIM.</span><span class="sxs-lookup"><span data-stu-id="93fd0-154">For more information about learning to test with assistive technologies, navigate to [Testing with Screen Readers][WebaimArticlesScreenreaderTesting] on WebAIM.</span></span>  

### <a name="testing-locally"></a><span data-ttu-id="93fd0-155">Локальное тестирование</span><span class="sxs-lookup"><span data-stu-id="93fd0-155">Testing Locally</span></span>  

<span data-ttu-id="93fd0-156">Большинство устройств включают вспомогательные технологии, встроенные в ОС.</span><span class="sxs-lookup"><span data-stu-id="93fd0-156">Most devices include assistive technology that is built-in to the OS.</span></span>  <span data-ttu-id="93fd0-157">Microsoft Windows включает в себя [считыватель экрана с рассказчиком Windows][MicrosoftSupport22798] и Windows [Magnifier.][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]</span><span class="sxs-lookup"><span data-stu-id="93fd0-157">Microsoft Windows includes the [Windows Narrator][MicrosoftSupport22798] screen reader and [Windows Magnifier][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span></span>  <span data-ttu-id="93fd0-158">Доступны сторонние вспомогательные технологии, такие как [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]и [ZoomText.][FreedomscientificSoftwareZoomtext]</span><span class="sxs-lookup"><span data-stu-id="93fd0-158">3rd party assistive technologies like [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws], and [ZoomText][FreedomscientificSoftwareZoomtext] are available to download.</span></span>  <span data-ttu-id="93fd0-159">MacOS Apple включает [считыватель экрана VoiceOver.][AppleAccessibilityMacVision]</span><span class="sxs-lookup"><span data-stu-id="93fd0-159">Apple macOS includes the [VoiceOver][AppleAccessibilityMacVision] screen reader.</span></span>  <span data-ttu-id="93fd0-160">А iOS, Android и Linux поддерживают различные вспомогательные технологии.</span><span class="sxs-lookup"><span data-stu-id="93fd0-160">And iOS, Android, and Linux all support a variety of assistive technologies.</span></span>  

### <a name="testing-in-virtual-machines-and-emulators"></a><span data-ttu-id="93fd0-161">Тестирование в виртуальных машинах и эмуляторах</span><span class="sxs-lookup"><span data-stu-id="93fd0-161">Testing in Virtual Machines and Emulators</span></span>  

<span data-ttu-id="93fd0-162">В macOS, если вы хотите протестировать с помощью вспомогательных технологий, доступных только для Windows, таких как Windows Narrator или NVDA, создайте виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="93fd0-162">Under macOS, if you want to test with an assistive technology only available for Windows, like Windows Narrator or NVDA, create a Windows virtual machine.</span></span>  <span data-ttu-id="93fd0-163">Виртуальные машины с Microsoft Edge \(EdgeHTML\) и IE доступны для VirtualBox и VMWare на странице загрузки [виртуальных машин.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="93fd0-163">Virtual machines with Microsoft Edge \(EdgeHTML\) and IE are available for VirtualBox and VMWare on the [Virtual Machines download page][MicrosoftDeveloperEdgeVms].</span></span>  

<span data-ttu-id="93fd0-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] включает эмулятор, который для тестирования вспомогательных технологий в [пакете доступности Android.][GooglePlayStoreAndroidAccessibilitySuite]</span><span class="sxs-lookup"><span data-stu-id="93fd0-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] includes an emulator that for you to test assistive technologies in the [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite].</span></span>  <span data-ttu-id="93fd0-165">Следуйте инструкциям по установке [виртуального устройства][AndroidDeveloperDevicesManagingAvdsHtml] и запуску [эмулятора,][AndroidDeveloperDevicesEmulatorHtml]а затем установите пакет доступности [Android][GooglePlayStoreAndroidAccessibilitySuite] из магазина GooglePlay.</span><span class="sxs-lookup"><span data-stu-id="93fd0-165">Follow the instructions to [set up a virtual device][AndroidDeveloperDevicesManagingAvdsHtml] and [start the emulator][AndroidDeveloperDevicesEmulatorHtml], then install [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] from the GooglePlay store.</span></span>  

> [!NOTE]
> <span data-ttu-id="93fd0-166">Симулятор iOS в настоящее время не включает VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="93fd0-166">The iOS Simulator does not currently include VoiceOver.</span></span>  

### <a name="cloud-based-testing-tools"></a><span data-ttu-id="93fd0-167">Облачные средства тестирования</span><span class="sxs-lookup"><span data-stu-id="93fd0-167">Cloud-based Testing Tools</span></span>  

<span data-ttu-id="93fd0-168">Если вспомогательные технологии недоступны на оси или не удалось установить ее на виртуальной машине или эмуляторе, средства тестирования вспомогательных технологий на облачной основе — это следующая лучшая вещь.</span><span class="sxs-lookup"><span data-stu-id="93fd0-168">If an assistive technology is not available on your OS or you not possible to install one on a virtual machine or emulator, cloud-based assistive technology testing tools are the next best thing.</span></span>  

*   <span data-ttu-id="93fd0-169">[Assistiv Labs (коммерческий)][AssistivlabsMain] позволяет вручную тестировать с помощью вспомогательных технологий с помощью любого современного веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="93fd0-169">[Assistiv Labs (commercial)][AssistivlabsMain] enables you to manually test with assistive technologies through any modern web browser.</span></span>  <span data-ttu-id="93fd0-170">Выберите вспомогательные технологии и браузер и соединит вас с виртуальной машиной, эмулятором или реальным устройством, с которым вы можете взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="93fd0-170">Choose an assistive technology and browser and it connects you with a virtual machine, emulator, or real device with which you may interact.</span></span>  

## <a name="resources"></a><span data-ttu-id="93fd0-171">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="93fd0-171">Resources</span></span>

### <a name="accessibility-basics"></a><span data-ttu-id="93fd0-172">Основы доступности</span><span class="sxs-lookup"><span data-stu-id="93fd0-172">Accessibility Basics</span></span>

#### [<a name="the-a11y-project"></a><span data-ttu-id="93fd0-173">Проект A11Y</span><span class="sxs-lookup"><span data-stu-id="93fd0-173">The A11Y Project</span></span>](http://a11yproject.com/)

<span data-ttu-id="93fd0-174">Проект A11Y — это работа, направленная на решение задач по упростить доступ к веб-сайтам.</span><span class="sxs-lookup"><span data-stu-id="93fd0-174">The A11Y Project is a community-driven effort to make web accessibility easier.</span></span> <span data-ttu-id="93fd0-175">Ознакомьтесь с сайтом [A11Y Project,](https://a11yproject.com/) чтобы узнать об основных принципах доступности, их доступной библиотеке шаблонов и виджетов [и](https://a11yproject.com/patterns)их ресурсах в программном обеспечении, блогах, книгах и средствах. [](http://a11yproject.com/resources.html)</span><span class="sxs-lookup"><span data-stu-id="93fd0-175">Check out [The A11Y Project](https://a11yproject.com/) site to learn about basic accessibility principles, their accessible pattern and widget [library](https://a11yproject.com/patterns), and their [resources](http://a11yproject.com/resources.html) on accessibility software, blogs, books, and tools.</span></span>

#### [<a name="web-accessibility-initiative-wai"></a><span data-ttu-id="93fd0-176">Инициатива по веб-доступности (WAI)</span><span class="sxs-lookup"><span data-stu-id="93fd0-176">Web Accessibility Initiative (WAI)</span></span>](https://w3.org/WAI/)

<span data-ttu-id="93fd0-177">Инициатива W3C по веб-доступности (WAI) — это усилия по улучшению доступности интернета.</span><span class="sxs-lookup"><span data-stu-id="93fd0-177">The W3C Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web.</span></span> <span data-ttu-id="93fd0-178">Их сайт предоставляет различные [](https://www.w3.org/WAI/gettingstarted/Overview.html)ресурсы для начала работы с веб-доступностью, [проектирование](https://www.w3.org/WAI/users/Overview.html)для включения, учебники и [презентации](https://www.w3.org/WAI/train.html)и другие.</span><span class="sxs-lookup"><span data-stu-id="93fd0-178">Their site provides a variety of resources for [Getting Started with Web Accessibility](https://www.w3.org/WAI/gettingstarted/Overview.html), [Designing for Inclusion](https://www.w3.org/WAI/users/Overview.html), [tutorials and presentations](https://www.w3.org/WAI/train.html), and more.</span></span>

### <a name="accessibility-blogs"></a><span data-ttu-id="93fd0-179">Блоги доступности</span><span class="sxs-lookup"><span data-stu-id="93fd0-179">Accessibility Blogs</span></span>

#### [<a name="the-paciello-group"></a><span data-ttu-id="93fd0-180">Группа Paciello</span><span class="sxs-lookup"><span data-stu-id="93fd0-180">The Paciello Group</span></span>](https://www.paciellogroup.com/blog/)

<span data-ttu-id="93fd0-181">Группа Paciello предоставляет консультационные и технологические решения организациям по всему миру, чтобы обеспечить эффективное и эффективное охват клиентов всеми аудиториями при одновременном обеспечении правительственных и международных стандартов.</span><span class="sxs-lookup"><span data-stu-id="93fd0-181">The Paciello Group provides consulting and technology solutions to organizations around the world to ensure their clients reach all audiences effectively and efficiently, while meeting governmental and international standards.</span></span> <span data-ttu-id="93fd0-182">Их блог охватывает такие темы, как лучшие практики, средства доступности и тенденции доступности веб-доступа.</span><span class="sxs-lookup"><span data-stu-id="93fd0-182">Their blog covers topics like web accessibility best practices, accessibility tools, and accessibility trends.</span></span>

#### [<a name="simply-accessible"></a><span data-ttu-id="93fd0-183">Просто доступно</span><span class="sxs-lookup"><span data-stu-id="93fd0-183">Simply Accessible</span></span>](http://simplyaccessible.com/articles/)

<span data-ttu-id="93fd0-184">Simply Accessible — это команда специалистов по доступности, предоставляющих обучение, консультации и другие возможности для изменения восприятия доступности в Интернете.</span><span class="sxs-lookup"><span data-stu-id="93fd0-184">Simply Accessible is a team of accessibility specialists providing accessibility training, consulting and more to change the perception of accessibility on the web.</span></span> <span data-ttu-id="93fd0-185">В [разделе Статьи](http://simplyaccessible.com/articles/) обсуждаются лучшие практики для веб-доступности, доступной разработки и других.</span><span class="sxs-lookup"><span data-stu-id="93fd0-185">Their [Articles](http://simplyaccessible.com/articles/) section discusses best practices for web accessibility, accessible design, and more.</span></span>

#### [<a name="ssb-bart-group-ssb"></a><span data-ttu-id="93fd0-186">Группа SSB BART (SSB)</span><span class="sxs-lookup"><span data-stu-id="93fd0-186">SSB BART Group (SSB)</span></span>](http://www.ssbbartgroup.com/blog/)

<span data-ttu-id="93fd0-187">SSB BART Group — это фирма по цифровой доступности, которая поддерживает своих клиентов в разработке и развертывании доступных продуктов и служб.</span><span class="sxs-lookup"><span data-stu-id="93fd0-187">SSB BART Group is a digital accessibility firm supporting their clients in developing and deploying accessible products and services.</span></span> <span data-ttu-id="93fd0-188">Их блог адресов темы, как ARIA передовая практика, тенденции доступности, веб-инары и другие.</span><span class="sxs-lookup"><span data-stu-id="93fd0-188">Their blog addresses topics like ARIA best practices, accessibility trends, webinars, and more.</span></span>

### <a name="accessible-examples"></a><span data-ttu-id="93fd0-189">Доступные примеры</span><span class="sxs-lookup"><span data-stu-id="93fd0-189">Accessible Examples</span></span>

#### [<a name="allyjs---tutorials"></a><span data-ttu-id="93fd0-190">ally.js - Учебники</span><span class="sxs-lookup"><span data-stu-id="93fd0-190">ally.js - Tutorials</span></span>](http://allyjs.io/tutorials/)

<span data-ttu-id="93fd0-191">Библиотека JavaScript, помогая современным веб-приложениям с проблемой доступности, упростив доступность.</span><span class="sxs-lookup"><span data-stu-id="93fd0-191">JavaScript library to help modern web applications with accessibility concerns by making accessibility simpler.</span></span>

#### [<a name="heydonworks---aria-examples"></a><span data-ttu-id="93fd0-192">Heydonworks — примеры ARIA</span><span class="sxs-lookup"><span data-stu-id="93fd0-192">Heydonworks - ARIA Examples</span></span>](http://heydonworks.com/practical_aria_examples/)

<span data-ttu-id="93fd0-193">Примеры практической ARIA для повышения доступности приложений</span><span class="sxs-lookup"><span data-stu-id="93fd0-193">Practical ARIA examples to enhance your application accessibility</span></span>

#### [<a name="openajax-examples"></a><span data-ttu-id="93fd0-194">Примеры OpenAjax</span><span class="sxs-lookup"><span data-stu-id="93fd0-194">OpenAjax Examples</span></span>](http://oaa-accessibility.org/)

<span data-ttu-id="93fd0-195">Веб-сайт Альянса OpenAjax — это отличный ресурс для проверки правил WAI-ARIA и содержит ряд примеров реализации WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="93fd0-195">The OpenAjax Alliance website is an excellent resource for verifying the rules for WAI-ARIA and provides a number of examples of WAI-ARIA implementations.</span></span>

#### [<a name="patterns"></a><span data-ttu-id="93fd0-196">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="93fd0-196">Patterns</span></span>](http://a11yproject.com/patterns.html)

<span data-ttu-id="93fd0-197">[Проект A11Y](http://a11yproject.com/) предлагает библиотеку доступных виджетов и шаблонов, таких как меню, кнопки, панели инструментов и другие.</span><span class="sxs-lookup"><span data-stu-id="93fd0-197">[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.</span></span>

### <a name="accessibility-techniques--tools"></a><span data-ttu-id="93fd0-198">Методы доступности & средства</span><span class="sxs-lookup"><span data-stu-id="93fd0-198">Accessibility Techniques & Tools</span></span>

#### [<a name="accessibility-creating-accessible-extension-icons-for-microsoft-edge"></a><span data-ttu-id="93fd0-199">Доступность: создание доступных значков расширения для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="93fd0-199">Accessibility: Creating accessible extension icons for Microsoft Edge</span></span>](../../edgehtml/extensions/guides/accessibility.md)

<span data-ttu-id="93fd0-200">Получите руководство по созданию значков доступных расширений для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="93fd0-200">Get guidance on creating accessible extensions icons for Microsoft Edge.</span></span>

#### [<a name="accessible-name-and-description-computation-and-mappings-11"></a><span data-ttu-id="93fd0-201">Доступное имя и описание: вычисления и сопоставления 1.1</span><span class="sxs-lookup"><span data-stu-id="93fd0-201">Accessible Name and Description: Computation and Mappings 1.1</span></span>](https://www.w3.org/TR/accname-1.1/)

<span data-ttu-id="93fd0-202">В этом документе сопоставления W3C объясняется, как браузеры определяют имена и описания доступных объектов из языков веб-контента и раскрывают их в API доступности.</span><span class="sxs-lookup"><span data-stu-id="93fd0-202">This W3C mapping document explains how browsers determine name and descriptions of accessible objects from web content languages and expose them in accessibility APIs.</span></span>

#### [<a name="accessibility-evaluation-resources"></a><span data-ttu-id="93fd0-203">Ресурсы оценки доступности</span><span class="sxs-lookup"><span data-stu-id="93fd0-203">Accessibility Evaluation Resources</span></span>](https://www.w3.org/WAI/eval/Overview.html)

<span data-ttu-id="93fd0-204">Ресурсы оценки доступности — это многоуровневый ресурс W3C, который описывает различные подходы к оценке доступности веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="93fd0-204">Accessibility Evaluation Resources is a multi-page resource by the W3C that outlines different approaches for evaluating websites for accessibility.</span></span>

#### [<a name="assistive-technology-compatibility-tests"></a><span data-ttu-id="93fd0-205">Тесты совместимости вспомогательных технологий</span><span class="sxs-lookup"><span data-stu-id="93fd0-205">Assistive technology compatibility tests</span></span>](http://www.powermapper.com/tests/)

<span data-ttu-id="93fd0-206">Результаты тестирования, показывающие, как различные типы контента и стандарты ведут себя в вспомогательных технологиях (AT) как считыватели экрана.</span><span class="sxs-lookup"><span data-stu-id="93fd0-206">Test results showing how different content types and standards behave in assistive technologies (AT) like screen readers.</span></span>

#### [<a name="building-accessible-websites-just-got-a-lot-easier"></a><span data-ttu-id="93fd0-207">Создание доступных веб-сайтов стало намного проще</span><span class="sxs-lookup"><span data-stu-id="93fd0-207">Building accessible websites just got a lot easier</span></span>](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

<span data-ttu-id="93fd0-208">В этом блоге веб-разработки и инструментов .NET описывается Visual Studio проверки доступности [веб-сайтов.](https://go.microsoft.com/fwlink/p/?linkid=841539)</span><span class="sxs-lookup"><span data-stu-id="93fd0-208">This .NET Web Development and Tools blog post describes the Visual Studio extension [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).</span></span>

#### [<a name="core-accessibility-api-mappings-11"></a><span data-ttu-id="93fd0-209">Сопоставление API API основных возможностей 1.1</span><span class="sxs-lookup"><span data-stu-id="93fd0-209">Core Accessibility API Mappings 1.1</span></span>](https://www.w3.org/TR/core-aam-1.1/)

<span data-ttu-id="93fd0-210">В этом документе сопоставления W3C объясняется, как семантика языков веб-контента подвергается воздействию API доступности.</span><span class="sxs-lookup"><span data-stu-id="93fd0-210">This W3C mapping document explains how the semantics of web content languages are exposed to accessibility APIs.</span></span>  

#### [<a name="easy-checks--a-first-review-of-web-accessibility"></a><span data-ttu-id="93fd0-211">Простые проверки — первый обзор веб-доступности</span><span class="sxs-lookup"><span data-stu-id="93fd0-211">Easy Checks – A First Review of Web Accessibility</span></span>](https://www.w3.org/WAI/eval/preliminary.html)

<span data-ttu-id="93fd0-212">Серия быстрых проверок WAI, которые помогут вам определить доступность веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="93fd0-212">A series of quick checks by the WAI that help you asses the accessibility of a web page.</span></span>

#### [<a name="how-to-meet-wcag-20"></a><span data-ttu-id="93fd0-213">Как выполнить WCAG 2.0</span><span class="sxs-lookup"><span data-stu-id="93fd0-213">How to Meet WCAG 2.0</span></span>](https://www.w3.org/WAI/WCAG20/quickref/)

<span data-ttu-id="93fd0-214">Быстрая ссылка на рекомендации по доступности веб-контента (WCAG) 2.0 (критерии успешности) и методы.</span><span class="sxs-lookup"><span data-stu-id="93fd0-214">A quick reference to Web Content Accessibility Guidelines (WCAG) 2.0 requirements (success criteria) and techniques.</span></span>

#### [<a name="html-accessibility-api-mappings-10"></a><span data-ttu-id="93fd0-215">Сопоставления API API доступности HTML 1.0</span><span class="sxs-lookup"><span data-stu-id="93fd0-215">HTML Accessibility API Mappings 1.0</span></span>](https://www.w3.org/TR/html-aam-1.0/)

<span data-ttu-id="93fd0-216">В этом документе сопоставления W3C объясняется, как элемент HTML5.1 и атрибуты сопоставления с API доступности платформы.</span><span class="sxs-lookup"><span data-stu-id="93fd0-216">This W3C mappings document explains how HTML5.1 element and attributes map to platform accessibility APIs.</span></span>

#### [<a name="quick-tips"></a><span data-ttu-id="93fd0-217">Краткие советы</span><span class="sxs-lookup"><span data-stu-id="93fd0-217">Quick Tips</span></span>](http://a11yproject.com/#Quick-tips)

<span data-ttu-id="93fd0-218">Список советов по быстрому веб-разработке для доступности [проекта A11Y.](http://a11yproject.com/)</span><span class="sxs-lookup"><span data-stu-id="93fd0-218">A list of quick web development tips for accessibility by [The A11Y Project](http://a11yproject.com/).</span></span>

#### [<a name="site-scan"></a><span data-ttu-id="93fd0-219">Сканирование сайта</span><span class="sxs-lookup"><span data-stu-id="93fd0-219">Site Scan</span></span>](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

<span data-ttu-id="93fd0-220">Средство сканирования сайтов в Центре разработчиков Microsoft Edge проверяет наличие устарелих библиотек, проблем макета и проблем с доступностью.</span><span class="sxs-lookup"><span data-stu-id="93fd0-220">The Site Scan tool on Microsoft Edge Dev Center checks for out-of-date libraries, layout issues, and accessibility issues.</span></span>

#### [<a name="techniques-for-wcag-20"></a><span data-ttu-id="93fd0-221">Методы для WCAG 2.0</span><span class="sxs-lookup"><span data-stu-id="93fd0-221">Techniques for WCAG 2.0</span></span>](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

<span data-ttu-id="93fd0-222">Методы W3C, которые предоставляют рекомендации для веб-разработчиков по встрече с Рекомендациями по доступности веб-контента [(WCAG) 2.0](https://w3.org/TR/WCAG20/) критериев успешности.</span><span class="sxs-lookup"><span data-stu-id="93fd0-222">Techniques from the W3C that provide guidance for web developers on meeting [Web Content Accessibility Guidelines (WCAG) 2.0](https://w3.org/TR/WCAG20/) success criteria.</span></span>

#### [<a name="tips-on-developing-for-web-accessibility"></a><span data-ttu-id="93fd0-223">Советы по разработке для веб-доступности</span><span class="sxs-lookup"><span data-stu-id="93fd0-223">Tips on Developing for Web Accessibility</span></span>](https://w3.org/WAI/gettingstarted/tips/developing.html)

<span data-ttu-id="93fd0-224">Советы W3C по разработке веб-контента, доступного для людей с ограниченными возможностями.</span><span class="sxs-lookup"><span data-stu-id="93fd0-224">Tips from the W3C on developing web content that is more accessible to people with disabilities.</span></span>

#### [<a name="wai-aria-authoring-practices-11"></a><span data-ttu-id="93fd0-225">WAI-ARIA Authoring Practices 1.1</span><span class="sxs-lookup"><span data-stu-id="93fd0-225">WAI-ARIA Authoring Practices 1.1</span></span>](http://w3c.github.io/aria-practices/)

<span data-ttu-id="93fd0-226">Документ W3C, который предоставляет читателям представление об использовании WAI-ARIA 1.1 и рекомендует подходы, чтобы сделать виджеты, навигацию и поведение доступными с помощью ролей, состояния и свойств WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="93fd0-226">A document by the W3C that provides readers with an understanding of how to use WAI-ARIA 1.1 and recommends approaches to make widgets, navigation, and behaviors accessible using WAI-ARIA roles, states, and properties.</span></span>

#### [<a name="wai-guidelines-and-techniques"></a><span data-ttu-id="93fd0-227">Рекомендации и методы WAI</span><span class="sxs-lookup"><span data-stu-id="93fd0-227">WAI Guidelines and Techniques</span></span>](https://w3.org/WAI/guid-tech.html)

<span data-ttu-id="93fd0-228">Серия рекомендаций и стандартов веб-доступности, разработанных WAI.</span><span class="sxs-lookup"><span data-stu-id="93fd0-228">A series of web accessibility guidelines and standards developed by the WAI.</span></span>  

#### [<a name="web-accessibility-evaluation-tools-list"></a><span data-ttu-id="93fd0-229">Список инструментов оценки доступности веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="93fd0-229">Web Accessibility Evaluation Tools List</span></span>](https://www.w3.org/WAI/ER/tools/index.html)

<span data-ttu-id="93fd0-230">Список средств оценки доступности веб-сайтов, которые помогут определить, соответствуют ли веб-сайты рекомендациям по доступности.</span><span class="sxs-lookup"><span data-stu-id="93fd0-230">A list of web accessibility evaluation tools to help determine if websites meet accessibility guidelines.</span></span>

#### [<a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a><span data-ttu-id="93fd0-231">Перспективы веб-доступности: изучение влияния и преимуществ для всех</span><span class="sxs-lookup"><span data-stu-id="93fd0-231">Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone</span></span>](https://w3.org/WAI/perspectives/)

<span data-ttu-id="93fd0-232">Серия коротких сиюмитных видео W3C о влиянии доступности и преимуществах для всех.</span><span class="sxs-lookup"><span data-stu-id="93fd0-232">A series of short situational videos by the W3C about the impact of accessibility and the benefits for everyone.</span></span>

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
