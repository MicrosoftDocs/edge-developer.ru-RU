---
description: Использование Playwright для автоматизации и тестирования в Microsoft Edge
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft edge, веб-разработка, разработчик, средства, автоматизация, тест, playwright, node, javascript, npm
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231085"
---
# <span data-ttu-id="f686f-104">Playwright</span><span class="sxs-lookup"><span data-stu-id="f686f-104">Playwright</span></span>  

<span data-ttu-id="f686f-105">[Playwright][|::ref1::|Main] — это [Node.js][NodejsMain] для автоматизации [Chromium,][ChromiumHome] [Firefox][FirefoxMain]и [WebKit][|::ref2::|Main] с помощью одного API.</span><span class="sxs-lookup"><span data-stu-id="f686f-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="f686f-106">Playwright создан для обеспечения кросс-браузерной веб-автоматизации, которая всегда зелена, способна, надежна и быстра.</span><span class="sxs-lookup"><span data-stu-id="f686f-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="f686f-107">Так [как Microsoft Edge создан на веб-платформе Chromium][MicrosoftBlogsWindowsExperience20181206]с открытым исходным кодом, Playwright также может автоматизировать Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f686f-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="f686f-108">По умолчанию Playwright запускает браузеры без [headless.][WikiHeadlessBrowser]</span><span class="sxs-lookup"><span data-stu-id="f686f-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="f686f-109">Браузеры без монитора не отображают пользовательский интерфейс, поэтому необходимо использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="f686f-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="f686f-110">Вы также можете настроить Playwright для полного запуска \(без headless\) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f686f-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="f686f-111">По умолчанию при установке Playwright установщик скачивает [Chromium,][ChromiumHome] [Firefox][FirefoxMain]и [WebKit.][|::ref3::|Main]</span><span class="sxs-lookup"><span data-stu-id="f686f-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="f686f-112">Если у вас также установлен Microsoft Edge \(Chromium\), для тестирования веб-сайта или приложения в Microsoft Edge playwright необходимо просто изменить код из одной строки.</span><span class="sxs-lookup"><span data-stu-id="f686f-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="f686f-113">Чтобы скачать Microsoft Edge \(Chromium\), перейдите к [загрузке Microsoft Edge.][MicrosoftEdgeDownload]</span><span class="sxs-lookup"><span data-stu-id="f686f-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="f686f-114">Установка Playwright</span><span class="sxs-lookup"><span data-stu-id="f686f-114">Installing Playwright</span></span>  

<span data-ttu-id="f686f-115">Установите [Playwright,][|::ref4::|Main] чтобы протестировать веб-сайт или приложение с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="f686f-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="f686f-116">Запуск Microsoft Edge с помощью Playwright</span><span class="sxs-lookup"><span data-stu-id="f686f-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="f686f-117">[Для воспроизведения требуется][|::ref5::|Main] Node.js версии 10.17 или выше.</span><span class="sxs-lookup"><span data-stu-id="f686f-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="f686f-118">Запустите командную строку, чтобы убедиться, что у вас совместимая `node -v` версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="f686f-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="f686f-119">Binaries браузера для Chromium, Firefox и WebKit работают в Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="f686f-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="f686f-120">Дополнительные сведения можно найти в [playwright System Requirements.][PlaywrightSystemRequirements]</span><span class="sxs-lookup"><span data-stu-id="f686f-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="f686f-121">Playwright должен быть знаком пользователям других механизмов проверки браузера, таких как [WebDriver][WebDriverChromiumMain] или [Вестер.][PuppeteerMain]</span><span class="sxs-lookup"><span data-stu-id="f686f-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="f686f-122">Вы создаете экземпляр браузера, открываете страницу, а затем управляете им с [помощью API Playwright.][PlaywrightAPIReference]</span><span class="sxs-lookup"><span data-stu-id="f686f-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="f686f-123">В следующем фрагменте кода Playwright запускает Microsoft Edge \(Chromium\), переходит к и сохраняет `https://www.microsoft.com/edge` снимок экрана как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="f686f-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="f686f-124">Скопируйте следующий фрагмент кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="f686f-124">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="f686f-125">`executablePath`Измените, чтобы указать на установку Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="f686f-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f686f-126">Например, в macOS для `executablePath` Microsoft Edge Canary должно быть установлено . `/Applications/Microsoft\ Edge\ Canary.app/`</span><span class="sxs-lookup"><span data-stu-id="f686f-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="f686f-127">Чтобы найти , перейдите к исполняемого пути на этой странице и скопируйте его или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] с помощью следующей команды. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f686f-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="f686f-128">В следующем фрагменте кода пакет [edge-paths][npmEdgePaths] используется для программного поиска пути к установке Microsoft Edge \(Chromium\) в операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f686f-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="f686f-129">Наконец, установите `executablePath: EDGE_PATH` в `example.js` .</span><span class="sxs-lookup"><span data-stu-id="f686f-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="f686f-130">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="f686f-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="f686f-131">Microsoft Edge \(EdgeHTML\) не работает с Playwright.</span><span class="sxs-lookup"><span data-stu-id="f686f-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="f686f-132">Необходимо установить [Microsoft Edge \(Chromium\),][MicrosoftEdgeDownload] чтобы продолжить следовать этому примеру.</span><span class="sxs-lookup"><span data-stu-id="f686f-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="f686f-133">Теперь `example.js` запустите из командной строки.</span><span class="sxs-lookup"><span data-stu-id="f686f-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="f686f-134">Playwright запускает Microsoft Edge, переходит к странице и сохраняет `https://www.microsoft.com/edge` снимок экрана.</span><span class="sxs-lookup"><span data-stu-id="f686f-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="f686f-135">Вы можете настроить размер страницы с помощью [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="f686f-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Файл example.png, который example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="f686f-137">Файл, `example.png` который был произведен</span><span class="sxs-lookup"><span data-stu-id="f686f-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="f686f-138">это простое демонстрация сценариев автоматизации и тестирования, включенных Playwright.</span><span class="sxs-lookup"><span data-stu-id="f686f-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="f686f-139">Чтобы сделать снимки экрана в нескольких веб-браузерах, измените следующий код.</span><span class="sxs-lookup"><span data-stu-id="f686f-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="f686f-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="f686f-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="f686f-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="f686f-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="f686f-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="f686f-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="f686f-143">Дополнительные сведения о Playwright можно найти на [веб-сайте Playwright.][|::ref6::|Main]</span><span class="sxs-lookup"><span data-stu-id="f686f-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="f686f-144">Ознакомьтесь  [с репозитарием Playwright на][PlaywrightRepo] GitHub.</span><span class="sxs-lookup"><span data-stu-id="f686f-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="f686f-145">Чтобы поделиться своим мнением об автоматизации и тестировании веб-сайта или приложения с помощью Playwright, [задайте проблему.][PlaywrightRepoNewIssue]</span><span class="sxs-lookup"><span data-stu-id="f686f-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="f686f-146">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f686f-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Документы Майкрософт"  
[PuppeteerMain]: ../puppeteer/index.md "Заметь | Документы Майкрософт"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта благодаря большей совместной работе с открытым кодом | Блог о microsoft Experience"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Скачать Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "edge-paths | npm"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Справочник по API Playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page.setViewportSize(viewportSize) | Справочник по API Playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Требования к системе для playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Новая проблема в repo Playwright | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Браузер без headless | Википедия"  
