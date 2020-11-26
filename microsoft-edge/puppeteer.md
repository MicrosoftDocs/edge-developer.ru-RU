---
description: Автоматизация и тестирование в Microsoft Edge с помощью Puppeteer
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, разработчик, инструменты, Автоматизация и тестирование
ms.openlocfilehash: e92a863f28c96157b4c7692bd88ba6884cbf8f52
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192235"
---
# <span data-ttu-id="0b395-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="0b395-104">Puppeteer</span></span>  

<span data-ttu-id="0b395-105">[Puppeteer][|::ref1::|Main] — это библиотека [узлов][NodejsMain] , которая предоставляет интерфейс API высокого уровня для управления Microsoft Edge \ (Chromium \) с помощью [протокола DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="0b395-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="0b395-106">По умолчанию Puppeteer запускает [автономные браузеры][WikiHeadlessBrowser] .</span><span class="sxs-lookup"><span data-stu-id="0b395-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="0b395-107">В бездисплейных браузерах пользовательский интерфейс не отображается, поэтому для этого нужно использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="0b395-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="0b395-108">Кроме того, вы можете настроить Puppeteer на выполнение полных и некачественных \ (без монитора) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b395-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="0b395-109">По умолчанию при установке Puppeteer программа установки загружает последнюю версию [Chromium][ChromiumHome]— обозреватель Open-Source, на котором [также построен Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="0b395-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="0b395-110">Если у вас установлен Microsoft Edge \ (Chromium \), вы можете использовать [puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="0b395-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="0b395-111">— Это упрощенная версия Puppeteer, которая запускает уже установленный браузер, например Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="0b395-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0b395-112">Чтобы скачать Microsoft Edge \ (Chromium \), перейдите в раздел [Загрузка каналов предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="0b395-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="0b395-113">Установка puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="0b395-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="0b395-114">Вы можете добавить `puppeteer-core` на веб-сайт или в приложение одну из указанных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="0b395-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="0b395-115">Запуск Microsoft Edge с puppeteer (Core)</span><span class="sxs-lookup"><span data-stu-id="0b395-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="0b395-116">опирается на узел v 8.9.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0b395-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="0b395-117">В примере ниже используется элемент `async` / `await` , который поддерживается только в node v 7.6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0b395-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="0b395-118">Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия Node.js.</span><span class="sxs-lookup"><span data-stu-id="0b395-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="0b395-119">Знакомство с пользователями других платформ тестирования браузера, таких как веб- [накопитель][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="0b395-119">should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="0b395-120">Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="0b395-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="0b395-121">В приведенном ниже примере кода `puppeteer-core` запускается Microsoft Edge \ (Chromium \), осуществляется переход на `https://www.microsoftedgeinsider.com` снимок экрана и сохранение его как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="0b395-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="0b395-122">Скопируйте приведенный ниже фрагмент кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0b395-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="0b395-123">Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="0b395-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="0b395-124">Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="0b395-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="0b395-125">Чтобы найти `executablePath` `edge://version` путь к **исполняемому** файлу на этой странице, найдите и скопируйте его и установите пакет [Edge-paths][npmEdgePaths] с помощью одной из указанных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="0b395-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="0b395-126">В примере кода ниже используется пакет [Edge-paths][npmEdgePaths] , чтобы программным образом найти путь к установке Microsoft Edge \ (Chromium \) в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="0b395-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="0b395-127">И, наконец, Set `executablePath: EDGE_PATH` in `example.js` .</span><span class="sxs-lookup"><span data-stu-id="0b395-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="0b395-128">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="0b395-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="0b395-129">Microsoft Edge \ (EdgeHTML \) не работает с другими приложениями `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="0b395-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="0b395-130">Чтобы продолжить работу в этом примере, необходимо установить [каналы предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="0b395-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="0b395-131">Теперь запустите `example.js` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="0b395-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="0b395-132">запускает Microsoft EDGE, переходит на `https://www.microsoftedgeinsider.com` снимок веб-страницы и сохраняет его.</span><span class="sxs-lookup"><span data-stu-id="0b395-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="0b395-133">Настройка размера снимка экрана с помощью [Page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="0b395-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, созданный example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="0b395-135">`example.png`Файл, созданный с помощью</span><span class="sxs-lookup"><span data-stu-id="0b395-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="0b395-136">В следующем простом примере используются сценарии автоматизации и тестирования, включенные с помощью Puppeteer и `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="0b395-136">The following simple example uses automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="0b395-137">Чтобы получить дополнительные сведения о Puppeteer и способах ее работы, перейдите к [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="0b395-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="0b395-138">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0b395-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="0b395-139">Группа разработчиков Microsoft Edge может услышать отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0b395-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="0b395-140">С помощью значка " **Отправить отзыв** " в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , чтобы группа Microsoft Edge знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="0b395-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок "Отправить отзыв" в Microsoft Edge DevTools" lightbox="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="0b395-142">Значок " **Отправить отзыв** " в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0b395-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
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

[WebdriverChromiumMain]: ./webdriver-chromium "[Chromium) | Документы Microsoft"  
[WebdriverEdgehtmlMain]: ./webdriver.md "[EdgeHTML) | Документы Microsoft"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Средство просмотра протоколов Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта в более чем больше возможностей для совместной работы с открытым кодом | Блог Microsoft Experience"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Пути к краям | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer и puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setViewport (окно просмотра) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-опубликовать твит | Контента"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
