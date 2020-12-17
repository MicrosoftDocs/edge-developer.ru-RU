---
description: Microsoft Edge в Linux, улучшенные советы webhint в средстве "Проблемы", новые функции отладки служебного сценария и т. д.
title: Что нового в средствах разработчика (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: a9c262075f3d541861ed825a8da96b3a86956c0e
ms.sourcegitcommit: c06a4ece7bcbfeae4677d15fca677ca42a0373b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2020
ms.locfileid: "11229480"
---
# <span data-ttu-id="69390-104">Что нового в средствах разработчика (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="69390-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="69390-105">Microsoft Edge и Microsoft Edge Driver теперь доступны в Linux</span><span class="sxs-lookup"><span data-stu-id="69390-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="69390-106">Microsoft Edge Dev теперь поддерживается в дистрибутивах Ubuntu, Debian, Fedora и openSUSE.</span><span class="sxs-lookup"><span data-stu-id="69390-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="69390-107">Скачайте и установите пакет Microsoft Edge Dev `.deb` или `.rpm` непосредственно с сайта [программы предварительной оценки Microsoft Edge][MicrosoftinsiderDownloadPlatformLinux] или используйте стандартные средства управления пакетами своего дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="69390-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="69390-108">Если вы используете среду Linux в решениях непрерывной интеграции и доставки \(CI/CD\), Microsoft Edge Driver также доступен в Linux.</span><span class="sxs-lookup"><span data-stu-id="69390-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="69390-109">Чтобы начать автоматизацию Microsoft Edge Dev с использованием Microsoft Edge Driver, перейдите на страницу [загрузок Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="69390-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="69390-110">Справку по автоматизации Microsoft Edge Dev вместе с Microsoft Edge Driver см. в статье [Использование WebDriver (Chromium) для автоматизации тестов][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="69390-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="Средства разработчика в Microsoft Edge в Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="69390-112">Средства разработчика в Microsoft Edge в Linux</span><span class="sxs-lookup"><span data-stu-id="69390-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="69390-113">Улучшенные советы webhint и платформы в средстве "Проблемы"</span><span class="sxs-lookup"><span data-stu-id="69390-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="69390-114">Средство с открытым кодом [webhint][WebhintMain]предоставляет отзывы в режиме реального времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="69390-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="69390-115">С [Microsoft Edge версии 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel] отзывы webhint доступны в средстве [Проблемы][DevtoolsIssuesIndex].</span><span class="sxs-lookup"><span data-stu-id="69390-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="69390-116">Проблемы, отображаемые в средстве **Проблемы**, теперь проще просматривать благодаря добавлению следующих категорий.</span><span class="sxs-lookup"><span data-stu-id="69390-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="69390-117">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="69390-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="69390-118">Совместимость</span><span class="sxs-lookup"><span data-stu-id="69390-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="69390-119">Производительность</span><span class="sxs-lookup"><span data-stu-id="69390-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="69390-120">Ошибки</span><span class="sxs-lookup"><span data-stu-id="69390-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="69390-121">PWA</span><span class="sxs-lookup"><span data-stu-id="69390-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="69390-122">Безопасность</span><span class="sxs-lookup"><span data-stu-id="69390-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="69390-123">Теперь вы можете отфильтровать сторонние проблемы с помощью новой галочки.</span><span class="sxs-lookup"><span data-stu-id="69390-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="69390-124">Функция фильтрации помогает скрыть проблемы, связанные с кодом сторонних библиотек или других источников.</span><span class="sxs-lookup"><span data-stu-id="69390-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="69390-125">Чтобы помочь с просмотром проблем, выявленных инструментом [webhint][WebhintMain], средство **Проблемы** теперь отображает следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="69390-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="69390-126">Улучшенные фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="69390-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="69390-127">Ссылки на другие связанные панели.</span><span class="sxs-lookup"><span data-stu-id="69390-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="69390-128">Ссылки на документацию по устранению проблем на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="69390-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Средство "Проблемы"" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="69390-130">Средство **Проблемы**</span><span class="sxs-lookup"><span data-stu-id="69390-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="69390-131">Составные слои теперь находятся в трехмерном представлении</span><span class="sxs-lookup"><span data-stu-id="69390-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="69390-132">Теперь вы можете визуализировать содержимое **Слои** вместе со значениями z-index и объектной моделью документов \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="69390-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="69390-133">Эта функция помогает выполнять отладку без частого переключения между средствами [Трехмерное представление][Devtools3dViewIndex] и **Слои**.</span><span class="sxs-lookup"><span data-stu-id="69390-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="69390-134">Для обеспечения комплексного визуального интерфейса отладки [трехмерное представление и составные слои теперь объединены][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="69390-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Панель "Составные слои"" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="69390-136">Панель **Составные слои**</span><span class="sxs-lookup"><span data-stu-id="69390-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="69390-137">Определения переменных CSS в панели "Стили"</span><span class="sxs-lookup"><span data-stu-id="69390-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="69390-138">В панели **Стили** [переменные CSS][MdnUsingCssCustomProperties] теперь связаны непосредственно с каждым определением.</span><span class="sxs-lookup"><span data-stu-id="69390-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="69390-139">Выберите переменную, чтобы легко просмотреть или изменить определение переменной CSS.</span><span class="sxs-lookup"><span data-stu-id="69390-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="69390-140">В этом примере средства разработчика отображают атрибуты CSS для элемента `body`.</span><span class="sxs-lookup"><span data-stu-id="69390-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="69390-141">Чтобы отобразить определение переменной CSS `--theme-body-background`, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-142">В области **Стили** выберите `var(--theme-body-background)`.</span><span class="sxs-lookup"><span data-stu-id="69390-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="69390-143">В области **Стили** отобразится определение переменной CSS `--theme-body-background`.</span><span class="sxs-lookup"><span data-stu-id="69390-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Переменная CSS, связанная со стилем" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="69390-145">Переменная CSS, связанная со стилем</span><span class="sxs-lookup"><span data-stu-id="69390-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Переменная CSS, связанная с целевым объектом стиля" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="69390-147">Переменная CSS, связанная с целевым объектом стиля</span><span class="sxs-lookup"><span data-stu-id="69390-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="69390-148">Улучшения отладки служебного сценария</span><span class="sxs-lookup"><span data-stu-id="69390-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="69390-149">Следующие новые функции средств [Сеть](#network-tool), [Приложение](#application-tool) и [Источники](#sources-tool) помогают создавать [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="69390-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="69390-150">Используйте следующие функции, если у вас возникли трудности при отладке служебного сценария.</span><span class="sxs-lookup"><span data-stu-id="69390-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="69390-151">Маршрутизация запросов отображает события `startup` и `fetch`, основанные на сетевых запросах, выполняемых в служебных сценариях.</span><span class="sxs-lookup"><span data-stu-id="69390-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="69390-152">Временные шкалы доступны в средстве **Приложение** или **Сеть**.</span><span class="sxs-lookup"><span data-stu-id="69390-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="69390-153">Временные шкалы удобно использовать, если у вас возникли проблемы со служебными сценариями и вы хотите проверить наличие ошибок в событиях `startup` или `fetch`.</span><span class="sxs-lookup"><span data-stu-id="69390-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="69390-154">Средство "Приложение"</span><span class="sxs-lookup"><span data-stu-id="69390-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="69390-155">Просматривайте все сведения о маршрутизации запросов служебных сценариев с помощью новой ссылки **Сетевые запросы**.</span><span class="sxs-lookup"><span data-stu-id="69390-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="69390-156">Чтобы отобразить дополнительный контекст при отладке служебного сценария, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-157">Выберите **Приложение** > **Служебные сценарии**.</span><span class="sxs-lookup"><span data-stu-id="69390-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="69390-158">Нажмите **Сетевые запросы**.</span><span class="sxs-lookup"><span data-stu-id="69390-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Открытие средства "Сеть" из панели "Служебные сценарии"" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="69390-160">Открытие средства **Сеть** из панели **Служебные сценарии**</span><span class="sxs-lookup"><span data-stu-id="69390-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="69390-161">Средство **Сеть** открывается в **консоли** и отображает все сетевые запросы, связанные со служебными сценариями.</span><span class="sxs-lookup"><span data-stu-id="69390-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="69390-162">Сетевые запросы фильтруются с помощью `is:service-worker-intercepted`.</span><span class="sxs-lookup"><span data-stu-id="69390-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Средство "Сеть" в консоли" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="69390-164">Средство **Сеть** в **консоли**</span><span class="sxs-lookup"><span data-stu-id="69390-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="69390-165">Чтобы вернуть средство **Сеть** на верхнюю панель, закройте **консоль**.</span><span class="sxs-lookup"><span data-stu-id="69390-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Закрытие консоли для возврата средства "Сеть"" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="69390-167">Закрытие **консоли** для возврата средства **Сеть**</span><span class="sxs-lookup"><span data-stu-id="69390-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="69390-168">Средство "Сеть"</span><span class="sxs-lookup"><span data-stu-id="69390-168">Network tool</span></span>  

<span data-ttu-id="69390-169">Выполняйте отладку сетевых запросов, выполняемых в служебных сценариях.</span><span class="sxs-lookup"><span data-stu-id="69390-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="69390-170">Вы также можете открывать сетевые запросы в средстве **Приложение**.</span><span class="sxs-lookup"><span data-stu-id="69390-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="69390-171">Для каждого запроса средства разработчика отображают следующие сведения в панели [Время][DevtoolsNetworkReferenceViewTimingBreakdownRequest].</span><span class="sxs-lookup"><span data-stu-id="69390-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="69390-172">Начало запроса и длительность начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="69390-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="69390-173">Изменения регистрации служебных сценариев.</span><span class="sxs-lookup"><span data-stu-id="69390-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="69390-174">Время выполнения обработчика события `fetch`.</span><span class="sxs-lookup"><span data-stu-id="69390-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="69390-175">Время выполнения всех событий `fetch` для загрузки клиента.</span><span class="sxs-lookup"><span data-stu-id="69390-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Панель "Время"" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="69390-177">Панель **Время**</span><span class="sxs-lookup"><span data-stu-id="69390-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-178">Средство "Источники"</span><span class="sxs-lookup"><span data-stu-id="69390-178">Sources tool</span></span>  

<span data-ttu-id="69390-179">В предыдущих версиях Microsoft Edge глубина в стеке вызовов была ограничена кодом JavaScript в вашем служебном сценарии.</span><span class="sxs-lookup"><span data-stu-id="69390-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="69390-180">Теперь в Microsoft Edge 88 стек вызовов отображает инициатора запросов, выполняемых в служебном сценарии.</span><span class="sxs-lookup"><span data-stu-id="69390-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="69390-181">Чтобы найти инициатора запроса, используйте стек вызовов своего кода JavaScript в служебном сценарии.</span><span class="sxs-lookup"><span data-stu-id="69390-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="69390-182">Стек вызовов на следующих рисунках начинается с кода JavaScript в вашем служебном сценарии и отображает ссылку на исходный запрос веб-страницы как `(index):157`.</span><span class="sxs-lookup"><span data-stu-id="69390-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="69390-183">На втором рисунке выбрана ссылка и открыт инициатор, выполнивший запрос.</span><span class="sxs-lookup"><span data-stu-id="69390-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="69390-184">Инициатором на втором рисунке является веб-страница.</span><span class="sxs-lookup"><span data-stu-id="69390-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Файл service-worker.js и стек вызовов с выделением инициатора запроса" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="69390-186">Файл `service-worker.js` и стек вызовов с выделением инициатора запроса</span><span class="sxs-lookup"><span data-stu-id="69390-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Веб-страница (индекс) является инициатором запроса" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="69390-188">Веб-страница `(index)` является инициатором запроса</span><span class="sxs-lookup"><span data-stu-id="69390-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="69390-189">Копирование значения свойства сетевого запроса</span><span class="sxs-lookup"><span data-stu-id="69390-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="69390-190">В средстве **Сеть** скопируйте значение свойства сетевого запроса с помощью нового параметра **Копировать значение**.</span><span class="sxs-lookup"><span data-stu-id="69390-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="69390-191">Значение свойства копируется в виде декодированного значения JSON.</span><span class="sxs-lookup"><span data-stu-id="69390-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="69390-192">В предыдущих версиях Microsoft Edge вам приходилось копировать значение с помощью одного из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="69390-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="69390-193">Выделение всего текста и его копирование.</span><span class="sxs-lookup"><span data-stu-id="69390-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="69390-194">Сохранение значения в качестве глобальной переменной (если применимо) и копирование его из вкладки [Консоль][DevtoolsConsoleIndex] средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="69390-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="69390-195">Сведения о копирования значения свойства в буфер обмена см. в разделе[Копирование форматированного отклика JSON в буфер обмена][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="69390-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="69390-196">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="69390-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Копирование значения свойства в средствах разработчика" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="69390-198">Копирование значения свойства в средствах разработчика</span><span class="sxs-lookup"><span data-stu-id="69390-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Вставка значения свойства в Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="69390-200">Вставка значения свойства в Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="69390-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="69390-201">Настройка сочетания клавиш с несколькими нажатиями</span><span class="sxs-lookup"><span data-stu-id="69390-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="69390-202">[С Microsoft Edge версии 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings] вы можете настраивать сочетания клавиш для любого действия в средствах разработчика.</span><span class="sxs-lookup"><span data-stu-id="69390-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="69390-203">В Microsoft Edge версии 88 теперь можно создавать сочетания клавиш с несколькими нажатиями.</span><span class="sxs-lookup"><span data-stu-id="69390-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="69390-204">Чтобы настроить сочетание клавиш для действия в средствах разработчика, перейдите в раздел [Параметры][DevtoolsCustomizeIndexSettings] > **Эксперименты** и установите флажок **Enable keyboard shortcut editor** (Включить редактор сочетания клавиш).</span><span class="sxs-lookup"><span data-stu-id="69390-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="69390-205">Дополнительные сведения о настройке и изменении сочетаний клавиш см. в разделе о [включении экспериментальной функции редактора сочетания клавиш][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="69390-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="69390-206">Например, красное выделение отображает сочетание клавиш с несколькими нажатиями, настроенное для действия **Начать запись событий**.</span><span class="sxs-lookup"><span data-stu-id="69390-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="69390-207">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="69390-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Аккордные сочетания клавиш" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="69390-209">Сочетания клавиш с несколькими нажатиями</span><span class="sxs-lookup"><span data-stu-id="69390-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="69390-210">Средства разработчика теперь соответствуют языку браузера</span><span class="sxs-lookup"><span data-stu-id="69390-210">DevTools now match browser language</span></span>  

<span data-ttu-id="69390-211">В Microsoft Edge версии 87, если вы включали параметр **Согласовать язык браузера** в [параметрах средств разработчика][DevtoolsCustomizeIndexSettings], язык средств разработчика не совпадал с языком браузера.</span><span class="sxs-lookup"><span data-stu-id="69390-211">In Microsoft Edge version 87, if you turned on the **Match browser language** setting in [DevTools Settings][DevtoolsCustomizeIndexSettings], DevTools did not match the browser language.</span></span>  <span data-ttu-id="69390-212">В Microsoft Edge версии 88 средства разработчика соответствуют языку браузера, если вы включите параметр **Согласовать язык браузера**.</span><span class="sxs-lookup"><span data-stu-id="69390-212">In Microsoft Edge version 88, DevTools now matches the browser language if you turn on the **Match browser language** setting.</span></span>  <span data-ttu-id="69390-213">Дополнительные сведения о параметре средств разработчика **Согласовать язык браузера** см. в статье [Изменение языковых параметров средств разработчика][DevtoolsCustomizeLocalization].</span><span class="sxs-lookup"><span data-stu-id="69390-213">For more information about the **Match browser language** DevTools Setting, navigate to [Change DevTools language settings][DevtoolsCustomizeLocalization].</span></span>  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Параметр средств разработчика "Согласовать язык браузера" на японском языке" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   <span data-ttu-id="69390-215">Параметр средств разработчика **Согласовать язык браузера** на японском языке</span><span class="sxs-lookup"><span data-stu-id="69390-215">**Match browser language** DevTools setting in Japanese</span></span>  
:::image-end:::  

## <span data-ttu-id="69390-216">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="69390-216">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="69390-217">Новые средства визуализации угла CSS</span><span class="sxs-lookup"><span data-stu-id="69390-217">New CSS angle visualization tools</span></span>  

<span data-ttu-id="69390-218">В средствах разработчика улучшена поддержка отладки угла CSS.</span><span class="sxs-lookup"><span data-stu-id="69390-218">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="69390-219">Если к элементу HTML на вашей странице применен угол CSS, рядом с углом в средстве **Стили** отображается значок часов.</span><span class="sxs-lookup"><span data-stu-id="69390-219">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="69390-220">Чтобы переключить наложение часов, щелкните значок часов.</span><span class="sxs-lookup"><span data-stu-id="69390-220">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="69390-221">Чтобы изменить угол, выберите любое место на часах или перетащите стрелку.</span><span class="sxs-lookup"><span data-stu-id="69390-221">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="69390-222">Чтобы изменить значение угла, вы также можете использовать мышь и сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="69390-222">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="69390-223">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1126178][CR1126178] и [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="69390-223">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="69390-224">Следующий угол CSS используется в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="69390-224">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Угол CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="69390-226">Угол CSS</span><span class="sxs-lookup"><span data-stu-id="69390-226">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-227">Эмуляция размера квоты хранилища в области "Хранилище"</span><span class="sxs-lookup"><span data-stu-id="69390-227">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="69390-228">Теперь вы можете переопределить размер квоты хранилища области **Хранилище**.</span><span class="sxs-lookup"><span data-stu-id="69390-228">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="69390-229">Эта функция позволяет эмулировать различные устройства и тестировать поведение веб-сайта или приложения в сценариях низкой доступности диска.</span><span class="sxs-lookup"><span data-stu-id="69390-229">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="69390-230">Чтобы эмулировать квоту хранилища, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-230">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-231">Выберите **Приложение** > **Хранилище**.</span><span class="sxs-lookup"><span data-stu-id="69390-231">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="69390-232">Установите флажок **Эмулировать настраиваемую квоту хранилища**.</span><span class="sxs-lookup"><span data-stu-id="69390-232">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="69390-233">Введите допустимое число.</span><span class="sxs-lookup"><span data-stu-id="69390-233">Enter a valid number.</span></span>  
    
<span data-ttu-id="69390-234">Дополнительные сведения о том, как эмулировать мобильные устройства и другие функции в средствах разработчика, см. в статье [Эмуляция мобильных устройств в средствах разработчика Microsoft Edge][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="69390-234">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="69390-235">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [945786][CR945786] и [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="69390-235">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Эмуляция размера квоты хранилища" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="69390-237">Эмуляция размера квоты хранилища</span><span class="sxs-lookup"><span data-stu-id="69390-237">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-238">Отчет об ошибках CORS в средстве "Сеть"</span><span class="sxs-lookup"><span data-stu-id="69390-238">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="69390-239">Попробуйте эту функцию, перейдя к [демонстрации ошибки CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="69390-239">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="69390-240">Откройте средство **Сеть**, обновите страницу и наблюдайте за сбоем сетевого запроса CORS.</span><span class="sxs-lookup"><span data-stu-id="69390-240">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="69390-241">В столбце состояния отображается **ошибка CORS**.</span><span class="sxs-lookup"><span data-stu-id="69390-241">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="69390-242">При наведении курсора на ошибку теперь отображается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="69390-242">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="69390-243">В Microsoft Edge версии 87 и более ранних версиях средства разработчика отображали только общее состояние **(сбой)** для ошибок CORS.</span><span class="sxs-lookup"><span data-stu-id="69390-243">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="69390-244">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="69390-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Ошибки CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="69390-246">Ошибки CORS</span><span class="sxs-lookup"><span data-stu-id="69390-246">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-247">Обновления представления сведений о фрейме</span><span class="sxs-lookup"><span data-stu-id="69390-247">Frame details view updates</span></span>  

#### <span data-ttu-id="69390-248">Сведения об изоляции между источниками в представлении сведений о фрейме</span><span class="sxs-lookup"><span data-stu-id="69390-248">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="69390-249">Теперь состояние изоляции между источниками отображается в разделе **Безопасность и изоляция**.</span><span class="sxs-lookup"><span data-stu-id="69390-249">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="69390-250">В новом разделе **Доступность API** отображается доступность `SharedArrayBuffer`s \(SAB\) и возможность совместного использования буферов с помощью `postMessage()`.</span><span class="sxs-lookup"><span data-stu-id="69390-250">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="69390-251">Если в настоящее время SAB и `postMessage()` доступны, но контекст не изолирован между источниками, отображается предупреждение о прекращении поддержки.</span><span class="sxs-lookup"><span data-stu-id="69390-251">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="69390-252">Дополнительные сведения об изоляции между источниками и о причине ее необходимости для таких функций, как `SharedArrayBuffers`, см. в разделе [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="69390-252">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="69390-253">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="69390-253">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Информация о взаимодействии источников" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="69390-255">Информация о взаимодействии источников</span><span class="sxs-lookup"><span data-stu-id="69390-255">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="69390-256">Сведения о новых рабочих веб-процессах в представлении сведений о фрейме</span><span class="sxs-lookup"><span data-stu-id="69390-256">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="69390-257">Средства разработчика теперь упорядочивают рабочие веб-процессы в соответствующем родительском фрейме.</span><span class="sxs-lookup"><span data-stu-id="69390-257">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="69390-258">Например, если фрейм `someName` создает `worker.js`, `worker.js` отображается в разделе `someName` в списке **Кадры**.</span><span class="sxs-lookup"><span data-stu-id="69390-258">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="69390-259">Чтобы просмотреть сведения о рабочем веб-процессе, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-259">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-260">Откройте средство **Приложение**.</span><span class="sxs-lookup"><span data-stu-id="69390-260">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="69390-261">Разверните фрейм, содержащий рабочие веб-процессы.</span><span class="sxs-lookup"><span data-stu-id="69390-261">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="69390-262">Разверните дерево **Рабочие процессы**.</span><span class="sxs-lookup"><span data-stu-id="69390-262">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="69390-263">Выберите рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="69390-263">Choose a worker.</span></span>  
    
<span data-ttu-id="69390-264">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1122507][CR1122507] и [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="69390-264">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Сведения о рабочих веб-процессах" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="69390-266">Сведения о рабочих веб-процессах</span><span class="sxs-lookup"><span data-stu-id="69390-266">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="69390-267">Отображение сведений об открывающем фрейме для открытых окон</span><span class="sxs-lookup"><span data-stu-id="69390-267">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="69390-268">Средства разработчика теперь упорядочивают открытые [окна][MdnWindowConstructors] в соответствующем родительском [фрейме][MdnWindowFrames].</span><span class="sxs-lookup"><span data-stu-id="69390-268">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="69390-269">Например, если фрейм `top` открывает `Window` для `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, `Window`отображается в разделе `top` в списке **Кадры**.</span><span class="sxs-lookup"><span data-stu-id="69390-269">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="69390-270">Чтобы открыть в средстве **Элементы** фрейм, отвечающий за открытие другого окна, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-270">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-271">Откройте дерево **Кадры**.</span><span class="sxs-lookup"><span data-stu-id="69390-271">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="69390-272">Разверните узел **Открытые окна** и выберите `Window` для родительского фрейма, сведения о котором вам нужны.</span><span class="sxs-lookup"><span data-stu-id="69390-272">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="69390-273">Щелкните ссылку **Открывающий фрейм**.</span><span class="sxs-lookup"><span data-stu-id="69390-273">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="69390-274">Отобразятся сведения о том, какой фрейм вызвал открытие другого объекта `Window`.</span><span class="sxs-lookup"><span data-stu-id="69390-274">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="69390-275">Чтобы отобразить открывающий элемент с средстве **Элементы**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-275">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-276">Откройте дерево **Кадры**.</span><span class="sxs-lookup"><span data-stu-id="69390-276">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="69390-277">Выберите открытое окно, чтобы открыть сведения об элементе `Window`.</span><span class="sxs-lookup"><span data-stu-id="69390-277">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="69390-278">Щелкните ссылку **Открывающий фрейм**.</span><span class="sxs-lookup"><span data-stu-id="69390-278">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="69390-279">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="69390-279">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Сведения об открытом фрейме" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="69390-281">Сведения об открытом фрейме</span><span class="sxs-lookup"><span data-stu-id="69390-281">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-282">Копирование трассировки стека для инициатора сети</span><span class="sxs-lookup"><span data-stu-id="69390-282">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="69390-283">Чтобы скопировать трассировку стека в буфер обмена, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69390-283">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="69390-284">Откройте контекстное меню \(щелкните правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="69390-284">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="69390-285">Выберите **Копировать** > **Копировать трассировку стека**.</span><span class="sxs-lookup"><span data-stu-id="69390-285">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="69390-286">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="69390-286">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Копирование трассировки стека" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="69390-288">Копирование трассировки стека</span><span class="sxs-lookup"><span data-stu-id="69390-288">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-289">Просмотр значения переменной Wasm при наведении указателя мыши</span><span class="sxs-lookup"><span data-stu-id="69390-289">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="69390-290">Используйте эту функцию для просмотра значения переменной WebAssembly \(Wasm\) при приостановке кода.</span><span class="sxs-lookup"><span data-stu-id="69390-290">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="69390-291">Чтобы отобразить текущее значение переменной, наведите курсор на нее.</span><span class="sxs-lookup"><span data-stu-id="69390-291">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="69390-292">Чтобы просмотреть обновления этой функции в режиме реального времени в проекте с открытым исходным кодом Chromium, перейдите к проблемам [1058836][CR1058836] и [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="69390-292">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Просмотр переменной Wasm при наведении указателя мыши" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="69390-294">Просмотр переменной Wasm при наведении указателя мыши</span><span class="sxs-lookup"><span data-stu-id="69390-294">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="69390-295">Согласованные единицы измерения для размеров файлов и памяти</span><span class="sxs-lookup"><span data-stu-id="69390-295">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="69390-296">Средства разработчика теперь согласованно используют `kB` для отображения размеров файлов и памяти.</span><span class="sxs-lookup"><span data-stu-id="69390-296">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="69390-297">Предыдущие средства смешивали использование `kB` и `KiB`.</span><span class="sxs-lookup"><span data-stu-id="69390-297">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="69390-298">или килобайт \(10^3 или 1000 байт\)</span><span class="sxs-lookup"><span data-stu-id="69390-298">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="69390-299">или кибибайт \(2^10 или 1024 байт\)</span><span class="sxs-lookup"><span data-stu-id="69390-299">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="69390-300">Например, средство **Сеть** ранее использовало `kB` в метках, но `KiB` — в вычислениях.</span><span class="sxs-lookup"><span data-stu-id="69390-300">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="69390-301">Ваши отзывы показали, что это несоответствие приводило к путанице.</span><span class="sxs-lookup"><span data-stu-id="69390-301">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="69390-302">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к проблеме [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="69390-302">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="69390-303">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="69390-303">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="69390-304">Если вы используете Windows, Linux или macOS, рассмотрите возможность использования [Microsoft Edge предварительных каналов][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69390-304">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="69390-305">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="69390-305">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="69390-306">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69390-306">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Трехмерное представление | Документация Майкрософт"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Обзор консоли | Документация Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Изменение языковых параметров средств разработчика | Документация Майкрософт"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в средствах разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включение редактора сочетаний клавиш — экспериментальные функции | Документация Майкрософт"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Включение составных слоев в трехмерном представлении — экспериментальные функции | Документация Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем со средством "Проблемы" средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Копирование форматированного отклика JSON в буфер обмена — справочник по анализу сети | Документация Майкрософт"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Просмотр разбивки времени запроса — справочник по анализу сети | Документация Майкрософт"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Использование WebDriver (Chromium) для автоматизации тестирования | Документация Майкрософт"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивное веб-приложение в Windows | Документация Майкрософт"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Настройка сочетания клавиш в параметрах — что нового в средствах разработчика (Microsoft Edge 87) | Документация Майкрософт"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Отзывы webhint в панели "Проблемы" — что нового в средствах разработчика (Microsoft Edge 85) | Документация Майкрософт"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачивание WebDriver | Программа Майкрософт для разработчиков"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Скачивание Microsoft Edge Insider Channels"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "Проблема 174309: средства разработчика: разрешение настройки сочетания клавиш | Ошибки Chromium"  
[CR945786]: https://crbug.com/945786 "Проблема 945786: средства разработчика: разрешение переопределения navigator.storage.estimate() | Ошибки Chromium"  
[CR1029427]: https://crbug.com/1029427 "Проблема 1029427: снижение нагрузки при отправке сообщений протоколом во внешнем интерфейсе | Ошибки Chromium"  
[CR1035309]: https://crbug.com/1035309 "Проблема 1035309: средства разработчика должны согласованно использовать МБ для обозначения мегабайт, а не мебибайт | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Проблема 1051466: поддержка отладки COOP/COEP в средствах разработчика | Ошибки Chromium"  
[CR1058836]: https://crbug.com/1058836 "Проблема 1058836: проблемы пользовательского интерфейса при отладке Wasm | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Проблема 1071432: ☂️ базовый интерфейс разработчика Wasm | Ошибки Chromium"  
[CR1107766]: https://crbug.com/1107766 "Проблема 1107766: отображение сведений о фреймах, созданных командой "window.open()", в дереве фреймов | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Проблема 1122507: получение сведений о рабочем процессе в представлении дерева фреймов | Ошибки Chromium"  
[CR1126178]: https://crbug.com/1126178 "Проблема 1126178: ☂ средства разработчика: компоненты CSS <type> | Ошибки Chromium"  
[CR1130556]: https://crbug.com/1130556 "Проблема 1130556: средства разработчика: откаты тестовых образов (эмуляция) | Ошибки Chromium"  
[CR1132084]: https://crbug.com/1132084 "Проблема 1132084: нет простого способа скопировать полезные данные запроса JSON | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Проблема 1136394: инструменты Flexbox | Ошибки Chromium"  
[CR1138633]: https://crbug.com/1138633 "Проблема 1138633: средства разработчика: компонент CSS <angle> должен отражать внешний вид своего свойства на фоне часов | Ошибки Chromium"  
[CR1139615]: https://crbug.com/1139615 "Проблема 1139615: инициатор сети должен предоставить возможность копирования трассировки стека | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Проблема 1139899: уведомление о доступности ограниченного API в представлении сведений о фрейме | Ошибки Chromium"  
[CR1139945]: https://crbug.com/1139945 "Проблема 1139945: значки для свойств CSS flexbox на панели "Стили" | Ошибки Chromium"  
[CR1141824]: https://crbug.com/1141824 "Проблема 1141824: улучшение отчетов об ошибках CORS в средствах разработчика | Ошибки Chromium"  
[CR1144090]: https://crbug.com/1144090 "Проблема 1144090: добавление графических объектов стиля flex в дерево "Элементы" | Ошибки Chromium"  
[CR1146985]: https://crbug.com/1146985 "Проблема 1146985: очищенный текст по-прежнему виден в текстовом поле раздела "Хранилище" окна "Средства разработчика" | Ошибки Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Ошибки CORS | Сбой"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Общий доступ к ресурсам независимо от источника (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Использование настраиваемых свойств CSS (переменные) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Конструкторы — окно | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Специальные возможности | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Совместимость | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Производительность | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Ошибки | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Безопасность | webhint"  

> [!NOTE]
> <span data-ttu-id="69390-358">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69390-358">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="69390-359">Исходная страница находится [здесь](https://developers.google.com/web/updates/2020/11/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="69390-359">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="69390-361">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69390-361">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
