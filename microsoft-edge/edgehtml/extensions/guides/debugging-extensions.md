---
description: С помощью средств разработчика F12 узнайте, как отлаголать фоновый сценарий расширения, скрипты содержимого и страницы расширений.
title: Расширения — отладка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, веб-разработка, html, javascript, разработчик, отладка, отладка
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 17da1a2badd99dd57bb8b1e3de063fe045b34333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235744"
---
# <span data-ttu-id="7d937-104">Отладка расширений</span><span class="sxs-lookup"><span data-stu-id="7d937-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7d937-105">Вы можете отлалать расширения в Microsoft Edge с помощью средств разработчика F12.</span><span class="sxs-lookup"><span data-stu-id="7d937-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="7d937-106">В следующем видео приводится нестрогая надстройка Microsoft Edge, которая проходит через каждый сценарий отладки и исправит его по пути.</span><span class="sxs-lookup"><span data-stu-id="7d937-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="7d937-107">Дополнительные сведения см. в пошаговом пошаговом инструкции ниже.</span><span class="sxs-lookup"><span data-stu-id="7d937-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="7d937-108">Чтобы воспользоваться преимуществами отладки расширений с помощью F12, необходимо сначала включить функции разработчика в about:flags.</span><span class="sxs-lookup"><span data-stu-id="7d937-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="7d937-109">Дополнительные [сведения о](./adding-and-removing-extensions.md) том, как это сделать, см. в дополнительных сведениях о добавлении и удалении расширений.</span><span class="sxs-lookup"><span data-stu-id="7d937-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="7d937-110">Отладка фонового сценария</span><span class="sxs-lookup"><span data-stu-id="7d937-110">Background script debugging</span></span>
<span data-ttu-id="7d937-111">Чтобы начать отладку фонового сценария расширения:</span><span class="sxs-lookup"><span data-stu-id="7d937-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="7d937-112">Щелкните **"Еще" (...)** и **"Расширения",** чтобы перейти в области расширений.</span><span class="sxs-lookup"><span data-stu-id="7d937-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![кнопка другие](./../media/morebutton.png)
2. <span data-ttu-id="7d937-114">Щелкните расширение, которое нужно отлажать.</span><span class="sxs-lookup"><span data-stu-id="7d937-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="7d937-115">Щелкните **ссылку на фоновую** страницу, чтобы отвести F12 для фонового процесса.</span><span class="sxs-lookup"><span data-stu-id="7d937-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![выбранное представление расширений параметров со ссылкой для проверки](./../media/debug-inspect.png)
4. <span data-ttu-id="7d937-117">Выберите **вкладку "Отладка"** в F12.</span><span class="sxs-lookup"><span data-stu-id="7d937-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="7d937-118">Перейдите к фоновому сценарию расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="7d937-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="7d937-119">Раз поместите точки останова для отладки, щелкнув слева от номера строки кода.</span><span class="sxs-lookup"><span data-stu-id="7d937-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![Консоль f12, в которой показан фоновый сценарий с точками разрыва](./../media/debug-f12-background.png)
7. <span data-ttu-id="7d937-121">Выберите **вкладку "Консоль"** и выполните команду `location.reload()` ".</span><span class="sxs-lookup"><span data-stu-id="7d937-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="7d937-122">Это позволит повторно выполнить фоновый сценарий, что позволит выполнить пошаговую пошаговую проверку кода.</span><span class="sxs-lookup"><span data-stu-id="7d937-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![консоль с введенной ссылкой location.reload](./../media/debug-f12-background-console.png)


## <span data-ttu-id="7d937-124">Отладка скриптов содержимого</span><span class="sxs-lookup"><span data-stu-id="7d937-124">Content script debugging</span></span>
<span data-ttu-id="7d937-125">Чтобы начать отладку скрипта содержимого расширения:</span><span class="sxs-lookup"><span data-stu-id="7d937-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="7d937-126">Запустите F12, нажав кнопку "Еще" **(...)** и выбрав "Средства разработчика **F12"** или нажав клавишу F12.</span><span class="sxs-lookup"><span data-stu-id="7d937-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="7d937-127">Перейдите к скрипту содержимого расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="7d937-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="7d937-128">Сценарии содержимого для запущенных расширений будут показаны в разных папках для каждого расширения.</span><span class="sxs-lookup"><span data-stu-id="7d937-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7d937-129">Будут отображаться только запущенные сценарии содержимого.</span><span class="sxs-lookup"><span data-stu-id="7d937-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="7d937-130">Раз поместите точки останова для отладки, щелкнув слева от номера строки кода.</span><span class="sxs-lookup"><span data-stu-id="7d937-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![f12 с отладка скрипта контента](./../media/debug-content-f12.png)
4. <span data-ttu-id="7d937-132">Обновите вкладку браузера, чтобы начать пошаговую работу кода.</span><span class="sxs-lookup"><span data-stu-id="7d937-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="7d937-133">Отладка страницы расширения</span><span class="sxs-lookup"><span data-stu-id="7d937-133">Extension page debugging</span></span>

<span data-ttu-id="7d937-134">Существует два метода доступа к исходным кодам страницы расширения для отладки.</span><span class="sxs-lookup"><span data-stu-id="7d937-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="7d937-135">Один метод применяется к различным страницам, а другой работает только для всплывающих страниц.</span><span class="sxs-lookup"><span data-stu-id="7d937-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="7d937-136">Отладка любой страницы расширения</span><span class="sxs-lookup"><span data-stu-id="7d937-136">Debugging any extension page</span></span>
<span data-ttu-id="7d937-137">Следующий метод работает для всех страниц расширений, таких как страница параметров и всплывающие меню:</span><span class="sxs-lookup"><span data-stu-id="7d937-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="7d937-138">Щелкните правой кнопкой мыши фон страницы.</span><span class="sxs-lookup"><span data-stu-id="7d937-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="7d937-139">Выберите **"Просмотр источника"**.</span><span class="sxs-lookup"><span data-stu-id="7d937-139">Select **"View source"**.</span></span>

   ![всплывающее отладка с помощью f12 — выберите](./../media/debug-popup-select.png)

3. <span data-ttu-id="7d937-141">После открытия F12 поместите точки останова в файл, который нужно отлалать.</span><span class="sxs-lookup"><span data-stu-id="7d937-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![отладка всплывающих папок с помощью f12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="7d937-143">Выберите **вкладку "Консоль"** и выполните `location.reload()` команду.</span><span class="sxs-lookup"><span data-stu-id="7d937-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="7d937-144">При этом сценарий страницы будет повторно выполняться, что позволяет выполнить пошаговую</span><span class="sxs-lookup"><span data-stu-id="7d937-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![консоль с введенной ссылкой location.reload](./../media/debug-f12-background-console.png)

### <span data-ttu-id="7d937-146">Отладка всплываемой страницы расширения</span><span class="sxs-lookup"><span data-stu-id="7d937-146">Debugging a popup extension page</span></span>
<span data-ttu-id="7d937-147">Хотя метод отладки страниц расширений также применяется к всплывающим страницам расширения, в следующих шагах описан другой способ отладки всплывающее представление:</span><span class="sxs-lookup"><span data-stu-id="7d937-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="7d937-148">Щелкните правой кнопкой мыши значок расширения.</span><span class="sxs-lookup"><span data-stu-id="7d937-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="7d937-149">Выберите **"Проверить всплывающее всплывающее".**</span><span class="sxs-lookup"><span data-stu-id="7d937-149">Select **"Inspect popup"**.</span></span>

   ![проверка всплывающее отлагивание](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="7d937-151">Выполните действия 3 и 4 выше, чтобы разместить точки останова и перезагрузить всплывающее.</span><span class="sxs-lookup"><span data-stu-id="7d937-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
