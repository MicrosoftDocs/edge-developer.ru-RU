---
description: Подражать недостаткам цветового зрения, док-станции налево в командном меню и другие.
title: Новые возможности в DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: f97155b12a679f630ce80c007e7f0ca693e19876
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408355"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a><span data-ttu-id="8ca95-104">Что нового в DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="8ca95-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="8ca95-105">В соответствии с обновленным расписанием хрома мы корректируем расписание предстоящих выпусков Microsoft Edge и отменяем выпуск Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="8ca95-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="8ca95-106">Дополнительные сведения можно [получить в][WindowsBlogStableRelease] нашем блоге.</span><span class="sxs-lookup"><span data-stu-id="8ca95-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="8ca95-107">Вот новые функции, доступные в DevTools в Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="8ca95-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8ca95-108">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8ca95-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="8ca95-109">В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="8ca95-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="8ca95-110">Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.</span><span class="sxs-lookup"><span data-stu-id="8ca95-110">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="8ca95-111">Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="8ca95-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a><span data-ttu-id="8ca95-112">Удаленное отлагивание Microsoft Edge на устройствах с Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ca95-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="8ca95-113">Приложение [Remote Tools для Microsoft Edge \(Beta\)][RemoteTools] теперь доступно в Microsoft [Store.][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="8ca95-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="8ca95-114">С помощью этого приложения, которое расширяет портал устройств [Windows,][WindowsUwpDebugTestPerfDevicePortal]вы можете подключиться от экземпляра Microsoft Edge, запущенного на компьютере разработки, к удаленному устройству Windows 10, отобразить список целей \(все вкладки в Microsoft Edge и [PWAs][ProgressiveWebAppsChromiumIndex] открыты на устройстве Windows 10\), а также использовать DevTools на машине разработки против целевой задачи, запущенной на удаленном устройстве Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8ca95-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, display a list of targets \(all tabs in Microsoft Edge and [PWAs][ProgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools for Microsoft Edge (Beta), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="8ca95-116">Приложение [Remote Tools for Microsoft Edge (Beta),][RemoteTools] доступное в Microsoft [Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="8ca95-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-117">[Ознакомьтесь с нашим руководством по настройке устройства Windows 10][DevtoolsRemoteDebuggingWindows]и компьютера разработки для удаленной отладки.</span><span class="sxs-lookup"><span data-stu-id="8ca95-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="8ca95-118">Дайте нам знать о вашем опыте удаленной отладки, отправив в [twitter][PostTweetEdgeDevTools] или отправив значок [обратной связи!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <a name="new-ways-to-access-settings"></a><span data-ttu-id="8ca95-119">Новые способы доступа к Настройкам</span><span class="sxs-lookup"><span data-stu-id="8ca95-119">New ways to access Settings</span></span>  

<span data-ttu-id="8ca95-120">Есть тонны параметров для DevTools, которые вы можете настроить, чтобы сделать DevTools выглядеть, чувствовать и работать так, как вам нужно.</span><span class="sxs-lookup"><span data-stu-id="8ca95-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="8ca95-121">В Microsoft Edge 83 доступ к [настройкам][DevtoolsCustomizeIndexSettings] в DevTools теперь намного проще.</span><span class="sxs-lookup"><span data-stu-id="8ca95-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span>  <span data-ttu-id="8ca95-122">Откройте параметры со значком передач рядом с оповещениями консоли и основным меню.</span><span class="sxs-lookup"><span data-stu-id="8ca95-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Значок передач открывает параметры в DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="8ca95-124">Значок передач открывает **параметры** в DevTools</span><span class="sxs-lookup"><span data-stu-id="8ca95-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-125">Вы также можете открыть [параметры][DevtoolsCustomizeIndexSettings] из **основного** меню в **дополнительных средствах.**</span><span class="sxs-lookup"><span data-stu-id="8ca95-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Главное меню > дополнительные средства > параметры" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="8ca95-127">**Главное меню**  >  **Дополнительные средства**  >  **Параметры**</span><span class="sxs-lookup"><span data-stu-id="8ca95-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-128">Проблема Chromium [#1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="8ca95-128">Chromium issue [#1050855][CR1050855]</span></span>

### <a name="new-and-improved-infobars"></a><span data-ttu-id="8ca95-129">Новые и улучшенные информационные панели</span><span class="sxs-lookup"><span data-stu-id="8ca95-129">New and improved infobars</span></span>

<span data-ttu-id="8ca95-130">Информационные панели уведомлений \(infobars\) в DevTools теперь имеют улучшенный внешний вид и более функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="8ca95-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="8ca95-131">В Microsoft Edge 83 информационные панели легче читать и предоставлять кнопки, чтобы можно было сразу принять соответствующие действия.</span><span class="sxs-lookup"><span data-stu-id="8ca95-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infobar для красивой печати добытого файла в Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="8ca95-133">Infobar для красивой печати добытого файла в Microsoft Edge Version 83</span><span class="sxs-lookup"><span data-stu-id="8ca95-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-134">Проблема Chromium [#1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="8ca95-134">Chromium issue [#1056348][CR1056348]</span></span>

### <a name="navigate-the-color-picker-with-your-keyboard"></a><span data-ttu-id="8ca95-135">Перейдите по выбору цвета с помощью клавиатуры</span><span class="sxs-lookup"><span data-stu-id="8ca95-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="8ca95-136">Выбор [цвета —][DevtoolsCssReferenceColorPicker] это GUI в панели [Elements][DevtoolsCssIndex] для изменений и `color` `background-color` объявлений.</span><span class="sxs-lookup"><span data-stu-id="8ca95-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="8ca95-137">В предыдущих версиях Microsoft Edge вы не могли перемещаться по разделу **Оттенки** выбора [цвета][DevtoolsCssReferenceColorPicker] с помощью клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="8ca95-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Теперь вы можете использовать клавиатуру для перемещения селектора в разделе Оттенки выбора цвета" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="8ca95-139">Теперь вы можете использовать клавиатуру для перемещения селектора в разделе **Оттенки** выбора [цвета][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="8ca95-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-140">В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **Оттенки** выбора цвета.</span><span class="sxs-lookup"><span data-stu-id="8ca95-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="8ca95-141">Проблема Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="8ca95-141">Chromium issue [#963183][CR963183]</span></span>  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a><span data-ttu-id="8ca95-142">Вкладка Свойства теперь заполняется после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="8ca95-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="8ca95-143">В Microsoft Edge 81 и ранее вкладка **Properties** в панели [Elements][DevtoolsCssIndex] была нарушена путем обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="8ca95-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="8ca95-144">При обновлении страницы вкладка **Properties** не заполняла свойства выбранного в настоящее время элемента.</span><span class="sxs-lookup"><span data-stu-id="8ca95-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="В Microsoft Edge 81 и ранее вкладка Properties была пустой после обновления страницы" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="8ca95-146">В Microsoft Edge 81 и ранее вкладка **Properties** была пустой после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="8ca95-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-147">В Microsoft Edge 83 теперь можно отобразить свойства выбранного в настоящее время элемента после обновления страницы на **вкладке Свойства.**</span><span class="sxs-lookup"><span data-stu-id="8ca95-147">In Microsoft Edge 83, you are now able to display the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="В Microsoft Edge 83 вкладка Properties отображает свойства выбранного в настоящее время элемента после обновления страницы" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="8ca95-149">В Microsoft Edge 83 вкладка **Properties** отображает свойства выбранного в настоящее время элемента после обновления страницы</span><span class="sxs-lookup"><span data-stu-id="8ca95-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-150">Проблема Chromium [#1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="8ca95-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a><span data-ttu-id="8ca95-151">Используйте клавиши стрелки для прокрутки в средстве Изменения</span><span class="sxs-lookup"><span data-stu-id="8ca95-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="8ca95-152">Средство **Изменения отслеживает** все изменения, внесенные в CSS или JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="8ca95-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="8ca95-153">Вы можете использовать средство **Изменения,** чтобы быстро отображать все изменения и возвращать их в редактор/IDE.</span><span class="sxs-lookup"><span data-stu-id="8ca95-153">You are able to use the **Changes tool** to quickly display all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="8ca95-154">Чтобы открыть средство **Изменения,** выберите `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [командное меню][DevToolsCommandMenuIndex] и введите `changes` .</span><span class="sxs-lookup"><span data-stu-id="8ca95-154">To open the **Changes tool**, select `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and type `changes`.</span></span>  <span data-ttu-id="8ca95-155">выберите и запустите команду **Show Changes,** чтобы открыть средство **Изменения** в ящике DevTools.</span><span class="sxs-lookup"><span data-stu-id="8ca95-155">choose and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="8ca95-156">При внесении изменения в минированную папку средство **Changes** позволяет прокручивать по горизонтали, чтобы отобразить весь заминированный код.</span><span class="sxs-lookup"><span data-stu-id="8ca95-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to display all of your minified code.</span></span>  <span data-ttu-id="8ca95-157">Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш стрелки на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="8ca95-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="В Microsoft Edge 83 можно прокручивать по горизонтали клавиши со стрелками, чтобы отобразить код в средстве Изменения" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="8ca95-159">В Microsoft Edge 83 можно прокручивать по горизонтали клавиши со стрелками, чтобы отобразить изменения, внесенные в ваш заминированный код в средстве **Изменения**</span><span class="sxs-lookup"><span data-stu-id="8ca95-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to display the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-160">Если вы используете считыватели экрана или клавиатуру для навигации по DevTools, отправьте нам свои отзывы, направив на нас твиты или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team) [][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="8ca95-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-161">Проблема Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="8ca95-161">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="8ca95-162">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="8ca95-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="8ca95-163">В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 83, которые были внесены в проект Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="8ca95-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <a name="emulate-vision-deficiencies"></a><span data-ttu-id="8ca95-164">Эмуляция дефектов зрения</span><span class="sxs-lookup"><span data-stu-id="8ca95-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="8ca95-165">Откройте [вкладку Rendering][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] и используйте новую функцию **эмулировать** недостатки зрения, чтобы получить представление о том, как люди с различными типами недостатков зрения испытывают на своем сайте.</span><span class="sxs-lookup"><span data-stu-id="8ca95-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Эмулирование размытого зрения" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="8ca95-167">Эмулирование размытого зрения</span><span class="sxs-lookup"><span data-stu-id="8ca95-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-168">DevTools может эмулировать размытое зрение и следующие типы [недостатков цветового зрения.][ColorBlindnessTypes]</span><span class="sxs-lookup"><span data-stu-id="8ca95-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="8ca95-169">Дефицит цветового зрения</span><span class="sxs-lookup"><span data-stu-id="8ca95-169">Color Vision Deficiency</span></span> | <span data-ttu-id="8ca95-170">Сведения</span><span class="sxs-lookup"><span data-stu-id="8ca95-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8ca95-171">Протанопия</span><span class="sxs-lookup"><span data-stu-id="8ca95-171">Protanopia</span></span> | <span data-ttu-id="8ca95-172">Невозможность воспринимать красный свет.</span><span class="sxs-lookup"><span data-stu-id="8ca95-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="8ca95-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="8ca95-173">Deuteranopia</span></span> | <span data-ttu-id="8ca95-174">Невозможность воспринимать зеленый свет.</span><span class="sxs-lookup"><span data-stu-id="8ca95-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="8ca95-175">Тританопия</span><span class="sxs-lookup"><span data-stu-id="8ca95-175">Tritanopia</span></span> | <span data-ttu-id="8ca95-176">Невозможность воспринимать синий свет.</span><span class="sxs-lookup"><span data-stu-id="8ca95-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="8ca95-177">Ахроматопсия</span><span class="sxs-lookup"><span data-stu-id="8ca95-177">Achromatopsia</span></span> | <span data-ttu-id="8ca95-178">Невозможность воспринимать любой цвет, за исключением оттенков серого \(крайне редко\).</span><span class="sxs-lookup"><span data-stu-id="8ca95-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="8ca95-179">Существуют менее экстремальные версии этих недостатков цветового зрения, и на самом деле они являются более распространенными.</span><span class="sxs-lookup"><span data-stu-id="8ca95-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="8ca95-180">Например, протаномали — это пониженная чувствительность к красному свету (в отличие от протанопии, которая является полной невозможностью воспринимать красный свет).</span><span class="sxs-lookup"><span data-stu-id="8ca95-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="8ca95-181">Тем не менее, эти недостатки зрения **omaly** не так четко определены: каждый человек с таким недостатком зрения отличается и может видеть вещи по-разному \(возможность воспринимать больше / меньше соответствующих цветов \).</span><span class="sxs-lookup"><span data-stu-id="8ca95-181">However, these **-omaly** vision deficiencies are not as clearly defined:  every person with such a vision deficiency is different and may see things differently \(being able to perceive more/less of the relevant colors\).</span></span>  

<span data-ttu-id="8ca95-182">При разработке более экстремальных моделей в DevTools ваши веб-приложения гарантированно будут доступны для людей с протаномалией, deuteranomaly, tritanomaly и achromatomaly.</span><span class="sxs-lookup"><span data-stu-id="8ca95-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="8ca95-183">Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-184">Проблема Chromium [#1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="8ca95-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <a name="emulate-locales"></a><span data-ttu-id="8ca95-185">Эмулировать локальные</span><span class="sxs-lookup"><span data-stu-id="8ca95-185">Emulate locales</span></span>  

<span data-ttu-id="8ca95-186">Эмулировать локальные параметры, задав расположение в **расположении**  >  **датчиков.**</span><span class="sxs-lookup"><span data-stu-id="8ca95-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="8ca95-187">[Откройте **командное меню и** ][DevToolsCommandMenuIndex] `Sensors` введите, чтобы получить доступ к **вкладке Датчики.**  После выполнения этих действий DevTools изменяет текущий локальный код по умолчанию, влияя на следующий код.</span><span class="sxs-lookup"><span data-stu-id="8ca95-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="8ca95-188">API, например:</span><span class="sxs-lookup"><span data-stu-id="8ca95-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="8ca95-189">Другие API JavaScript с локальными данными, например: `String.prototype.localeCompare` `*.prototype.toLocaleString`</span><span class="sxs-lookup"><span data-stu-id="8ca95-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="8ca95-190">API DOM, такие как `navigator.language` и</span><span class="sxs-lookup"><span data-stu-id="8ca95-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="8ca95-191">[Заглавная головка запроса http accept-Language][MDNAcceptLanguage] HTTP</span><span class="sxs-lookup"><span data-stu-id="8ca95-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="8ca95-192">Обновления и не видны сразу, но только после `navigator.language` `navigator.languages` следующей навигации или обновления страницы.</span><span class="sxs-lookup"><span data-stu-id="8ca95-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="8ca95-193">Изменения в `Accept-Language` загона HTTP отражаются только для последующих запросов.</span><span class="sxs-lookup"><span data-stu-id="8ca95-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Эмулирование локального" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="8ca95-195">Эмулирование локального</span><span class="sxs-lookup"><span data-stu-id="8ca95-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-196">Чтобы попробовать демонстрацию, перейдите к [примеру кода,][MathiasByensLocaleDemo]зависимого от locale.</span><span class="sxs-lookup"><span data-stu-id="8ca95-196">To try a demo, navigate to [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="8ca95-197">Проблема Chromium [#1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="8ca95-197">Chromium issue [#1051822][CR1051822]</span></span>

### <a name="cross-origin-embedder-policy-coep-debugging"></a><span data-ttu-id="8ca95-198">Отладка политики встраивляемого в поперечнике (COEP)</span><span class="sxs-lookup"><span data-stu-id="8ca95-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="8ca95-199">Панель Network теперь предоставляет сведения [о][COEP] отладки политики встраивляющихся между собой.</span><span class="sxs-lookup"><span data-stu-id="8ca95-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="8ca95-200">В **столбце Status** теперь приводится краткое объяснение, почему был заблокирован запрос, а также ссылка для просмотра заглавных окей этого запроса для дальнейшей отладки:</span><span class="sxs-lookup"><span data-stu-id="8ca95-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Заблокированные запросы в столбце **Status**" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="8ca95-202">Заблокированные запросы в **столбце Состояние**</span><span class="sxs-lookup"><span data-stu-id="8ca95-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-203">В **разделе Заглавные ответы** вкладки **"Заготки"** содержится дополнительные рекомендации по устранению проблем:</span><span class="sxs-lookup"><span data-stu-id="8ca95-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Дополнительные рекомендации в разделе Заглавные ответы" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="8ca95-205">Дополнительные рекомендации в **разделе Заглавные ответы**</span><span class="sxs-lookup"><span data-stu-id="8ca95-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-206">Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-207">Проблема Chromium [#1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="8ca95-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="8ca95-208">Новые значки для точек разрыва, условных точек и точек входа</span><span class="sxs-lookup"><span data-stu-id="8ca95-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="8ca95-209">Панель Источников имеет новые значки для точек разрыва, условных точек и точек входа:</span><span class="sxs-lookup"><span data-stu-id="8ca95-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="8ca95-210">Breakpoints \(</span><span class="sxs-lookup"><span data-stu-id="8ca95-210">Breakpoints \(</span></span>![Breakpoint](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="8ca95-212">\) представлены красными кругами.</span><span class="sxs-lookup"><span data-stu-id="8ca95-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="8ca95-213">Условные точки разрывов \.</span><span class="sxs-lookup"><span data-stu-id="8ca95-213">Conditional Breakpoints \(</span></span>![Условная точка разрыва](../../media/2020/03/conditional.msft.png)<span data-ttu-id="8ca95-215">\) представлены полу-красными полубелыми кругами.</span><span class="sxs-lookup"><span data-stu-id="8ca95-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="8ca95-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="8ca95-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="8ca95-218">\) представлены красными кругами с значками консоли.</span><span class="sxs-lookup"><span data-stu-id="8ca95-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="8ca95-219">Мотивация для новых значков была в том, чтобы сделать пользовательский интерфейс более совместимым с другими средствами отладки GUI \(которые обычно красные точки разлома цвета\) и упростить различие между 3 функциями с первого взгляда.</span><span class="sxs-lookup"><span data-stu-id="8ca95-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="8ca95-220">Проблема Chromium [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="8ca95-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a><span data-ttu-id="8ca95-221">Просмотр сетевых запросов, за набором определенного пути cookie</span><span class="sxs-lookup"><span data-stu-id="8ca95-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="8ca95-222">Используйте новое `cookie-path` ключевое слово фильтра в средстве **Network,** чтобы сосредоточиться на сетевых запросах, которые устанавливают определенный [путь cookie.][MDNCookiePath]</span><span class="sxs-lookup"><span data-stu-id="8ca95-222">Use the new `cookie-path` filter keyword in the **Network** tool to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="8ca95-223">Проверьте [запросы фильтра по свойствам,][DevtoolsNetworkReferenceFilterRequestsProperties] чтобы узнать больше ключевых слов, как `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="8ca95-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <a name="dock-to-left-from-the-command-menu"></a><span data-ttu-id="8ca95-224">Стыковка слева от меню команды</span><span class="sxs-lookup"><span data-stu-id="8ca95-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="8ca95-225">Откройте [командное меню][DevToolsCommandMenuIndex] и запустите команду для перемещения `Dock to left` DevTools слева от вашего представления.</span><span class="sxs-lookup"><span data-stu-id="8ca95-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools, пристыкованный слева от viewport" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="8ca95-227">DevTools, пристыкованный слева от viewport</span><span class="sxs-lookup"><span data-stu-id="8ca95-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8ca95-228">Функция **Dock слева** была доступна с Microsoft Edge 75, но ранее она была доступна только из [основного меню.][DevtoolsCustomizePlacementsChangeMainMenu]</span><span class="sxs-lookup"><span data-stu-id="8ca95-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="8ca95-229">Новая функция в Microsoft Edge 83 в том, что теперь вы можете получить доступ к этой функции из командного меню.</span><span class="sxs-lookup"><span data-stu-id="8ca95-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="8ca95-230">Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-231">Проблема Chromium [#1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="8ca95-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a><span data-ttu-id="8ca95-232">Панель аудитов теперь является панелью Маяк</span><span class="sxs-lookup"><span data-stu-id="8ca95-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="8ca95-233">Команда DevTools часто получает отзывы от веб-разработчиков о том, что хотя можно было запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они пытались его найти, они не могли найти панель "Маяк", поэтому панель **Аудиты** теперь панель **Маяк.**</span><span class="sxs-lookup"><span data-stu-id="8ca95-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Панель Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="8ca95-235">Панель Lighthouse</span><span class="sxs-lookup"><span data-stu-id="8ca95-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8ca95-236">Панель **Lighthouse** предоставляет ссылки на контент, который содержится на сторонних веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="8ca95-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="8ca95-237">Корпорация Майкрософт не несет ответственности и не контролирует содержимое этих сайтов и любые данные, которые они могут собирать.</span><span class="sxs-lookup"><span data-stu-id="8ca95-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <a name="delete-all-local-overrides-in-a-folder"></a><span data-ttu-id="8ca95-238">Удаление всех локальных переопределей в папке</span><span class="sxs-lookup"><span data-stu-id="8ca95-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="8ca95-239">После настройки \*\*\*\* локальных переопределей можно навести курсор на каталог, открыть контекстное меню \(правой кнопкой мыши\) и выбрать новый параметр **Удалить** все переопределения, чтобы удалить все локальные переопределения в этой папке.</span><span class="sxs-lookup"><span data-stu-id="8ca95-239">After setting up **Local Overrides** you may hover on a directory, open the contextual menu \(right-click\), and choose the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Удаление всех переопределе-" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="8ca95-241">Удаление всех переопределе-</span><span class="sxs-lookup"><span data-stu-id="8ca95-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-242">Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-243">Проблема Chromium [#1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="8ca95-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <a name="updated-long-tasks-ui"></a><span data-ttu-id="8ca95-244">Обновленный пользовательский интерфейс длинных задач</span><span class="sxs-lookup"><span data-stu-id="8ca95-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="8ca95-245">Long **Task —** это код JavaScript, который монополизирует основной поток в течение длительного времени, из-за чего веб-страница замерзает.</span><span class="sxs-lookup"><span data-stu-id="8ca95-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="8ca95-246">Некоторое время [][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] вы могли визуализировать длинные задачи в панели Performance, но в Microsoft Edge 83 пользовательский интерфейс визуализации длинных задач в панели Performance был обновлен.</span><span class="sxs-lookup"><span data-stu-id="8ca95-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="8ca95-247">Длинная часть задачи теперь окрашена полосатым красным фоном.</span><span class="sxs-lookup"><span data-stu-id="8ca95-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Новый пользовательский интерфейс long Task" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="8ca95-249">Новый пользовательский интерфейс long Task</span><span class="sxs-lookup"><span data-stu-id="8ca95-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="8ca95-250">Отправьте свои отзывы, [отправив твит][PostTweetEdgeDevTools] или отправив значок [Отправка отзывов!](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="8ca95-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="8ca95-251">Проблема Chromium [#1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="8ca95-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <a name="maskable-icon-support-in-the-manifest-pane"></a><span data-ttu-id="8ca95-252">Поддержка значка маскировки в области Манифест</span><span class="sxs-lookup"><span data-stu-id="8ca95-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="8ca95-253">Android Oreo представил адаптивные значки, которые отображают значки приложений в различных формах на разных моделях устройств.</span><span class="sxs-lookup"><span data-stu-id="8ca95-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="8ca95-254">**Маскируемые** значки — это новый формат значков, который поддерживает адаптивные значки, которые позволяют обеспечить хорошее внешний вид значка [PWA][ProgressiveWebAppsChromiumIndex] на устройствах, поддерживаюх стандартные значки с масками.</span><span class="sxs-lookup"><span data-stu-id="8ca95-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][ProgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="8ca95-255">Вкажите в новом **Show** только минимальную безопасную область для почтового ящика с масками значков в области **Манифест,** чтобы проверить, хорошо ли выглядит ваша маскабельная иконка на устройствах Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="8ca95-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Показать только минимальную безопасную область для проверки маскируемых значков" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="8ca95-257">Показать **только минимальную безопасную область для проверки маскируемых значков**</span><span class="sxs-lookup"><span data-stu-id="8ca95-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8ca95-258">Эта функция запущена в Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="8ca95-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="8ca95-259">Обновления, охватываемых здесь в Microsoft Edge 83, не были охвачены в [What's New In DevTools (Microsoft Edge 81).][WhatsNew81]</span><span class="sxs-lookup"><span data-stu-id="8ca95-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="8ca95-260">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="8ca95-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="8ca95-261">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ca95-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="8ca95-262">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="8ca95-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="8ca95-263">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ca95-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Новые возможности в DevTools (Microsoft Edge 81) | Документы Майкрософт"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Измените цвета с помощью | Документы Майкрософт"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Начало работы с просмотром и изменением CSS-| Документы Майкрософт"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение размещения из основного меню | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основных действий потоков | Документы Майкрософт"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности визуализации с помощью вкладки Rendering | Документы Майкрософт"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладки устройств Windows 10 | Документы Майкрософт"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Breakpoints line-of-code - How To Pause Your Code with Breakpoints in Microsoft Edge DevTools | Документы Майкрософт"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам — ссылки на | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка Microsoft Edge DevTools | Документы Майкрософт"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Обзор портала устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные средства для Microsoft Edge (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Обновление выпусков стабильных каналов для Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Новая проблема - MicrosoftDocs/edge-developer - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools учетной записи Twitter"  
[TheWebWeWant]: https://webwewant.fyi "Веб-сайт, который мы хотим"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Типы цветовой слепоты"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящих от локального доступа"  

[CR963183]: https://crbug.com/963183 "Выпуск 963183: DevTools не соответствуют требованиям WCAG"  
[CR1003700]: https://crbug.com/1003700 "Выпуск 1003700. Добавление поддержки DevTools для моделирования дефицита цветового зрения"  
[CR1011679]: https://crbug.com/1011679 "Выпуск 1011679: ввести пункт "Стыковка налево" с помощью командного меню"  
[CR1016501]: https://crbug.com/1016501 "Выпуск 1016501: запрос на функции: кнопка для удаления всех локальных переопределей"  
[CR1050999]: https://crbug.com/1050999 "Выпуск 1050999: Вкладка свойств"  
[CR1051466]: https://crbug.com/1051466 "Выпуск 1051466: поддержка отладки COOP/COEP в DevTools"  
[CR1054447]: https://crbug.com/1054447 "Выпуск 1054447: Обновление показателей производительности в Хронике DevTools"  
[CR1051822]: https://crbug.com/1051822 "Выпуск 1051822: DevTools: добавление пользовательского интерфейса для эмуляции локального интерфейса"
[CR1041830]: https://crbug.com/1041830 "Выпуск 1041830: улучшение цветов для точек разрыва"
[CR1050855]: https://crbug.com/1050855 "Выпуск 1050855: трудно найти представление параметров"
[CR1056348]: https://crbug.com/1056348 "Выпуск 1056348: обновление компонентов Infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "CoOP и COEP — политика кросс-origin Opener"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "CoOP и COEP — политика встраивляемого перекрестного происхождения"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Маяк | GitHub"  

> [!NOTE]
> <span data-ttu-id="8ca95-305">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8ca95-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8ca95-306">Оригинальная страница [](https://developers.google.com/web/updates/2020/03/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="8ca95-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8ca95-308">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8ca95-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
