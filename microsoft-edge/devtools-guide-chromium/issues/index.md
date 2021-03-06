---
description: Используйте средство Issues для поиска и устранения проблем с веб-сайтом.
title: Поиск и устранение проблем с помощью средства Microsoft Edge DevTools Issues
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: e16bd926ea5bae35ad82f54ac5d1ae2028e3c59d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398978"
---
<!-- Copyright Sam Dutton 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="find-and-fix-problems-with-the-microsoft-edge-devtools-issues-tool"></a><span data-ttu-id="fe19e-104">Поиск и устранение проблем с помощью средства Microsoft Edge DevTools Issues</span><span class="sxs-lookup"><span data-stu-id="fe19e-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="fe19e-105">Средство **Issues** в Microsoft Edge DevTools снижает усталость уведомлений и помехи **консоли.**</span><span class="sxs-lookup"><span data-stu-id="fe19e-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="fe19e-106">Используйте его для поиска решений проблем, обнаруженных браузером, таких как проблемы с файлами cookie и смешанный контент.</span><span class="sxs-lookup"><span data-stu-id="fe19e-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="fe19e-107">В Microsoft Edge 84 средство **Issues** поддерживает три типа проблем:</span><span class="sxs-lookup"><span data-stu-id="fe19e-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="fe19e-108">Проблемы с cookie</span><span class="sxs-lookup"><span data-stu-id="fe19e-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="fe19e-109">Смешанный контент</span><span class="sxs-lookup"><span data-stu-id="fe19e-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="fe19e-110">Проблемы COEP</span><span class="sxs-lookup"><span data-stu-id="fe19e-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="fe19e-111">Группа Microsoft Edge DevTools планирует поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fe19e-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <a name="open-the-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="fe19e-112">Откройте средство Issues в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="fe19e-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="fe19e-113">Перейдите на веб-страницу, [например samesite-sandbox.glitch.me,][GlitchSamesiteSandbox]которая содержит проблемы, которые необходимо устранить.</span><span class="sxs-lookup"><span data-stu-id="fe19e-113">Navigate to a webpage, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="fe19e-114">[Откройте DevTools][DevtoolsOpen].</span><span class="sxs-lookup"><span data-stu-id="fe19e-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="fe19e-115">Выберите **кнопку Перейти к вопросам** в желтой панели предупреждения.</span><span class="sxs-lookup"><span data-stu-id="fe19e-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Перейдите к кнопке "Проблемы" в желтой панели предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="fe19e-117">Кнопка **"Перейти к вопросам"** в желтой панели предупреждения при обнаружении проблем.</span><span class="sxs-lookup"><span data-stu-id="fe19e-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="fe19e-118">Кроме того, выберите **Вопросы из** меню **More tools.**</span><span class="sxs-lookup"><span data-stu-id="fe19e-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Средство issues в меню More tools" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="fe19e-120">**Средство issues** в **меню More tools**</span><span class="sxs-lookup"><span data-stu-id="fe19e-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="fe19e-121">При необходимости **выберите кнопку** Перезагрузить страницу.</span><span class="sxs-lookup"><span data-stu-id="fe19e-121">Choose the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Проблема средства в ящике DevTools с кнопкой перезагрузки страницы" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="fe19e-123">**Проблема средства** в ящике DevTools с **кнопкой перезагрузки страницы**</span><span class="sxs-lookup"><span data-stu-id="fe19e-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="fe19e-124">Проблемы, которые сообщаются в **консоли,** довольно трудно понять, например предупреждения о cookie на следующем изображении.</span><span class="sxs-lookup"><span data-stu-id="fe19e-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="fe19e-125">На основании сообщений о проблемах может быть не ясно, что нужно сделать.</span><span class="sxs-lookup"><span data-stu-id="fe19e-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Проблема средства в ящике DevTools с тремя вопросами cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="fe19e-127">**Проблема средства** в ящике DevTools с тремя вопросами cookie</span><span class="sxs-lookup"><span data-stu-id="fe19e-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <a name="view-items-in-the-issues-tool"></a><span data-ttu-id="fe19e-128">Просмотр элементов в средстве Issues</span><span class="sxs-lookup"><span data-stu-id="fe19e-128">View items in the Issues tool</span></span>  

<span data-ttu-id="fe19e-129">Средство **Issues** в ящике DevTools представляет предупреждения структурированным, агрегируемым и действий.</span><span class="sxs-lookup"><span data-stu-id="fe19e-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="fe19e-130">Выберите элемент в средстве **Issues,** чтобы получить рекомендации по устранению проблемы и поиску затронутых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe19e-130">Choose an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Пометить межуголевое cookie как проблему Secure, открытую в средстве Issues" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="fe19e-132">**Пометить межуголевое cookie как проблему Secure,** открытую в **средстве Issues**</span><span class="sxs-lookup"><span data-stu-id="fe19e-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="fe19e-133">Каждый элемент имеет четыре компонента:</span><span class="sxs-lookup"><span data-stu-id="fe19e-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="fe19e-134">Заголовок, описывающий проблему.</span><span class="sxs-lookup"><span data-stu-id="fe19e-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="fe19e-135">Описание, предоставляющая контекст и решение.</span><span class="sxs-lookup"><span data-stu-id="fe19e-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="fe19e-136">Раздел **AFFECTED RESOURCES,** который связывается с ресурсами в соответствующем контексте DevTools, например с панелью Network.</span><span class="sxs-lookup"><span data-stu-id="fe19e-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="fe19e-137">Ссылки на дополнительные рекомендации.</span><span class="sxs-lookup"><span data-stu-id="fe19e-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="fe19e-138">Выберите элементы **в AFFECTED RESOURCES для** просмотра сведений.</span><span class="sxs-lookup"><span data-stu-id="fe19e-138">Choose items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="fe19e-139">В следующем примере **маркеры Mark в качестве** проблемы Secure затрагивают один файл cookie и два запроса.</span><span class="sxs-lookup"><span data-stu-id="fe19e-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Затронутые ресурсы, открытые в средстве Issues" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="fe19e-141">Затронутые ресурсы, открытые в **средстве Issues** в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="fe19e-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <a name="view-issues-in-context"></a><span data-ttu-id="fe19e-142">Просмотр проблем в контексте</span><span class="sxs-lookup"><span data-stu-id="fe19e-142">View issues in context</span></span>  

1.  <span data-ttu-id="fe19e-143">Выберите ссылку ресурса для просмотра элемента в соответствующем контексте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="fe19e-143">Choose a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="fe19e-144">В следующем примере выберите `samesite-sandbox.glitch.me` в **статье Запросы,** чтобы показать файлы cookie, присоединенные к этому запросу.</span><span class="sxs-lookup"><span data-stu-id="fe19e-144">In the following example, choose `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Просмотр затронутых файлов cookie в средстве Сети DevTools" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="fe19e-146">Просмотр затронутых файлов cookie в \*\*\*\* средстве Сети DevTools</span><span class="sxs-lookup"><span data-stu-id="fe19e-146">View the affected cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="fe19e-147">Прокрутите, чтобы просмотреть элемент с проблемой: в следующем примере — `ck02` файл cookie.</span><span class="sxs-lookup"><span data-stu-id="fe19e-147">Scroll to view the item with a problem:  for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="fe19e-148">Наведите курсор **на столбец SameSite,** чтобы просмотреть `None` обнаруженную проблему.</span><span class="sxs-lookup"><span data-stu-id="fe19e-148">Hover on the **SameSite** column to review the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Нет значения в столбце SameSite для cookie ck02 в средстве Сети DevTools" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="fe19e-150">значение в столбце **SameSite** для `ck02` cookie в \*\*\*\* средстве Сети DevTools</span><span class="sxs-lookup"><span data-stu-id="fe19e-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** tool</span></span>  
    :::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="fe19e-151">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fe19e-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Тесты cookie SameSite | Glitch"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Файлы cookie SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанный контент | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика встраивляемого | Группа сообщества веб-инкубаторов"  

> [!NOTE]
> <span data-ttu-id="fe19e-157">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe19e-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fe19e-158">Оригинальная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/issues/index) и является автором [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="fe19e-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fe19e-160">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe19e-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
