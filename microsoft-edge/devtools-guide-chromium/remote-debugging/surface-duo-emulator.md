---
description: Начало работы с эмуляторами Surface Duo удаленного отладки.
title: Начало работы с эмуляторами Surface Duo удаленного отладки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, remote debugging, Android, surface duo
ms.openlocfilehash: a9696e63528a674d349b78fbdec2a1b804f61c49
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398016"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a>Начало работы с эмуляторами Surface Duo удаленного отладки  

В этой статье вы проходите процесс удаленной отладки веб-контента в [приложении Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] в эмуляторе [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] из настольного экземпляра [Microsoft Edge.][MicrosoftEdge]  Сведения о отладки на устройстве Surface Duo следуют в нашем руководстве по удаленной [отладки устройств Android.][DevtoolsRemoteDebuggingMain]  

## <a name="before-you-begin"></a>Перед началом

Установите [SDK Surface Duo][MicrosoftDownload100847] перед запуском эмулятора [Surface Duo.][DualScreenAndroidUseEmulator]  Дополнительные сведения вы можете получить [в surface Duo SDK.][DualScreenAndroidGetDuoSdk]  

## <a name="step-1-navigate-to-edgeinspect"></a>Шаг 1. Перейдите к edge://inspect  

Откройте экземпляр microsoft [Edge на рабочем][MicrosoftEdge]столе и перейдите к `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Страница edge://inspect Microsoft Edge на рабочем столе" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   Страница `edge://inspect` в Microsoft Edge на рабочем столе  
:::image-end:::

> [!NOTE]
> Если страница `edge://inspect` не распознает эмулятор [Surface Duo,][DualScreenAndroidUseEmulator]перезапустите эмулятор.  

## <a name="step-2-launch-the-surface-duo-emulator"></a>Шаг 2. Запуск эмулятора Surface Duo  

Запустите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]  Обратите внимание, что эмулятор отображает 2 различных экрана, работающих на эмуляторе.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Эмулятор Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Эмулятор Surface Duo  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a>Шаг 3. Загрузка веб-контента в Microsoft Edge в эмуляторе Surface Duo  

На любом экране проведите пальцем вверх по подносу Избранное [эмулятора Surface Duo][DualScreenAndroidUseEmulator] для отображения ящика приложений.  Выберите **Edge** для запуска [приложения Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Приложение Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Приложение Microsoft Edge в эмуляторе Surface Duo  
:::image-end:::  

Перейдите на веб-сайт или приложение, которое необходимо отлагировать в [приложении Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a>Шаг 4. Отладка веб-контента из эмулятора Surface Duo  

Переключение на настольный экземпляр [Microsoft Edge][MicrosoftEdge].  На `edge://inspect` странице теперь показан **surfaceDuoEmulator** со списком открытых вкладок или [PWAs,][ProgressiveWebAppsIndex] которые работают на эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, которое работает на эмуляторе" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   На странице отображается список открытых вкладок в `edge://inspect` приложении Microsoft Edge, которое работает на эмуляторе  
:::image-end:::  

> [!NOTE]
> Если **SurfaceDuoEmulator** не отображается на странице, попробуйте открыть или закрыть вкладки в `edge://inspect` [приложении Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]  Дополнительные действия по устранению неполадок перейдите в раздел устранения неполадок [для устройств Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]  

Из списка открытых вкладок, запущенных на **** эмуляторе, выберите инспектировать на вкладке, на которую необходимо отладить веб-содержимое.  Microsoft [Edge DevTools][DevtoolsIndex] откроется в новом окне.  Выберите **toggle Screencast** \( Toggle Screencast \) для просмотра веб-контента из эмулятора Surface Duo в окне ![ ][ImageToggleScreencastIcon] DevTools. [][DualScreenAndroidUseEmulator]  Теперь вы можете использовать Microsoft Edge DevTools для отладки веб-контента в [эмуляторе Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo  
:::image-end:::  

> [!NOTE]
> Если приложение [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] будет охватывать оба экрана эмулятора, то скринкаст будет отражать новый размер приложения, но не петлю.  Чтобы понять, как петля влияет на макет веб-контента, используйте эмулятор [Surface Duo,][DualScreenAndroidUseEmulator] а не скринкаст.  

## <a name="additional-resources"></a>Дополнительные ресурсы  

Веб является отличной платформой для нового класса складных и двухэкранных устройств, так как вы можете написать HTML, CSS и JavaScript один раз и иметь отличный внешний вид на одноэкранных, двухэкранных и складных устройствах.  Дополнительные сведения можно получить в следующих дополнительных ресурсах, чтобы начать создание веб-контента для этих новых устройств.  

*   [Документация по созданию приложений на устройствах с двойным экраном][DualScreenIndex]  
*   [Объяснение веб-платформы Microsoft Edge для новых API для создания веб-опытом на складных и двухэкранных устройствах][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Запись сеанса Дня разработчика Microsoft 365: создание двухэкранных опытом для веб-сайтов и веб-приложений][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Устранение неполадок. DevTools не обнаруживает устройство Android . Начало работы с удаленной отладки устройств Android | Документы Майкрософт"  

[DualScreenIndex]: /dual-screen/index "Создание приложений для устройств с двойным экраном | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Используйте эмулятор Surface DUo | Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите SDK-| Документы Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Представление нового microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Загрузка версии предварительного просмотра Surface Duo SDK | Центр загрузки Майкрософт"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: веб-браузер | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформы для просвещенного опыта на складных устройствах — MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Создание двухэкранных опытом для веб-сайта и веб-приложений | YouTube"  
