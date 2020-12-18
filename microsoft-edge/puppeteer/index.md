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
# Обзор висячего  

[Висячее][|::ref1::|Main] — это библиотека узлов, которая предоставляет высокоуровневый API для управления Microsoft Edge \(Chromium\) с помощью протокола [DevTools.][GithubChromedevtoolsProtocol] [][NodejsMain]  По умолчанию браузеры [без headeer][WikiHeadlessBrowser] запускают.  Браузеры без монитора не отображают пользовательский интерфейс, поэтому необходимо использовать командную строку.  Кроме того, вы можете настроить висячее устройство для полного запуска \(без headless\) Microsoft Edge.  

По умолчанию при установке Программы", установщик скачивает новую версию [Chromium][ChromiumHome], браузер с открытым исходным кодом, на основе который также [построен Microsoft Edge.][MicrosoftBlogsWindowsExperience20181206]  Если у вас установлен Microsoft Edge \(Chromium\), вы можете использовать [висячее ядро.][PuppeteerApivscore]  `puppeteer-core` — это облегченная версия Программы", которая запускает существующую установку браузера, например Microsoft Edge \(Chromium\).  Чтобы скачать Microsoft Edge \(Chromium\), перейдите к каналу скачать каналы программы [insider Microsoft Edge.][MicrosoftedgeinsiderDownload]  

## Установка заме-ядра  

Вы можете добавить `puppeteer-core` на свой веб-сайт или приложение с помощью одной из следующих команд.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Запуск Microsoft Edge с помощью программы -core  

> [!NOTE]
> `puppeteer-core` использует Node 8.9.0 или более поздней.  В примере ниже используется, который поддерживается только `async` / `await` в Node 7.6.0 или более поздней.  Запустите командную строку, чтобы убедиться, что у вас совместимая версия `node -v` Node.js.  

`puppeteer-core` должен быть знаком пользователям других браузерных тест-структур, таких как [WebDriver.][WebdriverChromiumMain]  Вы создаете экземпляр браузера, открываете страницу, а затем управляете им с помощью API".  В следующем примере кода `puppeteer-core` запускаетСя Microsoft Edge \(Chromium\), перейдите к `https://www.microsoftedgeinsider.com` и сохраняет снимок экрана как `example.png` .  

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

`executablePath`Измените, чтобы указать на установку Microsoft Edge \(Chromium\).  Например, в macOS для `executablePath` Microsoft Edge Canary должно быть установлено . `/Applications/Microsoft\ Edge\ Canary.app/`  Чтобы найти , перейдите к исполняемого пути на этой странице и скопируйте его или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] **** с помощью одной из следующих команд.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
В примере кода ниже используется пакет [edge-paths][npmEdgePaths] для поиска пути к вашей установке Microsoft Edge \(Chromium\) в ос.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Наконец, установите `executablePath: EDGE_PATH` в `example.js` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) не работает `puppeteer-core` с .  Чтобы продолжить следовать этому примеру, необходимо установить каналы программы [insider][MicrosoftedgeinsiderDownload] Microsoft Edge.  

Теперь запустите `example.js` из командной строки.  

```shell
node example.js
```  

`puppeteer-core` запускает Microsoft Edge, переходит к веб-странице и сохраняет снимок `https://www.microsoftedgeinsider.com` экрана.  Настройте размер снимка экрана с [помощью page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, который example.js" lightbox="./media/puppeteer-example.png":::
   Файл, `example.png` который был произведен `example.js`  
:::image-end:::  

Это всего лишь простой пример сценариев автоматизации и тестирования, включенных Википером и `puppeteer-core` .  Дополнительные сведения о Замесье и о том, как он работает, см. [в этой теме.][|::ref2::|Main]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

Команда разработчиков Microsoft Edge с нетерпением услышит ваши отзывы об использовании Программы для обеспечения безопасности и `puppeteer-core` Microsoft Edge.  Используйте **значок отправки отзывов** в Microsoft Edge DevTools или [твит][TwitterIntentTweetEdgedevtools] @EdgeDevTools, чтобы дать команде Microsoft Edge знать, что вы думаете.  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок отправки отзыва в Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок **отправки отзыва** в Microsoft Edge DevTools  
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
