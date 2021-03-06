---
description: Проверка и изменение анимации с помощью инспектора анимации Microsoft Edge DevTools.
title: Проверка эффектов анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 742096f13179de2ad1a95dc9fa62d2bbf3d7c226
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397736"
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

# <a name="inspect-animations"></a><span data-ttu-id="b0ba0-104">Проверка эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-104">Inspect animations</span></span>  

<span data-ttu-id="b0ba0-105">Проверка и изменение анимации с помощью инспектора анимации Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-105">Inspect and modify animations with the Microsoft Edge DevTools Animation Inspector.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   <span data-ttu-id="b0ba0-107">инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-107">animation inspector</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="b0ba0-108">Сводка</span><span class="sxs-lookup"><span data-stu-id="b0ba0-108">Summary</span></span>  

*   <span data-ttu-id="b0ba0-109">Захват анимации, открыв инспектор анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-109">Capture animations by opening the Animation Inspector.</span></span>  <span data-ttu-id="b0ba0-110">Инспектор анимации автоматически обнаруживает и сортируется анимации в группы.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-110">The Animation Inspector automatically detects and sorts animations into groups.</span></span>  
*   <span data-ttu-id="b0ba0-111">Проверьте анимации, замедляя каждую из них, повторив каждую из них или просматривая исходный код.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-111">Inspect animations by slowing down each one, replaying each one, or viewing the source code.</span></span>  
*   <span data-ttu-id="b0ba0-112">Изменение анимации путем изменения времени, задержки, продолжительности или смещения ключей.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-112">Modify animations by changing the timing, delay, duration, or keyframe offsets.</span></span>  

## <a name="overview"></a><span data-ttu-id="b0ba0-113">Обзор</span><span class="sxs-lookup"><span data-stu-id="b0ba0-113">Overview</span></span>  

<span data-ttu-id="b0ba0-114">Инспектор анимации Microsoft Edge DevTools имеет две основные цели.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-114">The Microsoft Edge DevTools Animation Inspector has two main purposes.</span></span>  

*   <span data-ttu-id="b0ba0-115">Проверка анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-115">Inspecting animations.</span></span>  <span data-ttu-id="b0ba0-116">Необходимо замедлить, повторить или проверить исходный код группы анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-116">You want to slow down, replay, or inspect the source code for an Animation Group.</span></span>  
*   <span data-ttu-id="b0ba0-117">Изменение анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-117">Modifying animations.</span></span>  <span data-ttu-id="b0ba0-118">Необходимо изменить смещение времени, задержки, продолжительности или смещения ключей группы анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-118">You want to modify the timing, delay, duration, or keyframe offsets of an Animation Group.</span></span>  <span data-ttu-id="b0ba0-119">Редактирование Безье и редактирование ключей в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-119">Bezier editing and keyframe editing are currently not supported.</span></span>  

<span data-ttu-id="b0ba0-120">Инспектор анимации поддерживает CSS-анимации, переходы CSS и веб-анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-120">The Animation Inspector supports CSS animations, CSS transitions, and web animations.</span></span>  `requestAnimationFrame` <span data-ttu-id="b0ba0-121">анимации в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-121">animations are currently not supported.</span></span>  

### <a name="what-is-an-animation-group"></a><span data-ttu-id="b0ba0-122">Что такое группа анимации?</span><span class="sxs-lookup"><span data-stu-id="b0ba0-122">What is an Animation Group?</span></span>  

<span data-ttu-id="b0ba0-123">Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-123">An Animation Group is a group of animations that may be related to each other.</span></span>  <span data-ttu-id="b0ba0-124">В настоящее время в Интернете нет реальной концепции групповой анимации, поэтому дизайнеры и разработчики движения должны составлять и время отдельных анимаций, чтобы анимации отобразить как один согласованный визуальный эффект.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-124">Currently, the web has no real concept of a group animation, so motion designers and developers have to compose and time individual animations so that the animations render as one coherent visual effect.</span></span>  <span data-ttu-id="b0ba0-125">Инспектор анимации предсказывает, какие анимации связаны в зависимости от времени начала \(за исключением задержек и так далее\).</span><span class="sxs-lookup"><span data-stu-id="b0ba0-125">The Animation Inspector predicts which animations are related based on start time \(excluding delays, and so on\).</span></span>  <span data-ttu-id="b0ba0-126">Инспектор анимации также группит анимации бок о бок.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-126">The Animation Inspector also groups the animations side-by-side.</span></span>  
<span data-ttu-id="b0ba0-127">Другими словами, набор анимаций, которые запускаются в одном блоке скриптов, сгруппирован вместе.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-127">In other words, a set of animations that are all triggered in the same script block are grouped together.</span></span>  <span data-ttu-id="b0ba0-128">Если анимация асинхронна, она помещается в отдельную группу.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-128">If an animation is asynchronous, it is placed in a separate group.</span></span>  

## <a name="get-started"></a><span data-ttu-id="b0ba0-129">Начало работы</span><span class="sxs-lookup"><span data-stu-id="b0ba0-129">Get started</span></span>  

<span data-ttu-id="b0ba0-130">Существует два способа открыть инспектор анимации:</span><span class="sxs-lookup"><span data-stu-id="b0ba0-130">There are two ways to open the Animation Inspector:</span></span>  

*   <span data-ttu-id="b0ba0-131">Откройте меню **Customize and Control DevTools**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-131">Open the **Customize and Control DevTools** menu</span></span>  
    1.  <span data-ttu-id="b0ba0-132">Перейдите в **подмену Дополнительные** средства.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-132">Navigate to the **More tools** sub-menu.</span></span>  
    1.  <span data-ttu-id="b0ba0-133">Выбор **анимаций:**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-133">Choose **Animations**:</span></span>  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Анимации с помощью основного меню" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           <span data-ttu-id="b0ba0-135">**Анимации** с помощью основного меню</span><span class="sxs-lookup"><span data-stu-id="b0ba0-135">**Animations** using Main Menu</span></span>  
    :::image-end:::  
        
*   <span data-ttu-id="b0ba0-136">Откройте **меню команд**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-136">Open the **Command Menu**</span></span>  
    1.  <span data-ttu-id="b0ba0-137">Введите `Drawer: Show Animations`.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-137">Type `Drawer: Show Animations`.</span></span>  

<span data-ttu-id="b0ba0-138">Инспектор анимации открывается рядом с **консольным средством.**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-138">The Animation Inspector opens next to the **Console** tool.</span></span>  <span data-ttu-id="b0ba0-139">Так как инспектор анимации является средством ящика, вы можете использовать инспектор анимации из любой панели DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-139">Since the Animation Inspector is a Drawer tool, you may use the Animation Inspector from any DevTools panel.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Инспектор пустой анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   <span data-ttu-id="b0ba0-141">Инспектор пустой анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-141">Empty Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-142">Инспектор анимации сгруппируется в четыре основных раздела \(или panes\).</span><span class="sxs-lookup"><span data-stu-id="b0ba0-142">The Animation Inspector is grouped into four main sections \(or panes\).</span></span>  <span data-ttu-id="b0ba0-143">Это руководство ссылается на каждую области следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b0ba0-143">This guide refers to each pane as follows:</span></span>  

| <span data-ttu-id="b0ba0-144">Индекс</span><span class="sxs-lookup"><span data-stu-id="b0ba0-144">Index</span></span> | <span data-ttu-id="b0ba0-145">Панель</span><span class="sxs-lookup"><span data-stu-id="b0ba0-145">Pane</span></span> | <span data-ttu-id="b0ba0-146">Описание</span><span class="sxs-lookup"><span data-stu-id="b0ba0-146">Description</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b0ba0-147">1</span><span class="sxs-lookup"><span data-stu-id="b0ba0-147">1</span></span> | **<span data-ttu-id="b0ba0-148">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="b0ba0-148">Controls</span></span>** | <span data-ttu-id="b0ba0-149">Отсюда можно очистить все захваченные в настоящее время группы анимации или изменить скорость выбранной в настоящее время группы анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-149">From here you may clear all currently captured Animation Groups, or change the speed of the currently selected Animation Group.</span></span> |  
| <span data-ttu-id="b0ba0-150">2</span><span class="sxs-lookup"><span data-stu-id="b0ba0-150">2</span></span> | **<span data-ttu-id="b0ba0-151">Обзор</span><span class="sxs-lookup"><span data-stu-id="b0ba0-151">Overview</span></span>** | <span data-ttu-id="b0ba0-152">Выберите группу анимации здесь, чтобы проверить и изменить ее в области **Подробности.**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-152">Choose an Animation Group here to inspect and modify it in the **Details** pane.</span></span> |  
| <span data-ttu-id="b0ba0-153">3</span><span class="sxs-lookup"><span data-stu-id="b0ba0-153">3</span></span> | **<span data-ttu-id="b0ba0-154">Информация о сроках</span><span class="sxs-lookup"><span data-stu-id="b0ba0-154">Timeline</span></span>** | <span data-ttu-id="b0ba0-155">Приостановка и запуск анимации отсюда или переход к определенной точке анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-155">Pause and start an animation from here, or jump to a specific point in the animation.</span></span> |  
| <span data-ttu-id="b0ba0-156">4</span><span class="sxs-lookup"><span data-stu-id="b0ba0-156">4</span></span> | **<span data-ttu-id="b0ba0-157">Сведения</span><span class="sxs-lookup"><span data-stu-id="b0ba0-157">Details</span></span>** | <span data-ttu-id="b0ba0-158">Проверка и изменение выбранной в настоящее время группы анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-158">Inspect and modify the currently selected Animation Group.</span></span> |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Аннотированный инспектор анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   <span data-ttu-id="b0ba0-160">Аннотированный инспектор анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-160">Annotated Animation Inspector</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-161">Чтобы захватить анимацию, просто выполните взаимодействие, которое запускает анимацию, пока инспектор анимации открыт.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-161">To capture an animation, just perform the interaction that triggers the animation while the Animation Inspector is open.</span></span>  <span data-ttu-id="b0ba0-162">Если анимация запускается на странице, обновите страницу с помощью инспектора анимации, открываемой для обнаружения анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-162">If an animation is triggered on page load, refresh the page with the Animation Inspector open to detect the animation.</span></span>  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a><span data-ttu-id="b0ba0-163">Проверка эффектов анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-163">Inspect animations</span></span>  

<span data-ttu-id="b0ba0-164">После захвата анимации существует несколько способов ее воспроизведения:</span><span class="sxs-lookup"><span data-stu-id="b0ba0-164">After you capture an animation, there are a few ways to replay it:</span></span>  

*   <span data-ttu-id="b0ba0-165">Наведите курсор на эскиз в области **Обзор,** чтобы просмотреть его предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-165">Hover on the thumbnail in the **Overview** pane to view a preview of it.</span></span>  
*   <span data-ttu-id="b0ba0-166">Выберите группу анимации из области **Обзор** \(так, \*\*\*\* чтобы она отображалась в области Details\) и выберите значок **повтора** \( значок ![ воспроизведения ][ImageReplayButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b0ba0-166">Choose the Animation Group from the **Overview** pane \(so that it is displayed in the **Details** pane\) and choose the **replay** \(![replay icon][ImageReplayButtonIcon]\) icon.</span></span>  <span data-ttu-id="b0ba0-167">Анимация повторяется в представлении.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-167">The animation is replayed in the viewport.</span></span>  <span data-ttu-id="b0ba0-168">Выберите **значки** скорости анимации \( значки скорости анимации\) для изменения скорости предварительного просмотра выбранной в настоящее время ![ ][ImageAnimationSpeedButtonsIcon] группы анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-168">Choose the **animation speed** \(![animation speed icons][ImageAnimationSpeedButtonsIcon]\) icons to change the preview speed of the currently selected Animation Group.</span></span>  <span data-ttu-id="b0ba0-169">Для изменения текущего положения можно использовать красную вертикальную планку.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-169">You may use the red vertical bar to change your current position.</span></span>  
*   <span data-ttu-id="b0ba0-170">Выберите и перетащите красную вертикальную планку для очистки анимации представления.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-170">Choose and drag the red vertical bar to scrub the viewport animation.</span></span>  
    
### <a name="view-animation-details"></a><span data-ttu-id="b0ba0-171">Просмотр сведений о анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-171">View animation details</span></span>  

<span data-ttu-id="b0ba0-172">После захвата группы анимации выберите на ней из области **Обзор,** чтобы просмотреть сведения.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-172">After you capture an Animation Group, choose on it from the **Overview** pane to view the details.</span></span>  <span data-ttu-id="b0ba0-173">В области **Details** каждой отдельной анимации назначена строка.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-173">In the **Details** pane each individual animation is assigned the a row.</span></span>  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Сведения о группе анимации" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="b0ba0-175">Сведения о группе анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-175">Animation Group details</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-176">Наведите курсор анимации, чтобы выделить ее в представлении.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-176">Hover on an animation to highlight it in the viewport.</span></span>  <span data-ttu-id="b0ba0-177">Выберите анимацию, чтобы выбрать ее в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="b0ba0-177">Choose the animation to select it in the **Elements** tool.</span></span>  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Наведите курсор анимации, чтобы выделить ее в представлении" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   <span data-ttu-id="b0ba0-179">Наведите курсор анимации, чтобы выделить ее в представлении</span><span class="sxs-lookup"><span data-stu-id="b0ba0-179">Hover on the animation to highlight it in viewport</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-180">Левый, более темный раздел анимации — это определение.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-180">The leftmost, darker section of an animation is the definition.</span></span>  <span data-ttu-id="b0ba0-181">Правый, более увядаемый раздел представляет итерации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-181">The right, more faded section represents iterations.</span></span>  <span data-ttu-id="b0ba0-182">Например, на следующем рисунке разделы 2 и 3 представляют итерации раздела 1.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-182">For example, in the following figure, sections two and three represent iterations of section one.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Схема итерации анимации" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   <span data-ttu-id="b0ba0-184">Схема итерации анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-184">Diagram of animation iterations</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-185">Если в двух элементах применена та же анимация, инспектор анимации назначает элементам один и тот же цвет.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-185">If two elements have the same animation applied, the Animation Inspector assigns the same color to the elements.</span></span>  <span data-ttu-id="b0ba0-186">Цвет случайный и не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-186">The color is random and has no significance.</span></span>  <span data-ttu-id="b0ba0-187">Например, на следующей фигуре применяются два элемента с одинаковой анимацией `div.cwccw.earlier` `div.cwccw.later` `spinrightleft` \( \) как и `div.ccwcw.earlier` `div.ccwcw.later` элементы.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-187">For example, in the following figure, the two elements `div.cwccw.earlier` and `div.cwccw.later` have the same animation \(`spinrightleft`\) applied, as do the `div.ccwcw.earlier` and `div.ccwcw.later` elements.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Цветные анимации" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   <span data-ttu-id="b0ba0-189">Цветные анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-189">Color-coded animations</span></span>  
:::image-end:::  

## <a name="modify-animations"></a><span data-ttu-id="b0ba0-190">Изменение анимации</span><span class="sxs-lookup"><span data-stu-id="b0ba0-190">Modify animations</span></span>  

<span data-ttu-id="b0ba0-191">Существует три способа изменения анимации с помощью инспектора анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-191">There are three ways you are able to modify an animation with the Animation Inspector.</span></span>  

*   <span data-ttu-id="b0ba0-192">Продолжительность анимации.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-192">Animation duration.</span></span>  
*   <span data-ttu-id="b0ba0-193">Сроки keyframe.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-193">Keyframe timings.</span></span>  
*   <span data-ttu-id="b0ba0-194">Задержка во времени начала.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-194">Start time delay.</span></span>  
    
<span data-ttu-id="b0ba0-195">На следующем рисунке представлена оригинальная анимация.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-195">In the following figure, the original animation is represented.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Оригинальная анимация перед изменением" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   <span data-ttu-id="b0ba0-197">Оригинальная анимация перед изменением</span><span class="sxs-lookup"><span data-stu-id="b0ba0-197">Original animation before modification</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-198">Чтобы изменить продолжительность анимации, выберите и перетащите первый или последний круг.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-198">To change the duration of an animation, choose and drag the first or last circle.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Измененная продолжительность" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   <span data-ttu-id="b0ba0-200">Измененная продолжительность</span><span class="sxs-lookup"><span data-stu-id="b0ba0-200">Modified duration</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-201">Если анимация определяет какие-либо правила keyframe, то они представляются белыми внутренними кругами.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-201">If the animation defines any keyframe rules, then these are represented as white inner circles.</span></span>  <span data-ttu-id="b0ba0-202">Выберите и перетащите один из них, чтобы изменить сроки ключевых рамок.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-202">Choose and drag one of these to change the timing of the keyframe.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Измененный keyframe" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   <span data-ttu-id="b0ba0-204">Измененный keyframe</span><span class="sxs-lookup"><span data-stu-id="b0ba0-204">Modified keyframe</span></span>  
:::image-end:::  

<span data-ttu-id="b0ba0-205">Чтобы добавить задержку в анимацию, выберите и перетащите ее в любом месте, кроме кругов.</span><span class="sxs-lookup"><span data-stu-id="b0ba0-205">To add a delay to an animation, choose and drag it anywhere except the circles.</span></span>  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Измененная задержка" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   <span data-ttu-id="b0ba0-207">Измененная задержка</span><span class="sxs-lookup"><span data-stu-id="b0ba0-207">Modified delay</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b0ba0-208">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b0ba0-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="b0ba0-209">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0ba0-209">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0ba0-210">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="b0ba0-210">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0ba0-212">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0ba0-212">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
