---
description: С помощью средств разработчика F12 узнайте, как отлагостить фоновый сценарий, сценарии контента и страницы расширения расширения.
title: Отладка | Расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, javascript, developer, debug, debugging
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399367"
---
# <a name="debugging-extensions"></a><span data-ttu-id="8cb63-104">Отладка расширений</span><span class="sxs-lookup"><span data-stu-id="8cb63-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="8cb63-105">Отламывка расширений в Microsoft Edge, можно с помощью средств разработчика F12.</span><span class="sxs-lookup"><span data-stu-id="8cb63-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>  

<span data-ttu-id="8cb63-106">Следующее видео проходит через багги Расширение Microsoft Edge, хотя каждый сценарий отладки и исправления его по пути.</span><span class="sxs-lookup"><span data-stu-id="8cb63-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span>  <span data-ttu-id="8cb63-107">Дополнительные сведения см. в пошаговом инструкции ниже.</span><span class="sxs-lookup"><span data-stu-id="8cb63-107">See the step-by-step instructions below for more info.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> <span data-ttu-id="8cb63-108">Чтобы использовать отладку расширения с помощью F12, сначала необходимо включить функции разработчика в about:flags.</span><span class="sxs-lookup"><span data-stu-id="8cb63-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span>  <span data-ttu-id="8cb63-109">Дополнительные [сведения](./adding-and-removing-extensions.md) о том, как это сделать, см. в добавлении и удалении расширений.</span><span class="sxs-lookup"><span data-stu-id="8cb63-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>  

## <a name="background-script-debugging"></a><span data-ttu-id="8cb63-110">Отладка фонового сценария</span><span class="sxs-lookup"><span data-stu-id="8cb63-110">Background script debugging</span></span>  

<span data-ttu-id="8cb63-111">Чтобы начать отладку фонового сценария расширения:</span><span class="sxs-lookup"><span data-stu-id="8cb63-111">To start debugging the background script of your extension:</span></span>  

1.  <span data-ttu-id="8cb63-112">Нажмите **кнопку Дополнительные (...)** с **последующими расширениями,** чтобы перейти в области расширения.</span><span class="sxs-lookup"><span data-stu-id="8cb63-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
    
    ![кнопка другие](../media/morebutton.png)  
    
1.  <span data-ttu-id="8cb63-114">Щелкните расширение, которое необходимо отлажать.</span><span class="sxs-lookup"><span data-stu-id="8cb63-114">Click on the extension that you want to debug.</span></span>  
1.  <span data-ttu-id="8cb63-115">Щелкните **ссылку Фоновая** страница, чтобы привести F12 для фонового процесса.</span><span class="sxs-lookup"><span data-stu-id="8cb63-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
    
    ![выбранное представление расширения параметров со ссылкой на проверку](../media/debug-inspect.png)  
    
1.  <span data-ttu-id="8cb63-117">Выберите **вкладку Debugger** в F12.</span><span class="sxs-lookup"><span data-stu-id="8cb63-117">Select the **Debugger** tab in F12.</span></span>  
1.  <span data-ttu-id="8cb63-118">Перейдите к фоновому сценарию расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="8cb63-118">Navigate to and select your extension's background script.</span></span>  
1.  <span data-ttu-id="8cb63-119">Поместите точки разлада для отладки, щелкнув слева от номера строки кода.</span><span class="sxs-lookup"><span data-stu-id="8cb63-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![консоль f12, показывающая фоновый сценарий с точками перерыва](../media/debug-f12-background.png)  
    
1.  <span data-ttu-id="8cb63-121">Выберите **вкладку Консоли** и выполните `location.reload()` команду.</span><span class="sxs-lookup"><span data-stu-id="8cb63-121">Select the **Console** tab and execute the `location.reload()` command.</span></span>  <span data-ttu-id="8cb63-122">При этом будет повторно выполняться фоновый сценарий, что позволит выполнить выполнение кода.</span><span class="sxs-lookup"><span data-stu-id="8cb63-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
    
    ![консоль с входом location.reload](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a><span data-ttu-id="8cb63-124">Отладка скрипта контента</span><span class="sxs-lookup"><span data-stu-id="8cb63-124">Content script debugging</span></span>  

<span data-ttu-id="8cb63-125">Чтобы начать отладку сценария контента вашего расширения:</span><span class="sxs-lookup"><span data-stu-id="8cb63-125">To start debugging the content script of your extension:</span></span>  

1.  <span data-ttu-id="8cb63-126">Запустите F12, переходя на кнопку **More (...)** и выбрав средства разработчика **F12,** или нажав `F12` на клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="8cb63-126">Launch F12 by either navigating to the **More (...)** button and selecting **F12 Developer Tools** or by pressing `F12` on your keyboard.</span></span>  
1.  <span data-ttu-id="8cb63-127">Перейдите к сценарию контента расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="8cb63-127">Navigate to and select your extension's content script.</span></span>  <span data-ttu-id="8cb63-128">Сценарии контента для расширений, запущенных в настоящее время, будут показаны в разных папках для каждого расширения.</span><span class="sxs-lookup"><span data-stu-id="8cb63-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="8cb63-129">Будут отображаться только сценарии содержимого.</span><span class="sxs-lookup"><span data-stu-id="8cb63-129">Only running content scripts will appear.</span></span>  
    
1.  <span data-ttu-id="8cb63-130">Поместите точки разлада для отладки, щелкнув слева от номера строки кода.</span><span class="sxs-lookup"><span data-stu-id="8cb63-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12 с отладка сценария контента](../media/debug-content-f12.png)  
    
1.  <span data-ttu-id="8cb63-132">Обновите вкладку браузера, чтобы начать шаг, хотя код.</span><span class="sxs-lookup"><span data-stu-id="8cb63-132">Refresh the browser tab to begin stepping though your code.</span></span>  
    
## <a name="extension-page-debugging"></a><span data-ttu-id="8cb63-133">Отладка страницы расширения</span><span class="sxs-lookup"><span data-stu-id="8cb63-133">Extension page debugging</span></span>  

<span data-ttu-id="8cb63-134">Существует два метода, которые можно использовать для доступа к исходным кодам страницы расширения для отладки.</span><span class="sxs-lookup"><span data-stu-id="8cb63-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span>  <span data-ttu-id="8cb63-135">Один метод применяется к различным страницам, а другой работает только для всплывающих страниц.</span><span class="sxs-lookup"><span data-stu-id="8cb63-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>  

### <a name="debugging-any-extension-page"></a><span data-ttu-id="8cb63-136">Отладка любой страницы расширения</span><span class="sxs-lookup"><span data-stu-id="8cb63-136">Debugging any extension page</span></span>  

<span data-ttu-id="8cb63-137">Следующий метод работает для всех страниц расширения, таких как страница параметры и всплывающие всплывающие ок.</span><span class="sxs-lookup"><span data-stu-id="8cb63-137">The following method works for all extension pages like the options page and popups:</span></span>  

1.  <span data-ttu-id="8cb63-138">Щелкните правой кнопкой мыши на фоне страницы.</span><span class="sxs-lookup"><span data-stu-id="8cb63-138">Right-click on the background of your page.</span></span>  
1.  <span data-ttu-id="8cb63-139">Выберите **источник Представления**.</span><span class="sxs-lookup"><span data-stu-id="8cb63-139">Select **View source**.</span></span>  
    
    ![Откройте отладку всплывающих веяния с помощью f12](../media/debug-popup-select.png)  
    
1.  <span data-ttu-id="8cb63-141">Как только откроется F12, разбей точки в файле, который нужно отламыть.</span><span class="sxs-lookup"><span data-stu-id="8cb63-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>  
    
    ![отладка всплывающих окей с помощью f12](../media/debug-popup-f12.png)  
    
1.  <span data-ttu-id="8cb63-143">Выберите **вкладку Консоли** и выполните `location.reload()` команду.</span><span class="sxs-lookup"><span data-stu-id="8cb63-143">Select the **Console** tab and execute the command `location.reload()`.</span></span>  <span data-ttu-id="8cb63-144">Это позволит повторно выполнить сценарий страницы, что позволит выполнить выполнение кода.</span><span class="sxs-lookup"><span data-stu-id="8cb63-144">This will re-execute the page script, allowing you to step through your code.</span></span>  
    
    ![консоль с входом location.reload](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a><span data-ttu-id="8cb63-146">Отладка страницы расширения всплывающих страниц</span><span class="sxs-lookup"><span data-stu-id="8cb63-146">Debugging a popup extension page</span></span>  

<span data-ttu-id="8cb63-147">Хотя метод отладки страниц расширения также применяется к всплывающее расширение страниц, следующие шаги наметить другой способ отладки всплывающее:</span><span class="sxs-lookup"><span data-stu-id="8cb63-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>  

1.  <span data-ttu-id="8cb63-148">Щелкните правой кнопкой мыши значок расширения.</span><span class="sxs-lookup"><span data-stu-id="8cb63-148">Right-click your extension's icon.</span></span>  
1.  <span data-ttu-id="8cb63-149">Выберите **всплывающее всплыва**</span><span class="sxs-lookup"><span data-stu-id="8cb63-149">Select **Inspect popup**.</span></span>  
    
    ![проверка отлагива](../media/debug-popup-inspect.png)  
    
1.  <span data-ttu-id="8cb63-151">Выполните действия 3 и 4 выше, чтобы разместить точки разрыва и перезагрузить всплывающее всплывающее всплывающее помещение.</span><span class="sxs-lookup"><span data-stu-id="8cb63-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>  
    