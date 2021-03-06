---
description: Использование веб-хинта в Visual Studio Code
title: webhint Visual Studio расширение кода
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, vs код, визуальный код студии, веб-хинт
ms.openlocfilehash: 3dfd900bf818d02dbc8123c00e7928e56d9b6ade
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399276"
---
# <a name="webhint-vs-code-extension"></a><span data-ttu-id="e4c41-104">Webhint Vs Расширение кода</span><span class="sxs-lookup"><span data-stu-id="e4c41-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="e4c41-105">Используйте [webhint][WebhintMain], настраиваемый инструмент подкладки, чтобы повысить доступность, производительность, совместимость между браузерами, совместимость PWA и безопасность вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="e4c41-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="e4c41-106">Он проверяет код на наличие лучших практик и распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="e4c41-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="e4c41-107">Этот проект с открытым исходным кодом, изначально разработанный командой Microsoft Edge, теперь является частью [OpenJS Foundation.][OpenjsFoundation]</span><span class="sxs-lookup"><span data-stu-id="e4c41-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="e4c41-108">Команда Microsoft Edge продолжает вносить вклад в веб-хинт вместе с веб-разработчиками в сообществе.</span><span class="sxs-lookup"><span data-stu-id="e4c41-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана расширения Visual Studio кода":::
   <span data-ttu-id="e4c41-110">Снимок экрана расширения Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="e4c41-110">Screenshot of webhint Visual Studio Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="e4c41-111">Определите и исправьте проблемы в HTML, CSS, JavaScript, TypeScript и других, добавив расширение веб-Visual Studio [Code.][VisualstudioMarketplaceWebhint]</span><span class="sxs-lookup"><span data-stu-id="e4c41-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="e4c41-112">Подсказки отображаются в качестве подчеркнутой линии и суммируются в области **Проблем.**</span><span class="sxs-lookup"><span data-stu-id="e4c41-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <a name="configuration"></a><span data-ttu-id="e4c41-113">Настройка</span><span class="sxs-lookup"><span data-stu-id="e4c41-113">Configuration</span></span>  

<span data-ttu-id="e4c41-114">В этом [][GithubWebhintioIndexjson] расширении используется json-файл конфигурации по умолчанию, который активирует подсказки и разметки для HTML, CSS, систем шаблонов \(JSX/TSX, Angular и т. д.), JavaScript/TypeScript и т. д.</span><span class="sxs-lookup"><span data-stu-id="e4c41-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
    ]
}
```  

<span data-ttu-id="e4c41-115">Если необходимо больше контролировать активированные подсказки и разберегатели, создайте локальный файл для `.hintrc` настройки веб-хинта.</span><span class="sxs-lookup"><span data-stu-id="e4c41-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="e4c41-116">Для справки по выходу из определенных подсказок перейдите в [руководство пользователя webhint.][WebhintDocsUserguideConfiguringSummary]</span><span class="sxs-lookup"><span data-stu-id="e4c41-116">For help with output from specific hints, navigate to [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <a name="getting-in-touch-with-the-webhint-team"></a><span data-ttu-id="e4c41-117">Контакт с командой веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="e4c41-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="e4c41-118">Отправка отзывов [путем отправки проблемы в][GithubWebhintioIssuesNew] [repo веб-службы GitHub.][GithubWebhintio]</span><span class="sxs-lookup"><span data-stu-id="e4c41-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="e4c41-119">Чтобы внести свой вклад в расширение, перейдите к [веб-Visual Studio в руководстве по расширению кода.][GithubWebhintioExtensionVscodeContributing]</span><span class="sxs-lookup"><span data-stu-id="e4c41-119">To contribute to the extension, navigate to [webhint Visual Studio Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4c41-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e4c41-120">See also</span></span>  

*   [<span data-ttu-id="e4c41-121">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="e4c41-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="e4c41-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="e4c41-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Доступность | Документы Майкрософт"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio код | Документы Майкрософт"  

[GithubWebhintio]: https://github.com/webhintio/hint "веб-| GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Способствуя — веб-| GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Новые проблемы — веб-| GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "веб-| Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Настройка веб-| документация по веб-сайтам"  
[WebhintMain]:  https://webhint.io "webhint"  
