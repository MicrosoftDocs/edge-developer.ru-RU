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
# <a name="puppeteer-overview"></a>Обзор Puppeteer  

[Puppeteer][|::ref1::|Main] — это [библиотека узлов,][NodejsMain] которая предоставляет API высокого уровня для управления Microsoft Edge \(Chromium\) с помощью [протокола DevTools.][GithubChromedevtoolsProtocol]  Puppeteer запускает [безголовые браузеры по][WikiHeadlessBrowser] умолчанию.  Безголовые браузеры не отображают пользовательский интерфейс, поэтому вместо этого необходимо использовать командную строку.  Вы также можете настроить Puppeteer для запуска полного \(безголовые\) Microsoft Edge.  

По умолчанию при установке Puppeteer установщик скачивает недавнюю версию [Chromium][ChromiumHome], браузер с открытым исходным кодом, на который также построен [Microsoft Edge.][MicrosoftBlogsWindowsExperience20181206]  Если у вас установлен Microsoft Edge \(Chromium\), вы можете использовать [puppeteer-core.][PuppeteerApivscore]  `puppeteer-core` — облегченная версия Puppeteer, которая запускает существующую установку браузера, например Microsoft Edge \(Chromium\).  Чтобы скачать Microsoft Edge \(Chromium\), перейдите по [каналу Загрузка каналов инсайдерской службы Microsoft Edge.][MicrosoftedgeinsiderDownload]  

## <a name="installing-puppeteer-core"></a>Установка кукловода-ядра  

Вы можете добавить `puppeteer-core` на свой веб-сайт или приложение одну из следующих команд.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a>Запуск Microsoft Edge с кукловод-ядром  

> [!NOTE]
> `puppeteer-core` зависит от Node v8.9.0 или более поздней.  В приведенной ниже примере используется только `async` / `await` поддержка в Node v7.6.0 или более поздней.  Запустите из командной строки, чтобы убедиться, что у вас есть совместимая версия `node -v` Node.js.  

`puppeteer-core` должны быть знакомы пользователям других браузерных тестов-фреймворков, таких как [WebDriver.][WebdriverChromiumMain]  Вы создаете экземпляр браузера, открываете страницу и затем управляете ею с API Puppeteer.  В следующем примере кода запускает `puppeteer-core` Microsoft Edge \(Chromium\), переходит к и сохраняет скриншот `https://www.microsoftedgeinsider.com` как `example.png` .  

Скопируйте следующий фрагмент кода и сохраните его как `example.js` .  

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

Изменение, `executablePath` указывав на установку Microsoft Edge \(Chromium\).  Например, на macOS необходимо установить для `executablePath` Microsoft Edge Canary `/Applications/Microsoft\ Edge\ Canary.app/` .  Чтобы найти, перейдите к исполняемой дорожке и скопируйте ее на этой странице или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] с одной из следующих команд. ****  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
В приведенном ниже примере кода используется пакет [edge-paths,][npmEdgePaths] чтобы программным образом найти путь к установке Microsoft Edge \(Chromium\) на вашей ОС.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Наконец, установите `executablePath: EDGE_PATH` `example.js` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) не работает `puppeteer-core` с .  Чтобы продолжить следовать этому примеру, необходимо установить каналы инсайдерской службы Microsoft [Edge.][MicrosoftedgeinsiderDownload]  

Теперь `example.js` запустите из командной строки.  

```shell
node example.js
```  

`puppeteer-core` запускает Microsoft Edge, переходит на страницу и сохраняет снимок `https://www.microsoftedgeinsider.com` экрана веб-страницы.  Настройка размера экрана с [помощью page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, производимый example.js" lightbox="./media/puppeteer-example.png":::
   Файл, `example.png` производимый `example.js`  
:::image-end:::  

Это простой пример сценариев автоматизации и тестирования, включенных в Puppeteer и `puppeteer-core` .  Дополнительные сведения о puppeteer и о том, как он работает, перейдите к [Puppeteer][|::ref2::|Main].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Взаимодействие с командой средств разработчика Microsoft Edge  

Команда разработчиков Microsoft Edge готова услышать ваши отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.  Используйте **значок Отправка** отзывов в Microsoft [][TwitterIntentTweetEdgedevtools] Edge DevTools или твит@EdgeDevTools чтобы команда Microsoft Edge знала, что вы думаете.  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправка отзывов в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок **Отправка** отзывов в Microsoft Edge DevTools  
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
