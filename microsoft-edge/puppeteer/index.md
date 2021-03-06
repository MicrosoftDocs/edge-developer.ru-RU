---
description: Использование puppeteer для автоматизации и тестирования в Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, разработчик, средства, автоматизация, тестирование
ms.openlocfilehash: 068a2289b0e3bf8fffb49c771b83337abb79ea83
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398471"
---
# <a name="puppeteer-overview"></a><span data-ttu-id="25441-104">Обзор Puppeteer</span><span class="sxs-lookup"><span data-stu-id="25441-104">Puppeteer overview</span></span>  

<span data-ttu-id="25441-105">[Puppeteer][|::ref1::|Main] — это [библиотека узлов,][NodejsMain] которая предоставляет API высокого уровня для управления Microsoft Edge \(Chromium\) с помощью [протокола DevTools.][GithubChromedevtoolsProtocol]</span><span class="sxs-lookup"><span data-stu-id="25441-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="25441-106">Puppeteer запускает [безголовые браузеры по][WikiHeadlessBrowser] умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25441-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="25441-107">Безголовые браузеры не отображают пользовательский интерфейс, поэтому вместо этого необходимо использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="25441-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="25441-108">Вы также можете настроить Puppeteer для запуска полного \(безголовые\) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="25441-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="25441-109">По умолчанию при установке Puppeteer установщик скачивает недавнюю версию [Chromium][ChromiumHome], браузер с открытым исходным кодом, на который также построен [Microsoft Edge.][MicrosoftBlogsWindowsExperience20181206]</span><span class="sxs-lookup"><span data-stu-id="25441-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="25441-110">Если у вас установлен Microsoft Edge \(Chromium\), вы можете использовать [puppeteer-core.][PuppeteerApivscore]</span><span class="sxs-lookup"><span data-stu-id="25441-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="25441-111">— облегченная версия Puppeteer, которая запускает существующую установку браузера, например Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="25441-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="25441-112">Чтобы скачать Microsoft Edge \(Chromium\), перейдите по [каналу Загрузка каналов инсайдерской службы Microsoft Edge.][MicrosoftedgeinsiderDownload]</span><span class="sxs-lookup"><span data-stu-id="25441-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <a name="installing-puppeteer-core"></a><span data-ttu-id="25441-113">Установка кукловода-ядра</span><span class="sxs-lookup"><span data-stu-id="25441-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="25441-114">Вы можете добавить `puppeteer-core` на свой веб-сайт или приложение одну из следующих команд.</span><span class="sxs-lookup"><span data-stu-id="25441-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a><span data-ttu-id="25441-115">Запуск Microsoft Edge с кукловод-ядром</span><span class="sxs-lookup"><span data-stu-id="25441-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="25441-116">зависит от Node v8.9.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="25441-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="25441-117">В приведенной ниже примере используется только `async` / `await` поддержка в Node v7.6.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="25441-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="25441-118">Запустите из командной строки, чтобы убедиться, что у вас есть совместимая версия `node -v` Node.js.</span><span class="sxs-lookup"><span data-stu-id="25441-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="25441-119">должны быть знакомы пользователям других браузерных тестов-фреймворков, таких как [WebDriver.][WebdriverChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="25441-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="25441-120">Вы создаете экземпляр браузера, открываете страницу и затем управляете ею с API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="25441-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="25441-121">В следующем примере кода запускает `puppeteer-core` Microsoft Edge \(Chromium\), переходит к и сохраняет скриншот `https://www.microsoftedgeinsider.com` как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="25441-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="25441-122">Скопируйте следующий фрагмент кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="25441-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="25441-123">Изменение, `executablePath` указывав на установку Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="25441-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="25441-124">Например, на macOS необходимо установить для `executablePath` Microsoft Edge Canary `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="25441-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="25441-125">Чтобы найти, перейдите к исполняемой дорожке и скопируйте ее на этой странице или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] с одной из следующих команд. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="25441-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="25441-126">В приведенном ниже примере кода используется пакет [edge-paths,][npmEdgePaths] чтобы программным образом найти путь к установке Microsoft Edge \(Chromium\) на вашей ОС.</span><span class="sxs-lookup"><span data-stu-id="25441-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="25441-127">Наконец, установите `executablePath: EDGE_PATH` `example.js` .</span><span class="sxs-lookup"><span data-stu-id="25441-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="25441-128">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="25441-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="25441-129">Microsoft Edge \(EdgeHTML\) не работает `puppeteer-core` с .</span><span class="sxs-lookup"><span data-stu-id="25441-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="25441-130">Чтобы продолжить следовать этому примеру, необходимо установить каналы инсайдерской службы Microsoft [Edge.][MicrosoftedgeinsiderDownload]</span><span class="sxs-lookup"><span data-stu-id="25441-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="25441-131">Теперь `example.js` запустите из командной строки.</span><span class="sxs-lookup"><span data-stu-id="25441-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="25441-132">запускает Microsoft Edge, переходит на страницу и сохраняет снимок `https://www.microsoftedgeinsider.com` экрана веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="25441-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="25441-133">Настройка размера экрана с [помощью page.setViewport()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="25441-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, производимый example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="25441-135">Файл, `example.png` производимый</span><span class="sxs-lookup"><span data-stu-id="25441-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="25441-136">Это простой пример сценариев автоматизации и тестирования, включенных в Puppeteer и `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="25441-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="25441-137">Дополнительные сведения о puppeteer и о том, как он работает, перейдите к [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="25441-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="25441-138">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="25441-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="25441-139">Команда разработчиков Microsoft Edge готова услышать ваши отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="25441-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="25441-140">Используйте **значок Отправка** отзывов в Microsoft [][TwitterIntentTweetEdgedevtools] Edge DevTools или твит@EdgeDevTools чтобы команда Microsoft Edge знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="25441-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="25441-142">Значок **Отправка** отзывов в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="25441-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
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

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome DevTools Protocol Viewer | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта с помощью более открытого | Блог microsoft Experience"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачивание Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Edge Paths | npm"  

[PuppeteerMain]: https://pptr.dev "Кукловод"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer vs. puppeteer-core | Кукловод"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport (viewport) | Кукловод"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools — выложите сообщение чирикать | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Безгол | Википедия"  
