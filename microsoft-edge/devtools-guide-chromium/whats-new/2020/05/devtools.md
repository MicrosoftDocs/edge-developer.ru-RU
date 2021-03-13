---
description: Используйте DevTools в режиме высокой контрастности Windows, уравнося клавишами клавиш в DevTools, чтобы Visual Studio код и другие.
title: Новые возможности в DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3264292721d5e4385b0e6d256d042c76182c21c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408327"
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
# <a name="whats-new-in-devtools-microsoft-edge-84"></a><span data-ttu-id="cf13f-104">Новые возможности в DevTools (Microsoft Edge 84)</span><span class="sxs-lookup"><span data-stu-id="cf13f-104">What's new in DevTools (Microsoft Edge 84)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cf13f-105">Объявления из команды Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cf13f-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="cf13f-106">В следующих разделах приводится список объявлений, которые вы, возможно, пропустили из команды Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="cf13f-107">Ознакомьтесь с объявлениями, чтобы попробовать новые возможности в расширениях Кода DevTools, Microsoft Visual Studio и других.</span><span class="sxs-lookup"><span data-stu-id="cf13f-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="cf13f-108">Чтобы оставаться в курсе всех последних и самых больших функций в средствах разработчика, скачайте каналы предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] и следуйте за нами [в Twitter.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="cf13f-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a><span data-ttu-id="cf13f-109">Использование DevTools в режиме высокой контрастности Windows</span><span class="sxs-lookup"><span data-stu-id="cf13f-109">Use the DevTools in Windows high contrast mode</span></span>

<span data-ttu-id="cf13f-110">Теперь Microsoft Edge DevTools отображаются в режиме высокой контрастности, когда Windows находится в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="cf13f-110">The Microsoft Edge DevTools are now displayed in high contrast mode when Windows is in high contrast mode.</span></span>  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools в режиме высокой контрастности" lightbox="../../media/2020/05/high-contrast.msft.png":::
   <span data-ttu-id="cf13f-112">Microsoft Edge DevTools в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="cf13f-112">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-113">[Следуйте инструкциям, чтобы включить режим высокой контрастности в Windows][MicrosoftSupportWindows10HighContrastMode].</span><span class="sxs-lookup"><span data-stu-id="cf13f-113">[Follow the instructions to turn on high contrast mode in Windows][MicrosoftSupportWindows10HighContrastMode].</span></span>  <span data-ttu-id="cf13f-114">Чтобы открыть DevTools в Microsoft Edge, выберите `F12` или `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="cf13f-114">To open the DevTools in Microsoft Edge, select `F12` or `Ctrl`+`Shift`+`I`.</span></span>  <span data-ttu-id="cf13f-115">DevTools отображаются в режиме высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="cf13f-115">The DevTools are displayed in high contrast mode.</span></span>  

> [!NOTE]
> <span data-ttu-id="cf13f-116">Microsoft Edge DevTools в настоящее время поддерживает режим высокой контрастности на Windows, но не на macOS.</span><span class="sxs-lookup"><span data-stu-id="cf13f-116">The Microsoft Edge DevTools currently support high contrast mode on Windows but not on macOS.</span></span>  

<span data-ttu-id="cf13f-117">Проблема Chromium [#1048378][CR1048378]</span><span class="sxs-lookup"><span data-stu-id="cf13f-117">Chromium issue [#1048378][CR1048378]</span></span>  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a><span data-ttu-id="cf13f-118">Совпадение клавиш в DevTools для Visual Studio кода</span><span class="sxs-lookup"><span data-stu-id="cf13f-118">Match keyboard shortcuts in the DevTools to Visual Studio Code</span></span>  

<span data-ttu-id="cf13f-119">Из [отзывов](#getting-in-touch-with-microsoft-edge-devtools-team) и отслеживания общедоступных проблем [Chromium][CRIssuesList]команда Microsoft Edge DevTools узнала, что вы хотите настроить ярлыки клавиатуры в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-119">From your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) and the [Chromium public issue tracker][CRIssuesList], the Microsoft Edge DevTools team learned that you wanted the ability to customize keyboard shortcuts in the DevTools.</span></span>  <span data-ttu-id="cf13f-120">В Microsoft Edge 84 теперь можно соотносят клавиши в DevTools с [кодом Visual Studio,][VisualStudioCode]который является лишь одной из функций, над которыми команда работает для настройки ярлыков.</span><span class="sxs-lookup"><span data-stu-id="cf13f-120">In Microsoft Edge 84, you are now able to match keyboard shortcuts in the DevTools to [Visual Studio Code][VisualStudioCode], which is just one of the features the team is working on for shortcut customization.</span></span>  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Совпадение клавиш в DevTools для Visual Studio кода" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   <span data-ttu-id="cf13f-122">Microsoft Edge DevTools в режиме высокой контрастности</span><span class="sxs-lookup"><span data-stu-id="cf13f-122">The Microsoft Edge DevTools in high contrast mode</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-123">Чтобы попробовать эксперимент, откройте Параметры DevTools, выбрав или выбрав значок Параметры DevTools в правом верхнем углу `?` ![ ][ImageSettingsIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-123">To try the experiment, open DevTools Settings by selecting `?` or choosing the ![DevTools Settings icon][ImageSettingsIcon] icon in the top-right corner of the DevTools.</span></span>  <span data-ttu-id="cf13f-124">Перейдите в раздел **Эксперименты** и проверьте вкладку Включить настраиваемые параметры ярлыков **клавиатуры (требуется перезагрузка).**</span><span class="sxs-lookup"><span data-stu-id="cf13f-124">Navigate to the **Experiments** section and check **Enable custom keyboard shortcuts settings tab (requires reload)**.</span></span>  <span data-ttu-id="cf13f-125">Теперь перезагрузить DevTools, открыть параметры снова и перейти к **разделу Ярлыки.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-125">Now reload the DevTools, open Settings again, and navigate to the **Shortcuts** section.</span></span>  

<span data-ttu-id="cf13f-126">Выберите **DevTools (По умолчанию)** в ярлыках **Match** из предустановленного отсева и **выберите код Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-126">Choose **DevTools (Default)** in the **Match shortcuts from preset** dropdown and select **Visual Studio Code**.</span></span>  <span data-ttu-id="cf13f-127">Ярлыки клавиатуры в DevTools теперь соответствуют ярлыкам для эквивалентных действий в Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="cf13f-127">The keyboard shortcuts in the DevTools now match the shortcuts for equivalent actions in Visual Studio Code.</span></span>  

<span data-ttu-id="cf13f-128">Например, ярлык клавиатуры для прио паузы или продолжения работы скрипта в [Visual Studio коде][VisualStudioCodeShortcuts] `F5` .</span><span class="sxs-lookup"><span data-stu-id="cf13f-128">For example, the keyboard shortcut for pausing or continuing running a script in [Visual Studio Code][VisualStudioCodeShortcuts] is `F5`.</span></span>  <span data-ttu-id="cf13f-129">С предустановленной программой **DevTools (По умолчанию)** этот же ярлык в DevTools есть, но с заранее задаваемой программой Visual Studio, этот ярлык теперь `F8` также \*\*\*\* `F5` .</span><span class="sxs-lookup"><span data-stu-id="cf13f-129">With the **DevTools (Default)** preset, that same shortcut in the DevTools is `F8` but with the **Visual Studio Code** preset, that shortcut is now also `F5`.</span></span>  

<span data-ttu-id="cf13f-130">В настоящее время эта функция доступна в Microsoft Edge 84 в качестве эксперимента, поэтому поделитесь своими [отзывами](#getting-in-touch-with-microsoft-edge-devtools-team) с командой!</span><span class="sxs-lookup"><span data-stu-id="cf13f-130">The feature is currently available in Microsoft Edge 84 as an experiment, so please share your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team) with the team!</span></span>  

<span data-ttu-id="cf13f-131">Проблема Chromium [#174309][CR174309]</span><span class="sxs-lookup"><span data-stu-id="cf13f-131">Chromium issue [#174309][CR174309]</span></span>  

### <a name="remote-debug-surface-duo-emulators"></a><span data-ttu-id="cf13f-132">Эмуляторы Surface Duo удаленного отладки</span><span class="sxs-lookup"><span data-stu-id="cf13f-132">Remote debug Surface Duo emulators</span></span>  

<span data-ttu-id="cf13f-133">Теперь вы можете удаленно отладить веб-контент, работающий в эмуляторе [Surface Duo,][DualScreensAndroidEmulator] используя полную мощность [Microsoft Edge DevTools][DevToolsChromiumGuide].</span><span class="sxs-lookup"><span data-stu-id="cf13f-133">You are now able to remotely debug your web content running in the [Surface Duo emulator][DualScreensAndroidEmulator] using the full power of the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

<span data-ttu-id="cf13f-134">С помощью [эмулятора Surface Duo][DualScreensAndroidEmulator]вы сможете проверить, как отрисовка веб-контента на новом классе складных и двухэкранных устройств.</span><span class="sxs-lookup"><span data-stu-id="cf13f-134">With the [Surface Duo emulator][DualScreensAndroidEmulator], you are able to test how your web content renders on a new class of foldable and dual-screen devices.</span></span>  <span data-ttu-id="cf13f-135">Эмулятор запускает операционную систему Android и предоставляет [приложение Microsoft Edge Android.][AndroidEdge]</span><span class="sxs-lookup"><span data-stu-id="cf13f-135">The emulator runs the Android operating system and provides the [Microsoft Edge Android app][AndroidEdge].</span></span>  <span data-ttu-id="cf13f-136">Загрузите веб-содержимое в [приложение Microsoft Edge и][AndroidEdge] отладите его с помощью Microsoft Edge [DevTools.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="cf13f-136">Load your web content in the [Microsoft Edge app][AndroidEdge] and debug it with the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="Приложение Microsoft Edge, запущенное в эмуляторе Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   <span data-ttu-id="cf13f-138">Приложение Microsoft Edge в эмуляторе Surface Duo</span><span class="sxs-lookup"><span data-stu-id="cf13f-138">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-139">На странице в настольном экземпляре Microsoft Edge показан `edge://inspect` **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs,][PwaIndex] которые работают на эмуляторе [Surface Duo.][DualScreensAndroidEmulator] [][DesktopEdge]</span><span class="sxs-lookup"><span data-stu-id="cf13f-139">The `edge://inspect` page in a desktop instance of [Microsoft Edge][DesktopEdge] shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaIndex] that are running on the [Surface Duo emulator][DualScreensAndroidEmulator].</span></span>  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="На edge://inspect отображается список открытых вкладок в приложении Microsoft Edge, которое работает на эмуляторе" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   <span data-ttu-id="cf13f-141">На странице отображается список открытых вкладок в `edge://inspect` приложении Microsoft Edge, которое работает на эмуляторе</span><span class="sxs-lookup"><span data-stu-id="cf13f-141">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>
:::image-end:::  

<span data-ttu-id="cf13f-142">Выберите **для** проверки вкладку или PWA, которую необходимо отладить, чтобы открыть [Microsoft Edge DevTools.][DevToolsChromiumGuide]</span><span class="sxs-lookup"><span data-stu-id="cf13f-142">Choose **inspect** for the tab or PWA that you want to debug to open the [Microsoft Edge DevTools][DevToolsChromiumGuide].</span></span>  <span data-ttu-id="cf13f-143">[Следуйте пошаговому][DevToolsRemoteDebugDuoEmulator]руководству по удаленной отладки веб-контента в эмуляторе Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="cf13f-143">[Follow the step-by-step guide to remotely debug your web content on the Surface Duo emulator][DevToolsRemoteDebugDuoEmulator].</span></span>  

### <a name="resize-the-devtools-drawer-more-easily"></a><span data-ttu-id="cf13f-144">Более простое решение по окантовке ящика DevTools</span><span class="sxs-lookup"><span data-stu-id="cf13f-144">Resize the DevTools drawer more easily</span></span>  

<span data-ttu-id="cf13f-145">В Microsoft Edge 83 или ранее можно было только повторно использовать [ящик DevTools,][DevToolsDrawer] зависая в панели инструментов ящика.</span><span class="sxs-lookup"><span data-stu-id="cf13f-145">In Microsoft Edge 83 or earlier, you were only able to resize the [DevTools Drawer][DevToolsDrawer] by hovering inside the toolbar of the Drawer.</span></span>  <span data-ttu-id="cf13f-146">Ящик вел себя по-другому, чем другие элементы управления, меняя их для стекол в DevTools, где вы наведите курсор на границе области, чтобы повторно ее использовать.</span><span class="sxs-lookup"><span data-stu-id="cf13f-146">The Drawer behaved differently than the other resize controls for panes in the DevTools where you hover on the border of the pane to resize it.</span></span>  <span data-ttu-id="cf13f-147">Выберите следующее изображение, чтобы отобразить, как работал ящик в версии 83 или более ранней версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf13f-147">Choose the following image to display how resizing the Drawer worked in version 83 or earlier of Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Размер ящика DevTools в Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   <span data-ttu-id="cf13f-149">Размер ящика DevTools в Microsoft Edge 83</span><span class="sxs-lookup"><span data-stu-id="cf13f-149">Resizing the DevTools Drawer in Microsoft Edge 83</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="cf13f-150">Начиная с Microsoft Edge 84, теперь вы можете повторно использовать ящик, зависая над границей ящика.</span><span class="sxs-lookup"><span data-stu-id="cf13f-150">Starting with Microsoft Edge 84, you are now able to resize the Drawer by hovering over the border of the Drawer.</span></span>  <span data-ttu-id="cf13f-151">Это изменение выравнивает поведение, меняющее размер ящика DevTools, с способом изменения размеров других стекол в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-151">This change aligns the behavior resizing the DevTools Drawer with the way you resize other panes in the DevTools.</span></span>  <span data-ttu-id="cf13f-152">Выберите следующее изображение для отображения размеров в действии в Microsoft Edge 84.</span><span class="sxs-lookup"><span data-stu-id="cf13f-152">Choose the following image to display resizing in action in Microsoft Edge 84.</span></span>  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Размер ящика DevTools в Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   <span data-ttu-id="cf13f-154">Размер ящика DevTools в Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="cf13f-154">Resizing the DevTools Drawer in Microsoft Edge 84</span></span>
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

<span data-ttu-id="cf13f-155">Проблема Chromium [#1076112][CR1076112]</span><span class="sxs-lookup"><span data-stu-id="cf13f-155">Chromium issue [#1076112][CR1076112]</span></span>  

### <a name="screencasting-navigation-buttons-display-focus"></a><span data-ttu-id="cf13f-156">Экранизация навигационных кнопок отображения фокуса</span><span class="sxs-lookup"><span data-stu-id="cf13f-156">Screencasting navigation buttons display focus</span></span>  

<span data-ttu-id="cf13f-157">При удаленном отладке android-устройства, устройства [Windows 10][DevToolsRemoteDebugWindows]или эмулятора [Surface Duo][DevToolsRemoteDebugDuoEmulator]можно отладить скринкастинг с помощью значка Toggle Screencast в левом верхнем углу [][DevToolsRemoteDebugAndroid] ![ ][ImageScreencastingIcon] DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-157">When remote debugging an [Android device][DevToolsRemoteDebugAndroid], a [Windows 10 device][DevToolsRemoteDebugWindows], or a [Surface Duo emulator][DevToolsRemoteDebugDuoEmulator], you are able to toggle screencasting with the ![Toggle Screencast][ImageScreencastingIcon] icon in the top-left corner of the DevTools.</span></span>  <span data-ttu-id="cf13f-158">Благодаря включенной экранной трансляции вы можете перемещать вкладку в Microsoft Edge на удаленном устройстве из окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="cf13f-158">With screencasting enabled, you are able to navigate the tab in Microsoft Edge on the remote device from the DevTools window.</span></span>  <span data-ttu-id="cf13f-159">В Microsoft Edge 84 эти кнопки навигации теперь также доступны для клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="cf13f-159">In Microsoft Edge 84, these navigation buttons are now also keyboard accessible.</span></span>  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Выберите Shift+Tab из экранируемой панели URL-адресов с фокусом на кнопке Обновление" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   <span data-ttu-id="cf13f-161">Выберите `Shift` + `Tab` из экранируемой панели URL-адресов фокус на кнопке **Обновление**</span><span class="sxs-lookup"><span data-stu-id="cf13f-161">Select `Shift`+`Tab` from the screencasted URL bar shows focus on the **Refresh** button</span></span>
:::image-end:::  

<span data-ttu-id="cf13f-162">Проблема Chromium [#1081486][CR1081486]</span><span class="sxs-lookup"><span data-stu-id="cf13f-162">Chromium issue [#1081486][CR1081486]</span></span>  

### <a name="network-panel-details-pane-is-now-accessible"></a><span data-ttu-id="cf13f-163">Теперь доступна панель сведений о панели сети</span><span class="sxs-lookup"><span data-stu-id="cf13f-163">Network panel Details pane is now accessible</span></span>  

<span data-ttu-id="cf13f-164">В Microsoft Edge 84 поле [Details][DevToolsNetworkDetails] в средстве **Network** теперь фокусируется при его открываемом ресурсе в [сетевом журнале.][DevToolsNetworkLog]</span><span class="sxs-lookup"><span data-stu-id="cf13f-164">In Microsoft Edge 84, the [Details pane][DevToolsNetworkDetails] in the **Network** tool now takes focus when you open it for a resource in the [Network Log][DevToolsNetworkLog].</span></span>  <span data-ttu-id="cf13f-165">Это изменение позволяет читателям экрана читать и взаимодействовать с содержимым области **Details.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-165">This change allows screen readers to read out and interact with the content of the **Details** pane.</span></span>  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="Панель Details в панели Network фокусируется при открываемом" lightbox="../../media/2020/05/network-details.msft.png":::
   <span data-ttu-id="cf13f-167">Области **подробностей** в **средстве Network** фокусируется при открываемом</span><span class="sxs-lookup"><span data-stu-id="cf13f-167">The **Details** pane in the **Network** tool takes focus when opened</span></span>
:::image-end:::  

<span data-ttu-id="cf13f-168">Проблема Chromium [#963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="cf13f-168">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="cf13f-169">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="cf13f-169">Announcements from the Chromium project</span></span>  

<span data-ttu-id="cf13f-170">В следующих разделах представлены дополнительные функции, доступные в Microsoft Edge 84, которые были внесены в проект Chromium с открытым исходным кодом.</span><span class="sxs-lookup"><span data-stu-id="cf13f-170">The following sections announce additional features available in Microsoft Edge 84 that were contributed to the open source Chromium project.</span></span>  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a><span data-ttu-id="cf13f-171">Устранение проблем с сайтом с помощью нового средства "Проблемы" в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="cf13f-171">Fix site issues with the new Issues tool in the DevTools Drawer</span></span>

<span data-ttu-id="cf13f-172">Новый инструмент **Issues** в ящике DevTools был создан, чтобы уменьшить усталость уведомлений и захламление **консоли.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-172">The new **Issues** tool in the DevTools Drawer was built to help reduce the notification fatigue and clutter of the **Console**.</span></span>  <span data-ttu-id="cf13f-173">В **настоящее** время консоль является центральным местом для разработчиков веб-сайтов, библиотек, рамок и Microsoft Edge для журналов сообщений, предупреждений и ошибок.</span><span class="sxs-lookup"><span data-stu-id="cf13f-173">Currently, the **Console** is the central place for website developers, libraries, frameworks, and Microsoft Edge to log messages, warnings, and errors.</span></span>  <span data-ttu-id="cf13f-174">Средство **Issues** собирает предупреждения из браузера структурированным, агрегируемым и действий способом ссылок на затронутые ресурсы в Microsoft Edge DevTools и предоставляет рекомендации по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="cf13f-174">The **Issues** tool aggregates warnings from the browser in a structured, aggregated, and actionable way, links to affected resources within Microsoft Edge DevTools, and provides guidance on how to fix the issues.</span></span>  <span data-ttu-id="cf13f-175">Со временем все больше и больше предупреждений \*\*\*\* в Microsoft Edge в инструменте Проблемы, а не консоли **,** которые должны помочь уменьшить беспорядок в **консоли**.</span><span class="sxs-lookup"><span data-stu-id="cf13f-175">Over time, more and more warnings are surfaced in Microsoft Edge in the **Issues** tool rather than the **Console**, which should help reduce the clutter in the **Console**.</span></span>  

<span data-ttu-id="cf13f-176">Чтобы начать работу, перейдите к поиску и устранению проблем с помощью средства [Microsoft Edge DevTools Issues.][DevtoolsIssuesIndex]</span><span class="sxs-lookup"><span data-stu-id="cf13f-176">To get started, navigate to [Find And Fix Problems With The Microsoft Edge DevTools Issues tool][DevtoolsIssuesIndex].</span></span>  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="Средство Проблемы в ящике DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   <span data-ttu-id="cf13f-178">Средство **Проблемы** в ящике DevTools</span><span class="sxs-lookup"><span data-stu-id="cf13f-178">The **Issues** tool in the DevTools Drawer</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-179">Проблема Chromium [#1068116][CR1068116]</span><span class="sxs-lookup"><span data-stu-id="cf13f-179">Chromium issue [#1068116][CR1068116]</span></span>  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a><span data-ttu-id="cf13f-180">Просмотр сведений о доступности в инструменте Inspect Mode</span><span class="sxs-lookup"><span data-stu-id="cf13f-180">View accessibility information in the Inspect Mode tooltip</span></span>  

<span data-ttu-id="cf13f-181">В **инструменте Inspect Mode** теперь указывается, имеет [][WebhintHintsAxeNameRoleValue] ли элемент доступное имя и роль и является ли он [фокусируемым на клавиатуре.][WebhintHintsAxeKeyboard]</span><span class="sxs-lookup"><span data-stu-id="cf13f-181">The **Inspect Mode** tooltip now indicates whether the element has an accessible [name and role][WebhintHintsAxeNameRoleValue] and is [keyboard-focusable][WebhintHintsAxeKeyboard].</span></span>  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Средство Inspect Mode с сведениями о доступности" lightbox="../../media/2020/05/a11y.msft.png":::
  <span data-ttu-id="cf13f-183">Средство **Inspect Mode** с сведениями о доступности</span><span class="sxs-lookup"><span data-stu-id="cf13f-183">The **Inspect Mode** tooltip with accessibility information</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-184">Проблема Chromium [#1040025][CR1040025]</span><span class="sxs-lookup"><span data-stu-id="cf13f-184">Chromium issue [#1040025][CR1040025]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="cf13f-185">Обновления панели производительности</span><span class="sxs-lookup"><span data-stu-id="cf13f-185">Performance panel updates</span></span>  

#### <a name="view-total-blocking-time-information-in-the-footer"></a><span data-ttu-id="cf13f-186">Просмотр сведений о времени блокировки в подножке</span><span class="sxs-lookup"><span data-stu-id="cf13f-186">View Total Blocking Time information in the footer</span></span>  

<span data-ttu-id="cf13f-187">После записи производительности нагрузки панель **Performance** теперь отображает сведения об общем времени блокировки \(TBT\) в подножке.</span><span class="sxs-lookup"><span data-stu-id="cf13f-187">After recording your load performance, the **Performance** panel now shows Total Blocking Time \(TBT\) information in the footer.</span></span>  <span data-ttu-id="cf13f-188">TBT — это показатель производительности нагрузки, который позволяет количественно определить, сколько времени занимает страница, чтобы стать полезной.</span><span class="sxs-lookup"><span data-stu-id="cf13f-188">TBT is a load performance metric that helps quantify how long a page takes to become usable.</span></span>  <span data-ttu-id="cf13f-189">В нем по существу измеряется, как долго страница может быть использовать \(так как содержимое отображается на экране\); но на самом деле не может быть удобным, так как JavaScript блокирует основной поток и поэтому страница не реагирует на ввод пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf13f-189">It essentially measures how long a page appears to be usable \(because the content is rendered to the screen\); but is not actually usable, because JavaScript is blocking the main thread and therefore the page does not respond to user input.</span></span>  <span data-ttu-id="cf13f-190">TBT является основным показателем для приближения первой задержки ввода.</span><span class="sxs-lookup"><span data-stu-id="cf13f-190">TBT is the main metric for approximating First Input Delay.</span></span>  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

<span data-ttu-id="cf13f-191">Чтобы получить сведения о времени блокировки, не используйте **значок** обновления страницы обновления страницы для записи производительности ![ ][ImageRefreshPageIcon] загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="cf13f-191">To get Total Blocking Time information, do not use the **Refresh Page** ![Refresh page icon][ImageRefreshPageIcon] workflow for recording page load performance.</span></span>  

<span data-ttu-id="cf13f-192">Вместо этого выберите **значок Запись** записи, вручную перезагрузите страницу, подождите загрузку страницы ![ и ][ImageRecordIcon] прекратите запись.</span><span class="sxs-lookup"><span data-stu-id="cf13f-192">Instead, select **Record** ![Record icon][ImageRecordIcon], manually reload the page, wait for the page to load, and then stop recording.</span></span>  

<span data-ttu-id="cf13f-193">Если отображается, Microsoft Edge DevTools не получают необходимые сведения из внутренних данных `Total Blocking Time: Unavailable` профилирование в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cf13f-193">If `Total Blocking Time: Unavailable` is displayed, Microsoft Edge DevTools did not get the required information from the internal profiling data in Microsoft Edge.</span></span>  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Общая информация о времени блокировки в подножке записи панели Performance" lightbox="../../media/2020/05/tbt.msft.png":::
   <span data-ttu-id="cf13f-195">Общая информация о времени блокировки в подножке записи панели **Performance**</span><span class="sxs-lookup"><span data-stu-id="cf13f-195">Total Blocking Time information in the footer of a **Performance** panel recording</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-196">Проблема Chromium [#1054381][CR1054381]</span><span class="sxs-lookup"><span data-stu-id="cf13f-196">Chromium issue [#1054381][CR1054381]</span></span>  

#### <a name="layout-shift-events-in-the-new-experience-section"></a><span data-ttu-id="cf13f-197">События переноса макета в новом разделе Experience</span><span class="sxs-lookup"><span data-stu-id="cf13f-197">Layout Shift events in the new Experience section</span></span>  

<span data-ttu-id="cf13f-198">Новый раздел **Experience** панели **Performance** помогает обнаруживать сдвиги макета.</span><span class="sxs-lookup"><span data-stu-id="cf13f-198">The new **Experience** section of the **Performance** panel helps you detect layout shifts.</span></span>  <span data-ttu-id="cf13f-199">Накопительная смена макета \(CLS\) — это метрика, которая помогает количественно оценить нежелательную визуальную нестабильность.</span><span class="sxs-lookup"><span data-stu-id="cf13f-199">Cumulative Layout Shift \(CLS\) is a metric that helps you quantify unwanted visual instability.</span></span>

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

<span data-ttu-id="cf13f-200">Выберите событие **Перенос макета,** чтобы отобразить сведения о переносе макета в области **Сводка.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-200">Choose the **Layout Shift** event to display the details of the layout shift in the **Summary** pane.</span></span>  <span data-ttu-id="cf13f-201">Наведите курсор на **перемещении** и **перемещении** в поля, чтобы визуализировать место, где произошла смена макета.</span><span class="sxs-lookup"><span data-stu-id="cf13f-201">Hover on the **Moved from** and **Moved to** fields to visualize where the layout shift occurred.</span></span>  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Сведения о переносе макета" lightbox="../../media/2020/05/cls.msft.png":::
   <span data-ttu-id="cf13f-203">Сведения о переносе макета</span><span class="sxs-lookup"><span data-stu-id="cf13f-203">The details of a layout shift</span></span>  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a><span data-ttu-id="cf13f-204">Более точная терминология обещаний в консоли</span><span class="sxs-lookup"><span data-stu-id="cf13f-204">More accurate promise terminology in the Console</span></span>  

<span data-ttu-id="cf13f-205">При входе в журнал консоли неправильно `Promise` при условии \*\*\*\* `PromiseStatus` значения, установленного `resolved` для .</span><span class="sxs-lookup"><span data-stu-id="cf13f-205">When logging a `Promise`, the **Console** incorrectly provided `PromiseStatus` value set to `resolved`.</span></span>  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Пример консоли с использованием старой разрешенной терминологии" lightbox="../../media/2020/05/resolved.msft.png":::
   <span data-ttu-id="cf13f-207">Пример консоли **с использованием** старой `resolved` терминологии</span><span class="sxs-lookup"><span data-stu-id="cf13f-207">An example of the **Console** using the old `resolved` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-208">Консоль **теперь** использует термин `fulfilled` , который соответствует `Promise` спецификации.</span><span class="sxs-lookup"><span data-stu-id="cf13f-208">The **Console** now uses the term `fulfilled`, which aligns with the `Promise` specification.</span></span>  <span data-ttu-id="cf13f-209">Дополнительные сведения о `Promise` спецификации перейдите в [Штаты и судьбы на GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span><span class="sxs-lookup"><span data-stu-id="cf13f-209">For more information about the `Promise` specification, navigate to [States and Fates on GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).</span></span>  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Пример консоли с использованием новой терминологии" lightbox="../../media/2020/05/fulfilled.msft.png":::
  <span data-ttu-id="cf13f-211">Пример консоли **с** использованием новой `fulfilled` терминологии</span><span class="sxs-lookup"><span data-stu-id="cf13f-211">An example of the **Console** using the new `fulfilled` terminology</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-212">Выпуск V8 [#6751][CRV86751]</span><span class="sxs-lookup"><span data-stu-id="cf13f-212">V8 issue [#6751][CRV86751]</span></span>  

### <a name="styles-pane-updates"></a><span data-ttu-id="cf13f-213">Обновления области стилей</span><span class="sxs-lookup"><span data-stu-id="cf13f-213">Styles pane updates</span></span>  

#### <a name="support-for-the-revert-keyword"></a><span data-ttu-id="cf13f-214">Поддержка ключевого слова revert</span><span class="sxs-lookup"><span data-stu-id="cf13f-214">Support for the revert keyword</span></span>  

<span data-ttu-id="cf13f-215">Пользовательский интерфейс автокомплекта области **Стилей** обнаруживает ключевое слово [][MDNRevert] CSS, которое возвращает каскадное значение свойства к предыдущему значению, примененному к стилю элемента.</span><span class="sxs-lookup"><span data-stu-id="cf13f-215">The autocomplete UI of the **Styles** pane now detects the [revert][MDNRevert] CSS keyword, which reverts the cascaded value of a property to the previous value applied to the styling of the element.</span></span>  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Настройка значения свойства для повторного" lightbox="../../media/2020/05/revert.msft.png":::
  <span data-ttu-id="cf13f-217">Настройка значения свойства для повторного</span><span class="sxs-lookup"><span data-stu-id="cf13f-217">Setting the value of a property to revert</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-218">Проблема Chromium [#1075437][CR1075437]</span><span class="sxs-lookup"><span data-stu-id="cf13f-218">Chromium issue [#1075437][CR1075437]</span></span>  

#### <a name="image-previews"></a><span data-ttu-id="cf13f-219">Предварительные просмотры изображений</span><span class="sxs-lookup"><span data-stu-id="cf13f-219">Image previews</span></span>  

<span data-ttu-id="cf13f-220">Наведите курсор на значение в области Стилей, чтобы отобразить предварительный просмотр изображения `background-image` в панели инструментов. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cf13f-220">Hover on a `background-image` value in the **Styles** pane to display a preview of the image in a tooltip.</span></span>  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Наведении на фоновое значение изображения" lightbox="../../media/2020/05/image-preview.msft.png":::
  <span data-ttu-id="cf13f-222">Наведении над `background-image` значением</span><span class="sxs-lookup"><span data-stu-id="cf13f-222">Hovering over a `background-image` value</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-223">Проблема Chromium [#1040019][CR1040019]</span><span class="sxs-lookup"><span data-stu-id="cf13f-223">Chromium issue [#1040019][CR1040019]</span></span>  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a><span data-ttu-id="cf13f-224">В color Picker теперь используется функциональная нотация с раздельным пространством</span><span class="sxs-lookup"><span data-stu-id="cf13f-224">Color Picker now uses space-separated functional color notation</span></span>  

<span data-ttu-id="cf13f-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] указывает, что цветовые функции, например, должны поддерживать аргументы, разделенные `rgb()` пространством.</span><span class="sxs-lookup"><span data-stu-id="cf13f-225">[CSS Color Module Level 4][CSSWGDraftsColor4Changes3] specifies that color functions, such as `rgb()`, should support space-separated arguments.</span></span>  <span data-ttu-id="cf13f-226">Например, команда `rgb(0, 0, 0)` эквивалентна `rbg(0 0 0)`.</span><span class="sxs-lookup"><span data-stu-id="cf13f-226">For example, `rgb(0, 0, 0)` is equivalent to `rbg(0 0 0)`.</span></span>  

<span data-ttu-id="cf13f-227">Когда вы выбираете [][DevtoolsCssReferenceColorPicker] цвета с помощью выбора цвета или чередуется между представлениями цветов в области **Стилей,** удерживая и выбирая значение, отображается синтаксис аргументов, разделенных `Shift` `background-color` пробелами.</span><span class="sxs-lookup"><span data-stu-id="cf13f-227">When you choose colors with the [Color Picker][DevtoolsCssReferenceColorPicker] or alternate between color representations in the **Styles** pane by holding `Shift` and selecting the `background-color` value, the space-separated argument syntax is displayed.</span></span>  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Использование аргументов, разделенных пространством, в области Стилей" lightbox="../../media/2020/05/color.msft.png":::
  <span data-ttu-id="cf13f-229">Использование аргументов, разделенных пространством, в области **Стилей**</span><span class="sxs-lookup"><span data-stu-id="cf13f-229">Using space-separated arguments in the **Styles** pane</span></span>  
:::image-end:::  

<span data-ttu-id="cf13f-230">Кроме того, необходимо отобразить синтаксис в **области Computed** и **инструментарий Режима** проверки.</span><span class="sxs-lookup"><span data-stu-id="cf13f-230">You should also display the syntax in the **Computed** pane and the **Inspect Mode** tooltip.</span></span>  

<span data-ttu-id="cf13f-231">Microsoft Edge DevTools использует новый синтаксис, так как предстоящие функции CSS, такие как [color()][CSSWGDraftsColor4Property] не поддерживают синтаксис аргументов, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="cf13f-231">Microsoft Edge DevTools is using the new syntax because upcoming CSS features such as [color()][CSSWGDraftsColor4Property] do not support the deprecated comma-separated argument syntax.</span></span>  

<span data-ttu-id="cf13f-232">Синтаксис аргументов, разделенных пробелами, некоторое время поддерживался в большинстве браузеров.</span><span class="sxs-lookup"><span data-stu-id="cf13f-232">The space-separated argument syntax has been supported in most browsers for a while.</span></span>  <span data-ttu-id="cf13f-233">Дополнительные сведения можно найти в [раздел "Можно ли использовать: функциональные нотации, разделенные пробелами"?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span><span class="sxs-lookup"><span data-stu-id="cf13f-233">For more information, navigate to [Can I use: Space-separated functional color notations?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]</span></span>  

<span data-ttu-id="cf13f-234">Проблема Chromium [#1072952][CR1072952]</span><span class="sxs-lookup"><span data-stu-id="cf13f-234">Chromium issue [#1072952][CR1072952]</span></span>  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a><span data-ttu-id="cf13f-235">Обесценение области свойств в панели Elements</span><span class="sxs-lookup"><span data-stu-id="cf13f-235">Deprecation of the Properties pane in the Elements panel</span></span>  

<span data-ttu-id="cf13f-236">Области **свойств** в **инструменте Elements** отстает.</span><span class="sxs-lookup"><span data-stu-id="cf13f-236">The **Properties** pane in the **Elements** tool is deprecated.</span></span>  <span data-ttu-id="cf13f-237">Вместо `console.dir($0)` этого **запустите в консоли.**</span><span class="sxs-lookup"><span data-stu-id="cf13f-237">Run `console.dir($0)` in the **Console** instead.</span></span>  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="Неуловимая панорама свойств" lightbox="../../media/2020/05/properties.msft.png":::
   <span data-ttu-id="cf13f-239">Неуловимая **панорама свойств**</span><span class="sxs-lookup"><span data-stu-id="cf13f-239">The deprecated **Properties** pane</span></span>  
:::image-end:::  

#### <a name="references"></a><span data-ttu-id="cf13f-240">Ссылки</span><span class="sxs-lookup"><span data-stu-id="cf13f-240">References</span></span>  

*   [<span data-ttu-id="cf13f-241">console.dir()</span><span class="sxs-lookup"><span data-stu-id="cf13f-241">console.dir()</span></span>][DevtoolsConsoleApiDir]  
*   [<span data-ttu-id="cf13f-242">$0</span><span class="sxs-lookup"><span data-stu-id="cf13f-242">$0</span></span>][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a><span data-ttu-id="cf13f-243">Поддержка ярлыков приложений в области Манифест</span><span class="sxs-lookup"><span data-stu-id="cf13f-243">App shortcuts support in the Manifest pane</span></span>  

<span data-ttu-id="cf13f-244">Ярлыки приложений помогают пользователям быстро приступить к общим или рекомендуемым задачам в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="cf13f-244">App shortcuts help users quickly start common or recommended tasks within a web app.</span></span>  <span data-ttu-id="cf13f-245">Меню ярлыков приложения отображается только [][PwaIndex] для прогрессивных веб-приложений, установленных на рабочем столе или мобильном устройстве пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf13f-245">The app shortcuts menu is shown only for [Progressive Web Apps][PwaIndex] that are installed on the user's desktop or mobile device.</span></span>  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Ярлыки приложения в области Манифест" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  <span data-ttu-id="cf13f-247">Ярлыки приложения в **области Манифест**</span><span class="sxs-lookup"><span data-stu-id="cf13f-247">App shortcuts in the **Manifest** pane</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="cf13f-248">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="cf13f-248">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="cf13f-249">Если вы находитесь на Windows или macOS, рассмотрите возможность использования каналов [предварительного][MicrosoftEdgePreviewChannels] просмотра Microsoft Edge в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf13f-249">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="cf13f-250">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="cf13f-250">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="cf13f-251">Контакт с командой Microsoft Edge Devtools</span><span class="sxs-lookup"><span data-stu-id="cf13f-251">Getting in touch with Microsoft Edge Devtools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Используйте эмулятор Surface Duo | Документы Майкрософт"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir — справочные | Документы Майкрософт"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Недавно выбранный элемент или объект JavaScript — справочные ссылки на API консоли | Документы Майкрософт"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Измените цвета с помощью выборки цвета — CSS Reference | Документы Майкрософт"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Ящик — настройка | Документы Майкрософт"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Средства разработки Microsoft Edge (Chromium) | Документы Майкрософт"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Поиск и устранение проблем с вкладками Microsoft Edge DevTools | Документы Майкрософт"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленной отладки android-устройств | Документы Майкрософт"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Начало работы с эмуляторами Surface Duo удаленного отладки | Документы Майкрософт"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладки устройств Windows 10 | Документы Майкрософт"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Проверка сведений о | Документы Майкрософт"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Журнал сетевой активности | Документы Майкрософт"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в Windows | Документы Майкрософт"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge Android app"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Разделенные пространством функциональные цветовые нотации — MDN | Могу ли я использовать"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: разрешить настраивать клавиши ярлыков и привязки клавиш | Ошибки Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools не соответствуют требованиям WCAG | Ошибки Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: легко просматривать изображения и фоновые изображения в области стилей | Ошибки Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: показать основные сведения a11y в элементе popover | Ошибки Chromium"  
[CR1048378]: https://crbug.com/1048378 "Поддержка пользовательского интерфейса DevTools для режима высокой контрастности | Ошибки Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Ошибки Chromium"  
[CR1068116]: https://crbug.com/1068116 "Панель проблем корабля | Ошибки Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: выбор цвета должен производить современный синтаксис цвета CSS | Ошибки Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: добавьте поддержку ключевого слова/значения CSS для | Ошибки Chromium"  
[CR1076112]: https://crbug.com/1076112 "Персонализация Devtools — resizer ящика"  
[CR1081486]: https://crbug.com/1081486 "Фокус клавиатуры не виден для кнопок навигации в режиме screencast | Ошибки Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus должен быть "выполнен", а не "разрешен" | Ошибки V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Изменения из цветов 3 — CSS Color Module Level 4 | Проекты редактора рабочей группы W3C CSS"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Цвет переднего плана: "цвет" - CSS Color Module Level 4 | Проекты редактора рабочей группы W3C CSS"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Представление нового microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Состояния и судьбы — domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "повторное | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Совместимость браузера | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Код"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio клавиши кода для Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: клавиатура | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Значение роли имени | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Включить или отключить режим высокой контрастности в Windows | Поддержка Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема — MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительного просмотра Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Веб-сайт, который мы хотим"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> <span data-ttu-id="cf13f-296">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf13f-296">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cf13f-297">Оригинальная страница [](https://developers.google.com/web/updates/2020/05/devtools/index) находится здесь и является автором [Kayce Basques][KayceBasques] \(Технический писатель, Chrome DevTools \& Маяк\).</span><span class="sxs-lookup"><span data-stu-id="cf13f-297">The original page is found [here](https://developers.google.com/web/updates/2020/05/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cf13f-299">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cf13f-299">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
