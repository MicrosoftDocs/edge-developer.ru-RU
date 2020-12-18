---
description: Режим IE и Microsoft Edge (Chromium) DevTools
title: Режим Internet Explorer и DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, ie11, Internet Explorer 11, режим ie
ms.openlocfilehash: c88da78e073a75a664561aba899ca5c8ada78477
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235155"
---
# <span data-ttu-id="2ee46-104">Режим Internet Explorer и DevTools</span><span class="sxs-lookup"><span data-stu-id="2ee46-104">Internet Explorer mode and the DevTools</span></span>  

<span data-ttu-id="2ee46-105">В этой статье описывается, как режим Internet Explorer \(режим IE\) интегрируется с Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ee46-105">This article describes how Internet Explorer mode \(IE mode\) integrates with the Microsoft Edge \(Chromium\) DevTools.</span></span>  

## <span data-ttu-id="2ee46-106">Общее представление о режиме IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-106">Understanding IE mode</span></span>  

<span data-ttu-id="2ee46-107">Режим IE позволяет предприятиям указывать список веб-сайтов, которые работают только в Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-107">IE mode allows enterprises to specify a list of web sites that only work in Internet Explorer 11.</span></span>  <span data-ttu-id="2ee46-108">При переходе к этим веб-сайтам в Microsoft Edge \(Chromium\) экземпляр Internet Explorer 11 запускается и отрисовка сайта на вкладке.  Эта функция позволяет предприятиям управлять совместимостью с технологиями, которые в настоящее время несовместимы с современными веб-браузерами.</span><span class="sxs-lookup"><span data-stu-id="2ee46-108">When you navigate to these web sites in Microsoft Edge \(Chromium\), an instance of Internet Explorer 11 runs and renders the site in a tab.  The functionality allows enterprises to manage compatibility with technologies that are currently not compatible with any modern web browsers.</span></span>  <span data-ttu-id="2ee46-109">Поддержка следующих технологий включена в режим IE.</span><span class="sxs-lookup"><span data-stu-id="2ee46-109">Support for the following technologies is included in IE mode.</span></span>  

*   <span data-ttu-id="2ee46-110">Режимы документов IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-110">IE document modes</span></span>  
*   <span data-ttu-id="2ee46-111">элементы ActiveX;</span><span class="sxs-lookup"><span data-stu-id="2ee46-111">ActiveX controls</span></span>  
*   <span data-ttu-id="2ee46-112">другие устаревшие компоненты</span><span class="sxs-lookup"><span data-stu-id="2ee46-112">other legacy components</span></span>  

<span data-ttu-id="2ee46-113">В режиме IE процесс отрисовки основан на Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-113">In IE mode, the rendering process is based on Internet Explorer 11.</span></span>  <span data-ttu-id="2ee46-114">Диспетчер процессов Microsoft Edge \(Chromium\) обрабатывает время существования процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2ee46-114">The Microsoft Edge \(Chromium\) process manager handles the lifetime of the rendering process.</span></span>  <span data-ttu-id="2ee46-115">Она ограничена сроком действия вкладки для определенного сайта \(или app\).</span><span class="sxs-lookup"><span data-stu-id="2ee46-115">It is constrained to the lifetime of the tab for a specific site \(or app\).</span></span>  <span data-ttu-id="2ee46-116">Когда вкладка отображается в режиме IE, индикатор событий отображается в адресной панели для определенной вкладки.</span><span class="sxs-lookup"><span data-stu-id="2ee46-116">When a tab renders in IE mode, a badge appears in the address bar for the specific tab.</span></span>  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Индикатор событий режима IE в адресной панели" lightbox="../media/ie-mode-badge.msft.png":::
   <span data-ttu-id="2ee46-118">Индикатор событий режима IE в адресной панели</span><span class="sxs-lookup"><span data-stu-id="2ee46-118">IE mode badge in the address bar</span></span>  
:::image-end:::  

<span data-ttu-id="2ee46-119">Режим IE в настоящее время доступен в Windows 10 версии 1903 \(обновление за май 2019 г.), но скоро появится на всех поддерживаемых платформах Windows.</span><span class="sxs-lookup"><span data-stu-id="2ee46-119">IE mode is currently available on Windows 10 Version 1903 \(May 2019 Update\), but is coming soon to all supported Windows platforms.</span></span>  

## <span data-ttu-id="2ee46-120">Запуск DevTools на вкладке в режиме IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-120">Launching the DevTools on a tab in IE mode</span></span>  

<span data-ttu-id="2ee46-121">Если вы пытаетесь просмотреть режим документов веб-сайта в режиме IE, выберите индикатор событий в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="2ee46-121">If you are trying to view the document mode of a web site in IE mode, choose the badge in the address bar.</span></span>  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Просмотр режима документов с помощью индикатора событий режима IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   <span data-ttu-id="2ee46-123">Просмотр режима документов с помощью индикатора событий режима IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-123">View document mode using IE mode badge</span></span>  
:::image-end:::  

<span data-ttu-id="2ee46-124">Если вкладка использует режим IE, DevTools не работает и возникают следующие условия.</span><span class="sxs-lookup"><span data-stu-id="2ee46-124">If a tab is using IE mode, the DevTools do not work and the following conditions occur.</span></span>

*   <span data-ttu-id="2ee46-125">Если выбрать или выбрать, будет запущен пустой экземпляр `F12` `Ctrl` + `Shift` + `I` Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ee46-125">If you select `F12` or select `Ctrl`+`Shift`+`I`, a blank instance of the Microsoft Edge \(Chromium\) DevTools is launched displays the following message.</span></span>  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   <span data-ttu-id="2ee46-126">If you open a contextual menu \(right-click\) and choose **View Source,** Notepad is launched.</span><span class="sxs-lookup"><span data-stu-id="2ee46-126">If you open a contextual menu \(right-click\) and choose **View Source**, Notepad is launched.</span></span>  
*   <span data-ttu-id="2ee46-127">Если открыть контекстное меню \(щелкните правой кнопкой мыши\), элемент **Inspect не** будет виден.</span><span class="sxs-lookup"><span data-stu-id="2ee46-127">If you open a contextual menu \(right-click\), the **Inspect Element** is not visible.</span></span>  

<span data-ttu-id="2ee46-128">Причина, по которой ряд средств в DevTools \*\*\*\* \(например, средства "Сеть" и "Производительность"), не работают, заключается в том, что механизм отрисовки переключается с Chromium на Internet Explorer 11 в режиме IE. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2ee46-128">The reason that a number of the tools within the DevTools \(like the **Network** and **Performance** tools\) do not work is the rendering engine switches from Chromium to Internet Explorer 11 in IE mode.</span></span>  <span data-ttu-id="2ee46-129">Чтобы предоставить отзыв, перейдите к [контакту с командой Разработчиков Microsoft Edge.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="2ee46-129">To provide feedback, navigate to [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools, запущенный в режиме IE" lightbox="../media/ie-mode-devtools.msft.png":::
   <span data-ttu-id="2ee46-131">DevTools, запущенный в режиме IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-131">DevTools launched in IE mode</span></span>  
:::image-end:::  

<span data-ttu-id="2ee46-132">Чтобы протестировать веб-сайт на основе Internet Explorer 11 (или app\) в Internet Explorer 11 и режиме IE, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2ee46-132">To test your Internet Explorer 11-based website \(or app\) in Internet Explorer 11 and IE mode, perform the following steps.</span></span>  

1.  <span data-ttu-id="2ee46-133">Откройте Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-133">Open Internet Explorer 11.</span></span>  
    *   <span data-ttu-id="2ee46-134">В Windows 10 найдите ярлык для Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-134">On Windows 10, locate the shortcut for Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="2ee46-135">**Меню "Пуск"**  >  **Дополнительные возможности**  >  Windows **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="2ee46-135">**Start Menu** > **Windows Accessories** > **Internet Explorer 11**.</span></span>  
    *   <span data-ttu-id="2ee46-136">В Windows 7 найдите Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-136">On Windows 7, locate Internet Explorer 11.</span></span>
        1.  <span data-ttu-id="2ee46-137">**Меню "Пуск"**  >  **Internet Explorer 11**.</span><span class="sxs-lookup"><span data-stu-id="2ee46-137">**Start Menu** > **Internet Explorer 11**.</span></span>  
1.  <span data-ttu-id="2ee46-138">В Internet Explorer 11 откройте ту же веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="2ee46-138">In Internet Explorer 11, open the same webpage.</span></span>  
1.  <span data-ttu-id="2ee46-139">Запустите Internet Explorer DevTools.</span><span class="sxs-lookup"><span data-stu-id="2ee46-139">Launch the Internet Explorer DevTools.</span></span>  
    *   <span data-ttu-id="2ee46-140">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="2ee46-140">Select `F12`.</span></span>  
    *   <span data-ttu-id="2ee46-141">Наведите курсор в любом месте, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите элемент **Inspect.**</span><span class="sxs-lookup"><span data-stu-id="2ee46-141">Hover anywhere, open a contextual menu \(right-click\), and choose **Inspect element**.</span></span>  <span data-ttu-id="2ee46-142">Дополнительные сведения об использовании этих средств можно найти в средстве разработчика [F12.][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]</span><span class="sxs-lookup"><span data-stu-id="2ee46-142">For more information about how to use those tools, navigate to [Using the F12 developer tools][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].</span></span>  

## <span data-ttu-id="2ee46-143">Удаленная отладка и режим IE</span><span class="sxs-lookup"><span data-stu-id="2ee46-143">Remote debugging and IE mode</span></span>  

<span data-ttu-id="2ee46-144">Запустите Microsoft Edge \(Chromium\) с включенной удаленной отладки из интерфейса командной строки.</span><span class="sxs-lookup"><span data-stu-id="2ee46-144">Launch Microsoft Edge \(Chromium\) with remote debugging turned on from the command-line interface.</span></span>  <span data-ttu-id="2ee46-145">Visual Studio, Visual Studio Code и другие средства разработки обычно запускают команду для запуска Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2ee46-145">Visual Studio, Visual Studio Code, and other development tools typically run a command to launch Microsoft Edge.</span></span>  <span data-ttu-id="2ee46-146">Следующая команда запускает Microsoft Edge с портом удаленной отладки, установленным на `9222` ..</span><span class="sxs-lookup"><span data-stu-id="2ee46-146">The following command launches Microsoft Edge with the remote debugging port set to `9222`.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="2ee46-147">После запуска Microsoft Edge \(Chromium\) с помощью аргумента командной строки режим IE недоступен.</span><span class="sxs-lookup"><span data-stu-id="2ee46-147">After you launch Microsoft Edge \(Chromium\) using a command-line argument, IE mode is unavailable.</span></span>  <span data-ttu-id="2ee46-148">Вы по-прежнему можете перейти на веб-сайты \(или приложения\), которые в противном случае отображаются в режиме IE.</span><span class="sxs-lookup"><span data-stu-id="2ee46-148">You may still navigate to websites \(or apps\) that would otherwise display in IE mode.</span></span>  <span data-ttu-id="2ee46-149">Содержимое веб-сайта \(или app\) визуален с помощью Chromium, а не Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="2ee46-149">The website \(or app\) content renders using Chromium, not Internet Explorer 11.</span></span>  <span data-ttu-id="2ee46-150">Ожидается, что части веб-страниц, зависят от IE11, например ActiveX элементов управления, не будут правильно отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2ee46-150">Expect the parts of the webpages that rely on IE11, such as ActiveX controls, to not render correctly.</span></span>  <span data-ttu-id="2ee46-151">Индикатор событий в режиме IE не появляется в адресной панели.</span><span class="sxs-lookup"><span data-stu-id="2ee46-151">The IE mode badge does not appear in the address bar.</span></span>  

<span data-ttu-id="2ee46-152">Режим IE остается недоступным до полного закрытия и перезапуска Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="2ee46-152">IE mode remains unavailable until you completely close and restart Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="2ee46-153">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2ee46-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Использование средств разработчика F12 | Документы Майкрософт"  
