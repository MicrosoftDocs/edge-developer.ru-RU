---
description: Узнайте, как оценить производительность выполнения в Microsoft Edge DevTools.
title: Начало работы с анализом производительности выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 439d6d4331550b7fc92bfc5fef4c3fc88df38872
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439614"
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

# <a name="get-started-with-analyzing-runtime-performance"></a><span data-ttu-id="cd293-104">Начало работы с анализом производительности выполнения</span><span class="sxs-lookup"><span data-stu-id="cd293-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="cd293-105">Чтобы узнать, как сделать загрузку страниц быстрее, перейдите к [оптимизации скорости веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="cd293-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="cd293-106">Производительность выполнения — это производительность страницы при ее запуске, а не загрузка.</span><span class="sxs-lookup"><span data-stu-id="cd293-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="cd293-107">В следующей статье руководства рассказывается об использовании панели Microsoft Edge DevTools Performance для анализа производительности выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd293-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="cd293-108">С точки зрения модели **RAIL** навыки, которые вы узнаете в этом руководстве, полезны для анализа этапов ответа, анимации и простоя страницы.</span><span class="sxs-lookup"><span data-stu-id="cd293-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a><span data-ttu-id="cd293-109">Начало работы</span><span class="sxs-lookup"><span data-stu-id="cd293-109">Get started</span></span>  

<span data-ttu-id="cd293-110">В следующем руководстве вы открываете DevTools на странице в прямом эфире и используете панель **Performance,** чтобы найти узкие места производительности на странице.</span><span class="sxs-lookup"><span data-stu-id="cd293-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="cd293-111">Откройте Microsoft Edge в **режиме InPrivate.**</span><span class="sxs-lookup"><span data-stu-id="cd293-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="cd293-112">Режим InPrivate гарантирует, что Microsoft Edge работает в чистом состоянии.</span><span class="sxs-lookup"><span data-stu-id="cd293-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="cd293-113">Например, если установлено множество расширений, расширения могут создавать шум в измерениях производительности.</span><span class="sxs-lookup"><span data-stu-id="cd293-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="cd293-114">Загрузите следующую страницу в окне InPrivate.</span><span class="sxs-lookup"><span data-stu-id="cd293-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="cd293-115">Страница — это демонстрация, которую вы собираетесь профилю.</span><span class="sxs-lookup"><span data-stu-id="cd293-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="cd293-116">На странице показана куча маленьких значков, перемещаясь вверх и вниз.</span><span class="sxs-lookup"><span data-stu-id="cd293-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="cd293-117">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\) для открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="cd293-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="Демонстрация слева и DevTools справа" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="cd293-119">Демонстрация слева и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="cd293-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-120">Для остальных фигур DevTools [][DevtoolsCustomizePlacement] отсоедино в отдельное окно, чтобы лучше сосредоточиться на содержимом.</span><span class="sxs-lookup"><span data-stu-id="cd293-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <a name="simulate-a-mobile-cpu"></a><span data-ttu-id="cd293-121">Имитация мобильного ЦП</span><span class="sxs-lookup"><span data-stu-id="cd293-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="cd293-122">Мобильные устройства имеют гораздо меньше мощности процессора, чем настольные компьютеры и ноутбуки.</span><span class="sxs-lookup"><span data-stu-id="cd293-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="cd293-123">При профилирование страницы используйте регулирование ЦП для имитации работы страницы на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="cd293-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="cd293-124">В DevTools выберите средство **Performance.**</span><span class="sxs-lookup"><span data-stu-id="cd293-124">In DevTools, choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="cd293-125">Убедитесь, что вы выбираете почтовый ящик рядом со **снимками экрана.**</span><span class="sxs-lookup"><span data-stu-id="cd293-125">Ensure the you choose the checkbox next to **Screenshots**.</span></span>  
1.  <span data-ttu-id="cd293-126">Выберите **Параметры захвата** \. ![ Параметры захвата ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="cd293-126">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>  <span data-ttu-id="cd293-127">В DevTools раскрываются параметры, связанные с тем, как он фиксирует показатели производительности.</span><span class="sxs-lookup"><span data-stu-id="cd293-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="cd293-128">Для **ЦП**выберите **4x замедление.**</span><span class="sxs-lookup"><span data-stu-id="cd293-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="cd293-129">DevTools разгорарит ЦП так, чтобы он был в 4 раза медленнее обычного.</span><span class="sxs-lookup"><span data-stu-id="cd293-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Throttle CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="cd293-131">Throttle CPU</span><span class="sxs-lookup"><span data-stu-id="cd293-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-132">При тестировании других страниц; если вы хотите убедиться, что каждая страница хорошо работает на мобильных устройствах низкого уровня, установите регулирование ЦП до **замедления 6x**.</span><span class="sxs-lookup"><span data-stu-id="cd293-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="cd293-133">Демонстрация не работает с 6x замедлением, поэтому она просто использует замедление 4x для учебных целей.</span><span class="sxs-lookup"><span data-stu-id="cd293-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <a name="set-up-the-demo"></a><span data-ttu-id="cd293-134">Настройка демонстрации</span><span class="sxs-lookup"><span data-stu-id="cd293-134">Set up the demo</span></span>  

<span data-ttu-id="cd293-135">Сложно создать демонстрацию производительности выполнения, которая последовательно работает для всех читателей веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="cd293-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="cd293-136">В следующем разделе вы можете настроить демонстрацию, чтобы убедиться, что ваш опыт относительно соответствует скриншотам и описаниям, независимо от конкретной настройки.</span><span class="sxs-lookup"><span data-stu-id="cd293-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="cd293-137">Выберите **кнопку Добавить 10,** пока синие значки не будут двигаться заметно медленнее, чем раньше.</span><span class="sxs-lookup"><span data-stu-id="cd293-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="cd293-138">На компьютере высокого уровня можно выбрать его около 20 раз.</span><span class="sxs-lookup"><span data-stu-id="cd293-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="cd293-139">Выберите **Оптимизируйте**.</span><span class="sxs-lookup"><span data-stu-id="cd293-139">Choose **Optimize**.</span></span>  <span data-ttu-id="cd293-140">Синие значки должны двигаться быстрее и более плавно.</span><span class="sxs-lookup"><span data-stu-id="cd293-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-141">Чтобы лучше отобразить разницу между оптимизированной и не оптимизированной версиями, выберите кнопку **Вычитание 10** несколько раз и попробуйте еще раз.</span><span class="sxs-lookup"><span data-stu-id="cd293-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="cd293-142">Если вы добавим слишком много синих значков, вы можете максимально выйти из ЦП, а затем вы не сможете наблюдать серьезные различия в результатах для двух версий.</span><span class="sxs-lookup"><span data-stu-id="cd293-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="cd293-143">Выберите **Un-Optimize**.</span><span class="sxs-lookup"><span data-stu-id="cd293-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="cd293-144">Синие значки снова перемещаются медленнее и с большей вялой скоростью.</span><span class="sxs-lookup"><span data-stu-id="cd293-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <a name="record-runtime-performance"></a><span data-ttu-id="cd293-145">Запись выполнения</span><span class="sxs-lookup"><span data-stu-id="cd293-145">Record runtime performance</span></span>  

<span data-ttu-id="cd293-146">При движении оптимизированной версии страницы синие значки перемещаются быстрее.</span><span class="sxs-lookup"><span data-stu-id="cd293-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="cd293-147">Почему так?</span><span class="sxs-lookup"><span data-stu-id="cd293-147">Why is that?</span></span>  <span data-ttu-id="cd293-148">Предполагается, что обе версии перемещают значки одинаковое количество пространства за одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="cd293-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="cd293-149">Возьмите запись в панели Performance, чтобы узнать, как определить узкие места производительности в не оптимизированной версии.</span><span class="sxs-lookup"><span data-stu-id="cd293-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="cd293-150">В DevTools выберите **Запись** \. ![ Запись ](../media/record-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="cd293-150">In DevTools, choose **Record** \(![Record](../media/record-icon.msft.png)\).</span></span>  <span data-ttu-id="cd293-151">DevTools фиксирует показатели производительности по мере выполнения страницы.</span><span class="sxs-lookup"><span data-stu-id="cd293-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Профиль страницы" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="cd293-153">Профиль страницы</span><span class="sxs-lookup"><span data-stu-id="cd293-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-154">Подождите несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="cd293-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="cd293-155">Выберите **Остановку**.</span><span class="sxs-lookup"><span data-stu-id="cd293-155">Choose **Stop**.</span></span>  <span data-ttu-id="cd293-156">DevTools прекращает запись, обрабатывает данные, а затем отображает результаты на панели Performance.</span><span class="sxs-lookup"><span data-stu-id="cd293-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Результаты профиля" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="cd293-158">Результаты профиля</span><span class="sxs-lookup"><span data-stu-id="cd293-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="cd293-159">Wow, это подавляющее количество данных.</span><span class="sxs-lookup"><span data-stu-id="cd293-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="cd293-160">не волнуйтесь, вскоре процесс станет более емким.</span><span class="sxs-lookup"><span data-stu-id="cd293-160">do not worry, soon the process makes more sense.</span></span>  

## <a name="analyze-the-results"></a><span data-ttu-id="cd293-161">Анализ результатов</span><span class="sxs-lookup"><span data-stu-id="cd293-161">Analyze the results</span></span>  

<span data-ttu-id="cd293-162">После записи производительности страницы измерьте качество производительности страницы и найдите причины.</span><span class="sxs-lookup"><span data-stu-id="cd293-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <a name="analyze-frames-per-second"></a><span data-ttu-id="cd293-163">Анализ кадров в секунду</span><span class="sxs-lookup"><span data-stu-id="cd293-163">Analyze frames per second</span></span>  

<span data-ttu-id="cd293-164">Основной метрикой для измерения производительности любой анимации является кадры в секунду \(FPS\).</span><span class="sxs-lookup"><span data-stu-id="cd293-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="cd293-165">Пользователи рады, когда анимации запускаются с 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="cd293-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="cd293-166">Просмотрите **диаграмму FPS.**</span><span class="sxs-lookup"><span data-stu-id="cd293-166">Review the **FPS** chart.</span></span>  <span data-ttu-id="cd293-167">Всякий раз, когда красная планка отображается выше **FPS,** это означает, что рамка упала настолько низко, что это, вероятно, вредит пользовательскому опыту.</span><span class="sxs-lookup"><span data-stu-id="cd293-167">Whenever a red bar is displayed above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="cd293-168">В общем, чем выше зеленая планка, тем выше FPS.</span><span class="sxs-lookup"><span data-stu-id="cd293-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Диаграмма FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="cd293-170">Диаграмма **FPS**</span><span class="sxs-lookup"><span data-stu-id="cd293-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-171">Ниже **диаграммы FPS** отображается диаграмма **ЦП.**</span><span class="sxs-lookup"><span data-stu-id="cd293-171">Below the **FPS** chart, the **CPU** chart is displayed.</span></span>  <span data-ttu-id="cd293-172">Цвета в диаграмме **ЦП** соответствуют цветам в панели **Сводка** в нижней части панели Performance.</span><span class="sxs-lookup"><span data-stu-id="cd293-172">The colors in the **CPU** chart correspond to the colors in the **Summary** panel, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="cd293-173">Тот факт, что **диаграмма ЦП** заполнена цветом, означает, что во время записи ЦП был максимум.</span><span class="sxs-lookup"><span data-stu-id="cd293-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="cd293-174">Всякий раз, когда ЦП в течение длительных периодов времени, это показатель того, что вы должны найти способы сделать меньше работы.</span><span class="sxs-lookup"><span data-stu-id="cd293-174">Whenever the CPU maxed out for long periods, it is an indicator that you should find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Диаграмма ЦП и панель сводки" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="cd293-176">Диаграмма **ЦП** и **панель сводки**</span><span class="sxs-lookup"><span data-stu-id="cd293-176">The **CPU** chart and **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-177">Наведите курсор **на диаграммы FPS,** **CPU**или **NET.**</span><span class="sxs-lookup"><span data-stu-id="cd293-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="cd293-178">В DevTools показан снимок экрана страницы в этот момент времени.</span><span class="sxs-lookup"><span data-stu-id="cd293-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="cd293-179">Переместите мышь влево и вправо, чтобы переиграть запись.</span><span class="sxs-lookup"><span data-stu-id="cd293-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="cd293-180">Действие ссылается на очистку, и оно полезно для ручного анализа прогрессии анимации.</span><span class="sxs-lookup"><span data-stu-id="cd293-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Просмотр экрана страницы вокруг отметки 2500 мс записи" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="cd293-182">Просмотр экрана страницы вокруг отметки 2500 мс записи</span><span class="sxs-lookup"><span data-stu-id="cd293-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-183">В разделе **Frames** наведите курсор на один из зеленых квадратов.</span><span class="sxs-lookup"><span data-stu-id="cd293-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="cd293-184">DevTools показывает FPS для этого конкретного кадра.</span><span class="sxs-lookup"><span data-stu-id="cd293-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="cd293-185">Каждый кадр, вероятно, значительно ниже целевой 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="cd293-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Наведите курсор на кадр" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="cd293-187">Наведите курсор на кадр</span><span class="sxs-lookup"><span data-stu-id="cd293-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="cd293-188">Конечно, на дисплее указывается, что веб-страницы выполняются не очень хорошо.</span><span class="sxs-lookup"><span data-stu-id="cd293-188">Of course, the display indicates that the webpage is not performing well.</span></span>  <span data-ttu-id="cd293-189">Но в реальных сценариях это может быть не так понятно, поэтому все средства, необходимые для измерения, пригодятся.</span><span class="sxs-lookup"><span data-stu-id="cd293-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <a name="bonus-open-the-fps-meter"></a><span data-ttu-id="cd293-190">Бонус: Откройте счетчик FPS</span><span class="sxs-lookup"><span data-stu-id="cd293-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="cd293-191">Еще одним удобным средством является счетчик FPS, который предоставляет оценки для FPS в режиме реального времени по мере работы страницы.</span><span class="sxs-lookup"><span data-stu-id="cd293-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="cd293-192">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**</span><span class="sxs-lookup"><span data-stu-id="cd293-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="cd293-193">Начните `Rendering` печатать в **командном меню** и выберите **show Rendering**.</span><span class="sxs-lookup"><span data-stu-id="cd293-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="cd293-194">В **средстве визуализации** включаем **счетчик FPS.**</span><span class="sxs-lookup"><span data-stu-id="cd293-194">In the **Rendering** tool, turn on **FPS Meter**.</span></span>  <span data-ttu-id="cd293-195">Новая накладка отображается в правом верхнем правой части представления.</span><span class="sxs-lookup"><span data-stu-id="cd293-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="Счетчик FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="cd293-197">Счетчик **FPS**</span><span class="sxs-lookup"><span data-stu-id="cd293-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="cd293-198">Выключите **счетчик FPS и** выберите, чтобы закрыть средство `Escape` **отрисовки.**</span><span class="sxs-lookup"><span data-stu-id="cd293-198">Turn off the **FPS Meter** and select `Escape` to close the **Rendering** tool.</span></span>  <span data-ttu-id="cd293-199">В этом руководстве не используется **счетчик FPS.**</span><span class="sxs-lookup"><span data-stu-id="cd293-199">You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <a name="find-the-bottleneck"></a><span data-ttu-id="cd293-200">Найти узкое место</span><span class="sxs-lookup"><span data-stu-id="cd293-200">Find the bottleneck</span></span>  

<span data-ttu-id="cd293-201">После измерения и проверки того, что анимация не выполняется хорошо, следующий шаг — ответить на вопрос "почему?".</span><span class="sxs-lookup"><span data-stu-id="cd293-201">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="cd293-202">Если события не выбраны, панель **Сводки** показывает разбивку активности.</span><span class="sxs-lookup"><span data-stu-id="cd293-202">When no events are chosen, the **Summary** panel shows you a breakdown of activity.</span></span>  <span data-ttu-id="cd293-203">Большая часть времени отрисовки проводилась на странице.</span><span class="sxs-lookup"><span data-stu-id="cd293-203">The page spent most of the time rendering.</span></span>  <span data-ttu-id="cd293-204">Так как производительность — это искусство делать меньше работы, ваша цель состоит в том, чтобы сократить время, затраченное на выполнение рендеринга.</span><span class="sxs-lookup"><span data-stu-id="cd293-204">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="Панель Сводка" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="cd293-206">Панель **Сводка**</span><span class="sxs-lookup"><span data-stu-id="cd293-206">The **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-207">**Расширь раздел Main.**</span><span class="sxs-lookup"><span data-stu-id="cd293-207">Expand the **Main** section.</span></span>  <span data-ttu-id="cd293-208">DevTools со временем показывает вам схему действий на основном потоке.</span><span class="sxs-lookup"><span data-stu-id="cd293-208">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="cd293-209">X-axis представляет запись со временем.</span><span class="sxs-lookup"><span data-stu-id="cd293-209">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="cd293-210">Каждый бар представляет событие.</span><span class="sxs-lookup"><span data-stu-id="cd293-210">Each bar represents an event.</span></span>  <span data-ttu-id="cd293-211">Более широкая планка означает, что событие заняло больше времени.</span><span class="sxs-lookup"><span data-stu-id="cd293-211">A wider bar means that event took longer.</span></span>  <span data-ttu-id="cd293-212">Y-axis представляет собой стек вызовов.</span><span class="sxs-lookup"><span data-stu-id="cd293-212">The y-axis represents the call stack.</span></span>  <span data-ttu-id="cd293-213">Если события укладываются друг на друга, это означает, что верхние события вызывают более низкие события.</span><span class="sxs-lookup"><span data-stu-id="cd293-213">When events are stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Основной раздел" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="cd293-215">Основной \*\*\*\* раздел</span><span class="sxs-lookup"><span data-stu-id="cd293-215">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cd293-216">В записи много данных.</span><span class="sxs-lookup"><span data-stu-id="cd293-216">There is a lot of data in the recording.</span></span>  <span data-ttu-id="cd293-217">Масштабирование одного события; выберите, удерживайте и перетаскивайте курсор над обзором **,** который является разделом, который включает диаграммы **FPS,** **CPU**и **NET.**</span><span class="sxs-lookup"><span data-stu-id="cd293-217">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="cd293-218">В **основном** разделе и **панели Сводка** отображаются только сведения для выбранной части записи.</span><span class="sxs-lookup"><span data-stu-id="cd293-218">The **Main** section and **Summary** panel only display information for the chosen portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Масштабирование события" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="cd293-220">Масштабирование события</span><span class="sxs-lookup"><span data-stu-id="cd293-220">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-221">Другой способ масштабирования, фокусировать **основной** раздел, выбрать фон или событие, а также выбрать `W` , или `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="cd293-221">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="cd293-222">Сосредоточься на красном треугольнике в правом верхнем справа от события **"Кадр** анимации".</span><span class="sxs-lookup"><span data-stu-id="cd293-222">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="cd293-223">Всякий раз, когда отображается красный треугольник, это предупреждение о том, что может возникнуть проблема, связанная с событием.</span><span class="sxs-lookup"><span data-stu-id="cd293-223">Whenever a red triangle is displayed, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-224">Событие **"Запуск кадров анимации"** происходит при запуске [вызова requestAnimationFrame()][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="cd293-224">The **Animation Frame Fired** event occurs whenever a [requestAnimationFrame() callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="cd293-225">Выберите событие **"Кадр анимации".**</span><span class="sxs-lookup"><span data-stu-id="cd293-225">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="cd293-226">На **панели Сводки** теперь показаны сведения об этом событии.</span><span class="sxs-lookup"><span data-stu-id="cd293-226">The **Summary** panel now shows you information about that event.</span></span>  <span data-ttu-id="cd293-227">Обратите внимание на **ссылку Reveal.**</span><span class="sxs-lookup"><span data-stu-id="cd293-227">Note the **Reveal** link.</span></span>  <span data-ttu-id="cd293-228">После его выбора в DevTools будет выделено событие, которое инициировало событие **"Кадры анимации".**</span><span class="sxs-lookup"><span data-stu-id="cd293-228">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="cd293-229">Кроме того, сосредоточься на **ссылкеapp.js:95.**</span><span class="sxs-lookup"><span data-stu-id="cd293-229">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="cd293-230">После его выбора отображается соответствующая строка в исходный код.</span><span class="sxs-lookup"><span data-stu-id="cd293-230">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Дополнительные сведения о событии "Кадр анимации"." lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="cd293-232">Дополнительные сведения о **событии "Кадр анимации".**</span><span class="sxs-lookup"><span data-stu-id="cd293-232">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-233">После выбора события используйте клавиши стрелки, чтобы выбрать события рядом с ней.</span><span class="sxs-lookup"><span data-stu-id="cd293-233">After choosing an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="cd293-234">В **событии app.update** имеется куча фиолетовых событий.</span><span class="sxs-lookup"><span data-stu-id="cd293-234">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="cd293-235">Если каждое фиолетовое событие было более широким, оно выглядит так, будто на каждом из них может быть красный треугольник.</span><span class="sxs-lookup"><span data-stu-id="cd293-235">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="cd293-236">Выберите одно из событий **фиолетового макета.**</span><span class="sxs-lookup"><span data-stu-id="cd293-236">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="cd293-237">DevTools предоставляет дополнительные сведения о событии в панели **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="cd293-237">DevTools provides more information about the event in the **Summary** panel.</span></span>  <span data-ttu-id="cd293-238">Действительно, существует предупреждение о принудительном повторном потоке \(другое слово для макета\).</span><span class="sxs-lookup"><span data-stu-id="cd293-238">Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="cd293-239">В панели **Сводка** выберите \*\* ссылкуapp.js:71\*\* в **статье Layout Forced**.</span><span class="sxs-lookup"><span data-stu-id="cd293-239">In the **Summary** panel, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="cd293-240">DevTools принимает вас к строке кода, которая заставила макет.</span><span class="sxs-lookup"><span data-stu-id="cd293-240">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="Строка кода, вызываемая принудительной компоновкой" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="cd293-242">Строка кода, вызываемая принудительной компоновкой</span><span class="sxs-lookup"><span data-stu-id="cd293-242">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="cd293-243">Проблема с кодом заключается в том, что в каждом кадре анимации он изменяет стиль для каждого значка, а затем запрашивает положение каждого значка на странице.</span><span class="sxs-lookup"><span data-stu-id="cd293-243">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="cd293-244">Так как стили изменились, браузер не знает, изменилась ли каждая позиция значка, поэтому для вычисления новой позиции ему необходимо изменить макет значка.</span><span class="sxs-lookup"><span data-stu-id="cd293-244">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="cd293-245">Это было многому научиться.</span><span class="sxs-lookup"><span data-stu-id="cd293-245">That was a lot to learn.</span></span>  <span data-ttu-id="cd293-246">Теперь в базовом рабочего процессах имеется прочная основа для анализа производительности выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd293-246">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="cd293-247">Молодец.</span><span class="sxs-lookup"><span data-stu-id="cd293-247">Good job.</span></span>  

### <a name="bonus-analyze-the-optimized-version"></a><span data-ttu-id="cd293-248">Бонус: анализ оптимизированной версии</span><span class="sxs-lookup"><span data-stu-id="cd293-248">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="cd293-249">Используя только что выучатые процессы \*\*\*\* и инструменты, выберите Оптимизируйте демо, чтобы включить оптимизированный код, сделать еще одну запись производительности и проанализировать результаты.</span><span class="sxs-lookup"><span data-stu-id="cd293-249">Using the workflows and tools that you just learned, choose **Optimize** on the demo to turn on the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="cd293-250">От улучшенного кадра до сокращения событий в схеме пламени в разделе **Main** оптимизированная версия приложения работает гораздо меньше, что приводит к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="cd293-250">From the improved framerate to the reduction in events in the flame chart in the **Main** section, the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="cd293-251">Даже оптимизированная версия не является отличной, так как она управляет `top` свойством каждого значка.</span><span class="sxs-lookup"><span data-stu-id="cd293-251">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="cd293-252">Лучше придерживаться свойств, которые влияют только на композитную работу.</span><span class="sxs-lookup"><span data-stu-id="cd293-252">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a><span data-ttu-id="cd293-253">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cd293-253">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

<span data-ttu-id="cd293-254">Чтобы удобнее работать с инструментом **Performance,** практика позволяет совершенствоваться.</span><span class="sxs-lookup"><span data-stu-id="cd293-254">To get more comfortable with the **Performance** tool, practice makes perfect.</span></span>  <span data-ttu-id="cd293-255">Попробуйте профилирование страниц и анализ результатов.</span><span class="sxs-lookup"><span data-stu-id="cd293-255">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="cd293-256">Если у вас возникли вопросы о \*\*\*\* результатах, используйте значок Отправка отзывов, выберите `Alt` + `Shift` + `I` \(Windows, Linux\), выберите `Option` + `Shift` + `I` \(macOS\) [][TwitterEdgeDevtools]или чирикать команду DevTools .</span><span class="sxs-lookup"><span data-stu-id="cd293-256">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="cd293-257">Если это возможно, включаем скриншоты или ссылки на воспроизводимые страницы.</span><span class="sxs-lookup"><span data-stu-id="cd293-257">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="Значок **Feedback** в Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="cd293-259">Значок **Отправка** отзывов в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cd293-259">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="cd293-260">Наконец, существует множество способов повышения производительности выполнения.</span><span class="sxs-lookup"><span data-stu-id="cd293-260">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="cd293-261">В этой статье основное внимание было уделялось одному конкретному узкому узким местам анимации, чтобы предоставить вам целенаправленный тур по панели Performance, но это только одно из многих узких моментов, с которыми вы можете столкнуться.</span><span class="sxs-lookup"><span data-stu-id="cd293-261">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cd293-262">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="cd293-262">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools (Undock, dock to bottom, dock to left)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools — публикация чирикать | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\\\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="cd293-267">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd293-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cd293-268">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="cd293-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cd293-270">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cd293-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
