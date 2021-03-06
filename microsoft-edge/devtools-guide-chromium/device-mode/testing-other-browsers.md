---
description: Ваша работа не заканчивается обеспечением того, чтобы ваш сайт отлично работает в Microsoft Edge и Android.  Несмотря на то, что режим устройства способен имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам проверить решения для эмуляции, предоставляемые другими браузерами.
title: Эмуляция и тестирование других браузеров
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6b1239db373bd13d798ac90ac47a10878d07cdcb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398688"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="emulate-and-test-other-browsers"></a><span data-ttu-id="bbb4b-105">Эмуляция и тестирование других браузеров</span><span class="sxs-lookup"><span data-stu-id="bbb4b-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="bbb4b-106">Ваша работа не заканчивается обеспечением того, чтобы ваш сайт отлично работает в Microsoft Edge и Android.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="bbb4b-107">Несмотря на то, что режим устройства способен имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам проверить решения для эмуляции, предоставляемые другими браузерами.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <a name="summary"></a><span data-ttu-id="bbb4b-108">Сводка</span><span class="sxs-lookup"><span data-stu-id="bbb4b-108">Summary</span></span>  

*   <span data-ttu-id="bbb4b-109">Если у вас нет определенного устройства или вы хотите что-то проверить, лучше всего подражать устройству прямо в браузере.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="bbb4b-110">Эмуляторы и симуляторы устройств позволяют имитировать сайт разработки на различных устройствах с рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="bbb4b-111">Облачные эмуляторы позволяют автоматизировать тесты единиц для вашего сайта на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <a name="browser-emulators"></a><span data-ttu-id="bbb4b-112">Эмуляторы браузера</span><span class="sxs-lookup"><span data-stu-id="bbb4b-112">Browser emulators</span></span>  

<span data-ttu-id="bbb4b-113">Эмуляторы браузера отлично подходит для тестирования отзывчивости сайта, но каждый из них не эмулирует различия в API, поддержке CSS и определенных действиях, отображаемых в мобильном браузере.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that is displayed on a mobile browser.</span></span>  <span data-ttu-id="bbb4b-114">Проверьте свой сайт в браузерах, работающих на реальных устройствах, чтобы быть уверены, что все ведет себя так, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <a name="firefox-responsive-design-view"></a><span data-ttu-id="bbb4b-115">Представление дизайна с отзывчивым запросом на Firefox</span><span class="sxs-lookup"><span data-stu-id="bbb4b-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="bbb4b-116">Firefox имеет [адаптивный][MDNResponsiveDesignMode] дизайн, который призывает вас перестать думать с точки зрения конкретных устройств и вместо этого изучить, как ваш дизайн меняется в общих размеров экрана или вашего собственного размера, перетаскивание края.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <a name="edgehtml-emulation"></a><span data-ttu-id="bbb4b-117">Эмуляция EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="bbb4b-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="bbb4b-118">Чтобы подражать телефонам Windows, используйте встроенную эмуляцию Microsoft Edge \(EdgeHTML\). [][DevToolsEdgeHtmlEmulation]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="bbb4b-119">Используйте [эмуляцию IE 11 для][Ie11DevToolsEmulation] имитации того, как может выглядеть страница в более старых версиях Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <a name="device-emulators-and-simulators"></a><span data-ttu-id="bbb4b-120">Эмуляторы и симуляторы устройств</span><span class="sxs-lookup"><span data-stu-id="bbb4b-120">Device emulators and simulators</span></span>  

<span data-ttu-id="bbb4b-121">Симуляторы устройств и эмуляторы имитируют не только среду браузера, но и все устройство.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="bbb4b-122">Каждый из них полезен для тестирования вещей, которые требуют интеграции ОС, например ввода форм с виртуальными клавиатурами.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <a name="android-emulator"></a><span data-ttu-id="bbb4b-123">Эмулятор Android</span><span class="sxs-lookup"><span data-stu-id="bbb4b-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="bbb4b-124">На данный момент нет способа установить Microsoft Edge на эмуляторе Android.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="bbb4b-125">Тем не менее, вы можете использовать Android Browser, Chromium Content Shell и Firefox для Android, которые мы рассмотрели позже в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="bbb4b-126">Chromium Content Shell работает с тем же механизмом визуализации хрома, что и Microsoft Edge, но не имеет каких-либо специальных функций браузера.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="bbb4b-127">Эмулятор Android поставляется с SDK Android, который необходимо скачать в составе [Android Studio.][AndroidStudioDownload]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="bbb4b-128">Затем выполните инструкции [по настройкам виртуального устройства][AndroidStudioCreateManageVirtualDevices] и [запуску эмулятора.][AndroidStudioRunAppsAndroidEmulator]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="bbb4b-129">После загрузки эмулятора выберите значок Браузер и проверьте свой сайт в старом браузере Stock для Android.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-129">Once your emulator is booted, choose on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <a name="chromium-content-shell-on-android"></a><span data-ttu-id="bbb4b-130">Оболочка контента Chromium на Android</span><span class="sxs-lookup"><span data-stu-id="bbb4b-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="bbb4b-131">Чтобы установить оболочку контента Chromium для Android, оставьте эмулятор запущенным и запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="bbb4b-132">Теперь вы можете протестировать свой сайт с помощью оболочки контента Chromium.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <a name="firefox-on-android"></a><span data-ttu-id="bbb4b-133">Firefox на Android</span><span class="sxs-lookup"><span data-stu-id="bbb4b-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="bbb4b-134">Как и в оболочке контента Chromium, вы можете получить AK для установки Firefox на эмулятор.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="bbb4b-135">[Скачайте правильный файл .apk][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="bbb4b-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="bbb4b-136">Чтобы установить файл на открытый эмулятор или подключенное android-устройство, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a><span data-ttu-id="bbb4b-137">симулятор iOS</span><span class="sxs-lookup"><span data-stu-id="bbb4b-137">iOS simulator</span></span>  

<span data-ttu-id="bbb4b-138">Симулятор iOS для Mac OS X поставляется с Xcode, который [устанавливается из App Store.][MacAppStoreXcode]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="bbb4b-139">После этого узнайте, как работать с симулятором с помощью документации [разработчика Apple.][AppleSimulatorHelp]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="bbb4b-140">Чтобы не открывать Xcode каждый раз, когда необходимо использовать симулятор iOS, откройте его, наведите курсор на значок симулятора iOS в доке, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Keep in Dock**.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, hover on the iOS Simulator icon in your dock, open the contextual menu \(right-click\), and choose **Keep in Dock**.</span></span>  <span data-ttu-id="bbb4b-141">Теперь просто выберите значок всякий раз, когда это нужно.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-141">Now just choose the icon whenever you need it.</span></span>  

###  <a name="microsoft-edge-edgehtml"></a><span data-ttu-id="bbb4b-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="bbb4b-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Современный IE VM" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="bbb4b-144">Современный IE VM</span><span class="sxs-lookup"><span data-stu-id="bbb4b-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="bbb4b-145">Виртуальные машины Microsoft Edge \(EdgeHTML\) позволяют получать доступ к различным версиям EdgeHTML и IE на компьютере с помощью VirtualBox \(или VMWare\).</span><span class="sxs-lookup"><span data-stu-id="bbb4b-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="bbb4b-146">Выберите [виртуальную машину на странице загрузки.][MicrosoftDeveloperEdgeVms]</span><span class="sxs-lookup"><span data-stu-id="bbb4b-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <a name="cloud-based-emulators-and-simulators"></a><span data-ttu-id="bbb4b-147">Облачные эмуляторы и симуляторы</span><span class="sxs-lookup"><span data-stu-id="bbb4b-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="bbb4b-148">Если вы не можете использовать эмуляторы и не имеете доступа к реальным устройствам, то облачные эмуляторы — это следующая лучшая вещь.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="bbb4b-149">Большое преимущество облачных эмуляторов перед реальными устройствами и локальными эмуляторами заключается в том, что вы можете автоматизировать тесты единиц для вашего сайта на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="bbb4b-150">[BrowserStack (коммерческий)][|::ref1::|] является самым простым в использовании для ручного тестирования.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="bbb4b-151">Вы выбираете операционную систему, выбираете версию браузера и тип устройства, выберите URL-адрес для просмотра, и она раскручивает виртуальную машину, с которой вы можете взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="bbb4b-152">Вы также можете запускать несколько эмуляторов на одном экране, что позволяет одновременно протестировать внешний вид приложения на нескольких устройствах.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="bbb4b-153">[SauceLabs (коммерческий)][SauceLabs] позволяет запускать блок-тесты внутри эмулятора, которые могут быть действительно полезны для скриптов потока через ваш сайт и просмотра видеозаписи этого на различных устройствах.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="bbb4b-154">Кроме того, вы можете делать ручное тестирование на своем сайте.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="bbb4b-155">[Device Anywhere (коммерческий)][AppExperience] использует не эмуляторы, а реальные устройства, которые можно управлять удаленно.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="bbb4b-156">Это очень полезно в случае, если вам необходимо воспроизвести проблему на определенном устройстве и не отображать ошибку с помощью каких-либо параметров в предыдущих руководствах.</span><span class="sxs-lookup"><span data-stu-id="bbb4b-156">This is very useful in the event where you need to reproduce a problem on a specific device and may not display the bug using any of the options in the previous guides.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bbb4b-157">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="bbb4b-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML) — эмуляция | Документы Майкрософт"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Эмулировать браузеры, размеры экрана и расположения GPS | Документы Майкрософт"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Скачивание виртуальных машин"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Создание и управление виртуальными устройствами | Разработчики Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Скачайте инструменты Android Studio и SDK | Разработчики Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Запустите приложения в эмуляторе Android | Разработчики Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Опыт работы с приложениями"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Справка по симулятору — текущее | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode в Магазине приложений Mac"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Адаптивный режим | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Скачайте браузер Firefox"  
[SauceLabs]: https://saucelabs.com "Лаборатории соуса"  

> [!NOTE]
> <span data-ttu-id="bbb4b-171">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bbb4b-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bbb4b-172">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и Пол [Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Средства, производительность, анимация, UX\).</span><span class="sxs-lookup"><span data-stu-id="bbb4b-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bbb4b-174">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bbb4b-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
