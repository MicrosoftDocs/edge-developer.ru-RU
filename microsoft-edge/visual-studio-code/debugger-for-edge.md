---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода VS
title: Отладка Microsoft EDGE (Chromium) из кода VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: d9f33a17db7083a6a7cbb013dbf9886755f92c5e
ms.sourcegitcommit: 56cb5821d1b8e96f55bfa14a4ce87a3845b009c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182303"
---
# <span data-ttu-id="f6558-104">Отладчик для расширения кода Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f6558-104">Debugger For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="f6558-105">С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS выполните отладку клиентского кода JavaScript по строкам и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="f6558-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] VS Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладчик для расширения кода EDGE на работе":::
   <span data-ttu-id="f6558-107">Отладчик для расширения кода EDGE на работе</span><span class="sxs-lookup"><span data-stu-id="f6558-107">Debugger for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge VS Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="f6558-108">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6558-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="f6558-109">Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \) на **панели действий**.</span><span class="sxs-lookup"><span data-stu-id="f6558-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="f6558-110">Если у вас нет каких бы то ни было конфигураций в коде VS, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="f6558-110">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="f6558-111">Выберите **ребро** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="f6558-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="f6558-112">Вы увидите `launch.json` файл со следующей конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="f6558-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="f6558-113">Если вы нажмете клавишу `F5` Windows или macOS или выбираете зеленую кнопку **воспроизведения** , код VS запускает Microsoft Edge \ (EdgeHTML \), и вы сможете выполнять отладку любого веб-проекта, который вы используете на порту `8080` прямо из кода VS!</span><span class="sxs-lookup"><span data-stu-id="f6558-113">If you press `F5` on Windows or macOS or select the green **Play** button again, VS Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from VS Code!</span></span>  

### <span data-ttu-id="f6558-114">Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="f6558-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="f6558-115">Если вы хотите запустить Microsoft Edge \ (Chromium \), следующую версию Microsoft EDGE, вместо Microsoft Edge \ (EdgeHTML \), просто добавьте `version` атрибут к существующей конфигурации с помощью версии Microsoft Edge \ (Chromium \), которую вы хотите запустить \ ( `stable` ,, `dev` `beta` или `canary` \).</span><span class="sxs-lookup"><span data-stu-id="f6558-115">If you want to launch Microsoft Edge \(Chromium\), the next version of Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`stable`, `dev`, `beta`, or `canary`\).</span></span> <span data-ttu-id="f6558-116">В приведенной ниже конфигурации ниже показано, как запустить Канарские версию Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="f6558-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="f6558-117">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6558-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="f6558-118">Прикрепление кода к Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="f6558-118">Attach VS Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="f6558-119">На своем терминале выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f6558-119">From your terminal, run the following command.</span></span>  

```console
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="f6558-120">Добавьте в файл указанную ниже конфигурацию `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="f6558-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="f6558-121">Если сейчас выполнить эту настройку, код VS прикрепляется к Microsoft Edge \ (Chromium \) и начнет отладку.</span><span class="sxs-lookup"><span data-stu-id="f6558-121">If you now run this configuration, VS Code attaches to Microsoft Edge \(Chromium\) and start debugging!</span></span>  

## <span data-ttu-id="f6558-122">Связь с элементами для группы расширения кода Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="f6558-122">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>    

<span data-ttu-id="f6558-123">Отправьте отзыв, выполнив в [репозитории][GithubMicrosoftVscodeEdgeDebug2] сообщение о том, что у вас [есть вопрос][GithubMicrosoftVscodeEdgeDebug2NewIssue] в расширении.</span><span class="sxs-lookup"><span data-stu-id="f6558-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="f6558-124">Укажите файл журнала адаптера отладки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="f6558-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="f6558-125">Перетащите этот файл в комментарий вопроса, чтобы отправить его в GitHub.</span><span class="sxs-lookup"><span data-stu-id="f6558-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="f6558-126">Чтобы лучше сделать элементы для расширения кода Microsoft EDGE более качественными, вы можете воспользоваться вашими публикациями!</span><span class="sxs-lookup"><span data-stu-id="f6558-126">To help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="f6558-127">Найдите все, что вам нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDebug2] на расширение.</span><span class="sxs-lookup"><span data-stu-id="f6558-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge VS Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "отладчик для расширения кода Edge VS в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая ошибка — Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
