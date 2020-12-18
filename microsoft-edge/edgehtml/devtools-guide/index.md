---
description: Знакомство со средствами разработчика в Microsoft Edge (EdgeHTML)
title: Средства разработчика в Microsoft Edge (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 89fdbcdf10d10c57836067ca7d02afa3fd48cbc9
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235361"
---
# <span data-ttu-id="a0a21-104">Средства разработчика в Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a0a21-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](../includes/new-devtools-version-note.md)]  

<span data-ttu-id="a0a21-105">Средства разработчика в Microsoft EDGE (EdgeHTML) созданы с помощью [TypeScript][|::ref1::|Index] на платформе с [открытым исходным кодом][GithubMicrosoftChakracore], оптимизированным для современных интерфейсных рабочих процессов. Теперь Средства разработчика стали доступны в виде [отдельного приложения Windows 10][MicrosoftStoreEdgeDevtoolsPreview] в магазине Microsoft Store!</span><span class="sxs-lookup"><span data-stu-id="a0a21-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="a0a21-106">Дополнительные сведения о новых возможностях см. в статье [Средства разработчика в последнем обновлении Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="a0a21-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="a0a21-107">Основные средства</span><span class="sxs-lookup"><span data-stu-id="a0a21-107">Core tools</span></span>  

:::image type="complex" source="./media/devtools.png" alt-text="Средства разработчика в Microsoft Edge (EdgeHTML)":::
   <span data-ttu-id="a0a21-109">Средства разработчика в Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="a0a21-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="a0a21-110">Средства разработчика в Microsoft Edge \(EdgeHTML\) включают следующее:</span><span class="sxs-lookup"><span data-stu-id="a0a21-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="a0a21-111">Панель [Элементы][DevtoolsGuideEdgehtml|::ref2::|] для редактирования HTML и CSS, изучения свойств специальных возможностей, просмотра прослушивателей событий и определения точек останова для изменений DOM</span><span class="sxs-lookup"><span data-stu-id="a0a21-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="a0a21-112">[Консоль][DevtoolsGuideEdgehtml|::ref3::|] для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также для запуска JavaScript в контексте выбранного окна или кадра</span><span class="sxs-lookup"><span data-stu-id="a0a21-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="a0a21-113">[Отладчик][DevtoolsGuideEdgehtml|::ref4::|] для пошагового выполнения кода, настройки контрольных значений и точек останова, динамического редактирования кода и проверки кэша веб-хранилища и файлов cookie</span><span class="sxs-lookup"><span data-stu-id="a0a21-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="a0a21-114">Панель [Сеть][DevtoolsGuideEdgehtml|::ref5::|] для отслеживания и проверки запросов и ответов из кэша сети и браузера</span><span class="sxs-lookup"><span data-stu-id="a0a21-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="a0a21-115">Панель [Производительность][DevtoolsGuideEdgehtml|::ref6::|] для профилирования времени и системных ресурсов, запрашиваемых вашим сайтом</span><span class="sxs-lookup"><span data-stu-id="a0a21-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="a0a21-116">Панель[Память][DevtoolsGuideEdgehtml|::ref7::|] для оценки использования ресурсов памяти и сравнения моментальных снимков кучи в разных состояниях среды выполнения кода.</span><span class="sxs-lookup"><span data-stu-id="a0a21-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="a0a21-117">Панель [Хранилище][DevtoolsGuideEdgehtml|::ref8::|] для просмотра и управления веб-хранилищем, IndexedDB, файлами cookie и кэшированием данных</span><span class="sxs-lookup"><span data-stu-id="a0a21-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="a0a21-118">Панель [Служебные сценарии][DevtoolsGuideEdgehtmlServiceworkers] для управления и отладки своих сервисных сценариев</span><span class="sxs-lookup"><span data-stu-id="a0a21-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="a0a21-119">Панель [Эмуляция][DevtoolsGuideEdgehtml|::ref9::|] для тестирования сайта с помощью различных профилей браузера, разрешений экрана и координат местоположения GPS</span><span class="sxs-lookup"><span data-stu-id="a0a21-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="a0a21-120">Не забудьте отправить свои [отзывы и запросы функций](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span><span class="sxs-lookup"><span data-stu-id="a0a21-120">Please keep sending your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

> [!TIP]
> <span data-ttu-id="a0a21-121">[Тестируйте в Microsoft Edge \ (EdgeHTML\) без использования любого браузера][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="a0a21-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="a0a21-122">Команда Microsoft Edge сотрудничала с [BrowserStack,][BrowserstackEdgehtml], чтобы предоставить возможность бесплатного динамического и автоматизированного тестирования в Microsoft Edge \ (EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="a0a21-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="a0a21-123">Приложение Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="a0a21-123">Microsoft Store app</span></span>  

<span data-ttu-id="a0a21-124">**Средства разработчика Microsoft Edge \(EdgeHTML\)** теперь [доступны][DevtoolsGuideEdgehtmlWhatsnew] в виде автономного [приложения Windows 10 из магазина Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], в дополнение ко встроенным в браузер функциональным средствам \(`F12`\).</span><span class="sxs-lookup"><span data-stu-id="a0a21-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="a0a21-125">В версии из магазина предусмотрена панель **средства выбора** для подключения к открытым локальным и удаленным конечным объектам страницы и макету с вкладками для удобного переключения между экземплярами Средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="a0a21-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="a0a21-126">Локальная отладка</span><span class="sxs-lookup"><span data-stu-id="a0a21-126">Local debugging</span></span>  

<span data-ttu-id="a0a21-127">Для локальной отладки страницы просто запустите приложение Средства разработчика в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a0a21-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="a0a21-128">На панели **Локальные** средства выбора выводится список всех активных процессов EdgeHTML для работы с содержимым, в том числе открытые вкладки Microsoft Edge, выполняемые [PWA][PwasEdgehtmlIndex] \ (процессы `WWAHost.exe`\) и элементы управления[webview][HostingWebview].</span><span class="sxs-lookup"><span data-stu-id="a0a21-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="a0a21-129">Выберите нужный конечный объект, чтобы вложить и открыть новый экземпляр вкладки Средства разработчика.</span><span class="sxs-lookup"><span data-stu-id="a0a21-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source=".//media/chooser_local.png" alt-text="Локальная панель приложения Средства разработчика":::
   <span data-ttu-id="a0a21-131">Локальная панель приложения Средства разработчика</span><span class="sxs-lookup"><span data-stu-id="a0a21-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="a0a21-132">Удаленная отладка</span><span class="sxs-lookup"><span data-stu-id="a0a21-132">Remote debugging</span></span>  

<span data-ttu-id="a0a21-133">Приложение Средства разработчика в Microsoft Edge предлагает базовую поддержку для отладки страниц на удаленном компьютере благодаря новому выпуску [протокола средства разработчика][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="a0a21-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="a0a21-134">В последнем выпуске предусмотрен удаленный доступ к базовым функциям на панелях [Отладчик][DevtoolsGuideEdgehtml|::ref10::|], [Элементы][DevtoolsGuideEdgehtml|::ref11::|] \ (только для чтения) и [Консоль][DevtoolsGuideEdgehtml|::ref12::|].</span><span class="sxs-lookup"><span data-stu-id="a0a21-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="a0a21-135">Удаленная отладка ограничена узлами рабочего стола, на которых выполняется Microsoft Edge \(EdgeHTML), с поддержкой других узлов EdgeHTML и устройств с Windows 10, которые поступят в следующих выпусках.</span><span class="sxs-lookup"><span data-stu-id="a0a21-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="a0a21-136">Чтобы приступить к работе, ознакомьтесь с разделом [*Средства разработчика в Microsoft Edge*][DevtoolsProtocolEdgehtmlClientsEdgePreview] в документации [Протокол средств разработчика][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="a0a21-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./media/chooser_remote.png" alt-text="Удаленная панель приложения Средства разработчика":::
   <span data-ttu-id="a0a21-138">Удаленная панель приложения Средства разработчика</span><span class="sxs-lookup"><span data-stu-id="a0a21-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="a0a21-139">Общие сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="a0a21-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a0a21-140">Все сочетания клавиш были проверены в последней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a21-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="a0a21-141">Если вам не удается использовать сочетание клавиш, то обновите свою копию Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a21-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="a0a21-142">Эти сочетания клавиш управляют главным окном Средств разработчика и должны работать во всех средствах.</span><span class="sxs-lookup"><span data-stu-id="a0a21-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="a0a21-143">Действие</span><span class="sxs-lookup"><span data-stu-id="a0a21-143">Action</span></span> | <span data-ttu-id="a0a21-144">Установленное напрямую доверие</span><span class="sxs-lookup"><span data-stu-id="a0a21-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="a0a21-145">Показать/скрытьСредства разработчика \(открывает последнюю просмотренную панель)</span><span class="sxs-lookup"><span data-stu-id="a0a21-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="a0a21-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="a0a21-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="a0a21-147">Включение или отключение стыковки \(Разблокировать/Внизу/Справа)</span><span class="sxs-lookup"><span data-stu-id="a0a21-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="a0a21-148">Открыть файл</span><span class="sxs-lookup"><span data-stu-id="a0a21-148">Open file</span></span> | `Ctrl`<span data-ttu-id="a0a21-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="a0a21-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="a0a21-150">Отображение не редактируемого открытого исходного HTML-кода в отладчике</span><span class="sxs-lookup"><span data-stu-id="a0a21-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="a0a21-151">Показать или скрыть консоль в нижней части любого другого средства</span><span class="sxs-lookup"><span data-stu-id="a0a21-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="a0a21-152">Переключиться на Элементы \ (проводник DOM)</span><span class="sxs-lookup"><span data-stu-id="a0a21-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="a0a21-153">Переключиться на Консоль</span><span class="sxs-lookup"><span data-stu-id="a0a21-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="a0a21-154">Переключиться в режим Отладчика</span><span class="sxs-lookup"><span data-stu-id="a0a21-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="a0a21-155">Переключиться на Сеть</span><span class="sxs-lookup"><span data-stu-id="a0a21-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="a0a21-156">Переключиться на Производительность</span><span class="sxs-lookup"><span data-stu-id="a0a21-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="a0a21-157">Переключиться на Память</span><span class="sxs-lookup"><span data-stu-id="a0a21-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="a0a21-158">Переключиться на Эмуляцию</span><span class="sxs-lookup"><span data-stu-id="a0a21-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="a0a21-159">Документ справки</span><span class="sxs-lookup"><span data-stu-id="a0a21-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="a0a21-160">Следующее средство</span><span class="sxs-lookup"><span data-stu-id="a0a21-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="a0a21-161">Предыдущее средство</span><span class="sxs-lookup"><span data-stu-id="a0a21-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="a0a21-162">Предыдущее средство \ (из истории)</span><span class="sxs-lookup"><span data-stu-id="a0a21-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="a0a21-163">Следующее средство \ (из истории)</span><span class="sxs-lookup"><span data-stu-id="a0a21-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="a0a21-164">Следующий подкадр</span><span class="sxs-lookup"><span data-stu-id="a0a21-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="a0a21-165">Предыдущий подкадр</span><span class="sxs-lookup"><span data-stu-id="a0a21-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="a0a21-166">Следующее соответствие в поле поиска</span><span class="sxs-lookup"><span data-stu-id="a0a21-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="a0a21-167">Предыдущее соответствие в поле поиска</span><span class="sxs-lookup"><span data-stu-id="a0a21-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="a0a21-168">Поиск в поле поиска</span><span class="sxs-lookup"><span data-stu-id="a0a21-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="a0a21-169">Перемещение фокуса на консоль в нижней части экрана</span><span class="sxs-lookup"><span data-stu-id="a0a21-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="a0a21-170">Запуск Средств разработчика на консоли</span><span class="sxs-lookup"><span data-stu-id="a0a21-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="a0a21-171">Обновить страницу.</span><span class="sxs-lookup"><span data-stu-id="a0a21-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="a0a21-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="a0a21-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="a0a21-173">Если в процессе отладки вы приостановили процесс в точке останова, то используйте действие **Обновить страницу**, чтобы сперва возобновить работу среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="a0a21-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="a0a21-174">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a0a21-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="a0a21-175">Отправьте свой отзыв, чтобы помочь улучшить Microsoft Edge \(EdgeHTML\) Средства разработчика.</span><span class="sxs-lookup"><span data-stu-id="a0a21-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="a0a21-176">Просто откройте средства \(`F12`), а затем нажмите кнопку [Отправить отзыв](#microsoft-edge-edgehtml-developer-tools).</span><span class="sxs-lookup"><span data-stu-id="a0a21-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="a0a21-177">Станьте участником [программы предварительной оценки Windows][WindowsInsiderProgram], чтобы предварительно просматривать [новейшие функции в Средствах разработчика][DevtoolsGuideEdgehtmlWhatsnew]</span><span class="sxs-lookup"><span data-stu-id="a0a21-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="a0a21-178">Используйте приложение Центра отзывов Windows, чтобы публиковать, голосовать, отслеживать и поддерживать общие предложения и вопросы о Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a21-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Консоль"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Отладчик"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Элементы"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Эмуляция"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Память"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Сеть"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Производительность"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Служебные сценарии"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Хранилище"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "Средства разработчика в последнем обновлении для Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Протокол средств разработчика в Microsoft Edge (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительный просмотр Средств разработчика в Microsoft Edge — Клиенты протокола средств разработчика"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) для приложений Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Прогрессивные веб-приложения (EdgeHTML) на Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительный просмотр средств разработчика в Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Программа предварительной оценки Windows"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Браузер Microsoft Edge, бесплатное тестирование | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
