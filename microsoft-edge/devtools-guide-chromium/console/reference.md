---
description: Всестороннюю ссылку на все функции и поведение, связанные с интерфейсом консоли в Microsoft Edge DevTools.
title: Ссылка консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1aed46486240dea19420e8b7cb52b6758f1f528b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399164"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="console-reference"></a><span data-ttu-id="63ede-104">Ссылка консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-104">Console reference</span></span>  

<span data-ttu-id="63ede-105">Эта страница является ссылкой на функции, связанные с консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="63ede-105">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="63ede-106">Предполагается, что вы уже знакомы с использованием консоли для просмотра зарегистрированных сообщений и запуска JavaScript.</span><span class="sxs-lookup"><span data-stu-id="63ede-106">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="63ede-107">Если нет, перейдите к [началу работы с запуском JavaScript в][DevToolsConsoleJavascript] консоли и начать работу с ведением журнала [сообщений в консоли][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="63ede-107">If not, navigate to [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="63ede-108">Если вы ищете ссылку API на такие `console.log()` функции, как, перейдите к [консоли API Reference][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="63ede-108">If you are looking for the API reference on functions like `console.log()`, navigate to [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="63ede-109">Для справки о таких `monitorEvents()` функциях, как, перейдите к [ссылке API консоли utilities][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="63ede-109">For the reference on functions like `monitorEvents()`, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="open-the-console"></a><span data-ttu-id="63ede-110">Откройте консоль</span><span class="sxs-lookup"><span data-stu-id="63ede-110">Open the Console</span></span>  

<span data-ttu-id="63ede-111">Консоль можно **открыть** как [средство](#open-the-console-tool) в верхней области или как средство [в ящике.](#open-the-console-tool-in-the-drawer)</span><span class="sxs-lookup"><span data-stu-id="63ede-111">You may open the **Console** as a [tool in the upper pane](#open-the-console-tool) or as a [tool in the Drawer](#open-the-console-tool-in-the-drawer).</span></span>  

### <a name="open-the-console-tool"></a><span data-ttu-id="63ede-112">Откройте средство Консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-112">Open the Console tool</span></span>  

<span data-ttu-id="63ede-113">Выберите `Control` + `Shift` + `J` \(Windows, Linux\) `Command` + `Option` + `J` или \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="63ede-113">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Средство Консоли" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="63ede-115">Средство **Консоли**</span><span class="sxs-lookup"><span data-stu-id="63ede-115">The **Console** tool</span></span>  
:::image-end:::  

<span data-ttu-id="63ede-116">Чтобы открыть **консольный** инструмент из командного [меню,][DevToolsCommandMenu]начните вводить текст и запустите команду "Показать консоль", рядом с ней имеется значок `Console` \*\*\*\* **Панель.**</span><span class="sxs-lookup"><span data-stu-id="63ede-116">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда, чтобы показать панель консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="63ede-118">Команда, чтобы показать **средство Консоли**</span><span class="sxs-lookup"><span data-stu-id="63ede-118">The command to show the **Console** tool</span></span>  
:::image-end:::  

### <a name="open-the-console-tool-in-the-drawer"></a><span data-ttu-id="63ede-119">Откройте средство Консоли в ящике</span><span class="sxs-lookup"><span data-stu-id="63ede-119">Open the Console tool in the Drawer</span></span>  

<span data-ttu-id="63ede-120">Выберите или выберите Настройка и `Escape` **управление DevTools** `...` \( \) и выберите **ящик консоли Show**.</span><span class="sxs-lookup"><span data-stu-id="63ede-120">Select `Escape` or choose **Customize And Control DevTools** \(`...`\) and then choose **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Показать ящик консоли" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="63ede-122">Показать ящик консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-122">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="63ede-123">Ящик всплывет в нижней части окна DevTools с открытым средством **консоли.**</span><span class="sxs-lookup"><span data-stu-id="63ede-123">The Drawer pops up at the bottom of your DevTools window, with the **Console** tool open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Средство консоли в ящике" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="63ede-125">Средство **консоли** в **ящике**</span><span class="sxs-lookup"><span data-stu-id="63ede-125">The **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="63ede-126">Чтобы открыть **консольный** инструмент из командного [меню,][DevToolsCommandMenu]начните вводить текст и запустите команду "Показать консоль", рядом с ней имеется значок `Console` \*\*\*\* **Ящика.**</span><span class="sxs-lookup"><span data-stu-id="63ede-126">To open the **Console** tool from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда, чтобы показать средство **Console** в ящике" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="63ede-128">Команда, чтобы показать **консольный** инструмент в **ящике**</span><span class="sxs-lookup"><span data-stu-id="63ede-128">The command to show the **Console** tool in the **Drawer**</span></span>  
:::image-end:::  

### <a name="open-console-settings"></a><span data-ttu-id="63ede-129">Параметры открытой консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-129">Open Console Settings</span></span>  

<span data-ttu-id="63ede-130">Выберите **параметры** консоли \. ![ Значок Параметры ][ImageSettingsButtonIcon] консоли \).</span><span class="sxs-lookup"><span data-stu-id="63ede-130">Choose **Console Settings** \(![Console Settings icon][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Параметры консоли" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="63ede-132">Параметры консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-132">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="63ede-133">Ссылки ниже объясняют каждый параметр:</span><span class="sxs-lookup"><span data-stu-id="63ede-133">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="63ede-134">Скрыть сеть</span><span class="sxs-lookup"><span data-stu-id="63ede-134">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="63ede-135">Сохранение журнала</span><span class="sxs-lookup"><span data-stu-id="63ede-135">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="63ede-136">Только выбранный контекст</span><span class="sxs-lookup"><span data-stu-id="63ede-136">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="63ede-137">Группа Similar</span><span class="sxs-lookup"><span data-stu-id="63ede-137">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="63ede-138">Журнал XmlHttpRequests</span><span class="sxs-lookup"><span data-stu-id="63ede-138">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="63ede-139">Оценка с желанием</span><span class="sxs-lookup"><span data-stu-id="63ede-139">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="63ede-140">Автозаполнеть из истории</span><span class="sxs-lookup"><span data-stu-id="63ede-140">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <a name="open-the-console-sidebar"></a><span data-ttu-id="63ede-141">Откройте боковую панель консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-141">Open the Console Sidebar</span></span>  

<span data-ttu-id="63ede-142">Выберите **боковую панель** консоли показать \. Показать боковую панель консоли \) для демонстрации боковой панели, которая полезна ![ для ][ImageShowConsoleSidebarIcon] фильтрации.</span><span class="sxs-lookup"><span data-stu-id="63ede-142">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Боковая панель консоли" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="63ede-144">**Консоль** Боковая панель</span><span class="sxs-lookup"><span data-stu-id="63ede-144">**Console** Sidebar</span></span>  
:::image-end:::  

## <a name="view-messages"></a><span data-ttu-id="63ede-145">Просмотр сообщений</span><span class="sxs-lookup"><span data-stu-id="63ede-145">View messages</span></span>  

<span data-ttu-id="63ede-146">В этом разделе содержатся функции, которые изменяют то, как сообщения представлены в консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-146">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="63ede-147">Для практических погон перейдите к [просмотру сообщений.][DevToolsConsoleViewMessages]</span><span class="sxs-lookup"><span data-stu-id="63ede-147">For a hands-on walkthrough, navigate to [View messages][DevToolsConsoleViewMessages].</span></span>  

### <a name="disable-message-grouping"></a><span data-ttu-id="63ede-148">Отключение группировки сообщений</span><span class="sxs-lookup"><span data-stu-id="63ede-148">Disable message grouping</span></span>  

<span data-ttu-id="63ede-149">[Откройте параметры консоли и](#open-console-settings) отключим **группу,** аналогичную отключению поведения группы сообщений по умолчанию консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-149">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="63ede-150">Например, перейдите к запросам [log XHR и Fetch](#log-xhr-and-fetch-requests).</span><span class="sxs-lookup"><span data-stu-id="63ede-150">For an example, navigate to [Log XHR and Fetch requests](#log-xhr-and-fetch-requests).</span></span>  

### <a name="log-xhr-and-fetch-requests"></a><span data-ttu-id="63ede-151">Запросы на журнал XHR и fetch</span><span class="sxs-lookup"><span data-stu-id="63ede-151">Log XHR and Fetch requests</span></span>  

<span data-ttu-id="63ede-152">[Откройте параметры консоли](#open-console-settings) и вйдите **в журнал XMLHttpRequests** для входа всех и запросов в консоль по мере их `XMLHttpRequest` `Fetch` создания.</span><span class="sxs-lookup"><span data-stu-id="63ede-152">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Запросы журнала XMLHttpRequest и Fetch" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="63ede-154">Журнал `XMLHttpRequest` и `Fetch` запросы</span><span class="sxs-lookup"><span data-stu-id="63ede-154">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="63ede-155">В верхнем сообщении на предыдущем рисунке отображается поведение группы консоли по **умолчанию.**</span><span class="sxs-lookup"><span data-stu-id="63ede-155">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <a name="persist-messages-across-page-loads"></a><span data-ttu-id="63ede-156">Упорязать сообщения во всех загрузках страниц</span><span class="sxs-lookup"><span data-stu-id="63ede-156">Persist messages across page loads</span></span>  

<span data-ttu-id="63ede-157">По умолчанию консоль очищается при загрузке новой страницы.</span><span class="sxs-lookup"><span data-stu-id="63ede-157">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="63ede-158">Для сохранения сообщений в разных нагрузках страниц [откройте параметры](#open-console-settings) консоли и вйдите в почтовый ящик **Preserve Log.**</span><span class="sxs-lookup"><span data-stu-id="63ede-158">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <a name="hide-network-messages"></a><span data-ttu-id="63ede-159">Скрыть сетевые сообщения</span><span class="sxs-lookup"><span data-stu-id="63ede-159">Hide network messages</span></span>  

<span data-ttu-id="63ede-160">По умолчанию браузер регистрит сетевые сообщения в **консоли.**</span><span class="sxs-lookup"><span data-stu-id="63ede-160">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="63ede-161">На следующем рисунке выбранное сообщение представляет код состояния HTTP `429` .</span><span class="sxs-lookup"><span data-stu-id="63ede-161">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Сообщение 429 в консоли" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="63ede-163">Сообщение `429` в **консоли**</span><span class="sxs-lookup"><span data-stu-id="63ede-163">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="63ede-164">Чтобы скрыть сетевые сообщения:</span><span class="sxs-lookup"><span data-stu-id="63ede-164">To hide network messages:</span></span>  

1.  <span data-ttu-id="63ede-165">[Параметры открытой консоли](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="63ede-165">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="63ede-166">Включить **почтовый ящик Hide Network.**</span><span class="sxs-lookup"><span data-stu-id="63ede-166">Enable the **Hide Network** checkbox.</span></span>  
    
## <a name="filter-messages"></a><span data-ttu-id="63ede-167">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="63ede-167">Filter messages</span></span>  

<span data-ttu-id="63ede-168">Существует множество способов фильтрации сообщений в консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-168">There are many ways to filter out messages in the Console.</span></span>  

### <a name="filter-out-browser-messages"></a><span data-ttu-id="63ede-169">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="63ede-169">Filter out browser messages</span></span>  

<span data-ttu-id="63ede-170">[Откройте боковую панель консоли](#open-the-console-sidebar) и **выберите сообщения пользователей,** чтобы показать только сообщения, которые поступили из JavaScript страницы.</span><span class="sxs-lookup"><span data-stu-id="63ede-170">[Open the Console Sidebar](#open-the-console-sidebar) and choose **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Просмотр сообщений пользователей" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="63ede-172">Просмотр сообщений пользователей</span><span class="sxs-lookup"><span data-stu-id="63ede-172">View user messages</span></span>  
:::image-end:::  

### <a name="filter-by-log-level"></a><span data-ttu-id="63ede-173">Фильтр по уровню журнала</span><span class="sxs-lookup"><span data-stu-id="63ede-173">Filter by log level</span></span>  

<span data-ttu-id="63ede-174">DevTools назначает каждому `console.*` методу уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="63ede-174">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="63ede-175">Существует 4 уровня: `Verbose` `Info` , , и `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="63ede-175">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="63ede-176">Например, `console.log()` находится в `Info` группе, в то время `console.error()` как в `Error` группе.</span><span class="sxs-lookup"><span data-stu-id="63ede-176">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="63ede-177">Ссылка [на API консоли][DevToolsConsoleApi] описывает уровень серьезности каждого применимого метода.</span><span class="sxs-lookup"><span data-stu-id="63ede-177">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="63ede-178">Каждое сообщение, которое браузер входит в консоль, также имеет уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="63ede-178">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="63ede-179">Вы можете скрыть любой уровень сообщений, который вас не интересует.</span><span class="sxs-lookup"><span data-stu-id="63ede-179">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="63ede-180">Например, если вас интересуют только сообщения, можно скрыть `Error` остальные 3 группы.</span><span class="sxs-lookup"><span data-stu-id="63ede-180">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="63ede-181">Выберите **отсев уровней** журналов, чтобы включить или отключить `Verbose` `Info` `Warning` `Error` сообщения.</span><span class="sxs-lookup"><span data-stu-id="63ede-181">Choose the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Отсев уровней журналов" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="63ede-183">**Отсев уровней** журналов</span><span class="sxs-lookup"><span data-stu-id="63ede-183">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="63ede-184">Вы также можете фильтровать по уровню [журнала,](#open-the-console-sidebar) открыв боковую панель консоли и затем вычеты **ошибок,** \*\*\*\* предупреждений, **info**или **Verbose**.</span><span class="sxs-lookup"><span data-stu-id="63ede-184">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and thenchoosing **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Использование боковой панели для просмотра предупреждений" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="63ede-186">Использование боковой панели для просмотра предупреждений</span><span class="sxs-lookup"><span data-stu-id="63ede-186">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <a name="filter-messages-by-url"></a><span data-ttu-id="63ede-187">Фильтрация сообщений по URL-адресу</span><span class="sxs-lookup"><span data-stu-id="63ede-187">Filter messages by URL</span></span>  

<span data-ttu-id="63ede-188">Введите `url:` url-адрес, чтобы просматривать только сообщения, которые пришли из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="63ede-188">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="63ede-189">После введите `url:` DevTools показывает все релевантные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="63ede-189">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="63ede-190">Домены также работают.</span><span class="sxs-lookup"><span data-stu-id="63ede-190">Domains also work.</span></span>  <span data-ttu-id="63ede-191">Например, если вы и журналируете сообщения, вы можете сосредоточиться на сообщениях `https://example.com/a.js` `https://example.com/b.js` из этих `url:https://example.com` 2 скриптов.</span><span class="sxs-lookup"><span data-stu-id="63ede-191">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Фильтр URL-адреса" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="63ede-193">Фильтр URL-адреса</span><span class="sxs-lookup"><span data-stu-id="63ede-193">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="63ede-194">`-url:`Введите, чтобы скрыть сообщения из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="63ede-194">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="63ede-195">Это называется фильтром отрицательного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="63ede-195">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Отрицательный URL-фильтр, который скрывает все сообщения, которые соответствуют https://b.wal.co URL-адресу" lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="63ede-197">Отрицательный URL-фильтр, который скрывает все сообщения, которые соответствуют `https://b.wal.co` URL-адресу</span><span class="sxs-lookup"><span data-stu-id="63ede-197">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="63ede-198">Вы также можете показывать сообщения из одного URL-адреса, открыв \*\*\*\* боковую панель [консоли,](#open-the-console-sidebar)расширив раздел "Сообщения пользователей", а затем нажав URL-адрес скрипта, содержащий сообщения, на которых необходимо сосредоточиться.</span><span class="sxs-lookup"><span data-stu-id="63ede-198">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and thenchoosing the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Просмотр сообщений, которые поступили из wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="63ede-200">Просмотр сообщений, которые пришли из</span><span class="sxs-lookup"><span data-stu-id="63ede-200">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <a name="filter-out-messages-from-different-contexts"></a><span data-ttu-id="63ede-201">Фильтрация сообщений из разных контекстов</span><span class="sxs-lookup"><span data-stu-id="63ede-201">Filter out messages from different contexts</span></span>  

<span data-ttu-id="63ede-202">Предположим, что на странице есть реклама \(ad\).</span><span class="sxs-lookup"><span data-stu-id="63ede-202">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="63ede-203">В консоль встроено большое количество `<iframe>` сообщений.</span><span class="sxs-lookup"><span data-stu-id="63ede-203">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="63ede-204">Так как это сообщение работает в другом контексте [JavaScript,](#select-javascript-context)одним [](#open-console-settings) из способов скрыть сообщения является открытие параметров консоли и включив выбранный почтовый ящик **Только** контекст.</span><span class="sxs-lookup"><span data-stu-id="63ede-204">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and turn on the **Selected Context Only** checkbox.</span></span>  

### <a name="filter-out-messages-that-do-not-match-a-regular-expression-pattern"></a><span data-ttu-id="63ede-205">Фильтрация сообщений, не совпадает с шаблоном регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="63ede-205">Filter out messages that do not match a regular expression pattern</span></span>  

<span data-ttu-id="63ede-206">Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовом окне **Filter,** чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.</span><span class="sxs-lookup"><span data-stu-id="63ede-206">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="63ede-207">DevTools проверяет, найден ли шаблон в тексте сообщения или скрипте, из-за чего сообщение было в журнале.</span><span class="sxs-lookup"><span data-stu-id="63ede-207">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Фильтрация сообщений, не совпадает с выражением regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="63ede-209">Фильтрация сообщений, не совпадает с `/[gm][ta][mi]/` выражением regex</span><span class="sxs-lookup"><span data-stu-id="63ede-209">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <a name="run-javascript"></a><span data-ttu-id="63ede-210">Запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="63ede-210">Run JavaScript</span></span>  

<span data-ttu-id="63ede-211">В этом разделе содержатся функции, связанные с запуском JavaScript в консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-211">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="63ede-212">Для практических походить перейдите к [запуску JavaScript][DevToolsConsoleOverviewJavascript].</span><span class="sxs-lookup"><span data-stu-id="63ede-212">For a hands-on walkthrough, navigate to [Run JavaScript][DevToolsConsoleOverviewJavascript].</span></span>  

### <a name="re-run-expressions-from-history"></a><span data-ttu-id="63ede-213">Повторное запуск выражений из истории</span><span class="sxs-lookup"><span data-stu-id="63ede-213">Re-run expressions from history</span></span>  

<span data-ttu-id="63ede-214">Выберите ключ для цикла в истории выражений JavaScript, которые были ранее в `Up Arrow` консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-214">Select the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="63ede-215">Выберите, `Enter` чтобы выполнить это выражение еще раз.</span><span class="sxs-lookup"><span data-stu-id="63ede-215">Select `Enter` to run that expression again.</span></span>  

### <a name="watch-the-value-of-an-expression-in-real-time-with-live-expressions"></a><span data-ttu-id="63ede-216">Просмотр значения выражения в режиме реального времени с помощью Live Expressions</span><span class="sxs-lookup"><span data-stu-id="63ede-216">Watch the value of an expression in real-time with Live Expressions</span></span>  

<span data-ttu-id="63ede-217">Если вы напечатаете одно и то же выражение JavaScript в консоли несколько раз, вам может быть проще создать **выражение Live.**</span><span class="sxs-lookup"><span data-stu-id="63ede-217">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="63ede-218">С **помощью Live Expressions** вы введите выражение один раз, а затем прикрепите его к верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="63ede-218">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="63ede-219">Значение обновлений выражения почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="63ede-219">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="63ede-220">Перейдите [к просмотру значений выражения JavaScript в Real-Time с живыми выражениями][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="63ede-220">Navigate to [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <a name="disable-eager-evaluation"></a><span data-ttu-id="63ede-221">Отключение оценки нетерпеливых</span><span class="sxs-lookup"><span data-stu-id="63ede-221">Disable Eager Evaluation</span></span>  

<span data-ttu-id="63ede-222">При вписывке выражений JavaScript в консоли **в режиме "Нетерпеливые** оценки" показан предварительный просмотр возвращаемого значения для этого выражения.</span><span class="sxs-lookup"><span data-stu-id="63ede-222">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="63ede-223">[Откройте параметры консоли и](#open-console-settings) отключите контрольный ящик **"Нетерпеливые** оценки", чтобы отключить предварительные просмотры возвращаемой стоимости.</span><span class="sxs-lookup"><span data-stu-id="63ede-223">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <a name="disable-autocomplete-from-history"></a><span data-ttu-id="63ede-224">Отключение автокомплекта из истории</span><span class="sxs-lookup"><span data-stu-id="63ede-224">Disable autocomplete from history</span></span>  

<span data-ttu-id="63ede-225">При введите выражение, в окне всплывающее окно автокомплета консоли показаны выражения, которые вы запустили ранее.</span><span class="sxs-lookup"><span data-stu-id="63ede-225">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="63ede-226">Эти выражения предварительно примыкают к `>` символу.</span><span class="sxs-lookup"><span data-stu-id="63ede-226">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="63ede-227">[Откройте параметры консоли](#open-console-settings) и отключите автоматический автомат из почтового ящика **"История",** чтобы перестать показывать выражения из вашей истории.</span><span class="sxs-lookup"><span data-stu-id="63ede-227">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="63ede-228">На следующем рисунке `document.querySelector('a')` и `document.querySelector('img')` находятся выражения, которые были оценены ранее.</span><span class="sxs-lookup"><span data-stu-id="63ede-228">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="Всплывающее всплывающее всплывающее окантовка автокомплекта отображает выражения из истории" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="63ede-230">Всплывающее всплывающее всплывающее окантовка автокомплекта отображает выражения из истории</span><span class="sxs-lookup"><span data-stu-id="63ede-230">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <a name="select-javascript-context"></a><span data-ttu-id="63ede-231">Выбор контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="63ede-231">Select JavaScript context</span></span>  

<span data-ttu-id="63ede-232">По умолчанию **выпадение контекста JavaScript** устанавливается на [][MDNBrowsingContext] вершину, \*\*\*\* что представляет контекст просмотра основного документа.</span><span class="sxs-lookup"><span data-stu-id="63ede-232">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Отсев контекста JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="63ede-234">**Отсев контекста JavaScript**</span><span class="sxs-lookup"><span data-stu-id="63ede-234">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="63ede-235">Предположим, у вас есть на странице, встроенная в `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="63ede-235">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="63ede-236">Необходимо запустить JavaScript, чтобы настроить DOM этого ad.</span><span class="sxs-lookup"><span data-stu-id="63ede-236">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="63ede-237">Сначала необходимо выбрать контекст просмотра рекламы из выпадаемого **контекста JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="63ede-237">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Выберите другой контекст JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="63ede-239">Выберите другой контекст JavaScript</span><span class="sxs-lookup"><span data-stu-id="63ede-239">Choose a different JavaScript context</span></span>  
:::image-end:::  

## <a name="clear-the-console"></a><span data-ttu-id="63ede-240">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="63ede-240">Clear the Console</span></span>  

<span data-ttu-id="63ede-241">Для очистки консоли можно использовать любой из следующих процессов:</span><span class="sxs-lookup"><span data-stu-id="63ede-241">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="63ede-242">Выберите **четкую** консоль \. ![ Четкая ][ImageClearConsoleIcon] консоль \).</span><span class="sxs-lookup"><span data-stu-id="63ede-242">Choose **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="63ede-243">Наведите курсор на сообщение, откройте контекстное меню \(righ-click\) и выберите **четкую консоль**.</span><span class="sxs-lookup"><span data-stu-id="63ede-243">Hover on a message, open the contextual menu \(righ-click\), and choose **Clear Console**.</span></span>  
*   <span data-ttu-id="63ede-244">Введите `clear()` консоль **и** выберите `Enter` .</span><span class="sxs-lookup"><span data-stu-id="63ede-244">Enter `clear()` in the **Console** and select `Enter`.</span></span>  
*   <span data-ttu-id="63ede-245">Запуск `console.clear()` с JavaScript для веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="63ede-245">Run `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="63ede-246">Выберите, `Control` + `L` **пока консоль** находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="63ede-246">Select `Control`+`L` while the **Console** is in focus.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="63ede-247">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="63ede-247">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Запустите команды с помощью командного меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Просмотр зарегистрированных сообщений — обзор консоли | Документы Майкрософт"  
[DevToolsConsoleApi]: ./api.md "Справочные | Документы Майкрософт"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Запуск JavaScript — обзор консоли | Документы Майкрософт"  
[DevToolsConsoleJavascript]: ./javascript.md "Начало работы с запуском JavaScript в консоли | Документы Майкрософт"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Просмотр значений выражений JavaScript в режиме реального времени с помощью live Expressions | Документы Майкрософт"  
[DevToolsConsoleLog]: ./log.md "Начало работы с ведением журналов сообщений в консоли | Документы Майкрософт"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочные ссылки на API консоли utilities | Документы Майкрософт"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Просмотр контекста | MDN"  

> [!NOTE]
> <span data-ttu-id="63ede-257">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63ede-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="63ede-258">Оригинальная страница [](https://developers.google.com/web/tools/chrome-devtools/console/reference) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="63ede-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="63ede-260">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="63ede-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
