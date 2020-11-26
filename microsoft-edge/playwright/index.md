---
description: Автоматизация и тестирование в Microsoft Edge с помощью playwright
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, разработчик, инструменты, Автоматизация, проверка, playwright, узел, сценарий JavaScript, NPM
ms.openlocfilehash: ac03923fb25da00f07cb70e81ac06b106a6e1452
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192214"
---
# <span data-ttu-id="c6769-104">Playwright</span><span class="sxs-lookup"><span data-stu-id="c6769-104">Playwright</span></span>  

<span data-ttu-id="c6769-105">[Playwright][|::ref1::|Main] — это библиотека [Node.js][NodejsMain] для автоматизации [Chromium][ChromiumHome], [Firefox][FirefoxMain]и [WebKit][|::ref2::|Main] с помощью единого API.</span><span class="sxs-lookup"><span data-stu-id="c6769-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="c6769-106">Playwright разработан для поддержки веб-автоматизации, которая всегда является зеленым, поддерживающим, надежной и быстрой.</span><span class="sxs-lookup"><span data-stu-id="c6769-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="c6769-107">Поскольку [Microsoft Edge разработан на веб-платформах Open-Source Chromium][MicrosoftBlogsWindowsExperience20181206], playwright также может автоматизировать Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6769-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="c6769-108">По умолчанию playwright запускает [автономные браузеры][WikiHeadlessBrowser] .</span><span class="sxs-lookup"><span data-stu-id="c6769-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="c6769-109">В бездисплейных браузерах пользовательский интерфейс не отображается, поэтому для этого нужно использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="c6769-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="c6769-110">Кроме того, вы можете настроить playwright на выполнение полных и некачественных \ (без монитора) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6769-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="c6769-111">По умолчанию при установке playwright установщик загружает [Chromium][ChromiumHome], [Firefox][FirefoxMain]и [WebKit][|::ref3::|Main].</span><span class="sxs-lookup"><span data-stu-id="c6769-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="c6769-112">Если у вас есть Microsoft Edge \ (Chromium \), playwright просто нужно изменить однострочный код, чтобы протестировать ваш веб-сайт или приложение в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6769-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="c6769-113">Чтобы скачать Microsoft Edge \ (Chromium \), перейдите в раздел [Загрузка Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="c6769-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="c6769-114">Установка playwright</span><span class="sxs-lookup"><span data-stu-id="c6769-114">Installing Playwright</span></span>  

<span data-ttu-id="c6769-115">Установите [playwright][|::ref4::|Main] для проверки веб-сайта или приложения с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="c6769-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="c6769-116">Запуск Microsoft Edge с помощью playwright</span><span class="sxs-lookup"><span data-stu-id="c6769-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="c6769-117">Для [playwright][|::ref5::|Main] требуется Node.js версии 10,17 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c6769-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="c6769-118">Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="c6769-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="c6769-119">Двоичные файлы браузера для Chromium, Firefox и WebKit работают в Windows, macOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="c6769-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="c6769-120">Дополнительные сведения можно найти в разделе [требования к системе playwright][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="c6769-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="c6769-121">Playwright должны быть знакомы с пользователями других платформ тестирования браузера, таких как веб- [накопитель][WebDriverChromiumMain] или [Puppeteer][PuppeteerMain].</span><span class="sxs-lookup"><span data-stu-id="c6769-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="c6769-122">Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью [API playwright][PlaywrightAPIReference].</span><span class="sxs-lookup"><span data-stu-id="c6769-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="c6769-123">В следующем фрагменте кода playwright запускает Microsoft Edge \ (Chromium \), переходит на `https://www.microsoft.com/edge` него и сохраняет снимок экрана как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="c6769-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="c6769-124">Скопируйте приведенный ниже фрагмент кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="c6769-124">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="c6769-125">Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="c6769-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c6769-126">Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="c6769-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="c6769-127">Чтобы найти `executablePath` `edge://version` путь к **исполняемому** файлу на этой странице, найдите и скопируйте его, а затем установите пакет [Edge-paths][npmEdgePaths] с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="c6769-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="c6769-128">В следующем фрагменте кода используется пакет [Edge-paths][npmEdgePaths] , чтобы программным образом найти путь к установке Microsoft Edge \ (Chromium \) в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="c6769-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="c6769-129">И, наконец, Set `executablePath: EDGE_PATH` in `example.js` .</span><span class="sxs-lookup"><span data-stu-id="c6769-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="c6769-130">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="c6769-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="c6769-131">Microsoft Edge \ (EdgeHTML \) не работает с playwright.</span><span class="sxs-lookup"><span data-stu-id="c6769-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="c6769-132">Для продолжения работы в этом примере необходимо установить [Microsoft Edge \ (Chromium \)][MicrosoftEdgeDownload] .</span><span class="sxs-lookup"><span data-stu-id="c6769-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="c6769-133">Теперь запустите `example.js` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="c6769-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="c6769-134">Playwright запускает Microsoft EDGE, переходит на `https://www.microsoft.com/edge` снимок страницы и сохраняет его.</span><span class="sxs-lookup"><span data-stu-id="c6769-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="c6769-135">Вы можете настроить размер страницы с помощью [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="c6769-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="Файл example.png, созданный example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="c6769-137">`example.png`Файл, созданный с помощью</span><span class="sxs-lookup"><span data-stu-id="c6769-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="c6769-138">— Это простая демонстрация сценариев автоматизации и тестирования, включенных playwright.</span><span class="sxs-lookup"><span data-stu-id="c6769-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="c6769-139">Чтобы сделать снимки экрана в нескольких веб-браузерах, измените приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="c6769-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="c6769-140">Chromium</span><span class="sxs-lookup"><span data-stu-id="c6769-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="c6769-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="c6769-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="c6769-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="c6769-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="c6769-143">Чтобы получить дополнительные сведения о playwright, перейдите на [веб-сайт playwright][|::ref6::|Main].</span><span class="sxs-lookup"><span data-stu-id="c6769-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="c6769-144">Изучите  [репозиторий playwright][PlaywrightRepo] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="c6769-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="c6769-145">Чтобы поделиться отзывом об автоматизации и тестировании веб-сайта или приложения с помощью playwright, закажите [вопрос][PlaywrightRepoNewIssue].</span><span class="sxs-lookup"><span data-stu-id="c6769-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="c6769-146">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6769-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "[Chromium) | Документы Microsoft"  
[PuppeteerMain]: ../puppeteer.md "Puppeteer | Документы Microsoft"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта в более чем больше возможностей для совместной работы с открытым кодом | Блог Microsoft Experience"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Загрузить Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Краевые пути | NPM"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Справочник по API playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "Page. setViewportSize (viewportSize) | Справочник по API playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Требования к системе playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Новая ошибка в репозитории playwright | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
