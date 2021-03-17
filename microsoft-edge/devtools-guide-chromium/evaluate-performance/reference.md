---
description: Ссылка на все способы записи и анализа производительности в Microsoft Edge DevTools.
title: Справочные материалы по анализу производительности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439691"
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

# <a name="performance-analysis-reference"></a><span data-ttu-id="79115-104">Справочные материалы по анализу производительности</span><span class="sxs-lookup"><span data-stu-id="79115-104">Performance analysis reference</span></span>  

<span data-ttu-id="79115-105">Эта страница — это всестороннюю ссылку на функции Microsoft Edge DevTools, связанные с анализом производительности.</span><span class="sxs-lookup"><span data-stu-id="79115-105">This page is a comprehensive reference of Microsoft Edge DevTools features related to analyzing performance.</span></span>  

<span data-ttu-id="79115-106">Перейдите [к началу][DevtoolsEvaluatePerformanceGettingStarted] работы с анализом производительности выполнения для руководства по анализу производительности страницы с помощью [Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="79115-106">Navigate to [Get Started With Analyzing Runtime Performance][DevtoolsEvaluatePerformanceGettingStarted] for a guided tutorial on how to analyze the performance of a page using [Microsoft Edge DevTools][MicrosoftEdgeDevTools].</span></span>  

## <a name="record-performance"></a><span data-ttu-id="79115-107">Запись производительности</span><span class="sxs-lookup"><span data-stu-id="79115-107">Record performance</span></span>  

### <a name="record-runtime-performance"></a><span data-ttu-id="79115-108">Запись выполнения</span><span class="sxs-lookup"><span data-stu-id="79115-108">Record runtime performance</span></span>  

<span data-ttu-id="79115-109">Запись производительности выполнения при анализе производительности страницы во время ее выполнения, а не загрузки.</span><span class="sxs-lookup"><span data-stu-id="79115-109">Record runtime performance when you want to analyze the performance of a page as it is running, as opposed to loading.</span></span>  

1.  <span data-ttu-id="79115-110">Перейдите на страницу, которую необходимо проанализировать.</span><span class="sxs-lookup"><span data-stu-id="79115-110">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="79115-111">Откройте средство **Performance** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="79115-111">Open the **Performance** tool in DevTools.</span></span>  
1.  <span data-ttu-id="79115-112">Выберите **запись** \. ![ Значок запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="79115-112">Choose **Record** \(![Record icon](../media/record-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Record" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **<span data-ttu-id="79115-114">Record</span><span class="sxs-lookup"><span data-stu-id="79115-114">Record</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="79115-115">Взаимодействие со страницей.</span><span class="sxs-lookup"><span data-stu-id="79115-115">Interact with the page.</span></span>  <span data-ttu-id="79115-116">DevTools записываю все действия страниц, которые происходят в результате взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="79115-116">DevTools records all page activity that occurs as a result of your interactions.</span></span>  
1.  <span data-ttu-id="79115-117">Выберите **запись** еще раз или **выберите Остановку,** чтобы остановить запись.</span><span class="sxs-lookup"><span data-stu-id="79115-117">Choose **Record** again or choose **Stop** to stop recording.</span></span>  
    
### <a name="record-load-performance"></a><span data-ttu-id="79115-118">Запись производительности нагрузки</span><span class="sxs-lookup"><span data-stu-id="79115-118">Record load performance</span></span>  

<span data-ttu-id="79115-119">Запись производительности нагрузки при анализе производительности страницы при ее загрузке, а не запуске.</span><span class="sxs-lookup"><span data-stu-id="79115-119">Record load performance when you want to analyze the performance of a page as it is loading, as opposed to running.</span></span>  

1.  <span data-ttu-id="79115-120">Перейдите на страницу, которую необходимо проанализировать.</span><span class="sxs-lookup"><span data-stu-id="79115-120">Navigate to the page that you want to analyze.</span></span>  
1.  <span data-ttu-id="79115-121">Откройте панель **Performance** devTools.</span><span class="sxs-lookup"><span data-stu-id="79115-121">Open the **Performance** panel of DevTools.</span></span>  
1.  <span data-ttu-id="79115-122">Выберите **страницу Обновления** \. ![ Страница обновления ](../media/refresh-page-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="79115-122">Choose **Refresh page** \(![Refresh Page](../media/refresh-page-icon.msft.png)\).</span></span>  <span data-ttu-id="79115-123">DevTools записывает показатели производительности при обновлении страницы, а затем автоматически останавливает запись через пару секунд после завершения нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79115-123">DevTools records performance metrics while the page refreshes and then automatically stops the recording a couple seconds after the load finishes.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Страница обновления" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **<span data-ttu-id="79115-125">Страница обновления</span><span class="sxs-lookup"><span data-stu-id="79115-125">Refresh page</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="79115-126">DevTools автоматически увеличивает масштаб на части записи, где происходило большинство действий.</span><span class="sxs-lookup"><span data-stu-id="79115-126">DevTools automatically zooms in on the portion of the recording where most of the activity occurred.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Запись загрузки страниц" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   <span data-ttu-id="79115-128">Запись загрузки страниц</span><span class="sxs-lookup"><span data-stu-id="79115-128">A page-load recording</span></span>  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a><span data-ttu-id="79115-129">Захват скриншотов во время записи</span><span class="sxs-lookup"><span data-stu-id="79115-129">Capture screenshots while recording</span></span>  

<span data-ttu-id="79115-130">Включив **контрольный ящик Screenshots,** чтобы запечатлеть снимок экрана каждого кадра во время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-130">Turn on the **Screenshots** checkbox to capture a screenshot of every frame while recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="Контрольный ящик Screenshots" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   <span data-ttu-id="79115-132">Контрольный **ящик Screenshots**</span><span class="sxs-lookup"><span data-stu-id="79115-132">The **Screenshots** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="79115-133">Перейдите [к просмотру экрана,](#view-a-screenshot) чтобы узнать, как взаимодействовать со снимками экрана.</span><span class="sxs-lookup"><span data-stu-id="79115-133">Navigate to [View a screenshot](#view-a-screenshot) to learn how to interact with screenshots.</span></span>  

### <a name="force-garbage-collection-while-recording"></a><span data-ttu-id="79115-134">Принудительное сбор мусора во время записи</span><span class="sxs-lookup"><span data-stu-id="79115-134">Force garbage collection while recording</span></span>  

<span data-ttu-id="79115-135">Во время записи страницы выберите **Сбор** мусора \( Сбор значка мусора \) для ![ ](../media/collect-garbage-icon.msft.png) принудительного сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="79115-135">While you are recording a page, choose **Collect garbage** \(![Collect garbage icon](../media/collect-garbage-icon.msft.png)\) to force garbage collection.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Сбор мусора" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   <span data-ttu-id="79115-137">Сбор мусора</span><span class="sxs-lookup"><span data-stu-id="79115-137">Collect garbage</span></span>  
:::image-end:::  

### <a name="show-recording-settings"></a><span data-ttu-id="79115-138">Показать параметры записи</span><span class="sxs-lookup"><span data-stu-id="79115-138">Show recording settings</span></span>  

<span data-ttu-id="79115-139">Выберите **параметры** Capture \. Параметры захвата \) для выбора дополнительных параметров, связанных с тем, как ![ ](../media/capture-settings-icon.msft.png) DevTools фиксирует записи производительности.</span><span class="sxs-lookup"><span data-stu-id="79115-139">Choose **Capture settings** \(![Capture settings](../media/capture-settings-icon.msft.png)\) to expose more settings related to how DevTools captures performance recordings.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Раздел Параметры захвата" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   <span data-ttu-id="79115-141">Раздел **Параметры захвата**</span><span class="sxs-lookup"><span data-stu-id="79115-141">The **Capture Settings** section</span></span>  
:::image-end:::  

### <a name="disable-javascript-samples"></a><span data-ttu-id="79115-142">Отключение образцов JavaScript</span><span class="sxs-lookup"><span data-stu-id="79115-142">Disable JavaScript samples</span></span>  

<span data-ttu-id="79115-143">По умолчанию в **основном разделе** записи отображаются подробные стеки вызовов функций JavaScript, которые были вызваны во время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-143">By default, the **Main** section of a recording displays detailed call stacks of JavaScript functions that were called during the recording.</span></span>  <span data-ttu-id="79115-144">Чтобы отключить эти стеки вызовов:</span><span class="sxs-lookup"><span data-stu-id="79115-144">To disable these call stacks:</span></span>  

1.  <span data-ttu-id="79115-145">Откройте меню **Параметры захвата.**</span><span class="sxs-lookup"><span data-stu-id="79115-145">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="79115-146">Перейдите [к показу параметров записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="79115-146">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="79115-147">Включим почтовый ящик **Disable JavaScript Samples.**</span><span class="sxs-lookup"><span data-stu-id="79115-147">Turn on the **Disable JavaScript Samples** checkbox.</span></span>  
1.  <span data-ttu-id="79115-148">Запись страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-148">Take a recording of the page.</span></span>  
    
<span data-ttu-id="79115-149">На следующих 2 рисунках отображается разница между отключением и включением образцов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79115-149">The following 2 figures display the difference between disabling and enabling JavaScript samples.</span></span>  <span data-ttu-id="79115-150">Основной **раздел** записи намного короче при отключении выборки, так как он ограничит все стеки вызовов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79115-150">The **Main** section of the recording is much shorter when sampling is disabled, because it omits all of the JavaScript call stacks.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Пример записи при отключении образцов JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         <span data-ttu-id="79115-152">Пример записи при отключении образцов JS</span><span class="sxs-lookup"><span data-stu-id="79115-152">An example of a recording when JS samples are disabled</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Пример записи при включении образцов JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         <span data-ttu-id="79115-154">Пример записи при включении образцов JS</span><span class="sxs-lookup"><span data-stu-id="79115-154">An example of a recording when JS samples are turned on</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a><span data-ttu-id="79115-155">Throttle сеть во время записи</span><span class="sxs-lookup"><span data-stu-id="79115-155">Throttle the network while recording</span></span>  

<span data-ttu-id="79115-156">Чтобы затормазать сеть во время записи:</span><span class="sxs-lookup"><span data-stu-id="79115-156">To throttle the network while recording:</span></span>  

1.  <span data-ttu-id="79115-157">Откройте меню **Параметры захвата.**</span><span class="sxs-lookup"><span data-stu-id="79115-157">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="79115-158">Перейдите [к показу параметров записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="79115-158">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="79115-159">Установите **Сеть** на нужный уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="79115-159">Set **Network** to the desired level of throttling.</span></span>  
    
### <a name="throttle-the-cpu-while-recording"></a><span data-ttu-id="79115-160">Throttle CPU во время записи</span><span class="sxs-lookup"><span data-stu-id="79115-160">Throttle the CPU while recording</span></span>  

<span data-ttu-id="79115-161">Чтобы затормазать ЦП во время записи:</span><span class="sxs-lookup"><span data-stu-id="79115-161">To throttle the CPU while recording:</span></span>  

1.  <span data-ttu-id="79115-162">Откройте меню **Параметры захвата.**</span><span class="sxs-lookup"><span data-stu-id="79115-162">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="79115-163">Перейдите [к показу параметров записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="79115-163">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="79115-164">Установите **ЦП** на нужный уровень регулирования.</span><span class="sxs-lookup"><span data-stu-id="79115-164">Set **CPU** to the desired level of throttling.</span></span>  
    
<span data-ttu-id="79115-165">Регулирование относительно возможностей компьютера.</span><span class="sxs-lookup"><span data-stu-id="79115-165">Throttling is relative to the capabilities of your computer.</span></span>  <span data-ttu-id="79115-166">Например, параметр **замедления 2x** делает работу ЦП в 2 раза медленнее обычной.</span><span class="sxs-lookup"><span data-stu-id="79115-166">For example, the **2x slowdown** option makes your CPU operate 2 times slower than normal.</span></span>  <span data-ttu-id="79115-167">DevTools не имитируют процессоры мобильных устройств, так как архитектура мобильных устройств сильно отличается от архитектуры настольных компьютеров и ноутбуков.</span><span class="sxs-lookup"><span data-stu-id="79115-167">DevTools do not truly simulate the CPUs of mobile devices, because the architecture of mobile devices is very different from that of desktops and laptops.</span></span>  

### <a name="turn-on-advanced-paint-instrumentation"></a><span data-ttu-id="79115-168">Включим расширенный инструментарий краски</span><span class="sxs-lookup"><span data-stu-id="79115-168">Turn on advanced paint instrumentation</span></span>  

<span data-ttu-id="79115-169">Чтобы просмотреть подробное инструментирование краски:</span><span class="sxs-lookup"><span data-stu-id="79115-169">To view detailed paint instrumentation:</span></span>  

1.  <span data-ttu-id="79115-170">Откройте меню **Параметры захвата.**</span><span class="sxs-lookup"><span data-stu-id="79115-170">Open the **Capture settings** menu.</span></span>  <span data-ttu-id="79115-171">Перейдите [к показу параметров записи.](#show-recording-settings)</span><span class="sxs-lookup"><span data-stu-id="79115-171">Navigate to [Show recording settings](#show-recording-settings).</span></span>  
1.  <span data-ttu-id="79115-172">Проверьте **контрольный ящик Enable advanced paint instrumentation (slow).**</span><span class="sxs-lookup"><span data-stu-id="79115-172">Check the **Enable advanced paint instrumentation (slow)** checkbox.</span></span>  

<span data-ttu-id="79115-173">Чтобы узнать, как взаимодействовать с информацией о краске, перейдите к [слоям Просмотра](#view-layers-information) и [просмотру профилера краски](#view-paint-profiler).</span><span class="sxs-lookup"><span data-stu-id="79115-173">To learn how to interact with the paint information, navigate to [View layers](#view-layers-information) and [View paint profiler](#view-paint-profiler).</span></span>  

## <a name="save-a-recording"></a><span data-ttu-id="79115-174">Сохранение записи</span><span class="sxs-lookup"><span data-stu-id="79115-174">Save a recording</span></span>  

<span data-ttu-id="79115-175">Чтобы сохранить запись, откройте контекстное меню \(правой кнопкой мыши\) и выберите **сохранить профиль**.</span><span class="sxs-lookup"><span data-stu-id="79115-175">To save a recording, open the contextual menu \(right-click\), and choose **Save Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Сохранение профиля" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **<span data-ttu-id="79115-177">Сохранение профиля</span><span class="sxs-lookup"><span data-stu-id="79115-177">Save Profile</span></span>**  
:::image-end:::  

## <a name="load-a-recording"></a><span data-ttu-id="79115-178">Загрузка записи</span><span class="sxs-lookup"><span data-stu-id="79115-178">Load a recording</span></span>  

<span data-ttu-id="79115-179">Чтобы загрузить запись, откройте контекстное меню \(правой кнопкой мыши\) и выберите **профиль нагрузки**.</span><span class="sxs-lookup"><span data-stu-id="79115-179">To load a recording, open the contextual menu \(right-click\), and choose **Load Profile**.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Профиль нагрузки" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **<span data-ttu-id="79115-181">Профиль нагрузки</span><span class="sxs-lookup"><span data-stu-id="79115-181">Load Profile</span></span>**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a><span data-ttu-id="79115-182">Очистка предыдущей записи</span><span class="sxs-lookup"><span data-stu-id="79115-182">Clear the previous recording</span></span>  

<span data-ttu-id="79115-183">После записи выберите **clear recording** \( Clear recording icon \) для очистки этой записи с панели ![ ](../media/clear-recording-icon.msft.png) **Performance.**</span><span class="sxs-lookup"><span data-stu-id="79115-183">After making a recording, choose **Clear recording** \(![Clear recording icon](../media/clear-recording-icon.msft.png)\) to clear that recording from the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Четкая запись" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **<span data-ttu-id="79115-185">Четкая запись</span><span class="sxs-lookup"><span data-stu-id="79115-185">Clear recording</span></span>**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a><span data-ttu-id="79115-186">Анализ записи производительности</span><span class="sxs-lookup"><span data-stu-id="79115-186">Analyze a performance recording</span></span>  

<span data-ttu-id="79115-187">После [записи производительности выполнения](#record-runtime-performance) или записи производительности нагрузки панель **Performance** предоставляет много данных для анализа производительности того, что только что произошло. [](#record-load-performance)</span><span class="sxs-lookup"><span data-stu-id="79115-187">After you [record runtime performance](#record-runtime-performance) or [record load performance](#record-load-performance), the **Performance** panel provides a lot of data for analyzing the performance of what just happened.</span></span>  

### <a name="select-a-portion-of-a-recording"></a><span data-ttu-id="79115-188">Выберите часть записи</span><span class="sxs-lookup"><span data-stu-id="79115-188">Select a portion of a recording</span></span>  

<span data-ttu-id="79115-189">Перетащите мышь влево или вправо по **обзору,** чтобы выбрать часть записи.</span><span class="sxs-lookup"><span data-stu-id="79115-189">Drag your mouse left or right across the **Overview** to select a portion of a recording.</span></span>  <span data-ttu-id="79115-190">Обзор **—** это раздел, содержащий **диаграммы FPS,** **CPU**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="79115-190">The **Overview** is the section that contains the **FPS**, **CPU**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Перетаскивать мышь через обзор для масштабирования" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   <span data-ttu-id="79115-192">Перетаскивать мышь через **обзор для** масштабирования</span><span class="sxs-lookup"><span data-stu-id="79115-192">Drag the mouse across the **Overview** to zoom</span></span>  
:::image-end:::  

<span data-ttu-id="79115-193">Чтобы выбрать часть с помощью клавиатуры:</span><span class="sxs-lookup"><span data-stu-id="79115-193">To select a portion using the keyboard:</span></span>  

1.  <span data-ttu-id="79115-194">Выберите фон основного **раздела** или любой из следующих разделов, например **Interactions,** **Network**или **GPU.**</span><span class="sxs-lookup"><span data-stu-id="79115-194">Choose the background of the **Main** section, or any of the sections next to it, such as **Interactions**, **Network**, or **GPU**.</span></span>  <span data-ttu-id="79115-195">Этот рабочий процесс клавиатуры работает только в том случае, если один из этих разделов находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="79115-195">This keyboard workflow only works when one of these sections is in focus.</span></span>  
1.  <span data-ttu-id="79115-196">Используйте `W` `A` клавиши , , чтобы увеличить, переместить `S` `D` влево, увеличить и переместить вправо, соответственно.</span><span class="sxs-lookup"><span data-stu-id="79115-196">Use the `W`, `A`, `S`, `D` keys to zoom in, move left, zoom out, and move right, respectively.</span></span>  

<span data-ttu-id="79115-197">Чтобы выбрать часть с помощью трекпада, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="79115-197">To select a portion using a trackpad, complete the following actions.</span></span>  

1.  <span data-ttu-id="79115-198">Наведите курсор мыши на раздел **Обзор** или раздел **Сведения.**</span><span class="sxs-lookup"><span data-stu-id="79115-198">Hover your mouse over the **Overview** section or the **Details** section.</span></span>  <span data-ttu-id="79115-199">Раздел **Обзор** — это область, содержащая **диаграммы FPS,** **CPU**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="79115-199">The **Overview** section is the area containing the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="79115-200">Раздел **Details** — это область, **содержащая основной** раздел, раздел **Взаимодействия** и так далее.</span><span class="sxs-lookup"><span data-stu-id="79115-200">The **Details** section is the area containing the **Main** section, the **Interactions** section, and so on.</span></span>  
1.  <span data-ttu-id="79115-201">С помощью двух пальцев проведите пальцем вверх, чтобы увеличить масштаб, проведите пальцем влево, чтобы переместить влево, проведите пальцем вниз, чтобы увеличить, и проведите пальцем вправо, чтобы переместить вправо.</span><span class="sxs-lookup"><span data-stu-id="79115-201">Using two fingers, swipe up to zoom out, swipe left to move left, swipe down to zoom in, and swipe right to move right.</span></span>  

<span data-ttu-id="79115-202">Чтобы прокрутить длинную диаграмму пламени в **разделе Main** или любом из соседей, выберите и удерживайте во время перетаскивание вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="79115-202">To scroll a long flame chart in the **Main** section or any of the neighbors, choose and hold while dragging up and down.</span></span>  <span data-ttu-id="79115-203">Перетащите влево и вправо, чтобы переместить выбранную часть записи.</span><span class="sxs-lookup"><span data-stu-id="79115-203">Drag left and right to move what portion of the recording is chosen.</span></span>  

### <a name="search-activities"></a><span data-ttu-id="79115-204">Действия поиска</span><span class="sxs-lookup"><span data-stu-id="79115-204">Search activities</span></span>  

<span data-ttu-id="79115-205">Выберите `Control` + `F` \(Windows, Linux\) `Command` + `F` или \(macOS\) \*\*\*\* для открытия окна поиска в нижней части панели Performance.</span><span class="sxs-lookup"><span data-stu-id="79115-205">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\) to open the search box at the bottom of the **Performance** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="Поле поиска" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   <span data-ttu-id="79115-207">Поле поиска</span><span class="sxs-lookup"><span data-stu-id="79115-207">The search box</span></span>  
:::image-end:::  

<span data-ttu-id="79115-208">Чтобы ориентироваться в действиях, которые соответствуют запросу:</span><span class="sxs-lookup"><span data-stu-id="79115-208">To navigate activities that match your query:</span></span>  

*   <span data-ttu-id="79115-209">Используйте **кнопки Previous** \( ![ Previous ](../media/previous-icon.msft.png) \) и **Next** ![ ](../media/next-icon.msft.png) \( Далее \).</span><span class="sxs-lookup"><span data-stu-id="79115-209">Use the **Previous** \(![Previous](../media/previous-icon.msft.png)\) and **Next** \(![Next](../media/next-icon.msft.png)\) buttons.</span></span>  
*   <span data-ttu-id="79115-210">Выберите `Shift` + `Enter` для выбора предыдущего или `Enter` для выбора следующего.</span><span class="sxs-lookup"><span data-stu-id="79115-210">Select `Shift`+`Enter` to select the previous or `Enter` to select the next.</span></span>  

<span data-ttu-id="79115-211">Изменение параметров запроса:</span><span class="sxs-lookup"><span data-stu-id="79115-211">To modify query settings:</span></span>  

*   <span data-ttu-id="79115-212">Выберите **деликатный** \. ![ Деловая ](../media/search-case-icon.msft.png) чувствительная \) для того, чтобы сделать запрос чувствительным.</span><span class="sxs-lookup"><span data-stu-id="79115-212">Choose **Case sensitive** \(![Case sensitive](../media/search-case-icon.msft.png)\) to make the query case sensitive.</span></span>  
*   <span data-ttu-id="79115-213">Выберите **Regex** \( Regex \) для использования ![ ](../media/search-regex-icon.msft.png) регулярного выражения в запросе.</span><span class="sxs-lookup"><span data-stu-id="79115-213">Choose **Regex** \(![Regex](../media/search-regex-icon.msft.png)\) to use a regular expression in your query.</span></span>  

<span data-ttu-id="79115-214">Чтобы скрыть поле поиска, выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="79115-214">To hide the search box, choose **Cancel**.</span></span>  

### <a name="view-main-thread-activity"></a><span data-ttu-id="79115-215">Просмотр основных действий потоков</span><span class="sxs-lookup"><span data-stu-id="79115-215">View main thread activity</span></span>  

<span data-ttu-id="79115-216">Используйте раздел **Main** для просмотра действий, которые произошли в основном потоке страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-216">Use the **Main** section to view activity that occurred on the main thread of the page.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   <span data-ttu-id="79115-218">Основной \*\*\*\* раздел</span><span class="sxs-lookup"><span data-stu-id="79115-218">The **Main** section</span></span>  
:::image-end:::  

<span data-ttu-id="79115-219">Выберите событие, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-219">Choose an event to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="79115-220">DevTools описывает выбранное событие.</span><span class="sxs-lookup"><span data-stu-id="79115-220">DevTools outlines the selected event.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Дополнительные сведения об анонимной функции в панели Сводка" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   <span data-ttu-id="79115-222">Дополнительные сведения о `anonymous` функции в панели **Сводка**</span><span class="sxs-lookup"><span data-stu-id="79115-222">More information about the `anonymous` function in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="79115-223">DevTools представляет собой основные потоковые действия с помощью схемы пламени.</span><span class="sxs-lookup"><span data-stu-id="79115-223">DevTools represents main thread activity with a flame chart.</span></span>  <span data-ttu-id="79115-224">X-axis представляет запись с течением времени.</span><span class="sxs-lookup"><span data-stu-id="79115-224">The x-axis represents the recording over time.</span></span>  <span data-ttu-id="79115-225">Y-axis представляет собой стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="79115-225">The y-axis represents the call stack.</span></span>  <span data-ttu-id="79115-226">События сверху вызывают события под ней.</span><span class="sxs-lookup"><span data-stu-id="79115-226">The events on top cause the events below it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Диаграмма пламени" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   <span data-ttu-id="79115-228">Диаграмма пламени</span><span class="sxs-lookup"><span data-stu-id="79115-228">A flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="79115-229">В предыдущем рисунке `click` событие вызвало в `Function Call` `activitytabs.js` строке 53.</span><span class="sxs-lookup"><span data-stu-id="79115-229">In the previous figure, a `click` event caused a `Function Call` in `activitytabs.js` on line 53.</span></span>  <span data-ttu-id="79115-230">Ниже `Function Call` см. отзыв о том, что была запустится анонимная функция.</span><span class="sxs-lookup"><span data-stu-id="79115-230">Below `Function Call`, review that an anonymous function was run.</span></span>  <span data-ttu-id="79115-231">Запрашиваемая анонимная функция `a` , которая запрашивала `wait` , которая запрашивала `Minor GC` .</span><span class="sxs-lookup"><span data-stu-id="79115-231">The anonymous function requested `a`, which requested `wait`, which requested `Minor GC`.</span></span>  

<span data-ttu-id="79115-232">DevTools назначает скрипты случайных цветов.</span><span class="sxs-lookup"><span data-stu-id="79115-232">DevTools assigns scripts random colors.</span></span>  <span data-ttu-id="79115-233">На предыдущем рисунке запросы функций из одного сценария имеют светло-зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="79115-233">In the previous figure, function requests from one script are colored light green.</span></span>  <span data-ttu-id="79115-234">Запросы из другого скрипта являются цветными бежевыми.</span><span class="sxs-lookup"><span data-stu-id="79115-234">Requests from another script are colored beige.</span></span>  <span data-ttu-id="79115-235">Более темный желтый цвет представляет действие скриптов, а фиолетовое событие — отрисовку.</span><span class="sxs-lookup"><span data-stu-id="79115-235">The darker yellow represents scripting activity, and the purple event represents rendering activity.</span></span>  <span data-ttu-id="79115-236">Эти более темные желтые и фиолетовые события согласуются во всех записях.</span><span class="sxs-lookup"><span data-stu-id="79115-236">These darker yellow and purple events are consistent across all recordings.</span></span>  

<span data-ttu-id="79115-237">Перейдите [к отключению образцов JavaScript,](#disable-javascript-samples) если вы хотите скрыть подробную схему пламени запросов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79115-237">Navigate to [Disable JavaScript samples](#disable-javascript-samples) if you want to hide the detailed flame chart of JavaScript requests.</span></span>  <span data-ttu-id="79115-238">Если образцы JS отключены, отображаются только события высокого уровня, такие как и из `Event: choose` `Function Call` `str` предыдущего рисунка.</span><span class="sxs-lookup"><span data-stu-id="79115-238">When JS samples are disabled, only high-level events such as `Event: choose` and `Function Call` from the previous figure `str` displayed.</span></span>  

### <a name="view-activities-in-a-table"></a><span data-ttu-id="79115-239">Просмотр действий в таблице</span><span class="sxs-lookup"><span data-stu-id="79115-239">View activities in a table</span></span>  

<span data-ttu-id="79115-240">После записи страницы не нужно полагаться только на основной **раздел** для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="79115-240">After recording a page, you do not need to rely solely on the **Main** section to analyze activities.</span></span>  <span data-ttu-id="79115-241">DevTools также предоставляет три табулярных представления для анализа действий.</span><span class="sxs-lookup"><span data-stu-id="79115-241">DevTools also provides three tabular views for analyzing activities.</span></span>  <span data-ttu-id="79115-242">Каждое представление дает различные точки зрения на действия:</span><span class="sxs-lookup"><span data-stu-id="79115-242">Each view gives you a different perspective on the activities:</span></span>  

*   <span data-ttu-id="79115-243">Если необходимо просмотреть корневые действия, которые вызывают большую часть работы, используйте панель [Дерева вызовов.](#the-call-tree-panel)</span><span class="sxs-lookup"><span data-stu-id="79115-243">When you want to view the root activities that cause the most work, use the [Call Tree](#the-call-tree-panel) panel.</span></span>  
*   <span data-ttu-id="79115-244">Если необходимо просмотреть действия, на которые было потрачено больше всего времени, используйте [панель Bottom-Up.](#the-bottom-up-panel)</span><span class="sxs-lookup"><span data-stu-id="79115-244">When you want to view the activities where the most time was directly spent, use the [Bottom-Up](#the-bottom-up-panel) panel.</span></span>  
*   <span data-ttu-id="79115-245">Если необходимо просмотреть действия в порядке, в котором они произошли во время записи, используйте панель [журнала событий.](#the-event-log-panel)</span><span class="sxs-lookup"><span data-stu-id="79115-245">When you want to view the activities in the order in which they occurred during the recording, use the [Event Log](#the-event-log-panel) panel.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="79115-246">В следующих трех разделах все ссылаются на одно и то же демо.</span><span class="sxs-lookup"><span data-stu-id="79115-246">The next three sections all refer to the same demo.</span></span>  <span data-ttu-id="79115-247">Запустите демонстрацию самостоятельно [в демо-версии вкладок Activity.][ActivityTabsDemo]</span><span class="sxs-lookup"><span data-stu-id="79115-247">Run the demo yourself at [Activity Tabs Demo][ActivityTabsDemo].</span></span>  

#### <a name="root-activities"></a><span data-ttu-id="79115-248">Корневые действия</span><span class="sxs-lookup"><span data-stu-id="79115-248">Root activities</span></span>  

<span data-ttu-id="79115-249">Вот объяснение концепции \*\*\*\* корневых действий, которая упоминается в панели **Дерево** вызовов, панели **Нижней** части и **панели журнала** событий.</span><span class="sxs-lookup"><span data-stu-id="79115-249">Here is an explanation of the **root activities** concept that is mentioned in the **Call Tree** panel, **Bottom-Up** panel, and **Event Log** panel.</span></span>  

<span data-ttu-id="79115-250">Корневые действия — это те действия, которые вызывают работу браузера.</span><span class="sxs-lookup"><span data-stu-id="79115-250">Root activities are those which cause the browser to do some work.</span></span>  <span data-ttu-id="79115-251">Например, при выборе веб-страницы браузер выполняет действие в `Event` качестве корневого действия.</span><span class="sxs-lookup"><span data-stu-id="79115-251">For example, when you choose a webpage, the browser runs an `Event` activity as the root activity.</span></span>  <span data-ttu-id="79115-252">Это `Event` может привести к запуску обработера и так далее.</span><span class="sxs-lookup"><span data-stu-id="79115-252">That `Event` may cause a handler to run, and so on.</span></span>  

<span data-ttu-id="79115-253">В диаграмме пламени раздела **Main** корневые действия находятся в верхней части диаграммы.</span><span class="sxs-lookup"><span data-stu-id="79115-253">In the flame chart of the **Main** section, root activities are at the top of the chart.</span></span>  <span data-ttu-id="79115-254">В **панелях Дерево вызовов** и **журнал событий** корневые действия являются элементами верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="79115-254">In the **Call Tree** and **Event Log** panels, root activities are the top-level items.</span></span>  

<span data-ttu-id="79115-255">Перейдите к [панели Дерева вызовов](#the-call-tree-panel) для примера корневых действий.</span><span class="sxs-lookup"><span data-stu-id="79115-255">Navigate to the [Call Tree](#the-call-tree-panel) panel for an example of root activities.</span></span>  

#### <a name="the-call-tree-panel"></a><span data-ttu-id="79115-256">Панель дерева вызовов</span><span class="sxs-lookup"><span data-stu-id="79115-256">The Call Tree panel</span></span>  

<span data-ttu-id="79115-257">Используйте панель **Дерево вызовов,** чтобы просмотреть, [какие корневые действия](#root-activities) вызывают большую часть работы.</span><span class="sxs-lookup"><span data-stu-id="79115-257">Use the **Call Tree** panel to view which [root activities](#root-activities) cause the most work.</span></span>  

<span data-ttu-id="79115-258">Панель **Дерева вызовов** отображает действия только во время выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="79115-258">The **Call Tree** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="79115-259">Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.</span><span class="sxs-lookup"><span data-stu-id="79115-259">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Панель дерева вызовов" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   <span data-ttu-id="79115-261">Панель **дерева вызовов**</span><span class="sxs-lookup"><span data-stu-id="79115-261">The **Call Tree** panel</span></span>  
:::image-end:::  

<span data-ttu-id="79115-262">На предыдущем рисунке верхний уровень элементов в столбце **Activity,** например корневых действий и `Evaluate Script` `Parse HTML` корневых.</span><span class="sxs-lookup"><span data-stu-id="79115-262">In the previous figure, the top-level of items in the **Activity** column, such as `Evaluate Script` and `Parse HTML` are root activities.</span></span>  <span data-ttu-id="79115-263">Вложение представляет собой стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="79115-263">The nesting represents the call stack.</span></span>  <span data-ttu-id="79115-264">Например, на предыдущем рисунке, который `Parse HTML` вызвал `Evaluate Script` и `Compile Script` `(anonymous)` .</span><span class="sxs-lookup"><span data-stu-id="79115-264">For example, in the previous figure, `Parse HTML` which caused `Evaluate Script` which caused `Compile Script` and `(anonymous)`.</span></span>  

<span data-ttu-id="79115-265">**Self Time** представляет время, непосредственно затраченное в этом действии.</span><span class="sxs-lookup"><span data-stu-id="79115-265">**Self Time** represents the time directly spent in that activity.</span></span>  <span data-ttu-id="79115-266">**Общее время** представляет время, затраченное в этом действии или на любое из детей.</span><span class="sxs-lookup"><span data-stu-id="79115-266">**Total Time** represents the time spent in that activity or any of the children.</span></span>  

<span data-ttu-id="79115-267">Для **сортировки**таблицы \*\*\*\* в этом столбце выберите "Время самостоятельно", \*\*\*\*"Общее время" или "Действие".</span><span class="sxs-lookup"><span data-stu-id="79115-267">Choose **Self Time**, **Total Time**, or **Activity** to sort the table by that column.</span></span>  

<span data-ttu-id="79115-268">Используйте **текстовое** поле Filter для фильтрации событий по имени действия.</span><span class="sxs-lookup"><span data-stu-id="79115-268">Use the **Filter** text box to filter events by activity name.</span></span>  

<span data-ttu-id="79115-269">По умолчанию **меню группировки** настроено на **No Grouping**.</span><span class="sxs-lookup"><span data-stu-id="79115-269">By default the **Grouping** menu is set to **No Grouping**.</span></span>  <span data-ttu-id="79115-270">Используйте меню **группировки** для сортировки таблицы действий на основе различных критериев.</span><span class="sxs-lookup"><span data-stu-id="79115-270">Use the **Grouping** menu to sort the activity table based on various criteria.</span></span>  

<span data-ttu-id="79115-271">Выберите **Показать самый тяжелый** стек \. Показать самый тяжелый стек \) чтобы показать другую таблицу ![ ](../media/show-heaviest-stack-icon.msft.png) справа от **таблицы Activity.**</span><span class="sxs-lookup"><span data-stu-id="79115-271">Choose **Show Heaviest Stack** \(![Show Heaviest Stack](../media/show-heaviest-stack-icon.msft.png)\) to reveal another table to the right of the **Activity** table.</span></span>  <span data-ttu-id="79115-272">Выберите действие для заполнения самой **тяжелой таблицы стеков.**</span><span class="sxs-lookup"><span data-stu-id="79115-272">Choose an activity to populate the **Heaviest Stack** table.</span></span>  <span data-ttu-id="79115-273">Самая **тяжелая таблица стеков** отображает, на которое дети выбранного действия убирали больше всего времени.</span><span class="sxs-lookup"><span data-stu-id="79115-273">The **Heaviest Stack** table displays which children of the selected activity took the longest time to run.</span></span>  

#### <a name="the-bottom-up-panel"></a><span data-ttu-id="79115-274">Панель Bottom-Up</span><span class="sxs-lookup"><span data-stu-id="79115-274">The Bottom-Up panel</span></span>  

<span data-ttu-id="79115-275">Используйте панель **снизу вверх,** чтобы просмотреть, какие действия непосредственно заняли больше всего времени в совокупности.</span><span class="sxs-lookup"><span data-stu-id="79115-275">Use the **Bottom-Up** panel to view which activities directly took up the most time in aggregate.</span></span>  

<span data-ttu-id="79115-276">Панель **Bottom-Up** отображает действия только во время выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="79115-276">The **Bottom-Up** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="79115-277">Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.</span><span class="sxs-lookup"><span data-stu-id="79115-277">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="Панель Bottom-Up" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   <span data-ttu-id="79115-279">Панель **снизу вверх**</span><span class="sxs-lookup"><span data-stu-id="79115-279">The **Bottom-Up** panel</span></span>  
:::image-end:::  

<span data-ttu-id="79115-280">В **диаграмме пламени** основного раздела предыдущего рисунка перейдите к этому практически все время, затраченное на `Parse HTML` запуск.</span><span class="sxs-lookup"><span data-stu-id="79115-280">In the **Main** section flame chart of the previous figure, navigate to that almost practically all of the time was spent running `Parse HTML`.</span></span>  <span data-ttu-id="79115-281">Верхнее действие в **панели Bottom-Up** предыдущего рисунка `Parse HTML` .</span><span class="sxs-lookup"><span data-stu-id="79115-281">The top activity in the **Bottom-Up** panel of the previous figure is `Parse HTML`.</span></span>  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  <span data-ttu-id="79115-282">Перейдите к **панели Bottom-Up,** следующая самая дорогая активность `Layout` .</span><span class="sxs-lookup"><span data-stu-id="79115-282">Navigate to the **Bottom-Up** panel, the next most expensive activity is `Layout`.</span></span>  

<span data-ttu-id="79115-283">Столбец **Self Time** представляет совокупное время, затраченное непосредственно в этом действии, во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="79115-283">The **Self Time** column represents the aggregated time spent directly in that activity, across all of the occurrences.</span></span>  

<span data-ttu-id="79115-284">Столбец **Общее** время представляет агрегированное время, затраченное в этом действии или любом из детей.</span><span class="sxs-lookup"><span data-stu-id="79115-284">The **Total Time** column represents aggregated time spent in that activity or any of the children.</span></span>  

#### <a name="the-event-log-panel"></a><span data-ttu-id="79115-285">Панель журнала событий</span><span class="sxs-lookup"><span data-stu-id="79115-285">The Event Log panel</span></span>  

<span data-ttu-id="79115-286">Панель **журнала событий** используется для просмотра действий в порядке, в котором они произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-286">Use the **Event Log** panel to view activities in the order in which they occurred during the recording.</span></span>  

<span data-ttu-id="79115-287">Панель **журнала событий** отображает действия только во время выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="79115-287">The **Event Log** panel only displays activities during the selected portion of the recording.</span></span>  <span data-ttu-id="79115-288">Перейдите [к выбору части записи,](#select-a-portion-of-a-recording) чтобы узнать, как выбрать части.</span><span class="sxs-lookup"><span data-stu-id="79115-288">Navigate to [Select a portion of a recording](#select-a-portion-of-a-recording) to learn how to select portions.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Панель журнала событий" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   <span data-ttu-id="79115-290">Панель **журнала событий**</span><span class="sxs-lookup"><span data-stu-id="79115-290">The **Event Log** panel</span></span>  
:::image-end:::  

<span data-ttu-id="79115-291">Столбец **Время** начала представляет точку, с которой началось это действие, относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="79115-291">The **Start Time** column represents the point at which that activity started, relative to the start of the recording.</span></span>  <span data-ttu-id="79115-292">Например, время начала работы выбранного элемента на предыдущем рисунке означает, что действие началось `175.7 ms` с 175,7 мс после начала записи.</span><span class="sxs-lookup"><span data-stu-id="79115-292">For example, the start time of `175.7 ms` for the selected item in the previous figure means that activity started 175.7 ms after the recording started.</span></span>  

<span data-ttu-id="79115-293">Столбец **Self Time** представляет время, затраченное непосредственно в этом действии.</span><span class="sxs-lookup"><span data-stu-id="79115-293">The **Self Time** column represents the time spent directly in that activity.</span></span>  

<span data-ttu-id="79115-294">Столбцы **Total Time** представляют время, затраченное непосредственно в этом действии или в любом из детей.</span><span class="sxs-lookup"><span data-stu-id="79115-294">The **Total Time** columns represents time spent directly in that activity or in any of the children.</span></span>  

<span data-ttu-id="79115-295">Выберите **время начала,** **время**самостоятельно или **общее** время сортировки таблицы в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="79115-295">Choose **Start Time**, **Self Time**, or **Total Time** to sort the table by that column.</span></span>

<span data-ttu-id="79115-296">Используйте **текстовое поле Filter** для фильтрации действий по имени.</span><span class="sxs-lookup"><span data-stu-id="79115-296">Use the **Filter** text box to filter activities by name.</span></span>  

<span data-ttu-id="79115-297">Используйте меню **Duration,** чтобы отфильтровать все действия, которые заняли менее 1 мс или 15 мс.</span><span class="sxs-lookup"><span data-stu-id="79115-297">Use the **Duration** menu to filter out any activities that took less than 1 ms or 15 ms.</span></span>  <span data-ttu-id="79115-298">По умолчанию **меню "Продолжительность"** заказано **всем,** то есть все действия показаны.</span><span class="sxs-lookup"><span data-stu-id="79115-298">By default the **Duration** menu is set to **All**, meaning all activities are shown.</span></span>  

<span data-ttu-id="79115-299">Отключить **контрольные ящики Loading,** **Scripting,** **Rendering**или **Painting,** чтобы отфильтровать все действия из этих категорий.</span><span class="sxs-lookup"><span data-stu-id="79115-299">Disable the **Loading**, **Scripting**, **Rendering**, or **Painting** checkboxes to filter out all activities from those categories.</span></span>  

### <a name="view-gpu-activity"></a><span data-ttu-id="79115-300">Просмотр действий GPU</span><span class="sxs-lookup"><span data-stu-id="79115-300">View GPU activity</span></span>  

<span data-ttu-id="79115-301">Просмотр действий GPU в разделе **GPU.**</span><span class="sxs-lookup"><span data-stu-id="79115-301">View GPU activity in the **GPU** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Раздел GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   <span data-ttu-id="79115-303">Раздел **GPU**</span><span class="sxs-lookup"><span data-stu-id="79115-303">The **GPU** section</span></span>  
:::image-end:::  

### <a name="view-raster-activity"></a><span data-ttu-id="79115-304">Просмотр действия raster</span><span class="sxs-lookup"><span data-stu-id="79115-304">View raster activity</span></span>  

<span data-ttu-id="79115-305">Просмотр действий raster в разделе **Raster.**</span><span class="sxs-lookup"><span data-stu-id="79115-305">View raster activity in the **Raster** section.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Раздел Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   <span data-ttu-id="79115-307">Раздел **Raster**</span><span class="sxs-lookup"><span data-stu-id="79115-307">The **Raster** section</span></span>  
:::image-end:::  

### <a name="view-interactions"></a><span data-ttu-id="79115-308">Просмотр взаимодействий</span><span class="sxs-lookup"><span data-stu-id="79115-308">View interactions</span></span>  

<span data-ttu-id="79115-309">Раздел **Взаимодействия используется** для поиска и анализа взаимодействий пользователей, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-309">Use the **Interactions** section to find and analyze user interactions that happened during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Раздел Взаимодействия" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   <span data-ttu-id="79115-311">Раздел **Взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="79115-311">The **Interactions** section</span></span>  
:::image-end:::  

<span data-ttu-id="79115-312">Красная строка в нижней части взаимодействия представляет время, затраченное на ожидание основного потока.</span><span class="sxs-lookup"><span data-stu-id="79115-312">A red line at the bottom of an interaction represents time spent waiting for the main thread.</span></span>  

<span data-ttu-id="79115-313">Выберите взаимодействие, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-313">Choose an interaction to view more information about it in the **Summary** panel.</span></span>  

### <a name="analyze-frames-per-second-fps"></a><span data-ttu-id="79115-314">Анализ кадров в секунду (FPS)</span><span class="sxs-lookup"><span data-stu-id="79115-314">Analyze frames per second (FPS)</span></span>  

<span data-ttu-id="79115-315">DevTools предоставляет множество способов анализа кадров в секунду:</span><span class="sxs-lookup"><span data-stu-id="79115-315">DevTools provides numerous ways to analyze frames per second:</span></span>  

*   <span data-ttu-id="79115-316">Используйте [диаграмму FPS,](#the-fps-chart) чтобы получить обзор FPS за время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-316">Use [the FPS chart](#the-fps-chart) to get an overview of FPS over the duration of the recording.</span></span>  
*   <span data-ttu-id="79115-317">Используйте [раздел Frames,](#the-frames-section) чтобы просмотреть, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="79115-317">Use [the Frames section](#the-frames-section) to view how long a particular frame took.</span></span>  
*   <span data-ttu-id="79115-318">Используйте **счетчик FPS для** оценки FPS в режиме реального времени при запуске страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-318">Use the **FPS meter** for a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="79115-319">Перейдите [к просмотру кадров в секунду в режиме реального времени с помощью счетчика FPS.](#view-frames-per-second-in-realtime-with-the-fps-meter)</span><span class="sxs-lookup"><span data-stu-id="79115-319">Navigate to [View frames per second in realtime with the FPS meter](#view-frames-per-second-in-realtime-with-the-fps-meter).</span></span>  
    
#### <a name="the-fps-chart"></a><span data-ttu-id="79115-320">Диаграмма FPS</span><span class="sxs-lookup"><span data-stu-id="79115-320">The FPS chart</span></span>  

<span data-ttu-id="79115-321">На **диаграмме FPS** представлен обзор частоты кадров в течение записи.</span><span class="sxs-lookup"><span data-stu-id="79115-321">The **FPS** chart provides an overview of the frame rate across the duration of a recording.</span></span>  <span data-ttu-id="79115-322">Как правило, чем выше зеленая планка, тем выше частота кадров.</span><span class="sxs-lookup"><span data-stu-id="79115-322">In general, the higher the green bar, the better the frame rate.</span></span>  

<span data-ttu-id="79115-323">Красная планка над **диаграммой FPS** — это предупреждение о том, что частота кадров снизилась настолько низко, что, вероятно, навредила опыту пользователя.</span><span class="sxs-lookup"><span data-stu-id="79115-323">A red bar above the **FPS** chart is a warning that the frame rate dropped so low that it probably harmed the user's experience.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   <span data-ttu-id="79115-325">Диаграмма **FPS**</span><span class="sxs-lookup"><span data-stu-id="79115-325">The **FPS** chart</span></span>  
:::image-end:::  

#### <a name="the-frames-section"></a><span data-ttu-id="79115-326">Раздел Кадры</span><span class="sxs-lookup"><span data-stu-id="79115-326">The Frames section</span></span>  

<span data-ttu-id="79115-327">В **разделе Frames** указывается, сколько времени занимает определенный кадр.</span><span class="sxs-lookup"><span data-stu-id="79115-327">The **Frames** section tells you exactly how long a particular frame took.</span></span>  

<span data-ttu-id="79115-328">Наведите курсор на кадр, чтобы просмотреть набор инструментов с дополнительными сведениями о нем.</span><span class="sxs-lookup"><span data-stu-id="79115-328">Hover on a frame to view a tooltip with more information about it.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Наведите курсор на кадр" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   <span data-ttu-id="79115-330">Наведите курсор на кадр</span><span class="sxs-lookup"><span data-stu-id="79115-330">Hover on a frame</span></span>  
:::image-end:::  

<span data-ttu-id="79115-331">Выберите кадр, чтобы просмотреть дополнительные сведения о кадре в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-331">Choose a frame to view more information about the frame in the **Summary** panel.</span></span>  <span data-ttu-id="79115-332">DevTools описывает выбранный кадр синим цветом.</span><span class="sxs-lookup"><span data-stu-id="79115-332">DevTools outlines the selected frame in blue.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Просмотр кадра в панели Сводка" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   <span data-ttu-id="79115-334">Просмотр кадра в панели **Сводка**</span><span class="sxs-lookup"><span data-stu-id="79115-334">View a frame in the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-network-requests"></a><span data-ttu-id="79115-335">Просмотр сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="79115-335">View network requests</span></span>  

<span data-ttu-id="79115-336">**Расширь раздел Network,** чтобы просмотреть водопад сетевых запросов, которые произошли во время записи.</span><span class="sxs-lookup"><span data-stu-id="79115-336">Expand the **Network** section to view a waterfall of network requests that occurred during the recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Раздел Network" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   <span data-ttu-id="79115-338">Раздел **Network**</span><span class="sxs-lookup"><span data-stu-id="79115-338">The **Network** section</span></span>  
:::image-end:::  

<span data-ttu-id="79115-339">Запросы закодироваться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="79115-339">Requests are color-coded as follows:</span></span>  

*   <span data-ttu-id="79115-340">HTML: Синий</span><span class="sxs-lookup"><span data-stu-id="79115-340">HTML: Blue</span></span>  
*   <span data-ttu-id="79115-341">CSS: Purple</span><span class="sxs-lookup"><span data-stu-id="79115-341">CSS: Purple</span></span>  
*   <span data-ttu-id="79115-342">JS: Желтый</span><span class="sxs-lookup"><span data-stu-id="79115-342">JS: Yellow</span></span>  
*   <span data-ttu-id="79115-343">Изображения: Зеленый</span><span class="sxs-lookup"><span data-stu-id="79115-343">Images: Green</span></span>  
    
<span data-ttu-id="79115-344">Выберите запрос, чтобы просмотреть дополнительные сведения о нем в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-344">Choose a request to view more information about it in the **Summary** panel.</span></span>  <span data-ttu-id="79115-345">Например, на предыдущем рисунке панель **Сводка** отображает дополнительные сведения о синем запросе, выбранном в разделе **Сеть.**</span><span class="sxs-lookup"><span data-stu-id="79115-345">For example, in the previous figure, the **Summary** panel is displaying more information about the blue request that is selected in the **Network** section.</span></span>  

<span data-ttu-id="79115-346">Темно-синий квадрат в верхнем левом конце запроса означает, что это запрос с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="79115-346">A darker-blue square in the top-left of a request means it is a higher-priority request.</span></span>  <span data-ttu-id="79115-347">Квадрат светло-синего цвета означает более низкий приоритет.</span><span class="sxs-lookup"><span data-stu-id="79115-347">A lighter-blue square means lower-priority.</span></span>  <span data-ttu-id="79115-348">Например, на предыдущем рисунке синий выбранный запрос имеет более высокий приоритет, а зеленый — более низкий.</span><span class="sxs-lookup"><span data-stu-id="79115-348">For example, in the previous figure, the blue, selected request is higher-priority, and the green one below it is lower-priority.</span></span>  

<span data-ttu-id="79115-349">В 1-м из следующих рисунков запрос представлен строкой слева, баром в центре с темной частью и светлой частью, а также строкой `www.bing.com` справа.</span><span class="sxs-lookup"><span data-stu-id="79115-349">In the 1st of the following figures, the request for `www.bing.com` is represented by a line on the left, a bar in the middle with a dark portion and a light portion, and a line on the right.</span></span>  <span data-ttu-id="79115-350">Во 2-м из следующих рисунков показано соответствующее представление того же запроса в панели **синхронизации** средства **Network.**</span><span class="sxs-lookup"><span data-stu-id="79115-350">In the 2nd of the following figures shows the corresponding representation of the same request in the **Timing** panel of the **Network** tool.</span></span>  <span data-ttu-id="79115-351">Ниже представлена карта этих двух представлений друг с другом:</span><span class="sxs-lookup"><span data-stu-id="79115-351">Here is how these two representations map to each other:</span></span>

*   <span data-ttu-id="79115-352">Левая строка — это все в соответствии с `Connection Start` группой событий, включительно.</span><span class="sxs-lookup"><span data-stu-id="79115-352">The left line is everything up to the `Connection Start` group of events, inclusive.</span></span>  <span data-ttu-id="79115-353">Другими словами, это все, прежде чем `Request Sent` , эксклюзивный.</span><span class="sxs-lookup"><span data-stu-id="79115-353">In other words, it is everything before `Request Sent`, exclusive.</span></span>  
*   <span data-ttu-id="79115-354">Светлая часть панели и `Request Sent` `Waiting (TTFB)` .</span><span class="sxs-lookup"><span data-stu-id="79115-354">The light portion of the bar is `Request Sent` and `Waiting (TTFB)`.</span></span>  
*   <span data-ttu-id="79115-355">Темная часть панели `Content Download` .</span><span class="sxs-lookup"><span data-stu-id="79115-355">The dark portion of the bar is `Content Download`.</span></span>  
*   <span data-ttu-id="79115-356">Правая линия — это, по сути, время, затраченное на ожидание основного потока.</span><span class="sxs-lookup"><span data-stu-id="79115-356">The right line is essentially time spent waiting for the main thread.</span></span>  <span data-ttu-id="79115-357">Это не представлено в панели **Timing.**</span><span class="sxs-lookup"><span data-stu-id="79115-357">This is not represented in the **Timing** panel.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Представление строки-панели www.bing.com запроса" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         <span data-ttu-id="79115-359">Представление строки-панели `www.bing.com` запроса</span><span class="sxs-lookup"><span data-stu-id="79115-359">The line-bar representation of the `www.bing.com` request</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="Средство Network" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         <span data-ttu-id="79115-361">Средство **Network**</span><span class="sxs-lookup"><span data-stu-id="79115-361">The **Network** tool</span></span>  
<span data-ttu-id="79115-362">:::image-end:::</span><span class="sxs-lookup"><span data-stu-id="79115-362">:     ::image-end:::</span></span>  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a><span data-ttu-id="79115-363">Просмотр метрик памяти</span><span class="sxs-lookup"><span data-stu-id="79115-363">View memory metrics</span></span>  

<span data-ttu-id="79115-364">Включив контрольный ящик **Памяти,** чтобы просмотреть показатели памяти из последней записи.</span><span class="sxs-lookup"><span data-stu-id="79115-364">Turn on the **Memory** checkbox to view memory metrics from the last recording.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="Контрольный ящик памяти" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   <span data-ttu-id="79115-366">Контрольный ящик **памяти**</span><span class="sxs-lookup"><span data-stu-id="79115-366">The **Memory** checkbox</span></span>  
:::image-end:::  

<span data-ttu-id="79115-367">В DevTools отображается новая диаграмма **памяти** над **панелью Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-367">DevTools displays a new **Memory** chart, above the **Summary** panel.</span></span>  <span data-ttu-id="79115-368">Существует также новая диаграмма ниже **диаграммы NET,** называемой **HEAP**.</span><span class="sxs-lookup"><span data-stu-id="79115-368">There is also a new chart below the **NET** chart, called **HEAP**.</span></span>  <span data-ttu-id="79115-369">Диаграмма **HEAP** содержит те же сведения, что и строка **JS Heap** в **диаграмме Памяти.**</span><span class="sxs-lookup"><span data-stu-id="79115-369">The **HEAP** chart provides the same information as the **JS Heap** line in the **Memory** chart.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Метрик памяти" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   <span data-ttu-id="79115-371">Метрик памяти</span><span class="sxs-lookup"><span data-stu-id="79115-371">Memory metrics</span></span>  
:::image-end:::  

<span data-ttu-id="79115-372">Цветные строки на карте диаграммы к цветным почтовым ящикам над диаграммой.</span><span class="sxs-lookup"><span data-stu-id="79115-372">The colored lines on the chart map to the colored checkboxes above the chart.</span></span>  
<span data-ttu-id="79115-373">Отключить контрольный ящик, чтобы скрыть эту категорию из диаграммы.</span><span class="sxs-lookup"><span data-stu-id="79115-373">Disable a checkbox to hide that category from the chart.</span></span>  

<span data-ttu-id="79115-374">На диаграмме отображается только область выбранной записи.</span><span class="sxs-lookup"><span data-stu-id="79115-374">The chart only displays the region of the recording that is currently selected.</span></span>  <span data-ttu-id="79115-375">Например, на предыдущем рисунке на диаграмме **Памяти** отображается только использование памяти от отметки 400 мс до отметки 1750 мс.</span><span class="sxs-lookup"><span data-stu-id="79115-375">For example, in the previous figure, the **Memory** chart is only showing memory usage from around the 400 ms mark to the 1750 ms mark.</span></span>  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a><span data-ttu-id="79115-376">Просмотр продолжительности части записи</span><span class="sxs-lookup"><span data-stu-id="79115-376">View the duration of a portion of a recording</span></span>  

<span data-ttu-id="79115-377">При анализе таких разделов, как **Network** или **Main,** иногда требуется более точная оценка того, сколько времени заняли определенные события.</span><span class="sxs-lookup"><span data-stu-id="79115-377">When analyzing a section like **Network** or **Main**, sometimes you need a more precise estimate of how long certain events took.</span></span>  <span data-ttu-id="79115-378">`Shift`Удерживайте, выберите и удерживайте и перетащите влево или вправо, чтобы выбрать часть записи.</span><span class="sxs-lookup"><span data-stu-id="79115-378">Hold `Shift`, choose and hold, and drag left or right to select a portion of the recording.</span></span>  <span data-ttu-id="79115-379">В нижней части выбора DevTools показывает, сколько времени занимает эта часть.</span><span class="sxs-lookup"><span data-stu-id="79115-379">At the bottom of your selection, DevTools shows how long that portion took.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Просмотр продолжительности части записи" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   <span data-ttu-id="79115-381">Просмотр продолжительности части записи</span><span class="sxs-lookup"><span data-stu-id="79115-381">View the duration of a portion of a recording</span></span>  
:::image-end:::  

### <a name="view-a-screenshot"></a><span data-ttu-id="79115-382">Просмотр экрана</span><span class="sxs-lookup"><span data-stu-id="79115-382">View a screenshot</span></span>  

<span data-ttu-id="79115-383">Перейдите [к захвату скриншотов во время записи,](#capture-screenshots-while-recording) чтобы узнать, как включить скриншоты.</span><span class="sxs-lookup"><span data-stu-id="79115-383">Navigate to [Capture screenshots while recording](#capture-screenshots-while-recording) to learn how to turn on screenshots.</span></span>  

<span data-ttu-id="79115-384">Наведите курсор на **обзор,** чтобы просмотреть снимок экрана, как выглядела страница в этот момент записи.</span><span class="sxs-lookup"><span data-stu-id="79115-384">Hover on the **Overview** to view a screenshot of how the page looked during that moment of the recording.</span></span>  <span data-ttu-id="79115-385">Обзор **—** это раздел, содержащий **диаграммы CPU,** **FPS**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="79115-385">The **Overview** is the section that contains the **CPU**, **FPS**, and **NET** charts.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Просмотр экрана" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   <span data-ttu-id="79115-387">Просмотр экрана</span><span class="sxs-lookup"><span data-stu-id="79115-387">View a screenshot</span></span>  
:::image-end:::  

<span data-ttu-id="79115-388">Вы также можете просмотреть скриншоты, выбрав кадр в разделе **Frames.**</span><span class="sxs-lookup"><span data-stu-id="79115-388">You may also view screenshots by choosing a frame in the **Frames** section.</span></span>  <span data-ttu-id="79115-389">DevTools отображает небольшую версию экрана в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="79115-389">DevTools displays a small version of the screenshot in the **Summary** panel.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Просмотр экрана в панели Сводка" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   <span data-ttu-id="79115-391">Просмотр экрана в панели **Сводка**</span><span class="sxs-lookup"><span data-stu-id="79115-391">View a screenshot in the **Summary** panel</span></span>  
:::image-end:::  

<span data-ttu-id="79115-392">Выберите эскиз на панели **Сводка,** чтобы увеличить масштаб экрана.</span><span class="sxs-lookup"><span data-stu-id="79115-392">Choose the thumbnail in the **Summary** panel to zoom in on the screenshot.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Масштабирование экрана с панели Сводка" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   <span data-ttu-id="79115-394">Масштабирование экрана с панели **Сводка**</span><span class="sxs-lookup"><span data-stu-id="79115-394">Zoom into a screenshot from the **Summary** panel</span></span>  
:::image-end:::  

### <a name="view-layers-information"></a><span data-ttu-id="79115-395">Просмотр сведений о слоях</span><span class="sxs-lookup"><span data-stu-id="79115-395">View layers information</span></span>  

<span data-ttu-id="79115-396">Чтобы просмотреть расширенные слои, сведения о кадре:</span><span class="sxs-lookup"><span data-stu-id="79115-396">To view advanced layers information about a frame:</span></span>  

1.  <span data-ttu-id="79115-397">[Включи расширенный инструментарий краски.](#turn-on-advanced-paint-instrumentation)</span><span class="sxs-lookup"><span data-stu-id="79115-397">[Turn on advanced paint instrumentation](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="79115-398">Выберите кадр в разделе **Frames.**</span><span class="sxs-lookup"><span data-stu-id="79115-398">Choose a frame in the **Frames** section.</span></span>  <span data-ttu-id="79115-399">DevTools отображает сведения о слоях в новой панели **Layers** рядом с панелью **Журнала событий.**</span><span class="sxs-lookup"><span data-stu-id="79115-399">DevTools displays information about the layers in the new **Layers** panel, next to the **Event Log** panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Области Слоев" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       <span data-ttu-id="79115-401">Области **Слоев**</span><span class="sxs-lookup"><span data-stu-id="79115-401">The **Layers** pane</span></span>  
    :::image-end:::  
    
<span data-ttu-id="79115-402">Наведите курсор на слой, чтобы выделить его на схеме.</span><span class="sxs-lookup"><span data-stu-id="79115-402">Hover on a layer to highlight it in the diagram.</span></span>  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Выделение слоя" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   <span data-ttu-id="79115-404">Выделение слоя</span><span class="sxs-lookup"><span data-stu-id="79115-404">Highlight a layer</span></span>  
:::image-end:::  

<span data-ttu-id="79115-405">Чтобы переместить схему:</span><span class="sxs-lookup"><span data-stu-id="79115-405">To move the diagram:</span></span>  

*   <span data-ttu-id="79115-406">Выберите **режим** Pan \( Pan Mode \) для ![ перемещения по осям X и ](../media/pan-mode-icon.msft.png) Y.</span><span class="sxs-lookup"><span data-stu-id="79115-406">Choose **Pan Mode** \(![Pan Mode](../media/pan-mode-icon.msft.png)\) to move along the X and Y axes.</span></span>  
*   <span data-ttu-id="79115-407">Выберите **режим вращать** \( ![ Вращать режим \) для ](../media/rotate-mode-icon.msft.png) поворота вдоль оси Z.</span><span class="sxs-lookup"><span data-stu-id="79115-407">Choose **Rotate Mode** \(![Rotate Mode](../media/rotate-mode-icon.msft.png)\) to rotate along the Z axis.</span></span>  
*   <span data-ttu-id="79115-408">Выберите **сброс преобразования** \. Сброс преобразования \) для ![ ](../media/reset-transform-icon.msft.png) сброса схемы в исходное положение.</span><span class="sxs-lookup"><span data-stu-id="79115-408">Choose **Reset Transform** \(![Reset Transform](../media/reset-transform-icon.msft.png)\) to reset the diagram to the original position.</span></span>  
    
### <a name="view-paint-profiler"></a><span data-ttu-id="79115-409">Просмотр профиля краски</span><span class="sxs-lookup"><span data-stu-id="79115-409">View paint profiler</span></span>  

<span data-ttu-id="79115-410">Чтобы просмотреть расширенные сведения о событии краски:</span><span class="sxs-lookup"><span data-stu-id="79115-410">To view advanced information about a paint event:</span></span>  

1.  <span data-ttu-id="79115-411">[Включаем](#turn-on-advanced-paint-instrumentation).</span><span class="sxs-lookup"><span data-stu-id="79115-411">[Turn on](#turn-on-advanced-paint-instrumentation).</span></span>  
1.  <span data-ttu-id="79115-412">Выберите событие **Paint** в **разделе Main.**</span><span class="sxs-lookup"><span data-stu-id="79115-412">Choose a **Paint** event in the **Main** section.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Панель профилера Paint" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       <span data-ttu-id="79115-414">Панель **профилера Paint**</span><span class="sxs-lookup"><span data-stu-id="79115-414">The **Paint Profiler** panel</span></span>  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a><span data-ttu-id="79115-415">Анализ производительности отрисовки с помощью средства визуализации</span><span class="sxs-lookup"><span data-stu-id="79115-415">Analyze rendering performance with the Rendering tool</span></span>  

<span data-ttu-id="79115-416">Используйте функции панели **rendering** для визуализации производительности визуализации страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-416">Use the features of the **Rendering** panel to help visualize the rendering performance of your page.</span></span>  

<span data-ttu-id="79115-417">Чтобы открыть **средство отрисовки:**</span><span class="sxs-lookup"><span data-stu-id="79115-417">To open the **Rendering** tool:</span></span>  

1.  <span data-ttu-id="79115-418">[Откройте командное меню.][DevToolsCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="79115-418">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="79115-419">Начните `Rendering` вводить и выберите `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="79115-419">Start typing `Rendering` and select `Show Rendering`.</span></span>  <span data-ttu-id="79115-420">DevTools отображает средство **визуализации** в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="79115-420">DevTools displays the **Rendering** tool at the bottom of your DevTools window.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="Средство отрисовки" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       <span data-ttu-id="79115-422">Средство **отрисовки**</span><span class="sxs-lookup"><span data-stu-id="79115-422">The **Rendering** tool</span></span>  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a><span data-ttu-id="79115-423">Просмотр кадров в секунду в режиме реального времени с помощью счетчика FPS</span><span class="sxs-lookup"><span data-stu-id="79115-423">View frames per second in realtime with the FPS meter</span></span>  

<span data-ttu-id="79115-424">Счетчик **FPS —** это наложение, которое отображается в правом верхнем углу представления.</span><span class="sxs-lookup"><span data-stu-id="79115-424">The **FPS meter** is an overlay that appears in the top-right corner of your viewport.</span></span>  <span data-ttu-id="79115-425">Он предоставляет оценку FPS в режиме реального времени по мере работы страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-425">It provides a realtime estimate of FPS as the page runs.</span></span>  <span data-ttu-id="79115-426">Чтобы открыть **счетчик FPS:**</span><span class="sxs-lookup"><span data-stu-id="79115-426">To open the **FPS meter**:</span></span>  

1.  <span data-ttu-id="79115-427">Откройте средство **отрисовки.**</span><span class="sxs-lookup"><span data-stu-id="79115-427">Open the **Rendering** tool.</span></span>  <span data-ttu-id="79115-428">[Анализ производительности визуализации с помощью средства визуализации.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="79115-428">[Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="79115-429">Включи **флажки счетчика FPS.**</span><span class="sxs-lookup"><span data-stu-id="79115-429">Turn on the **FPS Meter** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       <span data-ttu-id="79115-431">Счетчик **FPS**</span><span class="sxs-lookup"><span data-stu-id="79115-431">The **FPS meter**</span></span>  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a><span data-ttu-id="79115-432">Просмотр событий рисования в режиме реального времени с помощью мигания краски</span><span class="sxs-lookup"><span data-stu-id="79115-432">View painting events in realtime with Paint Flashing</span></span>  

<span data-ttu-id="79115-433">Чтобы получить представление всех событий краски на странице в режиме реального времени, используйте paint Flashing.</span><span class="sxs-lookup"><span data-stu-id="79115-433">Use Paint Flashing to get a realtime view of all paint events on the page.</span></span>  <span data-ttu-id="79115-434">Всякий раз, когда часть страницы перерисовывается, DevTools очертает этот раздел зеленым цветом.</span><span class="sxs-lookup"><span data-stu-id="79115-434">Whenever a part of the page gets re-painted, DevTools outlines that section in green.</span></span>  

<span data-ttu-id="79115-435">Чтобы включить мигание краски, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="79115-435">To turn on Paint Flashing, complete the following actions.</span></span>  

1.  <span data-ttu-id="79115-436">Откройте средство **отрисовки.**</span><span class="sxs-lookup"><span data-stu-id="79115-436">Open the **Rendering** tool.</span></span>  <span data-ttu-id="79115-437">Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="79115-437">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="79115-438">Включим **контрольный ящик "Мигать** краской".</span><span class="sxs-lookup"><span data-stu-id="79115-438">Turn on the **Paint Flashing** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Мигает краской" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **<span data-ttu-id="79115-440">Мигает краской</span><span class="sxs-lookup"><span data-stu-id="79115-440">Paint Flashing</span></span>**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a><span data-ttu-id="79115-441">Просмотр наложения слоев с границами слоев</span><span class="sxs-lookup"><span data-stu-id="79115-441">View an overlay of layers with Layer Borders</span></span>  

<span data-ttu-id="79115-442">Используйте **границы слоя,** чтобы просмотреть наложение границ слоев и плиток в верхней части страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-442">Use **Layer Borders** to view an overlay of layer borders and tiles on top of the page.</span></span>  

<span data-ttu-id="79115-443">Чтобы включить границы слоя, выполните следующие действия,</span><span class="sxs-lookup"><span data-stu-id="79115-443">To turn on Layer Borders, complete the following actions,</span></span>  

1.  <span data-ttu-id="79115-444">Откройте средство **отрисовки.**</span><span class="sxs-lookup"><span data-stu-id="79115-444">Open the **Rendering** tool.</span></span>  <span data-ttu-id="79115-445">Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="79115-445">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="79115-446">Включаем **почтовый ящик Layer Borders.**</span><span class="sxs-lookup"><span data-stu-id="79115-446">Turn on the **Layer Borders** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Границы слоя" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **<span data-ttu-id="79115-448">Границы слоя</span><span class="sxs-lookup"><span data-stu-id="79115-448">Layer Borders</span></span>**  
    :::image-end:::  
    
<span data-ttu-id="79115-449">Перейдите к комментариям [debug_colors.cc][ChromiumDebugColors] для объяснения цветового кодирования.</span><span class="sxs-lookup"><span data-stu-id="79115-449">Navigate to the comments in [debug_colors.cc][ChromiumDebugColors] for an explanation of the color-codings.</span></span>  

### <a name="find-scroll-performance-issues-in-realtime"></a><span data-ttu-id="79115-450">Поиск проблем с производительностью прокрутки в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="79115-450">Find scroll performance issues in realtime</span></span>  

<span data-ttu-id="79115-451">Используйте проблемы с производительностью прокрутки для определения элементов страницы, которые имеют слушателей событий, связанных с прокрутки, которые могут повредить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="79115-451">Use Scrolling Performance Issues to identify elements of the page that have event listeners related to scrolling that may harm the performance of the page.</span></span>  
<span data-ttu-id="79115-452">DevTools описывает потенциально проблемные элементы в teal.</span><span class="sxs-lookup"><span data-stu-id="79115-452">DevTools outlines the potentially-problematic elements in teal.</span></span>  

<span data-ttu-id="79115-453">Чтобы просмотреть проблемы с производительностью прокрутки, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="79115-453">To view scroll performance issues, complete the following actions.</span></span> 

1.  <span data-ttu-id="79115-454">Откройте средство **отрисовки.**</span><span class="sxs-lookup"><span data-stu-id="79115-454">Open the **Rendering** tool.</span></span>  <span data-ttu-id="79115-455">Перейдите [к анализу производительности отрисовки с помощью средства rendering.](#analyze-rendering-performance-with-the-rendering-tool)</span><span class="sxs-lookup"><span data-stu-id="79115-455">Navigate to [Analyze rendering performance with the Rendering tool](#analyze-rendering-performance-with-the-rendering-tool).</span></span>  
1.  <span data-ttu-id="79115-456">Включите **почтовый ящик "Проблемы с производительностью прокрутки".**</span><span class="sxs-lookup"><span data-stu-id="79115-456">Turn on the **Scrolling Performance Issues** checkbox.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Проблемы с прокруткой производительности указывают на то, что объекты с ограниченным представлением неслойного представления могут навредить производительности прокрутки" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       <span data-ttu-id="79115-458">**Проблемы с прокруткой** производительности указывают на то, что объекты с ограниченным представлением неслойного представления могут навредить производительности прокрутки</span><span class="sxs-lookup"><span data-stu-id="79115-458">**Scrolling Performance Issues** indicates that non-layer viewport-constrained objects may harm scroll performance</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="79115-459">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="79115-459">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Откройте командное меню — запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Начало работы с анализом производительности выполнения | Документы Майкрософт"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Демонстрация вкладок | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc — поиск кода"  

> [!NOTE]
> <span data-ttu-id="79115-465">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="79115-465">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="79115-466">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="79115-466">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="79115-468">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="79115-468">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
