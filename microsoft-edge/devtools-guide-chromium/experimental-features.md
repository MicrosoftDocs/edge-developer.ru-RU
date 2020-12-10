---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эксперименты
ms.openlocfilehash: b2b2e591834f1c75d51ec98523e2752d67a2d354
ms.sourcegitcommit: 6571bcc0b7f1c4c9d6ead65081374bab87cd4469
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203901"
---
# <span data-ttu-id="819f0-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="819f0-104">Experimental features</span></span>  

<span data-ttu-id="819f0-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые все еще находятся на стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="819f0-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="819f0-106">Вы можете протестировать и [оставить отзыв](#providing-feedback-on-experimental-features) , прежде чем каждый компонент будет выпущен.</span><span class="sxs-lookup"><span data-stu-id="819f0-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="819f0-107">Хотя экспериментальные функции доступны во всех каналах Microsoft EDGE, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Канарские Channel.</span><span class="sxs-lookup"><span data-stu-id="819f0-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="819f0-108">Включение экспериментальных функций</span><span class="sxs-lookup"><span data-stu-id="819f0-108">Turn on experimental features</span></span>  

<span data-ttu-id="819f0-109">Чтобы включить экспериментальные функции в Microsoft EDGE, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-110">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="819f0-110">[Open DevTools][DevtoolsOpen].</span></span>  
    *   <span data-ttu-id="819f0-111">Выберите `Control` + `Shift` + `I` \ (Windows, Linux \) или `Command` + `Option` + `I` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="819f0-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="819f0-112">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="819f0-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="819f0-113">Открытие области [параметров][DevToolsCustomizeSettings] .</span><span class="sxs-lookup"><span data-stu-id="819f0-113">Open the [Settings][DevToolsCustomizeSettings] pane.</span></span>  
    *   <span data-ttu-id="819f0-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="819f0-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="819f0-115">Дополнительные сведения можно найти в разделе [сочетания клавиш Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="819f0-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="819f0-116">В левой части области **параметров** выберите раздел **эксперименты** .</span><span class="sxs-lookup"><span data-stu-id="819f0-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Список экспериментов в параметрах DevTools" lightbox="./media/experiments-devtools.msft.png":::
       <span data-ttu-id="819f0-118">Список экспериментов в **параметрах** DevTools</span><span class="sxs-lookup"><span data-stu-id="819f0-118">List of experiments in DevTools **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="819f0-119">На странице " **эксперименты** " прокрутите список всех доступных экспериментальных функций и установите флажок рядом с каждым компонентом, который нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="819f0-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="819f0-120">Закройте и снова откройте Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="819f0-121">Экспериментальные функции постоянно обновляются и могут привести к проблемам с производительностью.</span><span class="sxs-lookup"><span data-stu-id="819f0-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="819f0-122">Чтобы отключить экспериментальную функцию, откройте страницу **эксперименты** и снимите флажок экспериментальной функции, которую вы хотите отключить.</span><span class="sxs-lookup"><span data-stu-id="819f0-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="819f0-123">Выделены экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="819f0-123">Highlighted experimental features</span></span>  

<span data-ttu-id="819f0-124">В следующих разделах описаны новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="819f0-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="819f0-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="819f0-125">Experimental feature</span></span> | <span data-ttu-id="819f0-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="819f0-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="819f0-127">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="819f0-127">Emulation: Support dual screen mode</span></span>](#emulation-support-dual-screen-mode) | <span data-ttu-id="819f0-128">84 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-128">84 or later</span></span> |  
| [<span data-ttu-id="819f0-129">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="819f0-129">Enable new CSS grid debugging features</span></span>](#enable-new-css-grid-debugging-features) | <span data-ttu-id="819f0-130">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-130">85 or later</span></span> |  
| [<span data-ttu-id="819f0-131">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="819f0-131">Enable support to move tabs between panels</span></span>](#enable-support-to-move-tabs-between-panels) | <span data-ttu-id="819f0-132">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-132">85 or later</span></span> |  
| [<span data-ttu-id="819f0-133">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="819f0-133">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="819f0-134">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-134">85 or later</span></span> |  
| [<span data-ttu-id="819f0-135">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="819f0-135">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="819f0-136">85 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-136">85 or later</span></span> |  
| [<span data-ttu-id="819f0-137">Средство просмотра исходного порядка</span><span class="sxs-lookup"><span data-stu-id="819f0-137">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="819f0-138">86 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-138">86 or later</span></span> |  
| [<span data-ttu-id="819f0-139">Включение редактора сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="819f0-139">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="819f0-140">87 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-140">87 or later</span></span> |  
| [<span data-ttu-id="819f0-141">Включение составных слоев в трехмерном представлении</span><span class="sxs-lookup"><span data-stu-id="819f0-141">Turn on Composited Layers in 3D View</span></span>](#turn-on-composited-layers-in-3d-view) | <span data-ttu-id="819f0-142">87 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819f0-142">87 or later</span></span> |  

### <span data-ttu-id="819f0-143">Эмуляция: поддержка двух режимов экрана</span><span class="sxs-lookup"><span data-stu-id="819f0-143">Emulation: Support dual screen mode</span></span>  

<span data-ttu-id="819f0-144">Предоставляет дополнительные функции для эмуляции двух новых двух экранов и устройств складная в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="819f0-144">Provides additional features for emulating two new dual-screen and foldable devices in Microsoft Edge.</span></span>  

*   [<span data-ttu-id="819f0-145">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="819f0-145">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="819f0-146">Samsung Galaxy сгиб</span><span class="sxs-lookup"><span data-stu-id="819f0-146">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="819f0-147">Эмулирует устройства и переключаться между следующими элементами.</span><span class="sxs-lookup"><span data-stu-id="819f0-147">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="819f0-148">режим с одним экраном или сложением</span><span class="sxs-lookup"><span data-stu-id="819f0-148">single-screen or folded posture</span></span>  
*   <span data-ttu-id="819f0-149">возможность установки на два экрана или несложенный</span><span class="sxs-lookup"><span data-stu-id="819f0-149">dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="819f0-150">[Включите экспериментальные API веб-платформ](#enable-experimental-apis) и используйте [функцию многоэкранной][DualScreenDocsCssMedia] группировки с экрана CSS и [API JavaScript getWindowSegments][DualScreenDocsJSAPI] для расширения вашего веб-сайта (или приложения) на двойном экране и на складная устройствах.</span><span class="sxs-lookup"><span data-stu-id="819f0-150">[Enable experimental Web Platform APIs](#enable-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Эмуляция Surface Duo в Microsoft Edge" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="819f0-152">Эмуляция Surface Duo в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="819f0-152">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

#### <span data-ttu-id="819f0-153">Включение экспериментальных API</span><span class="sxs-lookup"><span data-stu-id="819f0-153">Enable experimental APIs</span></span>  

<span data-ttu-id="819f0-154">Чтобы использовать [функцию многоэкранной области экрана CSS][DualScreenDocsCssMedia] и [API JavaScript getWindowSegments][DualScreenDocsJSAPI], включите `Experimental Web Platform features` флажок в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="819f0-154">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="819f0-155">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-155">Complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-156">Перейдите к `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="819f0-156">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="819f0-157">В текстовом поле **Флаги поиска** введите `Experimental Web Platform features` , выберите " **экспериментальные компоненты веб-платформы** ", а затем **Enabled**— " **Отключить** ".</span><span class="sxs-lookup"><span data-stu-id="819f0-157">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="819f0-158">Перезапустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="819f0-158">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Флажок включения функций экспериментальной веб-платформы" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="819f0-160">Флажок включения функций экспериментальной веб-платформы</span><span class="sxs-lookup"><span data-stu-id="819f0-160">Enable the Experimental Web Platform features flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="819f0-161">Если вы используете запросы на поиск [мультимедиа в каскадных таблицах][DualScreenDocsCssMedia] или [API-интерфейс перечисления сегмента Windows (JavaScript][DualScreenDocsJSAPI] ) для повышения качества сайта или приложения для служб [Surface Duo][SurfaceDevicesDuo], необходимо также включить флажок **экспериментальные возможности веб-платформы** в [приложении Android Microsoft Edge][GooglePlayMicrosoftEdge] на устройстве [Surface Duo][SurfaceDevicesDuo] .</span><span class="sxs-lookup"><span data-stu-id="819f0-161">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also enable the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="819f0-162">Если флажок **"экспериментальные веб-платформа** " включен [в классическом приложении Microsoft][MicrosoftEdge] EDGE и отключен для [приложения Android (Microsoft Edge][GooglePlayMicrosoftEdge]), поведение вашего веб-сайта или приложения в эмуляторе Duo Surface в классическом приложении Microsoft EDGE не совпадает с [приложением Android Microsoft][GooglePlayMicrosoftEdge] EDGE на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="819f0-162">If the **Experimental Web Platform features** flag is enabled in [desktop Microsoft Edge][MicrosoftEdge] and disabled in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="819f0-163">Убедитесь в том, что для устройств Android и Desktop Microsoft Edge успешно используются Эмуляторы Surface Duo в классической платформе [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="819f0-163">Ensure that the flags are matching across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

#### <span data-ttu-id="819f0-164">Тестирование на устройствах складная и на двух экранах</span><span class="sxs-lookup"><span data-stu-id="819f0-164">Testing on foldable and dual-screen devices</span></span>  

<span data-ttu-id="819f0-165">При эмуляции [Duo Surface][SurfaceDevicesDuo] в Microsoft Edge с двумя экранами на экране добавляется стык \ (расстояние между двумя экранами), нарисованный на веб-сайте или в приложении.</span><span class="sxs-lookup"><span data-stu-id="819f0-165">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="819f0-166">Эмулятор дисплея соответствует способу обработки веб-сайта \ (или приложения \) в [приложении Microsoft Edge Android][GooglePlayMicrosoftEdge] , работающем на [Surface Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="819f0-166">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="819f0-167">Возможно, вам потребуется обновить ваш веб-сайт \ (или приложение \), чтобы он лучше отображался на стыке.</span><span class="sxs-lookup"><span data-stu-id="819f0-167">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="819f0-168">Чтобы получить дополнительные сведения о адаптации вашего веб-сайта к стыку (или его приложению), перейдите к разделу [Работа с стыком][DualScreenIntroductionHowWorkSeam].</span><span class="sxs-lookup"><span data-stu-id="819f0-168">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="819f0-169">На [панели инструментов устройства][DevtoolsDeviceModeIndexSimulateMobileViewport] есть дополнительные функции, с помощью которых можно протестировать веб-сайт или приложение в нескольких элементах управления и ориентации.</span><span class="sxs-lookup"><span data-stu-id="819f0-169">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="819f0-170">**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите поворот на (повернуть).</span><span class="sxs-lookup"><span data-stu-id="819f0-170">Choose **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="819f0-171">Объедините функцию с **диапазоном** \ ( ![ Span ][ImageSpanIcon] \), чтобы переключаться между одним экраном или сложением, а также с двойным экраном или без сгиба.</span><span class="sxs-lookup"><span data-stu-id="819f0-171">Combine the feature with **Span** \(![Span][ImageSpanIcon]\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="819f0-172">Вместе функции позволяют тестировать ваш веб-сайт или приложение во всех четырех возможностях и ориентациях.</span><span class="sxs-lookup"><span data-stu-id="819f0-172">Together, the features enable testing your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Матрица геоуровней и ориентации для двухпроцессорных и складная устройств" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="819f0-174">Матрица геоуровней и ориентации для двухпроцессорных и складная устройств</span><span class="sxs-lookup"><span data-stu-id="819f0-174">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="819f0-175">Значок " **экспериментальные веб-платформы** " \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) отображает состояние флага " **экспериментальные веб-платформы** ".</span><span class="sxs-lookup"><span data-stu-id="819f0-175">The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="819f0-176">Если пометка включена, значок выделена.</span><span class="sxs-lookup"><span data-stu-id="819f0-176">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="819f0-177">Если флажок выключен, значок не выделяется.</span><span class="sxs-lookup"><span data-stu-id="819f0-177">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="819f0-178">Чтобы включить параметр \ (или выключить), найдите `edge://flags` и переключите флажок.</span><span class="sxs-lookup"><span data-stu-id="819f0-178">To turn on \(or off\) the flag, navigate to `edge://flags` and toggle the flag.</span></span>  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

<span data-ttu-id="819f0-179">Ниже приведены дополнительные ресурсы, которые помогут вам улучшить работу вашего веб-сайта (или приложения) на устройствах с двумя экранами.</span><span class="sxs-lookup"><span data-stu-id="819f0-179">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="819f0-180">Дополнительные сведения о веб-разработке на устройствах с двумя экранами можно найти на [веб-сайте с двумя экранами][DualScreenWebIndex].</span><span class="sxs-lookup"><span data-stu-id="819f0-180">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="819f0-181">Установите [эмулятор Surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="819f0-181">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="819f0-182">Он отличается от эмулятора в Microsoft EDGE, эмулирует центр Surface Duo с Android и интегрируется с [Android][AndroidDeveloperStudio].</span><span class="sxs-lookup"><span data-stu-id="819f0-182">It is different from the emulator in Microsoft Edge, emulates the Surface Duo running Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="819f0-183">Дополнительные сведения можно найти в [пакете SDK Surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="819f0-183">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="819f0-184">Ниже приведен список текущих известных проблем.</span><span class="sxs-lookup"><span data-stu-id="819f0-184">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="819f0-185">При использовании [клиента удаленного рабочего стола Microsoft][RemoteDesktopClientDocs] для подключения к удаленному компьютеру и эмуляции [Galaxyого сгиба][SamsungMobileGalaxyFold] [Surface Duo][SurfaceDevicesDuo] или Samsung, указатель может стабилизации видеоизображения или перебоям.</span><span class="sxs-lookup"><span data-stu-id="819f0-185">When using a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="819f0-186">Если вы столкнулись с проблемой, [отправьте отзыв](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="819f0-186">If you run into the issue, [send feedback](#providing-feedback-on-experimental-features).</span></span>  

### <span data-ttu-id="819f0-187">Включение новых функций отладки CSS Grid</span><span class="sxs-lookup"><span data-stu-id="819f0-187">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="819f0-188">Эта экспериментальная функция предоставляет ряд новых визуализаций, которые помогут вам в отладке макетов сетки CSS.</span><span class="sxs-lookup"><span data-stu-id="819f0-188">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="819f0-189">Чтобы просмотреть последние экспериментальные функции, [Включите этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-189">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="819f0-190">Этот эксперимент включен по умолчанию в Microsoft Edge версии 87 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="819f0-190">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="819f0-191">Просмотр наложенных указателей сетки с помощью средства проверки</span><span class="sxs-lookup"><span data-stu-id="819f0-191">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="819f0-192">С помощью средства **проверки** можно быстро определить и визуализировать макеты сетки CSS на веб-сайте, наведя на них указатель мыши.</span><span class="sxs-lookup"><span data-stu-id="819f0-192">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="819f0-193">Щелкните значок **проверить** \ ( ![ проверить ](./media/inspect-icon.msft.png) \) в левом верхнем углу DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-193">Choose the **Inspect** \(![Inspect](./media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="819f0-194">Затем наведите указатель мыши на элемент Grid на веб-сайте, который вы отлаживается.</span><span class="sxs-lookup"><span data-stu-id="819f0-194">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="819f0-195">Контуры отображаются вокруг сетки, а Заливка обозначает расположение зазоров сетки, если они есть.</span><span class="sxs-lookup"><span data-stu-id="819f0-195">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Просмотр сеток с помощью средства "Проверка"" lightbox="./media/grid-inspect.msft.png":::
   <span data-ttu-id="819f0-197">Просмотр сеток с помощью средства "Проверка"</span><span class="sxs-lookup"><span data-stu-id="819f0-197">Viewing grids with the Inspect tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="819f0-198">Просмотр наложенных закрытий сетки</span><span class="sxs-lookup"><span data-stu-id="819f0-198">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="819f0-199">В Microsoft Edge версии 86 или более поздней функция для экспериментальной сетки каскадных стилей также включает возможность включения постоянных наложений.</span><span class="sxs-lookup"><span data-stu-id="819f0-199">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="819f0-200">Сохраняемые перекрытия предоставляют несколько преимуществ.</span><span class="sxs-lookup"><span data-stu-id="819f0-200">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="819f0-201">После прокрутки на странице сохраняются сохраняемые наложения, перемещайте мышь и используйте другие функции DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-201">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="819f0-202">Одновременно может быть включена несколько постоянных наложений, что позволяет просматривать несколько макетов сетки за один раз.</span><span class="sxs-lookup"><span data-stu-id="819f0-202">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="819f0-203">Постоянные наложения предлагают множество параметров настройки, например скрытие и отображение имен в области сетки, зазоров сетки, размеров для отслеживания и т. д.</span><span class="sxs-lookup"><span data-stu-id="819f0-203">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="819f0-204">Два способа включения режима постоянной перекрытия сетки.</span><span class="sxs-lookup"><span data-stu-id="819f0-204">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="819f0-205">Щелкните значок овала **сетки** рядом с элементом Grid, отображаемым в дереве DOM инструмента **элементы** .</span><span class="sxs-lookup"><span data-stu-id="819f0-205">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Значок "овальный Grid" в инструменте "элементы"" lightbox="./media/grid-adorner.msft.png":::
       <span data-ttu-id="819f0-207">Значок "овальный Grid" в инструменте " **элементы** "</span><span class="sxs-lookup"><span data-stu-id="819f0-207">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="819f0-208">Откройте новую панель **макета** , расположенную в инструменте элементы, и установите флажок рядом с каждым элементом Grid, который вы хотите подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="819f0-208">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Панель макета в DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="819f0-210">Панель **макета** в DevTools</span><span class="sxs-lookup"><span data-stu-id="819f0-210">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="819f0-211">Настройка постоянных наложений</span><span class="sxs-lookup"><span data-stu-id="819f0-211">Configuring persistent overlays</span></span>  

<span data-ttu-id="819f0-212">В Microsoft Edge версии 86 или более поздней Новая панель **макета** находится в инструменте **элементы** рядом с вкладками **стили** и **вычисляемые** вкладки.</span><span class="sxs-lookup"><span data-stu-id="819f0-212">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="819f0-213">На панели **макета** выделяются параметры конфигурации для постоянных наложений.</span><span class="sxs-lookup"><span data-stu-id="819f0-213">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Функция отладки сетки каскадных стилей" lightbox="./media/experiments-grid.msft.png":::
   <span data-ttu-id="819f0-215">Функция отладки сетки каскадных стилей</span><span class="sxs-lookup"><span data-stu-id="819f0-215">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="819f0-216">Включение поддержки перемещения вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="819f0-216">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="819f0-217">Обычно такие инструменты, как **элементы** и **сеть** , могут открываться только в главной панели, расположенной в верхней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-217">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="819f0-218">Такие инструменты, как **трехмерные представления** и **проблемы** , которые обычно закрываются на панели **ящика** , которая находится в нижней части DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-218">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="819f0-219">После выбора эксперимента вы можете перемещать инструменты между верхней и нижней панелями.</span><span class="sxs-lookup"><span data-stu-id="819f0-219">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="819f0-220">Чтобы переместить инструмент, наведите на него указатель мыши, откройте контекстное меню, а затем выберите команду **переместить в начало** или **Переместить вниз**.</span><span class="sxs-lookup"><span data-stu-id="819f0-220">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="819f0-221">Этот эксперимент позволяет настроить макет DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-221">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="819f0-222">Чтобы показать или скрыть панель **ящика** , нажмите кнопку `Escape` .</span><span class="sxs-lookup"><span data-stu-id="819f0-222">To show or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Перемещение вкладок между панелями" lightbox="./media/experiments-move-panels.msft.png":::
   <span data-ttu-id="819f0-224">Перемещение вкладок между панелями</span><span class="sxs-lookup"><span data-stu-id="819f0-224">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="819f0-225">Включить подсказку</span><span class="sxs-lookup"><span data-stu-id="819f0-225">Enable webhint</span></span>  

<span data-ttu-id="819f0-226">веб- [Подсказка][WebhintMain] — это средство с открытым исходным кодом, которое предоставляет отзыв в реальном времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="819f0-226">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local web pages.</span></span>  <span data-ttu-id="819f0-227">Тип обратной связи, предоставляемой функцией " [Подсказка][WebhintMain]".</span><span class="sxs-lookup"><span data-stu-id="819f0-227">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="819f0-228">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="819f0-228">accessibility</span></span>  
*   <span data-ttu-id="819f0-229">совместимость с различными браузерами</span><span class="sxs-lookup"><span data-stu-id="819f0-229">cross-browser compatibility</span></span>  
*   <span data-ttu-id="819f0-230">безопасность"</span><span class="sxs-lookup"><span data-stu-id="819f0-230">security</span></span>  
*   <span data-ttu-id="819f0-231">эффективности</span><span class="sxs-lookup"><span data-stu-id="819f0-231">performance</span></span>  
*   <span data-ttu-id="819f0-232">Прогрессивные веб-приложения (PWAs)</span><span class="sxs-lookup"><span data-stu-id="819f0-232">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="819f0-233">другие распространенные проблемы с веб-разработками</span><span class="sxs-lookup"><span data-stu-id="819f0-233">other common web development issues</span></span>  
    
<span data-ttu-id="819f0-234">Эксперименты с этой [подсказкой][WebhintMain] отображаются на панели " [вопросы][DevtoolsIssues] " в виде обратной связи.</span><span class="sxs-lookup"><span data-stu-id="819f0-234">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="819f0-235">Выберите вопрос для отображения документации решения и списка уязвимых ресурсов на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="819f0-235">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="819f0-236">Выберите ссылку на ресурс, чтобы открыть область " **сеть**, **источники**или **элементы** " в DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-236">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Обратная связь по этой подсказке на панели "вопросы"" lightbox="./media/experiments-webhint.msft.png":::
   <span data-ttu-id="819f0-238">Обратная связь по этой подсказке на панели " **вопросы** "</span><span class="sxs-lookup"><span data-stu-id="819f0-238">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="819f0-239">Включение сетевой консоли</span><span class="sxs-lookup"><span data-stu-id="819f0-239">Enable Network Console</span></span>  

<span data-ttu-id="819f0-240">**Сетевая консоль** — это рабочее название эксперимента для создания искусственных сетевых запросов по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="819f0-240">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="819f0-241">Вы можете использовать эксперименты с **сетевой консолью** для отправки запросов на веб-API.</span><span class="sxs-lookup"><span data-stu-id="819f0-241">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="819f0-242">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-242">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="819f0-243">Чтобы использовать **консоль "сеть**", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-243">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-244">Открытие области " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="819f0-244">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="819f0-245">Найдите сетевой запрос, который вы хотите изменить и отправить повторно.</span><span class="sxs-lookup"><span data-stu-id="819f0-245">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="819f0-246">Откройте контекстное меню \ (щелкните правой кнопкой мыши и выберите команду **изменить и воспроизвести**).</span><span class="sxs-lookup"><span data-stu-id="819f0-246">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="819f0-247">Когда откроется **Сетевая консоль** , измените сведения о сетевом запросе.</span><span class="sxs-lookup"><span data-stu-id="819f0-247">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="819f0-248">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="819f0-248">Choose **Send**.</span></span>  
    
:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Сетевая консоль в консольном ящике" lightbox="./media/network-network-console.msft.png":::
   <span data-ttu-id="819f0-250">**Сетевая консоль** в **консольном** ящике</span><span class="sxs-lookup"><span data-stu-id="819f0-250">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="819f0-251">Средство просмотра исходного порядка</span><span class="sxs-lookup"><span data-stu-id="819f0-251">Source Order Viewer</span></span>  

<span data-ttu-id="819f0-252">**Средство просмотра исходного порядка** — это эксперимент, в котором отображается порядок элементов в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="819f0-252">**Source Order Viewer** is an experiment that displays the order of elements in the page source.</span></span>  <span data-ttu-id="819f0-253">Порядок отображения на экране может отличаться от порядка источников, который в своюмся случае будет использовать средство чтения с экрана и пользователи клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="819f0-253">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="819f0-254">Для поиска различий между порядком отображения на экране и порядком расположения источника используйте эксперимент в **средстве просмотра исходного порядка** .</span><span class="sxs-lookup"><span data-stu-id="819f0-254">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="819f0-255">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-255">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="819f0-256">Чтобы использовать **средство просмотра заказов исходного кода**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-256">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-257">Откройте область **элементы** .</span><span class="sxs-lookup"><span data-stu-id="819f0-257">Open the **Elements** pane.</span></span>  
1.  <span data-ttu-id="819f0-258">Откройте область **Специальные возможности** на панели ящик \ (Нижняя \).</span><span class="sxs-lookup"><span data-stu-id="819f0-258">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="819f0-259">В разделе **средство просмотра исходного заказа** установите флажок **Показать порядок источников** .</span><span class="sxs-lookup"><span data-stu-id="819f0-259">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="819f0-260">Выделит любой HTML-элемент, чтобы отобразить наложение, порядок расположения которых указан в источнике страницы.</span><span class="sxs-lookup"><span data-stu-id="819f0-260">Highlight any HTML element to display an overlay that the order in the page source.</span></span>  
    
:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Средство просмотра исходного порядка на панели "Специальные возможности"" lightbox="./media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="819f0-262">**Средство просмотра исходного порядка** на панели " **Специальные возможности** "</span><span class="sxs-lookup"><span data-stu-id="819f0-262">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="819f0-263">Включение редактора сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="819f0-263">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="819f0-264">После включения эксперимента с **редактором сочетаний клавиш** включена возможность настройки сочетаний клавиш для любых действий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-264">With the **Enable keyboard shortcut editor** experiment turned on, you are now able to customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="819f0-265">Чтобы настроить сочетание клавиш для определенного действия, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-265">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-266">[Откройте DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="819f0-266">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="819f0-267">Откройте [Параметры][DevToolsCustomizeSettings].</span><span class="sxs-lookup"><span data-stu-id="819f0-267">Open [Settings][DevToolsCustomizeSettings].</span></span>
    *   <span data-ttu-id="819f0-268">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="819f0-268">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="819f0-269">Перейдите на страницу " **сочетания клавиш** ".</span><span class="sxs-lookup"><span data-stu-id="819f0-269">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="819f0-270">Выберите действие, которое вы хотите настроить.</span><span class="sxs-lookup"><span data-stu-id="819f0-270">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="819f0-271">Щелкните значок **изменить** \ ( ![ EditKeyboardShortcut ][ImageEditKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="819f0-271">Choose the **Edit** \(![EditKeyboardShortcut][ImageEditKeyboardShortcutIcon]\) icon.</span></span>  
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Выберите действие, которое нужно настроить, на странице "ярлыки" в разделе "Параметры"" lightbox="./media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="819f0-273">Выберите действие, которое нужно настроить, на странице " **ярлыки** " в разделе " [Параметры][DevToolsCustomizeSettings] "</span><span class="sxs-lookup"><span data-stu-id="819f0-273">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeSettings]</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="819f0-274">На клавиатуре выберите клавиши, которые вы хотите привязать к действию.</span><span class="sxs-lookup"><span data-stu-id="819f0-274">On the keyboard, select the keys you want to bind to the action.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Выберите клавиши, которые вы хотите назначить действию." lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="819f0-276">Выберите клавиши, которые вы хотите назначить действию.</span><span class="sxs-lookup"><span data-stu-id="819f0-276">Select the keys you want to assign to the action</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="819f0-277">Чтобы сохранить новое сочетание клавиш, выберите флажок \ (</span><span class="sxs-lookup"><span data-stu-id="819f0-277">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut][ImageCheckmarkKeyboardShortcutIcon]<span data-ttu-id="819f0-279">\).</span><span class="sxs-lookup"><span data-stu-id="819f0-279">\) icon.</span></span>
    
    :::image type="complex" source="./media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Щелкните значок метки, чтобы сохранить новое сочетание клавиш" lightbox="./media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="819f0-281">Щелкните значок метки, чтобы сохранить новое сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="819f0-281">Choose the checkmark icon to save your new keyboard shortcut</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="819f0-282">Выберите новое сочетание клавиш, чтобы запустить действие в DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-282">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="819f0-283">На странице " **сочетания** клавиш" **Настраиваемый** значок сочетания клавиш ( ![ CustomKeyboardShortcut ][ImageCustomKeyboardShortcutIcon] \) отображает сочетания клавиш, которые вы настроили.</span><span class="sxs-lookup"><span data-stu-id="819f0-283">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut][ImageCustomKeyboardShortcutIcon]\) icon displays keyboard shortcuts that you have customized.</span></span>  <span data-ttu-id="819f0-284">Чтобы сбросить все сочетания клавиш, нажмите кнопку **восстановить сочетания клавиш по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="819f0-284">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="819f0-285">При редактировании сочетаний клавиш для действия, чтобы отменить изменения, щелкните значок X \ ( ![ XKeyboardShortcut ][ImageXKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="819f0-285">When you are editing the keyboard shortcuts for an action, to discard your changes, choose the X \(![XKeyboardShortcut][ImageXKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="819f0-286">Чтобы удалить сочетания клавиш для определенного действия, щелкните значок **удалить ярлык** \ ( ![ DeleteKeyboardShortcut ][ImageDeleteKeyboardShortcutIcon] \).</span><span class="sxs-lookup"><span data-stu-id="819f0-286">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut][ImageDeleteKeyboardShortcutIcon]\) icon.</span></span>  <span data-ttu-id="819f0-287">Чтобы добавить несколько сочетаний клавиш для действия, выберите команду **Добавить ярлык**.</span><span class="sxs-lookup"><span data-stu-id="819f0-287">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>

> [!NOTE]
> <span data-ttu-id="819f0-288">Если сочетание клавиш в настоящее время назначено другому действию, вы не сможете сохранить его для нового действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-288">If a keyboard shortcut is currently assigned to another action, you are not able to save it for a new action.</span></span>  <span data-ttu-id="819f0-289">Сначала нужно удалить сочетание клавиш для предыдущего действия, а затем добавить его в новое действие.</span><span class="sxs-lookup"><span data-stu-id="819f0-289">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->

### <span data-ttu-id="819f0-290">Включение составных слоев в трехмерном представлении</span><span class="sxs-lookup"><span data-stu-id="819f0-290">Turn on Composited Layers in 3D View</span></span>

<span data-ttu-id="819f0-291">Теперь вы можете визуализировать слои вместе с z-индексами и объектной моделью документов \ (DOM \).</span><span class="sxs-lookup"><span data-stu-id="819f0-291">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="819f0-292">Эта функция позволяет выполнять отладку без переключения контекстов в обычном режим.</span><span class="sxs-lookup"><span data-stu-id="819f0-292">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="819f0-293">Вы определили, что сокращенное переключение контекста было основным моментом.</span><span class="sxs-lookup"><span data-stu-id="819f0-293">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="819f0-294">Не всегда ясно, как написанный вами код влияет на веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="819f0-294">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="819f0-295">Для всесторонней визуальной отладки теперь можно объединять трехмерное представление и составные слои.</span><span class="sxs-lookup"><span data-stu-id="819f0-295">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  <span data-ttu-id="819f0-296">После включения эксперимента убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-296">After enabling the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="819f0-297">Чтобы использовать **Составные слои**, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="819f0-297">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="819f0-298">На ящике выберите инструмент **3D-представление** .</span><span class="sxs-lookup"><span data-stu-id="819f0-298">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="819f0-299">Открытие области " **Составные слои** ".</span><span class="sxs-lookup"><span data-stu-id="819f0-299">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="819f0-300">На экране появятся все окрашенные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="819f0-300">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="819f0-301">Попробуйте выполнить эту функцию с помощью собственных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="819f0-301">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="./media/experiments-layers.msft.png" alt-text="Область «составные слои»" lightbox="./media/experiments-layers.msft.png":::
   <span data-ttu-id="819f0-303">Область « **Составные слои** »</span><span class="sxs-lookup"><span data-stu-id="819f0-303">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

## <span data-ttu-id="819f0-304">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="819f0-304">Previous experimental features</span></span>  

*   <span data-ttu-id="819f0-305">Теперь [трехмерный вид][Devtools3dViewIndex] доступен и включен по умолчанию в Microsoft Edge версии 83 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="819f0-305">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="819f0-306">[Настройка сочетаний клавиш][DevtoolsCustomKeyboardShortcuts] теперь доступна и включена по умолчанию в Microsoft Edge версии 86 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="819f0-306">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  

## <span data-ttu-id="819f0-307">Отзывы о экспериментальных функциях</span><span class="sxs-lookup"><span data-stu-id="819f0-307">Providing feedback on experimental features</span></span>  

<span data-ttu-id="819f0-308">Чтобы оставить отзыв о экспериментах Microsoft Edge DevTools или каких-либо других связанных с DevTools.</span><span class="sxs-lookup"><span data-stu-id="819f0-308">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="819f0-309">Отправка отзыва с помощью значка " **Отправить отзыв** " в DevTools</span><span class="sxs-lookup"><span data-stu-id="819f0-309">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="819f0-310">Твит на [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="819f0-310">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="819f0-312">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="819f0-312">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  
[ImageEditKeyboardShortcutIcon]: ./media/edit-keyboard-shortcut-icon.msft.png  
[ImageCheckmarkKeyboardShortcutIcon]: ./media/checkmark-keyboard-shortcut-icon.msft.png  
[ImageCustomKeyboardShortcutIcon]: ./media/custom-keyboard-shortcut-icon.msft.png  
[ImageDeleteKeyboardShortcutIcon]: ./media/delete-keyboard-shortcut-icon.msft.png  
[ImageXKeyboardShortcutIcon]: ./media/discard-changes-keyboard-shortcut-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Трехмерный вид | Документы Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Сочетания клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpen]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Настройка сочетаний клавиш в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsOpenMain]: ./open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Веб-интерфейс на базе двух экранов | Документы Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Получение эмулятора Surface Duo | Документы Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Работа с стыками — введение в работу с устройствами с двумя экранами | Документы Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Использование эмулятора Surface Duo | Документы Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Функция многоэкранной группировки с экрана в каскадных таблицах CSS | Документы Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API getWindowSegments JavaScript для устройств с двумя экранами | Документы Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Клиенты удаленных рабочих столов | Документы Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy, сгиб | Samsung"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Контента"  

[WebhintMain]: https://webhint.io "Подсказка"  
