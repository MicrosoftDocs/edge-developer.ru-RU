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
# Playwright  

[Playwright][|::ref1::|Main] — это библиотека [Node.js][NodejsMain] для автоматизации [Chromium][ChromiumHome], [Firefox][FirefoxMain]и [WebKit][|::ref2::|Main] с помощью единого API.  Playwright разработан для поддержки веб-автоматизации, которая всегда является зеленым, поддерживающим, надежной и быстрой.  Поскольку [Microsoft Edge разработан на веб-платформах Open-Source Chromium][MicrosoftBlogsWindowsExperience20181206], playwright также может автоматизировать Microsoft Edge.  

По умолчанию playwright запускает [автономные браузеры][WikiHeadlessBrowser] .  В бездисплейных браузерах пользовательский интерфейс не отображается, поэтому для этого нужно использовать командную строку.  Кроме того, вы можете настроить playwright на выполнение полных и некачественных \ (без монитора) Microsoft Edge.  

По умолчанию при установке playwright установщик загружает [Chromium][ChromiumHome], [Firefox][FirefoxMain]и [WebKit][|::ref3::|Main].  Если у вас есть Microsoft Edge \ (Chromium \), playwright просто нужно изменить однострочный код, чтобы протестировать ваш веб-сайт или приложение в Microsoft Edge.  Чтобы скачать Microsoft Edge \ (Chromium \), перейдите в раздел [Загрузка Microsoft Edge][MicrosoftEdgeDownload].  

## Установка playwright  

Установите [playwright][|::ref4::|Main] для проверки веб-сайта или приложения с помощью следующей команды.  

```shell
npm i playwright
```  

## Запуск Microsoft Edge с помощью playwright  

> [!NOTE]
> Для [playwright][|::ref5::|Main] требуется Node.js версии 10,17 или более поздней. Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия Node.js.  Двоичные файлы браузера для Chromium, Firefox и WebKit работают в Windows, macOS и Linux. Дополнительные сведения можно найти в разделе [требования к системе playwright][PlaywrightSystemRequirements].  

Playwright должны быть знакомы с пользователями других платформ тестирования браузера, таких как веб- [накопитель][WebDriverChromiumMain] или [Puppeteer][PuppeteerMain].  Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью [API playwright][PlaywrightAPIReference].  В следующем фрагменте кода playwright запускает Microsoft Edge \ (Chromium \), переходит на `https://www.microsoft.com/edge` него и сохраняет снимок экрана как `example.png` .  

Скопируйте приведенный ниже фрагмент кода и сохраните его как `example.js` .  

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

Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).  Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .  Чтобы найти `executablePath` `edge://version` путь к **исполняемому** файлу на этой странице, найдите и скопируйте его, а затем установите пакет [Edge-paths][npmEdgePaths] с помощью следующей команды.  

```shell
npm i edge-paths
```  

В следующем фрагменте кода используется пакет [Edge-paths][npmEdgePaths] , чтобы программным образом найти путь к установке Microsoft Edge \ (Chromium \) в операционной системе.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

И, наконец, Set `executablePath: EDGE_PATH` in `example.js` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) не работает с playwright.  Для продолжения работы в этом примере необходимо установить [Microsoft Edge \ (Chromium \)][MicrosoftEdgeDownload] .  

Теперь запустите `example.js` из командной строки.  

```shell
node example.js
```  

Playwright запускает Microsoft EDGE, переходит на `https://www.microsoft.com/edge` снимок страницы и сохраняет его.  Вы можете настроить размер страницы с помощью [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="Файл example.png, созданный example.js" lightbox="../media/playwright-example.png":::
    `example.png`Файл, созданный с помощью `example.js`  
:::image-end:::  

`example.js` — Это простая демонстрация сценариев автоматизации и тестирования, включенных playwright.  Чтобы сделать снимки экрана в нескольких веб-браузерах, измените приведенный ниже код.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Чтобы получить дополнительные сведения о playwright, перейдите на [веб-сайт playwright][|::ref6::|Main].  Изучите  [репозиторий playwright][PlaywrightRepo] на GitHub.  Чтобы поделиться отзывом об автоматизации и тестировании веб-сайта или приложения с помощью playwright, закажите [вопрос][PlaywrightRepoNewIssue].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

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
