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
# Puppeteer  

[Puppeteer][|::ref1::|Main] — это библиотека [узлов][NodejsMain] , которая предоставляет интерфейс API высокого уровня для управления Microsoft Edge \ (Chromium \) с помощью [протокола DevTools][GithubChromedevtoolsProtocol].  По умолчанию Puppeteer запускает [автономные браузеры][WikiHeadlessBrowser] .  В бездисплейных браузерах пользовательский интерфейс не отображается, поэтому для этого нужно использовать командную строку.  Кроме того, вы можете настроить Puppeteer на выполнение полных и некачественных \ (без монитора) Microsoft Edge.  

По умолчанию при установке Puppeteer программа установки загружает последнюю версию [Chromium][ChromiumHome]— обозреватель Open-Source, на котором [также построен Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].  Если у вас установлен Microsoft Edge \ (Chromium \), вы можете использовать [puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` — Это упрощенная версия Puppeteer, которая запускает уже установленный браузер, например Microsoft Edge \ (Chromium \).  Чтобы скачать Microsoft Edge \ (Chromium \), перейдите в раздел [Загрузка каналов предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload].  

## Установка puppeteer-Core  

Вы можете добавить `puppeteer-core` на веб-сайт или в приложение одну из указанных ниже команд.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Запуск Microsoft Edge с puppeteer (Core)  

> [!NOTE]
> `puppeteer-core` опирается на узел v 8.9.0 или более поздней версии.  В примере ниже используется элемент `async` / `await` , который поддерживается только в node v 7.6.0 или более поздней версии.  Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия Node.js.  

`puppeteer-core` Знакомство с пользователями других платформ тестирования браузера, таких как веб- [накопитель][WebDriverEdgehtmlMain].  Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью API Puppeteer.  В приведенном ниже примере кода `puppeteer-core` запускается Microsoft Edge \ (Chromium \), осуществляется переход на `https://www.microsoftedgeinsider.com` снимок экрана и сохранение его как `example.png` .  

Скопируйте приведенный ниже фрагмент кода и сохраните его как `example.js` .  

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

Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).  Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .  Чтобы найти `executablePath` `edge://version` путь к **исполняемому** файлу на этой странице, найдите и скопируйте его и установите пакет [Edge-paths][npmEdgePaths] с помощью одной из указанных ниже команд.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
В примере кода ниже используется пакет [Edge-paths][npmEdgePaths] , чтобы программным образом найти путь к установке Microsoft Edge \ (Chromium \) в операционной системе.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

И, наконец, Set `executablePath: EDGE_PATH` in `example.js` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) не работает с другими приложениями `puppeteer-core` .  Чтобы продолжить работу в этом примере, необходимо установить [каналы предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload] .  

Теперь запустите `example.js` из командной строки.  

```shell
node example.js
```  

`puppeteer-core` запускает Microsoft EDGE, переходит на `https://www.microsoftedgeinsider.com` снимок веб-страницы и сохраняет его.  Настройка размера снимка экрана с помощью [Page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Файл example.png, созданный example.js" lightbox="./media/puppeteer-example.png":::
   `example.png`Файл, созданный с помощью `example.js`  
:::image-end:::  

В следующем простом примере используются сценарии автоматизации и тестирования, включенные с помощью Puppeteer и `puppeteer-core` .  Чтобы получить дополнительные сведения о Puppeteer и способах ее работы, перейдите к [Puppeteer][|::ref2::|Main].  

## Взаимодействие с командой средств разработчика Microsoft Edge  

Группа разработчиков Microsoft Edge может услышать отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.  С помощью значка " **Отправить отзыв** " в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , чтобы группа Microsoft Edge знала, что вы думаете.  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="Значок Отправить отзыв в Microsoft Edge DevTools" ::: lightbox="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   Значок " **Отправить отзыв** " в Microsoft Edge DevTools  
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
