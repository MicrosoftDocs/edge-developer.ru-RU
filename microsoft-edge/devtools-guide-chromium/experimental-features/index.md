---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: fbdeeb08599285a9cfa6edd467282cfbabbadd74
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235481"
---
# <span data-ttu-id="38561-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="38561-104">Experimental features</span></span>  

<span data-ttu-id="38561-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="38561-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="38561-106">Вы можете протестировать и [предоставить отзыв](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.</span><span class="sxs-lookup"><span data-stu-id="38561-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="38561-107">Хотя экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="38561-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="38561-108">Включить экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="38561-108">Turn on experimental features</span></span>  

<span data-ttu-id="38561-109">Чтобы включить экспериментальную функцию \(или off\) в Microsoft Edge, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-110">[Откройте DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="38561-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="38561-111">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) или `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="38561-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="38561-112">Для получения дополнительных сведений перейдите к [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="38561-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="38561-113">Откройте области ["Параметры".][DevToolsCustomizeSettings]</span><span class="sxs-lookup"><span data-stu-id="38561-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="38561-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="38561-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="38561-115">Для получения дополнительных сведений перейдите в [Microsoft Edge DevTools сочетания клавиш][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="38561-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="38561-116">В левой части **области** "Параметры" выберите раздел **"Эксперименты".**</span><span class="sxs-lookup"><span data-stu-id="38561-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="38561-118">Список экспериментов в параметрах \*\*\*\* DevTools</span><span class="sxs-lookup"><span data-stu-id="38561-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="38561-119">На странице **"Эксперименты"** прокрутите список всех доступных экспериментальных функций и выберите этот элемент рядом с каждой функцией, которую нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="38561-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="38561-120">Закроют и снова откроете Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="38561-121">Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="38561-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="38561-122">Чтобы отключить экспериментальную функцию, откройте страницу **"Эксперименты"** и скройте контрольный элемент экспериментальной функции, которую нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="38561-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="38561-123">Основные экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="38561-123">Highlighted experimental features</span></span>  

<span data-ttu-id="38561-124">В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38561-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="38561-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="38561-125">Experimental feature</span></span> | <span data-ttu-id="38561-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38561-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="38561-127">Эмуляция: поддержка режима двойного экрана</span><span class="sxs-lookup"><span data-stu-id="38561-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="38561-128">84 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-128">84 or later</span></span> |  
| [<span data-ttu-id="38561-129">Включить новые функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38561-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="38561-130">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-130">85 or later</span></span> |  
| [<span data-ttu-id="38561-131">Поддержка перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="38561-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="38561-132">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-132">85 or later</span></span> |  
| [<span data-ttu-id="38561-133">Включить веб-вехин</span><span class="sxs-lookup"><span data-stu-id="38561-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="38561-134">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-134">85 or later</span></span> |  
| [<span data-ttu-id="38561-135">Включить сетевую консоль</span><span class="sxs-lookup"><span data-stu-id="38561-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="38561-136">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-136">85 or later</span></span> |  
| [<span data-ttu-id="38561-137">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="38561-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="38561-138">86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-138">86 or later</span></span> |  
| [<span data-ttu-id="38561-139">Включить редактор сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="38561-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="38561-140">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-140">87 or later</span></span> |  
| [<span data-ttu-id="38561-141">Включить составные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="38561-141">Turn on Composited Layers in 3D View</span></span>](#turn-on-composited-layers-in-3d-view) | <span data-ttu-id="38561-142">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="38561-142">87 or later</span></span> |  

### <span data-ttu-id="38561-143">Эмуляция: поддержка режима двойного экрана</span><span class="sxs-lookup"><span data-stu-id="38561-143">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="38561-144">Предоставляет дополнительные функции для эмуалации двух новых двух- и папок устройств в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38561-144">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="38561-145">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="38561-145">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="38561-146">Папка "Сумяно"</span><span class="sxs-lookup"><span data-stu-id="38561-146">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="38561-147">Эмулируете устройства и перенимаете следующие положения.</span><span class="sxs-lookup"><span data-stu-id="38561-147">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="38561-148">Одноэкранное или сложенное положение</span><span class="sxs-lookup"><span data-stu-id="38561-148">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="38561-149">Двухэкранное или развернутое положение</span><span class="sxs-lookup"><span data-stu-id="38561-149">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="38561-150">[](#enable-experimental-apis) Включить экспериментальные API веб-платформы и использовать функцию расширения экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для улучшения веб-сайта \(или app\) для двухэкранных и папок устройств.</span><span class="sxs-lookup"><span data-stu-id="38561-150">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="38561-152">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="38561-152">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="38561-153">Включить экспериментальные API</span><span class="sxs-lookup"><span data-stu-id="38561-153">Enable experimental APIs</span></span>  

<span data-ttu-id="38561-154">Чтобы использовать функцию прокрутки экрана мультимедиа [CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments,][DualScreenDocsJSAPI]включите флаг `Experimental Web Platform features` в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38561-154">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="38561-155">Выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-155">Complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-156">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="38561-156">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="38561-157">In the **Search flags** textbox, `Experimental Web Platform features` enter, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="38561-157">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="38561-158">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38561-158">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Включить флаг экспериментальной веб-платформы" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="38561-160">Включить флаг экспериментальной веб-платформы</span><span class="sxs-lookup"><span data-stu-id="38561-160">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="38561-161">Если вы используете запросы мультимедиа [CSS][DualScreenDocsCssMedia] или [API нумерации][DualScreenDocsJSAPI] сегментов JavaScript для улучшения веб-сайта \*\*\*\* или приложения [для Surface Duo,][SurfaceDevicesDuo]необходимо также включить флаг экспериментальной веб-платформы в приложении Microsoft Edge для [Android][GooglePlayMicrosoftEdge] на устройстве Surface [Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38561-161">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="38561-162">Если \*\*\*\* флаг экспериментальной веб-платформы включен в [microsoft Edge][MicrosoftEdge] на настольном компьютере и отключен в приложении Microsoft Edge для [Android,][GooglePlayMicrosoftEdge]поведение вашего веб-сайта или приложения в эмуляторе Surface Duo на настольном компьютере Microsoft Edge не совпадает с приложением [Microsoft Edge для Android][GooglePlayMicrosoftEdge] на Surface [Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38561-162">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="38561-163">Убедитесь, что флаги совпадают в Android и на настольном компьютере Microsoft Edge, чтобы успешно использовать эмулятор Surface Duo в настольном [Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="38561-163">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="38561-164">Тестирование на устройствах с двумя экранами и папок</span><span class="sxs-lookup"><span data-stu-id="38561-164">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="38561-165">Когда вы эмулируете [Surface Duo][SurfaceDevicesDuo] в режиме двойного экрана в Microsoft Edge, на вашем веб-сайте или в приложении прорисовка пространства между двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="38561-165">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="38561-166">Эмулированный дисплей соответствует способу отображения вашего веб-сайта (или приложения\) в приложении [Microsoft Edge для Android,][GooglePlayMicrosoftEdge] запущенном на [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="38561-166">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="38561-167">Возможно, вам придется обновить свой веб-сайт \(или приложение\), чтобы лучше отображаться на этом пути.</span><span class="sxs-lookup"><span data-stu-id="38561-167">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="38561-168">Дополнительные сведения об адаптации веб-сайта \(или приложения\) [][DualScreenIntroductionHowWorkSeam]к скайму см. в подмыве.</span><span class="sxs-lookup"><span data-stu-id="38561-168">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="38561-169">Панель [инструментов устройства содержит][DevtoolsDeviceModeIndexSimulateMobileViewport] дополнительные функции, которые помогут вам протестировать веб-сайт или приложение в различных положениях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="38561-169">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="38561-170">Choose **Rotate** \( ![ Rotate ][ImageRotateIcon] \) to rotate the viewport to landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="38561-170">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="38561-171">Объединяйте эту функцию с **Span** \( Span \) для перекладки между одноэкранным экраном или сдвойте экран или ![ ][ImageSpanIcon] развернутые положения.</span><span class="sxs-lookup"><span data-stu-id="38561-171">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="38561-172">Вместе эти функции позволяют тестировать веб-сайт или приложение во всех четырех возможных положениях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="38561-172">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица положения и ориентации для двухэкранных и папок устройств" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="38561-174">Матрица положения и ориентации для двухэкранных и папок устройств</span><span class="sxs-lookup"><span data-stu-id="38561-174">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="38561-175">Значок **экспериментальной** веб-платформы \( ExperimentalApis \) отображает состояние флага экспериментальной ![ ][ImageExperimentalApisIcon] **веб-платформы.**</span><span class="sxs-lookup"><span data-stu-id="38561-175">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="38561-176">Если флаг включен, значок выделяется.</span><span class="sxs-lookup"><span data-stu-id="38561-176">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="38561-177">Если флаг отключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="38561-177">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="38561-178">Чтобы включить \(или отключить\) флаг, перейдите к флагу и `edge://flags` переключите его.</span><span class="sxs-lookup"><span data-stu-id="38561-178">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="38561-179">Вот дополнительные ресурсы, которые могут помочь вам улучшить веб-сайт \(или приложение\) для двухэкранных устройств.</span><span class="sxs-lookup"><span data-stu-id="38561-179">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="38561-180">Дополнительные сведения о веб-разработке на двухэкранных устройствах можно найти в двухэкранных [веб-приложениях.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="38561-180">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="38561-181">Установите [эмулятор Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="38561-181">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="38561-182">Он отличается от эмулятора в Microsoft Edge, эмулирует Surface Duo под управлением Android и интегрируется с [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="38561-182">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="38561-183">Для получения дополнительных сведений перейдите к [get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="38561-183">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="38561-184">Ниже приводится список текущих известных проблем.</span><span class="sxs-lookup"><span data-stu-id="38561-184">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="38561-185">При использовании клиента [удаленного][RemoteDesktopClientDocs] рабочего стола Майкрософт для подключения к удаленному КОМПЬЮТЕРу и эмуалации [папки Surface Duo][SurfaceDevicesDuo] или [Windows 2013][SamsungMobileGalaxyFold]указатель может встряхнуться или перебор.</span><span class="sxs-lookup"><span data-stu-id="38561-185">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="38561-186">Если у вас проблема, отправьте [отзыв.](#providing-feedback-on-experimental-features)</span><span class="sxs-lookup"><span data-stu-id="38561-186">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="38561-187">Включить новые функции отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38561-187">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="38561-188">Эта экспериментальная функция предоставляет ряд новых визуализаций для отлаки макетов сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="38561-188">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="38561-189">Чтобы просмотреть последние экспериментальные функции, в [этом эксперименте необходимо](#turn-on-experimental-features) включить и перезагрузить DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-189">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="38561-190">Этот эксперимент по умолчанию в Microsoft Edge версии 87 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="38561-190">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="38561-191">Просмотр наложения сетки при наведении с помощью средства inspect</span><span class="sxs-lookup"><span data-stu-id="38561-191">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="38561-192">Средство **Inspect** позволяет быстро определять и визуализировать макеты сетки CSS на веб-сайте, наведении на них указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="38561-192">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="38561-193">Choose the **Inspect** \( ![ Inspect ][ImageInspectIcon] \) icon in the top-left corner of DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-193">Choose the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="38561-194">Затем наведите курсор на элемент Grid на веб-сайте, который вы отладили.</span><span class="sxs-lookup"><span data-stu-id="38561-194">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="38561-195">Контуры отображаются вокруг сетки, а затенение указывает расположение разрывов сетки, если они присутствуют.</span><span class="sxs-lookup"><span data-stu-id="38561-195">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Просмотр сеток с помощью средства inspect" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="38561-197">Просмотр сеток с помощью **средства inspect**</span><span class="sxs-lookup"><span data-stu-id="38561-197">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="38561-198">Просмотр наложения сохраняемой сетки</span><span class="sxs-lookup"><span data-stu-id="38561-198">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="38561-199">В Microsoft Edge версии 86 или более поздней версии экспериментальная функция сетки CSS также предлагает возможность включить постоянные наложения Grid.</span><span class="sxs-lookup"><span data-stu-id="38561-199">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="38561-200">Постоянные наложения предоставляют ряд преимуществ.</span><span class="sxs-lookup"><span data-stu-id="38561-200">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="38561-201">Постоянные наложения остаются видимыми на странице при прокрутке, движении мыши и использовании других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-201">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="38561-202">Одновременно можно включить несколько постоянных наложения, что позволяет просмотреть несколько макетов сетки одновременно.</span><span class="sxs-lookup"><span data-stu-id="38561-202">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="38561-203">Постоянные наложения предоставляют множество параметров конфигурации, таких как скрытие или отображение имен в области сетки, разрывы сетки, отслеживание размеров и так далее.</span><span class="sxs-lookup"><span data-stu-id="38561-203">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="38561-204">Два способа переналожения сохраняемой сетки.</span><span class="sxs-lookup"><span data-stu-id="38561-204">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="38561-205">Выберите **значок** овала Grid рядом с любым элементом Grid, показанным в дереве DOM **средства "Элементы".**</span><span class="sxs-lookup"><span data-stu-id="38561-205">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Значок овала сетки в средстве "Элементы"" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="38561-207">Значок овала сетки в **средстве "Элементы"**</span><span class="sxs-lookup"><span data-stu-id="38561-207">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="38561-208">Откройте новую панель **макета,** расположенную в средстве "Элементы", и выберите этот элемент рядом с каждым элементом Grid, который нужно выделить.</span><span class="sxs-lookup"><span data-stu-id="38561-208">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="38561-210">**Панель** макета в DevTools</span><span class="sxs-lookup"><span data-stu-id="38561-210">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="38561-211">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="38561-211">Configuring persistent overlays</span></span>  

<span data-ttu-id="38561-212">В Microsoft Edge версии 86 \*\*\*\* или более поздней версии новая панель \*\*\*\* макета расположена в средстве **"Элементы"** вместе со вкладками "Стили" и **"Вычисленные".**</span><span class="sxs-lookup"><span data-stu-id="38561-212">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="38561-213">Панель **макета** позволяет параметров конфигурации для постоянных наложения.</span><span class="sxs-lookup"><span data-stu-id="38561-213">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Функция отладки сетки CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="38561-215">Функция отладки сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38561-215">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="38561-216">Поддержка перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="38561-216">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="38561-217">Обычно такие средства, \*\*\*\* как \*\*\*\* элементы и сеть, могут открываться только на главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-217">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="38561-218">Такие **средства, как трехмерный** просмотр и проблемы, которые обычно открываются только на панели "Drawer", расположенной в нижней части DevTools. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="38561-218">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="38561-219">После выбора эксперимента можно переместить инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="38561-219">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="38561-220">Чтобы переместить средство, наведите курсор на вкладку, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Переместить** в верхнюю" или "Переместить **в нижнюю часть".**</span><span class="sxs-lookup"><span data-stu-id="38561-220">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="38561-221">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-221">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="38561-222">Чтобы показать или скрыть панель **"Drawer",** выберите `Escape` .</span><span class="sxs-lookup"><span data-stu-id="38561-222">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="38561-224">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="38561-224">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="38561-225">Включить веб-вехин</span><span class="sxs-lookup"><span data-stu-id="38561-225">Enable webhint</span></span>  

<span data-ttu-id="38561-226">[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="38561-226">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="38561-227">Тип отзыва, предоставляемого [веб-хиной.][WebhintMain]</span><span class="sxs-lookup"><span data-stu-id="38561-227">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="38561-228">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="38561-228">accessibility</span></span>  
*   <span data-ttu-id="38561-229">совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="38561-229">cross-browser compatibility</span></span>  
*   <span data-ttu-id="38561-230">безопасность"</span><span class="sxs-lookup"><span data-stu-id="38561-230">security</span></span>  
*   <span data-ttu-id="38561-231">производительность</span><span class="sxs-lookup"><span data-stu-id="38561-231">performance</span></span>  
*   <span data-ttu-id="38561-232">Progressive Web Apps (PWAs)</span><span class="sxs-lookup"><span data-stu-id="38561-232">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="38561-233">другие распространенные проблемы веб-разработки</span><span class="sxs-lookup"><span data-stu-id="38561-233">other common web development issues</span></span>  
    
<span data-ttu-id="38561-234">В [эксперименте webhint][WebhintMain] на панели "Проблемы" отображается обратная связь [веб-хинта.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="38561-234">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="38561-235">Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="38561-235">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="38561-236">Выберите ссылку на ресурс, чтобы открыть \*\*\*\* соответствующую **области** **"Сеть",**"Источники" или "Элементы" в DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-236">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="обратная связь веб-панелей на панели "Проблемы"" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="38561-238">обратная связь веб-панелей на **панели "Проблемы"**</span><span class="sxs-lookup"><span data-stu-id="38561-238">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="38561-239">Включить сетевую консоль</span><span class="sxs-lookup"><span data-stu-id="38561-239">Enable Network Console</span></span>  

<span data-ttu-id="38561-240">**Сетовая** консоль — это рабочий заголовок эксперимента по запросам искусственных сетей по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="38561-240">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="38561-241">Вы можете использовать эксперимент **с сетевой** консолью для отправки запросов веб-API.</span><span class="sxs-lookup"><span data-stu-id="38561-241">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="38561-242">После включения эксперимента убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-242">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="38561-243">Чтобы использовать **сетевую консоль,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-243">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-244">Откройте **сетевую** области.</span><span class="sxs-lookup"><span data-stu-id="38561-244">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="38561-245">Найдите сетевой запрос, который вы хотите изменить, и повторно.</span><span class="sxs-lookup"><span data-stu-id="38561-245">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="38561-246">Откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Изменить **и повторить".**</span><span class="sxs-lookup"><span data-stu-id="38561-246">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="38561-247">Когда **откроется сетовая консоль,** отредактируете сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="38561-247">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="38561-248">Choose **Send**.</span><span class="sxs-lookup"><span data-stu-id="38561-248">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Сетовая консоль в консоли" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="38561-250">**Сетовая** консоль в **консоли**</span><span class="sxs-lookup"><span data-stu-id="38561-250">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="38561-251">Просмотр исходных заказов</span><span class="sxs-lookup"><span data-stu-id="38561-251">Source Order Viewer</span></span>  

<span data-ttu-id="38561-252">**"Просмотр порядка источника"** — это эксперимент, который отображает порядок элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="38561-252">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="38561-253">Порядок отображения на экране может отличаться от порядка источника, что приводит к путанице для чтения с экрана и пользователей клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="38561-253">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="38561-254">Используйте эксперимент **"Просмотр порядка источника",** чтобы найти различия между порядком отображения на экране и порядком источника.</span><span class="sxs-lookup"><span data-stu-id="38561-254">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="38561-255">После включения эксперимента убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-255">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="38561-256">Чтобы использовать **"Просмотр порядка источника",** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-256">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-257">Откройте области **элементов.**</span><span class="sxs-lookup"><span data-stu-id="38561-257">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="38561-258">Откройте панель **"Accessibility"** (Доступность) на панели "Drawer \(bottom\)".</span><span class="sxs-lookup"><span data-stu-id="38561-258">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="38561-259">В разделе **"Просмотр порядка источника"** выберите **"Показать** порядок источника".</span><span class="sxs-lookup"><span data-stu-id="38561-259">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="38561-260">Выделяем любой htmL-элемент, чтобы отобразить наложение, которое является порядком в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="38561-260">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="38561-262">**Source Order Viewer** in the **Accessibility** pane</span><span class="sxs-lookup"><span data-stu-id="38561-262">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="38561-263">Включить редактор сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="38561-263">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="38561-264">После того **как включен** эксперимент "Включить редактор сочетания клавиш", вы можете настраивать сочетания клавиш для любого действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-264">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="38561-265">Чтобы настроить сочетания клавиш для определенного действия, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-265">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-266">[Откройте DevTools.][DevtoolsOpenMain]</span><span class="sxs-lookup"><span data-stu-id="38561-266">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="38561-267">Откройте ["Параметры".][DevToolsCustomizeSettings]</span><span class="sxs-lookup"><span data-stu-id="38561-267">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="38561-268">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="38561-268">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="38561-269">Перейдите на **страницу ярлыков.**</span><span class="sxs-lookup"><span data-stu-id="38561-269">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="38561-270">Выберите действие, настраиваемую.</span><span class="sxs-lookup"><span data-stu-id="38561-270">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="38561-271">Choose the **Edit** \( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \) icon.</span><span class="sxs-lookup"><span data-stu-id="38561-271">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выбор действия для настройки на странице "Ярлыки" в параметрах" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="38561-273">Выбор действия для настройки на странице **"Ярлыки"** в [параметрах][DevToolsCustomizeSettings]</span><span class="sxs-lookup"><span data-stu-id="38561-273">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="38561-274">На клавиатуре выберите ключи, которые нужно привязать к действию.</span><span class="sxs-lookup"><span data-stu-id="38561-274">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выбор ключей, которые нужно назначить действию" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="38561-276">Выбор ключей, которые нужно назначить действию</span><span class="sxs-lookup"><span data-stu-id="38561-276">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="38561-277">Чтобы сохранить новый ярлык клавиатуры, выберите контрольный знак \(</span><span class="sxs-lookup"><span data-stu-id="38561-277">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="38561-279">\) значок.</span><span class="sxs-lookup"><span data-stu-id="38561-279">\) icon.</span></span>
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Choose the checkmark icon to save your new keyboard shortcut" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="38561-281">Choose the checkmark icon to save your new keyboard shortcut</span><span class="sxs-lookup"><span data-stu-id="38561-281">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="38561-282">Выберите новый ярлык клавиатуры для запуска действия в DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-282">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="38561-283">На странице **"Ярлыки"** значок настраиваемой клавиатуры **\(** ![ CustomKeyboardShortcut \) отображает настроенные сочетания ][ImageCustomKeyboardShortcutIcon] клавиш.</span><span class="sxs-lookup"><span data-stu-id="38561-283">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="38561-284">Чтобы сбросить все ярлыки, выберите **"Восстановить ярлыки по умолчанию".**</span><span class="sxs-lookup"><span data-stu-id="38561-284">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="38561-285">При редактировании сочетания клавиш для действия, чтобы отменить изменения, выберите значок X \( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="38561-285">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="38561-286">Чтобы удалить ярлыки для определенного действия, выберите значок **Delete shortcut** \( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="38561-286">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="38561-287">Чтобы добавить несколько ярлыков для действия, выберите **"Добавить ярлык".**</span><span class="sxs-lookup"><span data-stu-id="38561-287">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="38561-288">Если ярлык клавиатуры в настоящее время назначен другому действию, вы не сможете сохранить его для нового действия.</span><span class="sxs-lookup"><span data-stu-id="38561-288">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="38561-289">Сначала необходимо удалить ярлык клавиатуры для предыдущего действия, а затем добавить его в новое действие.</span><span class="sxs-lookup"><span data-stu-id="38561-289">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->

### <span data-ttu-id="38561-290">Включить составные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="38561-290">Turn on Composited Layers in 3D View</span></span>

<span data-ttu-id="38561-291">Теперь можно визуализировать слои вместе с z-индексами и объектной моделью документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="38561-291">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="38561-292">Эта функция помогает отлакить без переключения контекстов так часто.</span><span class="sxs-lookup"><span data-stu-id="38561-292">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="38561-293">Вы определили, что уменьшение переключения контекста является серьезной проблемой.</span><span class="sxs-lookup"><span data-stu-id="38561-293">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="38561-294">Не всегда понятно, как код, который вы пишете, влияет на веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="38561-294">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="38561-295">Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.</span><span class="sxs-lookup"><span data-stu-id="38561-295">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  <span data-ttu-id="38561-296">После включения эксперимента убедитесь, что перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-296">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="38561-297">Чтобы использовать **составные слои,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="38561-297">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="38561-298">В средстве **"3D View"** выберите в этом оке средство.</span><span class="sxs-lookup"><span data-stu-id="38561-298">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="38561-299">Откройте области **составных** слоев.</span><span class="sxs-lookup"><span data-stu-id="38561-299">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="38561-300">Отображаются все закрашенные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="38561-300">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="38561-301">Попробуйте эту функцию с собственными веб-приложениями.</span><span class="sxs-lookup"><span data-stu-id="38561-301">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="38561-303">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="38561-303">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## <span data-ttu-id="38561-304">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="38561-304">Previous experimental features</span></span>  

*   <span data-ttu-id="38561-305">[3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="38561-305">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="38561-306">[Настройка сочетания клавиш теперь][DevtoolsCustomKeyboardShortcuts] доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="38561-306">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="38561-307">Предоставление обратной связи по экспериментальным функциям</span><span class="sxs-lookup"><span data-stu-id="38561-307">Providing feedback on experimental features</span></span>  

<span data-ttu-id="38561-308">Предоставление отзывов о экспериментах Microsoft Edge DevTools или других экспериментах, связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="38561-308">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="38561-309">Отправьте свой отзыв с помощью **значка отправки отзыва** в DevTools</span><span class="sxs-lookup"><span data-stu-id="38561-309">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="38561-310">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="38561-310">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="38561-312">Значок **отправки отзыва** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="38561-312">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageCheckmarkKeyboardShortcutIcon]: ../media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ../media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ../media/delete-keyboard-shortcut-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ../media/edit-keyboard-shortcut-icon.msft.png  
[ImageExperimentalApisIcon]: ../media/experimental-apis-dark-icon.msft.png  
[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ../media/span-dark-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ../media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevToolsCustomizeSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств в режиме устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevToolsShortcuts]: ../shortcuts/index.md "Microsoft Edge DevTools сочетания клавиш | Документы Майкрософт"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Настройка сочетания клавиш в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsOpenMain]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[DualScreenWebIndex]: /dual-screen/web/index "Двухэкранные веб-| Документы Майкрософт"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получите эмулятор Surface | Документы Майкрософт"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Как работать с обоймой — введение в двухэкранные устройства | Документы Майкрософт"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Майкрософт"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция CSS media screen-spanning для обнаружения двухэкранного | Документы Майкрософт"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments для двухэкранных устройств | Документы Майкрософт"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих | Документы Майкрософт"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Папка | Сума"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
