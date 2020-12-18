---
description: Функции, добавленные в Microsoft Edge DevTools в Windows 10 Fall Creators Update (EdgeHTML 16)
title: DevTools в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft edge, веб-разработка, средства f12, devtools, edgehtml 16
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2d24b6851e843f491e470b18ccc18d559ed5533d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235206"
---
# <span data-ttu-id="7bd62-104">DevTools в Windows 10 Fall Creators Update (EdgeHTML 16)</span><span class="sxs-lookup"><span data-stu-id="7bd62-104">DevTools in the Windows 10 Fall Creators Update (EdgeHTML 16)</span></span>

<span data-ttu-id="7bd62-105">В этом выпуске мы начали основные усилия по рефакторингу DevTools для повышения надежности и производительности, а также добавили ряд новых функций, которые можно начать использовать уже сегодня!</span><span class="sxs-lookup"><span data-stu-id="7bd62-105">With this release we started a major DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today!</span></span> 

<span data-ttu-id="7bd62-106">Вот функции Microsoft Edge DevTools, которые поставляются с [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16).](https://aka.ms/devguide_edgehtml_16)</span><span class="sxs-lookup"><span data-stu-id="7bd62-106">Here are the Microsoft Edge DevTools features that shipped with the [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).</span></span>

## <span data-ttu-id="7bd62-107">Прослушиватели событий предка</span><span class="sxs-lookup"><span data-stu-id="7bd62-107">Ancestor event listeners</span></span> 

<span data-ttu-id="7bd62-108">Теперь **в области** "События" добавлена возможность просмотра прослушивателей событий, зарегистрированных на любом предке выбранного элемента (на панели **"Элементы"),** в дополнение к прослушивателям самого элемента.</span><span class="sxs-lookup"><span data-stu-id="7bd62-108">The **Events** pane now adds the option to view event listeners registered on any ancestor of the currently selected element (in the **Elements** panel), in addition to those on the element itself.</span></span> <span data-ttu-id="7bd62-109">Кроме того, теперь вы можете сгруппить отображение прослушиватель событий по *событиям* или *элементам.*</span><span class="sxs-lookup"><span data-stu-id="7bd62-109">Additionally, you can now group the event listener display by either *Event* or *Element*.</span></span> 

![Области проверки прослушиватель событий](../media/elements_ancestor_events.png)

## <span data-ttu-id="7bd62-111">Точки останова модификации DOM</span><span class="sxs-lookup"><span data-stu-id="7bd62-111">DOM mutation breakpoints</span></span>

<span data-ttu-id="7bd62-112">Теперь вы можете установить точки останова изменения изменения doM, чтобы вламывать отладить каждый раз, когда изменяется выбранный узел элемента.</span><span class="sxs-lookup"><span data-stu-id="7bd62-112">You can now set DOM mutation breakpoints to break into the Debugger whenever a selected element node changes.</span></span> <span data-ttu-id="7bd62-113">На панели **элементов** щелкните rt-щелкните любой элемент в представлении дерева DOM и выберите один или несколько из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="7bd62-113">From the **Elements** panel, rt-click on any element in the DOM tree view and select one or more of the following:</span></span>

 - <span data-ttu-id="7bd62-114">Разрыв на узле удален</span><span class="sxs-lookup"><span data-stu-id="7bd62-114">Break on Node removed</span></span>
 - <span data-ttu-id="7bd62-115">Break on Subtree modified</span><span class="sxs-lookup"><span data-stu-id="7bd62-115">Break on Subtree modified</span></span>
 - <span data-ttu-id="7bd62-116">Изменение приорвать атрибут</span><span class="sxs-lookup"><span data-stu-id="7bd62-116">Break on Attribute modified</span></span>

<span data-ttu-id="7bd62-117">Вы можете управлять своими точками останова в **doM** на панелях **элементов** или **отладки.**</span><span class="sxs-lookup"><span data-stu-id="7bd62-117">You can manage your mutation breakpoints from the **DOM breakpoints** pane in the **Elements** or **Debugger** panels.</span></span>

![DoM breakpoints pane](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="7bd62-119">Поддержка CSS при правиле</span><span class="sxs-lookup"><span data-stu-id="7bd62-119">CSS at-rule support</span></span>

<span data-ttu-id="7bd62-120">Правила CSS "at" (@) теперь представлены среди других объявлений \*\*\*\* правил CSS в области стилей, включая правила анимации (в настоящее время ограничены только для чтения), запросы функций и `@keyframes` `@supports` `@media` запросы.</span><span class="sxs-lookup"><span data-stu-id="7bd62-120">CSS "at" (@) rules are now represented among other CSS rule declarations on the **Styles** pane, including animation `@keyframes` rules (currently limited to read-only), `@supports` feature queries, and `@media` queries.</span></span>

![Проверка CSS на правилах из области стилей DevTools](../media/elements_at_rules.png)

## <span data-ttu-id="7bd62-122">Области шрифтов CSS</span><span class="sxs-lookup"><span data-stu-id="7bd62-122">CSS fonts pane</span></span>

<span data-ttu-id="7bd62-123">Правила CSS теперь имеют собственную выделенную области шрифтов, которая отображает, откуда загружается шрифт `@font-face` *(локальный* или сетевой) \*\*\*\* и сколько символов его использует. \*\*</span><span class="sxs-lookup"><span data-stu-id="7bd62-123">CSS `@font-face` rules now have their own dedicated **Fonts** pane that displays where the font is loaded from (*Local* or *Network*) and how many characters are using it.</span></span> <span data-ttu-id="7bd62-124">Если шрифт загружен из сети, DevTools отобразит правило, которое импортирует его вместе с псевдонимом и типом шрифта.</span><span class="sxs-lookup"><span data-stu-id="7bd62-124">If a font is loaded from the network,  DevTools will display the rule that imported it along with its alias and font type.</span></span>

![Сведения о шрифте CSS](../media/elements_fonts.png)

## <span data-ttu-id="7bd62-126">Поддержка псевдоэлементов CSS</span><span class="sxs-lookup"><span data-stu-id="7bd62-126">CSS pseudo-element support</span></span>

<span data-ttu-id="7bd62-127">Теперь **в** области стилей псевдоэлементы группироваться под собственными заголовками, и их содержимое больше не отображается как перекрестное.</span><span class="sxs-lookup"><span data-stu-id="7bd62-127">The **Styles** pane now groups pseudo-elements under their own headings and no longer displays their content as crossed out.</span></span>

**<span data-ttu-id="7bd62-128">До:</span><span class="sxs-lookup"><span data-stu-id="7bd62-128">Before:</span></span>**
<br>
![Ранее созданный контент был перекрест](../media/gc_before.png)

**<span data-ttu-id="7bd62-130">После:</span><span class="sxs-lookup"><span data-stu-id="7bd62-130">After:</span></span>**
<br>
![Сгенерированное содержимое больше не отображается с помощью загона](../media/gc_after.png)

## <span data-ttu-id="7bd62-132">Улучшения консоли</span><span class="sxs-lookup"><span data-stu-id="7bd62-132">Console improvements</span></span>

<span data-ttu-id="7bd62-133">Панель **консоли** получила отрегулятивную UX-технологию для улучшения качества использования и более быстрого и более простого использования Intellisense.</span><span class="sxs-lookup"><span data-stu-id="7bd62-133">The **Console** panel got a UX overhaul for improved usability and a faster, richer Intellisense experience.</span></span>

<span data-ttu-id="7bd62-134">**До:** 
![ Предыдущая консоль</span><span class="sxs-lookup"><span data-stu-id="7bd62-134">**Before:**
![Previous console</span></span>](../media/console_old.png)

<span data-ttu-id="7bd62-135">**После:** 
![ Новая консоль</span><span class="sxs-lookup"><span data-stu-id="7bd62-135">**After:**
![New console</span></span>](../media/console_new.png)

<span data-ttu-id="7bd62-136">Мы также добавили эти улучшения:</span><span class="sxs-lookup"><span data-stu-id="7bd62-136">We also added these improvements:</span></span>

 -  <span data-ttu-id="7bd62-137">Используется `Shift + Enter` для добавления дополнительной строки в команду перед ее выполнением. `Enter`</span><span class="sxs-lookup"><span data-stu-id="7bd62-137">Use `Shift + Enter` to add an additional line to a command before executing it with `Enter`.</span></span> <span data-ttu-id="7bd62-138">(Ранее была кнопка *переключателя "Переключиться на* многостроковой" или "однострочная".)</span><span class="sxs-lookup"><span data-stu-id="7bd62-138">(Formerly there was a *Switch to multiline/single-line mode* toggle button.)</span></span>

 - <span data-ttu-id="7bd62-139">Поддерживаются следующие новые API:</span><span class="sxs-lookup"><span data-stu-id="7bd62-139">The following new APIs are supported:</span></span>
    - <span data-ttu-id="7bd62-140">[ **Метод console.table(**_object_*_)_* ](../console/console-api.md#organizing-log-output)</span><span class="sxs-lookup"><span data-stu-id="7bd62-140">[**console.table(**_object_*_)_*](../console/console-api.md#organizing-log-output) method</span></span>
    - <span data-ttu-id="7bd62-141">[ **Команда getEventListeners(**_object_*_)_* ](../console/command-line.md#event-listeners)</span><span class="sxs-lookup"><span data-stu-id="7bd62-141">[**getEventListeners(**_object_*_)_*](../console/command-line.md#event-listeners) command</span></span>
    - <span data-ttu-id="7bd62-142">[ **команда keys(object)**__\*__\* ](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="7bd62-142">[**keys(**_object_*_)_*](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="7bd62-143">[ **команда values(object)**__\*__\* ](../console/command-line.md#object-inspection)</span><span class="sxs-lookup"><span data-stu-id="7bd62-143">[**values(**_object_*_)_*](../console/command-line.md#object-inspection) command</span></span>
    - <span data-ttu-id="7bd62-144">[ **$x(**_xpath expression_*_)_* ](../console/command-line.md#dom-selectors) selector</span><span class="sxs-lookup"><span data-stu-id="7bd62-144">[**$x(**_xpath expression_*_)_*](../console/command-line.md#dom-selectors) selector</span></span>

 - <span data-ttu-id="7bd62-145">Теперь поддерживается параметр форматирования [**%c()**](../console/console-api.md#logging-custom-messages)</span><span class="sxs-lookup"><span data-stu-id="7bd62-145">The [**%c()**](../console/console-api.md#logging-custom-messages) formatting parameter is now supported</span></span>

## <span data-ttu-id="7bd62-146">Улучшения отладки</span><span class="sxs-lookup"><span data-stu-id="7bd62-146">Debugging improvements</span></span>

<span data-ttu-id="7bd62-147">Помимо набора новых функций для отладки сотрудников [службы PWA](#progressive-web-app-debugging)и кэша, отладители добавили эти функции:</span><span class="sxs-lookup"><span data-stu-id="7bd62-147">In addition to a suite of new features for debugging your [PWA service workers and cache](#progressive-web-app-debugging), the Debugger added these features:</span></span>

### <span data-ttu-id="7bd62-148">Консолидированная отладка общих ресурсов</span><span class="sxs-lookup"><span data-stu-id="7bd62-148">Consolidated debugging for shared resources</span></span>

<span data-ttu-id="7bd62-149">Даже если на ресурс, например файл, загруженный из CDN, в коде несколько раз ссылается, DevTools теперь предоставляет один экземпляр отладки для этого файла, где можно установить общие точки останова, которые будут побиты независимо от того, на что ссылается этот файл.</span><span class="sxs-lookup"><span data-stu-id="7bd62-149">Even when a resource, such as a file loaded from CDN, is referenced multiple times throughout your code,  DevTools will now provide a single debugging instance for that file where you can then set common breakpoints which will be hit regardless of where that file is referenced.</span></span> <span data-ttu-id="7bd62-150">(Ранее каждая ссылка на сценарий рассматривалась как уникальный ресурс, сопозначалась с отдельным набором точек останова.)</span><span class="sxs-lookup"><span data-stu-id="7bd62-150">(Previously each script reference was considered a unique resource would map to a separate set of breakpoints.)</span></span>

### <span data-ttu-id="7bd62-151">Live edit JavaScript with *Edit-on-idle*</span><span class="sxs-lookup"><span data-stu-id="7bd62-151">Live edit JavaScript with *Edit-on-idle*</span></span>

<span data-ttu-id="7bd62-152">Теперь вы можете редактировать JavaScript в режиме live во время сеанса отладки.</span><span class="sxs-lookup"><span data-stu-id="7bd62-152">You can now edit your JavaScript live during a debugging session.</span></span> <span data-ttu-id="7bd62-153">Эта функция была экспериментальной (за флагом) в предыдущем [выпуске](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) *(Windows 10 Creators Update),* а теперь является постоянной функцией.</span><span class="sxs-lookup"><span data-stu-id="7bd62-153">This feature was experimentally available (behind a flag) in the [previous](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) release and now its a permanent feature.</span></span> <span data-ttu-id="7bd62-154">Просто выберите любой файл \*\*\*\* скрипта на панели отладки, отредактировать, а затем нажмите кнопку **"Сохранить"** (или ) для проверки изменений при следующем запуске `Ctrl+S` этого раздела кода.</span><span class="sxs-lookup"><span data-stu-id="7bd62-154">Simply select any script file from the **Debugger** panel, edit, then click **Save** (or `Ctrl+S`) to test your changes next time that section of code runs.</span></span> 

![Отладка позволяет в режиме жизни редактировать сценарий и отлаживка изменений](../media/debugger_edit_buttons.png) 

<span data-ttu-id="7bd62-156">Нажмите **кнопку "Сравнить документ с исходным",** чтобы просмотреть изменения.</span><span class="sxs-lookup"><span data-stu-id="7bd62-156">Click the **Compare document to original** button to view the diff of what you changed.</span></span>

![Diff view of edited code in the Debugger](../media/debugger_edit_code.png) 

<span data-ttu-id="7bd62-158">Помните о следующих ограничениях:</span><span class="sxs-lookup"><span data-stu-id="7bd62-158">Please be aware of the following constraints:</span></span>

- <span data-ttu-id="7bd62-159">Редактирование сценариев работает только во внешних *JS-файлах* (и не `<script>` внедрено в *HTML)*</span><span class="sxs-lookup"><span data-stu-id="7bd62-159">Script editing only works in external *.js* files (and not embedded `<script>` within *.html*)</span></span>
- <span data-ttu-id="7bd62-160">Изменения сохраняются в памяти и очищаются при повторной загрузке документа, поэтому вы не сможете запускать изменения в обработке, например `DOMContentLoaded`</span><span class="sxs-lookup"><span data-stu-id="7bd62-160">Edits are saved in memory and flushed when the document is reloaded, thus you won’t be able to run edits inside a `DOMContentLoaded` handler, for example</span></span>
- <span data-ttu-id="7bd62-161">В настоящее время не существует \*\*\*\* способа (например, параметр "Сохранить как"), чтобы сохранить изменения на диске из DevTools</span><span class="sxs-lookup"><span data-stu-id="7bd62-161">Currently there’s no way (such as a **Save As** option) to save your edits to disk from  DevTools</span></span>

## <span data-ttu-id="7bd62-162">Ярлыки</span><span class="sxs-lookup"><span data-stu-id="7bd62-162">Shortcuts</span></span>

<span data-ttu-id="7bd62-163">Теперь можно запустить DevTools на последней просматриваемой панели () или непосредственно в консоли ( ), как и в других `Ctrl+Shift+I` `Ctrl+Shift+J` основных браузерах.</span><span class="sxs-lookup"><span data-stu-id="7bd62-163">You can now launch DevTools to the last viewed panel (`Ctrl+Shift+I`) or directly to the Console (`Ctrl+Shift+J`) just like you would on other major browsers.</span></span>

## <span data-ttu-id="7bd62-164">Постепенная отладка веб-приложений</span><span class="sxs-lookup"><span data-stu-id="7bd62-164">Progressive Web App debugging</span></span>

<span data-ttu-id="7bd62-165">Протестировать экспериментальную поддержку для progressive Web Apps (PWAs) в Microsoft \*\*\*\* Edge и DevTools, выбрав параметр "Включить сотрудников службы" (и перезапустив `about:flags` Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="7bd62-165">Test out the experimental support for Progressive Web Apps (PWAs) in Microsoft Edge and  DevTools by selecting the **Enable service workers** option from `about:flags` (and restarting Microsoft Edge).</span></span> <span data-ttu-id="7bd62-166">Если на сайте \*\*\*\* используются рабочие работники и/или **API** кэша, \*\*\*\* будут заполняться записи в панели отладки для каждого источника аналогично работе веб-хранилища и проверки файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="7bd62-166">If a site makes use of **Service Workers** and/or the **Cache** API,  will populate entries in the **Debugger** panel for each origin, similar to how web storage and cookie inspection work.</span></span>

<span data-ttu-id="7bd62-167">Если щелкнуть определенную запись рабочего \*\*\*\* сотрудника службы, откроется "Обзор рабочего сотрудника службы", где можно управлять регистрацией рабочих служб для данной области и принудительно использовать тестовую push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="7bd62-167">Clicking on a specific service worker entry will open up the **Service Worker Overview**, where you can manage the service worker registration for the given scope and force a test push notification.</span></span> <span data-ttu-id="7bd62-168">Вы также можете **остановить запуск**отдельных сотрудников служб и проверить их в отдельном окне / \*\*\*\* отладки: \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7bd62-168">You can also **Stop**/**Start** individual service workers and **Inspect** them from a separate debugger window:</span></span>

![Обзорная области "Рабочий работник службы"](../media/debugger_sw_overview.png)

<span data-ttu-id="7bd62-170">Обратите внимание на следующие вопросы об отладке рабочих служб:</span><span class="sxs-lookup"><span data-stu-id="7bd62-170">Please note the following about service worker debugging:</span></span>

 - <span data-ttu-id="7bd62-171">Отладка сотрудника службы запускает новый экземпляр DevTools отдельно от средств страницы, так как сотрудники службы могут совместно использовать несколько вкладок.</span><span class="sxs-lookup"><span data-stu-id="7bd62-171">Debugging a service worker will launch a new instance of the DevTools separate from the page's tools because service workers can be shared across multiple tabs.</span></span> 
 - <span data-ttu-id="7bd62-172">Элементы [и](../elements.md) [](../emulation.md) панели эмуляции отсутствуют в отладке рабочего отладка службы, поскольку сотрудники службы работают в фоновом режиме и не управляют напрямую на переднем плане приложения.</span><span class="sxs-lookup"><span data-stu-id="7bd62-172">The [Elements](../elements.md) and [Emulation](../emulation.md) panels are absent from the service worker debugger, given that service workers run in the background and do not directly control the front-end of your app.</span></span>
 - <span data-ttu-id="7bd62-173">В настоящее время сетевой трафик для сотрудника службы передается только из экземпляра отладки DevTools для этого рабочего, а не из центрального экземпляра самой страницы.</span><span class="sxs-lookup"><span data-stu-id="7bd62-173">Currently network traffic for a service worker is only reported from the DevTools debugging instance for that worker, and not from the central instance for the page itself.</span></span>

<span data-ttu-id="7bd62-174">Если щелкнуть определенную запись кэша, откроется диспетчер кэша, где можно проверить и \*\* при желании удалить записи кэша *(пары* ключ-значение запроса и ответа). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7bd62-174">Clicking on a specific cache entry will open up the **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs).</span></span>
