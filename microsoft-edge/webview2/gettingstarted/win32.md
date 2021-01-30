---
description: Руководство по началу работы с WebView2 для приложений Win32
title: Начало работы с WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, элемент управления браузером, edge html
ms.openlocfilehash: 19bc0c5600ebd072ad9a6aa61d2a965e999865ce
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306161"
---
# <span data-ttu-id="64924-104">Начало работы с WebView2</span><span class="sxs-lookup"><span data-stu-id="64924-104">Getting started with WebView2</span></span>  

<span data-ttu-id="64924-105">В этой статье вы узнаете, как создать свое первое приложение WebView2, а также основные функции [WebView2.][MicrosoftDeveloperMicrosoftEdgeWebview2]</span><span class="sxs-lookup"><span data-stu-id="64924-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="64924-106">Дополнительные сведения об отдельных API WebView2 можно найти в справочнике [по API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="64924-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="64924-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="64924-107">Prerequisites</span></span>  

<span data-ttu-id="64924-108">Перед тем как при этом добиться этого, убедитесь, что вы установили следующий список необходимых условий.</span><span class="sxs-lookup"><span data-stu-id="64924-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="64924-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="64924-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="64924-110">Команда WebView рекомендует использовать канал Canary, а минимальная требуемая версия — 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="64924-110">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="64924-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 или более поздней с установленной поддержкой C++.</span><span class="sxs-lookup"><span data-stu-id="64924-111">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <span data-ttu-id="64924-112">Шаг 1. Создание одноокнего приложения</span><span class="sxs-lookup"><span data-stu-id="64924-112">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="64924-113">Начните с базового проекта настольного компьютера, который содержит одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="64924-113">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="64924-114">Чтобы лучше сосредоточиться на этом пономерии, используйте измененный пример кода из [walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span><span class="sxs-lookup"><span data-stu-id="64924-114">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="64924-115">Чтобы скачать измененный пример и начать работу, перейдите к [примеру WebView2.][GithubMicrosoftedgeWebview2samplesGettingStartedGuide]</span><span class="sxs-lookup"><span data-stu-id="64924-115">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="64924-116">В Visual Studio откройте `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="64924-116">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="64924-117">Если вы используете более старую версию Visual Studio, наведите курсор на проект **WebView2GettingStarted,** откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите **"Свойства".**</span><span class="sxs-lookup"><span data-stu-id="64924-117">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="64924-118">В **области "Общие**свойства конфигурации" измените версию Windows SDK и инструменты платформы, чтобы использовать доступный вам Visual Studio  >  \*\*\*\* Win10 SDK. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="64924-118">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Версия средства" lightbox="../media/tool-version.png":::
   <span data-ttu-id="64924-120">Версия средства</span><span class="sxs-lookup"><span data-stu-id="64924-120">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="64924-121">Visual Studio могут отображаться ошибки, так как в проекте отсутствует файл загона WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-121">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="64924-122">Ошибки должны быть исправлены [после шага 2.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="64924-122">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <span data-ttu-id="64924-123">Шаг 2. Установка SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="64924-123">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="64924-124">Добавьте в проект SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-124">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="64924-125">Установка win32 SDK с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="64924-125">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="64924-126">Наведите курсор на проект, откройте контекстное меню \(щелкните правой кнопкой мыши\) и выберите пункт **"Управление пакетами NuGet".**</span><span class="sxs-lookup"><span data-stu-id="64924-126">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Управление пакетами NuGet" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="64924-128">Управление пакетами NuGet</span><span class="sxs-lookup"><span data-stu-id="64924-128">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="64924-129">Установите библиотеку реализации Windows.</span><span class="sxs-lookup"><span data-stu-id="64924-129">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="64924-130">В панели поиска введите > `Microsoft.Windows.ImplementationLibrary` **Microsoft.Windows.ImplementationLibrary.**</span><span class="sxs-lookup"><span data-stu-id="64924-130">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="64924-131">В правом окне выберите **"Установить".**</span><span class="sxs-lookup"><span data-stu-id="64924-131">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="64924-132">NuGet скачивает библиотеку на компьютер.</span><span class="sxs-lookup"><span data-stu-id="64924-132">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="64924-133">Библиотека [реализации Windows][GithubMicrosoftWilMain] и библиотека шаблонов [C++][CppCxWrlTemplateLibraryVS2019] для времени выполнения Windows являются необязательными и упрощают работу с COM в этом примере.</span><span class="sxs-lookup"><span data-stu-id="64924-133">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Библиотека реализации Windows" lightbox="../media/wil.png":::
           <span data-ttu-id="64924-135">Библиотека реализации Windows</span><span class="sxs-lookup"><span data-stu-id="64924-135">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="64924-136">Установите SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-136">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="64924-137">В панели поиска введите > `Microsoft.Web.WebView2` **Microsoft.Web.WebView2.**</span><span class="sxs-lookup"><span data-stu-id="64924-137">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="64924-138">В правом окне выберите **"Установить".**</span><span class="sxs-lookup"><span data-stu-id="64924-138">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="64924-139">NuGet скачивает SDK на компьютер.</span><span class="sxs-lookup"><span data-stu-id="64924-139">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet диспетчер пакетов" lightbox="../media/nuget.png":::
           <span data-ttu-id="64924-141">NuGet диспетчер пакетов</span><span class="sxs-lookup"><span data-stu-id="64924-141">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="64924-142">Добавьте в проект загон WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-142">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="64924-143">В файле скопируйте следующий фрагмент кода и в `HelloWebView.cpp` paste его после последней `#include` строки.</span><span class="sxs-lookup"><span data-stu-id="64924-143">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="64924-144">Раздел "Включить" должен выглядеть примерно так, как в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="64924-144">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="64924-145">Готово к использованию и построению с использованием API WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-145">Ready to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="64924-146">Создание пустого примера приложения</span><span class="sxs-lookup"><span data-stu-id="64924-146">Build your empty sample app</span></span>  

<span data-ttu-id="64924-147">Чтобы создать и запустить пример приложения, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="64924-147">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="64924-148">Приложение отображает пустое окно.</span><span class="sxs-lookup"><span data-stu-id="64924-148">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Пустое приложение" lightbox="../media/empty-app.png":::
   <span data-ttu-id="64924-150">Пустое приложение</span><span class="sxs-lookup"><span data-stu-id="64924-150">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="64924-151">Шаг 3. Создание одного веб-приложения в родительском окне</span><span class="sxs-lookup"><span data-stu-id="64924-151">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="64924-152">Добавьте WebView в главное окно.</span><span class="sxs-lookup"><span data-stu-id="64924-152">Add a WebView to the main window.</span></span>  

 <span data-ttu-id="64924-153">Используйте этот метод, чтобы настроить среду и найти браузер Microsoft Edge \(Chromium\), в которой установлено `CreateCoreWebView2Environment` управление.</span><span class="sxs-lookup"><span data-stu-id="64924-153">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="64924-154">Этот метод также можно использовать, если нужно указать расположение браузера, папку пользователя, флаги браузера и так далее, а не параметр `CreateCoreWebView2EnvironmentWithOptions` по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64924-154">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="64924-155">По завершении работы метода запустите метод в callback и запустите метод, чтобы получить `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` связанный WebView.</span><span class="sxs-lookup"><span data-stu-id="64924-155">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="64924-156">В вызываемом окне установите еще несколько параметров, избавите webView на 100 % от родительского окна и перейдите к Bing.</span><span class="sxs-lookup"><span data-stu-id="64924-156">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="64924-157">Скопируйте следующий фрагмент кода и в конце комментария и `HelloWebView.cpp` `// <-- WebView2 sample code starts here -->` перед `// <-- WebView2 sample code ends here -->` комментарием.</span><span class="sxs-lookup"><span data-stu-id="64924-157">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <span data-ttu-id="64924-158">Создание примера приложения Bing</span><span class="sxs-lookup"><span data-stu-id="64924-158">Build your Bing sample app</span></span>  

<span data-ttu-id="64924-159">Чтобы выполнить сборку и запустить приложение, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="64924-159">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="64924-160">Теперь у вас есть окно WebView со страницей Bing.</span><span class="sxs-lookup"><span data-stu-id="64924-160">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Окно Bing" lightbox="../media/bing-window.png":::
   <span data-ttu-id="64924-162">Окно Bing</span><span class="sxs-lookup"><span data-stu-id="64924-162">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="64924-163">Шаг 4. События навигации</span><span class="sxs-lookup"><span data-stu-id="64924-163">Step 4 - Navigation events</span></span>  

<span data-ttu-id="64924-164">Команда WebView уже освещала переход на URL-адрес с помощью `ICoreWebView2::Navigate` метода на последнем шаге.</span><span class="sxs-lookup"><span data-stu-id="64924-164">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="64924-165">Во время навигации WebView сожмет последовательность событий, которые может прослушивать хост.</span><span class="sxs-lookup"><span data-stu-id="64924-165">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="64924-166">Для получения дополнительных сведений перейдите к [событиям навигации.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="64924-166">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="64924-168">События навигации</span><span class="sxs-lookup"><span data-stu-id="64924-168">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="64924-169">В случае ошибок может произойти одно или несколько из следующих событий в зависимости от того, продолжается ли навигация до веб-страницы ошибки.</span><span class="sxs-lookup"><span data-stu-id="64924-169">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> <span data-ttu-id="64924-170">Если происходит перенаправление HTTP, строка имеет `NavigationStarting` несколько событий.</span><span class="sxs-lookup"><span data-stu-id="64924-170">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="64924-171">В качестве примера использования событий зарегистрируйте обработок для события, чтобы отменить все запросы, не `NavigationStarting` относя такие как https.</span><span class="sxs-lookup"><span data-stu-id="64924-171">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="64924-172">Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="64924-172">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

<span data-ttu-id="64924-173">Теперь приложение не переходит на сайты без https.</span><span class="sxs-lookup"><span data-stu-id="64924-173">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="64924-174">Аналогичный механизм можно использовать для выполнения других задач, например ограничения навигации в пределах собственного домена.</span><span class="sxs-lookup"><span data-stu-id="64924-174">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="64924-175">Шаг 5. Сценарии</span><span class="sxs-lookup"><span data-stu-id="64924-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="64924-176">Вы можете использовать хост-приложения, чтобы ввести код JavaScript в элементы управления WebView2 во время работы.</span><span class="sxs-lookup"><span data-stu-id="64924-176">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="64924-177">Вы можете на задачу WebView запустить произвольный JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="64924-177">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="64924-178">Введенный JavaScript применяется ко всем новым документам верхнего уровня и всем потомков, пока JavaScript не будет удален.</span><span class="sxs-lookup"><span data-stu-id="64924-178">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="64924-179">Введенный JavaScript работает с определенными сроками.</span><span class="sxs-lookup"><span data-stu-id="64924-179">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="64924-180">Запустите его после создания глобального объекта.</span><span class="sxs-lookup"><span data-stu-id="64924-180">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="64924-181">Запустите его перед запуском любого другого сценария, включенного в HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="64924-181">Run it before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="64924-182">Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="64924-182">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

<span data-ttu-id="64924-183">Теперь WebView всегда должен зависать объект и `Object` возвращать документ страницы один раз.</span><span class="sxs-lookup"><span data-stu-id="64924-183">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="64924-184">API-коды для впрыска скриптов \(и некоторые другие API WebView2\) являются асинхронными, следует использовать функции вызова, если код должен запускаться в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="64924-184">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="64924-185">Шаг 6. Взаимодействие между хост-контентом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="64924-185">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="64924-186">С помощью этого метода хост и веб-контент также могут взаимодействовать друг с `postMessage` другом.</span><span class="sxs-lookup"><span data-stu-id="64924-186">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="64924-187">Веб-содержимое, запущенное в WebView, может размещаться на хост-сервере с помощью метода, а сообщение обрабатывается любым зарегистрированным обработом событий на `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` хост-сервере.</span><span class="sxs-lookup"><span data-stu-id="64924-187">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="64924-188">Аналогичным образом, хост может отправить сообщение веб-содержимому через или метод, который будет перехвачен обработчиками, добавленными `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` из `window.chrome.webview.addEventListener` прослушивателей.</span><span class="sxs-lookup"><span data-stu-id="64924-188">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="64924-189">Механизм связи позволяет веб-содержимому использовать свои возможности, передавая сообщения с запросом на запуск нативных API на хост-сервере.</span><span class="sxs-lookup"><span data-stu-id="64924-189">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="64924-190">В качестве примера для понимания механизма при попытке вывода URL-адреса документа в WebView происходят следующие действия.</span><span class="sxs-lookup"><span data-stu-id="64924-190">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="64924-191">Хост регистрирует обработок для возврата полученного сообщения в веб-содержимое</span><span class="sxs-lookup"><span data-stu-id="64924-191">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="64924-192">Хост внедряет сценарий в веб-содержимое, которое регистрирует обработок для печати сообщения с хоста</span><span class="sxs-lookup"><span data-stu-id="64924-192">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="64924-193">Хост внедряет сценарий в веб-содержимое, которое публикует URL-адрес на хост-сайте.</span><span class="sxs-lookup"><span data-stu-id="64924-193">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="64924-194">Запускается обработок хоста, который возвращает сообщение \(URL\) в веб-содержимое</span><span class="sxs-lookup"><span data-stu-id="64924-194">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="64924-195">Запускается обработок веб-содержимого, который печатает сообщение с хоста \(URL\)</span><span class="sxs-lookup"><span data-stu-id="64924-195">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="64924-196">Скопируйте следующий фрагмент кода и в paste в `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="64924-196">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <span data-ttu-id="64924-197">Создание примера приложения с URL-адресом для отображения</span><span class="sxs-lookup"><span data-stu-id="64924-197">Build your display URL sample app</span></span>  

<span data-ttu-id="64924-198">Чтобы выполнить сборку и запустить приложение, выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="64924-198">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="64924-199">URL-адрес отображается во всплывающее окно перед переходом на веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="64924-199">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Url-адрес отображения" lightbox="../media/show-url.png":::
   <span data-ttu-id="64924-201">Url-адрес отображения</span><span class="sxs-lookup"><span data-stu-id="64924-201">Display url</span></span>  
:::image-end:::  

<span data-ttu-id="64924-202">Поздравляем, вы создали свое первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="64924-202">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="64924-203">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="64924-203">Next steps</span></span>  

<span data-ttu-id="64924-204">Многие функции WebView2 не освещаются в этой статье. В следующем разделе предоставляется больше ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64924-204">Many of the WebView2 functionalities are not covered on this article, the following section provides more resources.</span></span>  

### <span data-ttu-id="64924-205">См. также</span><span class="sxs-lookup"><span data-stu-id="64924-205">See also</span></span>  

*   <span data-ttu-id="64924-206">Полный пример возможностей WebView2 можно найти в примере [API WebView2.][GithubMicrosoftedgeWebview2samplesApisample]</span><span class="sxs-lookup"><span data-stu-id="64924-206">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="64924-207">Для примера приложения, построенного с помощью WebView2, перейдите к [WebView2Browser.][GithubMicrosoftedgeWebview2browser]</span><span class="sxs-lookup"><span data-stu-id="64924-207">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="64924-208">Подробные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="64924-208">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <span data-ttu-id="64924-209">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="64924-209">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Разработчик Microsoft Edge"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Справочник по WebView2 Win32 C++ | Документы Майкрософт"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Майкрософт"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Библиотека шаблонов C++ (WRL) в | Документы Майкрософт"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Документы Майкрософт"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser — MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Пример API WebView2 — MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2 Samples — MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Библиотеки реализации Windows (WIL) — microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2"  
