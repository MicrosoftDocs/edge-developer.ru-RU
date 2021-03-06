---
description: В этом руководстве представлен обзор основ и средств PWA для создания прогрессивных веб-приложений (Chromium) в Windows.
title: Начало работы с прогрессивными веб-приложениями (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, Edge, Windows, PWABuilder, веб-манифест, работник службы, push
ms.openlocfilehash: 6ff24b2e9219b2f3755bb2e8f6db137dc7a721ec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398135"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a><span data-ttu-id="cac62-104">Начало работы с прогрессивными веб-приложениями (Chromium)</span><span class="sxs-lookup"><span data-stu-id="cac62-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="cac62-105">Прогрессивные веб-приложения \(PWAs\) — это веб-приложения, которые [постепенно улучшаются.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="cac62-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="cac62-106">Прогрессивные усовершенствования включают такие функции, как установка, поддержка в автономном режиме и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="cac62-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="cac62-107">Вы также можете упаковть PWA для магазинов приложений.</span><span class="sxs-lookup"><span data-stu-id="cac62-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="cac62-108">Возможные магазины приложений включают магазины Microsoft Store, Google Play, Mac App Store и другие.</span><span class="sxs-lookup"><span data-stu-id="cac62-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="cac62-109">Microsoft Store — это коммерческий магазин приложений, встроенный в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cac62-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="cac62-110">В следующем руководстве представлен обзор основ PWA, создав простое веб-приложение и расширив его как PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="cac62-111">Готовый проект работает в современных браузерах.</span><span class="sxs-lookup"><span data-stu-id="cac62-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="cac62-112">Вы можете использовать [PWABuilder][PwaBuilder] для создания новой PWA, улучшения существующего PWA или пакета PWA для магазинов приложений.</span><span class="sxs-lookup"><span data-stu-id="cac62-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="cac62-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="cac62-113">Prerequisites</span></span>  

*   <span data-ttu-id="cac62-114">Используйте [Visual Studio код,][VisualstudioCodeMain] чтобы изменить исходный код PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="cac62-115">Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="cac62-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <a name="create-a-basic-web-app"></a><span data-ttu-id="cac62-116">Создание базового веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cac62-116">Create a basic web app</span></span>  

<span data-ttu-id="cac62-117">Чтобы создать пустое веб-приложение, выполните действия в [Node Express App Generator][ExpressjsApplicationGenerator]и назовите ваше `MySamplePwa` приложение.</span><span class="sxs-lookup"><span data-stu-id="cac62-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="cac62-118">В запросе запустите следующие команды.</span><span class="sxs-lookup"><span data-stu-id="cac62-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="cac62-119">Команды создают пустое веб-приложение и устанавливают любые зависимости.</span><span class="sxs-lookup"><span data-stu-id="cac62-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="cac62-120">Теперь у вас есть простое функциональное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="cac62-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="cac62-121">Чтобы запустить веб-приложение, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="cac62-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="cac62-122">Теперь `http://localhost:3000` просмотрите, чтобы просмотреть новое веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="cac62-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск нового PWA на локальном сайте" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="cac62-124">Запуск нового PWA на локальном сайте</span><span class="sxs-lookup"><span data-stu-id="cac62-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <a name="get-started-building-a-pwa"></a><span data-ttu-id="cac62-125">Начало создания PWA</span><span class="sxs-lookup"><span data-stu-id="cac62-125">Get started building a PWA</span></span>  

<span data-ttu-id="cac62-126">Теперь, когда у вас есть простое веб-приложение, расширь его как PWA, добавив три требования к PWAs</span><span class="sxs-lookup"><span data-stu-id="cac62-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="cac62-127">: [HTTPS,](#step-1---use-https) [манифест веб-приложения](#step-2---create-a-web-app-manifest)и [сотрудник службы](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="cac62-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <a name="step-1---use-https"></a><span data-ttu-id="cac62-128">Шаг 1 — использование HTTPS</span><span class="sxs-lookup"><span data-stu-id="cac62-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="cac62-129">Ключевые части платформы PWA, такие как [Service Workers,][MDNServiceWorkerApi]требуют использования HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cac62-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="cac62-130">Когда PWA переходит в прямой эфир, необходимо опубликовать его на URL-адрес HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cac62-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="cac62-131">Для отладки Microsoft Edge также разрешает использовать `http://localhost` API PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="cac62-132">[Опубликуйте свое веб-приложение как живой сайт,][VisualStudioNodejsTutorialPublishAzureAppService]но убедитесь, что сервер настроен для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cac62-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="cac62-133">Например, можно создать свободную учетную запись [Azure.][AzureCreateFreeAccount]</span><span class="sxs-lookup"><span data-stu-id="cac62-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="cac62-134">Хост-сайт в [Службе приложений Microsoft Azure,][AzureWebApps] и по умолчанию он обслуживается через HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cac62-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="cac62-135">Следующее руководство, используйте `http://localhost` для создания PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <a name="step-2---create-a-web-app-manifest"></a><span data-ttu-id="cac62-136">Шаг 2 . Создание манифеста веб-приложений</span><span class="sxs-lookup"><span data-stu-id="cac62-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="cac62-137">Манифест [веб-приложения][MDNWebAppManifest] — это файл JSON, содержащий метаданные о вашем приложении, такие как имя, описание, значки и другие.</span><span class="sxs-lookup"><span data-stu-id="cac62-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="cac62-138">Добавление манифеста приложения в веб-приложение:</span><span class="sxs-lookup"><span data-stu-id="cac62-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="cac62-139">В Visual Studio коде выберите **папку File**Open и выберите созданный ранее  >  \*\*\*\* `MySamplePwa` каталог.</span><span class="sxs-lookup"><span data-stu-id="cac62-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="cac62-140">Выберите, `Ctrl` + `N` чтобы создать новый файл, и ввести в следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="cac62-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="cac62-141">Сохраните файл как `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="cac62-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="cac62-142">Добавьте изображение значка приложения 512x512 с `icon512.png` именем `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="cac62-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="cac62-143">Пример изображения можно [использовать для][ImagePwa] тестирования.</span><span class="sxs-lookup"><span data-stu-id="cac62-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="cac62-144">В Visual Studio Код откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.</span><span class="sxs-lookup"><span data-stu-id="cac62-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a><span data-ttu-id="cac62-145">Шаг 3 . Добавление сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="cac62-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="cac62-146">Сотрудники службы являются ключевой технологией pwAs, позволяющей использовать такие сценарии, как поддержка в автономном режиме, расширенный кэшинг и выполнение фоновых задач, ранее ограниченных для родных приложений.</span><span class="sxs-lookup"><span data-stu-id="cac62-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="cac62-147">Сотрудники служб — это фоновые задачи, перехватыватели сетевых запросов из вашего веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cac62-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="cac62-148">Сотрудники службы пытаются выполнить задачи, даже если ваш PWA не запущен.</span><span class="sxs-lookup"><span data-stu-id="cac62-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="cac62-149">Задачи включают следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cac62-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="cac62-150">Обслуживание запрашиваемых ресурсов из кэша</span><span class="sxs-lookup"><span data-stu-id="cac62-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="cac62-151">Отправка push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="cac62-151">Sending push notifications</span></span>  
*   <span data-ttu-id="cac62-152">Выполнение задач фонового получения</span><span class="sxs-lookup"><span data-stu-id="cac62-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="cac62-153">Значки badging</span><span class="sxs-lookup"><span data-stu-id="cac62-153">Badging icons</span></span>  
*   <span data-ttu-id="cac62-154">и больше</span><span class="sxs-lookup"><span data-stu-id="cac62-154">and more</span></span>  
    
<span data-ttu-id="cac62-155">Сотрудники служб определяются в специальном файле JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cac62-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="cac62-156">Дополнительные сведения можно получить в [API Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API.][MDNServiceWorkerApi]</span><span class="sxs-lookup"><span data-stu-id="cac62-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="cac62-157">Чтобы создать сотрудника службы в проекте, используйте рецепт сотрудника сетевой службы **Cache-first** от [PWA Builder.][PwaBuilderServiceWorker]</span><span class="sxs-lookup"><span data-stu-id="cac62-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="cac62-158">Перейдите [pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]выберите сотрудника сетевой службы **Cache-first** и выберите кнопку **Загрузка.**</span><span class="sxs-lookup"><span data-stu-id="cac62-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="cac62-159">Загруженный файл содержит следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="cac62-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="cac62-160">Скопируйте загруженные файлы в `public` папку в проекте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="cac62-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="cac62-161">В Visual Studio коде откройте и добавьте в тег следующий фрагмент `/public/index.html` `<head>` кода.</span><span class="sxs-lookup"><span data-stu-id="cac62-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="cac62-162">Теперь в вашем веб-приложении есть сотрудник службы, использующий стратегию кэш-первого.</span><span class="sxs-lookup"><span data-stu-id="cac62-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="cac62-163">Сначала новый сотрудник службы извлекает ресурсы из кэша и из сети только по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="cac62-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="cac62-164">Кэшные ресурсы включают изображения, JavaScript, CSS и HTML.</span><span class="sxs-lookup"><span data-stu-id="cac62-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="cac62-165">Чтобы подтвердить, что выполняется рабочий службы, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cac62-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="cac62-166">Перейдите к веб-приложению с помощью `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="cac62-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="cac62-167">Если ваше веб-приложение не доступно, запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="cac62-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="cac62-168">В Microsoft Edge выберите `F12` для открытия Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cac62-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="cac62-169">Выберите **приложение,** а затем **сотрудников службы,** чтобы просмотреть сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="cac62-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="cac62-170">Если сотрудник службы не отображается, обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="cac62-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Обзор сотрудника службы Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="cac62-172">Обзор сотрудника службы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cac62-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="cac62-173">Просмотр кэша сотрудника службы путем расширения **хранилища кэша** и выбора **pwabuilder-precache.**</span><span class="sxs-lookup"><span data-stu-id="cac62-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="cac62-174">Все ресурсы, кэшные работником службы, должны отображаться.</span><span class="sxs-lookup"><span data-stu-id="cac62-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="cac62-175">Ресурсы, кэшные работником службы, включают значок приложения, манифест приложения, CSS и файлы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cac62-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Кэш сотрудника службы в Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="cac62-177">Кэш сотрудника службы в Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="cac62-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="cac62-178">Попробуйте PWA как автономное приложение.</span><span class="sxs-lookup"><span data-stu-id="cac62-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="cac62-179">В Microsoft Edge DevTools `F12` \( \) выберите **Сеть,** а затем измените состояние **Online** в **автономном режиме.**</span><span class="sxs-lookup"><span data-stu-id="cac62-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Настройка приложения в автономном режиме в Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="cac62-181">Настройка приложения в автономном режиме в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cac62-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="cac62-182">Обновите приложение и отобразите автономный механизм обслуживания ресурсов приложения из кэша.</span><span class="sxs-lookup"><span data-stu-id="cac62-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Запуск PWA в автономном режиме" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="cac62-184">Запуск PWA в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="cac62-184">PWA running offline</span></span>
    :::image-end:::
    
## <a name="add-push-notifications-to-your-pwa"></a><span data-ttu-id="cac62-185">Добавление push-уведомлений в PWA</span><span class="sxs-lookup"><span data-stu-id="cac62-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="cac62-186">Вы можете создать PWAs, поддерживаюющие push-уведомления, выполняя следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="cac62-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="cac62-187">Подписка на службу обмена сообщениями с помощью [API Push][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="cac62-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="cac62-188">Отображение всплывающее сообщение при получении сообщения из службы с помощью [API уведомлений][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="cac62-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="cac62-189">Как и у сотрудников службы, API push-уведомлений являются API на основе стандартов.</span><span class="sxs-lookup"><span data-stu-id="cac62-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="cac62-190">API push-уведомлений работают в браузерах, поэтому код должен работать везде, где поддерживаются PWAs.</span><span class="sxs-lookup"><span data-stu-id="cac62-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="cac62-191">Дополнительные сведения о доставке push-сообщений в различные браузеры на сервере перейдите в [Web-Push.][NPMWebPush]</span><span class="sxs-lookup"><span data-stu-id="cac62-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="cac62-192">Следующие действия были адаптированы из книги "Push Rich Demo in [Service Worker Cookbook",][ServiceWorkerCookbookPushRichDemo] предоставленной Mozilla, которая имеет ряд других полезных рецептов веб-push и рабочих служб.</span><span class="sxs-lookup"><span data-stu-id="cac62-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <a name="step-1---generate-vapid-keys"></a><span data-ttu-id="cac62-193">Шаг 1 . Создание ключей VAPID</span><span class="sxs-lookup"><span data-stu-id="cac62-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="cac62-194">Push-уведомления требуют ключей VAPID \(Добровольная идентификация сервера приложений\) для отправки push-сообщений клиенту PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="cac62-195">Существует несколько генераторов ключей VAPID, доступных в Интернете \(например, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="cac62-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="cac62-196">После генерации необходимо получить объект JSON, содержащий общедоступный и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="cac62-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="cac62-197">Сохраните ключи для последующих действий в следующем учебнике.</span><span class="sxs-lookup"><span data-stu-id="cac62-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="cac62-198">Сведения о VAPID и WebPush перейдите к отправке [выявленных веб-уведомлений веб-приложения VAPID с помощью push-службы Mozilla.][MozillaServicesSendingVapidWebPushNotificationsPush]</span><span class="sxs-lookup"><span data-stu-id="cac62-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <a name="step-2---subscribe-to-push-notifications"></a><span data-ttu-id="cac62-199">Шаг 2 . Подписка на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="cac62-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="cac62-200">Сотрудники служб обрабатывают push-события и взаимодействие уведомлений в PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="cac62-201">Чтобы подписаться на PWA на push-уведомления сервера, убедитесь, что следующие условия выполнены.</span><span class="sxs-lookup"><span data-stu-id="cac62-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="cac62-202">Ваш PWA установлен, активен и зарегистрирован</span><span class="sxs-lookup"><span data-stu-id="cac62-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="cac62-203">Код для выполнения задачи подписки находится в основном потоке пользовательского интерфейса PWA</span><span class="sxs-lookup"><span data-stu-id="cac62-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="cac62-204">Подключение к сети</span><span class="sxs-lookup"><span data-stu-id="cac62-204">You have network connectivity</span></span>  
    
<span data-ttu-id="cac62-205">Перед тем как создать новую push-подписку, Microsoft Edge проверяет, предоставил ли пользователь разрешение PWA на получение уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cac62-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="cac62-206">Если нет, пользователь получает запрос от браузера на разрешение.</span><span class="sxs-lookup"><span data-stu-id="cac62-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="cac62-207">Если разрешение отказано, запрос на `registration.pushManager.subscribe` бросок `DOMException` , который должен быть обработан.</span><span class="sxs-lookup"><span data-stu-id="cac62-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="cac62-208">Дополнительные информации об управлении разрешениями перейдите к [push-уведомлениям в Microsoft Edge.][WindowsBlogsWebNotificationsEdge]</span><span class="sxs-lookup"><span data-stu-id="cac62-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="cac62-209">В `pwabuilder-sw-register.js` файле задайте следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="cac62-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="cac62-210">Дополнительные сведения перейдите в [PushManager][MDNPushManager] и [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="cac62-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <a name="step-3---listen-for-push-notifications"></a><span data-ttu-id="cac62-211">Шаг 3 . Прослушивание push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="cac62-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="cac62-212">После создания подписки в PWA добавьте обработчики для реагирования на события push-службы.</span><span class="sxs-lookup"><span data-stu-id="cac62-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="cac62-213">Push-событие отправляется с сервера для отображения всплывающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="cac62-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="cac62-214">В всплывающих уведомлениях отображаются данные для полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="cac62-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="cac62-215">Чтобы выполнить следующие задачи, необходимо добавить `click` обработник.</span><span class="sxs-lookup"><span data-stu-id="cac62-215">To complete the following tasks, you must add a `click` handler.</span></span>  

*   <span data-ttu-id="cac62-216">Отклонение уведомления всплывающих уведомлений</span><span class="sxs-lookup"><span data-stu-id="cac62-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="cac62-217">Откройте, сосредоточьте или откройте все открытые окна и сосредоточьте их</span><span class="sxs-lookup"><span data-stu-id="cac62-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="cac62-218">Откройте и сосредоточьте новое окно для отображения клиентской страницы PWA</span><span class="sxs-lookup"><span data-stu-id="cac62-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="cac62-219">В файл `pwabuilder-sw.js` добавьте следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="cac62-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <a name="step-4---try-it-out"></a><span data-ttu-id="cac62-220">Шаг 4 . Попробуйте его</span><span class="sxs-lookup"><span data-stu-id="cac62-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="cac62-221">Чтобы протестировать push-уведомления для PWA, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cac62-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="cac62-222">Перейдите к вашему PWA по `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="cac62-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="cac62-223">Когда сотрудник службы активируется и пытается подписаться на PWA для push-уведомлений, Microsoft Edge подсказывает вам разрешить PWA показывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="cac62-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="cac62-224">Выберите **Разрешить**.</span><span class="sxs-lookup"><span data-stu-id="cac62-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Диалоговое окно разрешений для включения уведомлений" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="cac62-226">Диалоговое окно разрешений для включения уведомлений</span><span class="sxs-lookup"><span data-stu-id="cac62-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="cac62-227">Имитация push-уведомления на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="cac62-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="cac62-228">Чтобы открыть PWA в `http://localhost:3000` браузере, выберите `F12` для открытия DevTools.</span><span class="sxs-lookup"><span data-stu-id="cac62-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="cac62-229">Выберите \*\*\*\*  >  **push-сообщение**  >  **сотрудника службы приложений,** чтобы отправить тест-push-уведомление в службу PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="cac62-230">Push-уведомление должно отображаться рядом с панелью задач.</span><span class="sxs-lookup"><span data-stu-id="cac62-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Push a notification from DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="cac62-232">Push a notification from DevTools</span><span class="sxs-lookup"><span data-stu-id="cac62-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="cac62-233">Если вы не выбираете \(или активируете\) всплывающее уведомление, система автоматически отключает его через несколько секунд и выстроит очередь в центре действий Windows.</span><span class="sxs-lookup"><span data-stu-id="cac62-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Уведомления в Центре действий Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="cac62-235">Уведомления в Центре действий Windows</span><span class="sxs-lookup"><span data-stu-id="cac62-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="cac62-236">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cac62-236">Next steps</span></span>  

<span data-ttu-id="cac62-237">Следующие действия включают дополнительные задачи, которые помогут вам понять создание pwAs в реальном мире.</span><span class="sxs-lookup"><span data-stu-id="cac62-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="cac62-238">Управление подписками push и хранение</span><span class="sxs-lookup"><span data-stu-id="cac62-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="cac62-239">[Шифрование][NPMWebPushEncrypt] данных полезной нагрузки</span><span class="sxs-lookup"><span data-stu-id="cac62-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="cac62-240">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="cac62-240">Responsive design</span></span>  
*   <span data-ttu-id="cac62-241">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="cac62-241">Deep-linking</span></span>  
*   [<span data-ttu-id="cac62-242">Тестирование кросс-браузера</span><span class="sxs-lookup"><span data-stu-id="cac62-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="cac62-243">Реализация практик проверки и тестирования, таких как [Webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="cac62-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="cac62-244">См. также</span><span class="sxs-lookup"><span data-stu-id="cac62-244">See also</span></span>  

*   [<span data-ttu-id="cac62-245">Прогрессивные веб-приложения в веб-docs MDN</span><span class="sxs-lookup"><span data-stu-id="cac62-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="cac62-246">Прогрессивные веб-приложения на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="cac62-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="cac62-247">[Читатели новостей][HackerNewsProgressiveWebApps] хакеров как прогрессивные веб-приложения — сравнивает различные структуры и шаблоны производительности для реализации примера \(Hacker News reader\) PWA.</span><span class="sxs-lookup"><span data-stu-id="cac62-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="cac62-248">Миф Busting PWAs</span><span class="sxs-lookup"><span data-stu-id="cac62-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="cac62-249">Прогрессивная дорожная карта для прогрессивного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="cac62-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="cac62-250">Автономные POS-карты с прогрессивными веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="cac62-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="cac62-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="cac62-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="cac62-252">Ставки в Интернете</span><span class="sxs-lookup"><span data-stu-id="cac62-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="cac62-253">Наименование прогрессивных веб-приложений</span><span class="sxs-lookup"><span data-stu-id="cac62-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="cac62-254">Проектирование и создание прогрессивного веб-приложения без рамок (часть 1)</span><span class="sxs-lookup"><span data-stu-id="cac62-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="cac62-255">Проектирование и создание прогрессивного веб-приложения без рамок (часть 2)</span><span class="sxs-lookup"><span data-stu-id="cac62-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="cac62-256">Проектирование и создание прогрессивного веб-приложения без рамок (часть 3)</span><span class="sxs-lookup"><span data-stu-id="cac62-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание приложения Node.js в Azure с Visual Studio кодом | Документы Майкрософт"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создание бесплатной учетной записи Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft Edge в Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Прогрессивная дорожная карта для прогрессивного веб-приложения"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "Миф Busting PWAs — новое edge edition"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Экспресс-генератор приложений | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Наименование прогрессивных веб-приложений"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Читатели новостей хакеров в качестве прогрессивных веб-приложений"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Ставки в Интернете"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивные веб-приложения \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Push API | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API API для сотрудников службы | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Использование рабочих | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Автономные POS-карты с прогрессивными веб-приложениями"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка уведомлений webPush с помощью службы push-службы Mozilla | Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "веб-push-| npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) — веб-| NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование — веб-| NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивные веб-приложения"  

[PwaBuilder]: https://www.pwabuilder.com "Строитель PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Работник службы | Строитель PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | Поваренная книга ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Проектирование и создание прогрессивного веб-приложения без рамок (часть 3)"  

[VapidkeysMain]: https://vapidkeys.com "Безопасный генератор ключей VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивные веб-приложения | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Прогрессивная | Википедия"  
