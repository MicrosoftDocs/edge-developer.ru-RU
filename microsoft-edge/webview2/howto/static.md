---
description: Узнайте, как статически связать библиотеку загрузщика WebView2.
title: Как статически связать библиотеку загрузчик WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, приложения win32, win32, edge, ICoreWebView2, ICoreWebView2Host, элемент управления браузером, edge html
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230931"
---
# <span data-ttu-id="10708-104">Статически связывать библиотеку загрузок WebView2</span><span class="sxs-lookup"><span data-stu-id="10708-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="10708-105">Возможно, вы захотите распространять приложение с одним исполняемым файлом, а не с пакетом из множества файлов.</span><span class="sxs-lookup"><span data-stu-id="10708-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="10708-106">Чтобы создать один исполняемый файл или уменьшить размер пакета, необходимо статически связать файлы WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="10708-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="10708-107">SDK WebView2 содержит файл загона `WebView2Loader.dll` и `IDL` файл.</span><span class="sxs-lookup"><span data-stu-id="10708-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="10708-108">— это небольшой компонент, который помогает приложениям находить на устройстве компоненты времени работы WebView2 или не стабильные каналы Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="10708-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="10708-109">Для приложений, которые не хотят погрузки, `WebView2Loader.dll` выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="10708-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="10708-110">Откройте файл `.vcxproj` проекта приложения в текстовом редакторе, например Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="10708-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="10708-111">Файл проекта может быть скрытым, то есть он не отображается `.vcproj` в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="10708-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="10708-112">Используйте командную строку для поиска скрытых файлов.</span><span class="sxs-lookup"><span data-stu-id="10708-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="10708-113">Найдите раздел в коде, где вы включаете файлы целевого пакета NuGet WebView2.</span><span class="sxs-lookup"><span data-stu-id="10708-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="10708-114">Расположение в коде выделено на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="10708-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Фрагмент кода project Files" lightbox="./media/inserthere.png":::
       <span data-ttu-id="10708-116">Фрагмент кода project Files</span><span class="sxs-lookup"><span data-stu-id="10708-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="10708-117">Скопируйте следующий фрагмент кода и включаем его там, `Microsoft.Web.WebView2.targets` где он включен.</span><span class="sxs-lookup"><span data-stu-id="10708-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Вставленный фрагмент кода" lightbox="./media/staticlib.png":::
       <span data-ttu-id="10708-119">Вставленный фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="10708-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10708-120">Изменение дополнительных зависимостей конфигурации сборки для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="10708-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="10708-121">Для начала найдите все `<AdditionalDependencies>` теги.</span><span class="sxs-lookup"><span data-stu-id="10708-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="10708-122">Для каждой из них `version.lib` добавьте дополнительную зависимость для каждой конфигурации сборки в `.vcxproj` файле.</span><span class="sxs-lookup"><span data-stu-id="10708-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Добавление version.lib в ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       <span data-ttu-id="10708-124">Добавление `version.lib` в</span><span class="sxs-lookup"><span data-stu-id="10708-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="10708-125">Команда WebView2 стремится автоматизировать добавление дополнительной зависимости в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="10708-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="10708-126">Скомпилировать и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="10708-126">Compile and run your app.</span></span>

### <span data-ttu-id="10708-127">Знакомство с командой WebView2</span><span class="sxs-lookup"><span data-stu-id="10708-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="10708-128">См. также</span><span class="sxs-lookup"><span data-stu-id="10708-128">See also</span></span>  

*   <span data-ttu-id="10708-129">Чтобы начать работу с WebView2, перейдите к руководствам по началу работы [WebView2.][Webview2MainGettingStarted]</span><span class="sxs-lookup"><span data-stu-id="10708-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="10708-130">Чтобы получить полный пример возможностей WebView2, перейдите к [webView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="10708-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="10708-131">Дополнительные сведения об API WebView2 можно найти в справочнике [по API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="10708-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="10708-132">Для получения дополнительных сведений о WebView2 перейдите к [ресурсам WebView2.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="10708-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Средства разработчика Microsoft Edge (Chromium) | Документы Майкрософт"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge WebView2 API Reference | Документы Майкрософт"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Начало работы — введение в Microsoft Edge WebView2 (предварительная версия) | Документы Майкрософт"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Обратная связь WebView — MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности - Отладатель JavaScript для Visual Studio Code — microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Приложения Microsoft Edge (Chromium) WebView — Visual Studio Code — отладка для Microsoft Edge — microsoft/vscode-edge-debug2 | GitHub"  
