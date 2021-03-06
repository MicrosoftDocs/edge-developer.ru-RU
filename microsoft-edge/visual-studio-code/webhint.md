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
# <a name="webhint-vs-code-extension"></a>Webhint Vs Расширение кода  

Используйте [webhint][WebhintMain], настраиваемый инструмент подкладки, чтобы повысить доступность, производительность, совместимость между браузерами, совместимость PWA и безопасность вашего сайта.  Он проверяет код на наличие лучших практик и распространенных ошибок. Этот проект с открытым исходным кодом, изначально разработанный командой Microsoft Edge, теперь является частью [OpenJS Foundation.][OpenjsFoundation]  Команда Microsoft Edge продолжает вносить вклад в веб-хинт вместе с веб-разработчиками в сообществе.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана расширения Visual Studio кода":::
   Снимок экрана расширения Visual Studio кода  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

Определите и исправьте проблемы в HTML, CSS, JavaScript, TypeScript и других, добавив расширение веб-Visual Studio [Code.][VisualstudioMarketplaceWebhint]  Подсказки отображаются в качестве подчеркнутой линии и суммируются в области **Проблем.**  

## <a name="configuration"></a>Настройка  

В этом [][GithubWebhintioIndexjson] расширении используется json-файл конфигурации по умолчанию, который активирует подсказки и разметки для HTML, CSS, систем шаблонов \(JSX/TSX, Angular и т. д.), JavaScript/TypeScript и т. д.  

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

Если необходимо больше контролировать активированные подсказки и разберегатели, создайте локальный файл для `.hintrc` настройки веб-хинта.  Для справки по выходу из определенных подсказок перейдите в [руководство пользователя webhint.][WebhintDocsUserguideConfiguringSummary]  

## <a name="getting-in-touch-with-the-webhint-team"></a>Контакт с командой веб-сайтов  

Отправка отзывов [путем отправки проблемы в][GithubWebhintioIssuesNew] [repo веб-службы GitHub.][GithubWebhintio]  

Чтобы внести свой вклад в расширение, перейдите к [веб-Visual Studio в руководстве по расширению кода.][GithubWebhintioExtensionVscodeContributing]  

## <a name="see-also"></a>См. также  

*   [Специальные возможности][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

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
