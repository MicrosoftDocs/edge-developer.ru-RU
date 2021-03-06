---
description: Узнайте, как использовать Microsoft Edge DevTools для поиска способов ускорения загрузки веб-сайтов.
title: Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 7de97ab27528e89e2373e0a0d1002e8c86e37613
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398114"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a><span data-ttu-id="477c6-104">Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="477c6-104">Optimize website speed with Microsoft Edge DevTools</span></span>  

## <a name="goal-of-tutorial"></a><span data-ttu-id="477c6-105">Цель учебника</span><span class="sxs-lookup"><span data-stu-id="477c6-105">Goal of tutorial</span></span>  

<span data-ttu-id="477c6-106">В этом руководстве рассказывается о том, как использовать Microsoft Edge DevTools для поиска способов ускорения загрузки веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="477c6-106">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="477c6-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="477c6-107">Prerequisites</span></span>  

*   <span data-ttu-id="477c6-108">Вы должны иметь базовый опыт веб-разработки, аналогичный тому, что преподается в этом классе ["Введение в веб-разработку".][CourseraIntroductionWebDevelopmentClass]</span><span class="sxs-lookup"><span data-stu-id="477c6-108">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="477c6-109">Вам не нужно ничего знать о производительности нагрузки.</span><span class="sxs-lookup"><span data-stu-id="477c6-109">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="477c6-110">Об этом вы узнаете в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="477c6-110">You learn about it in this tutorial.</span></span>  

## <a name="introduction"></a><span data-ttu-id="477c6-111">Введение</span><span class="sxs-lookup"><span data-stu-id="477c6-111">Introduction</span></span>  

<span data-ttu-id="477c6-112">Это Тони.</span><span class="sxs-lookup"><span data-stu-id="477c6-112">This is Tony.</span></span>  <span data-ttu-id="477c6-113">Тони очень известен в кошачьем обществе.</span><span class="sxs-lookup"><span data-stu-id="477c6-113">Tony is very famous in cat society.</span></span>  <span data-ttu-id="477c6-114">Он создал веб-сайт, чтобы его поклонники могли узнать о его любимых продуктах.</span><span class="sxs-lookup"><span data-stu-id="477c6-114">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="477c6-115">Его поклонники любят сайт, но Тони продолжает слышать жалобы, что сайт загружается медленно.</span><span class="sxs-lookup"><span data-stu-id="477c6-115">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="477c6-116">Тони попросил вас помочь ему ускорить сайт.</span><span class="sxs-lookup"><span data-stu-id="477c6-116">Tony has asked you to help him speed the site up.</span></span>  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony the cat" lightbox="../media/speed-tony.msft.png":::
   <span data-ttu-id="477c6-118">Tony the cat</span><span class="sxs-lookup"><span data-stu-id="477c6-118">Tony the cat</span></span>  
:::image-end:::  

## <a name="step-1-audit-the-site"></a><span data-ttu-id="477c6-119">Шаг 1. Аудит сайта</span><span class="sxs-lookup"><span data-stu-id="477c6-119">Step 1: Audit the site</span></span>  

<span data-ttu-id="477c6-120">Всякий раз, когда вы затеяли повышение производительности загрузки сайта, **всегда начните с аудита.**</span><span class="sxs-lookup"><span data-stu-id="477c6-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="477c6-121">Аудит имеет 2 важных функции:</span><span class="sxs-lookup"><span data-stu-id="477c6-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="477c6-122">Он создает **базовый уровень** для измерения последующих изменений.</span><span class="sxs-lookup"><span data-stu-id="477c6-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="477c6-123">Это дает вам **полезные советы** о том, какие изменения оказывают наибольшее влияние.</span><span class="sxs-lookup"><span data-stu-id="477c6-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  
    
### <a name="set-up"></a><span data-ttu-id="477c6-124">Настройка</span><span class="sxs-lookup"><span data-stu-id="477c6-124">Set up</span></span>  

<span data-ttu-id="477c6-125">Сначала необходимо настроить сайт, чтобы можно было внести изменения в него позже.</span><span class="sxs-lookup"><span data-stu-id="477c6-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="477c6-126">[Откройте исходный код сайта](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="477c6-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="477c6-127">Эта вкладка называется вкладка **редактора**.</span><span class="sxs-lookup"><span data-stu-id="477c6-127">This tab is referred to as the **editor tab**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Вкладка редактора" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       <span data-ttu-id="477c6-129">Вкладка **редактора**</span><span class="sxs-lookup"><span data-stu-id="477c6-129">The **editor tab**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-130">Выберите **Тони**.</span><span class="sxs-lookup"><span data-stu-id="477c6-130">Choose **tony**.</span></span>  <span data-ttu-id="477c6-131">Появляется меню.</span><span class="sxs-lookup"><span data-stu-id="477c6-131">A menu appears.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Меню, которое появляется после выбора Тони" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       <span data-ttu-id="477c6-133">Меню, которое появляется после выбора **Тони**</span><span class="sxs-lookup"><span data-stu-id="477c6-133">The menu that appears after choosing **tony**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-134">Выберите **Проект Remix**.</span><span class="sxs-lookup"><span data-stu-id="477c6-134">Choose **Remix Project**.</span></span>  <span data-ttu-id="477c6-135">Имя проекта изменяется с **тони** на какое-то случайным образом созданным именем.</span><span class="sxs-lookup"><span data-stu-id="477c6-135">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="477c6-136">Теперь у вас есть собственная редактируемая копия кода.</span><span class="sxs-lookup"><span data-stu-id="477c6-136">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="477c6-137">Позже вы можете внести изменения в этот код.</span><span class="sxs-lookup"><span data-stu-id="477c6-137">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="477c6-138">Выберите **Показать** и **выбрать в новом окне**.</span><span class="sxs-lookup"><span data-stu-id="477c6-138">Choose **Show** and choose **In a New Window**.</span></span>  <span data-ttu-id="477c6-139">Демонстрация открывается на новой вкладке.  Эта вкладка называется вкладка **демо.**  Загрузка сайта может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="477c6-139">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Вкладка демонстрации" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       <span data-ttu-id="477c6-141">Вкладка демонстрации</span><span class="sxs-lookup"><span data-stu-id="477c6-141">The demo tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-142">Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="477c6-142">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="477c6-143">Microsoft Edge DevTools открывается рядом с демонстрацией.</span><span class="sxs-lookup"><span data-stu-id="477c6-143">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools и демо" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       <span data-ttu-id="477c6-145">DevTools и демо</span><span class="sxs-lookup"><span data-stu-id="477c6-145">DevTools and the demo</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-146">Для остальных скриншотов в этом руководстве DevTools отображается в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="477c6-146">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="477c6-147">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\) `Undock` \*\*\*\* для открытия командного меню, ввода и выбора Undock в отдельное окно.</span><span class="sxs-lookup"><span data-stu-id="477c6-147">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="Неохватанные DevTools" lightbox="../media/speed-console.msft.png":::
   <span data-ttu-id="477c6-149">Неохватанные DevTools</span><span class="sxs-lookup"><span data-stu-id="477c6-149">Undocked DevTools</span></span>  
:::image-end:::  

### <a name="establish-a-baseline"></a><span data-ttu-id="477c6-150">Создание базового плана</span><span class="sxs-lookup"><span data-stu-id="477c6-150">Establish a baseline</span></span>  

<span data-ttu-id="477c6-151">Базовая запись о том, как сайт выполнялся, прежде чем вы сделали какие-либо улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="477c6-151">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="477c6-152">Выберите средство **аудита.**</span><span class="sxs-lookup"><span data-stu-id="477c6-152">Choose the **Audits** tool.</span></span>  <span data-ttu-id="477c6-153">Она может быть скрыта за кнопкой **More Panels** ![ \( More Panels ][ImageMorePanelsIcon] \) .</span><span class="sxs-lookup"><span data-stu-id="477c6-153">It may be hidden behind the **More Panels** \(![More Panels][ImageMorePanelsIcon]\) button.</span></span>  <span data-ttu-id="477c6-154">На этой панели есть маяк, так как проект, который имеет полномочия панели аудитов, называется **Маяк.**</span><span class="sxs-lookup"><span data-stu-id="477c6-154">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Средство аудита" lightbox="../media/speed-audits-performance.msft.png":::
       <span data-ttu-id="477c6-156">Средство **аудита**</span><span class="sxs-lookup"><span data-stu-id="477c6-156">The **Audits** tool</span></span>  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="477c6-157">Параметры конфигурации аудита совпадают с настройками предыдущего рисунка.</span><span class="sxs-lookup"><span data-stu-id="477c6-157">Match your audit configuration settings to those in the previous figure.</span></span>  <span data-ttu-id="477c6-158">Вот объяснение различных вариантов:</span><span class="sxs-lookup"><span data-stu-id="477c6-158">Here is an explanation of the different options:</span></span>  
    
    *   <span data-ttu-id="477c6-159">**Устройство**.</span><span class="sxs-lookup"><span data-stu-id="477c6-159">**Device**.</span></span>  <span data-ttu-id="477c6-160">Set to **Mobile** изменяет строку агента пользователя и имитирует мобильный видпорт.</span><span class="sxs-lookup"><span data-stu-id="477c6-160">Set to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="477c6-161">Установите для **настольного** компьютера в значительной степени просто отключит **мобильные** изменения.</span><span class="sxs-lookup"><span data-stu-id="477c6-161">Set to **Desktop** pretty much just turns off the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="477c6-162">**Аудиты**.</span><span class="sxs-lookup"><span data-stu-id="477c6-162">**Audits**.</span></span>  <span data-ttu-id="477c6-163">Отключите категорию, чтобы группа **аудитов** не проводила эти аудиты, и исключите эти аудиты из отчета.</span><span class="sxs-lookup"><span data-stu-id="477c6-163">Turn off a category to prevent the **Audits** panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="477c6-164">Оставьте остальные категории включенными, если вы хотите отобразить типы предоставляемых рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="477c6-164">Leave the other categories Turned on, if you want to display the types of recommendations that are provided.</span></span>  <span data-ttu-id="477c6-165">Отключите категории, чтобы немного ускорить процесс аудита.</span><span class="sxs-lookup"><span data-stu-id="477c6-165">Turn off categories to slightly speed up the auditing process.</span></span>  
    *   <span data-ttu-id="477c6-166">**Регулирование.**</span><span class="sxs-lookup"><span data-stu-id="477c6-166">**Throttling**.</span></span>  <span data-ttu-id="477c6-167">**Задаваемых для имитации медленного 4G, 4x замедление** ЦП имитирует типичные условия просмотра на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="477c6-167">Set to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="477c6-168">Она называется "смоделированная", так как панель аудита фактически не работает в процессе аудита.</span><span class="sxs-lookup"><span data-stu-id="477c6-168">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="477c6-169">Вместо этого он просто экстраполирует время загрузки страницы в условиях мобильной связи.</span><span class="sxs-lookup"><span data-stu-id="477c6-169">Instead, it just extrapolates how long the page takes to load under mobile conditions.</span></span>  <span data-ttu-id="477c6-170">Параметр **Applied...,** с другой стороны, фактически обрабатывает ЦП и сеть с помощью более длительного процесса аудита.</span><span class="sxs-lookup"><span data-stu-id="477c6-170">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="477c6-171">**Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="477c6-171">**Clear Storage**.</span></span>  <span data-ttu-id="477c6-172">Включив почтовый ящик, чтобы очистить все хранилища, связанные со страницей перед каждым аудитом.</span><span class="sxs-lookup"><span data-stu-id="477c6-172">Turn on the checkbox to clear all storage associated with the page before every audit.</span></span>  <span data-ttu-id="477c6-173">Оставьте этот параметр, если вы хотите проверять, как посетители впервые испытывают ваш сайт.</span><span class="sxs-lookup"><span data-stu-id="477c6-173">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="477c6-174">Отключите этот параметр, если вы хотите повторить посещение.</span><span class="sxs-lookup"><span data-stu-id="477c6-174">Turn off this setting when you want the repeat-visit experience.</span></span>  
    
1.  <span data-ttu-id="477c6-175">Выберите **выполнить аудиты.**</span><span class="sxs-lookup"><span data-stu-id="477c6-175">Choose **Run Audits**.</span></span>  <span data-ttu-id="477c6-176">Через 10-30 секунд панель **Аудита** отображает отчет о производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-176">After 10 to 30 seconds, the **Audits** panel displays a report of the performance of the site.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Отчет для панели аудитов производительности сайта" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       <span data-ttu-id="477c6-178">Отчет для панели аудитов производительности сайта</span><span class="sxs-lookup"><span data-stu-id="477c6-178">The report for the Audits panel of the performance of the site</span></span>  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a><span data-ttu-id="477c6-179">Обработка ошибок отчета</span><span class="sxs-lookup"><span data-stu-id="477c6-179">Handling report errors</span></span>  

<span data-ttu-id="477c6-180">Если вы когда-либо получили ошибку в отчете панели аудитов, попробуйте запускать вкладку демонстрации из окна **InPrivate** без открытия других вкладок.</span><span class="sxs-lookup"><span data-stu-id="477c6-180">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="477c6-181">Это гарантирует, что вы работаете Microsoft Edge из чистого состояния.</span><span class="sxs-lookup"><span data-stu-id="477c6-181">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="477c6-182">Расширение Microsoft Edge, в частности, часто вмешивается в процесс аудита.</span><span class="sxs-lookup"><span data-stu-id="477c6-182">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a><span data-ttu-id="477c6-183">Понимание отчета</span><span class="sxs-lookup"><span data-stu-id="477c6-183">Understand your report</span></span>  

<span data-ttu-id="477c6-184">Номер в верхней части отчета — это общая оценка производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-184">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="477c6-185">Позже при внесении изменений в код число отображаемого кода должно вырасти.</span><span class="sxs-lookup"><span data-stu-id="477c6-185">Later, as you make changes to the code, the number displayed should rise.</span></span>  <span data-ttu-id="477c6-186">Более высокий балл означает лучшую производительность.</span><span class="sxs-lookup"><span data-stu-id="477c6-186">A higher score means better performance.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Общая оценка производительности" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   <span data-ttu-id="477c6-188">Общая оценка производительности</span><span class="sxs-lookup"><span data-stu-id="477c6-188">The overall performance score</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-189">В **разделе Metrics** приводится количественная оценка производительности сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-189">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="477c6-190">Каждый показатель дает представление о различных аспектах производительности.</span><span class="sxs-lookup"><span data-stu-id="477c6-190">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="477c6-191">Например, first **Contentful Paint** сообщает вам, когда содержимое сначала покрашено на экран, что является важной вехой в восприятии пользователем нагрузки страницы, в то время как **Time To Interactive** указывает точку, на которой страница отображается достаточно готова для обработки взаимодействий пользователей.</span><span class="sxs-lookup"><span data-stu-id="477c6-191">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Раздел Метрик" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   <span data-ttu-id="477c6-193">Раздел **Метрик**</span><span class="sxs-lookup"><span data-stu-id="477c6-193">The **Metrics** section</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-194">Выберите выделенную кнопку торгле в следующем рисунке, чтобы отобразить описание для каждой метрики, и узнайте больше, **чтобы** прочитать документацию об этом.</span><span class="sxs-lookup"><span data-stu-id="477c6-194">Choose the highlighted toggle button in the following figure to display a description for each metric, and choose **Learn More** to read documentation about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Выберите выделенную кнопку toggle для расширения элементов Metrics" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   <span data-ttu-id="477c6-196">Выберите выделенную кнопку toggle для расширения элементов Metrics</span><span class="sxs-lookup"><span data-stu-id="477c6-196">Choose the highlighted toggle button to expand the Metrics items</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-197">Ниже Метрики — это коллекция скриншотов, которые показывают, как выглядела страница при загрузке.</span><span class="sxs-lookup"><span data-stu-id="477c6-197">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Скриншоты того, как выглядела страница при загрузке" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="477c6-199">Скриншоты того, как выглядела страница при загрузке</span><span class="sxs-lookup"><span data-stu-id="477c6-199">Screenshots of how the page looked while loading</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-200">В **разделе "Возможности"** приводится конкретный совет по повышению производительности нагрузки на этой конкретной странице.</span><span class="sxs-lookup"><span data-stu-id="477c6-200">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Раздел Возможности" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   <span data-ttu-id="477c6-202">Раздел **Возможности**</span><span class="sxs-lookup"><span data-stu-id="477c6-202">The **Opportunities** section</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-203">Выберите возможность узнать больше об этом.</span><span class="sxs-lookup"><span data-stu-id="477c6-203">Choose an opportunity to learn more about it.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Исключить возможность блокировки ресурсов отрисовки" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   <span data-ttu-id="477c6-205">**Исключить возможность блокировки ресурсов отрисовки**</span><span class="sxs-lookup"><span data-stu-id="477c6-205">**Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-206">Узнайте **больше,** чтобы отобразить документацию о том, почему важна возможность, и рекомендации по ее устранению.</span><span class="sxs-lookup"><span data-stu-id="477c6-206">Choose **Learn More** to display documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Документация по возможности устранения ресурсов, блокирующих отрисовки" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   <span data-ttu-id="477c6-208">Документация по возможности **устранения ресурсов, блокирующих отрисовки**</span><span class="sxs-lookup"><span data-stu-id="477c6-208">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-209">В **разделе Диагностика** содержится больше сведений о факторах, влияющих на время загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-209">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Раздел Диагностика" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   <span data-ttu-id="477c6-211">Раздел **Диагностика**</span><span class="sxs-lookup"><span data-stu-id="477c6-211">The **Diagnostics** section</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-212">В **разделе Пройденные аудиты** показано, что сайт делает правильно.</span><span class="sxs-lookup"><span data-stu-id="477c6-212">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="477c6-213">Выберите для расширения раздела.</span><span class="sxs-lookup"><span data-stu-id="477c6-213">Choose to expand the section.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Раздел Пройденные аудиты" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   <span data-ttu-id="477c6-215">Раздел **Пройденные аудиты**</span><span class="sxs-lookup"><span data-stu-id="477c6-215">The **Passed Audits** section</span></span>  
:::image-end:::  

## <a name="step-2-experiment"></a><span data-ttu-id="477c6-216">Шаг 2. Эксперимент</span><span class="sxs-lookup"><span data-stu-id="477c6-216">Step 2: Experiment</span></span>  

<span data-ttu-id="477c6-217">В разделе Возможности отчета о аудите вы можете получить советы по повышению производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-217">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="477c6-218">В этом разделе реализуются рекомендуемые изменения в кодовую базу, аудит сайта после каждого изменения, чтобы оценить, как это влияет на скорость сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-218">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <a name="enable-text-compression"></a><span data-ttu-id="477c6-219">Включить сжатие текста</span><span class="sxs-lookup"><span data-stu-id="477c6-219">Enable text compression</span></span>  

<span data-ttu-id="477c6-220">В отчете говорится, что одной из главных возможностей повышения производительности страницы является предотвращение огромных сетевых полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="477c6-220">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="477c6-221">Включение сжатия текста — это возможность повысить производительность страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-221">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="477c6-222">Сжатие текста — это уменьшение или сжатие размера текстового файла перед отправкой его по сети.</span><span class="sxs-lookup"><span data-stu-id="477c6-222">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="477c6-223">Аналогично тому, как можно архивировать каталог перед отправкой, чтобы уменьшить размер.</span><span class="sxs-lookup"><span data-stu-id="477c6-223">Similar to how you may archive a directory before sending it to reduce the size.</span></span>  

<span data-ttu-id="477c6-224">Перед тем как включить сжатие, ознакомьтесь с несколькими способами вручную проверить, сжаты ли текстовые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="477c6-224">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="477c6-225">Выберите средство **Network.**</span><span class="sxs-lookup"><span data-stu-id="477c6-225">Choose the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Панель Network" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       <span data-ttu-id="477c6-227">Средство **Network**</span><span class="sxs-lookup"><span data-stu-id="477c6-227">The **Network** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-228">Выберите **значок параметра Network.**</span><span class="sxs-lookup"><span data-stu-id="477c6-228">Choose the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="477c6-229">Выберите **почтовый ящик Use Large Request Rows.**</span><span class="sxs-lookup"><span data-stu-id="477c6-229">Choose the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="477c6-230">Высота строк в таблице сетевых запросов увеличивается.</span><span class="sxs-lookup"><span data-stu-id="477c6-230">The height of the rows in the table of network requests increases.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Большие строки в таблице сетевых запросов" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       <span data-ttu-id="477c6-232">Большие строки в таблице сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="477c6-232">Large rows in the network requests table</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-233">Если **столбец Размер** в таблице сетевых запросов не отображается, выберите заглавную таблицу > **Размер**.</span><span class="sxs-lookup"><span data-stu-id="477c6-233">If the **Size** column in the table of network requests is not displayed, choose the table header > **Size**.</span></span>  

<span data-ttu-id="477c6-234">Каждая **ячейка Size** отображает два значения.</span><span class="sxs-lookup"><span data-stu-id="477c6-234">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="477c6-235">Верхнее значение — размер загруженного ресурса.</span><span class="sxs-lookup"><span data-stu-id="477c6-235">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="477c6-236">Нижнее значение — это размер ненапечатаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="477c6-236">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="477c6-237">Если эти два значения одинаковы, ресурс не сжимается, когда он отправляется по сети.</span><span class="sxs-lookup"><span data-stu-id="477c6-237">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="477c6-238">Например, на предыдущем рисунке верхние и нижние значения `bundle.js` для них `1.2 MB` и `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="477c6-238">For example, in the previous figure, the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="477c6-239">Проверьте сжатие, проверив http-заготки ресурса:</span><span class="sxs-lookup"><span data-stu-id="477c6-239">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="477c6-240">Выберите `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="477c6-240">Choose `bundle.js`.</span></span>  
1.  <span data-ttu-id="477c6-241">Выберите панель **загона.**</span><span class="sxs-lookup"><span data-stu-id="477c6-241">Choose the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Панель "Заготки"" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       <span data-ttu-id="477c6-243">Панель **"Заготки"**</span><span class="sxs-lookup"><span data-stu-id="477c6-243">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-244">Поиск раздела **Заглавные ответы** для `content-encoding` загона.</span><span class="sxs-lookup"><span data-stu-id="477c6-244">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="477c6-245">Заголовки `content-encoding` не отображаются, что означает, `bundle.js` что не было сжато.</span><span class="sxs-lookup"><span data-stu-id="477c6-245">A `content-encoding` heading is not displayed, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="477c6-246">При сжатии ресурса этот заглавный загот обычно задатки `gzip` , `deflate` или `br` .</span><span class="sxs-lookup"><span data-stu-id="477c6-246">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="477c6-247">Для объяснения значений перейдите к [Директивам.][MDNContentEncodingDirectives]</span><span class="sxs-lookup"><span data-stu-id="477c6-247">For an explanation of the values, navigate to [Directives][MDNContentEncodingDirectives].</span></span>  

<span data-ttu-id="477c6-248">Достаточно объяснений.</span><span class="sxs-lookup"><span data-stu-id="477c6-248">Enough with the explanations.</span></span>  <span data-ttu-id="477c6-249">Время внести некоторые изменения.</span><span class="sxs-lookup"><span data-stu-id="477c6-249">Time to make some changes.</span></span>  <span data-ttu-id="477c6-250">Включить сжатие текста, добавив несколько строк кода:</span><span class="sxs-lookup"><span data-stu-id="477c6-250">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="477c6-251">На вкладке редактор выберите **server.js**.</span><span class="sxs-lookup"><span data-stu-id="477c6-251">In the editor tab, choose **server.js**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Изменение server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       <span data-ttu-id="477c6-253">Edit</span><span class="sxs-lookup"><span data-stu-id="477c6-253">Edit</span></span> `server.js`  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-254">Добавьте следующий код в \*\*server.js. \*\*</span><span class="sxs-lookup"><span data-stu-id="477c6-254">Add the following code to **server.js**.</span></span>  <span data-ttu-id="477c6-255">Убедитесь, что поставить `app.use(compression())` перед `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="477c6-255">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="477c6-256">Обычно, вы должны установить пакет `compression` с помощью что-то `npm i -S compression` вроде, но это уже было сделано для вас.</span><span class="sxs-lookup"><span data-stu-id="477c6-256">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="477c6-257">Подождите, пока глюк развернет новую сборку сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-257">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="477c6-258">Фантазия анимации рядом с **Инструменты** означает, что сайт перестроен и передиплоен.</span><span class="sxs-lookup"><span data-stu-id="477c6-258">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="477c6-259">Изменение готово, когда анимация рядом с **Инструменты** уходит.</span><span class="sxs-lookup"><span data-stu-id="477c6-259">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="477c6-260">Выберите **Показать** и **снова выбрать в новом окне.**</span><span class="sxs-lookup"><span data-stu-id="477c6-260">Choose **Show** and choose **In a New Window** again.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
<span data-ttu-id="477c6-261">Используйте рабочие процессы, которые вы узнали ранее, чтобы вручную проверить, работает ли сжатие:</span><span class="sxs-lookup"><span data-stu-id="477c6-261">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="477c6-262">Возвращайся на вкладку демонстрации и обнови страницу.</span><span class="sxs-lookup"><span data-stu-id="477c6-262">Go back to the demo tab and refresh the page.</span></span>  <span data-ttu-id="477c6-263">Столбец **Размер** теперь должен показывать 2 различных значения для текстовых ресурсов, таких как `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="477c6-263">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="477c6-264">На рисунке ниже верхнее значение для — размер файла, отправленного по сети, а нижним значением является `256 KB` `bundle.js` ненапечатаный размер `1.2 MB` файла.</span><span class="sxs-lookup"><span data-stu-id="477c6-264">In the figure after the following, the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="В столбце Размер теперь показаны 2 различных значения для текстовых ресурсов" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       <span data-ttu-id="477c6-266">В **столбце Размер** теперь показаны 2 различных значения для текстовых ресурсов</span><span class="sxs-lookup"><span data-stu-id="477c6-266">The **Size** column now shows 2 different values for text resources</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-267">Раздел **Заглавные ответы** теперь `bundle.js` должен включать `content-encoding: gzip` заглавную.</span><span class="sxs-lookup"><span data-stu-id="477c6-267">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="В разделе Заглавные ответы теперь содержится заготчик коди-кодинга контента" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       <span data-ttu-id="477c6-269">В **разделе Заглавные ответы** теперь содержится заготчик коди-кодинга контента</span><span class="sxs-lookup"><span data-stu-id="477c6-269">The **Response Headers** section now contains a content-encoding header</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-270">Проверь страницу еще раз, чтобы оценить, какое влияние оказывает сжатие текста на производительность нагрузки страницы:</span><span class="sxs-lookup"><span data-stu-id="477c6-270">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="477c6-271">Выберите средство **аудита.**</span><span class="sxs-lookup"><span data-stu-id="477c6-271">Choose the **Audits** tool.</span></span>  
1.  <span data-ttu-id="477c6-272">Выберите **Выполнение аудита** \. ![ Выполните аудит ][ImagePerformIcon] \).</span><span class="sxs-lookup"><span data-stu-id="477c6-272">Choose **Perform an audit** \(![Perform an audit][ImagePerformIcon]\).</span></span>  
1.  <span data-ttu-id="477c6-273">Оставьте параметры так же, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="477c6-273">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="477c6-274">Выберите **аудит Run**.</span><span class="sxs-lookup"><span data-stu-id="477c6-274">Choose **Run audit**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Отчет аудита после включения сжатия текста" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       <span data-ttu-id="477c6-276">Отчет аудита после включения сжатия текста</span><span class="sxs-lookup"><span data-stu-id="477c6-276">An Audits report after enabling text compression</span></span>  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  <span data-ttu-id="477c6-277">Общий показатель производительности должен был увеличиться, а это значит, что сайт становится быстрее.</span><span class="sxs-lookup"><span data-stu-id="477c6-277">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <a name="text-compression-in-the-real-world"></a><span data-ttu-id="477c6-278">Сжатие текста в реальном мире</span><span class="sxs-lookup"><span data-stu-id="477c6-278">Text compression in the real world</span></span>  

<span data-ttu-id="477c6-279">Большинство серверов действительно имеют простые исправления, такие как это для включения сжатия!</span><span class="sxs-lookup"><span data-stu-id="477c6-279">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="477c6-280">Просто сделайте поиск о том, как настроить любой сервер, который используется для сжатия текста.</span><span class="sxs-lookup"><span data-stu-id="477c6-280">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <a name="resize-images"></a><span data-ttu-id="477c6-281">Resize images</span><span class="sxs-lookup"><span data-stu-id="477c6-281">Resize images</span></span>  

<span data-ttu-id="477c6-282">В отчете указывается, что одной из главных возможностей повышения производительности страницы является предотвращение огромных сетевых полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="477c6-282">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="477c6-283">Размер изображений позволяет уменьшить размер полезной нагрузки сети.</span><span class="sxs-lookup"><span data-stu-id="477c6-283">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="477c6-284">Если пользователь просматривает изображения на экране мобильного устройства шириной 500 пикселей, отправка изображения шириной 1500 пикселей не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="477c6-284">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="477c6-285">В идеале вы отправляете не более 500 пикселей изображения.</span><span class="sxs-lookup"><span data-stu-id="477c6-285">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="477c6-286">В отчете выберите **Избегать огромных сетевых** полезной нагрузки для отображения изображений, которые следует повторно использовать.</span><span class="sxs-lookup"><span data-stu-id="477c6-286">In your report, choose **Avoid enormous network payloads** to display which images should be resized.</span></span>  <span data-ttu-id="477c6-287">Похоже, что 2 из jpg-файлов более 2000 КБ, что больше, чем необходимо.</span><span class="sxs-lookup"><span data-stu-id="477c6-287">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="477c6-288">Возвращаясь на вкладку редактора, откройте `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="477c6-288">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="477c6-289">Замените `const dir = 'big'` `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="477c6-289">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="477c6-290">Этот каталог содержит копии тех же изображений, которые были повторно размера.</span><span class="sxs-lookup"><span data-stu-id="477c6-290">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="477c6-291">Снова проверь страницу, чтобы показать, как изменение влияет на производительность нагрузки.</span><span class="sxs-lookup"><span data-stu-id="477c6-291">Audit the page again to display how the change affects load performance.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Отчет аудита после повторного размеров изображений" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       <span data-ttu-id="477c6-293">Отчет аудита после повторного размеров изображений</span><span class="sxs-lookup"><span data-stu-id="477c6-293">An Audits report after resizing images</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-294">Отображаемая перемена имеет незначительное влияние на общую оценку производительности.</span><span class="sxs-lookup"><span data-stu-id="477c6-294">The change displays only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="477c6-295">Однако одна вещь, которая не показывает четко, это то, сколько сетевых данных вы экономите пользователей.</span><span class="sxs-lookup"><span data-stu-id="477c6-295">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="477c6-296">Общий размер старых фотографий составил около 5,3 мегабайт, в то время как сейчас он составляет всего 0,18 мегабайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-296">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <a name="resizing-images-in-the-real-world"></a><span data-ttu-id="477c6-297">Размер изображений в реальном мире</span><span class="sxs-lookup"><span data-stu-id="477c6-297">Resizing images in the real world</span></span>  

<span data-ttu-id="477c6-298">Для небольшого приложения сделать разовую размер, как это может быть достаточно хорошо.</span><span class="sxs-lookup"><span data-stu-id="477c6-298">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="477c6-299">Но для большого приложения это, очевидно, не масштабируемо.</span><span class="sxs-lookup"><span data-stu-id="477c6-299">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="477c6-300">Вот некоторые стратегии управления изображениями в крупных приложениях:</span><span class="sxs-lookup"><span data-stu-id="477c6-300">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="477c6-301">Resize images during your build process.</span><span class="sxs-lookup"><span data-stu-id="477c6-301">Resize images during your build process.</span></span>  
*   <span data-ttu-id="477c6-302">Создайте несколько размеров каждого изображения в процессе сборки и используйте `srcset` в коде.</span><span class="sxs-lookup"><span data-stu-id="477c6-302">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="477c6-303">При запуске браузер принимает решение о том, какой размер лучше всего для устройства.</span><span class="sxs-lookup"><span data-stu-id="477c6-303">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="477c6-304">Используйте CDN изображения, который позволяет динамически реамизировать изображение при его запросе.</span><span class="sxs-lookup"><span data-stu-id="477c6-304">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="477c6-305">По крайней мере, оптимизируйте каждое изображение.</span><span class="sxs-lookup"><span data-stu-id="477c6-305">At the very least, optimize each image.</span></span>  <span data-ttu-id="477c6-306">Это может создать огромную экономию.</span><span class="sxs-lookup"><span data-stu-id="477c6-306">This may create huge savings.</span></span>  
  <span data-ttu-id="477c6-307">Оптимизация — это при запуске изображения через специальную программу, которая уменьшает размер файла изображений.</span><span class="sxs-lookup"><span data-stu-id="477c6-307">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="477c6-308">Дополнительные советы, перейдите к [существенной оптимизации изображения][EssentialImageOptimization].</span><span class="sxs-lookup"><span data-stu-id="477c6-308">For more tips, navigate to [Essential Image Optimization][EssentialImageOptimization].</span></span>  
    
### <a name="eliminate-render-blocking-resources"></a><span data-ttu-id="477c6-309">Устранение ресурсов, блокирующих рендеринг</span><span class="sxs-lookup"><span data-stu-id="477c6-309">Eliminate render-blocking resources</span></span>  

<span data-ttu-id="477c6-310">В последнем отчете говорится, что устранение ресурсов, блокирующих рендеринг, теперь является самой большой возможностью.</span><span class="sxs-lookup"><span data-stu-id="477c6-310">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="477c6-311">Ресурс, блокирующий отрисовку, — это внешний файл JavaScript или CSS, который браузер должен скачать, разбрасировать и запустить до отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-311">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="477c6-312">Цель состоит в том, чтобы выполнить только основной код CSS и JavaScript, необходимый для правильного отображения страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-312">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="477c6-313">Первой задачей является поиск кода, который не требуется запускать на странице нагрузки.</span><span class="sxs-lookup"><span data-stu-id="477c6-313">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="477c6-314">Выберите **исключить ресурсы, блокирующие отрисовки,** чтобы отобразить заблокированные ресурсы:</span><span class="sxs-lookup"><span data-stu-id="477c6-314">Choose **Eliminate render-blocking resources** to display the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="477c6-315">и `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="477c6-315">and `jquery.js`.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Дополнительные сведения о возможности устранения ресурсов, блокирующих отрисовки" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       <span data-ttu-id="477c6-317">Дополнительные сведения о возможности **устранения ресурсов, блокирующих отрисовки**</span><span class="sxs-lookup"><span data-stu-id="477c6-317">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-318">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) `Coverage` \*\*\*\* для открытия командного меню, начала ввода, а затем выберите Показать покрытие .</span><span class="sxs-lookup"><span data-stu-id="477c6-318">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then choose **Show Coverage**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Откройте меню команд из панели Аудиты" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       <span data-ttu-id="477c6-320">Откройте меню команд из панели **Аудиты**</span><span class="sxs-lookup"><span data-stu-id="477c6-320">Open the Command Menu from the **Audits** panel</span></span>  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="Средство Coverage" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       <span data-ttu-id="477c6-322">Средство **Coverage**</span><span class="sxs-lookup"><span data-stu-id="477c6-322">The **Coverage** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-323">Выберите **обновление** \. ![ Обновление ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="477c6-323">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="477c6-324">Средство **Coverage** предоставляет обзор того, сколько кода в , и запускается во время `bundle.js` `jquery.js` `lodash.js` загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-324">The **Coverage** tool provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="477c6-325">На следующем рисунке не используется соответственно около 76% и 30% файлов jQuery и Lodash.</span><span class="sxs-lookup"><span data-stu-id="477c6-325">In the figure after the following, about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="Отчет По охвату" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       <span data-ttu-id="477c6-327">Отчет По охвату</span><span class="sxs-lookup"><span data-stu-id="477c6-327">The Coverage report</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-328">Выберите **строкуjquery.js.**</span><span class="sxs-lookup"><span data-stu-id="477c6-328">Choose the **jquery.js** row.</span></span>  <span data-ttu-id="477c6-329">DevTools открывает файл в панели Источники.</span><span class="sxs-lookup"><span data-stu-id="477c6-329">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="477c6-330">Строка кода побежала, если рядом с ней имеется синяя строка.</span><span class="sxs-lookup"><span data-stu-id="477c6-330">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="477c6-331">Красная планка означает, что она не была запускаться и определенно не требуется для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-331">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Просмотр файла jQuery в панели Источники" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       <span data-ttu-id="477c6-333">Просмотр файла jQuery в панели **Источники**</span><span class="sxs-lookup"><span data-stu-id="477c6-333">Viewing the jQuery file in the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-334">Прокрутите код jQuery немного.</span><span class="sxs-lookup"><span data-stu-id="477c6-334">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="477c6-335">Некоторые строки, которые получают "запустить" на самом деле просто комментарии.</span><span class="sxs-lookup"><span data-stu-id="477c6-335">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="477c6-336">Запуск этого кода через мини-файл, который полосы комментариев является еще одним способом уменьшить размер этого файла.</span><span class="sxs-lookup"><span data-stu-id="477c6-336">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="477c6-337">Короче говоря, при работе с собственным кодом средство **Coverage** помогает анализировать код, строку за строкой и только отгрузку кода, необходимого для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-337">In short, when you are working with your own code, the **Coverage** tool helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="477c6-338">Нужны ли файлы и файлы `jquery.js` `lodash.js` для загрузки страницы?</span><span class="sxs-lookup"><span data-stu-id="477c6-338">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="477c6-339">Средство **блокировки** запроса отображает, что происходит, когда ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="477c6-339">The **Request blocking** tool displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="477c6-340">Выберите средство **Network.**</span><span class="sxs-lookup"><span data-stu-id="477c6-340">Choose the **Network** tool.</span></span>  
1.  <span data-ttu-id="477c6-341">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для повторного открытия командного меню.</span><span class="sxs-lookup"><span data-stu-id="477c6-341">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="477c6-342">Начните `blocking` вводить текст, а затем **выберите блокировку запроса на показ.**</span><span class="sxs-lookup"><span data-stu-id="477c6-342">Start typing `blocking` and then choose **Show Request Blocking**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="Средство блокировки запроса" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       <span data-ttu-id="477c6-344">Средство **блокировки запроса**</span><span class="sxs-lookup"><span data-stu-id="477c6-344">The **Request blocking** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-345">Выберите **Добавить шаблон** \. Добавьте шаблон ![ ][ImageAddPatternIcon] \), введите , а затем `/libs/*` `Enter` выберите, чтобы подтвердить.</span><span class="sxs-lookup"><span data-stu-id="477c6-345">Choose **Add Pattern** \(![Add Pattern][ImageAddPatternIcon]\), type `/libs/*`, and then select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Добавление шаблона для блокировки любого запроса в каталог libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="477c6-347">Добавление шаблона для блокировки любого запроса `libs` в каталог</span><span class="sxs-lookup"><span data-stu-id="477c6-347">Add a pattern to block any request to the `libs` directory</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-348">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="477c6-348">Refresh the page.</span></span>  <span data-ttu-id="477c6-349">Запросы jQuery и Lodash являются красными, что означает, что запросы были заблокированы.</span><span class="sxs-lookup"><span data-stu-id="477c6-349">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="477c6-350">Страница по-прежнему загружается и является интерактивной, поэтому похоже, что эти ресурсы вообще не нужны!</span><span class="sxs-lookup"><span data-stu-id="477c6-350">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="Панель Network показывает, что запросы были заблокированы" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       <span data-ttu-id="477c6-352">Средство **Network** показывает, что запросы заблокированы</span><span class="sxs-lookup"><span data-stu-id="477c6-352">The **Network** tool shows that the requests have been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-353">Выберите **Удалить все шаблоны** \. Удалите все ![ шаблоны ][ImageRemoveIcon] \) для удаления `/libs/*` шаблона блокировки.</span><span class="sxs-lookup"><span data-stu-id="477c6-353">Choose **Remove all patterns** \(![Remove all patterns][ImageRemoveIcon]\) to delete the `/libs/*` blocking pattern.</span></span>  
    
<span data-ttu-id="477c6-354">Как правило, средство блокировки **запроса** полезно для моделирования поведения страницы, если какой-либо ресурс не доступен.</span><span class="sxs-lookup"><span data-stu-id="477c6-354">In general, the **Request blocking** tool is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="477c6-355">Теперь удалите ссылки на эти файлы из кода и снова проверите страницу:</span><span class="sxs-lookup"><span data-stu-id="477c6-355">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="477c6-356">Возвращаясь на вкладку редактора, откройте `template.html` .</span><span class="sxs-lookup"><span data-stu-id="477c6-356">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="477c6-357">Удалите `<script src="/libs/lodash.js">` и `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="477c6-357">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="477c6-358">Дождись повторной сборки и повторного развертывания сайта.</span><span class="sxs-lookup"><span data-stu-id="477c6-358">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="477c6-359">Снова аудит страницы из средства **аудита.**</span><span class="sxs-lookup"><span data-stu-id="477c6-359">Audit the page again from the **Audits** tool.</span></span>  <span data-ttu-id="477c6-360">Ваш общий результат должен был улучшиться снова.</span><span class="sxs-lookup"><span data-stu-id="477c6-360">Your overall score should have improved again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Отчет аудита после удаления ресурсов, блокирующих рендеринг" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       <span data-ttu-id="477c6-362">Отчет **аудита** после удаления ресурсов, блокирующих рендеринг</span><span class="sxs-lookup"><span data-stu-id="477c6-362">An **Audits** report after removing the render-blocking resources</span></span>  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a><span data-ttu-id="477c6-363">Оптимизация пути критической визуализации в реальном мире</span><span class="sxs-lookup"><span data-stu-id="477c6-363">Optimizing the Critical Rendering Path in the real-world</span></span>  

<span data-ttu-id="477c6-364">Путь **критической визуализации** относится к коду, необходимому для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-364">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="477c6-365">В общем, ускорять загрузку страницы, только отгрузка критического кода во время загрузки страницы, а затем ленивая загрузка всего остального.</span><span class="sxs-lookup"><span data-stu-id="477c6-365">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="477c6-366">Маловероятно, что вы сможете найти сценарии, которые можно удалить прямо, но вы можете найти много скриптов, которые вам не нужно запрашивать во время загрузки страницы, а вместо этого может быть запротезировали асинхронно.</span><span class="sxs-lookup"><span data-stu-id="477c6-366">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--Navigate to [Using async or defer][async].  -->  
*   <span data-ttu-id="477c6-367">Если вы используете фреймворк, проверьте, есть ли в нем режим производства.</span><span class="sxs-lookup"><span data-stu-id="477c6-367">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="477c6-368">Этот режим может использовать [][WebpackTreeShaking] такую функцию, как встряхивания дерева, чтобы исключить ненужный код, блокирующий критически важную отрисовку.</span><span class="sxs-lookup"><span data-stu-id="477c6-368">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a><span data-ttu-id="477c6-369">Меньше работы основного потока</span><span class="sxs-lookup"><span data-stu-id="477c6-369">Do less main thread work</span></span>  

<span data-ttu-id="477c6-370">В последнем отчете показано некоторое незначительное потенциальное сэкономление в разделе Возможности, но если вы посмотрите вниз в разделе Диагностика, то, похоже, что самое большое узким местом является слишком большая активность основного потока.</span><span class="sxs-lookup"><span data-stu-id="477c6-370">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="477c6-371">Основной поток — это то, что браузер делает большую часть работы, необходимой для отображения страницы, например для размыва и запуска HTML, CSS и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="477c6-371">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="477c6-372">Цель состоит в том, чтобы использовать панель Performance для анализа работы основного потока во время загрузки страницы, а также поиска способов отложить или удалить ненужные работы.</span><span class="sxs-lookup"><span data-stu-id="477c6-372">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="477c6-373">Выберите **средство Performance.**</span><span class="sxs-lookup"><span data-stu-id="477c6-373">Choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="477c6-374">Выберите **Параметры захвата** \. ![ Параметры захвата ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="477c6-374">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>  
1.  <span data-ttu-id="477c6-375">Установите **сеть** для **замедления 3G** и **ЦП** до **замедления 6x**.</span><span class="sxs-lookup"><span data-stu-id="477c6-375">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="477c6-376">Мобильные устройства обычно имеют больше ограничений оборудования, чем ноутбуки или настольные компьютеры, поэтому эти параметры позволяет испытывать нагрузку на страницу, как если бы вы использовали менее мощное устройство.</span><span class="sxs-lookup"><span data-stu-id="477c6-376">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="477c6-377">Выберите **обновление** \. ![ Обновление ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="477c6-377">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="477c6-378">DevTools обновляет страницу, а затем создает визуализацию всей работы, выполняемой для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-378">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="477c6-379">Эта визуализация называется **трассировка**.</span><span class="sxs-lookup"><span data-stu-id="477c6-379">This visualization is referred to as the **trace**.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Трассировка средства Performance для загрузки страницы" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       <span data-ttu-id="477c6-381">**Трассировка** средства Performance для загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="477c6-381">The **Performance** tool trace of the page load</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-382">Трассировка показывает активность в хронологическом порядке, слева направо.</span><span class="sxs-lookup"><span data-stu-id="477c6-382">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="477c6-383">Диаграммы FPS, CPU и NET в верхней части дают обзор кадров в секунду, активности ЦП и сетевой активности.</span><span class="sxs-lookup"><span data-stu-id="477c6-383">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="477c6-384">Блок желтого цвета, выделенный на рисунке после следующего, ЦП был полностью занят действиями скриптов.</span><span class="sxs-lookup"><span data-stu-id="477c6-384">The block of yellow highlighted in the figure after the next, the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="477c6-385">Это подсказка о том, что вы можете ускорить загрузку страниц, делая меньше работы с JavaScript.</span><span class="sxs-lookup"><span data-stu-id="477c6-385">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="Раздел Обзор трассировки" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   <span data-ttu-id="477c6-387">Раздел Обзор трассировки</span><span class="sxs-lookup"><span data-stu-id="477c6-387">The Overview section of the trace</span></span>  
:::image-end:::  

<span data-ttu-id="477c6-388">Изучите след, чтобы найти способы сделать меньше работы JavaScript:</span><span class="sxs-lookup"><span data-stu-id="477c6-388">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="477c6-389">Чтобы расширить его, выберите раздел **Timings.**</span><span class="sxs-lookup"><span data-stu-id="477c6-389">Choose the **Timings** section to expand it.</span></span>  <span data-ttu-id="477c6-390">Основываясь на том, что может быть куча мер [Timings][MDNUserTimingApi] от React, кажется, что приложение Тони использует режим разработки React.</span><span class="sxs-lookup"><span data-stu-id="477c6-390">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="477c6-391">Переход на производственный режим React может привести к некоторому простому выигрышу производительности.</span><span class="sxs-lookup"><span data-stu-id="477c6-391">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Раздел Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       <span data-ttu-id="477c6-393">Раздел **Timings**</span><span class="sxs-lookup"><span data-stu-id="477c6-393">The **Timings** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-394">Снова **выберите Тайминги,** чтобы свернуть этот раздел.</span><span class="sxs-lookup"><span data-stu-id="477c6-394">Choose **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="477c6-395">Просмотрите **раздел Main.**</span><span class="sxs-lookup"><span data-stu-id="477c6-395">Browse the **Main** section.</span></span>  <span data-ttu-id="477c6-396">В этом разделе показан хронологический журнал основной активности потока слева направо.</span><span class="sxs-lookup"><span data-stu-id="477c6-396">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="477c6-397">Y-axis (сверху вниз) показывает, почему произошли события.</span><span class="sxs-lookup"><span data-stu-id="477c6-397">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="477c6-398">Например, в figyre после следующего события, событие вызвало функцию для запуска, что вызвало запуск, что вызвало `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` запуск, и так далее.</span><span class="sxs-lookup"><span data-stu-id="477c6-398">For example, in the figyre after the following, the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Основной раздел" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       <span data-ttu-id="477c6-400">Основной \*\*\*\* раздел</span><span class="sxs-lookup"><span data-stu-id="477c6-400">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="477c6-401">Прокрутите вниз в нижней части **основного** раздела.</span><span class="sxs-lookup"><span data-stu-id="477c6-401">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="477c6-402">При использовании фреймворка большая часть верхней активности вызвана рамками, которые обычно находятся вне вашего контроля.</span><span class="sxs-lookup"><span data-stu-id="477c6-402">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="477c6-403">Действие, вызываемая вашим приложением, обычно находится в нижней части.</span><span class="sxs-lookup"><span data-stu-id="477c6-403">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="477c6-404">В этом приложении кажется, что функция с именем вызывает большое количество запросов `App` для `mineBitcoin` функции.</span><span class="sxs-lookup"><span data-stu-id="477c6-404">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="477c6-405">Похоже, Тони может использовать устройства своих поклонников для майнинга криптовалюты...</span><span class="sxs-lookup"><span data-stu-id="477c6-405">It sounds like Tony may be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Наведите курсор на действие mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       <span data-ttu-id="477c6-407">Наведите курсор `mineBitcoin` на действие</span><span class="sxs-lookup"><span data-stu-id="477c6-407">Hover on the `mineBitcoin` activity</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="477c6-408">Несмотря на то, что запросы, которые делает ваша структура, обычно не под вашим контролем, иногда вы можете структурировать приложение таким образом, что это приводит к неэффективному запуску фреймворка.</span><span class="sxs-lookup"><span data-stu-id="477c6-408">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="477c6-409">Реструктуризация приложения для эффективного использования фреймворка — это способ сделать меньше основной работы потока.</span><span class="sxs-lookup"><span data-stu-id="477c6-409">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="477c6-410">Однако для этого требуется глубокое понимание того, как работает ваша структура, и какие изменения вы вносяте в собственный код для более эффективного использования фреймворка.</span><span class="sxs-lookup"><span data-stu-id="477c6-410">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  
    
1.  <span data-ttu-id="477c6-411">**Расширь раздел Bottom-Up.**</span><span class="sxs-lookup"><span data-stu-id="477c6-411">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="477c6-412">Эта вкладка разбивает, какие действия заняли больше всего времени.</span><span class="sxs-lookup"><span data-stu-id="477c6-412">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="477c6-413">Если в разделе Bottom-Up ничего не отображается, выберите метку для **раздела Main.**</span><span class="sxs-lookup"><span data-stu-id="477c6-413">If nothing is displayed in the Bottom-Up section, choose the label for **Main** section.</span></span>  <span data-ttu-id="477c6-414">В **разделе Bottom-Up** показаны только сведения о любых действиях или группах действий, выбранных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="477c6-414">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="477c6-415">Например, если вы выбрали одно из действий, в разделе Bottom-Up будут показываться только сведения `mineBitcoin` об этом одном действии. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="477c6-415">For example, if you chose one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="Вкладка Bottom-Up" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       <span data-ttu-id="477c6-417">Вкладка **Bottom-Up**</span><span class="sxs-lookup"><span data-stu-id="477c6-417">The **Bottom-Up** tab</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-418">Столбец **Self Time** показывает, сколько времени было затрачено непосредственно в каждом действии.</span><span class="sxs-lookup"><span data-stu-id="477c6-418">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="477c6-419">Например, на следующую цифру было потрачено около 63% основного времени потока на `mineBitcoin` функцию.</span><span class="sxs-lookup"><span data-stu-id="477c6-419">For example, in the following figure, about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="477c6-420">Время для проверки того, может ли использование режима производства и снижение активности JavaScript ускорить загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-420">Time to review whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="477c6-421">Начните с режима производства:</span><span class="sxs-lookup"><span data-stu-id="477c6-421">Start with production mode:</span></span>  

1.  <span data-ttu-id="477c6-422">На вкладке редактор откройте `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="477c6-422">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="477c6-423">Изменение `"mode":"development"` в `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="477c6-423">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="477c6-424">Подождите развертывание новой сборки.</span><span class="sxs-lookup"><span data-stu-id="477c6-424">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="477c6-425">Снова аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-425">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Отчет аудита после настройки вебпака для использования режима производства" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       <span data-ttu-id="477c6-427">Отчет аудита после настройки вебпака для использования режима производства</span><span class="sxs-lookup"><span data-stu-id="477c6-427">An Audits report after configuring webpack to use production mode</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-428">Уменьшите активность JavaScript, удалив запрос `mineBitcoin` на:</span><span class="sxs-lookup"><span data-stu-id="477c6-428">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="477c6-429">На вкладке редактор откройте `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="477c6-429">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="477c6-430">Комментарий `this.mineBitcoin(1500)` запроса в `constructor` .</span><span class="sxs-lookup"><span data-stu-id="477c6-430">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="477c6-431">Подождите развертывание новой сборки.</span><span class="sxs-lookup"><span data-stu-id="477c6-431">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="477c6-432">Снова аудит страницы.</span><span class="sxs-lookup"><span data-stu-id="477c6-432">Audit the page again.</span></span>  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Отчет аудита после удаления ненужной работы JavaScript" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       <span data-ttu-id="477c6-434">Отчет аудита после удаления ненужной работы JavaScript</span><span class="sxs-lookup"><span data-stu-id="477c6-434">An Audits report after removing unnecessary JavaScript work</span></span>  
    :::image-end:::  
    
<span data-ttu-id="477c6-435">Похоже, что последнее изменение вызвало массовый скачок производительности!</span><span class="sxs-lookup"><span data-stu-id="477c6-435">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="477c6-436">В этом разделе представлено краткое введение в панель Performance.</span><span class="sxs-lookup"><span data-stu-id="477c6-436">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="477c6-437">Дополнительные данные о том, как анализировать производительность страниц, перейдите к ссылке [на анализ производительности.][DevtoolsEvaluatePerformanceReference]</span><span class="sxs-lookup"><span data-stu-id="477c6-437">To learn more about how to analyze page performance, navigate to [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference].</span></span>  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a><span data-ttu-id="477c6-438">Работа с меньшим количеством основных потоков в реальном мире</span><span class="sxs-lookup"><span data-stu-id="477c6-438">Doing less main thread work in the real world</span></span>  

<span data-ttu-id="477c6-439">В общем, средство **Performance** — это наиболее распространенный способ понять, какие действия ваш сайт делает при загрузке, и найти способы удаления ненужных действий.</span><span class="sxs-lookup"><span data-stu-id="477c6-439">In general, the **Performance** tool is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="477c6-440">Если вы предпочитаете более похожий `console.log()` подход, [API][MDNUserTimingApi] времени пользователя позволяет произвольно отмечать определенные этапы жизненного цикла приложения, чтобы отслеживать, сколько времени занимает каждый из этих этапов.</span><span class="sxs-lookup"><span data-stu-id="477c6-440">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <a name="summary"></a><span data-ttu-id="477c6-441">Сводка</span><span class="sxs-lookup"><span data-stu-id="477c6-441">Summary</span></span>  

*   <span data-ttu-id="477c6-442">Всякий раз, когда вы затеяли оптимизацию производительности загрузки сайта, всегда начните с аудита.</span><span class="sxs-lookup"><span data-stu-id="477c6-442">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="477c6-443">Аудит устанавливает базовый уровень и дает советы по улучшению.</span><span class="sxs-lookup"><span data-stu-id="477c6-443">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="477c6-444">Внося по одному изменение за раз и проверяя веб-страницу после каждого изменения, чтобы отобразить, как это изолированное изменение влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="477c6-444">Make one change at a time, and audit the webpage after each change in order to display how that isolated change affects performance.</span></span>  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="477c6-445">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="477c6-445">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Справочные ссылки | Документы Майкрософт"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Введение в класс веб-разработки | Coursera"  

[EssentialImageOptimization]: https://images.guide "Необходимая оптимизация изображений"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Директивы — кодиро-кодиро-| MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API времени пользователя | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Встряхивания | webpack"  

> [!NOTE]
> <span data-ttu-id="477c6-452">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="477c6-452">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="477c6-453">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="477c6-453">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="477c6-455">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="477c6-455">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
