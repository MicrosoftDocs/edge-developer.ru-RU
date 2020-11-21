---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода Visual Studio
title: Отладка Microsoft EDGE (Chromium) из кода Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182507"
---
# <span data-ttu-id="b2760-104">Отладчик для расширения кода Microsoft Edge Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2760-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="b2760-105">С помощью [отладчика для расширения кода Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio выполните отладку клиентского кода JavaScript по строкам и просмотрите `console.log()` Операторы прямо из [кода Visual Studio][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="b2760-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Отладчик для расширения кода пограничного сервера Visual Studio на работе" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="b2760-107">Отладчик для расширения кода пограничного сервера Visual Studio на работе</span><span class="sxs-lookup"><span data-stu-id="b2760-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="b2760-108">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2760-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="b2760-109">Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \) на **панели действий**.</span><span class="sxs-lookup"><span data-stu-id="b2760-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="b2760-110">Если у вас нет каких бы то ни было конфигураций в коде Visual Studio, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="b2760-110">If you do not have any configurations in Visual Studio Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="b2760-111">Выберите **ребро** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="b2760-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="b2760-112">Вы увидите `launch.json` файл со следующей конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="b2760-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="b2760-113">При нажатии `F5` на Windows или macOS или нажатии зеленой кнопки **воспроизведения** код Visual Studio запускает Microsoft Edge \ (EdgeHTML \), и вы можете выполнять отладку любого веб-проекта, который вы используете для порта, `8080` прямо из кода Visual Studio!</span><span class="sxs-lookup"><span data-stu-id="b2760-113">If you press `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <span data-ttu-id="b2760-114">Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="b2760-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="b2760-115">Если вы хотите запустить Microsoft Edge \ (Chromium \), новый Microsoft EDGE вместо Microsoft Edge \ (EdgeHTML \), просто добавьте `version` атрибут в существующую конфигурацию с помощью версии Microsoft Edge \ (Chromium \), которую вы хотите запустить \ ( `dev` , `beta` или `canary` \).</span><span class="sxs-lookup"><span data-stu-id="b2760-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="b2760-116">В приведенной ниже конфигурации ниже показано, как запустить Канарские версию Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="b2760-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="b2760-117">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2760-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="b2760-118">Прикрепите код Visual Studio к Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="b2760-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="b2760-119">На своем терминале выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b2760-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="b2760-120">Добавьте в файл указанную ниже конфигурацию `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="b2760-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="b2760-121">Если теперь выполнить эту настройку, код Visual Studio прикрепляется к Microsoft Edge \ (Chromium \) и запускает отладку.</span><span class="sxs-lookup"><span data-stu-id="b2760-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <span data-ttu-id="b2760-122">Связь с элементами для группы расширения кода Microsoft Edge Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b2760-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="b2760-123">Отправьте отзыв, выполнив в [репозитории][GithubMicrosoftVscodeEdgeDebug2] сообщение о том, что у вас [есть вопрос][GithubMicrosoftVscodeEdgeDebug2NewIssue] в расширении.</span><span class="sxs-lookup"><span data-stu-id="b2760-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="b2760-124">Укажите файл журнала адаптера отладки, который создается для каждого запуска в `%temp%` каталоге с именем `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="b2760-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="b2760-125">Перетащите этот файл в комментарий вопроса, чтобы отправить его в GitHub.</span><span class="sxs-lookup"><span data-stu-id="b2760-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="b2760-126">Чтобы лучше сделать элементы для расширения кода Microsoft Edge Visual Studio более привлекательными, ваши публикации будут рады!</span><span class="sxs-lookup"><span data-stu-id="b2760-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="b2760-127">Найдите все, что вам нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDebug2] на расширение.</span><span class="sxs-lookup"><span data-stu-id="b2760-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "отладчик для расширения кода Visual Studio EDGE в действии"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Новая ошибка — Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Отладчик для Microsoft Edge | Visual Studio Marketplace"  
