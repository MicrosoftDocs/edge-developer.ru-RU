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
# <span data-ttu-id="4aead-104">Начало работы с эмуляторами Удаленной отладки Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-104">Get Started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="4aead-105">В этой статье мы пошагово пройдите процесс удаленной отладки веб-содержимого в приложении [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] на эмуляторе [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] из экземпляра Microsoft Edge для настольных [компьютеров.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="4aead-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="4aead-106">Сведения об отладки на устройстве Surface Duo можно получить в нашем руководстве по удаленной [отладки устройств с Android.][DevtoolsRemoteDebuggingMain]</span><span class="sxs-lookup"><span data-stu-id="4aead-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <span data-ttu-id="4aead-107">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="4aead-107">Before you Begin</span></span>

<span data-ttu-id="4aead-108">Установите [SDK Surface Duo][MicrosoftDownload100847] перед запуском эмулятора [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="4aead-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="4aead-109">Дополнительные сведения см. в [подкайке Surface Duo SDK.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="4aead-109">For more information, see [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="4aead-110">Шаг 1. Перейдите к edge://inspect</span><span class="sxs-lookup"><span data-stu-id="4aead-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="4aead-111">Откройте экземпляр Microsoft Edge на [настольном компьютере][MicrosoftEdge]и перейдите к `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="4aead-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Страница edge://inspect в Microsoft Edge на рабочем столе" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="4aead-113">Страница `edge://inspect` в Microsoft Edge на рабочем столе</span><span class="sxs-lookup"><span data-stu-id="4aead-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="4aead-114">Если страница не распознает эмулятор `edge://inspect` [Surface Duo,][DualScreenAndroidUseEmulator]перезапустите эмулятор.</span><span class="sxs-lookup"><span data-stu-id="4aead-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <span data-ttu-id="4aead-115">Шаг 2. Запуск эмулятора Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="4aead-116">Запустите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="4aead-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="4aead-117">Обратите внимание, что эмулятор отображает 2 различных экрана, запущенных на эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="4aead-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Эмулятор Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="4aead-119">Эмулятор Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <span data-ttu-id="4aead-120">Шаг 3. Загрузка веб-содержимого в Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="4aead-121">На любом экране проведите пальцем вверх по области избранного эмулятора [Surface Duo,][DualScreenAndroidUseEmulator] чтобы отобразить ящик приложений.</span><span class="sxs-lookup"><span data-stu-id="4aead-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="4aead-122">Выберите **Edge,** чтобы запустить [приложение Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="4aead-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Приложение Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="4aead-124">Приложение Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="4aead-125">Перейдите на веб-сайт или в приложение, которое нужно отлалать в [приложении Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="4aead-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <span data-ttu-id="4aead-126">Шаг 4. Отладка веб-содержимого из эмулятора Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="4aead-127">Переключиться обратно на настольный экземпляр [Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="4aead-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="4aead-128">Теперь `edge://inspect` на странице показан **SurfaceDuoEmulator** со списком открытых вкладок или [PWAS,][ProgressiveWebAppsIndex] запущенных в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="4aead-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, запущенного на эмуляторе" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="4aead-130">На странице отображается список открытых вкладок в приложении Microsoft Edge, запущенного `edge://inspect` на эмуляторе</span><span class="sxs-lookup"><span data-stu-id="4aead-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4aead-131">Если **surfaceDuoEmulator** на странице не видно, попробуйте открыть или закрыть вкладки в приложении Microsoft Edge в эмуляторе `edge://inspect` Surface [Duo.][DualScreenAndroidUseEmulator] [][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="4aead-131">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="4aead-132">Дополнительные действия по устранению неполадок см. в разделе ["Устранение неполадок" для устройств с Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="4aead-132">For additional troubleshooting steps, see the [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="4aead-133">В списке открытых вкладок, запущенных \*\*\*\* на эмуляторе, выберите "Проверить" на вкладке с веб-содержимым для отладки.</span><span class="sxs-lookup"><span data-stu-id="4aead-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="4aead-134">Microsoft [Edge DevTools][DevtoolsIndex] откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="4aead-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="4aead-135">Выберите **«Toggle Screencast** \( Toggle Screencast \), чтобы просмотреть веб-содержимое из эмулятора Surface Duo в окне ![ ][ImageToggleScreencastIcon] DevTools. [][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="4aead-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="4aead-136">Теперь вы можете использовать Microsoft Edge DevTools для отладки веб-содержимого в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="4aead-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="4aead-138">Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="4aead-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4aead-139">Если приложение [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] охватывает оба экрана эмулятора, экранная трансляция будет отражать новый размер приложения, но не hinge.</span><span class="sxs-lookup"><span data-stu-id="4aead-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="4aead-140">Чтобы понять, как hinge влияет на макет веб-содержимого, используйте эмулятор [Surface Duo][DualScreenAndroidUseEmulator] вместо экранной трансляции.</span><span class="sxs-lookup"><span data-stu-id="4aead-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <span data-ttu-id="4aead-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4aead-141">Additional Resources</span></span>  

<span data-ttu-id="4aead-142">Интернет — это отличная платформа для нового класса папок и двухэкранных устройств, так как вы можете написать HTML, CSS и JavaScript один раз и сделать его отличным на одноэкранных, двухэкранных и папок устройствах.</span><span class="sxs-lookup"><span data-stu-id="4aead-142">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="4aead-143">Дополнительные сведения см. в этих дополнительных ресурсах, чтобы начать создание веб-контента для этих новых устройств.</span><span class="sxs-lookup"><span data-stu-id="4aead-143">For more information, see these additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="4aead-144">Документация по созданию приложений на двухэкранных устройствах</span><span class="sxs-lookup"><span data-stu-id="4aead-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="4aead-145">Объяснение веб-платформы Microsoft Edge для новых API для создания веб-функций на папок и двухэкранных устройствах</span><span class="sxs-lookup"><span data-stu-id="4aead-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="4aead-146">Запись сеанса Дня разработчика Microsoft 365: создание двухэкранных режимов для веб-сайтов и веб-приложений</span><span class="sxs-lookup"><span data-stu-id="4aead-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

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
