---
description: Учебник по наиболее популярным сетевым функциям в Microsoft Edge DevTools.
title: Проверка сетевой активности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 16b60716c91d2f4ce778f1fac37afc0e73e30ab6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398660"
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

# <a name="inspect-network-activity-in-microsoft-edge-devtools"></a><span data-ttu-id="0e88b-104">Проверка сетевой активности в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0e88b-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="0e88b-105">Это практический учебник некоторых наиболее часто используемых функций DevTools, связанных с проверкой сетевой активности страницы.</span><span class="sxs-lookup"><span data-stu-id="0e88b-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="0e88b-106">Если вы хотите просмотреть функции, перейдите к [ссылке сети][DevtoolsNetworkReference].</span><span class="sxs-lookup"><span data-stu-id="0e88b-106">If you want to browse features, navigate to [Network Reference][DevtoolsNetworkReference].</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <a name="when-to-use-the-network-panel"></a><span data-ttu-id="0e88b-107">Когда использовать панель Network</span><span class="sxs-lookup"><span data-stu-id="0e88b-107">When to use the Network panel</span></span>  

<span data-ttu-id="0e88b-108">В общем случае используйте панель Network, когда необходимо убедиться, что ресурсы загружаются или загружаются как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="0e88b-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="0e88b-109">Наиболее распространенными случаями использования панели Network являются:</span><span class="sxs-lookup"><span data-stu-id="0e88b-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="0e88b-110">Убедитесь, что ресурсы фактически загружаются или загружаются вообще.</span><span class="sxs-lookup"><span data-stu-id="0e88b-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="0e88b-111">Проверка свойств отдельного ресурса, таких как http-headers, контент, размер и т. д.</span><span class="sxs-lookup"><span data-stu-id="0e88b-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="0e88b-112">Если вы ищете способы повышения производительности загрузки страниц, **не начинайте** с средства **Network.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="0e88b-113">Существует множество типов проблем производительности нагрузки, не связанных с сетевой активностью.</span><span class="sxs-lookup"><span data-stu-id="0e88b-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="0e88b-114">Начните с панели Аудиты, так как она дает вам целенаправленные предложения по улучшению страницы.</span><span class="sxs-lookup"><span data-stu-id="0e88b-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="0e88b-115">Перейдите к [оптимизации скорости веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="0e88b-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <a name="open-the-network-panel"></a><span data-ttu-id="0e88b-116">Откройте панель Network</span><span class="sxs-lookup"><span data-stu-id="0e88b-116">Open the Network panel</span></span>  

<span data-ttu-id="0e88b-117">Чтобы получить больше всего от этого руководства, откройте демонстрацию и попробуйте функции на демо-странице.</span><span class="sxs-lookup"><span data-stu-id="0e88b-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="0e88b-118">Откройте [демонстрацию "Начало работы".][GlitchNetworkGetStarted]</span><span class="sxs-lookup"><span data-stu-id="0e88b-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="0e88b-120">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="0e88b-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="0e88b-121">Чтобы [открыть DevTools,][DevToolsOpen] `Control` + `Shift` + `J` выберите \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="0e88b-121">To [Open DevTools][DevToolsOpen], select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="0e88b-122">Откроется **консольный** инструмент.</span><span class="sxs-lookup"><span data-stu-id="0e88b-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Консоль" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="0e88b-124">Консоль \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e88b-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0e88b-125">Вы можете [пристыковать DevTools к нижней части окна.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="0e88b-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools, пристыкованные к нижней части окна" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="0e88b-127">DevTools, пристыкованные к нижней части окна</span><span class="sxs-lookup"><span data-stu-id="0e88b-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-128">Откройте **средство Network.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-128">Open the **Network** tool.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Консольный инструмент в DevTools, пристыкованный к нижней части окна" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="0e88b-130">**Консольный** инструмент в DevTools, пристыкованный к нижней части окна</span><span class="sxs-lookup"><span data-stu-id="0e88b-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="0e88b-131">Сейчас средство **Network** пусто.</span><span class="sxs-lookup"><span data-stu-id="0e88b-131">Right now the **Network** tool is empty.</span></span>  <span data-ttu-id="0e88b-132">DevTools регистрит сетевое действие только после его открытия, и с момента открытия DevTools сетевой активности не было.</span><span class="sxs-lookup"><span data-stu-id="0e88b-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <a name="log-network-activity"></a><span data-ttu-id="0e88b-133">Сетевое действие журнала</span><span class="sxs-lookup"><span data-stu-id="0e88b-133">Log network activity</span></span>  

<span data-ttu-id="0e88b-134">Чтобы просмотреть сетевое действие, которое вызывает страница:</span><span class="sxs-lookup"><span data-stu-id="0e88b-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="0e88b-135">Обновление веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="0e88b-135">Refresh the webpage.</span></span>  <span data-ttu-id="0e88b-136">Панель Network регистрит все сетевые действия в **журнале Сети.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Журнал сети" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="0e88b-138">Журнал **сети**</span><span class="sxs-lookup"><span data-stu-id="0e88b-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0e88b-139">Каждая строка **сетевого журнала** представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="0e88b-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="0e88b-140">По умолчанию ресурсы перечислены в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="0e88b-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="0e88b-141">Верхний ресурс обычно является основным HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="0e88b-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="0e88b-142">Нижний ресурс — это все, что запрашивалось в последний раз.</span><span class="sxs-lookup"><span data-stu-id="0e88b-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="0e88b-143">Каждый столбец представляет сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="0e88b-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="0e88b-144">На предыдущем рисунке отображаются столбцы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e88b-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="0e88b-145">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-145">**Status**.</span></span>  <span data-ttu-id="0e88b-146">Код состояния HTTP для ответа.</span><span class="sxs-lookup"><span data-stu-id="0e88b-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="0e88b-147">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-147">**Type**.</span></span>  <span data-ttu-id="0e88b-148">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0e88b-148">The resource type.</span></span>  
    *   <span data-ttu-id="0e88b-149">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-149">**Initiator**.</span></span>  <span data-ttu-id="0e88b-150">Причина запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="0e88b-150">The cause of the resource request.</span></span>  <span data-ttu-id="0e88b-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span><span class="sxs-lookup"><span data-stu-id="0e88b-151">CHoosing a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="0e88b-152">**Время**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-152">**Time**.</span></span>  <span data-ttu-id="0e88b-153">Продолжительность запроса.</span><span class="sxs-lookup"><span data-stu-id="0e88b-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="0e88b-154">**Водопад**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-154">**Waterfall**.</span></span>  <span data-ttu-id="0e88b-155">Графическое представление различных этапов запроса.</span><span class="sxs-lookup"><span data-stu-id="0e88b-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="0e88b-156">Чтобы отобразить поломку, наведите курсор на водопад.</span><span class="sxs-lookup"><span data-stu-id="0e88b-156">To display a breakdown, hover on a Waterfall.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0e88b-157">График над журналом сети называется Обзором.</span><span class="sxs-lookup"><span data-stu-id="0e88b-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="0e88b-158">В этом руководстве не используется граф Обзор, поэтому его можно скрыть.</span><span class="sxs-lookup"><span data-stu-id="0e88b-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="0e88b-159">[Перейдите, чтобы скрыть области Обзор][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="0e88b-159">Navigate to [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="0e88b-160">После открытия DevTools записывалось сетевое действие в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="0e88b-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="0e88b-161">Чтобы продемонстрировать это, сначала посмотрите \*\*\*\* в нижней части сетевого журнала и сделайте умственную заметку о последнем действии.</span><span class="sxs-lookup"><span data-stu-id="0e88b-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="0e88b-162">Теперь выберите кнопку **Get Data** в демонстрации.</span><span class="sxs-lookup"><span data-stu-id="0e88b-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="0e88b-163">Посмотрите в нижней части **сетевого журнала** еще раз.</span><span class="sxs-lookup"><span data-stu-id="0e88b-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="0e88b-164">Отображается новый ресурс `getstarted.json` с именем.</span><span class="sxs-lookup"><span data-stu-id="0e88b-164">A new resource named `getstarted.json` is displayed.</span></span>  <span data-ttu-id="0e88b-165">Чтобы вызвать запрос файла на веб-страницу, выберите кнопку **Get Data.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-165">To cause the webpage to request the file, choose the **Get Data** button.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Новый ресурс в журнале network" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="0e88b-167">Новый ресурс в **журнале network**</span><span class="sxs-lookup"><span data-stu-id="0e88b-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <a name="show-more-information"></a><span data-ttu-id="0e88b-168">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0e88b-168">Show more information</span></span>  

<span data-ttu-id="0e88b-169">Столбцы сетевого журнала настраиваются.</span><span class="sxs-lookup"><span data-stu-id="0e88b-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="0e88b-170">Вы можете скрыть столбцы, которые вы не используете.</span><span class="sxs-lookup"><span data-stu-id="0e88b-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="0e88b-171">Существует также множество столбцов, скрытых по умолчанию, которые могут оказаться полезными.</span><span class="sxs-lookup"><span data-stu-id="0e88b-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="0e88b-172">Наведите курсор на загон для таблицы сетевого журнала, откройте контекстное меню \(правой кнопкой мыши\) и выберите **Домен**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="0e88b-173">Домен каждого ресурса теперь показан.</span><span class="sxs-lookup"><span data-stu-id="0e88b-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Включить столбец Домен" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="0e88b-175">Включить столбец Домен</span><span class="sxs-lookup"><span data-stu-id="0e88b-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="0e88b-176">Чтобы просмотреть полный URL-адрес ресурса, наведите курсор на ячейку в столбце **Имя.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-176">To review the full URL of a resource, hover on the cell in the **Name** column.</span></span>  
    
## <a name="simulate-a-slower-network-connection"></a><span data-ttu-id="0e88b-177">Имитация более медленного подключения к сети</span><span class="sxs-lookup"><span data-stu-id="0e88b-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="0e88b-178">Сетевое подключение компьютера, используемого для создания сайтов, вероятно, быстрее сетевых подключений мобильных устройств пользователей.</span><span class="sxs-lookup"><span data-stu-id="0e88b-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="0e88b-179">С помощью регулирования страницы вы получите более лучшее представление о том, сколько времени занимает страница для загрузки на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0e88b-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="0e88b-180">Выберите **отсев** регулирования, который по умолчанию устанавливается в **Online.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Включить регулирование" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="0e88b-182">Включить регулирование</span><span class="sxs-lookup"><span data-stu-id="0e88b-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-183">Выберите **медленную 3G**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Выбор медленного 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="0e88b-185">Выбор медленного 3G</span><span class="sxs-lookup"><span data-stu-id="0e88b-185">Choose Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-186">**Перезагрузить** в длительном прессе \( Перезагружать \) и затем выбрать ![ пустой ][ImageRefreshIcon] **кэш и твердую перезагрузку.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Пустой кэш и твердая перезагрузка" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="0e88b-188">Пустой кэш и твердая перезагрузка</span><span class="sxs-lookup"><span data-stu-id="0e88b-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="0e88b-189">При повторных посещениях браузер обычно обслуживает некоторые файлы из [кэша,][MDNHTTPCache]что ускоряет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="0e88b-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="0e88b-190">**Пустой кэш и твердая перезагрузка** вынуждают браузер идти по сети для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e88b-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="0e88b-191">Используйте его, чтобы отобразить, как первый посетитель испытывает нагрузку на страницу.</span><span class="sxs-lookup"><span data-stu-id="0e88b-191">Use it to display how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0e88b-192">Рабочий **процесс пустого кэша** и жесткой перезагрузки доступен только при открытом доступе DevTools.</span><span class="sxs-lookup"><span data-stu-id="0e88b-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <a name="capture-screenshots"></a><span data-ttu-id="0e88b-193">Захват скриншотов</span><span class="sxs-lookup"><span data-stu-id="0e88b-193">Capture screenshots</span></span>  

<span data-ttu-id="0e88b-194">На скриншотах отображается внешний вид веб-страницы во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="0e88b-194">Screenshots display how a webpage looks over time while it loads.</span></span>  

1.  <span data-ttu-id="0e88b-195">Выберите \. ![ Параметры ][ImageSettingsIcon] сети \) и включив почтовый ящик **скриншотов** захвата.</span><span class="sxs-lookup"><span data-stu-id="0e88b-195">Choose \(![Network settings][ImageSettingsIcon]\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="0e88b-196">Снова обновите страницу с помощью рабочего **процесса Пустой кэш и** тяжелая перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="0e88b-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="0e88b-197">Перейдите [к имитации более медленного подключения,](#simulate-a-slower-network-connection) если вам нужно напоминание о том, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="0e88b-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="0e88b-198">На панели Screenshots представлены эскизы того, как страница выглядела в различных точках во время процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="0e88b-198">The Screenshots panel provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Скриншоты загрузки страницы" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="0e88b-200">Скриншоты загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="0e88b-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-201">Выберите первый эскиз.</span><span class="sxs-lookup"><span data-stu-id="0e88b-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="0e88b-202">DevTools показывает, какие сетевые действия происходили в этот момент времени.</span><span class="sxs-lookup"><span data-stu-id="0e88b-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Сетевое действие, которое происходило во время первого скриншота" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="0e88b-204">Сетевое действие, которое происходило во время первого скриншота</span><span class="sxs-lookup"><span data-stu-id="0e88b-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-205">Выберите \. Параметры сети \) снова и отключите контрольный ящик скриншотов захвата, чтобы закрыть области ![ ][ImageSettingsIcon] скриншотов. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0e88b-205">Choose \(![Network settings][ImageSettingsIcon]\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="0e88b-206">Снова обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="0e88b-206">Refresh the page again.</span></span>  
    
## <a name="inspect-the-details-of-the-resource"></a><span data-ttu-id="0e88b-207">Проверка сведений о ресурсе</span><span class="sxs-lookup"><span data-stu-id="0e88b-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="0e88b-208">Выберите ресурс, чтобы узнать о нем дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0e88b-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="0e88b-209">Попробуйте его сейчас:</span><span class="sxs-lookup"><span data-stu-id="0e88b-209">Try it now:</span></span>  

1.  <span data-ttu-id="0e88b-210">Выберите `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="0e88b-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="0e88b-211">Показана панель **headers.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-211">The **Headers** panel is shown.</span></span>  <span data-ttu-id="0e88b-212">Используйте эту панель для проверки http-заглавных заглав.</span><span class="sxs-lookup"><span data-stu-id="0e88b-212">Use this panel to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Панель "Заготки"" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="0e88b-214">Панель **"Заготки"**</span><span class="sxs-lookup"><span data-stu-id="0e88b-214">The **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-215">Выберите панель **Preview.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-215">Choose the **Preview** panel.</span></span>  <span data-ttu-id="0e88b-216">Показана базовая визуализация HTML.</span><span class="sxs-lookup"><span data-stu-id="0e88b-216">A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Панель Предварительного просмотра" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="0e88b-218">Панель **Предварительного** просмотра</span><span class="sxs-lookup"><span data-stu-id="0e88b-218">The **Preview** panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0e88b-219">Панель полезна, когда API возвращает код ошибки в HTML.</span><span class="sxs-lookup"><span data-stu-id="0e88b-219">The panel is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="0e88b-220">При проверке изображений может быть проще считыть отрисовка HTML, чем исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="0e88b-220">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="0e88b-221">Выберите панель **ответа.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-221">Choose the **Response** panel.</span></span>  <span data-ttu-id="0e88b-222">Показан исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="0e88b-222">The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Панель ответов" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="0e88b-224">Панель **ответов**</span><span class="sxs-lookup"><span data-stu-id="0e88b-224">The **Response** panel</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="0e88b-225">При минировании файла выберите кнопку **Format** \( Format \) в нижней части панели ответа для повторного формата содержимого файла для ![ ][ImageFormatIcon] \*\*\*\* читаемости.</span><span class="sxs-lookup"><span data-stu-id="0e88b-225">When a file is minified, choose the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** panel to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="0e88b-226">Выберите панель **Timing.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-226">Choose the **Timing** panel.</span></span>  <span data-ttu-id="0e88b-227">Отображается разбивка сетевой активности для ресурса.</span><span class="sxs-lookup"><span data-stu-id="0e88b-227">A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Панель синхронизации" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="0e88b-229">Панель **синхронизации**</span><span class="sxs-lookup"><span data-stu-id="0e88b-229">The **Timing** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-230">Выберите **Закрыть** \( Закрыть \) чтобы ![ снова ][ImageCloseIcon] просмотреть журнал сети.</span><span class="sxs-lookup"><span data-stu-id="0e88b-230">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Кнопка Закрыть" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="0e88b-232">Кнопка **Закрыть**</span><span class="sxs-lookup"><span data-stu-id="0e88b-232">The **Close** button</span></span>  
    :::image-end:::  
    
## <a name="search-network-headers-and-responses"></a><span data-ttu-id="0e88b-233">Заглавные главы и ответы в сети поиска</span><span class="sxs-lookup"><span data-stu-id="0e88b-233">Search network headers and responses</span></span>  

<span data-ttu-id="0e88b-234">Используйте области **Поиска,** когда необходимо искать http-заготки и ответы всех ресурсов для определенной строки или регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="0e88b-234">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="0e88b-235">Например, предположим, что необходимо убедиться, что ваши ресурсы используют разумные **политики кэша.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-235">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="0e88b-236">Выберите **поиск** \. ![ Поиск ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0e88b-236">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="0e88b-237">Поле Поиска открывается слева от журнала Network.</span><span class="sxs-lookup"><span data-stu-id="0e88b-237">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Области поиска" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="0e88b-239">Области **поиска**</span><span class="sxs-lookup"><span data-stu-id="0e88b-239">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-240">Введите `Cache-Control` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0e88b-240">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="0e88b-241">В области поиска перечислены все экземпляры, которые он находит в загонах ресурсов `Cache-Control` или контенте.</span><span class="sxs-lookup"><span data-stu-id="0e88b-241">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Результаты поиска Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="0e88b-243">Результаты поиска по запросу </span><span class="sxs-lookup"><span data-stu-id="0e88b-243">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-244">Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.</span><span class="sxs-lookup"><span data-stu-id="0e88b-244">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="0e88b-245">Если вы ищете сведения о ресурсе, выберите результат, чтобы перейти непосредственно к ним.</span><span class="sxs-lookup"><span data-stu-id="0e88b-245">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="0e88b-246">Например, если запрос был найден в загонах, откроется панель **headers.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-246">For example, if the query was found in a header, the **Headers** panel opens.</span></span>   <span data-ttu-id="0e88b-247">Если запрос найден в содержимом, **откроется панель** ответа.</span><span class="sxs-lookup"><span data-stu-id="0e88b-247">If the query was found in content, the **Response** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Результат поиска, высветимый в панели Headers" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="0e88b-249">Результат поиска, высветимый в панели **Headers**</span><span class="sxs-lookup"><span data-stu-id="0e88b-249">A search result highlighted in the **Headers** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-250">Закрой панель поиска и панель **загона.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-250">Close the Search pane and the **Headers** panel.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Кнопки Закрыть" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="0e88b-252">Кнопки **Закрыть**</span><span class="sxs-lookup"><span data-stu-id="0e88b-252">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <a name="filter-resources"></a><span data-ttu-id="0e88b-253">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e88b-253">Filter resources</span></span>  

<span data-ttu-id="0e88b-254">DevTools предоставляет множество процессов для фильтрации ресурсов, не имеющих отношения к поставленной задаче.</span><span class="sxs-lookup"><span data-stu-id="0e88b-254">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Панель инструментов Filters" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="0e88b-256">Панель **инструментов Filters**</span><span class="sxs-lookup"><span data-stu-id="0e88b-256">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="0e88b-257">Панель **инструментов Filters** должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e88b-257">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="0e88b-258">Если нет:</span><span class="sxs-lookup"><span data-stu-id="0e88b-258">If not:</span></span>  

1.  <span data-ttu-id="0e88b-259">Выберите **фильтр** \( ![ Фильтр ][ImageFilterIcon] \) для его демонстрации.</span><span class="sxs-lookup"><span data-stu-id="0e88b-259">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <a name="filter-by-string-regular-expression-or-property"></a><span data-ttu-id="0e88b-260">Фильтр по строке, регулярному выражению или свойству</span><span class="sxs-lookup"><span data-stu-id="0e88b-260">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="0e88b-261">Текстовое поле **Filter** поддерживает множество различных типов фильтрации.</span><span class="sxs-lookup"><span data-stu-id="0e88b-261">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="0e88b-262">`png`Введите **текстовое поле Filter.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-262">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="0e88b-263">Показаны только файлы, содержащие `png` текст.</span><span class="sxs-lookup"><span data-stu-id="0e88b-263">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="0e88b-264">В этом случае единственными файлами, которые соответствуют фильтру, являются изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="0e88b-264">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Фильтр строки" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="0e88b-266">Фильтр строки</span><span class="sxs-lookup"><span data-stu-id="0e88b-266">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-267">Введите `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="0e88b-267">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="0e88b-268">DevTools отфильтровывает любой ресурс с иным файловым иным имям, которое не заканчивается с 1 или `j` `c` более `s` символов.</span><span class="sxs-lookup"><span data-stu-id="0e88b-268">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Фильтр регулярных выражений" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="0e88b-270">Фильтр регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="0e88b-270">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-271">Введите `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="0e88b-271">Type `-main.css`.</span></span>  <span data-ttu-id="0e88b-272">DevTools отфильтровываю. `main.css`</span><span class="sxs-lookup"><span data-stu-id="0e88b-272">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="0e88b-273">Если какой-либо файл соответствует шаблону, синица также отфильтровыется.</span><span class="sxs-lookup"><span data-stu-id="0e88b-273">If any file matches the pattern, tit is also filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Отрицательный фильтр" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="0e88b-275">Отрицательный фильтр</span><span class="sxs-lookup"><span data-stu-id="0e88b-275">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-276">`domain:cdn.glitch.com`Введите **текстовое поле Filter.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-276">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="0e88b-277">DevTools отфильтровывает любой ресурс с URL-адресом, который не соответствует этому домену.</span><span class="sxs-lookup"><span data-stu-id="0e88b-277">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Фильтр свойств" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="0e88b-279">Фильтр свойств</span><span class="sxs-lookup"><span data-stu-id="0e88b-279">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="0e88b-280">Полный список фильтруемых свойств перейдите к [запросам фильтрации по свойствам.][DevtoolsReferenceProperty]</span><span class="sxs-lookup"><span data-stu-id="0e88b-280">For the full list of filterable properties, navigate to [Filter requests by properties][DevtoolsReferenceProperty].</span></span>  
    
1.  <span data-ttu-id="0e88b-281">Очистить **текстовое** поле Filter любого текста.</span><span class="sxs-lookup"><span data-stu-id="0e88b-281">Clear the **Filter** text box of any text.</span></span>  
    
### <a name="filter-by-resource-type"></a><span data-ttu-id="0e88b-282">Фильтр по типу ресурса</span><span class="sxs-lookup"><span data-stu-id="0e88b-282">Filter by resource type</span></span>  

<span data-ttu-id="0e88b-283">Чтобы сосредоточиться на определенном типе файла, например таблицах стилей:</span><span class="sxs-lookup"><span data-stu-id="0e88b-283">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="0e88b-284">Выберите **CSS**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-284">Choose **CSS**.</span></span>  <span data-ttu-id="0e88b-285">Все другие типы файлов отфильтровыются.</span><span class="sxs-lookup"><span data-stu-id="0e88b-285">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Показать только файлы CSS" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="0e88b-287">Показать только файлы CSS</span><span class="sxs-lookup"><span data-stu-id="0e88b-287">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-288">Чтобы также отображать скрипты, выберите и удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите **JS**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-288">To also display scripts, select and hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Показать только файлы CSS и JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="0e88b-290">Показать только файлы CSS и JS</span><span class="sxs-lookup"><span data-stu-id="0e88b-290">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-291">Чтобы удалить фильтры и снова отобразить все ресурсы, выберите **All**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-291">To remove the filters and display all resources again, choose **All**.</span></span>  
    
<span data-ttu-id="0e88b-292">Для других процессов фильтрации перейдите к [запросам фильтрации.][DevtoolsNetworkReferenceFilter]</span><span class="sxs-lookup"><span data-stu-id="0e88b-292">For other filtering workflows, navigate to [Filter requests][DevtoolsNetworkReferenceFilter].</span></span>  

## <a name="block-requests"></a><span data-ttu-id="0e88b-293">Блокировка запросов</span><span class="sxs-lookup"><span data-stu-id="0e88b-293">Block requests</span></span>  

<span data-ttu-id="0e88b-294">Как выглядит и ведет себя страница, если некоторые ресурсы страницы недоступны?</span><span class="sxs-lookup"><span data-stu-id="0e88b-294">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="0e88b-295">Он полностью сбой или он все еще несколько функциональный?</span><span class="sxs-lookup"><span data-stu-id="0e88b-295">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="0e88b-296">Блокировка запросов, чтобы узнать:</span><span class="sxs-lookup"><span data-stu-id="0e88b-296">Block requests to find out:</span></span>  

1.  <span data-ttu-id="0e88b-297">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) `Command` + `Shift` + `P` или \(macOS\) для открытия **командного меню.**</span><span class="sxs-lookup"><span data-stu-id="0e88b-297">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Меню команд" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="0e88b-299">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="0e88b-299">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-300">`block`Введите, **выберите показать блокировку запроса**и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0e88b-300">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Показать блокировку запросов" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="0e88b-302">Показать блокировку запросов</span><span class="sxs-lookup"><span data-stu-id="0e88b-302">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-303">Выберите **Добавить шаблон** \. Добавьте шаблон ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="0e88b-303">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="0e88b-304">Введите `main.css`.</span><span class="sxs-lookup"><span data-stu-id="0e88b-304">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Блокировка main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="0e88b-306">Блокировка</span><span class="sxs-lookup"><span data-stu-id="0e88b-306">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-307">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="0e88b-307">Choose **Add**.</span></span>  
1.  <span data-ttu-id="0e88b-308">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="0e88b-308">Refresh the page.</span></span>  <span data-ttu-id="0e88b-309">Как и ожидалось, укладка страницы немного перепуталась, так как основной лист стилей был заблокирован.</span><span class="sxs-lookup"><span data-stu-id="0e88b-309">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0e88b-310">Строка `main.css` в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="0e88b-310">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="0e88b-311">Красный текст означает, что ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="0e88b-311">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css заблокирован" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="0e88b-313">заблокирована</span><span class="sxs-lookup"><span data-stu-id="0e88b-313">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0e88b-314">Deselect the **Enable request blocking** checkbox.</span><span class="sxs-lookup"><span data-stu-id="0e88b-314">Deselect the **Enable request blocking** checkbox.</span></span>  

## <a name="conclusion"></a><span data-ttu-id="0e88b-315">Заключение</span><span class="sxs-lookup"><span data-stu-id="0e88b-315">Conclusion</span></span>  

<span data-ttu-id="0e88b-316">Поздравляем, вы завершили учебник.</span><span class="sxs-lookup"><span data-stu-id="0e88b-316">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="0e88b-317">Теперь вы знаете, как использовать средство **Network** в Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="0e88b-317">You now know how to use the **Network** tool in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="0e88b-318">Перейдите к [ссылке на сеть,][DevtoolsNetworkReference] чтобы узнать больше функций DevTools, связанных с проверкой сетевой активности.</span><span class="sxs-lookup"><span data-stu-id="0e88b-318">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="0e88b-319">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0e88b-319">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение размещения Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsNetworkReference]: ./reference.md "Справочные ссылки на | Документы Майкрософт"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы на фильтрацию — ссылки на | Документы Майкрософт"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрыть области Обзор — ссылки на анализ сети | Документы Майкрософт"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам — ссылки на | Документы Майкрософт"
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Проверка демонстрации сетевой активности | Glitch"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Http кэш | MDN"  

> [!NOTE]
> <span data-ttu-id="0e88b-329">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0e88b-329">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0e88b-330">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/network/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="0e88b-330">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0e88b-332">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0e88b-332">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
