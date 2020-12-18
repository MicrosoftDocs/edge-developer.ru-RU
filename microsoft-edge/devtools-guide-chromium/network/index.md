---
description: Учебник по наиболее популярным сетевым функциям в Microsoft Edge DevTools.
title: Проверка сетевой активности в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1874c6222798755aa5ad7002e22b0cef00c8fd41
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230980"
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

# <span data-ttu-id="973b7-104">Проверка сетевой активности в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="973b7-104">Inspect network activity in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="973b7-105">Это практический учебник по некоторым наиболее часто используемым функциям DevTools, связанным с проверкой сетевой активности страницы.</span><span class="sxs-lookup"><span data-stu-id="973b7-105">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="973b7-106">Если [вы хотите][DevtoolsNetworkReference] просмотреть функции, см. справку по сети.</span><span class="sxs-lookup"><span data-stu-id="973b7-106">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="973b7-107">Когда использовать панель "Сеть"</span><span class="sxs-lookup"><span data-stu-id="973b7-107">When to use the Network panel</span></span>  

<span data-ttu-id="973b7-108">Как правило, используйте панель "Сеть", чтобы убедиться, что ресурсы загружаются или загружаются ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="973b7-108">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="973b7-109">Наиболее распространенные случаи использования для панели "Сеть":</span><span class="sxs-lookup"><span data-stu-id="973b7-109">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="973b7-110">Убедитесь, что ресурсы фактически загружаются или загружаются.</span><span class="sxs-lookup"><span data-stu-id="973b7-110">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="973b7-111">Проверка свойств отдельного ресурса, таких как http-загодеры, содержимое, размер и т. д.</span><span class="sxs-lookup"><span data-stu-id="973b7-111">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="973b7-112">Если вы ищете способы повышения производительности загрузки страницы, **не** начинайте с средства **"Сеть".**</span><span class="sxs-lookup"><span data-stu-id="973b7-112">If you are looking for ways to improve page load performance, **do not** start with the **Network** tool.</span></span>  <span data-ttu-id="973b7-113">Существует множество типов проблем с производительностью нагрузки, не связанных с сетевой активностью.</span><span class="sxs-lookup"><span data-stu-id="973b7-113">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="973b7-114">Начните с панели "Аудит", так как она дает вам рекомендации по улучшению страницы.</span><span class="sxs-lookup"><span data-stu-id="973b7-114">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="973b7-115">Перейдите к [оптимизации скорости веб-сайта.][DevtoolsSpeedGetStarted]</span><span class="sxs-lookup"><span data-stu-id="973b7-115">Navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="973b7-116">Открытие панели "Сеть"</span><span class="sxs-lookup"><span data-stu-id="973b7-116">Open the Network panel</span></span>  

<span data-ttu-id="973b7-117">Чтобы получить все возможности из этого руководства, откройте демонстрацию и попробуйте функции на странице демонстрации.</span><span class="sxs-lookup"><span data-stu-id="973b7-117">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="973b7-118">Откройте [демонстрационную версию "Начало работы".][GlitchNetworkGetStarted]</span><span class="sxs-lookup"><span data-stu-id="973b7-118">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="973b7-120">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="973b7-120">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="973b7-121">[Откройте DevTools,][DevToolsOpen] нажав `Control` + `Shift` + `J` \(Windows, Linux\) или `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="973b7-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="973b7-122">Откроется **средство** консоли.</span><span class="sxs-lookup"><span data-stu-id="973b7-122">The **Console** tool opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="Консоль" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="973b7-124">Консоль \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="973b7-124">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="973b7-125">Вы можете [пристыковать DevTools к нижней части окна.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="973b7-125">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools, закрепленный в нижней части окна" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="973b7-127">DevTools, закрепленный в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="973b7-127">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-128">Выберите **вкладку "Сеть".**  Откроется **панель** "Сеть".</span><span class="sxs-lookup"><span data-stu-id="973b7-128">Select the **Network** tab.  The **Network** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="Консольное средство в DevTools, закрепленное в нижней части окна" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="973b7-130">**Консольное** средство в DevTools, закрепленное в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="973b7-130">**Console** tool in the DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="973b7-131">Сейчас панель "Сеть" пуста.</span><span class="sxs-lookup"><span data-stu-id="973b7-131">Right now the Network panel is empty.</span></span>  <span data-ttu-id="973b7-132">DevTools записывает сетевое действие только после его открытия, и с момента открытия DevTools никаких сетевых действий не было.</span><span class="sxs-lookup"><span data-stu-id="973b7-132">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="973b7-133">Запись сетевой активности в журнал</span><span class="sxs-lookup"><span data-stu-id="973b7-133">Log network activity</span></span>  

<span data-ttu-id="973b7-134">Чтобы просмотреть сетевое действие, которое вызывает страница:</span><span class="sxs-lookup"><span data-stu-id="973b7-134">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="973b7-135">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="973b7-135">Reload the page.</span></span>  <span data-ttu-id="973b7-136">Панель "Сеть" записи всех сетевых действий в журнал **сети.**</span><span class="sxs-lookup"><span data-stu-id="973b7-136">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Сетевой журнал" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="973b7-138">Сетевой **журнал**</span><span class="sxs-lookup"><span data-stu-id="973b7-138">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="973b7-139">Каждая строка **сетевого журнала** представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="973b7-139">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="973b7-140">По умолчанию ресурсы перечислены в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="973b7-140">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="973b7-141">Верхний ресурс обычно является основным HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="973b7-141">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="973b7-142">Нижний ресурс — это ресурс, который был запросрош последним.</span><span class="sxs-lookup"><span data-stu-id="973b7-142">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="973b7-143">Каждый столбец представляет сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="973b7-143">Each column represents information about a resource.</span></span>  <span data-ttu-id="973b7-144">На предыдущем рисунке отображаются столбцы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="973b7-144">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="973b7-145">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="973b7-145">**Status**.</span></span>  <span data-ttu-id="973b7-146">Код состояния HTTP для ответа.</span><span class="sxs-lookup"><span data-stu-id="973b7-146">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="973b7-147">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="973b7-147">**Type**.</span></span>  <span data-ttu-id="973b7-148">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="973b7-148">The resource type.</span></span>  
    *   <span data-ttu-id="973b7-149">**Инициатор .**</span><span class="sxs-lookup"><span data-stu-id="973b7-149">**Initiator**.</span></span>  <span data-ttu-id="973b7-150">Причина запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="973b7-150">The cause of the resource request.</span></span>  <span data-ttu-id="973b7-151">При выборе ссылки в столбце "Инициатор" вы будете перенабором кода, который вызвал запрос.</span><span class="sxs-lookup"><span data-stu-id="973b7-151">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="973b7-152">**Time**.</span><span class="sxs-lookup"><span data-stu-id="973b7-152">**Time**.</span></span>  <span data-ttu-id="973b7-153">Продолжительность запроса.</span><span class="sxs-lookup"><span data-stu-id="973b7-153">The duration of the request.</span></span>  
    *   <span data-ttu-id="973b7-154">**Каскад .**</span><span class="sxs-lookup"><span data-stu-id="973b7-154">**Waterfall**.</span></span>  <span data-ttu-id="973b7-155">Графическое представление различных этапов запроса.</span><span class="sxs-lookup"><span data-stu-id="973b7-155">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="973b7-156">Наведите курсор на каскадный каскад, чтобы увидеть разбивку.</span><span class="sxs-lookup"><span data-stu-id="973b7-156">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="973b7-157">График над журналом сети называется обзором.</span><span class="sxs-lookup"><span data-stu-id="973b7-157">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="973b7-158">Вы не будете использовать график "Обзор" в этом руководстве, поэтому можете скрыть его.</span><span class="sxs-lookup"><span data-stu-id="973b7-158">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="973b7-159">См. ["Скрытие области обзора".][DevtoolsReferenceHideOverview]</span><span class="sxs-lookup"><span data-stu-id="973b7-159">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="973b7-160">После открытия DevTools он записи сетевой активности в сетевой журнал.</span><span class="sxs-lookup"><span data-stu-id="973b7-160">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="973b7-161">Чтобы продемонстрировать это, сначала посмотрите \*\*\*\* в нижнюю часть сетевого журнала и заметьте последнее действие.</span><span class="sxs-lookup"><span data-stu-id="973b7-161">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="973b7-162">Теперь выберите кнопку **"Получить данные"** в демонстрации.</span><span class="sxs-lookup"><span data-stu-id="973b7-162">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="973b7-163">Еще раз посмотрите на нижнюю **часть сетевого журнала.**</span><span class="sxs-lookup"><span data-stu-id="973b7-163">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="973b7-164">Вы увидите новый ресурс под названием `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="973b7-164">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="973b7-165">При **нажатии кнопки "Получить данные"** страница запросила этот файл.</span><span class="sxs-lookup"><span data-stu-id="973b7-165">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Новый ресурс в сетевом журнале" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="973b7-167">Новый ресурс в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="973b7-167">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="973b7-168">Показать дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="973b7-168">Show more information</span></span>  

<span data-ttu-id="973b7-169">Столбцы сетевого журнала настраиваются.</span><span class="sxs-lookup"><span data-stu-id="973b7-169">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="973b7-170">Вы можете скрыть столбцы, которые не используете.</span><span class="sxs-lookup"><span data-stu-id="973b7-170">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="973b7-171">Также существует много скрытых по умолчанию столбцов, которые могут оказаться полезными.</span><span class="sxs-lookup"><span data-stu-id="973b7-171">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="973b7-172">Наведите курсор на загон таблицы "Журнал сети", откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Домен".**</span><span class="sxs-lookup"><span data-stu-id="973b7-172">Hover on the header of the Network Log table, open the contextual menu \(right-click\), and choose **Domain**.</span></span>  <span data-ttu-id="973b7-173">Теперь отображается домен каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="973b7-173">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Включить столбец "Домен"" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="973b7-175">Включить столбец "Домен"</span><span class="sxs-lookup"><span data-stu-id="973b7-175">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="973b7-176">Чтобы увидеть полный URL-адрес ресурса, наведите курсор на ячейку в столбце **"Имя".**</span><span class="sxs-lookup"><span data-stu-id="973b7-176">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="973b7-177">Имитация более медленного сетевого подключения</span><span class="sxs-lookup"><span data-stu-id="973b7-177">Simulate a slower network connection</span></span>  

<span data-ttu-id="973b7-178">Сетевое подключение компьютера, используемого для создания сайтов, скорее всего, быстрее, чем сетевые подключения мобильных устройств пользователей.</span><span class="sxs-lookup"><span data-stu-id="973b7-178">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="973b7-179">Регулирование страницы позволяет лучше понять, сколько времени занимает страница для загрузки на мобильное устройство.</span><span class="sxs-lookup"><span data-stu-id="973b7-179">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="973b7-180">Выберите в **этом выпадаемом окне** значение **Online** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="973b7-180">Choose the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Включить регулирование" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="973b7-182">Включить регулирование</span><span class="sxs-lookup"><span data-stu-id="973b7-182">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-183">Choose **Slow 3G**.</span><span class="sxs-lookup"><span data-stu-id="973b7-183">Choose **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Выбор медленной 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="973b7-185">Выбор медленной 3G</span><span class="sxs-lookup"><span data-stu-id="973b7-185">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-186">Reload \( **Reload** ![ \( Reload ][ImageRefreshIcon] \) и выберите **пустой кэш и твердую перезагрузку.**</span><span class="sxs-lookup"><span data-stu-id="973b7-186">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then choose **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Пустой кэш и неостановленная перезагрузка" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="973b7-188">Пустой кэш и неостановленная перезагрузка</span><span class="sxs-lookup"><span data-stu-id="973b7-188">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="973b7-189">При повторном посещении браузер обычно [][MDNHTTPCache]обслуживает некоторые файлы из кэша, что ускоряет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="973b7-189">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="973b7-190">**Пустой кэш и твердая перезагрузка** заставляет браузер переходить по сети для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="973b7-190">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="973b7-191">Это полезно, если вы хотите увидеть, как посетитель в первый раз видит загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="973b7-191">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="973b7-192">Рабочий **процесс пустого кэша** и жесткой перезагрузки доступен, только если открыт DevTools.</span><span class="sxs-lookup"><span data-stu-id="973b7-192">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="973b7-193">Снимки экрана</span><span class="sxs-lookup"><span data-stu-id="973b7-193">Capture screenshots</span></span>  

<span data-ttu-id="973b7-194">Screenshots let you see how a page looked over time while it was loading.</span><span class="sxs-lookup"><span data-stu-id="973b7-194">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="973b7-195">Choose \( ![ Network settings ][ImageSettingsIcon] \) and turn on the **Capture screenshots** checkbox.</span><span class="sxs-lookup"><span data-stu-id="973b7-195">Choose \(![Network settings][ImageSettingsIcon]\) and turn on the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="973b7-196">Обновите страницу еще раз с помощью рабочего процесса "Пустой кэш" и **"Неокрепленная** перезагрузка".</span><span class="sxs-lookup"><span data-stu-id="973b7-196">Refresh the page again using the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="973b7-197">Если вам [нужно](#simulate-a-slower-network-connection) напоминание о том, как это сделать, перейдите к "Имитация медленных подключений".</span><span class="sxs-lookup"><span data-stu-id="973b7-197">Navigate to [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="973b7-198">На области "Снимки экрана" представлены эскизы того, как страница выглядела в различных точках во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="973b7-198">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Снимки экрана загрузки страницы" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="973b7-200">Снимки экрана загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="973b7-200">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-201">Выберите первый эскиз.</span><span class="sxs-lookup"><span data-stu-id="973b7-201">Choose the first thumbnail.</span></span>  <span data-ttu-id="973b7-202">DevTools показывает, какие сетевые действия происходили в этот момент времени.</span><span class="sxs-lookup"><span data-stu-id="973b7-202">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Сетевое действие, которое происходило на первом снимке экрана" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="973b7-204">Сетевое действие, которое происходило на первом снимке экрана</span><span class="sxs-lookup"><span data-stu-id="973b7-204">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-205">Снова выберите \( Параметры сети \) и отключите снимок экрана для закрытия области ![ ][ImageSettingsIcon] снимков экрана. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="973b7-205">Choose \(![Network settings][ImageSettingsIcon]\) again and turn off the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="973b7-206">Обновите страницу еще раз.</span><span class="sxs-lookup"><span data-stu-id="973b7-206">Refresh the page again.</span></span>  
    
## <span data-ttu-id="973b7-207">Проверка сведений о ресурсе</span><span class="sxs-lookup"><span data-stu-id="973b7-207">Inspect the details of the resource</span></span>  

<span data-ttu-id="973b7-208">Выберите ресурс, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="973b7-208">Choose a resource to learn more information about it.</span></span>  <span data-ttu-id="973b7-209">Попробуйте сделать это сейчас:</span><span class="sxs-lookup"><span data-stu-id="973b7-209">Try it now:</span></span>  

1.  <span data-ttu-id="973b7-210">Выберите `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="973b7-210">Choose `getstarted.html`.</span></span>  <span data-ttu-id="973b7-211">Отображается **вкладка** "Заглавные".</span><span class="sxs-lookup"><span data-stu-id="973b7-211">The **Headers** tab is shown.</span></span>  <span data-ttu-id="973b7-212">Эта вкладка используется для проверки http-headers.</span><span class="sxs-lookup"><span data-stu-id="973b7-212">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Вкладка "Заглавные"" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="973b7-214">Вкладка **"Заглавные"**</span><span class="sxs-lookup"><span data-stu-id="973b7-214">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-215">Выберите вкладку **"Предварительный** просмотр".  Показана базовая отрисовка HTML.</span><span class="sxs-lookup"><span data-stu-id="973b7-215">Choose the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Вкладка "Предварительный просмотр"" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="973b7-217">Вкладка **"Предварительный** просмотр"</span><span class="sxs-lookup"><span data-stu-id="973b7-217">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="973b7-218">Вкладка полезна, когда API возвращает код ошибки в HTML.</span><span class="sxs-lookup"><span data-stu-id="973b7-218">The tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="973b7-219">Может оказаться, что проще читать отрисовки HTML, чем исходный код HTML, или при проверке изображений.</span><span class="sxs-lookup"><span data-stu-id="973b7-219">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="973b7-220">Выберите **вкладку "Ответ".**  Показан исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="973b7-220">Choose the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Вкладка "Ответ"" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="973b7-222">Вкладка **"Ответ"**</span><span class="sxs-lookup"><span data-stu-id="973b7-222">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="973b7-223">При минифицировании файла выберите кнопку **Format** \( Format \) в нижней части вкладки "Ответ", чтобы повторно отформатирование содержимого файла для ![ ][ImageFormatIcon] \*\*\*\* учитаемости.</span><span class="sxs-lookup"><span data-stu-id="973b7-223">When a file is minified, choose the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab to re-format the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="973b7-224">Выберите вкладку **"Время".**  Отображается разбивка сетевой активности ресурса.</span><span class="sxs-lookup"><span data-stu-id="973b7-224">Choose the **Timing** tab.  A breakdown of the network activity for the resource is displayed.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Вкладка "Время"" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="973b7-226">Вкладка **"Время"**</span><span class="sxs-lookup"><span data-stu-id="973b7-226">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-227">Choose **Close** \( ![ Close ][ImageCloseIcon] \) to view the Network Log again.</span><span class="sxs-lookup"><span data-stu-id="973b7-227">Choose **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Кнопка "Закрыть"" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="973b7-229">Кнопка **"Закрыть"**</span><span class="sxs-lookup"><span data-stu-id="973b7-229">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="973b7-230">Поиск в сетевых загонах и ответах</span><span class="sxs-lookup"><span data-stu-id="973b7-230">Search network headers and responses</span></span>  

<span data-ttu-id="973b7-231">Используйте поиск **в области** поиска, если необходимо искать определенные строки или регулярные выражения в http-загонах и ответах всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="973b7-231">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="973b7-232">Например, предположим, что вы хотите убедиться, что ресурсы используют разумные **политики кэша.**</span><span class="sxs-lookup"><span data-stu-id="973b7-232">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="973b7-233">Choose **Search** \( ![ Search ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="973b7-233">Choose **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="973b7-234">Слева от сетевого журнала откроется окно поиска.</span><span class="sxs-lookup"><span data-stu-id="973b7-234">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="The Search pane" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="973b7-236">The **Search** pane</span><span class="sxs-lookup"><span data-stu-id="973b7-236">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-237">Введите `Cache-Control` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="973b7-237">Type `Cache-Control` and select `Enter`.</span></span>  <span data-ttu-id="973b7-238">В области поиска перечислены все экземпляры, которые она находит в `Cache-Control` загонах ресурсов или содержимом.</span><span class="sxs-lookup"><span data-stu-id="973b7-238">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Результаты поиска для Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="973b7-240">Результаты поиска по запросу </span><span class="sxs-lookup"><span data-stu-id="973b7-240">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-241">Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.</span><span class="sxs-lookup"><span data-stu-id="973b7-241">Choose a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="973b7-242">Если вы ищете сведения о ресурсе, выберите результат, чтобы перейти непосредственно к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="973b7-242">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="973b7-243">Например, если запрос был найден в заголке, откроется вкладка "Headers".</span><span class="sxs-lookup"><span data-stu-id="973b7-243">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="973b7-244">Если запрос найден в содержимом, откроется вкладка **"Ответ".**</span><span class="sxs-lookup"><span data-stu-id="973b7-244">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Результат поиска, выделенный на вкладке "Headers"" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="973b7-246">Результат поиска, выделенный на **вкладке "Headers"**</span><span class="sxs-lookup"><span data-stu-id="973b7-246">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-247">Закроем области поиска и вкладку "Headers".</span><span class="sxs-lookup"><span data-stu-id="973b7-247">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Кнопки закрытия" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="973b7-249">Кнопки **закрытия**</span><span class="sxs-lookup"><span data-stu-id="973b7-249">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="973b7-250">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="973b7-250">Filter resources</span></span>  

<span data-ttu-id="973b7-251">DevTools предоставляет множество процессов для фильтрации ресурсов, не имеющих отношения к задаче.</span><span class="sxs-lookup"><span data-stu-id="973b7-251">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Панель инструментов "Фильтры"" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="973b7-253">Панель **инструментов "Фильтры"**</span><span class="sxs-lookup"><span data-stu-id="973b7-253">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="973b7-254">Панель **инструментов фильтров** должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="973b7-254">The **Filters** toolbar should be turned on by default.</span></span>  <span data-ttu-id="973b7-255">Если нет:</span><span class="sxs-lookup"><span data-stu-id="973b7-255">If not:</span></span>  

1.  <span data-ttu-id="973b7-256">Выберите **фильтр** \( ![ Фильтр ][ImageFilterIcon] \), чтобы отдемонстрировать его.</span><span class="sxs-lookup"><span data-stu-id="973b7-256">Choose **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="973b7-257">Фильтрация по строке, регулярному выражению или свойству</span><span class="sxs-lookup"><span data-stu-id="973b7-257">Filter by string, regular expression, or property</span></span>  

<span data-ttu-id="973b7-258">**Текстовое** поле фильтра поддерживает различные типы фильтрации.</span><span class="sxs-lookup"><span data-stu-id="973b7-258">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="973b7-259">Введите `png` в **текстовое поле фильтра.**</span><span class="sxs-lookup"><span data-stu-id="973b7-259">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="973b7-260">Будут показаны только файлы, содержащие `png` текст.</span><span class="sxs-lookup"><span data-stu-id="973b7-260">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="973b7-261">В этом случае единственными файлами, которые соответствуют фильтру, являются изображения PNG.</span><span class="sxs-lookup"><span data-stu-id="973b7-261">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Фильтр строк" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="973b7-263">Фильтр строк</span><span class="sxs-lookup"><span data-stu-id="973b7-263">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-264">Введите `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="973b7-264">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="973b7-265">DevTools отфильтровывает любой ресурс с именом файла, который не заканчивается на 1 или более `j` `c` `s` символов.</span><span class="sxs-lookup"><span data-stu-id="973b7-265">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Фильтр регулярных выражений" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="973b7-267">Фильтр регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="973b7-267">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-268">Введите `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="973b7-268">Type `-main.css`.</span></span>  <span data-ttu-id="973b7-269">Фильтры DevTools `main.css` .</span><span class="sxs-lookup"><span data-stu-id="973b7-269">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="973b7-270">Если какой-либо другой файл соответствует шаблону, он также будет отфильтрован.</span><span class="sxs-lookup"><span data-stu-id="973b7-270">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Отрицательный фильтр" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="973b7-272">Отрицательный фильтр</span><span class="sxs-lookup"><span data-stu-id="973b7-272">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-273">Введите `domain:cdn.glitch.com` в **текстовое поле** "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="973b7-273">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="973b7-274">DevTools отфильтровывает любой ресурс с URL-адресом, который не соответствует этому домену.</span><span class="sxs-lookup"><span data-stu-id="973b7-274">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Фильтр свойств" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="973b7-276">Фильтр свойств</span><span class="sxs-lookup"><span data-stu-id="973b7-276">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="973b7-277">Полный [список фильтруемых][DevtoolsReferenceProperty] свойств см. в запросах фильтра по свойствам.</span><span class="sxs-lookup"><span data-stu-id="973b7-277">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="973b7-278">Очищает **текстовое** поле фильтра для любого текста.</span><span class="sxs-lookup"><span data-stu-id="973b7-278">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="973b7-279">Фильтрация по типу ресурса</span><span class="sxs-lookup"><span data-stu-id="973b7-279">Filter by resource type</span></span>  

<span data-ttu-id="973b7-280">Чтобы сосредоточиться на определенном типе файлов, таких как таблицы стилей:</span><span class="sxs-lookup"><span data-stu-id="973b7-280">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="973b7-281">Выберите **CSS.**</span><span class="sxs-lookup"><span data-stu-id="973b7-281">Choose **CSS**.</span></span>  <span data-ttu-id="973b7-282">Все остальные типы файлов отфильтровыются.</span><span class="sxs-lookup"><span data-stu-id="973b7-282">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Показывать только CSS-файлы" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="973b7-284">Показывать только CSS-файлы</span><span class="sxs-lookup"><span data-stu-id="973b7-284">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-285">Чтобы также увидеть сценарии, удерживайте `Control` \(Windows, Linux\) или `Command` \(macOS\) и выберите **JS.**</span><span class="sxs-lookup"><span data-stu-id="973b7-285">To also see scripts, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Показывать только CSS- и JS-файлы" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="973b7-287">Показывать только CSS- и JS-файлы</span><span class="sxs-lookup"><span data-stu-id="973b7-287">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-288">Выберите **"Все",** чтобы удалить фильтры и снова увидеть все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="973b7-288">Choose **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="973b7-289">См. [запросы фильтра][DevtoolsNetworkReferenceFilter] для других процессов фильтрации.</span><span class="sxs-lookup"><span data-stu-id="973b7-289">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="973b7-290">Блокировка запросов</span><span class="sxs-lookup"><span data-stu-id="973b7-290">Block requests</span></span>  

<span data-ttu-id="973b7-291">Как выглядит и работает страница, когда некоторые ресурсы страницы недоступны?</span><span class="sxs-lookup"><span data-stu-id="973b7-291">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="973b7-292">Полностью ли он дает сбой или по-прежнему работает?</span><span class="sxs-lookup"><span data-stu-id="973b7-292">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="973b7-293">Блокируют запросы, чтобы узнать:</span><span class="sxs-lookup"><span data-stu-id="973b7-293">Block requests to find out:</span></span>  

1.  <span data-ttu-id="973b7-294">Выберите `Control` + `Shift` + `P` \(Windows, Linux\) или `Command` + `Shift` + `P` \(macOS\), чтобы открыть меню **команд.**</span><span class="sxs-lookup"><span data-stu-id="973b7-294">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Меню команд" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="973b7-296">Меню **команд**</span><span class="sxs-lookup"><span data-stu-id="973b7-296">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-297">`block`Введите, **выберите "Показать блокирование запросов"** и "Выбрать". `Enter`</span><span class="sxs-lookup"><span data-stu-id="973b7-297">Type `block`, choose **Show Request Blocking**, and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Показать блокирование запросов" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="973b7-299">Показать блокирование запросов</span><span class="sxs-lookup"><span data-stu-id="973b7-299">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-300">Choose **Add Pattern** \( Add Pattern ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="973b7-300">Choose **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="973b7-301">Введите `main.css`.</span><span class="sxs-lookup"><span data-stu-id="973b7-301">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Блокировка main.css" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="973b7-303">Блокировка</span><span class="sxs-lookup"><span data-stu-id="973b7-303">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-304">Choose **Add**.</span><span class="sxs-lookup"><span data-stu-id="973b7-304">Choose **Add**.</span></span>  
1.  <span data-ttu-id="973b7-305">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="973b7-305">Reload the page.</span></span>  <span data-ttu-id="973b7-306">Как и ожидалось, оформление страницы немного перепутано, так как основная таблица стилей заблокирована.</span><span class="sxs-lookup"><span data-stu-id="973b7-306">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="973b7-307">Строка `main.css` в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="973b7-307">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="973b7-308">Красный текст означает, что ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="973b7-308">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="main.css заблокирован" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="973b7-310">заблокировано</span><span class="sxs-lookup"><span data-stu-id="973b7-310">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="973b7-311">Отбрасыйте этот **блокирующий запрос.**</span><span class="sxs-lookup"><span data-stu-id="973b7-311">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="973b7-312">Заключение</span><span class="sxs-lookup"><span data-stu-id="973b7-312">Conclusion</span></span>  

<span data-ttu-id="973b7-313">Поздравляем, вы завершили учебное руководство.</span><span class="sxs-lookup"><span data-stu-id="973b7-313">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="973b7-314">Теперь вы знаете, как использовать панель **"Сеть"** в Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="973b7-314">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<span data-ttu-id="973b7-315">Перейдите в [справочник по сети,][DevtoolsNetworkReference] чтобы найти дополнительные функции DevTools, связанные с проверкой сетевой активности.</span><span class="sxs-lookup"><span data-stu-id="973b7-315">Navigate to the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

## <span data-ttu-id="973b7-316">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="973b7-316">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
[DevtoolsNetworkReference]: ./reference.md "Справочник по анализу сети | Документы Майкрософт"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы фильтра — справочник по анализу сети | Документы Майкрософт"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрытие области обзора — справочник по анализу сети | Документы Майкрософт"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам — справочник по анализу сети | Документы Майкрософт"
[DevToolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Проверка демонстрации сетевой активности | Временный сбой"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэшинг HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="973b7-326">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="973b7-326">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="973b7-327">Исходная страница [](https://developers.google.com/web/tools/chrome-devtools/network/index) находится здесь и автором [kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="973b7-327">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="973b7-329">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="973b7-329">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
