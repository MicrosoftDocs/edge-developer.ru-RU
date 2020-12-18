---
description: Начало работы с эмуляторами Удаленной отладки Surface Duo.
title: Начало работы с эмуляторами Удаленной отладки Surface Duo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, удаленная отладка, android, surface duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230653"
---
# Начало работы с эмуляторами Удаленной отладки Surface Duo  

В этой статье мы пошагово пройдите процесс удаленной отладки веб-содержимого в приложении [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] на эмуляторе [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] из экземпляра Microsoft Edge для настольных [компьютеров.][MicrosoftEdge]  Сведения об отладки на устройстве Surface Duo можно получить в нашем руководстве по удаленной [отладки устройств с Android.][DevtoolsRemoteDebuggingMain]  

## Перед началом работы

Установите [SDK Surface Duo][MicrosoftDownload100847] перед запуском эмулятора [Surface Duo.][DualScreenAndroidUseEmulator]  Дополнительные сведения см. в [подкайке Surface Duo SDK.][DualScreenAndroidGetDuoSdk]  

## Шаг 1. Перейдите к edge://inspect  

Откройте экземпляр Microsoft Edge на [настольном компьютере][MicrosoftEdge]и перейдите к `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Страница edge://inspect в Microsoft Edge на рабочем столе" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   Страница `edge://inspect` в Microsoft Edge на рабочем столе  
:::image-end:::

> [!NOTE]
> Если страница не распознает эмулятор `edge://inspect` [Surface Duo,][DualScreenAndroidUseEmulator]перезапустите эмулятор.  

## Шаг 2. Запуск эмулятора Surface Duo  

Запустите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]  Обратите внимание, что эмулятор отображает 2 различных экрана, запущенных на эмуляторе.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Эмулятор Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Эмулятор Surface Duo  
:::image-end:::  

## Шаг 3. Загрузка веб-содержимого в Microsoft Edge в эмуляторе Surface Duo  

На любом экране проведите пальцем вверх по области избранного эмулятора [Surface Duo,][DualScreenAndroidUseEmulator] чтобы отобразить ящик приложений.  Выберите **Edge,** чтобы запустить [приложение Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Приложение Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Приложение Microsoft Edge в эмуляторе Surface Duo  
:::image-end:::  

Перейдите на веб-сайт или в приложение, которое нужно отлалать в [приложении Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]  

## Шаг 4. Отладка веб-содержимого из эмулятора Surface Duo  

Переключиться обратно на настольный экземпляр [Microsoft Edge.][MicrosoftEdge]  Теперь `edge://inspect` на странице показан **SurfaceDuoEmulator** со списком открытых вкладок или [PWAS,][ProgressiveWebAppsIndex] запущенных в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, запущенного на эмуляторе" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   На странице отображается список открытых вкладок в приложении Microsoft Edge, запущенного `edge://inspect` на эмуляторе  
:::image-end:::  

> [!NOTE]
> Если **surfaceDuoEmulator** на странице не видно, попробуйте открыть или закрыть вкладки в приложении Microsoft Edge в эмуляторе `edge://inspect` Surface [Duo.][DualScreenAndroidUseEmulator] [][GooglePlayStoreAppsComMicrosoftEmmx]  Дополнительные действия по устранению неполадок см. в разделе ["Устранение неполадок" для устройств с Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]  

В списке открытых вкладок, запущенных **** на эмуляторе, выберите "Проверить" на вкладке с веб-содержимым для отладки.  Microsoft [Edge DevTools][DevtoolsIndex] откроется в новом окне.  Выберите **«Toggle Screencast** \( Toggle Screencast \), чтобы просмотреть веб-содержимое из эмулятора Surface Duo в окне ![ ][ImageToggleScreencastIcon] DevTools. [][DualScreenAndroidUseEmulator]  Теперь вы можете использовать Microsoft Edge DevTools для отладки веб-содержимого в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo  
:::image-end:::  

> [!NOTE]
> Если приложение [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] охватывает оба экрана эмулятора, экранная трансляция будет отражать новый размер приложения, но не hinge.  Чтобы понять, как hinge влияет на макет веб-содержимого, используйте эмулятор [Surface Duo][DualScreenAndroidUseEmulator] вместо экранной трансляции.  

## Дополнительные ресурсы  

Интернет — это отличная платформа для нового класса папок и двухэкранных устройств, так как вы можете написать HTML, CSS и JavaScript один раз и сделать его отличным на одноэкранных, двухэкранных и папок устройствах.  Дополнительные сведения см. в этих дополнительных ресурсах, чтобы начать создание веб-контента для этих новых устройств.  

*   [Документация по созданию приложений на двухэкранных устройствах][DualScreenIndex]  
*   [Объяснение веб-платформы Microsoft Edge для новых API для создания веб-функций на папок и двухэкранных устройствах][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Запись сеанса Дня разработчика Microsoft 365: создание двухэкранных режимов для веб-сайтов и веб-приложений][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Прогрессивное веб-приложение в Windows | Документы Майкрософт"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Начало работы с удаленной отладой устройств с Android | Документы Майкрософт"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Устранение неполадок: DevTools не обнаруживает устройство с Android — начало работы с удаленной отладке устройств с Android | Документы Майкрософт"  

[DualScreenIndex]: /dual-screen/index "Создание приложений для двухэкранных устройств | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface DUo | Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Get the Surface Duo SDK | Документы Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Знакомство с новым Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Новый Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Скачать предварительный выпуск SDK Surface Duo | Центр загрузки Майкрософт"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: веб-браузер | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформы для поддержки на папок устройствах — MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Создание двухэкранных режимов для веб-сайтов и веб-приложений | YouTube"  
