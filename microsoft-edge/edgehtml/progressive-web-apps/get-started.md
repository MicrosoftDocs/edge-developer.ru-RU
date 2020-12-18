---
description: В этом руководстве представлен обзор основ и средств PWA для создания последовательных веб-приложений в Windows.
title: Начало работы с последовательными веб-приложениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: progressive web apps, PWA, Edge, Windows, PWABuilder, web manifest, service worker, push
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235124"
---
# <span data-ttu-id="cdbda-104">Начало работы с последовательными веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="cdbda-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="cdbda-105">Последовательные веб-приложения \(PWAs\) — [][WikiProgressiveEnhancement] это просто веб-приложения, которые постепенно улучшаются с помощью машинных функций, похожих на приложения, на вспомогательных платформах и браузерных системах, таких как установка с домашнего экрана, поддержка в автономном режиме и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="cdbda-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="cdbda-106">В Windows 10 с обдвижком Microsoft Edge \(EdgeHTML\) pwAs пользуются дополнительным преимуществом работы независимо от окна браузера в качестве приложений универсальной [платформы Windows.][WindowsUwpGetStartedWhat]</span><span class="sxs-lookup"><span data-stu-id="cdbda-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="cdbda-107">В этом руководстве приводится обзор основ PWA путем создания простого веб-приложения в качестве PWA с помощью Microsoft Visual Studio и некоторых программах `localhost` построитель PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="cdbda-108">Готовый продукт работает аналогично в любом браузере, который поддерживает PWAs.</span><span class="sxs-lookup"><span data-stu-id="cdbda-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="cdbda-109">Чтобы быстро преобразовать существующий сайт в PWA и упаковить его для Windows 10 и других платформ приложений, просмотрите [построитель PWA.][PwaBuilder]</span><span class="sxs-lookup"><span data-stu-id="cdbda-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="cdbda-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cdbda-110">Prerequisites</span></span>  

<span data-ttu-id="cdbda-111">Вы можете создавать PWAS с помощью любой IDE веб-разработки.</span><span class="sxs-lookup"><span data-stu-id="cdbda-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="cdbda-112">Ниже приводится только обязательное условие для этого руководства, которое поможет вам в поддержке инструментов PWA в экосистеме разработчиков Windows.</span><span class="sxs-lookup"><span data-stu-id="cdbda-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="cdbda-113">Скачайте файл \(free\) [Visual Studio Community 2017.][VisualStudioDownloads]</span><span class="sxs-lookup"><span data-stu-id="cdbda-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="cdbda-114">Вы также можете использовать выпуски Professional, Enterprise или [Preview.][VisualStudioPreview]</span><span class="sxs-lookup"><span data-stu-id="cdbda-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="cdbda-115">В установщике Visual Studio выберите следующие рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cdbda-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="cdbda-116">Разработка универсальной платформы Windows</span><span class="sxs-lookup"><span data-stu-id="cdbda-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="cdbda-117">Node.js разработки</span><span class="sxs-lookup"><span data-stu-id="cdbda-117">Node.js development</span></span>**  

## <span data-ttu-id="cdbda-118">Настройка базового веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cdbda-118">Set up a basic web app</span></span>  

<span data-ttu-id="cdbda-119">Для простоты используйте шаблон приложения Visual Studio [Node.js Express][VisualStudioNodeJsTutorial] для создания веб-приложения, которое обслуживает `localhost` `index.html` страницу.</span><span class="sxs-lookup"><span data-stu-id="cdbda-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="cdbda-120">Представьте себе это в качестве заметика для привлекательных полноразмерных веб-приложений, которые вы разрабатываете как PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="cdbda-121">Запустите Visual Studio и запустите новый проект.</span><span class="sxs-lookup"><span data-stu-id="cdbda-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="cdbda-122">**Файл**  >  **Новый**  >  **Project...**</span><span class="sxs-lookup"><span data-stu-id="cdbda-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="cdbda-123">В **javaScript**выберите **basic Node.js Express 4 Application**.</span><span class="sxs-lookup"><span data-stu-id="cdbda-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="cdbda-124">За выберите имя и расположение и выберите **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="cdbda-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Выбор шаблона Node.js express 4 в Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="cdbda-126">После загрузки нового проекта выберите **build** \( `Ctrl` + `Shift` + `B` \) и **Start Debugging** \( `F5` \).</span><span class="sxs-lookup"><span data-stu-id="cdbda-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="cdbda-127">Убедитесь, `index.html` что файл загружается при `http://localhost:1337` просмотре.</span><span class="sxs-lookup"><span data-stu-id="cdbda-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Запуск нового сайта на localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="cdbda-129">Как превратить приложение в PWA</span><span class="sxs-lookup"><span data-stu-id="cdbda-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="cdbda-130">Теперь настало время примедить основные требования [PWA][PwaEdgehtmlIndexRequirements] для вашего веб-приложения: манифест *веб-приложения,* *HTTPS* и *службы.*</span><span class="sxs-lookup"><span data-stu-id="cdbda-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="cdbda-131">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cdbda-131">Web App Manifest</span></span>  

<span data-ttu-id="cdbda-132">Манифест [веб-приложения][MDNWebAppManifest] — это файл метаданных JSON, описывающий ваше приложение, включая имя, автора, URL-адрес страницы записи и один или несколько значков.</span><span class="sxs-lookup"><span data-stu-id="cdbda-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="cdbda-133">Так как она основана на стандартной схеме, необходимо предоставить только один манифест [веб-приложения][W3cWebAppManifest]для PWA, устанавливаемого на любой платформе, ОС и комбинации устройств, поддерживаюшей PWAs.</span><span class="sxs-lookup"><span data-stu-id="cdbda-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="cdbda-134">В экосистеме Windows манифест веб-приложения сообщает веб-индекселю Bing, что ваш PWA является кандидатом на автоматическое включение в [Microsoft Store,][PwaEdgehtmlMicrosoftStore]где он может достигать почти 700 миллионов активных ежемесячных пользователей в качестве приложения для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cdbda-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="cdbda-135">Если это был существующий веб-сайт, можно создать манифест веб-приложения с помощью [построитель PWA.][PwaBuilder]</span><span class="sxs-lookup"><span data-stu-id="cdbda-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="cdbda-136">Так как это еще неопубликованный проект, скопируйте пример манифеста.</span><span class="sxs-lookup"><span data-stu-id="cdbda-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="cdbda-137">В обозревателе Visual Studio *щелкните*правой кнопкой мыши обную папку и выберите "Добавить новый \*\* \*\*\*\*  >  **файл...",** указав имя `manifest.json` элемента.</span><span class="sxs-lookup"><span data-stu-id="cdbda-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="cdbda-138">`manifest.json`Скопируйте в файл следующий код.</span><span class="sxs-lookup"><span data-stu-id="cdbda-138">In the `manifest.json` file, copy the following code.</span></span>  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    <span data-ttu-id="cdbda-139">В реальном PWA следующим шагом является настройка имени *,* *start_url*, *short_name*, *описание*и *значки* \(значки описаны на следующем шаге\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="cdbda-140">Дополнительные данные о различных значениях членов и связанных с ними целях см. в справочнике по [манифесту Web App.][MDNWebAppManifest]</span><span class="sxs-lookup"><span data-stu-id="cdbda-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="cdbda-141">Затем заполните пустой массив фактическими путями изображений с помощью генератора изображений `icons` приложения построитель PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="cdbda-142">С помощью веб-браузера скачайте этот пример изображения [PWA 512x512.][ImagePwa]</span><span class="sxs-lookup"><span data-stu-id="cdbda-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="cdbda-143">Перейдите в генератор изображений приложения построитель [PWA][PwaBuilderAppImageGenerator]и выберите изображение, которое вы только что сохранили в качестве входного изображения, а затем `pwa.png` нажать кнопку **"Скачать".** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdbda-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="cdbda-144">**Откройте** и **извлеките** ZIP-файл.</span><span class="sxs-lookup"><span data-stu-id="cdbda-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="cdbda-145">В обозревателе Visual Studio щелкните правой кнопкой мыши папку и откройте папку `public` **в проводнике.**</span><span class="sxs-lookup"><span data-stu-id="cdbda-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="cdbda-146">Создайте **папку с именем** `images` ..</span><span class="sxs-lookup"><span data-stu-id="cdbda-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="cdbda-147">Скопируйте все папки платформы \( , , , и т. д.\) из извлеченного ZIP-файла в папку и закройте `android` `chrome` окно `windows10` `images` проводника.</span><span class="sxs-lookup"><span data-stu-id="cdbda-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="cdbda-148">Добавьте папки в проект Visual Studio \(в обозревателе решений щелкните правой кнопкой мыши папку и выберите "Добавить существующую папку..." для каждой `images` \*\*\*\*  >  \*\*\*\* папки\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="cdbda-149">Откройте \(с Visual Studio или любым редактором\) файл из извлеченного ZIP-файла и скопируйте массив в файл `icons.json` `"icons": [...]` `manifest.json` проекта.</span><span class="sxs-lookup"><span data-stu-id="cdbda-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="cdbda-150">Теперь необходимо связать манифест веб-приложения с приложением.</span><span class="sxs-lookup"><span data-stu-id="cdbda-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="cdbda-151">Откройте файл \(в папке\) для редактирования и добавьте эту строку сразу после ссылки `layout.pug` `views` на таблицу стилей.</span><span class="sxs-lookup"><span data-stu-id="cdbda-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="cdbda-152">\(Это просто ярлык шаблона ["Уайл"][PugAttributes] узла `<link rel='manifest' href='/manifest.json'>` для \).</span><span class="sxs-lookup"><span data-stu-id="cdbda-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="cdbda-153">Теперь ваше веб-приложение обслуживает манифест и значки приложений, готовых к домашнему экрану!</span><span class="sxs-lookup"><span data-stu-id="cdbda-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="cdbda-154">Попробуйте запускать приложение \( `F5` \) и загружать манифест.</span><span class="sxs-lookup"><span data-stu-id="cdbda-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Загрузка манифеста веб-приложения с localhost][ImageVsNodejsExpressManifest]  

<span data-ttu-id="cdbda-156">И один из ваших значков.</span><span class="sxs-lookup"><span data-stu-id="cdbda-156">And one of your icons.</span></span>  

![Загрузка логотипа приложения Square71x71Logo с localhost][ImageVsNodejsExpressIcon]  

<span data-ttu-id="cdbda-158">Если вы публикуете приложение в режиме реального времени \(с фактическим \), поисковая система Bing определяет его в качестве кандидата для автоматической упаковки и отправки в Microsoft Store как устанавливаемое приложение `start_url` для Windows [][PwaEdgehtmlMicrosoftStore] 10.</span><span class="sxs-lookup"><span data-stu-id="cdbda-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="cdbda-159">Убедитесь, что manifest.jsфайл содержит сигналы качества для [последовательных веб-приложений,][WindowsBlogsPwaEdge] для которых Bing проверяется, включая следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="cdbda-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="cdbda-160">По крайней мере один значок квадрата размером 512 пкс или больше (чтобы обеспечить источник изображения достаточного разрешения для автоматического создания экрана-заставки вашего приложения, описание в магазине, изображение плитки и т. п.).</span><span class="sxs-lookup"><span data-stu-id="cdbda-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="cdbda-161">Кроме того, используйте [ПРОТОКОЛ HTTPS,](#https) [сотрудников служб](#service-workers)и соблюдайте политики [Microsoft Store.][LegalWindowsAgrementsMicrosoftStorePolicies]</span><span class="sxs-lookup"><span data-stu-id="cdbda-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="cdbda-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="cdbda-162">HTTPS</span></span>  

<span data-ttu-id="cdbda-163">[][MDNServiceWorkerApi] Сотрудники служб и другие ключевые технологии PWA, которые работают с сотрудниками [][MDNSyncManager] служб \(например, [][MDNCache]API кэша, [][MDNPushApi]push-файлов и фоновой синхронизации\), работают только через безопасные подключения, то есть [HTTPS][WikiHttps] для рабочих сайтов или в целях `localhost` отладки.</span><span class="sxs-lookup"><span data-stu-id="cdbda-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="cdbda-164">Если вы [публикуете это][VisualStudioNodejsTutorialPublishAzureAppService] веб-приложение как веб-сайт \(например, путем настройки бесплатной учетной записи [Azure][AzureCreateFreeAccount]\), необходимо убедиться, что сервер настроен для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cdbda-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="cdbda-165">Если для узла сайта используется [служба приложений Microsoft Azure,][AzureWebApps] она по умолчанию обслуживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cdbda-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="cdbda-166">В этом руководстве по-прежнему используется в качестве замещего для `http://localhost` обслуживаемого веб-сайта. `https://`</span><span class="sxs-lookup"><span data-stu-id="cdbda-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="cdbda-167">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="cdbda-167">Service Workers</span></span>  

<span data-ttu-id="cdbda-168">Service Workers is the key technology behind PWAs.</span><span class="sxs-lookup"><span data-stu-id="cdbda-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="cdbda-169">Сотрудники служб выступают в качестве прокси-сервера между PWA и сетью, чтобы ваш веб-сайт функционировал как установленное нативное приложение, которое обслуживает автономные сценарии, реагирует на push-уведомления сервера и выполняет фоновые задачи.</span><span class="sxs-lookup"><span data-stu-id="cdbda-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="cdbda-170">Кроме того, сотрудники служб открывают новые стратегии производительности.</span><span class="sxs-lookup"><span data-stu-id="cdbda-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="cdbda-171">Вам не требуется реализовать полное веб-приложение для использования кэша рабочих служб для точной настройки производительности загрузки страницы для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="cdbda-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="cdbda-172">Сотрудники службы — это фоновые потоки на основе событий, которые запускаются из файлов JavaScript, обслуживаемого вместе с обычными сценариями, которые используют ваше веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="cdbda-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="cdbda-173">Поскольку рабочие процессы не работают в основном потоке пользовательского интерфейса, [][MDNWorkerPrototypePostMessage] у сотрудников [][MDNDedicatedWorkerGlobalScopePostMessage] служб нет доступа к DOM, хотя поток пользовательского интерфейса и рабочий поток могут взаимодействовать с помощью обработчиков событий и обработчиков `postMessage()` `onmessage` событий.</span><span class="sxs-lookup"><span data-stu-id="cdbda-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="cdbda-174">Вы связываете сотрудника службы с приложением, регистрируете его в источнике URL-адреса сайта \(или указанном пути в нем\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="cdbda-175">После регистрации рабочий файл службы загружается, устанавливается и активируется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="cdbda-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="cdbda-176">Для получения дополнительной информации в веб-документы [][MDNUsingServiceWorkers] MDN есть полное руководство по использованию рабочих работников и подробная справка [по API рабочих][MDNServiceWorkerApi] служб.</span><span class="sxs-lookup"><span data-stu-id="cdbda-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="cdbda-177">В этом руководстве используйте рабочий сценарий службы автономной страницы в [ПОСТРОИТЕЛЕ PWA.][PwaBuilderServiceWorker]</span><span class="sxs-lookup"><span data-stu-id="cdbda-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="cdbda-178">Начните с настройки скрипта с дополнительными функциональными возможностями в соответствии с требованиями к производительности, пропускной способности сети и так далее.</span><span class="sxs-lookup"><span data-stu-id="cdbda-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="cdbda-179">Просмотрите [руководство по работе с рабочими службами,][ServiceWorkerCookbook]  предоставленное Mozilla, чтобы просмотреть ряд полезных идей о кэшинге рабочих служб.</span><span class="sxs-lookup"><span data-stu-id="cdbda-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="cdbda-180">Откройте и выберите рабочий сотрудник службы автономной страницы [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] \(default\) и нажмите кнопку "Загрузить **рабочий файл службы".** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdbda-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="cdbda-181">Откройте папку скачивания и скопируйте два следующих файла</span><span class="sxs-lookup"><span data-stu-id="cdbda-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="cdbda-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="cdbda-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="cdbda-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="cdbda-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="cdbda-184">Сохраните файлы в `public` папку проекта Visual Studio веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="cdbda-185">\(Из Visual Studio откройте проводник в проекте и перейдите `Ctrl` + `O` в `public` папку\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="cdbda-186">В обозревателе решений откройте `public/pwabuilder-sw.js` файл и измените значение на `offlineFallbackPage` `offline.html` .</span><span class="sxs-lookup"><span data-stu-id="cdbda-186">In Solution Explorer, open the `public/pwabuilder-sw.js` file, and change the value of `offlineFallbackPage` to `offline.html`.</span></span>  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    <span data-ttu-id="cdbda-187">Стоит инициировать код в обоих этих файлах, чтобы узнать, как зарегистрировать сотрудника службы, который кэширует назначенную страницу \( \) и обслуживает ее, когда происходит сбой сетевого `offline.html` получения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-187">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="cdbda-188">Затем создайте простую страницу в качестве замещего для `offline.html` автономной функциональности приложения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-188">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="cdbda-189">В обозревателе решений откройте файл и добавьте `views/layout.pug` следующую строку под тегами ссылок.</span><span class="sxs-lookup"><span data-stu-id="cdbda-189">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    <span data-ttu-id="cdbda-190">Сайт загружает и запускает скрипт регистрации рабочих служб.</span><span class="sxs-lookup"><span data-stu-id="cdbda-190">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="cdbda-191">В обозревателе решений щелкните папку правой кнопкой мыши и `public` выберите **"Добавить**  >  **новый файл"...**  `offline.html`Назовем его и добавьте содержимое и некоторые части `<title>` тела, например следующий код.</span><span class="sxs-lookup"><span data-stu-id="cdbda-191">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    <span data-ttu-id="cdbda-192">На этом этапе ваша `public` папка должна иметь три новых файла.</span><span class="sxs-lookup"><span data-stu-id="cdbda-192">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Файлы, добавленные в обную папку решения][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="cdbda-194">В обозревателе решений откройте файл и добавьте следующий код перед последней `routes\index.js` командой \( `module.exports = router;` \).</span><span class="sxs-lookup"><span data-stu-id="cdbda-194">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="cdbda-195">Это предписывает приложению обслуживать файл \(когда сотрудник службы извлекает его для `offline.html` автономного кэша\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-195">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="cdbda-196">Протестировать PWA!</span><span class="sxs-lookup"><span data-stu-id="cdbda-196">Test out your PWA!</span></span>  <span data-ttu-id="cdbda-197">Создайте \( `Ctrl` + `Shift` + `B` \) и запустите `F5` \( ваше веб-приложение, чтобы запустить Microsoft Edge и открыть `localhost` страницу.</span><span class="sxs-lookup"><span data-stu-id="cdbda-197">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="cdbda-198">Затем выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cdbda-198">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="cdbda-199">Откройте консоль Edge DevTools \*\*\*\* \( \) и `Ctrl` + `Shift` + `J` убедитесь, что сотрудник службы зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="cdbda-199">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="cdbda-200">На панели **отладки** разйдите к окне управления **"Service Workers" (Рабочие** службы) и щелкните свой источник.</span><span class="sxs-lookup"><span data-stu-id="cdbda-200">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="cdbda-201">В **обзоре рабочих служб**убедитесь, что ваш рабочий работник активирован и запущен.</span><span class="sxs-lookup"><span data-stu-id="cdbda-201">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Обзор рабочего сотрудника службы Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="cdbda-203">Раз развернуть **кэш-контроль** и `offline.html` убедиться, что страница кэшироваться.</span><span class="sxs-lookup"><span data-stu-id="cdbda-203">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Кэш рабочего кэша службы Edge DevTools][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="cdbda-205">Время попробовать PWA в качестве автономного приложения!</span><span class="sxs-lookup"><span data-stu-id="cdbda-205">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="cdbda-206">В Visual Studio остановите **отладку** \( \) вашего веб-приложения, а затем откройте `Shift` + `F5` Microsoft Edge \(или обновить\) на адрес localhost вашего веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="cdbda-206">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="cdbda-207">Теперь она должна загрузить страницу \(благодаря рабочим службам и автономному `offline.html` кэше\)!</span><span class="sxs-lookup"><span data-stu-id="cdbda-207">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline.html из http://localhost:1337 загруженного в Microsoft Edge][ImageOfflineHtml]  

## <span data-ttu-id="cdbda-209">Добавление push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="cdbda-209">Add push notifications</span></span>  

<span data-ttu-id="cdbda-210">Сделайте PWA более похожим на приложение, добавив поддержку push-уведомлений на стороне клиента с помощью [Push API][MDNPushApi] для подписки на службу обмена сообщениями и [API][MDNNotificationsApi] уведомлений для отображения всплывающее сообщение при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-210">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="cdbda-211">Как и для сотрудников служб, это основанные на стандартах API, работающие в разных браузерах, поэтому вам нужно написать код только один раз, чтобы он работал везде, где поддерживаются PWAs.</span><span class="sxs-lookup"><span data-stu-id="cdbda-211">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="cdbda-212">На стороне сервера используйте библиотеку с открытым кодом [Web-Push][NPMWebPush] для обработки различий, которые связаны с доставкой push-сообщений в различные браузеры.</span><span class="sxs-lookup"><span data-stu-id="cdbda-212">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="cdbda-213">Ниже приводится адаптация из книги "Push Rich Demo in [Service WorkerBook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет смысл инициировать ряд других полезных рабочих рецептов web Push и служб.</span><span class="sxs-lookup"><span data-stu-id="cdbda-213">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="cdbda-214">Шаг 1. Установка библиотеки веб-push NPM</span><span class="sxs-lookup"><span data-stu-id="cdbda-214">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="cdbda-215">В Visual Studio обозревателе решений щелкните правой кнопкой мыши проект и откройте **Node.js интерактивное окно...**  Введите в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="cdbda-215">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="cdbda-216">При этом будет [устанавливаться библиотека Web-Push.][NPMWebPush]</span><span class="sxs-lookup"><span data-stu-id="cdbda-216">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="cdbda-217">Затем откройте файл и добавьте следующую строку в верхнюю часть файла после `index.js` других требований.</span><span class="sxs-lookup"><span data-stu-id="cdbda-217">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="cdbda-218">Шаг 2. Создание ключей VAPID для сервера</span><span class="sxs-lookup"><span data-stu-id="cdbda-218">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="cdbda-219">Затем необходимо создать ключи VAPID \(Voluntary Application Server Identification\) для сервера для отправки push-сообщений клиенту PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-219">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="cdbda-220">Это необходимо сделать только один раз (то есть серверу требуется только одна пара ключей VAPID\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-220">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="cdbda-221">В интерактивном Node.js введите следующий код.</span><span class="sxs-lookup"><span data-stu-id="cdbda-221">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="cdbda-222">Выходные данные должны привести к объекту JSON, содержащего открытый и закрытый ключ, который копируется в логику сервера.</span><span class="sxs-lookup"><span data-stu-id="cdbda-222">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="cdbda-223">В `index.js` файле перед последней строкой \( `module.exports = router` \) добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="cdbda-223">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

<span data-ttu-id="cdbda-224">`publicKey`Скопируйте `privateKey` только что созданные значения и их значения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-224">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="cdbda-225">Вы также можете настроить адрес \(хотя это не обязательно для запуска `mailto` этого примера\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-225">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="cdbda-226">В [блоге разработчика Mozilla Services][MozillaServicesSendingVapidWebPushNotificationsPush] есть хорошее объяснение о VAPID и WebPush, если вас интересуют подробные сведения о том, как это работает.</span><span class="sxs-lookup"><span data-stu-id="cdbda-226">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="cdbda-227">Шаг 3. Обработка запросов серверов, связанных с push-запросами</span><span class="sxs-lookup"><span data-stu-id="cdbda-227">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="cdbda-228">Теперь настроим маршруты для обработки запросов, связанных с push-запросами от клиента PWA, включая обслуживание открытого ключа VAPID и регистрацию клиента для получения push-запросов.</span><span class="sxs-lookup"><span data-stu-id="cdbda-228">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="cdbda-229">В реальном сценарии push-уведомление, скорее всего, происходит из события в логике сервера.</span><span class="sxs-lookup"><span data-stu-id="cdbda-229">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="cdbda-230">Чтобы упростить эту процедуру, необходимо добавить кнопку push-уведомлений на нашу домашную странице PWA для создания push-уведомлений с сервера и конечную точку \*\*\*\* `/sendNotification` \(маршрут сервера\) для обработки этих запросов.</span><span class="sxs-lookup"><span data-stu-id="cdbda-230">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="cdbda-231">В файле следует добавить следующие маршруты сразу после кода инициализации VAPID, добавленного в `index.js` [шаг 2][#step-2---generate-vapid-keys-for-your-server].</span><span class="sxs-lookup"><span data-stu-id="cdbda-231">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

<span data-ttu-id="cdbda-232">После на месте кода на стороне сервера можно получать push-уведомления в клиенте PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-232">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="cdbda-233">Шаг 4. Подписка на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="cdbda-233">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="cdbda-234">В качестве прокси-служб сети PWA сотрудники службы обрабатывают события push-уведомлений и взаимодействия всплывающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cdbda-234">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="cdbda-235">Однако, как и при первой настройке \(или регистрации\) рабочего сервера службы, подписка PWA на сервер push-уведомлений происходит в основном потоке пользовательского интерфейса PWA и требует сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="cdbda-235">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="cdbda-236">Для подписки на push-уведомления требуется активная регистрация рабочих служб, поэтому необходимо сначала убедиться, что рабочий процесс службы установлен и активен, прежде чем пытаться подписать его на push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="cdbda-236">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="cdbda-237">Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cdbda-237">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="cdbda-238">В этом случае браузер запросит разрешение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="cdbda-238">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="cdbda-239">Если в разрешении отказано, запрос на `registration.pushManager.subscribe` отклонение `DOMException` запроса будет отклонен, поэтому его необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="cdbda-239">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="cdbda-240">Подробнее об управлении разрешениями см. в [push-уведомлениях в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]</span><span class="sxs-lookup"><span data-stu-id="cdbda-240">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="cdbda-241">В `pwabuilder-sw-register.js` файле в коде ниже.</span><span class="sxs-lookup"><span data-stu-id="cdbda-241">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
            });
        });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

<span data-ttu-id="cdbda-242">Дополнительные сведения о работе API и различных связанных параметрах можно узнать в документации MDN по интерфейсу [PushManager][MDNPushManager] и документации NPM в библиотеке [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="cdbda-242">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="cdbda-243">Шаг 5. Настройка обработчиков событий push-уведомлений и push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="cdbda-243">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="cdbda-244">После того как настроена наша push-подписка, оставшаяся часть работы будет происходить в сотруднике службы.</span><span class="sxs-lookup"><span data-stu-id="cdbda-244">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="cdbda-245">Сначала необходимо настроить обработок для событий push-уведомлений, отправленных сервером, и ответить всплывающим уведомлением \(если разрешение было предоставлено\) с отображением полезной нагрузки push-данных.</span><span class="sxs-lookup"><span data-stu-id="cdbda-245">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="cdbda-246">Далее добавляется обработок щелчка для всплывающее уведомление, чтобы отклонять уведомление и сортировать список открытых в настоящее время окон для открытия, фокуса или открытия и фокуса на нужной клиентской странице PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-246">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="cdbda-247">В `pwabuilder-sw.js` файле привяжем следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="cdbda-247">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### <span data-ttu-id="cdbda-248">Шаг 6. Попробуйте</span><span class="sxs-lookup"><span data-stu-id="cdbda-248">Step 6 - Try it out</span></span>  

<span data-ttu-id="cdbda-249">Время для тестирования push-уведомлений в PWA!</span><span class="sxs-lookup"><span data-stu-id="cdbda-249">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="cdbda-250">Запустите \( `F5` \) PWA в браузере.</span><span class="sxs-lookup"><span data-stu-id="cdbda-250">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="cdbda-251">Так как вы изменили рабочий код службы \( \), необходимо открыть `pwabuilder-sw.js` devTools Debugger \( \) на панели "Обзор рабочего сотрудника службы" и отозарегистрировать рабочий сотрудник службы и перезагрузить страницу, чтобы повторно зарегистрировать ее (или щелкнуть `F12` \*\*\*\* \*\*\*\* `F5` "Обновить\"). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cdbda-251">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="cdbda-252">В производственном сценарии браузер регулярно проверяет наличие обновлений рабочих служб и устанавливает их в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cdbda-252">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="cdbda-253">Вы должны принудительно использовать его для немедленного результата.</span><span class="sxs-lookup"><span data-stu-id="cdbda-253">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="cdbda-254">По мере активации и попытки подписки PWA на push-уведомления сотрудник службы должен увидеть диалоговое окно разрешений в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="cdbda-254">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Диалоговое окно разрешений для включения уведомлений][ImageNotificationPermission]  
    
    <span data-ttu-id="cdbda-256">Выберите **"Да",** чтобы включить всплывающие уведомления для PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-256">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="cdbda-257">В области "Общие сведения о рабочих службах" попробуйте нажать кнопку **"Push".**</span><span class="sxs-lookup"><span data-stu-id="cdbda-257">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="cdbda-258">Должно появиться всплывающее уведомление с жестко задаваемой кодой "Test push message from DevTools"\).</span><span class="sxs-lookup"><span data-stu-id="cdbda-258">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Push-уведомление от DevTools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="cdbda-260">Затем попробуйте нажать кнопку **"Отправить уведомление"** на домашней странице PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-260">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="cdbda-261">На этот раз появляется всплывающее уведомление с полезной нагрузкой с сервера.</span><span class="sxs-lookup"><span data-stu-id="cdbda-261">This time a toast with the payload from your server appears.</span></span>  
    
    ![Push-уведомление с сервера PWA][ImagePwaPush]  
    
    <span data-ttu-id="cdbda-263">Если вы не нажмете \(или активируете\) всплывающее уведомление, оно будет отклонено через несколько секунд и в очереди в центре уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="cdbda-263">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Уведомления в Центре уведомлений Windows][ImageWindowsActionCenter]  
    
    <span data-ttu-id="cdbda-265">У вас есть основы push-уведомлений PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-265">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="cdbda-266">В реальном приложении дальнейшие действия реализуются таким образом, чтобы управлять push-подписками и хранить их, а также правильно шифровать данные полезной нагрузки, отправляемые по сети. [][NPMWebPushEncrypt]</span><span class="sxs-lookup"><span data-stu-id="cdbda-266">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="cdbda-267">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="cdbda-267">Going further</span></span>  

<span data-ttu-id="cdbda-268">В этом руководстве демонстрируется базовая структура прогрессивного веб-приложения и средств разработки Microsoft PWA, включая Visual Studio, построитель PWA и Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cdbda-268">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="cdbda-269">Конечно, существует намного больше возможностей для создания отличной [веб-части][BrowserStackTestEdgeBrowser] [PWA,][PwaEdgehtmlIndexRequirements] которая выходит за рамки того, что вы здесь читаете, включая адаптивный дизайн, глубокие связи, тестирование в нескольких браузерах и другие лучшие методики [\(не][Webhint] говоря уже о возможностях вашего приложения!\), но надеемся, что в этом руководстве вы хорошо знаете основы PWA и некоторые идеи по началу работы.</span><span class="sxs-lookup"><span data-stu-id="cdbda-269">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="cdbda-270">Если у вас есть дополнительные вопросы о разработке PWA с помощью Windows или Visual Studio, оставьте комментарий!</span><span class="sxs-lookup"><span data-stu-id="cdbda-270">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="cdbda-271">Просмотрите другие руководства PWA, чтобы узнать, как повысить вовлеченность клиентов и обеспечить более простое, интегрированное с ОС взаимодействие с приложением.</span><span class="sxs-lookup"><span data-stu-id="cdbda-271">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="cdbda-272">[Подекание Windows.][PwaEdgehtmlWindowsFeatures]</span><span class="sxs-lookup"><span data-stu-id="cdbda-272">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="cdbda-273">Используя простое обнаружение функций, вы можете постепенно улучшить PWA для пользователей Windows 10 с помощью собственный API-интерфейсов windows runtime \(WinRT\), например для настройки уведомлений плитки меню "Пуск" **и** списков переходов на панели задач Windows, а также \(по разрешению\) работы с пользовательскими ресурсами, такими как фотографии, музыка и календарь.</span><span class="sxs-lookup"><span data-stu-id="cdbda-273">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="cdbda-274">[PWAs в Microsoft Store.][PwaEdgehtmlMicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="cdbda-274">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="cdbda-275">Узнайте больше о преимуществах распространения магазина приложений и о том, как отправить PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-275">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="cdbda-276">См. также</span><span class="sxs-lookup"><span data-stu-id="cdbda-276">See also</span></span>  

*   <span data-ttu-id="cdbda-277">[Прогрессивное веб-приложения в веб-документы MDN][MDNProgressiveWebApps] — отличное руководство по прогрессивному веб-приложениям.</span><span class="sxs-lookup"><span data-stu-id="cdbda-277">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="cdbda-278">[Прогрессивное веб-приложения на веб-сайте web.dev][WebDevProgressiveWebApps] — отличное руководство по прогрессивному веб-приложениям.</span><span class="sxs-lookup"><span data-stu-id="cdbda-278">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="cdbda-279">[Прогрессивное веб-приложение —][ProgressiveWebApps] демонстрация реальных примеров PWAs.</span><span class="sxs-lookup"><span data-stu-id="cdbda-279">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="cdbda-280">[Читатели новостей Хакера как прогрессивное веб-приложение][HackerNewsProgressiveWebApps] — сравнивают различные структуры и шаблоны производительности для реализации примера \(Читателя новостей хакера\) PWA.</span><span class="sxs-lookup"><span data-stu-id="cdbda-280">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Документы Майкрософт"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Progressive Web Apps \(EdgeHTML\)in the Microsoft Store | Документы Майкрософт"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Адаптировать PWA \(EdgeHTML\) для Windows | Документы Майкрософт"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Политики Microsoft Store | Документы Майкрософт"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Учебник. Создание приложения Node.js Express в Visual Studio | Документы Майкрософт"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Публикация в службе приложений Azure : создание приложения Node.js и приложения Express в Visual Studio | Документы Майкрософт"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Что такое приложение универсальной платформы Windows \(UWP\)?  | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Постепенное обновление веб-приложений в Microsoft Edge и Windows 10 | Блоги Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Загрузки | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Free Developer Software & Services | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio Preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивного веб-приложения"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope.postMessage\(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивное веб-приложение \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование сотрудников служб | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker.prototype.postMessage\(\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений WebPush с помощью службы push-уведомлений Mozilla | Службы Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивное веб-приложение"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Атрибуты | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Построитель PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Генератор изображений приложений"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Построитель PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorkerBook"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorkerBook"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Манифест веб-приложения | W3C"  

[Webhint]: https://sonarwhal.com "webhint, механизм подсказок для веб-методов" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-работников" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивное веб-приложение | web.dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Википедия"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивное улучшение | Википедия"  
