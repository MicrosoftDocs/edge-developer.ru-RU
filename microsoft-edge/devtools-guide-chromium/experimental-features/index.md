---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эксперимент
ms.openlocfilehash: 612b3b83aee1ee9035982e58e008395ec3645b2b
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408306"
---
# <a name="experimental-features"></a><span data-ttu-id="ea593-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ea593-104">Experimental features</span></span>  

<span data-ttu-id="ea593-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="ea593-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="ea593-106">Вы можете протестировать и [предоставить обратную связь](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.</span><span class="sxs-lookup"><span data-stu-id="ea593-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="ea593-107">В то время как экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="ea593-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="ea593-108">Включаем экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ea593-108">Turn on experimental features</span></span>  

<span data-ttu-id="ea593-109">Чтобы включить экспериментальные функции \(или off\) в Microsoft Edge, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea593-110">[Откройте DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="ea593-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="ea593-111">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ea593-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="ea593-112">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="ea593-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="ea593-113">Откройте области [Параметры.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="ea593-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="ea593-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="ea593-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="ea593-115">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="ea593-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="ea593-116">На левой стороне области **Параметры** выберите раздел **Эксперименты.**</span><span class="sxs-lookup"><span data-stu-id="ea593-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница Эксперименты в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="ea593-118">Страница **Эксперименты** в **параметрах**</span><span class="sxs-lookup"><span data-stu-id="ea593-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ea593-119">На странице **Эксперименты** прокрутите список всех доступных экспериментальных функций и выберите почтовый ящик рядом с каждой функцией, которую необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="ea593-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="ea593-120">Закрыть и открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="ea593-121">Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="ea593-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="ea593-122">Чтобы отключить экспериментальную функцию, откройте страницу **Эксперименты** и закройте контрольный ящик экспериментальной функции, которую необходимо отключить.</span><span class="sxs-lookup"><span data-stu-id="ea593-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="ea593-123">Основные экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ea593-123">Highlighted experimental features</span></span>  

<span data-ttu-id="ea593-124">В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea593-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="ea593-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ea593-125">Experimental feature</span></span> | <span data-ttu-id="ea593-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ea593-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="ea593-127">Включить веб-хинт</span><span class="sxs-lookup"><span data-stu-id="ea593-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="ea593-128">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-128">85 or later</span></span> |  
| [<span data-ttu-id="ea593-129">Включить консоль сети</span><span class="sxs-lookup"><span data-stu-id="ea593-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="ea593-130">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-130">85 or later</span></span> |  
| [<span data-ttu-id="ea593-131">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="ea593-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="ea593-132">86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-132">86 or later</span></span> |  
| [<span data-ttu-id="ea593-133">Включить композитные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="ea593-133">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="ea593-134">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-134">87 or later</span></span> |  
| [<span data-ttu-id="ea593-135">Включить новый инструмент редактора шрифта в области Стилей</span><span class="sxs-lookup"><span data-stu-id="ea593-135">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="ea593-136">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-136">89 or later</span></span> |  
| [<span data-ttu-id="ea593-137">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="ea593-137">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="ea593-138">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-138">89 or later</span></span> |  
| [<span data-ttu-id="ea593-139">Включить меню вкладок + кнопки, чтобы открыть дополнительные средства</span><span class="sxs-lookup"><span data-stu-id="ea593-139">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="ea593-140">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-140">89 or later</span></span> |  
| [<span data-ttu-id="ea593-141">Включить вкладку Welcome</span><span class="sxs-lookup"><span data-stu-id="ea593-141">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="ea593-142">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ea593-142">89 or later</span></span> |  

### <a name="enable-webhint"></a><span data-ttu-id="ea593-143">Включить веб-хинт</span><span class="sxs-lookup"><span data-stu-id="ea593-143">Enable webhint</span></span>  

<span data-ttu-id="ea593-144">[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ea593-144">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="ea593-145">Тип обратной связи, предоставляемый [веб-сайтом][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="ea593-145">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="ea593-146">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="ea593-146">accessibility</span></span>  
*   <span data-ttu-id="ea593-147">совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="ea593-147">cross-browser compatibility</span></span>  
*   <span data-ttu-id="ea593-148">безопасность"</span><span class="sxs-lookup"><span data-stu-id="ea593-148">security</span></span>  
*   <span data-ttu-id="ea593-149">производительность</span><span class="sxs-lookup"><span data-stu-id="ea593-149">performance</span></span>  
*   <span data-ttu-id="ea593-150">Прогрессивные веб-приложения (PWAs)</span><span class="sxs-lookup"><span data-stu-id="ea593-150">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="ea593-151">другие распространенные проблемы веб-разработки</span><span class="sxs-lookup"><span data-stu-id="ea593-151">other common web development issues</span></span>  
    
<span data-ttu-id="ea593-152">Эксперимент [webhint][WebhintMain] отображает обратную связь веб-хинта в панели [Issues.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="ea593-152">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="ea593-153">Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ea593-153">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="ea593-154">Выберите ссылку на ресурс, чтобы открыть **соответствующую**сеть, **источники**или **элементов** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-154">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="ea593-156">webhint feedback in the **Issues** panel</span><span class="sxs-lookup"><span data-stu-id="ea593-156">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="ea593-157">Включить консоль сети</span><span class="sxs-lookup"><span data-stu-id="ea593-157">Enable Network Console</span></span>  

<span data-ttu-id="ea593-158">**Network Console** — это рабочее название эксперимента по синтетическому запросу сети по HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea593-158">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="ea593-159">Вы можете использовать эксперимент **сетевой консоли** для отправки запросов веб-API.</span><span class="sxs-lookup"><span data-stu-id="ea593-159">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="ea593-160">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-160">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ea593-161">Для использования **сетевой консоли**выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-161">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea593-162">Откройте **области Сети.**</span><span class="sxs-lookup"><span data-stu-id="ea593-162">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="ea593-163">Найдите сетевой запрос, который необходимо изменить и повторно изменить.</span><span class="sxs-lookup"><span data-stu-id="ea593-163">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="ea593-164">Откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.</span><span class="sxs-lookup"><span data-stu-id="ea593-164">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="ea593-165">При **открываемой сетевой** консоли отредактируете сведения о запросе сети.</span><span class="sxs-lookup"><span data-stu-id="ea593-165">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="ea593-166">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ea593-166">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Консоль сети в ящике консоли" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="ea593-168">**Консоль сети** в **ящике консоли**</span><span class="sxs-lookup"><span data-stu-id="ea593-168">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="ea593-169">Source Order Viewer</span><span class="sxs-lookup"><span data-stu-id="ea593-169">Source Order Viewer</span></span>  

<span data-ttu-id="ea593-170">**Source Order Viewer** — это эксперимент, который отображает порядок элементов в источнике веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="ea593-170">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="ea593-171">Порядок отображения на экране может отличаться от порядка источника, что сбивает с толку читателя экрана и пользователей клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ea593-171">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="ea593-172">Чтобы **найти** различия между порядком отображения на экране и порядком источника, используйте эксперимент по просмотру исходных порядков.</span><span class="sxs-lookup"><span data-stu-id="ea593-172">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="ea593-173">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-173">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ea593-174">Чтобы использовать **viewer source order,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-174">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea593-175">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="ea593-175">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="ea593-176">Откройте панель **доступности** в панели ящика \(bottom\) .</span><span class="sxs-lookup"><span data-stu-id="ea593-176">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="ea593-177">В разделе **Просмотр источника порядка** выберите почтовый ящик Показать **исходный** порядок.</span><span class="sxs-lookup"><span data-stu-id="ea593-177">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="ea593-178">Выделение любого элемента HTML для отображения наложения, указываемой на источник веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="ea593-178">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Для просмотра исходных заказов в области доступности" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="ea593-180">**Для просмотра исходных заказов** в **области доступности**</span><span class="sxs-lookup"><span data-stu-id="ea593-180">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="ea593-181">Включить композитные слои в 3D-представлении</span><span class="sxs-lookup"><span data-stu-id="ea593-181">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="ea593-182">Теперь можно визуализировать Слои вместе с индексами z и объектной моделью документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="ea593-182">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="ea593-183">Эта функция позволяет отключить, не переключая контексты так часто.</span><span class="sxs-lookup"><span data-stu-id="ea593-183">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="ea593-184">Вы определили, что уменьшение переключения контекста является основной проблемой.</span><span class="sxs-lookup"><span data-stu-id="ea593-184">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="ea593-185">Не всегда понятно, как код, который вы пишете, влияет на ваше веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="ea593-185">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="ea593-186">Для обеспечения комплексного визуального интерфейса отладки трехмерное представление и составные слои теперь объединены.</span><span class="sxs-lookup"><span data-stu-id="ea593-186">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="ea593-187">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-187">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ea593-188">Чтобы использовать **композитные слои,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-188">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea593-189">В ящике выберите **средство 3D View.**</span><span class="sxs-lookup"><span data-stu-id="ea593-189">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="ea593-190">Откройте области **Композитные слои.**</span><span class="sxs-lookup"><span data-stu-id="ea593-190">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="ea593-191">Отображаются все расписные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="ea593-191">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="ea593-192">Попробуйте эту функцию с помощью собственных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="ea593-192">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="ea593-194">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="ea593-194">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="ea593-195">Включить новый инструмент редактора шрифта в области Стилей</span><span class="sxs-lookup"><span data-stu-id="ea593-195">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="ea593-196">Теперь для редактирования шрифтов можно использовать новый визуальный [редактор][DevtoolsInspectStylesEditFonts] шрифтов.</span><span class="sxs-lookup"><span data-stu-id="ea593-196">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="ea593-197">Используйте его для определения шрифтов и характеристик шрифтов.</span><span class="sxs-lookup"><span data-stu-id="ea593-197">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="ea593-198">Визуальный **редактор шрифта** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-198">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="ea593-199">Переключение между единицами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="ea593-199">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="ea593-200">Переключатель между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="ea593-200">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="ea593-201">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="ea593-201">Convert units</span></span>  
*   <span data-ttu-id="ea593-202">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="ea593-202">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="ea593-203">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-203">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ea593-204">Чтобы использовать новый визуальный **редактор шрифтов,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ea593-204">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea593-205">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="ea593-205">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="ea593-206">Откройте области **стилей.**</span><span class="sxs-lookup"><span data-stu-id="ea593-206">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="ea593-207">Выберите **значок Редактор шрифта.**</span><span class="sxs-lookup"><span data-stu-id="ea593-207">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="ea593-208">Дополнительные сведения о новом редакторе визуальных шрифтов **перейдите**к редактированию стилей и параметров шрифта CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="ea593-208">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена поле редактора визуальных шрифтов" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="ea593-210">Выделена поле **редактора** визуальных шрифтов</span><span class="sxs-lookup"><span data-stu-id="ea593-210">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="ea593-211">Включить новые функции отладки CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="ea593-211">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="ea593-212">Эта экспериментальная функция предоставляет множество новых визуализаций, которые помогут отламыть макеты CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="ea593-212">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="ea593-213">Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-213">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="ea593-214">Отображение постоянных наложения на макеты Flexbox с помощью средства Inspect</span><span class="sxs-lookup"><span data-stu-id="ea593-214">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="ea593-215">Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Flexbox на веб-сайте, зависая на них с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ea593-215">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="ea593-216">Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-216">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="ea593-217">Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера flex.</span><span class="sxs-lookup"><span data-stu-id="ea593-217">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="ea593-219">Отображение контейнеров Flexbox с помощью средства **Inspect**</span><span class="sxs-lookup"><span data-stu-id="ea593-219">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="ea593-220">Отображение настойчивых наложения на макеты Flexbox</span><span class="sxs-lookup"><span data-stu-id="ea593-220">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="ea593-221">В microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения на макеты Flexbox.</span><span class="sxs-lookup"><span data-stu-id="ea593-221">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="ea593-222">Постоянные наложения предоставляют следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="ea593-222">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="ea593-223">Постоянные наложения остаются видимыми на веб-странице во время прокрутки, перемещения мыши и использования других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-223">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="ea593-224">Одновременно можно использовать несколько настойчивых накладок, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.</span><span class="sxs-lookup"><span data-stu-id="ea593-224">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="ea593-225">Постоянные наложения предлагают параметры цветовой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ea593-225">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="ea593-226">Чтобы отладить постоянные наложения на макет Flexbox, используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="ea593-226">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="ea593-227">Выберите **значок овального** ящика Flexbox рядом с любым контейнером Flexbox, отображаемым в дереве DOM средства **Elements.**</span><span class="sxs-lookup"><span data-stu-id="ea593-227">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="ea593-228">Откройте новую панель **Макета,** расположенную в средстве **Elements,** и выберите контрольный ящик рядом с каждым контейнером Flexbox, который необходимо выделить.</span><span class="sxs-lookup"><span data-stu-id="ea593-228">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex icons and Layout panel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="ea593-230">Flex icons and **Layout** panel in DevTools</span><span class="sxs-lookup"><span data-stu-id="ea593-230">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="ea593-231">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="ea593-231">Configure persistent overlays</span></span>  

<span data-ttu-id="ea593-232">Чтобы настроить параметры для настойчивых накладок для сетки CSS или макетов Flexbox, используйте **области макета.**</span><span class="sxs-lookup"><span data-stu-id="ea593-232">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="ea593-233">Области **макета** расположен в **инструменте Elements** рядом со **стилями** и **вычислительными** стемнами.</span><span class="sxs-lookup"><span data-stu-id="ea593-233">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="ea593-235">Панель макета</span><span class="sxs-lookup"><span data-stu-id="ea593-235">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="ea593-236">Включить меню вкладок + кнопки, чтобы открыть дополнительные средства</span><span class="sxs-lookup"><span data-stu-id="ea593-236">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="ea593-237">Теперь можно открыть дополнительные средства с помощью нового значка **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="ea593-237">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="ea593-238">После включения меню вкладок **Включить +** кнопки, чтобы открыть дополнительные средства эксперимента и перезагрузить DevTools, плюс знак \( \) отображает справа от группы вкладок в верхней части `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-238">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="ea593-239">Чтобы отобразить список других средств, которые можно добавить в вкладку, выберите значок **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="ea593-239">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="ea593-241">**Дополнительные средства** в верхней области</span><span class="sxs-lookup"><span data-stu-id="ea593-241">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="ea593-242">Включить средство Welcome</span><span class="sxs-lookup"><span data-stu-id="ea593-242">Enable Welcome tool</span></span>

<span data-ttu-id="ea593-243">Этот эксперимент заменяет средство **What's New** новым средством **Welcome.**</span><span class="sxs-lookup"><span data-stu-id="ea593-243">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="ea593-244">Он отображает обновленный дизайн для следующего контента.</span><span class="sxs-lookup"><span data-stu-id="ea593-244">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="ea593-245">Ссылки на документы разработчика</span><span class="sxs-lookup"><span data-stu-id="ea593-245">Links to developer docs</span></span>  
*   <span data-ttu-id="ea593-246">последние функции</span><span class="sxs-lookup"><span data-stu-id="ea593-246">the latest features</span></span>  
*   <span data-ttu-id="ea593-247">заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ea593-247">release notes</span></span>  
*   <span data-ttu-id="ea593-248">Возможность связаться с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ea593-248">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="ea593-249">Средство **Welcome** автоматически открывается после каждого обновления microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ea593-249">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="ea593-250">Чтобы предотвратить отображение средства **Welcome** после каждого обновления, закройте почтовый ящик рядом с вкладками **Open** после каждого обновления под заголовком **Welcome** tool.</span><span class="sxs-lookup"><span data-stu-id="ea593-250">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="ea593-251">Если вы предпочитаете оригинальный инструмент **What's New,** перейдите в [Параметры][DevtoolsCustomizeIndexSettings]Эксперименты и удалите почтовый ящик рядом со вкладками  >  \*\*\*\* **Enable Welcome.**</span><span class="sxs-lookup"><span data-stu-id="ea593-251">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство welcome" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="ea593-253">**Средство welcome**</span><span class="sxs-lookup"><span data-stu-id="ea593-253">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="ea593-254">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ea593-254">Previous experimental features</span></span>  

*   <span data-ttu-id="ea593-255">[3D View][Devtools3dViewIndex] теперь доступен и включен по умолчанию в microsoft Edge версии 83 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-255">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="ea593-256">[Включив поддержку, чтобы][DevtoolsCustomizeIndex] переместить вкладки между панелями, теперь доступна и включена по умолчанию в microsoft Edge версии 85 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-256">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="ea593-257">[Совпадение клавиш в DevTools][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] с Microsoft Visual Studio код теперь доступен и включен по умолчанию в microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-257">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="ea593-258">Редактирование клавиш для любого действия [в DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] теперь доступно и включено по умолчанию в microsoft Edge версии 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-258">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="ea593-259">[Включив новые функции отладки сетки CSS,][DevtoolsCssGrid] теперь доступны и включены по умолчанию в версии Microsoft Edge 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-259">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="ea593-260">[Эмуляция. Поддержка режима двойного экрана][DevtoolsDeviceModeDualScreenAndFoldables] теперь доступна и включена по умолчанию в версии Microsoft Edge 90 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ea593-260">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="ea593-261">Предоставление отзывов по экспериментальным функциям</span><span class="sxs-lookup"><span data-stu-id="ea593-261">Providing feedback on experimental features</span></span>  

<span data-ttu-id="ea593-262">Предоставление отзывов об экспериментах Microsoft Edge DevTools или о чем-либо другом, связанном с DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea593-262">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="ea593-263">Отправка отзывов с помощью **значка Отправка отзывов** в DevTools</span><span class="sxs-lookup"><span data-stu-id="ea593-263">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="ea593-264">Чирикать [в @EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="ea593-264">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ea593-266">Значок **Отправка отзывов** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ea593-266">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Трехмерное представление | Документация Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверьте сетку CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Редактирование клавиш для любого действия в devTools | Документы Майкрософт"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Совпадение клавиш в DevTools с microsoft Visual Studio code | Документы Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsIssuesIndex]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмулировать устройства с двойным экраном и складными устройствами в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
