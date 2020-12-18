---
description: В этом руководстве представлен обзор основ и средств PWA для создания прогрессивного веб-приложения (Chromium) в Windows.
title: Начало работы с progressive Web Apps (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: progressive web apps, PWA, Edge, Windows, PWABuilder, web manifest, service worker, push
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231225"
---
# <span data-ttu-id="b601e-104">Начало работы с progressive Web Apps (Chromium)</span><span class="sxs-lookup"><span data-stu-id="b601e-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="b601e-105">Прогрессивное веб-приложения \(PWAs\) — это веб-приложения, [которые постепенно улучшаются.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="b601e-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="b601e-106">К последовательным усовершенствованиям относятся такие функции, как установка, поддержка в автономном режиме и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="b601e-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="b601e-107">Вы также можете упаковать PWA для магазинов приложений.</span><span class="sxs-lookup"><span data-stu-id="b601e-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="b601e-108">Возможные магазины приложений включают Microsoft Store, Google Play, Магазин приложений Mac и другие.</span><span class="sxs-lookup"><span data-stu-id="b601e-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="b601e-109">Microsoft Store — это коммерческий магазин приложений, встроенный в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="b601e-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="b601e-110">В следующем руководстве приводится обзор основ PWA путем создания простого веб-приложения и расширения его в качестве PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="b601e-111">Готовый проект работает в современных браузерах.</span><span class="sxs-lookup"><span data-stu-id="b601e-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="b601e-112">Вы можете использовать [PWABuilder][PwaBuilder] для создания нового PWA, улучшения существующей PWA или упаковки PWA для магазинов приложений.</span><span class="sxs-lookup"><span data-stu-id="b601e-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="b601e-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="b601e-113">Prerequisites</span></span>  

*   <span data-ttu-id="b601e-114">Используйте [Visual Studio code для][VisualstudioCodeMain] редактирования кода PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="b601e-115">Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="b601e-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <span data-ttu-id="b601e-116">Создание базового веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b601e-116">Create a basic web app</span></span>  

<span data-ttu-id="b601e-117">Чтобы создать пустое веб-приложение, следуйте шагам в [node Express App Generator][ExpressjsApplicationGenerator]и придайте приложению `MySamplePwa` имя.</span><span class="sxs-lookup"><span data-stu-id="b601e-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="b601e-118">В командной подсказке запустите следующие команды.</span><span class="sxs-lookup"><span data-stu-id="b601e-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="b601e-119">Команды создают пустое веб-приложение и устанавливают зависимости.</span><span class="sxs-lookup"><span data-stu-id="b601e-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="b601e-120">Теперь у вас есть простое функциональное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="b601e-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="b601e-121">Чтобы запустить веб-приложение, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b601e-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="b601e-122">Теперь `http://localhost:3000` перейдите, чтобы просмотреть новое веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="b601e-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск нового PWA на localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="b601e-124">Запуск нового PWA на localhost</span><span class="sxs-lookup"><span data-stu-id="b601e-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="b601e-125">Начало создания PWA</span><span class="sxs-lookup"><span data-stu-id="b601e-125">Get started building a PWA</span></span>  

<span data-ttu-id="b601e-126">Теперь, когда у вас есть простое веб-приложение, расширьте его как PWA, добавив три требования для PWAS</span><span class="sxs-lookup"><span data-stu-id="b601e-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="b601e-127">: [HTTPS,](#step-1---use-https)манифест [веб-приложения](#step-2---create-a-web-app-manifest)и [рабочий работник службы.](#step-3---add-a-service-worker)</span><span class="sxs-lookup"><span data-stu-id="b601e-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="b601e-128">Шаг 1. Использование ПРОТОКОЛА HTTPS</span><span class="sxs-lookup"><span data-stu-id="b601e-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="b601e-129">Ключевые части платформы PWA, такие как [сотрудники][MDNServiceWorkerApi]служб, требуют использования ПРОТОКОЛА HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b601e-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="b601e-130">Когда веб-сайт PWA будет работать, его необходимо опубликовать на URL-адресе HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b601e-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="b601e-131">В целях отладки Microsoft Edge также разрешает использовать `http://localhost` API PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="b601e-132">[Опубликуйте веб-приложение в качестве][VisualStudioNodejsTutorialPublishAzureAppService]веб-сайта, но убедитесь, что сервер настроен для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b601e-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="b601e-133">Например, вы можете создать бесплатную учетную [запись Azure.][AzureCreateFreeAccount]</span><span class="sxs-lookup"><span data-stu-id="b601e-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="b601e-134">Разойдите сайт в [службу приложений Microsoft Azure,][AzureWebApps] и он по умолчанию обслуживается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b601e-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="b601e-135">В следующем руководстве используется `http://localhost` для создания PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="b601e-136">Шаг 2. Создание манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b601e-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="b601e-137">Манифест [Веб-приложения][MDNWebAppManifest] — это JSON-файл, содержащий метаданные о вашем приложении, такие как имя, описание, значки и другие.</span><span class="sxs-lookup"><span data-stu-id="b601e-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="b601e-138">Добавление манифеста приложения в веб-приложение:</span><span class="sxs-lookup"><span data-stu-id="b601e-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="b601e-139">В Visual Studio code выберите **папку "Открыть**файл" и выберите созданный  >  \*\*\*\* `MySamplePwa` ранее каталог.</span><span class="sxs-lookup"><span data-stu-id="b601e-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="b601e-140">Выберите, `Ctrl` + `N` чтобы создать новый файл, и в paste в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="b601e-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  <span data-ttu-id="b601e-141">Сохраните файл как `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="b601e-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="b601e-142">Добавьте изображение значка приложения 512x512 с именем `icon512.png` `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="b601e-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="b601e-143">Пример изображения можно [использовать в][ImagePwa] целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="b601e-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="b601e-144">В Visual Studio Code откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.</span><span class="sxs-lookup"><span data-stu-id="b601e-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="b601e-145">Шаг 3. Добавление сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="b601e-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="b601e-146">Сотрудники службы — это ключевая технология, обеспечивающая такие сценарии, как поддержка в автономном режиме, расширенный кэш и выполнение фоновых задач, которые ранее были ограничены основными приложениями.</span><span class="sxs-lookup"><span data-stu-id="b601e-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="b601e-147">Сотрудники службы — это фоновые задачи, которые перехватывают сетевые запросы из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b601e-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="b601e-148">Сотрудники служб пытаются выполнить задачи, даже если PWA не запущен.</span><span class="sxs-lookup"><span data-stu-id="b601e-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="b601e-149">К задачам относятся следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b601e-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="b601e-150">Обслуживание запрашиваемых ресурсов из кэша</span><span class="sxs-lookup"><span data-stu-id="b601e-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="b601e-151">Отправка push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="b601e-151">Sending push notifications</span></span>  
*   <span data-ttu-id="b601e-152">Выполнение фоновых задач получения</span><span class="sxs-lookup"><span data-stu-id="b601e-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="b601e-153">Плохое значки</span><span class="sxs-lookup"><span data-stu-id="b601e-153">Badging icons</span></span>  
*   <span data-ttu-id="b601e-154">и другие</span><span class="sxs-lookup"><span data-stu-id="b601e-154">and more</span></span>  
    
<span data-ttu-id="b601e-155">Сотрудники служб определяются в специальном файле JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b601e-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="b601e-156">Для получения дополнительных сведений перейдите к использованию API ["Сотрудники службы"][MDNUsingServiceWorkers] [и "Рабочие службы".][MDNServiceWorkerApi]</span><span class="sxs-lookup"><span data-stu-id="b601e-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="b601e-157">Чтобы создать в проекте рабочий \*\*\*\* работник службы, используйте рабочий рецепт сетевой службы из кэша из [построщика PWA.][PwaBuilderServiceWorker]</span><span class="sxs-lookup"><span data-stu-id="b601e-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="b601e-158">Перейдите [pwabuilder.com/serviceworker,][PwaBuilderServiceWorker] **выберите** рабочий процесс сетевой службы с первым кэшом и кнопку **"Скачать".**</span><span class="sxs-lookup"><span data-stu-id="b601e-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="b601e-159">Загруженный файл содержит следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="b601e-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="b601e-160">Скопируйте загруженные файлы в `public` папку проекта веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b601e-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="b601e-161">В Visual Studio Code откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.</span><span class="sxs-lookup"><span data-stu-id="b601e-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="b601e-162">Теперь в вашем веб-приложении есть сотрудник службы, использующий стратегию с первого кэша.</span><span class="sxs-lookup"><span data-stu-id="b601e-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="b601e-163">Новый рабочий процесс службы сначала получает ресурсы из кэша и только из сети при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b601e-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="b601e-164">К кэшным ресурсам относятся изображения, JavaScript, CSS и HTML.</span><span class="sxs-lookup"><span data-stu-id="b601e-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="b601e-165">Чтобы подтвердить, что ваш рабочий работник работает, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b601e-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="b601e-166">Перейдите к веб-приложению с помощью `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="b601e-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="b601e-167">Если веб-приложение не доступно, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b601e-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="b601e-168">В Microsoft Edge `F12` выберите, чтобы открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b601e-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b601e-169">Выберите **"Приложение",** затем **"Сотрудники служб",** чтобы просмотреть сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="b601e-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="b601e-170">Если рабочий работник службы не отображается, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="b601e-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Обзор рабочих сотрудников службы Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="b601e-172">Обзор рабочих сотрудников службы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b601e-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="b601e-173">Просмотреть кэш рабочих \*\*\*\* служб, расширив хранилище кэша и выбрав **pwabuilder-precache.**</span><span class="sxs-lookup"><span data-stu-id="b601e-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="b601e-174">Должны отображаться все ресурсы, кэшные рабочим работником службы.</span><span class="sxs-lookup"><span data-stu-id="b601e-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="b601e-175">Ресурсы, кэшментные сотрудником службы, включают значок приложения, манифест приложения, CSS-файлы и файлы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b601e-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Кэш рабочих служб в Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="b601e-177">Кэш рабочих служб в Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="b601e-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="b601e-178">Попробуйте PWA в качестве автономного приложения.</span><span class="sxs-lookup"><span data-stu-id="b601e-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="b601e-179">В Microsoft Edge DevTools \( \) выберите "Сеть", а затем измените состояние `F12` **"Online"** на **"Автономный".** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b601e-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Настройка автономного режима приложения в Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="b601e-181">Настройка автономного режима приложения в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b601e-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="b601e-182">Обновите приложение, и оно должно отобразить автономный механизм обслуживания ресурсов приложения из кэша.</span><span class="sxs-lookup"><span data-stu-id="b601e-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск PWA в автономном режиме" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="b601e-184">Запуск PWA в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="b601e-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="b601e-185">Добавление push-уведомлений в PWA</span><span class="sxs-lookup"><span data-stu-id="b601e-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="b601e-186">Вы можете создать PWAS, которые поддерживают push-уведомления, выполв следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="b601e-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="b601e-187">Подписка на службу обмена сообщениями с помощью [API Push][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="b601e-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="b601e-188">Отображение всплывающее сообщение при получении сообщения от службы с помощью [API уведомлений][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="b601e-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="b601e-189">Как и в службах, API push-уведомлений являются основанными на стандартах API.</span><span class="sxs-lookup"><span data-stu-id="b601e-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="b601e-190">API push-уведомлений работают в браузерах, поэтому ваш код должен работать везде, где поддерживаются PWAs.</span><span class="sxs-lookup"><span data-stu-id="b601e-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="b601e-191">Дополнительные сведения о доставке push-сообщений в различные браузеры на сервере можно найти в [Web-Push.][NPMWebPush]</span><span class="sxs-lookup"><span data-stu-id="b601e-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="b601e-192">Следующие действия были адаптированы из книги "Push Rich Demo in [Service WorkerBook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет ряд других полезных рецептов для рабочих рабочих служб и веб-push-служб.</span><span class="sxs-lookup"><span data-stu-id="b601e-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="b601e-193">Шаг 1. Создание ключей VAPID</span><span class="sxs-lookup"><span data-stu-id="b601e-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="b601e-194">Для push-уведомлений требуются ключи VAPID \(Voluntary Application Server Identification\) для отправки push-сообщений клиенту PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="b601e-195">В Сети доступно несколько генераторов ключей VAPID (например, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="b601e-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="b601e-196">После генерации вы должны получить объект JSON, содержащий открытый и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b601e-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="b601e-197">Сохраните ключи для последующих действий в следующем руководстве.</span><span class="sxs-lookup"><span data-stu-id="b601e-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="b601e-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="b601e-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="b601e-199">Шаг 2. Подписка на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="b601e-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="b601e-200">Сотрудники служб обрабатывают события push-уведомлений и взаимодействия всплывающих уведомлений в PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="b601e-201">Чтобы подписать PWA на push-уведомления сервера, убедитесь, что выполнены следующие условия.</span><span class="sxs-lookup"><span data-stu-id="b601e-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="b601e-202">Веб-приложение PWA установлено, активно и зарегистрировано</span><span class="sxs-lookup"><span data-stu-id="b601e-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="b601e-203">Код для выполнения задачи подписки находится в основном потоке пользовательского интерфейса PWA</span><span class="sxs-lookup"><span data-stu-id="b601e-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="b601e-204">У вас есть сетевое подключение</span><span class="sxs-lookup"><span data-stu-id="b601e-204">You have network connectivity</span></span>  
    
<span data-ttu-id="b601e-205">Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b601e-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="b601e-206">В этом случае браузер запросит разрешение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="b601e-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="b601e-207">Если разрешение отказано, запрос на отклонение запроса `registration.pushManager.subscribe` , который должен быть `DOMException` обработан.</span><span class="sxs-lookup"><span data-stu-id="b601e-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="b601e-208">Для получения дополнительных информации об управлении разрешениями перейдите к [push-уведомлениям в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]</span><span class="sxs-lookup"><span data-stu-id="b601e-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="b601e-209">В `pwabuilder-sw-register.js` файле примените следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="b601e-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
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

<span data-ttu-id="b601e-210">Дополнительные сведения можно найти в [PushManager][MDNPushManager] и [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="b601e-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="b601e-211">Шаг 3. Прослушивание push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="b601e-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="b601e-212">После создания подписки в PWA добавьте обработчики в рабочий процесс службы для реагирования на события push-рассылки.</span><span class="sxs-lookup"><span data-stu-id="b601e-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="b601e-213">Событие Push отправляется с сервера для отображения всплывающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b601e-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="b601e-214">Всплывающие уведомления отображают данные о полученном сообщении.</span><span class="sxs-lookup"><span data-stu-id="b601e-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="b601e-215">Для выполнения следующих задач необходимо добавить обработок щелчка.</span><span class="sxs-lookup"><span data-stu-id="b601e-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="b601e-216">Отклонение всплывающее уведомление</span><span class="sxs-lookup"><span data-stu-id="b601e-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="b601e-217">Открывать, фокусировать или открывать и фокусировать любые открытые окна</span><span class="sxs-lookup"><span data-stu-id="b601e-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="b601e-218">Открытие и фокус в новом окне для отображения клиентской страницы PWA</span><span class="sxs-lookup"><span data-stu-id="b601e-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="b601e-219">Добавьте `pwabuilder-sw.js` в файл следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="b601e-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

### <span data-ttu-id="b601e-220">Шаг 4. Попробуйте</span><span class="sxs-lookup"><span data-stu-id="b601e-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="b601e-221">Чтобы протестировать push-уведомления для PWA, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b601e-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="b601e-222">Перейдите к PWA `http://localhost:3000` по</span><span class="sxs-lookup"><span data-stu-id="b601e-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="b601e-223">Когда ваш сотрудник службы активируется и пытается подписать PWA на push-уведомления, Microsoft Edge вы запросит разрешение PWA показывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="b601e-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="b601e-224">Выберите **"Разрешить".**</span><span class="sxs-lookup"><span data-stu-id="b601e-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Диалоговое окно разрешений для включения уведомлений" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="b601e-226">Диалоговое окно разрешений для включения уведомлений</span><span class="sxs-lookup"><span data-stu-id="b601e-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="b601e-227">Имитация push-уведомлений на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b601e-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="b601e-228">Открыв PWA в браузере, выберите открытие `http://localhost:3000` `F12` DevTools.</span><span class="sxs-lookup"><span data-stu-id="b601e-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="b601e-229">Выберите **push-уведомления**для сотрудников службы приложений, чтобы  >  \*\*\*\*  >  \*\*\*\* отправить тестовую push-уведомления в PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="b601e-230">Push-уведомление должно отображаться рядом с панелью задач.</span><span class="sxs-lookup"><span data-stu-id="b601e-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push-уведомление от DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="b601e-232">Push-уведомление от DevTools</span><span class="sxs-lookup"><span data-stu-id="b601e-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="b601e-233">Если не выбрать всплывающее уведомление (или активировать\), система автоматически отключит его через несколько секунд и включит его в очередь в центре уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="b601e-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Уведомления в Центре уведомлений Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="b601e-235">Уведомления в Центре уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="b601e-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="b601e-236">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b601e-236">Next steps</span></span>  

<span data-ttu-id="b601e-237">Следующие действия включают дополнительные задачи, которые помогут вам понять создание реальных pwAs.</span><span class="sxs-lookup"><span data-stu-id="b601e-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="b601e-238">Управление push-подписками и их хранение</span><span class="sxs-lookup"><span data-stu-id="b601e-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="b601e-239">[Шифрование][NPMWebPushEncrypt] данных полезной нагрузки</span><span class="sxs-lookup"><span data-stu-id="b601e-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="b601e-240">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="b601e-240">Responsive design</span></span>  
*   <span data-ttu-id="b601e-241">Глубокое связывание</span><span class="sxs-lookup"><span data-stu-id="b601e-241">Deep-linking</span></span>  
*   [<span data-ttu-id="b601e-242">Тестирование в разных браузерах</span><span class="sxs-lookup"><span data-stu-id="b601e-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="b601e-243">Реализация методик проверки и тестирования, таких как [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="b601e-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <span data-ttu-id="b601e-244">См. также</span><span class="sxs-lookup"><span data-stu-id="b601e-244">See also</span></span>  

*   [<span data-ttu-id="b601e-245">Прогрессивное веб-приложение в веб-документы MDN</span><span class="sxs-lookup"><span data-stu-id="b601e-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="b601e-246">Прогрессивное веб-приложение на веб-сайте web.dev</span><span class="sxs-lookup"><span data-stu-id="b601e-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="b601e-247">[Читатели новостей Хакера как прогрессивное веб-приложение][HackerNewsProgressiveWebApps] — сравнивают различные структуры и шаблоны производительности для реализации примера \(Читателя новостей хакера\) PWA.</span><span class="sxs-lookup"><span data-stu-id="b601e-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="b601e-248">Захиминг (PwAs)</span><span class="sxs-lookup"><span data-stu-id="b601e-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="b601e-249">Прогрессивное движение для прогрессивного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b601e-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="b601e-250">Автономные POS-карты с прогрессивной веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="b601e-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="b601e-251">Вопросы и&PWA</span><span class="sxs-lookup"><span data-stu-id="b601e-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="b601e-252">Подавка в Интернете</span><span class="sxs-lookup"><span data-stu-id="b601e-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="b601e-253">Именовка прогрессивного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b601e-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="b601e-254">Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)</span><span class="sxs-lookup"><span data-stu-id="b601e-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="b601e-255">Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)</span><span class="sxs-lookup"><span data-stu-id="b601e-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="b601e-256">Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)</span><span class="sxs-lookup"><span data-stu-id="b601e-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание Node.js в Azure с помощью Visual Studio кода | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "Вопросы и&PWA"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивное движение для прогрессивного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Захиминг PWAs — новый выпуск Edge Edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Генератор экспресс-приложений | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Именовка прогрессивного веб-приложения"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивного веб-приложения"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Подавка в Интернете"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивное веб-приложение \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочих служб | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование сотрудников служб | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные POS-карты с прогрессивной веб-приложениями"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений WebPush с помощью службы push-уведомлений Mozilla | Службы Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивное веб-приложение"  

[PwaBuilder]: https://www.pwabuilder.com "Построитель PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Построитель PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorkerBook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание прогрессивного веб-приложения без структуры (часть 3)"  

[VapidkeysMain]: https://vapidkeys.com "Безопасный генератор ключей VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивное веб-приложение | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивное улучшение | Википедия"  
