---
description: Автоматизация и тестирование в Microsoft Edge с помощью программы".
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, веб-разработка, разработчик, средства, автоматизация, тестирование
ms.openlocfilehash: 99d873a9b3988cb8a2827ecc9a69d574a196b037
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235158"
---
# <span data-ttu-id="ef84c-104">Обзор висячего</span><span class="sxs-lookup"><span data-stu-id="ef84c-104">Puppeteer overview</span></span>  

<span data-ttu-id="ef84c-105">[Висячее][|::ref1::|Main] — это библиотека узлов, которая предоставляет высокоуровневый API для управления Microsoft Edge \(Chromium\) с помощью протокола [DevTools.][GithubChromedevtoolsProtocol] [][NodejsMain]</span><span class="sxs-lookup"><span data-stu-id="ef84c-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="ef84c-106">По умолчанию браузеры [без headeer][WikiHeadlessBrowser] запускают.</span><span class="sxs-lookup"><span data-stu-id="ef84c-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="ef84c-107">Браузеры без монитора не отображают пользовательский интерфейс, поэтому необходимо использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="ef84c-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="ef84c-108">Кроме того, вы можете настроить висячее устройство для полного запуска \(без headless\) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef84c-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="ef84c-109">По умолчанию при установке Программы", установщик скачивает новую версию [Chromium][ChromiumHome], браузер с открытым исходным кодом, на основе который также [построен Microsoft Edge.][MicrosoftBlogsWindowsExperience20181206]</span><span class="sxs-lookup"><span data-stu-id="ef84c-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="ef84c-110">Если у вас установлен Microsoft Edge \(Chromium\), вы можете использовать [висячее ядро.][PuppeteerApivscore]</span><span class="sxs-lookup"><span data-stu-id="ef84c-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="ef84c-111">— это облегченная версия Программы", которая запускает существующую установку браузера, например Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="ef84c-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ef84c-112">Чтобы скачать Microsoft Edge \(Chromium\), перейдите к каналу скачать каналы программы [insider Microsoft Edge.][MicrosoftedgeinsiderDownload]</span><span class="sxs-lookup"><span data-stu-id="ef84c-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="ef84c-113">Установка заме-ядра</span><span class="sxs-lookup"><span data-stu-id="ef84c-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="ef84c-114">Вы можете добавить `puppeteer-core` на свой веб-сайт или приложение с помощью одной из следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ef84c-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="ef84c-115">Запуск Microsoft Edge с помощью программы -core</span><span class="sxs-lookup"><span data-stu-id="ef84c-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="ef84c-116">использует Node 8.9.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ef84c-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="ef84c-117">В примере ниже используется, который поддерживается только `async` / `await` в Node 7.6.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ef84c-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="ef84c-118">Запустите командную строку, чтобы убедиться, что у вас совместимая версия `node -v` Node.js.</span><span class="sxs-lookup"><span data-stu-id="ef84c-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="ef84c-119">должен быть знаком пользователям других браузерных тест-структур, таких как [WebDriver.][WebdriverChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="ef84c-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="ef84c-120">Вы создаете экземпляр браузера, открываете страницу, а затем управляете им с помощью API".</span><span class="sxs-lookup"><span data-stu-id="ef84c-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="ef84c-121">В следующем примере кода `puppeteer-core` запускаетСя Microsoft Edge \(Chromium\), перейдите к `https://www.microsoftedgeinsider.com` и сохраняет снимок экрана как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="ef84c-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="ef84c-122">Скопируйте следующий фрагмент кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ef84c-122">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="ef84c-123">`executablePath`Измените, чтобы указать на установку Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="ef84c-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ef84c-124">Например, в macOS для `executablePath` Microsoft Edge Canary должно быть установлено . `/Applications/Microsoft\ Edge\ Canary.app/`</span><span class="sxs-lookup"><span data-stu-id="ef84c-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="ef84c-125">Чтобы найти , перейдите к исполняемого пути на этой странице и скопируйте его или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] \*\*\*\* с помощью одной из следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ef84c-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="ef84c-126">В примере кода ниже используется пакет [edge-paths][npmEdgePaths] для поиска пути к вашей установке Microsoft Edge \(Chromium\) в ос.</span><span class="sxs-lookup"><span data-stu-id="ef84c-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="ef84c-127">Наконец, установите `executablePath: EDGE_PATH` в `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ef84c-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="ef84c-128">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="ef84c-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="ef84c-129">Microsoft Edge \(EdgeHTML\) не работает `puppeteer-core` с .</span><span class="sxs-lookup"><span data-stu-id="ef84c-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="ef84c-130">Чтобы продолжить следовать этому примеру, необходимо установить каналы программы [insider][MicrosoftedgeinsiderDownload] Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef84c-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="ef84c-131">Теперь запустите `example.js` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="ef84c-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="ef84c-132">запускает Microsoft Edge, переходит к веб-странице и сохраняет снимок `https://www.microsoftedgeinsider.com` экрана.</span><span class="sxs-lookup"><span data-stu-id="ef84c-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="ef84c-133">Настройте размер снимка экрана с [помощью page.setViewport()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="ef84c-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, который example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="ef84c-135">Файл, `example.png` который был произведен</span><span class="sxs-lookup"><span data-stu-id="ef84c-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="ef84c-136">Это всего лишь простой пример сценариев автоматизации и тестирования, включенных Википером и `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ef84c-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="ef84c-137">Дополнительные сведения о Замесье и о том, как он работает, см. [в этой теме.][|::ref2::|Main]</span><span class="sxs-lookup"><span data-stu-id="ef84c-137">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="ef84c-138">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ef84c-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ef84c-139">Команда разработчиков Microsoft Edge с нетерпением услышит ваши отзывы об использовании Программы для обеспечения безопасности и `puppeteer-core` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ef84c-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="ef84c-140">Используйте **значок отправки отзывов** в Microsoft Edge DevTools или [твит][TwitterIntentTweetEdgedevtools] @EdgeDevTools, чтобы дать команде Microsoft Edge знать, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="ef84c-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ef84c-142">Значок **отправки отзыва** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ef84c-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge:  Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Документы Майкрософт"  
<!--  [WebdriverEdgehtmlMain]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Просмотр протокола Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта благодаря большей совместной работе с открытым кодом | Блог о microsoft Experience"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Пути к границам | npm"  

[PuppeteerMain]: https://pptr.dev "Замесье"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "висячее и висячее | Замесье"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Замесье"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools - Опубликовать твит | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Браузер без headless | Википедия"  
