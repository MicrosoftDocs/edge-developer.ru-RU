---
description: Использование элементов для Microsoft Edge (Chromium) из Visual Studio Кода
title: Элементы для Microsoft Edge (Chromium) из Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, vs code, visual studio code, elements
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398457"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="73658-104">Microsoft Edge DevTools для расширения Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="73658-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="73658-105">Использование</span><span class="sxs-lookup"><span data-stu-id="73658-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="73658-106">это расширение для доступа в Microsoft Edge DevTools внутри [Microsoft Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="73658-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="73658-107">У вас есть доступ к **средствам Elements** и **Network** в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="73658-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="73658-108">Вы можете либо запустить, либо прикрепить к экземпляру Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="73658-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="73658-109">После подключения вы можете отобразить структуру HTML-кодов, изменить макет, устранить проблемы с укладкой и проверить сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="73658-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="73658-110">Средство Elements</span><span class="sxs-lookup"><span data-stu-id="73658-110">Elements tool</span></span>  

<span data-ttu-id="73658-111">По умолчанию расширение запускает экземпляр браузера в уникальном \*\*\*\* окне и предоставляет функциональность Элементов Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="73658-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools для Visual Studio кода с полным окном браузера" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="73658-113">Microsoft Edge DevTools для Visual Studio кода с полным окном браузера</span><span class="sxs-lookup"><span data-stu-id="73658-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="73658-114">В параметрах расширения можно включить дополнительные функциональные возможности, такие как **Режим без головы и** **сеть.**</span><span class="sxs-lookup"><span data-stu-id="73658-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Включение (или отключение) безголовых режимов и проверка сети в параметрах расширения" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="73658-116">Включение режима \(или отключения\) безголовых и сетевой проверки в параметрах расширения</span><span class="sxs-lookup"><span data-stu-id="73658-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="73658-117">Режим без головы</span><span class="sxs-lookup"><span data-stu-id="73658-117">Headless Mode</span></span>  

<span data-ttu-id="73658-118">В безголевом режиме это расширение не запускает полный экземпляр браузера для отлаживания.</span><span class="sxs-lookup"><span data-stu-id="73658-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="73658-119">Он запускает экземпляр в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="73658-119">It runs an instance in the background.</span></span>  <span data-ttu-id="73658-120">Возможно, вам придется оставаться в редакторе и взаимодействовать со встроенным браузером.</span><span class="sxs-lookup"><span data-stu-id="73658-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="73658-121">Дополнительный значок браузера не отображается в панели задач.</span><span class="sxs-lookup"><span data-stu-id="73658-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools для Visual Studio кода с безголовым управлением" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="73658-123">Microsoft Edge DevTools для Visual Studio кода с безголовым браузером</span><span class="sxs-lookup"><span data-stu-id="73658-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="73658-124">На macOS в качестве предпочтительного режима следует включить режим без головы.</span><span class="sxs-lookup"><span data-stu-id="73658-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="73658-125">Использование безголкового режима должно решить проблему, в которой, если окно не видно, окно браузера сообщает, что это `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="73658-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="73658-126">Средство "Сеть"</span><span class="sxs-lookup"><span data-stu-id="73658-126">Network tool</span></span>  

<span data-ttu-id="73658-127">Если вы также хотите проверить сетевой трафик приложения, откройте параметры и включите вкладку **Network.**</span><span class="sxs-lookup"><span data-stu-id="73658-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Проверка сети в Microsoft Edge DevTools для Visual Studio code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="73658-129">Проверка сети в Microsoft Edge DevTools для Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="73658-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="73658-130">Запуск Microsoft Edge from the extension</span><span class="sxs-lookup"><span data-stu-id="73658-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="73658-131">Перейдите к microsoft Edge Tools в **панели действий.**</span><span class="sxs-lookup"><span data-stu-id="73658-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="73658-132">Рядом с тем, где написано **Microsoft Edge Tools: Targets,** есть знак плюс, который открывает браузер для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="73658-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="73658-133">Если вы выбираете параметр **about:blank,** необходимо перейти к веб-приложению в браузере, чтобы оно появлялось в панели **Elements** в Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="73658-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="73658-134">Запуск Microsoft Edge из представления отлаговка</span><span class="sxs-lookup"><span data-stu-id="73658-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="73658-135">Если вы привыкли использовать представление debug в Visual Studio коде, в него можно получить доступ к Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="73658-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="73658-136">В Visual Studio коде перейдите к представлению Debug</span><span class="sxs-lookup"><span data-stu-id="73658-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="73658-137">Выберите `Ctrl` + `Shift` + `D` в Windows/Linux \( `Command` + `Shift` + `D` на macOS\).</span><span class="sxs-lookup"><span data-stu-id="73658-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="73658-138">Если в коде Visual Studio нет конфигураций, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="73658-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="73658-139">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="73658-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="73658-140">Выберите **кнопку Play** \(green\) .</span><span class="sxs-lookup"><span data-stu-id="73658-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="73658-141">В отсеве выберите **Edge** в отсеве.</span><span class="sxs-lookup"><span data-stu-id="73658-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="73658-142">Должен `launch.json` отображаться файл, содержащий следующую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="73658-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="73658-143">После загрузки правильной конфигурации выполните следующее действие.</span><span class="sxs-lookup"><span data-stu-id="73658-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="73658-144">Чтобы запустить **средство Elements** из Visual Studio Code, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="73658-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="73658-145">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="73658-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="73658-146">Выберите **кнопку Play** \(green\) .</span><span class="sxs-lookup"><span data-stu-id="73658-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="73658-147">Теперь вы можете сделать следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73658-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="73658-148">Доступ к скринкасту браузера.</span><span class="sxs-lookup"><span data-stu-id="73658-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="73658-149">Проверьте dom и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="73658-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="73658-150">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73658-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="73658-151">Чтобы открыть браузер и прикрепить экземпляр к Visual Studio коду, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73658-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="73658-152">Чтобы открыть экземпляр Microsoft Edge \(Chromium\), скопируйте и запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="73658-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="73658-153">После запуска экземпляра скопируйте и вклейте в файл следующий фрагмент `launch.json` кода.</span><span class="sxs-lookup"><span data-stu-id="73658-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="73658-154">В Visual Studio коде откройте выпадаемое меню **Debugger** и выберите Присоединение к Microsoft Edge и **откройте средства разработчика.**</span><span class="sxs-lookup"><span data-stu-id="73658-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="73658-155">Чтобы запустить **средство Elements** из Visual Studio Code, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="73658-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="73658-156">Выберите `F5` .</span><span class="sxs-lookup"><span data-stu-id="73658-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="73658-157">Выберите **кнопку Play** \(green\) .</span><span class="sxs-lookup"><span data-stu-id="73658-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="73658-158">Теперь вы можете сделать следующие действия.</span><span class="sxs-lookup"><span data-stu-id="73658-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="73658-159">Доступ к скринкасту браузера.</span><span class="sxs-lookup"><span data-stu-id="73658-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="73658-160">Проверьте dom и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="73658-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="73658-161">Контакт с командой microsoft Edge DevTools для Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="73658-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="73658-162">Отправьте свои [отзывы, подав жалобу][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] на репозитарий [GitHub][GithubMicrosoftVscodeEdgeDevtools] о расширении.</span><span class="sxs-lookup"><span data-stu-id="73658-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="73658-163">Если вы хотите помочь сделать</span><span class="sxs-lookup"><span data-stu-id="73658-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="73658-164">это расширение лучше, ваши вклады приветствуются.</span><span class="sxs-lookup"><span data-stu-id="73658-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="73658-165">Найдите все необходимое для начала в репозитарии [GitHub][GithubMicrosoftVscodeEdgeDevtools] расширения.</span><span class="sxs-lookup"><span data-stu-id="73658-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Код"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio Код"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая проблема — microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода"  
