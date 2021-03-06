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

# <a name="emulate-and-test-other-browsers"></a>Эмуляция и тестирование других браузеров  

Ваша работа не заканчивается обеспечением того, чтобы ваш сайт отлично работает в Microsoft Edge и Android.  Несмотря на то, что режим устройства способен имитировать ряд других устройств, таких как iPhone, мы рекомендуем вам проверить решения для эмуляции, предоставляемые другими браузерами.  

### <a name="summary"></a>Сводка  

*   Если у вас нет определенного устройства или вы хотите что-то проверить, лучше всего подражать устройству прямо в браузере.  
*   Эмуляторы и симуляторы устройств позволяют имитировать сайт разработки на различных устройствах с рабочей станции.  
*   Облачные эмуляторы позволяют автоматизировать тесты единиц для вашего сайта на разных платформах.  

## <a name="browser-emulators"></a>Эмуляторы браузера  

Эмуляторы браузера отлично подходит для тестирования отзывчивости сайта, но каждый из них не эмулирует различия в API, поддержке CSS и определенных действиях, отображаемых в мобильном браузере.  Проверьте свой сайт в браузерах, работающих на реальных устройствах, чтобы быть уверены, что все ведет себя так, как ожидалось.  

### <a name="firefox-responsive-design-view"></a>Представление дизайна с отзывчивым запросом на Firefox  

Firefox имеет [адаптивный][MDNResponsiveDesignMode] дизайн, который призывает вас перестать думать с точки зрения конкретных устройств и вместо этого изучить, как ваш дизайн меняется в общих размеров экрана или вашего собственного размера, перетаскивание края.  

### <a name="edgehtml-emulation"></a>Эмуляция EdgeHTML  

Чтобы подражать телефонам Windows, используйте встроенную эмуляцию Microsoft Edge \(EdgeHTML\). [][DevToolsEdgeHtmlEmulation]  

Используйте [эмуляцию IE 11 для][Ie11DevToolsEmulation] имитации того, как может выглядеть страница в более старых версиях Internet Explorer.  

## <a name="device-emulators-and-simulators"></a>Эмуляторы и симуляторы устройств  

Симуляторы устройств и эмуляторы имитируют не только среду браузера, но и все устройство.  Каждый из них полезен для тестирования вещей, которые требуют интеграции ОС, например ввода форм с виртуальными клавиатурами.  

### <a name="android-emulator"></a>Эмулятор Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

На данный момент нет способа установить Microsoft Edge на эмуляторе Android.  Тем не менее, вы можете использовать Android Browser, Chromium Content Shell и Firefox для Android, которые мы рассмотрели позже в этом руководстве.  Chromium Content Shell работает с тем же механизмом визуализации хрома, что и Microsoft Edge, но не имеет каких-либо специальных функций браузера.  

Эмулятор Android поставляется с SDK Android, который необходимо скачать в составе [Android Studio.][AndroidStudioDownload]  Затем выполните инструкции [по настройкам виртуального устройства][AndroidStudioCreateManageVirtualDevices] и [запуску эмулятора.][AndroidStudioRunAppsAndroidEmulator]  
После загрузки эмулятора выберите значок Браузер и проверьте свой сайт в старом браузере Stock для Android.  

#### <a name="chromium-content-shell-on-android"></a>Оболочка контента Chromium на Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Чтобы установить оболочку контента Chromium для Android, оставьте эмулятор запущенным и запустите следующую команду.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Теперь вы можете протестировать свой сайт с помощью оболочки контента Chromium.  

#### <a name="firefox-on-android"></a>Firefox на Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Как и в оболочке контента Chromium, вы можете получить AK для установки Firefox на эмулятор.  

[Скачайте правильный файл .apk][MozillaFirefoxDownload].  

Чтобы установить файл на открытый эмулятор или подключенное android-устройство, запустите следующую команду.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a>симулятор iOS  

Симулятор iOS для Mac OS X поставляется с Xcode, который [устанавливается из App Store.][MacAppStoreXcode]  

После этого узнайте, как работать с симулятором с помощью документации [разработчика Apple.][AppleSimulatorHelp]  

> [!NOTE]
> Чтобы не открывать Xcode каждый раз, когда необходимо использовать симулятор iOS, откройте его, наведите курсор на значок симулятора iOS в доке, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Keep in Dock**.  Теперь просто выберите значок всякий раз, когда это нужно.  

###  <a name="microsoft-edge-edgehtml"></a>Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Современный IE VM" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   Современный IE VM  
:::image-end:::  

Виртуальные машины Microsoft Edge \(EdgeHTML\) позволяют получать доступ к различным версиям EdgeHTML и IE на компьютере с помощью VirtualBox \(или VMWare\).  Выберите [виртуальную машину на странице загрузки.][MicrosoftDeveloperEdgeVms]  

## <a name="cloud-based-emulators-and-simulators"></a>Облачные эмуляторы и симуляторы  

Если вы не можете использовать эмуляторы и не имеете доступа к реальным устройствам, то облачные эмуляторы — это следующая лучшая вещь.  Большое преимущество облачных эмуляторов перед реальными устройствами и локальными эмуляторами заключается в том, что вы можете автоматизировать тесты единиц для вашего сайта на разных платформах.  

*   [BrowserStack (коммерческий)][|::ref1::|] является самым простым в использовании для ручного тестирования.  Вы выбираете операционную систему, выбираете версию браузера и тип устройства, выберите URL-адрес для просмотра, и она раскручивает виртуальную машину, с которой вы можете взаимодействовать.  Вы также можете запускать несколько эмуляторов на одном экране, что позволяет одновременно протестировать внешний вид приложения на нескольких устройствах.  
*   [SauceLabs (коммерческий)][SauceLabs] позволяет запускать блок-тесты внутри эмулятора, которые могут быть действительно полезны для скриптов потока через ваш сайт и просмотра видеозаписи этого на различных устройствах.  Кроме того, вы можете делать ручное тестирование на своем сайте.  
*   [Device Anywhere (коммерческий)][AppExperience] использует не эмуляторы, а реальные устройства, которые можно управлять удаленно.  Это очень полезно в случае, если вам необходимо воспроизвести проблему на определенном устройстве и не отображать ошибку с помощью каких-либо параметров в предыдущих руководствах.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

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
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) находится здесь и является автором [Meggin Kearney][MegginKearney] \(Tech Writer\) и Пол [Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Средства, производительность, анимация, UX\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
