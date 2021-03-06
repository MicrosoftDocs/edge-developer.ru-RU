---
description: Режим IE и Microsoft Edge (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, ie11, internet explorer 11, ie mode
ms.openlocfilehash: e65869cd88b449dcde0aec25c77df27f99b78f8d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398604"
---
# <a name="internet-explorer-mode-and-the-devtools"></a><span data-ttu-id="4b0ba-104">Режим Internet Explorer и DevTools</span><span class="sxs-lookup"><span data-stu-id="4b0ba-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="4b0ba-105">В этой статье описывается, как режим Internet Explorer \(IE mode\) интегрируется с Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <a name="understanding-ie-mode"></a><span data-ttu-id="4b0ba-106">Понимание режима IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-106">Understanding IE mode</span></span>  

<span data-ttu-id="4b0ba-107">Режим IE позволяет предприятиям указывать список веб-сайтов, которые работают только в Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="4b0ba-108">При переходе на эти веб-сайты в Microsoft Edge \(Chromium\), экземпляр Internet Explorer 11 запускает и отрисовывает сайт на вкладке.  Функциональность позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время не совместимы с любыми современными веб-браузерами.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="4b0ba-109">Поддержка следующих технологий включена в режим IE.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="4b0ba-110">Режимы документов IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-110">IE document modes</span></span>  
*   <span data-ttu-id="4b0ba-111">элементы ActiveX;</span><span class="sxs-lookup"><span data-stu-id="4b0ba-111">ActiveX controls</span></span>  
*   <span data-ttu-id="4b0ba-112">другие устаревшие компоненты</span><span class="sxs-lookup"><span data-stu-id="4b0ba-112">other legacy components</span></span>  

<span data-ttu-id="4b0ba-113">В режиме IE процесс визуализации основан на Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="4b0ba-114">Диспетчер процессов Microsoft Edge \(Chromium\) обрабатывает весь срок службы процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="4b0ba-115">Она ограничена сроком службы вкладки для определенного сайта \(или app\).</span><span class="sxs-lookup"><span data-stu-id="4b0ba-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="4b0ba-116">При отрисовке вкладки в режиме IE в панели адресов для определенной вкладки появляется значок.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Значок режима IE в панели адресов" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="4b0ba-118">Значок режима IE в панели адресов</span><span class="sxs-lookup"><span data-stu-id="4b0ba-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="4b0ba-119">Режим IE в настоящее время доступен на Windows 10 Версии 1903 \(Обновление мая 2019\), но скоро появится на всех поддерживаемых платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a><span data-ttu-id="4b0ba-120">Запуск DevTools на вкладке в режиме IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="4b0ba-121">Если вы пытаетесь просмотреть режим документа веб-сайта в режиме IE, выберите значок в панели адресов.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Просмотр режима документа с помощью значка режима IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="4b0ba-123">Просмотр режима документа с помощью значка режима IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="4b0ba-124">Если вкладка использует режим IE, devTools не работают и возникают следующие условия.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="4b0ba-125">Если выбрать или выбрать, пустой экземпляр `F12` `Ctrl` + `Shift` + `I` запущенных DevTools Microsoft Edge \(Chromium\) отображает следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="4b0ba-126">Если вы откроете контекстное меню \(правой кнопкой мыши\) и выберите **View Source,** запущен блокнот.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="4b0ba-127">Если вы откроете контекстное меню \(правой кнопкой мыши\), элемент **Inspect** не отображается.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="4b0ba-128">Причина того, что ряд средств в DevTools \*\*\*\* \(как средства сети и производительности\) не работают, заключается в том, что двигатель отрисовки переключается с Chromium на Internet Explorer 11 в режиме IE. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b0ba-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="4b0ba-129">Чтобы обеспечить обратную связь, перейдите к [контакту с командой Microsoft Edge DevTools.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="4b0ba-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools запущен в режиме IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="4b0ba-131">DevTools запущен в режиме IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="4b0ba-132">Чтобы протестировать веб-сайт Internet Explorer 11 на основе \(или app\) в режиме Internet Explorer 11 и IE, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="4b0ba-133">Откройте Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="4b0ba-134">В Windows 10 найдите ярлык для Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="4b0ba-135">**Меню пуск**  >  Аксессуары Для **Windows**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="4b0ba-136">В Windows 7 найдите Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="4b0ba-137">**Меню пуск**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="4b0ba-138">В Internet Explorer 11 откройте ту же страницу.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="4b0ba-139">Запуск Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="4b0ba-140">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="4b0ba-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="4b0ba-141">Наведите курсор в любом месте, откройте контекстное меню \(правой кнопкой мыши\) и выберите **элемент Inspect**.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="4b0ba-142">Дополнительные сведения об использовании этих средств перейдите к использованию средств [разработчика F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="4b0ba-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <a name="remote-debugging-and-ie-mode"></a><span data-ttu-id="4b0ba-143">Удаленный отладка и режим IE</span><span class="sxs-lookup"><span data-stu-id="4b0ba-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="4b0ba-144">Запустите Microsoft Edge \(Chromium\) с включенной удаленной отладки из интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="4b0ba-145">Microsoft Visual Studio, Microsoft Visual Studio code и другие средства разработки обычно запускают команду для запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-145">Microsoft Visual Studio, Microsoft Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="4b0ba-146">Следующая команда запускает Microsoft Edge с портом удаленной `9222` отладки.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="4b0ba-147">После запуска Microsoft Edge \(Chromium\) с помощью аргумента командной строки режим IE недоступен.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="4b0ba-148">Вы по-прежнему можете перейти к веб-сайтам \(или приложениям\), которые в противном случае отображаются в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-148">You may still navigate to websites \(or apps\) that are otherwise displayed in IE mode.</span></span>  <span data-ttu-id="4b0ba-149">Содержимое веб-сайта \(или app\) отрисовывается с помощью Chromium, а не Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="4b0ba-150">Ожидается, что части веб-страниц, которые зависят от IE11, например ActiveX элементов управления, не отрисуются правильно.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-150">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="4b0ba-151">Значок режима IE не появляется в панели адресов.</span><span class="sxs-lookup"><span data-stu-id="4b0ba-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="4b0ba-152">Режим IE остается недоступным до полного закрытия и перезапуска Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="4b0ba-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4b0ba-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4b0ba-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработки F12 | Документы Майкрософт"  
