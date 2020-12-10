---
description: Microsoft Edge для Linux, улучшенные советы по веб – подсказкам в инструменте "проблемы", новые функции отладки рабочих процессов и многое другое.
title: Новые возможности DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205245"
---
# <span data-ttu-id="e7a53-104">Новые возможности DevTools (Microsoft Edge 88)</span><span class="sxs-lookup"><span data-stu-id="e7a53-104">What's New in DevTools (Microsoft Edge 88)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="e7a53-105">Драйвер Microsoft EDGE и Microsoft EDGE, теперь доступные в Linux</span><span class="sxs-lookup"><span data-stu-id="e7a53-105">Microsoft Edge and Microsoft Edge Driver now available on Linux</span></span>  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

<span data-ttu-id="e7a53-106">Теперь приложение Microsoft Edge dev поддерживается для Debian, Fedora и openSUSE.</span><span class="sxs-lookup"><span data-stu-id="e7a53-106">Microsoft Edge Dev is now supported on Ubuntu, Debian, Fedora, and openSUSE distributions.</span></span>  <span data-ttu-id="e7a53-107">Скачайте и установите Microsoft Edge dev `.deb` или `.rpm` пакет прямо из [сайта предварительной оценки Microsoft Edge][MicrosoftinsiderDownloadPlatformLinux] или воспользуйтесь стандартными средствами управления пакетами для дистрибутива Linux.</span><span class="sxs-lookup"><span data-stu-id="e7a53-107">Download and install the Microsoft Edge Dev `.deb` or `.rpm` package directly from the [Microsoft Edge Insider site][MicrosoftinsiderDownloadPlatformLinux] or use the standard package management tools of your Linux distribution.</span></span>  

<span data-ttu-id="e7a53-108">Если вы используете среду Linux в решениях непрерывной интеграции и поставки \ (CI/CD \), драйвер Microsoft EDGE также доступен в ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="e7a53-108">If you are using a Linux environment in your continuous integration and delivery \(CI/CD\) solutions, Microsoft Edge Driver is also available on Linux.</span></span>  <span data-ttu-id="e7a53-109">Чтобы приступить к автоматизации разработки Microsoft Edge с помощью драйвера Microsoft EDGE, перейдите на [страницу загрузки драйверов Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="e7a53-109">To get started automating Microsoft Edge Dev with Microsoft Edge Driver, navigate to [Microsoft Edge Driver Downloads page][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="e7a53-110">Чтобы получить помощь по автоматизации разработки Microsoft Edge вместе с драйвером Microsoft EDGE, перейдите в раздел [Использование веб-накопителя (Chromium) для автоматизации тестов][WebDriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="e7a53-110">For help with automating Microsoft Edge Dev along with Microsoft Edge Driver, navigate to [Use WebDriver (Chromium) for test automation][WebDriverChromiumMain].</span></span>  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools в Microsoft Edge для Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   <span data-ttu-id="e7a53-112">DevTools в Microsoft Edge для Linux</span><span class="sxs-lookup"><span data-stu-id="e7a53-112">DevTools in Microsoft Edge on Linux</span></span>  
:::image-end:::  

## <span data-ttu-id="e7a53-113">Улучшенная подсказка и советы по платформе в инструменте "проблемы"</span><span class="sxs-lookup"><span data-stu-id="e7a53-113">Improved webhint and platform tips in the Issues tool</span></span>  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

<span data-ttu-id="e7a53-114">Средство веб- [подсказки][WebhintMain]с открытым кодом обеспечивает отзыв в реальном времени для веб-сайтов и локальных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="e7a53-114">An open-source tool, [webhint][WebhintMain], provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="e7a53-115">Начиная с [Microsoft Edge версии 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], изучите Отзывы по веб – подсказкам в инструменте " [вопросы][DevtoolsIssuesIndex] ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-115">Starting with [Microsoft Edge version 85][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], review webhint feedback in the [Issues][DevtoolsIssuesIndex] tool.</span></span>  <span data-ttu-id="e7a53-116">Проблемы, возникающие в инструменте " **проблемы** ", теперь проще проанализировать с добавлением следующих категорий.</span><span class="sxs-lookup"><span data-stu-id="e7a53-116">Issues that appear in the **Issues** tool are now easier to review with the addition of the following categories.</span></span>  

*   [<span data-ttu-id="e7a53-117">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="e7a53-117">Accessibility</span></span>][WebhintUserGuideHintsAccessibility]  
*   [<span data-ttu-id="e7a53-118">Совместимость</span><span class="sxs-lookup"><span data-stu-id="e7a53-118">Compatibility</span></span>][WebhintUserGuideHintsCompatibility]  
*   [<span data-ttu-id="e7a53-119">Производительность</span><span class="sxs-lookup"><span data-stu-id="e7a53-119">Performance</span></span>][WebhintUserGuideHintsPerformance]  
*   [<span data-ttu-id="e7a53-120">Ошибок</span><span class="sxs-lookup"><span data-stu-id="e7a53-120">Pitfalls</span></span>][WebhintUserGuideHintsPitfalls]  
*   [<span data-ttu-id="e7a53-121">PWA</span><span class="sxs-lookup"><span data-stu-id="e7a53-121">PWA</span></span>][WebhintUserGuideHintsPwa]  
*   [<span data-ttu-id="e7a53-122">Безопасность</span><span class="sxs-lookup"><span data-stu-id="e7a53-122">Security</span></span>][WebhintUserGuideHintsSecurity]  
    
<span data-ttu-id="e7a53-123">Теперь вы можете отфильтровать сторонние проблемы с помощью нового флажка.</span><span class="sxs-lookup"><span data-stu-id="e7a53-123">You are now able to filter out third-party issues using a new checkbox.</span></span>  <span data-ttu-id="e7a53-124">Функция фильтрации помогает скрыть проблемы, связанные с кодом из сторонних библиотек или из других источников.</span><span class="sxs-lookup"><span data-stu-id="e7a53-124">The filter functionality helps you hide issues related to code from third-party libraries or other sources.</span></span>  

<span data-ttu-id="e7a53-125">Для ознакомления с вопросами, обнаруженными с помощью этой [подсказки][WebhintMain], в инструменте " **проблемы** " отображаются следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="e7a53-125">To help you review issues revealed by [webhint][WebhintMain], the **Issues** tool now displays the following information.</span></span>  

*   <span data-ttu-id="e7a53-126">Улучшенные фрагменты кода.</span><span class="sxs-lookup"><span data-stu-id="e7a53-126">Improved code snippets.</span></span>  
*   <span data-ttu-id="e7a53-127">Ссылки на другие подходящие панели.</span><span class="sxs-lookup"><span data-stu-id="e7a53-127">Links to other relevant panels.</span></span>  
*   <span data-ttu-id="e7a53-128">Ссылки на документы, которые помогут вам устранить проблемы на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="e7a53-128">Links to documentation to help you fix problems in your website.</span></span>  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Инструмент "проблемы"" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   <span data-ttu-id="e7a53-130">Инструмент " **проблемы** "</span><span class="sxs-lookup"><span data-stu-id="e7a53-130">**Issues** tool</span></span>  
:::image-end:::  

## <span data-ttu-id="e7a53-131">Составные слои теперь отображаются в трехмерном представлении</span><span class="sxs-lookup"><span data-stu-id="e7a53-131">Composited Layers are now in 3D View</span></span>  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="e7a53-132">Теперь вы можете визуализировать содержимое **слоев** вместе со значениями z-индекса и объектной модели документов \ (DOM \).</span><span class="sxs-lookup"><span data-stu-id="e7a53-132">You may now visualize **Layers** content alongside z-index values and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="e7a53-133">Эта функция позволяет выполнять отладку, не переключаясь между инструментами [3D View][Devtools3dViewIndex] и **слоев** как можно чаще.</span><span class="sxs-lookup"><span data-stu-id="e7a53-133">This feature helps you debug without switching between the [3D view][Devtools3dViewIndex] and **Layers** tools as often.</span></span>  <span data-ttu-id="e7a53-134">Для всесторонней визуальной отладки [теперь можно объединять трехмерное представление и составные слои][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span><span class="sxs-lookup"><span data-stu-id="e7a53-134">For a comprehensive visual debugging experience, the [3D View and Composited Layers are now combined][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].</span></span>  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Область «составные слои»" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   <span data-ttu-id="e7a53-136">Область « **Составные слои** »</span><span class="sxs-lookup"><span data-stu-id="e7a53-136">**Composited Layers** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="e7a53-137">Определение переменных CSS на панели «Стили»</span><span class="sxs-lookup"><span data-stu-id="e7a53-137">CSS variable definitions in Styles pane</span></span>  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

<span data-ttu-id="e7a53-138">В области **стили** [CSS переменные][MdnUsingCssCustomProperties] теперь прямо связываются с каждым определением.</span><span class="sxs-lookup"><span data-stu-id="e7a53-138">In the **Styles** pane, [CSS variables][MdnUsingCssCustomProperties] now link directly to each definition.</span></span>  <span data-ttu-id="e7a53-139">Выберите переменную, чтобы легко просмотреть или изменить определение переменной CSS.</span><span class="sxs-lookup"><span data-stu-id="e7a53-139">Choose the variable to easily view or change the CSS variable definition.</span></span>  <span data-ttu-id="e7a53-140">В примере DevTools отображает атрибуты CSS для `body` элемента.</span><span class="sxs-lookup"><span data-stu-id="e7a53-140">In the example, DevTools displays the CSS attributes for the `body` element.</span></span>  <span data-ttu-id="e7a53-141">Чтобы отобразить определение переменной `--theme-body-background` CSS, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-141">To display the variable definition for the `--theme-body-background` CSS variable, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-142">В области **стили** выберите `var(--theme-body-background)` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-142">In the **Styles** pane, choose `var(--theme-body-background)`.</span></span>  
1.  <span data-ttu-id="e7a53-143">В области " **стили** " теперь отображается определение `--theme-body-background` переменной CSS.</span><span class="sxs-lookup"><span data-stu-id="e7a53-143">The **Styles** pane now displays the definition of the `--theme-body-background` CSS variable.</span></span>  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Переменная CSS, связанная с этим стилем" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         <span data-ttu-id="e7a53-145">Переменная CSS, связанная с этим стилем</span><span class="sxs-lookup"><span data-stu-id="e7a53-145">CSS variable linked to the style</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Переменная CSS, связанная с целевым объектом стиля" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         <span data-ttu-id="e7a53-147">Переменная CSS, связанная с целевым объектом стиля</span><span class="sxs-lookup"><span data-stu-id="e7a53-147">CSS variable linked to style target</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e7a53-148">Улучшения в отладке рабочих процессов служб</span><span class="sxs-lookup"><span data-stu-id="e7a53-148">Service worker debugging improvements</span></span>  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

<span data-ttu-id="e7a53-149">Ниже перечислены новые возможности средств " [сеть](#network-tool)", " [приложение](#application-tool)" и " [источники](#sources-tool) ", которые помогут вам создать [PWA][ProgressiveWebAppsChromiumIndex].</span><span class="sxs-lookup"><span data-stu-id="e7a53-149">The following new features in the [Network](#network-tool), [Application](#application-tool), and [Sources](#sources-tool) tools help you build your [PWA][ProgressiveWebAppsChromiumIndex].</span></span>  <span data-ttu-id="e7a53-150">Если у вас возникли проблемы при отладке вашего сотрудника службы, используйте следующие функции.</span><span class="sxs-lookup"><span data-stu-id="e7a53-150">Use the following features when you have difficulty debugging your service worker.</span></span>  

<span data-ttu-id="e7a53-151">В маршруте запроса отображаются `startup` события и данные, `fetch` основанные на запросах в сети, которые выполняются сотрудниками службы.</span><span class="sxs-lookup"><span data-stu-id="e7a53-151">Request routing displays the `startup` and `fetch` events based on the network requests that run through service workers.</span></span>  <span data-ttu-id="e7a53-152">Доступ к временной шкале осуществляется с помощью средства " **приложение** " или " **сеть** ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-152">The timelines are accessed from either the **Application** or **Network** tool.</span></span>  <span data-ttu-id="e7a53-153">Временные шкалы помогают вам при возникновении проблем с сотрудниками служб, которые хотят проверить, не возникло ли что-то с `startup` `fetch` событием.</span><span class="sxs-lookup"><span data-stu-id="e7a53-153">The timelines help when you are having trouble with service workers and want to see if something is wrong with the `startup` or `fetch` event.</span></span>  

### <span data-ttu-id="e7a53-154">Инструмент "приложение"</span><span class="sxs-lookup"><span data-stu-id="e7a53-154">Application tool</span></span>  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

<span data-ttu-id="e7a53-155">Просмотреть все сведения о маршруте запроса на обслуживание с помощью новой ссылки " **сетевые запросы** ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-155">View all service worker request routing information with the new **Network requests** link.</span></span>  <span data-ttu-id="e7a53-156">Чтобы отобразить дополнительный контекст при отладке рабочего процесса службы, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-156">To display additional context when debugging the service worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-157">Перейдите к \*\*\*\*  >  **сотрудникам службы**приложений.</span><span class="sxs-lookup"><span data-stu-id="e7a53-157">Navigate to **Application** > **Service Workers**.</span></span>  
1.  <span data-ttu-id="e7a53-158">Выберите **сетевые запросы**.</span><span class="sxs-lookup"><span data-stu-id="e7a53-158">Choose **Network requests**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Инструмент "открыть сеть" из области "работники службы"" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       <span data-ttu-id="e7a53-160">Инструмент "открыть **сеть** " из области " **работники службы** "</span><span class="sxs-lookup"><span data-stu-id="e7a53-160">Open **Network** tool from the **Service Workers** pane</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="e7a53-161">В **ящике** откроется средство " **сеть** ", в котором выводятся все сетевые запросы, связанные с сотрудниками служб.</span><span class="sxs-lookup"><span data-stu-id="e7a53-161">The **Network** tool opens in the **drawer** and displays all service worker-related network requests.</span></span>  <span data-ttu-id="e7a53-162">Сетевые запросы фильтруются с использованием `is:service-worker-intercepted` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-162">The network requests are filtered using `is:service-worker-intercepted`.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Инструмент "сеть" в ящике" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       <span data-ttu-id="e7a53-164">Инструмент " **сеть** " в **ящике**</span><span class="sxs-lookup"><span data-stu-id="e7a53-164">**Network** tool in **drawer**</span></span>  
    :::image-end:::
    
1. <span data-ttu-id="e7a53-165">Чтобы вернуть инструмент **Network (сеть** ) на верхнюю панель, закройте **денежный ящик**.</span><span class="sxs-lookup"><span data-stu-id="e7a53-165">To return the **Network** tool to the top panel, close the **drawer**.</span></span>  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Закройте денежный ящик, чтобы вернуть сетевое средство" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       <span data-ttu-id="e7a53-167">Закройте **денежный ящик** , чтобы вернуть **Сетевое** средство</span><span class="sxs-lookup"><span data-stu-id="e7a53-167">Close the **drawer** to return **Network** tool</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e7a53-168">Инструмент "сеть"</span><span class="sxs-lookup"><span data-stu-id="e7a53-168">Network tool</span></span>  

<span data-ttu-id="e7a53-169">Сетевые запросы на отладку, которые выполняются сотрудниками службы;</span><span class="sxs-lookup"><span data-stu-id="e7a53-169">Debug network requests that run through service workers.</span></span>  <span data-ttu-id="e7a53-170">Кроме того, вы можете открывать сетевые запросы из средства **приложения** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-170">You may also open network requests from the **Application** tool.</span></span>  <span data-ttu-id="e7a53-171">Для каждого запроса DevTools отобразить следующие сведения в области [временных интервалов][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .</span><span class="sxs-lookup"><span data-stu-id="e7a53-171">For each request, DevTools display the following information in the [Timing][DevtoolsNetworkReferenceViewTimingBreakdownRequest] pane.</span></span>  

*   <span data-ttu-id="e7a53-172">Начало запроса и продолжительность начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="e7a53-172">The start of a request and duration of the bootstrap.</span></span>  
*   <span data-ttu-id="e7a53-173">Изменения регистрации рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="e7a53-173">Changes to service worker registration.</span></span>  
*   <span data-ttu-id="e7a53-174">Среда выполнения `fetch` обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="e7a53-174">The runtime of a `fetch` event handler.</span></span>  
*   <span data-ttu-id="e7a53-175">Среда выполнения всех событий, возникающих `fetch` при загрузке клиента.</span><span class="sxs-lookup"><span data-stu-id="e7a53-175">The runtime of all `fetch` events for loading a client.</span></span>  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Область временных интервалов" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   <span data-ttu-id="e7a53-177">Область **временных интервалов**</span><span class="sxs-lookup"><span data-stu-id="e7a53-177">**Timing** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-178">Инструмент «источники»</span><span class="sxs-lookup"><span data-stu-id="e7a53-178">Sources tool</span></span>  

<span data-ttu-id="e7a53-179">В предыдущих версиях Microsoft Edge уровень глубины в стеке вызовов ограничен кодом JavaScript в сервисном рабочем процессе.</span><span class="sxs-lookup"><span data-stu-id="e7a53-179">In previous versions of Microsoft Edge, the level of depth in the call stack was limited to the JavaScript code in your service worker.</span></span>  <span data-ttu-id="e7a53-180">В Microsoft Edge 88 в стеке вызовов теперь отображаются инициаторы запросов, которые выполняются в рамках вашего сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="e7a53-180">In Microsoft Edge 88, the call stack now displays the initiator of requests that run through your service worker.</span></span>  

<span data-ttu-id="e7a53-181">Чтобы найти инициатора запроса, используйте стек вызовов вашего кода JavaScript в сервисном рабочем процессе.</span><span class="sxs-lookup"><span data-stu-id="e7a53-181">To locate the initiator of the request, use the call stack of your JavaScript code in the service worker.</span></span>  <span data-ttu-id="e7a53-182">Стек вызовов на приведенных ниже рисунках начинается с кода JavaScript в рабочем процессе и отображает ссылку на первоначальное приглашение на веб-страницу `(index):157` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-182">The call stack in the following figures starts with the JavaScript code in your service worker and displays a reference to the original webpage request as `(index):157`.</span></span>  <span data-ttu-id="e7a53-183">На втором рисунке показано, как выбрать ссылку и открыть инициатор, который сделал запрос.</span><span class="sxs-lookup"><span data-stu-id="e7a53-183">In the second figure, the reference is chosen and opened the initiator that made the request.</span></span>  <span data-ttu-id="e7a53-184">Инициатор на втором рисунке — это веб-страница.</span><span class="sxs-lookup"><span data-stu-id="e7a53-184">The initiator in the second figure is the webpage.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="Создатель запроса, который выделит service-worker.js файл и стек вызовов" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         <span data-ttu-id="e7a53-186">`service-worker.js`Инициатор запроса, выделяя файл и стек вызовов</span><span class="sxs-lookup"><span data-stu-id="e7a53-186">The `service-worker.js` file and call stack highlighting request originator</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="Веб-страница указателя является инициатором запроса" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         <span data-ttu-id="e7a53-188">`(index)`Веб-страница является инициатором запроса</span><span class="sxs-lookup"><span data-stu-id="e7a53-188">The `(index)` webpage is the request initiator</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e7a53-189">Копирование значения свойства сетевого запроса</span><span class="sxs-lookup"><span data-stu-id="e7a53-189">Copy property value of a network request</span></span>  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

<span data-ttu-id="e7a53-190">В средстве **Network (сеть** ) скопируйте значение свойства сетевого запроса с помощью нового параметра **Копировать значение** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-190">In the **Network** tool, copy the property value of a network request using the new **Copy value** option.</span></span>  <span data-ttu-id="e7a53-191">Значение свойства копируется как декодированное значение JSON.</span><span class="sxs-lookup"><span data-stu-id="e7a53-191">The property value is copied as a decoded JSON value.</span></span>  <span data-ttu-id="e7a53-192">В предыдущих версиях Microsoft Edge пришло время скопировать значение с помощью одного из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="e7a53-192">In previous versions of Microsoft Edge, you had to copy a value using one of the following actions.</span></span>  

*   <span data-ttu-id="e7a53-193">Выделит весь текст и скопируйте его.</span><span class="sxs-lookup"><span data-stu-id="e7a53-193">Highlight the entire text and copy it.</span></span>  
*   <span data-ttu-id="e7a53-194">Сохраните значение как глобальную переменную, если это применимо, и скопируйте ее из [консоли][DevtoolsConsoleIndex]DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7a53-194">Store the value as global variable, as applicable, and copy it from the DevTools [Console][DevtoolsConsoleIndex].</span></span>  
    
<span data-ttu-id="e7a53-195">Чтобы скопировать значение свойства в буфер обмена, перейдите в [буфер обмена, чтобы скопировать отформатированный JSON ответа][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span><span class="sxs-lookup"><span data-stu-id="e7a53-195">To copy the property value to your clipboard, navigate to [Copy formatted response JSON to the clipboard][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].</span></span>  <span data-ttu-id="e7a53-196">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1132084][CR1132084].</span><span class="sxs-lookup"><span data-stu-id="e7a53-196">To review the history of this feature in the Chromium open-source project, navigate to Issue [1132084][CR1132084].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Копирование значения свойства в DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         <span data-ttu-id="e7a53-198">Копирование значения свойства в DevTools</span><span class="sxs-lookup"><span data-stu-id="e7a53-198">Copy property value in DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Вставка значения свойства в код Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         <span data-ttu-id="e7a53-200">Вставка значения свойства в код Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e7a53-200">Paste property value in Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="e7a53-201">Настройка сочетаний клавиш с несколькими нажатиями клавиш</span><span class="sxs-lookup"><span data-stu-id="e7a53-201">Customize multi-press keyboard shortcuts</span></span>  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

<span data-ttu-id="e7a53-202">[Поскольку Microsoft Edge версии 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], вы можете настроить сочетания клавиш для любых действий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7a53-202">[Since Microsoft Edge version 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], you may customize keyboard shortcuts for any action in DevTools.</span></span>  <span data-ttu-id="e7a53-203">В Microsoft Edge версии 88 вы можете создать несколько сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="e7a53-203">In Microsoft Edge version 88, you may now create multi-press keyboard shortcuts.</span></span>  <span data-ttu-id="e7a53-204">Чтобы задать сочетание клавиш для действия в DevTools, перейдите в раздел [][DevtoolsCustomizeIndexSettings]  >  **эксперименты** с параметрами и установите флажок **включить редактор сочетаний клавиш**.</span><span class="sxs-lookup"><span data-stu-id="e7a53-204">To set a shortcut for an action in the DevTools, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments**  and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="e7a53-205">Дополнительные сведения о настройке и редактировании сочетаний клавиш можно найти в статье [включить режим экспериментального редактора сочетаних][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]клавиш.</span><span class="sxs-lookup"><span data-stu-id="e7a53-205">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="e7a53-206">Например, красная подсветка отображает сочетание клавиш для нескольких нажатий, настроенное для действия " **начать запись событий** ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-206">For example, the red highlight displays a multi-press keyboard shortcut customized for the **Start recording events** action.</span></span>  <span data-ttu-id="e7a53-207">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к [вопросу #174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="e7a53-207">To review real-time updates on this feature in the Chromium open-source project, navigate to [Issue #174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Сочетания клавиш для аккордов" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   <span data-ttu-id="e7a53-209">Сочетания клавиш для нескольких клавиш</span><span class="sxs-lookup"><span data-stu-id="e7a53-209">Multi-press keyboard shortcuts</span></span>  
:::image-end:::  

## <span data-ttu-id="e7a53-210">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="e7a53-210">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="e7a53-211">Новые инструменты визуализации для угла CSS</span><span class="sxs-lookup"><span data-stu-id="e7a53-211">New CSS angle visualization tools</span></span>  

<span data-ttu-id="e7a53-212">DevTools теперь имеет улучшенную поддержку отладки для углов CSS.</span><span class="sxs-lookup"><span data-stu-id="e7a53-212">DevTools now have better support for CSS angle debugging.</span></span>  <span data-ttu-id="e7a53-213">Если к элементу HTML на странице применен угол CSS, рядом с углом в инструменте " **стили** " отображается значок "Часы".</span><span class="sxs-lookup"><span data-stu-id="e7a53-213">When an HTML element on your page has CSS angle applied to it, a clock icon is displayed next to the angle in the **Styles** tool.</span></span>  <span data-ttu-id="e7a53-214">Чтобы включить или выключить наложение часов, щелкните значок часы.</span><span class="sxs-lookup"><span data-stu-id="e7a53-214">To toggle the clock overlay, choose the clock icon.</span></span>  <span data-ttu-id="e7a53-215">Чтобы изменить угол, выберите любое место в часах или перетащите поле стрелки.</span><span class="sxs-lookup"><span data-stu-id="e7a53-215">To change the angle, choose anywhere in the clock or drag the needle.</span></span>  <span data-ttu-id="e7a53-216">Для изменения значения угла вы также можете использовать клавиши мыши и сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="e7a53-216">To change the angle value, you may also use mouse and keyboard shortcuts.</span></span>  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  <span data-ttu-id="e7a53-217">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1126178][CR1126178] и [1138633][CR1138633].</span><span class="sxs-lookup"><span data-stu-id="e7a53-217">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1126178][CR1126178] and [1138633][CR1138633].</span></span>  

<!--todo:  add link when css angle clock section exists.  -->  

<span data-ttu-id="e7a53-218">Для этого примера используется следующий угол CSS.</span><span class="sxs-lookup"><span data-stu-id="e7a53-218">The following CSS angle is used for the example.</span></span>  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Угол CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   <span data-ttu-id="e7a53-220">Угол CSS</span><span class="sxs-lookup"><span data-stu-id="e7a53-220">CSS angle</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-221">Имитация размера квоты хранилища в области "хранилище"</span><span class="sxs-lookup"><span data-stu-id="e7a53-221">Simulate storage quota size in the Storage pane</span></span>  

<span data-ttu-id="e7a53-222">Теперь вы можете переопределить размер квоты хранилища в области **хранения** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-222">You may now override storage quota size in the **Storage** pane.</span></span>  <span data-ttu-id="e7a53-223">Эта функция позволяет моделировать различные устройства и тестировать работу вашего веб-сайта или приложения в сценариях недостаточной доступности диска.</span><span class="sxs-lookup"><span data-stu-id="e7a53-223">This feature allows you to simulate different devices and test the behavior of your website or app in low disk availability scenarios.</span></span>  <span data-ttu-id="e7a53-224">Чтобы смоделировать квоту хранилища, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-224">To simulate the storage quota, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-225">Перейдите в \*\*\*\* раздел  >  **хранилище**приложений.</span><span class="sxs-lookup"><span data-stu-id="e7a53-225">Navigate to **Application** > **Storage**.</span></span>  
1.  <span data-ttu-id="e7a53-226">Включите флажок **Эмуляция настраиваемой квоты хранилища** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-226">Turn on the **Simulate custom storage quota** checkbox.</span></span>  
1.  <span data-ttu-id="e7a53-227">Введите допустимое число.</span><span class="sxs-lookup"><span data-stu-id="e7a53-227">Enter a valid number.</span></span>  
    
<span data-ttu-id="e7a53-228">Дополнительные сведения о том, как эмулировать мобильные устройства и другие функции в DevTools, можно найти в [разделе Эмуляция мобильных устройств в Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="e7a53-228">For more information about how to emulate mobile devices and other features in the DevTools, navigate to [Emulate mobile devices in Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].</span></span>  <span data-ttu-id="e7a53-229">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [945786][CR945786] и [1146985][CR1146985].</span><span class="sxs-lookup"><span data-stu-id="e7a53-229">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [945786][CR945786] and [1146985][CR1146985].</span></span>  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Имитация размера квоты хранилища" lightbox="../../media/2020/11/storage-quota.msft.png":::
   <span data-ttu-id="e7a53-231">Имитация размера квоты хранилища</span><span class="sxs-lookup"><span data-stu-id="e7a53-231">Simulate storage quota size</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-232">Ошибки при составлении отчета CORS в инструменте "сеть"</span><span class="sxs-lookup"><span data-stu-id="e7a53-232">Report CORS errors in the Network tool</span></span>  

<span data-ttu-id="e7a53-233">Ознакомьтесь с этой функцией, перейдя в [демонстрацию ошибки CORS][GlitchCorsErrors].</span><span class="sxs-lookup"><span data-stu-id="e7a53-233">Try out this feature by navigating to [CORS error demo][GlitchCorsErrors].</span></span>  <span data-ttu-id="e7a53-234">Откройте средство **Network (сеть** ), обновите страницу и просмотрите ошибочный запрос CORS Network.</span><span class="sxs-lookup"><span data-stu-id="e7a53-234">Open the **Network** tool, refresh the page, and observe the failed CORS network request.</span></span>  <span data-ttu-id="e7a53-235">В столбце status отображается **Ошибка CORS**.</span><span class="sxs-lookup"><span data-stu-id="e7a53-235">The status column displays the **CORS error**.</span></span>  <span data-ttu-id="e7a53-236">При наведении указателя мыши на ошибку появляется подсказка с кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="e7a53-236">When you hover on the error, the tooltip now displays the error code.</span></span>  <span data-ttu-id="e7a53-237">В Microsoft Edge версии 87 и более ранних версий DevTools только что выводит общее состояние ошибки CORS **(сбой)** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-237">In Microsoft Edge version 87 and earlier, DevTools only displayed generic **(failed)** status for CORS errors.</span></span>  <span data-ttu-id="e7a53-238">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите к вопросу [1141824][CR1141824].</span><span class="sxs-lookup"><span data-stu-id="e7a53-238">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [1141824][CR1141824].</span></span>  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Ошибки CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   <span data-ttu-id="e7a53-240">Ошибки CORS</span><span class="sxs-lookup"><span data-stu-id="e7a53-240">CORS errors</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-241">Обновления представления "сведения о кадрах"</span><span class="sxs-lookup"><span data-stu-id="e7a53-241">Frame details view updates</span></span>  

#### <span data-ttu-id="e7a53-242">Сведения о межисточниковой изоляции в представлении сведений о кадре</span><span class="sxs-lookup"><span data-stu-id="e7a53-242">Cross-origin isolation information in the Frame details view</span></span>  

<span data-ttu-id="e7a53-243">Изолированное состояние "перекрестный источник" теперь отображается в разделе **изоляция & безопасности** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-243">The cross-origin isolated status is now displayed under the **Security & Isolation** section.</span></span>  <span data-ttu-id="e7a53-244">В разделе новый **доступ к API** отображаются сведения о доступности `SharedArrayBuffer` s \ (SAB \) и о том, можно ли совместно использовать буферы `postMessage()` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-244">The new **API availability** section displays the availability of `SharedArrayBuffer`s \(SAB\) and whether the buffers may be shared using `postMessage()`.</span></span>  <span data-ttu-id="e7a53-245">Предупреждение об устаревании отображается, если свойство SAB и в `postMessage()` настоящее время доступно, но контекст не является зависимым от других источников.</span><span class="sxs-lookup"><span data-stu-id="e7a53-245">A deprecation warning displays if the SAB and `postMessage()` is currently available, but the context is not cross-origin isolated.</span></span>  <span data-ttu-id="e7a53-246">Чтобы получить дополнительные сведения о межисточниковой изоляции и о том, что необходимо для таких функций `SharedArrayBuffers` , перейдите на сайт [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span><span class="sxs-lookup"><span data-stu-id="e7a53-246">For more information about cross-origin isolation and why it is required for features like `SharedArrayBuffers`, navigate to [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].</span></span>  <span data-ttu-id="e7a53-247">Чтобы просмотреть обновления в режиме реального времени в проекте Open-Source Chromium, перейдите к вопросу [1139899][CR1139899].</span><span class="sxs-lookup"><span data-stu-id="e7a53-247">To review real-time updates of this feature in the Chromium open-source project, navigate to Issue [1139899][CR1139899].</span></span>  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Сведения о разных источниках" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   <span data-ttu-id="e7a53-249">Сведения о разных источниках</span><span class="sxs-lookup"><span data-stu-id="e7a53-249">Cross-origin information</span></span>  
:::image-end:::  

#### <span data-ttu-id="e7a53-250">Новые сведения о веб-сотрудниках в представлении "сведения о кадре"</span><span class="sxs-lookup"><span data-stu-id="e7a53-250">New Web Workers information in the Frame details view</span></span>  

<span data-ttu-id="e7a53-251">Теперь DevTools организует веб-рабочие процессы в соответствующем родительском фрейме.</span><span class="sxs-lookup"><span data-stu-id="e7a53-251">DevTools now organizes web workers under the relevant parent frame.</span></span>  <span data-ttu-id="e7a53-252">Например, если `someName` рамка создана `worker.js` , в `worker.js` `someName` списке **кадры** появится надпись.</span><span class="sxs-lookup"><span data-stu-id="e7a53-252">For example, if the `someName` frame creates `worker.js`, then `worker.js` appears under `someName` in the **Frames** list.</span></span>  <span data-ttu-id="e7a53-253">Чтобы просмотреть сведения о веб-сотруднике, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-253">To view the details of the web worker, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-254">Откройте средство " **приложение** ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-254">Open **Application** tool.</span></span>  
1.  <span data-ttu-id="e7a53-255">Разверните рамку, содержащую веб-сотрудников.</span><span class="sxs-lookup"><span data-stu-id="e7a53-255">Expand a frame that contains web workers.</span></span>  
1.  <span data-ttu-id="e7a53-256">Разверните дерево " **сотрудники** ".</span><span class="sxs-lookup"><span data-stu-id="e7a53-256">Expand the **Workers** tree.</span></span>  
1.  <span data-ttu-id="e7a53-257">Выберите работника.</span><span class="sxs-lookup"><span data-stu-id="e7a53-257">Choose a worker.</span></span>  
    
<span data-ttu-id="e7a53-258">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1122507][CR1122507] и [1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="e7a53-258">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1122507][CR1122507] and [1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Сведения о веб-работниках" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   <span data-ttu-id="e7a53-260">Сведения о веб-работниках</span><span class="sxs-lookup"><span data-stu-id="e7a53-260">Web workers information</span></span>  
:::image-end:::  

#### <span data-ttu-id="e7a53-261">Отображение сведений о кадре opener для открытых окон</span><span class="sxs-lookup"><span data-stu-id="e7a53-261">Display opener frame details for opened windows</span></span>  

<span data-ttu-id="e7a53-262">DevTools теперь упорядочивает открытые [окна][MdnWindowConstructors] под соответствующим родительским [кадром][MdnWindowFrames].</span><span class="sxs-lookup"><span data-stu-id="e7a53-262">DevTools now organizes opened [Windows][MdnWindowConstructors] under the relevant parent [frame][MdnWindowFrames].</span></span>  <span data-ttu-id="e7a53-263">Например, если при `top` открытии кадра в поле `Window` "Кому" появится надпись `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` `Window` `top` в списке **рамок** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-263">For example, if the `top` frame opens a `Window` to `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, then the `Window` appears under `top` in the **Frames** list.</span></span>  

<span data-ttu-id="e7a53-264">Чтобы отобразить кадр, ответственный за открытие другого окна в инструменте " **элементы** ", выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-264">To reveal the frame responsible for opening another Window in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-265">Откройте дерево **рамок** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-265">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="e7a53-266">Разверните **открытые окна** и выберите `Window` родительский фрейм, который вы хотите узнать.</span><span class="sxs-lookup"><span data-stu-id="e7a53-266">Expand **Opened Windows** and choose the `Window` for the parent frame you want to know.</span></span>  
1.  <span data-ttu-id="e7a53-267">Щелкните ссылку **рамка opener** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-267">Choose the **Opener Frame** link.</span></span>  

<span data-ttu-id="e7a53-268">Отображаются сведения о том, какой кадр вызвал открытие другого `Window` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-268">The details are displayed about which frame caused the opening of another `Window`.</span></span>  <span data-ttu-id="e7a53-269">Чтобы открыть opener в инструменте **элементы** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-269">To reveal the opener in the **Elements** tool, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-270">Откройте дерево **рамок** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-270">Open the **Frames** tree.</span></span>  
1.  <span data-ttu-id="e7a53-271">Выберите открытое окно, чтобы открыть `Window` подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="e7a53-271">Choose an opened window to open the `Window` details.</span></span>  
1.  <span data-ttu-id="e7a53-272">Щелкните ссылку **рамка opener** .</span><span class="sxs-lookup"><span data-stu-id="e7a53-272">Choose the **Opener Frame** link.</span></span>  
    
<span data-ttu-id="e7a53-273">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1107766][CR1107766].</span><span class="sxs-lookup"><span data-stu-id="e7a53-273">To review the history of this feature in the Chromium open-source project, navigate to Issue [1107766][CR1107766].</span></span>  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Сведения об открытых кадрах" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   <span data-ttu-id="e7a53-275">Сведения об открытых кадрах</span><span class="sxs-lookup"><span data-stu-id="e7a53-275">Opened frame details</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-276">Копирование StackTrace для инициатора сети</span><span class="sxs-lookup"><span data-stu-id="e7a53-276">Copy stacktrace for network initiator</span></span>  

<span data-ttu-id="e7a53-277">Чтобы скопировать StackTrace в буфер обмена, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e7a53-277">To copy the stacktrace to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="e7a53-278">Откройте контекстное меню, щелкнув правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="e7a53-278">Open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="e7a53-279">Нажмите кнопку **Копировать**/скопировать  >  **StackTrace**.</span><span class="sxs-lookup"><span data-stu-id="e7a53-279">Choose **Copy** > **Copy stacktrace**.</span></span>  
    
<span data-ttu-id="e7a53-280">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1139615][CR1139615].</span><span class="sxs-lookup"><span data-stu-id="e7a53-280">To review the history of this feature in the Chromium open-source project, navigate to Issue [1139615][CR1139615].</span></span>

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Копирование StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   <span data-ttu-id="e7a53-282">Копирование StackTrace</span><span class="sxs-lookup"><span data-stu-id="e7a53-282">Copy stacktrace</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-283">Предварительный просмотр значения переменной Wasm на onmouseover</span><span class="sxs-lookup"><span data-stu-id="e7a53-283">Preview Wasm variable value on mouseover</span></span>  

<span data-ttu-id="e7a53-284">Используйте эту функцию для проверки значения переменной Assembly \ (Wasm \) при приостановке кода.</span><span class="sxs-lookup"><span data-stu-id="e7a53-284">Use this feature to review the value of a WebAssembly \(Wasm\) variable when your code is paused.</span></span>  <span data-ttu-id="e7a53-285">Для отображения текущего значения переменной наведите указатель мыши на переменную.</span><span class="sxs-lookup"><span data-stu-id="e7a53-285">To display the current value of a variable, hover on a variable.</span></span>  <span data-ttu-id="e7a53-286">Чтобы просмотреть обновления в реальном времени для этой функции в проекте Open-Source Chromium, перейдите в раздел проблемы [1058836][CR1058836] и [1071432][CR1071432].</span><span class="sxs-lookup"><span data-stu-id="e7a53-286">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [1058836][CR1058836] and [1071432][CR1071432].</span></span>  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Предварительный просмотр переменной Wasm на onmouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   <span data-ttu-id="e7a53-288">Предварительный просмотр переменной Wasm на onmouseover</span><span class="sxs-lookup"><span data-stu-id="e7a53-288">Preview Wasm variable on mouseover</span></span>  
:::image-end:::  

### <span data-ttu-id="e7a53-289">Единые единицы измерения для размеров файлов и памяти</span><span class="sxs-lookup"><span data-stu-id="e7a53-289">Consistent units of measurement for sizes of files and memory</span></span>  

<span data-ttu-id="e7a53-290">DevTools теперь постоянно используется `kB` для отображения размеров файлов и памяти.</span><span class="sxs-lookup"><span data-stu-id="e7a53-290">DevTools now consistently use `kB` for displaying sizes of files and memory.</span></span>  <span data-ttu-id="e7a53-291">Ранее DevTools смешанный `kB` и `KiB` .</span><span class="sxs-lookup"><span data-stu-id="e7a53-291">Previously DevTools mixed `kB` and `KiB`.</span></span>

*   `kB` <span data-ttu-id="e7a53-292">или КБ \ (10 ^ 3 или 1000 байт \)</span><span class="sxs-lookup"><span data-stu-id="e7a53-292">or kilobyte \(10^3 or 1000 bytes\)</span></span>  
*   `KiB` <span data-ttu-id="e7a53-293">или kibibyte \ (2 ^ 10 или 1024 байт \)</span><span class="sxs-lookup"><span data-stu-id="e7a53-293">or kibibyte \(2^10 or 1024 bytes\)</span></span>  
    
<span data-ttu-id="e7a53-294">Например, **Сетевое** средство, ранее использованное `kB` в этикетках, которое использовалось для `KiB` вычислений.</span><span class="sxs-lookup"><span data-stu-id="e7a53-294">For example, the **Network** tool previously used `kB` in the labels, but used `KiB` in calculations.</span></span>  <span data-ttu-id="e7a53-295">Ваше мнение показало, что эта несогласованность привела к путанице.</span><span class="sxs-lookup"><span data-stu-id="e7a53-295">Your feedback showed that this inconsistency caused confusion.</span></span>  <span data-ttu-id="e7a53-296">Чтобы просмотреть историю этой функции в проекте Open-Source Chromium, перейдите к вопросу [1035309][CR1035309].</span><span class="sxs-lookup"><span data-stu-id="e7a53-296">To review the history of this feature in the Chromium open-source project, navigate to Issue [1035309][CR1035309].</span></span>  

## <span data-ttu-id="e7a53-297">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e7a53-297">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="e7a53-298">Если вы используете операционную систему Windows, Linux или macOS, в качестве браузера разработки по умолчанию рекомендуется использовать [каналы предварительного просмотра Microsoft Edge] [MicrosoftEdgePreviewChannels].</span><span class="sxs-lookup"><span data-stu-id="e7a53-298">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="e7a53-299">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="e7a53-299">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="e7a53-300">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="e7a53-300">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Трехмерный вид | Документы Microsoft"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Обзор консоли | Документы Microsoft"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры: Настройка Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Эмуляция мобильных устройств в Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Включить редактор сочетаний клавиш — экспериментальные функции | Документы Microsoft"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Включение составных слоев в режиме трехмерной графики — экспериментальные функции | Документы Microsoft"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с помощью средства Microsoft Edge DevTools "вопросы" | Документы Microsoft"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Копирование отформатированного ответа JSON в буфер обмена — Справка по анализу сети | Документы Microsoft"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Просмотр разбиения по времени для запроса на анализ сети | Документы Microsoft"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Использование Chromium для проверки автоматизации тестов Документы Microsoft"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Microsoft"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Настройка сочетаний клавиш в окне "Параметры" — новые возможности DevTools (Microsoft Edge 87) | Документы Microsoft"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "отзыв о веб-подсказках на панели "вопросы" — новые возможности DevTools (Microsoft Edge 85) | Документы Microsoft"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Скачать "|" Разработчик Майкрософт"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Скачайте каналы предварительной оценки Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Код Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  

[CR174309]: https://crbug.com/174309 "Ошибка 174309: DevTools: разрешить настройку сочетаний клавиш и привязок клавиш | Ошибки Chromium"  
[CR945786]: https://crbug.com/945786 "Ошибка 945786: DevTools: разрешить переопределение навигатора. Storage. Оценка () | Ошибки Chromium"  
[CR1029427]: https://crbug.com/1029427 "Ошибка 1029427: сократите нагрузку на передачу сообщений протокола в интерфейсе | Ошибки Chromium"  
[CR1035309]: https://crbug.com/1035309 "Дата_выпуска 1035309: DevTools должен постоянно использовать для обозначения мегабайта (МБ), а не mebibyte | Ошибки Chromium"  
[CR1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools | Ошибки Chromium"  
[CR1058836]: https://crbug.com/1058836 "Проблема 1058836: проблемы с UX при отладке Wasm | Ошибки Chromium"  
[CR1071432]: https://crbug.com/1071432 "Вопрос 1071432: ☂️ Wasm Basic Developer | Ошибки Chromium"  
[CR1107766]: https://crbug.com/1107766 "Ошибка 1107766: отображает сведения о кадрах, созданных с помощью "Window. Open ()" в дереве кадров | Ошибки Chromium"  
[CR1122507]: https://crbug.com/1122507 "Ошибка 1122507: сведения о сотруднике Surface в представлении дерева кадров | Ошибки Chromium"  
[CR1126178]: https://crbug.com/1126178 "Ошибка 1126178: ☂ DevTools: CSS <Type> Components | Ошибки Chromium"  
[CR1130556]: https://crbug.com/1130556 "Ошибка 1130556: DevTools: Проверка резервных изображений (эмуляция) | Ошибки Chromium"  
[CR1132084]: https://crbug.com/1132084 "Ошибка 1132084: простой способ скопировать полезные данные запроса JSON | Ошибки Chromium"  
[CR1136394]: https://crbug.com/1136394 "Ошибка 1136394: средство управления подсказкой | Ошибки Chromium"  
[CR1138633]: https://crbug.com/1138633 "Ошибка 1138633: DevTools: CSS <Angle> компонент должен отражать его внешний вид свойства в фоновом режиме "Часы" | Ошибки Chromium"  
[CR1139615]: https://crbug.com/1139615 "Ошибка 1139615: инициатору сети следует предоставить возможность копировать трассировку стека | Ошибки Chromium"  
[CR1139899]: https://crbug.com/1139899 "Ошибка 1139899: создание отчета о доступности с ИНТЕРФЕЙСом в режиме "сведения о кадре" | Ошибки Chromium"  
[CR1139945]: https://crbug.com/1139945 "Вопрос 1139945: значки свойств CSS для подэлементного бокса на панели «Стили» | Ошибки Chromium"  
[CR1141824]: https://crbug.com/1141824 "Ошибка 1141824: ускорение работы с отчетами об ошибках CORS в DevTools | Ошибки Chromium"  
[CR1144090]: https://crbug.com/1144090 "Ошибка 1144090: Добавление графических элементов стиля Flex в дерево Elements | Ошибки Chromium"  
[CR1146985]: https://crbug.com/1146985 "Проблема 1146985: очищенный текст по-прежнему отображается в текстовом поле в разделе "хранилище" окна "средства разработки" | Ошибки Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Ошибки CORS | Цепь"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Общий доступ к ресурсам через источник (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Использование настраиваемых свойств CSS (переменных) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Конструкторы — окно | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "Подсказка"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Специальные возможности | Подсказка"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Совместимость | Подсказка"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Производительность | Подсказка"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Ловушки | Подсказка"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | Подсказка"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Безопасность | Подсказка"  

> [!NOTE]
> <span data-ttu-id="e7a53-351">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e7a53-351">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e7a53-352">Исходная страница [будет найдена, и](https://developers.google.com/web/updates/2020/11/devtools/index) ее можно создать с помощью [Jecelyn Yeen][JecelynYeen] \ (разработчик отвечает, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="e7a53-352">The original page is found [here](https://developers.google.com/web/updates/2020/11/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e7a53-354">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e7a53-354">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
