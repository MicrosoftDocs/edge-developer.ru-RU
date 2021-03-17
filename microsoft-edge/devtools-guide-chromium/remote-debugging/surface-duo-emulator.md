---
description: Начало работы с эмуляторами Surface Duo удаленного отладки.
title: Начало работы с эмуляторами Surface Duo удаленного отладки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, remote debugging, Android, surface duo
ms.openlocfilehash: 61f903a5b929b7ee7b924938cf6ddc21a9783ca7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439332"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="2bd8f-104">Начало работы с эмуляторами Surface Duo удаленного отладки</span><span class="sxs-lookup"><span data-stu-id="2bd8f-104">Get started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="2bd8f-105">В этой статье вы проходите процесс удаленной отладки веб-контента в [приложении Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] в эмуляторе [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] из настольного экземпляра [Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="2bd8f-106">Сведения о отладки на устройстве Surface Duo следуют в нашем руководстве по удаленной [отладки устройств Android.][DevtoolsRemoteDebuggingMain]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="2bd8f-107">Перед началом</span><span class="sxs-lookup"><span data-stu-id="2bd8f-107">Before you Begin</span></span>

<span data-ttu-id="2bd8f-108">Установите [SDK Surface Duo][MicrosoftDownload100847] перед запуском эмулятора [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2bd8f-109">Дополнительные сведения вы можете получить [в surface Duo SDK.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="2bd8f-110">Шаг 1. Перейдите к edge://inspect</span><span class="sxs-lookup"><span data-stu-id="2bd8f-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="2bd8f-111">Откройте экземпляр microsoft [Edge на рабочем][MicrosoftEdge]столе и перейдите к `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="2bd8f-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Страница edge://inspect Microsoft Edge на рабочем столе" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="2bd8f-113">Страница `edge://inspect` в Microsoft Edge на рабочем столе</span><span class="sxs-lookup"><span data-stu-id="2bd8f-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="2bd8f-114">Если страница `edge://inspect` не распознает эмулятор [Surface Duo,][DualScreenAndroidUseEmulator]перезапустите эмулятор.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="2bd8f-115">Шаг 2. Запуск эмулятора Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="2bd8f-116">Запустите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2bd8f-117">Обратите внимание, что эмулятор отображает 2 различных экрана, работающих на эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Эмулятор Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="2bd8f-119">Эмулятор Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="2bd8f-120">Шаг 3. Загрузка веб-контента в Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="2bd8f-121">На любом экране проведите пальцем вверх по подносу Избранное [эмулятора Surface Duo][DualScreenAndroidUseEmulator] для отображения ящика приложений.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="2bd8f-122">Выберите **Edge** для запуска [приложения Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Приложение Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="2bd8f-124">Приложение Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="2bd8f-125">Перейдите на веб-сайт или приложение, которое необходимо отлагировать в [приложении Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="2bd8f-126">Шаг 4. Отладка веб-контента из эмулятора Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="2bd8f-127">Переключение на настольный экземпляр [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="2bd8f-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="2bd8f-128">На `edge://inspect` странице теперь показан **surfaceDuoEmulator** со списком открытых вкладок или [PWAs,][ProgressiveWebAppsIndex] которые работают на эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, которое работает на эмуляторе" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="2bd8f-130">На странице отображается список открытых вкладок в `edge://inspect` приложении Microsoft Edge, которое работает на эмуляторе</span><span class="sxs-lookup"><span data-stu-id="2bd8f-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bd8f-131">Если **SurfaceDuoEmulator** не отображается на странице, попробуйте открыть или закрыть вкладки в `edge://inspect` [приложении Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] в эмуляторе [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="2bd8f-132">Дополнительные действия по устранению неполадок перейдите в раздел устранения неполадок [для устройств Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="2bd8f-133">Из списка открытых вкладок, запущенных на \*\*\*\* эмуляторе, выберите инспектировать на вкладке, на которую необходимо отладить веб-содержимое.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="2bd8f-134">Microsoft [Edge DevTools][DevtoolsIndex] откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="2bd8f-135">Выберите **toggle Screencast** \( Toggle Screencast \) для просмотра веб-контента из эмулятора Surface Duo в окне ![ ](../media/toggle-screencast-icon.msft.png) DevTools. [][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-135">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="2bd8f-136">Теперь вы можете использовать Microsoft Edge DevTools для отладки веб-контента в [эмуляторе Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="2bd8f-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="2bd8f-138">Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="2bd8f-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bd8f-139">Если приложение [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] будет охватывать оба экрана эмулятора, то скринкаст будет отражать новый размер приложения, но не петлю.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="2bd8f-140">Чтобы понять, как петля влияет на макет веб-контента, используйте эмулятор [Surface Duo,][DualScreenAndroidUseEmulator] а не скринкаст.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="2bd8f-141">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2bd8f-141">Additional Resources</span></span>  

<span data-ttu-id="2bd8f-142">Веб является отличной платформой для нового класса складных и двухэкранных устройств, так как вы можете написать HTML, CSS и JavaScript один раз и иметь отличный внешний вид на одноэкранных, двухэкранных и складных устройствах.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="2bd8f-143">Дополнительные сведения можно получить в следующих дополнительных ресурсах, чтобы начать создание веб-контента для этих новых устройств.</span><span class="sxs-lookup"><span data-stu-id="2bd8f-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="2bd8f-144">Документация по созданию приложений на устройствах с двойным экраном</span><span class="sxs-lookup"><span data-stu-id="2bd8f-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="2bd8f-145">Объяснение веб-платформы Microsoft Edge для новых API для создания веб-опытом на складных и двухэкранных устройствах</span><span class="sxs-lookup"><span data-stu-id="2bd8f-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="2bd8f-146">Запись сеанса Дня разработчика Microsoft 365: создание двухэкранных опытом для веб-сайтов и веб-приложений</span><span class="sxs-lookup"><span data-stu-id="2bd8f-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2bd8f-147">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2bd8f-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
