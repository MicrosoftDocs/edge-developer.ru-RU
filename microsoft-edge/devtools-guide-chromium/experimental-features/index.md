---
description: Последние экспериментальные функции в Microsoft Edge DevTools
title: Экспериментальные функции
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, эксперимент
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: c76830cb8bbcc597aa026f58e1926cd2f9bc2d62
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439586"
---
# <a name="experimental-features"></a><span data-ttu-id="ed577-104">Экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ed577-104">Experimental features</span></span>  

<span data-ttu-id="ed577-105">Microsoft Edge DevTools предоставляет доступ к экспериментальным функциям, которые еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="ed577-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="ed577-106">Вы можете протестировать и [предоставить обратную связь](#providing-feedback-on-experimental-features) перед тем, как будет выпущена каждая функция.</span><span class="sxs-lookup"><span data-stu-id="ed577-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="ed577-107">В то время как экспериментальные функции доступны во всех каналах Microsoft Edge, вы можете получить последние экспериментальные функции с помощью канала Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="ed577-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="ed577-108">Включаем экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ed577-108">Turn on experimental features</span></span>  

<span data-ttu-id="ed577-109">Чтобы включить экспериментальные функции \(или off\) в Microsoft Edge, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="ed577-110">[Откройте DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="ed577-110">[Open DevTools][DevtoolsOpenIndex].</span></span>  
    *   <span data-ttu-id="ed577-111">Выберите `Control` + `Shift` + `I` \(Windows, Linux\) `Command` + `Option` + `I` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ed577-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="ed577-112">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="ed577-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="ed577-113">Откройте области [Параметры.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="ed577-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="ed577-114">Выберите `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="ed577-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="ed577-115">Дополнительные сведения перейдите к [клавишам Microsoft Edge DevTools.][DevtoolsShortcutsIndex]</span><span class="sxs-lookup"><span data-stu-id="ed577-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevtoolsShortcutsIndex].</span></span>  
1.  <span data-ttu-id="ed577-116">На левой стороне области **Параметры** выберите раздел **Эксперименты.**</span><span class="sxs-lookup"><span data-stu-id="ed577-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="Страница Эксперименты в параметрах" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="ed577-118">Страница **Эксперименты** в **параметрах**</span><span class="sxs-lookup"><span data-stu-id="ed577-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ed577-119">На странице **Эксперименты** прокрутите список всех доступных экспериментальных функций и выберите почтовый ящик рядом с каждой функцией, которую необходимо протестировать.</span><span class="sxs-lookup"><span data-stu-id="ed577-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="ed577-120">Закрыть и открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="ed577-121">Экспериментальные функции постоянно обновляются и могут вызывать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="ed577-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="ed577-122">Чтобы отключить экспериментальную функцию, откройте страницу **Эксперименты** и закройте контрольный ящик экспериментальной функции, которую необходимо отключить.</span><span class="sxs-lookup"><span data-stu-id="ed577-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="ed577-123">Основные экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ed577-123">Highlighted experimental features</span></span>  

<span data-ttu-id="ed577-124">В следующих разделах описываются новые экспериментальные функции, доступные в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ed577-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="ed577-125">Экспериментальная функция</span><span class="sxs-lookup"><span data-stu-id="ed577-125">Experimental feature</span></span> | <span data-ttu-id="ed577-126">Версия Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ed577-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | <span data-ttu-id="ed577-127">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-127">85 or later</span></span> |  
| [Enable Network Console](#enable-network-console) | <span data-ttu-id="ed577-128">85 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-128">85 or later</span></span> |  
| [Source Order Viewer](#source-order-viewer) | <span data-ttu-id="ed577-129">86 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-129">86 or later</span></span> |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | <span data-ttu-id="ed577-130">87 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-130">87 or later</span></span> |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="ed577-131">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-131">89 or later</span></span> |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="ed577-132">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-132">89 or later</span></span> |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="ed577-133">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-133">89 or later</span></span> |  
| [Enable Welcome tab](#enable-welcome-tab) | <span data-ttu-id="ed577-134">89 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ed577-134">89 or later</span></span> |  

### Enable webhint  

<span data-ttu-id="ed577-135">[webhint —][WebhintMain] это средство с открытым исходным кодом, которое обеспечивает обратную связь в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ed577-135">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="ed577-136">Тип обратной связи, предоставляемый [веб-сайтом][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="ed577-136">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="ed577-137">специальные возможности</span><span class="sxs-lookup"><span data-stu-id="ed577-137">accessibility</span></span>  
*   <span data-ttu-id="ed577-138">совместимость между браузерами</span><span class="sxs-lookup"><span data-stu-id="ed577-138">cross-browser compatibility</span></span>  
*   <span data-ttu-id="ed577-139">безопасность"</span><span class="sxs-lookup"><span data-stu-id="ed577-139">security</span></span>  
*   <span data-ttu-id="ed577-140">производительность</span><span class="sxs-lookup"><span data-stu-id="ed577-140">performance</span></span>  
*   <span data-ttu-id="ed577-141">Прогрессивные веб-приложения (PWAs)</span><span class="sxs-lookup"><span data-stu-id="ed577-141">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="ed577-142">другие распространенные проблемы веб-разработки</span><span class="sxs-lookup"><span data-stu-id="ed577-142">other common web development issues</span></span>  
    
<span data-ttu-id="ed577-143">Эксперимент [webhint][WebhintMain] отображает обратную связь веб-хинта в панели [Issues.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="ed577-143">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssuesIndex] panel.</span></span>  <span data-ttu-id="ed577-144">Выберите проблему, чтобы отобразить документацию по решению и список затронутых ресурсов на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="ed577-144">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="ed577-145">Выберите ссылку на ресурс, чтобы открыть **соответствующую**сеть, **источники**или **элементов** в DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-145">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="webhint feedback in the Issues panel" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="ed577-147">webhint feedback in the **Issues** panel</span><span class="sxs-lookup"><span data-stu-id="ed577-147">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

<span data-ttu-id="ed577-148">**Network Console** — это рабочее название эксперимента по синтетическому запросу сети по HTTP.</span><span class="sxs-lookup"><span data-stu-id="ed577-148">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="ed577-149">Вы можете использовать эксперимент **сетевой консоли** для отправки запросов веб-API.</span><span class="sxs-lookup"><span data-stu-id="ed577-149">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="ed577-150">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-150">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ed577-151">Для использования **сетевой консоли**выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-151">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ed577-152">Откройте **области Сети.**</span><span class="sxs-lookup"><span data-stu-id="ed577-152">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="ed577-153">Найдите сетевой запрос, который необходимо изменить и повторно изменить.</span><span class="sxs-lookup"><span data-stu-id="ed577-153">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="ed577-154">Откройте контекстное меню \(правой кнопкой мыши\) и выберите **Изменить и переиграть**.</span><span class="sxs-lookup"><span data-stu-id="ed577-154">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="ed577-155">При **открываемой сетевой** консоли отредактируете сведения о запросе сети.</span><span class="sxs-lookup"><span data-stu-id="ed577-155">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="ed577-156">Выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="ed577-156">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Консоль сети в ящике консоли" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="ed577-158">**Консоль сети** в **ящике консоли**</span><span class="sxs-lookup"><span data-stu-id="ed577-158">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

<span data-ttu-id="ed577-159">**Source Order Viewer** это эксперимент, отображает порядок элементов в источнике веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="ed577-159">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="ed577-160">Порядок отображения на экране может отличаться от порядка источника, что сбивает с толку читателя экрана и пользователей клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ed577-160">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="ed577-161">Используйте эксперимент, чтобы найти различия между порядком отображения на экране и **Source Order Viewer** порядком источника.</span><span class="sxs-lookup"><span data-stu-id="ed577-161">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="ed577-162">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-162">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ed577-163">Чтобы **Source Order Viewer** использовать, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-163">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ed577-164">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="ed577-164">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="ed577-165">Откройте панель **доступности** в панели ящика \(bottom\) .</span><span class="sxs-lookup"><span data-stu-id="ed577-165">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="ed577-166">В разделе выберите почтовый ящик **Source Order Viewer** Show Source **Order.**</span><span class="sxs-lookup"><span data-stu-id="ed577-166">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="ed577-167">Выделение любого элемента HTML для отображения наложения, указываемой на источник веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="ed577-167">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text=":::<span data-ttu-id="ed577-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox=".. /media/experiments-source-order-viewer.msft.png"::: в **Source Order Viewer** области **доступности**</span><span class="sxs-lookup"><span data-stu-id="ed577-168">no-loc(Source Order Viewer)::: in the Accessibility pane" lightbox="../media/experiments-source-order-viewer.msft.png"::: **Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

<span data-ttu-id="ed577-169">Теперь можно визуализировать Слои вместе с индексами z и объектной моделью документа \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="ed577-169">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="ed577-170">Эта функция позволяет отключить, не переключая контексты так часто.</span><span class="sxs-lookup"><span data-stu-id="ed577-170">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="ed577-171">Вы определили, что уменьшение переключения контекста является основной проблемой.</span><span class="sxs-lookup"><span data-stu-id="ed577-171">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="ed577-172">Не всегда понятно, как код, который вы пишете, влияет на ваше веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="ed577-172">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="ed577-173">Для комплексного визуального отладки теперь 3D View объединяются композитные слои и композитные слои.</span><span class="sxs-lookup"><span data-stu-id="ed577-173">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="ed577-174">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-174">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ed577-175">Чтобы использовать **композитные слои,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-175">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ed577-176">В ящике выберите **3D View** средство.</span><span class="sxs-lookup"><span data-stu-id="ed577-176">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="ed577-177">Откройте области **Композитные слои.**</span><span class="sxs-lookup"><span data-stu-id="ed577-177">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="ed577-178">Отображаются все расписные слои приложения.</span><span class="sxs-lookup"><span data-stu-id="ed577-178">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="ed577-179">Попробуйте эту функцию с помощью собственных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="ed577-179">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="ed577-181">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="ed577-181">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

<span data-ttu-id="ed577-182">Теперь для редактирования шрифтов можно использовать новый визуальный [редактор][DevtoolsInspectStylesEditFonts] шрифтов.</span><span class="sxs-lookup"><span data-stu-id="ed577-182">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="ed577-183">Используйте его для определения шрифтов и характеристик шрифтов.</span><span class="sxs-lookup"><span data-stu-id="ed577-183">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="ed577-184">Визуальный **редактор шрифта** помогает выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-184">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="ed577-185">Переключение между единицами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="ed577-185">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="ed577-186">Переключатель между ключевыми словами для различных свойств шрифта</span><span class="sxs-lookup"><span data-stu-id="ed577-186">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="ed577-187">Преобразование единиц</span><span class="sxs-lookup"><span data-stu-id="ed577-187">Convert units</span></span>  
*   <span data-ttu-id="ed577-188">Создание точного кода CSS</span><span class="sxs-lookup"><span data-stu-id="ed577-188">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="ed577-189">После включите эксперимент, убедитесь, что вы перезапустите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-189">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="ed577-190">Чтобы использовать новый визуальный **редактор шрифтов,** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed577-190">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="ed577-191">Откройте **средство Elements.**</span><span class="sxs-lookup"><span data-stu-id="ed577-191">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="ed577-192">Откройте области **стилей.**</span><span class="sxs-lookup"><span data-stu-id="ed577-192">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="ed577-193">Выберите **значок Редактор шрифта.**</span><span class="sxs-lookup"><span data-stu-id="ed577-193">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="ed577-194">Дополнительные сведения о новом редакторе визуальных шрифтов **перейдите**к редактированию стилей и параметров шрифта CSS в области [Стилей в DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="ed577-194">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Выделена поле редактора визуальных шрифтов" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="ed577-196">Выделена поле **редактора** визуальных шрифтов</span><span class="sxs-lookup"><span data-stu-id="ed577-196">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

<span data-ttu-id="ed577-197">Эта экспериментальная функция предоставляет множество новых визуализаций, которые помогут отламыть макеты CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="ed577-197">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="ed577-198">Чтобы просмотреть последние экспериментальные функции, [включайте этот эксперимент](#turn-on-experimental-features) и перезагрузите DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-198">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="ed577-199">Отображение постоянных наложения на макеты Flexbox с помощью средства Inspect</span><span class="sxs-lookup"><span data-stu-id="ed577-199">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="ed577-200">Средство **Inspect** позволяет быстро определять и визуализировать макеты CSS Flexbox на веб-сайте, зависая на них с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="ed577-200">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="ed577-201">Выберите **значок Inspect** \( Inspect \) в левом верхнем углу ![ ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-201">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="ed577-202">Затем во время отладки веб-сайта наведите курсор на гибкий контейнер, чтобы отобразить контуры вокруг контейнера flex.</span><span class="sxs-lookup"><span data-stu-id="ed577-202">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Отображение контейнеров Flexbox с помощью средства Inspect" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="ed577-204">Отображение контейнеров Flexbox с помощью средства **Inspect**</span><span class="sxs-lookup"><span data-stu-id="ed577-204">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="ed577-205">Отображение настойчивых наложения на макеты Flexbox</span><span class="sxs-lookup"><span data-stu-id="ed577-205">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="ed577-206">В microsoft Edge версии 89 или более поздней версии экспериментальная функция CSS Flexbox также предлагает возможность включить постоянные наложения на макеты Flexbox.</span><span class="sxs-lookup"><span data-stu-id="ed577-206">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="ed577-207">Постоянные наложения предоставляют следующие преимущества.</span><span class="sxs-lookup"><span data-stu-id="ed577-207">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="ed577-208">Постоянные наложения остаются видимыми на веб-странице во время прокрутки, перемещения мыши и использования других функций DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-208">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="ed577-209">Одновременно можно использовать несколько настойчивых накладок, чтобы вы могли просмотреть несколько макетов Flexbox одновременно.</span><span class="sxs-lookup"><span data-stu-id="ed577-209">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="ed577-210">Постоянные наложения предлагают параметры цветовой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ed577-210">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="ed577-211">Чтобы отладить постоянные наложения на макет Flexbox, используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="ed577-211">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="ed577-212">Выберите **значок овального** ящика Flexbox рядом с любым контейнером Flexbox, отображаемым в дереве DOM средства **Elements.**</span><span class="sxs-lookup"><span data-stu-id="ed577-212">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="ed577-213">Откройте новую панель **Макета,** расположенную в средстве **Elements,** и выберите контрольный ящик рядом с каждым контейнером Flexbox, который необходимо выделить.</span><span class="sxs-lookup"><span data-stu-id="ed577-213">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Flex icons and Layout panel in DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="ed577-215">Flex icons and **Layout** panel in DevTools</span><span class="sxs-lookup"><span data-stu-id="ed577-215">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="ed577-216">Настройка постоянных наложения</span><span class="sxs-lookup"><span data-stu-id="ed577-216">Configure persistent overlays</span></span>  

<span data-ttu-id="ed577-217">Чтобы настроить параметры для настойчивых накладок для сетки CSS или макетов Flexbox, используйте **области макета.**</span><span class="sxs-lookup"><span data-stu-id="ed577-217">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="ed577-218">Области **макета** расположен в **инструменте Elements** рядом со **стилями** и **вычислительными** стемнами.</span><span class="sxs-lookup"><span data-stu-id="ed577-218">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Панель макета" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="ed577-220">Панель макета</span><span class="sxs-lookup"><span data-stu-id="ed577-220">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

<span data-ttu-id="ed577-221">Теперь можно открыть дополнительные средства с помощью нового значка **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="ed577-221">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="ed577-222">После включив эксперимент и перезагрузив DevTools, знак плюс \( \) отображает справа от группы вкладок в верхней части **Enable + button tab menus to open more tools** `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-222">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="ed577-223">Чтобы отобразить список других средств, которые можно добавить в вкладку, выберите значок **More Tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="ed577-223">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Дополнительные средства в верхней области" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="ed577-225">**Дополнительные средства** в верхней области</span><span class="sxs-lookup"><span data-stu-id="ed577-225">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

<span data-ttu-id="ed577-226">Этот эксперимент заменяет средство **What's New** новым средством **Welcome.**</span><span class="sxs-lookup"><span data-stu-id="ed577-226">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="ed577-227">Он отображает обновленный дизайн для следующего контента.</span><span class="sxs-lookup"><span data-stu-id="ed577-227">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="ed577-228">Ссылки на документы разработчика</span><span class="sxs-lookup"><span data-stu-id="ed577-228">Links to developer docs</span></span>  
*   <span data-ttu-id="ed577-229">последние функции</span><span class="sxs-lookup"><span data-stu-id="ed577-229">the latest features</span></span>  
*   <span data-ttu-id="ed577-230">заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ed577-230">release notes</span></span>  
*   <span data-ttu-id="ed577-231">Возможность связаться с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ed577-231">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="ed577-232">Средство **Welcome** автоматически открывается после каждого обновления microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ed577-232">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="ed577-233">Чтобы предотвратить отображение средства **Welcome** после каждого обновления, закройте почтовый ящик рядом с вкладками **Open** после каждого обновления под заголовком **Welcome** tool.</span><span class="sxs-lookup"><span data-stu-id="ed577-233">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="ed577-234">Если вы предпочитаете оригинальный **инструмент What's New,** перейдите к [параметрам][DevtoolsCustomizeIndexSettings]  >  **Эксперименты** и удалите контрольный ящик рядом **Enable Welcome tab** с .</span><span class="sxs-lookup"><span data-stu-id="ed577-234">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Средство welcome" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="ed577-236">**Средство welcome**</span><span class="sxs-lookup"><span data-stu-id="ed577-236">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="ed577-237">Предыдущие экспериментальные функции</span><span class="sxs-lookup"><span data-stu-id="ed577-237">Previous experimental features</span></span>  

*   <span data-ttu-id="ed577-238">[3D View][Devtools3dViewIndex] теперь доступна и включена по умолчанию в microsoft Edge версии 83 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-238">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="ed577-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] теперь доступна и включена по умолчанию в Microsoft Edge версии 85 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-239">[Turn on support to move tabs between panels][DevtoolsCustomizeIndex] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="ed577-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] теперь доступна и включена по умолчанию в microsoft Edge версии 86 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-240">[Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="ed577-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-241">[Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="ed577-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] теперь доступна и включена по умолчанию в microsoft Edge версии 89 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-242">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="ed577-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] теперь доступна и включена по умолчанию в microsoft Edge версии 90 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ed577-243">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 90 or later.</span></span>  

## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="ed577-244">Предоставление отзывов по экспериментальным функциям</span><span class="sxs-lookup"><span data-stu-id="ed577-244">Providing feedback on experimental features</span></span>  

<span data-ttu-id="ed577-245">Предоставление отзывов об экспериментах Microsoft Edge DevTools или о чем-либо другом, связанном с DevTools.</span><span class="sxs-lookup"><span data-stu-id="ed577-245">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="ed577-246">Отправка отзывов с помощью **значка Отправка отзывов** в DevTools</span><span class="sxs-lookup"><span data-stu-id="ed577-246">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="ed577-247">Чирикать [в @EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="ed577-247">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ed577-249">Значок **Отправка отзывов** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ed577-249">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "::::no-loc (3D View)::: | Документы Майкрософт"  
[DevtoolsCssGrid]: ../css/grid.md "Проверьте сетку CSS в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Настройка Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools ":Изменить клавиши клавиш для любого действия в DevTools | Документы Майкрософт"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Сочетания клавиш в DevTools для Microsoft Visual Studio Code | Документы Майкрософт"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильных устройств с помощью режима устройства в Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Изменение стилей и параметров шрифтов CSS в области Стилей в DevTools | Документы Майкрософт"  
[DevtoolsIssuesIndex]: ../issues/index.md "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsOpenIndex]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Клавиши Microsoft Edge DevTools | Документы Майкрософт"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Эмулировать устройства с двойным экраном и складными устройствами в Microsoft Edge DevTools | Документы Майкрософт"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
