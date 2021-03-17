---
description: Удаленное отладка живого контента на устройстве Android с компьютера Windows или macOS.
title: Начало работы по удаленной отладке устройств с Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 2beab5bf6d4b58dc93d883f5114e168213053e84
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439571"
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

# <a name="get-started-with-remote-debugging-android-devices"></a>Начало работы по удаленной отладке устройств с Android  

Удаленное отладка живого контента на устройстве Android с компьютера Windows или macOS.  На следующей странице руководства рассказывается о том, как выполнить следующие действия.  

*   Настройка устройства Android для удаленной отладки и обнаружение его на компьютере разработки.  
*   Проверка и отлаживка живого контента на устройстве Android на компьютере разработки.  
*   Содержимое screencast с устройства Android на экземпляр DevTools на компьютере разработки.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Удаленная отладка приложения Microsoft Edge на устройствах iOS в настоящее время не поддерживается.  В следующем руководстве основное внимание уделяется удаленной отладке Microsoft Edge на устройствах с Android.
> Если у вас есть macOS-устройство, выполните руководство по отладке [Brightcove,][BrightcoveSupportDebuggingMobileDevices] чтобы удаленно отладить Microsoft Edge на устройстве iOS с помощью Safari.  Дополнительные сведения о средстве веб-инспектора в Safari перейдите к [средствам веб-разработки Safari.][AppleDeveloperSafariTools]  

## <a name="step-1-discover-your-android-device"></a>Шаг 1. Откройте для себя устройство Android  

Рабочий процесс ниже работает для большинства пользователей.  Дополнительные справки можно найти в [разделе Устранение неполадок. В разделе DevTools](#troubleshooting-devtools-is-not-detecting-the-android-device) не обнаружен раздел устройства Android.  

1.  Откройте экран **Параметры разработчика** на Android.  Дополнительные сведения можно получить в меню Настройка параметров разработчика на [устройстве.][AndroidDeveloperStudioDevOptions]  
1.  Выберите **включить отладку USB.**  
1.  На компьютере разработки откройте Microsoft Edge.  
1.  Перейдите на `edge://inspect` страницу в Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Страница edge://inspect Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Рисунок 1.  Страница `edge://inspect` в Microsoft Edge  
    :::image-end:::  
    
1.  Подключите устройство Android непосредственно к компьютеру разработки с помощью USB-кабеля.  При первой попытке подключения следует отобразить подсказку о том, как DevTools обнаруживает неизвестное устройство.  Примите предложение **разрешить отладку USB** на устройстве Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Запрос разрешения разрешить отладку USB на устройстве Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Рисунок 2.  Запрос **разрешения разрешить отладку** USB на устройстве Android  
    :::image-end:::  
    
1.  Если отображается имя модели устройства Android, microsoft Edge успешно установила подключение к устройству.  Далее в [разделе Шаг 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a>Устранение неполадок: DevTools не обнаруживает устройство Android  

Воспользуйтесь следующими советами, которые помогут устранить ошибки в правильных настройках оборудования.  

*   Если вы используете концентратор USB, попробуйте подключить устройство Android непосредственно к компьютеру разработки.  
*   Попробуйте отключить USB-кабель между устройством Android и машиной разработки, а затем повторно подключить USB-кабель.  Выполните задачу, пока экраны android и машин разработки будут разблокированы.  
*   Убедитесь, что usb-кабель работает.  Вы должны иметь возможность проверять файлы на устройстве Android на компьютере разработки.  

Чтобы убедиться, что программное обеспечение настроено правильно, используйте следующие советы.  

*   Если на компьютере разработки работает Windows, попробуйте вручную установить драйверы USB для устройства Android.  Дополнительные сведения перейдите к [установке usb-драйверов OEM.][AndroidDeveloperToolsOemUsb]  
*   Некоторые сочетания устройств Windows и Android \(особенно Samsung\) требуют дополнительных параметров.  Дополнительные сведения можно получить в [DevTools Devices, не обнаруживающее][Stackoverflow21925992]устройство при подключении.  

Используйте следующие советы, чтобы помочь устранить неполадки, если на устройстве **Android** не отображается подсказка разрешить отладку USB.  

*   Отключение и повторное подключение USB-кабеля в то время как DevTools находится в центре внимания на вашем компьютере разработки и вашем домашнем экране Android показывает.  
    
    > [!NOTE]
    > Запрос отображается, если экраны android или компьютера разработки заблокированы.  

*   Обновление параметров отображения для устройства Android и машины разработки, чтобы каждый из них не заснул.  
*   Настройка режима USB для Android для PTP.  Дополнительные сведения: перейдите в Galaxy S4 не показывает диалоговое окно [авторизации отладки USB.][StackexchangeAndroid101933]  
*   Чтобы **сбросить** его в новое состояние, выберите отладку usb-отладки с экрана **"Параметры** разработчика" на устройстве Android.  

Если решение, которое не упоминается на этой странице или в [Устройствах DevTools,][Stackoverflow21925992] не обнаруживает устройство при подключении к переполнению стека, добавьте решение к вопросу переполнения стека.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->.  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a>Шаг 2. Отлаговка контента на устройстве Android с компьютера разработки  

1.  Откройте Microsoft Edge на устройстве Android.  
1.  Перейдите к , отображается имя модели устройства Android, а `edge://inspect` затем серийный номер устройства.  Ниже следует отобразить версию Microsoft Edge, запущенную на устройстве, с номером версии в скобки.  Каждая открытая вкладка Microsoft Edge получает уникальный раздел.  Вы можете взаимодействовать с этой вкладке из раздела.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Подключенное удаленное устройство" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Рисунок 3.  Подключенное удаленное устройство  
    :::image-end:::  
    
1.  В **вкладке Открыть с текстовым полем URL-адреса** введите URL-адрес и выберите **Открыть**.  Страница открывается в новой вкладке на устройстве Android.  
1.  Выберите **проверку** рядом с только что открываемой URL-адресом.  Открывается новый экземпляр DevTools.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a>Другие действия: фокус, обновление или закрытие вкладки  

Выберите **вкладку фокуса,** **перезагрузить**или закрыть рядом со вкладками, которые необходимо сосредоточиться, обновить или закрыть. ****  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Кнопки фокусии, обновления или закрытия вкладки" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Рисунок 4.  Кнопки фокусии, обновления или закрытия вкладки  
:::image-end:::  

### <a name="inspect-elements"></a>Проверка элементов  

Перейдите к **инструменту Elements** экземпляра DevTools и наведите курсор на элемент, чтобы выделить его в представлении устройства Android.  

Вы также можете выбрать элемент на экране устройства Android, чтобы выбрать его в **средстве Elements.**  Выберите **элемент** \( Выберите элемент \) значок в экземпляре ![ DevTools, а затем выберите элемент ](../media/select-element-icon.msft.png) на экране устройства Android.  

> [!NOTE]
> **Элемент Select** отключен после первого выбора, поэтому необходимо повторно включить его каждый раз, когда вы хотите использовать эту функцию.  

### <a name="screencast-your-android-screen-to-your-development-machine"></a>Screencast your Android screen to your development machine  

Выберите **значок Toggle Screencast** \( Toggle Screencast \) для просмотра содержимого устройства Android в экземпляре ![ ](../media/toggle-screencast-icon.msft.png) DevTools.  

Вы можете взаимодействовать со скринкастом следующими способами.  

*   Выборы переводятся в касания, выпустив соответствующие сенсорные события на устройстве.  
*   Клавиши на компьютере отправляются на устройство.  
*   Чтобы смоделировать жест щепотки, `Shift` удерживайте во время перетаскивание.  
*   Для прокрутки используйте трекпад или колесо мыши или найдите указатель мыши.

> [!NOTE]
> Используйте следующие советы, чтобы помочь вам скринкаст.  
> 
> *   Screencasts отображает только содержимое страницы.  Прозрачные части экрана представляют интерфейсы устройств, такие как адресная стойка Microsoft Edge, панели состояния Android или клавиатура Android.  
> *   Screencasts отрицательно влияет на частоту кадров.  Отключение скринкастинга при измерении свитков или анимаций, чтобы получить более точное представление о производительности страницы.  
> *   Если экран устройства Android блокируется, содержимое экрана исчезает.  Разблокировать экран устройства Android, чтобы автоматически возобновить скринкаст.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Настройка параметров разработчика на устройстве | Разработчик Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB OEM | Разработчики Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Средства веб-разработки Safari | Разработчик Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Отладка на мобильных устройствах | Поддержка Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb — Android Enthusiast Stack Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Устройства DevTools не обнаруживают устройство при подключении ."  

> [!NOTE]
> Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].  
> Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
