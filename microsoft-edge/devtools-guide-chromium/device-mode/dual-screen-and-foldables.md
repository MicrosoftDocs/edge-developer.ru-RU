---
description: Используйте виртуальные устройства в Microsoft Edge для улучшения веб-сайта для двухэкранных и папок устройств.
title: Эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эмуляция, устройство, моделирование, мобильный, двухэкранный режим, папка, Surface Dual, Surface Duo, Папка с двумя экранами
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313325"
---
# Эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools  

В Microsoft Edge версии 89 или более поздней можно эмулировать следующие двухэкранные и папки устройств.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Папка "Сумяно"][SamsungMobileGalaxyFold]  
    
Эмулируете устройства и перенимаете следующие положения.  

*   Одноэкранное или сложенное положение  
*   Двухэкранное или развернутое положение  
    
[](#turn-on-experimental-apis) Включите экспериментальные API веб-платформы и используйте функцию [CSS media screen-spanning][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для улучшения веб-сайта \(или app\) для двухэкранных и папок устройств.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Эмуляция Surface Duo в Microsoft Edge  
:::image-end:::  

## Включить экспериментальные API  

Чтобы использовать функцию прокрутки экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments,][DualScreenDocsJSAPI]включите флаг `Experimental Web Platform features` в Microsoft Edge.  Выполните следующие действия.  

1.  Перейдите к `edge://flags` .  
1.  In the **Search flags** textbox, `Experimental Web Platform features` enter, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.  
1.  Перезапустите Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Включить флаг экспериментальной веб-платформы" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Включить флаг **экспериментальной веб-платформы**  
:::image-end:::  

> [!NOTE]
> Если вы используете запросы мультимедиа [CSS][DualScreenDocsCssMedia] или API-код нумерации сегментов [JavaScript для][DualScreenDocsJSAPI] улучшения веб-сайта **** или приложения [для Surface Duo,][SurfaceDevicesDuo]необходимо также включить флаг экспериментальной веб-платформы в приложении [Microsoft Edge][GooglePlayMicrosoftEdge] для Android на устройстве [Surface Duo.][SurfaceDevicesDuo]  
> 
> Если **** флаг экспериментальной веб-платформы включен в настольном [microsoft Edge][MicrosoftEdge] и отключен в приложении Microsoft Edge для [Android,][GooglePlayMicrosoftEdge]поведение вашего веб-сайта или приложения в эмуляторе Surface Duo на настольном компьютере Microsoft Edge не совпадает с приложением [Microsoft Edge для Android][GooglePlayMicrosoftEdge] на Surface [Duo.][SurfaceDevicesDuo]  Убедитесь, что флаги совпадают в Android и на настольном компьютере Microsoft Edge, чтобы успешно использовать эмулятор Surface Duo на [настольном компьютере Microsoft Edge.][MicrosoftEdge]  

## Тестирование на устройствах с двумя экранами и папок  

Когда вы эмулируете [Surface Duo][SurfaceDevicesDuo] в режиме двойного экрана в Microsoft Edge, на вашем веб-сайте или в приложении нарисовка пространства между двумя экранами.  

Эмулированный дисплей соответствует способу отображения веб-сайта \(или приложения\) в приложении [Microsoft Edge для Android][GooglePlayMicrosoftEdge] во время работы на Surface [Duo.][SurfaceDevicesDuo]  Возможно, вам придется обновить свой веб-сайт \(или приложение\), чтобы лучше отображаться на этом пути.  Дополнительные сведения об адаптации веб-сайта \(или приложения\) [][DualScreenIntroductionHowWorkSeam]к скайму см. в подмыве.  

Панель [инструментов устройства содержит][DevtoolsDeviceModeIndexSimulateMobileViewport] дополнительные функции, которые помогут вам протестировать веб-сайт или приложение в различных положениях и ориентациях.  Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation. Объединяйте эту функцию с **Span** \( Span \) для перекладки между одноэкранным режимом, сворачиваемой и двухэкранной или ![ ](../media/span-dark-icon.msft.png) развернутой осями.  Вместе эти функции позволяют тестировать веб-сайт или приложение во всех четырех возможных положениях и ориентациях.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица положения и ориентации для двухэкранных и папок устройств" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Матрица положения и ориентации для двухэкранных и папок устройств  
:::image-end:::  

Значок **экспериментальной** веб-платформы \( ExperimentalApis \) отображает состояние флага экспериментальной ![ ](../media/experimental-apis-dark-icon.msft.png) **веб-платформы.**  Если флаг включен, значок выделяется.  Если флаг отключен, значок не выделяется.  Чтобы включить \(или выключение\) флага, либо выберите значок, либо перейдите к флагу и `edge://flags` переключите его.  

> [!NOTE]
> Ниже приводится список текущих известных проблем.  
> 
> *   Если вы используете клиент [удаленного][RemoteDesktopClientDocs] рабочего стола Майкрософт для подключения к удаленному компьютеру и эмулиации [папки Surface Duo][SurfaceDevicesDuo] или [Windows,][SamsungMobileGalaxyFold]указатель может встряхнуться или перебор.  Если у вас проблема, отправьте [отзыв.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Дополнительные ресурсы  

Вот дополнительные ресурсы, которые могут помочь вам улучшить веб-сайт \(или приложение\) для двухэкранных устройств.  

*   Дополнительные сведения о веб-разработке на двухэкранных устройствах можно найти в двухэкранных [веб-приложениях.][DualScreenWebIndex]  
*   Установите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]  Эмулятор Surface Duo отличается от эмулятора в Microsoft Edge, запускает Android и интегрируется с [Android Studio.][AndroidDeveloperStudio]  Для получения дополнительных сведений перейдите к [get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств в режиме устройства в Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для двухэкранного обнаружения | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Папка | Сума"  
