---
description: Узнайте, как отлалать элементы управления WebView2.
title: Начало отладки приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузером, edge html
ms.openlocfilehash: 4f94fe880f66f8aeb387d2db4a8bfaab20699466
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230700"
---
# <span data-ttu-id="9756a-104">Начало отладки приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="9756a-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="9756a-105">Цель средства управления Microsoft Edge WebView2 — объединить лучшие функции и средства разработки веб-приложений и приложений.</span><span class="sxs-lookup"><span data-stu-id="9756a-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="9756a-106">При разработке приложения WebView2 необходимо отлалать приложение.</span><span class="sxs-lookup"><span data-stu-id="9756a-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="9756a-107">В этой статье описаны различные средства для отлажений веб-кода и нативного кода в приложении WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="9756a-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9756a-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="9756a-109">Используйте инструменты разработчика [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-содержимого, отображаемого в элементе управления WebView2, так же, как вы можете отладить другую веб-страницу, отображаемую в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9756a-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="9756a-110">Чтобы открыть DevTools, установите фокус на веб-части управления и используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="9756a-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="9756a-111">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="9756a-111">Select `F12`.</span></span>  
*   <span data-ttu-id="9756a-112">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="9756a-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="9756a-113">Откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="9756a-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="9756a-114">Дополнительные сведения см. в [обзоре DevTools.][DevtoolsGuideChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="9756a-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="9756a-116">Отладка DevTools</span><span class="sxs-lookup"><span data-stu-id="9756a-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="9756a-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="9756a-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="9756a-118">Visual Studio предоставляет различные средства отладки для веб-кода и нативного кода в приложениях WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="9756a-119">В разделе Visual Studio основное внимание уделяется отладию элементов управления WebView, однако другие методы отладки в Visual Studio доступны как обычно.</span><span class="sxs-lookup"><span data-stu-id="9756a-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="9756a-120">Используйте следующий процесс для отлажений веб-кода и нативного кода только в приложениях Win32 или надстройки Office.</span><span class="sxs-lookup"><span data-stu-id="9756a-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9756a-121">При отладки приложения в Visual Studio с присоединенным отладителям выбор может вызвать собственный отладок, а не `F12` "Инструменты разработчика".</span><span class="sxs-lookup"><span data-stu-id="9756a-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="9756a-122">Выберите `Ctrl` + `Shift` + `I` или используйте контекстное меню \(щелкните правой кнопкой мыши\), чтобы избежать этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="9756a-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="9756a-123">Перед началом убедитесь, что выполнены следующие требования.</span><span class="sxs-lookup"><span data-stu-id="9756a-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="9756a-124">Для отлаки сценариев приложение должно быть запущено из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9756a-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="9756a-125">Отладка невозможно прикрепить к запущенной процедуре WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="9756a-126">Установите Visual Studio 2019 версии 16.4 Preview 2 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="9756a-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="9756a-127">Установите и настройте средства отладщика скриптов в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9756a-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="9756a-128">Выполните следующие действия, чтобы установить компонент **диагностики JavaScript** в разработке для **настольных компьютеров с помощью C++.**</span><span class="sxs-lookup"><span data-stu-id="9756a-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="9756a-129">В панели проводника Windows введите `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="9756a-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="9756a-130">Выберите **Visual Studio установщика,** чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="9756a-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="9756a-131">В установщике Visual Studio в установленной версии выберите **кнопку** "Еще" и выберите **"Изменить".**</span><span class="sxs-lookup"><span data-stu-id="9756a-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="9756a-132">В Visual Studio области **"Рабочие нагрузки"** выберите параметр "Разработка компьютеров **на C++".**</span><span class="sxs-lookup"><span data-stu-id="9756a-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio "Изменение рабочих нагрузок"" lightbox="./media/workloads.png":::
            <span data-ttu-id="9756a-134">Visual Studio "Изменение рабочих нагрузок"</span><span class="sxs-lookup"><span data-stu-id="9756a-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="9756a-135">Выберите **отдельные компоненты.**</span><span class="sxs-lookup"><span data-stu-id="9756a-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="9756a-136">В поле поиска введите `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="9756a-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="9756a-137">Выберите параметр **диагностики JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="9756a-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="9756a-138">Choose **Modify**.</span><span class="sxs-lookup"><span data-stu-id="9756a-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Вкладка "Изменение отдельных компонентов"" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="9756a-140">Visual Studio Вкладка "Изменение отдельных компонентов"</span><span class="sxs-lookup"><span data-stu-id="9756a-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="9756a-141">Включить отладку сценариев для приложений WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="9756a-142">В проекте WebView2 откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="9756a-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="9756a-143">В области **"Свойства конфигурации"** выберите **"Отладка".**</span><span class="sxs-lookup"><span data-stu-id="9756a-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="9756a-144">В области **"Тип отладка"** выберите **JavaScript (WebView2).**</span><span class="sxs-lookup"><span data-stu-id="9756a-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio конфигурации отладки" lightbox="./media/enbjs.png":::
           <span data-ttu-id="9756a-146">Visual Studio **конфигурации отладки**</span><span class="sxs-lookup"><span data-stu-id="9756a-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="9756a-147">Выполните следующие действия для отлаки приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="9756a-148">Чтобы установить точку останова в коде, наведите курсор слева от номера строки и выберите точку останова.</span><span class="sxs-lookup"><span data-stu-id="9756a-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="9756a-149">Адаптер отлаживки JS/TS не выполняет сопоставление исходных путей.</span><span class="sxs-lookup"><span data-stu-id="9756a-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="9756a-150">Необходимо открыть тот же путь, который связан с WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio точку останова" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="9756a-152">Visual Studio точку останова</span><span class="sxs-lookup"><span data-stu-id="9756a-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9756a-153">Чтобы запустить отладку, выберите размер бита платформы, а затем выберите зеленую кнопку воспроизведения рядом с локальным **отладильщиком Windows.**</span><span class="sxs-lookup"><span data-stu-id="9756a-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="9756a-154">Приложение запускается, и отладка подключается к первому созданному процессу WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio локального отладка Windows" lightbox="./media/run.png"::: 
       <span data-ttu-id="9756a-156">Visual Studio **локальный отладник Windows**</span><span class="sxs-lookup"><span data-stu-id="9756a-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9756a-157">В консоли **отладки**найдите выходные данные от отладки.</span><span class="sxs-lookup"><span data-stu-id="9756a-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio консоли отлаки" lightbox="./media/console.png"::: 
       <span data-ttu-id="9756a-159">Visual Studio консоли **отлаки**</span><span class="sxs-lookup"><span data-stu-id="9756a-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="9756a-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9756a-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="9756a-161">Используйте Microsoft Visual Studio Code для отлаки сценариев, которые запускают элементы управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="9756a-162">В Visual Studio Code выполните следующие действия для отлаки кода.</span><span class="sxs-lookup"><span data-stu-id="9756a-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="9756a-163">Проект должен иметь `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="9756a-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="9756a-164">Если в проекте нет файла, скопируйте следующий фрагмент кода и `launch.json` создайте `launch.json` новый файл.</span><span class="sxs-lookup"><span data-stu-id="9756a-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
    
1.  <span data-ttu-id="9756a-165">Чтобы установить точку останова в коде, наведите курсор на строку и выберите</span><span class="sxs-lookup"><span data-stu-id="9756a-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Точка останова за установлена в Visual Studio коде" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="9756a-167">Точка останова устанавливается в Visual Studio коде</span><span class="sxs-lookup"><span data-stu-id="9756a-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="9756a-168">Так Visual Studio Code не выполняет сопоставление источника, убедитесь, что вы установили точки останова в том же файле, который использует WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="9756a-169">Если пути не совпадают, код Visual Studio не приостанавливовка запущенного кода в точке останова.</span><span class="sxs-lookup"><span data-stu-id="9756a-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="9756a-170">Запустите код.</span><span class="sxs-lookup"><span data-stu-id="9756a-170">Run the code.</span></span>  
    1.  <span data-ttu-id="9756a-171">На **вкладке "Выполнить"** выберите конфигурацию запуска в меню в выпадаемом меню.</span><span class="sxs-lookup"><span data-stu-id="9756a-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="9756a-172">Чтобы начать отладку приложения, выберите "Начать отладку", который является зеленым треугольником рядом с drop down конфигурации запуска.</span><span class="sxs-lookup"><span data-stu-id="9756a-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio вкладки "Запуск кода"" lightbox="./media/runvs.png":::
           <span data-ttu-id="9756a-174">Visual Studio вкладки "Запуск кода"</span><span class="sxs-lookup"><span data-stu-id="9756a-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="9756a-175">Откройте **консоль отлаки,** чтобы просмотреть выходные данные и ошибки отлаки.</span><span class="sxs-lookup"><span data-stu-id="9756a-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio консоли отлаки кода" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="9756a-177">Visual Studio консоли отлаки кода</span><span class="sxs-lookup"><span data-stu-id="9756a-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9756a-178">**Дополнительные параметры:**</span><span class="sxs-lookup"><span data-stu-id="9756a-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="9756a-179">Отладка целевого веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9756a-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="9756a-180">В некоторых приложениях WebView2 можно использовать более одного управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="9756a-181">Чтобы выбрать отладку для управления WebView2 в этой ситуации, можно использовать целевую отладку webview2</span><span class="sxs-lookup"><span data-stu-id="9756a-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="9756a-182">Откройте `launch.json` и выполните следующие действия, чтобы использовать целевую отладку Веб-просмотр.</span><span class="sxs-lookup"><span data-stu-id="9756a-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="9756a-183">Подтвердим, `useWebview` что для параметра установлено заданный параметр `true` .</span><span class="sxs-lookup"><span data-stu-id="9756a-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="9756a-184">Добавьте `urlFilter` параметр.</span><span class="sxs-lookup"><span data-stu-id="9756a-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="9756a-185">Когда управление WebView2 переходит по URL-адресу, значение параметра используется для сравнения строк, которые `urlFilter` отображаются в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="9756a-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="9756a-186">При отладки приложения может потребоваться пошаговое начало процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9756a-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="9756a-187">Если веб-страницы отрисовываются на сайтах и у вас нет доступа к исходным кодам, можно использовать этот параметр, так как веб-страницы игнорируют невыявимые `?=value`  параметры.</span><span class="sxs-lookup"><span data-stu-id="9756a-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="9756a-188">После того как в URL-адресе будет найдено первое совпадение, отладка останавливается.</span><span class="sxs-lookup"><span data-stu-id="9756a-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="9756a-189">Невозможно одновременно отлалать два средства управления WebView2, так как порт CDP совместно используется всеми элементами управления WebView2 и использует один номер порта.</span><span class="sxs-lookup"><span data-stu-id="9756a-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="9756a-190">Отлагивание запущенных процессов</span><span class="sxs-lookup"><span data-stu-id="9756a-190">Debug running processes</span></span>  
    
    <span data-ttu-id="9756a-191">Возможно, вам потребуется присоединить отладчий отладок к запущенным процессам WebView2.</span><span class="sxs-lookup"><span data-stu-id="9756a-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="9756a-192">Для этого в `launch.json` окнах обновим `request` параметр до `attach` .</span><span class="sxs-lookup"><span data-stu-id="9756a-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="9756a-193">Чтобы разрешить отладку управления WebView2, необходимо открыть порт CDP.</span><span class="sxs-lookup"><span data-stu-id="9756a-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="9756a-194">Перед запуском отладка код должен быть создан таким образом, чтобы только один из них был открыт с помощью порта chrome Developer Protocol (CDP).</span><span class="sxs-lookup"><span data-stu-id="9756a-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="9756a-195">Параметры отлаки</span><span class="sxs-lookup"><span data-stu-id="9756a-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="9756a-196">Добавьте параметр `trace` в launch.js, чтобы включить трассировку отлаки.</span><span class="sxs-lookup"><span data-stu-id="9756a-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="9756a-197">Добавьте `trace` параметр.</span><span class="sxs-lookup"><span data-stu-id="9756a-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Сохраните выходные данные отлаки в файле журнала." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="9756a-199">Сохранение выходных данных отлаки в файле журнала</span><span class="sxs-lookup"><span data-stu-id="9756a-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Подробный вывод" lightbox="./media/verbose.png":::
                 <span data-ttu-id="9756a-201">Visual Studio отлаки кода с включенной подробной трассировой</span><span class="sxs-lookup"><span data-stu-id="9756a-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="9756a-202">Отлаговка надстроек Office.</span><span class="sxs-lookup"><span data-stu-id="9756a-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="9756a-203">Если вы отладка надстроек Office, откройте исходный код надстройки в отдельном экземпляре Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="9756a-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="9756a-204">Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладник к надстройки Office.</span><span class="sxs-lookup"><span data-stu-id="9756a-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="9756a-205">Устранение неполадок отладки</span><span class="sxs-lookup"><span data-stu-id="9756a-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="9756a-206">При использовании отладка могут возникнуть следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="9756a-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="9756a-207">Отладка не останавливается в точке останова, и вы вывод отладки.</span><span class="sxs-lookup"><span data-stu-id="9756a-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="9756a-208">Чтобы устранить проблему, подтвердим, что файл с точкой останова тот же, что используется в веб-view2.</span><span class="sxs-lookup"><span data-stu-id="9756a-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="9756a-209">Отладка не выполняет сопоставление исходных путей.</span><span class="sxs-lookup"><span data-stu-id="9756a-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="9756a-210">Вы не можете присоединяться к запущенным процессам, и вы получаете ошибку времени.</span><span class="sxs-lookup"><span data-stu-id="9756a-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="9756a-211">Чтобы устранить эту проблему, подтвердим, что для управления WebView2 открыт порт CDP.</span><span class="sxs-lookup"><span data-stu-id="9756a-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="9756a-212">Убедитесь, что значение в  `additionalBrowserArguments`  реестре правильное или параметры правильные.</span><span class="sxs-lookup"><span data-stu-id="9756a-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="9756a-213">Дополнительные сведения см. в дополнительных [данныхBrowserArguments для dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [additionalBrowserArguments для Win32.][Webview2ReferenceWin32Webview2IdlParameters]</span><span class="sxs-lookup"><span data-stu-id="9756a-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <span data-ttu-id="9756a-214">См. также</span><span class="sxs-lookup"><span data-stu-id="9756a-214">See also</span></span>  

*   <span data-ttu-id="9756a-215">Руководства по началу работы с WebView2 см. в руководстве [по началу работы с WebView2.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="9756a-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="9756a-216">Полный пример возможностей WebView2 см. в репозитарии [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="9756a-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="9756a-217">Дополнительные сведения об API WebView2 см. в справочнике [по API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="9756a-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="9756a-218">Дополнительные сведения о WebView2 см. в [поддоме "Ресурсы WebView2".][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="9756a-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <span data-ttu-id="9756a-219">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="9756a-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment — Globals | Документы Майкрософт"  
[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности - Отладатель JavaScript для Visual Studio Code — microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Приложения Microsoft Edge (Chromium) WebView — код Visual Studio отладка для Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
