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
# <span data-ttu-id="38873-104">Эмуляция двухэкранных и папок устройств в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="38873-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="38873-105">В Microsoft Edge версии 89 или более поздней можно эмулировать следующие двухэкранные и папки устройств.</span><span class="sxs-lookup"><span data-stu-id="38873-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="38873-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="38873-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="38873-107">Папка "Сумяно"</span><span class="sxs-lookup"><span data-stu-id="38873-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="38873-108">Эмулируете устройства и перенимаете следующие положения.</span><span class="sxs-lookup"><span data-stu-id="38873-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="38873-109">Одноэкранное или сложенное положение</span><span class="sxs-lookup"><span data-stu-id="38873-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="38873-110">Двухэкранное или развернутое положение</span><span class="sxs-lookup"><span data-stu-id="38873-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="38873-111">[](#turn-on-experimental-apis) Включите экспериментальные API веб-платформы и используйте функцию [CSS media screen-spanning][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для улучшения веб-сайта \(или app\) для двухэкранных и папок устройств.</span><span class="sxs-lookup"><span data-stu-id="38873-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="38873-113">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38873-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <span data-ttu-id="38873-114">Включить экспериментальные API</span><span class="sxs-lookup"><span data-stu-id="38873-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="38873-115">Чтобы использовать функцию прокрутки экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments,][DualScreenDocsJSAPI]включите флаг `Experimental Web Platform features` в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38873-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="38873-116">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38873-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="38873-117">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="38873-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="38873-118">In the **Search flags** textbox, `Experimental Web Platform features` enter, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="38873-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="38873-119">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38873-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Включить флаг экспериментальной веб-платформы" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="38873-121">Включить флаг **экспериментальной веб-платформы**</span><span class="sxs-lookup"><span data-stu-id="38873-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="38873-122">Если вы используете запросы мультимедиа [CSS][DualScreenDocsCssMedia] или API-код нумерации сегментов [JavaScript для][DualScreenDocsJSAPI] улучшения веб-сайта \*\*\*\* или приложения [для Surface Duo,][SurfaceDevicesDuo]необходимо также включить флаг экспериментальной веб-платформы в приложении [Microsoft Edge][GooglePlayMicrosoftEdge] для Android на устройстве [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38873-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="38873-123">Если \*\*\*\* флаг экспериментальной веб-платформы включен в настольном [microsoft Edge][MicrosoftEdge] и отключен в приложении Microsoft Edge для [Android,][GooglePlayMicrosoftEdge]поведение вашего веб-сайта или приложения в эмуляторе Surface Duo на настольном компьютере Microsoft Edge не совпадает с приложением [Microsoft Edge для Android][GooglePlayMicrosoftEdge] на Surface [Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38873-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="38873-124">Убедитесь, что флаги совпадают в Android и на настольном компьютере Microsoft Edge, чтобы успешно использовать эмулятор Surface Duo на [настольном компьютере Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="38873-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <span data-ttu-id="38873-125">Тестирование на устройствах с двумя экранами и папок</span><span class="sxs-lookup"><span data-stu-id="38873-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="38873-126">Когда вы эмулируете [Surface Duo][SurfaceDevicesDuo] в режиме двойного экрана в Microsoft Edge, на вашем веб-сайте или в приложении нарисовка пространства между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="38873-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="38873-127">Эмулированный дисплей соответствует способу отображения веб-сайта \(или приложения\) в приложении [Microsoft Edge для Android][GooglePlayMicrosoftEdge] во время работы на Surface [Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38873-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="38873-128">Возможно, вам придется обновить свой веб-сайт \(или приложение\), чтобы лучше отображаться на этом пути.</span><span class="sxs-lookup"><span data-stu-id="38873-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="38873-129">Дополнительные сведения об адаптации веб-сайта \(или приложения\) [][DualScreenIntroductionHowWorkSeam]к скайму см. в подмыве.</span><span class="sxs-lookup"><span data-stu-id="38873-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="38873-130">Панель [инструментов устройства содержит][DevtoolsDeviceModeIndexSimulateMobileViewport] дополнительные функции, которые помогут вам протестировать веб-сайт или приложение в различных положениях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="38873-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="38873-131">Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="38873-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="38873-132">Объединяйте эту функцию с **Span** \( Span \) для перекладки между одноэкранным режимом, сворачиваемой и двухэкранной или ![ ](../media/span-dark-icon.msft.png) развернутой осями.</span><span class="sxs-lookup"><span data-stu-id="38873-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="38873-133">Вместе эти функции позволяют тестировать веб-сайт или приложение во всех четырех возможных положениях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="38873-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица положения и ориентации для двухэкранных и папок устройств" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="38873-135">Матрица положения и ориентации для двухэкранных и папок устройств</span><span class="sxs-lookup"><span data-stu-id="38873-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="38873-136">Значок **экспериментальной** веб-платформы \( ExperimentalApis \) отображает состояние флага экспериментальной ![ ](../media/experimental-apis-dark-icon.msft.png) **веб-платформы.**</span><span class="sxs-lookup"><span data-stu-id="38873-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="38873-137">Если флаг включен, значок выделяется.</span><span class="sxs-lookup"><span data-stu-id="38873-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="38873-138">Если флаг отключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="38873-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="38873-139">Чтобы включить \(или выключение\) флага, либо выберите значок, либо перейдите к флагу и `edge://flags` переключите его.</span><span class="sxs-lookup"><span data-stu-id="38873-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="38873-140">Ниже приводится список текущих известных проблем.</span><span class="sxs-lookup"><span data-stu-id="38873-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="38873-141">Если вы используете клиент [удаленного][RemoteDesktopClientDocs] рабочего стола Майкрософт для подключения к удаленному компьютеру и эмулиации [папки Surface Duo][SurfaceDevicesDuo] или [Windows,][SamsungMobileGalaxyFold]указатель может встряхнуться или перебор.</span><span class="sxs-lookup"><span data-stu-id="38873-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="38873-142">Если у вас проблема, отправьте [отзыв.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="38873-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <span data-ttu-id="38873-143">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="38873-143">Additional Resources</span></span>  

<span data-ttu-id="38873-144">Вот дополнительные ресурсы, которые могут помочь вам улучшить веб-сайт \(или приложение\) для двухэкранных устройств.</span><span class="sxs-lookup"><span data-stu-id="38873-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="38873-145">Дополнительные сведения о веб-разработке на двухэкранных устройствах можно найти в двухэкранных [веб-приложениях.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="38873-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="38873-146">Установите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="38873-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="38873-147">Эмулятор Surface Duo отличается от эмулятора в Microsoft Edge, запускает Android и интегрируется с [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="38873-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="38873-148">Для получения дополнительных сведений перейдите к [get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="38873-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="38873-149">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38873-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
