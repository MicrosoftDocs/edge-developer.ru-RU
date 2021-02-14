---
description: Обзор создания и публикации расширений Microsoft Edge (Chromium).
title: Обзор расширений Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, разработка расширений, расширения браузера, надстройки, Центр партнеров, разработчик, расширения chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327528"
---
# <span data-ttu-id="8ae04-104">Обзор расширений Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="8ae04-104">Overview of Microsoft Edge (Chromium) Extensions</span></span>  

<span data-ttu-id="8ae04-105">Расширение — это небольшая программа, которую вы \(разработчик\) используете для добавления или изменения компонентов Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="8ae04-105">An extension is a small program that you \(a developer\) use to add or modify features for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="8ae04-106">Расширение предназначено для улучшения ежедневного просмотра пользователем.</span><span class="sxs-lookup"><span data-stu-id="8ae04-106">An extension is intended to improve a user's day-to-day browsing experience.</span></span>  <span data-ttu-id="8ae04-107">Он предоставляет нишевые функции, важные для целевой аудитории.</span><span class="sxs-lookup"><span data-stu-id="8ae04-107">It provides niche functionality that is important to a target audience.</span></span>  

<span data-ttu-id="8ae04-108">Вы можете создать расширение, если у вас есть идея или продукт, основанный на любом из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="8ae04-108">You may create an extension if you have an idea or product that is based upon either of the following conditions.</span></span>  

*   <span data-ttu-id="8ae04-109">Определенный веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="8ae04-109">A specific web browser.</span></span>  
*   <span data-ttu-id="8ae04-110">Усовершенствования функций определенных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="8ae04-110">Improvements to features of specific webpages.</span></span>  
    
<span data-ttu-id="8ae04-111">К примерам сопутствующих проектов относятся блокаторы и диспетчеры паролей.</span><span class="sxs-lookup"><span data-stu-id="8ae04-111">Examples of companion experiences include ad blockers and password managers.</span></span>  

<span data-ttu-id="8ae04-112">Расширение имеет структуру, аналогичную обычному веб-приложению.</span><span class="sxs-lookup"><span data-stu-id="8ae04-112">An extension is structured similar to a regular web app.</span></span>  <span data-ttu-id="8ae04-113">Как минимум, он должен включать следующие функции.</span><span class="sxs-lookup"><span data-stu-id="8ae04-113">At a minimum, it should include the following features.</span></span>

*   <span data-ttu-id="8ae04-114">JSON-файл манифеста приложения, содержащий базовые сведения о платформе.</span><span class="sxs-lookup"><span data-stu-id="8ae04-114">An app manifest JSON file that contains basic platform information.</span></span>  
*   <span data-ttu-id="8ae04-115">Файл JavaScript, который определяет функциональность.</span><span class="sxs-lookup"><span data-stu-id="8ae04-115">A JavaScript file that define functionality.</span></span>  
*   <span data-ttu-id="8ae04-116">HTML-файлы и CSS-файлы, которые определяют пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8ae04-116">HTML and CSS files that define the user interface.</span></span>  

<span data-ttu-id="8ae04-117">Чтобы работать непосредственно с веб-частью браузера, например с окном или вкладкой, необходимо отправлять запросы API и часто ссылаться на браузер по имени.</span><span class="sxs-lookup"><span data-stu-id="8ae04-117">To work directly with part of the browser, such as a window or tab, you must send API requests and often reference the browser by name.</span></span>  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Расширение Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  <span data-ttu-id="8ae04-119">Расширение Microsoft Edge \(Chromium\)</span><span class="sxs-lookup"><span data-stu-id="8ae04-119">A Microsoft Edge \(Chromium\) extension</span></span>  
:::image-end:::  

## <span data-ttu-id="8ae04-120">Базовое руководство</span><span class="sxs-lookup"><span data-stu-id="8ae04-120">Basic guidance</span></span>  

<span data-ttu-id="8ae04-121">Некоторые из самых популярных браузеров для создания расширений для: Safari, Firefox, Chrome, Opera, Чтобы создать и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8ae04-121">Some of the most popular browsers to build extensions for include Safari, Firefox, Chrome, Opera, Brave, and Microsoft Edge.</span></span>  <span data-ttu-id="8ae04-122">Отличные места для начала учебников по разработке расширений и изучения документации — это сайты, которые находятся в организациях браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-122">Great places to begin your extension development tutorials and documentation research are sites hosted by the browser organizations.</span></span>  <span data-ttu-id="8ae04-123">Следующая таблица не является точной и может использоваться в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="8ae04-123">The following table isn't definitive, and may be used as a starting point.</span></span>  

| <span data-ttu-id="8ae04-124">Браузер</span><span class="sxs-lookup"><span data-stu-id="8ae04-124">Web browser</span></span> | <span data-ttu-id="8ae04-125">На основе Chromium?</span><span class="sxs-lookup"><span data-stu-id="8ae04-125">Chromium-based?</span></span> | <span data-ttu-id="8ae04-126">Веб-страницы разработки расширений</span><span class="sxs-lookup"><span data-stu-id="8ae04-126">Extension development webpage</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="8ae04-127">Safari</span><span class="sxs-lookup"><span data-stu-id="8ae04-127">Safari</span></span> | <span data-ttu-id="8ae04-128">Нет</span><span class="sxs-lookup"><span data-stu-id="8ae04-128">No</span></span> | [<span data-ttu-id="8ae04-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span><span class="sxs-lookup"><span data-stu-id="8ae04-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span></span>][AppleDeveloperSafariservicesAppExtensions] |  
| <span data-ttu-id="8ae04-130">Firefox</span><span class="sxs-lookup"><span data-stu-id="8ae04-130">Firefox</span></span> | <span data-ttu-id="8ae04-131">Нет</span><span class="sxs-lookup"><span data-stu-id="8ae04-131">No</span></span> | [<span data-ttu-id="8ae04-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span><span class="sxs-lookup"><span data-stu-id="8ae04-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span></span>][MDNWebextensions] |  
| <span data-ttu-id="8ae04-133">Хром</span><span class="sxs-lookup"><span data-stu-id="8ae04-133">Chrome</span></span> | <span data-ttu-id="8ae04-134">Да</span><span class="sxs-lookup"><span data-stu-id="8ae04-134">Yes</span></span> | [<span data-ttu-id="8ae04-135">developer.chrome.com/extensions</span><span class="sxs-lookup"><span data-stu-id="8ae04-135">developer.chrome.com/extensions</span></span>][ChromeDeveloperExtensions] |  
| <span data-ttu-id="8ae04-136">Opera</span><span class="sxs-lookup"><span data-stu-id="8ae04-136">Opera</span></span> | <span data-ttu-id="8ae04-137">Да</span><span class="sxs-lookup"><span data-stu-id="8ae04-137">Yes</span></span> | [<span data-ttu-id="8ae04-138">dev.opera.com/extensions</span><span class="sxs-lookup"><span data-stu-id="8ae04-138">dev.opera.com/extensions</span></span>][OperaDevExtensions] |  
| <span data-ttu-id="8ae04-139">Сша</span><span class="sxs-lookup"><span data-stu-id="8ae04-139">Brave</span></span> | <span data-ttu-id="8ae04-140">Да</span><span class="sxs-lookup"><span data-stu-id="8ae04-140">Yes</span></span> | <span data-ttu-id="8ae04-141">Использование [веб-магазина Chrome][GoogleChromeWebstoreCategoryExtensions]</span><span class="sxs-lookup"><span data-stu-id="8ae04-141">Uses [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span></span> |  
| <span data-ttu-id="8ae04-142">новый Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ae04-142">new Microsoft Edge</span></span> | <span data-ttu-id="8ae04-143">Да</span><span class="sxs-lookup"><span data-stu-id="8ae04-143">Yes</span></span> | [<span data-ttu-id="8ae04-144">developer.microsoft.com/microsoft-edge/extensions</span><span class="sxs-lookup"><span data-stu-id="8ae04-144">developer.microsoft.com/microsoft-edge/extensions</span></span>][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> <span data-ttu-id="8ae04-145">Во многих учебниках сайтов используются API браузера, которые могут не совпадать с браузером, для которого вы разрабатываете.</span><span class="sxs-lookup"><span data-stu-id="8ae04-145">Many of the tutorials of the sites use browser-specific APIs that may not match the browser for which you develop.</span></span>  <span data-ttu-id="8ae04-146">В большинстве случаев расширение Chromium работает как есть в разных браузерах Chromium, а API работают ожидаемым образом.</span><span class="sxs-lookup"><span data-stu-id="8ae04-146">In most cases, a Chromium extension works as-is in different Chromium browsers and the APIs work as expected.</span></span>  <span data-ttu-id="8ae04-147">Только некоторые менее распространенные API могут быть строго специфическими для браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-147">Only some less common APIs may be strictly browser-specific.</span></span>  <span data-ttu-id="8ae04-148">Ссылки на учебники см. также в [этой ссылке.](#see-also)</span><span class="sxs-lookup"><span data-stu-id="8ae04-148">For links to the tutorials, navigate to [See also](#see-also).</span></span>  

## <span data-ttu-id="8ae04-149">Почему Chromium?</span><span class="sxs-lookup"><span data-stu-id="8ae04-149">Why Chromium?</span></span>  

<span data-ttu-id="8ae04-150">Если ваша цель — опубликовать расширение в хранилище расширений для каждого браузера, его необходимо изменить для каждой версии, чтобы оно было целевым и запускалось в каждой отдельной среде браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-150">If your goal is to publish your extension in the extensions store for each browser, it must be modified for each version to target and run in each distinct browser environment.</span></span>  <span data-ttu-id="8ae04-151">Например, расширения [Safari могут использовать][AppleDeveloperSafariservicesAppExtensions] как веб-, так и исходный код для взаимодействия с аналогами приложений.</span><span class="sxs-lookup"><span data-stu-id="8ae04-151">For example, [Safari extensions][AppleDeveloperSafariservicesAppExtensions] may use both web and native code to communicate with counterpart native applications.</span></span>  <span data-ttu-id="8ae04-152">Последние четыре браузера в предыдущей таблице используют один и тот же пакет кода и свести к минимуму требования к обслуживанию параллельных версий.</span><span class="sxs-lookup"><span data-stu-id="8ae04-152">The last four browsers in the previous table use the same code package, and minimizes the requirement to maintain parallel versions.</span></span>  <span data-ttu-id="8ae04-153">Эти браузеры основаны на проекте [Chromium с открытым исходным кодом.][|::ref1::|Home]</span><span class="sxs-lookup"><span data-stu-id="8ae04-153">These browsers are based on the [Chromium open-source project][|::ref1::|Home].</span></span>  

<span data-ttu-id="8ae04-154">Создайте расширение Chromium, чтобы написать наименьший объем кода.</span><span class="sxs-lookup"><span data-stu-id="8ae04-154">Create a Chromium extension to write the least amount of code.</span></span>  <span data-ttu-id="8ae04-155">Кроме того, он ориентирован на максимальное количество хранилищ расширений и максимальное количество пользователей, которые находят и приобретают ваше расширение.</span><span class="sxs-lookup"><span data-stu-id="8ae04-155">It also targets the maximum number of extension stores and ultimately the maximum number of users who find and acquire your extension.</span></span>  

<span data-ttu-id="8ae04-156">Следующее содержимое в основном посвящено расширениям Chromium.</span><span class="sxs-lookup"><span data-stu-id="8ae04-156">The following content focuses mostly on Chromium extensions.</span></span>  

## <span data-ttu-id="8ae04-157">Совместимость браузеров и тестирование расширений</span><span class="sxs-lookup"><span data-stu-id="8ae04-157">Browser compatibility and extension testing</span></span>  

<span data-ttu-id="8ae04-158">Иногда четность API не существует между браузерами Chromium.</span><span class="sxs-lookup"><span data-stu-id="8ae04-158">Occasionally, API parity doesn't exist between Chromium browsers.</span></span>  <span data-ttu-id="8ae04-159">Например, существуют различия в API удостоверений и платежей.</span><span class="sxs-lookup"><span data-stu-id="8ae04-159">For example, there are differences in the identity and payment APIs.</span></span>  <span data-ttu-id="8ae04-160">Чтобы убедиться, что расширение соответствует ожиданиям клиентов, просмотрите состояние API с помощью следующих официальных документы браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-160">To ensure your extension meets customer expectations, review API status through the following official browser docs.</span></span>  

*   [<span data-ttu-id="8ae04-161">API Chrome</span><span class="sxs-lookup"><span data-stu-id="8ae04-161">Chrome APIs</span></span>][ChromeDeveloperExtensionsApiIndex]  
*   [<span data-ttu-id="8ae04-162">API расширения, поддерживаемые в Opera</span><span class="sxs-lookup"><span data-stu-id="8ae04-162">Extension APIs supported in Opera</span></span>][OperaDevExtensionsApis]  
*   [<span data-ttu-id="8ae04-163">Перенос расширения Chrome в Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="8ae04-163">Port Chrome extension to Microsoft Edge (Chromium)</span></span>][ExtensionsChromiumDeveloperGuidePortChrome]  
    
<span data-ttu-id="8ae04-164">Необходимые API определяют изменения, которые необходимо внести для устранения различий между каждым браузером.</span><span class="sxs-lookup"><span data-stu-id="8ae04-164">The APIs you require define the changes you must make to address the differences between each browser.</span></span>  <span data-ttu-id="8ae04-165">Это может означать, что необходимо создать несколько разные пакеты кода с небольшими отличиями для каждого магазина.</span><span class="sxs-lookup"><span data-stu-id="8ae04-165">It may mean that you must create slightly different code packages with small differences for each store.</span></span>  

<span data-ttu-id="8ae04-166">Чтобы протестировать расширение в различных средах перед отправкой в хранилище браузера, разгрузите его в браузер во время разработки.</span><span class="sxs-lookup"><span data-stu-id="8ae04-166">To test your extension in different environments before you submit it to a browser store, sideload it into your browser while you develop it.</span></span>  

## <span data-ttu-id="8ae04-167">Публикация расширения в хранилищах браузера</span><span class="sxs-lookup"><span data-stu-id="8ae04-167">Publish your extension to browser stores</span></span>  

<span data-ttu-id="8ae04-168">Вы можете отправлять расширения браузера и искать их в следующих хранилищах браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-168">You may submit and seek browser extensions in the following browser stores.</span></span>  

*   [<span data-ttu-id="8ae04-169">Надстройки браузера Firefox</span><span class="sxs-lookup"><span data-stu-id="8ae04-169">Firefox Browser Add-ons</span></span>][MozillaAddonsFirefoxExtensions]  
*   [<span data-ttu-id="8ae04-170">Веб-магазин Chrome</span><span class="sxs-lookup"><span data-stu-id="8ae04-170">Chrome Web Store</span></span>][GoogleChromeWebstoreCategoryExtensions]  
*   [<span data-ttu-id="8ae04-171">Надстройки оперы</span><span class="sxs-lookup"><span data-stu-id="8ae04-171">Opera addons</span></span>][OperaAddonsExtensions]  
*   [<span data-ttu-id="8ae04-172">Надстройки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ae04-172">Microsoft Edge Add-ons</span></span>][MicrosoftEdgeAddonsCategoryExtensions]  

<span data-ttu-id="8ae04-173">Некоторые магазины позволяют скачивать перечисленные расширения из других браузеров.</span><span class="sxs-lookup"><span data-stu-id="8ae04-173">Some stores allow you to download listed extensions from other browsers.</span></span>  <span data-ttu-id="8ae04-174">Однако хранилища браузеров не гарантируют доступ к браузерам.</span><span class="sxs-lookup"><span data-stu-id="8ae04-174">However, cross-browser access is not guaranteed by browser stores.</span></span>  <span data-ttu-id="8ae04-175">Чтобы пользователи могли найти ваше расширение в разных браузерах, необходимо сохранить описание в каждом хранилище расширений браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-175">To ensure your users find your extension in different browsers, you should maintain a listing on each browser extension store.</span></span>  

<span data-ttu-id="8ae04-176">Пользователям может потребоваться установить расширение в разных браузерах.</span><span class="sxs-lookup"><span data-stu-id="8ae04-176">Users may need to install your extension in different browsers.</span></span> <span data-ttu-id="8ae04-177">В этом сценарии можно перенести существующие расширения Chromium из одного браузера в другой.</span><span class="sxs-lookup"><span data-stu-id="8ae04-177">In this scenario, you may migrate existing Chromium extensions from one browser to another.</span></span>  

### <span data-ttu-id="8ae04-178">Перенос существующего расширения в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ae04-178">Migrate an existing extension to Microsoft Edge</span></span>  

<span data-ttu-id="8ae04-179">Если вы уже разработали расширение для другого браузера Chromium, вы можете отправить его в магазин надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8ae04-179">If you've already developed an extension for another Chromium browser, you may submit it to the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="8ae04-180">Вам не нужно переописывать расширение и убедитесь, что оно работает в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8ae04-180">You don't need to rewrite your extension, and must verify it works in Microsoft Edge.</span></span>  <span data-ttu-id="8ae04-181">При переносе существующего расширения Chromium в другие браузеры Chromium убедитесь, что те же API или альтернативы доступны для вашего целевого браузера.</span><span class="sxs-lookup"><span data-stu-id="8ae04-181">When you migrate an existing Chromium extension to other Chromium browsers, ensure the same APIs or alternatives are available for your target browser.</span></span>  

<span data-ttu-id="8ae04-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span><span class="sxs-lookup"><span data-stu-id="8ae04-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span></span> <span data-ttu-id="8ae04-183">После переноса расширения в целевой браузер необходимо опубликовать его.</span><span class="sxs-lookup"><span data-stu-id="8ae04-183">After you port your extension to the target browser, the next step is to publish it.</span></span>  

### <span data-ttu-id="8ae04-184">Публикация на веб-сайте надстройки Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8ae04-184">Publish to the Microsoft Edge add-ons website</span></span>  

<span data-ttu-id="8ae04-185">Чтобы начать публикацию расширения в Microsoft [][MicrosoftDeveloperRegistration] Edge, необходимо зарегистрировать учетную запись разработчика с учетной записью электронной почты MSA, чтобы отправить описание расширения в Магазин.</span><span class="sxs-lookup"><span data-stu-id="8ae04-185">To start publishing your extension to Microsoft Edge, you must [register for a developer account][MicrosoftDeveloperRegistration] with an MSA email account to submit your extension listing to the store.</span></span>  <span data-ttu-id="8ae04-186">Учетная запись электронной почты MSA включает `@outlook.com` `@live.com` и т. д.</span><span class="sxs-lookup"><span data-stu-id="8ae04-186">An MSA email account includes `@outlook.com`, `@live.com`, and so on.</span></span>  <span data-ttu-id="8ae04-187">При выборе адреса электронной почты для регистрации рассмотрите возможность передачи или передачи прав владельца расширения другим лицам в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8ae04-187">When you choose an email address to register, consider if you must transfer or share ownership of the extension with others in your organization.</span></span>  <span data-ttu-id="8ae04-188">После завершения регистрации вы можете создать новую отправку расширения в магазин.</span><span class="sxs-lookup"><span data-stu-id="8ae04-188">After registration is complete, you may create a new extension submission to the store.</span></span>  

<span data-ttu-id="8ae04-189">Чтобы отправить расширение в Магазин, убедитесь, что вы предоставили следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="8ae04-189">To submit your extension to the store, ensure you provide the following items.</span></span>  

*   <span data-ttu-id="8ae04-190">Архивный \( `.zip` \) файл, содержащий файлы кода.</span><span class="sxs-lookup"><span data-stu-id="8ae04-190">An archive \(`.zip`\) file that contains your code files.</span></span>  
*   <span data-ttu-id="8ae04-191">Все необходимые визуальные ресурсы, включая логотип и небольшую рекламную плитку.</span><span class="sxs-lookup"><span data-stu-id="8ae04-191">All required visual assets, which include a logo and small promotional tile.</span></span>  
*   <span data-ttu-id="8ae04-192">Необязательный рекламный носиттель, например снимки экрана, рекламные плитки и URL-адрес видео.</span><span class="sxs-lookup"><span data-stu-id="8ae04-192">Optional promotional media, such as screenshots, promotional tiles, and a video URL.</span></span>  
*   <span data-ttu-id="8ae04-193">Сведения о расширении, такие как имя, краткое описание и ссылка на политику конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="8ae04-193">Information that describes your extension such as the name, short description, and a privacy policy link.</span></span>  

> [!NOTE]
> <span data-ttu-id="8ae04-194">У разных хранилищ могут быть разные требования к отправке.</span><span class="sxs-lookup"><span data-stu-id="8ae04-194">Different stores may have different submission requirements.</span></span>  <span data-ttu-id="8ae04-195">В списке выше приводится перечень [требований][ExtensionsChromiumPublish] для публикации расширения для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8ae04-195">The above list summarizes the [requirements][ExtensionsChromiumPublish] to publish an extension for Microsoft Edge.</span></span>  

<span data-ttu-id="8ae04-196">После успешной отправки расширения расширение проходит проверку и проходит или не проходит сертификацию.</span><span class="sxs-lookup"><span data-stu-id="8ae04-196">After you've successfully submitted your extension, your extension undergoes a review process and either passes or fails the certification process.</span></span>  <span data-ttu-id="8ae04-197">Владельцы уведомлены о результатах и при необходимости выдаются дальнейшие действия.</span><span class="sxs-lookup"><span data-stu-id="8ae04-197">Owners are notified of the outcome and given next steps as required.</span></span>  <span data-ttu-id="8ae04-198">При отправке обновления расширения в Магазин начинается новый процесс проверки.</span><span class="sxs-lookup"><span data-stu-id="8ae04-198">If you submit an extension update to the store, a new review process is started.</span></span>  

## <span data-ttu-id="8ae04-199">См. также</span><span class="sxs-lookup"><span data-stu-id="8ae04-199">See also</span></span>  

*   [<span data-ttu-id="8ae04-200">Перенос расширения Google Chrome</span><span class="sxs-lookup"><span data-stu-id="8ae04-200">Port a Google Chrome extension</span></span>][ExtensionworkshopPorting]  
*   [<span data-ttu-id="8ae04-201">Создание расширения приложения Safari</span><span class="sxs-lookup"><span data-stu-id="8ae04-201">Build a Safari App extension</span></span>][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [<span data-ttu-id="8ae04-202">Ваше первое расширение (Firefox)</span><span class="sxs-lookup"><span data-stu-id="8ae04-202">Your first extension (Firefox)</span></span>][MDNWebextensionsYourFirst]  
*   [<span data-ttu-id="8ae04-203">Руководство по началу работы (Chrome)</span><span class="sxs-lookup"><span data-stu-id="8ae04-203">Get started tutorial (Chrome)</span></span>][ChromeDeveloperExtensionsGetstarted]  
*   [<span data-ttu-id="8ae04-204">Начало работы (опера)</span><span class="sxs-lookup"><span data-stu-id="8ae04-204">Get started (Opera)</span></span>][OperaDevExtensionsGettingStarted]  
*   [<span data-ttu-id="8ae04-205">Начало работы с расширениями Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="8ae04-205">Get started with Microsoft Edge (Chromium) extensions</span></span>][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Перенос расширения Chrome в Microsoft Edge (Chromium) | Документы Майкрософт"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Начало работы с расширениями Microsoft Edge (Chromium) | Документы Майкрософт"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Публикация расширения | Документы Майкрософт"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Разработка расширений для Microsoft Edge | Разработчик (Майкрософт)"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Центр партнеров | Разработчик (Майкрософт)"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Расширения для Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Safari App Extensions | Разработчик Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Создание расширения приложения Safari | Разработчик Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "Что такое расширения? | Разработчик Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "API Chrome | Разработчик Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Руководство по началу работы | Разработчик Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Перенос расширения Google Chrome | Семинар по расширению"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Расширения браузера | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Ваше первое расширение | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Расширения | Надстройки для Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Расширения | Надстройки Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Документация по расширениям | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API расширения, поддерживаемые в Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Начало работы | Dev. Opera"  
