---
description: Отладка Microsoft Edge (Chromium) и Microsoft Edge (EdgeHTML) из Visual Studio Code
title: Отладка Microsoft Edge (Chromium) из Visual Studio кода
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, web development, f12 tools, devtools, vs code, visual studio code, debugger
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399297"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a><span data-ttu-id="8748d-104">Отладка для microsoft Edge Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="8748d-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="8748d-105">С [расширением кода Debugger][VisualstudioMarketplaceDebuggerMicrosoftEdge] для Microsoft Edge Visual Studio отладите переднюю строку кода JavaScript по очереди и см. отчеты непосредственно из `console.log()` [Visual Studio Code!][VisualstudioCode]</span><span class="sxs-lookup"><span data-stu-id="8748d-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладка для расширения Visual Studio edge на работе" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="8748d-107">Отладка для расширения Visual Studio edge на работе</span><span class="sxs-lookup"><span data-stu-id="8748d-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a><span data-ttu-id="8748d-108">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8748d-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="8748d-109">Перейдите к представлению отладки \( в `Ctrl` + `Shift` + `D` Windows или `Command` + `Shift` + `D` macOS\) в **панели действий.**</span><span class="sxs-lookup"><span data-stu-id="8748d-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="8748d-110">Если в коде Visual Studio нет конфигураций, выберите в Windows или macOS или выберите `F5` зеленую **кнопку Play.**</span><span class="sxs-lookup"><span data-stu-id="8748d-110">If you do not have any configurations in Visual Studio Code, select `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="8748d-111">Выберите **Edge** в отсеве.</span><span class="sxs-lookup"><span data-stu-id="8748d-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="8748d-112">Вы должны увидеть `launch.json` файл со следующей конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="8748d-112">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

<span data-ttu-id="8748d-113">Если вы выберите на Windows или macOS или снова выберите зеленую кнопку Play, Visual Studio Code запускает `F5` Microsoft Edge \(EdgeHTML\) и вы можете отладить любой веб-проект, запущенный в порту непосредственно из Visual Studio \*\*\*\* `8080` Code!</span><span class="sxs-lookup"><span data-stu-id="8748d-113">If you select `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <a name="microsoft-edge-chromium"></a><span data-ttu-id="8748d-114">Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="8748d-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="8748d-115">Если вы хотите запустить Microsoft Edge \(Chromium\), новый Microsoft Edge, а не Microsoft Edge \(EdgeHTML\), просто добавьте атрибут к существующей конфигурации с версией `version` Microsoft Edge \(Chromium\) вы хотите запустить \( `dev` , или `beta` `canary` \).</span><span class="sxs-lookup"><span data-stu-id="8748d-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="8748d-116">Следующая конфигурация ниже запускает канареевую версию Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="8748d-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="8748d-117">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8748d-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="8748d-118">Прикрепить Visual Studio к Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="8748d-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="8748d-119">Из терминала запустите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="8748d-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="8748d-120">Добавьте конфигурацию ниже в `launch.json` файл.</span><span class="sxs-lookup"><span data-stu-id="8748d-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="8748d-121">Если вы запустите эту конфигурацию, Visual Studio код прикрепится к Microsoft Edge \(Chromium\) и запустите отладку.</span><span class="sxs-lookup"><span data-stu-id="8748d-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a><span data-ttu-id="8748d-122">Контакт с командой расширения кода Elements for Microsoft Edge Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="8748d-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="8748d-123">Отправьте свои [отзывы, подав жалобу][GithubMicrosoftVscodeEdgeDebug2NewIssue] в репозитарий [GitHub][GithubMicrosoftVscodeEdgeDebug2] о расширении.</span><span class="sxs-lookup"><span data-stu-id="8748d-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="8748d-124">Включите файл журнала адаптера отключки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="8748d-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="8748d-125">Перетащите этот файл в комментарий проблемы, чтобы загрузить его в GitHub.</span><span class="sxs-lookup"><span data-stu-id="8748d-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="8748d-126">Чтобы помочь сделать расширение кода Elements для Microsoft Edge более Visual Studio, ваши вклады приветствуются!</span><span class="sxs-lookup"><span data-stu-id="8748d-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="8748d-127">Найдите все необходимое для начала в репозитарии [GitHub][GithubMicrosoftVscodeEdgeDebug2] расширения.</span><span class="sxs-lookup"><span data-stu-id="8748d-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Debugger for Edge Visual Studio в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Код"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Visual Studio Код"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая проблема — microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладка для Microsoft Edge | Visual Studio Marketplace"  
