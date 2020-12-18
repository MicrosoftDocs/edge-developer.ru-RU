---
description: Используйте средство консоли для интерактивной отладки и нерегламентного тестирования.
title: DevTools — консоль
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, консоль
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472aafa9e6c6fd98ea952804f0e92ed0b774f59c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235388"
---
# <span data-ttu-id="b551d-104">Консоль</span><span class="sxs-lookup"><span data-stu-id="b551d-104">Console</span></span>

<span data-ttu-id="b551d-105">Средство разработчика консоли в Microsoft Edge записи в журнал сведений, связанных с веб-страницей, таких как JavaScript, сетевые запросы и ошибки безопасности.</span><span class="sxs-lookup"><span data-stu-id="b551d-105">The Console developer tool in Microsoft Edge logs information that's associated with a webpage, such as JavaScript, network requests, and security errors.</span></span> <span data-ttu-id="b551d-106">Консоль можно использовать для интерактивной отладки и тестирования.</span><span class="sxs-lookup"><span data-stu-id="b551d-106">You can use the Console for interactive debugging and ad hoc testing.</span></span> 

<span data-ttu-id="b551d-107">Чтобы открыть консоль в Microsoft Edge, нажмите клавишу F12, чтобы открыть окно средства разработчика (или щелкните страницу правой кнопкой мыши и выберите элемент **Inspect).**</span><span class="sxs-lookup"><span data-stu-id="b551d-107">To open the Console tool in Microsoft Edge, press the F12 key to access the developer tool window (or right-click on the page, and then select **Inspect Element**).</span></span> <span data-ttu-id="b551d-108">Затем выберите **вкладку "Консоль"** в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="b551d-108">Then, select the **Console** tab at the top of the window.</span></span> 

<span data-ttu-id="b551d-109">Вы также можете использовать консоль для связи с запущенной веб-страницей и из нее.</span><span class="sxs-lookup"><span data-stu-id="b551d-109">You can also use the Console tool to communicate to and from a running webpage.</span></span> <span data-ttu-id="b551d-110">Консоль можно использовать для:</span><span class="sxs-lookup"><span data-stu-id="b551d-110">You can use the Console to:</span></span>

- <span data-ttu-id="b551d-111">Публикация [стандартных кодов ошибок и состояния](./console/error-and-status-codes.md) и информационных сообщений при запуске кода.</span><span class="sxs-lookup"><span data-stu-id="b551d-111">Post standard [error and status codes](./console/error-and-status-codes.md) and informational messages as your code runs.</span></span>
- <span data-ttu-id="b551d-112">Создавать пользовательские журналы отлаки из вызовов [API](./console/console-api.md) консоли, которые вы включаете в свой код.</span><span class="sxs-lookup"><span data-stu-id="b551d-112">Generate custom debug logs from the [Console API](./console/console-api.md) calls you include in your code.</span></span>
- <span data-ttu-id="b551d-113">Предоставление [командной строки](./console/command-line.md) и интерактивного древовидного представления для проверки текущих возвращаемых значений ключевых переменных и функций.</span><span class="sxs-lookup"><span data-stu-id="b551d-113">Provide a [command line](./console/command-line.md) and interactive tree view for inspecting current return values of key variables and functions.</span></span>

## <span data-ttu-id="b551d-114">Части консоли</span><span class="sxs-lookup"><span data-stu-id="b551d-114">Parts of the Console</span></span>

<span data-ttu-id="b551d-115">На следующем рисунке показаны основные части консоли:</span><span class="sxs-lookup"><span data-stu-id="b551d-115">The following image shows the key parts of the Console:</span></span>

![Консоль Microsoft Edge DevTools](./media/console.png)

1. <span data-ttu-id="b551d-117">**Ошибки**  /  **Предупреждения**  /  **Сведения**  /  **Журнал кнопок:** фильтровать выходные данные консоли по указанному типу.</span><span class="sxs-lookup"><span data-stu-id="b551d-117">**Errors** / **Warnings** / **Info** / **Logs** buttons: Filter console output by the specified type.</span></span> <span data-ttu-id="b551d-118">Вы можете выбрать несколько кнопок, удерживая клавишу **CTRL.**</span><span class="sxs-lookup"><span data-stu-id="b551d-118">You can multi-select buttons by holding down the **Ctrl** key.</span></span> <span data-ttu-id="b551d-119">Кнопка **"Все"** очищает все фильтры.</span><span class="sxs-lookup"><span data-stu-id="b551d-119">The **All** button clears all filters.</span></span>

2. <span data-ttu-id="b551d-120">**Кнопка "Очистить"** **(CTRL+L):** кнопка **"Очистить"** очищает текущий экран консоли.</span><span class="sxs-lookup"><span data-stu-id="b551d-120">**Clear** button (**Ctrl+L**): The **Clear** button clears the current console display.</span></span>

3. <span data-ttu-id="b551d-121">**Сохраняйте** журнал: \*\*\*\* при выборе этого окне выходные данные консоли сохраняются при обновлении страницы, закрытии и повторном закрытии DevTools.</span><span class="sxs-lookup"><span data-stu-id="b551d-121">**Preserve Log** check box: Selecting the **Preserve Log** check box persists your console output across page refreshes and closing and reopening DevTools.</span></span> <span data-ttu-id="b551d-122">История консоли очищается только при закрытии вкладки или при очистке консоли вручную.</span><span class="sxs-lookup"><span data-stu-id="b551d-122">The Console history clears only when the tab is closed or you manually clear the Console.</span></span>

4. <span data-ttu-id="b551d-123">**Target**: Используйте **целевое** меню для переключения на другой контекст выполнения, например на странице или `<iframe>` в запущенном расширении.</span><span class="sxs-lookup"><span data-stu-id="b551d-123">**Target**: Use the **Target** drop-down menu to switch to a different execution context, such as an `<iframe>` in your page or a running extension.</span></span> <span data-ttu-id="b551d-124">По умолчанию выбран кадр верхнего уровня страницы.</span><span class="sxs-lookup"><span data-stu-id="b551d-124">By default, the top-level frame of your page is selected.</span></span> <span data-ttu-id="b551d-125">При наведении курсор на выбранный кадр отображается tooltip, которая отображает полный URL-адрес для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="b551d-125">Hovering over a selected frame displays a tooltip that shows the full URL for that resource.</span></span>

5. <span data-ttu-id="b551d-126">**Показать консоль**  /  **Скрытие** кнопки консоли (**CTRL):** помимо панели консоли можно использовать консоль в нижней части любой другой панели +  **&grave;** DevTools, нажав кнопку **"Показать**консоль скрытие  /  **консоли".**</span><span class="sxs-lookup"><span data-stu-id="b551d-126">**Show Console** / **Hide Console** button (**Ctrl**+ **&grave;** ): In addition to the Console panel, you can use the console from the bottom of any other DevTools panel by pressing the **Show Console** / **Hide Console** button.</span></span> <span data-ttu-id="b551d-127">Кнопка не действует, если DevTools открыт на панели консоли.</span><span class="sxs-lookup"><span data-stu-id="b551d-127">The button has no effect when DevTools is open to the Console panel.</span></span>
 
6. <span data-ttu-id="b551d-128">**Журналы фильтров** (**CTRL+F).** Вы также можете фильтровать журналы, используя определенную текстовую строку в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="b551d-128">**Filter logs** (**Ctrl+F**) : You can also filter logs by using a specific text string in the search box.</span></span>

7. <span data-ttu-id="b551d-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span><span class="sxs-lookup"><span data-stu-id="b551d-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span></span>

## <span data-ttu-id="b551d-130">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="b551d-130">Shortcuts</span></span>

<span data-ttu-id="b551d-131">Действие</span><span class="sxs-lookup"><span data-stu-id="b551d-131">Action</span></span>                                            | <span data-ttu-id="b551d-132">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="b551d-132">Shortcut</span></span>               
:-------------------------------------------------| :----------------------
<span data-ttu-id="b551d-133">Запуск DevTools с консоли в фокусе</span><span class="sxs-lookup"><span data-stu-id="b551d-133">Launch DevTools with Console in focus</span></span>             | <span data-ttu-id="b551d-134">**CTRL**  +  **Shift**  +  **J**</span><span class="sxs-lookup"><span data-stu-id="b551d-134">**Ctrl** + **Shift** + **J**</span></span> 
<span data-ttu-id="b551d-135">Переход на консоль</span><span class="sxs-lookup"><span data-stu-id="b551d-135">Switch to the Console</span></span>                                 | <span data-ttu-id="b551d-136">**CTRL**  +  **2**</span><span class="sxs-lookup"><span data-stu-id="b551d-136">**Ctrl** + **2**</span></span>           
<span data-ttu-id="b551d-137">Показать или скрыть консоль на другой вкладке DevTools</span><span class="sxs-lookup"><span data-stu-id="b551d-137">Show/hide the Console from another DevTools tab</span></span>       | <span data-ttu-id="b551d-138">**CTRL**  +  **&grave;** (такт назад)</span><span class="sxs-lookup"><span data-stu-id="b551d-138">**Ctrl** + **&grave;** (back tick)</span></span>  
<span data-ttu-id="b551d-139">Execute (одностровая команда)</span><span class="sxs-lookup"><span data-stu-id="b551d-139">Execute (single-line command)</span></span>                     | **<span data-ttu-id="b551d-140">Ввод</span><span class="sxs-lookup"><span data-stu-id="b551d-140">Enter</span></span>**                
<span data-ttu-id="b551d-141">Разрыв строки без выполнения (многостроковая команда)</span><span class="sxs-lookup"><span data-stu-id="b551d-141">Line break without executing (multi-line command)</span></span> | <span data-ttu-id="b551d-142">**Shift**  +  **Ввод** или **ввод с CTRL**  +  \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b551d-142">**Shift** + **Enter** or **Ctrl** + **Enter**</span></span>      
<span data-ttu-id="b551d-143">Очистка консоли всех сообщений</span><span class="sxs-lookup"><span data-stu-id="b551d-143">Clear the Console of all messages</span></span>                 | <span data-ttu-id="b551d-144">**CTRL**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="b551d-144">**Ctrl** + **L**</span></span>           
<span data-ttu-id="b551d-145">Журналы фильтра (установите фокус на поле поиска)</span><span class="sxs-lookup"><span data-stu-id="b551d-145">Filter logs (set focus to search box)</span></span>             | <span data-ttu-id="b551d-146">**CTRL**  +  **F**</span><span class="sxs-lookup"><span data-stu-id="b551d-146">**Ctrl** + **F**</span></span>           
<span data-ttu-id="b551d-147">Принятие предложения автоматического завершения (когда в фокусе)</span><span class="sxs-lookup"><span data-stu-id="b551d-147">Accept auto-completion suggestion (when in focus)</span></span> | <span data-ttu-id="b551d-148">**Ввод** или **вкладка**</span><span class="sxs-lookup"><span data-stu-id="b551d-148">**Enter** or **Tab**</span></span>       
<span data-ttu-id="b551d-149">Предыдущее/следующее предложение автоматического завершения</span><span class="sxs-lookup"><span data-stu-id="b551d-149">Previous/next auto-completion suggestion</span></span>          | <span data-ttu-id="b551d-150">**Клавиша со стрелкой вверх** / **Клавиша со стрелкой вниз**</span><span class="sxs-lookup"><span data-stu-id="b551d-150">**Up arrow key**/**Down arrow key**</span></span>   
