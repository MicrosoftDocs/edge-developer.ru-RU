---
description: Справочник по всем способам записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d5b6be92c1419ba880a94c62c3f586a740816622
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230763"
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

# <span data-ttu-id="842c9-104">Справочные материалы по анализу производительности</span><span class="sxs-lookup"><span data-stu-id="842c9-104">Performance analysis reference</span></span>  

<span data-ttu-id="842c9-105">Эта страница является полным справочником по функциям Microsoft Edge DevTools, связанным с анализом производительности.</span><span class="sxs-lookup"><span data-stu-id="842c9-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="842c9-106">Перейдите [к курсу "Начало][DevtoolsEvaluatePerformanceGettingStarted] работы с анализом производительности времени выполнения", чтобы получить руководство по анализу производительности страницы с помощью [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="842c9-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <span data-ttu-id="842c9-107">Запись производительности</span><span class="sxs-lookup"><span data-stu-id="842c9-107">Record performance</span></span>  

### <span data-ttu-id="842c9-108">Запись производительности в времени выполнения</span><span class="sxs-lookup"><span data-stu-id="842c9-108">Record runtime performance</span></span>  

<span data-ttu-id="842c9-109">Зафиксируйте производительность времени выполнения, если нужно проанализировать производительность страницы в ее работе, а не загрузку.</span><span class="sxs-lookup"><span data-stu-id="842c9-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="842c9-110">Перейдите на страницу, которую нужно проанализировать.</span><span class="sxs-lookup"><span data-stu-id="842c9-110">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="842c9-111">Выберите **вкладку "Производительность"** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="842c9-111">Choose the **Performance** tab in DevTools.</span></span>  
1.  <span data-ttu-id="842c9-112">Choose **Record** \( ![ Record icon ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="842c9-112">Choose **Record** \(![Record icon][ImageRecordIcon]\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="842c9-114">Record</span><span class="sxs-lookup"><span data-stu-id="842c9-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="842c9-115">Взаимодействовать со страницей.</span><span class="sxs-lookup"><span data-stu-id="842c9-115">Interact with the page.</span></span>  <span data-ttu-id="842c9-116">DevTools записи все действия страницы, которые происходят в результате ваших взаимодействий.</span><span class="sxs-lookup"><span data-stu-id="842c9-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="842c9-117">Choose **Record** again or choose **Stop** to stop recording.</span><span class="sxs-lookup"><span data-stu-id="842c9-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <span data-ttu-id="842c9-118">Запись производительности загрузки</span><span class="sxs-lookup"><span data-stu-id="842c9-118">Record load performance</span></span>  

<span data-ttu-id="842c9-119">Зафиксируйте производительность загрузки, если нужно проанализировать производительность страницы во время ее загрузки, а не запускать ее.</span><span class="sxs-lookup"><span data-stu-id="842c9-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="842c9-120">Перейдите на страницу, которую нужно проанализировать.</span><span class="sxs-lookup"><span data-stu-id="842c9-120">Go to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="842c9-121">Откройте панель **производительности** DevTools.</span><span class="sxs-lookup"><span data-stu-id="842c9-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="842c9-122">Choose **Refresh page** \( Refresh Page ![ ][ImageRefreshPageIcon] \).</span><span class="sxs-lookup"><span data-stu-id="842c9-122">Choose **Refresh page** \(![Refresh Page][ImageRefreshPageIcon]\).</span></span>  <span data-ttu-id="842c9-123">DevTools записывает метрики производительности во время обновления страницы, а затем автоматически останавливает запись через пару секунд после завершения загрузки.</span><span class="sxs-lookup"><span data-stu-id="842c9-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Страница обновления" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="842c9-125">Страница обновления</span><span class="sxs-lookup"><span data-stu-id="842c9-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="842c9-126">DevTools автоматически масштабируется в части записи, где произошла большая часть действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Запись загрузки страницы" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="842c9-128">Запись загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="842c9-128">A page-load recording</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-129">Снимок экрана во время записи</span><span class="sxs-lookup"><span data-stu-id="842c9-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="842c9-130">Включив этот **снимок экрана,** зафиксировать снимок экрана каждого кадра во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="The Screenshots checkbox" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="842c9-132">The **Screenshots** checkbox</span><span class="sxs-lookup"><span data-stu-id="842c9-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-133">Перейдите [к снимку экрана,](#view-a-screenshot) чтобы узнать, как взаимодействовать со снимками экрана.</span><span class="sxs-lookup"><span data-stu-id="842c9-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <span data-ttu-id="842c9-134">Принудительное сбор мусора во время записи</span><span class="sxs-lookup"><span data-stu-id="842c9-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="842c9-135">Пока вы записываете страницу, выберите "Сбор **мусора"** \( Значок ![ "Сбор ][ImageCollectGarbageIcon] мусора"), чтобы принудительно собрать сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="842c9-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon][ImageCollectGarbageIcon]\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Сбор мусора" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="842c9-137">Сбор мусора</span><span class="sxs-lookup"><span data-stu-id="842c9-137">Collect garbage</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-138">Показать параметры записи</span><span class="sxs-lookup"><span data-stu-id="842c9-138">Show recording settings</span></span>  

<span data-ttu-id="842c9-139">Choose **Capture settings** \( ![ Capture settings ][ImageCaptureSettingsIcon] \) to expose more settings related to how DevTools captures performance recordings.</span><span class="sxs-lookup"><span data-stu-id="842c9-139">Choose **Capture settings** \(![Capture settings][ImageCaptureSettingsIcon]\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Раздел "Параметры захвата"" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="842c9-141">Раздел **"Параметры захвата"**</span><span class="sxs-lookup"><span data-stu-id="842c9-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-142">Отключение примеров JavaScript</span><span class="sxs-lookup"><span data-stu-id="842c9-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="842c9-143">По умолчанию в основном **разделе** записи отображаются подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="842c9-144">Чтобы отключить эти стеки вызовов:</span><span class="sxs-lookup"><span data-stu-id="842c9-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="842c9-145">Откройте меню **параметров захвата.**</span><span class="sxs-lookup"><span data-stu-id="842c9-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="842c9-146">Перейдите [к параметрам демонстрации записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="842c9-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="842c9-147">Включите **этот контрольный ящик.**</span><span class="sxs-lookup"><span data-stu-id="842c9-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="842c9-148">Зафиксим страницу.</span><span class="sxs-lookup"><span data-stu-id="842c9-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="842c9-149">На следующих двух рисунках показана разница между отключением и включением примеров JavaScript.</span><span class="sxs-lookup"><span data-stu-id="842c9-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="842c9-150">Основной **раздел** записи намного короче, если выборка отключена, так как он опустить все стеки вызовов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="842c9-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Пример записи, когда отключены примеры JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="842c9-152">Пример записи, когда отключены примеры JS</span><span class="sxs-lookup"><span data-stu-id="842c9-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Пример записи, когда примеры JS включены" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="842c9-154">Пример записи, когда примеры JS включены</span><span class="sxs-lookup"><span data-stu-id="842c9-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="842c9-155">Throttle the network while recording</span><span class="sxs-lookup"><span data-stu-id="842c9-155">Throttle the network while recording</span></span>  

<span data-ttu-id="842c9-156">Чтобы отлалить сеть во время записи:</span><span class="sxs-lookup"><span data-stu-id="842c9-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="842c9-157">Откройте меню **параметров захвата.**</span><span class="sxs-lookup"><span data-stu-id="842c9-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="842c9-158">Перейдите [к параметрам демонстрации записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="842c9-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="842c9-159">Установите **для сети** нужный уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="842c9-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <span data-ttu-id="842c9-160">Throttle the CPU while recording</span><span class="sxs-lookup"><span data-stu-id="842c9-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="842c9-161">Чтобы отлалить ЦП при записи:</span><span class="sxs-lookup"><span data-stu-id="842c9-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="842c9-162">Откройте меню **параметров захвата.**</span><span class="sxs-lookup"><span data-stu-id="842c9-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="842c9-163">Перейдите [к параметрам демонстрации записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="842c9-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="842c9-164">Установите **для ЦП** нужный уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="842c9-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="842c9-165">Регулирование относительно возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="842c9-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="842c9-166">Например, при **замедлении работы ЦП** в 2 раза медленнее, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="842c9-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="842c9-167">DevTools не имитируют ЦП мобильных устройств, так как архитектура мобильных устройств сильно отличается от архитектуры настольных компьютеров и ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="842c9-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <span data-ttu-id="842c9-168">Включить расширенный инструментарий paint</span><span class="sxs-lookup"><span data-stu-id="842c9-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="842c9-169">Чтобы просмотреть подробный инструментарий paint:</span><span class="sxs-lookup"><span data-stu-id="842c9-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="842c9-170">Откройте меню **параметров захвата.**</span><span class="sxs-lookup"><span data-stu-id="842c9-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="842c9-171">Перейдите [к параметрам демонстрации записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="842c9-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="842c9-172">Проверьте , **включить расширенный инструментарий paint (медленно).**</span><span class="sxs-lookup"><span data-stu-id="842c9-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="842c9-173">Чтобы узнать, как взаимодействовать с данными paint, перейдите к слоям просмотра [и](#view-layers-information) профилю [просмотра кисти.](#view-paint-profiler)</span><span class="sxs-lookup"><span data-stu-id="842c9-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <span data-ttu-id="842c9-174">Сохранение записи</span><span class="sxs-lookup"><span data-stu-id="842c9-174">Save a recording</span></span>  

<span data-ttu-id="842c9-175">Чтобы сохранить запись, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите "Сохранить **профиль".**</span><span class="sxs-lookup"><span data-stu-id="842c9-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Сохранение профиля" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="842c9-177">Сохранение профиля</span><span class="sxs-lookup"><span data-stu-id="842c9-177">Save Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="842c9-178">Загрузка записи</span><span class="sxs-lookup"><span data-stu-id="842c9-178">Load a recording</span></span>  

<span data-ttu-id="842c9-179">Чтобы загрузить запись, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Профиль загрузки".**</span><span class="sxs-lookup"><span data-stu-id="842c9-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Профиль загрузки" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="842c9-181">Профиль загрузки</span><span class="sxs-lookup"><span data-stu-id="842c9-181">Load Profile</span></span>**  
:::image-end:::  

## <span data-ttu-id="842c9-182">Очистка предыдущей записи</span><span class="sxs-lookup"><span data-stu-id="842c9-182">Clear the previous recording</span></span>  

<span data-ttu-id="842c9-183">После записи нажмите кнопку **Clear recording** \( Clear recording icon \), чтобы очистить эту запись с ![ панели ][ImageClearRecordingIcon] **"Производительность".**</span><span class="sxs-lookup"><span data-stu-id="842c9-183">After making a recording, press **Clear recording** \(![Clear recording icon][ImageClearRecordingIcon]\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Очистка записи" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="842c9-185">Очистка записи</span><span class="sxs-lookup"><span data-stu-id="842c9-185">Clear recording</span></span>**  
:::image-end:::  

## <span data-ttu-id="842c9-186">Анализ записи производительности</span><span class="sxs-lookup"><span data-stu-id="842c9-186">Analyze a performance recording</span></span>  

<span data-ttu-id="842c9-187">После [записи производительности](#record-runtime-performance) или загрузки \*\*\*\* [записи](#record-load-performance)панель производительности предоставляет большое количество данных для анализа производительности только что произошло.</span><span class="sxs-lookup"><span data-stu-id="842c9-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <span data-ttu-id="842c9-188">Выбор части записи</span><span class="sxs-lookup"><span data-stu-id="842c9-188">Select a portion of a recording</span></span>  

<span data-ttu-id="842c9-189">Перетащите мышь влево \*\*\*\* или вправо по обзору, чтобы выбрать часть записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="842c9-190">Обзор **—** это раздел, содержащий **диаграммы FPS,** **ЦП**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="842c9-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Перетащите мышь по обзору для масштабирования" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="842c9-192">Перетащите мышь по **обзору для** масштабирования</span><span class="sxs-lookup"><span data-stu-id="842c9-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-193">Чтобы выбрать часть с помощью клавиатуры:</span><span class="sxs-lookup"><span data-stu-id="842c9-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="842c9-194">Выберите фон раздела **Main** или любой из разделов рядом с ними, например "Взаимодействия", \*\*\*\* **"Сеть"** или **"GPU".**</span><span class="sxs-lookup"><span data-stu-id="842c9-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="842c9-195">Этот рабочий процесс клавиатуры работает только в том случае, если один из этих разделов находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="842c9-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="842c9-196">Используйте `W` клавиши , , , чтобы увеличить масштаб, переместить влево, уменьшить масштаб и переместить `A` `S` `D` вправо, соответственно.</span><span class="sxs-lookup"><span data-stu-id="842c9-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="842c9-197">Чтобы выбрать часть с помощью панели отслеживания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="842c9-198">Наведите указатель мыши на раздел **"Обзор"** или **"Сведения".**</span><span class="sxs-lookup"><span data-stu-id="842c9-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="842c9-199">Раздел **"Обзор"** — это область, **содержащая диаграммы FPS,** **ЦП**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="842c9-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="842c9-200">Раздел **"Сведения"** — это область, **содержащая основной** раздел, раздел **"Взаимодействия"** и так далее.</span><span class="sxs-lookup"><span data-stu-id="842c9-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="842c9-201">Двумя пальцами проведите пальцем вверх, чтобы уменьшить масштаб, проведите пальцем влево, прокрутка вниз, чтобы увеличить масштаб, и проведите пальцем вправо, чтобы переместить вправо.</span><span class="sxs-lookup"><span data-stu-id="842c9-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="842c9-202">Чтобы прокрутить длинную диаграмму в разделе **Main** или любой из соседей, выберите и удерживайте при перетаскиванием вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="842c9-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="842c9-203">Перетащите влево и вправо, чтобы переместить выбранную часть записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <span data-ttu-id="842c9-204">Действия поиска</span><span class="sxs-lookup"><span data-stu-id="842c9-204">Search activities</span></span>  

<span data-ttu-id="842c9-205">Выберите `Control` + `F` \(Windows, Linux\) или `Command` + `F` \(macOS\), \*\*\*\* чтобы открыть поле поиска в нижней части панели производительности.</span><span class="sxs-lookup"><span data-stu-id="842c9-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Поле поиска" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="842c9-207">Поле поиска</span><span class="sxs-lookup"><span data-stu-id="842c9-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-208">Для навигации по действиям, которые соответствуют вашему запросу:</span><span class="sxs-lookup"><span data-stu-id="842c9-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="842c9-209">Используйте кнопки **Previous** \( ![ Previous ][ImagePreviousIcon] \) и **Next** \( ![ Next ][ImageNextIcon] \).</span><span class="sxs-lookup"><span data-stu-id="842c9-209">Use the **Previous** \(![Previous][ImagePreviousIcon]\) and **Next** \(![Next][ImageNextIcon]\) buttons.</span></span>  
*   <span data-ttu-id="842c9-210">Выберите `Shift` + `Enter` предыдущий или `Enter` следующий.</span><span class="sxs-lookup"><span data-stu-id="842c9-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="842c9-211">Изменение параметров запроса:</span><span class="sxs-lookup"><span data-stu-id="842c9-211">To modify query settings:</span></span>  

*   <span data-ttu-id="842c9-212">Нажмите **"С чувствительным** к делу" \( ![ "С чувствительным к ][ImageSearchCaseIcon] делу"), чтобы сделать запрос чувствительным к делу.</span><span class="sxs-lookup"><span data-stu-id="842c9-212">Press **Case sensitive** \(![Case sensitive][ImageSearchCaseIcon]\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="842c9-213">Нажмите **Regex** \( ![ Regex ][ImageSearchRegexIcon] \), чтобы использовать регулярное выражение в запросе.</span><span class="sxs-lookup"><span data-stu-id="842c9-213">Press **Regex** \(![Regex][ImageSearchRegexIcon]\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="842c9-214">Чтобы скрыть поле поиска, нажмите кнопку **"Отмена".**</span><span class="sxs-lookup"><span data-stu-id="842c9-214">To hide the search box, press **Cancel**.</span></span>  

### <span data-ttu-id="842c9-215">Просмотр активности основного потока</span><span class="sxs-lookup"><span data-stu-id="842c9-215">View main thread activity</span></span>  

<span data-ttu-id="842c9-216">Используйте основной **раздел** для просмотра действий, которые произошли в основном потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="842c9-218">Основной \*\*\*\* раздел</span><span class="sxs-lookup"><span data-stu-id="842c9-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-219">Выберите событие, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**  DevTools описывает выбранное событие.</span><span class="sxs-lookup"><span data-stu-id="842c9-219">Choose an event to view more information about it in the **Summary** tab.  DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Дополнительные сведения об анонимной функции на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="842c9-221">Дополнительные сведения о `anonymous` функции на **вкладке "Сводка"**</span><span class="sxs-lookup"><span data-stu-id="842c9-221">More information about the `anonymous` function in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-222">DevTools представляет основные действия потока с помощью диаграммы ..</span><span class="sxs-lookup"><span data-stu-id="842c9-222">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="842c9-223">Ось x представляет запись с течением времени.</span><span class="sxs-lookup"><span data-stu-id="842c9-223">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="842c9-224">Ось Y представляет стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="842c9-224">The y-axis represents the call stack.</span></span>  <span data-ttu-id="842c9-225">События в верхней части вызывают события под ней.</span><span class="sxs-lookup"><span data-stu-id="842c9-225">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Диаграмма с замеской диаграммой" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="842c9-227">Диаграмма с замеской диаграммой</span><span class="sxs-lookup"><span data-stu-id="842c9-227">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-228">На предыдущем рисунке событие `click` вызвало событие `Function Call` в `activitytabs.js` строке 53.</span><span class="sxs-lookup"><span data-stu-id="842c9-228">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="842c9-229">Ниже `Function Call` приведены сообщения о том, что была запускаться анонимная функция.</span><span class="sxs-lookup"><span data-stu-id="842c9-229">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="842c9-230">Запрашиваемая анонимная `a` функция, которая запросила `wait` `Minor GC` запрос.</span><span class="sxs-lookup"><span data-stu-id="842c9-230">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="842c9-231">DevTools назначает скриптам случайные цвета.</span><span class="sxs-lookup"><span data-stu-id="842c9-231">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="842c9-232">На предыдущем рисунке запросы функций из одного сценария имеют светло-зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="842c9-232">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="842c9-233">Запросы от другого сценария имеют цвет бежевого цвета.</span><span class="sxs-lookup"><span data-stu-id="842c9-233">Requests from another script are colored beige.</span></span>  <span data-ttu-id="842c9-234">Темно-желтый представляет действие при написании скриптов, а сиреневый — действие отрисовки.</span><span class="sxs-lookup"><span data-stu-id="842c9-234">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="842c9-235">Эти темные желтые и сиреневые события согласованы во всех записях.</span><span class="sxs-lookup"><span data-stu-id="842c9-235">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="842c9-236">Если вы хотите скрыть подробную диаграмму запросов [JavaScript,](#disable-javascript-samples) перейдите в окне "Отключить примеры JavaScript".</span><span class="sxs-lookup"><span data-stu-id="842c9-236">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="842c9-237">Если примеры JS отключены, отображаются только события высокого уровня, такие как и на `Event: click` `Function Call` предыдущем `str` рисунке.</span><span class="sxs-lookup"><span data-stu-id="842c9-237">When JS samples are disabled, only high-level events such as `Event: click` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <span data-ttu-id="842c9-238">Просмотр действий в таблице</span><span class="sxs-lookup"><span data-stu-id="842c9-238">View activities in a table</span></span>  

<span data-ttu-id="842c9-239">После записи страницы вам не нужно полагаться \*\*\*\* только на основной раздел для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="842c9-239">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="842c9-240">DevTools также предоставляет три таблильных представления для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="842c9-240">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="842c9-241">Каждое представление дает разные представления о действиях:</span><span class="sxs-lookup"><span data-stu-id="842c9-241">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="842c9-242">Если вы хотите просмотреть корневые действия, которые вызывают большую часть работы, используйте вкладку ["Дерево вызовов".](#the-call-tree-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-242">When you want to view the root activities that cause the most work, use [the Call Tree tab](#the-call-tree-tab).</span></span>  
*   <span data-ttu-id="842c9-243">Если вы хотите просмотреть действия, на которые было потрачено больше всего времени, используйте вкладку [Bottom-Up.](#the-bottom-up-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-243">When you want to view the activities where the most time was directly spent, use [the Bottom-Up tab](#the-bottom-up-tab).</span></span>  
*   <span data-ttu-id="842c9-244">Чтобы просмотреть действия в том порядке, в котором они произошли во время записи, используйте вкладку ["Журнал событий".](#the-event-log-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-244">When you want to view the activities in the order in which they occurred during the recording, use [the Event Log tab](#the-event-log-tab).</span></span>  
    
> [!NOTE]
> <span data-ttu-id="842c9-245">Следующие три раздела относятся к одной и той же демонстрации.</span><span class="sxs-lookup"><span data-stu-id="842c9-245">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="842c9-246">Запустите демонстрацию самостоятельно на [демонстрационных вкладок активности.][ActivityTabsDemo]</span><span class="sxs-lookup"><span data-stu-id="842c9-246">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <span data-ttu-id="842c9-247">Корневые действия</span><span class="sxs-lookup"><span data-stu-id="842c9-247">Root activities</span></span>  

<span data-ttu-id="842c9-248">Ниже объясняется концепция \*\*\*\* корневых действий, \*\*\*\* упоминаемая в разделах "Дерево вызовов", "Снизу **вверх"** и **"Журнал событий".**</span><span class="sxs-lookup"><span data-stu-id="842c9-248">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** tab, **Bottom-Up** tab, and **Event Log** sections.</span></span>  

<span data-ttu-id="842c9-249">Корневые действия — это те действия, которые приводят к определенной работе браузера.</span><span class="sxs-lookup"><span data-stu-id="842c9-249">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="842c9-250">Например, при выборе веб-страницы браузер выполняет действие в качестве `Event` корневого действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-250">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="842c9-251">Это `Event` может привести к запуску обработера и так далее.</span><span class="sxs-lookup"><span data-stu-id="842c9-251">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="842c9-252">На диаграмме "Главный" **корневые** действия находятся в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="842c9-252">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="842c9-253">На **вкладке "Дерево вызовов"** и **"Журнал событий"** корневые действия являются элементами верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="842c9-253">In the **Call Tree** and **Event Log** tabs, root activities are the top-level items.</span></span>  

<span data-ttu-id="842c9-254">Перейдите [на вкладку "Дерево вызовов"](#the-call-tree-tab) для примера корневых действий.</span><span class="sxs-lookup"><span data-stu-id="842c9-254">Navigate to [The Call Tree tab](#the-call-tree-tab) for an example of root activities.</span></span>  

#### <span data-ttu-id="842c9-255">Вкладка "Дерево вызовов"</span><span class="sxs-lookup"><span data-stu-id="842c9-255">The Call Tree tab</span></span>  

<span data-ttu-id="842c9-256">Используйте **вкладку "Дерево** вызовов", чтобы просмотреть, какие [корневые действия](#root-activities) вызывают больше всего работы.</span><span class="sxs-lookup"><span data-stu-id="842c9-256">Use the **Call Tree** tab to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="842c9-257">Вкладка **"Дерево** вызовов" отображает действия только во время выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-257">The **Call Tree** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="842c9-258">Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="842c9-258">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Вкладка "Дерево вызовов"" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="842c9-260">Вкладка **"Дерево вызовов"**</span><span class="sxs-lookup"><span data-stu-id="842c9-260">The **Call Tree** tab</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-261">На предыдущем рисунке верхний уровень элементов в столбце "Действие", например корневые \*\*\*\* `Evaluate Script` `Parse HTML` действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-261">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="842c9-262">Вложенное представляет стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="842c9-262">The nesting represents the call stack.</span></span>  <span data-ttu-id="842c9-263">Например, на предыдущем рисунке, `Parse HTML` который вызвал `Evaluate Script` и `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="842c9-263">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="842c9-264">**Self Time** представляет время, непосредственно затраченное на это действие.</span><span class="sxs-lookup"><span data-stu-id="842c9-264">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="842c9-265">**Общее время** представляет время, затраченное на это действие или любой из его детей.</span><span class="sxs-lookup"><span data-stu-id="842c9-265">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="842c9-266">Выберите **"Самостоятельное время",** **"Общее время"** или **"Действия",** чтобы отсортировать таблицу по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="842c9-266">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="842c9-267">Используйте **текстовое поле фильтра** для фильтрации событий по имени действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-267">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="842c9-268">По умолчанию для **меню группировки** установлено значение **"Нет группировки".**</span><span class="sxs-lookup"><span data-stu-id="842c9-268">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="842c9-269">Используйте меню **группировки** для сортировки таблицы действий на основе различных критериев.</span><span class="sxs-lookup"><span data-stu-id="842c9-269">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="842c9-270">Choose **Show Heaviest Stack** \( Show ![ Heaviest Stack ][ImageShowHeaviestStackIcon] \) to reveal another table to the right of the **Activity** table.</span><span class="sxs-lookup"><span data-stu-id="842c9-270">Choose **Show Heaviest Stack** \(![Show Heaviest Stack][ImageShowHeaviestStackIcon]\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="842c9-271">Выберите действие для заполнения самой **активной таблицы стека.**</span><span class="sxs-lookup"><span data-stu-id="842c9-271">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="842c9-272">В **таблице "Самый большой** стек" отображается, какие из выбранных действий больше всего запускались.</span><span class="sxs-lookup"><span data-stu-id="842c9-272">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <span data-ttu-id="842c9-273">Вкладка Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="842c9-273">The Bottom-Up tab</span></span>  

<span data-ttu-id="842c9-274">Вкладка **"Снизу вверх"** используется для просмотра действий, которые непосредственно заняли больше всего времени в совокупности.</span><span class="sxs-lookup"><span data-stu-id="842c9-274">Use the **Bottom-Up** tab to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="842c9-275">На **вкладке "Снизу вверх"** отображаются только действия в выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-275">The **Bottom-Up** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="842c9-276">Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="842c9-276">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Вкладка Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="842c9-278">Вкладка **"Снизу вверх"**</span><span class="sxs-lookup"><span data-stu-id="842c9-278">The **Bottom-Up** tab</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-279">На **диаграмме "Главный** раздел" предыдущего рисунка перейдите к этому практически всему времени, затраченному на `Parse HTML` запуск.</span><span class="sxs-lookup"><span data-stu-id="842c9-279">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="842c9-280">Верхнее действие на **вкладке "Вверх"** предыдущего рисунка — `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="842c9-280">The top activity in the **Bottom-Up** tab of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="842c9-281">Перейдите на **вкладку "Снизу вверх".** Далее самое дорогое действие `Layout` .</span><span class="sxs-lookup"><span data-stu-id="842c9-281">Navigate to the **Bottom-Up** tab, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="842c9-282">Столбец **"Самообнаправление"** представляет собой агрегированное время, затраченное непосредственно на это действие, во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="842c9-282">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="842c9-283">Столбец **"Общее время"** представляет собой агрегированное время, затраченное на это действие или на какие-либо из его детей.</span><span class="sxs-lookup"><span data-stu-id="842c9-283">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <span data-ttu-id="842c9-284">Вкладка "Журнал событий"</span><span class="sxs-lookup"><span data-stu-id="842c9-284">The Event Log tab</span></span>  

<span data-ttu-id="842c9-285">Вкладка **"Журнал событий"** используется для просмотра действий в том порядке, в котором они произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-285">Use the **Event Log** tab to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="842c9-286">Вкладка **"Журнал** событий" отображает действия только во время выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-286">The **Event Log** tab only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="842c9-287">Перейдите [к "Выбор части записи",](#select-a-portion-of-a-recording) чтобы узнать, как выбрать ее.</span><span class="sxs-lookup"><span data-stu-id="842c9-287">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Вкладка "Журнал событий"" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="842c9-289">Вкладка **"Журнал событий"**</span><span class="sxs-lookup"><span data-stu-id="842c9-289">The **Event Log** tab</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-290">Столбец **"Время начала"** представляет точку начала этого действия относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-290">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="842c9-291">Например, время начала выбранного элемента на предыдущем рисунке означает, что действие началось `175.7 ms` со 175,7 мс после начала записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-291">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="842c9-292">Столбец **"Самостоятельное** время" представляет время, затраченное непосредственно на это действие.</span><span class="sxs-lookup"><span data-stu-id="842c9-292">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="842c9-293">Столбцы **"Общее время"** представляют время, затраченное непосредственно на это действие или на какие-либо из детей.</span><span class="sxs-lookup"><span data-stu-id="842c9-293">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="842c9-294">Выберите **время начала,** **время**самостоятельного выбора или **общее** время сортировки таблицы по этому столбцу.</span><span class="sxs-lookup"><span data-stu-id="842c9-294">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="842c9-295">Используйте **текстовое поле фильтра** для фильтрации действий по имени.</span><span class="sxs-lookup"><span data-stu-id="842c9-295">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="842c9-296">Используйте меню **"Длительность",** чтобы отфильтровать все действия, которые заняли менее 1 мс или 15 мс.</span><span class="sxs-lookup"><span data-stu-id="842c9-296">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="842c9-297">По умолчанию в **меню "Длительность"** установлено значение **"Все",** то есть показаны все действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-297">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="842c9-298">Отключает **проверки загрузки,** сценариев, отрисовки или рисования, чтобы отфильтровать все действия из этих категорий. \*\*\*\* \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="842c9-298">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <span data-ttu-id="842c9-299">Просмотр действий GPU</span><span class="sxs-lookup"><span data-stu-id="842c9-299">View GPU activity</span></span>  

<span data-ttu-id="842c9-300">Просмотр действий GPU в разделе **GPU.**</span><span class="sxs-lookup"><span data-stu-id="842c9-300">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Раздел GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="842c9-302">Раздел **GPU**</span><span class="sxs-lookup"><span data-stu-id="842c9-302">The **GPU** section</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-303">Просмотр растровой активности</span><span class="sxs-lookup"><span data-stu-id="842c9-303">View raster activity</span></span>  

<span data-ttu-id="842c9-304">Просмотр растерных действий в **разделе Растера.**</span><span class="sxs-lookup"><span data-stu-id="842c9-304">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Раздел "Растер"" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="842c9-306">Раздел **"Растер"**</span><span class="sxs-lookup"><span data-stu-id="842c9-306">The **Raster** section</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-307">Просмотр взаимодействий</span><span class="sxs-lookup"><span data-stu-id="842c9-307">View interactions</span></span>  

<span data-ttu-id="842c9-308">Раздел **"Взаимодействия"** используется для поиска и анализа взаимодействий с пользователем, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-308">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Раздел "Взаимодействия"" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="842c9-310">Раздел **"Взаимодействия"**</span><span class="sxs-lookup"><span data-stu-id="842c9-310">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-311">Красная линия в нижней части взаимодействия представляет время, затраченное на ожидание главного потока.</span><span class="sxs-lookup"><span data-stu-id="842c9-311">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="842c9-312">Выберите взаимодействие, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**</span><span class="sxs-lookup"><span data-stu-id="842c9-312">Choose an interaction to view more information about it in the **Summary** tab.</span></span>  

### <span data-ttu-id="842c9-313">Анализ кадров в секунду</span><span class="sxs-lookup"><span data-stu-id="842c9-313">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="842c9-314">DevTools предоставляет множество способов анализа кадров в секунду:</span><span class="sxs-lookup"><span data-stu-id="842c9-314">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="842c9-315">Используйте [диаграмму FPS,](#the-fps-chart) чтобы получить обзор FPS в течение всей записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-315">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="842c9-316">Используйте [раздел "Кадры",](#the-frames-section) чтобы просмотреть, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="842c9-316">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="842c9-317">Используйте счетчик **FPS для** оценки в режиме реального времени в FPS при запуске страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-317">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="842c9-318">Перейдите [к просмотру кадров в секунду в режиме реального времени с помощью счетчика кадров](#view-frames-per-second-in-realtime-with-the-fps-meter)в секунду.</span><span class="sxs-lookup"><span data-stu-id="842c9-318">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <span data-ttu-id="842c9-319">Диаграмма FPS</span><span class="sxs-lookup"><span data-stu-id="842c9-319">The FPS chart</span></span>  

<span data-ttu-id="842c9-320">Диаграмма **FPS** предоставляет обзор частоты кадров во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-320">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="842c9-321">Как правило, чем выше зеленая гля, тем выше частота кадров.</span><span class="sxs-lookup"><span data-stu-id="842c9-321">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="842c9-322">Красная черта над **диаграммой FPS** — это предупреждение о том, что частота кадров отброшена настолько низко, что это может нанести вред пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="842c9-322">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="842c9-324">Диаграмма **FPS**</span><span class="sxs-lookup"><span data-stu-id="842c9-324">The **FPS** chart</span></span>  
:::image-end:::  

#### <span data-ttu-id="842c9-325">Раздел "Кадры"</span><span class="sxs-lookup"><span data-stu-id="842c9-325">The Frames section</span></span>  

<span data-ttu-id="842c9-326">В **разделе "Кадры"** указывается, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="842c9-326">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="842c9-327">Наведите курсор на кадр, чтобы просмотреть tooltip с дополнительными сведениями о нем.</span><span class="sxs-lookup"><span data-stu-id="842c9-327">Hover over a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Наведении курсор на кадр" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="842c9-329">Наведении курсор на кадр</span><span class="sxs-lookup"><span data-stu-id="842c9-329">Hover over a frame</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-330">Выберите кадр, чтобы просмотреть дополнительные сведения о кадре на вкладке **"Сводка".**  DevTools описывает выбранный кадр синим цветом.</span><span class="sxs-lookup"><span data-stu-id="842c9-330">Choose a frame to view more information about the frame in the **Summary** tab.  DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Просмотр кадра на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="842c9-332">Просмотр кадра на вкладке **"Сводка"**</span><span class="sxs-lookup"><span data-stu-id="842c9-332">View a frame in the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-333">Просмотр сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="842c9-333">View network requests</span></span>  

<span data-ttu-id="842c9-334">Раз развернуть **раздел "Сеть",** чтобы просмотреть каскад сетевых запросов, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-334">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Раздел "Сеть"" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="842c9-336">Раздел **"Сеть"**</span><span class="sxs-lookup"><span data-stu-id="842c9-336">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-337">Запросы имеют код цвета следующим образом:</span><span class="sxs-lookup"><span data-stu-id="842c9-337">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="842c9-338">HTML: синий</span><span class="sxs-lookup"><span data-stu-id="842c9-338">HTML: Blue</span></span>  
*   <span data-ttu-id="842c9-339">CSS: Сиреневый</span><span class="sxs-lookup"><span data-stu-id="842c9-339">CSS: Purple</span></span>  
*   <span data-ttu-id="842c9-340">JS: желтый</span><span class="sxs-lookup"><span data-stu-id="842c9-340">JS: Yellow</span></span>  
*   <span data-ttu-id="842c9-341">Изображения: зеленый</span><span class="sxs-lookup"><span data-stu-id="842c9-341">Images: Green</span></span>  
    
<span data-ttu-id="842c9-342">Выберите запрос, чтобы просмотреть дополнительные сведения о нем на **вкладке "Сводка".**  Например, на предыдущем рисунке \*\*\*\* вкладка "Сводка" отображает дополнительные сведения о синем запросе, выбранном в разделе **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="842c9-342">Choose a request to view more information about it in the **Summary** tab.  For example, in the previous figure, the **Summary** tab is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="842c9-343">Темно-синий квадрат в левом верхнем конце запроса означает, что это запрос с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="842c9-343">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="842c9-344">Светлее-синий квадрат означает более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="842c9-344">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="842c9-345">Например, на предыдущем рисунке синий выбранный запрос имеет более высокий приоритет, а зеленый — более низкий.</span><span class="sxs-lookup"><span data-stu-id="842c9-345">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="842c9-346">На 1-м из следующих рисунков запрос представлен линией слева, строкой в середине с темной частью и светлой частью, а также линией `www.bing.com` справа.</span><span class="sxs-lookup"><span data-stu-id="842c9-346">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="842c9-347">Во 2-й части следующих рисунков показано соответствующее представление того же запроса на вкладке **"Синхронизация"** панели **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="842c9-347">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** tab of the **Network** panel.</span></span>  <span data-ttu-id="842c9-348">Вот как эти два представления соовествуют друг с другом:</span><span class="sxs-lookup"><span data-stu-id="842c9-348">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="842c9-349">Левая строка — это вся группа `Connection Start` событий включительно.</span><span class="sxs-lookup"><span data-stu-id="842c9-349">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="842c9-350">Другими словами, это все до `Request Sent` , монопольный.</span><span class="sxs-lookup"><span data-stu-id="842c9-350">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="842c9-351">Светлая часть панели — `Request Sent` и `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="842c9-351">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="842c9-352">Темная часть панели — `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="842c9-352">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="842c9-353">Правая строка — это, по сути, время, затраченное на ожидание главного потока.</span><span class="sxs-lookup"><span data-stu-id="842c9-353">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="842c9-354">Он не представлен на вкладке **"Синхронизация".**</span><span class="sxs-lookup"><span data-stu-id="842c9-354">This is not represented in the **Timing** tab.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Представление строки запроса www.bing.com строки" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="842c9-356">Представление запроса на строке `www.bing.com`</span><span class="sxs-lookup"><span data-stu-id="842c9-356">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Средство "Сеть"" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="842c9-358">Средство **"Сеть"**</span><span class="sxs-lookup"><span data-stu-id="842c9-358">The **Network** tool</span></span>  
<span data-ttu-id="842c9-359">: ::image-end:::</span><span class="sxs-lookup"><span data-stu-id="842c9-359">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="842c9-360">Просмотр метрик памяти</span><span class="sxs-lookup"><span data-stu-id="842c9-360">View memory metrics</span></span>  

<span data-ttu-id="842c9-361">Включив этот **параметр,** вы можете просмотреть показатели памяти из последней записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-361">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="The Memory checkbox" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="842c9-363">The **Memory** checkbox</span><span class="sxs-lookup"><span data-stu-id="842c9-363">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-364">DevTools отображает новую диаграмму **"Память"** над вкладками **"Сводка".**  Под диаграммой **NET** также есть новая диаграмма **HEAP.**</span><span class="sxs-lookup"><span data-stu-id="842c9-364">DevTools displays a new **Memory** chart, above the **Summary** tab.  There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="842c9-365">Диаграмма **HEAP** предоставляет те же сведения, что и строка **"Куче JS"** в **диаграмме "Память".**</span><span class="sxs-lookup"><span data-stu-id="842c9-365">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Показатели памяти" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="842c9-367">Показатели памяти</span><span class="sxs-lookup"><span data-stu-id="842c9-367">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-368">Цветные линии на диаграмме со картой цветных контрольных точек над диаграммой.</span><span class="sxs-lookup"><span data-stu-id="842c9-368">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="842c9-369">Отключать этот контрольный ящик, чтобы скрыть эту категорию в диаграмме.</span><span class="sxs-lookup"><span data-stu-id="842c9-369">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="842c9-370">Диаграмма отображает только область выбранной в данный момент записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-370">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="842c9-371">Например, на предыдущем рисунке \*\*\*\* диаграмма "Память" показывает только использование памяти от 400 мс до отметки 1750 мс.</span><span class="sxs-lookup"><span data-stu-id="842c9-371">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <span data-ttu-id="842c9-372">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="842c9-372">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="842c9-373">При анализе таких разделов, как **"Сеть"** или "Главная", \*\*\*\* иногда требуется более точную оценку времени, за который потребовалось определенное событие.</span><span class="sxs-lookup"><span data-stu-id="842c9-373">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="842c9-374">Удерживайте, выбирайте и удерживайте, перетаскивать влево или вправо, чтобы выбрать `Shift` часть записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-374">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="842c9-375">В нижней части выделения DevTools показывает, сколько времени занимает эта часть.</span><span class="sxs-lookup"><span data-stu-id="842c9-375">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Просмотр длительности части записи" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="842c9-377">Просмотр длительности части записи</span><span class="sxs-lookup"><span data-stu-id="842c9-377">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-378">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="842c9-378">View a screenshot</span></span>  

<span data-ttu-id="842c9-379">Перейдите [к снимкам экрана захвата](#capture-screenshots-while-recording) во время записи, чтобы узнать, как включить снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="842c9-379">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="842c9-380">Наведите курсор на **обзор,** чтобы просмотреть снимок экрана с изображением страницы в этот момент записи.</span><span class="sxs-lookup"><span data-stu-id="842c9-380">Hover over the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="842c9-381">Обзор **—** это раздел, содержащий **диаграммы ЦП,** **FPS**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="842c9-381">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Просмотр снимка экрана" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="842c9-383">Просмотр снимка экрана</span><span class="sxs-lookup"><span data-stu-id="842c9-383">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-384">Снимки экрана также можно просмотреть, выбрав кадр в разделе **"Кадры".**</span><span class="sxs-lookup"><span data-stu-id="842c9-384">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="842c9-385">DevTools отображает небольшую версию снимка экрана на вкладке **"Сводка".**</span><span class="sxs-lookup"><span data-stu-id="842c9-385">DevTools displays a small version of the screenshot in the **Summary** tab.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Просмотр снимка экрана на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="842c9-387">Просмотр снимка экрана на **вкладке "Сводка"**</span><span class="sxs-lookup"><span data-stu-id="842c9-387">View a screenshot in the **Summary** tab</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-388">Выберите эскиз на вкладке **"Сводка",** чтобы увеличить масштаб на снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="842c9-388">Choose the thumbnail in the **Summary** tab to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Масштабирование снимка экрана на вкладке "Сводка"" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="842c9-390">Масштабирование снимка экрана на **вкладке "Сводка"**</span><span class="sxs-lookup"><span data-stu-id="842c9-390">Zoom into a screenshot from the **Summary** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="842c9-391">Просмотр сведений о уровнях</span><span class="sxs-lookup"><span data-stu-id="842c9-391">View layers information</span></span>  

<span data-ttu-id="842c9-392">Чтобы просмотреть сведения о расширенных уровнях кадра:</span><span class="sxs-lookup"><span data-stu-id="842c9-392">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="842c9-393">[Включив расширенный инструментарий paint.](#turn-on-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="842c9-393">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="842c9-394">Выберите кадр в разделе **"Кадры".**</span><span class="sxs-lookup"><span data-stu-id="842c9-394">Select a frame in the **Frames** section.</span></span>  <span data-ttu-id="842c9-395">DevTools отображает сведения о слоях на новой вкладке **"Слои"** рядом с вкладкой **"Журнал событий".**</span><span class="sxs-lookup"><span data-stu-id="842c9-395">DevTools displays information about the layers in the new **Layers** tab, next to the **Event Log** tab.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="The Layers pane" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="842c9-397">The **Layers** pane</span><span class="sxs-lookup"><span data-stu-id="842c9-397">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="842c9-398">Наведите курсор на слой, чтобы выделить его на схеме.</span><span class="sxs-lookup"><span data-stu-id="842c9-398">Hover over a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Выделение слоя" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="842c9-400">Выделение слоя</span><span class="sxs-lookup"><span data-stu-id="842c9-400">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="842c9-401">Чтобы переместить схему:</span><span class="sxs-lookup"><span data-stu-id="842c9-401">To move the diagram:</span></span>  

*   <span data-ttu-id="842c9-402">Choose **Pan Mode** \( Pan Mode ![ ][ImagePanModeIcon] \) to move along the X and Y axes.</span><span class="sxs-lookup"><span data-stu-id="842c9-402">Choose **Pan Mode** \(![Pan Mode][ImagePanModeIcon]\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="842c9-403">Выберите **режим поворота** \( ![ Режим поворота ][ImageRotateModeIcon] \), чтобы вращаться вдоль оси Z.</span><span class="sxs-lookup"><span data-stu-id="842c9-403">Choose **Rotate Mode** \(![Rotate Mode][ImageRotateModeIcon]\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="842c9-404">Choose **Reset Transform** \( Reset Transform ![ ][ImageResetTransformIcon] \) to reset the diagram to the original position.</span><span class="sxs-lookup"><span data-stu-id="842c9-404">Choose **Reset Transform** \(![Reset Transform][ImageResetTransformIcon]\) to reset the diagram to the original position.</span></span>  
    
### <span data-ttu-id="842c9-405">Просмотр профиля paint</span><span class="sxs-lookup"><span data-stu-id="842c9-405">View paint profiler</span></span>  

<span data-ttu-id="842c9-406">Чтобы просмотреть дополнительные сведения о событии paint:</span><span class="sxs-lookup"><span data-stu-id="842c9-406">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="842c9-407">[Включит](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="842c9-407">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="842c9-408">Выберите событие **Paint** в основном **разделе.**</span><span class="sxs-lookup"><span data-stu-id="842c9-408">Select a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Вкладка "Профиль paint"" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="842c9-410">Вкладка **"Профиль paint"**</span><span class="sxs-lookup"><span data-stu-id="842c9-410">The **Paint Profiler** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="842c9-411">Анализ производительности отрисовки с помощью вкладки "Отрисовка"</span><span class="sxs-lookup"><span data-stu-id="842c9-411">Analyze rendering performance with the Rendering tab</span></span>  

<span data-ttu-id="842c9-412">Используйте функции вкладки **"Отрисовка"** для визуализации производительности отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-412">Use the features of the **Rendering** tab to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="842c9-413">Чтобы открыть **вкладку "Отрисовка":**</span><span class="sxs-lookup"><span data-stu-id="842c9-413">To open the **Rendering** tab:</span></span>  

1.  <span data-ttu-id="842c9-414">[Откройте меню команд.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="842c9-414">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="842c9-415">Начните ввод `Rendering` текста и выберите `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="842c9-415">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="842c9-416">DevTools отображает вкладку **"Отрисовка"** в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="842c9-416">DevTools displays the **Rendering** tab at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Вкладка "Отрисовка"" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="842c9-418">Вкладка **"Отрисовка"**</span><span class="sxs-lookup"><span data-stu-id="842c9-418">The **Rendering** tab</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="842c9-419">Просмотр кадров в секунду в режиме реального времени с помощью счетчика кадров в секунду</span><span class="sxs-lookup"><span data-stu-id="842c9-419">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="842c9-420">Счетчик **FPS —** это наложение, которое отображается в правом верхнем углу окна.</span><span class="sxs-lookup"><span data-stu-id="842c9-420">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="842c9-421">Он предоставляет оценку в режиме реального времени в FPS при запуске страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-421">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="842c9-422">Чтобы открыть счетчик **FPS:**</span><span class="sxs-lookup"><span data-stu-id="842c9-422">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="842c9-423">Откройте **вкладку "Отрисовка".**  Na [Анализ производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-423">Open the **Rendering** tab.  Na [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="842c9-424">Включите **флажки счетчика FPS.**</span><span class="sxs-lookup"><span data-stu-id="842c9-424">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="842c9-426">Счетчик **FPS**</span><span class="sxs-lookup"><span data-stu-id="842c9-426">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="842c9-427">Просмотр событий рисования в режиме реального времени с помощью paint Flashing</span><span class="sxs-lookup"><span data-stu-id="842c9-427">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="842c9-428">Используйте Paint Flashing, чтобы получить представление всех событий paint на странице в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="842c9-428">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="842c9-429">Каждый раз, когда часть страницы перерисовка, DevTools описывает этот раздел зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="842c9-429">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="842c9-430">Чтобы включить Paint Flashing, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-430">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="842c9-431">Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки на вкладке "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-431">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="842c9-432">Включите **контрольный ящик Paint Flashing.**</span><span class="sxs-lookup"><span data-stu-id="842c9-432">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="842c9-434">Paint Flashing</span><span class="sxs-lookup"><span data-stu-id="842c9-434">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <span data-ttu-id="842c9-435">Просмотр наложения слоев с границами уровней</span><span class="sxs-lookup"><span data-stu-id="842c9-435">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="842c9-436">Используйте **границы уровней** для просмотра наложения границ слоя и плиток в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-436">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="842c9-437">Чтобы включить границы уровня, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-437">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="842c9-438">Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-438">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="842c9-439">Включите **контрольный ящик "Границы** слоя".</span><span class="sxs-lookup"><span data-stu-id="842c9-439">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Границы слоя" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="842c9-441">Границы слоя</span><span class="sxs-lookup"><span data-stu-id="842c9-441">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="842c9-442">Перейдите к комментариям [в debug_colors.cc,][ChromiumDebugColors] чтобы получить объяснение цветового кодирования.</span><span class="sxs-lookup"><span data-stu-id="842c9-442">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <span data-ttu-id="842c9-443">Поиск проблем с производительностью прокрутки в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="842c9-443">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="842c9-444">Используйте проблемы с производительностью прокрутки, чтобы определить элементы страницы с прослушивателями событий, связанными с прокрутки, которые могут нанести вред производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="842c9-444">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="842c9-445">DevTools описывает потенциально проблемные элементы в этом документе.</span><span class="sxs-lookup"><span data-stu-id="842c9-445">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="842c9-446">Чтобы просмотреть проблемы с производительностью прокрутки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="842c9-446">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="842c9-447">Откройте **вкладку "Отрисовка".**  Перейдите [к анализу производительности отрисовки с помощью вкладки "Отрисовка".](#analyze-rendering-performance-with-the-rendering-tab)</span><span class="sxs-lookup"><span data-stu-id="842c9-447">Open the **Rendering** tab.  Navigate to [Analyze rendering performance with the Rendering tab](#analyze-rendering-performance-with-the-rendering-tab).</span></span>  
1.  <span data-ttu-id="842c9-448">Включите **контрольный список "Проблемы с производительностью прокрутки".**</span><span class="sxs-lookup"><span data-stu-id="842c9-448">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Проблемы прокрутки производительности указывают на то, что объекты с неуровневой прокруткой могут повредит производительности прокрутки" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="842c9-450">**Проблемы прокрутки производительности** указывают на то, что объекты с неуровневой прокруткой могут повредит производительности прокрутки</span><span class="sxs-lookup"><span data-stu-id="842c9-450">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="842c9-451">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="842c9-451">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Откройте меню команд — запустите команды с помощью меню команд Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Начало работы с анализом производительности во время выполнения | Документы Майкрософт"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Демонстрация вкладок активности | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc — поиск кода"  

> [!NOTE]
> <span data-ttu-id="842c9-457">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="842c9-457">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="842c9-458">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="842c9-458">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="842c9-460">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="842c9-460">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
