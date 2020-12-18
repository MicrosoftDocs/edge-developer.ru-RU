---
description: Используйте средство "Проблемы" для поиска и устранения проблем с веб-сайтом.
title: Поиск и устранение проблем с средством Microsoft Edge DevTools Issues
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8bd3e5950572a9d3fdce71ec6cd935f6b6d6a0b7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230665"
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

# <span data-ttu-id="03e15-104">Поиск и устранение проблем с средством Microsoft Edge DevTools Issues</span><span class="sxs-lookup"><span data-stu-id="03e15-104">Find and fix problems with the Microsoft Edge DevTools Issues tool</span></span>  

<span data-ttu-id="03e15-105">Средство **"Проблемы"** в Microsoft Edge DevTools позволяет уменьшить помехи в уведомлении **консоли.**</span><span class="sxs-lookup"><span data-stu-id="03e15-105">The **Issues** tool in Microsoft Edge DevTools reduces the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="03e15-106">Используйте его для поиска решений проблем, обнаруженных браузером, таких как проблемы с файлами cookie и смешанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="03e15-106">Use it to find solutions to problems detected by the browser, such as cookie issues and mixed content.</span></span>  

> [!NOTE]
> <span data-ttu-id="03e15-107">В Microsoft Edge 84 средство **"Проблемы"** поддерживает три типа проблем:</span><span class="sxs-lookup"><span data-stu-id="03e15-107">In Microsoft Edge 84, the **Issues** tool supports three types of issue:</span></span>  
> *   [<span data-ttu-id="03e15-108">Проблемы с файлами cookie</span><span class="sxs-lookup"><span data-stu-id="03e15-108">Cookie problems</span></span>][MDNSameSiteCookies]  
> *   [<span data-ttu-id="03e15-109">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="03e15-109">Mixed content</span></span>][MDNMixedContent]  
> *   [<span data-ttu-id="03e15-110">Проблемы COEP</span><span class="sxs-lookup"><span data-stu-id="03e15-110">COEP issues</span></span>][W3CCOEPSpec]
> 
> <span data-ttu-id="03e15-111">Группа разработчиков Microsoft Edge DevTools планирует поддерживать дополнительные типы проблем в будущих версиях Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03e15-111">The Microsoft Edge DevTools team plans to support more issue types in future versions of Microsoft Edge.</span></span>  

## <span data-ttu-id="03e15-112">Открытие средства "Проблемы" в средстве DevTools</span><span class="sxs-lookup"><span data-stu-id="03e15-112">Open the Issues tool in the DevTools drawer</span></span>  

1.  <span data-ttu-id="03e15-113">Посетите страницу, например [samesite-sandbox.glitch.me,][GlitchSamesiteSandbox]которая содержит проблемы, которые необходимо исправить.</span><span class="sxs-lookup"><span data-stu-id="03e15-113">Visit a page, such as [samesite-sandbox.glitch.me][GlitchSamesiteSandbox], that contains issues to fix.</span></span>  
1.  <span data-ttu-id="03e15-114">[Откройте DevTools.][DevtoolsOpen]</span><span class="sxs-lookup"><span data-stu-id="03e15-114">[Open DevTools][DevtoolsOpen].</span></span>  
1.  :::row:::
       :::column span="":::
          <span data-ttu-id="03e15-115">Choose the **Go to Issues** button in the yellow warning bar.</span><span class="sxs-lookup"><span data-stu-id="03e15-115">Choose the **Go to Issues** button in the yellow warning bar.</span></span>  
          
          :::image type="complex" source="../media/issues-open-issues-tab.msft.png" alt-text="Перейдите к кнопке "Проблемы" в желтой панели предупреждения при обнаружении проблем" lightbox="../media/issues-open-issues-tab.msft.png":::
             <span data-ttu-id="03e15-117">Кнопка **"Перейти к вопросам"** в желтой панели предупреждения при обнаружении проблем.</span><span class="sxs-lookup"><span data-stu-id="03e15-117">The **Go to Issues** button in the yellow warning bar when Issues are detected.</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="03e15-118">Кроме того, выберите **пункт "Проблемы"** в меню **"Дополнительные средства".**</span><span class="sxs-lookup"><span data-stu-id="03e15-118">Alternatively, choose **Issues** from the **More tools** menu.</span></span>  
          
          :::image type="complex" source="../media//issues-more-tools-menu.msft.png" alt-text="Средство "Проблемы" в меню "Дополнительные средства"" lightbox="../media//issues-more-tools-menu.msft.png":::
             <span data-ttu-id="03e15-120">**Средство "Проблемы"** в **меню "Дополнительные средства"**</span><span class="sxs-lookup"><span data-stu-id="03e15-120">**Issues** tool in **More tools** menu</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  <span data-ttu-id="03e15-121">При необходимости **выберите кнопку "Перезагрузить** страницу".</span><span class="sxs-lookup"><span data-stu-id="03e15-121">Select the **Reload page** button, if necessary.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-before-refresh.msft.png" alt-text="Средство "Проблемы" в средстве "DevTools Drawer" с кнопкой "Перезагрузить страницу"" lightbox="../media/issues-tab-before-refresh.msft.png":::
       <span data-ttu-id="03e15-123">**Средство "Проблемы"** в средстве "DevTools Drawer" с **кнопкой "Перезагрузить страницу"**</span><span class="sxs-lookup"><span data-stu-id="03e15-123">**Issues** tool in the DevTools Drawer with **Reload page** button</span></span>  
    :::image-end:::  

    <span data-ttu-id="03e15-124">Проблемы, о которые **сообщается** в консоли, довольно сложно понять, например предупреждения cookie на следующем изображении.</span><span class="sxs-lookup"><span data-stu-id="03e15-124">The issues reported in the **Console** are quite hard to understand, such as the cookie warnings in the following image.</span></span>  <span data-ttu-id="03e15-125">В зависимости от сообщений о проблемах может быть не ясно, что необходимо сделать.</span><span class="sxs-lookup"><span data-stu-id="03e15-125">Based upon the reported issues, it may not be clear what you must do.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-after-refresh.msft.png" alt-text="Средство "Проблемы" в средстве DevTools Drawer с тремя вопросами cookie" lightbox="../media/issues-tab-after-refresh.msft.png":::
       <span data-ttu-id="03e15-127">**Средство "Проблемы"** в средстве DevTools Drawer с тремя вопросами cookie</span><span class="sxs-lookup"><span data-stu-id="03e15-127">**Issues** tool in the DevTools Drawer with three cookie issues</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="03e15-128">Просмотр элементов в средстве "Проблемы"</span><span class="sxs-lookup"><span data-stu-id="03e15-128">View items in the Issues tool</span></span>  

<span data-ttu-id="03e15-129">Средство **"Проблемы"** в средстве "DevTools Drawer" представляет предупреждения структурированным, агрегируемым и в действии способом.</span><span class="sxs-lookup"><span data-stu-id="03e15-129">The **Issues** tool in the DevTools Drawer presents warnings in a structured, aggregated, and actionable way.</span></span>  

1.  <span data-ttu-id="03e15-130">Выберите элемент в средстве **"Проблемы",** чтобы получить инструкции по устранению проблемы и поиску затронутых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03e15-130">Select an item in the **Issues** tool to get guidance on how to fix the issue and find affected resources.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-issue-open.msft.png" alt-text="Пометить межсемейные файлы cookie как безопасные, открытые в средстве "Проблемы"" lightbox="../media/issues-tab-issue-open.msft.png":::
       <span data-ttu-id="03e15-132">**Пометить межсемейные файлы cookie как безопасные,** открытые в **средстве "Проблемы"**</span><span class="sxs-lookup"><span data-stu-id="03e15-132">**Mark cross-site cookies as Secure** issue open in the **Issues** tool</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="03e15-133">Каждый элемент имеет четыре компонента:</span><span class="sxs-lookup"><span data-stu-id="03e15-133">Each item has four components:</span></span>  
    
    *   <span data-ttu-id="03e15-134">Заголовок, описывающий проблему.</span><span class="sxs-lookup"><span data-stu-id="03e15-134">A headline describing the issue.</span></span>  
    *   <span data-ttu-id="03e15-135">Описание, предоставляющая контекст и решение.</span><span class="sxs-lookup"><span data-stu-id="03e15-135">A description providing the context and the solution.</span></span>  
    *   <span data-ttu-id="03e15-136">Раздел **"ЗАТРОНУТЫЕ** РЕСУРСЫ", который ссылается на ресурсы в соответствующем контексте DevTools, например на панели "Сеть".</span><span class="sxs-lookup"><span data-stu-id="03e15-136">An **AFFECTED RESOURCES** section that links to resources within the appropriate DevTools context such as the Network panel.</span></span>  
    *   <span data-ttu-id="03e15-137">Ссылки на дополнительные рекомендации.</span><span class="sxs-lookup"><span data-stu-id="03e15-137">Links to further guidance.</span></span>  
    
1.  <span data-ttu-id="03e15-138">Выберите элементы в **AFFECTED RESOURCES,** чтобы просмотреть сведения.</span><span class="sxs-lookup"><span data-stu-id="03e15-138">Select items in **AFFECTED RESOURCES** to view details.</span></span>  <span data-ttu-id="03e15-139">В следующем примере пометка меж сайта **cookie как** проблема "Безопасная" влияет на один файл cookie и два запроса.</span><span class="sxs-lookup"><span data-stu-id="03e15-139">In the following example, the **Mark cross-site cookies as Secure** issue affects one cookie and two requests.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-affected-resources.msft.png" alt-text="Затронутые ресурсы открываются на вкладке "Ящик проблем"" lightbox="../media/issues-tab-affected-resources.msft.png":::
       <span data-ttu-id="03e15-141">Затронутые ресурсы открываются в средстве **"Проблемы"** в средстве "DevTools Drawer"</span><span class="sxs-lookup"><span data-stu-id="03e15-141">Affected resources open in the **Issues** tool in the DevTools Drawer</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="03e15-142">Просмотр проблем в контексте</span><span class="sxs-lookup"><span data-stu-id="03e15-142">View issues in context</span></span>  

1.  <span data-ttu-id="03e15-143">Выберите ссылку на ресурс, чтобы просмотреть элемент в соответствующем контексте в DevTools.</span><span class="sxs-lookup"><span data-stu-id="03e15-143">Select a resource link to view the item in the appropriate context within DevTools.</span></span>  <span data-ttu-id="03e15-144">В следующем примере выберите в области `samesite-sandbox.glitch.me` **"Запросы",** чтобы показать файлы cookie, прикрепленные к этому запросу.</span><span class="sxs-lookup"><span data-stu-id="03e15-144">In the following example, select `samesite-sandbox.glitch.me` under **Requests** to show the cookies attached to that request.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-request.msft.png" alt-text="Просмотр затронутой области "Cookie" на панели "Сеть DevTools"" lightbox="../media/issues-tab-view-request.msft.png":::
       <span data-ttu-id="03e15-146">Просмотр затронутой области "Cookie" \*\*\*\* на панели "Сеть DevTools"</span><span class="sxs-lookup"><span data-stu-id="03e15-146">View the affected cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="03e15-147">Прокрутите страницу, чтобы просмотреть элемент с проблемой: в следующем примере файл `ck02` cookie.</span><span class="sxs-lookup"><span data-stu-id="03e15-147">Scroll to view the item with a problem: for the following example, the `ck02` cookie.</span></span>  <span data-ttu-id="03e15-148">Наведите курсор на **столбец SameSite,** чтобы увидеть `None` значение, обнаруженного проблемой.</span><span class="sxs-lookup"><span data-stu-id="03e15-148">Hover over the **SameSite** column to see the `None` value that the issue detected.</span></span>  
    
    :::image type="complex" source="../media/issues-tab-view-issue.msft.png" alt-text="Отсутствует значение в столбце SameSite для файла cookie ck02 на панели DevTools Network" lightbox="../media/issues-tab-view-issue.msft.png":::
       `None` <span data-ttu-id="03e15-150">значение в **столбце SameSite** для файла cookie на панели `ck02` Сети DevTools \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03e15-150">value in the **SameSite** column for the `ck02` cookie in the DevTools **Network** panel</span></span>  
    :::image-end:::  

## <span data-ttu-id="03e15-151">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03e15-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsOpen]: ../open/index.md "Откройте Microsoft Edge DevTools | Документы Майкрософт"  

[GlitchSamesiteSandbox]: https://samesite-sandbox.glitch.me "Тесты файлов cookie SameSite | Временный сбой"  

[MDNSameSiteCookies]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite "Файлы cookie SameSite | MDN"  
[MDNMixedContent]: https://developer.mozilla.org/docs/Web/Security/Mixed_content "Смешанное содержимое | MDN"  

[W3CCOEPSpec]: https://wicg.github.io/cross-origin-embedder-policy "Политика встраивляемого перекрестного источника | Группа сообщества веб-инкуаторов"  

> [!NOTE]
> <span data-ttu-id="03e15-157">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03e15-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="03e15-158">Исходная страница находится [здесь](https://developers.google.com/web/tools/chrome-devtools/issues/index) и автором [Sam Dutton][SamDutton] \(Developer Advocate\).</span><span class="sxs-lookup"><span data-stu-id="03e15-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/issues/index) and is authored by [Sam Dutton][SamDutton] \(Developer Advocate\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="03e15-160">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="03e15-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[SamDutton]: https://developers.google.com/web/resources/contributors/samdutton  
