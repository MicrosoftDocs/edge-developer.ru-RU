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
# Playwright  

[Playwright][|::ref1::|Main] — это [Node.js][NodejsMain] для автоматизации [Chromium,][ChromiumHome] [Firefox][FirefoxMain]и [WebKit][|::ref2::|Main] с помощью одного API.  Playwright создан для обеспечения кросс-браузерной веб-автоматизации, которая всегда зелена, способна, надежна и быстра.  Так [как Microsoft Edge создан на веб-платформе Chromium][MicrosoftBlogsWindowsExperience20181206]с открытым исходным кодом, Playwright также может автоматизировать Microsoft Edge.  

По умолчанию Playwright запускает браузеры без [headless.][WikiHeadlessBrowser]  Браузеры без монитора не отображают пользовательский интерфейс, поэтому необходимо использовать командную строку.  Вы также можете настроить Playwright для полного запуска \(без headless\) Microsoft Edge.  

По умолчанию при установке Playwright установщик скачивает [Chromium,][ChromiumHome] [Firefox][FirefoxMain]и [WebKit.][|::ref3::|Main]  Если у вас также установлен Microsoft Edge \(Chromium\), для тестирования веб-сайта или приложения в Microsoft Edge playwright необходимо просто изменить код из одной строки.  Чтобы скачать Microsoft Edge \(Chromium\), перейдите к [загрузке Microsoft Edge.][MicrosoftEdgeDownload]  

## Установка Playwright  

Установите [Playwright,][|::ref4::|Main] чтобы протестировать веб-сайт или приложение с помощью следующей команды.  

```shell
npm i playwright
```  

## Запуск Microsoft Edge с помощью Playwright  

> [!NOTE]
> [Для воспроизведения требуется][|::ref5::|Main] Node.js версии 10.17 или выше. Запустите командную строку, чтобы убедиться, что у вас совместимая `node -v` версия Node.js.  Binaries браузера для Chromium, Firefox и WebKit работают в Windows, macOS и Linux. Дополнительные сведения можно найти в [playwright System Requirements.][PlaywrightSystemRequirements]  

Playwright должен быть знаком пользователям других механизмов проверки браузера, таких как [WebDriver][WebDriverChromiumMain] или [Вестер.][PuppeteerMain]  Вы создаете экземпляр браузера, открываете страницу, а затем управляете им с [помощью API Playwright.][PlaywrightAPIReference]  В следующем фрагменте кода Playwright запускает Microsoft Edge \(Chromium\), переходит к и сохраняет `https://www.microsoft.com/edge` снимок экрана как `example.png` .  

Скопируйте следующий фрагмент кода и сохраните его как `example.js` .  

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

`executablePath`Измените, чтобы указать на установку Microsoft Edge \(Chromium\).  Например, в macOS для `executablePath` Microsoft Edge Canary должно быть установлено . `/Applications/Microsoft\ Edge\ Canary.app/`  Чтобы найти , перейдите к исполняемого пути на этой странице и скопируйте его или установите пакет `executablePath` `edge://version` [edge-paths][npmEdgePaths] с помощью следующей команды. ****  

```shell
npm i edge-paths
```  

В следующем фрагменте кода пакет [edge-paths][npmEdgePaths] используется для программного поиска пути к установке Microsoft Edge \(Chromium\) в операционной системы.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Наконец, установите `executablePath: EDGE_PATH` в `example.js` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) не работает с Playwright.  Необходимо установить [Microsoft Edge \(Chromium\),][MicrosoftEdgeDownload] чтобы продолжить следовать этому примеру.  

Теперь `example.js` запустите из командной строки.  

```shell
node example.js
```  

Playwright запускает Microsoft Edge, переходит к странице и сохраняет `https://www.microsoft.com/edge` снимок экрана.  Вы можете настроить размер страницы с помощью [page.setViewportSize()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="Файл example.png, который example.js" lightbox="../media/playwright-example.png":::
    Файл, `example.png` который был произведен `example.js`  
:::image-end:::  

`example.js` это простое демонстрация сценариев автоматизации и тестирования, включенных Playwright.  Чтобы сделать снимки экрана в нескольких веб-браузерах, измените следующий код.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Дополнительные сведения о Playwright можно найти на [веб-сайте Playwright.][|::ref6::|Main]  Ознакомьтесь  [с репозитарием Playwright на][PlaywrightRepo] GitHub.  Чтобы поделиться своим мнением об автоматизации и тестировании веб-сайта или приложения с помощью Playwright, [задайте проблему.][PlaywrightRepoNewIssue]  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
