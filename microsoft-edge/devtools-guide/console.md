---
description: Используйте консольное средство для интерактивной отладки и специальных проверок.
title: DevTools — Console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, Console
ms.custom: seodec18
ms.openlocfilehash: f2733cac57ed5f2364747ee64e669fa83aae41f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571780"
---
# <span data-ttu-id="af211-104">Console (консоль),</span><span class="sxs-lookup"><span data-stu-id="af211-104">Console</span></span>

<span data-ttu-id="af211-105">Средство разработчика консоли в Microsoft Edge регистрирует данные, связанные с веб-страницей, например JavaScript, сетевые запросы и ошибки безопасности.</span><span class="sxs-lookup"><span data-stu-id="af211-105">The Console developer tool in Microsoft Edge logs information that's associated with a webpage, such as JavaScript, network requests, and security errors.</span></span> <span data-ttu-id="af211-106">Вы можете использовать консоль для интерактивной отладки и специального тестирования.</span><span class="sxs-lookup"><span data-stu-id="af211-106">You can use the Console for interactive debugging and ad hoc testing.</span></span> 

<span data-ttu-id="af211-107">Чтобы открыть средство консоли в Microsoft EDGE, нажмите клавишу F12, чтобы открыть окно средства разработчика (или щелкните правой кнопкой мыши на странице, а затем выберите пункт **проверить элемент**).</span><span class="sxs-lookup"><span data-stu-id="af211-107">To open the Console tool in Microsoft Edge, press the F12 key to access the developer tool window (or right-click on the page, and then select **Inspect Element**).</span></span> <span data-ttu-id="af211-108">Затем в верхней части окна щелкните вкладку **консоль** .</span><span class="sxs-lookup"><span data-stu-id="af211-108">Then, select the **Console** tab at the top of the window.</span></span> 

<span data-ttu-id="af211-109">Вы также можете использовать консольное средство для обмена сообщениями с запущенной веб-страницей и с нее.</span><span class="sxs-lookup"><span data-stu-id="af211-109">You can also use the Console tool to communicate to and from a running webpage.</span></span> <span data-ttu-id="af211-110">С помощью консоли вы можете выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="af211-110">You can use the Console to:</span></span>

- <span data-ttu-id="af211-111">Разместите стандартные [ошибки и коды состояния](./console/error-and-status-codes.md) и информационные сообщения по мере выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="af211-111">Post standard [error and status codes](./console/error-and-status-codes.md) and informational messages as your code runs.</span></span>
- <span data-ttu-id="af211-112">Создавайте пользовательские журналы отладки из вызовов [API консоли](./console/console-api.md) , которые включаются в код.</span><span class="sxs-lookup"><span data-stu-id="af211-112">Generate custom debug logs from the [Console API](./console/console-api.md) calls you include in your code.</span></span>
- <span data-ttu-id="af211-113">Предоставьте [командную строку](./console/command-line.md) и интерактивное представление в виде дерева для проверки текущих возвращаемых значений ключевых переменных и функций.</span><span class="sxs-lookup"><span data-stu-id="af211-113">Provide a [command line](./console/command-line.md) and interactive tree view for inspecting current return values of key variables and functions.</span></span>

## <span data-ttu-id="af211-114">Части консоли</span><span class="sxs-lookup"><span data-stu-id="af211-114">Parts of the Console</span></span>

<span data-ttu-id="af211-115">На приведенном ниже рисунке показаны основные части консоли.</span><span class="sxs-lookup"><span data-stu-id="af211-115">The following image shows the key parts of the Console:</span></span>

![Консоль Microsoft Edge DevTools](./media/console.png)

1. <span data-ttu-id="af211-117">**Ошибки**  /  **Предупреждения**  /  **Сведения**  /  Кнопки " **журналы** ": Фильтрация вывода консоли указанным типом.</span><span class="sxs-lookup"><span data-stu-id="af211-117">**Errors** / **Warnings** / **Info** / **Logs** buttons: Filter console output by the specified type.</span></span> <span data-ttu-id="af211-118">Вы можете выбрать несколько кнопок, удерживая нажатой клавишу **CTRL** .</span><span class="sxs-lookup"><span data-stu-id="af211-118">You can multi-select buttons by holding down the **Ctrl** key.</span></span> <span data-ttu-id="af211-119">Кнопка " **все** " полностью удаляет все фильтры.</span><span class="sxs-lookup"><span data-stu-id="af211-119">The **All** button clears all filters.</span></span>

2. <span data-ttu-id="af211-120">Кнопка " **очистить** " (**CTRL + L**): кнопка " **очистить** " очищает текущее отображение консоли.</span><span class="sxs-lookup"><span data-stu-id="af211-120">**Clear** button (**Ctrl+L**): The **Clear** button clears the current console display.</span></span>

3. <span data-ttu-id="af211-121">Флажок **сохранить журнал** : установите флажок **сохранять журнал** , чтобы сохранить вывод на консоли при обновлении страницы, а затем закрыть и снова открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="af211-121">**Preserve Log** check box: Selecting the **Preserve Log** check box persists your console output across page refreshes and closing and reopening DevTools.</span></span> <span data-ttu-id="af211-122">Журнал консоли очищается только при закрытии вкладки или вручную очищается от консоли.</span><span class="sxs-lookup"><span data-stu-id="af211-122">The Console history clears only when the tab is closed or you manually clear the Console.</span></span>

4. <span data-ttu-id="af211-123">**Target (цель**): с помощью раскрывающегося меню **Target** можно переключаться на другой контекст выполнения, например `<iframe>` на страницу или запущенное расширение.</span><span class="sxs-lookup"><span data-stu-id="af211-123">**Target**: Use the **Target** drop-down menu to switch to a different execution context, such as an `<iframe>` in your page or a running extension.</span></span> <span data-ttu-id="af211-124">По умолчанию выделена рамка верхнего уровня на странице.</span><span class="sxs-lookup"><span data-stu-id="af211-124">By default, the top-level frame of your page is selected.</span></span> <span data-ttu-id="af211-125">При наведении указателя мыши на выделенный кадр отображается всплывающая подсказка, на которой показан полный URL-адрес для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="af211-125">Hovering over a selected frame displays a tooltip that shows the full URL for that resource.</span></span>

5. <span data-ttu-id="af211-126">**Показать консоль**  /  Кнопка " **Скрыть консоль** " (**CTRL** +  **&grave;** ): в дополнение к панели консоли вы можете использовать консоль в нижней части панели DevTools, нажав кнопку " **Показать**  /  **Скрыть** консоль".</span><span class="sxs-lookup"><span data-stu-id="af211-126">**Show Console** / **Hide Console** button (**Ctrl**+ **&grave;** ): In addition to the Console panel, you can use the console from the bottom of any other DevTools panel by pressing the **Show Console** / **Hide Console** button.</span></span> <span data-ttu-id="af211-127">Кнопка не действует, когда DevTools открыта на панели консоли.</span><span class="sxs-lookup"><span data-stu-id="af211-127">The button has no effect when DevTools is open to the Console panel.</span></span>
 
6. <span data-ttu-id="af211-128">**Фильтрация журналов** (**CTRL + F**): Вы также можете фильтровать журналы, используя определенную текстовую строку в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="af211-128">**Filter logs** (**Ctrl+F**) : You can also filter logs by using a specific text string in the search box.</span></span>

7. <span data-ttu-id="af211-129">**Отладчик**: выберите любую синюю исходную ссылку, чтобы открыть отладчик DevTools для этой конкретной строки кода для дальнейшей проверки.</span><span class="sxs-lookup"><span data-stu-id="af211-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span></span>

## <span data-ttu-id="af211-130">Горячие</span><span class="sxs-lookup"><span data-stu-id="af211-130">Shortcuts</span></span>

<span data-ttu-id="af211-131">Действие</span><span class="sxs-lookup"><span data-stu-id="af211-131">Action</span></span>                                            | <span data-ttu-id="af211-132">Появивше</span><span class="sxs-lookup"><span data-stu-id="af211-132">Shortcut</span></span>               
:-------------------------------------------------| :----------------------
<span data-ttu-id="af211-133">Запуск DevTools с консолью в фокусе</span><span class="sxs-lookup"><span data-stu-id="af211-133">Launch DevTools with Console in focus</span></span>             | <span data-ttu-id="af211-134">**Клавиша CTRL**  +  **SHIFT**  +  **J**</span><span class="sxs-lookup"><span data-stu-id="af211-134">**Ctrl** + **Shift** + **J**</span></span> 
<span data-ttu-id="af211-135">Переход на консоль</span><span class="sxs-lookup"><span data-stu-id="af211-135">Switch to the Console</span></span>                                 | <span data-ttu-id="af211-136">**Клавиша CTRL**  +  **2**</span><span class="sxs-lookup"><span data-stu-id="af211-136">**Ctrl** + **2**</span></span>           
<span data-ttu-id="af211-137">Показать или скрыть консоль на другой вкладке DevTools</span><span class="sxs-lookup"><span data-stu-id="af211-137">Show/hide the Console from another DevTools tab</span></span>       | <span data-ttu-id="af211-138">**Клавиша CTRL**  +  **&grave;** (задний импульс)</span><span class="sxs-lookup"><span data-stu-id="af211-138">**Ctrl** + **&grave;** (back tick)</span></span>  
<span data-ttu-id="af211-139">Выполнение (однострочная команда)</span><span class="sxs-lookup"><span data-stu-id="af211-139">Execute (single-line command)</span></span>                     | **<span data-ttu-id="af211-140">Ввод</span><span class="sxs-lookup"><span data-stu-id="af211-140">Enter</span></span>**                
<span data-ttu-id="af211-141">Разрыв строки без выполнения (многострочная команда)</span><span class="sxs-lookup"><span data-stu-id="af211-141">Line break without executing (multi-line command)</span></span> | <span data-ttu-id="af211-142">**SHIFT**  +  **Ввод** или **CTRL +**  +  **Ввод**</span><span class="sxs-lookup"><span data-stu-id="af211-142">**Shift** + **Enter** or **Ctrl** + **Enter**</span></span>      
<span data-ttu-id="af211-143">Очистка консоли для всех сообщений</span><span class="sxs-lookup"><span data-stu-id="af211-143">Clear the Console of all messages</span></span>                 | <span data-ttu-id="af211-144">**Клавиша CTRL**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="af211-144">**Ctrl** + **L**</span></span>           
<span data-ttu-id="af211-145">Фильтрация журналов (Установка фокуса на поле поиска)</span><span class="sxs-lookup"><span data-stu-id="af211-145">Filter logs (set focus to search box)</span></span>             | <span data-ttu-id="af211-146">**Клавиша CTRL**  +  **F**</span><span class="sxs-lookup"><span data-stu-id="af211-146">**Ctrl** + **F**</span></span>           
<span data-ttu-id="af211-147">Предложение о принятии автоматического завершения (в фокусе)</span><span class="sxs-lookup"><span data-stu-id="af211-147">Accept auto-completion suggestion (when in focus)</span></span> | <span data-ttu-id="af211-148">**Ввод** или **Табуляция**</span><span class="sxs-lookup"><span data-stu-id="af211-148">**Enter** or **Tab**</span></span>       
<span data-ttu-id="af211-149">Предыдущий или следующий вариант автоматического завершения</span><span class="sxs-lookup"><span data-stu-id="af211-149">Previous/next auto-completion suggestion</span></span>          | <span data-ttu-id="af211-150">**Клавиша** / стрелка вверх **Клавиша Стрелка вниз**</span><span class="sxs-lookup"><span data-stu-id="af211-150">**Up arrow key**/**Down arrow key**</span></span>   


