---
description: Microsoft EDGE (Chromium) и код Visual Studio
title: Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик, веб-подсказка
ms.openlocfilehash: 0d13c6eb9411f89e3a681176ade0caf8d59d46d8
ms.sourcegitcommit: 02c602379537ab3b9d0a355cea7fcf96fdbd8870
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2020
ms.locfileid: "11182750"
---
# Visual Studio Code  

[Код Visual Studio][VisualStudioCodeDocs] — это упрощенный, но мощный редактор исходного кода.  [Код Visual Studio][VisualStudioCodeDocs] доступен для Windows, Linux и macOS.  Она включает встроенную поддержку JavaScript, TypeScript и Node.js, поэтому она является прекрасным инструментом для веб-разработчиков перед настройкой.  Если вы еще не используете его, скачайте [код Visual Studio][VisualstudioCode].  

## Расширения  

<!--todo: We want to put something like the tiles for extensions Visual Studio Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page.  I think it's a web page.  I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->  

Чтобы получить какое-либо из расширений, выделеных ниже, перейдите к разделу расширения \ (выберите `Ctrl` + `Shift` + `X` в Windows или Linux или `Command` + `Shift` + `X` macOS \) в коде Visual Studio.  

Найдите нужное расширение рынка и нажмите кнопку **установить**.  

:::image type="complex" source="./media/vscode-debugger-install.png" alt-text="Установка отладчика для расширения кода Microsoft Edge Visual Studio" lightbox="./media/vscode-debugger-install.png":::
   Установка **отладчика для расширения кода Microsoft Edge** Visual Studio  
:::image-end:::  

:::row:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png" alt-text="Отладчик для расширения кода Microsoft Edge Visual Studio" lightbox="./media/visual-studio-code-extension-debugger-for-microsoft-edge.msft.png":::
         **Отладчик для Microsoft Edge** Расширение кода Visual Studio  
      :::image-end:::  
      [Отладчик для Microsoft Edge](#debugger-for-microsoft-edge)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png" alt-text="Инструменты Microsoft Edge для Visual Studio расширение кода Visual Studio" lightbox="./media/visual-studio-code-extension-microsoft-edge-tools-for-visual-studio-code.msft.png":::
         **Инструменты Microsoft Edge для кода Visual Studio** Расширение кода Visual Studio  
      :::image-end:::  
      [Инструменты Microsoft Edge для кода Visual Studio](#microsoft-edge-tools-for-visual-studio-code)  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="./media/visual-studio-code-extension-webhint.msft.png" alt-text="расширение кода Visual Studio Подсказка"::: lightbox="./media/visual-studio-code-extension-webhint.msft.png":::
         **Подсказка** Расширение кода Visual Studio  
      :::image-end:::  
      [webhint](#webhint)  
   :::column-end:::
:::row-end:::  

## Отладчик для Microsoft Edge  

С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio выполните отладку клиентского кода JavaScript и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode].  
      
С помощью средства отладки вы можете запустить и присоединиться к обоим Microsoft Edge \ (EdgeHTML \) и Microsoft Edge \ (Chromium \).  Для пошагового руководства по отладке Microsoft Edge из кода Visual Studio и образцов `launch.json` конфигураций перейдите в [отладчик для расширения кода Microsoft Edge Visual Studio][VisualStudioCodeDebuggerEdge].  Чтобы увидеть расширение в действии, выберите на следующем изображении.  

:::image type="complex" source="./media/debugger-for-edge.png" alt-text="Отладчик для расширения кода Edge Visual Studio в действии" lightbox="./media/debugger-for-edge.gif":::
   **Отладчик для Microsoft Edge** Расширение кода Visual Studio в действии  
:::image-end:::  

## Инструменты Microsoft Edge для кода Visual Studio

С помощью инструментов [Microsoft Edge для Visual Studio с кодом кода][VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode] Visual Studio используйте средство " **элементы** " в браузере Microsoft EDGE в коде Visual Studio.  Используйте его для указанных ниже действий.  

*   Присоединение к экземпляру или запуск экземпляра Microsoft Edge.  
*   Отобразите HTML-структуру среды выполнения.  
*   Обновите макет.  
*   Устранение проблем с стилизацией.  
    
Дополнительные сведения можно найти в разделе [инструменты Microsoft Edge для Visual Studio с расширением кода Visual][VisualStudioCodeMicrosoftEdgeDevtoolsExtension]Studio.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/microsoft-edge-tools-for-visual-studio-code.png" alt-text="Инструменты Microsoft Edge для Visual Studio, расширение кода Visual Studio в действии" lightbox="./media/microsoft-edge-tools-for-visual-studio-code.png":::
   **Инструменты Microsoft Edge для кода Visual Studio** Расширение кода Visual Studio в действии  
:::image-end:::  

## webhint  
      
Используйте веб- [подсказку][WebhintMain], настраиваемое средство linting, чтобы улучшить следующие функциональные возможности сайта.  

*   Специальные возможности
*   Производительность
*   Совместимость с различными браузерами
*   Совместимость с PWA
*   Безопасность

В коде проверяется, как проверяются правила кодирования и распространенные ошибки. Проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation][OpenjsFoundation].  Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.  <!--  Choose the following image to see the extension in action.  -->  
      
:::image type="complex" source="./media/webhint-extension.png" alt-text="Снимок экрана: расширение кода Visual Studio Подсказка"::: lightbox="./media/webhint-extension.png":::
   Снимок экрана: расширение кода Visual Studio " **Подсказка** "  
:::image-end:::  
      
Определите и устраните проблемы на веб-сайте, добавив расширение веб- [подсказки для кода Visual Studio][VisualstudioMarketplaceWebhint].  Подсказки изучит HTML, CSS, JavaScript, TypeScript и многое другое.  Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели " **проблемы** ".  
      
Для получения дополнительных сведений перейдите к [разделу Использование подсказки в коде Visual Studio][VisualStudioCodeWebhint].  

<!--links -->  

[VisualStudioCodeDebuggerEdge]: ./debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge Visual Studio | Документы Microsoft"  
[VisualStudioCodeMicrosoftEdgeDevtoolsExtension]: ./microsoft-edge-devtools-extension.md "Microsoft Edge DevTools для расширения кода Visual Studio | Документы Microsoft"  
[VisualStudioCodeWebhint]: ./webhint.md "Расширение кода Visual Studio "Подсказка" | Документы Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
[VisualstudioMarketplaceMicrosoftEdgeToolsVisualStudioCode]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Инструменты Microsoft Edge для Visual Studio, код | Visual Studio Marketplace"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "Подсказка | Visual Studio Marketplace"  

[WebhintMain]:  https://webhint.io "Подсказка"  
[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  
