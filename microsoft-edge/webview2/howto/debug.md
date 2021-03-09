---
description: Узнайте, как отлаговка элементов управления WebView2.
title: Начало отладки приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: f895634d5e005bb07579d9a5f41c6a988cd78a33
ms.sourcegitcommit: 140e09e508fa97f2d124f264d7d2ff77d12d1ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "11399846"
---
# <a name="get-started-debugging-webview2-apps"></a><span data-ttu-id="feb2c-104">Начало отладки приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="feb2c-104">Get started debugging WebView2 apps</span></span>  

<span data-ttu-id="feb2c-105">Цель управления Microsoft Edge WebView2 состоит в том, чтобы объединить лучшие функции и средства разработки веб-и родных приложений.</span><span class="sxs-lookup"><span data-stu-id="feb2c-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native app development features and tools.</span></span>  <span data-ttu-id="feb2c-106">При разработке приложения WebView2 необходимо отчудить приложение.</span><span class="sxs-lookup"><span data-stu-id="feb2c-106">When you develop your WebView2 app, you should debug your app.</span></span>  <span data-ttu-id="feb2c-107">В этой статье описаны различные средства, которые можно использовать для отлажений веб-кода и родного кода в приложении WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 app.</span></span>  

## [<a name="microsoft-edge-devtools"></a><span data-ttu-id="feb2c-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="feb2c-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="feb2c-109">Используйте средства разработчика [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-контента, отображаемого в средствах управления WebView2, так же, как вы можете отладить другую веб-страницу, отображаемую в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="feb2c-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="feb2c-110">Чтобы открыть DevTools, установите фокус на управление WebView и используйте одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="feb2c-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="feb2c-111">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-111">Select `F12`.</span></span>  
*   <span data-ttu-id="feb2c-112">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="feb2c-113">Откройте контекстное меню \(правой кнопкой мыши\) и выберите `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="feb2c-114">Дополнительные сведения перейдите к [обзору DevTools.][DevtoolsGuideChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="feb2c-114">For more information, navigate to [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="feb2c-116">Отладка DevTools</span><span class="sxs-lookup"><span data-stu-id="feb2c-116">DevTools debugging</span></span>  
:::image-end:::  

## [<a name="visual-studio"></a><span data-ttu-id="feb2c-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="feb2c-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="feb2c-118">Visual Studio предоставляет различные средства отладки для веб-и родного кода в приложениях WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-118">Visual Studio provides various debugging tools for web and native code in WebView2 apps.</span></span>  <span data-ttu-id="feb2c-119">В разделе Visual Studio основное внимание уделяется отладки элементов управления WebView, однако другие методы отладки в Visual Studio доступны в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="feb2c-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="feb2c-120">Используйте следующий процесс для отлажений веб-и родного кода в приложениях Win32 или надстройки Office.</span><span class="sxs-lookup"><span data-stu-id="feb2c-120">Use the following process to debug web and native code in Win32 apps or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="feb2c-121">Если отладить приложение в Visual Studio с подключенным отладильщиком, выбор может вызвать отладку, а не `F12` средства разработчика.</span><span class="sxs-lookup"><span data-stu-id="feb2c-121">When you debug your app in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="feb2c-122">Выберите `Ctrl` + `Shift` + `I` или используйте контекстное меню \(правой кнопкой мыши\), чтобы избежать ситуации.</span><span class="sxs-lookup"><span data-stu-id="feb2c-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="feb2c-123">Перед началом работы убедитесь, что следующие требования будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="feb2c-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="feb2c-124">Чтобы отламыть скрипты, приложение должно быть запущено из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="feb2c-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="feb2c-125">Нельзя прикрепить отладка к запущенной процедуре WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="feb2c-126">Установка Visual Studio версии 16.4 Preview 2 или более поздней версии 2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="feb2c-127">Установка и настройка средств отладки сценариев в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="feb2c-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="feb2c-128">Выполните следующие действия по установке компонента **диагностики JavaScript** в разработке настольных компьютеров **с помощью C++**.</span><span class="sxs-lookup"><span data-stu-id="feb2c-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    
    1.  <span data-ttu-id="feb2c-129">В панели Обозреватель Windows введите `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="feb2c-130">Выберите **Visual Studio установщик,** чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="feb2c-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="feb2c-131">В Visual Studio установщике в установленной версии выберите кнопку **More,** а затем **измените**.</span><span class="sxs-lookup"><span data-stu-id="feb2c-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="feb2c-132">В Visual Studio **в статье Workloads**выберите параметр **Desktop Development в параметре C++.**</span><span class="sxs-lookup"><span data-stu-id="feb2c-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio Экран изменения рабочих нагрузок" lightbox="./media/workloads.png":::
            <span data-ttu-id="feb2c-134">Visual Studio Экран изменения рабочих нагрузок</span><span class="sxs-lookup"><span data-stu-id="feb2c-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="feb2c-135">Выберите **отдельные компоненты.**</span><span class="sxs-lookup"><span data-stu-id="feb2c-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="feb2c-136">В поле поиска введите `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="feb2c-137">Выберите параметр **диагностики JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="feb2c-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="feb2c-138">Выберите **Изменение**.</span><span class="sxs-lookup"><span data-stu-id="feb2c-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Visual Studio Изменение вкладки отдельных компонентов" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="feb2c-140">Visual Studio Изменение вкладки отдельных компонентов</span><span class="sxs-lookup"><span data-stu-id="feb2c-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="feb2c-141">Включить отладку скриптов для приложений WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-141">Enable script debugging for WebView2 apps.</span></span>  
    1.  <span data-ttu-id="feb2c-142">В проекте WebView2 откройте контекстное меню \(правой кнопкой мыши\) и выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="feb2c-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="feb2c-143">В статье **Configuration Properties**выберите **отладку.**</span><span class="sxs-lookup"><span data-stu-id="feb2c-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="feb2c-144">В соответствии **с типом Debugger**выберите **JavaScript (WebView2).**</span><span class="sxs-lookup"><span data-stu-id="feb2c-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Visual Studio отладки свойства конфигурации" lightbox="./media/enbjs.png":::
           <span data-ttu-id="feb2c-146">Visual Studio **отладки свойства** конфигурации</span><span class="sxs-lookup"><span data-stu-id="feb2c-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="feb2c-147">Выполните следующие действия для отлаговки приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-147">Complete the following actions to debug your WebView2 app.</span></span>  

1.  <span data-ttu-id="feb2c-148">Чтобы установить точку разрыва в исходный код, наведите курсор слева от номера строки и выберите точку разрыва.</span><span class="sxs-lookup"><span data-stu-id="feb2c-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="feb2c-149">Адаптер отлажений JS/TS не выполняет сопоставление исходных путей.</span><span class="sxs-lookup"><span data-stu-id="feb2c-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="feb2c-150">Необходимо открыть тот же путь, который связан с веб-сайтом WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio точку разрыва" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="feb2c-152">Visual Studio точку разрыва</span><span class="sxs-lookup"><span data-stu-id="feb2c-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="feb2c-153">Чтобы запустить отладку, выберите размер бита платформы, а затем выберите зеленую кнопку воспроизведения рядом с **локальным Отладильщиком Windows.**</span><span class="sxs-lookup"><span data-stu-id="feb2c-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="feb2c-154">Приложение запускается, а отладка подключается к первому созданному процессу WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-154">The app runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio отладка Windows" lightbox="./media/run.png"::: 
       <span data-ttu-id="feb2c-156">Visual Studio **отладка Windows**</span><span class="sxs-lookup"><span data-stu-id="feb2c-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="feb2c-157">В консоли **отладки**найдите выход из отладки.</span><span class="sxs-lookup"><span data-stu-id="feb2c-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio отлаговка консоли" lightbox="./media/console.png"::: 
       <span data-ttu-id="feb2c-159">Visual Studio **отлаговка консоли**</span><span class="sxs-lookup"><span data-stu-id="feb2c-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a><span data-ttu-id="feb2c-160">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="feb2c-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="feb2c-161">Используйте Код Visual Studio Майкрософт для отлаговки скриптов, запускаемой в средствах управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="feb2c-162">В Visual Studio коде выполните следующие действия по отламыву кода.</span><span class="sxs-lookup"><span data-stu-id="feb2c-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="feb2c-163">В проекте должен быть `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="feb2c-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="feb2c-164">Если в проекте нет файла, скопируйте следующий фрагмент кода `launch.json` и создайте `launch.json` новый файл.</span><span class="sxs-lookup"><span data-stu-id="feb2c-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="feb2c-165">Visual Studio для сопоставления исходных путей кода теперь требуется URL-адрес, поэтому ваше приложение получает параметр командной строки при его старте.</span><span class="sxs-lookup"><span data-stu-id="feb2c-165">Visual Studio Code source path mapping now requires the URL, so your app now receives a command-line parameter when it starts.</span></span>  <span data-ttu-id="feb2c-166">При необходимости можно смело игнорировать `url` параметр.</span><span class="sxs-lookup"><span data-stu-id="feb2c-166">You may safely ignore the `url` parameter if needed.</span></span>  
    
1.  <span data-ttu-id="feb2c-167">Чтобы установить точку разрыва в исходный код, наведите курсор на строку и выберите</span><span class="sxs-lookup"><span data-stu-id="feb2c-167">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Точка breakpoint установлена в Visual Studio коде" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="feb2c-169">Точка breakpoint установлена в Visual Studio коде</span><span class="sxs-lookup"><span data-stu-id="feb2c-169">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="feb2c-170">Запустите код.</span><span class="sxs-lookup"><span data-stu-id="feb2c-170">Run the code.</span></span>  
    1.  <span data-ttu-id="feb2c-171">На **вкладке Run** выберите конфигурацию запуска из меню отсев.</span><span class="sxs-lookup"><span data-stu-id="feb2c-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="feb2c-172">Чтобы начать отладку приложения, выберите Пуск отладки, который является зеленым треугольником рядом с падением конфигурации запуска.</span><span class="sxs-lookup"><span data-stu-id="feb2c-172">To start debugging your app, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text=" Visual Studio вкладка "Запуск кода"" lightbox="./media/runvs.png":::
           <span data-ttu-id="feb2c-174">Visual Studio вкладка "Запуск кода"</span><span class="sxs-lookup"><span data-stu-id="feb2c-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="feb2c-175">Откройте **консоль отлаговка,** чтобы просмотреть выход отлагирования и ошибки.</span><span class="sxs-lookup"><span data-stu-id="feb2c-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text=" Visual Studio консоли отлаговка кода" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="feb2c-177">Visual Studio консоли отлаговка кода</span><span class="sxs-lookup"><span data-stu-id="feb2c-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="feb2c-178">**Расширенные параметры:**</span><span class="sxs-lookup"><span data-stu-id="feb2c-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="feb2c-179">Целевое отладка веб-просмотров.</span><span class="sxs-lookup"><span data-stu-id="feb2c-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="feb2c-180">В некоторых приложениях WebView2 можно использовать несколько устройств управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-180">In some WebView2 apps, you may use more than one WebView2 control.</span></span> <span data-ttu-id="feb2c-181">Чтобы выбрать управление WebView2 для отладки в этой ситуации, можно использовать целевое отладку webview2</span><span class="sxs-lookup"><span data-stu-id="feb2c-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="feb2c-182">Откройте `launch.json` и выполните следующие действия, чтобы использовать целевое отладка веб-просмотров.</span><span class="sxs-lookup"><span data-stu-id="feb2c-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="feb2c-183">Подтверди, `useWebview` что задан параметр `true` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="feb2c-184">Добавьте `urlFilter` параметр.</span><span class="sxs-lookup"><span data-stu-id="feb2c-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="feb2c-185">При переходе управления WebView2 на URL-адрес значение параметра используется для сравнения строк, которые `urlFilter` отображаются в URL-адресе.</span><span class="sxs-lookup"><span data-stu-id="feb2c-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="feb2c-186">При отладе приложения может потребоваться пройти код с самого начала процесса отрисовки.</span><span class="sxs-lookup"><span data-stu-id="feb2c-186">When debugging your app, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="feb2c-187">Если вы отрисовываю веб-страницы на сайтах и у вас нет доступа к исходным кодам, вы можете использовать этот параметр, так как веб-страницы игнорируют неузнаваемые `?=value`  параметры.</span><span class="sxs-lookup"><span data-stu-id="feb2c-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="feb2c-188">После первого совпадения в URL-адресе отладка прекращается.</span><span class="sxs-lookup"><span data-stu-id="feb2c-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="feb2c-189">Нельзя одновременно отламыть два управления WebView2, так как порт CDP используется всеми средствами управления WebView2 и использует один номер порта.</span><span class="sxs-lookup"><span data-stu-id="feb2c-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="feb2c-190">Отлачив процессы запуска</span><span class="sxs-lookup"><span data-stu-id="feb2c-190">Debug running processes</span></span>  
    
    <span data-ttu-id="feb2c-191">Возможно, потребуется прикрепить отладка к запущенным процессам WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="feb2c-192">Чтобы сделать это, в `launch.json` , обновить `request` параметр `attach` .</span><span class="sxs-lookup"><span data-stu-id="feb2c-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="feb2c-193">Чтобы разрешить отладку управления WebView2, необходимо открыть порт CDP.</span><span class="sxs-lookup"><span data-stu-id="feb2c-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="feb2c-194">Код должен быть создан для того, чтобы перед запуском отладки только один контроль WebView2 открыл порт Протокола разработчика Chrome (CDP).</span><span class="sxs-lookup"><span data-stu-id="feb2c-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="feb2c-195">Параметры отслеживания отлаговок</span><span class="sxs-lookup"><span data-stu-id="feb2c-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="feb2c-196">Добавьте параметр `trace` в launch.js, чтобы включить трассировку отлаговок.</span><span class="sxs-lookup"><span data-stu-id="feb2c-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="feb2c-197">Добавьте `trace` параметр.</span><span class="sxs-lookup"><span data-stu-id="feb2c-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text=" Сохранение вывода отлаговки в файл журнала." lightbox="./media/tracelog.png":::
                 <span data-ttu-id="feb2c-199">Сохранение вывода отлаговки в файл журнала</span><span class="sxs-lookup"><span data-stu-id="feb2c-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Многословный вывод" lightbox="./media/verbose.png":::
                 <span data-ttu-id="feb2c-201">Visual Studio отламывка кода с включенной многословной трассировой</span><span class="sxs-lookup"><span data-stu-id="feb2c-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="feb2c-202">Отламывка надстроек Office.</span><span class="sxs-lookup"><span data-stu-id="feb2c-202">Debug Office Add-ins.</span></span>  
    
    <span data-ttu-id="feb2c-203">Если вы отладка надстроек Office, откройте исходный код надстройки в отдельном экземпляре Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="feb2c-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="feb2c-204">Откройте launch.jsв приложении WebView2 и добавьте следующий фрагмент кода, чтобы прикрепить отладка к надстройки Office.</span><span class="sxs-lookup"><span data-stu-id="feb2c-204">Open launch.json in your WebView2 app and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="feb2c-205">Устранение неполадок отладки</span><span class="sxs-lookup"><span data-stu-id="feb2c-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="feb2c-206">При использовании отладки можно столкнуться со следующими сценариями.</span><span class="sxs-lookup"><span data-stu-id="feb2c-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="feb2c-207">Отладка не останавливается на точке разрыва, и у вас есть отладка вывода.</span><span class="sxs-lookup"><span data-stu-id="feb2c-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="feb2c-208">Чтобы решить проблему, подтвердим, что файл с точкой разрыва — это тот же файл, который используется с помощью управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="feb2c-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="feb2c-209">Отладка не выполняет сопоставление исходных путей.</span><span class="sxs-lookup"><span data-stu-id="feb2c-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="feb2c-210">Вы не можете прикрепиться к запущенным процессам, и вы получите ошибку времени.</span><span class="sxs-lookup"><span data-stu-id="feb2c-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="feb2c-211">Чтобы решить проблему, подтвердим, что управление WebView2 открыло порт CDP.</span><span class="sxs-lookup"><span data-stu-id="feb2c-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="feb2c-212"> `additionalBrowserArguments` Убедитесь, что значение в реестре правильное или правильные параметры.</span><span class="sxs-lookup"><span data-stu-id="feb2c-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="feb2c-213">Дополнительные сведения перейдите в [дополнительныеBrowserArguments для dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] и [дополнительныеBrowserArguments для Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="feb2c-213">For more information, navigate to [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  

## <a name="see-also"></a><span data-ttu-id="feb2c-214">См. также</span><span class="sxs-lookup"><span data-stu-id="feb2c-214">See also</span></span>  

*   <span data-ttu-id="feb2c-215">Чтобы начать работу с webView2, перейдите к руководствам по началу [webView2.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="feb2c-215">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="feb2c-216">Для полного примера возможностей WebView2 перейдите к [репо WebView2Samples][GithubMicrosoftedgeWebview2samples] в GitHub.</span><span class="sxs-lookup"><span data-stu-id="feb2c-216">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="feb2c-217">Дополнительные сведения об API WebView2 перейдите по ссылке [API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="feb2c-217">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="feb2c-218">Дополнительные сведения о WebView2 перейдите в [webView2 Resources.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="feb2c-218">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="feb2c-219">Контакт с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="feb2c-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "CoreWebView2EnvironmentOptions.AdditionalBrowserArguments Property (Microsoft.Web.WebView2.Core) | Документы Майкрософт"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Документы Майкрософт"  
[Webview2ApiReference]: ../webview2-api-reference.md "Ссылка на API API Microsoft Edge WebView2 | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Примеры WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
