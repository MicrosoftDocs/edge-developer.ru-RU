---
description: Microsoft Edge (Chromium) и Visual Studio
title: VisualStudio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, vs, visual studio, debugger
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387276"
---
# <a name="visual-studio"></a><span data-ttu-id="3c9af-104">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="3c9af-104">Visual Studio</span></span>  

<span data-ttu-id="3c9af-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] — это интегрированная среда разработки \(IDE\).</span><span class="sxs-lookup"><span data-stu-id="3c9af-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] is an integrated development environment \(IDE\).</span></span>   <span data-ttu-id="3c9af-106">Используйте его для редактирования, отлаговки, сборки и публикации веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="3c9af-106">Use it to edit, debug, build, and publish your web apps.</span></span>  <span data-ttu-id="3c9af-107">Это программа с богатыми функциями, которая может использоваться для многих аспектов веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="3c9af-107">It is a feature-rich program that may be used for many aspects of your web development.</span></span>  <span data-ttu-id="3c9af-108">Помимо стандартного редактора и отладки, которые предоставляют большинство IDEs, Visual Studio включает следующие функции, облегчаю процесс разработки.</span><span class="sxs-lookup"><span data-stu-id="3c9af-108">Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes the following features to ease your development process.</span></span>  

*   <span data-ttu-id="3c9af-109">компиляторы</span><span class="sxs-lookup"><span data-stu-id="3c9af-109">compilers</span></span>  
*   <span data-ttu-id="3c9af-110">Средства завершения кода</span><span class="sxs-lookup"><span data-stu-id="3c9af-110">code completion tools</span></span>  
*   <span data-ttu-id="3c9af-111">графические дизайнеры</span><span class="sxs-lookup"><span data-stu-id="3c9af-111">graphical designers</span></span>  
*   <span data-ttu-id="3c9af-112">многие другие</span><span class="sxs-lookup"><span data-stu-id="3c9af-112">many more</span></span>  
    
<span data-ttu-id="3c9af-113">Если вы еще не используете Visual Studio, перейдите по ссылке [Скачать Visual Studio,][MicrosoftVisualstudioDownloads] чтобы скачать его.</span><span class="sxs-lookup"><span data-stu-id="3c9af-113">If you are not already using Visual Studio, navigate to [Download Visual Studio][MicrosoftVisualstudioDownloads] to download it.</span></span>  

<span data-ttu-id="3c9af-114">В настоящее время Visual Studio 2019 г. поддерживает отладку JavaScript в Microsoft Edge для ASP.NET Framework и ASP.NET Core приложений.</span><span class="sxs-lookup"><span data-stu-id="3c9af-114">Currently, Visual Studio 2019 supports debugging JavaScript in Microsoft Edge for your ASP.NET Framework and ASP.NET Core apps.</span></span>  <span data-ttu-id="3c9af-115">Выполните следующие действия, чтобы использовать Visual Studio для отлаговки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c9af-115">Complete the following steps to use Visual Studio to debug Microsoft Edge.</span></span>  

## <a name="launch-microsoft-edge"></a><span data-ttu-id="3c9af-116">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9af-116">Launch Microsoft Edge</span></span>  

<span data-ttu-id="3c9af-117">Visual Studio завершает следующий рабочий процесс с помощью одной кнопки.</span><span class="sxs-lookup"><span data-stu-id="3c9af-117">Visual Studio completes the following workflow using a single button.</span></span>  

1.  <span data-ttu-id="3c9af-118">Создает приложение ASP.NET ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="3c9af-118">Builds your ASP.NET and ASP.NET Core app.</span></span>  
1.  <span data-ttu-id="3c9af-119">Запускает веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="3c9af-119">Starts your web server.</span></span>  
1.  <span data-ttu-id="3c9af-120">Запускает Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c9af-120">Launches Microsoft Edge.</span></span>  
1.  <span data-ttu-id="3c9af-121">Подключает Visual Studio отладка.</span><span class="sxs-lookup"><span data-stu-id="3c9af-121">Connects the Visual Studio debugger.</span></span>  
    
<span data-ttu-id="3c9af-122">Упрощенный рабочий процесс позволяет отламывать JavaScript, который работает в Microsoft Edge непосредственно из вашего IDE.</span><span class="sxs-lookup"><span data-stu-id="3c9af-122">The simplified workflow allows you to debug JavaScript that run in Microsoft Edge directly from your IDE.</span></span>  

### <a name="create-a-new-aspnet-core-web-app"></a><span data-ttu-id="3c9af-123">Создание нового ASP.NET основного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3c9af-123">Create a new ASP.NET Core web app</span></span>  

<span data-ttu-id="3c9af-124">Откройте Visual Studio 2019 г. и **выберите Создание нового проекта.**</span><span class="sxs-lookup"><span data-stu-id="3c9af-124">Open Visual Studio 2019 and choose **Create a new project**.</span></span>  <span data-ttu-id="3c9af-125">На следующем экране выберите ASP.NET **Веб-приложение**  >  **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-125">On the next screen, choose **ASP.NET Core Web app** > **Next**.</span></span>  

:::image type="complex" source="./media/create-new-project.png" alt-text="Создание нового ASP.NET основного веб-приложения" lightbox="./media/create-new-project.png":::
   <span data-ttu-id="3c9af-127">Создание нового ASP.NET основного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3c9af-127">Create a new ASP.NET Core Web app</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-128">**Укайте имя проекта** для нового проекта и выберите **Create**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-128">Provide a **Project name** for your new project and choose **Create**.</span></span>  <span data-ttu-id="3c9af-129">Для целей примера выберитеReact.js\*\* в \*\* качестве шаблона и выберите **Create**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-129">For the purposes of the example, choose **React.js** as the template, and choose **Create**.</span></span>  <span data-ttu-id="3c9af-130">Шаблон **React.js** указывает, как интегрировать React.js с приложением ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="3c9af-130">The **React.js** template specifies how to integrate React.js with an ASP.NET Core app.</span></span>  

### <a name="launch-microsoft-edge-from-visual-studio"></a><span data-ttu-id="3c9af-131">Запуск Microsoft Edge из Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-131">Launch Microsoft Edge from Visual Studio</span></span>  

<span data-ttu-id="3c9af-132">После создания проекта откройте `ClientApp/src/components/Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="3c9af-132">After you create your project, open `ClientApp/src/components/Counter.js`.</span></span>  <span data-ttu-id="3c9af-133">Теперь, чтобы использовать Visual Studio для отламки JavaScript, выберите выпадаемую кнопку рядом с зеленой кнопкой **Play** и **IIS Express.**</span><span class="sxs-lookup"><span data-stu-id="3c9af-133">Now, to use Visual Studio to debug JavaScript, choose the dropdown next to the green **Play** button and **IIS Express**.</span></span>  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="Выпадаемая часть рядом с зеленой кнопкой Play и IIS Express" lightbox="./media/vs-dropdown.png":::
   <span data-ttu-id="3c9af-135">Выпадаемая часть рядом с зеленой кнопкой **Play** и **IIS Express**</span><span class="sxs-lookup"><span data-stu-id="3c9af-135">The dropdown next to the green **Play** button and **IIS Express**</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-136">Выберите **включенную отладку**  >  **скриптов**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-136">Choose **Script Debugging** > **Enabled**.</span></span>  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Включаем отладку скриптов в Visual Studio" lightbox="./media/enable-script-debugging.png":::
   <span data-ttu-id="3c9af-138">Включаем отладку скриптов в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-138">Turn on script debugging in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-139">В одном и том \*\*\*\* же отсеве выберите веб-браузер > предварительного просмотра канала Microsoft Edge, который Visual Studio запускать, например Microsoft Edge Canary, Dev или Beta.</span><span class="sxs-lookup"><span data-stu-id="3c9af-139">In the same dropdown, choose **Web Browser** > the preview channel of Microsoft Edge that you want Visual Studio to launch, such as Microsoft Edge Canary, Dev, or Beta.</span></span>  <span data-ttu-id="3c9af-140">Если вы еще не используете один из каналов предварительного просмотра Microsoft Edge, перейдите к Скачать каналы предварительного просмотра Microsoft [Edge,][MicrosoftedgeinsiderDownload] чтобы скачать один из них.</span><span class="sxs-lookup"><span data-stu-id="3c9af-140">If you are not already using one of the Microsoft Edge preview channels, navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] to download one.</span></span>  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Выберите канал предварительного просмотра Microsoft Edge, который Visual Studio запустить" lightbox="./media/set-web-browser.png":::
   <span data-ttu-id="3c9af-142">Выберите канал предварительного просмотра Microsoft Edge, который Visual Studio запустить</span><span class="sxs-lookup"><span data-stu-id="3c9af-142">Choose the preview channel of Microsoft Edge that you want Visual Studio to launch</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3c9af-143">Если вы выбрали Microsoft Edge \(EdgeHTML\), Visual Studio запускает его вместо Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="3c9af-143">If you choose Microsoft Edge \(EdgeHTML\), Visual Studio launches it instead of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="3c9af-144">Установите один из каналов предварительного просмотра Microsoft Edge или убедитесь, что версия Microsoft [Edge,][MicrosoftedgeinsiderDownload] установленная на вашем компьютере, является Microsoft Edge \(Chromium\) а не Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="3c9af-144">[Install the one of the preview channels of Microsoft Edge][MicrosoftedgeinsiderDownload] or ensure that the version of Microsoft Edge installed on your machine is Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  

<span data-ttu-id="3c9af-145">Теперь, Visual Studio правильно настроена, выберите зеленую кнопку **Play.**</span><span class="sxs-lookup"><span data-stu-id="3c9af-145">Now that Visual Studio is correctly configured, choose the green **Play** button.</span></span>  <span data-ttu-id="3c9af-146">Visual Studio создает приложение, запустите веб-сервер, запустите Microsoft Edge и перейдите в порт или любой `https://localhost:44362/` порт, указанный в `launchSettings.json` .</span><span class="sxs-lookup"><span data-stu-id="3c9af-146">Visual Studio builds your app, start the web server, launch Microsoft Edge, and navigate to `https://localhost:44362/` or whatever port is specified in `launchSettings.json`.</span></span>  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge запускается с Visual Studio" lightbox="./media/edge-launch.png":::
   <span data-ttu-id="3c9af-148">Microsoft Edge запускается с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-148">Microsoft Edge launches from Visual Studio</span></span>  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a><span data-ttu-id="3c9af-149">Отламка JavaScript, запущенная в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9af-149">Debug JavaScript running in Microsoft Edge</span></span>  

<span data-ttu-id="3c9af-150">Переключение на Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c9af-150">Switch back to Visual Studio.</span></span>  <span data-ttu-id="3c9af-151">В `Counter.js` , чтобы установить точку разрыва на строке 13, выберите желоб рядом с строкой.</span><span class="sxs-lookup"><span data-stu-id="3c9af-151">In `Counter.js`, to set a breakpoint on Line 13, choose the gutter next to the line.</span></span>  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Выберите желоб рядом с строкой 13 в Counter.js, чтобы установить точку разрыва в Visual Studio" lightbox="./media/set-breakpoint.png":::
   <span data-ttu-id="3c9af-153">Выберите желоб рядом с строкой 13, чтобы установить точку `Counter.js` разрыва в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-153">Choose the gutter next to Line 13 in `Counter.js` to set a breakpoint in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-154">Теперь переключение на экземпляр Microsoft Edge, который Visual Studio запущен.</span><span class="sxs-lookup"><span data-stu-id="3c9af-154">Now switch back to the instance of Microsoft Edge that Visual Studio launched.</span></span>  <span data-ttu-id="3c9af-155">Выберите на **счетчике** в NavMenu слева от веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="3c9af-155">Choose on **Counter** in the NavMenu on the left of the webpage.</span></span>  <span data-ttu-id="3c9af-156">Теперь выберите **Приращение**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-156">Now choose **Increment**.</span></span>  

:::image type="complex" source="./media/edge-counter.png" alt-text="Страница Счетчик в нашем ASP.NET веб-приложении Core" lightbox="./media/edge-counter.png":::
   <span data-ttu-id="3c9af-158">Страница Счетчик в нашем ASP.NET веб-приложении Core</span><span class="sxs-lookup"><span data-stu-id="3c9af-158">The Counter page in our ASP.NET Core web app</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-159">Отладка JavaScript в Visual Studio попадает в точку разлома, в который вы вписались. `Counter.js`</span><span class="sxs-lookup"><span data-stu-id="3c9af-159">The JavaScript debugger in Visual Studio hits the breakpoint you set in `Counter.js`.</span></span>  <span data-ttu-id="3c9af-160">Visual Studio теперь приостанавливается время запуска JavaScript в Microsoft Edge, и вы можете ступить через строку сценария по очереди.</span><span class="sxs-lookup"><span data-stu-id="3c9af-160">Visual Studio now pauses the runtime of the JavaScript running in Microsoft Edge and you may step through the script line-by-line.</span></span>  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio JavaScript, запущенный в Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   <span data-ttu-id="3c9af-162">Visual Studio JavaScript, запущенный в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9af-162">Visual Studio pauses JavaScript running in Microsoft Edge</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-163">В этом примере была лишь небольшая демонстрация функциональных возможностей, доступных в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c9af-163">The example was just a minor demonstration of the functionality available in Visual Studio.</span></span>  <span data-ttu-id="3c9af-164">Дополнительные сведения о функциональных возможностях Visual Studio 2019 г. перейдите Visual Studio [документации.][VisualStudioWindowsIndex]</span><span class="sxs-lookup"><span data-stu-id="3c9af-164">For more information about the functionality in Visual Studio 2019, navigate to [Visual Studio documentation][VisualStudioWindowsIndex].</span></span>  

## <a name="attach-to-microsoft-edge"></a><span data-ttu-id="3c9af-165">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3c9af-165">Attach to Microsoft Edge</span></span>  

<span data-ttu-id="3c9af-166">Ранее необходимо было запустить Microsoft Edge из Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c9af-166">Previously, you had to launch Microsoft Edge from Visual Studio.</span></span>  <span data-ttu-id="3c9af-167">Теперь вы можете прикрепить отладку Visual Studio к уже запущенной экземпляру Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c9af-167">Now, you are able to attach the Visual Studio debugger to an already running instance of Microsoft Edge.</span></span>  

<span data-ttu-id="3c9af-168">Во-первых, убедитесь, что нет запущенных экземпляров Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c9af-168">First, ensure that there are no running instances of Microsoft Edge.</span></span>  <span data-ttu-id="3c9af-169">Теперь из командной строки запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="3c9af-169">Now, from your command line, run the following command.</span></span>  

```console
start msedge –remote-debugging-port=9222
```  

<span data-ttu-id="3c9af-170">Из Visual Studio откройте меню **Отлаговка** и выберите **Присоединение к процессу** или выберите `Ctrl` + `Alt` + `P` .</span><span class="sxs-lookup"><span data-stu-id="3c9af-170">From Visual Studio, open the **Debug** menu and choose **Attach to Process** or select `Ctrl`+`Alt`+`P`.</span></span>  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Выберите Присоединение к процессу в Visual Studio" lightbox="./media/attach-to-process.png":::
   <span data-ttu-id="3c9af-172">Выберите **Присоединение к процессу** в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-172">Choose **Attach to Process** in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-173">В **диалоговом** окне "Присоединение к процессу" установите тип **подключения** к веб-сайту протокола **chrome devtools (без проверки подлинности).**</span><span class="sxs-lookup"><span data-stu-id="3c9af-173">From the **Attach to Process** dialog, set **Connection type** to **Chrome devtools protocol websocket (no authentication)**.</span></span>  <span data-ttu-id="3c9af-174">В **целевом текстовом ящике Подключения** введите `http://localhost:9222/` и выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="3c9af-174">In the **Connecting target** textbox, type `http://localhost:9222/` and select `Enter`.</span></span>  <span data-ttu-id="3c9af-175">Просмотрите список открытых вкладок, указанных в диалоговом окте Microsoft Edge в диалоговом окте **"Присоединение к процессу".**</span><span class="sxs-lookup"><span data-stu-id="3c9af-175">Review the list of open tabs you have in Microsoft Edge listed out in the **Attach to Process** dialog.</span></span>  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Настройте диалоговое окно Attach to Process в Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   <span data-ttu-id="3c9af-177">Настройте **диалоговое окно Attach to Process** в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-177">Configure the **Attach to Process** dialog in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="3c9af-178">Выберите **Выберите...** > рядом с **JavaScript (Microsoft Edge — Chromium).**</span><span class="sxs-lookup"><span data-stu-id="3c9af-178">Choose **Select...** > the checkbox next to **JavaScript (Microsoft Edge – Chromium)**.</span></span>  <span data-ttu-id="3c9af-179">Чтобы добавить вкладки, перейдите на новые вкладки и закройте \*\*\*\* вкладки и отобразите изменения, отражающиеся в диалоговом окте "Присоединение к процессу", выберите кнопку **"Обновление".**</span><span class="sxs-lookup"><span data-stu-id="3c9af-179">To add tabs, navigate to new tabs, and close tabs and display the changes reflected in the **Attach to Process** dialog, choose the **Refresh** button.</span></span>  <span data-ttu-id="3c9af-180">Выберите вкладку, которая необходимо отлагывать, и **прикрепить**.</span><span class="sxs-lookup"><span data-stu-id="3c9af-180">Choose the tab you want to debug and choose **Attach**.</span></span>  

<span data-ttu-id="3c9af-181">Теперь Visual Studio отладка присоединена к Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3c9af-181">The Visual Studio debugger is now attached to Microsoft Edge.</span></span>  <span data-ttu-id="3c9af-182">Можно приостановить работу JavaScript, установить точки разрыва и просмотреть заявления непосредственно в окне `console.log()` Отлаговка в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c9af-182">You may pause the running of JavaScript, set breakpoints, and review `console.log()` statements directly in the Debug Output window in Visual Studio.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a><span data-ttu-id="3c9af-183">Контакт с командой Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-183">Getting in touch with the Microsoft Visual Studio team</span></span>  

<span data-ttu-id="3c9af-184">Команды Microsoft Visual Studio Microsoft Edge хотят узнать больше о работе с JavaScript в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3c9af-184">The Microsoft Visual Studio and Microsoft Edge teams wants to learn more about how you work with JavaScript in Visual Studio.</span></span>  <span data-ttu-id="3c9af-185">Чтобы отправить отзыв, выберите значок **Отправка** отзывов в Visual Studio или твит @VisualStudio [и @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span><span class="sxs-lookup"><span data-stu-id="3c9af-185">To send your feedback, choose the **Send Feedback** icon in Visual Studio or tweet [@VisualStudio and @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span></span>  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Значок Отправка отзывов в Visual Studio" lightbox="./media/feedback-icon.png":::
   <span data-ttu-id="3c9af-187">Значок **Отправка** отзывов в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3c9af-187">The **Send Feedback** icon in Visual Studio</span></span>  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio документации | Документы Майкрософт"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Загрузка Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Чирикать @VisualStudio и @EdgeDevTools | Twitter"  
