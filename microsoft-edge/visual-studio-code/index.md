---
description: Microsoft Edge (Chromium) и Visual Studio кода
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, средства f12, devtools, vs code, visual studio code, debugger, webhint
ms.openlocfilehash: 1aa5b66043e87ebb0f1b848dcd60e2553b378f36
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230693"
---
# Visual Studio кода  

[Visual Studio код —][VisualStudioCodeDocs] это облегченный, но мощный редактор исходных кодов.  [Visual Studio код][VisualStudioCodeDocs] доступен для Windows, Linux и macOS.  Он включает встроенную поддержку JavaScript, TypeScript и Node.js, поэтому это отличное средство для веб-разработчиков перед его настройкой.  Если вы еще не используете его, скачайте Visual Studio [Code.][VisualstudioCode]  

## Расширения  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Чтобы получить какие-либо расширения, которые выделены ниже, перейдите в Visual Studio `Ctrl` + `Shift` + `X` `Command` + `Shift` + `X` Code.  

Найщите в Marketplace определенное расширение и выберите **"Установить".**  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Установка отладщика для Microsoft Edge Visual Studio кода" lightbox="./media/vscode-debugger-install.png":::
   Установка **отладщика для Microsoft Edge** Visual Studio кода  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Отладка для расширения microsoft Edge Visual Studio Code" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Отладка для Microsoft Edge** Visual Studio расширения кода  
      :::image-end:::  
      [Отладка для Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Средства Microsoft Edge для Visual Studio кода** Visual Studio расширения кода  
      :::image-end:::  
      [Microsoft Edge Tools for Visual Studio Code](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="webhint Visual Studio code extension" lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **webhint** Visual Studio расширения кода  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Отладка для Microsoft Edge  

С помощью [расширения Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code отладите код javaScript переднего `console.log()` [Visual Studio.][VisualstudioCode]  
      
С помощью средства отладки можно запустить или присоединить к Microsoft Edge \(EdgeHTML\) и Microsoft Edge \(Chromium\).  Чтобы получить по walkthrough of debugging Microsoft Edge from Visual Studio Code and sample `launch.json` configurations, navigate to [Debugger For Microsoft Edge Visual Studio Code Extension.][VisualStudioCodeDebuggerEdge]  Выберите следующее изображение, чтобы увидеть расширение в действии.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Отладка для расширения Visual Studio Edge в действии" lightbox="./media/debugger-for-edge.gif":::
   **Отладка для Microsoft Edge** Visual Studio расширения кода в действии  
:::image-end:::  

## Microsoft Edge Tools for Visual Studio Code

С помощью [расширения Microsoft Edge Tools for Visual Studio Code][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio Code используйте средство **Elements** браузера Microsoft Edge в Visual Studio Code.  Используйте его для следующих действий.  

*   Присоединить к экземпляру или запустить экземпляр Microsoft Edge.  
*   Отображение HTML-структуры времени работы.  
*   Обновим макет.  
*   Устранение проблем со стилем.  
    
Для получения дополнительных сведений перейдите в [microsoft Edge Tools for Visual Studio Code Visual Studio Code extension.][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Microsoft Edge Tools for Visual Studio Code Visual Studio Code extension in action" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Средства Microsoft Edge для Visual Studio кода** Visual Studio расширения кода в действии  
:::image-end:::  

## webhint  
      
Используйте [webhint][WebhintMain], настраиваемый инструмент linting, чтобы улучшить следующие функциональные возможности сайта.  

*   Специальные возможности
*   Производительность
*   Совместимость между браузерами
*   Совместимость PWA
*   Безопасность

Он проверяет код на наличие методик написания кода и распространенных ошибок. Проект webhint с открытым исходным кодом, изначально разработанный командой Microsoft Edge, теперь является частью [OpenJS Foundation.][OpenjsFoundation]  Команда Microsoft Edge продолжает участвовать в веб-проектах вместе с веб-разработчиками в сообществе.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана с расширением webhint Visual Studio Code" lightbox="./media/webhint-extension.png":::
   Снимок экрана **с расширением webhint** Visual Studio Code  
:::image-end:::  
      
Выявляйте и устраняйте проблемы на своем веб-сайте, добавляя расширение [webhint для Visual Studio Code.][VisualstudioMarketplaceWebhint]  Подсказки проверяют HTML, CSS, JavaScript, TypeScript и другие.  Подсказки отображаются как подчеркнутые и суммарные в **области** "Проблемы".  
      
Для получения дополнительных сведений [перейдите к how to use webhint in Visual Studio Code][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Debugger for Microsoft Edge Visual Studio code extension | Документы Майкрософт"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools для расширения Visual Studio кода | Документы Майкрософт"  
[VisualStudioCodeWebhint]: ./webhint.md "Webhint Visual Studio code Extension | Документы Майкрософт"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio кода"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio кода"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "webhint"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
